[index (2).html](https://github.com/user-attachments/files/28066471/index.2.html)
# PLANNND.MEDIA
Content, photography, vision. Social-first, editorial, cinematic content and marketing assets.
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>PLANNND.MEDIA — Content. Photography. Vision.</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,400;0,500;1,400&family=DM+Sans:ital,opsz,wght@0,9..40,200;0,9..40,300;0,9..40,400;1,9..40,300&family=Space+Mono&display=swap" rel="stylesheet">
<style>
*, *::before, *::after { margin: 0; padding: 0; box-sizing: border-box; }

:root {
  --ink: #0a0a0a;
  --ink-2: #111;
  --ink-3: #1c1c1c;
  --ink-4: #282828;
  --mid: #555;
  --mid-2: #888;
  --edge: rgba(255,255,255,0.07);
  --edge-2: rgba(255,255,255,0.13);
  --edge-3: rgba(255,255,255,0.22);
  --white: #fafaf9;
  --f-serif: 'Playfair Display', Georgia, serif;
  --f-sans: 'DM Sans', sans-serif;
  --f-mono: 'Space Mono', monospace;
}

html { scroll-behavior: smooth; }

body {
  background: var(--ink);
  color: var(--white);
  font-family: var(--f-sans);
  font-weight: 300;
  line-height: 1.6;
  overflow-x: hidden;
  cursor: none;
}

.cur { position:fixed; width:8px; height:8px; background:var(--white); border-radius:50%; pointer-events:none; z-index:9999; transform:translate(-50%,-50%); transition:transform .15s; }
.cur-r { position:fixed; width:32px; height:32px; border:1px solid rgba(255,255,255,0.25); border-radius:50%; pointer-events:none; z-index:9998; transform:translate(-50%,-50%); transition:width .2s,height .2s,border-color .2s; }

nav {
  position:fixed; top:0; width:100%; z-index:100;
  padding:1.8rem 3.5rem;
  display:flex; justify-content:space-between; align-items:center;
  background:linear-gradient(to bottom,rgba(10,10,10,0.95),transparent);
}
.nav-logo { font-family:var(--f-mono); font-size:.72rem; letter-spacing:.18em; text-transform:uppercase; color:var(--white); text-decoration:none; }
.nav-links { display:flex; gap:2.5rem; list-style:none; }
.nav-links a { color:rgba(255,255,255,0.4); text-decoration:none; font-family:var(--f-mono); font-size:.56rem; letter-spacing:.16em; text-transform:uppercase; transition:color .2s; }
.nav-links a:hover { color:var(--white); }

#hero {
  min-height:100vh; display:flex; flex-direction:column; justify-content:flex-end;
  padding:0 3.5rem 4.5rem; position:relative; overflow:hidden;
}
.hero-kicker { font-family:var(--f-mono); font-size:.56rem; letter-spacing:.22em; text-transform:uppercase; color:rgba(255,255,255,0.3); margin-bottom:2rem; opacity:0; animation:up .8s .3s forwards; }
.hero-h1 { font-family:var(--f-serif); font-size:clamp(4rem,10vw,10rem); font-weight:400; line-height:.92; letter-spacing:-.02em; margin-bottom:4rem; opacity:0; animation:up .9s .5s forwards; }
.hero-h1 em { font-style:italic; color:rgba(255,255,255,0.3); }
.hero-h1 .ghost { color:transparent; -webkit-text-stroke:1px rgba(255,255,255,0.15); }

.hero-foot { display:flex; justify-content:space-between; align-items:flex-end; border-top:1px solid var(--edge); padding-top:2rem; opacity:0; animation:up .9s .9s forwards; }
.hero-desc { max-width:360px; font-size:.85rem; color:var(--mid-2); line-height:1.8; }
.hero-desc span { display:block; margin-top:.6rem; font-family:var(--f-mono); font-size:.52rem; letter-spacing:.14em; text-transform:uppercase; color:rgba(255,255,255,0.22); }
.hero-cta { display:inline-flex; align-items:center; gap:.7rem; color:var(--white); text-decoration:none; font-family:var(--f-mono); font-size:.58rem; letter-spacing:.14em; text-transform:uppercase; border:1px solid var(--edge-3); padding:.9rem 1.8rem; transition:background .25s,color .25s; }
.hero-cta:hover { background:var(--white); color:var(--ink); }

