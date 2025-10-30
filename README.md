# glowing-train-Profile-Theme
Kali Linux MAtrix Like themed Profile for web page for Github.io themes


<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>HACKTIVATE — Matrix Terminal</title>
  <link rel="icon" href="assets/favicon.svg" />
  <link rel="stylesheet" href="style.css" />
  <!-- optional analytics -->
  <!-- <script defer data-domain="hacktivate.app" src="https://plausible.io/js/script.js"></script> -->
</head>
<body>
<canvas id="matrix"></canvas>

<div class="desktop">
  <header class="header">
    <div class="brand">
      <svg class="logo" viewBox="0 0 720 190" xmlns="http://www.w3.org/2000/svg" role="img" aria-label="HACKTIVATE LABS">
        <defs>
          <linearGradient id="hx" x1="0" x2="1" y1="0.5" y2="0.5">
            <stop offset="0" stop-color="#00ff7f"/>
            <stop offset="1" stop-color="#00b2ff"/>
          </linearGradient>
        </defs>
        <rect x="0" y="26" width="720" height="130" rx="16" fill="rgba(1,12,10,0.3)"/>
        <text x="32" y="108" font-family="ui-monospace, SFMono-Regular, Menlo, Monaco, Consolas, 'Liberation Mono', 'Courier New', monospace" font-size="64" font-weight="700" letter-spacing="8" fill="url(#hx)">
          HACKTIVATE
        </text>
        <text x="520" y="144" font-family="Inter, system-ui, -apple-system" font-size="26" fill="#7fffd4" opacity="0.9">
          AI • SECURITY • AUTOMATION
        </text>
      </svg>
      <div class="title">Matrix Terminal • steve㉿hacktivate</div>
    </div>
    <nav class="nav">
      <button data-target="terminal" class="active">Terminal</button>
      <button data-target="about">About</button>
      <button data-target="projects">Projects</button>
      <button data-target="contact">Contact</button>
      <button data-target="download">Download</button>
    </nav>
  </header>

  <main class="main">
    <section id="terminal" class="panel active" aria-live="polite">
      <div class="term-header">─(steve㉿HACKTIVATE)-[~] └─$ welcome.sh</div>
      <div id="console" class="console" tabindex="0" role="application" aria-label="HACKTIVATE terminal">
        <div class="line">Welcome to <span class="accent">HACKTIVATE</span> — Matrix terminal interface.</div>
        <div class="line">Type <span class="cmd">help</span> to see commands or use the top nav.</div>
        <div id="output" class="output" aria-hidden="false"></div>
        <div class="prompt">
          <span class="user">steve㉿HACKTIVATE</span>:~$ 
          <input id="cmdline" autofocus autocomplete="off" spellcheck="false" />
        </div>
      </div>
      <div class="hint">Commands: <code>help</code> · <code>about</code> · <code>projects</code> · <code>contact</code> · <code>clear</code> · <code>download</code> · <code>launch</code></div>
    </section>

    <section id="about" class="panel">
      <h2>About — Steve Plasencia</h2>
      <p>Founder of <strong>HACKTIVATE LABS</strong>. Security researcher, AI automation strategist, Web3/staffing operator.</p>
      <p>Aliases: <code>@FunkyMonkey5150</code> · <code>Dappster</code> · <code>Crypto Head Hunter</code> · <code>HACKTIVATE</code></p>
      <ul>
        <li>AI / Agents / Automation (GoHighLevel, Zapier, Make, custom LLM tools)</li>
        <li>Cyber / Red Team / Pentesting / Wireless & IoT research</li>
        <li>Blockchain staffing: on-chain resumes, verifiable credentials, tokenized payroll</li>
      </ul>
    </section>

    <section id="projects" class="panel">
      <h2>Featured Projects</h2>
      <ul class="proj-list">
        <li><strong>Rocket Rabbit AI</strong> — AI SaaS & funnel automation engine.</li>
        <li><strong>The Staffing DAO</strong> — blockchain-powered workforce platform.</li>
        <li><strong>HACKTIVATE LABS Tools</strong> — NetMapper, LoRaMonitor, FuzzForge, TokenWatch, AI ReconX, PromptGuard, ContainerGuard.</li>
        <li><strong>Hardware / RF / Wireless</strong> — Pwnagotchi, Flipper Zero toolkit, ESP32 (LilyGO), WiFi Pineapple.</li>
      </ul>
      <p class="hint">All research is for authorized, educational, defensive use only.</p>
    </section>

    <section id="contact" class="panel">
      <h2>Contact / Collab</h2>
      <p>Fill the form or run <code>contact</code> in the terminal.</p>
      <form id="contactForm" action="https://formspree.io/f/your-form-id" method="POST" class="contact-form">
        <label>
          Your email
          <input name="email" type="email" required />
        </label>
        <label>
          Your message
          <textarea name="message" rows="4" required>Interested in AI SaaS / staffing automation / Web3 workforce.</textarea>
        </label>
        <button type="submit">Send Secure Request</button>
      </form>
      <p class="hint">Direct: <a href="mailto:info@stevesjobbs.com">info@stevesjobbs.com</a> · <a href="tel:+13233960096">+1 (323) 396-0096</a> · WhatsApp: 213-301-6016</p>
    </section>

    <section id="download" class="panel">
      <h2>Downloads</h2>
      <p><button id="downloadReadme" class="btn">Download HACKTIVATE README</button></p>
      <p><button id="downloadProfile" class="btn">Download Profile .txt</button></p>
      <p class="hint">Upload <code>index.html</code>, <code>style.css</code>, <code>script.js</code> to GitHub Pages.</p>
    </section>

  </main>

  <footer class="footer">
    <div>© 2025 Steve Plasencia — HACKTIVATE LABS</div>
    <div>Matrix UI • Terminal Router • GitHub Pages ready</div>
  </footer>
