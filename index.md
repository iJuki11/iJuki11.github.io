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
            background-color: black;
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

        /* New style for Cosmic Paradox Noire */
        #project1 h2 {
            font-size: 36px;
            text-align: left;
            margin-top: 20px;
            font-weight: bold;
        }

        .content-section {
            margin-top: 30px;
            text-align: left;
            padding-left: 50px;
        }

        .subsection {
            margin-bottom: 40px;
        }

        .section-title {
            font-size: 28px;
            font-weight: bold;
            margin-bottom: 15px;
        }

        ul {
            list-style: none;
            padding-left: 0;
        }

        ul li {
            font-size: 18px;
            margin: 5px 0;
        }

        .bullet {
            font-size: 24px;
            margin-right: 10px;
        }

        .video-container {
            margin-top: 20px;
        }

        .video-container h4 {
            font-size: 20px;
            text-align: center;
            margin-bottom: 10px;
        }

        video {
            display: block;
            margin: 0 auto;
            border-radius: 5px;
        }

        /* Hover styles for Shipped Project */
        .category:hover {
            background-color: white;
            color: black;
        }

        .category:hover .popup {
            background-color: #333;
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
        <h2>Cosmic Paradox: Noire</h2>
        
        <div class="content-section">
            <div class="subsection">
                <h3 class="section-title">Backgrounds</h3>
                <ul>
                    <li><span class="bullet">•</span> Level Design 1</li>
                    <li><span class="bullet">•</span> Level Design 2</li>
                    <li><span class="bullet">•</span> Level Design 3</li>
                </ul>

                <div class="video-container">
                    <h4>Level Design 1</h4>
                    <video controls width="500">
                        <source src="videos/Noire/BackGroundMissionRecapDesign.mp4" type="video/mp4">
                        Your browser does not support the video tag.
                    </video>
                </div>
                <div class="video-container">
                    <h4>Level Design 2</h4>
                    <video controls width="500">
                        <source src="videos/Noire/LevelDesign_01.mp4" type="video/mp4">
                        Your browser does not support the video tag.
                    </video>
                </div>
                <div class="video-container">
                    <h4>Level Design 3</h4>
                    <video controls width="500">
                        <source src="videos/Noire/LevelDesign_02.mp4" type="video/mp4">
                        Your browser does not support the video tag.
                    </video>
                </div>
            </div>

            <div class="subsection">
                <h3 class="section-title">VFX</h3>
                <ul>
                    <li><span class="bullet">•</span> Rampage VFX</li>
                    <li><span class="bullet">•</span> Shield VFX</li>
                </ul>

                <div class="video-container">
                    <h4>Rampage VFX</h4>
                    <video controls width="500">
                        <source src="videos/Noire/Rampage.mp4" type="video/mp4">
                        Your browser does not support the video tag.
                    </video>
                </div>
                <div class="video-container">
                    <h4>Shield VFX</h4>
                    <video controls width="500">
                        <source src="videos/Noire/ShieldVFX.mp4" type="video/mp4">
                        Your browser does not support the video tag.
                    </video>
                </div>
            </div>

            <div class="subsection">
                <h3 class="section-title">Splash Screen</h3>
                <ul>
                    <li><span class="bullet">•</span> Splash Screen VFX</li>
                </ul>

                <div class="video-container">
                    <h4>Splash Screen VFX</h4>
                    <video controls width="500">
                        <source src="videos/Noire/SplashScreen_vfx.mp4" type="video/mp4">
                        Your browser does not support the video tag.
                    </video>
                </div>
            </div>

            <div class="subsection">
                <h3 class="section-title">Text VFX</h3>
                <ul>
                    <li><span class="bullet">•</span> Text VFX</li>
                </ul>

                <div class="video-container">
                    <h4>Text VFX</h4>
                    <video controls width="500">
                        <source src="videos/Noire/Text_vfx.mp4" type="video/mp4">
                        Your browser does not support the video tag.
                    </video>
                </div>
            </div>

            <div class="subsection">
                <h3 class="section-title">UI Effects</h3>
                <ul>
                    <li><span class="bullet">•</span> UI VFX 1</li>
                    <li><span class="bullet">•</span> UI VFX 2</li>
                </ul>

                <div class="video-container">
                    <h4>UI VFX 1</h4>
                    <video controls width="500">
                        <source src="videos/Noire/UIVFX_01.mp4" type="video/mp4">
                        Your browser does not support the video tag.
                    </video>
                </div>
                <div class="video-container">
                    <h4>UI VFX 2</h4>
                    <video controls width="500">
                        <source src="videos/Noire/UIVFX_02.mp4" type="video/mp4">
                        Your browser does not support the video tag.
                    </video>
                </div>
            </div>
        </div>
    </div>

    <script>
        function showProject(projectId) {
            let projects = document.querySelectorAll('.project');
            projects.forEach(project => project.classList.remove('active'));

            document.getElementById(projectId).classList.add('active');
        }
    </script>

</body>
</html>
