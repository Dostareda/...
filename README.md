<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ДОСТАР доставка еды</title>
    <style>
        body {
            background-color: #FFFFFF; /* Белый фон */
            font-family: Arial, sans-serif; /* Общий стандартный шрифт */
        }
        h1 {
            color: #008000; /* Зеленый цвет заголовка */
            text-align: center; /* Выравнивание заголовка */
        }
        /* Общие стили кнопок */
        button {
            padding: 10px 20px; /* Внутренние отступы */
            background-color: #FFFF00; /* Желтый фон */
            color: black; /* Черный текст */
            border: 1px solid green; /* Зеленая рамка */
            border-radius: 5px; /* Слегка закругленные углы */
            cursor: pointer;
            font-size: 16px; /* Размер текста */
            font-family: Arial, sans-serif; /* Стандартный шрифт для кнопок */
            text-align: center; /* Центрирование текста */
            flex-grow: 1; /* Кнопки занимают одинаковое пространство */
            max-width: 400px; /* Максимальная ширина кнопок */
            margin: 5px 0; /* Небольшой отступ между кнопками */
        }
        button:hover {
            background-color: #FFD700; /* Темно-желтый при наведении */
            color: black;
        }
        /* Контейнер для кнопок с автоматическим выравниванием */
        .button-container {
            display: flex; /* Используем flexbox */
            flex-direction: column; /* Вертикальное расположение кнопок */
            align-items: center; /* Центрирование кнопок по горизонтали */
            gap: 10px; /* Отступ между кнопками */
            margin: 20px 0;
        }
        footer {
            display: flex;
            justify-content: center;
            align-items: center;
            margin-top: 20px;
            font-size: 14px;
            color: #666666;
            gap: 10px; /* Отступ между элементами */
        }
        footer a {
            color: #808080;
            text-decoration: none;
        }
        footer a:hover {
            text-decoration: underline;
        }
        #visitor-count {
            font-size: 14px;
            color: #555555;
        }
    </style>
</head>
<body>
    <!-- Добавлен перенос строки после слова "ДОСТАР" -->
    <h1>"ДОСТАР"<br>ДОСТАВКА ЕДЫ</h1>

    <!-- Контейнер с автоматическим выравниванием кнопок -->
    <div class="button-container">
        <button id="openWhatsApp1">Шашлык "Триумф" нажмите чтобы заказать</button>
        <button id="openWhatsApp2">Донер нажмите чтобы заказать</button>
    </div>

    <!-- Счетчик и пользовательское соглашение в футере -->
    <footer>
        <div id="visitor-count">Посетители: 0</div>
        <a href="terms.html" target="_blank">Пользовательское соглашение</a>
    </footer>

    <script>
        // Счетчик посещений
        function updateVisitorCount() {
            if (localStorage.getItem("visitorCount")) {
                let count = parseInt(localStorage.getItem("visitorCount"), 10);
                count++;
                localStorage.setItem("visitorCount", count);
                document.getElementById("visitor-count").innerText = `Посетители: ${count}`;
            } else {
                localStorage.setItem("visitorCount", 1);
                document.getElementById("visitor-count").innerText = `Посетители: 1`;
            }
        }

        // Обновляем счетчик при загрузке страницы
        updateVisitorCount();

        // Обработчик для первой кнопки
        const button1 = document.getElementById("openWhatsApp1");
        button1.addEventListener("click", function () {
            const phoneNumber1 = "77474705053";
            const url1 = `https://api.whatsapp.com/send?phone=${phoneNumber1}`;
            window.open(url1, "_blank");
        });

        // Обработчик для второй кнопки
        const button2 = document.getElementById("openWhatsApp2");
        button2.addEventListener("click", function () {
            const phoneNumber2 = "77081175050";
            const url2 = `https://api.whatsapp.com/send?phone=${phoneNumber2}`;
            window.open(url2, "_blank");
        });
    </script>
</body>
</html>
