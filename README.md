<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Suvajit Ghosh | Developer Portfolio</title>
  <link rel="stylesheet" href="style.css" />
<!--   <link href="https://unpkg.com/aos@2.3.1/dist/aos.css" rel="stylesheet"> -->
  <style>
    :root {
  --primary: #1dbf73;
  --dark: #0d1117;
  --light: #f0f0f0;
  --accent: #ffffff;
}

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: 'Segoe UI', sans-serif;
  background: var(--dark);
  color: var(--accent);
  scroll-behavior: smooth;
  padding-top: 70px;
}

/* NAVBAR */
header {
  background: #161b22;
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  z-index: 1000;
  box-shadow: 0 2px 5px rgba(0,0,0,0.3);
}

.nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 1rem;
  max-width: 1100px;
  margin: auto;
}

.logo {
  font-size: 1.8rem;
  color: var(--accent);
}

.logo span {
  color: var(--primary);
}

.menu-toggle {
  display: none;
  font-size: 2rem;
  cursor: pointer;
  color: white;
}

.menu {
  display: flex;
  align-items: center;
}

.menu a {
  color: white;
  font-weight: bold;
  text-decoration: none;
  margin-left: 1rem;
  padding: 0.4rem 0.6rem;
  border-radius: 4px;
  transition: background 0.3s;
}

.menu a:hover {
  background: rgba(255, 255, 255, 0.1);
  color: var(--primary);
}

/* BUTTON */
.btn {
  background: var(--primary);
  padding: 8px 14px;
  border-radius: 5px;
  color: #fff !important;
  font-weight: 600;
  text-decoration: none;
  margin-left: 1rem;
  display: inline-block;
}

/* THEME SWITCH */
.theme-switch {
  margin-left: 1rem;
  cursor: pointer;
}

.theme-switch input {
  display: none;
}

.slider {
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 24px;
  width: 36px;
  height: 36px;
  background: #333;
  border-radius: 50%;
  transition: 0.4s;
  color: white;
}

.slider::before {
  content: '🌙';
}

/* LIGHT MODE */
body.light-mode {
  background: white;
  color: black;
}

body.light-mode header {
  background: #f1f1f1;
}

body.light-mode .logo {
  color: black;
}

body.light-mode .menu a {
  color: black;
}

body.light-mode .slider {
  background: #ffd700;
}

body.light-mode .slider::before {
  content: '☀️';
}

/* HERO */
.hero {
  text-align: center;
  padding: 6rem 1rem 4rem;
}

.hero h2 {
  font-size: 2.5rem;
}

.hero span {
  color: var(--primary);
}

.hero p {
  margin-top: 1rem;
  margin-bottom: 1rem;
  font-size: 1.3rem;
  overflow: hidden;
  white-space: nowrap;
}

#typing-text {
  display: inline-block;
  max-width: 100%;
}

/* SECTION */
.section {
  padding: 4rem 1rem;
  max-width: 1100px;
  margin: auto;
}
.section h2 {
  text-align: center;
  font-size: 2rem;
  color: var(--primary);
  margin-bottom: 1.5rem;
}

/* SKILLS */
.skills-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(120px, 1fr));
  gap: 1rem;
  text-align: center;
}

.skill {
  background: #161b22;
  padding: 1rem;
  border-radius: 6px;
  transition: 0.3s;
}

.skill:hover {
  background: #1dbf7399;
}

/* PROJECTS */
.project-grid {
  display: grid;
  gap: 2rem;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
}

.project-card {
  background: #161b22;
  border-radius: 10px;
  padding: 1.5rem;
  transition: 0.3s;
}

.project-card:hover {
  transform: scale(1.03);
  background: #1dbf7322;
}

/* CONTACT */
.contact-section form {
  max-width: 600px;
  margin: auto;
}

.form-group {
  margin-bottom: 1rem;
}

input,
textarea {
  width: 100%;
  padding: 12px;
  border: none;
  border-radius: 5px;
  background: #222;
  color: #fff;
}

