<!DOCTYPE html>
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
            --accent-red: #FF0000;     /* Яркий красный */
            --bg: #CCE1FE;
            --text: #222;
            --shadow: 0 4px 15px rgba(0,0,0,0.1);
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Roboto', sans-serif;
            background-color: var(--bg);
            color: var(--text);
            line-height: 1.6;
            overflow-x: hidden;
        }
        
        header {
            padding: 10px 0;
            background: rgba(255,255,255,0.95);
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
            color: var(--accent-red);
            margin-bottom: 8px;
        }
        
        nav {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 10px;
        }
        
        nav a {
            text-decoration: none;
            color: var(--text);
            font-weight: 600;
            padding: 6px 10px;
            border-radius: 8px;
            transition: all 0.3s ease;
            white-space: nowrap;
            font-size: 0.95rem;
        }
        
        nav a:hover {
            background: var(--primary);
            color: white;
            transform: translateY(-2px);
        }
        
        .hero {
            text-align: center;
            padding: 20px 20px 20px; /* Ещё меньше сверху */
            animation: fadeIn 1.5s ease-out;
        }
        
        .logo {
            max-width: 320px;
            border-radius: 20px;
            box-shadow: var(--shadow);
            transition: transform 0.5s ease;
            animation: slideUp 1s ease-out;
        }
        
        .logo:hover {
            transform: scale(1.05);
        }
        
        h1 {
            font-family: 'Montserrat', sans-serif;
            font-size: 2.8rem;
            color: var(--primary);
            margin: 20px 0;
            animation: slideUp 1.2s ease-out;
        }
        
        h1 sup {
            font-size: 1.2rem;
            color: #555;
        }
        
        .banner {
            width: 100%;
            max-width: 1270px;
            margin: 30px auto;
            border-radius: 15px;
            overflow: hidden;
            box-shadow: var(--shadow);
            animation: fadeIn 2s ease-out;
        }
        
        .content {
            max-width: 1000px;
            margin: 40px auto;
            padding: 0 20px;
            font-size: 1.1rem;
            text-align: justify;
            animation: fadeInLeft 1.5s ease-out;
        }
        
        .gallery {
            max-width: 1200px;
            margin: 50px auto;
            padding: 0 20px;
        }
        
        .gallery h2 {
            text-align: center;
            font-family: 'Montserrat', sans-serif;
            font-size: 2.2rem;
            margin-bottom: 40px;
            color: var(--primary);
        }
        
        .grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 25px;
        }
        
        .grid img {
            width: 100%;
            height: auto;
            border-radius: 15px;
            box-shadow: var(--shadow);
            transition: all 0.4s ease;
            opacity: 0;
            animation: fadeInUp 1s ease-out forwards;
        }
        
        .grid img:hover {
            transform: translateY(-10px) scale(1.03);
            box-shadow: 0 15px 30px rgba(0,0,0,0.2);
        }
        
        .grid img:nth-child(1) { animation-delay: 0.2s; }
        .grid img:nth-child(2) { animation-delay: 0.4s; }
        .grid img:nth-child(3) { animation-delay: 0.6s; }
        .grid img:nth-child(4) { animation-delay: 0.8s; }
        .grid img:nth-child(5) { animation-delay: 1.0s; }
        .grid img:nth-child(6) { animation-delay: 1.2s; }
        
        footer {
            text-align: center;
            padding: 30px;
            background: rgba(255,255,255,0.9);
            margin-top: 50px;
            font-size: 0.9rem;
            color: #666;
        }
        
        @keyframes fadeIn { from { opacity: 0; } to { opacity: 1; } }
        @keyframes slideUp { from { opacity: 0; transform: translateY(50px); } to { opacity: 1; transform: translateY(0); } }
        @keyframes fadeInLeft { from { opacity: 0; transform: translateX(-50px); } to { opacity: 1; transform: translateX(0); } }
        @keyframes fadeInUp { from { opacity: 0; transform: translateY(30px); } to { opacity: 1; transform: translateY(0); } }
        
        /* Суперкомпактная шапка на телефоне */
        @media (max-width: 768px) {
            header {
                padding: 6px 0; /* Ещё меньше */
            }
            
            .site-title {
                font-size: 1.5rem; /* В 1.5 раза меньше */
                margin-bottom: 6px;
            }
            
            nav {
                gap: 6px;
                flex-direction: column;
                align-items: center;
            }
            
            nav a {
                font-size: 0.9rem;
                padding: 6px 8px;
                width: 92%;
                text-align: center;
            }
            
            h1 {
                font-size: 2.2rem;
            }
            
            .hero {
                padding-top: 10px; /* Минимальный отступ сверху */
            }
            
            .logo {
                max-width: 280px;
            }
        }
    </style>
</head>
<body>
    <header>
        <div class="header-content">
            <div class="site-title">MAG Industries</div>
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
        <h1>future - right now<sup>(будущее - прямо сейчас)</sup></h1>
        <img src="sait/pop.jpg" alt="Баннер MAG Industries" class="banner">
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
            <img src="sait/foto1.jpg" alt="Оборудование 1">
            <img src="sait/foto2.jpg" alt="Оборудование 2">
            <img src="sait/foto3.jpg" alt="Оборудование 3">
            <img src="sait/foto4.jpg" alt="Оборудование 4">
            <img src="sait/foto5.jpg" alt="Оборудование 5">
            <img src="sait/stol1.JPG" alt="Рабочее место 1">
            <img src="sait/stol2.JPG" alt="Рабочее место 2">
            <img src="sait/stol3.JPG" alt="Рабочее место 3">
            <img src="sait/stol4.JPG" alt="Рабочее место 4">
            <img src="sait/stol5.JPG" alt="Рабочее место 5">
            <img src="sait/stol6.JPG" alt="Рабочее место 6">
        </div>
    </section>

    <footer>
        обновление 2.5.0 &emsp; январь 2026 г.
    </footer>
</body>
</html>
