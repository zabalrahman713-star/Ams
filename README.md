<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Happy Valentine Devi Yulianti ❤️</title>

<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;600&family=Dancing+Script:wght@700&display=swap" rel="stylesheet">

<style>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    height: 100vh;
    overflow: hidden;
    display: flex;
    justify-content: center;
    align-items: center;
    text-align: center;
    font-family: 'Poppins', sans-serif;
    background: linear-gradient(135deg, #ff6b9d, #ff1e56);
    position: relative;
}

/* Container */
.container {
    z-index: 2;
    color: white;
    padding: 20px;
}

/* Main Title */
h1 {
    font-family: 'Dancing Script', cursive;
    font-size: 3rem;
    opacity: 0;
    animation: fadeIn 2s ease forwards;
    text-shadow: 0 0 10px rgba(255,255,255,0.8),
                 0 0 20px rgba(255,255,255,0.6),
                 0 0 30px rgba(255,0,80,0.8);
}

h2 {
    margin-top: 10px;
    font-weight: 300;
    opacity: 0;
    animation: fadeIn 3s ease forwards;
}

/* Button */
button {
    margin-top: 25px;
    padding: 12px 25px;
    border: none;
    border-radius: 30px;
    background: white;
    color: #ff1e56;
    font-size: 1rem;
    font-weight: bold;
    cursor: pointer;
    transition: 0.3s ease;
}

button:hover {
    transform: scale(1.1);
    box-shadow: 0 0 15px white;
}

/* Popup */
.popup {
    position: fixed;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%) scale(0);
    background: white;
    color: #ff1e56;
    padding: 25px 30px;
    border-radius: 20px;
    font-size: 1.2rem;
    font-weight: 600;
    text-align: center;
    box-shadow: 0 0 25px rgba(0,0,0,0.2);
    transition: transform 0.4s ease;
    z-index: 5;
}

.popup.show {
    transform: translate(-50%, -50%) scale(1);
}

/* Heart Animation */
.heart {
    position: absolute;
    color: rgba(255,255,255,0.8);
    font-size: 20px;
    animation: fall linear forwards;
}

@keyframes fall {
    to {
        transform: translateY(100vh);
        opacity: 0;
    }
}

@keyframes fadeIn {
    to {
        opacity: 1;
    }
}

/* Responsive */
@media (max-width: 600px) {
    h1 {
        font-size: 2.2rem;
    }
}
</style>
</head>

<body>

<div class="container">
    <h1>Happy Valentine’s Day ❤️</h1>
    <h2>Untuk Devi Yulianti 💕</h2>
    <button onclick="showMessage()">Klik Aku 💖</button>
</div>

<div class="popup" id="popup">
    Devi Yulianti, kamu adalah alasan senyumku setiap hari ❤️  
    Aku bersyukur memilikimu 💕
</div>

<script>
function showMessage() {
    const popup = document.getElementById("popup");
    popup.classList.add("show");
    setTimeout(() => {
        popup.classList.remove("show");
    }, 4000);
}

function createHeart() {
    const heart = document.createElement("div");
    heart.classList.add("heart");
    heart.innerHTML = "❤️";
    heart.style.left = Math.random() * 100 + "vw";
    heart.style.fontSize = Math.random() * 20 + 15 + "px";
    heart.style.animationDuration = Math.random() * 3 + 2 + "s";
    document.body.appendChild(heart);

    setTimeout(() => {
        heart.remove();
    }, 5000);
}

setInterval(createHeart, 300);
</script>

</body>
</html>
