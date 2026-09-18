<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Kanak Kushwaha | Neon Portfolio</title>
  <style>
    :root {
      --bg: #060816;
      --bg-2: #0c1224;
      --panel: rgba(11, 17, 33, 0.78);
      --panel-strong: rgba(16, 24, 46, 0.96);
      --line: rgba(96, 255, 214, 0.42);
      --cyan: #6ef2ff;
      --blue: #6aa9ff;
      --pink: #ff4fd8;
      --green: #7cffb2;
      --yellow: #ffe66d;
      --text: #eaf7ff;
      --muted: #b6c7d8;
      --shadow-cyan: 0 0 12px rgba(110, 242, 255, 0.8), 0 0 28px rgba(110, 242, 255, 0.35);
      --shadow-pink: 0 0 12px rgba(255, 79, 216, 0.8), 0 0 28px rgba(255, 79, 216, 0.35);
      --shadow-green: 0 0 12px rgba(124, 255, 178, 0.8), 0 0 28px rgba(124, 255, 178, 0.35);
    }

    * { box-sizing: border-box; }

    html {
      scroll-behavior: smooth;
    }

    body {
      margin: 0;
      font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
      background:
        radial-gradient(circle at top left, rgba(110, 242, 255, 0.18), transparent 24%),
        radial-gradient(circle at bottom right, rgba(255, 79, 216, 0.18), transparent 22%),
        linear-gradient(135deg, var(--bg) 0%, var(--bg-2) 35%, #070b14 100%);
      color: var(--text);
      min-height: 100vh;
      letter-spacing: 0.02em;
    }

    body::before {
      content: "";
      position: fixed;
      inset: 0;
      background-image: linear-gradient(rgba(255,255,255,0.04) 1px, transparent 1px), linear-gradient(90deg, rgba(255,255,255,0.04) 1px, transparent 1px);
      background-size: 32px 32px;
      mask-image: radial-gradient(circle at center, black 50%, transparent 100%);
      pointer-events: none;
    }

    .container {
      width: min(1100px, calc(100% - 32px));
      margin: 40px auto;
      padding: 22px;
      background: rgba(10, 15, 28, 0.75);
      border: 1px solid rgba(110, 242, 255, 0.45);
      border-radius: 24px;
      box-shadow: 0 0 0 1px rgba(255, 79, 216, 0.2), 0 0 22px rgba(110, 242, 255, 0.15), inset 0 0 30px rgba(110, 242, 255, 0.05);
      backdrop-filter: blur(8px);
      position: relative;
      overflow: hidden;
    }

    .container::before {
      content: "";
      position: absolute;
      inset: -40% auto auto -15%;
      width: 340px;
      height: 340px;
      background: radial-gradient(circle, rgba(110,242,255,0.22), transparent 65%);
      pointer-events: none;
    }

    .header {
      position: relative;
      z-index: 1;
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 24px;
      padding: 12px 8px 28px;
      border-bottom: 1px solid rgba(255,255,255,0.08);
    }

    .title-wrap {
      max-width: 700px;
    }

    .eyebrow {
      display: inline-block;
      margin-bottom: 10px;
      padding: 6px 12px;
      color: var(--cyan);
      border: 1px solid rgba(110,242,255,0.7);
      border-radius: 999px;
      font-size: 0.76rem;
      text-transform: uppercase;
      letter-spacing: 0.14em;
      background: rgba(110, 242, 255, 0.08);
      box-shadow: var(--shadow-cyan);
    }

    h1 {
      margin: 0;
      font-size: clamp(2.4rem, 5vw, 4.2rem);
      line-height: 1.05;
      letter-spacing: -0.04em;
      color: var(--text);
      text-shadow: 0 0 18px rgba(110, 242, 255, 0.42);
    }

    .highlight {
      background: linear-gradient(120deg, var(--cyan), var(--pink), var(--green));
      -webkit-background-clip: text;
      background-clip: text;
      color: transparent;
      text-shadow: none;
    }

    .subtext {
      margin: 16px 0 0;
      font-size: 1.06rem;
      color: var(--muted);
      line-height: 1.7;
      max-width: 760px;
    }

    .status-badge {
      display: inline-flex;
      align-items: center;
      justify-content: center;
      min-width: 168px;
      padding: 14px 18px;
      border-radius: 16px;
      color: var(--green);
      border: 1px solid rgba(124, 255, 178, 0.7);
      background: rgba(124, 255, 178, 0.08);
      font-weight: 700;
      letter-spacing: 0.08em;
      text-transform: uppercase;
      box-shadow: var(--shadow-green);
      white-space: nowrap;
    }

    section {
      position: relative;
      z-index: 1;
      padding: 30px 8px 0;
    }

    .section-title {
      margin: 0 0 18px;
      font-size: 1.12rem;
      text-transform: uppercase;
      letter-spacing: 0.18em;
      color: var(--cyan);
      text-shadow: var(--shadow-cyan);
    }

    .about-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
      gap: 18px;
      list-style: none;
      padding: 0;
      margin: 0;
    }

    .about-grid li {
      background: rgba(15, 23, 38, 0.72);
      border: 1px solid rgba(110, 242, 255, 0.24);
      border-radius: 16px;
      padding: 18px 16px;
      color: var(--muted);
      box-shadow: inset 0 0 20px rgba(110, 242, 255, 0.04), 0 0 18px rgba(110, 242, 255, 0.04);
    }

    .about-grid strong {
      display: block;
      color: var(--text);
      margin-bottom: 8px;
      font-size: 0.82rem;
      letter-spacing: 0.08em;
      text-transform: uppercase;
    }

    .skills-wrap {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
      gap: 18px;
    }

    .skill-box {
      background: rgba(12, 20, 35, 0.82);
      border: 1px solid rgba(255, 79, 216, 0.28);
      border-radius: 18px;
      padding: 18px 18px 16px;
      box-shadow: 0 0 18px rgba(255, 79, 216, 0.08);
    }

    .skill-box h3 {
      margin: 0 0 14px;
      font-size: 0.96rem;
      color: var(--pink);
      letter-spacing: 0.1em;
      text-transform: uppercase;
    }

    .pill-list {
      display: flex;
      flex-wrap: wrap;
      gap: 10px;
    }

    .pill {
      display: inline-block;
      padding: 8px 12px;
      border-radius: 999px;
      background: rgba(110, 242, 255, 0.08);
      border: 1px solid rgba(110, 242, 255, 0.34);
      color: var(--text);
      font-size: 0.88rem;
      box-shadow: var(--shadow-cyan);
    }

    .projects {
      display: grid;
      gap: 20px;
    }

    .project-card {
      background: linear-gradient(180deg, rgba(14, 22, 38, 0.88), rgba(12, 18, 32, 0.82));
      border: 1px solid rgba(110,242,255,0.25);
      border-radius: 20px;
      padding: 22px 20px;
      box-shadow: inset 0 0 25px rgba(110,242,255,0.04), 0 0 18px rgba(110,242,255,0.05);
    }

    .project-card h3 {
      margin: 0 0 10px;
      font-size: clamp(1.15rem, 2.5vw, 1.7rem);
      color: var(--text);
      text-shadow: 0 0 12px rgba(110,242,255,0.28);
    }

    .project-card p {
      margin: 0 0 14px;
      color: var(--muted);
      line-height: 1.7;
    }

    .tech {
      display: flex;
      flex-wrap: wrap;
      gap: 8px;
      margin: 12px 0 0;
    }

    .tech span {
      font-size: 0.8rem;
      padding: 7px 10px;
      border-radius: 999px;
      background: rgba(255, 79, 216, 0.08);
      border: 1px solid rgba(255,79,216,0.28);
      color: #ffd9f7;
      box-shadow: var(--shadow-pink);
    }

    ul.highlights {
      margin: 14px 0 0;
      padding-left: 18px;
      color: var(--muted);
      line-height: 1.8;
    }

    @media (max-width: 720px) {
      .header {
        flex-direction: column;
        align-items: flex-start;
      }

      .status-badge {
        min-width: auto;
      }
    }
  </style>
