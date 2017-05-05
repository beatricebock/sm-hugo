+++
title = "Get Invited"
description = "Want to know more?"
+++
<div class="message success" data-component="message"> We are having a workshop in JUNE, come join us! <span class="close small"></span></div>
<h4>Join our <span class="highlight">FREE</span> forum to learn how to bring the best out of your company.</h4>
<br/>
<p>Enter your e-mail <a href="#sign-up">below</a> and we'll contact you with more details.</p>

<br/>
<div class="row align-center" id="forum-desc">
<div class="col col-6">
  <h5>Presented by Datin Dr Wendy Liow</h5>
  <img src="/img/profiles/wendy.png" alt="Datin Dr Wendy">
  <br />
  <caption>Dean of ELM, HELP University</caption>
</div>
<div class="col col-6">
  <h5>Learn how to:</h5>
  <div id="forum-hook">
    <div class="pains">
      <i class="fa fa-check-square-o"></i>
      <p>
        Identify and overcome performance management challenges
      </p>
    </div>
    <div class="pains">
      <i class="fa fa-check-square-o"></i>
      <p>
        Reward and motivate employees (the RIGHT way!)
      </p>
    </div>
    <div class="pains">
      <i class="fa fa-check-square-o"></i>
      <p>
        How to set KPIs that matter
      </p>
    </div>
  </div>
</div>
</div>

<h5>Don't miss this opportunity!</h5>
<p>Learn from the absolute best in HR and let us help you find the best strategy for your company.</p>
<p>Simply enter your details below and we'll contact you for more details.</p>
<form action="" data-component="validate" method="post" class="form form-centered" id="sign-up"><input type="hidden" name="authorize-token" value="">

<div class="form-item">
    <label>Email <span id="user-email-validation-error"></span></label>
    <input type="email" name="user-email" autofocus="true" autocomplete="off" style="background-image: url(&quot;data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABAAAAASCAYAAABSO15qAAAAAXNSR0IArs4c6QAAAPhJREFUOBHlU70KgzAQPlMhEvoQTg6OPoOjT+JWOnRqkUKHgqWP4OQbOPokTk6OTkVULNSLVc62oJmbIdzd95NcuGjX2/3YVI/Ts+t0WLE2ut5xsQ0O+90F6UxFjAI8qNcEGONia08e6MNONYwCS7EQAizLmtGUDEzTBNd1fxsYhjEBnHPQNG3KKTYV34F8ec/zwHEciOMYyrIE3/ehKAqIoggo9inGXKmFXwbyBkmSQJqmUNe15IRhCG3byphitm1/eUzDM4qR0TTNjEixGdAnSi3keS5vSk2UDKqqgizLqB4YzvassiKhGtZ/jDMtLOnHz7TE+yf8BaDZXA509yeBAAAAAElFTkSuQmCC&quot;); background-repeat: no-repeat; background-attachment: scroll; background-size: 16px 18px; background-position: 98% 50%; cursor: auto;">
</div>

<div class="form-item">
    <label>Name <span id="user-password-validation-error"></span></label>
    <input type="text" name="user-password" autocomplete="off" style="background-image: url(&quot;data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABAAAAASCAYAAABSO15qAAAAAXNSR0IArs4c6QAAAPhJREFUOBHlU70KgzAQPlMhEvoQTg6OPoOjT+JWOnRqkUKHgqWP4OQbOPokTk6OTkVULNSLVc62oJmbIdzd95NcuGjX2/3YVI/Ts+t0WLE2ut5xsQ0O+90F6UxFjAI8qNcEGONia08e6MNONYwCS7EQAizLmtGUDEzTBNd1fxsYhjEBnHPQNG3KKTYV34F8ec/zwHEciOMYyrIE3/ehKAqIoggo9inGXKmFXwbyBkmSQJqmUNe15IRhCG3byphitm1/eUzDM4qR0TTNjEixGdAnSi3keS5vSk2UDKqqgizLqB4YzvassiKhGtZ/jDMtLOnHz7TE+yf8BaDZXA509yeBAAAAAElFTkSuQmCC&quot;); background-repeat: no-repeat; background-attachment: scroll; background-size: 16px 18px; background-position: 98% 50%; cursor: auto;">
</div>

<p><button class="button primary width-100">Get Invited</button></p>

</form>

<script>
// URL updates and the element focus is maintained
// originally found via in Update 3 on http://www.learningjquery.com/2007/10/improved-animated-scrolling-script-for-same-page-links

// filter handling for a /dir/ OR /indexordefault.page
function filterPath(string) {
return string
  .replace(/^\//, '')
  .replace(/(index|default).[a-zA-Z]{3,4}$/, '')
  .replace(/\/$/, '');
}

var locationPath = filterPath(location.pathname);
$('a[href*="#"]').each(function () {
var thisPath = filterPath(this.pathname) || locationPath;
var hash = this.hash;
if ($("#" + hash.replace(/#/, '')).length) {
  if (locationPath == thisPath && (location.hostname == this.hostname || !this.hostname) && this.hash.replace(/#/, '')) {
    var $target = $(hash), target = this.hash;
    if (target) {
      $(this).click(function (event) {
        event.preventDefault();
        $('html, body').animate({scrollTop: $target.offset().top}, 1000, function () {
          location.hash = target;
          $target.focus();
          if ($target.is(":focus")){ //checking if the target was focused
            return false;
          }else{
            $target.attr('tabindex','-1'); //Adding tabindex for elements not focusable
            $target.focus(); //Setting focus
          };
        });
      });
    }
  }
}
});
</script>
