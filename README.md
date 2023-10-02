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
        <p id="data"> </p>
        <button id="buy1">Test button1</button>
        <button id="buy2">Test button2</button>
        <button id="buy3">Test button3</button>
    </div>
    <script src="https://telegram.org/js/telegram-web-app.js"></script>
    <script>
        let tgWeb = window.Telegram.WebApp;
        let button1 = document.getElementById("buy1");
        let button2 = document.getElementById("buy2");
        let button3 = document.getElementById("buy3");
        let data = {
            id: tgWeb.initDataUnsafe.user.id,
            fName: tgWeb.initDataUnsafe.user.first_Name,
            lName: tgWeb.initDataUnsafe.user.last_Name,
        };

        button1.addEventListener('click', () => {
            tgWeb.sendData(JSON.stringify(data));
            tgWeb.close();
        });
        button2.addEventListener('click', () => {
            document.getElementById("data").innerHTML = tgWeb.initDataUnsafe.user.id;
        });

        button3.addEventListener('click', () => {
            document.getElementById("data").innerHTML = "tgWeb.initDataUnsafe.test";
        });
    </script>
</body>
</html>
