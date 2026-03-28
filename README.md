<!DOCTYPE html>
<html lang="de">
<head>
    <meta charset="UTF-8">
    <title>Royal CrimeLife | Regeln & Shop</title>
    <link href="https://fonts.googleapis.com/css2?family=Cinzel:wght@700;900&family=Rajdhani:wght@400;700&display=swap" rel="stylesheet">
    <style>
        :root { --gold: #c9a84c; --crimson: #8b0000; --bg: #050507; --card: #0d0d12; --text: #e8e0cc; }
        * { margin: 0; padding: 0; box-sizing: border-box; }
        body { background: var(--bg); color: var(--text); font-family: 'Rajdhani', sans-serif; }
        nav { position: fixed; top: 0; width: 100%; display: flex; justify-content: space-between; align-items: center; padding: 0 5%; height: 80px; background: rgba(5,5,7,0.95); border-bottom: 2px solid var(--gold); z-index: 100; }
        .logo { font-family: 'Cinzel', serif; font-size: 1.5rem; color: var(--gold); text-decoration: none; font-weight: 900; }
        .logo span { color: var(--crimson); }
        .nav-links { display: flex; list-style: none; gap: 20px; }
        .nav-links a { color: #aaa; text-decoration: none; font-weight: 700; text-transform: uppercase; cursor: pointer; }
        .nav-links a:hover, .active { color: var(--gold); }
        .container { max-width: 1000px; margin: 120px auto 50px; padding: 0 20px; }
        .section { display: none; }
        .active-sec { display: block; animation: fadeIn 0.5s ease; }
        .rules-box { background: var(--card); border-left: 4px solid var(--gold); padding: 30px; white-space: pre-wrap; font-size: 1.1rem; }
        .shop-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); gap: 20px; }
        .card { background: var(--card); border: 1px solid rgba(201,168,76,0.2); padding: 30px; text-align: center; }
        .price { font-size: 2rem; color: #fff; margin: 15px 0; font-weight: 700; }
        .btn { background: var(--crimson); color: #fff; border: none; padding: 12px; width: 100%; font-weight: 700; cursor: pointer; text-transform: uppercase; text-decoration: none; display: block; }
        .btn-discord { background: #5865F2; padding: 8px 15px; border-radius: 4px; color: white !important; }
        @keyframes fadeIn { from { opacity: 0; } to { opacity: 1; } }
    </style>
</head>
<body>

<nav>
    <a href="#" class="logo">ROYAL <span>CRIME</span></a>
    <ul class="nav-links">
        <li><a onclick="tab('rules')" id="t-rules" class="active">Regelwerk</a></li>
        <li><a onclick="tab('shop')" id="t-shop">Shop</a></li>
        <li><a href="DEIN_DISCORD_LINK" target="_blank" class="btn-discord">Discord</a></li>
    </ul>
</nav>

<div class="container">
    <div id="rules" class="section active-sec">
        <h1 style="font-family: 'Cinzel'; margin-bottom: 20px; color: var(--gold);">Server-Regelwerk</h1>
        <div class="rules-box">
§1 Allgemeines
Respektvoller Umgang ist Pflicht. Beleidigungen werden nicht geduldet.

§2 RDM & VDM
Töten ohne RP-Hintergrund (RDM) oder Überfahren (VDM) ist verboten.

§3 Combat Logging
Das Verlassen der Situation (Ausloggen) führt zum Ban.

§4 Power-RP
Gib deinem Gegenüber immer eine faire Chance zu reagieren.
        </div>
    </div>

    <div id="shop" class="section">
        <h1 style="font-family: 'Cinzel'; margin-bottom: 20px; color: var(--gold);">Premium Shop</h1>
        <div class="shop-grid">
            <div class="card">
                <h3>Starter Pack</h3>
                <div class="price">10,00€</div>
                <p>50k Geld + Discord Rang</p><br>
                <a href="DEIN_TEBEX_ODER_PAYPAL_LINK" class="btn">Kaufen</a>
            </div>
            <div class="card">
                <h3>VIP Status</h3>
                <div class="price">25,00€</div>
                <p>VIP Auto + Prio-Support</p><br>
                <a href="DEIN_TEBEX_ODER_PAYPAL_LINK" class="btn" style="background:var(--gold); color:black;">Kaufen</a>
            </div>
        </div>
    </div>
</div>

<script>
    function tab(id) {
        document.querySelectorAll('.section').forEach(s => s.classList.remove('active-sec'));
        document.querySelectorAll('.nav-links a').forEach(a => a.classList.remove('active'));
        document.getElementById(id).classList.add('active-sec');
        document.getElementById('t-'+id).classList.add('active');
    }
</script>
</body>
</html>
