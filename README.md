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
      font-family: Arial, Helvetica, sans-serif;
      background: #ffffff;
      color: #1d1d1f;
    }

    /* Navigation */

    nav {
      height: 52px;
      display: flex;
      align-items: center;
      justify-content: space-between;
      max-width: 980px;
      margin: auto;
      padding: 0 22px;
      font-size: 13px;
    }

    .logo {
      font-weight: 600;
      font-size: 16px;
    }

    .nav-links {
      display: flex;
      gap: 28px;
    }

    nav a {
      color: #1d1d1f;
      text-decoration: none;
    }

    /* Shared section design */

    .section {
      min-height: 650px;
      text-align: center;
      padding: 85px 20px;
      margin-bottom: 12px;
    }

    .light {
      background: #f5f5f7;
      color: #1d1d1f;
    }

    .dark {
      background: #000000;
      color: #f5f5f7;
    }

    /* Hero */

    .hero {
      min-height: 700px;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: flex-start;
      padding-top: 110px;
    }

    h1 {
      font-size: 64px;
      line-height: 1.05;
      letter-spacing: -2.5px;
      margin: 0;
      font-weight: 600;
    }

    .tagline {
      font-size: 30px;
      margin: 12px 0 0;
      font-weight: 400;
    }

    .description {
      font-size: 18px;
      color: #86868b;
      margin: 18px 0 0;
    }

    /* Buttons */

    .buttons {
      display: flex;
      justify-content: center;
      gap: 14px;
      margin-top: 28px;
      flex-wrap: wrap;
    }

    .button {
      display: inline-block;
      padding: 12px 22px;
      border-radius: 980px;
      font-size: 17px;
      text-decoration: none;
      background: #0071e3;
      color: white;
      border: 1px solid #0071e3;
      transition: 0.2s;
    }

    .button:hover {
      background: #0077ed;
    }

    .button-outline {
      background: transparent;
      color: #0071e3;
    }

    .button-outline:hover {
      background: #0071e3;
      color: white;
    }

    /* Section headings */

    h2 {
      font-size: 52px;
      letter-spacing: -2px;
      margin: 0;
      font-weight: 600;
    }

    .section-subtitle {
      font-size: 26px;
      margin: 8px 0 45px;
    }

    /* Team */

    .team-container {
      max-width: 700px;
      margin: 50px auto 0;
    }

    .role {
      color: #86868b;
      font-size: 14px;
      margin: 30px 0 10px;
    }

    .names {
      display: flex;
      justify-content: center;
      gap: 12px 28px;
      flex-wrap: wrap;
    }

    .names a {
      color: inherit;
      text-decoration: none;
      font-size: 20px;
    }

    .names a:hover {
      color: #0071e3;
    }

    /* Footer */

    footer {
      max-width: 980px;
      margin: auto;
      padding: 25px 22px 40px;
      color: #86868b;
      font-size: 12px;
    }

    /* Mobile */

    @media (max-width: 600px) {

      nav {
        height: 48px;
      }

      .nav-links {
        gap: 15px;
        font-size: 11px;
      }

      .hero {
        min-height: 610px;
        padding-top: 85px;
      }

      h1 {
        font-size: 48px;
        letter-spacing: -2px;
      }

      .tagline {
        font-size: 25px;
      }

      .description {
        font-size: 16px;
      }

      .section {
        min-height: 580px;
        padding: 70px 18px;
      }

      h2 {
        font-size: 42px;
      }

      .section-subtitle {
        font-size: 22px;
      }

      .names {
        flex-direction: column;
      }
    }
  </style>
</head>

<body>

  <!-- NAVIGATION -->

  <nav>
    <div class="logo">Arch Nemesis</div>

    <div class="nav-links">
      <a href="#team">Team</a>
      <a href="#documentation">Docs</a>
      <a href="#presentation">Presentation</a>
    </div>
  </nav>


  <!-- HERO -->

  <section class="section dark hero">

    <h1>Arch Nemesis</h1>

    <p class="tagline">Software Architecture.</p>

    <p class="description">
      CISC 322 / 326 · Queen's University
    </p>

    <div class="buttons">
      <a href="#team" class="button">Meet the team</a>

      <a href="#documentation"
         class="button button-outline">
        Documentation
      </a>
    </div>

  </section>


  <!-- TEAM -->

  <section class="section light" id="team">

    <h2>The Team</h2>

    <p class="section-subtitle">
      Meet Arch Nemesis.
    </p>

    <div class="team-container">

      <div class="role">TEAM LEAD</div>

      <div class="names">
        <a href="mailto:20ahc1@queensu.ca">
          Ali Haider Cheema
        </a>
      </div>


      <div class="role">PRESENTERS</div>

      <div class="names">

        <a href="mailto:paige.brossard@queensu.ca">
          Paige Brossard
        </a>

        <a href="mailto:23nr52@queensu.ca">
          Sandy Khodak
        </a>

      </div>


      <div class="role">TEAM MEMBERS</div>

      <div class="names">

        <a href="mailto:23hjl2@queensu.ca">
          Kezia Sorensen
        </a>

        <a href="mailto:23dlc4@queensu.ca">
          Sienna Bragg
        </a>

        <a href="mailto:23pfc1@queensu.ca">
          Stephanie Douglas
        </a>

      </div>

    </div>

  </section>


  <!-- DOCUMENTATION -->

  <section class="section dark" id="documentation">

    <h2>Documentation</h2>

    <p class="section-subtitle">
      Our work. All in one place.
    </p>

    <div class="buttons">

      <a href="#" class="button">
        Assignment 1
      </a>

      <a href="#" class="button button-outline">
        Assignment 2
      </a>

      <a href="#" class="button button-outline">
        Assignment 3
      </a>

    </div>

  </section>


  <!-- PRESENTATION -->

  <section class="section light" id="presentation">

    <h2>Presentation</h2>

    <p class="section-subtitle">
      See what we've built.
    </p>

    <div class="buttons">

      <a href="#" class="button">
        View slides
      </a>

      <a href="#" class="button button-outline">
        View script
      </a>

    </div>

  </section>


  <!-- FOOTER -->

  <footer>
    CISC 322 / 326 · Queen's University · Arch Nemesis
  </footer>

</body>
</html>