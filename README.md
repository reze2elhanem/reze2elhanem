<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>رزق الهانم — تحويل الملابس المتبرع بها إلى سبل عيش مستدامة</title>
    <meta name="description" content="رزق الهانم empowers rural women through clothing upcycling, training and sustainable income. Volunteer, donate or partner.">
    
    <!-- Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Cairo:wght@400;600;700&display=swap" rel="stylesheet">
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700&display=swap" rel="stylesheet">
    
    <!-- Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    
    <style>
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
            
            --container-width: 1200px;
            --spacing-xs: 8px;
            --spacing-sm: 16px;
            --spacing-md: 24px;
            --spacing-lg: 32px;
            --spacing-xl: 48px;
            --spacing-xxl: 64px;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Cairo', sans-serif;
            background-color: var(--bg-1);
            color: var(--text-dark);
            line-height: 1.6;
            direction: rtl;
        }

        body[dir="ltr"] {
            font-family: 'Inter', sans-serif;
            direction: ltr;
        }

        .container {
            max-width: var(--container-width);
            margin: 0 auto;
            padding: 0 var(--spacing-md);
        }

        /* Header Styles */
        header {
            background-color: var(--white);
            box-shadow: 0 2px 20px var(--shadow);
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
        }

        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: var(--spacing-sm) 0;
        }

        .logo {
            display: flex;
            align-items: center;
        }

        .logo-svg {
            width: 50px;
            height: 50px;
        }

        .logo-path {
            stroke: var(--primary-brown);
            stroke-width: 2;
            stroke-dasharray: 1000;
            stroke-dashoffset: 1000;
            animation: draw 900ms cubic-bezier(.2,.9,.3,1) forwards;
        }

        @keyframes draw {
            to {
                stroke-dashoffset: 0;
            }
        }

        .logo-text {
            font-size: 1.5rem;
            font-weight: 700;
            color: var(--primary-brown);
            margin-right: var(--spacing-sm);
        }

        nav ul {
            display: flex;
            list-style: none;
            gap: var(--spacing-lg);
        }

        nav a {
            text-decoration: none;
            color: var(--text-dark);
            font-weight: 600;
            transition: color 0.3s ease;
            position: relative;
        }

        nav a:hover {
            color: var(--primary-brown);
        }

        nav a::after {
            content: '';
            position: absolute;
            bottom: -5px;
            right: 0;
            width: 0;
            height: 2px;
            background-color: var(--primary-brown);
            transition: width 0.3s ease;
        }

        nav a:hover::after {
            width: 100%;
        }

        .header-actions {
            display: flex;
            align-items: center;
            gap: var(--spacing-md);
        }

        .language-toggle {
            background: none;
            border: 1px solid var(--accent-sand);
            padding: var(--spacing-xs) var(--spacing-sm);
            border-radius: 4px;
            cursor: pointer;
            display: flex;
            align-items: center;
            gap: var(--spacing-xs);
            transition: all 0.3s ease;
        }

        .language-toggle:hover {
            background-color: var(--accent-sand);
        }

        .hamburger {
            display: none;
            flex-direction: column;
            cursor: pointer;
            gap: 4px;
        }

        .hamburger span {
            width: 25px;
            height: 3px;
            background-color: var(--text-dark);
            transition: all 0.3s ease;
        }

        /* Hero Section */
        .hero {
            background: linear-gradient(135deg, var(--bg-1) 0%, var(--bg-2) 100%);
            padding: calc(var(--spacing-xxl) * 2) 0 var(--spacing-xxl);
            position: relative;
            overflow: hidden;
            margin-top: 80px;
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
            opacity: 0;
            transform: translateY(10px);
            animation: fadeUp 1s ease forwards;
        }

        @keyframes fadeUp {
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .hero h1 {
            font-size: 3rem;
            font-weight: 700;
            margin-bottom: var(--spacing-md);
            color: var(--primary-brown);
        }

        .hero p {
            font-size: 1.25rem;
            color: var(--muted);
            margin-bottom: var(--spacing-xl);
            max-width: 600px;
            margin-right: auto;
            margin-left: auto;
        }

        .hero-stats {
            display: flex;
            justify-content: center;
            gap: var(--spacing-xl);
            margin-bottom: var(--spacing-xl);
            flex-wrap: wrap;
        }

        .stat {
            text-align: center;
        }

        .stat-number {
            font-size: 2rem;
            font-weight: 700;
            color: var(--primary-brown);
            display: block;
        }

        .stat-label {
            font-size: 0.9rem;
            color: var(--muted);
        }

        .cta-buttons {
            display: flex;
            gap: var(--spacing-md);
            justify-content: center;
            flex-wrap: wrap;
        }

        .btn {
            padding: var(--spacing-md) var(--spacing-xl);
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
            position: relative;
            overflow: hidden;
        }

        .btn-primary {
            background-color: var(--primary-brown);
            color: var(--white);
        }

        .btn-primary:hover {
            background-color: #7a5235;
            transform: translateY(-2px);
            box-shadow: 0 8px 20px var(--shadow);
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
            transform: none !important;
        }

        .btn-disabled:hover {
            background-color: var(--muted);
            color: var(--white);
            transform: none !important;
            box-shadow: none !important;
        }

        /* Sections Common Styles */
        section {
            padding: var(--spacing-xxl) 0;
        }

        .section-header {
            text-align: center;
            margin-bottom: var(--spacing-xl);
        }

        .section-header h2 {
            font-size: 2.5rem;
            color: var(--primary-brown);
            margin-bottom: var(--spacing-md);
        }

        .section-header p {
            font-size: 1.1rem;
            color: var(--muted);
            max-width: 600px;
            margin: 0 auto;
        }

        /* Volunteer Section */
        .volunteer {
            background-color: var(--bg-2);
        }

        .volunteer-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: var(--spacing-xl);
            align-items: start;
        }

        .benefits-grid {
            display: grid;
            gap: var(--spacing-md);
        }

        .benefit-card {
            background: var(--white);
            padding: var(--spacing-lg);
            border-radius: 12px;
            box-shadow: 0 4px 15px var(--shadow);
            transition: transform 0.3s ease;
        }

        .benefit-card:hover {
            transform: translateY(-5px);
        }

        .benefit-card h4 {
            color: var(--primary-brown);
            margin-bottom: var(--spacing-xs);
        }

        .faq-list {
            margin-top: var(--spacing-lg);
        }

        .faq-item {
            background: var(--white);
            margin-bottom: var(--spacing-sm);
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 2px 8px var(--shadow);
        }

        .faq-question {
            padding: var(--spacing-md);
            background: var(--accent-sand);
            font-weight: 600;
            cursor: pointer;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .faq-answer {
            padding: var(--spacing-md);
            display: none;
        }

        .faq-item.active .faq-answer {
            display: block;
        }

        /* Donate Section */
        .donate-options {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: var(--spacing-md);
            margin-bottom: var(--spacing-xl);
        }

        .donate-option {
            background: var(--white);
            padding: var(--spacing-lg);
            border-radius: 12px;
            text-align: center;
            cursor: pointer;
            transition: all 0.3s ease;
            border: 2px solid transparent;
        }

        .donate-option:hover {
            transform: translateY(-5px);
            border-color: var(--primary-brown);
            box-shadow: 0 8px 20px var(--shadow);
        }

        .donate-option.selected {
            border-color: var(--primary-brown);
            background-color: var(--bg-2);
        }

        .amount {
            font-size: 2rem;
            font-weight: 700;
            color: var(--primary-brown);
            margin-bottom: var(--spacing-xs);
        }

        .purpose {
            font-size: 0.9rem;
            color: var(--muted);
        }

        .custom-amount {
            display: flex;
            gap: var(--spacing-sm);
            max-width: 400px;
            margin: 0 auto var(--spacing-xl);
        }

        .custom-amount input {
            flex: 1;
            padding: var(--spacing-md);
            border: 2px solid var(--accent-sand);
            border-radius: 8px;
            font-size: 1rem;
        }

        .breakdown {
            background: var(--white);
            padding: var(--spacing-lg);
            border-radius: 12px;
            max-width: 500px;
            margin: 0 auto;
        }

        .breakdown-item {
            display: flex;
            justify-content: space-between;
            margin-bottom: var(--spacing-sm);
            padding-bottom: var(--spacing-sm);
            border-bottom: 1px solid var(--accent-sand);
        }

        .breakdown-item:last-child {
            border-bottom: none;
            margin-bottom: 0;
        }

        .coming-soon {
            text-align: center;
            padding: var(--spacing-xl);
            background: var(--bg-2);
            border-radius: 12px;
            margin: var(--spacing-lg) 0;
        }

        .coming-soon i {
            font-size: 3rem;
            color: var(--accent-green);
            margin-bottom: var(--spacing-md);
        }

        /* About Section */
        .about {
            background-color: var(--bg-2);
        }

        .story-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: var(--spacing-xl);
            align-items: center;
        }

        .story-text {
            font-size: 1.1rem;
            line-height: 1.8;
        }

        .quote {
            background: var(--white);
            padding: var(--spacing-lg);
            border-right: 4px solid var(--primary-brown);
            margin: var(--spacing-lg) 0;
            font-style: italic;
            border-radius: 0 8px 8px 0;
        }

        .process-steps {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: var(--spacing-lg);
            margin-top: var(--spacing-xl);
        }

        .step {
            text-align: center;
            padding: var(--spacing-lg);
        }

        .step-number {
            width: 60px;
            height: 60px;
            background: var(--primary-brown);
            color: var(--white);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.5rem;
            font-weight: 700;
            margin: 0 auto var(--spacing-md);
        }

        /* Impact Section */
        .impact-counters {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: var(--spacing-xl);
            margin-bottom: var(--spacing-xxl);
        }

        .impact-counter {
            text-align: center;
            padding: var(--spacing-lg);
            background: var(--white);
            border-radius: 12px;
            box-shadow: 0 4px 15px var(--shadow);
        }

        .counter-number {
            font-size: 3rem;
            font-weight: 700;
            color: var(--primary-brown);
            margin-bottom: var(--spacing-sm);
        }

        /* Partners Section - Temporarily Hidden */
        .partners {
            display: none;
            background-color: var(--bg-2);
        }

        .partners-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
            gap: var(--spacing-xl);
            align-items: center;
        }

        .partner-logo {
            background: var(--white);
            padding: var(--spacing-lg);
            border-radius: 12px;
            display: flex;
            align-items: center;
            justify-content: center;
            height: 120px;
            transition: transform 0.3s ease;
        }

        .partner-logo:hover {
            transform: scale(1.05);
        }

        /* Footer */
        footer {
            background-color: var(--text-dark);
            color: var(--white);
            padding: var(--spacing-xxl) 0 var(--spacing-xl);
        }

        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: var(--spacing-xl);
            margin-bottom: var(--spacing-xl);
        }

        .footer-section h4 {
            color: var(--accent-sand);
            margin-bottom: var(--spacing-md);
        }

        .footer-links {
            list-style: none;
        }

        .footer-links li {
            margin-bottom: var(--spacing-xs);
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
            gap: var(--spacing-md);
            margin-top: var(--spacing-md);
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

        .social-tooltip {
            position: absolute;
            bottom: -40px;
            right: 50%;
            transform: translateX(50%);
            background: var(--text-dark);
            color: var(--white);
            padding: var(--spacing-xs) var(--spacing-sm);
            border-radius: 4px;
            font-size: 0.8rem;
            white-space: nowrap;
            opacity: 0;
            visibility: hidden;
            transition: all 0.3s ease;
        }

        .social-link:hover .social-tooltip {
            opacity: 1;
            visibility: visible;
            bottom: -35px;
        }

        .footer-bottom {
            text-align: center;
            padding-top: var(--spacing-lg);
            border-top: 1px solid var(--muted);
            color: var(--accent-sand);
        }

        /* Modal */
        .modal {
            display: none;
            position: fixed;
            top: 0;
            right: 0;
            width: 100%;
            height: 100%;
            background: rgba(0,0,0,0.5);
            z-index: 2000;
            align-items: center;
            justify-content: center;
        }

        .modal.active {
            display: flex;
        }

        .modal-content {
            background: var(--white);
            padding: var(--spacing-xl);
            border-radius: 12px;
            max-width: 500px;
            width: 90%;
            transform: scale(0.95);
            opacity: 0;
            transition: all 0.2s ease;
        }

        .modal.active .modal-content {
            transform: scale(1);
            opacity: 1;
        }

        .modal-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: var(--spacing-lg);
        }

        .close-modal {
            background: none;
            border: none;
            font-size: 1.5rem;
            cursor: pointer;
            color: var(--muted);
        }

        /* Responsive Design */
        @media (max-width: 1024px) {
            .hero h1 {
                font-size: 2.5rem;
            }
            
            .volunteer-content,
            .story-content {
                grid-template-columns: 1fr;
            }
        }

        @media (max-width: 768px) {
            .header-content {
                flex-wrap: wrap;
            }
            
            nav {
                display: none;
                width: 100%;
                margin-top: var(--spacing-md);
            }
            
            nav.active {
                display: block;
            }
            
            nav ul {
                flex-direction: column;
                gap: var(--spacing-sm);
            }
            
            .hamburger {
                display: flex;
            }
            
            .hero h1 {
                font-size: 2rem;
            }
            
            .hero-stats {
                gap: var(--spacing-lg);
            }
            
            .cta-buttons {
                flex-direction: column;
                align-items: center;
            }
            
            .btn {
                width: 100%;
                max-width: 300px;
            }
            
            .impact-counters {
                grid-template-columns: repeat(2, 1fr);
            }
        }

        @media (max-width: 640px) {
            .hero h1 {
                font-size: 1.75rem;
            }
            
            .section-header h2 {
                font-size: 2rem;
            }
            
            .impact-counters {
                grid-template-columns: 1fr;
            }
            
            .donate-options {
                grid-template-columns: 1fr;
            }
            
            .process-steps {
                grid-template-columns: 1fr;
            }
        }

        /* Language Toggle Animation */
        .content-transition {
            transition: transform 0.25s ease;
        }

        .content-transition.flipping {
            transform: rotateY(90deg);
        }

        /* Sticky Mobile CTA */
        .mobile-cta {
            display: none;
            position: fixed;
            bottom: 0;
            right: 0;
            width: 100%;
            background: var(--white);
            padding: var(--spacing-sm);
            box-shadow: 0 -2px 20px var(--shadow);
            z-index: 1000;
        }

        .mobile-cta-buttons {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: var(--spacing-sm);
        }

        @media (max-width: 768px) {
            .mobile-cta {
                display: block;
            }
        }

        /* Tooltip */
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
            padding: var(--spacing-sm);
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
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container">
            <div class="header-content">
                <div class="logo">
                    <svg class="logo-svg" viewBox="0 0 100 100">
                        <path class="logo-path" d="M30,30 Q50,10 70,30 T90,30 M30,50 Q50,30 70,50 T90,50 M30,70 Q50,50 70,70 T90,70" fill="none"/>
                    </svg>
                    <span class="logo-text">رزق الهانم</span>
                </div>
                
                <nav id="main-nav">
                    <ul>
                        <li><a href="#home">الرئيسية</a></li>
                        <li><a href="#volunteer">التطوع</a></li>
                        <li><a href="#donate">التبرع</a></li>
                        <li><a href="#about">عنّا</a></li>
                        <li><a href="#impact">التأثير</a></li>
                        <li><a href="#contact">اتصل بنا</a></li>
                    </ul>
                </nav>
                
                <div class="header-actions">
                    <button class="language-toggle" id="language-toggle">
                        <span>EN</span>
                    </button>
                    <div class="hamburger" id="hamburger">
                        <span></span>
                        <span></span>
                        <span></span>
                    </div>
                </div>
            </div>
        </div>
    </header>

    <!-- Hero Section -->
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
                    <a href="#donate" class="btn btn-secondary">تبرع الآن</a>
                </div>
                
                <p style="margin-top: var(--spacing-md); font-size: 0.9rem; color: var(--muted);">
                    بدأنا: 12 أغسطس · 40+ متطوع · 100+ عنصر تبرع
                </p>
            </div>
        </div>
    </section>

    <!-- Volunteer Section -->
    <section class="volunteer" id="volunteer">
        <div class="container">
            <div class="section-header">
                <h2>التطوع — كن خيطًا في القصة</h2>
                <p>ساعد في توسيع نطاق الحل المحلي: اعمل مع النساء الريفيات، وصمم الحملات، وادير ورش العمل، أو ادعم العمليات اللوجستية. لا توجد خبرة مطلوبة - فقط الالتزام.</p>
            </div>
            
            <div class="volunteer-content">
                <div>
                    <h3 style="margin-bottom: var(--spacing-md); color: var(--primary-brown);">فوائد التطوع</h3>
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
                    <div style="background: var(--primary-brown); color: white; padding: var(--spacing-lg); border-radius: 12px; margin-bottom: var(--spacing-lg); text-align: center;">
                        <h3 style="margin-bottom: var(--spacing-sm);">مستعد للانضمام؟ تقدم الآن →</h3>
                        <a href="https://docs.google.com/forms/d/e/1FAIpQLScXk6EimANoKZWZAM8LcPrB4bxW6AnWC1GiwBqCRBS5NhgtPQ/viewform?usp=header" 
                           class="btn" style="background: var(--white); color: var(--primary-brown);">استمارة التطوع</a>
                    </div>
                    
                    <div class="faq-list">
                        <h3 style="margin-bottom: var(--spacing-md); color: var(--primary-brown);">الأسئلة الشائعة</h3>
                        
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

    <!-- Donate Section -->
    <section class="donate" id="donate">
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
            
            <div style="text-align: center; margin-bottom: var(--spacing-xl);">
                <button class="btn btn-primary btn-disabled" style="padding: var(--spacing-lg) var(--spacing-xxl);">
                    تبرع الآن
                </button>
            </div>
            
            <div class="breakdown">
                <h3 style="text-align: center; margin-bottom: var(--spacing-lg); color: var(--primary-brown);">أين يذهب تبرعك؟</h3>
                
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

    <!-- About Section -->
    <section class="about" id="about">
        <div class="container">
            <div class="section-header">
                <h2>لماذا بدأنا</h2>
            </div>
            
            <div class="story-content">
                <div class="story-text">
                    <p>"لا أريد ملابس - أريد عملاً"، قالت عزة لنا. هذه الجملة غيرت كل شيء. بدأ رزق الهانم لتحويل هذه الجملة إلى مسار: من صناديق التبرعات إلى فرص مخيطة.</p>
                    
                    <div class="quote">
                        "لا أريد ملابس - أريد عملاً"
                    </div>
                    
                    <p>من خلال التدريب والدعم المستمر، نساعد النساء الريفيات على تحويل الملابس المتبرع بها إلى منتجات ذات قيمة مضافة، مما يوفر مصدر دخل مستدام ومهارات قابلة للتطوير.</p>
                </div>
                
                <div>
                    <h3 style="margin-bottom: var(--spacing-lg); color: var(--primary-brown); text-align: center;">كيف نعمل</h3>
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

    <!-- Impact Section -->
    <section class="impact" id="impact">
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

    <!-- Partners Section - Temporarily Hidden -->
    <section class="partners" id="partners" style="display: none;">
        <div class="container">
            <div class="section-header">
                <h2>شركاؤنا</h2>
                <p>نعمل مع منظمات وشركات ملتزمة بدعم تمكين المرأة والاستدامة</p>
            </div>
            
            <div class="partners-grid">
                <div class="partner-logo">شريك 1</div>
                <div class="partner-logo">شريك 2</div>
                <div class="partner-logo">شريك 3</div>
                <div class="partner-logo">شريك 4</div>
                <div class="partner-logo">شريك 5</div>
                <div class="partner-logo">شريك 6</div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer id="contact">
        <div class="container">
            <div class="footer-content">
                <div class="footer-section">
                    <h4>رزق الهانم</h4>
                    <p>تحويل الملابس المتبرع بها إلى سبل عيش مستدامة للنساء في ريف مصر.</p>
                    <div class="social-links">
                        <a href="https://www.instagram.com/reze2_elhanem?igsh=YzljYTk1ODg3Zg==" class="social-link" target="_blank">
                            <i class="fab fa-instagram"></i>
                            <span class="social-tooltip">تابعنا على إنستجرام</span>
                        </a>
                        <a href="https://www.linkedin.com/company/reze2-el-hanem/" class="social-link" target="_blank">
                            <i class="fab fa-linkedin-in"></i>
                            <span class="social-tooltip">تابعنا على لينكد إن</span>
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

    <!-- Donate Modal -->
    <div class="modal" id="donate-modal">
        <div class="modal-content">
            <div class="modal-header">
                <h3>اكمل تبرعك</h3>
                <button class="close-modal" onclick="closeDonateModal()">×</button>
            </div>
            
            <div id="modal-body">
                <!-- This will be populated dynamically -->
            </div>
        </div>
    </div>

    <!-- Mobile CTA -->
    <div class="mobile-cta">
        <div class="container">
            <div class="mobile-cta-buttons">
                <a href="#volunteer" class="btn btn-primary">تطوع</a>
                <a href="#donate" class="btn btn-secondary btn-disabled">تبرع</a>
            </div>
        </div>
    </div>

    <script>
        // Counter Animation
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

        // Initialize counters when in viewport
        function initCounters() {
            const volunteersCount = document.getElementById('volunteers-count');
            const itemsCount = document.getElementById('items-count');
            const womenCount = document.getElementById('women-count');
            const workshopsCount = document.getElementById('workshops-count');
            
            animateCounter(volunteersCount, 40);
            animateCounter(itemsCount, 100);
            animateCounter(womenCount, 20);
            animateCounter(workshopsCount, 5);
            
            // Impact section counters
            document.getElementById('impact-volunteers').textContent = '40+';
            document.getElementById('impact-items').textContent = '100+';
            document.getElementById('impact-women').textContent = '20+';
            document.getElementById('impact-workshops').textContent = '5+';
        }

        // Language Toggle
        document.getElementById('language-toggle').addEventListener('click', function() {
            const body = document.body;
            const isArabic = body.getAttribute('dir') === 'rtl';
            
            // Animation flip
            const content = document.querySelector('.content-transition') || document.body;
            content.classList.add('flipping');
            
            setTimeout(() => {
                if (isArabic) {
                    body.setAttribute('dir', 'ltr');
                    body.setAttribute('lang', 'en');
                    this.innerHTML = '<span>AR</span>';
                    // Update all text content to English here
                    document.querySelector('.logo-text').textContent = 'Rezq El Hanem';
                    document.querySelector('.hero h1').textContent = 'Rezq El Hanem — Turning donated clothes into sustainable livelihoods';
                    document.querySelector('.hero p').textContent = 'We train women in rural Egypt to upcycle textiles and earn steady income. Join us — donate, volunteer, or partner.';
                    // ... update all other text content
                } else {
                    body.setAttribute('dir', 'rtl');
                    body.setAttribute('lang', 'ar');
                    this.innerHTML = '<span>EN</span>';
                    // Update all text content to Arabic here
                    document.querySelector('.logo-text').textContent = 'رزق الهانم';
                    document.querySelector('.hero h1').textContent = 'رزق الهانم — تحويل الملابس المتبرع بها إلى سبل عيش مستدامة';
                    document.querySelector('.hero p').textContent = 'نحن ندرب النساء في ريف مصر على إعادة تدوير المنسوجات وكسب دخل ثابت. انضم إلينا - تبرع، تطوع، أو كن شريكًا.';
                    // ... update all other text content
                }
                
                content.classList.remove('flipping');
            }, 125);
        });

        // Mobile Navigation
        document.getElementById('hamburger').addEventListener('click', function() {
            const nav = document.getElementById('main-nav');
            nav.classList.toggle('active');
            this.classList.toggle('active');
        });

        // FAQ Accordion
        document.querySelectorAll('.faq-question').forEach(question => {
            question.addEventListener('click', () => {
                const item = question.parentElement;
                item.classList.toggle('active');
                
                // Toggle plus/minus icon
                const icon = question.querySelector('span:last-child');
                icon.textContent = item.classList.contains('active') ? '−' : '+';
            });
        });

        // Donate Option Selection
        let selectedAmount = 0;
        
        document.querySelectorAll('.donate-option').forEach(option => {
            option.addEventListener('click', function() {
                document.querySelectorAll('.donate-option').forEach(opt => {
                    opt.classList.remove('selected');
                });
                this.classList.add('selected');
                selectedAmount = parseInt(this.getAttribute('data-amount'));
            });
        });

        function selectCustomAmount() {
            const customAmount = document.getElementById('custom-amount').value;
            if (customAmount) {
                selectedAmount = parseInt(customAmount);
                document.querySelectorAll('.donate-option').forEach(opt => {
                    opt.classList.remove('selected');
                });
            }
        }

        // Modal Functions - Disabled for now
        function openDonateModal() {
            // Donation functionality temporarily disabled
            return false;
        }

        function closeDonateModal() {
            document.getElementById('donate-modal').classList.remove('active');
        }

        // Close modal when clicking outside
        document.getElementById('donate-modal').addEventListener('click', function(e) {
            if (e.target === this) {
                closeDonateModal();
            }
        });

        // Smooth scrolling for anchor links
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
                    
                    // Close mobile menu if open
                    document.getElementById('main-nav').classList.remove('active');
                    document.getElementById('hamburger').classList.remove('active');
                }
            });
        });

        // Initialize on load
        document.addEventListener('DOMContentLoaded', function() {
            initCounters();
            
            // Add content transition class to body
            document.body.classList.add('content-transition');
            
            // Initialize first donate option as selected
            document.querySelector('.donate-option').click();
            
            // Disable donation buttons
            document.querySelectorAll('a[href="#donate"], .btn-secondary').forEach(btn => {
                if (btn.textContent.includes('تبرع') || btn.textContent.includes('Donate')) {
                    btn.classList.add('btn-disabled');
                    btn.addEventListener('click', function(e) {
                        e.preventDefault();
                    });
                }
            });
        });

        // Intersection Observer for scroll animations
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -50px 0px'
        };

        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.style.opacity = '1';
                    entry.target.style.transform = 'translateY(0)';
                }
            });
        }, observerOptions);

        // Observe elements for animation
        document.querySelectorAll('.benefit-card, .impact-counter, .step, .partner-logo').forEach(el => {
            el.style.opacity = '0';
            el.style.transform = 'translateY(18px)';
            el.style.transition = 'opacity 0.6s ease, transform 0.6s ease';
            observer.observe(el);
        });
    </script>
</body>
</html>
