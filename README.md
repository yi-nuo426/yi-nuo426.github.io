<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Yi Nuo | Open Source Champion & Full-Stack Developer</title>
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css" rel="stylesheet">
    <style>
        :root {
            --primary: #009688; /* Energetic tech green */
            --primary-dark: #00796B;
            --secondary: #2C3E50;
            --light: #F8F9FA;
            --text-main: #333333;
            --text-muted: #666666;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Roboto, Helvetica, Arial, sans-serif;
        }

        body {
            line-height: 1.6;
            color: var(--text-main);
            background-color: var(--light);
        }

        /* Navigation */
        nav {
            background-color: white;
            padding: 1rem 5%;
            position: fixed;
            width: 100%;
            top: 0;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
            z-index: 1000;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        nav .logo {
            font-size: 1.5rem;
            font-weight: bold;
            color: var(--secondary);
            text-decoration: none;
        }

        nav .logo span {
            color: var(--primary);
        }

        nav ul {
            list-style: none;
            display: flex;
            gap: 2rem;
        }

        nav a {
            text-decoration: none;
            color: var(--secondary);
            font-weight: 500;
            transition: color 0.3s;
        }

        nav a:hover {
            color: var(--primary);
        }

        /* Hero Section */
        .hero {
            padding: 8rem 5% 4rem;
            background: linear-gradient(135deg, #ffffff 0%, #f0f7f6 100%);
            display: flex;
            align-items: center;
            justify-content: space-between;
            gap: 4rem;
            min-height: 100vh;
        }

        .hero-content {
            flex: 1;
        }

        .hero-content h1 {
            font-size: 3.5rem;
            color: var(--secondary);
            line-height: 1.2;
            margin-bottom: 1rem;
        }

        .hero-content h2 {
            font-size: 1.5rem;
            color: var(--primary);
            margin-bottom: 1.5rem;
            font-weight: 400;
        }

        .hero-content p {
            font-size: 1.1rem;
            color: var(--text-muted);
            margin-bottom: 2rem;
        }

        .hero-image {
            flex: 1;
            display: flex;
            justify-content: center;
        }

        .hero-image img {
            max-width: 100%;
            border-radius: 20px;
            box-shadow: 0 20px 40px rgba(0,0,0,0.1);
            border: 4px solid white;
        }

        /* Sections General */
        section {
            padding: 5rem 5%;
        }

        .section-title {
            text-align: center;
            font-size: 2.5rem;
            color: var(--secondary);
            margin-bottom: 3rem;
            position: relative;
        }

        .section-title::after {
            content: '';
            display: block;
            width: 60px;
            height: 4px;
            background-color: var(--primary);
            margin: 10px auto 0;
            border-radius: 2px;
        }

        /* About & Mission Section */
        .about-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 3rem;
            background: white;
            padding: 3rem;
            border-radius: 15px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
        }

        .mission-box {
            background: #f8fcfb;
            padding: 2rem;
            border-left: 4px solid var(--primary);
            border-radius: 0 8px 8px 0;
            margin-top: 1.5rem;
        }

        /* Experience & Work Section */
        .work-container {
            max-width: 1000px;
            margin: 0 auto;
        }

        .card {
            background: white;
            border-radius: 10px;
            padding: 2.5rem;
            margin-bottom: 2rem;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
            transition: transform 0.3s;
        }

        .card:hover {
            transform: translateY(-5px);
        }

        .card h3 {
            color: var(--secondary);
            font-size: 1.5rem;
            margin-bottom: 0.5rem;
        }

        .card h4 {
            color: var(--primary);
            margin-bottom: 1.5rem;
            font-weight: 500;
        }

        /* Skills Tag */
        .skills-flex {
            display: flex;
            flex-wrap: wrap;
            gap: 0.8rem;
            margin-top: 1.5rem;
        }

        .skill-tag {
            background: #e0f2f1;
            color: var(--primary-dark);
            padding: 0.4rem 1rem;
            border-radius: 20px;
            font-size: 0.9rem;
            font-weight: 500;
        }

        /* Open Source Highlight */
        .os-highlight {
            background: linear-gradient(135deg, var(--secondary) 0%, #1a252f 100%);
            color: white;
            text-align: center;
            padding: 5rem 5%;
        }

        .os-highlight h2 {
            color: white;
        }

        .os-highlight h2::after {
            background-color: var(--primary);
        }

        .cncf-badge {
            display: inline-block;
            background: rgba(255,255,255,0.1);
            padding: 2rem;
            border-radius: 15px;
            border: 1px solid rgba(255,255,255,0.2);
            max-width: 600px;
            margin: 0 auto;
        }

        /* Footer */
        footer {
            background: var(--light);
            text-align: center;
            padding: 3rem 5%;
            color: var(--text-muted);
        }

        .social-links {
            margin-bottom: 1.5rem;
        }

        .social-links a {
            color: var(--secondary);
            font-size: 1.5rem;
            margin: 0 10px;
            transition: color 0.3s;
        }

        .social-links a:hover {
            color: var(--primary);
        }

        /* Responsive */
        @media (max-width: 768px) {
            .hero {
                flex-direction: column-reverse;
                text-align: center;
                padding-top: 6rem;
            }
            .about-grid {
                grid-template-columns: 1fr;
            }
            nav ul {
                display: none; /* Mobile menu can be added later */
            }
        }
    </style>
</head>
<body>

    <nav>
        <a href="#" class="logo">Yi <span>Nuo</span></a>
        <ul>
            <li><a href="#about">About</a></li>
            <li><a href="#experience">Experience</a></li>
            <li><a href="#opensource">Open Source</a></li>
        </ul>
    </nav>

    <section class="hero">
        <div class="hero-content">
            <h1>Hi, I'm Yi Nuo.</h1>
            <h2>IT Officer & Open Source Champion</h2>
            <p>I am a 26-year-old technologist dedicated to building modern, robust applications while pioneering open-source culture and Linux adoption within traditional enterprise IT landscapes.</p>
            <div class="social-links" style="text-align: left; margin-top: 2rem;">
                <a href="https://github.com/yi-nuo426" target="_blank"><i class="fab fa-github"></i></a>
                <a href="#"><i class="fab fa-linkedin"></i></a>
                <a href="#"><i class="fas fa-envelope"></i></a>
            </div>
        </div>
        <div class="hero-image">
            <img src="yi-nuo-hku.png" alt="Yi Nuo - IT Professional at Hong Kong University">
        </div>
    </section>

    <section id="about">
        <h2 class="section-title">The Mission</h2>
        <div class="about-grid">
            <div>
                <p>Hello! I'm an energetic software developer and IT professional with over three years of experience navigating the dynamic intersection of enterprise technology and digital transformation. I currently serve on the IT team at the prestigious Hong Kong University (HKU).</p>
                <br>
                <p>My core drive? <strong>Modernization.</strong> I am deeply passionate about introducing Linux-based infrastructures and fostering a true open-source culture on our main campus. I believe that working and learning openly is the fastest path to innovation.</p>
            </div>
            <div>
                <div class="mission-box">
                    <h3><i class="fas fa-fire-alt" style="color: var(--primary);"></i> Driving Cultural Shift</h3>
                    <p style="margin-top: 10px;">Navigating systemic change is challenging. While I have executive support, bridging the gap between legacy pacing and modern, agile technology execution can be frustrating. However, this friction only fuels my resilience. I am committed to proving the value of open-source methodologies, one project and one deployment at a time.</p>
                </div>
            </div>
        </div>
    </section>

    <section id="experience" style="background: var(--light);">
        <h2 class="section-title">Professional Experience</h2>
        <div class="work-container">
            <div class="card">
                <h3>Programmer (IT Officer)</h3>
                <h4>Clinical Trials Centre (HKU-CTC) | The University of Hong Kong</h4>
                <p>Working at a leading clinical trials management platform under HKUMed, I manage and facilitate the technology behind international-standard clinical trials on new drugs and medical devices.</p>
                
                <ul style="margin-top: 1rem; margin-left: 1.5rem; color: var(--text-muted);">
                    <li>Design, develop, and deploy in-house IT systems, web applications, and web services supporting crucial medical research.</li>
                    <li>Analyze user requirements, execute system/database architectural design, and manage data migration.</li>
                    <li>Research, evaluate, and recommend cutting-edge technologies to accelerate our digital transformation goals.</li>
                </ul>

                <div class="skills-flex">
                    <span class="skill-tag">C# / .NET Core MVC</span>
                    <span class="skill-tag">PHP (Laravel/Symfony)</span>
                    <span class="skill-tag">JavaScript / React / Angular</span>
                    <span class="skill-tag">MS SQL / MySQL</span>
                    <span class="skill-tag">Azure DevOps / Git / Jenkins</span>
                    <span class="skill-tag">Linux / DevOps</span>
                </div>
            </div>
        </div>
    </section>

    <section id="opensource" class="os-highlight">
        <h2 class="section-title">Open Source Impact</h2>
        <p style="margin-bottom: 2rem; font-size: 1.1rem; max-width: 700px; margin-left: auto; margin-right: auto;">
            My commitment to open-source isn't just internal to my job—it extends to the global developer community. 
        </p>
        
        <div class="cncf-badge">
            <i class="fab fa-osi" style="font-size: 3rem; color: var(--primary); margin-bottom: 1rem;"></i>
            <h3 style="font-size: 1.5rem; margin-bottom: 0.5rem;">Meshery Extensions Maintainer</h3>
            <h4 style="color: var(--primary); margin-bottom: 1rem;">Cloud Native Computing Foundation (CNCF)</h4>
            <p style="color: #ccc; font-size: 0.95rem;">
                I am actively involved in maintaining Meshery Extensions, part of the CNCF project Meshery. Through this work, I help build out the cloud-native management plane, collaborating with developers worldwide and championing the ethos of working openly.
            </p>
        </div>
    </section>

    <footer>
        <div class="social-links">
            <a href="https://github.com/yi-nuo426" target="_blank"><i class="fab fa-github"></i></a>
            <a href="#"><i class="fab fa-linkedin"></i></a>
        </div>
        <p>&copy; 2026 Yi Nuo. Built with <i class="fas fa-heart" style="color: var(--primary);"></i> and Open Source.</p>
    </footer>

</body>
</html>
