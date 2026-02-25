<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Sanjan Kumar – GitHub Profile</title>
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
    cursor: none;
  }

  /* ── CUSTOM CURSOR ── */
  .cursor-dot {
    width: 8px; height: 8px;
    background: var(--cyan);
    border-radius: 50%;
    position: fixed;
    pointer-events: none;
    z-index: 99999;
    transform: translate(-50%, -50%);
    transition: transform 0.05s;
    box-shadow: 0 0 12px var(--cyan), 0 0 24px var(--cyan);
  }
  .cursor-ring {
    width: 32px; height: 32px;
    border: 1px solid rgba(0,245,255,0.5);
    border-radius: 50%;
    position: fixed;
    pointer-events: none;
    z-index: 99998;
    transform: translate(-50%, -50%);
    transition: transform 0.12s ease, width 0.2s, height 0.2s, border-color 0.2s;
  }
  body:has(a:hover) .cursor-ring,
  body:has(.pill:hover) .cursor-ring,
  body:has(.work-card:hover) .cursor-ring {
    width: 48px; height: 48px;
    border-color: var(--green);
  }

  /* ── PARTICLES CANVAS ── */
  #particles {
    position: fixed;
    inset: 0;
    pointer-events: none;
    z-index: 0;
  }

  /* ── GRID BACKGROUND ── */
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
    animation: gridPulse 8s ease-in-out infinite;
  }

  @keyframes gridPulse {
    0%, 100% { opacity: 1; }
    50% { opacity: 0.4; }
  }

  /* ── SCANLINE ── */
  .scanline {
    position: fixed;
    left: 0; right: 0;
    height: 3px;
    background: linear-gradient(90deg, transparent, rgba(0,245,255,0.2), transparent);
    animation: scanline 5s linear infinite;
    pointer-events: none;
    z-index: 9999;
  }
  @keyframes scanline {
    0% { top: -3px; }
    100% { top: 100vh; }
  }

  /* ── CONTAINER ── */
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
    padding: 70px 0 56px;
    position: relative;
  }

  /* Rotating orb behind hero */
  .hero::before {
    content: '';
    position: absolute;
    top: 50%; left: 50%;
    transform: translate(-50%, -50%);
    width: 600px; height: 400px;
    background: radial-gradient(ellipse, rgba(0,245,255,0.06) 0%, transparent 65%);
    animation: orbPulse 4s ease-in-out infinite;
    pointer-events: none;
  }
  @keyframes orbPulse {
    0%, 100% { opacity: 1; transform: translate(-50%, -50%) scale(1); }
    50% { opacity: 0.5; transform: translate(-50%, -50%) scale(1.1); }
  }

  /* ── BOOT TEXT ── */
  .boot-text {
    font-family: 'Share Tech Mono', monospace;
    font-size: 12px;
    color: rgba(0,245,255,0.5);
    letter-spacing: 3px;
    margin-bottom: 32px;
    min-height: 20px;
  }

  /* ── GLITCH TITLE ── */
  .glitch-wrap {
    position: relative;
    display: inline-block;
    margin: 4px 0 12px;
    opacity: 0;
    animation: fadeUp 0.6s ease 2.2s forwards;
  }

  .hero-title {
    font-family: 'Orbitron', monospace;
    font-size: clamp(26px, 5vw, 50px);
    font-weight: 900;
    color: #fff;
    letter-spacing: 3px;
    position: relative;
    text-shadow: 0 0 40px rgba(0,245,255,0.3);
  }

  .hero-title span { color: var(--cyan); }

  /* Glitch layers */
  .glitch-wrap::before,
  .glitch-wrap::after {
    content: attr(data-text);
    font-family: 'Orbitron', monospace;
    font-size: clamp(26px, 5vw, 50px);
    font-weight: 900;
    letter-spacing: 3px;
    position: absolute;
    top: 0; left: 0;
    width: 100%;
    color: #fff;
    clip-path: inset(0 0 100% 0);
  }
  .glitch-wrap::before {
    color: #ff00ff;
    text-shadow: -3px 0 #ff00ff;
    animation: glitchTop 5s infinite linear;
  }
  .glitch-wrap::after {
    color: var(--cyan);
    text-shadow: 3px 0 var(--cyan);
    animation: glitchBot 5s infinite linear;
  }

  @keyframes glitchTop {
    0%, 90%, 100% { clip-path: inset(0 0 100% 0); transform: none; }
    92% { clip-path: inset(0 0 60% 0); transform: translate(-3px, -2px); }
    94% { clip-path: inset(20% 0 50% 0); transform: translate(3px, 0); }
    96% { clip-path: inset(40% 0 30% 0); transform: translate(-2px, 1px); }
    98% { clip-path: inset(60% 0 10% 0); transform: translate(2px, -1px); }
  }
  @keyframes glitchBot {
    0%, 90%, 100% { clip-path: inset(100% 0 0 0); transform: none; }
    92% { clip-path: inset(60% 0 0 0); transform: translate(3px, 2px); }
    94% { clip-path: inset(50% 0 20% 0); transform: translate(-3px, 0); }
    96% { clip-path: inset(30% 0 40% 0); transform: translate(2px, -1px); }
    98% { clip-path: inset(10% 0 60% 0); transform: translate(-2px, 1px); }
  }

  /* ── TYPING SUBTITLE ── */
  .typing-wrap {
    font-family: 'Share Tech Mono', monospace;
    color: rgba(224,232,240,0.6);
    font-size: 13px;
    letter-spacing: 2px;
    min-height: 22px;
    opacity: 0;
    animation: fadeIn 0.4s ease 2.8s forwards;
  }
  .typing-wrap em { color: var(--green); font-style: normal; }
  .type-cursor {
    display: inline-block;
    width: 2px; height: 14px;
    background: var(--green);
    vertical-align: middle;
    margin-left: 2px;
    animation: blink 0.8s step-end infinite;
  }
  @keyframes blink { 0%,100%{opacity:1} 50%{opacity:0} }

  /* ── DIVIDER ── */
  .divider {
    height: 1px;
    background: linear-gradient(90deg, transparent, var(--cyan), var(--purple), transparent);
    margin: 40px 0;
    opacity: 0;
    position: relative;
    overflow: visible;
    animation: fadeIn 0.8s ease 3s forwards;
  }
  .divider::after {
    content: '';
    position: absolute;
    top: -1px; left: 0;
    width: 60px; height: 3px;
    background: var(--cyan);
    box-shadow: 0 0 12px var(--cyan);
    animation: dividerSweep 3s ease-in-out 3.2s infinite;
  }
  @keyframes dividerSweep {
    0% { left: 0; opacity: 1; }
    100% { left: 100%; opacity: 0; }
  }

  /* ── STATS ── */
  .stats {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 16px;
    margin-bottom: 40px;
  }

  .stat-card {
    border: 1px solid var(--border);
    background: var(--card);
    border-radius: 8px;
    padding: 20px 16px;
    text-align: center;
    position: relative;
    overflow: hidden;
    transition: border-color 0.3s, box-shadow 0.3s, transform 0.3s;
    opacity: 0;
    transform: translateY(30px);
  }
  .stat-card.visible {
    animation: slideIn 0.5s ease forwards;
  }
  .stat-card:nth-child(1) { animation-delay: 0.1s; }
  .stat-card:nth-child(2) { animation-delay: 0.2s; }
  .stat-card:nth-child(3) { animation-delay: 0.3s; }

  .stat-card::before {
    content: '';
    position: absolute;
    top: 0; left: 0; right: 0;
    height: 2px;
    background: linear-gradient(90deg, var(--cyan), var(--purple));
    animation: shimmer 3s ease-in-out infinite;
  }
  @keyframes shimmer {
    0%, 100% { background-position: 0%; opacity: 1; }
    50% { opacity: 0.5; }
  }

  .stat-card:hover {
    border-color: var(--cyan);
    box-shadow: var(--glow), inset 0 0 30px rgba(0,245,255,0.03);
    transform: translateY(-4px) scale(1.02);
  }

  .stat-num {
    font-family: 'Orbitron', monospace;
    font-size: 36px;
    font-weight: 700;
    color: var(--cyan);
    display: block;
    animation: numberGlow 3s ease-in-out infinite;
  }
  @keyframes numberGlow {
    0%, 100% { text-shadow: 0 0 10px rgba(0,245,255,0.5); }
    50% { text-shadow: 0 0 30px rgba(0,245,255,1), 0 0 60px rgba(0,245,255,0.5); }
  }

  .stat-label {
    font-size: 11px;
    letter-spacing: 2px;
    text-transform: uppercase;
    color: rgba(224,232,240,0.5);
    margin-top: 4px;
  }

  /* ── SCROLL REVEAL ── */
  .reveal {
    opacity: 0;
    transform: translateY(40px);
    transition: opacity 0.7s ease, transform 0.7s ease;
  }
  .reveal.visible {
    opacity: 1;
    transform: translateY(0);
  }
  .reveal-left {
    opacity: 0;
    transform: translateX(-40px);
    transition: opacity 0.7s ease, transform 0.7s ease;
  }
  .reveal-left.visible { opacity: 1; transform: translateX(0); }

  @keyframes slideIn {
    from { opacity: 0; transform: translateY(30px); }
    to { opacity: 1; transform: translateY(0); }
  }

  /* ── SECTIONS ── */
  .section { margin-bottom: 40px; }

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
    flex: 1; height: 1px;
    background: var(--border);
    position: relative;
    overflow: hidden;
  }
  .section-header .line::after {
    content: '';
    position: absolute;
    top: 0; left: -100%;
    width: 100%; height: 100%;
    background: linear-gradient(90deg, transparent, var(--cyan), transparent);
    animation: lineSweep 2.5s ease-in-out infinite;
  }
  @keyframes lineSweep {
    0% { left: -100%; }
    100% { left: 100%; }
  }
  .section-header .icon { font-size: 16px; }

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
    transition: border-color 0.3s, transform 0.3s, background 0.3s;
    opacity: 0;
    transform: translateX(-20px);
  }
  .about-item.visible {
    animation: slideInLeft 0.5s ease forwards;
  }
  @keyframes slideInLeft {
    to { opacity: 1; transform: translateX(0); }
  }
  .about-item:hover {
    border-color: rgba(0,245,255,0.6);
    background: rgba(0,245,255,0.04);
    transform: translateX(4px);
  }
  .about-item .dot {
    width: 6px; height: 6px;
    border-radius: 50%;
    background: var(--cyan);
    flex-shrink: 0;
    margin-top: 6px;
    box-shadow: 0 0 8px var(--cyan);
    animation: dotPulse 2s ease-in-out infinite;
  }
  @keyframes dotPulse {
    0%, 100% { box-shadow: 0 0 4px var(--cyan); transform: scale(1); }
    50% { box-shadow: 0 0 16px var(--cyan); transform: scale(1.4); }
  }

  /* ── TECH STACK ── */
  .tech-group { margin-bottom: 16px; }

  .tech-group-label {
    font-family: 'Share Tech Mono', monospace;
    font-size: 11px;
    letter-spacing: 3px;
    color: var(--purple);
    text-transform: uppercase;
    margin-bottom: 10px;
    animation: purplePulse 3s ease-in-out infinite;
  }
  @keyframes purplePulse {
    0%, 100% { color: var(--purple); }
    50% { color: rgba(191,0,255,0.5); }
  }

  .tech-pills { display: flex; flex-wrap: wrap; gap: 8px; }

  .pill {
    font-family: 'Share Tech Mono', monospace;
    font-size: 12px;
    padding: 5px 14px;
    border-radius: 3px;
    border: 1px solid var(--border);
    background: rgba(0,245,255,0.04);
    color: rgba(224,232,240,0.85);
    letter-spacing: 1px;
    transition: all 0.25s;
    cursor: default;
    position: relative;
    overflow: hidden;
    opacity: 0;
    transform: scale(0.85);
  }
  .pill.visible {
    animation: popIn 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275) forwards;
  }
  @keyframes popIn {
    to { opacity: 1; transform: scale(1); }
  }
  .pill::before {
    content: '';
    position: absolute;
    top: 0; left: -100%;
    width: 100%; height: 100%;
    background: linear-gradient(90deg, transparent, rgba(255,255,255,0.06), transparent);
    transition: left 0.4s;
  }
  .pill:hover::before { left: 100%; }
  .pill:hover {
    border-color: var(--cyan);
    color: var(--cyan);
    background: rgba(0,245,255,0.08);
    box-shadow: 0 0 16px rgba(0,245,255,0.25);
    transform: translateY(-2px);
  }
  .pill.green { border-color: rgba(57,255,20,0.25); }
  .pill.green:hover { border-color: var(--green); color: var(--green); box-shadow: 0 0 16px rgba(57,255,20,0.25); }
  .pill.purple { border-color: rgba(191,0,255,0.25); }
  .pill.purple:hover { border-color: var(--purple); color: var(--purple); box-shadow: 0 0 16px rgba(191,0,255,0.25); }

  /* ── WORK CARDS ── */
  .work-grid {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 12px;
  }

  .work-card {
    border: 1px solid var(--border);
    background: var(--card);
    border-radius: 8px;
    padding: 18px 20px;
    position: relative;
    overflow: hidden;
    transition: all 0.35s;
    opacity: 0;
    transform: translateY(20px);
  }
  .work-card.visible {
    animation: slideIn 0.5s ease forwards;
  }
  .work-card::before {
    content: '';
    position: absolute;
    top: -50%; left: -50%;
    width: 200%; height: 200%;
    background: conic-gradient(from 0deg, transparent 0%, rgba(0,245,255,0.04) 50%, transparent 100%);
    animation: cardRotate 8s linear infinite;
    opacity: 0;
    transition: opacity 0.3s;
  }
  .work-card:hover::before { opacity: 1; }
  @keyframes cardRotate {
    from { transform: rotate(0deg); }
    to { transform: rotate(360deg); }
  }
  .work-card::after {
    content: '';
    position: absolute;
    bottom: 0; left: 0; right: 0;
    height: 2px;
    background: linear-gradient(90deg, var(--cyan), var(--green));
    transform: scaleX(0);
    transform-origin: left;
    transition: transform 0.4s;
  }
  .work-card:hover::after { transform: scaleX(1); }
  .work-card:hover {
    border-color: rgba(0,245,255,0.5);
    box-shadow: 0 8px 32px rgba(0,245,255,0.1);
    transform: translateY(-5px);
  }

  .work-icon {
    font-size: 22px;
    margin-bottom: 10px;
    display: block;
    transition: transform 0.3s;
  }
  .work-card:hover .work-icon { transform: scale(1.2) rotate(-5deg); }

  .work-title {
    font-family: 'Orbitron', monospace;
    font-size: 11px;
    font-weight: 700;
    letter-spacing: 1px;
    color: #fff;
  }
  .work-desc {
    font-size: 12px;
    color: rgba(224,232,240,0.45);
    margin-top: 4px;
  }

  /* ── FOCUS ── */
  .focus-list { display: flex; flex-direction: column; gap: 10px; }

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
    transition: all 0.3s;
    position: relative;
    overflow: hidden;
    opacity: 0;
    transform: translateX(-30px);
  }
  .focus-item.visible {
    animation: slideInLeft 0.5s ease forwards;
  }
  .focus-item::after {
    content: '';
    position: absolute;
    top: 0; left: 0;
    width: 0; height: 100%;
    background: rgba(0,245,255,0.04);
    transition: width 0.4s;
  }
  .focus-item:hover::after { width: 100%; }
  .focus-item:hover {
    border-left-color: var(--green);
    transform: translateX(6px);
  }
  .focus-item .tag {
    font-family: 'Share Tech Mono', monospace;
    font-size: 10px;
    letter-spacing: 2px;
    color: var(--cyan);
    min-width: 70px;
    position: relative;
    z-index: 1;
    animation: tagGlow 3s ease-in-out infinite;
  }
  @keyframes tagGlow {
    0%, 100% { text-shadow: none; }
    50% { text-shadow: 0 0 10px var(--cyan); }
  }
  .focus-item span:last-child { position: relative; z-index: 1; }

  /* ── CTA ── */
  .cta {
    text-align: center;
    padding: 56px 0 32px;
  }

  .cta-text {
    font-family: 'Share Tech Mono', monospace;
    color: rgba(224,232,240,0.4);
    font-size: 12px;
    letter-spacing: 3px;
    margin-bottom: 24px;
    animation: ctaFade 3s ease-in-out infinite;
  }
  @keyframes ctaFade {
    0%, 100% { opacity: 0.4; }
    50% { opacity: 0.8; }
  }

  .cta-btn {
    display: inline-block;
    font-family: 'Orbitron', monospace;
    font-size: 12px;
    font-weight: 700;
    letter-spacing: 4px;
    text-transform: uppercase;
    padding: 16px 42px;
    border: 1px solid var(--cyan);
    color: var(--cyan);
    text-decoration: none;
    border-radius: 3px;
    position: relative;
    overflow: hidden;
    transition: all 0.35s;
    box-shadow: 0 0 0px var(--cyan);
    animation: btnPulse 3s ease-in-out infinite;
  }
  @keyframes btnPulse {
    0%, 100% { box-shadow: 0 0 8px rgba(0,245,255,0.2); }
    50% { box-shadow: 0 0 24px rgba(0,245,255,0.5); }
  }
  .cta-btn::before {
    content: '';
    position: absolute;
    inset: 0;
    background: var(--cyan);
    transform: scaleX(0);
    transform-origin: left;
    transition: transform 0.35s;
  }
  .cta-btn:hover { color: var(--dark); box-shadow: var(--glow); }
  .cta-btn:hover::before { transform: scaleX(1); }
  .cta-btn span { position: relative; z-index: 1; }

  /* ── FOOTER ── */
  .footer {
    text-align: center;
    padding: 24px 0;
    border-top: 1px solid var(--border);
    font-family: 'Share Tech Mono', monospace;
    font-size: 11px;
    color: rgba(224,232,240,0.15);
    letter-spacing: 2px;
    animation: footerBlink 6s ease-in-out infinite;
  }
  @keyframes footerBlink {
    0%, 100% { opacity: 0.6; }
    50% { opacity: 1; }
  }

  /* ── HELPERS ── */
  @keyframes fadeUp {
    from { opacity: 0; transform: translateY(20px); }
    to { opacity: 1; transform: translateY(0); }
  }
  @keyframes fadeIn {
    from { opacity: 0; }
    to { opacity: 1; }
  }

  @media (max-width: 600px) {
    .about-grid { grid-template-columns: 1fr; }
    .work-grid { grid-template-columns: 1fr; }
    .hero-title { font-size: 24px; }
    body { cursor: auto; }
    .cursor-dot, .cursor-ring { display: none; }
  }
