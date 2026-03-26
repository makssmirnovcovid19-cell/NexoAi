<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>NexusAI | Платформа искусственного интеллекта</title>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">
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
        }
        html {
            scroll-behavior: smooth;
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
        }
        .nav-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        .logo {
            font-size: 28px;
            font-weight: 800;
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
            cursor: pointer;
            transition: color 0.2s;
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
        }
        .btn-nav:hover {
            background: #1E293B;
            transform: translateY(-2px);
        }
        .mobile-menu-btn {
            display: none;
            font-size: 24px;
            cursor: pointer;
        }
        @media (max-width: 768px) {
            .nav-links {
                display: none;
            }
            .mobile-menu-btn {
                display: block;
            }
        }
        .hero {
            padding: 180px 0 100px;
            position: relative;
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
        }
        .hero h1 {
            font-size: 72px;
            font-weight: 800;
            line-height: 1.1;
            margin-bottom: 32px;
            max-width: 900px;
        }
        @media (max-width: 768px) {
            .hero h1 {
                font-size: 40px;
            }
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
        }
        .btn-primary:hover {
            background: #1E293B;
            transform: translateY(-3px);
        }
        .btn-outline {
            background: transparent;
            border: 2px solid #E2E8F0;
            padding: 14px 36px;
            border-radius: 100px;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s;
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
        }
        .grid-bg {
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background-image: linear-gradient(rgba(59, 130, 246, 0.03) 1px, transparent 1px), linear-gradient(90deg, rgba(59, 130, 246, 0.03) 1px, transparent 1px);
            background-size: 50px 50px;
            pointer-events: none;
        }
        .features {
            padding: 100px 0;
            background: #F8FAFE;
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
        @media (max-width: 768px) {
            .section-title h2 {
                font-size: 32px;
            }
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
        .pricing {
            padding: 100px 0;
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
        .price {
            font-size: 48px;
            font-weight: 800;
            margin: 32px 0;
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
        }
        .btn-price {
            width: 100%;
            padding: 14px;
            border-radius: 100px;
            font-weight: 600;
            cursor: pointer;
            margin-top: auto;
        }
        .resources {
            padding: 100px 0;
            background: #F8FAFE;
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
            cursor: pointer;
            transition: all 0.3s;
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
        .cta {
            background: linear-gradient(135deg, #0F172A 0%, #1E293B 100%);
            margin: 60px 48px;
            border-radius: 48px;
            padding: 80px 60px;
            text-align: center;
        }
        @media (max-width: 768px) {
            .cta {
                margin: 40px 24px;
                padding: 60px 32px;
            }
            .cta h2 {
                font-size: 32px;
            }
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
        }
        .modal-close {
            background: #0F172A;
            color: white;
            padding: 12px 32px;
            border-radius: 100px;
            border: none;
            font-weight: 600;
            cursor: pointer;
        }
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
        @media (max-width: 768px) {
            .footer-grid {
                grid-template-columns: 1fr;
                gap: 40px;
            }
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
        }
        .copyright {
            text-align: center;
            padding-top: 40px;
            border-top: 1px solid #E4E7EC;
            color: #6C7281;
            font-size: 14px;
        }
    </style>
</head>
<body>

<nav>
    <div class="container nav-container">
        <div class="logo" onclick="scrollToTop()">NEXUS<span style="color: #3B82F6;">AI</span></div>
        <div class="nav-links">
            <a onclick="scrollToSection('features')">Платформа</a>
            <a onclick="scrollToSection('pricing')">Тарифы</a>
            <a onclick="scrollToSection('resources')">Ресурсы</a>
            <button class="btn-nav" onclick="openModal('Начать работу', 'Зарегистрируйтесь и получите 14 дней бесплатного доступа.')">Начать</button>
        </div>
        <div class="mobile-menu-btn" onclick="openModal('Меню', 'В полной версии здесь будет адаптивное меню.')">
            <i class="fas fa-bars"></i>
        </div>
    </div>
</nav>

<section class="hero" id="hero">
    <div class="grid-bg"></div>
    <div class="container">
        <div class="hero-badge">✨ Искусственный интеллект 2.0</div>
        <h1>Будущее <span class="gradient-text">бизнеса</span><br>начинается сегодня</h1>
        <p>Автоматизируйте рутину, увеличивайте прибыль и принимайте решения на основе данных.</p>
        <div class="hero-buttons">
            <button class="btn-primary" onclick="openModal('Начните бесплатно', '14 дней бесплатного доступа ко всем функциям.')">Начать бесплатно →</button>
            <button class="btn-outline" onclick="openModal('Демо-презентация', 'Запишитесь на индивидуальную демонстрацию платформы.')">Смотреть демо</button>
        </div>
        <div class="stats">
            <div class="stat-item"><h3>5000+</h3><p>активных клиентов</p></div>
            <div class="stat-item"><h3>98%</h3><p>точности прогнозов</p></div>
            <div class="stat-item"><h3>24/7</h3><p>AI-поддержка</p></div>
            <div class="stat-item"><h3>120+</h3><p>нейросетей</p></div>
        </div>
    </div>
</section>

<section class="features" id="features">
    <div class="container">
        <div class="section-title">
            <h2>Всё для <span class="gradient-text">AI-трансформации</span></h2>
            <p>Мощные инструменты для вашего бизнеса</p>
        </div>
        <div class="features-grid">
            <div class="feature-card" onclick="openModal('Генерация контента', 'Создавайте контент в 10 раз быстрее с помощью AI.')">
                <div class="feature-icon"><i class="fas fa-brain"></i></div>
                <h3>Генерация контента</h3>
                <p>Статьи, посты, сценарии за секунды.</p>
            </div>
            <div class="feature-card" onclick="openModal('Предиктивная аналитика', 'Прогнозируйте продажи с точностью 98%.')">
                <div class="feature-icon"><i class="fas fa-chart-line"></i></div>
                <h3>Предиктивная аналитика</h3>
                <p>Прогнозы и аналитика для бизнеса.</p>
            </div>
            <div class="feature-card" onclick="openModal('AI-агенты 24/7', 'Умные чат-боты без участия человека.')">
                <div class="feature-icon"><i class="fas fa-robot"></i></div>
                <h3>AI-агенты 24/7</h3>
                <p>Автоматическая поддержка клиентов.</p>
            </div>
            <div class="feature-card" onclick="openModal('Нейродизайн', 'Генерация изображений и логотипов.')">
                <div class="feature-icon"><i class="fas fa-palette"></i></div>
                <h3>Нейродизайн</h3>
                <p>Уникальные креативы за секунды.</p>
            </div>
            <div class="feature-card" onclick="openModal('API интеграции', 'Подключайте AI к вашим системам.')">
                <div class="feature-icon"><i class="fas fa-code"></i></div>
                <h3>API интеграции</h3>
                <p>Гибкая настройка под ваш бизнес.</p>
            </div>
            <div class="feature-card" onclick="openModal('Безопасность данных', 'Шифрование и защита данных.')">
                <div class="feature-icon"><i class="fas fa-shield-alt"></i></div>
                <h3>Безопасность данных</h3>
                <p>Соответствие всем стандартам.</p>
            </div>
        </div>
    </div>
</section>

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
                </ul>
                <button class="btn-outline btn-price" onclick="openModal('Тариф Старт', 'Вы выбрали тариф Старт. Перейдите к оформлению.')">Выбрать</button>
            </div>
            <div class="pricing-card popular">
                <div class="popular-badge">🔥 Популярный</div>
                <h3>Бизнес</h3>
                <div class="price">9 990 ₽ <span>/месяц</span></div>
                <ul class="pricing-features">
                    <li><i class="fas fa-check-circle"></i> Неограниченные запросы</li>
                    <li><i class="fas fa-check-circle"></i> 120+ AI моделей</li>
                    <li><i class="fas fa-check-circle"></i> Приоритетная поддержка</li>
                    <li><i class="fas fa-check-circle"></i> API доступ</li>
                </ul>
                <button class="btn-primary btn-price" onclick="openModal('Тариф Бизнес', 'Вы выбрали тариф Бизнес. Получите полный доступ.')">Начать сейчас</button>
            </div>
            <div class="pricing-card">
                <h3>Корпоративный</h3>
                <div class="price-individual">Индивидуально</div>
                <ul class="pricing-features">
                    <li><i class="fas fa-check-circle"></i> Выделенный кластер</li>
                    <li><i class="fas fa-check-circle"></i> SLA 99.9%</li>
                    <li><i class="fas fa-check-circle"></i> Персональный менеджер</li>
                </ul>
                <button class="btn-outline btn-price" onclick="openModal('Корпоративный тариф', 'Оставьте заявку, менеджер подготовит предложение.')">Связаться</button>
            </div>
        </div>
    </div>
</section>

<section class="resources" id="resources">
    <div class="container">
        <div class="section-title">
            <h2>Полезные <span class="gradient-text">ресурсы</span></h2>
            <p>Узнайте больше об искусственном интеллекте</p>
        </div>
        <div class="resources-grid">
            <div class="resource-card" onclick="openModal('Блог', 'Свежие статьи и кейсы по AI.')">
                <div class="resource-icon"><i class="fas fa-blog"></i></div>
                <h3>Блог</h3>
                <p>Статьи и новости из мира AI</p>
            </div>
            <div class="resource-card" onclick="openModal('Академия AI', 'Бесплатные курсы и вебинары.')">
                <div class="resource-icon"><i class="fas fa-graduation-cap"></i></div>
                <h3>Академия AI</h3>
                <p>Обучающие материалы</p>
            </div>
            <div class="resource-card" onclick="openModal('Кейсы', 'Истории успеха клиентов.')">
                <div class="resource-icon"><i class="fas fa-chart-line"></i></div>
                <h3>Кейсы</h3>
                <p>Реальные примеры внедрения</p>
            </div>
        </div>
    </div>
</section>

<div class="cta">
    <h2>Готовы к AI-революции?</h2>
    <p>Присоединяйтесь к 5000+ компаний, которые уже увеличили прибыль</p>
    <div class="cta-buttons">
        <button class="btn-white" onclick="openModal('Демо-доступ', 'Получите демо-доступ к платформе.')">Получить демо</button>
        <button class="btn-primary" style="background: white; color: #0F172A;" onclick="openModal('Консультация', 'Эксперт свяжется с вами.')">Консультация</button>
    </div>
</div>

<footer>
    <div class="container">
        <div class="footer-grid">
            <div class="footer-col">
                <h4>NEXUS<span style="color: #3B82F6;">AI</span></h4>
                <p>Платформа искусственного интеллекта для бизнеса.</p>
                <div class="social-icons">
                    <i class="fab fa-telegram" onclick="openModal('Telegram', 'Присоединяйтесь к нашему каналу.')"></i>
                    <i class="fab fa-linkedin-in" onclick="openModal('LinkedIn', 'Следите за нами в LinkedIn.')"></i>
                </div>
            </div>
            <div class="footer-col">
                <h4>Продукт</h4>
                <a onclick="scrollToSection('features')">Возможности</a>
                <a onclick="scrollToSection('pricing')">Тарифы</a>
                <a onclick="openModal('API', 'Мощный API для интеграций.')">API</a>
            </div>
            <div class="footer-col">
                <h4>Ресурсы</h4>
                <a onclick="openModal('Блог', 'Читайте наш блог.')">Блог</a>
                <a onclick="openModal('Поддержка', '24/7 поддержка клиентов.')">Поддержка</a>
            </div>
            <div class="footer-col">
                <h4>Контакты</h4>
                <p>hello@nexusai.com</p>
                <p>+7 (495) 123-45-67</p>
            </div>
        </div>
        <div class="copyright">© 2025 NexusAI. Все права защищены.</div>
    </div>
</footer>

<div class="modal" id="modal">
    <div class="modal-content">
        <div class="modal-icon"><i class="fas fa-check-circle"></i></div>
        <h3 id="modalTitle">Спасибо!</h3>
        <p id="modalText">Мы свяжемся с вами в ближайшее время.</p>
        <button class="modal-close" onclick="closeModal()">Отлично</button>
    </div>
</div>

<script>
    function openModal(title, message) {
        document.getElementById('modalTitle').innerText = title;
        document.getElementById('modalText').innerText = message;
        document.getElementById('modal').classList.add('active');
    }
    function closeModal() {
        document.getElementById('modal').classList.remove('active');
    }
    document.getElementById('modal').addEventListener('click', function(e) {
        if (e.target === this) closeModal();
    });
    function scrollToSection(id) {
        var el = document.getElementById(id);
        if (el) {
            var offset = 80;
            var pos = el.getBoundingClientRect().top + window.pageYOffset - offset;
            window.scrollTo({ top: pos, behavior: 'smooth' });
        }
    }
    function scrollToTop() {
        window.scrollTo({ top: 0, behavior: 'smooth' });
    }
    var observer = new IntersectionObserver(function(entries) {
        entries.forEach(function(entry) {
            if (entry.isIntersecting) {
                entry.target.style.opacity = '1';
                entry.target.style.transform = 'translateY(0)';
            }
        });
    }, { threshold: 0.1 });
    var elements = document.querySelectorAll('.feature-card, .pricing-card, .resource-card');
    for (var i = 0; i < elements.length; i++) {
        elements[i].style.opacity = '0';
        elements[i].style.transform = 'translateY(30px)';
        elements[i].style.transition = 'all 0.6s ease';
        observer.observe(elements[i]);
    }
</script>
</body>
</html>
