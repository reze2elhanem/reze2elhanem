<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>رزق الهانم — تحويل الملابس المتبرع بها إلى سبل عيش مستدامة</title>
    
    <!-- Fonts -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Cairo:wght@300;400;600;700&display=swap" rel="stylesheet">
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;500;600;700&display=swap" rel="stylesheet">
    <link href="https://fonts.googleapis.com/css2?family=Dancing+Script:wght@400;500;600;700&display=swap" rel="stylesheet">
    
    <!-- Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    
    <style>
        /* Reset CSS */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            -webkit-tap-highlight-color: transparent;
        }

        html {
            scroll-behavior: smooth;
            font-size: 16px;
        }

        body {
            font-family: 'Cairo', sans-serif;
            background: linear-gradient(135deg, #F7EFE6 0%, #FFF9F4 50%, #F8F4F0 100%);
            color: #2E2E2E;
            line-height: 1.7;
            direction: rtl;
            overflow-x: hidden;
            min-height: 100vh;
            width: 100%;
        }

        :root {
            --bg-1: #F7EFE6;
            --bg-2: #FFF9F4;
            --primary-brown: #8B5E3C;
            --accent-green: #3E7B4E;
            --accent-sand: #E7CBAF;
            --accent-pink: #E8B4B8;
            --accent-gold: #D4AF37;
            --text-dark: #2E2E2E;
            --muted: #6B6B6B;
            --white: #FFFFFF;
            --success: #2EAC6A;
            --shadow: rgba(46,46,46,0.1);
            --shadow-strong: rgba(46,46,46,0.15);
        }

        .container {
            max-width: 1400px;
            margin: 0 auto;
            padding: 0 1rem;
            width: 100%;
        }

        /* Enhanced Header with Glass Effect */
        header {
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(20px);
            -webkit-backdrop-filter: blur(20px);
            box-shadow: 0 8px 32px rgba(139, 94, 60, 0.1);
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            height: 70px;
            border-bottom: 1px solid rgba(255, 255, 255, 0.2);
            transition: all 0.4s cubic-bezier(0.22, 0.61, 0.36, 1);
        }

        header.scrolled {
            height: 65px;
            background: rgba(255, 255, 255, 0.98);
            box-shadow: 0 5px 20px rgba(139, 94, 60, 0.15);
        }

        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
            height: 100%;
            padding: 0 0.5rem;
            width: 100%;
        }

        .logo {
            display: flex;
            align-items: center;
            gap: 0.8rem;
            text-decoration: none;
            transition: transform 0.3s ease;
        }

        .logo:hover {
            transform: translateY(-2px);
        }

        .logo-svg {
            width: 40px;
            height: 40px;
            transition: all 0.4s ease;
        }

        .logo:hover .logo-svg {
            transform: rotate(5deg) scale(1.1);
        }

        .logo-path {
            stroke: var(--primary-brown);
            stroke-width: 2.5;
            stroke-dasharray: 1000;
            stroke-dashoffset: 1000;
            animation: draw 1.5s cubic-bezier(.2,.9,.3,1) forwards;
        }

        @keyframes draw {
            to { stroke-dashoffset: 0; }
        }

        .logo-text {
            font-family: 'Playfair Display', serif;
            font-size: 1.3rem;
            font-weight: 700;
            color: var(--primary-brown);
            letter-spacing: -0.5px;
            text-shadow: 0 2px 4px rgba(0,0,0,0.05);
        }

        /* Mobile Navigation */
        .mobile-nav-toggle {
            display: none;
            background: none;
            border: none;
            font-size: 1.5rem;
            color: var(--primary-brown);
            cursor: pointer;
            z-index: 1001;
            padding: 0.5rem;
        }

        /* Enhanced Navigation */
        .desktop-nav {
            display: flex;
            gap: 1.5rem;
        }

        .desktop-nav a {
            text-decoration: none;
            color: var(--text-dark);
            font-weight: 600;
            font-size: 0.95rem;
            transition: all 0.4s cubic-bezier(0.22, 0.61, 0.36, 1);
            position: relative;
            padding: 0.5rem 0;
        }

        .desktop-nav a::before {
            content: '';
            position: absolute;
            bottom: 0;
            right: 0;
            width: 0;
            height: 3px;
            background: linear-gradient(90deg, var(--accent-pink), var(--accent-gold));
            border-radius: 3px;
            transition: width 0.4s cubic-bezier(0.22, 0.61, 0.36, 1);
        }

        .desktop-nav a:hover {
            color: var(--primary-brown);
            transform: translateY(-2px);
        }

        .desktop-nav a:hover::before {
            width: 100%;
        }

        .header-actions {
            display: flex;
            align-items: center;
            gap: 0.8rem;
        }

        .language-toggle {
            background: linear-gradient(135deg, rgba(139, 94, 60, 0.1), rgba(232, 180, 184, 0.1));
            border: 2px solid rgba(139, 94, 60, 0.2);
            padding: 0.4rem 0.8rem;
            border-radius: 50px;
            cursor: pointer;
            display: flex;
            align-items: center;
            gap: 0.5rem;
            transition: all 0.4s cubic-bezier(0.22, 0.61, 0.36, 1);
            font-weight: 600;
            color: var(--primary-brown);
            backdrop-filter: blur(10px);
            font-size: 0.85rem;
        }

        .language-toggle:hover {
            background: linear-gradient(135deg, rgba(139, 94, 60, 0.15), rgba(232, 180, 184, 0.15));
            border-color: rgba(139, 94, 60, 0.3);
            transform: translateY(-3px) scale(1.05);
            box-shadow: 0 8px 25px rgba(139, 94, 60, 0.2);
        }

        /* Ultimate Hero Section */
        .hero {
            position: relative;
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            overflow: hidden;
            background: linear-gradient(135deg, #F7EFE6 0%, #FFF9F4 30%, #F8F4F0 70%, #F7EFE6 100%);
            padding: 70px 0 2rem;
            width: 100%;
        }

        .hero-background {
            position: absolute;
            top: 0;
            right: 0;
            width: 100%;
            height: 100%;
            opacity: 0.4;
            background: 
                radial-gradient(circle at 20% 20%, rgba(139, 94, 60, 0.1) 0%, transparent 50%),
                radial-gradient(circle at 80% 80%, rgba(232, 180, 184, 0.1) 0%, transparent 50%),
                radial-gradient(circle at 40% 40%, rgba(212, 175, 55, 0.05) 0%, transparent 50%);
            animation: floatBackground 20s ease-in-out infinite;
        }

        @keyframes floatBackground {
            0%, 100% { transform: translate(0, 0) scale(1); }
            33% { transform: translate(-30px, -20px) scale(1.05); }
            66% { transform: translate(20px, 30px) scale(0.95); }
        }

        .hero-particles {
            position: absolute;
            top: 0;
            right: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
        }

        .particle {
            position: absolute;
            background: linear-gradient(135deg, var(--accent-pink), var(--accent-gold));
            border-radius: 50%;
            opacity: 0.3;
            animation: floatParticle 15s infinite linear;
        }

        @keyframes floatParticle {
            0% { transform: translateY(100vh) rotate(0deg); }
            100% { transform: translateY(-100px) rotate(360deg); }
        }

        .hero-content {
            position: relative;
            z-index: 10;
            text-align: center;
            width: 100%;
            max-width: 1200px;
            padding: 1rem;
        }

        .hero h1 {
            font-family: 'Playfair Display', serif;
            font-size: 2rem;
            font-weight: 700;
            margin-bottom: 1.2rem;
            color: var(--primary-brown);
            line-height: 1.2;
            text-shadow: 0 4px 20px rgba(0,0,0,0.1);
            background: linear-gradient(135deg, var(--primary-brown), #A07854, var(--accent-gold));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            animation: shimmer 3s ease-in-out infinite;
        }

        @keyframes shimmer {
            0%, 100% { background-position: -200% center; }
            50% { background-position: 200% center; }
        }

        .hero p {
            font-size: 1rem;
            color: var(--muted);
            margin-bottom: 2rem;
            line-height: 1.6;
            max-width: 800px;
            margin-left: auto;
            margin-right: auto;
            font-weight: 300;
            backdrop-filter: blur(10px);
            padding: 1.2rem;
            border-radius: 15px;
            background: rgba(255,255,255,0.3);
            border: 1px solid rgba(255,255,255,0.2);
        }

        .hero-stats {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 1rem;
            margin: 2.5rem auto;
            max-width: 600px;
            width: 100%;
        }

        .stat {
            text-align: center;
            padding: 1.2rem 0.8rem;
            background: rgba(255,255,255,0.7);
            border-radius: 15px;
            backdrop-filter: blur(20px);
            box-shadow: 0 8px 20px rgba(0,0,0,0.1);
            border: 1px solid rgba(255,255,255,0.3);
            transition: all 0.5s cubic-bezier(0.22, 0.61, 0.36, 1);
            position: relative;
            overflow: hidden;
        }

        .stat::before {
            content: '';
            position: absolute;
            top: 0;
            right: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(135deg, transparent, rgba(232, 180, 184, 0.1), transparent);
            transform: translateX(-100%);
            transition: transform 0.6s ease;
        }

        .stat:hover {
            transform: translateY(-8px) scale(1.02);
            box-shadow: 0 15px 30px rgba(139, 94, 60, 0.2);
        }

        .stat:hover::before {
            transform: translateX(100%);
        }

        .stat-number {
            font-size: 1.8rem;
            font-weight: 700;
            color: var(--primary-brown);
            display: block;
            margin-bottom: 0.3rem;
            text-shadow: 0 2px 10px rgba(0,0,0,0.1);
            line-height: 1;
        }

        .stat-label {
            font-size: 0.8rem;
            color: var(--muted);
            font-weight: 600;
            line-height: 1.2;
        }

        .cta-buttons {
            display: flex;
            flex-direction: column;
            gap: 1rem;
            justify-content: center;
            align-items: center;
            margin: 2.5rem 0;
            width: 100%;
        }

        .btn {
            padding: 1rem 2rem;
            border: none;
            border-radius: 50px;
            font-size: 1rem;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.5s cubic-bezier(0.22, 0.61, 0.36, 1);
            text-decoration: none;
            display: inline-flex;
            align-items: center;
            justify-content: center;
            gap: 0.8rem;
            position: relative;
            overflow: hidden;
            backdrop-filter: blur(10px);
            width: 100%;
            max-width: 280px;
        }

        .btn::before {
            content: '';
            position: absolute;
            top: 0;
            right: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(135deg, rgba(255,255,255,0.2), transparent);
            transform: translateX(-100%);
            transition: transform 0.6s ease;
        }

        .btn:hover::before {
            transform: translateX(0);
        }

        .btn-primary {
            background: linear-gradient(135deg, var(--primary-brown), #A07854, var(--primary-brown));
            background-size: 200% 200%;
            color: var(--white);
            box-shadow: 0 8px 20px rgba(139, 94, 60, 0.4);
            animation: gradientShift 3s ease infinite;
        }

        @keyframes gradientShift {
            0%, 100% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
        }

        .btn-primary:hover {
            transform: translateY(-5px) scale(1.03);
            box-shadow: 0 12px 25px rgba(139, 94, 60, 0.6);
        }

        .btn-secondary {
            background: transparent;
            color: var(--primary-brown);
            border: 2px solid var(--primary-brown);
            box-shadow: 0 6px 15px rgba(139, 94, 60, 0.2);
        }

        .btn-secondary:hover {
            background: var(--primary-brown);
            color: var(--white);
            transform: translateY(-5px) scale(1.03);
            box-shadow: 0 12px 20px rgba(139, 94, 60, 0.3);
        }

        .btn-disabled {
            background: var(--muted);
            color: var(--white);
            cursor: not-allowed;
            opacity: 0.7;
        }

        .btn-disabled:hover {
            transform: none !important;
            box-shadow: 0 6px 15px rgba(139, 94, 60, 0.2) !important;
        }

        .hero-micro {
            font-size: 0.8rem;
            color: var(--muted);
            margin-top: 1.5rem;
            backdrop-filter: blur(10px);
            padding: 0.8rem 1.2rem;
            border-radius: 50px;
            background: rgba(255,255,255,0.3);
            border: 1px solid rgba(255,255,255,0.2);
            display: inline-block;
            max-width: 100%;
        }

        /* Enhanced Volunteer Section */
        .volunteer {
            background: linear-gradient(135deg, rgba(255,255,255,0.9) 0%, rgba(248, 244, 240, 0.9) 100%);
            padding: 4rem 0;
            position: relative;
            overflow: hidden;
            width: 100%;
        }

        .volunteer::before {
            content: '';
            position: absolute;
            top: 0;
            right: 0;
            width: 100%;
            height: 100%;
            background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100"><path d="M30,30 Q50,10 70,30 T90,30" stroke="%238B5E3C" fill="none" stroke-width="1" opacity="0.03"/></svg>');
            background-size: 300px 300px;
            animation: float 30s linear infinite;
        }

        .section-header {
            text-align: center;
            margin-bottom: 2.5rem;
            position: relative;
        }

        .section-header h2 {
            font-family: 'Playfair Display', serif;
            font-size: 1.8rem;
            color: var(--primary-brown);
            margin-bottom: 1rem;
            position: relative;
            display: inline-block;
        }

        .section-header h2::after {
            content: '';
            position: absolute;
            bottom: -10px;
            right: 0;
            width: 100%;
            height: 3px;
            background: linear-gradient(90deg, transparent, var(--accent-pink), var(--accent-gold), var(--accent-pink), transparent);
            border-radius: 3px;
            animation: widthPulse 3s ease-in-out infinite;
        }

        @keyframes widthPulse {
            0%, 100% { width: 100%; }
            50% { width: 80%; }
        }

        .section-header p {
            font-size: 1rem;
            color: var(--muted);
            max-width: 700px;
            margin: 0 auto;
            font-weight: 300;
            line-height: 1.6;
        }

        .volunteer-content {
            display: flex;
            flex-direction: column;
            gap: 2.5rem;
        }

        .benefits-grid {
            display: grid;
            gap: 1.2rem;
        }

        .benefit-card {
            background: var(--white);
            padding: 1.5rem 1.2rem;
            border-radius: 15px;
            box-shadow: 0 12px 25px var(--shadow);
            transition: all 0.5s cubic-bezier(0.22, 0.61, 0.36, 1);
            border: 1px solid rgba(139, 94, 60, 0.1);
            position: relative;
            overflow: hidden;
            backdrop-filter: blur(10px);
        }

        .benefit-card::before {
            content: '';
            position: absolute;
            top: 0;
            right: 0;
            width: 5px;
            height: 100%;
            background: linear-gradient(180deg, var(--accent-pink), var(--accent-gold));
            transition: width 0.5s ease;
        }

        .benefit-card:hover {
            transform: translateY(-8px) scale(1.02);
            box-shadow: 0 15px 30px var(--shadow-strong);
        }

        .benefit-card:hover::before {
            width: 7px;
        }

        .benefit-card h4 {
            color: var(--primary-brown);
            margin-bottom: 0.6rem;
            font-size: 1.1rem;
            font-weight: 700;
        }

        .benefit-card p {
            color: var(--muted);
            line-height: 1.5;
            font-size: 0.9rem;
        }

        .volunteer-cta-container {
            position: relative;
        }

        .volunteer-notice {
            background: linear-gradient(135deg, #FFF9F4, #FFE8E8);
            border: 2px dashed var(--accent-pink);
            padding: 1.2rem;
            border-radius: 12px;
            margin-bottom: 1.5rem;
            text-align: center;
            box-shadow: 0 6px 15px rgba(232, 180, 184, 0.2);
            position: relative;
            overflow: hidden;
        }

        .volunteer-notice::before {
            content: '';
            position: absolute;
            top: -50%;
            right: -50%;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle, rgba(255,255,255,0.3) 0%, transparent 70%);
            animation: rotate 10s linear infinite;
        }

        .volunteer-notice h4 {
            color: var(--primary-brown);
            margin-bottom: 0.6rem;
            font-size: 1.1rem;
            position: relative;
            z-index: 1;
        }

        .volunteer-notice p {
            color: var(--muted);
            margin-bottom: 0.5rem;
            position: relative;
            z-index: 1;
            font-weight: 500;
            font-size: 0.85rem;
        }

        .volunteer-cta {
            background: linear-gradient(135deg, var(--primary-brown), #A07854);
            color: white;
            padding: 2rem 1.2rem;
            border-radius: 15px;
            text-align: center;
            box-shadow: 0 12px 25px rgba(139, 94, 60, 0.4);
            position: relative;
            overflow: hidden;
        }

        .volunteer-cta::before {
            content: '';
            position: absolute;
            top: -50%;
            right: -50%;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle, rgba(255,255,255,0.1) 0%, transparent 70%);
            animation: rotate 15s linear infinite;
        }

        .volunteer-cta h3 {
            font-size: 1.3rem;
            margin-bottom: 1rem;
            position: relative;
            z-index: 1;
        }

        .volunteer-cta p {
            color: rgba(255,255,255,0.9);
            margin-bottom: 1.2rem;
            position: relative;
            z-index: 1;
            font-size: 0.95rem;
            line-height: 1.5;
        }

        .volunteer-cta .btn {
            background: var(--white);
            color: var(--primary-brown);
            margin-top: 0.8rem;
            position: relative;
            z-index: 1;
            font-size: 0.95rem;
            padding: 0.8rem 1.5rem;
            max-width: 220px;
        }

        /* Enhanced Hanem Journal Section */
        .hanem-journal {
            padding: 4rem 0;
            background: linear-gradient(135deg, #F7EFE6 0%, #F8F4F0 50%, #FFF9F4 100%);
            position: relative;
            overflow: hidden;
            width: 100%;
        }

        .journal-background {
            position: absolute;
            top: 0;
            right: 0;
            width: 100%;
            height: 100%;
            opacity: 0.4;
            background: 
                radial-gradient(circle at 20% 20%, rgba(139, 94, 60, 0.1) 0%, transparent 50%),
                radial-gradient(circle at 80% 80%, rgba(232, 180, 184, 0.1) 0%, transparent 50%);
            background-size: 100px 100px;
            animation: floatBackground 25s ease-in-out infinite;
        }

        .journal-header {
            text-align: center;
            margin-bottom: 2.5rem;
            position: relative;
        }

        .journal-header h2 {
            font-family: 'Dancing Script', cursive;
            font-size: 2.5rem;
            color: var(--primary-brown);
            margin-bottom: 1rem;
            text-shadow: 0 4px 20px rgba(0,0,0,0.1);
            background: linear-gradient(135deg, var(--primary-brown), var(--accent-gold), var(--accent-pink));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            animation: shimmer 4s ease-in-out infinite;
        }

        .journal-header p {
            font-size: 1rem;
            color: var(--muted);
            max-width: 600px;
            margin: 0 auto;
            font-style: italic;
            font-weight: 300;
            line-height: 1.6;
        }

        /* Journal Tabs */
        .journal-tabs {
            display: flex;
            flex-direction: column;
            gap: 0.8rem;
            margin-bottom: 2.5rem;
            align-items: center;
        }

        .tab-btn {
            background: rgba(255, 255, 255, 0.8);
            border: 2px solid var(--accent-sand);
            padding: 0.8rem 1.5rem;
            border-radius: 50px;
            font-family: 'Cairo', sans-serif;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.5s cubic-bezier(0.22, 0.61, 0.36, 1);
            color: var(--text-dark);
            position: relative;
            overflow: hidden;
            box-shadow: 0 5px 12px rgba(0,0,0,0.1);
            backdrop-filter: blur(10px);
            width: 100%;
            max-width: 250px;
            font-size: 0.95rem;
        }

        .tab-btn::before {
            content: '';
            position: absolute;
            top: 0;
            right: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(135deg, var(--accent-pink), var(--accent-gold));
            opacity: 0;
            transition: opacity 0.5s ease;
            z-index: -1;
        }

        .tab-btn:hover, .tab-btn.active {
            color: var(--white);
            border-color: var(--accent-pink);
            transform: translateY(-3px) scale(1.02);
            box-shadow: 0 8px 20px rgba(232, 180, 184, 0.4);
        }

        .tab-btn:hover::before, .tab-btn.active::before {
            opacity: 1;
        }

        /* Tab Content */
        .tab-content {
            display: none;
        }

        .tab-content.active {
            display: block;
            animation: fadeInUp 1s ease;
        }

        @keyframes fadeInUp {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }

        /* Founders Corner */
        .founders-grid {
            display: grid;
            grid-template-columns: 1fr;
            gap: 1.5rem;
        }

        .founder-card {
            background: rgba(255, 255, 255, 0.9);
            padding: 1.5rem 1.2rem;
            border-radius: 15px;
            box-shadow: 0 12px 25px var(--shadow);
            position: relative;
            transition: transform 0.5s cubic-bezier(0.22, 0.61, 0.36, 1);
            border: 1px solid rgba(139, 94, 60, 0.1);
            overflow: hidden;
            backdrop-filter: blur(15px);
        }

        .founder-card::before {
            content: '';
            position: absolute;
            top: 0;
            right: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(135deg, transparent 60%, rgba(232, 180, 184, 0.08));
            z-index: 0;
        }

        .founder-card::after {
            content: '';
            position: absolute;
            top: 8px;
            right: 8px;
            bottom: 8px;
            left: 8px;
            border: 2px dashed var(--accent-pink);
            border-radius: 12px;
            pointer-events: none;
            opacity: 0.3;
        }

        .founder-card:hover {
            transform: translateY(-8px) scale(1.02);
            box-shadow: 0 20px 40px var(--shadow-strong);
        }

        .founder-card h3 {
            font-family: 'Playfair Display', serif;
            color: var(--primary-brown);
            margin-bottom: 1rem;
            font-size: 1.3rem;
            position: relative;
            z-index: 1;
        }

        .founder-card p {
            color: var(--muted);
            line-height: 1.5;
            position: relative;
            z-index: 1;
            font-size: 0.95rem;
        }

        /* Volunteers Section */
        .volunteers-section {
            position: relative;
        }

        .volunteers-carousel {
            display: flex;
            overflow-x: auto;
            gap: 1.2rem;
            padding: 1.5rem 0.8rem;
            scroll-behavior: smooth;
            scrollbar-width: none;
            -ms-overflow-style: none;
        }

        .volunteers-carousel::-webkit-scrollbar {
            display: none;
        }

        .volunteer-journal-card {
            flex: 0 0 85%;
            background: rgba(255, 255, 255, 0.9);
            border-radius: 15px;
            padding: 1.5rem 1.2rem;
            box-shadow: 0 12px 25px var(--shadow);
            transition: all 0.6s cubic-bezier(0.22, 0.61, 0.36, 1);
            position: relative;
            border: 1px solid rgba(139, 94, 60, 0.1);
            overflow: hidden;
            backdrop-filter: blur(15px);
        }

        .volunteer-journal-card::before {
            content: '';
            position: absolute;
            top: 0;
            right: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(135deg, transparent 40%, rgba(232, 180, 184, 0.08));
            z-index: 0;
        }

        .volunteer-journal-card::after {
            content: '';
            position: absolute;
            top: 12px;
            right: 12px;
            bottom: 12px;
            left: 12px;
            border: 2px dashed var(--accent-pink);
            border-radius: 12px;
            pointer-events: none;
            opacity: 0.3;
        }

        .volunteer-journal-card:hover {
            transform: translateY(-8px) scale(1.02);
            box-shadow: 0 20px 40px var(--shadow-strong);
        }

        .volunteer-image {
            width: 70px;
            height: 70px;
            border-radius: 50%;
            background: linear-gradient(135deg, var(--accent-sand), #F0DBC4);
            margin: 0 auto 1.2rem;
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--primary-brown);
            font-size: 1.8rem;
            position: relative;
            overflow: hidden;
            z-index: 1;
            box-shadow: 0 8px 20px rgba(0,0,0,0.15);
        }

        .volunteer-image::after {
            content: '';
            position: absolute;
            top: 0;
            right: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(135deg, transparent 60%, rgba(232, 180, 184, 0.3));
        }

        .volunteer-info {
            text-align: center;
            margin-bottom: 1.2rem;
            position: relative;
            z-index: 1;
        }

        .volunteer-name {
            font-weight: 700;
            color: var(--primary-brown);
            font-size: 1.2rem;
            margin-bottom: 0.4rem;
            font-family: 'Playfair Display', serif;
        }

        .volunteer-country {
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 0.4rem;
            color: var(--muted);
            font-size: 0.9rem;
        }

        .volunteer-quote {
            color: var(--text-dark);
            line-height: 1.5;
            position: relative;
            padding: 0 0.4rem;
            font-size: 0.95rem;
            z-index: 1;
        }

        .volunteer-quote::before {
            content: '"';
            font-size: 3rem;
            color: var(--accent-pink);
            position: absolute;
            top: -2rem;
            right: 0;
            opacity: 0.2;
            font-family: 'Playfair Display', serif;
            z-index: -1;
        }

        .carousel-nav {
            display: flex;
            justify-content: center;
            gap: 1.2rem;
            margin-top: 2rem;
        }

        .carousel-btn {
            width: 45px;
            height: 45px;
            border-radius: 50%;
            background: rgba(255, 255, 255, 0.9);
            border: 2px solid var(--accent-sand);
            display: flex;
            align-items: center;
            justify-content: center;
            cursor: pointer;
            transition: all 0.4s cubic-bezier(0.22, 0.61, 0.36, 1);
            color: var(--primary-brown);
            box-shadow: 0 5px 12px rgba(0,0,0,0.15);
            backdrop-filter: blur(10px);
        }

        .carousel-btn:hover {
            background: var(--accent-pink);
            color: var(--white);
            border-color: var(--accent-pink);
            transform: scale(1.08);
            box-shadow: 0 6px 15px rgba(232, 180, 184, 0.4);
        }

        /* Women Stories Section */
        .women-stories {
            text-align: center;
            padding: 3rem 1.2rem;
            background: linear-gradient(135deg, rgba(255,255,255,0.9) 0%, rgba(248, 244, 240, 0.9) 100%);
            border-radius: 15px;
            margin: 1.2rem auto;
            max-width: 1000px;
            box-shadow: 0 12px 25px var(--shadow);
            position: relative;
            overflow: hidden;
        }

        .women-stories::before {
            content: '';
            position: absolute;
            top: 0;
            right: 0;
            width: 100%;
            height: 100%;
            background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100"><path d="M30,30 Q50,10 70,30 T90,30" stroke="%238B5E3C" fill="none" stroke-width="1" opacity="0.05"/></svg>');
            background-size: 200px 200px;
        }

        .women-stories h3 {
            font-family: 'Playfair Display', serif;
            font-size: 1.5rem;
            color: var(--primary-brown);
            margin-bottom: 1rem;
        }

        .women-stories p {
            font-size: 1rem;
            color: var(--muted);
            max-width: 600px;
            margin: 0 auto;
            line-height: 1.5;
        }

        /* Share Button */
        .share-story {
            text-align: center;
            margin-top: 2.5rem;
        }

        .share-btn {
            background: linear-gradient(135deg, var(--accent-pink), var(--primary-brown));
            color: var(--white);
            border: none;
            padding: 1rem 2rem;
            border-radius: 50px;
            font-family: 'Cairo', sans-serif;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.5s cubic-bezier(0.22, 0.61, 0.36, 1);
            display: inline-flex;
            align-items: center;
            gap: 0.8rem;
            box-shadow: 0 8px 20px rgba(232, 180, 184, 0.5);
            font-size: 1rem;
            backdrop-filter: blur(10px);
        }

        .share-btn:hover {
            transform: translateY(-5px) scale(1.03);
            box-shadow: 0 12px 25px rgba(232, 180, 184, 0.6);
        }

        /* Mobile Menu */
        .mobile-menu {
            position: fixed;
            top: 0;
            right: -100%;
            width: 80%;
            height: 100vh;
            background: rgba(255, 255, 255, 0.98);
            backdrop-filter: blur(20px);
            z-index: 999;
            transition: right 0.4s cubic-bezier(0.22, 0.61, 0.36, 1);
            padding: 5rem 1.5rem 2rem;
            display: flex;
            flex-direction: column;
            gap: 1.5rem;
            box-shadow: -5px 0 25px rgba(0,0,0,0.1);
        }

        .mobile-menu.active {
            right: 0;
        }

        .mobile-menu a {
            text-decoration: none;
            color: var(--text-dark);
            font-weight: 600;
            font-size: 1.1rem;
            padding: 1rem 0;
            border-bottom: 1px solid rgba(139, 94, 60, 0.1);
            transition: all 0.3s ease;
        }

        .mobile-menu a:hover {
            color: var(--primary-brown);
            transform: translateX(-8px);
        }

        .menu-overlay {
            position: fixed;
            top: 0;
            right: 0;
            width: 100%;
            height: 100%;
            background: rgba(0,0,0,0.5);
            z-index: 998;
            opacity: 0;
            visibility: hidden;
            transition: all 0.3s ease;
        }

        .menu-overlay.active {
            opacity: 1;
            visibility: visible;
        }

        /* Responsive Design */
        @media (min-width: 768px) {
            .container {
                padding: 0 1.5rem;
            }
            
            .hero {
                padding: 70px 0 3rem;
            }
            
            .hero h1 {
                font-size: 2.8rem;
            }
            
            .hero p {
                font-size: 1.2rem;
            }
            
            .hero-stats {
                grid-template-columns: repeat(4, 1fr);
                gap: 1.5rem;
                max-width: 1000px;
            }
            
            .stat {
                padding: 1.5rem 1rem;
            }
            
            .stat-number {
                font-size: 2.2rem;
            }
            
            .stat-label {
                font-size: 0.9rem;
            }
            
            .cta-buttons {
                flex-direction: row;
                gap: 1.5rem;
            }
            
            .btn {
                width: auto;
                max-width: none;
            }
            
            .volunteer-content {
                flex-direction: row;
                gap: 3rem;
            }
            
            .benefits-grid {
                grid-template-columns: 1fr;
            }
            
            .journal-tabs {
                flex-direction: row;
                gap: 1.2rem;
            }
            
            .tab-btn {
                width: auto;
            }
            
            .founders-grid {
                grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            }
            
            .volunteer-journal-card {
                flex: 0 0 350px;
            }
        }

        @media (min-width: 1024px) {
            .hero h1 {
                font-size: 3.5rem;
            }
            
            .hero p {
                font-size: 1.4rem;
            }
            
            .section-header h2 {
                font-size: 2.5rem;
            }
            
            .journal-header h2 {
                font-size: 3.5rem;
            }
            
            .volunteer-journal-card {
                flex: 0 0 400px;
                padding: 2rem 1.5rem;
            }
            
            .benefits-grid {
                grid-template-columns: 1fr;
            }
            
            .founders-grid {
                grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            }
        }

        @media (max-width: 767px) {
            .desktop-nav {
                display: none;
            }
            
            .mobile-nav-toggle {
                display: block;
            }
            
            .header-content {
                padding: 0 0.3rem;
            }
            
            .logo-text {
                font-size: 1.2rem;
            }
            
            .language-toggle {
                padding: 0.3rem 0.6rem;
                font-size: 0.8rem;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header id="main-header">
        <div class="container">
            <div class="header-content">
                <a href="#home" class="logo">
                    <svg class="logo-svg" viewBox="0 0 100 100">
                        <path class="logo-path" d="M30,30 Q50,10 70,30 T90,30 M30,50 Q50,30 70,50 T90,50 M30,70 Q50,50 70,70 T90,70" fill="none"/>
                    </svg>
                    <span class="logo-text">رزق الهانم</span>
                </a>
                
                <!-- Desktop Navigation -->
                <nav class="desktop-nav">
                    <a href="#home">الرئيسية</a>
                    <a href="#volunteer">التطوع</a>
                    <a href="#hanem-journal">Hanem Journal</a>
                    <a href="#contact">اتصل بنا</a>
                </nav>
                
                <div class="header-actions">
                    <button class="language-toggle" id="language-toggle">
                        <span>EN</span>
                    </button>
                    <button class="mobile-nav-toggle" id="mobile-nav-toggle">
                        <i class="fas fa-bars"></i>
                    </button>
                </div>
            </div>
        </div>
    </header>

    <!-- Mobile Menu -->
    <div class="mobile-menu" id="mobile-menu">
        <a href="#home">الرئيسية</a>
        <a href="#volunteer">التطوع</a>
        <a href="#hanem-journal">Hanem Journal</a>
        <a href="#contact">اتصل بنا</a>
    </div>
    <div class="menu-overlay" id="menu-overlay"></div>

    <!-- Ultimate Hero Section -->
    <section class="hero" id="home">
        <div class="hero-background"></div>
        <div class="hero-particles" id="particles-container"></div>
        <div class="container">
            <div class="hero-content">
                <h1>رزق الهانم — تحويل الملابس المتبرع بها إلى سبل عيش مستدامة</h1>
                <p>نحن ندرب النساء في ريف مصر على إعادة تدوير المنسوجات وكسب دخل ثابت. انضم إلينا في رحلة صنع التغيير - تبرع، تطوع، أو كن شريكًا في تمكين المرأة.</p>
                
                <div class="hero-stats">
                    <div class="stat">
                        <span class="stat-number" id="volunteers-count">0</span>
                        <span class="stat-label">متطوع مناصر للتغيير</span>
                    </div>
                    <div class="stat">
                        <span class="stat-number" id="items-count">0</span>
                        <span class="stat-label">قطعة ملابس أعيد تدويرها</span>
                    </div>
                    <div class="stat">
                        <span class="stat-number" id="women-count">0</span>
                        <span class="stat-label">امرأة مدربة وتمكينت</span>
                    </div>
                    <div class="stat">
                        <span class="stat-number" id="workshops-count">0</span>
                        <span class="stat-label">ورشة تمكين واحترافية</span>
                    </div>
                </div>
                
                <div class="cta-buttons">
                    <a href="#volunteer" class="btn btn-primary">
                        <i class="fas fa-hands-helping"></i>
                        انضم إلينا كمتطوع
                    </a>
                    <a href="#donate" class="btn btn-secondary btn-disabled">
                        <i class="fas fa-heart"></i>
                        ادعم رحلتنا بالتبرع
                    </a>
                </div>
                
                <p class="hero-micro">بدأنا رحلتنا في أغسطس 2025 · 100+ متطوع ملهم · 100+ قصة نجاح</p>
            </div>
        </div>
    </section>

    <!-- Volunteer Section -->
    <section class="volunteer" id="volunteer">
        <div class="container">
            <div class="section-header">
                <h2>التطوع — كن خيطًا في نسيج التغيير</h2>
                <p>ساعد في توسيع نطاق الحل المحلي: اعمل مع النساء الريفيات، وصمم الحملات، وادير ورش العمل، أو ادعم العمليات اللوجستية. لا توجد خبرة مطلوبة - فقط الالتزام والشغف لصنع الفرق.</p>
            </div>
            
            <div class="volunteer-content">
                <div>
                    <h3 style="margin-bottom: 1.5rem; color: var(--primary-brown);">ماذا تقدم لك رحلة التطوع معنا؟</h3>
                    <div class="benefits-grid">
                        <div class="benefit-card">
                            <h4>شهادة مشاركة معتمدة</h4>
                            <p>بعد إكمال 4 مهام تطوعية، تحصل على شهادة معتمدة تثبت مساهمتك في تمكين المرأة</p>
                        </div>
                        <div class="benefit-card">
                            <h4>خطاب توصية شخصي</h4>
                            <p>بعد إكمال 8+ مهام، نمنحك خطاب توصية مفصل يعزز سيرتك الذاتية</p>
                        </div>
                        <div class="benefit-card">
                            <h4>ورش عمل احترافية</h4>
                            <p>جلسات تطوير مهارات قيادية وإدارية مع مختصين في المجال</p>
                        </div>
                        <div class="benefit-card">
                            <h4>أولوية المشاركة</h4>
                            <p>وصول مسبق وحصري للفعاليات والأنشطة والفرص القيادية</p>
                        </div>
                        <div class="benefit-card">
                            <h4>شارة رقمية مميزة</h4>
                            <p>شارة رقمية لعرضها على لينكد إن ومنصات التواصل المهنية</p>
                        </div>
                    </div>
                </div>
                
                <div class="volunteer-cta-container">
                    <div class="volunteer-notice">
                        <h4>ملاحظة هامة</h4>
                        <p>التطوع مفتوح حالياً لمحرري الفيديو فقط</p>
                        <p>سيتم فتح باب التطوع لجميع المجالات قريباً جداً</p>
                        <p>سيغلق باب التطوع لمحرري الفيديو فور اكتمال العدد المطلوب</p>
                    </div>
                    
                    <div class="volunteer-cta">
                        <h3>مستعد لبدء رحلتك التطوعية؟</h3>
                        <p>انضم إلى عائلة رزق الهانم وكن جزءاً من التغيير</p>
                        <a href="https://docs.google.com/forms/d/e/1FAIpQLScTvPe_V0Za6NQE1msuLLszegdj5xYxPsNrvnsxfqPyeUo0rQ/viewform?usp=header" 
                           class="btn" target="_blank">
                            <i class="fas fa-rocket"></i>
                            ابدأ رحلتك الآن
                        </a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Enhanced Hanem Journal Section -->
    <section class="hanem-journal" id="hanem-journal">
        <div class="journal-background"></div>
        <div class="container">
            <div class="journal-header">
                <h2>Hanem Journal</h2>
                <p>قصص وإلهامات من رحلة رزق الهانم - حيث تلتقي القلوب بالحرف وتتحول الأحلام إلى واقع</p>
            </div>
            
            <div class="journal-tabs">
                <button class="tab-btn active" data-tab="founders">ركن المؤسسين</button>
                <button class="tab-btn" data-tab="volunteers">أصوات المتطوعين</button>
                <button class="tab-btn" data-tab="stories">قصص الملهمات</button>
            </div>
            
            <!-- Founders Corner -->
            <div class="tab-content active" id="founders">
                <div class="founders-grid">
                    <div class="founder-card">
                        <h3>بداية الحلم</h3>
                        <p>كل شيء بدأ بكلمات بسيطة: "لا أريد ملابس، أريد عملاً". هذه الجملة غيرت مسار حياتنا وألهمتنا لخلق رزق الهانم. من خلال إعادة تدوير الملابس، لم نخلق فرص عمل فحسب، بل بنينا مجتمعاً من النساء القويات اللواتي يخلقن مستقبلاً أفضل لأنفسهن وعائلاتهن.</p>
                    </div>
                    <div class="founder-card">
                        <h3>رحلة الإيمان</h3>
                        <p>في كل زيارة قرية، نرى الأمل يتجدد في عيون النساء. التحول من الشعور بالعجز إلى الإحساس بالتمكين هو أجمل ما في رحلتنا. كل قطعة قماش نعيد تدويرها تحمل قصة، وكل امرأة نتدربها تروي حكاية جديدة من التحدي إلى النجاح.</p>
                    </div>
                    <div class="founder-card">
                        <h3>خيوط الأمل</h3>
                        <p>قريباً سنشارككم قصة تأسيس رزق الهانم بالتفصيل - من الفكرة الأولى إلى الواقع الملموس. كيف تحول حلم بسيط إلى حركة إيجابية تمس حياة المئات من النساء والمتطوعين. تابعونا لمعرفة المزيد عن رحلتنا الملهمة.</p>
                    </div>
                </div>
            </div>
            
            <!-- Volunteers' Voices -->
            <div class="tab-content" id="volunteers">
                <div class="volunteers-section">
                    <div class="volunteers-carousel" id="volunteersCarousel">
                        <!-- Volunteer 1 -->
                        <div class="volunteer-journal-card">
                            <div class="volunteer-image">
                                <i class="fas fa-user"></i>
                            </div>
                            <div class="volunteer-info">
                                <div class="volunteer-name">صفاء</div>
                                <div class="volunteer-country">
                                    <i class="fas fa-map-marker-alt"></i>
                                    المغرب
                                </div>
                            </div>
                            <div class="volunteer-quote">
                                التجربة تاعي في رزق الهانم كانت واعرة بزاف عجباتي الفكرة تاع المشروع او الخدمة تاع الفريق، او اكتر حاجة عجباتني هيا خدمتي او كيفاش كنت تنشر فكرة المشروع تاعنا باش نعاونو ناس كتر. تعلمت مهارات الحوار او العمل في مجموعات او انني نكون في الوقت. كنشجع الناس بزاف على انها تتطوع فهاد المشروع الزوين او تتعلم حاجات بزاف منو لي غادي تنفعها فحياتها الاكاديمية او المهنية او كنوعدكم انكم ماغاديش تندمو عليه.
                            </div>
                        </div>
                        
                        <!-- Volunteer 2 -->
                        <div class="volunteer-journal-card">
                            <div class="volunteer-image">
                                <i class="fas fa-user"></i>
                            </div>
                            <div class="volunteer-info">
                                <div class="volunteer-name">Amr Khattab</div>
                                <div class="volunteer-country">
                                    <i class="fas fa-map-marker-alt"></i>
                                    مصر
                                </div>
                            </div>
                            <div class="volunteer-quote">
                                I had an amazing experience. I really love to use my skills as a graphic designer to help people in need. The most valuable lesson I learned was teamwork and how to organize my work and I also learned that time management is very important and that I have to deal with my tasks in an organized way. I would certainly recommend others to join this experience to learn these lessons.
                            </div>
                        </div>
                        
                        <!-- Volunteer 3 -->
                        <div class="volunteer-journal-card">
                            <div class="volunteer-image">
                                <i class="fas fa-user"></i>
                            </div>
                            <div class="volunteer-info">
                                <div class="volunteer-name">Zeina Mohamed</div>
                                <div class="volunteer-country">
                                    <i class="fas fa-map-marker-alt"></i>
                                    مصر
                                </div>
                            </div>
                            <div class="volunteer-quote">
                                Actually, it was my first time going through this experience, and it was a really wonderful one. I enjoyed it a lot, and for sure I will recommend it to others.
                            </div>
                        </div>
                    </div>
                    
                    <div class="carousel-nav">
                        <button class="carousel-btn" id="prevBtn">
                            <i class="fas fa-chevron-right"></i>
                        </button>
                        <button class="carousel-btn" id="nextBtn">
                            <i class="fas fa-chevron-left"></i>
                        </button>
                    </div>
                </div>
            </div>
            
            <!-- Women Stories Section -->
            <div class="tab-content" id="stories">
                <div class="women-stories">
                    <h3>قصص الملهمات</h3>
                    <p>قريباً سنشارككم قصص النساء الملهمات اللواتي تغيرت حياتهن بفضل رزق الهانم. قصص من الكفاح إلى النجاح، ومن التحدي إلى التمكين.</p>
                    <p style="margin-top: 1.2rem; font-style: italic; color: var(--primary-brown);">
                        "من حلم بسيط إلى واقع ملموس، ننسج معاً قصة تمكين لا تنتهي"
                    </p>
                </div>
            </div>
            
            <div class="share-story">
                <button class="share-btn">
                    <i class="fas fa-share-alt"></i>
                    شارك قصتك معنا
                </button>
            </div>
        </div>
    </section>

    <script>
        // Create floating particles
        function createParticles() {
            const container = document.getElementById('particles-container');
            const particleCount = 25;
            
            for (let i = 0; i < particleCount; i++) {
                const particle = document.createElement('div');
                particle.className = 'particle';
                
                // Random properties
                const size = Math.random() * 5 + 2;
                const posX = Math.random() * 100;
                const delay = Math.random() * 15;
                const duration = Math.random() * 10 + 15;
                
                particle.style.width = `${size}px`;
                particle.style.height = `${size}px`;
                particle.style.right = `${posX}%`;
                particle.style.animationDelay = `${delay}s`;
                particle.style.animationDuration = `${duration}s`;
                
                container.appendChild(particle);
            }
        }

        // Counter Animation
        function animateCounter(element, target, duration = 1500) {
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

        // Initialize counters
        function initCounters() {
            animateCounter(document.getElementById('volunteers-count'), 100);
            animateCounter(document.getElementById('items-count'), 100);
            animateCounter(document.getElementById('women-count'), 10);
            animateCounter(document.getElementById('workshops-count'), 1);
        }

        // Header scroll effect
        function handleHeaderScroll() {
            const header = document.getElementById('main-header');
            if (window.scrollY > 50) {
                header.classList.add('scrolled');
            } else {
                header.classList.remove('scrolled');
            }
        }

        // Tab functionality
        const tabBtns = document.querySelectorAll('.tab-btn');
        const tabContents = document.querySelectorAll('.tab-content');
        
        tabBtns.forEach(btn => {
            btn.addEventListener('click', () => {
                // Remove active class from all buttons and contents
                tabBtns.forEach(b => b.classList.remove('active'));
                tabContents.forEach(c => c.classList.remove('active'));
                
                // Add active class to clicked button
                btn.classList.add('active');
                
                // Show corresponding content
                const tabId = btn.getAttribute('data-tab');
                document.getElementById(tabId).classList.add('active');
            });
        });
        
        // Carousel functionality
        const carousel = document.getElementById('volunteersCarousel');
        const prevBtn = document.getElementById('prevBtn');
        const nextBtn = document.getElementById('nextBtn');
        
        if (carousel && prevBtn && nextBtn) {
            nextBtn.addEventListener('click', () => {
                carousel.scrollBy({ left: 250, behavior: 'smooth' });
            });
            
            prevBtn.addEventListener('click', () => {
                carousel.scrollBy({ left: -250, behavior: 'smooth' });
            });
        }
        
        // Mobile menu functionality
        const mobileNavToggle = document.getElementById('mobile-nav-toggle');
        const mobileMenu = document.getElementById('mobile-menu');
        const menuOverlay = document.getElementById('menu-overlay');
        
        if (mobileNavToggle && mobileMenu && menuOverlay) {
            mobileNavToggle.addEventListener('click', () => {
                mobileMenu.classList.add('active');
                menuOverlay.classList.add('active');
                document.body.style.overflow = 'hidden';
            });
            
            menuOverlay.addEventListener('click', () => {
                mobileMenu.classList.remove('active');
                menuOverlay.classList.remove('active');
                document.body.style.overflow = '';
            });
            
            // Close menu when clicking on a link
            const mobileMenuLinks = mobileMenu.querySelectorAll('a');
            mobileMenuLinks.forEach(link => {
                link.addEventListener('click', () => {
                    mobileMenu.classList.remove('active');
                    menuOverlay.classList.remove('active');
                    document.body.style.overflow = '';
                });
            });
        }
        
        // Language toggle with full translation
        document.getElementById('language-toggle').addEventListener('click', function() {
            const body = document.body;
            const isArabic = body.getAttribute('dir') === 'rtl';
            
            if (isArabic) {
                // Switch to English
                body.setAttribute('dir', 'ltr');
                body.setAttribute('lang', 'en');
                this.innerHTML = '<span>AR</span>';
                
                // Update all text content to English
                document.querySelector('.logo-text').textContent = 'Rezq El Hanem';
                document.querySelector('.hero h1').textContent = 'Rezq El Hanem — Turning donated clothes into sustainable livelihoods';
                document.querySelector('.hero p').textContent = 'We train women in rural Egypt to upcycle textiles and earn steady income. Join us in our journey of making change - donate, volunteer, or partner in women empowerment.';
                document.querySelector('.hero-micro').textContent = 'Started our journey in August 2025 · 100+ inspiring volunteers · 100+ success stories';
                
                // Update navigation
                const navLinks = document.querySelectorAll('.desktop-nav a, .mobile-menu a');
                navLinks[0].textContent = 'Home';
                navLinks[1].textContent = 'Volunteer';
                navLinks[2].textContent = 'Hanem Journal';
                navLinks[3].textContent = 'Contact Us';
                
                // Update volunteer section
                document.querySelector('.section-header h2').textContent = 'Volunteering — Be a thread in the fabric of change';
                document.querySelector('.section-header p').textContent = 'Help scale the local solution: work with rural women, design campaigns, manage workshops, or support logistics. No experience required - just commitment and passion to make a difference.';
                document.querySelector('.volunteer-content h3').textContent = 'What does volunteering with us offer you?';
                
                // Update benefit cards
                const benefitCards = document.querySelectorAll('.benefit-card');
                benefitCards[0].querySelector('h4').textContent = 'Certified Participation Certificate';
                benefitCards[0].querySelector('p').textContent = 'After completing 4 volunteer tasks, you receive a certified certificate proving your contribution to women empowerment';
                benefitCards[1].querySelector('h4').textContent = 'Personal Recommendation Letter';
                benefitCards[1].querySelector('p').textContent = 'After completing 8+ tasks, we provide you with a detailed recommendation letter that enhances your CV';
                benefitCards[2].querySelector('h4').textContent = 'Professional Workshops';
                benefitCards[2].querySelector('p').textContent = 'Leadership and management skills development sessions with specialists in the field';
                benefitCards[3].querySelector('h4').textContent = 'Priority Participation';
                benefitCards[3].querySelector('p').textContent = 'Early and exclusive access to events, activities, and leadership opportunities';
                benefitCards[4].querySelector('h4').textContent = 'Distinctive Digital Badge';
                benefitCards[4].querySelector('p').textContent = 'Digital badge to display on LinkedIn and professional networking platforms';
                
                // Update volunteer notice
                document.querySelector('.volunteer-notice h4').textContent = 'Important Note';
                const noticeParagraphs = document.querySelectorAll('.volunteer-notice p');
                noticeParagraphs[0].textContent = 'Volunteering is currently open for video editors only';
                noticeParagraphs[1].textContent = 'Volunteering for all fields will open very soon';
                noticeParagraphs[2].textContent = 'Volunteering for video editors will close once the required number is completed';
                
                // Update volunteer CTA
                document.querySelector('.volunteer-cta h3').textContent = 'Ready to start your volunteering journey?';
                document.querySelector('.volunteer-cta p').textContent = 'Join the Rezq El Hanem family and be part of the change';
                document.querySelector('.volunteer-cta .btn').innerHTML = '<i class="fas fa-rocket"></i> Start Your Journey Now';
                
                // Update CTA buttons
                const ctaButtons = document.querySelectorAll('.cta-buttons .btn');
                ctaButtons[0].innerHTML = '<i class="fas fa-hands-helping"></i> Join Us as a Volunteer';
                ctaButtons[1].innerHTML = '<i class="fas fa-heart"></i> Support Our Journey by Donating';
                
                // Update stat labels
                const statLabels = document.querySelectorAll('.stat-label');
                statLabels[0].textContent = 'Volunteers Advocating for Change';
                statLabels[1].textContent = 'Clothing Items Upcycled';
                statLabels[2].textContent = 'Women Trained and Empowered';
                statLabels[3].textContent = 'Empowerment and Professional Workshops';
                
                // Update Hanem Journal
                document.querySelector('.journal-header h2').textContent = 'Hanem Journal';
                document.querySelector('.journal-header p').textContent = 'Stories and inspirations from the Rezq El Hanem journey - where hearts meet craftsmanship and dreams become reality';
                
                // Update tab buttons
                const tabButtons = document.querySelectorAll('.tab-btn');
                tabButtons[0].textContent = 'Founders Corner';
                tabButtons[1].textContent = 'Volunteers Voices';
                tabButtons[2].textContent = 'Inspiring Stories';
                
                // Update founders section
                const founderCards = document.querySelectorAll('.founder-card');
                founderCards[0].querySelector('h3').textContent = 'The Beginning of the Dream';
                founderCards[0].querySelector('p').textContent = 'Everything started with simple words: "I don\'t want clothes, I want work." This sentence changed the course of our lives and inspired us to create Rezq El Hanem. Through upcycling clothes, we not only created job opportunities but built a community of strong women who create a better future for themselves and their families.';
                founderCards[1].querySelector('h3').textContent = 'Journey of Faith';
                founderCards[1].querySelector('p').textContent = 'In every village visit, we see hope renewed in the eyes of women. The transformation from feeling helpless to feeling empowered is the most beautiful part of our journey. Every piece of fabric we upcycle carries a story, and every woman we train tells a new tale from challenge to success.';
                founderCards[2].querySelector('h3').textContent = 'Threads of Hope';
                founderCards[2].querySelector('p').textContent = 'Soon we will share with you the detailed story of the founding of Rezq El Hanem - from the first idea to tangible reality. How a simple dream turned into a positive movement touching the lives of hundreds of women and volunteers. Follow us to learn more about our inspiring journey.';
                
                // Update women stories section
                document.querySelector('.women-stories h3').textContent = 'Inspiring Stories';
                document.querySelector('.women-stories p').textContent = 'Soon we will share with you the inspiring stories of women whose lives have changed thanks to Rezq El Hanem. Stories from struggle to success, from challenge to empowerment.';
                document.querySelector('.women-stories p:nth-child(3)').textContent = '"From a simple dream to tangible reality, we weave together an endless story of empowerment"';
                
                // Update share button
                document.querySelector('.share-btn').innerHTML = '<i class="fas fa-share-alt"></i> Share Your Story With Us';
                
            } else {
                // Switch to Arabic
                body.setAttribute('dir', 'rtl');
                body.setAttribute('lang', 'ar');
                this.innerHTML = '<span>EN</span>';
                
                // Update all text content to Arabic
                document.querySelector('.logo-text').textContent = 'رزق الهانم';
                document.querySelector('.hero h1').textContent = 'رزق الهانم — تحويل الملابس المتبرع بها إلى سبل عيش مستدامة';
                document.querySelector('.hero p').textContent = 'نحن ندرب النساء في ريف مصر على إعادة تدوير المنسوجات وكسب دخل ثابت. انضم إلينا في رحلة صنع التغيير - تبرع، تطوع، أو كن شريكًا في تمكين المرأة.';
                document.querySelector('.hero-micro').textContent = 'بدأنا رحلتنا في أغسطس 2025 · 100+ متطوع ملهم · 100+ قصة نجاح';
                
                // Update navigation
                const navLinks = document.querySelectorAll('.desktop-nav a, .mobile-menu a');
                navLinks[0].textContent = 'الرئيسية';
                navLinks[1].textContent = 'التطوع';
                navLinks[2].textContent = 'Hanem Journal';
                navLinks[3].textContent = 'اتصل بنا';
                
                // Update volunteer section
                document.querySelector('.section-header h2').textContent = 'التطوع — كن خيطًا في نسيج التغيير';
                document.querySelector('.section-header p').textContent = 'ساعد في توسيع نطاق الحل المحلي: اعمل مع النساء الريفيات، وصمم الحملات، وادير ورش العمل، أو ادعم العمليات اللوجستية. لا توجد خبرة مطلوبة - فقط الالتزام والشغف لصنع الفرق.';
                document.querySelector('.volunteer-content h3').textContent = 'ماذا تقدم لك رحلة التطوع معنا؟';
                
                // Update benefit cards
                const benefitCards = document.querySelectorAll('.benefit-card');
                benefitCards[0].querySelector('h4').textContent = 'شهادة مشاركة معتمدة';
                benefitCards[0].querySelector('p').textContent = 'بعد إكمال 4 مهام تطوعية، تحصل على شهادة معتمدة تثبت مساهمتك في تمكين المرأة';
                benefitCards[1].querySelector('h4').textContent = 'خطاب توصية شخصي';
                benefitCards[1].querySelector('p').textContent = 'بعد إكمال 8+ مهام، نمنحك خطاب توصية مفصل يعزز سيرتك الذاتية';
                benefitCards[2].querySelector('h4').textContent = 'ورش عمل احترافية';
                benefitCards[2].querySelector('p').textContent = 'جلسات تطوير مهارات قيادية وإدارية مع مختصين في المجال';
                benefitCards[3].querySelector('h4').textContent = 'أولوية المشاركة';
                benefitCards[3].querySelector('p').textContent = 'وصول مسبق وحصري للفعاليات والأنشطة والفرص القيادية';
                benefitCards[4].querySelector('h4').textContent = 'شارة رقمية مميزة';
                benefitCards[4].querySelector('p').textContent = 'شارة رقمية لعرضها على لينكد إن ومنصات التواصل المهنية';
                
                // Update volunteer notice
                document.querySelector('.volunteer-notice h4').textContent = 'ملاحظة هامة';
                const noticeParagraphs = document.querySelectorAll('.volunteer-notice p');
                noticeParagraphs[0].textContent = 'التطوع مفتوح حالياً لمحرري الفيديو فقط';
                noticeParagraphs[1].textContent = 'سيتم فتح باب التطوع لجميع المجالات قريباً جداً';
                noticeParagraphs[2].textContent = 'سيغلق باب التطوع لمحرري الفيديو فور اكتمال العدد المطلوب';
                
                // Update volunteer CTA
                document.querySelector('.volunteer-cta h3').textContent = 'مستعد لبدء رحلتك التطوعية؟';
                document.querySelector('.volunteer-cta p').textContent = 'انضم إلى عائلة رزق الهانم وكن جزءاً من التغيير';
                document.querySelector('.volunteer-cta .btn').innerHTML = '<i class="fas fa-rocket"></i> ابدأ رحلتك الآن';
                
                // Update CTA buttons
                const ctaButtons = document.querySelectorAll('.cta-buttons .btn');
                ctaButtons[0].innerHTML = '<i class="fas fa-hands-helping"></i> انضم إلينا كمتطوع';
                ctaButtons[1].innerHTML = '<i class="fas fa-heart"></i> ادعم رحلتنا بالتبرع';
                
                // Update stat labels
                const statLabels = document.querySelectorAll('.stat-label');
                statLabels[0].textContent = 'متطوع مناصر للتغيير';
                statLabels[1].textContent = 'قطعة ملابس أعيد تدويرها';
                statLabels[2].textContent = 'امرأة مدربة وتمكينت';
                statLabels[3].textContent = 'ورشة تمكين واحترافية';
                
                // Update Hanem Journal
                document.querySelector('.journal-header h2').textContent = 'Hanem Journal';
                document.querySelector('.journal-header p').textContent = 'قصص وإلهامات من رحلة رزق الهانم - حيث تلتقي القلوب بالحرف وتتحول الأحلام إلى واقع';
                
                // Update tab buttons
                const tabButtons = document.querySelectorAll('.tab-btn');
                tabButtons[0].textContent = 'ركن المؤسسين';
                tabButtons[1].textContent = 'أصوات المتطوعين';
                tabButtons[2].textContent = 'قصص الملهمات';
                
                // Update founders section
                const founderCards = document.querySelectorAll('.founder-card');
                founderCards[0].querySelector('h3').textContent = 'بداية الحلم';
                founderCards[0].querySelector('p').textContent = 'كل شيء بدأ بكلمات بسيطة: "لا أريد ملابس، أريد عملاً". هذه الجملة غيرت مسار حياتنا وألهمتنا لخلق رزق الهانم. من خلال إعادة تدوير الملابس، لم نخلق فرص عمل فحسب، بل بنينا مجتمعاً من النساء القويات اللواتي يخلقن مستقبلاً أفضل لأنفسهن وعائلاتهن.';
                founderCards[1].querySelector('h3').textContent = 'رحلة الإيمان';
                founderCards[1].querySelector('p').textContent = 'في كل زيارة قرية، نرى الأمل يتجدد في عيون النساء. التحول من الشعور بالعجز إلى الإحساس بالتمكين هو أجمل ما في رحلتنا. كل قطعة قماش نعيد تدويرها تحمل قصة، وكل امرأة نتدربها تروي حكاية جديدة من التحدي إلى النجاح.';
                founderCards[2].querySelector('h3').textContent = 'خيوط الأمل';
                founderCards[2].querySelector('p').textContent = 'قريباً سنشارككم قصة تأسيس رزق الهانم بالتفصيل - من الفكرة الأولى إلى الواقع الملموس. كيف تحول حلم بسيط إلى حركة إيجابية تمس حياة المئات من النساء والمتطوعين. تابعونا لمعرفة المزيد عن رحلتنا الملهمة.';
                
                // Update women stories section
                document.querySelector('.women-stories h3').textContent = 'قصص الملهمات';
                document.querySelector('.women-stories p').textContent = 'قريباً سنشارككم قصص النساء الملهمات اللواتي تغيرت حياتهن بفضل رزق الهانم. قصص من الكفاح إلى النجاح، ومن التحدي إلى التمكين.';
                document.querySelector('.women-stories p:nth-child(3)').textContent = '"من حلم بسيط إلى واقع ملموس، ننسج معاً قصة تمكين لا تنتهي"';
                
                // Update share button
                document.querySelector('.share-btn').innerHTML = '<i class="fas fa-share-alt"></i> شارك قصتك معنا';
            }
        });
        
        // Initialize on load
        document.addEventListener('DOMContentLoaded', function() {
            createParticles();
            initCounters();
            
            // Header scroll effect
            window.addEventListener('scroll', handleHeaderScroll);
            handleHeaderScroll(); // Initial check
            
            // Disable donation buttons
            document.querySelectorAll('.btn-disabled').forEach(btn => {
                btn.addEventListener('click', (e) => e.preventDefault());
            });
            
            // Share button functionality
            const shareBtn = document.querySelector('.share-btn');
            shareBtn.addEventListener('click', () => {
                alert('سيتم توجيهك إلى نموذج مشاركة القصص قريباً!');
            });
        });
    </script>
</body>
</html>
