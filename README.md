<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>For Saad Lodhi ❤️</title>
    <style>
        body { 
            text-align: center; 
            font-family: 'Arial', sans-serif; 
            background-color: #ffeff5; 
            display: flex; 
            flex-direction: column; 
            justify-content: center; 
            align-items: center; 
            height: 100vh; 
            margin: 0; 
            overflow: hidden; 
        }
        .container { z-index: 10; background: white; padding: 40px; border-radius: 30px; box-shadow: 0 10px 30px rgba(214, 51, 132, 0.2); border: 2px solid #ffb3d1; }
        h1 { color: #d63384; font-size: 2.2rem; margin-bottom: 25px; line-height: 1.4; }
        .buttons { position: relative; height: 100px; width: 100%; display: flex; justify-content: center; align-items: center; }
        button { padding: 15px 35px; font-size: 1.2rem; cursor: pointer; border-radius: 50px; border: none; transition: 0.3s; position: absolute; font-weight: bold; }
        #yesBtn { background-color: #ff4d4d; color: white; transform: translateX(-70px); box-shadow: 0 4px 15px rgba(255, 77, 77, 0.4); }
        #noBtn { background-color: #808080; color: white; transform: translateX(70px); transition: 0.15s; }
        
        .heart { position: absolute; color: #ff4d4d; animation: float 4s linear infinite; font-size: 25px; z-index: 1; opacity: 0.6; }
        @keyframes float {
            0% { transform: translateY(110vh) rotate(0deg); opacity: 0.8; }
            100% { transform: translateY(-10vh) rotate(360deg); opacity: 0; }
        }
    </style>
</head>
<body>

    <div class="container" id="mainCard">
        <h1>Hey Saad Lodhi, <br> Will you be my Valentine? ❤️</h1>
        <div class="buttons">
            <button id="yesBtn" onclick="celebrate()">Yes!</button>
            <button id="noBtn" onmouseover="moveButton()" onclick="moveButton()">No</button>
        </div>
    </div>

    <script>
        // Create floating background hearts
        setInterval(() => {
            const heart = document.createElement('div');
            heart.classList.add('heart');
            heart.innerHTML = '❤️';
            heart.style.left = Math.random() * 100 + 'vw';
            heart.style.animationDuration = (Math.random() * 2 + 3) + 's';
            document.body.appendChild(heart);
            setTimeout(() => heart.remove(), 4000);
        }, 400);

        function moveButton() {
            const btn = document.getElementById('noBtn');
            const x = Math.random() * (window.innerWidth - btn.offsetWidth);
            const y = Math.random() * (window.innerHeight - btn.offsetHeight);
            btn.style.position = 'fixed';
            btn.style.left = x + 'px';
            btn.style.top = y + 'px';
            btn.style.transform = 'none';
        }

        function celebrate() {
            const card = document.getElementById('mainCard');
            card.innerHTML = `
                <h1 style="font-size: 3rem;">YAY! 🥰</h1>
                <p style="font-size: 1.4rem; color: #d63384; font-weight: bold;">
                    Saad Lodhi + Shayahhh <br> ❤️ Forever ❤️
                </p>
            `;
            // Add extra celebration hearts instantly
            for(let i=0; i<30; i++) {
                setTimeout(() => {
                    const heart = document.createElement('div');
                    heart.innerHTML = '💖';
                    heart.className = 'heart';
                    heart.style.left = Math.random() * 100 + 'vw';
                    heart.style.fontSize = '40px';
                    document.body.appendChild(heart);
                }, i * 100);
            }
        }
    </script>
</body>
</html>
