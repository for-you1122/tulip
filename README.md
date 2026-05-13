<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>For Veda 🌷</title>
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600&family=Playfair+Display:wght@600&display=swap" rel="stylesheet">

<style>
*{
margin:0;
padding:0;
box-sizing:border-box;
}

html{
scroll-behavior:smooth;
}

body{
font-family:'Inter',sans-serif;
background:#0f172a;
color:white;
overflow-x:hidden;
}

.section{
min-height:100vh;
display:flex;
justify-content:center;
align-items:center;
padding:40px 20px;
position:relative;
}

.bg{
position:fixed;
inset:0;
background:radial-gradient(circle at top,#1e293b,#0f172a 60%);
z-index:-3;
}

.blur1,.blur2{
position:fixed;
border-radius:50%;
filter:blur(90px);
z-index:-2;
opacity:0.5;
}

.blur1{
width:300px;
height:300px;
background:#ff7aa2;
top:-50px;
left:-50px;
animation:move1 10s infinite alternate;
}

.blur2{
width:350px;
height:350px;
background:#7dd3fc;
bottom:-100px;
right:-80px;
animation:move2 12s infinite alternate;
}

@keyframes move1{
from{transform:translateY(0px)}
to{transform:translateY(60px)}
}

@keyframes move2{
from{transform:translateX(0px)}
to{transform:translateX(-60px)}
}

.card{
width:100%;
max-width:900px;
backdrop-filter:blur(18px);
background:rgba(255,255,255,0.06);
border:1px solid rgba(255,255,255,0.1);
border-radius:35px;
padding:60px 35px;
text-align:center;
box-shadow:0 20px 50px rgba(0,0,0,0.35);
}

h1{
font-family:'Playfair Display',serif;
font-size:4rem;
margin-bottom:20px;
background:linear-gradient(to right,#ffd1dc,#ffffff);
-webkit-background-clip:text;
-webkit-text-fill-color:transparent;
}

.line{
font-size:1.15rem;
line-height:2;
color:#e2e8f0;
opacity:0;
transform:translateY(30px);
animation:fadeUp 1s forwards;
}

.line:nth-child(2){animation-delay:1s}
.line:nth-child(3){animation-delay:2.5s}
.line:nth-child(4){animation-delay:4s}
.line:nth-child(5){animation-delay:5.5s}

@keyframes fadeUp{
to{
opacity:1;
transform:translateY(0);
}
}

.glass{
width:140px;
height:220px;
margin:50px auto;
background:rgba(255,255,255,0.08);
border:2px solid rgba(255,255,255,0.18);
border-radius:25px 25px 40px 40px;
position:relative;
overflow:hidden;
box-shadow:inset 0 0 30px rgba(255,255,255,0.08);
}

.glass::before{
content:'';
position:absolute;
inset:0;
background:linear-gradient(to right,transparent,rgba(255,255,255,0.15),transparent);
transform:translateX(-100%);
animation:shine 4s infinite;
}

@keyframes shine{
100%{transform:translateX(200%)}
}

.crack{
position:absolute;
width:3px;
height:120px;
background:#f8fafc;
left:60px;
top:50px;
transform:rotate(20deg);
opacity:0.7;
}

.soil{
position:absolute;
width:100%;
height:65px;
background:#3f2b1d;
bottom:0;
}

.tulip{
position:absolute;
width:4px;
height:65px;
background:#22c55e;
bottom:55px;
}

.tulip::before{
content:'';
position:absolute;
width:20px;
height:20px;
background:#ff7aa2;
border-radius:50% 50% 40% 40%;
top:-10px;
left:-8px;
box-shadow:0 0 15px rgba(255,122,162,0.5);
}

.t1{left:45px}
.t2{right:45px}

.scroll{
margin-top:40px;
font-size:0.9rem;
letter-spacing:3px;
color:#cbd5e1;
animation:bounce 2s infinite;
}

@keyframes bounce{
50%{transform:translateY(8px)}
}

.garden{
display:flex;
justify-content:center;
align-items:center;
flex-direction:column;
text-align:center;
width:100%;
}

.garden-title{
font-size:4rem;
font-family:'Playfair Display',serif;
margin-bottom:25px;
}

.quote{
max-width:700px;
font-size:1.2rem;
line-height:2;
color:#f1f5f9;
opacity:0;
transform:translateY(40px);
transition:1s;
}

.quote.show{
opacity:1;
transform:translateY(0);
}

.flowers{
margin-top:50px;
font-size:5rem;
letter-spacing:20px;
animation:float 4s ease-in-out infinite;
}

@keyframes float{
50%{transform:translateY(-15px)}
}

.petals span{
position:absolute;
font-size:20px;
animation:fall linear infinite;
opacity:0.8;
}

@keyframes fall{
from{
transform:translateY(-100px) rotate(0deg);
}

to{
transform:translateY(110vh) rotate(360deg);
}
}

.highlight{
color:#ffd1dc;
font-weight:600;
}

@media(max-width:768px){
h1,.garden-title{
font-size:2.6rem;
}

.card{
padding:45px 20px;
}

.line,.quote{
font-size:1rem;
}
}
</style>
</head>
<body>

<div class="bg"></div>
<div class="blur1"></div>
<div class="blur2"></div>

<div class="petals" id="petals"></div>

<section class="section">
<div class="card">

<h1>For Veda 🌷</h1>

<p class="line">
I know it felt bad seeing the little tulips break before they even fully grew.
</p>

<div class="glass">
<div class="crack"></div>
<div class="soil"></div>
<div class="tulip t1"></div>
<div class="tulip t2"></div>
</div>

<p class="line">
But maybe beautiful things are not only beautiful when they survive forever.
</p>

<p class="line">
Sometimes they become special simply because someone cared for them deeply.
</p>

<p class="line">
And honestly... the way you notice small beautiful things says a lot about you.
</p>

<div class="scroll">
SCROLL ↓
</div>

</div>
</section>

<section class="section">
<div class="garden">

<h2 class="garden-title">A Small Garden For Veda</h2>

<div class="flowers">🌷 ✨ 🌷</div>

<p class="quote" id="quote">
Those tulips may not have fully bloomed yet,
<br><br>
but the excitement with which you planted them still mattered.
<br><br>
<span class="highlight">You have a calming kind of presence.</span>
<br>
<span class="highlight">The type that notices little things others ignore.</span>
<br><br>
And that makes ordinary moments feel softer.
<br><br>
So maybe this little website cannot fix the broken tumbler...
<br>
but maybe it can remind you that some beautiful moments stay beautiful even after they break 🌷
</p>

</div>
</section>

<script>
const quote=document.getElementById('quote');

window.addEventListener('scroll',()=>{
const top=quote.getBoundingClientRect().top;

if(top<window.innerHeight-100){
quote.classList.add('show');
}
})

const petals=document.getElementById('petals');

for(let i=0;i<35;i++){
let span=document.createElement('span');
span.innerHTML='🌸';
span.style.left=Math.random()*100+'vw';
span.style.animationDuration=(Math.random()*5+5)+'s';
span.style.animationDelay=Math.random()*5+'s';
petals.appendChild(span);
}
</script>

</body>
</html>
