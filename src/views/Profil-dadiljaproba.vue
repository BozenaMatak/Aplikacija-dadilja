<template>
   <div class="profil">
       <div class="row">
		    <div class="naslov">
		        <h2>Moj profil</h2>
                <button type="submit" class="btn btn-primary">Uredi</button>
                
		    </div>
		</div>
        <div class="dadilja" >
            <div class="col-md-12">
                <form>
                    <div class="form-group row">
                        <label for="username" class="col-4 col-form-label">Ime</label> 
                        <div class="col-6">
                        <input id="username" name="username" class="form-control here" required="required" type="text">
                        </div>
                    </div>
                        <div class="form-group row">
                        <label for="name" class="col-4 col-form-label">Prezime</label> 
                        <div class="col-6">
                            <input id="name" name="name" class="form-control here" type="text">
                        </div>
                    </div>
                    <div class="form-group row">
                        <label for="name" class="col-4 col-form-label">Spol</label> 
                        <div class="col-6">
                            <input id="name" name="name" class="form-control here" type="text"> 
                        </div> 
                        </div>
                    <div class="form-group row">
                        <label for="lastname" class="col-4 col-form-label">Grad</label> 
                        <div class="col-6">
                            <input id="lastname" name="lastname"  class="form-control here" type="text">
                        </div>
                    </div>
                    <div class="form-group row">
                        <label for="text" class="col-4 col-form-label">Koliko imam godina</label> 
                        <div class="col-6">
                            <input id="number" class="form-control here" required="required" type="number">
                        </div>
                    </div>
                    <div class="form-group row">
                        <label for="select" class="col-4 col-form-label">Kontakt broj</label>
                        <div class="col-6">
                            <input id="text" name="text" class="form-control here" required="required" type="text">
                        </div>
                    </div>
                    <div class="form-group row">
                        <label for="email" class="col-4 col-form-label">Vozačka dozvola</label>
                        <div class="col-6">
                            <input id="text" name="text" class="form-control here" required="required" type="text">
                        </div>
                    </div>
                    <div class="form-group row">
                        <label for="email" class="col-4 col-form-label">Mjesto čuvanja djece</label> 
                        <div class="col-6">
                            <input id="text" name="text" class="form-control here" required="required" type="text"> 
                        </div>
                    </div>
                    <div class="form-group row">
                        <label for="email" class="col-4 col-form-label">Iskustvo</label> 
                        <div class="col-6">
                            <input id="email" name="email" class="form-control here" required="required" type="text">
                        </div>
                    </div>
                    <div class="form-group row">
                        <label for="email" class="col-4 col-form-label">Ostalo</label> 
                        <p style="white-space: pre-line; font-size: 80%;"></p>
                        <br>
                        <div class="col-6">
                            <textarea style="font-size: 80%;"></textarea>
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
  },
}
</script>

