<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Happy New Year & Love ❤️</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        :root {
            --primary-color: #ff2e63;
            --secondary-color: #08d9d6;
            --accent-color: #ffde7d;
            --dark-color: #252a34;
            --light-color: #eaeaea;
        }
        
        body {
            background: var(--dark-color);
            color: var(--light-color);
            overflow-x: hidden;
            min-height: 100vh;
        }
        
        /* صفحة الدخول */
        .login-page {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(rgba(0, 0, 0, 0.8), rgba(0, 0, 0, 0.9)), url('https://images.unsplash.com/photo-1513297887119-d46091b24bfa?ixlib=rb-4.0.3&auto=format&fit=crop&w=2070&q=80');
            background-size: cover;
            background-position: center;
            display: flex;
            justify-content: center;
            align-items: center;
            z-index: 1000;
            transition: opacity 1.5s ease;
        }
        
        .login-container {
            background: rgba(37, 42, 52, 0.9);
            padding: 3rem;
            border-radius: 20px;
            box-shadow: 0 15px 35px rgba(255, 46, 99, 0.3);
            text-align: center;
            max-width: 500px;
            width: 90%;
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 222, 125, 0.2);
            animation: float 6s ease-in-out infinite;
        }
        
        @keyframes float {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-15px); }
        }
        
        .login-title {
            font-size: 2.8rem;
            margin-bottom: 0.5rem;
            background: linear-gradient(45deg, var(--primary-color), var(--accent-color));
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            font-weight: bold;
        }
        
        .login-subtitle {
            font-size: 1.2rem;
            margin-bottom: 2rem;
            color: var(--accent-color);
        }
        
        .password-container {
            position: relative;
            margin: 2rem 0;
        }
        
        .password-input {
            width: 100%;
            padding: 15px 20px;
            background: rgba(255, 255, 255, 0.1);
            border: 2px solid var(--primary-color);
            border-radius: 50px;
            color: white;
            font-size: 1.2rem;
            text-align: center;
            outline: none;
            transition: all 0.3s;
        }
        
        .password-input:focus {
            border-color: var(--secondary-color);
            box-shadow: 0 0 20px rgba(8, 217, 214, 0.5);
        }
        
        .password-label {
            position: absolute;
            top: -10px;
            left: 20px;
            background: var(--dark-color);
            padding: 0 10px;
            color: var(--accent-color);
            font-size: 0.9rem;
        }
        
        .unlock-btn {
            background: linear-gradient(45deg, var(--primary-color), #ff6b9d);
            color: white;
            border: none;
            padding: 15px 40px;
            border-radius: 50px;
            font-size: 1.2rem;
            font-weight: bold;
            cursor: pointer;
            transition: all 0.3s;
            margin-top: 1rem;
            box-shadow: 0 5px 15px rgba(255, 46, 99, 0.4);
        }
        
        .unlock-btn:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(255, 46, 99, 0.6);
        }
        
        .hint {
            margin-top: 1rem;
            color: var(--secondary-color);
            font-size: 0.9rem;
        }
        
        /* تأثيرات القلوب */
        .hearts-container {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: 2000;
        }
        
        .heart {
            position: absolute;
            font-size: 24px;
            opacity: 0;
            animation: floatUp 5s linear forwards;
        }
        
        @keyframes floatUp {
            0% {
                transform: translateY(100vh) rotate(0deg);
                opacity: 1;
            }
            100% {
                transform: translateY(-100px) rotate(360deg);
                opacity: 0;
            }
        }
        
        /* الصفحة الرئيسية */
        .main-page {
            display: none;
            opacity: 0;
            transition: opacity 1s ease;
        }
        
        .header {
            background: linear-gradient(to right, rgba(37, 42, 52, 0.95), rgba(255, 46, 99, 0.2));
            padding: 2rem;
            text-align: center;
            border-bottom: 2px solid var(--primary-color);
            position: relative;
            overflow: hidden;
        }
        
        .header::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: url('https://images.unsplash.com/photo-1518709268805-4e9042af2176?ixlib=rb-4.0.3&auto=format&fit=crop&w=2068&q=80');
            background-size: cover;
            opacity: 0.2;
            z-index: -1;
        }
        
        .main-title {
            font-size: 3.5rem;
            margin-bottom: 0.5rem;
            background: linear-gradient(45deg, var(--primary-color), var(--accent-color), var(--secondary-color));
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            text-shadow: 0 0 30px rgba(255, 46, 99, 0.5);
        }
        
        .subtitle {
            font-size: 1.5rem;
            color: var(--accent-color);
        }
        
        .year-badge {
            display: inline-block;
            background: linear-gradient(45deg, var(--primary-color), var(--secondary-color));
            color: white;
            padding: 5px 20px;
            border-radius: 30px;
            margin-top: 1rem;
            font-weight: bold;
            box-shadow: 0 5px 15px rgba(255, 46, 99, 0.4);
            animation: pulse 2s infinite;
        }
        
        @keyframes pulse {
            0%, 100% { transform: scale(1); }
            50% { transform: scale(1.05); }
        }
        
        /* أقسام المحتوى */
        .content-container {
            display: flex;
            flex-wrap: wrap;
            padding: 2rem;
            gap: 2rem;
        }
        
        .messages-section {
            flex: 2;
            min-width: 300px;
        }
        
        .media-section {
            flex: 1;
            min-width: 300px;
        }
        
        .section-title {
            font-size: 2rem;
            margin-bottom: 1.5rem;
            padding-bottom: 10px;
            border-bottom: 2px solid var(--primary-color);
            color: var(--accent-color);
            position: relative;
        }
        
        .section-title::after {
            content: '';
            position: absolute;
            bottom: -2px;
            left: 0;
            width: 100px;
            height: 2px;
            background: var(--secondary-color);
        }
        
        /* الرسائل */
        .message-card {
            background: rgba(255, 255, 255, 0.05);
            border-radius: 15px;
            padding: 2rem;
            margin-bottom: 2rem;
            border-left: 5px solid var(--primary-color);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
            transition: transform 0.3s;
        }
        
        .message-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 25px rgba(255, 46, 99, 0.2);
        }
        
        .message-title {
            font-size: 1.8rem;
            color: var(--secondary-color);
            margin-bottom: 1rem;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .poem {
            font-size: 1.3rem;
            line-height: 2.2;
            text-align: center;
            color: var(--light-color);
            font-family: 'Arial', sans-serif;
            margin: 1.5rem 0;
            padding: 1.5rem;
            background: rgba(255, 255, 255, 0.03);
            border-radius: 10px;
            border-right: 3px solid var(--accent-color);
        }
        
        .message-footer {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-top: 1.5rem;
            padding-top: 1rem;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            color: var(--accent-color);
        }
        
        .message-icon {
            font-size: 1.5rem;
            color: var(--primary-color);
        }
        
        /* قسم الوسائط */
        .media-card {
            background: rgba(255, 255, 255, 0.05);
            border-radius: 15px;
            padding: 1.5rem;
            margin-bottom: 2rem;
            text-align: center;
            border-top: 5px solid var(--secondary-color);
        }
        
        .video-placeholder {
            width: 100%;
            height: 200px;
            background: linear-gradient(45deg, rgba(255, 46, 99, 0.2), rgba(8, 217, 214, 0.2));
            border-radius: 10px;
            display: flex;
            justify-content: center;
            align-items: center;
            margin-bottom: 1rem;
            font-size: 4rem;
            color: var(--accent-color);
        }
        
        .video-title {
            font-size: 1.3rem;
            color: var(--light-color);
            margin-bottom: 0.5rem;
        }
        
        .video-desc {
            color: rgba(255, 255, 255, 0.7);
            font-size: 0.9rem;
        }
        
        .media-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(120px, 1fr));
            gap: 1rem;
            margin-top: 1.5rem;
        }
        
        .media-item {
            background: rgba(255, 255, 255, 0.05);
            border-radius: 10px;
            padding: 10px;
            text-align: center;
            transition: transform 0.3s;
        }
        
        .media-item:hover {
            transform: scale(1.05);
            background: rgba(255, 46, 99, 0.1);
        }
        
        .media-icon {
            font-size: 2rem;
            color: var(--secondary-color);
            margin-bottom: 5px;
        }
        
        /* التذييل */
        .footer {
            background: rgba(0, 0, 0, 0.5);
            padding: 2rem;
            text-align: center;
            margin-top: 3rem;
            border-top: 1px solid rgba(255, 46, 99, 0.3);
        }
        
        .love-message {
            font-size: 1.5rem;
            color: var(--primary-color);
            margin-bottom: 1rem;
        }
        
        .copyright {
            color: rgba(255, 255, 255, 0.6);
        }
        
        /* الأضواء والتأثيرات */
        .light-effect {
            position: fixed;
            width: 300px;
            height: 300px;
            border-radius: 50%;
            background: radial-gradient(circle, rgba(255, 46, 99, 0.2) 0%, transparent 70%);
            pointer-events: none;
            z-index: -1;
        }
        
        /* الشارات */
        .badge {
            display: inline-block;
            background: var(--primary-color);
            color: white;
            padding: 5px 15px;
            border-radius: 20px;
            font-size: 0.8rem;
            margin-left: 10px;
        }
        
        /* شريط التقدم */
        .progress-container {
            width: 100%;
            height: 5px;
            background: rgba(255, 255, 255, 0.1);
            position: fixed;
            top: 0;
            left: 0;
            z-index: 9999;
        }
        
        .progress-bar {
            height: 100%;
            background: linear-gradient(to right, var(--primary-color), var(--secondary-color));
            width: 0%;
            transition: width 0.3s;
        }
        
        /* التأثيرات الخاصة */
        .sparkle {
            position: absolute;
            width: 10px;
            height: 10px;
            background: white;
            border-radius: 50%;
            box-shadow: 0 0 10px white;
            animation: sparkleAnim 1s linear infinite;
        }
        
        @keyframes sparkleAnim {
            0%, 100% { opacity: 0; transform: scale(0); }
            50% { opacity: 1; transform: scale(1); }
        }
        
        /* التجاوب */
        @media (max-width: 768px) {
            .login-container {
                padding: 2rem;
            }
            
            .login-title {
                font-size: 2.2rem;
            }
            
            .main-title {
                font-size: 2.5rem;
            }
            
            .content-container {
                flex-direction: column;
            }
            
            .poem {
                font-size: 1.1rem;
                line-height: 1.8;
            }
        }
    </style>
