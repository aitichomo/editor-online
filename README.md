# editor-online
<!DOCTYPE html>
<html >
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/boot/bootstrap/4.5.0/css/bootstrap.min.css" crossorigin="anonymous">
    <link rel="icon" href="logoh.jpg">
    <title> Editor-code</title>
  <style>
    nav img{
    max-width: 64px;
    max-height: 64px;
    object-fit: scale-down;
    border-radius: 50%;
    margin-left: 80%;
 
}
main{
    text-align: center;
}
#codes{
    width: 98%;
    min-height: 280px;
    border-radius: 20px;
    border: 2px solid rgb(131, 131, 131);
    margin-top: 20px;
}
#buttons{
    display: flex;
    justify-content: space-evenly;
}
#buttons button {
    border-radius: 12px;
    width: 40%;
    border: 0px;
    padding: 14px;

} 
#remove{
    background-color: rgb(216, 37, 37);
    color: white;
}
#play{
    background-color: rgb(39, 36, 36);
    color: white;
}
#result{
    padding: 15px;
    border-bottom: 2px solid rgb(131,131,131);
    margin:10px 0px ;
    font-weight: bold;
}
#mark{
    max-width: 100% !important;
}

#aid{
    font-style: oblique;
    font-weight: 1000;
    font-size: large;
}
</style>
 
</head>
<body>
    <nav>
        <a id="aid">
            Mustapha Editor
        </a>

        
      <img src="hack1.jpg" alt=""> 
      </nav> 
<main>
    <textarea name="" id="codes" cols="30" rows="10">
        <!DOCTYPE html>
        <html>
            <head></head>
            <body>
                
            </body>
        </html>
    </textarea>

    <div id="buttons">
        <button id="remove">Remove Code</button>
        <button id="play"> Play Code</button>
    </div>
    <p id="result"> Result Of Code</p>
</main>

<div id="mark">

</div>

    <script >
        let codes = document.getElementById("codes");
let play = document.getElementById("play");
let remove= document.getElementById("remove");
let mark = document.getElementById("mark");

play.onclick= ()=>{
    mark.innerHTML = codes.value ;
    localStorage.setItem("result",codes.value )
};

remove.onclick = ()=>{
    mark.innerHTML = "" ;
   // codes.value= "";
};

onload = ()=>{
  //codes.value = localStorage.getItem("result");
  mark.innerHTML = codes.value ;
};
    </script>
</body>
</html>
