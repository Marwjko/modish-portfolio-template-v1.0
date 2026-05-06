/* ==========================================
   Modish Portfolio Template
   Author: Marwan Jaafar Abduljalil Modish
   Version: 1.0.0
   ========================================== */

/* Root Variables */
:root {
    --primary-color: #6c5ce7;
    --secondary-color: #00b894;
    --accent-color: #ff7675;
    --dark-bg: #1a1a2e;
    --light-bg: #f8f9fa;
    --text-dark: #2d3436;
    --text-light: #636e72;
    --border-color: #dfe6e9;
    --shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
    --shadow-lg: 0 20px 60px rgba(0, 0, 0, 0.15);
    --transition: all 0.3s ease;
}

/* Dark Mode */
body.dark-mode {
    --light-bg: #1a1a2e;
    --text-dark: #ecf0f1;
    --text-light: #bdc3c7;
    --border-color: #2d3436;
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
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    background-color: var(--light-bg);
    color: var(--text-dark);
    line-height: 1.6;
    transition: var(--transition);
}

/* Typography */
h1, h2, h3, h4, h5, h6 {
    font-weight: 700;
    margin-bottom: 1rem;
}

p {
    color: var(--text-light);
    margin-bottom: 1rem;
}

a {
    text-decoration: none;
    color: inherit;
    transition: var(--transition);
}

/* Container */
.container {
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 20px;
}

/* ==========================================
   Navigation Bar
   ========================================== */

.navbar {
    position: fixed;
    top: 0;
    width: 100%;
    background: rgba(255, 255, 255, 0.95);
    backdrop-filter: blur(10px);
    z-index: 1000;
    box-shadow: var(--shadow);
    transition: var(--transition);
}

body.dark-mode .navbar {
    background: rgba(26, 26, 46, 0.95);
}

.nav-container {
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 20px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    height: 70px;
}

.logo {
    display: flex;
    align-items: center;
    gap: 10px;
    font-size: 24px;
    font-weight: 800;
    color: var(--primary-color);
}

.logo i {
    font-size: 28px;
}

.nav-menu {
    display: flex;
    list-style: none;
    gap: 30px;
}

.nav-link {
    color: var(--text-dark);
    font-weight: 500;
    position: relative;
    transition: var(--transition);
}

.nav-link::after {
    content: '';
    position: absolute;
    bottom: -5px;
    right: 0;
    width: 0;
    height: 2px;
    background: var(--primary-color);
    transition: var(--transition);
}

.nav-link:hover::after {
    width: 100%;
}

.nav-toggle {
    display: none;
    flex-direction: column;
    cursor: pointer;
    gap: 5px;
}

.nav-toggle span {
    width: 25px;
    height: 3px;
    background: var(--text-dark);
    border-radius: 3px;
    transition: var(--transition);
}

.theme-toggle {
    background: none;
    border: none;
    font-size: 20px;
    cursor: pointer;
    color: var(--text-dark);
    transition: var(--transition);
}

.theme-toggle:hover {
    color: var(--primary-color);
    transform: rotate(20deg);
}

/* ==========================================
   Hero Section
   ========================================== */

.hero {
    margin-top: 70px;
    min-height: calc(100vh - 70px);
    display: flex;
    align-items: center;
    justify-content: center;
    position: relative;
    overflow: hidden;
    background: linear-gradient(135deg, var(--primary-color) 0%, var(--secondary-color) 100%);
}

.hero-content {
    position: relative;
    z-index: 2;
    text-align: center;
    color: white;
    max-width: 600px;
    animation: fadeInUp 1s ease;
}

.hero-title {
    font-size: 60px;
    margin-bottom: 20px;
    font-weight: 800;
    line-height: 1.2;
}

.hero-subtitle {
    font-size: 20px;
    margin-bottom: 40px;
    color: rgba(255, 255, 255, 0.9);
    font-weight: 300;
}

.hero-buttons {
    display: flex;
    gap: 20px;
    justify-content: center;
    flex-wrap: wrap;
    margin-bottom: 60px;
}

.btn {
    padding: 15px 40px;
    border-radius: 50px;
    font-weight: 600;
    cursor: pointer;
    border: none;
    transition: var(--transition);
    font-size: 16px;
}

.btn-primary {
    background: white;
    color: var(--primary-color);
}

.btn-primary:hover {
    transform: translateY(-3px);
    box-shadow: 0 15px 40px rgba(0, 0, 0, 0.2);
}

.btn-secondary {
    background: transparent;
    color: white;
    border: 2px solid white;
}

.btn-secondary:hover {
    background: white;
    color: var(--primary-color);
}

.scroll-indicator {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 10px;
    color: rgba(255, 255, 255, 0.7);
    animation: bounce 2s infinite;
}

.scroll-indicator i {
    font-size: 24px;
}

