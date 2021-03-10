
<!DOCTYPE html>
<html>
    <head>
        <meta charset="utf-8"/>
        <meta name="viewport" content="width=device-width,initial-scale=1"/>
        <title>Live Frame | Codeframe</title>
    </head>
    <body>
        <style>
    body {
        font-family: system-ui, sans-serif;
        width: 96%;
        max-width: 600px;
        margin: 0 auto;
    }
    p {
        line-height: 1.5em;
    }
    #clock {
        color: black;
        //background-color: #95E1D3;
        //background-color: #A7E0CE;
        //height: 2em;
    }
    #cycleNum {
        background-color: #95E1D3;
    }
    .flex-container {
        display: flex;
        background-color: white;//#A7E0CE;
        flex-direction: column;
        width: 100%;
        border: 3px solid #333;
        //border-radius: 10px;
        box-shadow: 5px 5px;
    }
    .centerAll {
        justify-content: center;
        align-items: center;
    }
    .clockBox {
        width: 100%;
        background-color: #95E1D3;
    }
    .flex-container,
    .flex-item {
        box-sizing: border-box;
    }
    .flex-item {
        margin-left: 10px;
        margin-right: 10px;
    }
    button {
        background-color: #95E1D3;
        border: 3px solid #333;
        //border-radius: 10px;
        font-family: system-ui, sans-serif;
        box-shadow: 3px 3px;
        outline: none;
        font-weight: bold;
        width: 49.5%;
        justify-content: center;
    }
    button:hover {
        background-color: #0E9E6F;
        color: #FFFFFF;
        box-shadow: 2px 2px #000000;
    }
    h1 {
        margin-left: 15px;
        margin-right: 15px;
    }
</style>

<br>
<div class="flex-container centerAll clockBox">
<h1><div id="clock"></div> </h1>
</div>
<br>
<!-- Fix display here -->
<div class="flex-container centerAll" id="pomoBox">
<div class="flex-item">
    <h1><span id="pomoStatusWords"></span><span id="pomoStatus"></span></h1>
</div>
<div class="flex-item">
    <h1><div id="pomo"></div></h1>
</div>
</div>
<br>
<div class="flex-container centerAll" >
    <h1><span>Since reloading the page, you have completed&nbsp</span><span id="cycleNum"></span>
</div>
<br>
<button id="startPomo">Start Timer</button>
<button id="pausePomo">Pause Timer</button>
<!-- Add stop/pause button -->
        <script src="https://unpkg.com/torus-dom/dist/index.min.js"></script>
        <script>function updateClock()
{
    //Get current date and h:m:s
    var d = new Date();
    var h = d.getHours();
    var m = d.getMinutes();
    var s = d.getSeconds();
    //Adjust minutes and seconds to always show two digits
    if(m < 10)
    {
        var m = "0"+m;
    }
    if(s < 10)
    {
        var s = "0"+s;
    }
    //Get "clock" element to update with time
    var salutation = "Good morning! ";
    var ampm = "AM";
    if(h>=17)
    {
        salutation = "Good evening! ";
        h = h-12;
        ampm = "PM";
    } else if(h>11 && h < 17) {
        salutation = "Good afternoon! ";
        if (h > 12)
        {
            h = h-12;
        }
        ampm = "PM";
    }
    document.getElementById('clock').innerHTML = salutation + "It's currently "+h+":"+m+" "+ampm; 
    //Update every second
    setTimeout(updateClock, 1000);
}
//Call update clock function
updateClock();

//Set global variables
var currentTime = new Date();
var diffReset = 45;
var breakReset = 15;
var diff = diffReset;
var breakTime = breakReset;
var pomoEndTime = new Date(currentTime.getTime() + diff*60000);
var pomoOn = true;
var breakEndTime = new Date(pomoEndTime.getTime() + breakTime*60000);
var lastPomoMin = Math.floor(diffReset);
var lastPomoSec = Math.floor((diffReset-lastPomoMin)*60);
var lastBreakMin = Math.floor(breakReset);
var lastBreakSec = Math.floor((breakReset-lastBreakMin)*60);
var switchState = false;
var cyclesCompleted = 0;
if(lastPomoSec < 10)
{
    var lastPomoSec = "0"+lastPomoSec;
}
if(lastBreakSec < 10)
{
    var lastBreakSec = "0"+lastBreakSec;
}
var pomoPause = true;

