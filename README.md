# B1ting.github.io
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=yes">
    <title>Photo.nn52 | Анна Корочкина - фотограф</title>
    <link href="https://fonts.googleapis.com/css2?family=Inter:opsz,wght@14..32,300;14..32,400;14..32,500;14..32,600;14..32,700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Inter', sans-serif;
            background-color: #faf9f8;
            color: #1e1e2a;
            line-height: 1.5;
        }

        /* Навигация */
        .navbar {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 1.2rem 5%;
            background: white;
            box-shadow: 0 2px 20px rgba(0,0,0,0.05);
            position: sticky;
            top: 0;
            z-index: 100;
            flex-wrap: wrap;
        }

        .logo h1 {
            font-size: 1.6rem;
            font-weight: 600;
            background: linear-gradient(135deg, #2b2b36, #c49a6c);
            background-clip: text;
            -webkit-background-clip: text;
            color: transparent;
        }

        .logo p {
            font-size: 0.7rem;
            color: #7a6e62;
        }

        .nav-links {
            display: flex;
            gap: 2rem;
            list-style: none;
        }

        .nav-links a {
            text-decoration: none;
            font-weight: 500;
            color: #2c2824;
            transition: 0.2s;
            padding: 0.5rem 0;
        }

        .nav-links a:hover, .nav-links a.active {
            color: #c49a6c;
            border-bottom: 2px solid #c49a6c;
        }

        .burger {
            display: none;
            font-size: 1.5rem;
            cursor: pointer;
        }

        /* Hero секция */
        .hero {
            background: linear-gradient(135deg, #f5f0eb 0%, #fff 100%);
            padding: 4rem 5%;
            text-align: center;
        }

        .hero-content h2 {
            font-size: 1.2rem;
            font-weight: 400;
            color: #c49a6c;
            letter-spacing: 2px;
        }

        .hero-content h1 {
            font-size: 3rem;
            margin: 1rem 0;
        }

        .highlight {
            color: #c49a6c;
        }

        .hero-content p {
            max-width: 600px;
            margin: 0 auto 2rem;
            color: #5f554b;
        }

        .hero-buttons {
            display: flex;
            gap: 1rem;
            justify-content: center;
            flex-wrap: wrap;
        }

        .btn {
            padding: 0.8rem 2rem;
            border-radius: 40px;
            text-decoration: none;
            font-weight: 500;
            transition: 0.2s;
            border: none;
            cursor: pointer;
            font-family: 'Inter', sans-serif;
            display: inline-block;
        }

        .btn-primary {
            background: #2c2824;
            color: white;
        }

        .btn-primary:hover {
            background: #c49a6c;
            transform: translateY(-2px);
        }

        .btn-secondary {
            background: transparent;
            color: #2c2824;
            border: 2px solid #2c2824;
        }

        .btn-secondary:hover {
            background: #2c2824;
            color: white;
        }

        .hero-stats {
            display: flex;
            justify-content: center;
            gap: 3rem;
            margin-top: 3rem;
            flex-wrap: wrap;
        }

        .stat {
            text-align: center;
        }

        .stat h3 {
            font-size: 2rem;
            color: #c49a6c;
        }

        .stat p {
            color: #5f554b;
        }

        /* Секция услуг */
        .services {
            padding: 4rem 5%;
            background: white;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        .section-title {
            text-align: center;
            font-size: 2rem;
            margin-bottom: 0.5rem;
        }

        .section-subtitle {
            text-align: center;
            color: #7a6e62;
            margin-bottom: 2rem;
        }

        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            margin-top: 2rem;
        }

        .service-card {
            text-align: center;
            padding: 2rem;
            background: #faf9f8;
            border-radius: 20px;
            transition: 0.3s;
        }

        .service-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
        }

        .service-card i {
            font-size: 2.5rem;
            color: #c49a6c;
            margin-bottom: 1rem;
        }

        .service-card h3 {
            margin-bottom: 0.5rem;
        }

        /* Форма заявки */
        .request-section {
            padding: 4rem 5%;
            background: linear-gradient(135deg, #2c2824, #3a332c);
            color: white;
        }

        .booking-form {
            max-width: 600px;
            margin: 0 auto;
            background: white;
            padding: 2rem;
            border-radius: 20px;
            color: #1e1e2a;
        }

        .form-group {
            margin-bottom: 1rem;
        }

        .form-group input, .form-group select, .form-group textarea {
            width: 100%;
            padding: 0.8rem;
            border: 1px solid #ddd;
            border-radius: 12px;
            font-family: 'Inter', sans-serif;
            font-size: 1rem;
        }

        .btn-submit {
            width: 100%;
            background: #c49a6c;
        }

        .btn-submit:hover {
            background: #a87b4e;
        }

        .form-note {
            font-size: 0.7rem;
            text-align: center;
            margin-top: 1rem;
            color: #999;
        }

        .form-success {
            text-align: center;
            margin-top: 1rem;
            padding: 1rem;
            background: #4caf50;
            color: white;
            border-radius: 12px;
        }

        .hidden {
            display: none;
        }

        /* Портфолио */
        .portfolio-section {
            padding: 3rem 5%;
            background: #faf9f8;
        }

        .filter-buttons {
            display: flex;
            justify-content: center;
            gap: 0.8rem;
            flex-wrap: wrap;
            margin-bottom: 2rem;
        }

        .filter-btn {
            padding: 0.5rem 1.5rem;
            border: 1px solid #ddd;
            background: white;
            border-radius: 40px;
            cursor: pointer;
            transition: 0.2s;
            font-family: 'Inter', sans-serif;
        }

        .filter-btn.active, .filter-btn:hover {
            background: #c49a6c;
            color: white;
            border-color: #c49a6c;
        }

        .portfolio-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 1.5rem;
        }

        .portfolio-item {
            position: relative;
            border-radius: 16px;
            overflow: hidden;
            cursor: pointer;
            aspect-ratio: 4/3;
        }

        .portfolio-item img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: 0.3s;
        }

        .portfolio-item:hover img {
            transform: scale(1.05);
        }

        .portfolio-overlay {
            position: absolute;
            bottom: 0;
            left: 0;
            right: 0;
            background: linear-gradient(to top, rgba(0,0,0,0.7), transparent);
            padding: 1rem;
            color: white;
            opacity: 0;
            transition: 0.2s;
        }

        .portfolio-item:hover .portfolio-overlay {
            opacity: 1;
        }

        /* Отзывы */
        .reviews-section {
            padding: 3rem 5%;
            background: white;
        }

        .reviews-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(320px, 1fr));
            gap: 2rem;
        }

        .review-card {
            background: #faf9f8;
            padding: 1.5rem;
            border-radius: 20px;
            box-shadow: 0 5px 20px rgba(0,0,0,0.05);
        }

        .review-stars {
            color: #ffc107;
            margin-bottom: 1rem;
        }

        .review-text {
            font-style: italic;
            margin-bottom: 1rem;
            color: #555;
            line-height: 1.6;
        }

        .review-author h4 {
            color: #c49a6c;
        }

        .review-author span {
            font-size: 0.8rem;
            color: #999;
        }

        /* Контакты */
        .contacts-section {
            padding: 3rem 5%;
            background: #faf9f8;
        }

        .contacts-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 2rem;
        }

        .contact-card {
            display: flex;
            align-items: center;
            gap: 1rem;
            padding: 1rem;
            background: white;
            border-radius: 16px;
            margin-bottom: 1rem;
            box-shadow: 0 2px 10px rgba(0,0,0,0.05);
        }

        .contact-card i {
            font-size: 2rem;
            color: #c49a6c;
        }

        .contact-card a {
            text-decoration: none;
            color: #2c2824;
            font-weight: 500;
        }

        .contact-card a:hover {
            color: #c49a6c;
        }

        .contact-card p {
            color: #7a6e62;
            font-size: 0.9rem;
        }

        .contact-form-wrapper {
            background: white;
            padding: 2rem;
            border-radius: 20px;
            box-shadow: 0 2px 10px rgba(0,0,0,0.05);
        }

        .contact-form-wrapper h3 {
            margin-bottom: 1rem;
            color: #2c2824;
        }

        .direct-form input, .direct-form textarea {
            width: 100%;
            padding: 0.8rem;
            margin-bottom: 1rem;
            border: 1px solid #ddd;
            border-radius: 12px;
            font-family: 'Inter', sans-serif;
        }

        /* Модальное окно */
        .modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0,0,0,0.9);
            z-index: 1000;
            justify-content: center;
            align-items: center;
        }

        .modal.active {
            display: flex;
        }

        .modal-content {
            max-width: 90%;
            max-height: 90%;
            border-radius: 12px;
        }

        .close-modal {
            position: absolute;
            top: 20px;
            right: 30px;
            font-size: 2rem;
            color: white;
            cursor: pointer;
            background: rgba(0,0,0,0.5);
            width: 40px;
            height: 40px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
        }

        .close-modal:hover {
            background: #c49a6c;
        }

        .modal-caption {
            position: absolute;
            bottom: 20px;
            left: 0;
            right: 0;
            text-align: center;
            color: white;
            background: rgba(0,0,0,0.5);
            padding: 0.5rem 1rem;
            width: fit-content;
            margin: 0 auto;
            border-radius: 20px;
        }

        /* Footer */
        footer {
            background: #2c2824;
            color: white;
            padding: 2rem 1rem 1rem;
        }

        .footer-content {
            max-width: 1200px;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
            gap: 1rem;
        }

        .footer-social a {
            color: white;
            font-size: 1.5rem;
            margin-left: 1rem;
            transition: 0.2s;
        }

        .footer-social a:hover {
            color: #c49a6c;
        }

        .footer-bottom {
            text-align: center;
            padding-top: 1rem;
            margin-top: 1rem;
            border-top: 1px solid #444;
        }

        /* Адаптив */
        @media (max-width: 768px) {
            .burger {
                display: block;
            }
            
            .nav-links {
                display: none;
                width: 100%;
                flex-direction: column;
                text-align: center;
                padding: 1rem 0;
            }
            
            .nav-links.active {
                display: flex;
            }
            
            .hero-content h1 {
                font-size: 2rem;
            }
            
            .services-grid {
                grid-template-columns: 1fr;
            }
            
            .contacts-grid {
                grid-template-columns: 1fr;
            }
            
            .reviews-grid {
                grid-template-columns: 1fr;
            }
        }

        /* Секции навигации по страницам */
        .page {
            display: none;
        }
        
        .page.active-page {
            display: block;
        }
    </style>
