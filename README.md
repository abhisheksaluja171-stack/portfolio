[abhishek_saluja_portfolio_updated.html](https://github.com/user-attachments/files/26573562/abhishek_saluja_portfolio_updated.html)
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Abhishek Saluja | Finance & MIS Analyst</title>
<link href="https://fonts.googleapis.com/css2?family=DM+Serif+Display:ital@0;1&family=DM+Sans:wght@300;400;500;600&display=swap" rel="stylesheet">
<style>
  :root {
    --bg: #f7f6f3;
    --surface: #ffffff;
    --navy: #0f1c2e;
    --slate: #2d3f55;
    --accent: #1a56a0;
    --accent-light: #e8f0fb;
    --muted: #7a8a9b;
    --border: #e2e5eb;
    --shadow: 0 2px 16px rgba(15,28,46,0.07);
    --shadow-md: 0 6px 28px rgba(15,28,46,0.11);
    --radius: 10px;
  }
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
  html { scroll-behavior: smooth; font-size: 16px; }
  body { font-family: 'DM Sans', sans-serif; background: var(--bg); color: var(--navy); line-height: 1.7; }

  /* NAV */
  nav {
    position: fixed; top: 0; left: 0; right: 0; z-index: 100;
    background: rgba(247,246,243,0.92); backdrop-filter: blur(12px);
    border-bottom: 1px solid var(--border);
    display: flex; align-items: center; justify-content: space-between;
    padding: 0 5%;
    height: 62px;
  }
  .nav-brand { font-family: 'DM Serif Display', serif; font-size: 1.15rem; color: var(--navy); text-decoration: none; letter-spacing: -0.01em; }
  .nav-links { display: flex; gap: 32px; list-style: none; }
  .nav-links a { color: var(--slate); text-decoration: none; font-size: 0.88rem; font-weight: 500; letter-spacing: 0.02em; transition: color 0.2s; }
  .nav-links a:hover { color: var(--accent); }
  .hamburger { display: none; flex-direction: column; gap: 5px; cursor: pointer; background: none; border: none; }
  .hamburger span { display: block; width: 22px; height: 2px; background: var(--navy); border-radius: 2px; transition: 0.3s; }
  .mobile-menu { display: none; position: fixed; top: 62px; left: 0; right: 0; background: var(--surface); border-bottom: 1px solid var(--border); padding: 20px 5%; z-index: 99; }
  .mobile-menu.open { display: block; }
  .mobile-menu a { display: block; padding: 12px 0; color: var(--slate); text-decoration: none; font-weight: 500; border-bottom: 1px solid var(--border); }
  .mobile-menu a:last-child { border-bottom: none; }

  /* LAYOUT */
  .section { padding: 80px 5%; max-width: 1080px; margin: 0 auto; }
  .section-label { font-size: 0.75rem; font-weight: 600; letter-spacing: 0.12em; text-transform: uppercase; color: var(--accent); margin-bottom: 8px; }
  .section-title { font-family: 'DM Serif Display', serif; font-size: 2rem; color: var(--navy); margin-bottom: 40px; line-height: 1.2; }
  .divider { width: 48px; height: 3px; background: var(--accent); margin-bottom: 40px; border-radius: 2px; }

  /* HERO */
  #hero {
    min-height: 100vh; display: flex; align-items: center;
    padding-top: 62px;
    background: var(--surface);
    border-bottom: 1px solid var(--border);
    position: relative;
    overflow: hidden;
  }
  #hero::before {
    content: '';
    position: absolute; top: 0; right: 0;
    width: 42%; height: 100%;
    background: linear-gradient(135deg, #e8f0fb 0%, #f0f4fb 100%);
    clip-path: polygon(12% 0, 100% 0, 100% 100%, 0% 100%);
  }
  .hero-inner {
    max-width: 1080px; margin: 0 auto; padding: 0 5%;
    width: 100%; position: relative; z-index: 1;
  }
  .hero-tag {
    display: inline-block;
    background: var(--accent-light); color: var(--accent);
    font-size: 0.75rem; font-weight: 600; letter-spacing: 0.1em;
    text-transform: uppercase; padding: 5px 14px; border-radius: 100px;
    margin-bottom: 24px;
  }
  .hero-name {
    font-family: 'DM Serif Display', serif;
    font-size: clamp(2.8rem, 6vw, 4.2rem);
    color: var(--navy); line-height: 1.05; margin-bottom: 16px;
    letter-spacing: -0.02em;
  }
  .hero-title {
    font-size: 1rem; font-weight: 500; color: var(--accent);
    letter-spacing: 0.04em; margin-bottom: 20px;
  }
  .hero-divider { width: 40px; height: 3px; background: var(--accent); margin: 24px 0; border-radius: 2px; }
  .hero-tagline {
    font-size: 1.05rem; color: var(--slate); max-width: 520px;
    line-height: 1.75; margin-bottom: 36px; font-weight: 300;
  }
  .hero-cta { display: flex; gap: 16px; flex-wrap: wrap; }
  .btn-primary {
    background: var(--navy); color: #fff;
    padding: 13px 30px; border-radius: var(--radius);
    text-decoration: none; font-weight: 600; font-size: 0.9rem;
    letter-spacing: 0.02em; transition: background 0.2s, transform 0.15s;
    border: 2px solid var(--navy);
  }
  .btn-primary:hover { background: var(--accent); border-color: var(--accent); transform: translateY(-1px); }
  .btn-secondary {
    background: transparent; color: var(--navy);
    padding: 13px 30px; border-radius: var(--radius);
    text-decoration: none; font-weight: 600; font-size: 0.9rem;
    letter-spacing: 0.02em; transition: all 0.2s;
    border: 2px solid var(--navy);
  }
  .btn-secondary:hover { background: var(--navy); color: #fff; transform: translateY(-1px); }
  .hero-stats {
    display: flex; gap: 40px; margin-top: 52px;
    padding-top: 40px; border-top: 1px solid var(--border);
    flex-wrap: wrap;
  }
  .stat-num { font-family: 'DM Serif Display', serif; font-size: 1.9rem; color: var(--navy); }
  .stat-label { font-size: 0.8rem; color: var(--muted); font-weight: 500; margin-top: 2px; }

  /* ABOUT */
  #about { background: var(--bg); }
  .about-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 56px; align-items: start; }
  .about-text p { color: var(--slate); font-weight: 300; margin-bottom: 18px; font-size: 1rem; }
  .about-highlights { display: flex; flex-direction: column; gap: 14px; margin-top: 28px; }
  .highlight-item {
    display: flex; align-items: center; gap: 12px;
    background: var(--surface); padding: 14px 18px;
    border-radius: var(--radius); border-left: 3px solid var(--accent);
    box-shadow: var(--shadow); font-size: 0.9rem; color: var(--slate); font-weight: 500;
  }
  .highlight-item span.icon { font-size: 1.1rem; }
  .about-card {
    background: var(--surface); border-radius: 14px;
    padding: 32px; box-shadow: var(--shadow);
    border: 1px solid var(--border);
  }
  .about-card h4 { font-family: 'DM Serif Display', serif; font-size: 1.15rem; margin-bottom: 20px; color: var(--navy); }
  .info-row { display: flex; gap: 10px; margin-bottom: 14px; font-size: 0.9rem; color: var(--slate); }
  .info-row strong { color: var(--navy); min-width: 80px; font-weight: 600; }
  .seeking-tags { display: flex; flex-wrap: wrap; gap: 8px; margin-top: 20px; }
  .tag {
    background: var(--accent-light); color: var(--accent);
    font-size: 0.78rem; font-weight: 600; padding: 5px 13px;
    border-radius: 100px; letter-spacing: 0.02em;
  }

  /* SKILLS */
  #skills { background: var(--surface); }
  .skills-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 24px; }
  .skill-card {
    background: var(--bg); border-radius: 14px;
    padding: 28px 24px; border: 1px solid var(--border);
    box-shadow: var(--shadow); transition: transform 0.2s, box-shadow 0.2s;
  }
  .skill-card:hover { transform: translateY(-3px); box-shadow: var(--shadow-md); }
  .skill-card-icon { font-size: 1.5rem; margin-bottom: 12px; }
  .skill-card h4 { font-weight: 700; font-size: 0.85rem; text-transform: uppercase; letter-spacing: 0.08em; color: var(--accent); margin-bottom: 16px; }
  .skill-item { display: flex; align-items: center; gap: 8px; margin-bottom: 10px; font-size: 0.9rem; color: var(--slate); }
  .skill-dot { width: 6px; height: 6px; border-radius: 50%; background: var(--accent); flex-shrink: 0; }

  /* EXPERIENCE */
  #experience { background: var(--bg); }
  .exp-timeline { display: flex; flex-direction: column; gap: 0; }
  .exp-item {
    display: grid; grid-template-columns: 180px 1fr;
    gap: 32px; padding-bottom: 40px; position: relative;
  }
  .exp-item:not(:last-child)::after {
    content: ''; position: absolute;
    left: 180px; top: 8px; bottom: 0;
    width: 1px; background: var(--border);
    margin-left: 16px;
  }
  .exp-meta { text-align: right; padding-right: 32px; }
  .exp-date { font-size: 0.78rem; font-weight: 600; color: var(--accent); letter-spacing: 0.05em; text-transform: uppercase; }
  .exp-company { font-size: 0.85rem; color: var(--muted); margin-top: 4px; }
  .exp-body { padding-left: 32px; border-left: none; position: relative; }
  .exp-body::before {
    content: ''; position: absolute; left: -5px; top: 8px;
    width: 10px; height: 10px; border-radius: 50%;
    background: var(--accent); border: 2px solid var(--bg);
    box-shadow: 0 0 0 2px var(--accent);
  }
  .exp-role { font-family: 'DM Serif Display', serif; font-size: 1.2rem; color: var(--navy); margin-bottom: 6px; }
  .exp-org { font-size: 0.85rem; font-weight: 600; color: var(--accent); margin-bottom: 14px; }
  .exp-bullets { list-style: none; }
  .exp-bullets li { position: relative; padding-left: 16px; font-size: 0.92rem; color: var(--slate); margin-bottom: 8px; font-weight: 300; }
  .exp-bullets li::before { content: '→'; position: absolute; left: 0; color: var(--accent); font-size: 0.8rem; top: 2px; }

  /* PROJECTS */
  #projects { background: var(--surface); }
  .projects-grid { display: grid; grid-template-columns: repeat(2, 1fr); gap: 24px; }
  .project-card {
    background: var(--bg); border-radius: 14px;
    padding: 28px; border: 1px solid var(--border);
    box-shadow: var(--shadow); display: flex; flex-direction: column;
    transition: transform 0.2s, box-shadow 0.2s;
  }
  .project-card:hover { transform: translateY(-3px); box-shadow: var(--shadow-md); }
  .project-num { font-family: 'DM Serif Display', serif; font-size: 2rem; color: var(--border); margin-bottom: 12px; }
  .project-title { font-family: 'DM Serif Display', serif; font-size: 1.15rem; color: var(--navy); margin-bottom: 10px; }
  .project-desc { font-size: 0.9rem; color: var(--slate); font-weight: 300; margin-bottom: 16px; line-height: 1.65; }
  .project-tags { display: flex; flex-wrap: wrap; gap: 7px; margin-bottom: 18px; }
  .project-tag { background: var(--accent-light); color: var(--accent); font-size: 0.74rem; font-weight: 600; padding: 4px 11px; border-radius: 100px; }
  .project-highlights { list-style: none; margin-bottom: 20px; }
  .project-highlights li { font-size: 0.87rem; color: var(--slate); padding-left: 16px; position: relative; margin-bottom: 6px; font-weight: 300; }
  .project-highlights li::before { content: '▸'; position: absolute; left: 0; color: var(--accent); }
  .project-link {
    margin-top: auto; display: inline-flex; align-items: center; gap: 6px;
    color: var(--accent); font-weight: 600; font-size: 0.85rem;
    text-decoration: none; letter-spacing: 0.02em; transition: gap 0.2s;
  }
  .project-link:hover { gap: 10px; }

  /* CERTIFICATIONS */
  #certifications { background: var(--bg); }
  .cert-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 20px; }
  .cert-card {
    background: var(--surface); border-radius: 14px;
    padding: 24px; border: 1px solid var(--border);
    box-shadow: var(--shadow); transition: transform 0.2s;
  }
  .cert-card:hover { transform: translateY(-2px); }
  .cert-icon { font-size: 1.4rem; margin-bottom: 10px; }
  .cert-name { font-weight: 700; font-size: 0.95rem; color: var(--navy); margin-bottom: 6px; }
  .cert-issuer { font-size: 0.8rem; color: var(--accent); font-weight: 600; margin-bottom: 8px; }
  .cert-desc { font-size: 0.85rem; color: var(--muted); font-weight: 300; }

  /* ADDITIONAL */
  #additional { background: var(--surface); }
  .extra-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 20px; }
  .extra-card {
    background: var(--bg); border-radius: 14px;
    padding: 24px; border: 1px solid var(--border); box-shadow: var(--shadow);
  }
  .extra-card .extra-icon { font-size: 1.6rem; margin-bottom: 10px; }
  .extra-card h4 { font-weight: 700; font-size: 0.95rem; color: var(--navy); margin-bottom: 6px; }
  .extra-card p { font-size: 0.85rem; color: var(--muted); font-weight: 300; }

  /* CONTACT */
  #contact { background: var(--navy); }
  #contact .section-label { color: #7fb3f5; }
  #contact .section-title { color: #fff; }
  .contact-wrapper { display: grid; grid-template-columns: 1fr 1fr; gap: 56px; align-items: start; }
  .contact-intro p { color: #a0b4c8; font-weight: 300; font-size: 1rem; line-height: 1.8; }
  .contact-items { display: flex; flex-direction: column; gap: 20px; margin-top: 32px; }
  .contact-item { display: flex; align-items: center; gap: 16px; }
  .contact-item-icon {
    width: 42px; height: 42px; border-radius: 10px;
    background: rgba(255,255,255,0.07); display: flex;
    align-items: center; justify-content: center; font-size: 1.1rem;
    flex-shrink: 0;
  }
  .contact-item-info { font-size: 0.9rem; }
  .contact-item-label { color: #7fb3f5; font-size: 0.75rem; font-weight: 600; text-transform: uppercase; letter-spacing: 0.08em; }
  .contact-item-value { color: #d0dde8; margin-top: 2px; }
  .contact-item-value a { color: #d0dde8; text-decoration: none; }
  .contact-item-value a:hover { color: #fff; }
  .social-links { display: flex; gap: 14px; margin-top: 32px; }
  .social-btn {
    display: inline-flex; align-items: center; gap: 8px;
    background: rgba(255,255,255,0.08); color: #d0dde8;
    padding: 10px 20px; border-radius: var(--radius);
    text-decoration: none; font-size: 0.85rem; font-weight: 600;
    transition: background 0.2s, color 0.2s; border: 1px solid rgba(255,255,255,0.1);
  }
  .social-btn:hover { background: var(--accent); color: #fff; border-color: var(--accent); }
  .contact-cta {
    background: rgba(255,255,255,0.05); border: 1px solid rgba(255,255,255,0.1);
    border-radius: 16px; padding: 36px;
  }
  .contact-cta h3 { font-family: 'DM Serif Display', serif; color: #fff; font-size: 1.4rem; margin-bottom: 12px; }
  .contact-cta p { color: #a0b4c8; font-size: 0.9rem; font-weight: 300; margin-bottom: 24px; line-height: 1.7; }
  .btn-white {
    display: inline-block; background: #fff; color: var(--navy);
    padding: 13px 28px; border-radius: var(--radius);
    text-decoration: none; font-weight: 700; font-size: 0.9rem;
    transition: background 0.2s, transform 0.15s;
  }
  .btn-white:hover { background: var(--accent-light); transform: translateY(-1px); }

  /* FOOTER */
  footer {
    background: #0a1520; text-align: center;
    padding: 24px 5%; color: #4a6080; font-size: 0.82rem;
  }

  /* RESPONSIVE */
  @media (max-width: 900px) {
    .about-grid { grid-template-columns: 1fr; }
    .skills-grid { grid-template-columns: 1fr 1fr; }
    .projects-grid { grid-template-columns: 1fr; }
    .cert-grid { grid-template-columns: 1fr 1fr; }
    .extra-grid { grid-template-columns: 1fr 1fr; }
    .contact-wrapper { grid-template-columns: 1fr; }
    .exp-item { grid-template-columns: 1fr; }
    .exp-item:not(:last-child)::after { display: none; }
    .exp-meta { text-align: left; padding-right: 0; padding-bottom: 8px; }
    .exp-body { padding-left: 20px; }
  }
  @media (max-width: 640px) {
    .nav-links { display: none; }
    .hamburger { display: flex; }
    .skills-grid { grid-template-columns: 1fr; }
    .cert-grid { grid-template-columns: 1fr; }
    .extra-grid { grid-template-columns: 1fr; }
    .hero-stats { gap: 24px; }
    #hero::before { display: none; }
    .section-title { font-size: 1.6rem; }
  }
</style>
</head>
<body>

<!-- NAV -->
<nav>
  <a href="#hero" class="nav-brand">Abhishek Saluja</a>
  <ul class="nav-links">
    <li><a href="#about">About</a></li>
    <li><a href="#skills">Skills</a></li>
    <li><a href="#experience">Experience</a></li>
    <li><a href="#projects">Projects</a></li>
    <li><a href="#certifications">Certifications</a></li>
    <li><a href="#contact">Contact</a></li>
  </ul>
  <button class="hamburger" onclick="toggleMenu()" aria-label="Menu">
    <span></span><span></span><span></span>
  </button>
</nav>
<div class="mobile-menu" id="mobileMenu">
  <a href="#about" onclick="closeMenu()">About</a>
  <a href="#skills" onclick="closeMenu()">Skills</a>
  <a href="#experience" onclick="closeMenu()">Experience</a>
  <a href="#projects" onclick="closeMenu()">Projects</a>
  <a href="#certifications" onclick="closeMenu()">Certifications</a>
  <a href="#contact" onclick="closeMenu()">Contact</a>
</div>

<!-- HERO -->
<section id="hero">
  <div class="hero-inner">
    <span class="hero-tag">Open to Finance · MIS · Accounts Roles</span>
    <h1 class="hero-name">Abhishek<br>Saluja</h1>
    <p class="hero-title">Finance &nbsp;|&nbsp; MIS Reporting &nbsp;|&nbsp; Accounts &nbsp;|&nbsp; Excel Analytics</p>
    <div class="hero-divider"></div>
    <p class="hero-tagline">BBA (Finance) graduate with practical exposure to accounting, financial analysis, and Excel-based reporting. Focused on finance operations, MIS reporting, and business analysis.</p>
    <div class="hero-cta">
      <a href="#projects" class="btn-primary">View Projects</a>
      <a href="#" class="btn-secondary" onclick="alert('Resume download — please link your PDF here.')">Download Resume</a>
    </div>
    <div class="hero-stats">
      <div>
        <div class="stat-num">4+</div>
        <div class="stat-label">Finance Projects</div>
      </div>
      <div>
        <div class="stat-num">2</div>
        <div class="stat-label">Work Experiences</div>
      </div>
      <div>
        <div class="stat-num">3+</div>
        <div class="stat-label">Certifications</div>
      </div>
      <div>
        <div class="stat-num">BBA</div>
        <div class="stat-label">Finance · 2026</div>
      </div>
    </div>
  </div>
</section>

<!-- ABOUT -->
<section id="about">
  <div class="section">
    <div class="section-label">Who I Am</div>
    <h2 class="section-title">About Me</h2>
    <div class="about-grid">
      <div class="about-text">
        <p>I'm a final-year BBA (Finance) student at Dev Bhoomi Uttarakhand University, building a strong foundation in financial analysis, accounting, and Excel-based MIS reporting.</p>
        <p>During my internship at a Chartered Accountant firm, I gained practical exposure to GST filing, TDS compliance, bookkeeping, bank reconciliation, and audit documentation — working directly with real client files.</p>
        <p>I've independently built financial models and dashboards for companies like Tata Motors, L&T, and HDFC Bank, developing my ability to interpret financial statements and turn data into business insights.</p>
        <p>I'm detail-oriented, quick to learn, and genuinely interested in how numbers tell the story of a business. I'm actively looking for entry-level roles where I can contribute from day one.</p>
        <div class="about-highlights">
          <div class="highlight-item"><span class="icon">📊</span> Excel-based 3-Statement Financial Modeling</div>
          <div class="highlight-item"><span class="icon">🧾</span> GST / TDS / Bank Reconciliation (CA Firm)</div>
          <div class="highlight-item"><span class="icon">📈</span> MIS Reporting & Dashboard Development</div>
          <div class="highlight-item"><span class="icon">🔍</span> Financial Ratio & Trend Analysis</div>
        </div>
      </div>
      <div>
        <div class="about-card">
          <h4>Quick Info</h4>
          <div class="info-row"><strong>Degree</strong><span>BBA – Finance (2023–2026)</span></div>
          <div class="info-row"><strong>University</strong><span>Dev Bhoomi Uttarakhand University</span></div>
          <div class="info-row"><strong>Location</strong><span>Rudrapur, Uttarakhand / Delhi NCR</span></div>
          <div class="info-row"><strong>Email</strong><span><a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="a6c7c4cecfd5cec3cdd5c7cad3ccc7979197e6c1cbc7cfca88c5c9cb">[email&#160;protected]</a></span></div>
          <div class="info-row"><strong>Phone</strong><span>+91 7455941268</span></div>
          <div class="info-row"><strong>LinkedIn</strong><span><a href="https://www.linkedin.com/in/abhisheksaluja9748" target="_blank" style="color:var(--accent)">linkedin.com/in/abhisheksaluja9748</a></span></div>
          <div style="margin-top:20px; font-size:0.8rem; font-weight:700; color:var(--navy); text-transform:uppercase; letter-spacing:0.08em;">Seeking Roles In</div>
          <div class="seeking-tags">
            <span class="tag">Finance Analyst</span>
            <span class="tag">MIS Executive</span>
            <span class="tag">Accounts Assistant</span>
            <span class="tag">Business Analyst</span>
            <span class="tag">Back Office Finance</span>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- SKILLS -->
<section id="skills">
  <div class="section">
    <div class="section-label">What I Know</div>
    <h2 class="section-title">Core Skills</h2>
    <div class="skills-grid">
      <div class="skill-card">
        <div class="skill-card-icon">📊</div>
        <h4>Technical Finance</h4>
        <div class="skill-item"><span class="skill-dot"></span>Financial Statement Analysis</div>
        <div class="skill-item"><span class="skill-dot"></span>Financial Modeling (3-Statement)</div>
        <div class="skill-item"><span class="skill-dot"></span>Ratio & Trend Analysis</div>
        <div class="skill-item"><span class="skill-dot"></span>Budgeting & Forecasting</div>
        <div class="skill-item"><span class="skill-dot"></span>MIS Reporting</div>
      </div>
      <div class="skill-card">
        <div class="skill-card-icon">⚙️</div>
        <h4>Tools & Software</h4>
        <div class="skill-item"><span class="skill-dot"></span>Advanced Excel (Pivot, VLOOKUP, XLOOKUP, Slicers)</div>
        <div class="skill-item"><span class="skill-dot"></span>Power BI (Basic)</div>
        <div class="skill-item"><span class="skill-dot"></span>SAP Financials (Basic)</div>
        <div class="skill-item"><span class="skill-dot"></span>Tally ERP</div>
        <div class="skill-item"><span class="skill-dot"></span>Microsoft Office Suite</div>
      </div>
      <div class="skill-card">
        <div class="skill-card-icon">🧾</div>
        <h4>Accounting & Tax</h4>
        <div class="skill-item"><span class="skill-dot"></span>GST Filing & Compliance</div>
        <div class="skill-item"><span class="skill-dot"></span>TDS Returns</div>
        <div class="skill-item"><span class="skill-dot"></span>Bank Reconciliation</div>
        <div class="skill-item"><span class="skill-dot"></span>Ledger Scrutiny & Bookkeeping</div>
        <div class="skill-item"><span class="skill-dot"></span>Audit Documentation Support</div>
      </div>
    </div>
    <div style="display:flex; flex-wrap:wrap; gap:10px; margin-top:28px;">
      <span class="tag">Attention to Detail</span>
      <span class="tag">Analytical Thinking</span>
      <span class="tag">Communication</span>
      <span class="tag">Team Coordination</span>
      <span class="tag">Problem Solving</span>
      <span class="tag">Time Management</span>
    </div>
  </div>
</section>

<!-- EXPERIENCE -->
<section id="experience">
  <div class="section">
    <div class="section-label">Work History</div>
    <h2 class="section-title">Experience</h2>
    <div class="exp-timeline">
      <div class="exp-item">
        <div class="exp-meta">
          <div class="exp-date">Oct 2025 – Present</div>
          <div class="exp-company">Rudrapur, UK</div>
        </div>
        <div class="exp-body">
          <div class="exp-role">Business Operations & Finance Support</div>
          <div class="exp-org">Toran Biotic India Pvt. Ltd.</div>
          <ul class="exp-bullets">
            <li>Managed relationships with 15+ doctors, clinics, and distributors; coordinated product communication and market outreach.</li>
            <li>Prepared structured daily MIS reports tracking market performance metrics for management review.</li>
            <li>Supported internal expense monitoring, basic financial documentation, and operational bookkeeping.</li>
            <li>Coordinated cross-functional business activities and maintained accurate stakeholder records.</li>
          </ul>
        </div>
      </div>
      <div class="exp-item">
        <div class="exp-meta">
          <div class="exp-date">Jun 2025 – Jul 2025</div>
          <div class="exp-company">Rudrapur, UK</div>
        </div>
        <div class="exp-body">
          <div class="exp-role">Accounts & Tax Intern</div>
          <div class="exp-org">CA Kapil Arora & Associates</div>
          <ul class="exp-bullets">
            <li>Assisted in statutory audit preparation including audit working papers and financial documentation for client accounts.</li>
            <li>Performed bookkeeping, bank reconciliation, and detailed ledger scrutiny for 10+ client accounts using MS Excel.</li>
            <li>Supported GST return filing, TDS compliance, and income tax documentation under direct CA supervision.</li>
            <li>Gained hands-on exposure to accounting standards and real-world financial compliance workflows.</li>
          </ul>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- PROJECTS -->
<section id="projects">
  <div class="section">
    <div class="section-label">Work Samples</div>
    <h2 class="section-title">Finance Projects</h2>
    <div class="projects-grid">

      <div class="project-card">
        <div class="project-num">01</div>
        <h3 class="project-title">HDFC Bank – Financial Dashboard</h3>
        <p class="project-desc">Built an interactive Excel dashboard to analyze HDFC Bank's financial performance, enabling clear visualization of key metrics for management reporting.</p>
        <div class="project-tags">
          <span class="project-tag">Advanced Excel</span>
          <span class="project-tag">Pivot Tables</span>
          <span class="project-tag">Dashboard</span>
        </div>
        <ul class="project-highlights">
          <li>Dynamic dashboard using Pivot Tables, Slicers, Sparklines & Conditional Formatting</li>
          <li>Ratio analysis covering profitability, liquidity, and efficiency metrics</li>
          <li>Automated data refresh using structured Excel named ranges</li>
        </ul>
        <a href="https://docs.google.com/spreadsheets/d/1GI3pPpMBGbfUMfj8B_WGChsyFLry4vFS/edit" class="project-link" target="_blank">View Project &rarr;</a>
      </div>

      <div class="project-card">
        <div class="project-num">02</div>
        <h3 class="project-title">Larsen & Toubro – Financial Analysis</h3>
        <p class="project-desc">Conducted a comprehensive multi-year financial analysis of L&T using historical financial statements to evaluate business performance and identify trends.</p>
        <div class="project-tags">
          <span class="project-tag">Financial Modeling</span>
          <span class="project-tag">Trend Analysis</span>
          <span class="project-tag">Excel</span>
        </div>
        <ul class="project-highlights">
          <li>Multi-sheet model covering Income Statement, Balance Sheet & Cash Flow</li>
          <li>5-year revenue and expense trend analysis with CAGR calculations</li>
          <li>Ratio analysis across profitability, solvency & working capital metrics</li>
        </ul>
        <a href="https://docs.google.com/spreadsheets/d/1kJZYNCB9mLT1hgPHTMoorGpOmeO6N2S-/edit" class="project-link" target="_blank">View Project &rarr;</a>
      </div>

      <div class="project-card">
        <div class="project-num">03</div>
        <h3 class="project-title">Tata Motors – Scenario Financial Model</h3>
        <p class="project-desc">Developed an end-to-end 3-statement financial model with integrated scenario analysis to assess Tata Motors' performance and forecast future outcomes.</p>
        <div class="project-tags">
          <span class="project-tag">3-Statement Model</span>
          <span class="project-tag">Scenario Analysis</span>
          <span class="project-tag">Forecasting</span>
        </div>
        <ul class="project-highlights">
          <li>Base / Bull / Bear case scenarios with dynamic revenue assumptions</li>
          <li>Integrated P&L, Balance Sheet, and Cash Flow statements</li>
          <li>Sensitivity analysis on key drivers: revenue growth, EBITDA margins</li>
        </ul>
        <a href="https://docs.google.com/spreadsheets/d/1Dx5FzoKzj3iBNKco6R0WqKWVdBeN_4gb/edit" class="project-link" target="_blank">View Project &rarr;</a>
      </div>

      <div class="project-card">
        <div class="project-num">04</div>
        <h3 class="project-title">Trent Limited – Forecast Model</h3>
        <p class="project-desc">Built an assumption-driven financial forecast model for Trent Limited, projecting revenues, costs, and margins using structured Excel modeling techniques.</p>
        <div class="project-tags">
          <span class="project-tag">Forecasting</span>
          <span class="project-tag">Cost Analysis</span>
          <span class="project-tag">Excel Modeling</span>
        </div>
        <ul class="project-highlights">
          <li>Assumption-based revenue and cost projections over a 3–5 year horizon</li>
          <li>Gross margin and EBITDA margin analysis with adjustable growth drivers</li>
          <li>Structured model with clear input, assumption, and output sheets</li>
        </ul>
        <a href="https://docs.google.com/spreadsheets/d/1-Kc-ylfUcMG4SN8mKCik81M4-A0A6T7N/edit" class="project-link" target="_blank">View Project &rarr;</a>
      </div>

    </div>
  </div>
</section>

<!-- CERTIFICATIONS -->
<section id="certifications">
  <div class="section">
    <div class="section-label">Learning & Credentials</div>
    <h2 class="section-title">Certifications</h2>
    <div class="cert-grid">
      <div class="cert-card">
        <div class="cert-icon">🎓</div>
        <div class="cert-name">SAP Financials Essential Training</div>
        <div class="cert-issuer">LinkedIn Learning</div>
        <div class="cert-desc">Core SAP FI module concepts including accounting entries, asset management, and financial reporting workflows.</div>
      </div>
      <div class="cert-card">
        <div class="cert-icon">📐</div>
        <div class="cert-name">Six Sigma Principles</div>
        <div class="cert-issuer">Coursera</div>
        <div class="cert-desc">Fundamentals of process improvement, DMAIC methodology, and data-driven quality management.</div>
      </div>
      <div class="cert-card">
        <div class="cert-icon">⚡</div>
        <div class="cert-name">Six Sigma White Belt</div>
        <div class="cert-issuer">Quality Hub India</div>
        <div class="cert-desc">Entry-level certification in Six Sigma concepts, process thinking, and operational efficiency principles.</div>
      </div>
      <div class="cert-card">
        <div class="cert-icon">📊</div>
        <div class="cert-name">Financial Modeling (Advanced)</div>
        <div class="cert-issuer">Internshala</div>
        <div class="cert-desc">Practical Excel-based modeling covering 3-statement models, dashboards, scenario analysis, and AI in finance.</div>
        <a href="https://drive.google.com/file/d/1X0qFkh5iR2_U0H6eSSVK1VCuA8vU0Lng/view" target="_blank" style="display:inline-block;margin-top:12px;font-size:0.8rem;font-weight:600;color:var(--accent);text-decoration:none;">View Certificate &rarr;</a>
      </div>
      <div class="cert-card">
        <div class="cert-icon">🏦</div>
        <div class="cert-name">CPBFI – Banking, Finance & Insurance</div>
        <div class="cert-issuer">Bajaj Finserv / TimesPro</div>
        <div class="cert-desc">120-hour certification with exposure to banking operations, NBFC concepts, and corporate finance fundamentals.</div>
      </div>
    </div>
  </div>
</section>

<!-- ADDITIONAL EXPOSURE -->
<section id="additional">
  <div class="section">
    <div class="section-label">Beyond Coursework</div>
    <h2 class="section-title">Additional Exposure</h2>
    <div class="extra-grid">
      <div class="extra-card">
        <div class="extra-icon">🚀</div>
        <h4>E-Summit – IIT Roorkee</h4>
        <p>Participated in IIT Roorkee's entrepreneurship summit, gaining exposure to startup ecosystems, business pitching, and emerging market trends.</p>
      </div>
      <div class="extra-card">
        <div class="extra-icon">💡</div>
        <h4>Avishkar Innovation Event</h4>
        <p>Engaged in an inter-college innovation event focused on business problem-solving, analytical thinking, and presentation of ideas to a panel.</p>
      </div>
      <div class="extra-card">
        <div class="extra-icon">🤝</div>
        <h4>Volunteer Experience</h4>
        <p>Volunteered in organizing academic and social events, developing coordination, communication, and team management skills in fast-paced environments.</p>
      </div>
    </div>
  </div>
</section>

<!-- CONTACT -->
<section id="contact" style="padding: 0;">
  <div class="section" style="padding-top:80px; padding-bottom:80px; max-width:1080px;">
    <div class="section-label">Get In Touch</div>
    <h2 class="section-title">Contact</h2>
    <div class="contact-wrapper">
      <div class="contact-intro">
        <p>I'm actively looking for entry-level roles in Finance, MIS Reporting, Accounting, and Business Analysis. If you're hiring or want to connect, feel free to reach out directly.</p>
        <div class="contact-items">
          <div class="contact-item">
            <div class="contact-item-icon">📧</div>
            <div class="contact-item-info">
              <div class="contact-item-label">Email</div>
              <div class="contact-item-value"><a href="/cdn-cgi/l/email-protection#4322212b2a302b262830222f36292272747203242e222a2f6d202c2e"><span class="__cf_email__" data-cfemail="6706050f0e140f020c14060b120d0656505627000a060e0b4904080a">[email&#160;protected]</span></a></div>
            </div>
          </div>
          <div class="contact-item">
            <div class="contact-item-icon">📱</div>
            <div class="contact-item-info">
              <div class="contact-item-label">Phone</div>
              <div class="contact-item-value"><a href="tel:+917455941268">+91 7455941268</a></div>
            </div>
          </div>
          <div class="contact-item">
            <div class="contact-item-icon">📍</div>
            <div class="contact-item-info">
              <div class="contact-item-label">Location</div>
              <div class="contact-item-value">Rudrapur, Uttarakhand &nbsp;|&nbsp; Open to Delhi NCR</div>
            </div>
          </div>
        </div>
        <div class="social-links">
          <a href="https://www.linkedin.com/in/abhisheksaluja9748" target="_blank" class="social-btn">🔗 LinkedIn</a>
          <a href="#" class="social-btn">💼 Portfolio (GitHub)</a>
        </div>
      </div>
      <div class="contact-cta">
        <h3>Available for Immediate Joining</h3>
        <p>Open to full-time roles, internships, and contract positions in Finance, Accounts, MIS, and Business Analysis. Willing to relocate to Delhi NCR and other major cities.</p>
        <a href="/cdn-cgi/l/email-protection#98f9faf0f1ebf0fdf3ebf9f4edf2f9a9afa9d8fff5f9f1f4b6fbf7f5" class="btn-white">Send Me a Message</a>
      </div>
    </div>
  </div>
</section>

<footer>
  <p>© 2026 Abhishek Saluja &nbsp;·&nbsp; Built for professional opportunities in Finance & Accounts</p>
</footer>

<script data-cfasync="false" src="/cdn-cgi/scripts/5c5dd728/cloudflare-static/email-decode.min.js"></script><script>
  function toggleMenu() {
    document.getElementById('mobileMenu').classList.toggle('open');
  }
  function closeMenu() {
    document.getElementById('mobileMenu').classList.remove('open');
  }
  // Highlight active nav link on scroll
  c
