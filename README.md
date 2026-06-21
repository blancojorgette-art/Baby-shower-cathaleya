# Baby-shower-cathaleya<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Baby Shower de Cathaleya</title>

<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@500;700&family=Poppins:wght@300;400;500&display=swap" rel="stylesheet">

<style>
*{
margin:0;
padding:0;
box-sizing:border-box;
}

body{
font-family:'Poppins',sans-serif;
background:linear-gradient(180deg,#f8fff7,#eef7e8);
color:#333;
overflow-x:hidden;
}

.hero{
position:relative;
text-align:center;
padding:40px 20px;
}

.hero img{
width:100%;
max-width:450px;
border-radius:25px;
box-shadow:0 10px 30px rgba(0,0,0,.2);
border:6px solid #d4af37;
animation:flotar 4s ease-in-out infinite;
}

@keyframes flotar{
0%,100%{transform:translateY(0);}
50%{transform:translateY(-10px);}
}

.overlay{
margin-top:25px;
}

h1{
font-family:'Playfair Display',serif;
font-size:3rem;
color:#b68b00;
}

.sub{
font-size:1.2rem;
color:#4f6f3a;
margin-top:10px;
}

.card{
background:white;
width:90%;
max-width:650px;
margin:25px auto;
padding:25px;
border-radius:20px;
box-shadow:0 6px 20px rgba(0,0,0,.08);
}

.card h2{
color:#b68b00;
margin-bottom:15px;
}

.info{
font-size:1.1rem;
line-height:2;
}

.countdown{
display:flex;
justify-content:center;
gap:15px;
flex-wrap:wrap;
margin-top:20px;
}

.box{
background:#4f6f3a;
color:white;
padding:15px;
border-radius:15px;
min-width:80px;
}

.box span{
display:block;
font-size:2rem;
font-weight:bold;
}

.buttons{
display:flex;
flex-wrap:wrap;
justify-content:center;
gap:15px;
margin-top:25px;
}

.btn{
text-decoration:none;
padding:15px 25px;
border-radius:50px;
font-weight:600;
transition:.3s;
}

.whatsapp{
background:#25D366;
color:white;
}

.location{
background:#d4af37;
color:white;
}

.btn:hover{
transform:scale(1.05);
}

.message{
font-style:italic;
font-size:1.1rem;
color:#555;
text-align:center;
line-height:1.8;
}

footer{
text-align:center;
padding:30px;
color:#777;
}

.flor{
position:fixed;
font-size:24px;
animation:caer linear infinite;
opacity:.7;
}

@keyframes caer{
from{
transform:translateY(-100px);
}
to{
transform:translateY(110vh);
}
}
</style>
</head>

<body>

<div class="hero">
<img src="cathaleya.jpg" alt="Baby Shower Cathaleya">

<div class="overlay">
<h1>Cathaleya</h1>
<p class="sub">Baby Shower</p>
</div>
</div>

<div class="card">
<h2>✨ Estás Invitado ✨</h2>

<p class="message">
Con mucha alegría te invitamos a celebrar la próxima llegada de nuestra princesa.
Tu presencia hará este día aún más especial.
</p>

<div class="info">
📅 <strong>Sábado 11 de julio de 2026</strong><br>
⏰ <strong>11:00 a. m.</strong><br>
📍 <strong>Casa de mis abuelos, Santa Rita, Los Próceres, Calle Las Mercedes</strong>
</div>
</div>

<div class="card">
<h2>⏳ Cuenta Regresiva</h2>

<div class="countdown">
<div class="box">
<span id="days">0</span>
Días
</div>

<div class="box">
<span id="hours">0</span>
Horas
</div>

<div class="box">
<span id="minutes">0</span>
Minutos
</div>

<div class="box">
<span id="seconds">0</span>
Segundos
</div>
</div>
</div>

<div class="buttons">
<a class="btn whatsapp"
href="https://wa.me/584127907686?text=Hola,%20confirmo%20mi%20asistencia%20al%20Baby%20Shower%20de%20Cathaleya"
target="_blank">
Confirmar Asistencia
</a>

<a class="btn location"
href="https://maps.google.com/?q=Santa+Rita+Los+Proceres+Calle+Las+Mercedes"
target="_blank">
Ver Ubicación
</a>
</div>

<footer>
💚 Te esperamos para compartir este hermoso momento 💚
</footer>

<script>

const evento = new Date("July 11, 2026 11:00:00").getTime();

setInterval(() => {

const ahora = new Date().getTime();
const diferencia = evento - ahora;

const dias = Math.floor(diferencia / (1000*60*60*24));
const horas = Math.floor((diferencia % (1000*60*60*24)) / (1000*60*60));
const minutos = Math.floor((diferencia % (1000*60*60)) / (1000*60));
const segundos = Math.floor((diferencia % (1000*60)) / 1000);

document.getElementById("days").innerHTML = dias;
document.getElementById("hours").innerHTML = horas;
document.getElementById("minutes").innerHTML = minutos;
document.getElementById("seconds").innerHTML = segundos;

},1000);

for(let i=0;i<20;i++){

const flor=document.createElement("div");
flor.className="flor";
flor.innerHTML=Math.random()>0.5?"🌸":"🦋";

flor.style.left=Math.random()*100+"vw";
flor.style.animationDuration=(5+Math.random()*10)+"s";
flor.style.animationDelay=Math.random()*5+"s";

document.body.appendChild(flor);
}

</script>

</body>
</html>
