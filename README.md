<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>South Florida Bulls Baseball</title>
<meta name="description" content="South Florida Bulls Baseball - a premier youth and travel baseball organization in South Florida. Tournament champions, dedicated coaching, and a home for young ballplayers.">
<link rel="icon" href="assets/logo.png">
<style>
  :root{
    --black:#0b0b0c;
    --charcoal:#141416;
    --gold:#c9a24b;
    --gold-light:#e2c887;
    --white:#f7f6f3;
    --gray:#9a9a9e;
  }
  *{box-sizing:border-box;margin:0;padding:0;}
  html{scroll-behavior:smooth;}
  body{
    font-family:'Helvetica Neue', Arial, sans-serif;
    background:var(--black);
    color:var(--white);
    line-height:1.6;
  }
  img{max-width:100%;display:block;}
  a{color:inherit;text-decoration:none;}
  .container{max-width:1180px;margin:0 auto;padding:0 24px;}
  h1,h2,h3{font-family:'Helvetica Neue', Arial, sans-serif;letter-spacing:.5px;}
  .eyebrow{
    text-transform:uppercase;
    letter-spacing:3px;
    font-size:13px;
    color:var(--gold);
    font-weight:700;
    margin-bottom:10px;
  }
  .section-title{
    font-size:clamp(28px,4vw,42px);
    font-weight:800;
    text-transform:uppercase;
    margin-bottom:18px;
  }
  .btn{
    display:inline-block;
    padding:14px 30px;
    border-radius:2px;
    font-weight:700;
    text-transform:uppercase;
    letter-spacing:1.5px;
    font-size:13px;
    transition:all .2s ease;
    border:2px solid var(--gold);
  }
  .btn-primary{background:var(--gold);color:var(--black);}
  .btn-primary:hover{background:var(--gold-light);border-color:var(--gold-light);}
  .btn-outline{background:transparent;color:var(--white);}
  .btn-outline:hover{background:var(--gold);color:var(--black);border-color:var(--gold);}

  /* Top bar */
  .topbar{
    background:var(--gold);
    color:var(--black);
    font-size:12px;
    font-weight:700;
    letter-spacing:1px;
    text-align:center;
    padding:8px 16px;
    text-transform:uppercase;
  }

  /* Header */
  header{
    position:sticky;top:0;z-index:100;
    background:rgba(11,11,12,.96);
    border-bottom:1px solid rgba(201,162,75,.25);
    backdrop-filter:blur(6px);
  }
  .nav-wrap{
    display:flex;align-items:center;justify-content:space-between;
    padding:12px 0;
  }
  .brand{display:flex;align-items:center;gap:12px;}
  .brand img{height:52px;width:auto;}
  .brand-text{font-weight:800;letter-spacing:1px;font-size:15px;text-transform:uppercase;}
  .brand-text span{display:block;font-size:11px;color:var(--gold);font-weight:600;letter-spacing:2px;}
  nav ul{display:flex;gap:30px;list-style:none;}
  nav ul li a{
    font-size:13px;font-weight:700;text-transform:uppercase;letter-spacing:1px;
    padding:6px 0;border-bottom:2px solid transparent;
  }
  nav ul li a:hover{color:var(--gold);border-color:var(--gold);}
  .nav-actions{display:flex;align-items:center;gap:16px;}
  .icon-link{
    width:36px;height:36px;border-radius:50%;
    border:1px solid rgba(255,255,255,.25);
    display:flex;align-items:center;justify-content:center;
    transition:all .2s ease;
  }
  .icon-link:hover{border-color:var(--gold);background:var(--gold);color:var(--black);}
  .menu-toggle{display:none;background:none;border:0;color:var(--white);font-size:26px;cursor:pointer;}

  /* Hero */
  .hero{
    position:relative;
    min-height:92vh;
    display:flex;align-items:center;justify-content:center;
    text-align:center;
    overflow:hidden;
    background:#000;
  }
  .hero video, .hero img.hero-fallback{
    position:absolute;inset:0;width:100%;height:100%;object-fit:cover;opacity:.45;
  }
  .hero::after{
    content:'';position:absolute;inset:0;
    background:linear-gradient(180deg, rgba(11,11,12,.55) 0%, rgba(11,11,12,.35) 40%, rgba(11,11,12,.92) 100%);
  }
  .hero-content{position:relative;z-index:2;padding:0 20px;max-width:820px;}
  .hero-content img.hero-logo{
    width:150px;margin:0 auto 26px;filter:drop-shadow(0 8px 24px rgba(0,0,0,.5));
  }
  .hero-content h1{
    font-size:clamp(34px,6vw,64px);
    font-weight:900;
    text-transform:uppercase;
    letter-spacing:2px;
    line-height:1.05;
  }
  .hero-content h1 em{color:var(--gold);font-style:normal;}
  .hero-content p{
    margin:20px auto 34px;
    max-width:560px;
    color:var(--gray);
    font-size:17px;
  }
  .hero-btns{display:flex;gap:16px;justify-content:center;flex-wrap:wrap;}

  /* Marquee stat strip */
  .stat-strip{
    background:var(--gold);
    color:var(--black);
    padding:26px 0;
  }
  .stat-strip .container{
    display:flex;flex-wrap:wrap;justify-content:space-between;gap:20px;text-align:center;
  }
  .stat-strip .stat{flex:1;min-width:130px;}
  .stat-strip .stat b{display:block;font-size:clamp(24px,3.2vw,34px);font-weight:900;}
  .stat-strip .stat span{font-size:11px;text-transform:uppercase;letter-spacing:1.5px;font-weight:700;}

  /* Section spacing */
  section{padding:90px 0;}
  .section-alt{background:var(--charcoal);}

  /* About */
  .about-grid{
    display:grid;grid-template-columns:1fr 1fr;gap:60px;align-items:center;
  }
  .about-grid p{color:var(--gray);margin-bottom:16px;font-size:15.5px;}
  .about-grid img{border:1px solid rgba(201,162,75,.3);}

  /* Video */
  .video-wrap{
    position:relative;border-radius:4px;overflow:hidden;border:1px solid rgba(201,162,75,.3);
    max-width:900px;margin:0 auto;
  }
  .video-wrap video{width:100%;display:block;background:#000;}

  /* Gallery */
  .gallery-grid{
    display:grid;grid-template-columns:1.3fr 1fr;gap:20px;
  }
  .gallery-grid img{
    width:100%;height:100%;object-fit:cover;border:1px solid rgba(201,162,75,.25);
  }
  .gallery-caption{
    text-align:center;color:var(--gray);font-size:13px;margin-top:14px;text-transform:uppercase;letter-spacing:1px;
  }

  /* Social */
  .social{
    text-align:center;
  }
  .social-handle{
    display:inline-flex;align-items:center;gap:10px;
    background:var(--gold);color:var(--black);
    padding:16px 32px;border-radius:2px;
    font-weight:800;text-transform:uppercase;letter-spacing:1px;font-size:14px;
    margin-top:10px;
  }
  .social-handle:hover{background:var(--gold-light);}

  /* Programs */
  .programs{display:grid;grid-template-columns:repeat(3,1fr);gap:24px;}
  .program-card{
    background:var(--charcoal);
    border:1px solid rgba(201,162,75,.2);
    padding:34px 28px;
  }
  .program-card h3{
    text-transform:uppercase;font-size:19px;margin-bottom:12px;color:var(--gold-light);
  }
  .program-card p{color:var(--gray);font-size:14.5px;}

  /* Contact / CTA */
  .cta{
    background:linear-gradient(135deg, var(--charcoal), #1c1c1f);
    border:1px solid rgba(201,162,75,.25);
    padding:60px 40px;
    text-align:center;
    border-radius:4px;
  }
  .cta p{color:var(--gray);max-width:520px;margin:14px auto 30px;}

  /* Footer */
  footer{
    background:var(--charcoal);
    border-top:1px solid rgba(201,162,75,.2);
    padding:60px 0 30px;
  }
  .footer-grid{
    display:grid;grid-template-columns:1.4fr 1fr 1fr;gap:40px;margin-bottom:40px;
  }
  .footer-brand{display:flex;align-items:center;gap:12px;margin-bottom:16px;}
  .footer-brand img{height:44px;}
  footer h4{
    text-transform:uppercase;font-size:13px;letter-spacing:1.5px;color:var(--gold);margin-bottom:16px;
  }
  footer ul{list-style:none;}
  footer ul li{margin-bottom:10px;font-size:14px;color:var(--gray);}
  footer ul li a:hover{color:var(--gold);}
  footer p{color:var(--gray);font-size:14px;}
  .footer-social{display:flex;gap:12px;margin-top:16px;}
  .footer-bottom{
    border-top:1px solid rgba(255,255,255,.08);
    padding-top:24px;
    display:flex;justify-content:space-between;flex-wrap:wrap;gap:10px;
    color:var(--gray);font-size:12.5px;
  }

  @media (max-width:900px){
    nav{display:none;}
    .menu-toggle{display:block;}
    .about-grid{grid-template-columns:1fr;}
    .gallery-grid{grid-template-columns:1fr;}
    .programs{grid-template-columns:1fr;}
    .footer-grid{grid-template-columns:1fr;}
    .stat-strip .container{justify-content:center;}
  }

  nav.open{
    display:block;position:absolute;top:100%;left:0;right:0;
    background:var(--black);border-bottom:1px solid rgba(201,162,75,.25);
  }
  nav.open ul{flex-direction:column;gap:0;padding:10px 24px 20px;}
  nav.open ul li{border-top:1px solid rgba(255,255,255,.06);}
  nav.open ul li a{display:block;padding:14px 0;}
</style>
</head>
<body>

<div class="topbar">South Florida Bulls Baseball &nbsp;•&nbsp; Youth &amp; Travel Baseball &nbsp;•&nbsp; South Florida</div>

<header>
  <div class="container nav-wrap">
    <a href="#top" class="brand">
      <img src="assets/logo.png" alt="South Florida Bulls Logo">
      <span class="brand-text">South Florida Bulls<span>Baseball</span></span>
    </a>
    <nav id="mainNav">
      <ul>
        <li><a href="#about">About</a></li>
        <li><a href="#programs">Teams</a></li>
        <li><a href="#championships">Championships</a></li>
        <li><a href="#video">Video</a></li>
        <li><a href="#gallery">Gallery</a></li>
        <li><a href="#contact">Contact</a></li>
      </ul>
    </nav>
    <div class="nav-actions">
      <a class="icon-link" href="https://www.instagram.com/sfbullsbaseball/?hl=en" target="_blank" rel="noopener" aria-label="Instagram">
        <svg width="17" height="17" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><rect x="2" y="2" width="20" height="20" rx="5"/><circle cx="12" cy="12" r="4"/><circle cx="17.5" cy="6.5" r="1"/></svg>
      </a>
      <a href="#contact" class="btn btn-primary" style="padding:10px 20px;font-size:12px;">Join The Bulls</a>
      <button class="menu-toggle" id="menuToggle" aria-label="Toggle menu">&#9776;</button>
    </div>
  </div>
</header>

<main id="top">
  <!-- HERO -->
  <section class="hero" style="padding:0;">
    <video autoplay muted loop playsinline poster="assets/video-poster.jpg">
      <source src="assets/highlight.mp4" type="video/mp4">
    </video>
    <div class="hero-content">
      <img class="hero-logo" src="assets/logo.png" alt="South Florida Bulls">
      <h1>South Florida <em>Bulls</em> Baseball</h1>
      <p>A youth and travel baseball organization built on hard work, family, and championship-level competition. Home is South Florida — the game is everything.</p>
      <div class="hero-btns">
        <a href="#contact" class="btn btn-primary">Join The Bulls</a>
        <a href="https://www.instagram.com/sfbullsbaseball/?hl=en" target="_blank" rel="noopener" class="btn btn-outline">Follow @sfbullsbaseball</a>
      </div>
    </div>
  </section>

  <!-- STAT STRIP -->
  <div class="stat-strip">
    <div class="container">
      <div class="stat"><b>2024</b><span>Gold Bat Champions</span></div>
      <div class="stat"><b>50+</b><span>Players in the Program</span></div>
      <div class="stat"><b>Multiple</b><span>Tournament Titles</span></div>
      <div class="stat"><b>South FL</b><span>Home Grown Talent</span></div>
    </div>
  </div>

  <!-- ABOUT -->
  <section id="about">
    <div class="container about-grid">
      <div>
        <div class="eyebrow">Who We Are</div>
        <h2 class="section-title">A Different Kind Of Program</h2>
        <p>South Florida Bulls Baseball is a competitive youth and travel baseball organization dedicated to developing ballplayers both on and off the field. Our coaching staff focuses on fundamentals, discipline, and a team-first culture that prepares players for the next level.</p>
        <p>From our youngest athletes to our most advanced travel squads, the Bulls compete against top competition across South Florida and beyond — building champions one game at a time.</p>
        <a href="#programs" class="btn btn-outline">See Our Teams</a>
      </div>
      <div>
        <img src="assets/team-champions.jpg" alt="South Florida Bulls - Gold Bat Championship team">
      </div>
    </div>
  </section>

  <!-- CHAMPIONSHIPS -->
  <section id="championships" class="section-alt">
    <div class="container" style="text-align:center;">
      <div class="eyebrow">Winning Culture</div>
      <h2 class="section-title">Championships</h2>
      <p style="color:var(--gray);max-width:640px;margin:0 auto 40px;">Our players compete — and win — at the highest level of youth tournament baseball, including USSSA Gold Bat Championship honors.</p>
      <img src="assets/team-champions.jpg" alt="South Florida Bulls Gold Bat Champions" style="max-width:700px;margin:0 auto;border:1px solid rgba(201,162,75,.3);">
    </div>
  </section>

  <!-- VIDEO -->
  <section id="video">
    <div class="container" style="text-align:center;">
      <div class="eyebrow">Bulls In Action</div>
      <h2 class="section-title">Watch The Highlights</h2>
      <p style="color:var(--gray);max-width:560px;margin:0 auto 40px;">Get a look at the South Florida Bulls on the field.</p>
      <div class="video-wrap">
        <video controls poster="assets/video-poster.jpg">
          <source src="assets/highlight.mp4" type="video/mp4">
          Your browser does not support embedded video.
        </video>
      </div>
    </div>
  </section>

  <!-- PROGRAMS -->
  <section id="programs" class="section-alt">
    <div class="container">
      <div style="text-align:center;">
        <div class="eyebrow">Get Involved</div>
        <h2 class="section-title">Our Programs</h2>
      </div>
      <div class="programs" style="margin-top:40px;">
        <div class="program-card">
          <h3>Youth Teams</h3>
          <p>Foundational coaching for our youngest Bulls, building fundamentals, love of the game, and team chemistry from the ground up.</p>
        </div>
        <div class="program-card">
          <h3>Travel Baseball</h3>
          <p>Competitive travel squads that battle for hardware at top South Florida and national tournaments throughout the season.</p>
        </div>
        <div class="program-card">
          <h3>Player Development</h3>
          <p>Individualized instruction and training focused on hitting, pitching, fielding, and the mental side of the game.</p>
        </div>
      </div>
    </div>
  </section>

  <!-- GALLERY -->
  <section id="gallery">
    <div class="container">
      <div style="text-align:center;">
        <div class="eyebrow">Bulls Nation</div>
        <h2 class="section-title">Gallery</h2>
      </div>
      <div class="gallery-grid" style="margin-top:40px;">
        <img src="assets/team-group-web.jpg" alt="South Florida Bulls team and coaches">
        <img src="assets/team-champions.jpg" alt="South Florida Bulls Gold Bat Champions">
      </div>
      <div class="gallery-caption">South Florida Bulls Baseball — Players, Coaches &amp; Family</div>
    </div>
  </section>

  <!-- SOCIAL -->
  <section class="section-alt social">
    <div class="container">
      <div class="eyebrow">Find Us Online</div>
      <h2 class="section-title">Follow The Bulls</h2>
      <p style="color:var(--gray);max-width:520px;margin:0 auto 10px;">Stay up to date on tryouts, tournaments, and team news. Follow the South Florida Bulls on Instagram.</p>
      <a class="social-handle" href="https://www.instagram.com/sfbullsbaseball/?hl=en" target="_blank" rel="noopener">
        <svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><rect x="2" y="2" width="20" height="20" rx="5"/><circle cx="12" cy="12" r="4"/><circle cx="17.5" cy="6.5" r="1"/></svg>
        @sfbullsbaseball
      </a>
    </div>
  </section>

  <!-- CONTACT / CTA -->
  <section id="contact">
    <div class="container">
      <div class="cta">
        <div class="eyebrow">Join The Bulls</div>
        <h2 class="section-title" style="margin-bottom:0;">Interested In Playing For The Bulls?</h2>
        <p>Reach out to learn more about tryouts, team placement, and upcoming tournaments for the South Florida Bulls.</p>
        <div class="hero-btns">
          <a href="mailto:info@sfbullsbaseball.com" class="btn btn-primary">Email Us</a>
          <a href="https://www.instagram.com/sfbullsbaseball/?hl=en" target="_blank" rel="noopener" class="btn btn-outline">Message Us On Instagram</a>
        </div>
      </div>
    </div>
  </section>
</main>

<footer>
  <div class="container">
    <div class="footer-grid">
      <div>
        <div class="footer-brand">
          <img src="assets/logo.png" alt="South Florida Bulls">
          <b style="text-transform:uppercase;letter-spacing:1px;">South Florida Bulls</b>
        </div>
        <p>A youth and travel baseball organization proudly representing South Florida. Building ballplayers, teammates, and champions.</p>
        <div class="footer-social">
          <a class="icon-link" href="https://www.instagram.com/sfbullsbaseball/?hl=en" target="_blank" rel="noopener" aria-label="Instagram">
            <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><rect x="2" y="2" width="20" height="20" rx="5"/><circle cx="12" cy="12" r="4"/><circle cx="17.5" cy="6.5" r="1"/></svg>
          </a>
        </div>
      </div>
      <div>
        <h4>Quick Links</h4>
        <ul>
          <li><a href="#about">About</a></li>
          <li><a href="#programs">Teams</a></li>
          <li><a href="#championships">Championships</a></li>
          <li><a href="#gallery">Gallery</a></li>
        </ul>
      </div>
      <div>
        <h4>Contact</h4>
        <ul>
          <li><a href="mailto:info@sfbullsbaseball.com">info@sfbullsbaseball.com</a></li>
          <li><a href="https://www.instagram.com/sfbullsbaseball/?hl=en" target="_blank" rel="noopener">@sfbullsbaseball</a></li>
          <li>South Florida</li>
        </ul>
      </div>
    </div>
    <div class="footer-bottom">
      <span>&copy; 2026 South Florida Bulls Baseball. All Rights Reserved.</span>
      <span>Different Brand Of Baseball</span>
    </div>
  </div>
</footer>

<script>
  const toggle = document.getElementById('menuToggle');
  const nav = document.getElementById('mainNav');
  toggle.addEventListener('click', () => nav.classList.toggle('open'));
  nav.querySelectorAll('a').forEach(a => a.addEventListener('click', () => nav.classList.remove('open')));
</script>

</body>
</html>

