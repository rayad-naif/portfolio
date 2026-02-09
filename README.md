
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Creative Directory | IR Official Portfolio</title>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;800&family=Space+Grotesk:wght@300;500;700&display=swap" rel="stylesheet">
    <style>
        /* --- CSS VARIABLES & RESET --- */
        :root {
            --bg: #050505;
            --card-bg: #111111;
            --accent: #ffffff;
            --text: #ffffff;
            --text-dim: #888888;
            --font-head: 'Space Grotesk', sans-serif;
            --font-body: 'Inter', sans-serif;
            --transition: all 0.5s cubic-bezier(0.16, 1, 0.3, 1);
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            background-color: var(--bg);
            color: var(--text);
            font-family: var(--font-body);
            overflow-x: hidden;
            line-height: 1.6;
        }

        /* --- BACKGROUND GRADIENT --- */
        .bg-glow {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: radial-gradient(circle at 50% -20%, #1a1a1a 0%, #050505 100%);
            z-index: -1;
        }

        /* --- NAVIGATION --- */
        nav {
            padding: 40px 5%;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-family: var(--font-head);
            font-size: 1.2rem;
            font-weight: 700;
            letter-spacing: -1px;
            text-transform: uppercase;
        }

        .domain-tag {
            font-family: monospace;
            color: var(--text-dim);
            font-size: 0.8rem;
            border: 1px solid #222;
            padding: 5px 12px;
            border-radius: 50px;
        }

        /* --- HERO --- */
        header {
            padding: 100px 5% 60px;
            text-align: center;
        }

        header h1 {
            font-family: var(--font-head);
            font-size: clamp(3rem, 10vw, 6rem);
            font-weight: 700;
            line-height: 0.9;
            margin-bottom: 20px;
            letter-spacing: -3px;
        }

        header p {
            color: var(--text-dim);
            font-size: 1.1rem;
            max-width: 600px;
            margin: 0 auto;
        }

        /* --- PROJECT GRID --- */
        .project-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(350px, 1fr));
            gap: 20px;
            padding: 40px 5% 100px;
        }

        .project-card {
            background: var(--card-bg);
            border: 1px solid #222;
            padding: 40px;
            text-decoration: none;
            color: var(--text);
            transition: var(--transition);
            position: relative;
            overflow: hidden;
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            min-height: 280px;
        }

        .project-card:hover {
            border-color: #444;
            background: #161616;
            transform: translateY(-5px);
        }

        .project-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 2px;
            background: linear-gradient(90deg, transparent, var(--accent), transparent);
            transform: translateX(-100%);
            transition: 0.6s ease;
        }

        .project-card:hover::before {
            transform: translateX(100%);
        }

        .card-category {
            font-size: 0.7rem;
            text-transform: uppercase;
            letter-spacing: 2px;
            color: var(--text-dim);
            margin-bottom: 10px;
            display: block;
        }

        .card-title {
            font-family: var(--font-head);
            font-size: 1.8rem;
            font-weight: 500;
            margin-bottom: 15px;
            line-height: 1.1;
        }

        .card-desc {
            font-size: 0.9rem;
            color: var(--text-dim);
            margin-bottom: 30px;
        }

        .card-link {
            font-size: 0.8rem;
            text-transform: uppercase;
            letter-spacing: 1px;
            font-weight: 600;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .card-link svg {
            width: 15px;
            transition: transform 0.3s ease;
        }

        .project-card:hover .card-link svg {
            transform: translateX(5px);
        }

        /* --- FOOTER --- */
        footer {
            padding: 60px 5%;
            border-top: 1px solid #111;
            display: flex;
            justify-content: space-between;
            align-items: center;
            font-size: 0.8rem;
            color: var(--text-dim);
        }

        /* --- RESPONSIVE --- */
        @media (max-width: 768px) {
            .project-grid {
                grid-template-columns: 1fr;
            }
            header h1 {
                font-size: 3.5rem;
            }
        }
    </style>
</head>
<body>
    <div class="bg-glow"></div>

    <nav>
        <div class="logo">IR Official</div>
        <div class="domain-tag">portfolio.irofficial.com</div>
    </nav>

    <header>
        <h1>DESIGN<br>DIRECTORY</h1>
        <p>A curated collection of high-performance landing pages, production-ready architectures, and digital experiences.</p>
    </header>

    <main class="project-grid">
        <!-- 1. LUMINA SKINCARE -->
        <a href="lumina-skincare.html" class="project-card">
            <div>
                <span class="card-category">Beauty & Wellness</span>
                <h2 class="card-title">Lumina Skincare</h2>
                <p class="card-desc">Minimalist high-key aesthetic focusing on clinical results and organic sourcing.</p>
            </div>
            <div class="card-link">View Project <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M5 12h14M12 5l7 7-7 7"/></svg></div>
        </a>

        <!-- 2. TITAN WEALTH -->
        <a href="titan-wealth.html" class="project-card">
            <div>
                <span class="card-category">Finance</span>
                <h2 class="card-title">Titan Wealth</h2>
                <p class="card-desc">Deep emerald and gold institutional private equity site with animated market statistics.</p>
            </div>
            <div class="card-link">View Project <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M5 12h14M12 5l7 7-7 7"/></svg></div>
        </a>

        <!-- 3. VELOCITY -->
        <a href="velocity.html" class="project-card">
            <div>
                <span class="card-category">Automotive</span>
                <h2 class="card-title">Velocity EV</h2>
                <p class="card-desc">Aggressive dark-mode landing page for luxury electric vehicles with real-time performance counters.</p>
            </div>
            <div class="card-link">View Project <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M5 12h14M12 5l7 7-7 7"/></svg></div>
        </a>

        <!-- 4. ARKITEKT -->
        <a href="arkitekt.html" class="project-card">
            <div>
                <span class="card-category">Architecture</span>
                <h2 class="card-title">Arkitekt Studio</h2>
                <p class="card-desc">Brutalist grid-heavy design showcasing international monuments and sustainable form.</p>
            </div>
            <div class="card-link">View Project <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M5 12h14M12 5l7 7-7 7"/></svg></div>
        </a>

        <!-- 5. NEXUS AGENCY -->
        <a href="nexus.html" class="project-card">
            <div>
                <span class="card-category">Digital Agency</span>
                <h2 class="card-title">Nexus Creative</h2>
                <p class="card-desc">Bold typography and neon accents for a tech-focused creative engineering studio.</p>
            </div>
            <div class="card-link">View Project <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M5 12h14M12 5l7 7-7 7"/></svg></div>
        </a>

        <!-- 6. AETHER FASHION -->
        <a href="aether.html" class="project-card">
            <div>
                <span class="card-category">Luxury Fashion</span>
                <h2 class="card-title">Aether Atelier</h2>
                <p class="card-desc">Soft, fluid interactions designed for a high-end Florence-based silk atelier.</p>
            </div>
            <div class="card-link">View Project <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M5 12h14M12 5l7 7-7 7"/></svg></div>
        </a>

        <!-- 7. NEON BITES -->
        <a href="neon-bites.html" class="project-card">
            <div>
                <span class="card-category">Restaurant</span>
                <h2 class="card-title">Neon Bites</h2>
                <p class="card-desc">Cyberpunk-themed dining experience featuring glitch effects and bioluminescent visuals.</p>
            </div>
            <div class="card-link">View Project <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M5 12h14M12 5l7 7-7 7"/></svg></div>
        </a>

        <!-- 8. VIGNETTE PORTFOLIO -->
        <a href="vignette-portfolio.html" class="project-card">
            <div>
                <span class="card-category">Graphic Design</span>
                <h2 class="card-title">Vignette Studio</h2>
                <p class="card-desc">Experimental portfolio with infinite scroll marquees and dynamic project hover reveals.</p>
            </div>
            <div class="card-link">View Project <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M5 12h14M12 5l7 7-7 7"/></svg></div>
        </a>

        <!-- 9. AURA STUDIOS -->
        <a href="aura-studios.html" class="project-card">
            <div>
                <span class="card-category">Photography</span>
                <h2 class="card-title">Aura Fine Art</h2>
                <p class="card-desc">Cinematic photography studio site with masonry galleries and custom cursor interactions.</p>
            </div>
            <div class="card-link">View Project <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M5 12h14M12 5l7 7-7 7"/></svg></div>
        </a>

        <!-- 10. SERAPHINA BLOOM -->
        <a href="seraphina-bloom.html" class="project-card">
            <div>
                <span class="card-category">Life Coaching</span>
                <h2 class="card-title">Seraphina Bloom</h2>
                <p class="card-desc">Warm, flowery aesthetic for holistic coaching featuring custom falling petal animations.</p>
            </div>
            <div class="card-link">View Project <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M5 12h14M12 5l7 7-7 7"/></svg></div>
        </a>

        <!-- 11. STEPHEN ETZEL -->
        <a href="https://thestephenetzel.com/home" class="project-card">
            <div>
                <span class="card-category">Real Estate Education</span>
                <h2 class="card-title">Stephen Etzel</h2>
                <p class="card-desc">Professional corporate redesign for a senior instructor featuring integrated calendars.</p>
            </div>
            <div class="card-link">View Project <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M5 12h14M12 5l7 7-7 7"/></svg></div>
        </a>
    </main>

    <footer>
        <div>© 2024 IR Official Directory</div>
        <div>Built for high-performance browsing</div>
    </footer>

    <script>
        // Simple entry animation for cards
        const cards = document.querySelectorAll('.project-card');
        const observer = new IntersectionObserver((entries) => {
            entries.forEach((entry, index) => {
                if (entry.isIntersecting) {
                    setTimeout(() => {
                        entry.target.style.opacity = '1';
                        entry.target.style.transform = 'translateY(0)';
                    }, index * 100);
                }
            });
        }, { threshold: 0.1 });

        cards.forEach(card => {
            card.style.opacity = '0';
            card.style.transform = 'translateY(20px)';
            card.style.transition = 'all 0.6s cubic-bezier(0.16, 1, 0.3, 1)';
            observer.observe(card);
        });
    </script>
</body>
</html>
