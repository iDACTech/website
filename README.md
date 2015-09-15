# website

<!DOCTYPE html>
<html lang="en">
<head>
  <title>Bootstrap Example</title>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <link rel="stylesheet" href="http://maxcdn.bootstrapcdn.com/bootstrap/3.3.5/css/bootstrap.min.css">
  <script src="https://ajax.googleapis.com/ajax/libs/jquery/1.11.3/jquery.min.js"></script>
  <script src="http://maxcdn.bootstrapcdn.com/bootstrap/3.3.5/js/bootstrap.min.js"></script>
  <script type="text/javascript">
	$(document).ready(function(){
		$("#myModal").modal('show');
		
	});

	var attempt = 3; // Variable to count number of attempts.
	// Below function Executes on click of login button.
	function validate(){
	var username = document.getElementById("user").value;
	var password = document.getElementById("pass").value;
	if ( username == "Admin" && password == "1234"){
	alert ("Login successfully");
	   $("#submit").attr("data-dismiss","modal");
	  //document.getElementById("submit").data-dismiss=modal;
	//window.location = "success.html"; // Redirecting to other page.
	//return false;
	}
	else{
	attempt --;// Decrementing by one.
	alert("You have left "+attempt+" attempt;");
	// Disabling fields after 3 attempts.
	if( attempt == 0){
	document.getElementById("user").disabled = true;
	document.getElementById("pass").disabled = true;
	document.getElementById("submit").disabled = true;
	return false;
	}
	}
	}
</script>
</head>
<body>

<div class="container">
   <p>heyyee</p>
   <p>heyyee</p>
   <p>heyyee</p>
   <p>heyyee</p>
   <p>heyyee</p>
   <p>heyyee</p>
   <p>heyyee</p>
   <p>heyyee</p>
   <p>heyyee</p>
  <!-- Modal -->
  <div class="modal" id="myModal" role="dialog"  data-backdrop="static" data-keyboard="false">
    <div class="modal-dialog">
   <form method="post" > 
    
      <div class="modal-content">
        <div class="modal-header">
          
          <h4 class="modal-title">Login to Web App</h4>
        </div>
        <div class="modal-body">
          
        <p><input type="text" name="login" value="" id="user"/></p>
        <p><input type="password" name="password" value="" id="pass"/></p>
        <p class="remember_me">
          <label>
            <input type="checkbox" name="remember_me" id="remember_me"/>
            Remember me on this computer
          </label>
        </p>
        
      
        </div>
        <div class="modal-footer">
          <p class="submit"><input type="button" id="submit" name="commit" value="Login" onclick="validate()"></p>
      </div>
      </form>
    </div>
  </div>
  
</div>
</body>
</html>
