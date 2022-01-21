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
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Canvas Application</title>
    <style>
        .maincontainer{
            text-align: center;
            color: whitesmoke;
        }
        body{
            background-color:#B8143A;
        }
        canvas{
            background-color: white;
        }
    </style>

<script type="text/javascript">
var shape;
var color;
function myClickEvent(e){
        var ctx = c.getContext("2d");
        ctx.beginPath();
        if(color==1){
            ctx.strokeStyle='red';
        }else if(color==2){
            ctx.strokeStyle='yellow';
        }else if(color==3){
            ctx.strokeStyle='blue';
        }
        if(shape == 0){
            ctx.arc(e.offsetX,e.offsetY, 45, 0, 2 * Math.PI);
            ctx.stroke();
            
        }else if(shape == 1){

            ctx.moveTo(75, 50);
            ctx.lineTo(100, 75);
            ctx.lineTo(100, 25);
            ctx.closePath();
            ctx.stroke();
            
        }else if(shape==2){
            ctx.rect(e.offsetX,e.offsetY, 150, 100);
            ctx.stroke();


        }else if(shape==3){
            ctx.rect(e.offsetX, e.offsetY, 50, 50);
            ctx.stroke();
        }
    }

        function circleClicked(){
            shape=0;
        }
        function triangleClicked(){
            shape=1;
        }
        function rectangleClicked(){
            shape=2;
        }
        function squareClicked(){
            shape=3;
        }
        function redClicked(){
            color=1;
        }
        function blueClicked(){
            color=3;
        }
        function yellowClicked(){
            color=2;
        }

</script>
</head>
<body>
    <div class="maincontainer">
        <h1><u>Canvas Drawing Application</u></h1>
    <canvas id="myCanvas" width="800" height="800" style="border:2px solid #000000 ;border-radius: 4px;"></canvas>
    <div>
        <input type="button" id="circle" value="Circle">
        <input type="button" id="line" value="Triangle">
        <input type="button" id="rectangle" value="Rectangle">
        <input type="button" id="square" value="Square">
        
    </div>
    <div>
        <input type="button" id="red" value="Red">
        <input type="button" id="blue" value="Blue">
        <input type="button" id="yellow" value="Yellow">
    </div>
        <script type ="text/javascript">
            var c = document.getElementById("myCanvas");
            c.addEventListener("click", myClickEvent);
            document.getElementById("circle").addEventListener("click", circleClicked);
            document.getElementById("line").addEventListener("click",  triangleClicked);
            document.getElementById("rectangle").addEventListener("click",rectangleClicked);
            document.getElementById("square").addEventListener("click",squareClicked);
            document.getElementById("red").addEventListener("click",redClicked);
            document.getElementById("blue").addEventListener("click",blueClicked);
            document.getElementById("yellow").addEventListener("click",yellowClicked);
           
        </script>
</body>
</html>
~~~

## OUTPUT:

![GitHub Logo](app.jpg)

## Result:

Thus a website is designed and validated for paint application using HTML5 canvas.