</style>
</head>
<body>

<!-- Custom cursor -->
<div class="cursor-dot" id="cursorDot"></div>
<div class="cursor-ring" id="cursorRing"></div>

<!-- Particles -->
<canvas id="particles"></canvas>

<!-- Scanline -->
<div class="scanline"></div>

<div class="container">

  <!-- HERO -->
  <div class="hero">
    <div class="boot-text" id="bootText"></div>
    <div class="glitch-wrap" id="glitchWrap" data-text="SANJAN KUMAR">
      <h1 class="hero-title">SANJAN <span>KUMAR</span></h1>
    </div>
    <div class="typing-wrap" id="typingWrap">
      <span id="typingTarget"></span><span class="type-cursor"></span>
    </div>
  </div>

  <div class="divider"></div>

  <!-- STATS -->
  <div class="stats">
    <div class="stat-card">
      <span class="stat-num" data-target="5">0</span>
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
  <div class="section reveal">
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
  <div class="section reveal">
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
  <div class="section reveal">
    <div class="section-header">
      <span class="icon">🚀</span>
      <h2>Featured Work</h2>
      <div class="line"></div>
    </div>
    <div class="work-grid">
      <div class="work-card"><span class="work-icon">🔌</span><div class="work-title">Custom WordPress Plugins</div><div class="work-desc">Tailored functionality beyond limits</div></div>
      <div class="work-card"><span class="work-icon">📅</span><div class="work-title">Booking & Villa Systems</div><div class="work-desc">End-to-end management platforms</div></div>
      <div class="work-card"><span class="work-icon">🤝</span><div class="work-title">CRM Systems</div><div class="work-desc">Enterprise-grade relationship tools</div></div>
      <div class="work-card"><span class="work-icon">⚙️</span><div class="work-title">API-Based Applications</div><div class="work-desc">Seamless integrations & REST services</div></div>
      <div class="work-card"><span class="work-icon">🕷️</span><div class="work-title">Web Scraping Solutions</div><div class="work-desc">Automated data extraction pipelines</div></div>
      <div class="work-card"><span class="work-icon">🌐</span><div class="work-title">Full-Stack MERN Apps</div><div class="work-desc">Scalable, modern web applications</div></div>
    </div>
  </div>

  <!-- CURRENT FOCUS -->
  <div class="section reveal">
    <div class="section-header">
      <span class="icon">🎯</span>
      <h2>Current Focus</h2>
      <div class="line"></div>
    </div>
    <div class="focus-list">
      <div class="focus-item"><span class="tag">SAAS</span><span>Scalable SaaS Applications — building for growth from day one</span></div>
      <div class="focus-item"><span class="tag">CMS</span><span>Advanced WordPress Architecture — custom systems that actually scale</span></div>
      <div class="focus-item"><span class="tag">API</span><span>Microservices & API Optimization — faster, leaner, more resilient</span></div>
    </div>
  </div>

  <!-- CTA -->
  <div class="cta reveal">
    <div class="cta-text">// ready to build something remarkable?</div>
    <a href="mailto:" class="cta-btn"><span>Let's Collaborate</span></a>
  </div>

  <div class="footer">
    SANJAN.KUMAR &nbsp;///&nbsp; FULL STACK DEVELOPER &nbsp;///&nbsp; 2025
  </div>

