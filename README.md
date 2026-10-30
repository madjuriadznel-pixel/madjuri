<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Adznel J. Madjuri | Portfolio</title>

<style>

/* GENERAL SETTINGS */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    scroll-behavior: smooth;
}

body {
    font-family: 'Arial', sans-serif;
    background: #071426;
    color: white;
    overflow-x: hidden;
}

/* ANIMATED BACKGROUND */
body::before {
    content: "";
    position: fixed;
    width: 400px;
    height: 400px;
    background: #087bff;
    filter: blur(160px);
    opacity: 0.3;
    top: -100px;
    left: -100px;
    z-index: -1;
}

body::after {
    content: "";
    position: fixed;
    width: 400px;
    height: 400px;
    background: #00d4ff;
    filter: blur(160px);
    opacity: 0.2;
    bottom: -100px;
    right: -100px;
    z-index: -1;
}

/* NAVIGATION */
nav {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 20px 8%;
    background: rgba(7, 20, 38, 0.85);
    backdrop-filter: blur(15px);
    position: sticky;
    top: 0;
    z-index: 100;
    border-bottom: 1px solid rgba(0, 195, 255, 0.2);
}

.logo {
    color: #00d4ff;
    font-size: 23px;
    font-weight: bold;
    letter-spacing: 2px;
}

nav a {
    color: white;
    text-decoration: none;
    margin-left: 20px;
    transition: 0.3s;
}

nav a:hover {
    color: #00d4ff;
}

/* HERO SECTION */
.hero {
    min-height: 90vh;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-wrap: wrap;
    gap: 60px;
    padding: 70px 8%;
}

