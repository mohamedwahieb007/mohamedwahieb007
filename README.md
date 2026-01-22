<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mohamed Hassan - Full-Stack .NET Developer</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: #0d1117;
            color: #ffffff;
            line-height: 1.6;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }

        /* Header Section */
        .header {
            text-align: center;
            padding: 40px 0;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            border-radius: 0 0 50px 50px;
            margin-bottom: 40px;
        }

        .header h1 {
            font-size: 3rem;
            margin-bottom: 10px;
            animation: fadeInDown 1s ease;
        }

        .header p {
            font-size: 1.5rem;
            opacity: 0.9;
        }

        @keyframes fadeInDown {
            from {
                opacity: 0;
                transform: translateY(-20px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        /* Typing Animation */
        .typing-container {
            text-align: center;
            margin: 30px 0;
        }

        .typing-text {
            font-size: 1.5rem;
            color: #00D9FF;
            font-family: 'Fira Code', monospace;
        }

        /* Social Links */
        .social-links {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 15px;
            margin: 30px 0;
        }

        .social-link {
            display: inline-block;
            padding: 12px 24px;
            border-radius: 8px;
            text-decoration: none;
            color: white;
            font-weight: bold;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }

        .social-link:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.3);
        }

        .linkedin { background-color: #0077B5; }
        .github { background-color: #333; }
        .gmail { background-color: #D14836; }
        .whatsapp { background-color: #25D366; }

        /* Stats Badges */
        .stats-badges {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin: 20px 0;
            flex-wrap: wrap;
        }

        .badge {
            background: linear-gradient(135deg, #1a1b27 0%, #2d2d44 100%);
            padding: 10px 20px;
            border-radius: 8px;
            border: 1px solid #00D9FF;
            color: #00D9FF;
            font-weight: bold;
        }

        /* Section Styles */
        .section {
            margin: 50px 0;
            padding: 30px;
            background-color: #161b22;
            border-radius: 15px;
            border: 1px solid #30363d;
        }

        .section-title {
            font-size: 2rem;
            margin-bottom: 25px;
            color: #00D9FF;
            border-bottom: 2px solid #00D9FF;
            padding-bottom: 10px;
            display: inline-block;
        }

        /* About Me Section */
        .about-container {
            display: flex;
            gap: 40px;
            align-items: flex-start;
            flex-wrap: wrap;
        }

        .about-text {
            flex: 1;
            min-width: 300px;
        }

        .about-text p {
            margin-bottom: 15px;
            font-size: 1.1rem;
        }

        .about-image {
            flex: 0 0 400px;
        }

        .about-image img {
            width: 100%;
            border-radius: 10px;
        }

        /* YAML Style Box */
        .yaml-box {
            background-color: #1a1b27;
            border-radius: 10px;
            padding: 20px;
            margin: 20px 0;
            border-left: 4px solid #00D9FF;
            font-family: 'Fira Code', monospace;
        }

        .yaml-box pre {
            color: #e6e6e6;
            white-space: pre-wrap;
            line-height: 1.8;
        }

        .yaml-key {
            color: #00D9FF;
        }

        .yaml-value {
            color: #98c379;
        }

        /* Highlights List */
        .highlights {
            list-style: none;
            margin-top: 20px;
        }

        .highlights li {
            padding: 10px 0;
            padding-left: 30px;
            position: relative;
            font-size: 1.1rem;
        }

        .highlights li::before {
            content: '';
            position: absolute;
            left: 0;
            top: 50%;
            transform: translateY(-50%);
            width: 20px;
            height: 20px;
            background-size: contain;
        }

        /* Tech Stack Section */
        .tech-category {
            margin: 30px 0;
        }

        .tech-category h3 {
            color: #ffffff;
            margin-bottom: 15px;
            font-size: 1.3rem;
        }

        .tech-badges {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            justify-content: center;
        }

        .tech-badge {
            display: inline-flex;
            align-items: center;
            padding: 8px 16px;
            border-radius: 6px;
            font-weight: bold;
            font-size: 0.9rem;
            color: white;
            transition: transform 0.2s ease;
        }

        .tech-badge:hover {
            transform: scale(1.05);
        }

        /* Tech Badge Colors */
        .csharp { background-color: #239120; }
        .dotnet { background-color: #512BD4; }
        .angular { background-color: #DD0031; }
        .typescript { background-color: #007ACC; }
        .javascript { background-color: #F7DF1E; color: black; }
        .html { background-color: #E34F26; }
        .css { background-color: #1572B6; }
        .bootstrap { background-color: #563D7C; }
        .sqlserver { background-color: #CC2927; }
        .clean-arch { background-color: #00C7B7; }
        .cqrs { background-color: #FF6B6B; }
        .repository { background-color: #4ECDC4; }
        .mediator { background-color: #9B59B6; }
        .solid { background-color: #45B8AC; }
        .ntier { background-color: #E74C3C; }
        .oop { background-color: #3498DB; }
        .patterns { background-color: #F39C12; }
        .signalr { background-color: #512BD4; }
        .stripe { background-color: #008CDD; }
        .openai { background-color: #412991; }
        .rest { background-color: #009688; }
        .swagger { background-color: #85EA2D; color: black; }
        .jwt { background-color: #000000; }
        .git { background-color: #F05032; }
        .github-badge { background-color: #181717; }
        .vs { background-color: #5C2D91; }
        .vscode { background-color: #007ACC; }
        .postman { background-color: #FF6C37; }
        .xunit { background-color: #512BD4; }
        .testing { background-color: #25A162; }
        .agile { background-color: #0052CC; }
        .scrum { background-color: #6DB33F; }

        /* Projects Section */
        .project-card {
            background: linear-gradient(135deg, #1a1b27 0%, #252836 100%);
            border-radius: 15px;
            padding: 30px;
            margin: 30px 0;
            border: 1px solid #30363d;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }

        .project-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 30px rgba(0, 217, 255, 0.1);
        }

        .project-title {
            font-size: 1.8rem;
            color: #00D9FF;
            margin-bottom: 10px;
        }

        .project-badges {
            display: flex;
            gap: 10px;
            margin: 15px 0;
            flex-wrap: wrap;
        }

        .project-badge {
            padding: 6px 12px;
            border-radius: 20px;
            font-size: 0.85rem;
            font-weight: bold;
        }

        .badge-success { background-color: #28a745; }
        .badge-blue { background-color: #007bff; }
        .badge-orange { background-color: #fd7e14; }
        .badge-purple { background-color: #6f42c1; }

        .project-description {
            font-size: 1.1rem;
            color: #b0b0b0;
            margin: 15px 0;
            padding-left: 20px;
            border-left: 3px solid #00D9FF;
        }

        .project-links {
            display: flex;
            gap: 15px;
            margin-top: 20px;
            flex-wrap: wrap;
        }

        .project-link {
            padding: 10px 20px;
            border-radius: 8px;
            text-decoration: none;
            color: white;
            font-weight: bold;
            transition: transform 0.2s ease;
        }

        .project-link:hover {
            transform: scale(1.05);
        }

        .link-demo { background-color: #00C7B7; }
        .link-frontend { background-color: #DD0031; }
        .link-backend { background-color: #512BD4; }
        .link-github { background-color: #181717; }

        /* Expandable Details */
        .details-container {
            margin-top: 20px;
        }

        .details-toggle {
            background-color: #30363d;
            color: #00D9FF;
            padding: 12px 20px;
            border: none;
            border-radius: 8px;
            cursor: pointer;
            font-size: 1rem;
            font-weight: bold;
            transition: background-color 0.3s ease;
        }

        .details-toggle:hover {
            background-color: #3d4450;
        }

        .details-content {
            display: none;
            margin-top: 20px;
            padding: 20px;
            background-color: #1a1b27;
            border-radius: 10px;
        }

        .details-content.active {
            display: block;
        }

        /* Feature Table */
        .feature-table {
            width: 100%;
            border-collapse: collapse;
            margin: 20px 0;
        }

        .feature-table th,
        .feature-table td {
            padding: 15px;
            text-align: left;
            border-bottom: 1px solid #30363d;
        }

        .feature-table th {
            background-color: #21262d;
            color: #00D9FF;
        }

        .feature-table tr:hover {
            background-color: #21262d;
        }

        /* Experience Section */
        .experience-card {
            background: linear-gradient(135deg, #1a1b27 0%, #252836 100%);
            border-radius: 15px;
            padding: 30px;
            margin: 30px 0;
            border-left: 4px solid #00D9FF;
        }

        .experience-header {
            text-align: center;
            margin-bottom: 20px;
        }

        .experience-title {
            font-size: 1.5rem;
            color: #ffffff;
        }

        .experience-company {
            color: #00D9FF;
            font-size: 1.2rem;
            margin: 10px 0;
        }

        .experience-meta {
            color: #8b949e;
        }

        .achievements-box {
            background-color: #1a1b27;
            border-radius: 10px;
            padding: 20px;
            margin-top: 20px;
            font-family: 'Fira Code', monospace;
        }

        .achievements-box pre {
            color: #98c379;
            white-space: pre-wrap;
            line-height: 1.8;
        }

        /* GitHub Stats Section */
        .github-stats {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 20px;
            margin: 30px 0;
        }

        .github-stats img {
            max-width: 100%;
            height: auto;
            border-radius: 10px;
        }

        /* Education Section */
        .education-card {
            text-align: center;
            padding: 30px;
        }

        .education-icon {
            font-size: 4rem;
            margin-bottom: 20px;
        }

        .education-degree {
            font-size: 1.5rem;
            color: #00D9FF;
            margin-bottom: 10px;
        }

        .education-university {
            font-size: 1.2rem;
            color: #ffffff;
            margin-bottom: 20px;
        }

        .education-details {
            display: flex;
            justify-content: center;
            gap: 50px;
            flex-wrap: wrap;
        }

        .education-item {
            text-align: center;
        }

        .education-label {
            color: #8b949e;
            font-size: 0.9rem;
        }

        .education-value {
            font-size: 1.3rem;
            color: #00D9FF;
            font-weight: bold;
        }

        /* Certifications Table */
        .cert-table {
            width: 100%;
            border-collapse: collapse;
            margin: 20px auto;
            max-width: 800px;
        }

        .cert-table th,
        .cert-table td {
            padding: 15px 20px;
            text-align: center;
            border-bottom: 1px solid #30363d;
        }

        .cert-table th {
            background-color: #21262d;
            color: #00D9FF;
        }

        /* Languages Table */
        .lang-table {
            width: 100%;
            max-width: 500px;
            margin: 20px auto;
            border-collapse: collapse;
        }

        .lang-table td {
            padding: 15px 20px;
            text-align: center;
            border-bottom: 1px solid #30363d;
        }

        .lang-flag {
            font-size: 1.5rem;
        }

        /* Contact Section */
        .contact-section {
            text-align: center;
        }

        .contact-gif {
            width: 100px;
            margin-bottom: 30px;
        }

        .contact-links {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 15px;
            margin: 30px 0;
        }

        .contact-link {
            padding: 15px 25px;
            border-radius: 10px;
            text-decoration: none;
            color: white;
            font-weight: bold;
            font-size: 1rem;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }

        .contact-link:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.3);
        }

        .contact-info {
            font-size: 1.2rem;
            color: #8b949e;
            margin-top: 20px;
        }

        /* Footer Section */
        .footer {
            text-align: center;
            padding: 50px 0;
            margin-top: 50px;
        }

        .quote {
            font-size: 1.3rem;
            font-style: italic;
            color: #8b949e;
            margin-bottom: 30px;
        }

        .quote span {
            color: #00D9FF;
        }

        .footer-wave {
            width: 100%;
            margin-top: 30px;
        }

        .thanks-message {
            font-size: 1.5rem;
            color: #00D9FF;
            margin: 30px 0;
        }

        .footer-badges {
            display: flex;
            justify-content: center;
            gap: 15px;
            flex-wrap: wrap;
            margin-top: 20px;
        }

        .footer-badge {
            padding: 10px 20px;
            border-radius: 8px;
            font-weight: bold;
        }

        .badge-red { background-color: #dc3545; }
        .badge-green { background-color: #28a745; }
        .badge-purple { background-color: #512BD4; }

        /* Responsive Design */
        @media (max-width: 768px) {
            .header h1 {
                font-size: 2rem;
            }

            .header p {
                font-size: 1.2rem;
            }

            .typing-text {
                font-size: 1.2rem;
            }

            .about-container {
                flex-direction: column;
            }

            .about-image {
                flex: 0 0 auto;
                width: 100%;
            }

            .section-title {
                font-size: 1.5rem;
            }

            .project-title {
                font-size: 1.4rem;
            }

            .education-details {
                gap: 30px;
            }

            .github-stats {
                flex-direction: column;
                align-items: center;
            }
        }

        /* Animations */
        @keyframes pulse {
            0%, 100% { opacity: 1; }
            50% { opacity: 0.5; }
        }

        .animate-pulse {
            animation: pulse 2s infinite;
        }

        /* Divider */
        .divider {
            height: 1px;
            background: linear-gradient(90deg, transparent, #30363d, transparent);
            margin: 40px 0;
        }
    </style>
    <link href="https://fonts.googleapis.com/css2?family=Fira+Code:wght@400;500;600&display=swap" rel="stylesheet">
</head>
<body>

    <!-- Header Section -->
    <header class="header">
        <h1>👋 Mohamed Hassan</h1>
        <p>Full-Stack .NET Developer</p>
    </header>

    <div class="container">

        <!-- Typing Animation -->
        <div class="typing-container">
            <p class="typing-text">Full-Stack .NET Developer 💻 | Clean Architecture Enthusiast 🏗️ | Building Scalable Applications 🚀</p>
        </div>

        <!-- Social Links -->
        <div class="social-links">
            <a href="https://linkedin.com/in/YOUR_LINKEDIN_USERNAME" class="social-link linkedin">
                🔗 LinkedIn
            </a>
            <a href="https://github.com/YOUR_GITHUB_USERNAME" class="social-link github">
                💻 GitHub
            </a>
            <a href="mailto:mohamedwahieb57@gmail.com" class="social-link gmail">
                📧 Gmail
            </a>
            <a href="https://wa.me/201068382382" class="social-link whatsapp">
                💬 WhatsApp
            </a>
        </div>

        <!-- Stats Badges -->
        <div class="stats-badges">
            <span class="badge">👀 Profile Views: 1000+</span>
            <span class="badge">👥 Followers: Growing</span>
        </div>

        <div class="divider"></div>

        <!-- About Me Section -->
        <section class="section">
            <h2 class="section-title">🧑‍💻 About Me</h2>
            
            <div class="about-container">
                <div class="about-text">
                    <p>Hey there! I'm <strong>Mohamed Hassan</strong> 👋</p>
                    
                    <p>A passionate <strong>Full-Stack .NET Developer</strong> from <strong>Cairo, Egypt</strong> 🇪🇬 who loves turning complex problems into elegant, scalable solutions.</p>
                    
                    <p>I graduated from <strong>Fayoum University</strong> with a <strong>B.Sc. in Mechatronics Engineering</strong> (GPA: 3.33/4.0), where I built a <strong>Self-Driving Car</strong> 🚗 as my graduation project and received an <strong>Excellent</strong> grade!</p>
                    
                    <p>I specialize in the <strong>Microsoft .NET ecosystem</strong>, crafting clean, scalable backend systems using <strong>C#</strong>, <strong>ASP.NET Core</strong>, and <strong>Entity Framework Core</strong>. I'm a firm believer in <strong>Clean Architecture</strong>, <strong>SOLID principles</strong>, and writing code that's a pleasure to maintain.</p>

                    <div class="yaml-box">
                        <pre>
<span class="yaml-key">🎯 Role:</span> <span class="yaml-value">Full-Stack .NET Developer</span>
<span class="yaml-key">📍 Location:</span> <span class="yaml-value">Cairo, Egypt</span>
<span class="yaml-key">🎓 Education:</span> <span class="yaml-value">B.Sc. Mechatronics Engineering</span>
<span class="yaml-key">🏫 University:</span> <span class="yaml-value">Fayoum University (2018-2023)</span>
<span class="yaml-key">📊 GPA:</span> <span class="yaml-value">3.33/4.0 (84.5%)</span>
<span class="yaml-key">🚗 Grad Project:</span> <span class="yaml-value">Self-Driving Car (Excellent Grade)</span>
<span class="yaml-key">🌍 Languages:</span> <span class="yaml-value">Arabic (Native) | English (IELTS 7.5)</span>
                        </pre>
                    </div>

                    <h3 style="color: #00D9FF; margin-top: 30px;">🔹 What I'm Up To</h3>
                    <ul class="highlights">
                        <li>🔭 Building <strong>KORIEK</strong> - Automotive Service Marketplace</li>
                        <li>🌱 Learning <strong>Microservices</strong>, <strong>Docker</strong> & <strong>Azure</strong></li>
                        <li>👨‍🏫 Trained <strong>100+ students</strong> in programming</li>
                        <li>🚀 Created <strong>100+ RESTful API endpoints</strong></li>
                        <li>⚡ Achieved <strong>&lt;200ms response times</strong> in production</li>
                        <li>💬 Ask me about <strong>.NET, Clean Architecture, API Design</strong></li>
                        <li>📫 Reach me at <strong>mohamedwahieb57@gmail.com</strong></li>
                    </ul>
                </div>

                <div class="about-image">
                    <img src="https://user-images.githubusercontent.com/74038190/229223263-cf2e4b07-2615-4f87-9c38-e37600f8381a.gif" alt="Coding Animation">
                </div>
            </div>
        </section>

        <div class="divider"></div>

        <!-- Tech Stack Section -->
        <section class="section">
            <h2 class="section-title">🛠️ Tech Stack</h2>

            <!-- Backend -->
            <div class="tech-category">
                <h3>💻 Backend Development</h3>
                <div class="tech-badges">
                    <span class="tech-badge csharp">C#</span>
                    <span class="tech-badge dotnet">.NET</span>
                    <span class="tech-badge dotnet">ASP.NET Core</span>
                    <span class="tech-badge dotnet">Entity Framework</span>
                    <span class="tech-badge dotnet">Web API</span>
                    <span class="tech-badge dotnet">LINQ</span>
                    <span class="tech-badge dotnet">Dapper</span>
                </div>
            </div>

            <!-- Frontend -->
            <div class="tech-category">
                <h3>🎨 Frontend Development</h3>
                <div class="tech-badges">
                    <span class="tech-badge angular">Angular</span>
                    <span class="tech-badge typescript">TypeScript</span>
                    <span class="tech-badge javascript">JavaScript</span>
                    <span class="tech-badge html">HTML5</span>
                    <span class="tech-badge css">CSS3</span>
                    <span class="tech-badge bootstrap">Bootstrap</span>
                </div>
            </div>

            <!-- Database -->
            <div class="tech-category">
                <h3>🗄️ Database</h3>
                <div class="tech-badges">
                    <span class="tech-badge sqlserver">SQL Server</span>
                    <span class="tech-badge sqlserver">T-SQL</span>
                </div>
            </div>

            <!-- Architecture -->
            <div class="tech-category">
                <h3>🏗️ Architecture & Patterns</h3>
                <div class="tech-badges">
                    <span class="tech-badge clean-arch">Clean Architecture</span>
                    <span class="tech-badge cqrs">CQRS</span>
                    <span class="tech-badge repository">Repository Pattern</span>
                    <span class="tech-badge mediator">Mediator Pattern</span>
                    <span class="tech-badge solid">SOLID Principles</span>
                    <span class="tech-badge ntier">N-Tier Architecture</span>
                    <span class="tech-badge oop">OOP</span>
                    <span class="tech-badge patterns">Design Patterns</span>
                </div>
            </div>

            <!-- Integrations -->
            <div class="tech-category">
                <h3>🔌 Integrations & APIs</h3>
                <div class="tech-badges">
                    <span class="tech-badge signalr">SignalR</span>
                    <span class="tech-badge stripe">Stripe</span>
                    <span class="tech-badge openai">OpenAI API</span>
                    <span class="tech-badge rest">REST API</span>
                    <span class="tech-badge swagger">Swagger</span>
                </div>
            </div>

            <!-- Security -->
            <div class="tech-category">
                <h3>🔐 Security</h3>
                <div class="tech-badges">
                    <span class="tech-badge jwt">JWT</span>
                    <span class="tech-badge dotnet">ASP.NET Identity</span>
                </div>
            </div>

            <!-- Tools -->
            <div class="tech-category">
                <h3>🔧 Tools & DevOps</h3>
                <div class="tech-badges">
                    <span class="tech-badge git">Git</span>
                    <span class="tech-badge github-badge">GitHub</span>
                    <span class="tech-badge git">GitFlow</span>
                    <span class="tech-badge vs">Visual Studio</span>
                    <span class="tech-badge vscode">VS Code</span>
                    <span class="tech-badge postman">Postman</span>
                </div>
            </div>

            <!-- Testing -->
            <div class="tech-category">
                <h3>🧪 Testing</h3>
                <div class="tech-badges">
                    <span class="tech-badge xunit">xUnit</span>
                    <span class="tech-badge testing">Unit Testing</span>
                </div>
            </div>

            <!-- Methodologies -->
            <div class="tech-category">
                <h3>📋 Methodologies</h3>
                <div class="tech-badges">
                    <span class="tech-badge agile">Agile</span>
                    <span class="tech-badge scrum">Scrum</span>
                </div>
            </div>
        </section>

        <div class="divider"></div>

        <!-- Projects Section -->
        <section class="section">
            <h2 class="section-title">🚀 Featured Projects</h2>

            <!-- KORIEK Project -->
            <div class="project-card">
                <h3 class="project-title">🚗 KORIEK - Automotive Service Marketplace</h3>
                
                <div class="project-badges">
                    <span class="project-badge badge-success">✅ Completed</span>
                    <span class="project-badge badge-blue">Full Stack</span>
                    <span class="project-badge badge-orange">Dec 2025</span>
                </div>

                <p class="project-description">
                    🔹 <strong>Full-stack marketplace</strong> connecting car owners with verified workshops for service discovery, real-time booking, and secure payments.
                </p>

                <div class="project-links">
                    <a href="YOUR_DEMO_LINK" class="project-link link-demo">🌐 Live Demo</a>
                    <a href="YOUR_FRONTEND_REPO" class="project-link link-frontend">🎨 Frontend Code</a>
                    <a href="YOUR_BACKEND_REPO" class="project-link link-backend">⚙️ Backend Code</a>
                </div>

                <div class="details-container">
                    <button class="details-toggle" onclick="toggleDetails('koriek-details')">📋 Click to see full project details</button>
                    
                    <div id="koriek-details" class="details-content">
                        <h4 style="color: #00D9FF; margin-bottom: 15px;">✨ Key Features</h4>
                        
                        <table class="feature-table">
                            <tr>
                                <th>Feature</th>
                                <th>Description</th>
                            </tr>
                            <tr>
                                <td>📡 <strong>100+ RESTful Endpoints</strong></td>
                                <td>Account, Booking, Payment, Workshop, AI Chat, Car, Indicators, Reviews, Notifications</td>
                            </tr>
                            <tr>
                                <td>🗄️ <strong>30+ Database Tables</strong></td>
                                <td>Normalized design with optimized queries achieving &lt;200ms response times</td>
                            </tr>
                            <tr>
                                <td>🔔 <strong>Real-time Notifications</strong></td>
                                <td>SignalR integration for instant updates</td>
                            </tr>
                            <tr>
                                <td>💳 <strong>Payment Processing</strong></td>
                                <td>Stripe/Paymob integration for secure transactions</td>
                            </tr>
                            <tr>
                                <td>🤖 <strong>AI Chatbot</strong></td>
                                <td>OpenAI GPT integration for customer assistance</td>
                            </tr>
                            <tr>
                                <td>🔐 <strong>Security</strong></td>
                                <td>JWT Authentication, Role-based Authorization, HTTPS enforcement</td>
                            </tr>
                            <tr>
                                <td>✅ <strong>Testing</strong></td>
                                <td>Comprehensive Unit Testing with xUnit</td>
                            </tr>
                            <tr>
                                <td>📚 <strong>Documentation</strong></td>
                                <td>Complete Swagger/OpenAPI documentation</td>
                            </tr>
                        </table>

                        <h4 style="color: #00D9FF; margin: 20px 0 15px;">🛠️ Tech Stack Used</h4>
                        <div class="tech-badges">
                            <span class="tech-badge dotnet">ASP.NET Core 9</span>
                            <span class="tech-badge angular">Angular</span>
                            <span class="tech-badge sqlserver">SQL Server</span>
                            <span class="tech-badge clean-arch">Clean Architecture</span>
                            <span class="tech-badge cqrs">CQRS</span>
                            <span class="tech-badge signalr">SignalR</span>
                            <span class="tech-badge stripe">Stripe</span>
                            <span class="tech-badge openai">OpenAI GPT</span>
                            <span class="tech-badge jwt">JWT</span>
                            <span class="tech-badge xunit">xUnit</span>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Travel Booking Project -->
            <div class="project-card">
                <h3 class="project-title">✈️ Tare2k A5dar - Travel Booking System</h3>
                
                <div class="project-badges">
                    <span class="project-badge badge-success">✅ Completed</span>
                    <span class="project-badge badge-purple">Console App</span>
                    <span class="project-badge badge-orange">July 2025</span>
                </div>

                <p class="project-description">
                    🔹 <strong>Console-based booking system</strong> with complete lifecycle: flight reservation, cancellation, payment simulation, and loyalty points.
                </p>

                <div class="project-links">
                    <a href="YOUR_REPO_LINK" class="project-link link-github">⚙️ View Code</a>
                </div>

                <div class="details-container">
                    <button class="details-toggle" onclick="toggleDetails('travel-details')">📋 Click to see full project details</button>
                    
                    <div id="travel-details" class="details-content">
                        <h4 style="color: #00D9FF; margin-bottom: 15px;">✨ Key Features</h4>
                        
                        <table class="feature-table">
                            <tr>
                                <th>Feature</th>
                                <th>Description</th>
                            </tr>
                            <tr>
                                <td>🏗️ <strong>OOP Architecture</strong></td>
                                <td>6 classes (Trip, Customer, Booking, BookingManager, CancellationManager, PaymentManager) following SRP</td>
                            </tr>
                            <tr>
                                <td>💾 <strong>File Persistence</strong></td>
                                <td>System.IO for data manipulation without LINQ or database</td>
                            </tr>
                            <tr>
                                <td>🔄 <strong>Complete Lifecycle</strong></td>
                                <td>Flight reservation, cancellation, payment simulation, loyalty points</td>
                            </tr>
                        </table>

                        <h4 style="color: #00D9FF; margin: 20px 0 15px;">🛠️ Tech Stack Used</h4>
                        <div class="tech-badges">
                            <span class="tech-badge csharp">C#</span>
                            <span class="tech-badge dotnet">.NET Console</span>
                            <span class="tech-badge oop">OOP</span>
                            <span class="tech-badge solid">SOLID Principles</span>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <div class="divider"></div>

        <!-- Professional Experience Section -->
        <section class="section">
            <h2 class="section-title">💼 Professional Experience</h2>

            <!-- Full-Stack Developer -->
            <div class="experience-card">
                <div class="experience-header">
                    <h3 class="experience-title">🏢 Full-Stack .NET Developer</h3>
                    <p class="experience-company">Information Technology Institute (ITI) - Intensive Code Camp</p>
                    <p class="experience-meta">📍 Fayoum, Egypt | 📅 Jul 2025 - Dec 2025</p>
                </div>

                <div class="achievements-box">
                    <pre>
🏆 ACHIEVEMENTS
─────────────────────────────────────────────────────────────────
✅ Selected as 1 of 30 candidates for competitive 4-month program
✅ Mastered full-stack development with ASP.NET Core & Angular
✅ Led development of KORIEK platform (100+ APIs, 30+ tables)
✅ Served 50+ concurrent users with <200ms response times
✅ Integrated Stripe/Paymob, SignalR, and OpenAI GPT
✅ Implemented JWT authentication & role-based authorization
✅ Applied Clean Architecture with Repository Pattern & CQRS
✅ Collaborated in Agile environment with daily standups
                    </pre>
                </div>
            </div>

            <!-- Technical Instructor -->
            <div class="experience-card">
                <div class="experience-header">
                    <h3 class="experience-title">🎓 Technical Instructor - Embedded Systems & Programming</h3>
                    <p class="experience-company">Information Technology Institute (ITI)</p>
                    <p class="experience-meta">📍 Cairo, Egypt | 📅 Jul 2023 - Oct 2023</p>
                </div>

                <div class="achievements-box">
                    <pre>
🏆 ACHIEVEMENTS
─────────────────────────────────────────────────────────────────
✅ Trained 100+ students achieving 85% satisfaction rate
✅ Delivered structured curriculum on programming & OOP concepts
✅ Improved debugging efficiency by 60%
✅ Mentored 15 graduation project teams (100% success rate)
✅ Provided architecture guidance & code reviews
                    </pre>
                </div>
            </div>
        </section>

        <div class="divider"></div>

        <!-- GitHub Statistics Section -->
        <section class="section">
            <h2 class="section-title">📊 GitHub Statistics</h2>

            <div class="github-stats">
                <img src="https://github-readme-stats.vercel.app/api?username=YOUR_GITHUB_USERNAME&show_icons=true&theme=tokyonight&hide_border=true&bg_color=0D1117&title_color=00D9FF&icon_color=00D9FF&text_color=FFFFFF&count_private=true" alt="GitHub Stats">
                <img src="https://github-readme-streak-stats.herokuapp.com/?user=YOUR_GITHUB_USERNAME&theme=tokyonight&hide_border=true&background=0D1117&ring=00D9FF&fire=00D9FF&currStreakLabel=00D9FF" alt="GitHub Streak">
            </div>

            <div class="github-stats">
                <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=YOUR_GITHUB_USERNAME&layout=compact&theme=tokyonight&hide_border=true&bg_color=0D1117&title_color=00D9FF&text_color=FFFFFF" alt="Top Languages">
            </div>
        </section>

        <div class="divider"></div>

        <!-- GitHub Trophies Section -->
        <section class="section">
            <h2 class="section-title">🏆 GitHub Trophies</h2>

            <div style="text-align: center;">
                <img src="https://github-profile-trophy.vercel.app/?username=YOUR_GITHUB_USERNAME&theme=tokyonight&no-frame=true&no-bg=true&column=7" alt="GitHub Trophies" style="max-width: 100%;">
            </div>
        </section>

        <div class="divider"></div>

        <!-- Contribution Graph Section -->
        <section class="section">
            <h2 class="section-title">📈 Contribution Graph</h2>

            <div style="text-align: center;">
                <img src="https://github-readme-activity-graph.vercel.app/graph?username=YOUR_GITHUB_USERNAME&theme=tokyo-night&hide_border=true&bg_color=0D1117&color=00D9FF&line=00D9FF&point=FFFFFF" alt="Contribution Graph" style="max-width: 100%; border-radius: 10px;">
            </div>
        </section>

        <div class="divider"></div>

        <!-- Education Section -->
        <section class="section">
            <h2 class="section-title">🎓 Education</h2>

            <div class="education-card">
                <div class="education-icon">🎓</div>
                <h3 class="education-degree">B.Sc. Mechatronics Engineering</h3>
                <p class="education-university">Fayoum University | 📅 2018 - 2023</p>

                <div class="education-details">
                    <div class="education-item">
                        <p class="education-label">📊 GPA</p>
                        <p class="education-value">3.33 / 4.0 (84.5%)</p>
                    </div>
                    <div class="education-item">
                        <p class="education-label">🚗 Graduation Project</p>
                        <p class="education-value">Self-Driving Car (Excellent)</p>
                    </div>
                </div>
            </div>
        </section>

        <div class="divider"></div>

        <!-- Certifications Section -->
        <section class="section">
            <h2 class="section-title">📜 Certifications</h2>

            <table class="cert-table">
                <tr>
                    <th>🏅 Certificate</th>
                    <th>🏛️ Provider</th>
                    <th>📅 Year</th>
                </tr>
                <tr>
                    <td>📚 Database Fundamentals</td>
                    <td>MaharaTech (ITI)</td>
                    <td>2025</td>
                </tr>
                <tr>
                    <td>💻 Programming in C#</td>
                    <td>Coursera</td>
                    <td>2025</td>
                </tr>
            </table>
        </section>

        <div class="divider"></div>

        <!-- Languages Section -->
        <section class="section">
            <h2 class="section-title">🌐 Languages</h2>

            <table class="lang-table">
                <tr>
                    <td><span class="lang-flag">🇪🇬</span> <strong>Arabic</strong></td>
                    <td>Native Speaker</td>
                </tr>
                <tr>
                    <td><span class="lang-flag">🇬🇧</span> <strong>English</strong></td>
                    <td>Professional Proficiency (IELTS 7.5)</td>
                </tr>
            </table>
        </section>

        <div class="divider"></div>

        <!-- Contact Section -->
        <section class="section contact-section">
            <h2 class="section-title">🤝 Let's Connect!</h2>

            <img src="https://user-images.githubusercontent.com/74038190/235294012-0a55e343-37ad-4b0f-924f-c8431d9d2483.gif" alt="Handshake" class="contact-gif">

            <div class="contact-links">
                <a href="https://linkedin.com/in/YOUR_LINKEDIN_USERNAME" class="contact-link linkedin">🔗 Connect on LinkedIn</a>
                <a href="mailto:mohamedwahieb57@gmail.com" class="contact-link gmail">📧 Send Me an Email</a>
                <a href="https://wa.me/201068382382" class="contact-link whatsapp">💬 Chat on WhatsApp</a>
                <a href="https://github.com/YOUR_GITHUB_USERNAME" class="contact-link github">💻 Follow on GitHub</a>
            </div>

            <p class="contact-info">
                📧 mohamedwahieb57@gmail.com | 📱 +20 1068 382 382
            </p>
        </section>

        <!-- Footer Section -->
        <footer class="footer">
            <p class="quote">
                💡 <em>"Clean code always looks like it was written by someone who cares."</em> - <span>Robert C. Martin</span>
            </p>

            <img src="https://user-images.githubusercontent.com/74038190/212284100-561aa473-3905-4a80-b561-0d28506553ee.gif" alt="Wave" style="width: 100%; max-width: 700px; margin: 30px auto; display: block;">

            <p class="thanks-message">⭐ Thanks for visiting my profile! Let's build something amazing together! 🚀</p>

            <div class="footer-badges">
                <span class="footer-badge badge-red">Made with ❤️</span>
                <span class="footer-badge badge-green">From Egypt 🇪🇬</span>
                <span class="footer-badge badge-purple">Powered by .NET</span>
            </div>
        </footer>

    </div>

    <script>
        function toggleDetails(id) {
            const element = document.getElementById(id);
            element.classList.toggle('active');
        }

        // Typing animation effect
        const typingText = document.querySelector('.typing-text');
        const texts = [
            'Full-Stack .NET Developer 💻',
            'Clean Architecture Enthusiast 🏗️',
            'Building Scalable Web Applications 🚀',
            '100+ API Endpoints Created 📡',
            'Trained 100+ Students 👨‍🏫',
            'Always Learning & Improving 🌱'
        ];
        let textIndex = 0;
        let charIndex = 0;
        let isDeleting = false;

        function typeEffect() {
            const currentText = texts[textIndex];
            
            if (isDeleting) {
                typingText.textContent = currentText.substring(0, charIndex - 1);
                charIndex--;
            } else {
                typingText.textContent = currentText.substring(0, charIndex + 1);
                charIndex++;
            }

            if (!isDeleting && charIndex === currentText.length) {
                setTimeout(() => isDeleting = true, 2000);
            } else if (isDeleting && charIndex === 0) {
                isDeleting = false;
                textIndex = (textIndex + 1) % texts.length;
            }

            const speed = isDeleting ? 50 : 100;
            setTimeout(typeEffect, speed);
        }

        // Start typing animation
        typeEffect();

        // Smooth scroll for anchor links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });

        // Add fade-in animation on scroll
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -50px 0px'
        };

        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.style.opacity = '1';
                    entry.target.style.transform = 'translateY(0)';
                }
            });
        }, observerOptions);

        document.querySelectorAll('.section').forEach(section => {
            section.style.opacity = '0';
            section.style.transform = 'translateY(20px)';
            section.style.transition = 'opacity 0.6s ease, transform 0.6s ease';
            observer.observe(section);
        });
    </script>

</body>
</html>
