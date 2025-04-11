<!DOCTYPE html>
<html lang="zh-Hant">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>點擊計數器</title>
    <style>
        body {
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            height: 100vh;
            margin: 0;
            background-color: #f0f0f0;
            font-family: Arial, sans-serif;
        }
        #clicker {
            width: 300px;
            height: 300px;
            background-image: url(p1.jpeg); /* 圖一的 URL */
            background-size: cover;
            cursor: pointer;
            transition: transform 0.1s;
        }
        #clicker:active {
            transform: scale(0.95);
        }
        #count {
            font-size: 24px;
            margin-top: 20px;
        }
    </style>
</head>
<body>
    <div id="clicker" onclick="incrementCount()"></div>
    <div id="count">點擊次數: 0</div>

    <script>
        let count = 0;
        let clicked = false;

        function incrementCount() {
            count++;
            document.getElementById('count').innerText = '點擊次數: ' + count;

            const clicker = document.getElementById('clicker');
            clicked = !clicked; // 切換狀態

            if (clicked) {
                clicker.style.backgroundImage = "url(p2.jpeg)"; // 圖二的 URL
            } else {
                clicker.style.backgroundImage = "url(p1.jpeg)"; // 圖一的 URL
            }
        }
    </script>
</body>
</html>
