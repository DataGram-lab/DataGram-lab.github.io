<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>DataGram - LeadsMiner | الطريقة الأذكى لجلب العملاء</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Tajawal:wght@300;400;500;700;800;900&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/aos/2.3.4/aos.css">
    <style>
        :root {
            --primary: #4361ee;
            --primary-light: #4895ef;
            --secondary: #3a86ff;
            --accent: #7209b7;
            --accent-light: #9d4edd;
            --light: #ffffff;
            --light-gray: #f8f9fa;
            --medium-gray: #e9ecef;
            --text-dark: #2d3748;
            --text-medium: #4a5568;
            --gradient: linear-gradient(135deg, var(--primary), var(--accent-light));
            --gradient-light: linear-gradient(135deg, var(--primary-light), var(--accent-light));
            --shadow: 0 10px 30px rgba(0, 0, 0, 0.08);
            --shadow-hover: 0 15px 35px rgba(0, 0, 0, 0.12);
            --transition: all 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Tajawal', sans-serif;
        }

        body {
            background-color: var(--light);
            color: var(--text-medium);
            line-height: 1.6;
            overflow-x: hidden;
        }

        .container {
            width: 100%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        section {
            padding: 100px 0;
        }

        h1, h2, h3 {
            margin-bottom: 25px;
            font-weight: 800;
            line-height: 1.3;
            color: var(--text-dark);
        }

        h1 {
            font-size: 3.2rem;
            background: var(--gradient);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        h2 {
            font-size: 2.5rem;
            text-align: center;
            margin-bottom: 60px;
            position: relative;
        }

        h2:after {
            content: '';
            position: absolute;
            bottom: -20px;
            right: 50%;
            transform: translateX(50%);
            width: 100px;
            height: 4px;
            background: var(--gradient);
            border-radius: 2px;
        }

        p {
            margin-bottom: 25px;
            font-size: 1.15rem;
            color: var(--text-medium);
        }

        .btn {
            display: inline-block;
            padding: 18px 35px;
            border-radius: 50px;
            text-decoration: none;
            font-weight: 700;
            font-size: 1.1rem;
            transition: var(--transition);
            cursor: pointer;
            box-shadow: var(--shadow);
            text-align: center;
            border: none;
            position: relative;
            overflow: hidden;
            z-index: 1;
        }

        .btn:before {
            content: '';
            position: absolute;
            top: 0;
            right: 0;
            width: 0%;
            height: 100%;
            background: var(--gradient-light);
            transition: var(--transition);
            z-index: -1;
            border-radius: 50px;
        }

        .btn-primary {
            background: var(--gradient);
            color: white;
        }

        .btn-primary:hover:before {
            width: 100%;
            right: auto;
            left: 0;
        }

        .btn-secondary {
            background: white;
            color: var(--primary);
            border: 2px solid var(--primary);
        }

        .btn-secondary:hover {
            background: var(--primary);
            color: white;
            transform: translateY(-5px);
            box-shadow: var(--shadow-hover);
        }

        .btn-group {
            display: flex;
            gap: 20px;
            margin-top: 40px;
            flex-wrap: wrap;
            justify-content: center;
        }

        .logo-container {
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 25px;
            margin-bottom: 40px;
            flex-wrap: wrap;
        }

        .logo {
            height: 70px;
            width: auto;
            filter: drop-shadow(0 5px 15px rgba(0, 0, 0, 0.1));
        }

        /* Hero Section */
        .hero {
            min-height: 100vh;
            display: flex;
            align-items: center;
            position: relative;
            overflow: hidden;
            padding-top: 80px;
            background: var(--light-gray);
        }

        .hero:before {
            content: '';
            position: absolute;
            top: 0;
            right: 0;
            bottom: 0;
            left: 0;
            background: 
                radial-gradient(circle at 90% 10%, rgba(67, 97, 238, 0.1) 0%, transparent 30%),
                radial-gradient(circle at 10% 80%, rgba(157, 78, 221, 0.1) 0%, transparent 30%);
            z-index: 0;
        }

        .hero-content {
            text-align: center;
            position: relative;
            z-index: 1;
            padding: 40px 0;
        }

        .hero h1 {
            font-size: 3.5rem;
            margin-bottom: 25px;
            animation: fadeInUp 1s ease;
        }

        .hero p {
            font-size: 1.4rem;
            max-width: 800px;
            margin: 0 auto 40px;
            animation: fadeInUp 1s ease 0.2s;
            animation-fill-mode: both;
        }

        .floating-particles {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: 0;
            overflow: hidden;
        }

        .particle {
            position: absolute;
            background: var(--gradient);
            border-radius: 50%;
            opacity: 0.2;
            animation: float 15s infinite linear;
        }

        /* What is LeadsMiner Section */
        .about {
            background: white;
            border-radius: 20px;
            margin: 40px;
            position: relative;
            overflow: hidden;
            box-shadow: var(--shadow);
        }

        .about:before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle, rgba(67, 97, 238, 0.05) 0%, transparent 70%);
            z-index: 0;
            transform: rotate(30deg);
        }

        .about-content {
            display: flex;
            align-items: center;
            gap: 60px;
            flex-wrap: wrap;
        }

        .about-text {
            flex: 1;
            min-width: 300px;
        }

        .about-image {
            flex: 1;
            min-width: 300px;
            text-align: center;
            position: relative;
        }

        .about-image img {
            max-width: 100%;
            border-radius: 20px;
            box-shadow: var(--shadow);
            transform: perspective(1000px) rotateY(-10deg);
            transition: var(--transition);
        }

        .about-image img:hover {
            transform: perspective(1000px) rotateY(0deg);
        }

        /* How it Works Section */
        .how-it-works {
            position: relative;
            background: var(--light-gray);
        }

        .video-container {
            position: relative;
            padding-bottom: 56.25%;
            height: 0;
            overflow: hidden;
            border-radius: 20px;
            box-shadow: var(--shadow);
            max-width: 900px;
            margin: 0 auto 50px;
            background: white;
            transform: perspective(1000px) rotateX(5deg);
            transition: var(--transition);
        }

        .video-container:hover {
            transform: perspective(1000px) rotateX(0deg);
            box-shadow: var(--shadow-hover);
        }

        .video-container video {
            position: absolute;
            top: 0;
            right: 0;
            width: 100%;
            height: 100%;
            object-fit: cover;
            border-radius: 20px;
        }

        .video-text {
            text-align: center;
            max-width: 800px;
            margin: 0 auto;
        }

        /* Features Section */
        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(330px, 1fr));
            gap: 40px;
            margin-bottom: 60px;
        }

        .feature-card {
            background: white;
            padding: 40px 30px;
            border-radius: 20px;
            box-shadow: var(--shadow);
            transition: var(--transition);
            text-align: center;
            border: 1px solid var(--medium-gray);
            position: relative;
            overflow: hidden;
            z-index: 1;
        }

        .feature-card:before {
            content: '';
            position: absolute;
            top: 0;
            right: 0;
            width: 100%;
            height: 0%;
            background: var(--gradient);
            opacity: 0.05;
            transition: var(--transition);
            z-index: -1;
            border-radius: 20px;
        }

        .feature-card:hover {
            transform: translateY(-15px);
            box-shadow: var(--shadow-hover);
            border-color: rgba(113, 73, 217, 0.2);
        }

        .feature-card:hover:before {
            height: 100%;
        }

        .feature-icon {
            font-size: 3.5rem;
            margin-bottom: 25px;
            background: var(--gradient);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            display: inline-block;
            transition: var(--transition);
        }

        .feature-card:hover .feature-icon {
            transform: scale(1.2) rotate(5deg);
        }

        .feature-card h3 {
            font-size: 1.6rem;
            margin-bottom: 20px;
        }

        /* Contact Section */
        .contact {
            background: var(--gradient);
            color: white;
            text-align: center;
            border-radius: 20px;
            margin: 40px;
            position: relative;
            overflow: hidden;
        }

        .contact:before {
            content: '';
            position: absolute;
            top: 0;
            right: 0;
            bottom: 0;
            left: 0;
            background: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 1440 320'%3E%3Cpath fill='%23ffffff' fill-opacity='0.1' d='M0,128L48,117.3C96,107,192,85,288,112C384,139,480,213,576,218.7C672,224,768,160,864,138.7C960,117,1056,139,1152,149.3C1248,160,1344,160,1392,160L1440,160L1440,320L1392,320C1344,320,1248,320,1152,320C1056,320,960,320,864,320C768,320,672,320,576,320C480,320,384,320,288,320C192,320,96,320,48,320L0,320Z'%3E%3C/path%3E%3C/svg%3E");
            background-size: cover;
            background-position: center bottom;
            z-index: 0;
        }

        .contact h2 {
            color: white;
        }

        .contact h2:after {
            background: white;
        }

        .contact p {
            color: rgba(255, 255, 255, 0.9);
        }

        .footer {
            padding: 50px 0 30px;
            text-align: center;
            background: var(--light-gray);
            color: var(--text-medium);
            position: relative;
        }

        .footer:before {
            content: '';
            position: absolute;
            top: 0;
            right: 0;
            width: 100%;
            height: 1px;
            background: var(--gradient);
        }

        .footer-logo {
            height: 50px;
            margin-bottom: 25px;
            opacity: 0.9;
        }

        .social-icons {
            display: flex;
            justify-content: center;
            gap: 25px;
            margin: 30px 0;
        }

        .social-icons a {
            color: var(--primary);
            font-size: 1.8rem;
            transition: var(--transition);
            width: 60px;
            height: 60px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            background: white;
            box-shadow: var(--shadow);
        }

        .social-icons a:hover {
            color: white;
            transform: translateY(-5px);
            background: var(--gradient);
            box-shadow: var(--shadow-hover);
        }

        /* Animations */
        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        @keyframes float {
            0% {
                transform: translateY(0) rotate(0deg);
            }
            50% {
                transform: translateY(-20px) rotate(10deg);
            }
            100% {
                transform: translateY(0) rotate(0deg);
            }
        }

        .fade-in {
            opacity: 0;
            transform: translateY(30px);
            transition: opacity 0.8s ease, transform 0.8s ease;
        }

        .fade-in.visible {
            opacity: 1;
            transform: translateY(0);
        }

        /* Navigation */
        .navbar {
            position: fixed;
            top: 0;
            right: 0;
            width: 100%;
            padding: 20px 0;
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(10px);
            z-index: 1000;
            transition: var(--transition);
            box-shadow: 0 5px 20px rgba(0, 0, 0, 0.05);
        }

        .navbar.scrolled {
            padding: 15px 0;
            box-shadow: 0 5px 20px rgba(0, 0, 0, 0.1);
        }

        .nav-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .nav-logo {
            height: 40px;
        }

        .nav-links {
            display: flex;
            gap: 30px;
        }

        .nav-links a {
            color: var(--text-dark);
            text-decoration: none;
            font-weight: 500;
            transition: var(--transition);
            position: relative;
        }

        .nav-links a:after {
            content: '';
            position: absolute;
            bottom: -5px;
            right: 0;
            width: 0;
            height: 2px;
            background: var(--gradient);
            transition: var(--transition);
        }

        .nav-links a:hover {
            color: var(--primary);
        }

        .nav-links a:hover:after {
            width: 100%;
        }

        /* Mobile Nav Toggle */
        .nav-toggle {
            display: none;
            background: none;
            border: none;
            color: var(--text-dark);
            font-size: 1.5rem;
            cursor: pointer;
        }

        /* Responsive Design */
        @media (max-width: 992px) {
            h1 {
                font-size: 2.8rem;
            }
            
            h2 {
                font-size: 2.2rem;
            }
            
            .about-content {
                flex-direction: column-reverse;
            }
            
            .about, .contact {
                margin: 20px;
            }
            
            .nav-links {
                display: none;
                position: absolute;
                top: 100%;
                right: 0;
                width: 100%;
                background: white;
                flex-direction: column;
                padding: 20px;
                box-shadow: var(--shadow);
            }
            
            .nav-links.active {
                display: flex;
            }
            
            .nav-toggle {
                display: block;
            }
        }

        @media (max-width: 768px) {
            h1 {
                font-size: 2.3rem;
            }
            
            h2 {
                font-size: 1.9rem;
            }
            
            .btn-group {
                flex-direction: column;
                align-items: center;
            }
            
            .btn {
                width: 100%;
                max-width: 300px;
            }
            
            .hero h1 {
                font-size: 2.8rem;
            }
            
            .hero p {
                font-size: 1.2rem;
            }
            
            section {
                padding: 80px 0;
            }
            
            .features-grid {
                grid-template-columns: 1fr;
            }
            
            .navbar {
                padding: 15px 0;
            }
        }
    </style>
