# gmodpixel.github.io
Pixel Battle
function generateRandomPixels() {
    let pixels = [];
    for (let i = 0; i < 10; i++) {
        let pixel = {
            x: Math.floor(Math.random() * 100), 
            y: Math.floor(Math.random() * 100), 
            color: '#' + Math.floor(Math.random() * 16777215).toString(16)
        };
        pixels.push(pixel);
    }
    return pixels;
}

function updatePixels() {
    let pixels = generateRandomPixels();
    let pixelData = JSON.stringify({ pixels: pixels });
}

setInterval(updatePixels, 2000);

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Pixel Battle</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
        }
        #pixel-display {
            font-size: 14px;
            white-space: pre-wrap;
            background-color: #111;
            color: #00FF00;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0, 255, 0, 0.5);
            margin-top: 20px;
        }
    </style>
</head>
<body>
    <h1>Pixel Battle</h1>
    <p>Welcome to the Pixel Battle! Watch as the pixels change randomly!</p>
    <div id="pixel-display">
        {"pixels": []}
    </div>
    <script src="pixel.js"></script>
</body>
</html>
