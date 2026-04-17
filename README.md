
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>MIC CHEQUE | Professional Storytelling</title>
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

        /* Main Header */
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

        /* Navigation */
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

        /* Container */
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

        /* Featured Story */
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

        .featured-media img,
        .featured-media video {
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

        /* Stories Grid */
        .stories-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(350px, 1fr));
            gap: 2rem;
            margin-bottom: 3rem;
        }

        .story-card {
            background: white;
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 3px 15px rgba(0,0,0,0.08);
            transition: transform 0.3s, box-shadow 0.3s;
        }

        .story-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 30px rgba(0,0,0,0.15);
        }

        .story-image {
            position: relative;
            height: 220px;
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
            font-size: 1.2rem;
            font-weight: 700;
            line-height: 1.3;
            margin-bottom: 0.75rem;
            color: var(--primary-color);
        }

        .story-excerpt {
            font-size: 0.9rem;
            color: #666;
            line-height: 1.5;
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

        /* Full Story Content */
        .full-story {
            background: white;
            padding: 3rem;
            border-radius: 8px;
            margin-bottom: 3rem;
            box-shadow: 0 3px 15px rgba(0,0,0,0.08);
        }

        .full-story-title {
            font-family: var(--font-heading);
            font-size: 2.5rem;
            font-weight: 900;
            line-height: 1.2;
            margin-bottom: 1.5rem;
            color: var(--primary-color);
            text-align: center;
        }

        .full-story-content {
            font-size: 1.1rem;
            line-height: 1.8;
            color: var(--text-color);
        }

        .full-story-content p {
            margin-bottom: 1.5rem;
            text-align: justify;
        }

        .full-story-content p::first-letter {
            float: left;
            font-size: 4rem;
            line-height: 0.8;
            font-weight: bold;
            margin-right: 15px;
            margin-top: 10px;
            font-family: var(--font-display);
            color: var(--accent-color);
        }

        .story-media {
            margin: 2rem 0;
            text-align: center;
        }

        .story-media img,
        .story-media video {
            max-width: 100%;
            height: auto;
            border-radius: 8px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.15);
        }

        /* Video Section */
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
            padding-bottom: 56.25%;
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

            .stories-grid {
                grid-template-columns: 1fr;
            }

            .full-story {
                padding: 2rem 1rem;
            }

            .full-story-title {
                font-size: 1.8rem;
            }

            .nav-menu a {
                padding: 1rem;
                font-size: 0.75rem;
            }
        }

        @media (max-width: 600px) {
            .subscribe-form {
                flex-direction: column;
            }
        }
    </style>
