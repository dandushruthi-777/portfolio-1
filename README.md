<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, viewport-fit=cover">
    <title>Dandu Shruthi | Professional Portfolio</title>
    <!-- Google Fonts + Font Awesome -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:opsz,wght@14..32,300;14..32,400;14..32,500;14..32,600;14..32,700;14..32,800&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Inter', sans-serif;
            background: #f5f7fb;
            color: #1a2634;
            line-height: 1.5;
            scroll-behavior: smooth;
        }

        /* Custom scrollbar - professional */
        ::-webkit-scrollbar {
            width: 8px;
        }
        ::-webkit-scrollbar-track {
            background: #e9ecef;
        }
        ::-webkit-scrollbar-thumb {
            background: #2c7da0;
            border-radius: 10px;
        }

        /* Navigation - clean & sticky */
        .navbar {
            position: fixed;
            top: 0;
            width: 100%;
            background: rgba(255, 255, 255, 0.98);
            box-shadow: 0 2px 20px rgba(0, 0, 0, 0.05);
            z-index: 1000;
            backdrop-filter: blur(4px);
            border-bottom: 1px solid #e2e8f0;
        }
        .nav-container {
            max-width: 1280px;
            margin: 0 auto;
            padding: 1rem 2rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        .logo a {
            font-size: 1.5rem;
            font-weight: 700;
            color: #1e4a6b;
            text-decoration: none;
            letter-spacing: -0.3px;
        }
        .nav-menu {
            display: flex;
            list-style: none;
            gap: 2rem;
        }
        .nav-link {
            text-decoration: none;
            font-weight: 500;
            color: #334155;
            transition: 0.2s;
            font-size: 0.95rem;
        }
        .nav-link:hover {
            color: #2c7da0;
        }
        .hamburger {
            display: none;
            cursor: pointer;
        }
        .bar {
            width: 25px;
            height: 3px;
            background: #2c7da0;
            margin: 4px 0;
            border-radius: 2px;
        }

        /* Hero Section */
        .hero {
            min-height: 100vh;
            display: flex;
            align-items: center;
            background: linear-gradient(135deg, #f0f9ff 0%, #e6f0fa 100%);
            padding-top: 70px;
        }
        .container {
            max-width: 1280px;
            margin: 0 auto;
            padding: 0 2rem;
        }
        .hero-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 3rem;
            align-items: center;
        }
        .hero-content h1 {
            font-size: 3.2rem;
            font-weight: 800;
            color: #0f2b3d;
            margin-bottom: 0.5rem;
            letter-spacing: -0.02em;
        }
        .hero-badge {
            display: inline-block;
            background: #e2f0f7;
            color: #1e6f9f;
            padding: 0.25rem 1rem;
            border-radius: 30px;
            font-size: 0.8rem;
            font-weight: 600;
            margin-bottom: 1rem;
        }
        .typing-text {
            font-size: 1.5rem;
            font-weight: 600;
            color: #2c7da0;
            margin: 0.75rem 0;
        }
        .hero-description {
            font-size: 1rem;
            color: #475569;
            margin: 1rem 0 1.5rem;
            line-height: 1.6;
        }
        .btn {
            padding: 0.75rem 1.8rem;
            border-radius: 40px;
            font-weight: 600;
            text-decoration: none;
            display: inline-block;
            margin-right: 1rem;
            transition: 0.2s;
            font-size: 0.9rem;
        }
        .btn-primary {
            background: #2c7da0;
            color: white;
            border: none;
        }
        .btn-primary:hover {
            background: #1f5e7a;
            transform: translateY(-2px);
        }
        .btn-secondary {
            background: transparent;
            color: #2c7da0;
            border: 1.5px solid #2c7da0;
        }
        .btn-secondary:hover {
            background: #eef6fc;
            transform: translateY(-2px);
        }
        .social-links {
            display: flex;
            gap: 1rem;
            margin-top: 2rem;
        }
        .social-links a {
            background: white;
            width: 40px;
            height: 40px;
            display: inline-flex;
            align-items: center;
            justify-content: center;
            border-radius: 50%;
            color: #2c7da0;
            font-size: 1.1rem;
            transition: 0.2s;
            box-shadow: 0 2px 8px rgba(0,0,0,0.05);
            border: 1px solid #e2e8f0;
        }
        .social-links a:hover {
            background: #2c7da0;
            color: white;
            transform: translateY(-3px);
        }
        .profile-card {
            background: white;
            border-radius: 2rem;
            padding: 1rem;
            box-shadow: 0 20px 35px -10px rgba(0,0,0,0.1);
            text-align: center;
            border: 1px solid #eef2ff;
        }
        .avatar-icon {
            background: linear-gradient(145deg, #d4eaf5, #b8d9ec);
            width: 260px;
            height: 260px;
            margin: 0 auto;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
        }
        .avatar-icon i {
            font-size: 110px;
            color: #2c7da0;
        }

        /* Section styling */
        section {
            padding: 5rem 0;
        }
        .section-title {
            font-size: 2rem;
            font-weight: 700;
            margin-bottom: 2.5rem;
            color: #0f2b3d;
            position: relative;
            display: inline-block;
        }
        .section-title:after {
            content: '';
            position: absolute;
            bottom: -10px;
            left: 0;
            width: 60px;
            height: 3px;
            background: #2c7da0;
            border-radius: 3px;
        }
        .about-card {
            background: white;
            border-radius: 1.5rem;
            padding: 2rem;
            box-shadow: 0 5px 20px rgba(0,0,0,0.03);
            border: 1px solid #eef2f5;
        }
        .stats-grid {
            display: flex;
            gap: 1.5rem;
            flex-wrap: wrap;
            margin-top: 1rem;
        }
        .stat-item {
            background: #f8fafc;
            padding: 0.8rem 1.5rem;
            border-radius: 50px;
            font-weight: 500;
            font-size: 0.9rem;
        }

        /* Skills */
        .skills-wrapper {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
            gap: 2rem;
        }
        .skill-card {
            background: white;
            border-radius: 1.2rem;
            padding: 1.5rem;
            box-shadow: 0 2px 12px rgba(0,0,0,0.04);
            border: 1px solid #eef2f5;
        }
        .skill-card h3 {
            font-size: 1.3rem;
            margin-bottom: 1.2rem;
            color: #1e4a6b;
            border-left: 3px solid #2c7da0;
            padding-left: 0.8rem;
        }
        .skill-item {
            margin-bottom: 1rem;
        }
        .skill-name {
            display: flex;
            justify-content: space-between;
            font-weight: 500;
            font-size: 0.9rem;
        }
        .progress-bar {
            background: #e2e8f0;
            height: 6px;
            border-radius: 10px;
            margin-top: 5px;
        }
        .progress {
            background: #2c7da0;
            width: 0%;
            height: 100%;
            border-radius: 10px;
            transition: width 0.8s ease;
        }

        /* Projects grid */
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(320px, 1fr));
            gap: 2rem;
        }
        .project-card {
            background: white;
            border-radius: 1.2rem;
            overflow: hidden;
            transition: 0.2s;
            box-shadow: 0 5px 15px rgba(0,0,0,0.03);
            border: 1px solid #edf2f7;
        }
        .project-card:hover {
            transform: translateY(-4px);
            box-shadow: 0 12px 25px rgba(0,0,0,0.08);
        }
        .project-header {
            background: #eef2fa;
            padding: 1.5rem;
            text-align: center;
        }
        .project-header i {
            font-size: 2.5rem;
            color: #2c7da0;
        }
        .project-body {
            padding: 1.5rem;
        }
        .project-body h3 {
            font-size: 1.2rem;
            margin-bottom: 0.5rem;
        }
        .tech-stack {
            display: flex;
            flex-wrap: wrap;
            gap: 0.5rem;
            margin-top: 1rem;
        }
        .tech-tag {
            background: #eff6ff;
            padding: 0.2rem 0.8rem;
            border-radius: 30px;
            font-size: 0.7rem;
            font-weight: 500;
            color: #1e6f9f;
        }

        /* Certifications & Internships combined */
        .certs-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
            gap: 1.5rem;
        }
        .cert-item {
            background: white;
            padding: 1.2rem;
            border-radius: 1rem;
            border-left: 4px solid #2c7da0;
            box-shadow: 0 2px 8px rgba(0,0,0,0.02);
        }
        .internship-row {
            background: #f8fafc;
            border-radius: 1rem;
            padding: 1.2rem;
            margin-top: 1rem;
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
            align-items: center;
        }

        /* Contact */
        .contact-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 2rem;
        }
        .contact-info-card {
            background: white;
            padding: 1.8rem;
            border-radius: 1.2rem;
            border: 1px solid #eef2f5;
        }
        .contact-detail {
            display: flex;
            align-items: center;
            gap: 1rem;
            margin-bottom: 1.5rem;
        }
        .contact-detail i {
            width: 42px;
            height: 42px;
            background: #eff6ff;
            display: flex;
            align-items: center;
            justify-content: center;
            border-radius: 50%;
            color: #2c7da0;
        }
        .contact-form input, .contact-form textarea {
            width: 100%;
            padding: 0.8rem;
            margin-bottom: 1rem;
            border: 1px solid #cfdfe9;
            border-radius: 0.8rem;
            font-family: inherit;
            background: white;
        }
        footer {
            background: #0f2b3d;
            color: #cddfe7;
            text-align: center;
            padding: 2rem;
            margin-top: 2rem;
        }
        @media (max-width: 850px) {
            .hero-grid { grid-template-columns: 1fr; text-align: center; }
            .contact-grid { grid-template-columns: 1fr; }
            .hamburger { display: block; }
            .nav-menu {
                position: fixed;
                left: -100%;
                top: 70px;
                flex-direction: column;
                background: white;
                width: 100%;
                text-align: center;
                padding: 2rem;
                gap: 1rem;
                box-shadow: 0 15px 20px rgba(0,0,0,0.05);
                transition: 0.3s;
            }
            .nav-menu.active { left: 0; }
            .section-title:after { left: 50%; transform: translateX(-50%); }
            .section-title { display: block; text-align: center; }
        }
        .highlight {
            font-weight: 600;
            color: #1e6f9f;
        }
        .inline-badge {
            background: #eef2ff;
            padding: 0.2rem 0.8rem;
            border-radius: 20px;
            font-size: 0.8rem;
        }
    </style>