textarea {
  resize: none;
}
button.btn {
  display: block;
  margin: 1.5rem auto 0;
  padding: 10px 20px;
  font-size: 1rem;
  cursor: pointer;
  border: none;
}
/* MODAL */
.modal {
  display: none;
  position: fixed;
  z-index: 999;
  padding: 60px;
  left: 0;
  top: 0;
  width: 100%;
  height: 100%;
  overflow: auto;
  background: rgba(0, 0, 0, 0.8);
}

.modal-content {
  background: #161b22;
  margin: auto;
  padding: 20px;
  border-radius: 10px;
  width: 80%;
  color: #fff;
}

.close {
  float: right;
  font-size: 28px;
  cursor: pointer;
}

/* SCROLL TO TOP BUTTON */
#scrollTopBtn {
  position: fixed;
  bottom: 30px;
  right: 20px;
  display: none;
  background: var(--primary);
  color: #fff;
  border: none;
  border-radius: 50%;
  font-size: 20px;
  padding: 10px 14px;
  cursor: pointer;
  z-index: 1000;
}

/* FOOTER */
footer {
  background: #161b22;
  text-align: center;
  padding: 1rem;
  color: #888;
  margin-top: 2rem;
}

/* LIGHT MODE Overrides */
body.light-mode .skill,
body.light-mode .project-card,
body.light-mode .modal-content,
body.light-mode #scrollTopBtn {
  background: #f1f1f1;
  color: #000;
}

body.light-mode input,
body.light-mode textarea {
  background: #fff;
  color: #000;
  border: 1px solid #ccc;
}

/* RESPONSIVE */
@media (max-width: 768px) {
  .menu-toggle {
    display: block;
  }

  .menu {
    flex-direction: column;
    position: absolute;
    top: 100%;
    left: 0;
    background: #161b22;
    width: 100%;
    display: none;
  }

  .menu.show {
    display: flex;
  }

  .menu a {
    margin: 0.5rem 0;
    padding: 0.5rem 1rem;
  }

  .hero h2 {
    font-size: 2rem;
  }

  .hero p {
    font-size: 1rem;
  }
}

@media (max-width: 480px) {
  .hero {
    padding: 4rem 1rem;
  }

  .btn {
    padding: 6px 10px;
    font-size: 0.9rem;
  }

  #scrollTopBtn {
    bottom: 20px;
    right: 10px;
  }
}
/* ABOUT SECTION */
#about {
  background-color: #0d1117;
  text-align: center;
  padding: 4rem 1rem;
}

#about h2 {
  font-size: 2rem;
  color: var(--primary);
  margin-bottom: 1.5rem;
}

#about p {
  font-size: 1.1rem;
  color: #ccc;
  max-width: 850px;
  margin: 1rem auto;
  line-height: 1.8;
}

.about-list-container {
  max-width: 800px;
  margin: 1.5rem auto;
}

.about-list {
  list-style: none;
  padding: 0;
  margin: 1rem 0;
  text-align: left;
  color: #aaa;
}

.about-list li {
  margin-bottom: 0.6rem;
  position: relative;
  padding-left: 1.5rem;
  font-size: 1rem;
}

.about-list li::before {
  content: "✔";
  position: absolute;
  left: 0;
  color: var(--primary);
  font-weight: bold;
}

#about a {
  color: var(--primary);
  font-weight: bold;
  text-decoration: none;
}

#about a:hover {
  text-decoration: underline;
}

/* LIGHT MODE SUPPORT */
body.light-mode #about {
  background-color: #f9f9f9;
}

body.light-mode #about p,
body.light-mode .about-list li {
  color: #333;
}

body.light-mode .about-list li::before {
  color: var(--primary);
}

  </style>