.ticker { padding:1.2rem 0; border-top:1px solid var(--edge); border-bottom:1px solid var(--edge); overflow:hidden; white-space:nowrap; background:var(--ink-2); }
.ticker-inner { display:inline-block; animation:tick 28s linear infinite; }
.ticker-inner span { font-family:var(--f-mono); font-size:.56rem; letter-spacing:.2em; text-transform:uppercase; color:rgba(255,255,255,0.28); margin:0 2.5rem; }
.ticker-inner b { color:rgba(255,255,255,0.1); font-weight:400; }

section { padding:8rem 3.5rem; }
.s-label { font-family:var(--f-mono); font-size:.54rem; letter-spacing:.22em; text-transform:uppercase; color:rgba(255,255,255,0.28); margin-bottom:1.2rem; }
.s-title { font-family:var(--f-serif); font-size:clamp(2.8rem,5vw,5rem); font-weight:400; line-height:1.05; letter-spacing:-.01em; margin-bottom:4.5rem; }
.s-title em { font-style:italic; color:rgba(255,255,255,0.28); }

/* portfolio */
#portfolio { background:var(--ink-2); }

.pf-filter { display:flex; margin-bottom:3.5rem; border:1px solid var(--edge); width:fit-content; }
.pf-btn { font-family:var(--f-mono); font-size:.54rem; letter-spacing:.14em; text-transform:uppercase; padding:.7rem 1.4rem; background:none; border:none; color:rgba(255,255,255,0.28); cursor:none; transition:background .2s,color .2s; border-right:1px solid var(--edge); }
.pf-btn:last-child { border-right:none; }
.pf-btn.active,.pf-btn:hover { background:rgba(255,255,255,0.05); color:var(--white); }

.p-grid { display:grid; grid-template-columns:repeat(12,1fr); gap:2px; }
.p-item { position:relative; overflow:hidden; background:var(--ink-3); cursor:none; transition:opacity .35s; }
.p-item:nth-child(1){grid-column:span 7}
.p-item:nth-child(2){grid-column:span 5}
.p-item:nth-child(3){grid-column:span 5}
.p-item:nth-child(4){grid-column:span 7}
.p-item:nth-child(5){grid-column:span 4}
.p-item:nth-child(6){grid-column:span 4}
.p-item:nth-child(7){grid-column:span 4}
.p-item:nth-child(8){grid-column:span 8}
.p-item:nth-child(9){grid-column:span 4}

