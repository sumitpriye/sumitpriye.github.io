<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>Sumit Priye — QA Automation Specialist</title>
<link rel="preconnect" href="https://fonts.googleapis.com" />
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
<link href="https://fonts.googleapis.com/css2?family=DM+Sans:ital,opsz,wght@0,9..40,300;0,9..40,400;0,9..40,500;1,9..40,300&family=DM+Serif+Display:ital@0;1&display=swap" rel="stylesheet" />
<style>
  *, *::before, *::after { margin: 0; padding: 0; box-sizing: border-box; }

  :root {
    --navy: #0f1f3d;
    --navy-mid: #1a3260;
    --accent: #2563eb;
    --accent-light: #dbeafe;
    --accent-muted: #93c5fd;
    --gold: #b45309;
    --gold-light: #fef3c7;
    --text-primary: #0f172a;
    --text-secondary: #475569;
    --text-muted: #94a3b8;
    --surface: #ffffff;
    --surface-2: #f8fafc;
    --border: #e2e8f0;
    --border-strong: #cbd5e1;
    --radius: 12px;
    --radius-sm: 8px;
    --shadow: 0 1px 3px rgba(0,0,0,.06), 0 4px 16px rgba(0,0,0,.04);
    --shadow-md: 0 4px 24px rgba(0,0,0,.08);
  }

  html { scroll-behavior: smooth; }

  body {
    font-family: 'DM Sans', sans-serif;
    background: var(--surface-2);
    color: var(--text-primary);
    font-size: 15px;
    line-height: 1.6;
    -webkit-font-smoothing: antialiased;
  }

  /* ── Nav ── */
  nav {
    position: sticky; top: 0; z-index: 200;
    background: rgba(255,255,255,0.92);
    backdrop-filter: blur(12px);
    border-bottom: 1px solid var(--border);
    display: flex; align-items: center; justify-content: space-between;
    padding: 0 2.5rem; height: 60px;
  }
  .nav-brand { font-size: 15px; font-weight: 500; color: var(--text-primary); letter-spacing: -0.01em; }
  .nav-brand span { color: var(--text-primary); }
  .nav-links { display: flex; gap: 2rem; list-style: none; }
  .nav-links a { font-size: 13px; color: var(--text-secondary); text-decoration: none; font-weight: 400; transition: color .2s; }
  .nav-links a:hover { color: var(--accent); }
  .nav-cta {
    font-size: 13px; font-weight: 500; padding: 7px 16px;
    background: var(--navy); color: #fff; border-radius: 99px;
    text-decoration: none; transition: background .2s;
  }
  .nav-cta:hover { background: var(--accent); }

  /* ── Page Layout ── */
  .page { max-width: 900px; margin: 0 auto; padding: 0 2rem; }

  /* ── Hero ── */
  .hero-wrap {
    background: linear-gradient(135deg, var(--navy) 0%, var(--navy-mid) 100%);
    padding: 5rem 0 4rem;
    position: relative; overflow: hidden;
  }
  .hero-wrap::before {
    content: '';
    position: absolute; inset: 0;
    background: radial-gradient(ellipse 80% 60% at 70% 50%, rgba(37,99,235,.18) 0%, transparent 70%);
  }
  .hero-inner { max-width: 900px; margin: 0 auto; padding: 0 2rem; position: relative; }
  .hero-tag {
    display: inline-flex; align-items: center; gap: 6px;
    font-size: 12px; font-weight: 500; letter-spacing: 0.08em; text-transform: uppercase;
    color: var(--accent-muted);
    margin-bottom: 1.5rem;
  }
  .hero-tag-dot { width: 6px; height: 6px; border-radius: 50%; background: #22c55e; flex-shrink: 0; animation: pulse 2s infinite; }
  @keyframes pulse { 0%,100%{opacity:1;} 50%{opacity:.4;} }

  .hero-name {
    font-family: 'DM Serif Display', serif;
    font-size: clamp(2.8rem, 6vw, 4.2rem);
    line-height: 1.1;
    letter-spacing: -0.02em;
    margin-bottom: 1rem;
    background: linear-gradient(120deg, #e0f2fe 0%, #7dd3fc 40%, #38bdf8 70%, #818cf8 100%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
  }
  .hero-name em { font-style: italic; -webkit-text-fill-color: inherit; }

  .hero-desc { font-size: 16px; color: rgba(255,255,255,.65); max-width: 520px; line-height: 1.75; margin-bottom: 2rem; }

  .hero-actions { display: flex; gap: 12px; flex-wrap: wrap; }
  .btn-hero-primary {
    display: inline-flex; align-items: center; gap: 8px;
    padding: 11px 22px; border-radius: 99px;
    background: var(--accent); color: #fff;
    font-size: 14px; font-weight: 500; text-decoration: none;
    transition: transform .15s, box-shadow .15s;
  }
  .btn-hero-primary:hover { transform: translateY(-1px); box-shadow: 0 4px 20px rgba(37,99,235,.4); }
  .btn-hero-secondary {
    display: inline-flex; align-items: center; gap: 8px;
    padding: 11px 22px; border-radius: 99px;
    background: rgba(255,255,255,.1); color: rgba(255,255,255,.85);
    border: 1px solid rgba(255,255,255,.2);
    font-size: 14px; font-weight: 400; text-decoration: none;
    transition: background .2s;
  }
  .btn-hero-secondary:hover { background: rgba(255,255,255,.18); }

  .hero-stats {
    display: flex; gap: 2.5rem; margin-top: 3rem;
    border-top: 1px solid rgba(255,255,255,.1); padding-top: 2rem;
  }
  .stat-num { font-size: 26px; font-weight: 500; color: #fff; }
  .stat-label { font-size: 12px; color: rgba(255,255,255,.5); margin-top: 2px; }

  /* ── Sections ── */
  .section { padding: 4rem 0; }
  .section + .section { border-top: 1px solid var(--border); }

  .section-eyebrow {
    font-size: 11px; font-weight: 500; letter-spacing: 0.1em;
    text-transform: uppercase; color: var(--accent);
    margin-bottom: 0.5rem;
  }
  .section-title {
    font-family: 'DM Serif Display', serif;
    font-size: 26px; color: var(--navy);
    letter-spacing: -0.02em; margin-bottom: 2rem;
  }

  /* ── About ── */
  .about-text { font-size: 16px; color: var(--text-secondary); line-height: 1.85; }
  .about-text + .about-text { margin-top: 1rem; }

  /* ── Experience ── */
  .timeline { display: flex; flex-direction: column; gap: 0; }
  .tl-item { display: grid; grid-template-columns: 130px 1fr; gap: 0 1.5rem; }
  .tl-item:not(:last-child) { padding-bottom: 2rem; }
  .tl-left { padding-top: 4px; }
  .tl-period { font-size: 12px; color: var(--text-muted); line-height: 1.5; }
  .tl-duration { font-size: 11px; color: var(--text-muted); opacity: .7; margin-top: 2px; }
  .tl-connector {
    display: flex; flex-direction: column; align-items: flex-end;
    padding-right: 1.5rem; margin-top: 0.5rem;
  }
  .tl-dot { width: 8px; height: 8px; border-radius: 50%; background: var(--accent); flex-shrink: 0; margin-top: 6px; }
  .tl-line { width: 1px; flex: 1; background: var(--border); margin-top: 4px; }

  .tl-right { padding-bottom: 0; }
  .tl-card {
    background: var(--surface); border: 1px solid var(--border);
    border-radius: var(--radius); padding: 1.25rem 1.5rem;
    box-shadow: var(--shadow); margin-bottom: 2rem;
  }
  .tl-card:last-child { margin-bottom: 0; }
  .tl-role { font-size: 15px; font-weight: 500; color: var(--text-primary); }
  .tl-company { font-size: 13px; color: var(--accent); margin-bottom: 0.75rem; }
  .tl-bullets { list-style: none; padding: 0; }
  .tl-bullets li {
    font-size: 13.5px; color: var(--text-secondary); line-height: 1.65;
    padding-left: 16px; position: relative; margin-bottom: 4px;
  }
  .tl-bullets li::before { content: "→"; position: absolute; left: 0; color: var(--accent-muted); font-size: 11px; top: 3px; }

  /* ── Projects ── */
  .projects-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(260px, 1fr)); gap: 1.25rem; }
  .proj-card {
    background: var(--surface); border: 1px solid var(--border);
    border-radius: var(--radius); padding: 1.5rem;
    box-shadow: var(--shadow); display: flex; flex-direction: column;
    transition: transform .15s, box-shadow .15s;
  }
  .proj-card:hover { transform: translateY(-2px); box-shadow: var(--shadow-md); }
  .proj-icon-wrap {
    width: 42px; height: 42px; border-radius: var(--radius-sm);
    background: var(--accent-light); display: flex; align-items: center;
    justify-content: center; margin-bottom: 1rem;
  }
  .proj-icon-wrap svg { width: 20px; height: 20px; stroke: var(--accent); fill: none; stroke-width: 1.8; stroke-linecap: round; stroke-linejoin: round; }
  .proj-title { font-size: 15px; font-weight: 500; margin-bottom: 6px; }
  .proj-desc { font-size: 13.5px; color: var(--text-secondary); line-height: 1.65; flex: 1; margin-bottom: 1rem; }
  .tag-row { display: flex; flex-wrap: wrap; gap: 5px; }
  .tag {
    font-size: 11px; padding: 3px 9px; border-radius: 99px;
    background: var(--accent-light); color: #1d4ed8; font-weight: 500;
  }

  /* ── Skills ── */
  .skills-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(200px, 1fr)); gap: 1rem; }
  .skill-card {
    background: var(--surface); border: 1px solid var(--border);
    border-radius: var(--radius); padding: 1.1rem 1.25rem;
    box-shadow: var(--shadow);
  }
  .skill-cat {
    font-size: 11px; font-weight: 500; text-transform: uppercase;
    letter-spacing: 0.08em; color: var(--text-muted); margin-bottom: 10px;
  }
  .skill-pills { display: flex; flex-wrap: wrap; gap: 5px; }
  .skill-pill {
    font-size: 12px; padding: 4px 10px; border-radius: 99px;
    border: 1px solid var(--border-strong); color: var(--text-secondary);
    background: var(--surface-2);
  }

  /* ── Education ── */
  .edu-list { display: flex; flex-direction: column; gap: 1rem; }
  .edu-card {
    background: var(--surface); border: 1px solid var(--border);
    border-radius: var(--radius); padding: 1.1rem 1.5rem;
    display: flex; align-items: flex-start; gap: 14px;
    box-shadow: var(--shadow);
  }
  .edu-icon-wrap {
    width: 38px; height: 38px; flex-shrink: 0; border-radius: var(--radius-sm);
    background: var(--navy); display: flex; align-items: center; justify-content: center;
  }
  .edu-icon-wrap svg { width: 18px; height: 18px; stroke: rgba(255,255,255,.8); fill: none; stroke-width: 1.8; stroke-linecap: round; stroke-linejoin: round; }
  .edu-degree { font-size: 14px; font-weight: 500; }
  .edu-school { font-size: 13px; color: var(--accent); margin-top: 1px; }
  .edu-meta { font-size: 12px; color: var(--text-muted); margin-top: 2px; }

  /* ── Certifications ── */
  .certs-list { display: flex; flex-direction: column; gap: 8px; }
  .cert-item {
    background: var(--surface); border: 1px solid var(--border);
    border-radius: var(--radius-sm); padding: 0.85rem 1.25rem;
    display: flex; align-items: center; gap: 12px;
    box-shadow: var(--shadow);
  }
  .cert-badge {
    width: 32px; height: 32px; flex-shrink: 0; border-radius: 50%;
    background: var(--accent-light); display: flex; align-items: center; justify-content: center;
  }
  .cert-badge svg { width: 16px; height: 16px; stroke: var(--accent); fill: none; stroke-width: 1.8; stroke-linecap: round; stroke-linejoin: round; }
  .cert-name { font-size: 13.5px; font-weight: 400; color: var(--text-primary); }
  .cert-org { font-size: 12px; color: var(--text-muted); }
  .cert-link { font-size: 12px; color: var(--accent); text-decoration: none; white-space: nowrap; flex-shrink: 0; margin-left: 12px; }
  .cert-link:hover { text-decoration: underline; }

  /* ── Award ── */
  .award-grid { display: flex; flex-direction: column; gap: 10px; }
  .award-card {
    display: flex; align-items: flex-start; gap: 14px;
    background: var(--surface); border: 1px solid var(--border);
    border-radius: var(--radius); padding: 1.1rem 1.5rem;
    box-shadow: var(--shadow);
  }
  .award-icon-wrap {
    width: 38px; height: 38px; flex-shrink: 0; border-radius: var(--radius-sm);
    background: var(--accent-light); display: flex; align-items: center; justify-content: center;
  }
  .award-icon-wrap svg { width: 18px; height: 18px; stroke: var(--accent); fill: none; stroke-width: 1.8; stroke-linecap: round; stroke-linejoin: round; }
  .award-title { font-size: 14px; font-weight: 500; color: var(--text-primary); }
  .award-sub { font-size: 13px; color: var(--text-secondary); margin-top: 2px; }
  .award-org { font-size: 11px; color: var(--text-muted); margin-top: 3px; }

  /* ── Contact ── */
  .contact-intro { font-size: 15px; color: var(--text-secondary); line-height: 1.8; margin-bottom: 1.5rem; }
  .social-row { display: flex; flex-wrap: wrap; gap: 10px; }
  .social-btn {
    display: inline-flex; align-items: center; gap: 8px;
    padding: 10px 18px; border-radius: 99px;
    border: 1px solid var(--border-strong);
    background: var(--surface); color: var(--text-secondary);
    font-size: 13px; text-decoration: none; font-weight: 400;
    transition: border-color .15s, color .15s, background .15s;
  }
  .social-btn:hover { border-color: var(--accent); color: var(--accent); background: var(--accent-light); }
  .social-btn svg { width: 16px; height: 16px; stroke: currentColor; fill: none; stroke-width: 1.8; stroke-linecap: round; stroke-linejoin: round; }

  /* ── Footer ── */
  footer {
    background: var(--navy); color: rgba(255,255,255,.4);
    text-align: center; padding: 2rem;
    font-size: 12px; letter-spacing: 0.03em;
  }
  footer a { color: rgba(255,255,255,.6); text-decoration: none; }

  /* ── Animations ── */
  .fade-in { opacity: 0; transform: translateY(16px); animation: fadeIn .5s ease forwards; }
  @keyframes fadeIn { to { opacity: 1; transform: translateY(0); } }
  .delay-1 { animation-delay: .1s; }
  .delay-2 { animation-delay: .2s; }
  .delay-3 { animation-delay: .3s; }

  @media (max-width: 640px) {
    nav { padding: 0 1.25rem; }
    .nav-links { display: none; }
    .page { padding: 0 1.25rem; }
    .hero-inner { padding: 0 1.25rem; }
    .hero-stats { gap: 1.5rem; flex-wrap: wrap; }
    .tl-item { grid-template-columns: 1fr; }
    .tl-left { display: none; }
  }
