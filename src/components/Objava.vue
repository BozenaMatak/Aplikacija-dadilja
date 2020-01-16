<template>
    <div class="card text-center" style="margin: auto; width: 30%; margin-bottom: 30px;">

        <div class="card-header text-left">
         <strong>{{ info.ime }} {{info.prezime}}</strong>
        </div> 
        <div class="card-header text-left" style="background-color: white;" >
          <strong>{{info.naslov}}</strong>
        </div>
        <div class="card-body">
          
          {{info.tekst}}
          
        </div>
        <div class="card-footer text-left">
          {{timeAgo}}
        </div>
    </div>
</template>

<script>
import moment from 'moment'
import store from '@/store.js'
export default {
    props: ["info"],
    data () {
     return store;
  },
  
  computed: {
    timeAgo () {
      return moment(this.info.posted_at).fromNow()
    }
  }

}
</script>

<style scoped>



</style>
