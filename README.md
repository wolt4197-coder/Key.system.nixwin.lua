<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Nixwin.lua | Key System</title>
    <style>
        body {
            background-color: #0f0f0f;
            color: white;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
        }
        .container {
            background-color: #1a1a1a;
            padding: 30px;
            border-radius: 12px;
            box-shadow: 0 8px 24px rgba(0,0,0,0.5);
            text-align: center;
            width: 350px;
            border: 1px solid #333;
        }
        h2 { color: #00ff88; margin-bottom: 10px; }
        p { color: #aaa; font-size: 14px; }
        .btn {
            display: block;
            width: 100%;
            padding: 12px;
            margin: 10px 0;
            border: none;
            border-radius: 6px;
            background-color: #333;
            color: white;
            cursor: pointer;
            font-weight: bold;
            transition: 0.3s;
        }
        .btn.active { background-color: #00ff88; color: #000; }
        .btn:disabled { opacity: 0.5; cursor: not-allowed; }
        #key-display {
            margin-top: 20px;
            padding: 10px;
            background: #222;
            border: 1px dashed #00ff88;
            display: none;
        }
    </style>
</head>
<body>

<div class="container">
    <h2>Nixwin.lua</h2>
    <p>Чтобы получить ключ, выполните 2 задания:</p>
    
    <button id="task1" class="btn active" onclick="completeTask(1)">1. Перейти в Телеграм</button>
    <button id="task2" class="btn" onclick="completeTask(2)" disabled>2. Подписаться на канал</button>
    
    <div id="key-display">
        <p>Ваш ключ:</p>
        <strong id="key-value">NIX-WIN-777-XYZ</strong>
    </div>
    
    <button id="get-key" class="btn" style="display:none;" onclick="showKey()">Получить ключ</button>
</div>

<script>
    let step = 0;

    function completeTask(taskNum) {
        if (taskNum === 1) {
            // Здесь должна быть ссылка на Linkvertise или другое задание
            window.open('https://t.me/your_channel', '_blank');
            
            setTimeout(() => {
                document.getElementById('task1').disabled = true;
                document.getElementById('task1').innerText = '✅ Задание 1 выполнено';
                document.getElementById('task1').classList.remove('active');
                
                document.getElementById('task2').disabled = false;
                document.getElementById('task2').classList.add('active');
            }, 2000);
        } else if (taskNum === 2) {
            window.open('https://youtube.com/your_channel', '_blank');
            
            setTimeout(() => {
                document.getElementById('task2').disabled = true;
                document.getElementById('task2').innerText = '✅ Задание 2 выполнено';
                document.getElementById('task2').classList.remove('active');
                
                document.getElementById('get-key').style.display = 'block';
                document.getElementById('get-key').classList.add('active');
            }, 2000);
        }
    }

    function showKey() {
        document.getElementById('key-display').style.display = 'block';
        document.getElementById('get-key').style.display = 'none';
    }
</script>

</body>
</html>

