# arthuro.github.io
testing
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Answer Honestly!</title>
    <style>
        body {
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            height: 100vh;
            font-family: Arial, sans-serif;
            background-color: #ffe6e6;
            margin: 0;
            overflow: hidden;
        }
        h1 {
            color: #d32f2f;
        }
        .buttons {
            margin-top: 20px;
        }
        button {
            font-size: 1.2rem;
            padding: 10px 20px;
            margin: 0 15px;
            cursor: pointer;
            border: none;
            border-radius: 5px;
        }
        #yesBtn {
            background-color: #4caf50;
            color: white;
        }
        #noBtn {
            background-color: #f44336;
            color: white;
            position: absolute; /* Crucial for moving the button anywhere */
        }
    </style>
</head>
<body>

    <h1>Do you love me? ❤️</h1>
    
    <div class="buttons">
        <button id="yesBtn" onclick="alert('I knew it! 🥰')">Yes</button>
        <button id="noBtn">No</button>
    </div>

    <script>
        const noBtn = document.getElementById('noBtn');

        // Set initial positions so it stays next to the Yes button at first
        noBtn.style.left = 'calc(50% + 20px)';
        noBtn.style.top = 'calc(50% + 20px)';

        // Detect when the mouse enters or hovers over the button
        noBtn.addEventListener('mouseover', () => {
            // Calculate random positions within the browser window bounds
            const maxX = window.innerWidth - noBtn.offsetWidth;
            const maxY = window.innerHeight - noBtn.offsetHeight;

            const randomX = Math.floor(Math.random() * maxX);
            const randomY = Math.floor(Math.random() * maxY);

            // Instantly move the button
            noBtn.style.left = randomX + 'px';
            noBtn.style.top = randomY + 'px';
        });
    </script>

</body>
</html>
