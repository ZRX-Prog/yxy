<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ZRX有限公司 - 高端家具生产与定制</title>
    <meta name="description" content="ZRX有限公司专注高品质家具研发、生产与销售，提供全屋家具定制服务。">
    <style>
        /* ============ CSS Reset & Variables ============ */
        :root {
            --wood-dark: #4A3728;
            --wood-mid: #6B4C3B;
            --wood-light: #8B6914;
            --cream: #F5F0E8;
            --warm-bg: #FAF7F2;
            --accent: #C8974A;
            --accent-hover: #A67B3D;
            --text-dark: #2C2416;
            --text-mid: #5C5348;
            --text-light: #8C8276;
            --white: #FFFFFF;
            --border: #E0D8CC;
            --shadow-sm: 0 2px 8px rgba(74, 55, 40, 0.08);
            --shadow-md: 0 4px 20px rgba(74, 55, 40, 0.12);
            --shadow-lg: 0 8px 40px rgba(74, 55, 40, 0.16);
            --radius-sm: 8px;
            --radius-md: 12px;
            --radius-lg: 20px;
            --transition: 0.3s cubic-bezier(0.4, 0, 0.2, 1);
            --max-width: 1200px;
            --header-h: 72px;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        html {
            scroll-behavior: smooth;
            scroll-padding-top: var(--header-h);
        }

        body {
            font-family: "PingFang SC", "Microsoft YaHei", "Hiragino Sans GB", "Noto Sans SC", system-ui, -apple-system, sans-serif;
            background: var(--warm-bg);
            color: var(--text-dark);
            line-height: 1.6;
            -webkit-font-smoothing: antialiased;
        }

        /* ============ Header / Navbar ============ */
        .header {
            position: fixed;
            top: 0;
            left: 0;
            right: 0;
            z-index: 1000;
            background: rgba(250, 247, 242, 0.92);
            backdrop-filter: blur(12px);
            -webkit-backdrop-filter: blur(12px);
            border-bottom: 1px solid var(--border);
            height: var(--header-h);
            transition: var(--transition);
        }

        .header-inner {
            max-width: var(--max-width);
            margin: 0 auto;
            padding: 0 24px;
            display: flex;
            align-items: center;
            justify-content: space-between;
            height: 100%;
        }

        .logo {
            display: flex;
            align-items: center;
            gap: 10px;
            text-decoration: none;
            color: var(--text-dark);
            font-weight: 700;
            font-size: 1.4rem;
            letter-spacing: 2px;
        }

        .logo-icon {
            width: 42px;
            height: 42px;
            background: linear-gradient(135deg, var(--wood-mid), var(--wood-dark));
            border-radius: var(--radius-sm);
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--cream);
            font-size: 1.2rem;
        }

        .nav-links {
            display: flex;
            list-style: none;
            gap: 4px;
        }

        .nav-links a {
            color: var(--text-mid);
            text-decoration: none;
            padding: 8px 16px;
            border-radius: 6px;
            font-size: 0.95rem;
            font-weight: 500;
            transition: var(--transition);
        }

        .nav-links a:hover,
        .nav-links a.active {
            color: var(--wood-mid);
            background: rgba(107, 76, 59, 0.08);
        }

        .nav-cta {
            background: var(--wood-mid) !important;
            color: var(--white) !important;
            padding: 10px 20px !important;
            border-radius: 8px !important;
        }

        .nav-cta:hover {
            background: var(--wood-dark) !important;
            color: var(--white) !important;
            transform: translateY(-1px);
            box-shadow: var(--shadow-sm);
        }

        /* Mobile menu toggle */
        .menu-toggle {
            display: none;
            background: none;
            border: none;
            cursor: pointer;
            padding: 8px;
            flex-direction: column;
            gap: 5px;
        }

        .menu-toggle span {
            display: block;
            width: 24px;
            height: 2px;
            background: var(--text-dark);
            border-radius: 2px;
            transition: var(--transition);
        }

        /* ============ Hero Section ============ */
        .hero {
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            background:
                linear-gradient(rgba(44, 36, 22, 0.55), rgba(44, 36, 22, 0.65)),
                url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1200 800"><defs><linearGradient id="g" x1="0%" y1="0%" x2="100%" y2="100%"><stop offset="0%" style="stop-color:%238B7355"/><stop offset="50%" style="stop-color:%236B4C3B"/><stop offset="100%" style="stop-color:%234A3728"/></linearGradient></defs><rect fill="url(%23g)" width="1200" height="800"/><rect y="620" width="1200" height="180" fill="%23F5F0E8" opacity="0.15"/><circle cx="200" cy="150" r="60" fill="%23C8974A" opacity="0.3"/><circle cx="1050" cy="450" r="100" fill="%23C8974A" opacity="0.2"/><circle cx="600" cy="350" r="250" fill="%23C8974A" opacity="0.08"/></svg>');
            background-size: cover;
            background-position: center;
            padding: 0 24px;
        }

        .hero-content {
            max-width: 720px;
            color: var(--white);
        }

        .hero-badge {
            display: inline-block;
            background: rgba(255, 255, 255, 0.15);
            backdrop-filter: blur(8px);
            border: 1px solid rgba(255, 255, 255, 0.25);
            padding: 6px 18px;
            border-radius: 50px;
            font-size: 0.9rem;
            letter-spacing: 4px;
            margin-bottom: 28px;
            animation: fadeInUp 0.8s ease-out;
        }

        .hero h1 {
            font-size: clamp(2.4rem, 5vw, 3.6rem);
            font-weight: 800;
            letter-spacing: 3px;
            line-height: 1.25;
            margin-bottom: 20px;
            animation: fadeInUp 0.8s 0.15s ease-out both;
        }

        .hero h1 span {
            color: var(--accent);
        }

        .hero p {
            font-size: 1.15rem;
            color: rgba(255, 255, 255, 0.85);
            max-width: 520px;
            margin: 0 auto 36px;
            animation: fadeInUp 0.8s 0.3s ease-out both;
        }

        .hero-buttons {
            display: flex;
            gap: 16px;
            justify-content: center;
            flex-wrap: wrap;
            animation: fadeInUp 0.8s 0.45s ease-out both;
        }

        .btn {
            display: inline-flex;
            align-items: center;
            gap: 8px;
            padding: 14px 32px;
            border-radius: 10px;
            font-size: 1rem;
            font-weight: 600;
            text-decoration: none;
            border: none;
            cursor: pointer;
            transition: var(--transition);
            white-space: nowrap;
        }

        .btn-primary {
            background: var(--accent);
            color: var(--white);
        }

        .btn-primary:hover {
            background: var(--accent-hover);
            transform: translateY(-2px);
            box-shadow: 0 6px 24px rgba(200, 151, 74, 0.4);
        }

        .btn-outline {
            background: transparent;
            color: var(--white);
            border: 2px solid rgba(255, 255, 255, 0.5);
        }

        .btn-outline:hover {
            background: rgba(255, 255, 255, 0.1);
            border-color: var(--white);
            transform: translateY(-2px);
        }

        .scroll-hint {
            position: absolute;
            bottom: 40px;
            left: 50%;
            transform: translateX(-50%);
            animation: bounce 2s infinite;
        }

        .scroll-hint svg {
            width: 24px;
            height: 24px;
            stroke: rgba(255, 255, 255, 0.7);
        }

        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(24px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        @keyframes bounce {
            0%, 100% { transform: translateX(-50%) translateY(0); }
            50% { transform: translateX(-50%) translateY(10px); }
        }

        /* ============ Section Common ============ */
        .section {
            padding: 100px 24px;
        }

        .section-inner {
            max-width: var(--max-width);
            margin: 0 auto;
        }

        .section-header {
            text-align: center;
            margin-bottom: 60px;
        }

        .section-tag {
            display: inline-block;
            color: var(--accent);
            font-weight: 600;
            font-size: 0.9rem;
            letter-spacing: 3px;
            text-transform: uppercase;
            margin-bottom: 12px;
        }

        .section-title {
            font-size: clamp(1.8rem, 3.5vw, 2.4rem);
            font-weight: 700;
            color: var(--text-dark);
            margin-bottom: 16px;
        }

        .section-desc {
            color: var(--text-light);
            max-width: 560px;
            margin: 0 auto;
            font-size: 1.05rem;
        }

        /* ============ Products Grid ============ */
        .products-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 28px;
        }

        .product-card {
            background: var(--white);
            border-radius: var(--radius-lg);
            overflow: hidden;
            box-shadow: var(--shadow-sm);
            transition: var(--transition);
            cursor: pointer;
        }

        .product-card:hover {
            transform: translateY(-6px);
            box-shadow: var(--shadow-lg);
        }

        .product-img {
            height: 220px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 3.5rem;
            position: relative;
            overflow: hidden;
        }

        .product-img.bedroom { background: linear-gradient(135deg, #E8DFF0, #F0E5F5); }
        .product-img.living { background: linear-gradient(135deg, #F0E8DF, #F5EFE5); }
        .product-img.dining { background: linear-gradient(135deg, #E8F0E8, #E5F0E5); }
        .product-img.office { background: linear-gradient(135deg, #DFE8F0, #E5ECF5); }
        .product-img.kitchen { background: linear-gradient(135deg, #F0F0DF, #F5F5E5); }
        .product-img.kids { background: linear-gradient(135deg, #F0DFE8, #F5E5F0); }

        .product-tag {
            position: absolute;
            top: 16px;
            right: 16px;
            background: var(--accent);
            color: var(--white);
            font-size: 0.75rem;
            font-weight: 600;
            padding: 4px 12px;
            border-radius: 50px;
        }

        .product-info {
            padding: 24px;
        }

        .product-info h3 {
            font-size: 1.2rem;
            margin-bottom: 8px;
            color: var(--text-dark);
        }

        .product-info p {
            color: var(--text-light);
            font-size: 0.9rem;
            margin-bottom: 16px;
        }

        .product-link {
            color: var(--wood-mid);
            font-weight: 600;
            text-decoration: none;
            font-size: 0.95rem;
            display: inline-flex;
            align-items: center;
            gap: 6px;
            transition: var(--transition);
        }

        .product-link:hover {
            color: var(--accent);
            gap: 10px;
        }

        /* ============ Services ============ */
        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
            gap: 28px;
        }

        .service-card {
            background: var(--white);
            border-radius: var(--radius-md);
            padding: 36px 28px;
            text-align: center;
            box-shadow: var(--shadow-sm);
            transition: var(--transition);
            border: 1px solid transparent;
        }

        .service-card:hover {
            border-color: var(--accent);
            box-shadow: var(--shadow-md);
            transform: translateY(-4px);
        }

        .service-icon {
            width: 64px;
            height: 64px;
            margin: 0 auto 20px;
            background: var(--cream);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.8rem;
        }

        .service-card h3 {
            font-size: 1.1rem;
            margin-bottom: 10px;
        }

        .service-card p {
            color: var(--text-light);
            font-size: 0.9rem;
        }

        /* ============ Process Timeline ============ */
        .process-list {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 0;
            counter-reset: step;
        }

        .process-step {
            flex: 1 1 180px;
            min-width: 160px;
            text-align: center;
            padding: 32px 20px;
            position: relative;
        }

        .process-step::after {
            content: '';
            position: absolute;
            top: 52px;
            left: calc(50% + 40px);
            width: calc(100% - 80px);
            height: 2px;
            background: var(--border);
            z-index: 0;
        }

        .process-step:last-child::after {
            display: none;
        }

        .step-num {
            width: 48px;
            height: 48px;
            background: var(--wood-mid);
            color: var(--white);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.1rem;
            font-weight: 700;
            margin: 0 auto 16px;
            position: relative;
            z-index: 1;
        }

        .process-step h4 {
            font-size: 1rem;
            margin-bottom: 6px;
        }

        .process-step .step-desc {
            color: var(--text-light);
            font-size: 0.85rem;
        }

        /* ============ Case Gallery ============ */
        .cases-grid {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 16px;
        }

        .case-item {
            aspect-ratio: 1;
            border-radius: var(--radius-md);
            overflow: hidden;
            position: relative;
            cursor: pointer;
        }

        .case-item:nth-child(1) { background: linear-gradient(135deg, #D4C4B0, #C4B5A0); }
        .case-item:nth-child(2) { background: linear-gradient(135deg, #B8C4B0, #A8B5A0); }
        .case-item:nth-child(3) { background: linear-gradient(135deg, #C4B0C0, #B5A0B0); }
        .case-item:nth-child(4) { background: linear-gradient(135deg, #B0C0C4, #A0B0B5); }

        .case-overlay {
            position: absolute;
            inset: 0;
            background: rgba(74, 55, 40, 0.7);
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            color: var(--white);
            opacity: 0;
            transition: var(--transition);
        }

        .case-item:hover .case-overlay {
            opacity: 1;
        }

        .case-overlay span {
            font-size: 1.2rem;
            font-weight: 600;
        }

        .case-overlay small {
            font-size: 0.85rem;
            opacity: 0.8;
        }

        /* ============ About ============ */
        .about-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 60px;
            align-items: center;
        }

        .about-visual {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 16px;
        }

        .about-stat {
            background: var(--white);
            border-radius: var(--radius-md);
            padding: 32px 24px;
            text-align: center;
            box-shadow: var(--shadow-sm);
        }

        .about-stat .stat-num {
            font-size: 2rem;
            font-weight: 800;
            color: var(--accent);
            display: block;
        }

        .about-stat .stat-label {
            color: var(--text-light);
            font-size: 0.9rem;
            margin-top: 4px;
        }

        .about-text h3 {
            font-size: 1.6rem;
            margin-bottom: 16px;
        }

        .about-text p {
            color: var(--text-mid);
            margin-bottom: 12px;
        }

        /* ============ CTA Banner ============ */
        .cta-banner {
            background: linear-gradient(135deg, var(--wood-dark), var(--wood-mid));
            border-radius: var(--radius-lg);
            padding: 60px 48px;
            text-align: center;
            color: var(--white);
        }

        .cta-banner h2 {
            font-size: 2rem;
            margin-bottom: 12px;
        }

        .cta-banner p {
            color: rgba(255, 255, 255, 0.8);
            margin-bottom: 28px;
        }

        .cta-banner .btn-primary {
            background: var(--white);
            color: var(--wood-dark);
        }

        .cta-banner .btn-primary:hover {
            background: var(--cream);
            box-shadow: 0 6px 24px rgba(0, 0, 0, 0.2);
        }

        /* ============ Contact ============ */
        .contact-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 40px;
        }

        .contact-info-list {
            list-style: none;
            display: flex;
            flex-direction: column;
            gap: 20px;
        }

        .contact-info-list li {
            display: flex;
            gap: 16px;
            align-items: flex-start;
        }

        .contact-icon {
            width: 44px;
            height: 44px;
            background: var(--cream);
            border-radius: var(--radius-sm);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.2rem;
            flex-shrink: 0;
        }

        .contact-info-list h4 {
            font-size: 0.95rem;
            margin-bottom: 2px;
        }

        .contact-info-list span {
            color: var(--text-light);
            font-size: 0.9rem;
        }

        .contact-form {
            background: var(--white);
            padding: 36px;
            border-radius: var(--radius-lg);
            box-shadow: var(--shadow-sm);
        }

        .contact-form h3 {
            margin-bottom: 24px;
            font-size: 1.3rem;
        }

        .form-group {
            margin-bottom: 18px;
        }

        .form-group label {
            display: block;
            font-size: 0.9rem;
            font-weight: 500;
            margin-bottom: 6px;
            color: var(--text-mid);
        }

        .form-group input,
        .form-group select,
        .form-group textarea {
            width: 100%;
            padding: 12px 16px;
            border: 1px solid var(--border);
            border-radius: var(--radius-sm);
            font-size: 0.95rem;
            font-family: inherit;
            background: var(--warm-bg);
            transition: var(--transition);
            color: var(--text-dark);
        }

        .form-group input:focus,
        .form-group select:focus,
        .form-group textarea:focus {
            outline: none;
            border-color: var(--accent);
            box-shadow: 0 0 0 3px rgba(200, 151, 74, 0.15);
        }

        .form-row {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 16px;
        }

        /* ============ Footer ============ */
        .footer {
            background: var(--wood-dark);
            color: rgba(255, 255, 255, 0.7);
            padding: 60px 24px 30px;
        }

        .footer-grid {
            max-width: var(--max-width);
            margin: 0 auto;
            display: grid;
            grid-template-columns: 2fr 1fr 1fr 1.5fr;
            gap: 40px;
            margin-bottom: 40px;
        }

        .footer-brand .logo-text {
            color: var(--white);
            font-size: 1.3rem;
            font-weight: 700;
            letter-spacing: 2px;
        }

        .footer-brand p {
            margin-top: 12px;
            font-size: 0.9rem;
            line-height: 1.7;
        }

        .footer h4 {
            color: var(--white);
            font-size: 1rem;
            margin-bottom: 18px;
        }

        .footer ul {
            list-style: none;
        }

        .footer ul li {
            margin-bottom: 10px;
        }

        .footer ul a {
            color: rgba(255, 255, 255, 0.6);
            text-decoration: none;
            font-size: 0.9rem;
            transition: var(--transition);
        }

        .footer ul a:hover {
            color: var(--accent);
        }

        .footer-qr {
            width: 100px;
            height: 100px;
            background: var(--white);
            border-radius: var(--radius-sm);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 0.75rem;
            color: var(--text-mid);
            margin-bottom: 10px;
        }

        .footer-bottom {
            max-width: var(--max-width);
            margin: 0 auto;
            padding-top: 24px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            display: flex;
            justify-content: space-between;
            flex-wrap: wrap;
            gap: 12px;
            font-size: 0.85rem;
        }

        /* ============ Back to Top ============ */
        .back-to-top {
            position: fixed;
            bottom: 32px;
            right: 32px;
            width: 44px;
            height: 44px;
            background: var(--wood-mid);
            color: var(--white);
            border: none;
            border-radius: 50%;
            cursor: pointer;
            font-size: 1.2rem;
            box-shadow: var(--shadow-md);
            transition: var(--transition);
            opacity: 0;
            pointer-events: none;
            z-index: 999;
        }

        .back-to-top.visible {
            opacity: 1;
            pointer-events: auto;
        }

        .back-to-top:hover {
            background: var(--accent);
            transform: translateY(-3px);
        }

        /* ============ Responsive ============ */
        @media (max-width: 1024px) {
            .footer-grid {
                grid-template-columns: 1fr 1fr;
            }
        }

        @media (max-width: 768px) {
            .nav-links {
                display: none;
            }

            .menu-toggle {
                display: flex;
            }

            .nav-links.mobile-open {
                display: flex;
                flex-direction: column;
                position: absolute;
                top: var(--header-h);
                left: 0;
                right: 0;
                background: var(--warm-bg);
                padding: 16px;
                border-bottom: 1px solid var(--border);
                box-shadow: var(--shadow-md);
            }

            .hero h1 {
                font-size: 2rem;
            }

            .about-grid,
            .contact-grid {
                grid-template-columns: 1fr;
                gap: 32px;
            }

            .cases-grid {
                grid-template-columns: repeat(2, 1fr);
            }

            .form-row {
                grid-template-columns: 1fr;
            }

            .footer-grid {
                grid-template-columns: 1fr;
                gap: 28px;
            }

            .process-step::after {
                display: none;
            }

            .section {
                padding: 64px 16px;
            }

            .cta-banner {
                padding: 40px 24px;
            }
        }

        @media (max-width: 480px) {
            .hero-buttons {
                flex-direction: column;
                align-items: center;
            }

            .products-grid {
                grid-template-columns: 1fr;
            }

            .services-grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>

    <!-- ==================== Header ==================== -->
    <header class="header" id="header">
        <div class="header-inner">
            <a href="#" class="logo">
                <div class="logo-icon">🏠</div>
                ZRX 家具
            </a>
            <nav>
                <ul class="nav-links" id="navLinks">
                    <li><a href="#home" class="active">首页</a></li>
                    <li><a href="#products">产品中心</a></li>
                    <li><a href="#services">定制服务</a></li>
                    <li><a href="#process">生产工艺</a></li>
                    <li><a href="#cases">案例展示</a></li>
                    <li><a href="#about">关于我们</a></li>
                    <li><a href="#contact">联系我们</a></li>
                    <li><a href="#contact" class="nav-cta">免费咨询</a></li>
                </ul>
            </nav>
            <button class="menu-toggle" id="menuToggle" aria-label="菜单">
                <span></span><span></span><span></span>
            </button>
        </div>
    </header>

    <!-- ==================== Hero ==================== -->
    <section class="hero" id="home">
        <div class="hero-content">
            <div class="hero-badge">ZRX · 品质生活</div>
            <h1>匠心制造 <span>美好家居</span></h1>
            <p>ZRX有限公司专注高端家具研发、生产与定制，从设计到交付，为每个家庭创造舒适、耐用、美观的家具产品。</p>
            <div class="hero-buttons">
                <a href="#products" class="btn btn-primary">🛋️ 浏览产品</a>
                <a href="#contact" class="btn btn-outline">📋 获取报价</a>
            </div>
        </div>
        <div class="scroll-hint">
            <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                <path d="M7 13l5 5 5-5M7 6l5 5 5-5"/>
            </svg>
        </div>
    </section>

    <!-- ==================== Products ==================== -->
    <section class="section" id="products">
        <div class="section-inner">
            <div class="section-header">
                <div class="section-tag">Products</div>
                <h2 class="section-title">产品中心</h2>
                <p class="section-desc">覆盖全屋空间，提供从单件家具到整体家居的一站式解决方案</p>
            </div>
            <div class="products-grid">
                <!-- 客厅家具 -->
                <div class="product-card">
                    <div class="product-img living">
                        🛋️
                        <span class="product-tag">热销</span>
                    </div>
                    <div class="product-info">
                        <h3>客厅家具</h3>
                        <p>沙发、茶几、电视柜、展示柜——打造温馨会客空间</p>
                        <a href="#" class="product-link">查看系列 →</a>
                    </div>
                </div>
                <!-- 卧室家具 -->
                <div class="product-card">
                    <div class="product-img bedroom">
                        🛏️
                        <span class="product-tag">新品</span>
                    </div>
                    <div class="product-info">
                        <h3>卧室家具</h3>
                        <p>床、衣柜、梳妆台、床头柜——营造舒适睡眠环境</p>
                        <a href="#" class="product-link">查看系列 →</a>
                    </div>
                </div>
                <!-- 餐厅家具 -->
                <div class="product-card">
                    <div class="product-img dining">
                        🍽️
                    </div>
                    <div class="product-info">
                        <h3>餐厅家具</h3>
                        <p>餐桌、餐椅、餐边柜、酒柜——享受每一餐的美好</p>
                        <a href="#" class="product-link">查看系列 →</a>
                    </div>
                </div>
                <!-- 办公家具 -->
                <div class="product-card">
                    <div class="product-img office">
                        💼
                    </div>
                    <div class="product-info">
                        <h3>办公家具</h3>
                        <p>办公桌、书柜、会议桌、人体工学椅——高效工作空间</p>
                        <a href="#" class="product-link">查看系列 →</a>
                    </div>
                </div>
                <!-- 厨房家具 -->
                <div class="product-card">
                    <div class="product-img kitchen">
                        🍳
                    </div>
                    <div class="product-info">
                        <h3>厨房定制</h3>
                        <p>整体橱柜、中岛台、收纳系统——功能与美学兼得</p>
                        <a href="#" class="product-link">查看系列 →</a>
                    </div>
                </div>
                <!-- 儿童家具 -->
                <div class="product-card">
                    <div class="product-img kids">
                        🧸
                    </div>
                    <div class="product-info">
                        <h3>儿童家具</h3>
                        <p>儿童床、书桌、收纳柜——安全环保，陪伴成长</p>
                        <a href="#" class="product-link">查看系列 →</a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- ==================== Services ==================== -->
    <section class="section" id="services" style="background: var(--white);">
        <div class="section-inner">
            <div class="section-header">
                <div class="section-tag">Services</div>
                <h2 class="section-title">定制服务</h2>
                <p class="section-desc">从需求沟通到安装交付，全流程一对一专属服务</p>
            </div>
            <div class="services-grid">
                <div class="service-card">
                    <div class="service-icon">📐</div>
                    <h3>免费量尺设计</h3>
                    <p>专业设计师上门量尺，根据空间与需求提供3D效果图方案</p>
                </div>
                <div class="service-card">
                    <div class="service-icon">🪵</div>
                    <h3>选材定制</h3>
                    <p>实木、板材、金属、石材等多种材质可选，满足不同风格与预算</p>
                </div>
                <div class="service-card">
                    <div class="service-icon">🏭</div>
                    <h3>自有工厂生产</h3>
                    <p>5000㎡现代化工厂，德国进口设备，严格品控保障品质</p>
                </div>
                <div class="service-card">
                    <div class="service-icon">🚚</div>
                    <h3>配送安装</h3>
                    <p>专业物流团队配送上门，熟练师傅现场安装，省心无忧</p>
                </div>
                <div class="service-card">
                    <div class="service-icon">🛡️</div>
                    <h3>5年质保</h3>
                    <p>所有产品享受5年质量保证，终身维护，让您用得放心</p>
                </div>
                <div class="service-card">
                    <div class="service-icon">🔄</div>
                    <h3>免费翻新保养</h3>
                    <p>定期回访，提供家具保养指导及翻新服务，延长使用寿命</p>
                </div>
            </div>
        </div>
    </section>

    <!-- ==================== Process ==================== -->
    <section class="section" id="process">
        <div class="section-inner">
            <div class="section-header">
                <div class="section-tag">Process</div>
                <h2 class="section-title">生产工艺</h2>
                <p class="section-desc">每一件家具都经过严格的生产流程，确保卓越品质</p>
            </div>
            <div class="process-list">
                <div class="process-step">
                    <div class="step-num">01</div>
                    <h4>需求沟通</h4>
                    <p class="step-desc">了解客户需求与空间特点</p>
                </div>
                <div class="process-step">
                    <div class="step-num">02</div>
                    <h4>方案设计</h4>
                    <p class="step-desc">3D建模 + 材质搭配方案</p>
                </div>
                <div class="process-step">
                    <div class="step-num">03</div>
                    <h4>精选原料</h4>
                    <p class="step-desc">严选环保板材与进口五金</p>
                </div>
                <div class="process-step">
                    <div class="step-num">04</div>
                    <h4>精密制造</h4>
                    <p class="step-desc">CNC加工 + 手工打磨结合</p>
                </div>
                <div class="process-step">
                    <div class="step-num">05</div>
                    <h4>品质检验</h4>
                    <p class="step-desc">4道质检工序，层层把关</p>
                </div>
                <div class="process-step">
                    <div class="step-num">06</div>
                    <h4>交付安装</h4>
                    <p class="step-desc">专业配送 + 无忧安装服务</p>
                </div>
            </div>
        </div>
    </section>

    <!-- ==================== Cases ==================== -->
    <section class="section" id="cases" style="background: var(--white);">
        <div class="section-inner">
            <div class="section-header">
                <div class="section-tag">Cases</div>
                <h2 class="section-title">案例展示</h2>
                <p class="section-desc">超过 500+ 家庭与企业的共同选择</p>
            </div>
            <div class="cases-grid">
                <div class="case-item">
                    <div class="case-overlay">
                        <span>现代简约客厅</span>
                        <small>120㎡ 三居室</small>
                    </div>
                </div>
                <div class="case-item">
                    <div class="case-overlay">
                        <span>新中式主卧</span>
                        <small>150㎡ 大平层</small>
                    </div>
                </div>
                <div class="case-item">
                    <div class="case-overlay">
                        <span>轻奢餐厅套系</span>
                        <small>别墅定制</small>
                    </div>
                </div>
                <div class="case-item">
                    <div class="case-overlay">
                        <span>企业办公空间</span>
                        <small>2000㎡ 办公区</small>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- ==================== About ==================== -->
    <section class="section" id="about">
        <div class="section-inner">
            <div class="about-grid">
                <div class="about-visual">
                    <div class="about-stat">
                        <span class="stat-num">15+</span>
                        <span class="stat-label">年行业经验</span>
                    </div>
                    <div class="about-stat">
                        <span class="stat-num">5000㎡</span>
                        <span class="stat-label">生产基地</span>
                    </div>
                    <div class="about-stat">
                        <span class="stat-num">500+</span>
                        <span class="stat-label">服务客户</span>
                    </div>
                    <div class="about-stat">
                        <span class="stat-num">50+</span>
                        <span class="stat-label">专业团队</span>
                    </div>
                </div>
                <div class="about-text">
                    <div class="section-tag">About Us</div>
                    <h3>关于 ZRX 有限公司</h3>
                    <p>ZRX有限公司成立于2010年，总部位于中国家具之都，是一家集家具研发、设计、生产、销售、服务于一体的现代化企业。</p>
                    <p>我们拥有 5000㎡ 的现代化生产基地，引进德国豪迈（HOMAG）全自动生产线，采用 E0 级环保板材与进口五金配件，严格执行 ISO 9001 质量管理体系。</p>
                    <p>公司秉承"匠心品质，服务至上"的经营理念，以精湛工艺与贴心服务，致力于为每一位客户打造理想的家居空间。</p>
                    <a href="#contact" class="btn btn-primary" style="margin-top: 12px;">了解更多 →</a>
                </div>
            </div>
        </div>
    </section>

    <!-- ==================== CTA Banner ==================== -->
    <section class="section">
        <div class="section-inner">
            <div class="cta-banner">
                <h2>🏠 为您打造理想中的家</h2>
                <p>现在预约，即可享受免费上门量尺 + 3D效果图设计服务</p>
                <a href="#contact" class="btn btn-primary">立即预约免费设计</a>
            </div>
        </div>
    </section>

    <!-- ==================== Contact ==================== -->
    <section class="section" id="contact" style="background: var(--white);">
        <div class="section-inner">
            <div class="section-header">
                <div class="section-tag">Contact</div>
                <h2 class="section-title">联系我们</h2>
                <p class="section-desc">期待与您的沟通，让我们为您提供最优质的服务</p>
            </div>
            <div class="contact-grid">
                <!-- Contact Info -->
                <div>
                    <ul class="contact-info-list">
                        <li>
                            <div class="contact-icon">📍</div>
                            <div>
                                <h4>公司地址</h4>
                                <span>中国家具产业园区 ZRX大厦</span>
                            </div>
                        </li>
                        <li>
                            <div class="contact-icon">📞</div>
                            <div>
                                <h4>联系电话</h4>
                                <span>400-XXX-XXXX</span>
                            </div>
                        </li>
                        <li>
                            <div class="contact-icon">📧</div>
                            <div>
                                <h4>电子邮箱</h4>
                                <span>contact@zrx-furniture.com</span>
                            </div>
                        </li>
                        <li>
                            <div class="contact-icon">🕐</div>
                            <div>
                                <h4>营业时间</h4>
                                <span>周一至周六 8:30 - 18:00</span>
                            </div>
                        </li>
                    </ul>
                </div>
                <!-- Contact Form -->
                <div class="contact-form">
                    <h3>在线留言</h3>
                    <form onsubmit="handleSubmit(event)">
                        <div class="form-row">
                            <div class="form-group">
                                <label for="name">您的姓名 *</label>
                                <input type="text" id="name" placeholder="请输入姓名" required>
                            </div>
                            <div class="form-group">
                                <label for="phone">联系电话 *</label>
                                <input type="tel" id="phone" placeholder="请输入电话" required>
                            </div>
                        </div>
                        <div class="form-group">
                            <label for="interest">关注产品</label>
                            <select id="interest">
                                <option value="">请选择您感兴趣的产品类型</option>
                                <option value="living">客厅家具</option>
                                <option value="bedroom">卧室家具</option>
                                <option value="dining">餐厅家具</option>
                                <option value="office">办公家具</option>
                                <option value="kitchen">厨房定制</option>
                                <option value="kids">儿童家具</option>
                                <option value="full">全屋定制</option>
                            </select>
                        </div>
                        <div class="form-group">
                            <label for="message">留言内容</label>
                            <textarea id="message" rows="4" placeholder="请描述您的需求（如户型、风格偏好、预算等）"></textarea>
                        </div>
                        <button type="submit" class="btn btn-primary" style="width: 100%; justify-content: center;">✉️ 提交留言</button>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <!-- ==================== Footer ==================== -->
    <footer class="footer">
        <div class="footer-grid">
            <div class="footer-brand">
                <div class="logo-text">ZRX 家具</div>
                <p>ZRX有限公司 — 专注高端家具研发、生产与定制。以匠心品质，为每个家庭创造美好生活空间。</p>
            </div>
            <div>
                <h4>产品中心</h4>
                <ul>
                    <li><a href="#">客厅家具</a></li>
                    <li><a href="#">卧室家具</a></li>
                    <li><a href="#">餐厅家具</a></li>
                    <li><a href="#">办公家具</a></li>
                    <li><a href="#">厨房定制</a></li>
                </ul>
            </div>
            <div>
                <h4>服务支持</h4>
                <ul>
                    <li><a href="#">定制流程</a></li>
                    <li><a href="#">售后服务</a></li>
                    <li><a href="#">保养指南</a></li>
                    <li><a href="#">常见问题</a></li>
                    <li><a href="#">企业新闻</a></li>
                </ul>
            </div>
            <div>
                <h4>关注我们</h4>
                <div class="footer-qr">公众号<br>二维码</div>
                <p style="font-size: 0.85rem;">扫码关注微信公众号<br>获取最新优惠与家居灵感</p>
            </div>
        </div>
        <div class="footer-bottom">
            <span>© 2024 ZRX有限公司. All rights reserved.</span>
            <span>备案号：粤ICP备XXXXXXXX号</span>
        </div>
    </footer>

    <!-- Back to Top -->
    <button class="back-to-top" id="backToTop" aria-label="返回顶部">↑</button>

    <script>
        // ============ Mobile Menu Toggle ============
        const menuToggle = document.getElementById('menuToggle');
        const navLinks = document.getElementById('navLinks');

        menuToggle.addEventListener('click', () => {
            navLinks.classList.toggle('mobile-open');
        });

        // Close menu when clicking a link
        navLinks.querySelectorAll('a').forEach(link => {
            link.addEventListener('click', () => {
                navLinks.classList.remove('mobile-open');
            });
        });

        // ============ Active Nav Link Highlight ============
        const sections = document.querySelectorAll('section[id]');
        const navItems = document.querySelectorAll('.nav-links a:not(.nav-cta)');

        function updateActiveLink() {
            let current = '';
            sections.forEach(section => {
                const sectionTop = section.offsetTop - 100;
                if (window.scrollY >= sectionTop) {
                    current = section.getAttribute('id');
                }
            });
            navItems.forEach(link => {
                link.classList.remove('active');
                if (link.getAttribute('href') === '#' + current) {
                    link.classList.add('active');
                }
            });
        }

        window.addEventListener('scroll', updateActiveLink);

        // ============ Back to Top ============
        const backToTop = document.getElementById('backToTop');

        window.addEventListener('scroll', () => {
            if (window.scrollY > 600) {
                backToTop.classList.add('visible');
            } else {
                backToTop.classList.remove('visible');
            }
        });

        backToTop.addEventListener('click', () => {
            window.scrollTo({ top: 0, behavior: 'smooth' });
        });

        // ============ Contact Form ============
        function handleSubmit(event) {
            event.preventDefault();
            const name = document.getElementById('name').value;
            const phone = document.getElementById('phone').value;
            const interest = document.getElementById('interest').value;
            const message = document.getElementById('message').value;

            if (!name || !phone) {
                alert('请填写姓名和联系电话');
                return;
            }

            // 这里可以接入实际的表单提交 API
            alert(`感谢 ${name}！\n\n您的留言已成功提交，我们的客服将在24小时内与您联系。\n\n如需紧急咨询，请拨打：400-XXX-XXXX`);
            event.target.reset();
        }

        // ============ Smooth scroll for anchor links (fallback) ============
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    // Smooth scroll is handled by CSS scroll-behavior
                }
            });
        });
    </script>
</body>
</html>