</head>
<body>

    <!-- Top Bar -->
    <div class="top-bar">
        <div class="top-bar-content">
            <div class="breaking-news">
                <span class="breaking-label">Breaking</span>
                <span class="ticker-text">Nairobi Tech Scene Hits Record Investment Numbers!</span>
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
                    <span>Professional Storytelling</span>
                </div>
            </div>
        </div>
    </header>

    <!-- Navigation -->
    <nav class="main-nav">
        <div class="nav-content">
            <ul class="nav-menu">
                <li><a href="#" class="active">Home</a></li>
                <li><a href="#tech">Technology</a></li>
                <li><a href="#culture">Culture</a></li>
                <li><a href="#innovation">Innovation</a></li>
                <li><a href="#lifestyle">Lifestyle</a></li>
                <li><a href="#video">Video</a></li>
                <li><a href="#about">About</a></li>
            </ul>
        </div>
    </nav>

    <main class="container">

        <!-- Featured Story: Nairobi Tech Hustle -->
        <section class="featured-story" id="tech">
            <div class="featured-media">
                <img src="./tech_story_1.jpg" alt="Nairobi Tech Innovation">
            </div>
            <div class="featured-content">
                <span class="category-tag">Technology</span>
                <h2 class="featured-title">Nairobi's Tech Hustle: From Small Rooms to Global Impact</h2>
                <p class="featured-excerpt">
                    In the modern heartbeat of Kenya, Nairobi has grown into one of Africa's most influential 
                    innovation centers. What once looked like a city focused mainly on trade and administration 
                    is now home to fast-growing startups and digital creators.
                </p>
                <div class="meta-info">
                    <span>📅 April 17, 2026</span>
                    <span>⏱️ 8 min read</span>
                    <span>👁️ 15.2K views</span>
                </div>
            </div>
        </section>

        <!-- Full Story 1: Nairobi Tech Hustle -->
        <article class="full-story">
            <h2 class="full-story-title">Nairobi's Tech Hustle: From Small Rooms to Global Impact</h2>

            <div class="full-story-content">
                <p>In the modern heartbeat of Kenya, Nairobi has grown into one of Africa's most influential innovation centers. What once looked like a city focused mainly on trade and administration is now home to fast-growing startups, digital creators, and software engineers shaping solutions for global markets.</p>

                <p>This transformation did not happen overnight. It started in small internet cafés, university dorm rooms, and cramped rented apartments where young people experimented with code, design, and online business ideas. Many had no formal funding, no advanced equipment, and limited mentorship. What they had was curiosity and persistence.</p>

                <div class="story-media">
                    <img src="./tech_story_1.jpg" alt="Nairobi Tech Innovation">
                </div>

                <p>Today, those early experiments have evolved into real companies. Fintech platforms are now handling payments across East Africa. Logistics startups are improving delivery systems for small businesses. Health-tech tools are helping patients in remote areas access medical advice without traveling long distances.</p>

                <p>A major driver of this growth is mobile technology. With widespread smartphone adoption and mobile money systems, developers have been able to build services that reach millions instantly. This has made Kenya one of the most advanced mobile-first economies in the world.</p>

                <div class="story-media">
                    <img src="./tech_story_2.jpg" alt="Mobile Technology in Kenya">
                </div>

                <p>However, the journey is still far from easy. Many startups struggle with funding gaps, especially at early stages. Others face infrastructure challenges such as inconsistent internet in certain areas or high operational costs. Competition is also intense, with hundreds of new ideas launched every year.</p>

                <div class="story-media">
                    <img src="./tech_story_3.jpg" alt="Startups in Nairobi">
                </div>

                <p>Despite these challenges, the energy remains strong. Incubators and innovation hubs continue to support young talent. Universities are producing more tech graduates than ever before. International investors are increasingly paying attention to Nairobi as a serious tech destination.</p>

                <p>What stands out most is the mindset shift. Young innovators are no longer waiting for jobs—they are building them. They are creating platforms that solve local problems while also competing globally. Nairobi is no longer just participating in the digital economy; it is actively shaping it.</p>

                <div class="story-media">
                    <img src="./tech_story_4.jpg" alt="Future of Nairobi Tech">
                </div>
            </div>
        </article>

        <!-- Section Header -->
        <div class="section-header">
            <h3 class="section-title">More Stories</h3>
        </div>

        <!-- Story Cards Grid -->
        <div class="stories-grid">
            <!-- Matatu Culture Card -->
            <article class="story-card" id="culture">
                <div class="story-image">
                    <img src="./matatu_story_1.jpg" alt="Matatu Graffiti Art">
                    <span class="video-badge">FEATURED</span>
                </div>
                <div class="story-content">
                    <div class="story-category">Culture</div>
                    <h3 class="story-title">Nairobi Matatu Culture: The Moving Art That Never Sleeps</h3>
                    <p class="story-excerpt">
                        In the fast-moving urban life of Kenya, few things define daily experience more vividly 
                        than the matatu system. These minibuses are not just transport—they are a living cultural 
                        phenomenon.
                    </p>
                    <div class="story-meta">
                        <span>April 17, 2026</span>
                        <span>⏱️ 6 min read</span>
                    </div>
                </div>
            </article>

            <!-- Additional Story Card -->
            <article class="story-card">
                <div class="story-image">
                    <img src="./matatu_story_2.jpg" alt="Matatu Interior">
                </div>
                <div class="story-content">
                    <div class="story-category">Lifestyle</div>
                    <h3 class="story-title">Inside Nairobi's Most Iconic Matatu Routes</h3>
                    <p class="story-excerpt">
                        From Rongai to Ngong, explore the routes that have become legends in Nairobi's 
                        public transport history and the stories behind them.
                    </p>
                    <div class="story-meta">
                        <span>April 16, 2026</span>
                        <span>⏱️ 4 min read</span>
                    </div>
                </div>
            </article>

            <!-- Tech Story Card -->
            <article class="story-card">
                <div class="story-image">
                    <img src="./tech_story_3.jpg" alt="Tech Hub">
                </div>
                <div class="story-content">
                    <div class="story-category">Innovation</div>
                    <h3 class="story-title">The Rise of Nairobi's Innovation Hubs</h3>
                    <p class="story-excerpt">
                        How iHub, Nailab, and other incubators are nurturing the next generation of 
                        African tech entrepreneurs and changing the startup landscape.
                    </p>
                    <div class="story-meta">
                        <span>April 15, 2026</span>
                        <span>⏱️ 5 min read</span>
                    </div>
                </div>
            </article>
        </div>

        <!-- Full Story 2: Matatu Culture -->
        <article class="full-story" id="culture">
            <h2 class="full-story-title">Nairobi Matatu Culture: The Moving Art That Never Sleeps</h2>

            <div class="full-story-content">
                <p>In the fast-moving urban life of Kenya, few things define daily experience more vividly than the matatu system. These minibuses are not just a transport network—they are a living cultural phenomenon that blends art, music, economy, and street identity into one moving ecosystem.</p>

                <p>Every matatu begins its identity long before it hits the road. Artists spend hours designing graffiti-style exteriors, often inspired by pop culture, local heroes, music icons, or social themes. Inside, the transformation continues with LED lights, high-powered sound systems, custom seats, and unique branding that makes each vehicle distinct.</p>

                <div class="story-media">
                    <img src="./matatu_story_1.jpg" alt="Matatu Graffiti Art">
                </div>

                <p>For passengers, stepping into a matatu is an experience of its own. Music fills the air, sometimes so loud it becomes part of the ride itself. Conductors call out destinations in fast, rhythmic chants that feel like performance poetry. Young people often see matatus as more than transport—they are social spaces where conversations, trends, and culture are exchanged.</p>

                <div class="story-media">
                    <img src="./matatu_story_2.jpg" alt="Matatu Interior Experience">
                </div>

                <p>Behind this creativity is a crucial transport system that keeps Nairobi moving. Every day, millions of people rely on matatus to travel to work, school, markets, and hospitals. Without them, the city's mobility would collapse under pressure.</p>

                <div class="story-media">
                    <img src="./matatu_story_3.jpg" alt="Nairobi Public Transport">
                </div>

                <p>But the system operates in a complex environment. Traffic congestion in Nairobi is among the most challenging in the region, often causing long delays during peak hours. Route competition between operators can be intense, with each sacco trying to dominate popular routes. Regulations also evolve frequently, affecting pricing, design, and operation standards.</p>

                <div class="story-media">
                    <img src="./matatu_story_4.jpg" alt="Matatu Route Competition">
                </div>

                <p>Despite these issues, matatu culture continues to evolve rather than disappear. New designs appear regularly, each trying to push boundaries in creativity and style. The culture has even influenced fashion, music, and digital content creation, becoming a symbol of urban expression.</p>

                <p>For outsiders, it may look chaotic. For locals, it is structured chaos with rhythm and identity. It represents survival, creativity, and movement all at once. Matatus are not just part of Nairobi—they are Nairobi in motion.</p>
            </div>
        </article>

    </main>

    <!-- Video Section with Fixed Video -->
    <section class="video-section" id="video">
        <div class="container">
            <div class="section-header">
                <h3 class="section-title">Must Watch: Matatu Culture in Motion</h3>
            </div>

            <div class="video-grid">
                <div class="video-card">
                    <div class="video-wrapper">
                        <video 
                            id="matatu-video"
                            controls
                            preload="metadata"
                            poster="./matatu_story_4.jpg">
                            <source src="./matatu_culture_video.mp4" type="video/mp4">
                            <source src="./matatu_culture_video.webm" type="video/webm">
                            Your browser does not support the video tag.
                        </video>
                    </div>
                    <div class="video-card-content">
                        <h4 class="video-card-title">The Art of the Matatu</h4>
                        <p style="font-size:0.9rem; opacity:0.8;">Experience Nairobi's moving art culture in action</p>
                    </div>
                </div>

                <div class="video-card">
                    <div class="video-wrapper">
                        <video 
                            controls
                            preload="metadata"
                            poster="./tech_story_1.jpg">
                            <source src="./matatu_culture_video.mp4" type="video/mp4">
                            Your browser does not support the video tag.
                        </video>
                    </div>
                    <div class="video-card-content">
                        <h4 class="video-card-title">Tech Innovation in Nairobi</h4>
                        <p style="font-size:0.9rem; opacity:0.8;">How startups are transforming the city</p>
                    </div>
                </div>

                <div class="video-card">
                    <div class="video-wrapper">
                        <video 
                            controls
                            preload="metadata"
                            poster="./matatu_story_2.jpg">
                            <source src="./matatu_culture_video.mp4" type="video/mp4">
                            Your browser does not support the video tag.
                        </video>
                    </div>
                    <div class="video-card-content">
                        <h4 class="video-card-title">Inside the Matatu Experience</h4>
                        <p style="font-size:0.9rem; opacity:0.8;">A passenger's journey through Nairobi</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Subscription Section -->
    <section class="subscription-section">
        <div class="subscription-content">
            <h2>Join the Mic Cheque Family</h2>
            <p>Get exclusive stories, behind-the-scenes content, and updates delivered straight to your inbox.</p>
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
            </div>
            <p class="copyright">&copy; 2026 MIC CHEQUE. ALL RIGHTS RESERVED.</p>
        </div>
    </footer>

    <!-- JavaScript -->
    <script>
        // Set current date
        document.getElementById('current-date').textContent = new Date().toLocaleDateString('en-US', { 
            weekday: 'long', 
            year: 'numeric', 
            month: 'long', 
            day: 'numeric' 
        });

        // Video autoplay handling
        document.addEventListener('DOMContentLoaded', function() {
            const videos = document.querySelectorAll('video[autoplay]');

            videos.forEach(function(video) {
                video.muted = true;
                var playPromise = video.play();

                if (playPromise !== undefined) {
                    playPromise.then(function() {
                        console.log('Video autoplay started');
                    }).catch(function(error) {
                        console.log('Autoplay prevented:', error);
                        video.setAttribute('controls', '');
                    });
                }
            });
        });

        // Breaking news ticker
        const tickerTexts = [
            "Nairobi Tech Scene Hits Record Investment Numbers!",
            "New Matatu Design Trends Taking Over the City!",
            "Kenyan Startup Raises $5M in Series A Funding!",
            "Matatu Art Exhibition Opens at National Museum!"
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
