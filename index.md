---
layout: default
title: SUSINIRGS - Trap Artist & Producer
---

<!-- Floating Navigation -->
<nav class="floating-nav">
  <a href="#hero" class="nav-link">🏠 Home</a>
  <a href="#videos" class="nav-link">🎬 Videos</a>
  <a href="#tracks" class="nav-link">🎵 Tracks</a>
  <a href="#gallery" class="nav-link">🎨 Gallery</a>
  <a href="#projects" class="nav-link">🚀 Projects</a>
  <a href="#connect" class="nav-link">🔗 Connect</a>
  <style>
    .floating-nav {
      position: fixed;
      top: 20px;
      right: 20px;
      z-index: 9999;
      background: rgba(10, 14, 39, 0.95);
      border: 2px solid #ff006e;
      border-radius: 10px;
      padding: 15px;
      display: flex;
      flex-direction: column;
      gap: 10px;
      box-shadow: 0 10px 40px rgba(255, 0, 110, 0.3);
      backdrop-filter: blur(10px);
    }
    
    .floating-nav .nav-link {
      color: #00f5ff;
      text-decoration: none;
      font-size: 14px;
      font-weight: 700;
      text-transform: uppercase;
      padding: 8px 15px;
      border-radius: 5px;
      transition: all 0.3s ease;
      border: 1px solid transparent;
      white-space: nowrap;
    }
    
    .floating-nav .nav-link:hover {
      background: rgba(255, 0, 110, 0.2);
      border-color: #ff006e;
      color: #ffbe0b;
      transform: translateX(-5px);
    }
    
    @media (max-width: 768px) {
      .floating-nav {
        flex-direction: row;
        top: auto;
        bottom: 10px;
        right: 10px;
        left: 10px;
        padding: 10px;
        overflow-x: auto;
        gap: 5px;
      }
      
      .floating-nav .nav-link {
        font-size: 11px;
        padding: 6px 10px;
      }
    }
  </style>
</nav>

