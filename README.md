<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=5.0, user-scalable=yes, viewport-fit=cover">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <meta name="description" content="Chaitanya - Full Stack Developer, Creative Mind, and Tech Enthusiast. Explore my portfolio, hobbies, and connect with me.">
    <meta name="theme-color" content="#0a0e27">
    <meta http-equiv="Content-Security-Policy" content="default-src 'self'; script-src 'self' https://cdn.jsdelivr.net; style-src 'self' 'unsafe-inline'; img-src 'self' data: https:; font-src 'self'; connect-src 'self' https:;">
    <meta http-equiv="X-Content-Type-Options" content="nosniff">
    <meta http-equiv="X-Frame-Options" content="SAMEORIGIN">
    <meta http-equiv="Referrer-Policy" content="strict-origin-when-cross-origin">
    <meta name="apple-mobile-web-app-capable" content="yes">
    <meta name="apple-mobile-web-app-status-bar-style" content="black-translucent">
    <title>Chaitanya - Full Stack Developer & Creative Mind</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Courier New', monospace;
            background: #0a0e27;
            color: #00ff88;
            line-height: 1.6;
            overflow-x: hidden;
            -webkit-user-select: none;
            user-select: none;
            -webkit-touch-callout: none;
            -webkit-tap-highlight-color: transparent;
        }

        /* Smooth scroll behavior */
        html {
            scroll-behavior: smooth;
        }

        /* Navigation Bar */
        nav {
            background: rgba(10, 14, 39, 0.98);
            padding: 1.5rem 2rem;
            position: sticky;
            top: 0;
            z-index: 100;
            box-shadow: 0 0 20px rgba(0, 255, 136, 0.3);
            display: flex;
            justify-content: space-between;
            align-items: center;
            animation: slideDown 0.6s ease-out;
            border-bottom: 2px solid #00ff88;
        }

        @keyframes slideDown {
            from {
                transform: translateY(-100%);
                opacity: 0;
            }
            to {
                transform: translateY(0);
                opacity: 1;
            }
        }

        .logo {
            font-size: 1.8rem;
            font-weight: 700;
            color: #00ff88;
            letter-spacing: 2px;
            text-shadow: 0 0 10px #00ff88, 0 0 20px #00ff88;
        }

        nav ul {
            list-style: none;
            display: flex;
            gap: 2rem;
            align-items: center;
        }

        nav a {
            text-decoration: none;
            color: #00ff88;
            font-weight: 500;
            position: relative;
            transition: all 0.3s ease;
        }

        nav a::after {
            content: '';
            position: absolute;
            width: 0;
            height: 3px;
            bottom: -5px;
            left: 0;
            background: #ff006e;
            transition: width 0.3s ease;
            box-shadow: 0 0 10px #ff006e;
        }

        nav a:hover::after {
            width: 100%;
        }

        .nav-btn {
            background: transparent;
            color: #00ff88;
            padding: 0.8rem 1.5rem;
            border-radius: 0;
            cursor: pointer;
            transition: all 0.3s ease;
            border: 2px solid #00ff88;
            font-weight: 600;
            font-family: 'Courier New', monospace;
            min-height: 44px;
            min-width: 44px;
            -webkit-tap-highlight-color: transparent;
        }

        .nav-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 0 15px #00ff88, inset 0 0 10px rgba(0, 255, 136, 0.3);
            background: rgba(0, 255, 136, 0.1);
        }

        /* Security Badge */
        .security-badge {
            position: fixed;
            bottom: 20px;
            right: 20px;
            background: rgba(0, 255, 136, 0.1);
            border: 1px solid #00ff88;
            padding: 0.5rem 1rem;
            border-radius: 20px;
            font-size: 0.75rem;
            color: #00ff88;
            text-shadow: 0 0 5px #00ff88;
            z-index: 40;
            display: flex;
            align-items: center;
            gap: 0.5rem;
            backdrop-filter: blur(10px);
            cursor: help;
            transition: all 0.3s ease;
        }

        .security-badge:hover {
            background: rgba(0, 255, 136, 0.2);
            box-shadow: 0 0 15px rgba(0, 255, 136, 0.4);
        }

        .security-badge::before {
            content: '🔒';
        }
        .hero {
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            padding: 2rem;
            background: linear-gradient(135deg, #0a0e27 0%, #16213e 50%, #0f3460 100%);
            text-align: center;
            color: #00ff88;
            position: relative;
            overflow: hidden;
        }

        .hero::before {
            content: '';
            position: absolute;
            width: 300px;
            height: 300px;
            background: rgba(0, 255, 136, 0.05);
            border-radius: 50%;
            top: -50px;
            left: -50px;
            animation: float 6s ease-in-out infinite;
            box-shadow: 0 0 40px rgba(0, 255, 136, 0.3);
        }

        .hero::after {
            content: '';
            position: absolute;
            width: 200px;
            height: 200px;
            background: rgba(255, 0, 110, 0.05);
            border-radius: 50%;
            bottom: -30px;
            right: -30px;
            animation: float 8s ease-in-out infinite reverse;
            box-shadow: 0 0 40px rgba(255, 0, 110, 0.3);
        }

        @keyframes float {
            0%, 100% {
                transform: translateY(0px);
            }
            50% {
                transform: translateY(30px);
            }
        }

        .hero-content {
            position: relative;
            z-index: 1;
            animation: fadeInUp 0.8s ease-out;
        }

        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .hero h1 {
            font-size: 4rem;
            margin-bottom: 1rem;
            color: #00ff88;
            text-shadow: 0 0 20px #00ff88, 0 0 40px #00ff88;
            animation: slideInDown 0.8s ease-out;
            letter-spacing: 2px;
        }

        @keyframes slideInDown {
            from {
                opacity: 0;
                transform: translateY(-50px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .hero p {
            font-size: 1.5rem;
            margin-bottom: 2rem;
            opacity: 0.9;
            animation: fadeInUp 0.8s ease-out 0.2s backwards;
            color: #00ddff;
        }

        .cta-button {
            display: inline-block;
            background: transparent;
            color: #00ff88;
            padding: 1rem 2.5rem;
            border-radius: 0;
            text-decoration: none;
            font-weight: 700;
            margin: 0 1rem;
            transition: all 0.3s ease;
            cursor: pointer;
            border: 2px solid #00ff88;
            font-size: 1rem;
            animation: fadeInUp 0.8s ease-out 0.4s backwards;
            font-family: 'Courier New', monospace;
            letter-spacing: 1px;
            -webkit-user-select: none;
            user-select: none;
            min-height: 44px;
            min-width: 44px;
            -webkit-tap-highlight-color: transparent;
        }

        .cta-button:hover {
            transform: translateY(-5px);
            box-shadow: 0 0 20px #00ff88, inset 0 0 20px rgba(0, 255, 136, 0.2);
            background: rgba(0, 255, 136, 0.1);
        }

        /* Mouse Scroll Indicator */
        .mouse-scroll {
            position: absolute;
            bottom: 40px;
            left: 50%;
            transform: translateX(-50%);
            z-index: 10;
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 1rem;
            animation: fadeInUp 0.8s ease-out 0.6s backwards;
        }

        .mouse {
            width: 26px;
            height: 40px;
            border: 2px solid #00ff88;
            border-radius: 13px;
            position: relative;
            box-shadow: 0 0 10px #00ff88;
        }

        .mouse::after {
            content: '';
            position: absolute;
            width: 4px;
            height: 8px;
            background: #ff006e;
            border-radius: 2px;
            top: 8px;
            left: 50%;
            transform: translateX(-50%);
            animation: mouseScroll 1.5s infinite;
            box-shadow: 0 0 5px #ff006e;
        }

        @keyframes mouseScroll {
            0% {
                opacity: 1;
                transform: translateX(-50%) translateY(0);
            }
            100% {
                opacity: 0;
                transform: translateX(-50%) translateY(12px);
            }
        }

        .scroll-label {
            font-size: 0.85rem;
            color: #00ff88;
            text-shadow: 0 0 10px #00ff88;
            animation: scrollGlow 2s ease-in-out infinite;
            font-family: 'Courier New', monospace;
            letter-spacing: 1px;
        }

        @keyframes scrollGlow {
            0%, 100% {
                color: #00ff88;
                text-shadow: 0 0 10px #00ff88;
            }
            50% {
                color: #ff006e;
                text-shadow: 0 0 15px #ff006e;
            }
        }
        section {
            padding: 5rem 2rem;
            background: #0f1419;
            margin: 2rem 0;
            border-radius: 0;
            margin-left: 1rem;
            margin-right: 1rem;
            border: 1px solid #00ff88;
            box-shadow: 0 0 20px rgba(0, 255, 136, 0.2);
        }

        .section-title {
            font-size: 2.5rem;
            margin-bottom: 2rem;
            text-align: center;
            color: #00ff88;
            text-shadow: 0 0 20px #00ff88, 0 0 40px #00ff88;
            letter-spacing: 2px;
        }

        /* Bio Section */
        .bio-container {
            display: flex;
            gap: 3rem;
            align-items: center;
            flex-wrap: wrap;
        }

        .bio-image {
            flex: 1;
            min-width: 250px;
            text-align: center;
        }

        .bio-image img {
            width: 250px;
            height: 250px;
            border-radius: 0;
            border: 3px solid #00ff88;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            animation: zoomIn 0.8s ease-out;
            box-shadow: 0 0 20px #00ff88;
        }

        @keyframes zoomIn {
            from {
                opacity: 0;
                transform: scale(0.8);
            }
            to {
                opacity: 1;
                transform: scale(1);
            }
        }

        .bio-image img:hover {
            transform: scale(1.05);
            box-shadow: 0 0 40px #ff006e, 0 0 20px #00ff88;
        }

        .bio-content {
            flex: 1;
            min-width: 250px;
        }

        .bio-content h3 {
            font-size: 1.5rem;
            color: #00ff88;
            margin-bottom: 1rem;
            text-shadow: 0 0 10px #00ff88;
        }

        .bio-content p {
            font-size: 1.1rem;
            color: #00ddff;
            margin-bottom: 1rem;
            line-height: 1.8;
        }

        /* Portfolio Section */
        .portfolio-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }

        .portfolio-card {
            background: #0a0e27;
            padding: 2rem;
            border-radius: 0;
            color: #00ff88;
            transition: all 0.3s ease;
            cursor: pointer;
            position: relative;
            overflow: hidden;
            animation: slideInUp 0.6s ease-out;
            border: 2px solid #00ff88;
        }

        @keyframes slideInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .portfolio-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(135deg, #ff006e 0%, #00ddff 100%);
            transition: left 0.3s ease;
            z-index: 0;
        }

        .portfolio-card:hover::before {
            left: 0;
        }

        .portfolio-card-content {
            position: relative;
            z-index: 1;
        }

        .portfolio-card h3 {
            font-size: 1.5rem;
            margin-bottom: 1rem;
        }

        .portfolio-card p {
            font-size: 0.95rem;
            margin-bottom: 1rem;
            opacity: 0.9;
        }

        .portfolio-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 0 30px #ff006e, 0 0 20px #00ff88;
        }

        /* Gallery Section */
        .gallery {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 2rem;
        }

        .gallery-item {
            position: relative;
            overflow: hidden;
            border-radius: 0;
            height: 250px;
            cursor: pointer;
            border: 2px solid #00ff88;
            box-shadow: 0 0 15px rgba(0, 255, 136, 0.3);
        }

        .gallery-item img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.3s ease;
        }

        .gallery-item:hover img {
            transform: scale(1.1) rotate(2deg);
        }

        .gallery-overlay {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 255, 136, 0.2);
            display: flex;
            align-items: center;
            justify-content: center;
            opacity: 0;
            transition: opacity 0.3s ease;
            border-radius: 0;
            border: 2px solid #00ff88;
        }

        .gallery-item:hover .gallery-overlay {
            opacity: 1;
        }

        .gallery-overlay p {
            color: #00ff88;
            font-size: 1.2rem;
            font-weight: 600;
            text-align: center;
            text-shadow: 0 0 10px #00ff88;
        }

        /* Hobbies Section */
        .hobbies-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
        }

        .hobby-card {
            background: #0a0e27;
            padding: 2rem;
            border-radius: 0;
            text-align: center;
            color: #00ff88;
            transition: all 0.3s ease;
            animation: slideInUp 0.6s ease-out;
            border: 2px solid #ff006e;
        }

        .hobby-card:hover {
            transform: translateY(-8px);
            box-shadow: 0 0 25px #ff006e, 0 0 15px #00ff88;
            border-color: #00ff88;
        }

        .hobby-icon {
            font-size: 3rem;
            margin-bottom: 1rem;
        }

        .hobby-card h3 {
            font-size: 1.5rem;
            margin-bottom: 1rem;
        }

        .hobby-card p {
            font-size: 0.95rem;
            opacity: 0.9;
        }

        /* Contact Section */
        .contact-container {
            max-width: 600px;
            margin: 0 auto;
        }

        .contact-form {
            display: flex;
            flex-direction: column;
            gap: 1.5rem;
        }

        .form-group {
            display: flex;
            flex-direction: column;
        }

        .form-group label {
            margin-bottom: 0.5rem;
            font-weight: 600;
            color: #00ff88;
        }

        .form-group input,
        .form-group textarea {
            padding: 1rem;
            border: 2px solid #00ff88;
            border-radius: 0;
            font-family: 'Courier New', monospace;
            font-size: 1rem;
            transition: all 0.3s ease;
            background: #0a0e27;
            color: #00ff88;
            -webkit-user-select: text;
            user-select: text;
            -webkit-tap-highlight-color: rgba(0, 255, 136, 0.1);
            min-height: 44px;
            -webkit-touch-callout: none;
        }

        .form-group input:focus,
        .form-group textarea:focus {
            outline: none;
            border-color: #ff006e;
            box-shadow: 0 0 20px #ff006e, 0 0 10px #00ff88;
        }

        .form-group textarea {
            resize: vertical;
            min-height: 150px;
        }

        .submit-btn {
            background: transparent;
            color: #00ff88;
            padding: 1rem;
            border: 2px solid #00ff88;
            border-radius: 0;
            font-weight: 700;
            font-size: 1rem;
            cursor: pointer;
            transition: all 0.3s ease;
            font-family: 'Courier New', monospace;
            letter-spacing: 1px;
        }

        .submit-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 0 20px #00ff88, inset 0 0 15px rgba(0, 255, 136, 0.2);
            background: rgba(0, 255, 136, 0.1);
        }

        /* Social Section */
        .social-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }

        .social-card {
            background: #0a0e27;
            padding: 2rem;
            border-radius: 0;
            color: #00ff88;
            transition: all 0.3s ease;
            cursor: pointer;
            position: relative;
            overflow: hidden;
            animation: slideInUp 0.6s ease-out;
            border: 2px solid #00ff88;
        }

        .social-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(135deg, #ff006e 0%, #00ddff 100%);
            transition: left 0.3s ease;
            z-index: 0;
        }

        .social-card:hover::before {
            left: 0;
        }

        .social-card-content {
            position: relative;
            z-index: 1;
        }

        .social-icon {
            font-size: 3rem;
            margin-bottom: 1rem;
        }

        .neon-icon {
            width: 80px;
            height: 80px;
            display: block;
            filter: drop-shadow(0 0 15px #ff006e) drop-shadow(0 0 8px #d946ef);
        }

        .social-icon-link .neon-icon {
            transition: all 0.3s ease;
        }

        .social-icon-link:hover .neon-icon {
            filter: drop-shadow(0 0 30px #ff006e) drop-shadow(0 0 15px #d946ef);
            transform: scale(1.15) rotate(-8deg);
        }

        .social-card:nth-child(2) .neon-icon {
            filter: drop-shadow(0 0 15px #00ddff) drop-shadow(0 0 8px #0099cc);
        }

        .social-card:nth-child(2) .social-icon-link:hover .neon-icon {
            filter: drop-shadow(0 0 30px #00ddff) drop-shadow(0 0 15px #0099cc);
        }

        .social-card h3 {
            font-size: 1.8rem;
            margin-bottom: 1rem;
        }

        .social-card p {
            font-size: 0.95rem;
            margin-bottom: 1.5rem;
            opacity: 0.9;
        }

        .social-button {
            display: inline-block;
            background: transparent;
            color: #00ff88;
            padding: 0.8rem 1.5rem;
            border-radius: 0;
            text-decoration: none;
            font-weight: 700;
            transition: all 0.3s ease;
            border: 2px solid #00ff88;
            font-family: 'Courier New', monospace;
            letter-spacing: 1px;
        }

        .social-button:hover {
            transform: translateY(-3px);
            box-shadow: 0 0 15px #00ff88, inset 0 0 10px rgba(0, 255, 136, 0.3);
            background: rgba(0, 255, 136, 0.1);
        }

        .social-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 0 30px #ff006e, 0 0 20px #00ff88;
        }

        .social-links {
            display: flex;
            gap: 1.5rem;
            justify-content: center;
            margin-top: 2rem;
        }

        .social-link {
            width: 50px;
            height: 50px;
            border-radius: 0;
            background: transparent;
            display: flex;
            align-items: center;
            justify-content: center;
            color: #00ff88;
            text-decoration: none;
            font-size: 1.5rem;
            transition: all 0.3s ease;
            border: 2px solid #00ff88;
        }

        .social-link:hover {
            transform: translateY(-5px);
            box-shadow: 0 0 20px #00ff88, 0 0 15px #ff006e;
            background: rgba(0, 255, 136, 0.1);
        }

        /* Footer */
        footer {
            background: #0a0e27;
            color: #00ff88;
            text-align: center;
            padding: 2rem;
            margin-top: 2rem;
            border-top: 2px solid #00ff88;
            box-shadow: 0 -10px 20px rgba(0, 255, 136, 0.2);
        }

        footer p {
            margin-bottom: 0.5rem;
            text-shadow: 0 0 10px #00ff88;
        }

        /* Mobile Responsive */
        @media (max-width: 768px) {
            nav {
                flex-direction: column;
                gap: 1rem;
            }

            nav ul {
                flex-direction: column;
                gap: 1rem;
                width: 100%;
            }

            .hero h1 {
                font-size: 2.5rem;
            }

            .hero p {
                font-size: 1.1rem;
            }

            section {
                padding: 3rem 1.5rem;
                margin: 1rem 0.5rem;
            }

            .section-title {
                font-size: 2rem;
            }

            .bio-container {
                gap: 1.5rem;
                flex-direction: column;
            }

            .portfolio-grid,
            .hobbies-grid,
            .gallery {
                grid-template-columns: 1fr;
            }

            .cta-button {
                display: block;
                margin: 0.5rem 0;
            }
        }

        @media (max-width: 480px) {
            .hero h1 {
                font-size: 1.8rem;
            }

            .hero p {
                font-size: 0.9rem;
            }

            .section-title {
                font-size: 1.5rem;
            }

            nav ul {
                gap: 0.5rem;
            }

            nav a {
                font-size: 0.9rem;
            }
    </style>
    <!-- EmailJS Library -->
    <script type="text/javascript" src="https://cdn.jsdelivr.net/npm/@emailjs/browser@3/dist/index.min.js"></script>
</head>
<body>
    <!-- Navigation -->
    <nav>
        <div class="logo">Chaitanya</div>
        <ul>
            <li><a href="#home">Home</a></li>
            <li><a href="#bio">Bio</a></li>
            <li><a href="#hobbies">Hobbies</a></li>
            <li><a href="#social">Social</a></li>
            <li><a href="#contact">Contact</a></li>
            <li><button class="nav-btn" onclick="scrollToSection('contact')">Get in Touch</button></li>
        </ul>
    </nav>

    <!-- Hero Section -->
    <section class="hero" id="home">
        <div class="hero-content">
            <h1>Welcome to My Digital Universe</h1>
            <p>Full Stack Developer | Creative Mind | Tech Enthusiast</p>
            <button class="cta-button" onclick="scrollToSection('hobbies')">View My Work</button>
            <button class="cta-button" onclick="scrollToSection('contact')">Connect With Me</button>
        </div>
        <div class="mouse-scroll">
            <div class="mouse"></div>
            <span class="scroll-label">SCROLL</span>
        </div>
    </section>

    <!-- Bio Section -->
    <section id="bio">
        <h2 class="section-title">About Me</h2>
        <div class="bio-container">
            <div class="bio-image">
                <img src="https://via.placeholder.com/250?text=Your+Photo" alt="Profile Photo">
            </div>
            <div class="bio-content">
                <h3>Hi, I'm Chaitanya!</h3>
                <p>I'm a passionate full-stack developer with a keen eye for design and a heart for solving complex problems. With expertise in web development, I create beautiful and functional digital experiences that make a difference.</p>
                <p>My journey in tech started with curiosity and has evolved into a commitment to excellence. I believe in continuous learning, innovation, and creating solutions that matter.</p>
                <p>When I'm not coding, you can find me exploring new technologies, contributing to open-source projects, or enjoying the creative side of development.</p>
            </div>
        </div>
    </section>

    <!-- Hobbies Section -->
    <section id="hobbies">
        <h2 class="section-title">My Hobbies & Interests</h2>
        <div class="hobbies-grid">
            <div class="hobby-card">
                <div class="hobby-icon">🎮</div>
                <h3>Gaming</h3>
                <p>I love exploring immersive gaming worlds and challenging myself with strategic games. Gaming fuels my creativity and problem-solving skills.</p>
            </div>
            <div class="hobby-card">
                <div class="hobby-icon">🔍</div>
                <h3>Curious</h3>
                <p>I have an insatiable curiosity about how things work and why they work that way. Exploring new ideas, technologies, and perspectives drives my passion for continuous learning and discovery.</p>
            </div>
            <div class="hobby-card">
                <div class="hobby-icon">🚀</div>
                <h3>Innovation</h3>
                <p>Always exploring new technologies and frameworks. I love experimenting with cutting-edge tools to build the next generation of applications.</p>
            </div>
            <div class="hobby-card">
                <div class="hobby-icon">🎵</div>
                <h3>Music</h3>
                <p>Music is my creative escape. Whether it's discovering new artists or enjoying pop music, it keeps me inspired and focused.</p>
            </div>
        </div>
    </section>

    <!-- Social Section -->
    <section id="social">
        <h2 class="section-title">Connect With Me</h2>
        <div class="social-grid">
            <div class="social-card">
                <div class="social-card-content">
                    <a href="https://www.instagram.com/no_one_is_random/" target="_blank" class="social-icon-link" title="Visit Instagram">
                        <img src="instagram-neon.svg" alt="Instagram" class="neon-icon">
                    </a>
                    <h3>Instagram</h3>
                    <p>Follow my creative journey and daily updates on Instagram. Let's connect and share our passion for technology and design.</p>
                    <a href="https://www.instagram.com/no_one_is_random/" target="_blank" class="social-button">Visit Profile</a>
                </div>
            </div>
            <div class="social-card">
                <div class="social-card-content">
                    <a href="https://www.linkedin.com/in/sri-krishna-chaitanya-bulusu-941928397/" target="_blank" class="social-icon-link" title="Visit LinkedIn">
                        <img src="linkedin-neon.svg" alt="LinkedIn" class="neon-icon">
                    </a>
                    <h3>LinkedIn</h3>
                    <p>Connect with me on LinkedIn to explore my professional experience, skills, and career achievements. Let's network!</p>
                    <a href="https://www.linkedin.com/in/sri-krishna-chaitanya-bulusu-941928397/" target="_blank" class="social-button">Visit Profile</a>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact">
        <h2 class="section-title">Get In Touch</h2>
        <div class="contact-container">
            <form class="contact-form" onsubmit="handleSubmit(event)">
                <div class="form-group">
                    <label for="name">Name</label>
                    <input type="text" id="name" name="name" required placeholder="Your Name">
                </div>
                <div class="form-group">
                    <label for="email">Email</label>
                    <input type="email" id="email" name="email" required placeholder="Your Email">
                </div>
                <div class="form-group">
                    <label for="subject">Subject</label>
                    <input type="text" id="subject" name="subject" required placeholder="Message Subject">
                </div>
                <div class="form-group">
                    <label for="message">Message</label>
                    <textarea id="message" name="message" required placeholder="Your Message..."></textarea>
                </div>
                <button type="submit" class="submit-btn">Send Message</button>
            </form>

            <div class="social-links">
                <a href="#" class="social-link" title="GitHub">🐙</a>
                <a href="#" class="social-link" title="LinkedIn">💼</a>
                <a href="#" class="social-link" title="Twitter">🐦</a>
                <a href="#" class="social-link" title="Email">✉️</a>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <p>&copy; 2026 Chaitanya. All rights reserved.</p>
        <p>Designed & developed with ❤️ | www.bulusuchaitanyatech.in</p>
    </footer>

    <!-- Security Badge -->
    <div class="security-badge" title="This website uses HTTPS encryption, security headers, and follows web security best practices.">SECURE</div>

    <script>
        // Initialize EmailJS
        emailjs.init('YOUR_EMAIL_PUBLIC_KEY'); // We'll set up a free public key

        // Smooth scroll to section
        function scrollToSection(sectionId) {
            const section = document.getElementById(sectionId);
            if (section) {
                section.scrollIntoView({ behavior: 'smooth' });
            }
        }

        // Form submission handler - sends email via Gmail
        function handleSubmit(event) {
            event.preventDefault();
            const name = document.getElementById('name').value;
            const email = document.getElementById('email').value;
            const subject = document.getElementById('subject').value;
            const message = document.getElementById('message').value;

            // Email parameters
            const templateParams = {
                to_email: 'chaitanyabulusu3@gmail.com',
                from_name: name,
                from_email: email,
                subject: subject,
                message: message
            };

            // Send email using EmailJS
            emailjs.send('service_gmail', 'template_contact', templateParams)
                .then(function(response) {
                    alert(`Thank you, ${name}! Your message has been sent successfully to chaitanyabulusu3@gmail.com. I'll get back to you soon!`);
                    document.querySelector('.contact-form').reset();
                }, function(error) {
                    console.error('Email send error:', error);
                    // Fallback: open Gmail compose with pre-filled data
                    const gmailLink = `https://mail.google.com/mail/?view=cm&fs=1&to=chaitanyabulusu3@gmail.com&su=${encodeURIComponent(subject)}&body=${encodeURIComponent(`Name: ${name}\nEmail: ${email}\n\nMessage:\n${message}`)}`;
                    alert('Opening Gmail to send your message. Please complete and send the email.');
                    window.open(gmailLink, '_blank');
                });
        }

        // Add scroll animation for sections
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -100px 0px'
        };

        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.style.opacity = '1';
                    entry.target.style.transform = 'translateY(0)';
                }
            });
        }, observerOptions);

        // Observe all sections
        document.querySelectorAll('section').forEach(section => {
            section.style.opacity = '0';
            section.style.transform = 'translateY(20px)';
            section.style.transition = 'all 0.6s ease-out';
            observer.observe(section);
        });

        // Add dark mode toggle (optional)
        let isDarkMode = false;
        function toggleDarkMode() {
            isDarkMode = !isDarkMode;
            if (isDarkMode) {
                document.body.style.filter = 'invert(1)';
            } else {
                document.body.style.filter = 'invert(0)';
            }
        }
    </script>
</body>
</html>
