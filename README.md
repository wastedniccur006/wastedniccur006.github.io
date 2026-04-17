<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>MIC CHEQUE | Professional Storytelling</title>
    <link href="https://fonts.googleapis.com/css2?family=Cinzel+Decorative:wght@400;700;900&family=Playfair+Display:ital,wght@0,400;0,700;0,900;1,400&family=Lora:ital,wght@0,400;0,700;1,400&family=Montserrat:wght@300;400;600;800&display=swap" rel="stylesheet">
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
           FULL STORY ARTICLE (DARK)
        =========================== */
        .full-story-wrap {
            background: var(--card-bg);
            border-radius: 6px;
            padding: 2rem;
            margin-bottom: 2rem;
            box-shadow: 0 4px 20px rgba(0,0,0,0.3);
        }

        .full-story-header {
            border-bottom: 1px solid #333;
            padding-bottom: 1.5rem;
            margin-bottom: 1.5rem;
        }

        .full-story-title {
            font-family: var(--font-heading);
            font-size: 2.2rem;
            font-weight: 900;
            color: #fff;
            line-height: 1.2;
            margin-bottom: 1rem;
        }

        .full-story-meta {
            font-family: var(--font-accent);
            font-size: 0.75rem;
            color: var(--text-muted);
            display: flex;
            gap: 1.5rem;
        }

        .full-story-body {
            font-family: var(--font-body);
            font-size: 1.1rem;
            line-height: 1.8;
            color: #ccc;
        }

        .full-story-body p { margin-bottom: 1.5rem; }

        .story-media-block {
            margin: 2rem 0;
            border-radius: 8px;
            overflow: hidden;
        }

        .img-placeholder {
            width: 100%; height: 300px;
            background: #2a2a2a;
            display: flex; align-items: center; justify-content: center;
            color: #555; font-size: 0.9rem; text-align: center;
        }

        .img-caption {
            font-family: var(--font-accent);
            font-size: 0.75rem;
            color: #666;
            padding: 0.5rem 0;
            font-style: italic;
            border-bottom: 1px solid #222;
        }

        /* ===========================
           SIDEBAR WIDGETS
        =========================== */
        .sidebar-widget {
            background: var(--card-bg);
            padding: 1.2rem;
            border-radius: 6px;
            margin-bottom: 1.5rem;
        }

        .widget-title {
            font-size: 0.85rem;
            font-weight: 800;
            text-transform: uppercase;
            color: #fff;
            border-bottom: 2px solid var(--tuko-red);
            padding-bottom: 0.5rem;
            margin-bottom: 1rem;
        }

        .trending-item {
            display: flex;
            gap: 0.8rem;
            padding: 0.8rem 0;
            border-bottom: 1px solid #333;
        }

        .trending-num { font-size: 1.5rem; font-weight: 900; color: #444; }
        .trending-title { font-size: 0.85rem; color: #fff; font-family: var(--font-heading); }

        /* ===========================
           VIDEO SECTION
        =========================== */
        .video-section {
            background: #000;
            padding: 3rem 0;
            margin-top: 2rem;
        }

        .video-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 1.5rem;
            max-width: 1280px;
            margin: 0 auto;
            padding: 0 1rem;
        }

        .video-card { background: #111; border-radius: 8px; overflow: hidden; }
        .video-thumb { position: relative; padding-top: 56.25%; background: #222; }
        .video-thumb video { position: absolute; top: 0; left: 0; width: 100%; height: 100%; object-fit: cover; }
        .video-info { padding: 1rem; }
        .video-title { color: white; font-size: 0.95rem; font-weight: 700; }

        /* ===========================
           FOOTER
        =========================== */
        footer {
            background: #000;
            padding: 4rem 1rem 2rem;
            border-top: 1px solid #222;
        }

        .footer-inner { max-width: 1280px; margin: 0 auto; display: grid; grid-template-columns: 2fr 1fr 1fr 1fr; gap: 2rem; }
        .footer-col h4 { color: white; margin-bottom: 1.5rem; text-transform: uppercase; font-size: 0.8rem; }
        .footer-col ul { list-style: none; }
        .footer-col li { margin-bottom: 0.8rem; font-size: 0.8rem; color: #888; }

        /* ===========================
           RESPONSIVE
        =========================== */
        @media (max-width: 1024px) {
            .content-layout { grid-template-columns: 1fr; }
            .stories-grid { grid-template-columns: 1fr 1fr; }
        }

        @media (max-width: 768px) {
            .hero-section { grid-template-columns: 1fr; }
            .stories-grid { grid-template-columns: 1fr; }
            .video-grid { grid-template-columns: 1fr; }
            .footer-inner { grid-template-columns: 1fr; }
            .full-story-title { font-size: 1.6rem; }
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
                    <div class="img-placeholder">Arsenal 2026 Champions Image</div>
                    <div class="hero-overlay">
                        <span class="card-category">Sports</span>
                        <h2 class="hero-title">Arsenal Crowned Premier League Champions 2026: The 22-Year Wait is Over</h2>
                    </div>
                </div>
                <div class="hero-side">
                    <div class="story-card" style="display: flex; height: 195px; margin-bottom: 10px;">
                        <div style="width: 40%; background: #333;"><div class="img-placeholder">Festival</div></div>
                        <div class="card-body" style="width: 60%;">
                            <span class="card-category">Culture</span>
                            <h3 class="card-title" style="font-size: 0.9rem;">Summertides Festival 2026: Nairobi's Biggest Music Event</h3>
                        </div>
                    </div>
                    <div class="story-card" style="display: flex; height: 195px;">
                        <div style="width: 40%; background: #333;"><div class="img-placeholder">Nyashinski</div></div>
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
                        <div class="img-placeholder">Nairobi Tech Innovation Image</div>
                        <p class="img-caption">Nairobi's tech ecosystem continues to attract global attention — Photo: MIC CHEQUE</p>
                    </div>
                    <p>Today, those early experiments have evolved into real companies. Fintech platforms are now handling payments across East Africa. Logistics startups are improving delivery systems for small businesses. Health-tech tools are helping patients in remote areas access medical advice without traveling long distances.</p>
                    <p>A major driver of this growth is mobile technology. With widespread smartphone adoption and mobile money systems, developers have been able to build services that reach millions instantly. This has made Kenya one of the most advanced mobile-first economies in the world.</p>
                    <div class="story-media-block">
                        <div class="img-placeholder">Mobile Technology in Kenya Image</div>
                        <p class="img-caption">Mobile technology is the backbone of Kenya's digital economy — Photo: MIC CHEQUE</p>
                    </div>
                    <p>However, the journey is still far from easy. Many startups struggle with funding gaps, especially at early stages. Others face infrastructure challenges such as inconsistent internet in certain areas or high operational costs. Competition is also intense, with hundreds of new ideas launched every year.</p>
                    <div class="story-media-block">
                        <div class="img-placeholder">Startups in Nairobi Image</div>
                        <p class="img-caption">Startup culture is thriving despite funding challenges — Photo: MIC CHEQUE</p>
                    </div>
                    <p>Despite these challenges, the energy remains strong. Incubators and innovation hubs continue to support young talent. Universities are producing more tech graduates than ever before. International investors are increasingly paying attention to Nairobi as a serious tech destination.</p>
                    <p>What stands out most is the mindset shift. Young innovators are no longer waiting for jobs—they are building them. They are creating platforms that solve local problems while also competing globally. Nairobi is no longer just participating in the digital economy; it is actively shaping it.</p>
                    <div class="story-media-block">
                        <div class="img-placeholder">Future of Nairobi Tech Image</div>
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
                        <div class="img-placeholder">Matatu Graffiti Art Image</div>
                        <p class="img-caption">Matatu graffiti art is a statement of identity and culture — Photo: MIC CHEQUE</p>
                    </div>
                    <p>For passengers, stepping into a matatu is an experience of its own. Music fills the air, sometimes so loud it becomes part of the ride itself. Conductors call out destinations in fast, rhythmic chants that feel like performance poetry. Young people often see matatus as more than transport—they are social spaces where conversations, trends, and culture are exchanged.</p>
                    <div class="story-media-block">
                        <div class="img-placeholder">Matatu Interior Experience Image</div>
                        <p class="img-caption">Inside a matatu — a sensory experience unlike any other — Photo: MIC CHEQUE</p>
                    </div>
                    <p>Behind this creativity is a crucial transport system that keeps Nairobi moving. Every day, millions of people rely on matatus to travel to work, school, markets, and hospitals. Without them, the city's mobility would collapse under pressure.</p>
                    <div class="story-media-block">
                        <div class="img-placeholder">Nairobi Public Transport Image</div>
                        <p class="img-caption">Matatus are the lifeblood of Nairobi's public transport network — Photo: MIC CHEQUE</p>
                    </div>
                    <p>But the system operates in a complex environment. Traffic congestion in Nairobi is among the most challenging in the region, often causing long delays during peak hours. Route competition between operators can be intense, with each sacco trying to dominate popular routes. Regulations also evolve frequently, affecting pricing, design, and operation standards.</p>
                    <div class="story-media-block">
                        <div class="img-placeholder">Matatu Route Competition Image</div>
                        <p class="img-caption">Competition on popular routes is fierce among matatu saccos — Photo: MIC CHEQUE</p>
                    </div>
                    <p>Despite these issues, matatu culture continues to evolve rather than disappear. New designs appear regularly, each trying to push boundaries in creativity and style. The culture has even influenced fashion, music, and digital content creation, becoming a symbol of urban expression.</p>
                    <p>For outsiders, it may look chaotic. For locals, it is structured chaos with rhythm and identity. It represents survival, creativity, and movement all at once. Matatus are not just part of Nairobi—they are Nairobi in motion.</p>
                </div>
            </article>

            <!-- More Stories Section -->
            <div class="section-header">
                <h2 class="section-title">More Stories</h2>
            </div>
            <div class="stories-grid">
                <article class="story-card">
                    <div class="card-img"><div class="img-placeholder">Tech News</div></div>
                    <div class="card-body">
                        <span class="card-category">Technology</span>
                        <h3 class="card-title">Kenya's Silicon Savannah Welcomes New AI Hub</h3>
                        <p class="card-excerpt">A major investment in Nairobi's tech scene aims to position Kenya as Africa's AI leader.</p>
                    </div>
                </article>
                <article class="story-card">
                    <div class="card-img"><div class="img-placeholder">Fashion</div></div>
                    <div class="card-body">
                        <span class="card-category">Lifestyle</span>
                        <h3 class="card-title">Nairobi Fashion Week: The Bold and the Beautiful</h3>
                        <p class="card-excerpt">Local designers showcase stunning collections that blend tradition with modern flair.</p>
                    </div>
                </article>
                <article class="story-card">
                    <div class="card-img"><div class="img-placeholder">Economy</div></div>
                    <div class="card-body">
                        <span class="card-category">Business</span>
                        <h3 class="card-title">Shilling Strengthens Against the Dollar in Q1 2026</h3>
                        <p class="card-excerpt">Economic analysts predict a stable year for the Kenyan currency following new trade deals.</p>
                    </div>
                </article>
            </div>

            <!-- New Stories Section -->
            <div class="section-header">
                <h2 class="section-title">New Stories</h2>
            </div>
            <div class="stories-grid">
                <article class="story-card">
                    <div class="card-img"><div class="img-placeholder">Travel</div></div>
                    <div class="card-body">
                        <span class="card-category">Travel</span>
                        <h3 class="card-title">Hidden Gems: 5 Must-Visit Spots in Lamu</h3>
                        <p class="card-excerpt">Discover the untouched beauty of Lamu's quietest beaches and historic alleys.</p>
                    </div>
                </article>
                <article class="story-card">
                    <div class="card-img"><div class="img-placeholder">Health</div></div>
                    <div class="card-body">
                        <span class="card-category">Health</span>
                        <h3 class="card-title">The Rise of Wellness Retreats in the Rift Valley</h3>
                        <p class="card-excerpt">Why more Kenyans are choosing nature-based healing over traditional vacations.</p>
                    </div>
                </article>
                <article class="story-card">
                    <div class="card-img"><div class="img-placeholder">Food</div></div>
                    <div class="card-body">
                        <span class="card-category">Lifestyle</span>
                        <h3 class="card-title">Nairobi's Best Street Food: A Culinary Tour</h3>
                        <p class="card-excerpt">From smoky mutura to spicy bhajias, we explore the city's favorite flavors.</p>
                    </div>
                </article>
            </div>

        </main>

        <!-- Sidebar -->
        <aside class="sidebar">
            
            <div class="sidebar-widget">
                <h3 class="widget-title">Trending Now</h3>
                <div class="trending-item">
                    <span class="trending-num">1</span>
                    <div class="trending-title">Arsenal's 2026 Victory Parade: Full Route and Details</div>
                </div>
                <div class="trending-item">
                    <span class="trending-num">2</span>
                    <div class="trending-title">Nyashinski's New Album 'Legacy' Breaks Streaming Records</div>
                </div>
                <div class="trending-item">
                    <span class="trending-num">3</span>
                    <div class="trending-title">Summertides Festival: Early Bird Tickets Sold Out in Minutes</div>
                </div>
                <div class="trending-item">
                    <span class="trending-num">4</span>
                    <div class="trending-title">How to Secure Your 2027 General Election Voter ID</div>
                </div>
                <div class="trending-item">
                    <span class="trending-num">5</span>
                    <div class="trending-title">Nairobi Expressway: New Toll Rates Announced for 2026</div>
                </div>
            </div>

            <div class="sidebar-widget">
                <h3 class="widget-title">Latest</h3>
                <div style="display: flex; gap: 10px; margin-bottom: 15px;">
                    <div style="width: 60px; height: 60px; background: #333;"></div>
                    <div>
                        <h4 style="font-size: 0.75rem; color: #fff;">Safaricom Launches 6G Pilot in Nairobi CBD</h4>
                        <span style="font-size: 0.6rem; color: #666;">10 mins ago</span>
                    </div>
                </div>
                <div style="display: flex; gap: 10px; margin-bottom: 15px;">
                    <div style="width: 60px; height: 60px; background: #333;"></div>
                    <div>
                        <h4 style="font-size: 0.75rem; color: #fff;">Kenyatta University Wins Inter-Varsity Debate</h4>
                        <span style="font-size: 0.6rem; color: #666;">45 mins ago</span>
                    </div>
                </div>
                <div style="display: flex; gap: 10px;">
                    <div style="width: 60px; height: 60px; background: #333;"></div>
                    <div>
                        <h4 style="font-size: 0.75rem; color: #fff;">New Housing Project Launched in Ruiru</h4>
                        <span style="font-size: 0.6rem; color: #666;">2 hours ago</span>
                    </div>
                </div>
            </div>

        </aside>
    </div>
</div>

<!-- Video Section -->
<section class="video-section" id="video">
    <div class="section-header" style="max-width: 1280px; margin: 0 auto 2rem; padding: 0 1rem;">
        <h2 class="section-title">Must Watch</h2>
    </div>
    <div class="video-grid">
        <div class="video-card">
            <div class="video-thumb">
                <video controls poster="./summertides_poster.jpg">
                    <source src="./summertides_video.mp4" type="video/mp4">
                </video>
            </div>
            <div class="video-info">
                <h4 class="video-title">Summertides Festival 2026 Highlights</h4>
            </div>
        </div>
        <div class="video-card">
            <div class="video-thumb">
                <video controls poster="./nyashinski_poster.jpg">
                    <source src="./nyashinski_video.mp4" type="video/mp4">
                </video>
            </div>
            <div class="video-info">
                <h4 class="video-title">Nyashinski Live at Kasarani Stadium</h4>
            </div>
        </div>
        <div class="video-card">
            <div class="video-thumb">
                <video controls poster="./arsenal_poster.jpg">
                    <source src="./arsenal_video.mp4" type="video/mp4">
                </video>
            </div>
            <div class="video-info">
                <h4 class="video-title">Arsenal: The Road to the 2026 Title</h4>
            </div>
        </div>
    </div>
</section>

<footer>
    <div class="footer-inner">
        <div class="footer-col">
            <h3 style="color: var(--accent-color); font-family: var(--font-display); margin-bottom: 1rem;">MIC CHEQUE</h3>
            <p style="font-size: 0.8rem; color: #666;">Professional storytelling from the heart of Kenya. NIKO KADI JE WEWE?</p>
        </div>
        <div class="footer-col">
            <h4>Sections</h4>
            <ul>
                <li>Entertainment</li>
                <li>Sports</li>
                <li>Technology</li>
                <li>Lifestyle</li>
            </ul>
        </div>
        <div class="footer-col">
            <h4>Company</h4>
            <ul>
                <li>About Us</li>
                <li>Contact</li>
                <li>Careers</li>
            </ul>
        </div>
        <div class="footer-col">
            <h4>Legal</h4>
            <ul>
                <li>Privacy Policy</li>
                <li>Terms of Use</li>
            </ul>
        </div>
    </div>
    <div style="text-align: center; margin-top: 3rem; font-size: 0.7rem; color: #444;">
        &copy; 2026 MIC CHEQUE. ALL RIGHTS RESERVED.
    </div>
</footer>

<script>
    document.getElementById('current-date').textContent = new Date().toLocaleDateString('en-US', { 
        weekday: 'long', year: 'numeric', month: 'long', day: 'numeric' 
    });

    const tickerTexts = [
        "Arsenal Win the Premier League 2026!",
        "Nyashinski's 'Legacy' Album Hits 100M Streams!",
        "Summertides Festival 2026: Full Lineup Released!",
        "Nairobi Tech Hub Secures $50M Funding!"
    ];
    let tickerIndex = 0;
    setInterval(() => {
        tickerIndex = (tickerIndex + 1) % tickerTexts.length;
        const ticker = document.getElementById('ticker');
        ticker.style.opacity = 0;
        setTimeout(() => {
            ticker.textContent = tickerTexts[tickerIndex];
            ticker.style.opacity = 1;
        }, 300);
    }, 5000);
</script>

</body>
</html>
