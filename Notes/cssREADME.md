/* Attribute Selectors ------------- */

.form-contact {
  padding: 20px 24px;
  background: #f4f7f8;
}

#container {
  max-width: 500px;
  margin: auto;
}

input[type="email"] {
  background: #fdfee6;
}

a[target="_blank"] {
  color: #39add1;
  text-decoration: none;
  border-bottom: 1px dotted;
}

/* DRY Classes ------------- */

.br {
  border-radius: .5em;
}

.avatar {
  display: block;
  margin: 0 auto 2em;
}

.rounded {
  border-radius: 50%;
}

.btn {
  cursor: pointer;
  font-size: .875em;
  font-weight: 400;
  color: #fff;
  padding-left: 20px;
  padding-right: 20px;
  text-transform: uppercase;
}

.btn:hover {
  opacity: .75;
}

.default {
  background-color: #52bab3;
}

.error {
  background-color: #ff784f;
}

@media (min-width: 769px) {
  .inln {
    width: auto;
    display: inline-block;
  }
  .btn + .btn {
  margin-left: 20px;
}
}
/* Combinators ------------- */

form > a {
  font-size: .7em;
}
h1 ~ label {
  background: tomato;
  color: white;
  padding: 5px;
}
<!-- HTML to see markup and semantic -->
<!DOCTYPE html>
<html>
<head>
	<title>Selectors</title>
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <link href='http://fonts.googleapis.com/css?family=Nunito:400,300' rel='stylesheet' type='text/css'>
  <link rel="stylesheet" href="css/base-style.css">
  <link rel="stylesheet" href="css/selectors.css">
</head>
<body>
	<div id="container">
		<form class="form-contact br">
	  	<h1>Contact</h1>

		  <label for="name">Name:</label> 
		  <input type="text" id="name">

     	<label for="email">Email:</label>
     	<input type="email" id="email" placeholder="email@website.com">
  
     	<label for="msg">Message:</label>
     	<textarea id="msg" rows="7"></textarea>

		  <input class="btn inln default" type="submit" value="Submit">
 		  <input class="btn inln error" type="reset" value="Reset"> 
		</form>
		
		<hr>
 		<img class="avatar rounded" src="img/avatar.png" alt="Mountains"> 
		
		<form class="form-login">
			<label for="username">Username:</label> 
			<input type="text" id="username">

			<label for="password">Password:</label>
			<input type="password" id="password">
     
			<input class="btn default" type="submit" value="Login">
      <a href="#" target="_blank">Forgot your password?</a> 
		</form>
	</div>
</body>
</html>
<!-- EXERCISE BORDER AND COLORFULNESS ON IT -->
.callout {
  display: block;
  width: 250px;
  padding: .25rem 1rem;
  border-radius: 20px/10px;
  margin: 1rem auto;
  box-shadow: 1px 2px 3px rgba(0,1,30,.5);
  background-image: linear-gradient(135deg, rgba(255,255,224,.8) 0%, rgba(250,100,50,.2) 50%), linear-gradient(#b40 0%, #d63 50%, #c51 51%, #e74 100%);
  color: white;
  text-align: center;
  font-size: 1.25rem;
}

<!-- Using :empty is good idea for checking html and see if you might have some semantics that just occupy space -->

<!-- empty, onlychild usage -->
<!-- /* Structural Pseudo-classes------------------ */ -->

li:first-child {
  background-color: #52bab3;
  color: white;
}
li:last-child {
  border: none;
}
span:only-child {
  color: #52bab3;
  font-size: 1.5em;
}

li:empty {
  background-color: tomato;
}
<!-- example how to put image right next to text without repeating itself over and over  -->
a[href^="http:"] {
   color: #52bab3;
  text-decoration: none;
  background-repeat: no-repeat;
  background-size: 18px 18px;
  padding-left: 25px;
  <!-- /* Substring Matching Attribute Selectors ---- */ -->

a[href^="http:"] {
  color: #52bab3;
  text-decoration: none;

}
a[href$=".pdf"] {
  background-image: url('../img/icn-pdf.svg');
}
a[href$=".jpg"] {
  background-image: url('../img/icn-picture.svg');
}
a[href$=".zip"] {
  background-image: url('../img/icn-zip.svg');
}
a[href*="downloads"] {
  background-repeat: no-repeat;
  background-size: 18px 18px;
  padding-left: 25px;
}
img[src*="thumb"] {
  margin: 4px;
  border: solid 2px;
  width: 180px;
  height: 140px;
}

img[src*="bay"] {
  border-color: red;
}
<!-- /* UI element states pseudo-classes ------------ */ -->

input:focus,
textarea:focus {
  border-color: #52bab3;
}

input:disabled {
  background: #ddd;
}

input[type="checkbox"]:checked + label {
  font-weight: bold;
}
<!-- /* Structural Pseudo-classes------------------ */ -->

div:nth-child(an+b) {
  background: #52bab3;
  color: white;
}

div:nth-last-of-type(4) {
  background: #52bab3;
  color: white;
}
div:nth-of-type(4) {
  background: #52bab3;
  color: white;
}
<!-- ROOT, TARGET, NOT -->

:root {
  background: #e3effb;
}

:target {
  background: #384047;
  color: white;
}
#col-c:target {
  background: #eff1f2;
  color: initial;
  box-shadow: 0 0 6px rgba(0,0,0, .2);
}
input:not([type="submit"]) {
  box-shadow: inset 0 2px 0 rgba(0,0,0, .15);
}

.col:not(:first-child),
nav a:not(:first-child) {
  margin-left: 15px;
}
<!-- /* Pseudo-elements -------------------------------- */ -->

.intro:first-line {
  font-weight: bold;
  font-size: 1.4em;
}

.intro:first-letter {
  float: left;
  font-size: 80px;
  color: white;
  padding: 5px 10px;
  background: #384047;
  margin: 10px 10px 0 0;
  border-radius: 5px;
  line-height: 1;
}
    
.jpg::before {
  content: url(../img/icn-picture.svg);
  margin-right: 8px;
}

.zip::before {
  content: url(../img/icn-zip.svg);
  margin-right: 8px;
}

h1::before,
h1::after {
  content: "";
  display: inline-block;
  width: 24px;
  height: 24px;
  border-radius: 50%;
  background: coral;
  margin: 0 10px;
}