</head>
<body>
<nav class="navbar">
    <div class="nav-container">
        <div class="logo"><a href="#">Dandu Shruthi</a></div>
        <ul class="nav-menu">
            <li><a href="#home" class="nav-link">Home</a></li>
            <li><a href="#about" class="nav-link">About</a></li>
            <li><a href="#skills" class="nav-link">Skills</a></li>
            <li><a href="#projects" class="nav-link">Projects</a></li>
            <li><a href="#certifications" class="nav-link">Certifications</a></li>
            <li><a href="#contact" class="nav-link">Contact</a></li>
        </ul>
        <div class="hamburger">
            <div class="bar"></div><div class="bar"></div><div class="bar"></div>
        </div>
    </div>
</nav>

<!-- Hero Section -->
<section id="home" class="hero">
    <div class="container">
        <div class="hero-grid">
            <div class="hero-content">
                <div class="hero-badge"><i class="fas fa-graduation-cap"></i> B.Tech CSE • 2027</div>
                <h1>Dandu Shruthi</h1>
                <div class="typing-text" id="roleText">Python & SQL Developer</div>
                <p class="hero-description">Aspiring Software Engineer with strong foundation in Python, SQL, Web Development, and Cloud fundamentals. Proven ability to deliver clean interfaces and solve real-world problems. Quick learner, team player, and recipient of Letter of Recommendation from Prodigy InfoTech.</p>
                <div>
                    <a href="#contact" class="btn btn-primary"><i class="fas fa-paper-plane"></i> Contact</a>
                    <a href="#projects" class="btn btn-secondary"><i class="fas fa-code"></i> Projects</a>
                </div>
                <div class="social-links">
                    <a href="#"><i class="fab fa-github"></i></a>
                    <a href="#"><i class="fab fa-linkedin"></i></a>
                    <a href="mailto:dandushruthi.624@gmail.com"><i class="fas fa-envelope"></i></a>
                </div>
            </div>
            <div class="profile-card">
                <div class="avatar-icon">
                    <i class="fas fa-user-astronaut"></i>
                </div>
                <div style="margin-top: 1rem;">
                    <p><i class="fas fa-map-marker-alt"></i> Hyderabad, India</p>
                    <p class="inline-badge" style="display: inline-block; margin-top: 0.5rem;"><i class="fas fa-trophy"></i> LOR - Prodigy InfoTech</p>
                </div>
            </div>
        </div>
    </div>
