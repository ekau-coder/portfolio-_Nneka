<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title> Nneka Udoye - Senior Salesforce field Service  Administrator</title>
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        :root {
            --primary-color: #002244; /* Deep Midnight Blue */
            --secondary-color: #DD5A01; /* Rich Burnt Orange */
            --accent-color: #F0A500; /* Vibrant Gold Accent */
            --dark-color: #000000; /* Black for main text */
            --light-color: #F0F4F8; /* Light Gray/Blue for backgrounds */
            --text-light: #333333; /* Dark gray for secondary text */
            --white: #FFFFFF; /* Pure White */
            --gradient-primary: linear-gradient(135deg, #002244 0%, #0A436D 100%);
            --gradient-secondary: linear-gradient(135deg, #DD5A01 0%, #FF8C00 100%);
            --shadow: 0 4px 20px rgba(0, 26, 51, 0.15);
            --shadow-hover: 0 8px 30px rgba(0, 26, 51, 0.25);
            --card-bg: #FFFFFF; /* White cards */
            --section-bg: #E3E9F0; /* Lighter gray/blue for section background */
        }

        body {
            font-family: 'Georgia', serif;
            line-height: 1.6;
            color: var(--dark-color);
            overflow-x: hidden;
            background-color: var(--section-bg);
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* Header & Navigation */
        .header {
            background-color: var(--primary-color);
            color: var(--white);
            padding: 1rem 0;
            box-shadow: var(--shadow);
        }
        
        .header .container {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-size: 1.5rem;
            font-weight: bold;
            color: var(--accent-color);
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .nav-links {
            display: flex;
            list-style: none;
            gap: 2rem;
        }

        .nav-links a {
            text-decoration: none;
            color: var(--white);
            font-weight: 500;
            transition: color 0.3s ease;
        }

        .nav-links a:hover {
            color: var(--secondary-color);
        }

        .mobile-menu {
            display: none;
            font-size: 1.5rem;
            cursor: pointer;
            color: var(--white);
        }

        /* About Section (Hero) */
        .about-hero {
            padding: 80px 0;
            text-align: center;
            background-color: var(--white);
            box-shadow: var(--shadow);
            margin-bottom: 2rem;
            border-bottom: 5px solid var(--secondary-color);
        }

        .about-hero h1 {
            font-size: 3.5rem;
            color: var(--primary-color);
            margin-bottom: 1rem;
        }

        .about-hero p {
            font-size: 1.1rem;
            max-width: 800px;
            margin: 0 auto 1.5rem;
            color: var(--text-light);
            line-height: 1.8;
        }
        
        .about-hero .profile-pic {
            width: 200px;
            height: 200px;
            border-radius: 50%;
            object-fit: cover;
            border: 4px solid var(--accent-color);
            box-shadow: 0 6px 15px rgba(0, 0, 0, 0.2);
            margin-bottom: 2rem;
        }
        
        .contact-info {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 20px;
            list-style: none;
            padding: 0;
            margin: 2rem 0 0;
        }
        
        .contact-info li {
            display: flex;
            align-items: center;
            gap: 10px;
            color: var(--primary-color);
            font-weight: 600;
        }
        
        .contact-info a {
            text-decoration: none;
            color: var(--primary-color);
            transition: color 0.3s ease;
        }
        
        .contact-info a:hover {
            color: var(--secondary-color);
        }

        /* Section Styling */
        .section {
            padding: 80px 0;
            margin-top: 2rem;
        }

        .section-title {
            text-align: center;
            font-size: 2.5rem;
            margin-bottom: 3rem;
            color: var(--primary-color);
            position: relative;
        }

        .section-title::after {
            content: '';
            width: 80px;
            height: 4px;
            background-color: var(--accent-color);
            position: absolute;
            left: 50%;
            transform: translateX(-50%);
            bottom: -15px;
            border-radius: 2px;
        }

        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }

        .skill-card {
            background: var(--card-bg);
            padding: 2rem;
            border-radius: 15px;
            box-shadow: var(--shadow);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            border-left: 6px solid var(--accent-color);
        }

        .skill-card:hover {
            transform: translateY(-5px);
            box-shadow: var(--shadow-hover);
        }

        .skill-icon {
            font-size: 2.5rem;
            color: var(--secondary-color);
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

        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 2rem;
        }

        .project-card {
            background: var(--card-bg);
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
            background: var(--gradient-primary);
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

        /* Footer */
        .footer {
            background: var(--primary-color);
            color: var(--white);
            text-align: center;
            padding: 2rem 0;
            margin-top: 60px;
            border-top: 2px solid var(--accent-color);
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

        /* Responsive Design */
        @media (max-width: 768px) {
            .nav-links {
                display: none;
            }
            .mobile-menu {
                display: block;
            }
            .about-hero h1 {
                font-size: 2.5rem;
            }
            .about-hero p {
                font-size: 1rem;
            }
            .contact-info {
                flex-direction: column;
                align-items: center;
            }
            .projects-grid, .skills-grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <header class="header">
        <div class="container">
            <div class="logo">FSL Expert</div>
            <ul class="nav-links">
                <li><a href="#about">About</a></li>
                <li><a href="#skills">Skills</a></li>
                <li><a href="#projects">Projects</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
            <div class="mobile-menu">
                <i class="fas fa-bars"></i>
            </div>
        </div>
    </header>

    <section id="about" class="about-hero">
        <div class="container">
            <img src="https://assets-global.website-files.com/6573c9f280a9d0b642674288/657754b2b2b189b87e2f5b61_IMG_20231210_134812_684.jpg" alt="Ijeoma Udoye" class="profile-pic">
            <h1>Ijeoma Udoye</h1>
            <p class="hero-subtitle">Senior Salesforce Administrator & Field Service (FSL) Specialist</p>
            <p>
                Hello, I'm Ijeoma Udoye, a certified Senior Salesforce Field Service Administrator with extensive experience in leading digital transformations. My passion lies in architecting and implementing robust FSL solutions that not only meet business needs but also exceed operational expectations.
            </p>
            <p>
                I specialize in streamlining complex field service workflows, from intelligent work order automation and resource optimization to comprehensive mobile configurations and asset management. I'm dedicated to delivering solutions that boost productivity, improve customer satisfaction, and provide clear, actionable insights through advanced analytics.
            </p>
            <ul class="contact-info">
                <li><i class="fas fa-map-marker-alt"></i> Murrieta, California, USA</li>
                <li><i class="fas fa-envelope"></i> <a href="mailto:your.email@example.com">your.email@example.com</a></li>
                <li><i class="fas fa-phone"></i> <a href="tel:+15551234567">+1 (555) 123-4567</a></li>
                <li><i class="fab fa-linkedin"></i> <a href="https://www.linkedin.com/in/yourprofile" target="_blank">LinkedIn Profile</a></li>
            </ul>
        </div>
    </section>

    <div class="container">
        <section id="skills" class="section">
            <h2 class="section-title">Skills & Expertise</h2>
            <div class="skills-grid">
                <div class="skill-card">
                    <div class="skill-icon"><i class="fas fa-cogs"></i></div>
                    <h3 class="skill-title">Automation & Optimization</h3>
                    <p class="skill-description">Expert in Work Orders & Service Appointments automation using Flows, scheduling policies, and optimization algorithms for maximum efficiency.</p>
                </div>
                <div class="skill-card">
                    <div class="skill-icon"><i class="fas fa-users"></i></div>
                    <h3 class="skill-title">Resource Management</h3>
                    <p class="skill-description">Advanced resource, skill, and territory management with operating hours configuration for optimal workforce allocation.</p>
                </div>
                <div class="skill-card">
                    <div class="skill-icon"><i class="fas fa-calendar-alt"></i></div>
                    <h3 class="skill-title">Dispatcher Console</h3>
                    <p class="skill-description">Gantt optimization specialist with geolocation services and intelligent routing for enhanced dispatch operations.</p>
                </div>
                <div class="skill-card">
                    <div class="skill-icon"><i class="fas fa-mobile-alt"></i></div>
                    <h3 class="skill-title">Mobile Configuration</h3>
                    <p class="skill-description">Mobile app customization expert including offline capabilities, quick actions, and screen flows for field technicians.</p>
                </div>
                <div class="skill-card">
                    <div class="skill-icon"><i class="fas fa-tools"></i></div>
                    <h3 class="skill-title">Asset & Inventory</h3>
                    <p class="skill-description">Comprehensive asset management, maintenance plans, and parts/inventory tracking with returns processing systems.</p>
                </div>
                <div class="skill-card">
                    <div class="skill-icon"><i class="fas fa-link"></i></div>
                    <h3 class="skill-title">Service Cloud Integration</h3>
                    <p class="skill-description">Seamless FSL integration with Service Cloud including Cases, Entitlements, Milestones, and Knowledge management.</p>
                </div>
            </div>
        </section>

        <section id="projects" class="section">
            <h2 class="section-title">Featured Projects</h2>
            <div class="projects-grid">
                <div class="project-card">
                    <div class="project-image"><i class="fas fa-robot"></i></div>
                    <div class="project-content">
                        <h3 class="project-title">Smart Scheduling System</h3>
                        <p class="project-description">Implemented intelligent work order automation with dynamic scheduling policies, reducing manual dispatch time by 65% and improving first-visit fix rates to 89%.</p>
                    </div>
                </div>
                <div class="project-card">
                    <div class="project-image"><i class="fas fa-mobile-alt"></i></div>
                    <div class="project-content">
                        <h3 class="project-title">Offline-First Mobile App</h3>
                        <p class="project-description">Configured comprehensive mobile solution with offline capabilities, custom quick actions, and screen flows, enabling 40% faster job completion in remote areas.</p>
                    </div>
                </div>
                <div class="project-card">
                    <div class="project-image"><i class="fas fa-route"></i></div>
                    <div class="project-content">
                        <h3 class="project-title">Geolocation Routing Engine</h3>
                        <p class="project-description">Built advanced dispatcher console with Gantt optimization and geolocation routing, cutting travel time by 30% and increasing daily job capacity by 25%.</p>
                    </div>
                </div>
                <div class="project-card">
                    <div class="project-image"><i class="fas fa-plug"></i></div>
                    <div class="project-content">
                        <h3 class="project-title">Unified Service Platform</h3>
                        <p class="project-description">Integrated FSL with Service Cloud, implementing a seamless case-to-work-order flow with entitlements and SLA tracking, improving customer satisfaction by 45%.</p>
                    </div>
                </div>
            </div>
        </section>
        
        <section id="contact" class="section contact">
            <h2 class="section-title" style="color: var(--white);">Get In Touch</h2>
            <div class="contact-content">
                <div class="contact-info">
                    <p>I am available for new projects and opportunities. Feel free to reach out to me via email or LinkedIn.</p>
                    <div class="contact-item">
                        <i class="fas fa-envelope"></i>
                        <span><a href="mailto:winifred.udoye@gmail.com">your.email@example.com</a></span>
                    </div>
                    <div class="contact-item">
                        <i class="fab fa-linkedin"></i>
                        <span><a href="[https://www.linkedin.com/in/yourprofile](https://www.linkedin.com/in/salesforcewinnie/)" target="_blank">LinkedIn Profile</a></span>
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
                        <label for="message">Message</label>
                        <textarea id="message" name="message" required></textarea>
                    </div>
                    <button type="submit" class="btn btn-primary" style="background-color: var(--secondary-color); color: var(--white);">Send Message</button>
                </form>
            </div>
        </section>
    </div>

    <footer class="footer">
        <p>&copy; 2025 Nneka Udoye. All rights reserved.</p>
    </footer>
</body>
</html>
