# Flores-amarillas-

<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Para Verónica 💛</title>
    <style>
        /* Fondo de Galaxia Nebulosa */
        body {
            margin: 0;
            padding: 0;
            width: 100vw;
            height: 100vh;
            background: radial-gradient(circle at 50% 50%, #1a0b2e 0%, #0b0314 70%, #000000 100%);
            overflow: hidden;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            color: white;
        }

        /* Contenedor de Nebulosa y Estrellas */
        .nebula {
            position: absolute;
            width: 150%;
            height: 150%;
            background: radial-gradient(circle at 30% 20%, rgba(138, 43, 226, 0.15) 0%, transparent 40%),
                        radial-gradient(circle at 70% 80%, rgba(218, 165, 32, 0.1) 0%, transparent 40%);
            filter: blur(40px);
            z-index: 1;
            animation: floatNebula 20s ease-in-out infinite alternate;
        }

        @keyframes floatNebula {
            0% { transform: translate(-5%, -5%) scale(1); }
            100% { transform: translate(5%, 5%) scale(1.1); }
        }

        .star {
            position: absolute;
            background-color: white;
            border-radius: 50%;
            z-index: 2;
            animation: blink var(--duration) ease-in-out infinite;
        }

        @keyframes blink {
            0%, 100% { opacity: 0.2; }
            50% { opacity: 1; }
        }

        /* Contenido Principal */
        .card {
            text-align: center;
            z-index: 10;
            background: rgba(255, 255, 255, 0.05);
            padding: 30px;
            border-radius: 20px;
            backdrop-filter: blur(10px);
            box-shadow: 0 8px 32px 0 rgba(0, 0, 0, 0.37);
            border: 1px solid rgba(255, 255, 255, 0.1);
            max-width: 90%;
            width: 350px;
            animation: fadeIn 2s ease-in-out;
        }

        h1 {
            font-size: 2rem;
            margin-bottom: 10px;
            color: #ffe600;
            text-shadow: 0 0 10px rgba(255, 230, 0, 0.6);
        }

        p {
            font-size: 1.1rem;
            line-height: 1.5;
            color: #f0f0f0;
            margin-bottom: 25px;
        }

        /* Indicación de audio */
        .audio-hint {
            font-size: 0.85rem;
            color: #ffcc00;
            margin-bottom: 15px;
            opacity: 0.8;
            animation: pulseHint 1.5s infinite alternate;
        }

        @keyframes pulseHint {
            from { opacity: 0.4; }
            to { opacity: 1; }
        }

        /* Gran Ramo de Flores Amarillas con CSS Puro */
        .bouquet {
            position: relative;
            width: 150px;
            height: 150px;
            margin: 0 auto;
            animation: pulse 2s infinite ease-in-out;
            cursor: pointer;
        }

        @keyframes pulse {
            0%, 100% { transform: scale(1); }
            50% { transform: scale(1.08); }
        }

        /* Tallos */
        .stems {
            position: absolute;
            bottom: 10px;
            left: 50%;
            transform: translateX(-50%);
            width: 10px;
            height: 60px;
            background: #2d7a43;
            border-radius: 5px;
            z-index: 4;
        }
        .stems::before, .stems::after {
            content: '';
            position: absolute;
            width: 8px;
            height: 55px;
            background: #246335;
            border-radius: 5px;
        }
        .stems::before { transform: rotate(15deg); left: -6px; }
        .stems::after { transform: rotate(-15deg); right: -6px; }

        /* Lazo del Ramo */
        .ribbon {
            position: absolute;
            bottom: 25px;
            left: 50%;
            transform: translateX(-50%);
            width: 24px;
            height: 12px;
            background: #ff477e;
            border-radius: 4px;
            z-index: 6;
            box-shadow: 0 2px 5px rgba(0,0,0,0.3);
        }

        /* Estructura de las Flores */
        .flower {
            position: absolute;
            width: 50px;
            height: 50px;
            z-index: 5;
        }

        /* Posiciones del Ramo */
        .f1 { top: 15px; left: 50px; }
        .f2 { top: 35px; left: 15px; }
        .f3 { top: 35px; left: 85px; }
        .f4 { top: 55px; left: 30px; }
        .f5 { top: 55px; left: 70px; }

        /* Pétalos y Centro */
        .center {
            position: absolute;
            top: 17.5px;
            left: 17.5px;
            width: 15px;
            height: 15px;
            background: #8b5a00;
            border-radius: 50%;
            z-index: 2;
            box-shadow: inset 0 0 4px #000;
        }

        .petals {
            position: absolute;
            width: 100%;
            height: 100%;
            animation: spin 20s linear infinite;
        }

        .petal {
            position: absolute;
            background: #ffcc00;
            border-radius: 50% 50% 0 0;
            width: 14px;
            height: 25px;
            left: 18px;
            top: 0;
            transform-origin: bottom center;
            box-shadow: 0 1px 3px rgba(0,0,0,0.1);
        }

        /* Rotación de los 8 pétalos */
        .p1 { transform: rotate(0deg); }
        .p2 { transform: rotate(45deg); }
        .p3 { transform: rotate(90deg); }
        .p4 { transform: rotate(135deg); }
        .p5 { transform: rotate(180deg); }
        .p6 { transform: rotate(225deg); }
        .p7 { transform: rotate(270deg); }
        .p8 { transform: rotate(315deg); }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }

        /* Ocultar el iframe de música */
        #music-player {
            position: absolute;
            width: 1px;
            height: 1px;
            opacity: 0;
            pointer-events: none;
        }
    </style>