</style>
</head>
<body>

<!-- Nav -->
<nav>
  <span class="nav-brand">Sumit <span>Priye</span></span>
  <ul class="nav-links">
    <li><a href="#about">About</a></li>
    <li><a href="#experience">Experience</a></li>
    <li><a href="#projects">Projects</a></li>
    <li><a href="#skills">Skills</a></li>
    <li><a href="#education">Education</a></li>
    <li><a href="#contact">Contact</a></li>
  </ul>
  <a href="mailto:sumitsinha125@gmail.com" class="nav-cta">Hire me</a>
</nav>

<!-- Hero -->
<div class="hero-wrap">
  <div class="hero-inner">
    <div class="hero-tag fade-in">
      <span class="hero-tag-dot"></span>
      Available for opportunities
    </div>
    <h1 class="hero-name fade-in delay-1">Sumit <em>Priye</em></h1>
    <p class="hero-desc fade-in delay-2">
      QA Automation Specialist with 9+ years designing scalable test frameworks, 
      integrating CI/CD pipelines, and exploring AI-driven testing at enterprise scale.
    </p>
    <div class="hero-actions fade-in delay-3">
      <a href="mailto:sumitsinha125@gmail.com" class="btn-hero-primary">
        <svg viewBox="0 0 24 24" style="width:16px;height:16px;stroke:#fff;fill:none;stroke-width:1.8;stroke-linecap:round;stroke-linejoin:round"><rect x="2" y="4" width="20" height="16" rx="2"/><path d="m2 7 10 7 10-7"/></svg>
        Get in touch
      </a>
      <a href="#" onclick="alert('Replace this with your resume PDF URL')" class="btn-hero-secondary">
        <svg viewBox="0 0 24 24" style="width:16px;height:16px;stroke:rgba(255,255,255,.8);fill:none;stroke-width:1.8;stroke-linecap:round;stroke-linejoin:round"><path d="M21 15v4a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2v-4"/><polyline points="7 10 12 15 17 10"/><line x1="12" y1="15" x2="12" y2="3"/></svg>
        Download resume
      </a>
    </div>
    <div class="hero-stats fade-in delay-3">
      <div>
        <div class="stat-num">9+</div>
        <div class="stat-label">Years of experience</div>
      </div>
      <div>
        <div class="stat-num">3</div>
        <div class="stat-label">Companies</div>
      </div>
      <div>
        <div class="stat-num">8</div>
        <div class="stat-label">Certifications</div>
      </div>
      <div>
        <div class="stat-num">4</div>
        <div class="stat-label">Awards won</div>
      </div>
    </div>
  </div>
