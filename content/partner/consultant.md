+++
title= "Become Our HR Consultant"
description= "Got expertise to share?"
+++

<fieldset>
  <legend>Enter your contact details below</legend>
  <form id="newhr">
  <div class="form-item">
    <label>Salutation</label>
    <select class="small" id="hr-salut>
      <option value="Mx">Mx</option>
      <option value="Miss">Miss</option>
      <option value="Mrs">Mrs</option>
      <option value="Mr">Mr</option>
    </select>
  </div>
  <div class="form-item">
    <label>Name</label>
    <input type="text" name="name" id="hr-name" placeholder="Name" required/>
  </div>
  <div class="form-item">
    <label>E-mail<span class="req"></span></label>
    <input type="email" name="email" id="hr-email" placeholder="example@company.com" required/>
  </div>

  <div class="form-item">
    <label>Company</label>
    <input type="text" name="company" id="hr-company" placeholder="Company Co." required/>
  </div>
  <div class="form-item">
    <label>Company Website</label>
    <input type="url" name="site" id="hr-site" placeholder="example.com" />
  </div>
  <button id="hr-submit" type="submit">Talk to us</button>
  </form>
</fieldset>

<script>
$(function() {
  //just make a variable to keep track of the data coming from Firebase
  var data = [];

  //create a new connection to firebase
  var ref = new Firebase('https://form-firebase.firebaseio.com/partner/hr');

  //listen to data updates from firebase
  ref.on("value", function(snapshot) {
    console.log(snapshot.val());
    //when data updates at Firebase, put it in the data variable
    data = snapshot.val();
  })



  $('#newhr').submit(function(event) {
    var $form = $(this);
    console.log("submit to Firebase");

    //make the submit disabled
    $form.find("#hr-submit").prop('disabled', true);

    //get the actual values that we will send to firebase
    var salutToSend = $('#hr-salut').val();
    console.log(salutToSend);

    var nameToSend = $('#hr-name').val();
    console.log(nameToSend);

    var emailToSend = $('#hr-email').val();
    console.log(emailToSend);

    var companyToSend = $('#hr-company').val();
    console.log(companyToSend)

    var siteToSend = $('#hr-site').val();

    //take the values from the form, and put them in an object
    var newhr = {
      "salutation": salutToSend,
      "name": nameToSend,
      "email": emailToSend,
      "company": companyToSend,
      "site": siteToSend
    }
    //put the new object into the data array
    data.push(newhr);
    console.log(data);
    //send the new data to Firebase
    ref.set(data);

    return false;
  })
})
</script>
