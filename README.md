<!DOCTYPE html>
<html>
<head>
<title>FORMS ASSIGNMENT</title>
<style>
	input{
		border-radius:4%;
		color:black;
		background-color: white;
	}
	body{
		box-sizing: border-box;
		background-color:lightblue;
		
	}
	form{
		padding-left:41%;
	}
	label{
		margin-bottom:30px;
	}
	.input input{
		padding:10px;
		margin:2% 0 0 0;
		padding-right:90px;
	}
	h2{
		text-align:center;
		padding:30px;
	}
	.genderr{
		font-size:15px;
		padding:6px; 
	}
	.choose{
		font-size:18px;
	}
	select {
        width: 120px;
        margin: 15px 0 15px 0;
        padding:6px;
    }
    .location select{
    	width:170px;
    	padding:9px;
    }
    .location select option{
    	padding:6px;
    }
    .day input{
    	padding:10px;
    }
    span{
    	color: red;
    	font-size: 13px;
    }
    input[type=submit]{
    	padding: 5px;
    	font-size: 15px;
    }
    input[type=file]{
    	padding: 5px;
    }
</style>
</head>
<body>
	<script>
		function validateform(){
			const x=document.getElementById("fname").value;
			const a=document.getElementById("lname").value;
			const b=document.getElementById("email").value;
			const c=document.getElementById("number").value;
			if(x == null || x =="" ){
				document.getElementById("fName").innerHTML= "*Enter first Name";
			}
			if(a == null || a == ""){
				document.getElementById("lName").innerHTML="*Enter Last Name";
			}
			if(b == null || b == ""){
				document.getElementById("eMail").innerHTML="*Enter Email";
			}
			if(c == null || c == ""){
				document.getElementById("num").innerHTML="*Enter Number";
			}
			const valid=false;
			const y=document.myForm.gender;
			for(var i=0;i<y.length;i++){
				if(y[i].checked){
					valid=true;
					break;
				}
			}
			if(valid){
				document.getElementById("radi").style.display=none;
			}
			else{
				document.getElementById("radi").innerHTML="*Please select gender";
			}
			var valid1=false;
			if(document.getElementById("html").checked){
       valid1=true;
     }
      else if(document.getElementById("css").checked){
       valid1=true;
     }
      else if(document.getElementById("js").checked){
       valid1=true;
     }
      else if(document.getElementById("python").checked){
       valid1=true;
     }
      else if(document.getElementById("php").checked){
       valid1=true;
}
    if(valid1){
				document.getElementById("check").style.display=none;
			}
			else{
				document.getElementById("check").innerHTML="*Please select one technology";
			}

			if(myForm.stream.selectedIndex==0){
				document.getElementById("sel").innerHTML="*Please select one stream";
			}
			const valid2=false;
			const z=document.getElementById("locations");
			for(var i=0;i<z.options.length;i++){
				if(z.options[i].selected===true){
					valid2=true;
					break;
				}
			}
			if(valid2){
				document.getElementById("msel").style.display=none;
			}
			else{
				document.getElementById("msel").innerHTML="*Please select one location";
			}
			var userdate=document.getElementById("OBD").value;
			if(userdate==null || userdate==""){
				document.getElementById("dan").innerHTML="*Please select a date";
			}
			var filein=document.getElementById("fille").value;
			if(!filein){
				document.getElementById("upload").innerHTML="*Please select file";
			}
		}
		
	</script>
<h2 >FORMS </h2>
<form name="myForm">
<div class="input">	
  <label>First name:</label><br>
  <input type="text" id=fname name="fname" placeholder="Enter your First name"><br>
  <span id="fName"></span><br>
  <label>Last name:</label><br>
  <input type="text" id=lname name="lname" placeholder="Enter your Last Name" ><br>
  <span id="lName"></span><br> 
  <label>Email:</label><br>
  <input type="Email" id="email" placeholder="Enter your Email" ><br>
  <span id="eMail"></span><br>
  <label>Mobile Number:</label><br>
  <input type="tel" id="number" placeholder="Enter your Mobile Number" required><br>
  <span id="num"></span><br>
</div>
<div class="genderr">
 <h3>GENDER</h3>
 <input type="radio" name="gender" > MALE<br>
 <input type="radio" name="gender">FEMALE<br>
 <input type="radio" name="gender">NONE<br>
 <span id="radi"></span><br>
</div>
<div>
	<h3> Hobbies</h3>
		<input type="checkbox" id="html"> HTML<br>
		<input type="checkbox" id="css">CSS<br>
		<input type="checkbox" id="js">JAVASCRIPT<br>
		<input type="checkbox" id="python">PYTHON<br>
		<input type="checkbox" id="php">PHP<br>
		<span id="check"></span><br>
	</div>
	<div class="choose">
	<h3>Choose Your Stream</h3>
	<select id="streamm" name="stream">
	    <option value="CSE">CSE</option>
	    <option value="ECE">ECE</option>
	    <option value="MECH">MECH</option>
	    <option value="CIVIL">CIVIL</option>

	</select>
		    <br><span id="sel"></span>
	<br>
	</div>
<div class="location">
	<h3>Locations</h3>
	<select id="locations" name="location" size="5" multiple>
	    <option value="chennai">Chennai</option>
	    <option value="hyderabad">Hyderabad</option>
	    <option value="banglore">Bangalore</option>
	    <option value="kochi">Kochi</option>
	    <option value="singapore">Singapore</option>
	</select><br>
	<span id="msel"></span><br>
	</div>
	<div class="day">
	<h3>Select your Onboarding-date:</h3>
	<input type="date" id=OBD><br>
	<span id="dan"></span><br>
		</div>
	<h3> upload file</h3>
	<input type="file"name="file" id = fille accept=""><br>
	<span id="upload"></span><br>
	<br><br>
	<input type="submit" name="button"  onclick="validateform()">
</form>
	</body>
</html>
