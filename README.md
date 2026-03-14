<!DOCTYPE html>
<html lang="pt-BR">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <meta name="description"
        content="JP Cell - Venda de celulares, acessórios e assistência técnica especializada. Seu celular novo ou consertado com quem entende.">
    <title>JP Cell - Assistência Técnica e Smartshop</title>

    <!-- Google Fonts: Poppins -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700;800&display=swap"
        rel="stylesheet">

    <!-- Font Awesome Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">

    <style>
        /* CSS Variables */
        :root {
            --primary-color: #FFD400;
            /* Amarelo destaque */
            --bg-color: #000000;
            /* Preto profundo */
            --card-bg: #1A1A1A;
            /* Cinza escuro */
            --text-color: #FFFFFF;
            /* Branco */
            --text-muted: #CCCCCC;
            --font-main: 'Poppins', sans-serif;
            --transition: all 0.3s cubic-bezier(0.25, 0.8, 0.25, 1);
        }

        /* Reset & Base Styles */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            font-family: var(--font-main);
            background-color: var(--bg-color);
            color: var(--text-color);
            line-height: 1.6;
            overflow-x: hidden;
        }

        /* Typography */
        h1,
        h2,
        h3,
        h4 {
            font-weight: 700;
        }

        p {
            color: var(--text-muted);
        }

        a {
            text-decoration: none;
            color: var(--text-color);
            transition: var(--transition);
        }

        a:hover {
            color: var(--primary-color);
        }

        /* Reusable Components */
        .section {
            padding: 100px 5%;
        }

        .section-title {
            text-align: center;
            font-size: 2.5rem;
            margin-bottom: 60px;
            color: var(--text-color);
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .section-title span {
            color: var(--primary-color);
        }

        .btn {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            gap: 10px;
            padding: 14px 32px;
            border-radius: 8px;
            font-weight: 600;
            font-size: 1rem;
            transition: var(--transition);
            cursor: pointer;
            border: none;
            position: relative;
            overflow: hidden;
            z-index: 1;
        }

        .btn-primary {
            background-color: var(--primary-color);
            color: #000000;
        }

        .btn-primary:hover {
            background-color: #e6be00;
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(255, 212, 0, 0.3);
            color: #000000;
        }

        .btn-outline {
            border: 2px solid var(--primary-color);
            color: var(--primary-color);
            background: transparent;
        }

        .btn-outline:hover {
            background-color: var(--primary-color);
            color: #000000;
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(255, 212, 0, 0.2);
        }

        .btn-whatsapp {
            background-color: #25D366;
            color: white;
            padding: 10px 20px;
        }

        .btn-whatsapp:hover {
            background-color: #1ebe57;
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(37, 211, 102, 0.4);
            color: white;
        }

        /* Scroll Reveal Animation Classes */
        .reveal {
            opacity: 0;
            transform: translateY(40px);
            transition: all 0.8s cubic-bezier(0.5, 0, 0, 1);
        }

        .reveal.active {
            opacity: 1;
            transform: translateY(0);
        }

        .delay-1 {
            transition-delay: 0.1s;
        }

        .delay-2 {
            transition-delay: 0.2s;
        }

        .delay-3 {
            transition-delay: 0.3s;
        }

        /* Header & Navigation */
        header {
            position: fixed;
            top: 0;
            width: 100%;
            padding: 20px 5%;
            display: flex;
            justify-content: space-between;
            align-items: center;
            background-color: rgba(0, 0, 0, 0.85);
            backdrop-filter: blur(12px);
            -webkit-backdrop-filter: blur(12px);
            z-index: 1000;
            border-bottom: 1px solid rgba(255, 255, 255, 0.05);
            transition: var(--transition);
        }

        header.scrolled {
            padding: 15px 5%;
            box-shadow: 0 5px 20px rgba(0, 0, 0, 0.5);
            background-color: rgba(0, 0, 0, 0.95);
        }

        .logo {
            font-size: 2rem;
            font-weight: 800;
            color: var(--text-color);
            letter-spacing: 1px;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .logo span {
            color: var(--primary-color);
        }

        nav ul {
            list-style: none;
            display: flex;
            align-items: center;
            gap: 35px;
        }

        nav ul li a {
            font-weight: 500;
            font-size: 1rem;
            position: relative;
        }

        nav ul li a::after {
            content: '';
            position: absolute;
            width: 0;
            height: 2px;
            bottom: -5px;
            left: 0;
            background-color: var(--primary-color);
            transition: var(--transition);
        }

        nav ul li a:hover::after {
            width: 100%;
        }

        .menu-toggle {
            display: none;
            font-size: 1.8rem;
            cursor: pointer;
            color: var(--primary-color);
            z-index: 1001;
        }

        /* Hero Section */
        .hero {
            height: 100vh;
            min-height: 600px;
            display: flex;
            align-items: center;
            background: linear-gradient(to right, rgba(0, 0, 0, 0.9) 0%, rgba(0, 0, 0, 0.6) 100%),
                url('https://images.unsplash.com/photo-1580910051074-3eb694886505?ixlib=rb-4.0.3&auto=format&fit=crop&w=1920&q=80') center/cover no-repeat;
            padding: 0 5%;
            position: relative;
        }

        .hero-content {
            max-width: 800px;
            margin-top: 80px;
            position: relative;
            z-index: 2;
        }

        .hero h1 {
            font-size: 4rem;
            margin-bottom: 20px;
            line-height: 1.1;
            animation: fadeUp 1s ease forwards;
        }

        .hero h1 span {
            color: var(--primary-color);
        }

        .hero p {
            font-size: 1.25rem;
            margin-bottom: 40px;
            font-weight: 300;
            max-width: 600px;
            animation: fadeUp 1s ease 0.2s forwards;
            opacity: 0;
        }

        .hero-btns {
            display: flex;
            gap: 20px;
            animation: fadeUp 1s ease 0.4s forwards;
            opacity: 0;
        }

        @keyframes fadeUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }

            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        /* Services Section */
        .services {
            background-color: var(--bg-color);
        }

        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }

        .service-card {
            background-color: var(--card-bg);
            padding: 50px 40px;
            border-radius: 16px;
            text-align: center;
            transition: var(--transition);
            border: 1px solid rgba(255, 255, 255, 0.03);
            position: relative;
            overflow: hidden;
            z-index: 1;
        }

        .service-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(135deg, rgba(255, 212, 0, 0.1) 0%, rgba(0, 0, 0, 0) 100%);
            z-index: -1;
            opacity: 0;
            transition: var(--transition);
        }

        .service-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.6);
            border-color: rgba(255, 212, 0, 0.2);
        }

        .service-card:hover::before {
            opacity: 1;
        }

        .service-icon {
            width: 80px;
            height: 80px;
            background-color: rgba(255, 212, 0, 0.1);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 2.5rem;
            color: var(--primary-color);
            margin: 0 auto 25px;
            transition: var(--transition);
        }

        .service-card:hover .service-icon {
            background-color: var(--primary-color);
            color: #000;
            transform: scale(1.1);
        }

        .service-card h3 {
            font-size: 1.5rem;
            margin-bottom: 15px;
        }

        /* Differentials Section */
        .differentials {
            background-color: var(--card-bg);
            border-top: 1px solid rgba(255, 255, 255, 0.05);
            border-bottom: 1px solid rgba(255, 255, 255, 0.05);
            padding: 80px 5%;
        }

        .diff-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
            gap: 40px;
            text-align: center;
        }

        .diff-item {
            padding: 20px;
        }

        .diff-item .icon {
            font-size: 3rem;
            color: var(--primary-color);
            margin-bottom: 20px;
            transition: var(--transition);
        }

        .diff-item:hover .icon {
            transform: scale(1.1) rotate(5deg);
        }

        .diff-item h4 {
            font-size: 1.2rem;
            font-weight: 600;
            margin-bottom: 10px;
        }

        .diff-item p {
            font-size: 0.95rem;
            color: var(--text-muted);
        }

        /* Gallery / Products */
        .gallery-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 25px;
        }

        .gallery-item {
            position: relative;
            border-radius: 12px;
            overflow: hidden;
            aspect-ratio: 4 / 3;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.5);
        }

        .gallery-item img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.6s cubic-bezier(0.25, 0.8, 0.25, 1);
        }

        .gallery-item:hover img {
            transform: scale(1.1);
        }

        .gallery-overlay {
            position: absolute;
            inset: 0;
            background: linear-gradient(to top, rgba(0, 0, 0, 0.9) 0%, rgba(0, 0, 0, 0.2) 50%, transparent 100%);
            display: flex;
            align-items: flex-end;
            padding: 30px;
            opacity: 0;
            transition: var(--transition);
        }

        .gallery-item:hover .gallery-overlay {
            opacity: 1;
        }

        .gallery-overlay h3 {
            color: var(--primary-color);
            font-size: 1.5rem;
            transform: translateY(20px);
            transition: var(--transition);
        }

        .gallery-item:hover .gallery-overlay h3 {
            transform: translateY(0);
        }

        /* CTA Section */
        .cta {
            background: linear-gradient(135deg, #1A1A1A 0%, #000000 100%);
            text-align: center;
            border-top: 2px solid var(--primary-color);
            padding: 100px 5%;
            position: relative;
            overflow: hidden;
        }

        .cta::after {
            content: '\f232';
            font-family: "Font Awesome 6 Brands";
            position: absolute;
            font-size: 300px;
            color: rgba(37, 211, 102, 0.03);
            right: -50px;
            bottom: -50px;
            z-index: 0;
            transform: rotate(-15deg);
        }

        .cta-content {
            position: relative;
            z-index: 1;
            max-width: 800px;
            margin: 0 auto;
        }

        .cta h2 {
            font-size: 3rem;
            margin-bottom: 20px;
        }

        .cta p {
            font-size: 1.2rem;
            margin-bottom: 40px;
        }

        .btn-large {
            padding: 18px 40px;
            font-size: 1.2rem;
        }

        /* Footer */
        footer {
            background-color: #050505;
            padding: 80px 5% 30px;
            border-top: 1px solid rgba(255, 255, 255, 0.05);
        }

        .footer-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 40px;
            margin-bottom: 60px;
        }

        .footer-col h3 {
            font-size: 1.3rem;
            margin-bottom: 25px;
            color: var(--primary-color);
            position: relative;
            display: inline-block;
        }

        .footer-col h3::after {
            content: '';
            position: absolute;
            left: 0;
            bottom: -8px;
            width: 40px;
            height: 2px;
            background-color: var(--primary-color);
        }

        .footer-col p {
            margin-bottom: 15px;
        }

        .footer-col ul {
            list-style: none;
        }

        .footer-col ul li {
            margin-bottom: 15px;
        }

        .footer-col ul li a {
            color: var(--text-muted);
            display: inline-block;
        }

        .footer-col ul li a:hover {
            color: var(--primary-color);
            transform: translateX(5px);
        }

        .contact-info li {
            display: flex;
            align-items: center;
            gap: 15px;
        }

        .contact-info li i {
            color: var(--primary-color);
            font-size: 1.2rem;
            width: 20px;
            text-align: center;
        }

        .social-links {
            display: flex;
            gap: 15px;
            margin-top: 20px;
        }

        .social-links a {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 45px;
            height: 45px;
            background-color: rgba(255, 255, 255, 0.05);
            border-radius: 50%;
            color: var(--text-color);
            font-size: 1.2rem;
        }

        .social-links a:hover {
            background-color: var(--primary-color);
            color: #000;
            transform: translateY(-5px);
            box-shadow: 0 5px 15px rgba(255, 212, 0, 0.3);
        }

        .footer-bottom {
            text-align: center;
            padding-top: 30px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            color: #777;
            font-size: 0.9rem;
        }

        /* Responsive Design (Mobile-First approach adapted) */
        @media (max-width: 992px) {
            .hero h1 {
                font-size: 3.5rem;
            }

            .section {
                padding: 80px 5%;
            }
        }

        @media (max-width: 768px) {
            header {
                padding: 20px 5%;
            }

            .menu-toggle {
                display: block;
            }

            nav {
                position: fixed;
                top: 0;
                right: -100%;
                width: 80%;
                max-width: 400px;
                height: 100vh;
                background-color: var(--card-bg);
                box-shadow: -10px 0 30px rgba(0, 0, 0, 0.8);
                transition: right 0.4s cubic-bezier(0.25, 0.8, 0.25, 1);
                z-index: 1000;
                display: flex;
                align-items: center;
                justify-content: center;
            }

            nav.active {
                right: 0;
            }

            .nav-overlay {
                position: fixed;
                top: 0;
                left: 0;
                width: 100%;
                height: 100%;
                background: rgba(0, 0, 0, 0.7);
                backdrop-filter: blur(5px);
                z-index: 999;
                opacity: 0;
                visibility: hidden;
                transition: var(--transition);
            }

            .nav-overlay.active {
                opacity: 1;
                visibility: visible;
            }

            nav ul {
                flex-direction: column;
                gap: 30px;
                width: 100%;
                padding: 0 40px;
            }

            nav ul li {
                width: 100%;
                text-align: center;
            }

            nav ul li a {
                font-size: 1.5rem;
                display: block;
            }

            .btn-whatsapp-nav {
                margin-top: 20px;
                width: 100%;
            }

            .hero h1 {
                font-size: 2.8rem;
            }

            .hero-btns {
                flex-direction: column;
                gap: 15px;
            }

            .btn {
                width: 100%;
            }

            .section-title {
                font-size: 2rem;
            }

            .cta h2 {
                font-size: 2.2rem;
            }
        }

        @media (max-width: 480px) {
            .hero h1 {
                font-size: 2.2rem;
            }

            .hero p {
                font-size: 1rem;
            }

            .service-card {
                padding: 40px 20px;
            }

            .gallery-grid {
                grid-template-columns: 1fr;
            }

            .floating-buttons {
                bottom: 20px;
                right: 20px;
            }

            .btn-floating {
                width: 50px;
                height: 50px;
                font-size: 1.5rem;
            }
        }

        /* Floating Buttons */
        .floating-buttons {
            position: fixed;
            bottom: 30px;
            right: 30px;
            display: flex;
            flex-direction: column;
            gap: 15px;
            z-index: 999;
        }

        .btn-floating {
            width: 55px;
            height: 55px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.8rem;
            color: white;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.4);
            transition: var(--transition);
        }

        .btn-floating:hover {
            transform: translateY(-5px) scale(1.05);
            box-shadow: 0 8px 25px rgba(0, 0, 0, 0.5);
            color: white;
        }

        .btn-instagram {
            background: linear-gradient(45deg, #f09433 0%, #e6683c 25%, #dc2743 50%, #cc2366 75%, #bc1888 100%);
        }

        .btn-instagram:hover {
            box-shadow: 0 8px 25px rgba(220, 39, 67, 0.4);
        }

        .btn-location {
            background-color: #EA4335;
        }

        .btn-location:hover {
            background-color: #d33828;
            box-shadow: 0 8px 25px rgba(234, 67, 53, 0.4);
        }
    </style>
</head>

<body>

    <!-- Header -->
    <header id="header">
        <a href="#" class="logo">
            <i class="fa-solid fa-mobile-screen-button"></i> JP<span>Cell</span>
        </a>

        <div class="menu-toggle" id="mobile-menu">
            <i class="fa-solid fa-bars"></i>
        </div>

        <div class="nav-overlay" id="nav-overlay"></div>

        <nav id="nav-menu">
            <ul>
                <li><a href="#inicio" class="nav-link">Início</a></li>
                <li><a href="#servicos" class="nav-link">Serviços</a></li>
                <li><a href="#produtos" class="nav-link">Produtos</a></li>
                <li><a href="#contato" class="nav-link">Contato</a></li>
                <li>
                    <a href="https://wa.me/558499954417" target="_blank" class="btn btn-whatsapp btn-whatsapp-nav">
                        <i class="fa-brands fa-whatsapp"></i> WhatsApp
                    </a>
                </li>
            </ul>
        </nav>
    </header>

    <!-- Hero Section -->
    <section id="inicio" class="hero">
        <div class="hero-content">
            <h1>Seu celular novo ou consertado com <span>quem entende.</span></h1>
            <p>Venda de celulares, acessórios e assistência técnica especializada. Referência em qualidade e confiança.
            </p>
            <div class="hero-btns">
                <a href="#contato" class="btn btn-primary">
                    <i class="fa-solid fa-clipboard-list"></i> Fazer Orçamento
                </a>
                <a href="https://wa.me/558499954417" target="_blank" class="btn btn-outline">
                    <i class="fa-brands fa-whatsapp"></i> Falar no WhatsApp
                </a>
            </div>
        </div>
    </section>

    <!-- Services Section -->
    <section id="servicos" class="section services">
        <h2 class="section-title reveal">Nossos <span>Serviços</span></h2>

        <div class="services-grid">
            <!-- Service 1 -->
            <div class="service-card reveal delay-1">
                <div class="service-icon">
                    <i class="fa-solid fa-screwdriver-wrench"></i>
                </div>
                <h3>Assistência Técnica</h3>
                <p>Troca de tela, bateria, conectores, banho químico e reparos avançados em placas para todas as marcas.
                </p>
            </div>

            <!-- Service 2 -->
            <div class="service-card reveal delay-2">
                <div class="service-icon">
                    <i class="fa-solid fa-mobile-screen"></i>
                </div>
                <h3>Venda de Celulares</h3>
                <p>Smartphones novos e seminovos das melhores marcas com garantia, procedência e os melhores preços.</p>
            </div>

            <!-- Service 3 -->
            <div class="service-card reveal delay-3">
                <div class="service-icon">
                    <i class="fa-solid fa-headphones-simple"></i>
                </div>
                <h3>Acessórios</h3>
                <p>Capinhas, películas 3D/Privacidade, carregadores turbo, cabos originais, fones bluetooth e muito
                    mais.</p>
            </div>
        </div>
    </section>

    <!-- Differentials Section -->
    <section class="differentials">
        <div class="diff-grid">
            <div class="diff-item reveal">
                <i class="fa-solid fa-bolt icon"></i>
                <h4>Reparo Rápido</h4>
                <p>Consertos ágeis para você não ficar desconectado. A maioria dos reparos é levada a termo no mesmo
                    dia.</p>
            </div>
            <div class="diff-item reveal delay-1">
                <i class="fa-solid fa-user-gear icon"></i>
                <h4>Técnicos Especializados</h4>
                <p>Profissionais capacitados e em constante atualização para diagnosticar e resolver problemas com
                    precisão.</p>
            </div>
            <div class="diff-item reveal delay-2">
                <i class="fa-solid fa-shield-halved icon"></i>
                <h4>Garantia no Serviço</h4>
                <p>Todos os nossos reparos contam com garantia assegurada, para oferecer a você a máxima tranquilidade.
                </p>
            </div>
            <div class="diff-item reveal delay-3">
                <i class="fa-solid fa-microchip icon"></i>
                <h4>Peças de Qualidade</h4>
                <p>Utilizamos apenas componentes originais ou de primeira linha, visando o máximo desempenho do seu
                    aparelho.</p>
            </div>
        </div>
    </section>

    <!-- Gallery / Products Section -->
    <section id="produtos" class="section">
        <h2 class="section-title reveal">Nossa <span>Galeria</span></h2>

        <div class="gallery-grid">
            <!-- Galeria 1: Celulares -->
            <div class="gallery-item reveal delay-1">
                <img src="celulares.png"
                    alt="Smartphones novos e seminovos">
                <div class="gallery-overlay">
                    <h3>Celulares</h3>
                </div>
            </div>

            <!-- Galeria 2: Acessórios -->
            <div class="gallery-item reveal delay-2">
                <img src="acessorios.jpeg"
                    alt="Acessórios e fones">
                <div class="gallery-overlay">
                    <h3>Acessórios</h3>
                </div>
            </div>

            <!-- Galeria 3: Assistência -->
            <div class="gallery-item reveal delay-3">
                <img src="assistencia tecnica.png"
                    alt="Técnico realizando reparo em um celular">
                <div class="gallery-overlay">
                    <h3>Assistência Técnica</h3>
                </div>
            </div>

            <!-- Galeria 4: Loja -->
            <div class="gallery-item reveal delay-1">
                <img src="loja.jpeg"
                    alt="Faixada da Loja JP Cell">
                <div class="gallery-overlay">
                    <h3>Nossa Loja</h3>
                </div>
            </div>
        </div>
    </section>

    <!-- CTA Section -->
    <section class="cta reveal">
        <div class="cta-content">
            <h2>Quebrou seu celular?</h2>
            <p>Traga seu aparelho para a JP Cell. Orçamento rápido, transparente e com a qualidade que seu smartphone
                merece.</p>
            <a href="https://wa.me/558499954417" target="_blank" class="btn btn-whatsapp btn-large">
                <i class="fa-brands fa-whatsapp"></i> Solicitar Orçamento no WhatsApp
            </a>
        </div>
    </section>

    <!-- Footer -->
    <footer id="contato">
        <div class="footer-grid">
            <div class="footer-col reveal">
                <a href="#" class="logo" style="margin-bottom: 20px;">
                    <i class="fa-solid fa-mobile-screen-button"></i> JP<span>Cell</span>
                </a>
                <p>Especialistas em fazer seu celular voltar a ser novo. Venda, acessórios e assistência técnica de
                    confiança.</p>
                <div class="social-links">
                    <a href="https://www.instagram.com/jp.cell96/" target="_blank" rel="noopener noreferrer"
                        aria-label="Instagram"><i class="fa-brands fa-instagram"></i></a>
                    <a href="#" aria-label="Facebook"><i class="fa-brands fa-facebook-f"></i></a>
                    <a href="https://wa.me/558499954417" target="_blank" rel="noopener noreferrer"
                        aria-label="WhatsApp"><i class="fa-brands fa-whatsapp"></i></a>
                </div>
            </div>

            <div class="footer-col reveal delay-1">
                <h3>Links Rápidos</h3>
                <ul>
                    <li><a href="#inicio">Início</a></li>
                    <li><a href="#servicos">Nossos Serviços</a></li>
                    <li><a href="#produtos">Produtos e Galeria</a></li>
                    <li><a href="#contato">Fale Conosco</a></li>
                </ul>
            </div>

            <div class="footer-col reveal delay-2">
                <h3>Contato</h3>
                <ul class="contact-info">
                    <li><i class="fa-solid fa-location-dot"></i> Av. Brg. Trompowsky, 992 - Monte Castelo, Parnamirim -
                        RN, 59146-260</li>
                    <li><i class="fa-brands fa-whatsapp"></i> (84) 99995-4417</li>
                    <li><i class="fa-solid fa-envelope"></i> jpcellparnamirim@gmail.com</li>
                    <li><i class="fa-solid fa-clock"></i> Seg a Sex: 08h às 18h | Sáb: 08h às 12h</li>
                </ul>
            </div>
        </div>

        <div class="footer-bottom reveal delay-3">
            <p><strong>&copy; 2026 JP Cell &mdash; Todos os direitos reservados</strong></p>
        </div>
    </footer>

    <!-- Floating Buttons -->
    <div class="floating-buttons">
        <a href="https://www.instagram.com/jp.cell96/" target="_blank" rel="noopener noreferrer"
            class="btn-floating btn-instagram" aria-label="Instagram">
            <i class="fa-brands fa-instagram"></i>
        </a>
        <a href="https://www.google.com/maps/place/JP+Cell+Monte+Castelo+-+Assist%C3%AAncia+T%C3%A9cnica+e+Acess%C3%B3rios/@-5.9071394,-35.2692043,21z/data=!4m15!1m8!3m7!1s0x7b25702a8611195:0x2fa03df4a944d209!2sAv.+Brg.+Trompowsky,+992+-+Monte+Castelo,+Parnamirim+-+RN,+59146-260!3b1!8m2!3d-5.9070764!4d-35.2691771!16s%2Fg%2F11fy9zgqsp!3m5!1s0x7b257565b3500db:0x52ceee38cfaf8eba!8m2!3d-5.9070764!4d-35.2691771!16s%2Fg%2F11wr6ns09_?hl=pt-BR&entry=ttu&g_ep=EgoyMDI2MDMxMS4wIKXMDSoASAFQAw%3D%3D"
            target="_blank" rel="noopener noreferrer" class="btn-floating btn-location" aria-label="Localização">
            <i class="fa-solid fa-location-dot"></i>
        </a>
    </div>

    <!-- Scripts -->
    <script>
        document.addEventListener('DOMContentLoaded', () => {
            // Header Scroll Effect
            const header = document.getElementById('header');

            window.addEventListener('scroll', () => {
                if (window.scrollY > 50) {
                    header.classList.add('scrolled');
                } else {
                    header.classList.remove('scrolled');
                }
            });

            // Mobile Menu Toggle
            const mobileMenuBtn = document.getElementById('mobile-menu');
            const navMenu = document.getElementById('nav-menu');
            const navOverlay = document.getElementById('nav-overlay');
            const navLinks = document.querySelectorAll('.nav-link');

            function toggleMenu() {
                navMenu.classList.toggle('active');
                navOverlay.classList.toggle('active');
                const icon = mobileMenuBtn.querySelector('i');
                if (navMenu.classList.contains('active')) {
                    icon.classList.remove('fa-bars');
                    icon.classList.add('fa-xmark');
                } else {
                    icon.classList.remove('fa-xmark');
                    icon.classList.add('fa-bars');
                }
            }

            mobileMenuBtn.addEventListener('click', toggleMenu);
            navOverlay.addEventListener('click', toggleMenu);

            navLinks.forEach(link => {
                link.addEventListener('click', () => {
                    if (navMenu.classList.contains('active')) {
                        toggleMenu();
                    }
                });
            });

            // Scroll Reveal Animation (Intersection Observer)
            const revealElements = document.querySelectorAll('.reveal');

            const revealOptions = {
                threshold: 0.15,
                rootMargin: "0px 0px -50px 0px"
            };

            const revealObserver = new IntersectionObserver((entries, observer) => {
                entries.forEach(entry => {
                    if (entry.isIntersecting) {
                        entry.target.classList.add('active');
                        observer.unobserve(entry.target); // Optional: Stop observing once revealed
                    }
                });
            }, revealOptions);

            revealElements.forEach(el => {
                revealObserver.observe(el);
            });
        });
    </script>
</body>

</html>