</head>
<body>

<nav class="navbar">
    <div class="logo">
        <h1>Photo.nn52</h1>
        <p>Анна Корочкина</p>
    </div>
    <ul class="nav-links">
        <li><a href="#" data-page="home" class="active">Главная</a></li>
        <li><a href="#" data-page="portfolio">Портфолио</a></li>
        <li><a href="#" data-page="reviews">Отзывы</a></li>
        <li><a href="#" data-page="contacts">Контакты</a></li>
    </ul>
    <div class="burger">
        <i class="fas fa-bars"></i>
    </div>
</nav>

<!-- Главная страница -->
<div id="home-page" class="page active-page">
    <section class="hero">
        <div class="hero-content">
            <h2>Анна Корочкина</h2>
            <h1>Фотограф, который <span class="highlight">видит душу</span></h1>
            <p>Создаю кадры, которые живут вечно. Ваши эмоции, любовь и счастье — в каждом снимке.</p>
            <div class="hero-buttons">
                <a href="#" class="btn btn-primary" data-page="portfolio">Смотреть работы</a>
                <a href="#request-form" class="btn btn-secondary">Оставить заявку</a>
            </div>
        </div>
        <div class="hero-stats">
            <div class="stat">
                <h3>150+</h3>
                <p>Счастливых клиентов</p>
            </div>
            <div class="stat">
                <h3>5+</h3>
                <p>Лет опыта</p>
            </div>
            <div class="stat">
                <h3>20+</h3>
                <p>Локаций</p>
            </div>
        </div>
    </section>

    <section class="services">
        <div class="container">
            <h2 class="section-title">Что я предлагаю</h2>
            <div class="services-grid">
                <div class="service-card">
                    <i class="fas fa-camera-retro"></i>
                    <h3>Портретная съёмка</h3>
                    <p>Индивидуальные фотосессии, подчеркивающие вашу уникальность</p>
                </div>
                <div class="service-card">
                    <i class="fas fa-heart"></i>
                    <h3>Love Story</h3>
                    <p>Романтические истории для пар и семейные фотосессии</p>
                </div>
                <div class="service-card">
                    <i class="fas fa-ring"></i>
                    <h3>Свадебная съёмка</h3>
                    <p>Самый важный день в красивых и живых кадрах</p>
                </div>
                <div class="service-card">
                    <i class="fas fa-image"></i>
                    <h3>Репортаж</h3>
                    <p>Мероприятия, праздники и важные события</p>
                </div>
            </div>
        </div>
    </section>

    <section id="request-form" class="request-section">
        <div class="container">
            <h2 class="section-title">Записаться на фотосессию</h2>
            <p class="section-subtitle">Оставьте заявку, и я свяжусь с вами в ближайшее время</p>
            <form id="bookingForm" class="booking-form">
                <div class="form-group">
                    <input type="text" id="name" placeholder="Ваше имя" required>
                </div>
                <div class="form-group">
                    <input type="tel" id="phone" placeholder="Номер телефона" required>
                </div>
                <div class="form-group">
                    <select id="service">
                        <option value="">Выберите тип съёмки</option>
                        <option value="portrait">Портретная</option>
                        <option value="love">Love Story</option>
                        <option value="wedding">Свадебная</option>
                        <option value="event">Репортаж/Мероприятие</option>
                    </select>
                </div>
                <div class="form-group">
                    <textarea id="message" rows="3" placeholder="Ваши пожелания (дата, место, идеи...)"></textarea>
                </div>
                <button type="submit" class="btn btn-primary btn-submit">Отправить заявку</button>
                <p class="form-note">Нажимая на кнопку, вы соглашаетесь с обработкой данных</p>
            </form>
            <div id="formSuccess" class="form-success hidden">
                <i class="fas fa-check-circle"></i>
                <p>Спасибо! Ваша заявка отправлена. Я свяжусь с вами в ближайшее время.</p>
            </div>
        </div>
    </section>