<!-- Hero Section -->
<div class="hero-section" id="hero">
<div class="hero-section">
  <div class="hero-content">
    <div class="artist-logo">
      <h1 class="artist-name">SUSINIRGS</h1>
      <p class="artist-tagline">🔥 TRAP | HIP-HOP | BEATS 🔥</p>
    </div>
    <p class="hero-subtitle">Artista Trap & Hip-Hop | Energía Mística Universal</p>
    <div class="hero-cta">
      <a href="#tracks" class="btn btn-primary">Ver Mis Videos</a>
      <a href="#gallery" class="btn btn-secondary">Galería Visual</a>
    </div>
  </div>
  <style>
    .hero-section {
      background: linear-gradient(135deg, rgba(0, 0, 0, 0.85) 0%, rgba(26, 26, 62, 0.9) 100%), 
                  url('CRANEO/silver-surfer-all-alone-in-the-space-wallpaper-with-ai-v0-68daljq9mide1.webp') center/cover;
      color: #fff;
      padding: 120px 20px;
      text-align: center;
      border-bottom: 3px solid #ff006e;
      position: relative;
      overflow: hidden;
      min-height: 600px;
      display: flex;
      align-items: center;
      justify-content: center;
    }
    
    .hero-section::before {
      content: '';
      position: absolute;
      top: 0;
      left: 0;
      right: 0;
      bottom: 0;
      background: repeating-linear-gradient(
        45deg,
        transparent,
        transparent 10px,
        rgba(255, 0, 110, 0.03) 10px,
        rgba(255, 0, 110, 0.03) 20px
      );
      pointer-events: none;
      animation: slide 20s linear infinite;
    }
    
    @keyframes slide {
      0% { background-position: 0 0; }
      100% { background-position: 100px 100px; }
    }
    
    @keyframes float {
      0%, 100% { transform: translateY(0px); }
      50% { transform: translateY(-10px); }
    }
    
    @keyframes pulse {
      0%, 100% { opacity: 1; }
      50% { opacity: 0.8; }
    }
    
    .hero-content {
      position: relative;
      z-index: 1;
      animation: float 6s ease-in-out infinite;
    }
    
    .artist-logo {
      margin-bottom: 30px;
    }
    
    .artist-name {
      font-size: 72px;
      font-weight: 900;
      margin: 0;
      text-transform: uppercase;
      letter-spacing: 3px;
      background: linear-gradient(90deg, #ff006e, #ffbe0b, #8338ec);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      background-clip: text;
      text-shadow: 2px 2px 20px rgba(255, 0, 110, 0.3);
    }
    
    .artist-tagline {
      font-size: 24px;
      margin: 10px 0 0 0;
      color: #ffbe0b;
      font-weight: 700;
      letter-spacing: 2px;
      text-transform: uppercase;
    }
    
    .hero-subtitle {
      font-size: 20px;
      color: #ccc;
      margin: 20px 0 40px 0;
      font-weight: 300;
    }
    
    .hero-cta {
      display: flex;
      gap: 20px;
      justify-content: center;
      flex-wrap: wrap;
    }
    
    .btn {
      padding: 15px 40px;
      font-size: 16px;
      font-weight: 700;
      text-transform: uppercase;
      letter-spacing: 1px;
      border: none;
      cursor: pointer;
      transition: all 0.3s ease;
      text-decoration: none;
      display: inline-block;
    }
    
    .btn-primary {
      background: linear-gradient(90deg, #ff006e, #fb5607);
      color: white;
      border-radius: 5px;
    }
    
    .btn-primary:hover {
      transform: scale(1.05);
      box-shadow: 0 10px 30px rgba(255, 0, 110, 0.4);
    }
    
    .btn-secondary {
      background: transparent;
      color: #ffbe0b;
      border: 2px solid #ffbe0b;
      border-radius: 5px;
    }
    
    .btn-secondary:hover {
      background: #ffbe0b;
      color: #1a1a1a;
      transform: scale(1.05);
    }
    
    @media (max-width: 768px) {
      .artist-name {
        font-size: 48px !important;
      }
      
      .artist-tagline {
        font-size: 18px !important;
      }
      
      .hero-subtitle {
        font-size: 16px !important;
      }
      
      .hero-section {
        padding: 80px 15px !important;
        min-height: 500px !important;
      }
    }
  </style>
</div>

---

<!-- Video Embeds Section -->
<div class="video-section" id="videos">
  <h2>🎬 VIDEOS DESTACADOS 🎬</h2>
  <div class="video-grid">
    <div class="video-card">
      <div class="video-wrapper">
        <iframe width="100%" height="315" src="https://www.youtube.com/embed/cB5sIhH067A" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
      </div>
      <h3>PROYECTO MÁS RECIENTE</h3>
      <p>Mi trabajo más fresco y actual</p>
    </div>
    
    <div class="video-card">
      <div class="video-wrapper">
        <iframe width="100%" height="315" src="https://www.youtube.com/embed/uDAziScqsUk" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
      </div>
      <h3>VIDEO MÁS CRANEADO</h3>
      <p>El video que más cerebro me voló</p>
    </div>
    
    <div class="video-card">
      <div class="video-wrapper">
        <iframe width="100%" height="315" src="https://www.youtube.com/embed/zAjGlkn3udw" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
      </div>
      <h3>ENERGÍA MÍSTICA UNIVERSAL</h3>
      <p>Proyecto con vibras cósmicas</p>
    </div>
  </div>
  
  <style>
    .video-section {
      padding: 80px 20px;
      background: linear-gradient(135deg, #1a1a3e 0%, #0f0f2e 100%);
      color: #fff;
    }
    
    .video-section h2 {
      font-size: 48px;
      text-align: center;
      margin-bottom: 60px;
      color: #ff006e;
      text-transform: uppercase;
      letter-spacing: 2px;
      font-weight: 900;
      text-shadow: 0 0 20px rgba(255, 0, 110, 0.5);
    }
    
    .video-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
      gap: 40px;
      max-width: 1400px;
      margin: 0 auto;
    }
    
    .video-card {
      background: linear-gradient(135deg, #2d2d2d, #1a1a1a);
      border: 3px solid #ff006e;
      border-radius: 12px;
      padding: 20px;
      transition: all 0.4s ease;
      box-shadow: 0 10px 30px rgba(255, 0, 110, 0.2);
    }
    
    .video-card:hover {
      transform: translateY(-15px);
      border-color: #00ff00;
      box-shadow: 0 20px 60px rgba(255, 0, 110, 0.4);
    }
    
    .video-wrapper {
      position: relative;
      padding-bottom: 56.25%;
      height: 0;
      overflow: hidden;
      border-radius: 8px;
      margin-bottom: 20px;
    }
    
    .video-wrapper iframe {
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
    }
    
    .video-card h3 {
      font-size: 22px;
      margin: 15px 0 10px 0;
      color: #ffbe0b;
      text-transform: uppercase;
      letter-spacing: 1px;
    }
    
    .video-card p {
      font-size: 14px;
      color: #bbb;
      margin: 0;
    }
  </style>
</div>

---

<!-- Tracks Section -->
<div class="tracks-section" id="tracks">
  <h2>🎵 MIS PROYECTOS MÁS CRANEADOS 🎵</h2>
  <div class="tracks-grid">
    <div class="track-card">
      <div class="track-number">01</div>
      <h3>PROYECTO MÁS RECIENTE</h3>
      <p class="track-info">Mi trabajo más fresco y actual</p>
      <p class="track-stats">🔥 Nuevo Release</p>
      <a href="https://www.youtube.com/watch?v=cB5sIhH067A" target="_blank" class="track-btn">▶ VER</a>
    </div>
    
    <div class="track-card">
      <div class="track-number">02</div>
      <h3>VIDEO MÁS CRANEADO</h3>
      <p class="track-info">El video que más cerebro me voló</p>
      <p class="track-stats">🔥 Top Vibes</p>
      <a href="https://www.youtube.com/watch?v=uDAziScqsUk" target="_blank" class="track-btn">▶ VER</a>
    </div>
    
    <div class="track-card">
      <div class="track-number">03</div>
      <h3>ENERGÍA MÍSTICA UNIVERSAL</h3>
      <p class="track-info">Proyecto con vibras cósmicas</p>
      <p class="track-stats">🔥 Mística Total</p>
      <a href="https://www.youtube.com/watch?v=zAjGlkn3udw" target="_blank" class="track-btn">▶ VER</a>
    </div>
    
    <div class="track-card">
      <div class="track-number">04</div>
      <h3>MÁS RAPERO</h3>
      <p class="track-info">Flow puro y lírica real</p>
      <p class="track-stats">🔥 Rap Game</p>
      <a href="https://www.youtube.com/watch?v=otPFUIPQkIs" target="_blank" class="track-btn">▶ VER</a>
    </div>
    
    <div class="track-card">
      <div class="track-number">05</div>
      <h3>DATA SAGRADA</h3>
      <p class="track-info">Información pura y espiritual</p>
      <p class="track-stats">🔥 Sacred</p>
      <a href="https://www.youtube.com/watch?v=VcEhBUNhPs4" target="_blank" class="track-btn">▶ VER</a>
    </div>
    
    <div class="track-card">
      <div class="track-number">06</div>
      <h3>LA DIFERENCIA ES LO QUE VALE</h3>
      <p class="track-info">Proyecto acontecible y único</p>
      <p class="track-stats">🔥 Diferente</p>
      <a href="https://www.youtube.com/watch?v=J-li4emQsS0" target="_blank" class="track-btn">▶ VER</a>
    </div>
  </div>
  
  <style>
    .tracks-section {
      padding: 80px 20px;
      background: linear-gradient(135deg, rgba(15, 15, 15, 0.95) 0%, rgba(26, 26, 26, 0.95) 100%),
                  url('CRANEO/Batman-Wallpapers-Desktop-32209.jpg') center/cover fixed;
      color: #fff;
      position: relative;
    }
    
    .tracks-section::before {
      content: '';
      position: absolute;
      top: 0;
      left: 0;
      right: 0;
      bottom: 0;
      background: rgba(0, 0, 0, 0.6);
      pointer-events: none;
    }
    
    .tracks-section h2 {
      font-size: 48px;
      text-align: center;
      margin-bottom: 60px;
      color: #ffbe0b;
      text-transform: uppercase;
      letter-spacing: 2px;
      font-weight: 900;
      position: relative;
      z-index: 1;
    }
    
    .tracks-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
      gap: 30px;
      max-width: 1200px;
      margin: 0 auto;
      position: relative;
      z-index: 1;
    }
    
    .track-card {
      background: linear-gradient(135deg, #1a1a1a, #2d2d2d);
      border: 2px solid #333;
      border-left: 4px solid #ff006e;
      padding: 30px;
      border-radius: 8px;
      transition: all 0.3s ease;
      position: relative;
      overflow: hidden;
    }
    
    .track-card::before {
      content: '';
      position: absolute;
      top: 0;
      left: -100%;
      width: 100%;
      height: 100%;
      background: linear-gradient(90deg, transparent, rgba(255, 0, 110, 0.1), transparent);
      transition: left 0.3s ease;
    }
    
    .track-card:hover {
      transform: translateY(-10px);
      border-color: #ff006e;
      box-shadow: 0 20px 40px rgba(255, 0, 110, 0.2);
    }
    
    .track-card:hover::before {
      left: 100%;
    }
    
    .track-number {
      font-size: 48px;
      font-weight: 900;
      color: #ffbe0b;
      margin-bottom: 10px;
      opacity: 0.3;
    }
    
    .track-card h3 {
      font-size: 24px;
      margin: 0 0 10px 0;
      text-transform: uppercase;
      font-weight: 900;
      letter-spacing: 1px;
    }
    
    .track-info {
      font-size: 14px;
      color: #bbb;
      margin: 10px 0;
      font-style: italic;
    }
    
    .track-stats {
      font-size: 13px;
      color: #ffbe0b;
      font-weight: 700;
      margin: 15px 0;
    }
    
    .track-btn {
      display: inline-block;
      background: linear-gradient(90deg, #ff006e, #fb5607);
      color: white;
      padding: 10px 20px;
      text-decoration: none;
      border-radius: 4px;
      font-weight: 700;
      text-transform: uppercase;
      font-size: 12px;
      letter-spacing: 1px;
      transition: all 0.3s ease;
    }
    
    .track-btn:hover {
      transform: scale(1.1);
      box-shadow: 0 5px 15px rgba(255, 0, 110, 0.3);
    }
  </style>
</div>

---

<!-- Gallery Section -->
<div class="gallery-section" id="gallery">
  <h2>🎨 VISUAL CRANEO 🎨</h2>
  <p class="gallery-subtitle">Arte y estética que define mi música</p>
  <div class="gallery-grid">
    <div class="gallery-item"><img src="CRANEO/SPOOKY (1) (1).png" alt="Spooky Art" loading="lazy"></div>
    <div class="gallery-item"><img src="CRANEO/@720pts.jpeg" alt="720pts" loading="lazy"></div>
    <div class="gallery-item"><img src="CRANEO/GcM5IGVXMAAPiLF.jpeg" alt="Visual Art" loading="lazy"></div>
    <div class="gallery-item"><img src="CRANEO/_Freedom starts from within__.jpeg" alt="Freedom" loading="lazy"></div>
    <div class="gallery-item"><img src="CRANEO/download - 2025-12-09T124825.697.jpg" alt="Art 1" loading="lazy"></div>
    <div class="gallery-item"><img src="CRANEO/download - 2025-12-09T125039.980.jpg" alt="Art 2" loading="lazy"></div>
    <div class="gallery-item"><img src="CRANEO/download - 2025-12-09T125120.584.jpg" alt="Art 3" loading="lazy"></div>
    <div class="gallery-item"><img src="CRANEO/download - 2025-12-09T125323.452.jpg" alt="Art 4" loading="lazy"></div>
    <div class="gallery-item"><img src="CRANEO/silver-surfer-all-alone-in-the-space-wallpaper-with-ai-v0-68daljq9mide1.webp" alt="Silver Surfer" loading="lazy"></div>
    <div class="gallery-item"><img src="CRANEO/god.jpg" alt="God" loading="lazy"></div>
    <div class="gallery-item"><img src="CRANEO/pollloooo.jpeg" alt="Pollo" loading="lazy"></div>
    <div class="gallery-item"><img src="CRANEO/🂡 ʳˡʸᶜʳᵘˢʰ.jpeg" alt="Crush" loading="lazy"></div>
  </div>
  
  <style>
    .gallery-section {
      padding: 80px 20px;
      background: linear-gradient(135deg, #0f0f0f 0%, #1a1a1a 100%);
      color: #fff;
    }
    
    .gallery-section h2 {
      font-size: 48px;
      text-align: center;
      margin-bottom: 20px;
      color: #8338ec;
      text-transform: uppercase;
      letter-spacing: 2px;
      font-weight: 900;
    }
    
    .gallery-subtitle {
      text-align: center;
      font-size: 20px;
      color: #bbb;
      margin-bottom: 50px;
      font-style: italic;
    }
    
    .gallery-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
      gap: 20px;
      max-width: 1400px;
      margin: 0 auto;
    }
    
    .gallery-item {
      position: relative;
      overflow: hidden;
      border-radius: 10px;
      border: 3px solid #333;
      transition: all 0.4s ease;
      aspect-ratio: 1;
      background: #000;
    }
    
    .gallery-item:hover {
      transform: scale(1.05) rotate(2deg);
      border-color: #ff006e;
      box-shadow: 0 20px 50px rgba(255, 0, 110, 0.5);
      z-index: 10;
    }
    
    .gallery-item img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      transition: all 0.4s ease;
    }
    
    .gallery-item:hover img {
      transform: scale(1.1);
      filter: brightness(1.2) saturate(1.3);
    }
  </style>
</div>

---

<!-- Featured Projects Section -->
<div class="projects-section" id="projects">
  <h2>🚀 MIS PROYECTOS DESTACADOS 🚀</h2>
  <div class="projects-grid">
    <div class="project-card">
      <div class="project-icon">🎬</div>
      <h3>CANAL DE YOUTUBE</h3>
      <p>Todo mi contenido audiovisual, videos musicales, y proyectos visuales están en mi canal oficial. Suscríbete para no perderte nada.</p>
      <div class="project-meta">
        <span class="tag">Videos</span>
        <span class="tag">Music</span>
      </div>
      <a href="https://www.youtube.com/@susinirgs" target="_blank" class="project-link">Ver Canal →</a>
    </div>
    
    <div class="project-card">
      <div class="project-icon">🎵</div>
      <h3>SPOTIFY OFICIAL</h3>
      <p>Toda mi discografía disponible en Spotify. Escucha mis tracks, álbumes y proyectos completos.</p>
      <div class="project-meta">
        <span class="tag">Streaming</span>
        <span class="tag">Music</span>
      </div>
      <a href="https://open.spotify.com/intl-es/artist/78uCfenEleQDaQJM21K2fk?si=7O3kEBUITZyZWnRXtJ8bhg" target="_blank" class="project-link">Escuchar →</a>
    </div>
    
    <div class="project-card">
      <div class="project-icon">📸</div>
      <h3>INSTAGRAM</h3>
      <p>Sígueme en Instagram para ver contenido exclusivo, behind the scenes, y actualizaciones diarias.</p>
      <div class="project-meta">
        <span class="tag">Social</span>
        <span class="tag">Daily</span>
      </div>
      <a href="https://www.instagram.com/susinirgs/" target="_blank" class="project-link">Seguir →</a>
    </div>
    
    <div class="project-card">
      <div class="project-icon">🎙️</div>
      <h3>PROYECTO RECIENTE</h3>
      <p>Mi trabajo más fresco y reciente. Un proyecto que representa mi evolución artística y creativa.</p>
      <div class="project-meta">
        <span class="tag">New</span>
        <span class="tag">Fresh</span>
      </div>
      <a href="https://www.youtube.com/watch?v=cB5sIhH067A" target="_blank" class="project-link">Ver →</a>
    </div>
    
    <div class="project-card">
      <div class="project-icon">🧠</div>
      <h3>VIDEO MÁS CRANEADO</h3>
      <p>El video que más cerebro me voló hacer. Creatividad pura y conceptos únicos.</p>
      <div class="project-meta">
        <span class="tag">Creative</span>
        <span class="tag">Mind-Blown</span>
      </div>
      <a href="https://www.youtube.com/watch?v=uDAziScqsUk" target="_blank" class="project-link">Ver →</a>
    </div>
    
    <div class="project-card">
      <div class="project-icon">✨</div>
      <h3>ENERGÍA MÍSTICA</h3>
      <p>Proyecto con vibras cósmicas y energía universal. Una experiencia única y espiritual.</p>
      <div class="project-meta">
        <span class="tag">Mystic</span>
        <span class="tag">Energy</span>
      </div>
      <a href="https://www.youtube.com/watch?v=zAjGlkn3udw" target="_blank" class="project-link">Ver →</a>
    </div>
  </div>
  
  <style>
    .projects-section {
      padding: 80px 20px;
      background: linear-gradient(135deg, #1a1a1a 0%, #0f0f0f 100%);
      color: #fff;
    }
    
    .projects-section h2 {
      font-size: 48px;
      text-align: center;
      margin-bottom: 60px;
      color: #ff006e;
      text-transform: uppercase;
      letter-spacing: 2px;
      font-weight: 900;
    }
    
    .projects-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
      gap: 30px;
      max-width: 1200px;
      margin: 0 auto;
    }
    
    .project-card {
      background: linear-gradient(135deg, #2d2d2d, #1a1a1a);
      padding: 40px 30px;
      border-radius: 8px;
      border: 2px solid #333;
      border-top: 3px solid #8338ec;
      transition: all 0.3s ease;
      display: flex;
      flex-direction: column;
    }
    
    .project-card:hover {
      transform: translateY(-15px);
      border-color: #8338ec;
      box-shadow: 0 30px 50px rgba(131, 56, 236, 0.2);
    }
    
    .project-icon {
      font-size: 48px;
      margin-bottom: 15px;
    }
    
    .project-card h3 {
      font-size: 22px;
      margin: 0 0 15px 0;
      text-transform: uppercase;
      font-weight: 900;
      letter-spacing: 1px;
    }
    
    .project-card p {
      font-size: 14px;
      color: #bbb;
      margin: 0 0 20px 0;
      line-height: 1.6;
      flex-grow: 1;
    }
    
    .project-meta {
      display: flex;
      gap: 10px;
      margin-bottom: 20px;
      flex-wrap: wrap;
    }
    
    .tag {
      display: inline-block;
      background: rgba(255, 190, 11, 0.1);
      color: #ffbe0b;
      padding: 5px 12px;
      border-radius: 20px;
      font-size: 12px;
      font-weight: 700;
      text-transform: uppercase;
      letter-spacing: 0.5px;
      border: 1px solid #ffbe0b;
    }
    
    .project-link {
      display: inline-block;
      color: #ff006e;
      text-decoration: none;
      font-weight: 700;
      font-size: 14px;
      text-transform: uppercase;
      letter-spacing: 1px;
      transition: all 0.3s ease;
      align-self: flex-start;
    }
    
    .project-link:hover {
      color: #ffbe0b;
      transform: translateX(5px);
    }
  </style>
</div>

---

<!-- Social Links Section -->
<div class="social-section" id="connect">
  <h2>🔗 CONNECT WITH ME 🔗</h2>
  <p class="social-subtitle">Join the community and stay updated with fresh beats & announcements</p>
  
  <div class="social-links">
    <a href="https://open.spotify.com/intl-es/artist/78uCfenEleQDaQJM21K2fk?si=7O3kEBUITZyZWnRXtJ8bhg" target="_blank" class="social-btn spotify" title="Spotify">
      <span class="icon">🎵</span>
      <span class="label">Spotify</span>
    </a>
    <a href="https://www.youtube.com/@susinirgs" target="_blank" class="social-btn youtube" title="YouTube">
      <span class="icon">▶️</span>
      <span class="label">YouTube</span>
    </a>
    <a href="https://www.instagram.com/susinirgs/" target="_blank" class="social-btn instagram" title="Instagram">
      <span class="icon">📸</span>
      <span class="label">Instagram</span>
    </a>
  </div>
  
  <style>
    .social-section {
      padding: 80px 20px;
      background: linear-gradient(135deg, #8338ec 0%, #ff006e 100%);
      text-align: center;
      color: #fff;
    }
    
    .social-section h2 {
      font-size: 48px;
      margin-bottom: 15px;
      text-transform: uppercase;
      font-weight: 900;
      letter-spacing: 2px;
    }
    
    .social-subtitle {
      font-size: 18px;
      margin-bottom: 50px;
      color: rgba(255, 255, 255, 0.9);
      font-weight: 300;
    }
    
    .social-links {
      display: flex;
      gap: 20px;
      justify-content: center;
      flex-wrap: wrap;
      max-width: 900px;
      margin: 0 auto;
    }
    
    .social-btn {
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      gap: 8px;
      width: 100px;
      height: 100px;
      background: rgba(255, 255, 255, 0.1);
      border: 2px solid rgba(255, 255, 255, 0.3);
      border-radius: 10px;
      text-decoration: none;
      color: #fff;
      transition: all 0.3s ease;
      font-weight: 700;
      font-size: 12px;
      text-transform: uppercase;
      letter-spacing: 0.5px;
    }
    
    .social-btn .icon {
      font-size: 32px;
      display: block;
    }
    
    .social-btn .label {
      display: block;
    }
    
    .social-btn:hover {
      background: rgba(255, 255, 255, 0.2);
      border-color: rgba(255, 255, 255, 0.8);
      transform: translateY(-5px);
      box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
    }
    
    .social-btn.spotify:hover {
      border-color: #1DB954;
      background: rgba(29, 185, 84, 0.2);
    }
    
    .social-btn.soundcloud:hover {
      border-color: #FF7700;
      background: rgba(255, 119, 0, 0.2);
    }
    
    .social-btn.youtube:hover {
      border-color: #FF0000;
      background: rgba(255, 0, 0, 0.2);
    }
    
    .social-btn.twitter:hover {
      border-color: #1DA1F2;
      background: rgba(29, 161, 242, 0.2);
    }
    
    .social-btn.instagram:hover {
      border-color: #E4405F;
      background: rgba(228, 64, 95, 0.2);
    }
    
    .social-btn.discord:hover {
      border-color: #5865F2;
      background: rgba(88, 101, 242, 0.2);
    }
    
    .social-btn.tiktok:hover {
      border-color: #25F4EE;
      background: rgba(37, 244, 238, 0.2);
    }
    
    .social-btn.email:hover {
      border-color: #ffbe0b;
      background: rgba(255, 190, 11, 0.2);
    }
  </style>
</div>

---

<!-- Footer -->
<footer class="footer">
  <div class="footer-content">
    <div class="footer-logo">
      <h3>SUSINIRGS</h3>
      <p>🔥 TRAP | HIP-HOP | BEATS 🔥</p>
    </div>
    <div class="footer-links">
      <a href="https://www.youtube.com/@susinirgs" target="_blank">YouTube</a>
      <a href="https://open.spotify.com/intl-es/artist/78uCfenEleQDaQJM21K2fk?si=7O3kEBUITZyZWnRXtJ8bhg" target="_blank">Spotify</a>
      <a href="https://www.instagram.com/susinirgs/" target="_blank">Instagram</a>
    </div>
    <p class="footer-copy">&copy; 2025 SUSINIRGS. All Rights Reserved.</p>
    <p class="footer-tagline">🎵 Made with passion for the culture | Energía Mística Universal 🎵</p>
  </div>
  <style>
    .footer {
      background: linear-gradient(135deg, #0a0e27 0%, #1a1a3e 100%);
      color: #888;
      text-align: center;
      padding: 50px 20px;
      border-top: 3px solid #ff006e;
      font-size: 14px;
      position: relative;
      overflow: hidden;
    }
    
    .footer::before {
      content: '';
      position: absolute;
      top: 0;
      left: 0;
      right: 0;
      height: 3px;
      background: linear-gradient(90deg, #ff006e, #ffbe0b, #8338ec, #00ff00);
      animation: rainbow 5s linear infinite;
    }
    
    @keyframes rainbow {
      0% { background-position: 0% 50%; }
      100% { background-position: 100% 50%; }
    }
    
    .footer-content {
      max-width: 800px;
      margin: 0 auto;
    }
    
    .footer-logo h3 {
      font-size: 32px;
      color: #ff006e;
      margin: 0 0 10px 0;
      text-transform: uppercase;
      letter-spacing: 3px;
    }
    
    .footer-logo p {
      color: #ffbe0b;
      font-weight: 700;
      margin: 5px 0 30px 0;
    }
    
    .footer-links {
      display: flex;
      gap: 30px;
      justify-content: center;
      margin: 30px 0;
      flex-wrap: wrap;
    }
    
    .footer-links a {
      color: #00f5ff;
      text-decoration: none;
      font-weight: 700;
      text-transform: uppercase;
      letter-spacing: 1px;
      transition: all 0.3s ease;
      border-bottom: 2px solid transparent;
    }
    
    .footer-links a:hover {
      color: #00ff00;
      border-bottom-color: #00ff00;
      text-shadow: 0 0 10px #00ff00;
    }
    
    .footer-copy {
      margin: 30px 0 10px 0;
      color: #bbb;
    }
    
    .footer-tagline {
      color: #888;
      font-size: 12px;
      font-style: italic;
    }
  </style>
</footer>