<style scoped>

    .profil{
        width: 40%;
        margin: 5% auto;
        background-color: white;
        border-radius: 20px;
        margin: 3% 5%;
        padding: 2% 0;
        font-family: Cambria, Cochin, Georgia, Times, 'Times New Roman', serif;
        float: left;
       
    }
    .profil1{
         width: 40%;
        margin: 5% auto;
        background-color: white;
        border-radius: 20px;
        margin: 3% 5%;
        padding: 2% 0;
        font-family: Cambria, Cochin, Georgia, Times, 'Times New Roman', serif;
        float: right;
    }
    .naslov{
    border-bottom: 2px solid	#bcbec0;
    width: 80%;
    margin:auto;
    margin-bottom: 10%;
    text-align: left;
    }


    button{
        border-radius: 12px;
        width: 50%;
        font-size: 20px;
        margin-top: 5%;
    }
    input{
        border-top: none;
        border-left: none;
        border-right: none;
    }

    label{
        font-size: 20px;
    }

    textarea{
        font-size: 20px; 
        border-top: none;
        border-left: none;
        border-right: none;
        width: 100%;
        font-family: Cambria, Cochin, Georgia, Times, 'Times New Roman', serif;
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








<div class="row">
		  <div class="naslov">
		      <h2>Moj profil</h2>
          <button type="submit" class="btn btn-primary">Uredi</button>
      </div>
		</div>
    <div>
      <article :key="location" v-for="location in locations">
        <h1>{{ location.ime }}</h1>
      </article>
    </div>


    <div class="roditelj" >
      <div class="col-md-12">
        <form>
          <div class="form-group row">
            <label for="username" class="col-4 col-form-label">Ime</label> 
            <div class="col-6">
            </div>
          </div>
          <div class="form-group row">
            <label for="name" class="col-4 col-form-label">Prezime</label> 
            <div class="col-6">
            </div>
          </div>
          <div class="form-group row">
            <label for="lastname" class="col-4 col-form-label">Mjesto stanovanja</label> 
            <div class="col-6">
              <input id="lastname" name="lastname" placeholder="Mjesto stanovanja" class="form-control here" type="text">
            </div>
          </div>
          <div class="form-group row">
            <label for="text" class="col-4 col-form-label">Kontakt broj</label> 
            <div class="col-6">
              <input id="text" name="text" placeholder="Kontakt broj" class="form-control here" required="required" type="text">
            </div>
          </div>
          <div class="form-group row">
            <label for="email" class="col-4 col-form-label">Broj djece</label> 
            <div class="col-6">
              <input id="email" name="email" placeholder="Broj djece" class="form-control here" required="required" type="text">
            </div>
          </div>
        </form>
      </div>
    </div>  


    <div class="dadilja" >
            <div class="col-md-12">
                <form>
                    <div class="form-group row">
                        <label for="username" class="col-4 col-form-label">Ime</label> 
                        <div class="col-6">
                        <input id="username" name="username" class="form-control here" required="required" type="text">
                        </div>
                    </div>
                        <div class="form-group row">
                        <label for="name" class="col-4 col-form-label">Prezime</label> 
                        <div class="col-6">
                            <input id="name" name="name" class="form-control here" type="text">
                        </div>
                    </div>
                    <div class="form-group row">
                        <label for="name" class="col-4 col-form-label">Spol</label> 
                        <div class="col-6">
                            <input id="name" name="name" class="form-control here" type="text"> 
                        </div> 
                        </div>
                    <div class="form-group row">
                        <label for="lastname" class="col-4 col-form-label">Grad</label> 
                        <div class="col-6">
                            <input id="lastname" name="lastname"  class="form-control here" type="text">
                        </div>
                    </div>
                    <div class="form-group row">
                        <label for="text" class="col-4 col-form-label">Koliko imam godina</label> 
                        <div class="col-6">
                            <input id="number" class="form-control here" required="required" type="number">
                        </div>
                    </div>
                    <div class="form-group row">
                        <label for="select" class="col-4 col-form-label">Kontakt broj</label>
                        <div class="col-6">
                            <input id="text" name="text" class="form-control here" required="required" type="text">
                        </div>
                    </div>
                    <div class="form-group row">
                        <label for="email" class="col-4 col-form-label">Vozačka dozvola</label>
                        <div class="col-6">
                            <input id="text" name="text" class="form-control here" required="required" type="text">
                        </div>
                    </div>
                    <div class="form-group row">
                        <label for="email" class="col-4 col-form-label">Mjesto čuvanja djece</label> 
                        <div class="col-6">
                            <input id="text" name="text" class="form-control here" required="required" type="text"> 
                        </div>
                    </div>
                    <div class="form-group row">
                        <label for="email" class="col-4 col-form-label">Iskustvo</label> 
                        <div class="col-6">
                            <input id="email" name="email" class="form-control here" required="required" type="text">
                        </div>
                    </div>
                    <div class="form-group row">
                        <label for="email" class="col-4 col-form-label">Ostalo</label> 
                        <p style="white-space: pre-line; font-size: 80%;"></p>
                        <br>
                        <div class="col-6">
                            <textarea style="font-size: 80%;"></textarea>
                        </div>
                    </div>
                </form>
            </div>
        </div>