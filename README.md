![Logo Banner](https://github.com/swarupcoding56/swarupcoding56/assets/150075661/11652be4-5ec0-4f26-a53c-e250af07acd0)
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Swarup Mitra - Full Stack Developer</title>
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #0f0f23, #1a1a2e, #16213e, #0f3460);
            background-size: 400% 400%;
            animation: gradientShift 8s ease infinite;
            color: #ffffff;
            overflow-x: hidden;
            min-height: 100vh;
        }

        @keyframes gradientShift {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }

        .header {
            text-align: center;
            padding: 60px 0;
            position: relative;
        }

        .profile-img {
            width: 200px;
            height: 200px;
            border-radius: 50%;
            margin: 0 auto 30px;
            background: linear-gradient(45deg, #00d4ff, #ff00d4, #ffaa00);
            padding: 5px;
            animation: profileSpin 10s linear infinite;
            display: flex;
            align-items: center;
            justify-content: center;
            position: relative;
            overflow: hidden;
        }

        .profile-img::before {
            content: "SM";
            font-size: 60px;
            font-weight: bold;
            background: linear-gradient(45deg, #00d4ff, #ff00d4);
            -webkit-background-clip: text;
            background-clip: text;
            -webkit-text-fill-color: transparent;
            animation: textGlow 2s ease-in-out infinite alternate;
        }

        @keyframes profileSpin {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }

        @keyframes textGlow {
            0% { filter: drop-shadow(0 0 5px #00d4ff); }
            100% { filter: drop-shadow(0 0 20px #ff00d4); }
        }

        .typing-container {
            height: 120px;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
        }

        .typing-text {
            font-size: 3.5rem;
            font-weight: bold;
            background: linear-gradient(45deg, #00d4ff, #ff00d4, #ffaa00, #00ff88);
            background-size: 400% 400%;
            -webkit-background-clip: text;
            background-clip: text;
            -webkit-text-fill-color: transparent;
            animation: gradientText 3s ease infinite, fadeInUp 1s ease;
            text-shadow: 0 0 30px rgba(0, 212, 255, 0.5);
            margin-bottom: 20px;
        }

        @keyframes gradientText {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }

        .reverse-text {
            font-size: 2rem;
            height: 60px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: #4dd0e1;
            text-shadow: 0 0 10px rgba(77, 208, 225, 0.8);
        }

        .floating-elements {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: -1;
        }

        .floating-element {
            position: absolute;
            opacity: 0.1;
            animation: float 6s ease-in-out infinite;
        }

        @keyframes float {
            0%, 100% { transform: translateY(0px) rotate(0deg); }
            50% { transform: translateY(-20px) rotate(180deg); }
        }

        .section {
            margin: 80px 0;
            padding: 40px;
            background: rgba(255, 255, 255, 0.05);
            border-radius: 20px;
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.1);
            animation: slideInUp 1s ease;
            position: relative;
            overflow: hidden;
        }

        .section::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: linear-gradient(45deg, transparent, rgba(77, 208, 225, 0.1), transparent);
            animation: shimmer 4s linear infinite;
        }

        @keyframes shimmer {
            0% { transform: translateX(-100%); }
            100% { transform: translateX(100%); }
        }

        @keyframes slideInUp {
            from { opacity: 0; transform: translateY(50px); }
            to { opacity: 1; transform: translateY(0); }
        }

        .section-title {
            font-size: 2.5rem;
            margin-bottom: 30px;
            text-align: center;
            background: linear-gradient(45deg, #00d4ff, #ff00d4);
            -webkit-background-clip: text;
            background-clip: text;
            -webkit-text-fill-color: transparent;
            position: relative;
        }

        .tech-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(120px, 1fr));
            gap: 20px;
            margin-top: 30px;
        }

        .tech-card {
            background: linear-gradient(135deg, rgba(77, 208, 225, 0.1), rgba(255, 0, 212, 0.1));
            padding: 20px;
            border-radius: 15px;
            text-align: center;
            border: 1px solid rgba(77, 208, 225, 0.3);
            transition: all 0.4s ease;
            cursor: pointer;
            position: relative;
            overflow: hidden;
        }

        .tech-card:hover {
            transform: translateY(-10px) scale(1.05);
            box-shadow: 0 20px 40px rgba(77, 208, 225, 0.4);
            border-color: #4dd0e1;
        }

        .tech-card::after {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: linear-gradient(45deg, transparent, rgba(255, 255, 255, 0.1), transparent);
            transition: all 0.4s ease;
            transform: rotate(45deg);
            opacity: 0;
        }

        .tech-card:hover::after {
            opacity: 1;
            animation: cardShine 0.6s ease;
        }

        @keyframes cardShine {
            0% { transform: translateX(-100%) rotate(45deg); }
            100% { transform: translateX(100%) rotate(45deg); }
        }

        .tech-icon {
            font-size: 2.5rem;
            margin-bottom: 10px;
            color: #4dd0e1;
            transition: all 0.3s ease;
        }

        .tech-card:hover .tech-icon {
            animation: iconBounce 0.6s ease;
        }

        @keyframes iconBounce {
            0%, 100% { transform: scale(1); }
            50% { transform: scale(1.3); }
        }

        .stats-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
            margin: 40px 0;
        }

        .stat-card {
            background: linear-gradient(135deg, rgba(0, 212, 255, 0.1), rgba(255, 170, 0, 0.1));
            padding: 30px;
            border-radius: 20px;
            text-align: center;
            border: 1px solid rgba(0, 212, 255, 0.3);
            transition: all 0.4s ease;
        }

        .stat-card:hover {
            transform: scale(1.05);
            box-shadow: 0 15px 30px rgba(0, 212, 255, 0.3);
        }

        .stat-number {
            font-size: 3rem;
            font-weight: bold;
            color: #4dd0e1;
            margin-bottom: 10px;
        }

        .contact-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            margin-top: 40px;
        }

        .contact-card {
            background: linear-gradient(135deg, rgba(255, 0, 212, 0.1), rgba(255, 170, 0, 0.1));
            padding: 30px;
            border-radius: 20px;
            text-align: center;
            border: 1px solid rgba(255, 0, 212, 0.3);
            transition: all 0.4s ease;
            cursor: pointer;
        }

        .contact-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 20px 40px rgba(255, 0, 212, 0.3);
        }

        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 30px;
            margin-top: 40px;
        }

        .project-card {
            background: linear-gradient(135deg, rgba(0, 255, 136, 0.1), rgba(77, 208, 225, 0.1));
            padding: 30px;
            border-radius: 20px;
            border: 1px solid rgba(0, 255, 136, 0.3);
            transition: all 0.4s ease;
            position: relative;
            overflow: hidden;
        }

        .project-card:hover {
            transform: scale(1.02);
            box-shadow: 0 25px 50px rgba(0, 255, 136, 0.3);
        }

        .btn {
            display: inline-block;
            padding: 15px 30px;
            background: linear-gradient(45deg, #00d4ff, #ff00d4);
            border: none;
            border-radius: 50px;
            color: white;
            text-decoration: none;
            font-weight: bold;
            transition: all 0.4s ease;
            cursor: pointer;
            position: relative;
            overflow: hidden;
        }

        .btn:hover {
            transform: scale(1.1);
            box-shadow: 0 10px 30px rgba(77, 208, 225, 0.5);
        }

        .pulse {
            animation: pulse 2s infinite;
        }

        @keyframes pulse {
            0% { box-shadow: 0 0 0 0 rgba(77, 208, 225, 0.7); }
            70% { box-shadow: 0 0 0 10px rgba(77, 208, 225, 0); }
            100% { box-shadow: 0 0 0 0 rgba(77, 208, 225, 0); }
        }

        @keyframes fadeInUp {
            from { opacity: 0; transform: translateY(30px); }
            to { opacity: 1; transform: translateY(0); }
        }

        .fade-in {
            animation: fadeInUp 1s ease;
        }

        @media (max-width: 768px) {
            .typing-text { font-size: 2.5rem; }
            .reverse-text { font-size: 1.5rem; }
            .section-title { font-size: 2rem; }
            .github-stats {
                grid-template-columns: 1fr;
            }
            .stat-image-card {
                min-width: unset;
            }
        }
    </style>
</head>
<body>
    <div class="floating-elements"></div>
    
    <div class="container">
        <header class="header">
            <div class="profile-img"></div>
            <div class="typing-container">
                <h1 class="typing-text">Swarup Mitra</h1>
                <div class="reverse-text" id="reverseText"></div>
            </div>
        </header>

        <section class="section">
            <h2 class="section-title"><i class="fas fa-rocket"></i> About Me</h2>
            <div class="stats-container">
                <div class="stat-card">
                    <div class="stat-number">5+</div>
                    <p>Programming Languages</p>
                </div>
                <div class="stat-card">
                    <div class="stat-number">10+</div>
                    <p>Technologies Mastered</p>
                </div>
                <div class="stat-card">
                    <div class="stat-number">15+</div>
                    <p>Projects Completed</p>
                </div>
                <div class="stat-card">
                    <div class="stat-number">100%</div>
                    <p>Passion for Coding</p>
                </div>
            </div>
            <p style="text-align: center; font-size: 1.2rem; margin-top: 30px; line-height: 1.8;">
                Welcome to my digital realm! I'm a passionate Full Stack Developer who transforms ideas into reality through code. 
                With expertise spanning multiple programming languages and frameworks, I create seamless digital experiences 
                that push the boundaries of what's possible on the web.
            </p>
        </section>

        <section class="section">
            <h2 class="section-title"><i class="fas fa-code"></i> Tech Arsenal</h2>
            <div class="tech-grid">
                <div class="tech-card">
                    <div class="tech-icon"><i class="fab fa-js-square"></i></div>
                    <h3>JavaScript</h3>
                    <p>ES6+ Magic</p>
                </div>
                <div class="tech-card">
                    <div class="tech-icon"><i class="fab fa-react"></i></div>
                    <h3>React</h3>
                    <p>Component Mastery</p>
                </div>
                <div class="tech-card">
                    <div class="tech-icon"><i class="fab fa-node-js"></i></div>
                    <h3>Node.js</h3>
                    <p>Backend Power</p>
                </div>
                <div class="tech-card">
                    <div class="tech-icon"><i class="fab fa-python"></i></div>
                    <h3>Python</h3>
                    <p>AI & Automation</p>
                </div>
                <div class="tech-card">
                    <div class="tech-icon"><i class="fab fa-java"></i></div>
                    <h3>Java</h3>
                    <p>Enterprise Solutions</p>
                </div>
                <div class="tech-card">
                    <div class="tech-icon"><i class="fas fa-database"></i></div>
                    <h3>MongoDB</h3>
                    <p>NoSQL Expert</p>
                </div>
                <div class="tech-card">
                    <div class="tech-icon"><i class="fab fa-html5"></i></div>
                    <h3>HTML5</h3>
                    <p>Semantic Web</p>
                </div>
                <div class="tech-card">
                    <div class="tech-icon"><i class="fab fa-css3-alt"></i></div>
                    <h3>CSS3</h3>
                    <p>Modern Styling</p>
                </div>
                <div class="tech-card">
                    <div class="tech-icon"><i class="fas fa-server"></i></div>
                    <h3>Express.js</h3>
                    <p>API Architect</p>
                </div>
                <div class="tech-card">
                    <div class="tech-icon"><i class="fab fa-git-alt"></i></div>
                    <h3>Git</h3>
                    <p>Version Control</p>
                </div>
            </div>
        </section>

        <section class="section">
            <h2 class="section-title"><i class="fas fa-project-diagram"></i> Featured Projects</h2>
            <div class="projects-grid">
                <div class="project-card">
                    <h3><i class="fas fa-shopping-cart"></i> E-Commerce Platform</h3>
                    <p>Full-stack MERN application with advanced features including real-time inventory management, secure payment processing, and responsive design.</p>
                    <div style="margin-top: 15px;">
                        <span style="background: rgba(77, 208, 225, 0.3); padding: 5px 10px; border-radius: 15px; margin: 5px;">React</span>
                        <span style="background: rgba(255, 170, 0, 0.3); padding: 5px 10px; border-radius: 15px; margin: 5px;">Node.js</span>
                        <span style="background: rgba(0, 255, 136, 0.3); padding: 5px 10px; border-radius: 15px; margin: 5px;">MongoDB</span>
                    </div>
                </div>
                <div class="project-card">
                    <h3><i class="fas fa-blog"></i> Dynamic Blog Platform</h3>
                    <p>Modern blogging platform with markdown support, real-time comments, user authentication, and SEO optimization.</p>
                    <div style="margin-top: 15px;">
                        <span style="background: rgba(77, 208, 225, 0.3); padding: 5px 10px; border-radius: 15px; margin: 5px;">Next.js</span>
                        <span style="background: rgba(255, 0, 212, 0.3); padding: 5px 10px; border-radius: 15px; margin: 5px;">Express</span>
                        <span style="background: rgba(255, 170, 0, 0.3); padding: 5px 10px; border-radius: 15px; margin: 5px;">JWT</span>
                    </div>
                </div>
                <div class="project-card">
                    <h3><i class="fas fa-brain"></i> AI Chat Application</h3>
                    <p>Intelligent chatbot with natural language processing, machine learning capabilities, and real-time communication features.</p>
                    <div style="margin-top: 15px;">
                        <span style="background: rgba(77, 208, 225, 0.3); padding: 5px 10px; border-radius: 15px; margin: 5px;">Python</span>
                        <span style="background: rgba(0, 255, 136, 0.3); padding: 5px 10px; border-radius: 15px; margin: 5px;">TensorFlow</span>
                        <span style="background: rgba(255, 0, 212, 0.3); padding: 5px 10px; border-radius: 15px; margin: 5px;">WebSocket</span>
                    </div>
                </div>
            </div>
        </section>

        <section class="section">
            <h2 class="section-title"><i class="fas fa-envelope"></i> Let's Connect</h2>
            <div class="contact-grid">
                <div class="contact-card" onclick="window.open('mailto:swarupmtra3456@gmail.com')">
                    <i class="fas fa-envelope" style="font-size: 3rem; color: #4dd0e1; margin-bottom: 15px;"></i>
                    <h3>Email Me</h3>
                    <p>swarupmtra3456@gmail.com</p>
                </div>
                <div class="contact-card" onclick="window.open('https://instagram.com/swarup3421', '_blank')">
                    <i class="fab fa-instagram" style="font-size: 3rem; color: #ff00d4; margin-bottom: 15px;"></i>
                    <h3>Instagram</h3>
                    <p>@swarup3421</p>
                </div>
                <div class="contact-card" onclick="window.open('https://github.com/swarupcoding56', '_blank')">
                    <i class="fab fa-github" style="font-size: 3rem; color: #ffaa00; margin-bottom: 15px;"></i>
                    <h3>GitHub</h3>
                    <p>@swarupcoding56</p>
                </div>
            </div>
            
            <div style="text-align: center; margin-top: 50px;">
                <a href="mailto:swarupmtra3456@gmail.com" class="btn pulse">
                    <i class="fas fa-rocket"></i> Let's Build Something Amazing!
                </a>
            </div>
        </section>
    </div>

    <script>
        // Reverse text animation
        const reverseTexts = [
            "Full Stack Web Developer",
            "Python Developer", 
            "Java Developer",
            "MERN Stack Expert",
            "Problem Solver",
            "Code Architect",
            "Tech Enthusiast",
            "Digital Creator",
            "Innovation Driver"
        ];
        
        let currentIndex = 0;
        const reverseTextElement = document.getElementById('reverseText');
        
        function typeReverse(text, element, callback) {
            let index = text.length;
            element.textContent = text;
            
            const interval = setInterval(() => {
                if (index > 0) {
                    element.textContent = text.substring(0, index - 1);
                    index--;
                } else {
                    clearInterval(interval);
                    setTimeout(() => {
                        typeForward(reverseTexts[currentIndex], element, callback);
                    }, 500);
                }
            }, 50);
        }
        
        function typeForward(text, element, callback) {
            let index = 0;
            element.textContent = '';
            
            const interval = setInterval(() => {
                if (index < text.length) {
                    element.textContent += text[index];
                    index++;
                } else {
                    clearInterval(interval);
                    setTimeout(callback, 2000);
                }
            }, 100);
        }
        
        function animateText() {
            const nextIndex = (currentIndex + 1) % reverseTexts.length;
            typeReverse(reverseTexts[currentIndex], reverseTextElement, () => {
                currentIndex = nextIndex;
                animateText();
            });
        }
        
        // Start animation
        reverseTextElement.textContent = reverseTexts[0];
        setTimeout(() => animateText(), 2000);
        
        // Floating elements
        function createFloatingElements() {
            const container = document.querySelector('.floating-elements');
            const icons = ['💻', '🚀', '⚡', '🔥', '✨', '💡', '🌟', '🎯'];
            
            for (let i = 0; i < 20; i++) {
                const element = document.createElement('div');
                element.className = 'floating-element';
                element.textContent = icons[Math.floor(Math.random() * icons.length)];
                element.style.left = Math.random() * 100 + '%';
                element.style.top = Math.random() * 100 + '%';
                element.style.fontSize = (Math.random() * 30 + 20) + 'px';
                element.style.animationDelay = Math.random() * 6 + 's';
                element.style.animationDuration = (Math.random() * 4 + 4) + 's';
                container.appendChild(element);
            }
        }
        
        createFloatingElements();
        
        // Intersection Observer for animations
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -50px 0px'
        };
        
        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('fade-in');
                }
            });
        }, observerOptions);
        
        document.querySelectorAll('.section').forEach(section => {
            observer.observe(section);
        });
        
        // Interactive cursor effect
        document.addEventListener('mousemove', (e) => {
            const cursor = document.querySelector('.cursor');
            if (!cursor) {
                const newCursor = document.createElement('div');
                newCursor.className = 'cursor';
                newCursor.style.cssText = `
                    position: fixed;
                    width: 20px;
                    height: 20px;
                    background: radial-gradient(circle, #4dd0e1, transparent);
                    border-radius: 50%;
                    pointer-events: none;
                    z-index: 1000;
                    opacity: 0.6;
                    transition: transform 0.1s ease;
                `;
                document.body.appendChild(newCursor);
            }
            
            const cursorElement = document.querySelector('.cursor');
            cursorElement.style.left = (e.clientX - 10) + 'px';
            cursorElement.style.top = (e.clientY - 10) + 'px';
        });
        
        // Parallax effect
        window.addEventListener('scroll', () => {
            const scrolled = window.pageYOffset;
            const parallax = document.querySelector('.floating-elements');
            if (parallax) {
                parallax.style.transform = `translateY(${scrolled * 0.5}px)`;
            }
        });
        
        // Tech card click effects
        document.querySelectorAll('.tech-card').forEach(card => {
            card.addEventListener('click', () => {
                card.style.animation = 'none';
                setTimeout(() => {
                    card.style.animation = 'pulse 0.6s ease';
                }, 10);
            });
        });
    </script>
</body>
</html>
