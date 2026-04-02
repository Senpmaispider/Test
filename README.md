# <!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>HypixelSMP LifeSteal</title>

<style>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: Arial, sans-serif;
}

body {
    background: linear-gradient(135deg, #0f2027, #203a43, #2c5364);
    color: white;
}

/* Header */
header {
    padding: 40px 20px;
    text-align: center;
}

h1 {
    font-size: 2.5rem;
    color: #00ffcc;
}

.subtitle {
    margin-top: 10px;
    font-size: 1.2rem;
}

/* Container */
.container {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 20px;
    padding: 20px;
}

/* Cards */
.card {
    background: rgba(0,0,0,0.6);
    padding: 20px;
    border-radius: 15px;
    width: 300px;
    max-width: 90%;
    text-align: center;
    box-shadow: 0 0 15px rgba(0,255,204,0.4);
    transition: transform 0.3s;
}

.card:hover {
    transform: scale(1.05);
}

/* Buttons */
button {
    background: #00ffcc;
    border: none;
    padding: 12px 18px;
    border-radius: 10px;
    cursor: pointer;
    margin-top: 10px;
    font-weight: bold;
}

button:hover {
    background: #00cc99;
}

/* Footer */
footer {
    text-align: center;
    padding: 20px;
    color: #aaa;
}

/* Mobile */
@media (max-width: 600px) {
    h1 {
        font-size: 2rem;
    }
}
</style>
</head>

<body>

<header>
    <h1>HypixelSMP</h1>
    <p class="subtitle">🔥 LifeSteal Minecraft Server 🔥</p>
</header>

<div class="container">

    <div class="card">
        <h2>Server IP</h2>
        <p id="ip">Hypixelsmp.aternos.me</p>
        <button onclick="copyIP()">Copy IP</button>
    </div>

    <div class="card">
        <h2>Server Staff</h2>
        <p><b>Owner:</b> senpmaispider</p>
        <p><b>2nd Owner:</b> deadly_araf_og</p>
        <p><b>SR Admin:</b> prohmas</p>
    </div>

    <div class="card">
        <h2>Discord</h2>
        <a href="https://discord.gg/R6G7yYpzr" target="_blank">
            <button>Join Server</button>
        </a>
    </div>

</div>

<footer>
    © 2026 HypixelSMP | LifeSteal
</footer>

<script>
function copyIP() {
    const ip = document.getElementById("ip").innerText;
    navigator.clipboard.writeText(ip);
    alert("Copied: " + ip);
}
</script>

</body>
</html>
Test
