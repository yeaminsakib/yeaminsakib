<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Yeamin Sakib · modern profile</title>
    <!-- Font Awesome 6 (free) -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <!-- Google Fonts: Inter & Space Grotesk -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:opsz,wght@14..32,300..700&family=Space+Grotesk:wght@400;500;600&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            background: linear-gradient(145deg, #f6f9fc 0%, #edf2f9 100%);
            font-family: "Inter", system-ui, -apple-system, sans-serif;
            display: flex;
            justify-content: center;
            padding: 2.5rem 1.5rem;
            color: #1e293b;
            line-height: 1.5;
        }

        .profile-card {
            max-width: 1280px;
            width: 100%;
            background: rgba(255,255,255,0.75);
            backdrop-filter: blur(8px);
            -webkit-backdrop-filter: blur(8px);
            border-radius: 3rem;
            box-shadow: 0 25px 50px -12px rgba(0,0,0,0.15), 0 0 0 1px rgba(148,163,184,0.1);
            padding: 2.5rem;
        }

        /* layout grid */
        .grid-main {
            display: grid;
            grid-template-columns: 1fr 2.2fr;
            gap: 2rem;
            margin-top: 0.5rem;
        }

        /* left panel — intro & contact */
        .intro-panel {
            background: white;
            border-radius: 2rem;
            padding: 2rem 1.8rem;
            box-shadow: 0 8px 20px -6px rgba(0,20,40,0.08);
            border: 1px solid rgba(203, 213, 225, 0.3);
            transition: 0.2s;
        }

        .avatar-title {
            display: flex;
            align-items: center;
            gap: 1.2rem;
            margin-bottom: 1.8rem;
            flex-wrap: wrap;
        }

        .avatar-icon {
            background: #0f172a;
            color: white;
            width: 70px;
            height: 70px;
            border-radius: 30% 70% 70% 30% / 30% 30% 70% 70%; /* organic modern shape */
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 2rem;
            font-weight: 600;
            box-shadow: 0 15px 25px -8px #0f172a40;
        }

        .name h1 {
            font-size: 2rem;
            font-weight: 700;
            letter-spacing: -0.02em;
            line-height: 1.2;
        }

        .name h1 span {
            font-weight: 500;
            color: #475569;
            font-size: 1.2rem;
            display: block;
            margin-top: 0.2rem;
        }

        .badge-row {
            display: flex;
            flex-wrap: wrap;
            gap: 0.8rem;
            margin: 1.5rem 0 1.2rem;
        }

        .chip {
            background: #eef2ff;
            color: #1e3a8a;
            padding: 0.5rem 1.2rem;
            border-radius: 40px;
            font-size: 0.9rem;
            font-weight: 500;
            display: inline-flex;
            align-items: center;
            gap: 8px;
            border: 1px solid #a5b4fc60;
            backdrop-filter: blur(2px);
        }

        .chip i {
            font-size: 0.9rem;
            color: #2563eb;
        }

        .stat-box {
            background: #f8fafc;
            border-radius: 1.5rem;
            padding: 1.2rem 1.5rem;
            display: flex;
            justify-content: space-between;
            margin: 1.8rem 0 1.5rem;
            border: 1px solid #e2e8f0;
        }

        .stat-item {
            text-align: center;
        }

        .stat-number {
            font-weight: 700;
            font-size: 1.4rem;
            color: #0f172a;
        }

        .stat-label {
            font-size: 0.8rem;
            text-transform: uppercase;
            letter-spacing: 0.03em;
            color: #64748b;
        }

        .contact-list {
            display: flex;
            flex-direction: column;
            gap: 0.8rem;
            margin-top: 1.2rem;
        }

        .contact-item {
            display: flex;
            align-items: center;
            gap: 0.8rem;
            font-size: 0.95rem;
            color: #1e293b;
            text-decoration: none;
            transition: 0.15s;
            padding: 0.6rem 1rem;
            border-radius: 50px;
            background: #f1f5f9;
        }

        .contact-item i {
            width: 24px;
            color: #2563eb;
            font-size: 1.2rem;
        }

        .contact-item:hover {
            background: #e6edf8;
            transform: translateX(4px);
        }

        .social-links {
            display: flex;
            flex-wrap: wrap;
            gap: 0.8rem;
            margin: 1.8rem 0 1rem;
        }

        .social-icon {
            background: white;
            border-radius: 40px;
            padding: 0.6rem 1rem;
            border: 1px solid #cbd5e1;
            color: #1e293b;
            font-size: 0.9rem;
            display: inline-flex;
            align-items: center;
            gap: 0.5rem;
            transition: 0.15s;
            text-decoration: none;
        }

        .social-icon i {
            font-size: 1.1rem;
            color: #2563eb;
        }

        .social-icon:hover {
            background: #2563eb;
            border-color: #2563eb;
            color: white;
        }
        .social-icon:hover i {
            color: white;
        }

        /* right panel — main content */
        .main-panel {
            display: flex;
            flex-direction: column;
            gap: 2rem;
        }

        .section {
            background: white;
            border-radius: 2rem;
            padding: 1.8rem 2rem;
            border: 1px solid #e9eef3;
            box-shadow: 0 4px 10px -8px #b0c4de;
        }

        .section-title {
            font-size: 1.3rem;
            font-weight: 600;
            letter-spacing: -0.01em;
            margin-bottom: 1.5rem;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .section-title i {
            background: #dbeafe;
            color: #1d4ed8;
            padding: 8px;
            border-radius: 14px;
            font-size: 1rem;
        }

        .project-block {
            background: #f9fbfe;
            border-radius: 1.5rem;
            padding: 1.5rem;
            border-left: 6px solid #2563eb;
            margin-bottom: 1.2rem;
        }

        .project-title {
            font-weight: 700;
            font-size: 1.25rem;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .project-desc {
            color: #334155;
            margin: 0.7rem 0 1rem;
        }

        .btn-outline {
            background: transparent;
            border: 1.5px solid #2563eb;
            color: #2563eb;
            padding: 0.5rem 1.5rem;
            border-radius: 40px;
            font-weight: 500;
            text-decoration: none;
            display: inline-flex;
            align-items: center;
            gap: 6px;
            transition: 0.2s;
        }

        .btn-outline:hover {
            background: #2563eb;
            color: white;
        }

        /* tool tags */
        .tools-cloud {
            display: flex;
            flex-wrap: wrap;
            gap: 0.6rem 0.8rem;
            margin-top: 1rem;
        }

        .tool-tag {
            background: #ecfdf5;
            color: #065f46;
            padding: 0.45rem 1.2rem;
            border-radius: 40px;
            font-size: 0.85rem;
            font-weight: 500;
            border: 1px solid #a7f3d0;
            transition: 0.1s;
        }

        .tool-tag i {
            margin-right: 4px;
            font-size: 0.8rem;
            color: #059669;
        }

        /* stats cards */
        .stats-row {
            display: flex;
            flex-wrap: wrap;
            gap: 1.2rem;
            margin-top: 1rem;
        }

        .stat-card {
            background: #f1f5f9;
            flex: 1 1 180px;
            border-radius: 1.5rem;
            padding: 1.2rem;
            display: flex;
            align-items: center;
            gap: 1rem;
            border: 1px solid #d9e2ef;
        }

        .stat-card i {
            font-size: 2rem;
            color: #2563eb;
        }

        .stat-card div p:first-child {
            font-size: 0.8rem;
            color: #475569;
        }

        .stat-card div p:last-child {
            font-weight: 700;
            font-size: 1.5rem;
            line-height: 1.3;
        }

        .trophy-row {
            display: flex;
            flex-wrap: wrap;
            gap: 0.5rem 1rem;
            margin: 1rem 0 0.2rem;
            background: #fffbeb;
            padding: 0.8rem 1.2rem;
            border-radius: 60px;
            align-items: center;
        }

        .trophy-row i {
            color: #d97706;
        }

        /* responsiveness */
        @media (max-width: 900px) {
            .grid-main {
                grid-template-columns: 1fr;
            }
            .profile-card { padding: 1.5rem; }
        }
        @media (max-width: 500px) {
            .avatar-title { flex-direction: column; align-items: start; }
        }

        hr {
            border: none;
            border-top: 2px dashed #cbd5e1;
            margin: 1rem 0;
        }

        /* tweaks */
        .link-muted {
            color: #2563eb;
            text-decoration: none;
            font-weight: 500;
        }
        .footer-note {
            font-size: 0.85rem;
            color: #626e7e;
            margin-top: 2rem;
            text-align: center;
            border-top: 1px dashed #cbd5e1;
            padding-top: 1.5rem;
        }
    </style>
</head>
<body>
    <div class="profile-card">
        <!-- header trophy / twitter badge (clean version) -->
        <div style="display: flex; justify-content: space-between; align-items: center; flex-wrap: wrap; margin-bottom: 1rem;">
            <div class="trophy-row">
                <i class="fas fa-trophy" style="font-size: 1.2rem;"></i>
                <span style="font-weight: 500;">github-profile-trophy · 9 achievements </span>
                <span style="color: #b45309;">🏆</span>
            </div>
            <a href="https://twitter.com/yeaminsakib" target="_blank" style="background:#0f172a; color:white; padding:0.4rem 1.2rem; border-radius:40px; text-decoration:none; font-weight:500; display:inline-flex; align-items:center; gap:0.4rem;">
                <i class="fab fa-twitter" style="font-size:1rem;"></i> @yeaminsakib
                <span style="background:#2563eb; padding:0.2rem 0.7rem; border-radius:60px; margin-left:0.3rem; font-size:0.75rem;">1.2K</span>
            </a>
        </div>

        <!-- main grid -->
        <div class="grid-main">
            <!-- LEFT PANEL: intro + contact + stats compact -->
            <div class="intro-panel">
                <div class="avatar-title">
                    <div class="avatar-icon">YS</div>
                    <div class="name">
                        <h1>Md. Yeamin Islam Sakib <span>@yeaminsakib</span></h1>
                    </div>
                </div>

                <div class="badge-row">
                    <span class="chip"><i class="fas fa-code"></i> web developer</span>
                    <span class="chip"><i class="fas fa-shield-halved"></i> Jr. security analyst</span>
                    <span class="chip"><i class="fas fa-bug"></i> bug hunter</span>
                </div>

                <div class="stat-box">
                    <div class="stat-item">
                        <div class="stat-number">17+</div>
                        <div class="stat-label">projects</div>
                    </div>
                    <div class="stat-item">
                        <div class="stat-number">2.1k</div>
                        <div class="stat-label">🌟 stars</div>
                    </div>
                    <div class="stat-item">
                        <div class="stat-number">32</div>
                        <div class="stat-label">followers</div>
                    </div>
                </div>

                <!-- contact & reach -->
                <div class="contact-list">
                    <a href="mailto:yeaminsakib@gmail.com" class="contact-item"><i class="fas fa-envelope"></i> yeaminsakib@gmail.com</a>
                    <a href="https://yeaminsakib.com" target="_blank" class="contact-item"><i class="fas fa-globe"></i> yeaminsakib.com</a>
                    <a href="#" class="contact-item"><i class="fas fa-map-pin"></i> Dhaka, Bangladesh</a>
                </div>

                <!-- social cluster (modern row) -->
                <div class="social-links">
                    <a href="https://linkedin.com/in/yeaminsakib" class="social-icon"><i class="fab fa-linkedin-in"></i> <span>in</span></a>
                    <a href="https://twitter.com/yeaminsakib" class="social-icon"><i class="fab fa-x-twitter"></i> X</a>
                    <a href="https://github.com/yeaminsakib" class="social-icon"><i class="fab fa-github"></i> gh</a>
                    <a href="https://fb.com/yeamin5akib" class="social-icon"><i class="fab fa-facebook-f"></i> fb</a>
                    <a href="https://stackoverflow.com/users/yeaminsakib" class="social-icon"><i class="fab fa-stack-overflow"></i> SO</a>
                    <a href="https://medium.com/@yeaminsakib" class="social-icon"><i class="fab fa-medium"></i> med</a>
                    <a href="https://hackerrank.com/yeaminsakib" class="social-icon"><i class="fab fa-hackerrank"></i> HR</a>
                    <a href="https://behance.net/yeaminsakib" class="social-icon"><i class="fab fa-behance"></i> be</a>
                    <a href="https://kaggle.com/sakib27631" class="social-icon"><i class="fab fa-kaggle"></i> kg</a>
                </div>

                <hr>
                <div style="font-size:0.9rem; color:#2c3e50;"><i class="fas fa-exclamation-circle" style="color:#2563eb;"></i> “secure code · clean design”</div>
            </div>

            <!-- RIGHT PANEL (main) -->
            <div class="main-panel">
                <!-- featured project -->
                <div class="section">
                    <div class="section-title"><i class="fas fa-microchip"></i> 🔭 current project</div>
                    <div class="project-block">
                        <div class="project-title">
                            <i class="fas fa-brain"></i> Student stress & mobile addiction
                        </div>
                        <div class="project-desc">
                            ML-based analysis using Python, pandas, scikit-learn. Predicts stress patterns from mobile usage. <span style="background:#e9f0ff; padding:0.1rem 0.6rem; border-radius:60px;">#research</span>
                        </div>
                        <a href="https://github.com/yeaminsakib/project/tree/main/Stress_Test" class="btn-outline"><i class="fab fa-github"></i> repository</a>
                    </div>

                    <!-- current learning & status -->
                    <div style="display: flex; flex-wrap: wrap; gap: 1rem; margin-top: 1rem;">
                        <span style="background:#dbeafe; border-radius:60px; padding:0.5rem 1.3rem;"><i class="fas fa-seedling" style="color:#2563eb;"></i> learning <strong>Bug Hunting</strong></span>
                        <span style="background:#f1f5f9; border-radius:60px; padding:0.5rem 1.3rem;"><i class="fas fa-bug"></i> OWASP top10 · BurpSuite</span>
                    </div>
                </div>

                <!-- languages & tools (modern tags) -->
                <div class="section">
                    <div class="section-title"><i class="fas fa-laptop-code"></i> toolchain & languages</div>
                    <div class="tools-cloud">
                        <span class="tool-tag"><i class="fab fa-python"></i> Python</span>
                        <span class="tool-tag"><i class="fas fa-code"></i> C</span>
                        <span class="tool-tag"><i class="fab fa-golang"></i> Go</span>
                        <span class="tool-tag"><i class="fab fa-js"></i> JavaScript</span>
                        <span class="tool-tag"><i class="fab fa-html5"></i> HTML5</span>
                        <span class="tool-tag"><i class="fab fa-css3-alt"></i> CSS3</span>
                        <span class="tool-tag"><i class="fab fa-bootstrap"></i> Bootstrap</span>
                        <span class="tool-tag"><i class="fas fa-database"></i> MySQL</span>
                        <span class="tool-tag"><i class="fas fa-database"></i> MSSQL</span>
                        <span class="tool-tag"><i class="fab fa-django"></i> Django</span>
                        <span class="tool-tag"><i class="fas fa-chart-line"></i> pandas</span>
                        <span class="tool-tag"><i class="fas fa-chart-bar"></i> seaborn</span>
                        <span class="tool-tag"><i class="fas fa-eye"></i> scikit-learn</span>
                        <span class="tool-tag"><i class="fas fa-fire"></i> PyTorch</span>
                        <span class="tool-tag"><i class="fas fa-tensorflow"></i> TensorFlow</span>
                        <span class="tool-tag"><i class="fas fa-microchip"></i> Arduino</span>
                        <span class="tool-tag"><i class="fas fa-terminal"></i> Bash</span>
                        <span class="tool-tag"><i class="fab fa-linux"></i> Linux</span>
                        <span class="tool-tag"><i class="fab fa-git-alt"></i> Git</span>
                        <span class="tool-tag"><i class="fas fa-cubes"></i> MATLAB</span>
                        <span class="tool-tag"><i class="fas fa-paint-brush"></i> Figma</span>
                    </div>
                </div>

                <!-- GitHub stats row (modern) -->
                <div class="section">
                    <div class="section-title"><i class="fas fa-chart-simple"></i> GitHub pulse</div>
                    <div class="stats-row">
                        <div class="stat-card">
                            <i class="fas fa-code"></i>
                            <div>
                                <p>top language</p>
                                <p>Python · 52%</p>
                            </div>
                        </div>
                        <div class="stat-card">
                            <i class="fas fa-star"></i>
                            <div>
                                <p>repos contributed</p>
                                <p>24</p>
                            </div>
                        </div>
                        <div class="stat-card">
                            <i class="fas fa-ranking-star"></i>
                            <div>
                                <p>rank (trophy)</p>
                                <p>#1203</p>
                            </div>
                        </div>
                    </div>
                    <!-- embed original stats as inline compact -->
                    <div style="display: flex; flex-wrap: wrap; gap: 0.8rem; background: #f1f5f9; border-radius: 1.5rem; padding: 1.2rem; margin-top: 1.2rem;">
                        <img src="https://github-readme-stats.vercel.app/api/top-langs?username=yeaminsakib&show_icons=true&locale=en&layout=compact" alt="top langs" style="border-radius:12px; max-width:100%; height:auto;">
                        <img src="https://github-readme-stats.vercel.app/api?username=yeaminsakib&show_icons=true&locale=en" alt="github stats" style="border-radius:12px; max-width:100%; height:auto;">
                    </div>
                </div>

                <!-- quick extra: all projects link & medium -->
                <div style="display: flex; gap: 1rem; flex-wrap: wrap;">
                    <a href="https://yeaminsakib.com" style="background:#0f172a; color:white; padding:0.8rem 2rem; border-radius:60px; text-decoration:none; font-weight:600;"><i class="fas fa-folder-open"></i> all projects → yeaminsakib.com</a>
                    <a href="https://medium.com/@yeaminsakib" style="background:#1e1e1e; color:white; padding:0.8rem 2rem; border-radius:60px; text-decoration:none;"><i class="fab fa-medium"></i> articles on medium</a>
                </div>
            </div>
        </div>

        <!-- footer note with hackerrank / kaggle etc (keeps all links) -->
        <div class="footer-note">
            <i class="fas fa-shield"></i> junior security analyst · 
            <i class="fab fa-hackerrank"></i> hackerrank @yeaminsakib ·
            <i class="fab fa-kaggle"></i> kaggle/sakib27631 · 
            <i class="fab fa-behance"></i> behance/yeaminsakib 
            · <i class="fas fa-bolt"></i> always learning
        </div>
    </div>
</body>
</html>
