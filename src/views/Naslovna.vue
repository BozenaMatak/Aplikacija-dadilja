<template>
    <div class="naslovna">
      <div v-if="authenticated">
        <form @submit.prevent="Objavi">
            <div class="form-group">
                <p style="white-space: pre-line; font-size: 80%;"></p>
                <div class="kreirajteobjavu">
                    <strong><p>Kreirajte objavu</p></strong>
                </div>
                 <input v-model="naslov" class="naslov" type="text"  placeholder="Unesite naslov">
                <textarea v-model="novaobjava"  type="text" placeholder="Dodajte objavu..." style="font-size: 80%;"></textarea>
            </div>
            <div class="dugme">
                <button class="btn btn primary" style=" background-color:lightsteelblue;" type="submit">Objavi</button>
            </div>   
        </form>
        </div>
        <Objava :key="karla.id" :info="karla" v-for="karla in filteredCards" />
       
    </div>

    
</template>

<script>
    
    import Objava from '@/components/Objava.vue'
    import store from '@/store.js'

export default {
    data(){
        return store;
    },
  name: 'Naslovna',
  components: {
    Objava
  },
  computed: {
   filteredCards () {
    return this.postovi;
   }
  },

  methods: {
    Objavi(){
         db.collection("objave").add({        
          tekst: this.novaobjava,
          ime: this.ime,
          prezime: this.prezime,
          naslov: this.naslov,
          posted_at: Date.now()
        })
    }
  },
 
    
}
</script>

<style scoped>

p {
    margin: 0 5%;
    padding: 2% 0;
    font-size: 16px;
}
  
  form{
    font-size: 20px;
    width: 30%;
    margin: auto;
    margin-top: 2%;
    margin-bottom: 5%;
  }


.form-group{
    clear: both;
    text-align: left;
    margin: 0;
}

.kreirajteobjavu{
    background: rgb(236, 236, 236);
    
}

textarea{
  font-size: 20px; 
  width: 100%;
  font-family: Cambria, Cochin, Georgia, Times, 'Times New Roman', serif;
  border: none;
  margin: 0;
}

.dugme{
     float: left;
     font-family: Cambria, Cochin, Georgia, Times, 'Times New Roman', serif;
     
     

}

.naslov{
  width: 100%;
  font-size: 80%;
  font-family: Cambria, Cochin, Georgia, Times, 'Times New Roman', serif;
  padding: 1.5%;

  
}





</style>