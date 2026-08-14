<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Fe y Alegría 21 | Plataforma Educativa</title>

<style>

*{
box-sizing:border-box;
}

body{
margin:0;
font-family:Arial,sans-serif;
background:#eef5ff;
color:#222;
}

header{
background:linear-gradient(135deg,#1565c0,#0d47a1);
color:white;
text-align:center;
padding:30px 15px;
}

header h1{
font-size:38px;
margin:0 0 8px;
}

nav{
background:#082f70;
padding:10px;
display:flex;
flex-wrap:wrap;
justify-content:center;
gap:5px;
}

nav button{
background:transparent;
color:white;
border:0;
padding:12px;
cursor:pointer;
border-radius:8px;
}

nav button:hover{
background:#1565c0;
}

main{
max-width:1100px;
margin:auto;
padding:20px;
}

.pagina{
display:none;
background:white;
padding:25px;
border-radius:18px;
margin-bottom:20px;
box-shadow:0 4px 15px #0002;
}

.activa{
display:block;
}

h2{
color:#1565c0;
}

button{
background:#43a047;
color:white;
border:0;
padding:11px 16px;
margin:5px;
border-radius:8px;
cursor:pointer;
font-weight:bold;
}

button:hover{
transform:scale(1.03);
}

.rojo{
background:#d32f2f;
}

.azul{
background:#1565c0;
}

input,select{
padding:11px;
border:1px solid #bbb;
border-radius:8px;
margin:5px;
font-size:15px;
}

.tarjetas{
display:grid;
grid-template-columns:repeat(2,1fr);
gap:15px;
}

.tarjeta{
padding:22px;
background:#f4f8ff;
border-radius:14px;
text-align:center;
}

.icono{
font-size:35px;
}

.tarea,.material,.clase{
padding:18px;
margin:12px 0;
border-radius:12px;
background:#f8f8f8;
border-left:6px solid #1565c0;
}

.proxima{
border-left-color:#ff9800;
background:#fff8e1;
}

.atrasada{
border-left-color:#d32f2f;
background:#ffebee;
}

.completada{
border-left-color:#43a047;
background:#e8f5e9;
}

.notificacion{
padding:15px;
margin:10px 0;
border-radius:10px;
background:#fff3cd;
border-left:5px solid #ff9800;
}

.alerta{
padding:15px;
margin:10px 0;
border-radius:10px;
background:#ffebee;
border-left:5px solid #d32f2f;
}

.exito{
padding:15px;
margin:10px 0;
border-radius:10px;
background:#e8f5e9;
border-left:5px solid #43a047;
}

.niveles{
text-align:center;
}

.juego{
background:#f5f8ff;
padding:25px;
border-radius:15px;
text-align:center;
}

.opciones{
display:grid;
grid-template-columns:repeat(2,1fr);
gap:10px;
max-width:650px;
margin:auto;
}

.opciones button{
background:#1976d2;
font-size:17px;
}

.opciones button:hover{
background:#0d47a1;
}

.seleccionado{
background:#43a047!important;
}

#pregunta{
font-size:22px;
font-weight:bold;
margin:25px 0;
}

.stats{
display:grid;
grid-template-columns:repeat(4,1fr);
gap:12px;
}

.stat{
background:#f4f8ff;
padding:20px;
border-radius:12px;
text-align:center;
}

.stat strong{
font-size:27px;
display:block;
color:#1565c0;
}

.barra{
height:28px;
background:#ddd;
border-radius:20px;
overflow:hidden;
}

#barra{
height:100%;
width:0%;
background:#43a047;
transition:.5s;
}

.habito{
background:#f5f5f5;
padding:18px;
margin:12px 0;
border-radius:12px;
}

#temporizador{
font-size:60px;
font-weight:bold;
text-align:center;
color:#1565c0;
margin:25px;
}

footer{
background:#082f70;
color:white;
text-align:center;
padding:25px;
}

@media(max-width:700px){

header h1{
font-size:28px;
}

nav{
flex-direction:column;
}

nav button{
width:100%;
}

.tarjetas{
grid-template-columns:1fr;
}

.stats{
grid-template-columns:repeat(2,1fr);
}

.opciones{
grid-template-columns:1fr;
}

.pagina{
padding:18px;
}

}

