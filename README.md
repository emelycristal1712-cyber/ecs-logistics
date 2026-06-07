<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="description" content="ECS Logistics – Importador mayorista de bicicletas eléctricas, MTB, motos deportivas y scooters eléctricos. Entrega nacional 30-45 días. República Dominicana.">
<meta name="keywords" content="bicicletas electricas, importar bicicletas, mayorista bicicletas, ECS Logistics, mountain bike, scooter electrico, moto electrica, distribuidor bicicletas">
<title>ECS Logistics – Your Imports, Simplified</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Rajdhani:wght@400;500;600;700&family=Barlow:wght@300;400;500;600&family=Barlow+Condensed:wght@600;700&display=swap" rel="stylesheet">
<style>
  :root {
    --navy: #0a1628;
    --navy-mid: #0d2044;
    --navy-light: #122a5e;
    --blue: #1a4fa0;
    --blue-bright: #2563c8;
    --blue-accent: #3b82f6;
    --white: #ffffff;
    --off-white: #f0f4fa;
    --gray-light: #e2e8f0;
    --gray: #94a3b8;
    --text-muted: #64748b;
    --gold: #f59e0b;
    --success: #10b981;
  }
  * { margin:0; padding:0; box-sizing:border-box; }
  html { scroll-behavior: smooth; }
  body {
    font-family: 'Barlow', sans-serif;
    background: var(--white);
    color: var(--navy);
    overflow-x: hidden;
  }

  /* ─── NAV ─── */
  nav {
    position: fixed; top:0; left:0; right:0; z-index:1000;
    background: rgba(10,22,40,0.97);
    backdrop-filter: blur(12px);
    border-bottom: 1px solid rgba(37,99,200,0.3);
    padding: 0 5%;
    display: flex; align-items: center; justify-content: space-between;
    height: 70px;
  }
  .nav-logo {
    font-family: 'Rajdhani', sans-serif;
    font-size: 1.5rem; font-weight: 700;
    color: var(--white); letter-spacing: 2px;
    display: flex; align-items: center; gap: 10px;
    text-decoration: none;
  }
  .nav-logo span { color: var(--blue-accent); }
  .nav-logo-sub { font-size: 0.55rem; color: var(--gray); letter-spacing: 3px; display:block; line-height:1; font-weight:400; font-family:'Barlow',sans-serif; }
  .nav-links { display: flex; gap: 2rem; list-style: none; align-items: center; }
  .nav-links a {
    color: var(--gray-light); text-decoration: none;
    font-size: 0.85rem; font-weight: 500; letter-spacing: 1px;
    text-transform: uppercase; transition: color .2s;
  }
  .nav-links a:hover { color: var(--blue-accent); }
  .nav-cta {
    background: var(--blue-bright); color: var(--white)!important;
    padding: 8px 20px; border-radius: 4px;
    font-weight: 600!important; transition: background .2s!important;
  }
  .nav-cta:hover { background: var(--blue-accent)!important; }
  .nav-hamburger { display:none; flex-direction:column; gap:5px; cursor:pointer; }
  .nav-hamburger span { width:25px; height:2px; background:var(--white); display:block; transition:.3s; }

  /* ─── HERO ─── */
  #hero {
    min-height: 100vh;
    background: linear-gradient(135deg, var(--navy) 0%, var(--navy-mid) 50%, var(--navy-light) 100%);
    position: relative; overflow: hidden;
    display: flex; align-items: center;
    padding: 70px 5% 0;
  }
  .hero-bg-pattern {
    position:absolute; inset:0; opacity:0.04;
    background-image: repeating-linear-gradient(45deg, var(--blue-accent) 0, var(--blue-accent) 1px, transparent 0, transparent 50%);
    background-size: 30px 30px;
  }
  .hero-glow {
    position:absolute; top:-200px; right:-200px;
    width:700px; height:700px; border-radius:50%;
    background: radial-gradient(circle, rgba(37,99,200,0.3) 0%, transparent 70%);
    pointer-events:none;
  }
  .hero-glow2 {
    position:absolute; bottom:-200px; left:-100px;
    width:500px; height:500px; border-radius:50%;
    background: radial-gradient(circle, rgba(59,130,246,0.15) 0%, transparent 70%);
    pointer-events:none;
  }
  .hero-content { position:relative; z-index:2; max-width:700px; }
  .hero-badge {
    display: inline-flex; align-items:center; gap:8px;
    background: rgba(37,99,200,0.25); border: 1px solid rgba(59,130,246,0.4);
    color: var(--blue-accent); padding: 6px 16px; border-radius: 100px;
    font-size: 0.75rem; font-weight: 600; letter-spacing: 2px; text-transform: uppercase;
    margin-bottom: 1.5rem;
    animation: fadeInDown .8s ease both;
  }
  .hero-badge::before { content:''; width:6px; height:6px; border-radius:50%; background:var(--blue-accent); display:inline-block; animation: pulse 2s infinite; }
  @keyframes pulse { 0%,100%{opacity:1;transform:scale(1)} 50%{opacity:0.5;transform:scale(1.3)} }
  .hero-title {
    font-family: 'Rajdhani', sans-serif;
    font-size: clamp(2.8rem, 6vw, 5rem);
    font-weight: 700; line-height: 1.05;
    color: var(--white); margin-bottom: 1.5rem;
    animation: fadeInUp .8s ease .2s both;
  }
  .hero-title .accent { color: var(--blue-accent); }
  .hero-subtitle {
    font-size: 1.15rem; color: #9ab5d8; line-height: 1.7;
    margin-bottom: 2.5rem; font-weight: 300;
    animation: fadeInUp .8s ease .4s both;
    max-width: 550px;
  }
  .hero-actions {
    display: flex; gap: 1rem; flex-wrap: wrap;
    animation: fadeInUp .8s ease .6s both;
  }
  .btn-primary {
    display: inline-flex; align-items:center; gap:8px;
    background: var(--blue-bright); color: var(--white);
    padding: 14px 30px; border-radius: 6px;
    font-weight: 600; font-size: 0.95rem; text-decoration:none;
    transition: all .2s; border:none; cursor:pointer;
    letter-spacing: 0.5px;
  }
  .btn-primary:hover { background: var(--blue-accent); transform: translateY(-2px); box-shadow: 0 10px 30px rgba(37,99,200,0.4); }
  .btn-secondary {
    display: inline-flex; align-items:center; gap:8px;
    background: transparent; color: var(--white);
    padding: 14px 30px; border-radius: 6px;
    font-weight: 500; font-size: 0.95rem; text-decoration:none;
    transition: all .2s; border: 1px solid rgba(255,255,255,0.25); cursor:pointer;
  }
  .btn-secondary:hover { background: rgba(255,255,255,0.08); border-color: rgba(255,255,255,0.5); }
  .hero-stats {
    display: flex; gap: 3rem; margin-top: 4rem;
    animation: fadeInUp .8s ease .8s both;
    flex-wrap: wrap;
  }
  .hero-stat { text-align:left; }
  .hero-stat-number {
    font-family: 'Rajdhani', sans-serif;
    font-size: 2.2rem; font-weight: 700;
    color: var(--white); line-height:1;
  }
  .hero-stat-number .accent { color: var(--blue-accent); }
  .hero-stat-label { font-size: 0.78rem; color: var(--gray); text-transform:uppercase; letter-spacing:1px; margin-top:4px; }
  .hero-image-side {
    position:absolute; right:0; top:0; bottom:0; width:45%;
    display:flex; align-items:center; justify-content:flex-end;
  }
  .hero-img-wrapper {
    width:100%; height:100%;
    overflow:hidden;
    opacity:0.18;
  }
  .hero-img-wrapper img { width:100%; height:100%; object-fit:cover; object-position:center; }
  @keyframes fadeInDown { from{opacity:0;transform:translateY(-20px)} to{opacity:1;transform:translateY(0)} }
  @keyframes fadeInUp { from{opacity:0;transform:translateY(30px)} to{opacity:1;transform:translateY(0)} }

  /* ─── SECTIONS ─── */
  section { padding: 90px 5%; }
  .section-label {
    font-size: 0.72rem; font-weight: 700; letter-spacing: 3px;
    text-transform: uppercase; color: var(--blue-bright);
    display: block; margin-bottom: 0.8rem;
  }
  .section-title {
    font-family: 'Rajdhani', sans-serif;
    font-size: clamp(1.8rem, 4vw, 2.8rem);
    font-weight: 700; color: var(--navy);
    line-height: 1.15; margin-bottom: 1rem;
  }
  .section-title .accent { color: var(--blue-bright); }
  .section-desc { font-size: 1.05rem; color: var(--text-muted); line-height: 1.7; max-width: 600px; }
  .section-header { margin-bottom: 3.5rem; }
  .section-header.centered { text-align:center; }
  .section-header.centered .section-desc { margin: 0 auto; }

  /* ─── SERVICES BAR ─── */
  #servicios-bar {
    background: var(--navy);
    padding: 0;
  }
  .services-bar-inner {
    display: grid; grid-template-columns: repeat(4, 1fr);
    border-top: 3px solid var(--blue-bright);
  }
  .service-bar-item {
    padding: 2rem 1.5rem;
    border-right: 1px solid rgba(255,255,255,0.06);
    display: flex; flex-direction:column; gap:10px;
    transition: background .2s;
    cursor:default;
  }
  .service-bar-item:last-child { border-right:none; }
  .service-bar-item:hover { background: rgba(37,99,200,0.15); }
  .service-bar-icon {
    width:42px; height:42px; border-radius:8px;
    background: rgba(37,99,200,0.25);
    display:flex; align-items:center; justify-content:center;
    font-size:1.2rem;
  }
  .service-bar-title { font-family:'Rajdhani',sans-serif; font-weight:600; color:var(--white); font-size:1.05rem; letter-spacing:0.5px; }
  .service-bar-desc { font-size:0.8rem; color:var(--gray); line-height:1.5; }

  /* ─── CATALOGUE ─── */
  #catalogo { background: var(--off-white); }
  .cat-filter {
    display: flex; gap:.7rem; flex-wrap:wrap; margin-bottom:2.5rem;
  }
  .cat-btn {
    padding: 8px 20px; border-radius: 100px;
    border: 1.5px solid var(--gray-light);
    background: var(--white); color: var(--text-muted);
    font-size: 0.82rem; font-weight: 600; cursor:pointer;
    letter-spacing:0.5px; text-transform:uppercase;
    transition: all .2s;
  }
  .cat-btn:hover, .cat-btn.active {
    background: var(--navy); color: var(--white);
    border-color: var(--navy);
  }
  .products-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(310px, 1fr));
    gap: 1.5rem;
  }
  .product-card {
    background: var(--white);
    border-radius: 12px; overflow:hidden;
    border: 1px solid var(--gray-light);
    transition: all .3s;
    display: flex; flex-direction:column;
  }
  .product-card:hover { transform: translateY(-6px); box-shadow: 0 20px 50px rgba(10,22,40,0.12); border-color: var(--blue-accent); }
  .product-img {
    height: 220px; overflow:hidden;
    background: var(--navy);
    position:relative;
  }
  .product-img img { width:100%; height:100%; object-fit:cover; transition: transform .5s; }
  .product-card:hover .product-img img { transform: scale(1.06); }
  .product-badge {
    position:absolute; top:12px; left:12px;
    background: var(--blue-bright); color:var(--white);
    font-size:0.65rem; font-weight:700; letter-spacing:1.5px;
    text-transform:uppercase; padding:4px 10px; border-radius:4px;
  }
  .product-badge.green { background: var(--success); }
  .product-badge.gold { background: var(--gold); color: var(--navy); }
  .product-body { padding: 1.4rem; flex:1; display:flex; flex-direction:column; }
  .product-category { font-size:0.68rem; font-weight:700; letter-spacing:2px; text-transform:uppercase; color:var(--blue-bright); margin-bottom:.4rem; }
  .product-name { font-family:'Rajdhani',sans-serif; font-size:1.2rem; font-weight:700; color:var(--navy); margin-bottom:.6rem; line-height:1.2; }
  .product-desc { font-size:0.85rem; color:var(--text-muted); line-height:1.6; margin-bottom:1rem; }
  .product-specs { display:flex; flex-direction:column; gap:.3rem; margin-bottom:1.2rem; }
  .spec-row { display:flex; justify-content:space-between; align-items:center; padding:.3rem 0; border-bottom:1px solid var(--gray-light); }
  .spec-row:last-child { border-bottom:none; }
  .spec-label { font-size:0.75rem; color:var(--text-muted); font-weight:500; }
  .spec-val { font-size:0.8rem; color:var(--navy); font-weight:600; text-align:right; }
  .product-footer { margin-top:auto; padding-top:1rem; border-top:1px solid var(--gray-light); display:flex; justify-content:space-between; align-items:center; }
  .product-cta {
    display:inline-flex; align-items:center; gap:6px;
    background: var(--navy); color: var(--white);
    padding: 8px 18px; border-radius:6px;
    font-size:0.8rem; font-weight:600; text-decoration:none;
    transition: background .2s; letter-spacing:.5px;
  }
  .product-cta:hover { background: var(--blue-bright); }
  .product-cert { font-size:0.68rem; color:var(--gray); }

  /* ─── WHY ─── */
  #por-que { background: var(--white); }
  .why-grid { display:grid; grid-template-columns:repeat(auto-fill, minmax(260px, 1fr)); gap:1.5rem; }
  .why-card {
    padding:2rem; border-radius:10px;
    border: 1px solid var(--gray-light);
    transition: all .3s;
  }
  .why-card:hover { border-color: var(--blue-accent); box-shadow: 0 8px 30px rgba(37,99,200,0.1); }
  .why-icon { font-size:2rem; margin-bottom:1rem; display:block; }
  .why-title { font-family:'Rajdhani',sans-serif; font-size:1.15rem; font-weight:700; color:var(--navy); margin-bottom:.5rem; }
  .why-text { font-size:0.88rem; color:var(--text-muted); line-height:1.65; }

  /* ─── B2B ─── */
  #b2b {
    background: var(--navy);
    position:relative; overflow:hidden;
  }
  .b2b-bg {
    position:absolute; inset:0; opacity:0.04;
    background-image: repeating-linear-gradient(90deg, var(--blue-accent) 0, var(--blue-accent) 1px, transparent 0, transparent 80px);
  }
  .b2b-inner { position:relative; z-index:2; display:grid; grid-template-columns:1fr 1fr; gap:5rem; align-items:center; }
  .b2b-content .section-title { color:var(--white); }
  .b2b-content .section-desc { color:#9ab5d8; max-width:100%; }
  .b2b-features { display:flex; flex-direction:column; gap:1rem; margin:2rem 0; }
  .b2b-feature { display:flex; align-items:flex-start; gap:12px; }
  .b2b-feature-icon { width:28px; height:28px; border-radius:6px; background:rgba(59,130,246,0.2); display:flex; align-items:center; justify-content:center; font-size:.85rem; flex-shrink:0; margin-top:2px; }
  .b2b-feature-text h4 { font-size:.95rem; font-weight:600; color:var(--white); margin-bottom:2px; }
  .b2b-feature-text p { font-size:.82rem; color:#7a9abf; line-height:1.5; }
  .b2b-form-panel {
    background: rgba(255,255,255,0.05);
    border: 1px solid rgba(255,255,255,0.1);
    border-radius: 12px; padding: 2.5rem;
  }
  .b2b-form-title { font-family:'Rajdhani',sans-serif; font-size:1.3rem; font-weight:700; color:var(--white); margin-bottom:1.5rem; }
  .form-group { margin-bottom:1rem; }
  .form-group label { display:block; font-size:.78rem; font-weight:600; color:#9ab5d8; letter-spacing:.5px; margin-bottom:.4rem; text-transform:uppercase; }
  .form-group input, .form-group select, .form-group textarea {
    width:100%; padding:11px 14px;
    background: rgba(255,255,255,0.07); border: 1px solid rgba(255,255,255,0.12);
    border-radius:6px; color:var(--white); font-size:.9rem; font-family:'Barlow',sans-serif;
    transition: border-color .2s;
    appearance: none;
  }
  .form-group input::placeholder, .form-group textarea::placeholder { color: rgba(255,255,255,0.3); }
  .form-group input:focus, .form-group select:focus, .form-group textarea:focus { outline:none; border-color:var(--blue-accent); background:rgba(59,130,246,0.1); }
  .form-group select option { background:var(--navy-mid); color:var(--white); }
  .form-group textarea { resize:vertical; min-height:90px; }
  .form-row { display:grid; grid-template-columns:1fr 1fr; gap:.8rem; }
  .btn-form {
    width:100%; padding:13px; border:none; cursor:pointer;
    background: var(--blue-bright); color:var(--white);
    border-radius:6px; font-size:.95rem; font-weight:700;
    font-family:'Barlow',sans-serif; letter-spacing:.5px;
    transition: all .2s; margin-top:.5rem;
  }
  .btn-form:hover { background:var(--blue-accent); transform:translateY(-1px); }

  /* ─── TRACKING ─── */
  #seguimiento { background: var(--off-white); }
  .tracking-box {
    max-width:650px; margin:0 auto;
    background:var(--white); border-radius:12px;
    border: 1px solid var(--gray-light); padding:2.5rem;
  }
  .track-input-row { display:flex; gap:1rem; margin-bottom:1.5rem; }
  .track-input {
    flex:1; padding:12px 16px;
    border: 1.5px solid var(--gray-light); border-radius:6px;
    font-size:.95rem; font-family:'Barlow',sans-serif; color:var(--navy);
    transition: border-color .2s;
  }
  .track-input:focus { outline:none; border-color:var(--blue-accent); }
  .btn-track {
    padding:12px 24px; background:var(--navy); color:var(--white);
    border:none; border-radius:6px; font-size:.9rem; font-weight:600;
    cursor:pointer; transition:background .2s; white-space:nowrap;
    font-family:'Barlow',sans-serif;
  }
  .btn-track:hover { background:var(--blue-bright); }
  .tracking-steps { display:flex; flex-direction:column; gap:.5rem; }
  .tracking-step { display:flex; align-items:center; gap:14px; padding:.8rem 0; position:relative; }
  .tracking-step::before { content:''; position:absolute; left:15px; top:50%; bottom:-50%; width:2px; background:var(--gray-light); z-index:0; }
  .tracking-step:last-child::before { display:none; }
  .step-dot { width:32px; height:32px; border-radius:50%; border:2px solid var(--gray-light); background:var(--white); display:flex; align-items:center; justify-content:center; font-size:.8rem; z-index:1; flex-shrink:0; font-weight:700; color:var(--gray); }
  .step-dot.done { background:var(--success); border-color:var(--success); color:var(--white); }
  .step-dot.active { background:var(--blue-bright); border-color:var(--blue-bright); color:var(--white); animation: pulse 2s infinite; }
  .step-info h4 { font-size:.9rem; font-weight:600; color:var(--navy); }
  .step-info p { font-size:.78rem; color:var(--text-muted); }

  /* ─── NOSOTROS ─── */
  #nosotros { background:var(--white); }
  .about-grid { display:grid; grid-template-columns:1fr 1fr; gap:5rem; align-items:center; }
  .about-img-block { position:relative; }
  .about-img-main {
    width:100%; border-radius:12px; overflow:hidden;
    aspect-ratio: 4/3;
    background: var(--navy-mid);
  }
  .about-img-main img { width:100%; height:100%; object-fit:cover; }
  .about-img-badge {
    position:absolute; bottom:-20px; right:-20px;
    background:var(--blue-bright); color:var(--white);
    border-radius:10px; padding:1.2rem 1.5rem;
    text-align:center; box-shadow:0 10px 30px rgba(37,99,200,0.35);
  }
  .about-img-badge-num { font-family:'Rajdhani',sans-serif; font-size:2rem; font-weight:700; line-height:1; }
  .about-img-badge-txt { font-size:.72rem; font-weight:500; letter-spacing:1px; text-transform:uppercase; opacity:.85; }
  .about-content { }
  .about-values { display:flex; flex-direction:column; gap:.8rem; margin-top:2rem; }
  .about-value { display:flex; align-items:flex-start; gap:12px; }
  .about-value-dot { width:8px; height:8px; border-radius:50%; background:var(--blue-bright); margin-top:7px; flex-shrink:0; }
  .about-value-text h4 { font-size:.95rem; font-weight:600; color:var(--navy); margin-bottom:2px; }
  .about-value-text p { font-size:.85rem; color:var(--text-muted); line-height:1.5; }

  /* ─── BLOG ─── */
  #blog { background:var(--off-white); }
  .blog-grid { display:grid; grid-template-columns:repeat(auto-fill, minmax(300px, 1fr)); gap:1.5rem; }
  .blog-card {
    background:var(--white); border-radius:10px; overflow:hidden;
    border:1px solid var(--gray-light); transition:all .3s;
  }
  .blog-card:hover { transform:translateY(-4px); box-shadow:0 12px 35px rgba(10,22,40,0.1); }
  .blog-img { height:180px; overflow:hidden; background:var(--navy); }
  .blog-img img { width:100%; height:100%; object-fit:cover; transition:transform .5s; }
  .blog-card:hover .blog-img img { transform:scale(1.05); }
  .blog-body { padding:1.3rem; }
  .blog-tag { font-size:.65rem; font-weight:700; letter-spacing:2px; text-transform:uppercase; color:var(--blue-bright); margin-bottom:.4rem; display:block; }
  .blog-title { font-family:'Rajdhani',sans-serif; font-size:1.05rem; font-weight:700; color:var(--navy); margin-bottom:.5rem; line-height:1.3; }
  .blog-excerpt { font-size:.82rem; color:var(--text-muted); line-height:1.6; }
  .blog-meta { display:flex; align-items:center; gap:8px; margin-top:1rem; padding-top:.8rem; border-top:1px solid var(--gray-light); font-size:.72rem; color:var(--gray); }

  /* ─── CONTACT ─── */
  #contacto { background:var(--navy); position:relative; overflow:hidden; }
  .contact-bg { position:absolute; inset:0; opacity:0.03; background-image:repeating-linear-gradient(45deg, var(--blue-accent) 0, var(--blue-accent) 1px, transparent 0, transparent 40px); background-size:40px 40px; }
  .contact-inner { position:relative; z-index:2; display:grid; grid-template-columns:1fr 1fr; gap:5rem; align-items:start; }
  .contact-info .section-title { color:var(--white); }
  .contact-info .section-desc { color:#9ab5d8; max-width:100%; }
  .contact-cards { display:flex; flex-direction:column; gap:1rem; margin-top:2rem; }
  .contact-card { display:flex; align-items:center; gap:14px; padding:1rem 1.2rem; background:rgba(255,255,255,0.05); border:1px solid rgba(255,255,255,0.08); border-radius:8px; transition:background .2s; text-decoration:none; }
  .contact-card:hover { background:rgba(37,99,200,0.2); }
  .contact-card-icon { width:38px; height:38px; border-radius:8px; background:rgba(59,130,246,0.2); display:flex; align-items:center; justify-content:center; font-size:1rem; flex-shrink:0; }
  .contact-card-info h4 { font-size:.85rem; font-weight:600; color:var(--white); margin-bottom:2px; }
  .contact-card-info p { font-size:.8rem; color:#7a9abf; }
  .social-row { display:flex; gap:.7rem; margin-top:1.5rem; }
  .social-btn { width:38px; height:38px; border-radius:8px; background:rgba(255,255,255,0.07); border:1px solid rgba(255,255,255,0.12); display:flex; align-items:center; justify-content:center; font-size:.9rem; color:var(--white); text-decoration:none; transition:all .2s; }
  .social-btn:hover { background:var(--blue-bright); border-color:var(--blue-bright); }
  .contact-form-panel { background:rgba(255,255,255,0.05); border:1px solid rgba(255,255,255,0.1); border-radius:12px; padding:2.5rem; }

  /* ─── FOOTER ─── */
  footer {
    background: #050e1d;
    padding: 3rem 5% 1.5rem;
    border-top: 1px solid rgba(255,255,255,0.06);
  }
  .footer-top { display:grid; grid-template-columns:2fr 1fr 1fr 1fr; gap:3rem; margin-bottom:2.5rem; }
  .footer-brand .nav-logo { display:inline-flex; margin-bottom:1rem; font-size:1.3rem; }
  .footer-brand p { font-size:.83rem; color:#5a7a9e; line-height:1.65; max-width:280px; }
  .footer-col h4 { font-family:'Rajdhani',sans-serif; font-size:.95rem; font-weight:700; color:var(--white); letter-spacing:1px; margin-bottom:1rem; text-transform:uppercase; }
  .footer-col ul { list-style:none; display:flex; flex-direction:column; gap:.5rem; }
  .footer-col ul li a { font-size:.82rem; color:#5a7a9e; text-decoration:none; transition:color .2s; }
  .footer-col ul li a:hover { color:var(--blue-accent); }
  .footer-bottom { border-top:1px solid rgba(255,255,255,0.06); padding-top:1.5rem; display:flex; justify-content:space-between; align-items:center; flex-wrap:wrap; gap:.5rem; }
  .footer-bottom p { font-size:.75rem; color:#3a5a7a; }

  /* ─── WHATSAPP FLOAT ─── */
  .whatsapp-float {
    position:fixed; bottom:25px; right:25px; z-index:9999;
    width:56px; height:56px; border-radius:50%;
    background: #25d366; color:var(--white);
    display:flex; align-items:center; justify-content:center;
    font-size:1.5rem; text-decoration:none;
    box-shadow: 0 6px 25px rgba(37,211,102,0.5);
    animation: floatBounce 3s ease-in-out infinite;
    transition: transform .2s;
  }
  .whatsapp-float:hover { transform: scale(1.1); }
  @keyframes floatBounce { 0%,100%{transform:translateY(0)} 50%{transform:translateY(-6px)} }

  /* ─── RESPONSIVE ─── */
  @media (max-width: 1024px) {
    .b2b-inner, .about-grid, .contact-inner { grid-template-columns:1fr; gap:3rem; }
    .footer-top { grid-template-columns:1fr 1fr; gap:2rem; }
    .hero-image-side { display:none; }
    .services-bar-inner { grid-template-columns:repeat(2,1fr); }
  }
  @media (max-width: 768px) {
    .nav-links { display:none; }
    .nav-hamburger { display:flex; }
    .nav-links.open { display:flex; flex-direction:column; position:fixed; top:70px; left:0; right:0; background:var(--navy); padding:2rem; gap:1.5rem; border-bottom:1px solid rgba(255,255,255,0.1); }
    .hero-stats { gap:1.5rem; }
    .services-bar-inner { grid-template-columns:1fr; }
    .footer-top { grid-template-columns:1fr; }
    .form-row { grid-template-columns:1fr; }
    .about-img-badge { position:static; margin-top:1rem; display:inline-flex; gap:1rem; align-items:center; }
    .track-input-row { flex-direction:column; }
  }

  /* ─── CART SIDEBAR ─── */
  .cart-overlay { position:fixed; inset:0; background:rgba(0,0,0,0.5); z-index:2000; opacity:0; pointer-events:none; transition:opacity .3s; }
  .cart-overlay.open { opacity:1; pointer-events:all; }
  .cart-sidebar {
    position:fixed; right:0; top:0; bottom:0; width:380px; max-width:95vw;
    background:var(--white); z-index:2001;
    transform:translateX(100%); transition:transform .35s ease;
    display:flex; flex-direction:column; box-shadow:-10px 0 40px rgba(0,0,0,0.2);
  }
  .cart-sidebar.open { transform:translateX(0); }
  .cart-header { padding:1.5rem; border-bottom:1px solid var(--gray-light); display:flex; justify-content:space-between; align-items:center; }
  .cart-header h3 { font-family:'Rajdhani',sans-serif; font-size:1.2rem; font-weight:700; color:var(--navy); }
  .cart-close { background:none; border:none; font-size:1.3rem; cursor:pointer; color:var(--text-muted); }
  .cart-items { flex:1; overflow-y:auto; padding:1rem 1.5rem; }
  .cart-empty { text-align:center; padding:3rem 1rem; color:var(--text-muted); }
  .cart-empty-icon { font-size:3rem; margin-bottom:1rem; opacity:.4; }
  .cart-item { display:flex; gap:12px; padding:1rem 0; border-bottom:1px solid var(--gray-light); }
  .cart-item-info { flex:1; }
  .cart-item-info h4 { font-size:.88rem; font-weight:600; color:var(--navy); }
  .cart-item-info p { font-size:.78rem; color:var(--text-muted); margin-top:2px; }
  .cart-item-remove { background:none; border:none; color:var(--gray); cursor:pointer; font-size:1rem; padding:0; }
  .cart-item-qty { display:flex; align-items:center; gap:8px; margin-top:6px; }
  .qty-btn { width:24px; height:24px; border-radius:4px; border:1px solid var(--gray-light); background:var(--white); cursor:pointer; font-size:.85rem; display:flex; align-items:center; justify-content:center; }
  .qty-num { font-size:.85rem; font-weight:600; color:var(--navy); min-width:20px; text-align:center; }
  .cart-footer { padding:1.5rem; border-top:1px solid var(--gray-light); }
  .cart-footer-note { font-size:.78rem; color:var(--text-muted); margin-bottom:1rem; line-height:1.5; }
  .btn-cart-checkout { width:100%; padding:13px; background:var(--navy); color:var(--white); border:none; border-radius:6px; font-size:.95rem; font-weight:700; cursor:pointer; font-family:'Barlow',sans-serif; transition:background .2s; }
  .btn-cart-checkout:hover { background:var(--blue-bright); }
  .cart-btn-nav { background:none; border:none; cursor:pointer; color:var(--white); font-size:1.2rem; position:relative; padding:5px; }
  .cart-count { position:absolute; top:-4px; right:-4px; width:16px; height:16px; border-radius:50%; background:var(--blue-accent); color:var(--white); font-size:.62rem; font-weight:700; display:flex; align-items:center; justify-content:center; }

  /* Notification toast */
  .toast { position:fixed; bottom:90px; right:25px; background:var(--navy); color:var(--white); padding:10px 18px; border-radius:8px; font-size:.85rem; font-weight:500; z-index:3000; transform:translateY(20px); opacity:0; transition:all .3s; pointer-events:none; box-shadow:0 6px 20px rgba(0,0,0,0.3); }
  .toast.show { transform:translateY(0); opacity:1; }
</style>
</head>
<body>

<!-- WHATSAPP FLOAT -->
<a href="https://wa.me/18295623551" target="_blank" class="whatsapp-float" title="WhatsApp ECS Logistics">
  <svg width="26" height="26" viewBox="0 0 24 24" fill="currentColor"><path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347m-5.421 7.403h-.004a9.87 9.87 0 01-5.031-1.378l-.361-.214-3.741.982.998-3.648-.235-.374a9.86 9.86 0 01-1.51-5.26c.001-5.45 4.436-9.884 9.888-9.884 2.64 0 5.122 1.03 6.988 2.898a9.825 9.825 0 012.893 6.994c-.003 5.45-4.437 9.884-9.885 9.884m8.413-18.297A11.815 11.815 0 0012.05 0C5.495 0 .16 5.335.157 11.892c0 2.096.547 4.142 1.588 5.945L.057 24l6.305-1.654a11.882 11.882 0 005.683 1.448h.005c6.554 0 11.89-5.335 11.893-11.893a11.821 11.821 0 00-3.48-8.413z"/></svg>
</a>

<!-- TOAST -->
<div class="toast" id="toast"></div>

<!-- CART OVERLAY -->
<div class="cart-overlay" id="cartOverlay" onclick="closeCart()"></div>
<div class="cart-sidebar" id="cartSidebar">
  <div class="cart-header">
    <h3>🛒 Carrito de Pedido</h3>
    <button class="cart-close" onclick="closeCart()">✕</button>
  </div>
  <div class="cart-items" id="cartItems">
    <div class="cart-empty">
      <div class="cart-empty-icon">🚲</div>
      <p>Tu carrito está vacío.<br>Agrega productos del catálogo.</p>
    </div>
  </div>
  <div class="cart-footer" id="cartFooter" style="display:none">
    <p class="cart-footer-note">⚠️ Pedido mínimo: 30 unidades por modelo. Los precios se cotizan según modelo y cantidad. Te contactaremos en menos de 24 horas.</p>
    <button class="btn-cart-checkout" onclick="sendOrder()">Solicitar Cotización →</button>
  </div>
</div>

<!-- NAV -->
<nav>
  <a href="#hero" class="nav-logo">
    ECS <span>LOGISTICS</span>
    <span class="nav-logo-sub">YOUR IMPORTS, SIMPLIFIED</span>
  </a>
  <ul class="nav-links" id="navLinks">
    <li><a href="#catalogo">Catálogo</a></li>
    <li><a href="#b2b">B2B</a></li>
    <li><a href="#seguimiento">Seguimiento</a></li>
    <li><a href="#nosotros">Nosotros</a></li>
    <li><a href="#blog">Blog</a></li>
    <li><a href="#contacto">Contacto</a></li>
    <li><a href="#contacto" class="nav-cta">Cotizar Ahora</a></li>
    <li>
      <button class="cart-btn-nav" onclick="openCart()" title="Ver carrito">
        🛒 <span class="cart-count" id="cartCount">0</span>
      </button>
    </li>
  </ul>
  <div class="nav-hamburger" onclick="toggleNav()">
    <span></span><span></span><span></span>
  </div>
</nav>

<!-- HERO -->
<section id="hero">
  <div class="hero-bg-pattern"></div>
  <div class="hero-glow"></div>
  <div class="hero-glow2"></div>
  <div class="hero-content">
    <div class="hero-badge">🌎 Entrega Nacional · República Dominicana</div>
    <h1 class="hero-title">
      Movilidad Eléctrica<br>
      <span class="accent">sin Fronteras</span>
    </h1>
    <p class="hero-subtitle">
      Importamos bicicletas eléctricas, MTB, motos deportivas y scooters directamente para tu negocio. Calidad de fábrica, entrega en 30–45 días.
    </p>
    <div class="hero-actions">
      <a href="#catalogo" class="btn-primary">Ver Catálogo Completo →</a>
      <a href="#b2b" class="btn-secondary">Área Mayorista B2B</a>
    </div>
    <div class="hero-stats">
      <div class="hero-stat">
        <div class="hero-stat-number">30<span class="accent">+</span></div>
        <div class="hero-stat-label">Modelos disponibles</div>
      </div>
      <div class="hero-stat">
        <div class="hero-stat-number">45<span class="accent">d</span></div>
        <div class="hero-stat-label">Entrega máxima</div>
      </div>
      <div class="hero-stat">
        <div class="hero-stat-number">100<span class="accent">%</span></div>
        <div class="hero-stat-label">Certificados CE/EEC</div>
      </div>
      <div class="hero-stat">
        <div class="hero-stat-number">B2<span class="accent">B</span></div>
        <div class="hero-stat-label">Mayoristas & flotas</div>
      </div>
    </div>
  </div>
  <div class="hero-image-side">
    <div class="hero-img-wrapper">
      <img src="https://images.unsplash.com/photo-1558618666-fcd25c85cd64?w=800&q=80" alt="Movilidad eléctrica">
    </div>
  </div>
</section>

<!-- SERVICES BAR -->
<div id="servicios-bar">
  <div class="services-bar-inner">
    <div class="service-bar-item">
      <div class="service-bar-icon">⚡</div>
      <div class="service-bar-title">Eléctricas Urbanas</div>
      <div class="service-bar-desc">E-bikes 350W–1500W, scooters y motos sport para ciudad y ruta</div>
    </div>
    <div class="service-bar-item">
      <div class="service-bar-icon">🏔️</div>
      <div class="service-bar-title">Mountain Bike MTB</div>
      <div class="service-bar-desc">Aluminio alloy, frenos disco, suspensión aceite, 21–30 velocidades</div>
    </div>
    <div class="service-bar-item">
      <div class="service-bar-icon">🏍️</div>
      <div class="service-bar-title">Motos Deportivas</div>
      <div class="service-bar-desc">Moto eléctrica RUSION 3000W, 85 km/h, certificación EEC</div>
    </div>
    <div class="service-bar-item">
      <div class="service-bar-icon">📦</div>
      <div class="service-bar-title">Logística Integral</div>
      <div class="service-bar-desc">Importación simplificada, tracking en tiempo real, entrega nacional</div>
    </div>
  </div>
</div>

<!-- CATÁLOGO -->
<section id="catalogo">
  <div class="section-header">
    <span class="section-label">Catálogo 2026</span>
    <h2 class="section-title">Nuestra Línea de <span class="accent">Productos</span></h2>
    <p class="section-desc">Desde bicicletas urbanas eléctricas hasta motos deportivas de alto rendimiento. Todos los productos con certificaciones internacionales.</p>
  </div>

  <div class="cat-filter">
    <button class="cat-btn active" onclick="filterCat('all', this)">Todos</button>
    <button class="cat-btn" onclick="filterCat('electrica', this)">⚡ Eléctricas</button>
    <button class="cat-btn" onclick="filterCat('mtb', this)">🏔️ MTB</button>
    <button class="cat-btn" onclick="filterCat('moto', this)">🏍️ Motos</button>
    <button class="cat-btn" onclick="filterCat('ruta', this)">🚴 Ruta</button>
    <button class="cat-btn" onclick="filterCat('lineas', this)">🏷️ Líneas ECS</button>
  </div>

  <div class="products-grid" id="productsGrid">

    <!-- ESA Urbana -->
    <div class="product-card" data-cat="electrica">
      <div class="product-img">
        <img src="https://images.unsplash.com/photo-1571068316344-75bc76f77890?w=600&q=80" alt="Bicicleta eléctrica urbana motor brushless">
        <span class="product-badge">⚡ Eléctrica</span>
      </div>
      <div class="product-body">
        <div class="product-category">Eléctrica Urbana</div>
        <div class="product-name">ESA — Bicicleta Eléctrica Urbana</div>
        <p class="product-desc">Suspensión delantera hidráulica, frenos de tambor, iluminación LED y señal de giro. Hasta 45 km por carga.</p>
        <div class="product-specs">
          <div class="spec-row"><span class="spec-label">Motor</span><span class="spec-val">350W / 500W Brushless</span></div>
          <div class="spec-row"><span class="spec-label">Batería litio</span><span class="spec-val">48V 20AH / 30AH</span></div>
          <div class="spec-row"><span class="spec-label">Autonomía</span><span class="spec-val">25–45 km/carga</span></div>
          <div class="spec-row"><span class="spec-label">Velocidad máx.</span><span class="spec-val">35–40 km/h</span></div>
          <div class="spec-row"><span class="spec-label">Frenos</span><span class="spec-val">Tambor del. y tras.</span></div>
        </div>
        <div class="product-footer">
          <span class="product-cert">CE · EN15194 · COC</span>
          <button class="product-cta" onclick="addToCart('ESA Eléctrica Urbana')">+ Carrito</button>
        </div>
      </div>
    </div>

    <!-- Golden Eagle -->
    <div class="product-card" data-cat="electrica">
      <div class="product-img">
        <img src="https://images.unsplash.com/photo-1593764592116-bfb2a97c642a?w=600&q=80" alt="Motor eléctrico bicicleta compacta brushless">
        <span class="product-badge green">Compacta</span>
      </div>
      <div class="product-body">
        <div class="product-category">Eléctrica Compacta 14"</div>
        <div class="product-name">Golden Eagle — E-Bike 14"</div>
        <p class="product-desc">Motor brushless silencioso, ideal para última milla. Producción de hasta 8,000 unidades/mes. Múltiples certificaciones.</p>
        <div class="product-specs">
          <div class="spec-row"><span class="spec-label">Motor</span><span class="spec-val">350–500W Brushless</span></div>
          <div class="spec-row"><span class="spec-label">Batería</span><span class="spec-val">48V 12Ah / 20Ah</span></div>
          <div class="spec-row"><span class="spec-label">Autonomía</span><span class="spec-val">30–60 km/carga</span></div>
          <div class="spec-row"><span class="spec-label">Carga máx.</span><span class="spec-val">180 kg</span></div>
          <div class="spec-row"><span class="spec-label">OEM/ODM</span><span class="spec-val">Disponible</span></div>
        </div>
        <div class="product-footer">
          <span class="product-cert">CE · EEC · ISO · EPA</span>
          <button class="product-cta" onclick="addToCart('Golden Eagle E-Bike 14&quot;')">+ Carrito</button>
        </div>
      </div>
    </div>

    <!-- EMA Fat Tire -->
    <div class="product-card" data-cat="electrica">
      <div class="product-img">
        <img src="https://images.unsplash.com/photo-1591637333184-19aa84b3e01f?w=600&q=80" alt="E-bike fat tire motor 1000W todo terreno">
        <span class="product-badge gold">1000W</span>
      </div>
      <div class="product-body">
        <div class="product-category">E-Bike Alto Rendimiento</div>
        <div class="product-name">EMA — Fat Tire E-Bike 1000W</div>
        <p class="product-desc">Neumáticos fat que dominan playa, barro, asfalto o montaña. Hasta 80 km de autonomía con batería de litio 72V30AH.</p>
        <div class="product-specs">
          <div class="spec-row"><span class="spec-label">Motor</span><span class="spec-val">1000W / 1200W / 1500W</span></div>
          <div class="spec-row"><span class="spec-label">Batería litio</span><span class="spec-val">60V–72V, 20–30AH</span></div>
          <div class="spec-row"><span class="spec-label">Autonomía</span><span class="spec-val">50–80 km</span></div>
          <div class="spec-row"><span class="spec-label">Velocidad máx.</span><span class="spec-val">40–45 km/h</span></div>
          <div class="spec-row"><span class="spec-label">Neumáticos</span><span class="spec-val">3.00-10 Fat Vacuum</span></div>
        </div>
        <div class="product-footer">
          <span class="product-cert">CE · Brushless</span>
          <button class="product-cta" onclick="addToCart('EMA Fat Tire 1000W')">+ Carrito</button>
        </div>
      </div>
    </div>

    <!-- Scooter Eléctrico -->
    <div class="product-card" data-cat="electrica">
      <div class="product-img">
        <img src="https://images.unsplash.com/photo-1558981806-ec527fa84c39?w=600&q=80" alt="Scooter eléctrico pasola urbana 60V deportiva">
        <span class="product-badge">⚡ 60V</span>
      </div>
      <div class="product-body">
        <div class="product-category">Scooter Eléctrico Urbano</div>
        <div class="product-name">EMA — Scooter Eléctrico 60V</div>
        <p class="product-desc">Estilo moderno con potencia de 501–1000W y 60V. Look deportivo perfecto para commuting urbano. 50,000 unidades/año.</p>
        <div class="product-specs">
          <div class="spec-row"><span class="spec-label">Potencia</span><span class="spec-val">501–1000W (esp. 1000W)</span></div>
          <div class="spec-row"><span class="spec-label">Voltaje</span><span class="spec-val">60V</span></div>
          <div class="spec-row"><span class="spec-label">Faros</span><span class="spec-val">LED integrados</span></div>
          <div class="spec-row"><span class="spec-label">Pendiente</span><span class="spec-val">30 grados</span></div>
          <div class="spec-row"><span class="spec-label">Producción</span><span class="spec-val">50,000 uds/año</span></div>
        </div>
        <div class="product-footer">
          <span class="product-cert">CE</span>
          <button class="product-cta" onclick="addToCart('Scooter Eléctrico 60V')">+ Carrito</button>
        </div>
      </div>
    </div>

    <!-- MTB LWBI -->
    <div class="product-card" data-cat="mtb">
      <div class="product-img">
        <img src="https://images.unsplash.com/photo-1544191696-102dbdaeeaa0?w=600&q=80" alt="Mountain bike MTB aluminio suspensión aceite frenos disco">
        <span class="product-badge">🏔️ MTB</span>
      </div>
      <div class="product-body">
        <div class="product-category">Mountain Bike 27.5"</div>
        <div class="product-name">LWBI-2-5 — Mountain Bike 27.5"</div>
        <p class="product-desc">Cuadro de aluminio, suspensión delantera de aceite y frenos de disco mecánico. Para senderos exigentes y terrenos irregulares.</p>
        <div class="product-specs">
          <div class="spec-row"><span class="spec-label">Rueda</span><span class="spec-val">12–28 pulg. disponibles</span></div>
          <div class="spec-row"><span class="spec-label">Velocidades</span><span class="spec-val">11–30 velocidades</span></div>
          <div class="spec-row"><span class="spec-label">Frenos</span><span class="spec-val">Disco mecánico</span></div>
          <div class="spec-row"><span class="spec-label">Suspensión</span><span class="spec-val">Delantera de aceite</span></div>
          <div class="spec-row"><span class="spec-label">Diseño</span><span class="spec-val">Rígido premium</span></div>
        </div>
        <div class="product-footer">
          <span class="product-cert">Make-to-Order</span>
          <button class="product-cta" onclick="addToCart('MTB LWBI-2-5 27.5&quot;')">+ Carrito</button>
        </div>
      </div>
    </div>

    <!-- FR-2706 MTB Aluminio -->
    <div class="product-card" data-cat="mtb">
      <div class="product-img">
        <img src="https://images.unsplash.com/photo-1507035895480-2b3156c31fc8?w=600&q=80" alt="MTB aluminio full spec 21 velocidades bicicleta montaña">
        <span class="product-badge green">21 VEL</span>
      </div>
      <div class="product-body">
        <div class="product-category">MTB Aluminio Full Spec</div>
        <div class="product-name">FR-2706 — MTB 27.5" Aluminio</div>
        <p class="product-desc">Cuadro, horquilla, manillar, sillín y llantas en aluminio. Frenos de disco mecánico y suspensión de aceite para máximo control.</p>
        <div class="product-specs">
          <div class="spec-row"><span class="spec-label">Cuadro</span><span class="spec-val">27.5" Aluminio Alloy</span></div>
          <div class="spec-row"><span class="spec-label">Velocidades</span><span class="spec-val">3×7 = 21 vel.</span></div>
          <div class="spec-row"><span class="spec-label">Neumático</span><span class="spec-val">27.5 × 2.10"</span></div>
          <div class="spec-row"><span class="spec-label">Color</span><span class="spec-val">Rojo y negro</span></div>
          <div class="spec-row"><span class="spec-label">OEM</span><span class="spec-val">Disponible</span></div>
        </div>
        <div class="product-footer">
          <span class="product-cert">Aluminio integral</span>
          <button class="product-cta" onclick="addToCart('FR-2706 MTB Aluminio')">+ Carrito</button>
        </div>
      </div>
    </div>

    <!-- Road Bike -->
    <div class="product-card" data-cat="ruta">
      <div class="product-img">
        <img src="https://images.unsplash.com/photo-1485965120184-e220f721d03e?w=600&q=80" alt="Bicicleta de ruta road bike aluminio aerodinámico velocidades">
        <span class="product-badge">🚴 Ruta</span>
      </div>
      <div class="product-body">
        <div class="product-category">Bicicleta de Ruta</div>
        <div class="product-name">LWRB-1-9 — Road Bike Longwin</div>
        <p class="product-desc">Cuadro de aluminio ligero, diseño aerodinámico con 24–30 velocidades. Perfecta para ruta, carreras y ciclovías.</p>
        <div class="product-specs">
          <div class="spec-row"><span class="spec-label">Rueda</span><span class="spec-val">24–28 pulgadas</span></div>
          <div class="spec-row"><span class="spec-label">Velocidades</span><span class="spec-val">24–30 velocidades</span></div>
          <div class="spec-row"><span class="spec-label">Sensor</span><span class="spec-val">Velocidad y Cadencia</span></div>
          <div class="spec-row"><span class="spec-label">Cuadro</span><span class="spec-val">Aluminio Alloy</span></div>
          <div class="spec-row"><span class="spec-label">Personalización</span><span class="spec-val">Talla a medida</span></div>
        </div>
        <div class="product-footer">
          <span class="product-cert">Marca Longwin</span>
          <button class="product-cta" onclick="addToCart('Road Bike LWRB-1-9 Longwin')">+ Carrito</button>
        </div>
      </div>
    </div>

    <!-- Moto Deportiva Eléctrica -->
    <div class="product-card" data-cat="moto">
      <div class="product-img">
        <img src="https://images.unsplash.com/photo-1558980394-34764db076b4?w=600&q=80" alt="Moto deportiva eléctrica sport 3000W hub motor motocross">
        <span class="product-badge gold">3000W</span>
      </div>
      <div class="product-body">
        <div class="product-category">Moto Eléctrica Deportiva</div>
        <div class="product-name">Mini Sport — Electric Moto 3000W</div>
        <p class="product-desc">Motocicleta eléctrica estilo sport RUSION con 3000W y 85 km/h. Diseño de competición, 200 kg carga útil, múltiples colores.</p>
        <div class="product-specs">
          <div class="spec-row"><span class="spec-label">Motor</span><span class="spec-val">3000W Hub Motor</span></div>
          <div class="spec-row"><span class="spec-label">Velocidad máx.</span><span class="spec-val">85 km/h</span></div>
          <div class="spec-row"><span class="spec-label">Voltaje</span><span class="spec-val">72V</span></div>
          <div class="spec-row"><span class="spec-label">Carga máx.</span><span class="spec-val">200 kg</span></div>
          <div class="spec-row"><span class="spec-label">Marca</span><span class="spec-val">RUSION</span></div>
        </div>
        <div class="product-footer">
          <span class="product-cert">Cert. EEC</span>
          <button class="product-cta" onclick="addToCart('Mini Sport Electric Moto 3000W')">+ Carrito</button>
        </div>
      </div>
    </div>

    <!-- ECS MTB Línea Propia -->
    <div class="product-card" data-cat="lineas">
      <div class="product-img">
        <img src="https://images.unsplash.com/photo-1511994298241-608e28f14fde?w=600&q=80" alt="Bicicleta BMX MTB acero carbono línea ECS propia">
        <span class="product-badge">ECS MTB</span>
      </div>
      <div class="product-body">
        <div class="product-category">Línea ECS — Catálogo Propio</div>
        <div class="product-name">ECS MTB — Bicicletas de Montaña</div>
        <p class="product-desc">Acero alto carbono, 5 colores, freno disco. Disponible desde 16 hasta 29 pulgadas para todo tipo de rider.</p>
        <div class="product-specs">
          <div class="spec-row"><span class="spec-label">Ruedas</span><span class="spec-val">16–29 pulgadas</span></div>
          <div class="spec-row"><span class="spec-label">Velocidades</span><span class="spec-val">21 velocidades</span></div>
          <div class="spec-row"><span class="spec-label">Frenos</span><span class="spec-val">Disco</span></div>
          <div class="spec-row"><span class="spec-label">Colores</span><span class="spec-val">5 colores</span></div>
          <div class="spec-row"><span class="spec-label">Pedido mín.</span><span class="spec-val">30 unidades</span></div>
        </div>
        <div class="product-footer">
          <span class="product-cert">Línea ECS exclusiva</span>
          <button class="product-cta" onclick="addToCart('ECS MTB Línea Propia')">+ Carrito</button>
        </div>
      </div>
    </div>

    <!-- ECS Lithium -->
    <div class="product-card" data-cat="lineas electrica">
      <div class="product-img">
        <img src="https://images.unsplash.com/photo-1526178613552-2b45c6c302f0?w=600&q=80" alt="Motor eléctrico lithium ebike batería litio 250W 500W">
        <span class="product-badge green">ECS Lithium</span>
      </div>
      <div class="product-body">
        <div class="product-category">Línea ECS Eléctrica</div>
        <div class="product-name">ECS Lithium — E-Bikes 250–500W</div>
        <p class="product-desc">Motor 250–500W, batería de litio, autonomía de 40–60 km. Disponible en 7 velocidades para ruedas de 20 a 29 pulgadas.</p>
        <div class="product-specs">
          <div class="spec-row"><span class="spec-label">Motor</span><span class="spec-val">250–500W</span></div>
          <div class="spec-row"><span class="spec-label">Autonomía</span><span class="spec-val">40–60 km</span></div>
          <div class="spec-row"><span class="spec-label">Batería</span><span class="spec-val">Litio</span></div>
          <div class="spec-row"><span class="spec-label">Ruedas</span><span class="spec-val">20–29 pulgadas</span></div>
          <div class="spec-row"><span class="spec-label">Pedido mín.</span><span class="spec-val">30 unidades</span></div>
        </div>
        <div class="product-footer">
          <span class="product-cert">Línea ECS exclusiva</span>
          <button class="product-cta" onclick="addToCart('ECS Lithium E-Bike')">+ Carrito</button>
        </div>
      </div>
    </div>

    <!-- ECS Folding -->
    <div class="product-card" data-cat="lineas">
      <div class="product-img">
        <img src="https://images.unsplash.com/photo-1609525313400-27e3b4f07e01?w=600&q=80" alt="Bicicleta plegable folding compacta urbana city">
        <span class="product-badge">Plegable</span>
      </div>
      <div class="product-body">
        <div class="product-category">Línea ECS Folding</div>
        <div class="product-name">ECS Folding — Bicicleta Plegable</div>
        <p class="product-desc">Se pliega en segundos. Ruedas de 20, 24 y 26 pulgadas con freno disco. Ideal para ciudad y transporte público.</p>
        <div class="product-specs">
          <div class="spec-row"><span class="spec-label">Ruedas</span><span class="spec-val">20, 24, 26 pulg.</span></div>
          <div class="spec-row"><span class="spec-label">Velocidades</span><span class="spec-val">6–7 velocidades</span></div>
          <div class="spec-row"><span class="spec-label">Frenos</span><span class="spec-val">Disco</span></div>
          <div class="spec-row"><span class="spec-label">Colores</span><span class="spec-val">3 colores</span></div>
          <div class="spec-row"><span class="spec-label">Pedido mín.</span><span class="spec-val">30 unidades</span></div>
        </div>
        <div class="product-footer">
          <span class="product-cert">Línea ECS exclusiva</span>
          <button class="product-cta" onclick="addToCart('ECS Folding Plegable')">+ Carrito</button>
        </div>
      </div>
    </div>

    <!-- ECS City Bike -->
    <div class="product-card" data-cat="lineas">
      <div class="product-img">
        <img src="https://images.unsplash.com/photo-1502744688674-c619d1586c9e?w=600&q=80" alt="Bicicleta urbana city bike commuting acero aluminio">
        <span class="product-badge green">City</span>
      </div>
      <div class="product-body">
        <div class="product-category">Línea ECS City Bike</div>
        <div class="product-name">ECS City — Urbana / Commuting</div>
        <p class="product-desc">Perfecta para la ciudad. Ruedas de 26, 27 y 28 pulgadas, 7 velocidades, cuadro de acero o aluminio. Cómoda y durable.</p>
        <div class="product-specs">
          <div class="spec-row"><span class="spec-label">Ruedas</span><span class="spec-val">26, 27, 28 pulg.</span></div>
          <div class="spec-row"><span class="spec-label">Velocidades</span><span class="spec-val">7 velocidades</span></div>
          <div class="spec-row"><span class="spec-label">Frenos</span><span class="spec-val">V-brake</span></div>
          <div class="spec-row"><span class="spec-label">Cuadro</span><span class="spec-val">Acero o Aluminio</span></div>
          <div class="spec-row"><span class="spec-label">Pedido mín.</span><span class="spec-val">30 unidades</span></div>
        </div>
        <div class="product-footer">
          <span class="product-cert">3 colores disp.</span>
          <button class="product-cta" onclick="addToCart('ECS City Bike Urbana')">+ Carrito</button>
        </div>
      </div>
    </div>

  </div>

  <!-- PDF Download -->
  <div style="text-align:center; margin-top:3rem;">
    <p style="font-size:.9rem; color:var(--text-muted); margin-bottom:1rem;">¿Quieres todas las especificaciones técnicas?</p>
    <a href="https://wa.me/18295623551?text=Hola!%20Me%20interesa%20recibir%20el%20catálogo%20completo%20en%20PDF%20de%20ECS%20Logistics." target="_blank" class="btn-primary" style="background:var(--navy);">
      📄 Descargar Catálogo PDF Completo
    </a>
  </div>
</section>

<!-- B2B -->
<section id="b2b">
  <div class="b2b-bg"></div>
  <div class="b2b-inner">
    <div class="b2b-content">
      <span class="section-label" style="color:#7aafef">Área Mayorista</span>
      <h2 class="section-title">Soluciones <span class="accent">B2B</span><br>Para tu Empresa</h2>
      <p class="section-desc">Trabaja con distribuidores, tiendas y flotas corporativas. Pedido mínimo 30 unidades. Cotización personalizada en menos de 24 horas.</p>

      <div class="b2b-features">
        <div class="b2b-feature">
          <div class="b2b-feature-icon">🏢</div>
          <div class="b2b-feature-text">
            <h4>Distribuidores & Tiendas</h4>
            <p>Márgenes competitivos, OEM/ODM disponible y soporte técnico post-venta.</p>
          </div>
        </div>
        <div class="b2b-feature">
          <div class="b2b-feature-icon">🚗</div>
          <div class="b2b-feature-text">
            <h4>Flotas Corporativas</h4>
            <p>Equipamos empresas de delivery, turismo y logística con flotas eléctricas.</p>
          </div>
        </div>
        <div class="b2b-feature">
          <div class="b2b-feature-icon">📦</div>
          <div class="b2b-feature-text">
            <h4>Importación Simplificada</h4>
            <p>Nos encargamos de toda la logística: aduana, flete y entrega nacional.</p>
          </div>
        </div>
        <div class="b2b-feature">
          <div class="b2b-feature-icon">⏱️</div>
          <div class="b2b-feature-text">
            <h4>Entrega en 30–45 días</h4>
            <p>Desde la confirmación de orden hasta la entrega en tu ubicación.</p>
          </div>
        </div>
      </div>
    </div>

    <div class="b2b-form-panel">
      <div class="b2b-form-title">📋 Solicitar Cotización Mayorista</div>
      <div class="form-row">
        <div class="form-group">
          <label>Nombre</label>
          <input type="text" id="bNombre" placeholder="Tu nombre">
        </div>
        <div class="form-group">
          <label>Empresa</label>
          <input type="text" id="bEmpresa" placeholder="Nombre empresa">
        </div>
      </div>
      <div class="form-group">
        <label>WhatsApp / Teléfono</label>
        <input type="tel" id="bTel" placeholder="809-000-0000">
      </div>
      <div class="form-group">
        <label>Producto de interés</label>
        <select id="bProducto">
          <option value="">Selecciona un producto</option>
          <option>ESA — Bicicleta Eléctrica Urbana</option>
          <option>Golden Eagle — E-Bike Compacta 14"</option>
          <option>EMA — Fat Tire E-Bike 1000W</option>
          <option>EMA — Scooter Eléctrico 60V</option>
          <option>LWBI-2-5 — Mountain Bike 27.5"</option>
          <option>FR-2706 — MTB Aluminio Full Spec</option>
          <option>LWRB-1-9 — Road Bike Longwin</option>
          <option>Mini Sport — Moto Eléctrica 3000W</option>
          <option>Líneas ECS (MTB / City / Folding / Lithium)</option>
          <option>Múltiples productos</option>
        </select>
      </div>
      <div class="form-group">
        <label>Cantidad aproximada</label>
        <select id="bCantidad">
          <option value="">Selecciona cantidad</option>
          <option>30–50 unidades</option>
          <option>51–100 unidades</option>
          <option>101–300 unidades</option>
          <option>300+ unidades (contenedor)</option>
        </select>
      </div>
      <div class="form-group">
        <label>Comentarios adicionales</label>
        <textarea id="bComentarios" placeholder="Cuéntanos más sobre tu proyecto..."></textarea>
      </div>
      <button class="btn-form" onclick="submitB2B()">Enviar Solicitud de Cotización →</button>
    </div>
  </div>
</section>

<!-- SEGUIMIENTO -->
<section id="seguimiento">
  <div class="section-header centered">
    <span class="section-label">Tracking</span>
    <h2 class="section-title">Seguimiento de <span class="accent">Pedido</span></h2>
    <p class="section-desc">Rastrea el estado de tu orden en tiempo real desde la confirmación hasta la entrega.</p>
  </div>

  <div class="tracking-box">
    <div class="track-input-row">
      <input class="track-input" id="trackInput" type="text" placeholder="Ingresa tu número de orden (ej. ECS-2026-001)">
      <button class="btn-track" onclick="trackOrder()">Rastrear →</button>
    </div>
    <div class="tracking-steps" id="trackingSteps">
      <div class="tracking-step">
        <div class="step-dot done">✓</div>
        <div class="step-info">
          <h4>Orden Confirmada</h4>
          <p>Tu pedido fue recibido y confirmado</p>
        </div>
      </div>
      <div class="tracking-step">
        <div class="step-dot done">✓</div>
        <div class="step-info">
          <h4>Producción en Fábrica</h4>
          <p>Los productos están siendo fabricados</p>
        </div>
      </div>
      <div class="tracking-step">
        <div class="step-dot active">→</div>
        <div class="step-info">
          <h4>En Tránsito Internacional</h4>
          <p>Tu carga está en camino desde origen</p>
        </div>
      </div>
      <div class="tracking-step">
        <div class="step-dot">4</div>
        <div class="step-info">
          <h4>Aduana &amp; Despacho</h4>
          <p>Procesando documentación aduanal</p>
        </div>
      </div>
      <div class="tracking-step">
        <div class="step-dot">5</div>
        <div class="step-info">
          <h4>Entregado</h4>
          <p>Pedido recibido en tu ubicación</p>
        </div>
      </div>
    </div>
    <p style="font-size:.78rem; color:var(--gray); text-align:center; margin-top:1.5rem;">¿Necesitas ayuda? <a href="https://wa.me/18295623551" style="color:var(--blue-bright)">Contáctanos por WhatsApp →</a></p>
  </div>
</section>

<!-- NOSOTROS -->
<section id="nosotros">
  <div class="about-grid">
    <div class="about-img-block">
      <div class="about-img-main">
        <img src="https://images.unsplash.com/photo-1565793298595-6a879b1d9492?w=700&q=80" alt="Equipo ECS Logistics importación bicicletas eléctricas República Dominicana">
      </div>
      <div class="about-img-badge">
        <div>
          <div class="about-img-badge-num">2026</div>
          <div class="about-img-badge-txt">Catálogo actualizado</div>
        </div>
      </div>
    </div>
    <div class="about-content">
      <span class="section-label">Sobre Nosotros</span>
      <h2 class="section-title">Tu Socio de <span class="accent">Importación</span> de Confianza</h2>
      <p class="section-desc">ECS Logistics nació con un propósito claro: democratizar la movilidad sostenible en República Dominicana, dando acceso a vehículos de calidad a precios mayoristas directos de fábrica.</p>
      <p style="font-size:.95rem; color:var(--text-muted); line-height:1.7; margin-top:1rem;">Somos especialistas en importación de bicicletas eléctricas, convencionales y motocicletas. Trabajamos directamente con fabricantes certificados en Asia, coordinando toda la cadena logística para que tú solo te preocupes por vender.</p>

      <div class="about-values">
        <div class="about-value">
          <div class="about-value-dot"></div>
          <div class="about-value-text">
            <h4>Simplicidad en cada importación</h4>
            <p>Nos encargamos de toda la logística, desde la fábrica hasta tu almacén.</p>
          </div>
        </div>
        <div class="about-value">
          <div class="about-value-dot"></div>
          <div class="about-value-text">
            <h4>Productos certificados CE / EEC</h4>
            <p>Todos nuestros productos cumplen con estándares internacionales de seguridad.</p>
          </div>
        </div>
        <div class="about-value">
          <div class="about-value-dot"></div>
          <div class="about-value-text">
            <h4>Cobertura nacional</h4>
            <p>Entregamos en todo el territorio dominicano con tiempo de entrega garantizado.</p>
          </div>
        </div>
        <div class="about-value">
          <div class="about-value-dot"></div>
          <div class="about-value-text">
            <h4>Soporte real post-venta</h4>
            <p>Nuestro equipo te acompaña antes, durante y después de cada orden.</p>
          </div>
        </div>
      </div>

      <div style="margin-top:2rem;">
        <a href="#contacto" class="btn-primary">Habla con Nosotros →</a>
      </div>
    </div>
  </div>
</section>

<!-- POR QUÉ ECS -->
<section id="por-que" style="background:var(--off-white)">
  <div class="section-header centered">
    <span class="section-label">Nuestras Ventajas</span>
    <h2 class="section-title">¿Por Qué Elegir <span class="accent">ECS?</span></h2>
  </div>
  <div class="why-grid">
    <div class="why-card">
      <span class="why-icon">🏭</span>
      <div class="why-title">Directo de Fábrica</div>
      <p class="why-text">Trabajamos con fabricantes certificados en Asia, sin intermediarios. Eso se traduce en mejor precio para ti.</p>
    </div>
    <div class="why-card">
      <span class="why-icon">📋</span>
      <div class="why-title">Certificaciones Internacionales</div>
      <p class="why-text">CE, EEC, EN15194, ISO, EPA, CQC. Todos los productos listos para cumplimiento legal y reventa.</p>
    </div>
    <div class="why-card">
      <span class="why-icon">🚚</span>
      <div class="why-title">Logística Completa</div>
      <p class="why-text">Desde la producción hasta la entrega en tu puerta. Aduana, flete y documentación incluidos.</p>
    </div>
    <div class="why-card">
      <span class="why-icon">🔧</span>
      <div class="why-title">OEM / ODM Disponible</div>
      <p class="why-text">Personaliza modelos con tu marca. Colores, serigrafía y configuraciones a tu medida.</p>
    </div>
    <div class="why-card">
      <span class="why-icon">💬</span>
      <div class="why-title">Atención Personalizada</div>
      <p class="why-text">Respondemos por WhatsApp, email o llamada. Sin bots, trato humano y directo.</p>
    </div>
    <div class="why-card">
      <span class="why-icon">🌱</span>
      <div class="why-title">Movilidad Sostenible</div>
      <p class="why-text">Contribuimos al futuro verde de la isla con vehículos eléctricos de cero emisiones.</p>
    </div>
  </div>
</section>

<!-- BLOG -->
<section id="blog">
  <div class="section-header">
    <span class="section-label">Blog ECS</span>
    <h2 class="section-title">Recursos para tu <span class="accent">Negocio</span></h2>
    <p class="section-desc">Guías, tendencias y consejos para distribuidores y entusiastas de la movilidad eléctrica.</p>
  </div>
  <div class="blog-grid">
    <div class="blog-card">
      <div class="blog-img">
        <img src="https://images.unsplash.com/photo-1609774605271-853e17c8a439?w=500&q=80" alt="Cómo importar bicicletas eléctricas República Dominicana distribuidores">
      </div>
      <div class="blog-body">
        <span class="blog-tag">Guía</span>
        <div class="blog-title">¿Cómo es el proceso de importar con ECS Logistics?</div>
        <p class="blog-excerpt">Desde la selección del modelo hasta la entrega en tu almacén. Todo lo que necesitas saber en 5 pasos.</p>
        <div class="blog-meta">⏱ 5 min lectura · Mayo 2026</div>
      </div>
    </div>
    <div class="blog-card">
      <div class="blog-img">
        <img src="https://images.unsplash.com/photo-1558618666-fcd25c85cd64?w=500&q=80" alt="Mercado bicicletas eléctricas RD 2026 tendencias motor brushless">
      </div>
      <div class="blog-body">
        <span class="blog-tag">Tendencias</span>
        <div class="blog-title">5 razones para ofrecer bicicletas eléctricas en tu tienda en 2026</div>
        <p class="blog-excerpt">El mercado de e-bikes creció un 40% en 2025. Descubre por qué los distribuidores que entraron temprano ya lideran.</p>
        <div class="blog-meta">⏱ 7 min lectura · Abril 2026</div>
      </div>
    </div>
    <div class="blog-card">
      <div class="blog-img">
        <img src="https://images.unsplash.com/photo-1526401485004-46910ecc8e51?w=500&q=80" alt="Rentabilidad distribuidores bicicletas eléctricas mayoristas margenes">
      </div>
      <div class="blog-body">
        <span class="blog-tag">Negocios</span>
        <div class="blog-title">¿Cuánto puedo ganar revendiendo bicicletas eléctricas?</div>
        <p class="blog-excerpt">Analizamos los márgenes reales del mercado dominicano y cómo calcular tu rentabilidad por unidad.</p>
        <div class="blog-meta">⏱ 6 min lectura · Marzo 2026</div>
      </div>
    </div>
  </div>
</section>

<!-- CONTACTO -->
<section id="contacto">
  <div class="contact-bg"></div>
  <div class="contact-inner">
    <div class="contact-info">
      <span class="section-label" style="color:#7aafef">Contacto</span>
      <h2 class="section-title">Hablemos de <span class="accent">tu Proyecto</span></h2>
      <p class="section-desc">Estamos listos para asesorarte. Respuesta garantizada en menos de 24 horas hábiles.</p>

      <div class="contact-cards">
        <a href="https://wa.me/18295623551" target="_blank" class="contact-card">
          <div class="contact-card-icon">💬</div>
          <div class="contact-card-info">
            <h4>WhatsApp</h4>
            <p>829-562-3551 — Respuesta inmediata</p>
          </div>
        </a>
        <a href="mailto:emely.ecslogistics@gmail.com" class="contact-card">
          <div class="contact-card-icon">✉️</div>
          <div class="contact-card-info">
            <h4>Email</h4>
            <p>emely.ecslogistics@gmail.com</p>
          </div>
        </a>
        <a href="#" class="contact-card">
          <div class="contact-card-icon">📍</div>
          <div class="contact-card-info">
            <h4>Cobertura</h4>
            <p>Todo el territorio nacional · RD</p>
          </div>
        </a>
        <a href="#" class="contact-card">
          <div class="contact-card-icon">⏰</div>
          <div class="contact-card-info">
            <h4>Tiempo de entrega</h4>
            <p>30–45 días desde confirmación de orden</p>
          </div>
        </a>
      </div>

      <div class="social-row">
        <a href="https://instagram.com" target="_blank" class="social-btn" title="Instagram">📸</a>
        <a href="https://facebook.com" target="_blank" class="social-btn" title="Facebook">👍</a>
        <a href="https://linkedin.com" target="_blank" class="social-btn" title="LinkedIn">💼</a>
        <a href="https://wa.me/18295623551" target="_blank" class="social-btn" title="WhatsApp">💬</a>
      </div>
    </div>

    <div class="contact-form-panel">
      <div class="b2b-form-title">📩 Formulario de Contacto</div>
      <div class="form-group">
        <label>Nombre completo</label>
        <input type="text" id="cNombre" placeholder="Tu nombre">
      </div>
      <div class="form-group">
        <label>Correo electrónico</label>
        <input type="email" id="cEmail" placeholder="tucorreo@gmail.com">
      </div>
      <div class="form-group">
        <label>Teléfono</label>
        <input type="tel" id="cTel" placeholder="809-000-0000">
      </div>
      <div class="form-group">
        <label>Asunto</label>
        <select id="cAsunto">
          <option value="">Selecciona un asunto</option>
          <option>Cotización mayorista</option>
          <option>Información de productos</option>
          <option>Seguimiento de pedido</option>
          <option>OEM / Personalización</option>
          <option>Alianza comercial</option>
          <option>Otro</option>
        </select>
      </div>
      <div class="form-group">
        <label>Mensaje</label>
        <textarea id="cMensaje" placeholder="Escríbenos tu consulta..."></textarea>
      </div>
      <button class="btn-form" onclick="submitContact()">Enviar Mensaje →</button>
    </div>
  </div>
</section>

<!-- FOOTER -->
<footer>
  <div class="footer-top">
    <div class="footer-brand">
      <a href="#hero" class="nav-logo">ECS <span>LOGISTICS</span></a>
      <p>Importación simplificada de bicicletas eléctricas, MTB y motos deportivas. Tu socio de movilidad sostenible en República Dominicana.</p>
      <p style="margin-top:.8rem; font-size:.78rem; color:#3a5a7a;">📞 829-562-3551 · ✉️ emely.ecslogistics@gmail.com</p>
    </div>
    <div class="footer-col">
      <h4>Productos</h4>
      <ul>
        <li><a href="#catalogo">Bicicletas Eléctricas</a></li>
        <li><a href="#catalogo">Mountain Bike MTB</a></li>
        <li><a href="#catalogo">Bicicletas de Ruta</a></li>
        <li><a href="#catalogo">Scooters Eléctricos</a></li>
        <li><a href="#catalogo">Motos Deportivas</a></li>
        <li><a href="#catalogo">Líneas ECS</a></li>
      </ul>
    </div>
    <div class="footer-col">
      <h4>Empresa</h4>
      <ul>
        <li><a href="#nosotros">Sobre Nosotros</a></li>
        <li><a href="#b2b">Área B2B</a></li>
        <li><a href="#seguimiento">Rastrear Pedido</a></li>
        <li><a href="#blog">Blog</a></li>
        <li><a href="#contacto">Contacto</a></li>
      </ul>
    </div>
    <div class="footer-col">
      <h4>Contacto</h4>
      <ul>
        <li><a href="https://wa.me/18295623551">WhatsApp: 829-562-3551</a></li>
        <li><a href="mailto:emely.ecslogistics@gmail.com">emely.ecslogistics@gmail.com</a></li>
        <li><a href="#">Entrega Nacional 30–45 días</a></li>
        <li><a href="#">Mínimo 30 unidades/modelo</a></li>
      </ul>
    </div>
  </div>
  <div class="footer-bottom">
    <p>© 2026 ECS Logistics · Your Imports, Simplified · República Dominicana</p>
    <p>Certificaciones: CE · EEC · EN15194 · ISO · EPA · COC</p>
  </div>
</footer>

<script>
// Cart state
let cart = [];

function addToCart(name) {
  const existing = cart.find(i => i.name === name);
  if (existing) {
    existing.qty++;
  } else {
    cart.push({ name, qty: 30 });
  }
  updateCartUI();
  showToast(`✅ ${name.substring(0,25)}... agregado`);
}

function removeFromCart(idx) {
  cart.splice(idx, 1);
  updateCartUI();
}

function changeQty(idx, delta) {
  cart[idx].qty = Math.max(30, cart[idx].qty + delta);
  updateCartUI();
}

function updateCartUI() {
  document.getElementById('cartCount').textContent = cart.length;
  const itemsEl = document.getElementById('cartItems');
  const footerEl = document.getElementById('cartFooter');
  if (cart.length === 0) {
    itemsEl.innerHTML = '<div class="cart-empty"><div class="cart-empty-icon">🚲</div><p>Tu carrito está vacío.<br>Agrega productos del catálogo.</p></div>';
    footerEl.style.display = 'none';
    return;
  }
  footerEl.style.display = 'block';
  itemsEl.innerHTML = cart.map((item, i) => `
    <div class="cart-item">
      <div class="cart-item-info">
        <h4>${item.name}</h4>
        <p>Pedido mínimo 30 unidades</p>
        <div class="cart-item-qty">
          <button class="qty-btn" onclick="changeQty(${i},-10)">−</button>
          <span class="qty-num">${item.qty}</span>
          <button class="qty-btn" onclick="changeQty(${i},10)">+</button>
          <span style="font-size:.72rem;color:var(--text-muted);margin-left:4px">uds.</span>
        </div>
      </div>
      <button class="cart-item-remove" onclick="removeFromCart(${i})">✕</button>
    </div>
  `).join('');
}

function openCart() {
  document.getElementById('cartSidebar').classList.add('open');
  document.getElementById('cartOverlay').classList.add('open');
}

function closeCart() {
  document.getElementById('cartSidebar').classList.remove('open');
  document.getElementById('cartOverlay').classList.remove('open');
}

function sendOrder() {
  if (cart.length === 0) return;
  const items = cart.map(i => `${i.name}: ${i.qty} uds.`).join('%0A');
  const msg = `Hola! Me interesa cotizar los siguientes productos:%0A%0A${items}%0A%0APor favor contáctame.`;
  window.open(`https://wa.me/18295623551?text=${msg}`, '_blank');
}

// Filter catalogue
function filterCat(cat, btn) {
  document.querySelectorAll('.cat-btn').forEach(b => b.classList.remove('active'));
  btn.classList.add('active');
  document.querySelectorAll('.product-card').forEach(card => {
    if (cat === 'all' || card.dataset.cat.includes(cat)) {
      card.style.display = 'flex';
    } else {
      card.style.display = 'none';
    }
  });
}

// Toast
function showToast(msg) {
  const t = document.getElementById('toast');
  t.textContent = msg;
  t.classList.add('show');
  setTimeout(() => t.classList.remove('show'), 2500);
}

// Nav toggle
function toggleNav() {
  document.getElementById('navLinks').classList.toggle('open');
}

// Track order
function trackOrder() {
  const val = document.getElementById('trackInput').value.trim();
  if (!val) { showToast('⚠️ Ingresa un número de orden'); return; }
  showToast(`🔍 Buscando orden ${val}...`);
  setTimeout(() => {
    showToast('📞 Para detalles exactos, contáctanos por WhatsApp');
  }, 2000);
}

// B2B submit
function submitB2B() {
  const nombre = document.getElementById('bNombre').value;
  const empresa = document.getElementById('bEmpresa').value;
  const tel = document.getElementById('bTel').value;
  const producto = document.getElementById('bProducto').value;
  const cantidad = document.getElementById('bCantidad').value;
  if (!nombre || !tel || !producto) { showToast('⚠️ Completa nombre, teléfono y producto'); return; }
  const msg = `Hola ECS Logistics! Solicito cotización mayorista:%0A%0A👤 Nombre: ${nombre}%0A🏢 Empresa: ${empresa}%0A📞 Tel: ${tel}%0A🚲 Producto: ${producto}%0A📦 Cantidad: ${cantidad}`;
  window.open(`https://wa.me/18295623551?text=${msg}`, '_blank');
  showToast('✅ Redirigiendo a WhatsApp...');
}

// Contact submit
function submitContact() {
  const nombre = document.getElementById('cNombre').value;
  const email = document.getElementById('cEmail').value;
  const tel = document.getElementById('cTel').value;
  const asunto = document.getElementById('cAsunto').value;
  const mensaje = document.getElementById('cMensaje').value;
  if (!nombre || !tel) { showToast('⚠️ Completa nombre y teléfono'); return; }
  const msg = `Hola ECS! Mi consulta:%0A%0A👤 ${nombre}%0A📧 ${email}%0A📞 ${tel}%0A📌 Asunto: ${asunto}%0A💬 ${mensaje}`;
  window.open(`https://wa.me/18295623551?text=${msg}`, '_blank');
  showToast('✅ Mensaje enviado!');
}

// Smooth scroll for nav links
document.querySelectorAll('a[href^="#"]').forEach(a => {
  a.addEventListener('click', function(e) {
    const target = document.querySelector(this.getAttribute('href'));
    if (target) {
      e.preventDefault();
      target.scrollIntoView({ behavior: 'smooth' });
      document.getElementById('navLinks').classList.remove('open');
    }
  });
});

// Fade in on scroll
const observer = new IntersectionObserver((entries) => {
  entries.forEach(e => {
    if (e.isIntersecting) {
      e.target.style.opacity = '1';
      e.target.style.transform = 'translateY(0)';
    }
  });
}, { threshold: 0.1 });

document.querySelectorAll('.product-card, .why-card, .blog-card').forEach(el => {
  el.style.opacity = '0';
  el.style.transform = 'translateY(30px)';
  el.style.transition = 'opacity .5s ease, transform .5s ease';
  observer.observe(el);
});
</script>
</body>
</html>
