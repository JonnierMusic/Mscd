<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Descargar Audio de YouTube</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f0f0f0;
            margin: 0;
            padding: 20px;
            text-align: center;
        }
        .container {
            max-width: 600px;
            margin: 0 auto;
            background: white;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 0 10px rgba(0,0,0,0.1);
        }
        h1 {
            color: #ff0000;
        }
        input {
            width: 80%;
            padding: 10px;
            margin: 10px 0;
            border: 1px solid #ccc;
            border-radius: 4px;
        }
        button {
            background-color: #ff0000;
            color: white;
            border: none;
            padding: 10px 20px;
            border-radius: 4px;
            cursor: pointer;
        }
        button:hover {
            background-color: #cc0000;
        }
        #result {
            margin-top: 20px;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Descargar Audio de YouTube</h1>
        <p>Pega el enlace de YouTube aquí:</p>
        <input type="text" id="youtube-url" placeholder="Ej: https://www.youtube.com/watch?v=...">
        <button onclick="downloadAudio()">Descargar Audio</button>
        <div id="result"></div>
    </div>

    <script>
        function downloadAudio() {
            const url = document.getElementById('youtube-url').value;
            const resultDiv = document.getElementById('result');

            if (!url.includes('youtube.com') && !url.includes('youtu.be')) {
                resultDiv.innerHTML = '<p style="color: red;">⚠️ Ingresa un enlace válido de YouTube.</p>';
                return;
            }

            // API pública para conversión (ejemplo: loader.to)
            resultDiv.innerHTML = '<p>Convirtiendo audio... ⏳</p>';
            
            // Nota: Para una solución real, necesitarías una API propia o un servicio como:
            // - loader.to (tiene API de pago)
            // - yt-dlp (requiere backend)
            // Este es un ejemplo simplificado.
            
            setTimeout(() => {
                resultDiv.innerHTML = `
                    <p>✅ Audio listo para descargar.</p>
                    <p><small><i>Nota: Este es un ejemplo. Para una funcionalidad real, necesitarías configurar un backend.</i></small></p>
