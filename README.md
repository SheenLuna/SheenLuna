<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>SheenLuna · GitHub Profile</title>
    <style>
        :root {
            --bg: #0a0c12;
            --surface: #10131c;
            --surface-hover: #151a26;
            --border: #242b3d;
            --text: #e8ecf5;
            --dim: #9aa3b8;
            --accent: #8b9dff;
            --accent-soft: rgba(139, 157, 255, 0.12);
            --mint: #7fe0c3;
            --rose: #f4a2c0;
            --gold: #e6c67c;
            --radius: 24px;
            --radius-sm: 16px;
            --shadow-glow: 0 0 40px rgba(139, 157, 255, 0.15);
            --shadow-card: 0 18px 35px -10px rgba(0, 0, 0, 0.7);
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            background: var(--bg);
            background-image: radial-gradient(circle at 18% 15%, #182036 0%, #0a0c12 55%);
            font-family: 'Inter', 'SF Pro Display', 'Segoe UI', 'PingFang SC', 'Microsoft YaHei', system-ui, sans-serif;
            color: var(--text);
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            padding: 1.5rem;
            line-height: 1.55;
            letter-spacing: 0.01em;
        }

        .profile {
            max-width: 1100px;
            width: 100%;
            background: rgba(15, 18, 26, 0.88);
            backdrop-filter: blur(24px);
            -webkit-backdrop-filter: blur(24px);
            border: 1px solid var(--border);
            border-radius: var(--radius);
            box-shadow: var(--shadow-glow), var(--shadow-card);
            padding: 2.8rem 2.5rem;
            transition: all 0.2s;
        }

        @media (max-width: 640px) {
            body { padding: 0.8rem; }
            .profile { padding: 2rem 1.2rem; border-radius: 20px; }
        }

        /* 头部 */
        .header {
            display: flex;
            flex-wrap: wrap;
            align-items: baseline;
            justify-content: space-between;
            gap: 1rem;
            margin-bottom: 2.5rem;
            padding-bottom: 1.8rem;
            border-bottom: 1px solid rgba(255, 255, 255, 0.06);
        }

        .name-block {
            display: flex;
            flex-wrap: wrap;
            align-items: baseline;
            gap: 0.6rem 1.2rem;
        }

        .name {
            font-size: 3rem;
            font-weight: 700;
            letter-spacing: -0.02em;
            background: linear-gradient(135deg, #ffffff 0%, #c8d4ff 70%, #9aabff 100%);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            white-space: nowrap;
        }

        .aliases {
            display: flex;
            gap: 0.8rem;
            flex-wrap: wrap;
        }

        .aliases span {
            color: var(--dim);
            background: rgba(255, 255, 255, 0.04);
            padding: 0.25rem 1rem;
            border-radius: 30px;
            border: 1px solid rgba(255, 255, 255, 0.08);
            font-size: 0.95rem;
        }

        .badges {
            display: flex;
            gap: 0.7rem;
            flex-wrap: wrap;
        }

        .badge {
            background: var(--accent-soft);
            border: 1px solid rgba(139, 157, 255, 0.4);
            padding: 0.35rem 1.2rem;
            border-radius: 30px;
            font-size: 0.85rem;
            font-weight: 500;
            color: #ccd7ff;
            transition: 0.2s;
            letter-spacing: 0.01em;
        }

        .badge:hover {
            background: rgba(139, 157, 255, 0.2);
            border-color: #a8b7ff;
        }

        /* 关于我卡片网格 */
        .about-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 1.8rem;
            margin-bottom: 2.5rem;
        }

        .info-card {
            background: var(--surface);
            border: 1px solid var(--border);
            border-radius: var(--radius-sm);
            padding: 1.8rem 1.6rem;
            transition: all 0.25s ease;
            box-shadow: 0 8px 20px rgba(0, 0, 0, 0.25);
        }

        .info-card:hover {
            background: var(--surface-hover);
            border-color: #35405c;
            transform: translateY(-3px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.5), 0 0 20px rgba(139, 157, 255, 0.12);
        }

        .card-heading {
            display: flex;
            align-items: center;
            gap: 0.6rem;
            font-size: 1.3rem;
            font-weight: 600;
            color: #eaf0ff;
            margin-bottom: 1.4rem;
            letter-spacing: -0.01em;
        }

        .card-heading .icon {
            font-size: 1.6rem;
            filter: drop-shadow(0 0 6px rgba(139, 157, 255, 0.5));
        }

        .field-list {
            list-style: none;
            display: flex;
            flex-direction: column;
            gap: 1rem;
        }

        .field-item {
            font-size: 0.98rem;
            color: var(--dim);
            line-height: 1.5;
        }

        .field-label {
            display: block;
            color: #d3dcf5;
            font-weight: 600;
            margin-bottom: 0.2rem;
            font-size: 0.95rem;
            letter-spacing: 0.01em;
        }

        .field-content {
            color: #cbd3e8;
        }

        .field-content p {
            margin-bottom: 0.4rem;
        }

        .field-content p:last-child {
            margin-bottom: 0;
        }

        .highlight {
            color: var(--mint);
            font-weight: 500;
        }

        .accent-text {
            color: var(--accent);
            font-weight: 600;
        }

        .tag-container {
            display: flex;
            flex-wrap: wrap;
            gap: 0.5rem;
            margin-top: 0.6rem;
        }

        .tag {
            background: rgba(255, 255, 255, 0.04);
            border: 1px solid rgba(255, 255, 255, 0.1);
            padding: 0.25rem 0.9rem;
            border-radius: 22px;
            font-size: 0.85rem;
            color: #c4cee8;
            transition: 0.15s;
        }

        .tag:hover {
            background: rgba(139, 157, 255, 0.1);
            border-color: rgba(139, 157, 255, 0.4);
        }

        .separator {
            height: 1px;
            background: rgba(255, 255, 255, 0.06);
            margin: 1.2rem 0;
        }

        .contact-buttons {
            display: flex;
            flex-wrap: wrap;
            gap: 0.8rem;
            margin-top: 1.2rem;
        }

        .contact-btn {
            text-decoration: none;
            background: #1a2030;
            border: 1px solid rgba(139, 157, 255, 0.4);
            border-radius: 40px;
            padding: 0.55rem 1.4rem;
            color: #d5dfff;
            font-size: 0.9rem;
            transition: 0.2s;
            display: inline-flex;
            align-items: center;
            gap: 0.4rem;
            font-weight: 500;
        }

        .contact-btn:hover {
            background: #202840;
            border-color: #a2b4ff;
            box-shadow: 0 0 18px rgba(139, 157, 255, 0.25);
            color: #ffffff;
        }

        .repo-intro {
            background: rgba(139, 157, 255, 0.05);
            border: 1px solid rgba(139, 157, 255, 0.2);
            border-radius: 18px;
            padding: 1.5rem 1.8rem;
            margin-top: 0.5rem;
            color: #d0daf5;
            font-size: 1rem;
            line-height: 1.6;
            font-style: italic;
        }

        .footer {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 1.2rem;
            margin-top: 2.5rem;
            padding-top: 1.5rem;
            border-top: 1px solid rgba(255, 255, 255, 0.05);
            color: #717b94;
            font-size: 0.9rem;
        }

        .footer span {
            white-space: nowrap;
        }

        @media (max-width: 550px) {
            .name { font-size: 2.4rem; }
            .card-heading { font-size: 1.2rem; }
            .field-item { font-size: 0.93rem; }
        }
    </style>
</head>
<body>
    <div class="profile">
        <!-- 头部区域：姓名与别名 -->
        <div class="header">
            <div class="name-block">
                <h1 class="name">SheenLuna</h1>
                <div class="aliases">
                    <span>珝玥</span>
                    <span>希恩·露娜</span>
                </div>
            </div>
            <div class="badges">
                <span class="badge">🇨🇳 China</span>
                <span class="badge">17-year-old</span>
                <span class="badge">Freelancer</span>
            </div>
        </div>

        <!-- About Me 卡片网格（保留所有英文原文） -->
        <div class="about-grid">
            <!-- 基本信息卡（Name, Gender, Nationality, Speech, Actual Age, Future Direction 等） -->
            <div class="info-card">
                <div class="card-heading">
                    <span class="icon">🧬</span> About Me
                </div>
                <ul class="field-list">
                    <!-- Name -->
                    <li class="field-item">
                        <span class="field-label">Name</span>
                        <div class="field-content">
                            <p>希恩·露娜、珝玥、SheenLuna</p>
                        </div>
                    </li>
                    <!-- Gender -->
                    <li class="field-item">
                        <span class="field-label">Gender</span>
                        <div class="field-content">
                            <p>Cisgender Male</p>
                        </div>
                    </li>
                    <!-- Nationality -->
                    <li class="field-item">
                        <span class="field-label">Nationality</span>
                        <div class="field-content">
                            <p>🇨🇳 China</p>
                            <p>I was born in Guangdong Province, China, and currently live in the northern part of China.</p>
                        </div>
                    </li>
                    <!-- Speech -->
                    <li class="field-item">
                        <span class="field-label">Speech</span>
                        <div class="field-content">
                            <p>🇨🇳简体中文、🇭🇰繁體中文、🇬🇧English</p>
                            <p>Both Simplified Chinese and Traditional Chinese are my native languages, and English is the second language I am most proficient in. You can communicate with me fluently in any of the above languages.</p>
                        </div>
                    </li>
                    <!-- Actual Age -->
                    <li class="field-item">
                        <span class="field-label">Actual Age</span>
                        <div class="field-content">
                            <p>17-year-old</p>
                            <p>I have a diploma from a key high school in China. I am currently on a leave of absence and do not plan to attend university. In the future, I intend to study on my own and take self-taught higher education exams or pursue professional certifications.</p>
                        </div>
                    </li>
                    <!-- Future Direction -->
                    <li class="field-item">
                        <span class="field-label">Future Direction</span>
                        <div class="field-content">
                            <p>Freelancer</p>
                            <p>Make my own money.</p>
                        </div>
                    </li>
                </ul>
            </div>

            <!-- 学习与技能卡（Be Learning, Programming Languages） -->
            <div class="info-card">
                <div class="card-heading">
                    <span class="icon">📚</span> Be Learning & Skills
                </div>
                <ul class="field-list">
                    <!-- Be Learning -->
                    <li class="field-item">
                        <span class="field-label">Be Learning</span>
                        <div class="field-content">
                            <p>Math、C/C++、Data Structures and Algorithms、Philosophy、Art、Musicology、Commerce、Psychology</p>
                            <p>More skills never weigh you down.</p>
                        </div>
                        <div class="tag-container">
                            <span class="tag">Math</span>
                            <span class="tag">C/C++</span>
                            <span class="tag">Data Structures</span>
                            <span class="tag">Algorithms</span>
                            <span class="tag">Philosophy</span>
                            <span class="tag">Art</span>
                            <span class="tag">Musicology</span>
                            <span class="tag">Commerce</span>
                            <span class="tag">Psychology</span>
                        </div>
                    </li>
                    <!-- Programming Languages -->
                    <li class="field-item" style="margin-top: 1rem;">
                        <span class="field-label">Programming Languages</span>
                        <div class="field-content">
                            <p>HTML/CSS、C、C++、Java、Lua、Shell</p>
                            <p>I can use these programming languages.</p>
                        </div>
                        <div class="tag-container">
                            <span class="tag">HTML/CSS</span>
                            <span class="tag">C</span>
                            <span class="tag">C++</span>
                            <span class="tag">Java</span>
                            <span class="tag">Lua</span>
                            <span class="tag">Shell</span>
                        </div>
                    </li>
                </ul>
            </div>

            <!-- 联系方式卡（Discord, QQ ID） -->
            <div class="info-card">
                <div class="card-heading">
                    <span class="icon">🌐</span> Contact & Repository
                </div>
                <ul class="field-list">
                    <!-- Discord -->
                    <li class="field-item">
                        <span class="field-label">Discord</span>
                        <div class="field-content">
                            <p>#sheenluna</p>
                            <p>I don't use Discord very often, but if you'd like me to join a server or add me as a friend, I can use Discord.</p>
                        </div>
                    </li>
                    <!-- QQ ID -->
                    <li class="field-item">
                        <span class="field-label">QQ ID</span>
                        <div class="field-content">
                            <p>SheenLuna</p>
                            <p>This is my personal Tencent QQ. You can search for my personal account by "QQ ID". QQ is also what I use most on a daily basis. If you'd like to contact me directly, or if you want to join my QQ group chat or QQ channel, you can find me there. However, QQ is primarily designed for users in China.</p>
                        </div>
                    </li>
                </ul>
                <div class="contact-buttons">
                    <a href="#" class="contact-btn">💬 QQ: SheenLuna</a>
                    <a href="#" class="contact-btn">🎧 Discord: #sheenluna</a>
                </div>
            </div>
        </div>

        <!-- Introduce 部分（仓库介绍） -->
        <div class="repo-intro">
            <strong style="font-style: normal; display: block; margin-bottom: 0.5rem; color: #bdcaff;">📁 Introduce</strong>
            This repository is used to store my personal articles and materials, functioning like a small personal blog that is currently in use.
        </div>

        <!-- 底部签名 -->
        <div class="footer">
            <span>✨ SheenLuna · 珝玥 · 希恩·露娜</span>
            <span>📍 China · Northern part</span>
            <span>📫 QQ: SheenLuna | Discord: #sheenluna</span>
            <span>📄 GitHub Profile · Premium Design</span>
        </div>
    </div>
</body>
</html>
