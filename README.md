<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Dear Letter</title>
    <style>
        body {
            font-family: 'Comic Sans MS', cursive, sans-serif;
            background-color: #ffe4e1;
            text-align: center;
            color: #ff69b4;
            margin: 0;
            padding: 0;
        }
        .scrapbook {
            background: url('scrapbook-background.jpg') no-repeat center center;
            background-size: cover;
            padding: 30px;
            margin: 10px auto;
            width: 90%;
            max-width: 600px;
            border: 15px solid #f8c8dc;
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
            border-radius: 15px;
        }
        .envelope {
            font-size: 80px;
            margin: 20px auto;
            cursor: pointer;
            transition: transform 0.3s;
        }
        .envelope:hover {
            transform: scale(1.2);
        }
        .surprise, .message, .polaroid {
            display: none;
        }
        .surprise {
            font-size: 60px;
            margin: 20px 0;
            animation: pop 0.5s ease-in-out forwards;
        }
        .polaroid {
            margin: 20px auto;
            width: 300px;
            height: 400px;
            background-color: #fff;
            border: 10px solid #ffb6c1;
            box-shadow: 5px 5px 15px rgba(0,0,0,0.2);
            transform: rotate(-5deg);
        }
        .polaroid img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            border-radius: 5px;
        }
        .message {
            font-size: 24px;
            margin-top: 20px;
            background-color: #fff;
            padding: 15px;
            border-radius: 10px;
            box-shadow: 3px 3px 10px rgba(0,0,0,0.1);
            transform: rotate(2deg);
        }
        @keyframes pop {
            0% { transform: scale(0); }
            100% { transform: scale(1); }
        }
    </style>
</head>
<body>
    <div class="scrapbook">
        <div class="envelope" id="envelope">💌</div>
        <div class="surprise" id="surprise">🎉</div>
        <div class="polaroid" id="polaroid">
            <img src="your-friends-photo.jpg" alt="Happy Birthday">
        </div>
        <div class="message" id="message">Happy Birthday! Wishing you all the joy and happiness in the world!</div>
    </div>

    <script>
        document.getElementById('envelope').addEventListener('click', function() {
            this.style.display = 'none';
            document.getElementById('surprise').style.display = 'block';
            setTimeout(function() {
                document.getElementById('surprise').style.display = 'none';
                document.getElementById('polaroid').style.display = 'block';
                document.getElementById('message').style.display = 'block';
            }, 1000);
        });
    </script>
</body>
</html>
