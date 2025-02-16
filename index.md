<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Portfolio</title>
  <style>
    body {
      background-image: url('images/cowboy2.jpg');
      background-repeat: no-repeat;
      background-attachment: fixed;
      background-size: cover;
      font-family: Arial, sans-serif;
      text-align: center;
      background-color 1s, color 1s;
      color: #000000;
    }

    /* Category Section */
    .categories {
      display: flex;
      justify-content: center;
      gap: 50px;
      font-size: 24px;
      margin-top: 50px;
      font-weight: bold;
      position: relative;
    }

    /* Category Base Style */
    .category {
      position: relative;
      cursor: pointer;
      padding-bottom: 5px;
      display: inline-block;
      padding: 10px 20px;
      transition: background-color 0.3s, color 0.3s;
    }

    /* Hover Animation for all Categories */
    .category:hover {
      font-size: 28px;
      transform: scale(1.1);
      color: gold;
      transition: all 0.3s ease;
    }

    .category::after {
      content: "";
      display: block;
      width: 100%;
      height: 2px;
      background-color: white;
      margin-top: 5px;
      transition: all 0.3s ease;
    }

    .category:hover::after {
      width: 100%;
      height: 4px;
      background-color: rgba(75, 114, 180, 1);
      position: absolute;
      bottom: 0;
      left: 0;
    }

    /* Dropdown Menu */
    .dropdown {
      position: absolute;
      left: 100%;
      top: 0;
      display: none;
      background-color: #4b72b4;
      padding: 10px;
      border-radius: 5px;
      width: 200px;
      text-align: left;
      margin-top: 10px;
    }

    .category:hover .dropdown {
      display: block;
    }

    .dropdown button {
      background-color: transparent;
      color: white;
      border: none;
      cursor: pointer;
      font-size: 18px;
      display: block;
      width: 100%;
      text-align: left;
      padding: 8px 0;
    }

    .dropdown button:hover {
      text-decoration: underline;
    }

    /* Project Sections */
    .project {
      display: none;
      margin-top: 50px;
      text-align: left;
      padding-left: 50px;
      padding-right: 50px;
    }

    .active {
      display: block;
    }

    /* Fine line for categories */
    .category {
      padding-bottom: 10px;
      font-size: 28px;
    }

    /* Style for VFX Reel */
    .project iframe, .project video {
      width: 500px;
      height: 300px;
      margin-top: 50px;
    }

    /* Style for the videos and text */
    .videos {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
    }

    .videos h4 {
      width: 100%;
      text-align: left;
      font-size: 30px;
      margin-left: 20px;
    }

    .videos h5 {
      width: 100%;
      text-align: left;
      font-size: 22px;
      margin-left: 20px;
    }

    .video-container {
      margin: 20px;
      display: flex;
      flex-direction: column;
      align-items: center;
    }

    .video-title-centered {
      margin-top: 10px;
      font-size: 15px;
      text-align: center;
    }

    /* Blue popup style */
    .popup {
      display: none;
      position: absolute;
      top: 100%;
      left: 50%;
      transform: translateX(-50%);
      background-color: #4b72b4;
      padding: 20px;
      color: white;
      font-size: 18px;
      border-radius: 5px;
      width: 200px;
      text-align: center;
      z-index: 10;
    }

    .category:hover .popup {
      display: block;
    }

    /* Hover Effect for Projects in Pop-up */
    .popup p {
      font-size: 20px;
      margin: 10px 0;
      transition: all 0.3s ease;
    }

    .popup p:hover {
      font-size: 24px;
      color: gold;
      transform: scale(1.1);
    }
  </style>
