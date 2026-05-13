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
    overflow:hidden;
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
    height:100vh;
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
    width:170px;
    height:120px;
    background:#8b5e3c;
    clip-path:polygon(15% 0%,85% 0%,100% 100%,0% 100%);
    position:relative;
    margin:auto;
    transition:1s;
}

.crack{
    position:absolute;
    width:5px;
    height:100px;
    background:white;
    left:50%;
    top:10px;
    transform:rotate(20deg);
    opacity:1;
    transition:1s;
}

.tulip{
    position:absolute;
    width:25px;
    height:70px;
    background:linear-gradient(to top,#16a34a,#4ade80);
    bottom:100px;
}

.tulip::before{
    content:'';
    position:absolute;
    width:50px;
    height:50px;
    background:#ff4d88;
    border-radius:50% 50% 10% 10%;
    top:-35px;
    left:-12px;
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

<h1>For Veda 🌷</h1>

<div class="message show" id="msg">
<div class="typewriter">
I know your tulip pot breaking made you sad...
</div>
</div>

<div class="pot-area" id="potArea">
    <div class="tulip t1"></div>
    <div class="tulip t2"></div>

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

    <h1>Veda, You Make Things Beautiful</h1>

    <div class="final-text">
        Some things break, but that never removes the beauty they carried.
        <br><br>

        Just like your tulips, your care is what made them special.
        <br><br>

        <span class="highlight">Your smile feels calming.</span>
        <br>
        <span class="highlight">Your energy feels warm.</span>
        <br>
        <span class="highlight">And your presence makes ordinary moments feel softer.</span>
        <br><br>

        Even a broken flower pot could never take away the beauty you created around it.
        <br><br>

        So this is your little reminder:
        <br>
        <span class="highlight">Broken things can still bloom beautifully 🌷</span>
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
    step3=true;

    const tulips=document.querySelectorAll('.tulip');

    tulips.forEach(t=>{
        t.style.transform='scale(1.2) translateY(-10px)';
        t.style.transition='1s';
    });

    checkComplete();
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
