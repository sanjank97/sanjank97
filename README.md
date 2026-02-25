<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Sanjan Kumar – GitHub Profile Preview</title>
<link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@400;700;900&family=Share+Tech+Mono&family=Rajdhani:wght@300;400;600&display=swap" rel="stylesheet">
<style>
  :root {
    --cyan: #00f5ff;
    --green: #39ff14;
    --purple: #bf00ff;
    --dark: #030712;
    --card: #0a0f1e;
    --border: rgba(0,245,255,0.2);
    --glow: 0 0 20px rgba(0,245,255,0.4);
  }

  * { margin: 0; padding: 0; box-sizing: border-box; }

  body {
    background: var(--dark);
    color: #e0e8f0;
    font-family: 'Rajdhani', sans-serif;
    font-size: 16px;
    line-height: 1.6;
    min-height: 100vh;
    overflow-x: hidden;
  }

  /* Grid background */
  body::before {
    content: '';
    position: fixed;
    inset: 0;
    background-image:
      linear-gradient(rgba(0,245,255,0.03) 1px, transparent 1px),
      linear-gradient(90deg, rgba(0,245,255,0.03) 1px, transparent 1px);
    background-size: 40px 40px;
    pointer-events: none;
    z-index: 0;
  }

  .container {
    max-width: 860px;
    margin: 0 auto;
    padding: 40px 24px;
    position: relative;
    z-index: 1;
  }

  /* ── HERO ── */
  .hero {
    text-align: center;
    padding: 60px 0 48px;
    position: relative;
  }

  .hero::before {
    content: '';
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    width: 500px;
    height: 300px;
    background: radial-gradient(ellipse, rgba(0,245,255,0.07) 0%, transparent 70%);
    pointer-events: none;
  }

  .greeting {
    font-family: 'Share Tech Mono', monospace;
    color: var(--cyan);
    font-size: 13px;
    letter-spacing: 4px;
    text-transform: uppercase;
    opacity: 0;
    animation: fadeUp 0.6s ease 0.1s forwards;
  }

  .hero h1 {
    font-family: 'Orbitron', monospace;
    font-size: clamp(28px, 5vw, 48px);
    font-weight: 900;
    color: #fff;
    letter-spacing: 2px;
    margin: 12px 0 8px;
    opacity: 0;
    animation: fadeUp 0.6s ease 0.25s forwards;
    text-shadow: 0 0 40px rgba(0,245,255,0.3);
  }

  .hero h1 span {
    color: var(--cyan);
  }

  .subtitle {
    font-family: 'Share Tech Mono', monospace;
    color: rgba(224,232,240,0.6);
    font-size: 13px;
    letter-spacing: 2px;
    opacity: 0;
    animation: fadeUp 0.6s ease 0.4s forwards;
  }

  .subtitle em {
    color: var(--green);
    font-style: normal;
  }

  .divider {
    height: 1px;
    background: linear-gradient(90deg, transparent, var(--cyan), var(--purple), transparent);
    margin: 40px 0;
    opacity: 0;
    animation: fadeIn 0.8s ease 0.6s forwards;
  }

  /* ── STATS ROW ── */
  .stats {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 16px;
    margin-bottom: 40px;
    opacity: 0;
    animation: fadeUp 0.6s ease 0.7s forwards;
  }

  .stat-card {
    border: 1px solid var(--border);
    background: var(--card);
    border-radius: 8px;
    padding: 20px 16px;
    text-align: center;
    position: relative;
    overflow: hidden;
    transition: border-color 0.3s, box-shadow 0.3s;
  }

  .stat-card::before {
    content: '';
    position: absolute;
    top: 0; left: 0; right: 0;
    height: 2px;
    background: linear-gradient(90deg, var(--cyan), var(--purple));
  }

  .stat-card:hover {
    border-color: var(--cyan);
    box-shadow: var(--glow);
  }

  .stat-num {
    font-family: 'Orbitron', monospace;
    font-size: 32px;
    font-weight: 700;
    color: var(--cyan);
    display: block;
  }

  .stat-label {
    font-size: 11px;
    letter-spacing: 2px;
    text-transform: uppercase;
    color: rgba(224,232,240,0.5);
    margin-top: 4px;
  }

  /* ── SECTION ── */
  .section {
    margin-bottom: 40px;
    opacity: 0;
    animation: fadeUp 0.6s ease forwards;
  }

  .section:nth-child(1) { animation-delay: 0.8s; }
  .section:nth-child(2) { animation-delay: 0.95s; }
  .section:nth-child(3) { animation-delay: 1.1s; }
  .section:nth-child(4) { animation-delay: 1.25s; }

  .section-header {
    display: flex;
    align-items: center;
    gap: 12px;
    margin-bottom: 20px;
  }

  .section-header h2 {
    font-family: 'Orbitron', monospace;
    font-size: 13px;
    font-weight: 700;
    letter-spacing: 3px;
    text-transform: uppercase;
    color: var(--cyan);
  }

  .section-header .line {
    flex: 1;
    height: 1px;
    background: var(--border);
  }

  .section-header .icon {
    font-size: 16px;
  }

  /* ── ABOUT ── */
  .about-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 12px;
  }

  .about-item {
    display: flex;
    align-items: flex-start;
    gap: 10px;
    background: var(--card);
    border: 1px solid var(--border);
    border-radius: 6px;
    padding: 12px 14px;
    font-size: 14px;
    color: rgba(224,232,240,0.8);
    transition: border-color 0.2s;
  }

  .about-item:hover { border-color: rgba(0,245,255,0.5); }

  .about-item .dot {
    width: 6px;
    height: 6px;
    border-radius: 50%;
    background: var(--cyan);
    flex-shrink: 0;
    margin-top: 6px;
    box-shadow: 0 0 8px var(--cyan);
  }

  /* ── TECH STACK ── */
  .tech-group {
    margin-bottom: 16px;
  }

  .tech-group-label {
    font-family: 'Share Tech Mono', monospace;
    font-size: 11px;
    letter-spacing: 3px;
    color: var(--purple);
    text-transform: uppercase;
    margin-bottom: 10px;
  }

  .tech-pills {
    display: flex;
    flex-wrap: wrap;
    gap: 8px;
  }

  .pill {
    font-family: 'Share Tech Mono', monospace;
    font-size: 12px;
    padding: 5px 14px;
    border-radius: 3px;
    border: 1px solid var(--border);
    background: rgba(0,245,255,0.04);
    color: rgba(224,232,240,0.85);
    letter-spacing: 1px;
    transition: all 0.2s;
    cursor: default;
  }

  .pill:hover {
    border-color: var(--cyan);
    color: var(--cyan);
    background: rgba(0,245,255,0.08);
    box-shadow: 0 0 12px rgba(0,245,255,0.2);
  }

  .pill.green { border-color: rgba(57,255,20,0.25); }
  .pill.green:hover { border-color: var(--green); color: var(--green); box-shadow: 0 0 12px rgba(57,255,20,0.2); }
  .pill.purple { border-color: rgba(191,0,255,0.25); }
  .pill.purple:hover { border-color: var(--purple); color: var(--purple); box-shadow: 0 0 12px rgba(191,0,255,0.2); }

  /* ── FEATURED WORK ── */
  .work-grid {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 12px;
  }

  .work-card {
    border: 1px solid var(--border);
    background: var(--card);
    border-radius: 8px;
    padding: 16px 18px;
    position: relative;
    overflow: hidden;
    transition: all 0.3s;
  }

  .work-card:hover {
    border-color: var(--green);
    box-shadow: 0 0 20px rgba(57,255,20,0.1);
    transform: translateY(-2px);
  }

  .work-card::after {
    content: '';
    position: absolute;
    bottom: 0; left: 0; right: 0;
    height: 1px;
    background: linear-gradient(90deg, var(--cyan), var(--green));
    opacity: 0;
    transition: opacity 0.3s;
  }

  .work-card:hover::after { opacity: 1; }

  .work-icon {
    font-size: 20px;
    margin-bottom: 8px;
  }

  .work-title {
    font-family: 'Orbitron', monospace;
    font-size: 11px;
    font-weight: 700;
    letter-spacing: 1px;
    color: #fff;
  }

  .work-desc {
    font-size: 12px;
    color: rgba(224,232,240,0.5);
    margin-top: 4px;
  }

  /* ── FOCUS ── */
  .focus-list {
    display: flex;
    flex-direction: column;
    gap: 10px;
  }

  .focus-item {
    display: flex;
    align-items: center;
    gap: 16px;
    padding: 14px 18px;
    border: 1px solid var(--border);
    border-left: 2px solid var(--cyan);
    background: var(--card);
    border-radius: 0 6px 6px 0;
    font-size: 14px;
    transition: background 0.2s;
  }

  .focus-item:hover { background: rgba(0,245,255,0.05); }

  .focus-item .tag {
    font-family: 'Share Tech Mono', monospace;
    font-size: 10px;
    letter-spacing: 2px;
    color: var(--cyan);
    min-width: 70px;
  }

  /* ── CTA ── */
  .cta {
    text-align: center;
    padding: 48px 0 32px;
    opacity: 0;
    animation: fadeUp 0.6s ease 1.4s forwards;
  }

  .cta-text {
    font-family: 'Share Tech Mono', monospace;
    color: rgba(224,232,240,0.5);
    font-size: 12px;
    letter-spacing: 3px;
    margin-bottom: 20px;
  }

  .cta-btn {
    display: inline-block;
    font-family: 'Orbitron', monospace;
    font-size: 12px;
    font-weight: 700;
    letter-spacing: 3px;
    text-transform: uppercase;
    padding: 14px 36px;
    border: 1px solid var(--cyan);
    color: var(--cyan);
    text-decoration: none;
    border-radius: 3px;
    position: relative;
    overflow: hidden;
    transition: all 0.3s;
  }

  .cta-btn::before {
    content: '';
    position: absolute;
    inset: 0;
    background: var(--cyan);
    transform: scaleX(0);
    transform-origin: left;
    transition: transform 0.3s;
  }

  .cta-btn:hover {
    color: var(--dark);
    box-shadow: var(--glow);
  }

  .cta-btn:hover::before { transform: scaleX(1); }

  .cta-btn span { position: relative; z-index: 1; }

  /* ── FOOTER ── */
  .footer {
    text-align: center;
    padding: 24px 0;
    border-top: 1px solid var(--border);
    font-family: 'Share Tech Mono', monospace;
    font-size: 11px;
    color: rgba(224,232,240,0.2);
    letter-spacing: 2px;
  }

  /* ── SCAN LINE ── */
  @keyframes scanline {
    0% { top: -2px; }
    100% { top: 100%; }
  }

  .scanline {
    position: fixed;
    left: 0; right: 0;
    height: 2px;
    background: linear-gradient(90deg, transparent, rgba(0,245,255,0.15), transparent);
    animation: scanline 6s linear infinite;
    pointer-events: none;
    z-index: 9999;
  }

  @keyframes fadeUp {
    from { opacity: 0; transform: translateY(20px); }
    to { opacity: 1; transform: translateY(0); }
  }

  @keyframes fadeIn {
    from { opacity: 0; }
    to { opacity: 1; }
  }

  /* ── BLINK CURSOR ── */
  @keyframes blink {
    0%, 100% { opacity: 1; }
    50% { opacity: 0; }
  }

  .cursor {
    display: inline-block;
    width: 2px;
    height: 1em;
    background: var(--cyan);
    margin-left: 4px;
    vertical-align: middle;
    animation: blink 1s step-end infinite;
  }

  @media (max-width: 600px) {
    .stats { grid-template-columns: repeat(3, 1fr); }
    .about-grid { grid-template-columns: 1fr; }
    .work-grid { grid-template-columns: 1fr; }
    .hero h1 { font-size: 24px; }
  }