</style>
</head>

<body>

<header>

<h1>🎓 Fe y Alegría 21</h1>

<p>
Plataforma Educativa Interactiva
</p>

</header>


<nav>

<button onclick="mostrar('inicio')">🏠 Inicio</button>

<button onclick="mostrar('personal')">👤 Personalizar</button>

<button onclick="mostrar('horario')">📅 Horario</button>

<button onclick="mostrar('entregas')">📝 Entregas</button>

<button onclick="mostrar('juegos')">🎮 Juegos</button>

<button onclick="mostrar('materiales')">📚 Materiales</button>

<button onclick="mostrar('habitos')">🧠 Hábitos</button>

<button onclick="mostrar('estudio')">⏱️ Estudiar</button>

<button onclick="mostrar('progreso')">🏆 Progreso</button>

</nav>


<main>


<!-- INICIO -->

<section id="inicio" class="pagina activa">

<h2>👋 Bienvenido</h2>

<div id="bienvenida"></div>

<div id="alertas"></div>

<div class="tarjetas">

<div class="tarjeta">

<div class="icono">👤</div>

<h3>Personaliza</h3>

<p>
Configura tu perfil y tus datos.
</p>

</div>

<div class="tarjeta">

<div class="icono">📅</div>

<h3>Organiza</h3>

<p>
Crea tu propio horario.
</p>

</div>

<div class="tarjeta">

<div class="icono">📝</div>

<h3>Controla tus tareas</h3>

<p>
Agrega fechas y entregas.
</p>

</div>

<div class="tarjeta">

<div class="icono">🎮</div>

<h3>Aprende jugando</h3>

<p>
Juega y gana puntos.
</p>

</div>

</div>

</section>


<!-- PERSONALIZAR -->

<section id="personal" class="pagina">

<h2>👤 Mi espacio personal</h2>

<h3>Datos del estudiante</h3>

<input id="nombre"
placeholder="Nombre">

<select id="nivel">

<option>Primaria</option>

<option>Secundaria</option>

</select>

<input id="grado"
placeholder="Grado y sección">


<br>

<button onclick="guardarPerfil()">
💾 Guardar perfil
</button>

<div id="perfilMensaje"></div>


<hr>


<h2>📅 Crear mi horario</h2>

<select id="diaClase">

<option>Lunes</option>
<option>Martes</option>
<option>Miércoles</option>
<option>Jueves</option>
<option>Viernes</option>

</select>

<input id="horaClase" type="time">

<input id="cursoClase"
placeholder="Curso">

<input id="profesor"
placeholder="Profesor (opcional)">

<button onclick="agregarClase()">
➕ Agregar clase
</button>

<div id="misClases"></div>


<hr>


<h2>📝 Crear mis tareas</h2>

<input id="tareaNombre"
placeholder="Ejemplo: Tarea de Matemática">

<select id="diaTarea">

<option>Lunes</option>
<option>Martes</option>
<option>Miércoles</option>
<option>Jueves</option>
<option>Viernes</option>

</select>

<br>

<label>Fecha:</label>

<input id="fechaTarea" type="date">

<label>Hora:</label>

<input id="horaTarea" type="time">


<select id="prioridad">

<option>🟢 Normal</option>

<option>🟡 Importante</option>

<option>🔴 Urgente</option>

</select>

<br>

<button onclick="agregarTarea()">
➕ Agregar tarea
</button>

<div id="misTareas"></div>

</section>


<!-- HORARIO -->

<section id="horario" class="pagina">

<h2>📅 Mi horario</h2>

<p>
Aquí aparecerá el horario que hayas creado.
</p>

<div id="horarioCompleto"></div>

</section>


<!-- ENTREGAS -->

<section id="entregas" class="pagina">

<h2>📝 Mis entregas</h2>

<div id="avisosTareas"></div>

<div id="entregasLista"></div>

</section>


<!-- JUEGOS -->

<section id="juegos" class="pagina">

<h2>🎮 Juegos educativos</h2>

<div class="juego">

<h3>Selecciona dificultad</h3>

<div class="niveles">

<button onclick="nivelJuego('basico')">
🟢 Básico
</button>

