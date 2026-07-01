<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>GitHub Profile README - Ruchita V Bhosale</title>
    <style>
        /* Modern Dark Theme Variables */
        :root {
            --bg-primary: #0d1117;
            --bg-secondary: #161b22;
            --border-color: #30363d;
            --text-primary: #c9d1d9;
            --text-secondary: #8b949e;
            --accent-purple: #8a2be2;
            --accent-blue: #58a6ff;
            --accent-green: #3fb950;
            --shadow-glow: rgba(138, 43, 226, 0.2);
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
            padding: 20px;
            display: flex;
            justify-content: center;
        }

        /* Container Layout */
        .readme-container {
            width: 100%;
            max-width: 850px;
            background-color: var(--bg-primary);
            border: 1px solid var(--border-color);
            border-radius: 6px;
            padding: 40px;
            box-shadow: 0 8px 24px rgba(0,0,0,0.5);
            animation: fadeIn 1s ease-out;
        }

        /* Banner & Header */
        .banner {
            width: 100%;
            height: 180px;
            border-radius: 6px;
            background: linear-gradient(135deg, #1f1f3a 0%, #0d1117 100%);
            border: 1px solid var(--border-color);
            display: flex;
            align-items: center;
            justify-content: center;
            position: relative;
            overflow: hidden;
            margin-bottom: 30px;
        }

        .banner::before {
            content: '';
            position: absolute;
            width: 200%;
            height: 200%;
            background: linear-gradient(45deg, transparent, rgba(138, 43, 226, 0.1), transparent);
            transform: rotate(45deg);
            animation: streaming 6s linear infinite;
        }

        .banner-text {
            font-size: 2.2rem;
            font-weight: 700;
            letter-spacing: 2px;
            background: linear-gradient(45deg, #58a6ff, #8a2be2, #ff79c6);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            z-index: 1;
            text-align: center;
        }

        /* Section Headings with Purple Marker */
        .section-title {
            font-size: 1.3rem;
            font-weight: 600;
            margin-top: 35px;
            margin-bottom: 15px;
            display: flex;
            align-items: center;
            border-bottom: 1px solid var(--border-color);
            padding-bottom: 8px;
        }

        .section-title::before {
            content: "█";
            color: var(--accent-purple);
            margin-right: 10px;
            font-size: 1.1rem;
            text-shadow: 0 0 8px var(--accent-purple);
        }

        /* Content Blocks */
        p {
            color: var(--text-primary);
            font-size: 0.95rem;
            margin-bottom: 12px;
        }

        .highlight {
            color: var(--accent-blue);
            font-weight: 500;
        }

        /* Badge Grids */
        .badge-grid {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            margin-top: 15px;
        }

        .badge {
            background-color: var(--bg-secondary);
            border: 1px solid var(--border-color);
            border-radius: 20px;
            padding: 6px 14px;
            font-size: 0.85rem;
            font-weight: 500;
            display: flex;
            align-items: center;
            gap: 6px;
            transition: all 0.3s ease;
            cursor: default;
        }

        .badge:hover {
            transform: translateY(-3px);
            border-color: var(--accent-purple);
            box-shadow: 0 4px 12px var(--shadow-glow);
            color: #ffffff;
        }

        /* Experience Timeline Layout */
        .timeline {
            margin-top: 15px;
            border-left: 2px solid var(--border-color);
            padding-left: 20px;
            position: relative;
        }

        .timeline-item {
            margin-bottom: 25px;
            position: relative;
            animation: slideUp 1s ease-out;
        }

        .timeline-item::before {
            content: '';
            position: absolute;
            left: -27px;
            top: 6px;
            width: 12px;
            height: 12px;
            border-radius: 50%;
            background-color: var(--bg-primary);
            border: 2px solid var(--accent-blue);
            transition: background-color 0.3s;
        }

        .timeline-item:hover::before {
            background-color: var(--accent-purple);
            border-color: var(--accent-purple);
        }

        .job-title {
            font-weight: 600;
            font-size: 1rem;
            color: #ffffff;
        }

        .company-date {
            font-size: 0.85rem;
            color: var(--text-secondary);
            margin-bottom: 6px;
        }

        .job-desc {
            font-size: 0.9rem;
            color: var(--text-primary);
            list-style-type: square;
            padding-left: 20px;
        }

        .job-desc li {
            margin-bottom: 4px;
        }

        /* Dashboard Metrics Block */
        .analytics-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
            gap: 20px;
            margin-top: 20px;
        }

        .card {
            background-color: var(--bg-secondary);
            border: 1px solid var(--border-color);
            border-radius: 6px;
            padding: 20px;
            text-align: center;
            transition: border-color 0.3s;
        }

        .card:hover {
            border-color: var(--border-color);
        }

        .card-val {
            font-size: 1.8rem;
            font-weight: 700;
            color: var(--accent-green);
            margin-bottom: 5px;
        }

        .card-lbl {
            font-size: 0.85rem;
            color: var(--text-secondary);
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        /* Animations */
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(10px); }
            to { opacity: 1; transform: translateY(0); }
        }

        @keyframes slideUp {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }

        @keyframes streaming {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }
    </style>
