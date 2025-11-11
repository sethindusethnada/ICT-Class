<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Information & Communication Technology | Dompe ICT Class</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: #333;
            line-height: 1.6;
            overflow-x: hidden;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }

        /* Header Styles */
        header {
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(10px);
            padding: 40px 20px;
            text-align: center;
            border-radius: 20px;
            margin: 20px;
            box-shadow: 0 20px 60px rgba(0, 0, 0, 0.3);
            animation: fadeInDown 1s ease;
        }

        h1 {
            font-size: 3em;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            margin-bottom: 10px;
            font-weight: 700;
        }

        .subtitle {
            font-size: 1.2em;
            color: #666;
            font-weight: 300;
        }

        /* Hero Section */
        .hero {
            background: white;
            border-radius: 20px;
            padding: 60px 40px;
            margin: 30px 20px;
            box-shadow: 0 20px 60px rgba(0, 0, 0, 0.3);
            animation: fadeInUp 1s ease;
            text-align: center;
        }

        .hero-image {
            width: 400px;
            height: 400px;
            border-radius: 20px;
            object-fit: cover;
            box-shadow: 0 15px 40px rgba(102, 126, 234, 0.4);
            transition: transform 0.3s ease;
            margin: 20px 0;
        }

        .hero-image:hover {
            transform: scale(1.05) rotate(2deg);
        }

        /* About Section */
        .about-section {
            background: rgba(255, 255, 255, 0.95);
            border-radius: 20px;
            padding: 50px 40px;
            margin: 30px 20px;
            box-shadow: 0 20px 60px rgba(0, 0, 0, 0.3);
            animation: fadeIn 1.2s ease;
        }

        .section-title {
            font-size: 2.5em;
            color: #667eea;
            margin-bottom: 20px;
            text-align: center;
            position: relative;
            padding-bottom: 15px;
        }

        .section-title::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 50%;
            transform: translateX(-50%);
            width: 100px;
            height: 4px;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            border-radius: 2px;
        }

        .about-text {
            font-size: 1.2em;
            color: #555;
            text-align: center;
            max-width: 800px;
            margin: 30px auto;
            line-height: 1.8;
        }

        /* Teacher Section */
        .teacher-section {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            border-radius: 20px;
            padding: 50px 40px;
            margin: 30px 20px;
            box-shadow: 0 20px 60px rgba(0, 0, 0, 0.3);
            color: white;
            text-align: center;
            animation: fadeInLeft 1s ease;
        }

        .teacher-card {
            background: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(10px);
            border-radius: 20px;
            padding: 40px;
            max-width: 500px;
            margin: 30px auto;
            border: 2px solid rgba(255, 255, 255, 0.2);
            transition: transform 0.3s ease;
        }

        .teacher-card:hover {
            transform: translateY(-10px);
        }

        .teacher-image {
            width: 200px;
            height: 200px;
            border-radius: 50%;
            border: 5px solid white;
            box-shadow: 0 15px 40px rgba(0, 0, 0, 0.3);
            margin-bottom: 20px;
            object-fit: cover;
        }

        .teacher-name {
            font-size: 2em;
            margin: 20px 0;
            font-weight: 600;
        }

        /* Students Section */
        .students-section {
            background: white;
            border-radius: 20px;
            padding: 50px 40px;
            margin: 30px 20px;
            box-shadow: 0 20px 60px rgba(0, 0, 0, 0.3);
            animation: fadeInRight 1s ease;
        }

        .students-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            margin-top: 30px;
        }

        .student-card {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 25px;
            border-radius: 15px;
            text-align: center;
            font-size: 1.1em;
            font-weight: 500;
            box-shadow: 0 10px 30px rgba(102, 126, 234, 0.3);
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }

        .student-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: rgba(255, 255, 255, 0.1);
            transition: left 0.3s ease;
        }

        .student-card:hover::before {
            left: 100%;
        }

        .student-card:hover {
            transform: translateY(-5px) scale(1.05);
            box-shadow: 0 15px 40px rgba(102, 126, 234, 0.5);
        }

        .student-number {
            font-size: 2em;
            opacity: 0.3;
            font-weight: 700;
            margin-bottom: 10px;
        }

        /* Footer */
        footer {
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(10px);
            border-radius: 20px;
            padding: 40px;
            margin: 30px 20px 20px;
            text-align: center;
            box-shadow: 0 20px 60px rgba(0, 0, 0, 0.3);
            animation: fadeInUp 1.2s ease;
        }

        footer p {
            color: #555;
            margin: 10px 0;
            font-size: 1em;
        }

        .heart {
            color: #ff6b6b;
            animation: heartbeat 1.5s infinite;
        }

        .code {
            color: #667eea;
            font-weight: 600;
        }

        /* Animations */
        @keyframes fadeInDown {
            from {
                opacity: 0;
                transform: translateY(-50px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(50px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        @keyframes fadeIn {
            from {
                opacity: 0;
            }
            to {
                opacity: 1;
            }
        }

        @keyframes fadeInLeft {
            from {
                opacity: 0;
                transform: translateX(-50px);
            }
            to {
                opacity: 1;
                transform: translateX(0);
            }
        }

        @keyframes fadeInRight {
            from {
                opacity: 0;
                transform: translateX(50px);
            }
            to {
                opacity: 1;
                transform: translateX(0);
            }
        }

        @keyframes heartbeat {
            0%, 100% { transform: scale(1); }
            50% { transform: scale(1.1); }
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            h1 {
                font-size: 2em;
            }

            .section-title {
                font-size: 1.8em;
            }

            .hero-image {
                width: 300px;
                height: 300px;
            }

            .students-grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <h1>Information & Communication<br>Technology</h1>
            <p class="subtitle">Excellence in Digital Education</p>
        </header>

        <section class="hero">
            <img src="https://tse1.mm.bing.net/th/id/OIP.RpWfnayfLUwGUZMtpndCVAHaHa?cb=ucfimgc2&rs=1&pid=ImgDetMain&o=7&rm=3" alt="ICT Class" class="hero-image">
        </section>

        <section class="about-section">
            <h2 class="section-title">ICT Group Class, Dompe</h2>
            <p class="about-text">
                Welcome to our vibrant ICT learning community in Dompe! Our class brings together seven enthusiastic students under the expert guidance of our talented instructor, Dilshan Andaramana. We foster a dynamic learning environment where education meets enjoyment, combining rigorous technical training with a friendly, collaborative atmosphere. Together, we explore the exciting world of technology while building lasting friendships and valuable skills.
            </p>
        </section>

        <section class="teacher-section">
            <h2 class="section-title" style="color: white;">Our Teacher</h2>
            <div class="teacher-card">
                <img src="https://th.bing.com/th/id/OIP.vQBe6L3FpuMHO-z8PiexFQHaHa?w=160&h=180&c=7&r=0&o=7&cb=ucfimgc2&dpr=1.3&pid=1.7&rm=3" alt="Dilshan Andaramana" class="teacher-image">
                <h3 class="teacher-name">Dilshan Andaramana</h3>
                <p style="font-size: 1.1em; line-height: 1.8;">Expert ICT Instructor & Mentor</p>
            </div>
        </section>

        <section class="students-section">
            <h2 class="section-title">Our Students</h2>
            <div class="students-grid">
                <div class="student-card">
                    <div class="student-number">01</div>
                    Sethindu Sethnada
                </div>
                <div class="student-card">
                    <div class="student-number">02</div>
                    Hiruja Senitha
                </div>
                <div class="student-card">
                    <div class="student-number">03</div>
                    Yasith Yositha
                </div>
                <div class="student-card">
                    <div class="student-number">04</div>
                    Pemitha Sasrutha
                </div>
                <div class="student-card">
                    <div class="student-number">05</div>
                    Madushan
                </div>
                <div class="student-card">
                    <div class="student-number">06</div>
                    Haritha
                </div>
                <div class="student-card">
                    <div class="student-number">07</div>
                    Udithma Thathasara
                </div>
            </div>
        </section>

        <footer>
            <p>&copy; 2025 Sethindu Sethnada. All rights reserved.</p>
            <p>Designed & Developed with <span class="heart">❤️</span> and <span class="code">Code</span></p>
        </footer>
    </div>
</body>
</html>
