#  <!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="theme-color" content="#070b18">
<title>Madjuri | IT Portfolio</title>

<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&display=swap" rel="stylesheet">

<style>
:root {
  --bg: #070b18;
  --card: rgba(16, 29, 52, .78);
  --blue: #3984ff;
  --cyan: #35e5ff;
  --white: #f4f8ff;
  --muted: #a2b1cb;
}

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

html {
  scroll-behavior: smooth;
  scroll-padding-top: 85px;
}

body {
  background: var(--bg);
  color: var(--white);
  font-family: 'Inter', sans-serif;
  overflow-x: hidden;
  line-height: 1.7;
}

a {
  text-decoration: none;
  color: inherit;
}

.container {
  width: min(1100px, 90%);
  margin: auto;
}

header {
  position: sticky;
  top: 0;
  z-index: 100;
  background: rgba(7, 11, 24, .85);
  backdrop-filter: blur(18px);
  border-bottom: 1px solid #1a2943;
}

nav {
  min-height: 75px;
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.logo {
  font-size: 1.4rem;
  font-weight: 800;
}

.logo span, .gradient {
  color: var(--cyan);
  text-shadow: 0 0 22px #35e5ff55;
}

.nav-links {
  display: flex;
  gap: 25px;
  list-style: none;
}

.nav-links a {
  color: var(--muted);
  transition: .3s;
}

.nav-links a:hover {
  color: var(--cyan);
}

.menu-btn {
  display: none;
  background: none;
  color: white;
  border: 1px solid #30415e;
  border-radius: 8px;
  padding: 5px 11px;
  font-size: 1.4rem;
}

.hero {
  min-height: 88vh;
  display: grid;
  grid-template-columns: 1.2fr .8fr;
  align-items: center;
  gap: 45px;
  position: relative;
}

.hero::before {
  content: "";
  position: absolute;
  width: 400px;
  height: 400px;
  background: #155dff25;
  filter: blur(100px);
  border-radius: 50%;
  left: 10%;
  top: 15%;
  z-index: -1;
  animation: glow 6s infinite alternate;
}

.intro {
  animation: appear 1s ease both;
}

.eyebrow {
  display: inline-block;
  color: var(--cyan);
  border: 1px solid #35e5ff44;
  background: #35e5ff0b;
  padding: 7px 14px;
  border-radius: 30px;
  font-size: .8rem;
  margin-bottom: 20px;
}

h1 {
  font-size: clamp(2.7rem, 5vw, 4.7rem);
  line-height: 1.12;
  letter-spacing: -2px;
  margin-bottom: 22px;
}

.intro p, .section-desc {
  color: var(--muted);
  margin-bottom: 28px;
}

.buttons {
  display: flex;
  flex-wrap: wrap;
  gap: 14px;
}

.btn {
  display: inline-block;
  padding: 12px 21px;
  border-radius: 10px;
  font-weight: 700;
  transition: .3s;
}

.primary {
  color: #061020;
  background: linear-gradient(110deg, var(--cyan), #79aaff);
}

.secondary {
  border: 1px solid #30415e;
}

.btn:hover {
  transform: translateY(-4px);
  box-shadow: 0 0 25px #35e5ff35;
}

/* Profile picture */

.profile-area {
  display: flex;
  justify-content: center;
  align-items: center;
  animation: appear 1.2s ease both;
}

.profile-frame {
  width: min(330px, 75vw);
  aspect-ratio: 1;
  padding: 7px;
  border-radius: 50%;
  position: relative;
  background: conic-gradient(
    from 0deg,
    var(--cyan),
    #2563ff,
    #9d5cff,
    var(--cyan)
  );
  box-shadow: 0 0 25px #35e5ff40,
              0 0 80px #2563ff20;
  animation: float 4s ease-in-out infinite;
}

.profile-frame::before {
  content: "";
  position: absolute;
  inset: -12px;
  border: 1px solid #35e5ff55;
  border-radius: 50%;
  animation: rotate 12s linear infinite;
}

.profile-frame img {
  display: block;
  width: 100%;
  height: 100%;
  object-fit: cover;
  object-position: center;
  border-radius: 50%;
  border: 5px solid var(--bg);
  background: #101a30;
}

.status {
  position: absolute;
  bottom: 12%;
  right: -5px;
  background: #10223a;
  border: 1px solid #35e5ff77;
  color: var(--cyan);
  padding: 8px 13px;
  border-radius: 30px;
  font-size: .75rem;
  box-shadow: 0 0 20px #35e5ff20;
}

/* Sections */

section:not(.hero) {
  padding: 85px 0;
}

.section-title {
  margin-bottom: 32px;
}

.section-title small {
  color: var(--cyan);
  letter-spacing: 3px;
  font-weight: 700;
}

.section-title h2 {
  font-size: clamp(2rem, 4vw, 3rem);
  line-height: 1.25;
  margin-top: 8px;
}

.glass {
  padding: 28px;
  border-radius: 18px;
  border: 1px solid #7895c426;
  background: var(--card);
  backdrop-filter: blur(14px);
  transition: transform .35s, border-color .35s,
              box-shadow .35s;
}

.glass:hover {
  transform: translateY(-6px);
  border-color: #35e5ff88;
  box-shadow: 0 12px 35px #0003, 0 0 22px #35e5ff0b;
}

.glass p {
  color: var(--muted);
}

.grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 20px;
}

.skill-icon {
  font-size: 2rem;
  margin-bottom: 10px;
}

.glass h3 {
  margin-bottom: 7px;
}

.project-icon {
  font-size: 2.8rem;
  margin-bottom: 12px;
}

.tags {
  display: flex;
  flex-wrap: wrap;
  gap: 8px;
  margin: 16px 0;
}

.tags span {
  color: var(--cyan);
  background: #35e5ff0c;
  border: 1px solid #35e5ff30;
  padding: 3px 9px;
  border-radius: 6px;
  font-size: .75rem;
}

.project-link {
  color: var(--cyan);
  font-weight: 600;
}

.contact {
  text-align: center;
  padding: 40px 25px !important;
}

.contact .section-desc {
  max-width: 550px;
  margin: 15px auto 25px;
}

footer {
  text-align: center;
  color: var(--muted);
  padding: 25px 0;
  border-top: 1px solid #1a2943;
  font-size: .85rem;
}

/* Scroll animations */

.reveal {
  opacity: 0;
  transform: translateY(25px);
  transition: opacity .7s ease, transform .7s ease;
}

.reveal.visible {
  opacity: 1;
  transform: translateY(0);
}

@keyframes appear {
  from { opacity: 0; transform: translateY(25px); }
  to { opacity: 1; transform: translateY(0); }
}

@keyframes float {
  0%, 100% { transform: translateY(0); }
  50% { transform: translateY(-12px); }
}

@keyframes rotate {
  to { transform: rotate(360deg); }
}

@keyframes glow {
  from { transform: scale(1); }
  to { transform: scale(1.2) translate(20px, -15px); }
}

@media (max-width: 800px) {
  .hero {
    grid-template-columns: 1fr;
    text-align: center;
    padding-top: 65px;
    gap: 45px;
  }

  .intro {
    order: 2;
  }

  .profile-area {
    order: 1;
  }

  .buttons {
    justify-content: center;
  }

  .profile-frame {
    width: min(260px, 65vw);
  }

  .grid {
    grid-template-columns: repeat(2, 1fr);
  }

  .menu-btn {
    display: block;
    cursor: pointer;
  }

  .nav-links {
    display: none;
    position: absolute;
    top: 75px;
    left: 0;
    right: 0;
    background: #0b1224;
    padding: 22px 5%;
    flex-direction: column;
    gap: 16px;
    border-bottom: 1px solid #30415e;
  }

  .nav-links.open {
    display: flex;
  }
}

@media (max-width: 520px) {
  .grid {
    grid-template-columns: 1fr;
  }

  section:not(.hero) {
    padding: 65px 0;
  }

  h1 {
    letter-spacing: -1px;
  }

  .glass {
    padding: 23px;
  }
}

@media (prefers-reduced-motion: reduce) {
  *, *::before, *::after {
    animation: none !important;
    scroll-behavior: auto !important;
    transition: none !important;
  }

  .reveal {
    opacity: 1;
    transform: none;
  }
}
</style>
</head>

<body>

<header>
  <nav class="container">
    <a class="logo" href="#home">MADJURI<span>.</span></a>

    <button class="menu-btn" id="menuBtn"
      aria-label="Open menu" aria-expanded="false">☰</button>

    <ul class="nav-links" id="navLinks">
      <li><a href="#home">Home</a></li>
      <li><a href="#about">About</a></li>
      <li><a href="#skills">Skills</a></li>
      <li><a href="#projects">Projects</a></li>
      <li><a href="#contact">Contact</a></li>
    </ul>
  </nav>
</header>

<main>
  <section class="hero container" id="home">

    <div class="intro">
      <span class="eyebrow">WELCOME TO MY PORTFOLIO</span>

      <h1>
        Hi, I'm <span class="gradient">Madjuri</span><br>
        Future IT Professional.
      </h1>

      <p>
        An aspiring IT professional passionate about technology,
        programming, networking, and modern web design.
        Learning today, building for tomorrow.
      </p>

      <div class="buttons">
        <a href="#projects" class="btn primary">Explore Projects ↗</a>
        <a href="#contact" class="btn secondary">Contact Me</a>
      </div>
    </div>

    <div class="profile-area">
      <div class="profile-frame">
        <!-- Put Profile.jpg beside index.html -->
        <img src="profile.jpg" alt="My Profile Picture">
          onerror="this.style.visibility='hidden'">
        <span class="status">● IT Student</span>
      </div>
    </div>

  </section>

  <section id="about">
    <div class="container reveal">
      <div class="section-title">
        <small>01 / ABOUT ME</small>
        <h2>Who <span class="gradient">I Am</span></h2>
      </div>

      <div class="glass">
        <p>
          Hello! I'm Madjuri, an Information Technology student
          interested in web development, programming, and computer
          networking. I enjoy learning new skills and creating
          projects that turn ideas into practical digital experiences.
          My goal is to continue improving and become a skilled IT
          professional.
        </p>
      </div>
    </div>
  </section>

  <section id="skills">
    <div class="container reveal">
      <div class="section-title">
        <small>02 / MY SKILLS</small>
        <h2>What I'm <span class="gradient">Learning</span></h2>
      </div>

      <div class="grid">
        <article class="glass">
          <div class="skill-icon">🌐</div>
          <h3>HTML</h3>
          <p>Creating the structure of web pages.</p>
        </article>

        <article class="glass">
          <div class="skill-icon">🎨</div>
          <h3>CSS</h3>
          <p>Designing layouts, effects, and animations.</p>
        </article>

        <article class="glass">
          <div class="skill-icon">💻</div>
          <h3>Programming</h3>
          <p>Learning coding fundamentals and logic.</p>
        </article>

        <article class="glass">
          <div class="skill-icon">🖧</div>
          <h3>Networking</h3>
          <p>Understanding IP addresses, routers, and switches.</p>
        </article>

        <article class="glass">
          <div class="skill-icon">⚙️</div>
          <h3>GitHub</h3>
          <p>Managing and publishing website projects.</p>
        </article>

        <article class="glass">
          <div class="skill-icon">🚀</div>
          <h3>Problem Solving</h3>
          <p>Developing solutions through technology.</p>
        </article>
      </div>
    </div>
  </section>

  <section id="projects">
    <div class="container reveal">
      <div class="section-title">
        <small>03 / MY WORK</small>
        <h2>Featured <span class="gradient">Projects</span></h2>
      </div>

      <div class="grid">
        <article class="glass">
          <div class="project-icon">🌌</div>
          <h3>Personal Portfolio</h3>
          <p>A website introducing my background,
            learning journey, and projects.</p>
          <div class="tags">
            <span>HTML</span><span>CSS</span><span>JavaScript</span>
          </div>
          <a class="project-link"
            href="https://madjuriadznel-pixel.github.io/Portfolio---Madjuri-/"
            target="_blank" rel="noopener noreferrer">
            View Website ↗
          </a>
        </article>

        <article class="glass">
          <div class="project-icon">💡</div>
          <h3>Upcoming Project</h3>
          <p>A space for my next web development or
            information technology project.</p>
          <div class="tags">
            <span>Web Design</span><span>IT</span>
          </div>
          <a class="project-link" href="#contact">Get in Touch ↗</a>
        </article>
      </div>
    </div>
  </section>

  <section id="contact">
    <div class="container reveal">
      <div class="glass contact">
        <div class="section-title">
          <small>04 / CONTACT</small>
          <h2>Let's Connect <span class="gradient">!</span></h2>
        </div>

        <p class="section-desc">
          Interested in my projects or learning journey?
          Visit my GitHub profile to see my work.
        </p>

        <a class="btn primary"
          href="https://github.com/madjuriadznel-pixel"
          target="_blank" rel="noopener noreferrer">
          Visit My GitHub ↗
        </a>
      </div>
    </div>
  </section>
</main>

<footer>
  <div class="container">
    © <span id="year"></span> Madjuri | Designed with HTML, CSS & JavaScript
  </div>
</footer>

<script>
const menuBtn = document.getElementById("menuBtn");
const navLinks = document.getElementById("navLinks");

menuBtn.addEventListener("click", () => {
  const open = navLinks.classList.toggle("open");
  menuBtn.setAttribute("aria-expanded", String(open));
  menuBtn.setAttribute("aria-label", open ? "Close menu" : "Open menu");
  menuBtn.textContent = open ? "✕" : "☰";
});

navLinks.querySelectorAll("a").forEach(link => {
  link.addEventListener("click", () => {
    navLinks.classList.remove("open");
    menuBtn.setAttribute("aria-expanded", "false");
    menuBtn.setAttribute("aria-label", "Open menu");
    menuBtn.textContent = "☰";
  });
});

const observer = new IntersectionObserver(entries => {
  entries.forEach(entry => {
    if (entry.isIntersecting) {
      entry.target.classList.add("visible");
      observer.unobserve(entry.target);
    }
  });
}, { threshold: 0.12 });

document.querySelectorAll(".reveal").forEach(el => {
  observer.observe(el);
});

document.getElementById("year").textContent =
  new Date().getFullYear();
</script>

</body>
</html>

