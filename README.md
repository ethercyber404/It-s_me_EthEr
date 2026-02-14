<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>ONLY FOR SAIKA...🙈</title>
<style>
body{
    margin:0;
    font-family: 'Poppins', sans-serif;
    text-align:center;
    background: linear-gradient(135deg,#ff9ec4,#ffcce6);
    overflow:hidden;
}
.screen{
    display:none;
    padding-top:120px;
    color:white;
}

button{
    padding:15px 30px;
    font-size:22px;
    border:none;
    border-radius:30px;
    cursor:pointer;
    margin:20px;
    transition:.3s;
}

#intro{ display:block; }

#no{
    position:absolute;
    background:gray;
    color:white;
}

#yes{
    background:#ff4d88;
    color:white;
}

.heart{
    position:absolute;
    animation: float 5s linear infinite;
    z-index:999;
}

@keyframes float{
    0%{transform:translateY(100vh);opacity:1;}
    100%{transform:translateY(-10vh);opacity:0;}
}
</style>
</head>

<body>

<!-- Hidden YouTube music iframe -->
<iframe
  id="music"
  width="1"
  height="1"
  src=""
  frameborder="0"
  allow="autoplay; encrypted-media">
</iframe>

<div id="intro" class="screen">
    <h1>HEY SAIKA😅</h1>
    <button onclick="start()">Tap Koro..🙃</button>
</div>

<div id="loading" class="screen">
    <h1>Checking Our Love Compatibility... 💞</h1>
    <h2 id="percent">0%</h2>
</div>

<div id="question" class="screen">
    <h1>Will you be my Valentine?!😁💖</h1>
    <h6>কেউ নাই! তাই তোমারে দিলাম 🫣|আর সুন্দর কেউ নাই list এ</h6>
    <button id="yes">Yes😍</button>
    <button id="no">No!😌</button>
    <h6>Hints : The No! button is a Bit Say...🙈</h6>
    
</div>

<div id="final" class="screen">
    <h1>Yea! Good choice!- আমি জানতাম!!🥰</h1>
    <!-- Cute animated couple GIF -->
[<img src="https://gifdb.com/gif/cute-animated-couple-i-love-you-jpt2cd82u5cw79my.html" width="300" alt="I Love You Couple GIF">](https://dl.glitter-graphics.com/pub/2561/2561941mue86g3ygg.gif
)


</div>

<script>
// Start function for intro
function start(){
    document.getElementById("intro").style.display="none";
    document.getElementById("loading").style.display="block";

    // Set music src after user click to allow autoplay
    document.getElementById("music").src =
        "https://www.youtube.com/embed/WeXVuFG9MZU?autoplay=1&loop=1&playlist=WeXVuFG9MZU&mute=0";

    let percent = 0;
    let interval = setInterval(()=>{
        percent++;
        document.getElementById("percent").innerText = percent + "%";

        if(percent >= 100){
            clearInterval(interval);
            showQuestion();
        }
    },30);
}

function showQuestion(){
    document.getElementById("loading").style.display="none";
    document.getElementById("question").style.display="block";
}

// No button dodging
let noBtn = document.getElementById("no");
let yesBtn = document.getElementById("yes");
let size = 22;

noBtn.addEventListener("mouseover", function(){
    let x = Math.random()*(window.innerWidth-120);
    let y = Math.random()*(window.innerHeight-120);
    noBtn.style.left = x+"px";
    noBtn.style.top = y+"px";

    size += 5;
    yesBtn.style.fontSize = size+"px";
});

// Yes button click
yesBtn.addEventListener("click", function(){
    document.getElementById("question").style.display="none";
    document.getElementById("final").style.display="block";
    launchHearts();
});

// Floating hearts animation
function launchHearts(){
    for(let i=0;i<50;i++){
        let heart=document.createElement("div");
        heart.classList.add("heart");
        heart.innerHTML="💖";
        heart.style.left=Math.random()*100+"vw";
        heart.style.fontSize=(20+Math.random()*30)+"px";
        document.body.appendChild(heart);
        setTimeout(()=>heart.remove(),5000);
    }
}
</script>

</body>
</html>

