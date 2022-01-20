# Web Page for Paint Application

## AIM:

To design a static website for Paint Application using HTML5 canvas.

## DESIGN STEPS:

### Step 1:

Requirement collection.

### Step 2:

Creating the layout using HTML,CSS and canvas.

### Step 3:

Write javascript to capture move events.

### Step 4:

Perform the drawing operation based on the user input.

### Step 5:

Validate the layout in various browsers.

### Step 6:

Validate the HTML code.

### Step 6:

Publish the website in the given URL.

## PROGRAM :

~~~
<!DOCTYPE html>
<html>
<body id="Jaeger">
    <h1>Canvas Painting Application</h1>
    <div id="light">
<canvas id="myCanvas" width="800" height="800" onclick="showCoords(event)"></canvas></div>
<center>
<button onclick="shape=1" id="Eren" >Rectangle</button>
<button onclick="shape=2" id="Eren">Circle</button>
<button onclick="shape=4" id="Eren">Square</button>
<button onclick="shape=6" id="Eren">Triangle</button>
<br>
<center>
<button onclick="change_color(this)" id="Yagami" style="background: rgb(153, 0, 255);"></button>
<button onclick="change_color(this)" id="Yagami" style="background: rgb(54, 0, 124);"></button>
<button onclick="change_color(this)" id="Yagami" style="background: #f30c0c;"></button>
</center>

<script>


const canvas = document.getElementById("myCanvas");
const ctx = canvas.getContext("2d");
ctx.fillStyle = "#FF0000";
canvas.height = canvas.width;
ctx.transform(1, 0, 0, -1, 0, canvas.height);
let xMax = canvas.height;
let yMax = canvas.width;
let lsize=50;
let bsize=30;
let csize= 20;
let sqsize= 50;
let tsize=30;
let tatakae="black";

function change_color(element){
    tatakae=element.style.background;
}

    function showCoords(event)

    {
    var x = event.clientX-545;
    var y = yMax-event.clientY;
    var coords = "X coords: " + x + ", Y coords: " + y;
    document.getElementById("demo").innerHTML = coords;
    
        if (shape==1){
            ctx.beginPath();
            ctx.rect(x,y, lsize,bsize);
            ctx.strokeStyle=tatakae;
            ctx.stroke();
        }
        if (shape==2){
            ctx.beginPath();
            ctx.arc(x, y, csize, 0, 2 * Math.PI);
            ctx.strokeStyle=tatakae;
            ctx.stroke();
        }
        
        if (shape==4){
            ctx.beginPath();
            ctx.rect(x-(sqsize/2),y-(sqsize/2), sqsize,sqsize);
            ctx.strokeStyle=tatakae;
            ctx.stroke();
        }
        if (shape==6){
            ctx.beginPath();
            ctx.moveTo(x, y);
            ctx.lineTo(x-(tsize/2),y-(tsize*0.86602));
            ctx.lineTo(x+(tsize/2),y-(tsize*0.86602));
            ctx.lineTo(x,y)
            ctx.strokeStyle=tatakae
            ctx.stroke();
        }
     
    
}

</script>
<center><p id="demo" style="color: white;"></p></center>
<p style="color: white; font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;" >Developed By Yuvadarshini S</p>
<style>
h1{
    font-family: Georgia, 'Times New Roman', Times, serif;
    text-align: center;
    color: whitesmoke;
    font-size: 60px;
}
#light{
    padding-left: 545px;
   
}
#myCanvas{
    padding-left: 500px;
    background-color: #ffffff; 
    border: 5px solid black;
}
#Eren{
    background-color: gainsboro;
    border: 2px solid black;
    color: black;
    padding: 15px 32px;
    text-align: justify;
    display: inline-block;
    font-size: 16px;
    margin: 4px 2px;
    cursor: pointer;
}


#Jaeger{
    background-color:#B8143A;
}
#Yagami{
    border: 2px solid #ffffff;
    border-radius: 25px;
    padding: 25px 25px;
    text-align: center;
    display: inline-block;
    font-size: 16px;
    margin: 4px 2px;
    cursor: pointer;
}

</style>
</body>
</html>

~~~

## OUTPUT:

![GitHub Logo](app.jpg)

## Result:

Thus a website is designed and validated for paint application using HTML5 canvas.
