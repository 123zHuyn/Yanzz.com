<!DOCTYPE html>
<html lang="th">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Invite Yanzz's Discord Bot</title>
    <style>
        /* ตั้งค่าพื้นฐาน */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Arial', sans-serif;
            background-color: #2c2f33;
            color: #fff;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            padding: 20px;
        }

        .container {
            text-align: center;
            background-color: #23272a;
            padding: 40px;
            border-radius: 10px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.3);
            max-width: 500px;
            width: 100%;
        }

        h1 {
            color: #7289da;
            font-size: 2.5rem;
            margin-bottom: 20px;
        }

        p {
            font-size: 1.2rem;
            margin-bottom: 30px;
        }

        .invite-btn {
            display: inline-block;
            padding: 15px 30px;
            background-color: #7289da;
            color: white;
            font-size: 1.2rem;
            text-decoration: none;
            border-radius: 5px;
            transition: background-color 0.3s ease;
        }

        .invite-btn:hover {
            background-color: #5b6eae;
        }

        .bot-icon {
            width: 100px;
            height: 100px;
            border-radius: 50%;
            margin: 0 auto 20px auto; /* ปรับให้ไอคอนอยู่ตรงกลาง */
            background-color: #7289da;
            background-position: center;
            background-size: cover;
        }

        .error-msg {
            color: #ff4d4d;
            font-size: 1rem;
            display: none;
        }

        /* สำหรับขนาดหน้าจอเล็ก */
        @media (max-width: 768px) {
            h1 {
                font-size: 2rem;
            }

            p {
                font-size: 1rem;
            }

            .invite-btn {
                padding: 10px 20px;
                font-size: 1rem;
            }
        }
    </style>
</head>
<body>

    <div class="container">
        <h1>Invite Yanzz's Bot</h1>
        <div id="bot-icon" class="bot-icon"></div>
        <p>เชิญบอทของฉันเพื่อเพิ่มประสิทธิภาพให้กับ Discord Server ของคุณ!</p>
        <a href="https://discord.com/oauth2/authorize?client_id=1243606891666608269" class="invite-btn">Invite Now</a>
        <p id="error-msg" class="error-msg">ไม่พบไอคอนของบอท, ใช้รูปภาพเริ่มต้นแทน</p>
    </div>

    <script>
        // ลิงก์ภาพไอคอนบอท (ที่คุณให้มา)
        const botIconUrl = 'https://cdn.discordapp.com/avatars/1243606891666608269/613bd672e9cab7cc80bc03b440a31327.png?size=2048';

        const botIconElement = document.getElementById('bot-icon');
        const errorMsgElement = document.getElementById('error-msg');

        // ฟังก์ชันตรวจสอบว่ารูปภาพโหลดได้หรือไม่
        function checkBotIcon(url) {
            const img = new Image();
            img.src = url;

            img.onload = function() {
                botIconElement.style.backgroundImage = `url(${url})`;
            };

            img.onerror = function() {
                // ถ้าภาพโหลดไม่ได้ จะแสดงข้อความแจ้งเตือน
                errorMsgElement.style.display = 'block';
            };
        }

        // เรียกใช้งานฟังก์ชันตรวจสอบไอคอน
        checkBotIcon(botIconUrl);
    </script>

</body>
</html>
