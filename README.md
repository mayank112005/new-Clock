<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.0.2/dist/js/bootstrap.bundle.min.js"></script>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.0.2/dist/css/bootstrap.min.css" rel="stylesheet">
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap-icons@1.11.3/font/bootstrap-icons.min.css">
    <title>Clock </title>
<style>
  #clock {
    font-family: Arial, sans-serif;
    font-size: 48px;
    text-align: center;
    margin-top: 100px;
    color:#333;
  }
  body{
    background-image: url('https://i.pinimg.com/originals/f1/15/5d/f1155d9669cb046a23e2217a8bb9f2e1.gif');
    background-size: cover;
    background-repeat: no-repeat;
    padding:5%;
  }
  #bd{
   
    height: 200px;
    width: 200px;
  
  }
  #clock{
    color: aliceblue;
  }
</style>
</head>
<body>
<div id="bd" class="container">
    <div id="clock"></div>
</div>
<audio autoplay loop  > 
  <source src="zombie-attack-6419.mp3" type="audio/ogg" >

Your browser does not support the audio element.
</audio> 
<script>
function updateClock() {
  var now = new Date();
  var hours = now.getHours();
  var minutes = now.getMinutes();
  var seconds = now.getSeconds();
  
  hours = hours < 10 ? '0' + hours : hours;
  minutes = minutes < 10 ? '0' + minutes : minutes;
  seconds = seconds < 10 ? '0' + seconds : seconds;
  
  var timeString = hours + ':' + minutes + ':' + seconds;
  
  document.getElementById('clock').innerText = timeString;
}

// Call updateClock every second
setInterval(updateClock, 1000);

// Initial call to display the clock immediately
updateClock();
</script>
</body>
</html>
