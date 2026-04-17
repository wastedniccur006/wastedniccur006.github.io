
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>MIC CHEQUE | Entertainment & Stories</title>
    <!-- Premium Classic & Modern Font Pairing -->
    <link href="https://fonts.googleapis.com/css2?family=Cinzel+Decorative:wght@400;700;900&family=Playfair+Display:ital,wght@0,400;0,700;0,900;1,400&family=Lora:ital,wght@0,400;0,700;1,400&family=Montserrat:wght@300;400;600;800&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary-color: #1a1a1a;
            --accent-color: #c5a059;
            --text-color: #333333;
            --bg-color: #f5f5f5;
            --card-bg: #ffffff;
            --tuko-red: #e74c3c;
            --tuko-dark: #2c3e50;
            --font-heading: 'Playfair Display', serif;
            --font-display: 'Cinzel Decorative', serif;
            --font-body: 'Lora', serif;
            --font-accent: 'Montserrat', sans-serif;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            background-color: var(--bg-color);
            color: var(--text-color);
            font-family: var(--font-body);
            line-height: 1.6;
            -webkit-font-smoothing: antialiased;
            overflow-x: hidden;
        }

        /* TUKO Style Top Bar */
        .top-bar {
            background: var(--tuko-dark);
            color: white;
            padding: 0.5rem 0;
            font-family: var(--font-accent);
            font-size: 0.75rem;
            border-bottom: 3px solid var(--tuko-red);
        }

        .top-bar-content {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 1rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .breaking-news {
            display: flex;
            align-items: center;
            gap: 1rem;
        }

        .breaking-label {
            background: var(--tuko-red);
            color: white;
            padding: 0.25rem 0.75rem;
            font-weight: 800;
            text-transform: uppercase;
            letter-spacing: 1px;
            animation: pulse 2s infinite;
        }

        @keyframes pulse {
            0%, 100% { opacity: 1; }
            50% { opacity: 0.7; }
        }

        .ticker-text {
            color: #fff;
            font-weight: 600;
        }

        /* Header & Logo - TUKO Style */
        .main-header {
            background: white;
            padding: 1rem 0;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
            position: sticky;
            top: 0;
            z-index: 1000;
        }

        .header-content {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 1rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo-section {
            display: flex;
            align-items: center;
            gap: 1rem;
        }

        .logo-section img {
            height: 50px;
            width: auto;
        }

        .site-branding h1 {
            font-family: var(--font-display);
            font-size: 2rem;
            color: var(--primary-color);
            letter-spacing: 2px;
            margin: 0;
        }

        .site-branding span {
            font-family: var(--font-accent);
            font-size: 0.7rem;
            color: var(--tuko-red);
            text-transform: uppercase;
            letter-spacing: 3px;
            font-weight: 800;
        }

        /* Navigation - TUKO Style */
        .main-nav {
            background: var(--primary-color);
            padding: 0;
        }

        .nav-content {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 1rem;
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
            padding: 1rem 1.5rem;
            color: white;
            text-decoration: none;
            font-family: var(--font-accent);
            font-size: 0.8rem;
            font-weight: 600;
            text-transform: uppercase;
            letter-spacing: 1px;
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
            max-width: 1200px;
            margin: 0 auto;
            padding: 2rem 1rem;
        }

        /* Section Headers */
        .section-header {
            display: flex;
            align-items: center;
            justify-content: space-between;
            margin-bottom: 2rem;
            padding-bottom: 0.5rem;
            border-bottom: 3px solid var(--tuko-red);
        }

        .section-title {
            font-family: var(--font-accent);
            font-size: 1.5rem;
            font-weight: 800;
            text-transform: uppercase;
            letter-spacing: 2px;
            color: var(--primary-color);
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }

        .section-title::before {
            content: '';
            display: inline-block;
            width: 8px;
            height: 24px;
            background: var(--tuko-red);
        }

        .view-all {
            font-family: var(--font-accent);
            font-size: 0.8rem;
            color: var(--tuko-red);
            text-decoration: none;
            font-weight: 600;
            text-transform: uppercase;
        }

        /* Featured Story - Hero Section */
        .featured-story {
            display: grid;
            grid-template-columns: 1.2fr 1fr;
            gap: 2rem;
            margin-bottom: 3rem;
            background: white;
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 5px 20px rgba(0,0,0,0.1);
        }

        .featured-media {
            position: relative;
            min-height: 400px;
            background: #000;
        }

        .featured-media video,
        .featured-media img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        .video-overlay {
            position: absolute;
            bottom: 0;
            left: 0;
            right: 0;
            padding: 2rem;
            background: linear-gradient(to top, rgba(0,0,0,0.8), transparent);
            color: white;
        }

        .play-button {
            width: 60px;
            height: 60px;
            background: var(--tuko-red);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin-bottom: 1rem;
            cursor: pointer;
            transition: transform 0.3s;
        }

        .play-button:hover {
            transform: scale(1.1);
        }

        .play-button::after {
            content: '▶';
            font-size: 1.5rem;
            margin-left: 4px;
        }

        .featured-content {
            padding: 2rem;
            display: flex;
            flex-direction: column;
            justify-content: center;
        }

        .category-tag {
            display: inline-block;
            background: var(--tuko-red);
            color: white;
            padding: 0.25rem 0.75rem;
            font-family: var(--font-accent);
            font-size: 0.7rem;
            font-weight: 700;
            text-transform: uppercase;
            letter-spacing: 1px;
            margin-bottom: 1rem;
            width: fit-content;
        }

        .featured-title {
            font-family: var(--font-heading);
            font-size: 2rem;
            font-weight: 900;
            line-height: 1.2;
            margin-bottom: 1rem;
            color: var(--primary-color);
        }

        .featured-excerpt {
            font-size: 1rem;
            color: #666;
            margin-bottom: 1.5rem;
        }

        .meta-info {
            display: flex;
            gap: 1.5rem;
            font-family: var(--font-accent);
            font-size: 0.75rem;
            color: #999;
            text-transform: uppercase;
        }

        .meta-info span {
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }

        /* Stories Grid - TUKO Style Cards */
        .stories-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 2rem;
            margin-bottom: 3rem;
        }

        .story-card {
            background: white;
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 3px 15px rgba(0,0,0,0.08);
            transition: transform 0.3s, box-shadow 0.3s;
            cursor: pointer;
        }

        .story-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 30px rgba(0,0,0,0.15);
        }

        .story-image {
            position: relative;
            height: 200px;
            overflow: hidden;
        }

        .story-image img,
        .story-image video {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.3s;
        }

        .story-card:hover .story-image img,
        .story-card:hover .story-image video {
            transform: scale(1.05);
        }

        .video-badge {
            position: absolute;
            top: 1rem;
            right: 1rem;
            background: var(--tuko-red);
            color: white;
            padding: 0.25rem 0.5rem;
            font-family: var(--font-accent);
            font-size: 0.7rem;
            font-weight: 700;
            border-radius: 4px;
        }

        .story-content {
            padding: 1.5rem;
        }

        .story-category {
            font-family: var(--font-accent);
            font-size: 0.7rem;
            font-weight: 700;
            text-transform: uppercase;
            letter-spacing: 1px;
            color: var(--tuko-red);
            margin-bottom: 0.5rem;
        }

        .story-title {
            font-family: var(--font-heading);
            font-size: 1.1rem;
            font-weight: 700;
            line-height: 1.3;
            margin-bottom: 0.75rem;
            color: var(--primary-color);
            display: -webkit-box;
            -webkit-line-clamp: 2;
            -webkit-box-orient: vertical;
            overflow: hidden;
        }

        .story-excerpt {
            font-size: 0.9rem;
            color: #666;
            line-height: 1.5;
            display: -webkit-box;
            -webkit-line-clamp: 3;
            -webkit-box-orient: vertical;
            overflow: hidden;
            margin-bottom: 1rem;
        }

        .story-meta {
            font-family: var(--font-accent);
            font-size: 0.7rem;
            color: #999;
            text-transform: uppercase;
            display: flex;
            justify-content: space-between;
        }

        /* Two Column Layout */
        .two-column {
            display: grid;
            grid-template-columns: 2fr 1fr;
            gap: 2rem;
        }

        /* Sidebar */
        .sidebar {
            position: sticky;
            top: 100px;
            height: fit-content;
        }

        .sidebar-widget {
            background: white;
            padding: 1.5rem;
            border-radius: 8px;
            margin-bottom: 2rem;
            box-shadow: 0 3px 15px rgba(0,0,0,0.08);
        }

        .widget-title {
            font-family: var(--font-accent);
            font-size: 1rem;
            font-weight: 800;
            text-transform: uppercase;
            letter-spacing: 1px;
            color: var(--primary-color);
            margin-bottom: 1rem;
            padding-bottom: 0.5rem;
            border-bottom: 2px solid var(--tuko-red);
        }

        .trending-list {
            list-style: none;
        }

        .trending-item {
            display: flex;
            gap: 1rem;
            padding: 1rem 0;
            border-bottom: 1px solid #eee;
        }

        .trending-item:last-child {
            border-bottom: none;
        }

        .trending-number {
            font-family: var(--font-display);
            font-size: 2rem;
            font-weight: 900;
            color: var(--tuko-red);
            opacity: 0.3;
            line-height: 1;
        }

        .trending-content h4 {
            font-family: var(--font-heading);
            font-size: 0.95rem;
            font-weight: 700;
            margin-bottom: 0.25rem;
            color: var(--primary-color);
        }

        .trending-content span {
            font-family: var(--font-accent);
            font-size: 0.7rem;
            color: #999;
            text-transform: uppercase;
        }

        /* Video Section Special Styling */
        .video-section {
            background: linear-gradient(135deg, #1a1a1a 0%, #2c3e50 100%);
            padding: 3rem 0;
            margin: 3rem 0;
        }

        .video-section .section-title {
            color: white;
        }

        .video-section .section-title::before {
            background: var(--accent-color);
        }

        .video-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(350px, 1fr));
            gap: 2rem;
        }

        .video-card {
            background: rgba(255,255,255,0.05);
            border-radius: 8px;
            overflow: hidden;
            border: 1px solid rgba(255,255,255,0.1);
        }

        .video-wrapper {
            position: relative;
            padding-bottom: 56.25%; /* 16:9 Aspect Ratio */
            height: 0;
            overflow: hidden;
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

        .video-card-content {
            padding: 1.5rem;
            color: white;
        }

        .video-card-title {
            font-family: var(--font-heading);
            font-size: 1.2rem;
            margin-bottom: 0.5rem;
        }

        /* Subscription Section */
        .subscription-section {
            background: var(--tuko-red);
            color: white;
            padding: 4rem 2rem;
            text-align: center;
            margin: 4rem 0;
            position: relative;
            overflow: hidden;
        }

        .subscription-section::before {
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

        .subscription-content {
            position: relative;
            z-index: 1;
            max-width: 600px;
            margin: 0 auto;
        }

        .subscription-section h2 {
            font-family: var(--font-display);
            font-size: 2.5rem;
            margin-bottom: 1rem;
        }

        .subscribe-form {
            display: flex;
            gap: 0;
            margin-top: 2rem;
            box-shadow: 0 10px 30px rgba(0,0,0,0.3);
        }

        .subscribe-form input {
            flex: 1;
            padding: 1rem 1.5rem;
            border: none;
            font-family: var(--font-body);
            font-size: 1rem;
        }

        .subscribe-form button {
            padding: 1rem 2rem;
            background: var(--primary-color);
            color: white;
            border: none;
            font-family: var(--font-accent);
            font-weight: 700;
            text-transform: uppercase;
            letter-spacing: 1px;
            cursor: pointer;
            transition: background 0.3s;
        }

        .subscribe-form button:hover {
            background: #000;
        }

        /* Footer */
        footer {
            background: var(--primary-color);
            color: white;
            padding: 4rem 1rem 2rem;
            text-align: center;
        }

        .footer-content {
            max-width: 1200px;
            margin: 0 auto;
        }

        .footer-tagline {
            font-family: var(--font-display);
            font-size: 2.5rem;
            color: var(--accent-color);
            margin-bottom: 1rem;
        }

        .footer-links {
            display: flex;
            justify-content: center;
            gap: 2rem;
            margin: 2rem 0;
            flex-wrap: wrap;
        }

        .footer-links a {
            color: white;
            text-decoration: none;
            font-family: var(--font-accent);
            font-size: 0.8rem;
            text-transform: uppercase;
            letter-spacing: 1px;
            transition: color 0.3s;
        }

        .footer-links a:hover {
            color: var(--accent-color);
        }

        .copyright {
            font-family: var(--font-accent);
            font-size: 0.75rem;
            color: #666;
            text-transform: uppercase;
            letter-spacing: 2px;
            margin-top: 2rem;
            padding-top: 2rem;
            border-top: 1px solid #333;
        }

        /* Responsive */
        @media (max-width: 968px) {
            .featured-story {
                grid-template-columns: 1fr;
            }

            .two-column {
                grid-template-columns: 1fr;
            }

            .sidebar {
                position: static;
            }

            .nav-menu {
                gap: 0;
            }

            .nav-menu a {
                padding: 1rem;
                font-size: 0.75rem;
            }
        }

        @media (max-width: 600px) {
            .stories-grid {
                grid-template-columns: 1fr;
            }

            .video-grid {
                grid-template-columns: 1fr;
            }

            .subscribe-form {
                flex-direction: column;
            }
        }
    </style>
</head>
<body>

    <!-- TUKO Style Top Bar -->
    <div class="top-bar">
        <div class="top-bar-content">
            <div class="breaking-news">
                <span class="breaking-label">Breaking</span>
                <span class="ticker-text">Sauti Sol announces reunion concert dates for 2026!</span>
            </div>
            <div class="date-weather">
                <span id="current-date"></span>
            </div>
        </div>
    </div>

    <!-- Main Header -->
    <header class="main-header">
        <div class="header-content">
            <div class="logo-section">
                <img src="./mic_cheque_logo.png" alt="MIC CHEQUE Logo">
                <div class="site-branding">
                    <h1>MIC CHEQUE</h1>
                    <span>Entertainment & Stories</span>
                </div>
            </div>
            <div class="social-icons">
                <!-- Social icons can be added here -->
            </div>
        </div>
    </header>

    <!-- Navigation -->
    <nav class="main-nav">
        <div class="nav-content">
            <ul class="nav-menu">
                <li><a href="#" class="active">Home</a></li>
                <li><a href="#">Entertainment</a></li>
                <li><a href="#">Celebrity News</a></li>
                <li><a href="#">Music</a></li>
                <li><a href="#">Movies</a></li>
                <li><a href="#">Events</a></li>
                <li><a href="#">Culture</a></li>
                <li><a href="#">Lifestyle</a></li>
            </ul>
        </div>
    </nav>

    <main class="container">

        <!-- Featured Story with Fixed Video -->
        <section class="featured-story">
            <div class="featured-media">
                <!-- FIXED VIDEO: Multiple formats, poster image, proper attributes -->
                <video 
                    id="featured-video"
                    autoplay 
                    muted 
                    loop 
                    playsinline
                    preload="auto"
                    poster="./matatu_story_4.jpg"
                    style="width:100%; height:100%; object-fit:cover;">
                    <source src="./matatu_culture_video.mp4" type="video/mp4">
                    <source src="./matatu_culture_video.webm" type="video/webm">
                    <!-- Fallback message -->
                    Your browser does not support the video tag.
                </video>
                <div class="video-overlay">
                    <div class="play-button" onclick="toggleVideo('featured-video')"></div>
                    <span class="category-tag">Featured Video</span>
                </div>
            </div>
            <div class="featured-content">
                <span class="category-tag">Entertainment</span>
                <h2 class="featured-title">Nairobi Matatu Culture: The Moving Art That Never Sleeps</h2>
                <p class="featured-excerpt">
                    In the fast-moving urban life of Kenya, few things define daily experience more vividly than the matatu system. 
                    These minibuses are not just transport—they are a living cultural phenomenon blending art, music, economy, 
                    and street identity into one moving ecosystem.
                </p>
                <div class="meta-info">
                    <span>📅 April 17, 2026</span>
                    <span>⏱️ 5 min read</span>
                    <span>👁️ 12.5K views</span>
                </div>
            </div>
        </section>

        <!-- Latest Entertainment Stories -->
        <div class="section-header">
            <h3 class="section-title">Latest Entertainment</h3>
            <a href="#" class="view-all">View All →</a>
        </div>

        <div class="stories-grid">
            <!-- Story 1 -->
            <article class="story-card" onclick="openStory('story1')">
                <div class="story-image">
                    <img src="./tech_story_1.jpg" alt="Entertainment News">
                    <span class="video-badge">VIDEO</span>
                </div>
                <div class="story-content">
                    <div class="story-category">Celebrity News</div>
                    <h3 class="story-title">Diamond Platnumz Drops New Album Featuring International Artists</h3>
                    <p class="story-excerpt">
                        The Bongo Flava superstar surprised fans with a midnight release featuring collaborations 
                        with artists from Nigeria, South Africa, and the US.
                    </p>
                    <div class="story-meta">
                        <span>2 hours ago</span>
                        <span>💬 234 comments</span>
                    </div>
                </div>
            </article>

            <!-- Story 2 -->
            <article class="story-card" onclick="openStory('story2')">
                <div class="story-image">
                    <img src="./tech_story_2.jpg" alt="Entertainment News">
                </div>
                <div class="story-content">
                    <div class="story-category">Movies</div>
                    <h3 class="story-title">Kenyan Film 'Nairobi Half Life' Sequel Announced for 2027</h3>
                    <p class="story-excerpt">
                        After years of speculation, the director confirms production will begin next year 
                        with original cast members returning to tell the next chapter.
                    </p>
                    <div class="story-meta">
                        <span>4 hours ago</span>
                        <span>💬 189 comments</span>
                    </div>
                </div>
            </article>

            <!-- Story 3 -->
            <article class="story-card" onclick="openStory('story3')">
                <div class="story-image">
                    <img src="./tech_story_3.jpg" alt="Entertainment News">
                    <span class="video-badge">EXCLUSIVE</span>
                </div>
                <div class="story-content">
                    <div class="story-category">Music</div>
                    <h3 class="story-title">Sauti Sol Members Launch Solo Projects: What Fans Need to Know</h3>
                    <p class="story-excerpt">
                        Each member reveals individual artistic directions while promising the group 
                        will reunite for special projects and tours in the future.
                    </p>
                    <div class="story-meta">
                        <span>6 hours ago</span>
                        <span>💬 567 comments</span>
                    </div>
                </div>
            </article>

            <!-- Story 4 -->
            <article class="story-card" onclick="openStory('story4')">
                <div class="story-image">
                    <img src="./matatu_story_1.jpg" alt="Entertainment News">
                </div>
                <div class="story-content">
                    <div class="story-category">Events</div>
                    <h3 class="story-title">Blankets & Wine Festival Returns with International Headliners</h3>
                    <p class="story-excerpt">
                        East Africa's premier lifestyle festival announces lineup featuring Grammy-nominated 
                        artists and top local performers for the December edition.
                    </p>
                    <div class="story-meta">
                        <span>8 hours ago</span>
                        <span>💬 123 comments</span>
                    </div>
                </div>
            </article>

            <!-- Story 5 -->
            <article class="story-card" onclick="openStory('story5')">
                <div class="story-image">
                    <img src="./matatu_story_2.jpg" alt="Entertainment News">
                    <span class="video-badge">TRENDING</span>
                </div>
                <div class="story-content">
                    <div class="story-category">Lifestyle</div>
                    <h3 class="story-title">Inside Nairobi's Underground Comedy Scene</h3>
                    <p class="story-excerpt">
                        We explore the rising stand-up comedy clubs in the city where new talent 
                        is challenging established names and reshaping Kenyan humor.
                    </p>
                    <div class="story-meta">
                        <span>12 hours ago</span>
                        <span>💬 89 comments</span>
                    </div>
                </div>
            </article>

            <!-- Story 6 -->
            <article class="story-card" onclick="openStory('story6')">
                <div class="story-image">
                    <img src="./matatu_story_3.jpg" alt="Entertainment News">
                </div>
                <div class="story-content">
                    <div class="story-category">Culture</div>
                    <h3 class="story-title">Gengetone Evolution: How the Sound is Going Global</h3>
                    <p class="story-excerpt">
                        From Nairobi estates to international streaming charts, Gengetone artists 
                        are redefining Kenyan music for a new generation.
                    </p>
                    <div class="story-meta">
                        <span>1 day ago</span>
                        <span>💬 445 comments</span>
                    </div>
                </div>
            </article>
        </div>

        <!-- Two Column Layout -->
        <div class="two-column">
            <div class="main-content">
                <div class="section-header">
                    <h3 class="section-title">More Stories</h3>
                </div>

                <!-- Additional Stories List -->
                <div class="stories-list">
                    <article class="story-card" style="display:flex; gap:1.5rem; margin-bottom:1.5rem;">
                        <div class="story-image" style="width:200px; height:150px; flex-shrink:0;">
                            <img src="./tech_story_4.jpg" alt="Story" style="width:100%; height:100%; object-fit:cover;">
                        </div>
                        <div class="story-content" style="flex:1; padding:0;">
                            <div class="story-category">Celebrity Gossip</div>
                            <h3 class="story-title">Eric Omondi Addresses Beef with Fellow Comedians</h3>
                            <p class="story-excerpt">The comedian sets the record straight on recent social media drama...</p>
                            <div class="story-meta">
                                <span>2 days ago</span>
                                <span>💬 892 comments</span>
                            </div>
                        </div>
                    </article>

                    <article class="story-card" style="display:flex; gap:1.5rem; margin-bottom:1.5rem;">
                        <div class="story-image" style="width:200px; height:150px; flex-shrink:0;">
                            <img src="./matatu_story_4.jpg" alt="Story" style="width:100%; height:100%; object-fit:cover;">
                        </div>
                        <div class="story-content" style="flex:1; padding:0;">
                            <div class="story-category">TV & Radio</div>
                            <h3 class="story-title">Popular Radio Presenter Joins New Station</h3>
                            <p class="story-excerpt">After 5 years at the previous network, the move shocks industry insiders...</p>
                            <div class="story-meta">
                                <span>2 days ago</span>
                                <span>💬 234 comments</span>
                            </div>
                        </div>
                    </article>
                </div>
            </div>

            <!-- Sidebar -->
            <aside class="sidebar">
                <div class="sidebar-widget">
                    <h4 class="widget-title">🔥 Trending Now</h4>
                    <ul class="trending-list">
                        <li class="trending-item">
                            <span class="trending-number">1</span>
                            <div class="trending-content">
                                <h4>Willy Paul New Controversy</h4>
                                <span>15K shares</span>
                            </div>
                        </li>
                        <li class="trending-item">
                            <span class="trending-number">2</span>
                            <div class="trending-content">
                                <h4>Bahati and Diana Split Rumors</h4>
                                <span>12K shares</span>
                            </div>
                        </li>
                        <li class="trending-item">
                            <span class="trending-number">3</span>
                            <div class="trending-content">
                                <h4>Kenya vs Nigeria Music Debate</h4>
                                <span>8K shares</span>
                            </div>
                        </li>
                        <li class="trending-item">
                            <span class="trending-number">4</span>
                            <div class="trending-content">
                                <h4>New Reality Show Announcement</h4>
                                <span>6K shares</span>
                            </div>
                        </li>
                        <li class="trending-item">
                            <span class="trending-number">5</span>
                            <div class="trending-content">
                                <h4>Award Show Nominees List</h4>
                                <span>5K shares</span>
                            </div>
                        </li>
                    </ul>
                </div>

                <div class="sidebar-widget">
                    <h4 class="widget-title">📧 Newsletter</h4>
                    <p style="font-size:0.9rem; color:#666; margin-bottom:1rem;">
                        Get the hottest entertainment news delivered to your inbox daily!
                    </p>
                    <form class="subscribe-form" style="flex-direction:column; gap:0.5rem;">
                        <input type="email" placeholder="Your email" style="border:1px solid #ddd; border-radius:4px;">
                        <button type="submit" style="border-radius:4px; background:var(--tuko-red);">Subscribe</button>
                    </form>
                </div>
            </aside>
        </div>

    </main>

    <!-- Video Section -->
    <section class="video-section">
        <div class="container">
            <div class="section-header">
                <h3 class="section-title">Must Watch Videos</h3>
                <a href="#" class="view-all" style="color:white;">View All →</a>
            </div>

            <div class="video-grid">
                <!-- Video 1 -->
                <div class="video-card">
                    <div class="video-wrapper">
                        <video 
                            id="video-1"
                            controls
                            preload="metadata"
                            poster="./matatu_story_1.jpg">
                            <source src="./matatu_culture_video.mp4" type="video/mp4">
                            Your browser does not support the video tag.
                        </video>
                    </div>
                    <div class="video-card-content">
                        <h4 class="video-card-title">Behind the Scenes: Matatu Art Creation</h4>
                        <p style="font-size:0.9rem; opacity:0.8;">Watch how Nairobi's iconic matatu art comes to life</p>
                    </div>
                </div>

                <!-- Video 2 -->
                <div class="video-card">
                    <div class="video-wrapper">
                        <video 
                            id="video-2"
                            controls
                            preload="metadata"
                            poster="./tech_story_1.jpg">
                            <source src="./matatu_culture_video.mp4" type="video/mp4">
                            Your browser does not support the video tag.
                        </video>
                    </div>
                    <div class="video-card-content">
                        <h4 class="video-card-title">Interview: Rising Star in Kenyan Music</h4>
                        <p style="font-size:0.9rem; opacity:0.8;">Exclusive conversation with the artist taking over charts</p>
                    </div>
                </div>

                <!-- Video 3 -->
                <div class="video-card">
                    <div class="video-wrapper">
                        <video 
                            id="video-3"
                            controls
                            preload="metadata"
                            poster="./matatu_story_2.jpg">
                            <source src="./matatu_culture_video.mp4" type="video/mp4">
                            Your browser does not support the video tag.
                        </video>
                    </div>
                    <div class="video-card-content">
                        <h4 class="video-card-title">Event Coverage: Nairobi Festival 2026</h4>
                        <p style="font-size:0.9rem; opacity:0.8;">Highlights from the biggest cultural celebration of the year</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Subscription Section -->
    <section class="subscription-section">
        <div class="subscription-content">
            <h2>Join the Mic Cheque Family</h2>
            <p>Get exclusive entertainment news, behind-the-scenes content, and VIP event access delivered straight to your inbox.</p>
            <form class="subscribe-form" onsubmit="event.preventDefault(); alert('Welcome to Mic Cheque! Check your email for confirmation.');">
                <input type="email" placeholder="Enter your email address" required>
                <button type="submit">Subscribe Now</button>
            </form>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="footer-content">
            <p class="footer-tagline">NIKO KADI JE WEWE?</p>
            <div class="footer-links">
                <a href="#">About Us</a>
                <a href="#">Contact</a>
                <a href="#">Advertise</a>
                <a href="#">Privacy Policy</a>
                <a href="#">Terms of Use</a>
                <a href="#">Careers</a>
            </div>
            <p class="copyright">&copy; 2026 MIC CHEQUE. ALL RIGHTS RESERVED.</p>
        </div>
    </footer>

    <!-- JavaScript for Video Handling and Interactivity -->
    <script>
        // Set current date
        document.getElementById('current-date').textContent = new Date().toLocaleDateString('en-US', { 
            weekday: 'long', 
            year: 'numeric', 
            month: 'long', 
            day: 'numeric' 
        });

        // Video Autoplay Fix - Ensure videos play properly
        document.addEventListener('DOMContentLoaded', function() {
            const videos = document.querySelectorAll('video[autoplay]');

            videos.forEach(function(video) {
                // Ensure muted for autoplay
                video.muted = true;

                // Attempt to play
                var playPromise = video.play();

                if (playPromise !== undefined) {
                    playPromise.then(function() {
                        console.log('Video autoplay started successfully');
                    }).catch(function(error) {
                        console.log('Autoplay prevented:', error);
                        // Show play button if autoplay fails
                        video.setAttribute('controls', '');
                    });
                }

                // Handle visibility change (pause when tab not active to save resources)
                document.addEventListener('visibilitychange', function() {
                    if (document.hidden) {
                        video.pause();
                    } else if (video.hasAttribute('autoplay')) {
                        video.play().catch(function(e) {
                            console.log('Resume play failed:', e);
                        });
                    }
                });
            });
        });

        // Toggle play/pause for featured video
        function toggleVideo(videoId) {
            const video = document.getElementById(videoId);
            if (video.paused) {
                video.play();
                video.setAttribute('controls', '');
            } else {
                video.pause();
            }
        }

        // Story click handler
        function openStory(storyId) {
            console.log('Opening story:', storyId);
            // In real implementation, this would navigate to story page
            // window.location.href = '/story/' + storyId;
        }

        // Breaking news ticker animation
        const tickerTexts = [
            "Sauti Sol announces reunion concert dates for 2026!",
            "Diamond Platnumz new album breaks streaming records!",
            "Kenyan film selected for Cannes Film Festival!",
            "Major artist collaboration announced for Blankets & Wine!"
        ];

        let tickerIndex = 0;
        setInterval(function() {
            tickerIndex = (tickerIndex + 1) % tickerTexts.length;
            document.querySelector('.ticker-text').style.opacity = '0';
            setTimeout(function() {
                document.querySelector('.ticker-text').textContent = tickerTexts[tickerIndex];
                document.querySelector('.ticker-text').style.opacity = '1';
            }, 300);
        }, 5000);
    </script>

</body>
</html>