.p-thumb { aspect-ratio:4/3; display:flex; align-items:center; justify-content:center; position:relative; overflow:hidden; }
.p-bg { position:absolute; inset:0; transition:transform .7s cubic-bezier(.25,.46,.45,.94); }
.p-item:hover .p-bg { transform:scale(1.04); }
.t1{background:linear-gradient(145deg,#1a1a1a,#0e0e0e)}
.t2{background:linear-gradient(145deg,#141414,#1e1e1e)}
.t3{background:linear-gradient(145deg,#121212,#1c1c1c)}
.t4{background:linear-gradient(145deg,#181818,#0f0f0f)}
.t5{background:linear-gradient(145deg,#1f1f1f,#131313)}
.t6{background:linear-gradient(145deg,#111,#1a1a1a)}
.t7{background:linear-gradient(145deg,#161616,#0d0d0d)}
.t8{background:linear-gradient(145deg,#1b1b1b,#111)}
.t9{background:linear-gradient(145deg,#131313,#1e1e1e)}

.p-icon { position:relative; z-index:1; color:rgba(255,255,255,0.06); font-size:2rem; }
.p-over { position:absolute; inset:0; background:linear-gradient(to top,rgba(0,0,0,.88) 0%,rgba(0,0,0,.2) 50%,transparent 100%); opacity:0; transition:opacity .35s; display:flex; flex-direction:column; justify-content:flex-end; padding:1.5rem; }
.p-item:hover .p-over { opacity:1; }
.p-cat { font-family:var(--f-mono); font-size:.5rem; letter-spacing:.18em; text-transform:uppercase; color:rgba(255,255,255,0.45); margin-bottom:.3rem; }
.p-name { font-size:.95rem; color:var(--white); }
.p-bar { padding:.9rem 1.2rem; display:flex; justify-content:space-between; align-items:center; border-top:1px solid var(--edge); }
.p-type { font-family:var(--f-mono); font-size:.5rem; letter-spacing:.12em; text-transform:uppercase; color:rgba(255,255,255,0.22); }
.p-note { font-size:.68rem; color:rgba(255,255,255,0.1); font-style:italic; }

/* services */
#services { background:var(--ink); }
.svc-list { display:flex; flex-direction:column; border-top:1px solid var(--edge); }
.svc { display:grid; grid-template-columns:3rem 1fr 1.2fr auto; gap:3rem; align-items:start; padding:2.5rem 0; border-bottom:1px solid var(--edge); position:relative; transition:background .25s; }
.svc::after { content:''; position:absolute; left:0; bottom:-1px; height:1px; width:0; background:rgba(255,255,255,0.4); transition:width .5s ease; }
.svc:hover::after { width:100%; }
.svc:hover { background:rgba(255,255,255,0.02); }
.svc-num { font-family:var(--f-mono); font-size:.54rem; color:rgba(255,255,255,0.18); padding-top:.3rem; }
.svc-name { font-family:var(--f-serif); font-size:1.4rem; font-weight:400; line-height:1.2; }
.svc-desc { font-size:.82rem; color:var(--mid-2); line-height:1.85; }
.svc-tags { display:flex; flex-direction:column; gap:.4rem; align-items:flex-end; }
.stag { font-family:var(--f-mono); font-size:.48rem; letter-spacing:.1em; text-transform:uppercase; color:rgba(255,255,255,0.22); white-space:nowrap; }

/* about */
#about { background:var(--ink-2); }
.about-wrap { display:grid; grid-template-columns:1fr 1fr; gap:8rem; align-items:start; }
.about-img { aspect-ratio:3/4; background:var(--ink-3); border:1px solid var(--edge); position:relative; overflow:hidden; display:flex; align-items:center; justify-content:center; }
.about-ph { text-align:center; color:rgba(255,255,255,0.1); }
.about-ph p { font-family:var(--f-mono); font-size:.52rem; letter-spacing:.15em; text-transform:uppercase; margin-top:.6rem; }
.about-cap { position:absolute; bottom:0; left:0; right:0; padding:1.2rem 1.5rem; border-top:1px solid var(--edge); font-family:var(--f-mono); font-size:.52rem; letter-spacing:.12em; text-transform:uppercase; color:rgba(255,255,255,0.22); background:var(--ink-3); }
.about-txt .s-title { margin-bottom:1.5rem; }
.about-lead { font-size:1rem; color:rgba(255,255,255,0.58); line-height:1.85; margin-bottom:1.8rem; }
.about-body { font-size:.82rem; color:var(--mid-2); line-height:2; }

/* testimonials */
#testimonials { background:var(--ink); }
.t-grid { display:grid; grid-template-columns:repeat(3,1fr); gap:1px; background:var(--edge); }
.t-card { background:var(--ink-2); padding:2.5rem; transition:background .3s; }
.t-card:hover { background:var(--ink-3); }
.t-stars { letter-spacing:.06em; color:rgba(255,255,255,0.7); font-size:.68rem; margin-bottom:1.5rem; }
.t-q { font-family:var(--f-serif); font-size:3rem; line-height:.4; color:rgba(255,255,255,0.08); margin-bottom:1.2rem; font-style:italic; }
.t-text { font-size:.8rem; color:var(--mid-2); line-height:1.9; margin-bottom:2rem; font-style:italic; }
.t-author { display:flex; align-items:center; gap:.9rem; }
.t-av { width:34px; height:34px; border-radius:50%; background:var(--ink-4); border:1px solid var(--edge-2); display:flex; align-items:center; justify-content:center; font-family:var(--f-mono); font-size:.48rem; color:rgba(255,255,255,0.35); }
.t-n { font-size:.8rem; color:var(--white); }
.t-r { font-family:var(--f-mono); font-size:.5rem; letter-spacing:.08em; color:rgba(255,255,255,0.28); margin-top:.2rem; }

/* contact */
#contact { background:var(--ink-2); }
.c-wrap { display:grid; grid-template-columns:1fr 1.3fr; gap:8rem; }
.c-info .s-title { margin-bottom:1.5rem; }
.c-info p { font-size:.82rem; color:var(--mid-2); line-height:1.9; margin-bottom:3rem; }
.c-det { margin-bottom:1.8rem; }
.c-lbl { font-family:var(--f-mono); font-size:.5rem; letter-spacing:.18em; text-transform:uppercase; color:rgba(255,255,255,0.25); margin-bottom:.3rem; }
.c-val { font-size:.88rem; color:var(--white); }
.c-form { display:flex; flex-direction:column; gap:1.4rem; }
.f-g { display:flex; flex-direction:column; gap:.5rem; }
.f-row { display:grid; grid-template-columns:1fr 1fr; gap:1rem; }
label { font-family:var(--f-mono); font-size:.5rem; letter-spacing:.16em; text-transform:uppercase; color:rgba(255,255,255,0.28); }
input,select,textarea { background:var(--ink-3); border:1px solid var(--edge); color:var(--white); padding:.9rem 1.1rem; font-family:var(--f-sans); font-size:.85rem; font-weight:300; outline:none; transition:border-color .2s; width:100%; -webkit-appearance:none; }
input:focus,select:focus,textarea:focus { border-color:var(--edge-3); }
input::placeholder,textarea::placeholder { color:rgba(255,255,255,0.14); }
select option { background:var(--ink-3); }
textarea { resize:vertical; min-height:130px; }
.btn-sub { display:inline-flex; align-items:center; gap:.7rem; border:1px solid var(--edge-3); background:none; color:var(--white); padding:.9rem 2rem; font-family:var(--f-mono); font-size:.58rem; letter-spacing:.14em; text-transform:uppercase; cursor:none; align-self:flex-start; transition:background .25s,color .25s; }
.btn-sub:hover { background:var(--white); color:var(--ink); }

footer { padding:2.5rem 3.5rem; border-top:1px solid var(--edge); display:flex; justify-content:space-between; align-items:center; }
.f-logo { font-family:var(--f-mono); font-size:.68rem; letter-spacing:.18em; text-transform:uppercase; }
.f-copy { font-family:var(--f-mono); font-size:.5rem; letter-spacing:.1em; color:rgba(255,255,255,0.2); }
.f-links { display:flex; gap:2rem; list-style:none; }
.f-links a { font-family:var(--f-mono); font-size:.5rem; letter-spacing:.12em; text-transform:uppercase; color:rgba(255,255,255,0.22); text-decoration:none; transition:color .2s; }
.f-links a:hover { color:var(--white); }

.rev { opacity:0; transform:translateY(20px); transition:opacity .75s ease,transform .75s ease; }
.rev.in { opacity:1; transform:translateY(0); }

@keyframes up { from{opacity:0;transform:translateY(28px)} to{opacity:1;transform:translateY(0)} }
@keyframes tick { from{transform:translateX(0)} to{transform:translateX(-50%)} }

@media(max-width:768px){
  nav{padding:1.2rem 1.5rem}
  .nav-links{display:none}
  #hero{padding:0 1.5rem 3.5rem}
  section{padding:5rem 1.5rem}
  .p-grid .p-item:nth-child(n){grid-column:span 12}
  .about-wrap,.c-wrap{grid-template-columns:1fr;gap:3rem}
  .t-grid{grid-template-columns:1fr}
  .svc{grid-template-columns:2rem 1fr;gap:1.5rem}
  .svc-tags{display:none}
  footer{flex-direction:column;gap:1.2rem;text-align:center}
}
</style>
</head>
<body>

<div class="cur" id="cur"></div>
<div class="cur-r" id="cur-r"></div>

<nav>
  <a href="#hero" class="nav-logo">PLANNND.MEDIA</a>
  <ul class="nav-links">
    <li><a href="#portfolio">Portfolio</a></li>
    <li><a href="#services">Services</a></li>
    <li><a href="#about">About</a></li>
    <li><a href="#testimonials">Clients</a></li>
    <li><a href="#contact">Contact</a></li>
  </ul>
</nav>

<!-- HERO -->
<section id="hero">
  <p class="hero-kicker">Content · Photography · Vision</p>
  <h1 class="hero-h1">We create content<br><em>so you</em><br><span class="ghost">don't have to.</span></h1>
  <div class="hero-foot">
    <div class="hero-desc">
      Social-first, editorial, cinematic content and marketing assets.
      <span>Serving clients worldwide</span>
    </div>
    <a href="#contact" class="hero-cta">Start a project <svg width="12" height="12" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5"><path d="M5 12h14M12 5l7 7-7 7"/></svg></a>
  </div>
</section>

<!-- TICKER -->
<div class="ticker">
  <div class="ticker-inner">
    <span>Content Production</span><b>—</b><span>Editorial Photography</span><b>—</b><span>Drone Footage</span><b>—</b><span>Reels & Short-Form</span><b>—</b><span>Hospitality Content</span><b>—</b><span>Graphic Design</span><b>—</b><span>Usage Rights & Licensing</span><b>—</b><span>Social Media Management</span><b>—</b>
    <span>Content Production</span><b>—</b><span>Editorial Photography</span><b>—</b><span>Drone Footage</span><b>—</b><span>Reels & Short-Form</span><b>—</b><span>Hospitality Content</span><b>—</b><span>Graphic Design</span><b>—</b><span>Usage Rights & Licensing</span><b>—</b><span>Social Media Management</span><b>—</b>
  </div>
</div>

<!-- PORTFOLIO -->
<section id="portfolio">
  <div class="rev"><p class="s-label">Portfolio</p><h2 class="s-title">The work speaks<br><em>for itself.</em></h2></div>
  <div class="pf-filter rev">
    <button class="pf-btn active" onclick="filter('all',this)">All</button>
    <button class="pf-btn" onclick="filter('video',this)">Video & Drone</button>
    <button class="pf-btn" onclick="filter('photo',this)">Photography</button>
    <button class="pf-btn" onclick="filter('hospitality',this)">Hospitality</button>
  </div>
  <div class="p-grid">
    <div class="p-item rev" data-cat="video"><div class="p-thumb"><div class="p-bg t1"></div><div class="p-icon">▶</div><div class="p-over"><p class="p-cat">Drone · Cinematic</p><p class="p-name">Aerial Brand Campaign</p></div></div><div class="p-bar"><span class="p-type">4K Drone Video</span><span class="p-note">Add your video</span></div></div>
    <div class="p-item rev" data-cat="photo"><div class="p-thumb"><div class="p-bg t2"></div><div class="p-icon">◻</div><div class="p-over"><p class="p-cat">Editorial · Photo</p><p class="p-name">Brand Editorial Shoot</p></div></div><div class="p-bar"><span class="p-type">Photography</span><span class="p-note">Add your photo</span></div></div>
    <div class="p-item rev" data-cat="hospitality"><div class="p-thumb"><div class="p-bg t3"></div><div class="p-icon">◈</div><div class="p-over"><p class="p-cat">Hospitality · Airbnb</p><p class="p-name">Property Content Package</p></div></div><div class="p-bar"><span class="p-type">Photo + Video</span><span class="p-note">Add your work</span></div></div>
    <div class="p-item rev" data-cat="video"><div class="p-thumb"><div class="p-bg t4"></div><div class="p-icon">▶</div><div class="p-over"><p class="p-cat">Social · Reels</p><p class="p-name">Short-Form Campaign</p></div></div><div class="p-bar"><span class="p-type">Instagram Reels</span><span class="p-note">Add your reel</span></div></div>
    <div class="p-item rev" data-cat="photo"><div class="p-thumb"><div class="p-bg t5"></div><div class="p-icon">◻</div><div class="p-over"><p class="p-cat">Aerial · Photo</p><p class="p-name">Drone Photography Series</p></div></div><div class="p-bar"><span class="p-type">Aerial Photography</span><span class="p-note">Add your photo</span></div></div>
    <div class="p-item rev" data-cat="hospitality"><div class="p-thumb"><div class="p-bg t6"></div><div class="p-icon">◈</div><div class="p-over"><p class="p-cat">Hotel · Content</p><p class="p-name">Hotel Visual Identity</p></div></div><div class="p-bar"><span class="p-type">Hospitality Content</span><span class="p-note">Add your work</span></div></div>
    <div class="p-item rev" data-cat="video"><div class="p-thumb"><div class="p-bg t7"></div><div class="p-icon">▶</div><div class="p-over"><p class="p-cat">Corporate · Video</p><p class="p-name">Company Showreel</p></div></div><div class="p-bar"><span class="p-type">Brand Film</span><span class="p-note">Add your video</span></div></div>
    <div class="p-item rev" data-cat="photo"><div class="p-thumb"><div class="p-bg t8"></div><div class="p-icon">◻</div><div class="p-over"><p class="p-cat">Event · Photo</p><p class="p-name">Event Coverage</p></div></div><div class="p-bar"><span class="p-type">Photography</span><span class="p-note">Add your photo</span></div></div>
    <div class="p-item rev" data-cat="hospitality"><div class="p-thumb"><div class="p-bg t9"></div><div class="p-icon">◈</div><div class="p-over"><p class="p-cat">Airbnb · Photo + Drone</p><p class="p-name">Villa Content Package</p></div></div><div class="p-bar"><span class="p-type">Hospitality</span><span class="p-note">Add your work</span></div></div>
  </div>
</section>

<!-- SERVICES -->
<section id="services">
  <div class="rev"><p class="s-label">What We Offer</p><h2 class="s-title">Services.</h2></div>
  <div class="svc-list">

    <div class="svc rev">
      <span class="svc-num">01</span>
      <h3 class="svc-name">Content Production</h3>
      <p class="svc-desc">Complete visual content packages for brands, hotels, restaurants, and experiences. Cinematic video, aerial drone footage, editorial photography, and marketing assets — everything you need to show up with intention, with usage rights and licensing included.</p>
      <div class="svc-tags"><span class="stag">Video</span><span class="stag">Photography</span><span class="stag">Drone</span><span class="stag">Marketing Assets</span><span class="stag">Usage Rights</span></div>
    </div>

    <div class="svc rev">
      <span class="svc-num">02</span>
      <h3 class="svc-name">Reels & Short-Form</h3>
      <p class="svc-desc">Platform-native content built for performance. Instagram Reels, TikToks, YouTube Shorts — designed for reach, built for the algorithm, made to convert.</p>
      <div class="svc-tags"><span class="stag">Instagram</span><span class="stag">TikTok</span><span class="stag">Shorts</span></div>
    </div>

    <div class="svc rev">
      <span class="svc-num">03</span>
      <h3 class="svc-name">Social Media Management</h3>
      <p class="svc-desc">Strategy, scheduling, and execution for brands that need consistent, quality presence without running it themselves.</p>
      <div class="svc-tags"><span class="stag">Strategy</span><span class="stag">Scheduling</span><span class="stag">Analytics</span></div>
    </div>

    <div class="svc rev">
      <span class="svc-num">04</span>
      <h3 class="svc-name">Graphic Design</h3>
      <p class="svc-desc">Visual identities, marketing assets, social graphics — everything your brand needs to look as refined as it performs.</p>
      <div class="svc-tags"><span class="stag">Branding</span><span class="stag">Assets</span><span class="stag">Print</span></div>
    </div>

  </div>
</section>

<!-- ABOUT -->
<section id="about">
  <div class="about-wrap">
    <div class="about-img rev">
      <div class="about-ph"><div style="font-size:2.5rem">◻</div><p>Your photo here</p></div>
      <div class="about-cap">Valencia, Spain — Available Worldwide</div>
    </div>
    <div class="rev">
      <p class="s-label">The Story</p>
      <h2 class="s-title">Behind<br><em>the lens.</em></h2>
      <p class="about-lead">PLANNND.MEDIA was founded to help brands show up with intention, clarity, and strong visual identity.</p>
      <p class="about-body">We are a content-led creative studio working with brands, hotels, restaurants, and experiences that care about how they are seen online.<br><br>Our work is rooted in cinematic video, aerial drone footage, and editorial photography, created for brands that want to define how they appear across digital platforms. Every piece of content is built to reflect the atmosphere, energy, and identity of what a brand truly is.<br><br>We work with clients worldwide across hospitality, lifestyle, and experience-led brands, creating consistent content that elevates how they show up.</p>
    </div>
  </div>
</section>

<!-- TESTIMONIALS -->
<section id="testimonials">
  <div class="rev"><p class="s-label">Client Feedback</p><h2 class="s-title">What Clients<br><em>Say.</em></h2></div>
  <div class="t-grid">

    <div class="t-card rev">
      <div class="t-stars">★★★★★</div>
      <div class="t-q">"</div>
      <p class="t-text">Working with Plannnd was one of the best decisions we made for our listing. The content is stunning — we now use it across our website, social media, and Airbnb listing. Guests comment on it constantly before they even arrive.</p>
      <div class="t-author">
        <div class="t-av">RL</div>
        <div><div class="t-n">Roos & Luca V.</div><div class="t-r">Airbnb Hosts · Valencia</div></div>
      </div>
    </div>

    <div class="t-card rev">
      <div class="t-stars">★★★★★</div>
      <div class="t-q">"</div>
      <p class="t-text">Ela mou! I was sceptical at first — I run a Greek restaurant in Brooklyn, we are busy, we don't stop. But the content they made for us? Unbelievable. People come in and say they found us on Instagram. That never happened before. Worth every euro — or dollar, whatever.</p>
      <div class="t-author">
        <div class="t-av">NK</div>
        <div><div class="t-n">Nikos Karavelis</div><div class="t-r">Owner, Thálassa Kitchen · Brooklyn, NY</div></div>
      </div>
    </div>

    <div class="t-card rev">
      <div class="t-stars">★★★★★</div>
      <div class="t-q">"</div>
      <p class="t-text">The Airbnb content package was worth every cent. Our bookings increased noticeably after the new photos and video went live, and having full usage rights made everything so straightforward. I've already recommended Plannnd to three other hosts.</p>
      <div class="t-author">
        <div class="t-av">SM</div>
        <div><div class="t-n">Sofía Menchero</div><div class="t-r">Airbnb Superhost · Mallorca</div></div>
      </div>
    </div>

  </div>
</section>

<!-- CONTACT -->
<section id="contact">
  <div class="c-wrap">
    <div class="rev">
      <p class="s-label">Get in Touch</p>
      <h2 class="s-title">Let's Build<br><em>Something.</em></h2>
      <p>Got a project in mind? Whether it's a property content package, a brand campaign, or ongoing social media — let's talk.</p>
      <div class="c-det"><div class="c-lbl">Instagram</div><div class="c-val">@plannn.d</div></div>
      <div class="c-det"><div class="c-lbl">Based in</div><div class="c-val">Valencia, Spain</div></div>
      <div class="c-det"><div class="c-lbl">Available for</div><div class="c-val">Projects worldwide</div></div>
    </div>
    <form class="c-form rev" onsubmit="handleSubmit(event)">
      <div class="f-row">
        <div class="f-g"><label for="fn">Name</label><input type="text" id="fn" placeholder="Your name" required></div>
        <div class="f-g"><label for="co">Company</label><input type="text" id="co" placeholder="Brand or property"></div>
      </div>
      <div class="f-g"><label for="em">Email</label><input type="email" id="em" placeholder="your@email.com" required></div>
      <div class="f-g">
        <label for="sv">Service</label>
        <select id="sv">
          <option value="">What are you looking for?</option>
          <option>Content Production Package</option>
          <option>Hospitality Content (Airbnb / Hotel)</option>
          <option>Reels & Short-Form Content</option>
          <option>Social Media Management</option>
          <option>Graphic Design</option>
          <option>Full Package</option>
          <option>Not sure — let's talk</option>
        </select>
      </div>
      <div class="f-g"><label for="msg">Project Brief</label><textarea id="msg" placeholder="Tell me what you're working on — type of project, timeline, anything relevant..."></textarea></div>
      <button type="submit" class="btn-sub">Send Message <svg width="12" height="12" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5"><path d="M5 12h14M12 5l7 7-7 7"/></svg></button>
    </form>
  </div>
</section>

<footer>
  <div class="f-logo">PLANNND.MEDIA</div>
  <p class="f-copy">© 2025 PLANNND.MEDIA</p>
  <ul class="f-links"><li><a href="#portfolio">Portfolio</a></li><li><a href="#services">Services</a></li><li><a href="#contact">Contact</a></li></ul>
</footer>

<script>
const cur=document.getElementById('cur'),ring=document.getElementById('cur-r');
let mx=0,my=0,rx=0,ry=0;
document.addEventListener('mousemove',e=>{mx=e.clientX;my=e.clientY;cur.style.left=mx+'px';cur.style.top=my+'px';});
(function a(){rx+=(mx-rx)*.1;ry+=(my-ry)*.1;ring.style.left=rx+'px';ring.style.top=ry+'px';requestAnimationFrame(a)})();
document.querySelectorAll('a,button,.p-item,.svc').forEach(el=>{
  el.addEventListener('mouseenter',()=>{cur.style.transform='translate(-50%,-50%) scale(0)';ring.style.width='50px';ring.style.height='50px';ring.style.borderColor='rgba(255,255,255,0.5)';});
  el.addEventListener('mouseleave',()=>{cur.style.transform='translate(-50%,-50%) scale(1)';ring.style.width='32px';ring.style.height='32px';ring.style.borderColor='rgba(255,255,255,0.25)';});
});
const obs=new IntersectionObserver(entries=>entries.forEach((e,i)=>{if(e.isIntersecting){setTimeout(()=>e.target.classList.add('in'),i*60);obs.unobserve(e.target);}}),{threshold:.08,rootMargin:'0px 0px -50px 0px'});
document.querySelectorAll('.rev').forEach(el=>obs.observe(el));
function filter(cat,btn){
  document.querySelectorAll('.pf-btn').forEach(b=>b.classList.remove('active'));btn.classList.add('active');
  document.querySelectorAll('.p-item').forEach(item=>{item.style.opacity=cat==='all'||item.dataset.cat===cat?'1':'0.1';item.style.pointerEvents=cat==='all'||item.dataset.cat===cat?'auto':'none';});
}
function handleSubmit(e){
  e.preventDefault();const btn=e.target.querySelector('.btn-sub');
  btn.textContent='✓ Sent';btn.style.borderColor='rgba(255,255,255,0.5)';
  setTimeout(()=>{btn.innerHTML='Send Message <svg width="12" height="12" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5"><path d="M5 12h14M12 5l7 7-7 7"/></svg>';btn.style.borderColor='';e.target.reset();},3000);
}
</script>
</body>
</html>