.hero-background {
    position: absolute;
    width: 100%;
    height: 100%;
    top: 0;
    left: 0;
    z-index: 1;
    overflow: hidden;
}

.floating-shape {
    position: absolute;
    opacity: 0.1;
    border-radius: 50%;
}

.shape-1 {
    width: 300px;
    height: 300px;
    background: white;
    top: -100px;
    right: -100px;
    animation: float 6s ease-in-out infinite;
}

.shape-2 {
    width: 200px;
    height: 200px;
    background: white;
    bottom: -50px;
    left: -50px;
    animation: float 8s ease-in-out infinite reverse;
}

.shape-3 {
    width: 150px;
    height: 150px;
    background: white;
    top: 50%;
    left: 10%;
    animation: float 7s ease-in-out infinite;
}

/* ==========================================
   About Section
   ========================================== */

.about {
    padding: 100px 0;
    background: var(--light-bg);
}

.section-title {
    text-align: center;
    font-size: 40px;
    margin-bottom: 60px;
    color: var(--text-dark);
    position: relative;
    display: inline-block;
    width: 100%;
}

.section-title::after {
    content: '';
    position: absolute;
    bottom: -15px;
    left: 50%;
    transform: translateX(-50%);
    width: 60px;
    height: 4px;
    background: var(--primary-color);
    border-radius: 2px;
}

.about-content {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 50px;
    align-items: center;
}

.about-text p {
    margin-bottom: 20px;
    font-size: 16px;
    line-height: 1.8;
}

.skills {
    margin-top: 30px;
}

.skill-item {
    margin-bottom: 25px;
}

.skill-name {
    display: block;
    margin-bottom: 8px;
    font-weight: 600;
    color: var(--text-dark);
}

.skill-bar {
    width: 100%;
    height: 8px;
    background: var(--border-color);
    border-radius: 10px;
    overflow: hidden;
}

.skill-progress {
    height: 100%;
    background: linear-gradient(90deg, var(--primary-color), var(--secondary-color));
    border-radius: 10px;
    transition: width 1s ease;
}

.about-image {
    display: flex;
    justify-content: center;
    align-items: center;
}

.image-placeholder {
    width: 300px;
    height: 300px;
    background: linear-gradient(135deg, var(--primary-color), var(--secondary-color));
    border-radius: 20px;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 120px;
    color: rgba(255, 255, 255, 0.3);
    box-shadow: var(--shadow-lg);
}

/* ==========================================
   Portfolio Section
   ========================================== */

.portfolio {
    padding: 100px 0;
    background: var(--light-bg);
}

.portfolio-filters {
    display: flex;
    justify-content: center;
    gap: 15px;
    margin-bottom: 50px;
    flex-wrap: wrap;
}

.filter-btn {
    padding: 10px 25px;
    border: 2px solid var(--border-color);
    background: transparent;
    color: var(--text-dark);
    border-radius: 30px;
    cursor: pointer;
    font-weight: 600;
    transition: var(--transition);
}

.filter-btn:hover,
.filter-btn.active {
    background: var(--primary-color);
    color: white;
    border-color: var(--primary-color);
}

.portfolio-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 30px;
}

.portfolio-item {
    background: white;
    border-radius: 15px;
    overflow: hidden;
    box-shadow: var(--shadow);
    transition: var(--transition);
    cursor: pointer;
}

body.dark-mode .portfolio-item {
    background: #2d3436;
}

.portfolio-item:hover {
    transform: translateY(-10px);
    box-shadow: var(--shadow-lg);
}

.portfolio-image {
    position: relative;
    width: 100%;
    height: 250px;
    overflow: hidden;
    background: linear-gradient(135deg, var(--primary-color), var(--secondary-color));
}

.portfolio-image .image-placeholder {
    width: 100%;
    height: 100%;
    border-radius: 0;
    box-shadow: none;
}

.portfolio-overlay {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: rgba(0, 0, 0, 0.7);
    display: flex;
    align-items: center;
    justify-content: center;
    opacity: 0;
    transition: var(--transition);
}

.portfolio-item:hover .portfolio-overlay {
    opacity: 1;
}

.portfolio-link {
    width: 50px;
    height: 50px;
    background: var(--primary-color);
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    color: white;
    font-size: 20px;
    transition: var(--transition);
}

.portfolio-link:hover {
    transform: scale(1.2);
    background: var(--secondary-color);
}

.portfolio-item h3 {
    padding: 20px 20px 10px;
    color: var(--text-dark);
}

.portfolio-item p {
    padding: 0 20px 20px;
    font-size: 14px;
}

/* ==========================================
   Services Section
   ========================================== */

.services {
    padding: 100px 0;
    background: var(--light-bg);
}

.services-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 30px;
}