</div>

<!-- About -->
<div class="page">
  <section class="section" id="about">
    <div class="section-eyebrow">About me</div>
    <h2 class="section-title">Building quality at scale</h2>
    <p class="about-text">Experienced QA Automation Engineer with 9+ years of expertise in designing, developing, and maintaining scalable automation frameworks for enterprise web applications. Strong hands-on experience with Selenium WebDriver, TestNG, Maven, and Data-Driven/BDD automation frameworks, covering the complete test automation lifecycle from framework development to CI/CD integration with Jenkins.</p>
    <p class="about-text">Skilled in Core Java, Python, SQL, Azure DevOps, and Azure Cosmos DB, with deep experience in API and web services testing using Postman and SoapUI. Currently exploring AI-driven testing approaches to enhance test automation, productivity, and defect analysis — passionate about building reliable automation solutions and contributing to high-quality software delivery in Agile environments.</p>
  </section>

  <!-- Experience -->
  <section class="section" id="experience">
    <div class="section-eyebrow">Career</div>
    <h2 class="section-title">Work experience</h2>
    <div class="timeline">

      <div class="tl-item">
        <div class="tl-left">
          <div class="tl-period">Oct 2021 – Present</div>
          <div class="tl-duration">4 yrs 8 mos</div>
        </div>
        <div class="tl-right">
          <div class="tl-card">
            <div class="tl-role">Quality Automation Specialist</div>
            <div class="tl-company">NatWest Group · Gurugram</div>
            <ul class="tl-bullets">
              <li>Architected and maintained scalable BDD-based automation frameworks using <strong>Selenium WebDriver</strong>, <strong>TestNG</strong>, and <strong>Maven</strong> for enterprise-grade banking web applications</li>
              <li>Designed and implemented Data-Driven test suites integrated with <strong>Jenkins CI/CD</strong> pipelines, enabling continuous regression across release cycles</li>
              <li>Managed test environments and data pipelines on <strong>Azure DevOps</strong> and <strong>Azure Cosmos DB</strong>; coordinated deployments with cross-functional Agile teams</li>
              <li>Performed comprehensive API and web services testing using <strong>Postman</strong> and <strong>SoapUI</strong> for both REST and SOAP endpoints</li>
              <li>Executed functional, regression, smoke, integration, and UAT test cycles; tracked and managed defects through <strong>Jira</strong> with thorough root-cause analysis</li>
              <li>Pioneered AI-driven testing approaches — leveraging modern AI tooling to enhance test coverage, defect prediction, and productivity across the QA team</li>
            </ul>
          </div>
        </div>
      </div>

      <div class="tl-item">
        <div class="tl-left">
          <div class="tl-period">Mar 2020 – Oct 2021</div>
          <div class="tl-duration">1 yr 8 mos</div>
        </div>
        <div class="tl-right">
          <div class="tl-card">
            <div class="tl-role">Lead Engineer — Testing</div>
            <div class="tl-company">Fidelity Information Services (FIS) · Bengaluru</div>
            <div style="font-size:12px;color:var(--text-muted);margin-bottom:10px;">Project: Modern Banking Platform (MBP) — Next-generation core banking with Plug &amp; Play architecture</div>
            <ul class="tl-bullets">
              <li>Led end-to-end QA automation for the <strong>Modern Banking Platform (MBP)</strong> — a next-generation core banking system serving both commercial and retail lines of business</li>
              <li>Developed and reviewed automated test cases using <strong>Selenium WebDriver with Java</strong>; created test conditions from Business Analyst requirement documents</li>
              <li>Conducted thorough <strong>API testing</strong> for REST and SOAP web services using <strong>Postman</strong> and <strong>SoapUI</strong>; validated end-to-end banking transaction flows</li>
              <li>Managed defect lifecycle — raising, tracking, retesting, and closing issues in <strong>Jira</strong> — maintaining clear traceability across test artefacts</li>
              <li>Functioned as an active QA lead within Agile Scrum ceremonies, directly engaging with clients from sprint inception through delivery; consistently met sprint commitments</li>
              <li>Managed test data and validation against <strong>Oracle SQL</strong> databases; used <strong>Git (BitBucket)</strong> for version control of automation scripts</li>
              <li>Recognised with the <strong>Kudos Award (Q4 2020)</strong> and <strong>Appreciation Award (Q2 2020)</strong> for exceptional delivery within short ramp-up timelines</li>
            </ul>
          </div>
        </div>
      </div>

      <div class="tl-item">
        <div class="tl-left">
          <div class="tl-period">Jun 2019 – Feb 2020</div>
          <div class="tl-duration">9 mos</div>
        </div>
        <div class="tl-right">
          <div class="tl-card">
            <div class="tl-role">Test Engineering Analyst</div>
            <div class="tl-company">Accenture · Bengaluru</div>
            <div style="font-size:12px;color:var(--text-muted);margin-bottom:10px;">Client: TELUS International — Canadian telecommunications services provider</div>
            <ul class="tl-bullets">
              <li>Performed functional, regression, smoke, and integration testing for telecom enterprise applications; ensured releases met agreed quality thresholds</li>
              <li>Collaborated with onshore Agile Scrum teams across planning, grooming, and retrospective ceremonies; owned testing deliverables end-to-end</li>
              <li>Contributed to Selenium WebDriver UI automation framework development; authored reusable test modules in <strong>Java</strong> using <strong>TestNG</strong></li>
              <li>Tracked and managed defects in <strong>Jira</strong> and <strong>HP Quality Center</strong>; coordinated with Testing Coordinators to ensure complete and timely functional coverage</li>
              <li>Managed QA documentation — test plans, test cases, and execution reports — ensuring process adherence and stakeholder visibility</li>
            </ul>
          </div>
        </div>
      </div>

      <div class="tl-item">
        <div class="tl-left">
          <div class="tl-period">Apr 2017 – May 2019</div>
          <div class="tl-duration">2 yrs 2 mos</div>
        </div>
        <div class="tl-right">
          <div class="tl-card">
            <div class="tl-role">Associate Software Engineer</div>
            <div class="tl-company">Accenture · Bengaluru</div>
            <div style="font-size:12px;color:var(--text-muted);margin-bottom:10px;">Client: TELUS International — Canadian telecommunications services provider</div>
            <ul class="tl-bullets">
              <li>Developed, modified, and executed software test plans and test cases based on requirements; authored test conditions in alignment with Business Analyst specifications</li>
              <li>Built UI automation scripts using <strong>Selenium WebDriver</strong> with Core <strong>Java</strong> as part of a collaborative framework development effort</li>
              <li>Performed test estimation and effort analysis using Assessment-Intake Forms; supported test planning and scheduling for project milestones</li>
              <li>Managed the complete defect lifecycle — raising, retesting, and closing issues — via <strong>Jira</strong>, <strong>Bugzilla</strong>, and <strong>HP Quality Center</strong></li>
              <li>Partnered with Testing Coordinators and onshore teams to document and communicate the QA process; ensured traceability and compliance throughout</li>
              <li>Won the <strong>APEX Award</strong> for two consecutive fiscal quarters (FY19 Q2 &amp; Q3) for demonstrating ownership and driving automation adoption; awarded <strong>Performer of the Year</strong> in the CMT domain</li>
            </ul>
          </div>
        </div>
      </div>

    </div>
  </section>

  <!-- Projects -->
  <section class="section" id="projects">
    <div class="section-eyebrow">Work</div>
    <h2 class="section-title">Featured projects</h2>
    <div class="projects-grid">

      <div class="proj-card">
        <div class="proj-icon-wrap">
          <svg viewBox="0 0 24 24"><rect x="3" y="11" width="18" height="10" rx="2"/><path d="M7 11V7a5 5 0 0 1 10 0v4"/><circle cx="12" cy="16" r="1.5" fill="#2563eb" stroke="none"/></svg>
        </div>
        <div class="proj-title">Ticket Booking E2E Automation</div>
        <div class="proj-desc">Complete end-to-end automated test suite for a ticket booking application — covering search, seat selection, payment, and booking confirmation flows using Selenium WebDriver with BDD.</div>
        <div class="tag-row">
          <span class="tag">Selenium</span><span class="tag">Java</span><span class="tag">TestNG</span><span class="tag">Maven</span><span class="tag">BDD</span>
        </div>
      </div>

      <div class="proj-card">
        <div class="proj-icon-wrap">
          <svg viewBox="0 0 24 24"><polyline points="22 12 18 12 15 21 9 3 6 12 2 12"/></svg>
        </div>
        <div class="proj-title">ML Regression & Classification</div>
        <div class="proj-desc">Machine learning projects solving real-world supervised learning problems — including data preprocessing, feature engineering, model training, hyperparameter tuning, and performance evaluation.</div>
        <div class="tag-row">
          <span class="tag">Python</span><span class="tag">Scikit-learn</span><span class="tag">Pandas</span><span class="tag">Feature Engineering</span><span class="tag">EDA</span>
        </div>
      </div>

      <div class="proj-card">
        <div class="proj-icon-wrap">
          <svg viewBox="0 0 24 24"><circle cx="12" cy="8" r="4"/><path d="M6 20v-2a6 6 0 0 1 12 0v2"/><circle cx="18" cy="8" r="2" stroke-dasharray="2 2"/></svg>
        </div>
        <div class="proj-title">Face Recognition System</div>
        <div class="proj-desc">Deep learning-based face recognition system capable of identifying and verifying individuals from images using convolutional neural networks and OpenCV for real-time processing.</div>
        <div class="tag-row">
          <span class="tag">Python</span><span class="tag">Deep Learning</span><span class="tag">CNN</span><span class="tag">OpenCV</span>
        </div>
      </div>

    </div>
  </section>

  <!-- Skills -->
  <section class="section" id="skills">
    <div class="section-eyebrow">Expertise</div>
    <h2 class="section-title">Skills & tech stack</h2>
    <div class="skills-grid">
      <div class="skill-card">
        <div class="skill-cat">Automation</div>
        <div class="skill-pills">
          <span class="skill-pill">Selenium WebDriver</span>
          <span class="skill-pill">TestNG</span>
          <span class="skill-pill">Maven</span>
          <span class="skill-pill">BDD / Cucumber</span>
          <span class="skill-pill">Data-Driven</span>
        </div>
      </div>
      <div class="skill-card">
        <div class="skill-cat">Languages</div>
        <div class="skill-pills">
          <span class="skill-pill">Core Java</span>
          <span class="skill-pill">Python</span>
          <span class="skill-pill">SQL</span>
        </div>
      </div>
      <div class="skill-card">
        <div class="skill-cat">API & Testing</div>
        <div class="skill-pills">
          <span class="skill-pill">Postman</span>
          <span class="skill-pill">SoapUI</span>
          <span class="skill-pill">REST APIs</span>
          <span class="skill-pill">Functional</span>
          <span class="skill-pill">Regression</span>
          <span class="skill-pill">Integration</span>
        </div>
      </div>
      <div class="skill-card">
        <div class="skill-cat">Cloud & DevOps</div>
        <div class="skill-pills">
          <span class="skill-pill">Azure DevOps</span>
          <span class="skill-pill">Azure Cosmos DB</span>
          <span class="skill-pill">Jenkins</span>
          <span class="skill-pill">CI/CD</span>
        </div>
      </div>
      <div class="skill-card">
        <div class="skill-cat">Tools</div>
        <div class="skill-pills">
          <span class="skill-pill">Jira</span>
          <span class="skill-pill">Bugzilla</span>
          <span class="skill-pill">HP Quality Center</span>
          <span class="skill-pill">Git</span>
        </div>
      </div>
      <div class="skill-card">
        <div class="skill-cat">Data & AI</div>
        <div class="skill-pills">
          <span class="skill-pill">Feature Engineering</span>
          <span class="skill-pill">EDA</span>
          <span class="skill-pill">Machine Learning</span>
          <span class="skill-pill">Deep Learning</span>
          <span class="skill-pill">Generative AI</span>
        </div>
      </div>
    </div>
  </section>

  <!-- Education -->
  <section class="section" id="education">
    <div class="section-eyebrow">Background</div>
    <h2 class="section-title">Education</h2>
    <div class="edu-list">
      <div class="edu-card">
        <div class="edu-icon-wrap">
          <svg viewBox="0 0 24 24"><path d="M22 10v6M2 10l10-5 10 5-10 5-10-5z"/><path d="M6 12v5c3 3 9 3 12 0v-5"/></svg>
        </div>
        <div>
          <div class="edu-degree">B.Tech, Mechanical Engineering</div>
          <div class="edu-school">BIT Sindri</div>
          <div class="edu-meta">2012 – 2016</div>
        </div>
      </div>
      <div class="edu-card">
        <div class="edu-icon-wrap">
          <svg viewBox="0 0 24 24"><rect x="2" y="3" width="20" height="14" rx="2"/><path d="M8 21h8M12 17v4"/></svg>
        </div>
        <div>
          <div class="edu-degree">AISSCE (Class XII) — CBSE</div>
          <div class="edu-school">DAV Public School Bistupur, Jamshedpur</div>
          <div class="edu-meta">Physics · Chemistry · Mathematics · Economics</div>
        </div>
      </div>
      <div class="edu-card">
        <div class="edu-icon-wrap">
          <svg viewBox="0 0 24 24"><rect x="2" y="3" width="20" height="14" rx="2"/><path d="M8 21h8M12 17v4"/></svg>
        </div>
        <div>
          <div class="edu-degree">AISSE (Class X) — CBSE</div>
          <div class="edu-school">SDSM School For Excellence, Jamshedpur</div>
          <div class="edu-meta">Mathematics · Science · English · Hindi</div>
        </div>
      </div>
    </div>
  </section>

  <!-- Certifications -->
  <section class="section">
    <div class="section-eyebrow">Learning</div>
    <h2 class="section-title">Certifications</h2>
    <div class="certs-list">
      <div class="cert-item">
        <div class="cert-badge"><svg viewBox="0 0 24 24" style="width:16px;height:16px;stroke:var(--accent);fill:none;stroke-width:1.8;stroke-linecap:round;stroke-linejoin:round"><circle cx="12" cy="8" r="6"/><path d="M15.477 12.89 17 22l-5-3-5 3 1.523-9.11"/></svg></div>
        <div style="flex:1;">
          <div class="cert-name">Selenium WebDriver with Java — Basics to Advanced + Frameworks</div>
          <div class="cert-org">Udemy</div>
        </div>
        <a href="https://www.udemy.com/certificate/UC-OFY7S7IX/" target="_blank" class="cert-link">View ↗</a>
      </div>
      <div class="cert-item">
        <div class="cert-badge"><svg viewBox="0 0 24 24" style="width:16px;height:16px;stroke:var(--accent);fill:none;stroke-width:1.8;stroke-linecap:round;stroke-linejoin:round"><circle cx="12" cy="8" r="6"/><path d="M15.477 12.89 17 22l-5-3-5 3 1.523-9.11"/></svg></div>
        <div style="flex:1;">
          <div class="cert-name">Generative AI for Executives and Business Leaders</div>
          <div class="cert-org">Coursera</div>
        </div>
        <a href="https://www.coursera.org/account/accomplishments/certificate/JCU6TMYN35BC" target="_blank" class="cert-link">View ↗</a>
      </div>
      <div class="cert-item">
        <div class="cert-badge"><svg viewBox="0 0 24 24" style="width:16px;height:16px;stroke:var(--accent);fill:none;stroke-width:1.8;stroke-linecap:round;stroke-linejoin:round"><circle cx="12" cy="8" r="6"/><path d="M15.477 12.89 17 22l-5-3-5 3 1.523-9.11"/></svg></div>
        <div style="flex:1;">
          <div class="cert-name">Machine Learning with Python</div>
          <div class="cert-org">NatWest × DataCamp</div>
        </div>
        <a href="https://www.datacamp.com/completed/statement-of-accomplishment/track/2c307dd3a10a1bbc908665948e9c5d05f2674ac7" target="_blank" class="cert-link">View ↗</a>
      </div>
      <div class="cert-item">
        <div class="cert-badge"><svg viewBox="0 0 24 24" style="width:16px;height:16px;stroke:var(--accent);fill:none;stroke-width:1.8;stroke-linecap:round;stroke-linejoin:round"><circle cx="12" cy="8" r="6"/><path d="M15.477 12.89 17 22l-5-3-5 3 1.523-9.11"/></svg></div>
        <div style="flex:1;">
          <div class="cert-name">Python Fundamentals for Data Science</div>
          <div class="cert-org">NatWest × DataCamp</div>
        </div>
        <a href="https://www.datacamp.com/completed/statement-of-accomplishment/track/081b49800a9ed366cc22a4b875600965387975f3" target="_blank" class="cert-link">View ↗</a>
      </div>
      <div class="cert-item">
        <div class="cert-badge"><svg viewBox="0 0 24 24" style="width:16px;height:16px;stroke:var(--accent);fill:none;stroke-width:1.8;stroke-linecap:round;stroke-linejoin:round"><circle cx="12" cy="8" r="6"/><path d="M15.477 12.89 17 22l-5-3-5 3 1.523-9.11"/></svg></div>
        <div style="flex:1;">
          <div class="cert-name">Introduction to Python</div>
          <div class="cert-org">DataCamp</div>
        </div>
        <a href="https://www.datacamp.com/statement-of-accomplishment/course/8882e255fb9e3ed7a8280439c73517a50eb0d56e?raw=1" target="_blank" class="cert-link">View ↗</a>
      </div>
      <div class="cert-item">
        <div class="cert-badge"><svg viewBox="0 0 24 24" style="width:16px;height:16px;stroke:var(--accent);fill:none;stroke-width:1.8;stroke-linecap:round;stroke-linejoin:round"><circle cx="12" cy="8" r="6"/><path d="M15.477 12.89 17 22l-5-3-5 3 1.523-9.11"/></svg></div>
        <div style="flex:1;">
          <div class="cert-name">Intermediate Python</div>
          <div class="cert-org">DataCamp</div>
        </div>
        <a href="https://www.datacamp.com/statement-of-accomplishment/course/c5c44f0124cae28e689e92398c7e812f1f8e6003?raw=1" target="_blank" class="cert-link">View ↗</a>
      </div>
      <div class="cert-item">
        <div class="cert-badge"><svg viewBox="0 0 24 24" style="width:16px;height:16px;stroke:var(--accent);fill:none;stroke-width:1.8;stroke-linecap:round;stroke-linejoin:round"><circle cx="12" cy="8" r="6"/><path d="M15.477 12.89 17 22l-5-3-5 3 1.523-9.11"/></svg></div>
        <div style="flex:1;">
          <div class="cert-name">Introduction to Azure</div>
          <div class="cert-org">DataCamp</div>
        </div>
        <a href="https://www.datacamp.com/statement-of-accomplishment/course/bc9ab693a914769ce2cc983a865cfce200d391d7?raw=1" target="_blank" class="cert-link">View ↗</a>
      </div>
      <div class="cert-item">
        <div class="cert-badge"><svg viewBox="0 0 24 24" style="width:16px;height:16px;stroke:var(--accent);fill:none;stroke-width:1.8;stroke-linecap:round;stroke-linejoin:round"><circle cx="12" cy="8" r="6"/><path d="M15.477 12.89 17 22l-5-3-5 3 1.523-9.11"/></svg></div>
        <div style="flex:1;">
          <div class="cert-name">DevOps Fundamentals — CI/CD with AWS + Docker + Ansible + Jenkins</div>
          <div class="cert-org">Udemy</div>
        </div>
        <a href="https://www.udemy.com/certificate/UC-990f125e-1314-4bd0-981a-f56f67b25566/" target="_blank" class="cert-link">View ↗</a>
      </div>
    </div>
  </section>

  <!-- Award -->
  <section class="section">
    <div class="section-eyebrow">Recognition</div>
    <h2 class="section-title">Honours & awards</h2>
    <div class="award-grid">
      <div class="award-card">
        <div class="award-icon-wrap">
          <svg viewBox="0 0 24 24"><circle cx="12" cy="8" r="6"/><path d="M15.477 12.89 17 22l-5-3-5 3 1.523-9.11"/></svg>
        </div>
        <div>
          <div class="award-title">APEX Award — FY19 Q2 &amp; Q3 (two consecutive quarters)</div>
          <div class="award-sub">Recognised for demonstrating strong ownership and driving automation adoption that contributed to business growth</div>
          <div class="award-org">Accenture</div>
        </div>
      </div>
      <div class="award-card">
        <div class="award-icon-wrap">
          <svg viewBox="0 0 24 24"><path d="M12 2l3.09 6.26L22 9.27l-5 4.87 1.18 6.88L12 17.77l-6.18 3.25L7 14.14 2 9.27l6.91-1.01L12 2z"/></svg>
        </div>
        <div>
          <div class="award-title">Performer of the Year — CMT Domain</div>
          <div class="award-sub">Awarded for exceptional performance in deliverables and for spearheading automation initiatives in the Communications, Media &amp; Technology domain</div>
          <div class="award-org">Accenture</div>
        </div>
      </div>
      <div class="award-card">
        <div class="award-icon-wrap">
          <svg viewBox="0 0 24 24"><path d="M14 9V5a3 3 0 0 0-3-3l-4 9v11h11.28a2 2 0 0 0 2-1.7l1.38-9a2 2 0 0 0-2-2.3H14z"/><path d="M7 22H4a2 2 0 0 1-2-2v-7a2 2 0 0 1 2-2h3"/></svg>
        </div>
        <div>
          <div class="award-title">Kudos Award — Q4 2020</div>
          <div class="award-sub">Recognised for exceptional work and rapid impact delivered within a short ramp-up period</div>
          <div class="award-org">Fidelity Information Services (FIS)</div>
        </div>
      </div>
      <div class="award-card">
        <div class="award-icon-wrap">
          <svg viewBox="0 0 24 24"><path d="M14 9V5a3 3 0 0 0-3-3l-4 9v11h11.28a2 2 0 0 0 2-1.7l1.38-9a2 2 0 0 0-2-2.3H14z"/><path d="M7 22H4a2 2 0 0 1-2-2v-7a2 2 0 0 1 2-2h3"/></svg>
        </div>
        <div>
          <div class="award-title">Appreciation Award — Q2 2020</div>
          <div class="award-sub">Awarded for quickly developing deep system understanding and completing all assigned deliverables within the stipulated timeframe</div>
          <div class="award-org">Fidelity Information Services (FIS)</div>
        </div>
      </div>
    </div>
  </section>

  <!-- Contact -->
  <section class="section" id="contact">
    <div class="section-eyebrow">Connect</div>
    <h2 class="section-title">Get in touch</h2>
    <p class="contact-intro">Open to connecting with recruiters, collaborators, and the broader tech community. Whether you have an opportunity, a project idea, or just want to say hello — reach out via any of the channels below.</p>
    <div class="social-row">
      <a href="mailto:sumitsinha125@gmail.com" class="social-btn">
        <svg viewBox="0 0 24 24"><rect x="2" y="4" width="20" height="16" rx="2"/><path d="m2 7 10 7 10-7"/></svg>
        sumitsinha125@gmail.com
      </a>
      <a href="https://www.linkedin.com/in/sumit-priye" target="_blank" class="social-btn">
        <svg viewBox="0 0 24 24"><path d="M16 8a6 6 0 0 1 6 6v7h-4v-7a2 2 0 0 0-2-2 2 2 0 0 0-2 2v7h-4v-7a6 6 0 0 1 6-6z"/><rect x="2" y="9" width="4" height="12"/><circle cx="4" cy="4" r="2"/></svg>
        LinkedIn
      </a>
      <a href="https://github.com/sumitpriye" target="_blank" class="social-btn">
        <svg viewBox="0 0 24 24"><path d="M15 22v-4a4.8 4.8 0 0 0-1-3.5c3 0 6-2 6-5.5.08-1.25-.27-2.48-1-3.5.28-1.15.28-2.35 0-3.5 0 0-1 0-3 1.5-2.64-.5-5.36-.5-8 0C6 2 5 2 5 2c-.3 1.15-.3 2.35 0 3.5A5.403 5.403 0 0 0 4 9c0 3.5 3 5.5 6 5.5-.39.49-.68 1.05-.85 1.65-.17.6-.22 1.23-.15 1.85v4"/><path d="M9 18c-4.51 2-5-2-7-2"/></svg>
        GitHub
      </a>
      <a href="https://twitter.com/" target="_blank" class="social-btn">
        <svg viewBox="0 0 24 24"><path d="M4 4l16 16M4 20L20 4"/></svg>
        Twitter / X
      </a>
    </div>
  </section>
</div>

<footer>
  <p>© 2026 Sumit Priye &nbsp;·&nbsp; <a href="mailto:sumitsinha125@gmail.com">sumitsinha125@gmail.com</a></p>
</footer>

</body>
</html>
