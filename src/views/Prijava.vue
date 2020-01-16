<template>
  <div class="login">
    <div class="naslov">
      <h1>Prijava</h1>
    </div>
    <form @submit.prevent="login">
      <div class="form-group">
        <input v-model="email" type="email" class="form-control" id="exampleInputEmail1" aria-describedby="emailHelp" placeholder="Unesi email">
      </div>
      <div class="form-group">
        <input v-model="password" type="password" class="form-control" id="exampleInputPassword1" placeholder="Unesi lozinku">
      </div>
      <div class="form-group form-check">
        <input type="checkbox" class="form-check-input" id="exampleCheck1">
        <label class="form-check-label" for="exampleCheck1">Zapamti me </label>
      </div>
      <button type="submit" class="btn btn-primary">Prijavi se</button>
    </form>
  </div>
</template>

<script>
export default {
   data (){
    return{
      email:'',
      password:''
    }
  },
  methods: {
    login () {
      firebase.auth().signInWithEmailAndPassword(this.email, this.password).catch(function(error) {
        console.log(error)
      });
    },
  }
 
}
</script>

<style scoped>
  .login{
    width: 30%;
    background-color:rgb(205, 227, 235);
    border-radius: 20px;
    margin: 5% auto;
    padding: 2% 0;
    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
  }
  .naslov{
    border-bottom: 1.5px solid 	#428bca;
    width: 80%;
    margin: auto;
    margin-bottom: 13%;
  }

  form{
    font-size: 20px;
    width: 80%;
    margin: auto;
  }
  .form-group{
    margin: 8% 5%;
    clear: both;
  }
  input{
    border-radius: 12px;
    padding: 6% 4%;
  }
  form button{
    font-size: 20px;
    border-radius: 15px;
    width: 90%;
    margin:auto;
    
  }
</style>

