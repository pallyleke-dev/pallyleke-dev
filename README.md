<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Segun Olukayode — Data Analyst & AI Annotation Specialist</title>
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600&family=Playfair+Display:wght@700&display=swap" rel="stylesheet">
<style>
  :root {
    --navy: #0f1f38;
    --navy-mid: #1a2f50;
    --teal: #2a9d8f;
    --teal-light: #3ab5a5;
    --gold: #e9c46a;
    --cream: #f8f5f0;
    --text: #1a1a2e;
    --muted: #6b7280;
    --white: #ffffff;
    --card-bg: #ffffff;
    --border: #e5e7eb;
  }

  * { margin: 0; padding: 0; box-sizing: border-box; }

  body {
    font-family: 'Inter', sans-serif;
    background: var(--cream);
    color: var(--text);
    line-height: 1.6;
  }

  /* NAV */
  nav {
    position: fixed; top: 0; left: 0; right: 0;
    background: rgba(15, 31, 56, 0.97);
    backdrop-filter: blur(10px);
    z-index: 100;
    padding: 0 5%;
    display: flex; justify-content: space-between; align-items: center;
    height: 60px;
    border-bottom: 1px solid rgba(42,157,143,0.3);
  }
  .nav-logo {
    font-family: 'Playfair Display', serif;
    color: var(--gold);
    font-size: 1.1rem;
    letter-spacing: 0.05em;
  }
  .nav-links { display: flex; gap: 2rem; }
  .nav-links a {
    color: rgba(255,255,255,0.75);
    text-decoration: none;
    font-size: 0.82rem;
    font-weight: 500;
    letter-spacing: 0.08em;
    text-transform: uppercase;
    transition: color 0.2s;
  }
  .nav-links a:hover { color: var(--teal-light); }

  /* HERO */
  .hero {
    min-height: 100vh;
    background: var(--navy);
    display: flex; align-items: center;
    padding: 100px 5% 80px;
    position: relative;
    overflow: hidden;
  }
  .hero::before {
    content: '';
    position: absolute; top: -30%; right: -10%;
    width: 600px; height: 600px;
    border-radius: 50%;
    background: radial-gradient(circle, rgba(42,157,143,0.12) 0%, transparent 70%);
    pointer-events: none;
  }
  .hero::after {
    content: '';
    position: absolute; bottom: -10%; left: 20%;
    width: 400px; height: 400px;
    border-radius: 50%;
    background: radial-gradient(circle, rgba(233,196,106,0.06) 0%, transparent 70%);
    pointer-events: none;
  }
  .hero-inner {
    max-width: 900px;
    position: relative; z-index: 1;
  }
  .hero-eyebrow {
    display: inline-flex; align-items: center; gap: 0.6rem;
    background: rgba(42,157,143,0.15);
    border: 1px solid rgba(42,157,143,0.4);
    border-radius: 100px;
    padding: 0.35rem 1rem;
    color: var(--teal-light);
    font-size: 0.78rem;
    font-weight: 600;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    margin-bottom: 1.5rem;
  }
  .hero-eyebrow::before {
    content: '';
    width: 6px; height: 6px;
    background: var(--teal-light);
    border-radius: 50%;
    animation: pulse 2s infinite;
  }
  @keyframes pulse {
    0%, 100% { opacity: 1; }
    50% { opacity: 0.3; }
  }
  .hero h1 {
    font-family: 'Playfair Display', serif;
    font-size: clamp(2.8rem, 6vw, 4.5rem);
    color: var(--white);
    line-height: 1.1;
    margin-bottom: 0.4rem;
  }
  .hero h1 span { color: var(--gold); }
  .hero-sub {
    font-size: clamp(1rem, 2vw, 1.2rem);
    color: var(--teal-light);
    font-weight: 500;
    margin-bottom: 1.5rem;
    letter-spacing: 0.02em;
  }
  .hero-desc {
    color: rgba(255,255,255,0.65);
    font-size: 1rem;
    max-width: 560px;
    margin-bottom: 2.5rem;
    line-height: 1.75;
  }
  .hero-actions { display: flex; gap: 1rem; flex-wrap: wrap; }
  .btn-primary {
    background: var(--teal);
    color: white;
    padding: 0.75rem 1.8rem;
    border-radius: 6px;
    text-decoration: none;
    font-weight: 600;
    font-size: 0.88rem;
    letter-spacing: 0.04em;
    transition: background 0.2s, transform 0.15s;
    display: inline-flex; align-items: center; gap: 0.5rem;
  }
  .btn-primary:hover { background: var(--teal-light); transform: translateY(-1px); }
  .btn-outline {
    border: 1.5px solid rgba(255,255,255,0.3);
    color: rgba(255,255,255,0.8);
    padding: 0.75rem 1.8rem;
    border-radius: 6px;
    text-decoration: none;
    font-weight: 500;
    font-size: 0.88rem;
    letter-spacing: 0.04em;
    transition: border-color 0.2s, color 0.2s;
  }
  .btn-outline:hover { border-color: var(--gold); color: var(--gold); }

  .hero-stats {
    display: flex; gap: 3rem; margin-top: 4rem;
    padding-top: 2.5rem;
    border-top: 1px solid rgba(255,255,255,0.1);
  }
  .stat-num {
    font-family: 'Playfair Display', serif;
    font-size: 2rem;
    color: var(--gold);
    display: block;
    line-height: 1;
  }
  .stat-label {
    font-size: 0.75rem;
    color: rgba(255,255,255,0.5);
    text-transform: uppercase;
    letter-spacing: 0.08em;
    margin-top: 0.3rem;
  }

  /* SECTIONS */
  section { padding: 90px 5%; }
  .section-inner { max-width: 960px; margin: 0 auto; }
  .section-label {
    font-size: 0.72rem;
    font-weight: 700;
    letter-spacing: 0.15em;
    text-transform: uppercase;
    color: var(--teal);
    margin-bottom: 0.6rem;
  }
  .section-title {
    font-family: 'Playfair Display', serif;
    font-size: clamp(1.8rem, 3.5vw, 2.5rem);
    color: var(--navy);
    margin-bottom: 1rem;
    line-height: 1.2;
  }
  .section-intro {
    color: var(--muted);
    max-width: 580px;
    font-size: 0.97rem;
    line-height: 1.75;
    margin-bottom: 3rem;
  }

  /* ABOUT */
  #about { background: var(--white); }
  .about-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 4rem;
    align-items: start;
  }
  .about-text p {
    color: #374151;
    font-size: 0.97rem;
    line-height: 1.8;
    margin-bottom: 1rem;
  }
  .about-highlight {
    background: linear-gradient(135deg, var(--navy) 0%, var(--navy-mid) 100%);
    border-radius: 12px;
    padding: 2rem;
    color: white;
  }
  .about-highlight h3 {
    font-family: 'Playfair Display', serif;
    font-size: 1.1rem;
    color: var(--gold);
    margin-bottom: 1.2rem;
  }
  .highlight-item {
    display: flex; align-items: flex-start; gap: 0.8rem;
    margin-bottom: 1rem;
    font-size: 0.88rem;
    color: rgba(255,255,255,0.8);
    line-height: 1.5;
  }
  .highlight-dot {
    width: 6px; height: 6px;
    background: var(--teal-light);
    border-radius: 50%;
    margin-top: 0.45rem;
    flex-shrink: 0;
  }

  /* SKILLS */
  #skills { background: var(--cream); }
  .skills-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 1.5rem;
  }
  .skill-card {
    background: var(--white);
    border: 1px solid var(--border);
    border-radius: 10px;
    padding: 1.6rem;
    transition: border-color 0.2s, box-shadow 0.2s;
  }
  .skill-card:hover {
    border-color: var(--teal);
    box-shadow: 0 4px 20px rgba(42,157,143,0.1);
  }
  .skill-icon {
    font-size: 1.6rem;
    margin-bottom: 0.8rem;
  }
  .skill-card h3 {
    font-size: 0.88rem;
    font-weight: 700;
    color: var(--navy);
    margin-bottom: 0.6rem;
    letter-spacing: 0.03em;
    text-transform: uppercase;
  }
  .skill-tags { display: flex; flex-wrap: wrap; gap: 0.4rem; }
  .tag {
    background: rgba(42,157,143,0.08);
    color: var(--teal);
    border: 1px solid rgba(42,157,143,0.2);
    padding: 0.2rem 0.6rem;
    border-radius: 100px;
    font-size: 0.75rem;
    font-weight: 500;
  }

  /* EXPERIENCE */
  #experience { background: var(--white); }
  .timeline { position: relative; padding-left: 2rem; }
  .timeline::before {
    content: '';
    position: absolute; left: 0; top: 8px; bottom: 0;
    width: 2px;
    background: linear-gradient(to bottom, var(--teal), transparent);
  }
  .timeline-item {
    position: relative;
    margin-bottom: 3rem;
    padding-left: 2rem;
  }
  .timeline-item::before {
    content: '';
    position: absolute; left: -2rem; top: 8px;
    width: 10px; height: 10px;
    border-radius: 50%;
    background: var(--teal);
    border: 2px solid var(--white);
    box-shadow: 0 0 0 2px var(--teal);
  }
  .timeline-item:first-child::before {
    background: var(--gold);
    box-shadow: 0 0 0 2px var(--gold);
  }
  .job-header {
    display: flex; justify-content: space-between; align-items: flex-start;
    margin-bottom: 0.4rem; flex-wrap: wrap; gap: 0.5rem;
  }
  .job-title {
    font-weight: 700;
    font-size: 1rem;
    color: var(--navy);
  }
  .job-date {
    font-size: 0.78rem;
    font-weight: 600;
    color: var(--teal);
    background: rgba(42,157,143,0.08);
    border: 1px solid rgba(42,157,143,0.2);
    padding: 0.2rem 0.6rem;
    border-radius: 100px;
    white-space: nowrap;
  }
  .job-company {
    font-size: 0.88rem;
    color: var(--muted);
    margin-bottom: 0.8rem;
  }
  .job-bullets { list-style: none; }
  .job-bullets li {
    font-size: 0.9rem;
    color: #374151;
    padding: 0.3rem 0;
    padding-left: 1.2rem;
    position: relative;
    line-height: 1.6;
  }
  .job-bullets li::before {
    content: '→';
    position: absolute; left: 0;
    color: var(--teal);
    font-size: 0.8rem;
  }
  .current-badge {
    display: inline-block;
    background: rgba(233,196,106,0.15);
    border: 1px solid rgba(233,196,106,0.5);
    color: #b8860b;
    font-size: 0.7rem;
    font-weight: 700;
    letter-spacing: 0.08em;
    text-transform: uppercase;
    padding: 0.15rem 0.5rem;
    border-radius: 100px;
    margin-left: 0.5rem;
    vertical-align: middle;
  }

  /* EDUCATION */
  #education { background: var(--cream); }
  .edu-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 1.5rem; }
  .edu-card {
    background: var(--white);
    border: 1px solid var(--border);
    border-radius: 10px;
    padding: 1.8rem;
    transition: border-color 0.2s;
  }
  .edu-card:hover { border-color: var(--teal); }
  .edu-degree {
    font-weight: 700;
    font-size: 0.95rem;
    color: var(--navy);
    margin-bottom: 0.3rem;
  }
  .edu-field {
    font-size: 0.88rem;
    color: var(--teal);
    font-weight: 500;
    margin-bottom: 0.5rem;
  }
  .edu-school {
    font-size: 0.83rem;
    color: var(--muted);
  }
  .edu-year {
    font-size: 0.75rem;
    font-weight: 700;
    color: var(--gold);
    margin-top: 0.8rem;
    letter-spacing: 0.05em;
  }

  /* CONTACT */
  #contact {
    background: var(--navy);
    text-align: center;
  }
  #contact .section-title { color: var(--white); }
  #contact .section-label { color: var(--teal-light); }
  .contact-desc {
    color: rgba(255,255,255,0.6);
    font-size: 0.97rem;
    max-width: 480px;
    margin: 0 auto 2.5rem;
    line-height: 1.75;
  }
  .contact-links { display: flex; justify-content: center; gap: 1rem; flex-wrap: wrap; }
  .contact-link {
    display: inline-flex; align-items: center; gap: 0.5rem;
    background: rgba(255,255,255,0.06);
    border: 1px solid rgba(255,255,255,0.15);
    color: rgba(255,255,255,0.85);
    padding: 0.75rem 1.4rem;
    border-radius: 8px;
    text-decoration: none;
    font-size: 0.88rem;
    font-weight: 500;
    transition: background 0.2s, border-color 0.2s;
  }
  .contact-link:hover {
    background: rgba(42,157,143,0.15);
    border-color: var(--teal);
    color: var(--teal-light);
  }

  /* FOOTER */
  footer {
    background: #07111f;
    text-align: center;
    padding: 1.5rem;
    color: rgba(255,255,255,0.3);
    font-size: 0.78rem;
    letter-spacing: 0.05em;
  }

  /* PROJECTS */
  #projects { background: var(--navy); }
  #projects .section-label { color: var(--teal-light); }
  #projects .section-title { color: var(--white); }
  #projects .section-intro { color: rgba(255,255,255,0.55); }
  .projects-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 1.5rem;
  }
  .project-card {
    background: rgba(255,255,255,0.04);
    border: 1px solid rgba(255,255,255,0.1);
    border-radius: 12px;
    overflow: hidden;
    transition: border-color 0.2s, transform 0.2s;
  }
  .project-card:hover {
    border-color: var(--teal);
    transform: translateY(-3px);
  }
  .project-visual {
    height: 160px;
    display: flex; align-items: center; justify-content: center;
    font-size: 3rem;
    position: relative;
    overflow: hidden;
  }
  .project-visual.cad1 { background: linear-gradient(135deg, #0f2d4a, #1a4a6e); }
  .project-visual.cad2 { background: linear-gradient(135deg, #0d3b2e, #1a6b50); }
  .project-visual.cad3 { background: linear-gradient(135deg, #2d1a0f, #6e3a1a); }
  .project-visual.ann1 { background: linear-gradient(135deg, #0f2d2d, #1a5e5e); }
  .project-visual.ann2 { background: linear-gradient(135deg, #2d2a0f, #6e5e1a); }
  .project-visual svg {
    width: 80px; height: 80px;
    opacity: 0.7;
  }
  .project-body { padding: 1.2rem; }
  .project-cat {
    font-size: 0.68rem;
    font-weight: 700;
    letter-spacing: 0.12em;
    text-transform: uppercase;
    color: var(--teal-light);
    margin-bottom: 0.4rem;
  }
  .project-title {
    font-weight: 700;
    font-size: 0.92rem;
    color: var(--white);
    margin-bottom: 0.5rem;
    line-height: 1.3;
  }
  .project-desc {
    font-size: 0.8rem;
    color: rgba(255,255,255,0.5);
    line-height: 1.6;
    margin-bottom: 0.8rem;
  }
  .project-tags { display: flex; flex-wrap: wrap; gap: 0.3rem; margin-bottom: 0.9rem; }
  .project-tag {
    background: rgba(42,157,143,0.1);
    border: 1px solid rgba(42,157,143,0.25);
    color: var(--teal-light);
    padding: 0.15rem 0.5rem;
    border-radius: 100px;
    font-size: 0.7rem;
    font-weight: 500;
  }
  .project-view-btn {
    display: inline-flex; align-items: center; gap: 0.4rem;
    background: rgba(42,157,143,0.15);
    border: 1px solid rgba(42,157,143,0.4);
    color: var(--teal-light);
    padding: 0.4rem 0.9rem;
    border-radius: 6px;
    font-size: 0.75rem;
    font-weight: 600;
    cursor: pointer;
    transition: background 0.2s, border-color 0.2s;
    letter-spacing: 0.03em;
  }
  .project-view-btn:hover {
    background: rgba(42,157,143,0.3);
    border-color: var(--teal-light);
  }

  /* MODAL */
  .modal-overlay {
    display: none;
    position: fixed; inset: 0;
    background: rgba(0,0,0,0.85);
    z-index: 1000;
    align-items: center; justify-content: center;
    padding: 2rem;
  }
  .modal-overlay.active { display: flex; }
  .modal-box {
    background: #0f1f38;
    border: 1px solid rgba(42,157,143,0.3);
    border-radius: 16px;
    max-width: 820px;
    width: 100%;
    max-height: 90vh;
    overflow-y: auto;
    position: relative;
  }
  .modal-close {
    position: absolute; top: 1rem; right: 1rem;
    background: rgba(255,255,255,0.1);
    border: none; color: white;
    width: 32px; height: 32px;
    border-radius: 50%;
    font-size: 1.1rem;
    cursor: pointer;
    display: flex; align-items: center; justify-content: center;
    transition: background 0.2s;
    z-index: 10;
  }
  .modal-close:hover { background: rgba(255,255,255,0.25); }
  .modal-visual {
    width: 100%;
    height: 300px;
    display: flex; align-items: center; justify-content: center;
    border-radius: 16px 16px 0 0;
    overflow: hidden;
    position: relative;
  }
  .modal-visual svg { width: 260px; height: 260px; }
  .modal-visual-label {
    position: absolute; bottom: 1rem; left: 1rem;
    background: rgba(0,0,0,0.6);
    color: rgba(255,255,255,0.7);
    font-size: 0.7rem;
    font-family: monospace;
    letter-spacing: 0.08em;
    padding: 0.3rem 0.7rem;
    border-radius: 100px;
    border: 1px solid rgba(255,255,255,0.1);
  }
  .modal-content { padding: 2rem; }
  .modal-cat {
    font-size: 0.72rem; font-weight: 700;
    letter-spacing: 0.12em; text-transform: uppercase;
    color: var(--teal-light); margin-bottom: 0.5rem;
  }
  .modal-title {
    font-family: 'Playfair Display', serif;
    font-size: 1.4rem; color: white;
    margin-bottom: 1rem; line-height: 1.3;
  }
  .modal-desc {
    color: rgba(255,255,255,0.65);
    font-size: 0.9rem; line-height: 1.8;
    margin-bottom: 1.2rem;
  }
  .modal-details {
    background: rgba(255,255,255,0.04);
    border: 1px solid rgba(255,255,255,0.08);
    border-radius: 10px;
    padding: 1.2rem;
    margin-bottom: 1.2rem;
  }
  .modal-details h4 {
    font-size: 0.75rem; font-weight: 700;
    text-transform: uppercase; letter-spacing: 0.1em;
    color: var(--gold); margin-bottom: 0.8rem;
  }
  .modal-detail-item {
    display: flex; gap: 0.6rem;
    font-size: 0.83rem; color: rgba(255,255,255,0.7);
    padding: 0.3rem 0; line-height: 1.5;
  }
  .modal-detail-item::before { content: '→'; color: var(--teal); flex-shrink: 0; }
  .modal-tags { display: flex; flex-wrap: wrap; gap: 0.4rem; }
  .project-view-btn {
    display: inline-flex; align-items: center; gap: 0.4rem;
    margin-top: 1rem;
    background: transparent;
    border: 1px solid rgba(42,157,143,0.4);
    color: var(--teal-light);
    padding: 0.4rem 0.9rem;
    border-radius: 6px;
    font-size: 0.78rem;
    font-weight: 600;
    text-decoration: none;
    letter-spacing: 0.03em;
    transition: background 0.2s, border-color 0.2s, color 0.2s;
  }
  .project-view-btn:hover {
    background: rgba(42,157,143,0.15);
    border-color: var(--teal-light);
    color: white;
  }
  .project-visual img {
    width: 100%; height: 100%;
    object-fit: cover;
    transition: transform 0.3s;
  }
  .project-card:hover .project-visual img { transform: scale(1.04); }

  @media (max-width: 768px) {
    .projects-grid { grid-template-columns: 1fr 1fr; }
  }
  @media (max-width: 480px) {
    .projects-grid { grid-template-columns: 1fr; }
  }

  /* RESPONSIVE */
  @media (max-width: 768px) {
    .nav-links { display: none; }
    .about-grid { grid-template-columns: 1fr; gap: 2rem; }
    .skills-grid { grid-template-columns: 1fr 1fr; }
    .edu-grid { grid-template-columns: 1fr; }
    .hero-stats { gap: 2rem; }
  }
  @media (max-width: 480px) {
    .skills-grid { grid-template-columns: 1fr; }
  }
</style>
</head>
<body>

<!-- NAV -->
<nav>
  <div class="nav-logo">S. Olukayode</div>
  <div class="nav-links">
    <a href="#about">About</a>
    <a href="#skills">Skills</a>
    <a href="#projects">Projects</a>
    <a href="#experience">Experience</a>
    <a href="#education">Education</a>
    <a href="#contact">Contact</a>
  </div>
</nav>

<!-- HERO -->
<section class="hero">
  <div class="hero-inner">
    <div class="hero-eyebrow">Available for New Opportunities</div>
    <h1>Segun<br><span>Olukayode</span></h1>
    <p class="hero-sub">CAD Annotation Specialist · AI Training Data · Data Analyst</p>
    <p class="hero-desc">
      Detail-oriented data professional with hands-on experience in CAD modelling, AI training data preparation, and operational reporting. I bring precision and consistency to every technical task.
    </p>
    <div class="hero-actions">
      <a href="mailto:pallyleke@gmail.com" class="btn-primary">✉ Get in Touch</a>
      <a href="#experience" class="btn-outline">View Experience</a>
    </div>
    <div class="hero-stats">
      <div>
        <span class="stat-num">8+</span>
        <span class="stat-label">CAD Tools Proficient</span>
      </div>
      <div>
        <span class="stat-num">MSc</span>
        <span class="stat-label">Supply Chain, Hull</span>
      </div>
      <div>
        <span class="stat-num">C2</span>
        <span class="stat-label">English Proficiency</span>
      </div>
    </div>
  </div>
</section>

<!-- ABOUT -->
<section id="about">
  <div class="section-inner">
    <p class="section-label">Who I Am</p>
    <h2 class="section-title">Data-driven. Detail-obsessed.<br>Technically versatile.</h2>
    <div class="about-grid">
      <div class="about-text">
        <p>
          I'm a CAD Annotation Specialist and Data Analyst with hands-on experience across professional CAD tools, AI training data preparation, and high-volume data operations.
        </p>
        <p>
          My background spans logistics reporting at DHL, precision inventory auditing at RGIS, and independent CAD and annotation work — building expertise across FreeCAD, AutoCAD Mechanical, AutoDesk Inventor, Rhino 3D, VectorWorks, BlenderBIM/Bonsai, LibreCAD, and SolveSpace.
        </p>
        <p>
          I thrive in remote, self-managed environments and bring the same rigour I developed in data operations to every annotation and modelling task I take on.
        </p>
      </div>
      <div class="about-highlight">
        <h3>Core Strengths</h3>
        <div class="highlight-item">
          <span class="highlight-dot"></span>
          <span>Proficient across a wide range of professional CAD and BIM tools</span>
        </div>
        <div class="highlight-item">
          <span class="highlight-dot"></span>
          <span>Experienced in 3D digital asset annotation and AI training data preparation</span>
        </div>
        <div class="highlight-item">
          <span class="highlight-dot"></span>
          <span>Strong data validation and quality assurance discipline from operational roles</span>
        </div>
        <div class="highlight-item">
          <span class="highlight-dot"></span>
          <span>Reliable remote worker with strong written and spoken English (C2)</span>
        </div>
        <div class="highlight-item">
          <span class="highlight-dot"></span>
          <span>MSc-level analytical thinking applied to complex technical tasks</span>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- SKILLS -->
<section id="skills">
  <div class="section-inner">
    <p class="section-label">Capabilities</p>
    <h2 class="section-title">Skills & Tools</h2>
    <p class="section-intro">CAD tools, AI annotation, and data operations — built for professional AI research projects.</p>
    <div class="skills-grid">
      <div class="skill-card">
        <div class="skill-icon">🏗️</div>
        <h3>CAD Modelling Tools</h3>
        <div class="skill-tags">
          <span class="tag">FreeCAD</span>
          <span class="tag">AutoCAD Mechanical</span>
          <span class="tag">AutoDesk Inventor</span>
          <span class="tag">Rhino 3D</span>
          <span class="tag">VectorWorks</span>
          <span class="tag">LibreCAD / QCAD CE</span>
          <span class="tag">SolveSpace</span>
        </div>
      </div>
      <div class="skill-card">
        <div class="skill-icon">🧱</div>
        <h3>BIM & IFC Tools</h3>
        <div class="skill-tags">
          <span class="tag">FreeCAD BIM / IFC</span>
          <span class="tag">BlenderBIM / Bonsai</span>
          <span class="tag">Structural Modelling</span>
          <span class="tag">Digital Twin Assets</span>
          <span class="tag">IFC Standards</span>
        </div>
      </div>
      <div class="skill-card">
        <div class="skill-icon">🤖</div>
        <h3>AI Data Annotation</h3>
        <div class="skill-tags">
          <span class="tag">3D CAD Annotation</span>
          <span class="tag">Digital Asset Refinement</span>
          <span class="tag">Bounding Boxes</span>
          <span class="tag">Semantic Segmentation</span>
          <span class="tag">Point Cloud Labelling</span>
          <span class="tag">Quality Review</span>
        </div>
      </div>
      <div class="skill-card">
        <div class="skill-icon">📊</div>
        <h3>Data & Reporting</h3>
        <div class="skill-tags">
          <span class="tag">SQL</span>
          <span class="tag">IBM Cognos Analytics</span>
          <span class="tag">Data Validation</span>
          <span class="tag">Auditing</span>
          <span class="tag">Process Mapping</span>
        </div>
      </div>
      <div class="skill-card">
        <div class="skill-icon">🗄️</div>
        <h3>HRIS & People Systems</h3>
        <div class="skill-tags">
          <span class="tag">UKG Pro</span>
          <span class="tag">iCIMS ATS</span>
          <span class="tag">Workflow Mapping</span>
          <span class="tag">U.S. HR Compliance</span>
          <span class="tag">System Analysis</span>
        </div>
      </div>
      <div class="skill-card">
        <div class="skill-icon">⚙️</div>
        <h3>Work Style</h3>
        <div class="skill-tags">
          <span class="tag">Remote-Ready</span>
          <span class="tag">Self-Managed</span>
          <span class="tag">Detail-Oriented</span>
          <span class="tag">Analytical Thinking</span>
          <span class="tag">English C2</span>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- PROJECTS -->
<section id="projects">
  <div class="section-inner">
    <p class="section-label">Portfolio</p>
    <h2 class="section-title">Projects & Work Samples</h2>
    <p class="section-intro">A selection of CAD annotation, digital asset work, and data operations projects.</p>
    <div class="projects-grid">

      <!-- PROJECT 1: FreeCAD Mechanical -->
      <div class="project-card">
        <div class="project-visual" style="padding:0; height:180px; overflow:hidden;">
          <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/f/f9/FreeCAD_1.0_Dark_Assembly_Example.png/800px-FreeCAD_1.0_Dark_Assembly_Example.png"
            alt="FreeCAD Mechanical Assembly Annotation"
            onerror="this.parentElement.style.background='linear-gradient(135deg,#0f1f38,#1a3a5c)'; this.style.display='none';">
        </div>
        <div class="project-body">
          <div class="project-cat">CAD Annotation · AI Training</div>
          <div class="project-title">Mechanical Parts Classification — FreeCAD</div>
          <div class="project-desc">Annotated 3D mechanical assemblies in FreeCAD, labelling components, joints, and tolerances to build training datasets for AI recognition models.</div>
          <div class="project-tags">
            <span class="project-tag">FreeCAD</span>
            <span class="project-tag">3D Labelling</span>
            <span class="project-tag">AI Training Data</span>
          </div>
          <a href="https://www.freecad.org/features.php" target="_blank" class="project-view-btn">🔗 View Tool</a>
        </div>
      </div>

      <!-- PROJECT 2: BlenderBIM Structural -->
      <div class="project-card">
        <div class="project-visual" style="padding:0; height:180px; overflow:hidden;">
          <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/a/a2/FreeCAD_1.0_Dark_BIM_Example.png/800px-FreeCAD_1.0_Dark_BIM_Example.png"
            alt="BIM Structural Model Annotation"
            onerror="this.parentElement.style.background='linear-gradient(135deg,#0d3b2e,#1a6b50)'; this.style.display='none';">
        </div>
        <div class="project-body">
          <div class="project-cat">CAD · BIM Annotation</div>
          <div class="project-title">Structural Model Annotation — BlenderBIM</div>
          <div class="project-desc">Applied semantic labels to BIM structural models in BlenderBIM/Bonsai, classifying beams, columns, and slabs to support digital twin development.</div>
          <div class="project-tags">
            <span class="project-tag">BlenderBIM</span>
            <span class="project-tag">FreeCAD BIM/IFC</span>
            <span class="project-tag">Semantic Labels</span>
          </div>
          <a href="https://blenderbim.org/blenderbim/" target="_blank" class="project-view-btn">🔗 View Tool</a>
        </div>
      </div>

      <!-- PROJECT 3: AutoCAD 2D Drawing -->
      <div class="project-card">
        <div class="project-visual" style="padding:0; height:180px; overflow:hidden;">
          <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/1/1e/FreeCAD_1.0_Light_PartDesign_Pozidriv.png/800px-FreeCAD_1.0_Light_PartDesign_Pozidriv.png"
            alt="2D Technical Drawing Annotation"
            onerror="this.parentElement.style.background='linear-gradient(135deg,#2d1a0f,#6e3a1a)'; this.style.display='none';">
        </div>
        <div class="project-body">
          <div class="project-cat">CAD · AutoCAD · VectorWorks</div>
          <div class="project-title">2D Technical Drawing Annotation</div>
          <div class="project-desc">Labelled AutoCAD and VectorWorks technical drawings for AI component recognition, tagging dimensions, tolerances, part references, and assembly notes.</div>
          <div class="project-tags">
            <span class="project-tag">AutoCAD</span>
            <span class="project-tag">VectorWorks</span>
            <span class="project-tag">Dimension Tagging</span>
          </div>
          <a href="https://www.autodesk.com/products/autocad/overview" target="_blank" class="project-view-btn">🔗 View Tool</a>
        </div>
      </div>

      <!-- PROJECT 4: IBM Cognos / DHL -->
      <div class="project-card">
        <div class="project-visual" style="padding:0; height:180px; overflow:hidden; background:linear-gradient(135deg,#0a1f3a,#1a3a5c);">
          <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/8/8f/Cognos-Analytics-11-1-7-dashboard.png/800px-Cognos-Analytics-11-1-7-dashboard.png"
            alt="IBM Cognos Analytics Dashboard"
            onerror="this.parentElement.innerHTML='<div style=\'display:flex;align-items:center;justify-content:center;height:100%;flex-direction:column;gap:0.5rem;\'><span style=\'font-size:2.5rem;\'>📊</span><span style=\'font-size:0.7rem;color:rgba(255,255,255,0.4);font-family:monospace;\'>IBM COGNOS ANALYTICS</span></div>'; this.style.display='none';">
        </div>
        <div class="project-body">
          <div class="project-cat">Data Reporting · DHL</div>
          <div class="project-title">Operational KPI Dashboard — IBM Cognos</div>
          <div class="project-desc">Built and maintained recurring operational reports at DHL using IBM Cognos Analytics, tracking throughput, accuracy rates, and workflow efficiency across high-volume logistics shifts.</div>
          <div class="project-tags">
            <span class="project-tag">IBM Cognos</span>
            <span class="project-tag">KPI Reporting</span>
            <span class="project-tag">Data Validation</span>
            <span class="project-tag">Logistics Ops</span>
          </div>
          <a href="https://www.ibm.com/products/cognos-analytics" target="_blank" class="project-view-btn">🔗 View Tool</a>
        </div>
      </div>

      <!-- PROJECT 5: RGIS Inventory -->
      <div class="project-card">
        <div class="project-visual" style="padding:0; height:180px; overflow:hidden;">
          <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/5/5e/Barcode_Scanner_in_Warehouse.jpg/800px-Barcode_Scanner_in_Warehouse.jpg"
            alt="Inventory Audit at RGIS"
            onerror="this.parentElement.style.background='linear-gradient(135deg,#0d2a1f,#1a4a35)'; this.style.display='none';">
        </div>
        <div class="project-body">
          <div class="project-cat">Inventory Audit · RGIS</div>
          <div class="project-title">Inventory Discrepancy Reporting System</div>
          <div class="project-desc">Designed structured audit workflows at RGIS to capture stock variances across client sites. Identified discrepancy root causes and produced resolution reports improving data integrity.</div>
          <div class="project-tags">
            <span class="project-tag">Inventory Auditing</span>
            <span class="project-tag">Variance Analysis</span>
            <span class="project-tag">Data Integrity</span>
            <span class="project-tag">Reporting</span>
          </div>
          <a href="https://www.rgis.com/services/" target="_blank" class="project-view-btn">🔗 View Organisation</a>
        </div>
      </div>

      <!-- PROJECT 6: UKG Pro / iCIMS -->
      <div class="project-card">
        <div class="project-visual" style="padding:0; height:180px; overflow:hidden;">
          <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/0/05/HR_Management_Software_Screenshot.png/800px-HR_Management_Software_Screenshot.png"
            alt="UKG Pro HRIS Workflow"
            onerror="this.parentElement.style.background='linear-gradient(135deg,#1a1030,#2d1a50)'; this.parentElement.innerHTML+='<div style=\'display:flex;align-items:center;justify-content:center;height:100%;flex-direction:column;gap:0.6rem;padding:1rem;\'><div style=\'display:flex;gap:10px;width:90%;\'><div style=\'flex:1;background:rgba(233,196,106,0.1);border:1px solid rgba(233,196,106,0.4);border-radius:8px;padding:10px;\'><div style=\'font-size:0.6rem;color:#e9c46a;font-family:monospace;font-weight:700;margin-bottom:6px;\'>UKG PRO</div><div style=\'font-size:0.55rem;color:rgba(255,255,255,0.5);font-family:monospace;line-height:1.6;\'>✓ Onboarding<br>✓ Audit Log<br>✓ Compliance</div></div><div style=\'display:flex;align-items:center;color:rgba(255,255,255,0.3);font-size:0.9rem;\'>⇄</div><div style=\'flex:1;background:rgba(42,157,143,0.1);border:1px solid rgba(42,157,143,0.4);border-radius:8px;padding:10px;\'><div style=\'font-size:0.6rem;color:#2a9d8f;font-family:monospace;font-weight:700;margin-bottom:6px;\'>iCIMS ATS</div><div style=\'font-size:0.55rem;color:rgba(255,255,255,0.5);font-family:monospace;line-height:1.6;\'>✓ Pipeline<br>✓ Screening<br>✓ Workflow</div></div></div></div>'; this.style.display='none';">
        </div>
        <div class="project-body">
          <div class="project-cat">HRIS · People Systems</div>
          <div class="project-title">UKG Pro & iCIMS Workflow Documentation</div>
          <div class="project-desc">Mapped end-to-end HRIS workflows in UKG Pro and iCIMS ATS — covering onboarding, data validation, and compliance audit trails — to support system analysis and process improvement.</div>
          <div class="project-tags">
            <span class="project-tag">UKG Pro</span>
            <span class="project-tag">iCIMS ATS</span>
            <span class="project-tag">Workflow Docs</span>
            <span class="project-tag">Compliance</span>
          </div>
          <a href="https://www.ukg.com/solutions/hcm-software/hr-management" target="_blank" class="project-view-btn">🔗 View Tool</a>
        </div>
      </div>

      <!-- PROJECT 7: Object Detection -->
      <div class="project-card">
        <div class="project-visual" style="padding:0; height:180px; overflow:hidden;">
          <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/3/38/Detected-with-YOLO--Schreibtisch-mit-Objekten.jpg/800px-Detected-with-YOLO--Schreibtisch-mit-Objekten.jpg"
            alt="Object Detection Bounding Box Annotation"
            onerror="this.parentElement.style.background='linear-gradient(135deg,#0f2d2d,#1a5e5e)'; this.style.display='none';">
        </div>
        <div class="project-body">
          <div class="project-cat">AI Annotation · Image Data</div>
          <div class="project-title">Object Detection Dataset Preparation</div>
          <div class="project-desc">Prepared and reviewed image annotation datasets for object detection models, applying bounding boxes, polygon masks, and class labels across thousands of frames.</div>
          <div class="project-tags">
            <span class="project-tag">Bounding Boxes</span>
            <span class="project-tag">Polygon Masks</span>
            <span class="project-tag">Class Labelling</span>
          </div>
          <a href="https://paperswithcode.com/task/object-detection" target="_blank" class="project-view-btn">🔗 View Reference</a>
        </div>
      </div>

      <!-- PROJECT 8: Point Cloud -->
      <div class="project-card">
        <div class="project-visual" style="padding:0; height:180px; overflow:hidden;">
          <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/4/4c/Point_cloud_of_a_statue.png/800px-Point_cloud_of_a_statue.png"
            alt="3D Point Cloud Labelling"
            onerror="this.parentElement.style.background='linear-gradient(135deg,#2d2a0f,#6e5e1a)'; this.style.display='none';">
        </div>
        <div class="project-body">
          <div class="project-cat">AI Training Data · QA</div>
          <div class="project-title">Point Cloud & 3D Object Labelling</div>
          <div class="project-desc">Classified and labelled 3D point cloud objects for autonomous systems training, with quality assurance review at each annotation stage to ensure label accuracy.</div>
          <div class="project-tags">
            <span class="project-tag">Point Cloud</span>
            <span class="project-tag">3D Object Labels</span>
            <span class="project-tag">QA Review</span>
          </div>
          <a href="https://paperswithcode.com/task/3d-point-cloud-classification" target="_blank" class="project-view-btn">🔗 View Reference</a>
        </div>
      </div>

    </div>
  </div>
</section>

<!-- EXPERIENCE -->
<section id="experience">
  <div class="section-inner">
    <p class="section-label">Career Journey</p>
    <h2 class="section-title">Professional Experience</h2>
    <p class="section-intro">A career built on data precision, structured validation, and technical detail — the same skills that drive quality AI annotation work.</p>
    <div class="timeline">

      <div class="timeline-item">
        <div class="job-header">
          <span class="job-title">CAD Annotation Specialist & Data Analyst <span class="current-badge">Current</span></span>
          <span class="job-date">Apr 2025 – Present</span>
        </div>
        <div class="job-company">Independent Projects · Dallas, Texas, USA</div>
        <ul class="job-bullets">
          <li>Producing annotated 3D CAD models and technical drawings using FreeCAD, AutoCAD Mechanical, Rhino 3D, VectorWorks, BlenderBIM/Bonsai, LibreCAD, and SolveSpace</li>
          <li>Building and refining digital assets to support AI model training workflows, ensuring labelling accuracy and consistency</li>
          <li>Applying structured data validation and quality review processes across annotation deliverables</li>
          <li>Developing HRIS workflow documentation in UKG Pro and iCIMS ATS, supporting U.S. HR compliance analysis</li>
        </ul>
      </div>

      <div class="timeline-item">
        <div class="job-header">
          <span class="job-title">Associate</span>
          <span class="job-date">Sep 2023 – Jan 2025</span>
        </div>
        <div class="job-company">DHL · Manchester, United Kingdom</div>
        <ul class="job-bullets">
          <li>Supported high-volume operations with a focus on data accuracy and reporting integrity</li>
          <li>Generated operational reports using IBM Cognos Analytics</li>
          <li>Conducted data validation and system checks to improve data integrity across teams</li>
          <li>Collaborated cross-functionally to identify and optimise workflow inefficiencies</li>
        </ul>
      </div>

      <div class="timeline-item">
        <div class="job-header">
          <span class="job-title">Inventory Specialist</span>
          <span class="job-date">Dec 2022 – Aug 2023</span>
        </div>
        <div class="job-company">RGIS · Manchester, United Kingdom</div>
        <ul class="job-bullets">
          <li>Executed precision inventory audits with consistently high accuracy rates</li>
          <li>Identified and resolved data discrepancies through structured reporting</li>
          <li>Maintained data integrity across inventory management systems</li>
        </ul>
      </div>

    </div>
  </div>
</section>

<!-- EDUCATION -->
<section id="education">
  <div class="section-inner">
    <p class="section-label">Academic Background</p>
    <h2 class="section-title">Education</h2>
    <p class="section-intro">A foundation in supply chain thinking, sharpened by real-world data and systems experience.</p>
    <div class="edu-grid">
      <div class="edu-card">
        <div class="edu-degree">Master of Science (MSc)</div>
        <div class="edu-field">Logistics & Supply Chain Management</div>
        <div class="edu-school">University of Hull · Hull, United Kingdom</div>
        <div class="edu-year">2024</div>
      </div>
      <div class="edu-card">
        <div class="edu-degree">Bachelor of Science (BSc)</div>
        <div class="edu-field">Agronomy & Crop Science</div>
        <div class="edu-school">Babcock University · Nigeria</div>
        <div class="edu-year">2012</div>
      </div>
    </div>
  </div>
</section>

<!-- CONTACT -->
<section id="contact">
  <div class="section-inner">
    <p class="section-label">Let's Talk</p>
    <h2 class="section-title">Open to New Opportunities</h2>
    <p class="contact-desc">
      Available for CAD annotation, AI training data, and data analyst roles. Remote-ready, detail-oriented, and always open to interesting technical work.
    </p>
    <div class="contact-links">
      <a href="mailto:pallyleke@gmail.com" class="contact-link">✉ pallyleke@gmail.com</a>
      <a href="tel:+14699937632" class="contact-link">📞 +1 (469) 993-7632</a>
      <a href="https://github.com/pallyleke-dev" class="contact-link" target="_blank">🐙 GitHub Profile</a>
    </div>
  </div>
</section>

<footer>
  © 2025 Segun Olukayode · CAD Annotation Specialist · AI Training Data · Dallas, Texas
</footer>

</body>
</html>
