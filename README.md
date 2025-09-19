# website
<!doctype html>
<html lang="de">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Meine einfache Webseite</title>
  <style>
    /* Basis Reset */
    * { box-sizing: border-box; margin: 0; padding: 0; }
    :root{
      --max-width: 1100px;
      --accent: #2b6cb0;
      --muted: #6b7280;
      --bg: #f7fafc;
      --card-bg: #ffffff;
    }
    body{
      font-family: Inter, system-ui, Arial, sans-serif;
      background: var(--bg);
      color: #0f172a;
      line-height: 1.5;
      padding: 24px;
      display: flex;
      justify-content: center;
    }
    .container{
      width: 100%;
      max-width: var(--max-width);
    }

    /* Kopfbereich */
    header{
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 16px;
      margin-bottom: 24px;
    }
    .brand{ display: flex; align-items: center; gap: 12px; }
    .logo{
      width: 48px; height: 48px; border-radius: 10px; background: linear-gradient(135deg,var(--accent), #4fd1c5);
      display: flex; align-items: center; justify-content: center; color: white; font-weight: 700;
    }
    nav{ display: flex; gap: 12px; }
    nav a{
      text-decoration: none; padding: 8px 12px; border-radius: 8px; color: var(--muted);
    }
    nav a.primary{ background: var(--accent); color: white; }

    /* Hero */
    .hero{
      background: linear-gradient(180deg, rgba(43,108,176,0.06), transparent);
      padding: 28px; border-radius: 14px; margin-bottom: 20px;
      display: grid; grid-template-columns: 1fr 320px; gap: 20px; align-items: center;
    }
    .hero h1{ font-size: 28px; margin-bottom: 8px; }
    .hero p{ color: var(--muted); }
    .hero .image{
      height: 180px; border-radius: 10px; background: linear-gradient(135deg,#e6f2ff,#ffffff); display: flex; align-items: center; justify-content: center; color: var(--accent); font-weight: 700;
    }

    /* Features */
    .features{ display: grid; grid-template-columns: repeat(auto-fit, minmax(220px, 1fr)); gap: 14px; margin-bottom: 20px; }
    .card{ background: var(--card-bg); padding: 16px; border-radius: 12px; box-shadow: 0 6px 18px rgba(11,28,50,0.06); }
    .card h3{ margin-bottom: 8px; }
    .muted{ color: var(--muted); font-size: 14px; }

    /* Kontakt */
    .contact{ display: grid; grid-template-columns: 1fr 320px; gap: 18px; }
    form{ background: var(--card-bg); padding: 16px; border-radius: 12px; }
    label{ display: block; font-size: 14px; margin-bottom: 6px; }
    input, textarea{ width: 100%; padding: 10px; border-radius: 8px; border: 1px solid #e6e9ef; margin-bottom: 12px; }
    button{ padding: 10px 14px; border-radius: 8px; border: none; background: var(--accent); color: white; cursor: pointer; }

    /* Footer */
    footer{ margin-top: 22px; color: var(--muted); font-size: 14px; text-align: center; }

    /* Responsive */
    @media (max-width: 800px){
      .hero, .contact{ grid-template-columns: 1fr; }
      nav{ display: none; }
    }
  </style>
</head>
<body>
  <div class="container">
    <header>
      <div class="brand">
        <div class="logo">MK</div>
        <div>
          <div style="font-weight:700;">Meine Seite</div>
          <div class="muted" style="font-size:13px;">Einfach. Schnell. Klar.</div>
        </div>
      </div>
      <nav>
        <a href="#features">Funktionen</a>
        <a href="#kontakt">Kontakt</a>
        <a class="primary" href="#">Live ansehen</a>
      </nav>
    </header>

    <main>
      <section class="hero">
        <div>
          <h1>Schlichte Beispielseite</h1>
          <p class="muted">Diese Vorlage zeigt wie du eine einfache Webseite mit HTML und CSS erstellst. Du kannst den Code direkt kopieren und anpassen.</p>
          <p style="margin-top:12px;">Nutze die Bereiche unten um Elemente hinzuzufuegen oder zu loeschen.</p>
        </div>
        <div class="image">Hero Bild</div>
      </section>

      <section id="features" class="features">
        <article class="card">
          <h3>Responsive Layout</h3>
          <p class="muted">Funktioniert auf Desktop und Handy ohne extra Arbeit.</p>
        </article>
        <article class="card">
          <h3>Klare Struktur</h3>
          <p class="muted">Header, Inhalt und Footer sind sauber getrennt und leicht zu verstehen.</p>
        </article>
        <article class="card">
          <h3>Einfache Anpassung</h3>
          <p class="muted">Aendere Farben und Text mit wenigen Zeilen CSS.</p>
        </article>
      </section>

      <section id="kontakt" class="contact">
        <form>
          <h3>Kontaktformular</h3>
          <label for="name">Name</label>
          <input id="name" placeholder="Dein Name" />

          <label for="email">Email</label>
          <input id="email" placeholder="deine@email.de" />

          <label for="message">Nachricht</label>
          <textarea id="message" rows="4" placeholder="Schreibe hier deine Nachricht"></textarea>

          <button type="button">Senden</button>
        </form>
        <div class="card">
          <h3>Kurz info</h3>
          <p class="muted">Du kannst diese Seite lokal testen oder auf GitHub Pages hochladen. Wenn du willst, helfe ich dir beim Hochladen.</p>
        </div>
      </section>
    </main>

    <footer>
      <div>© 2025 Meine Seite</div>
    </footer>
  </div>
</body>
</html>
