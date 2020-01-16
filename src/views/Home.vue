<template>
  <div class="home">
    <div class="row"> 
    <div class="col-sm-6"><img class="naslovna" src="naslovna.jpg" alt="dadilja i dijete"> </div>
    <div class="col-sm-6">
      <div class="tekst">
        <h4><h1><strong>Dobrodošli u aplikaciju <span style="color:#f77299;">Pronađi dadilju.</span></strong></h1> Aplikacija je namjenjena roditeljima koji traže dadilju te dadiljama koje traže posao.
        Ako ste zainteresirani za jedno ili drugo ovo je pravo mjesto za vas.</h4>
        <router-link to="/Prijava"><button>Prijava</button></router-link>
        <router-link to="/Registracija"><button>Registracija</button></router-link>
      </div>
      </div>
    </div>
    </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'Home',
  components: {
    HelloWorld
  }
}
</script>
 
<style scoped>
   button{
     margin: 8%;
     font-size: 150%; 
     font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
     color:#2c3e50;
     border-radius: 20px;
     padding: 2% 10%;
     background-color:lightsteelblue;
     text-shadow: -1px 0 black, 0 1px black, 1px 0 black, 0 -1px black; 
   }
    button:hover{
     box-shadow: 9px 9px 7px gray;
     background-color: #5c7a99;

    }
  .tekst{
    width: 80%;
    font-family:'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
    margin-top: 15%;
  }

  .tekst h1{
    margin-bottom: 5%;
  }
  .tekst h4{
    line-height: 150%;

  }
  
  .row{
    max-width: 100%;
  }
  
  .naslovna{ 
    width: 80%;
    align-items: center;
    margin-top: 10%;
    box-shadow: 10px 10px 5px gray;
    border-radius: 20%;

 
  }
</style>