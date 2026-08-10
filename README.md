```html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Happy Birthday Cutie 💗</title>

<style>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: "Segoe UI", sans-serif;
    overflow: hidden;
    background: #fff0f6;
    color: #5a2942;
}

.screen {
    width: 100%;
    height: 100vh;
    display: none;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    text-align: center;
    position: relative;
    overflow: hidden;
}

.screen.active {
    display: flex;
}

/* ---------- OPENING ---------- */

#letterScreen {
    background: linear-gradient(135deg, #ffd6e8, #fff1f7);
}

.envelope {
    width: 300px;
    padding: 45px 25px;
    background: rgba(255,255,255,0.85);
    border-radius: 25px;
    box-shadow: 0 20px 50px rgba(180,70,120,0.2);
    animation: float 3s ease-in-out infinite;
}

.envelope h1 {
    font-size: 32px;
    color: #e83e8c;
    margin-bottom: 15px;
}

.envelope p {
    font-size: 17px;
    margin-bottom: 25px;
}

button {
    border: none;
    cursor: pointer;
    font-size: 16px;
    font-weight: bold;
    padding: 13px 27px;
    border-radius: 30px;
    background: #ff5c9a;
    color: white;
    box-shadow: 0 8px 20px rgba(255,92,154,0.3);
    transition: 0.3s;
}

button:hover {
    transform: scale(1.08);
}

/* ---------- YES NO ---------- */

#questionScreen {
    background: linear-gradient(135deg, #ffe1ed, #fff7fa);
}

.question-box {
    background: rgba(255,255,255,0.9);
    padding: 40px;
    border-radius: 30px;
    width: min(90%, 500px);
    box-shadow: 0 20px 50px rgba(180,70,120,0.18);
}

.question-box h1 {
    color: #e83e8c;
    margin-bottom: 15px;
}

.question-box p {
    margin-bottom: 25px;
}

.buttons {
    display: flex;
    justify-content: center;
    gap: 20px;
}

.no {
    background: #aaa;
}

/* ---------- FLOWERS ---------- */

#flowerScreen {
    background: linear-gradient(#fff0f7, #ffd8e9);
}

.flower {
    position: absolute;
    top: -60px;
    font-size: 30px;
    animation: fall linear forwards;
    pointer-events: none;
}

@keyframes fall {
    to {
        transform: translateY(110vh) rotate(720deg);
    }
}

/* ---------- BOUQUET ---------- */

.bouquet {
    font-size: 120px;
    animation: bouquetPop 1.5s ease forwards;
}

@keyframes bouquetPop {
    0% {
        transform: scale(0) rotate(-20deg);
        opacity: 0;
    }

    70% {
        transform: scale(1.15) rotate(5deg);
    }

    100% {
        transform: scale(1);
        opacity: 1;
    }
}

.bouquet-text {
    max-width: 600px;
    padding: 20px;
}

.bouquet-text h1 {
    color: #e83e8c;
    margin-bottom: 15px;
}

.bouquet-text p {
    font-size: 19px;
    line-height: 1.6;
}

/* ---------- REASONS ---------- */

#reasonScreen {
    background: linear-gradient(135deg, #fff0f6, #ffe0ed);
    padding: 30px;
}

.reason-title {
    color: #e83e8c;
    margin-bottom: 30px;
}

.reason-container {
    display: flex;
    gap: 20px;
    flex-wrap: wrap;
    justify-content: center;
}

.reason-card {
    width: 220px;
    min-height: 170px;
    padding: 25px;
    border-radius: 25px;
    background: rgba(255,255,255,0.9);
    box-shadow: 0 15px 35px rgba(180,70,120,0.15);
    transition: 0.4s;
}

.reason-card:hover {
    transform: translateY(-12px) rotate(2deg);
}

.reason-card h2 {
    color: #e83e8c;
    margin-bottom: 15px;
}

.reason-card p {
    line-height: 1.5;
}

/* ---------- CAKE ---------- */

#cakeScreen {
    background: radial-gradient(circle, #fff4f8, #ffd9e8);
}

.cake {
    font-size: 150px;
    margin-bottom: 10px;
    animation: cakeFloat 2s ease-in-out infinite;
}

@keyframes cakeFloat {
    0%, 100% {
        transform: translateY(0);
    }

    50% {
        transform: translateY(-10px);
    }
}

.cake-screen h1 {
    color: #e83e8c;
    margin-bottom: 10px;
}

.cake-screen p {
    margin-bottom: 25px;
}

/* ---------- FINAL ---------- */

#finalScreen {
    background: linear-gradient(135deg, #ffb6d5, #ffeaf3);
}

.final-heart {
    font-size: 100px;
    animation: heartBeat 1s infinite;
}

@keyframes heartBeat {
    0%, 100% {
        transform: scale(1);
    }

    50% {
        transform: scale(1.2);
    }
}

#finalScreen h1 {
    color: #e52d7b;
    font-size: clamp(35px, 7vw, 65px);
    margin: 15px;
}

#finalScreen p {
    font-size: 20px;
    max-width: 600px;
    line-height: 1.7;
    padding: 20px;
}

/* CONFETTI */

.confetti {
    position: absolute;
    top: -20px;
    width: 10px;
    height: 20px;
    animation: confettiFall 3s linear forwards;
}

@keyframes confettiFall {
    to {
        transform: translateY(110vh) rotate(720deg);
    }
}

/* HEARTS */

.heart {
    position: absolute;
    font-size: 25px;
    animation: heartFloat 4s linear forwards;
}

@keyframes heartFloat {
    0% {
        transform: translateY(100vh);
        opacity: 0;
    }

    20% {
        opacity: 1;
    }

    100% {
        transform: translateY(-20vh);
        opacity: 0;
    }
}

/* MOBILE */

@media(max-width:600px) {

    .envelope {
        width: 85%;
    }

    .envelope h1 {
        font-size: 27px;
    }

    .question-box {
        padding: 30px 20px;
    }

    .reason-card {
        width: 90%;
    }

    .bouquet {
        font-size: 90px;
    }

    .cake {
        font-size: 110px;
    }
}
</style>
</head>

<body>

<!-- ================= LETTER ================= -->

<section id="letterScreen" class="screen active">

    <div class="envelope">

        <h1>💌 Happy Birthday Cutie 💗</h1>

        <p>
            I made a little surprise for you...<br>
            Tap below to open it ✨
        </p>

        <button onclick="openLetter()">
            Tap to Open 💕
        </button>

    </div>

</section>


<!-- ================= YES / NO ================= -->

<section id="questionScreen" class="screen">

    <div class="question-box">

        <h1>🥺 One little question...</h1>

        <p id="questionText">
            Do you want to open your birthday surprise? 💗
        </p>

        <div class="buttons">

            <button onclick="yesClicked()">
                YES 💕
            </button>

            <button class="no" onclick="noClicked()">
                NO 😭
            </button>

        </div>

    </div>

</section>


<!-- ================= FLOWERS ================= -->

<section id="flowerScreen" class="screen">

    <div class="bouquet">
        💐
    </div>

    <div class="bouquet-text">

        <h1>A Bouquet Just For You 🌸</h1>

        <p>
            Because someone as special as you deserves
            a whole garden of flowers. 🌷💗
            <br>
            Happy Birthday, Cutie. You make everything brighter. ✨
        </p>

        <br>

        <button onclick="showReasons()">
            There's More 💕
        </button>

    </div>

</section>


<!-- ================= REASONS ================= -->

<section id="reasonScreen" class="screen">

    <h1 class="reason-title">
        💕 Reasons I Like You 💕
    </h1>

    <div class="reason-container">

        <div class="reason-card">

            <h2>😊 Your Smile</h2>

            <p>
                Your smile has this magical way of making
                everything around you feel better.
            </p>

        </div>


        <div class="reason-card">

            <h2>💗 Your Heart</h2>

            <p>
                You're genuinely caring and sweet,
                and that's something I really adore about you.
            </p>

        </div>


        <div class="reason-card">

            <h2>✨ Just You</h2>

            <p>
                Honestly, I don't even need a reason.
                You're simply you, and that's enough.
            </p>

        </div>

    </div>

    <br><br>

    <button onclick="showCake()">
        One Last Surprise 🎁
    </button>

</section>


<!-- ================= CAKE ================= -->

<section id="cakeScreen" class="screen cake-screen">

    <div class="cake">
        🎂
    </div>

    <h1>Make a Wish ✨</h1>

    <p>
        Close your eyes...<br>
        Make your biggest wish... 💗
    </p>

    <button onclick="blowCandles()">
        🕯️ Blow the Candles
    </button>

</section>


<!-- ================= FINAL ================= -->

<section id="finalScreen" class="screen">

    <div class="final-heart">
        💗
    </div>

    <h1>
        HAPPY BIRTHDAY CUTIE! 🎉
    </h1>

    <p>
        I hope your day is as beautiful, adorable
        and special as you are. 🌸
        <br><br>
        Keep smiling, keep shining,
        and never forget how special you are. 💕
        <br><br>
        Once again... Happy Birthday! 🎂✨
    </p>

</section>


<script>

/* =========================================
   SCREEN CONTROL
========================================= */

function showScreen(id) {

    document.querySelectorAll(".screen").forEach(screen => {
        screen.classList.remove("active");
    });

    document.getElementById(id).classList.add("active");
}


/* =========================================
   OPEN LETTER
========================================= */

function openLetter() {

    showScreen("questionScreen");

}


/* =========================================
   NO BUTTON
========================================= */

function noClicked() {

    const text = document.getElementById("questionText");

    text.innerHTML =
        "Why nooo? 🥺💔<br><br>" +
        "I made this little surprise just for you...";

}


/* =========================================
   YES BUTTON
========================================= */

function yesClicked() {

    showScreen("flowerScreen");

    startFlowerRain();

}


/* =========================================
   FLOWER RAIN
========================================= */

function startFlowerRain() {

    const flowers = [
        "🌸",
        "🌷",
        "🌹",
        "🌺",
        "🌻",
        "💮",
        "🌼",
        "🪷"
    ];

    for(let i = 0; i < 120; i++) {

        setTimeout(() => {

            const flower = document.createElement("div");

            flower.className = "flower";

            flower.innerText =
                flowers[Math.floor(Math.random() * flowers.length)];

            flower.style.left =
                Math.random() * 100 + "vw";

            flower.style.fontSize =
                (20 + Math.random() * 25) + "px";

            flower.style.animationDuration =
                (3 + Math.random() * 5) + "s";

            document.getElementById("flowerScreen")
                .appendChild(flower);

            setTimeout(() => {
                flower.remove();
            }, 9000);

        }, i * 40);

    }

}


/* =========================================
   REASONS
========================================= */

function showReasons() {

    showScreen("reasonScreen");

}


/* =========================================
   CAKE
========================================= */

function showCake() {

    showScreen("cakeScreen");

}


/* =========================================
   BLOW CANDLES
========================================= */

function blowCandles() {

    showScreen("finalScreen");

    createConfetti();

    createHearts();

}


/* =========================================
   CONFETTI
========================================= */

function createConfetti() {

    for(let i = 0; i < 150; i++) {

        const piece = document.createElement("div");

        piece.className = "confetti";

        piece.style.left =
            Math.random() * 100 + "vw";

        piece.style.animationDuration =
            (2 + Math.random() * 3) + "s";

        piece.style.background =
            `hsl(${Math.random() * 360}, 80%, 65%)`;

        piece.style.transform =
            `rotate(${Math.random() * 360}deg)`;

        document.getElementById("finalScreen")
            .appendChild(piece);

    }

}


/* =========================================
   FLOATING HEARTS
========================================= */

function createHearts() {

    const hearts = [
        "💗",
        "💖",
        "💕",
        "💓",
        "❤️",
        "💘"
    ];

    for(let i = 0; i < 40; i++) {

        setTimeout(() => {

            const heart = document.createElement("div");

            heart.className = "heart";

            heart.innerText =
                hearts[Math.floor(Math.random() * hearts.length)];

            heart.style.left =
                Math.random() * 100 + "vw";

            heart.style.animationDuration =
                (3 + Math.random() * 3) + "s";

            document.getElementById("finalScreen")
                .appendChild(heart);

        }, i * 100);

    }

}

</script>

</body>
</html>
```
