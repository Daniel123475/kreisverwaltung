# kreisverwaltungen
<!DOCTYPE html>
<html lang="de">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Kreisverwaltungen Rheinland-Pfalz</title>
  <style>
    body {
      margin: 0;
      font-family: Arial, sans-serif;
      background-color: #f4f4f4;
      color: #333;
    }

    header {
      background-color: #0073e6;
      color: white;
      padding: 30px 20px;
      text-align: center;
    }

    .intro {
      text-align: center;
      padding: 30px 20px;
      max-width: 900px;
      margin: 0 auto;
    }

    .verwaltung-container {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 30px;
      padding: 20px;
    }

    .verwaltung-card {
      background-color: white;
      border-radius: 10px;
      box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
      width: 300px;
      padding: 20px;
      text-align: left;
      transition: transform 0.3s ease;
    }

    .verwaltung-card:hover {
      transform: scale(1.03);
    }

    .verwaltung-card h2 {
      color: #0073e6;
      margin-top: 0;
    }

    .verwaltung-card button,
    .verwaltung-card a {
      display: inline-block;
      margin-top: 10px;
      color: #0073e6;
      font-weight: bold;
      background: none;
      border: none;
      cursor: pointer;
      text-decoration: underline;
    }

    footer {
      text-align: center;
      padding: 20px;
      background-color: #ddd;
      margin-top: 40px;
    }

    .overlay {
      display: none;
      position: fixed;
      top: 0;
      left: 0;
      width: 100vw;
      height: 100vh;
      background-color: rgba(0, 0, 0, 0.5);
      justify-content: center;
      align-items: center;
      z-index: 1000;
    }

    .detail-view {
      background-color: #fff;
      border-radius: 10px;
      padding: 0;
      width: 80%;
      max-width: 700px;
      max-height: 90vh;
      overflow-y: auto;
      box-shadow: 0 4px 20px rgba(0, 0, 0, 0.3);
      position: relative;
    }

    .detail-banner {
      width: 100%;
      height: 200px;
      object-fit: cover;
      border-top-left-radius: 10px;
      border-top-right-radius: 10px;
    }

    .detail-content {
      padding: 20px;
    }

    .close-btn {
      position: absolute;
      top: 10px;
      right: 20px;
      background: none;
      border: none;
      font-size: 20px;
      cursor: pointer;
      color: #0073e6;
    }

    .image-gallery {
      display: flex;
      justify-content: center;
      gap: 30px;
      padding: 60px 20px 40px;
      flex-wrap: wrap;
    }

    .image-gallery div {
      text-align: center;
    }

    .image-gallery img {
      width: 250px;
      height: 150px;
      object-fit: cover;
      border-radius: 8px;
      box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
    }
  </style>