<button onclick="nivelJuego('medio')">
🟡 Medio
</button>

<button onclick="nivelJuego('dificil')">
🔴 Difícil
</button>

</div>

<p>
⭐ Puntos: <strong id="puntosJuego">0</strong>
</p>

<p>
Pregunta <strong id="numero">0</strong>
</p>

<div id="pregunta">
Selecciona un nivel para comenzar.
</div>

<div id="opciones" class="opciones"></div>

<p id="respuesta"></p>

<button onclick="siguiente()">
➡️ Siguiente
</button>

</div>

</section>


<!-- MATERIALES -->

<section id="materiales" class="pagina">

<h2>📚 Biblioteca educativa</h2>

<button onclick="filtrar('todos')">
Todos
</button>

<button onclick="filtrar('Matemática')">
➗ Matemática
</button>

<button onclick="filtrar('Comunicación')">
📖 Comunicación
</button>

<button onclick="filtrar('Ciencia')">
🔬 Ciencia
</button>

<button onclick="filtrar('Sociales')">
🌎 Sociales
</button>

<button onclick="filtrar('EPT')">
💻 EPT
</button>


<div class="material" data-curso="Matemática">

<h3>➗ Matemática</h3>

<p>
Ejercicios, operaciones y problemas.
</p>

<button onclick="estudiarMaterial('Matemática')">
📖 Estudiar
</button>

</div>


<div class="material" data-curso="Comunicación">

<h3>📖 Comunicación</h3>

<p>
Lectura, comprensión y escritura.
</p>

<button onclick="estudiarMaterial('Comunicación')">
📖 Estudiar
</button>

</div>


<div class="material" data-curso="Ciencia">

<h3>🔬 Ciencia y Tecnología</h3>

<p>
Ciencia, ambiente y tecnología.
</p>

<button onclick="estudiarMaterial('Ciencia')">
📖 Estudiar
</button>

</div>


<div class="material" data-curso="Sociales">

<h3>🌎 Ciencias Sociales</h3>

<p>
Historia, geografía y sociedad.
</p>

<button onclick="estudiarMaterial('Sociales')">
📖 Estudiar
</button>

</div>


<div class="material" data-curso="EPT">

<h3>💻 Educación para el Trabajo</h3>

<p>
Tecnología, proyectos y emprendimiento.
</p>

<button onclick="estudiarMaterial('EPT')">
📖 Estudiar
</button>

</div>

<div id="materialMensaje"></div>

</section>


<!-- HABITOS -->

<section id="habitos" class="pagina">

<h2>🧠 Mis hábitos</h2>

<div class="habito">

<p>
¿Terminaste tus tareas?
</p>

<button onclick="habito(true)">
Sí 👍
</button>

<button onclick="habito(false)">
No 👎
</button>

</div>


<div class="habito">

<p>
¿Estudiaste hoy?
</p>

<button onclick="habito(true)">
Sí 👍
</button>

<button onclick="habito(false)">
No 👎
</button>

</div>


<div class="habito">

<p>
¿Organizaste tu tiempo?
</p>

<button onclick="habito(true)">
Sí 👍
</button>

<button onclick="habito(false)">
No 👎
</button>

</div>


<div class="habito">

<p>
¿Preparaste tus materiales?
</p>

<button onclick="habito(true)">
Sí 👍
</button>

<button onclick="habito(false)">
No 👎
</button>

</div>


<div id="habitoResultado"></div>

</section>


<!-- ESTUDIO -->

<section id="estudio" class="pagina">

<h2>⏱️ Temporizador de estudio</h2>

<div id="temporizador">
30:00
</div>

<div style="text-align:center">

<button onclick="iniciar()">
▶️ Iniciar
</button>

<button onclick="pausar()">
⏸️ Pausar
</button>

<button onclick="reiniciar()">
🔄 Reiniciar
</button>

</div>

<p id="tiempoMensaje"></p>

</section>


<!-- PROGRESO -->

<section id="progreso" class="pagina">

<h2>🏆 Mi progreso</h2>

<div class="stats">

<div class="stat">

<strong id="puntosTotal">
0
</strong>

⭐ Puntos

</div>


<div class="stat">

