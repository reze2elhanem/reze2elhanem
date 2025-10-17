<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>رزق الهانم — تحويل الملابس المتبرع بها إلى سبل عيش مستدامة</title>
    <meta name="description" content="رزق الهانم - ندرب النساء في ريف مصر على إعادة تدوير المنسوجات وكسب دخل ثابت. تبرع، تطوع، أو كن شريكًا.">
    
    <!-- الخطوط -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Cairo:wght@400;600;700&display=swap" rel="stylesheet">
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700&display=swap" rel="stylesheet">
    
    <!-- الأيقونات -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    
    <style>
        /* Reset كامل */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            -webkit-tap-highlight-color: transparent;
            -webkit-text-size-adjust: 100%;
            -moz-text-size-adjust: 100%;
            -ms-text-size-adjust: 100%;
        }

        :root {
            --bg-1: #F7EFE6;
            --bg-2: #FFF9F4;
            --primary-brown: #8B5E3C;
            --accent-green: #3E7B4E;
            --accent-sand: #E7CBAF;
            --text-dark: #2E2E2E;
            --muted: #6B6B6B;
            --white: #FFFFFF;
            --success: #2EAC6A;
            --shadow: rgba(46,46,46,0.08);
        }

        html {
            scroll-behavior: smooth;
            font-size: 16px;
        }

        body {
            font-family: 'Cairo', 'Segoe UI', Tahoma, sans-serif;
            background-color: var(--bg-1);
            color: var(--text-dark);
            line-height: 1.6;
            direction: rtl;
            overflow-x: hidden;
            -webkit-font-smoothing: antialiased;
            -moz-osx-font-smoothing: grayscale;
            -webkit-overflow-scrolling: touch;
        }

        body[dir="ltr"] {
            font-family: 'Inter', sans-serif;
            direction: ltr;
        }

        /* الحاوية */
        .container {
            width: 100%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 1rem;
        }

        @media (min-width: 768px) {
            .container {
                padding: 0 2rem;
            }
        }

        /* الهيدر */
        header {
            background-color: var(--white);
            box-shadow: 0 2px 20px var(--shadow);
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            height: 70px;
        }

        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
            height: 70px;
            padding: 0 1rem;
        }

        .logo {
            display: flex;
            align-items: center;
            gap: 0.75rem;
        }

        .logo-svg {
            width: 40px;
            height: 40px;
        }

        .logo-path {
            stroke: var(--primary-brown);
            stroke-width: 2;
            stroke-dasharray: 1000;
            stroke-dashoffset: 1000;
            animation: draw 900ms cubic-bezier(.2,.9,.3,1) forwards;
        }

        @keyframes draw {
            to { stroke-dashoffset: 0; }
        }

        .logo-text {
            font-size: 1.25rem;
            font-weight: 700;
            color: var(--primary-brown);
        }

        /* القائمة */
        .desktop-nav {
            display: none;
        }

        .mobile-menu {
            display: block;
        }

        .hamburger {
            background: none;
            border: none;
            font-size: 1.5rem;
            cursor: pointer;
            padding: 0.5rem;
            color: var(--text-dark);
            width: 44px;
            height: 44px;
            display: flex;
            align-items: center;
            justify-content: center;
        }

        .mobile-nav {
            position: fixed;
            top: 0;
            right: -100%;
            width: 85%;
            height: 100vh;
            background: var(--white);
            transition: right 0.3s ease;
            z-index: 1001;
            padding: 2rem;
            box-shadow: -5px 0 15px var(--shadow);
            overflow-y: auto;
        }

        .mobile-nav.active {
            right: 0;
        }

        .close-menu {
            background: none;
            border: none;
            font-size: 1.5rem;
            position: absolute;
            left: 1rem;
            top: 1rem;
            cursor: pointer;
            width: 44px;
            height: 44px;
            display: flex;
            align-items: center;
            justify-content: center;
        }

        .mobile-nav ul {
            list-style: none;
            margin-top: 3rem;
        }

        .mobile-nav li {
            margin-bottom: 1.5rem;
        }

        .mobile-nav a {
            text-decoration: none;
            color: var(--text-dark);
            font-size: 1.1rem;
            font-weight: 600;
            display: block;
            padding: 0.75rem 0;
            transition: color 0.3s ease;
        }

        .mobile-nav a:hover {
            color: var(--primary-brown);
        }

        .header-actions {
            display: flex;
            align-items: center;
            gap: 1rem;
        }

        .language-toggle {
            background: none;
            border: 1px solid var(--accent-sand);
            padding: 0.5rem 1rem;
            border-radius: 4px;
            cursor: pointer;
            display: flex;
            align-items: center;
            gap: 0.5rem;
            transition: all 0.3s ease;
            font-size: 0.9rem;
        }

        .language-toggle:hover {
            background-color: var(--accent-sand);
        }

        @media (min-width: 768px) {
            .desktop-nav {
                display: flex;
                gap: 2rem;
            }

            .mobile-menu {
                display: none;
            }

            .desktop-nav a {
                text-decoration: none;
                color: var(--text-dark);
                font-weight: 600;
                transition: color 0.3s ease;
                position: relative;
            }

            .desktop-nav a:hover {
                color: var(--primary-brown);
            }

            .desktop-nav a::after {
                content: '';
                position: absolute;
                bottom: -5px;
                right: 0;
                width: 0;
                height: 2px;
                background-color: var(--primary-brown);
                transition: width 0.3s ease;
            }

            .desktop-nav a:hover::after {
                width: 100%;
            }
        }

        /* الهيرو */
        .hero {
            background: linear-gradient(135deg, var(--bg-1) 0%, var(--bg-2) 100%);
            padding: 6rem 1rem 3rem;
            position: relative;
            overflow: hidden;
            min-height: 100vh;
            display: flex;
            align-items: center;
            margin-top: 70px;
        }

        .hero-background {
            position: absolute;
            top: 0;
            right: 0;
            width: 100%;
            height: 100%;
            opacity: 0.1;
            background-image: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100"><path d="M30,30 Q50,10 70,30 T90,30" stroke="%238B5E3C" fill="none" stroke-width="2"/></svg>');
            animation: moveThread 30s linear infinite;
        }

        @keyframes moveThread {
            0% { transform: translateX(0) translateY(0); }
            100% { transform: translateX(-100px) translateY(100px); }
        }

        .hero-content {
            position: relative;
            z-index: 2;
            text-align: center;
            width: 100%;
        }

        .hero h1 {
            font-size: 1.75rem;
            font-weight: 700;
            margin-bottom: 1rem;
            color: var(--primary-brown);
            line-height: 1.3;
        }

        .hero p {
            font-size: 1rem;
            color: var(--muted);
            margin-bottom: 2rem;
            line-height: 1.6;
        }

        .hero-stats {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 1.5rem;
            margin: 2rem auto;
            max-width: 400px;
        }

        .stat {
            text-align: center;
            padding: 1rem;
        }

        .stat-number {
            font-size: 1.75rem;
            font-weight: 700;
            color: var(--primary-brown);
            display: block;
            margin-bottom: 0.5rem;
        }

        .stat-label {
            font-size: 0.85rem;
            color: var(--muted);
        }

        .cta-buttons {
            display: flex;
            flex-direction: column;
            gap: 1rem;
            justify-content: center;
            align-items: center;
            margin: 2rem 0;
        }

        .btn {
            padding: 1rem 2rem;
            border: none;
            border-radius: 8px;
            font-size: 1rem;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
            text-decoration: none;
            display: inline-flex;
            align-items: center;
            justify-content: center;
            min-width: 200px;
            min-height: 54px;
            width: 100%;
            max-width: 280px;
        }

        .btn-primary {
            background-color: var(--primary-brown);
            color: var(--white);
        }

        .btn-primary:hover {
            background-color: #7a5235;
            transform: translateY(-2px);
        }

        .btn-secondary {
            background-color: transparent;
            color: var(--primary-brown);
            border: 2px solid var(--primary-brown);
        }

        .btn-secondary:hover {
            background-color: var(--primary-brown);
            color: var(--white);
            transform: translateY(-2px);
        }

        .btn-disabled {
            background-color: var(--muted);
            color: var(--white);
            cursor: not-allowed;
            opacity: 0.6;
        }

        .btn-disabled:hover {
            transform: none !important;
        }

        .hero-micro {
            font-size: 0.9rem;
            color: var(--muted);
            margin-top: 1rem;
        }

        @media (min-width: 480px) {
            .hero h1 {
                font-size: 2rem;
            }
            
            .hero p {
                font-size: 1.1rem;
            }
            
            .cta-buttons {
                flex-direction: row;
                flex-wrap: wrap;
            }
            
            .btn {
                width: auto;
            }
        }

        @media (min-width: 768px) {
            .hero {
                padding: 8rem 2rem 4rem;
            }
            
            .hero h1 {
                font-size: 2.5rem;
            }
            
            .hero-stats {
                grid-template-columns: repeat(4, 1fr);
                max-width: 600px;
            }
            
            .stat-number {
                font-size: 2rem;
            }
        }

        @media (min-width: 1024px) {
            .hero h1 {
                font-size: 3rem;
            }
        }

        /* السيكشنز العامة */
        section {
            padding: 4rem 1rem;
        }

        .section-header {
            text-align: center;
            margin-bottom: 3rem;
        }

        .section-header h2 {
            font-size: 1.75rem;
            color: var(--primary-brown);
            margin-bottom: 1rem;
        }

        .section-header p {
            font-size: 1rem;
            color: var(--muted);
            max-width: 600px;
            margin: 0 auto;
        }

        @media (min-width: 768px) {
            section {
                padding: 5rem 2rem;
            }
            
            .section-header h2 {
                font-size: 2.5rem;
            }
            
            .section-header p {
                font-size: 1.1rem;
            }
        }

        /* سيكشن التطوع */
        .volunteer {
            background-color: var(--bg-2);
        }

        .volunteer-content {
            display: grid;
            grid-template-columns: 1fr;
            gap: 2rem;
        }

        .benefits-grid {
            display: grid;
            gap: 1rem;
        }

        .benefit-card {
            background: var(--white);
            padding: 1.5rem;
            border-radius: 12px;
            box-shadow: 0 4px 15px var(--shadow);
            transition: transform 0.3s ease;
        }

        .benefit-card:hover {
            transform: translateY(-5px);
        }

        .benefit-card h4 {
            color: var(--primary-brown);
            margin-bottom: 0.5rem;
            font-size: 1.1rem;
        }

        .volunteer-cta {
            background: var(--primary-brown);
            color: white;
            padding: 1.5rem;
            border-radius: 12px;
            margin-bottom: 2rem;
            text-align: center;
        }

        .volunteer-cta .btn {
            background: var(--white);
            color: var(--primary-brown);
            margin-top: 1rem;
        }

        .faq-list {
            margin-top: 2rem;
        }

        .faq-item {
            background: var(--white);
            margin-bottom: 1rem;
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 2px 8px var(--shadow);
        }

        .faq-question {
            padding: 1.5rem;
            background: var(--accent-sand);
            font-weight: 600;
            cursor: pointer;
            display: flex;
            justify-content: space-between;
            align-items: center;
            font-size: 1rem;
        }

        .faq-answer {
            padding: 1.5rem;
            display: none;
        }

        .faq-item.active .faq-answer {
            display: block;
        }

        @media (min-width: 1024px) {
            .volunteer-content {
                grid-template-columns: 1fr 1fr;
            }
        }

        /* سيكشن التبرع */
        .donate-options {
            display: grid;
            grid-template-columns: 1fr;
            gap: 1rem;
            margin-bottom: 2rem;
        }

        .donate-option {
            background: var(--white);
            padding: 1.5rem;
            border-radius: 12px;
            text-align: center;
            cursor: pointer;
            transition: all 0.3s ease;
            border: 2px solid transparent;
        }

        .donate-option:hover {
            transform: translateY(-5px);
            border-color: var(--primary-brown);
        }

        .donate-option.selected {
            border-color: var(--primary-brown);
            background-color: var(--bg-2);
        }

        .amount {
            font-size: 1.75rem;
            font-weight: 700;
            color: var(--primary-brown);
            margin-bottom: 0.5rem;
        }

        .purpose {
            font-size: 0.9rem;
            color: var(--muted);
        }

        .coming-soon {
            text-align: center;
            padding: 2rem;
            background: var(--bg-2);
            border-radius: 12px;
            margin: 2rem 0;
        }

        .coming-soon i {
            font-size: 2.5rem;
            color: var(--accent-green);
            margin-bottom: 1rem;
        }

        .coming-soon h3 {
            font-size: 1.5rem;
            margin-bottom: 1rem;
            color: var(--primary-brown);
        }

        .breakdown {
            background: var(--white);
            padding: 1.5rem;
            border-radius: 12px;
            margin: 0 auto;
        }

        .breakdown-item {
            display: flex;
            justify-content: space-between;
            margin-bottom: 1rem;
            padding-bottom: 1rem;
            border-bottom: 1px solid var(--accent-sand);
        }

        .breakdown-item:last-child {
            border-bottom: none;
            margin-bottom: 0;
        }

        @media (min-width: 768px) {
            .donate-options {
                grid-template-columns: repeat(3, 1fr);
            }
            
            .breakdown {
                max-width: 500px;
            }
        }

        /* سيكشن عنّا */
        .about {
            background-color: var(--bg-2);
        }

        .story-content {
            display: grid;
            grid-template-columns: 1fr;
            gap: 2rem;
        }

        .story-text {
            font-size: 1rem;
            line-height: 1.8;
        }

        .quote {
            background: var(--white);
            padding: 1.5rem;
            border-right: 4px solid var(--primary-brown);
            margin: 1.5rem 0;
            font-style: italic;
            border-radius: 0 8px 8px 0;
            font-size: 1.1rem;
        }

        .process-steps {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 1.5rem;
            margin-top: 2rem;
        }

        .step {
            text-align: center;
            padding: 1.5rem;
        }

        .step-number {
            width: 50px;
            height: 50px;
            background: var(--primary-brown);
            color: var(--white);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.25rem;
            font-weight: 700;
            margin: 0 auto 1rem;
        }

        @media (min-width: 768px) {
            .story-content {
                grid-template-columns: 1fr 1fr;
            }
            
            .process-steps {
                grid-template-columns: repeat(4, 1fr);
            }
        }

        /* سيكشن التأثير */
        .impact-counters {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 1.5rem;
            margin-bottom: 3rem;
        }

        .impact-counter {
            text-align: center;
            padding: 1.5rem;
            background: var(--white);
            border-radius: 12px;
            box-shadow: 0 4px 15px var(--shadow);
        }

        .counter-number {
            font-size: 2rem;
            font-weight: 700;
            color: var(--primary-brown);
            margin-bottom: 0.5rem;
        }

        @media (min-width: 768px) {
            .impact-counters {
                grid-template-columns: repeat(4, 1fr);
                gap: 2rem;
            }
            
            .counter-number {
                font-size: 2.5rem;
            }
        }

        /* الفوتر */
        footer {
            background-color: var(--text-dark);
            color: var(--white);
            padding: 3rem 1rem 2rem;
        }

        .footer-content {
            display: grid;
            grid-template-columns: 1fr;
            gap: 2rem;
            margin-bottom: 2rem;
        }

        .footer-section h4 {
            color: var(--accent-sand);
            margin-bottom: 1rem;
            font-size: 1.25rem;
        }

        .footer-links {
            list-style: none;
        }

        .footer-links li {
            margin-bottom: 0.5rem;
        }

        .footer-links a {
            color: var(--white);
            text-decoration: none;
            transition: color 0.3s ease;
        }

        .footer-links a:hover {
            color: var(--accent-sand);
        }

        .social-links {
            display: flex;
            gap: 1rem;
            margin-top: 1rem;
        }

        .social-link {
            width: 44px;
            height: 44px;
            background: var(--primary-brown);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            transition: all 0.3s ease;
            position: relative;
        }

        .social-link:hover {
            background: var(--accent-green);
            transform: translateY(-3px);
        }

        .social-link i {
            font-size: 1.2rem;
            color: var(--white);
        }

        .footer-bottom {
            text-align: center;
            padding-top: 2rem;
            border-top: 1px solid var(--muted);
            color: var(--accent-sand);
        }

        @media (min-width: 768px) {
            .footer-content {
                grid-template-columns: repeat(3, 1fr);
            }
        }

        /* CTA الموبايل */
        .mobile-cta {
            display: block;
            position: fixed;
            bottom: 0;
            right: 0;
            width: 100%;
            background: var(--white);
            padding: 1rem;
            box-shadow: 0 -2px 20px var(--shadow);
            z-index: 999;
        }

        .mobile-cta-buttons {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 1rem;
        }

        .mobile-cta .btn {
            min-height: 48px;
            font-size: 0.9rem;
        }

        @media (min-width: 768px) {
            .mobile-cta {
                display: none;
            }
        }

        /* التلميحات */
        .tooltip {
            position: relative;
            display: inline-block;
            margin-right: 5px;
        }

        .tooltip-icon {
            background: var(--accent-sand);
            color: var(--text-dark);
            width: 20px;
            height: 20px;
            border-radius: 50%;
            display: inline-flex;
            align-items: center;
            justify-content: center;
            font-size: 0.8rem;
            cursor: help;
        }

        .tooltip-text {
            position: absolute;
            bottom: 125%;
            right: 50%;
            transform: translateX(50%);
            background: var(--text-dark);
            color: var(--white);
            padding: 0.5rem;
            border-radius: 6px;
            font-size: 0.8rem;
            width: 200px;
            opacity: 0;
            visibility: hidden;
            transition: all 0.3s ease;
            z-index: 1000;
        }

        .tooltip:hover .tooltip-text {
            opacity: 1;
            visibility: visible;
        }

        /* الأنيميشن */
        .content-transition {
            transition: transform 0.25s ease;
        }

        .content-transition.flipping {
            transform: rotateY(90deg);
        }

        /* إصلاح المسافات للهيدر الثابت */
        .section-anchor {
            position: relative;
            top: -80px;
        }
    </style>
