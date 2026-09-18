<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Arch Nemesis</title>

  <style>
    * {
      box-sizing: border-box;
    }

    html {
      scroll-behavior: smooth;
    }

    body {
      margin: 0;
      background: #111111;
      color: #f2f2ed;
      font-family: Arial, Helvetica, sans-serif;
    }

    a {
      color: inherit;
      text-decoration: none;
    }

    /* NAV */

    nav {
      height: 72px;
      border-bottom: 1px solid #343434;
      display: flex;
      align-items: center;
      justify-content: space-between;
      padding: 0 5vw;
    }

    .logo {
      font-size: 14px;
      font-weight: bold;
      letter-spacing: 0.08em;
    }

    .course {
      font-family: "Courier New", monospace;
      color: #888;
      font-size: 12px;
      letter-spacing: 0.1em;
    }

    /* HERO */

    .hero {
      min-height: 720px;
      padding: 70px 5vw;
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      border-bottom: 1px solid #343434;
      position: relative;
      overflow: hidden;
    }

    .hero-number {
      font-family: "Courier New", monospace;
      font-size: 12px;
      letter-spacing: 0.15em;
      color: #777;
    }

    .hero-title {
      position: relative;
      z-index: 2;
    }

    .arch {
      display: block;
      font-size: clamp(85px, 17vw, 210px);
      line-height: 0.7;
      font-weight: 700;
      letter-spacing: -0.07em;

      color: transparent;
      -webkit-text-stroke: 1px #555;
    }

    .nemesis {
      display: block;
      font-size: clamp(75px, 16vw, 195px);
      line-height: 0.8;
      font-weight: 700;
      letter-spacing: -0.07em;
      margin-left: 12vw;
    }

    .hero-bottom {
      display: flex;
      justify-content: space-between;
      align-items: end;
      gap: 30px;
    }

    .hero-description {
      max-width: 420px;
      color: #999;
      font-size: 16px;
      line-height: 1.6;
    }

    .explore {
      font-family: "Courier New", monospace;
      font-size: 12px;
      letter-spacing: 0.12em;
      padding-bottom: 5px;
      border-bottom: 1px solid #f2f2ed;
    }

    /* GENERAL SECTIONS */

    .section {
      padding: 90px 5vw;
      border-bottom: 1px solid #343434;
    }

    .section-header {
      display: flex;
      justify-content: space-between;
      align-items: center;
      margin-bottom: 60px;
    }

    .section-number {
      font-family: "Courier New", monospace;
      color: #666;
      font-size: 12px;
    }

    h2 {
      margin: 0;
      font-size: clamp(36px, 6vw, 72px);
      letter-spacing: -0.04em;
      font-weight: 500;
    }

    /* TEAM */

    .team {
      border-top: 1px solid #343434;
    }

    .member {
      min-height: 82px;
      border-bottom: 1px solid #343434;
      display: grid;
      grid-template-columns: 60px 1fr 220px 40px;
      align-items: center;
      transition: 0.25s ease;
    }

    .member:hover {
      background: #f2f2ed;
      color: #111;
      padding-left: 18px;
      padding-right: 18px;
    }

    .member-number {
      font-family: "Courier New", monospace;
      color: #666;
      font-size: 11px;
    }

    .member-name {
      font-size: 22px;
    }

    .member-role {
      font-family: "Courier New", monospace;
      font-size: 11px;
      letter-spacing: 0.12em;
      color: #777;
    }

    .arrow {
      font-size: 20px;
      text-align: right;
    }

    /* DOCUMENTATION */

    .docs {
      background: #e9e7df;
      color: #111;
    }

    .docs .section-number {
      color: #777;
    }

    .doc-list {
      border-top: 1px solid #aaa79e;
    }

    .doc {
      min-height: 110px;
      border-bottom: 1px solid #aaa79e;
      display: flex;
      align-items: center;
      justify-content: space-between;
      transition: 0.25s ease;
    }

    .doc:hover {
      padding-left: 25px;
      padding-right: 25px;
      background: #111;
      color: #f2f2ed;
    }

    .doc-left {
      display: flex;
      align-items: center;
      gap: 40px;
    }

    .doc-number {
      font-family: "Courier New", monospace;
      font-size: 11px;
      color: #777;
    }

    .doc-title {
      font-size: clamp(24px, 4vw, 40px);
      letter-spacing: -0.03em;
    }

    .doc-arrow {
      font-size: 30px;
    }

    /* PRESENTATION */

    .presentation-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      border-top: 1px solid #343434;
    }

    .presentation-card {
      min-height: 260px;
      padding: 35px;
      border-bottom: 1px solid #343434;
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      transition: 0.25s ease;
    }

    .presentation-card:first-child {
      border-right: 1px solid #343434;
    }

    .presentation-card:hover {
      background: #f2f2ed;
      color: #111;
    }

    .card-label {
      font-family: "Courier New", monospace;
      color: #777;
      font-size: 11px;
      letter-spacing: 0.12em;
    }

    .card-bottom {
      display: flex;
      align-items: end;
      justify-content: space-between;
    }

    .card-title {
      font-size: clamp(32px, 5vw, 60px);
      letter-spacing: -0.04em;
    }

    .card-arrow {
      font-size: 35px;
    }

    /* FOOTER */

    footer {
      min-height: 170px;
      padding: 45px 5vw;
      display: flex;
      justify-content: space-between;
      align-items: end;
      color: #777;
      font-family: "Courier New", monospace;
      font-size: 11px;
      letter-spacing: 0.08em;
    }

    /* MOBILE */

    @media (max-width: 700px) {

      nav {
        height: 60px;
      }

      .hero {
        min-height: 620px;
        padding-top: 60px;
      }

      .arch {
        font-size: 25vw;
      }

      .nemesis {
        font-size: 21vw;
        margin-left: 5vw;
        margin-top: 18px;
      }

      .hero-bottom {
        align-items: flex-start;
        flex-direction: column;
      }

      .section {
        padding-top: 65px;
        padding-bottom: 65px;
      }

      .section-header {
        margin-bottom: 40px;
      }

      .member {
        grid-template-columns: 35px 1fr 30px;
        min-height: 90px;
      }

      .member-role {
        grid-column: 2;
        margin-top: -25px;
      }

      .presentation-grid {
        grid-template-columns: 1fr;
      }

      .presentation-card:first-child {
        border-right: none;
      }

      footer {
        flex-direction: column;
        align-items: flex-start;
        gap: 15px;
      }
    }
  </style>
