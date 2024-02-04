# INPUT-VALIDATION
<!DOCTYPE html>
<html lang>
<head>
  <title>validation form</title>
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.4.1/css/bootstrap.min.css">
  <script src="https://ajax.googleapis.com/ajax/libs/jquery/1.11.3/jquery.min.js"></script> 
  <script src="http://maxcdn.bootstrapcdn.com/bootstrap/3.3.5/js/bootstrap.min.js"></script>
  <style>

  body {
      height: 100%;
      background-image: url("pic4.jpeg");
      background-size: cover;
      opacity: 0.9;
  }
   
  .global-container {
      height: 100%;
      display: flex;
      align-items: center;
      justify-content: center;

 
  }
   
  form {
      padding-top: 5pxpx;
      font-size: 14px;
      margin-top: 30px;
      
  }
   
  .card-title {
      font-weight: 300;
  }
   
  .btn {
      font-size: 14px;
      margin-top: 20px;
  }
   
  .login-form {
      width: 1000px;
      margin: 50px;
   
  }
   
  .alert {
      margin-bottom: -30px;
      font-size: 13px;
      margin-top: 20px;
  }
  </style>
  <script>  
    function validateform(){  
    var name=document.myform.name.value;  
    var password=document.myform.password.value;  
    var password1=document.myform.password1.value;
    var email=document.myform.email.value;
    var phone=document.myform.phone.value;
    var radio = document.myform.radio.value;
    let checkbox=document.getElementById("check");
    
    
    if (name==null || name==""){  
      alert("Name can't be blank");  
      return false;  
    }
    if(name.length<5)
    {
        alert("name size max 5"); 
        return false;
    }
    if(name.length!= ""){
           var regex = /^(?=.*[0-9])(?=.*[!@#\$%\^&\*])/;              
            if(regex.test(name) === true) 
            {    alert("Please enter alphabet");
                    return false;
            }       
    }
    
    if (password == "") {
            alert("Please enter your password");
            password.focus();
            return false;
        }
    
    if(password != password1){
        alert("Password mismatch");
            return false;
    }
    if(password.length!= ""){
           var regex = /^(?=.*[a-z])(?=.*[A-Z])(?=.*[0-9])(?=.*[!@#\$%\^&\*])(?=.{8,})/;                
            if(regex.test(password) === false) 
            {    alert("Please enter a valid password");
                    return false;
            }       
    }
    if(email == ""){
        alert("Please enter your email");
        email.focus();
            return false;
    
    }
    if(email.charAt(email.length-4)!='.'){
        alert("Please enter your email at 4th");
        return false;
    
    }
    if (phone == ""){  
      alert("enter Number");  
      return false;  
    }
    if (isNaN(phone)){  
      alert("enter numeric value");  
      return false;  
    }
    if(phone.length<10){
        alert("MObile number must  be 10 digit");  
      return false; 
    
    }
    if (radio == null || radio == "") {
                alert("Mention your gener");
                return false;
            }
    if (check.checked){
            }
            else{
                alert("Agree to terms and conditions!!");
                return false;
            }
    }
    </script>  
  </head>
<body>
        
        </form>  
  <div class="global-container">
    <div class="card login-form">
        <div class="card-body">
            <h3 class="card-title text-center"><b  style="font-size: larger; color: crimson;">SIGN UP</b></h3>
            <div class="card-text">
                <form name="myform" method="post" action="" onsubmit="return validateform()"> <br>>
                  <div class="form-group">
                    <label for="usr"><b style="color:aqua;">NAME</b></label>
                    <input type="text" name="name" class="form-control form-control-sm" id="usr">
                </div><br>
                <div class="form-group">
                  <label for="we"><B style="color:aqua;">PASSWORD</B></label>
                  <a href="#" style="float:right;font-size:12px;">Forgot password? </a>
                  <input type="password"  name="password" class="form-control form-control-sm"id="we">
              </div><br>
              <div class="form-group">
                <label for="we"><B style="color:aqua;"> CONFIRM PASSWORD</B></label>
                <input type="password"  name="password1" class="form-control form-control-sm"id="we">
            </div><br>
                    <div class="form-group">
                        <label for="usr"><b style="color:aqua;">EMAIL ADDRESS</b></label><input type="email" name="email" size = "25" placeholder="priya@gmail.com"class="form-control form-control-sm" id="usr">
                    </div> 
                    <label for=""><B style="color:aqua;"> MOBILE:</B></label>
                    <input type = "text"  name="phone"   size = "10" placeholder="enter number"><br><BR>
                        <input type="radio" id="radio1" name="radio" value="Yes"><b style="color:aqua;">FEMALE</b><br>
                     <input type="radio" id="radio2" name="radio" value="No"><b style="color:aqua;">MALE</b><br><br>
                    <input id ="check" type="checkbox" name="c" value="checked"><label><a href="sign in.html">..I agree to terms and conditions</a></label>

                        <button type="submit" class="btn" formaction=""><a href=""
                            style="text-decoration: none;color:black;">Sign in</a></button>
                  
                </form>
            </div>
        </div>
    </div>
</div>
          
</body>
</html>