<strong id="juegosTotal">
0
</strong>

🎮 Juegos

</div>


<div class="stat">

<strong id="tareasTotal">
0
</strong>

📝 Tareas

</div>


<div class="stat">

<strong id="nivelUsuario">
Principiante
</strong>

🏅 Nivel

</div>

</div>


<h3>📊 Barra de progreso</h3>

<div class="barra">

<div id="barra"></div>

</div>


<p id="progresoMensaje"></p>

</section>


</main>


<footer>

<p>
🎓 Fe y Alegría 21
</p>

<p>
Plataforma educativa interactiva
</p>

</footer>


<script>


/* ================= DATOS GUARDADOS ================= */

let perfil=
JSON.parse(localStorage.getItem("FA21_perfil"))||{
nombre:"",
nivel:"Primaria",
grado:""
};


let clases=
JSON.parse(localStorage.getItem("FA21_clases"))||[];


let tareas=
JSON.parse(localStorage.getItem("FA21_tareas"))||[];


let puntos=
Number(localStorage.getItem("FA21_puntos"))||0;


let juegos=
Number(localStorage.getItem("FA21_juegos"))||0;


let nivelActual="";


let preguntaActual=0;


let puntosJuego=0;


/* ================= NAVEGACIÓN ================= */

function mostrar(id){

document.querySelectorAll(".pagina")
.forEach(x=>x.classList.remove("activa"));

document.getElementById(id)
.classList.add("activa");

if(id==="inicio"){

actualizarInicio();

}

if(id==="horario"){

mostrarHorario();

}

if(id==="entregas"){

mostrarEntregas();

}

if(id==="personal"){

cargarPerfil();

mostrarClases();

mostrarTareas();

}

if(id==="progreso"){

actualizarProgreso();

}

}


/* ================= PERFIL ================= */

function guardarPerfil(){

perfil.nombre=
document.getElementById("nombre").value;

perfil.nivel=
document.getElementById("nivel").value;

perfil.grado=
document.getElementById("grado").value;


localStorage.setItem(
"FA21_perfil",
JSON.stringify(perfil)
);


document.getElementById("perfilMensaje")
.innerHTML=
'<div class="exito">✅ Perfil guardado.</div>';

actualizarInicio();

}


function cargarPerfil(){

document.getElementById("nombre").value=
perfil.nombre;

document.getElementById("nivel").value=
perfil.nivel;

document.getElementById("grado").value=
perfil.grado;

}


/* ================= CLASES ================= */

function agregarClase(){

let dia=
document.getElementById("diaClase").value;

let hora=
document.getElementById("horaClase").value;

let curso=
document.getElementById("cursoClase").value;

let profesor=
document.getElementById("profesor").value;


if(!hora||!curso){

alert("⚠️ Escribe la hora y el curso.");

return;

}


clases.push({

id:Date.now(),

dia:dia,

hora:hora,

curso:curso,

profesor:profesor

});


guardarClases();

document.getElementById("cursoClase").value="";

document.getElementById("profesor").value="";

mostrarClases();

mostrarHorario();

}


function guardarClases(){

localStorage.setItem(
"FA21_clases",
JSON.stringify(clases)
);

}


function mostrarClases(){

let contenedor=
document.getElementById("misClases");

if(!contenedor)return;


if(clases.length===0){

contenedor.innerHTML=
"<p>📅 No tienes clases personalizadas.</p>";

return;

}


let html="";


clases.forEach(c=>{

html+=`

<div class="clase">

<strong>📅 ${c.dia}</strong>

<br>

⏰ ${c.hora}

<br>

📚 ${c.curso}

${c.profesor?
"<br>👨‍🏫 "+c.profesor:""}

<br>

<button class="rojo"
onclick="eliminarClase(${c.id})">

🗑️ Eliminar

</button>

</div>

`;

});


contenedor.innerHTML=html;

}


