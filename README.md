# <!DOCTYPE html>
<!DOCTYPE html>
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
    text-align: center;
}

/* Header */
header {
    padding: 40px 20px 20px;
}

h1 {
    font-size: 2.5rem;
    color: #00ffcc;
}

.subtitle {
    margin-top: 10px;
}

/* Cards Layout */
.container {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 20px;
    padding: 20px;
}

/* Card */
.card {
    background: rgba(0,0,0,0.6);
    padding: 20px;
    border-radius: 15px;
    width: 300px;
    max-width: 90%;
    box-shadow: 0 0 15px rgba(0,255,204,0.4);
}

/* Button */
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

/* Status */
.status {
    font-size: 18px;
    margin-top: 10px;
}

/* Footer */
footer {
    margin-top: 20px;
    padding: 20px;
    color: #aaa;
}
</style>
</head>

<body>

<header>
    <h1>HypixelSMP</h1>
    <p class="subtitle">🔥 LifeSteal Minecraft Server 🔥</p>
</header>

<div class="container">

    <!-- Server Status -->
    <div class="card">
        <h2>Server Status</h2>
        <p class="status" id="status">Checking...</p>
        <p id="players"></p>
    </div>

    <!-- IP -->
    <div class="card">
        <h2>Server IP</h2>
        <p id="ip">Hypixelsmp.aternos.me</p>
        <button onclick="copyIP()">Copy IP</button>
    </div>

    <!-- Staff -->
    <div class="card">
        <h2>Server Staff</h2>
        <p><b>Owner:</b> senpmaispider</p>
        <p><b>2nd Owner:</b> deadly_araf_og</p>
        <p><b>SR Admin:</b> prohmas</p>
    </div>

    <!-- Discord -->
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
// Copy IP
function copyIP() {
    const ip = document.getElementById("ip").innerText;
    navigator.clipboard.writeText(ip);
    alert("Copied: " + ip);
}

// Server Status API
fetch("https://api.mcsrvstat.us/2/Hypixelsmp.aternos.me")
.then(res => res.json())
.then(data => {
    if (data.online) {
        document.getElementById("status").innerHTML = "🟢 Online";
        document.getElementById("players").innerHTML =
            "Players: " + data.players.online + "/" + data.players.max;
    } else {
        document.getElementById("status").innerHTML = "🔴 Offline";
    }
})
.catch(() => {
    document.getElementById("status").innerHTML = "Error loading";
});
</script>

</body>
</html>