</div>

<script>
// ── CUSTOM CURSOR ──
const dot = document.getElementById('cursorDot');
const ring = document.getElementById('cursorRing');
let mx = -100, my = -100, rx = -100, ry = -100;

document.addEventListener('mousemove', e => { mx = e.clientX; my = e.clientY; });

function animateCursor() {
  dot.style.left = mx + 'px'; dot.style.top = my + 'px';
  rx += (mx - rx) * 0.12; ry += (my - ry) * 0.12;
  ring.style.left = rx + 'px'; ring.style.top = ry + 'px';
  requestAnimationFrame(animateCursor);
}
animateCursor();

// ── PARTICLES ──
const canvas = document.getElementById('particles');
const ctx = canvas.getContext('2d');
let particles = [];

function resizeCanvas() {
  canvas.width = window.innerWidth;
  canvas.height = window.innerHeight;
}
resizeCanvas();
window.addEventListener('resize', resizeCanvas);

function createParticle() {
  return {
    x: Math.random() * canvas.width,
    y: Math.random() * canvas.height,
    vx: (Math.random() - 0.5) * 0.4,
    vy: -Math.random() * 0.6 - 0.2,
    size: Math.random() * 2 + 0.5,
    opacity: Math.random() * 0.6 + 0.1,
    color: Math.random() > 0.6 ? '#00f5ff' : Math.random() > 0.5 ? '#39ff14' : '#bf00ff',
    life: 0,
    maxLife: Math.random() * 300 + 150,
  };
}