.profile {
    width: 260px;
    height: 260px;
    border-radius: 50%;
    padding: 7px;
    background: linear-gradient(135deg, #00d4ff, #0866ff);
    box-shadow: 0 0 30px #008cff;
    animation: float 4s ease-in-out infinite;
}

.profile img {
    width: 100%;
    height: 100%;
    border-radius: 50%;
    object-fit: cover;
    border: 4px solid #071426;
}

.hero-text {
    max-width: 550px;
    animation: slideUp 1.2s ease;
}

.hero-text h3 {
    color: #00d4ff;
    font-size: 22px;
}

.hero-text h1 {
    font-size: 45px;
    margin: 15px 0;
}

.hero-text h1 span {
    color: #00d4ff;
}

.hero-text p {
    color: #b9c9dc;
    line-height: 1.8;
    font-size: 17px;
}

.btn {
    display: inline-block;
    margin-top: 25px;
    padding: 13px 30px;
    background: #00bfff;
    color: #071426;
    text-decoration: none;
    border-radius: 30px;
    font-weight: bold;
    transition: 0.4s;
}

.btn:hover {
    background: white;
    box-shadow: 0 0 25px #00d4ff;
    transform: translateY(-5px);
}

/* SECTIONS */
section {
    padding: 75px 8%;
    text-align: center;
}

.section-title {
    font-size: 32px;
    margin-bottom: 35px;
    color: #00d4ff;
}

/* GLASS CARDS */
.card-container {
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
    gap: 25px;
}

.card {
    background: rgba(255,255,255,0.06);
    border: 1px solid rgba(0,212,255,0.25);
    backdrop-filter: blur(15px);
    padding: 30px;
    border-radius: 18px;
    width: 280px;
    transition: 0.4s;
    animation: slideUp 1s ease;
}

.card:hover {
    transform: translateY(-12px);
    box-shadow: 0 0 25px rgba(0,212,255,0.3);
    border-color: #00d4ff;
}

.card h3 {
    color: #00d4ff;
    margin-bottom: 15px;
    font-size: 22px;
}

.card p {
    color: #c4d2e3;
    line-height: 1.7;
}

/* ABOUT */
.about-text {
    max-width: 750px;
    margin: auto;
    color: #c4d2e3;
    font-size: 18px;
    line-height: 1.9;
}

/* SKILLS */
.skills {
    max-width: 750px;
    margin: auto;
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 15px;
}

.skill {
    padding: 13px 25px;
    background: rgba(0,190,255,0.12);
    border: 1px solid #00bfff;
    color: #00d4ff;
    border-radius: 25px;
    transition: 0.3s;
}

.skill:hover {
    background: #00bfff;
    color: #071426;
    transform: scale(1.1);
}

/* CONTACT */
.contact p {
    margin: 15px;
    color: #c4d2e3;
    font-size: 17px;
}

/* FOOTER */
footer {
    padding: 25px;
    text-align: center;
    background: #030c18;
    color: #8ca4bd;
    border-top: 1px solid rgba(0,212,255,0.2);
}

/* ANIMATIONS */
@keyframes float {
    0%, 100% {
        transform: translateY(0);
    }
    50% {
        transform: translateY(-18px);
    }
}

@keyframes slideUp {
    from {
        opacity: 0;
        transform: translateY(40px);
    }
    to {
        opacity: 1;
        transform: translateY(0);
    }
}

/* MOBILE RESPONSIVE */
@media (max-width: 768px) {

    nav {
        flex-direction: column;
        gap: 15px;
    }

    nav a {
        margin: 5px;
        font-size: 13px;
    }

    .hero {
        flex-direction: column;
        text-align: center;
        gap: 35px;
    }

    .profile {
        width: 210px;
        height: 210px;
    }

    .hero-text h1 {
        font-size: 32px;
    }

    .hero-text h3 {
        font-size: 18px;
    }

    section {
        padding: 55px 6%;
    }

    .section-title {
        font-size: 27px;
    }

    .card {
        width: 100%;
    }
}

</style>
</head>

<body>

<!-- NAVIGATION -->
<nav>
    <div class="logo">ADZNEL.</div>

    <div>
        <a href="#home">Home</a>
        <a href="#about">About</a>
        <a href="#skills">Skills</a>
        <a href="#projects">Projects</a>
        <a href="#contact">Contact</a>
    </div>
</nav>

<!-- HOME -->
<section class="hero" id="home">

    <div class="profile">
    <img src="profile.jpg" alt="Adznel's Profile Picture">
</div>

    <div class="hero-text">
        <h3>Hello, Welcome to My Portfolio!</h3>

        <h1>I'm <span>Adznel J. Madjuri</span></h1>

        <p>
            I am an Information Technology student
            at MSU-SULU College. I love programming,
            web development, networking, and exploring
            modern technologies.
        </p>

        <a href="#about" class="btn">Explore More</a>
    </div>

</section>

<!-- ABOUT -->
<section id="about">

    <h2 class="section-title">About Me</h2>

    <p class="about-text">
        My name is Adznel J. Madjuri. I am an IT student
        who enjoys learning new technologies and
        developing creative digital projects.
        My goal is to improve my programming skills
        and become a successful IT professional.
    </p>

</section>

<!-- SKILLS -->
<section id="skills">

    <h2 class="section-title">My Skills</h2>

    <div class="skills">
        <div class="skill">HTML</div>
        <div class="skill">CSS</div>
        <div class="skill">JavaScript</div>
        <div class="skill">C++</div>
        <div class="skill">Networking</div>
        <div class="skill">Web Development</div>
    </div>

</section>

<!-- PROJECTS -->
<section id="projects">

    <h2 class="section-title">My Projects</h2>

    <div class="card-container">

        <div class="card">
            <h3>Personal Portfolio</h3>
            <p>
                A modern personal website
                showcasing my profile, skills,
                and personal information.
            </p>
        </div>

        <div class="card">
            <h3>Network Learning</h3>
            <p>
                A learning website about computer
                networking, devices, Wi-Fi,
                routers, and IP addresses.
            </p>
        </div>

        <div class="card">
            <h3>Arduino Project</h3>
            <p>
                An automatic vehicle gate detector
                concept using Arduino technology.
            </p>
        </div>

    </div>

</section>

<!-- CONTACT -->
<section id="contact" class="contact">

    <h2 class="section-title">Contact Me</h2>

    <p>Email: madjuriadznel@gmail.com</p>
    <p>Location: Alat, Jolo, Sulu</p>

    <a href="mailto:madjuriadznel@gmail.com" class="btn">
        Send Me an Email
    </a>

</section>

<!-- PERSONAL INFORMATION -->
<section>

    <h2 class="section-title">Personal Information</h2>

    <div class="card-container">

        <div class="card">
            <h3>Full Name</h3>
            <p>Adznel J. Madjuri</p>
        </div>

        <div class="card">
            <h3>Course</h3>
            <p>Information Technology</p>
        </div>

        <div class="card">
            <h3>College</h3>
            <p>MSU-SULU College</p>
        </div>

    </div>

</section>

<!-- FOOTER -->
<footer>
    <p>© 2026 Adznel J. Madjuri | My Personal Portfolio</p>
    <p>Designed with HTML & CSS</p>
</footer>

</body>
</html>
