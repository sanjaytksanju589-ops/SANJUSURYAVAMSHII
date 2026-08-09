html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <title>sanjay Portfolio</title>

  <!-- Font Awesome -->
  <link rel="stylesheet"
        href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.2/css/all.min.css">

  <style>

    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    html {
      scroll-behavior: smooth;
    }

    body {
      font-family: Arial, sans-serif;
      background: #050816;
      color: white;
    }

    /* ================= NAVBAR ================= */

    nav {
      position: fixed;
      top: 0;
      width: 100%;

      display: flex;
      justify-content: space-between;
      align-items: center;

      padding: 20px 8%;

      background: #050816dd;
      backdrop-filter: blur(15px);

      z-index: 1000;
    }

    nav h2 {
      color: #00eaff;
    }

    nav ul {
      display: flex;
      gap: 25px;
      list-style: none;
    }

    nav a {
      color: white;
      text-decoration: none;
    }

    nav a:hover {
      color: #00eaff;
    }


    /* ================= COMMON ================= */

    section {
      min-height: 100vh;
      padding: 120px 8%;
    }

    section > h2 {
      text-align: center;
      font-size: 40px;
      color: #00eaff;
      margin-bottom: 50px;
    }


    /* ================= HERO ================= */

    .hero {
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 50px;

      background:
        linear-gradient(#00eaff11 1px, transparent 1px),
        linear-gradient(90deg, #00eaff11 1px, transparent 1px);

      background-size: 50px 50px;
    }

    .hero-content {
      max-width: 600px;
    }

    .hero-content > p:first-child {
      color: #00eaff;
      letter-spacing: 3px;
    }

    .hero h1 {
      font-size: 70px;
      margin: 20px 0;
    }

    .hero h1 span {
      display: block;
      color: #00eaff;
    }

    .buttons {
      margin-top: 30px;
      display: flex;
      gap: 15px;
    }

    .btn {
      display: inline-block;
      padding: 14px 25px;

      border: 1px solid #00eaff;
      border-radius: 30px;

      color: white;
      text-decoration: none;

      transition: 0.3s;
    }

    .btn:hover {
      background: #00eaff;
      color: #001018;
      transform: translateY(-4px);
    }


    /* ================= CLOUD ================= */

    .cloud {
      width: 350px;
      height: 180px;

      border-radius: 100px;

      background: linear-gradient(
        145deg,
        white,
        #a9dfff
      );

      color: #10233e;

      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: flex-end;

      padding-bottom: 25px;

      box-shadow:
        0 0 50px #00eaff88;

      position: relative;

      animation: float 4s infinite ease-in-out;
    }

    .cloud img {
      width: 130px;
      height: 130px;

      object-fit: cover;

      border-radius: 50%;

      border: 4px solid #00eaff;

      position: absolute;
      top: -70px;
    }

    .cloud h2 {
      font-size: 25px;
    }

    @keyframes float {

      0%, 100% {
        transform: translateY(0);
      }

      50% {
        transform: translateY(-15px);
      }

    }


    /* ================= ABOUT ================= */

    .card {
      max-width: 850px;
      margin: auto;

      background: #ffffff08;

      border: 1px solid #00eaff22;

      border-radius: 20px;

      padding: 30px;

      line-height: 1.8;
    }


    /* ================= SKILLS ================= */

    .skills {
      max-width: 1000px;
      margin: auto;

      display: grid;

      grid-template-columns:
        repeat(auto-fit, minmax(180px, 1fr));

      gap: 20px;
    }

    .skill {
      text-align: center;

      background: #ffffff08;

      border: 1px solid #00eaff22;

      border-radius: 20px;

      padding: 30px;

      cursor: pointer;

      transition: 0.3s;
    }

    .skill:hover {
      transform: translateY(-8px);

      border-color: #00eaff;

      box-shadow:
        0 0 25px #00eaff33;
    }

    .skill i {
      font-size: 45px;

      color: #00eaff;

      margin-bottom: 15px;
    }

    .skill h3 {
      margin-top: 5px;
    }


    /* ================= PROJECTS ================= */

    .projects {
      display: grid;

      grid-template-columns:
        repeat(auto-fit, minmax(270px, 1fr));

      gap: 25px;
    }

    .project {
      background: #ffffff08;

      border: 1px solid #00eaff22;

      border-radius: 20px;

      padding: 30px;

      cursor: pointer;

      transition: 0.3s;
    }

    .project:hover {
      transform: translateY(-8px);

      border-color: #00eaff;

      box-shadow:
        0 0 25px #00eaff33;
    }

    .project i {
      font-size: 35px;

      color: #00eaff;

      margin-bottom: 20px;
    }

    .project h3 {
      margin-bottom: 15px;
    }

    .project p {
      color: #b7c2d5;

      line-height: 1.6;
    }


    /* ================= SOCIAL ================= */

    #contact {
      text-align: center;
    }

    .socials {
      display: flex;

      justify-content: center;

      gap: 20px;

      margin-top: 30px;
    }

    .socials a {
      width: 55px;
      height: 55px;

      display: flex;

      align-items: center;
      justify-content: center;

      border: 1px solid #00eaff;

      border-radius: 50%;

      color: white;

      transition: 0.3s;
    }

    .socials a:hover {
      background: #00eaff;

      color: black;

      transform: translateY(-5px);
    }


    /* ================= FOOTER ================= */

    footer {
      text-align: center;

      padding: 30px;

      color: #78869d;
    }


    /* ================= POPUP ================= */

    .popup {
      display: none;

      position: fixed;

      inset: 0;

      background: rgba(0, 0, 0, 0.75);

      backdrop-filter: blur(8px);

      align-items: center;
      justify-content: center;

      z-index: 5000;

      padding: 20px;
    }

    .popup.active {
      display: flex;
    }

    .popup-box {
      width: 100%;
      max-width: 600px;

      background:
        linear-gradient(
          145deg,
          #07152e,
          #050816
        );

      border: 1px solid #00eaff;

      border-radius: 25px;

      padding: 35px;

      position: relative;

      box-shadow:
        0 0 50px #00eaff44;

      animation: popupAnimation 0.3s ease;
    }

    @keyframes popupAnimation {

      from {
        transform: scale(0.8);
        opacity: 0;
      }

      to {
        transform: scale(1);
        opacity: 1;
      }

    }

    .popup-icon {
      font-size: 50px;

      color: #00eaff;

      margin-bottom: 15px;
    }

    .popup-box h2 {
      color: #00eaff;

      margin-bottom: 15px;
    }

    .popup-box p {
      color: #c4cfdf;

      line-height: 1.8;
    }

    .popup-box ul {
      margin-top: 15px;

      padding-left: 20px;

      color: #c4cfdf;

      line-height: 1.8;
    }

    .close-btn {
      position: absolute;

      top: 15px;
      right: 20px;

      width: 40px;
      height: 40px;

      border-radius: 50%;

      border: 1px solid #00eaff;

      background: transparent;

      color: white;

      font-size: 20px;

      cursor: pointer;
    }

    .close-btn:hover {
      background: #00eaff;

      color: black;
    }


    /* ================= MOBILE ================= */

    @media (max-width: 800px) {

      nav ul {
        display: none;
      }

      .hero {
        flex-direction: column;

        text-align: center;
      }

      .hero h1 {
        font-size: 50px;
      }

      .buttons {
        justify-content: center;
      }

      .cloud {
        transform: scale(0.8);
      }

    }

  </style>
</head>


<body>


  <!-- ================= NAVIGATION ================= -->

  <nav>

    <h2>BCA</h2>

    <ul>

      <li>
        <a href="#home">Home</a>
      </li>

      <li>
        <a href="#about">About</a>
      </li>

      <li>
        <a href="#skills">Skills</a>
      </li>

      <li>
        <a href="#projects">Projects</a>
      </li>

      <li>
        <a href="#contact">Contact</a>
      </li>

    </ul>

  </nav>


  <!-- ================= HERO ================= -->

  <section id="home" class="hero">

    <div class="hero-content">

      <p>WEB DEVELOPER</p>

      <h1>
        Hi, I'm
        <span>SANJAY</span>
        <style>bold</style>
      </h1>

      <p>
        Passionate about programming, web development
        and modern technology.
      </p>

      <div class="buttons">

        <a href="#projects" class="btn">
          View My Work
        </a>

        <a href="#contact" class="btn">
          Contact Me:7411244793
        </a>

      </div>

    </div>


    <div class="cloud">

      <img src="sanpg1(2).jpeg"
           alt="sanpg1(2).jpeg">

      <h2>SANJAY SURYAVAMSHII</h2>

      <p>WEB Developer</p>

    </div>

  </section>


  <!-- ================= ABOUT ================= -->

  <section id="about">

    <h2>About Me</h2>

    <div class="card">

      <p>
        I am currently pursuing Bachelor of Computer
        Applications (BCA). I enjoy learning programming,
        database management, web development and
        emerging technologies.

        My goal is to develop useful applications and
        continuously improve my technical skills.
      </p>

    </div>

  </section>


  <!-- ================= SKILLS ================= -->

  <section id="skills">

    <h2>Technical Skills</h2>

    <div class="skills">


      <!-- HTML -->

      <div class="skill"
           onclick="showSkill('html')">

        <i class="fa-brands fa-html5"></i>

        <h3>HTML</h3>

      </div>


      <!-- CSS -->

      <div class="skill"
           onclick="showSkill('css')">

        <i class="fa-brands fa-css3-alt"></i>

        <h3>CSS</h3>

      </div>


      <!-- JavaScript -->

      <div class="skill"
           onclick="showSkill('javascript')">

        <i class="fa-brands fa-js"></i>

        <h3>JavaScript</h3>

      </div>


      <!-- Java -->

      <div class="skill"
           onclick="showSkill('java')">

        <i class="fa-brands fa-java"></i>

        <h3>Java</h3>

      </div>


      <!-- SQL -->

      <div class="skill"
           onclick="showSkill('sql')">

        <i class="fa-solid fa-database"></i>

        <h3>SQL</h3>

      </div>


      <!-- GitHub -->

      <div class="skill"
           onclick="showSkill('github')">

        <i class="fa-brands fa-github"></i>

        <h3>Git & GitHub</h3>

      </div>

    </div>

  </section>


  <!-- ================= PROJECTS ================= -->

  <section id="projects">

    <h2>My Projects</h2>

    <div class="projects">


      <!-- Web Development -->

      <div class="project"
           onclick="showProject('web')">

        <i class="fa-solid fa-code"></i>

        <h3>Web Development Project</h3>

        <p>
          Click to view project information.
        </p>

      </div>


      <!-- Student Management -->

      <div class="project"
           onclick="showProject('student')">

        <i class="fa-solid fa-users"></i>

        <h3>Student Management System</h3>

        <p>
          Click to view project information.
        </p>

      </div>


      <!-- Library -->

      <div class="project"
           onclick="showProject('library')">

        <i class="fa-solid fa-book"></i>

        <h3>Library Management System</h3>

        <p>
          Click to view project information.
        </p>

      </div>

    </div>

  </section>


  <!-- ================= CONTACT ================= -->

  <section id="contact">

    <h2>Let's Connect</h2>

    <p>
      Click an icon to open the corresponding profile.
    </p>

    <div class="socials">

      <a href="#"
         onclick="openLink(PortfolioLinks.github); return false;">
        <i class="fa-brands fa-github"></i>
      </a>

      <a href="#"
         onclick="openLink(PortfolioLinks.linkedin); return false;">
        <i class="fa-brands fa-linkedin"></i>
      </a>

      <a href="#"
         onclick="openLink(PortfolioLinks.instagram); return false;">
        <i class="fa-brands fa-instagram"></i>
      </a>

      <a href="#"
         onclick="openLink(PortfolioLinks.email); return false;">
        <i class="fa-solid fa-envelope"></i>
      </a>

    </div>

  </section>


  <footer>

    © 2026 SANJAY tk| BCA Portfolio

  </footer>


  <!-- ================================================= -->
  <!-- POPUP -->
  <!-- ================================================= -->

  <div id="infoPopup" class="popup">

    <div class="popup-box">

      <button class="close-btn"
              onclick="closePopup()">
        ×
      </button>

      <div id="popupIcon"
           class="popup-icon">
      </div>

      <h2 id="popupTitle">
        Information
      </h2>

      <div id="popupContent">
      </div>

    </div>

  </div>


  <!-- ================= JAVASCRIPT ================= -->

  <script>


    /* ================================================
       SKILL INFORMATION
    ================================================= */

    const skillData = {

      html: {

        title: "HTML",

        icon: '<i class="fa-brands fa-html5"></i>',

        content: `
          <p>
            HTML stands for HyperText Markup Language.
            It is used to create the basic structure of
            websites and web pages.
          </p>

          <ul>
            <li>Creates webpage structure</li>
            <li>Uses headings, paragraphs and forms</li>
            <li>Supports images, videos and links</li>
            <li>Works together with CSS and JavaScript</li>
          </ul>
        `
      },


      css: {

        title: "CSS",

        icon: '<i class="fa-brands fa-css3-alt"></i>',

        content: `
          <p>
            CSS stands for Cascading Style Sheets.
            It is used to design and style HTML webpages.
          </p>

          <ul>
            <li>Controls colors and fonts</li>
            <li>Creates responsive layouts</li>
            <li>Adds animations and transitions</li>
            <li>Creates modern user interfaces</li>
          </ul>
        `
      },


      javascript: {

        title: "JavaScript",

        icon: '<i class="fa-brands fa-js"></i>',

        content: `
          <p>
            JavaScript is a programming language used
            to make websites interactive and dynamic.
          </p>

          <ul>
            <li>Handles button clicks</li>
            <li>Creates interactive webpages</li>
            <li>Works with HTML and CSS</li>
            <li>Can communicate with APIs</li>
          </ul>
        `
      },


      java: {

        title: "Java",

        icon: '<i class="fa-brands fa-java"></i>',

        content: `
          <p>
            Java is a popular object-oriented programming
            language used for software and application
            development.
          </p>

          <ul>
            <li>Object-oriented programming</li>
            <li>Platform independent</li>
            <li>Supports classes and objects</li>
            <li>Used in desktop and enterprise applications</li>
            <li>Useful for BCA programming projects</li>
          </ul>
        `
      },


      sql: {

        title: "SQL",

        icon: '<i class="fa-solid fa-database"></i>',

        content: `
          <p>
            SQL stands for Structured Query Language.
            It is used to store, retrieve and manage
            information in relational databases.
          </p>

          <ul>
            <li>SELECT data from databases</li>
            <li>INSERT new records</li>
            <li>UPDATE existing records</li>
            <li>DELETE records</li>
            <li>Works with MySQL and other databases</li>
          </ul>
        `
      },


      github: {

        title: "Git & GitHub",

        icon: '<i class="fa-brands fa-github"></i>',

        content: `
          <p>
            Git is a version control system and GitHub
            is a platform for storing and collaborating
            on software projects.
          </p>

          <ul>
            <li>Track code changes</li>
            <li>Store projects online</li>
            <li>Collaborate with developers</li>
            <li>Manage project versions</li>
          </ul>
        `
      }

    };


    /* ================================================
       PROJECT INFORMATION
    ================================================= */

    const projectData = {

      web: {

        title: "Web Development Project",

        icon: '<i class="fa-solid fa-code"></i>',

        content: `
          <p>
            This project focuses on creating a modern,
            responsive and user-friendly website using
            HTML, CSS and JavaScript.
          </p>

          <ul>
            <li>Responsive website design</li>
            <li>HTML for webpage structure</li>
            <li>CSS for styling and animations</li>
            <li>JavaScript for interactions</li>
            <li>Mobile and desktop support</li>
          </ul>
        `
      },


      student: {

        title: "Student Management System",

        icon: '<i class="fa-solid fa-users"></i>',

        content: `
          <p>
            A software application designed to manage
            student records and academic information.
          </p>

          <ul>
            <li>Add student information</li>
            <li>Update student records</li>
            <li>Search student details</li>
            <li>Delete records</li>
            <li>Database connectivity</li>
          </ul>

          <p>
            Technologies:
            Java, MySQL and JDBC.
          </p>
        `
      },


      library: {

        title: "Library Management System",

        icon: '<i class="fa-solid fa-book"></i>',

        content: `
          <p>
            A library management application used to
            manage books, students and issue/return
            transactions.
          </p>

          <ul>
            <li>Add and manage books</li>
            <li>Search books</li>
            <li>Issue books</li>
            <li>Return books</li>
            <li>Manage student information</li>
          </ul>

          <p>
            Technologies:
            Java, SQL and Database Management.
          </p>
        `
      }

    };


    /* ================================================
       SHOW SKILL
    ================================================= */

    function showSkill(skillName) {

      const skill = skillData[skillName];

      if (!skill) {
        return;
      }

      document.getElementById("popupIcon").innerHTML =
        skill.icon;

      document.getElementById("popupTitle").innerText =
        skill.title;

      document.getElementById("popupContent").innerHTML =
        skill.content;

      document.getElementById("infoPopup")
        .classList.add("active");
    }


    /* ================================================
       SHOW PROJECT
    ================================================= */

    function showProject(projectName) {

      const project = projectData[projectName];

      if (!project) {
        return;
      }

      document.getElementById("popupIcon").innerHTML =
        project.icon;

      document.getElementById("popupTitle").innerText =
        project.title;

      document.getElementById("popupContent").innerHTML =
        project.content;

      document.getElementById("infoPopup")
        .classList.add("active");
    }


    /* ================================================
       CLOSE POPUP
    ================================================= */

    function closePopup() {

      document.getElementById("infoPopup")
        .classList.remove("active");

    }


    /* ================================================
       CLOSE WHEN CLICKING OUTSIDE
    ================================================= */

    document.getElementById("infoPopup")
      .addEventListener("click", function(event) {

        if (event.target === this) {
          closePopup();
        }

      });


    /* ================================================
       ESC KEY CLOSE
    ================================================= */

    document.addEventListener("keydown", function(event) {

      if (event.key === "Escape") {
        closePopup();
      }

    });


    /* ================================================
       SOCIAL LINK LIBRARY
    ================================================= */

    const PortfolioLinks = {

      github:
        "https://github.com/sanjaytksanju589-ops",

      linkedin:
        "https://www.linkedin.com/posts/sanju-sanjay-084a9a386_ibmskillsbuild-customerengagement-careerdevelopment-ugcPost-7376918733430145024-MRyU/?utm_source=share&utm_medium=member_android&rcm=ACoAAF8zdOQBE1Iw9cMA27d8fUqPFZoIf2WwQaU",

      instagram:
        "https://www.instagram.com/sanju_suryavamshii?igsh=MXFkb2pocG5rcGMxbA==",

      email:
        "mailto:sanjaytksanju@gmail.com",
                  

      open: function(url) {

        if (!url) {
          return;
        }

        if (url.startsWith("mailto:")) {

          window.location.href = url;

        } else {

          window.open(
            url,
            "_blank",
            "noopener,noreferrer"
          );

        }

      }

    };


    function openLink(url) {

      PortfolioLinks.open(url);

    }

  </script>

</body>
</html>
```