</head>
<body>
    <!-- الهيدر -->
    <header>
        <div class="container">
            <div class="header-content">
                <div class="logo">
                    <svg class="logo-svg" viewBox="0 0 100 100">
                        <path class="logo-path" d="M30,30 Q50,10 70,30 T90,30 M30,50 Q50,30 70,50 T90,50 M30,70 Q50,50 70,70 T90,70" fill="none"/>
                    </svg>
                    <span class="logo-text">رزق الهانم</span>
                </div>
                
                <!-- القائمة للكمبيوتر -->
                <nav class="desktop-nav">
                    <a href="#home">الرئيسية</a>
                    <a href="#volunteer">التطوع</a>
                    <a href="#donate">التبرع</a>
                    <a href="#about">عنّا</a>
                    <a href="#impact">التأثير</a>
                    <a href="#contact">اتصل بنا</a>
                </nav>
                
                <div class="header-actions">
                    <button class="language-toggle" id="language-toggle">
                        <span>EN</span>
                    </button>
                    
                    <!-- القائمة للجوال -->
                    <div class="mobile-menu">
                        <button class="hamburger">☰</button>
                        <nav class="mobile-nav">
                            <button class="close-menu">✕</button>
                            <ul>
                                <li><a href="#home">الرئيسية</a></li>
                                <li><a href="#volunteer">التطوع</a></li>
                                <li><a href="#donate">التبرع</a></li>
                                <li><a href="#about">عنّا</a></li>
                                <li><a href="#impact">التأثير</a></li>
                                <li><a href="#contact">اتصل بنا</a></li>
                            </ul>
                        </nav>
                    </div>
                </div>
            </div>
        </div>
    </header>

    <!-- الهيرو -->
    <section class="hero" id="home">
        <div class="hero-background"></div>
        <div class="container">
            <div class="hero-content">
                <h1>رزق الهانم — تحويل الملابس المتبرع بها إلى سبل عيش مستدامة</h1>
                <p>نحن ندرب النساء في ريف مصر على إعادة تدوير المنسوجات وكسب دخل ثابت. انضم إلينا - تبرع، تطوع، أو كن شريكًا.</p>
                
                <div class="hero-stats">
                    <div class="stat">
                        <span class="stat-number" id="volunteers-count">0</span>
                        <span class="stat-label">متطوع</span>
                    </div>
                    <div class="stat">
                        <span class="stat-number" id="items-count">0</span>
                        <span class="stat-label">عنصر تبرع</span>
                    </div>
                    <div class="stat">
                        <span class="stat-number" id="women-count">0</span>
                        <span class="stat-label">امرأة مدربة</span>
                    </div>
                    <div class="stat">
                        <span class="stat-number" id="workshops-count">0</span>
                        <span class="stat-label">ورشة عمل</span>
                    </div>
                </div>
                
                <div class="cta-buttons">
                    <a href="#volunteer" class="btn btn-primary">تطوع معنا</a>
                    <a href="#donate" class="btn btn-secondary btn-disabled">تبرع الآن</a>
                </div>
                
                <p class="hero-micro">بدأنا: 12 أغسطس · 40+ متطوع · 100+ عنصر تبرع</p>
            </div>
        </div>
    </section>

    <!-- التطوع -->
    <section class="volunteer" id="volunteer">
        <div class="section-anchor"></div>
        <div class="container">
            <div class="section-header">
                <h2>التطوع — كن خيطًا في القصة</h2>
                <p>ساعد في توسيع نطاق الحل المحلي: اعمل مع النساء الريفيات، وصمم الحملات، وادير ورش العمل، أو ادعم العمليات اللوجستية. لا توجد خبرة مطلوبة - فقط الالتزام.</p>
            </div>
            
            <div class="volunteer-content">
                <div>
                    <h3 style="margin-bottom: 1rem; color: var(--primary-brown);">فوائد التطوع</h3>
                    <div class="benefits-grid">
                        <div class="benefit-card">
                            <h4>شهادة مشاركة</h4>
                            <p>بعد إكمال 8 مهام تطوعية</p>
                        </div>
                        <div class="benefit-card">
                            <h4>خطاب توصية</h4>
                            <p>بعد إكمال 10+ مهام</p>
                        </div>
                        <div class="benefit-card">
                            <h4>ورش عمل عملية</h4>
                            <p>جلسات مهارات احترافية</p>
                        </div>
                        <div class="benefit-card">
                            <h4>وصول مسبق للأنشطة</h4>
                            <p>أولوية المشاركة في الفعاليات</p>
                        </div>
                        <div class="benefit-card">
                            <h4>شارة رقمية</h4>
                            <p>لعرضها على لينكد إن</p>
                        </div>
                    </div>
                </div>
                
                <div>
                    <div class="volunteer-cta">
                        <h3 style="margin-bottom: 1rem;">مستعد للانضمام؟ تقدم الآن →</h3>
                        <a href="https://docs.google.com/forms/d/e/1FAIpQLScXk6EimANoKZWZAM8LcPrB4bxW6AnWC1GiwBqCRBS5NhgtPQ/viewform?usp=header" 
                           class="btn" target="_blank">استمارة التطوع</a>
                    </div>
                    
                    <div class="faq-list">
                        <h3 style="margin-bottom: 1rem; color: var(--primary-brown);">الأسئلة الشائعة</h3>
                        
                        <div class="faq-item">
                            <div class="faq-question">
                                <span>كم من الوقت مطلوب؟</span>
                                <span>+</span>
                            </div>
                            <div class="faq-answer">
                                <p>مهمة واحدة في الأسبوع؛ جدولة مرنة.</p>
                            </div>
                        </div>
                        
                        <div class="faq-item">
                            <div class="faq-question">
                                <span>هل أحتاج إلى خبرة مهنية؟</span>
                                <span>+</span>
                            </div>
                            <div class="faq-answer">
                                <p>لا. نحن ندرب المتطوعين ونوجههم.</p>
                            </div>
                        </div>
                        
                        <div class="faq-item">
                            <div class="faq-question">
                                <span>ما هو مسار الحصول على خطاب التوصية؟</span>
                                <span>+</span>
                            </div>
                            <div class="faq-answer">
                                <p>أكمل 10+ مهام مثبتة ومشاركة نشطة.</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- التبرع -->
    <section class="donate" id="donate">
        <div class="section-anchor"></div>
        <div class="container">
            <div class="section-header">
                <h2>التبرع — موّل مهارة، غيّر حياة</h2>
                <p>تدعم الأموال المعدات ومواد ورش العمل والخدمات اللوجستية وميزانية تشغيلية شفافة. كل جنيه يمول التدريب وفرص الدخل.</p>
            </div>
            
            <div class="coming-soon">
                <i class="fas fa-heart"></i>
                <h3>التبرعات الإلكترونية ستكون متاحة قريبًا!</h3>
                <p>شكرًا لدعمكم 💛</p>
            </div>
            
            <div class="donate-options">
                <div class="donate-option" data-amount="50">
                    <div class="amount">50 ج.م</div>
                    <div class="purpose">مواد لمتدربة واحدة</div>
                </div>
                <div class="donate-option" data-amount="250">
                    <div class="amount">250 ج.م</div>
                    <div class="purpose">إمدادات ورش عمل لأسبوع</div>
                </div>
                <div class="donate-option" data-amount="500">
                    <div class="amount">500 ج.م</div>
                    <div class="purpose">صيانة ماكينة خياطة وقطع غيار</div>
                </div>
            </div>
            
            <div style="text-align: center; margin: 2rem 0;">
                <button class="btn btn-primary btn-disabled">تبرع الآن</button>
            </div>
            
            <div class="breakdown">
                <h3 style="text-align: center; margin-bottom: 1.5rem; color: var(--primary-brown);">أين يذهب تبرعك؟</h3>
                
                <div class="breakdown-item">
                    <span>60% — مدفوعات للحرفيات</span>
                    <span class="tooltip">
                        <span class="tooltip-icon">?</span>
                        <span class="tooltip-text">المبالغ المدفوعة مباشرة للنساء الحرفيات مقابل عملهن</span>
                    </span>
                </div>
                <div class="breakdown-item">
                    <span>15% — العمليات والخدمات اللوجستية</span>
                    <span class="tooltip">
                        <span class="tooltip-icon">?</span>
                        <span class="tooltip-text">تكاليف النقل والتخزين وإدارة العمليات</span>
                    </span>
                </div>
                <div class="breakdown-item">
                    <span>10% — التغليف والتوصيل</span>
                    <span class="tooltip">
                        <span class="tooltip-icon">?</span>
                        <span class="tooltip-text">مواد التغليف وتكاليف الشحن للمنتجات النهائية</span>
                    </span>
                </div>
                <div class="breakdown-item">
                    <span>10% — التسويق والدعم البيعي</span>
                    <span class="tooltip">
                        <span class="tooltip-icon">?</span>
                        <span class="tooltip-text">أنشطة التسويق والمبيعات لتوسيع نطاق الوصول</span>
                    </span>
                </div>
                <div class="breakdown-item">
                    <span>5% — الإدارة والطوارئ</span>
                    <span class="tooltip">
                        <span class="tooltip-icon">?</span>
                        <span class="tooltip-text">التكاليف الإدارية واحتياطي الطوارئ</span>
                    </span>
                </div>
            </div>
        </div>
    </section>

    <!-- عنّا -->
    <section class="about" id="about">
        <div class="section-anchor"></div>
        <div class="container">
            <div class="section-header">
                <h2>لماذا بدأنا</h2>
            </div>
            
            <div class="story-content">
                <div class="story-text">
                    <p>"لا أريد ملابس - أريد عملاً"، قالت عزة لنا. هذه الجملة غيرت كل شيء. بدأ رزق الهانم لتحويل هذه الجملة إلى مسار: من صناديق التبرعات إلى فرص مخيطة.</p>
                    
                    <div class="quote">"لا أريد ملابس - أريد عملاً"</div>
                    
                    <p>من خلال التدريب والدعم المستمر، نساعد النساء الريفيات على تحويل الملابس المتبرع بها إلى منتجات ذات قيمة مضافة، مما يوفر مصدر دخل مستدام ومهارات قابلة للتطوير.</p>
                </div>
                
                <div>
                    <h3 style="margin-bottom: 1.5rem; color: var(--primary-brown); text-align: center;">كيف نعمل</h3>
                    <div class="process-steps">
                        <div class="step">
                            <div class="step-number">1</div>
                            <h4>التجميع</h4>
                            <p>جمع الملابس المتبرع بها</p>
                        </div>
                        <div class="step">
                            <div class="step-number">2</div>
                            <h4>التدريب</h4>
                            <p>تدريب النساء على إعادة التدوير</p>
                        </div>
                        <div class="step">
                            <div class="step-number">3</div>
                            <h4>الإنتاج</h4>
                            <p>تحويل الملابس إلى منتجات جديدة</p>
                        </div>
                        <div class="step">
                            <div class="step-number">4</div>
                            <h4>السوق</h4>
                            <p>بيع المنتجات وإعادة الأرباح</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- التأثير -->
    <section class="impact" id="impact">
        <div class="section-anchor"></div>
        <div class="container">
            <div class="section-header">
                <h2>تأثيرنا</h2>
                <p>نقيس نجاحنا من خلال الأثر الملموس على حياة النساء والمجتمعات الريفية</p>
            </div>
            
            <div class="impact-counters">
                <div class="impact-counter">
                    <div class="counter-number" id="impact-volunteers">40+</div>
                    <div class="counter-label">متطوع</div>
                </div>
                <div class="impact-counter">
                    <div class="counter-number" id="impact-items">100+</div>
                    <div class="counter-label">عنصر تبرع</div>
                </div>
                <div class="impact-counter">
                    <div class="counter-number" id="impact-women">20+</div>
                    <div class="counter-label">امرأة مدربة</div>
                </div>
                <div class="impact-counter">
                    <div class="counter-number" id="impact-workshops">5+</div>
                    <div class="counter-label">ورشة عمل</div>
                </div>
            </div>
        </div>
    </section>

    <!-- الفوتر -->
    <footer id="contact">
        <div class="container">
            <div class="footer-content">
                <div class="footer-section">
                    <h4>رزق الهانم</h4>
                    <p>تحويل الملابس المتبرع بها إلى سبل عيش مستدامة للنساء في ريف مصر.</p>
                    <div class="social-links">
                        <a href="https://www.instagram.com/reze2_elhanem?igsh=YzljYTk1ODg3Zg==" class="social-link" target="_blank">
                            <i class="fab fa-instagram"></i>
                        </a>
                        <a href="https://www.linkedin.com/company/reze2-el-hanem/" class="social-link" target="_blank">
                            <i class="fab fa-linkedin-in"></i>
                        </a>
                    </div>
                </div>
                
                <div class="footer-section">
                    <h4>روابط سريعة</h4>
                    <ul class="footer-links">
                        <li><a href="#home">الرئيسية</a></li>
                        <li><a href="#volunteer">التطوع</a></li>
                        <li><a href="#donate">التبرع</a></li>
                        <li><a href="#about">عنّا</a></li>
                        <li><a href="#impact">التأثير</a></li>
                    </ul>
                </div>
                
                <div class="footer-section">
                    <h4>اتصل بنا</h4>
                    <p>البريد الإلكتروني: Reze2elhanem@gmail.com</p>
                    <p>تابعنا على وسائل التواصل الاجتماعي</p>
                </div>
            </div>
            
            <div class="footer-bottom">
                <p>© 2025 رزق الهانم — جميع الحقوق محفوظة</p>
            </div>
        </div>
    </footer>

    <!-- CTA الموبايل -->
    <div class="mobile-cta">
        <div class="container">
            <div class="mobile-cta-buttons">
                <a href="#volunteer" class="btn btn-primary">تطوع</a>
                <a href="#donate" class="btn btn-secondary btn-disabled">تبرع</a>
            </div>
        </div>
    </div>

    <script>
        // القائمة المتنقلة
        const hamburger = document.querySelector('.hamburger');
        const closeMenu = document.querySelector('.close-menu');
        const mobileNav = document.querySelector('.mobile-nav');
        
        hamburger.addEventListener('click', () => {
            mobileNav.classList.add('active');
            document.body.style.overflow = 'hidden';
        });
        
        closeMenu.addEventListener('click', () => {
            mobileNav.classList.remove('active');
            document.body.style.overflow = '';
        });
        
        // إغلاق القائمة عند النقر على رابط
        document.querySelectorAll('.mobile-nav a').forEach(link => {
            link.addEventListener('click', () => {
                mobileNav.classList.remove('active');
                document.body.style.overflow = '';
            });
        });
        
        // العدادات
        function animateCounter(element, target, duration = 1200) {
            const start = 0;
            const increment = target / (duration / 16);
            let current = start;
            
            const timer = setInterval(() => {
                current += increment;
                if (current >= target) {
                    element.textContent = target + '+';
                    clearInterval(timer);
                } else {
                    element.textContent = Math.floor(current) + '+';
                }
            }, 16);
        }
        
        function initCounters() {
            animateCounter(document.getElementById('volunteers-count'), 40);
            animateCounter(document.getElementById('items-count'), 100);
            animateCounter(document.getElementById('women-count'), 20);
            animateCounter(document.getElementById('workshops-count'), 5);
        }
        
        // تبديل اللغة
        document.getElementById('language-toggle').addEventListener('click', function() {
            const body = document.body;
            const isArabic = body.getAttribute('dir') === 'rtl';
            
            const content = document.body;
            content.classList.add('flipping');
            
            setTimeout(() => {
                if (isArabic) {
                    body.setAttribute('dir', 'ltr');
                    body.setAttribute('lang', 'en');
                    this.innerHTML = '<span>AR</span>';
                    document.querySelector('.logo-text').textContent = 'Rezq El Hanem';
                    document.querySelector('.hero h1').textContent = 'Rezq El Hanem — Turning donated clothes into sustainable livelihoods';
                    document.querySelector('.hero p').textContent = 'We train women in rural Egypt to upcycle textiles and earn steady income. Join us — donate, volunteer, or partner.';
                } else {
                    body.setAttribute('dir', 'rtl');
                    body.setAttribute('lang', 'ar');
                    this.innerHTML = '<span>EN</span>';
                    document.querySelector('.logo-text').textContent = 'رزق الهانم';
                    document.querySelector('.hero h1').textContent = 'رزق الهانم — تحويل الملابس المتبرع بها إلى سبل عيش مستدامة';
                    document.querySelector('.hero p').textContent = 'نحن ندرب النساء في ريف مصر على إعادة تدوير المنسوجات وكسب دخل ثابت. انضم إلينا - تبرع، تطوع، أو كن شريكًا.';
                }
                
                content.classList.remove('flipping');
            }, 125);
        });
        
        // الأسئلة الشائعة
        document.querySelectorAll('.faq-question').forEach(question => {
            question.addEventListener('click', () => {
                const item = question.parentElement;
                item.classList.toggle('active');
                const icon = question.querySelector('span:last-child');
                icon.textContent = item.classList.contains('active') ? '−' : '+';
            });
        });
        
        // خيارات التبرع
        document.querySelectorAll('.donate-option').forEach(option => {
            option.addEventListener('click', function() {
                document.querySelectorAll('.donate-option').forEach(opt => {
                    opt.classList.remove('selected');
                });
                this.classList.add('selected');
            });
        });
        
        // التنقل السلس
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const targetId = this.getAttribute('href');
                if (targetId === '#') return;
                
                const targetElement = document.querySelector(targetId);
                if (targetElement) {
                    const headerHeight = document.querySelector('header').offsetHeight;
                    const targetPosition = targetElement.getBoundingClientRect().top + window.pageYOffset - headerHeight;
                    
                    window.scrollTo({
                        top: targetPosition,
                        behavior: 'smooth'
                    });
                }
            });
        });
        
        // التهيئة
        document.addEventListener('DOMContentLoaded', function() {
            initCounters();
            document.querySelector('.donate-option').click();
            
            // تعطيل أزرار التبرع
            document.querySelectorAll('.btn-disabled').forEach(btn => {
                btn.addEventListener('click', (e) => e.preventDefault());
            });
        });
    </script>
</body>
</html>
