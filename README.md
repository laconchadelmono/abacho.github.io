<!DOCTYPE html>
<html lang="es">
<head>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Anton+SC&family=Coral+Pixels&display=swap" rel="stylesheet">
    <meta charset="UTF-8">
    <link rel="icon" href="media/LOGO CANNA 2.png">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CANNA</title>
    <style>
        /* Estilos CSS básicos para la landing page */
        body {
            font-family: "Anton SC", sans-serif;
            font-weight: 50;
            font-style: oblique;
            margin: 0;
            padding: 0;
            background-color: #76B041;
            color: #fafafa;
            text-align: center;
        }
        header {
            color: white;
            padding: 50px 0;
            letter-spacing: 8px;
            text-decoration: double;
        }
        h1 {
            font-size: 7em;
            margin-bottom: 20px;
            letter-spacing: 8px;
        }
        .countdown-container {
            padding: 40px 20px;
            background-color: #76B041;
            margin: 20px auto;
            letter-spacing: 8px;
            border-radius: 8px;
            max-width: 600px;
        }
        #countdown {
            font-size: 2.5em;
            font-weight: bold;
            letter-spacing: 8px;
            color: #E9F1F7; /* Color llamativo para la cuenta */
        }
        footer {
            Color: #E9F1F7;
            padding: 20px 0;
            position: fixed;
            bottom: 0;
            width: 100%;
        }
        .social-links a {
            color: #E9F1F7;
            margin: 0 20px;
            text-decoration: wavy;
            font-size: 2em;
        }
        .social-links a:hover {
            color: #4d814b;
            transition: 0.5s;
        }
    </style>
</head>
<body>

    <header>
        <h1>CANNA</h1>
        <p>¡Algo grande está por llegar!</p>

    <div class="countdown-container">
        <h2>Lanzamiento en:</h2>
        <p id="countdown">Cargando...</p>
    </div>
</header>
    <footer>
        <div class="social-links">
            <p>Enterate más acá:</p>
            <a href="https://www.tiktok.com/@canna.ar" target="_blank">TikTok</a>
            <a href="https://www.instagram.com/canna_ar/" target="_blank">Instagram</a>
            <a href="https://x.com/Cannaar" target="_blank">X</a>
        </div>
        <p>&copy; 2025 CANNA. Todos los derechos reservados.</p>
    </footer>

    <script>
        // Establece la fecha y hora de destino (ejemplo: 1 de diciembre de 2025 a las 10:00:00)
        const targetDate = new Date("Dec 1, 2025 10:00:00").getTime();

        // Actualiza la cuenta regresiva cada 1 segundo
        const interval = setInterval(function() {

            // Obtiene la fecha y hora de hoy
            const now = new Date().getTime();

            // Encuentra la distancia entre ahora y la fecha de destino
            const distance = targetDate - now;

            // Cálculos de tiempo para días, horas, minutos y segundos
            const days = Math.floor(distance / (1000 * 60 * 60 * 24));
            const hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
            const minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
            const seconds = Math.floor((distance % (1000 * 60)) / 1000);

            // Muestra el resultado en el elemento con id="countdown"
            document.getElementById("countdown").innerHTML = days + "D " + hours + "H "
            + minutes + "M " + seconds + "S ";

            // Si la cuenta regresiva ha terminado, escribe un texto
            if (distance < 0) {
                clearInterval(interval);
                document.getElementById("countdown").innerHTML = "¡LANZADO!";
            }
        }, 1000);
    </script>

</body>
</html>
