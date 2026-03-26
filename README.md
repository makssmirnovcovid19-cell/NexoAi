
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, viewport-fit=cover">
    <title>NexusAI | Платформа искусственного интеллекта</title>
    <meta name="description" content="Платформа нового поколения для бизнеса на основе искусственного интеллекта. Автоматизация, аналитика, генерация контента.">
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:opsz,wght@14..32,300;14..32,400;14..32,500;14..32,600;14..32,700;14..32,800&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Inter', sans-serif;
            background: #FFFFFF;
            color: #111827;
            overflow-x: hidden;
        }

        html {
            scroll-behavior: smooth;
        }

        /* Custom cursor */
        .cursor {
            width: 8px;
            height: 8px;
            background: #3B82F6;
            border-radius: 50%;
            position: fixed;
            pointer-events: none;
            z-index: 9999;
            transition: transform 0.1s;
        }

        .cursor-follower {
            width: 40px;
            height: 40px;
            border: 2px solid rgba(59, 130, 246, 0.3);
            border-radius: 50%;
            position: fixed;
            pointer-events: none;
            z-index: 9998;
            transition: transform 0.15s;
        }

        @media (max-width: 768px) {
            .cursor, .cursor-follower { display: none; }
        }

        .container {
            max-width: 1280px;
            margin: 0 auto;
            padding: 0 48px;
        }

        @media (max-width: 768px) {
            .container {
                padding: 0 24px;
            }
        }

        /* Navigation */
        nav {
            position: fixed;
            top: 0;
            left: 0;
            right: 0;
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(20px);
            border-bottom: 1px solid rgba(0, 0, 0, 0.05);
            z-index: 1000;
            padding: 20px 0;
            transition: all 0.3s;
        }

        .nav-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-size: 28px;
            font-weight: 800;
            letter-spacing: -0.02em;
            background: linear-gradient(135deg, #1E293B 0%, #3B82F6 100%);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            cursor: pointer;
        }

        .nav-links {
            display: flex;
            gap: 48px;
            align-items: center;
        }

        .nav-links a {
            text-decoration: none;
            color: #334155;
            font-weight: 500;
            transition: color 0.2s;
            font-size: 15px;
            cursor: pointer;
        }

        .nav-links a:hover {
            color: #3B82F6;
        }

        .btn-nav {
            background: #0F172A;
            color: white;
            padding: 10px 28px;
            border-radius: 100px;
            font-weight: 600;
            border: none;
            cursor: pointer;
            transition: all 0.2s;
            font-size: 14px;
        }

        .btn-nav:hover {
            background: #1E293B;
            transform: translateY(-2px);
        }

        .mobile-menu-btn {
            display: none;
            font-size: 24px;
            cursor: pointer;
            color: #0F172A;
        }

        @media (max-width: 768px) {
            .nav-links {
                display: none;
            }
            .mobile-menu-btn {
                display: block;
            }
        }

        /* Hero Section */
        .hero {
            padding: 180px 0 100px;
            position: relative;
            overflow: hidden;
        }

        .hero-badge {
            display: inline-block;
            padding: 6px 16px;
            background: rgba(59, 130, 246, 0.1);
            border-radius: 100px;
            color: #3B82F6;
            font-weight: 600;
            font-size: 14px;
            margin-bottom: 32px;
            backdrop-filter: blur(10px);
        }

        .hero h1 {
            font-size: 72px;
            font-weight: 800;
            line-height: 1.1;
            letter-spacing: -0.02em;
            margin-bottom: 32px;
            max-width: 900px;
        }

        .gradient-text {
            background: linear-gradient(135deg, #3B82F6, #8B5CF6, #EC489A);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
        }

        .hero p {
            font-size: 18px;
            color: #5B6E8C;
            line-height: 1.6;
            max-width: 600px;
            margin-bottom: 48px;
        }

        .hero-buttons {
            display: flex;
            gap: 20px;
            flex-wrap: wrap;
            margin-bottom: 80px;
        }

        .btn-primary {
            background: #0F172A;
            color: white;
            padding: 14px 36px;
            border-radius: 100px;
            font-weight: 600;
            border: none;
            cursor: pointer;
            transition: all 0.3s;
            font-size: 16px;
        }

        .btn-primary:hover {
            background: #1E293B;
            transform: translateY(-3px);
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
        }

        .btn-outline {
            background: transparent;
            border: 2px solid #E2E8F0;
            padding: 14px 36px;
            border-radius: 100px;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s;
            font-size: 16px;
        }

        .btn-outline:hover {
            border-color: #3B82F6;
            background: rgba(59, 130, 246, 0.05);
        }

        .stats {
            display: flex;
            gap: 60px;
            flex-wrap: wrap;
            border-top: 1px solid #EFF3F8;
            padding-top: 60px;
        }

        .stat-item h3 {
            font-size: 40px;
            font-weight: 800;
            margin-bottom: 8px;
        }

        .stat-item p {
            font-size: 14px;
            color: #6C7281;
            margin: 0;
        }

        .grid-bg {
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background-image: 
                linear-gradient(rgba(59, 130, 246, 0.03) 1px, transparent 1px),
                linear-gradient(90deg, rgba(59, 130, 246, 0.03) 1px, transparent 1px);
            background-size: 50px 50px;
            pointer-events: none;
        }

        /* Features Section */
        .features {
            padding: 100px 0;
            background: #F8FAFE;
            scroll-margin-top: 80px;
        }

        .section-title {
            text-align: center;
            margin-bottom: 80px;
        }

        .section-title h2 {
            font-size: 48px;
            font-weight: 800;
            margin-bottom: 20px;
        }

        .section-title p {
            font-size: 18px;
            color: #5B6E8C;
            max-width: 600px;
            margin: 0 auto;
        }

        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 32px;
        }

        .feature-card {
            background: white;
            border-radius: 32px;
            padding: 40px;
            transition: all 0.3s;
            border: 1px solid #EFF3F8;
            cursor: pointer;
        }

        .feature-card:hover {
            transform: translateY(-8px);
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.08);
            border-color: #E2E8F0;
        }

        .feature-icon {
            width: 64px;
            height: 64px;
            background: linear-gradient(135deg, #EEF2FF, #FAF5FF);
            border-radius: 20px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 28px;
            color: #3B82F6;
            margin-bottom: 32px;
        }

        .feature-card h3 {
            font-size: 24px;
            font-weight: 700;
            margin-bottom: 16px;
        }

        .feature-card p {
            color: #5B6E8C;
            line-height: 1.6;
        }

        /* Pricing Section */
        .pricing {
            padding: 100px 0;
            scroll-margin-top: 80px;
        }

        .pricing-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
            gap: 32px;
            max-width: 1100px;
            margin: 0 auto;
        }

        .pricing-card {
            background: white;
            border-radius: 40px;
            padding: 48px 40px;
            border: 1px solid #EFF3F8;
            transition: all 0.3s;
            position: relative;
            display: flex;
            flex-direction: column;
        }

        .pricing-card.popular {
            border: 2px solid #3B82F6;
            box-shadow: 0 20px 40px rgba(59, 130, 246, 0.1);
        }

        .popular-badge {
            position: absolute;
            top: -12px;
            left: 50%;
            transform: translateX(-50%);
            background: #3B82F6;
            color: white;
            padding: 4px 16px;
            border-radius: 100px;
            font-size: 12px;
            font-weight: 600;
            white-space: nowrap;
        }

        .pricing-card h3 {
            font-size: 28px;
            font-weight: 700;
            margin-bottom: 16px;
        }

        .price {
            font-size: 48px;
            font-weight: 800;
            margin: 32px 0;
            line-height: 1.2;
            word-break: break-word;
        }

        .price span {
            font-size: 16px;
            font-weight: 500;
            color: #6C7281;
        }

        .price-individual {
            font-size: 32px;
            font-weight: 700;
            margin: 32px 0;
            color: #3B82F6;
            line-height: 1.2;
        }

        .pricing-features {
            list-style: none;
            margin: 32px 0;
            flex-grow: 1;
        }

        .pricing-features li {
            padding: 12px 0;
            display: flex;
            align-items: center;
            gap: 12px;
            color: #334155;
        }

        .pricing-features i {
            color: #10B981;
            flex-shrink: 0;
        }

        .btn-price {
            width: 100%;
            padding: 14px;
            border-radius: 100px;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s;
            margin-top: auto;
        }

        /* Resources Section */
        .resources {
            padding: 100px 0;
            background: #F8FAFE;
            scroll-margin-top: 80px;
        }

        .resources-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 32px;
            margin-top: 48px;
        }

        .resource-card {
            background: white;
            border-radius: 28px;
            padding: 32px;
            transition: all 0.3s;
            cursor: pointer;
        }

        .resource-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.08);
        }

        .resource-icon {
            font-size: 40px;
            color: #3B82F6;
            margin-bottom: 20px;
        }

        .resource-card h3 {
            font-size: 20px;
            font-weight: 700;
            margin-bottom: 12px;
        }

        .resource-card p {
            color: #5B6E8C;
            line-height: 1.5;
        }

        /* CTA Section */
        .cta {
            background: linear-gradient(135deg, #0F172A 0%, #1E293B 100%);
            margin: 60px 48px;
            border-radius: 48px;
            padding: 80px 60px;
            text-align: center;
            position: relative;
            overflow: hidden;
        }

        .cta h2 {
            font-size: 48px;
            font-weight: 800;
            color: white;
            margin-bottom: 24px;
        }

        .cta p {
            font-size: 18px;
            color: rgba(255, 255, 255, 0.7);
            max-width: 600px;
            margin: 0 auto 40px;
        }

        .cta-buttons {
            display: flex;
            gap: 20px;
            justify-content: center;
            flex-wrap: wrap;
        }

        .btn-white {
            background: white;
            color: #0F172A;
            padding: 14px 36px;
            border-radius: 100px;
            font-weight: 600;
            border: none;
            cursor: pointer;
            transition: all 0.3s;
        }

        .btn-white:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 30px rgba(255, 255, 255, 0.2);
        }

        /* Modal */
        .modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.8);
            backdrop-filter: blur(8px);
            z-index: 10000;
            align-items: center;
            justify-content: center;
        }

        .modal.active {
            display: flex;
        }

        .modal-content {
            background: white;
            border-radius: 32px;
            padding: 48px;
            max-width: 500px;
            width: 90%;
            text-align: center;
            animation: modalSlideIn 0.4s ease forwards;
        }

        @keyframes modalSlideIn {
            from {
                transform: scale(0.9);
                opacity: 0;
            }
            to {
                transform: scale(1);
                opacity: 1;
            }
        }

        .modal-icon {
            width: 80px;
            height: 80px;
            background: linear-gradient(135deg, #EEF2FF, #FAF5FF);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 0 auto 24px;
            font-size: 40px;
            color: #3B82F6;
        }

        .modal h3 {
            font-size: 28px;
            font-weight: 700;
            margin-bottom: 16px;
        }

        .modal p {
            color: #5B6E8C;
            margin-bottom: 32px;
            line-height: 1.6;
        }

        .modal-close {
            background: #0F172A;
            color: white;
            padding: 12px 32px;
            border-radius: 100px;
            border: none;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s;
        }

        .modal-close:hover {
            background: #1E293B;
            transform: translateY(-2px);
        }

        /* Footer */
        footer {
            background: #F8FAFE;
            padding: 80px 0 40px;
            margin-top: 60px;
        }

        .footer-grid {
            display: grid;
            grid-template-columns: 2fr 1fr 1fr 1fr;
            gap: 60px;
            margin-bottom: 60px;
        }

        .footer-col h4 {
            font-size: 18px;
            font-weight: 700;
            margin-bottom: 24px;
        }

        .footer-col p, .footer-col a {
            color: #5B6E8C;
            text-decoration: none;
            display: block;
            margin: 12px 0;
            font-size: 14px;
            transition: color 0.2s;
            cursor: pointer;
        }

        .footer-col a:hover {
            color: #3B82F6;
        }

        .social-icons {
            display: flex;
            gap: 20px;
            margin-top: 20px;
        }

        .social-icons i {
            font-size: 20px;
            cursor: pointer;
            transition: color 0.2s;
        }

        .social-icons i:hover {
            color: #3B82F6;
        }

        .copyright {
            text-align: center;
            padding-top: 40px;
            border-top: 1px solid #E4E7EC;
            color: #6C7281;
            font-size: 14px;
        }

        @media (max-width: 768px) {
            .footer-grid {
                grid-template-columns: 1fr;
                gap: 40px;
            }
            .hero h1 {
                font-size: 40px;
            }
            .features-grid {
                grid-template-columns: 1fr;
            }
            .section-title h2 {
                font-size: 32px;
            }
            .pricing-grid {
                grid-template-columns: 1fr;
                gap: 48px;
            }
            .cta {
                margin: 40px 24px;
                padding: 60px 32px;
            }
            .cta h2 {
                font-size: 32px;
            }
        }

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

        .fade-up {
            animation: fadeInUp 0.8s ease forwards;
        }
    </style>
</head>
<body>

<!-- Custom cursor -->
<div class="cursor"></div>
<div class="cursor-follower"></div>

<!-- Navigation -->
<nav>
    <div class="container nav-container">
        <div class="logo" onclick="scrollToSection('hero')">NEXUS<span style="color: #3B82F6;">AI</span></div>
        <div class="nav-links">
            <a onclick="scrollToSection('features')">Платформа</a>
            <a onclick="scrollToSection('features')">Возможности</a>
            <a onclick="scrollToSection('pricing')">Тарифы</a>
            <a onclick="scrollToSection('resources')">Ресурсы</a>
            <button class="btn-nav" onclick="openModal('Начать работу', 'Зарегистрируйтесь сейчас и получите бесплатный 14-дневный доступ ко всем функциям платформы.')">Начать</button>
        </div>
        <div class="mobile-menu-btn" onclick="showMobileMenu()">
            <i class="fas fa-bars"></i>
        </div>
    </div>
</nav>

<!-- Hero Section -->
<section class="hero" id="hero">
    <div class="grid-bg"></div>
    <div class="container">
        <div class="hero-badge fade-up">✨ Искусственный интеллект 2.0</div>
        <h1 class="fade-up">Будущее <span class="gradient-text">бизнеса</span><br>начинается сегодня</h1>
        <p class="fade-up">Автоматизируйте рутину, увеличивайте прибыль и принимайте решения на основе данных с помощью передовых AI-технологий.</p>
        <div class="hero-buttons fade-up">
            <button class="btn-primary" onclick="openModal('Начните бесплатно', 'Вы получите доступ к 14-дневному пробному периоду. Письмо с инструкциями отправлено на ваш email.')">Начать бесплатно →</button>
            <button class="btn-outline" onclick="openModal('Демо-презентация', 'Запишитесь на индивидуальную демонстрацию платформы. Наш специалист покажет все возможности в удобное для вас время.')">Смотреть демо</button>
        </div>
        <div class="stats fade-up">
            <div class="stat-item">
                <h3>5000+</h3>
                <p>активных клиентов</p>
            </div>
            <div class="stat-item">
                <h3>98%</h3>
                <p>точности прогнозов</p>
            </div>
            <div class="stat-item">
                <h3>24/7</h3>
                <p>AI-поддержка</p>
            </div>
            <div class="stat-item">
                <h3>120+</h3>
                <p>нейросетей</p>
            </div>
        </div>
    </div>
</section>

<!-- Features Section -->
<section class="features" id="features">
    <div class="container">
        <div class="section-title">
            <h2>Всё необходимое для <span class="gradient-text">AI-трансформации</span></h2>
            <p>Мощные инструменты, которые работают вместе, чтобы вывести ваш бизнес на новый уровень</p>
        </div>
        <div class="features-grid">
            <div class="feature-card" onclick="openModal('Генерация контента', 'Создавайте статьи, посты, видео-сценарии и email-рассылки в 10 раз быстрее с помощью LLM нового поколения. Доступно на 50+ языках.')">
                <div class="feature-icon"><i class="fas fa-brain"></i></div>
                <h3>Генерация контента</h3>
                <p>Создавайте статьи, посты, видео-сценарии и email-рассылки в 10 раз быстрее с помощью LLM нового поколения.</p>
            </div>
            <div class="feature-card" onclick="openModal('Предиктивная аналитика', 'Прогнозируйте продажи, поведение клиентов и рыночные тренды с точностью до 98%. Интеграция с вашими BI-системами.')">
                <div class="feature-icon"><i class="fas fa-chart-line"></i></div>
                <h3>Предиктивная аналитика</h3>
                <p>Прогнозируйте продажи, поведение клиентов и рыночные тренды с точностью до 98%.</p>
            </div>
            <div class="feature-card" onclick="openModal('AI-агенты 24/7', 'Умные чат-боты, которые обрабатывают 80% запросов без участия человека. Поддержка по всем каналам связи.')">
                <div class="feature-icon"><i class="fas fa-robot"></i></div>
                <h3>AI-агенты 24/7</h3>
                <p>Умные чат-боты, которые обрабатывают 80% запросов без участия человека.</p>
            </div>
            <div class="feature-card" onclick="openModal('Нейродизайн', 'Генерация уникальных изображений, логотипов и креативов под ваш бренд за секунды. Экономия до 80% бюджета на дизайн.')">
                <div class="feature-icon"><i class="fas fa-palette"></i></div>
                <h3>Нейродизайн</h3>
                <p>Генерация уникальных изображений, логотипов и креативов под ваш бренд за секунды.</p>
            </div>
            <div class="feature-card" onclick="openModal('API интеграции', 'Подключайте AI к вашим CRM, ERP и сайтам через простой REST API. Полная документация и SDK для Python, JS, PHP.')">
                <div class="feature-icon"><i class="fas fa-code"></i></div>
                <h3>API интеграции</h3>
                <p>Подключайте AI к вашим CRM, ERP и сайтам через простой REST API.</p>
            </div>
            <div class="feature-card" onclick="openModal('Безопасность данных', 'Шифрование end-to-end, выбор региона хранения данных, сертификация ISO 27001 и полное соответствие GDPR.')">
                <div class="feature-icon"><i class="fas fa-shield-alt"></i></div>
                <h3>Безопасность данных</h3>
                <p>Шифрование end-to-end, выбор региона хранения и полное соответствие GDPR.</p>
            </div>
        </div>
    </div>
</section>

<!-- Pricing Section -->
<section class="pricing" id="pricing">
    <div class="container">
        <div class="section-title">
            <h2>Выберите <span class="gradient-text">идеальный тариф</span></h2>
            <p>Гибкие условия для бизнеса любого масштаба</p>
        </div>
        <div class="pricing-grid">
            <div class="pricing-card">
                <h3>Старт</h3>
                <div class="price">2 490 ₽ <span>/месяц</span></div>
                <ul class="pricing-features">
                    <li><i class="fas fa-check-circle"></i> До 100 запросов/день</li>
                    <li><i class="fas fa-check-circle"></i> 20 AI моделей</li>
                    <li><i class="fas fa-check-circle"></i> Базовая аналитика</li>
                    <li><i class="fas fa-check-circle"></i> Чат-поддержка</li>
                </ul>
                <button class="btn-outline btn-price" onclick="openModal('Тариф Старт', 'Вы выбрали тариф Старт. Перейдите к оформлению подписки, чтобы получить доступ ко всем возможностям платформы.')">Выбрать тариф</button>
            </div>
            <div class="pricing-card popular">
                <div class="popular-badge">🔥 Популярный</div>
                <h3>Бизнес</h3>
                <div class="price">9 990 ₽ <span>/месяц</span></div>
                <ul class="pricing-features">
                    <li><i class="fas fa-check-circle"></i> Неограниченные запросы</li>
                    <li><i class="fas fa-check-circle"></i> 120+ AI моделей</li>
                    <li><i class="fas fa-check-circle"></i> Расширенная аналитика</li>
                    <li><i class="fas fa-check-circle"></i> Приоритетная поддержка 24/7</li>
                    <li><i class="fas fa-check-circle"></i> API доступ</li>
                </ul>
                <button class="btn-primary btn-price" onclick="openModal('Тариф Бизнес', 'Вы выбрали тариф Бизнес. Перейдите к оформлению подписки и получите полный доступ ко всем функциям платформы.')">Начать сейчас</button>
            </div>
            <div class="pricing-card">
                <h3>Корпоративный</h3>
                <div class="price-individual">Индивидуально</div>
                <ul class="pricing-features">
                    <li><i class="fas fa-check-circle"></i> Выделенный кластер</li>
                    <li><i class="fas fa-check-circle"></i> SLA 99.9%</li>
                    <li><i class="fas fa-check-circle"></i> Кастомизация моделей</li>
                    <li><i class="fas fa-check-circle"></i> Персональный менеджер</li>
                    <li><i class="fas fa-check-circle"></i> SSO интеграция</li>
                </ul>
                <button class="btn-outline btn-price" onclick="openModal('Корпоративный тариф', 'Оставьте заявку, и наш менеджер подготовит индивидуальное предложение с учетом всех ваших потребностей.')">Связаться</button>
            </div>
        </div>
    </div>
</section>

<!-- Resources Section -->
<section class="resources" id="resources">
    <div class="container">
        <div class="section-title">
            <h2>Полезные <span class="gradient-text">ресурсы</span></h2>
            <p>Узнайте больше об искусственном интеллекте и его возможностях</p>
        </div>
        <div class="resources-grid">
            <div class="resource-card" onclick="openModal('Блог NexusAI', 'Читайте свежие статьи о трендах AI, кейсы внедрения и практические руководства. Обновляется еженедельно.')">
                <div class="resource-icon"><i class="fas fa-blog"></i></div>
                <h3>Блог</h3>
                <p>Свежие статьи, кейсы и новости из мира искусственного интеллекта</p>
            </div>
            <div class="resource-card" onclick="openModal('Академия AI', 'Бесплатные курсы и вебинары по внедрению AI в бизнес. Сертификаты после прохождения.')">
                <div class="resource-icon"><i class="fas fa-graduation-cap"></i></div>
                <h3>Академия AI</h3>
                <p>Обучающие материалы, вебинары и руководства по работе с платформой</p>
            </div>
            <div class="resource-card" onclick="openModal('Кейсы клиентов', 'Реальные истории успеха наших клиентов. Узнайте, как компании увеличили прибыль с помощью AI.')">
                <div class="resource-icon"><i class="fas fa-chart-line"></i></div>
                <h3>Кейсы</h3>
                <p>Реальные истории успеха и примеры внедрения AI в различных отраслях</p>
            </div>
            <div class="resource-card" onclick="openModal('Поддержка', 'Круглосуточная техническая поддержка. Чат, email, телефон — выберите удобный способ связи.')">
                <div class="resource-icon"><i class="fas fa-headset"></i></div>
                <h3>Поддержка</h3>
                <p>Помощь специалистов 24/7. Отвечаем на любые вопросы</p>
            </div>
        </div>
    </div>
</section>

<!-- CTA Section -->
<section class="cta">
    <h2>Готовы к AI-революции?</h2>
    <p>Присоединяйтесь к 5000+ компаний, которые уже увеличили прибыль на 40% с помощью нашей платформы</p>
    <div class="cta-buttons">
        <button class="btn-white" onclick="openModal('Демо-доступ', 'Получите демо-доступ к платформе. Наш менеджер свяжется с вами для уточнения деталей.')">Получить демо-доступ</button>
        <button class="btn-primary" style="background: white; color: #0F172A;" onclick="openModal('Консультация эксперта', 'Эксперт по AI-внедрению свяжется с вами в ближайшее время. Подготовим индивидуальное решение для вашего бизнеса.')">Консультация эксперта</button>
    </div>
</section>

<!-- Footer -->
<footer>
    <div class="container">
        <div class="footer-grid">
            <div class="footer-col">
                <h4 style="font-size: 24px; margin-bottom: 20px;">NEXUS<span style="color: #3B82F6;">AI</span></h4>
                <p>Платформа искусственного интеллекта нового поколения для бизнеса.</p>
                <div class="social-icons">
                    <i class="fab fa-telegram" onclick="openModal('Telegram', 'Присоединяйтесь к нашему Telegram-каналу для получения свежих новостей и обновлений.')"></i>
                    <i class="fab fa-linkedin-in" onclick="openModal('LinkedIn', 'Следите за нами в LinkedIn для профессионального контента и новостей компании.')"></i>
                    <i class="fab fa-x-twitter" onclick="openModal('X (Twitter)', 'Подписывайтесь на наш Twitter для оперативных новостей и анонсов.')"></i>
                    <i class="fab fa-github" onclick="openModal('GitHub', 'Изучайте нашу документацию и open-source инструменты на GitHub.')"></i>
                </div>
            </div>
            <div class="footer-col">
                <h4>Продукт</h4>
                <a onclick="scrollToSection('features')">Возможности</a>
                <a onclick="scrollToSection('pricing')">Тарифы</a>
                <a onclick="openModal('API', 'Мощный REST API для интеграции с вашими системами. Полная документация и примеры кода.')">API</a>
                <a onclick="openModal('Безопасность', 'Сертификация ISO 27001, шифрование данных и полное соответствие требованиям безопасности.')">Безопасность</a>
            </div>
            <div class="footer-col">
                <h4>Ресурсы</h4>
                <a onclick="openModal('Блог', 'Читайте свежие статьи о трендах AI, кейсы внедрения и практические руководства.')">Блог</a>
                <a onclick="openModal('Академия AI', 'Бесплатные курсы и вебинары по внедрению AI в бизнес.')">Академия AI</a>
                <a onclick="openModal('Кейсы', 'Реальные истории успеха наших клиентов в различных отраслях.')">Кейсы</a>
                <a onclick="openModal('Поддержка', 'Круглосуточная техническая поддержка. Чат, email, телефон.')">Поддержка</a>
            </div>
            <div class="footer-col">
                <h4>Контакты</h4>
                <p>hello@nexusai.com</p>
                <p>+7 (495) 123-45-67</p>
                <p>Москва, ул. Тверская, 15</p>
            </div>
        </div>
        <div class="copyright">
            © 2025 NexusAI. Все права защищены.
        </div>
    </div>
</section>

<!-- Modal -->
<div class="modal" id="modal">
    <div class="modal-content">
        <div class="modal-icon">
            <i class="fas fa-check-circle"></i>
        </div>
        <h3 id="modalTitle">Спасибо!</h3>
        <p id="modalText">Мы получили ваш запрос. Наш менеджер свяжется с вами в ближайшее время.</p>
        <button class="modal-close" onclick="closeModal()">Отлично</button>
    </div>
</div>

<script>
    // Modal functions
    function openModal(title, message) {
        const modal = document.getElementById('modal');
        document.getElementById('modalTitle').textContent = title;
        document.getElementById('modalText').textContent = message;
        modal.classList.add('active');
    }

    function closeModal() {
        const modal = document.getElementById('modal');
        modal.classList.remove('active');
    }

    // Close modal on overlay click
    document.getElementById('modal').addEventListener('click', (e) => {
        if (e.target === document.getElementById('modal')) {
            closeModal();
        }
    });

    // Scroll to section function
    function scrollToSection(sectionId) {
        const element = document.getElementById(sectionId);
        if (element) {
            const offset = 80;
            const elementPosition = element.getBoundingClientRect().top;
            const offsetPosition = elementPosition + window.pageYOffset - offset;
            
            window.scrollTo({
                top: offsetPosition,
                behavior: 'smooth'
            });
        }
    }

    // Mobile menu
    function showMobileMenu() {
        openModal('Мобильное меню', 'В полной версии сайта здесь будет адаптивное меню со всеми разделами: Платформа, Возможности, Тарифы, Ресурсы, Личный кабинет.');
    }

    // Custom cursor
    const cursor = document.querySelector('.cursor');
    const cursorFollower = document.querySelector('.cursor-follower');

    if (cursor && cursorFollower) {
        document.addEventListener('mousemove', (e) => {
            cursor.style.left = e.clientX + 'px';
            cursor.style.top = e.clientY + 'px';
            
            setTimeout(() => {
                cursorFollower.style.left = e.clientX - 20 + 'px';
                cursorFollower.style.top = e.clientY - 20 + 'px';
            }, 50);
        });
    }

    // Navbar scroll effect
    window.addEventListener('scroll', () => {
        const nav = document.querySelector('nav');
        if (window.scrollY > 50) {
            nav.style.background = 'rgba(255, 255, 255, 0.95)';
            nav.style.boxShadow = '0 4px 20px rgba(0,0,0,0.05)';
        } else {
            nav.style.background = 'rgba(255, 255, 255, 0.95)';
            nav.style.boxShadow = 'none';
        }
    });

    // Animations on scroll
    const observerOptions = {
        threshold: 0.1,
        rootMargin: '0px 0px -50px 0px'
    };

    const observer = new IntersectionObserver((entries) => {
        entries.forEach(entry => {
            if (entry.isIntersecting) {
                entry.target.style.opacity = '1';
                entry.target.style.transform = 'translateY(0)';
            }
        });
    }, observerOptions);

    document.querySelectorAll('.feature-card, .pricing-card, .resource-card').forEach(el => {
        el.style.opacity = '0';
        el.style.transform = 'translateY(30px)';
        el.style.transition = 'all 0.6s ease';
        observer.observe(el);
    });

