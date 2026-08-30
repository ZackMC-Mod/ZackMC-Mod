<!DOCTYPE html>
<html lang="de">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>ZackMC-Mods</title>

<style>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

html {
    scroll-behavior: smooth;
}

body {
    font-family: Arial, Helvetica, sans-serif;
    background: #07080a;
    color: white;
    line-height: 1.6;
}

/* NAVBAR */

.navbar {
    position: sticky;
    top: 0;
    z-index: 1000;

    height: 72px;

    display: flex;
    align-items: center;
    justify-content: space-between;

    padding: 0 6%;

    background: rgba(7, 8, 10, 0.9);
    backdrop-filter: blur(15px);

    border-bottom: 1px solid #292c32;
}

.logo {
    display: flex;
    align-items: center;
    gap: 10px;

    color: white;
    text-decoration: none;

    font-size: 20px;
    font-weight: 900;
}

.logo-box {
    width: 38px;
    height: 38px;

    display: grid;
    place-items: center;

    background: #f2b84b;
    color: #17120a;

    border-radius: 9px;

    font-weight: 900;
    font-size: 21px;
}

.nav-links {
    display: flex;
    gap: 28px;
}

.nav-links a {
    color: #999;
    text-decoration: none;
    font-size: 14px;
    transition: 0.2s;
}

.nav-links a:hover {
    color: white;
}

.nav-download {
    padding: 11px 17px;

    background: #f2b84b;
    color: #17120a;

    border-radius: 10px;

    text-decoration: none;

    font-size: 14px;
    font-weight: 800;

    transition: 0.2s;
}

.nav-download:hover {
    background: #ffda7c;
    transform: translateY(-2px);
}

/* HERO */

.hero {
    max-width: 950px;
    margin: auto;

    text-align: center;

    padding: 110px 24px 70px;
}

.badge {
    color: #f2b84b;

    font-size: 11px;
    font-weight: 900;

    letter-spacing: 0.16em;
}

.hero h1 {
    margin: 22px 0;

    font-size: clamp(50px, 8vw, 90px);

    line-height: 0.95;

    letter-spacing: -0.055em;
}

.hero h1 span {
    color: #f2b84b;
}

.hero p {
    max-width: 680px;
    margin: auto;

    color: #9ca1aa;

    font-size: 18px;
}

.buttons {
    margin-top: 32px;

    display: flex;
    justify-content: center;
    gap: 12px;

    flex-wrap: wrap;
}

.button {
    display: inline-flex;
    align-items: center;
    justify-content: center;

    padding: 14px 21px;

    border-radius: 11px;

    border: 1px solid #303238;

    text-decoration: none;

    color: white;

    font-size: 14px;
    font-weight: 800;

    transition: 0.2s;
}

.primary {
    background: #f2b84b;
    color: #17120a;

    border-color: #f2b84b;
}

.primary:hover {
    background: #ffda7c;
    transform: translateY(-2px);
}

.secondary {
    background: #111318;
}

.secondary:hover {
    background: #1a1c21;
    transform: translateY(-2px);
}

.status {
    margin-top: 18px;

    color: #70757e;

    font-size: 12px;
}

.status span {
    color: #69d391;
}

/* PREVIEW */

.preview {
    max-width: 680px;
    margin: auto;

    padding: 0 24px 90px;
}

.minecraft-card {
    padding: 38px;

    text-align: center;

    border: 1px solid #373a42;

    border-radius: 18px;

    background:
        linear-gradient(
            145deg,
            #191c23,
            #0e1015
        );

    box-shadow:
        0 25px 80px rgba(0,0,0,.6);
}

.minecraft-title {
    color: #888;

    font-size: 12px;
    font-weight: 900;

    letter-spacing: 0.15em;
}

.money {
    margin: 8px 0;

    color: #f2b84b;

    font-size: clamp(45px, 8vw, 70px);

    font-weight: 900;
}

.preview-text {
    color: #70757e;

    font-size: 13px;
}

/* SECTIONS */

section {
    max-width: 1100px;
    margin: auto;

    padding: 85px 24px;
}

.eyebrow {
    color: #f2b84b;

    font-size: 11px;
    font-weight: 900;

    letter-spacing: 0.16em;
}

.section-title {
    margin: 10px 0 35px;

    font-size: 42px;

    line-height: 1.1;

    letter-spacing: -0.04em;
}

/* FEATURES */

.features {
    display: grid;

    grid-template-columns:
        repeat(4, 1fr);

    gap: 15px;
}

.card {
    padding: 27px;

    background: #111318;

    border: 1px solid #292c32;

    border-radius: 16px;

    transition: 0.2s;
}

