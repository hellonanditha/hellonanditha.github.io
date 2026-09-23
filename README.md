<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>The Beauty Files — Nanditha V.</title>

<style>
@import url('https://fonts.googleapis.com/css2?family=Cormorant+Garamond:wght@400;500;600&family=DM+Mono:wght@300;400;500&display=swap');

:root {
  --black: #080708;
  --deep: #10090c;
  --wine: #3d111d;
  --burgundy: #641b2c;
  --red: #8e3047;
  --cream: #eee5df;
  --muted: #a89b9d;
  --line: rgba(238,229,223,.18);
}

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

html {
  scroll-behavior: smooth;
}

body {
  background: var(--black);
  color: var(--cream);
  font-family: "DM Mono", monospace;
  overflow-x: hidden;
}

/* subtle film texture */
body::before {
  content: "";
  position: fixed;
  inset: 0;
  pointer-events: none;
  opacity: .045;
  z-index: 100;
  background-image:
    repeating-linear-gradient(
      0deg,
      transparent,
      transparent 2px,
      rgba(255,255,255,.18) 3px
    );
}

/* NAVIGATION */

nav {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  padding: 22px 5vw;
  display: flex;
  justify-content: space-between;
  align-items: center;
  z-index: 50;
  background: linear-gradient(
    to bottom,
    rgba(8,7,8,.95),
    transparent
  );
}

.nav-logo {
  font-size: 10px;
  letter-spacing: .25em;
}

.nav-links {
  display: flex;
  gap: 28px;
}

.nav-links a {
  color: var(--cream);
  text-decoration: none;
  font-size: 9px;
  letter-spacing: .16em;
  opacity: .7;
  transition: .3s;
}

.nav-links a:hover {
  opacity: 1;
  color: #c86b82;
}

/* GENERAL */

section {
  position: relative;
  min-height: 100vh;
  padding: 130px 7vw;
}

.label {
  font-size: 9px;
  letter-spacing: .28em;
  color: #b65b72;
  text-transform: uppercase;
}

.small {
  font-size: 9px;
  line-height: 1.9;
  color: var(--muted);
}

h1, h2, h3 {
  font-family: "Cormorant Garamond", serif;
  font-weight: 400;
}

/* COVER */

.hero {
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  background:
    radial-gradient(
      circle at 75% 50%,
      rgba(100,27,44,.30),
      transparent 35%
    ),
    var(--black);
}

.hero::after {
  content: "";
  position: absolute;
  right: 8vw;
  top: 20%;
  width: 1px;
  height: 60%;
  background: linear-gradient(
    transparent,
    var(--burgundy),
    transparent
  );
}

.hero-top {
  margin-bottom: 50px;
}

.hero h1 {
  font-size: clamp(70px, 13vw, 190px);
  line-height: .78;
  letter-spacing: -.04em;
  max-width: 1000px;
}

.hero h1 span {
  display: block;
  color: #713044;
}

.hero-meta {
  margin-top: 55px;
  display: flex;
  gap: 35px;
  flex-wrap: wrap;
}

.case-open {
  margin-top: 65px;
  display: inline-flex;
  align-items: center;
  gap: 14px;
  color: var(--cream);
  text-decoration: none;
  font-size: 10px;
  letter-spacing: .18em;
}

.case-open::before {
  content: "→";
  color: #b65b72;
}

/* CASE NOTES */

.notes {
  background:
    linear-gradient(
      120deg,
      var(--deep),
      #160b0f 50%,
      var(--black)
    );
}

.notes-inner {
  max-width: 850px;
}

.notes h2 {
  font-size: clamp(55px, 8vw, 110px);
  margin: 35px 0 55px;
}

.notes-copy {
  font-family: "Cormorant Garamond", serif;
  font-size: clamp(25px, 3vw, 42px);
  line-height: 1.2;
  max-width: 800px;
}

.notes-bottom {
  margin-top: 80px;
  border-top: 1px solid var(--line);
  padding-top: 25px;
  display: flex;
  gap: 70px;
  flex-wrap: wrap;
}

/* INVESTIGATOR */

.investigator {
  background: var(--black);
}

.investigator-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  min-height: 70vh;
  gap: 8vw;
  align-items: center;
}

.investigator h2 {
  font-size: clamp(70px, 10vw, 140px);
  line-height: .8;
  margin: 25px 0 40px;
}

.investigator-name {
  color: #9a4058;
}

.investigator-copy {
  font-family: "Cormorant Garamond", serif;
  font-size: 27px;
  line-height: 1.3;
  max-width: 500px;
}

