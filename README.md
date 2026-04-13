<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<title>Seres Vivos - Thiago Resnicoff</title>

<style>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Segoe UI', Roboto, Helvetica, Arial, sans-serif;
}

body {
    /* Fondo de bosque con lago cálido y overlay de atardecer */
    background: linear-gradient(rgba(88, 54, 10, 0.4), rgba(15, 23, 42, 0.7)), 
                url('https://img.freepik.com/foto-gratis/foto-hermoso-paisaje-lago-montanas-verdes-parque-nacional-jiuzhaigou-china_181624-43867.jpg?semt=ais_hybrid&w=740&q=80');
    background-size: cover;
    background-position: center;
    background-attachment: fixed;
    color: white;
    padding: 30px;
    min-height: 100vh;
    display: flex;
    flex-direction: column;
}

/* TITULO PRINCIPAL */
header {
    text-align: center;
    margin-bottom: 40px;
}

header h1 {
    display: inline-block;
    font-size: 42px;
    padding: 10px 30px;
    background: rgba(255, 255, 255, 0.15);
    backdrop-filter: blur(12px);
    -webkit-backdrop-filter: blur(12px);
    border-radius: 20px;
    border: 1px solid rgba(255, 255, 255, 0.3);
    text-shadow: 0 4px 10px rgba(0, 0, 0, 0);
    letter-spacing: 2px;
}

/* SECCIONES */
.section {
    margin-bottom: 40px;
    flex: 1;
}

.section h2 {
    display: inline-block;
    margin-bottom: 15px;
    padding: 5px 20px;
    font-size: 20px;
    background: rgba(251, 146, 60, 0.2); /* Tono naranja suave */
    backdrop-filter: blur(8px);
    -webkit-backdrop-filter: blur(8px);
    border-radius: 12px;
    border: 1px solid rgba(255, 255, 255, 0.2);
    color: white;
    cursor: pointer;
    transition: 0.3s;
}

.section h2:hover {
    background: rgba(251, 146, 60, 0.4);
    transform: translateX(5px);
}

/* GRID Y CARDS */
.grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
    gap: 15px;
}

.card {
    background: rgba(255, 255, 255, 0.1);
    backdrop-filter: blur(15px);
    -webkit-backdrop-filter: blur(15px);
    border: 1px solid rgba(255, 255, 255, 0.15);
    border-radius: 16px;
    padding: 20px;
    text-align: center;
    cursor: pointer;
    transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
}

.card:hover {
    transform: translateY(-5px);
    background: rgba(255, 255, 255, 0.2);
    box-shadow: 0 10px 20px rgba(0,0,0,0.3);
    border-color: rgba(251, 146, 60, 0.5);
}

/* VENTANAS */
.window {
    position: fixed;
    width: 280px;
    background: rgba(28, 18, 10, 0.9);
    backdrop-filter: blur(25px);
    -webkit-backdrop-filter: blur(25px);
    border: 1px solid rgba(251, 146, 60, 0.3);
    border-radius: 18px;
    padding: 20px;
    z-index: 1000;
    box-shadow: 0 15px 35px rgba(0,0,0,0.6);
    animation: fadeIn 0.2s ease-out;
}

@keyframes fadeIn {
    from { opacity: 0; transform: scale(0.9); }
    to { opacity: 1; transform: scale(1); }
}

.window-header {
    display: flex;
    align-items: center;
    margin-bottom: 12px;
    border-bottom: 1px solid rgba(255, 255, 255, 0.1);
    padding-bottom: 8px;
    cursor: grab;
}

.close-btn {
    width: 12px;
    height: 12px;
    background: #ff0d00;
    border-radius: 50%;
    margin-right: 12px;
    cursor: pointer;
}

.window p {
    font-size: 14px;
    line-height: 1.5;
    color: #ffe8d1;
}

/* FOOTER */
footer {
    text-align: center;
    padding: 20px;
    margin-top: 40px;
    background: rgba(0, 0, 0, 0.2);
    backdrop-filter: blur(10px);
    -webkit-backdrop-filter: blur(10px);
    border-radius: 15px;
    border: 1px solid rgba(255, 255, 255, 0.1);
    color: rgba(255, 255, 255, 0.7);
    font-size: 14px;
}

footer strong {
    color: #fb923c;
}
</style>
</head>
<body>

<header>
    <h1>Seres Vivos</h1>
</header>

<div class="section">
    <h2 onclick="openAll(this.parentElement)">• Características</h2>
    <div class="grid">
        <div class="card" onclick="openWindow('celula')">Organización celular</div>
        <div class="card" onclick="openWindow('metabolismo')">Metabolismo</div>
        <div class="card" onclick="openWindow('homeostasis')">Homeostasis</div>
        <div class="card" onclick="openWindow('crecimiento')">Crecimiento</div>
        <div class="card" onclick="openWindow('reproduccion')">Reproducción</div>
        <div class="card" onclick="openWindow('irritabilidad')">Irritabilidad</div>
        <div class="card" onclick="openWindow('evolucion')">Evolución</div>
        <div class="card" onclick="openWindow('desarrollo')">Desarrollo</div>
    </div>
