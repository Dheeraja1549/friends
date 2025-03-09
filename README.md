<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Goodbye Friends</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            margin: 0;
            padding: 0;
            background-image: url('https://www.w3schools.com/w3images/mountains.jpg'); /* Change image URL */
            background-size: cover;
            background-position: center;
            color: #fff;
            height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            text-align: center;
        }
        .overlay {
            background-color: rgba(0, 0, 0, 0.6); /* semi-transparent overlay */
            padding: 30px;
            border-radius: 10px;
        }
        h1 {
            font-size: 3em;
            color: #ff6347;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.6);
        }
        .quote {
            font-size: 1.5em;
            font-style: italic;
            color: #fff;
            margin-top: 20px;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.6);
        }
        .footer {
            font-size: 1.2em;
            color: #fff;
            margin-top: 30px;
            font-weight: lighter;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.6);
        }
        button {
            background-color: #ff6347;
            color: #fff;
            font-size: 1.2em;
            padding: 15px 30px;
            border: none;
            border-radius: 10px;
            cursor: pointer;
            margin-top: 30px;
            transition: background-color 0.3s;
        }
        button:hover {
            background-color: #ff4500;
        }
        .heart {
            position: absolute;
            font-size: 30px;
            color: red;
            animation: heart-animation 1s ease-in-out forwards;
        }
        @keyframes heart-animation {
            0% {
                transform: scale(0);
            }
            100% {
                transform: scale(2) translateY(-200px);
            }
        }
    </style>
</head>
<body>

<div class="overlay">
    <h1>Bye Bye, Friends!</h1>
    <p class="quote">"Bye Bye Mittro, Maje karna aage<br>Yad aaygi pure sal ki backchodi </p>
    <div class="footer">
        <p>Thank you for all the memories. Until we meet again!</p>
    </div>
    <button id="byeButton">Bye!</button>
</div>

<script>
    document.getElementById('byeButton').addEventListener('click', function() {
        for (let i = 0; i < 50; i++) {
            let heart = document.createElement('div');
            heart.classList.add('heart');
            heart.innerHTML = '❤️';
            heart.style.left = `${Math.random() * window.innerWidth}px`;
            heart.style.top = `${Math.random() * window.innerHeight}px`;
            document.body.appendChild(heart);
            
            // Remove heart after animation completes
            setTimeout(() => {
                heart.remove();
            }, 1000);
        }
    });
</script>

</body>
</html>