</head>
<body>

  <!-- Category Navigation -->
  <div class="categories">
    <div class="category" id="vfx-reel">
      <span>VFX Reel</span>
    </div>

    <div class="category">
      <span>Shipped Projects</span>
      <!-- Pop-up window with project names -->
      <div class="popup">
        <p id="cosmic-paradox-link">Cosmic Paradox: Noire</p>
        <p id="magnitude-link">Magnitude</p>
        <p>Puzzle Piecer</p>
      </div>
    </div>
  </div>

  <!-- Project Sections -->
  <!-- VFX Reel Section (Default) -->
  <div id="vfx-reel-project" class="project active">
    <br><br><br><br><br><br>
    <h2>VFX Reel</h2>
    <video width="500" height="300" controls muted>
      <source src="videos/FxReel.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
  </div>

  <!-- Cosmic Paradox Section -->
  <div id="cosmic-paradox" class="project">
    <h1>Cosmic Paradox: Noire</h1>
    <ul>
      <li><strong>VFX:</strong> Created UI effects and the majority of in-game visual effects</li>
      <li><strong>Background Design:</strong> Designed and developed backgrounds</li>
      <li><strong>Optimization:</strong> Collaborated with programmers to optimize performance and resolve graphic issues for PC and PlayStation ports</li>
      <li><strong>Visual Identity:</strong> Developed the game’s overall visual identity, ensuring consistency across all visual elements</li>
      <br><br><br>
    </ul>
    <h2>Level Backgrounds</h2>
    <div class="video-container">
      <video controls muted>
        <source src="videos/Noire/LevelDesign_01.mp4" type="video/mp4">
      </video>
      <h5 class="video-title-centered">First Level Design</h5>
    </div>
    <div class="video-container">
      <video controls muted>
        <source src="videos/Noire/LevelDesign_02.mp4" type="video/mp4">
      </video>
      <h5 class="video-title-centered">Second Level Design</h5>
    </div>
    <div class="video-container">
      <video controls muted>
        <source src="videos/Noire/LevelDesign_03.mp4" type="video/mp4">
      </video>
      <h5 class="video-title-centered">Third Level Design</h5>
    </div>
    <h2>VFX</h2>
    <div class="video-container">
      <video controls muted>
        <source src="videos/Noire/Rampage.mp4" type="video/mp4">
      </video>
      <h5 class="video-title-centered">Rampage VFX</h5>
    </div>
    <div class="video-container">
      <video controls muted>
        <source src="videos/Noire/ShieldVFX.mp4" type="video/mp4">
      </video>
      <h5 class="video-title-centered">Shield VFX</h5>
    </div>
    <div class="video-container">
      <video controls muted>
        <source src="videos/Noire/UIVFX_01.mp4" type="video/mp4">
      </video>
      <h5 class="video-title-centered">UI fx</h5>
    </div>
    <div class="video-container">
      <video controls muted>
        <source src="videos/Noire/UIVFX_02.mp4" type="video/mp4">
      </video>
      <h5 class="video-title-centered">UI fx(02)</h5>
    </div>
    <br><br>
    <h2>Splash Screen</h2>
    <div class="video-container">
      <video controls muted>
        <source src="videos/Noire/SplashScreen_vfx.mp4" type="video/mp4">
      </video>
    </div>
    <br><br>
    <h2>Text Transition</h2>
    <div class="video-container">
      <video controls muted>
        <source src="videos/Noire/Text_vfx.mp4" type="video/mp4">
      </video>
    </div>
  </div>

  <!-- Magnitude Section -->
  <div id="magnitude" class="project">
    <h2>Magnitude</h2>
    <ul>
      <strong>
      <li>VFX: Vfx and whole art</li>
        </strong>
    <div class="video-container">
      <video controls muted>
        <source src="videos/Magnitude/Shield.mp4" type="video/mp4">
      </video>
      <h5 class="video-title-centered">Shield</h5>
    </div>
    <div class="video-container">
      <video controls muted>
        <source src="videos/Magnitude/Background.mp4" type="video/mp4">
      </video>
      <h5 class="video-title-centered">Background</h5>
    </div>
  </div>

  <script>
    // When clicking on VFX Reel, show only the VFX Reel project.
    document.getElementById('vfx-reel').addEventListener('click', function() {
      document.getElementById('vfx-reel-project').classList.add('active');
      document.getElementById('cosmic-paradox').classList.remove('active');
      document.getElementById('magnitude').classList.remove('active');
    });

    // When clicking on Cosmic Paradox, show only the Cosmic Paradox project.
    document.getElementById('cosmic-paradox-link').addEventListener('click', function() {
      document.getElementById('vfx-reel-project').classList.remove('active');
      document.getElementById('cosmic-paradox').classList.add('active');
      document.getElementById('magnitude').classList.remove('active');
    });

    // When clicking on Magnitude in the popup, show only the Magnitude project.
    document.getElementById('magnitude-link').addEventListener('click', function() {
      document.getElementById('vfx-reel-project').classList.remove('active');
      document.getElementById('cosmic-paradox').classList.remove('active');
      document.getElementById('magnitude').classList.add('active');
    });
  </script>

</body>
</html>
