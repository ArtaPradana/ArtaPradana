<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>I Made Arta Pradana - GitHub Profile</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary: #6e44ff;
            --secondary: #ff6b6b;
            --accent: #1a8fe3;
            --dark: #1a1a2e;
            --light: #f8f9fa;
            --gradient: linear-gradient(135deg, var(--primary), var(--accent));
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background-color: #0d1117;
            color: var(--light);
            line-height: 1.6;
            padding: 20px;
            max-width: 1100px;
            margin: 0 auto;
        }
        
        .container {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 20px;
            margin-top: 30px;
        }
        
        @media (max-width: 768px) {
            .container {
                grid-template-columns: 1fr;
            }
        }
        
        .card {
            background: #161b22;
            border-radius: 16px;
            padding: 25px;
            box-shadow: 0 8px 30px rgba(0, 0, 0, 0.3);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            border: 1px solid #30363d;
        }
        
        .card:hover {
            transform: translateY(-5px);
            box-shadow: 0 12px 40px rgba(0, 0, 0, 0.4);
        }
        
        .header {
            text-align: center;
            margin-bottom: 30px;
            position: relative;
            padding: 30px 0;
            background: linear-gradient(135deg, #161b22 0%, #0d1117 100%);
            border-radius: 16px;
            overflow: hidden;
        }
        
        .header::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 5px;
            background: var(--gradient);
        }
        
        .profile-img {
            width: 150px;
            height: 150px;
            border-radius: 50%;
            object-fit: cover;
            border: 5px solid var(--primary);
            box-shadow: 0 0 25px rgba(110, 68, 255, 0.5);
            margin-bottom: 20px;
            transition: transform 0.5s ease;
        }
        
        .profile-img:hover {
            transform: scale(1.05);
        }
        
        .name {
            font-size: 2.5rem;
            margin-bottom: 10px;
            background: var(--gradient);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            font-weight: 700;
        }
        
        .tagline {
            font-size: 1.2rem;
            color: #8b949e;
            margin-bottom: 20px;
        }
        
        .badges {
            display: flex;
            justify-content: center;
            gap: 10px;
            margin-bottom: 20px;
            flex-wrap: wrap;
        }
        
        .badge {
            background: var(--gradient);
            color: white;
            padding: 6px 15px;
            border-radius: 20px;
            font-size: 0.9rem;
            display: flex;
            align-items: center;
            gap: 5px;
        }
        
        .stats {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 20px;
        }
        
        .stat {
            text-align: center;
            background: rgba(110, 68, 255, 0.1);
            padding: 15px;
            border-radius: 12px;
            min-width: 120px;
        }
        
        .stat-number {
            font-size: 1.8rem;
            font-weight: 700;
            background: var(--gradient);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }
        
        .stat-label {
            font-size: 0.9rem;
            color: #8b949e;
        }
        
        h2 {
            font-size: 1.5rem;
            margin-bottom: 20px;
            padding-bottom: 10px;
            border-bottom: 2px solid var(--primary);
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .about p {
            margin-bottom: 15px;
            color: #c9d1d9;
        }
        
        .interests {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            margin-top: 15px;
        }
        
        .interest {
            background: rgba(26, 143, 227, 0.15);
            color: #58a6ff;
            padding: 5px 12px;
            border-radius: 15px;
            font-size: 0.9rem;
        }
        
        .tech-stack {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 15px;
        }
        
        .tech-category {
            margin-bottom: 20px;
        }
        
        .tech-category h3 {
            font-size: 1.1rem;
            margin-bottom: 10px;
            color: var(--accent);
            display: flex;
            align-items: center;
            gap: 8px;
        }
        
        .tech-items {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
        }
        
        .tech-item {
            background: rgba(255, 255, 255, 0.05);
            padding: 8px 15px;
            border-radius: 12px;
            font-size: 0.9rem;
            display: flex;
            align-items: center;
            gap: 8px;
            transition: background 0.3s ease;
        }
        
        .tech-item:hover {
            background: rgba(110, 68, 255, 0.2);
        }
        
        .projects-grid {
            display: grid;
            grid-template-columns: 1fr;
            gap: 15px;
        }
        
        .project {
            background: rgba(255, 255, 255, 0.03);
            padding: 20px;
            border-radius: 12px;
            border-left: 4px solid var(--primary);
        }
        
        .project h3 {
            font-size: 1.2rem;
            margin-bottom: 10px;
            color: var(--secondary);
        }
        
        .project p {
            color: #8b949e;
            margin-bottom: 15px;
        }
        
        .project-tech {
            display: flex;
            flex-wrap: wrap;
            gap: 8px;
            margin-bottom: 15px;
        }
        
        .project-tech span {
            background: rgba(110, 68, 255, 0.15);
            color: #c9d1d9;
            padding: 4px 10px;
            border-radius: 10px;
            font-size: 0.8rem;
        }
        
        .social-links {
            display: flex;
            justify-content: center;
            gap: 15px;
            margin-top: 30px;
        }
        
        .social-link {
            width: 50px;
            height: 50px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            background: var(--gradient);
            color: white;
            font-size: 1.2rem;
            transition: transform 0.3s ease;
        }
        
        .social-link:hover {
            transform: scale(1.1);
        }
        
        .quote {
            text-align: center;
            margin: 40px 0;
            font-style: italic;
            color: #8b949e;
            padding: 20px;
            border-radius: 12px;
            background: rgba(110, 68, 255, 0.05);
            border-left: 4px solid var(--secondary);
        }
        
        .highlight {
            color: var(--secondary);
            font-weight: 600;
        }
        
        .footer {
            text-align: center;
            margin-top: 50px;
            padding: 20px;
            color: #8b949e;
            font-size: 0.9rem;
            border-top: 1px solid #30363d;
        }
        
        .typewriter {
            overflow: hidden;
            border-right: 0.15em solid var(--primary);
            white-space: nowrap;
            margin: 0 auto;
            letter-spacing: 0.15em;
            animation: typing 3.5s steps(40, end), blink-caret 0.75s step-end infinite;
        }
        
        @keyframes typing {
            from { width: 0 }
            to { width: 100% }
        }
        
        @keyframes blink-caret {
            from, to { border-color: transparent }
            50% { border-color: var(--primary) }
        }
        
        .pulse {
            animation: pulse 2s infinite;
        }
        
        @keyframes pulse {
            0% { transform: scale(1); }
            50% { transform: scale(1.05); }
            100% { transform: scale(1); }
        }
    </style>
</head>
<body>
    <div class="header">
        <img src="https://avatars.githubusercontent.com/u/112266941" alt="I Made Arta Pradana" class="profile-img">
        <h1 class="name">I Made Arta Pradana</h1>
        <p class="tagline">Developer Passionate | Open Source Enthusiast | Tech Lover</p>
        
        <div class="badges">
            <div class="badge"><i class="fas fa-code"></i> Full Stack Developer</div>
            <div class="badge"><i class="fas fa-rocket"></i> Tech Innovator</div>
            <div class="badge"><i class="fas fa-music"></i> Musician</div>
        </div>
        
        <div class="stats">
            <div class="stat">
                <div class="stat-number">15+</div>
                <div class="stat-label">Projects</div>
            </div>
            <div class="stat">
                <div class="stat-number">500+</div>
                <div class="stat-label">Contributions</div>
            </div>
            <div class="stat">
                <div class="stat-number">2+</div>
                <div class="stat-label">Years Experience</div>
            </div>
        </div>
    </div>
    
    <div class="container">
        <div class="card">
            <h2><i class="fas fa-user"></i> About Me</h2>
            <div class="about">
                <p>Halo! Saya seorang <span class="highlight">Full Stack Developer</span> yang antusias dengan teknologi terbaru. Saya senang belajar hal-hal baru dan berkontribusi pada proyek open source.</p>
                <p>Di waktu luang, saya menikmati membaca buku teknologi, bereksperimen dengan framework baru, dan tentu saja bermain musik.</p>
                
                <div class="interests">
                    <div class="interest"><i class="fas fa-laptop-code"></i> Web Development</div>
                    <div class="interest"><i class="fas fa-mobile-alt"></i> Responsive Design</div>
                    <div class="interest"><i class="fas fa-server"></i> Backend Technologies</div>
                    <div class="interest"><i class="fas fa-guitar"></i> Music Production</div>
                </div>
            </div>
        </div>
        
        <div class="card">
            <h2><i class="fas fa-laptop-code"></i> Tech Stack</h2>
            <div class="tech-stack">
                <div class="tech-category">
                    <h3><i class="fas fa-code"></i> Languages</h3>
                    <div class="tech-items">
                        <div class="tech-item"><i class="fab fa-js"></i> JavaScript</div>
                        <div class="tech-item"><i class="fab fa-php"></i> PHP</div>
                        <div class="tech-item"><i class="fas fa-code"></i> TypeScript</div>
                    </div>
                </div>
                
                <div class="tech-category">
                    <h3><i class="fas fa-layer-group"></i> Frameworks</h3>
                    <div class="tech-items">
                        <div class="tech-item"><i class="fab fa-react"></i> React</div>
                        <div class="tech-item"><i class="fab fa-laravel"></i> Laravel</div>
                        <div class="tech-item"><i class="fas fa-bolt"></i> jQuery</div>
                    </div>
                </div>
                
                <div class="tech-category">
                    <h3><i class="fas fa-database"></i> Database</h3>
                    <div class="tech-items">
                        <div class="tech-item"><i class="fas fa-database"></i> MySQL</div>
                    </div>
                </div>
                
                <div class="tech-category">
                    <h3><i class="fas fa-tools"></i> Tools</h3>
                    <div class="tech-items">
                        <div class="tech-item"><i class="fab fa-git-alt"></i> Git</div>
                        <div class="tech-item"><i class="fas fa-code"></i> VS Code</div>
                        <div class="tech-item"><i class="fab fa-github"></i> GitHub</div>
                    </div>
                </div>
            </div>
        </div>
        
        <div class="card">
            <h2><i class="fas fa-briefcase"></i> Projects</h2>
            <div class="projects-grid">
                <div class="project">
                    <h3>E-Commerce Platform</h3>
                    <p>Platform e-commerce lengkap dengan dashboard admin, sistem pembayaran, dan manajemen inventaris.</p>
                    <div class="project-tech">
                        <span>Laravel</span>
                        <span>MySQL</span>
                        <span>JavaScript</span>
                    </div>
                    <a href="#" class="badge"><i class="fas fa-external-link-alt"></i> View Project</a>
                </div>
                
                <div class="project">
                    <h3>Task Management App</h3>
                    <p>Aplikasi manajemen tugas dengan fitur drag-and-drop, kolaborasi tim, dan notifikasi real-time.</p>
                    <div class="project-tech">
                        <span>React</span>
                        <span>Node.js</span>
                        <span>MongoDB</span>
                    </div>
                    <a href="#" class="badge"><i class="fas fa-external-link-alt"></i> View Project</a>
                </div>
                
                <div class="project">
                    <h3>Portfolio Website</h3>
                    <p>Website portfolio interaktif dengan animasi modern dan desain responsif.</p>
                    <div class="project-tech">
                        <span>HTML/CSS</span>
                        <span>JavaScript</span>
                        <span>GSAP</span>
                    </div>
                    <a href="#" class="badge"><i class="fas fa-external-link-alt"></i> View Project</a>
                </div>
            </div>
        </div>
        
        <div class="card">
            <h2><i class="fas fa-trophy"></i> Achievements</h2>
            <div class="projects-grid">
                <div class="project">
                    <h3><i class="fas fa-award"></i> Hackathon Winner</h3>
                    <p>Memenangkan hackathon nasional dengan membuat solusi inovatif untuk masalah pendidikan.</p>
                </div>
                
                <div class="project">
                    <h3><i class="fas fa-certificate"></i> Open Source Contributor</h3>
                    <p>Berkontribusi pada beberapa proyek open source dengan fokus pada tools developer.</p>
                </div>
                
                <div class="project">
                    <h3><i class="fas fa-medal"></i> Coding Challenge Champion</h3>
                    <p>Mendapat posisi pertama dalam kompetisi coding challenge yang diadakan oleh komunitas developer.</p>
                </div>
            </div>
        </div>
    </div>
    
    <div class="quote">
        <p>"Code is like humor. When you have to explain it, it's bad." - Cory House</p>
    </div>
    
    <div class="social-links">
        <a href="https://github.com/ArtaPradana" class="social-link"><i class="fab fa-github"></i></a>
        <a href="mailto:artapradana11@gmail.com" class="social-link"><i class="fas fa-envelope"></i></a>
        <a href="#" class="social-link"><i class="fab fa-linkedin"></i></a>
        <a href="#" class="social-link"><i class="fab fa-twitter"></i></a>
        <a href="#" class="social-link"><i class="fab fa-instagram"></i></a>
    </div>
    
    <div class="footer">
        <p>Made with <i class="fas fa-heart" style="color: var(--secondary);"></i> by I Made Arta Pradana</p>
        <p>© 2023 - All rights reserved</p>
    </div>

    <script>
        // Animasi untuk elemen stat
        document.addEventListener('DOMContentLoaded', function() {
            const stats = document.querySelectorAll('.stat-number');
            stats.forEach(stat => {
                const target = parseInt(stat.textContent);
                let count = 0;
                const duration = 2000; // ms
                const increment = target / (duration / 16);

                const updateCount = () => {
                    if (count < target) {
                        count += increment;
                        stat.textContent = Math.round(count) + '+';
                        setTimeout(updateCount, 16);
                    } else {
                        stat.textContent = target + '+';
                    }
                };

                setTimeout(updateCount, 500);
            });
        });
    </script>

</body>
</html>