.service-card {
    background: white;
    padding: 40px 30px;
    border-radius: 15px;
    text-align: center;
    box-shadow: var(--shadow);
    transition: var(--transition);
}

body.dark-mode .service-card {
    background: #2d3436;
}

.service-card:hover {
    transform: translateY(-10px);
    box-shadow: var(--shadow-lg);
}

.service-icon {
    font-size: 50px;
    color: var(--primary-color);
    margin-bottom: 20px;
    transition: var(--transition);
}

.service-card:hover .service-icon {
    color: var(--secondary-color);
    transform: scale(1.1);
}

.service-card h3 {
    font-size: 20px;
    margin-bottom: 15px;
    color: var(--text-dark);
}

.service-card p {
    font-size: 14px;
    color: var(--text-light);
}

/* ==========================================
   Contact Section
   ========================================== */

.contact {
    padding: 100px 0;
    background: var(--light-bg);
}

.contact-content {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 50px;
    margin-top: 50px;
}

.contact-info {
    display: flex;
    flex-direction: column;
    gap: 30px;
}

.info-item {
    display: flex;
    gap: 20px;
    align-items: flex-start;
}

.info-item i {
    font-size: 30px;
    color: var(--primary-color);
    margin-top: 5px;
}

.info-item h4 {
    color: var(--text-dark);
    margin-bottom: 5px;
}

.info-item p {
    color: var(--text-light);
    margin: 0;
}

.contact-form {
    display: flex;
    flex-direction: column;
    gap: 20px;
}

.form-group {
    display: flex;
    flex-direction: column;
}

.form-group input,
.form-group textarea {
    padding: 15px;
    border: 2px solid var(--border-color);
    border-radius: 10px;
    font-family: inherit;
    font-size: 14px;
    color: var(--text-dark);
    background: white;
    transition: var(--transition);
}

body.dark-mode .form-group input,
body.dark-mode .form-group textarea {
    background: #2d3436;
    color: var(--text-dark);
    border-color: #444;
}

.form-group input:focus,
.form-group textarea:focus {
    outline: none;
    border-color: var(--primary-color);
    box-shadow: 0 0 0 3px rgba(108, 92, 231, 0.1);
}

/* ==========================================
   Footer
   ========================================== */

.footer {
    background: var(--dark-bg);
    color: white;
    padding: 60px 0 20px;
}

.footer-content {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 40px;
    margin-bottom: 40px;
}

.footer-section h4 {
    color: white;
    margin-bottom: 15px;
}

.footer-section p {
    color: #bdc3c7;
    margin: 0;
}

.footer-section ul {
    list-style: none;
}

.footer-section ul li {
    margin-bottom: 10px;
}

.footer-section a {
    color: #bdc3c7;
    transition: var(--transition);
}

.footer-section a:hover {
    color: var(--primary-color);
}

.social-links {
    display: flex;
    gap: 15px;
}

.social-links a {
    width: 40px;
    height: 40px;
    background: rgba(255, 255, 255, 0.1);
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    transition: var(--transition);
}

.social-links a:hover {
    background: var(--primary-color);
}

.footer-bottom {
    text-align: center;
    padding-top: 20px;
    border-top: 1px solid rgba(255, 255, 255, 0.1);
    color: #bdc3c7;
}

/* ==========================================
   Animations
   ========================================== */

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

@keyframes bounce {
    0%, 100% {
        transform: translateY(0);
    }
    50% {
        transform: translateY(-20px);
    }
}

@keyframes float {
    0%, 100% {
        transform: translateY(0px);
    }
    50% {
        transform: translateY(-20px);
    }
}

/* ==========================================
   Responsive Design
   ========================================== */

@media (max-width: 768px) {
    .nav-menu {
        display: none;
    }

    .nav-toggle {
        display: flex;
    }

    .hero-title {
        font-size: 40px;
    }

    .hero-subtitle {
        font-size: 16px;
    }

    .hero-buttons {
        flex-direction: column;
    }

    .btn {
        width: 100%;
    }

    .about-content {
        grid-template-columns: 1fr;
    }

    .contact-content {
        grid-template-columns: 1fr;
    }

    .section-title {
        font-size: 30px;
    }

    .portfolio-grid {
        grid-template-columns: 1fr;
    }

    .services-grid {
        grid-template-columns: 1fr;
    }

    .footer-content {
        grid-template-columns: 1fr;
    }
}

@media (max-width: 480px) {
    .hero-title {
        font-size: 28px;
    }

    .nav-container {
        height: 60px;
    }

    .logo {
        font-size: 18px;
    }

    .logo i {
        font-size: 22px;
    }

    .section-title {
        font-size: 24px;
    }

    .portfolio-filters {
        gap: 10px;
    }

    .filter-btn {
        padding: 8px 15px;
        font-size: 12px;
    }
}
