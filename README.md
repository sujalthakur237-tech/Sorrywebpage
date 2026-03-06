<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>A Heartfelt Apology</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            background: linear-gradient(135deg, #ffeef8 0%, #fff0f6 50%, #ffe6f0 100%);
            overflow: hidden;
        }

        /* Floral Background Animation */
        .flower {
            position: absolute;
            opacity: 0.6;
            font-size: 3rem;
            animation: float 6s ease-in-out infinite;
        }

        .flower:nth-child(1) {
            top: 10%;
            left: 5%;
            animation-delay: 0s;
        }

        .flower:nth-child(2) {
            top: 15%;
            right: 8%;
            animation-delay: 1s;
            font-size: 2.5rem;
        }

        .flower:nth-child(3) {
            bottom: 15%;
            left: 10%;
            animation-delay: 2s;
            font-size: 2rem;
        }

        .flower:nth-child(4) {
            bottom: 10%;
            right: 5%;
            animation-delay: 1.5s;
            font-size: 2.5rem;
        }

        .flower:nth-child(5) {
            top: 50%;
            left: 2%;
            animation-delay: 0.5s;
            font-size: 2rem;
        }

        .flower:nth-child(6) {
            top: 30%;
            right: 3%;
            animation-delay: 2.5s;
            font-size: 2.2rem;
        }

        @keyframes float {
            0%, 100% {
                transform: translateY(0px);
            }
            50% {
                transform: translateY(-20px);
            }
        }

        /* Main Container */
        .container {
            position: relative;
            z-index: 10;
            text-align: center;
            background: rgba(255, 255, 255, 0.95);
            padding: 3rem 2rem;
            border-radius: 20px;
            box-shadow: 0 20px 60px rgba(0, 0, 0, 0.15);
            max-width: 500px;
            width: 90%;
            backdrop-filter: blur(10px);
        }

        h1 {
            color: #d4547b;
            margin-bottom: 1.5rem;
            font-size: 2.5rem;
            letter-spacing: 1px;
        }

        .emoji {
            font-size: 3rem;
            margin-bottom: 1rem;
            display: block;
            animation: pulse 2s ease-in-out infinite;
        }

        @keyframes pulse {
            0%, 100% {
                transform: scale(1);
            }
            50% {
                transform: scale(1.1);
            }
        }

        .subtitle {
            color: #888;
            font-size: 0.95rem;
            margin-bottom: 2rem;
            line-height: 1.6;
        }

        /* Sorry Button */
        .sorry-btn {
            background: linear-gradient(135deg, #ff6b9d 0%, #d4547b 100%);
            color: white;
            border: none;
            padding: 15px 40px;
            font-size: 1.1rem;
            border-radius: 50px;
            cursor: pointer;
            transition: all 0.3s ease;
            font-weight: 600;
            box-shadow: 0 10px 25px rgba(255, 107, 157, 0.4);
            margin-bottom: 2rem;
        }

        .sorry-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 15px 35px rgba(255, 107, 157, 0.6);
        }

        .sorry-btn:active {
            transform: translateY(-1px);
        }

        /* Message Box */
        .message-box {
            max-height: 0;
            overflow: hidden;
            transition: max-height 0.6s ease, opacity 0.6s ease;
            opacity: 0;
        }

        .message-box.show {
            max-height: 500px;
            opacity: 1;
        }

        .message-text {
            background: linear-gradient(135deg, #ffe6f0 0%, #fff0f6 100%);
            border-left: 4px solid #ff6b9d;
            padding: 2rem;
            border-radius: 10px;
            color: #555;
            line-height: 1.8;
            font-size: 1rem;
            text-align: left;
            margin-top: 1rem;
        }

        .message-text p {
            margin-bottom: 1rem;
        }

        .message-text p:last-child {
            margin-bottom: 0;
        }

        .signature {
            margin-top: 1.5rem;
            color: #d4547b;
            font-style: italic;
            font-weight: 600;
        }

        /* Footer */
        .footer {
            position: fixed;
            bottom: 20px;
            right: 20px;
            font-size: 0.85rem;
            color: #999;
        }

        /* Responsive */
        @media (max-width: 600px) {
            .container {
                padding: 2rem 1.5rem;
                margin: 20px;
            }

            h1 {
                font-size: 2rem;
            }

            .emoji {
                font-size: 2.5rem;
            }

            .sorry-btn {
                padding: 12px 30px;
                font-size: 1rem;
            }

            .message-text {
                padding: 1.5rem;
            }
        }
    </style>
</head>
<body>
    <!-- Floating Flowers -->
    <div class="flower">🌸</div>
    <div class="flower">🌹</div>
    <div class="flower">🌺</div>
    <div class="flower">🌼</div>
    <div class="flower">💐</div>
    <div class="flower">🌻</div>

    <!-- Main Container -->
    <div class="container">
        <span class="emoji">💔</span>
        <h1>I'm Sorry</h1>
        <p class="subtitle">I want to express my sincere apologies to you.</p>

        <!-- Sorry Button -->
        <button class="sorry-btn" onclick="showMessage()">Show My Apology</button>

        <!-- Message Box -->
        <div class="message-box" id="messageBox">
            <div class="message-text">
                <p>
                    I want to sincerely apologize for my actions. I realize I made a mistake,
                    and I understand how it may have hurt you.
                </p>
                <p>
                    There's no excuse for what I did. I take full responsibility and deeply
                    regret my behavior. You deserve better, and I'm truly sorry.
                </p>
                <p>
                    I hope you can find it in your heart to forgive me. I'm committed to
                    making things right and being better moving forward.
                </p>
                <p>
                    Thank you for taking the time to listen. Your feelings matter to me.
                </p>
                <div class="signature">
                    With sincere regrets,<br>
                    Someone Who Cares
                </div>
            </div>
        </div>
    </div>

    <div class="footer">
        Created with 💕 and sincerity
    </div>

    <script>
        function showMessage() {
            const messageBox = document.getElementById('messageBox');
            messageBox.classList.toggle('show');
        }
    </script>
</body>
</html>
