
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Lis's Portfolio | Medical AI Specialist</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', system-ui, sans-serif;
        }
        
        :root {
            --primary: #000000;
            --secondary: #ed1c24;
            --accent: #f26265;
            --light: #ffffff;
            --dark: #000000;
            --gray: #555555;
            --text: #333333;
            --shadow: 0 5px 15px rgba(0, 0, 0, 0.08);
        }
        
        body {
            background-color: #ffffff;
            color: var(--text);
            line-height: 1.6;
            min-height: 100vh;
            padding: 0;
        }
        
        .container {
            max-width: 1000px;
            margin: 0 auto;
            padding: 2rem;
        }
        
        header {
            text-align: center;
            margin-bottom: 3rem;
            padding: 2rem 0;
            position: relative;
        }
        
        header::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 50%;
            transform: translateX(-50%);
            width: 100px;
            height: 4px;
            background: var(--accent);
            border-radius: 2px;
        }
        
        .logo {
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 10px;
            margin-bottom: 1rem;
        }
        
        .logo i {
            font-size: 2.5rem;
            color: var(--secondary);
        }
        
        h1 {
            font-size: 2.5rem;
            font-weight: 700;
            color: var(--primary);
            margin-bottom: 0.5rem;
        }
        
        .subtitle {
            font-size: 1.2rem;
            color: var(--gray);
            font-weight: 400;
        }
        
        .intro-card {
            background: white;
            border-radius: 12px;
            padding: 2.5rem;
            box-shadow: var(--shadow);
            margin-bottom: 3rem;
            text-align: center;
            position: relative;
            overflow: hidden;
            border: 1px solid #eeeeee;
        }
        
        .intro-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 5px;
            background: var(--secondary);
        }
        
        .intro-card h2 {
            font-size: 1.8rem;
            margin-bottom: 1rem;
            color: var(--primary);
        }
        
        .intro-card p {
            font-size: 1.1rem;
            margin-bottom: 1.5rem;
            color: var(--text);
        }
        
        .btn {
            display: inline-flex;
            align-items: center;
            gap: 8px;
            background: var(--secondary);
            color: white;
            padding: 12px 24px;
            border-radius: 50px;
            text-decoration: none;
            font-weight: 600;
            transition: all 0.3s ease;
            box-shadow: 0 4px 6px rgba(237, 28, 36, 0.3);
        }
        
        .btn:hover {
            background: var(--primary);
            transform: translateY(-2px);
            box-shadow: 0 6px 12px rgba(237, 28, 36, 0.4);
        }
        
        .section {
            margin-bottom: 3rem;
        }
        
        .section-title {
            display: flex;
            align-items: center;
            gap: 10px;
            font-size: 1.5rem;
            margin-bottom: 1.5rem;
            color: var(--primary);
            padding-bottom: 0.5rem;
            border-bottom: 2px solid rgba(0, 0, 0, 0.1);
        }
        
        .section-title i {
            color: var(--accent);
        }
        
        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 1.5rem;
        }
        
        .skill-card {
            background: white;
            border-radius: 10px;
            padding: 1.5rem;
            box-shadow: var(--shadow);
            transition: transform 0.3s ease;
            border: 1px solid #eeeeee;
        }
        
        .skill-card:hover {
            transform: translateY(-5px);
        }
        
        .skill-card h3 {
            display: flex;
            align-items: center;
            gap: 10px;
            font-size: 1.2rem;
            margin-bottom: 1rem;
            color: var(--primary);
        }
        
        .skill-card h3 i {
            color: var(--secondary);
        }
        
        .skill-card ul {
            list-style: none;
            padding-left: 0;
        }
        
        .skill-card li {
            padding: 0.5rem 0;
            border-bottom: 1px solid rgba(0, 0, 0, 0.05);
            display: flex;
            align-items: center;
            gap: 8px;
        }
        
        .skill-card li:last-child {
            border-bottom: none;
        }
        
        .skill-card li i {
            color: var(--accent);
            font-size: 0.8rem;
        }
        
        .projects-table {
            width: 100%;
            border-collapse: collapse;
            background: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: var(--shadow);
            border: 1px solid #eeeeee;
        }
        
        .projects-table thead {
            background: var(--secondary);
            color: white;
        }
        
        .projects-table th {
            padding: 1.2rem 1rem;
            text-align: left;
            font-weight: 600;
        }
        
        .projects-table tbody tr {
            border-bottom: 1px solid rgba(0, 0, 0, 0.05);
            transition: background 0.3s ease;
        }
        
        .projects-table tbody tr:hover {
            background: rgba(242, 98, 101, 0.05);
        }
        
        .projects-table td {
            padding: 1.2rem 1rem;
        }
        
        .project-name {
            font-weight: 600;
            color: var(--primary);
        }
        
        .tech-tags {
            display: flex;
            flex-wrap: wrap;
            gap: 6px;
        }
        
        .tech-tag {
            background: rgba(242, 98, 101, 0.1);
            color: var(--accent);
            padding: 4px 10px;
            border-radius: 50px;
            font-size: 0.8rem;
            font-weight: 500;
        }
        
        .contact-links {
            display: flex;
            justify-content: center;
            gap: 1.5rem;
            margin-top: 1.5rem;
        }
        
        .contact-link {
            display: flex;
            align-items: center;
            gap: 8px;
            background: white;
            color: var(--primary);
            padding: 12px 24px;
            border-radius: 50px;
            text-decoration: none;
            font-weight: 600;
            transition: all 0.3s ease;
            box-shadow: var(--shadow);
            border: 1px solid #eeeeee;
        }
        
        .contact-link:hover {
            background: var(--secondary);
            color: white;
            transform: translateY(-3px);
        }
        
        footer {
            text-align: center;
            margin-top: 4rem;
            padding: 2rem 0;
            color: var(--gray);
            font-size: 0.9rem;
            border-top: 1px solid rgba(0, 0, 0, 0.1);
        }
        
        .page-indicator {
            display: flex;
            justify-content: center;
            gap: 10px;
            margin-top: 2rem;
        }
        
        .page-dot {
            width: 10px;
            height: 10px;
            border-radius: 50%;
            background: var(--gray);
            opacity: 0.5;
        }
        
        .page-dot.active {
            background: var(--secondary);
            opacity: 1;
        }
        
        @media (max-width: 768px) {
            .container {
                padding: 1.5rem;
            }
            
            h1 {
                font-size: 2rem;
            }
            
            .skills-grid {
                grid-template-columns: 1fr;
            }
            
            .projects-table {
                display: block;
                overflow-x: auto;
            }
            
            .contact-links {
                flex-direction: column;
                align-items: center;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <div class="logo">
                <i class="fas fa-brain"></i>
            </div>
            <h1>Lis's Portfolio</h1>
            <p class="subtitle">Computer Engineer & Artificial Intelligence Developer</p>
        </header>
        
        <section class="intro-card">
            <h2>Welcome to My Technical Portfolio</h2>
            <p>I work in the research and development of artificial intelligence models for neuroimaging analysis. My main focus is on using deep learning to segment tissues and visualize 3D data from brain MRI scans.</p>
            <a href="https://github.com/Cyberpink6" class="btn">
                <i class="fab fa-github"></i> View My GitHub Profile
            </a>
        </section>
        
        <section class="section">
            <h2 class="section-title">
                <i class="fas fa-check-circle"></i> Technical Specializations
            </h2>
            <div class="skills-grid">
                <div class="skill-card">
                    <h3><i class="fas fa-file-medical-alt"></i> Medical Imaging & AI</h3>
                    <ul>
                        <li><i class="fas fa-chevron-right"></i> Deep learning for brain MRI and X-ray image processing</li>
                        <li><i class="fas fa-chevron-right"></i> Medical image analysis </li>
                        <li><i class="fas fa-chevron-right"></i> Segmentation algorithms</li>
                    </ul>
                </div>
                
                <div class="skill-card">
                    <h3><i class="fas fa-cube"></i> 3D Data Processing</h3>
                    <ul>
                        <li><i class="fas fa-chevron-right"></i> 3D Convolutional Neural Networks (CNNs)</li>
                        <li><i class="fas fa-chevron-right"></i> Point cloud segmentation</li>
                        <li><i class="fas fa-chevron-right"></i> Mesh processing and analysis</li>
                    </ul>
                </div>
                
                <div class="skill-card">
                    <h3><i class="fas fa-code"></i> Programming & Tools</h3>
                    <ul>
                        <li><i class="fas fa-chevron-right"></i> Python, PyTorch, TensorFlow</li>
                        <li><i class="fas fa-chevron-right"></i> Keras, MATLAB</li>
                        <li><i class="fas fa-chevron-right"></i> Pandas</li>
                    </ul>
                </div>
            </div>
        </section>
        
        <section class="section">
            <h2 class="section-title">
                <i class="fas fa-star"></i> Featured Projects
            </h2>
            <h3 style="margin-bottom: 1.5rem; color: var(--primary);">Brain MRI Analysis & Segmentation</h3>
            
            <table class="projects-table">
                <thead>
                    <tr>
                        <th>Project</th>
                        <th>Description</th>
                        <th>Technologies</th>
                    </tr>
                </thead>
                <tbody>
                    <tr>
                        <td class="project-name">Report Generator Project</td>
                        <td>Brain Segmentation and SCA2 diagnose</td>
                        <td>
                            <div class="tech-tags">
                                <span class="tech-tag">Python</span>
                                <span class="tech-tag">TensorFlow</span>
                                <span class="tech-tag">Keras</span>
                                <span class="tech-tag">3D CNN</span>
                            </div>
                        </td>
                    </tr>
                    <tr>
                        <td class="project-name">CNN & Atlas</td>
                        <td>Research about the combination of CNN & MRI Global Atlases for SCA2 detection</td>
                        <td>
                            <div class="tech-tags">
                                <span class="tech-tag">Python</span>
                                <span class="tech-tag">TensorFlow</span>
                                <span class="tech-tag">Keras</span>
                                <span class="tech-tag">3D CNN</span>
                            </div>
                        </td>
                    </tr>
                </tbody>
            </table>
        </section>
        
        <section class="section">
            <h2 class="section-title">
                <i class="fas fa-paper-plane"></i> Connect with Me
            </h2>
            <div style="text-align: center;">
                <p style="margin-bottom: 1.5rem;">Feel free to reach out for collaborations or just to say hello!</p>
                <div class="contact-links">
                    <a href="https://github.com/cyberpink6" class="contact-link">
                        <i class="fab fa-github"></i> @cyberpink6
                    </a>
                    <a href="https://cyberpink6.github.io" class="contact-link">
                        <i class="fas fa-globe"></i> cyberpink6.github.io
                    </a>
                </div>
            </div>
        </section>
        
        <footer>
            <p>This portfolio is continuously updated with new projects and contributions to the field of medical AI.</p>
            <p>Hosted on GitHub Pages — Theme by orderedlist</p>
            <p><a href="https://cyberpink6.github.io" style="color: var(--secondary); text-decoration: none;">https://cyberpink6.github.io</a></p>
            
            <div class="page-indicator">
                <div class="page-dot active"></div>
                <div class="page-dot"></div>
            </div>
        </footer>
    </div>

    <script>
        // Simple animation on scroll
        document.addEventListener('DOMContentLoaded', function() {
            const skillCards = document.querySelectorAll('.skill-card');
            const options = {
                threshold: 0.1,
                rootMargin: '0px 0px -50px 0px'
            };
            
            const observer = new IntersectionObserver(function(entries, observer) {
                entries.forEach(entry => {
                    if (entry.isIntersecting) {
                        entry.target.style.opacity = '1';
                        entry.target.style.transform = 'translateY(0)';
                    }
                });
            }, options);
            
            skillCards.forEach(card => {
                card.style.opacity = '0';
                card.style.transform = 'translateY(20px)';
                card.style.transition = 'opacity 0.5s ease, transform 0.5s ease';
                observer.observe(card);
            });
        });
    </script>
</body>
</html>
