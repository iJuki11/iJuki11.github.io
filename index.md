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
        }
        .profile {
            margin-top: 20px;
        }
        .profile img {
            width: 100px;
            height: 100px;
            border-radius: 50%;
            border: 2px solid white;
        }
        .nav {
            margin-top: 20px;
        }
        .nav button {
            background-color: #4b72b4;
            color: white;
            padding: 10px;
            margin: 5px;
            border: none;
            cursor: pointer;
            font-size: 18px;
        }
        .nav button:hover {
            background-color: #345a8a;
        }
        .project {
            display: none; /* Hide all projects initially */
            margin-top: 20px;
        }
        .active {
            display: block; /* Show the active project */
        }
    </style>
</head>
<body>

    <!-- Profile Section -->
    <div class="profile">
        <h1>My Name</h1>
        <img src="images/profile.jpg" alt="Profile Picture">
    </div>

    <!-- Navigation Buttons -->
    <div class="nav">
        <button onclick="showProject('project1')">Project One</button>
        <button onclick="showProject('project2')">Project Two</button>
        <button onclick="showProject('project3')">Project Three</button>
    </div>

    <!-- Project Sections -->
    <div id="project1" class="project active">
        <h2>Project One</h2>
        <img src="images/project1-1.jpg" width="400">
        <img src="images/project1-2.jpg" width="400">
    </div>

    <div id="project2" class="project">
        <h2>Project Two</h2>
        <img src="images/project2-1.jpg" width="400">
        <img src="images/project2-2.jpg" width="400">
    </div>

    <div id="project3" class="project">
        <h2>Project Three</h2>
        <img src="images/project3-1.jpg" width="400">
        <img src="images/project3-2.jpg" width="400">
    </div>

    <script>
        function showProject(projectId) {
            // Hide all projects
            let projects = document.querySelectorAll('.project');
            projects.forEach(project => {
                project.classList.remove('active');
            });

            // Show the selected project
            document.getElementById(projectId).classList.add('active');
        }
    </script>

</body>
</html>
