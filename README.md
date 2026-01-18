
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
            --light-yellow: #FFFFE0;
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
            background: var(--light-yellow);
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
            margin-bottom: 15px;
        }

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
            grid-template-columns: 1fr 1fr 1fr;
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
            background: rgba(255,255,255,0.6);
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

        /* ХРОНОЛОГИЯ */
        .horizontal-timeline-section {
            padding: 80px 20px;
            background: linear-gradient(to bottom, var(--bg), #ffffff);
        }
        .horizontal-timeline-section h2 {
            text-align: center;
            font-family: 'Montserrat', sans-serif;
            font-size: 2.2rem;
            margin-bottom: 70px;
            color: var(--primary);
        }
        .timeline-cards {
            display: flex;
            gap: 40px;
            overflow-x: auto;
            padding: 40px 20px;
            scroll-behavior: smooth;
            scrollbar-width: thin;
        }
        .timeline-cards::-webkit-scrollbar {
            height: 8px;
        }
        .timeline-cards::-webkit-scrollbar-thumb {
            background: var(--primary);
            border-radius: 4px;
        }
        .timeline-card {
            flex: 0 0 300px;
            max-width: 320px;
            width: 100%;
            background: white;
            border-radius: 15px;
            box-shadow: var(--shadow);
            overflow: hidden;
            text-align: center;
            opacity: 0;
            transform: translateY(40px);
            transition: opacity 0.8s ease, transform 0.8s ease;
            cursor: pointer;
        }
        .timeline-card.visible {
            opacity: 1;
            transform: translateY(0);
        }
        .timeline-card img {
            width: 100%;
            height: 300px;
            object-fit: cover;
            transition: transform 0.4s ease;
        }
        .timeline-card img:hover {
            transform: scale(1.05);
        }
        .timeline-info {
            padding: 20px 15px;
        }
        .timeline-date {
            font-weight: 700;
            font-size: 1.3rem;
            color: var(--primary);
            margin-bottom: 10px;
        }
        .timeline-title {
            font-weight: 600;
            font-size: 1.2rem;
            color: #333;
        }

        /* Bottom Sheet */
        .bottom-sheet {
            position: fixed;
            bottom: -100%;
            left: 0;
            right: 0;
            height: 85vh;
            background: white;
            border-top-left-radius: 24px;
            border-top-right-radius: 24px;
            box-shadow: 0 -10px 40px rgba(0,0,0,0.35);
            z-index: 2000;
            transition: bottom 0.5s cubic-bezier(0.25, 0.8, 0.25, 1);
            overflow-y: auto;
        }

        .bottom-sheet.active {
            bottom: 0;
        }

        .bottom-sheet-content {
            padding: 18px 24px 40px;
            position: relative;
        }

        .handle {
            width: 48px;
            height: 5px;
            background: #ccc;
            border-radius: 4px;
            margin: 12px auto 24px;
        }

        .close-btn {
            position: absolute;
            top: 16px;
            right: 20px;
            background: #f0f0f0;
            border: none;
            width: 36px;
            height: 36px;
            border-radius: 50%;
            font-size: 1.4rem;
            cursor: pointer;
            transition: background 0.2s;
        }

        .close-btn:hover {
            background: #e0e0e0;
        }

        .sheet-image-container {
            text-align: center;
            margin: 20px 0 30px;
        }

        #sheetMainImage {
            max-width: 100%;
            max-height: 320px;
            border-radius: 16px;
            box-shadow: 0 8px 25px rgba(0,0,0,0.15);
        }

        .specs h3 {
            color: var(--primary);
            margin: 28px 0 12px;
            font-family: 'Montserrat', sans-serif;
        }

        .specs ul {
            list-style: none;
            padding-left: 0;
        }

        .specs li {
            padding: 10px 0;
            border-bottom: 1px solid #eee;
            display: flex;
            justify-content: space-between;
        }

        .specs li strong {
            color: #444;
            min-width: 140px;
        }

        .specs li span {
            color: #666;
            text-align: right;
        }

        @media (max-width: 900px) {
            .timeline-cards {
                flex-direction: column;
                align-items: center;
                gap: 30px;
                padding: 20px 0;
                overflow-x: visible;
            }
            .timeline-card {
                flex: none;
                width: 90%;
                max-width: 400px;
            }
            .timeline-card img {
                height: 350px;
            }
        }

        @media (max-width: 600px) {
            .bottom-sheet {
                height: 92vh;
            }
            #sheetMainImage {
                max-height: 260px;
            }
        }

        @media (max-width: 768px) {
            .site-title { font-size: 1.9rem; }
            h1 { font-size: 2.4rem; }
            .subtitle { font-size: 1.4rem; }
            nav { grid-template-columns: 1fr 1fr; }
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
            <div class="header-divider"></div>
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

    <!-- ХРОНОЛОГИЯ СОЗДАНИЯ ЧАСОВ -->
    <section class="horizontal-timeline-section">
        <h2>Хронология создания часов</h2>
        <div class="timeline-cards">
            <div class="timeline-card">
                <img src="sait/clock-1.png" alt="Clock-1">
                <div class="timeline-info">
                    <div class="timeline-date">Май 2022</div>
                    <div class="timeline-title">Clock-1</div>
                </div>
            </div>
            <div class="timeline-card">
                <img src="sait/clock-2.png" alt="Clock-2">
                <div class="timeline-info">
                    <div class="timeline-date">Май 2023</div>
                    <div class="timeline-title">Clock-2</div>
                </div>
            </div>
            <div class="timeline-card">
                <img src="sait/clock-3.png" alt="Clock-3">
                <div class="timeline-info">
                    <div class="timeline-date">Июль 2023</div>
                    <div class="timeline-title">Clock-3</div>
                </div>
            </div>
            <div class="timeline-card">
                <img src="sait/clock-4.jpg" alt="Clock-4">
                <div class="timeline-info">
                    <div class="timeline-date">Апрель 2024</div>
                    <div class="timeline-title">Clock-4</div>
                </div>
            </div>
            <div class="timeline-card">
                <img src="sait/clock-4(P).png" alt="Clock-4(P)">
                <div class="timeline-info">
                    <div class="timeline-date">Май 2025</div>
                    <div class="timeline-title">Clock-4(P)</div>
                </div>
            </div>
            <div class="timeline-card">
                <img src="sait/clock-5.jpg" alt="Clock-5">
                <div class="timeline-info">
                    <div class="timeline-date">Декабрь 2025</div>
                    <div class="timeline-title">Clock-5</div>
                </div>
            </div>
        </div>
    </section>

    <!-- Bottom Sheet / Выезжающая панель -->
    <div class="bottom-sheet" id="bottomSheet">
        <div class="bottom-sheet-content">
            <div class="handle"></div>
            <button class="close-btn" id="closeSheet">✕</button>
            
            <h2 id="sheetTitle">Clock-X</h2>
            
            <div class="sheet-image-container">
                <img id="sheetMainImage" src="" alt="Часы">
            </div>
            
            <div class="specs">
                <h3>Основные характеристики</h3>
                <ul id="sheetSpecs"></ul>
                
                <h3>Функции</h3>
                <ul id="sheetFeatures"></ul>
            </div>
        </div>
    </div>

    <footer>
        обновление 3.3 &emsp; январь 2026 г.
    </footer>

    <script>
        // Данные о часах
        const clockData = {
            "Clock-1": {
                title: "Clock-1 (Май 2022)",
                image: "sait/clock-1.png",
                specs: [
                    ["Микроконтроллер", "ATmega328P"],
                    ["Дисплей", "7 сегментные индикаторы"],
                    ["Питание", "USB-C"],
                    ["Корпус", "PLA (3D-печать)"],
		    ["Время работы", "1.5 суток"],
                    ["Сложность", "★★★★☆"]
                ],
                features: [
                    "Показ времени",
                    "Таймер 5 минутный",
                    "Режим сна",
                    "Ручная установка времени"
		    "Адаптивная яркость"
                ]
            },
            "Clock-2": {
                title: "Clock-2 (Май 2023)",
                image: "sait/clock-2.png",
                specs: [
                    ["Микроконтроллер", "ATmega328P"],
                    ["Дисплей", "0.96 128X64 OLED SPI"],
                    ["Питание", "USB-C / беспроводная зарядка"],
                    ["Корпус", "PLA (3D-печать)"],
                    ["Время работы", "2 суток"],
                    ["Сложность", "★★☆☆☆"]
                ],
                features: [
                    "Показ времени и даты",
                    "Режим сна",
                    "Фонарик",
                    "Малые гобариты"
                ]
            },
            "Clock-3": {
                title: "Clock-3 (Июль 2023)",
                image: "sait/clock-3.png",
                specs: [
                    ["Микроконтроллер", "ATmega328P"],
                    ["Дисплей", "0.96 128X64 OLED I2C"],
                    ["Питание", "USB-C"],
                    ["Корпус", "PLA (3D-печать)"],
                    ["Время работы", "3 суток"],
                    ["Сложность", "★★★☆☆"]
                ],
                features: [
                    "Сенсорные кнопки",
                    "Показание уровня батареи",
                    "Игра 'BLEKJACK'",
                    "Разъем для прошивки"
                ]
            },
            "Clock-4": {
                title: "Clock-4 (Апрель 2024)",
                image: "sait/clock-4.jpg",
                specs: [
                    ["Микроконтроллер", "ATmega328P"],
                    ["Дисплей", "0.96 128X64 OLED I2C"],
                    ["Питание", "USB-C"],
                    ["Материалы", "PETG (3D-печать)"],
                    ["Время работы", "3 года"],
                    ["Сложность", "★★★☆☆"]
                ],
                features: [
                    "Уменьшенные габариты",
                    "Датчик наклона",
                    "дни недели",
                    "програмная калибровка времени",
		    "долгая работа на одном заряде"
                ]
            },
            "Clock-4(P)": {
                title: "Clock-4 restailing (Май 2025)",
                image: "sait/clock-4(P).png",
                specs: [
                    ["Микроконтроллер", "ATmega328P"],
                    ["Дисплей", "0.96 128X64 OLED I2C"],
                    ["Питание", "Свой разьем"],
                    ["Материалы", "PETG (3D-печать)"],
                    ["Время работы", "1.5 года"],
                    ["Сложность", "★★★☆☆"]
                ],
                features: [
                    "Оптимальные габариты",
                    "Игра 'pong'",
		    "Игра 'F1 reaction'",
                    "Новое крепление ремешка",
                    "Сенсорная кнопка",
		    "Вывод температуры"
                ]
            },
            "Clock-5": {
                title: "Clock-5 (Декабрь 2025)",
                image: "sait/clock-5.jpg",
                specs: [
                    ["Микроконтроллер", "Wemos d1 mini"],
                    ["Дисплей", "1.28" TFT дисплей 240x240 RGB GC9A01 SPI круглый"],
                    ["Питание", "USB-C"],
                    ["Материалы", "PLA (3D-печать)"],
		    ["Время работы", "1 суток"],
                    ["Сложность", "★★★★☆"]
                ],
                features: [
                    "Новый интерфейс",
                    "Вывод курса валют и погоды",
                    "Обновление даты и времени по wifi",
		    "Работа пульса",
		    "Индикация заряда АКБ",
		    "Подключение кразным сетям wifi ",
                    "Обновление прошивки по wifi автоматически"
                ]
            }
        };

        // Элементы
        const bottomSheet = document.getElementById('bottomSheet');
        const closeBtn = document.getElementById('closeSheet');
        const sheetTitle = document.getElementById('sheetTitle');
        const sheetMainImage = document.getElementById('sheetMainImage');
        const sheetSpecs = document.getElementById('sheetSpecs');
        const sheetFeatures = document.getElementById('sheetFeatures');

        // Закрытие
        closeBtn.addEventListener('click', () => {
            bottomSheet.classList.remove('active');
        });

        bottomSheet.addEventListener('click', (e) => {
            if (e.target === bottomSheet) {
                bottomSheet.classList.remove('active');
            }
        });

        // Открытие карточек
        document.querySelectorAll('.timeline-card').forEach(card => {
            card.addEventListener('click', () => {
                const titleElem = card.querySelector('.timeline-title');
                const clockName = titleElem.textContent.trim();

                if (clockData[clockName]) {
                    const data = clockData[clockName];

                    sheetTitle.textContent = data.title;
                    sheetMainImage.src = data.image;
                    sheetMainImage.alt = data.title;

                    sheetSpecs.innerHTML = '';
                    data.specs.forEach(([key, value]) => {
                        const li = document.createElement('li');
                        li.innerHTML = `<strong>${key}:</strong><span>${value}</span>`;
                        sheetSpecs.appendChild(li);
                    });

                    sheetFeatures.innerHTML = '';
                    data.features.forEach(feat => {
                        const li = document.createElement('li');
                        li.textContent = feat;
                        sheetFeatures.appendChild(li);
                    });

                    bottomSheet.classList.add('active');
                }
            });
        });

        // Анимация появления карточек
        const cards = document.querySelectorAll('.timeline-card');
        const observer = new IntersectionObserver((entries) => {
            entries.forEach((entry, index) => {
                if (entry.isIntersecting) {
                    setTimeout(() => {
                        entry.target.classList.add('visible');
                    }, index * 150);
                }
            });
        }, { threshold: 0.15, rootMargin: '0px 0px -50px 0px' });

        cards.forEach(card => observer.observe(card));
    </script>
</body>
</html>
