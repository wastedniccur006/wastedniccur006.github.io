<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>MIC CHEQUE | Professional Storytelling</title>
    <link href="https://fonts.googleapis.com/css2?family=Cinzel+Decorative:wght@400;700;900&family=Playfair+Display:ital,wght@0,400;0,700;0,900;1,400&family=Lora:ital,wght@0,400;0,700;1,400&family=Montserrat:wght@300;400;600;800&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        /* ===========================
           ROOT VARIABLES (DARK THEME)
        =========================== */
        :root {
            --color-bg: #0a0a0a;
            --color-bg-secondary: #1a1a1a;
            --color-text: #e0e0e0;
            --color-text-light: #b0b0b0;
            --color-accent: #ff0000;
            --color-accent-dark: #cc0000;
            --color-border: #333333;
            --font-display: 'Cinzel Decorative', serif;
            --font-heading: 'Playfair Display', serif;
            --font-body: 'Montserrat', sans-serif;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            background-color: var(--color-bg);
            color: var(--color-text);
            font-family: var(--font-body);
            line-height: 1.6;
        }

        /* ===========================
           UTILITY BAR (TOP)
        =========================== */
        .utility-bar {
            background-color: var(--color-bg-secondary);
            border-bottom: 1px solid var(--color-border);
            padding: 0.75rem 1rem;
            font-size: 0.85rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .utility-left {
            display: flex;
            gap: 2rem;
        }

        .utility-right {
            display: flex;
            gap: 1.5rem;
        }

        .utility-bar a {
            color: var(--color-text-light);
            text-decoration: none;
            transition: color 0.3s;
        }

        .utility-bar a:hover {
            color: var(--color-accent);
        }

        /* ===========================
           BREAKING NEWS TICKER
        =========================== */
        .ticker-container {
            background-color: var(--color-accent);
            color: white;
            padding: 0.75rem 1rem;
            display: flex;
            align-items: center;
            gap: 1rem;
            font-weight: 800;
            font-size: 0.9rem;
        }

        .ticker-label {
            background-color: var(--color-accent-dark);
            padding: 0.4rem 0.8rem;
            border-radius: 2px;
            white-space: nowrap;
        }

        #ticker {
            flex: 1;
            animation: fade 0.3s ease-in-out;
        }

        @keyframes fade {
            0% { opacity: 1; }
            50% { opacity: 0; }
            100% { opacity: 1; }
        }

        /* ===========================
           HEADER
        =========================== */
        .main-header {
            background-color: var(--color-bg-secondary);
            border-bottom: 2px solid var(--color-border);
            padding: 1rem 1rem;
            position: sticky;
            top: 0;
            z-index: 100;
        }

        .header-inner {
            max-width: 1280px;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
            gap: 2rem;
        }

        .logo {
            display: flex;
            align-items: center;
            gap: 1.5rem;
            text-decoration: none;
        }

        .logo-mark {
            width: 180px; /* 4x bigger (from ~45px to 180px) */
            height: 180px;
            display: flex;
            align-items: center;
            justify-content: center;
            perspective: 1000px;
            overflow: visible;
        }

        .logo-3d {
            width: 100%;
            height: 100%;
            object-fit: contain;
            animation: spin3d 10s linear infinite;
            transform-style: preserve-3d;
            filter: drop-shadow(0 10px 30px rgba(255, 215, 0, 0.2));
            background: transparent;
        }

        @keyframes spin3d {
            0% { transform: rotateY(0deg); }
            100% { transform: rotateY(360deg); }
        }

        .logo-mark:hover .logo-3d {
            animation-duration: 5s;
        }

        .logo-text {
            display: none; /* Hide text as it's now in the 3D logo */
        }

        .search-bar {
            flex: 1;
            max-width: 400px;
            display: flex;
            gap: 0.5rem;
        }

        .search-bar input {
            flex: 1;
            padding: 0.8rem;
            background-color: var(--color-bg);
            border: 1px solid var(--color-border);
            color: var(--color-text);
            border-radius: 2px;
            font-size: 0.9rem;
        }

        .search-bar button {
            padding: 0.8rem 1.2rem;
            background-color: var(--color-accent);
            color: white;
            border: none;
            cursor: pointer;
            border-radius: 2px;
            font-weight: 800;
            transition: background-color 0.3s;
        }

        .search-bar button:hover {
            background-color: var(--color-accent-dark);
        }

        /* ===========================
           NAVIGATION
        =========================== */
        .main-nav {
            background-color: var(--color-bg-secondary);
            border-bottom: 1px solid var(--color-border);
            padding: 0;
        }

        .nav-inner {
            max-width: 1280px;
            margin: 0 auto;
            display: flex;
        }

        .nav-inner a {
            flex: 1;
            padding: 1rem;
            text-align: center;
            color: var(--color-text);
            text-decoration: none;
            border-right: 1px solid var(--color-border);
            transition: background-color 0.3s, color 0.3s;
            font-weight: 600;
            font-size: 0.9rem;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .nav-inner a:last-child {
            border-right: none;
        }

        .nav-inner a:hover {
            background-color: var(--color-accent);
            color: white;
        }

        /* ===========================
           MAIN LAYOUT
        =========================== */
        .container {
            max-width: 1280px;
            margin: 0 auto;
            padding: 0 1rem;
            display: grid;
            grid-template-columns: 1fr 300px;
            gap: 2rem;
            padding-top: 2rem;
            padding-bottom: 2rem;
        }

        .main-content {
            grid-column: 1;
        }

        .sidebar {
            grid-column: 2;
        }

        /* ===========================
           HERO SECTION
        =========================== */
        .hero-section {
            display: grid;
            grid-template-columns: 2fr 1fr;
            gap: 1rem;
            margin-bottom: 3rem;
        }

        .hero-main {
            position: relative;
            height: 400px;
            background-color: var(--color-bg-secondary);
            border-radius: 4px;
            overflow: hidden;
        }

        .hero-main video {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        .hero-overlay {
            position: absolute;
            bottom: 0;
            left: 0;
            right: 0;
            background: linear-gradient(to top, rgba(0,0,0,0.9), transparent);
            padding: 2rem 1.5rem;
            color: white;
        }

        .hero-overlay .card-category {
            background-color: var(--color-accent);
            padding: 0.4rem 0.8rem;
            border-radius: 2px;
            font-size: 0.75rem;
            font-weight: 800;
            text-transform: uppercase;
            display: inline-block;
            margin-bottom: 0.8rem;
        }

        .hero-title {
            font-family: var(--font-heading);
            font-size: 1.8rem;
            font-weight: 700;
            line-height: 1.3;
        }

        .hero-side {
            display: flex;
            flex-direction: column;
            gap: 1rem;
        }

        .story-card {
            display: flex;
            height: 130px;
            background-color: var(--color-bg-secondary);
            border-radius: 4px;
            overflow: hidden;
            transition: transform 0.3s;
        }

        .story-card:hover {
            transform: translateY(-4px);
        }

        .card-img {
            width: 40%;
            background-color: var(--color-border);
            overflow: hidden;
        }

        .card-img img,
        .card-img video {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        .card-body {
            width: 60%;
            padding: 1rem;
            display: flex;
            flex-direction: column;
            justify-content: space-between;
        }

        .card-category {
            background-color: var(--color-accent);
            color: white;
            padding: 0.3rem 0.6rem;
            border-radius: 2px;
            font-size: 0.65rem;
            font-weight: 800;
            text-transform: uppercase;
            width: fit-content;
        }

        .card-title {
            font-family: var(--font-heading);
            font-size: 0.95rem;
            font-weight: 700;
            line-height: 1.2;
            color: white;
        }

        /* ===========================
           SECTION HEADERS
        =========================== */
        .section-header {
            display: flex;
            align-items: center;
            gap: 1rem;
            margin-bottom: 1.5rem;
            border-bottom: 2px solid var(--color-accent);
            padding-bottom: 0.8rem;
        }

        .section-title {
            font-family: var(--font-heading);
            font-size: 1.8rem;
            font-weight: 700;
            color: white;
            text-transform: uppercase;
            letter-spacing: 2px;
        }

        /* ===========================
           ARTICLE SECTIONS
        =========================== */
        .article-section {
            background-color: var(--color-bg-secondary);
            padding: 2rem;
            border-radius: 4px;
            margin-bottom: 3rem;
        }

        .article-header {
            margin-bottom: 1.5rem;
        }

        .article-category {
            background-color: var(--color-accent);
            color: white;
            padding: 0.5rem 1rem;
            border-radius: 2px;
            font-size: 0.8rem;
            font-weight: 800;
            text-transform: uppercase;
            display: inline-block;
            margin-bottom: 1rem;
        }

        .article-title {
            font-family: var(--font-heading);
            font-size: 2.2rem;
            font-weight: 700;
            line-height: 1.3;
            margin-bottom: 1rem;
            color: white;
        }

        .article-meta {
            display: flex;
            gap: 1.5rem;
            font-size: 0.9rem;
            color: var(--color-text-light);
            margin-bottom: 1.5rem;
        }

        .article-content {
            line-height: 1.8;
            color: var(--color-text);
        }

        .article-content p {
            margin-bottom: 1.2rem;
            text-align: justify;
        }

        .article-content p:first-letter {
            font-size: 2.5rem;
            font-weight: 700;
            float: left;
            line-height: 1;
            padding-right: 0.5rem;
            color: var(--color-accent);
        }

        .article-image {
            margin: 1.5rem 0;
            border-radius: 4px;
            overflow: hidden;
        }

        .article-image img {
            width: 100%;
            height: auto;
            display: block;
        }

        .image-caption {
            font-size: 0.85rem;
            color: var(--color-text-light);
            font-style: italic;
            margin-top: 0.5rem;
            text-align: center;
        }

        /* ===========================
           STORY GRID (More Stories)
        =========================== */
        .story-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 1.5rem;
            margin-bottom: 3rem;
        }

        .grid-card {
            background-color: var(--color-bg-secondary);
            border-radius: 4px;
            overflow: hidden;
            transition: transform 0.3s;
        }

        .grid-card:hover {
            transform: translateY(-6px);
        }

        .grid-card-img {
            width: 100%;
            height: 200px;
            background-color: var(--color-border);
            overflow: hidden;
            position: relative;
        }

        .grid-card-img img,
        .grid-card-img video {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        .grid-card-body {
            padding: 1.2rem;
        }

        .grid-card-body .card-category {
            display: inline-block;
            margin-bottom: 0.8rem;
        }

        .grid-card-body .card-title {
            font-size: 1.1rem;
            margin-bottom: 0.5rem;
        }

        /* ===========================
           VIDEO SECTION
        =========================== */
        .video-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 1.5rem;
            margin-bottom: 3rem;
        }

        .video-card {
            position: relative;
            height: 250px;
            background-color: var(--color-border);
            border-radius: 4px;
            overflow: hidden;
            cursor: pointer;
            transition: transform 0.3s;
        }

        .video-card:hover {
            transform: scale(1.02);
        }

        .video-card video {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        .play-btn {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            width: 60px;
            height: 60px;
            background-color: rgba(255, 0, 0, 0.8);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 1.8rem;
            transition: background-color 0.3s;
            cursor: pointer;
            z-index: 10;
        }

        .play-btn:hover {
            background-color: var(--color-accent) !important;
        }

        /* ===========================
           SIDEBAR
        =========================== */
        .sidebar-widget {
            background-color: var(--color-bg-secondary);
            border-radius: 4px;
            padding: 1.5rem;
            margin-bottom: 1.5rem;
        }

        .widget-title {
            font-family: var(--font-heading);
            font-size: 1.3rem;
            font-weight: 700;
            margin-bottom: 1rem;
            padding-bottom: 0.8rem;
            border-bottom: 2px solid var(--color-accent);
            color: white;
        }

        .trending-item {
            display: flex;
            gap: 0.8rem;
            margin-bottom: 1rem;
            padding-bottom: 1rem;
            border-bottom: 1px solid var(--color-border);
        }

        .trending-item:last-child {
            border-bottom: none;
            margin-bottom: 0;
            padding-bottom: 0;
        }

        .trending-img {
            width: 60px;
            height: 60px;
            background-color: var(--color-border);
            border-radius: 2px;
            overflow: hidden;
            flex-shrink: 0;
        }

        .trending-img img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        .trending-content {
            flex: 1;
        }

        .trending-title {
            font-size: 0.85rem;
            font-weight: 600;
            line-height: 1.3;
            margin-bottom: 0.3rem;
            color: white;
        }

        .trending-views {
            font-size: 0.75rem;
            color: var(--color-text-light);
        }

        .newsletter-form {
            display: flex;
            flex-direction: column;
            gap: 0.8rem;
        }

        .newsletter-form input {
            padding: 0.8rem;
            background-color: var(--color-bg);
            border: 1px solid var(--color-border);
            color: var(--color-text);
            border-radius: 2px;
            font-size: 0.9rem;
        }

        .newsletter-form button {
            padding: 0.8rem;
            background-color: var(--color-accent);
            color: white;
            border: none;
            cursor: pointer;
            border-radius: 2px;
            font-weight: 800;
            transition: background-color 0.3s;
        }

        .newsletter-form button:hover {
            background-color: var(--color-accent-dark);
        }

        .tags-cloud {
            display: flex;
            flex-wrap: wrap;
            gap: 0.5rem;
        }

        .tag {
            background-color: var(--color-border);
            color: var(--color-text);
            padding: 0.4rem 0.8rem;
            border-radius: 2px;
            font-size: 0.8rem;
            cursor: pointer;
            transition: background-color 0.3s;
        }

        .tag:hover {
            background-color: var(--color-accent);
            color: white;
        }

        /* ===========================
           FOOTER
        =========================== */
        .main-footer {
            background-color: var(--color-bg-secondary);
            border-top: 2px solid var(--color-accent);
            padding: 2rem 1rem;
        }

        .footer-inner {
            max-width: 1280px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 2rem;
            margin-bottom: 2rem;
        }

        .footer-col h4 {
            font-family: var(--font-heading);
            font-size: 1.1rem;
            margin-bottom: 1rem;
            color: white;
        }

        .footer-col p {
            font-size: 0.9rem;
            color: var(--color-text-light);
            line-height: 1.6;
        }

        .footer-links {
            list-style: none;
        }

        .footer-links li {
            margin-bottom: 0.6rem;
        }

        .footer-links a {
            color: var(--color-text-light);
            text-decoration: none;
            font-size: 0.9rem;
            transition: color 0.3s;
        }

        .footer-links a:hover {
            color: var(--color-accent);
        }

        .social-icons {
            display: flex;
            gap: 1rem;
        }

        .social-icons a {
            color: white;
            font-size: 1.3rem;
            transition: color 0.3s;
        }

        .social-icons a:hover {
            color: var(--color-accent);
        }

        .footer-bottom {
            max-width: 1280px;
            margin: 0 auto;
            text-align: center;
            padding-top: 2rem;
            border-top: 1px solid var(--color-border);
            font-size: 0.85rem;
            color: var(--color-text-light);
        }

        /* ===========================
           RESPONSIVE DESIGN
        =========================== */
        @media (max-width: 768px) {
            .container {
                grid-template-columns: 1fr;
            }

            .sidebar {
                grid-column: 1;
            }

            .hero-section {
                grid-template-columns: 1fr;
            }

            .story-grid,
            .video-grid {
                grid-template-columns: repeat(2, 1fr);
            }

            .footer-inner {
                grid-template-columns: repeat(2, 1fr);
            }

            .header-inner {
                flex-wrap: wrap;
            }

            .search-bar {
                order: 3;
                flex-basis: 100%;
            }

            .logo-mark {
                width: 120px;
                height: 120px;
            }
        }

        @media (max-width: 480px) {
            .story-grid,
            .video-grid {
                grid-template-columns: 1fr;
            }

            .footer-inner {
                grid-template-columns: 1fr;
            }

            .article-title {
                font-size: 1.6rem;
            }

            .hero-title {
                font-size: 1.3rem;
            }
        }
    </style>
</head>
<body>

<!-- Utility Bar -->
<div class="utility-bar">
    <div class="utility-left">
        <span id="current-date">Saturday, April 18, 2026</span>
    </div>
    <div class="utility-right">
        <a href="#">ABOUT</a>
        <a href="#">CONTACT</a>
        <a href="#">ADVERTISE</a>
    </div>
</div>

<!-- Breaking News Ticker -->
<div class="ticker-container">
    <div class="ticker-label">BREAKING</div>
    <div id="ticker">Arsenal Win the Premier League 2026! Celebration erupts in London!</div>
</div>

<!-- Header -->
<header class="main-header">
    <div class="header-inner">
        <a href="#" class="logo">
            <div class="logo-mark">
                <img src="logo_3d_clean.png" alt="MIC CHEQUE" class="logo-3d">
            </div>
        </a>
        <div class="search-bar">
            <input type="text" placeholder="Search stories...">
            <button>🔍</button>
        </div>
    </div>
</header>

<!-- Navigation -->
<nav class="main-nav">
    <div class="nav-inner">
        <a href="#home">HOME</a>
        <a href="#technology">TECHNOLOGY</a>
        <a href="#culture">CULTURE</a>
        <a href="#sports">SPORTS</a>
        <a href="#lifestyle">LIFESTYLE</a>
        <a href="#video">VIDEO</a>
    </div>
</nav>

<!-- Main Content -->
<div class="container">
    <main class="main-content">
        
        <!-- Hero Section -->
        <div class="hero-section">
            <div class="hero-main" style="position: relative;">
                <video width="100%" height="100%" style="object-fit: cover;" poster="hero_arsenal_poster.jpg" class="video-player">
                    <source src="hero_arsenal.mp4" type="video/mp4">
                    Your browser does not support the video tag.
                </video>
                <div class="play-btn">▶</div>
                <div class="hero-overlay" style="pointer-events: none;">
                    <span class="card-category">Sports</span>
                    <h2 class="hero-title">Arsenal Crowned Premier League Champions 2026: The 22-Year Wait is Over</h2>
                </div>
            </div>
            <div class="hero-side">
                <div class="story-card" style="display: flex; height: 195px; margin-bottom: 10px;">
                    <div style="width: 40%; background: #333;"><img src="hero_summertides.jpg" alt="Festival" style="height: 100%; object-fit: cover;"></div>
                    <div class="card-body" style="width: 60%;">
                        <span class="card-category">Culture</span>
                        <h3 class="card-title">Summertides Festival 2026: Nairobi's Biggest Music Event</h3>
                    </div>
                </div>
                <div class="story-card" style="display: flex; height: 195px;">
                    <div style="width: 40%; background: #333;"><img src="hero_nyashinski.jpg" alt="Nyashinski" style="height: 100%; object-fit: cover;"></div>
                    <div class="card-body" style="width: 60%;">
                        <span class="card-category">Entertainment</span>
                        <h3 class="card-title">Nyashinski Shuts Down Kasarani with Historic Performance</h3>
                    </div>
                </div>
            </div>
        </div>

        <!-- Featured Story: Technology -->
        <div class="article-section" id="technology">
            <div class="article-header">
                <span class="article-category">Featured Story: Technology</span>
            </div>
            <h2 class="article-title">Nairobi's Tech Hustle: From Small Rooms to Global Impact</h2>
            <div class="article-meta">
                <span>📅 April 17, 2026</span>
                <span>⏱️ 8 min read</span>
                <span>✍️ MIC CHEQUE Staff</span>
            </div>
            <div class="article-content">
                <p>In the modern heartbeat of Kenya, Nairobi has grown into one of Africa's most influential innovation centers. What once looked like a city focused mainly on trade and administration is now home to fast-growing startups, digital creators, and software engineers shaping solutions for global markets.</p>

                <p>This transformation did not happen overnight. It started in small internet cafés, university dorm rooms, and cramped rented apartments where young people experimented with code, design, and online business ideas. Many had no formal funding, no advanced equipment, and limited mentorship. What they had was curiosity and persistence.</p>

                <div class="article-image">
                    <img src="tech_story_1.jpg" alt="Nairobi's tech ecosystem">
                    <div class="image-caption">Nairobi's tech ecosystem continues to attract global attention — Photo: MIC CHEQUE</div>
                </div>

                <p>Today, those early experiments have evolved into real companies. Fintech platforms are now handling payments across East Africa. Logistics startups are improving delivery systems for small businesses. Health-tech tools are helping patients in remote areas access medical advice without traveling long distances.</p>

                <p>A major driver of this growth is mobile technology. With widespread smartphone adoption and mobile money systems, developers have been able to build services that reach millions instantly. This has made Kenya one of the most advanced mobile-first economies in the world.</p>

                <div class="article-image">
                    <img src="tech_story_2.jpg" alt="Mobile technology in Kenya">
                    <div class="image-caption">Mobile technology is the backbone of Kenya's digital economy — Photo: MIC CHEQUE</div>
                </div>

                <p>However, the journey is still far from easy. Many startups struggle with funding gaps, especially at early stages. Others face infrastructure challenges such as inconsistent internet in certain areas or high operational costs. Competition is also intense, with hundreds of new ideas launched every year.</p>

                <div class="article-image">
                    <img src="tech_story_3.jpg" alt="Startup culture in Nairobi">
                    <div class="image-caption">Startup culture is thriving despite funding challenges — Photo: MIC CHEQUE</div>
                </div>

                <p>Despite these challenges, the energy remains strong. Incubators and innovation hubs continue to support young talent. Universities are producing more tech graduates than ever before. International investors are increasingly paying attention to Nairobi as a serious tech destination.</p>

                <p>What stands out most is the mindset shift. Young innovators are no longer waiting for jobs—they are building them. They are creating platforms that solve local problems while also competing globally. Nairobi is no longer just participating in the digital economy; it is actively shaping it.</p>

                <div class="article-image">
                    <img src="tech_story_4.jpg" alt="Future of Nairobi tech">
                    <div class="image-caption">The future of Nairobi's tech scene looks brighter than ever — Photo: MIC CHEQUE</div>
                </div>
            </div>
        </div>

        <!-- Deep Dive: Culture -->
        <div class="article-section" id="culture">
            <div class="article-header">
                <span class="article-category">Deep Dive: Culture</span>
            </div>
            <h2 class="article-title">Nairobi Matatu Culture: The Moving Art That Never Sleeps</h2>
            <div class="article-meta">
                <span>📅 April 17, 2026</span>
                <span>⏱️ 6 min read</span>
                <span>✍️ MIC CHEQUE Staff</span>
            </div>
            <div class="article-content">
                <p>In the fast-moving urban life of Kenya, few things define daily experience more vividly than the matatu system. These minibuses are not just a transport network—they are a living cultural phenomenon that blends art, music, economy, and street identity into one moving ecosystem.</p>

                <p>Every matatu begins its identity long before it hits the road. Artists spend hours designing graffiti-style exteriors, often inspired by pop culture, local heroes, music icons, or social themes. Inside, the transformation continues with LED lights, high-powered sound systems, custom seats, and unique branding that makes each vehicle distinct.</p>

                <div class="article-image">
                    <img src="matatu_story_1.jpg" alt="Matatu graffiti art">
                    <div class="image-caption">Matatu graffiti art is a statement of identity and culture — Photo: MIC CHEQUE</div>
                </div>

                <p>For passengers, stepping into a matatu is an experience of its own. Music fills the air, sometimes so loud it becomes part of the ride itself. Conductors call out destinations in fast, rhythmic chants that feel like performance poetry. Young people often see matatus as more than transport—they are social spaces where conversations, trends, and culture are exchanged.</p>

                <div class="article-image">
                    <img src="matatu_story_2.jpg" alt="Inside a matatu">
                    <div class="image-caption">Inside a matatu — a sensory experience unlike any other — Photo: MIC CHEQUE</div>
                </div>

                <p>Behind this creativity is a crucial transport system that keeps Nairobi moving. Every day, millions of people rely on matatus to travel to work, school, markets, and hospitals. Without them, the city's mobility would collapse under pressure.</p>

                <div class="article-image">
                    <img src="matatu_story_3.jpg" alt="Nairobi public transport">
                    <div class="image-caption">Matatus are the lifeblood of Nairobi's public transport network — Photo: MIC CHEQUE</div>
                </div>

                <p>But the system operates in a complex environment. Traffic congestion in Nairobi is among the most challenging in the region, often causing long delays during peak hours. Route competition between operators can be intense, with each sacco trying to dominate popular routes. Regulations also evolve frequently, affecting pricing, design, and operation standards.</p>

                <div class="article-image">
                    <img src="matatu_story_4.jpg" alt="Matatu competition">
                    <div class="image-caption">Competition on popular routes is fierce among matatu saccos — Photo: MIC CHEQUE</div>
                </div>

                <p>Despite these issues, matatu culture continues to evolve rather than disappear. New designs appear regularly, each trying to push boundaries in creativity and style. The culture has even influenced fashion, music, and digital content creation, becoming a symbol of urban expression.</p>

                <p>For outsiders, it may look chaotic. For locals, it is structured chaos with rhythm and identity. It represents survival, creativity, and movement all at once. Matatus are not just buses; they are the soul of Nairobi's streets.</p>
            </div>
        </div>

        <!-- More Stories -->
        <div class="section-header">
            <h2 class="section-title">More Stories</h2>
        </div>
        <div class="story-grid">
            <div class="grid-card">
                <div class="grid-card-img"><img src="more_story_1.jpg" alt="AI Hub"></div>
                <div class="grid-card-body">
                    <span class="card-category">Tech</span>
                    <h3 class="card-title">Kenya Launches New AI Research Hub in Nairobi</h3>
                </div>
            </div>
            <div class="grid-card">
                <div class="grid-card-img"><img src="more_story_2.jpg" alt="Fashion Week"></div>
                <div class="grid-card-body">
                    <span class="card-category">Lifestyle</span>
                    <h3 class="card-title">Nairobi Fashion Week 2026: Top Trends to Watch</h3>
                </div>
            </div>
            <div class="grid-card">
                <div class="grid-card-img"><img src="more_story_3.jpg" alt="Economy"></div>
                <div class="grid-card-body">
                    <span class="card-category">Business</span>
                    <h3 class="card-title">Kenyan Shilling Strengthens Against Major Currencies</h3>
                </div>
            </div>
        </div>

        <!-- New Stories -->
        <div class="section-header">
            <h2 class="section-title">New Stories</h2>
        </div>
        <div class="story-grid">
            <div class="grid-card">
                <div class="grid-card-img"><img src="new_story_1.jpg" alt="Lamu"></div>
                <div class="grid-card-body">
                    <span class="card-category">Travel</span>
                    <h3 class="card-title">Hidden Gems: Exploring the Magic of Lamu Island</h3>
                </div>
            </div>
            <div class="grid-card">
                <div class="grid-card-img"><img src="new_story_2.jpg" alt="Wellness"></div>
                <div class="grid-card-body">
                    <span class="card-category">Wellness</span>
                    <h3 class="card-title">Rift Valley Retreats: The Ultimate Wellness Guide</h3>
                </div>
            </div>
            <div class="grid-card">
                <div class="grid-card-img" style="position: relative;">
                    <video width="100%" height="100%" style="object-fit: cover;" poster="new_story_3.jpg" class="video-player">
                        <source src="new_story_3.mp4" type="video/mp4">
                        Your browser does not support the video tag.
                    </video>
                    <div class="play-btn">▶</div>
                </div>
                <div class="grid-card-body">
                    <span class="card-category">Food</span>
                    <h3 class="card-title">Nairobi's Best Street Food: A Culinary Journey</h3>
                </div>
            </div>
        </div>

        <!-- Must Watch Videos -->
        <div class="section-header">
            <h2 class="section-title">Must Watch</h2>
        </div>
        <div class="video-grid">
            <div class="video-card">
                <video width="100%" height="100%" style="object-fit: cover;" poster="video_summertides_poster.jpg" class="video-player">
                    <source src="video_summertides.mp4" type="video/mp4">
                    Your browser does not support the video tag.
                </video>
                <div class="play-btn">▶</div>
                <div style="position: absolute; bottom: 10px; left: 10px; color: white; font-size: 0.8rem; font-weight: 800; pointer-events: none;">Summertides Festival 2026 Highlights</div>
            </div>
            <div class="video-card">
                <video width="100%" height="100%" style="object-fit: cover;" poster="video_nyashinski_poster.jpg" class="video-player">
                    <source src="video_nyashinski.mp4" type="video/mp4">
                    Your browser does not support the video tag.
                </video>
                <div class="play-btn">▶</div>
                <div style="position: absolute; bottom: 10px; left: 10px; color: white; font-size: 0.8rem; font-weight: 800; pointer-events: none;">Nyashinski Live at Kasarani Stadium</div>
            </div>
            <div class="video-card">
                <video width="100%" height="100%" style="object-fit: cover;" poster="video_arsenal_poster.jpg" class="video-player">
                    <source src="video_arsenal.mp4" type="video/mp4">
                    Your browser does not support the video tag.
                </video>
                <div class="play-btn">▶</div>
                <div style="position: absolute; bottom: 10px; left: 10px; color: white; font-size: 0.8rem; font-weight: 800; pointer-events: none;">Arsenal: The Road to the 2026 Title</div>
            </div>
        </div>
    </main>

    <!-- Sidebar -->
    <aside class="sidebar">
        <!-- Trending Now -->
        <div class="sidebar-widget">
            <h3 class="widget-title">Trending Now</h3>
            <div class="trending-item">
                <div class="trending-img"><img src="trending_arsenal.jpg" alt="Arsenal"></div>
                <div class="trending-content">
                    <div class="trending-title">Arsenal 2026 Victory Parade: Millions Expected in London</div>
                    <div class="trending-views">👁️ 45.2K views</div>
                </div>
            </div>
            <div class="trending-item">
                <div class="trending-img"><img src="trending_nyashinski.jpg" alt="Nyashinski"></div>
                <div class="trending-content">
                    <div class="trending-title">Nyashinski's New Album Breaks Streaming Records in 24 Hours</div>
                    <div class="trending-views">👁️ 38.9K views</div>
                </div>
            </div>
            <div class="trending-item">
                <div class="trending-img"><img src="trending_summertides.jpg" alt="Festival"></div>
                <div class="trending-content">
                    <div class="trending-title">Summertides Festival 2026: Full Artist Lineup Revealed</div>
                    <div class="trending-views">👁️ 32.1K views</div>
                </div>
            </div>
            <div class="trending-item">
                <div class="trending-img"><img src="trending_safaricom.jpg" alt="Safaricom"></div>
                <div class="trending-content">
                    <div class="trending-title">Safaricom Announces 6G Pilot Program in Nairobi</div>
                    <div class="trending-views">👁️ 28.7K views</div>
                </div>
            </div>
            <div class="trending-item">
                <div class="trending-img"><img src="trending_housing.jpg" alt="Housing"></div>
                <div class="trending-content">
                    <div class="trending-title">New Housing Projects Set to Transform Nairobi Skyline</div>
                    <div class="trending-views">👁️ 24.3K views</div>
                </div>
            </div>
        </div>

        <!-- Newsletter -->
        <div class="sidebar-widget">
            <h3 class="widget-title">Newsletter</h3>
            <p style="margin-bottom: 1rem; font-size: 0.9rem;">Get the best stories delivered to your inbox daily.</p>
            <form class="newsletter-form">
                <input type="email" placeholder="Your email" required>
                <button type="submit">SUBSCRIBE</button>
            </form>
        </div>

        <!-- Topics -->
        <div class="sidebar-widget">
            <h3 class="widget-title">Topics</h3>
            <div class="tags-cloud">
                <span class="tag">Technology</span>
                <span class="tag">Culture</span>
                <span class="tag">Sports</span>
                <span class="tag">Lifestyle</span>
                <span class="tag">Business</span>
                <span class="tag">Travel</span>
                <span class="tag">Entertainment</span>
                <span class="tag">Wellness</span>
            </div>
        </div>

        <!-- Latest Stories -->
        <div class="sidebar-widget">
            <h3 class="widget-title">Latest Stories</h3>
            <div style="display: flex; flex-direction: column; gap: 0.8rem;">
                <div style="display: flex; gap: 0.8rem; padding-bottom: 0.8rem; border-bottom: 1px solid var(--color-border);">
                    <img src="latest_safaricom.jpg" alt="Safaricom" style="width: 50px; height: 50px; border-radius: 2px; object-fit: cover;">
                    <div style="flex: 1;">
                        <div style="font-size: 0.85rem; font-weight: 600; line-height: 1.2; color: white;">Safaricom 6G Pilot: What You Need to Know</div>
                    </div>
                </div>
                <div style="display: flex; gap: 0.8rem; padding-bottom: 0.8rem; border-bottom: 1px solid var(--color-border);">
                    <img src="latest_university.jpg" alt="University" style="width: 50px; height: 50px; border-radius: 2px; object-fit: cover;">
                    <div style="flex: 1;">
                        <div style="font-size: 0.85rem; font-weight: 600; line-height: 1.2; color: white;">University Debates: The Future of Education in Kenya</div>
                    </div>
                </div>
                <div style="display: flex; gap: 0.8rem; padding-bottom: 0.8rem; border-bottom: 1px solid var(--color-border);">
                    <img src="latest_expressway.jpg" alt="Expressway" style="width: 50px; height: 50px; border-radius: 2px; object-fit: cover;">
                    <div style="flex: 1;">
                        <div style="font-size: 0.85rem; font-weight: 600; line-height: 1.2; color: white;">Nairobi Expressway Phase 2: Construction Updates</div>
                    </div>
                </div>
                <div style="display: flex; gap: 0.8rem;">
                    <img src="latest_energy.jpg" alt="Energy" style="width: 50px; height: 50px; border-radius: 2px; object-fit: cover;">
                    <div style="flex: 1;">
                        <div style="font-size: 0.85rem; font-weight: 600; line-height: 1.2; color: white;">Kenya's Green Energy Revolution: New Wind Farm Opens</div>
                    </div>
                </div>
            </div>
        </div>
    </aside>
</div>

<!-- Footer -->
<footer class="main-footer">
    <div class="footer-inner">
        <div class="footer-col">
            <h4 style="font-family: var(--font-display); color: white; font-size: 1.2rem;">MIC CHEQUE</h4>
            <p style="font-size: 0.75rem; line-height: 1.8;">Professional storytelling and deep dives into the heart of Kenya's culture, technology, and lifestyle.</p>
        </div>
        <div class="footer-col">
            <h4>Sections</h4>
            <ul class="footer-links">
                <li><a href="#technology">Technology</a></li>
                <li><a href="#culture">Culture</a></li>
                <li><a href="#sports">Sports</a></li>
                <li><a href="#lifestyle">Lifestyle</a></li>
            </ul>
        </div>
        <div class="footer-col">
            <h4>Company</h4>
            <ul class="footer-links">
                <li><a href="#">About Us</a></li>
                <li><a href="#">Contact</a></li>
                <li><a href="#">Privacy Policy</a></li>
                <li><a href="#">Terms of Service</a></li>
            </ul>
        </div>
        <div class="footer-col">
            <h4>Follow Us</h4>
            <div class="social-icons">
                <a href="#" title="Facebook"><i class="fab fa-facebook"></i></a>
                <a href="#" title="Twitter"><i class="fab fa-twitter"></i></a>
                <a href="#" title="Instagram"><i class="fab fa-instagram"></i></a>
                <a href="#" title="YouTube"><i class="fab fa-youtube"></i></a>
            </div>
        </div>
    </div>
    <div class="footer-bottom">
        &copy; 2026 MIC CHEQUE. All rights reserved. Designed with passion for storytelling.
    </div>
</footer>

<script>
    // Set current date
    const options = { weekday: 'long', year: 'numeric', month: 'long', day: 'numeric' };
    document.getElementById('current-date').textContent = new Date().toLocaleDateString('en-US', options);

    // Ticker animation
    const headlines = [
        "Arsenal Win the Premier League 2026! Celebration erupts in London!",
        "Nyashinski's New Album Breaks Streaming Records in 24 Hours",
        "Safaricom Announces 6G Pilot Program in Nairobi",
        "Summertides Festival 2026: Nairobi's Biggest Music Event"
    ];
    let currentIdx = 0;
    const tickerEl = document.getElementById('ticker');

    setInterval(() => {
        tickerEl.style.opacity = 0;
        setTimeout(() => {
            currentIdx = (currentIdx + 1) % headlines.length;
            tickerEl.textContent = headlines[currentIdx];
            tickerEl.style.opacity = 1;
        }, 300);
    }, 5000);

    // Video playback control - only one video plays at a time
    const videoPlayers = document.querySelectorAll('.video-player');
    const playButtons = document.querySelectorAll('.play-btn');

    videoPlayers.forEach((video, index) => {
        video.addEventListener('click', function(e) {
            e.preventDefault();
            handleVideoClick(video);
        });

        if (playButtons[index]) {
            playButtons[index].addEventListener('click', function(e) {
                e.preventDefault();
                e.stopPropagation();
                handleVideoClick(video);
            });
        }

        video.addEventListener('play', function() {
            videoPlayers.forEach(otherVideo => {
                if (otherVideo !== video && !otherVideo.paused) {
                    otherVideo.pause();
                }
            });
            const playBtn = video.parentElement.querySelector('.play-btn');
            if (playBtn) playBtn.style.display = 'none';
        });

        video.addEventListener('pause', function() {
            const playBtn = video.parentElement.querySelector('.play-btn');
            if (playBtn) playBtn.style.display = 'flex';
        });
    });

    function handleVideoClick(video) {
        videoPlayers.forEach(otherVideo => {
            if (otherVideo !== video) {
                otherVideo.pause();
            }
        });
        if (video.paused) {
            video.play();
        } else {
            video.pause();
        }
    }
</script>

</body>
</html>
