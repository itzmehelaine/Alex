<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Happy Birthday Alex!</title>
<meta name="viewport" content="width=device-width, initial-scale=1">
<style>
*,*::before,*::after{box-sizing:border-box;margin:0;padding:0}
:root{
  --pink:#ff69b4;--deep:#ff1493;--gold:#ffd700;--mint:#98fb98;--sky:#87ceeb;
  --txt:#fff;--bg:#fff;--shadow:0 8px 20px rgba(0,0,0,.2);
  --trans:all .5s cubic-bezier(.4,0,.2,1);
}
@media (prefers-color-scheme:dark){
  :root{--txt:#222;--bg:#111;}
}
html{font-family:'Comic Sans MS',cursive,system-ui;height:100%;
     cursor:url('data:image/svg+xml;utf8,<svg xmlns=%22http://www.w3.org/2000/svg%22 width=%2216%22 height=%2216%22 viewBox=%220 0 16 16%22><path fill=%22%23ff69b4%22 d=%22M8 1C5.3 1 3 3.3 3 6c0 4 5 9 5 9s5-5 5-9c0-2.7-2.3-5-5-5z%22/></svg>') 8 8,auto;}
body{min-height:100%;display:flex;align-items:center;justify-content:center;background:var(--bg);color:var(--txt);overflow:hidden;position:relative}

.slide{position:absolute;inset:0;display:flex;flex-direction:column;align-items:center;justify-content:center;
  opacity:0;pointer-events:none;transform:translateY(30px);transition:var(--trans);}
.slide.active{opacity:1;pointer-events:auto;transform:none;z-index:10}

.text-box{padding:clamp(1rem,5vw,2rem) clamp(2rem,8vw,4rem);
  background:var(--pink);color:var(--deep);font-weight:900;font-size:clamp(2rem,8vw,4rem);
  text-align:center;border-radius:1.5rem;box-shadow:var(--shadow);text-transform:uppercase;letter-spacing:.2ch;
  position:relative;overflow:hidden;}
.text-box::before{content:'';position:absolute;inset:0;background:radial-gradient(circle at 30% 30%,rgba(255,255,255,.3),transparent);pointer-events:none;}

.name span{display:inline-block;opacity:0;transform:translateY(20px);animation:bounceIn .6s forwards;}
@keyframes bounceIn{to{opacity:1;transform:none}}

.btn{margin-top:2rem;padding:.8rem 2rem;font-size:1.2rem;font-weight:bold;border:none;border-radius:3rem;
  background:var(--deep);color:#fff;cursor:pointer;box-shadow:var(--shadow);transition:var(--trans);
  position:relative;overflow:hidden;}
.btn:hover{transform:translateY(-4px) scale(1.05);box-shadow:0 12px 24px rgba(0,0,0,.25);}
.btn:active{transform:scale(.95);}
.btn::after{content:'Sparkles';position:absolute;inset:0;display:flex;align-items:center;justify-content:center;
  font-size:2rem;opacity:0;transform:scale(0);transition:transform .3s,opacity .3s;}
.btn:hover::after{opacity:.2;transform:scale(1);}

.cake{width:clamp(180px,45vw,260px);height:auto;margin:2rem 0;position:relative;}
.cake .sprinkle{position:absolute;width:6px;height:6px;border-radius:50%;background:var(--gold);box-shadow:0 0 4px #fff;}
.cake .cherry{fill:#ff0000;stroke:#cc0000;stroke-width:2;}
.cake .smiley{fill:#ff1493;font-size:12px;font-weight:bold;}

.flame{animation:flicker .7s infinite alternate;transform-origin:bottom;}
@keyframes flicker{from{opacity:1;transform:scale(1)}to{opacity:.6;transform:scale(.9)}}

.particle{position:fixed;pointer-events:none;opacity:.7;animation:float 6s infinite linear;font-size:1.5rem;}
@keyframes float{0%{transform:translateY(100vh) rotate(0deg)}100%{transform:translateY(-20px) rotate(360deg)}}

#confetti{position:fixed;inset:0;pointer-events:none;z-index:100}
#darkToggle{position:fixed;top:1rem;right:1rem;background:var(--deep);color:#fff;border:none;border-radius:50%;width:2.5rem;height:2.5rem;font-size:1.5rem;cursor:pointer;}
#cat{display:none;position:fixed;bottom:1rem;right:1rem;width:60px;animation:meow 2s infinite;}
@keyframes meow{0%,100%{transform:scale(1)}50%{transform:scale(1.1)}}

@media (prefers-reduced-motion:reduce){*,*::before,*::after{animation:none!important;transition:none!important}}
</style>
</head>

<body>
<button id="darkToggle" aria-label="Toggle dark mode">Moon</button>
<canvas id="confetti"></canvas>

<!-- Slide 1 -->
<section id="s1" class="slide active">
  <div class="text-box">
    <div class="name">H a p p y &nbsp; B i r t h d a y &nbsp; A L E X ! !</div>
  </div>
  <button class="btn" onclick="go(2)">Thanks! Red heart</button>
</section>

<!-- Slide 2 -->
<section id="s2" class="slide">
  <div class="text-box">Make a wish!</div>
  <svg class="cake" viewBox="0 0 200 180" onclick="easterEgg()">
    <rect x="50" y="100" width="100" height="50" rx="10" fill="#f4a460"/>
    <rect x="45" y="95" width="110" height="10" rx="5" fill="#deb887"/>
    <path d="M55 95Q65 85,75 95Q85 85,95 95Q105 85,115 95Q125 85,135 95Q145 85,145 95L145 100L55 100Z" fill="#fff0f5"/>
    <rect x="75" y="70" width="8" height="25" rx="2" fill="#87ceeb"/>
    <rect x="95" y="70" width="8" height="25" rx="2" fill="#ffb6c1"/>
    <rect x="115" y="70" width="8" height="25" rx="2" fill="#98fb98"/>
    <path class="flame" d="M77 65Q79 60,81 65Q79 62,77 65Z" fill="#ffd700"/>
    <path class="flame" d="M97 65Q99 60,101 65Q99 62,97 65Z" fill="#ffd700"/>
    <path class="flame" d="M117 65Q119 60,121 65Q119 62,117 65Z" fill="#ffd700"/>
    <circle class="sprinkle" cx="62" cy="88" r="3"/>
    <circle class="sprinkle" cx="80" cy="82" r="3"/>
    <circle class="sprinkle" cx="100" cy="86" r="3"/>
    <circle class="sprinkle" cx="120" cy="81" r="3"/>
    <circle class="sprinkle" cx="138" cy="89" r="3"/>
    <circle class="cherry" cx="70" cy="78" r="5"/>
    <circle class="cherry" cx="130" cy="78" r="5"/>
    <text class="smiley" x="97" y="92" text-anchor="middle">Smiling face</text>
  </svg>
  <button class="btn" id="blowBtn">Blow! Wind</button>
</section>

<!-- Slide 3 -->
<section id="s3" class="slide">
  <div class="text-box">Wish granted! Party popper</div>
  <svg class="cake" viewBox="0 0 200 180">
    <rect x="50" y="100" width="100" height="50" rx="10" fill="#f4a460"/>
    <rect x="45" y="95" width="110" height="10" rx="5" fill="#deb887"/>
    <path d="M55 95Q65 85,75 95Q85 85,95 95Q105 85,115 95Q125 85,135 95Q145 85,145 95L145 100L55 100Z" fill="#fff0f5"/>
    <rect x="75" y="70" width="8" height="25" rx="2" fill="#87ceeb"/>
    <rect x="95" y="70" width="8" height="25" rx="2" fill="#ffb6c1"/>
    <rect x="115" y="70" width="8" height="25" rx="2" fill="#98fb98"/>
    <circle class="sprinkle" cx="62" cy="88" r="3"/>
    <circle class="sprinkle" cx="80" cy="82" r="3"/>
    <circle class="sprinkle" cx="100" cy="86" r="3"/>
    <circle class="sprinkle" cx="120" cy="81" r="3"/>
    <circle class="sprinkle" cx="138" cy="89" r="3"/>
    <circle class="cherry" cx="70" cy="78" r="5"/>
    <circle class="cherry" cx="130" cy="78" r="5"/>
    <text class="smiley" x="97" y="92" text-anchor="middle">Smiling face</text>
  </svg>
</section>

<img id="cat" src="https://i.imgur.com/8fK8Y0E.png" alt="Cute cat">

<script>
const slides=['s1','s2','s3'];
function go(n){
  document.querySelector('.slide.active').classList.remove('active');
  setTimeout(()=>document.getElementById('s'+n).classList.add('active'),100);
  if(n===3) setTimeout(confettiBurst,600);
}

document.querySelectorAll('.name span').forEach((s,i)=>s.style.animationDelay=i*80+'ms');

let blowAudio=new Audio('data:audio/wav;base64,UklGRl9vT19XQVZFZm10IBAAAAABAAEAQB8AAEAfAAABAAgAZGF0YU'+'R4nOAA');
const blowBtn=document.getElementById('blowBtn');
let audioCtx, analyser, mic;
async function startMic(){
  try{
    const stream=await navigator.mediaDevices.getUserMedia({audio:true});
    audioCtx=new AudioContext();
    analyser=audioCtx.createAnalyser();
    mic=audioCtx.createMediaStreamSource(stream);
    mic.connect(analyser);
    analyser.fftSize=256;
    const data=new Uint8Array(analyser.frequencyBinCount);
    const detect=()=>{
      analyser.getByteFrequencyData(data);
      const vol=data.reduce((a,b)=>a+b)/data.length;
      if(vol>90){ extinguish(); }
      else requestAnimationFrame(detect);
    };
    detect();
  }catch(e){}
}
blowBtn.addEventListener('click',()=>{ extinguish(); });
function extinguish(){
  if(blowBtn.disabled) return;
  blowBtn.disabled=true;
  document.querySelectorAll('.flame').forEach(f=>f.remove());
  blowAudio.play();
  setTimeout(()=>go(3),800);
}
if('mediaDevices' in navigator) startMic();

const canvas=document.getElementById('confetti'),ctx=canvas.getContext('2d');
canvas.width=innerWidth; canvas.height=innerHeight;
addEventListener('resize',()=>{canvas.width=innerWidth;canvas.height=innerHeight;});
let particles=[];
function confettiBurst(){
  for(let i=0;i<180;i++){
    particles.push({
      x:Math.random()*canvas.width,
      y:Math.random()*canvas.height-100,
      size:Math.random()*8+4,
      speed:Math.random()*4+2,
      angle:Math.random()*360,
      spin:Math.random()*10-5,
      color:[['#ff69b4','#ff1493'],['#ffd700','#ffffff'],['#98fb98','#87ceeb'])[Math.floor(Math.random()*3)]
    });
  }
  animate();
}
function animate(){
  ctx.clearRect(0,0,canvas.width,canvas.height);
  particles.forEach((p,i)=>{
    p.y+=p.speed; p.angle+=p.spin; p.speed*=0.99;
    ctx.fillStyle=`hsl(${p.angle%360},100%,70%)`;
    ctx.beginPath(); ctx.arc(p.x,p.y,p.size,0,Math.PI*2); ctx.fill();
    if(p.y>canvas.height) particles.splice(i,1);
  });
  if(particles.length) requestAnimationFrame(animate);
}

setInterval(()=>{
  const p=document.createElement('div');
  p.className='particle';
  p.innerHTML=Math.random()>.5?'Red heart':'Star';
  p.style.fontSize=Math.random()*20+15+'px';
  p.style.color=['#ff69b4','#ffd700','#98fb98'][Math.floor(Math.random()*3)];
  p.style.left=Math.random()*100+'vw';
  p.style.animationDuration=4+Math.random()*4+'s';
  document.body.appendChild(p);
  setTimeout(()=>p.remove(),8000);
},600);

document.getElementById('darkToggle').addEventListener('click',()=>{
  document.body.classList.toggle('dark');
  const isDark=document.body.classList.contains('dark');
  document.getElementById('darkToggle').textContent=isDark?'Sun':'Moon';
});
if(matchMedia('(prefers-color-scheme:dark)').matches) document.body.classList.add('dark');

let cakeClicks=0;
function easterEgg(){
  cakeClicks++;
  if(cakeClicks===3){
    const cat=document.getElementById('cat');
    cat.style.display='block';
    setTimeout(()=>cat.style.display='none',5000);
    cakeClicks=0;
  }
}

document.querySelector('.name').innerHTML=[...('Happy Birthday ALEX!!')].map(c=>`<span>${c===' '?'&nbsp;':c}</span>`).join('');
</script>
</body>
</html>