.card:hover {
    transform: translateY(-5px);

    border-color: #4b3a20;

    box-shadow:
        0 15px 45px rgba(0,0,0,.4);
}

.icon {
    margin-bottom: 18px;

    font-size: 27px;
}

.card h3 {
    margin-bottom: 8px;

    font-size: 18px;
}

.card p {
    color: #999;

    font-size: 14px;
}

code {
    padding: 3px 7px;

    background: #08090b;

    color: #f2b84b;

    border-radius: 6px;

    font-family: monospace;
}

/* COMMANDS */

.commands-section {
    max-width: none;

    background: #0d0f13;

    border-top: 1px solid #292c32;
    border-bottom: 1px solid #292c32;
}

.commands-container {
    max-width: 1100px;
    margin: auto;

    padding: 85px 24px;
}

.commands {
    display: grid;

    gap: 10px;
}

.command {
    display: flex;

    align-items: center;
    justify-content: space-between;

    gap: 20px;

    padding: 18px 20px;

    background: #111318;

    border: 1px solid #292c32;

    border-radius: 12px;
}

.command span {
    color: #888;

    font-size: 13px;
}

/* DOWNLOAD */

.download-box {
    display: flex;

    align-items: center;
    justify-content: space-between;

    gap: 30px;

    padding: 38px;

    border: 1px solid #4b3a20;

    border-radius: 20px;

    background:
        linear-gradient(
            120deg,
            #1b150c,
            #111318
        );

    box-shadow:
        0 20px 60px rgba(0,0,0,.35);
}

.download-box p {
    max-width: 650px;

    margin-top: 8px;

    color: #999;

    font-size: 14px;
}

/* INSTALLATION */

.steps {
    display: grid;

    gap: 12px;

    list-style: none;
}

.step {
    position: relative;

    padding: 20px 20px 20px 65px;

    background: #111318;

    border: 1px solid #292c32;

    border-radius: 14px;

    color: #999;

    font-size: 14px;
}

.step-number {
    position: absolute;

    left: 19px;
    top: 19px;

    width: 30px;
    height: 30px;

    display: grid;
    place-items: center;

    border-radius: 8px;

    background: #211b0e;

    color: #f2b84b;

    font-weight: 900;
}

.step strong {
    color: white;
}

/* NOTICE */

.notice {
    max-width: 1050px;

    margin: 0 auto 75px;

    padding: 20px;

    background: #12100b;

    border: 1px solid #3a3325;

    border-radius: 13px;

    color: #aaa;

    font-size: 13px;
}

.notice strong {
    color: #f2b84b;
}

/* FOOTER */

footer {
    padding: 30px 6%;

    display: flex;

    justify-content: space-between;

    border-top: 1px solid #292c32;

    color: #666;

    font-size: 11px;
}

/* MOBILE */

@media (max-width: 850px) {

    .nav-links {
        display: none;
    }

    .features {
        grid-template-columns: 1fr 1fr;
    }

    .download-box {
        flex-direction: column;

        align-items: flex-start;
    }

    .command {
        flex-direction: column;

        align-items: flex-start;

        gap: 8px;
    }
}

@media (max-width: 520px) {

    .features {
        grid-template-columns: 1fr;
    }

    .hero {
        padding-top: 80px;
    }

    .hero h1 {
        font-size: 48px;
    }

    .section-title {
        font-size: 34px;
    }

    footer {
        flex-direction: column;

        gap: 10px;
    }
}
</style>
</head>

<body>

<!-- NAVIGATION -->

<header class="navbar">

<a href="#" class="logo">

<span class="logo-box">
Z
</span>

ZackMC-Mods

</a>

<nav class="nav-links">

<a href="#features">
Features
</a>

<a href="#commands">
Befehle
</a>

<a href="#download">
Download
</a>

<a href="#install">
Installation
</a>

</nav>

<a
href="#download"
class="nav-download">

Download

</a>

</header>


<!-- HERO -->

<main>

<section class="hero">

<div class="badge">
FABRIC • MINECRAFT JAVA • 1.21.11
</div>

<h1>

ZackMC-Mods.<br>

<span>
Deine Mods.
</span>

</h1>

<p>

Willkommen bei ZackMC-Mods.

Hier findest du Minecraft-Mods
für Fabric, darunter FakeBalance
und FakePayments.

</p>

<div class="buttons">

<a
href="#download"
class="button primary">

↓ Mod herunterladen

</a>

<a
href="#commands"
class="button secondary">

Befehle ansehen

</a>

</div>

<div class="status">

<span>●</span>

Client-only • Keine echten Zahlungen

</div>

</section>


<!-- PREVIEW -->

<div class="preview">

