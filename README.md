<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Virtual Rose for Chhavi</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        body, html {
            height: 100%;
            display: flex;
            justify-content: center;
            align-items: center;
            background-color: #f0f8ff;
            overflow: hidden;
            position: relative;
            font-family: 'Arial', sans-serif;
        }
        .rose-container {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            display: flex;
            justify-content: center;
            align-items: center;
            flex-direction: column;
        }
        .rose {
            position: absolute;
            width: 100px;
            height: 100px;
            background-color: red;
            border-radius: 50%;
            box-shadow: 0 0 15px rgba(255, 0, 0, 0.7);
            animation: float 5s ease-in-out infinite;
        }
        .rose:nth-child(odd) {
            animation-duration: 7s;
            animation-delay: 2s;
        }
        .rose:nth-child(even) {
            animation-duration: 6s;
            animation-delay: 4s;
        }
        @keyframes float {
            0% {
                transform: translateY(0) rotate(0deg);
            }
            50% {
                transform: translateY(-100px) rotate(180deg);
            }
            100% {
                transform: translateY(0) rotate(360deg);
            }
        }
        .message-box {
            position: absolute;
            text-align: center;
            z-index: 1000;
            color: white;
            font-size: 2rem;
            font-weight: bold;
            text-shadow: 2px 2px 10px rgba(0, 0, 0, 0.5);
        }
    </style>
</head>
<body>
    <div class="rose-container">
        <!-- Virtual Roses -->
        <div class="rose" style="left: 10%; animation-delay: 0s;"></div>
        <div class="rose" style="left: 50%; animation-delay: 1s;"></div>
        <div class="rose" style="left: 80%; animation-delay: 3s;"></div>
        <div class="rose" style="left: 20%; animation-delay: 2s;"></div>
        <div class="rose" style="left: 60%; animation-delay: 4s;"></div>

        <!-- Message Box -->
        <div class="message-box" id="message">
            <p>My Dearest Chhavi,</p>
            <p>No matter the time, no matter the place, I love you in every way, and in every situation.</p>
            <p>Happy Rose Day!</p>
        </div>
    </div>

    <script>
        // You can change the message dynamically using JavaScript
        const message = "No matter the time, no matter the place, I love you in every way, and in every situation.";
        const messageElement = document.getElementById('message');

        messageElement.innerHTML = `
            <p>My Dearest Chhavi,</p>
            <p>${message}</p>
            <p>Happy Rose Day!</p>
        `;
    </script>
</body>
</html>
