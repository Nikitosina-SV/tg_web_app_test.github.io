<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport"
          content="width=device-width, user-scalable=no, initial-scale=1.0, maximum-scale=1.0, minimum-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>TestWebApp</title>
</head>
<body>
    <div id="main">
        <h1>Telegram Web App</h1>
        <img src="https://fuzeservers.ru/wp-content/uploads/e/6/5/e6582e3f04d623bb4823f869c9a53c5d.png">
        <p>Testing data sending</p>
        <button id="buy">Test button</button>
    </div>
    <script src="https://telegram.org/js/telegram-web-app.js"></script>
    <script>
        let tgWeb = window.Telegram.WebApp;
        let button = document.getElementById("buy");

        button.addEventListener('click', () => {
            tgWeb.close();
        });
    </script>
</body>
</html>
