<template>
    <div class="card text-center" style="margin:auto; font-size: 20px;">
        <div class="row">
		  <div class="naslov" style="display:inline-block;">
		      <h2>Moj profil</h2>
              <button type="submit" class="btn btn-primary" style="margin-bottom:1%;">Uredi</button>
          </div>
		</div>
        <br>

    <div class="roditelj" v-if="tip==='roditelj'">
      <div class="col-md-12">
        <form>
          <div class="form-group row" >
            <label for="username" class="col-4 col-form-label">Ime</label>
            <div class="col-6">
                {{ime}}
            </div>
          </div>
          <div class="form-group row">
            <label for="name" class="col-4 col-form-label">Prezime</label>
            <div class="col-6">
                {{prezime}}
            </div>
          </div>
          <div class="form-group row">
            <label for="lastname" class="col-4 col-form-label">Grad</label>
            <div class="col-6">
              {{grad}}
            </div>
          </div>
          <div class="form-group row">
            <label for="text" class="col-4 col-form-label">Kontakt broj</label>
            <div class="col-6">
              {{kontakt}}
            </div>
          </div>
          <div class="form-group row">
            <label for="email" class="col-4 col-form-label">Broj djece</label> 
            <div class="col-6">
              {{brojdjece}}
            </div>
          </div>
        </form>
      </div>
    </div>  


    <div class="dadilja" v-if="tip==='dadilja'">
        <div class="col-md-12">
            <form>
                <div class="form-group row">
                    <label for="username" class="col-6 col-form-label">Ime</label> 
                    <div class="col-6">
                    {{ime}}
                    </div>
                </div>
                    <div class="form-group row">
                    <label for="name" class="col-6 col-form-label">Prezime</label> 
                    <div class="col-6">
                        {{prezime}}
                    </div>
                </div>
                <div class="form-group row">
                    <label for="text" class="col-6 col-form-label">Koliko imam godina</label> 
                    <div class="col-6">
                       {{brojgodina}}
                    </div>
                </div>
                <div class="form-group row">
                    <label for="name" class="col-6 col-form-label">Spol</label> 
                    <div class="col-6">
                        {{spol}}
                    </div> 
                    </div>
                <div class="form-group row">
                    <label for="lastname" class="col-6 col-form-label">Grad</label> 
                    <div class="col-6">
                        {{grad}}
                    </div>
                </div>
                <div class="form-group row">
                    <label for="select" class="col-6 col-form-label">Kontakt broj</label>
                    <div class="col-6">
                        {{kontakt}}
                    </div>
                </div>
                <div class="form-group row">
                    <label for="email" class="col-6 col-form-label">Godine iskustva</label>
                    <div class="col-6">
                        {{iskustvo}}
                    </div>
                </div>
                <div class="form-group row">
                    <label for="email" class="col-6 col-form-label">Vozačka dozvola</label>
                    <div class="col-6">
                        {{dozvola}}
                    </div>
                </div>
                <div class="form-group row">
                    <label for="email" class="col-6 col-form-label">Mjesto čuvanja djece</label> 
                    <div class="col-6">
                        {{mjestocuvanjadjece}} 
                    </div>
                </div>
                <div class="form-group row">
                    <label for="email" class="col-6 col-form-label">Ostalo</label> 
                    <p style="white-space: pre-line; font-size: 80%;"></p>
                    <br>
                    <div class="col-6">
                        {{ostalo}}
                    </div>
                </div>
            </form>
        </div>
    </div>
        
    
    </div>
</template>

<script>
import store from '@/store.js'
export default {
    data () {
     return store;
  }

}
</script>

<style scoped>
    
    .naslov{
    border-bottom: 2px solid	#bcbec0;
    width: 80%;
    margin:auto;
    text-align: left;
    }

    button{
        border-radius: 12px;
        width: 50%;
        font-size: 20px;
    }

    textarea{
        font-size: 20px; 
        width: 100%;
        font-family:-apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
    }
    button{
    font-size: 20px;
    border-radius: 10px;
    width: 20%;
    float: right;
    margin: auto;
    background-color: rgb(76, 172, 76);
    border: none;
    margin-top: -7%;

   
  }
</style>