</head>
<body>
  <div class="container">
    <header class="header">
      <div class="title-wrap">
        <div class="eyebrow">AI & ML Student</div>
        <h1>Hi, I'm <span class="highlight">Kanak Kushwaha</span></h1>
        <p class="subtext">
          B.Tech Artificial Intelligence & Machine Learning student at Pranveer Singh Institute of Technology,
          focused on building practical solutions with Python, Machine Learning, and Data Science.
        </p>
      </div>
      <div class="status-badge">Open to Internships</div>
    </header>

    <section>
      <h2 class="section-title">About Me</h2>
      <ul class="about-grid">
        <li><strong>Education</strong>B.Tech in Artificial Intelligence & Machine Learning | 2024–2028</li>
        <li><strong>Focus</strong>Python, Machine Learning, Data Science, and AI</li>
        <li><strong>Growth</strong>Strengthening DSA, SQL, and software development</li>
        <li><strong>Goal</strong>AI/ML Engineering and Internship opportunities</li>
      </ul>
    </section>

    <section>
      <h2 class="section-title">Technical Skills</h2>
      <div class="skills-wrap">
        <div class="skill-box">
          <h3>Programming</h3>
          <div class="pill-list">
            <span class="pill">Python</span>
            <span class="pill">SQL</span>
          </div>
        </div>

        <div class="skill-box">
          <h3>AI / ML</h3>
          <div class="pill-list">
            <span class="pill">Machine Learning</span>
            <span class="pill">NLP</span>
            <span class="pill">Data Analysis</span>
          </div>
        </div>

        <div class="skill-box">
          <h3>Web</h3>
          <div class="pill-list">
            <span class="pill">Flask</span>
            <span class="pill">Django</span>
            <span class="pill">HTML</span>
            <span class="pill">CSS</span>
          </div>
        </div>

        <div class="skill-box">
          <h3>Tools</h3>
          <div class="pill-list">
            <span class="pill">Git</span>
            <span class="pill">GitHub</span>
            <span class="pill">ArduPilot SITL</span>
            <span class="pill">DroneKit</span>
            <span class="pill">MAVLink</span>
            <span class="pill">WebSockets</span>
          </div>
        </div>
      </div>
    </section>

    <section>
      <h2 class="section-title">Projects</h2>
      <div class="projects">
        <article class="project-card">
          <h3>DroneShieldX</h3>
          <p>
            A drone cybersecurity testbed designed for experimenting with and analyzing drone communication and security scenarios.
          </p>
          <div class="tech">
            <span>Python</span>
            <span>Django</span>
            <span>ArduPilot SITL</span>
            <span>DroneKit</span>
            <span>MAVLink</span>
            <span>WebSockets</span>
          </div>
        </article>

        <article class="project-card">
          <h3>DroneShieldX — Drone Cybersecurity Testbed</h3>
          <p>
            A cybersecurity research and education testbed for simulating drone security scenarios using ArduPilot SITL and MAVLink,
            with integrated detection, defense, and real-time monitoring.
          </p>
          <div class="tech">
            <span>Python</span>
            <span>Django</span>
            <span>ArduPilot SITL</span>
            <span>DroneKit</span>
            <span>MAVLink</span>
            <span>WebSockets</span>
            <span>Figma</span>
            <span>Vercel</span>
          </div>
          <ul class="highlights">
            <li>Simulated drone security scenarios in a controlled environment</li>
            <li>Intrusion and anomaly detection mechanisms</li>
            <li>GPS spoofing and communication-threat detection</li>
            <li>Real-time drone status, threat, and alert monitoring</li>
            <li>Responsive web dashboard for security visualization</li>
          </ul>
        </article>
      </div>
    </section>
  </div>
</body>
</html>

