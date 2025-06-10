<!DOCTYPE html>
<html lang="ja">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>森のアニメテーマ</title>
    <style>
        /* スタイルここから */
        body {
            font-family: 'Yomogi', cursive;
            background-color: #e8f5e9;
            background-image: url('https://i.pinimg.com/originals/25/9c/d4/259cd4b7a5979a9e1a1e4a6e5d9b9b6a.png');
            background-size: cover;
            margin: 0;
            padding: 0;
            color: #2e7d32;
        }

        .header {
            text-align: center;
            padding: 50px 0;
            background: rgba(255, 255, 255, 0.7);
        }

        h1 {
            font-size: 3em;
            text-shadow: 2px 2px 4px #81c784;
        }

        .nav {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin: 20px 0;
        }

        .nav a {
            text-decoration: none;
            color: white;
            background-color: #81c784;
            padding: 10px 20px;
            border-radius: 50px;
            transition: all 0.3s;
        }

        .nav a:hover {
            background-color: #2e7d32;
            transform: scale(1.1);
        }

        .content {
            padding: 20px;
            background: rgba(255, 255, 255, 0.8);
            max-width: 800px;
            margin: 20px auto;
            border-radius: 15px;
            box-shadow: 0 0 15px rgba(129, 199, 132, 0.5);
        }

        .footer {
            text-align: center;
            padding: 10px;
            background: rgba(129, 199, 132, 0.7);
            position: fixed;
            bottom: 0;
            width: 100%;
        }

        /* 光の粒アニメーション */
        @keyframes sparkle {
            0% { opacity: 0; }
            50% { opacity: 1; }
            100% { opacity: 0; }
        }

        .sparkle {
            position: absolute;
            background: white;
            border-radius: 50%;
            animation: sparkle 2s infinite;
        }
    </style>
    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Yomogi&display=swap" rel="stylesheet">
</head>
<body>
    <div class="header">
        <h1>ようこそ森へ</h1>
        <div class="nav">
            <a href="#">ホーム</a>
            <a href="#">について</a>
            <a href="#">ギャラリー</a>
            <a href="#">お問い合わせ</a>
        </div>
    </div>

    <div class="content">
        <h2>森の物語</h2>
        <p>このサイトはアニメのような緑の森をテーマにしています。リラックスできる空間をお楽しみください。</p>
        <p>🌿 自分でイラストやテキストを追加してみてね！</p>
    </div>

    <div class="footer">
        <p>© 2023 森のアニメテーマ</p>
    </div>

    <!-- 光の粒をランダムに生成 -->
    <script>
        document.addEventListener('DOMContentLoaded', function() {
            for (let i = 0; i < 50; i++) {
                createSparkle();
            }
        });

        function createSparkle() {
            const sparkle = document.createElement('div');
            sparkle.className = 'sparkle';
            
            // ランダムな位置とサイズ
            const size = Math.random() * 5 + 3;
            sparkle.style.width = `${size}px`;
            sparkle.style.height = `${size}px`;
            sparkle.style.left = `${Math.random() * 100}vw`;
            sparkle.style.top = `${Math.random() * 100}vh`;
            sparkle.style.animationDelay = `${Math.random() * 2}s`;
            
            document.body.appendChild(sparkle);
        }
    </script>
</body>
</html>
