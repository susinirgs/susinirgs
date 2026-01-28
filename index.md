---
layout: default
title: SUSINIRGS - Artista Trap & Productor Musical
---

<!-- Subtle Background Texture -->
<div id="texture-overlay"></div>

<!-- Navigation -->
<nav class="main-nav" id="main-nav">
  <div class="nav-brand">SUSINIRGS</div>
  <div class="nav-toggle" onclick="toggleNav()">
    <span></span>
    <span></span>
    <span></span>
  </div>
  <div class="nav-links">
    <a href="#hero" class="nav-link active">Inicio</a>
    <a href="#about" class="nav-link">Sobre Mí</a>
    <a href="#music" class="nav-link">Música</a>
    <a href="#videos" class="nav-link">Videos</a>
    <a href="#gallery" class="nav-link">Galería</a>
    <a href="#connect" class="nav-link">Conectar</a>
  </div>
</nav>

<style>
  /* ===== TEXTURE OVERLAY ===== */
  #texture-overlay {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    pointer-events: none;
    z-index: 0;
    opacity: 0.03;
    background-image: url("data:image/svg+xml,%3Csvg viewBox='0 0 200 200' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='noise'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.65' numOctaves='3' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%' height='100%' filter='url(%23noise)'/%3E%3C/svg%3E");
  }
  
  /* ===== NAVIGATION ===== */
  .main-nav {
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    z-index: 9999;
    background: rgba(26, 26, 31, 0.95);
    border-bottom: 1px solid rgba(196, 101, 74, 0.2);
    padding: 0 40px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    height: 70px;
    backdrop-filter: blur(12px);
    transition: all 0.4s ease;
  }
  
  .nav-brand {
    font-family: 'Playfair Display', serif;
    font-size: 24px;
    font-weight: 700;
    color: #f5f0e8;
    letter-spacing: 3px;
  }
  
  .nav-toggle {
    display: none;
    flex-direction: column;
    gap: 5px;
    cursor: pointer;
    padding: 5px;
  }
  
  .nav-toggle span {
    display: block;
    width: 24px;
    height: 2px;
    background: #c4654a;
    transition: all 0.3s ease;
  }
  
  .nav-links {
    display: flex;
    gap: 8px;
  }
  
  .main-nav .nav-link {
    color: #e8e3db;
    text-decoration: none;
    font-size: 13px;
    font-weight: 500;
    text-transform: uppercase;
    padding: 10px 18px;
    border-radius: 6px;
    transition: all 0.3s ease;
    letter-spacing: 1px;
    position: relative;
  }
  
  .main-nav .nav-link::after {
    content: '';
    position: absolute;
    bottom: 6px;
    left: 50%;
    width: 0;
    height: 2px;
    background: #c4654a;
    transition: all 0.3s ease;
    transform: translateX(-50%);
  }
  
  .main-nav .nav-link:hover::after,
  .main-nav .nav-link.active::after {
    width: calc(100% - 36px);
  }
  
  .main-nav .nav-link:hover {
    color: #c4654a;
  }
  
  .main-nav .nav-link.active {
    color: #c4654a;
  }
  
  @media (max-width: 768px) {
    .main-nav {
      padding: 0 20px;
    }
    
    .nav-toggle {
      display: flex;
    }
    
    .nav-links {
      position: absolute;
      top: 70px;
      left: 0;
      right: 0;
      background: rgba(26, 26, 31, 0.98);
      flex-direction: column;
      padding: 20px;
      gap: 5px;
      display: none;
      border-bottom: 1px solid rgba(196, 101, 74, 0.2);
    }
    
    .nav-links.show {
      display: flex;
    }
    
    .main-nav .nav-link {
      padding: 12px 15px;
    }
  }
</style>

<script>
  // Toggle mobile nav
  function toggleNav() {
    document.querySelector('.nav-links').classList.toggle('show');
  }
  
  // Smooth scroll highlight
  document.addEventListener('scroll', function() {
    const sections = document.querySelectorAll('[id]');
    const navLinks = document.querySelectorAll('.nav-link');
    let current = '';
    
    sections.forEach(section => {
      const sectionTop = section.offsetTop;
      if (pageYOffset >= sectionTop - 150) {
        current = section.getAttribute('id');
      }
    });
    
    navLinks.forEach(link => {
      link.classList.remove('active');
      if (link.getAttribute('href') === '#' + current) {
        link.classList.add('active');
      }
    });
    
    // Nav background on scroll
    const nav = document.getElementById('main-nav');
    if (window.scrollY > 50) {
      nav.style.background = 'rgba(26, 26, 31, 0.98)';
      nav.style.boxShadow = '0 4px 20px rgba(0, 0, 0, 0.3)';
    } else {
      nav.style.background = 'rgba(26, 26, 31, 0.95)';
      nav.style.boxShadow = 'none';
    }
  });
</script>

