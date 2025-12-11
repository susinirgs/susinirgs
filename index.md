---
layout: default
title: SUSINIRGS - Trap Artist & Producer
---

<!-- Hero Section -->
<div class="hero-section">
  <div class="hero-content">
    <div class="artist-logo">
      <h1 class="artist-name">SUSINIRGS</h1>
      <p class="artist-tagline">🔥 TRAP | HIP-HOP | BEATS 🔥</p>
    </div>
    <p class="hero-subtitle">Next Generation Trap & Hip-Hop Artist</p>
    <div class="hero-cta">
      <a href="#tracks" class="btn btn-primary">Listen Now</a>
      <a href="#projects" class="btn btn-secondary">Check Projects</a>
    </div>
  </div>
  <style>
    .hero-section {
      background: linear-gradient(135deg, #1a1a1a 0%, #2d2d2d 100%);
      color: #fff;
      padding: 80px 20px;
      text-align: center;
      border-bottom: 3px solid #ff006e;
      position: relative;
      overflow: hidden;
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
    }
    
    .hero-content {
      position: relative;
      z-index: 1;
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
  </style>
</div>

---

<!-- Tracks Section -->
<div class="tracks-section" id="tracks">
  <h2>🎵 HOTTEST TRACKS 🎵</h2>
  <div class="tracks-grid">
    <div class="track-card">
      <div class="track-number">01</div>
      <h3>TRAP DYNASTY</h3>
      <p class="track-info">Hard-hitting trap beat with aggressive hi-hats</p>
      <p class="track-stats">🔥 2.3M Listens</p>
      <a href="#" class="track-btn">▶ PLAY</a>
    </div>
    
    <div class="track-card">
      <div class="track-number">02</div>
      <h3>NEON NIGHTS</h3>
      <p class="track-info">Hypnotic synth-driven trap anthem</p>
      <p class="track-stats">🔥 1.8M Listens</p>
      <a href="#" class="track-btn">▶ PLAY</a>
    </div>
    
    <div class="track-card">
      <div class="track-number">03</div>
      <h3>CROWN</h3>
      <p class="track-info">Premium rap track for the top dogs</p>
      <p class="track-stats">🔥 1.5M Listens</p>
      <a href="#" class="track-btn">▶ PLAY</a>
    </div>
    
    <div class="track-card">
      <div class="track-number">04</div>
      <h3>NIGHT MODE</h3>
      <p class="track-info">Dark, moody trap production masterpiece</p>
      <p class="track-stats">🔥 1.2M Listens</p>
      <a href="#" class="track-btn">▶ PLAY</a>
    </div>
    
    <div class="track-card">
      <div class="track-number">05</div>
      <h3>GRIND NEVER STOPS</h3>
      <p class="track-info">Motivational hip-hop anthem for hustlers</p>
      <p class="track-stats">🔥 980K Listens</p>
      <a href="#" class="track-btn">▶ PLAY</a>
    </div>
    
    <div class="track-card">
      <div class="track-number">06</div>
      <h3>DIGITAL CRIME</h3>
      <p class="track-info">Cyberpunk trap vibes with heavy bass</p>
      <p class="track-stats">🔥 750K Listens</p>
      <a href="#" class="track-btn">▶ PLAY</a>
    </div>
  </div>
  
  <style>
    .tracks-section {
      padding: 80px 20px;
      background: #0f0f0f;
      color: #fff;
    }
    
    .tracks-section h2 {
      font-size: 48px;
      text-align: center;
      margin-bottom: 60px;
      color: #ffbe0b;
      text-transform: uppercase;
      letter-spacing: 2px;
      font-weight: 900;
    }
    
    .tracks-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
      gap: 30px;
      max-width: 1200px;
      margin: 0 auto;
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

<!-- Featured Projects Section -->
<div class="projects-section" id="projects">
  <h2>🚀 FEATURED PROJECTS 🚀</h2>
  <div class="projects-grid">
    <div class="project-card">
      <div class="project-icon">🎬</div>
      <h3>TRAP BEATS VOL. 1</h3>
      <p>Exclusive collection of 50 hard-hitting trap instrumentals. Perfect for producers and creators worldwide.</p>
      <div class="project-meta">
        <span class="tag">Production</span>
        <span class="tag">Beats</span>
      </div>
      <a href="#" class="project-link">Explore →</a>
    </div>
    
    <div class="project-card">
      <div class="project-icon">🎙️</div>
      <h3>STREET POETRY EP</h3>
      <p>Raw and authentic hip-hop narratives capturing the essence of modern struggle and triumph. 8 tracks of pure lyricism.</p>
      <div class="project-meta">
        <span class="tag">Hip-Hop</span>
        <span class="tag">Lyricism</span>
      </div>
      <a href="#" class="project-link">Explore →</a>
    </div>
    
    <div class="project-card">
      <div class="project-icon">🎛️</div>
      <h3>REMIX PACKAGE</h3>
      <p>Creative remixes of top tracks with experimental production techniques. Pushing boundaries of trap music.</p>
      <div class="project-meta">
        <span class="tag">Remix</span>
        <span class="tag">Experimental</span>
      </div>
      <a href="#" class="project-link">Explore →</a>
    </div>
    
    <div class="project-card">
      <div class="project-icon">🔊</div>
      <h3>SOUND DESIGN MASTERCLASS</h3>
      <p>Educational content teaching the fundamentals of modern trap production and sound design principles.</p>
      <div class="project-meta">
        <span class="tag">Education</span>
        <span class="tag">Production</span>
      </div>
      <a href="#" class="project-link">Explore →</a>
    </div>
    
    <div class="project-card">
      <div class="project-icon">🌐</div>
      <h3>COLLAB WITH TOP ARTISTS</h3>
      <p>Exclusive collaborations featuring featured artists and producers from around the globe. Next-level authenticity.</p>
      <div class="project-meta">
        <span class="tag">Collaboration</span>
        <span class="tag">Featured</span>
      </div>
      <a href="#" class="project-link">Explore →</a>
    </div>
    
    <div class="project-card">
      <div class="project-icon">💿</div>
      <h3>MIXTAPE 2025</h3>
      <p>The ultimate trap compilation for 2025. Featuring the freshest beats, hottest tracks, and emerging talent.</p>
      <div class="project-meta">
        <span class="tag">Mixtape</span>
        <span class="tag">2025</span>
      </div>
      <a href="#" class="project-link">Explore →</a>
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
<div class="social-section">
  <h2>🔗 CONNECT WITH ME 🔗</h2>
  <p class="social-subtitle">Join the community and stay updated with fresh beats & announcements</p>
  
  <div class="social-links">
    <a href="https://spotify.com" class="social-btn spotify" title="Spotify">
      <span class="icon">🎵</span>
      <span class="label">Spotify</span>
    </a>
    <a href="https://soundcloud.com" class="social-btn soundcloud" title="SoundCloud">
      <span class="icon">☁️</span>
      <span class="label">SoundCloud</span>
    </a>
    <a href="https://youtube.com" class="social-btn youtube" title="YouTube">
      <span class="icon">▶️</span>
      <span class="label">YouTube</span>
    </a>
    <a href="https://twitter.com" class="social-btn twitter" title="Twitter/X">
      <span class="icon">𝕏</span>
      <span class="label">Twitter</span>
    </a>
    <a href="https://instagram.com" class="social-btn instagram" title="Instagram">
      <span class="icon">📸</span>
      <span class="label">Instagram</span>
    </a>
    <a href="https://discord.com" class="social-btn discord" title="Discord">
      <span class="icon">💬</span>
      <span class="label">Discord</span>
    </a>
    <a href="https://tiktok.com" class="social-btn tiktok" title="TikTok">
      <span class="icon">🎭</span>
      <span class="label">TikTok</span>
    </a>
    <a href="mailto:contact@susinirgs.com" class="social-btn email" title="Email">
      <span class="icon">✉️</span>
      <span class="label">Email</span>
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
  <p>&copy; 2025 SUSINIRGS. All Rights Reserved. | Trap Artist & Producer</p>
  <p style="color: #888; font-size: 12px;">🎵 Made with passion for the culture 🎵</p>
  <style>
    .footer {
      background: #0f0f0f;
      color: #888;
      text-align: center;
      padding: 30px 20px;
      border-top: 2px solid #ff006e;
      font-size: 14px;
    }
    
    .footer p {
      margin: 5px 0;
    }
  </style>
</footer>