</head>
<body>
    <!-- Navigation -->
    <nav class="navbar">
        <div class="container nav-container">
            <img src="https://raw.githubusercontent.com/DataGram-lab/DataGram-lab.github.io/main/DataGram-title.png" alt="DataGram Logo" class="nav-logo">
            <div class="nav-links">
                <a href="#home">الرئيسية</a>
                <a href="#about">عن البرنامج</a>
                <a href="#how-it-works">كيف يعمل</a>
                <a href="#features">الميزات</a>
                <a href="#contact">اتصل بنا</a>
            </div>
            <button class="nav-toggle">
                <i class="fas fa-bars"></i>
            </button>
        </div>
    </nav>

    <!-- Hero Section -->
    <section class="hero" id="home">
        <div class="floating-particles" id="particles"></div>
        <div class="container">
            <div class="hero-content">
                <h1 data-aos="fade-up">الطريقة الأذكى لجلب عملاء مهتمين بدون تكاليف إعلانات</h1>
                <p data-aos="fade-up" data-aos-delay="200">اكتشف قوة البيانات واستهدف عملاء محتملين بذكاء مع LeadsMiner - الحل المتكامل لتنمية أعمالك وتحقيق أرباح غير مسبوقة</p>
                <div class="btn-group" data-aos="fade-up" data-aos-delay="400">
                    <a href="https://github.com/DataGram-lab/LeadsMiner/releases/download/LeadsMiner/LeadsMinerInstaller.exe" class="btn btn-primary">تحميل البرنامج</a>
                    <a href="https://wa.me/201027930040" class="btn btn-secondary">تواصل معنا</a>
                </div>
            </div>
        </div>
    </section>

    <!-- What is LeadsMiner Section -->
    <section class="about" id="about" data-aos="fade-up">
        <div class="container">
            <h2>ما هو LeadsMiner ؟</h2>
            <div class="about-content">
                <div class="about-text">
                    <p data-aos="fade-left">LeadsMiner أداة قوية على نظام الويندوز تمكنك من استخراج وتحليل البيانات من مختلف المصاعد على الإنترنت. تم تصميم البرنامج خصيصًا لمساعدتك في العثور على عملاء محتملين مهتمين بخدماتك أو منتجاتك دون الحاجة إلى إنفاق الأموال على الحملات الإعلانية التقليدية.</p>
                    <p data-aos="fade-left" data-aos-delay="200">باستخدام تقنيات الذكاء الاصطناعي المتقدمة، يقوم LeadsMiner بجمع وتصنيف البيانات ذات الصلة بأعمالك، مما يمكنك من الوصول إلى قاعدة عملاء مستهدفين بدقة عالية وبأقل التكاليف.</p>
                    <div class="btn-group" data-aos="fade-left" data-aos-delay="400">
                        <a href="https://github.com/DataGram-lab/LeadsMiner/releases/download/LeadsMiner/LeadsMinerInstaller.exe" class="btn btn-primary">تحميل البرنامج</a>
                        <a href="https://wa.me/201027930040" class="btn btn-secondary">تواصل معنا</a>
                    </div>
                </div>
                <div class="about-image" data-aos="fade-left" data-aos-delay="300">
                    <img src="https://raw.githubusercontent.com/DataGram-lab/DataGram-lab.github.io/main/leadsminer%20logo.png" alt="LeadsMiner Illustration">
                </div>
            </div>
        </div>
    </section>

    <!-- How it Works Section -->
    <section class="how-it-works" id="how-it-works">
        <div class="container">
            <h2 data-aos="fade-up">طريقة استخدام برنامج LeadsMiner?</h2>
            <div class="video-container" data-aos="zoom-in" data-aos-delay="300">
                <video controls poster="https://raw.githubusercontent.com/DataGram-lab/DataGram-lab.github.io/main/leadsminer%20logo.png" preload="metadata">
                    <source src="howitworks.mp4" type="video/mp4">
                    متصفحك لا يدعم تشغيل الفيديو
                </video>
            </div>
            <div class="video-text">
                <p data-aos="fade-up">شاهد كيف يمكن لـ LeadsMiner أن يغير طريقة عملك إلى الأبد. في هذا الفيديو التوضيحي، سنريك كيف يمكنك بسهولة استخراج البيانات، تحليلها، والوصول إلى عملاء محتملين مهتمين بخدماتك في دقائق معدودة.</p>
                <div class="btn-group" data-aos="fade-up" data-aos-delay="200">
                    <a href="https://github.com/DataGram-lab/LeadsMiner/releases/download/LeadsMiner/LeadsMinerInstaller.exe" class="btn btn-primary">تحميل البرنامج</a>
                    <a href="https://wa.me/201027930040" class="btn btn-secondary">تواصل معنا</a>
                </div>
            </div>
        </div>
    </section>

    <!-- Features Section -->
    <section class="features" id="features">
        <div class="container">
            <h2 data-aos="fade-up">ميزات LeadsMiner</h2>
            <div class="features-grid">
                <div class="feature-card" data-aos="fade-up" data-aos-delay="100">
                    <div class="feature-icon">
                        <i class="fas fa-users"></i>
                    </div>
                    <h3>عملاء غير محدودين</h3>
                    <p>احصل على عدد غير محدود من العملاء المحتملين دون قيود، وزد من فرص نمو أعمالك بشكل متواصل</p>
                </div>
                <div class="feature-card" data-aos="fade-up" data-aos-delay="200">
                    <div class="feature-icon">
                        <i class="fas fa-globe"></i>
                    </div>
                    <h3>استهداف عالمي</h3>
                    <p>استهدف العملاء من أي مكان في العالم، ووسع نطاق عملك beyond الحدود الجغرافية التقليدية</p>
                </div>
                <div class="feature-card" data-aos="fade-up" data-aos-delay="300">
                    <div class="feature-icon">
                        <i class="fas fa-brain"></i>
                    </div>
                    <h3>استهداف ذكي</h3>
                    <p>استخدم خوارزميات الذكاء الاصطناعي المتقدمة لاستهداف العملاء المناسبين في الوقت المناسب</p>
                </div>
                <div class="feature-card" data-aos="fade-up" data-aos-delay="100">
                    <div class="feature-icon">
                        <i class="fas fa-shield-alt"></i>
                    </div>
                    <h3>خصوصية وأمان</h3>
                    <p>بياناتك محمية بأعلى معايير الأمان، ونضمن خصوصية تامة لجميع عمليات الاستخراج والتحليل</p>
                </div>
                <div class="feature-card" data-aos="fade-up" data-aos-delay="200">
                    <div class="feature-icon">
                        <i class="fas fa-money-bill-wave"></i>
                    </div>
                    <h3>توفير المال</h3>
                    <p>وفر آلاف الدولارات التي تنفقها على الإعلانات التقليدية مع نتائج أفضل وتكاليف أقل</p>
                </div>
                <div class="feature-card" data-aos="fade-up" data-aos-delay="300">
                    <div class="feature-icon">
                        <i class="fas fa-headset"></i>
                    </div>
                    <h3>دعم فني 24/7</h3>
                    <p>فريق دعم فني متاح على مدار الساعة لمساعدتك في أي استفسار أو مشكلة تواجهك</p>
                </div>
            </div>
            <div class="btn-group" data-aos="fade-up">
                <a href="https://github.com/DataGram-lab/LeadsMiner/releases/download/LeadsMiner/LeadsMinerInstaller.exe" class="btn btn-primary">تحميل البرنامج</a>
                <a href="https://wa.me/201027930040" class="btn btn-secondary">تواصل معنا</a>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section class="contact" id="contact" data-aos="fade-up">
        <div class="container">
            <h2>تواصل معنا الآن</h2>
            <p>هل لديك استفسار أو تحتاج إلى مساعدة؟ فريقنا متاح دائماً لمساعدتك في رحلتك نحو النجاح</p>
            <div class="btn-group">
                <a href="https://wa.me/201027930040" class="btn btn-secondary">التواصل عبر واتساب</a>
                <a href="https://github.com/DataGram-lab/LeadsMiner/releases/download/LeadsMiner/LeadsMinerInstaller.exe" class="btn btn-primary">تحميل البرنامج</a>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="footer">
        <div class="container">
            <img src="https://raw.githubusercontent.com/DataGram-lab/DataGram-lab.github.io/main/DataGram-title.png" alt="DataGram Logo" class="footer-logo">
            <p>© 2023 DataGram - LeadsMiner. جميع الحقوق محفوظة</p>
        </div>
    </footer>

    <script src="https://cdnjs.cloudflare.com/ajax/libs/aos/2.3.4/aos.js"></script>
    <script>
        // Initialize AOS
        AOS.init({
            duration: 1000,
            once: true,
            easing: 'ease-out-back'
        });

        // Create floating particles
        function createParticles() {
            const container = document.getElementById('particles');
            const particleCount = 30;
            
            for (let i = 0; i < particleCount; i++) {
                const particle = document.createElement('div');
                particle.classList.add('particle');
                
                // Random properties
                const size = Math.random() * 20 + 5;
                const posX = Math.random() * 100;
                const posY = Math.random() * 100;
                const delay = Math.random() * 15;
                
                particle.style.width = `${size}px`;
                particle.style.height = `${size}px`;
                particle.style.top = `${posY}%`;
                particle.style.left = `${posX}%`;
                particle.style.animationDelay = `${delay}s`;
                
                // Random gradient
                const gradients = [
                    'linear-gradient(135deg, #4361ee, #7209b7)',
                    'linear-gradient(135deg, #3a56d4, #9d4edd)',
                    'linear-gradient(135deg, #00b4d8, #4361ee)'
                ];
                particle.style.background = gradients[Math.floor(Math.random() * gradients.length)];
                
                container.appendChild(particle);
            }
        }
        
        // Navbar scroll effect
        window.addEventListener('scroll', function() {
            const navbar = document.querySelector('.navbar');
            if (window.scrollY > 50) {
                navbar.classList.add('scrolled');
            } else {
                navbar.classList.remove('scrolled');
            }
        });
        
        // Mobile nav toggle
        const navToggle = document.querySelector('.nav-toggle');
        const navLinks = document.querySelector('.nav-links');
        
        if (navToggle) {
            navToggle.addEventListener('click', function() {
                navLinks.classList.toggle('active');
            });
        }
        
        // Smooth scrolling for navigation links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                
                const targetId = this.getAttribute('href');
                if (targetId === '#') return;
                
                const targetElement = document.querySelector(targetId);
                if (targetElement) {
                    window.scrollTo({
                        top: targetElement.offsetTop - 80,
                        behavior: 'smooth'
                    });
                    
                    // Close mobile menu if open
                    if (navLinks.classList.contains('active')) {
                        navLinks.classList.remove('active');
                    }
                }
            });
        });
        
        // Initialize everything when DOM is loaded
        document.addEventListener('DOMContentLoaded', function() {
            createParticles();
            
            // Video lazy loading
            const video = document.querySelector('video');
            if (video) {
                video.setAttribute('preload', 'metadata');
            }
        });
    </script>
</body>
</html>
