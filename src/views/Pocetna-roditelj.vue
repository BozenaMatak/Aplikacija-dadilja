<template>
  <div class="pocetna-roditelj">
    <div class="roditelj"><img class="naslovna" src="roditelj.jpg" alt="dadilja i dijete">
    </div>
    
      <button type="submit" class="btn btn-primary">Profil</button>
      <button type="submit" class="btn btn-primary">Traži dadilju</button>
      <button type="submit" class="btn btn-primary">Odjava</button>

  </div>
</template>

<style scoped>
    .naslovna{
    width: 45%;
    align-items: center;
    margin-top: 2%;
    }
    button{
    margin-top: 2%;
    margin-left: 3%;
    margin-right: 3%;
     font-size: 140%; 
     padding: 1% 4%;
     font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
     color:#2c3e50;
     border-radius: 20px;
     background-color:lightsteelblue;
     text-shadow: -1px 0 black, 0 1px black, 1px 0 black, 0 -1px black; 
   }
   button:hover{
     box-shadow: 9px 9px 7px gray;
     background-color: #5c7a99;

    }

</style>