</style>
</head>
<body>

<div class="scanline"></div>

<div class="container">

  <!-- HERO -->
  <div class="hero">
    <div class="greeting">// initializing profile.exe</div>
    <h1>SANJAN <span>KUMAR</span></h1>
    <div class="subtitle">Senior Full Stack Developer &nbsp;|&nbsp; <em>PHP • WordPress • Laravel • MERN</em></div>
  </div>

  <div class="divider"></div>

  <!-- STATS -->
  <div class="stats">
    <div class="stat-card">
      <span class="stat-num">5+</span>
      <div class="stat-label">Years Active</div>
    </div>
    <div class="stat-card">
      <span class="stat-num">∞</span>
      <div class="stat-label">Lines Shipped</div>
    </div>
    <div class="stat-card">
      <span class="stat-num">01</span>
      <div class="stat-label">Mission: Scale</div>
    </div>
  </div>

  <!-- ABOUT -->
  <div class="section">
    <div class="section-header">
      <span class="icon">⚡</span>
      <h2>About</h2>
      <div class="line"></div>
    </div>
    <div class="about-grid">
      <div class="about-item"><div class="dot"></div>Expert in PHP & WordPress Custom Plugin Dev</div>
      <div class="about-item"><div class="dot"></div>Strong Laravel Application Architecture</div>
      <div class="about-item"><div class="dot"></div>MERN Stack Developer (MongoDB, Express, React, Node)</div>
      <div class="about-item"><div class="dot"></div>REST API Development & Integration Specialist</div>
      <div class="about-item"><div class="dot"></div>CRM, Booking Systems & Automation Tools</div>
      <div class="about-item"><div class="dot"></div>Performance, Scalability & Clean Architecture</div>
    </div>
  </div>

  <!-- TECH STACK -->
  <div class="section">
    <div class="section-header">
      <span class="icon">🛠</span>
      <h2>Tech Stack</h2>
      <div class="line"></div>
    </div>

    <div class="tech-group">
      <div class="tech-group-label">▸ Backend</div>
      <div class="tech-pills">
        <div class="pill">PHP</div>
        <div class="pill">Laravel</div>
        <div class="pill">Node.js</div>
        <div class="pill">Express.js</div>
      </div>
    </div>

    <div class="tech-group">
      <div class="tech-group-label">▸ Frontend</div>
      <div class="tech-pills">
        <div class="pill green">React.js</div>
        <div class="pill green">JavaScript ES6+</div>
        <div class="pill green">HTML5</div>
        <div class="pill green">CSS3</div>
      </div>
    </div>

    <div class="tech-group">
      <div class="tech-group-label">▸ Database</div>
      <div class="tech-pills">
        <div class="pill purple">MySQL</div>
        <div class="pill purple">MongoDB</div>
      </div>
    </div>

    <div class="tech-group">
      <div class="tech-group-label">▸ CMS & Tools</div>
      <div class="tech-pills">
        <div class="pill">WordPress</div>
        <div class="pill">WooCommerce</div>
        <div class="pill">Git / GitHub</div>
        <div class="pill">REST APIs</div>
        <div class="pill">Web Scraping</div>
        <div class="pill">Automation</div>
      </div>
    </div>
  </div>

  <!-- FEATURED WORK -->
  <div class="section">
    <div class="section-header">
      <span class="icon">🚀</span>
      <h2>Featured Work</h2>
      <div class="line"></div>
    </div>
    <div class="work-grid">
      <div class="work-card">
        <div class="work-icon">🔌</div>
        <div class="work-title">Custom WordPress Plugins</div>
        <div class="work-desc">Tailored functionality beyond limits</div>
      </div>
      <div class="work-card">
        <div class="work-icon">📅</div>
        <div class="work-title">Booking & Villa Systems</div>
        <div class="work-desc">End-to-end management platforms</div>
      </div>
      <div class="work-card">
        <div class="work-icon">🤝</div>
        <div class="work-title">CRM Systems</div>
        <div class="work-desc">Enterprise-grade relationship tools</div>
      </div>
      <div class="work-card">
        <div class="work-icon">⚙️</div>
        <div class="work-title">API-Based Applications</div>
        <div class="work-desc">Seamless integrations & REST services</div>
      </div>
      <div class="work-card">
        <div class="work-icon">🕷️</div>
        <div class="work-title">Web Scraping Solutions</div>
        <div class="work-desc">Automated data extraction pipelines</div>
      </div>
      <div class="work-card">
        <div class="work-icon">🌐</div>
        <div class="work-title">Full-Stack MERN Apps</div>
        <div class="work-desc">Scalable, modern web applications</div>
      </div>
    </div>
  </div>

  <!-- CURRENT FOCUS -->
  <div class="section">
    <div class="section-header">
      <span class="icon">🎯</span>
      <h2>Current Focus</h2>
      <div class="line"></div>
    </div>
    <div class="focus-list">
      <div class="focus-item">
        <span class="tag">SAAS</span>
        Scalable SaaS Applications — building for growth from day one
      </div>
      <div class="focus-item">
        <span class="tag">CMS</span>
        Advanced WordPress Architecture — custom systems that actually scale
      </div>
      <div class="focus-item">
        <span class="tag">API</span>
        Microservices & API Optimization — faster, leaner, more resilient
      </div>
    </div>
  </div>

  <!-- CTA -->
  <div class="cta">
    <div class="cta-text">// ready to build something remarkable?</div>
    <a href="mailto:" class="cta-btn"><span>Let's Collaborate</span></a>
  </div>

  <div class="footer">
    SANJAN.KUMAR &nbsp;///&nbsp; FULL STACK DEVELOPER &nbsp;///&nbsp; 2025
  </div>

</div>

</body>
</html>