for (let i = 0; i < 80; i++) particles.push(createParticle());

function drawParticles() {
  ctx.clearRect(0, 0, canvas.width, canvas.height);

  // Connection lines between nearby particles
  for (let i = 0; i < particles.length; i++) {
    for (let j = i + 1; j < particles.length; j++) {
      const dx = particles[i].x - particles[j].x;
      const dy = particles[i].y - particles[j].y;
      const dist = Math.sqrt(dx*dx + dy*dy);
      if (dist < 120) {
        ctx.beginPath();
        ctx.strokeStyle = `rgba(0,245,255,${0.06 * (1 - dist / 120)})`;
        ctx.lineWidth = 0.5;
        ctx.moveTo(particles[i].x, particles[i].y);
        ctx.lineTo(particles[j].x, particles[j].y);
        ctx.stroke();
      }
    }
  }

  particles.forEach((p, i) => {
    p.x += p.vx; p.y += p.vy; p.life++;
    const lifeRatio = p.life / p.maxLife;
    const alpha = p.opacity * Math.sin(lifeRatio * Math.PI);

    ctx.beginPath();
    ctx.arc(p.x, p.y, p.size, 0, Math.PI * 2);
    ctx.fillStyle = p.color.replace(')', `,${alpha})`).replace('rgb', 'rgba').replace('#00f5ff', `rgba(0,245,255,${alpha})`).replace('#39ff14', `rgba(57,255,20,${alpha})`).replace('#bf00ff', `rgba(191,0,255,${alpha})`);

    // Draw glow
    ctx.shadowBlur = 10;
    ctx.shadowColor = p.color;
    ctx.fill();
    ctx.shadowBlur = 0;

    if (p.life >= p.maxLife || p.y < -10) particles[i] = createParticle();
  });

  requestAnimationFrame(drawParticles);
}
drawParticles();

