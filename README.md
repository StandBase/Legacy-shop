<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Магазин</title>
    <style>
        body {
            font-family: 'Roboto', sans-serif;
            margin: 0;
            padding: 0;
            background: #2C2C1B; /* Тёмно-жёлтый фон */
            color: #FFF8E1; /* Светлый жёлтый текст */
        }
        header {
            background: linear-gradient(90deg, #444, #222); /* Тёмно-серая тема для шапки */
            padding: 10px 20px;
            color: #FFF8E1;
            display: flex;
            justify-content: space-between;
            align-items: center;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.2);
            position: fixed;
            top: 0;
            width: 100%;
            z-index: 1000;
        }
        header nav {
            display: flex;
            gap: 20px;
            align-items: center;
        }
        header nav a {
            color: #FFF8E1;
            text-decoration: none;
            font-size: 18px;
            padding: 10px 20px;
            border-radius: 5px;
            transition: background 0.3s;
        }
        header nav a:hover {
            background: #FFC107;
        }
        .start-game {
            background: #333; /* Тёмный фон кнопки */
            color: #FFF8E1;
            padding: 10px 20px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            font-size: 18px;
            transition: background 0.3s, transform 0.2s;
            margin-left: -40px; /* Сдвиг кнопки ещё левее */
        }
        .start-game:hover {
            background: #444;
            transform: scale(1.05);
        }
        .container {
            max-width: 1200px;
            margin: 130px auto 20px;
            padding: 20px;
            background: #3E3E2D; /* Тёмно-жёлто-зеленый фон */
            border-radius: 8px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.5);
        }
        .section-links {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-bottom: 20px;
        }
        .section-links a {
            color: #FFF8E1;
            text-decoration: none;
            padding: 10px 15px;
            background: #FFC107;
            border-radius: 5px;
            transition: background 0.3s, transform 0.2s;
        }
        .section-links a:hover {
            background: #FF9800;
            transform: scale(1.1);
        }
        .items {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
        }
        .item {
            background: #4E4E33; /* Тёмно-жёлто-зеленый фон для предметов */
            border-radius: 8px;
            text-align: center;
            padding: 15px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.3);
            transition: background 0.3s;
        }
        .item:hover {
            background: #FFEB3B; /* Светло-желтая при наведении */
            color: #2C2C1B;
        }
        .item img {
            width: 100%;
            height: auto;
            max-width: 300px;
            margin: 0 auto 10px;
            border-radius: 10px;
            object-fit: cover;
        }
        .item h3 {
            margin: 10px 0;
            color: inherit;
        }
        .item p {
            margin: 5px 0 10px;
            color: inherit;
        }
        .price {
            font-weight: bold;
            color: #FF5722;
            margin: 10px 0;
        }
        .btn {
            background: #FFEB3B; /* Желто-оранжевый градиент */
            color: #2C2C1B;
            border: none;
            padding: 10px 20px;
            border-radius: 5px;
            cursor: pointer;
            transition: background 0.3s, transform 0.2s, color 0.2s;
        }
        .hidden {
            display: none;
        }
        .message {
            text-align: center;
            font-size: 18px;
            color: #FFF8E1;
            margin-top: 20px;
        }
    </style>
</head>
<body>
    <header>
        <nav>
            <a href="https://standbase.github.io/Legacy/" target="_blank">Главная</a>
            <a href="https://standbase.github.io/Legacy-shop/" target="_blank">Магазин</a>
            <a href="https://standbase.github.io/Legacy-forum/" target="_blank">Форум</a>
        </nav>
        <button class="start-game">Начать игру</button>
    </header>

    <div class="container">
        <!-- Navigation links section above the items -->
        <div class="section-links">
            <a href="#" onclick="showSection('main')">Главная</a>
            <a href="#" onclick="showSection('misc')">Разное</a>
            <a href="#" onclick="showSection('vip')">VIP</a>
            <a href="#" onclick="showSection('skins')">Скины</a>
            <a href="#" onclick="showSection('cars')">Машины</a>
            <a href="#" onclick="showSection('accessories')">Аксессуары</a>
        </div>

        <!-- Main content (items) -->
        <div class="items">
            <div class="item">
                <img src="https://pc.rod-ins.com/resource/web/arizona/shop/cards/50049.jpg" alt="AZ Монета">
                <h3>AZ Монета</h3>
                <p>Донат валюта</p>
                <button class="btn" onclick="location.href='https://t.me'">Приобрести</button>
            </div>

            <div class="item">
                <img src="https://pc.rod-ins.com/resource/web/arizona/shop/cards/scm_pack2.jpg" alt="Набор Основателя">
                <h3>Набор Основателя</h3>
                <p>Случайный скин</p>
                <p>рандомная машина</p>
                <p>15 000 000 виртов</p>
                <button class="btn" onclick="location.href='https://t.me'">100 рублей</button>
            </div>

            <div class="item">
                <img src="https://pc.rod-ins.com/resource/web/arizona/shop/cards/starting_capital_1.jpg" alt="Стартовый капитал №1">
                <h3>Стартовый капитал №1</h3>
                <p>10 500 000 виртов</p>
                <p>10 случайных ларцов</p>
                <button class="btn" onclick="location.href='https://t.me'">50 рублей</button>
            </div>
        </div>

    </div>

    <div class="container hidden" id="misc">
        <p class="message">Раздел в разработке. Пожалуйста, зайдите позже!</p>
    </div>

    <div class="container hidden" id="vip">
        <p class="message">Раздел в разработке. Пожалуйста, зайдите позже!</p>
    </div>

    <div class="container hidden" id="skins">
        <p class="message">Раздел в разработке. Пожалуйста, зайдите позже!</p>
    </div>

    <div class="container hidden" id="cars">
        <p class="message">Раздел в разработке. Пожалуйста, зайдите позже!</p>
    </div>

    <div class="container hidden" id="accessories">
        <p class="message">Раздел в разработке. Пожалуйста, зайдите позже!</p>
    </div>

    <script>
        function showSection(sectionId) {
            document.querySelectorAll('.container').forEach(section => {
                section.classList.add('hidden');
            });
            document.getElementById(sectionId).classList.remove('hidden');
        }
    </script>
</body>
</html>