.portrait-box {
  height: 560px;
  border: 1px solid var(--line);
  background:
    linear-gradient(
      135deg,
      transparent 30%,
      rgba(100,27,44,.35)
    ),
    #0d090b;
  display: flex;
  align-items: flex-end;
  padding: 25px;
}

/* SPECIALIZATIONS */

.specializations {
  background: #11090c;
}

.spec-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 7vw;
  margin-top: 70px;
}

.spec-list {
  border-top: 1px solid var(--line);
}

.spec-item {
  padding: 22px 0;
  border-bottom: 1px solid var(--line);
  display: flex;
  justify-content: space-between;
  font-size: 11px;
  letter-spacing: .08em;
}

.spec-item span {
  color: #9a4058;
}

/* CASE HISTORY */

.history {
  background:
    linear-gradient(
      150deg,
      #080708,
      #210d13,
      #080708
    );
}

.history-card {
  max-width: 950px;
  margin-top: 70px;
  border: 1px solid var(--line);
  padding: 45px;
  background: rgba(255,255,255,.015);
}

.history-card h3 {
  font-size: 42px;
  margin-bottom: 25px;
}

.history-card p {
  font-family: "Cormorant Garamond", serif;
  font-size: 25px;
  line-height: 1.35;
}

.history-meta {
  margin-top: 45px;
  display: flex;
  flex-wrap: wrap;
  gap: 20px;
}

.tag {
  border: 1px solid var(--line);
  padding: 10px 14px;
  font-size: 8px;
  letter-spacing: .15em;
}

/* ACTIVE CASES */

.cases {
  background: var(--black);
}

.case-index {
  margin-top: 70px;
}

.case-row {
  position: relative;
  display: grid;
  grid-template-columns: 100px 1fr auto;
  align-items: center;
  gap: 30px;
  padding: 35px 0;
  border-top: 1px solid var(--line);
  text-decoration: none;
  color: var(--cream);
  transition: .4s;
}

.case-row:last-child {
  border-bottom: 1px solid var(--line);
}

.case-row:hover {
  padding-left: 20px;
  background: linear-gradient(
    90deg,
    rgba(100,27,44,.2),
    transparent
  );
}

.case-number {
  color: #a44861;
  font-size: 11px;
}

.case-title {
  font-family: "Cormorant Garamond", serif;
  font-size: clamp(38px, 6vw, 75px);
}

.case-sub {
  font-size: 8px;
  letter-spacing: .15em;
  color: var(--muted);
}

.arrow {
  font-size: 20px;
  color: #a44861;
}

/* CASE DETAIL */

.case-detail {
  background:
    radial-gradient(
      circle at 80% 20%,
      rgba(100,27,44,.22),
      transparent 35%
    ),
    var(--black);
}

.case-heading {
  display: flex;
  justify-content: space-between;
  align-items: flex-end;
  gap: 30px;
  margin-bottom: 80px;
}

.case-heading h2 {
  font-size: clamp(70px, 11vw, 150px);
  line-height: .75;
}

.objective {
  max-width: 300px;
  font-size: 9px;
  line-height: 1.8;
}

/* EVIDENCE */

.evidence-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 70px 35px;
}

.evidence {
  min-width: 0;
}

.evidence-number {
  font-size: 8px;
  color: #b65b72;
  letter-spacing: .18em;
  margin-bottom: 15px;
}

.evidence h3 {
  font-size: 38px;
  margin-bottom: 20px;
}

.video-placeholder {
  aspect-ratio: 16 / 10;
  border: 1px solid var(--line);
  background:
    linear-gradient(
      135deg,
      #10090c,
      #2a0e17
    );
  display: flex;
  align-items: center;
  justify-content: center;
  color: #8e5966;
  font-size: 8px;
  letter-spacing: .18em;
}

/* PRODUCT FILE */

.product {
  background:
    linear-gradient(
      135deg,
      #090708,
      #1d0b11
    );
}

.product-intro {
  max-width: 700px;
  margin-bottom: 70px;
}

.product-intro h2 {
  font-size: clamp(65px, 10vw, 135px);
  line-height: .75;
  margin: 25px 0;
}

.product-intro p {
  font-family: "Cormorant Garamond", serif;
  font-size: 25px;
}

/* CREATOR FILE */

.creator {
  background: var(--black);
}

.workflow {
  max-width: 1000px;
  margin-top: 65px;
}

.workflow-row {
  display: grid;
  grid-template-columns: 70px 180px 1fr;
  gap: 25px;
  padding: 28px 0;
  border-top: 1px solid var(--line);
}

.workflow-row:last-child {
  border-bottom: 1px solid var(--line);
}

