<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Kingsley CJ - GitHub Profile</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
            padding: 20px;
            color: #333;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            background: rgba(255, 255, 255, 0.95);
            border-radius: 20px;
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.1);
            padding: 40px;
            backdrop-filter: blur(10px);
        }

        .header {
            text-align: center;
            margin-bottom: 40px;
            padding: 30px 0;
            background: linear-gradient(135deg, #4facfe 0%, #00f2fe 100%);
            border-radius: 15px;
            color: white;
            position: relative;
            overflow: hidden;
        }

        .header::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: repeating-linear-gradient(
                45deg,
                transparent,
                transparent 10px,
                rgba(255, 255, 255, 0.1) 10px,
                rgba(255, 255, 255, 0.1) 20px
            );
            animation: shimmer 3s linear infinite;
        }

        @keyframes shimmer {
            0% { transform: translateX(-100%); }
            100% { transform: translateX(100%); }
        }

        .header h1 {
            font-size: 3em;
            margin-bottom: 10px;
            position: relative;
            z-index: 1;
        }

        .header .subtitle {
            font-size: 1.3em;
            font-weight: 300;
            position: relative;
            z-index: 1;
        }

        .intro {
            background: #f8f9fa;
            padding: 30px;
            border-radius: 15px;
            margin-bottom: 30px;
            border-left: 5px solid #4facfe;
        }

        .intro p {
            font-size: 1.1em;
            line-height: 1.6;
            color: #555;
        }

        .section {
            margin-bottom: 40px;
        }

        .section h2 {
            font-size: 2em;
            margin-bottom: 20px;
            color: #2c3e50;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .section h2::before {
            content: '';
            width: 4px;
            height: 30px;
            background: linear-gradient(45deg, #4facfe, #00f2fe);
            border-radius: 2px;
        }

        .current-work {
            display: flex;
            gap: 20px;
            flex-wrap: wrap;
        }

        .work-item {
            flex: 1;
            min-width: 300px;
            background: white;
            padding: 25px;
            border-radius: 12px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            border: 1px solid #e0e0e0;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }

        .work-item:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.15);
        }

        .work-item h3 {
            color: #4facfe;
            margin-bottom: 10px;
            font-size: 1.3em;
        }

        .tech-stack {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
        }

        .tech-category {
            background: white;
            padding: 20px;
            border-radius: 12px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            border: 1px solid #e0e0e0;
        }

        .tech-category h3 {
            color: #2c3e50;
            margin-bottom: 15px;
            font-size: 1.2em;
            display: flex;
            align-items: center;
            gap: 8px;
        }

        .tech-category h3::before {
            content: '🔧';
            font-size: 1em;
        }

        .tech-list {
            display: flex;
            flex-wrap: wrap;
            gap: 8px;
        }

        .tech-item {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 6px 12px;
            border-radius: 20px;
            font-size: 0.9em;
            font-weight: 500;
        }

        .connect-section {
            text-align: center;
            background: #f8f9fa;
            padding: 30px;
            border-radius: 15px;
            margin-bottom: 30px;
        }

        .connect-links {
            display: flex;
            justify-content: center;
            gap: 20px;
            flex-wrap: wrap;
            margin-top: 20px;
        }

        .connect-link {
            background: white;
            padding: 15px 25px;
            border-radius: 10px;
            text-decoration: none;
            color: #333;
            font-weight: 600;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            transition: all 0.3s ease;
            border: 2px solid transparent;
        }

        .connect-link:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.15);
            border-color: #4facfe;
        }

        .certifications {
            background: white;
            padding: 25px;
            border-radius: 12px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            border: 1px solid #e0e0e0;
        }

        .cert-item {
            display: inline-block;
            background: linear-gradient(135deg, #4facfe 0%, #00f2fe 100%);
            color: white;
            padding: 10px 20px;
            border-radius: 25px;
            text-decoration: none;
            font-weight: 600;
            margin: 5px;
            transition: all 0.3s ease;
        }

        .cert-item:hover {
            transform: scale(1.05);
            box-shadow: 0 5px 15px rgba(79, 172, 254, 0.4);
        }

        .stats-section {
            text-align: center;
            background: #2c3e50;
            padding: 40px;
            border-radius: 15px;
            color: white;
        }

        .stats-container {
            display: flex;
            justify-content: center;
            gap: 20px;
            flex-wrap: wrap;
            margin-top: 20px;
        }

        .stat-item {
            background: rgba(255, 255, 255, 0.1);
            padding: 20px;
            border-radius: 12px;
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.2);
        }

        .stat-item img {
            border-radius: 8px;
            max-width: 100%;
            height: auto;
        }

        @media (max-width: 768px) {
            .container {
                padding: 20px;
            }

            .header h1 {
                font-size: 2.5em;
            }

            .current-work {
                flex-direction: column;
            }

            .work-item {
                min-width: auto;
            }

            .connect-links {
                flex-direction: column;
                align-items: center;
            }

            .stats-container {
                flex-direction: column;
                align-items: center;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="header">
            <h1>Hi, I'm Kingsley CJ 👋</h1>
            <p class="subtitle">🚀 Backend & Blockchain Developer && Web3 Enthusiast</p>
        </div>

        <div class="intro">
            <p>I am a passionate backend developer with experience in <strong>JavaScript, Node.js, and Express.js</strong>, actively advancing my expertise in <strong>Blockchain Development</strong> with Solidity and Ethers.js. My focus is on building scalable backend systems and decentralized applications.</p>
        </div>

        <div class="section">
            <h2>🔹 What I'm Currently Working On</h2>
            <div class="current-work">
                <div class="work-item">
                    <h3>🔗 Blockchain Development</h3>
                    <p>Exploring smart contract development, blockchain security, and Web3 integrations.</p>
                </div>
                <div class="work-item">
                    <h3>⚙️ Backend Engineering</h3>
                    <p>Enhancing my skills in API development, database management, and system architecture.</p>
                </div>
            </div>
        </div>

        <div class="section">
            <h2>🛠️ Tech Stack</h2>
            <div class="tech-stack">
                <div class="tech-category">
                    <h3>Languages</h3>
                    <div class="tech-list">
                        <span class="tech-item">JavaScript</span>
                        <span class="tech-item">Solidity</span>
                    </div>
                </div>
                <div class="tech-category">
                    <h3>Backend</h3>
                    <div class="tech-list">
                        <span class="tech-item">Node.js</span>
                        <span class="tech-item">Express.js</span>
                    </div>
                </div>
                <div class="tech-category">
                    <h3>Blockchain</h3>
                    <div class="tech-list">
                        <span class="tech-item">Hardhat</span>
                        <span class="tech-item">Ethers.js</span>
                        <span class="tech-item">Solidity</span>
                    </div>
                </div>
                <div class="tech-category">
                    <h3>Databases</h3>
                    <div class="tech-list">
                        <span class="tech-item">MongoDB</span>
                        <span class="tech-item">PostgreSQL</span>
                    </div>
                </div>
                <div class="tech-category">
                    <h3>Tools & Others</h3>
                    <div class="tech-list">
                        <span class="tech-item">Git</span>
                        <span class="tech-item">Docker</span>
                        <span class="tech-item">REST APIs</span>
                    </div>
                </div>
            </div>
        </div>

        <div class="section">
            <h2>🌍 Let's Connect</h2>
            <div class="connect-section">
                <p>I'm always excited to connect with fellow developers and discuss new opportunities!</p>
                <div class="connect-links">
                    <a href="https://www.linkedin.com/in/kingsleycj" class="connect-link" target="_blank">
                        💼 LinkedIn
                    </a>
                    <a href="https://x.com/kingsleycj8_" class="connect-link" target="_blank">
                        🐦 Twitter
                    </a>
                    <a href="https://flowcv.me/kingsleycj" class="connect-link" target="_blank">
                        📄 Portfolio
                    </a>
                </div>
            </div>
        </div>

        <div class="section">
            <h2>🏆 Certifications</h2>
            <div class="certifications">
                <a href="https://drive.google.com/file/d/16sju084HvQPE0WV2NzFZYoM1HcaNTGI6/view?usp=sharing" class="cert-item" target="_blank">
                    📜 Backend Development
                </a>
            </div>
        </div>

        <div class="section">
            <h2>📊 My GitHub Stats</h2>
            <div class="stats-section">
                <p>Here's a snapshot of my GitHub activity and contributions:</p>
                <div class="stats-container">
                    <div class="stat-item">
                        <img src="https://github-readme-stats.vercel.app/api?username=kingsleycj&show_icons=true&count_private=true&theme=gotham&hide_border=false&bg_color=00000000" alt="GitHub Stats" />
                    </div>
                    <div class="stat-item">
                        <img src="https://github-readme-streak-stats.herokuapp.com/?user=kingsleycj&stroke=ffffff&background=1c1917&ring=0891b2&fire=0891b2&currStreakNum=ffffff&currStreakLabel=0891b2&sideNums=ffffff&sideLabels=ffffff&dates=ffffff&hide_border=true" alt="GitHub Streak" />
                    </div>
                </div>
            </div>
        </div>
    </div>
</body>
</html>