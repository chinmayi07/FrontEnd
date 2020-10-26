# Link for repl.it
https://repl.it/join/agjkdhbp-18pa1a1207bezaw

# Video Link of the bot web page
https://youtu.be/Sx5GpQtO01Y

# Code for Front End of the bot(HTML,CSS,JS)
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width">
    <title>repl.it</title>
    <link href="style.css" rel="stylesheet" type="text/css" />
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.4.1/css/bootstrap.min.css" integrity="sha384-Vkoo8x4CGsO3+Hhxv8T/Q5PaXtkKtu6ug5TOeNV6gBiFeWPGFN9MuhOf23Q9Ifjh" crossorigin="anonymous" />
<link rel="stylesheet" href="https://use.fontawesome.com/releases/v5.7.0/css/all.css" integrity="sha384-lZN37f5QGtY3VHgisS14W3ExzMWZxybE1SJSEsQp9S+oqd12jhcu+A56Ebc1zFSJ" crossorigin="anonymous" />
  </head>
  <body class="body">
    <script src="script.js"></script>
   <nav class="navbar navbar-expand-sm navsize">
     <a class="navbar-brand" href="#">
       <img src="https://i.pinimg.com/originals/9a/11/33/9a1133d4af3b637e1c6c8ff251785f27.jpg" class="img1">
     </a>
     <ul class="navbar-nav">
       <li class="nav-item"><a href="#" class="nav-link white send"><span class="fas-fa-home">Home</span></a></li>
       <li class="nav-item"><a href="#" class="nav-link white"><span class="fas-fa-phone">ContactUs</span></a></li>
       <li class="nav-item"><a href="#" class="nav-link white"><span class="fas-fa-home">News</span></a></li>
       <li class="nav-item"><a href="#" class="nav-link white"><span class="fas-fa-home">Info</span></a></li>
       <li class="nav-item"><a href="#" class="nav-link white"><span class="fas-fa-home">AboutUs</span></a></li>
       </ul>
       </nav>
       <h1 class="h1 white">TALK TO BOT!...</h1>
       <p class="white size"><b><i>Hello! Welcome to chatbot.I am here to tell you<br> about the weather in the place that you would like<br> and also date and time of your place and also<br> of any place.Let's chat!...</b></i></p>
       <div class="chatbot">
         <input type="text" placeholder="Enter message" id="input1" class="inp1"><br>
         <button onclick='greet()' class="btn btn-primary b1">Click</button>
         <p id='demo' class="p1"></p>
         <input type="text" placeholder="what do you want to know" class="inp2">
         <br>
         <button onclick='show_menu()' class="btn btn-primary b2">Click</button>
         <p id="demo1" class="p2"></p>
         <input type="text" placeholder="Tell your choice" class="inp3">
         <br>
         <button onclick='display()' class="btn btn-primary b3">Click</button>
         <p id="demo2" class="p3"></p>
       </div>
  </body>
</html>

CSS:

.send{
  margin-left:1000px;
}

.h1{
  margin-left:1080px;
  margin-top:40px;
}
.chatbot{
  margin-top: -120px;
  background:rgba(0, 0, 0, 0.582);
    height: 550px;
    width: 500px;
    border-radius: 40px;
    margin-left:1000px;
}

.inp1{
  width:300px;
  height:60px;
  margin-left:35px;
  margin-top:35px;
  border-radius: 30px;
}

.inp2{
  width:300px;
  height:60px;
  margin-left:35px;
  margin-top:10px;
  border-radius: 30px;
}

.inp3{
  width:300px;
  height:60px;
  margin-left:35px;
  margin-top:10px;
  border-radius: 30px;
}

.b1{
  margin-left: 50px;
  margin-top:3px;
}

.b2{
  margin-left: 50px;
  margin-top:3px;
}

.b3{
  margin-left: 50px;
  margin-top:3px;
}

.p1{
  background: white;
  width:420px;
  border-radius:30px;
  margin-left:75px;
  margin-top: 10px;
}

.p2{
  background: white;
  width:420px;
  border-radius:30px;
  margin-left:75px;
  margin-top: 10px;
}

.p3{
  background: white;
  width:420px;
  border-radius:30px;
  margin-left:75px;
margin-top: 10px;
}

Java Script:

function greet(){
  var name= prompt("  Hello I am bot!..May I know your name please?", "Name: ");
  if (name!=null) {
    document.getElementById("demo").innerHTML="Hello " + name+ "! How are you today? How can I help you?";
  }
}

function show_menu(){
  document.getElementById("demo1").innerHTML="1.I will tell you the date and time of your place<br>2.I will tell you the weather of a place"
}

function display(){
  var choice=prompt("What do you want to know out of the two choices given?");
  if(choice!=null){
    if(choice=="what is the date and time now"){
      var date=new Date();
      document.getElementById('demo2').innerHTML="Date: "+date.getDate()+"-"+date.getMonth()+"-"+date.getFullYear()+"<br>Time: "+date.getHours()+":"+date.getMinutes()+":"+date.getSeconds();
    }
    else if(choice=="what is the weather in Vijayawada"){
      document.getElementById('demo2').innerHTML="The temperature in Vijayawada is 30 degrees and it is cloudy."
    }
    else if(choice=="what is the weather in Bhimavaram"){
      document.getElementById('demo2').innerHTML="The temperature in Bhimavaram is 35 degrees and it is sunny.";
    }
    else if(choice=="what is the weather in Hyderabad"){
      document.getElementById('demo2').innerHTML="The temperature in Hyderabad is 28 degrees and it is raining heavily.";
    }
    else if(choice=="what is the weather in Sarvepalli"){
      document.getElementById('demo2').innerHTML="Enter the correct city name to know weather.";
    }
    else if(choice=="End this chat"){
      document.getElementById("demo2").innerHTML="Thank you.Let's meet again";
    }
  }
  else if(choice==null){
    document.getElementById('demo2').innerHTML="Enter the right choice."
  }
}







