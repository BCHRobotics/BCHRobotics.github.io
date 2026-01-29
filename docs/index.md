<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Team 2386 Programming</title>

  <!-- Pico CSS -->
  <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/@picocss/pico@1/css/pico.min.css">

  <style>
:root { --accent:#ff3c3c; }
html { scroll-behavior:smooth; }

#boot{position:fixed;inset:0;background:black;color:#ff3c3c;z-index:9999;display:flex;align-items:center;justify-content:center}
#terminal{font-family:monospace;font-size:.9rem}

.cyber-grid{position:fixed;inset:0;z-index:-1;background:linear-gradient(rgba(255,60,60,.07) 1px,transparent 1px),linear-gradient(90deg,rgba(255,60,60,.07) 1px,transparent 1px);background-size:40px 40px;animation:gridMove 20s linear infinite}
@keyframes gridMove{to{background-position:400px 400px}}

.repo-card{position:relative;border-radius:1rem;overflow:hidden;transition:.4s;cursor:pointer}
.repo-card:hover{transform:translateY(-10px) scale(1.03);box-shadow:0 0 40px rgba(255,60,60,.5)}
.repo-card::before,.repo-card::after{content:"";position:absolute;width:20px;height:20px;border:2px solid var(--accent)}
.repo-card::before{top:10px;left:10px;border-right:none;border-bottom:none}
.repo-card::after{bottom:10px;right:10px;border-left:none;border-top:none}

.robot-info{position:absolute;inset:0;background:rgba(0,0,0,.9);backdrop-filter:blur(6px);padding:1rem;transform:scaleY(0);transform-origin:top;transition:.4s;font-size:.85rem}
.repo-card.active .robot-info{transform:scaleY(1)}

.stat{margin:.4rem 0}
.bar{height:6px;background:#333;border-radius:3px;overflow:hidden}
.bar span{display:block;height:100%;background:var(--accent)}
</style>

<script>
const lines=["Initializing FRC Systems...","Loading Robot Profiles...","Connecting to GitHub...","Boot complete."];
const term=document.getElementById('terminal');let i=0;
const iv=setInterval(()=>{term.textContent+=lines[i]+"
";i++;if(i===lines.length){clearInterval(iv);setTimeout(()=>boot.style.display='none',800)}},600);
document.querySelectorAll('.repo-card').forEach(c=>c.addEventListener('click',()=>c.classList.toggle('active')));
</script>

  <script>
    const reveals = document.querySelectorAll('.reveal');
    window.addEventListener('scroll', () => {
      reveals.forEach(el => {
        const top = el.getBoundingClientRect().top;
        if (top < window.innerHeight - 100) {
          el.classList.add('active');
        }
      });
    });
  </script>
</head>
<body>

  <!-- BOOT UP OVERLAY -->
  <div id="boot"><pre id="terminal"></pre></div>
  <div class="cyber-grid"></div>

  <nav class="container-fluid">
    <ul>
      <li><strong>Team 2386 Programming</strong></li>
    </ul>
    <ul>
      <li><a href="#repos">Repositories</a></li>
      <li><a href="#links">Links</a></li>
      <li><a href="https://bchrobotics.com/" role="button">Main Site</a></li>
    </ul>
  </nav>

  <!-- Main Content -->
  <main class="container">

    <!-- Hero Section -->
    <header class="hero">
      <img src="img/trojan_title.png" alt="Team 2386 Trojan Logo">
      <p>
        This is the official programming documentation hub for FRC Team 2386.
        While this isn’t our main team website, it’s where we host code, notes,
        and experiments related to robot programming.
      </p>
      <p><em>More cool stuff may appear here soon. Who knows?</em></p>
    </header>

    <!-- Repositories -->
    <section id="repos">
  <h2>Robot Systems</h2>
  <div class="grid">

    <article class="repo-card">
      <h3>TankBot</h3>
      <img src="img/tankbot.png" width="200" alt="TankBot">
      <div class="robot-info">
        <pre>&gt; SYSTEM: TankBot
&gt; MODE: Training / Drivetrain Testing</pre>
        <div class="stat">Weight<div class="bar"><span style="width:65%"></span></div></div>
        <div class="stat">Drivetrain<div class="bar"><span style="width:80%"></span></div></div>
        <div class="stat">Autonomy<div class="bar"><span style="width:50%"></span></div></div>
        <a href="https://github.com/BCHRobotics/TankBot" target="_blank">Access Repository →</a>
      </div>
    </article>

    <article class="repo-card">
      <h3>MiniBot</h3>
      <img src="img/minibot.png" width="200" alt="MiniBot">
      <div class="robot-info">
        <pre>&gt; SYSTEM: MiniBot
&gt; MODE: Prototyping / Sensors</pre>
        <div class="stat">Weight<div class="bar"><span style="width:40%"></span></div></div>
        <div class="stat">Drivetrain<div class="bar"><span style="width:60%"></span></div></div>
        <div class="stat">Autonomy<div class="bar"><span style="width:45%"></span></div></div>
        <a href="https://github.com/BCHRobotics/MiniBot" target="_blank">Access Repository →</a>
      </div>
    </article>

    <article class="repo-card">
      <h3>2025 Competition Robot</h3>
      <img src="img/2025.png" width="200" alt="2025 Robot">
      <div class="robot-info">
        <pre>&gt; SYSTEM: 2025 Robot
&gt; MODE: Competition</pre>
        <div class="stat">Weight<div class="bar"><span style="width:85%"></span></div></div>
        <div class="stat">Drivetrain<div class="bar"><span style="width:90%"></span></div></div>
        <div class="stat">Autonomy<div class="bar"><span style="width:95%"></span></div></div>
        <a href="https://github.com/BCHRobotics/2025_Updated" target="_blank">Access Repository →</a>
      </div>
    </article>

    <article class="repo-card">
      <h3>2024 Competition Robot</h3>
      <img src="img/2024.png" width="200" alt="2024 Robot">
      <div class="robot-info">
        <pre>&gt; SYSTEM: 2024 Robot
&gt; MODE: Competition</pre>
        <div class="stat">Weight<div class="bar"><span style="width:80%"></span></div></div>
        <div class="stat">Drivetrain<div class="bar"><span style="width:85%"></span></div></div>
        <div class="stat">Autonomy<div class="bar"><span style="width:75%"></span></div></div>
        <a href="https://github.com/BCHRobotics/2024_Updated" target="_blank">Access Repository →</a>
      </div>
    </article>

  </div>
</section>

    <!-- Links -->
    <section id="links" style="margin-top: 3rem;">
      <h2>Other Important Links</h2>
      <ul>
        <li><a href="https://github.com/BCHRobotics/BCHRobotics.github.io" target="_blank">Website GitHub Repository</a></li>
        <li><a href="https://github.com/BCHRobotics" target="_blank">FRC 2386 GitHub Organization</a></li>
        <li><a href="https://bchrobotics.com/" target="_blank">Main Team 2386 Website</a></li>
        <li><a href="https://github.com/full-auto-robots" target="_blank">FAR Robotics GitHub</a></li>
      </ul>
    </section>

  </main>

  <!-- Footer -->
  <footer class="container">
    <small>
      © Team 2386 • Programming Documentation Hub
    </small>
  </footer>

</body>
</html>