</head>
<body>

    <div class="readme-container">
        
        <!-- Animated Title Banner -->
        <div class="banner">
            <div class="banner-text">RUCHITA V BHOSALE</div>
        </div>

        <!-- About Me Section -->
        <div class="section-title">About Me</div>
        <p>I am an <span class="highlight">MCA Student</span> and web enthusiast passionate about turning modern development concepts into scalable digital products. I blend multi-disciplinary skills spanning Full Stack Development, Data Operations, and HR Management to build clean applications with optimized user experiences[cite: 1].</p>
        <p>Currently pursuing my Master's degree at <span class="highlight">MIT World Peace University, Pune</span>[cite: 1].</p>

        <!-- Tech Stack Badges -->
        <div class="section-title">Tech Stack & Programming</div>
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

        <!-- Tools & Design Frameworks -->
        <div class="section-title">Tools & Frameworks</div>
        <div class="badge-grid">
            <div class="badge">🐙 Git & GitHub</div>
            <div class="badge">💻 VS Code</div>
            <div class="badge">🤖 Android Studio</div>
            <div class="badge">📐 Figma</div>
            <div class="badge">💎 Adobe XD</div>
            <div class="badge">📊 MS Excel</div>
        </div>

        <!-- Professional Experience Timeline -->
        <div class="section-title">Experience</div>
        <div class="timeline">
            <div class="timeline-item">
                <div class="job-title">Full Stack Developer Intern</div>
                <div class="company-date">Skillected | June 2025 - Dec 2025</div>
                <ul class="job-desc">
                    <li>Developed responsive web applications utilizing React.js, Node.js, and MongoDB[cite: 1].</li>
                    <li>Integrated external RESTful APIs and managed structural database schemas[cite: 1].</li>
                </ul>
            </div>
            <div class="timeline-item">
                <div class="job-title">Associate Executive Intern (Data Analysis)</div>
                <div class="company-date">MDIndia Healthcare Services | Jan 2026 - Mar 2026</div>
                <ul class="job-desc">
                    <li>Analyzed complex healthcare datasets using functional Microsoft Excel engines[cite: 1].</li>
                    <li>Executed data validations, cross-verifications, and automated administrative reporting tasks[cite: 1].</li>
                </ul>
            </div>
        </div>

        <!-- Productivity & Performance Analytics Grid -->
        <div class="section-title">Performance Metrics</div>
        <div class="analytics-container">
            <div class="card">
                <div class="card-val">40+ WPM</div>
                <div class="card-lbl">Typing Speed</div>
            </div>
            <div class="card">
                <div class="card-val">6+ Tools</div>
                <div class="card-lbl">Design & UI Engines</div>
            </div>
            <div class="card">
                <div class="card-val">5 Languages</div>
                <div class="card-lbl">Linguistic Skills</div>
            </div>
        </div>

    </div>

</body>
</html>
