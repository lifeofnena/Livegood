
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>LiveGood - Tu Puerta hacia la Libertad Financiera</title>
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;700&family=Inter:wght@300;400;600;700&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
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

        body {
            font-family: 'Inter', sans-serif;
            background: var(--black);
            color: var(--white);
            overflow-x: hidden;
        }

        /* Hero Section */
        .hero {
            min-height: 100vh;
            background: linear-gradient(135deg, #0a0a0a 0%, #1a1a2e 50%, #16213e 100%);
            position: relative;
            display: flex;
            align-items: center;
            justify-content: center;
            overflow: hidden;
        }

        .hero::before {
            content: '';
            position: absolute;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle, rgba(212,175,55,0.1) 0%, transparent 70%);
            animation: pulse 4s ease-in-out infinite;
        }

        @keyframes pulse {
            0%, 100% { transform: scale(1); opacity: 0.5; }
            50% { transform: scale(1.1); opacity: 0.8; }
        }

        .hero-content {
            position: relative;
            z-index: 2;
            text-align: center;
            padding: 2rem;
            max-width: 1000px;
        }

        .badge {
            display: inline-block;
            background: rgba(212,175,55,0.2);
            border: 1px solid var(--gold);
            color: var(--gold);
            padding: 0.5rem 1.5rem;
            border-radius: 50px;
            font-size: 0.9rem;
            font-weight: 600;
            letter-spacing: 2px;
            text-transform: uppercase;
            margin-bottom: 2rem;
            animation: fadeInDown 1s ease;
        }

        h1 {
            font-family: 'Playfair Display', serif;
            font-size: clamp(2.5rem, 6vw, 4.5rem);
            line-height: 1.1;
            margin-bottom: 1.5rem;
            background: linear-gradient(135deg, var(--white) 0%, var(--gold) 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            animation: fadeInUp 1s ease 0.2s both;
        }

        .subtitle {
            font-size: 1.25rem;
            color: #ccc;
            margin-bottom: 2rem;
            line-height: 1.6;
            animation: fadeInUp 1s ease 0.4s both;
        }

        .highlight {
            color: var(--gold);
            font-weight: 700;
        }

        /* Video Container - YouTube Embed */
        .video-container {
            position: relative;
            width: 100%;
            max-width: 900px;
            margin: 3rem auto;
            border-radius: 20px;
            overflow: hidden;
            box-shadow: 0 25px 50px -12px rgba(212,175,55,0.25);
            border: 3px solid rgba(212,175,55,0.3);
            animation: fadeInUp 1s ease 0.6s both;
            background: #000;
        }

        .video-wrapper {
            position: relative;
            padding-bottom: 56.25%; /* 16:9 Aspect Ratio */
            height: 0;
            overflow: hidden;
        }

        .video-wrapper iframe {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            border: none;
        }

        .video-glow {
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
            background: var(--gold);
            color: var(--black);
            padding: 0.5rem 1.5rem;
            border-radius: 50px;
            font-weight: 700;
            font-size: 0.9rem;
            white-space: nowrap;
            box-shadow: 0 5px 15px rgba(212,175,55,0.3);
        }

        /* CTA Buttons */
        .cta-section {
            display: flex;
            flex-direction: column;
            gap: 1rem;
            margin-top: 5rem;
            animation: fadeInUp 1s ease 0.8s both;
        }

        .btn {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            padding: 1.2rem 2.5rem;
            border-radius: 50px;
            font-weight: 700;
            font-size: 1.1rem;
            text-decoration: none;
            transition: all 0.3s ease;
            cursor: pointer;
            border: none;
            position: relative;
            overflow: hidden;
        }

        .btn-primary {
            background: linear-gradient(135deg, var(--gold) 0%, #B8941F 100%);
            color: var(--black);
            box-shadow: 0 10px 30px rgba(212,175,55,0.3);
        }

        .btn-primary:hover {
            transform: translateY(-3px);
            box-shadow: 0 15px 40px rgba(212,175,55,0.5);
        }

        .btn-secondary {
            background: transparent;
            color: var(--gold);
            border: 2px solid var(--gold);
        }

        .btn-secondary:hover {
            background: var(--gold);
            color: var(--black);
            transform: translateY(-3px);
        }

        .btn-telegram {
            background: linear-gradient(135deg, #0088cc 0%, #005885 100%);
            color: white;
            box-shadow: 0 10px 30px rgba(0,136,204,0.3);
        }

        .btn-telegram:hover {
            transform: translateY(-3px);
            box-shadow: 0 15px 40px rgba(0,136,204,0.5);
        }

        .btn::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255,255,255,0.3), transparent);
            transition: left 0.5s;
        }

        .btn:hover::before {
            left: 100%;
        }

        /* Benefits Section */
        .benefits {
            padding: 6rem 2rem;
            background: var(--white);
            color: var(--black);
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
        }

        .section-title {
            font-family: 'Playfair Display', serif;
            font-size: 2.5rem;
            text-align: center;
            margin-bottom: 3rem;
            color: var(--dark-green);
        }

        .benefits-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }

        .benefit-card {
            background: var(--gray);
            padding: 2.5rem;
            border-radius: 20px;
            border-left: 4px solid var(--gold);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }

        .benefit-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 20px 40px rgba(0,0,0,0.1);
        }

        .benefit-icon {
            width: 60px;
            height: 60px;
            background: linear-gradient(135deg, var(--gold) 0%, #B8941F 100%);
            border-radius: 15px;
            display: flex;
            align-items: center;
            justify-content: center;
            margin-bottom: 1.5rem;
            font-size: 1.5rem;
        }

        .benefit-card h3 {
            font-size: 1.3rem;
            margin-bottom: 1rem;
            color: var(--dark-green);
        }

        .benefit-card p {
            color: #666;
            line-height: 1.6;
        }

        .price-highlight {
            background: linear-gradient(135deg, var(--dark-green) 0%, var(--gold) 100%);
            color: white;
            padding: 0.2rem 0.5rem;
            border-radius: 5px;
            font-weight: 700;
        }

        /* Comparison Section - Costco Style */
        .comparison {
            padding: 6rem 2rem;
            background: linear-gradient(135deg, var(--dark-green) 0%, #0f281f 100%);
            color: white;
        }

        .costco-comparison {
            background: rgba(255,255,255,0.05);
            border-radius: 20px;
            padding: 3rem;
            max-width: 900px;
            margin: 0 auto;
            border: 2px solid rgba(212,175,55,0.3);
        }

        .costco-header {
            text-align: center;
            margin-bottom: 2rem;
        }

        .costco-logo-style {
            font-size: 2rem;
            font-weight: 700;
            color: var(--gold);
            letter-spacing: 2px;
            margin-bottom: 0.5rem;
        }

        .comparison-row {
            display: grid;
            grid-template-columns: 1fr 1fr 1fr;
            gap: 2rem;
            align-items: center;
            margin: 2rem 0;
            padding: 1.5rem;
            background: rgba(0,0,0,0.2);
            border-radius: 15px;
        }

        .comparison-item {
            text-align: center;
        }

        .comparison-item h4 {
            font-size: 1.1rem;
            margin-bottom: 0.5rem;
            opacity: 0.9;
        }

        .comparison-item .price {
            font-size: 2rem;
            font-weight: 700;
            color: var(--gold);
        }

        .comparison-item .detail {
            font-size: 0.9rem;
            opacity: 0.8;
            margin-top: 0.5rem;
        }

        .vs-divider {
            font-weight: 700;
            color: var(--gold);
            font-size: 1.2rem;
        }

        .savings-box {
            background: linear-gradient(135deg, var(--gold) 0%, #B8941F 100%);
            color: var(--black);
            padding: 1.5rem;
            border-radius: 15px;
            text-align: center;
            margin-top: 2rem;
            font-weight: 700;
            font-size: 1.2rem;
        }

        /* Passive Income Section */
        .passive-income {
            padding: 6rem 2rem;
            background: var(--black);
            text-align: center;
        }

        .income-box {
            background: linear-gradient(135deg, rgba(212,175,55,0.1) 0%, rgba(27,77,62,0.1) 100%);
            border: 2px solid var(--gold);
            border-radius: 25px;
            padding: 3rem;
            max-width: 900px;
            margin: 0 auto;
            position: relative;
            overflow: hidden;
        }

        .income-box::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle, rgba(212,175,55,0.1) 0%, transparent 70%);
            animation: rotate 20s linear infinite;
        }

        @keyframes rotate {
            from { transform: rotate(0deg); }
            to { transform: rotate(360deg); }
        }

        .income-amount {
            font-family: 'Playfair Display', serif;
            font-size: 4rem;
            color: var(--gold);
            font-weight: 700;
            margin: 1rem 0;
            position: relative;
            z-index: 1;
        }

        .income-label {
            font-size: 1.2rem;
            color: #ccc;
            margin-bottom: 2rem;
            position: relative;
            z-index: 1;
        }

        .no-work-list {
            text-align: left;
            background: rgba(0,0,0,0.3);
            padding: 2rem;
            border-radius: 15px;
            margin: 2rem 0;
            position: relative;
            z-index: 1;
        }

        .no-work-list h4 {
            color: var(--gold);
            margin-bottom: 1rem;
            text-align: center;
        }

        .no-work-list ul {
            list-style: none;
            color: #aaa;
        }

        .no-work-list li {
            padding: 0.5rem 0;
            padding-left: 2rem;
            position: relative;
        }

        .no-work-list li::before {
            content: '✗';
            position: absolute;
            left: 0;
            color: var(--red);
            font-weight: 700;
        }

        .disclaimer {
            font-size: 0.75rem;
            color: #666;
            margin-top: 2rem;
            line-height: 1.6;
            font-style: italic;
            position: relative;
            z-index: 1;
        }

        /* Two Paths Section */
        .two-paths {
            padding: 6rem 2rem;
            background: var(--white);
            color: var(--black);
        }

        .paths-container {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 3rem;
            max-width: 1100px;
            margin: 3rem auto;
            position: relative;
        }

        .path-card {
            padding: 3rem 2rem;
            border-radius: 20px;
            text-align: center;
            transition: transform 0.3s ease;
            position: relative;
            overflow: hidden;
        }

        .path-card:hover {
            transform: translateY(-10px);
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
            font-size: 3rem;
            margin-bottom: 1rem;
        }

        .path-card h3 {
            font-family: 'Playfair Display', serif;
            font-size: 1.8rem;
            margin-bottom: 1rem;
        }

        .path-card.retirement h3 {
            color: var(--dark-green);
        }

        .path-card.entrepreneur h3 {
            color: var(--gold);
        }

        .path-card p {
            color: #666;
            line-height: 1.8;
            margin-bottom: 1.5rem;
        }

        .path-benefits {
            text-align: left;
            list-style: none;
            font-size: 0.95rem;
        }

        .path-benefits li {
            padding: 0.5rem 0;
            padding-left: 1.5rem;
            position: relative;
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
            position: absolute;
            left: 50%;
            top: 50%;
            transform: translate(-50%, -50%);
            background: var(--black);
            color: var(--gold);
            width: 60px;
            height: 60px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: 700;
            font-size: 1.2rem;
            border: 3px solid var(--gold);
            z-index: 10;
        }

        /* Final CTA */
        .final-cta {
            padding: 6rem 2rem;
            background: linear-gradient(135deg, var(--gold) 0%, #B8941F 100%);
            text-align: center;
            color: var(--black);
        }

        .final-cta h2 {
            font-family: 'Playfair Display', serif;
            font-size: 2.5rem;
            margin-bottom: 1rem;
        }

        .final-cta p {
            font-size: 1.2rem;
            margin-bottom: 2rem;
            opacity: 0.9;
        }

        .btn-dark {
            background: var(--black);
            color: var(--gold);
            font-size: 1.2rem;
            padding: 1.5rem 3rem;
        }

        .btn-dark:hover {
            background: var(--dark-green);
            color: white;
            transform: translateY(-3px);
        }

        /* Footer */
        footer {
            padding: 3rem 2rem;
            background: var(--black);
            text-align: center;
            color: #666;
            border-top: 1px solid rgba(212,175,55,0.2);
        }

        /* Animations */
        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        @keyframes fadeInDown {
            from {
                opacity: 0;
                transform: translateY(-30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        /* Responsive */
        @media (max-width: 768px) {
            .paths-container {
                grid-template-columns: 1fr;
                gap: 2rem;
            }
            
            .or-divider {
                display: none;
            }
            
            .comparison-row {
                grid-template-columns: 1fr;
                gap: 1rem;
            }
            
            .vs-divider {
                transform: rotate(90deg);
            }
            
            .btn {
                width: 100%;
            }

            .income-amount {
                font-size: 2.5rem;
            }

            .video-container {
                margin: 2rem auto 4rem auto;
            }
        }

        /* Floating particles */
        .particles {
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

        .highlight-box {
            background: rgba(212,175,55,0.2);
            border-left: 4px solid var(--gold);
            padding: 1.5rem;
            border-radius: 10px;
            margin: 2rem 0;
            text-align: left;
        }

        .highlight-box p {
            margin: 0;
            color: #ddd;
            font-style: italic;
        }
    </style>
</head>
<body>

    <!-- Floating Particles -->
    <div class="particles" id="particles"></div>

    <!-- Hero Section -->
    <section class="hero">
        <div class="hero-content">
            <div class="badge">Oportunidad Exclusiva 2024</div>
            <h1>Libertad Financiera<br>al Alcance de Tu Mano</h1>
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
                    ✨ Estoy Listo para la Libertad - Asegura tu lugar GRATIS
                </a>
                <a href="https://t.me/jaelsidehustle" class="btn btn-telegram">
                    💬 Contáctame - Únete a Presentaciones en Vivo
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
                    <p>Solo <span class="price-highlight">$50</span> de inscripción y <span class="price-highlight">$9.95/mes</span> de membresía. Al igual que Costco, pagas una cuota mínima para acceder a precios exclusivos de mayorista.</p>
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
            <h2 class="section-title" style="color:white; margin-bottom: 3rem;">Como Costco, Pero Mejor</h2>
            
            <div class="costco-comparison">
                <div class="costco-header">
                    <div class="costco-logo-style">COMPARACIÓN DE MEMBRESÍAS</div>
                    <p style="opacity: 0.8;">Entiende el poder de comprar al costo</p>
                </div>

                <div class="comparison-row">
                    <div class="comparison-item">
                        <h4>Amazon / Tiendas Retail</h4>
                        <div class="price">$70-80</div>
                        <div class="detail">Proteína/Colágeno<br>Sin membresía, precio alto</div>
                    </div>
                    <div class="vs-divider">VS</div>
                    <div class="comparison-item">
                        <h4>Costco Wholesale</h4>
                        <div class="price">$60-65</div>
                        <div class="detail">Con membresía $60/año<br>Ahorro moderado</div>
                    </div>
                </div>

                <div class="comparison-row" style="background: rgba(212,175,55,0.2); border: 2px solid var(--gold);">
                    <div class="comparison-item" style="grid-column: 1 / -1;">
                        <h4 style="color: var(--gold); font-size: 1.3rem;">🌟 LIVEGOOD MEMBERSHIP 🌟</h4>
                        <div class="price" style="font-size: 2.5rem;">$30-40</div>
                        <div class="detail" style="font-size: 1.1rem;">
                            Misma calidad premium, precio de mayorista real<br>
                            Membresión: $9.95/mes | Inscripción: $50 único pago
                        </div>
                    </div>
                </div>

                <div class="savings-box">
                    💰 AHORRO REAL: Hasta 50% menos que retail + Oportunidad de generar ingresos 💰
                </div>
            </div>

            <div class="highlight-box" style="max-width: 800px; margin: 3rem auto 0;">
                <p>"Al igual que pagas membresía en Costco para comprar papel higiénico y pollo más barato, con LiveGood pagas $9.95 al mes para comprar suplementos de alta calidad a precios que no encontrarás en ningún otro lugar."</p>
            </div>
        </div>
    </section>

    <!-- Passive Income Section -->
    <section class="passive-income">
        <div class="container">
            <div class="income-box">
                <h2 style="font-family: 'Playfair Display', serif; font-size: 2rem; margin-bottom: 1rem; position: relative; z-index: 1;">
                    Ingresos sin Trabajar
                </h2>
                
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

                <p style="font-size: 1.1rem; color: #ccc; line-height: 1.8; position: relative; z-index: 1;">
                    Imagina recibir pagos como <strong>dividendos de inversión</strong>. El sistema está diseñado para recompensar tu posición en la matriz con el tiempo. Mientras otros trabajan 40 horas semanales, tú puedes construir un ingreso residual que crece automáticamente.
                </p>

                <div class="disclaimer">
                    *Las ganancias de $2,000 mensuales representan el tope máximo potencial en el plan de compensación para miembros que no realizan actividades de marketing ni construyen equipos. Estos ingresos se generan a través del sistema de recompensas matriciales estilo dividendos y requieren tiempo para desarrollarse según el crecimiento orgánico de la red. Los resultados individuales varían y no garantizan ingresos específicos. Con esfuerzo adicional (construcción de equipo, marketing activo), los ingresos potenciales son significativamente mayores.
                </div>
            </div>
        </div>
    </section>

    <!-- Two Paths Section -->
    <section class="two-paths">
        <div class="container">
            <h2 class="section-title">Dos Caminos, Una Oportunidad</h2>
            <p style="text-align: center; color: #666; max-width: 600px; margin: -2rem auto 3rem;">
                LiveGood se adapta a tu estilo de vida y metas. Elige cómo quieres aprovechar esta membresía:
            </p>

            <div class="paths-container">
                <div class="path-card retirement">
                    <div class="path-icon">🏖️</div>
                    <h3>El Planificador de Jubilación</h3>
                    <p>
                        Para quienes piensan en el largo plazo. Quieres asegurar un ingreso pasivo que crezca mientras te enfocas en tu trabajo actual o disfrutas tu vida.
                    </p>
                    <ul class="path-benefits">
                        <li>Asegura ingresos para tu retiro</li>
                        <li>Cero presión por ventas</li>
                        <li>Crecimiento orgánico automático</li>
                        <li>Perfecto para profesionales ocupados</li>
                        <li>Diversificación de ingresos pasivos</li>
                    </ul>
                </div>

                <div class="or-divider">O</div>

                <div class="path-card entrepreneur">
                    <div class="path-icon">💼</div>
                    <h3>El Constructor de Imperios</h3>
                    <p>
                        Para emprendedores ambiciosos. Quieres maximizar esta plataforma como un negocio escalable completo, similar a ser influencer pero con mejor monetización.
                    </p>
                    <ul class="path-benefits">
                        <li>Ingresos ilimitados escalables</li>
                        <li>Marketing de influencer integrado</li>
                        <li>6 formas de ganar dinero</li>
                        <li>Equipo y comunidad global</li>
                        <li>Libertad financiera total</li>
                    </ul>
                </div>
            </div>

            <div class="highlight-box" style="max-width: 800px; margin: 3rem auto 0; text-align: center;">
                <p style="text-align: center; font-style: normal; font-weight: 600; color: var(--dark-green);">
                    "Ya sea que quieras tranquilidad financiera para tu vejez o construir un imperio hoy, LiveGood tiene el sistema para ti. La membresía es la misma, las posibilidades son infinitas."
                </p>
            </div>
        </div>
    </section>

    <!-- Final CTA -->
    <section class="final-cta">
        <div class="container">
            <h2>El Momento es AHORA</h2>
            <p>Cada día que pasa es una oportunidad perdida. Las posiciones se llenan rápidamente.<br>
            <strong>No dejes que esta oportunidad pase frente a tus ojos.</strong></p>
            
            <a href="https://livegoodtour.com/Lifeofnena" class="btn btn-dark">
                🚀 Quiero Asegurar Mi Lugar Gratis Ahora
            </a>
            
            <div style="margin-top: 2rem;">
                <a href="https://t.me/jaelsidehustle" style="color: var(--black); text-decoration: underline; font-weight: 600;">
                    ¿Tienes dudas? Escríbeme directamente aquí →
                </a>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <p>© 2024 LiveGood Independent Affiliate. Todos los derechos reservados.</p>
        <p style="margin-top: 1rem; font-size: 0.9rem;">
            Esta es una oportunidad de negocio independiente. Los resultados pueden variar según el esfuerzo individual.
        </p>
        <p style="margin-top: 0.5rem; font-size: 0.8rem; color: #444;">
            *Los ingresos pasivos de hasta $2,000/mes representan el máximo potencial sin actividad de marketing según el plan de compensación actual. 
            Los resultados típicos varían. Los ingresos significativos requieren tiempo, consistencia y/o esfuerzo de construcción de red según el camino elegido.
        </p>
    </footer>

    <script>
        // Create floating particles
        function createParticles() {
            const container = document.getElementById('particles');
            for (let i = 0; i < 20; i++) {
                const particle = document.createElement('div');
                particle.className = 'particle';
                particle.style.left = Math.random() * 100 + '%';
                particle.style.animationDelay = Math.random() * 20 + 's';
                particle.style.animationDuration = (15 + Math.random() * 10) + 's';
                container.appendChild(particle);
            }
        }
        createParticles();

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

        // Observe all cards
        document.querySelectorAll('.benefit-card, .path-card').forEach((el) => {
            el.style.opacity = "0";
            el.style.transform = "translateY(20px)";
            el.style.transition = "all 0.6s ease";
            observer.observe(el);
        });
    </script>
</body>
</html>
