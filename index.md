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
        }

        .category {
            position: relative;
            cursor: pointer;
            padding-bottom: 5px;
        }

        .category::after {
            content: "";
            display: block;
            width: 100%;
            height: 2px;
            background-color: white;
            margin-top: 5px;
        }

        /* Dropdown Menu */
        .dropdown {
            position: absolute;
            left: 50%;
            transform: translateX(-50%);
            top: 100%;
            display: none;
            background-color: rgba(75, 114, 180, 0.9);
            padding: 10px;
            border-radius: 5px;
            width: 150px;
            text-align: left;
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
            margin-top: 20px;
            text-align: left;
            padding-left: 50px;
        }

        .active {
            display: block;
        }
    </style>
</head>
<body>

    <!-- Category Navigation -->
    <div class="categories">
        <div class="category">
            VFX
            <div class="dropdown">
                <button onclick="showProject('project1')">VFX Reel</button>
                <button onclick="showProject('project2')">Explosion</button>
                <button onclick="showProject('project3')">Meteor</button>
            </div>
        </div>

        <div class="category">
            2D Art
            <div class="dropdown">
                <button onclick="showProject('project4')">Illustration</button>
                <button onclick="showProject('project5')">Character Design</button>
            </div>
        </div>
    </div>

    <!-- Project Sections -->
    <div id="project1" class="project active">
        <h2>VFX Reel</h2>
        <video width="500" height="300" controls>
            <source src="videos/FxReel.mp4" type="video/mp4">
            Your browser does not support the video tag.
        </video>
    </div>

    <div id="project2" class="project">
        <h2>Explosion</h2>
        <video width="500" height="300" controls>
            <source src="videos/Explosion.mp4" type="video/mp4">
            Your browser does not support the video tag.
        </video>
    </div>

    <div id="project3" class="project">
        <h2>Meteor</h2>
        <video width="500" height="300" controls>
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
        function showProject(projectId) {
            let projects = document.querySelectorAll('.project');
            projects.forEach(project => project.classList.remove('active'));

            document.getElementById(projectId).classList.add('active');
        }
    </script>

</body>
</html>
