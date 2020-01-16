<template>
  <div class="profil">
     
    <mojprofil class="mojprofil"/>

  </div>
            
</template>

<script>
import store from '@/store.js'
import mojprofil from '@/components/mojprofil.vue'
export default {

  components: {
    mojprofil
  }
}
</script>

<style scoped>

    .profil{
        margin: 5%;
        width: 30%;
        background-color: white;
        border-radius: 20px;
        padding: 2%;
        font-family: Cambria, Cochin, Georgia, Times, 'Times New Roman', serif;
        float: left;
    
  }
  .mojprofil{
    border: none;

  }
</style>