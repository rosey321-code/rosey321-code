<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Warda Riffat | Software Engineer & AI Automation Specialist</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <style>
        /* ==================== RESET & BASE STYLES ==================== */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        :root {
            --primary-color: #FF4500;
            --secondary-color: #00ADB5;
            --dark-bg: #0d1117;
            --light-bg: #161b22;
            --text-color: #ffffff;
            --text-muted: #8b949e;
            --border-color: #30363d;
            --success-color: #28a745;
            --gradient-1: linear-gradient(135deg, #FF4500 0%, #00ADB5 100%);
            --gradient-2: linear-gradient(135deg, #00ADB5 0%, #FF4500 100%);
            --shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
            --transition: all 0.3s ease;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            font-family: 'Poppins', sans-serif;
            background-color: var(--dark-bg);
            color: var(--text-color);
            line-height: 1.6;
            overflow-x: hidden;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        .section-title {
            text-align: center;
            font-size: 2.5rem;
            margin-bottom: 3rem;
            position: relative;
            background: var(--gradient-1);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .section-title::after {
            content: '';
            position: absolute;
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
            width: 100px;
            height: 3px;
            background: var(--gradient-1);
            border-radius: 2px;
        }

        /* ==================== NAVIGATION ==================== */
        .navbar {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            background: rgba(13, 17, 23, 0.95);
            backdrop-filter: blur(10px);
            z-index: 1000;
            padding: 1rem 0;
            border-bottom: 1px solid var(--border-color);
        }

        .nav-container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-size: 1.8rem;
            font-weight: 700;
        }

        .logo-text {
            background: var(--gradient-1);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            padding: 10px 20px;
            border: 2px solid var(--primary-color);
            border-radius: 8px;
        }

        .nav-menu {
            display: flex;
            list-style: none;
            gap: 2rem;
        }

        .nav-menu a {
            color: var(--text-color);
            text-decoration: none;
            font-weight: 500;
            transition: var(--transition);
            position: relative;
        }

        .nav-menu a::after {
            content: '';
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 0;
            height: 2px;
            background: var(--gradient-1);
            transition: var(--transition);
        }

        .nav-menu a:hover::after {
            width: 100%;
        }

        .nav-menu a:hover {
            color: var(--primary-color);
        }

        .hamburger {
            display: none;
            cursor: pointer;
        }

        .bar {
            display: block;
            width: 25px;
            height: 3px;
            margin: 5px auto;
            background: var(--text-color);
            transition: var(--transition);
        }

        /* ==================== HERO SECTION ==================== */
        .hero {
            min-height: 100vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            padding: 100px 20px 50px;
            background: var(--dark-bg);
            position: relative;
            overflow: hidden;
        }

        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: radial-gradient(circle at 30% 50%, rgba(255, 69, 0, 0.1) 0%, transparent 50%),
                        radial-gradient(circle at 70% 50%, rgba(0, 173, 181, 0.1) 0%, transparent 50%);
            z-index: 0;
        }

        .hero-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 4rem;
            max-width: 1200px;
            width: 100%;
            z-index: 1;
            align-items: center;
        }

        .hero-text {
            animation: fadeInLeft 1s ease;
        }

        .greeting {
            font-size: 1.2rem;
            color: var(--primary-color);
            margin-bottom: 0.5rem;
        }

        .name {
            font-size: 3.5rem;
            font-weight: 700;
            background: var(--gradient-1);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            margin-bottom: 0.5rem;
        }

        .title {
            font-size: 1.5rem;
            color: var(--text-muted);
            margin-bottom: 1rem;
        }

        .typing-container {
            font-size: 1.2rem;
            color: var(--secondary-color);
            margin-bottom: 1.5rem;
            min-height: 30px;
        }

        .description {
            color: var(--text-muted);
            margin-bottom: 2rem;
            line-height: 1.8;
        }

        .hero-buttons {
            display: flex;
            gap: 1rem;
            margin-bottom: 2rem;
        }

        .btn {
            padding: 12px 30px;
            border-radius: 50px;
            text-decoration: none;
            font-weight: 600;
            transition: var(--transition);
            display: inline-block;
            border: none;
            cursor: pointer;
            font-size: 1rem;
        }

        .btn-primary {
            background: var(--gradient-1);
            color: white;
        }

        .btn-primary:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(255, 69, 0, 0.3);
        }

        .btn-secondary {
            background: transparent;
            color: var(--primary-color);
            border: 2px solid var(--primary-color);
        }

        .btn-secondary:hover {
            background: var(--primary-color);
            color: white;
            transform: translateY(-3px);
        }

        .social-links {
            display: flex;
            gap: 1rem;
        }

        .social-links a {
            width: 45px;
            height: 45px;
            border-radius: 50%;
            background: var(--light-bg);
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--text-color);
            font-size: 1.2rem;
            transition: var(--transition);
            border: 1px solid var(--border-color);
        }

        .social-links a:hover {
            background: var(--primary-color);
            transform: translateY(-3px);
        }

        .hero-image {
            animation: fadeInRight 1s ease;
        }

        .image-container {
            position: relative;
            width: 350px;
            height: 350px;
            margin: 0 auto;
        }

        .profile-img {
            width: 100%;
            height: 100%;
            border-radius: 50%;
            background: var(--gradient-1);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 10rem;
            color: white;
            position: relative;
            z-index: 2;
            box-shadow: var(--shadow);
        }

        .floating-icons {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
        }

        .float-icon {
            position: absolute;
            width: 60px;
            height: 60px;
            background: var(--light-bg);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.5rem;
            color: var(--primary-color);
            border: 2px solid var(--primary-color);
            animation: float 3s ease-in-out infinite;
        }

        .icon-1 { top: 0; left: 50%; animation-delay: 0s; }
        .icon-2 { top: 50%; right: 0; animation-delay: 0.5s; }
        .icon-3 { bottom: 0; left: 50%; animation-delay: 1s; }
        .icon-4 { top: 50%; left: 0; animation-delay: 1.5s; }

        .scroll-indicator {
            position: absolute;
            bottom: 30px;
            left: 50%;
            transform: translateX(-50%);
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 10px;
            color: var(--text-muted);
            animation: bounce 2s infinite;
        }

        /* ==================== ABOUT SECTION ==================== */
        .about {
            padding: 100px 0;
            background: var(--light-bg);
        }

        .about-content {
            display: grid;
            grid-template-columns: 2fr 1fr;
            gap: 4rem;
            align-items: center;
        }

        .about-info p {
            color: var(--text-muted);
            margin-bottom: 1.5rem;
            line-height: 1.8;
        }

        .about-info strong {
            color: var(--primary-color);
        }

        .personal-info {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 1.5rem;
            margin-top: 2rem;
        }

        .info-item {
            display: flex;
            gap: 1rem;
            align-items: flex-start;
        }

        .info-item i {
            font-size: 1.5rem;
            color: var(--primary-color);
            width: 30px;
        }

        .info-item h4 {
            font-size: 1rem;
            margin-bottom: 0.3rem;
        }

        .info-item p {
            font-size: 0.9rem;
            color: var(--text-color);
            margin-bottom: 0.2rem;
        }

        .info-item span {
            font-size: 0.8rem;
            color: var(--text-muted);
        }

        .about-stats {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 1.5rem;
        }

        .stat-card {
            background: var(--dark-bg);
            padding: 2rem;
            border-radius: 15px;
            text-align: center;
            border: 1px solid var(--border-color);
            transition: var(--transition);
        }

        .stat-card:hover {
            transform: translateY(-5px);
            border-color: var(--primary-color);
        }

        .stat-card i {
            font-size: 2.5rem;
            color: var(--primary-color);
            margin-bottom: 1rem;
        }

        .stat-card h3 {
            font-size: 2.5rem;
            background: var(--gradient-1);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            margin-bottom: 0.5rem;
        }

        .stat-card p {
            color: var(--text-muted);
            font-size: 0.9rem;
        }

        /* ==================== SKILLS SECTION ==================== */
        .skills {
            padding: 100px 0;
            background: var(--dark-bg);
        }

        .skills-content {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 3rem;
        }

        .skills-category {
            background: var(--light-bg);
            padding: 2rem;
            border-radius: 15px;
            border: 1px solid var(--border-color);
        }

        .skills-category h3 {
            font-size: 1.3rem;
            margin-bottom: 1.5rem;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .skills-category h3 i {
            color: var(--primary-color);
        }

        .skill-bars {
            display: flex;
            flex-direction: column;
            gap: 1.5rem;
        }

        .skill-bar {
            width: 100%;
        }

        .skill-info {
            display: flex;
            justify-content: space-between;
            margin-bottom: 0.5rem;
            font-size: 0.9rem;
        }

        .skill-info span:first-child {
            color: var(--text-color);
        }

        .skill-info span:last-child {
            color: var(--primary-color);
        }

        .bar {
            width: 100%;
            height: 10px;
            background: var(--dark-bg);
            border-radius: 5px;
            overflow: hidden;
        }

        .progress {
            height: 100%;
            background: var(--gradient-1);
            border-radius: 5px;
            width: 0;
            transition: width 1.5s ease;
        }

        /* ==================== PROJECTS SECTION ==================== */
        .projects {
            padding: 100px 0;
            background: var(--light-bg);
        }

        .projects-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 2rem;
        }

        .project-card {
            background: var(--dark-bg);
            padding: 2rem;
            border-radius: 15px;
            border: 1px solid var(--border-color);
            transition: var(--transition);
        }

        .project-card:hover {
            transform: translateY(-10px);
            border-color: var(--primary-color);
            box-shadow: var(--shadow);
        }

        .project-icon {
            width: 70px;
            height: 70px;
            background: var(--gradient-1);
            border-radius: 15px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 2rem;
            color: white;
            margin-bottom: 1.5rem;
        }

        .project-card h3 {
            font-size: 1.3rem;
            margin-bottom: 1rem;
        }

        .project-card p {
            color: var(--text-muted);
            font-size: 0.9rem;
            margin-bottom: 1.5rem;
            line-height: 1.6;
        }

        .tech-stack {
            display: flex;
            flex-wrap: wrap;
            gap: 0.5rem;
            margin-bottom: 1.5rem;
        }

        .tech-stack span {
            background: var(--light-bg);
            padding: 5px 12px;
            border-radius: 20px;
            font-size: 0.8rem;
            color: var(--secondary-color);
            border: 1px solid var(--border-color);
        }

        .project-links {
            display: flex;
            gap: 1rem;
        }

        .btn-link {
            color: var(--primary-color);
            text-decoration: none;
            font-size: 0.9rem;
            display: flex;
            align-items: center;
            gap: 5px;
            transition: var(--transition);
        }

        .btn-link:hover {
            color: var(--secondary-color);
        }

        /* ==================== EXPERIENCE SECTION ==================== */
        .experience {
            padding: 100px 0;
            background: var(--dark-bg);
        }

        .timeline {
            position: relative;
            max-width: 800px;
            margin: 0 auto;
        }

        .timeline::before {
            content: '';
            position: absolute;
            left: 50%;
            transform: translateX(-50%);
            width: 2px;
            height: 100%;
            background: var(--gradient-1);
        }

        .timeline-item {
            display: flex;
            justify-content: flex-end;
            padding-right: 50px;
            position: relative;
            margin-bottom: 3rem;
            width: 50%;
        }

        .timeline-item:nth-child(even) {
            justify-content: flex-start;
            padding-right: 0;
            padding-left: 50px;
            margin-left: 50%;
        }

        .timeline-dot {
            position: absolute;
            right: -8px;
            top: 0;
            width: 18px;
            height: 18px;
            background: var(--primary-color);
            border-radius: 50%;
            border: 3px solid var(--dark-bg);
        }

        .timeline-item:nth-child(even) .timeline-dot {
            right: auto;
            left: -8px;
        }

        .timeline-content {
            background: var(--light-bg);
            padding: 2rem;
            border-radius: 15px;
            border: 1px solid var(--border-color);
            max-width: 400px;
            transition: var(--transition);
        }

        .timeline-content:hover {
            border-color: var(--primary-color);
            transform: translateX(-5px);
        }

        .timeline-item:nth-child(even) .timeline-content:hover {
            transform: translateX(5px);
        }

        .timeline-date {
            display: inline-block;
            background: var(--gradient-1);
            padding: 5px 15px;
            border-radius: 20px;
            font-size: 0.85rem;
            font-weight: 600;
            margin-bottom: 1rem;
        }

        .timeline-content h3 {
            font-size: 1.2rem;
            margin-bottom: 0.5rem;
        }

        .timeline-content h4 {
            color: var(--secondary-color);
            font-size: 1rem;
            margin-bottom: 1rem;
            font-weight: 500;
        }

        .timeline-content ul {
            list-style: none;
        }

        .timeline-content ul li {
            color: var(--text-muted);
            font-size: 0.9rem;
            margin-bottom: 0.5rem;
            padding-left: 1.5rem;
            position: relative;
        }

        .timeline-content ul li::before {
            content: '▸';
            position: absolute;
            left: 0;
            color: var(--primary-color);
        }

        /* ==================== CERTIFICATIONS SECTION ==================== */
        .certifications {
            padding: 100px 0;
            background: var(--light-bg);
        }

        .cert-grid {
            display: grid;
            grid-template-columns: repeat(5, 1fr);
            gap: 1.5rem;
        }

        .cert-card {
            background: var(--dark-bg);
            padding: 2rem 1.5rem;
            border-radius: 15px;
            text-align: center;
            border: 1px solid var(--border-color);
            transition: var(--transition);
        }

        .cert-card:hover {
            transform: translateY(-5px);
            border-color: var(--primary-color);
        }

        .cert-card i {
            font-size: 2.5rem;
            color: var(--primary-color);
            margin-bottom: 1rem;
        }

        .cert-card h4 {
            font-size: 1rem;
            margin-bottom: 0.5rem;
        }

        .cert-card p {
            color: var(--text-muted);
            font-size: 0.85rem;
        }

        /* ==================== WEBSITES SECTION ==================== */
        .websites {
            padding: 100px 0;
            background: var(--dark-bg);
        }

        .websites-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 2rem;
        }

        .website-card {
            background: var(--light-bg);
            padding: 2rem;
            border-radius: 15px;
            border: 1px solid var(--border-color);
            text-align: center;
            transition: var(--transition);
        }

        .website-card:hover {
            transform: translateY(-10px);
            border-color: var(--primary-color);
            box-shadow: var(--shadow);
        }

        .website-card i {
            font-size: 3rem;
            color: var(--primary-color);
            margin-bottom: 1rem;
        }

        .website-card h3 {
            font-size: 1.2rem;
            margin-bottom: 0.5rem;
        }

        .website-card p {
            color: var(--text-muted);
            font-size: 0.9rem;
            margin-bottom: 1.5rem;
        }

        /* ==================== CONTACT SECTION ==================== */
        .contact {
            padding: 100px 0;
            background: var(--dark-bg);
        }

        .contact-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 4rem;
        }

        .contact-info h3 {
            font-size: 1.8rem;
            margin-bottom: 1rem;
        }

        .contact-info > p {
            color: var(--text-muted);
            margin-bottom: 2rem;
        }

        .contact-details {
            display: flex;
            flex-direction: column;
            gap: 1.5rem;
            margin-bottom: 2rem;
        }

        .contact-item {
            display: flex;
            gap: 1rem;
            align-items: flex-start;
        }

        .contact-item i {
            font-size: 1.5rem;
            color: var(--primary-color);
            width: 30px;
        }

        .contact-item h4 {
            font-size: 1rem;
            margin-bottom: 0.3rem;
        }

        .contact-item a,
        .contact-item p {
            color: var(--text-muted);
            text-decoration: none;
            transition: var(--transition);
        }

        .contact-item a:hover {
            color: var(--primary-color);
        }

        .social-links-contact {
            display: flex;
            gap: 1rem;
        }

        .social-links-contact a {
            width: 50px;
            height: 50px;
            border-radius: 50%;
            background: var(--light-bg);
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--text-color);
            font-size: 1.3rem;
            transition: var(--transition);
            border: 1px solid var(--border-color);
        }

        .social-links-contact a:hover {
            background: var(--primary-color);
            transform: translateY(-3px);
        }

        .contact-form {
            background: var(--light-bg);
            padding: 2.5rem;
            border-radius: 15px;
            border: 1px solid var(--border-color);
        }

        .form-group {
            margin-bottom: 1.5rem;
        }

        .form-group input,
        .form-group textarea {
            width: 100%;
            padding: 15px;
            background: var(--dark-bg);
            border: 1px solid var(--border-color);
            border-radius: 8px;
            color: var(--text-color);
            font-family: 'Poppins', sans-serif;
            font-size: 1rem;
            transition: var(--transition);
        }

        .form-group input:focus,
        .form-group textarea:focus {
            outline: none;
            border-color: var(--primary-color);
        }

        .form-group textarea {
            resize: vertical;
        }

        /* ==================== FOOTER ==================== */
        .footer {
            background: var(--light-bg);
            padding: 50px 0 20px;
            border-top: 1px solid var(--border-color);
        }

        .footer-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 2rem;
            flex-wrap: wrap;
            gap: 2rem;
        }

        .footer-logo .logo-text {
            font-size: 1.5rem;
        }

        .footer-logo p {
            color: var(--text-muted);
            font-size: 0.9rem;
            margin-top: 0.5rem;
        }

        .footer-links {
            display: flex;
            gap: 2rem;
        }

        .footer-links a {
            color: var(--text-color);
            text-decoration: none;
            transition: var(--transition);
        }

        .footer-links a:hover {
            color: var(--primary-color);
        }

        .footer-social {
            display: flex;
            gap: 1rem;
        }

        .footer-social a {
            width: 40px;
            height: 40px;
            border-radius: 50%;
            background: var(--dark-bg);
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--text-color);
            transition: var(--transition);
            border: 1px solid var(--border-color);
        }

        .footer-social a:hover {
            background: var(--primary-color);
        }

        .footer-bottom {
            text-align: center;
            padding-top: 2rem;
            border-top: 1px solid var(--border-color);
        }

        .footer-bottom p {
            color: var(--text-muted);
            font-size: 0.9rem;
            margin-bottom: 0.5rem;
        }

        /* ==================== ANIMATIONS ==================== */
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

        @keyframes float {
            0%, 100% {
                transform: translateY(0);
            }
            50% {
                transform: translateY(-20px);
            }
        }

        @keyframes bounce {
            0%, 100% {
                transform: translateX(-50%) translateY(0);
            }
            50% {
                transform: translateX(-50%) translateY(10px);
            }
        }

        /* ==================== RESPONSIVE DESIGN ==================== */
        @media (max-width: 992px) {
            .hero-content {
                grid-template-columns: 1fr;
                text-align: center;
            }

            .hero-text {
                order: 2;
            }

            .hero-image {
                order: 1;
            }

            .hero-buttons {
                justify-content: center;
            }

            .social-links {
                justify-content: center;
            }

            .about-content {
                grid-template-columns: 1fr;
            }

            .skills-content {
                grid-template-columns: 1fr;
            }

            .projects-grid {
                grid-template-columns: repeat(2, 1fr);
            }

            .cert-grid {
                grid-template-columns: repeat(3, 1fr);
            }

            .websites-grid {
                grid-template-columns: 1fr;
            }

            .timeline::before {
                left: 20px;
            }

            .timeline-item {
                width: 100%;
                padding-right: 50px;
                padding-left: 50px;
                justify-content: flex-start;
            }

            .timeline-item:nth-child(even) {
                margin-left: 0;
                padding-left: 50px;
            }

            .timeline-dot {
                left: 11px !important;
                right: auto !important;
            }

            .timeline-content {
                max-width: 100%;
            }

            .contact-content {
                grid-template-columns: 1fr;
            }
        }

        @media (max-width: 768px) {
            .nav-menu {
                position: fixed;
                left: -100%;
                top: 70px;
                flex-direction: column;
                background: var(--light-bg);
                width: 100%;
                text-align: center;
                transition: var(--transition);
                padding: 2rem 0;
                border-bottom: 1px solid var(--border-color);
            }

            .nav-menu.active {
                left: 0;
            }

            .hamburger {
                display: block;
            }

            .hamburger.active .bar:nth-child(2) {
                opacity: 0;
            }

            .hamburger.active .bar:nth-child(1) {
                transform: translateY(8px) rotate(45deg);
            }

            .hamburger.active .bar:nth-child(3) {
                transform: translateY(-8px) rotate(-45deg);
            }

            .name {
                font-size: 2.5rem;
            }

            .title {
                font-size: 1.2rem;
            }

            .image-container {
                width: 280px;
                height: 280px;
            }

            .profile-img {
                font-size: 8rem;
            }

            .personal-info {
                grid-template-columns: 1fr;
            }

            .projects-grid {
                grid-template-columns: 1fr;
            }

            .cert-grid {
                grid-template-columns: repeat(2, 1fr);
            }

            .footer-content {
                flex-direction: column;
                text-align: center;
            }

            .footer-links {
                flex-wrap: wrap;
                justify-content: center;
            }
        }

        @media (max-width: 480px) {
            .hero-buttons {
                flex-direction: column;
            }

            .btn {
                width: 100%;
                text-align: center;
            }

            .about-stats {
                grid-template-columns: 1fr;
            }

            .cert-grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <!-- Navigation -->
    <nav class="navbar">
        <div class="nav-container">
            <div class="logo">
                <span class="logo-text">WR</span>
            </div>
            <ul class="nav-menu">
                <li><a href="#home">Home</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#skills">Skills</a></li>
                <li><a href="#projects">Projects</a></li>
                <li><a href="#experience">Experience</a></li>
                <li><a href="#websites">Websites</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
            <div class="hamburger">
                <span class="bar"></span>
                <span class="bar"></span>
                <span class="bar"></span>
            </div>
        </div>
    </nav>

    <!-- Hero Section -->
    <section id="home" class="hero">
        <div class="hero-content">
            <div class="hero-text">
                <p class="greeting">Hello, I'm</p>
                <h1 class="name">Warda Riffat</h1>
                <h2 class="title">Software Engineering Student</h2>
                <div class="typing-container">
                    <span class="typing-text"></span>
                </div>
                <p class="description">
                    A dedicated Software Engineering student with a comprehensive skill set spanning 
                    WordPress development, AI automation, digital marketing, and graphic design. 
                    Highly proficient in developing websites from conception to launch, implementing 
                    robust automation workflows (n8n), and managing client communication.
                </p>
                <div class="hero-buttons">
                    <a href="#contact" class="btn btn-primary">Hire Me</a>
                    <a href="#projects" class="btn btn-secondary">View Work</a>
                </div>
                <div class="social-links">
                    <a href="mailto:wardariffat1@gmail.com"><i class="fas fa-envelope"></i></a>
                    <a href="https://linkedin.com/in/warda-riffat-556731317" target="_blank"><i class="fab fa-linkedin"></i></a>
                    <a href="https://wa.me/923255585309" target="_blank"><i class="fab fa-whatsapp"></i></a>
                    <a href="https://github.com/wardariffat" target="_blank"><i class="fab fa-github"></i></a>
                </div>
            </div>
            <div class="hero-image">
                <div class="image-container">
                    <div class="profile-img">
                        <i class="fas fa-user-circle"></i>
                    </div>
                    <div class="floating-icons">
                        <div class="float-icon icon-1"><i class="fab fa-wordpress"></i></div>
                        <div class="float-icon icon-2"><i class="fas fa-robot"></i></div>
                        <div class="float-icon icon-3"><i class="fab fa-python"></i></div>
                        <div class="float-icon icon-4"><i class="fas fa-database"></i></div>
                    </div>
                </div>
            </div>
        </div>
        <div class="scroll-indicator">
            <span>Scroll Down</span>
            <i class="fas fa-chevron-down"></i>
        </div>
    </section>

    <!-- About Section -->
    <section id="about" class="about">
        <div class="container">
            <h2 class="section-title">About Me</h2>
            <div class="about-content">
                <div class="about-info">
                    <p>
                        I'm a dedicated <strong>Software Engineering student</strong> with a comprehensive skill set 
                        spanning <strong>WordPress development</strong>, <strong>AI automation</strong>, 
                        <strong>digital marketing</strong>, and <strong>graphic design</strong>.
                    </p>
                    <p>
                        Highly proficient in developing websites from conception to launch, implementing 
                        robust automation workflows using <strong>n8n</strong>, and managing client communication. 
                        I possess strong problem-solving skills with experience in identifying and resolving 
                        technical issues across different platforms.
                    </p>
                    <div class="personal-info">
                        <div class="info-item">
                            <i class="fas fa-graduation-cap"></i>
                            <div>
                                <h4>Education</h4>
                                <p>BS Software Engineering (2027)</p>
                                <span>GPA: 3.66/4.0</span>
                            </div>
                        </div>
                        <div class="info-item">
                            <i class="fas fa-map-marker-alt"></i>
                            <div>
                                <h4>Location</h4>
                                <p>Rawalpindi, Pakistan</p>
                                <span>Available Remote Worldwide</span>
                            </div>
                        </div>
                        <div class="info-item">
                            <i class="fas fa-envelope"></i>
                            <div>
                                <h4>Email</h4>
                                <p>wardariffat1@gmail.com</p>
                                <span>Available for Hire</span>
                            </div>
                        </div>
                        <div class="info-item">
                            <i class="fas fa-phone"></i>
                            <div>
                                <h4>Phone</h4>
                                <p>+92 325 5585309</p>
                                <span>WhatsApp Available</span>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="about-stats">
                    <div class="stat-card">
                        <i class="fas fa-project-diagram"></i>
                        <h3 class="counter" data-target="10">0</h3>
                        <p>Projects Completed</p>
                    </div>
                    <div class="stat-card">
                        <i class="fas fa-users"></i>
                        <h3 class="counter" data-target="15">0</h3>
                        <p>Happy Clients</p>
                    </div>
                    <div class="stat-card">
                        <i class="fas fa-code"></i>
                        <h3 class="counter" data-target="5">0</h3>
                        <p>Years Learning</p>
                    </div>
                    <div class="stat-card">
                        <i class="fas fa-certificate"></i>
                        <h3 class="counter" data-target="5">0</h3>
                        <p>Certifications</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Skills Section -->
    <section id="skills" class="skills">
        <div class="container">
            <h2 class="section-title">Technical Skills</h2>
            <div class="skills-content">
                <div class="skills-category">
                    <h3><i class="fas fa-code"></i> Programming Languages</h3>
                    <div class="skill-bars">
                        <div class="skill-bar">
                            <div class="skill-info">
                                <span>Python</span>
                                <span>85%</span>
                            </div>
                            <div class="bar">
                                <div class="progress" data-width="85%"></div>
                            </div>
                        </div>
                        <div class="skill-bar">
                            <div class="skill-info">
                                <span>JavaScript</span>
                                <span>75%</span>
                            </div>
                            <div class="bar">
                                <div class="progress" data-width="75%"></div>
                            </div>
                        </div>
                        <div class="skill-bar">
                            <div class="skill-info">
                                <span>PHP</span>
                                <span>80%</span>
                            </div>
                            <div class="bar">
                                <div class="progress" data-width="80%"></div>
                            </div>
                        </div>
                        <div class="skill-bar">
                            <div class="skill-info">
                                <span>Java</span>
                                <span>70%</span>
                            </div>
                            <div class="bar">
                                <div class="progress" data-width="70%"></div>
                            </div>
                        </div>
                        <div class="skill-bar">
                            <div class="skill-info">
                                <span>C/C++</span>
                                <span>65%</span>
                            </div>
                            <div class="bar">
                                <div class="progress" data-width="65%"></div>
                            </div>
                        </div>
                    </div>
                </div>

                <div class="skills-category">
                    <h3><i class="fab fa-wordpress"></i> Web & CMS</h3>
                    <div class="skill-bars">
                        <div class="skill-bar">
                            <div class="skill-info">
                                <span>WordPress</span>
                                <span>95%</span>
                            </div>
                            <div class="bar">
                                <div class="progress" data-width="95%"></div>
                            </div>
                        </div>
                        <div class="skill-bar">
                            <div class="skill-info">
                                <span>HTML5/CSS3</span>
                                <span>90%</span>
                            </div>
                            <div class="bar">
                                <div class="progress" data-width="90%"></div>
                            </div>
                        </div>
                        <div class="skill-bar">
                            <div class="skill-info">
                                <span>WooCommerce</span>
                                <span>85%</span>
                            </div>
                            <div class="bar">
                                <div class="progress" data-width="85%"></div>
                            </div>
                        </div>
                        <div class="skill-bar">
                            <div class="skill-info">
                                <span>Elementor</span>
                                <span>90%</span>
                            </div>
                            <div class="bar">
                                <div class="progress" data-width="90%"></div>
                            </div>
                        </div>
                        <div class="skill-bar">
                            <div class="skill-info">
                                <span>MySQL</span>
                                <span>75%</span>
                            </div>
                            <div class="bar">
                                <div class="progress" data-width="75%"></div>
                            </div>
                        </div>
                    </div>
                </div>

                <div class="skills-category">
                    <h3><i class="fas fa-robot"></i> AI & Automation</h3>
                    <div class="skill-bars">
                        <div class="skill-bar">
                            <div class="skill-info">
                                <span>n8n Automation</span>
                                <span>90%</span>
                            </div>
                            <div class="bar">
                                <div class="progress" data-width="90%"></div>
                            </div>
                        </div>
                        <div class="skill-bar">
                            <div class="skill-info">
                                <span>YOLO (v5/v8)</span>
                                <span>80%</span>
                            </div>
                            <div class="bar">
                                <div class="progress" data-width="80%"></div>
                            </div>
                        </div>
                        <div class="skill-bar">
                            <div class="skill-info">
                                <span>Google Gemini AI</span>
                                <span>85%</span>
                            </div>
                            <div class="bar">
                                <div class="progress" data-width="85%"></div>
                            </div>
                        </div>
                        <div class="skill-bar">
                            <div class="skill-info">
                                <span>OpenCV</span>
                                <span>75%</span>
                            </div>
                            <div class="bar">
                                <div class="progress" data-width="75%"></div>
                            </div>
                        </div>
                    </div>
                </div>

                <div class="skills-category">
                    <h3><i class="fas fa-chart-line"></i> Digital Marketing</h3>
                    <div class="skill-bars">
                        <div class="skill-bar">
                            <div class="skill-info">
                                <span>Google Analytics</span>
                                <span>80%</span>
                            </div>
                            <div class="bar">
                                <div class="progress" data-width="80%"></div>
                            </div>
                        </div>
                        <div class="skill-bar">
                            <div class="skill-info">
                                <span>Facebook Ads</span>
                                <span>75%</span>
                            </div>
                            <div class="bar">
                                <div class="progress" data-width="75%"></div>
                            </div>
                        </div>
                        <div class="skill-bar">
                            <div class="skill-info">
                                <span>Canva Design</span>
                                <span>85%</span>
                            </div>
                            <div class="bar">
                                <div class="progress" data-width="85%"></div>
                            </div>
                        </div>
                        <div class="skill-bar">
                            <div class="skill-info">
                                <span>Microsoft Office</span>
                                <span>90%</span>
                            </div>
                            <div class="bar">
                                <div class="progress" data-width="90%"></div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Projects Section -->
    <section id="projects" class="projects">
        <div class="container">
            <h2 class="section-title">Featured Projects</h2>
            <div class="projects-grid">
                <div class="project-card">
                    <div class="project-icon">
                        <i class="fab fa-whatsapp"></i>
                    </div>
                    <h3>WhatsApp AI Chatbot</h3>
                    <p>AI-powered WhatsApp chatbot to automate customer support using n8n workflow with Google Gemini integration for intelligent responses.</p>
                    <div class="tech-stack">
                        <span>n8n</span>
                        <span>Google Gemini</span>
                        <span>Google Sheets</span>
                        <span>Memory Node</span>
                    </div>
                    <div class="project-links">
                        <a href="https://chat.qwen.ai/s/deploy/t_26c47def-68e5-49d9-818d-b0e56e3cd771" target="_blank" class="btn-link">
                            <i class="fas fa-external-link-alt"></i> Live Demo
                        </a>
                    </div>
                </div>

                <div class="project-card">
                    <div class="project-icon">
                        <i class="fas fa-eye"></i>
                    </div>
                    <h3>YOLOv8 Object Detection</h3>
                    <p>Production-ready computer vision system with real-time detection, bounding boxes, confidence scores, and AI voice alerts.</p>
                    <div class="tech-stack">
                        <span>Python</span>
                        <span>YOLOv8</span>
                        <span>OpenCV</span>
                        <span>pyttsx3</span>
                    </div>
                    <div class="project-links">
                        <a href="#" class="btn-link">
                            <i class="fab fa-github"></i> View Code
                        </a>
                    </div>
                </div>

                <div class="project-card">
                    <div class="project-icon">
                        <i class="fas fa-video"></i>
                    </div>
                    <h3>YOLOv5 Real-Time Detection</h3>
                    <p>Live webcam detection system built on Google Colab with bounding box overlays and voice output alerts for real-time monitoring.</p>
                    <div class="tech-stack">
                        <span>Python</span>
                        <span>YOLOv5</span>
                        <span>OpenCV</span>
                        <span>Google Colab</span>
                    </div>
                    <div class="project-links">
                        <a href="#" class="btn-link">
                            <i class="fab fa-github"></i> View Code
                        </a>
                    </div>
                </div>

                <div class="project-card">
                    <div class="project-icon">
                        <i class="fab fa-wordpress"></i>
                    </div>
                    <h3>WordPress E-Commerce</h3>
                    <p>Responsive WordPress websites and e-commerce stores with WooCommerce configuration, payment gateways, and Elementor customization.</p>
                    <div class="tech-stack">
                        <span>WordPress</span>
                        <span>WooCommerce</span>
                        <span>Elementor</span>
                        <span>MySQL</span>
                    </div>
                    <div class="project-links">
                        <a href="https://roseydesigner.netlify.app/" target="_blank" class="btn-link">
                            <i class="fas fa-external-link-alt"></i> View Portfolio
                        </a>
                    </div>
                </div>

                <div class="project-card">
                    <div class="project-icon">
                        <i class="fas fa-cogs"></i>
                    </div>
                    <h3>n8n Automation Workflows</h3>
                    <p>Custom automation workflows connecting various APIs and services to streamline repetitive business processes for clients.</p>
                    <div class="tech-stack">
                        <span>n8n</span>
                        <span>API Integration</span>
                        <span>Webhooks</span>
                        <span>Automation</span>
                    </div>
                    <div class="project-links">
                        <a href="https://my-agentic-ai.netlify.app/" target="_blank" class="btn-link">
                            <i class="fas fa-external-link-alt"></i> Learn More
                        </a>
                    </div>
                </div>

                <div class="project-card">
                    <div class="project-icon">
                        <i class="fas fa-bullhorn"></i>
                    </div>
                    <h3>Digital Marketing Campaigns</h3>
                    <p>Complete digital marketing strategies including Google Analytics setup, Facebook Ads management, and social media content creation.</p>
                    <div class="tech-stack">
                        <span>Google Analytics</span>
                        <span>Facebook Ads</span>
                        <span>Meta Tags</span>
                        <span>Canva</span>
                    </div>
                    <div class="project-links">
                        <a href="#" class="btn-link">
                            <i class="fas fa-external-link-alt"></i> View Case Studies
                        </a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Experience Section -->
    <section id="experience" class="experience">
        <div class="container">
            <h2 class="section-title">Work Experience</h2>
            <div class="timeline">
                <div class="timeline-item">
                    <div class="timeline-dot"></div>
                    <div class="timeline-content">
                        <div class="timeline-date">2026</div>
                        <h3>Social Media Handler & Web Developer</h3>
                        <h4>Technospire Global Technologies</h4>
                        <ul>
                            <li>Managed social media platforms and created engaging content for advertising campaigns</li>
                            <li>Assisted in website development and maintenance tasks</li>
                            <li>Performed regular checks and updates for smooth website operation</li>
                        </ul>
                    </div>
                </div>

                <div class="timeline-item">
                    <div class="timeline-dot"></div>
                    <div class="timeline-content">
                        <div class="timeline-date">2025</div>
                        <h3>WordPress Development & Automation Intern</h3>
                        <h4>WebRabbit Agency</h4>
                        <ul>
                            <li>Designed and implemented n8n-based automation workflows</li>
                            <li>Managed client relationships and conducted requirement gathering meetings</li>
                            <li>Resolved technical bugs in live WordPress websites</li>
                            <li>Customized WordPress themes and plugins for clients</li>
                        </ul>
                    </div>
                </div>

                <div class="timeline-item">
                    <div class="timeline-dot"></div>
                    <div class="timeline-content">
                        <div class="timeline-date">2023</div>
                        <h3>WordPress Development Intern</h3>
                        <h4>EZITECH Institute</h4>
                        <ul>
                            <li>Designed and deployed responsive WordPress websites</li>
                            <li>Configured WooCommerce for product listings and payment gateways</li>
                            <li>Customized themes using Elementor</li>
                            <li>Implemented marketing strategies, GA4 setup, Facebook Ads</li>
                        </ul>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Certifications Section -->
    <section class="certifications">
        <div class="container">
            <h2 class="section-title">Certifications</h2>
            <div class="cert-grid">
                <div class="cert-card">
                    <i class="fab fa-wordpress"></i>
                    <h4>WordPress Development</h4>
                    <p>Learning With Earning</p>
                </div>
                <div class="cert-card">
                    <i class="fas fa-palette"></i>
                    <h4>Canva Design</h4>
                    <p>Learning With Earning</p>
                </div>
                <div class="cert-card">
                    <i class="fas fa-chart-line"></i>
                    <h4>WordPress + Digital Marketing</h4>
                    <p>Ezitech Institute</p>
                </div>
                <div class="cert-card">
                    <i class="fas fa-code"></i>
                    <h4>Web Development + Client Solutions</h4>
                    <p>WebRabbit Agency</p>
                </div>
                <div class="cert-card">
                    <i class="fas fa-bullhorn"></i>
                    <h4>Web Developer + Social Media Manager</h4>
                    <p>Technospire Global</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Websites Section -->
    <section id="websites" class="websites">
        <div class="container">
            <h2 class="section-title">My Websites</h2>
            <div class="websites-grid">
                <div class="website-card">
                    <i class="fas fa-robot"></i>
                    <h3>Agentic AI Portfolio</h3>
                    <p>AI Automation & Chatbot Showcase</p>
                    <a href="https://my-agentic-ai.netlify.app/" target="_blank" class="btn btn-primary">
                        <i class="fas fa-external-link-alt"></i> Visit
                    </a>
                </div>
                <div class="website-card">
                    <i class="fas fa-palette"></i>
                    <h3>Rosey Designer</h3>
                    <p>Design & WordPress Portfolio</p>
                    <a href="https://roseydesigner.netlify.app/" target="_blank" class="btn btn-primary">
                        <i class="fas fa-external-link-alt"></i> Visit
                    </a>
                </div>
                <div class="website-card">
                    <i class="fas fa-comments"></i>
                    <h3>AI Chatbot Demo</h3>
                    <p>WhatsApp AI Chatbot Live Demo</p>
                    <a href="https://chat.qwen.ai/s/deploy/t_26c47def-68e5-49d9-818d-b0e56e3cd771" target="_blank" class="btn btn-primary">
                        <i class="fas fa-external-link-alt"></i> Visit
                    </a>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="contact">
        <div class="container">
            <h2 class="section-title">Get In Touch</h2>
            <div class="contact-content">
                <div class="contact-info">
                    <h3>Let's Work Together</h3>
                    <p>I'm available for remote freelance projects, paid internships, and AI automation collaborations worldwide.</p>
                    
                    <div class="contact-details">
                        <div class="contact-item">
                            <i class="fas fa-envelope"></i>
                            <div>
                                <h4>Email</h4>
                                <a href="mailto:wardariffat1@gmail.com">wardariffat1@gmail.com</a>
                            </div>
                        </div>
                        <div class="contact-item">
                            <i class="fas fa-phone"></i>
                            <div>
                                <h4>Phone</h4>
                                <a href="tel:+923255585309">+92 325 5585309</a>
                            </div>
                        </div>
                        <div class="contact-item">
                            <i class="fab fa-whatsapp"></i>
                            <div>
                                <h4>WhatsApp</h4>
                                <a href="https://wa.me/923255585309" target="_blank">Chat on WhatsApp</a>
                            </div>
                        </div>
                        <div class="contact-item">
                            <i class="fas fa-map-marker-alt"></i>
                            <div>
                                <h4>Location</h4>
                                <p>Awan Colony, Rawalpindi, Pakistan</p>
                            </div>
                        </div>
                    </div>

                    <div class="social-links-contact">
                        <a href="https://linkedin.com/in/warda-riffat-556731317" target="_blank"><i class="fab fa-linkedin"></i></a>
                        <a href="https://github.com/wardariffat" target="_blank"><i class="fab fa-github"></i></a>
                        <a href="https://my-agentic-ai.netlify.app/" target="_blank"><i class="fas fa-globe"></i></a>
                    </div>
                </div>

                <div class="contact-form">
                    <form id="contactForm">
                        <div class="form-group">
                            <input type="text" id="name" name="name" placeholder="Your Name" required>
                        </div>
                        <div class="form-group">
                            <input type="email" id="email" name="email" placeholder="Your Email" required>
                        </div>
                        <div class="form-group">
                            <input type="text" id="subject" name="subject" placeholder="Subject" required>
                        </div>
                        <div class="form-group">
                            <textarea id="message" name="message" rows="5" placeholder="Your Message" required></textarea>
                        </div>
                        <button type="submit" class="btn btn-primary">Send Message</button>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="footer">
        <div class="container">
            <div class="footer-content">
                <div class="footer-logo">
                    <span class="logo-text">WR</span>
                    <p>Software Engineering Student</p>
                </div>
                <div class="footer-links">
                    <a href="#home">Home</a>
                    <a href="#about">About</a>
                    <a href="#skills">Skills</a>
                    <a href="#projects">Projects</a>
                    <a href="#contact">Contact</a>
                </div>
                <div class="footer-social">
                    <a href="mailto:wardariffat1@gmail.com"><i class="fas fa-envelope"></i></a>
                    <a href="https://linkedin.com/in/warda-riffat-556731317" target="_blank"><i class="fab fa-linkedin"></i></a>
                    <a href="https://github.com/wardariffat" target="_blank"><i class="fab fa-github"></i></a>
                </div>
            </div>
            <div class="footer-bottom">
                <p>&copy; 2026 Warda Riffat. All Rights Reserved.</p>
                <p>"Automating the boring stuff so humans can focus on what matters."</p>
            </div>
        </div>
    </footer>

    <script>
        // ==================== NAVIGATION TOGGLE ====================
        const hamburger = document.querySelector('.hamburger');
        const navMenu = document.querySelector('.nav-menu');

        hamburger.addEventListener('click', () => {
            hamburger.classList.toggle('active');
            navMenu.classList.toggle('active');
        });

        document.querySelectorAll('.nav-menu a').forEach(link => {
            link.addEventListener('click', () => {
                hamburger.classList.remove('active');
                navMenu.classList.remove('active');
            });
        });

        // ==================== TYPING ANIMATION ====================
        const typingText = document.querySelector('.typing-text');
        const phrases = [
            'AI Automation Specialist 🤖',
            'n8n Workflow Expert ⚡',
            'WordPress Developer 🛒',
            'YOLO Object Detection Engineer 👁️',
            'WhatsApp AI Chatbot Builder 💬'
        ];

        let phraseIndex = 0;
        let charIndex = 0;
        let isDeleting = false;
        let typingSpeed = 100;

        function type() {
            const currentPhrase = phrases[phraseIndex];
            
            if (isDeleting) {
                typingText.textContent = currentPhrase.substring(0, charIndex - 1);
                charIndex--;
                typingSpeed = 50;
            } else {
                typingText.textContent = currentPhrase.substring(0, charIndex + 1);
                charIndex++;
                typingSpeed = 100;
            }

            if (!isDeleting && charIndex === currentPhrase.length) {
                isDeleting = true;
                typingSpeed = 2000;
            } else if (isDeleting && charIndex === 0) {
                isDeleting = false;
                phraseIndex = (phraseIndex + 1) % phrases.length;
                typingSpeed = 500;
            }

            setTimeout(type, typingSpeed);
        }

        document.addEventListener('DOMContentLoaded', type);

        // ==================== SKILL BARS ANIMATION ====================
        const skillBars = document.querySelectorAll('.progress');

        const observerOptions = {
            threshold: 0.5
        };

        const skillObserver = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    const bar = entry.target;
                    bar.style.width = bar.getAttribute('data-width');
                }
            });
        }, observerOptions);

        skillBars.forEach(bar => {
            skillObserver.observe(bar);
        });

        // ==================== COUNTER ANIMATION ====================
        const counters = document.querySelectorAll('.counter');

        const counterObserver = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    const counter = entry.target;
                    const target = parseInt(counter.getAttribute('data-target'));
                    const duration = 2000;
                    const increment = target / (duration / 16);
                    let current = 0;

                    const updateCounter = () => {
                        current += increment;
                        if (current < target) {
                            counter.textContent = Math.ceil(current);
                            setTimeout(updateCounter, 16);
                        } else {
                            counter.textContent = target + '+';
                        }
                    };

                    updateCounter();
                    counterObserver.unobserve(counter);
                }
            });
        }, observerOptions);

        counters.forEach(counter => {
            counterObserver.observe(counter);
        });

        // ==================== SMOOTH SCROLL ====================
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({
                        behavior: 'smooth',
                        block: 'start'
                    });
                }
            });
        });

        // ==================== CONTACT FORM ====================
        const contactForm = document.getElementById('contactForm');

        contactForm.addEventListener('submit', (e) => {
            e.preventDefault();
            
            const name = document.getElementById('name').value;
            const email = document.getElementById('email').value;
            const subject = document.getElementById('subject').value;
            const message = document.getElementById('message').value;

            const mailtoLink = `mailto:wardariffat1@gmail.com?subject=${encodeURIComponent(subject)}&body=${encodeURIComponent('Name: ' + name + '\nEmail: ' + email + '\n\n' + message)}`;
            
            window.location.href = mailtoLink;
            
            alert('Thank you for your message! Your email client will open to send the message.');
            
            contactForm.reset();
        });

        // ==================== NAVBAR SCROLL EFFECT ====================
        window.addEventListener('scroll', () => {
            const navbar = document.querySelector('.navbar');
            if (window.scrollY > 100) {
                navbar.style.background = 'rgba(13, 17, 23, 0.98)';
                navbar.style.boxShadow = '0 5px 20px rgba(0, 0, 0, 0.3)';
            } else {
                navbar.style.background = 'rgba(13, 17, 23, 0.95)';
                navbar.style.boxShadow = 'none';
            }
        });

        // ==================== ACTIVE SECTION HIGHLIGHT ====================
        const sections = document.querySelectorAll('section');

        window.addEventListener('scroll', () => {
            const scrollY = window.scrollY;

            sections.forEach(section => {
                const sectionTop = section.offsetTop - 100;
                const sectionHeight = section.offsetHeight;
                const sectionId = section.getAttribute('id');

                if (scrollY >= sectionTop && scrollY < sectionTop + sectionHeight) {
                    document.querySelectorAll('.nav-menu a').forEach(link => {
                        link.style.color = '';
                        if (link.getAttribute('href') === `#${sectionId}`) {
                            link.style.color = '#FF4500';
                        }
                    });
                }
            });
        });

        // ==================== TILT EFFECT FOR CARDS ====================
        const cards = document.querySelectorAll('.project-card, .cert-card, .stat-card, .timeline-content, .website-card');

        cards.forEach(card => {
            card.addEventListener('mousemove', (e) => {
                const rect = card.getBoundingClientRect();
                const x = e.clientX - rect.left;
                const y = e.clientY - rect.top;
                
                const centerX = rect.width / 2;
                const centerY = rect.height / 2;
                
                const rotateX = (y - centerY) / 20;
                const rotateY = (centerX - x) / 20;
                
                card.style.transform = `perspective(1000px) rotateX(${rotateX}deg) rotateY(${rotateY}deg) translateY(-5px)`;
            });
            
            card.addEventListener('mouseleave', () => {
                card.style.transform = 'perspective(1000px) rotateX(0) rotateY(0) translateY(0)';
            });
        });

        console.log('Portfolio loaded successfully! 🚀');
    </script>
</body>
</html>
