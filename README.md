<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Mikaela Nicole Cando — GitHub Profile</title>
<link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@300;400;500;600;700&family=Fira+Code:wght@400;500&display=swap" rel="stylesheet"/>
<style>
*{margin:0;padding:0;box-sizing:border-box}
:root{
  --purple:#7C3AED;--purple-light:#A855F7;--purple-dark:#4C1D95;
  --glow:#9B59B6;--bg:#080812;--surface:#0F0F23;--card:#161630;
  --border:#2A2A5A;--text:#E8E8FF;--muted:#8888AA;--accent:#C084FC;
}
body{background:var(--bg);color:var(--text);font-family:'Space Grotesk',sans-serif;min-height:100vh;overflow-x:hidden}

/* Stars BG */
body::before{
  content:'';position:fixed;inset:0;
  background:radial-gradient(ellipse at 20% 20%, rgba(124,58,237,0.15) 0%, transparent 60%),
             radial-gradient(ellipse at 80% 80%, rgba(168,85,247,0.1) 0%, transparent 60%);
  pointer-events:none;z-index:0;
}

.container{max-width:900px;margin:0 auto;padding:0 2rem;position:relative;z-index:1}

/* HERO */
.hero{padding:5rem 0 4rem;display:grid;grid-template-columns:1fr auto;gap:3rem;align-items:center}
.hero-badge{display:inline-flex;align-items:center;gap:8px;background:rgba(124,58,237,0.15);border:1px solid rgba(124,58,237,0.3);border-radius:20px;padding:6px 16px;font-size:12px;letter-spacing:0.15em;color:var(--accent);margin-bottom:1.5rem;text-transform:uppercase}
.hero-badge::before{content:'';width:8px;height:8px;background:var(--accent);border-radius:50%;animation:pulse 2s infinite}
@keyframes pulse{0%,100%{opacity:1;transform:scale(1)}50%{opacity:0.5;transform:scale(1.3)}}

h1{font-size:clamp(2rem, 5vw, 3.5rem);font-weight:700;line-height:1.1;margin-bottom:0.5rem}
h1 span{background:linear-gradient(135deg, var(--purple-light), var(--accent));-webkit-background-clip:text;-webkit-text-fill-color:transparent;background-clip:text}

.typewriter{font-family:'Fira Code',monospace;font-size:1.2rem;color:var(--muted);margin-bottom:1.5rem}
.typewriter span{color:var(--accent);border-right:2px solid var(--accent);animation:blink 0.75s step-end infinite}
@keyframes blink{50%{border-color:transparent}}

.hero-desc{color:var(--muted);line-height:1.7;border-left:3px solid var(--purple);padding-left:1rem;margin-bottom:2rem;font-size:0.95rem}

.socials{display:flex;gap:12px;flex-wrap:wrap}
.social-btn{display:flex;align-items:center;justify-content:center;width:44px;height:44px;border-radius:12px;border:1px solid var(--border);background:var(--card);color:var(--muted);text-decoration:none;font-size:18px;transition:all 0.3s;cursor:pointer}
.social-btn:hover{border-color:var(--purple);color:var(--accent);transform:translateY(-3px);box-shadow:0 8px 24px rgba(124,58,237,0.3)}

