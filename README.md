<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Nneka Udoye - Senior Salesforce Field Service Administrator</title>
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        :root {
            --primary-color: #7A8471;           /* Sage green */
            --secondary-color: #D4A574;         /* Warm honey */
            --accent-color: #8B7355;            /* Warm taupe */
            --dark-color: #3D3426;              /* Deep earth brown */
            --light-color: #F5F3F0;             /* Warm cream */
            --text-light: #000000;              /* Medium brown */
            --white: #FEFEFE;                   /* Off-white */
            --gradient-primary: linear-gradient(135deg, #7A8471 0%, #9BA088 100%);
            --gradient-secondary: linear-gradient(135deg, #8B7355 0%, #A08B73 100%);
            --shadow: 0 4px 20px rgba(61, 52, 38, 0.1);
            --shadow-hover: 0 8px 30px rgba(61, 52, 38, 0.15);
            --card-bg: #F9F7F4;                 /* Soft cream */
            --section-bg: #EDEAE5;              /* Light stone */
        }

        body {
            font-family: 'Georgia', 'Times New Roman', serif;
            line-height: 1.6;
            color: var(--dark-color);
            overflow-x: hidden;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* Header & Navigation */
        .header {
            position: fixed;
            top: 0;
            width: 100%;
            background: rgba(249, 247, 244, 0.95);
            backdrop-filter: blur(10px);
            z-index: 1000;
            transition: all 0.3s ease;
            box-shadow: var(--shadow);
        }

        .nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 1rem 0;
        }

        .logo {
            font-size: 1.5rem;
            font-weight: bold;
            color: var(--primary-color);
        }

        .nav-links {
            display: flex;
            list-style: none;
            gap: 2rem;
        }

        .nav-links a {
            text-decoration: none;
            color: var(--dark-color);
            font-weight: 500;
            transition: color 0.3s ease;
        }

        .nav-links a:hover {
            color: var(--primary-color);
        }

        .mobile-menu {
            display: none;
            font-size: 1.5rem;
            cursor: pointer;
            color: var(--primary-color);
        }

        /* Hero Section */
        .hero {
            background: var(--gradient-primary);
            color: var(--white);
            padding: 120px 0 80px;
            text-align: center;
            position: relative;
            overflow: hidden;
        }

        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1000 100"><polygon fill="rgba(255,255,255,0.1)" points="0,100 100,0 200,50 300,0 400,75 500,25 600,50 700,0 800,25 900,75 1000,0 1000,100"/></svg>') repeat-x;
            opacity: 0.3;
        }

        .hero-content {
            position: relative;
            z-index: 2;
        }

        .hero h1 {
            font-size: 3.5rem;
            margin-bottom: 1rem;
            animation: fadeInUp 1s ease;
        }

        .hero-subtitle {
            font-size: 1.3rem;
            margin-bottom: 0.5rem;
            opacity: 0.9;
            animation: fadeInUp 1s ease 0.2s both;
        }

        .hero-description {
            font-size: 1.1rem;
            max-width: 600px;
            margin: 0 auto 2rem;
            opacity: 0.8;
            animation: fadeInUp 1s ease 0.4s both;
        }

        .cta-buttons {
            display: flex;
            gap: 1rem;
            justify-content: center;
            flex-wrap: wrap;
            animation: fadeInUp 1s ease 0.6s both;
        }

        .btn {
            padding: 12px 30px;
            border: none;
            border-radius: 25px;
            font-weight: 600;
            text-decoration: none;
            cursor: pointer;
            transition: all 0.3s ease;
            display: inline-flex;
            align-items: center;
            gap: 0.5rem;
        }

        .btn-primary {
            background: var(--white);
            color: var(--primary-color);
        }

        .btn-primary:hover {
            transform: translateY(-2px);
            box-shadow: var(--shadow-hover);
            background: var(--card-bg);
        }

        .btn-outline {
            background: transparent;
            color: var(--white);
            border: 2px solid var(--white);
        }

        .btn-outline:hover {
            background: var(--white);
            color: var(--primary-color);
        }

        /* Skills Section */
        .skills {
            padding: 80px 0;
            background: var(--light-color);
        }

        .section-title {
            text-align: center;
            font-size: 2.5rem;
            margin-bottom: 3rem;
            color: var(--dark-color);
        }

        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            margin-top: 2rem;
        }

        .skill-card {
            background: var(--white);
            padding: 2rem;
            border-radius: 15px;
            box-shadow: var(--shadow);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            border-top: 4px solid var(--primary-color);
        }

        .skill-card:hover {
            transform: translateY(-5px);
            box-shadow: var(--shadow-hover);
        }

        .skill-icon {
            font-size: 2.5rem;
            color: var(--primary-color);
            margin-bottom: 1rem;
        }

        .skill-title {
            font-size: 1.3rem;
            margin-bottom: 1rem;
            color: var(--dark-color);
        }

        .skill-description {
            color: var(--text-light);
            line-height: 1.6;
        }

        /* Projects Section */
        .projects {
            padding: 80px 0;
        }

        .projects-filter {
            display: flex;
            justify-content: center;
            gap: 1rem;
            margin-bottom: 3rem;
            flex-wrap: wrap;
        }

        .filter-btn {
            padding: 8px 20px;
            background: transparent;
            border: 2px solid var(--primary-color);
            color: var(--primary-color);
            border-radius: 20px;
            cursor: pointer;
            transition: all 0.3s ease;
            font-weight: 500;
        }

        .filter-btn.active,
        .filter-btn:hover {
            background: var(--primary-color);
            color: var(--white);
        }

        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 2rem;
        }

        .project-card {
            background: var(--white);
            border-radius: 15px;
            overflow: hidden;
            box-shadow: var(--shadow);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }

        .project-card:hover {
            transform: translateY(-5px);
            box-shadow: var(--shadow-hover);
        }

        .project-image {
            height: 200px;
            background: var(--gradient-secondary);
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--white);
            font-size: 3rem;
        }

        .project-content {
            padding: 1.5rem;
        }

        .project-title {
            font-size: 1.3rem;
            margin-bottom: 0.5rem;
            color: var(--dark-color);
        }

        .project-category {
            color: var(--primary-color);
            font-size: 0.9rem;
            font-weight: 600;
            margin-bottom: 1rem;
        }

        .project-description {
            color: var(--text-light);
            margin-bottom: 1rem;
            line-height: 1.6;
        }

        .project-tags {
            display: flex;
            flex-wrap: wrap;
            gap: 0.5rem;
            margin-bottom: 1rem;
        }

        .tag {
            background: var(--section-bg);
            color: var(--text-light);
            padding: 0.3rem 0.8rem;
            border-radius: 15px;
            font-size: 0.8rem;
        }

        .project-links {
            display: flex;
            gap: 1rem;
        }

        .project-link {
            color: var(--primary-color);
            text-decoration: none;
            font-weight: 500;
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }

        .project-link:hover {
            color: var(--accent-color);
        }

        /* Services Section */
        .services {
            padding: 80px 0;
            background: var(--light-color);
        }

        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
        }

        .service-card {
            background: var(--white);
            padding: 2rem;
            border-radius: 15px;
            text-align: center;
            box-shadow: var(--shadow);
            transition: transform 0.3s ease;
        }

        .service-card:hover {
            transform: translateY(-5px);
        }

        .service-icon {
            font-size: 3rem;
            color: var(--primary-color);
            margin-bottom: 1rem;
        }

        .service-title {
            font-size: 1.2rem;
            margin-bottom: 1rem;
            color: var(--dark-color);
        }

        /* About Section */
        .about {
            padding: 80px 0;
        }

        .about-content {
            display: grid;
            grid-template-columns: 1fr 2fr;
            gap: 3rem;
            align-items: center;
        }

        .about-image {
            text-align: center;
        }

        .about-photo {
            width: 250px;
            height: 250px;
            border-radius: 50%;
            background: var(--gradient-primary);
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--white);
            font-size: 4rem;
            margin: 0 auto;
        }

        .about-text h2 {
            font-size: 2rem;
            margin-bottom: 1rem;
            color: var(--dark-color);
        }

        .about-text p {
            color: var(--text-light);
            margin-bottom: 1rem;
            line-height: 1.8;
        }

        .certifications {
            display: flex;
            flex-wrap: wrap;
            gap: 1rem;
            margin-top: 2rem;
        }

        .cert-badge {
            background: var(--primary-color);
            color: var(--white);
            padding: 0.5rem 1rem;
            border-radius: 20px;
            font-size: 0.9rem;
            font-weight: 500;
        }

        /* Contact Section */
        .contact {
            padding: 80px 0;
            background: var(--dark-color);
            color: var(--white);
        }

        .contact-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 3rem;
        }

        .contact-info h2 {
            font-size: 2rem;
            margin-bottom: 1rem;
        }

        .contact-info p {
            margin-bottom: 2rem;
            opacity: 0.8;
        }

        .contact-item {
            display: flex;
            align-items: center;
            gap: 1rem;
            margin-bottom: 1rem;
        }

        .contact-item i {
            font-size: 1.2rem;
            color: var(--secondary-color);
            width: 20px;
        }

        .contact-form {
            background: rgba(122, 132, 113, 0.1);
            padding: 2rem;
            border-radius: 15px;
        }

        .form-group {
            margin-bottom: 1.5rem;
        }

        .form-group label {
            display: block;
            margin-bottom: 0.5rem;
            font-weight: 500;
        }

        .form-group input,
        .form-group textarea {
            width: 100%;
            padding: 12px;
            border: none;
            border-radius: 8px;
            background: rgba(255, 255, 255, 0.9);
            color: var(--dark-color);
        }

        .form-group textarea {
            height: 120px;
            resize: vertical;
        }

        /* Footer */
        .footer {
            background: var(--dark-color);
            color: var(--white);
            text-align: center;
            padding: 2rem 0;
            border-top: 1px solid rgba(122, 132, 113, 0.3);
        }

        .social-links {
            display: flex;
            justify-content: center;
            gap: 1rem;
            margin-bottom: 1rem;
        }

        .social-link {
            color: var(--white);
            font-size: 1.5rem;
            transition: color 0.3s ease;
        }

        .social-link:hover {
            color: var(--secondary-color);
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

        /* Responsive Design */
        @media (max-width: 768px) {
            .nav-links {
                display: none;
            }

            .mobile-menu {
                display: block;
            }

            .hero h1 {
                font-size: 2.5rem;
            }

            .hero-subtitle {
                font-size: 1.1rem;
            }

            .cta-buttons {
                flex-direction: column;
                align-items: center;
            }

            .about-content {
                grid-template-columns: 1fr;
                text-align: center;
            }

            .contact-content {
                grid-template-columns: 1fr;
            }

            .projects-grid {
                grid-template-columns: 1fr;
            }

            .skills-grid {
                grid-template-columns: 1fr;
            }
        }

        @media (max-width: 480px) {
            .container {
                padding: 0 15px;
            }

            .hero {
                padding: 100px 0 60px;
            }

            .section-title {
                font-size: 2rem;
            }

            .about-photo {
                width: 200px;
                height: 200px;
                font-size: 3rem;
            }
        }

        /* Utility Classes */
        .text-center { text-align: center; }
        .mb-2 { margin-bottom: 2rem; }
        .mt-2 { margin-top: 2rem; }
    </style>
</head>
<body>
    <!-- Header -->
    <header class="header">
        <nav class="nav container">
            <div class="logo">Salesforce Field lightning Expert</div>
            <ul class="nav-links">
                <li><a href="#home">Home</a></li>
                <li><a href="#skills">Skills</a></li>
                <li><a href="#projects">Projects</a></li>
                <li><a href="#services">Services</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
            <div class="mobile-menu">
                <i class="fas fa-bars"></i>
            </div>
        </nav>
    </header>

    <!-- Hero Section -->
    <section id="home" class="hero">
        <div class="container">
            <div class="hero-content">
                <h1>Senior Salesforce Field service Administrator</h1>
                <p class="hero-subtitle">Transforming Field Operations Through Intelligent Automation</p>
                <p class="hero-description">
                    7+ years of expertise in Field Service Lightning, optimizing work orders, scheduling, and mobile solutions 
                    that boost productivity and streamline operations across industries.
                </p>
                <div class="cta-buttons">
                    <a href="#projects" class="btn btn-primary">
                        <i class="fas fa-eye"></i> View My Work
                    </a>
                    <a href="#contact" class="btn btn-outline">
                        <i class="fas fa-envelope"></i> Get In Touch
                    </a>
                </div>
            </div>
        </div>
    </section>

    <!-- Skills Section -->
    <section id="skills" class="skills">
        <div class="container">
            <h2 class="section-title">Core Salesforce Field Service  Expertise</h2>
            <div class="skills-grid">
                <div class="skill-card">
                    <div class="skill-icon">
                        <i class="fas fa-cogs"></i>
                    </div>
                    <h3 class="skill-title">Automation & Optimization</h3>
                    <p class="skill-description">
                        Expert in Work Orders & Service Appointments automation using Flows, scheduling policies, 
                        and optimization algorithms for maximum efficiency.
                    </p>
                </div>

                <div class="skill-card">
                    <div class="skill-icon">
                        <i class="fas fa-users"></i>
                    </div>
                    <h3 class="skill-title">Resource Management</h3>
                    <p class="skill-description">
                        Advanced resource, skill, and territory management with operating hours configuration 
                        for optimal workforce allocation.
                    </p>
                </div>

                <div class="skill-card">
                    <div class="skill-icon">
                        <i class="fas fa-calendar-alt"></i>
                    </div>
                    <h3 class="skill-title">Dispatcher Console</h3>
                    <p class="skill-description">
                        Gantt optimization specialist with geolocation services and intelligent routing 
                        for enhanced dispatch operations.
                    </p>
                </div>

                <div class="skill-card">
                    <div class="skill-icon">
                        <i class="fas fa-mobile-alt"></i>
                    </div>
                    <h3 class="skill-title">Mobile Configuration</h3>
                    <p class="skill-description">
                        Mobile app customization expert, including offline capabilities, quick actions, 
                        and screen flows for field technicians.
                    </p>
                </div>

                <div class="skill-card">
                    <div class="skill-icon">
                        <i class="fas fa-tools"></i>
                    </div>
                    <h3 class="skill-title">Asset & Inventory</h3>
                    <p class="skill-description">
                        Comprehensive asset management, maintenance plans, and parts/inventory tracking 
                        with returns processing systems.
                    </p>
                </div>

                <div class="skill-card">
                    <div class="skill-icon">
                        <i class="fas fa-link"></i>
                    </div>
                    <h3 class="skill-title">Service Cloud Integration</h3>
                    <p class="skill-description">
                        Seamless Salesforce Field Service  integration with Service Cloud, including Cases, Entitlements, 
                        Milestones, and Knowledge management.
                    </p>
                </div>

                <div class="skill-card">
                    <div class="skill-icon">
                        <i class="fas fa-shield-alt"></i>
                    </div>
                    <h3 class="skill-title">Security & Deployment</h3>
                    <p class="skill-description">
                        Security compliance expert with profiles, permission sets, and DevOps Center 
                        deployment using change sets and best practices.
                    </p>
                </div>

                <div class="skill-card">
                    <div class="skill-icon">
                        <i class="fas fa-chart-line"></i>
                    </div>
                    <h3 class="skill-title">Analytics & KPIs</h3>
                    <p class="skill-description">
                        Advanced reporting and dashboards for first-visit fix rates, SLA compliance, 
                        utilization metrics, and system troubleshooting.
                    </p>
                </div>
            </div>
        </div>
    </section>

    <!-- Projects Section -->
    <section id="projects" class="projects">
        <div class="container">
            <h2 class="section-title">Featured Salesforce Field Service Projects</h2>
            
            <div class="projects-filter">
                <button class="filter-btn active" data-filter="all">All Projects</button>
                <button class="filter-btn" data-filter="automation">Automation</button>
                <button class="filter-btn" data-filter="mobile">Mobile</button>
                <button class="filter-btn" data-filter="optimization">Optimization</button>
                <button class="filter-btn" data-filter="integration">Integration</button>
            </div>

            <div class="projects-grid">
                <div class="project-card" data-category="automation optimization">
                    <div class="project-image">
                        <i class="fas fa-robot"></i>
                    </div>
                    <div class="project-content">
                        <div class="project-category">Automation & Optimization</div>
                        <h3 class="project-title">Smart Scheduling System</h3>
                        <p class="project-description">
                            Implemented intelligent work order automation with dynamic scheduling policies, 
                            reducing manual dispatch time by 65% and improving first-visit fix rates to 89%.
                        </p>
                        <div class="project-tags">
                            <span class="tag">Flows</span>
                            <span class="tag">Scheduling Policies</span>
                            <span class="tag">Work Orders</span>
                            <span class="tag">KPI Tracking</span>
                        </div>
                        <div class="project-links">
                            <a href="#" class="project-link">
                                <i class="fas fa-eye"></i> View Details
                            </a>
                            <a href="#" class="project-link">
                                <i class="fas fa-external-link-alt"></i> Live Demo
                            </a>
                        </div>
                    </div>
                </div>

                <div class="project-card" data-category="mobile">
                    <div class="project-image">
                        <i class="fas fa-mobile-alt"></i>
                    </div>
                    <div class="project-content">
                        <div class="project-category">Mobile Solutions</div>
                        <h3 class="project-title">Offline-First Mobile App</h3>
                        <p class="project-description">
                            Configured comprehensive mobile solution with offline capabilities, custom quick actions, 
                            and screen flows, enabling 40% faster job completion in remote areas.
                        </p>
                        <div class="project-tags">
                            <span class="tag">Mobile Config</span>
                            <span class="tag">Offline Mode</span>
                            <span class="tag">Quick Actions</span>
                            <span class="tag">Screen Flows</span>
                        </div>
                        <div class="project-links">
                            <a href="#" class="project-link">
                                <i class="fas fa-eye"></i> View Details
                            </a>
                            <a href="#" class="project-link">
                                <i class="fas fa-play"></i> Demo Video
                            </a>
                        </div>
                    </div>
                </div>

                <div class="project-card" data-category="optimization">
                    <div class="project-image">
                        <i class="fas fa-route"></i>
                    </div>
                    <div class="project-content">
                        <div class="project-category">Route Optimization</div>
                        <h3 class="project-title">Geolocation Routing Engine</h3>
                        <p class="project-description">
                            Built advanced dispatcher console with Gantt optimization and geolocation routing, 
                            cutting travel time by 30% and increasing daily job capacity by 25%.
                        </p>
                        <div class="project-tags">
                            <span class="tag">Dispatcher Console</span>
                            <span class="tag">Gantt Charts</span>
                            <span class="tag">Geolocation</span>
                            <span class="tag">Route Optimization</span>
                        </div>
                        <div class="project-links">
                            <a href="#" class="project-link">
                                <i class="fas fa-eye"></i> View Details
                            </a>
                            <a href="#" class="project-link">
                                <i class="fas fa-chart-line"></i> Results
                            </a>
                        </div>
                    </div>
                </div>

                <div class="project-card" data-category="integration">
                    <div class="project-image">
                        <i class="fas fa-plug"></i>
                    </div>
                    <div class="project-content">
                        <div class="project-category">Service Cloud Integration</div>
                        <h3 class="project-title">Unified Service Platform</h3>
                        <p class="project-description">
                            Integrated Salesforce Field Service with Service Cloud, implementing seamless case-to-work-order flow 
                            with entitlements and SLA tracking, improving customer satisfaction by 45%.
                        </p>
                        <div class="project-tags">
                            <span class="tag">Service Cloud</span>
                            <span class="tag">Cases</span>
                            <span class="tag">Entitlements</span>
                            <span class="tag">SLA Management</span>
                        </div>
                        <div class="project-links">
                            <a href="#" class="project-link">
                                <i class="fas fa-eye"></i> View Details
                            </a>
                            <a href="#" class="project-link">
                                <i class="fas fa-download"></i> Case Study
                            </a>
                        </div>
                    </div>
                </div>

                <div class="project-card" data-category="automation">
                    <div class="project-image">
                        <i class="fas fa-boxes"></i>
                    </div>
                    <div class="project-content">
                        <div class="project-category">Asset Management</div>
                        <h3 class="project-title">Predictive Maintenance System</h3>
                        <p class="project-description">
                            Developed comprehensive asset tracking with predictive maintenance plans and 
                            automated parts inventory management, reducing equipment downtime by 50%.
                        </p>
                        <div class="project-tags">
                            <span class="tag">Asset Management</span>
                            <span class="tag">Maintenance Plans</span>
                            <span class="tag">Inventory Tracking</span>
                            <span class="tag">Predictive Analytics</span>
                        </div>
                        <div class="project-links">
                            <a href="#" class="project-link">
                                <i class="fas fa-eye"></i> View Details
                            </a>
                            <a href="#" class="project-link">
                                <i class="fas fa-cog"></i> Technical Specs
                            </a>
                        </div>
                    </div>
                </div>

                <div class="project-card" data-category="optimization">
                    <div class="project-image">
                        <i class="fas fa-chart-bar"></i>
                    </div>
                    <div class="project-content">
                        <div class="project-category">Analytics & Reporting</div>
                        <h3 class="project-title">Executive KPI Dashboard</h3>
                        <p class="project-description">
                            Created comprehensive analytics suite with real-time KPI tracking, including 
                            first-visit fix rates, technician utilization, and SLA compliance monitoring.
                        </p>
                        <div class="project-tags">
                            <span class="tag">Dashboards</span>
                            <span class="tag">KPI Tracking</span>
                            <span class="tag">Real-time Analytics</span>
                            <span class="tag">SLA Monitoring</span>
                        </div>
                        <div class="project-links">
                            <a href="#" class="project-link">
                                <i class="fas fa-eye"></i> View Details
                            </a>
                            <a href="#" class="project-link">
                                <i class="fas fa-chart-line"></i> Live Dashboard
                            </a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Services Section -->
    <section id="services" class="services">
        <div class="container">
            <h2 class="section-title">Salesforce Field lightning Services I Provide</h2>
            <div class="services-grid">
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-rocket"></i>
                    </div>
                    <h3 class="service-title">Salesforce Field lightning Implementation</h3>
                    <p>Complete Field Service Lightning setup from planning to go-live with best practices.</p>
                </div>

                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-sync"></i>
                    </div>
                    <h3 class="service-title">Process Optimization</h3>
                    <p>Streamline existing Salesforce Field Lightning processes for maximum efficiency and user adoption.</p>
                    </div>

                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-graduation-cap"></i>
                    </div>
                    <h3 class="service-title">Training & Adoption</h3>
                    <p>Comprehensive user training and change management for successful Salesforce Field Lightning adoption.</p>
                </div>

                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-stethoscope"></i>
                    </div>
                    <h3 class="service-title">Health Checks</h3>
                    <p>Complete Salesforce Field lightning org audits with performance optimization recommendations.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section id="about" class="about">
        <div class="container">
            <div class="about-content">
                <div class="about-image">
                    <div class="about-photo">
                        <i class="fas fa-user"></i>
                    </div>
                </div>
                <div class="about-text">
                    <h2>About Me</h2>
                    <p>
                        With over 7 years of specialized experience in Salesforce Field Service Lightning, 
                        I've helped organizations across industries transform their field operations through 
                        intelligent automation and strategic optimization.
                    </p>
                    <p>
                        My passion lies in bridging the gap between complex technical capabilities and 
                        real-world business needs, ensuring that every Salesforce Field Lightning implementation delivers 
                        measurable value and drives user adoption.
                    </p>
                    <p>
                        From multinational corporations to growing startups, I've consistently delivered 
                        solutions that improve first-visit fix rates, reduce operational costs, and 
                        enhance customer satisfaction through smart field service management.
                    </p>
                    
                    <div class="certifications">
                        <span class="cert-badge">Salesforce Field lightning Consultant Certified</span>
                        <span class="cert-badge">Advanced Administrator</span>
                        <span class="cert-badge">Platform App Builder</span>
                        <span class="cert-badge">Service Cloud Consultant</span>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="contact">
        <div class="container">
            <div class="contact-content">
                <div class="contact-info">
                    <h2>Let's Optimize Your Field Operations</h2>
                    <p>
                        Ready to transform your field service operations? Let's discuss how Salesforce Field lightning can 
                        drive efficiency and growth for your organization.
                    </p>
                    
                    <div class="contact-item">
                        <i class="fas fa-envelope"></i>
                        <span>winifred.udoye@gmail.com</span>
                    </div>
                    
                    <div class="contact-item">
                        <i class="fas fa-phone"></i>
                        <span>+1 (951) 404-6278</span>
                    </div>
                    
                    <div class="contact-item">
                        <i class="fas fa-map-marker-alt"></i>
                        <span>Murrieta, California </span>
                    </div>
                    
                    <div class="contact-item">
                        <i class="fab fa-linkedin"></i>
                        <span>https://www.linkedin.com/in/salesforcewinnie/</span>
                    </div>
                </div>
                
                <form class="contact-form">
                    <div class="form-group">
                        <label for="name">Name</label>
                        <input type="text" id="name" name="name" required>
                    </div>
                    
                    <div class="form-group">
                        <label for="email">Email</label>
                        <input type="email" id="email" name="email" required>
                    </div>
                    
                    <div class="form-group">
                        <label for="subject">Subject</label>
                        <input type="text" id="subject" name="subject" required>
                    </div>
                    
                    <div class="form-group">
                        <label for="message">Message</label>
                        <textarea id="message" name="message" required></textarea>
                    </div>
                    
                    <button type="submit" class="btn btn-primary">
                        <i class="fas fa-paper-plane"></i> Send Message
                    </button>
                </form>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="footer">
        <div class="container">
            <div class="social-links">
                <a href="#" class="social-link"><i class="fab fa-linkedin"></i></a>
                <a href="#" class="social-link"><i class="fab fa-github"></i></a>
                <a href="#" class="social-link"><i class="fab fa-twitter"></i></a>
                <a href="#" class="social-link"><i class="fas fa-envelope"></i></a>
            </div>
            <p>&copy; 2025  Nneka.W.udoye. All rights reserved.</p>
        </div>
    </footer>

    <script>
        // Smooth scrolling for navigation links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
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

        // Header background on scroll
        window.addEventListener('scroll', () => {
            const header = document.querySelector('.header');
            if (window.scrollY > 100) {
                header.style.background = 'rgba(249, 247, 244, 0.98)';
            } else {
                header.style.background = 'rgba(249, 247, 244, 0.95)';
            }
        });

        // Project filtering
        const filterButtons = document.querySelectorAll('.filter-btn');
        const projectCards = document.querySelectorAll('.project-card');

        filterButtons.forEach(button => {
            button.addEventListener('click', () => {
                // Remove active class from all buttons
                filterButtons.forEach(btn => btn.classList.remove('active'));
                // Add active class to clicked button
                button.classList.add('active');

                const filterValue = button.getAttribute('data-filter');

                projectCards.forEach(card => {
                    if (filterValue === 'all') {
                        card.style.display = 'block';
                    } else {
                        const categories = card.getAttribute('data-category');
                        if (categories && categories.includes(filterValue)) {
                            card.style.display = 'block';
                        } else {
                            card.style.display = 'none';
                        }
                    }
                });
            });
        });

        // Contact form submission
        document.querySelector('.contact-form').addEventListener('submit', function(e) {
            e.preventDefault();
            alert('Thank you for your message! I\'ll get back to you soon.');
            this.reset();
        });

        // Mobile menu toggle (basic implementation)
        document.querySelector('.mobile-menu').addEventListener('click', function() {
            const navLinks = document.querySelector('.nav-links');
            navLinks.style.display = navLinks.style.display === 'flex' ? 'none' : 'flex';
        });
    </script>
</body>
</html>