</div>

<script src="script.js"></script>
</body>
</html>

// MATRIX RAIN
const canvas = document.getElementById('matrix');
const ctx = canvas.getContext('2d');
function resizeMatrix() {
  canvas.width = window.innerWidth;
  canvas.height = window.innerHeight;
}
resizeMatrix();
window.addEventListener('resize', resizeMatrix);
const letters = 'アァカサタナハマヤャラワガザダバパイィキシチニヒミリヰギジヂビピウゥクスツヌフムユュルグズヅブプエェケセテネヘメレヱゲゼデベペオォコソトノホモヨョロヲゴゾドボポ0123456789HACKTIVATE';
const fontSize = 14;
let drops = [];
function initDrops() {
  drops = new Array(Math.floor(canvas.width / fontSize)).fill(1);
}
initDrops();
function drawMatrix() {
  ctx.fillStyle = 'rgba(0,0,0,0.09)';
  ctx.fillRect(0,0,canvas.width,canvas.height);
  ctx.fillStyle = '#00ff7f';
  ctx.font = fontSize + 'px monospace';
  for (let i = 0; i < drops.length; i++) {
    const text = letters.charAt(Math.floor(Math.random() * letters.length));
    ctx.fillText(text, i * fontSize, drops[i] * fontSize);
    if (drops[i] * fontSize > canvas.height && Math.random() > 0.975) {
      drops[i] = 0;
    }
    drops[i]++;
  }
}
setInterval(drawMatrix, 45);

// TERMINAL + SPA ROUTER
const cmdInput = document.getElementById('cmdline');
const output = document.getElementById('output');
const consoleDiv = document.getElementById('console');
const navButtons = document.querySelectorAll('.nav button');
const panels = document.querySelectorAll('.panel');

const commands = {
  help: `Available commands:
  help        Show this help
  about       Open About panel
  projects    Open Projects panel
  contact     Open Contact panel
  download    Download README
  clear       Clear terminal
  launch      Simulate system launch`,
  about: `HACKTIVATE LABS — founder: Steve Plasencia.
AI + Automation + Web3 + Offensive Security.
Aliases: FunkyMonkey5150, Dappster, Crypto Head Hunter.`,
  projects: `Projects:
  - Rocket Rabbit AI — AI SaaS engine
  - The Staffing DAO — Web3 staffing
  - HACKTIVATE Tools — NetMapper, FuzzForge, TokenWatch, AI ReconX
  - Hardware: Pwnagotchi / Flipper Zero / ESP32`,
  contact: `Contact:
  Email: info@stevesjobbs.com
  Alt:   hacktivate5150@gmail.com
  Phone: 323-396-0096
  WhatsApp: 213-301-6016`
};

