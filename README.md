<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>MIC CHEQUE | Professional Storytelling</title>
    <link href="https://fonts.googleapis.com/css2?family=Cinzel+Decorative:wght@400;700;900&family=Playfair+Display:ital,wght@0,400;0,700;0,900;1,400&family=Lora:ital,wght@0,400;0,700;1,400&family=Montserrat:wght@300;400;600;800&display=swap" rel="stylesheet">
    <style>
        /* ===========================
           ROOT VARIABLES
        =========================== */
        :root {
            --primary-color: #1a1a1a;
            --accent-color: #c5a059;
            --text-color: #333333;
            --bg-color: #f0f0f0;
            --card-bg: #ffffff;
            --tuko-red: #e8001c;
            --tuko-dark: #1a1a2e;
            --tuko-yellow: #f5c518;
            --border-color: #e0e0e0;
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
            color: #ccc;
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
            gap: 1rem;
        }

        .top-left-links {
            display: flex;
            gap: 1.2rem;
            align-items: center;
        }

        .top-left-links a {
            color: #ccc;
            text-transform: uppercase;
            letter-spacing: 0.5px;
            transition: color 0.2s;
        }

        .top-left-links a:hover { color: white; }

        .top-right-info {
            display: flex;
            align-items: center;
            gap: 1.5rem;
        }

        .top-date {
            color: #aaa;
            font-size: 0.7rem;
        }

        .social-icons {
            display: flex;
            gap: 0.6rem;
        }

        .social-icons a {
            width: 24px;
            height: 24px;
            background: rgba(255,255,255,0.1);
            border-radius: 3px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 0.7rem;
            transition: background 0.2s;
        }

        .social-icons a:hover { background: var(--tuko-red); }

        /* ===========================
           BREAKING NEWS TICKER
        =========================== */
        .breaking-bar {
            background: white;
            border-bottom: 1px solid var(--border-color);
            padding: 0.5rem 0;
            overflow: hidden;
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
            letter-spacing: 1px;
            white-space: nowrap;
            animation: pulse 2s infinite;
            flex-shrink: 0;
        }

        @keyframes pulse {
            0%, 100% { opacity: 1; }
            50% { opacity: 0.75; }
        }

        .ticker-wrapper {
            overflow: hidden;
            flex: 1;
        }

        .ticker-text {
            font-family: var(--font-accent);
            font-size: 0.8rem;
            font-weight: 600;
            color: var(--primary-color);
            white-space: nowrap;
            transition: opacity 0.3s;
        }

        /* ===========================
           MAIN HEADER
        =========================== */
        .main-header {
            background: white;
            padding: 0.8rem 0;
            box-shadow: 0 2px 8px rgba(0,0,0,0.08);
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
            gap: 0.8rem;
        }

        .logo-wrap img {
            height: 48px;
            width: auto;
        }

        .site-name h1 {
            font-family: var(--font-display);
            font-size: 1.9rem;
            color: var(--primary-color);
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
            align-items: center;
            border: 2px solid var(--border-color);
            border-radius: 4px;
            overflow: hidden;
        }

        .header-search input {
            border: none;
            outline: none;
            padding: 0.5rem 1rem;
            font-family: var(--font-accent);
            font-size: 0.8rem;
            width: 220px;
        }

        .header-search button {
            background: var(--tuko-red);
            border: none;
            color: white;
            padding: 0.5rem 1rem;
            cursor: pointer;
            font-size: 0.9rem;
        }

        /* ===========================
           NAVIGATION
        =========================== */
        .main-nav {
            background: var(--primary-color);
        }

        .nav-inner {
            max-width: 1280px;
            margin: 0 auto;
            padding: 0 1rem;
            display: flex;
            align-items: center;
            justify-content: space-between;
        }

        .nav-menu {
            list-style: none;
            display: flex;
            overflow-x: auto;
            scrollbar-width: none;
        }

        .nav-menu::-webkit-scrollbar { display: none; }

        .nav-menu li { border-right: 1px solid #333; }

        .nav-menu a {
            display: block;
            padding: 0.85rem 1.2rem;
            color: white;
            font-family: var(--font-accent);
            font-size: 0.75rem;
            font-weight: 600;
            text-transform: uppercase;
            letter-spacing: 0.8px;
            transition: background 0.2s;
            white-space: nowrap;
        }

        .nav-menu a:hover,
        .nav-menu a.active {
            background: var(--tuko-red);
        }

        .nav-hamburger {
            display: none;
            color: white;
            font-size: 1.4rem;
            cursor: pointer;
            padding: 0.5rem;
        }

        /* ===========================
           PAGE LAYOUT (3-column)
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

        .main-content { min-width: 0; }

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
            letter-spacing: 2px;
            color: var(--primary-color);
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }

        .section-title::before {
            content: '';
            display: inline-block;
            width: 5px;
            height: 20px;
            background: var(--tuko-red);
        }

        .see-all {
            font-family: var(--font-accent);
            font-size: 0.7rem;
            font-weight: 700;
            color: var(--tuko-red);
            text-transform: uppercase;
            letter-spacing: 1px;
            border: 1px solid var(--tuko-red);
            padding: 0.2rem 0.6rem;
            transition: all 0.2s;
        }

        .see-all:hover {
            background: var(--tuko-red);
            color: white;
        }

        /* ===========================
           HERO / FEATURED STORY
        =========================== */
        .hero-section {
            display: grid;
            grid-template-columns: 1.5fr 1fr;
            gap: 1rem;
            margin-bottom: 1.5rem;
        }

        .hero-main {
            position: relative;
            border-radius: 6px;
            overflow: hidden;
            background: #111;
        }

        .hero-main img {
            width: 100%;
            height: 380px;
            object-fit: cover;
            opacity: 0.85;
            transition: opacity 0.3s;
        }

        .hero-main:hover img { opacity: 1; }

        .hero-overlay {
            position: absolute;
            bottom: 0;
            left: 0;
            right: 0;
            padding: 1.5rem;
            background: linear-gradient(to top, rgba(0,0,0,0.85) 0%, rgba(0,0,0,0.4) 60%, transparent 100%);
        }

        .hero-category {
            display: inline-block;
            background: var(--tuko-red);
            color: white;
            padding: 0.15rem 0.6rem;
            font-family: var(--font-accent);
            font-size: 0.65rem;
            font-weight: 700;
            text-transform: uppercase;
            letter-spacing: 1px;
            margin-bottom: 0.5rem;
        }

        .hero-title {
            font-family: var(--font-heading);
            font-size: 1.5rem;
            font-weight: 900;
            color: white;
            line-height: 1.25;
            margin-bottom: 0.5rem;
        }

        .hero-meta {
            display: flex;
            gap: 1rem;
            font-family: var(--font-accent);
            font-size: 0.68rem;
            color: rgba(255,255,255,0.75);
        }

        /* Hero side stack */
        .hero-side {
            display: flex;
            flex-direction: column;
            gap: 0.8rem;
        }

        .hero-side-card {
            display: flex;
            gap: 0.8rem;
            background: white;
            border-radius: 6px;
            overflow: hidden;
            box-shadow: 0 2px 8px rgba(0,0,0,0.06);
            transition: box-shadow 0.2s;
        }

        .hero-side-card:hover { box-shadow: 0 4px 16px rgba(0,0,0,0.12); }

        .hero-side-img {
            width: 110px;
            height: 85px;
            flex-shrink: 0;
            overflow: hidden;
            background: #ddd;
        }

        .hero-side-img img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.3s;
        }

        .hero-side-card:hover .hero-side-img img { transform: scale(1.05); }

        .hero-side-body {
            padding: 0.6rem 0.8rem 0.6rem 0;
            display: flex;
            flex-direction: column;
            justify-content: center;
        }

        .hero-side-cat {
            font-family: var(--font-accent);
            font-size: 0.6rem;
            font-weight: 700;
            color: var(--tuko-red);
            text-transform: uppercase;
            letter-spacing: 0.5px;
            margin-bottom: 0.3rem;
        }

        .hero-side-title {
            font-family: var(--font-heading);
            font-size: 0.88rem;
            font-weight: 700;
            line-height: 1.3;
            color: var(--primary-color);
        }

        .hero-side-date {
            font-family: var(--font-accent);
            font-size: 0.62rem;
            color: #999;
            margin-top: 0.3rem;
        }

        /* ===========================
           FULL STORY ARTICLE
        =========================== */
        .full-story-wrap {
            background: white;
            border-radius: 6px;
            padding: 2rem 2.5rem;
            margin-bottom: 1.5rem;
            box-shadow: 0 2px 10px rgba(0,0,0,0.06);
        }

        .full-story-header {
            border-bottom: 2px solid var(--border-color);
            padding-bottom: 1.2rem;
            margin-bottom: 1.5rem;
        }

        .full-story-cat {
            display: inline-block;
            background: var(--tuko-red);
            color: white;
            padding: 0.2rem 0.7rem;
            font-family: var(--font-accent);
            font-size: 0.68rem;
            font-weight: 700;
            text-transform: uppercase;
            letter-spacing: 1px;
            margin-bottom: 0.8rem;
        }

        .full-story-title {
            font-family: var(--font-heading);
            font-size: 2rem;
            font-weight: 900;
            line-height: 1.2;
            color: var(--primary-color);
            margin-bottom: 0.8rem;
        }

        .full-story-meta {
            display: flex;
            gap: 1.5rem;
            font-family: var(--font-accent);
            font-size: 0.72rem;
            color: #888;
            flex-wrap: wrap;
        }

        .full-story-meta span {
            display: flex;
            align-items: center;
            gap: 0.3rem;
        }

        .full-story-body {
            font-family: var(--font-body);
            font-size: 1.05rem;
            line-height: 1.85;
            color: #2a2a2a;
        }

        .full-story-body p {
            margin-bottom: 1.3rem;
        }

        .full-story-body p:first-child::first-letter {
            font-family: var(--font-heading);
            font-size: 3.5rem;
            font-weight: 900;
            float: left;
            line-height: 0.8;
            margin: 0.1em 0.1em 0 0;
            color: var(--tuko-red);
        }

        .story-media-block {
            margin: 1.5rem 0;
            border-radius: 6px;
            overflow: hidden;
        }

        .story-media-block img {
            width: 100%;
            height: 380px;
            object-fit: cover;
        }

        .story-media-block .img-placeholder {
            width: 100%;
            height: 380px;
            background: linear-gradient(135deg, #f0f0f0 25%, #e0e0e0 50%, #f0f0f0 75%);
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            border: 2px dashed #ccc;
            border-radius: 6px;
            color: #999;
            font-family: var(--font-accent);
            font-size: 0.85rem;
            gap: 0.5rem;
        }

        .story-media-block .img-placeholder .icon {
            font-size: 2.5rem;
            opacity: 0.4;
        }

        .img-caption {
            font-family: var(--font-accent);
            font-size: 0.72rem;
            color: #888;
            padding: 0.4rem 0;
            font-style: italic;
            border-bottom: 1px solid var(--border-color);
        }

        /* ===========================
           STORY CARDS GRID
        =========================== */
        .stories-grid-3 {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 1rem;
            margin-bottom: 1.5rem;
        }

        .stories-grid-2 {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 1rem;
            margin-bottom: 1.5rem;
        }

        .story-card {
            background: white;
            border-radius: 6px;
            overflow: hidden;
            box-shadow: 0 2px 8px rgba(0,0,0,0.06);
            transition: transform 0.25s, box-shadow 0.25s;
        }

        .story-card:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 24px rgba(0,0,0,0.12);
        }

        .card-img {
            position: relative;
            height: 190px;
            overflow: hidden;
            background: #e8e8e8;
        }

        .card-img img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.3s;
        }

        .story-card:hover .card-img img { transform: scale(1.04); }

        /* Placeholder for new story images */
        .card-img .img-placeholder-card {
            width: 100%;
            height: 100%;
            background: linear-gradient(135deg, #f5f5f5 0%, #e0e0e0 50%, #f5f5f5 100%);
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            color: #bbb;
            font-family: var(--font-accent);
            font-size: 0.72rem;
            gap: 0.4rem;
            border: 2px dashed #d0d0d0;
        }

        .card-img .img-placeholder-card .ph-icon {
            font-size: 2rem;
            opacity: 0.5;
        }

        .card-badge {
            position: absolute;
            top: 0.6rem;
            left: 0.6rem;
            background: var(--tuko-red);
            color: white;
            padding: 0.15rem 0.5rem;
            font-family: var(--font-accent);
            font-size: 0.6rem;
            font-weight: 700;
            text-transform: uppercase;
            letter-spacing: 0.5px;
            border-radius: 2px;
        }

        .card-badge.featured { background: var(--tuko-dark); }
        .card-badge.video { background: #222; }

        .card-body {
            padding: 1rem;
        }

        .card-category {
            font-family: var(--font-accent);
            font-size: 0.62rem;
            font-weight: 700;
            color: var(--tuko-red);
            text-transform: uppercase;
            letter-spacing: 0.5px;
            margin-bottom: 0.4rem;
        }

        .card-title {
            font-family: var(--font-heading);
            font-size: 0.95rem;
            font-weight: 700;
            line-height: 1.35;
            color: var(--primary-color);
            margin-bottom: 0.5rem;
        }

        .card-excerpt {
            font-family: var(--font-body);
            font-size: 0.82rem;
            color: #666;
            line-height: 1.5;
            margin-bottom: 0.6rem;
            display: -webkit-box;
            -webkit-line-clamp: 3;
            -webkit-box-orient: vertical;
            overflow: hidden;
        }

        .card-meta {
            display: flex;
            gap: 1rem;
            font-family: var(--font-accent);
            font-size: 0.62rem;
            color: #aaa;
        }

        /* ===========================
           HORIZONTAL LIST CARD
        =========================== */
        .list-card {
            display: flex;
            gap: 0.8rem;
            padding: 0.8rem 0;
            border-bottom: 1px solid var(--border-color);
            transition: background 0.2s;
        }

        .list-card:last-child { border-bottom: none; }
        .list-card:hover { background: #fafafa; }

        .list-card-num {
            font-family: var(--font-accent);
            font-size: 1.5rem;
            font-weight: 800;
            color: #e8e8e8;
            flex-shrink: 0;
            width: 30px;
            line-height: 1;
            padding-top: 0.2rem;
        }

        .list-card-img {
            width: 80px;
            height: 65px;
            flex-shrink: 0;
            overflow: hidden;
            border-radius: 4px;
            background: #e0e0e0;
        }

        .list-card-img img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        .list-card-body { flex: 1; }

        .list-card-cat {
            font-family: var(--font-accent);
            font-size: 0.6rem;
            font-weight: 700;
            color: var(--tuko-red);
            text-transform: uppercase;
            margin-bottom: 0.2rem;
        }

        .list-card-title {
            font-family: var(--font-heading);
            font-size: 0.85rem;
            font-weight: 700;
            line-height: 1.3;
            color: var(--primary-color);
        }

        .list-card-date {
            font-family: var(--font-accent);
            font-size: 0.6rem;
            color: #aaa;
            margin-top: 0.25rem;
        }

        /* ===========================
           SIDEBAR
        =========================== */
        .sidebar { position: relative; }

        .sidebar-widget {
            background: white;
            border-radius: 6px;
            padding: 1.2rem;
            margin-bottom: 1.5rem;
            box-shadow: 0 2px 8px rgba(0,0,0,0.06);
        }

        .widget-title {
            font-family: var(--font-accent);
            font-size: 0.85rem;
            font-weight: 800;
            text-transform: uppercase;
            letter-spacing: 1.5px;
            color: var(--primary-color);
            padding-bottom: 0.6rem;
            border-bottom: 3px solid var(--tuko-red);
            margin-bottom: 1rem;
            display: flex;
            align-items: center;
            gap: 0.4rem;
        }

        .widget-title::before {
            content: '';
            display: inline-block;
            width: 4px;
            height: 16px;
            background: var(--tuko-red);
        }

        /* Trending list */
        .trending-item {
            display: flex;
            gap: 0.7rem;
            padding: 0.7rem 0;
            border-bottom: 1px solid #f0f0f0;
            cursor: pointer;
            transition: background 0.2s;
        }

        .trending-item:last-child { border-bottom: none; }
        .trending-item:hover { background: #fafafa; margin: 0 -1.2rem; padding-left: 1.2rem; padding-right: 1.2rem; }

        .trending-num {
            font-family: var(--font-accent);
            font-size: 1.2rem;
            font-weight: 800;
            color: #e0e0e0;
            flex-shrink: 0;
            width: 24px;
        }

        .trending-img {
            width: 70px;
            height: 55px;
            flex-shrink: 0;
            overflow: hidden;
            border-radius: 3px;
            background: #e8e8e8;
        }

        .trending-img img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        .trending-body { flex: 1; }

        .trending-title {
            font-family: var(--font-heading);
            font-size: 0.8rem;
            font-weight: 700;
            line-height: 1.3;
            color: var(--primary-color);
        }

        .trending-cat {
            font-family: var(--font-accent);
            font-size: 0.58rem;
            font-weight: 700;
            color: var(--tuko-red);
            text-transform: uppercase;
            margin-top: 0.2rem;
        }

        /* Newsletter widget */
        .newsletter-widget {
            background: var(--tuko-dark);
            color: white;
            border-radius: 6px;
            padding: 1.5rem;
            margin-bottom: 1.5rem;
            text-align: center;
        }

        .newsletter-widget h4 {
            font-family: var(--font-display);
            font-size: 1.1rem;
            color: var(--accent-color);
            margin-bottom: 0.5rem;
        }

        .newsletter-widget p {
            font-family: var(--font-accent);
            font-size: 0.75rem;
            color: #aaa;
            margin-bottom: 1rem;
            line-height: 1.5;
        }

        .newsletter-form input {
            width: 100%;
            padding: 0.6rem 0.8rem;
            border: none;
            border-radius: 3px;
            font-family: var(--font-accent);
            font-size: 0.8rem;
            margin-bottom: 0.5rem;
        }

        .newsletter-form button {
            width: 100%;
            padding: 0.6rem;
            background: var(--tuko-red);
            color: white;
            border: none;
            border-radius: 3px;
            font-family: var(--font-accent);
            font-size: 0.78rem;
            font-weight: 700;
            text-transform: uppercase;
            letter-spacing: 1px;
            cursor: pointer;
            transition: background 0.2s;
        }

        .newsletter-form button:hover { background: #c0001a; }

        /* Tags cloud */
        .tags-cloud {
            display: flex;
            flex-wrap: wrap;
            gap: 0.5rem;
        }

        .tag-pill {
            background: #f5f5f5;
            border: 1px solid var(--border-color);
            padding: 0.25rem 0.7rem;
            font-family: var(--font-accent);
            font-size: 0.68rem;
            color: #555;
            border-radius: 3px;
            cursor: pointer;
            transition: all 0.2s;
        }

        .tag-pill:hover {
            background: var(--tuko-red);
            color: white;
            border-color: var(--tuko-red);
        }

        /* ===========================
           VIDEO SECTION
        =========================== */
        .video-section {
            background: var(--tuko-dark);
            padding: 2rem 0;
            margin: 1.5rem 0;
        }

        .video-section-inner {
            max-width: 1280px;
            margin: 0 auto;
            padding: 0 1rem;
        }

        .video-section .section-header {
            border-bottom-color: var(--accent-color);
        }

        .video-section .section-title {
            color: white;
        }

        .video-section .section-title::before {
            background: var(--accent-color);
        }

        .video-grid {
            display: grid;
            grid-template-columns: 1.8fr 1fr 1fr;
            gap: 1rem;
        }

        .video-card {
            border-radius: 6px;
            overflow: hidden;
            background: #111;
        }

        .video-card.main-video { grid-row: span 1; }

        .video-wrapper {
            position: relative;
            padding-bottom: 56.25%;
            height: 0;
            overflow: hidden;
        }

        .video-wrapper video {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        .video-card-info {
            padding: 0.8rem 1rem;
            background: #1a1a1a;
        }

        .video-card-title {
            font-family: var(--font-heading);
            font-size: 0.9rem;
            color: white;
            margin-bottom: 0.3rem;
        }

        .video-card-desc {
            font-family: var(--font-accent);
            font-size: 0.7rem;
            color: #888;
        }

        /* ===========================
           NEW STORY PLACEHOLDER SECTION
        =========================== */
        .new-stories-section {
            background: white;
            border-radius: 6px;
            padding: 1.5rem;
            margin-bottom: 1.5rem;
            box-shadow: 0 2px 8px rgba(0,0,0,0.06);
            border: 2px dashed #d0d0d0;
        }

        .new-story-placeholder {
            background: #fafafa;
            border: 2px dashed #ddd;
            border-radius: 6px;
            padding: 1.5rem;
            margin-bottom: 1rem;
            display: grid;
            grid-template-columns: 280px 1fr;
            gap: 1.5rem;
            align-items: start;
        }

        .new-story-placeholder:last-child { margin-bottom: 0; }

        .new-story-img-slot {
            height: 200px;
            background: linear-gradient(135deg, #f0f0f0 0%, #e0e0e0 50%, #f0f0f0 100%);
            border: 2px dashed #ccc;
            border-radius: 4px;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            color: #bbb;
            font-family: var(--font-accent);
            font-size: 0.72rem;
            gap: 0.5rem;
            text-align: center;
        }

        .new-story-img-slot .ph-icon { font-size: 2.5rem; opacity: 0.4; }

        .new-story-img-slot code {
            background: #e8e8e8;
            padding: 0.2rem 0.5rem;
            border-radius: 3px;
            font-size: 0.68rem;
            color: #666;
            font-family: monospace;
        }

        .new-story-content-slot h4 {
            font-family: var(--font-heading);
            font-size: 1.2rem;
            color: #bbb;
            margin-bottom: 0.5rem;
        }

        .new-story-content-slot p {
            font-family: var(--font-body);
            font-size: 0.85rem;
            color: #ccc;
            line-height: 1.5;
        }

        .new-story-label {
            display: inline-block;
            background: #e8e8e8;
            color: #999;
            padding: 0.2rem 0.6rem;
            font-family: var(--font-accent);
            font-size: 0.65rem;
            font-weight: 700;
            text-transform: uppercase;
            letter-spacing: 1px;
            margin-bottom: 0.5rem;
            border-radius: 3px;
        }

        /* ===========================
           SUBSCRIPTION SECTION
        =========================== */
        .subscription-section {
            background: var(--tuko-red);
            color: white;
            padding: 3rem 1rem;
            text-align: center;
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
                rgba(255,255,255,0.04) 10px,
                rgba(255,255,255,0.04) 20px
            );
            animation: slide 20s linear infinite;
        }

        @keyframes slide {
            0% { transform: translate(0, 0); }
            100% { transform: translate(50px, 50px); }
        }

        .subscription-inner {
            position: relative;
            z-index: 1;
            max-width: 560px;
            margin: 0 auto;
        }

        .subscription-inner h2 {
            font-family: var(--font-display);
            font-size: 2rem;
            margin-bottom: 0.5rem;
        }

        .subscription-inner p {
            font-family: var(--font-accent);
            font-size: 0.85rem;
            opacity: 0.85;
            margin-bottom: 1.5rem;
        }

        .subscribe-form {
            display: flex;
            box-shadow: 0 8px 24px rgba(0,0,0,0.25);
        }

        .subscribe-form input {
            flex: 1;
            padding: 0.9rem 1.2rem;
            border: none;
            font-family: var(--font-body);
            font-size: 0.9rem;
            outline: none;
        }

        .subscribe-form button {
            padding: 0.9rem 1.5rem;
            background: var(--primary-color);
            color: white;
            border: none;
            font-family: var(--font-accent);
            font-weight: 700;
            font-size: 0.8rem;
            text-transform: uppercase;
            letter-spacing: 1px;
            cursor: pointer;
            transition: background 0.2s;
            white-space: nowrap;
        }

        .subscribe-form button:hover { background: #000; }

        /* ===========================
           FOOTER
        =========================== */
        footer {
            background: var(--primary-color);
            color: white;
            padding: 3rem 1rem 1.5rem;
        }

        .footer-inner {
            max-width: 1280px;
            margin: 0 auto;
        }

        .footer-grid {
            display: grid;
            grid-template-columns: 2fr 1fr 1fr 1fr;
            gap: 2rem;
            margin-bottom: 2rem;
        }

        .footer-brand h3 {
            font-family: var(--font-display);
            font-size: 1.4rem;
            color: var(--accent-color);
            margin-bottom: 0.5rem;
        }

        .footer-brand p {
            font-family: var(--font-accent);
            font-size: 0.75rem;
            color: #888;
            line-height: 1.6;
            margin-bottom: 1rem;
        }

        .footer-tagline {
            font-family: var(--font-display);
            font-size: 1rem;
            color: var(--accent-color);
            margin-top: 0.5rem;
        }

        .footer-col h4 {
            font-family: var(--font-accent);
            font-size: 0.8rem;
            font-weight: 800;
            text-transform: uppercase;
            letter-spacing: 1.5px;
            color: white;
            margin-bottom: 1rem;
            padding-bottom: 0.5rem;
            border-bottom: 2px solid var(--tuko-red);
        }

        .footer-col ul {
            list-style: none;
        }

        .footer-col ul li {
            margin-bottom: 0.5rem;
        }

        .footer-col ul li a {
            font-family: var(--font-accent);
            font-size: 0.75rem;
            color: #888;
            transition: color 0.2s;
        }

        .footer-col ul li a:hover { color: var(--accent-color); }

        .footer-bottom {
            border-top: 1px solid #2a2a2a;
            padding-top: 1.2rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
            gap: 0.5rem;
        }

        .copyright {
            font-family: var(--font-accent);
            font-size: 0.7rem;
            color: #555;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .footer-bottom-links {
            display: flex;
            gap: 1.5rem;
        }

        .footer-bottom-links a {
            font-family: var(--font-accent);
            font-size: 0.7rem;
            color: #555;
            text-transform: uppercase;
            letter-spacing: 0.5px;
            transition: color 0.2s;
        }

        .footer-bottom-links a:hover { color: var(--accent-color); }

        /* ===========================
           DIVIDER
        =========================== */
        .section-divider {
            height: 1px;
            background: var(--border-color);
            margin: 1.5rem 0;
        }

        /* ===========================
           RESPONSIVE
        =========================== */
        @media (max-width: 1024px) {
            .content-layout {
                grid-template-columns: 1fr;
            }

            .sidebar {
                display: grid;
                grid-template-columns: repeat(2, 1fr);
                gap: 1rem;
            }

            .video-grid {
                grid-template-columns: 1fr 1fr;
            }

            .footer-grid {
                grid-template-columns: 1fr 1fr;
            }
        }

        @media (max-width: 768px) {
            .hero-section {
                grid-template-columns: 1fr;
            }

            .hero-main img { height: 260px; }

            .stories-grid-3 {
                grid-template-columns: repeat(2, 1fr);
            }

            .new-story-placeholder {
                grid-template-columns: 1fr;
            }

            .video-grid {
                grid-template-columns: 1fr;
            }

            .footer-grid {
                grid-template-columns: 1fr;
            }

            .header-search { display: none; }

            .nav-hamburger { display: block; }

            .site-name h1 { font-size: 1.4rem; }

            .full-story-title { font-size: 1.5rem; }

            .full-story-wrap { padding: 1.2rem; }
        }

        @media (max-width: 480px) {
            .stories-grid-3,
            .stories-grid-2 {
                grid-template-columns: 1fr;
            }

            .subscribe-form { flex-direction: column; }

            .sidebar { grid-template-columns: 1fr; }

            .top-left-links { display: none; }
        }
    </style>
</head>
<body>

<!-- ===========================
     TOP UTILITY BAR
=========================== -->
<div class="top-utility-bar">
    <div class="top-utility-inner">
        <div class="top-left-links">
            <a href="#about">About</a>
            <a href="#contact">Contact</a>
            <a href="#advertise">Advertise</a>
        </div>
        <div class="top-right-info">
            <span class="top-date" id="current-date"></span>
            <div class="social-icons">
                <a href="#" title="Facebook">f</a>
                <a href="#" title="Twitter">𝕏</a>
                <a href="#" title="Instagram">ig</a>
                <a href="#" title="YouTube">▶</a>
            </div>
        </div>
    </div>
</div>

<!-- ===========================
     BREAKING NEWS TICKER
=========================== -->
<div class="breaking-bar">
    <div class="breaking-inner">
        <span class="breaking-label">Breaking</span>
        <div class="ticker-wrapper">
            <span class="ticker-text" id="ticker">Nairobi Tech Scene Hits Record Investment Numbers!</span>
        </div>
    </div>
</div>

<!-- ===========================
     MAIN HEADER
=========================== -->
<header class="main-header">
    <div class="header-inner">
        <div class="logo-wrap">
            <img src="./mic_cheque_logo.png" alt="MIC CHEQUE Logo" onerror="this.style.display='none'">
            <div class="site-name">
                <h1>MIC CHEQUE</h1>
                <span>Professional Storytelling</span>
            </div>
        </div>
        <div class="header-search">
            <input type="text" placeholder="Search stories...">
            <button>&#128269;</button>
        </div>
    </div>
</header>

<!-- ===========================
     NAVIGATION
=========================== -->
<nav class="main-nav">
    <div class="nav-inner">
        <ul class="nav-menu" id="nav-menu">
            <li><a href="#home" class="active">Home</a></li>
            <li><a href="#tech">Technology</a></li>
            <li><a href="#culture">Culture</a></li>
            <li><a href="#innovation">Innovation</a></li>
            <li><a href="#lifestyle">Lifestyle</a></li>
            <li><a href="#video">Video</a></li>
            <li><a href="#new-stories">New Stories</a></li>
            <li><a href="#about">About</a></li>
        </ul>
        <span class="nav-hamburger" onclick="toggleNav()">&#9776;</span>
    </div>
</nav>

<!-- ===========================
     PAGE WRAPPER
=========================== -->
<div class="page-wrapper" id="home">
    <div class="content-layout">

        <!-- ====== MAIN CONTENT ====== -->
        <main class="main-content">

            <!-- HERO SECTION -->
            <div class="section-header">
                <h2 class="section-title">Top Stories</h2>
                <a href="#" class="see-all">See All</a>
            </div>

            <div class="hero-section" id="tech">
                <!-- Hero Main Card -->
                <div class="hero-main">
                    <img src="./tech_story_1.jpg" alt="Nairobi Tech Innovation" onerror="this.src='data:image/svg+xml,<svg xmlns=%22http://www.w3.org/2000/svg%22 width=%22800%22 height=%22400%22><rect fill=%22%231a1a2e%22 width=%22800%22 height=%22400%22/><text fill=%22%23c5a059%22 font-size=%2228%22 x=%22400%22 y=%22200%22 text-anchor=%22middle%22>tech_story_1.jpg</text></svg>'">
                    <div class="hero-overlay">
                        <span class="hero-category">Technology</span>
                        <h2 class="hero-title">Nairobi's Tech Hustle: From Small Rooms to Global Impact</h2>
                        <div class="hero-meta">
                            <span>&#128197; April 17, 2026</span>
                            <span>&#9200; 8 min read</span>
                            <span>&#128065; 15.2K views</span>
                        </div>
                    </div>
                </div>

                <!-- Hero Side Stack -->
                <div class="hero-side">
                    <div class="hero-side-card">
                        <div class="hero-side-img">
                            <img src="./matatu_story_1.jpg" alt="Matatu Culture" onerror="this.src='data:image/svg+xml,<svg xmlns=%22http://www.w3.org/2000/svg%22 width=%22200%22 height=%22120%22><rect fill=%22%23e0e0e0%22 width=%22200%22 height=%22120%22/><text fill=%22%23999%22 font-size=%2211%22 x=%22100%22 y=%2265%22 text-anchor=%22middle%22>matatu_story_1.jpg</text></svg>'">
                        </div>
                        <div class="hero-side-body">
                            <div class="hero-side-cat">Culture</div>
                            <div class="hero-side-title">Nairobi Matatu Culture: The Moving Art That Never Sleeps</div>
                            <div class="hero-side-date">&#128197; April 17, 2026 &nbsp;&#9200; 6 min</div>
                        </div>
                    </div>

                    <div class="hero-side-card">
                        <div class="hero-side-img">
                            <img src="./matatu_story_2.jpg" alt="Matatu Routes" onerror="this.src='data:image/svg+xml,<svg xmlns=%22http://www.w3.org/2000/svg%22 width=%22200%22 height=%22120%22><rect fill=%22%23e0e0e0%22 width=%22200%22 height=%22120%22/><text fill=%22%23999%22 font-size=%2211%22 x=%22100%22 y=%2265%22 text-anchor=%22middle%22>matatu_story_2.jpg</text></svg>'">
                        </div>
                        <div class="hero-side-body">
                            <div class="hero-side-cat">Lifestyle</div>
                            <div class="hero-side-title">Inside Nairobi's Most Iconic Matatu Routes</div>
                            <div class="hero-side-date">&#128197; April 16, 2026 &nbsp;&#9200; 4 min</div>
                        </div>
                    </div>

                    <div class="hero-side-card">
                        <div class="hero-side-img">
                            <img src="./tech_story_3.jpg" alt="Innovation Hubs" onerror="this.src='data:image/svg+xml,<svg xmlns=%22http://www.w3.org/2000/svg%22 width=%22200%22 height=%22120%22><rect fill=%22%23e0e0e0%22 width=%22200%22 height=%22120%22/><text fill=%22%23999%22 font-size=%2211%22 x=%22100%22 y=%2265%22 text-anchor=%22middle%22>tech_story_3.jpg</text></svg>'">
                        </div>
                        <div class="hero-side-body">
                            <div class="hero-side-cat">Innovation</div>
                            <div class="hero-side-title">The Rise of Nairobi's Innovation Hubs</div>
                            <div class="hero-side-date">&#128197; April 15, 2026 &nbsp;&#9200; 5 min</div>
                        </div>
                    </div>
                </div>
            </div>

            <!-- ============================
                 FULL STORY 1: NAIROBI TECH
            ============================ -->
            <div class="section-header">
                <h2 class="section-title">Featured Story</h2>
            </div>

            <article class="full-story-wrap">
                <div class="full-story-header">
                    <span class="full-story-cat">Technology</span>
                    <h2 class="full-story-title">Nairobi's Tech Hustle: From Small Rooms to Global Impact</h2>
                    <div class="full-story-meta">
                        <span>&#128197; April 17, 2026</span>
                        <span>&#9200; 8 min read</span>
                        <span>&#128065; 15,200 views</span>
                        <span>&#9997; MIC CHEQUE Staff</span>
                    </div>
                </div>

                <div class="full-story-body">
                    <p>In the modern heartbeat of Kenya, Nairobi has grown into one of Africa's most influential innovation centers. What once looked like a city focused mainly on trade and administration is now home to fast-growing startups, digital creators, and software engineers shaping solutions for global markets.</p>

                    <p>This transformation did not happen overnight. It started in small internet cafés, university dorm rooms, and cramped rented apartments where young people experimented with code, design, and online business ideas. Many had no formal funding, no advanced equipment, and limited mentorship. What they had was curiosity and persistence.</p>

                    <div class="story-media-block">
                        <img src="./tech_story_1.jpg" alt="Nairobi Tech Innovation" onerror="this.parentElement.innerHTML='<div class=\'img-placeholder\'><span class=\'icon\'>&#128247;</span><span>tech_story_1.jpg</span></div>'">
                        <p class="img-caption">Nairobi's tech ecosystem continues to attract global attention — Photo: MIC CHEQUE</p>
                    </div>

                    <p>Today, those early experiments have evolved into real companies. Fintech platforms are now handling payments across East Africa. Logistics startups are improving delivery systems for small businesses. Health-tech tools are helping patients in remote areas access medical advice without traveling long distances.</p>

                    <p>A major driver of this growth is mobile technology. With widespread smartphone adoption and mobile money systems, developers have been able to build services that reach millions instantly. This has made Kenya one of the most advanced mobile-first economies in the world.</p>

                    <div class="story-media-block">
                        <img src="./tech_story_2.jpg" alt="Mobile Technology in Kenya" onerror="this.parentElement.innerHTML='<div class=\'img-placeholder\'><span class=\'icon\'>&#128247;</span><span>tech_story_2.jpg</span></div>'">
                        <p class="img-caption">Mobile technology is the backbone of Kenya's digital economy — Photo: MIC CHEQUE</p>
                    </div>

                    <p>However, the journey is still far from easy. Many startups struggle with funding gaps, especially at early stages. Others face infrastructure challenges such as inconsistent internet in certain areas or high operational costs. Competition is also intense, with hundreds of new ideas launched every year.</p>

                    <div class="story-media-block">
                        <img src="./tech_story_3.jpg" alt="Startups in Nairobi" onerror="this.parentElement.innerHTML='<div class=\'img-placeholder\'><span class=\'icon\'>&#128247;</span><span>tech_story_3.jpg</span></div>'">
                        <p class="img-caption">Startup culture is thriving despite funding challenges — Photo: MIC CHEQUE</p>
                    </div>

                    <p>Despite these challenges, the energy remains strong. Incubators and innovation hubs continue to support young talent. Universities are producing more tech graduates than ever before. International investors are increasingly paying attention to Nairobi as a serious tech destination.</p>

                    <p>What stands out most is the mindset shift. Young innovators are no longer waiting for jobs — they are building them. They are creating platforms that solve local problems while also competing globally. Nairobi is no longer just participating in the digital economy; it is actively shaping it.</p>

                    <div class="story-media-block">
                        <img src="./tech_story_4.jpg" alt="Future of Nairobi Tech" onerror="this.parentElement.innerHTML='<div class=\'img-placeholder\'><span class=\'icon\'>&#128247;</span><span>tech_story_4.jpg</span></div>'">
                        <p class="img-caption">The future of Nairobi's tech scene looks brighter than ever — Photo: MIC CHEQUE</p>
                    </div>
                </div>
            </article>

            <!-- STORY CARDS SECTION -->
            <div class="section-header" id="culture">
                <h2 class="section-title">More Stories</h2>
                <a href="#" class="see-all">See All</a>
            </div>

            <div class="stories-grid-3">
                <!-- Matatu Culture Card -->
                <article class="story-card">
                    <div class="card-img">
                        <img src="./matatu_story_1.jpg" alt="Matatu Graffiti Art" onerror="this.parentElement.innerHTML='<div class=\'img-placeholder-card\'><span class=\'ph-icon\'>&#128247;</span><span>matatu_story_1.jpg</span></div>'">
                        <span class="card-badge featured">Featured</span>
                    </div>
                    <div class="card-body">
                        <div class="card-category">Culture</div>
                        <h3 class="card-title">Nairobi Matatu Culture: The Moving Art That Never Sleeps</h3>
                        <p class="card-excerpt">In the fast-moving urban life of Kenya, few things define daily experience more vividly than the matatu system. These minibuses are not just transport — they are a living cultural phenomenon.</p>
                        <div class="card-meta">
                            <span>&#128197; April 17, 2026</span>
                            <span>&#9200; 6 min</span>
                        </div>
                    </div>
                </article>

                <!-- Matatu Routes Card -->
                <article class="story-card">
                    <div class="card-img">
                        <img src="./matatu_story_2.jpg" alt="Matatu Interior" onerror="this.parentElement.innerHTML='<div class=\'img-placeholder-card\'><span class=\'ph-icon\'>&#128247;</span><span>matatu_story_2.jpg</span></div>'">
                    </div>
                    <div class="card-body">
                        <div class="card-category">Lifestyle</div>
                        <h3 class="card-title">Inside Nairobi's Most Iconic Matatu Routes</h3>
                        <p class="card-excerpt">From Rongai to Ngong, explore the routes that have become legends in Nairobi's public transport history and the stories behind them.</p>
                        <div class="card-meta">
                            <span>&#128197; April 16, 2026</span>
                            <span>&#9200; 4 min</span>
                        </div>
                    </div>
                </article>

                <!-- Innovation Hubs Card -->
                <article class="story-card" id="innovation">
                    <div class="card-img">
                        <img src="./tech_story_3.jpg" alt="Tech Hub" onerror="this.parentElement.innerHTML='<div class=\'img-placeholder-card\'><span class=\'ph-icon\'>&#128247;</span><span>tech_story_3.jpg</span></div>'">
                    </div>
                    <div class="card-body">
                        <div class="card-category">Innovation</div>
                        <h3 class="card-title">The Rise of Nairobi's Innovation Hubs</h3>
                        <p class="card-excerpt">How iHub, Nailab, and other incubators are nurturing the next generation of African tech entrepreneurs and changing the startup landscape.</p>
                        <div class="card-meta">
                            <span>&#128197; April 15, 2026</span>
                            <span>&#9200; 5 min</span>
                        </div>
                    </div>
                </article>
            </div>

            <!-- ============================
                 FULL STORY 2: MATATU CULTURE
            ============================ -->
            <div class="section-header">
                <h2 class="section-title">Deep Dive: Matatu Culture</h2>
            </div>

            <article class="full-story-wrap" id="matatu-full">
                <div class="full-story-header">
                    <span class="full-story-cat">Culture</span>
                    <h2 class="full-story-title">Nairobi Matatu Culture: The Moving Art That Never Sleeps</h2>
                    <div class="full-story-meta">
                        <span>&#128197; April 17, 2026</span>
                        <span>&#9200; 6 min read</span>
                        <span>&#9997; MIC CHEQUE Staff</span>
                    </div>
                </div>

                <div class="full-story-body">
                    <p>In the fast-moving urban life of Kenya, few things define daily experience more vividly than the matatu system. These minibuses are not just a transport network — they are a living cultural phenomenon that blends art, music, economy, and street identity into one moving ecosystem.</p>

                    <p>Every matatu begins its identity long before it hits the road. Artists spend hours designing graffiti-style exteriors, often inspired by pop culture, local heroes, music icons, or social themes. Inside, the transformation continues with LED lights, high-powered sound systems, custom seats, and unique branding that makes each vehicle distinct.</p>

                    <div class="story-media-block">
                        <img src="./matatu_story_1.jpg" alt="Matatu Graffiti Art" onerror="this.parentElement.innerHTML='<div class=\'img-placeholder\'><span class=\'icon\'>&#128247;</span><span>matatu_story_1.jpg</span></div>'">
                        <p class="img-caption">Matatu graffiti art is a statement of identity and culture — Photo: MIC CHEQUE</p>
                    </div>

                    <p>For passengers, stepping into a matatu is an experience of its own. Music fills the air, sometimes so loud it becomes part of the ride itself. Conductors call out destinations in fast, rhythmic chants that feel like performance poetry. Young people often see matatus as more than transport — they are social spaces where conversations, trends, and culture are exchanged.</p>

                    <div class="story-media-block">
                        <img src="./matatu_story_2.jpg" alt="Matatu Interior Experience" onerror="this.parentElement.innerHTML='<div class=\'img-placeholder\'><span class=\'icon\'>&#128247;</span><span>matatu_story_2.jpg</span></div>'">
                        <p class="img-caption">Inside a matatu — a sensory experience unlike any other — Photo: MIC CHEQUE</p>
                    </div>

                    <p>Behind this creativity is a crucial transport system that keeps Nairobi moving. Every day, millions of people rely on matatus to travel to work, school, markets, and hospitals. Without them, the city's mobility would collapse under pressure.</p>

                    <div class="story-media-block">
                        <img src="./matatu_story_3.jpg" alt="Nairobi Public Transport" onerror="this.parentElement.innerHTML='<div class=\'img-placeholder\'><span class=\'icon\'>&#128247;</span><span>matatu_story_3.jpg</span></div>'">
                        <p class="img-caption">Matatus are the lifeblood of Nairobi's public transport network — Photo: MIC CHEQUE</p>
                    </div>

                    <p>But the system operates in a complex environment. Traffic congestion in Nairobi is among the most challenging in the region, often causing long delays during peak hours. Route competition between operators can be intense, with each sacco trying to dominate popular routes. Regulations also evolve frequently, affecting pricing, design, and operation standards.</p>

                    <div class="story-media-block">
                        <img src="./matatu_story_4.jpg" alt="Matatu Route Competition" onerror="this.parentElement.innerHTML='<div class=\'img-placeholder\'><span class=\'icon\'>&#128247;</span><span>matatu_story_4.jpg</span></div>'">
                        <p class="img-caption">Competition on popular routes is fierce among matatu saccos — Photo: MIC CHEQUE</p>
                    </div>

                    <p>Despite these issues, matatu culture continues to evolve rather than disappear. New designs appear regularly, each trying to push boundaries in creativity and style. The culture has even influenced fashion, music, and digital content creation, becoming a symbol of urban expression.</p>

                    <p>For outsiders, it may look chaotic. For locals, it is structured chaos with rhythm and identity. It represents survival, creativity, and movement all at once. Matatus are not just part of Nairobi — they are Nairobi in motion.</p>
                </div>
            </article>

            <!-- ============================
                 NEW STORIES PLACEHOLDER SECTION
            ============================ -->
            <div class="section-header" id="new-stories">
                <h2 class="section-title">New Stories</h2>
                <span style="font-family:var(--font-accent);font-size:0.7rem;color:#aaa;font-style:italic;">Add your photos to the folder and update the src below</span>
            </div>

            <div class="new-stories-section">
                <p style="font-family:var(--font-accent);font-size:0.78rem;color:#aaa;margin-bottom:1.2rem;text-align:center;">
                    &#128193; Place your new story photos in the same folder as this HTML file, then replace the <code style="background:#f0f0f0;padding:0.1rem 0.4rem;border-radius:3px;">src</code> values below with your actual filenames.
                </p>

                <!-- NEW STORY SLOT 1 -->
                <div class="new-story-placeholder">
                    <div class="new-story-img-slot">
                        <span class="ph-icon">&#128247;</span>
                        <span>Add your photo here</span>
                        <code>src="./new_story_1.jpg"</code>
                    </div>
                    <div class="new-story-content-slot">
                        <span class="new-story-label">New Story 1</span>
                        <h4>Your Story Title Goes Here</h4>
                        <p>Replace this placeholder with your story content. Add your photo to the folder and update the image source code on the left to <strong>./your_photo_name.jpg</strong></p>
                        <br>
                        <p style="font-size:0.75rem;color:#bbb;">To add this story: copy one of the <code style="background:#f0f0f0;padding:0.1rem 0.3rem;border-radius:2px;font-size:0.7rem;color:#666;">story-card</code> or <code style="background:#f0f0f0;padding:0.1rem 0.3rem;border-radius:2px;font-size:0.7rem;color:#666;">full-story-wrap</code> blocks above and paste it here, then update the text and image src.</p>
                    </div>
                </div>

                <!-- NEW STORY SLOT 2 -->
                <div class="new-story-placeholder">
                    <div class="new-story-img-slot">
                        <span class="ph-icon">&#128247;</span>
                        <span>Add your photo here</span>
                        <code>src="./new_story_2.jpg"</code>
                    </div>
                    <div class="new-story-content-slot">
                        <span class="new-story-label">New Story 2</span>
                        <h4>Your Story Title Goes Here</h4>
                        <p>Replace this placeholder with your story content. Add your photo to the folder and update the image source code on the left to <strong>./your_photo_name.jpg</strong></p>
                    </div>
                </div>

                <!-- NEW STORY SLOT 3 -->
                <div class="new-story-placeholder">
                    <div class="new-story-img-slot">
                        <span class="ph-icon">&#128247;</span>
                        <span>Add your photo here</span>
                        <code>src="./new_story_3.jpg"</code>
                    </div>
                    <div class="new-story-content-slot">
                        <span class="new-story-label">New Story 3</span>
                        <h4>Your Story Title Goes Here</h4>
                        <p>Replace this placeholder with your story content. Add your photo to the folder and update the image source code on the left to <strong>./your_photo_name.jpg</strong></p>
                    </div>
                </div>
            </div>

        </main><!-- end .main-content -->

        <!-- ====== SIDEBAR ====== -->
        <aside class="sidebar">

            <!-- TRENDING WIDGET -->
            <div class="sidebar-widget">
                <h3 class="widget-title">Trending Now</h3>

                <div class="trending-item">
                    <span class="trending-num">1</span>
                    <div class="trending-img">
                        <img src="./tech_story_1.jpg" alt="Tech" onerror="this.src='data:image/svg+xml,<svg xmlns=%22http://www.w3.org/2000/svg%22 width=%22100%22 height=%22100%22><rect fill=%22%23e0e0e0%22 width=%22100%22 height=%22100%22/></svg>'">
                    </div>
                    <div class="trending-body">
                        <div class="trending-title">Nairobi's Tech Hustle: From Small Rooms to Global Impact</div>
                        <div class="trending-cat">Technology &bull; 15.2K views</div>
                    </div>
                </div>

                <div class="trending-item">
                    <span class="trending-num">2</span>
                    <div class="trending-img">
                        <img src="./matatu_story_1.jpg" alt="Matatu" onerror="this.src='data:image/svg+xml,<svg xmlns=%22http://www.w3.org/2000/svg%22 width=%22100%22 height=%22100%22><rect fill=%22%23e0e0e0%22 width=%22100%22 height=%22100%22/></svg>'">
                    </div>
                    <div class="trending-body">
                        <div class="trending-title">Nairobi Matatu Culture: The Moving Art That Never Sleeps</div>
                        <div class="trending-cat">Culture &bull; 9.8K views</div>
                    </div>
                </div>

                <div class="trending-item">
                    <span class="trending-num">3</span>
                    <div class="trending-img">
                        <img src="./matatu_story_2.jpg" alt="Routes" onerror="this.src='data:image/svg+xml,<svg xmlns=%22http://www.w3.org/2000/svg%22 width=%22100%22 height=%22100%22><rect fill=%22%23e0e0e0%22 width=%22100%22 height=%22100%22/></svg>'">
                    </div>
                    <div class="trending-body">
                        <div class="trending-title">Inside Nairobi's Most Iconic Matatu Routes</div>
                        <div class="trending-cat">Lifestyle &bull; 7.1K views</div>
                    </div>
                </div>

                <div class="trending-item">
                    <span class="trending-num">4</span>
                    <div class="trending-img">
                        <img src="./tech_story_3.jpg" alt="Hubs" onerror="this.src='data:image/svg+xml,<svg xmlns=%22http://www.w3.org/2000/svg%22 width=%22100%22 height=%22100%22><rect fill=%22%23e0e0e0%22 width=%22100%22 height=%22100%22/></svg>'">
                    </div>
                    <div class="trending-body">
                        <div class="trending-title">The Rise of Nairobi's Innovation Hubs</div>
                        <div class="trending-cat">Innovation &bull; 5.4K views</div>
                    </div>
                </div>

                <div class="trending-item">
                    <span class="trending-num">5</span>
                    <div class="trending-img">
                        <img src="./tech_story_2.jpg" alt="Mobile" onerror="this.src='data:image/svg+xml,<svg xmlns=%22http://www.w3.org/2000/svg%22 width=%22100%22 height=%22100%22><rect fill=%22%23e0e0e0%22 width=%22100%22 height=%22100%22/></svg>'">
                    </div>
                    <div class="trending-body">
                        <div class="trending-title">Mobile-First Kenya: How Smartphones Changed Everything</div>
                        <div class="trending-cat">Technology &bull; 4.2K views</div>
                    </div>
                </div>
            </div>

            <!-- NEWSLETTER WIDGET -->
            <div class="newsletter-widget">
                <h4>Join Mic Cheque</h4>
                <p>Get exclusive stories and updates delivered straight to your inbox.</p>
                <form class="newsletter-form" onsubmit="event.preventDefault(); alert('Welcome to Mic Cheque! Check your email.');">
                    <input type="email" placeholder="Your email address" required>
                    <button type="submit">Subscribe Now</button>
                </form>
            </div>

            <!-- TAGS WIDGET -->
            <div class="sidebar-widget">
                <h3 class="widget-title">Topics</h3>
                <div class="tags-cloud">
                    <span class="tag-pill">Technology</span>
                    <span class="tag-pill">Culture</span>
                    <span class="tag-pill">Innovation</span>
                    <span class="tag-pill">Lifestyle</span>
                    <span class="tag-pill">Nairobi</span>
                    <span class="tag-pill">Startups</span>
                    <span class="tag-pill">Matatu</span>
                    <span class="tag-pill">Fintech</span>
                    <span class="tag-pill">Art</span>
                    <span class="tag-pill">Transport</span>
                    <span class="tag-pill">Youth</span>
                    <span class="tag-pill">Business</span>
                </div>
            </div>

            <!-- LATEST STORIES LIST WIDGET -->
            <div class="sidebar-widget">
                <h3 class="widget-title">Latest</h3>

                <div class="list-card">
                    <div class="list-card-img">
                        <img src="./tech_story_4.jpg" alt="" onerror="this.src='data:image/svg+xml,<svg xmlns=%22http://www.w3.org/2000/svg%22 width=%22100%22 height=%22100%22><rect fill=%22%23e0e0e0%22 width=%22100%22 height=%22100%22/></svg>'">
                    </div>
                    <div class="list-card-body">
                        <div class="list-card-cat">Technology</div>
                        <div class="list-card-title">Nairobi's Tech Hustle: From Small Rooms to Global Impact</div>
                        <div class="list-card-date">April 17, 2026</div>
                    </div>
                </div>

                <div class="list-card">
                    <div class="list-card-img">
                        <img src="./matatu_story_3.jpg" alt="" onerror="this.src='data:image/svg+xml,<svg xmlns=%22http://www.w3.org/2000/svg%22 width=%22100%22 height=%22100%22><rect fill=%22%23e0e0e0%22 width=%22100%22 height=%22100%22/></svg>'">
                    </div>
                    <div class="list-card-body">
                        <div class="list-card-cat">Culture</div>
                        <div class="list-card-title">Nairobi Matatu Culture: The Moving Art That Never Sleeps</div>
                        <div class="list-card-date">April 17, 2026</div>
                    </div>
                </div>

                <div class="list-card">
                    <div class="list-card-img">
                        <img src="./matatu_story_2.jpg" alt="" onerror="this.src='data:image/svg+xml,<svg xmlns=%22http://www.w3.org/2000/svg%22 width=%22100%22 height=%22100%22><rect fill=%22%23e0e0e0%22 width=%22100%22 height=%22100%22/></svg>'">
                    </div>
                    <div class="list-card-body">
                        <div class="list-card-cat">Lifestyle</div>
                        <div class="list-card-title">Inside Nairobi's Most Iconic Matatu Routes</div>
                        <div class="list-card-date">April 16, 2026</div>
                    </div>
                </div>

                <div class="list-card">
                    <div class="list-card-img">
                        <img src="./tech_story_3.jpg" alt="" onerror="this.src='data:image/svg+xml,<svg xmlns=%22http://www.w3.org/2000/svg%22 width=%22100%22 height=%22100%22><rect fill=%22%23e0e0e0%22 width=%22100%22 height=%22100%22/></svg>'">
                    </div>
                    <div class="list-card-body">
                        <div class="list-card-cat">Innovation</div>
                        <div class="list-card-title">The Rise of Nairobi's Innovation Hubs</div>
                        <div class="list-card-date">April 15, 2026</div>
                    </div>
                </div>
            </div>

        </aside><!-- end .sidebar -->

    </div><!-- end .content-layout -->
</div><!-- end .page-wrapper -->

<!-- ===========================
     VIDEO SECTION
=========================== -->
<section class="video-section" id="video">
    <div class="video-section-inner">
        <div class="section-header">
            <h3 class="section-title">Must Watch: Matatu Culture in Motion</h3>
            <a href="#" class="see-all" style="color:var(--accent-color);border-color:var(--accent-color);">See All Videos</a>
        </div>

        <div class="video-grid">
            <div class="video-card main-video">
                <div class="video-wrapper">
                    <video controls preload="metadata" poster="./matatu_story_4.jpg">
                        <source src="./matatu_culture_video.mp4" type="video/mp4">
                        <source src="./matatu_culture_video.webm" type="video/webm">
                        Your browser does not support the video tag.
                    </video>
                </div>
                <div class="video-card-info">
                    <h4 class="video-card-title">The Art of the Matatu</h4>
                    <p class="video-card-desc">Experience Nairobi's moving art culture in action</p>
                </div>
            </div>

            <div class="video-card">
                <div class="video-wrapper">
                    <video controls preload="metadata" poster="./tech_story_1.jpg">
                        <source src="./matatu_culture_video.mp4" type="video/mp4">
                        Your browser does not support the video tag.
                    </video>
                </div>
                <div class="video-card-info">
                    <h4 class="video-card-title">Tech Innovation in Nairobi</h4>
                    <p class="video-card-desc">How startups are transforming the city</p>
                </div>
            </div>

            <div class="video-card">
                <div class="video-wrapper">
                    <video controls preload="metadata" poster="./matatu_story_2.jpg">
                        <source src="./matatu_culture_video.mp4" type="video/mp4">
                        Your browser does not support the video tag.
                    </video>
                </div>
                <div class="video-card-info">
                    <h4 class="video-card-title">Inside the Matatu Experience</h4>
                    <p class="video-card-desc">A passenger's journey through Nairobi</p>
                </div>
            </div>
        </div>
    </div>
</section>

<!-- ===========================
     SUBSCRIPTION SECTION
=========================== -->
<section class="subscription-section">
    <div class="subscription-inner">
        <h2>Join the Mic Cheque Family</h2>
        <p>Get exclusive stories, behind-the-scenes content, and updates delivered straight to your inbox.</p>
        <form class="subscribe-form" onsubmit="event.preventDefault(); alert('Welcome to Mic Cheque! Check your email for confirmation.');">
            <input type="email" placeholder="Enter your email address" required>
            <button type="submit">Subscribe Now</button>
        </form>
    </div>
</section>

<!-- ===========================
     FOOTER
=========================== -->
<footer id="about">
    <div class="footer-inner">
        <div class="footer-grid">
            <div class="footer-brand">
                <h3>MIC CHEQUE</h3>
                <p>Professional storytelling from the heart of Kenya. We cover technology, culture, innovation, and the stories that shape our world.</p>
                <div class="footer-tagline">NIKO KADI JE WEWE?</div>
            </div>

            <div class="footer-col">
                <h4>Sections</h4>
                <ul>
                    <li><a href="#tech">Technology</a></li>
                    <li><a href="#culture">Culture</a></li>
                    <li><a href="#innovation">Innovation</a></li>
                    <li><a href="#lifestyle">Lifestyle</a></li>
                    <li><a href="#video">Video</a></li>
                </ul>
            </div>

            <div class="footer-col">
                <h4>Company</h4>
                <ul>
                    <li><a href="#about">About Us</a></li>
                    <li><a href="#contact">Contact</a></li>
                    <li><a href="#advertise">Advertise</a></li>
                    <li><a href="#careers">Careers</a></li>
                </ul>
            </div>

            <div class="footer-col">
                <h4>Legal</h4>
                <ul>
                    <li><a href="#">Privacy Policy</a></li>
                    <li><a href="#">Terms of Use</a></li>
                    <li><a href="#">Cookie Policy</a></li>
                    <li><a href="#">Editorial Policy</a></li>
                </ul>
            </div>
        </div>

        <div class="footer-bottom">
            <p class="copyright">&copy; 2026 MIC CHEQUE. All Rights Reserved.</p>
            <div class="footer-bottom-links">
                <a href="#">Privacy</a>
                <a href="#">Terms</a>
                <a href="#">Contact</a>
            </div>
        </div>
    </div>
</footer>

<!-- ===========================
     JAVASCRIPT
=========================== -->
<script>
    // Set current date
    const dateEl = document.getElementById('current-date');
    if (dateEl) {
        dateEl.textContent = new Date().toLocaleDateString('en-US', {
            weekday: 'long',
            year: 'numeric',
            month: 'long',
            day: 'numeric'
        });
    }

    // Breaking news ticker
    const tickerTexts = [
        "Nairobi Tech Scene Hits Record Investment Numbers!",
        "New Matatu Design Trends Taking Over the City!",
        "Kenyan Startup Raises $5M in Series A Funding!",
        "Matatu Art Exhibition Opens at National Museum!",
        "MIC CHEQUE: Professional Storytelling from Nairobi"
    ];

    let tickerIndex = 0;
    const tickerEl = document.getElementById('ticker');

    setInterval(function () {
        tickerIndex = (tickerIndex + 1) % tickerTexts.length;
        tickerEl.style.opacity = '0';
        setTimeout(function () {
            tickerEl.textContent = tickerTexts[tickerIndex];
            tickerEl.style.opacity = '1';
        }, 300);
    }, 5000);

    // Mobile nav toggle
    function toggleNav() {
        const menu = document.getElementById('nav-menu');
        if (menu.style.display === 'flex') {
            menu.style.display = 'none';
        } else {
            menu.style.display = 'flex';
            menu.style.flexDirection = 'column';
        }
    }

    // Active nav link on scroll
    const sections = document.querySelectorAll('section[id], div[id], article[id]');
    const navLinks = document.querySelectorAll('.nav-menu a');

    window.addEventListener('scroll', function () {
        let current = '';
        sections.forEach(function (section) {
            const sectionTop = section.offsetTop - 120;
            if (window.scrollY >= sectionTop) {
                current = section.getAttribute('id');
            }
        });

        navLinks.forEach(function (link) {
            link.classList.remove('active');
            if (link.getAttribute('href') === '#' + current) {
                link.classList.add('active');
            }
        });
    });

    // Video autoplay handling
    document.addEventListener('DOMContentLoaded', function () {
        const videos = document.querySelectorAll('video[autoplay]');
        videos.forEach(function (video) {
            video.muted = true;
            const playPromise = video.play();
            if (playPromise !== undefined) {
                playPromise.catch(function () {
                    video.setAttribute('controls', '');
                });
            }
        });
    });
</script>

</body>
</html>