function mostrarHorario(){

let contenedor=
document.getElementById("horarioCompleto");

if(!contenedor)return;


if(clases.length===0){

contenedor.innerHTML=
"<p>📅 Primero agrega clases desde Personalizar.</p>";

return;

}


let dias=[
"Lunes",
"Martes",
"Miércoles",
"Jueves",
"Viernes"
];


let html="";


dias.forEach(dia=>{

let lista=
clases
.filter(c=>c.dia===dia)
.sort((a,b)=>a.hora.localeCompare(b.hora));


if(lista.length){

html+=`<h3>📅 ${dia}</h3>`;

lista.forEach(c=>{

html+=`

<div class="clase">

⏰ <strong>${c.hora}</strong>

📚 ${c.curso}

${c.profesor?
" | 👨‍🏫 "+c.profesor:""}

</div>

`;

});

}

});


contenedor.innerHTML=html;

}


function eliminarClase(id){

clases=
clases.filter(c=>c.id!==id);

guardarClases();

mostrarClases();

mostrarHorario();

}


/* ================= TAREAS ================= */

function agregarTarea(){

let nombre=
document.getElementById("tareaNombre").value;

let dia=
document.getElementById("diaTarea").value;

let fecha=
document.getElementById("fechaTarea").value;

let hora=
document.getElementById("horaTarea").value;

let prioridad=
document.getElementById("prioridad").value;


if(!nombre||!fecha){

alert("⚠️ Escribe la tarea y la fecha.");

return;

}


tareas.push({

id:Date.now(),

nombre:nombre,

dia:dia,

fecha:fecha,

hora:hora,

prioridad:prioridad,

completada:false

});


guardarTareas();

document.getElementById("tareaNombre").value="";

mostrarTareas();

mostrarEntregas();

}


function guardarTareas(){

localStorage.setItem(
"FA21_tareas",
JSON.stringify(tareas)
);

}


function mostrarTareas(){

let contenedor=
document.getElementById("misTareas");

if(!contenedor)return;


let html="";


if(tareas.length===0){

contenedor.innerHTML=
"<p>📝 No tienes tareas.</p>";

return;

}


tareas.forEach(t=>{

let estado="🟢 Pendiente";

let clase="";


if(t.completada){

estado="✅ Completada";

clase="completada";

}

else{

let fecha=new Date(
t.fecha+"T"+(t.hora||"23:59")
);

if(fecha<new Date()){

estado="🔴 ATRASADA";

clase="atrasada";

}

else{

let dias=
Math.ceil(
(fecha-new Date())/
86400000
);

if(dias<=2){

estado="🟡 PRÓXIMA";

clase="proxima";

}

}

}


html+=`

<div class="tarea ${clase}">

<h3>${t.nombre}</h3>

<p>📅 ${t.dia}</p>

<p>📆 ${t.fecha}</p>

${t.hora?
"<p>⏰ "+t.hora+"</p>":""}

<p>${t.prioridad}</p>

<p><strong>${estado}</strong></p>

${
!t.completada?

`<button onclick="completarTarea(${t.id})">
✅ Terminé
</button>`

:""
}

<button class="rojo"
onclick="eliminarTarea(${t.id})">

🗑️ Eliminar

</button>

</div>

`;

});


contenedor.innerHTML=html;

}


function mostrarEntregas(){

let contenedor=
document.getElementById("entregasLista");

let avisos=
document.getElementById("avisosTareas");


if(!contenedor)return;


let html="";

let alertas="";


tareas.forEach(t=>{

let fecha=
new Date(
t.fecha+"T"+(t.hora||"23:59")
);

let estado="🟢 Pendiente";

let clase="";


if(t.completada){

estado="✅ Completada";

clase="completada";

}

else if(fecha<new Date()){

estado="🔴 ATRASADA";

clase="atrasada";

alertas+=
'<div class="alerta">🔴 La tarea "'+
t.nombre+
'" está atrasada.</div>';

}

else{

let dias=
Math.ceil(
(fecha-new Date())/
86400000
);

if(dias<=2){

estado="🟡 PRÓXIMA";

clase="proxima";

alertas+=
'<div class="notificacion">🔔 La tarea "'+
t.nombre+
'" está próxima.</div>';

}

}


html+=`

<div class="tarea ${clase}">

<h3>${t.nombre}</h3>

<p>📅 ${t.dia}</p>

<p>📆 Entrega: ${t.fecha}</p>

${t.hora?
"<p>⏰ "+t.hora+"</p>":""}

<p>${t.prioridad}</p>

<strong>${estado}</strong>

</div>

`;

});


contenedor.innerHTML=
html||"<p>No tienes tareas.</p>";

avisos.innerHTML=alertas;

}