<div class="minecraft-card">

<div class="minecraft-title">

ZACKMC-MODS • FAKEBALANCE

</div>

<div class="money">

$1,000,000

</div>

<div class="preview-text">

Nur lokale Anzeige

</div>

</div>

</div>


<!-- FEATURES -->

<section id="features">

<div class="eyebrow">
FEATURES
</div>

<h2 class="section-title">
Was kann die Mod?
</h2>

<div class="features">

<article class="card">

<div class="icon">
💰
</div>

<h3>
FakeBalance
</h3>

<p>
Setze einen beliebigen Betrag,
der nur lokal angezeigt wird.
</p>

</article>


<article class="card">

<div class="icon">
💸
</div>

<h3>
FakePayments
</h3>

<p>
Simuliere eine Zahlung mit
<code>/pay Name Betrag</code>.
</p>

</article>


<article class="card">

<div class="icon">
👁️
</div>

<h3>
Unauffällig
</h3>

<p>
Keine permanente zusätzliche
Anzeige auf dem Bildschirm.
</p>

</article>


<article class="card">

<div class="icon">
🛡️
</div>

<h3>
Client-only
</h3>

<p>
Kein echtes Guthaben wird
verändert oder übertragen.
</p>

</article>

</div>

</section>


<!-- COMMANDS -->

<section
id="commands"
class="commands-section">

<div class="commands-container">

<div class="eyebrow">
BEFEHLE
</div>

<h2 class="section-title">
Alles über den Chat.
</h2>

<div class="commands">

<div class="command">

<code>
/fakebalance 1000000
</code>

<span>
Fake-Guthaben setzen
</span>

</div>


<div class="command">

<code>
/fakebalance off
</code>

<span>
Fake-Anzeige deaktivieren
</span>

</div>


<div class="command">

<code>
/fakebalance status
</code>

<span>
Status anzeigen
</span>

</div>


<div class="command">

<code>
/fakebalance fakepayments on
</code>

<span>
FakePayments aktivieren
</span>

</div>


<div class="command">

<code>
/pay Max Mustermann 10000
</code>

<span>
Zahlung lokal simulieren
</span>

</div>


<div class="command">

<code>
/fakebalance fakepayments off
</code>

<span>
FakePayments deaktivieren
</span>

</div>

</div>

</div>

</section>


<!-- DOWNLOAD -->

<section id="download">

<div class="download-box">

<div>

<div class="eyebrow">
DOWNLOAD
</div>

<h2
class="section-title"
style="margin-bottom:0">

ZackMC-Mods 1.21.11

</h2>

<p>

Lade hier die aktuelle
ZackMC-Mods-JAR herunter.

</p>

</div>


<!--
WICHTIG:
Diese Datei muss genau so heißen:

ZackMC-Mods-1.21.11.jar

und im gleichen Ordner
wie diese index.html liegen.
-->

<a
href="./ZackMC-Mods-1.21.11.jar"
download="ZackMC-Mods-1.21.11.jar"
class="button primary">

↓ JAR herunterladen

</a>

</div>

</section>


<!-- INSTALLATION -->

<section id="install">

<div class="eyebrow">
INSTALLATION
</div>

<h2 class="section-title">
In 4 Schritten startklar.
</h2>

<ol class="steps">


<li class="step">

<span class="step-number">
1
</span>

<strong>
Fabric installieren
</strong>

<br>

Installiere Fabric für
Minecraft 1.21.11.

</li>


<li class="step">

<span class="step-number">
2
</span>

<strong>
Mod herunterladen
</strong>

<br>

Klicke auf den Download-Button
und lade die JAR herunter.

</li>


<li class="step">

<span class="step-number">
3
</span>

<strong>
JAR verschieben
</strong>

<br>

Verschiebe die Datei in:

<br><br>

<code>
%appdata%\.minecraft\mods
</code>

</li>


<li class="step">

<span class="step-number">
4
</span>

<strong>
Minecraft starten
</strong>

<br>

Starte Minecraft mit deinem
Fabric-Profil.

</li>

</ol>

</section>


<!-- NOTICE -->

<div class="notice">

<strong>
Wichtig:
</strong>

FakeBalance und FakePayments
sind clientseitige Anzeige- und
Simulationsfunktionen.

Es wird kein echtes Guthaben
verändert und kein echtes Geld
übertragen.

Nicht offiziell mit Mojang,
Microsoft oder DonutSMP verbunden.

</div>

</main>


<!-- FOOTER -->

<footer>

<div>
© 2026 ZackMC-Mods
</div>

<div>
Minecraft Java • Fabric • 1.21.11
</div>

</footer>

</body>
</html>
