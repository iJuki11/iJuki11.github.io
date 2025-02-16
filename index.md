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
            color: white;
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

        .category {
            position: relative;
            cursor: pointer;
            padding-bottom: 5px;
            display: inline-block;
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

        /* Hover Animation for Shipped Projects */
        .category:hover {
            font-size: 28px; /* Increase font size on hover */
            transform: scale(1.1);
            transition: all 0.3s ease;
        }

        /* Dropdown Menu */
        .dropdown {
            position: absolute;
            left: 100%;
            top: 0;
            display: none;
            background-color: rgba(75, 114, 180, 0.9);
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
        }

        /* Blue popup style */
        .popup {
            display: none;
            position: absolute;
            top: 100%;
            left: 50%;
            transform: translateX(-50%);
            background-color: rgba(0, 0, 255, 0.9);
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

    </style>
</head>
<body>

    <!-- Category Navigation -->
    <div class="categories">
        <div class="category">
            VFX Reel
        </div>

        <div class="category">
            Shipped Projects
            <!-- Pop-up window with project names -->
            <div class="popup">
                <p><strong>Cosmic Paradox: Noire</strong></p>
                <p><strong>Magnitude / Magnitude Epsilon</strong></p>
                <p><strong>Puzzle Piecer: The World Below</strong></p>
            </div>
        </div>
    </div>

    <!-- Project Sections -->
    <div id="project1" class="project active">
        <h2>VFX Reel</h2>
        <video width="500" height="300" controls muted>
            <source src="videos/FxReel.mp4" type="video/mp4">
            Your browser does not support the video tag.
        </video>
    </div>

    <div id="project2" class="project">
        <h2>Explosion</h2>
        <video width="500" height="300" controls muted>
            <source src="videos/Explosion.mp4" type="video/mp4">
            Your browser does not support the video tag.
        </video>
    </div>

    <div id="project3" class="project">
        <h2>Meteor</h2>
        <video width="500" height="300" controls muted>
            <source src="videos/Meteor.mp4" type="video/mp4">
            Your browser does not support the video tag.
        </video>
    </div>

    <div id="project4" class="project">
        <h2>Illustration</h2>
        <img src="images/illustration.jpg" width="400">
    </div>

    <div id="project5" class="project">
        <h2>Character Design</h2>
        <img src="images/character.jpg" width="400">
    </div>

    <!-- Cosmic Paradox Section (Hidden by default) -->
    <div id="cosmic-paradox" class="project">
        <h2>Cosmic Paradox: Noire</h2>
        <div class="videos">
            <!-- Backgrounds -->
            <h4>Backgrounds</h4>
            <div class="video-container">
                <h5>First Level Design</h5>
                <video controls muted>
                    <source src="videos/Noire/LevelDesign_01.mp4" type="video/mp4">
                </video>
            </div>
            <div class="video-container">
                <h5>Second Level Design</h5>
                <video controls muted>
                    <source src="videos/Noire/LevelDesign_02.mp4" type="video/mp4">
                </video>
            </div>
            <div class="video-container">
                <h5>Third Level Design</h5>
                <video controls muted>
                    <source src="videos/Noire/LevelDesign_03.mp4" type="video/mp4">
                </video>
            </div>

            <!-- VFX -->
            <h4>VFX</h4>
            <div class="video-container">
                <h5>Rampage VFX</h5>
                <video controls muted>
                    <source src="videos/Noire/Rampage.mp4" type="video/mp4">
                </video>
            </div>
            <div class="video-container">
                <h5>Shield VFX</h5>
                <video controls muted>
                    <source src="videos/Noire/ShieldVFX.mp4" type="video/mp4">
                </video>
            </div>

            <!-- Splash Screen -->
            <h4>Splash Screen</h4>
            <div class="video-container">
                <video controls muted>
                    <source src="videos/Noire/SplashScreen_vfx.mp4" type="video/mp4">
                </video>
            </div>

            <!-- Text VFX -->
            <h4>Text VFX</h4>
            <div class="video-container">
                <video controls muted>
                    <source src="videos/Noire/Text_vfx.mp4" type="video/mp4">
                </video>
            </div>

            <!-- UI Effects -->
            <h4>UI Effects</h4>
            <div class="video-container">
                <video controls muted>
                    <source src="videos/Noire/UIVFX_01.mp4" type="video/mp4">
                </video>
            </div>
            <div class="video-container">
                <video controls muted>
                    <source src="videos/Noire/UIVFX_02.mp4" type="video/mp4">
                </video>
            </div>
        </div>
    </div>

    <script>
        // When "Cosmic Paradox: Noire" is clicked, show the corresponding videos and remove the VFX Reel
        document.querySelector('.popup').addEventListener('click', function() {
            document.getElementById('cosmic-paradox').classList.add('active');
            document.getElementById('project1').classList.remove('active');
        });
    </script>

</body>
</html>