// ── BOOT TEXT SEQUENCE ──
const bootLines = [
  '> Booting system...',
  '> Loading profile.exe',
  '> Auth: VERIFIED ✓',
];
let lineIdx = 0, charIdx = 0;
const bootEl = document.getElementById('bootText');

function typeBoot() {
  if (lineIdx >= bootLines.length) {
    setTimeout(() => {
      bootEl.style.transition = 'opacity 0.5s';
      bootEl.style.opacity = '0';
      setTimeout(startTitle, 500);
    }, 300);
    return;
  }
  const line = bootLines[lineIdx];
  bootEl.textContent = line.substring(0, charIdx + 1);
  charIdx++;
  if (charIdx >= line.length) {
    charIdx = 0; lineIdx++;
    setTimeout(typeBoot, 400);
  } else {
    setTimeout(typeBoot, 40);
  }
}

function startTitle() {
  document.getElementById('glitchWrap').style.animationPlayState = 'running';
  setTimeout(startSubtitle, 600);
}

// ── TYPING SUBTITLE ──
const subtitle = 'Senior Full Stack Developer | PHP • WordPress • Laravel • MERN';
let si = 0;
const typingEl = document.getElementById('typingTarget');
const typingWrap = document.getElementById('typingWrap');

function typeSubtitle() {
  typingEl.textContent = subtitle.substring(0, si);
  si++;
  if (si <= subtitle.length) setTimeout(typeSubtitle, 35);
}

