<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>LiveGood - Tu Puerta hacia la Libertad Financiera</title>
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;700&family=Inter:wght@300;400;600;700&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            -webkit-tap-highlight-color: transparent;
        }

        :root {
            --gold: #D4AF37;
            --dark-green: #1B4D3E;
            --light-gold: #F4E8C1;
            --black: #0a0a0a;
            --white: #ffffff;
            --gray: #f8f9fa;
            --red: #e74c3c;
        }

        html {
            scroll-behavior: smooth;
            overflow-x: hidden;
        }

        body {
            font-family: 'Inter', sans-serif;
            background: var(--black);
            color: var(--white);
            overflow-x: hidden;
            width: 100%;
            min-height: 100vh;
        }

        /* Hero Section - Mobile Optimized */
        .hero {
            min-height: auto;
            background: linear-gradient(135deg, #0a0a0a 0%, #1a1a2e 50%, #16213e 100%);
            position: relative;
            display: flex;
            align-items: flex-start;
            justify-content: center;
            padding: 1rem 0.5rem 2rem 0.5rem;
            overflow: hidden;
        }

        .hero::before {
            content: '';
            position: absolute;
            width: 200%;
            height: 100%;
            background: radial-gradient(circle, rgba(212,175,55,0.1) 0%, transparent 70%);
            animation: pulse 4s ease-in-out infinite;
            top: 0;
            left: -50%;
        }

        @keyframes pulse {
            0%, 100% { transform: scale(1); opacity: 0.5; }
            50% { transform: scale(1.1); opacity: 0.8; }
        }

        .hero-content {
            position: relative;
            z-index: 2;
            text-align: center;
            padding: 0.5rem;
            width: 100%;
            max-width: 100%;
        }

        .badge {
            display: inline-block;
            background: rgba(212,175,55,0.2);
            border: 1px solid var(--gold);
            color: var(--gold);
            padding: 0.4rem 1rem;
            border-radius: 50px;
            font-size: 0.75rem;
            font-weight: 600;
            letter-spacing: 1px;
            text-transform: uppercase;
            margin-bottom: 1rem;
            animation: fadeInDown 1s ease;
        }

        h1 {
            font-family: 'Playfair Display', serif;
            font-size: clamp(1.8rem, 8vw, 3rem);
            line-height: 1.2;
            margin-bottom: 1rem;
            background: linear-gradient(135deg, var(--white) 0%, var(--gold) 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            animation: fadeInUp 1s ease 0.2s both;
            padding: 0 0.5rem;
        }

        .subtitle {
            font-size: clamp(0.9rem, 4vw, 1.1rem);
            color: #ccc;
            margin-bottom: 1.5rem;
            line-height: 1.5;
            animation: fadeInUp 1s ease 0.4s both;
            padding: 0 0.5rem;
        }

        .highlight {
            color: var(--gold);
            font-weight: 700;
        }

        /* Video Container - Mobile First */
        .video-container {
            position: relative;
            width: 100%;
            max-width: 100%;
            margin: 1.5rem auto;
            border-radius: 12px;
            overflow: hidden;
            box-shadow: 0 10px 30px rgba(212,175,55,0.2);
            border: 2px solid rgba(212,175,55,0.3);
            animation: fadeInUp 1s ease 0.6s both;
            background: #000;
        }

        .video-wrapper {
            position: relative;
            padding-bottom: 56.25%; /* 16:9 Aspect Ratio */
            height: 0;
            overflow: hidden;
            background: #000;
        }

        .video-wrapper iframe {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            border: none;
            min-height: 200px;
        }

        .video-glow {
            display: none; /* Remove glow on mobile for performance */
        }

        .video-label {
            background: var(--gold);
            color: var(--black);
            padding: 0.6rem;
            font-weight: 700;
            font-size: 0.85rem;
            text-align: center;
            display: block;
        }

        /* CTA Buttons - Mobile Optimized */
        .cta-section {
            display: flex;
            flex-direction: column;
            gap: 0.8rem;
            margin-top: 2rem;
            padding: 0 0.5rem;
            animation: fadeInUp 1s ease 0.8s both;
            width: 100%;
        }

        .btn {
            display: flex;
            align-items: center;
            justify-content: center;
            padding: 1rem 1.2rem;
            border-radius: 50px;
            font-weight: 700;
            font-size: clamp(0.85rem, 3.5vw, 1rem);
            text-decoration: none;
            transition: all 0.3s ease;
            cursor: pointer;
            border: none;
            position: relative;
            overflow: hidden;
            width: 100%;
            min-height: 50px;
            text-align: center;
            line-height: 1.3;
        }

        .btn-primary {
            background: linear-gradient(135deg, var(--gold) 0%, #B8941F 100%);
            color: var(--black);
            box-shadow: 0 5px 15px rgba(212,175,55,0.3);
            order: 1;
        }

        .btn-telegram {
            background: linear-gradient(135deg, #0088cc 0%, #005885 100%);
            color: white;
            box-shadow: 0 5px 15px rgba(0,136,204,0.3);
            order: 2;
        }

        .btn-secondary {
            background: transparent;
            color: var(--gold);
            border: 2px solid var(--gold);
            order: 3;
        }

        .btn:active {
            transform: scale(0.98);
        }

        /* Benefits Section */
        .benefits {
            padding: 3rem 1rem;
            background: var(--white);
            color: var(--black);
        }

        .container {
            width: 100%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 0.5rem;
        }

        .section-title {
            font-family: 'Playfair Display', serif;
            font-size: clamp(1.5rem, 6vw, 2.5rem);
            text-align: center;
            margin-bottom: 2rem;
            color: var(--dark-green);
            line-height: 1.3;
        }

        .benefits-grid {
            display: grid;
            grid-template-columns: 1fr;
            gap: 1rem;
        }

        .benefit-card {
            background: var(--gray);
            padding: 1.5rem;
            border-radius: 15px;
            border-left: 4px solid var(--gold);
            transition: transform 0.3s ease;
        }

        .benefit-card:active {
            transform: scale(0.98);
        }

        .benefit-icon {
            width: 50px;
            height: 50px;
            background: linear-gradient(135deg, var(--gold) 0%, #B8941F 100%);
            border-radius: 12px;
            display: flex;
            align-items: center;
            justify-content: center;
            margin-bottom: 1rem;
            font-size: 1.3rem;
        }

        .benefit-card h3 {
            font-size: 1.1rem;
            margin-bottom: 0.5rem;
            color: var(--dark-green);
        }

        .benefit-card p {
            color: #555;
            line-height: 1.5;
            font-size: 0.9rem;
        }

        .price-highlight {
            background: linear-gradient(135deg, var(--dark-green) 0%, var(--gold) 100%);
            color: white;
            padding: 0.15rem 0.4rem;
            border-radius: 4px;
            font-weight: 700;
            white-space: nowrap;
        }

        /* Comparison Section */
        .comparison {
            padding: 3rem 1rem;
            background: linear-gradient(135deg, var(--dark-green) 0%, #0f281f 100%);
            color: white;
        }

        .costco-comparison {
            background: rgba(255,255,255,0.05);
            border-radius: 15px;
            padding: 1.5rem 1rem;
            width: 100%;
            border: 2px solid rgba(212,175,55,0.3);
        }

        .costco-header {
            text-align: center;
            margin-bottom: 1.5rem;
        }

        .costco-logo-style {
            font-size: 1.3rem;
            font-weight: 700;
            color: var(--gold);
            letter-spacing: 1px;
            margin-bottom: 0.3rem;
        }

        .comparison-row {
            display: flex;
            flex-direction: column;
            gap: 1rem;
            margin: 1rem 0;
            padding: 1rem;
            background: rgba(0,0,0,0.2);
            border-radius: 12px;
        }

        .comparison-item {
            text-align: center;
            padding: 0.5rem;
        }

        .comparison-item h4 {
            font-size: 0.9rem;
            margin-bottom: 0.3rem;
            opacity: 0.9;
        }

        .comparison-item .price {
            font-size: 1.5rem;
            font-weight: 700;
            color: var(--gold);
        }

        .comparison-item .detail {
            font-size: 0.8rem;
            opacity: 0.8;
            margin-top: 0.3rem;
            line-height: 1.3;
        }

        .vs-divider {
            font-weight: 700;
            color: var(--gold);
            font-size: 0.9rem;
            margin: 0.5rem 0;
        }

        .comparison-row.highlight {
            background: rgba(212,175,55,0.2);
            border: 2px solid var(--gold);
        }

        .comparison-row.highlight .comparison-item {
            width: 100%;
        }

        .comparison-row.highlight h4 {
            font-size: 1.1rem;
            color: var(--gold);
        }

        .comparison-row.highlight .price {
            font-size: 2rem;
        }

        .savings-box {
            background: linear-gradient(135deg, var(--gold) 0%, #B8941F 100%);
            color: var(--black);
            padding: 1rem;
            border-radius: 12px;
            text-align: center;
            margin-top: 1.5rem;
            font-weight: 700;
            font-size: 0.95rem;
            line-height: 1.4;
        }

        .highlight-box {
            background: rgba(212,175,55,0.2);
            border-left: 4px solid var(--gold);
            padding: 1rem;
            border-radius: 8px;
            margin: 2rem auto 0;
            max-width: 100%;
        }

        .highlight-box p {
            margin: 0;
            color: #ddd;
            font-style: italic;
            font-size: 0.9rem;
            line-height: 1.5;
            text-align: center;
        }

        /* Passive Income Section */
        .passive-income {
            padding: 3rem 1rem;
            background: var(--black);
            text-align: center;
        }

        .income-box {
            background: linear-gradient(135deg, rgba(212,175,55,0.1) 0%, rgba(27,77,62,0.1) 100%);
            border: 2px solid var(--gold);
            border-radius: 20px;
            padding: 2rem 1rem;
            width: 100%;
            position: relative;
            overflow: hidden;
        }

        .income-box h2 {
            font-family: 'Playfair Display', serif;
            font-size: 1.5rem;
            margin-bottom: 0.5rem;
            position: relative;
            z-index: 1;
        }

        .income-amount {
            font-family: 'Playfair Display', serif;
            font-size: clamp(2.5rem, 10vw, 4rem);
            color: var(--gold);
            font-weight: 700;
            margin: 0.5rem 0;
            position: relative;
            z-index: 1;
            line-height: 1;
        }

        .income-label {
            font-size: 0.9rem;
            color: #ccc;
            margin-bottom: 1.5rem;
            position: relative;
            z-index: 1;
            line-height: 1.4;
        }

        .no-work-list {
            text-align: left;
            background: rgba(0,0,0,0.3);
            padding: 1.5rem 1rem;
            border-radius: 12px;
            margin: 1.5rem 0;
            position: relative;
            z-index: 1;
        }

        .no-work-list h4 {
            color: var(--gold);
            margin-bottom: 0.8rem;
            text-align: center;
            font-size: 1rem;
        }

        .no-work-list ul {
            list-style: none;
            color: #aaa;
            font-size: 0.85rem;
        }

        .no-work-list li {
            padding: 0.4rem 0;
            padding-left: 1.5rem;
            position: relative;
            line-height: 1.4;
        }

        .no-work-list li::before {
            content: '✗';
            position: absolute;
            left: 0;
            color: var(--red);
            font-weight: 700;
        }

        .income-box > p {
            font-size: 0.9rem;
            color: #ccc;
            line-height: 1.6;
            position: relative;
            z-index: 1;
        }

        .disclaimer {
            font-size: 0.7rem;
            color: #666;
            margin-top: 1.5rem;
            line-height: 1.5;
            font-style: italic;
            position: relative;
            z-index: 1;
            padding: 0 0.5rem;
        }

        /* Two Paths Section */
        .two-paths {
            padding: 3rem 1rem;
            background: var(--white);
            color: var(--black);
        }

        .paths-container {
            display: flex;
            flex-direction: column;
            gap: 1.5rem;
            width: 100%;
            margin: 2rem auto;
        }

        .path-card {
            padding: 2rem 1.5rem;
            border-radius: 15px;
            text-align: center;
            transition: transform 0.3s ease;
        }

        .path-card:active {
            transform: scale(0.98);
        }

        .path-card.retirement {
            background: linear-gradient(135deg, #f8f9fa 0%, #e9ecef 100%);
            border: 3px solid var(--dark-green);
        }

        .path-card.entrepreneur {
            background: linear-gradient(135deg, rgba(212,175,55,0.1) 0%, rgba(212,175,55,0.2) 100%);
            border: 3px solid var(--gold);
        }

        .path-icon {
            font-size: 2.5rem;
            margin-bottom: 0.5rem;
        }

        .path-card h3 {
            font-family: 'Playfair Display', serif;
            font-size: 1.4rem;
            margin-bottom: 0.8rem;
        }

        .path-card.retirement h3 {
            color: var(--dark-green);
        }

        .path-card.entrepreneur h3 {
            color: var(--gold);
        }

        .path-card > p {
            color: #555;
            line-height: 1.5;
            margin-bottom: 1rem;
            font-size: 0.9rem;
        }

        .path-benefits {
            text-align: left;
            list-style: none;
            font-size: 0.85rem;
            color: #444;
        }

        .path-benefits li {
            padding: 0.4rem 0;
            padding-left: 1.5rem;
            position: relative;
            line-height: 1.4;
        }

        .path-card.retirement .path-benefits li::before {
            content: '🛡️';
            position: absolute;
            left: 0;
        }

        .path-card.entrepreneur .path-benefits li::before {
            content: '🚀';
            position: absolute;
            left: 0;
        }

        .or-divider {
            display: none; /* Hide on mobile, show on desktop */
        }

        .two-paths .highlight-box {
            margin: 2rem auto 0;
            background: rgba(27,77,62,0.1);
            border-left-color: var(--dark-green);
        }

        .two-paths .highlight-box p {
            color: var(--dark-green);
            font-weight: 600;
        }

        /* Final CTA */
        .final-cta {
            padding: 3rem 1rem;
            background: linear-gradient(135deg, var(--gold) 0%, #B8941F 100%);
            text-align: center;
            color: var(--black);
        }

        .final-cta h2 {
            font-family: 'Playfair Display', serif;
            font-size: clamp(1.5rem, 6vw, 2.5rem);
            margin-bottom: 0.8rem;
            line-height: 1.3;
        }

        .final-cta > p {
            font-size: 0.95rem;
            margin-bottom: 1.5rem;
            opacity: 0.9;
            line-height: 1.5;
        }

        .btn-dark {
            background: var(--black);
            color: var(--gold);
            font-size: 1rem;
            padding: 1.2rem 1.5rem;
            width: 100%;
            margin-bottom: 1rem;
        }

        .final-cta a:not(.btn) {
            color: var(--black);
            text-decoration: underline;
            font-weight: 600;
            font-size: 0.9rem;
            display: inline-block;
            margin-top: 0.5rem;
        }

        /* Footer */
        footer {
            padding: 2rem 1rem;
            background: var(--black);
            text-align: center;
            color: #666;
            border-top: 1px solid rgba(212,175,55,0.2);
        }

        footer p {
            font-size: 0.8rem;
            line-height: 1.5;
            margin-bottom: 0.5rem;
        }

        footer p:last-child {
            font-size: 0.7rem;
            color: #444;
            margin-top: 1rem;
        }

        /* Animations */
        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(20px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        @keyframes fadeInDown {
            from {
                opacity: 0;
                transform: translateY(-20px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        /* Tablet and Desktop */
        @media (min-width: 768px) {
            .hero {
                padding: 2rem;
                min-height: 100vh;
                align-items: center;
            }

            .hero-content {
                max-width: 900px;
                padding: 2rem;
            }

            .badge {
                font-size: 0.9rem;
                padding: 0.5rem 1.5rem;
                margin-bottom: 2rem;
            }

            h1 {
                font-size: clamp(2.5rem, 5vw, 4rem);
                margin-bottom: 1.5rem;
            }

            .subtitle {
                font-size: 1.2rem;
                margin-bottom: 2rem;
            }

            .video-container {
                max-width: 800px;
                margin: 2rem auto;
                border-radius: 20px;
                border-width: 3px;
            }

            .video-glow {
                display: block;
                position: absolute;
                top: -10px;
                left: -10px;
                right: -10px;
                bottom: -10px;
                background: linear-gradient(45deg, var(--gold), transparent, var(--gold));
                border-radius: 25px;
                z-index: -1;
                opacity: 0.5;
                filter: blur(20px);
                animation: glowPulse 3s ease-in-out infinite;
            }

            @keyframes glowPulse {
                0%, 100% { opacity: 0.3; transform: scale(1); }
                50% { opacity: 0.6; transform: scale(1.02); }
            }

            .video-label {
                position: absolute;
                bottom: -40px;
                left: 50%;
                transform: translateX(-50%);
                border-radius: 50px;
                padding: 0.5rem 1.5rem;
            }

            .cta-section {
                flex-direction: row;
                flex-wrap: wrap;
                justify-content: center;
                gap: 1rem;
                margin-top: 4rem;
            }

            .btn {
                width: auto;
                min-width: 280px;
                padding: 1.2rem 2rem;
                font-size: 1.1rem;
            }

            .benefits {
                padding: 6rem 2rem;
            }

            .benefits-grid {
                grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
                gap: 2rem;
            }

            .benefit-card {
                padding: 2.5rem;
            }

            .comparison {
                padding: 6rem 2rem;
            }

            .costco-comparison {
                padding: 3rem;
                max-width: 900px;
                margin: 0 auto;
            }

            .costco-logo-style {
                font-size: 2rem;
            }

            .comparison-row {
                flex-direction: row;
                display: grid;
                grid-template-columns: 1fr auto 1fr;
                gap: 2rem;
                padding: 1.5rem;
            }

            .comparison-item .price {
                font-size: 2rem;
            }

            .comparison-row.highlight {
                display: block;
            }

            .comparison-row.highlight .price {
                font-size: 2.5rem;
            }

            .vs-divider {
                margin: 0;
            }

            .savings-box {
                font-size: 1.2rem;
                padding: 1.5rem;
            }

            .passive-income {
                padding: 6rem 2rem;
            }

            .income-box {
                max-width: 900px;
                margin: 0 auto;
                padding: 3rem;
            }

            .income-box h2 {
                font-size: 2rem;
            }

            .income-label {
                font-size: 1.2rem;
            }

            .no-work-list {
                padding: 2rem;
                margin: 2rem 0;
            }

            .no-work-list h4 {
                font-size: 1.2rem;
            }

            .no-work-list ul {
                font-size: 1rem;
            }

            .disclaimer {
                font-size: 0.75rem;
            }

            .two-paths {
                padding: 6rem 2rem;
            }

            .paths-container {
                flex-direction: row;
                max-width: 1100px;
                gap: 3rem;
                position: relative;
            }

            .path-card {
                flex: 1;
                padding: 3rem 2rem;
            }

            .path-icon {
                font-size: 3rem;
            }

            .path-card h3 {
                font-size: 1.8rem;
            }

            .or-divider {
                display: flex;
                position: absolute;
                left: 50%;
                top: 50%;
                transform: translate(-50%, -50%);
                background: var(--black);
                color: var(--gold);
                width: 60px;
                height: 60px;
                border-radius: 50%;
                align-items: center;
                justify-content: center;
                font-weight: 700;
                font-size: 1.2rem;
                border: 3px solid var(--gold);
                z-index: 10;
            }

            .final-cta {
                padding: 6rem 2rem;
            }

            .final-cta h2 {
                font-size: 2.5rem;
            }

            .final-cta > p {
                font-size: 1.2rem;
            }

            .btn-dark {
                width: auto;
                padding: 1.5rem 3rem;
                font-size: 1.2rem;
            }

            footer {
                padding: 3rem 2rem;
            }

            footer p {
                font-size: 0.9rem;
            }
        }

        /* Large Desktop */
        @media (min-width: 1200px) {
            .video-container {
                max-width: 900px;
            }
        }

        /* Floating particles - Desktop only */
        .particles {
            display: none;
        }

        @media (min-width: 1024px) {
            .particles {
                display: block;
                position: fixed;
                top: 0;
                left: 0;
                width: 100%;
                height: 100%;
                pointer-events: none;
                z-index: 1;
            }

            .particle {
                position: absolute;
                width: 10px;
                height: 10px;
                background: var(--gold);
                border-radius: 50%;
                opacity: 0.3;
                animation: float 20s infinite;
            }

            @keyframes float {
                0%, 100% {
                    transform: translateY(100vh) rotate(0deg);
                    opacity: 0;
                }
                10% {
                    opacity: 0.3;
                }
                90% {
                    opacity: 0.3;
                }
                100% {
                    transform: translateY(-100vh) rotate(720deg);
                    opacity: 0;
                }
            }
        }
    </style>
</head>
<body>

    <!-- Floating Particles - Desktop Only -->
    <div class="particles" id="particles"></div>

    <!-- Hero Section -->
    <section class="hero">
        <div class="hero-content">
            <div class="badge">Oportunidad Exclusiva 2024</div>
            <h1>Libertad Financiera al Alcance de Tu Mano</h1>
            <p class="subtitle">
                Descubre <span class="highlight">LiveGood</span>: el sistema revolucionario que está cambiando vidas. 
                Inversión mínima, potencial ilimitado. <strong>¿Estás listo para transformar tu futuro?</strong>
            </p>

            <!-- YouTube Video Embed -->
            <div class="video-container">
                <div class="video-glow"></div>
                <div class="video-wrapper">
                    <iframe 
                        src="https://www.youtube.com/embed/0D09XGK7hL0?autoplay=0&rel=0&modestbranding=1&playsinline=1"
                        title="LiveGood Presentation"
                        allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
                        allowfullscreen>
                    </iframe>
                </div>
                <div class="video-label">▶ Mira la presentación completa</div>
            </div>

            <!-- CTA Buttons -->
            <div class="cta-section">
                <a href="https://livegoodtour.com/Lifeofnena" class="btn btn-primary">
                    ✨ Estoy Listo para la Libertad
                </a>
                <a href="https://t.me/jaelsidehustle" class="btn btn-telegram">
                    💬 Contáctame en Telegram
                </a>
                <button class="btn btn-secondary" onclick="scrollToInfo()">
                    📋 Conocer Más Detalles
                </button>
            </div>
        </div>
    </section>

    <!-- Benefits Section -->
    <section class="benefits" id="info">
        <div class="container">
            <h2 class="section-title">¿Por Qué LiveGood es Diferente?</h2>
            <div class="benefits-grid">
                <div class="benefit-card">
                    <div class="benefit-icon">💳</div>
                    <h3>Membresía Accesible</h3>
                    <p>Solo <span class="price-highlight">$50</span> de inscripción y <span class="price-highlight">$9.95/mes</span> de membresía. Como Costco, pagas una cuota mínima para acceder a precios exclusivos de mayorista.</p>
                </div>
                <div class="benefit-card">
                    <div class="benefit-icon">🏠</div>
                    <h3>Emprende desde Casa</h3>
                    <p>Trabaja desde cualquier lugar del mundo. Sin horarios, sin jefes, sin limitaciones. Tu negocio, tus reglas, tu ritmo.</p>
                </div>
                <div class="benefit-card">
                    <div class="benefit-icon">🌟</div>
                    <h3>Productos de Alta Demanda</h3>
                    <p>Suplementos premium que se venden solos. Calidad garantizada que genera clientes satisfechos y recurrentes.</p>
                </div>
                <div class="benefit-card">
                    <div class="benefit-icon">🤝</div>
                    <h3>Soporte Total del Equipo</h3>
                    <p>No estás solo. Recibe mentoría personalizada, capacitaciones constantes y herramientas innovadoras para tu éxito.</p>
                </div>
                <div class="benefit-card">
                    <div class="benefit-icon">🚀</div>
                    <h3>Crecimiento Acelerado</h3>
                    <p>Estructura diseñada para escalar rápidamente. Mientras otros tardan años, tú verás resultados en semanas.</p>
                </div>
                <div class="benefit-card">
                    <div class="benefit-icon">🛡️</div>
                    <h3>Garantía de Satisfacción</h3>
                    <p>Productos de calidad comprobada. Si no estás satisfecho, tenemos políticas flexibles que protegen tu inversión.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Costco Comparison Section -->
    <section class="comparison">
        <div class="container">
            <h2 class="section-title" style="color:white; margin-bottom: 2rem;">Como Costco, Pero Mejor</h2>
            
            <div class="costco-comparison">
                <div class="costco-header">
                    <div class="costco-logo-style">COMPARACIÓN DE MEMBRESÍAS</div>
                    <p style="opacity: 0.8; font-size: 0.9rem;">Entiende el poder de comprar al costo</p>
                </div>

                <div class="comparison-row">
                    <div class="comparison-item">
                        <h4>Amazon / Retail</h4>
                        <div class="price">$70-80</div>
                        <div class="detail">Proteína/Colágeno<br>Sin membresía</div>
                    </div>
                    <div class="vs-divider">VS</div>
                    <div class="comparison-item">
                        <h4>Costco</h4>
                        <div class="price">$60-65</div>
                        <div class="detail">Membresía $60/año<br>Ahorro moderado</div>
                    </div>
                </div>

                <div class="comparison-row highlight">
                    <div class="comparison-item">
                        <h4>🌟 LIVEGOOD 🌟</h4>
                        <div class="price">$30-40</div>
                        <div class="detail">Misma calidad, precio real de mayorista<br>Membresía: $9.95/mes</div>
                    </div>
                </div>

                <div class="savings-box">
                    💰 AHORRO REAL: Hasta 50% menos + Oportunidad de ingresos 💰
                </div>
            </div>

            <div class="highlight-box">
                <p>"Al igual que pagas membresía en Costco para comprar más barato, con LiveGood pagas $9.95 al mes por suplementos premium a precios irrepetibles."</p>
            </div>
        </div>
    </section>

    <!-- Passive Income Section -->
    <section class="passive-income">
        <div class="container">
            <div class="income-box">
                <h2>Ingresos sin Trabajar</h2>
                
                <div class="income-amount">$2,000/mes</div>
                <div class="income-label">
                    Ganancia potencial máxima SIN hacer marketing<br>
                    <span style="color: var(--gold); font-weight: 600;">Sistema de dividendos automatizado</span>
                </div>

                <div class="no-work-list">
                    <h4>❌ Sin Necesidad de:</h4>
                    <ul>
                        <li>Invitar a amigos o familiares</li>
                        <li>Crear equipos de ventas</li>
                        <li>Hacer videos de marketing</li>
                        <li>Recomendar productos activamente</li>
                        <li>Usar TikTok Shop o redes sociales</li>
                        <li>Vender nada directamente</li>
                    </ul>
                </div>

                <p>Imagina recibir pagos como <strong>dividendos de inversión</strong>. El sistema recompensa tu posición en la matriz con el tiempo. Mientras otros trabajan 40 horas semanales, tú construyes un ingreso residual automático.</p>

                <div class="disclaimer">
                    *Las ganancias de $2,000 mensuales representan el tope máximo potencial en el plan de compensación para miembros que no realizan actividades de marketing. Estos ingresos se generan a través del sistema de recompensas matriciales estilo dividendos y requieren tiempo para desarrollarse según el crecimiento orgánico de la red. Los resultados individuales varían. Con esfuerzo adicional, los ingresos potenciales son significativamente mayores.
                </div>
            </div>
        </div>
    </section>

    <!-- Two Paths Section -->
    <section class="two-paths">
        <div class="container">
            <h2 class="section-title">Dos Caminos, Una Oportunidad</h2>
            <p style="text-align: center; color: #666; margin: -1.5rem 0 2rem; font-size: 0.95rem;">
                Elige cómo quieres aprovechar esta membresía:
            </p>

            <div class="paths-container">
                <div class="path-card retirement">
                    <div class="path-icon">🏖️</div>
                    <h3>El Planificador</h3>
                    <p>Para quienes piensan en el largo plazo. Asegura un ingreso pasivo para tu jubilación mientras disfrutas tu vida hoy.</p>
                    <ul class="path-benefits">
                        <li>Ingresos para tu retiro</li>
                        <li>Cero presión por ventas</li>
                        <li>Crecimiento automático</li>
                        <li>Perfecto si estás ocupado</li>
                        <li>Diversificación de ingresos</li>
                    </ul>
                </div>

                <div class="or-divider">O</div>

                <div class="path-card entrepreneur">
                    <div class="path-icon">💼</div>
                    <h3>El Constructor</h3>
                    <p>Para emprendedores ambiciosos. Maximiza esta plataforma como un negocio escalable completo con ingresos ilimitados.</p>
                    <ul class="path-benefits">
                        <li>Ingresos ilimitados</li>
                        <li>Marketing de influencer</li>
                        <li>6 formas de ganar</li>
                        <li>Equipo global</li>
                        <li>Libertad total</li>
                    </ul>
                </div>
            </div>

            <div class="highlight-box">
                <p>"Ya sea que quieras tranquilidad para tu vejez o construir un imperio hoy, LiveGood se adapta a ti. La membresía es la misma, las posibilidades son infinitas."</p>
            </div>
        </div>
    </section>

    <!-- Final CTA -->
    <section class="final-cta">
        <div class="container">
            <h2>El Momento es AHORA</h2>
            <p>Cada día que pasa es una oportunidad perdida.<br>
            <strong>No dejes que esta oportunidad pase.</strong></p>
            
            <a href="https://livegoodtour.com/Lifeofnena" class="btn btn-dark">
                🚀 Asegurar Mi Lugar Gratis
            </a>
            
            <a href="https://t.me/jaelsidehustle">¿Tienes dudas? Escríbeme directamente aquí →</a>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <p>© 2024 LiveGood Independent Affiliate. Todos los derechos reservados.</p>
        <p>Esta es una oportunidad de negocio independiente. Los resultados pueden variar.</p>
        <p>*Los ingresos pasivos de hasta $2,000/mes representan el máximo potencial sin actividad de marketing según el plan de compensación actual. Los resultados típicos varían. Los ingresos significativos requieren tiempo, consistencia y/o esfuerzo según el camino elegido.</p>
    </footer>

    <script>
        // Create floating particles - Desktop only
        if (window.innerWidth > 1024) {
            function createParticles() {
                const container = document.getElementById('particles');
                for (let i = 0; i < 15; i++) {
                    const particle = document.createElement('div');
                    particle.className = 'particle';
                    particle.style.left = Math.random() * 100 + '%';
                    particle.style.animationDelay = Math.random() * 20 + 's';
                    particle.style.animationDuration = (15 + Math.random() * 10) + 's';
                    container.appendChild(particle);
                }
            }
            createParticles();
        }

        // Smooth scroll to info
        function scrollToInfo() {
            document.getElementById('info').scrollIntoView({ behavior: 'smooth' });
        }

        // Add scroll animations
        const observerOptions = {
            threshold: 0.1,
            rootMargin: "0px 0px -50px 0px"
        };

        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.style.opacity = "1";
                    entry.target.style.transform = "translateY(0)";
                }
            });
        }, observerOptions);

        // Observe elements
        document.querySelectorAll('.benefit-card, .path-card, .comparison-row').forEach((el) => {
            el.style.opacity = "0";
            el.style.transform = "translateY(20px)";
            el.style.transition = "all 0.6s ease";
            observer.observe(el);
        });

        // Optimize video loading on mobile
        if (window.innerWidth < 768) {
            const iframe = document.querySelector('iframe');
            if (iframe) {
                // Ensure video doesn't autoplay on mobile data
                iframe.setAttribute('loading', 'lazy');
            }
        }
    </script>
</body>
</html>