</head>
<body>

    <div class="nebula"></div>
    <div id="stars-container"></div>

    <!-- Reproductor de YouTube Invisible -->
    <iframe id="music-player" src="https://youtube.com" allow="autoplay"></iframe>

    <div class="card">
        <h1>¡Para ti, Verónica! 💛</h1>
        <p>Un detalle brillante en medio del universo. Hoy te esperan muchas flores amarillas y sonrisas.</p>
        
        <div class="audio-hint">✨ Toca las flores para activar la música ✨</div>
        
        <!-- El Ramo Animado -->
        <div class="bouquet" onclick="lanzarEfecto()">
            <div class="stems"></div>
            <div class="ribbon"></div>
            
            <!-- Flor 1 -->
            <div class="flower f1">
                <div class="center"></div>
                <div class="petals">
                    <div class="petal p1"></div><div class="petal p2"></div>
                    <div class="petal p3"></div><div class="petal p4"></div>
                    <div class="petal p5"></div><div class="petal p6"></div>
                    <div class="petal p7"></div><div class="petal p8"></div>
                </div>
            </div>
            <!-- Flor 2 -->
            <div class="flower f2">
                <div class="center"></div>
                <div class="petals">
                    <div class="petal p1"></div><div class="petal p2"></div>
                    <div class="petal p3"></div><div class="petal p4"></div>
                    <div class="petal p5"></div><div class="petal p6"></div>
                    <div class="petal p7"></div><div class="petal p8"></div>
                </div>
            </div>
            <!-- Flor 3 -->
            <div class="flower f3">
                <div class="center"></div>
                <div class="petals">
                    <div class="petal p1"></div><div class="petal p2"></div>
                    <div class="petal p3"></div><div class="petal p4"></div>
                    <div class="petal p5"></div><div class="petal p6"></div>
                    <div class="petal p7"></div><div class="petal p8"></div>
                </div>
            </div>
            <!-- Flor 4 -->
            <div class="flower f4">
                <div class="center"></div>
                <div class="petals">
                    <div class="petal p1"></div><div class="petal p2"></div>
                    <div class="petal p3"></div><div class="petal p4"></div>
                    <div class="petal p5"></div><div class="petal p6"></div>
                    <div class="petal p7"></div><div class="petal p8"></div>
                </div>
            </div>
            <!-- Flor 5 -->
            <div class="flower f5">
                <div class="center"></div>
                <div class="petals">
                    <div class="petal p1"></div><div class="petal p2"></div>
                    <div class="petal p3"></div><div class="petal p4"></div>
                    <div class="petal p5"></div><div class="petal p6"></div>
                    <div class="petal p7"></div><div class="petal p8"></div>
                </div>
            </div>
        </div>
    </div>

    <script>
        // Generador de estrellas aleatorias
        const container = document.getElementById('stars-container');
        const starCount = 80;

        for (let i = 0; i < starCount; i++) {
            const star = document.createElement('div');
            star.classList.add('star');
            const size = Math.random() * 3 + 1;
            star.style.width = `${size}px`;
            star.style.height = `${size}px`;

star.style.top = ${Math.random() * 100}vh;
star.style.left = ${Math.random() * 100}vw;
star.style.setProperty('--duration', ${Math.random() * 3 + 2}s);
container.appendChild(star);
}
// Variable para controlar que la música empiece solo una vez
let musicStarted = false;
// Animación sorpresa interactiva al tocar el ramo + Play Música
function lanzarEfecto() {
// Reproducir música de Tan Biónica a través de la API del iframe
if (!musicStarted) {
const player = document.getElementById('music-player');
player.contentWindow.postMessage('{"event":"command","func":"playVideo","args":""}', '*');
musicStarted = true;
document.querySelector('.audio-hint').style.display = 'none'; // Oculta el recordatorio
}
// Efecto de chispas ✨
for (let i = 0; i < 15; i++) {
const sparkle = document.createElement('div');
sparkle.innerText = '✨';
sparkle.style.position = 'absolute';
sparkle.style.fontSize = '20px';
sparkle.style.left = '50%';
sparkle.style.top = '50%';
sparkle.style.transform = 'translate(-50%, -50%)';
sparkle.style.zIndex = '100';
sparkle.style.transition = 'all 1s ease-out';
document.querySelector('.card').appendChild(sparkle);
const angle = Math.random() * Math.PI * 2;
const distance = Math.random() * 120 + 50;
const x = Math.cos(angle) * distance;
const y = Math.sin(angle) * distance;
setTimeout(() => {
sparkle.style.transform = translate(calc(-50% + ${x}px), calc(-50% + ${y}px)) scale(0);
sparkle.style.opacity = '0';
}, 50);
setTimeout(() => sparkle.remove(), 1000);
}
}


