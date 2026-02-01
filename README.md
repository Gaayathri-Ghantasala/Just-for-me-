<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Ammulu ❤️</title>

    <style>
        body {
            margin: 0;
            height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            background: linear-gradient(135deg, #ff9a9e, #fad0c4);
            font-family: Arial, sans-serif;
            overflow: hidden;
        }

        .card {
            position: relative;
            width: 650px;
            height: 460px;
            background: white;
            border-radius: 25px;
            box-shadow: 0 15px 40px rgba(0,0,0,0.25);
            text-align: center;
            padding: 50px 25px 0;
        }

        h1 {
            color: #e63946;
        }

        p {
            color: red;
            margin-bottom: 25px;
            font-size: 16px;
        }

        h2 {
            margin-bottom: 40px;
            font-size: 18px;
            color: #333;
        }

        .yes {
            background: #ff4d6d;
            color: white;
            border: none;
            padding: 14px 28px;
            border-radius: 30px;
            font-size: 16px;
            cursor: pointer;
        }

        .no {
            position: absolute;
            background: #adb5bd;
            color: white;
            border: none;
            padding: 14px 28px;
            border-radius: 30px;
            font-size: 16px;
            cursor: pointer;
            top: 310px;
            left: 390px;
        }

        #result {
            margin-top: 35px;
            font-size: 22px;
            color: #2a9d8f;
            display: none;
        }
    </style>
</head>
<body>

<div class="card" id="card">
    <h1>Hey Girls</h1>
    <p>Okati adagana</p>

    <h2>
        Nv nannu gajubomma laga chusukunta annav kada,<br>
        mari alane chusukuntava nannu nijam cheppu ma?
    </h2>

    <button class="yes" onclick="yesAnswer()">Ha Podam 💖</button>
    <button class="no" id="noBtn">Vaddu povaddu 💔</button>

    <div id="result"></div>
</div>

<script>
    const noBtn = document.getElementById("noBtn");
    const card = document.getElementById("card");

    function moveNoButton() {
        const cardWidth = card.clientWidth;
        const cardHeight = card.clientHeight;

        const btnWidth = noBtn.offsetWidth;
        const btnHeight = noBtn.offsetHeight;

        const randomX = Math.random() * (cardWidth - btnWidth);
        const randomY = Math.random() * (cardHeight - btnHeight);

        noBtn.style.left = randomX + "px";
        noBtn.style.top = randomY + "px";
    }

    noBtn.addEventListener("mouseenter", moveNoButton);
    noBtn.addEventListener("touchstart", function(e) {
        e.preventDefault();
        moveNoButton();
    });

    function yesAnswer() {
        const result = document.getElementById("result");
        result.style.display = "block";
        result.innerHTML = "Then Get ready";
    }
</script>

</body>
</html>