function printLine(text) {
  const d = document.createElement('div');
  d.textContent = text;
  output.appendChild(d);
  consoleDiv.scrollTop = consoleDiv.scrollHeight;
}
function activatePanel(id) {
  panels.forEach(p => p.classList.remove('active'));
  const target = document.getElementById(id);
  if (target) target.classList.add('active');
  navButtons.forEach(b => b.classList.remove('active'));
  const btn = document.querySelector('.nav button[data-target="'+id+'"]');
  if (btn) btn.classList.add('active');
}
function triggerDownload() {
  const content = `# HACKTIVATE\n\nSteve Plasencia — HACKTIVATE LABS\nAI • Security • Automation`;
  const blob = new Blob([content], { type: 'text/plain;charset=utf-8' });
  const a = document.createElement('a');
  a.href = URL.createObjectURL(blob);
  a.download = 'HACKTIVATE_README.md';
  a.click();
}
function simulateLaunch() {
  printLine('Initializing HACKTIVATE systems...');
  setTimeout(() => printLine('Loading AI agents...'), 700);
  setTimeout(() => printLine('Provisioning secure automation nodes...'), 1350);
  setTimeout(() => printLine('Deploying staffing / Web3 modules...'), 2000);
  setTimeout(() => printLine('✅ All systems online. Welcome, Steve.'), 2600);
}
function runCommand(cmd) {
  cmd = cmd.trim();
  if (!cmd) return;
  printLine('$ ' + cmd);
  if (cmd === 'clear') {
    output.innerHTML = '';
    return;
  }
  if (cmd === 'about' || cmd === 'projects' || cmd === 'contact' || cmd === 'download') {
    activatePanel(cmd);
  }
  if (commands[cmd]) {
    printLine(commands[cmd]);
    if (cmd === 'download') triggerDownload();
  } else if (cmd === 'launch') {
    simulateLaunch();
  } else if (!(cmd === 'about' || cmd === 'projects' || cmd === 'contact')) {
    printLine('Command not found: ' + cmd);
  }
}
cmdInput.addEventListener('keydown', e => {
  if (e.key === 'Enter') {
    runCommand(cmdInput.value);
    cmdInput.value = '';
  } else if (e.key === 'Tab') {
    e.preventDefault();
    const val = cmdInput.value;
    const opts = ['help','about','projects','contact','download','clear','launch'];
    const match = opts.find(o => o.startsWith(val));
    if (match) cmdInput.value = match;
  }
});
navButtons.forEach(btn => {
  btn.addEventListener('click', () => {
    const target = btn.getAttribute('data-target');
    activatePanel(target);
  });
});
document.getElementById('downloadReadme').addEventListener('click', () => triggerDownload());
document.getElementById('downloadProfile').addEventListener('click', () => {
  const profile = `Steve Plasencia (HACKTIVATE)
SaaS • AI Agents • Web3 • Blockchain • Automation • Cybersecurity
Direct: 323-396-0096
Email: info@stevesjobbs.com
Aliases: FunkyMonkey5150 · Dappster · Crypto Head Hunter`;
  const blob = new Blob([profile], { type: 'text/plain;charset=utf-8' });
  const a = document.createElement('a');
  a.href = URL.createObjectURL(blob);
  a.download = 'STEVE_HACKTIVATE_PROFILE.txt';
  a.click();
});
// form
const form = document.getElementById('contactForm');
if (form) {
  form.addEventListener('submit', async (e) => {
    e.preventDefault();
    printLine('Submitting contact request...');
    try {
      const data = new FormData(form);
      await fetch(form.action, { method: 'POST', body: data, headers: { 'Accept': 'application/json' } });
      printLine('Contact request sent. You will be contacted securely.');
      form.reset();
    } catch (err) {
      printLine('Error sending request. Use: info@stevesjobbs.com');
    }
  });
}
consoleDiv.addEventListener('click', () => cmdInput.focus());
window.addEventListener('load', () => cmdInput.focus());