</section>

<!-- About + Education -->
<section id="about">
    <div class="container">
        <h2 class="section-title">Professional Profile</h2>
        <div class="about-card">
            <p style="margin-bottom: 1rem;">🎓 <strong>B.Tech in Computer Science Engineering</strong> — SR University | CGPA: 7.12</p>
            <div class="stats-grid">
                <span class="stat-item"><i class="fas fa-chart-line"></i> Intermediate: 87%</span>
                <span class="stat-item"><i class="fas fa-star"></i> SSC: 100%</span>
                <span class="stat-item"><i class="fas fa-cloud"></i> AWS Internship</span>
                <span class="stat-item"><i class="fas fa-laptop-code"></i> Web Dev Internship</span>
            </div>
            <p style="margin-top: 1.2rem;">Dedicated CSE student with hands-on experience in building responsive web interfaces, cloud services (AWS), and database management. Recognized with a Letter of Recommendation for outstanding performance during Web Development Internship at Prodigy InfoTech. Passionate about leveraging technology to solve real-world challenges.</p>
        </div>
    </div>
</section>

<!-- Technical Skills -->
<section id="skills" style="background: #f9fbfd;">
    <div class="container">
        <h2 class="section-title">Technical Competencies</h2>
        <div class="skills-wrapper">
            <div class="skill-card">
                <h3><i class="fab fa-python"></i> Programming & Databases</h3>
                <div class="skill-item"><div class="skill-name">Python <span>88%</span></div><div class="progress-bar"><div class="progress" data-width="88"></div></div></div>
                <div class="skill-item"><div class="skill-name">SQL <span>80%</span></div><div class="progress-bar"><div class="progress" data-width="80"></div></div></div>
                <div class="skill-item"><div class="skill-name">C Programming <span>75%</span></div><div class="progress-bar"><div class="progress" data-width="75"></div></div></div>
                <div class="skill-item"><div class="skill-name">Data Structures <span>78%</span></div><div class="progress-bar"><div class="progress" data-width="78"></div></div></div>
            </div>
            <div class="skill-card">
                <h3><i class="fas fa-cloud"></i> Cloud & DevOps</h3>
                <div class="skill-item"><div class="skill-name">AWS (EC2, S3, IAM) <span>72%</span></div><div class="progress-bar"><div class="progress" data-width="72"></div></div></div>
                <div class="skill-item"><div class="skill-name">Cloud Fundamentals <span>75%</span></div><div class="progress-bar"><div class="progress" data-width="75"></div></div></div>
                <div class="skill-item"><div class="skill-name">Git / GitHub <span>80%</span></div><div class="progress-bar"><div class="progress" data-width="80"></div></div></div>
            </div>
            <div class="skill-card">
                <h3><i class="fas fa-code"></i> Web Development</h3>
                <div class="skill-item"><div class="skill-name">HTML5 & CSS3 <span>90%</span></div><div class="progress-bar"><div class="progress" data-width="90"></div></div></div>
                <div class="skill-item"><div class="skill-name">Responsive Design <span>85%</span></div><div class="progress-bar"><div class="progress" data-width="85"></div></div></div>
                <div class="skill-item"><div class="skill-name">JavaScript (Basic) <span>70%</span></div><div class="progress-bar"><div class="progress" data-width="70"></div></div></div>
            </div>
        </div>
        <div style="margin-top: 1.5rem; text-align: center;"><span class="inline-badge"><i class="fas fa-users"></i> Quick Learner</span> <span class="inline-badge"><i class="fas fa-comments"></i> Team Player</span> <span class="inline-badge"><i class="fas fa-chalkboard"></i> Communication</span></div>
    </div>
