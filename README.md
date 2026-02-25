<!DOCTYPE html>
<html lang="uk">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Android Control</title>
    <script src="https://telegram.org/js/telegram-web-app.js"></script>
    <style>
        body {
            font-family: sans-serif;
            background-color: #1c1c1c;
            color: white;
            margin: 0;
            padding: 15px;
            display: flex;
            flex-direction: column;
            gap: 15px;
        }
        .grid {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 10px;
        }
        .section-title {
            font-size: 14px;
            color: #888;
            text-transform: uppercase;
            margin-top: 10px;
        }
        button {
            background-color: #2b2b2b;
            color: white;
            border: 1px solid #444;
            padding: 15px 10px;
            border-radius: 12px;
            font-size: 14px;
            cursor: pointer;
            transition: 0.2s;
        }
        button:active {
            background-color: #444;
            transform: scale(0.95);
        }
        .btn-main {
            background: linear-gradient(135deg, #28a745, #1e7e34);
            grid-column: span 2;
            font-weight: bold;
        }
        .btn-danger {
            background: linear-gradient(135deg, #dc3545, #a71d2a);
        }
    </style>
</head>
<body>

    <div class="section-title">Основне керування</div>
    <div class="grid">
        <button class="btn-main" onclick="send('🚀 ПУСК')">🚀 ПУСК</button>
        <button onclick="send('🧠 AI ЧАТ')">🧠 AI ЧАТ</button>
        <button onclick="send('🌍 СИСТЕМА')">🌍 СИСТЕМА</button>
    </div>

    <div class="section-title">Файли та Медіа</div>
    <div class="grid">
        <button onclick="send('📁 ФАЙЛИ')">📁 ФАЙЛИ</button>
        <button onclick="send('📩 ЗАВАНТАЖИТИ')">📩 ЗАВАНТАЖИТИ</button>
        <button onclick="send('🌊 ТОРРЕНТ')">🌊 ТОРРЕНТ</button>
        <button onclick="send('📊 СТАТИСТИКА')">📊 СТАТИСТИКА</button>
    </div>

    <div class="section-title">Інструменти</div>
    <div class="grid">
        <button onclick="send('📝 БЛОКНОТ')">📝 БЛОКНОТ</button>
        <button onclick="send('📌 НАГАДУВАННЯ')">📌 НАГАДУВАННЯ</button>
        <button onclick="send('⏳ ТАЙМЕР')">⏳ ТАЙМЕР</button>
        <button onclick="send('⚡ СКРИПТИ')">⚡ СКРИПТИ</button>
        <button onclick="send('🧹 ОЧИЩЕННЯ')">🧹 ОЧИЩЕННЯ</button>
        <button onclick="send('📟 КОНСОЛЬ')">📟 КОНСОЛЬ</button>
    </div>

    <div class="section-title">Система</div>
    <div class="grid">
        <button onclick="send('🤖 БОТ')">🤖 БОТ</button>
        <button onclick="send('⚙️ НАЛАШТУВАННЯ')">⚙️ НАЛАШТУВАННЯ</button>
        <button class="btn-danger" onclick="send('💀 ВИМКНУТИ')">💀 ВИМКНУТИ</button>
    </div>

    <script>
        const tg = window.Telegram.WebApp;
        tg.expand(); // Розгортає вікно на весь екран

        function send(cmd) {
            tg.sendData(cmd); // Відправляє текст кнопки боту
        }
    </script>
</body>
</html>

