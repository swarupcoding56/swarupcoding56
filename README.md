<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Swarup Mitra | Full Stack Developer</title>
  <link href="https://fonts.googleapis.com/css2?family=Fira+Code:wght@400;700&display=swap" rel="stylesheet">
  <style>
    body {
      margin: 0;
      font-family: 'Fira Code', monospace;
      background: linear-gradient(135deg, #0f2027, #203a43, #2c5364);
      color: #fff;
      overflow-x: hidden;
    }
    header {
      text-align: center;
      padding: 80px 20px;
    }
    header h1 {
      font-size: 3rem;
      color: #00f2fe;
      text-shadow: 0px 0px 15px #00f2fe;
    }
    header h2 {
      font-size: 1.5rem;
      color: #4DD0E1;
      margin-top: 10px;
    }
    #typing {
      font-size: 1.3rem;
      margin-top: 20px;
      color: #FFD700;
    }
    .glow {
      text-shadow: 0px 0px 15px #4DD0E1, 0px 0px 25px #00f2fe;
    }
    section {
      padding: 50px 20px;
      max-width: 900px;
      margin: auto;
    }
    .tech-icons img {
      height: 60px;
      margin: 15px;
      transition: transform 0.3s ease;
    }
    .tech-icons img:hover {
      transform: scale(1.2);
    }
    footer {
      text-align: center;
      padding: 30px;
      font-size: 14px;
      color: #aaa;
    }
    canvas {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      z-index: -1;
    }
  </style>
</head>
<body>
  <canvas id="bg"></canvas>

  <header>
    <h1 class="glow">👋 Hi, I'm Swarup Mitra</h1>
    <h2>🔥 Full Stack Developer | Problem Solver</h2>
    <p id="typing"></p>
  </header>

  <section>
    <h2>🚀 About Me</h2>
    <p>I'm a passionate developer mastering the MERN stack and exploring Python, Java, and scalable architectures. I love building impactful, production-ready apps that stun people. 💡</p>
  </section>

  <section>
    <h2>🛠️ Tech Stack</h2>
    <div class="tech-icons">
      <img src="https://skillicons.dev/icons?i=html" alt="HTML">
      <img src="https://skillicons.dev/icons?i=css" alt="CSS">
      <img src="https://skillicons.dev/icons?i=javascript" alt="JavaScript">
      <img src="https://skillicons.dev/icons?i=react" alt="React">
      <img src="https://skillicons.dev/icons?i=nodejs" alt="Node.js">
      <img src="https://skillicons.dev/icons?i=express" alt="Express">
      <img src="https://skillicons.dev/icons?i=mongodb" alt="MongoDB">
      <img src="https://skillicons.dev/icons?i=python" alt="Python">
      <img src="https://skillicons.dev/icons?i=java" alt="Java">
      <img src="https://skillicons.dev/icons?i=git" alt="Git">
      <img src="https://skillicons.dev/icons?i=github" alt="GitHub">
    </div>
  </section>

  <footer>
    Made with ❤️ by Swarup Mitra
  </footer>

  <script>
    // Typing effect
    const text = ["I am a Full Stack Web Developer", "I am a Python Developer", "I am a Java Developer", "I am a Dreamer 🚀"];
    let i = 0, j = 0, current = "", isDeleting = false;
    function type() {
      current = text[i];
      document.getElementById("typing").innerHTML = current.substring(0, j);
      if (!isDeleting && j < current.length) {
        j++;
        setTimeout(type, 100);
      } else if (isDeleting && j > 0) {
        j--;
        setTimeout(type, 60);
      } else {
        isDeleting = !isDeleting;
        if (!isDeleting) i = (i + 1) % text.length;
        setTimeout(type, 1000);
      }
    }
    type();

    // Background particles
    const canvas = document.getElementById("bg");
    const ctx = canvas.getContext("2d");
    canvas.width = window.innerWidth;
    canvas.height = window.innerHeight;
    let particles = [];
    class Particle {
      constructor() {
        this.x = Math.random() * canvas.width;
        this.y = Math.random() * canvas.height;
        this.radius = Math.random() * 2;
        this.dx = (Math.random() - 0.5) * 1;
        this.dy = (Math.random() - 0.5) * 1;
      }
      draw() {
        ctx.beginPath();
        ctx.arc(this.x, this.y, this.radius, 0, Math.PI * 2);
        ctx.fillStyle = "#4DD0E1";
        ctx.fill();
      }
      update() {
        this.x += this.dx;
        this.y += this.dy;
        if (this.x < 0 || this.x > canvas.width) this.dx *= -1;
        if (this.y < 0 || this.y > canvas.height) this.dy *= -1;
        this.draw();
      }
    }
    for (let i = 0; i < 100; i++) particles.push(new Particle());
    function animate() {
      ctx.clearRect(0, 0, canvas.width, canvas.height);
      particles.forEach(p => p.update());
      requestAnimationFrame(animate);
    }
    animate();
    window.addEventListener("resize", () => {
      canvas.width = window.innerWidth;
      canvas.height = window.innerHeight;
    });
  </script>
</body>
</html>
