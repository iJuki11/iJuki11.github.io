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

        /* Popup for Shipped Projects */
        .popup {
            display: none;
            position: absolute;
            top: 100%;
            left: 50%;
            transform: translateX(-50%);
            background-color: rgba(0, 0, 255, 0.9); /* Changed to blue */
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

        /* Pop-up content for Cosmic Paradox */
        .popup-content {
            display: none;
            padding-top: 20px;
        }

        .show-content .popup-content {
            display: block;
        }

        .popup-content h4 {
            margin-bottom: 10px;
        }

        .popup-content video {
            margin: 5px 0;
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
            <div class="popup" onclick="showPopupContent()">
                <p><strong>Cosmic Paradox: Noire</strong></p>
                <p><strong>Magnitude / Magnitude Epsilon</strong></p>
                <p><strong>Puzzle Piecer: The World Below</strong></p>
                <!-- Pop-up content for Cosmic Paradox -->
                <div class="popup-content">
                    <h4>Backgrounds</h4>
                    <video controls muted>
                        <source src="videos/BackGroundMissionRecapDesign.mp4" type="video/mp4">
                    </video>
                    <video controls muted>
                        <source src="videos/LevelDesign_01.mp4" type="video/mp4">
                    </video>
                    <video controls muted>
                        <source src="videos/LevelDesign_02.mp4" type="video/mp4">
                    </video>
                    <video controls muted>
                        <source src="videos/LevelDesign_03.mp4" type="video/mp4">
                    </video>

                    <h4>Some VFX</h4>
                    <video controls muted>
                        <source src="videos/Rampage.mp4" type="video/mp4">
                    </video>
                    <video controls muted>
                        <source src="videos/ShieldVFX.mp4" type="video/mp4">
                    </video>

                    <h4>Splash Screen</h4>
                    <video controls muted>
                        <source src="videos/SplashScreen_vfx.mp4" type="video/mp4">
                    </video>

                    <h4>Text VFX</h4>
                    <video controls muted>
                        <source src="videos/Text_vfx.mp4" type="video/mp4">
                    </video>

                    <h4>UI Effects</h4>
                    <video controls muted>
                        <source src="videos/UIVFX_01.mp4" type="video/mp4">
                    </video>
                    <video controls muted>
                        <source src="videos/UIVFX_02.mp4" type="video/mp4">
                    </video>
                </div>
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

    <script>
        function showPopupContent() {
            const popup = document.querySelector('.popup');
            popup.classList.toggle('show-content');
        }
    </script>

</body>
</html>
