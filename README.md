<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Social Media Links</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div class="container">
        <header>
            <h1>Welcome to My Social Media</h1>
        </header>
        <main>
            <section class="social-links">
                <a href="https://www.tiktok.com" target="_blank" class="social-link">
                    <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/e/e3/TikTok_logo_2021.svg/1200px-TikTok_logo_2021.svg.png" alt="TikTok" class="social-icon">
                </a>
                <a href="https://www.youtube.com" target="_blank" class="social-link">
                    <img src="https://upload.wikimedia.org/wikipedia/commons/4/42/YouTube_icon_%282013-2017%29.png" alt="YouTube" class="social-icon">
                </a>
                <a href="https://twitter.com" target="_blank" class="social-link">
                    <img src="https://upload.wikimedia.org/wikipedia/commons/6/60/Twitter_Logo_2021.svg" alt="Twitter" class="social-icon">
                </a>
                <a href="https://www.instagram.com" target="_blank" class="social-link">
                    <img src="https://upload.wikimedia.org/wikipedia/commons/a/a5/Instagram_icon.png" alt="Instagram" class="social-icon">
                </a>
                <a href="https://discord.com" target="_blank" class="social-link">
                    <img src="https://upload.wikimedia.org/wikipedia/commons/5/53/Discord_logo_2021.svg" alt="Discord" class="social-icon">
                </a>
            </section>
            <section class="about">
                <button class="info-btn" onclick="showInfo()">About Me</button>
                <div id="info" class="info-box" style="display:none;">
                    <p>Hello! I'm a passionate content creator who loves to connect with people. Follow me on my social media for updates!</p>
                </div>
            </section>
        </main>
    </div>
    <script>
        function showInfo() {
            var infoBox = document.getElementById('info');
            if (infoBox.style.display === 'none') {
                infoBox.style.display = 'block';
            } else {
                infoBox.style.display = 'none';
            }
        }
    </script>
</body>
</html>
