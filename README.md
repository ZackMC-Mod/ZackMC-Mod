<!DOCTYPE html>
<html lang="de">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>ZackMC-Mods | Minecraft Mods</title>

<style>
* {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
}

html {
    scroll-behavior: smooth;
}

body {
    font-family: Arial, Helvetica, sans-serif;
    background:
        radial-gradient(circle at top, #202020 0%, #0b0b0b 45%, #050505 100%);
    color: white;
    min-height: 100vh;
}

a {
    text-decoration: none;
    color: inherit;
}

/* NAVIGATION */

.navbar {
    position: sticky;
    top: 0;
    z-index: 1000;

    height: 72px;
    padding: 0 6%;

    display: flex;
    align-items: center;
    justify-content: space-between;

    background: rgba(5, 5, 5, 0.88);
    backdrop-filter: blur(15px);

    border-bottom: 1px solid #292929;
}

.logo {
    display: flex;
    align-items: center;
    gap: 10px;

    font-size: 21px;
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

    font-size: 21px;
    font-weight: 900;

    box-shadow: 0 0 25px rgba(242,184,75,.25);
}

.nav-links {
    display: flex;
    gap: 28px;

    color: #a6a6a6;
    font-size: 14px;
}

.nav-links a {
    transition: .2s;
}

.nav-links a:hover {
    color: white;
}

.nav-download {
    padding: 11px 17px;

    background: #f2b84b;
    color: #17120a;

    border-radius: 10px;

    font-weight: 800;
    font-size: 14px;

    transition: .2s;
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

    padding: 115px 24px 75px;
}

.badge {
    display: inline-block;

    padding: 7px 13px;

    border: 1px solid #4a3b20;
    border-radius: 999px;

    background: rgba(242,184,75,.07);

    color: #f2b84b;

    font-size: 11px;
    font-weight: 900;

    letter-spacing: .15em;
}

.hero h1 {
    margin: 25px 0 22px;

    font-size: clamp(48px, 8vw, 90px);
    line-height: .95;

    letter-spacing: -.055em;
}

.hero h1 span {
    color: #f2b84b;
}

.hero p {
    max-width: 680px;
    margin: auto;

    color: #a5a5a5;

    font-size: 18px;
    line-height: 1.7;
}

.buttons {
    margin-top: 32px;

    display: flex;
    justify-content: center;
    gap: 12px;

    flex-wrap: wrap;
}

.button {
    padding: 14px 21px;

    border-radius: 11px;

    border: 1px solid #303030;

    font-size: 14px;
    font-weight: 800;

    transition: .2s;
}

.button-primary {
    background: #f2b84b;
    color: #17120a;

    border-color: #f2b84b;
}

.button-primary:hover {
    background: #ffda7c;
    transform: translateY(-2px);
}

.button-secondary {
    background: #111111;
}

.button-secondary:hover {
    background: #1c1c1c;
    transform: translateY(-2px);
}

.status {
    margin-top: 18px;

    color: #777;

    font-size: 12px;
}

.status span {
    color: #6bd38d;
}

/* PREVIEW */

.preview {
    max-width: 700px;
    margin: auto;

    padding: 15px 24px 100px;
}

.minecraft-card {
    padding: 38px;

    text-align: center;

    border: 1px solid #373737;
    border-radius: 18px;

    background:
        linear-gradient(145deg, #1b1b1b, #0c0c0c);

    box-shadow:
        0 25px 80px rgba(0,0,0,.6);
}

.minecraft-title {
    color: #888;

    font-size: 12px;
    font-weight: 900;

    letter-spacing: .15em;
}

.fake-money {
    margin: 10px 0;

    color: #f2b84b;

    font-size: clamp(45px, 8vw, 72px);
    font-weight: 900;
}

.preview-text {
    color: #707070;
    font-size: 13px;
}

/* SECTIONS */

section {
    max-width: 1100px;
    margin: auto;

    padding: 90px 24px;
}

.eyebrow {
    color: #f2b84b;

    font-size: 11px;
    font-weight: 900;

    letter-spacing: .16em;
}

.section-title {
    margin: 10px 0 38px;

    font-size: 42px;

    letter-spacing: -.04em;
}

/* FEATURES */

.feature-grid {
    display: grid;

    grid-template-columns: repeat(4, 1fr);

    gap: 15px;
}

.feature {
    padding: 28px;

    background: #111111;

    border: 1px solid #282828;
    border-radius: 16px;

    transition: .2s;
}

.feature:hover {
    transform: translateY(-5px);

    border-color: #4c3b20;

    box-shadow:
        0 15px 45px rgba(0,0,0,.35);
}

.feature-icon {
    margin-bottom: 20px;

    font-size: 27px;
}

.feature h3 {
    margin-bottom: 9px;

    font-size: 18px;
}

.feature p {
    color: #999;

    font-size: 14px;
    line-height: 1.6;
}

code {
    padding: 3px 7px;

    border-radius: 6px;

    background: #080808;

    color: #f2b84b;

    font-family: monospace;
}

/* COMMANDS */

.commands-section {
    max-width: none;

    background: #0d0d0d;

    border-top: 1px solid #252525;
    border-bottom: 1px solid #252525;
}

.commands-container {
    max-width: 1100px;
    margin: auto;
}

.commands {
    display: grid;
    gap: 10px;
}

.command {
    display: flex;

    justify-content: space-between;
    align-items: center;

    gap: 20px;

    padding: 18px 20px;

    background: #111111;

    border: 1px solid #292929;
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
            #111111
        );

    box-shadow:
        0 20px 60px rgba(0,0,0,.35);
}

.download-box p {
    max-width: 650px;

    margin-top: 8px;

    color: #999;

    font-size: 14px;
    line-height: 1.6;
}

.download-button {
    white-space: nowrap;
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

    background: #111111;

    border: 1px solid #282828;
    border-radius: 14px;

    color: #999;

    font-size: 14px;
    line-height: 1.6;
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
    margin: 0 auto 80px;

    padding: 20px;

    border: 1px solid #3b3325;
    border-radius: 13px;

    background: #12100b;

    color: #aaa;

    font-size: 13px;
    line-height: 1.7;
}

.notice strong {
    color: #f2b84b;
}

/* FOOTER */

footer {
    padding: 30px 6%;

    display: flex;

    justify-content: space-between;

    border-top: 1px solid #252525;

    color: #666;

    font-size: 11px;
}

/* RESPONSIVE */

@media (max-width: 850px) {

    .nav-links {
        display: none;
    }

    .feature-grid {
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

    .hero {
        padding-top: 80px;
    }

    .feature-grid {
        grid-template-columns: 1fr;
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

    <a href="#home" class="logo">
        <span class="logo-box">Z</span>
        ZackMC-Mods
    </a>

    <nav class="nav-links">
        <a href="#features">Features</a>
        <a href="#commands">Befehle</a>
        <a href="#download">Download</a>
        <a href="#install">Installation</a>
    </nav>

    <a href="#download" class="nav-download">
        Download
    </a>

</header>


<!-- HERO -->

<main id="home">

<section class="hero">

    <div class="badge">
        FABRIC • MINECRAFT JAVA • 1.21.11
    </div>

    <h1>
        ZackMC-Mods.<br>
        <span>Deine Mods.</span>
    </h1>

    <p>
        Willkommen bei ZackMC-Mods.
        Hier findest du unsere Minecraft-Mods,
        darunter FakeBalance und FakePayments
        für Fabric.
    </p>

    <div class="buttons">

        <a href="#download"
           class="button button-primary">
            ↓ Mod herunterladen
        </a>

        <a href="#commands"
           class="button button-secondary">
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

        <div class="fake-money">
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

    <div class="feature-grid">

        <article class="feature">

            <div class="feature-icon">
                💰
            </div>

            <h3>
                FakeBalance
            </h3>

            <p>
                Setze einen beliebigen Betrag,
                der nur auf deinem Client angezeigt wird.
            </p>

        </article>


        <article class="feature">

            <div class="feature-icon">
                💸
            </div>

            <h3>
                FakePayments
            </h3>

            <p>
                Simuliere Zahlungen lokal mit
                <code>/pay Name Betrag</code>.
            </p>

        </article>


        <article class="feature">

            <div class="feature-icon">
                👁️
            </div>

            <h3>
                Unauffällig
            </h3>

            <p>
                Die Mod zeigt keine permanente
                zusätzliche Anzeige auf deinem Bildschirm.
            </p>

        </article>


        <article class="feature">

            <div class="feature-icon">
                🛡️
            </div>

            <h3>
                Client-only
            </h3>

            <p>
                Es wird kein echtes Guthaben verändert
                und kein echtes Geld übertragen.
            </p>

        </article>

    </div>

</section>


<!-- COMMANDS -->

<section id="commands"
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

            <h2 class="section-title"
                style="margin-bottom:0;">
                ZackMC-Mods 1.21.11
            </h2>

            <p>
                Lade die aktuelle ZackMC-Mods-JAR
                herunter und installiere sie in deinem
                Fabric-Minecraft.
            </p>

        </div>

        <!--
            WICHTIG:
            Die Datei muss im gleichen Ordner
            wie diese index.html liegen.
        -->

        <a
            href="ZackMC-Mods-1.21.11.jar"
            download
            class="button button-primary download-button">

            ↓ ZackMC-Mods herunterladen

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

            Installiere Fabric für Minecraft
            1.21.11 und starte Minecraft einmal
            mit dem Fabric-Profil.

        </li>


        <li class="step">

            <span class="step-number">
                2
            </span>

            <strong>
                Mod herunterladen
            </strong>

            <br>

            Klicke oben auf den Download-Button
            und lade die ZackMC-Mods-JAR herunter.

        </li>


        <li class="step">

            <span class="step-number">
                3
            </span>

            <strong>
                JAR in den Mods-Ordner
            </strong>

            <br>

            Verschiebe die JAR in:

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

            Starte Minecraft über dein
            Fabric-Profil und benutze anschließend
            die Mod-Befehle im Chat.

        </li>

    </ol>

</section>


<!-- NOTICE -->

<div class="notice">

    <strong>Wichtig:</strong>

    ZackMC-Mods/FakeBalance/FakePayments
    sind clientseitige Anzeige- und
    Simulationsfunktionen.

    Es wird kein echtes Guthaben verändert,
    kein Geld übertragen und keine echte
    Server-Transaktion ausgeführt.

    Die Mod ist kein offizielles Produkt von
    Mojang, Microsoft oder DonutSMP.

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
