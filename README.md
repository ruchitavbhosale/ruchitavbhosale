<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>GitHub Profile README - Ruchita V Bhosale</title>
    <style>
        /* Modern GitHub Dark Mode Theme Variables */
        :root {
            --bg-primary: #0d1117;
            --bg-secondary: #161b22;
            --border-color: #30363d;
            --text-primary: #c9d1d9;
            --text-secondary: #8b949e;
            --accent-purple: #8a2be2;
            --accent-blue: #58a6ff;
            --accent-green: #3fb950;
            --glow-color: rgba(138, 43, 226, 0.35);
        }

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        body {
            background-color: var(--bg-primary);
            color: var(--text-primary);
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, Arial, sans-serif;
            line-height: 1.6;
            padding: 40px 20px;
            display: flex;
            justify-content: center;
        }

        /* Container inspired by github readme.jfif layout */
        .readme-container {
            width: 100%;
            max-width: 850px;
            background-color: var(--bg-primary);
            border: 1px solid var(--border-color);
            border-radius: 6px;
            padding: 40px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.6);
            animation: containerFadeIn 1.2s cubic-bezier(0.16, 1, 0.3, 1) both;
        }

        /* Animated Glowing Header Banner */
        .banner {
            width: 100%;
            height: 160px;
            border-radius: 6px;
            background: linear-gradient(-45deg, #0d1117, #1f1f3a, #161b22, #24143e);
            background-size: 400% 400%;
            border: 1px solid var(--border-color);
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            position: relative;
            overflow: hidden;
            margin-bottom: 35px;
            animation: gradientShift 15s ease infinite;
        }

        .banner-text {
            font-size: 2.4rem;
            font-weight: 800;
            letter-spacing: 3px;
            background: linear-gradient(45deg, #58a6ff, #8a2be2, #ff79c6, #58a6ff);
            background-size: 200% auto;
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            animation: shineText 4s linear infinite;
            text-align: center;
            z-index: 1;
        }

        .banner-subtitle {
            font-size: 0.95rem;
            color: var(--text-secondary);
            margin-top: 8px;
            letter-spacing: 1px;
            z-index: 1;
            animation: pulseFade 2s ease-in-out infinite alternate;
        }

        /* Standard Section Header featuring the iconic Purple Marker block from github readme.jfif */
        .section-title {
            font-size: 1.3rem;
            font-weight: 600;
            margin-top: 40px;
            margin-bottom: 18px;
            display: flex;
            align-items: center;
            border-bottom: 1px solid var(--border-color);
            padding-bottom: 8px;
        }

        .section-title::before {
            content: "█";
            color: var(--accent-purple);
            margin-right: 12px;
            font-size: 1.1rem;
            text-shadow: 0 0 10px var(--accent-purple);
            animation: blockPulse 1.5s ease-in-out infinite alternate;
        }

        p {
            color: var(--text-primary);
            font-size: 0.98rem;
            margin-bottom: 14px;
        }

        .highlight {
            color: var(--accent-blue);
            font-weight: 500;
        }

        /* Hover-Animated Grid for Tech Stack Badges */
        .badge-grid {
            display: flex;
            flex-wrap: wrap;
            gap: 12px;
            margin-top: 15px;
        }

        .badge {
            background-color: var(--bg-secondary);
            border: 1px solid var(--border-color);
            border-radius: 20px;
            padding: 8px 16px;
            font-size: 0.88rem;
            font-weight: 500;
            display: flex;
            align-items: center;
            gap: 8px;
            transition: all 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
            cursor: default;
        }

        .badge:hover {
            transform: translateY(-5px) scale(1.03);
            border-color: var(--accent-purple);
            box-shadow: 0 5px 15px var(--glow-color);
            color: #ffffff;
        }

        /* Interactive Timeline for Professional Experience */
        .timeline {
            margin-top: 20px;
            border-left: 2px solid var(--border-color);
            padding-left: 24px;
            position: relative;
        }

        .timeline-item {
            margin-bottom: 30px;
            position: relative;
        }

        .timeline-item::before {
            content: '';
            position: absolute;
            left: -31px;
            top: 6px;
            width: 12px;
            height: 12px;
            border-radius: 50%;
            background-color: var(--bg-primary);
            border: 2px solid var(--accent-blue);
            transition: all 0.3s ease;
        }

        .timeline-item:hover::before {
            background-color: var(--accent-purple);
            border-color: var(--accent-purple);
            transform: scale(1.3);
            box-shadow: 0 0 8px var(--accent-purple);
        }

        .job-title {
            font-weight: 600;
            font-size: 1.05rem;
            color: #ffffff;
            transition: color 0.3s ease;
        }

        .timeline-item:hover .job-title {
            color: var(--accent-blue);
        }

        .company-date {
            font-size: 0.85rem;
            color: var(--text-secondary);
            margin-bottom: 8px;
        }

        .job-desc {
            font-size: 0.92rem;
            color: var(--text-primary);
            padding-left: 20px;
        }

        .job-desc li {
            margin-bottom: 6px;
        }

        /* Grid Framework for Custom Performance Metrics Charts */
        .analytics-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
            gap: 20px;
            margin-top: 20px;
        }

        .card {
            background-color: var(--bg-secondary);
            border: 1px solid var(--border-color);
            border-radius: 6px;
            padding: 24px;
            text-align: center;
            position: relative;
            overflow: hidden;
            transition: border-color 0.3s, transform 0.3s;
        }

        .card:hover {
            border-color: #444c56;
            transform: translateY(-2px);
        }

        /* Subtle animated underline glow on metric cards */
        .card::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 100%;
            height: 3px;
            background: linear-gradient(90deg, transparent, var(--accent-purple), transparent);
            transform: scaleX(0);
            transition: transform 0.4s ease;
        }

        .card:hover::after {
            transform: scaleX(1);
        }

        .card-val {
            font-size: 2rem;
            font-weight: 700;
            color: var(--accent-green);
            margin-bottom: 6px;
        }

        .card-lbl {
            font-size: 0.85rem;
            color: var(--text-secondary);
            text-transform: uppercase;
            letter-spacing: 1.5px;
        }

        /* Core CSS Keyframe Animations */
        @keyframes containerFadeIn {
            from { opacity: 0; transform: translateY(30px); }
            to { opacity: 1; transform: translateY(0); }
        }

        @keyframes gradientShift {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }

        @keyframes shineText {
            to { background-position: 200% center; }
        }

        @keyframes pulseFade {
            from { opacity: 0.6; }
            to { opacity: 1; }
        }

        @keyframes blockPulse {
            from { opacity: 0.7; text-shadow: 0 0 4px var(--accent-purple); }
            to { opacity: 1; text-shadow: 0 0 12px var(--accent-purple); }
        }
    </style>
