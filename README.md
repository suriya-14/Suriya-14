
<style>
@import url('https://fonts.googleapis.com/css2?family=Space+Mono:wght@400;700&family=Syne:wght@700;800&display=swap');
*{box-sizing:border-box;margin:0;padding:0}
body{background:transparent}
.readme-wrap{font-family:'Space Mono',monospace;background:var(--color-background-primary);border:0.5px solid var(--color-border-tertiary);border-radius:var(--border-radius-lg);overflow:hidden;max-width:680px}
.banner{background:#0d1117;padding:2.5rem 2rem 1.5rem;position:relative;overflow:hidden;min-height:200px}
.grid-bg{position:absolute;inset:0;background-image:linear-gradient(rgba(56,189,248,0.07) 1px,transparent 1px),linear-gradient(90deg,rgba(56,189,248,0.07) 1px,transparent 1px);background-size:32px 32px;animation:gridpan 20s linear infinite}
@keyframes gridpan{0%{background-position:0 0}100%{background-position:32px 32px}}
.dot-glow{position:absolute;width:320px;height:320px;border-radius:50%;background:radial-gradient(circle,rgba(56,189,248,0.13) 0%,transparent 70%);top:-80px;right:-60px;animation:pulse 4s ease-in-out infinite}
@keyframes pulse{0%,100%{transform:scale(1);opacity:0.8}50%{transform:scale(1.15);opacity:1}}
.name-row{position:relative;z-index:2;display:flex;align-items:center;gap:1rem;margin-bottom:0.75rem}
.avatar-ring{width:64px;height:64px;border-radius:50%;border:2px solid #38bdf8;padding:2px;flex-shrink:0;animation:spin-ring 8s linear infinite}
@keyframes spin-ring{0%{border-color:#38bdf8}33%{border-color:#a78bfa}66%{border-color:#34d399}100%{border-color:#38bdf8}}
.avatar-inner{width:100%;height:100%;border-radius:50%;background:linear-gradient(135deg,#1e3a5f,#0f4c75);display:flex;align-items:center;justify-content:center;font-family:'Syne',sans-serif;font-size:22px;font-weight:800;color:#38bdf8}
.name-block h1{font-family:'Syne',sans-serif;font-weight:800;font-size:26px;color:#f0f6fc;letter-spacing:-0.5px;animation:fadein 0.8s ease}
.name-block p{font-size:11px;color:#38bdf8;letter-spacing:2px;text-transform:uppercase;animation:fadein 1s ease}
@keyframes fadein{from{opacity:0;transform:translateX(-12px)}to{opacity:1;transform:translateX(0)}}
.tagline{position:relative;z-index:2;color:#8b949e;font-size:12px;line-height:1.6;max-width:420px;border-left:2px solid #38bdf8;padding-left:0.75rem;margin-top:0.5rem}
.typing{display:inline-block;overflow:hidden;white-space:nowrap;border-right:2px solid #38bdf8;width:0;animation:type 2.5s steps(40,end) 0.3s forwards,blink 0.7s step-end infinite}
@keyframes type{from{width:0}to{width:100%}}
@keyframes blink{0%,100%{border-color:transparent}50%{border-color:#38bdf8}}
.badges-row{position:relative;z-index:2;display:flex;flex-wrap:wrap;gap:0.4rem;margin-top:1rem}
.badge{font-family:'Space Mono',monospace;font-size:10px;padding:3px 10px;border-radius:20px;border:1px solid;animation:popbadge 0.4s ease both}
@keyframes popbadge{from{opacity:0;transform:scale(0.7)}to{opacity:1;transform:scale(1)}}
.badge.blue{background:rgba(56,189,248,0.1);border-color:#38bdf8;color:#38bdf8}
.badge.purple{background:rgba(167,139,250,0.1);border-color:#a78bfa;color:#a78bfa}
.badge.green{background:rgba(52,211,153,0.1);border-color:#34d399;color:#34d399}
.badge.amber{background:rgba(251,191,36,0.1);border-color:#fbbf24;color:#fbbf24}
.content{padding:1.5rem 2rem}
.section{margin-bottom:1.75rem}
.sec-label{font-family:'Syne',sans-serif;font-size:13px;font-weight:700;color:var(--color-text-secondary);text-transform:uppercase;letter-spacing:2px;margin-bottom:0.75rem;display:flex;align-items:center;gap:0.5rem}
.sec-label::after{content:'';flex:1;height:0.5px;background:var(--color-border-tertiary)}
.skill-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(140px,1fr));gap:0.5rem}
.skill-card{background:var(--color-background-secondary);border:0.5px solid var(--color-border-tertiary);border-radius:var(--border-radius-md);padding:0.6rem 0.75rem;display:flex;align-items:center;gap:0.5rem;font-size:12px;color:var(--color-text-primary);transition:border-color 0.2s}
.skill-card:hover{border-color:var(--color-border-primary)}
.skill-dot{width:8px;height:8px;border-radius:50%;flex-shrink:0}
.projects{display:flex;flex-direction:column;gap:0.6rem}
.proj-card{background:var(--color-background-secondary);border:0.5px solid var(--color-border-tertiary);border-radius:var(--border-radius-md);padding:0.75rem 1rem;display:flex;justify-content:space-between;align-items:flex-start;gap:1rem;transition:border-color 0.2s,transform 0.2s}
.proj-card:hover{border-color:var(--color-border-primary);transform:translateX(4px)}
.proj-name{font-size:13px;font-weight:700;color:var(--color-text-primary);margin-bottom:2px}
.proj-desc{font-size:11px;color:var(--color-text-secondary);line-height:1.5}
.proj-tag{font-size:10px;padding:2px 8px;border-radius:10px;border:0.5px solid;white-space:nowrap;flex-shrink:0;margin-top:2px}
.stat-row{display:grid;grid-template-columns:repeat(3,1fr);gap:0.6rem}
.stat-box{background:var(--color-background-secondary);border:0.5px solid var(--color-border-tertiary);border-radius:var(--border-radius-md);padding:0.75rem;text-align:center}
.stat-num{font-family:'Syne',sans-serif;font-size:22px;font-weight:800;color:var(--color-text-primary);display:block;animation:countup 1.5s ease}
.stat-lbl{font-size:10px;color:var(--color-text-secondary);text-transform:uppercase;letter-spacing:1px}
.links-row{display:flex;flex-wrap:wrap;gap:0.5rem}
.link-btn{font-family:'Space Mono',monospace;font-size:11px;padding:5px 14px;border:0.5px solid var(--color-border-secondary);border-radius:var(--border-radius-md);color:var(--color-text-primary);text-decoration:none;background:var(--color-background-primary);transition:background 0.2s,border-color 0.2s;cursor:pointer}
.link-btn:hover{background:var(--color-background-secondary);border-color:var(--color-border-primary)}
.quote-block{border-left:2px solid #38bdf8;padding:0.5rem 0.75rem;background:var(--color-background-secondary);border-radius:0 var(--border-radius-md) var(--border-radius-md) 0;font-size:12px;color:var(--color-text-secondary);line-height:1.7;font-style:italic}
.activity-bar{display:flex;align-items:flex-end;gap:3px;height:40px;margin-top:0.5rem}
.bar{width:18px;background:var(--color-background-tertiary);border-radius:3px 3px 0 0;border:0.5px solid var(--color-border-tertiary);animation:growbar 1s ease both}
@keyframes growbar{from{height:0}to{height:var(--h)}}
</style>

<h2 class="sr-only">Suriya's GitHub profile README preview</h2>

<div class="readme-wrap">
  <div class="banner">
    <div class="grid-bg"></div>
    <div class="dot-glow"></div>
    <div class="name-row">
      <div class="avatar-ring">
        <div class="avatar-inner">S</div>
      </div>
      <div class="name-block">
        <h1>Suriya V G</h1>
        <p>AI &amp; Data Science Engineer</p>
      </div>
    </div>
    <div class="tagline">
      <span class="typing">Building intelligent systems · Coimbatore, India 🇮🇳</span>
    </div>
    <div class="badges-row">
      <span class="badge blue" style="animation-delay:0.1s">B.Tech AI&amp;DS</span>
      <span class="badge purple" style="animation-delay:0.2s">SNS College of Engineering</span>
      <span class="badge green" style="animation-delay:0.3s">Open to Opportunities</span>
      <span class="badge amber" style="animation-delay:0.4s">🏀 District Champion</span>
    </div>
  </div>

  <div class="content">
    <div class="section">
      <div class="sec-label">About</div>
      <p style="font-size:13px;color:var(--color-text-secondary);line-height:1.8">
        Final-year AI &amp; Data Science student building real-world ML systems — from emotion detection to driver safety. Targeting MNC roles as a Machine Learning Engineer. Planning to pursue higher studies in Germany.
      </p>
      <div class="quote-block" style="margin-top:0.75rem">
        "Discipline, ambition, and heart will take you further than talent alone."
      </div>
    </div>

    <div class="section">
      <div class="sec-label">Flagship Projects</div>
      <div class="projects">
        <div class="proj-card">
          <div>
            <div class="proj-name">MicroMind</div>
            <div class="proj-desc">Real-time multi-emotion detection · CNN + MobileNetV3 · 7 emotions · Live OpenCV graphs</div>
          </div>
          <span class="proj-tag" style="border-color:#38bdf8;color:#38bdf8;background:rgba(56,189,248,0.08)">Python · CV</span>
        </div>
        <div class="proj-card">
          <div>
            <div class="proj-name">WakeVision</div>
            <div class="proj-desc">Driver drowsiness detection · EAR calibration · PERCLOS · 5-level gradient · CSV telemetry</div>
          </div>
          <span class="proj-tag" style="border-color:#34d399;color:#34d399;background:rgba(52,211,153,0.08)">OpenCV · ML</span>
        </div>
        <div class="proj-card">
          <div>
            <div class="proj-name">EchoAid</div>
            <div class="proj-desc">Voice AI assistant for elderly &amp; speech-impaired users · MSME Hackathon entry</div>
          </div>
          <span class="proj-tag" style="border-color:#a78bfa;color:#a78bfa;background:rgba(167,139,250,0.08)">Voice AI</span>
        </div>
        <div class="proj-card">
          <div>
            <div class="proj-name">Netflix Analytics Hub</div>
            <div class="proj-desc">5-page interactive Power BI dashboard · genre, ratings, country, release trends</div>
          </div>
          <span class="proj-tag" style="border-color:#fbbf24;color:#fbbf24;background:rgba(251,191,36,0.08)">Power BI</span>
        </div>
      </div>
    </div>

    <div class="section">
      <div class="sec-label">Tech Stack</div>
      <div class="skill-grid">
        <div class="skill-card"><div class="skill-dot" style="background:#38bdf8"></div>Python</div>
        <div class="skill-card"><div class="skill-dot" style="background:#a78bfa"></div>Machine Learning</div>
        <div class="skill-card"><div class="skill-dot" style="background:#34d399"></div>OpenCV</div>
        <div class="skill-card"><div class="skill-dot" style="background:#fbbf24"></div>Power BI</div>
        <div class="skill-card"><div class="skill-dot" style="background:#f87171"></div>PyTorch</div>
        <div class="skill-card"><div class="skill-dot" style="background:#38bdf8"></div>Streamlit</div>
        <div class="skill-card"><div class="skill-dot" style="background:#a78bfa"></div>Git / GitHub</div>
        <div class="skill-card"><div class="skill-dot" style="background:#34d399"></div>Canva / Figma</div>
      </div>
    </div>

    <div class="section">
      <div class="sec-label">Stats</div>
      <div class="stat-row">
        <div class="stat-box">
          <span class="stat-num">9</span>
          <span class="stat-lbl">Repos</span>
        </div>
        <div class="stat-box">
          <span class="stat-num">3+</span>
          <span class="stat-lbl">ML Projects</span>
        </div>
        <div class="stat-box">
          <span class="stat-num">🥇</span>
          <span class="stat-lbl">District Champ</span>
        </div>
      </div>
    </div>

    <div class="section">
      <div class="sec-label">Connect</div>
      <div class="links-row">
        <a class="link-btn" href="https://www.linkedin.com/in/suriya-v-g-">LinkedIn ↗</a>
        <a class="link-btn" href="https://leetcode.com/u/SURIYA_V_G/">LeetCode ↗</a>
        <a class="link-btn" href="mailto:vgsuriya@gmail.com">Email ↗</a>
      </div>
    </div>
  </div>
</div>
