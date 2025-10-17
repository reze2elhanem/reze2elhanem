<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>رزق الهانم - إعادة تدوير الملابس وتمكين المرأة</title>
    <img src="https://instagram.faly1-2.fna.fbcdn.net/v/t51.2885-19/527543323_18019665344718964_5192333461726657432_n.jpg?stp=dst-jpg_s150x150_tt6&efg=eyJ2ZW5jb2RlX3RhZyI6InByb2ZpbGVfcGljLmRqYW5nby4xMDgwLmMyIn0&_nc_ht=instagram.faly1-2.fna.fbcdn.net&_nc_cat=104&_nc_oc=Q6cZ2QHWS0s12drF0NbvKJAl-FcV1MkjXyZtpXPJQZY4wCrlFAcX-uJjlT-TqstqCA2W6to&_nc_ohc=toBxsLLV7lIQ7kNvwGCKbF_&_nc_gid=qNAx78IRRAuxgP6Dri9nAw&edm=AHzjunoBAAAA&ccb=7-5&oh=00_Afb2F0ooDh35BR5VK3Sy1zwo19wanA6cOwwHKuNende-Eg&oe=68CB7E9A&_nc_sid=ba8368" alt="">
    <!-- الخطوط -->
    <link href="https://fonts.googleapis.com/css2?family=Cairo:wght@300;400;600;700&display=swap" rel="stylesheet">
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600&display=swap" rel="stylesheet">
    
    <!-- أيقونات -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    
    <style>
        :root {
            --primary: #4e3c2e79;
            --secondary: #E0A96D;
            --light: #F9F5F0;
            --dark: #2C1E1A;
            --white: #FFFFFF;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Cairo', sans-serif;
            color: #333;
            background-color: var(--white);
            overflow-x: hidden;
        }
        
        body.english {
            font-family: 'Poppins', sans-serif;
            direction: ltr;
        }
        
        /* الشريط العلوي */
        .navbar {
            background-color: var(--white);
            box-shadow: 0 2px 15px rgba(0, 0, 0, 0.1);
            padding: 0.8rem 5%;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            height: 50px;
            display: flex;
            align-items: center;
        }
        
        .logo img {
            height: 100%;
        }
        
        .nav-links {
            display: flex;
            list-style: none;
        }
        
        .nav-links li {
            margin: 0 15px;
        }
        
        .nav-links a {
            text-decoration: none;
            color: var(--dark);
            font-weight: 600;
            font-size: 1rem;
            transition: all 0.3s ease;
            position: relative;
        }
        
        .nav-links a:after {
            content: '';
            position: absolute;
            bottom: -5px;
            right: 0;
            width: 0;
            height: 2px;
            background-color: var(--secondary);
            transition: width 0.3s ease;
        }
        
        .nav-links a:hover:after {
            width: 100%;
        }
        
        .nav-buttons {
            display: flex;
            align-items: center;
        }
        
        .language-toggle {
            background: none;
            border: 1px solid var(--primary);
            color: var(--primary);
            padding: 0.4rem 0.8rem;
            border-radius: 20px;
            cursor: pointer;
            font-family: inherit;
            font-weight: 600;
            margin-left: 15px;
            transition: all 0.3s ease;
        }
        
        .language-toggle:hover {
            background-color: var(--primary);
            color: var(--white);
        }
        
        .cta-button {
            background-color: var(--primary);
            color: var(--white);
            border: none;
            padding: 0.6rem 1.5rem;
            border-radius: 25px;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
            font-family: inherit;
        }
        
        .cta-button:hover {
            background-color: var(--secondary);
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(78, 52, 46, 0.2);
        }
        
        /* قسم البطل */
        .hero {
            height: 100vh;
            background: linear-gradient(rgba(78, 52, 46, 0.7), rgba(78, 52, 46, 0.7)), url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" width="100" height="100" viewBox="0 0 100 100"><rect width="100" height="100" fill="%234E342E"/><path d="M0 0L100 100" stroke="%23E0A96D" stroke-width="2"/><path d="M100 0L0 100" stroke="%23E0A96D" stroke-width="2"/></svg>');
            background-size: cover;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            color: var(--white);
            padding: 0 5%;
            position: relative;
            overflow: hidden;
        }
        
        .hero-content {
            max-width: 900px;
            z-index: 2;
            animation: fadeIn 1.5s ease-out;
        }
        
        .hero h1 {
            font-size: 3.5rem;
            margin-bottom: 1.5rem;
            line-height: 1.3;
        }
        
        .hero p {
            font-size: 1.5rem;
            margin-bottom: 2.5rem;
            line-height: 1.6;
        }
        
        .hero-buttons {
            display: flex;
            justify-content: center;
            gap: 20px;
        }
        
        .secondary-button {
            background-color: transparent;
            color: var(--white);
            border: 2px solid var(--white);
            padding: 0.8rem 2rem;
            border-radius: 25px;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
            font-family: inherit;
        }
        
        .secondary-button:hover {
            background-color: var(--white);
            color: var(--primary);
        }
        
        .countdown {
            margin-top: 3rem;
            background-color: rgba(255, 255, 255, 0.2);
            padding: 1rem;
            border-radius: 10px;
            display: inline-block;
        }
        
        .countdown h3 {
            margin-bottom: 0.5rem;
        }
        
        .countdown-timer {
            display: flex;
            justify-content: center;
            gap: 15px;
        }
        
        .countdown-unit {
            background-color: var(--primary);
            padding: 0.5rem;
            border-radius: 5px;
            min-width: 60px;
        }
        
        .countdown-number {
            font-size: 1.8rem;
            font-weight: 700;
        }
        
        .countdown-label {
            font-size: 0.8rem;
        }
        
        /* قسم من نحن */
        .about {
            padding: 6rem 5%;
            display: flex;
            align-items: center;
            justify-content: space-between;
            flex-wrap: wrap;
        }
        
        .about-content {
            flex: 1;
            min-width: 300px;
            padding: 20px;
        }
        
        .about-image {
            flex: 1;
            min-width: 300px;
            text-align: center;
        }
        
        .about-image img {
            max-width: 100%;
            border-radius: 10px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
        }
        
        .section-title {
            font-size: 2.5rem;
            color: var(--primary);
            margin-bottom: 1.5rem;
            position: relative;
            display: inline-block;
        }
        
        .section-title:after {
            content: '';
            position: absolute;
            bottom: -10px;
            right: 0;
            width: 50%;
            height: 3px;
            background-color: var(--secondary);
        }
        
        .about p {
            font-size: 1.1rem;
            line-height: 1.8;
            margin-bottom: 1.5rem;
            color: #555;
        }
        
        .features {
            display: flex;
            justify-content: space-between;
            margin-top: 2rem;
            flex-wrap: wrap;
        }
        
        .feature {
            text-align: center;
            flex: 1;
            min-width: 150px;
            margin: 10px;
            padding: 20px;
            border-radius: 10px;
            background-color: var(--light);
            transition: all 0.3s ease;
        }
        
        .feature:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
        }
        
        .feature i {
            font-size: 2.5rem;
            color: var(--primary);
            margin-bottom: 1rem;
        }
        
        .feature h3 {
            font-size: 1.2rem;
            margin-bottom: 0.5rem;
        }
        
        /* قسم التطوع */
        .volunteer {
            padding: 6rem 5%;
            background-color: var(--light);
            text-align: center;
        }
        
        .volunteer-cards {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 30px;
            margin-top: 3rem;
        }
        
        .card {
            background-color: var(--white);
            border-radius: 15px;
            padding: 2rem;
            width: 250px;
            box-shadow: 0 5px 20px rgba(0, 0, 0, 0.1);
            transition: all 0.3s ease;
        }
        
        .card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.15);
        }
        
        .card i {
            font-size: 3rem;
            color: var(--secondary);
            margin-bottom: 1.5rem;
        }
        
        .card h3 {
            font-size: 1.3rem;
            margin-bottom: 1rem;
            color: var(--primary);
        }
        
        .card p {
            color: #666;
            line-height: 1.6;
        }
        
        /* قسم وسائل التواصل */
        .social {
            padding: 6rem 5%;
            text-align: center;
        }
        
        .social-icons {
            display: flex;
            justify-content: center;
            gap: 30px;
            margin-top: 3rem;
            flex-wrap: wrap;
        }
        
        .social-icon {
            width: 70px;
            height: 70px;
            border-radius: 50%;
            background-color: var(--light);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.8rem;
            color: var(--primary);
            transition: all 0.3s ease;
            text-decoration: none;
        }
        
        .social-icon:hover {
            background-color: var(--primary);
            color: var(--white);
            transform: scale(1.1) rotate(5deg);
        }
        
        /* المعرض */
        .gallery {
            padding: 6rem 5%;
            background-color: var(--light);
        }
        
        .gallery-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            gap: 20px;
            margin-top: 3rem;
        }
        
        .gallery-item {
            height: 250px;
            border-radius: 10px;
            overflow: hidden;
            position: relative;
        }
        
        .gallery-item img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: all 0.5s ease;
        }
        
        .gallery-item:hover img {
            transform: scale(1.1);
        }
        
        .gallery-caption {
            position: absolute;
            bottom: 0;
            right: 0;
            left: 0;
            background: linear-gradient(transparent, rgba(78, 52, 46, 0.8));
            color: var(--white);
            padding: 20px;
            transform: translateY(100%);
            transition: all 0.3s ease;
        }
        
        .gallery-item:hover .gallery-caption {
            transform: translateY(0);
        }
        
        /* التذييل */
        .footer {
            background-color: var(--dark);
            color: var(--white);
            padding: 4rem 5% 2rem;
        }
        
        .footer-content {
            display: flex;
            justify-content: space-between;
            flex-wrap: wrap;
            gap: 40px;
        }
        
        .footer-logo {
            flex: 1;
            min-width: 250px;
        }
        
        .footer-logo img {
            height: 60px;
            margin-bottom: 1rem;
        }
        
        .footer-links {
            flex: 1;
            min-width: 200px;
        }
        
        .footer-links h3 {
            font-size: 1.3rem;
            margin-bottom: 1.5rem;
            position: relative;
            display: inline-block;
        }
        
        .footer-links h3:after {
            content: '';
            position: absolute;
            bottom: -10px;
            right: 0;
            width: 50%;
            height: 2px;
            background-color: var(--secondary);
        }
        
        .footer-links ul {
            list-style: none;
        }
        
        .footer-links li {
            margin-bottom: 0.8rem;
        }
        
        .footer-links a {
            color: #ccc;
            text-decoration: none;
            transition: all 0.3s ease;
        }
        
        .footer-links a:hover {
            color: var(--secondary);
            padding-right: 5px;
        }
        
        .footer-bottom {
            margin-top: 3rem;
            text-align: center;
            padding-top: 2rem;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        /* الحركات والتفاعلات */
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }
        
        @keyframes float {
            0% { transform: translateY(0px); }
            50% { transform: translateY(-10px); }
            100% { transform: translateY(0px); }
        }
        
        .animated {
            opacity: 0;
            transform: translateY(20px);
            transition: opacity 0.5s ease, transform 0.5s ease;
        }
        
        .in-view {
            opacity: 1;
            transform: translateY(0);
        }
        
        /* التجاوب مع الشاشات */
        @media (max-width: 768px) {
            .navbar {
                flex-direction: column;
                padding: 1rem;
            }
            
            .nav-links {
                margin-top: 1rem;
                flex-wrap: wrap;
                justify-content: center;
            }
            
            .nav-links li {
                margin: 5px 10px;
            }
            
            .hero h1 {
                font-size: 2.5rem;
            }
            
            .hero p {
                font-size: 1.2rem;
            }
            
            .hero-buttons {
                flex-direction: column;
                gap: 15px;
            }
            
            .about, .footer-content {
                flex-direction: column;
            }
            
            .section-title {
                font-size: 2rem;
            }
            
            .volunteer-cards {
                gap: 20px;
            }
            
            .card {
                width: 100%;
                max-width: 300px;
            }
        }
        
        /* نمط اللغة الإنجليزية */
        body.english .section-title:after {
            right: auto;
            left: 0;
        }
        
        body.english .footer-links h3:after {
            right: auto;
            left: 0;
        }
        
        body.english .footer-links a:hover {
            padding-right: 0;
            padding-left: 5px;
        }
    </style>
