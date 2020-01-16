<template>
  <div id="app">
    <div id="nav">
      <nav>
          <router-link to="/"><h2>Pronađi dadilju</h2></router-link>
        <ul>
          <li><router-link to="/">Početna</router-link></li>
          <li><router-link v-if="!authenticated" to="/Prijava">Prijava</router-link></li>
          <li><router-link v-if="!authenticated" to="/Registracija">Registracija</router-link></li>
          <li><router-link v-if="authenticated" to="/profil">Moj profil</router-link></li>
          <li><router-link v-if="authenticated" to="/Naslovna">Naslovna</router-link></li>
          <li><router-link v-if="authenticated" to="/Trazilica">Tražilica</router-link></li>
          {{userEmail}}
          <li v-if="authenticated">
            <a @click.prevent="logout" href="#">Odjava</a>
          </li>
        </ul>
      </nav>
    </div>
    <router-view/>
  </div>
</template>

<script>
import store from '@/store.js'
export default {
  data (){
    return store;
  },

  methods: {
    logout() {
      firebase.auth().signOut();
    }
  },
  
  mounted() {
    const self = this;
    firebase.auth().onAuthStateChanged(function(user) {
      if (user) {
        self.userEmail = user.email;
        self.authenticated = true;

        db.collection("roditelj")
        .doc(self.userEmail)
        .get()
        .then(doc => {
          if (doc.exists) {
            console.log("Document data:", doc.data());
            self.ime = doc.data().ime;
            self.prezime = doc.data().prezime;
            self.kontakt = doc.data().kontakt;
            self.brojdjece = doc.data().broj;
            self.tip = doc.data().tip;
            self.grad = doc.data().grad;
          } else {
            // doc.data() will be undefined in this case
            console.log("No such document!");
          }
        });
        db.collection("dadilja")
        .doc(self.userEmail)
        .get()
        .then(doc => {
          if (doc.exists) {
            console.log("Document data:", doc.data());
            self.ime = doc.data().ime;
            self.prezime = doc.data().prezime;
            self.kontakt = doc.data().kontakt;
            self.grad = doc.data().grad;
            self.tip = doc.data().tip;
            self.iskustvo = doc.data().iskustvo;
            self.ostalo = doc.data().ostalo;
            self.brojgodina = doc.data().brojgodina;
            self.mjestocuvanjadjece = doc.data().mjestocuvanjadjece;
            self.spol = doc.data().spol;
            self.dozvola = doc.data().dozvola;

          } else {
            // doc.data() will be undefined in this case
            console.log("No such document!");
          }
        });
        
        console.log(`Authenticated: ${self.userEmail}`)
        if (self.$route.name !== 'Naslovna')
          self.$router.push({name: 'Naslovna'})
      }
      else {
        self.authenticated = false
        console.log('Logged out')
        if (self.$route.name !== 'Home')
          self.$router.push({name: 'Home'})
      }
    });
   db.collection("objave").orderBy("posted_at")
      .onSnapshot(snapshot => {
        snapshot.docChanges().forEach(change => {
          const data = change.doc.data()
          if (change.type !== "added") return
            const karla = {id: change.doc.id,  tekst: data.tekst, ime: data.ime,prezime: data.prezime, naslov: data.naslov, posted_at: data.posted_at}
            self.postovi.unshift(karla)
        });
    });

    
  }
}
</script>

<style lang="scss">
#nav h2 {
	margin: auto;
  color:white;
	display: inline;
  font-family: Arial, Helvetica, sans-serif;
  text-shadow: -1px 0 black, 0 1px black, 1px 0 black, 0 -1px black;
}

nav ul {
	margin: 0;
	float: right;
}

nav ul li{
	font-size: 20px;
	color: white;
	display: inline;
	list-style-type: none;
	padding: 9px 15px;
  text-shadow: -1px 0 black, 0 1px black, 1px 0 black, 0 -1px black;
}


#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
 nav{
	 display: flex;
	 align-items: center;
	 justify-content: space-around;
 }

#nav {
  background:lightsteelblue;
	padding: 0.9% 0;

  a {
    font-weight: bold;
    color: lightslategray;
    text-decoration: none;

    &.router-link-exact-active {
      color: white;
    }
  }
}
</style>
