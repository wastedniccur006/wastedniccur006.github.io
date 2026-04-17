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

        /* Logo Fix: Using a placeholder if file missing, but styled for dark theme */
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
        }

        /* Placeholder for missing images */
        .img-placeholder {
            width: 100%; height: 100%;
            background: #2a2a2a;
            display: flex; align-items: center; justify-content: center;
            color: #555; font-size: 0.8rem; text-align: center; padding: 1rem;
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
            <!-- Logo Fix: Using a styled placeholder that looks like a logo -->
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
            <li><a href="#">Entertainment</a></li>
            <li><a href="#">Sports</a></li>
            <li><a href="#">Lifestyle</a></li>
            <li><a href="#">Politics</a></li>
            <li><a href="#">Business</a></li>
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
<section class="video-section">
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