/* Profile Card */
.profile-card{position:relative;width:240px;flex-shrink:0}
.profile-img-wrap{width:220px;height:280px;border-radius:20px;border:2px solid rgba(124,58,237,0.4);overflow:hidden;position:relative;background:linear-gradient(135deg,#1a1a3e,#2d1b69)}
.profile-placeholder{width:100%;height:100%;display:flex;align-items:center;justify-content:center;font-size:80px;background:linear-gradient(135deg,#1a0533,#2d1b69)}
.open-badge{position:absolute;top:-12px;right:-12px;background:var(--card);border:1px solid rgba(124,58,237,0.4);border-radius:12px;padding:8px 14px;font-size:12px;line-height:1.4}
.open-badge strong{display:block;color:var(--accent);font-weight:600}
.code-tag{position:absolute;bottom:-16px;left:50%;transform:translateX(-50%);background:var(--card);border:1px solid var(--border);border-radius:10px;padding:10px 16px;font-family:'Fira Code',monospace;font-size:11px;color:var(--accent);white-space:nowrap}
.code-tag .kw{color:#7DD3FC}

/* SECTION */
.section{padding:4rem 0}
.section-label{display:flex;align-items:center;gap:12px;margin-bottom:2.5rem;text-transform:uppercase;letter-spacing:0.2em;font-size:13px;color:var(--muted)}
.section-label::before,.section-label::after{content:'';flex:1;height:1px;background:var(--border)}
.section-label span{display:flex;align-items:center;gap:8px}
.dot{width:8px;height:8px;background:var(--purple);border-radius:50%;flex-shrink:0}

/* ABOUT */
.about-text{text-align:center;max-width:680px;margin:0 auto;color:var(--muted);line-height:1.8;font-size:1rem}
.about-text strong{color:var(--text)}

/* SKILLS GRID */
.skills-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(190px,1fr));gap:1.5rem}
.skill-card{background:var(--card);border:1px solid var(--border);border-radius:16px;padding:2rem 1.5rem;text-align:center;transition:all 0.3s;position:relative;overflow:hidden}
.skill-card::before{content:'';position:absolute;inset:0;background:linear-gradient(135deg,rgba(124,58,237,0.05),transparent);opacity:0;transition:opacity 0.3s}
.skill-card:hover{border-color:rgba(124,58,237,0.5);transform:translateY(-4px);box-shadow:0 12px 40px rgba(124,58,237,0.2)}
.skill-card:hover::before{opacity:1}
.skill-icon{font-size:2.5rem;margin-bottom:1rem;display:block}
.skill-card h3{font-size:0.85rem;letter-spacing:0.1em;font-weight:600;color:var(--text);margin-bottom:0.75rem;text-transform:uppercase}
.skill-card p{font-size:0.85rem;color:var(--muted);line-height:1.6}

/* TECH STACK */
.tech-cols{display:grid;grid-template-columns:repeat(3,1fr);gap:2rem}
.tech-group h4{font-size:11px;letter-spacing:0.15em;color:var(--muted);text-transform:uppercase;margin-bottom:1rem;text-align:center}
.tech-items{display:flex;flex-wrap:wrap;gap:10px;justify-content:center}
.tech-badge{display:flex;align-items:center;gap:8px;background:var(--card);border:1px solid var(--border);border-radius:10px;padding:8px 14px;font-size:13px;color:var(--text);transition:all 0.3s}
.tech-badge:hover{border-color:var(--purple);color:var(--accent)}
.tech-icon{width:20px;height:20px;border-radius:4px;display:flex;align-items:center;justify-content:center;font-size:14px;font-weight:bold;flex-shrink:0}

/* PROJECTS */
.projects-grid{display:grid;grid-template-columns:1fr 1fr;gap:1.5rem}
.project-card{background:var(--card);border:1px solid var(--border);border-radius:16px;padding:1.5rem;transition:all 0.3s}
.project-card:hover{border-color:rgba(124,58,237,0.5);transform:translateY(-3px);box-shadow:0 10px 32px rgba(124,58,237,0.15)}
.project-preview{height:120px;background:linear-gradient(135deg,#0d0d2b,#1a1a4e);border-radius:10px;margin-bottom:1rem;display:flex;align-items:center;justify-content:center;font-size:2rem;border:1px solid var(--border)}
.project-card h3{font-size:1.1rem;font-weight:600;margin-bottom:0.5rem;color:var(--text)}
.project-card p{font-size:0.85rem;color:var(--muted);line-height:1.6;margin-bottom:1rem}
.project-tag{display:inline-block;background:rgba(124,58,237,0.15);border:1px solid rgba(124,58,237,0.3);color:var(--accent);font-size:12px;padding:4px 12px;border-radius:20px;text-decoration:none}

/* FOOTER */
.footer{padding:4rem 0;text-align:center;border-top:1px solid var(--border)}
.quote-card{background:var(--card);border:1px solid var(--border);border-radius:16px;padding:2rem;max-width:480px;margin:0 auto 2rem;position:relative}
.quote-mark{position:absolute;top:-16px;left:24px;background:var(--purple);border-radius:8px;width:32px;height:32px;display:flex;align-items:center;justify-content:center;font-size:18px;font-weight:bold;color:white}
.quote-text{color:var(--muted);line-height:1.7;font-style:italic}
.signature{font-family:'Fira Code',monospace;font-size:1.4rem;color:var(--accent);margin-top:1rem}

@media(max-width:700px){
  .hero{grid-template-columns:1fr;text-align:center}
  .profile-card{display:none}
  .tech-cols{grid-template-columns:1fr}
  .projects-grid{grid-template-columns:1fr}
  .socials{justify-content:center}
}
</style>
</head>
<body>
<div class="container">

  <!-- HERO -->
  <section class="hero">
    <div>
      <div class="hero-badge">
        <span>Welcome to my GitHub</span>
      </div>
      <h1>Hi, I'm<br/><span>Mikaela Nicole Cando</span></h1>
      <div class="typewriter">I design, build, and ship<span>&nbsp;</span></div>
      <p class="hero-desc">Turning ideas into digital experiences<br/>that are clean, functional, and user-centered.</p>
      <div class="socials">
        <a class="social-btn" href="mailto:YOUR_EMAIL" title="Email">✉</a>
        <a class="social-btn" href="https://linkedin.com/in/YOUR_LINKEDIN" title="LinkedIn">in</a>
        <a class="social-btn" href="https://YOUR_PORTFOLIO" title="Portfolio">🌐</a>
        <a class="social-btn" href="https://github.com/YOUR_USERNAME" title="GitHub">⌥</a>
      </div>
    </div>
    <div class="profile-card">
      <div class="open-badge">Open to<strong>opportunities ◆</strong></div>
      <div class="profile-img-wrap">
        <div class="profile-placeholder">👩‍💻</div>
      </div>
      <div class="code-tag"><span class="kw">&gt; Building</span> the future,<br/>one line at a time.</div>
    </div>
  </section>

  <!-- ABOUT -->
  <section class="section">
    <div class="section-label"><span><span class="dot"></span> About Me</span></div>
    <p class="about-text">
      I'm a <strong>UI/UX Designer</strong> and Web Developer who enjoys creating clean interfaces, building functional systems, and providing support <strong>that makes a</strong> difference.<br/><br/>
      I blend creativity with logic to deliver digital solutions that are not only beautiful, but also effective.
    </p>
  </section>

  <!-- WHAT I DO -->
  <section class="section" style="padding-top:0">
    <div class="skills-grid">
      <div class="skill-card">
        <span class="skill-icon">🎨</span>
        <h3>UI/UX Design</h3>
        <p>I design intuitive and user-friendly interfaces that provide meaningful experiences.</p>
      </div>
      <div class="skill-card">
        <span class="skill-icon">&lt;/&gt;</span>
        <h3>Web Development</h3>
        <p>I build responsive and functional websites using modern web technologies.</p>
      </div>
      <div class="skill-card">
        <span class="skill-icon">🎧</span>
        <h3>Technical Support</h3>
        <p>I provide basic technical support, troubleshooting, and system navigation assistance.</p>
      </div>
      <div class="skill-card">
        <span class="skill-icon">📁</span>
        <h3>Productivity & Admin Support</h3>
        <p>I help organize, manage, and create digital materials that support productivity.</p>
      </div>
    </div>
  </section>

  <!-- TECH STACK -->
  <section class="section">
    <div class="section-label"><span><span class="dot"></span> Tech Stack</span></div>
    <div class="tech-cols">
      <div class="tech-group">
        <h4>Design Tools</h4>
        <div class="tech-items">
          <div class="tech-badge"><span class="tech-icon" style="background:#1e1e2e">🎨</span>Figma</div>
          <div class="tech-badge"><span class="tech-icon" style="background:#00C4CC">C</span>Canva</div>
          <div class="tech-badge"><span class="tech-icon" style="background:#0055FF">F</span>Framer</div>
          <div class="tech-badge"><span class="tech-icon" style="background:#111">▶</span>CapCut</div>
        </div>
      </div>
      <div class="tech-group">
        <h4>Web Development</h4>
        <div class="tech-items">
          <div class="tech-badge"><span class="tech-icon" style="background:#E34F26;color:white;font-size:11px">H5</span>HTML5</div>
          <div class="tech-badge"><span class="tech-icon" style="background:#1572B6;color:white;font-size:11px">C3</span>CSS3</div>
          <div class="tech-badge"><span class="tech-icon" style="background:#F7DF1E;color:black;font-size:11px">JS</span>JavaScript</div>
          <div class="tech-badge"><span class="tech-icon" style="background:#777BB4;color:white;font-size:11px">P</span>PHP</div>
        </div>
      </div>
      <div class="tech-group">
        <h4>Productivity</h4>
        <div class="tech-items">
          <div class="tech-badge"><span class="tech-icon" style="background:#D83B01;color:white;font-size:10px">M</span>M365</div>
          <div class="tech-badge"><span class="tech-icon" style="background:#4285F4;color:white;font-size:10px">G</span>G Suite</div>
          <div class="tech-badge"><span class="tech-icon" style="background:#111;color:white;font-size:11px">N</span>Notion</div>
        </div>
      </div>
    </div>
  </section>

  <!-- PROJECTS -->
  <section class="section">
    <div class="section-label"><span><span class="dot"></span> Featured Projects</span></div>
    <div class="projects-grid">
      <div class="project-card">
        <div class="project-preview">🚀</div>
        <h3>iSTART</h3>
        <p>UI/UX design, database ERD, and technical documentation for a DOST-related system.</p>
        <a class="project-tag" href="#">DOST Project</a>
      </div>
      <div class="project-card">
        <div class="project-preview">🎓</div>
        <h3>COACH</h3>
        <p>A mentoring platform built as my capstone project with backend logic, database structure, frontend work, and research documentation.</p>
        <a class="project-tag" href="#">Capstone Project</a>
      </div>
    </div>
  </section>

  <!-- FOOTER -->
  <footer class="footer">
    <div class="quote-card">
      <div class="quote-mark">"</div>
      <p class="quote-text">I'm always learning, growing, and building better solutions for the future.</p>
    </div>
    <div class="signature">Mikaela ♡</div>
  </footer>

</div>
</body>
</html>
