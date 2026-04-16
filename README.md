<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>MIC CHEQUE | Professional Storytelling</title>
    <link href="https://fonts.googleapis.com/css2?family=Cinzel+Decorative:wght@400;700;900&family=Playfair+Display:ital,wght@0,400;0,700;0,900;1,400&family=Lora:ital,wght@0,400;0,700;1,400&family=Montserrat:wght@300;400;600&display=swap" rel="stylesheet">
    <script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.12.2/gsap.min.js"></script>
    <style>
        :root {
            --primary-color: #1a1a1a;
            --accent-color: #c5a059;
            --text-color: #e0e0e0;
            --bg-color: #0a0a0a;
            --card-bg: #151515;
            --font-heading: 'Playfair Display', serif;
            --font-display: 'Cinzel Decorative', serif;
            --font-body: 'Lora', serif;
            --font-accent: 'Montserrat', sans-serif;
        }

        * { margin: 0; padding: 0; box-sizing: border-box; }

        body {
            background-color: var(--bg-color);
            color: var(--text-color);
            font-family: var(--font-body);
            line-height: 1.8;
            overflow-x: hidden;
        }

        body.loading { overflow: hidden; }

        /* Animation Overlay */
        #intro-overlay {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: #000;
            z-index: 9999;
            display: flex;
            justify-content: center;
            align-items: center;
            overflow: hidden;
        }

        .animation-container {
            position: relative;
            width: 800px;
            height: 400px;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
        }

        .blocks-container {
            display: flex;
            gap: 10px;
            margin-bottom: 50px;
        }

        .letter-block {
            width: 60px;
            height: 60px;
            background: #d4a76a;
            border: 3px solid #8b5e3c;
            display: flex;
            justify-content: center;
            align-items: center;
            font-family: 'Cinzel Decorative', serif;
            font-size: 32px;
            font-weight: 900;
            color: #3e2723;
            box-shadow: inset 0 0 10px rgba(0,0,0,0.2), 4px 4px 5px rgba(0,0,0,0.5);
            position: relative;
        }

        #jerry {
            position: absolute;
            width: 80px;
            bottom: 20px;
            left: -100px;
            z-index: 10001;
        }

        #tom {
            position: absolute;
            width: 150px;
            bottom: 0px;
            left: -300px;
            z-index: 10002;
        }

        .fade-out {
            opacity: 0 !important;
            visibility: hidden !important;
            transition: opacity 1s ease, visibility 1s;
        }

        /* Rest of the styles (Navigation, Header, Main, etc.) */
        .top-nav { position: sticky; top: 0; background: rgba(10, 10, 10, 0.95); backdrop-filter: blur(10px); z-index: 1000; border-bottom: 1px solid #222; padding: 1rem 0; }
        .top-nav ul { list-style: none; display: flex; justify-content: center; gap: 3rem; }
        .top-nav a { text-decoration: none; color: #fff; font-family: var(--font-accent); font-size: 0.7rem; font-weight: 600; text-transform: uppercase; letter-spacing: 2px; }
        header { padding: 6rem 1rem 4rem; text-align: center; background: linear-gradient(to bottom, #0a0a0a, #151515); }
        .logo-container img { max-width: 400px; height: auto; margin-bottom: 2rem; mix-blend-mode: screen; }
        h1.site-title { font-family: var(--font-display); font-size: clamp(3rem, 8vw, 5.5rem); font-weight: 900; color: #fff; letter-spacing: 6px; text-transform: uppercase; }
        .site-tagline { font-family: var(--font-accent); text-transform: uppercase; font-size: 0.85rem; letter-spacing: 6px; color: var(--accent-color); font-weight: 600; }
        main { max-width: 1000px; margin: 0 auto; padding: 4rem 1.5rem; }
        .post { background: var(--card-bg); padding: 4rem; border-radius: 8px; margin-bottom: 4rem; border: 1px solid #222; }
        .post-title { font-family: var(--font-heading); font-size: clamp(2.5rem, 5vw, 3.8rem); font-weight: 900; color: #fff; text-align: center; margin-bottom: 2.5rem; }
        .post-content { font-size: 1.2rem; text-align: justify; max-width: 800px; margin: 0 auto; color: #ccc; }
        .post-content p { margin-bottom: 2rem; }
        .post-content p::first-letter { float: left; font-size: 4.5rem; line-height: 0.8; font-weight: bold; margin-right: 15px; margin-top: 10px; font-family: var(--font-display); color: var(--accent-color); }
        footer { padding: 6rem 1rem; text-align: center; background-color: #000; color: #fff; border-top: 1px solid #222; }
        .footer-tagline { font-family: var(--font-display); font-size: 2.2rem; color: var(--accent-color); }
        .copyright { font-family: var(--font-accent); font-size: 0.7rem; text-transform: uppercase; color: #666; }
    </style>
</head>
<body class="loading">

    <div id="intro-overlay">
        <div class="animation-container">
            <div class="blocks-container">
                <div class="letter-block" data-letter="M">M</div>
                <div class="letter-block" data-letter="I">I</div>
                <div class="letter-block" data-letter="C">C</div>
                <div style="width: 20px;"></div>
                <div class="letter-block" data-letter="C">C</div>
                <div class="letter-block" data-letter="H">H</div>
                <div class="letter-block" data-letter="E">E</div>
                <div class="letter-block" data-letter="Q">Q</div>
                <div class="letter-block" data-letter="U">U</div>
                <div class="letter-block" data-letter="E">E</div>
            </div>
            <img id="jerry" src="https://i.ibb.co/v4pX2p0/jerry-run.png" alt="Jerry">
            <img id="tom" src="https://i.ibb.co/W2W7X0y/tom-run.png" alt="Tom">
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
        <article class="post">
            <h2 class="post-title">Nairobi’s Tech Hustle</h2>
            <div class="post-content">
                <p>In the modern heartbeat of Kenya, Nairobi has grown into one of Africa’s most influential innovation centers...</p>
            </div>
        </article>
    </main>

    <footer>
        <p class="footer-tagline">NIKO KADI JE WEWE?</p>
        <p class="copyright">&copy; 2026 MIC CHEQUE. ALL RIGHTS RESERVED.</p>
    </footer>

    <script>
        // Sound handling
        const sounds = {
            hit: new Audio('https://www.soundjay.com/misc/sounds/wood-hit-1.mp3'),
            run: new Audio('https://www.soundjay.com/human/sounds/footsteps-4.mp3'),
            chase: new Audio('https://www.soundjay.com/misc/sounds/fail-trombone-01.mp3')
        };

        window.addEventListener('load', () => {
            const tl = gsap.timeline({
                onComplete: () => {
                    document.getElementById('intro-overlay').classList.add('fade-out');
                    document.body.classList.remove('loading');
                }
            });

            const blocks = document.querySelectorAll('.letter-block');
            
            // 1. Blocks fall messily
            tl.from(blocks, {
                y: -500,
                rotation: () => Math.random() * 90 - 45,
                x: () => Math.random() * 100 - 50,
                duration: 1,
                stagger: 0.1,
                ease: "bounce.out",
                onStart: () => sounds.hit.play()
            });

            // 2. Jerry enters
            tl.to("#jerry", {
                left: "20%",
                duration: 1.5,
                ease: "power1.inOut",
                onStart: () => {
                    sounds.run.loop = true;
                    sounds.run.play();
                }
            });

            // 3. Jerry fixes blocks one by one
            blocks.forEach((block, i) => {
                tl.to("#jerry", {
                    left: block.offsetLeft - 10,
                    duration: 0.4,
                    ease: "power1.inOut"
                });
                tl.to(block, {
                    rotation: 0,
                    x: 0,
                    y: 0,
                    duration: 0.3,
                    ease: "back.out(1.7)",
                    onStart: () => sounds.hit.play()
                });
            });

            // 4. Jerry finishes and poses
            tl.to("#jerry", {
                scale: 1.2,
                duration: 0.5,
                yoyo: true,
                repeat: 1
            });

            // 5. Tom enters, Jerry panics
            tl.to("#tom", {
                left: "-50px",
                duration: 1,
                ease: "power2.out",
                onStart: () => sounds.chase.play()
            });

            // 6. The Chase!
            tl.to("#jerry", {
                left: "120%",
                duration: 2,
                ease: "power1.in"
            });
            tl.to("#tom", {
                left: "110%",
                duration: 2,
                ease: "power1.in",
                delay: -1.8
            });

            // 7. Final Fade
            tl.to("#intro-overlay", {
                opacity: 0,
                duration: 1,
                delay: 0.5
            });
        });
    </script>
</body>
</html>
