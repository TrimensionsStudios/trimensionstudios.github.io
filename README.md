<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Trimensions Studios</title>
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,300;0,400;0,600;1,300;1,400&family=Barlow:wght@300;400;500;600&family=Barlow+Condensed:wght@300;400;500;600;700&display=swap" rel="stylesheet"/>
<style>
*{margin:0;padding:0;box-sizing:border-box;}
:root{
  --black:#0a0a0a;
  --white:#f5f2ed;
  --cream:#e8e2d9;
  --gold:#c9a96e;
  --gold-dim:#8a6d42;
  --dark:#111010;
  --mid:#1e1c1b;
  --panel:#161412;
  --text-muted:#7a7570;
  --text-sub:#4a4643;
}
html{scroll-behavior:smooth;}
body{
  background:var(--black);
  color:var(--white);
  font-family:'Barlow',sans-serif;
  font-weight:300;
  overflow-x:hidden;
}

/* NAV */
nav{
  position:fixed;top:0;left:0;right:0;z-index:100;
  display:flex;align-items:center;justify-content:space-between;
  padding:1.5rem 3rem;
  background:linear-gradient(to bottom,rgba(10,10,10,0.95),transparent);
}
.nav-logo{
  font-family:'Barlow Condensed',sans-serif;
  font-size:1.1rem;font-weight:600;letter-spacing:0.25em;
  color:var(--white);text-transform:uppercase;text-decoration:none;
}
.nav-logo span{color:var(--gold);}
.nav-links{display:flex;gap:2.5rem;list-style:none;}
.nav-links a{
  font-size:0.75rem;font-weight:400;letter-spacing:0.18em;
  color:var(--text-muted);text-transform:uppercase;text-decoration:none;
  transition:color 0.3s;
}
.nav-links a:hover{color:var(--gold);}