/* Matrix terminal aesthetic */
:root {
  --bg: #000a05;
  --panel: rgba(3, 12, 10, 0.45);
  --accent: #00ff7f;
  --accent2: #00b2ff;
  --muted: #7fb6a7;
  --glass: rgba(255,255,255,0.03);
  --mono: "Fira Code", "Roboto Mono", Menlo, Monaco, monospace;
  --radius: 10px;
}
* { box-sizing: border-box; }
html, body {
  height: 100%;
  margin: 0;
  background: #000;
  font-family: Inter, system-ui, -apple-system, "Segoe UI", Roboto, Arial, sans-serif;
  color: #d7f6e5;
}
#matrix {
  position: fixed;
  inset: 0;
  z-index: 0;
  background: #000;
}
.desktop {
  position: relative;
  z-index: 1;
  min-height: 100vh;
  display: flex;
  flex-direction: column;
}
.header {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 16px;
  padding: 14px 20px;
  background: radial-gradient(circle at top, rgba(0,0,0,0.3), rgba(0,0,0,0));
  border-bottom: 1px solid rgba(255,255,255,0.02);
  backdrop-filter: blur(6px);
}
.brand {
  display: flex;
  align-items: center;
  gap: 16px;
}
.logo {
  height: 54px;
}
.title {
  font-weight: 700;
  color: var(--accent);
  letter-spacing: .4px;
  font-size: 14px;
}
.nav button {
  background: transparent;
  border: 0;
  color: var(--muted);
  padding: 7px 12px;
  border-radius: 6px;
  font-weight: 700;
  cursor: pointer;
  transition: 0.15s;
}
.nav button.active,
.nav button:hover {
  background: linear-gradient(90deg, var(--accent), var(--accent2));
  color: #001411;
}
.main {
  display: flex;
  padding: 26px;
  gap: 24px;
  align-items: flex-start;
}
.panel {
  flex: 1;
  background: radial-gradient(circle at top, rgba(0,0,0,0.15), rgba(0,0,0,0));
  background-color: rgba(0,0,0,0.25);
  border: 1px solid rgba(0,255,127,0.08);
  border-radius: var(--radius);
  padding: 18px;
  min-height: 520px;
  display: none;
  box-shadow: 0 8px 35px rgba(0,0,0,0.6);
}
.panel.active {
  display: block;
}
.term-header {
  font-family: var(--mono);
  font-size: 12px;
  color: #7dffb7;
  margin-bottom: 8px;
}
.console {
  background: rgba(0, 10, 4, 0.6);
  border: 1px solid rgba(0,255,127,0.05);
  border-radius: 8px;
  padding: 16px;
  min-height: 360px;
  font-family: var(--mono);
  color: #bfffd8;
  overflow-y: auto;
  max-height: 480px;
}
.console .line {
  margin-bottom: 8px;
}
.prompt {
  display: flex;
  gap: 8px;
  align-items: center;
  margin-top: 12px;
}
.user {
  color: var(--accent);
  font-weight: 700;
}
#cmdline {
  background: transparent;
  border: 0;
  outline: none;
  color: #fff;
  font-family: var(--mono);
  font-size: 14px;
  flex: 1;
}
.output {
  white-space: pre-wrap;
}
.hint {
  margin-top: 10px;
  color: var(--muted);
  font-size: 12px;
}
.proj-list {
  list-style: square;
  padding-left: 18px;
  line-height: 1.5;
}
.contact-form {
  display: flex;
  flex-direction: column;
  gap: 12px;
  max-width: 460px;
}
.contact-form input,
.contact-form textarea {
  background: rgba(0,0,0,0.35);
  border: 1px solid rgba(0,255,127,0.09);
  border-radius: 6px;
  padding: 6px 8px;
  color: #fff;
  font-family: inherit;
}
.contact-form button {
  background: linear-gradient(90deg, var(--accent), var(--accent2));
  border: 0;
  padding: 8px 10px;
  border-radius: 6px;
  font-weight: 700;
  cursor: pointer;
  color: #001411;
}
.btn {
  background: linear-gradient(90deg, var(--accent), var(--accent2));
  border: 0;
  border-radius: 6px;
  padding: 8px 14px;
  color: #001411;
  font-weight: 600;
  cursor: pointer;
}
.footer {
  margin-top: auto;
  padding: 12px 26px;
  font-size: 12px;
  color: var(--muted);
  display: flex;
  justify-content: space-between;
  border-top: 1px solid rgba(0,0,0,0.1);
  background: rgba(0,0,0,0.25);
  backdrop-filter: blur(6px);
}
@media (max-width: 900px) {
  .main { flex-direction: column; }
  .panel { min-height: 400px; }
  .header { flex-wrap: wrap; gap: 12px; }
}