</div>

<!-- Портфолио страница -->
<div id="portfolio-page" class="page">
    <section class="hero" style="padding: 2rem 5%;">
        <div class="hero-content">
            <h2>Мои работы</h2>
            <h1>Портфолио</h1>
            <p>Вдохновение в каждом кадре</p>
        </div>
    </section>
    <section class="portfolio-section">
        <div class="container">
            <div class="filter-buttons">
                <button class="filter-btn active" data-filter="all">Все работы</button>
                <button class="filter-btn" data-filter="portrait">Портрет</button>
                <button class="filter-btn" data-filter="love">Love Story</button>
                <button class="filter-btn" data-filter="wedding">Свадьба</button>
                <button class="filter-btn" data-filter="event">Репортаж</button>
            </div>
            <div class="portfolio-grid" id="portfolioGrid"></div>
        </div>
    </section>
</div>

<!-- Отзывы страница -->
<div id="reviews-page" class="page">
    <section class="hero" style="padding: 2rem 5%;">
        <div class="hero-content">
            <h2>Что говорят клиенты</h2>
            <h1>Отзывы</h1>
            <p>Спасибо каждому, кто доверил мне свои моменты</p>
        </div>
    </section>
    <section class="reviews-section">
        <div class="container">
            <div class="reviews-grid" id="reviewsGrid"></div>
        </div>
    </section>
