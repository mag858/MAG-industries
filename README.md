
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="author" content="Glushnev Mikhail Alekseevich">
    <meta name="description" content="Сайт компании MAG Industries – будущая многомиллиардная компания по производству автомобилей и электроники в СНГ">
    <meta name="keywords" content="MAG industries, стартап, автомобили, электроника, 3D-принтер, Arduino, технологии, СНГ, инновации">
    <title>MAG Industries | Будущее — прямо сейчас</title>
   
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;600;700&family=Roboto:wght@300;400&display=swap" rel="stylesheet">
   
    <style>
        :root {
            --primary: #F3A000;
            --red: #FF0000;
            --bg: #CCE1FE;
            --text: #222;
            --shadow: 0 4px 15px rgba(0,0,0,0.1);
            --header-bg: #FFF8E1; /* Новый мягкий цвет шторки */
            --transition-fast: 0.3s ease;
            --transition-medium: 0.5s ease;
            --transition-slow: 0.8s cubic-bezier(0.25, 0.8, 0.25, 1);
        }
       
        * { margin: 0; padding: 0; box-sizing: border-box; }
       
        body {
            font-family: 'Roboto', sans-serif;
            background-color: var(--bg);
            color: var(--text);
            line-height: 1.6;
            overflow-x: hidden;
        }

        .fade-in {
            opacity: 0;
            transform: translateY(40px);
            transition: opacity 0.8s var(--transition-slow), transform 0.8s var(--transition-slow);
        }
        .fade-in.visible {
            opacity: 1;
            transform: translateY(0);
        }
       
        header {
            padding: 16px 0;
            background: var(--header-bg);
            box-shadow: var(--shadow);
            position: sticky;
            top: 0;
            z-index: 100;
            backdrop-filter: blur(10px);
            transition: background 0.4s ease;
        }
       
        .header-content {
            max-width: 1200px;
            margin: 0 auto;
            text-align: center;
            padding: 0 15px;
        }
       
        .site-title {
            font-family: 'Montserrat', sans-serif;
            font-size: 2.3rem;
            font-weight: 700;
            color: var(--red);
            margin-bottom: 16px;
            opacity: 0;
            animation: slideDown 0.8s var(--transition-slow) forwards;
        }

        @keyframes slideDown {
            from { opacity: 0; transform: translateY(-30px); }
            to { opacity: 1; transform: translateY(0); }
        }
       
        nav {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 12px;
            max-width: 1000px;
            margin: 0 auto;
            position: relative;
        }

        /* Декоративные разделители в навбаре */
        nav::before,
        nav::after {
            content: '';
            position: absolute;
            top: 50%;
            width: 1px;
            height: 40px;
            background: rgba(243,160,0,0.3);
            transform: translateY(-50%);
        }
        nav::before { left: 33.33%; }
        nav::after { left: 66.66%; }

        nav a {
            text-decoration: none;
            color: var(--text);
            font-weight: 600;
            padding: 12px 8px;
            border-radius: 10px;
            transition: all var(--transition-fast);
            font-size: 0.95rem;
            text-align: center;
            background: rgba(255,255,255,0.6);
            position: relative;
            overflow: hidden;
        }

        nav a::before {
            content: '';
            position: absolute;
            top: 0; left: -100%;
            width: 100%; height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255,255,255,0.4), transparent);
            transition: left 0.6s ease;
        }

        nav a:hover::before {
            left: 100%;
        }
       
        nav a:hover {
            background: var(--primary);
            color: white;
            transform: translateY(-4px);
            box-shadow: 0 8px 20px rgba(243,160,0,0.3);
        }
       
        .hero {
            text-align: center;
            padding: 30px 20px 50px;
            position: relative;
            overflow: hidden;
        }

        .hero::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle, rgba(243,160,0,0.07) 0%, transparent 70%);
            animation: pulse 12s infinite ease-in-out;
        }

        @keyframes pulse {
            0%, 100% { transform: scale(1); }
            50% { transform: scale(1.15); }
        }
       
        .logo {
            max-width: 320px;
            border-radius: 20px;
            box-shadow: var(--shadow);
            margin-bottom: 24px;
            opacity: 0;
            animation: zoomIn 1s var(--transition-slow) 0.3s forwards;
        }

        @keyframes zoomIn {
            from { opacity: 0; transform: scale(0.8); }
            to { opacity: 1; transform: scale(1); }
        }
       
        h1 {
            font-family: 'Montserrat', sans-serif;
            font-size: 3rem;
            color: var(--primary);
            margin: 0 0 12px 0;
            line-height: 1.2;
            opacity: 0;
            animation: fadeUp 1s var(--transition-slow) 0.6s forwards;
        }

        .subtitle {
            font-size: 1.6rem;
            color: #333;
            font-weight: 500;
            opacity: 0;
            animation: fadeUp 1s var(--transition-slow) 0.9s forwards;
        }

        @keyframes fadeUp {
            from { opacity: 0; transform: translateY(30px); }
            to { opacity: 1; transform: translateY(0); }
        }
       
        .banner {
            width: 100%;
            max-width: 1270px;
            margin: 40px auto;
            border-radius: 15px;
            overflow: hidden;
            box-shadow: var(--shadow);
            opacity: 0;
            transform: scale(0.95);
            animation: bannerReveal 1.2s var(--transition-slow) 1.2s forwards;
        }

        @keyframes bannerReveal {
            to { opacity: 1; transform: scale(1); }
        }
       
        .content {
            max-width: 1000px;
            margin: 40px auto;
            padding: 0 20px;
            font-size: 1.1rem;
            text-align: justify;
        }

        .content p {
            margin-bottom: 24px;
            opacity: 0;
            transform: translateX(-30px);
            transition: all 0.8s var(--transition-slow);
        }

        .content p.visible {
            opacity: 1;
            transform: translateX(0);
        }
       
        .gallery h2 {
            text-align: center;
            font-family: 'Montserrat', sans-serif;
            font-size: 2.2rem;
            margin: 60px 0 40px;
            color: var(--primary);
            position: relative;
            opacity: 0;
            animation: fadeUp 1s var(--transition-slow) forwards;
        }

        .gallery h2::after {
            content: '';
            position: absolute;
            bottom: -12px;
            left: 50%;
            transform: translateX(-50%);
            width: 80px;
            height: 4px;
            background: var(--primary);
            border-radius: 2px;
            animation: lineGrow 1s var(--transition-slow) 0.5s forwards;
            opacity: 0;
        }

        @keyframes lineGrow {
            to { width: 120px; opacity: 1; }
        }
       
        .grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 25px;
            max-width: 1200px;
            margin: 0 auto 60px;
            padding: 0 20px;
        }
       
        .grid img {
            width: 100%;
            height: 250px;
            object-fit: cover;
            border-radius: 15px;
            box-shadow: var(--shadow);
            transition: all 0.6s var(--transition-slow);
            opacity: 0;
            transform: translateY(50px) scale(0.95);
        }

        .grid img.visible {
            opacity: 1;
            transform: translateY(0) scale(1);
        }
       
        .grid img:hover {
            transform: translateY(-15px) scale(1.05);
            box-shadow: 0 20px 40px rgba(0,0,0,0.25);
        }
       
        .grid img:last-child {
            grid-column: 1 / -1;
            width: 100%;
            max-width: 400px;
            height: 250px;
            margin: 0 auto;
            justify-self: center;
            object-fit: cover;
        }
       
        footer {
            text-align: center;
            padding: 40px;
            background: var(--header-bg);
            font-size: 0.9rem;
            color: #666;
            opacity: 0;
            animation: fadeIn 1.5s ease 1s forwards;
        }

        @keyframes fadeIn {
            to { opacity: 1; }
        }
       
        /* ==================== МОБИЛЬНАЯ АДАПТАЦИЯ ==================== */
        @media (max-width: 768px) {
            .site-title { font-size: 2rem; margin-bottom: 12px; }
            h1 { font-size: 2.6rem; }
            .subtitle { font-size: 1.5rem; }
            .logo { max-width: 260px; }

            /* На мобильных — одна колонка и горизонтальные разделители */
            nav {
                grid-template-columns: 1fr;
                gap: 10px;
            }

            nav::before, nav::after { display: none; }

            nav a {
                padding: 14px 10px;
                font-size: 1rem;
                position: relative;
            }

            /* Горизонтальные декоративные линии между пунктами */
            nav a:not(:last-child)::after {
                content: '';
                position: absolute;
                bottom: -5px;
                left: 50%;
                transform: translateX(-50%);
                width: 60%;
                height: 1px;
                background: rgba(243,160,0,0.3);
            }

            .hero { padding: 30px 15px 50px; }
            .content { padding: 0 15px; font-size: 1.15rem; }
            .grid { padding: 0 15px; gap: 20px; }
            .grid img { height: 200px; }
            .grid img:last-child { height: 200px; max-width: 300px; }
        }

        @media (max-width: 480px) {
            .site-title { font-size: 1.8rem; }
            h1 { font-size: 2.3rem; }
            .subtitle { font-size: 1.3rem; }
            nav a { font-size: 0.95rem; padding: 12px 8px; }
        }
    </style>