</div>

<div class="section">
    <h2 onclick="openAll(this.parentElement)">• CHONPS</h2>
    <div class="grid">
        <div class="card" onclick="openWindow('c')"> C</div>
        <div class="card" onclick="openWindow('h')"> H</div>
        <div class="card" onclick="openWindow('o')"> O</div>
        <div class="card" onclick="openWindow('n')"> N</div>
        <div class="card" onclick="openWindow('p')"> P</div>
        <div class="card" onclick="openWindow('s')"> S</div>
    </div>
</div>

<div class="section">
    <h2 onclick="openAll(this.parentElement)">• Niveles de Organización</h2>
    <div class="grid">
        <div class="card" onclick="openWindow('atomo')">Átomo</div>
        <div class="card" onclick="openWindow('molecula')">Molécula</div>
        <div class="card" onclick="openWindow('celula')">Célula</div>
        <div class="card" onclick="openWindow('tejido')">Tejido</div>
        <div class="card" onclick="openWindow('organo')">Órgano</div>
        <div class="card" onclick="openWindow('sistema')">Sistema</div>
        <div class="card" onclick="openWindow('organismo')">Organismo</div>
        <div class="card" onclick="openWindow('poblacion')">Población</div>
        <div class="card" onclick="openWindow('comunidad')">Comunidad</div>
        <div class="card" onclick="openWindow('ecosistema')">Ecosistema</div>
        <div class="card" onclick="openWindow('biosfera')">Biosfera</div>
    </div>
</div>

<footer>
    Hecho por <strong>Thiago Resnicoff, Si te sirvió este proyecto, puedes donar a: thiago231012.mp</strong>
</footer>

<script>
const data = {
    celula: "Todos los seres vivos están formados por una o más células.",
    metabolismo: "Conjunto de reacciones químicas que permiten transformar nutrientes en energía.",
    homeostasis: "Capacidad de mantener condiciones internas estables a pesar de los cambios en el exterior.",
    crecimiento: "Aumento del tamaño de las celulas o del número de células.",
    desarrollo: "Cambios morfológicos y funcionales que ocurren a lo largo del ciclo de vida.",
    reproduccion: "Capacidad de reproducirse.",
    irritabilidad: "Capacidad de detectar y reaccionar a estímulos del medio ambiente.",
    evolucion: "Capacidad de las poblaciones de adaptarse y cambiar genéticamente a través de muchas generaciones.",
    c: "Carbono",
    h: "Hidrógeno",
    o: "Oxígeno",
    n: "Nitrógeno",
    p: "Fósforo",
    s: "Azufre",
    atomo: "Unidad más pequeña.",
    molecula: "Unión de dos o mas átomos.",
    celula: "Unidad mas pequeña de la vida.",
    tejido: "Conjunto de células que trabajan de forma coordinada.",
    organo: "Tejidos que trabajan para cumplir una funcion.",
    sistema: "Órganos que cumplen las funciones vitales de un ser vivo.",
    organismo: "Ser vivo completo.",
    poblacion: "Conjunto de organismos de la misma especie.",
    comunidad: "Conjunto de distintas especies.",
    ecosistema: "Comunidad + Ambiente.",
    biosfera: "Todos los ecosistemas de el planeta tierra."
};

let z = 1000;
let offset = 0;

function createWindow(key){
    const win = document.createElement("div");
    win.className = "window";
    win.style.top = (100 + (offset % 300)) + "px";
    win.style.left = (100 + (offset % 300)) + "px";
    win.style.zIndex = z++;
    offset += 30;

    win.innerHTML = `
        <div class="window-header">
            <div class="close-btn"></div>
            <strong style="font-size: 12px; color: #fb923c;">${key.toUpperCase()}</strong>
        </div>
        <p>${data[key]}</p>
    `;

    win.querySelector(".close-btn").onclick = () => win.remove();
    win.onclick = () => win.style.zIndex = z++;

    let isDragging = false;
    let offsetX, offsetY;
    const header = win.querySelector(".window-header");

    header.addEventListener("mousedown", (e) => {
        isDragging = true;
        offsetX = e.clientX - win.offsetLeft;
        offsetY = e.clientY - win.offsetTop;
        win.style.zIndex = z++;
    });

    document.addEventListener("mousemove", (e) => {
        if(isDragging){
            win.style.left = (e.clientX - offsetX) + "px";
            win.style.top = (e.clientY - offsetY) + "px";
        }
    });

    document.addEventListener("mouseup", () => isDragging = false);
    document.body.appendChild(win);
}

function openWindow(key){
    createWindow(key);
}

function openAll(section){
    const cards = section.querySelectorAll(".card");
    cards.forEach(card => card.click());
}
</script>

</body>
</html>