</div>

<!-- Контакты страница -->
<div id="contacts-page" class="page">
    <section class="hero" style="padding: 2rem 5%;">
        <div class="hero-content">
            <h2>Свяжитесь со мной</h2>
            <h1>Контакты</h1>
            <p>Я всегда на связи и рада новым проектам</p>
        </div>
    </section>
    <section class="contacts-section">
        <div class="container">
            <div class="contacts-grid">
                <div class="contact-info">
                    <div class="contact-card">
                        <i class="fas fa-phone-alt"></i>
                        <div>
                            <h3>Телефон</h3>
                            <a href="tel:89965640578">8 (996) 564-05-78</a>
                        </div>
                    </div>
                    <div class="contact-card">
                        <i class="fab fa-instagram"></i>
                        <div>
                            <h3>Instagram</h3>
                            <a href="https://instagram.com/photo.nn52" target="_blank">@photo.nn52</a>
                        </div>
                    </div>
                    <div class="contact-card">
                        <i class="fab fa-vk"></i>
                        <div>
                            <h3>ВКонтакте</h3>
                            <a href="https://vk.com/korochkina9" target="_blank">@korochkina9</a>
                        </div>
                    </div>
                    <div class="contact-card">
                        <i class="fas fa-map-marker-alt"></i>
                        <div>
                            <h3>Работаю по всей России</h3>
                            <p>Выезд в любую точку, съёмка в студии и на локациях</p>
                        </div>
                    </div>
                </div>
                <div class="contact-form-wrapper">
                    <h3>Напишите мне</h3>
                    <form id="directMessageForm" class="direct-form">
                        <input type="text" placeholder="Ваше имя" id="msgName" required>
                        <input type="tel" placeholder="Ваш телефон" id="msgPhone" required>
                        <textarea rows="4" placeholder="Сообщение..." id="msgText" required></textarea>
                        <button type="submit" class="btn btn-primary">Отправить сообщение</button>
                    </form>
                </div>
            </div>
        </div>
    </section>