function startSubtitle() {
  typingWrap.style.opacity = '1';
  typeSubtitle();
}

setTimeout(typeBoot, 400);

// ── COUNTER ANIMATION ──
function animateCounter(el, target) {
  let current = 0;
  const step = target / 30;
  const interval = setInterval(() => {
    current += step;
    if (current >= target) { el.textContent = target + '+'; clearInterval(interval); }
    else el.textContent = Math.floor(current) + '+';
  }, 50);
}

// ── INTERSECTION OBSERVER ──
const observer = new IntersectionObserver((entries) => {
  entries.forEach(entry => {
    if (entry.isIntersecting) {
      entry.target.classList.add('visible');
      observer.unobserve(entry.target);
    }
  });
}, { threshold: 0.1 });

// Reveal sections
document.querySelectorAll('.reveal').forEach(el => observer.observe(el));

// Stat cards
document.querySelectorAll('.stat-card').forEach((card, i) => {
  const obsCard = new IntersectionObserver(entries => {
    if (entries[0].isIntersecting) {
      setTimeout(() => {
        card.classList.add('visible');
        const numEl = card.querySelector('[data-target]');
        if (numEl) animateCounter(numEl, parseInt(numEl.dataset.target));
      }, i * 120);
      obsCard.unobserve(card);
    }
  }, { threshold: 0.2 });
  obsCard.observe(card);
});

