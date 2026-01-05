
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
            --light-yellow: #FFFFE0; /* Лёгкий неяркий жёлтый */
        }
       
        * { margin: 0; padding: 0; box-sizing: border-box; }
       
        body {
            font-family: 'Roboto', sans-serif;
            background-color: var(--bg);
            color: var(--text);
            line-height: 1.6;
        }
       
        header {
            padding: 12px 0;
            background: var(--light-yellow); /* Изменённый цвет шторки */
            box-shadow: var(--shadow);
            position: sticky;
            top: 0;
            z-index: 100;
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
            margin-bottom: 15px; /* Увеличил отступ */
        }
       
        /* Новый разделитель */
        .header-divider {
            height: 2px;
            background: var(--primary);
            width: 60%;
            max-width: 400px;
            margin: 0 auto 20px;
            border-radius: 2px;
        }
       
        nav {
            display: grid;
            grid-template-columns: 1fr 1fr 1fr; /* Всегда 3 колонки */
            gap: 8px 12px;
            max-width: 1000px;
            margin: 0 auto;
        }
       
        nav a {
            text-decoration: none;
            color: var(--text);
            font-weight: 600;
            padding: 10px 6px;
            border-radius: 8px;
            transition: all 0.3s ease;
            font-size: 0.95rem;
            text-align: center;
            background: rgba(255,255,255,0.6); /* Слегка смягчил фон ссылок */
            border: 1px solid rgba(0,0,0,0.1);
        }
       
        nav a:hover {
            background: var(--primary);
            color: white;
            border-color: var(--primary);
        }
       
        .hero {
            text-align: center;
            padding: 25px 20px 40px;
        }
       
        .logo {
            max-width: 320px;
            border-radius: 20px;
            box-shadow: var(--shadow);
            margin-bottom: 20px;
        }
       
        h1 {
            font-family: 'Montserrat', sans-serif;
            font-size: 3rem;
            color: var(--primary);
            margin: 0 0 10px 0;
            line-height: 1.2;
        }
       
        .subtitle {
            font-size: 1.6rem;
            color: #333;
            font-weight: 500;
        }
       
        .banner {
            width: 100%;
            max-width: 1270px;
            margin: 40px auto;
            border-radius: 15px;
            overflow: hidden;
            box-shadow: var(--shadow);
        }
       
        .content {
            max-width: 1000px;
            margin: 40px auto;
            padding: 0 20px;
            font-size: 1.1rem;
            text-align: justify;
        }
       
        .gallery h2 {
            text-align: center;
            font-family: 'Montserrat', sans-serif;
            font-size: 2.2rem;
            margin: 60px 0 40px;
            color: var(--primary);
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
            transition: all 0.4s ease;
        }
       
        .grid img:hover {
            transform: translateY(-10px) scale(1.03);
            box-shadow: 0 15px 30px rgba(0,0,0,0.2);
        }
       
        .grid img:last-child {
            grid-column: 1 / -1;
            max-width: 400px;
            height: 250px;
            margin: 0 auto;
            justify-self: center;
        }
       
        footer {
            text-align: center;
            padding: 40px;
            background: rgba(255,255,255,0.9);
            font-size: 0.9rem;
            color: #666;
        }
       
        @media (max-width: 768px) {
            .site-title { font-size: 1.9rem; }
            h1 { font-size: 2.4rem; }
            .subtitle { font-size: 1.4rem; }
            nav { grid-template-columns: 1fr 1fr; } /* На мобильных чуть удобнее */
            nav a { font-size: 0.9rem; padding: 10px 4px; }
            .logo { max-width: 280px; }
            .grid img { height: 200px; }
            .grid img:last-child { height: 200px; }
        }
    </style>
</head>
<body>
    <header>
        <div class="header-content">
            <div class="site-title">MAG Industries</div>
            <div class="header-divider"></div> <!-- Новый разделитель -->
            <nav>
                <a href="https://mag858.github.io/mag_svas/">Связаться с нами</a>
                <a href="https://mag858.github.io/mag_idea/">Поделиться идеями</a>
                <a href="https://mag858.github.io/mag_opros/">Опрос по машинам</a>
                <a href="https://mag858.github.io/opros_electronics/">Опрос по электронике</a>
                <a href="https://mag858.github.io/mag_help_me/">Помощь в развитии</a>
                <a href="https://mag858.github.io/mag_help_you/">Техническая помощь</a>
            </nav>
        </div>
    </header>
    <section class="hero">
        <img src="sait/logo_2.jpeg" alt="Логотип MAG Industries" class="logo">
        <h1>future - right now</h1>
        <div class="subtitle">(будущее - прямо сейчас)</div>
        <img src="sait/pop.jpg" alt="Баннер" class="banner">
    </section>
    <section class="content">
        <p>Всем привет! Мы — будущая многомиллиардная компания MAG Industries, которая будет заниматься производством автомобилей на территории СНГ.</p>
        <p>Мы хотим, чтобы вы помогли нам финансово или своим мнением о продукте, который мы планируем выпустить на авторынок.</p>
        <p>Мы прекрасно понимаем, что создать автомобильную компанию с нуля крайне сложно, поэтому начинаем с небольших электронных устройств. Они будут постепенно перерастать в крупные проекты, приносящие прибыль для развития автомобилестроения.</p>
        <p>Если у вас есть идеи — предлагайте их <a href="https://mag858.github.io/mag_idea/">здесь</a>.</p>
    </section>
    <section class="gallery">
        <h2>Наши возможности</h2>
        <div class="grid">
            <img src="sait/foto1.jpg" alt="">
            <img src="sait/foto2.jpg" alt="">
            <img src="sait/foto3.jpg" alt="">
            <img src="sait/foto4.jpg" alt="">
            <img src="sait/foto5.jpg" alt="">
            <img src="sait/stol1.JPG" alt="">
            <img src="sait/stol2.JPG" alt="">
            <img src="sait/stol3.JPG" alt="">
            <img src="sait/stol4.JPG" alt="">
            <img src="sait/stol5.JPG" alt="">
            <img src="sait/stol6.JPG" alt="">
        </div>
    </section>
    <footer>
        обновление 3.1 &emsp; январь 2026 г.
    </footer>
</body>
</html>
