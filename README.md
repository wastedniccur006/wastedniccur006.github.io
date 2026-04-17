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
            --primary-color: #0a0a0a;
            --accent-color: #c5a059;
            --text-color: #e0e0e0;
            --text-muted: #a0a0a0;
            --bg-color: #121212;
            --card-bg: #1e1e1e;
            --tuko-red: #e8001c;
            --tuko-dark: #000000;
            --border-color: #333333;
            --font-heading: 'Playfair Display', serif;
            --font-display: 'Cinzel Decorative', serif;
            --font-body: 'Lora', serif;
            --font-accent: 'Montserrat', sans-serif;
            --sidebar-width: 300px;
        }

        * { margin: 0; padding: 0; box-sizing: border-box; }

        body {
            background-color: var(--bg-color);
            color: var(--text-color);
            font-family: var(--font-body);
            line-height: 1.6;
            -webkit-font-smoothing: antialiased;
            overflow-x: hidden;
        }

        a { text-decoration: none; color: inherit; }
        img { max-width: 100%; display: block; }

        /* ===========================
           TOP UTILITY BAR
        =========================== */
        .top-utility-bar {
            background: var(--tuko-dark);
            color: #888;
            padding: 0.4rem 0;
            font-family: var(--font-accent);
            font-size: 0.72rem;
            border-bottom: 2px solid var(--tuko-red);
        }

        .top-utility-inner {
            max-width: 1280px;
            margin: 0 auto;
            padding: 0 1rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .top-left-links a {
            color: #888;
            text-transform: uppercase;
            margin-right: 1.2rem;
            transition: color 0.2s;
        }

        .top-left-links a:hover { color: white; }

        .top-right-info {
            display: flex;
            align-items: center;
            gap: 1.5rem;
        }

        .social-icons a {
            margin-left: 0.6rem;
            color: #888;
            transition: color 0.2s;
        }

        .social-icons a:hover { color: var(--tuko-red); }

        /* ===========================
           BREAKING NEWS TICKER
        =========================== */
        .breaking-bar {
            background: #1a1a1a;
            border-bottom: 1px solid var(--border-color);
            padding: 0.5rem 0;
        }

        .breaking-inner {
            max-width: 1280px;
            margin: 0 auto;
            padding: 0 1rem;
            display: flex;
            align-items: center;
            gap: 1rem;
        }

        .breaking-label {
            background: var(--tuko-red);
            color: white;
            padding: 0.2rem 0.8rem;
            font-family: var(--font-accent);
            font-size: 0.72rem;
            font-weight: 800;
            text-transform: uppercase;
            animation: pulse 2s infinite;
        }

        @keyframes pulse {
            0%, 100% { opacity: 1; }
            50% { opacity: 0.75; }
        }

        .ticker-text {
            font-family: var(--font-accent);
            font-size: 0.8rem;
            font-weight: 600;
            color: #fff;
            white-space: nowrap;
            transition: opacity 0.3s;
        }

        /* ===========================
           MAIN HEADER
        =========================== */
        .main-header {
            background: #000;
            padding: 1rem 0;
            box-shadow: 0 2px 15px rgba(0,0,0,0.5);
            position: sticky;
            top: 0;
            z-index: 1000;
        }

        .header-inner {
            max-width: 1280px;
            margin: 0 auto;
            padding: 0 1rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo-wrap {
            display: flex;
            align-items: center;
            gap: 1rem;
        }

        .logo-placeholder {
            width: 50px;
            height: 50px;
            background: var(--tuko-red);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-family: var(--font-display);
            font-weight: 900;
            color: white;
            font-size: 1.5rem;
        }

        .site-name h1 {
            font-family: var(--font-display);
            font-size: 2rem;
            color: #fff;
            letter-spacing: 2px;
            line-height: 1;
        }

        .site-name span {
            font-family: var(--font-accent);
            font-size: 0.65rem;
            color: var(--tuko-red);
            text-transform: uppercase;
            letter-spacing: 3px;
            font-weight: 800;
        }

        .header-search {
            display: flex;
            background: #222;
            border-radius: 4px;
            overflow: hidden;
        }

        .header-search input {
            background: transparent;
            border: none;
            color: white;
            padding: 0.5rem 1rem;
            font-size: 0.8rem;
            outline: none;
        }

        .header-search button {
            background: var(--tuko-red);
            border: none;
            color: white;
            padding: 0.5rem 1rem;
            cursor: pointer;
        }

        /* ===========================
           NAVIGATION
        =========================== */
        .main-nav {
            background: #111;
            border-bottom: 1px solid #222;
        }

        .nav-inner {
            max-width: 1280px;
            margin: 0 auto;
            padding: 0 1rem;
        }

        .nav-menu {
            list-style: none;
            display: flex;
            overflow-x: auto;
        }

        .nav-menu li { border-right: 1px solid #222; }

        .nav-menu a {
            display: block;
            padding: 0.9rem 1.2rem;
            color: #bbb;
            font-family: var(--font-accent);
            font-size: 0.75rem;
            font-weight: 600;
            text-transform: uppercase;
            transition: all 0.2s;
            white-space: nowrap;
        }

        .nav-menu a:hover,
        .nav-menu a.active {
            background: var(--tuko-red);
            color: white;
        }

        /* ===========================
           PAGE LAYOUT
        =========================== */
        .page-wrapper {
            max-width: 1280px;
            margin: 0 auto;
            padding: 1.5rem 1rem;
        }

        .content-layout {
            display: grid;
            grid-template-columns: 1fr var(--sidebar-width);
            gap: 1.5rem;
        }

        /* ===========================
           SECTION HEADERS
        =========================== */
        .section-header {
            display: flex;
            align-items: center;
            justify-content: space-between;
            margin-bottom: 1.2rem;
            padding-bottom: 0.5rem;
            border-bottom: 3px solid var(--tuko-red);
        }

        .section-title {
            font-family: var(--font-accent);
            font-size: 1rem;
            font-weight: 800;
            text-transform: uppercase;
            color: #fff;
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }

        .section-title::before {
            content: '';
            width: 5px;
            height: 20px;
            background: var(--tuko-red);
        }

        /* ===========================
           STORY CARDS & GRIDS
        =========================== */
        .hero-section {
            display: grid;
            grid-template-columns: 1.5fr 1fr;
            gap: 1rem;
            margin-bottom: 2rem;
        }

        .hero-main {
            position: relative;
            border-radius: 6px;
            overflow: hidden;
            height: 400px;
        }

        .hero-main img { width: 100%; height: 100%; object-fit: cover; }

        .hero-overlay {
            position: absolute;
            bottom: 0; left: 0; right: 0;
            padding: 2rem;
            background: linear-gradient(transparent, rgba(0,0,0,0.9));
        }

        .hero-title { font-size: 1.8rem; color: white; font-family: var(--font-heading); line-height: 1.2; }

        .story-card {
            background: var(--card-bg);
            border-radius: 6px;
            overflow: hidden;
            margin-bottom: 1rem;
            transition: transform 0.3s;
        }

        .story-card:hover { transform: translateY(-5px); }

        .card-img { height: 180px; background: #333; position: relative; }
        .card-img img { width: 100%; height: 100%; object-fit: cover; }

        .card-body { padding: 1rem; }
        .card-category { color: var(--tuko-red); font-size: 0.65rem; font-weight: 800; text-transform: uppercase; margin-bottom: 0.5rem; }
        .card-title { font-size: 1rem; color: white; font-family: var(--font-heading); margin-bottom: 0.5rem; }
        .card-excerpt { font-size: 0.85rem; color: var(--text-muted); }

        .stories-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 1rem;
            margin-bottom: 2rem;
        }

        /* ===========================
           FULL STORY STYLING
        =========================== */
        .full-story-wrap {
            background: var(--card-bg);
            padding: 2rem;
            border-radius: 8px;
            margin-bottom: 3rem;
        }

        .full-story-header { margin-bottom: 2rem; border-bottom: 1px solid var(--border-color); padding-bottom: 1rem; }
        .full-story-title { font-family: var(--font-heading); font-size: 2.5rem; color: white; line-height: 1.1; margin-bottom: 1rem; }
        .full-story-meta { font-family: var(--font-accent); font-size: 0.75rem; color: var(--text-muted); display: flex; gap: 1.5rem; }

        .full-story-body p { margin-bottom: 1.5rem; font-size: 1.1rem; color: #ccc; }
        .full-story-body p::first-letter {
            float: left;
            font-size: 4rem;
            line-height: 1;
            font-weight: 900;
            margin-right: 0.5rem;
            color: var(--tuko-red);
            font-family: var(--font-display);
        }
        .full-story-body p + p::first-letter { float: none; font-size: inherit; line-height: inherit; font-weight: inherit; margin-right: 0; color: inherit; font-family: inherit; }

        .story-media-block { margin: 2.5rem 0; }
        .story-media-block img { border-radius: 8px; width: 100%; }
        .img-caption { font-family: var(--font-accent); font-size: 0.75rem; color: var(--text-muted); margin-top: 0.5rem; text-align: center; font-style: italic; }

        /* ===========================
           SIDEBAR STYLING
        =========================== */
        .sidebar-widget { background: var(--card-bg); padding: 1.2rem; border-radius: 6px; margin-bottom: 1.5rem; }
        .widget-title {
            font-family: var(--font-accent);
            font-size: 0.85rem;
            font-weight: 800;
            text-transform: uppercase;
            color: white;
            margin-bottom: 1rem;
            padding-bottom: 0.5rem;
            border-bottom: 2px solid var(--tuko-red);
        }

        .trending-item { display: flex; gap: 0.8rem; margin-bottom: 1rem; align-items: center; }
        .trending-num { font-size: 1.5rem; font-weight: 900; color: #333; font-family: var(--font-display); }
        .trending-text { font-size: 0.85rem; font-weight: 600; color: #eee; line-height: 1.3; }

        /* ===========================
           VIDEO SECTION
        =========================== */
        .video-section { background: #000; padding: 3rem 0; margin: 3rem 0; }
        .video-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 1.5rem; max-width: 1280px; margin: 0 auto; padding: 0 1rem; }
        .video-card { position: relative; border-radius: 8px; overflow: hidden; height: 200px; }
        .video-card img { width: 100%; height: 100%; object-fit: cover; opacity: 0.6; }
        .play-btn {
            position: absolute;
            top: 50%; left: 50%;
            transform: translate(-50%, -50%);
            width: 50px; height: 50px;
            background: var(--tuko-red);
            border-radius: 50%;
            display: flex; align-items: center; justify-content: center;
            color: white; font-size: 1.2rem;
        }

        /* ===========================
           FOOTER
        =========================== */
        .main-footer { background: #000; color: #888; padding: 4rem 0 2rem; border-top: 4px solid var(--tuko-red); }
        .footer-inner { max-width: 1280px; margin: 0 auto; padding: 0 1rem; display: grid; grid-template-columns: repeat(4, 1fr); gap: 2rem; }
        .footer-col h4 { color: white; font-family: var(--font-accent); font-size: 0.9rem; margin-bottom: 1.5rem; text-transform: uppercase; }
        .footer-links { list-style: none; }
        .footer-links li { margin-bottom: 0.6rem; font-size: 0.8rem; }
        .footer-bottom { max-width: 1280px; margin: 2rem auto 0; padding: 2rem 1rem 0; border-top: 1px solid #222; text-align: center; font-size: 0.7rem; }

        /* Placeholders */
        .img-placeholder {
            width: 100%;
            height: 100%;
            background: #2a2a2a;
            display: flex;
            align-items: center;
            justify-content: center;
            color: #555;
            font-family: var(--font-accent);
            font-size: 0.8rem;
            text-align: center;
            padding: 1rem;
        }

        @media (max-width: 992px) {
            .content-layout { grid-template-columns: 1fr; }
            .hero-section { grid-template-columns: 1fr; }
            .stories-grid { grid-template-columns: repeat(2, 1fr); }
            .video-grid { grid-template-columns: repeat(2, 1fr); }
        }

        @media (max-width: 600px) {
            .stories-grid { grid-template-columns: 1fr; }
            .video-grid { grid-template-columns: 1fr; }
            .footer-inner { grid-template-columns: 1fr; }
        }
    </style>
</head>
<body>

<!-- Top Bar -->
<div class="top-utility-bar">
    <div class="top-utility-inner">
        <div class="top-left-links">
            <a href="#">About</a>
            <a href="#">Contact</a>
            <a href="#">Advertise</a>
        </div>
        <div class="top-right-info">
            <span id="current-date"></span>
            <div class="social-icons">
                <a href="#">FB</a>
                <a href="#">TW</a>
                <a href="#">IG</a>
            </div>
        </div>
    </div>
</div>

<!-- Breaking News -->
<div class="breaking-bar">
    <div class="breaking-inner">
        <span class="breaking-label">Breaking</span>
        <span class="ticker-text" id="ticker">Arsenal Win the Premier League 2026! Celebration erupts in London!</span>
    </div>
</div>

<!-- Header -->
<header class="main-header">
    <div class="header-inner">
        <div class="logo-wrap">
            <div class="logo-placeholder">MC</div>
            <div class="site-name">
                <h1>MIC CHEQUE</h1>
                <span>Professional Storytelling</span>
            </div>
        </div>
        <div class="header-search">
            <input type="text" placeholder="Search stories...">
            <button>🔍</button>
        </div>
    </div>
</header>

<!-- Nav -->
<nav class="main-nav">
    <div class="nav-inner">
        <ul class="nav-menu">
            <li><a href="#" class="active">Home</a></li>
            <li><a href="#tech">Technology</a></li>
            <li><a href="#culture">Culture</a></li>
            <li><a href="#sports">Sports</a></li>
            <li><a href="#lifestyle">Lifestyle</a></li>
            <li><a href="#video">Video</a></li>
        </ul>
    </div>
</nav>

<div class="page-wrapper">
    <div class="content-layout">
        
        <!-- Main Content -->
        <main class="main-content">
            
            <!-- Hero Section -->
            <div class="hero-section">
                <div class="hero-main">
                    <video width="100%" height="100%" style="object-fit: cover;" poster="./tech_story_1.jpg" controls>
                        <source src="./Arsenal.mp4" type="video/mp4">
                        Your browser does not support the video tag.
                    </video>
                    <div class="hero-overlay" style="pointer-events: none;">
                        <span class="card-category">Sports</span>
                        <h2 class="hero-title">Arsenal Crowned Premier League Champions 2026: The 22-Year Wait is Over</h2>
                    </div>
                </div>
                <div class="hero-side">
                    <div class="story-card" style="display: flex; height: 195px; margin-bottom: 10px;">
                        <div style="width: 40%; background: #333;"><img src="./tech_story_2.jpg" alt="Festival" style="height: 100%; object-fit: cover;"></div>
                        <div class="card-body" style="width: 60%;">
                            <span class="card-category">Culture</span>
                            <h3 class="card-title" style="font-size: 0.9rem;">Summertides Festival 2026: Nairobi's Biggest Music Event</h3>
                        </div>
                    </div>
                    <div class="story-card" style="display: flex; height: 195px;">
                        <div style="width: 40%; background: #333;"><img src="./tech_story_3.jpg" alt="Nyashinski" style="height: 100%; object-fit: cover;"></div>
                        <div class="card-body" style="width: 60%;">
                            <span class="card-category">Entertainment</span>
                            <h3 class="card-title" style="font-size: 0.9rem;">Nyashinski Shuts Down Kasarani with Historic Performance</h3>
                        </div>
                    </div>
                </div>
            </div>

            <!-- FULL STORY 1: NAIROBI TECH -->
            <div class="section-header" id="tech">
                <h2 class="section-title">Featured Story: Technology</h2>
            </div>
            <article class="full-story-wrap">
                <div class="full-story-header">
                    <h2 class="full-story-title">Nairobi's Tech Hustle: From Small Rooms to Global Impact</h2>
                    <div class="full-story-meta">
                        <span>📅 April 17, 2026</span>
                        <span>⏱️ 8 min read</span>
                        <span>✍️ MIC CHEQUE Staff</span>
                    </div>
                </div>
                <div class="full-story-body">
                    <p>In the modern heartbeat of Kenya, Nairobi has grown into one of Africa's most influential innovation centers. What once looked like a city focused mainly on trade and administration is now home to fast-growing startups, digital creators, and software engineers shaping solutions for global markets.</p>
                    <p>This transformation did not happen overnight. It started in small internet cafés, university dorm rooms, and cramped rented apartments where young people experimented with code, design, and online business ideas. Many had no formal funding, no advanced equipment, and limited mentorship. What they had was curiosity and persistence.</p>
                    <div class="story-media-block">
                        <img src="./tech_story_1.jpg" alt="Nairobi Tech Innovation">
                        <p class="img-caption">Nairobi's tech ecosystem continues to attract global attention — Photo: MIC CHEQUE</p>
                    </div>
                    <p>Today, those early experiments have evolved into real companies. Fintech platforms are now handling payments across East Africa. Logistics startups are improving delivery systems for small businesses. Health-tech tools are helping patients in remote areas access medical advice without traveling long distances.</p>
                    <p>A major driver of this growth is mobile technology. With widespread smartphone adoption and mobile money systems, developers have been able to build services that reach millions instantly. This has made Kenya one of the most advanced mobile-first economies in the world.</p>
                    <div class="story-media-block">
                        <img src="./tech_story_2.jpg" alt="Mobile Technology in Kenya">
                        <p class="img-caption">Mobile technology is the backbone of Kenya's digital economy — Photo: MIC CHEQUE</p>
                    </div>
                    <p>However, the journey is still far from easy. Many startups struggle with funding gaps, especially at early stages. Others face infrastructure challenges such as inconsistent internet in certain areas or high operational costs. Competition is also intense, with hundreds of new ideas launched every year.</p>
                    <div class="story-media-block">
                        <img src="./tech_story_3.jpg" alt="Startups in Nairobi">
                        <p class="img-caption">Startup culture is thriving despite funding challenges — Photo: MIC CHEQUE</p>
                    </div>
                    <p>Despite these challenges, the energy remains strong. Incubators and innovation hubs continue to support young talent. Universities are producing more tech graduates than ever before. International investors are increasingly paying attention to Nairobi as a serious tech destination.</p>
                    <p>What stands out most is the mindset shift. Young innovators are no longer waiting for jobs—they are building them. They are creating platforms that solve local problems while also competing globally. Nairobi is no longer just participating in the digital economy; it is actively shaping it.</p>
                    <div class="story-media-block">
                        <img src="./tech_story_4.jpg" alt="Future of Nairobi Tech">
                        <p class="img-caption">The future of Nairobi's tech scene looks brighter than ever — Photo: MIC CHEQUE</p>
                    </div>
                </div>
            </article>

            <!-- FULL STORY 2: MATATU CULTURE -->
            <div class="section-header" id="culture">
                <h2 class="section-title">Deep Dive: Culture</h2>
            </div>
            <article class="full-story-wrap">
                <div class="full-story-header">
                    <h2 class="full-story-title">Nairobi Matatu Culture: The Moving Art That Never Sleeps</h2>
                    <div class="full-story-meta">
                        <span>📅 April 17, 2026</span>
                        <span>⏱️ 6 min read</span>
                        <span>✍️ MIC CHEQUE Staff</span>
                    </div>
                </div>
                <div class="full-story-body">
                    <p>In the fast-moving urban life of Kenya, few things define daily experience more vividly than the matatu system. These minibuses are not just a transport network—they are a living cultural phenomenon that blends art, music, economy, and street identity into one moving ecosystem.</p>
                    <p>Every matatu begins its identity long before it hits the road. Artists spend hours designing graffiti-style exteriors, often inspired by pop culture, local heroes, music icons, or social themes. Inside, the transformation continues with LED lights, high-powered sound systems, custom seats, and unique branding that makes each vehicle distinct.</p>
                    <div class="story-media-block">
                        <img src="./matatu_story_1.jpg" alt="Matatu Graffiti Art">
                        <p class="img-caption">Matatu graffiti art is a statement of identity and culture — Photo: MIC CHEQUE</p>
                    </div>
                    <p>For passengers, stepping into a matatu is an experience of its own. Music fills the air, sometimes so loud it becomes part of the ride itself. Conductors call out destinations in fast, rhythmic chants that feel like performance poetry. Young people often see matatus as more than transport—they are social spaces where conversations, trends, and culture are exchanged.</p>
                    <div class="story-media-block">
                        <img src="./matatu_story_2.jpg" alt="Matatu Interior Experience">
                        <p class="img-caption">Inside a matatu — a sensory experience unlike any other — Photo: MIC CHEQUE</p>
                    </div>
                    <p>Behind this creativity is a crucial transport system that keeps Nairobi moving. Every day, millions of people rely on matatus to travel to work, school, markets, and hospitals. Without them, the city's mobility would collapse under pressure.</p>
                    <div class="story-media-block">
                        <img src="./matatu_story_3.jpg" alt="Nairobi Public Transport">
                        <p class="img-caption">Matatus are the lifeblood of Nairobi's public transport network — Photo: MIC CHEQUE</p>
                    </div>
                    <p>But the system operates in a complex environment. Traffic congestion in Nairobi is among the most challenging in the region, often causing long delays during peak hours. Route competition between operators can be intense, with each sacco trying to dominate popular routes. Regulations also evolve frequently, affecting pricing, design, and operation standards.</p>
                    <div class="story-media-block">
                        <img src="./matatu_story_4.jpg" alt="Nairobi Matatu Culture">
                        <p class="img-caption">Competition on popular routes is fierce among matatu saccos — Photo: MIC CHEQUE</p>
                    </div>
                    <p>Despite these issues, matatu culture continues to evolve rather than disappear. New designs appear regularly, each trying to push boundaries in creativity and style. The culture has even influenced fashion, music, and digital content creation, becoming a symbol of urban expression.</p>
                    <p>For outsiders, it may look chaotic. For locals, it is structured chaos with rhythm and identity. It represents survival, creativity, and movement all at once. Matatus are not just buses; they are the soul of Nairobi's streets.</p>
                </div>
            </article>

            <!-- More Stories Grid -->
            <div class="section-header">
                <h2 class="section-title">More Stories</h2>
            </div>
            <div class="stories-grid">
                <div class="story-card">
                    <div class="card-img"><img src="./tech_story_1.jpg" alt="AI Hub"></div>
                    <div class="card-body">
                        <span class="card-category">Tech</span>
                        <h3 class="card-title">Kenya Launches New AI Research Hub in Nairobi</h3>
                    </div>
                </div>
                <div class="story-card">
                    <div class="card-img"><img src="./matatu_story_2.jpg" alt="Fashion"></div>
                    <div class="card-body">
                        <span class="card-category">Lifestyle</span>
                        <h3 class="card-title">Nairobi Fashion Week 2026: Top Trends to Watch</h3>
                    </div>
                </div>
                <div class="story-card">
                    <div class="card-img"><img src="./tech_story_4.jpg" alt="Economy"></div>
                    <div class="card-body">
                        <span class="card-category">Business</span>
                        <h3 class="card-title">Kenyan Shilling Strengthens Against Major Currencies</h3>
                    </div>
                </div>
            </div>

            <!-- New Stories Section -->
            <div class="section-header" id="new-stories">
                <h2 class="section-title">New Stories</h2>
            </div>
            <div class="stories-grid">
                <div class="story-card">
                    <div class="card-img"><img src="./matatu_story_1.jpg" alt="Lamu"></div>
                    <div class="card-body">
                        <span class="card-category">Travel</span>
                        <h3 class="card-title">Hidden Gems: Exploring the Magic of Lamu Island</h3>
                    </div>
                </div>
                <div class="story-card">
                    <div class="card-img"><img src="./tech_story_2.jpg" alt="Wellness"></div>
                    <div class="card-body">
                        <span class="card-category">Wellness</span>
                        <h3 class="card-title">Rift Valley Retreats: The Ultimate Wellness Guide</h3>
                    </div>
                </div>
                <div class="story-card">
                    <div class="card-img">
                        <video width="100%" height="100%" style="object-fit: cover;" poster="./tech_story_3.jpg" controls>
                            <source src="./Streetfood.mp4" type="video/mp4">
                            Your browser does not support the video tag.
                        </video>
                    </div>
                    <div class="card-body">
                        <span class="card-category">Food</span>
                        <h3 class="card-title">Nairobi's Best Street Food: A Culinary Journey</h3>
                    </div>
                </div>
            </div>

        </main>

        <!-- Sidebar -->
        <aside class="sidebar">
            
            <div class="sidebar-widget">
                <h3 class="widget-title">Trending Now</h3>
                <div class="trending-item">
                    <span class="trending-num">1</span>
                    <p class="trending-text">Arsenal 2026 Victory Parade: Millions Expected in London</p>
                </div>
                <div class="trending-item">
                    <span class="trending-num">2</span>
                    <p class="trending-text">Nyashinski's New Album Breaks Streaming Records in 24 Hours</p>
                </div>
                <div class="trending-item">
                    <span class="trending-num">3</span>
                    <p class="trending-text">Summertides Festival 2026: Full Artist Lineup Revealed</p>
                </div>
                <div class="trending-item">
                    <span class="trending-num">4</span>
                    <p class="trending-text">Safaricom Announces 6G Pilot Program in Nairobi</p>
                </div>
                <div class="trending-item">
                    <span class="trending-num">5</span>
                    <p class="trending-text">New Housing Projects Set to Transform Nairobi Skyline</p>
                </div>
            </div>

            <div class="sidebar-widget">
                <h3 class="widget-title">Latest Stories</h3>
                <div style="font-size: 0.8rem; color: #ccc;">
                    <p style="margin-bottom: 0.8rem; border-bottom: 1px solid #333; padding-bottom: 0.5rem;">• Safaricom 6G Pilot: What You Need to Know</p>
                    <p style="margin-bottom: 0.8rem; border-bottom: 1px solid #333; padding-bottom: 0.5rem;">• University Debates: The Future of Education in Kenya</p>
                    <p style="margin-bottom: 0.8rem; border-bottom: 1px solid #333; padding-bottom: 0.5rem;">• Nairobi Expressway Phase 2: Construction Updates</p>
                    <p>• Kenya's Green Energy Revolution: New Wind Farm Opens</p>
                </div>
            </div>

            <div class="sidebar-widget" style="background: var(--tuko-red); color: white;">
                <h3 class="widget-title" style="border-color: white;">Newsletter</h3>
                <p style="font-size: 0.8rem; margin-bottom: 1rem;">Get the best stories delivered to your inbox daily.</p>
                <input type="email" placeholder="Your email" style="width: 100%; padding: 0.5rem; border: none; border-radius: 4px; margin-bottom: 0.5rem;">
                <button style="width: 100%; padding: 0.5rem; background: #000; color: white; border: none; border-radius: 4px; font-weight: 800; cursor: pointer;">SUBSCRIBE</button>
            </div>

        </aside>
    </div>
</div>

<!-- Video Section -->
<div class="video-section" id="video">
    <div class="section-header" style="max-width: 1280px; margin: 0 auto 2rem; padding: 0 1rem;">
        <h2 class="section-title">Must Watch</h2>
    </div>
    <div class="video-grid">
        <div class="video-card">
            <video width="100%" height="100%" style="object-fit: cover;" poster="./tech_story_2.jpg" controls>
                <source src="./summertidesvideo.mp4" type="video/mp4">
                Your browser does not support the video tag.
            </video>
            <div style="position: absolute; bottom: 10px; left: 10px; color: white; font-size: 0.8rem; font-weight: 800; pointer-events: none;">Summertides Festival 2026 Highlights</div>
        </div>
        <div class="video-card">
            <img src="./tech_story_3.jpg" alt="Nyashinski">
            <div class="play-btn">▶</div>
            <div style="position: absolute; bottom: 10px; left: 10px; color: white; font-size: 0.8rem; font-weight: 800;">Nyashinski Live at Kasarani Stadium</div>
        </div>
        <div class="video-card">
            <video width="100%" height="100%" style="object-fit: cover;" poster="./tech_story_1.jpg" controls>
                <source src="./Arsenal.mp4" type="video/mp4">
                Your browser does not support the video tag.
            </video>
            <div style="position: absolute; bottom: 10px; left: 10px; color: white; font-size: 0.8rem; font-weight: 800; pointer-events: none;">Arsenal: The Road to the 2026 Title</div>
        </div>
    </div>
</div>

<footer class="main-footer">
    <div class="footer-inner">
        <div class="footer-col">
            <h4 style="font-family: var(--font-display); color: white; font-size: 1.2rem;">MIC CHEQUE</h4>
            <p style="font-size: 0.75rem; line-height: 1.8;">Professional storytelling and deep dives into the heart of Kenya's culture, technology, and lifestyle.</p>
        </div>
        <div class="footer-col">
            <h4>Sections</h4>
            <ul class="footer-links">
                <li><a href="#tech">Technology</a></li>
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
            <div class="social-icons" style="display: flex; gap: 1rem;">
                <a href="#" style="color: white; font-size: 1.2rem;" title="Facebook"><i class="fab fa-facebook"></i></a>
                <a href="#" style="color: white; font-size: 1.2rem;" title="Twitter"><i class="fab fa-twitter"></i></a>
                <a href="#" style="color: white; font-size: 1.2rem;" title="Instagram"><i class="fab fa-instagram"></i></a>
                <a href="#" style="color: white; font-size: 1.2rem;" title="YouTube"><i class="fab fa-youtube"></i></a>
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
</script>

</body>
</html>
