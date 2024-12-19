# سنقوم بضغط الكود الخاص بالموقع في ملف ZIP حتى تتمكن من تنزيله واستخدامه بسهولة

import zipfile
import os

# مسار الملف المضغوط النهائي
zip_path = '/mnt/data/personal_website.zip'

# مسار ملف HTML
html_content = """<!DOCTYPE html>
<html lang="ar">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Personal | مشعل</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Arial', sans-serif;
            background: linear-gradient(135deg, #2c003e, #6a0dad);
            color: #fff;
            text-align: center;
            overflow-x: hidden;
        }

        header {
            padding: 50px 0;
        }

        .logo {
            font-size: 3rem;
            font-weight: bold;
            color: #fff;
            text-shadow: 0 0 10px #fff, 0 0 20px #ff00ff, 0 0 40px #ff00ff;
        }

        .bio {
            margin-top: 20px;
            font-size: 1.2rem;
            line-height: 1.6;
        }

        .social-links {
            margin-top: 30px;
            display: flex;
            justify-content: center;
            gap: 20px;
        }

        .social-links a {
            color: #fff;
            font-size: 1.2rem;
            text-decoration: none;
            text-align: center;
        }

        .social-links a span {
            display: block;
            font-size: 0.8rem;
            color: #ddd;
            margin-top: 5px;
        }

        .social-links a:hover {
            color: #ff00ff;
        }

        footer {
            margin-top: 50px;
            padding: 20px;
            background-color: #1a001f;
        }

        footer p {
            font-size: 0.9rem;
            color: #bbb;
        }

        footer a {
            color: #ff00ff;
            text-decoration: none;
        }

        footer a:hover {
            text-decoration: underline;
        }

        .math-background {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: -1;
            overflow: hidden;
        }

        .math-symbol {
            position: absolute;
            font-size: 2rem;
            color: rgba(255, 255, 255, 0.1);
            animation: float 10s linear infinite;
        }

        @keyframes float {
            from {
                transform: translateY(100vh) rotate(0deg);
            }
            to {
                transform: translateY(-100vh) rotate(360deg);
            }
        }
    </style>
</head>
<body>

<div class="math-background" id="math-background"></div>

<header>
    <h1 class="logo">Personal</h1>
    <p class="bio">I love to laugh | Best team for me #HalaMadrid | I like play, story game, shooter, Apex Legend has best game for me. I like series more than movies and anime.</p>
</header>

<section class="social-links">
    <a href="https://www.twitch.tv/personal_11" target="_blank">Twitch<span>ツイッチ</span></a>
    <a href="https://x.com/personal_11" target="_blank">X<span>エックス</span></a>
    <a href="https://www.youtube.com/@Personal_11/videos" target="_blank">YouTube<span>ユーチューブ</span></a>
    <a href="https://www.tiktok.com/@personal_l1?_t=8ockdfj2wf4&_r=1" target="_blank">TikTok<span>ティックトック</span></a>
    <a href="https://discord.gg/WUgj8CpxvG" target="_blank">Discord<span>ディスコード</span></a>
</section>

<footer>
    <p>&copy; 2024 Personal | جميع الحقوق محفوظة</p>
</footer>

<script>
    const symbols = ['π', '∞', '∑', '√', 'x', 'y', 'z', 'a', 'b', 'c', '+', '-', '=', '/', '*', 'E=mc^2', 'a^2 + b^2 = c^2', 'F=ma', 'y=mx+b', '∫ f(x) dx', 'Solve: 2x + 3 = 7', 'Simplify: (x + 2)(x - 2)', 'Find x: 5x - 15 = 0'];
    const mathBackground = document.getElementById('math-background');

    function createMathSymbols() {
        for (let i = 0; i < 50; i++) {
            const symbol = document.createElement('div');
            symbol.classList.add('math-symbol');
            symbol.textContent = symbols[Math.floor(Math.random() * symbols.length)];
            symbol.style.left = `${Math.random() * 100}%`;
            symbol.style.animationDuration = `${Math.random() * 10 + 5}s`;
            symbol.style.fontSize = `${Math.random() * 1.5 + 1}rem`;
            mathBackground.appendChild(symbol);
        }
    }

    createMathSymbols();
</script>

</body>
</html>