</head>
<body>
    <!-- شريط التقدم -->
    <div class="progress-container">
        <div class="progress-bar" id="progressBar"></div>
    </div>
    
    <!-- صفحة الدخول -->
    <div class="login-page" id="loginPage">
        <div class="login-container">
            <h1 class="login-title">Secrets of the Heart ❤️</h1>
            <p class="login-subtitle">Unlock the message for a special person</p>
            
            <div class="password-container">
                <div class="password-label">Enter Password</div>
                <input type="text" class="password-input" id="passwordInput" placeholder="DD/MM">
            </div>
            
            <button class="unlock-btn" id="unlockBtn">
                <i class="fas fa-lock-open"></i> Unlock My Heart
            </button>
            
            <p class="hint">Hint: A special date (23/03)</p>
        </div>
    </div>
    
    <!-- حاوية القلوب للتأثيرات -->
    <div class="hearts-container" id="heartsContainer"></div>
    
    <!-- الأضواء المتحركة -->
    <div class="light-effect" id="light1"></div>
    <div class="light-effect" id="light2"></div>
    <div class="light-effect" id="light3"></div>
    
    <!-- الصفحة الرئيسية (مخفية في البداية) -->
    <div class="main-page" id="mainPage">
        <!-- الرأس -->
        <header class="header">
            <h1 class="main-title">To The Love of My Life ❤️</h1>
            <p class="subtitle">Messages from the heart for the new year and beyond</p>
            <div class="year-badge">New Year 2024 • New Beginnings</div>
        </header>
        
        <!-- المحتوى الرئيسي -->
        <div class="content-container">
            <!-- قسم الرسائل -->
            <section class="messages-section">
                <h2 class="section-title">
                    <i class="fas fa-heart"></i> Letters of Love
                </h2>
                
                <!-- الرسالة الأولى -->
                <div class="message-card">
                    <h3 class="message-title">
                        <i class="fas fa-star"></i> في بداية العام الجديد
                        <span class="badge">New Year</span>
                    </h3>
                    <div class="poem">
                        مع إشراقة فجر عام جديد..<br>
                        أبعثُ إليكِ بأحرِّ التهاني<br>
                        وأقول: كم أتمنى أن تكونِ<br>
                        سعادتي في جميع الأزمان<br><br>
                        
                        يا من بقلبكِ أسكنُ آمنًا<br>
                        كالعصفور في وكره الدافئ<br>
                        أهديكِ نبضات قلبي شعرًا<br>
                        وعودًا بأيامٍ أكثر رائعة<br>
                    </div>
                    <div class="message-footer">
                        <div class="message-date">1 يناير 2024</div>
                        <div class="message-icon">❤️</div>
                    </div>
                </div>
                
                <!-- الرسالة الثانية -->
                <div class="message-card">
                    <h3 class="message-title">
                        <i class="fas fa-moon"></i> حديث القلب
                        <span class="badge">Love</span>
                    </h3>
                    <div class="poem">
                        حبيبتي.. أنتِ النور في ظلامي<br>
                        والربيع في كلِّ أيامي<br>
                        بكِ أجدُ معنى للحياة<br>
                        وبقربكِ تزولُ الآلام<br><br>
                        
                        لو أن البحرَ يحملُ كلماتي<br>
                        لما وسعتْ حرفًا من أشواقي<br>
                        ولو أن الورقَ كانَ سمائي<br>
                        لما حوتْ سطرًا من أحلامي<br><br>
                        
                        أنتِ أكثر من مجرد حب<br>
                        أنتِ قصتي التي لن تكتمل<br>
                        إلا ببقائكِ إلى جانبي<br>
                        في رحلة العمر الطويلة<br>
                    </div>
                    <div class="message-footer">
                        <div class="message-date">للأبد</div>
                        <div class="message-icon">🌹</div>
                    </div>
                </div>
                
                <!-- الرسالة الثالثة -->
                <div class="message-card">
                    <h3 class="message-title">
                        <i class="fas fa-sun"></i> أمنيات العام الجديد
                        <span class="badge">Wishes</span>
                    </h3>
                    <div class="poem">
                        أتمنى أن يحملَ العامُ الجديد<br>
                        لكِ كلَّ السعادة والهناء<br>
                        وأن تروا الشمسَ دافئةً<br>
                        في كلِّ صباحٍ مع الأصدقاء<br><br>
                        
                        أتمنى أن تتحقَّقَ أحلامكِ<br>
                        كما تتحقَّقُ النجومُ في السماء<br>
                        وأن تبقى ابتسامتُكِ مشرقةً<br>
                        كشروقِ الفجرِ في الغباء<br><br>
                        
                        وأعدكِ بأنني سأبقى<br>
                        خلفَكِ في كلِّ الخطوات<br>
                        أدعمُكِ، أحبكِ، أحميكِ<br>
                        في جميعِ الحالات<br>
                    </div>
                    <div class="message-footer">
                        <div class="message-date">2024</div>
                        <div class="message-icon">🎉</div>
                    </div>
                </div>
                
                <!-- الرسالة الرابعة -->
                <div class="message-card">
                    <h3 class="message-title">
                        <i class="fas fa-gem"></i> وعد الأبد
                        <span class="badge">Promise</span>
                    </h3>
                    <div class="poem">
                        أعدكِ بأن الحبَّ سيبقى<br>
                        نقيًا كندى الصباح<br>
                        وسنكونُ معًا دائمًا<br>
                        في السراء والضراء<br><br>
                        
                        أعدكِ بأنني سأرسمُ<br>
                        البسمةَ على شفتيكِ كلَّ يوم<br>
                        وأحملُ همومَكِ عنكِ<br>
                        لأريحَ قلبَكِ الملئ بالهموم<br><br>
       
