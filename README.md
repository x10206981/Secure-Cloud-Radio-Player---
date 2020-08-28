# Secure-Cloud-Radio-Player---
Secure Cloud Radio Player! :-)
<!DOCTYPE html>
<html>
	<head>
		<meta http-equiv="Content-Type" content="text/html; charset=utf-8">
		<title>Secure Cloud Radio Player! :-)</title>
		<style type="text/css">

		body {
			margin: 0px;
			padding: 0px;
			overflow: hidden;
			height: 100%; 
			max-height: 100%; 
			font-family:Sans-serif;
			line-height: 1.5em;
		}

		#header {
			position: absolute;
			top: 0px;
			left: 0px;
			width: 100%;
			height: 100px; 
			overflow: hidden; 
			background: #BCCE98;
		}

		#nav {
			position: absolute; 
			top: 0px;
			bottom: 0;
			right: 0;
			width: 280px;
			overflow: scroll; 
			background: #DAE9BC;
		}

		#logo {
			padding:20px;
		}

		main {
			position: fixed;
			top: 40%; /* Set this to the height of the header */
			right: 45%; /* Set this to the width of the navigation bar */
			bottom: 20%;
			overflow: auto; 
            color: blue; 
		}

        </head>    

		.innertube {
			margin: 25px; /* Provides padding for the content */
		}

		p {
			color: #555;
		}

		nav ul {
			list-style-type: none;
			margin: 10px;
			padding: 0px;
		}

		nav ul a {
			color: blue;
            margin: 0px; 
			text-decoration: none;
		}

		/*IE6 fix*/
		* html body{
			padding: 100px 280px 0 0; /* Set the first value to the height of the header and second value to the width of the nav */
		}

		* html main{ 
			height: 100%; 
			width: 100%; 
		}

		</style>

	</head>

	<body>		

		<main>
			<div class="innertube">

				<h2>SECURE CLOUD RADIO PLAYER! :-)</h2> 
				<p><script>generateText(300)</script></p>

			</div>
		</main>

		<nav id="nav">
			<div class="innertube">

            <ul>
				<li><a 1.<html>
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<link href="https://fonts.googleapis.com/css?family=Raleway" rel="stylesheet">
<style>
* {
  box-sizing: border-box;
}

body {
  background-color: #f1f1f1;
}

#regForm {
  background-color: #ffffff;
  margin: 1px auto;
  font-family: Raleway;
  padding: 1px;
  width: 50%;
  min-width: 250px;
}

h1 {
  text-align: center;
  color: blue;
}

input {
  padding: 10px;
  width: 100%;
  font-size: 17px;
  font-family: Raleway;
  border: 1px solid #aaaaaa;
}

/* Mark input boxes that gets an error on validation: */
input.invalid {
  background-color: #ffdddd;
}

/* Hide all steps by default: */
.tab {
  display: none;
}

button {
  background-color: #4CAF50;
  color: #ffffff;
  border: none;
  padding: 10px 20px;
  font-size: 17px;
  font-family: Raleway;
  cursor: pointer;
}

button:hover {
  opacity: 0.8;
}

#prevBtn {
  background-color: #bbbbbb;
}

/* Make circles that indicate the steps of the form: */
.step {
  height: 15px;
  width: 15px;
  margin: 0 2px;
  background-color: #bbbbbb;
  border: none;  
  border-radius: 50%;
  display: inline-block;
  opacity: 0.5;
}

.step.active {
  opacity: 1;
}

/* Mark the steps that are finished and valid: */
.step.finish {
  background-color: #4CAF50;
}
</style>

<form id="regForm" action="/action_page.php">
  <h1>Register New User:</h1>
  <!-- One "tab" for each step in the form: -->
  <div class="tab">Create Username:
    <p><input placeholder="Username..." oninput="this.className = ''" name="fname"></p> 
  </div>
  <div class="tab">Contact Info:
    <p><input placeholder="E-mail..." oninput="this.className = ''" name="email"></p>
  </div>
  <div class="tab">Login Info:
    <p><input placeholder="Username..." oninput="this.className = ''" name="uname"></p>
    <p><input placeholder="Password..." oninput="this.className = ''" name="pword" type="password"></p>
  </div>
  <div style="overflow:auto;">
    <div style="float:right;">
      <button type="button" id="prevBtn" onclick="nextPrev(-1)">Previous</button>
      <button type="button" id="nextBtn" onclick="nextPrev(1)">Next</button>
    </div>
  </div>
  <!-- Circles which indicates the steps of the form: -->
  <div style="text-align:center;margin-top:40px;">
    <span class="step"></span>
    <span class="step"></span>
    <span class="step"></span>
    <span class="step"></span>
  </div>
</form>

<script>
var currentTab = 0; // Current tab is set to be the first tab (0)
showTab(currentTab); // Display the current tab

function showTab(n) {
  // This function will display the specified tab of the form...
  var x = document.getElementsByClassName("tab");
  x[n].style.display = "block";
  //... and fix the Previous/Next buttons:
  if (n == 0) {
    document.getElementById("prevBtn").style.display = "none";
  } else {
    document.getElementById("prevBtn").style.display = "inline";
  }
  if (n == (x.length - 1)) {
    document.getElementById("nextBtn").innerHTML = "Submit";
  } else {
    document.getElementById("nextBtn").innerHTML = "Next";
  }
  //... and run a function that will display the correct step indicator:
  fixStepIndicator(n)
}

function nextPrev(n) {
  // This function will figure out which tab to display
  var x = document.getElementsByClassName("tab");
  // Exit the function if any field in the current tab is invalid:
  if (n == 1 && !validateForm()) return false;
  // Hide the current tab:
  x[currentTab].style.display = "none";
  // Increase or decrease the current tab by 1:
  currentTab = currentTab + n;
  // if you have reached the end of the form...
  if (currentTab >= x.length) {
    // ... the form gets submitted:
    document.getElementById("regForm").submit();
    return false;
  }
  // Otherwise, display the correct tab:
  showTab(currentTab);
}

function validateForm() {
  // This function deals with validation of the form fields
  var x, y, i, valid = true;
  x = document.getElementsByClassName("tab");
  y = x[currentTab].getElementsByTagName("input");
  // A loop that checks every input field in the current tab:
  for (i = 0; i < y.length; i++) {
    // If a field is empty...
    if (y[i].value == "") {
      // add an "invalid" class to the field:
      y[i].className += " invalid";
      // and set the current valid status to false
      valid = false;
    }
  }
  // If the valid status is true, mark the step as finished and valid:
  if (valid) {
    document.getElementsByClassName("step")[currentTab].className += " finish";
  }
  return valid; // return the valid status
}

function fixStepIndicator(n) {
  // This function removes the "active" class of all steps...
  var i, x = document.getElementsByClassName("step");
  for (i = 0; i < x.length; i++) {
    x[i].className = x[i].className.replace(" active", "");
  }
  //... and adds the "active" class on the current step:
  x[n].className += " active";
}
</script>

            <h3>*PLAY CLOUD RADIO:</h3>
			<ul>
            	<li><a href="https://liveradio.ie/stations/radio-nova">1.Radio NOVA*</a>
                <li><a href="https://www.liveradio.ie/stations/dublins-q102">2.Dublin's Q102</a>
                <li><a href="https://radiofm-online.com/rmf-fm">3.Radio RMF-FM</a>
                <li><a href="https://radiofm-online.com/antyradio">4.AntyRadio</a>
              </li>
             </ul>
          </nav>
        </div> 
    </body>
</html>