.workflow-num {
  color: #a44861;
}

.workflow-title {
  font-family: "Cormorant Garamond", serif;
  font-size: 27px;
}

.workflow-desc {
  color: var(--muted);
  font-size: 9px;
  line-height: 1.8;
}

/* TRANSFORMATION */

.transformation {
  background:
    linear-gradient(
      180deg,
      #080708,
      #230d14,
      #080708
    );
}

.transform-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 25px;
  margin-top: 60px;
}

.transform-box {
  aspect-ratio: 16 / 10;
  border: 1px solid var(--line);
  background: #10090c;
  display: flex;
  align-items: center;
  justify-content: center;
}

.transform-label {
  margin-top: 15px;
  font-size: 9px;
  letter-spacing: .15em;
}

.changes {
  margin-top: 70px;
  display: flex;
  gap: 12px;
  flex-wrap: wrap;
}

/* HOW WE WORK */

.work {
  background: #10090c;
}

.work-steps {
  max-width: 950px;
  margin-top: 60px;
}

.work-step {
  display: grid;
  grid-template-columns: 70px 200px 1fr;
  gap: 25px;
  padding: 30px 0;
  border-top: 1px solid var(--line);
}

.work-step:last-child {
  border-bottom: 1px solid var(--line);
}

.work-step-number {
  color: #a44861;
}

.work-step-title {
  font-family: "Cormorant Garamond", serif;
  font-size: 28px;
}

.work-step-text {
  color: var(--muted);
  font-size: 9px;
  line-height: 1.8;
}

/* CONTACT */

.contact {
  min-height: 90vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  background:
    radial-gradient(
      circle at 50% 50%,
      rgba(100,27,44,.3),
      transparent 45%
    ),
    var(--black);
}

.contact h2 {
  font-size: clamp(70px, 12vw, 170px);
  line-height: .75;
  max-width: 900px;
}

.contact-copy {
  margin: 50px 0;
  font-family: "Cormorant Garamond", serif;
  font-size: 27px;
}

.contact-links {
  display: flex;
  gap: 30px;
  flex-wrap: wrap;
}

.contact-links a {
  color: var(--cream);
  text-decoration: none;
  border-bottom: 1px solid #8e3047;
  padding-bottom: 8px;
  font-size: 9px;
  letter-spacing: .15em;
}

.rate-card {
  margin-top: 50px;
}

.rate-card a {
  display: inline-block;
  border: 1px solid #8e3047;
  padding: 15px 22px;
  color: var(--cream);
  text-decoration: none;
  font-size: 9px;
  letter-spacing: .15em;
  transition: .3s;
}

.rate-card a:hover {
  background: #641b2c;
}

/* FOOTER */

