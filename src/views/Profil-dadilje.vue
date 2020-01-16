<template>
    <div class="profil-dadilja">
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
                                <label for="name" class="col-4 col-form-label">Spol</label> 
                                <div class="form-check form-check-inline" style="margin-left: 2.5%;">
                                    <input class="form-check-input" type="radio" name="inlineRadioOptions" id="inlineRadio1" value="Muško">
                                    <label class="form-check-label">Muško</label>
                                </div>
                                <div class="form-check form-check-inline">
                                    <input class="form-check-input" type="radio" name="inlineRadioOptions" id="inlineRadio2" value="Žensko">
                                    <label class="form-check-label">Žensko</label>
                                </div>
                              </div>
                              <div class="form-group row">
                                <label for="lastname" class="col-4 col-form-label">Grad</label> 
                                <div class="col-6">
                                  <input id="lastname" name="lastname" placeholder="Grad" class="form-control here" type="text">
                                </div>
                              </div>
                              <div class="form-group row">
                                <label for="text" class="col-4 col-form-label">Broj godina </label> 
                                <div class="col-6">
                                  <input id="number" min=18 placeholder="Broj godina" class="form-control here" required="required" type="number">
                                </div>
                              </div>
                              <div class="form-group row">
                                <label for="select" class="col-4 col-form-label">Kontakt broj</label>
                                <div class="col-6">
                                  <input id="text" name="text" placeholder="Kontakt broj" class="form-control here" required="required" type="text">
                                </div>
                              </div>
                              <div class="form-group row">
                                <label for="email" class="col-4 col-form-label">Adresa e-pošte</label> 
                                <div class="col-6">
                                  <input id="email" name="email" placeholder="Adresa e-pošte" class="form-control here" required="required" type="text">
                                </div>
                              </div>
                              <div class="form-group row">
                                <label for="email" class="col-4 col-form-label">Vozačka dozvola</label> 
                                <div class="form-check form-check-inline" style="margin-left: 2.5%;">
                                    <input class="form-check-input" type="radio" name="inlineRadioOptions" id="inlineRadio1" value="Da">
                                    <label class="form-check-label">Da</label>
                                </div>

                                <div class="form-check form-check-inline">
                                    <input class="form-check-input" type="radio" name="inlineRadioOptions" id="inlineRadio2" value="Ne">
                                    <label class="form-check-label">Ne</label>
                                </div>
                              </div>
                               <div class="form-group row">
                                <label for="email" class="col-4 col-form-label">Mjesto čuvanja djece</label> 
                                <div class="form-check form-check-inline" style="margin-left: 2.5%;">
                                    <input class="form-check-input" type="checkbox" id="inlineCheckbox1" value="Kod roditelja">
                                    <label class="form-check-label">Kod roditelja</label>
                                </div>
                                <div class="form-check form-check-inline">
                                    <input class="form-check-input" type="checkbox" id="inlineCheckbox2" value="Kod dadilje">
                                    <label class="form-check-label">Kod dadilje</label>
                                </div>
                              </div>
                              <div class="form-group row">
                                <label for="email" class="col-4 col-form-label">Adresa e-pošte</label> 
                                <div class="col-6">
                                  <input id="email" name="email" placeholder="Adresa e-pošte" class="form-control here" required="required" type="text">
                                </div>
                              </div>
                              <div class="form-group row">
                                <label for="email" class="col-4 col-form-label">Obrazovanje</label> 
                                <div class="col-6">
                                  <input id="email" name="email" placeholder="Obrazovanje" class="form-control here" required="required" type="text">
                                </div>
                              </div>
                              <div class="form-group row">
                                <label for="email" class="col-4 col-form-label">Ostalo</label> 
                                <div class="col-6">
                                  <input id="email" name="email" placeholder="Ostalo" class="form-control here" required="required" type="text">
                                </div>
                              </div>
                              <div class="form-group row">
                                <div class="offset-4 col-6">
                                  <router-link to="/Pocetna-dadilja"><button name="submit" type="submit" class="btn btn-primary">Potvrdi profil</button></router-link>
                                </div>
                              </div>
                            </form>
		                </div>
		            </div> 
		        </div>
</template>

<style scoped>

    .profil-dadilja{
        width: 40%;
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
        margin-top: 5%;
    }
    input{
        border-radius: 12px;
        padding: 8% 4%;
    }

    label{
        font-size: 20px;
    }

    
    
 

</style>