<!-- Hero Section -->
<div class="hero-section" id="hero">
  <div class="hero-content">
    <div class="artist-visual">
      <div class="visual-frame">
        <img src="CRANEO/download - 2025-12-09T125353.235.jpg" alt="SUSINIRGS">
        <div class="visual-overlay"></div>
      </div>
    </div>
    <div class="hero-text">
      <span class="hero-label">Artista Independiente</span>
      <h1 class="artist-name">SUSINIRGS</h1>
      <div class="tagline">
        <span>Trap</span>
        <span class="dot"></span>
        <span>Hip-Hop</span>
        <span class="dot"></span>
        <span>Producción</span>
      </div>
      <p class="hero-description">
        Creando música que fusiona sonidos oscuros con vibras cósmicas. 
        Cada track es un viaje por dimensiones sonoras inexploradas.
      </p>
      <div class="hero-cta">
        <a href="#music" class="btn-primary">
          <span class="btn-icon">▶</span> Escuchar Ahora
        </a>
        <a href="#about" class="btn-outline">Conocer Más</a>
      </div>
    </div>
  </div>
  <div class="scroll-hint">
    <span>Descubre</span>
    <div class="scroll-line"></div>
  </div>
  
  <style>
    .hero-section {
      min-height: 100vh;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      padding: 120px 40px 60px;
      position: relative;
      background: linear-gradient(175deg, #1a1a1f 0%, #151518 100%);
    }
    
    .hero-section::before {
      content: '';
      position: absolute;
      top: 0;
      left: 0;
      right: 0;
      bottom: 0;
      background: 
        radial-gradient(ellipse at 30% 20%, rgba(196, 101, 74, 0.08) 0%, transparent 50%),
        radial-gradient(ellipse at 70% 80%, rgba(122, 154, 138, 0.06) 0%, transparent 50%);
      pointer-events: none;
    }
    
    .hero-content {
      display: grid;
      grid-template-columns: 1fr 1.2fr;
      gap: 80px;
      max-width: 1200px;
      width: 100%;
      align-items: center;
      position: relative;
      z-index: 1;
    }
    
    .artist-visual {
      position: relative;
    }
    
    .visual-frame {
      position: relative;
      border-radius: 16px;
      overflow: hidden;
      box-shadow: 0 30px 80px rgba(0, 0, 0, 0.5);
    }
    
    .visual-frame::before {
      content: '';
      position: absolute;
      top: -3px;
      left: -3px;
      right: -3px;
      bottom: -3px;
      background: linear-gradient(135deg, #c4654a, #7a9a8a, #c9a962);
      border-radius: 18px;
      z-index: -1;
      opacity: 0.6;
    }
    
    .visual-frame img {
      width: 100%;
      height: auto;
      display: block;
      filter: grayscale(20%) contrast(1.05);
      transition: all 0.5s ease;
    }
    
    .visual-frame:hover img {
      filter: grayscale(0%) contrast(1.1);
      transform: scale(1.02);
    }
    
    .visual-overlay {
      position: absolute;
      bottom: 0;
      left: 0;
      right: 0;
      height: 40%;
      background: linear-gradient(to top, rgba(26, 26, 31, 0.9), transparent);
      pointer-events: none;
    }
    
    .hero-text {
      padding: 20px 0;
    }
    
    .hero-label {
      display: inline-block;
      background: rgba(196, 101, 74, 0.15);
      color: #c4654a;
      padding: 8px 20px;
      border-radius: 30px;
      font-size: 12px;
      font-weight: 600;
      text-transform: uppercase;
      letter-spacing: 2px;
      margin-bottom: 20px;
      border: 1px solid rgba(196, 101, 74, 0.3);
    }
    
    .artist-name {
      font-family: 'Playfair Display', serif;
      font-size: 72px;
      font-weight: 700;
      color: #f5f0e8;
      letter-spacing: 6px;
      margin: 0 0 20px 0;
      line-height: 1.1;
    }
    
    .tagline {
      display: flex;
      align-items: center;
      gap: 15px;
      margin-bottom: 25px;
    }
    
    .tagline span {
      font-size: 16px;
      font-weight: 600;
      color: #c9a962;
      text-transform: uppercase;
      letter-spacing: 3px;
    }
    
    .tagline .dot {
      width: 6px;
      height: 6px;
      background: #7a9a8a;
      border-radius: 50%;
    }
    
    .hero-description {
      font-size: 17px;
      color: #b5b0a8;
      line-height: 1.8;
      margin-bottom: 35px;
      max-width: 500px;
    }
    
    .hero-cta {
      display: flex;
      gap: 20px;
      flex-wrap: wrap;
    }
    
    .btn-primary {
      display: inline-flex;
      align-items: center;
      gap: 10px;
      padding: 16px 32px;
      background: linear-gradient(135deg, #c4654a, #a85540);
      color: #f5f0e8;
      text-decoration: none;
      border-radius: 8px;
      font-weight: 600;
      font-size: 14px;
      text-transform: uppercase;
      letter-spacing: 1px;
      transition: all 0.3s ease;
      box-shadow: 0 8px 30px rgba(196, 101, 74, 0.3);
    }
    
    .btn-primary:hover {
      transform: translateY(-3px);
      box-shadow: 0 12px 40px rgba(196, 101, 74, 0.4);
      background: linear-gradient(135deg, #d4856a, #c4654a);
    }
    
    .btn-icon {
      font-size: 12px;
    }
    
    .btn-outline {
      display: inline-flex;
      align-items: center;
      padding: 16px 32px;
      background: transparent;
      color: #c9a962;
      text-decoration: none;
      border: 2px solid #c9a962;
      border-radius: 8px;
      font-weight: 600;
      font-size: 14px;
      text-transform: uppercase;
      letter-spacing: 1px;
      transition: all 0.3s ease;
    }
    
    .btn-outline:hover {
      background: #c9a962;
      color: #1a1a1f;
      transform: translateY(-3px);
    }
    
    .scroll-hint {
      position: absolute;
      bottom: 40px;
      left: 50%;
      transform: translateX(-50%);
      display: flex;
      flex-direction: column;
      align-items: center;
      gap: 10px;
    }
    
    .scroll-hint span {
      font-size: 11px;
      color: #6a6a72;
      text-transform: uppercase;
      letter-spacing: 2px;
    }
    
    .scroll-line {
      width: 1px;
      height: 40px;
      background: linear-gradient(to bottom, #c4654a, transparent);
      animation: scroll-pulse 2s ease-in-out infinite;
    }
    
    @keyframes scroll-pulse {
      0%, 100% { opacity: 1; height: 40px; }
      50% { opacity: 0.5; height: 30px; }
    }
    
    @media (max-width: 900px) {
      .hero-content {
        grid-template-columns: 1fr;
        gap: 40px;
        text-align: center;
      }
      
      .artist-visual {
        max-width: 350px;
        margin: 0 auto;
      }
      
      .artist-name {
        font-size: 48px;
        letter-spacing: 4px;
      }
      
      .tagline {
        justify-content: center;
      }
      
      .hero-description {
        margin: 0 auto 35px;
      }
      
      .hero-cta {
        justify-content: center;
      }
      
      .hero-section {
        padding: 100px 20px 80px;
      }
    }
  </style>
</div>

<!-- About Section -->
<div class="about-section" id="about">
  <div class="about-container">
    <div class="section-header">
      <span class="section-label">Conóceme</span>
      <h2>Sobre Mí</h2>
      <div class="header-accent"></div>
    </div>
    
    <div class="about-content">
      <div class="about-text">
        <h3 class="about-title">La Voz del Underground</h3>
        <p class="about-intro">
          <strong>SUSINIRGS</strong> es un artista independiente de Trap y Hip-Hop que fusiona 
          sonidos oscuros con vibras cósmicas, creando una experiencia musical única que trasciende 
          los límites del género.
        </p>
        
        <div class="about-details">
          <div class="detail-card">
            <div class="detail-icon">🎤</div>
            <div class="detail-content">
              <h4>Estilo Musical</h4>
              <p>Trap experimental, Hip-Hop alternativo, beats oscuros con toques de misticismo y espiritualidad.</p>
            </div>
          </div>
          
          <div class="detail-card">
            <div class="detail-icon">🌌</div>
            <div class="detail-content">
              <h4>Filosofía Artística</h4>
              <p>Energía Mística Universal - cada track es un viaje por dimensiones sonoras inexploradas.</p>
            </div>
          </div>
          
          <div class="detail-card">
            <div class="detail-icon">🎬</div>
            <div class="detail-content">
              <h4>Visión Creativa</h4>
              <p>Producción propia, lírica consciente y visuales cinematográficos. Cada proyecto es una obra completa.</p>
            </div>
          </div>
        </div>
      </div>
      
      <div class="about-visual">
        <div class="quote-card">
          <div class="quote-mark">"</div>
          <p class="quote-text">La música es el portal hacia otras dimensiones. Cada beat es una frecuencia que conecta almas.</p>
          <span class="quote-author">— SUSINIRGS</span>
        </div>
        <div class="stats-mini">
          <div class="stat-mini-item">
            <span class="stat-mini-number">15+</span>
            <span class="stat-mini-label">Proyectos</span>
          </div>
          <div class="stat-mini-item">
            <span class="stat-mini-number">2024</span>
            <span class="stat-mini-label">Activo</span>
          </div>
          <div class="stat-mini-item">
            <span class="stat-mini-number">∞</span>
            <span class="stat-mini-label">Creatividad</span>
          </div>
        </div>
      </div>
    </div>
  </div>
  
  <style>
    .about-section {
      padding: 120px 40px;
      background: linear-gradient(180deg, #151518 0%, #1a1a1f 50%, #1e1e24 100%);
      position: relative;
    }
    
    .about-section::before {
      content: '';
      position: absolute;
      top: 0;
      left: 0;
      right: 0;
      height: 1px;
      background: linear-gradient(90deg, transparent, rgba(196, 101, 74, 0.3), transparent);
    }
    
    .about-container {
      max-width: 1100px;
      margin: 0 auto;
    }
    
    .section-header {
      text-align: center;
      margin-bottom: 70px;
    }
    
    .section-label {
      display: inline-block;
      color: #7a9a8a;
      font-size: 12px;
      font-weight: 600;
      text-transform: uppercase;
      letter-spacing: 3px;
      margin-bottom: 12px;
    }
    
    .section-header h2 {
      font-family: 'Playfair Display', serif;
      font-size: 48px;
      font-weight: 700;
      color: #f5f0e8;
      margin: 0 0 20px 0;
      border: none;
      padding: 0;
    }
    
    .header-accent {
      width: 60px;
      height: 3px;
      background: linear-gradient(90deg, #c4654a, #c9a962);
      margin: 0 auto;
      border-radius: 2px;
    }
    
    .about-content {
      display: grid;
      grid-template-columns: 1.3fr 1fr;
      gap: 60px;
      align-items: start;
    }
    
    .about-title {
      font-family: 'Playfair Display', serif;
      font-size: 28px;
      font-weight: 600;
      color: #c4654a;
      margin: 0 0 20px 0;
    }
    
    .about-intro {
      font-size: 16px;
      line-height: 1.9;
      color: #b5b0a8;
      margin-bottom: 35px;
    }
    
    .about-intro strong {
      color: #c9a962;
    }
    
    .about-details {
      display: flex;
      flex-direction: column;
      gap: 18px;
    }
    
    .detail-card {
      display: flex;
      gap: 18px;
      padding: 22px;
      background: rgba(42, 42, 50, 0.5);
      border-radius: 12px;
      border-left: 3px solid #c4654a;
      transition: all 0.3s ease;
    }
    
    .detail-card:hover {
      background: rgba(196, 101, 74, 0.1);
      transform: translateX(8px);
    }
    
    .detail-icon {
      font-size: 28px;
      flex-shrink: 0;
    }
    
    .detail-content h4 {
      font-size: 15px;
      font-weight: 700;
      color: #7a9a8a;
      margin: 0 0 8px 0;
      text-transform: uppercase;
      letter-spacing: 1px;
    }
    
    .detail-content p {
      font-size: 14px;
      color: #9a9590;
      margin: 0;
      line-height: 1.7;
    }
    
    .about-visual {
      display: flex;
      flex-direction: column;
      gap: 30px;
    }
    
    .quote-card {
      background: linear-gradient(145deg, rgba(196, 101, 74, 0.12), rgba(201, 169, 98, 0.08));
      border-radius: 16px;
      padding: 35px;
      position: relative;
    }
    
    .quote-mark {
      font-family: 'Playfair Display', serif;
      font-size: 60px;
      color: #c4654a;
      line-height: 1;
      position: absolute;
      top: 15px;
      left: 25px;
      opacity: 0.5;
    }
    
    .quote-text {
      font-family: 'Playfair Display', serif;
      font-size: 20px;
      font-style: italic;
      color: #e8e3db;
      line-height: 1.7;
      margin: 20px 0 15px 0;
    }
    
    .quote-author {
      font-size: 14px;
      color: #c9a962;
      font-weight: 600;
    }
    
    .stats-mini {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 15px;
    }
    
    .stat-mini-item {
      background: rgba(42, 42, 50, 0.6);
      border-radius: 12px;
      padding: 25px 15px;
      text-align: center;
      border: 1px solid rgba(122, 154, 138, 0.2);
      transition: all 0.3s ease;
    }
    
    .stat-mini-item:hover {
      border-color: rgba(196, 101, 74, 0.4);
      transform: translateY(-5px);
    }
    
    .stat-mini-number {
      display: block;
      font-family: 'Playfair Display', serif;
      font-size: 32px;
      font-weight: 700;
      color: #c4654a;
      margin-bottom: 5px;
    }
    
    .stat-mini-label {
      font-size: 11px;
      color: #7a7a82;
      text-transform: uppercase;
      letter-spacing: 1px;
    }
    
    @media (max-width: 900px) {
      .about-content {
        grid-template-columns: 1fr;
        gap: 50px;
      }
      
      .section-header h2 {
        font-size: 36px;
      }
      
      .about-section {
        padding: 80px 20px;
      }
    }
  </style>
</div>

<!-- Music Section -->
<div class="music-section" id="music">
  <div class="music-container">
    <div class="section-header">
      <span class="section-label">Discografía</span>
      <h2>Mi Música</h2>
      <div class="header-accent"></div>
      <p class="section-desc">Escucha mis últimos lanzamientos y tracks más populares</p>
    </div>
    
    <div class="music-content">
      <div class="spotify-embed">
        <div class="spotify-header">
          <span class="platform-badge">Spotify</span>
        </div>
        <iframe style="border-radius:12px" src="https://open.spotify.com/embed/artist/78uCfenEleQDaQJM21K2fk?utm_source=generator&theme=0" width="100%" height="400" frameBorder="0" allowfullscreen="" allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture" loading="lazy"></iframe>
        <a href="https://open.spotify.com/intl-es/artist/78uCfenEleQDaQJM21K2fk" target="_blank" class="spotify-link">
          Abrir en Spotify →
        </a>
      </div>
      
      <div class="tracks-list">
        <h3 class="tracks-title">Proyectos Destacados</h3>
        
        <a href="https://www.youtube.com/watch?v=cB5sIhH067A" target="_blank" class="track-item featured">
          <span class="track-rank">01</span>
          <div class="track-info">
            <span class="track-name">Proyecto Más Reciente</span>
            <span class="track-meta">Mi trabajo más fresco y actual</span>
          </div>
          <span class="track-badge">Nuevo</span>
          <span class="track-play">▶</span>
        </a>
        
        <a href="https://www.youtube.com/watch?v=zAjGlkn3udw" target="_blank" class="track-item">
          <span class="track-rank">02</span>
          <div class="track-info">
            <span class="track-name">Energía Mística Universal</span>
            <span class="track-meta">Vibras cósmicas y espirituales</span>
          </div>
          <span class="track-play">▶</span>
        </a>
        
        <a href="https://www.youtube.com/watch?v=uDAziScqsUk" target="_blank" class="track-item">
          <span class="track-rank">03</span>
          <div class="track-info">
            <span class="track-name">Video Más Craneado</span>
            <span class="track-meta">El video que más cerebro me voló</span>
          </div>
          <span class="track-play">▶</span>
        </a>
        
        <a href="https://www.youtube.com/watch?v=VcEhBUNhPs4" target="_blank" class="track-item">
          <span class="track-rank">04</span>
          <div class="track-info">
            <span class="track-name">Data Sagrada</span>
            <span class="track-meta">Información pura y espiritual</span>
          </div>
          <span class="track-play">▶</span>
        </a>
        
        <a href="https://www.youtube.com/watch?v=otPFUIPQkIs" target="_blank" class="track-item">
          <span class="track-rank">05</span>
          <div class="track-info">
            <span class="track-name">Más Rapero</span>
            <span class="track-meta">Flow puro y lírica real</span>
          </div>
          <span class="track-play">▶</span>
        </a>
        
        <a href="https://www.youtube.com/watch?v=J-li4emQsS0" target="_blank" class="track-item">
          <span class="track-rank">06</span>
          <div class="track-info">
            <span class="track-name">La Diferencia Es Lo Que Vale</span>
            <span class="track-meta">Proyecto excepcional y único</span>
          </div>
          <span class="track-play">▶</span>
        </a>
      </div>
    </div>
  </div>
  
  <style>
    .music-section {
      padding: 120px 40px;
      background: linear-gradient(180deg, #1e1e24 0%, #1a1a1f 50%, #151518 100%);
      position: relative;
    }
    
    .music-container {
      max-width: 1200px;
      margin: 0 auto;
    }
    
    .section-desc {
      font-size: 16px;
      color: #7a7a82;
      margin-top: 20px;
      max-width: 450px;
      margin-left: auto;
      margin-right: auto;
    }
    
    .music-content {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 50px;
      margin-top: 60px;
    }
    
    .spotify-embed {
      background: linear-gradient(145deg, #2a2a32, #1a1a1f);
      border-radius: 16px;
      padding: 25px;
      border: 1px solid rgba(122, 154, 138, 0.2);
    }
    
    .spotify-header {
      margin-bottom: 20px;
    }
    
    .platform-badge {
      display: inline-block;
      background: rgba(29, 185, 84, 0.15);
      color: #1DB954;
      padding: 6px 16px;
      border-radius: 20px;
      font-size: 12px;
      font-weight: 700;
      letter-spacing: 1px;
      text-transform: uppercase;
      border: 1px solid rgba(29, 185, 84, 0.3);
    }
    
    .spotify-link {
      display: block;
      text-align: center;
      margin-top: 18px;
      color: #1DB954;
      text-decoration: none;
      font-weight: 600;
      font-size: 14px;
      transition: all 0.3s ease;
    }
    
    .spotify-link:hover {
      color: #f5f0e8;
    }
    
    .tracks-list {
      display: flex;
      flex-direction: column;
      gap: 12px;
    }
    
    .tracks-title {
      font-family: 'Playfair Display', serif;
      font-size: 22px;
      font-weight: 600;
      color: #c9a962;
      margin: 0 0 15px 0;
    }
    
    .track-item {
      display: flex;
      align-items: center;
      gap: 15px;
      padding: 18px 22px;
      background: rgba(42, 42, 50, 0.4);
      border-radius: 12px;
      border: 1px solid transparent;
      transition: all 0.3s ease;
      text-decoration: none;
      cursor: pointer;
    }
    
    .track-item:hover {
      background: rgba(196, 101, 74, 0.1);
      border-color: rgba(196, 101, 74, 0.3);
      transform: translateX(8px);
    }
    
    .track-item.featured {
      background: linear-gradient(135deg, rgba(196, 101, 74, 0.15), rgba(201, 169, 98, 0.1));
      border-color: rgba(196, 101, 74, 0.3);
    }
    
    .track-rank {
      font-family: 'Playfair Display', serif;
      font-size: 18px;
      font-weight: 700;
      color: #4a4a52;
      width: 30px;
      text-align: center;
    }
    
    .track-item.featured .track-rank,
    .track-item:hover .track-rank {
      color: #c4654a;
    }
    
    .track-info {
      flex-grow: 1;
    }
    
    .track-name {
      display: block;
      font-size: 15px;
      font-weight: 600;
      color: #f5f0e8;
      margin-bottom: 4px;
    }
    
    .track-meta {
      display: block;
      font-size: 12px;
      color: #7a7a82;
    }
    
    .track-badge {
      background: linear-gradient(135deg, #c4654a, #a85540);
      color: #f5f0e8;
      font-size: 10px;
      font-weight: 700;
      padding: 5px 12px;
      border-radius: 15px;
      letter-spacing: 1px;
      text-transform: uppercase;
    }
    
    .track-play {
      width: 38px;
      height: 38px;
      display: flex;
      align-items: center;
      justify-content: center;
      background: linear-gradient(135deg, #c4654a, #a85540);
      color: #f5f0e8;
      border-radius: 50%;
      font-size: 12px;
      transition: all 0.3s ease;
      flex-shrink: 0;
    }
    
    .track-item:hover .track-play {
      transform: scale(1.1);
      box-shadow: 0 6px 20px rgba(196, 101, 74, 0.4);
    }
    
    @media (max-width: 900px) {
      .music-content {
        grid-template-columns: 1fr;
        gap: 40px;
      }
      
      .music-section {
        padding: 80px 20px;
      }
    }
  </style>
</div>

<!-- Video Section -->
<div class="video-section" id="videos">
  <div class="video-container">
    <div class="section-header">
      <span class="section-label">Contenido Visual</span>
      <h2>Videos Musicales</h2>
      <div class="header-accent"></div>
      <p class="section-desc">Videos oficiales, visualizers y contenido exclusivo</p>
    </div>
    
    <div class="video-grid">
      <div class="video-card featured">
        <div class="video-label">Destacado</div>
        <div class="video-wrapper">
          <iframe width="100%" height="315" src="https://www.youtube.com/embed/cB5sIhH067A" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
        </div>
        <div class="video-info">
          <h3>Proyecto Más Reciente</h3>
          <p>Mi trabajo más fresco y actual - El proyecto que define mi evolución artística</p>
          <div class="video-tags">
            <span class="video-tag">Nuevo</span>
            <span class="video-tag">2024</span>
          </div>
        </div>
      </div>
      
      <div class="video-card">
        <div class="video-wrapper">
          <iframe width="100%" height="315" src="https://www.youtube.com/embed/uDAziScqsUk" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
        </div>
        <div class="video-info">
          <h3>Video Más Craneado</h3>
          <p>El video que más cerebro me voló hacer</p>
          <div class="video-tags">
            <span class="video-tag">Creativo</span>
          </div>
        </div>
      </div>
      
      <div class="video-card">
        <div class="video-wrapper">
          <iframe width="100%" height="315" src="https://www.youtube.com/embed/zAjGlkn3udw" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
        </div>
        <div class="video-info">
          <h3>Energía Mística Universal</h3>
          <p>Proyecto con vibras cósmicas y espirituales</p>
          <div class="video-tags">
            <span class="video-tag">Místico</span>
          </div>
        </div>
      </div>
    </div>
    
    <div class="video-cta">
      <a href="https://www.youtube.com/@susinirgs" target="_blank" class="btn-youtube">
        <span>▶</span> Ver Todos en YouTube
      </a>
    </div>
  </div>
  
  <style>
    .video-section {
      padding: 120px 40px;
      background: linear-gradient(180deg, #151518 0%, #1a1a1f 100%);
      position: relative;
    }
    
    .video-container {
      max-width: 1300px;
      margin: 0 auto;
    }
    
    .video-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(380px, 1fr));
      gap: 30px;
      margin-top: 60px;
    }
    
    .video-card {
      background: linear-gradient(145deg, #2a2a32, #1a1a1f);
      border: 1px solid #3a3a45;
      border-radius: 16px;
      overflow: hidden;
      transition: all 0.4s ease;
      position: relative;
    }
    
    .video-card:hover {
      transform: translateY(-10px);
      border-color: #c4654a;
      box-shadow: 0 25px 60px rgba(196, 101, 74, 0.15);
    }
    
    .video-card.featured {
      grid-column: span 2;
      border-color: #c9a962;
    }
    
    .video-card.featured .video-wrapper {
      padding-bottom: 45%;
    }
    
    .video-label {
      position: absolute;
      top: 15px;
      left: 15px;
      background: linear-gradient(135deg, #c9a962, #a98942);
      color: #1a1a1f;
      padding: 6px 15px;
      border-radius: 20px;
      font-size: 11px;
      font-weight: 700;
      z-index: 10;
      letter-spacing: 1px;
      text-transform: uppercase;
    }
    
    .video-wrapper {
      position: relative;
      padding-bottom: 56.25%;
      height: 0;
      overflow: hidden;
    }
    
    .video-wrapper iframe {
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
    }
    
    .video-info {
      padding: 25px;
    }
    
    .video-card h3 {
      font-family: 'Playfair Display', serif;
      font-size: 18px;
      margin: 0 0 10px 0;
      color: #f5f0e8;
      font-weight: 600;
    }
    
    .video-card p {
      font-size: 14px;
      color: #9a9590;
      margin: 0 0 15px 0;
      line-height: 1.6;
    }
    
    .video-tags {
      display: flex;
      gap: 8px;
    }
    
    .video-tag {
      background: rgba(196, 101, 74, 0.15);
      color: #c4654a;
      padding: 5px 12px;
      border-radius: 15px;
      font-size: 11px;
      font-weight: 600;
      text-transform: uppercase;
      letter-spacing: 0.5px;
    }
    
    .video-cta {
      text-align: center;
      margin-top: 50px;
    }
    
    .btn-youtube {
      display: inline-flex;
      align-items: center;
      gap: 12px;
      padding: 16px 36px;
      background: linear-gradient(135deg, #cc0000, #aa0000);
      color: #f5f0e8;
      text-decoration: none;
      border-radius: 8px;
      font-weight: 600;
      font-size: 14px;
      text-transform: uppercase;
      letter-spacing: 1px;
      transition: all 0.3s ease;
      box-shadow: 0 8px 30px rgba(204, 0, 0, 0.25);
    }
    
    .btn-youtube:hover {
      transform: translateY(-3px);
      box-shadow: 0 12px 40px rgba(204, 0, 0, 0.35);
    }
    
    @media (max-width: 900px) {
      .video-card.featured {
        grid-column: span 1;
      }
      
      .video-card.featured .video-wrapper {
        padding-bottom: 56.25%;
      }
      
      .video-grid {
        grid-template-columns: 1fr;
      }
      
      .video-section {
        padding: 80px 20px;
      }
    }
  </style>
</div>

<!-- Gallery Section -->
<div class="gallery-section" id="gallery">
  <div class="gallery-container">
    <div class="section-header">
      <span class="section-label">Visual</span>
      <h2>Galería</h2>
      <div class="header-accent"></div>
      <p class="section-desc">Arte, estética y visuales que definen mi universo creativo</p>
    </div>
    
    <div class="gallery-grid">
      <div class="gallery-item large"><img src="CRANEO/SPOOKY (1) (1).png" alt="Spooky Art" loading="lazy"><div class="gallery-overlay"><span class="gallery-title">Spooky Vibes</span></div></div>
      <div class="gallery-item"><img src="CRANEO/@720pts.jpeg" alt="720pts" loading="lazy"><div class="gallery-overlay"><span class="gallery-title">720pts</span></div></div>
      <div class="gallery-item"><img src="CRANEO/GcM5IGVXMAAPiLF.jpeg" alt="Visual Art" loading="lazy"><div class="gallery-overlay"><span class="gallery-title">Arte Visual</span></div></div>
      <div class="gallery-item tall"><img src="CRANEO/_Freedom starts from within__.jpeg" alt="Freedom" loading="lazy"><div class="gallery-overlay"><span class="gallery-title">Libertad</span></div></div>
      <div class="gallery-item"><img src="CRANEO/download - 2025-12-09T124825.697.jpg" alt="Art 1" loading="lazy"><div class="gallery-overlay"><span class="gallery-title">Arte I</span></div></div>
      <div class="gallery-item"><img src="CRANEO/download - 2025-12-09T125039.980.jpg" alt="Art 2" loading="lazy"><div class="gallery-overlay"><span class="gallery-title">Arte II</span></div></div>
      <div class="gallery-item large"><img src="CRANEO/download - 2025-12-09T125120.584.jpg" alt="Art 3" loading="lazy"><div class="gallery-overlay"><span class="gallery-title">Arte III</span></div></div>
      <div class="gallery-item"><img src="CRANEO/download - 2025-12-09T125323.452.jpg" alt="Art 4" loading="lazy"><div class="gallery-overlay"><span class="gallery-title">Arte IV</span></div></div>
      <div class="gallery-item tall"><img src="CRANEO/silver-surfer-all-alone-in-the-space-wallpaper-with-ai-v0-68daljq9mide1.webp" alt="Silver Surfer" loading="lazy"><div class="gallery-overlay"><span class="gallery-title">Cosmic</span></div></div>
      <div class="gallery-item"><img src="CRANEO/god.jpg" alt="God" loading="lazy"><div class="gallery-overlay"><span class="gallery-title">Divino</span></div></div>
      <div class="gallery-item"><img src="CRANEO/pollloooo.jpeg" alt="Pollo" loading="lazy"><div class="gallery-overlay"><span class="gallery-title">Expresión</span></div></div>
      <div class="gallery-item"><img src="CRANEO/🂡 ʳˡʸᶜʳᵘˢʰ.jpeg" alt="Crush" loading="lazy"><div class="gallery-overlay"><span class="gallery-title">Crush</span></div></div>
    </div>
  </div>
  
  <style>
    .gallery-section {
      padding: 120px 40px;
      background: linear-gradient(180deg, #1a1a1f 0%, #1e1e24 50%, #1a1a1f 100%);
      position: relative;
    }
    
    .gallery-container {
      max-width: 1400px;
      margin: 0 auto;
    }
    
    .gallery-grid {
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      grid-auto-rows: 250px;
      gap: 15px;
      margin-top: 60px;
    }
    
    .gallery-item {
      position: relative;
      overflow: hidden;
      border-radius: 12px;
      border: 1px solid #3a3a45;
      transition: all 0.5s ease;
      cursor: pointer;
    }
    
    .gallery-item.large {
      grid-column: span 2;
    }
    
    .gallery-item.tall {
      grid-row: span 2;
    }
    
    .gallery-item:hover {
      border-color: #c4654a;
      box-shadow: 0 20px 50px rgba(196, 101, 74, 0.2);
      z-index: 10;
      transform: scale(1.02);
    }
    
    .gallery-item img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      transition: all 0.5s ease;
      filter: grayscale(30%) contrast(1.05);
    }
    
    .gallery-item:hover img {
      transform: scale(1.1);
      filter: grayscale(0%) contrast(1.1) brightness(0.8);
    }
    
    .gallery-overlay {
      position: absolute;
      bottom: 0;
      left: 0;
      right: 0;
      padding: 30px 20px 20px;
      background: linear-gradient(to top, rgba(26, 26, 31, 0.95) 0%, transparent 100%);
      opacity: 0;
      transform: translateY(15px);
      transition: all 0.4s ease;
    }
    
    .gallery-item:hover .gallery-overlay {
      opacity: 1;
      transform: translateY(0);
    }
    
    .gallery-title {
      font-family: 'Playfair Display', serif;
      font-size: 14px;
      font-weight: 600;
      color: #f5f0e8;
      text-transform: uppercase;
      letter-spacing: 2px;
    }
    
    @media (max-width: 1000px) {
      .gallery-grid {
        grid-template-columns: repeat(2, 1fr);
        grid-auto-rows: 200px;
      }
      
      .gallery-item.large,
      .gallery-item.tall {
        grid-column: span 1;
        grid-row: span 1;
      }
    }
    
    @media (max-width: 600px) {
      .gallery-grid {
        grid-template-columns: 1fr;
        grid-auto-rows: 280px;
      }
      
      .gallery-section {
        padding: 80px 20px;
      }
    }
  </style>
</div>

<!-- Connect Section -->
<div class="connect-section" id="connect">
  <div class="connect-container">
    <div class="section-header light">
      <span class="section-label">Comunidad</span>
      <h2>Conecta Conmigo</h2>
      <div class="header-accent light"></div>
      <p class="section-desc light">Únete a la comunidad y mantente al día con nueva música</p>
    </div>
    
    <div class="social-links">
      <a href="https://open.spotify.com/intl-es/artist/78uCfenEleQDaQJM21K2fk?si=7O3kEBUITZyZWnRXtJ8bhg" target="_blank" class="social-card spotify">
        <div class="social-icon">🎵</div>
        <span class="social-name">Spotify</span>
        <span class="social-action">Escuchar</span>
      </a>
      <a href="https://www.youtube.com/@susinirgs" target="_blank" class="social-card youtube">
        <div class="social-icon">▶</div>
        <span class="social-name">YouTube</span>
        <span class="social-action">Suscribirse</span>
      </a>
      <a href="https://www.instagram.com/susinirgs/" target="_blank" class="social-card instagram">
        <div class="social-icon">📷</div>
        <span class="social-name">Instagram</span>
        <span class="social-action">Seguir</span>
      </a>
    </div>
    
    <div class="connect-cta">
      <h3>¿Listo para sumergirte en el universo SUSINIRGS?</h3>
      <p>Escucha mi música, ve mis videos y únete a la comunidad</p>
      <a href="#music" class="btn-cta">Empezar a Escuchar</a>
    </div>
  </div>
  
  <style>
    .connect-section {
      padding: 120px 40px;
      background: linear-gradient(135deg, #c4654a 0%, #a85540 50%, #8a4535 100%);
      text-align: center;
      position: relative;
      overflow: hidden;
    }
    
    .connect-section::before {
      content: '';
      position: absolute;
      top: 0;
      left: 0;
      right: 0;
      bottom: 0;
      background: 
        radial-gradient(circle at 20% 30%, rgba(255, 255, 255, 0.08) 0%, transparent 40%),
        radial-gradient(circle at 80% 70%, rgba(0, 0, 0, 0.15) 0%, transparent 40%);
      pointer-events: none;
    }
    
    .connect-container {
      max-width: 1000px;
      margin: 0 auto;
      position: relative;
      z-index: 1;
    }
    
    .section-header.light .section-label {
      color: rgba(245, 240, 232, 0.8);
    }
    
    .section-header.light h2 {
      color: #f5f0e8 !important;
    }
    
    .header-accent.light {
      background: rgba(245, 240, 232, 0.5);
    }
    
    .section-desc.light {
      color: rgba(245, 240, 232, 0.85);
    }
    
    .social-links {
      display: flex;
      gap: 25px;
      justify-content: center;
      flex-wrap: wrap;
      margin: 60px auto;
    }
    
    .social-card {
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      gap: 10px;
      width: 150px;
      height: 150px;
      background: rgba(245, 240, 232, 0.1);
      border: 2px solid rgba(245, 240, 232, 0.25);
      border-radius: 16px;
      text-decoration: none;
      color: #f5f0e8;
      transition: all 0.4s ease;
      backdrop-filter: blur(8px);
    }
    
    .social-icon {
      font-size: 36px;
    }
    
    .social-name {
      font-size: 14px;
      font-weight: 700;
      text-transform: uppercase;
      letter-spacing: 1px;
    }
    
    .social-action {
      font-size: 11px;
      color: rgba(245, 240, 232, 0.7);
      text-transform: uppercase;
      letter-spacing: 1px;
    }
    
    .social-card:hover {
      background: rgba(245, 240, 232, 0.2);
      border-color: rgba(245, 240, 232, 0.6);
      transform: translateY(-8px) scale(1.05);
      box-shadow: 0 15px 40px rgba(0, 0, 0, 0.25);
    }
    
    .social-card.spotify:hover {
      background: rgba(29, 185, 84, 0.3);
      border-color: #1DB954;
    }
    
    .social-card.youtube:hover {
      background: rgba(255, 0, 0, 0.3);
      border-color: #FF0000;
    }
    
    .social-card.instagram:hover {
      background: rgba(228, 64, 95, 0.3);
      border-color: #E4405F;
    }
    
    .connect-cta {
      margin-top: 50px;
      padding-top: 50px;
      border-top: 1px solid rgba(245, 240, 232, 0.2);
    }
    
    .connect-cta h3 {
      font-family: 'Playfair Display', serif;
      font-size: 28px;
      font-weight: 600;
      margin: 0 0 15px 0;
      color: #f5f0e8;
    }
    
    .connect-cta p {
      font-size: 16px;
      color: rgba(245, 240, 232, 0.85);
      margin: 0 0 30px 0;
    }
    
    .btn-cta {
      display: inline-flex;
      align-items: center;
      gap: 10px;
      padding: 18px 40px;
      background: #f5f0e8;
      color: #a85540;
      text-decoration: none;
      border-radius: 8px;
      font-weight: 700;
      font-size: 14px;
      text-transform: uppercase;
      letter-spacing: 1px;
      transition: all 0.3s ease;
      box-shadow: 0 8px 30px rgba(0, 0, 0, 0.2);
    }
    
    .btn-cta:hover {
      transform: translateY(-4px) scale(1.02);
      box-shadow: 0 15px 45px rgba(0, 0, 0, 0.3);
      background: #c9a962;
      color: #1a1a1f;
    }
    
    @media (max-width: 600px) {
      .social-card {
        width: 120px;
        height: 120px;
      }
      
      .social-icon {
        font-size: 28px;
      }
      
      .connect-cta h3 {
        font-size: 22px;
      }
      
      .connect-section {
        padding: 80px 20px;
      }
    }
  </style>
</div>

<!-- Footer -->
<footer class="footer">
  <div class="footer-container">
    <div class="footer-top">
      <div class="footer-brand">
        <h3 class="footer-logo">SUSINIRGS</h3>
        <p class="footer-tagline">Trap · Hip-Hop · Producción</p>
        <p class="footer-desc">Artista independiente creando música que trasciende dimensiones. Energía Mística Universal.</p>
      </div>
      
      <div class="footer-nav">
        <h4>Navegación</h4>
        <a href="#hero">Inicio</a>
        <a href="#about">Sobre Mí</a>
        <a href="#music">Música</a>
        <a href="#videos">Videos</a>
        <a href="#gallery">Galería</a>
      </div>
      
      <div class="footer-social">
        <h4>Plataformas</h4>
        <a href="https://www.youtube.com/@susinirgs" target="_blank">YouTube</a>
        <a href="https://open.spotify.com/intl-es/artist/78uCfenEleQDaQJM21K2fk" target="_blank">Spotify</a>
        <a href="https://www.instagram.com/susinirgs/" target="_blank">Instagram</a>
      </div>
    </div>
    
    <div class="footer-bottom">
      <div class="footer-line"></div>
      <p class="footer-copy">© 2025 SUSINIRGS. Todos los derechos reservados.</p>
      <p class="footer-credit">Hecho con pasión por la cultura</p>
    </div>
  </div>
  
  <style>
    .footer {
      background: linear-gradient(180deg, #1a1a1f 0%, #151518 100%);
      color: #7a7a82;
      padding: 80px 40px 40px;
      position: relative;
    }
    
    .footer::before {
      content: '';
      position: absolute;
      top: 0;
      left: 0;
      right: 0;
      height: 1px;
      background: linear-gradient(90deg, transparent, rgba(196, 101, 74, 0.3), transparent);
    }
    
    .footer-container {
      max-width: 1100px;
      margin: 0 auto;
    }
    
    .footer-top {
      display: grid;
      grid-template-columns: 2fr 1fr 1fr;
      gap: 50px;
      margin-bottom: 50px;
    }
    
    .footer-logo {
      font-family: 'Playfair Display', serif;
      font-size: 32px;
      font-weight: 700;
      margin: 0 0 10px 0;
      color: #f5f0e8;
      letter-spacing: 3px;
    }
    
    .footer-tagline {
      color: #c4654a;
      font-weight: 600;
      font-size: 13px;
      margin: 0 0 15px 0;
      letter-spacing: 2px;
    }
    
    .footer-desc {
      color: #6a6a72;
      font-size: 14px;
      line-height: 1.7;
      margin: 0;
      max-width: 300px;
    }
    
    .footer-nav h4,
    .footer-social h4 {
      font-size: 13px;
      font-weight: 700;
      color: #b5b0a8;
      text-transform: uppercase;
      letter-spacing: 2px;
      margin: 0 0 20px 0;
    }
    
    .footer-nav a,
    .footer-social a {
      display: block;
      color: #6a6a72;
      text-decoration: none;
      font-size: 14px;
      margin-bottom: 12px;
      transition: all 0.3s ease;
    }
    
    .footer-nav a:hover,
    .footer-social a:hover {
      color: #c4654a;
      transform: translateX(5px);
    }
    
    .footer-bottom {
      text-align: center;
      padding-top: 30px;
    }
    
    .footer-line {
      height: 1px;
      background: linear-gradient(90deg, transparent, #3a3a45, transparent);
      margin-bottom: 30px;
    }
    
    .footer-copy {
      color: #9a9590;
      font-size: 13px;
      margin: 0 0 8px 0;
    }
    
    .footer-credit {
      color: #5a5a62;
      font-size: 12px;
      margin: 0;
    }
    
    @media (max-width: 768px) {
      .footer-top {
        grid-template-columns: 1fr;
        gap: 30px;
        text-align: center;
      }
      
      .footer-desc {
        max-width: 100%;
      }
      
      .footer-nav a:hover,
      .footer-social a:hover {
        transform: none;
      }
      
      .footer {
        padding: 60px 20px 30px;
      }
    }
  </style>
</footer>