footer {
  min-height: 45vh;
  padding: 100px 7vw;
  background: #070607;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}

.footer-title {
  font-family: "Cormorant Garamond", serif;
  font-size: clamp(45px, 8vw, 100px);
}

.footer-status {
  font-size: 9px;
  letter-spacing: .2em;
  color: #a44861;
}

/* MOBILE */

@media (max-width: 700px) {

  nav {
    padding: 18px 5vw;
  }

  .nav-links {
    gap: 12px;
  }

  .nav-links a {
    font-size: 7px;
  }

  section {
    padding: 105px 6vw;
  }

  .hero {
    min-height: 100svh;
  }

  .hero h1 {
    font-size: 20vw;
  }

  .hero-meta {
    gap: 15px;
    flex-direction: column;
  }

  .hero::after {
    display: none;
  }

  .investigator-grid,
  .spec-grid,
  .evidence-grid,
  .transform-grid {
    grid-template-columns: 1fr;
  }

  .portrait-box {
    height: 400px;
  }

  .case-row {
    grid-template-columns: 45px 1fr 20px;
    gap: 12px;
  }

  .case-title {
    font-size: 39px;
  }

  .case-heading {
    display: block;
  }

  .case-heading h2 {
    margin-bottom: 35px;
  }

  .workflow-row,
  .work-step {
    grid-template-columns: 45px 1fr;
    gap: 12px;
  }

  .workflow-desc,
  .work-step-text {
    grid-column: 2;
  }

  .workflow-title,
  .work-step-title {
    font-size: 25px;
  }

  .history-card {
    padding: 25px;
  }

  .history-card h3 {
    font-size: 34px;
  }

  .history-card p {
    font-size: 22px;
  }

  .contact h2 {
    font-size: 19vw;
  }

  .contact-copy {
    font-size: 23px;
  }

  .footer-title {
    font-size: 15vw;
  }
}
</style>
</head>

<body>

<nav>
  <div class="nav-logo">THE BEAUTY FILES</div>

  <div class="nav-links">
    <a href="#cases">CASES</a>
    <a href="#contact">CONTACT</a>
  </div>
</nav>


<!-- COVER -->

<section class="hero" id="top">

  <div class="hero-top label">
    CONFIDENTIAL / VISUAL CONTENT INVESTIGATION UNIT
  </div>

  <h1>
    THE
    <span>BEAUTY</span>
    FILES
  </h1>

  <div class="hero-meta">
    <div class="small">NANDITHA V.</div>
    <div class="small">22 YEARS OLD</div>
    <div class="small">VIDEO EDITOR • UGC CREATOR</div>
  </div>

  <div class="small" style="margin-top:20px;">
    BEAUTY • LIFESTYLE • SELF-CARE
  </div>

  <a class="case-open" href="#notes">
    OPEN THE FILE
  </a>

</section>


<!-- CASE NOTES -->

<section class="notes" id="notes">

  <div class="notes-inner">

    <div class="label">CASE NOTES</div>

    <h2>THE CASE</h2>

    <p class="notes-copy">
      Beauty content is everywhere. But why do some videos make you stop
      scrolling while others disappear in seconds?
      <br><br>
      That's the case I'm interested in.
    </p>

    <p class="notes-copy" style="margin-top:35px;">
      I turn ideas, raw footage and content concepts into visual stories
      designed to capture attention, communicate the subject and keep the
      viewer watching.
    </p>

    <div class="notes-bottom">

      <div>
        <div class="label">SPECIALIZATION</div>
        <div class="small" style="margin-top:12px;">
          BEAUTY • LIFESTYLE • SELF-CARE<br>
          UGC • CREATOR CONTENT
        </div>
      </div>

      <div>
        <div class="label">CASE OBJECTIVE</div>
        <div class="small" style="margin-top:12px;">
          FROM THE FIRST IDEA TO THE FINAL CUT —
          DEVELOPING, CREATING AND SHAPING CONTENT
          MADE TO BE WATCHED.
        </div>
      </div>

    </div>

  </div>

</section>


<!-- INVESTIGATOR -->

<section class="investigator">

  <div class="investigator-grid">

    <div>

      <div class="label">PERSON OF INTEREST</div>

      <h2>
        THE<br>
        <span class="investigator-name">INVESTIGATOR</span>
      </h2>

      <div class="small" style="margin-bottom:25px;">
        NANDITHA V. / 22 YEARS OLD
      </div>

      <p class="investigator-copy">
        Strong hooks. Intentional pacing. Visual storytelling.
        Aesthetic visuals, sound design, captions and clean editing —
        with an eye for the content idea behind every piece.
      </p>

    </div>

    <div class="portrait-box">

      <div>
        <div class="label">SUBJECT FILE</div>
        <div class="small" style="margin-top:10px;">
          VIDEO EDITOR • UGC CREATOR
        </div>
      </div>

    </div>

  </div>

</section>


<!-- SPECIALIZATIONS -->

<section class="specializations">

  <div class="label">EDITOR'S KIT</div>

  <h2 style="font-size:clamp(65px,10vw,130px); margin-top:25px;">
    SPECIALIZATIONS
  </h2>

  <div class="spec-grid">

    <div>

      <div class="label" style="margin-bottom:20px;">
        SPECIALIZATIONS
      </div>

      <div class="spec-list">
        <div class="spec-item">BEAUTY <span>01</span></div>
        <div class="spec-item">LIFESTYLE <span>02</span></div>
        <div class="spec-item">SELF-CARE <span>03</span></div>
        <div class="spec-item">UGC <span>04</span></div>
        <div class="spec-item">CREATOR CONTENT <span>05</span></div>
      </div>

    </div>

    <div>

      <div class="label" style="margin-bottom:20px;">
        TOOLS & KNOWLEDGE
      </div>

      <div class="spec-list">
        <div class="spec-item">VIDEO EDITING <span>+</span></div>
        <div class="spec-item">CONTENT CREATION <span>+</span></div>
        <div class="spec-item">STORYTELLING <span>+</span></div>
        <div class="spec-item">SCRIPTING <span>+</span></div>
        <div class="spec-item">SOCIAL CONTENT <span>+</span></div>
      </div>

    </div>

  </div>

</section>


<!-- CASE HISTORY -->

<section class="history">

  <div class="label">CASE HISTORY</div>

  <div class="history-card">

    <div class="label">CURRENT CASE</div>

    <h3>TANYA CHAWLA / @thatDELHIGIRL</h3>

    <div class="small">
      UGC CREATOR • BEAUTY • LIFESTYLE
    </div>

    <p style="margin-top:30px;">
      Currently managing Instagram content from concept and creation
      through editing and publishing.
      <br><br>
      YouTube content management begins next month.
    </p>

    <div class="history-meta">
      <div class="tag">BEAUTY</div>
      <div class="tag">MAKEUP TUTORIALS</div>
      <div class="tag">SELF-CARE</div>
      <div class="tag">HAIR CARE</div>
      <div class="tag">WELLNESS</div>
    </div>

  </div>

</section>


<!-- ACTIVE CASES -->

<section class="cases" id="cases">

  <div class="label">ARCHIVE INDEX</div>

  <h2 style="font-size:clamp(65px,10vw,135px); margin-top:25px;">
    ACTIVE CASES
  </h2>

  <div class="case-index">

    <a href="#beauty" class="case-row">
      <div class="case-number">001</div>
      <div>
        <div class="case-title">THE BEAUTY FILE</div>
        <div class="case-sub">
          BEAUTY • SELF-CARE • FASHION + LIFESTYLE
        </div>
      </div>
      <div class="arrow">→</div>
    </a>

    <a href="#product" class="case-row">
      <div class="case-number">002</div>
      <div>
        <div class="case-title">THE PRODUCT FILE</div>
        <div class="case-sub">
          UGC CREATION
        </div>
      </div>
      <div class="arrow">→</div>
    </a>

    <a href="#creator" class="case-row">
      <div class="case-number">003</div>
      <div>
        <div class="case-title">THE CREATOR FILE</div>
        <div class="case-sub">
          YOUTUBE • LONG-FORM VIDEO
        </div>
      </div>
      <div class="arrow">→</div>
    </a>

  </div>

</section>


<!-- CASE 001 -->

<section class="case-detail" id="beauty">

  <div class="case-heading">

    <div>
      <div class="label">CASE 001</div>

      <h2>
        THE<br>
        BEAUTY<br>
        FILE
      </h2>
    </div>

    <div class="objective">
      <div class="label">OBJECTIVE</div>
      <br>
      MAKE THE VIEWER STOP SCROLLING.
    </div>

  </div>

  <div class="evidence-grid">

    <div class="evidence">
      <div class="evidence-number">EVIDENCE 001</div>
      <h3>SKINCARE</h3>
      <div class="video-placeholder">VIDEO / ADD YOUR WORK HERE</div>
    </div>

    <div class="evidence">
      <div class="evidence-number">EVIDENCE 002</div>
      <h3>HAIRCARE</h3>
      <div class="video-placeholder">VIDEO / ADD YOUR WORK HERE</div>
    </div>

    <div class="evidence">
      <div class="evidence-number">EVIDENCE 003</div>
      <h3>BODY CARE</h3>
      <div class="video-placeholder">VIDEO / ADD YOUR WORK HERE</div>
    </div>

    <div class="evidence">
      <div class="evidence-number">EVIDENCE 004</div>
      <h3>MAKEUP / GRWM</h3>
      <div class="video-placeholder">VIDEO / ADD YOUR WORK HERE</div>
    </div>

    <div class="evidence">
      <div class="evidence-number">EVIDENCE 005</div>
      <h3>LIFESTYLE</h3>
      <div class="video-placeholder">VIDEO / ADD YOUR WORK HERE</div>
    </div>

  </div>

</section>


<!-- CASE 002 -->

<section class="case-detail product" id="product">

  <div class="product-intro">

    <div class="label">CASE 002 / THE PRODUCT FILE</div>

    <h2>UGC<br>CREATION</h2>

    <p>
      Product-focused content built to show the product,
      communicate the experience and keep the viewer engaged.
    </p>

  </div>

  <div class="evidence-grid">

    <div class="evidence">
      <div class="evidence-number">01</div>
      <h3>PRODUCT HAUL</h3>
      <div class="video-placeholder">VIDEO / ADD YOUR WORK HERE</div>
    </div>

    <div class="evidence">
      <div class="evidence-number">02</div>
      <h3>PRODUCT TEXTURE / EXPERIENCE</h3>
      <div class="video-placeholder">VIDEO / ADD YOUR WORK HERE</div>
    </div>

    <div class="evidence">
      <div class="evidence-number">03</div>
      <h3>VOICEOVER PRODUCT VIDEO</h3>
      <div class="video-placeholder">VIDEO / ADD YOUR WORK HERE</div>
    </div>

    <div class="evidence">
      <div class="evidence-number">04</div>
      <h3>TALKING / ON-CAMERA UGC</h3>
      <div class="video-placeholder">VID
