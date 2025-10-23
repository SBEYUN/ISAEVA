<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>JDM Culture - Японская автомобильная культура</title>
    <style>
        /* Общие стили */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        body {
            background-color: #0a0a0a;
            color: #f0f0f0;
            line-height: 1.6;
        }
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        /* Шапка сайта */
        header {
            background-color: rgba(10, 10, 10, 0.9);
            position: fixed;
            width: 100%;
            z-index: 1000;
            border-bottom: 1px solid #c00;
        }
        .header-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 15px 0;
        }
        .logo {
            font-size: 24px;
            font-weight: bold;
            color: #c00;
            text-transform: uppercase;
            letter-spacing: 2px;
        }
        .logo span {
            color: #f0f0f0;
        }
        nav ul {
            display: flex;
            list-style: none;
        }
        nav ul li {
            margin-left: 30px;
        }
        nav ul li a {
            color: #f0f0f0;
            text-decoration: none;
            font-weight: 500;
            transition: color 0.3s;
        }
        nav ul li a:hover {
            color: #c00;
        }
        /* Герой секция */
        .hero {
            height: 100vh;
            background: linear-gradient(rgba(0, 0, 0, 0.7), rgba(0, 0, 0, 0.7)),
                        url('https://images.unsplash.com/photo-1592198084033-aade902d1aae?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2070&q=80') no-repeat center center/cover;
            display: flex;
            align-items: center;
            text-align: center;
        }
        .hero-content {
            max-width: 800px;
            margin: 0 auto;
        }
        .hero h1 {
            font-size: 48px;
            margin-bottom: 20px;
            text-transform: uppercase;
            letter-spacing: 3px;
        }
        .hero p {
            font-size: 18px;
            margin-bottom: 30px;
            color: #ccc;
        }
        .btn {
            display: inline-block;
            background-color: #c00;
            color: #fff;
            padding: 12px 30px;
            text-decoration: none;
            border-radius: 4px;
            font-weight: bold;
            text-transform: uppercase;
            letter-spacing: 1px;
            transition: background-color 0.3s;
        }
        .btn:hover {
            background-color: #a00;
        }
        /* Секции */
        section {
            padding: 80px 0;
        }
        .section-title {
            text-align: center;
            margin-bottom: 50px;
            position: relative;
        }
        .section-title h2 {
            font-size: 36px;
            text-transform: uppercase;
            letter-spacing: 2px;
            display: inline-block;
        }
        .section-title h2::after {
            content: '';
            display: block;
            width: 80px;
            height: 3px;
            background-color: #c00;
            margin: 10px auto;
        }
        /* О JDM */
        .about-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 40px;
            align-items: center;
        }
        .about-text p {
            margin-bottom: 20px;
            color: #ccc;
        }
        .about-image img {
            width: 100%;
            border-radius: 8px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.5);
        }
        /* Популярные автомобили */
        .cars-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
            gap: 30px;
        }
        .car-card {
            background-color: #1a1a1a;
            border-radius: 8px;
            overflow: hidden;
            transition: transform 0.3s;
        }
        .car-card:hover {
            transform: translateY(-10px);
        }
        .car-image {
            height: 200px;
            overflow: hidden;
        }
        .car-image img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s;
        }
        .car-card:hover .car-image img {
            transform: scale(1.1);
        }
        .car-info {
            padding: 20px;
        }
        .car-info h3 {
            font-size: 20px;
            margin-bottom: 10px;
            color: #c00;
        }
        /* Мероприятия */
        .events-list {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(350px, 1fr));
            gap: 30px;
        }
        .event-card {
            background-color: #1a1a1a;
            border-radius: 8px;
            padding: 25px;
            border-left: 4px solid #c00;
        }
        .event-date {
            color: #c00;
            font-weight: bold;
            margin-bottom: 10px;
        }
        .event-card h3 {
            margin-bottom: 15px;
        }
        /* Галерея */
        .gallery-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            gap: 15px;
        }
        .gallery-item {
            height: 200px;
            overflow: hidden;
            border-radius: 8px;
            position: relative;
        }
        .gallery-item img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s;
        }
        .gallery-item:hover img {
            transform: scale(1.1);
        }
        /* Подвал */
        footer {
            background-color: #111;
            padding: 50px 0 20px;
        }
        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 40px;
            margin-bottom: 40px;
        }
        .footer-column h3 {
            color: #c00;
            margin-bottom: 20px;
            font-size: 18px;
        }
        .footer-column ul {
            list-style: none;
        }
        .footer-column ul li {
            margin-bottom: 10px;
        }
        .footer-column ul li a {
            color: #ccc;
            text-decoration: none;
            transition: color 0.3s;
        }
        .footer-column ul li a:hover {
            color: #c00;
        }
        .social-links {
            display: flex;
            gap: 15px;
        }
        .social-links a {
            display: inline-block;
            width: 40px;
            height: 40px;
            background-color: #333;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: #fff;
            transition: background-color 0.3s;
        }
        .social-links a:hover {
            background-color: #c00;
        }
        .copyright {
            text-align: center;
            padding-top: 20px;
            border-top: 1px solid #333;
            color: #777;
            font-size: 14px;
        }
        /* Адаптивность */
        @media (max-width: 768px) {
            .header-container {
                flex-direction: column;
            }
            nav ul {
                margin-top: 15px;
            }
            nav ul li {
                margin-left: 15px;
                margin-right: 15px;
            }
            .hero h1 {
                font-size: 36px;
            }
            .about-content {
                grid-template-columns: 1fr;
            }
            section {
                padding: 50px 0;
            }
        }
    </style>
