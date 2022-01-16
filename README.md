# Web Page for Mathematical Calculations

## AIM:

To design a static website with validation to perform mathematical calculations in client side.

## DESIGN STEPS:

### Step 1:

Requirement collection.

### Step 2:

Creating the layout using HTML and CSS.

### Step 3:

Write javascript to perform the calculations.

### Step 4:

Include regularexpression based input validation.

### Step 5:

Validate the layout in various browsers.

### Step 6:

Validate the HTML code.

### Step 6:

Publish the website in the given URL.

## PROGRAM :
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mathematical Calculation</title>
    <style>
        * {
            box-sizing: border-box;
            font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
        }
        body {
            background-color:rgb(88, 45, 99);
        }
        .container {
            width: 1080px;
            margin-left: auto;
            margin-right: auto;
        }
        .box1{
            width: 500px;
            margin-left: auto;
            margin-right: auto;
            height: 500px; 
        }
        .content {
            display: block;
            width: 100%;
            background-color: rgb(191, 143, 245);
            margin-top: 50px;
            min-height: 500px;
        }
        .content1 {
          display: block;
            width: 100%;
            background-color: rgb(191, 143, 245);
            margin-top: 30px;
            min-height: 500px;
        }
        h1{
            text-align: center;
            font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif;
            padding-top: 20px;
            font-size: 55px;
        }
        .formelement{
            text-align: center;
            padding-bottom: 15px;
            font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
            font-size: 35px;
        }
        .footer{
            text-align: right;
            padding-right:20px;
            color:white;
            font-size: 35px
        }

    </style>
</head>
<body>
    <div class="container">
        <div class="content">
            <div class="box1">
                <h1>Volume Of Cone</h1>
                <form>
                   <div class="formelement">
                        <label for="aedit" >Radius =</label>
                        <input type="text" id="aedit" value="0"/>Meters
                        
                    </div> 
                    <div class="formelement">
                        <label for="bedit">Height =</label>
                        <input type="text" id="bedit" value="0" />Meters
                        
                    </div>
                    <div class="formelement">
                         <input type="button" value="CALCULATE VOLUME" id="addbutton"/>
                    </div>
                    <div class="formelement">
                        <label for="cedit">Volume =</label>
                        <input type="text" id="cedit" value="0" readonly />Meter<sup>3</sup>
                        
                    </div>
                </form>
            </div>
           
        </div>
    </div>
<script>
    var button;
    button=document.querySelector("#addbutton");
    button.addEventListener("click",function(){
        var atext,btext,ctext;
        var aval,bval,cval;
        var pi;
        atext=document.querySelector("#aedit");
        btext=document.querySelector("#bedit");
        ctext=document.querySelector("#cedit");

        rexp=new RegExp("^[1-9]+[0-9]*$");
     
        aval=atext.value;
        r1=aval.match(rexp);
        bval=btext.value;
        r2=bval.match(rexp)
        pi=3.14;
        

        if(r1==null)
        {
            alert("Please Enter Positive Integers Only for Radius");
        }
        if(r2==null)
        {
            alert("Please Enter Positive Integers Only for Height");
        }
        
        cval=pi*aval*aval*bval/3;
        ctext.value=" "+cval;
    
    });
</script>   
    <div class="container">
        <div class="content1">
            <div class="box1">
                <h1>Area Of a Triangle</h1>
                <form>
                   <div class="formelement">
                        <label for="dedit" >Base  =</label>
                        <input type="text" id="dedit" value="0"/>Meters
                    </div> 
                    <div class="formelement">
                        <label for="eedit">Height =</label>
                        <input type="text" id="eedit" value="0"/>Meters
                    </div>
                    <div class="formelement">
                         <input type="button" value="CALCULATE AREA" id="addbuttons"/>
                    </div>
                    <div class="formelement">
                        <label for="fedit">Area =</label>
                        <input type="text" id="fedit" value="0" readonly />Meter<sup>3</sup>
                    </div>
                    
                </form>
            </div>
           
        </div>
        <div class="footer">
            <p>Developed by Naga durga</p>
        </div>
    </div>

<script>
  var button;
  button=document.querySelector("#addbuttons");
  button.addEventListener("click",function(){
      var dtext,etext,ftext;
      var dval,eval,fval;
 
      dtext=document.querySelector("#dedit");
      etext=document.querySelector("#eedit");
      ftext=document.querySelector("#fedit");

      rexp=new RegExp("^[1-9]+[0-9]*$");

      dval=dtext.value;
      r3=dval.match(rexp);
      eval=etext.value;
      r4=eval.match(rexp)

      if(r3==null)
      {
         alert("Please Enter Positive Integers Only for Base");
      }
      if(r4==null)
      {
         alert("Please Enter Positive Integers Only for Height");
      }
      fval=1/2*eval*dval;
      ftext.value=" "+fval;
  });
  
</script>    


</body>
</html>
```
## OUTPUT:

![output](./math.PNG)

## Result:

Thus a website is designed to perform mathematical calculations in the client side.
