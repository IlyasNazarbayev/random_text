<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Случайный текст</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            margin-top: 50px;
            padding: 20px;
            background-color: #f9f9f9;
        }
        .random-text {
            font-size: 24px;
            color: #333;
            font-style: italic;
            margin-top: 20px;
        }
        .author {
            font-size: 18px;
            color: #666;
            margin-top: 10px;
        }
    </style>
</head>
<body>
    <div class="random-text" id="randomText"></div>
    <div class="author" id="authorText"></div>

    <script>
        // Массив текстов с цитатами и авторами
        const texts = [
            { text: "Carrie reminds me of a heroine who has lost her moral compass.", author: "Anne Brontë" },
            { text: "She fights for freedom, but does she truly know what she wants?", author: "Anne Brontë" },
            { text: "Had Carrie lived in my time, society would have condemned her, yet today she is a symbol of change.", author: "Anne Brontë" },
            { text: "In the steppe, her path would have been different—she would seek balance, not just success.", author: "Chingiz Aitmatov" },
            { text: "A person without roots is like a river without a course—Carrie moves forward, but where to?", author: "Chingiz Aitmatov" },
            { text: "Instead of chasing the empty lights of the big city, she should have found the fire within herself.", author: "Chingiz Aitmatov" },
            { text: "She is like a city—shining on the outside, but empty within.", author: "Sergey Yesenin" },
            { text: "Carrie is an autumn leaf in the wind, not knowing where home is.", author: "Sergey Yesenin" },
            { text: "She should have lived in the countryside, gazing at the stars, rather than chasing someone else’s dreams.", author: "Sergey Yesenin" },
            { text: "She keeps moving forward, but has she lost something important along the way?", author: "Sergey Yesenin" }
        ];

        // Функция для выбора случайного текста
        function getRandomText() {
            const randomIndex = Math.floor(Math.random() * texts.length);
            return texts[randomIndex];
        }

        // Показываем случайный текст и автора при загрузке страницы
        window.onload = function() {
            const randomTextElement = document.getElementById("randomText");
            const authorTextElement = document.getElementById("authorText");
            const randomTextData = getRandomText();

            randomTextElement.textContent = `"${randomTextData.text}"`;
            authorTextElement.textContent = `— ${randomTextData.author}`;
        };

        // Обновляем текст и автора при клике на странице
        document.body.addEventListener("click", function() {
            const randomTextElement = document.getElementById("randomText");
            const authorTextElement = document.getElementById("authorText");
            const randomTextData = getRandomText();

            randomTextElement.textContent = `"${randomTextData.text}"`;
            authorTextElement.textContent = `— ${randomTextData.author}`;
        });
    </script>
</body>
</html>
