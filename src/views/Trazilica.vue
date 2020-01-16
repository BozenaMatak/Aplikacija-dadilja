<template>
    <div>
        <form>
            <div class="row">
                <div class="form-group">
                    <h5>Pretraži po gradu: </h5>  
                    <select v-model="searchterm" class="form-control form-control-lg">
                        <option :key="g.id" v-for="g in gradovi">{{g}}</option>
                    </select>
                    <button type="submit" class="btn btn-primary">Traži</button>
                </div>
            </div>   
        </form>
        <Pretrazenprofil :key="pretrazi.id" :podatak="pretrazi" v-for="pretrazi in filteredCards"/>
        
    </div>  
</template>


<script>
import store from '@/store.js'
import Pretrazenprofil from '@/components/Pretrazenprofil.vue'
export default {

    data(){
        return store;
    },
    name: 'Trazilica',
  components: {
    Pretrazenprofil
  },
  computed: {
   filteredCards () {
            return this.znj;
        
   }
  },
  mounted(){

    const self=this;
    db.collection("dadilja").where("grad", "==", "Slavonski Brod")
    .onSnapshot(function(snapshot) {
        snapshot.docChanges().forEach(function(change) {
          const data = change.doc.data()
            if (change.type === "added") {
                const pretrazen = {id: change.doc.id, ime: data.ime,prezime: data.prezime, spol:data.spol, brojgodina:data.brojgodina, grad:data.grad, kontakt:data.kontakt, ostalo:data.ostalo}
                self.znj.unshift(pretrazen)
            }
        });
    });

  }
}
</script>

<style scoped>

    .form-group{
    margin: auto;
    clear: both;
    text-align:center;
  }

  select{
    border-radius: 12px;
    width: 150%
    
  }
  .row{
    
    padding: 0;
    margin: 4% 5%;
}
button{
    width: 60%;
    border-radius: 10px;
    font-size: 20px;
}

 

</style>