</section>

<!-- Projects Section (based on resume) -->
<section id="projects">
    <div class="container">
        <h2 class="section-title">Key Projects</h2>
        <div class="projects-grid">
            <div class="project-card">
                <div class="project-header"><i class="fas fa-utensils"></i></div>
                <div class="project-body">
                    <h3>Restaurant Web Interface</h3>
                    <p>Designed a fully responsive restaurant UI with menu catalog and reservation mockup. Focused on semantic HTML5, modern CSS, and cross-browser compatibility.</p>
                    <div class="tech-stack"><span class="tech-tag">HTML5</span><span class="tech-tag">CSS3</span><span class="tech-tag">Responsive</span></div>
                </div>
            </div>
            <div class="project-card">
                <div class="project-header"><i class="fas fa-database"></i></div>
                <div class="project-body">
                    <h3>Student Management System</h3>
                    <p>SQL-based application to manage student records, perform CRUD operations, and generate analytical reports. Strengthened database design & query optimization.</p>
                    <div class="tech-stack"><span class="tech-tag">SQL</span><span class="tech-tag">Python</span><span class="tech-tag">DBMS</span></div>
                </div>
            </div>
            <div class="project-card">
                <div class="project-header"><i class="fab fa-aws"></i></div>
                <div class="project-body">
                    <h3>AWS Static Website Hosting</h3>
                    <p>Deployed a static portfolio on AWS S3 with bucket policies, configured CloudFront for content delivery, and learned IAM roles for secure access.</p>
                    <div class="tech-stack"><span class="tech-tag">AWS S3</span><span class="tech-tag">CloudFront</span><span class="tech-tag">IAM</span></div>
                </div>
            </div>
        </div>
    </div>
