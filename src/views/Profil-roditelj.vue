<template>
    <div class="profil-roditelj">
		            <div class="row">
		                <div class="col-md-12">
		                    <h1>Izrada profila</h1>
		                </div>
		            </div>
		            <div class="row">
		                <div class="col-md-12">
		                    <form>
                              <div class="form-group row">
                                <label for="username" class="col-4 col-form-label">Ime</label> 
                                <div class="col-6">
                                  <input id="username" name="username" placeholder="Ime" class="form-control here" required="required" type="text">
                                </div>
                              </div>
                              <div class="form-group row">
                                <label for="name" class="col-4 col-form-label">Prezime</label> 
                                <div class="col-6">
                                  <input id="name" name="name" placeholder="Prezime" class="form-control here" type="text">
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
                                <label for="select" class="col-4 col-form-label">Adresa e-pošte</label>
                                <div class="col-6">
                                  <input id="text" name="text" placeholder="Adresa e-pošte" class="form-control here" required="required" type="text">
                                </div>
                              </div>
                              <div class="form-group row">
                                <label for="email" class="col-4 col-form-label">Broj djece</label> 
                                <div class="col-6">
                                  <input id="email" name="email" placeholder="Broj djece" class="form-control here" required="required" type="text">
                                </div>
                              </div>
                              <div class="form-group row">
                                <div class="offset-4 col-6">
                                  <router-link to="/Pocetna-roditelj"><button name="submit" type="submit" class="btn btn-primary">Potvrdi profil</button></router-link>
                                </div>
                              </div>
                            </form>
		                </div>
		            </div> 
		        </div>
</template>

<style scoped>

    .profil-roditelj{
        width: 35%;
        margin: 5% auto;
        background-color: rgb(205, 227, 235);
        border-radius: 20px;
        margin: 3% auto;
        padding: 2% 0;
        font-family: Cambria, Cochin, Georgia, Times, 'Times New Roman', serif;
       
    }

    .col-md-12 h1{
    border-bottom: 1.5px solid 	#428bca;
    width: 80%;
    margin: auto;
    margin-bottom: 5%;
    }

    button{
        border-radius: 12px;
        width: 50%;
        font-size: 20px;
    }
    input{
        border-radius: 12px;
        padding: 8% 4%;
    }

    label{
        font-size: 20px;
    }
 

</style>