</head>
<body>

  <!-- NAVBAR -->
  <header>
    <div class="container nav">
      <h1 class="logo">Suvajit<span>Dev</span></h1>
      <div class="menu-toggle" id="menu-toggle">☰</div>
      <div class="menu" id="menu">
        <a href="#home">Home</a>
        <a href="#skills">Skills</a>
        <a href="#projects">Projects</a>
        <a href="#contact">Contact</a>
        <a href="https://www.fiverr.com/codewithsuvajit" class="btn" target="_blank">Hire Me</a>
        <a href="admin.html" class="btn" target="_blank">Admin Panel</a>
        <label class="theme-switch">
          <input type="checkbox" id="theme-toggle">
          <span class="slider"></span>
        </label>
      </div>
    </div>
  </header>

  <!-- HERO -->
  <section id="home" class="hero">
    <div class="container">
      <h2>Hello, I'm <span>Suvajit Ghosh</span></h2>
      <p><span id="typing-text"></span></p>
      <a href="assets/Suvajit_Ghosh_Resume.pdf" class="btn" download>Download Resume</a>
    </div>
  </section>

  <!-- ABOUT -->
  <!-- ABOUT SECTION -->
<section id="about" class="section">
  <div class="container">
    <h2>About Me</h2>
    <p>
      👋 Hi, I’m <strong>Suvajit Ghosh</strong> — a results-driven <strong>Full Stack Developer</strong> with over <strong>3 years of experience</strong> delivering custom websites, web apps, and smart business solutions.
    </p>
    <p>
      I specialize in building <strong>responsive, high-performance web applications</strong> using technologies like <strong>React.js, Node.js, Firebase, Python, WordPress</strong>, and modern JavaScript frameworks.
    </p>
    <p>
      From landing pages and eCommerce platforms to chatbots and admin dashboards — I turn complex requirements into clean, scalable, and user-friendly digital products.
    </p>
    <div class="about-list-container">
      <p>🚀 I’m passionate about:</p>
      <ul class="about-list">
        <li>Crafting beautiful, functional UIs</li>
        <li>Writing clean, maintainable code</li>
        <li>Optimizing for speed, SEO & mobile responsiveness</li>
        <li>Collaborating with businesses to bring their vision to life</li>
      </ul>
    </div>
    <p>
      💼 Whether you’re a startup, agency, or entrepreneur, I’m here to help you <strong>build faster, smarter, and better.</strong>
    </p>
    <p>
      📩 <strong>Let’s talk!</strong> Need a developer you can rely on? <a href="#contact">Contact me below</a> or <a href="https://www.fiverr.com/codewithsuvajit" target="_blank">Hire me on Fiverr</a> to get started today.
    </p>
  </div>
</section>


  <!-- SKILLS -->
  <section id="skills" class="section">
    <div class="container">
      <h2>Skills</h2>
      <div class="skills-grid">
        <div class="skill">HTML5</div>
        <div class="skill">CSS3</div>
        <div class="skill">JavaScript</div>
        <div class="skill">React.js</div>
        <div class="skill">WordPress</div>
        <div class="skill">Python</div>
        <div class="skill">Firebase</div>
        <div class="skill">Git & GitHub</div>
      </div>
    </div>
  </section>

  <!-- PROJECTS -->
  <section id="projects" class="section">
    <div class="container">
      <h2>Projects</h2>
      <div class="project-grid">
        <div class="project-card" data-aos="fade-up">
          <img src="assets/project1.jpg" alt="Landing Page">
          <div class="card-content">
            <h3>Startup Landing Page</h3>
            <p>Responsive SaaS landing page using HTML, CSS, JS.</p>
            <a href="#" class="btn view-more" data-project="1">View More</a>
          </div>
        </div>
        <div class="project-card" data-aos="fade-up" data-aos-delay="100">
          <img src="assets/project2.jpg" alt="React Task App">
          <div class="card-content">
            <h3>React Task Manager</h3>
            <p>Productivity tool with filters and dark mode.</p>
            <a href="#" class="btn view-more" data-project="2">View More</a>
          </div>
        </div>
        <div class="project-card" data-aos="fade-up" data-aos-delay="200">
          <img src="assets/project3.jpg" alt="WordPress Site">
          <div class="card-content">
            <h3>Bakery WordPress Website</h3>
            <p>Custom WordPress site with menu and gallery.</p>
            <a href="#" class="btn view-more" data-project="3">View More</a>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- CONTACT -->
  <section id="contact" class="section contact-section">
    <div class="container">
      <h2>Contact Me</h2>
      <form id="contact-form">
        <div class="form-group"><input type="text" placeholder="Your Name" required></div>
        <div class="form-group"><input type="email" placeholder="Your Email" required></div>
        <div class="form-group"><textarea placeholder="Your Message" required></textarea></div>
        <button type="submit" class="btn">Send Message</button>
      </form>
    </div>
  </section>

  <!-- SCROLL TO TOP -->
  <button id="scrollTopBtn" title="Go to top">↑</button>

  <!-- MODAL -->
  <div id="modal" class="modal">
    <div class="modal-content">
      <span class="close">&times;</span>
      <h3>Project Title</h3>
      <p>Project details go here.</p>
    </div>
  </div>

  <footer><p>© 2025 Suvajit Ghosh. Built with HTML, CSS, JS.</p></footer>

  <script >
    // =======================
