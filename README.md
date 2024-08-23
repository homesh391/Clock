# Clock
<!DOCTYPE html>
<html lang="en" dir="ltr">
<head>
<meta charset="utf-8">
<title>Digital Clock with Glowing Effect </title>
<link rel="stylesheet" href="styless.css">
</head>
<body>
<div class="wrapper">
<div class="display">
<div id="time"></div>
</div>
<span></span>
<span></span>
</div>
<script> setInterval(()=>{
const time = document.querySelector(".display #time"); let date = new Date();
let hours = date.getHours();
 
let minutes = date.getMinutes(); let seconds = date.getSeconds(); let day_night = "AM";
if(hours > 12){ day_night = "PM"; hours = hours - 12;
}
if(seconds < 10){
seconds = "0" + seconds;
}
if(minutes < 10){
minutes = "0" + minutes;
}
if(hours < 10){
hours = "0" + hours;
}
time.textContent = hours + ":" + minutes + ":" + seconds + " "+ day_night;
});
</script>
</body>
</html>


CSS:
body{
margin: 0px; padding: 0px;
background-color: #011627;
 
color: #fdfffc; text-align: center;
background-position: center; background-repeat: no-repeat; background-size: cover; height: 100vh;
}
h1{
font-size: 45px;
}


input{
width: 75px; height: 50px; font-size: 45px;
border-radius: 10px; margin: 10px; background-color: white; color: black;
border-style: none;
}
.btn:hover{
background-color:yellow; cursor: pointer;
}