</head>
<body>
  <header>
    <h1>Kreisverwaltungen in Rheinland-Pfalz</h1>
    <p>Ein Vergleich der Aufgaben und Besonderheiten</p>
  </header>

  <section class="intro">
    <p>Hier findest du einen Überblick über die wichtigsten Aufgabenbereiche und Besonderheiten der drei Kreisverwaltungen: Rhein-Hunsrück-Kreis (Simmern), Bad Kreuznach und Birkenfeld. Die Informationen stammen aus offiziellen Quellen und eigener Recherche.</p>
  </section>

  <section class="verwaltung-container">
    <div class="verwaltung-card">
      <h2>Rhein-Hunsrück-Kreis (Simmern)</h2>
      <p><strong>Aufgaben:</strong> Lebensmittelüberwachung, Gesundheitswesen, Katastrophenschutz</p>
      <p><strong>Besonderheiten:</strong> Naturprojekte zur Verbesserung von Lebensräumen</p>
      <button onclick="openDetail('simmern')">Mehr erfahren</button>
      <a href="https://www.kreis-sim.de" target="_blank">Zur Website</a>
    </div>

    <div class="verwaltung-card">
      <h2>Bad Kreuznach</h2>
      <p><strong>Aufgaben:</strong> Ordnung, Sozial- und Jugendhilfe, Bauwesen, Gesundheitsamt, Veterinärwesen, Finanzen</p>
      <p><strong>Besonderheiten:</strong> KFZ-Zulassung, Bauprojekte, Kita-Personal, Abfallentsorgung</p>
      <button onclick="openDetail('kh')">Mehr erfahren</button>
      <a href="https://www.kreis-badkreuznach.de" target="_blank">Zur Website</a>
    </div>

    <div class="verwaltung-card">
      <h2>Landkreis Birkenfeld</h2>
      <p><strong>Aufgaben:</strong> Soziale, wirtschaftliche, gesundheitliche und ökologische Daseinsvorsorge</p>
      <p><strong>Besonderheiten:</strong> Digitale Strategie, starke Umwelt- und Bildungsförderung</p>
      <button onclick="openDetail('birkenfeld')">Mehr erfahren</button>
      <a href="https://www.landkreis-birkenfeld.de" target="_blank">Zur Website</a>
    </div>
  </section>

  <!-- Detail Overlays mit lokalen Bildern -->
  <div id="simmern" class="overlay">
    <div class="detail-view">
      <button class="close-btn" onclick="closeDetail('simmern')">&times;</button>
      <img src="bilder/simmern.jpg" alt="Simmern Banner" class="detail-banner">
      <div class="detail-content">
        <h2>Rhein-Hunsrück-Kreis (Simmern)</h2>
        <ul>
          <li>Gesundheitsamt mit Impfzentrum, Schulärztlicher Dienst</li>
          <li>Trinkwasserkontrolle, Lebensmittelüberwachung</li>
          <li>Katastrophenschutzkoordination</li>
          <li>Großer Fokus auf Natur- und Klimaschutzprojekte</li>
          <li>Umfassender Bürgerservice mit Online-Angeboten</li>
        </ul>
      </div>
    </div>
  </div>

  <div id="kh" class="overlay">
    <div class="detail-view">
      <button class="close-btn" onclick="closeDetail('kh')">&times;</button>
      <img src="bilder/bad_kreuznach.jpg" alt="Bad Kreuznach Banner" class="detail-banner">
      <div class="detail-content">
        <h2>Kreisverwaltung Bad Kreuznach</h2>
        <ul>
          <li>Digitale Antragstellung (z. B. Ausweis, Baugenehmigung)</li>
          <li>Jugendamt mit Schutzkonzepten & Fachberatung</li>
          <li>Breites Serviceangebot mit Bürgertelefon und Infostellen</li>
          <li>Bauabteilung mit Genehmigungsverfahren & Umweltprüfungen</li>
          <li>Veterinärwesen & Lebensmittelüberwachung</li>
        </ul>
      </div>
    </div>
  </div>

  <div id="birkenfeld" class="overlay">
    <div class="detail-view">
      <button class="close-btn" onclick="closeDetail('birkenfeld')">&times;</button>
      <img src="bilder/birkenfeld.jpg" alt="Birkenfeld Banner" class="detail-banner">
      <div class="detail-content">
        <h2>Landkreis Birkenfeld</h2>
        <ul>
          <li>Wirtschaftsförderung & Kooperation mit Umweltcampus</li>
          <li>Digitale Plattform für Förderanträge & Bauanträge</li>
          <li>Koordination von Klimaprojekten</li>
          <li>Starke soziale Ausrichtung (z. B. Kinderbetreuung, Bildungszugang)</li>
          <li>Innovative Smart-City-Projekte in Pilotphasen</li>
        </ul>
      </div>
    </div>
  </div>

  <section class="image-gallery">
    <div>
      <img src="bilder/simmern.jpg" alt="Simmern Bild">
      <p><strong>Rhein-Hunsrück-Kreis (Simmern)</strong></p>
    </div>
    <div>
      <img src="bilder/bad_kreuznach.jpg" alt="Bad Kreuznach Bild">
      <p><strong>Bad Kreuznach</strong></p>
    </div>
    <div>
      <img src="bilder/birkenfeld.jpg" alt="Birkenfeld Bild">
      <p><strong>Landkreis Birkenfeld</strong></p>
    </div>
  </section>

  <footer>
    <p>&copy; Projektarbeit – Vergleich Kreisverwaltungen RLP</p>
  </footer>

  <script>
    function openDetail(id) {
      document.getElementById(id).style.display = "flex";
    }
    function closeDetail(id) {
      document.getElementById(id).style.display = "none";
    }
  </script>
</body>
</html>