</section>

<!-- Certifications & Internships -->
<section id="certifications" style="background: #f9fbfd;">
    <div class="container">
        <h2 class="section-title">Certifications & Internships</h2>
        <div class="certs-grid">
            <div class="cert-item"><i class="fab fa-aws"></i> <strong>AWS Internship & Training</strong><br>Cloud computing, EC2, S3, IAM fundamentals</div>
            <div class="cert-item"><i class="fas fa-laptop-code"></i> <strong>Web Development Internship</strong><br>Built interactive web pages, real-world UI tasks</div>
            <div class="cert-item"><i class="fas fa-network-wired"></i> <strong>Cisco Networking Essentials</strong><br>Networking & security basics</div>
            <div class="cert-item"><i class="fab fa-microsoft"></i> <strong>Microsoft 365 Certified</strong><br>Productivity tools & cloud collaboration</div>
            <div class="cert-item"><i class="fas fa-chalkboard"></i> <strong>TCS iON Career Edge</strong><br>Professional skills & soft skills</div>
        </div>
        <div class="internship-row">
            <span><i class="fas fa-briefcase"></i> <strong>Internships:</strong> AWS Cloud Internship + Web Development Internship (Prodigy InfoTech)</span>
            <span class="tech-tag"><i class="fas fa-medal"></i> Letter of Recommendation - Prodigy InfoTech</span>
        </div>
    </div>
</section>

