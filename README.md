<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Mohammad Zisadul Islam | SOC Analyst GitHub README</title>
<link href="https://fonts.googleapis.com/css2?family=Share+Tech+Mono&family=Orbitron:wght@400;700;900&family=Rajdhani:wght@300;400;600;700&display=swap" rel="stylesheet"/>
<style>
  :root {
    --bg:      #020b0f;
    --surface: #041520;
    --border:  #0d3d55;
    --accent:  #00ffe1;
    --accent2: #00a8ff;
    --danger:  #ff2e4c;
    --warn:    #ffb800;
    --text:    #c0dde8;
    --muted:   #3d6575;
    --green:   #00ff88;
    --glow:    0 0 18px rgba(0,255,225,0.35);
    --glow2:   0 0 30px rgba(0,168,255,0.2);
  }
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
  body {
    background: var(--bg);
    color: var(--text);
    font-family: 'Rajdhani', sans-serif;
    font-size: 16px;
    line-height: 1.6;
    min-height: 100vh;
    overflow-x: hidden;
    position: relative;
  }
  body::before {
    content: '';
    position: fixed; inset: 0;
    background: repeating-linear-gradient(0deg, transparent, transparent 2px, rgba(0,0,0,0.06) 2px, rgba(0,0,0,0.06) 4px);
    pointer-events: none; z-index: 999;
  }
  body::after {
    content: '';
    position: fixed; inset: 0;
    background-image:
      linear-gradient(rgba(0,255,225,0.03) 1px, transparent 1px),
      linear-gradient(90deg, rgba(0,255,225,0.03) 1px, transparent 1px);
    background-size: 40px 40px;
    pointer-events: none; z-index: 0;
  }
  .page { max-width: 900px; margin: 0 auto; padding: 40px 24px 80px; position: relative; z-index: 1; }

  /* ── HEADER ── */
  .header { text-align: center; padding: 50px 0 40px; }
  .header-top-line {
    font-family: 'Share Tech Mono', monospace;
    font-size: 11px; color: var(--muted);
    letter-spacing: 4px; text-transform: uppercase;
    margin-bottom: 20px;
    animation: fadeIn 0.6s ease both;
  }
  .avatar-ring {
    width: 140px; height: 140px;
    border-radius: 50%; margin: 0 auto 28px;
    position: relative; animation: fadeIn 0.8s ease both 0.1s;
  }
  .avatar-ring::before, .avatar-ring::after {
    content: ''; position: absolute; inset: -5px;
    border-radius: 50%; border: 2px solid transparent;
  }
  .avatar-ring::before { border-top-color: var(--accent); border-right-color: var(--accent); animation: spin 3s linear infinite; }
  .avatar-ring::after  { border-bottom-color: var(--accent2); border-left-color: var(--accent2); animation: spin 4s linear infinite reverse; inset: -10px; }
  @keyframes spin { to { transform: rotate(360deg); } }
  .avatar-inner {
    width: 100%; height: 100%; border-radius: 50%;
    background: linear-gradient(135deg, #041a28, #0a2f45);
    border: 2px solid var(--border);
    display: flex; align-items: center; justify-content: center;
    font-size: 56px;
    box-shadow: var(--glow), inset 0 0 30px rgba(0,255,225,0.05);
  }
  .name {
    font-family: 'Orbitron', sans-serif;
    font-size: clamp(20px, 4.5vw, 36px);
    font-weight: 900; letter-spacing: 2px; text-transform: uppercase;
    background: linear-gradient(90deg, var(--accent), var(--accent2), var(--accent));
    background-size: 200%;
    -webkit-background-clip: text; -webkit-text-fill-color: transparent;
    animation: shimmer 3s linear infinite, fadeIn 0.8s ease both 0.2s;
    margin-bottom: 8px;
  }
  @keyframes shimmer { to { background-position: 200% center; } }
  .role { font-family: 'Share Tech Mono', monospace; font-size: 13px; color: var(--accent); letter-spacing: 4px; text-transform: uppercase; animation: fadeIn 0.8s ease both 0.3s; margin-bottom: 20px; }
  .typing-wrap { font-family: 'Share Tech Mono', monospace; font-size: 14px; color: var(--accent2); animation: fadeIn 0.8s ease both 0.4s; min-height: 22px; }
  .cursor { display: inline-block; width: 2px; height: 14px; background: var(--accent); vertical-align: middle; animation: blink 0.8s step-end infinite; }
  @keyframes blink { 50% { opacity: 0; } }

  .badges { display: flex; flex-wrap: wrap; gap: 10px; justify-content: center; margin: 28px 0 0; animation: fadeIn 0.8s ease both 0.5s; }
  .badge { font-family: 'Share Tech Mono', monospace; font-size: 11px; padding: 5px 14px; border-radius: 3px; text-transform: uppercase; letter-spacing: 1.5px; border: 1px solid; transition: box-shadow 0.2s; cursor: default; }
  .badge:hover { box-shadow: var(--glow); }
  .badge-cyan  { color: var(--accent);  border-color: var(--accent);  background: rgba(0,255,225,0.06); }
  .badge-blue  { color: var(--accent2); border-color: var(--accent2); background: rgba(0,168,255,0.06); }
  .badge-green { color: var(--green);   border-color: var(--green);   background: rgba(0,255,136,0.06); }
  .badge-red   { color: var(--danger);  border-color: var(--danger);  background: rgba(255,46,76,0.06); }

  /* ── SECTION ── */
  .section { margin-top: 48px; animation: fadeIn 0.6s ease both; }
  .section-header { display: flex; align-items: center; gap: 12px; margin-bottom: 20px; }
  .section-icon { font-size: 18px; }
  .section-title { font-family: 'Orbitron', sans-serif; font-size: 13px; font-weight: 700; letter-spacing: 3px; text-transform: uppercase; color: var(--accent); }
  .section-line { flex: 1; height: 1px; background: linear-gradient(90deg, var(--border), transparent); }

  /* ── TERMINAL ── */
  .terminal { background: #010c14; border: 1px solid var(--border); border-radius: 6px; overflow: hidden; box-shadow: var(--glow2); }
  .terminal-bar { background: #041624; padding: 9px 14px; display: flex; align-items: center; gap: 8px; border-bottom: 1px solid var(--border); }
  .dot { width: 10px; height: 10px; border-radius: 50%; }
  .dot-r { background: var(--danger); } .dot-y { background: var(--warn); } .dot-g { background: var(--green); }
  .terminal-title { font-family: 'Share Tech Mono', monospace; font-size: 11px; color: var(--muted); margin-left: auto; margin-right: auto; letter-spacing: 2px; }
  .terminal-body { padding: 20px 22px; font-family: 'Share Tech Mono', monospace; font-size: 13px; line-height: 2; }
  .t-prompt { color: var(--accent); } .t-cmd { color: #fff; } .t-out { color: var(--text); }
  .t-key { color: var(--accent2); } .t-val { color: var(--green); } .t-comment { color: var(--muted); }

  /* ── STATS ── */
  .stats-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(165px, 1fr)); gap: 16px; }
  .stat-card { background: var(--surface); border: 1px solid var(--border); border-radius: 6px; padding: 20px 18px; text-align: center; position: relative; overflow: hidden; transition: border-color 0.2s, box-shadow 0.2s; }
  .stat-card::before { content: ''; position: absolute; top: 0; left: 0; right: 0; height: 2px; background: linear-gradient(90deg, var(--accent), var(--accent2)); }
  .stat-card:hover { border-color: var(--accent); box-shadow: var(--glow); }
  .stat-num { font-family: 'Orbitron', sans-serif; font-size: 28px; font-weight: 900; color: var(--accent); display: block; line-height: 1; margin-bottom: 6px; }
  .stat-label { font-size: 11px; color: var(--muted); letter-spacing: 1px; text-transform: uppercase; font-family: 'Share Tech Mono', monospace; }

  /* ── SKILLS ── */
  .skill-list { display: flex; flex-direction: column; gap: 14px; }
  .skill-row { display: flex; flex-direction: column; gap: 5px; }
  .skill-meta { display: flex; justify-content: space-between; align-items: center; }
  .skill-name { font-family: 'Share Tech Mono', monospace; font-size: 12px; color: var(--text); letter-spacing: 1px; }
  .skill-pct  { font-family: 'Orbitron', monospace; font-size: 11px; color: var(--accent); }
  .bar-track { height: 6px; background: #051821; border-radius: 3px; border: 1px solid var(--border); overflow: hidden; }
  .bar-fill { height: 100%; border-radius: 3px; background: linear-gradient(90deg, var(--accent2), var(--accent)); box-shadow: 0 0 8px rgba(0,255,225,0.4); animation: growBar 1.4s cubic-bezier(.22,1,.36,1) both; animation-delay: var(--d, 0s); }
  @keyframes growBar { from { width: 0 !important; } }

  /* ── TOOLS ── */
  .tools-grid { display: grid; grid-template-columns: repeat(auto-fill, minmax(130px, 1fr)); gap: 12px; }
  .tool-card { background: var(--surface); border: 1px solid var(--border); border-radius: 6px; padding: 16px 12px; text-align: center; transition: border-color 0.2s, box-shadow 0.2s, transform 0.2s; cursor: default; }
  .tool-card:hover { border-color: var(--accent2); box-shadow: var(--glow2); transform: translateY(-2px); }
  .tool-icon { font-size: 24px; margin-bottom: 8px; display: block; }
  .tool-name { font-family: 'Share Tech Mono', monospace; font-size: 11px; color: var(--text); letter-spacing: 0.5px; }
  .tool-cat  { font-size: 10px; color: var(--muted); margin-top: 3px; }

  /* ── CERTS ── */
  .cert-list { display: flex; flex-direction: column; gap: 12px; }
  .cert-card { background: var(--surface); border: 1px solid var(--border); border-radius: 6px; padding: 16px 20px; display: flex; align-items: center; gap: 16px; transition: border-color 0.2s, box-shadow 0.2s; }
  .cert-card:hover { border-color: var(--accent); box-shadow: var(--glow); }
  .cert-badge { width: 46px; height: 46px; border-radius: 8px; display: flex; align-items: center; justify-content: center; font-size: 22px; flex-shrink: 0; border: 1px solid var(--border); }
  .cert-body { flex: 1; }
  .cert-name { font-family: 'Rajdhani', sans-serif; font-weight: 700; font-size: 16px; color: #fff; }
  .cert-issuer { font-family: 'Share Tech Mono', monospace; font-size: 11px; color: var(--muted); margin-top: 2px; }
  .cert-status { font-family: 'Share Tech Mono', monospace; font-size: 10px; letter-spacing: 1px; text-transform: uppercase; padding: 3px 10px; border-radius: 3px; border: 1px solid; }
  .cert-active  { color: var(--green); border-color: var(--green); background: rgba(0,255,136,0.06); }
  .cert-in-prog { color: var(--warn);  border-color: var(--warn);  background: rgba(255,184,0,0.06); }

  /* ── EDUCATION ── */
  .edu-list { display: flex; flex-direction: column; gap: 14px; }
  .edu-card { background: var(--surface); border: 1px solid var(--border); border-radius: 6px; padding: 18px 22px; border-left: 3px solid var(--accent2); transition: box-shadow 0.2s; }
  .edu-card:hover { box-shadow: var(--glow2); }
  .edu-degree { font-family: 'Rajdhani', sans-serif; font-weight: 700; font-size: 16px; color: #fff; }
  .edu-inst   { font-family: 'Share Tech Mono', monospace; font-size: 11px; color: var(--accent2); margin-top: 3px; }
  .edu-meta   { display: flex; gap: 16px; margin-top: 8px; flex-wrap: wrap; }
  .edu-pill   { font-family: 'Share Tech Mono', monospace; font-size: 10px; padding: 3px 10px; border-radius: 3px; border: 1px solid var(--border); color: var(--text); letter-spacing: 0.5px; }
  .edu-year   { font-family: 'Share Tech Mono', monospace; font-size: 10px; color: var(--muted); margin-left: auto; }

  /* ── PROJECTS ── */
  .proj-list { display: flex; flex-direction: column; gap: 12px; }
  .proj-card { background: var(--surface); border: 1px solid var(--border); border-radius: 6px; padding: 16px 20px; display: flex; gap: 14px; align-items: flex-start; transition: border-color 0.2s, box-shadow 0.2s; }
  .proj-card:hover { border-color: var(--accent); box-shadow: var(--glow); }
  .proj-num { font-family: 'Orbitron', sans-serif; font-size: 10px; color: var(--accent); opacity: 0.5; flex-shrink: 0; padding-top: 3px; }
  .proj-body {}
  .proj-title { font-family: 'Rajdhani', sans-serif; font-weight: 700; font-size: 15px; color: #fff; }
  .proj-desc  { font-family: 'Share Tech Mono', monospace; font-size: 11px; color: var(--muted); margin-top: 4px; line-height: 1.6; }

  /* ── ALERT FEED ── */
  .alert-feed { display: flex; flex-direction: column; gap: 10px; }
  .alert-item { background: var(--surface); border-left: 3px solid; border-radius: 0 6px 6px 0; padding: 12px 16px; display: flex; gap: 12px; align-items: flex-start; font-family: 'Share Tech Mono', monospace; font-size: 12px; border-top: 1px solid var(--border); border-right: 1px solid var(--border); border-bottom: 1px solid var(--border); }
  .alert-high { border-left-color: var(--danger); } .alert-med { border-left-color: var(--warn); } .alert-low { border-left-color: var(--accent2); } .alert-info { border-left-color: var(--green); }
  .alert-sev { font-size: 10px; padding: 2px 7px; border-radius: 3px; white-space: nowrap; letter-spacing: 1px; font-weight: 700; }
  .sev-high { background: rgba(255,46,76,0.15); color: var(--danger); } .sev-med { background: rgba(255,184,0,0.12); color: var(--warn); } .sev-low { background: rgba(0,168,255,0.12); color: var(--accent2); } .sev-info { background: rgba(0,255,136,0.1); color: var(--green); }
  .alert-time { color: var(--muted); white-space: nowrap; margin-left: auto; flex-shrink: 0; }
  .alert-msg { color: var(--text); flex: 1; }

  /* ── HEATMAP ── */
  .heatmap { display: flex; gap: 4px; flex-wrap: wrap; }
  .hm-cell { width: 12px; height: 12px; border-radius: 2px; background: #051821; border: 1px solid rgba(0,255,225,0.06); transition: transform 0.1s; }
  .hm-cell:hover { transform: scale(1.4); }
  .hm-1 { background: rgba(0,255,225,0.2); } .hm-2 { background: rgba(0,255,225,0.4); } .hm-3 { background: rgba(0,255,225,0.65); }
  .hm-4 { background: var(--accent); box-shadow: 0 0 6px var(--accent); }

  /* ── CONNECT ── */
  .connect-grid { display: grid; grid-template-columns: repeat(auto-fill, minmax(150px, 1fr)); gap: 12px; }
  .connect-btn { display: flex; align-items: center; gap: 10px; background: var(--surface); border: 1px solid var(--border); border-radius: 6px; padding: 14px 16px; text-decoration: none; transition: border-color 0.2s, box-shadow 0.2s, transform 0.2s; }
  .connect-btn:hover { border-color: var(--accent); box-shadow: var(--glow); transform: translateY(-2px); }
  .connect-icon { font-size: 20px; }
  .connect-text { font-family: 'Share Tech Mono', monospace; font-size: 11px; color: var(--text); }

  /* ── QUOTE ── */
  .quote-box { border: 1px solid var(--border); border-left: 3px solid var(--accent); background: rgba(0,255,225,0.03); border-radius: 0 6px 6px 0; padding: 16px 22px; font-family: 'Share Tech Mono', monospace; font-size: 13px; color: var(--accent); letter-spacing: 0.5px; }

  /* ── FOOTER ── */
  .footer { text-align: center; padding-top: 60px; font-family: 'Share Tech Mono', monospace; font-size: 11px; color: var(--muted); letter-spacing: 2px; }
  .footer span { color: var(--accent); }

  @keyframes fadeIn { from { opacity: 0; transform: translateY(12px); } to { opacity: 1; transform: none; } }

  @media (max-width: 600px) {
    .stats-grid { grid-template-columns: repeat(2, 1fr); }
    .tools-grid { grid-template-columns: repeat(3, 1fr); }
    .connect-grid { grid-template-columns: repeat(2, 1fr); }
  }
</style>
</head>
<body>
<div class="page">

  <!-- ═══════════════ HEADER ═══════════════ -->
  <header class="header">
    <p class="header-top-line">// SECURITY OPERATIONS CENTER // BLUE TEAM // THREAT DETECTION //</p>

    <div class="avatar-ring">
      <div class="avatar-inner">🛡️</div>
    </div>

    <h1 class="name">Mohammad Zisadul Islam</h1>
    <p class="role">◈ SOC Analyst · Blue Team Junior Analyst · Cybersecurity Professional ◈</p>
    <p class="typing-wrap" id="typing"></p>

    <div class="badges">
      <span class="badge badge-cyan">🟢 Open to Opportunities</span>
      <span class="badge badge-blue">🔵 Blue Team Defender</span>
      <span class="badge badge-green">✅ Blue Team Junior Analyst L1</span>
      <span class="badge badge-red">⚡ Wazuh · ELK · Suricata</span>
      <span class="badge badge-cyan">📍 Dhaka, Bangladesh</span>
    </div>
  </header>

  <!-- ═══════════════ ABOUT / TERMINAL ═══════════════ -->
  <section class="section">
    <div class="section-header">
      <span class="section-icon">💻</span>
      <span class="section-title">Operator Profile</span>
      <div class="section-line"></div>
    </div>
    <div class="terminal">
      <div class="terminal-bar">
        <span class="dot dot-r"></span><span class="dot dot-y"></span><span class="dot dot-g"></span>
        <span class="terminal-title">zisad@soc-ops:~$</span>
      </div>
      <div class="terminal-body">
        <div><span class="t-prompt">➜ </span><span class="t-cmd">cat profile.json</span></div>
        <div class="t-out">{</div>
        <div><span style="padding-left:20px" class="t-key">"name"</span><span class="t-out">: </span><span class="t-val">"Mohammad Zisadul Islam"</span><span class="t-out">,</span></div>
        <div><span style="padding-left:20px" class="t-key">"role"</span><span class="t-out">: </span><span class="t-val">"SOC Analyst | Blue Team Junior Analyst"</span><span class="t-out">,</span></div>
        <div><span style="padding-left:20px" class="t-key">"location"</span><span class="t-out">: </span><span class="t-val">"Golsan 2, Dhaka 1212, Bangladesh"</span><span class="t-out">,</span></div>
        <div><span style="padding-left:20px" class="t-key">"email"</span><span class="t-out">: </span><span class="t-val">"jrzisad@gmail.com"</span><span class="t-out">,</span></div>
        <div><span style="padding-left:20px" class="t-key">"focus"</span><span class="t-out">: [</span><span class="t-val">"Threat Detection"</span><span class="t-out">, </span><span class="t-val">"SIEM Monitoring"</span><span class="t-out">, </span><span class="t-val">"Incident Response"</span><span class="t-out">],</span></div>
        <div><span style="padding-left:20px" class="t-key">"currently"</span><span class="t-out">: </span><span class="t-val">"Building open-source SOC lab · Learning DFIR"</span><span class="t-out">,</span></div>
        <div><span style="padding-left:20px" class="t-key">"education"</span><span class="t-out">: </span><span class="t-val">"BSc CSE @ AIUB | Major: Security"</span></div>
        <div class="t-out">}</div>
        <br/>
        <div><span class="t-prompt">➜ </span><span class="t-cmd">echo $MISSION</span></div>
        <div class="t-comment"># Detect. Investigate. Contain. Harden. Repeat.</div>
        <br/>
        <div><span class="t-prompt">➜ </span><span class="t-cmd">cat summary.txt</span></div>
        <div class="t-out" style="color:var(--text); line-height:1.8; max-width:620px">
          Dedicated cybersecurity professional with hands-on SOC lab experience.<br>
          Proficient in monitoring alerts, analyzing logs, and investigating suspicious<br>
          activities using open-source tools. Passionate about Blue Team operations,<br>
          threat detection, incident response, and defensive cybersecurity practices.
        </div>
      </div>
    </div>
  </section>

  <!-- ═══════════════ SOC METRICS ═══════════════ -->
  <section class="section">
    <div class="section-header">
      <span class="section-icon">📊</span>
      <span class="section-title">Operational Metrics</span>
      <div class="section-line"></div>
    </div>
    <div class="stats-grid">
      <div class="stat-card"><span class="stat-num">3.54</span><span class="stat-label">CGPA / 4.0</span></div>
      <div class="stat-card"><span class="stat-num">2+</span><span class="stat-label">Certs Earned</span></div>
      <div class="stat-card"><span class="stat-num">10+</span><span class="stat-label">Tools Mastered</span></div>
      <div class="stat-card"><span class="stat-num">4+</span><span class="stat-label">Lab Projects Built</span></div>
      <div class="stat-card"><span class="stat-num">CTF</span><span class="stat-label">Blue Team Challenges</span></div>
      <div class="stat-card"><span class="stat-num">24/7</span><span class="stat-label">SOC Lab Running</span></div>
    </div>
  </section>

  <!-- ═══════════════ LIVE ALERT FEED (Simulated) ═══════════════ -->
  <section class="section">
    <div class="section-header">
      <span class="section-icon">🚨</span>
      <span class="section-title">SOC Lab Alert Feed (Simulated)</span>
      <div class="section-line"></div>
    </div>
    <div class="alert-feed">
      <div class="alert-item alert-high">
        <span class="alert-sev sev-high">CRITICAL</span>
        <span class="alert-msg">Wazuh Alert — Rootkit IOC detected | Host: lab-ubuntu01 | Rule ID: 510 | Integrity check failed</span>
        <span class="alert-time">00:02:31</span>
      </div>
      <div class="alert-item alert-high">
        <span class="alert-sev sev-high">HIGH</span>
        <span class="alert-msg">Suricata IDS — ET MALWARE Suspicious User-Agent (curl) outbound | SRC: 10.0.0.15 | DST: 185.220.x.x</span>
        <span class="alert-time">00:14:07</span>
      </div>
      <div class="alert-item alert-med">
        <span class="alert-sev sev-med">MEDIUM</span>
        <span class="alert-msg">ELK SIEM — Brute-force SSH login | 87 failed attempts in 30s | User: root | SRC: 192.168.1.44</span>
        <span class="alert-time">00:29:55</span>
      </div>
      <div class="alert-item alert-low">
        <span class="alert-sev sev-low">LOW</span>
        <span class="alert-msg">ModSecurity WAF — OWASP SQLi attempt blocked | URI: /login.php | Payload: ' OR 1=1 --</span>
        <span class="alert-time">01:08:12</span>
      </div>
      <div class="alert-item alert-info">
        <span class="alert-sev sev-info">INFO</span>
        <span class="alert-msg">YARA scan complete — 0 matches in /tmp | Malware sample classified as benign | Engine: ClamAV</span>
        <span class="alert-time">02:45:00</span>
      </div>
    </div>
  </section>

  <!-- ═══════════════ SKILLS ═══════════════ -->
  <section class="section">
    <div class="section-header">
      <span class="section-icon">⚡</span>
      <span class="section-title">Skill Matrix</span>
      <div class="section-line"></div>
    </div>
    <div class="skill-list">
      <div class="skill-row">
        <div class="skill-meta"><span class="skill-name">SIEM Alert Monitoring (Wazuh / ELK Stack)</span><span class="skill-pct">92%</span></div>
        <div class="bar-track"><div class="bar-fill" style="width:92%; --d:0.1s"></div></div>
      </div>
      <div class="skill-row">
        <div class="skill-meta"><span class="skill-name">Log Analysis & Correlation</span><span class="skill-pct">88%</span></div>
        <div class="bar-track"><div class="bar-fill" style="width:88%; --d:0.2s"></div></div>
      </div>
      <div class="skill-row">
        <div class="skill-meta"><span class="skill-name">Threat Detection · IoA & IoC Analysis</span><span class="skill-pct">85%</span></div>
        <div class="bar-track"><div class="bar-fill" style="width:85%; --d:0.3s"></div></div>
      </div>
      <div class="skill-row">
        <div class="skill-meta"><span class="skill-name">IDS/IPS (Suricata · Snort)</span><span class="skill-pct">82%</span></div>
        <div class="bar-track"><div class="bar-fill" style="width:82%; --d:0.4s"></div></div>
      </div>
      <div class="skill-row">
        <div class="skill-meta"><span class="skill-name">Malware Analysis (YARA Rules)</span><span class="skill-pct">78%</span></div>
        <div class="bar-track"><div class="bar-fill" style="width:78%; --d:0.5s"></div></div>
      </div>
      <div class="skill-row">
        <div class="skill-meta"><span class="skill-name">Incident Investigation & Triage</span><span class="skill-pct">83%</span></div>
        <div class="bar-track"><div class="bar-fill" style="width:83%; --d:0.6s"></div></div>
      </div>
      <div class="skill-row">
        <div class="skill-meta"><span class="skill-name">Network Traffic Analysis</span><span class="skill-pct">80%</span></div>
        <div class="bar-track"><div class="bar-fill" style="width:80%; --d:0.7s"></div></div>
      </div>
      <div class="skill-row">
        <div class="skill-meta"><span class="skill-name">Web Security · WAF (ModSecurity · BunkerWeb)</span><span class="skill-pct">76%</span></div>
        <div class="bar-track"><div class="bar-fill" style="width:76%; --d:0.8s"></div></div>
      </div>
      <div class="skill-row">
        <div class="skill-meta"><span class="skill-name">Documentation & Security Reporting</span><span class="skill-pct">87%</span></div>
        <div class="bar-track"><div class="bar-fill" style="width:87%; --d:0.9s"></div></div>
      </div>
    </div>
  </section>

  <!-- ═══════════════ TOOLS ═══════════════ -->
  <section class="section">
    <div class="section-header">
      <span class="section-icon">🔧</span>
      <span class="section-title">Tools & Technologies</span>
      <div class="section-line"></div>
    </div>
    <div class="tools-grid">
      <div class="tool-card"><span class="tool-icon">🔍</span><span class="tool-name">Wazuh</span><span class="tool-cat">SIEM / HIDS</span></div>
      <div class="tool-card"><span class="tool-icon">🦌</span><span class="tool-name">ELK Stack</span><span class="tool-cat">Log Analytics</span></div>
      <div class="tool-card"><span class="tool-icon">🦈</span><span class="tool-name">Suricata</span><span class="tool-cat">IDS / IPS</span></div>
      <div class="tool-card"><span class="tool-icon">🐷</span><span class="tool-name">Snort</span><span class="tool-cat">IDS / IPS</span></div>
      <div class="tool-card"><span class="tool-icon">🧅</span><span class="tool-name">TheHive</span><span class="tool-cat">IR Platform</span></div>
      <div class="tool-card"><span class="tool-icon">🧠</span><span class="tool-name">Cortex</span><span class="tool-cat">Threat Enrichment</span></div>
      <div class="tool-card"><span class="tool-icon">🔱</span><span class="tool-name">YARA</span><span class="tool-cat">Malware Rules</span></div>
      <div class="tool-card"><span class="tool-icon">🛡️</span><span class="tool-name">ModSecurity</span><span class="tool-cat">WAF</span></div>
      <div class="tool-card"><span class="tool-icon">🕸️</span><span class="tool-name">BunkerWeb</span><span class="tool-cat">Web Security</span></div>
      <div class="tool-card"><span class="tool-icon">🔥</span><span class="tool-name">Iptables</span><span class="tool-cat">Firewall</span></div>
    </div>
  </section>

  <!-- ═══════════════ CERTIFICATIONS ═══════════════ -->
  <section class="section">
    <div class="section-header">
      <span class="section-icon">🏅</span>
      <span class="section-title">Certifications</span>
      <div class="section-line"></div>
    </div>
    <div class="cert-list">
      <div class="cert-card">
        <div class="cert-badge" style="background:rgba(0,255,225,0.05);">🔵</div>
        <div class="cert-body">
          <div class="cert-name">Blue Team Junior Analyst — Level 1</div>
          <div class="cert-issuer">Blue Team Labs Online · SOC Operations</div>
        </div>
        <span class="cert-status cert-active">Active</span>
      </div>
      <div class="cert-card">
        <div class="cert-badge" style="background:rgba(255,46,76,0.05);">🎯</div>
        <div class="cert-body">
          <div class="cert-name">Jr. Penetration Tester</div>
          <div class="cert-issuer">Byte Capsule IT · Offensive Security Fundamentals</div>
        </div>
        <span class="cert-status cert-active">Active</span>
      </div>
      <div class="cert-card">
        <div class="cert-badge" style="background:rgba(255,184,0,0.05);">📘</div>
        <div class="cert-body">
          <div class="cert-name">CompTIA Security+ / SOC-200</div>
          <div class="cert-issuer">Target Certification · In Progress</div>
        </div>
        <span class="cert-status cert-in-prog">Goal</span>
      </div>
    </div>
  </section>

  <!-- ═══════════════ EDUCATION ═══════════════ -->
  <section class="section">
    <div class="section-header">
      <span class="section-icon">🎓</span>
      <span class="section-title">Education</span>
      <div class="section-line"></div>
    </div>
    <div class="edu-list">
      <div class="edu-card">
        <div class="edu-degree">BSc in Computer Science & Engineering</div>
        <div class="edu-inst">American International University – Bangladesh (AIUB)</div>
        <div class="edu-meta">
          <span class="edu-pill">Major: Network Security</span>
          <span class="edu-pill">CGPA: 3.54 / 4.0</span>
          <span class="edu-pill">🟢 Running</span>
          <span class="edu-year">2022 – Present</span>
        </div>
      </div>
      <div class="edu-card">
        <div class="edu-degree">Higher Secondary Certificate (HSC)</div>
        <div class="edu-inst">Madinatul Ulum Model Institute Alim Madrasah, Bandarban</div>
        <div class="edu-meta">
          <span class="edu-pill">GPA: 4.50 / 5.0</span>
          <span class="edu-year">2022</span>
        </div>
      </div>
      <div class="edu-card">
        <div class="edu-degree">Secondary School Certificate (SSC)</div>
        <div class="edu-inst">Madinatul Ulum Model Institute Alim Madrasah, Bandarban</div>
        <div class="edu-meta">
          <span class="edu-pill">GPA: 4.68 / 5.0</span>
          <span class="edu-year">2020</span>
        </div>
      </div>
    </div>
  </section>

  <!-- ═══════════════ PROJECTS ═══════════════ -->
  <section class="section">
    <div class="section-header">
      <span class="section-icon">🚀</span>
      <span class="section-title">Notable Projects & Activities</span>
      <div class="section-line"></div>
    </div>
    <div class="proj-list">
      <div class="proj-card">
        <span class="proj-num">[01]</span>
        <div class="proj-body">
          <div class="proj-title">🏠 Home SOC Lab — Wazuh + ELK Stack</div>
          <div class="proj-desc">Built a full open-source SOC environment from scratch for hands-on SIEM monitoring, alert analysis, log correlation, and threat detection practice in a self-managed lab.</div>
        </div>
      </div>
      <div class="proj-card">
        <span class="proj-num">[02]</span>
        <div class="proj-body">
          <div class="proj-title">🛡️ WAF Deployment — ModSecurity + BunkerWeb</div>
          <div class="proj-desc">Deployed and configured a Web Application Firewall in a test environment to actively defend against OWASP Top 10 threats including SQLi, XSS, and CSRF attacks.</div>
        </div>
      </div>
      <div class="proj-card">
        <span class="proj-num">[03]</span>
        <div class="proj-body">
          <div class="proj-title">🔱 Malware Analysis — YARA Rule Engineering</div>
          <div class="proj-desc">Practiced malware analysis using custom YARA rules to identify, classify, and document malicious samples across various threat categories in isolated sandbox environments.</div>
        </div>
      </div>
      <div class="proj-card">
        <span class="proj-num">[04]</span>
        <div class="proj-body">
          <div class="proj-title">🏴 CTF Challenges — Blue Team & IR Scenarios</div>
          <div class="proj-desc">Completed Capture The Flag challenges focused on Blue Team defense and Incident Response, sharpening skills in log forensics, IOC hunting, and alert triage under pressure.</div>
        </div>
      </div>
      <div class="proj-card">
        <span class="proj-num">[05]</span>
        <div class="proj-body">
          <div class="proj-title">🤝 Active Cybersecurity Community Member</div>
          <div class="proj-desc">Engaged in cybersecurity communities, forums, and knowledge-sharing groups for continuous professional development and staying current with the evolving threat landscape.</div>
        </div>
      </div>
    </div>
  </section>

  <!-- ═══════════════ HEATMAP ═══════════════ -->
  <section class="section">
    <div class="section-header">
      <span class="section-icon">📅</span>
      <span class="section-title">GitHub Activity</span>
      <div class="section-line"></div>
    </div>
    <div class="terminal">
      <div class="terminal-bar">
        <span class="dot dot-r"></span><span class="dot dot-y"></span><span class="dot dot-g"></span>
        <span class="terminal-title">github.com/mohammadzisadul-islam · contributions</span>
      </div>
      <div class="terminal-body">
        <div class="heatmap" id="heatmap"></div>
        <br/>
        <span class="t-comment"># Less &nbsp;&nbsp;</span>
        <span style="display:inline-flex;gap:4px;vertical-align:middle;margin-right:4px">
          <span class="hm-cell"></span><span class="hm-cell hm-1"></span>
          <span class="hm-cell hm-2"></span><span class="hm-cell hm-3"></span><span class="hm-cell hm-4"></span>
        </span>
        <span class="t-comment">More</span>
      </div>
    </div>
  </section>

  <!-- ═══════════════ QUOTE ═══════════════ -->
  <section class="section">
    <div class="quote-box">
      &gt; "With dedication, sincerity, and hard work, I strive to continuously improve my skills<br>
      &nbsp;&nbsp;&nbsp;and contribute to a dynamic team — one detection rule and one alert triage at a time."
    </div>
  </section>

  <!-- ═══════════════ CONNECT ═══════════════ -->
  <section class="section">
    <div class="section-header">
      <span class="section-icon">🔗</span>
      <span class="section-title">Establish Connection</span>
      <div class="section-line"></div>
    </div>
    <div class="connect-grid">
      <a class="connect-btn" href="https://linkedin.com/in/mzisadulislam" target="_blank">
        <span class="connect-icon">💼</span><span class="connect-text">LinkedIn</span>
      </a>
      <a class="connect-btn" href="https://github.com/mohammadzisadul-islam" target="_blank">
        <span class="connect-icon">🐙</span><span class="connect-text">GitHub</span>
      </a>
      <a class="connect-btn" href="mailto:jrzisad@gmail.com">
        <span class="connect-icon">📧</span><span class="connect-text">jrzisad@gmail.com</span>
      </a>
      <a class="connect-btn" href="tel:+8801954884526">
        <span class="connect-icon">📞</span><span class="connect-text">+880 1954-884526</span>
      </a>
    </div>
  </section>

  <!-- ═══════════════ FOOTER ═══════════════ -->
  <footer class="footer">
    <p>⟨ SYSTEM STATUS: <span>ALL SENSORS ACTIVE</span> ⟩ &nbsp;·&nbsp; SESSION TIME: <span id="uptime">00:00:00</span></p>
    <p style="margin-top:10px;">© 2025 Mohammad Zisadul Islam &nbsp;·&nbsp; <span>Dhaka, Bangladesh</span> &nbsp;·&nbsp; <span>Defend Forward</span></p>
  </footer>

</div>

<script>
  /* TYPING ANIMATION */
  const phrases = [
    "Monitoring SIEM alerts with Wazuh + ELK Stack...",
    "Analyzing logs, hunting Indicators of Compromise...",
    "Defending against OWASP Top 10 with BunkerWeb WAF...",
    "Writing YARA rules to classify malware samples...",
    "Triaging incidents & practicing SOC playbooks...",
    "Learning. Building. Defending. Repeat. 🛡️"
  ];
  let pi = 0, ci = 0, deleting = false;
  const el = document.getElementById('typing');
  function type() {
    const phrase = phrases[pi];
    if (!deleting) {
      el.innerHTML = phrase.slice(0, ci++) + '<span class="cursor"></span>';
      if (ci > phrase.length) { deleting = true; setTimeout(type, 1800); return; }
    } else {
      el.innerHTML = phrase.slice(0, ci--) + '<span class="cursor"></span>';
      if (ci < 0) { deleting = false; pi = (pi + 1) % phrases.length; ci = 0; }
    }
    setTimeout(type, deleting ? 35 : 65);
  }
  type();

  /* HEATMAP */
  const levels = [0,0,0,1,1,2,3,4];
  const hm = document.getElementById('heatmap');
  for (let i = 0; i < 52 * 7; i++) {
    const cell = document.createElement('span');
    const lvl = levels[Math.floor(Math.random() * levels.length)];
    cell.className = 'hm-cell' + (lvl ? ' hm-' + lvl : '');
    hm.appendChild(cell);
  }

  /* UPTIME */
  const start = Date.now();
  setInterval(() => {
    const s = Math.floor((Date.now() - start) / 1000);
    const h = String(Math.floor(s/3600)).padStart(2,'0');
    const m = String(Math.floor((s%3600)/60)).padStart(2,'0');
    const sc = String(s%60).padStart(2,'0');
    document.getElementById('uptime').textContent = h+':'+m+':'+sc;
  }, 1000);
</script>
</body>
</html>
