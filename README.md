# PropuestaYis
Pagina web para el 14 
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>¿Pasamos el 14 de febrero juntos?</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            margin: 50px;
        }
        #mensaje {
            font-size: 20px;
            margin-bottom: 20px;
        }
        #botones {
            position: relative;
        }
        button {
            font-size: 20px;
            padding: 10px 20px;
            margin: 10px;
            cursor: pointer;
        }
        #no {
            transition: all 0.3s ease;
            position: absolute;
        }
    </style>
</head>
<body>
    <h2>Amor mío, mi vida entera, mi amorcito, mi todo...</h2>
    <p id="mensaje">Sé que aunque no podremos estar juntos físicamente, quiero que sepas que cuando te vea, lo celebraremos. Te amo muchísimo, y mi amor por ti crece exponencialmente cada día. Será solo un símbolo, y lo pasaremos juntos cuando se pueda. ¡Te amo muchísimo!</p>
    <div id="botones">
        <button id="si" onclick="aceptar()">Sí</button>
        <button id="no" onclick="rechazar()">No</button>
    </div>
    
    <script>
        let intentos = 0;
        function aceptar() {
            alert("¡Sabía que dirías que sí! 🥰 Te amo muchísimo 💖");
        }
        function rechazar() {
            intentos++;
            let noBtn = document.getElementById("no");
            let siBtn = document.getElementById("si");
            let mensaje = document.getElementById("mensaje");
            
            if (intentos < 3) {
                noBtn.style.fontSize = (20 - intentos * 5) + "px";
                siBtn.style.fontSize = (20 + intentos * 5) + "px";
                mensaje.innerText = "Sé que sí quieres, pero se te habrá presionado mal... 💖";
            } else {
                mensaje.innerText = "Vamos, sé que te vas a divertir... 😘";
                noBtn.style.position = "absolute";
                moverBoton();
            }
        }
        function moverBoton() {
            let noBtn = document.getElementById("no");
            let maxX = window.innerWidth - noBtn.offsetWidth;
            let maxY = window.innerHeight - noBtn.offsetHeight;
            noBtn.style.left = Math.random() * maxX + "px";
            noBtn.style.top = Math.random() * maxY + "px";
        }
    </script>
</body>
</html>

