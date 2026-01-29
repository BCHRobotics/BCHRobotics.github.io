<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Team 2386 Programming</title>

  <!-- Pico CSS -->
  <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/@picocss/pico@1/css/pico.min.css">

  <style>
    header.hero {
      text-align: center;
      padding: 3rem 1rem 2rem;
    }

    header.hero img {
      max-width: 420px;
      margin-bottom: 1.5rem;
    }

    .repo-card img {
      border-radius: 0.75rem;
      margin-top: 1rem;
    }

    .repo-card {
      height: 100%;
    }

    footer {
      margin-top: 4rem;
      text-align: center;
    }
  </style>
</head>
<body>

  <!-- Navigation -->
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
      <h2>Important Repositories</h2>
      <div class="grid">

        <article class="repo-card">
          <h3>TankBot</h3>
          <p>Experimental and training robot code.</p>
          <a href="https://github.com/BCHRobotics/TankBot" target="_blank">View Repository →</a>
          <img src="img/tankbot.png" alt="TankBot" width="200" height="200">
        </article>

        <article class="repo-card">
          <h3>MiniBot</h3>
          <p>Small-scale robot used for prototyping and learning.</p>
          <a href="https://github.com/BCHRobotics/MiniBot" target="_blank">View Repository →</a>
          <img src="img/minibot.png" alt="MiniBot" width="200" height="200">
        </article>

        <article class="repo-card">
          <h3>2025 Robot</h3>
          <p>Main competition robot code for the 2025 season.</p>
          <a href="https://github.com/BCHRobotics/2025_Updated" target="_blank">View Repository →</a>
          <img src="img/2025.png" alt="2025 Robot" width="200" height="200">
        </article>

        <article class="repo-card">
          <h3>2024 Robot</h3>
          <p>Main competition robot code for the 2024 season.</p>
          <a href="https://github.com/BCHRobotics/2024_Updated" target="_blank">View Repository →</a>
          <img src="img/2024.png" alt="2024 Robot" width="200" height="200">
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