function updatePomo()
{
    //Get pomoEndTime
    var d = new Date();
    if(!pomoPause)
    {
         var msDiff = pomoEndTime-d;
         if(!pomoOn)
        {
            msDiff = breakEndTime-d;
            diff = diffReset;
            pomoEndTime = new Date(breakEndTime.getTime() + diff*60000 + 1000);
        } else {
            breakTime = breakReset;
            breakEndTime = new Date(pomoEndTime.getTime() + breakTime*60000 + 1000);
        }
        var secDiff = msDiff/1000 + 1;
        var minDiff = secDiff/60;
        var m = Math.floor(minDiff);
        var s = Math.floor((minDiff-m)*60);
        //Adjust minutes and seconds to always show two digits
        if(m < 10)
        {
            var m = "0"+m;
        }
        if(s < 10)
        {
            var s = "0"+s;
        }
        if (msDiff <= 0)
        {
            m = "00";
            s = "00";
            pomoOn = !pomoOn;
            switchState = true;
            if(!pomoOn) {
                cyclesCompleted = cyclesCompleted + 1;
            }
        } else {
            switchState = false;
        }
    }
    if(pomoPause)
    {
        if(pomoOn) {
            m = lastPomoMin;
            s = lastPomoSec;
        } else {
            m = lastBreakMin;
            s = lastBreakSec;
        }
    }
    if(pomoOn) {
        lastPomoMin = m;
        lastPomoSec = s;
    } else {
        lastBreakMin = m;
        lastBreakSec = s;
    } 
    //Update UI blocks
    if(pomoPause) {
        document.getElementById('pomoStatusWords').innerHTML = "Right now, your timer is ";
        document.getElementById('pomoStatus').innerHTML = "&nbsppaused.&nbsp"
        document.getElementById('pomoStatus').style.backgroundColor = "#FCE38A";
        //document.getElementById('pomoBox').style.backgroundColor = "#ffe396";
    } else if((!pomoOn && !switchState) || (pomoOn && switchState)){
        document.getElementById('pomoStatusWords').innerHTML = "Right now, you're on a ";
        document.getElementById('pomoStatus').innerHTML = "&nbspbreak :)&nbsp"
        document.getElementById('pomoStatus').style.backgroundColor = "#95E1D3";
        //document.getElementById('pomoBox').style.backgroundColor = "#A7E0CE";
    } else if (pomoOn || (!pomoOn && switchState))
    {
        document.getElementById('pomoStatusWords').innerHTML = "Right now, you should be ";
        document.getElementById('pomoStatus').innerHTML = "&nbspworking.&nbsp"
        document.getElementById('pomoStatus').style.backgroundColor = "#ff75a0";
        //document.getElementById('pomoBox').style.backgroundColor = "#eba0a0";
    }
    //Get "clock" element to update with time
    if(cyclesCompleted == 1) {
        document.getElementById('cycleNum').innerHTML = "&nbsp"+cyclesCompleted+"&nbspwork cycle.&nbsp";
    } else {
        document.getElementById('cycleNum').innerHTML = "&nbsp"+cyclesCompleted+"&nbspwork cycles.&nbsp";
    }
    document.getElementById('pomo').innerHTML = "Time remaining: "+m+":"+s; 
    //document.getElementById('clock').backgroundColor = "red";//#A7E0CE";
    //Update every second
    setTimeout(updatePomo, 1000);
}
//Call update clock function
updatePomo();


document.getElementById("startPomo").addEventListener("click", resetPomo);
function resetPomo()
{
   //TODO
    var oldDate = new Date();
    if(pomoOn)
    {
        if(pomoPause)
        {
            pomoPause = false;
            diff = lastPomoMin + lastPomoSec/60;
            pomoEndTime = new Date(oldDate.getTime() + diff*60000);
        }     
    } else {
        if(pomoPause)
        {
            pomoPause = false;
            breakTime = lastBreakMin + lastBreakSec/60;
            breakEndTime = new Date(oldDate.getTime() + breakTime*60000);
        }
    }
    
    //Get "clock" element to update with time
    //document.getElementById('pomo').innerHTML = "The current time on your pomodoro timer is "+h+":"+m+":"+s; 
   //document.getElementById('startPomo').style.backgroundColor = "#A7E0CE"; 
}


document.getElementById("pausePomo").addEventListener("click", pausePomo);
function pausePomo()
{
   //TODO
    pomoPause = true;
    //Get "clock" element to update with time
    //document.getElementById('pomo').innerHTML = "The current time on your pomodoro timer is "+h+":"+m+":"+s; 
   //document.getElementById('startPomo').style.backgroundColor = "#A7E0CE"; 
}</script>
    </body>
</html>
