# website
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
<style type="text/css">
*{
  margin:10;
  padding:10;
  }
 body{
       
    background-image: url(op.jpg);
    margin-top:40px;
    background-position:center;
   background-size:cover;
   font-family:sans-serif;
    }

   .regform{
          width:800px;
    background-color:rgb(0,0,0,0.6);
    margin:auto;
    color:#FFFFFF;
    padding:10px 0px 10px 0px;
    text-align:center;
    border-radius:15px 15px 0px 0px ;
    }  
.main{
      background-color:rgb(0,0,0,0.5);
   width:800px;
   margin:auto;}
  
  form{
      padding:10px;
   
  } 
  
  #name{
       width:100%;
    height:100px;
    
    }  
 .name{
            margin-left:25px;
   margin-top:30px;
   width: 125px;
            color: white;
            font-size: 18px;
            font-weight: 700;}
.firstname{
                   position: relative;
       left:200px;
       top:-37px;
       line-height: 40px;
       border-radius: 6px;
       padding: 0 22px;
       font-size: 16px;
       
       }
.lastname{
             position: relative;
       left:417px;
       top:-80px;
       line-height: 40px;
       border-radius: 6px;
       padding: 0 22px;
       font-size: 16px;
       color:#555;       
                  }  
 .firstlabel{
            position:relative;
            color:#E5E5E5;    
      text-transform: capitalize;
   font-size: 14px;
   left:203px;
   top:-45px;
   }   
.lastlabel{
            position:relative;
   color:#E5E5E5;
   text-transform:capitalize;
   font-size:14px;
   left:492px;
   top:-76px;
     } 
.company{
           position:relative;
     left:200px;
     top:-37px;
     line-height: 40px;
     width:480px;
        border-radius: 6px;
     padding: 0 22px;
     font-size: 16px;
     color: #555;  }
 .email{
        position:relative;
  left:200px;
     top:-37px;
     line-height: 40px;
     width:480px;
        border-radius: 6px;
     padding: 0 22px;
     font-size: 16px;
     color: #555;  
    }     
 
   .Code{
         position:relative;
  left:200px;
     top:-37px;
     line-height: 40px;
     width:95px;
        border-radius: 6px;
     padding: 0 22px;
     font-size: 16px;
     color: #555;  
  }
 .number{
         position:relative;
  left:200px;
     top:-37px;
     line-height: 40px;
     width:255px;
        border-radius: 6px;
     padding: 0 22px;
     font-size: 16px;
     color: #555; 
     }
 .area-code{
            position:relative;
      color:#E5E5E5;
      text-transform:capitalize;
      font-size:16px;
      left:54px;
      top:-4px;
     }
 .phone-number{
              position:relative;
      color:#E5E5E5;
      text-transform:capitalize;
      font-size:16px;
      left:-100px;
      top:-2px;
     }
 .option{
         position:relative;
  left:200px;
     top:-37px;
     line-height: 40px;
     width:532px;
     height:40px;
        border-radius: 6px;
     padding: 0 22px;
     font-size: 16px;
     color: #555; 
     outline:none;
     overflow:hidden;
  }    
     .option option{
                 font-size:20px;
       }
   #coustomer{
                margin-left:25px;
    color:white;
    font-size:18px;
    
      } 
     .radio{
         display:inline-block;
   padding-right:70px;
   font-size:25px;
   margin-left:25px;
   margin-top:15px;
   color:white;
   }
.radio input{
              width:20px;
     height:20px;
     border-radius:50%;
     cursor:pointer;
     outline:none;
    } 
    button{
        background-color:#3BAF9F;
     display:block;
     margin:20px 0px 0px 20px;
     text-align:center;
     border-radius:12px;
     border:2px solid #366473;
     padding:14px 110px;
     outline:none;
     color:white;
     cursor:pointer;
     transition:0.25px;
    } 
   button:hover{
                background-color:#5390F5;
      }  
</style>
</head>

<body>
    <div class="regform">
        <h1>
 BFC LEAGUE SEASON-6 FORM</h1>
<h2 class="name">
<div class="center">
  <div class="form-input">
    <label for="file-ip-1"> Photo</label>
    <input type="file" id="file-ip-1" accept="image/*" onchange="showPreview(event);">
    <div class="preview">
      <img id="file-ip-1-preview">
    </div>
  </div>
</div>
<style type="text/css">
body {
  margin:0px;
  height:100vh;
}
.center {
  height:100%;
  display:flex;
  align-items:center;
  justify-content:center;
}
.form-input {
  width:250px;
  padding:20px;
  border:2px dashed #555;
}
.form-input input {
  display:none;
}
.form-input label {
  width:100%;
  height:100px;
  line-height:100px;
  text-align:center;
  color:#fff;
  font-size:30px;
  font-family:"Open Sans",sans-serif;
  text-transform:Uppercase;
  font-weight:600;
  border-radius:10px;
  cursor:pointer;
}

.form-input img {
  width:100%;
  display:none;
  margin-top:10px;
}
</style>
<script>
function showPreview(event){
  if(event.target.files.length > 0){
    var src = URL.createObjectURL(event.target.files[0]);
    var preview = document.getElementById("file-ip-1-preview");
    preview.src = src;
    preview.style.display = "block";
  }
}
</script>
<?php

      if(isset($_FILES['file'])){
  
    $file = $_FILES['file'] ;
  
    $error = $file['error'];
    $name= $file['name'] ;
    $tmp_name = $file['tmp_name'] ;
    $size = $file['size'] ;
  
    if($error == 0){
     //type restriction
     $ext =  explode(".", $name) ;
     $ext = end($ext) ;
     $ext = strtolower($ext ) ;
     $allow = array("jpg", "png") ;
   
     if(in_array($ext,  $allow)){
     
        // check file size
        if($size <= 2000000){
      
      //check wether file uploaded or not
      if(move_uploaded_file( $tmp_name, $name)){
       
       echo $name ;
      }else{
       echo 'file not uploaded' ;
      }
      
     }else{
      echo 'File is too big' ;
     }
    
    
     }else{
      echo 'Type not allowed';
     }
   
   
   
   
   
    }else{
   
     echo 'error in file';
    }
  
  
  
  
   }

 ?>
</div>

<div class="main">
    
        <form method="POST">
            <div id="name">
                <h2 class="name">
Name </h2>
<input class="firstname" type="text" name="first_name">
<br>
                <label class="firstlabel">first name</label>
                <input class="lastname" type="text" name="last_name"><br>
                <label class="lastlabel">last name</label>
            </div>

</body>
<br>
Club</h2>
<br>
<input class="firstname" type="text" name="first_name">
            <h2 class="name">
Age</h2>
<input class="company" type="text" name="company">
            <h2 class="name">
Phone</h2>
<input class="Code" type="text" name="area_code">
            <label class="area-code">Area Code</label>
            <input class="number" type="text" name="phone">
            <label class="phone-number">Phone Number</label>
    
    
            <h2 class="name">
Position</h2>
<select class="option" name="subject">
                <option disabled="disabled" selected="selected">--Choose option--</option>
                <option>Forward</option>
                <option>Center Midfielder</option>
                <option>Defensive Midfielder</option>
 		<option>Defense</option>
		<option>GoalKeeper</option>
            </select>
    
            <h2 id="coustomer">

            <button type="submit">Register</button>
    
    
        </form>
</div>
</body>
</html>
