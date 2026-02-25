<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Sanjan Kumar — GitHub README Preview</title>
<link href="https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@400;600;700&family=Syne:wght@700;800&display=swap" rel="stylesheet"/>
<style>
  *, *::before, *::after { margin: 0; padding: 0; box-sizing: border-box; }

  :root {
    --bg: #0d1117;
    --surface: #161b22;
    --surface2: #1c2330;
    --cyan: #00d4ff;<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Sanjan Kumar — GitHub README Preview</title>
<link href="https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@400;600;700&family=Syne:wght@700;800&display=swap" rel="stylesheet"/>
<style>
  *, *::before, *::after { margin: 0; padding: 0; box-sizing: border-box; }

  :root {
    --bg: #0d1117;
    --surface: #161b22;
    --surface2: #1c2330;
    --cyan: #00d4ff;
    --purple: #7b2ff7;
    --green: #39d353;
    --text: #c9d1d9;
    --muted: #8b949e;
    --border: rgba(0,212,255,0.15);
  }

  body {
    background: var(--bg);
    color: var(--text);
    font-family: 'JetBrains Mono', monospace;
    line-height: 1.6;
    overflow-x: hidden;
  }

  /* ANIMATED GRID BACKGROUND */
  body::before {
    content: '';
    position: fixed;
    inset: 0;
    background-image:
      linear-gradient(rgba(0,212,255,0.03) 1px, transparent 1px),
      linear-gradient(90deg, rgba(0,212,255,0.03) 1px, transparent 1px);
    background-size: 40px 40px;
    pointer-events: none;
    z-index: 0;
  }

  .container {
    max-width: 860px;
    margin: 0 auto;
    padding: 0 24px 60px;
    position: relative;
    z-index: 1;
  }

  /* ─── HEADER ─── */
  .header {
    position: relative;
    text-align: center;
    padding: 0 0 40px;
    overflow: hidden;
  }

  .header-wave {
    width: 100%;
    height: 180px;
    background: linear-gradient(135deg, #0d1117 0%, #0a1628 40%, #0d1528 60%, #0d1117 100%);
    position: relative;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    border-radius: 0 0 40px 40px;
    margin-bottom: 28px;
    border: 1px solid var(--border);
    border-top: none;
  }

  .header-wave::before {
    content: '';
    position: absolute;
    inset: 0;
    background: linear-gradient(135deg, rgba(0,212,255,0.08) 0%, rgba(123,47,247,0.12) 100%);
    border-radius: inherit;
  }

  /* Animated scan line */
  .header-wave::after {
    content: '';
    position: absolute;
    left: 0; right: 0;
    height: 2px;
    background: linear-gradient(90deg, transparent, var(--cyan), transparent);
    animation: scanLine 3s ease-in-out infinite;
    opacity: 0.6;
  }

  @keyframes scanLine {
    0% { top: 0; opacity: 0; }
    10% { opacity: 0.6; }
    90% { opacity: 0.6; }
    100% { top: 100%; opacity: 0; }
  }

  .name {
    font-family: 'Syne', sans-serif;
    font-size: 2.8rem;
    font-weight: 800;
    background: linear-gradient(135deg, #ffffff 0%, var(--cyan) 50%, var(--purple) 100%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
    position: relative;
    z-index: 1;
    animation: fadeSlideDown 0.8s ease both;
  }

  .role {
    font-size: 0.85rem;
    color: var(--cyan);
    letter-spacing: 3px;
    text-transform: uppercase;
    position: relative;
    z-index: 1;
    animation: fadeSlideDown 0.8s 0.2s ease both;
    opacity: 0;
    animation-fill-mode: forwards;
  }

  @keyframes fadeSlideDown {
    from { opacity: 0; transform: translateY(-16px); }
    to { opacity: 1; transform: translateY(0); }
  }

  /* Typing animation */
  .typing-container {
    display: flex;
    justify-content: center;
    gap: 8px;
    flex-wrap: wrap;
  }

  .typing-text {
    color: var(--cyan);
    font-size: 0.9rem;
    overflow: hidden;
    white-space: nowrap;
    border-right: 2px solid var(--cyan);
    animation: typing 3.5s steps(40) infinite, blink 0.75s step-end infinite;
    max-width: 500px;
    text-align: left;
  }

  @keyframes typing {
    0%,100% { width: 0 }
    30%,70% { width: 100% }
  }
  @keyframes blink {
    50% { border-color: transparent }
  }

  /* ─── BADGES ─── */
  .badges {
    display: flex;
    justify-content: center;
    gap: 10px;
    flex-wrap: wrap;
    margin: 20px 0;
  }

  .badge {
    padding: 6px 16px;
    border-radius: 20px;
    font-size: 0.72rem;
    font-weight: 600;
    letter-spacing: 1px;
    text-transform: uppercase;
    animation: fadeIn 1s ease both;
  }

  .badge-cyan { background: rgba(0,212,255,0.12); border: 1px solid rgba(0,212,255,0.4); color: var(--cyan); }
  .badge-purple { background: rgba(123,47,247,0.12); border: 1px solid rgba(123,47,247,0.4); color: #a878ff; }
  .badge-green { background: rgba(57,211,83,0.12); border: 1px solid rgba(57,211,83,0.4); color: var(--green); }

  @keyframes fadeIn {
    from { opacity: 0; transform: scale(0.9); }
    to { opacity: 1; transform: scale(1); }
  }

  /* ─── SECTION HEADERS ─── */
  .section-title {
    font-size: 0.8rem;
    color: var(--cyan);
    letter-spacing: 2px;
    text-transform: uppercase;
    margin: 48px 0 20px;
    display: flex;
    align-items: center;
    gap: 12px;
  }

  .section-title::before { content: '>'; color: var(--purple); }
  .section-title::after {
    content: '';
    flex: 1;
    height: 1px;
    background: linear-gradient(90deg, var(--border), transparent);
  }

  /* ─── ABOUT CARD ─── */
  .about-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 12px;
  }

  .about-item {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 10px;
    padding: 14px 18px;
    display: flex;
    align-items: flex-start;
    gap: 12px;
    transition: border-color 0.3s, transform 0.3s;
  }

  .about-item:hover {
    border-color: rgba(0,212,255,0.4);
    transform: translateY(-2px);
  }

  .about-icon { font-size: 1.2rem; flex-shrink: 0; margin-top: 2px; }
  .about-text { font-size: 0.8rem; color: var(--text); line-height: 1.5; }
  .about-text strong { color: var(--cyan); display: block; font-size: 0.7rem; letter-spacing: 1px; margin-bottom: 2px; }

  /* ─── CODE BLOCK ─── */
  .code-block {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 12px;
    overflow: hidden;
  }

  .code-header {
    display: flex;
    align-items: center;
    gap: 8px;
    padding: 10px 16px;
    background: var(--surface2);
    border-bottom: 1px solid var(--border);
  }

  .dot { width: 10px; height: 10px; border-radius: 50%; }
  .dot-red { background: #ff5f57; }
  .dot-yellow { background: #ffbd2e; }
  .dot-green { background: #28c940; }
  .code-filename { font-size: 0.72rem; color: var(--muted); margin-left: 8px; }

  .code-body {
    padding: 20px;
    font-size: 0.82rem;
    line-height: 1.8;
  }

  .kw { color: #ff7b72; }
  .fn { color: #d2a8ff; }
  .str { color: #a5d6ff; }
  .prop { color: #79c0ff; }
  .comment { color: #8b949e; font-style: italic; }

  /* ─── TECH STACK ─── */
  .tech-category { margin-bottom: 20px; }
  .tech-category-title {
    font-size: 0.7rem;
    color: var(--muted);
    letter-spacing: 2px;
    text-transform: uppercase;
    margin-bottom: 10px;
  }

  .tech-pills {
    display: flex;
    flex-wrap: wrap;
    gap: 8px;
  }

  .pill {
    padding: 6px 14px;
    border-radius: 6px;
    font-size: 0.75rem;
    font-weight: 600;
    border: 1px solid;
    transition: transform 0.2s, box-shadow 0.2s;
    cursor: default;
  }

  .pill:hover {
    transform: translateY(-3px);
    box-shadow: 0 4px 20px rgba(0,212,255,0.2);
  }

  .pill-php { background: rgba(119,107,180,0.15); border-color: rgba(119,107,180,0.5); color: #9b8fdb; }
  .pill-laravel { background: rgba(255,45,32,0.1); border-color: rgba(255,45,32,0.4); color: #ff6b5b; }
  .pill-node { background: rgba(51,153,51,0.1); border-color: rgba(51,153,51,0.4); color: #5dba5d; }
  .pill-express { background: rgba(200,200,200,0.08); border-color: rgba(200,200,200,0.2); color: #ccc; }
  .pill-react { background: rgba(97,218,251,0.1); border-color: rgba(97,218,251,0.4); color: #61dafb; }
  .pill-js { background: rgba(247,223,30,0.1); border-color: rgba(247,223,30,0.3); color: #f7df1e; }
  .pill-html { background: rgba(227,79,38,0.1); border-color: rgba(227,79,38,0.4); color: #e34f26; }
  .pill-css { background: rgba(21,114,182,0.1); border-color: rgba(21,114,182,0.4); color: #4dabf7; }
  .pill-mysql { background: rgba(68,121,161,0.1); border-color: rgba(68,121,161,0.4); color: #5da0d0; }
  .pill-mongo { background: rgba(71,162,72,0.1); border-color: rgba(71,162,72,0.4); color: #4db461; }
  .pill-wp { background: rgba(33,117,179,0.1); border-color: rgba(33,117,179,0.4); color: #56a7d9; }
  .pill-git { background: rgba(240,80,50,0.1); border-color: rgba(240,80,50,0.4); color: #f0583a; }
  .pill-api { background: rgba(0,212,255,0.1); border-color: rgba(0,212,255,0.3); color: var(--cyan); }
  .pill-woo { background: rgba(150,88,138,0.1); border-color: rgba(150,88,138,0.4); color: #c278b0; }

  /* ─── PROJECTS TABLE ─── */
  .projects-grid {
    display: grid;
    gap: 10px;
  }

  .project-row {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    gap: 1px;
    background: var(--border);
    border-radius: 10px;
    overflow: hidden;
    border: 1px solid var(--border);
    transition: border-color 0.3s;
  }

  .project-row:hover { border-color: rgba(0,212,255,0.35); }

  .project-cell {
    background: var(--surface);
    padding: 14px 16px;
    font-size: 0.78rem;
  }

  .project-cell:first-child { color: var(--cyan); font-weight: 700; }
  .project-cell:nth-child(2) { color: var(--muted); }
  .project-cell:nth-child(3) { color: #a878ff; font-size: 0.72rem; }

  .table-header .project-cell {
    background: var(--surface2);
    color: var(--muted);
    font-size: 0.65rem;
    letter-spacing: 1.5px;
    text-transform: uppercase;
  }

  /* ─── STATS ─── */
  .stats-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 12px;
  }

  .stat-card {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 12px;
    padding: 20px;
    text-align: center;
    transition: transform 0.3s, border-color 0.3s;
  }

  .stat-card:hover {
    transform: translateY(-4px);
    border-color: rgba(0,212,255,0.4);
  }

  .stat-number {
    font-family: 'Syne', sans-serif;
    font-size: 2rem;
    font-weight: 800;
    background: linear-gradient(135deg, var(--cyan), var(--purple));
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
  }

  .stat-label { font-size: 0.7rem; color: var(--muted); letter-spacing: 1.5px; text-transform: uppercase; margin-top: 4px; }

  /* ─── CONNECT ─── */
  .connect-grid {
    display: flex;
    gap: 12px;
    flex-wrap: wrap;
    justify-content: center;
  }

  .connect-btn {
    padding: 12px 24px;
    border-radius: 8px;
    font-size: 0.78rem;
    font-weight: 700;
    letter-spacing: 1px;
    text-transform: uppercase;
    text-decoration: none;
    border: 1px solid;
    transition: all 0.3s;
    display: flex;
    align-items: center;
    gap: 8px;
  }

  .connect-btn:hover { transform: translateY(-3px); box-shadow: 0 8px 24px rgba(0,212,255,0.2); }

  .btn-linkedin { background: rgba(0,119,181,0.15); border-color: rgba(0,119,181,0.5); color: #5badd6; }
  .btn-github { background: rgba(255,255,255,0.05); border-color: rgba(255,255,255,0.2); color: #eee; }
  .btn-email { background: rgba(234,67,53,0.1); border-color: rgba(234,67,53,0.4); color: #f07060; }
  .btn-portfolio { background: rgba(0,212,255,0.1); border-color: rgba(0,212,255,0.35); color: var(--cyan); }

  /* ─── QUOTE ─── */
  .quote {
    text-align: center;
    margin-top: 40px;
    padding: 28px;
    background: linear-gradient(135deg, rgba(0,212,255,0.05), rgba(123,47,247,0.08));
    border: 1px solid var(--border);
    border-radius: 16px;
    font-size: 0.85rem;
    color: var(--muted);
    font-style: italic;
    position: relative;
  }

  .quote::before {
    content: '"';
    font-size: 4rem;
    color: var(--cyan);
    opacity: 0.2;
    position: absolute;
    top: -10px;
    left: 20px;
    font-family: 'Syne', sans-serif;
  }

  /* ─── FOOTER ─── */
  .footer-wave {
    margin-top: 50px;
    height: 80px;
    background: linear-gradient(135deg, rgba(123,47,247,0.2), rgba(0,212,255,0.2));
    border-radius: 40px 40px 0 0;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 0.7rem;
    color: var(--muted);
    letter-spacing: 2px;
    border: 1px solid var(--border);
    border-bottom: none;
  }

  /* Divider */
  .divider {
    height: 1px;
    background: linear-gradient(90deg, transparent, var(--border), transparent);
    margin: 8px 0;
  }

  /* Floating particles */
  .particles {
    position: fixed;
    inset: 0;
    pointer-events: none;
    overflow: hidden;
    z-index: 0;
  }

  .particle {
    position: absolute;
    width: 2px;
    height: 2px;
    background: var(--cyan);
    border-radius: 50%;
    animation: float linear infinite;
    opacity: 0;
  }

  @keyframes float {
    0% { transform: translateY(100vh) translateX(0); opacity: 0; }
    10% { opacity: 0.4; }
    90% { opacity: 0.4; }
    100% { transform: translateY(-100px) translateX(var(--dx)); opacity: 0; }
  }

  @media (max-width: 600px) {
    .about-grid { grid-template-columns: 1fr; }
    .stats-grid { grid-template-columns: 1fr 1fr; }
    .project-row { grid-template-columns: 1fr; }
    .name { font-size: 2rem; }
  }
</style>
</head>
<body>

<!-- Floating particles -->
<div class="particles" id="particles"></div>

<div class="container">

  <!-- ─── HEADER ─── -->
  <div class="header">
    <div class="header-wave">
      <div class="name">Sanjan Kumar</div>
      <div class="role">Senior Full Stack Developer</div>
    </div>

    <div class="typing-container">
      <span class="typing-text">PHP • WordPress • Laravel • MERN • REST API • SaaS</span>
    </div>

    <div class="badges" style="margin-top:16px;">
      <span class="badge badge-cyan">⚡ 5+ Years XP</span>
      <span class="badge badge-purple">🔌 API Specialist</span>
      <span class="badge badge-green">✅ Open to Collaborate</span>
    </div>
  </div>

  <div class="divider"></div>

  <!-- ─── ABOUT ─── -->
  <div class="section-title">whoami</div>

  <div class="about-grid">
    <div class="about-item">
      <div class="about-icon">🔥</div>
      <div class="about-text"><strong>WordPress Expert</strong>Custom plugin dev, WooCommerce, API integrations at scale</div>
    </div>
    <div class="about-item">
      <div class="about-icon">⚙️</div>
      <div class="about-text"><strong>Laravel Architect</strong>Enterprise apps, clean architecture, service layers</div>
    </div>
    <div class="about-item">
      <div class="about-icon">🌐</div>
      <div class="about-text"><strong>MERN Stack Dev</strong>MongoDB · Express · React · Node.js full-cycle builds</div>
    </div>
    <div class="about-item">
      <div class="about-icon">🔌</div>
      <div class="about-text"><strong>API Specialist</strong>REST API design, third-party integrations & automation</div>
    </div>
    <div class="about-item">
      <div class="about-icon">🛠️</div>
      <div class="about-text"><strong>Systems Builder</strong>CRM, Booking Systems, Scrapers & Automation Tools</div>
    </div>
    <div class="about-item">
      <div class="about-icon">📈</div>
      <div class="about-text"><strong>Performance First</strong>Scalable, clean, maintainable code — always</div>
    </div>
  </div>

  <!-- ─── CURRENT FOCUS ─── -->
  <div class="section-title">current --focus</div>

  <div class="code-block">
    <div class="code-header">
      <div class="dot dot-red"></div>
      <div class="dot dot-yellow"></div>
      <div class="dot dot-green"></div>
      <span class="code-filename">mission.js</span>
    </div>
    <div class="code-body">
      <span class="kw">const</span> <span class="fn">currentMission</span> = {<br/>
      &nbsp;&nbsp;<span class="prop">building</span>&nbsp;&nbsp;: <span class="str">"Scalable SaaS Applications"</span>,<br/>
      &nbsp;&nbsp;<span class="prop">mastering</span> : <span class="str">"Advanced WordPress Architecture"</span>,<br/>
      &nbsp;&nbsp;<span class="prop">exploring</span> : <span class="str">"Microservices & API Optimization"</span>,<br/>
      &nbsp;&nbsp;<span class="prop">goal</span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;: <span class="str">"Craft solutions that last, scale, and impress."</span><br/>
      };<br/><br/>
      <span class="comment">// 5+ years of building. Still shipping. Still scaling.</span>
    </div>
  </div>

  <!-- ─── TECH STACK ─── -->
  <div class="section-title">tech --stack</div>

  <div class="tech-category">
    <div class="tech-category-title">⚙ Backend</div>
    <div class="tech-pills">
      <span class="pill pill-php">PHP</span>
      <span class="pill pill-laravel">Laravel</span>
      <span class="pill pill-node">Node.js</span>
      <span class="pill pill-express">Express.js</span>
    </div>
  </div>

  <div class="tech-category">
    <div class="tech-category-title">🌐 Frontend</div>
    <div class="tech-pills">
      <span class="pill pill-react">React.js</span>
      <span class="pill pill-js">JavaScript ES6+</span>
      <span class="pill pill-html">HTML5</span>
      <span class="pill pill-css">CSS3</span>
    </div>
  </div>

  <div class="tech-category">
    <div class="tech-category-title">🗄 Database</div>
    <div class="tech-pills">
      <span class="pill pill-mysql">MySQL</span>
      <span class="pill pill-mongo">MongoDB</span>
    </div>
  </div>

  <div class="tech-category">
    <div class="tech-category-title">🛠 CMS & Tools</div>
    <div class="tech-pills">
      <span class="pill pill-wp">WordPress</span>
      <span class="pill pill-woo">WooCommerce</span>
      <span class="pill pill-git">Git / GitHub</span>
      <span class="pill pill-api">REST APIs</span>
    </div>
  </div>

  <!-- ─── PROJECTS ─── -->
  <div class="section-title">projects --featured</div>

  <div class="projects-grid">
    <div class="project-row table-header">
      <div class="project-cell">Project Type</div>
      <div class="project-cell">Tech Used</div>
      <div class="project-cell">Outcome</div>
    </div>
    <div class="project-row">
      <div class="project-cell">⚡ Custom WordPress Plugins</div>
      <div class="project-cell">PHP · WP API · MySQL</div>
      <div class="project-cell">Tailored features for 20+ clients</div>
    </div>
    <div class="project-row">
      <div class="project-cell">🏨 Booking & Villa Mgmt</div>
      <div class="project-cell">Laravel · React · MySQL</div>
      <div class="project-cell">End-to-end reservation automation</div>
    </div>
    <div class="project-row">
      <div class="project-cell">📊 CRM Systems</div>
      <div class="project-cell">MERN Stack · REST API</div>
      <div class="project-cell">Streamlined business workflows</div>
    </div>
    <div class="project-row">
      <div class="project-cell">🔌 API Applications</div>
      <div class="project-cell">Node.js · Express · MongoDB</div>
      <div class="project-cell">High-throughput integrations</div>
    </div>
    <div class="project-row">
      <div class="project-cell">🕷️ Web Scraping Tools</div>
      <div class="project-cell">PHP · Puppeteer · Node.js</div>
      <div class="project-cell">Automated data pipelines</div>
    </div>
    <div class="project-row">
      <div class="project-cell">🚀 Full-Stack MERN Apps</div>
      <div class="project-cell">MongoDB · Express · React</div>
      <div class="project-cell">Scalable SPA architecture</div>
    </div>
  </div>

  <!-- ─── STATS ─── -->
  <div class="section-title">git stats --summary</div>

  <div class="stats-grid">
    <div class="stat-card">
      <div class="stat-number">5+</div>
      <div class="stat-label">Years Experience</div>
    </div>
    <div class="stat-card">
      <div class="stat-number">50+</div>
      <div class="stat-label">Projects Shipped</div>
    </div>
    <div class="stat-card">
      <div class="stat-number">20+</div>
      <div class="stat-label">Happy Clients</div>
    </div>
  </div>

  <!-- ─── CONNECT ─── -->
  <div class="section-title">connect --me</div>

  <div class="connect-grid">
    <a href="#" class="connect-btn btn-linkedin">🔗 LinkedIn</a>
    <a href="#" class="connect-btn btn-github">🐙 GitHub</a>
    <a href="#" class="connect-btn btn-email">📧 Email</a>
    <a href="#" class="connect-btn btn-portfolio">🌐 Portfolio</a>
  </div>

  <!-- ─── QUOTE ─── -->
  <div class="quote">
    I don't just write code — I architect experiences that scale.
  </div>

  <!-- ─── FOOTER ─── -->
  <div class="footer-wave">
    ✦ &nbsp; SANJAN KUMAR &nbsp; · &nbsp; FULL STACK DEVELOPER &nbsp; ✦
  </div>

</div>

<script><!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Sanjan Kumar — GitHub README Preview</title>
<link href="https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@400;600;700&family=Syne:wght@700;800&display=swap" rel="stylesheet"/>
<style>
  *, *::before, *::after { margin: 0; padding: 0; box-sizing: border-box; }

  :root {
    --bg: #0d1117;
    --surface: #161b22;
    --surface2: #1c2330;
    --cyan: #00d4ff;
    --purple: #7b2ff7;
    --green: #39d353;
    --text: #c9d1d9;
    --muted: #8b949e;
    --border: rgba(0,212,255,0.15);
  }

  body {
    background: var(--bg);
    color: var(--text);
    font-family: 'JetBrains Mono', monospace;
    line-height: 1.6;
    overflow-x: hidden;
  }

  /* ANIMATED GRID BACKGROUND */
  body::before {
    content: '';
    position: fixed;
    inset: 0;
    background-image:
      linear-gradient(rgba(0,212,255,0.03) 1px, transparent 1px),
      linear-gradient(90deg, rgba(0,212,255,0.03) 1px, transparent 1px);
    background-size: 40px 40px;
    pointer-events: none;
    z-index: 0;
  }

  .container {
    max-width: 860px;
    margin: 0 auto;
    padding: 0 24px 60px;
    position: relative;
    z-index: 1;
  }

  /* ─── HEADER ─── */
  .header {
    position: relative;
    text-align: center;
    padding: 0 0 40px;
    overflow: hidden;
  }

  .header-wave {
    width: 100%;
    height: 180px;
    background: linear-gradient(135deg, #0d1117 0%, #0a1628 40%, #0d1528 60%, #0d1117 100%);
    position: relative;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    border-radius: 0 0 40px 40px;
    margin-bottom: 28px;
    border: 1px solid var(--border);
    border-top: none;
  }

  .header-wave::before {
    content: '';
    position: absolute;
    inset: 0;
    background: linear-gradient(135deg, rgba(0,212,255,0.08) 0%, rgba(123,47,247,0.12) 100%);
    border-radius: inherit;
  }

  /* Animated scan line */
  .header-wave::after {
    content: '';
    position: absolute;
    left: 0; right: 0;
    height: 2px;
    background: linear-gradient(90deg, transparent, var(--cyan), transparent);
    animation: scanLine 3s ease-in-out infinite;
    opacity: 0.6;
  }

  @keyframes scanLine {
    0% { top: 0; opacity: 0; }
    10% { opacity: 0.6; }
    90% { opacity: 0.6; }
    100% { top: 100%; opacity: 0; }
  }

  .name {
    font-family: 'Syne', sans-serif;
    font-size: 2.8rem;
    font-weight: 800;
    background: linear-gradient(135deg, #ffffff 0%, var(--cyan) 50%, var(--purple) 100%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
    position: relative;
    z-index: 1;
    animation: fadeSlideDown 0.8s ease both;
  }

  .role {
    font-size: 0.85rem;
    color: var(--cyan);
    letter-spacing: 3px;
    text-transform: uppercase;
    position: relative;
    z-index: 1;
    animation: fadeSlideDown 0.8s 0.2s ease both;
    opacity: 0;
    animation-fill-mode: forwards;
  }

  @keyframes fadeSlideDown {
    from { opacity: 0; transform: translateY(-16px); }
    to { opacity: 1; transform: translateY(0); }
  }

  /* Typing animation */
  .typing-container {
    display: flex;
    justify-content: center;
    gap: 8px;
    flex-wrap: wrap;
  }

  .typing-text {
    color: var(--cyan);
    font-size: 0.9rem;
    overflow: hidden;
    white-space: nowrap;
    border-right: 2px solid var(--cyan);
    animation: typing 3.5s steps(40) infinite, blink 0.75s step-end infinite;
    max-width: 500px;
    text-align: left;
  }

  @keyframes typing {
    0%,100% { width: 0 }
    30%,70% { width: 100% }
  }
  @keyframes blink {
    50% { border-color: transparent }
  }

  /* ─── BADGES ─── */
  .badges {
    display: flex;
    justify-content: center;
    gap: 10px;
    flex-wrap: wrap;
    margin: 20px 0;
  }

  .badge {
    padding: 6px 16px;
    border-radius: 20px;
    font-size: 0.72rem;
    font-weight: 600;
    letter-spacing: 1px;
    text-transform: uppercase;
    animation: fadeIn 1s ease both;
  }

  .badge-cyan { background: rgba(0,212,255,0.12); border: 1px solid rgba(0,212,255,0.4); color: var(--cyan); }
  .badge-purple { background: rgba(123,47,247,0.12); border: 1px solid rgba(123,47,247,0.4); color: #a878ff; }
  .badge-green { background: rgba(57,211,83,0.12); border: 1px solid rgba(57,211,83,0.4); color: var(--green); }

  @keyframes fadeIn {
    from { opacity: 0; transform: scale(0.9); }
    to { opacity: 1; transform: scale(1); }
  }

  /* ─── SECTION HEADERS ─── */
  .section-title {
    font-size: 0.8rem;
    color: var(--cyan);
    letter-spacing: 2px;
    text-transform: uppercase;
    margin: 48px 0 20px;
    display: flex;
    align-items: center;
    gap: 12px;
  }

  .section-title::before { content: '>'; color: var(--purple); }
  .section-title::after {
    content: '';
    flex: 1;
    height: 1px;
    background: linear-gradient(90deg, var(--border), transparent);
  }

  /* ─── ABOUT CARD ─── */
  .about-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 12px;
  }

  .about-item {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 10px;
    padding: 14px 18px;
    display: flex;
    align-items: flex-start;
    gap: 12px;
    transition: border-color 0.3s, transform 0.3s;
  }

  .about-item:hover {
    border-color: rgba(0,212,255,0.4);
    transform: translateY(-2px);
  }

  .about-icon { font-size: 1.2rem; flex-shrink: 0; margin-top: 2px; }
  .about-text { font-size: 0.8rem; color: var(--text); line-height: 1.5; }
  .about-text strong { color: var(--cyan); display: block; font-size: 0.7rem; letter-spacing: 1px; margin-bottom: 2px; }

  /* ─── CODE BLOCK ─── */
  .code-block {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 12px;
    overflow: hidden;
  }

  .code-header {
    display: flex;
    align-items: center;
    gap: 8px;
    padding: 10px 16px;
    background: var(--surface2);
    border-bottom: 1px solid var(--border);
  }

  .dot { width: 10px; height: 10px; border-radius: 50%; }
  .dot-red { background: #ff5f57; }
  .dot-yellow { background: #ffbd2e; }
  .dot-green { background: #28c940; }
  .code-filename { font-size: 0.72rem; color: var(--muted); margin-left: 8px; }

  .code-body {
    padding: 20px;
    font-size: 0.82rem;
    line-height: 1.8;
  }

  .kw { color: #ff7b72; }
  .fn { color: #d2a8ff; }
  .str { color: #a5d6ff; }
  .prop { color: #79c0ff; }
  .comment { color: #8b949e; font-style: italic; }

  /* ─── TECH STACK ─── */
  .tech-category { margin-bottom: 20px; }
  .tech-category-title {
    font-size: 0.7rem;
    color: var(--muted);
    letter-spacing: 2px;
    text-transform: uppercase;
    margin-bottom: 10px;
  }

  .tech-pills {
    display: flex;
    flex-wrap: wrap;
    gap: 8px;
  }

  .pill {
    padding: 6px 14px;
    border-radius: 6px;
    font-size: 0.75rem;
    font-weight: 600;
    border: 1px solid;
    transition: transform 0.2s, box-shadow 0.2s;
    cursor: default;
  }

  .pill:hover {
    transform: translateY(-3px);
    box-shadow: 0 4px 20px rgba(0,212,255,0.2);
  }

  .pill-php { background: rgba(119,107,180,0.15); border-color: rgba(119,107,180,0.5); color: #9b8fdb; }
  .pill-laravel { background: rgba(255,45,32,0.1); border-color: rgba(255,45,32,0.4); color: #ff6b5b; }
  .pill-node { background: rgba(51,153,51,0.1); border-color: rgba(51,153,51,0.4); color: #5dba5d; }
  .pill-express { background: rgba(200,200,200,0.08); border-color: rgba(200,200,200,0.2); color: #ccc; }
  .pill-react { background: rgba(97,218,251,0.1); border-color: rgba(97,218,251,0.4); color: #61dafb; }
  .pill-js { background: rgba(247,223,30,0.1); border-color: rgba(247,223,30,0.3); color: #f7df1e; }
  .pill-html { background: rgba(227,79,38,0.1); border-color: rgba(227,79,38,0.4); color: #e34f26; }
  .pill-css { background: rgba(21,114,182,0.1); border-color: rgba(21,114,182,0.4); color: #4dabf7; }
  .pill-mysql { background: rgba(68,121,161,0.1); border-color: rgba(68,121,161,0.4); color: #5da0d0; }
  .pill-mongo { background: rgba(71,162,72,0.1); border-color: rgba(71,162,72,0.4); color: #4db461; }
  .pill-wp { background: rgba(33,117,179,0.1); border-color: rgba(33,117,179,0.4); color: #56a7d9; }
  .pill-git { background: rgba(240,80,50,0.1); border-color: rgba(240,80,50,0.4); color: #f0583a; }
  .pill-api { background: rgba(0,212,255,0.1); border-color: rgba(0,212,255,0.3); color: var(--cyan); }
  .pill-woo { background: rgba(150,88,138,0.1); border-color: rgba(150,88,138,0.4); color: #c278b0; }

  /* ─── PROJECTS TABLE ─── */
  .projects-grid {
    display: grid;
    gap: 10px;
  }

  .project-row {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    gap: 1px;
    background: var(--border);
    border-radius: 10px;
    overflow: hidden;
    border: 1px solid var(--border);
    transition: border-color 0.3s;
  }

  .project-row:hover { border-color: rgba(0,212,255,0.35); }

  .project-cell {
    background: var(--surface);
    padding: 14px 16px;
    font-size: 0.78rem;
  }

  .project-cell:first-child { color: var(--cyan); font-weight: 700; }
  .project-cell:nth-child(2) { color: var(--muted); }
  .project-cell:nth-child(3) { color: #a878ff; font-size: 0.72rem; }

  .table-header .project-cell {
    background: var(--surface2);
    color: var(--muted);
    font-size: 0.65rem;
    letter-spacing: 1.5px;
    text-transform: uppercase;
  }

  /* ─── STATS ─── */
  .stats-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 12px;
  }

  .stat-card {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 12px;
    padding: 20px;
    text-align: center;
    transition: transform 0.3s, border-color 0.3s;
  }

  .stat-card:hover {
    transform: translateY(-4px);
    border-color: rgba(0,212,255,0.4);
  }

  .stat-number {
    font-family: 'Syne', sans-serif;
    font-size: 2rem;
    font-weight: 800;
    background: linear-gradient(135deg, var(--cyan), var(--purple));
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
  }

  .stat-label { font-size: 0.7rem; color: var(--muted); letter-spacing: 1.5px; text-transform: uppercase; margin-top: 4px; }

  /* ─── CONNECT ─── */
  .connect-grid {
    display: flex;
    gap: 12px;
    flex-wrap: wrap;
    justify-content: center;
  }

  .connect-btn {
    padding: 12px 24px;
    border-radius: 8px;
    font-size: 0.78rem;
    font-weight: 700;
    letter-spacing: 1px;
    text-transform: uppercase;
    text-decoration: none;
    border: 1px solid;
    transition: all 0.3s;
    display: flex;
    align-items: center;
    gap: 8px;
  }

  .connect-btn:hover { transform: translateY(-3px); box-shadow: 0 8px 24px rgba(0,212,255,0.2); }

  .btn-linkedin { background: rgba(0,119,181,0.15); border-color: rgba(0,119,181,0.5); color: #5badd6; }
  .btn-github { background: rgba(255,255,255,0.05); border-color: rgba(255,255,255,0.2); color: #eee; }
  .btn-email { background: rgba(234,67,53,0.1); border-color: rgba(234,67,53,0.4); color: #f07060; }
  .btn-portfolio { background: rgba(0,212,255,0.1); border-color: rgba(0,212,255,0.35); color: var(--cyan); }

  /* ─── QUOTE ─── */
  .quote {
    text-align: center;
    margin-top: 40px;
    padding: 28px;
    background: linear-gradient(135deg, rgba(0,212,255,0.05), rgba(123,47,247,0.08));
    border: 1px solid var(--border);
    border-radius: 16px;
    font-size: 0.85rem;
    color: var(--muted);
    font-style: italic;
    position: relative;
  }

  .quote::before {
    content: '"';
    font-size: 4rem;
    color: var(--cyan);
    opacity: 0.2;
    position: absolute;
    top: -10px;
    left: 20px;
    font-family: 'Syne', sans-serif;
  }

  /* ─── FOOTER ─── */
  .footer-wave {
    margin-top: 50px;
    height: 80px;
    background: linear-gradient(135deg, rgba(123,47,247,0.2), rgba(0,212,255,0.2));
    border-radius: 40px 40px 0 0;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 0.7rem;
    color: var(--muted);
    letter-spacing: 2px;
    border: 1px solid var(--border);
    border-bottom: none;
  }

  /* Divider */
  .divider {
    height: 1px;
    background: linear-gradient(90deg, transparent, var(--border), transparent);
    margin: 8px 0;
  }

  /* Floating particles */
  .particles {
    position: fixed;
    inset: 0;
    pointer-events: none;
    overflow: hidden;
    z-index: 0;
  }

  .particle {
    position: absolute;
    width: 2px;
    height: 2px;
    background: var(--cyan);
    border-radius: 50%;
    animation: float linear infinite;
    opacity: 0;
  }

  @keyframes float {
    0% { transform: translateY(100vh) translateX(0); opacity: 0; }
    10% { opacity: 0.4; }
    90% { opacity: 0.4; }
    100% { transform: translateY(-100px) translateX(var(--dx)); opacity: 0; }
  }

  @media (max-width: 600px) {
    .about-grid { grid-template-columns: 1fr; }
    .stats-grid { grid-template-columns: 1fr 1fr; }
    .project-row { grid-template-columns: 1fr; }
    .name { font-size: 2rem; }
  }
</style>
</head>
<body>

<!-- Floating particles -->
<div class="particles" id="particles"></div>

<div class="container">

  <!-- ─── HEADER ─── -->
  <div class="header">
    <div class="header-wave">
      <div class="name">Sanjan Kumar</div>
      <div class="role">Senior Full Stack Developer</div>
    </div>

    <div class="typing-container">
      <span class="typing-text">PHP • WordPress • Laravel • MERN • REST API • SaaS</span>
    </div>

    <div class="badges" style="margin-top:16px;">
      <span class="badge badge-cyan">⚡ 5+ Years XP</span>
      <span class="badge badge-purple">🔌 API Specialist</span>
      <span class="badge badge-green">✅ Open to Collaborate</span>
    </div>
  </div>

  <div class="divider"></div>

  <!-- ─── ABOUT ─── -->
  <div class="section-title">whoami</div>

  <div class="about-grid">
    <div class="about-item">
      <div class="about-icon">🔥</div>
      <div class="about-text"><strong>WordPress Expert</strong>Custom plugin dev, WooCommerce, API integrations at scale</div>
    </div>
    <div class="about-item">
      <div class="about-icon">⚙️</div>
      <div class="about-text"><strong>Laravel Architect</strong>Enterprise apps, clean architecture, service layers</div>
    </div>
    <div class="about-item">
      <div class="about-icon">🌐</div>
      <div class="about-text"><strong>MERN Stack Dev</strong>MongoDB · Express · React · Node.js full-cycle builds</div>
    </div>
    <div class="about-item">
      <div class="about-icon">🔌</div>
      <div class="about-text"><strong>API Specialist</strong>REST API design, third-party integrations & automation</div>
    </div>
    <div class="about-item">
      <div class="about-icon">🛠️</div>
      <div class="about-text"><strong>Systems Builder</strong>CRM, Booking Systems, Scrapers & Automation Tools</div>
    </div>
    <div class="about-item">
      <div class="about-icon">📈</div>
      <div class="about-text"><strong>Performance First</strong>Scalable, clean, maintainable code — always</div>
    </div>
  </div>

  <!-- ─── CURRENT FOCUS ─── -->
  <div class="section-title">current --focus</div>

  <div class="code-block">
    <div class="code-header">
      <div class="dot dot-red"></div>
      <div class="dot dot-yellow"></div>
      <div class="dot dot-green"></div>
      <span class="code-filename">mission.js</span>
    </div>
    <div class="code-body">
      <span class="kw">const</span> <span class="fn">currentMission</span> = {<br/>
      &nbsp;&nbsp;<span class="prop">building</span>&nbsp;&nbsp;: <span class="str">"Scalable SaaS Applications"</span>,<br/>
      &nbsp;&nbsp;<span class="prop">mastering</span> : <span class="str">"Advanced WordPress Architecture"</span>,<br/>
      &nbsp;&nbsp;<span class="prop">exploring</span> : <span class="str">"Microservices & API Optimization"</span>,<br/>
      &nbsp;&nbsp;<span class="prop">goal</span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;: <span class="str">"Craft solutions that last, scale, and impress."</span><br/>
      };<br/><br/>
      <span class="comment">// 5+ years of building. Still shipping. Still scaling.</span>
    </div>
  </div>

  <!-- ─── TECH STACK ─── -->
  <div class="section-title">tech --stack</div>

  <div class="tech-category">
    <div class="tech-category-title">⚙ Backend</div>
    <div class="tech-pills">
      <span class="pill pill-php">PHP</span>
      <span class="pill pill-laravel">Laravel</span>
      <span class="pill pill-node">Node.js</span>
      <span class="pill pill-express">Express.js</span>
    </div>
  </div>

  <div class="tech-category">
    <div class="tech-category-title">🌐 Frontend</div>
    <div class="tech-pills">
      <span class="pill pill-react">React.js</span>
      <span class="pill pill-js">JavaScript ES6+</span>
      <span class="pill pill-html">HTML5</span>
      <span class="pill pill-css">CSS3</span>
    </div>
  </div>

  <div class="tech-category">
    <div class="tech-category-title">🗄 Database</div>
    <div class="tech-pills">
      <span class="pill pill-mysql">MySQL</span>
      <span class="pill pill-mongo">MongoDB</span>
    </div>
  </div>

  <div class="tech-category">
    <div class="tech-category-title">🛠 CMS & Tools</div>
    <div class="tech-pills">
      <span class="pill pill-wp">WordPress</span>
      <span class="pill pill-woo">WooCommerce</span>
      <span class="pill pill-git">Git / GitHub</span>
      <span class="pill pill-api">REST APIs</span>
    </div>
  </div>

  <!-- ─── PROJECTS ─── -->
  <div class="section-title">projects --featured</div>

  <div class="projects-grid">
    <div class="project-row table-header">
      <div class="project-cell">Project Type</div>
      <div class="project-cell">Tech Used</div>
      <div class="project-cell">Outcome</div>
    </div>
    <div class="project-row">
      <div class="project-cell">⚡ Custom WordPress Plugins</div>
      <div class="project-cell">PHP · WP API · MySQL</div>
      <div class="project-cell">Tailored features for 20+ clients</div>
    </div>
    <div class="project-row">
      <div class="project-cell">🏨 Booking & Villa Mgmt</div>
      <div class="project-cell">Laravel · React · MySQL</div>
      <div class="project-cell">End-to-end reservation automation</div>
    </div>
    <div class="project-row">
      <div class="project-cell">📊 CRM Systems</div>
      <div class="project-cell">MERN Stack · REST API</div>
      <div class="project-cell">Streamlined business workflows</div>
    </div>
    <div class="project-row">
      <div class="project-cell">🔌 API Applications</div>
      <div class="project-cell">Node.js · Express · MongoDB</div>
      <div class="project-cell">High-throughput integrations</div>
    </div>
    <div class="project-row">
      <div class="project-cell">🕷️ Web Scraping Tools</div>
      <div class="project-cell">PHP · Puppeteer · Node.js</div>
      <div class="project-cell">Automated data pipelines</div>
    </div>
    <div class="project-row">
      <div class="project-cell">🚀 Full-Stack MERN Apps</div>
      <div class="project-cell">MongoDB · Express · React</div>
      <div class="project-cell">Scalable SPA architecture</div>
    </div>
  </div>

  <!-- ─── STATS ─── -->
  <div class="section-title">git stats --summary</div>

  <div class="stats-grid">
    <div class="stat-card">
      <div class="stat-number">5+</div>
      <div class="stat-label">Years Experience</div>
    </div>
    <div class="stat-card">
      <div class="stat-number">50+</div>
      <div class="stat-label">Projects Shipped</div>
    </div>
    <div class="stat-card">
      <div class="stat-number">20+</div>
      <div class="stat-label">Happy Clients</div>
    </div>
  </div>

  <!-- ─── CONNECT ─── -->
  <div class="section-title">connect --me</div>

  <div class="connect-grid">
    <a href="#" class="connect-btn btn-linkedin">🔗 LinkedIn</a>
    <a href="#" class="connect-btn btn-github">🐙 GitHub</a>
    <a href="#" class="connect-btn btn-email">📧 Email</a>
    <a href="#" class="connect-btn btn-portfolio">🌐 Portfolio</a>
  </div>

  <!-- ─── QUOTE ─── -->
  <div class="quote">
    I don't just write code — I architect experiences that scale.
  </div>

  <!-- ─── FOOTER ─── -->
  <div class="footer-wave">
    ✦ &nbsp; SANJAN KUMAR &nbsp; · &nbsp; FULL STACK DEVELOPER &nbsp; ✦
  </div>

</div>

<script>
  // Generate floating particles
  const container = document.getElementById('particles');
  for (let i = 0; i < 25; i++) {
    const p = document.createElement('div');
    p.className = 'particle';
    p.style.cssText = `
      left: ${Math.random() * 100}%;
      animation-duration: ${6 + Math.random() * 10}s;
      animation-delay: ${Math.random() * 8}s;
      --dx: ${(Math.random() - 0.5) * 100}px;
      opacity: 0;
      ${Math.random() > 0.5 ? 'background: #7b2ff7;' : ''}
    `;
    container.appendChild(p);
  }
</script>

</body>
</html><div className="flex items-center justify-between px-6 py-5 border-b border-gray-200 dark:border-gray-800">

  {/* Logo Area */}
  {!collapsed ? (
    <h2 className="text-lg font-semibold tracking-wide text-gray-800 dark:text-white">
      Gigsoft Admin
    </h2>
  ) : (
    <div className="w-10 h-10 flex items-center justify-center rounded-xl bg-black dark:bg-white shadow-md">
      <LayoutGrid
        size={20}
        strokeWidth={1.8}
        className="text-white dark:text-black"
      />
    </div>
  )}

  {/* Collapse Toggle */}
  <button
    onClick={() => setCollapsed(!collapsed)}
    className="p-2 rounded-lg 
    text-gray-700 dark:text-gray-300
    hover:bg-gray-200 dark:hover:bg-gray-800 
    transition-colors duration-200"
  >
    {collapsed ? (
      <ChevronRight
        size={18}
        strokeWidth={2}
        className="text-current"
      />
    ) : (
      <ChevronLeft
        size={18}
        strokeWidth={2}
        className="text-current"
      />
    )}
  </button>

</div>
  // Generate floating particles
  const container = document.getElementById('particles');
  for (let i = 0; i < 25; i++) {
    const p = document.createElement('div');
    p.className = 'particle';
    p.style.cssText = `
      left: ${Math.random() * 100}%;
      animation-duration: ${6 + Math.random() * 10}s;
      animation-delay: ${Math.random() * 8}s;
      --dx: ${(Math.random() - 0.5) * 100}px;
      opacity: 0;
      ${Math.random() > 0.5 ? 'background: #7b2ff7;' : ''}
    `;
    container.appendChild(p);
  }
</script>

</body>
</html>
    --purple: #7b2ff7;
    --green: #39d353;
    --text: #c9d1d9;
    --muted: #8b949e;
    --border: rgba(0,212,255,0.15);
  }

  body {
    background: var(--bg);
    color: var(--text);
    font-family: 'JetBrains Mono', monospace;
    line-height: 1.6;
    overflow-x: hidden;
  }

  /* ANIMATED GRID BACKGROUND */
  body::before {
    content: '';
    position: fixed;
    inset: 0;
    background-image:
      linear-gradient(rgba(0,212,255,0.03) 1px, transparent 1px),
      linear-gradient(90deg, rgba(0,212,255,0.03) 1px, transparent 1px);
    background-size: 40px 40px;
    pointer-events: none;
    z-index: 0;
  }

  .container {
    max-width: 860px;
    margin: 0 auto;
    padding: 0 24px 60px;
    position: relative;
    z-index: 1;
  }

  /* ─── HEADER ─── */
  .header {
    position: relative;
    text-align: center;
    padding: 0 0 40px;
    overflow: hidden;
  }

  .header-wave {
    width: 100%;
    height: 180px;
    background: linear-gradient(135deg, #0d1117 0%, #0a1628 40%, #0d1528 60%, #0d1117 100%);
    position: relative;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    border-radius: 0 0 40px 40px;
    margin-bottom: 28px;
    border: 1px solid var(--border);
    border-top: none;
  }

  .header-wave::before {
    content: '';
    position: absolute;
    inset: 0;
    background: linear-gradient(135deg, rgba(0,212,255,0.08) 0%, rgba(123,47,247,0.12) 100%);
    border-radius: inherit;
  }

  /* Animated scan line */
  .header-wave::after {
    content: '';
    position: absolute;
    left: 0; right: 0;
    height: 2px;
    background: linear-gradient(90deg, transparent, var(--cyan), transparent);
    animation: scanLine 3s ease-in-out infinite;
    opacity: 0.6;
  }

  @keyframes scanLine {
    0% { top: 0; opacity: 0; }
    10% { opacity: 0.6; }
    90% { opacity: 0.6; }
    100% { top: 100%; opacity: 0; }
  }

  .name {
    font-family: 'Syne', sans-serif;
    font-size: 2.8rem;
    font-weight: 800;
    background: linear-gradient(135deg, #ffffff 0%, var(--cyan) 50%, var(--purple) 100%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
    position: relative;
    z-index: 1;
    animation: fadeSlideDown 0.8s ease both;
  }

  .role {
    font-size: 0.85rem;
    color: var(--cyan);
    letter-spacing: 3px;
    text-transform: uppercase;
    position: relative;
    z-index: 1;
    animation: fadeSlideDown 0.8s 0.2s ease both;
    opacity: 0;
    animation-fill-mode: forwards;
  }

  @keyframes fadeSlideDown {
    from { opacity: 0; transform: translateY(-16px); }
    to { opacity: 1; transform: translateY(0); }
  }

  /* Typing animation */
  .typing-container {
    display: flex;
    justify-content: center;
    gap: 8px;
    flex-wrap: wrap;
  }

  .typing-text {
    color: var(--cyan);
    font-size: 0.9rem;
    overflow: hidden;
    white-space: nowrap;
    border-right: 2px solid var(--cyan);
    animation: typing 3.5s steps(40) infinite, blink 0.75s step-end infinite;
    max-width: 500px;
    text-align: left;
  }

  @keyframes typing {
    0%,100% { width: 0 }
    30%,70% { width: 100% }
  }
  @keyframes blink {
    50% { border-color: transparent }
  }

  /* ─── BADGES ─── */
  .badges {
    display: flex;
    justify-content: center;
    gap: 10px;
    flex-wrap: wrap;
    margin: 20px 0;
  }

  .badge {
    padding: 6px 16px;
    border-radius: 20px;
    font-size: 0.72rem;
    font-weight: 600;
    letter-spacing: 1px;
    text-transform: uppercase;
    animation: fadeIn 1s ease both;
  }

  .badge-cyan { background: rgba(0,212,255,0.12); border: 1px solid rgba(0,212,255,0.4); color: var(--cyan); }
  .badge-purple { background: rgba(123,47,247,0.12); border: 1px solid rgba(123,47,247,0.4); color: #a878ff; }
  .badge-green { background: rgba(57,211,83,0.12); border: 1px solid rgba(57,211,83,0.4); color: var(--green); }

  @keyframes fadeIn {
    from { opacity: 0; transform: scale(0.9); }
    to { opacity: 1; transform: scale(1); }
  }

  /* ─── SECTION HEADERS ─── */
  .section-title {
    font-size: 0.8rem;
    color: var(--cyan);
    letter-spacing: 2px;
    text-transform: uppercase;
    margin: 48px 0 20px;
    display: flex;
    align-items: center;
    gap: 12px;
  }

  .section-title::before { content: '>'; color: var(--purple); }
  .section-title::after {
    content: '';
    flex: 1;
    height: 1px;
    background: linear-gradient(90deg, var(--border), transparent);
  }

  /* ─── ABOUT CARD ─── */
  .about-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 12px;
  }

  .about-item {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 10px;
    padding: 14px 18px;
    display: flex;
    align-items: flex-start;
    gap: 12px;
    transition: border-color 0.3s, transform 0.3s;
  }

  .about-item:hover {
    border-color: rgba(0,212,255,0.4);
    transform: translateY(-2px);
  }

  .about-icon { font-size: 1.2rem; flex-shrink: 0; margin-top: 2px; }
  .about-text { font-size: 0.8rem; color: var(--text); line-height: 1.5; }
  .about-text strong { color: var(--cyan); display: block; font-size: 0.7rem; letter-spacing: 1px; margin-bottom: 2px; }

  /* ─── CODE BLOCK ─── */
  .code-block {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 12px;
    overflow: hidden;
  }

  .code-header {
    display: flex;
    align-items: center;
    gap: 8px;
    padding: 10px 16px;
    background: var(--surface2);
    border-bottom: 1px solid var(--border);
  }

  .dot { width: 10px; height: 10px; border-radius: 50%; }
  .dot-red { background: #ff5f57; }
  .dot-yellow { background: #ffbd2e; }
  .dot-green { background: #28c940; }
  .code-filename { font-size: 0.72rem; color: var(--muted); margin-left: 8px; }

  .code-body {
    padding: 20px;
    font-size: 0.82rem;
    line-height: 1.8;
  }

  .kw { color: #ff7b72; }
  .fn { color: #d2a8ff; }
  .str { color: #a5d6ff; }
  .prop { color: #79c0ff; }
  .comment { color: #8b949e; font-style: italic; }

  /* ─── TECH STACK ─── */
  .tech-category { margin-bottom: 20px; }
  .tech-category-title {
    font-size: 0.7rem;
    color: var(--muted);
    letter-spacing: 2px;
    text-transform: uppercase;
    margin-bottom: 10px;
  }

  .tech-pills {
    display: flex;
    flex-wrap: wrap;
    gap: 8px;
  }

  .pill {
    padding: 6px 14px;
    border-radius: 6px;
    font-size: 0.75rem;
    font-weight: 600;
    border: 1px solid;
    transition: transform 0.2s, box-shadow 0.2s;
    cursor: default;
  }

  .pill:hover {
    transform: translateY(-3px);
    box-shadow: 0 4px 20px rgba(0,212,255,0.2);
  }

  .pill-php { background: rgba(119,107,180,0.15); border-color: rgba(119,107,180,0.5); color: #9b8fdb; }
  .pill-laravel { background: rgba(255,45,32,0.1); border-color: rgba(255,45,32,0.4); color: #ff6b5b; }
  .pill-node { background: rgba(51,153,51,0.1); border-color: rgba(51,153,51,0.4); color: #5dba5d; }
  .pill-express { background: rgba(200,200,200,0.08); border-color: rgba(200,200,200,0.2); color: #ccc; }
  .pill-react { background: rgba(97,218,251,0.1); border-color: rgba(97,218,251,0.4); color: #61dafb; }
  .pill-js { background: rgba(247,223,30,0.1); border-color: rgba(247,223,30,0.3); color: #f7df1e; }
  .pill-html { background: rgba(227,79,38,0.1); border-color: rgba(227,79,38,0.4); color: #e34f26; }
  .pill-css { background: rgba(21,114,182,0.1); border-color: rgba(21,114,182,0.4); color: #4dabf7; }
  .pill-mysql { background: rgba(68,121,161,0.1); border-color: rgba(68,121,161,0.4); color: #5da0d0; }
  .pill-mongo { background: rgba(71,162,72,0.1); border-color: rgba(71,162,72,0.4); color: #4db461; }
  .pill-wp { background: rgba(33,117,179,0.1); border-color: rgba(33,117,179,0.4); color: #56a7d9; }
  .pill-git { background: rgba(240,80,50,0.1); border-color: rgba(240,80,50,0.4); color: #f0583a; }
  .pill-api { background: rgba(0,212,255,0.1); border-color: rgba(0,212,255,0.3); color: var(--cyan); }
  .pill-woo { background: rgba(150,88,138,0.1); border-color: rgba(150,88,138,0.4); color: #c278b0; }

  /* ─── PROJECTS TABLE ─── */
  .projects-grid {
    display: grid;
    gap: 10px;
  }

  .project-row {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    gap: 1px;
    background: var(--border);
    border-radius: 10px;
    overflow: hidden;
    border: 1px solid var(--border);
    transition: border-color 0.3s;
  }

  .project-row:hover { border-color: rgba(0,212,255,0.35); }

  .project-cell {
    background: var(--surface);
    padding: 14px 16px;
    font-size: 0.78rem;
  }

  .project-cell:first-child { color: var(--cyan); font-weight: 700; }
  .project-cell:nth-child(2) { color: var(--muted); }
  .project-cell:nth-child(3) { color: #a878ff; font-size: 0.72rem; }

  .table-header .project-cell {
    background: var(--surface2);
    color: var(--muted);
    font-size: 0.65rem;
    letter-spacing: 1.5px;
    text-transform: uppercase;
  }

  /* ─── STATS ─── */
  .stats-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 12px;
  }

  .stat-card {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 12px;
    padding: 20px;
    text-align: center;
    transition: transform 0.3s, border-color 0.3s;
  }

  .stat-card:hover {
    transform: translateY(-4px);
    border-color: rgba(0,212,255,0.4);
  }

  .stat-number {
    font-family: 'Syne', sans-serif;
    font-size: 2rem;
    font-weight: 800;
    background: linear-gradient(135deg, var(--cyan), var(--purple));
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
  }

  .stat-label { font-size: 0.7rem; color: var(--muted); letter-spacing: 1.5px; text-transform: uppercase; margin-top: 4px; }

  /* ─── CONNECT ─── */
  .connect-grid {
    display: flex;
    gap: 12px;
    flex-wrap: wrap;
    justify-content: center;
  }

  .connect-btn {
    padding: 12px 24px;
    border-radius: 8px;
    font-size: 0.78rem;
    font-weight: 700;
    letter-spacing: 1px;
    text-transform: uppercase;
    text-decoration: none;
    border: 1px solid;
    transition: all 0.3s;
    display: flex;
    align-items: center;
    gap: 8px;
  }

  .connect-btn:hover { transform: translateY(-3px); box-shadow: 0 8px 24px rgba(0,212,255,0.2); }

  .btn-linkedin { background: rgba(0,119,181,0.15); border-color: rgba(0,119,181,0.5); color: #5badd6; }
  .btn-github { background: rgba(255,255,255,0.05); border-color: rgba(255,255,255,0.2); color: #eee; }
  .btn-email { background: rgba(234,67,53,0.1); border-color: rgba(234,67,53,0.4); color: #f07060; }
  .btn-portfolio { background: rgba(0,212,255,0.1); border-color: rgba(0,212,255,0.35); color: var(--cyan); }

  /* ─── QUOTE ─── */
  .quote {
    text-align: center;
    margin-top: 40px;
    padding: 28px;
    background: linear-gradient(135deg, rgba(0,212,255,0.05), rgba(123,47,247,0.08));
    border: 1px solid var(--border);
    border-radius: 16px;
    font-size: 0.85rem;
    color: var(--muted);
    font-style: italic;
    position: relative;
  }

  .quote::before {
    content: '"';
    font-size: 4rem;
    color: var(--cyan);
    opacity: 0.2;
    position: absolute;
    top: -10px;
    left: 20px;
    font-family: 'Syne', sans-serif;
  }

  /* ─── FOOTER ─── */
  .footer-wave {
    margin-top: 50px;
    height: 80px;
    background: linear-gradient(135deg, rgba(123,47,247,0.2), rgba(0,212,255,0.2));
    border-radius: 40px 40px 0 0;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 0.7rem;
    color: var(--muted);
    letter-spacing: 2px;
    border: 1px solid var(--border);
    border-bottom: none;
  }

  /* Divider */
  .divider {
    height: 1px;
    background: linear-gradient(90deg, transparent, var(--border), transparent);
    margin: 8px 0;
  }

  /* Floating particles */
  .particles {
    position: fixed;
    inset: 0;
    pointer-events: none;
    overflow: hidden;
    z-index: 0;
  }

  .particle {
    position: absolute;
    width: 2px;
    height: 2px;
    background: var(--cyan);
    border-radius: 50%;
    animation: float linear infinite;
    opacity: 0;
  }

  @keyframes float {
    0% { transform: translateY(100vh) translateX(0); opacity: 0; }
    10% { opacity: 0.4; }
    90% { opacity: 0.4; }
    100% { transform: translateY(-100px) translateX(var(--dx)); opacity: 0; }
  }

  @media (max-width: 600px) {
    .about-grid { grid-template-columns: 1fr; }
    .stats-grid { grid-template-columns: 1fr 1fr; }
    .project-row { grid-template-columns: 1fr; }
    .name { font-size: 2rem; }
  }
</style>
</head>
<body>

<!-- Floating particles -->
<div class="particles" id="particles"></div>

<div class="container">

  <!-- ─── HEADER ─── -->
  <div class="header">
    <div class="header-wave">
      <div class="name">Sanjan Kumar</div>
      <div class="role">Senior Full Stack Developer</div>
    </div>

    <div class="typing-container">
      <span class="typing-text">PHP • WordPress • Laravel • MERN • REST API • SaaS</span>
    </div>

    <div class="badges" style="margin-top:16px;">
      <span class="badge badge-cyan">⚡ 5+ Years XP</span>
      <span class="badge badge-purple">🔌 API Specialist</span>
      <span class="badge badge-green">✅ Open to Collaborate</span>
    </div>
  </div>

  <div class="divider"></div>

  <!-- ─── ABOUT ─── -->
  <div class="section-title">whoami</div>

  <div class="about-grid">
    <div class="about-item">
      <div class="about-icon">🔥</div>
      <div class="about-text"><strong>WordPress Expert</strong>Custom plugin dev, WooCommerce, API integrations at scale</div>
    </div>
    <div class="about-item">
      <div class="about-icon">⚙️</div>
      <div class="about-text"><strong>Laravel Architect</strong>Enterprise apps, clean architecture, service layers</div>
    </div>
    <div class="about-item">
      <div class="about-icon">🌐</div>
      <div class="about-text"><strong>MERN Stack Dev</strong>MongoDB · Express · React · Node.js full-cycle builds</div>
    </div>
    <div class="about-item">
      <div class="about-icon">🔌</div>
      <div class="about-text"><strong>API Specialist</strong>REST API design, third-party integrations & automation</div>
    </div>
    <div class="about-item">
      <div class="about-icon">🛠️</div>
      <div class="about-text"><strong>Systems Builder</strong>CRM, Booking Systems, Scrapers & Automation Tools</div>
    </div>
    <div class="about-item">
      <div class="about-icon">📈</div>
      <div class="about-text"><strong>Performance First</strong>Scalable, clean, maintainable code — always</div>
    </div>
  </div>

  <!-- ─── CURRENT FOCUS ─── -->
  <div class="section-title">current --focus</div>

  <div class="code-block">
    <div class="code-header">
      <div class="dot dot-red"></div>
      <div class="dot dot-yellow"></div>
      <div class="dot dot-green"></div>
      <span class="code-filename">mission.js</span>
    </div>
    <div class="code-body">
      <span class="kw">const</span> <span class="fn">currentMission</span> = {<br/>
      &nbsp;&nbsp;<span class="prop">building</span>&nbsp;&nbsp;: <span class="str">"Scalable SaaS Applications"</span>,<br/>
      &nbsp;&nbsp;<span class="prop">mastering</span> : <span class="str">"Advanced WordPress Architecture"</span>,<br/>
      &nbsp;&nbsp;<span class="prop">exploring</span> : <span class="str">"Microservices & API Optimization"</span>,<br/>
      &nbsp;&nbsp;<span class="prop">goal</span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;: <span class="str">"Craft solutions that last, scale, and impress."</span><br/>
      };<br/><br/>
      <span class="comment">// 5+ years of building. Still shipping. Still scaling.</span>
    </div>
  </div>

  <!-- ─── TECH STACK ─── -->
  <div class="section-title">tech --stack</div>

  <div class="tech-category">
    <div class="tech-category-title">⚙ Backend</div>
    <div class="tech-pills">
      <span class="pill pill-php">PHP</span>
      <span class="pill pill-laravel">Laravel</span>
      <span class="pill pill-node">Node.js</span>
      <span class="pill pill-express">Express.js</span>
    </div>
  </div>

  <div class="tech-category">
    <div class="tech-category-title">🌐 Frontend</div>
    <div class="tech-pills">
      <span class="pill pill-react">React.js</span>
      <span class="pill pill-js">JavaScript ES6+</span>
      <span class="pill pill-html">HTML5</span>
      <span class="pill pill-css">CSS3</span>
    </div>
  </div>

  <div class="tech-category">
    <div class="tech-category-title">🗄 Database</div>
    <div class="tech-pills">
      <span class="pill pill-mysql">MySQL</span>
      <span class="pill pill-mongo">MongoDB</span>
    </div>
  </div>

  <div class="tech-category">
    <div class="tech-category-title">🛠 CMS & Tools</div>
    <div class="tech-pills">
      <span class="pill pill-wp">WordPress</span>
      <span class="pill pill-woo">WooCommerce</span>
      <span class="pill pill-git">Git / GitHub</span>
      <span class="pill pill-api">REST APIs</span>
    </div>
  </div>

  <!-- ─── PROJECTS ─── -->
  <div class="section-title">projects --featured</div>

  <div class="projects-grid">
    <div class="project-row table-header">
      <div class="project-cell">Project Type</div>
      <div class="project-cell">Tech Used</div>
      <div class="project-cell">Outcome</div>
    </div>
    <div class="project-row">
      <div class="project-cell">⚡ Custom WordPress Plugins</div>
      <div class="project-cell">PHP · WP API · MySQL</div>
      <div class="project-cell">Tailored features for 20+ clients</div>
    </div>
    <div class="project-row">
      <div class="project-cell">🏨 Booking & Villa Mgmt</div>
      <div class="project-cell">Laravel · React · MySQL</div>
      <div class="project-cell">End-to-end reservation automation</div>
    </div>
    <div class="project-row">
      <div class="project-cell">📊 CRM Systems</div>
      <div class="project-cell">MERN Stack · REST API</div>
      <div class="project-cell">Streamlined business workflows</div>
    </div>
    <div class="project-row">
      <div class="project-cell">🔌 API Applications</div>
      <div class="project-cell">Node.js · Express · MongoDB</div>
      <div class="project-cell">High-throughput integrations</div>
    </div>
    <div class="project-row">
      <div class="project-cell">🕷️ Web Scraping Tools</div>
      <div class="project-cell">PHP · Puppeteer · Node.js</div>
      <div class="project-cell">Automated data pipelines</div>
    </div>
    <div class="project-row">
      <div class="project-cell">🚀 Full-Stack MERN Apps</div>
      <div class="project-cell">MongoDB · Express · React</div>
      <div class="project-cell">Scalable SPA architecture</div>
    </div>
  </div>

  <!-- ─── STATS ─── -->
  <div class="section-title">git stats --summary</div>

  <div class="stats-grid">
    <div class="stat-card">
      <div class="stat-number">5+</div>
      <div class="stat-label">Years Experience</div>
    </div>
    <div class="stat-card">
      <div class="stat-number">50+</div>
      <div class="stat-label">Projects Shipped</div>
    </div>
    <div class="stat-card">
      <div class="stat-number">20+</div>
      <div class="stat-label">Happy Clients</div>
    </div>
  </div>

  <!-- ─── CONNECT ─── -->
  <div class="section-title">connect --me</div>

  <div class="connect-grid">
    <a href="#" class="connect-btn btn-linkedin">🔗 LinkedIn</a>
    <a href="#" class="connect-btn btn-github">🐙 GitHub</a>
    <a href="#" class="connect-btn btn-email">📧 Email</a>
    <a href="#" class="connect-btn btn-portfolio">🌐 Portfolio</a>
  </div>

  <!-- ─── QUOTE ─── -->
  <div class="quote">
    I don't just write code — I architect experiences that scale.
  </div>

  <!-- ─── FOOTER ─── -->
  <div class="footer-wave">
    ✦ &nbsp; SANJAN KUMAR &nbsp; · &nbsp; FULL STACK DEVELOPER &nbsp; ✦
  </div>

</div>

<script>
  // Generate floating particles
  const container = document.getElementById('particles');
  for (let i = 0; i < 25; i++) {
    const p = document.createElement('div');
    p.className = 'particle';
    p.style.cssText = `
      left: ${Math.random() * 100}%;
      animation-duration: ${6 + Math.random() * 10}s;
      animation-delay: ${Math.random() * 8}s;
      --dx: ${(Math.random() - 0.5) * 100}px;
      opacity: 0;
      ${Math.random() > 0.5 ? 'background: #7b2ff7;' : ''}
    `;
    container.appendChild(p);
  }
</script>

</body>
</html>
