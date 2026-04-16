<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>MIC CHEQUE | Professional Storytelling</title>
    <!-- Premium Classic & Modern Font Pairing -->
    <link href="https://fonts.googleapis.com/css2?family=Cinzel+Decorative:wght@400;700;900&family=Playfair+Display:ital,wght@0,400;0,700;0,900;1,400&family=Lora:ital,wght@0,400;0,700;1,400&family=Montserrat:wght@300;400;600&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary-color: #1a1a1a;
            --accent-color: #c5a059;
            --text-color: #e0e0e0;
            --bg-color: #0f0f0f;
            --card-bg: #1a1a1a;
            --font-heading: 'Playfair Display', serif;
            --font-display: 'Cinzel Decorative', serif;
            --font-body: 'Lora', serif;
            --font-accent: 'Montserrat', sans-serif;
        }

        body.no-scroll {
            overflow: hidden;
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
            line-height: 1.8;
            -webkit-font-smoothing: antialiased;
            overflow-x: hidden;
            transition: background-color 0.3s ease;
        }

        /* Introduction Overlay Styles */
        #intro-overlay {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: #000;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            z-index: 9999;
            transition: opacity 2s ease, visibility 2s;
            overflow: hidden;
        }

        /* Traveling Star Animation */
        .star {
            position: absolute;
            width: 2px;
            height: 2px;
            background: white;
            border-radius: 50%;
            box-shadow: 0 0 10px 2px white, 0 0 20px 5px var(--accent-color);
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%) scale(0);
            opacity: 0;
            z-index: 10000;
            animation: starTravel 6s forwards ease-in;
        }

        @keyframes starTravel {
            0% { transform: translate(-50%, -50%) scale(0); opacity: 0; }
            20% { opacity: 1; }
            80% { transform: translate(-50%, -50%) scale(50); opacity: 1; filter: blur(2px); }
            100% { transform: translate(-50%, -50%) scale(200); opacity: 0; }
        }

        .intro-content {
            text-align: center;
            opacity: 0;
            z-index: 10001;
            animation: logoReveal 4s 3s forwards ease-out;
        }

        .intro-logo {
            max-width: 300px;
            margin-bottom: 2rem;
            filter: drop-shadow(0 0 30px rgba(197, 160, 89, 0.6));
        }

        .intro-text {
            font-family: var(--font-display);
            color: var(--accent-color);
            font-size: 2.5rem;
            letter-spacing: 12px;
            text-transform: uppercase;
            text-shadow: 0 0 20px rgba(197, 160, 89, 0.8);
        }

        @keyframes logoReveal {
            0% { opacity: 0; transform: scale(0.9); filter: blur(10px); }
            100% { opacity: 1; transform: scale(1); filter: blur(0px); }
        }

        .fade-out {
            opacity: 0 !important;
            visibility: hidden !important;
        }

        /* Modern Navigation Bar */
        .top-nav {
            position: sticky;
            top: 0;
            background: rgba(15, 15, 15, 0.98);
            backdrop-filter: blur(10px);
            z-index: 1000;
            border-bottom: 1px solid #333;
            padding: 1rem 0;
        }

        .top-nav ul {
            list-style: none;
            display: flex;
            justify-content: center;
            gap: 3rem;
        }

        .top-nav a {
            text-decoration: none;
            color: var(--text-color);
            font-family: var(--font-accent);
            font-size: 0.7rem;
            font-weight: 600;
            text-transform: uppercase;
            letter-spacing: 2px;
            transition: color 0.3s;
        }

        .top-nav a:hover {
            color: var(--accent-color);
        }

        header {
            padding: 6rem 1rem 4rem;
            text-align: center;
            background: linear-gradient(to bottom, #0f0f0f, #1a1a1a);
        }

        .logo-container img {
            max-width: 400px;
            height: auto;
            margin-bottom: 2rem;
            filter: drop-shadow(0 10px 15px rgba(0,0,0,0.1));
        }

        h1.site-title {
            font-family: var(--font-display);
            font-size: clamp(3rem, 8vw, 5.5rem);
            font-weight: 900;
            color: var(--accent-color);
            letter-spacing: 6px;
            margin-bottom: 0.5rem;
            text-shadow: 2px 2px 0px rgba(0,0,0,0.5), 4px 4px 0px rgba(197, 160, 89, 0.2);
            text-transform: uppercase;
        }

        .site-tagline {
            font-family: var(--font-accent);
            text-transform: uppercase;
            font-size: 0.85rem;
            letter-spacing: 6px;
            color: var(--accent-color);
            font-weight: 600;
        }

        main {
            max-width: 1000px;
            margin: 0 auto;
            padding: 4rem 1.5rem;
        }

        /* Modern Story Layout */
        .post {
            background: #1a1a1a;
            padding: 4rem;
            border-radius: 8px;
            margin-bottom: 4rem;
            border: 1px solid #333;
        }

        .post-title {
            font-family: var(--font-heading);
            font-size: clamp(2.5rem, 5vw, 3.8rem);
            font-weight: 900;
            line-height: 1.1;
            margin-bottom: 2.5rem;
            color: var(--accent-color);
            text-shadow: 1px 1px 0px rgba(0,0,0,0.5), 2px 2px 0px rgba(197, 160, 89, 0.15);
            text-align: center;
        }

        .post-content {
            font-size: 1.2rem;
            text-align: justify;
            max-width: 800px;
            margin: 0 auto;
        }

        .post-content p {
            margin-bottom: 2rem;
        }

        .post-content p::first-letter {
            float: left;
            font-size: 4.5rem;
            line-height: 0.8;
            font-weight: bold;
            margin-right: 15px;
            margin-top: 10px;
            font-family: var(--font-display);
            color: var(--accent-color);
        }

        /* Distinct Professional Separator */
        .story-separator {
            padding: 6rem 0;
            text-align: center;
            position: relative;
        }

        .story-separator::before {
            content: "";
            position: absolute;
            top: 50%;
            left: 0;
            right: 0;
            height: 1px;
            background: linear-gradient(to right, transparent, #555, transparent);
            z-index: 1;
        }

        .separator-icon {
            background: var(--bg-color);
            padding: 0 2rem;
            position: relative;
            z-index: 2;
            display: inline-block;
            filter: brightness(1.2) drop-shadow(0 0 15px rgba(197, 160, 89, 0.5));
        }

        .separator-icon img {
            width: 60px;
            height: auto;
            opacity: 0.6;
        }

        /* Media styling */
        .post-media {
            margin: 4rem -4rem;
            text-align: center;
        }

        .post-media img, .post-media video {
            max-width: 100%;
            height: auto;
            box-shadow: 0 20px 40px rgba(0,0,0,0.15);
        }

        /* Subscription Section - Modernized */
        .subscription-section {
            background-color: var(--primary-color);
            color: white;
            padding: 6rem 2rem;
            text-align: center;
            margin-top: 4rem;
        }

        .subscription-section h2 {
            font-family: var(--font-display);
            font-size: 2.5rem;
            margin-bottom: 1.5rem;
            color: var(--accent-color);
        }

        .subscription-section p {
            font-family: var(--font-body);
            margin-bottom: 3rem;
            opacity: 0.8;
        }

        .subscribe-form {
            display: flex;
            justify-content: center;
            max-width: 500px;
            margin: 0 auto;
            box-shadow: 0 10px 30px rgba(0,0,0,0.3);
        }

        .subscribe-form input {
            flex: 1;
            padding: 1.2rem 1.5rem;
            border: none;
            font-family: var(--font-body);
            outline: none;
            border-radius: 4px 0 0 4px;
        }

        .subscribe-form button {
            padding: 1.2rem 2.5rem;
            background-color: var(--accent-color);
            color: var(--primary-color);
            border: none;
            font-family: var(--font-accent);
            text-transform: uppercase;
            font-size: 0.8rem;
            font-weight: 700;
            letter-spacing: 2px;
            cursor: pointer;
            transition: all 0.3s;
            border-radius: 0 4px 4px 0;
        }

        .subscribe-form button:hover {
            background-color: #d4b47a;
        }

        footer {
            padding: 6rem 1rem;
            text-align: center;
            background-color: #000;
            color: #fff;
        }

        .footer-tagline {
            font-family: var(--font-display);
            font-size: 2.2rem;
            letter-spacing: 4px;
            margin-bottom: 1.5rem;
            color: var(--accent-color);
        }

        .copyright {
            font-family: var(--font-accent);
            font-size: 0.7rem;
            text-transform: uppercase;
            letter-spacing: 4px;
            color: #444;
        }

        @media (max-width: 768px) {
            .post { padding: 2rem; }
            .post-media { margin: 2rem 0; }
            .subscribe-form { flex-direction: column; }
            .subscribe-form input, .subscribe-form button { border-radius: 4px; margin-bottom: 10px; }
        }
    </style>
</head>
<body>

    <!-- Introduction Overlay -->
    <div id="intro-overlay">
        <div class="star"></div>
        <div class="intro-content">
            <img src="./miccheque_logo.png" alt="MIC CHEQUE Logo" class="intro-logo">
            <div class="intro-text">Mic Cheque</div>
        </div>
    </div>

    <nav class="top-nav">
        <ul>
            <li><a href="#">Chronicles</a></li>
            <li><a href="#">The Vault</a></li>
            <li><a href="#">About</a></li>
            <li><a href="#">Contact</a></li>
        </ul>
    </nav>

    <header>
        <div class="logo-container">
            <img src="./miccheque_logo.png" alt="MIC CHEQUE Logo">
        </div>
        <h1 class="site-title">MIC CHEQUE</h1>
        <p class="site-tagline">The Art of the Untold Story</p>
    </header>

    <main>
        <!-- Story 1: Nairobi's Tech Hustle -->
        <article class="post">
            <h2 class="post-title">Nairobi’s Tech Hustle: From Small Rooms to Global Impact</h2>
            <div class="post-content">
                <p>In the modern heartbeat of Kenya, Nairobi has grown into one of Africa’s most influential innovation centers. What once looked like a city focused mainly on trade and administration is now home to fast-growing startups, digital creators, and software engineers shaping solutions for global markets.</p>
                <p>This transformation did not happen overnight. It started in small internet cafés, university dorm rooms, and cramped rented apartments where young people experimented with code, design, and online business ideas. Many had no formal funding, no advanced equipment, and limited mentorship. What they had was curiosity and persistence.</p>
                
                <div class="post-media">
                    <img src="./tech_story_1.jpg" alt="Nairobi Tech Innovation">
                </div>

                <p>Today, those early experiments have evolved into real companies. Fintech platforms are now handling payments across East Africa. Logistics startups are improving delivery systems for small businesses. Health-tech tools are helping patients in remote areas access medical advice without traveling long distances.</p>
                <p>A major driver of this growth is mobile technology. With widespread smartphone adoption and mobile money systems, developers have been able to build services that reach millions instantly. This has made Kenya one of the most advanced mobile-first economies in the world.</p>

                <div class="post-media">
                    <img src="./tech_story_2.jpg" alt="Mobile Technology in Kenya">
                </div>

                <p>However, the journey is still far from easy. Many startups struggle with funding gaps, especially at early stages. Others face infrastructure challenges such as inconsistent internet in certain areas or high operational costs. Competition is also intense, with hundreds of new ideas launched every year.</p>
                
                <div class="post-media">
                    <img src="./tech_story_3.jpg" alt="Startups in Nairobi">
                </div>

                <p>Despite these challenges, the energy remains strong. Incubators and innovation hubs continue to support young talent. Universities are producing more tech graduates than ever before. International investors are increasingly paying attention to Nairobi as a serious tech destination.</p>
                <p>What stands out most is the mindset shift. Young innovators are no longer waiting for jobs—they are building them. They are creating platforms that solve local problems while also competing globally. Nairobi is no longer just participating in the digital economy; it is actively shaping it.</p>
                
                <div class="post-media">
                    <img src="./tech_story_4.jpg" alt="Future of Nairobi Tech">
                </div>
            </div>
        </article>

        <!-- Distinct Professional Separator -->
        <div class="story-separator">
            <div class="separator-icon">
                <img src="./miccheque_logo.png" alt="Separator">
            </div>
        </div>

        <!-- Story 2: Nairobi Matatu Culture -->
        <article class="post">
            <h2 class="post-title">Nairobi Matatu Culture: The Moving Art That Never Sleeps</h2>
            <div class="post-content">
                <p>In the fast-moving urban life of Kenya, few things define daily experience more vividly than the matatu system. These minibuses are not just a transport network—they are a living cultural phenomenon that blends art, music, economy, and street identity into one moving ecosystem.</p>
                <p>Every matatu begins its identity long before it hits the road. Artists spend hours designing graffiti-style exteriors, often inspired by pop culture, local heroes, music icons, or social themes. Inside, the transformation continues with LED lights, high-powered sound systems, custom seats, and unique branding that makes each vehicle distinct.</p>
                
                <div class="post-media">
                    <img src="./matatu_story_1.jpg" alt="Matatu Graffiti Art">
                </div>

                <p>For passengers, stepping into a matatu is an experience of its own. Music fills the air, sometimes so loud it becomes part of the ride itself. Conductors call out destinations in fast, rhythmic chants that feel like performance poetry. Young people often see matatus as more than transport—they are social spaces where conversations, trends, and culture are exchanged.</p>
                
                <div class="post-media">
                    <img src="./matatu_story_2.jpg" alt="Matatu Interior Experience">
                </div>

                <p>Behind this creativity is a crucial transport system that keeps Nairobi moving. Every day, millions of people rely on matatus to travel to work, school, markets, and hospitals. Without them, the city’s mobility would collapse under pressure.</p>
                
                <div class="post-media">
                    <img src="./matatu_story_3.jpg" alt="Nairobi Public Transport">
                </div>

                <p>But the system operates in a complex environment. Traffic congestion in Nairobi is among the most challenging in the region, often causing long delays during peak hours. Route competition between operators can be intense, with each sacco trying to dominate popular routes. Regulations also evolve frequently, affecting pricing, design, and operation standards.</p>
                
                <div class="post-media">
                    <img src="./matatu_story_4.jpg" alt="Matatu Route Competition">
                </div>

                <p>Despite these issues, matatu culture continues to evolve rather than disappear. New designs appear regularly, each trying to push boundaries in creativity and style. The culture has even influenced fashion, music, and digital content creation, becoming a symbol of urban expression.</p>
                <p>For outsiders, it may look chaotic. For locals, it is structured chaos with rhythm and identity. It represents survival, creativity, and movement all at once. Matatus are not just part of Nairobi—they are Nairobi in motion.</p>
                
            </div>
        </article>
    </main>

    <section class="subscription-section">
        <h2>Join the Inner Circle</h2>
        <p>Receive our weekly chronicles directly in your inbox.</p>
        <form class="subscribe-form" onsubmit="event.preventDefault(); alert('Thank you for subscribing to MIC CHEQUE!');">
            <input type="email" placeholder="Your email address" required>
            <button type="submit">Subscribe</button>
        </form>
    </section>

    <footer>
        <p class="footer-tagline">NIKO KADI JE WEWE?</p>
        <p class="copyright">&copy; 2026 MIC CHEQUE. ALL RIGHTS RESERVED.</p>
    </footer>

    <!-- Script to handle Intro Fade Out and Scroll Control -->
    <script>
        window.addEventListener('DOMContentLoaded', (event) => {
            // Disable scrolling when page loads
            document.body.classList.add('no-scroll');
            
            // Wait for 10 seconds total before fading out the intro
            setTimeout(() => {
                const intro = document.getElementById('intro-overlay');
                intro.classList.add('fade-out');
                
                // Remove from DOM after fade animation is complete (2 seconds)
                setTimeout(() => {
                    intro.style.display = 'none';
                    // Re-enable scrolling after intro is gone
                    document.body.classList.remove('no-scroll');
                }, 2000);
            }, 10000); 
        });
    </script>

</body>
</html>