function completarTarea(id){

let tarea=
tareas.find(t=>t.id===id);

if(!tarea||tarea.completada)return;

tarea.completada=true;

guardarTareas();

sumarPuntos(10);

mostrarTareas();

mostrarEntregas();

}


function eliminarTarea(id){

tareas=
tareas.filter(t=>t.id!==id);

guardarTareas();

mostrarTareas();

mostrarEntregas();

}


/* ================= JUEGO ================= */

let preguntas={

basico:[

["¿Cuánto es 5 + 7?",["10","12","14","15"],1],

["¿Capital del Perú?",["Lima","Cusco","Piura","Tacna"],0],

["¿Cuántos días tiene una semana?",["5","6","7","8"],2],

["¿Cuánto es 8 × 4?",["24","28","32","36"],2],

["¿En qué planeta vivimos?",["Marte","Tierra","Venus","Júpiter"],1],

["¿Cuánto es 20 - 9?",["9","10","11","12"],2]

],

medio:[

["¿Cuánto es 15 × 6?",["80","90","100","120"],1],

["¿Cuánto es 144 ÷ 12?",["10","11","12","14"],2],

["¿Qué órgano bombea la sangre?",["Pulmón","Corazón","Riñón","Cerebro"],1],

["¿Cuál es un sinónimo de feliz?",["Triste","Contento","Enojado","Cansado"],1],

["¿Qué gas necesitamos para respirar?",["Oxígeno","Helio","Neón","Hidrógeno"],0],

["¿En qué continente está Perú?",["Asia","Europa","América","África"],2]

],

dificil:[

["¿Cuánto es 25²?",["525","625","725","825"],1],

["Si x + 15 = 32, ¿cuánto vale x?",["15","17","18","20"],1],

["¿Cuál es la raíz cuadrada de 144?",["10","11","12","14"],2],

["¿Qué proceso permite a las plantas fabricar alimento?",["Digestión","Fotosíntesis","Evaporación","Fermentación"],1],

["¿Cuál es la tercera ley de Newton?",["Inercia","Acción y reacción","Gravedad","Energía"],1],

["¿Cuánto es 18²?",["324","328","342","361"],0]

]

};


function nivelJuego(nivel){

nivelActual=nivel;

preguntaActual=0;

puntosJuego=0;

document.getElementById("puntosJuego")
.textContent=0;

cargarPregunta();

}


function cargarPregunta(){

let lista=
preguntas[nivelActual];

let q=
lista[preguntaActual%lista.length];

document.getElementById("numero")
.textContent=preguntaActual+1;

document.getElementById("pregunta")
.textContent=q[0];

document.getElementById("respuesta")
.textContent="";

let contenedor=
document.getElementById("opciones");

contenedor.innerHTML="";


q[1].forEach((opcion,i)=>{

let b=
document.createElement("button");

b.textContent=opcion;

b.onclick=
()=>responderJuego(i,q[2]);

contenedor.appendChild(b);

});

}


function responderJuego(respuesta,correcta){

let puntosGanados=
nivelActual==="basico"
?10
:nivelActual==="medio"
?15
:25;


if(respuesta===correcta){

puntosJuego+=puntosGanados;

sumarPuntos(puntosGanados);

document.getElementById("respuesta")
.textContent=
"🎉 ¡Correcto! +"+
puntosGanados+
" puntos.";

juegos++;

localStorage.setItem(
"FA21_juegos",
juegos
);

}

else{

document.getElementById("respuesta")
.textContent=
"❌ Incorrecto. ¡Sigue intentando!";

}


document.getElementById("puntosJuego")
.textContent=puntosJuego;

}


function siguiente(){

if(!nivelActual){

alert("⚠️ Primero selecciona un nivel.");

return;

}

preguntaActual++;

cargarPregunta();

}


/* ================= MATERIALES ================= */

function filtrar(curso){

document
.querySelectorAll(".material")
.forEach(m=>{

if(
curso==="todos"||
m.dataset.curso===curso
){

m.style.display="block";

}

else{

m.style.display="none";

}

});

}