</head>
<body>
    <!-- الشريط العلوي -->
    <nav class="navbar">
        <div class="logo">
            <img src="data:image/svg+xml;utf8,<svg xmlns='http://www.w3.org/2000/svg' width='200' height='50' viewBox='0 0 200 50'><rect width='200' height='50' fill='%234E342E' rx='5'/><text x='100' y='30' font-family='Cairo' font-size='20' fill='%23E0A96D' text-anchor='middle'>رزق الهانم</text></svg>" alt="رزق الهانم">
        </div>
        
        <ul class="nav-links">
            <li><a href="#home">الرئيسية</a></li>
            <li><a href="#about">من نحن</a></li>
            <li><a href="#volunteer">التطوع</a></li>
            <li><a href="#gallery">المعرض</a></li>
            <li><a href="#contact">اتصل بنا</a></li>
        </ul>
        
        <div class="nav-buttons">
            <button class="language-toggle" id="languageToggle">EN</button>
            <button class="cta-button">تطوّع معانا</button>
        </div>
    </nav>

    <!-- قسم البطل -->
    <section class="hero" id="home">
        <div class="hero-content">
            <h1>رزق الهانم – بنحوّل الهدوم القديمة لفرص جديدة</h1>
            <p>معانا… القماش بيتجدّد، والستات حياتهم كمان بتتجدّد.</p>
            <div class="hero-buttons">
                <button class="cta-button">تطوّع معانا</button>
                <button class="secondary-button">اعرف أكتر</button>
            </div>
            <div class="countdown">
                <h3>موعد انتهاء التطوع:</h3>
                <div class="countdown-timer">
                    <div class="countdown-unit">
                        <div class="countdown-number" id="days">15</div>
                        <div class="countdown-label">أيام</div>
                    </div>
                    <div class="countdown-unit">
                        <div class="countdown-number" id="hours">10</div>
                        <div class="countdown-label">ساعات</div>
                    </div>
                    <div class="countdown-unit">
                        <div class="countdown-number" id="minutes">25</div>
                        <div class="countdown-label">دقائق</div>
                    </div>
                    <div class="countdown-unit">
                        <div class="countdown-number" id="seconds">30</div>
                        <div class="countdown-label">ثواني</div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- قسم من نحن -->
    <section class="about" id="about">
        <div class="about-content">
            <h2 class="section-title">من نحن</h2>
            <p>رزق الهانم هي مبادرة تهدف إلى إعادة تدوير الملابس المستعملة وتحويلها إلى منتجات جديدة ذات قيمة، مما يساهم في تمكين السيدات اقتصادياً وحماية البيئة من خلال تقليل النفايات.</p>
            <p>نحن نؤمن بأن التجديد لا يقتصر على الأقمشة والملابس فقط، بل يمتد ليشمل حياة النساء اللواتي نقوم بتدريبهن وتوظيفهن، مما يمنحهن فرصاً جديدة لتحسين أوضاعهن المعيشية.</p>
            
            <div class="features">
                <div class="feature animated">
                    <i class="fas fa-recycle"></i>
                    <h3>إعادة التدوير</h3>
                </div>
                <div class="feature animated">
                    <i class="fas fa-tshirt"></i>
                    <h3>تمكين المرأة</h3>
                </div>
                <div class="feature animated">
                    <i class="fas fa-globe-africa"></i>
                    <h3>حماية البيئة</h3>
                </div>
            </div>
        </div>
        
        <div class="about-image">
            <img src="data:image/svg+xml;utf8,<svg xmlns='http://www.w3.org/2000/svg' width='400' height='300' viewBox='0 0 400 300'><rect width='400' height='300' fill='%23F9F5F0' rx='10'/><circle cx='150' cy='120' r='70' fill='%23E0A96D'/><rect x='230' y='80' width='120' height='140' fill='%234E342E' rx='10'/></svg>" alt="About Reze2 Elhanem">
        </div>
    </section>

    <!-- قسم التطوع -->
    <section class="volunteer" id="volunteer">
        <h2 class="section-title">لماذا تنضم إلينا</h2>
        
        <div class="volunteer-cards">
            <div class="card animated">
                <i class="fas fa-lightbulb"></i>
                <h3>تعلم مهارات جديدة</h3>
                <p>اكتسب خبرة في إعادة التدوير والتصميم والخياطة</p>
            </div>
            
            <div class="card animated">
                <i class="fas fa-hands-helping"></i>
                <h3>كون جزء من تغيير حقيقي</h3>
                <p>ساهم في إحداث تأثير إيجابي في مجتمعك</p>
            </div>
            
            <div class="card animated">
                <i class="fas fa-leaf"></i>
                <h3>ساعد البيئة</h3>
                <p>قلل من النفايات ودعم الاستدامة البيئية</p>
            </div>
            
            <div class="card animated">
                <i class="fas fa-heart"></i>
                <h3>ادعم السيدات</h3>
                <p>ساعد في تمكين المرأة economically واجتماعياً</p>
            </div>
        </div>
        
        <button class="cta-button" style="margin-top: 40px;">سجّل دلوقتي</button>
    </section>

    <!-- قسم وسائل التواصل -->
    <section class="social" id="social">
        <h2 class="section-title">تابعنا وكن جزء من الرحلة</h2>
        
        <div class="social-icons">
            <a href="https://www.instagram.com/reze2_elhanem" class="social-icon animated">
                <i class="fab fa-instagram"></i>
            </a>
            <a href="https://www.facebook.com/share/1C9T6HNBc5/" class="social-icon animated">
                <i class="fab fa-facebook-f"></i>
            </a>
            <a href="https://www.linkedin.com/company/108305134/admin" class="social-icon animated">
                <i class="fab fa-linkedin-in"></i>
            </a>
            <a href="https://www.tiktok.com/@reze2.elhanem" class="social-icon animated">
                <i class="fab fa-tiktok"></i>
            </a>
        </div>
    </section>

    <!-- المعرض -->
    <section class="gallery" id="gallery">
        <h2 class="section-title">معرض أعمالنا</h2>
        
        <div class="gallery-grid">
            <div class="gallery-item animated">
                <img src="data:image/svg+xml;utf8,<svg xmlns='http://www.w3.org/2000/svg' width='300' height='300' viewBox='0 0 300 300'><rect width='300' height='300' fill='%23E0A96D'/><circle cx='150' cy='120' r='50' fill='%234E342E'/></svg>" alt="Project 1">
                <div class="gallery-caption">
                    <h3>إعادة تدوير الملابس</h3>
                </div>
            </div>
            
            <div class="gallery-item animated">
                <img src="data:image/svg+xml;utf8,<svg xmlns='http://www.w3.org/2000/svg' width='300' height='300' viewBox='0 0 300 300'><rect width='300' height='300' fill='%234E342E'/><polygon points='150,80 220,220 80,220' fill='%23E0A96D'/></svg>" alt="Project 2">
                <div class="gallery-caption">
                    <h3>ورش العمل</h3>
                </div>
            </div>
            
            <div class="gallery-item animated">
                <img src="data:image/svg+xml;utf8,<svg xmlns='http://www.w3.org/2000/svg' width='300' height='300' viewBox='0 0 300 300'><rect width='300' height='300' fill='%23F9F5F0'/><rect x='80' y='100' width='140' height='100' fill='%234E342E' rx='10'/></svg>" alt="Project 3">
                <div class="gallery-caption">
                    <h3>المنتجات النهائية</h3>
                </div>
            </div>
            
            <div class="gallery-item animated">
                <img src="data:image/svg+xml;utf8,<svg xmlns='http://www.w3.org/2000/svg' width='300' height='300' viewBox='0 0 300 300'><rect width='300' height='300' fill='%23E0A96D'/><rect x='100' y='70' width='100' height='160' fill='%234E342E' rx='5'/></svg>" alt="Project 4">
                <div class="gallery-caption">
                    <h3>فريق العمل</h3>
                </div>
            </div>
            
            <div class="gallery-item animated">
                <img src="data:image/svg+xml;utf8,<svg xmlns='http://www.w3.org/2000/svg' width='300' height='300' viewBox='0 0 300 300'><rect width='300' height='300' fill='%234E342E'/><circle cx='150' cy='150' r='60' fill='%23E0A96D'/></svg>" alt="Project 5">
                <div class="gallery-caption">
                    <h3>التدريب</h3>
                </div>
            </div>
            
            <div class="gallery-item animated">
                <img src="data:image/svg+xml;utf8,<svg xmlns='http://www.w3.org/2000/svg' width='300' height='300' viewBox='0 0 300 300'><rect width='300' height='300' fill='%23F9F5F0'/><polygon points='100,100 200,100 150,200' fill='%234E342E'/></svg>" alt="Project 6">
                <div class="gallery-caption">
                    <h3>التمكين</h3>
                </div>
            </div>
        </div>
    </section>

    <!-- التذييل -->
    <footer class="footer" id="contact">
        <div class="footer-content">
            <div class="footer-logo">
                <img src="data:image/svg+xml;utf8,<svg xmlns='http://www.w3.org/2000/svg' width='200' height='50' viewBox='0 0 200 50'><rect width='200' height='50' fill='%23E0A96D' rx='5'/><text x='100' y='30' font-family='Cairo' font-size='20' fill='%234E342E' text-anchor='middle'>رزق الهانم</text></svg>" alt="رزق الهانم">
                <p>نسعى لتحقيق تنمية مستدامة من خلال إعادة تدوير الملابس وتمكين المرأة.</p>
            </div>
            
            <div class="footer-links">
                <h3>روابط سريعة</h3>
                <ul>
                    <li><a href="#home">الرئيسية</a></li>
                    <li><a href="#about">من نحن</a></li>
                    <li><a href="#volunteer">التطوع</a></li>
                    <li><a href="#gallery">المعرض</a></li>
                    <li><a href="#social">وسائل التواصل</a></li>
                </ul>
            </div>
            
            <div class="footer-links">
                <h3>اتصل بنا</h3>
                <ul>
                    <li><i class="fas fa-envelope"></i> info@reze2elhanem.com</li>
                    <li><i class="fas fa-phone"></i> +20 123 456 7890</li>
                    <li><i class="fas fa-map-marker-alt"></i> القاهرة، مصر</li>
                </ul>
            </div>
        </div>
        
        <div class="footer-bottom">
            <p>&copy; 2023 رزق الهانم. جميع الحقوق محفوظة.</p>
            <button class="language-toggle" id="footerLanguageToggle">EN</button>
        </div>
    </footer>

    <script>
        // تبديل اللغة
        document.getElementById('languageToggle').addEventListener('click', function() {
            document.body.classList.toggle('english');
            if (document.body.classList.contains('english')) {
                this.textContent = 'AR';
                // هنا يمكن إضافة الترجمة الفعلية للمحتوى
            } else {
                this.textContent = 'EN';
            }
        });
        
        document.getElementById('footerLanguageToggle').addEventListener('click', function() {
            document.body.classList.toggle('english');
            if (document.body.classList.contains('english')) {
                this.textContent = 'AR';
            } else {
                this.textContent = 'EN';
            }
        });
        
        // العد التنازلي
        function updateCountdown() {
            const targetDate = new Date();
            targetDate.setDate(targetDate.getDate() + 15);
            
            const now = new Date();
            const difference = targetDate - now;
            
            const days = Math.floor(difference / (1000 * 60 * 60 * 24));
            const hours = Math.floor((difference % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
            const minutes = Math.floor((difference % (1000 * 60 * 60)) / (1000 * 60));
            const seconds = Math.floor((difference % (1000 * 60)) / 1000);
            
            document.getElementById('days').textContent = days;
            document.getElementById('hours').textContent = hours;
            document.getElementById('minutes').textContent = minutes;
            document.getElementById('seconds').textContent = seconds;
        }
        
        setInterval(updateCountdown, 1000);
        updateCountdown();
        
        // حركات التمرير
        function checkScroll() {
            const elements = document.querySelectorAll('.animated');
            
            elements.forEach(element => {
                const position = element.getBoundingClientRect();
                
                if (position.top < window.innerHeight - 100) {
                    element.classList.add('in-view');
                }
            });
        }
        
        window.addEventListener('scroll', checkScroll);
        window.addEventListener('load', checkScroll);
        
        // تأثيرات التمرير السلس
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                e.preventDefault();
                
                const targetId = this.getAttribute('href');
                if (targetId === '#') return;
                
                const targetElement = document.querySelector(targetId);
                if (targetElement) {
                    window.scrollTo({
                        top: targetElement.offsetTop - 80,
                        behavior: 'smooth'
                    });
                }
            });
        });
    </script>
</body>
</html>