</head>
<body>

    <div class="readme-container">
        
        <!-- Animated Title Card Banner Component -->
        <div class="banner">
            <div class="banner-text">RUCHITA V BHOSALE</div>
            <div class="banner-subtitle">MCA Student • Full Stack Developer • HR Recruiter</div>
        </div>

        <!-- About Me Dashboard Module -->
        <div class="section-title">About Me</div>
        <p>I am an ambitious <span class="highlight">MCA Student</span> and tech enthusiast with a multi-disciplinary background spanning software systems, full-stack application logic, corporate data engineering, and talent recruitment workflows[cite: 1].</p>
        <p>I thrive on creating clean, structural, and beautifully integrated web interfaces while tracking key back-end and infrastructure analytics safely[cite: 1]. Currently based in Pune, pursuing my professional specialization path at <span class="highlight">MIT World Peace University</span>[cite: 1].</p>

        <!-- Tech Stack Component Block -->
        <div class="section-title">Tech Stack & Languages</div>
        <div class="badge-grid">
            <div class="badge">🌐 HTML5</div>
            <div class="badge">🎨 CSS3</div>
            <div class="badge">⚛️ React.js</div>
            <div class="badge">🟢 Node.js</div>
            <div class="badge">🚂 Express.js</div>
            <div class="badge">🍃 MongoDB</div>
            <div class="badge">🛢️ MySQL</div>
            <div class="badge">⚙️ C</div>
            <div class="badge">🛠️ C++</div>
            <div class="badge">☕ Java</div>
            <div class="badge">🟨 JavaScript</div>
            <div class="badge">🐘 PHP</div>
        </div>

        <!-- System & Framework Tools Badges -->
        <div class="section-title">Tools & Architecture Paradigms</div>
        <div class="badge-grid">
            <div class="badge">🐙 Git & GitHub</div>
            <div class="badge">💻 VS Code</div>
            <div class="badge">🤖 Android Studio</div>
            <div class="badge">📐 Figma & Adobe XD</div>
            <div class="badge">📊 MS Excel & Sheets</div>
            <div class="badge">🔑 RESTful APIs & JWT</div>
        </div>

        <!-- Animated Chronology Professional Timeline -->
        <div class="section-title">Experience Timeline</div>
        <div class="timeline">
            <div class="timeline-item">
                <div class="job-title">Full Stack Developer Intern</div>
                <div class="company-date">Skillected | June 2025 - December 2025</div>
                <ul class="job-desc">
                    <li>Engineered cleanly optimized responsive pages inside React.js framework environments[cite: 1].</li>
                    <li>Built node structural server integrations and handled safe database deployments[cite: 1].</li>
                </ul>
            </div>
            <div class="timeline-item">
                <div class="job-title">Associate Executive Intern (Data Analysis)</div>
                <div class="company-date">MDIndia Healthcare Services | January 2026 - March 2026</div>
                <ul class="job-desc">
                    <li>Analyzed intricate healthcare operations datasets using predictive Excel logic[cite: 1].</li>
                    <li>Managed secure record systems, data verification protocols, and strategic team reports[cite: 1].</li>
                </ul>
            </div>
            <div class="timeline-item">
                <div class="job-title">Executive Intern</div>
                <div class="company-date">Textualizes | April 2026 - June 2026</div>
                <ul class="job-desc">
                    <li>Supported key business logistics, continuous data tracking, and dynamic cross-team workflows[cite: 1].</li>
                </ul>
            </div>
        </div>

        <!-- Numerical Capability Analytical Block -->
        <div class="section-title">Performance Analytics</div>
        <div class="analytics-container">
            <div class="card">
                <div class="card-val">40+ WPM</div>
                <div class="card-lbl">Keyboard Sprint Velocity</div>
            </div>
            <div class="card">
                <div class="card-val">4 Languages</div>
                <div class="card-lbl">Global Linguistic Matrix</div>
            </div>
            <div class="card">
                <div class="card-val">6+ Certs</div>
                <div class="card-lbl">Verified Field Credentials</div>
            </div>
        </div>

    </div>

</body>
</html>