</div>

<footer>
    <div class="footer-content">
        <div class="footer-info">
            <h3>Photo.nn52</h3>
            <p>Анна Корочкина</p>
            <p>Фотограф с душой и сердцем</p>
        </div>
        <div class="footer-social">
            <a href="https://instagram.com/photo.nn52" target="_blank"><i class="fab fa-instagram"></i></a>
            <a href="https://vk.com/korochkina9" target="_blank"><i class="fab fa-vk"></i></a>
            <a href="tel:89965640578"><i class="fas fa-phone"></i></a>
        </div>
    </div>
    <div class="footer-bottom">
        <p>&copy; 2026 Photo.nn52 | Все права защищены</p>
    </div>
</footer>

<div class="modal" id="imageModal">
    <span class="close-modal">&times;</span>
    <img class="modal-content" id="modalImage">
    <div class="modal-caption" id="modalCaption"></div>
</div>

<script>
    // Данные для портфолио
    const portfolioData = [
        { id: 1, url: "https://images.pexels.com/photos/1181690/pexels-photo-1181690.jpeg?auto=compress&cs=tinysrgb&w=600", title: "Нежный портрет", category: "portrait" },
        { id: 2, url: "https://images.pexels.com/photos/2085998/pexels-photo-2085998.jpeg?auto=compress&cs=tinysrgb&w=600", title: "Горное озеро", category: "portrait" },
        { id: 3, url: "https://images.pexels.com/photos/1024993/pexels-photo-1024993.jpeg?auto=compress&cs=tinysrgb&w=600", title: "Свадебный танец", category: "wedding" },
        { id: 4, url: "https://images.pexels.com/photos/2253871/pexels-photo-2253871.jpeg?auto=compress&cs=tinysrgb&w=600", title: "Творческая студия", category: "portrait" },
        { id: 5, url: "https://images.pexels.com/photos/1680140/pexels-photo-1680140.jpeg?auto=compress&cs=tinysrgb&w=600", title: "Уличная съёмка", category: "portrait" },
        { id: 6, url: "https://images.pexels.com/photos/2253870/pexels-photo-2253870.jpeg?auto=compress&cs=tinysrgb&w=600", title: "Романтический закат", category: "love" },
        { id: 7, url: "https://images.pexels.com/photos/257536/pexels-photo-257536.jpeg?auto=compress&cs=tinysrgb&w=600", title: "Свадебный портрет", category: "wedding" },
        { id: 8, url: "https://images.pexels.com/photos/2600187/pexels-photo-2600187.jpeg?auto=compress&cs=tinysrgb&w=600", title: "Корпоратив", category: "event" }
    ];

    // Отзывы
    const reviewsData = [
        { name: "Екатерина Смирнова", service: "Свадебная съёмка", text: "Анна — настоящий профессионал! Фотосессия прошла на одном дыхании. Результат превзошёл все ожидания. Спасибо за такие тёплые и живые кадры!", rating: 5 },
        { name: "Дмитрий и Мария", service: "Love Story", text: "Очень понравилось работать с Анной. Она чувствует кадр, умеет расслабить и создать комфортную атмосферу. Фотографии получились очень естественными и красивыми.", rating: 5 },
        { name: "Алина Кравцова", service: "Портретная съёмка", text: "Лучший фотограф! Сделала прекрасные снимки для моего портфолио. Рекомендую всем!", rating: 5 },
        { name: "Компания 'Импульс'", service: "Репортаж", text: "Спасибо за потрясающие фото с нашего корпоратива! Всё быстро, качественно, профессионально. Обязательно обратимся ещё!", rating: 5 }
    ];

    // Рендер портфолио
    function renderPortfolio(filter = "all") {
        const grid = document.getElementById("portfolioGrid");
        if (!grid) return;
        
        let filtered = portfolioData;
        if (filter !== "all") {
            filtered = portfolioData.filter(item => item.category === filter);
        }
        
        grid.innerHTML = filtered.map(item => `
            <div class="portfolio-item" data-id="${item.id}">
                <img src="${item.url}" alt="${item.title}" loading="lazy">
                <div class="portfolio-overlay">
                    <span>${item.title}</span>
                </div>
            </div>
        `).join("");
        
        // Добавляем обработчики для открытия модалки
        document.querySelectorAll(".portfolio-item").forEach(item => {
            item.addEventListener("click", () => {
                const id = parseInt(item.getAttribute("data-id"));
                const photo = portfolioData.find(p => p.id === id);
                if (photo) openModal(photo.url, photo.title);
            });
        });
    }

    // Рендер отзывов
    function renderReviews() {
        const grid = document.getElementById("reviewsGrid");
        if (!grid) return;
        
        grid.innerHTML = reviewsData.map(review => `
            <div class="review-card">
                <div class="review-stars">
                    ${'<i class="fas fa-star"></i>'.repeat(review.rating)}
                </div>
                <p class="review-text">"${review.text}"</p>
                <div class="review-author">
                    <h4>${review.name}</h4>
                    <span>${review.service}</span>
                </div>
            </div>
        `).join("");
    }

    // Модальное окно
    const modal = document.getElementById("imageModal");
    const modalImg = document.getElementById("modalImage");
    const modalCaption = document.getElementById("modalCaption");
    
    function openModal(url, title) {
        modalImg.src = url;
        modalCaption.textContent = title;
        modal.classList.add("active");
        document.body.style.overflow = "hidden";
    }
    
    function closeModal() {
        modal.classList.remove("active");
        document.body.style.overflow = "";
    }
    
    document.querySelector(".close-modal").addEventListener("click", closeModal);
    modal.addEventListener("click", (e) => {
        if (e.target === modal) closeModal();
    });
    document.addEventListener("keydown", (e) => {
        if (e.key === "Escape" && modal.classList.contains("active")) closeModal();
    });

    // Навигация между страницами
    function showPage(pageId) {
        document.querySelectorAll(".page").forEach(page => {
            page.classList.remove("active-page");
        });
        document.getElementById(`${pageId}-page`).classList.add("active-page");
        
        document.querySelectorAll(".nav-links a").forEach(link => {
            link.classList.remove("active");
            if (link.getAttribute("data-page") === pageId) {
                link.classList.add("active");
            }
        });
        
        if (pageId === "portfolio") {
            renderPortfolio();
        } else if (pageId === "reviews") {
            renderReviews();
        }
        
        window.scrollTo({ top: 0, behavior: "smooth" });
    }
    
    document.querySelectorAll(".nav-links a").forEach(link => {
        link.addEventListener("click", (e) => {
            e.preventDefault();
            const pageId = link.getAttribute("data-page");
            showPage(pageId);
        });
    });
    
    document.querySelectorAll("[data-page]").forEach(link => {
        if (link.getAttribute("data-page") && !link.closest(".nav-links")) {
            link.addEventListener("click", (e) => {
                e.preventDefault();
                const pageId = link.getAttribute("data-page");
                showPage(pageId);
            });
        }
    });
    
    // Фильтры портфолио
    document.querySelectorAll(".filter-btn").forEach(btn => {
        btn.addEventListener("click", () => {
            document.querySelectorAll(".filter-btn").forEach(b => b.classList.remove("active"));
            btn.classList.add("active");
            const filter = btn.getAttribute("data-filter");
            renderPortfolio(filter);
        });
    });
    
    // Форма заявки
    document.getElementById("bookingForm")?.addEventListener("submit", (e) => {
        e.preventDefault();
        document.getElementById("bookingForm").classList.add("hidden");
        document.getElementById("formSuccess").classList.remove("hidden");
        setTimeout(() => {
            document.getElementById("bookingForm").reset();
            document.getElementById("bookingForm").classList.remove("hidden");
            document.getElementById("formSuccess").classList.add("hidden");
        }, 3000);
    });
    
    // Форма сообщения
    document.getElementById("directMessageForm")?.addEventListener("submit", (e) => {
        e.preventDefault();
        alert("Сообщение отправлено! Я свяжусь с вами в ближайшее время.");
        document.getElementById("directMessageForm").reset();
    });
    
    // Бургер меню
    document.querySelector(".burger")?.addEventListener("click", () => {
        document.querySelector(".nav-links").classList.toggle("active");
    });
    
    // Инициализация
    renderPortfolio();
    renderReviews();
</script>
</body>
</html>