</head>
<body>
    <!-- Шапка сайта -->
    <header>
        <div class="container header-container">
            <div class="logo">JDM<span>Culture</span></div>
            <nav>
                <ul>
                    <li><a href="#home">Главная</a></li>
                    <li><a href="#about">О JDM</a></li>
                    <li><a href="#cars">Автомобили</a></li>
                    <li><a href="#events">Мероприятия</a></li>
                    <li><a href="#gallery">Галерея</a></li>
                </ul>
            </nav>
        </div>
    </header>
    <!-- Герой секция -->
    <section class="hero" id="home">
        <div class="container hero-content">
            <h1>JDM Культура</h1>
            <p>Погрузитесь в мир японских автомобилей, тюнинга и уникальной автомобильной культуры, зародившейся в Японии и покорившей весь мир.</p>
            <a href="#about" class="btn">Узнать больше</a>
        </div>
    </section>
    <!-- О JDM -->
    <section id="about">
        <div class="container">
            <div class="section-title">
                <h2>О JDM Культуре</h2>
            </div>
            <div class="about-content">
                <div class="about-text">
                    <p>JDM (Japanese Domestic Market) - это термин, обозначающий автомобили и запчасти, предназначенные для внутреннего рынка Японии. Со временем это понятие превратилось в целую культуру, объединяющую любителей японских автомобилей по всему миру.</p>
                    <p>JDM культура включает в себя не только автомобили, но и особый подход к тюнингу, стилю вождения и образу жизни. Это сообщество людей, ценящих качество, надежность и уникальный дизайн японских автомобилей.</p>
                    <p>От классических спорткаров 90-х до современных технологичных моделей - JDM охватывает все поколения японского автопрома, создавая уникальное сообщество энтузиастов.</p>
                </div>
                <div class="about-image">
                    <img src="https://images.unsplash.com/photo-1580273916550-e323be2ae537?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1964&q=80" alt="JDM автомобиль">
                </div>
            </div>
        </div>
    </section>
    <!-- Популярные автомобили -->
    <section id="cars">
        <div class="container">
            <div class="section-title">
                <h2>Популярные JDM автомобили</h2>
            </div>
            <div class="cars-grid">
                <div class="car-card">
                    <div class="car-image">
                        <img src="https://images.unsplash.com/photo-1621007947382-bb3c3994e3fb?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2070&q=80" alt="Nissan Skyline GT-R">
                    </div>
                    <div class="car-info">
                        <h3>Nissan Skyline GT-R</h3>
                        <p>Легендарный "Годзилла" - икона JDM культуры, известный своими победами в гонках и передовыми технологиями.</p>
                    </div>
                </div>
                <div class="car-card">
                    <div class="car-image">
                        <img src="https://images.unsplash.com/photo-1621007947382-bb3c3994e3fb?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2070&q=80" alt="Toyota Supra">
                    </div>
                    <div class="car-info">
                        <h3>Toyota Supra</h3>
                        <p>Знаменитый спортивный автомобиль с культовым двигателем 2JZ, прославившийся в фильме "Форсаж".</p>
                    </div>
                </div>
                <div class="car-card">
                    <div class="car-image">
                        <img src="https://images.unsplash.com/photo-1621007947382-bb3c3994e3fb?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2070&q=80" alt="Mazda RX-7">
                    </div>
                    <div class="car-info">
                        <h3>Mazda RX-7</h3>
                        <p>Спортивный автомобиль с роторным двигателем Ванкеля, известный своим уникальным дизайном и характеристиками.</p>
                    </div>
                </div>
                <div class="car-card">
                    <div class="car-image">
                        <img src="https://images.unsplash.com/photo-1621007947382-bb3c3994e3fb?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2070&q=80" alt="Honda NSX">
                    </div>
                    <div class="car-info">
                        <h3>Honda NSX</h3>
                        <p>Японский суперкар, созданный при участии Айртона Сенны, сочетающий в себе высокие технологии и надежность.</p>
                    </div>
                </div>
            </div>
        </div>
    </section>
    <!-- Мероприятия -->
    <section id="events">
        <div class="container">
            <div class="section-title">
                <h2>Ближайшие мероприятия</h2>
            </div>
            <div class="events-list">
                <div class="event-card">
                    <div class="event-date">15 октября 2025</div>
                    <h3>Tokyo Auto Salon</h3>
                    <p>Крупнейшая выставка тюнинга и автомобильной культуры в Японии. Уникальная возможность увидеть новейшие тюнинг-проекты и концепты.</p>
                </div>
                <div class="event-card">
                    <div class="event-date">5 ноября 2025</div>
                    <h3>JDM Meet Moscow</h3>
                    <p>Ежемесячная встреча поклонников JDM в Москве. Общение, демонстрация автомобилей и обмен опытом.</p>
                </div>
                <div class="event-card">
                    <div class="event-date">20 ноября 2025</div>
                    <h3>Drift Challenge</h3>
                    <p>Соревнования по дрифту среди владельцев JDM автомобилей. Шоу и зрелищные заезды на специально подготовленной трассе.</p>
                </div>
            </div>
        </div>
    </section>
    <!-- Галерея -->
    <section id="gallery">
        <div class="container">
            <div class="section-title">
                <h2>Галерея</h2>
            </div>
            <div class="gallery-grid">
                <div class="gallery-item">
                    <img src="https://images.unsplash.com/photo-1592198084033-aade902d1aae?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2070&q=80" alt="JDM автомобиль">
                </div>
                <div class="gallery-item">
                    <img src="https://images.unsplash.com/photo-1580273916550-e323be2ae537?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1964&q=80" alt="JDM автомобиль">
                </div>
                <div class="gallery-item">
                    <img src="https://images.unsplash.com/photo-1621007947382-bb3c3994e3fb?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2070&q=80" alt="JDM автомобиль">
                </div>
                <div class="gallery-item">
                    <img src="https://images.unsplash.com/photo-1621007947382-bb3c3994e3fb?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2070&q=80" alt="JDM автомобиль">
                </div>
                <div class="gallery-item">
                    <img src="https://images.unsplash.com/photo-1621007947382-bb3c3994e3fb?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2070&q=80" alt="JDM автомобиль">
                </div>
                <div class="gallery-item">
                    <img src="https://images.unsplash.com/photo-1621007947382-bb3c3994e3fb?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2070&q=80" alt="JDM автомобиль">
                </div>
            </div>
        </div>
    </section>
    <!-- Подвал -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-column">
                    <h3>JDM Culture</h3>
                    <p>Сайт посвящен японской автомобильной культуре и всему, что с ней связано.</p>
                    <div class="social-links">
                        <a href="#">VK</a>
                        <a href="#">TG</a>
                        <a href="#">YT</a>
                        <a href="#">IG</a>
                    </div>
                </div>
                <div class="footer-column">
                    <h3>Разделы</h3>
                    <ul>
                        <li><a href="#home">Главная</a></li>
                        <li><a href="#about">О JDM</a></li>
                        <li><a href="#cars">Автомобили</a></li>
                        <li><a href="#events">Мероприятия</a></li>
                        <li><a href="#gallery">Галерея</a></li>
                    </ul>
                </div>
                <div class="footer-column">
                    <h3>Контакты</h3>
                    <ul>
                        <li>Сайт воссоздала Исаева Рина</li>
                        <li>Телефон: +7 (977) 905-27-02</li>
                        <li>Адрес: Москва, ул. Автомобильная, 15</li>
                    </ul>
                </div>
            </div>
            <div class="copyright">
                <p>&copy; 2025 JDM Culture. Все права защищены.</p>
            </div>
        </div>
    </footer>
</body>
</html>
