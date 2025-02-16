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
        .category {
            margin-top: 50px;
            font-size: 24px;
            cursor: pointer;
            background-color: #4b72b4;
            padding: 15px;
            width: 200px;
            margin: 10px auto;
            border-radius: 10px;
        }
        .category:hover {
            background-color: #345a8a;
        }
        .dropdown {
            display: none;
            background-color: #4b72b4;
            padding: 10px;
            border-radius: 10px;
            width: 200px;
            margin: 0 auto;
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
        .project {
            display: none;
            margin-top: 20px;
        }
        .active {
            display: block;
        }
    </style>
</head>
<body>

    <!-- Dropdown Menus -->
    <div class="category" onclick="toggleDropdown('vfxMenu')">VFX</div>
    <div id="vfxMenu" class="dropdown">
        <button onclick="showProject('project1')">Sword Slash</button>
        <button onclick="showProject('project2')">Explosion</button>
        <button onclick="showProject('project3')">Meteor</button>
    </div>

    <div class="category" onclick="toggleDropdown('artMenu')">2D Art</div>
    <div id="artMenu" class="dropdown">
        <button onclick="showProject('project4')">Illustration</button>
        <button onclick="showProject('project5')">Character Design</button>
    </div>

    <!-- Project Sections -->
    <div id="project1" class="project active">
        <h2>Sword Slash</h2>
        <video width="500" height="300" controls>
            <source src="videos/SwordSlash.mp4" type="video/mp4">
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
        function toggleDropdown(menuId) {
            let menu = document.getElementById(menuId);
            menu.style.display = (menu.style.display === "block") ? "none" : "block";
        }

        function showProject(projectId) {
            let projects = document.querySelectorAll('.project');
            projects.forEach(project => project.classList.remove('active'));

            document.getElementById(projectId).classList.add('active');
        }
    </script>

</body>
</html>
