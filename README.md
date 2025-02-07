<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>¿Quieres ser mi San Valentín?</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            text-align: center;
            background: #f8f9fa;
            color: #333;
            margin-top: 50px;
        }
        button {
            font-size: 1.2em;
            padding: 10px 20px;
            margin: 10px;
            cursor: pointer;
            border: none;
            border-radius: 5px;
            transition: background 0.3s, transform 0.3s;
        }
        button:hover {
            transform: scale(1.1);
        }
        #yesBtn {
            background: #28a745;
            color: #fff;
        }
        #noBtn {
            background: #dc3545;
            color: #fff;
        }
        .hidden {
            display: none;
        }
        .celebration {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            text-align: center;
        }
        .confetti {
            position: absolute;
            width: 10px;
            height: 10px;
            background: #ffd700;
            animation: fall 2s linear infinite;
        }
        @keyframes fall {
            0% { top: -10px; opacity: 1; }
            100% { top: 100%; opacity: 0; }
        }
    </style>
</head>
<body>
    <h1>Mi vida, ya falta poco para vernos</h1>
    <p>y solo quería preguntarte si quisieras ser mi San Valentín?</p>
    <button id="yesBtn">Sí</button>
    <button id="noBtn">No</button>
    <p id="response" class="hidden">¡Gracias por aceptar!</p>
    <p id="tryAgain" class="hidden">Por favor, vuelve a intentarlo.</p>
    
    <div id="celebration" class="celebration hidden">
        <h2>¡Felicidades!</h2>
        <div class="confetti" style="animation-delay: 0s;"></div>
        <div class="confetti" style="animation-delay: 0.2s;"></div>
        <div class="confetti" style="animation-delay: 0.4s;"></div>
        <div class="confetti" style="animation-delay: 0.6s;"></div>
        <div class="confetti" style="animation-delay: 0.8s;"></div>
    </div>
    
    <script>
        document.getElementById("yesBtn").addEventListener("click", function() {
            document.getElementById("response").classList.remove("hidden");
            document.getElementById("tryAgain").classList.add("hidden");
            document.getElementById("celebration").classList.remove("hidden");
        });
        document.getElementById("noBtn").addEventListener("click", function() {
            document.getElementById("tryAgain").classList.remove("hidden");
            document.getElementById("response").classList.add("hidden");
            document.getElementById("celebration").classList.add("hidden");
        });
    </script>
    <p><a href="https://example.com">Comparte esta página</a></p>
</body>
</html>

