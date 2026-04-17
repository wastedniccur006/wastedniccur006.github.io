
html_content = '''<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>TUKO | Kenya's Leading Digital News Platform</title>
    <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@300;400;500;700;900&family=Merriweather:wght@300;400;700;900&display=swap" rel="stylesheet">
    <style>
        :root {
            --tuko-red: #e74c3c;
            --tuko-dark: #1a1a1a;
            --tuko-gray: #2d2d2d;
            --text-dark: #333;
            --text-light: #666;
            --bg-light: #f5f5f5;
            --white: #ffffff;
            --accent: #c5a059;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Roboto', sans-serif;
            background: var(--bg-light);
            color: var(--text-dark);
            line-height: 1.6;
        }

        /* Breaking News Bar */
        .breaking-bar {
            background: var(--tuko-red);
            color: white;
            padding: 8px 0;
            position: fixed;
            top: 0;
            left: 0;
            right: 0;
            z-index: 1000;
            font-size: 14px;
            font-weight: 500;
        }

        .breaking-content {
            max-width: 1400px;
            margin: 0 auto;
            padding: 0 20px;
            display: flex;
            align-items: center;
            gap: 15px;
        }

        .breaking-label {
            background: white;
            color: var(--tuko-red);
            padding: 4px 12px;
            font-weight: 900;
            text-transform: uppercase;
            font-size: 12px;
            letter-spacing: 1px;
            animation: pulse 2s infinite;
            white-space: nowrap;
        }

        @keyframes pulse {
            0%, 100% { opacity: 1; }
            50% { opacity: 0.7; }
        }

        .ticker-wrap {
            flex: 1;
            overflow: hidden;
            white-space: nowrap;
        }

        .ticker-text {
            display: inline-block;
            animation: ticker 20s linear infinite;
        }

        @keyframes ticker {
            0% { transform: translateX(100%); }
            100% { transform: translateX(-100%); }
        }

        /* Header */
        .main-header {
            background: var(--white);
            padding: 15px 0;
            margin-top: 40px;
            border-bottom: 3px solid var(--tuko-red);
            position: sticky;
            top: 40px;
            z-index: 999;
        }

        .header-content {
            max-width: 1400px;
            margin: 0 auto;
            padding: 0 20px;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .logo-text {
            font-size: 42px;
            font-weight: 900;
            color: var(--tuko-red);
            letter-spacing: -2px;
            text-transform: uppercase;
        }

        .logo-tagline {
            font-size: 11px;
            color: var(--text-light);
            text-transform: uppercase;
            letter-spacing: 3px;
            margin-top: -5px;
        }

        .header-actions {
            display: flex;
            gap: 20px;
            align-items: center;
        }

        .social-links {
            display: flex;
            gap: 15px;
        }

        .social-links a {
            color: var(--text-light);
            text-decoration: none;
            font-size: 18px;
            transition: color 0.3s;
        }

        .social-links a:hover {
            color: var(--tuko-red);
        }

        /* Navigation */
        .main-nav {
            background: var(--tuko-dark);
            border-bottom: 1px solid #333;
        }

        .nav-content {
            max-width: 1400px;
            margin: 0 auto;
            padding: 0 20px;
        }

        .nav-menu {
            list-style: none;
            display: flex;
            gap: 0;
            overflow-x: auto;
        }

        .nav-menu li {
            border-right: 1px solid #333;
        }

        .nav-menu a {
            display: block;
            padding: 15px 20px;
            color: white;
            text-decoration: none;
            font-size: 13px;
            font-weight: 500;
            text-transform: uppercase;
            letter-spacing: 0.5px;
            transition: all 0.3s;
            white-space: nowrap;
        }

        .nav-menu a:hover,
        .nav-menu a.active {
            background: var(--tuko-red);
            color: white;
        }

        /* Main Container */
        .container {
            max-width: 1400px;
            margin: 0 auto;
            padding: 30px 20px;
        }

        /* Section Headers */
        .section-header {
            display: flex;
            align-items: center;
            justify-content: space-between;
            margin-bottom: 25px;
            padding-bottom: 10px;
            border-bottom: 3px solid var(--tuko-red);
        }

        .section-title {
            font-size: 20px;
            font-weight: 900;
            text-transform: uppercase;
            color: var(--tuko-dark);
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .section-title::before {
            content: '';
            width: 4px;
            height: 24px;
            background: var(--tuko-red);
        }

        .view-all {
            color: var(--tuko-red);
            text-decoration: none;
            font-size: 13px;
            font-weight: 600;
            text-transform: uppercase;
        }

        /* Featured Story Layout */
        .featured-section {
            display: grid;
            grid-template-columns: 2fr 1fr;
            gap: 25px;
            margin-bottom: 40px;
        }

        .hero-story {
            position: relative;
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 10px 40px rgba(0,0,0,0.15);
        }

        .hero-image {
            width: 100%;
            height: 500px;
            object-fit: cover;
        }

        .hero-overlay {
            position: absolute;
            bottom: 0;
            left: 0;
            right: 0;
            padding: 40px;
            background: linear-gradient(to top, rgba(0,0,0,0.9) 0%, transparent 100%);
            color: white;
        }

        .hero-category {
            display: inline-block;
            background: var(--tuko-red);
            color: white;
            padding: 5px 15px;
            font-size: 11px;
            font-weight: 700;
            text-transform: uppercase;
            letter-spacing: 1px;
            margin-bottom: 15px;
        }

        .hero-title {
            font-family: 'Merriweather', serif;
            font-size: 32px;
            font-weight: 900;
            line-height: 1.2;
            margin-bottom: 15px;
        }

        .hero-excerpt {
            font-size: 15px;
            opacity: 0.9;
            line-height: 1.6;
            margin-bottom: 15px;
        }

        .hero-meta {
            display: flex;
            gap: 20px;
            font-size: 12px;
            opacity: 0.7;
            text-transform: uppercase;
        }

        /* Side Stories */
        .side-stories {
            display: flex;
            flex-direction: column;
            gap: 20px;
        }

        .side-story {
            display: flex;
            gap: 15px;
            background: white;
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 3px 15px rgba(0,0,0,0.08);
            transition: transform 0.3s;
        }

        .side-story:hover {
            transform: translateY(-3px);
        }

        .side-image {
            width: 120px;
            height: 100px;
            object-fit: cover;
            flex-shrink: 0;
        }

        .side-content {
            padding: 15px;
            flex: 1;
        }

        .side-category {
            color: var(--tuko-red);
            font-size: 11px;
            font-weight: 700;
            text-transform: uppercase;
            letter-spacing: 1px;
            margin-bottom: 8px;
        }

        .side-title {
            font-size: 15px;
            font-weight: 700;
            line-height: 1.4;
            color: var(--tuko-dark);
        }

        .side-meta {
            font-size: 11px;
            color: var(--text-light);
            margin-top: 8px;
        }

        /* Stories Grid */
        .stories-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 25px;
            margin-bottom: 40px;
        }

        .story-card {
            background: white;
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 3px 15px rgba(0,0,0,0.08);
            transition: all 0.3s;
        }

        .story-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 30px rgba(0,0,0,0.15);
        }

        .story-image-wrap {
            position: relative;
            height: 200px;
            overflow: hidden;
        }

        .story-image {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.3s;
        }

        .story-card:hover .story-image {
            transform: scale(1.05);
        }

        .story-badge {
            position: absolute;
            top: 15px;
            left: 15px;
            background: var(--tuko-red);
            color: white;
            padding: 5px 12px;
            font-size: 10px;
            font-weight: 700;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .story-content {
            padding: 20px;
        }

        .story-category {
            color: var(--tuko-red);
            font-size: 11px;
            font-weight: 700;
            text-transform: uppercase;
            letter-spacing: 1px;
            margin-bottom: 10px;
        }

        .story-title {
            font-family: 'Merriweather', serif;
            font-size: 18px;
            font-weight: 700;
            line-height: 1.4;
            color: var(--tuko-dark);
            margin-bottom: 10px;
        }

        .story-excerpt {
            font-size: 14px;
            color: var(--text-light);
            line-height: 1.5;
            margin-bottom: 15px;
        }

        .story-meta {
            display: flex;
            justify-content: space-between;
            font-size: 12px;
            color: #999;
        }

        /* Full Story Content */
        .full-story {
            background: white;
            padding: 40px;
            border-radius: 8px;
            margin-bottom: 40px;
            box-shadow: 0 3px 15px rgba(0,0,0,0.08);
        }

        .full-story-header {
            text-align: center;
            margin-bottom: 40px;
            padding-bottom: 30px;
            border-bottom: 1px solid #eee;
        }

        .full-category {
            display: inline-block;
            background: var(--tuko-red);
            color: white;
            padding: 8px 20px;
            font-size: 12px;
            font-weight: 700;
            text-transform: uppercase;
            letter-spacing: 2px;
            margin-bottom: 20px;
        }

        .full-title {
            font-family: 'Merriweather', serif;
            font-size: 42px;
            font-weight: 900;
            line-height: 1.2;
            color: var(--tuko-dark);
            margin-bottom: 20px;
        }

        .full-meta {
            display: flex;
            justify-content: center;
            gap: 30px;
            font-size: 13px;
            color: var(--text-light);
            text-transform: uppercase;
        }

        .full-content {
            font-family: 'Merriweather', serif;
            font-size: 18px;
            line-height: 1.9;
            color: var(--text-dark);
        }

        .full-content p {
            margin-bottom: 25px;
            text-align: justify;
        }

        .full-content p:first-of-type::first-letter {
            float: left;
            font-size: 5rem;
            font-weight: 900;
            margin-right: 15px;
            margin-top: 10px;
            color: var(--tuko-red);
            font-family: 'Merriweather', serif;
        }

        .story-media {
            margin: 30px 0;
            text-align: center;
        }

        .story-media img,
        .story-media video {
            max-width: 100%;
            border-radius: 8px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.2);
        }

        /* Video Section */
        .video-section {
            background: var(--tuko-dark);
            padding: 40px 0;
            margin: 40px 0;
        }

        .video-section .section-title {
            color: white;
        }

        .video-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 25px;
        }

        .video-card {
            background: rgba(255,255,255,0.05);
            border-radius: 8px;
            overflow: hidden;
            border: 1px solid rgba(255,255,255,0.1);
        }

        .video-wrapper {
            position: relative;
            padding-bottom: 56.25%;
            background: #000;
        }

        .video-wrapper video {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        .video-info {
            padding: 20px;
            color: white;
        }

        .video-title {
            font-size: 16px;
            font-weight: 700;
            margin-bottom: 8px;
        }

        .video-desc {
            font-size: 13px;
            opacity: 0.7;
        }

        /* Newsletter */
        .newsletter-section {
            background: linear-gradient(135deg, var(--tuko-red) 0%, #c0392b 100%);
            padding: 60px 20px;
            text-align: center;
            margin: 40px 0;
            position: relative;
            overflow: hidden;
        }

        .newsletter-section::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: repeating-linear-gradient(
                45deg,
                transparent,
                transparent 10px,
                rgba(255,255,255,0.05) 10px,
                rgba(255,255,255,0.05) 20px
            );
            animation: slide 20s linear infinite;
        }

        @keyframes slide {
            0% { transform: translate(0, 0); }
            100% { transform: translate(50px, 50px); }
        }

        .newsletter-content {
            position: relative;
            z-index: 1;
            max-width: 600px;
            margin: 0 auto;
        }

        .newsletter-title {
            font-size: 32px;
            font-weight: 900;
            color: white;
            margin-bottom: 15px;
            text-transform: uppercase;
        }

        .newsletter-text {
            color: rgba(255,255,255,0.9);
            font-size: 16px;
            margin-bottom: 30px;
        }

        .newsletter-form {
            display: flex;
            gap: 0;
            box-shadow: 0 10px 30px rgba(0,0,0,0.3);
        }

        .newsletter-form input {
            flex: 1;
            padding: 15px 20px;
            border: none;
            font-size: 14px;
        }

        .newsletter-form button {
            padding: 15px 30px;
            background: var(--tuko-dark);
            color: white;
            border: none;
            font-weight: 700;
            text-transform: uppercase;
            letter-spacing: 1px;
            cursor: pointer;
            transition: background 0.3s;
        }

        .newsletter-form button:hover {
            background: #000;
        }

        /* Footer */
        footer {
            background: var(--tuko-dark);
            color: white;
            padding: 60px 20px 30px;
        }

        .footer-content {
            max-width: 1400px;
            margin: 0 auto;
        }

        .footer-top {
            display: grid;
            grid-template-columns: 2fr 1fr 1fr 1fr;
            gap: 40px;
            margin-bottom: 40px;
        }

        .footer-brand {
            font-size: 36px;
            font-weight: 900;
            color: var(--tuko-red);
            margin-bottom: 20px;
        }

        .footer-desc {
            color: #999;
            font-size: 14px;
            line-height: 1.6;
        }

        .footer-links h4 {
            font-size: 14px;
            font-weight: 700;
            text-transform: uppercase;
            letter-spacing: 1px;
            margin-bottom: 20px;
            color: white;
        }

        .footer-links ul {
            list-style: none;
        }

        .footer-links li {
            margin-bottom: 10px;
        }

        .footer-links a {
            color: #999;
            text-decoration: none;
            font-size: 13px;
            transition: color 0.3s;
        }

        .footer-links a:hover {
            color: var(--tuko-red);
        }

        .footer-bottom {
            border-top: 1px solid #333;
            padding-top: 30px;
            text-align: center;
            color: #666;
            font-size: 13px;
        }

        /* Responsive */
        @media (max-width: 1024px) {
            .featured-section {
                grid-template-columns: 1fr;
            }
            
            .stories-grid,
            .video-grid {
                grid-template-columns: repeat(2, 1fr);
            }
            
            .footer-top {
                grid-template-columns: repeat(2, 1fr);
            }
        }

        @media (max-width: 768px) {
            .hero-title {
                font-size: 24px;
            }
            
            .stories-grid,
            .video-grid {
                grid-template-columns: 1fr;
            }
            
            .nav-menu {
                font-size: 12px;
            }
            
            .nav-menu a {
                padding: 12px 15px;
            }
            
            .full-title {
                font-size: 28px;
            }
            
            .full-content {
                font-size: 16px;
            }
            
            .footer-top {
                grid-template-columns: 1fr;
                text-align: center;
            }
            
            .newsletter-form {
                flex-direction: column;
            }
        }
    </style>
</head>
<body>

    <!-- Breaking News Bar -->
    <div class="breaking-bar">
        <div class="breaking-content">
            <span class="breaking-label">Breaking</span>
            <div class="ticker-wrap">
                <span class="ticker-text">
                    Nairobi Tech Scene Hits Record Investment Numbers! • Matatu Art Exhibition Opens at National Museum! • Kenyan Startup Raises $5M in Series A! • New Expressway Route Reduces Traffic by 40%! • Safari Rally 2026 Dates Announced!
                </span>
            </div>
        </div>
    </div>

    <!-- Main Header -->
    <header class="main-header">
        <div class="header-content">
            <div class="logo">
                <div>
                    <div class="logo-text">TUKO</div>
                    <div class="logo-tagline">Kenya's Leading Digital News</div>
                </div>
            </div>
            <div class="header-actions">
                <div class="social-links">
                    <a href="#">📘</a>
                    <a href="#">🐦</a>
                    <a href="#">📸</a>
                    <a href="#">▶️</a>
                </div>
            </div>
        </div>
    </header>

    <!-- Navigation -->
    <nav class="main-nav">
        <div class="nav-content">
            <ul class="nav-menu">
                <li><a href="#" class="active">Home</a></li>
                <li><a href="#news">News</a></li>
                <li><a href="#tech">Technology</a></li>
                <li><a href="#culture">Culture</a></li>
                <li><a href="#business">Business</a></li>
                <li><a href="#sports">Sports</a></li>
                <li><a href="#entertainment">Entertainment</a></li>
                <li><a href="#lifestyle">Lifestyle</a></li>
                <li><a href="#videos">Videos</a></li>
            </ul>
        </div>
    </nav>

    <main class="container">

        <!-- Featured Section -->
        <div class="featured-section">
            <!-- Hero Story: Nairobi Tech -->
            <article class="hero-story">
                <img src="./tech_story_1.jpg" alt="Nairobi Tech" class="hero-image">
                <div class="hero-overlay">
                    <span class="hero-category">Technology</span>
                    <h1 class="hero-title">Nairobi's Tech Hustle: From Small Rooms to Global Impact</h1>
                    <p class="hero-excerpt">In the modern heartbeat of Kenya, Nairobi has grown into one of Africa's most influential innovation centers. What once looked like a city focused mainly on trade and administration is now home to fast-growing startups and digital creators.</p>
                    <div class="hero-meta">
                        <span>📅 April 17, 2026</span>
                        <span>⏱️ 8 min read</span>
                        <span>👁️ 15.2K views</span>
                    </div>
                </div>
            </article>

            <!-- Side Stories -->
            <div class="side-stories">
                <article class="side-story">
                    <img src="./matatu_story_1.jpg" alt="Matatu" class="side-image">
                    <div class="side-content">
                        <div class="side-category">Culture</div>
                        <h3 class="side-title">Nairobi Matatu Culture: The Moving Art That Never Sleeps</h3>
                        <div class="side-meta">April 17, 2026 • 6 min read</div>
                    </div>
                </article>

                <article class="side-story">
                    <img src="./tech_story_2.jpg" alt="Tech Hub" class="side-image">
                    <div class="side-content">
                        <div class="side-category">Innovation</div>
                        <h3 class="side-title">The Rise of Nairobi's Innovation Hubs</h3>
                        <div class="side-meta">April 16, 2026 • 5 min read</div>
                    </div>
                </article>

                <article class="side-story">
                    <img src="./matatu_story_2.jpg" alt="Matatu Interior" class="side-image">
                    <div class="side-content">
                        <div class="side-category">Lifestyle</div>
                        <h3 class="side-title">Inside Nairobi's Most Iconic Matatu Routes</h3>
                        <div class="side-meta">April 15, 2026 • 4 min read</div>
                    </div>
                </article>

                <article class="side-story">
                    <img src="./tech_story_3.jpg" alt="Startup" class="side-image">
                    <div class="side-content">
                        <div class="side-category">Business</div>
                        <h3 class="side-title">How Kenyan Startups Are Attracting Global Investors</h3>
                        <div class="side-meta">April 14, 2026 • 7 min read</div>
                    </div>
                </article>
            </div>
        </div>

        <!-- Latest Stories Grid -->
        <div class="section-header">
            <h2 class="section-title">Latest Stories</h2>
            <a href="#" class="view-all">View All →</a>
        </div>

        <div class="stories-grid">
            <article class="story-card">
                <div class="story-image-wrap">
                    <img src="./tech_story_1.jpg" alt="Tech" class="story-image">
                    <span class="story-badge">Featured</span>
                </div>
                <div class="story-content">
                    <div class="story-category">Technology</div>
                    <h3 class="story-title">Mobile Money Revolution: How M-Pesa Changed Africa</h3>
                    <p class="story-excerpt">The story of how a simple mobile payment system transformed an entire continent's financial landscape.</p>
                    <div class="story-meta">
                        <span>April 17, 2026</span>
                        <span>5 min read</span>
                    </div>
                </div>
            </article>

            <article class="story-card">
                <div class="story-image-wrap">
                    <img src="./matatu_story_1.jpg" alt="Matatu" class="story-image">
                    <span class="story-badge">Trending</span>
                </div>
                <div class="story-content">
                    <div class="story-category">Culture</div>
                    <h3 class="story-title">The Art of Matatu Graffiti: Nairobi's Rolling Canvas</h3>
                    <p class="story-excerpt">Meet the artists who transform ordinary buses into moving masterpieces of urban art.</p>
                    <div class="story-meta">
                        <span>April 17, 2026</span>
                        <span>6 min read</span>
                    </div>
                </div>
            </article>

            <article class="story-card">
                <div class="story-image-wrap">
                    <img src="./tech_story_2.jpg" alt="Innovation" class="story-image">
                </div>
                <div class="story-content">
                    <div class="story-category">Innovation</div>
                    <h3 class="story-title">Silicon Savannah: Kenya's Tech Ecosystem Explained</h3>
                    <p class="story-excerpt">From iHub to Google Launchpad, explore the infrastructure powering Kenya's digital revolution.</p>
                    <div class="story-meta">
                        <span>April 16, 2026</span>
                        <span>8 min read</span>
                    </div>
                </div>
            </article>

            <article class="story-card">
                <div class="story-image-wrap">
                    <img src="./matatu_story_2.jpg" alt="Transport" class="story-image">
                </div>
                <div class="story-content">
                    <div class="story-category">Lifestyle</div>
                    <h3 class="story-title">A Day in the Life of a Matatu Conductor</h3>
                    <p class="story-excerpt">The untold stories of the men and women who keep Nairobi moving 24/7.</p>
                    <div class="story-meta">
                        <span>April 16, 2026</span>
                        <span>4 min read</span>
                    </div>
                </div>
            </article>

            <article class="story-card">
                <div class="story-image-wrap">
                    <img src="./tech_story_3.jpg" alt="Startup" class="story-image">
                    <span class="story-badge">Exclusive</span>
                </div>
                <div class="story-content">
                    <div class="story-category">Business</div>
                    <h3 class="story-title">From Garage to Global: Kenyan Startup Success Stories</h3>
                    <p class="story-excerpt">How young entrepreneurs are building million-dollar companies from humble beginnings.</p>
                    <div class="story-meta">
                        <span>April 15, 2026</span>
                        <span>7 min read</span>
                    </div>
                </div>
            </article>

            <article class="story-card">
                <div class="story-image-wrap">
                    <img src="./matatu_story_3.jpg" alt="Art" class="story-image">
                </div>
                <div class="story-content">
                    <div class="story-category">Entertainment</div>
                    <h3 class="story-title">Matatu Music: The Soundtrack of Nairobi Streets</h3>
                    <p class="story-excerpt">From gengetone to benga, the evolution of music in Nairobi's public transport.</p>
                    <div class="story-meta">
                        <span>April 15, 2026</span>
                        <span>5 min read</span>
                    </div>
                </div>
            </article>
        </div>

        <!-- Full Story: Nairobi Tech -->
        <article class="full-story" id="tech">
            <div class="full-story-header">
                <span class="full-category">Technology</span>
                <h1 class="full-title">Nairobi's Tech Hustle: From Small Rooms to Global Impact</h1>
                <div class="full-meta">
                    <span>📅 April 17, 2026</span>
                    <span>✍️ By TUKO Correspondent</span>
                    <span>⏱️ 8 min read</span>
                    <span>👁️ 15.2K views</span>
                </div>
            </div>

            <div class="full-content">
                <p>In the modern heartbeat of Kenya, Nairobi has grown into one of Africa's most influential innovation centers. What once looked like a city focused mainly on trade and administration is now home to fast-growing startups, digital creators, and software engineers shaping solutions for global markets.</p>

                <p>This transformation did not happen overnight. It started in small internet cafés, university dorm rooms, and cramped rented apartments where young people experimented with code, design, and online business ideas. Many had no formal funding, no advanced equipment, and limited mentorship. What they had was curiosity and persistence.</p>

                <div class="story-media">
                    <img src="./tech_story_1.jpg" alt="Nairobi Tech Innovation">
                </div>

                <p>Today, those early experiments have evolved into real companies. Fintech platforms are now handling payments across East Africa. Logistics startups are improving delivery systems for small businesses. Health-tech tools are helping patients in remote areas access medical advice without traveling long distances.</p>

                <p>A major driver of this growth is mobile technology. With widespread smartphone adoption and mobile money systems, developers have been able to build services that reach millions instantly. This has made Kenya one of the most advanced mobile-first economies in the world.</p>

                <div class="story-media">
                    <img src="./tech_story_2.jpg" alt="Mobile Technology">
                </div>

                <p>However, the journey is still far from easy. Many startups struggle with funding gaps, especially at early stages. Others face infrastructure challenges such as inconsistent internet in certain areas or high operational costs. Competition is also intense, with hundreds of new ideas launched every year.</p>

                <div class="story-media">
                    <img src="./tech_story_3.jpg" alt="Startups">
                </div>

                <p>Despite these challenges, the energy remains strong. Incubators and innovation hubs continue to support young talent. Universities are producing more tech graduates than ever before. International investors are increasingly paying attention to Nairobi as a serious tech destination.</p>

                <p>What stands out most is the mindset shift. Young innovators are no longer waiting for jobs—they are building them. They are creating platforms that solve local problems while also competing globally. Nairobi is no longer just participating in the digital economy; it is actively shaping it.</p>

                <div class="story-media">
                    <img src="./tech_story_4.jpg" alt="Future">
                </div>
            </div>
        </article>

        <!-- Full Story: Matatu Culture -->
        <article class="full-story" id="culture">
            <div class="full-story-header">
                <span class="full-category">Culture</span>
                <h1 class="full-title">Nairobi Matatu Culture: The Moving Art That Never Sleeps</h1>
                <div class="full-meta">
                    <span>📅 April 17, 2026</span>
                    <span>✍️ By TUKO Culture Desk</span>
                    <span>⏱️ 6 min read</span>
                    <span>👁️ 12.8K views</span>
                </div>
            </div>

            <div class="full-content">
                <p>In the fast-moving urban life of Kenya, few things define daily experience more vividly than the matatu system. These minibuses are not just a transport network—they are a living cultural phenomenon that blends art, music, economy, and street identity into one moving ecosystem.</p>

                <p>Every matatu begins its identity long before it hits the road. Artists spend hours designing graffiti-style exteriors, often inspired by pop culture, local heroes, music icons, or social themes. Inside, the transformation continues with LED lights, high-powered sound systems, custom seats, and unique branding that makes each vehicle distinct.</p>

                <div class="story-media">
                    <img src="./matatu_story_1.jpg" alt="Matatu Graffiti">
                </div>

                <p>For passengers, stepping into a matatu is an experience of its own. Music fills the air, sometimes so loud it becomes part of the ride itself. Conductors call out destinations in fast, rhythmic chants that feel like performance poetry. Young people often see matatus as more than transport—they are social spaces where conversations, trends, and culture are exchanged.</p>

                <div class="story-media">
                    <img src="./matatu_story_2.jpg" alt="Matatu Interior">
                </div>

                <p>Behind this creativity is a crucial transport system that keeps Nairobi moving. Every day, millions of people rely on matatus to travel to work, school, markets, and hospitals. Without them, the city's mobility would collapse under pressure.</p>

                <div class="story-media">
                    <img src="./matatu_story_3.jpg" alt="Transport">
                </div>

                <p>But the system operates in a complex environment. Traffic congestion in Nairobi is among the most challenging in the region, often causing long delays during peak hours. Route competition between operators can be intense, with each sacco trying to dominate popular routes. Regulations also evolve frequently, affecting pricing, design, and operation standards.</p>

                <div class="story-media">
                    <img src="./matatu_story_4.jpg" alt="Routes">
                </div>

                <p>Despite these issues, matatu culture continues to evolve rather than disappear. New designs appear regularly, each trying to push boundaries in creativity and style. The culture has even influenced fashion, music, and digital content creation, becoming a symbol of urban expression.</p>

                <p>For outsiders, it may look chaotic. For locals, it is structured chaos with rhythm and identity. It represents survival, creativity, and movement all at once. Matatus are not just part of Nairobi—they are Nairobi in motion.</p>
            </div>
        </article>

    </main>

    <!-- Video Section -->
    <section class="video-section" id="videos">
        <div class="container">
            <div class="section-header">
                <h2 class="section-title">Must Watch</h2>
                <a href="#" class="view-all">View All Videos →</a>
            </div>

            <div class="video-grid">
                <div class="video-card">
                    <div class="video-wrapper">
                        <video controls poster="./matatu_story_4.jpg">
                            <source src="./video1.mp4" type="video/mp4">
                        </video>
                    </div>
                    <div class="video-info">
                        <h4 class="video-title">The Art of the Matatu</h4>
                        <p class="video-desc">Experience Nairobi's moving art culture in action</p>
                    </div>
                </div>

                <div class="video-card">
                    <div class="video-wrapper">
                        <video controls poster="./tech_story_1.jpg">
                            <source src="./video2.mp4" type="video/mp4">
                        </video>
                    </div>
                    <div class="video-info">
                        <h4 class="video-title">Tech Innovation in Nairobi</h4>
                        <p class="video-desc">How startups are transforming the city</p>
                    </div>
                </div>

                <div class="video-card">
                    <div class="video-wrapper">
                        <video controls poster="./matatu_story_2.jpg">
                            <source src="./video3.mp4" type="video/mp4">
                        </video>
                    </div>
                    <div class="video-info">
                        <h4 class="video-title">Inside the Matatu Experience</h4>
                        <p class="video-desc">A passenger's journey through Nairobi</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Newsletter -->
    <section class="newsletter-section">
        <div class="newsletter-content">
            <h2 class="newsletter-title">Stay Informed</h2>
            <p class="newsletter-text">Get the latest news, exclusive stories, and breaking updates delivered straight to your inbox.</p>
            <form class="newsletter-form" onsubmit="event.preventDefault(); alert('Thank you for subscribing to TUKO!');">
                <input type="email" placeholder="Enter your email address" required>
                <button type="submit">Subscribe</button>
            </form>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="footer-content">
            <div class="footer-top">
                <div>
                    <div class="footer-brand">TUKO</div>
                    <p class="footer-desc">Kenya's leading digital news platform. Delivering breaking news, in-depth analysis, and exclusive stories from across the country and beyond.</p>
                </div>
                <div class="footer-links">
                    <h4>Quick Links</h4>
                    <ul>
                        <li><a href="#">About Us</a></li>
                        <li><a href="#">Contact</a></li>
                        <li><a href="#">Careers</a></li>
                        <li><a href="#">Advertise</a></li>
                    </ul>
                </div>
                <div class="footer-links">
                    <h4>Sections</h4>
                    <ul>
                        <li><a href="#">News</a></li>
                        <li><a href="#">Politics</a></li>
                        <li><a href="#">Business</a></li>
                        <li><a href="#">Entertainment</a></li>
                    </ul>
                </div>
                <div class="footer-links">
                    <h4>Legal</h4>
                    <ul>
                        <li><a href="#">Privacy Policy</a></li>
                        <li><a href="#">Terms of Use</a></li>
                        <li><a href="#">Cookie Policy</a></li>
                        <li><a href="#">Disclaimer</a></li>
                    </ul>
                </div>
            </div>
            <div class="footer-bottom">
                <p>&copy; 2026 TUKO. All Rights Reserved. | Kenya's Leading Digital News Platform</p>
            </div>
        </div>
    </footer>

    <script>
        // Auto-update date
        document.getElementById('current-date') && (document.getElementById('current-date').textContent = new Date().toLocaleDateString('en-US', { 
            weekday: 'long', 
            year: 'numeric', 
            month: 'long', 
            day: 'numeric' 
        }));
    </script>

</body>
</html>'''