/* HERO */
#hero{
  min-height:100vh;position:relative;
  display:flex;align-items:flex-end;
  padding:0 3rem 5rem;
  overflow:hidden;
}
.hero-bg{
  position:absolute;inset:0;
  background:
    radial-gradient(ellipse 60% 70% at 70% 40%, rgba(201,169,110,0.08) 0%, transparent 60%),
    radial-gradient(ellipse 40% 50% at 20% 80%, rgba(201,169,110,0.04) 0%, transparent 50%),
    var(--black);
}
.hero-grid{
  position:absolute;inset:0;
  background-image:
    linear-gradient(rgba(201,169,110,0.04) 1px, transparent 1px),
    linear-gradient(90deg, rgba(201,169,110,0.04) 1px, transparent 1px);
  background-size:80px 80px;
  mask-image:radial-gradient(ellipse 80% 80% at 60% 40%, black 30%, transparent 80%);
}
.hero-tag{
  position:absolute;top:50%;right:3rem;transform:translateY(-50%);
  writing-mode:vertical-rl;text-orientation:mixed;
  font-family:'Barlow Condensed',sans-serif;
  font-size:0.65rem;font-weight:400;letter-spacing:0.3em;
  color:var(--text-sub);text-transform:uppercase;
}
.hero-content{position:relative;max-width:780px;}
.hero-eyebrow{
  font-family:'Barlow Condensed',sans-serif;
  font-size:0.7rem;font-weight:500;letter-spacing:0.35em;
  color:var(--gold);text-transform:uppercase;
  margin-bottom:1.5rem;display:flex;align-items:center;gap:1rem;
}
.hero-eyebrow::before{content:'';display:block;width:2rem;height:1px;background:var(--gold);}
h1.hero-title{
  font-family:'Cormorant Garamond',serif;
  font-size:clamp(3.5rem,7vw,6rem);
  font-weight:300;line-height:1.05;
  color:var(--white);margin-bottom:1.5rem;
}
h1.hero-title em{color:var(--gold);font-style:italic;}
.hero-desc{
  font-size:0.95rem;font-weight:300;line-height:1.8;
  color:var(--text-muted);max-width:440px;margin-bottom:2.5rem;
}
.hero-actions{display:flex;gap:1.25rem;align-items:center;}
.btn-primary{
  font-family:'Barlow Condensed',sans-serif;
  font-size:0.75rem;font-weight:500;letter-spacing:0.2em;text-transform:uppercase;
  padding:0.9rem 2.2rem;
  background:var(--gold);color:var(--black);
  border:none;cursor:pointer;text-decoration:none;
  transition:background 0.3s,transform 0.2s;display:inline-block;
}
.btn-primary:hover{background:#d4b47e;transform:translateY(-2px);}
.btn-outline{
  font-family:'Barlow Condensed',sans-serif;
  font-size:0.75rem;font-weight:500;letter-spacing:0.2em;text-transform:uppercase;
  padding:0.9rem 2.2rem;
  background:transparent;color:var(--white);
  border:1px solid rgba(245,242,237,0.2);cursor:pointer;text-decoration:none;
  transition:border-color 0.3s,color 0.3s;display:inline-block;
}
.btn-outline:hover{border-color:var(--gold);color:var(--gold);}

/* STATS BAR */
.stats-bar{
  background:var(--panel);
  border-top:1px solid rgba(201,169,110,0.12);
  border-bottom:1px solid rgba(201,169,110,0.12);
  padding:2rem 3rem;
  display:flex;align-items:center;justify-content:space-around;
  gap:2rem;flex-wrap:wrap;
}
.stat-item{text-align:center;}
.stat-num{
  font-family:'Cormorant Garamond',serif;
  font-size:2rem;font-weight:300;color:var(--gold);display:block;
}
.stat-label{
  font-size:0.65rem;font-weight:400;letter-spacing:0.2em;
  color:var(--text-muted);text-transform:uppercase;margin-top:0.25rem;
}
.stat-divider{width:1px;height:3rem;background:rgba(201,169,110,0.15);}

/* SECTION */
section{padding:6rem 3rem;}
.section-eyebrow{
  font-family:'Barlow Condensed',sans-serif;
  font-size:0.65rem;font-weight:500;letter-spacing:0.3em;
  color:var(--gold);text-transform:uppercase;
  display:flex;align-items:center;gap:1rem;margin-bottom:1rem;
}
.section-eyebrow::before{content:'';display:block;width:2rem;height:1px;background:var(--gold);}
h2.section-title{
  font-family:'Cormorant Garamond',serif;
  font-size:clamp(2rem,4vw,3rem);font-weight:300;line-height:1.1;
  margin-bottom:1.5rem;
}
h2.section-title em{color:var(--gold);font-style:italic;}

/* SERVICES */
#services{background:var(--dark);}
.services-intro{
  display:grid;grid-template-columns:1fr 1fr;gap:4rem;
  align-items:start;margin-bottom:4rem;
}
.services-desc{
  font-size:0.9rem;font-weight:300;line-height:1.9;
  color:var(--text-muted);padding-top:0.5rem;
}
.services-grid{
  display:grid;grid-template-columns:repeat(3,1fr);gap:1px;
  background:rgba(201,169,110,0.1);border:1px solid rgba(201,169,110,0.1);
}
.service-card{
  background:var(--dark);
  padding:2.5rem 2rem;
  transition:background 0.3s;cursor:default;
}
.service-card:hover{background:var(--mid);}
.service-icon{
  width:2.5rem;height:2.5rem;
  border:1px solid rgba(201,169,110,0.3);
  display:flex;align-items:center;justify-content:center;
  margin-bottom:1.5rem;
}
.service-icon svg{width:16px;height:16px;stroke:var(--gold);fill:none;stroke-width:1.5;}
.service-name{
  font-family:'Barlow Condensed',sans-serif;
  font-size:0.8rem;font-weight:600;letter-spacing:0.15em;
  text-transform:uppercase;color:var(--white);margin-bottom:0.75rem;
}
.service-desc{
  font-size:0.82rem;font-weight:300;line-height:1.8;
  color:var(--text-muted);
}
.service-tag{
  margin-top:1.5rem;
  font-size:0.65rem;font-weight:500;letter-spacing:0.15em;
  color:var(--gold);text-transform:uppercase;
  display:flex;align-items:center;gap:0.5rem;
}
.service-tag::after{content:'→';}

/* PORTFOLIO PREVIEW */
#portfolio{background:var(--black);}
.portfolio-header{
  display:flex;justify-content:space-between;align-items:flex-end;margin-bottom:3rem;
}
.portfolio-grid{
  display:grid;
  grid-template-columns:1.6fr 1fr;
  grid-template-rows:auto auto;
  gap:1px;background:rgba(201,169,110,0.08);
}
.portfolio-item{
  position:relative;overflow:hidden;cursor:pointer;
  background:var(--mid);
}
.portfolio-item:nth-child(1){grid-row:span 2;}
.portfolio-item:nth-child(2){grid-column:2;}
.portfolio-item:nth-child(3){grid-column:2;}
.port-render{
  width:100%;aspect-ratio:4/3;
  display:flex;align-items:center;justify-content:center;
  font-family:'Cormorant Garamond',serif;
  font-size:5rem;font-weight:300;
  color:rgba(201,169,110,0.06);
  position:relative;
  overflow:hidden;
}
.portfolio-item:nth-child(1) .port-render{aspect-ratio:3/4;}
.portfolio-item:nth-child(2) .port-render,
.portfolio-item:nth-child(3) .port-render{aspect-ratio:16/9;}
.port-render-bg{
  position:absolute;inset:0;
  display:flex;align-items:center;justify-content:center;
}
.port-render-grid{
  position:absolute;inset:0;
  background-image:
    linear-gradient(rgba(201,169,110,0.03) 1px,transparent 1px),
    linear-gradient(90deg,rgba(201,169,110,0.03) 1px,transparent 1px);
  background-size:40px 40px;
}
.port-shape-1{
  width:60%;height:70%;
  border:1px solid rgba(201,169,110,0.08);
  position:absolute;top:15%;left:20%;
}
.port-shape-2{
  width:40%;height:50%;
  border:1px solid rgba(201,169,110,0.05);
  position:absolute;top:25%;left:30%;
  transform:rotate(15deg);
}
.port-line-h{
  position:absolute;left:0;right:0;
  height:1px;background:rgba(201,169,110,0.06);
}
.port-line-v{
  position:absolute;top:0;bottom:0;
  width:1px;background:rgba(201,169,110,0.06);
}
.port-dot{
  position:absolute;
  width:4px;height:4px;border-radius:50%;
  background:var(--gold);opacity:0.4;
}
.port-overlay{
  position:absolute;inset:0;
  background:linear-gradient(to top,rgba(10,10,10,0.9) 0%,transparent 50%);
  display:flex;flex-direction:column;justify-content:flex-end;
  padding:1.5rem;
  opacity:0;transition:opacity 0.3s;
}
.portfolio-item:hover .port-overlay{opacity:1;}
.port-cat{
  font-size:0.6rem;font-weight:500;letter-spacing:0.2em;
  color:var(--gold);text-transform:uppercase;margin-bottom:0.4rem;
}
.port-title{
  font-family:'Cormorant Garamond',serif;
  font-size:1.3rem;font-weight:300;color:var(--white);
}
.port-label{
  position:absolute;top:1rem;left:1rem;
  font-size:0.6rem;font-weight:500;letter-spacing:0.2em;
  color:var(--text-muted);text-transform:uppercase;
}

/* PROCESS */
#process{background:var(--panel);}
.process-grid{
  display:grid;grid-template-columns:repeat(4,1fr);
  gap:0;margin-top:3rem;
  border-left:1px solid rgba(201,169,110,0.1);
}
.process-step{
  padding:2rem 2rem 2rem 2rem;
  border-right:1px solid rgba(201,169,110,0.1);
  border-bottom:1px solid rgba(201,169,110,0.1);
  position:relative;
}
.step-num{
  font-family:'Cormorant Garamond',serif;
  font-size:3.5rem;font-weight:300;
  color:rgba(201,169,110,0.12);
  line-height:1;margin-bottom:1rem;
}
.step-name{
  font-family:'Barlow Condensed',sans-serif;
  font-size:0.8rem;font-weight:600;letter-spacing:0.15em;
  text-transform:uppercase;color:var(--white);margin-bottom:0.75rem;
}
.step-desc{
  font-size:0.8rem;font-weight:300;line-height:1.8;
  color:var(--text-muted);
}

/* ABOUT */
#about{background:var(--dark);}
.about-grid{
  display:grid;grid-template-columns:1fr 1fr;gap:5rem;align-items:center;
}
.about-visual{
  position:relative;
  aspect-ratio:3/4;
  border:1px solid rgba(201,169,110,0.12);
}
.about-visual-inner{
  position:absolute;inset:0;
  background:var(--mid);
  display:flex;align-items:center;justify-content:center;
  font-family:'Cormorant Garamond',serif;
  font-size:0.75rem;letter-spacing:0.3em;
  color:rgba(201,169,110,0.15);text-transform:uppercase;
}
.about-visual-corner{
  position:absolute;width:1.5rem;height:1.5rem;
}
.about-visual-corner.tl{top:-1px;left:-1px;border-top:2px solid var(--gold);border-left:2px solid var(--gold);}
.about-visual-corner.br{bottom:-1px;right:-1px;border-bottom:2px solid var(--gold);border-right:2px solid var(--gold);}
.about-content p{
  font-size:0.9rem;font-weight:300;line-height:1.9;
  color:var(--text-muted);margin-bottom:1.5rem;
}
.about-specialties{
  display:flex;flex-wrap:wrap;gap:0.75rem;margin-top:2rem;
}
.specialty-tag{
  font-size:0.65rem;font-weight:500;letter-spacing:0.15em;
  text-transform:uppercase;padding:0.5rem 1rem;
  border:1px solid rgba(201,169,110,0.2);color:var(--gold);
}

/* CONTACT */
#contact{background:var(--black);}
.contact-grid{
  display:grid;grid-template-columns:1fr 1.2fr;gap:5rem;align-items:start;
}
.contact-info p{
  font-size:0.9rem;font-weight:300;line-height:1.9;
  color:var(--text-muted);margin-bottom:2rem;
}
.contact-detail{
  display:flex;align-items:flex-start;gap:1rem;margin-bottom:1.5rem;
}
.contact-detail-icon{
  width:1.5rem;height:1.5rem;
  border:1px solid rgba(201,169,110,0.25);
  display:flex;align-items:center;justify-content:center;flex-shrink:0;margin-top:2px;
}
.contact-detail-icon svg{width:12px;height:12px;stroke:var(--gold);fill:none;stroke-width:1.5;}
.contact-detail-text{
  font-size:0.82rem;font-weight:300;line-height:1.6;color:var(--text-muted);
}
.contact-detail-text strong{display:block;color:var(--white);font-weight:400;margin-bottom:0.2rem;letter-spacing:0.05em;}
.contact-form{display:flex;flex-direction:column;gap:1rem;}
.form-row{display:grid;grid-template-columns:1fr 1fr;gap:1rem;}
.form-field{display:flex;flex-direction:column;gap:0.4rem;}
.form-field label{
  font-size:0.65rem;font-weight:500;letter-spacing:0.18em;
  color:var(--text-muted);text-transform:uppercase;
}
.form-field input,
.form-field select,
.form-field textarea{
  background:var(--mid);
  border:1px solid rgba(201,169,110,0.12);
  color:var(--white);
  padding:0.75rem 1rem;
  font-family:'Barlow',sans-serif;font-size:0.85rem;font-weight:300;
  outline:none;transition:border-color 0.3s;
  -webkit-appearance:none;
}
.form-field input:focus,
.form-field select,
.form-field textarea:focus{border-color:rgba(201,169,110,0.4);}
.form-field textarea{resize:vertical;min-height:100px;}
.form-field select option{background:var(--dark);}
.form-submit{margin-top:0.5rem;}

/* FOOTER */
footer{
  background:var(--panel);
  border-top:1px solid rgba(201,169,110,0.1);
  padding:2.5rem 3rem;
  display:flex;justify-content:space-between;align-items:center;flex-wrap:wrap;gap:1rem;
}
.footer-logo{
  font-family:'Barlow Condensed',sans-serif;
  font-size:0.9rem;font-weight:600;letter-spacing:0.25em;
  color:var(--white);text-transform:uppercase;
}
.footer-logo span{color:var(--gold);}
.footer-copy{
  font-size:0.7rem;font-weight:300;letter-spacing:0.1em;
  color:var(--text-sub);
}
.footer-links{display:flex;gap:2rem;}
.footer-links a{
  font-size:0.65rem;font-weight:400;letter-spacing:0.15em;
  color:var(--text-sub);text-transform:uppercase;text-decoration:none;
  transition:color 0.3s;
}
.footer-links a:hover{color:var(--gold);}

/* SCROLL REVEAL */
.reveal{opacity:0;transform:translateY(24px);transition:opacity 0.7s ease,transform 0.7s ease;}
.reveal.visible{opacity:1;transform:translateY(0);}
</style>
</head>
<body>

<nav>
  <a class="nav-logo" href="#hero">TRI<span>·</span>MENSIONS</a>
  <ul class="nav-links">
    <li><a href="#services">Services</a></li>
    <li><a href="#portfolio">Portfolio</a></li>
    <li><a href="#process">Process</a></li>
    <li><a href="#about">Studio</a></li>
    <li><a href="#contact">Contact</a></li>
  </ul>
</nav>

<!-- HERO -->
<section id="hero">
  <div class="hero-bg"></div>
  <div class="hero-grid"></div>
  <div class="hero-tag">Architecture · 3D · Rendering</div>
  <div class="hero-content">
    <div class="hero-eyebrow">Trimensions Studios</div>
    <h1 class="hero-title">
      Where Space<br>Becomes <em>Vision</em>
    </h1>
    <p class="hero-desc">
      Architectural 3D visualisation and photorealistic rendering for interiors, residences, villas, high-rises, and commercial spaces. We translate blueprints into breathtaking realities.
    </p>
    <div class="hero-actions">
      <a href="#portfolio" class="btn-primary">View Our Work</a>
      <a href="#contact" class="btn-outline">Start a Project</a>
    </div>
  </div>
</section>

<!-- STATS -->
<div class="stats-bar">
  <div class="stat-item">
    <span class="stat-num">120+</span>
    <div class="stat-label">Projects Delivered</div>
  </div>
  <div class="stat-divider"></div>
  <div class="stat-item">
    <span class="stat-num">5+</span>
    <div class="stat-label">Years of Experience</div>
  </div>
  <div class="stat-divider"></div>
  <div class="stat-item">
    <span class="stat-num">98%</span>
    <div class="stat-label">Client Satisfaction</div>
  </div>
  <div class="stat-divider"></div>
  <div class="stat-item">
    <span class="stat-num">40+</span>
    <div class="stat-label">Architects & Developers</div>
  </div>
</div>

<!-- SERVICES -->
<section id="services">
  <div class="services-intro reveal">
    <div>
      <div class="section-eyebrow">What We Do</div>
      <h2 class="section-title">Crafted with<br><em>Light & Detail</em></h2>
    </div>
    <p class="services-desc">
      From intimate interiors to soaring high-rises, every project at Trimensions Studios is treated as an opportunity to push the boundaries of photorealistic rendering. Our work doesn't just show spaces — it makes people feel them.
    </p>
  </div>
  <div class="services-grid reveal">
    <div class="service-card">
      <div class="service-icon">
        <svg viewBox="0 0 24 24"><rect x="3" y="3" width="18" height="18" rx="1"/><path d="M3 9h18M9 21V9"/></svg>
      </div>
      <div class="service-name">Interior Rendering</div>
      <p class="service-desc">Photorealistic visualisation of living spaces, bedrooms, kitchens, bathrooms, and commercial interiors with precise material and lighting accuracy.</p>
      <div class="service-tag">Explore</div>
    </div>
    <div class="service-card">
      <div class="service-icon">
        <svg viewBox="0 0 24 24"><path d="M3 21h18M5 21V7l7-4 7 4v14"/><path d="M9 21v-6h6v6"/></svg>
      </div>
      <div class="service-name">Residential Villas</div>
      <p class="service-desc">Exterior and interior renders for bungalows and luxury villas — capturing architecture, landscaping, and atmosphere in full cinematic quality.</p>
      <div class="service-tag">Explore</div>
    </div>
    <div class="service-card">
      <div class="service-icon">
        <svg viewBox="0 0 24 24"><rect x="4" y="2" width="16" height="20" rx="1"/><path d="M8 6h8M8 10h8M8 14h8M8 18h4"/></svg>
      </div>
      <div class="service-name">High-Rise & Commercial</div>
      <p class="service-desc">Large-scale architectural renders for towers, office complexes, retail spaces, and mixed-use developments with full environmental context.</p>
      <div class="service-tag">Explore</div>
    </div>
  </div>
</section>

<!-- PORTFOLIO -->
<section id="portfolio">
  <div class="portfolio-header reveal">
    <div>
      <div class="section-eyebrow">Selected Works</div>
      <h2 class="section-title">Our <em>Portfolio</em></h2>
    </div>
    <a href="#contact" class="btn-outline">Commission a Project</a>
  </div>
  <div class="portfolio-grid reveal">
    <div class="portfolio-item">
      <div class="port-render">
        <div class="port-render-bg">
          <div class="port-render-grid"></div>
          <div class="port-shape-1"></div>
          <div class="port-shape-2"></div>
          <div class="port-line-h" style="top:30%"></div>
          <div class="port-line-h" style="top:60%"></div>
          <div class="port-line-v" style="left:35%"></div>
          <div class="port-line-v" style="left:70%"></div>
          <div class="port-dot" style="top:30%;left:35%"></div>
          <div class="port-dot" style="top:60%;left:70%"></div>
          <div class="port-dot" style="top:30%;left:70%"></div>
        </div>
        TS
      </div>
      <div class="port-label">Featured</div>
      <div class="port-overlay">
        <div class="port-cat">Luxury Villa · Exterior</div>
        <div class="port-title">Serene Modern Residence</div>
      </div>
    </div>
    <div class="portfolio-item">
      <div class="port-render">
        <div class="port-render-bg">
          <div class="port-render-grid"></div>
          <div class="port-shape-1" style="width:50%;height:60%;top:20%;left:25%"></div>
          <div class="port-line-h" style="top:50%"></div>
          <div class="port-line-v" style="left:50%"></div>
          <div class="port-dot" style="top:50%;left:50%"></div>
        </div>
        TS
      </div>
      <div class="port-label">Interior</div>
      <div class="port-overlay">
        <div class="port-cat">Interior · Living Room</div>
        <div class="port-title">The Warm Loft</div>
      </div>
    </div>
    <div class="portfolio-item">
      <div class="port-render">
        <div class="port-render-bg">
          <div class="port-render-grid"></div>
          <div class="port-shape-1" style="width:70%;height:65%;top:18%;left:15%"></div>
          <div class="port-line-h" style="top:40%"></div>
          <div class="port-line-h" style="top:70%"></div>
          <div class="port-line-v" style="left:30%"></div>
          <div class="port-dot" style="top:40%;left:30%"></div>
          <div class="port-dot" style="top:70%;left:70%"></div>
        </div>
        TS
      </div>
      <div class="port-label">Commercial</div>
      <div class="port-overlay">
        <div class="port-cat">Commercial · Office</div>
        <div class="port-title">Glass Tower Lobby</div>
      </div>
    </div>
  </div>
</section>

<!-- PROCESS -->
<section id="process">
  <div class="reveal">
    <div class="section-eyebrow">How We Work</div>
    <h2 class="section-title">The <em>Process</em></h2>
  </div>
  <div class="process-grid reveal">
    <div class="process-step">
      <div class="step-num">01</div>
      <div class="step-name">Brief & Discovery</div>
      <p class="step-desc">We begin by understanding your vision — floor plans, references, mood boards, materials, and the story you want to tell.</p>
    </div>
    <div class="process-step">
      <div class="step-num">02</div>
      <div class="step-name">3D Modelling</div>
      <p class="step-desc">Our team builds a precise, detailed 3D model of your space using industry-standard tools.</p>
    </div>
    <div class="process-step">
      <div class="step-num">03</div>
      <div class="step-name">Lighting & Materials</div>
      <p class="step-desc">Every surface, texture, and light source is dialled in to achieve photorealistic accuracy and emotional depth.</p>
    </div>
    <div class="process-step">
      <div class="step-num">04</div>
      <div class="step-name">Final Render & Delivery</div>
      <p class="step-desc">High-resolution renders are delivered with revisions included, ensuring the result exceeds your expectations.</p>
    </div>
  </div>
</section>

<!-- ABOUT -->
<section id="about">
  <div class="about-grid reveal">
    <div class="about-visual">
      <div class="about-visual-inner">Trimensions Studios</div>
      <div class="about-visual-corner tl"></div>
      <div class="about-visual-corner br"></div>
    </div>
    <div class="about-content">
      <div class="section-eyebrow">The Studio</div>
      <h2 class="section-title">Built on a<br>Passion for <em>Rendering</em></h2>
      <p>Trimensions Studios was born from a deep love of architectural visualisation. We believe a render isn't just a preview — it's a promise. A beautifully crafted image can sell a dream, win a client, and inspire a builder before a single brick is laid.</p>
      <p>We specialise across every scale of the built environment — from intimate residential interiors to large-scale commercial developments — but our heart lies in rendering: the play of light, shadow, texture, and atmosphere that makes a space feel alive.</p>
      <div class="about-specialties">
        <span class="specialty-tag">Interiors</span>
        <span class="specialty-tag">Residential</span>
        <span class="specialty-tag">Villas</span>
        <span class="specialty-tag">High-Rise</span>
        <span class="specialty-tag">Commercial</span>
        <span class="specialty-tag">Photorealistic Renders</span>
        <span class="specialty-tag">3D Visualisation</span>
      </div>
    </div>
  </div>
</section>

<!-- CONTACT -->
<section id="contact">
  <div class="section-eyebrow reveal">Let's Create Together</div>
  <h2 class="section-title reveal">Start a <em>Project</em></h2>
  <div class="contact-grid" style="margin-top:3rem;">
    <div class="contact-info reveal">
      <p>Ready to bring your space to life? Tell us about your project and we'll get back to you within 24 hours with a tailored proposal.</p>
      <div class="contact-detail">
        <div class="contact-detail-icon">
          <svg viewBox="0 0 24 24"><path d="M22 16.92v3a2 2 0 01-2.18 2 19.79 19.79 0 01-8.63-3.07A19.5 19.5 0 013.07 9.67 19.79 19.79 0 01.1 1.14 2 2 0 012.08 0h3a2 2 0 012 1.72c.127.96.361 1.903.7 2.81a2 2 0 01-.45 2.11L6.09 7.91a16 16 0 006 6l1.27-1.27a2 2 0 012.11-.45c.907.339 1.85.573 2.81.7A2 2 0 0122 16.92z"/></svg>
        </div>
        <div class="contact-detail-text">
          <strong>Phone</strong>
          +91 98765 43210
        </div>
      </div>
      <div class="contact-detail">
        <div class="contact-detail-icon">
          <svg viewBox="0 0 24 24"><path d="M4 4h16c1.1 0 2 .9 2 2v12c0 1.1-.9 2-2 2H4c-1.1 0-2-.9-2-2V6c0-1.1.9-2 2-2z"/><polyline points="22,6 12,13 2,6"/></svg>
        </div>
        <div class="contact-detail-text">
          <strong>Email</strong>
          hello@trimensions.studio
        </div>
      </div>
      <div class="contact-detail">
        <div class="contact-detail-icon">
          <svg viewBox="0 0 24 24"><path d="M21 10c0 7-9 13-9 13s-9-6-9-13a9 9 0 0118 0z"/><circle cx="12" cy="10" r="3"/></svg>
        </div>
        <div class="contact-detail-text">
          <strong>Location</strong>
          Ahmedabad, Gujarat, India
        </div>
      </div>
    </div>
    <div class="contact-form reveal">
      <div class="form-row">
        <div class="form-field">
          <label>Your Name</label>
          <input type="text" placeholder="Full name" />
        </div>
        <div class="form-field">
          <label>Email Address</label>
          <input type="email" placeholder="your@email.com" />
        </div>
      </div>
      <div class="form-row">
        <div class="form-field">
          <label>Phone</label>
          <input type="tel" placeholder="+91 ..." />
        </div>
        <div class="form-field">
          <label>Project Type</label>
          <select>
            <option>Interior Rendering</option>
            <option>Residential / Bungalow</option>
            <option>Luxury Villa</option>
            <option>High-Rise Building</option>
            <option>Commercial Space</option>
            <option>Other</option>
          </select>
        </div>
      </div>
      <div class="form-field">
        <label>Project Brief</label>
        <textarea placeholder="Tell us about your project — space size, style references, timeline, budget..."></textarea>
      </div>
      <div class="form-submit">
        <button class="btn-primary" style="width:100%;" onclick="alert('Thank you! We\'ll be in touch within 24 hours.')">Send Project Brief</button>
      </div>
    </div>
  </div>
</section>

<!-- FOOTER -->
<footer>
  <div class="footer-logo">TRI<span>·</span>MENSIONS <span style="color:var(--text-sub);font-weight:300;">Studios</span></div>
  <div class="footer-copy">© 2024 Trimensions Studios. All rights reserved.</div>
  <div class="footer-links">
    <a href="#services">Services</a>
    <a href="#portfolio">Portfolio</a>
    <a href="#contact">Contact</a>
  </div>
</footer>

<script>
const reveals = document.querySelectorAll('.reveal');
const observer = new IntersectionObserver((entries) => {
  entries.forEach(e => {
    if(e.isIntersecting){ e.target.classList.add('visible'); }
  });
}, {threshold:0.1});
reveals.forEach(r => observer.observe(r));
</script>
</body>
</html>
