---
layout: default
title: SUSINIRGS - Artista Trap & Productor Musical
---

<!-- Animated Particles Background -->
<div id="particles-container"></div>

<!-- Floating Navigation -->
<nav class="floating-nav" id="main-nav">
  <div class="nav-toggle" onclick="toggleNav()">☰</div>
  <div class="nav-links">
    <a href="#hero" class="nav-link active">🏠 Inicio</a>
    <a href="#about" class="nav-link">👤 Sobre Mí</a>
    <a href="#music" class="nav-link">🎵 Música</a>
    <a href="#videos" class="nav-link">🎬 Videos</a>
    <a href="#gallery" class="nav-link">🎨 Galería</a>
    <a href="#stats" class="nav-link">📊 Logros</a>
    <a href="#connect" class="nav-link">🔗 Conectar</a>
  </div>
</nav>

<style>
  /* ===== PARTICLE ANIMATION ===== */
  #particles-container {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    pointer-events: none;
    z-index: 0;
    overflow: hidden;
  }
  
  .particle {
    position: absolute;
    width: 4px;
    height: 4px;
    background: radial-gradient(circle, #ff006e 0%, transparent 70%);
    border-radius: 50%;
    animation: floatParticle 15s infinite ease-in-out;
    opacity: 0.6;
  }
  
  @keyframes floatParticle {
    0%, 100% { transform: translateY(100vh) translateX(0) scale(0); opacity: 0; }
    10% { opacity: 0.8; transform: scale(1); }
    90% { opacity: 0.8; }
    100% { transform: translateY(-10vh) translateX(100px) scale(0); opacity: 0; }
  }
  
  /* ===== NAVIGATION ===== */
  .floating-nav {
    position: fixed;
    top: 20px;
    right: 20px;
    z-index: 9999;
    background: rgba(10, 14, 39, 0.95);
    border: 2px solid #ff006e;
    border-radius: 15px;
    padding: 15px;
    box-shadow: 0 10px 40px rgba(255, 0, 110, 0.3), 0 0 60px rgba(131, 56, 236, 0.2);
    backdrop-filter: blur(15px);
    transition: all 0.4s cubic-bezier(0.25, 0.8, 0.25, 1);
  }
  
  .floating-nav:hover {
    box-shadow: 0 15px 50px rgba(255, 0, 110, 0.5), 0 0 80px rgba(131, 56, 236, 0.3);
    border-color: #ffbe0b;
  }
  
  .nav-toggle {
    display: none;
    color: #ff006e;
    font-size: 24px;
    cursor: pointer;
    text-align: center;
  }
  
  .nav-links {
    display: flex;
    flex-direction: column;
    gap: 8px;
  }
  
  .floating-nav .nav-link {
    color: #00f5ff;
    text-decoration: none;
    font-size: 13px;
    font-weight: 700;
    text-transform: uppercase;
    padding: 10px 18px;
    border-radius: 8px;
    transition: all 0.3s cubic-bezier(0.25, 0.8, 0.25, 1);
    border: 1px solid transparent;
    white-space: nowrap;
    position: relative;
    overflow: hidden;
  }
  
  .floating-nav .nav-link::before {
    content: '';
    position: absolute;
    top: 0;
    left: -100%;
    width: 100%;
    height: 100%;
    background: linear-gradient(90deg, transparent, rgba(255, 0, 110, 0.3), transparent);
    transition: left 0.5s;
  }
  
  .floating-nav .nav-link:hover::before {
    left: 100%;
  }
  
  .floating-nav .nav-link:hover {
    background: rgba(255, 0, 110, 0.2);
    border-color: #ff006e;
    color: #ffbe0b;
    transform: translateX(-8px);
    box-shadow: 0 0 20px rgba(255, 0, 110, 0.3);
  }
  
  .floating-nav .nav-link.active {
    background: linear-gradient(135deg, rgba(255, 0, 110, 0.3), rgba(131, 56, 236, 0.3));
    border-color: #ff006e;
  }
  
  @media (max-width: 768px) {
    .floating-nav {
      top: 10px;
      right: 10px;
      left: 10px;
      padding: 12px;
    }
    
    .nav-toggle {
      display: block;
    }
    
    .nav-links {
      display: none;
      flex-direction: row;
      flex-wrap: wrap;
      gap: 5px;
      margin-top: 10px;
    }
    
    .nav-links.show {
      display: flex;
    }
    
    .floating-nav .nav-link {
      font-size: 10px;
      padding: 6px 10px;
    }
  }
</style>

<script>
  // Create floating particles
  function createParticles() {
    const container = document.getElementById('particles-container');
    const colors = ['#ff006e', '#ffbe0b', '#8338ec', '#00f5ff', '#00ff00'];
    
    for (let i = 0; i < 50; i++) {
      const particle = document.createElement('div');
      particle.className = 'particle';
      particle.style.left = Math.random() * 100 + '%';
      particle.style.animationDelay = Math.random() * 15 + 's';
      particle.style.animationDuration = (10 + Math.random() * 20) + 's';
      particle.style.background = `radial-gradient(circle, ${colors[Math.floor(Math.random() * colors.length)]} 0%, transparent 70%)`;
      particle.style.width = (3 + Math.random() * 5) + 'px';
      particle.style.height = particle.style.width;
      container.appendChild(particle);
    }
  }
  
  // Toggle mobile nav
  function toggleNav() {
    document.querySelector('.nav-links').classList.toggle('show');
  }
  
  // Initialize particles on load
  document.addEventListener('DOMContentLoaded', createParticles);
  
  // Smooth scroll highlight
  document.addEventListener('scroll', function() {
    const sections = document.querySelectorAll('[id]');
    const navLinks = document.querySelectorAll('.nav-link');
    let current = '';
    
    sections.forEach(section => {
      const sectionTop = section.offsetTop;
      if (pageYOffset >= sectionTop - 200) {
        current = section.getAttribute('id');
      }
    });
    
    navLinks.forEach(link => {
      link.classList.remove('active');
      if (link.getAttribute('href') === '#' + current) {
        link.classList.add('active');
      }
    });
  });
</script>

<!-- Hero Section -->
<div class="hero-section" id="hero">
  <div class="hero-bg-overlay"></div>
  <div class="hero-content">
    <div class="artist-avatar">
      <div class="avatar-glow"></div>
      <div class="avatar-ring"></div>
      <span class="avatar-icon">🎤</span>
    </div>
    <div class="artist-logo">
      <h1 class="artist-name glitch" data-text="SUSINIRGS">SUSINIRGS</h1>
      <div class="tagline-container">
        <span class="tagline-word">🔥 TRAP</span>
        <span class="tagline-divider">•</span>
        <span class="tagline-word">HIP-HOP</span>
        <span class="tagline-divider">•</span>
        <span class="tagline-word">BEATS 🔥</span>
      </div>
    </div>
    <p class="hero-subtitle">
      <span class="typing-text">Artista Independiente | Productor Musical | Energía Mística Universal</span>
    </p>
    <div class="hero-stats">
      <div class="stat-item">
        <span class="stat-number">+15</span>
        <span class="stat-label">Proyectos</span>
      </div>
      <div class="stat-divider"></div>
      <div class="stat-item">
        <span class="stat-number">2024</span>
        <span class="stat-label">Activo</span>
      </div>
      <div class="stat-divider"></div>
      <div class="stat-item">
        <span class="stat-number">🌎</span>
        <span class="stat-label">Global</span>
      </div>
    </div>
    <div class="hero-cta">
      <a href="#music" class="btn btn-primary pulse-btn">
        <span class="btn-icon">▶</span> Escuchar Ahora
      </a>
      <a href="#about" class="btn btn-secondary">
        <span class="btn-icon">👤</span> Conocer Más
      </a>
    </div>
    <div class="scroll-indicator">
      <span class="scroll-text">Desliza hacia abajo</span>
      <div class="scroll-arrow">↓</div>
    </div>
  </div>
  
  <style>
    .hero-section {
      background: linear-gradient(135deg, rgba(0, 0, 0, 0.9) 0%, rgba(26, 26, 62, 0.95) 100%), 
                  url('CRANEO/silver-surfer-all-alone-in-the-space-wallpaper-with-ai-v0-68daljq9mide1.webp') center/cover fixed;
      color: #fff;
      padding: 140px 20px 100px;
      text-align: center;
      position: relative;
      overflow: hidden;
      min-height: 100vh;
      display: flex;
      align-items: center;
      justify-content: center;
    }
    
    .hero-bg-overlay {
      position: absolute;
      top: 0;
      left: 0;
      right: 0;
      bottom: 0;
      background: 
        radial-gradient(ellipse at 20% 80%, rgba(255, 0, 110, 0.15) 0%, transparent 50%),
        radial-gradient(ellipse at 80% 20%, rgba(131, 56, 236, 0.15) 0%, transparent 50%),
        radial-gradient(ellipse at 50% 50%, rgba(0, 245, 255, 0.08) 0%, transparent 60%);
      pointer-events: none;
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
        rgba(255, 0, 110, 0.02) 10px,
        rgba(255, 0, 110, 0.02) 20px
      );
      pointer-events: none;
      animation: slide 30s linear infinite;
    }
    
    .hero-section::after {
      content: '';
      position: absolute;
      bottom: 0;
      left: 0;
      right: 0;
      height: 200px;
      background: linear-gradient(to top, #0a0e27, transparent);
      pointer-events: none;
    }
    
    @keyframes slide {
      0% { background-position: 0 0; }
      100% { background-position: 100px 100px; }
    }
    
    @keyframes float {
      0%, 100% { transform: translateY(0px); }
      50% { transform: translateY(-15px); }
    }
    
    @keyframes pulse {
      0%, 100% { opacity: 1; box-shadow: 0 0 20px rgba(255, 0, 110, 0.5); }
      50% { opacity: 0.9; box-shadow: 0 0 40px rgba(255, 0, 110, 0.8); }
    }
    
    @keyframes rotate {
      from { transform: rotate(0deg); }
      to { transform: rotate(360deg); }
    }
    
    @keyframes glitchAnim {
      0% { clip-path: inset(40% 0 61% 0); transform: translate(-2px, 2px); }
      20% { clip-path: inset(92% 0 1% 0); transform: translate(2px, -2px); }
      40% { clip-path: inset(43% 0 1% 0); transform: translate(-2px, 2px); }
      60% { clip-path: inset(25% 0 58% 0); transform: translate(2px, -2px); }
      80% { clip-path: inset(54% 0 7% 0); transform: translate(-2px, 2px); }
      100% { clip-path: inset(58% 0 43% 0); transform: translate(2px, -2px); }
    }
    
    .hero-content {
      position: relative;
      z-index: 1;
      animation: float 8s ease-in-out infinite;
    }
    
    .artist-avatar {
      position: relative;
      width: 120px;
      height: 120px;
      margin: 0 auto 30px;
    }
    
    .avatar-glow {
      position: absolute;
      top: -10px;
      left: -10px;
      right: -10px;
      bottom: -10px;
      background: radial-gradient(circle, rgba(255, 0, 110, 0.4) 0%, transparent 70%);
      border-radius: 50%;
      animation: pulse 3s ease-in-out infinite;
    }
    
    .avatar-ring {
      position: absolute;
      top: -5px;
      left: -5px;
      right: -5px;
      bottom: -5px;
      border: 3px solid transparent;
      border-top-color: #ff006e;
      border-right-color: #ffbe0b;
      border-bottom-color: #8338ec;
      border-left-color: #00f5ff;
      border-radius: 50%;
      animation: rotate 4s linear infinite;
    }
    
    .avatar-icon {
      display: flex;
      align-items: center;
      justify-content: center;
      width: 100%;
      height: 100%;
      font-size: 50px;
      background: linear-gradient(135deg, #1a1a3e, #0a0e27);
      border-radius: 50%;
      border: 3px solid #333;
    }
    
    .artist-logo {
      margin-bottom: 25px;
    }
    
    .artist-name {
      font-size: 80px;
      font-weight: 900;
      margin: 0;
      text-transform: uppercase;
      letter-spacing: 5px;
      background: linear-gradient(90deg, #ff006e, #ffbe0b, #8338ec, #00f5ff);
      background-size: 300% 100%;
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      background-clip: text;
      animation: gradientShift 5s ease infinite;
      position: relative;
    }
    
    @keyframes gradientShift {
      0% { background-position: 0% 50%; }
      50% { background-position: 100% 50%; }
      100% { background-position: 0% 50%; }
    }
    
    .artist-name.glitch::before,
    .artist-name.glitch::after {
      content: attr(data-text);
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: linear-gradient(90deg, #ff006e, #ffbe0b, #8338ec);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      background-clip: text;
    }
    
    .artist-name.glitch::before {
      animation: glitchAnim 3s infinite linear alternate-reverse;
      color: #ff006e;
      z-index: -1;
    }
    
    .artist-name.glitch::after {
      animation: glitchAnim 2s infinite linear alternate-reverse;
      color: #00f5ff;
      z-index: -2;
    }
    
    .tagline-container {
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 15px;
      margin-top: 15px;
      flex-wrap: wrap;
    }
    
    .tagline-word {
      font-size: 20px;
      font-weight: 800;
      color: #ffbe0b;
      letter-spacing: 3px;
      text-transform: uppercase;
      text-shadow: 0 0 20px rgba(255, 190, 11, 0.5);
    }
    
    .tagline-divider {
      color: #ff006e;
      font-size: 24px;
    }
    
    .hero-subtitle {
      font-size: 18px;
      color: #e0e0e0;
      margin: 25px 0 30px 0;
      font-weight: 400;
      letter-spacing: 1px;
    }
    
    .hero-stats {
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 30px;
      margin-bottom: 40px;
      flex-wrap: wrap;
    }
    
    .stat-item {
      text-align: center;
    }
    
    .stat-number {
      display: block;
      font-size: 32px;
      font-weight: 900;
      color: #00f5ff;
      text-shadow: 0 0 20px rgba(0, 245, 255, 0.5);
    }
    
    .stat-label {
      font-size: 12px;
      color: #888;
      text-transform: uppercase;
      letter-spacing: 2px;
    }
    
    .stat-divider {
      width: 2px;
      height: 40px;
      background: linear-gradient(to bottom, transparent, #ff006e, transparent);
    }
    
    .hero-cta {
      display: flex;
      gap: 20px;
      justify-content: center;
      flex-wrap: wrap;
      margin-bottom: 50px;
    }
    
    .btn {
      padding: 18px 35px;
      font-size: 15px;
      font-weight: 700;
      text-transform: uppercase;
      letter-spacing: 1px;
      border: none;
      cursor: pointer;
      transition: all 0.4s cubic-bezier(0.25, 0.8, 0.25, 1);
      text-decoration: none;
      display: inline-flex;
      align-items: center;
      gap: 10px;
      border-radius: 50px;
    }
    
    .btn-icon {
      font-size: 14px;
    }
    
    .btn-primary {
      background: linear-gradient(135deg, #ff006e, #fb5607);
      color: white;
      box-shadow: 0 10px 30px rgba(255, 0, 110, 0.4);
    }
    
    .btn-primary.pulse-btn {
      animation: btnPulse 2s infinite;
    }
    
    @keyframes btnPulse {
      0%, 100% { box-shadow: 0 10px 30px rgba(255, 0, 110, 0.4); }
      50% { box-shadow: 0 15px 50px rgba(255, 0, 110, 0.6); }
    }
    
    .btn-primary:hover {
      transform: translateY(-5px) scale(1.05);
      box-shadow: 0 20px 50px rgba(255, 0, 110, 0.6);
    }
    
    .btn-secondary {
      background: transparent;
      color: #ffbe0b;
      border: 2px solid #ffbe0b;
    }
    
    .btn-secondary:hover {
      background: #ffbe0b;
      color: #1a1a1a;
      transform: translateY(-5px) scale(1.05);
      box-shadow: 0 15px 40px rgba(255, 190, 11, 0.4);
    }
    
    .scroll-indicator {
      position: absolute;
      bottom: 30px;
      left: 50%;
      transform: translateX(-50%);
      text-align: center;
      animation: bounce 2s infinite;
    }
    
    @keyframes bounce {
      0%, 20%, 50%, 80%, 100% { transform: translateX(-50%) translateY(0); }
      40% { transform: translateX(-50%) translateY(-15px); }
      60% { transform: translateX(-50%) translateY(-7px); }
    }
    
    .scroll-text {
      font-size: 11px;
      color: #666;
      text-transform: uppercase;
      letter-spacing: 2px;
      display: block;
      margin-bottom: 8px;
    }
    
    .scroll-arrow {
      font-size: 20px;
      color: #ff006e;
    }
    
    @media (max-width: 768px) {
      .artist-name {
        font-size: 42px !important;
        letter-spacing: 2px !important;
      }
      
      .tagline-word {
        font-size: 14px !important;
      }
      
      .hero-subtitle {
        font-size: 14px !important;
      }
      
      .hero-section {
        padding: 120px 15px 80px !important;
        min-height: auto !important;
      }
      
      .artist-avatar {
        width: 80px;
        height: 80px;
      }
      
      .avatar-icon {
        font-size: 35px;
      }
      
      .stat-number {
        font-size: 24px;
      }
      
      .hero-stats {
        gap: 15px;
      }
      
      .btn {
        padding: 14px 25px;
        font-size: 13px;
      }
    }
  </style>
</div>

<!-- About Section - Sobre Mí -->
<div class="about-section" id="about">
  <div class="about-container">
    <div class="section-header">
      <span class="section-tag">Conóceme</span>
      <h2>👤 SOBRE MÍ</h2>
      <div class="header-line"></div>
    </div>
    
    <div class="about-content">
      <div class="about-image">
        <div class="image-frame">
          <img src="CRANEO/download - 2025-12-09T125353.235.jpg" alt="SUSINIRGS">
          <div class="image-glow"></div>
        </div>
        <div class="image-badge">
          <span class="badge-text">ARTISTA INDEPENDIENTE</span>
        </div>
      </div>
      
      <div class="about-text">
        <h3 class="about-title">🔥 La Voz del Underground 🔥</h3>
        <p class="about-intro">
          <strong>SUSINIRGS</strong> es un artista independiente de Trap y Hip-Hop que fusiona 
          sonidos oscuros con vibras cósmicas, creando una experiencia musical única que trasciende 
          los límites del género.
        </p>
        
        <div class="about-details">
          <div class="detail-item">
            <span class="detail-icon">🎤</span>
            <div class="detail-content">
              <h4>Estilo Musical</h4>
              <p>Trap experimental, Hip-Hop alternativo, beats oscuros con toques de misticismo y espiritualidad.</p>
            </div>
          </div>
          
          <div class="detail-item">
            <span class="detail-icon">🌌</span>
            <div class="detail-content">
              <h4>Filosofía Artística</h4>
              <p>Energía Mística Universal - cada track es un viaje por dimensiones sonoras inexploradas, donde el flow se encuentra con la consciencia.</p>
            </div>
          </div>
          
          <div class="detail-item">
            <span class="detail-icon">🧠</span>
            <div class="detail-content">
              <h4>Visión Creativa</h4>
              <p>Producción propia, lírica consciente y visuales cinematográficos. Cada proyecto es una obra de arte completa.</p>
            </div>
          </div>
        </div>
        
        <blockquote class="artist-quote">
          <span class="quote-mark">"</span>
          La música es el portal hacia otras dimensiones. Cada beat es una frecuencia que conecta almas.
          <span class="quote-mark">"</span>
          <cite>— SUSINIRGS</cite>
        </blockquote>
        
        <div class="about-cta">
          <a href="#music" class="btn-about">Escuchar Mi Música</a>
          <a href="#videos" class="btn-about secondary">Ver Videos</a>
        </div>
      </div>
    </div>
  </div>
  
  <style>
    .about-section {
      padding: 100px 20px;
      background: linear-gradient(180deg, #0a0e27 0%, #1a1a3e 50%, #0f0f2e 100%);
      color: #fff;
      position: relative;
      overflow: hidden;
    }
    
    .about-section::before {
      content: '';
      position: absolute;
      top: 0;
      left: 0;
      right: 0;
      height: 3px;
      background: linear-gradient(90deg, transparent, #ff006e, #ffbe0b, #8338ec, transparent);
    }
    
    .about-container {
      max-width: 1200px;
      margin: 0 auto;
    }
    
    .section-header {
      text-align: center;
      margin-bottom: 60px;
    }
    
    .section-tag {
      display: inline-block;
      background: linear-gradient(135deg, rgba(255, 0, 110, 0.2), rgba(131, 56, 236, 0.2));
      color: #ff006e;
      padding: 8px 20px;
      border-radius: 30px;
      font-size: 12px;
      font-weight: 700;
      text-transform: uppercase;
      letter-spacing: 3px;
      margin-bottom: 15px;
      border: 1px solid rgba(255, 0, 110, 0.3);
    }
    
    .section-header h2 {
      font-size: 48px;
      font-weight: 900;
      margin: 0 0 20px 0;
      text-transform: uppercase;
      letter-spacing: 3px;
      background: linear-gradient(90deg, #ff006e, #ffbe0b);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      background-clip: text;
    }
    
    .header-line {
      width: 100px;
      height: 4px;
      background: linear-gradient(90deg, #ff006e, #8338ec);
      margin: 0 auto;
      border-radius: 2px;
    }
    
    .about-content {
      display: grid;
      grid-template-columns: 1fr 1.5fr;
      gap: 60px;
      align-items: start;
    }
    
    .about-image {
      position: relative;
    }
    
    .image-frame {
      position: relative;
      border-radius: 20px;
      overflow: hidden;
      border: 3px solid #333;
      transition: all 0.4s ease;
    }
    
    .image-frame:hover {
      border-color: #ff006e;
      transform: scale(1.02);
    }
    
    .image-frame img {
      width: 100%;
      height: auto;
      display: block;
      filter: saturate(1.1) contrast(1.05);
    }
    
    .image-glow {
      position: absolute;
      bottom: 0;
      left: 0;
      right: 0;
      height: 50%;
      background: linear-gradient(to top, rgba(255, 0, 110, 0.3), transparent);
      pointer-events: none;
    }
    
    .image-badge {
      position: absolute;
      bottom: -15px;
      left: 50%;
      transform: translateX(-50%);
      background: linear-gradient(135deg, #ff006e, #8338ec);
      padding: 10px 25px;
      border-radius: 30px;
      box-shadow: 0 10px 30px rgba(255, 0, 110, 0.4);
    }
    
    .badge-text {
      font-size: 11px;
      font-weight: 800;
      letter-spacing: 2px;
      text-transform: uppercase;
      white-space: nowrap;
    }
    
    .about-text {
      padding-top: 10px;
    }
    
    .about-title {
      font-size: 28px;
      font-weight: 900;
      margin: 0 0 20px 0;
      color: #ffbe0b;
    }
    
    .about-intro {
      font-size: 17px;
      line-height: 1.8;
      color: #ddd;
      margin-bottom: 30px;
    }
    
    .about-intro strong {
      color: #00f5ff;
    }
    
    .about-details {
      display: flex;
      flex-direction: column;
      gap: 20px;
      margin-bottom: 30px;
    }
    
    .detail-item {
      display: flex;
      gap: 15px;
      padding: 20px;
      background: rgba(255, 255, 255, 0.03);
      border-radius: 12px;
      border-left: 3px solid #ff006e;
      transition: all 0.3s ease;
    }
    
    .detail-item:hover {
      background: rgba(255, 0, 110, 0.1);
      transform: translateX(10px);
    }
    
    .detail-icon {
      font-size: 30px;
      flex-shrink: 0;
    }
    
    .detail-content h4 {
      font-size: 16px;
      font-weight: 800;
      color: #00f5ff;
      margin: 0 0 8px 0;
      text-transform: uppercase;
      letter-spacing: 1px;
    }
    
    .detail-content p {
      font-size: 14px;
      color: #bbb;
      margin: 0;
      line-height: 1.6;
    }
    
    .artist-quote {
      background: linear-gradient(135deg, rgba(131, 56, 236, 0.15), rgba(255, 0, 110, 0.15));
      border: none;
      border-radius: 15px;
      padding: 30px;
      margin: 30px 0;
      font-style: italic;
      font-size: 18px;
      color: #e0e0e0;
      position: relative;
      line-height: 1.7;
    }
    
    .quote-mark {
      font-size: 40px;
      color: #ff006e;
      font-style: normal;
      line-height: 1;
    }
    
    .artist-quote cite {
      display: block;
      margin-top: 15px;
      font-size: 14px;
      color: #ffbe0b;
      font-style: normal;
      font-weight: 700;
    }
    
    .about-cta {
      display: flex;
      gap: 15px;
      flex-wrap: wrap;
    }
    
    .btn-about {
      padding: 14px 30px;
      background: linear-gradient(135deg, #ff006e, #fb5607);
      color: white;
      text-decoration: none;
      border-radius: 30px;
      font-weight: 700;
      font-size: 13px;
      text-transform: uppercase;
      letter-spacing: 1px;
      transition: all 0.3s ease;
      box-shadow: 0 8px 25px rgba(255, 0, 110, 0.3);
    }
    
    .btn-about:hover {
      transform: translateY(-3px);
      box-shadow: 0 12px 35px rgba(255, 0, 110, 0.5);
    }
    
    .btn-about.secondary {
      background: transparent;
      border: 2px solid #8338ec;
      color: #8338ec;
      box-shadow: none;
    }
    
    .btn-about.secondary:hover {
      background: #8338ec;
      color: white;
    }
    
    @media (max-width: 900px) {
      .about-content {
        grid-template-columns: 1fr;
        gap: 40px;
      }
      
      .about-image {
        max-width: 400px;
        margin: 0 auto;
      }
      
      .section-header h2 {
        font-size: 36px;
      }
      
      .about-title {
        font-size: 24px;
      }
    }
  </style>
</div>

<!-- Music Section with Spotify Embed -->
<div class="music-section" id="music">
  <div class="music-container">
    <div class="section-header">
      <span class="section-tag">Discografía</span>
      <h2>🎵 MI MÚSICA</h2>
      <div class="header-line"></div>
      <p class="section-subtitle">Escucha mis últimos lanzamientos y tracks más populares en las plataformas digitales</p>
    </div>
    
    <div class="music-content">
      <!-- Spotify Player -->
      <div class="spotify-embed">
        <div class="spotify-header">
          <span class="spotify-icon">🎧</span>
          <span class="spotify-title">SPOTIFY</span>
        </div>
        <iframe style="border-radius:12px" src="https://open.spotify.com/embed/artist/78uCfenEleQDaQJM21K2fk?utm_source=generator&theme=0" width="100%" height="400" frameBorder="0" allowfullscreen="" allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture" loading="lazy"></iframe>
        <a href="https://open.spotify.com/intl-es/artist/78uCfenEleQDaQJM21K2fk" target="_blank" class="spotify-link">
          Abrir en Spotify →
        </a>
      </div>
      
      <!-- Featured Tracks List -->
      <div class="tracks-list">
        <h3 class="tracks-title">🔥 PROYECTOS DESTACADOS</h3>
        
        <div class="track-item featured">
          <span class="track-rank">01</span>
          <div class="track-info">
            <span class="track-name">PROYECTO MÁS RECIENTE</span>
            <span class="track-meta">Mi trabajo más fresco y actual</span>
          </div>
          <span class="track-badge">NUEVO</span>
          <a href="https://www.youtube.com/watch?v=cB5sIhH067A" target="_blank" class="track-play">▶</a>
        </div>
        
        <div class="track-item">
          <span class="track-rank">02</span>
          <div class="track-info">
            <span class="track-name">ENERGÍA MÍSTICA UNIVERSAL</span>
            <span class="track-meta">Vibras cósmicas y espirituales</span>
          </div>
          <a href="https://www.youtube.com/watch?v=zAjGlkn3udw" target="_blank" class="track-play">▶</a>
        </div>
        
        <div class="track-item">
          <span class="track-rank">03</span>
          <div class="track-info">
            <span class="track-name">VIDEO MÁS CRANEADO</span>
            <span class="track-meta">El video que más cerebro me voló</span>
          </div>
          <a href="https://www.youtube.com/watch?v=uDAziScqsUk" target="_blank" class="track-play">▶</a>
        </div>
        
        <div class="track-item">
          <span class="track-rank">04</span>
          <div class="track-info">
            <span class="track-name">DATA SAGRADA</span>
            <span class="track-meta">Información pura y espiritual</span>
          </div>
          <a href="https://www.youtube.com/watch?v=VcEhBUNhPs4" target="_blank" class="track-play">▶</a>
        </div>
        
        <div class="track-item">
          <span class="track-rank">05</span>
          <div class="track-info">
            <span class="track-name">MÁS RAPERO</span>
            <span class="track-meta">Flow puro y lírica real</span>
          </div>
          <a href="https://www.youtube.com/watch?v=otPFUIPQkIs" target="_blank" class="track-play">▶</a>
        </div>
        
        <div class="track-item">
          <span class="track-rank">06</span>
          <div class="track-info">
            <span class="track-name">LA DIFERENCIA ES LO QUE VALE</span>
            <span class="track-meta">Proyecto excepcional y único</span>
          </div>
          <a href="https://www.youtube.com/watch?v=J-li4emQsS0" target="_blank" class="track-play">▶</a>
        </div>
      </div>
    </div>
  </div>
  
  <style>
    .music-section {
      padding: 100px 20px;
      background: linear-gradient(135deg, #0f0f2e 0%, #1a1a3e 50%, #0a0e27 100%);
      color: #fff;
      position: relative;
    }
    
    .music-container {
      max-width: 1200px;
      margin: 0 auto;
    }
    
    .section-subtitle {
      font-size: 16px;
      color: #888;
      margin-top: 20px;
      max-width: 500px;
      margin-left: auto;
      margin-right: auto;
    }
    
    .music-content {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 50px;
      margin-top: 50px;
    }
    
    .spotify-embed {
      background: linear-gradient(135deg, #1a1a1a, #2d2d2d);
      border-radius: 20px;
      padding: 25px;
      border: 2px solid #1DB954;
      box-shadow: 0 20px 50px rgba(29, 185, 84, 0.2);
    }
    
    .spotify-header {
      display: flex;
      align-items: center;
      gap: 10px;
      margin-bottom: 20px;
    }
    
    .spotify-icon {
      font-size: 24px;
    }
    
    .spotify-title {
      font-size: 14px;
      font-weight: 800;
      color: #1DB954;
      letter-spacing: 2px;
      text-transform: uppercase;
    }
    
    .spotify-link {
      display: block;
      text-align: center;
      margin-top: 15px;
      color: #1DB954;
      text-decoration: none;
      font-weight: 700;
      font-size: 14px;
      transition: all 0.3s ease;
    }
    
    .spotify-link:hover {
      color: #fff;
    }
    
    .tracks-list {
      display: flex;
      flex-direction: column;
      gap: 15px;
    }
    
    .tracks-title {
      font-size: 20px;
      font-weight: 900;
      color: #ffbe0b;
      margin-bottom: 10px;
      text-transform: uppercase;
      letter-spacing: 1px;
    }
    
    .track-item {
      display: flex;
      align-items: center;
      gap: 15px;
      padding: 18px 20px;
      background: rgba(255, 255, 255, 0.03);
      border-radius: 12px;
      border: 1px solid #333;
      transition: all 0.3s ease;
    }
    
    .track-item:hover {
      background: rgba(255, 0, 110, 0.1);
      border-color: #ff006e;
      transform: translateX(10px);
    }
    
    .track-item.featured {
      background: linear-gradient(135deg, rgba(255, 0, 110, 0.15), rgba(131, 56, 236, 0.15));
      border-color: #ff006e;
    }
    
    .track-rank {
      font-size: 18px;
      font-weight: 900;
      color: #444;
      width: 30px;
      text-align: center;
    }
    
    .track-item.featured .track-rank,
    .track-item:hover .track-rank {
      color: #ff006e;
    }
    
    .track-info {
      flex-grow: 1;
    }
    
    .track-name {
      display: block;
      font-size: 14px;
      font-weight: 700;
      color: #fff;
      margin-bottom: 4px;
    }
    
    .track-meta {
      display: block;
      font-size: 12px;
      color: #888;
    }
    
    .track-badge {
      background: linear-gradient(135deg, #ff006e, #fb5607);
      color: white;
      font-size: 10px;
      font-weight: 800;
      padding: 4px 10px;
      border-radius: 15px;
      letter-spacing: 1px;
    }
    
    .track-play {
      width: 40px;
      height: 40px;
      display: flex;
      align-items: center;
      justify-content: center;
      background: linear-gradient(135deg, #ff006e, #8338ec);
      color: white;
      border-radius: 50%;
      text-decoration: none;
      font-size: 14px;
      transition: all 0.3s ease;
      flex-shrink: 0;
    }
    
    .track-play:hover {
      transform: scale(1.1);
      box-shadow: 0 8px 25px rgba(255, 0, 110, 0.5);
    }
    
    @media (max-width: 900px) {
      .music-content {
        grid-template-columns: 1fr;
        gap: 40px;
      }
    }
  </style>
</div>

<!-- Video Embeds Section -->
<div class="video-section" id="videos">
  <div class="video-container">
    <div class="section-header">
      <span class="section-tag">Contenido Visual</span>
      <h2>🎬 VIDEOS MUSICALES</h2>
      <div class="header-line"></div>
      <p class="section-subtitle">Videos oficiales, visualizers y contenido exclusivo</p>
    </div>
    
    <div class="video-grid">
      <div class="video-card featured-video">
        <div class="video-label">⭐ DESTACADO</div>
        <div class="video-wrapper">
          <iframe width="100%" height="315" src="https://www.youtube.com/embed/cB5sIhH067A" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
        </div>
        <div class="video-info">
          <h3>PROYECTO MÁS RECIENTE</h3>
          <p>Mi trabajo más fresco y actual - El proyecto que define mi evolución artística</p>
          <div class="video-tags">
            <span class="v-tag">Nuevo</span>
            <span class="v-tag">2024</span>
          </div>
        </div>
      </div>
      
      <div class="video-card">
        <div class="video-wrapper">
          <iframe width="100%" height="315" src="https://www.youtube.com/embed/uDAziScqsUk" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
        </div>
        <div class="video-info">
          <h3>VIDEO MÁS CRANEADO</h3>
          <p>El video que más cerebro me voló hacer</p>
          <div class="video-tags">
            <span class="v-tag">Creativo</span>
          </div>
        </div>
      </div>
      
      <div class="video-card">
        <div class="video-wrapper">
          <iframe width="100%" height="315" src="https://www.youtube.com/embed/zAjGlkn3udw" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
        </div>
        <div class="video-info">
          <h3>ENERGÍA MÍSTICA UNIVERSAL</h3>
          <p>Proyecto con vibras cósmicas y espirituales</p>
          <div class="video-tags">
            <span class="v-tag">Místico</span>
          </div>
        </div>
      </div>
    </div>
    
    <div class="video-cta">
      <a href="https://www.youtube.com/@susinirgs" target="_blank" class="btn-video">
        <span class="btn-icon">▶️</span> Ver Todos en YouTube
      </a>
    </div>
  </div>
  
  <style>
    .video-section {
      padding: 100px 20px;
      background: linear-gradient(135deg, #1a1a3e 0%, #0f0f2e 100%);
      color: #fff;
      position: relative;
    }
    
    .video-container {
      max-width: 1300px;
      margin: 0 auto;
    }
    
    .video-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(380px, 1fr));
      gap: 35px;
      margin-top: 50px;
    }
    
    .video-card {
      background: linear-gradient(135deg, #1a1a1a, #2d2d2d);
      border: 2px solid #333;
      border-radius: 16px;
      overflow: hidden;
      transition: all 0.4s cubic-bezier(0.25, 0.8, 0.25, 1);
      position: relative;
    }
    
    .video-card:hover {
      transform: translateY(-12px);
      border-color: #ff006e;
      box-shadow: 0 25px 60px rgba(255, 0, 110, 0.3);
    }
    
    .video-card.featured-video {
      grid-column: span 2;
      border-color: #ffbe0b;
    }
    
    .video-card.featured-video .video-wrapper {
      padding-bottom: 45%;
    }
    
    .video-label {
      position: absolute;
      top: 15px;
      left: 15px;
      background: linear-gradient(135deg, #ffbe0b, #fb5607);
      color: #000;
      padding: 6px 15px;
      border-radius: 20px;
      font-size: 11px;
      font-weight: 800;
      z-index: 10;
      letter-spacing: 1px;
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
      font-size: 18px;
      margin: 0 0 10px 0;
      color: #fff;
      text-transform: uppercase;
      font-weight: 800;
      letter-spacing: 1px;
    }
    
    .video-card p {
      font-size: 14px;
      color: #aaa;
      margin: 0 0 15px 0;
      line-height: 1.5;
    }
    
    .video-tags {
      display: flex;
      gap: 8px;
    }
    
    .v-tag {
      background: rgba(255, 0, 110, 0.2);
      color: #ff006e;
      padding: 4px 12px;
      border-radius: 15px;
      font-size: 11px;
      font-weight: 700;
      text-transform: uppercase;
      letter-spacing: 0.5px;
    }
    
    .video-cta {
      text-align: center;
      margin-top: 50px;
    }
    
    .btn-video {
      display: inline-flex;
      align-items: center;
      gap: 10px;
      padding: 18px 40px;
      background: linear-gradient(135deg, #ff0000, #cc0000);
      color: white;
      text-decoration: none;
      border-radius: 50px;
      font-weight: 700;
      font-size: 14px;
      text-transform: uppercase;
      letter-spacing: 1px;
      transition: all 0.3s ease;
      box-shadow: 0 10px 30px rgba(255, 0, 0, 0.3);
    }
    
    .btn-video:hover {
      transform: translateY(-5px);
      box-shadow: 0 15px 45px rgba(255, 0, 0, 0.5);
    }
    
    @media (max-width: 900px) {
      .video-card.featured-video {
        grid-column: span 1;
      }
      
      .video-card.featured-video .video-wrapper {
        padding-bottom: 56.25%;
      }
      
      .video-grid {
        grid-template-columns: 1fr;
      }
    }
  </style>
</div>

<!-- Gallery Section -->
<div class="gallery-section" id="gallery">
  <div class="gallery-container">
    <div class="section-header">
      <span class="section-tag">Visual</span>
      <h2>🎨 GALERÍA VISUAL</h2>
      <div class="header-line"></div>
      <p class="section-subtitle">Arte, estética y visuales que definen mi universo creativo</p>
    </div>
    
    <div class="gallery-grid">
      <div class="gallery-item large"><img src="CRANEO/SPOOKY (1) (1).png" alt="Spooky Art" loading="lazy"><div class="gallery-overlay"><span class="gallery-title">SPOOKY VIBES</span></div></div>
      <div class="gallery-item"><img src="CRANEO/@720pts.jpeg" alt="720pts" loading="lazy"><div class="gallery-overlay"><span class="gallery-title">720PTS</span></div></div>
      <div class="gallery-item"><img src="CRANEO/GcM5IGVXMAAPiLF.jpeg" alt="Visual Art" loading="lazy"><div class="gallery-overlay"><span class="gallery-title">ARTE VISUAL</span></div></div>
      <div class="gallery-item tall"><img src="CRANEO/_Freedom starts from within__.jpeg" alt="Freedom" loading="lazy"><div class="gallery-overlay"><span class="gallery-title">LIBERTAD</span></div></div>
      <div class="gallery-item"><img src="CRANEO/download - 2025-12-09T124825.697.jpg" alt="Art 1" loading="lazy"><div class="gallery-overlay"><span class="gallery-title">ARTE I</span></div></div>
      <div class="gallery-item"><img src="CRANEO/download - 2025-12-09T125039.980.jpg" alt="Art 2" loading="lazy"><div class="gallery-overlay"><span class="gallery-title">ARTE II</span></div></div>
      <div class="gallery-item large"><img src="CRANEO/download - 2025-12-09T125120.584.jpg" alt="Art 3" loading="lazy"><div class="gallery-overlay"><span class="gallery-title">ARTE III</span></div></div>
      <div class="gallery-item"><img src="CRANEO/download - 2025-12-09T125323.452.jpg" alt="Art 4" loading="lazy"><div class="gallery-overlay"><span class="gallery-title">ARTE IV</span></div></div>
      <div class="gallery-item tall"><img src="CRANEO/silver-surfer-all-alone-in-the-space-wallpaper-with-ai-v0-68daljq9mide1.webp" alt="Silver Surfer" loading="lazy"><div class="gallery-overlay"><span class="gallery-title">COSMIC</span></div></div>
      <div class="gallery-item"><img src="CRANEO/god.jpg" alt="God" loading="lazy"><div class="gallery-overlay"><span class="gallery-title">DIVINO</span></div></div>
      <div class="gallery-item"><img src="CRANEO/pollloooo.jpeg" alt="Pollo" loading="lazy"><div class="gallery-overlay"><span class="gallery-title">EXPRESIÓN</span></div></div>
      <div class="gallery-item"><img src="CRANEO/🂡 ʳˡʸᶜʳᵘˢʰ.jpeg" alt="Crush" loading="lazy"><div class="gallery-overlay"><span class="gallery-title">CRUSH</span></div></div>
    </div>
  </div>
  
  <style>
    .gallery-section {
      padding: 100px 20px;
      background: linear-gradient(135deg, #0a0e27 0%, #1a1a3e 50%, #0f0f2e 100%);
      color: #fff;
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
      margin-top: 50px;
    }
    
    .gallery-item {
      position: relative;
      overflow: hidden;
      border-radius: 12px;
      border: 2px solid #333;
      transition: all 0.5s cubic-bezier(0.25, 0.8, 0.25, 1);
      cursor: pointer;
    }
    
    .gallery-item.large {
      grid-column: span 2;
    }
    
    .gallery-item.tall {
      grid-row: span 2;
    }
    
    .gallery-item:hover {
      border-color: #ff006e;
      box-shadow: 0 25px 60px rgba(255, 0, 110, 0.4);
      z-index: 10;
      transform: scale(1.03);
    }
    
    .gallery-item img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      transition: all 0.5s ease;
    }
    
    .gallery-item:hover img {
      transform: scale(1.15);
      filter: brightness(0.7) saturate(1.3);
    }
    
    .gallery-overlay {
      position: absolute;
      bottom: 0;
      left: 0;
      right: 0;
      padding: 30px 20px 20px;
      background: linear-gradient(to top, rgba(0, 0, 0, 0.9) 0%, transparent 100%);
      opacity: 0;
      transform: translateY(20px);
      transition: all 0.4s ease;
    }
    
    .gallery-item:hover .gallery-overlay {
      opacity: 1;
      transform: translateY(0);
    }
    
    .gallery-title {
      font-size: 14px;
      font-weight: 800;
      color: #fff;
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
    }
  </style>
</div>

<!-- Stats/Achievements Section -->
<div class="stats-section" id="stats">
  <div class="stats-container">
    <div class="section-header">
      <span class="section-tag">Trayectoria</span>
      <h2>📊 MIS LOGROS</h2>
      <div class="header-line"></div>
    </div>
    
    <div class="stats-grid">
      <div class="stat-card">
        <div class="stat-icon">🎵</div>
        <div class="stat-value" data-value="15">15+</div>
        <div class="stat-name">Proyectos Lanzados</div>
        <div class="stat-desc">Tracks, videos y colaboraciones</div>
      </div>
      
      <div class="stat-card">
        <div class="stat-icon">🎬</div>
        <div class="stat-value">6+</div>
        <div class="stat-name">Videos Musicales</div>
        <div class="stat-desc">Contenido visual de alta calidad</div>
      </div>
      
      <div class="stat-card">
        <div class="stat-icon">🎧</div>
        <div class="stat-value">3</div>
        <div class="stat-name">Plataformas</div>
        <div class="stat-desc">Spotify, YouTube, Instagram</div>
      </div>
      
      <div class="stat-card">
        <div class="stat-icon">🌎</div>
        <div class="stat-value">24/7</div>
        <div class="stat-name">Creando</div>
        <div class="stat-desc">Siempre trabajando en nuevo material</div>
      </div>
    </div>
    
    <div class="timeline">
      <h3 class="timeline-title">🚀 EVOLUCIÓN ARTÍSTICA</h3>
      <div class="timeline-items">
        <div class="timeline-item">
          <div class="timeline-marker"></div>
          <div class="timeline-content">
            <span class="timeline-date">2024</span>
            <h4>Lanzamiento de Nuevos Proyectos</h4>
            <p>Expansión del universo sonoro con tracks que fusionan trap, hip-hop y elementos místicos.</p>
          </div>
        </div>
        <div class="timeline-item">
          <div class="timeline-marker"></div>
          <div class="timeline-content">
            <span class="timeline-date">Presente</span>
            <h4>Energía Mística Universal</h4>
            <p>Consolidación del estilo único, videos cinematográficos y presencia en plataformas digitales.</p>
          </div>
        </div>
        <div class="timeline-item">
          <div class="timeline-marker"></div>
          <div class="timeline-content">
            <span class="timeline-date">Futuro</span>
            <h4>Expansión Global</h4>
            <p>Nuevas colaboraciones, proyectos audiovisuales y crecimiento de la comunidad.</p>
          </div>
        </div>
      </div>
    </div>
  </div>
  
  <style>
    .stats-section {
      padding: 100px 20px;
      background: linear-gradient(135deg, #0f0f2e 0%, #0a0e27 100%);
      color: #fff;
      position: relative;
    }
    
    .stats-section::before {
      content: '';
      position: absolute;
      top: 0;
      left: 0;
      right: 0;
      height: 3px;
      background: linear-gradient(90deg, transparent, #8338ec, #ff006e, transparent);
    }
    
    .stats-container {
      max-width: 1200px;
      margin: 0 auto;
    }
    
    .stats-grid {
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      gap: 25px;
      margin: 50px 0;
    }
    
    .stat-card {
      background: linear-gradient(135deg, rgba(255, 255, 255, 0.03), rgba(255, 255, 255, 0.01));
      border: 1px solid #333;
      border-radius: 16px;
      padding: 35px 25px;
      text-align: center;
      transition: all 0.4s ease;
      position: relative;
      overflow: hidden;
    }
    
    .stat-card::before {
      content: '';
      position: absolute;
      top: 0;
      left: 0;
      right: 0;
      height: 3px;
      background: linear-gradient(90deg, #ff006e, #8338ec);
      transform: scaleX(0);
      transition: transform 0.4s ease;
    }
    
    .stat-card:hover::before {
      transform: scaleX(1);
    }
    
    .stat-card:hover {
      transform: translateY(-10px);
      border-color: #ff006e;
      box-shadow: 0 20px 50px rgba(255, 0, 110, 0.2);
    }
    
    .stat-icon {
      font-size: 40px;
      margin-bottom: 15px;
    }
    
    .stat-value {
      font-size: 48px;
      font-weight: 900;
      background: linear-gradient(90deg, #ff006e, #ffbe0b);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      background-clip: text;
      margin-bottom: 10px;
    }
    
    .stat-name {
      font-size: 16px;
      font-weight: 700;
      color: #fff;
      text-transform: uppercase;
      letter-spacing: 1px;
      margin-bottom: 8px;
    }
    
    .stat-desc {
      font-size: 12px;
      color: #888;
    }
    
    .timeline {
      margin-top: 60px;
      padding-top: 50px;
      border-top: 1px solid #333;
    }
    
    .timeline-title {
      text-align: center;
      font-size: 24px;
      font-weight: 900;
      color: #ffbe0b;
      margin-bottom: 40px;
      text-transform: uppercase;
      letter-spacing: 2px;
    }
    
    .timeline-items {
      display: flex;
      justify-content: space-between;
      position: relative;
      padding: 0 20px;
    }
    
    .timeline-items::before {
      content: '';
      position: absolute;
      top: 20px;
      left: 0;
      right: 0;
      height: 3px;
      background: linear-gradient(90deg, #ff006e, #8338ec, #ffbe0b);
    }
    
    .timeline-item {
      flex: 1;
      text-align: center;
      position: relative;
      padding: 0 15px;
    }
    
    .timeline-marker {
      width: 40px;
      height: 40px;
      background: linear-gradient(135deg, #ff006e, #8338ec);
      border-radius: 50%;
      margin: 0 auto 20px;
      position: relative;
      z-index: 1;
      box-shadow: 0 0 20px rgba(255, 0, 110, 0.5);
    }
    
    .timeline-content {
      background: rgba(255, 255, 255, 0.03);
      border-radius: 12px;
      padding: 25px;
      border: 1px solid #333;
    }
    
    .timeline-date {
      display: inline-block;
      background: linear-gradient(135deg, #ff006e, #8338ec);
      color: white;
      padding: 5px 15px;
      border-radius: 20px;
      font-size: 12px;
      font-weight: 700;
      margin-bottom: 15px;
    }
    
    .timeline-content h4 {
      font-size: 16px;
      font-weight: 800;
      color: #00f5ff;
      margin: 0 0 10px 0;
    }
    
    .timeline-content p {
      font-size: 13px;
      color: #aaa;
      margin: 0;
      line-height: 1.6;
    }
    
    @media (max-width: 900px) {
      .stats-grid {
        grid-template-columns: repeat(2, 1fr);
      }
      
      .timeline-items {
        flex-direction: column;
        gap: 30px;
      }
      
      .timeline-items::before {
        display: none;
      }
      
      .stat-value {
        font-size: 36px;
      }
    }
    
    @media (max-width: 600px) {
      .stats-grid {
        grid-template-columns: 1fr;
      }
    }
  </style>
</div>



<!-- Social Links Section -->
<div class="social-section" id="connect">
  <div class="social-container">
    <div class="section-header light">
      <span class="section-tag light">Comunidad</span>
      <h2>🔗 CONECTA CONMIGO</h2>
      <div class="header-line light"></div>
      <p class="section-subtitle light">Únete a la comunidad y mantente al día con nueva música y anuncios</p>
    </div>
    
    <div class="social-links">
      <a href="https://open.spotify.com/intl-es/artist/78uCfenEleQDaQJM21K2fk?si=7O3kEBUITZyZWnRXtJ8bhg" target="_blank" class="social-btn spotify" title="Spotify">
        <span class="social-icon">🎵</span>
        <span class="social-name">Spotify</span>
        <span class="social-action">Escuchar</span>
      </a>
      <a href="https://www.youtube.com/@susinirgs" target="_blank" class="social-btn youtube" title="YouTube">
        <span class="social-icon">▶️</span>
        <span class="social-name">YouTube</span>
        <span class="social-action">Suscribirse</span>
      </a>
      <a href="https://www.instagram.com/susinirgs/" target="_blank" class="social-btn instagram" title="Instagram">
        <span class="social-icon">📸</span>
        <span class="social-name">Instagram</span>
        <span class="social-action">Seguir</span>
      </a>
    </div>
    
    <div class="connect-cta">
      <div class="cta-content">
        <h3>¿Listo para sumergirte en el universo SUSINIRGS?</h3>
        <p>Escucha mi música, ve mis videos y únete a la comunidad de la Energía Mística Universal</p>
        <a href="#music" class="btn-cta">🎧 Empezar a Escuchar</a>
      </div>
    </div>
  </div>
  
  <style>
    .social-section {
      padding: 100px 20px;
      background: linear-gradient(135deg, #8338ec 0%, #ff006e 50%, #fb5607 100%);
      text-align: center;
      color: #fff;
      position: relative;
      overflow: hidden;
    }
    
    .social-section::before {
      content: '';
      position: absolute;
      top: 0;
      left: 0;
      right: 0;
      bottom: 0;
      background: 
        radial-gradient(circle at 20% 30%, rgba(255, 255, 255, 0.1) 0%, transparent 40%),
        radial-gradient(circle at 80% 70%, rgba(0, 0, 0, 0.1) 0%, transparent 40%);
      pointer-events: none;
    }
    
    .social-container {
      max-width: 1000px;
      margin: 0 auto;
      position: relative;
      z-index: 1;
    }
    
    .section-header.light .section-tag {
      background: rgba(255, 255, 255, 0.2);
      color: white;
      border-color: rgba(255, 255, 255, 0.4);
    }
    
    .section-header.light h2 {
      color: white !important;
      -webkit-text-fill-color: white;
      background: none;
      text-shadow: 2px 2px 10px rgba(0, 0, 0, 0.3);
    }
    
    .header-line.light {
      background: rgba(255, 255, 255, 0.5);
    }
    
    .section-subtitle.light {
      color: rgba(255, 255, 255, 0.9);
    }
    
    .social-links {
      display: flex;
      gap: 25px;
      justify-content: center;
      flex-wrap: wrap;
      margin: 50px auto;
    }
    
    .social-btn {
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      gap: 8px;
      width: 140px;
      height: 140px;
      background: rgba(255, 255, 255, 0.1);
      border: 2px solid rgba(255, 255, 255, 0.3);
      border-radius: 20px;
      text-decoration: none;
      color: #fff;
      transition: all 0.4s cubic-bezier(0.25, 0.8, 0.25, 1);
      backdrop-filter: blur(10px);
    }
    
    .social-icon {
      font-size: 40px;
      display: block;
      margin-bottom: 5px;
    }
    
    .social-name {
      font-size: 14px;
      font-weight: 800;
      text-transform: uppercase;
      letter-spacing: 1px;
    }
    
    .social-action {
      font-size: 11px;
      color: rgba(255, 255, 255, 0.7);
      text-transform: uppercase;
      letter-spacing: 1px;
    }
    
    .social-btn:hover {
      background: rgba(255, 255, 255, 0.25);
      border-color: rgba(255, 255, 255, 0.8);
      transform: translateY(-10px) scale(1.05);
      box-shadow: 0 20px 40px rgba(0, 0, 0, 0.3);
    }
    
    .social-btn.spotify:hover {
      background: rgba(29, 185, 84, 0.4);
      border-color: #1DB954;
    }
    
    .social-btn.youtube:hover {
      background: rgba(255, 0, 0, 0.4);
      border-color: #FF0000;
    }
    
    .social-btn.instagram:hover {
      background: rgba(228, 64, 95, 0.4);
      border-color: #E4405F;
    }
    
    .connect-cta {
      margin-top: 50px;
      padding-top: 50px;
      border-top: 1px solid rgba(255, 255, 255, 0.2);
    }
    
    .cta-content h3 {
      font-size: 26px;
      font-weight: 800;
      margin: 0 0 15px 0;
      text-shadow: 2px 2px 10px rgba(0, 0, 0, 0.3);
    }
    
    .cta-content p {
      font-size: 16px;
      color: rgba(255, 255, 255, 0.85);
      margin: 0 0 30px 0;
      max-width: 500px;
      margin-left: auto;
      margin-right: auto;
    }
    
    .btn-cta {
      display: inline-flex;
      align-items: center;
      gap: 10px;
      padding: 18px 40px;
      background: white;
      color: #ff006e;
      text-decoration: none;
      border-radius: 50px;
      font-weight: 800;
      font-size: 15px;
      text-transform: uppercase;
      letter-spacing: 1px;
      transition: all 0.3s ease;
      box-shadow: 0 10px 30px rgba(0, 0, 0, 0.2);
    }
    
    .btn-cta:hover {
      transform: translateY(-5px) scale(1.05);
      box-shadow: 0 20px 50px rgba(0, 0, 0, 0.3);
      background: #ffbe0b;
      color: #1a1a1a;
    }
    
    @media (max-width: 600px) {
      .social-btn {
        width: 110px;
        height: 110px;
      }
      
      .social-icon {
        font-size: 32px;
      }
      
      .cta-content h3 {
        font-size: 22px;
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
        <p class="footer-tagline">🔥 TRAP • HIP-HOP • BEATS 🔥</p>
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
      <div class="footer-line-gradient"></div>
      <p class="footer-copy">&copy; 2025 SUSINIRGS. Todos los derechos reservados.</p>
      <p class="footer-credit">🎵 Hecho con pasión por la cultura | Energía Mística Universal 🎵</p>
    </div>
  </div>
  
  <style>
    .footer {
      background: linear-gradient(180deg, #0a0e27 0%, #050810 100%);
      color: #888;
      padding: 80px 20px 40px;
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
      background: linear-gradient(90deg, #ff006e, #ffbe0b, #8338ec, #00f5ff, #ff006e);
      background-size: 200% 100%;
      animation: gradientMove 5s linear infinite;
    }
    
    @keyframes gradientMove {
      0% { background-position: 0% 0%; }
      100% { background-position: 200% 0%; }
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
    
    .footer-brand {
      text-align: left;
    }
    
    .footer-logo {
      font-size: 36px;
      font-weight: 900;
      margin: 0 0 10px 0;
      background: linear-gradient(90deg, #ff006e, #ffbe0b);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      background-clip: text;
      letter-spacing: 3px;
    }
    
    .footer-tagline {
      color: #ffbe0b;
      font-weight: 700;
      font-size: 14px;
      margin: 0 0 15px 0;
    }
    
    .footer-desc {
      color: #777;
      font-size: 14px;
      line-height: 1.7;
      margin: 0;
      max-width: 300px;
    }
    
    .footer-nav h4,
    .footer-social h4 {
      font-size: 14px;
      font-weight: 800;
      color: #fff;
      text-transform: uppercase;
      letter-spacing: 2px;
      margin: 0 0 20px 0;
    }
    
    .footer-nav a,
    .footer-social a {
      display: block;
      color: #888;
      text-decoration: none;
      font-size: 14px;
      margin-bottom: 12px;
      transition: all 0.3s ease;
    }
    
    .footer-nav a:hover,
    .footer-social a:hover {
      color: #ff006e;
      transform: translateX(5px);
    }
    
    .footer-bottom {
      text-align: center;
      padding-top: 30px;
    }
    
    .footer-line-gradient {
      height: 1px;
      background: linear-gradient(90deg, transparent, #333, transparent);
      margin-bottom: 30px;
    }
    
    .footer-copy {
      color: #aaa;
      font-size: 13px;
      margin: 0 0 10px 0;
    }
    
    .footer-credit {
      color: #666;
      font-size: 12px;
      font-style: italic;
      margin: 0;
    }
    
    @media (max-width: 768px) {
      .footer-top {
        grid-template-columns: 1fr;
        gap: 30px;
        text-align: center;
      }
      
      .footer-brand {
        text-align: center;
      }
      
      .footer-desc {
        max-width: 100%;
      }
      
      .footer-nav a:hover,
      .footer-social a:hover {
        transform: none;
      }
    }
  </style>
</footer>