// About items stagger
document.querySelectorAll('.about-item').forEach((item, i) => {
  const obs = new IntersectionObserver(entries => {
    if (entries[0].isIntersecting) {
      setTimeout(() => item.classList.add('visible'), i * 80);
      obs.unobserve(item);
    }
  }, { threshold: 0.1 });
  obs.observe(item);
});

// Pills stagger
document.querySelectorAll('.pill').forEach((pill, i) => {
  const obs = new IntersectionObserver(entries => {
    if (entries[0].isIntersecting) {
      setTimeout(() => pill.classList.add('visible'), i * 60);
      obs.unobserve(pill);
    }
  }, { threshold: 0.1 });
  obs.observe(pill);
});

// Work cards stagger
document.querySelectorAll('.work-card').forEach((card, i) => {
  const obs = new IntersectionObserver(entries => {
    if (entries[0].isIntersecting) {
      setTimeout(() => card.classList.add('visible'), i * 90);
      obs.unobserve(card);
    }
  }, { threshold: 0.1 });
  obs.observe(card);
});

// Focus items
document.querySelectorAll('.focus-item').forEach((item, i) => {
  const obs = new IntersectionObserver(entries => {
    if (entries[0].isIntersecting) {
      setTimeout(() => item.classList.add('visible'), i * 120);
      obs.unobserve(item);
    }
  }, { threshold: 0.1 });
  obs.observe(item);
});
</script>

</body>
</html>