// CONTACT FORM HANDLER
// =======================
document.getElementById('contact-form').addEventListener('submit', function (e) {
  e.preventDefault();
  const n = this.querySelector('input[placeholder="Your Name"]').value.trim();
  const eMail = this.querySelector('input[placeholder="Your Email"]').value.trim();
  const msg = this.querySelector('textarea').value.trim();

  if (!n || !eMail || !msg) return alert('Please fill out all fields.');
  if (!/^[^@\s]+@[^@\s]+\.[^@\s]+$/.test(eMail)) return alert('Please enter a valid email address.');

  const messages = JSON.parse(localStorage.getItem("messages") || "[]");
  messages.push({ name: n, email: eMail, message: msg });
  localStorage.setItem("messages", JSON.stringify(messages));

  alert("Thank you! I'll get back to you shortly.");
  this.reset();
});

// =======================
// TYPING ANIMATION
// =======================
const phrases = ["Full Stack Developer", "Web App Specialist", "Chatbot Builder", "WordPress Expert"];
let i = 0, j = 0, curr = [], del = false;

(function loop() {
  const el = document.getElementById("typing-text");
  if (el) el.innerHTML = curr.join('');

  if (i < phrases.length) {
    if (!del && j <= phrases[i].length) curr.push(phrases[i][j++]);
    if (del && j > 0) curr.pop(), j--;

    if (j === phrases[i].length) {
      del = true;
      setTimeout(loop, 1000);
      return;
    }

    if (del && j === 0) {
      del = false;
      i = (i + 1) % phrases.length;
    }
  }

  setTimeout(loop, del ? 50 : 100);
})();

// =======================
// SCROLL TO TOP
// =======================
const scrollBtn = document.getElementById('scrollTopBtn');
window.onscroll = () => {
  scrollBtn.style.display = window.scrollY > 200 ? 'block' : 'none';
};
scrollBtn.onclick = () => {
  window.scrollTo({ top: 0, behavior: 'smooth' });
};

// =======================
// MODAL VIEW MORE
// =======================
document.querySelectorAll('.view-more').forEach(btn =>
  btn.addEventListener('click', e => {
    e.preventDefault();
    document.getElementById('modal').style.display = 'block';
  })
);

document.querySelector('.close').onclick = () =>
  document.getElementById('modal').style.display = 'none';

window.onclick = e => {
  if (e.target == document.getElementById('modal')) {
    document.getElementById('modal').style.display = 'none';
  }
};

// =======================
// THEME TOGGLE
// =======================
const toggle = document.getElementById('theme-toggle');

if (localStorage.getItem('theme') === 'light') {
  document.body.classList.add('light-mode');
  toggle.checked = true;
}

toggle.addEventListener('change', () => {
  document.body.classList.toggle('light-mode');
  localStorage.setItem('theme', document.body.classList.contains('light-mode') ? 'light' : 'dark');
});

// =======================
// NAVBAR TOGGLE
// =======================
const menuToggle = document.getElementById('menu-toggle');
const menu = document.getElementById('menu');

menuToggle.addEventListener('click', () => {
  menu.style.display = (menu.style.display === 'flex') ? 'none' : 'flex';
});

window.addEventListener('resize', () => {
  if (window.innerWidth > 768) {
    menu.style.display = 'flex';
  } else {
    menu.style.display = 'none';
  }
});

  </script>
  <script src="https://unpkg.com/aos@2.3.1/dist/aos.js"></script>
  <script>AOS.init();</script>
</body>
</html>