</head>
<body>
    <header>
        <div class="header-content">
            <div class="site-title">MAG industries</div>
            <nav>
                <a href="https://mag858.github.io/mag_svas/">Связаться с нами</a>
                <a href="https://mag858.github.io/mag_idea/">Поделиться идеями</a>
                <a href="https://mag858.github.io/mag_opros/">Опрос по часам</a>
                <a href="https://mag858.github.io/opros_electronics/">Опрос по электронике</a>
                <a href="https://mag858.github.io/mag_help_me/">Помощь в развитии</a>
                <a href="https://mag858.github.io/mag_help_you/">Техническая помощь</a>
            </nav>
        </div>
    </header>

    <section class="hero fade-in">
        <img src="sait/logo_2.jpeg" alt="Логотип MAG Industries" class="logo">
        <h1>future - right now</h1>
        <div class="subtitle">(будущее - прямо сейчас)</div>
        <img src="sait/pop.jpg" alt="Баннер" class="banner">
    </section>

    <section class="content fade-in">
        <p>Всем привет! Мы — будущая многомиллиардная компания MAG industries, которая будет заниматься производством электронных наручных часов и электроникой на территории СНГ, США и ЕВРОПЫ.</p>
        <p>Мы хотим, чтобы вы помогли нам финансово или своим мнением о продукте, который мы планируем выпустить на рынок.</p>
        <p>Мы запустим наш бренд по всему миру и будем развивать его и нашу компанию</p>
        <p>Если у вас есть идеи по часам — предлагайте их <a href="https://mag858.github.io/mag_idea/">здесь</a>.</p>
    </section>

    <section class="gallery">
        <h2 class="fade-in">Наши возможности</h2>
        <div class="grid">
            <img src="sait/foto1.jpg" alt="" class="fade-in">
            <img src="sait/foto2.jpg" alt="" class="fade-in">
            <img src="sait/foto3.jpg" alt="" class="fade-in">
            <img src="sait/foto4.jpg" alt="" class="fade-in">
            <img src="sait/foto5.jpg" alt="" class="fade-in">
            <img src="sait/stol1.JPG" alt="" class="fade-in">
            <img src="sait/stol2.JPG" alt="" class="fade-in">
            <img src="sait/stol3.JPG" alt="" class="fade-in">
            <img src="sait/stol4.JPG" alt="" class="fade-in">
            <img src="sait/stol5.JPG" alt="" class="fade-in">
            <img src="sait/stol6.JPG" alt="" class="fade-in">
        </div>
    </section>

    <footer>
        обновление 3.1 &emsp; январь 2026 г.
    </footer>

    <script>
        document.addEventListener('DOMContentLoaded', () => {
            const elements = document.querySelectorAll('.fade-in, .content p, .grid img');
            
            const observer = new IntersectionObserver((entries) => {
                entries.forEach(entry => {
                    if (entry.isIntersecting) {
                        entry.target.classList.add('visible');
                    }
                });
            }, { threshold: 0.1 });

            elements.forEach(el => observer.observe(el));
        });
    </script>
</body>
</html>