</head>

<body>

  <!-- NAVIGATION -->

  <nav>
    <div class="logo">ARCH NEMESIS</div>
    <div class="course">CISC 322 / 326</div>
  </nav>


  <!-- HERO -->

  <section class="hero">

    <div class="hero-number">
      SOFTWARE ARCHITECTURE / 2026
    </div>

    <div class="hero-title">
      <span class="arch">ARCH</span>
      <span class="nemesis">NEMESIS</span>
    </div>

    <div class="hero-bottom">

      <div class="hero-description">
        A software architecture project group at
        Queen's University. Designing, documenting,
        and understanding software systems.
      </div>

      <a class="explore" href="#team">
        EXPLORE PROJECT ↓
      </a>

    </div>

  </section>


  <!-- TEAM -->

  <section class="section" id="team">

    <div class="section-header">
      <h2>The Team</h2>
      <div class="section-number">01 / 03</div>
    </div>

    <div class="team">

      <a class="member" href="mailto:20ahc1@queensu.ca">
        <span class="member-number">01</span>
        <span class="member-name">Ali Haider Cheema</span>
        <span class="member-role">TEAM LEAD</span>
        <span class="arrow">↗</span>
      </a>

      <a class="member" href="mailto:paige.brossard@queensu.ca">
        <span class="member-number">02</span>
        <span class="member-name">Paige Brossard</span>
        <span class="member-role">PRESENTER</span>
        <span class="arrow">↗</span>
      </a>

      <a class="member" href="mailto:23nr52@queensu.ca">
        <span class="member-number">03</span>
        <span class="member-name">Sandy Khodak</span>
        <span class="member-role">PRESENTER</span>
        <span class="arrow">↗</span>
      </a>

      <a class="member" href="mailto:23hjl2@queensu.ca">
        <span class="member-number">04</span>
        <span class="member-name">Kezia Sorensen</span>
        <span class="member-role">TEAM MEMBER</span>
        <span class="arrow">↗</span>
      </a>

      <a class="member" href="mailto:23dlc4@queensu.ca">
        <span class="member-number">05</span>
        <span class="member-name">Sienna Bragg</span>
        <span class="member-role">TEAM MEMBER</span>
        <span class="arrow">↗</span>
      </a>

      <a class="member" href="mailto:23pfc1@queensu.ca">
        <span class="member-number">06</span>
        <span class="member-name">Stephanie Douglas</span>
        <span class="member-role">TEAM MEMBER</span>
        <span class="arrow">↗</span>
      </a>

    </div>

  </section>


  <!-- DOCUMENTATION -->

  <section class="section docs">

    <div class="section-header">
      <h2>Project Files</h2>
      <div class="section-number">02 / 03</div>
    </div>

    <div class="doc-list">

      <a href="#" class="doc">
        <div class="doc-left">
          <span class="doc-number">001</span>
          <span class="doc-title">Assignment 01</span>
        </div>
        <span class="doc-arrow">↗</span>
      </a>

      <a href="#" class="doc">
        <div class="doc-left">
          <span class="doc-number">002</span>
          <span class="doc-title">Assignment 02</span>
        </div>
        <span class="doc-arrow">↗</span>
      </a>

      <a href="#" class="doc">
        <div class="doc-left">
          <span class="doc-number">003</span>
          <span class="doc-title">Assignment 03</span>
        </div>
        <span class="doc-arrow">↗</span>
      </a>

    </div>

  </section>


  <!-- PRESENTATION -->

  <section class="section">

    <div class="section-header">
      <h2>Presentation</h2>
      <div class="section-number">03 / 03</div>
    </div>

    <div class="presentation-grid">

      <a href="#" class="presentation-card">

        <span class="card-label">
          PRESENTATION / 01
        </span>

        <div class="card-bottom">
          <span class="card-title">Slides</span>
          <span class="card-arrow">↗</span>
        </div>

      </a>


      <a href="#" class="presentation-card">

        <span class="card-label">
          PRESENTATION / 02
        </span>

        <div class="card-bottom">
          <span class="card-title">Script</span>
          <span class="card-arrow">↗</span>
        </div>

      </a>

    </div>

  </section>


  <!-- FOOTER -->

  <footer>

    <span>ARCH NEMESIS © 2026</span>

    <span>
      CISC 322 / 326 · QUEEN'S UNIVERSITY
    </span>

  </footer>

</body>
</html>