<!-- Contact Section -->
<section id="contact">
    <div class="container">
        <h2 class="section-title">Get In Touch</h2>
        <div class="contact-grid">
            <div class="contact-info-card">
                <h3 style="margin-bottom: 1rem;">Let's connect</h3>
                <div class="contact-detail"><i class="fas fa-envelope"></i><div><strong>Email</strong><br>dandushruthi.624@gmail.com</div></div>
                <div class="contact-detail"><i class="fas fa-phone-alt"></i><div><strong>Phone</strong><br>+91 6304740323</div></div>
                <div class="contact-detail"><i class="fab fa-linkedin"></i><div><strong>LinkedIn</strong><br>linkedin.com/in/dandu-shruthi</div></div>
                <p style="margin-top: 1rem;">Open for entry-level opportunities, collaborations, and cloud/web development roles.</p>
            </div>
            <form class="contact-info-card contact-form" id="contactForm">
                <input type="text" placeholder="Full name" required>
                <input type="email" placeholder="Email address" required>
                <textarea rows="4" placeholder="Your message / opportunity details" required></textarea>
                <button type="submit" class="btn btn-primary" style="width: 100%; border: none; cursor: pointer;">Send Message</button>
            </form>
        </div>
    </div>
</section>

<footer>
    <p>© 2025 Dandu Shruthi — Built with professionalism & passion. All credentials verified.</p>
    <p style="margin-top: 0.5rem; font-size: 0.85rem;">Python • SQL • Web • AWS • Certified & Internship-ready</p>
</footer>

<script>
    // Mobile menu toggle
    const hamburger = document.querySelector('.hamburger');
    const navMenu = document.querySelector('.nav-menu');
    if(hamburger) {
        hamburger.addEventListener('click', () => {
            hamburger.classList.toggle('active');
            navMenu.classList.toggle('active');
        });
    }
    document.querySelectorAll('.nav-link').forEach(link => {
        link.addEventListener('click', () => {
            hamburger?.classList.remove('active');
            navMenu?.classList.remove('active');
        });
    });

    // Smooth scroll
    document.querySelectorAll('a[href^="#"]').forEach(anchor => {
        anchor.addEventListener('click', function(e) {
            e.preventDefault();
            const target = document.querySelector(this.getAttribute('href'));
            if(target) target.scrollIntoView({ behavior: 'smooth' });
        });
    });

    // Progress bar animation
    const progressBars = document.querySelectorAll('.progress');
    let animated = false;
    function animateProgress() {
        if(animated) return;
        const skillsSection = document.querySelector('#skills');
        if(!skillsSection) return;
        const rect = skillsSection.getBoundingClientRect();
        if(rect.top < window.innerHeight - 100) {
            progressBars.forEach(bar => {
                const width = bar.getAttribute('data-width');
                if(width && bar.style.width !== width+'%') {
                    bar.style.width = width + '%';
                }
            });
            animated = true;
        }
    }
    window.addEventListener('scroll', animateProgress);
    window.addEventListener('load', animateProgress);

    // Typing effect for roles
    const roles = ["Python & SQL Developer", "Cloud Enthusiast (AWS)", "Web UI Designer", "Quick Learner | Team Player"];
    let idx = 0, charIdx = 0, isDeleting = false;
    const roleSpan = document.getElementById('roleText');
    function typeEffect() {
        if(!roleSpan) return;
        const current = roles[idx];
        if(isDeleting) {
            roleSpan.textContent = current.substring(0, charIdx-1);
            charIdx--;
        } else {
            roleSpan.textContent = current.substring(0, charIdx+1);
            charIdx++;
        }
        if(!isDeleting && charIdx === current.length) {
            isDeleting = true;
            setTimeout(typeEffect, 1800);
            return;
        }
        if(isDeleting && charIdx === 0) {
            isDeleting = false;
            idx = (idx+1) % roles.length;
        }
        setTimeout(typeEffect, isDeleting ? 40 : 90);
    }
    typeEffect();

    // Contact form alert
    const form = document.getElementById('contactForm');
    if(form) {
        form.addEventListener('submit', (e) => {
            e.preventDefault();
            alert("Thank you for reaching out! Shruthi will respond within 24 hours.");
            form.reset();
        });
    }
</script>
</body>
</html>
