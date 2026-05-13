<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>For Veda 🌷</title>
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&family=Dancing+Script:wght@700&display=swap" rel="stylesheet">

<style>
*{
    margin:0;
    padding:0;
    box-sizing:border-box;
}

body{
    overflow-x:hidden;
    overflow-y:auto;
    font-family:'Poppins',sans-serif;
    background:linear-gradient(to bottom,#0f172a,#1e293b,#111827);
    height:100vh;
    color:white;
}

canvas{
    position:fixed;
    top:0;
    left:0;
    width:100%;
    height:100%;
    z-index:-1;
}

.container{
    min-height:100vh;
    display:flex;
    justify-content:center;
    align-items:center;
    flex-direction:column;
    text-align:center;
    padding:20px;
}

h1{
    font-size:4rem;
    font-family:'Dancing Script',cursive;
    margin-bottom:20px;
    color:#ffd6e7;
    animation:glow 2s infinite alternate;
}

@keyframes glow{
    from{ text-shadow:0 0 10px #ff9ec7; }
    to{ text-shadow:0 0 25px #ffb6d5,0 0 40px #ff8db5; }
}

.message{
    max-width:750px;
    font-size:1.2rem;
    line-height:1.9;
    color:#f8fafc;
    opacity:0;
    transform:translateY(20px);
    transition:1s;
}

.message.show{
    opacity:1;
    transform:translateY(0);
}

.pot-area{
    position:relative;
    margin:30px 0;
    height:260px;
}

.pot{
    width:150px;
    height:220px;
    background:linear-gradient(to bottom,#d97706,#92400e);
    border-radius:18px 18px 45px 45px;
    position:relative;
    box-shadow:0 15px 30px rgba(0,0,0,0.35), inset 0 0 20px rgba(255,255,255,0.1);
    position:relative;
    margin:auto;
    transition:1s;
}

.pot::after{
    content:'';
    position:absolute;
    bottom:-18px;
    left:15px;
    width:120px;
    height:25px;
    background:rgba(0,0,0,0.2);
    border-radius:50%;
    filter:blur(6px);
}

.pot::before{
    content:'';
    position:absolute;
    top:20px;
    left:15px;
    right:15px;
    height:25px;
    background:rgba(255,255,255,0.12);
    border-radius:20px;
}

.crack{
    position:absolute;
    width:5px;
    height:130px;
    background:#f8fafc;
    left:48%;
    top:10px;
    transform:rotate(20deg);
    opacity:1;
    transition:1s;
}

.tulip{
    position:absolute;
    width:16px;
    height:42px;
    background:linear-gradient(to top,#16a34a,#4ade80);
    bottom:145px;
}

.tulip::after{
    content:'';
    position:absolute;
    width:30px;
    height:15px;
    background:#22c55e;
    border-radius:50%;
    left:-10px;
    top:15px;
    transform:rotate(-30deg);
}

.tulip::before{
    content:'';
    position:absolute;
    width:24px;
    height:24px;
    background:linear-gradient(to bottom,#ff4d88,#ff80ab);
    border-radius:50% 50% 35% 35%;
    top:-16px;
    left:-4px;
    box-shadow:0 0 15px #ff80ab;
}

.t1{ left:40px; }
.t2{ right:40px; }

.buttons{
    display:flex;
    gap:20px;
    flex-wrap:wrap;
    justify-content:center;
    margin-top:20px;
}

button{
    padding:15px 28px;
    border:none;
    border-radius:50px;
    background:linear-gradient(45deg,#ff5f9e,#ff8fab);
    color:white;
    font-size:1rem;
    cursor:pointer;
    transition:0.4s;
    box-shadow:0 0 20px rgba(255,105,180,0.4);
}

button:hover{
    transform:scale(1.1);
    box-shadow:0 0 30px rgba(255,182,193,0.8);
}

.sparkle{
    position:absolute;
    width:4px;
    height:4px;
    background:white;
    border-radius:50%;
    animation:twinkle 2s infinite;
}

@keyframes twinkle{
    0%{opacity:0.2;transform:scale(1)}
    50%{opacity:1;transform:scale(2)}
    100%{opacity:0.2;transform:scale(1)}
}

.final-scene{
    position:absolute;
    inset:0;
    display:flex;
    justify-content:center;
    align-items:center;
    flex-direction:column;
    opacity:0;
    pointer-events:none;
    transition:2s;
    background:radial-gradient(circle at center,#ff9ec7 0%,#1e293b 60%,#0f172a 100%);
}

.final-scene.show{
    opacity:1;
}

.final-text{
    max-width:850px;
    font-size:1.3rem;
    line-height:2;
    padding:20px;
}

.highlight{
    color:#ffe066;
    font-weight:700;
}

.big-tulips{
    font-size:5rem;
    animation:float 3s infinite ease-in-out;
}

@keyframes float{
    0%{ transform:translateY(0px); }
    50%{ transform:translateY(-15px); }
    100%{ transform:translateY(0px); }
}

.petals{
    position:absolute;
    width:15px;
    height:15px;
    background:pink;
    border-radius:50% 0 50% 50%;
    opacity:0.7;
    animation:fall linear infinite;
}

@keyframes fall{
    from{
        transform:translateY(-100px) rotate(0deg);
    }
    to{
        transform:translateY(110vh) rotate(360deg);
    }
}

.typewriter{
    overflow:hidden;
    border-right:3px solid white;
    white-space:nowrap;
    animation:typing 5s steps(40,end),blink .8s infinite;
}

@keyframes typing{
    from{ width:0 }
    to{ width:100% }
}

@keyframes blink{
    50%{ border-color:transparent }
}

@media(max-width:768px){
    h1{
        font-size:2.8rem;
    }

    .message,.final-text{
        font-size:1rem;
    }

    .typewriter{
        white-space:normal;
        border:none;
        animation:none;
    }
}
</style>
</head>
<body>

<canvas id="stars"></canvas>

<div class="container">

<audio autoplay loop>
<source src="https://cdn.pixabay.com/download/audio/2022/03/15/audio_c8c8e1b3d1.mp3?filename=beautiful-piano-ambient-110624.mp3" type="audio/mpeg">
</audio>

<h1>For Veda 🌷</h1>

<div class="message show" id="msg">
<p style="margin-bottom:20px;font-size:1.1rem;color:#ffd1dc;">
Some things feel special simply because someone cared about them the way you did, Veda 🌷
</p>
<div class="typewriter">
I know it felt bad seeing the little tulips break before they even fully grew...
</div>
</div>

<div class="pot-area" id="potArea">
    <div class="tulip tulip-small t1"></div>
    <div class="tulip tulip-small t2"></div>

    <div class="pot" id="pot">
        <div class="crack" id="crack"></div>
    </div>
</div>

<div class="buttons">
    <button onclick="heal1()">Pick up the pieces ✨</button>
    <button onclick="heal2()">Give sunlight ☀️</button>
    <button onclick="heal3()">Water the tulips 💧</button>
</div>

</div>

<div class="final-scene" id="finalScene">
    <div class="big-tulips">🌷🌷</div>

    <h1>For Veda 🌷</h1>

    <div class="final-text">
<div style="font-size:1.4rem;margin-bottom:25px;color:#fff0f6;">
✨ A little garden made just for Veda ✨
</div>
        Some things don't need to fully bloom to still matter.
        <br><br>

        Those little tulips were special because you planted them with excitement and care.
        <br><br>

        <span class="highlight">You notice small beautiful things.</span>
        <br>
        <span class="highlight">That makes your presence feel comforting.</span>
        <br>
        <span class="highlight">And honestly, that's rare.</span>
        <br><br>

        And a broken tumbler cannot erase the happiness those tulips gave you.
        <br><br>

        So this is your little reminder:
        <br>
        <span class="highlight">Some beautiful moments stay beautiful even after they break 🌷</span>
    </div>
</div>

<script>
let step1=false;
let step2=false;
let step3=false;

function checkComplete(){
    if(step1 && step2 && step3){
        document.getElementById('finalScene').classList.add('show');
        createPetals();
        createSparkles();
    }
}

function heal1(){
    step1=true;
    document.getElementById('crack').style.opacity='0';
    checkComplete();
}

function heal2(){
    step2=true;
    document.body.style.background='linear-gradient(to bottom,#f9a8d4,#7dd3fc,#1e293b)';
    checkComplete();
}

function heal3(){
    document.querySelector('.typewriter').innerHTML='Maybe this little website cannot fix the tumbler... but maybe it can make you smile for a minute.';
    step3=true;

    const tulips=document.querySelectorAll('.tulip');

    tulips.forEach(t=>{
        t.style.transform='scale(1.2) translateY(-10px)';
        t.style.transition='1s';
    });

    checkComplete();
}

function createSparkles(){
    for(let i=0;i<60;i++){
        let sparkle=document.createElement('div');
        sparkle.classList.add('sparkle');
        sparkle.style.left=Math.random()*100+'vw';
        sparkle.style.top=Math.random()*100+'vh';
        sparkle.style.animationDuration=(Math.random()*3+2)+'s';
        document.body.appendChild(sparkle);
    }
}

function createPetals(){
    for(let i=0;i<40;i++){
        let petal=document.createElement('div');
        petal.classList.add('petals');
        petal.style.left=Math.random()*100+'vw';
        petal.style.animationDuration=(Math.random()*5+5)+'s';
        petal.style.opacity=Math.random();
        document.body.appendChild(petal);
    }
}

const canvas=document.getElementById('stars');
const ctx=canvas.getContext('2d');

canvas.width=window.innerWidth;
canvas.height=window.innerHeight;

let stars=[];

for(let i=0;i<120;i++){
    stars.push({
        x:Math.random()*canvas.width,
        y:Math.random()*canvas.height,
        r:Math.random()*2
    });
}

function drawStars(){
    ctx.clearRect(0,0,canvas.width,canvas.height);

    ctx.fillStyle='white';

    stars.forEach(star=>{
        ctx.beginPath();
        ctx.arc(star.x,star.y,star.r,0,Math.PI*2);
        ctx.fill();
    });

    requestAnimationFrame(drawStars);
}

drawStars();
</script>

</body>
</html>