function estudiarMaterial(nombre){

document.getElementById("materialMensaje")
.innerHTML=
'<div class="exito">📚 Estás estudiando '+nombre+
'. ¡Buen trabajo!</div>';

sumarPuntos(5);

}


/* ================= HÁBITOS ================= */

let respuestas=0;


function habito(valor){

if(valor){

respuestas++;

document.getElementById("habitoResultado")
.innerHTML=
'<div class="exito">🟢 ¡Muy bien! Sigue así.</div>';

sumarPuntos(5);

}

else{

document.getElementById("habitoResultado")
.innerHTML=
'<div class="notificacion">🟡 Puedes mejorar poco a poco.</div>';

}

}


/* ================= TEMPORIZADOR ================= */

let tiempo=1800;

let intervalo=null;


function mostrarTiempo(){

let min=
Math.floor(tiempo/60);

let seg=
tiempo%60;

document.getElementById("temporizador")
.textContent=
String(min).padStart(2,"0")+
":"+
String(seg).padStart(2,"0");

}


function iniciar(){

if(intervalo)return;

intervalo=setInterval(()=>{

if(tiempo>0){

tiempo--;

mostrarTiempo();

}

else{

clearInterval(intervalo);

intervalo=null;

sumarPuntos(20);

document.getElementById("tiempoMensaje")
.textContent=
"🎉 ¡Terminaste! Ganaste 20 puntos.";

}

},1000);

}


function pausar(){

clearInterval(intervalo);

intervalo=null;

document.getElementById("tiempoMensaje")
.textContent=
"⏸️ Pausado.";

}


function reiniciar(){

clearInterval(intervalo);

intervalo=null;

tiempo=1800;

mostrarTiempo();

}


/* ================= PUNTOS ================= */

function sumarPuntos(cantidad){

puntos+=cantidad;

localStorage.setItem(
"FA21_puntos",
puntos
);

actualizarProgreso();

}


function actualizarProgreso(){

document.getElementById("puntosTotal")
.textContent=puntos;

document.getElementById("juegosTotal")
.textContent=juegos;

document.getElementById("tareasTotal")
.textContent=tareas.length;


let nivel="🌱 Principiante";

if(puntos>=150){

nivel="🏆 Maestro";

}

else if(puntos>=100){

nivel="💎 Experto";

}

else if(puntos>=60){

nivel="🥇 Avanzado";

}

else if(puntos>=30){

nivel="🥈 Intermedio";

}


document.getElementById("nivelUsuario")
.textContent=nivel;


let porcentaje=
Math.min((puntos%30)/30*100,100);

if(puntos>=150){

porcentaje=100;

}


document.getElementById("barra")
.style.width=porcentaje+"%";


document.getElementById("progresoMensaje")
.textContent=
"⭐ Tienes "+puntos+
" puntos. ¡Sigue avanzando!";

}


/* ================= INICIO ================= */

function actualizarInicio(){

let texto="";

if(perfil.nombre){

texto=
"<h3>👋 Hola, "+
perfil.nombre+
"</h3>"+
"<p>"+
perfil.nivel+
" — "+
perfil.grado+
"</p>";

}

else{

texto=
"<p>👋 Personaliza tu perfil para comenzar.</p>";

}


document.getElementById("bienvenida")
.innerHTML=texto;


let alertas="";

tareas.forEach(t=>{

if(t.completada)return;

let fecha=
new Date(
t.fecha+"T"+(t.hora||"23:59")
);

if(fecha<new Date()){

alertas+=
'<div class="alerta">🔴 Tienes una tarea atrasada: '+
t.nombre+
'</div>';

}

else{

let dias=
Math.ceil(
(fecha-new Date())/
86400000
);

if(dias<=2){

alertas+=
'<div class="notificacion">🔔 Próxima entrega: '+
t.nombre+
'</div>';

}

}

});


document.getElementById("alertas")
.innerHTML=alertas;

}


/* ================= CARGA ================= */

cargarPerfil();

mostrarClases();

mostrarTareas();

mostrarHorario();

mostrarEntregas();

actualizarInicio();

actualizarProgreso();

mostrarTiempo();

</script>

</body>
</html>
