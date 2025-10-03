<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>「Made in heaven」——神秘人千叶 - 第五人格辅助工具</title>
    <style>
        /* 基础重置 */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: "Microsoft YaHei", "Segoe UI", sans-serif;
            background: #0a0a16;
            color: #e0e0e0;
            line-height: 1.5;
            min-height: 100vh;
        }
        
        .container {
            max-width: 900px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        /* 头部样式 */
        header {
            background: rgba(15, 15, 25, 0.95);
            padding: 12px 0;
            box-shadow: 0 3px 15px rgba(0, 0, 0, 0.4);
            position: sticky;
            top: 0;
            z-index: 100;
            border-bottom: 1px solid rgba(255, 255, 255, 0.08);
        }
        
        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .logo-icon {
            color: #ff4757;
            font-size: 20px;
            width: 20px;
            height: 20px;
            display: flex;
            align-items: center;
            justify-content: center;
        }
        
        .logo h1 {
            font-size: 18px;
            font-weight: 600;
            color: #ff4757;
        }
        
        nav ul {
            display: flex;
            list-style: none;
            gap: 20px;
        }
        
        nav ul li a {
            color: #b0b0b0;
            text-decoration: none;
            font-weight: 500;
            transition: all 0.3s;
            padding: 6px 10px;
            border-radius: 5px;
            font-size: 14px;
        }
        
        nav ul li a:hover, nav ul li a.active {
            color: #ff6b81;
            background: rgba(255, 107, 129, 0.1);
        }
        
        /* 英雄区域样式 */
        .hero {
            padding: 70px 0 40px;
            text-align: center;
            background: linear-gradient(135deg, #0a0a16 0%, #1a1a2e 50%, #0f0f1f 100%);
        }
        
        .hero-content {
            max-width: 700px;
            margin: 0 auto;
        }
        
        .hero h2 {
            font-size: 32px;
            margin-bottom: 15px;
            color: #ffffff;
            font-weight: 700;
        }
        
        .hero p {
            font-size: 16px;
            margin: 0 auto 20px;
            color: #b0b0b0;
            max-width: 600px;
        }
        
        .tagline {
            display: inline-block;
            background: rgba(255, 71, 87, 0.15);
            color: #ff6b81;
            padding: 6px 16px;
            border-radius: 20px;
            font-size: 14px;
            margin-bottom: 20px;
            border: 1px solid rgba(255, 107, 129, 0.3);
        }
        
        .warning {
            background: rgba(211, 47, 47, 0.15);
            border: 1px solid rgba(211, 47, 47, 0.3);
            padding: 15px;
            margin: 20px auto;
            border-radius: 8px;
            max-width: 600px;
            text-align: left;
        }
        
        .warning h3 {
            color: #ff6b6b;
            margin-bottom: 8px;
            font-size: 16px;
            display: flex;
            align-items: center;
            gap: 8px;
        }
        
        .warning-icon {
            font-size: 18px;
        }
        
        .warning p {
            color: #cccccc;
            font-size: 14px;
            margin: 0;
        }
        
        /* 下载区域样式 */
        .download-section {
            padding: 40px 0 60px;
            text-align: center;
            background: linear-gradient(135deg, #0a0a16 0%, #1a1a2e 50%, #0f0f1f 100%);
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 30px;
            font-size: 26px;
            color: #ffffff;
            font-weight: 600;
        }
        
        .download-card {
            background: rgba(30, 30, 46, 0.8);
            border-radius: 12px;
            padding: 35px 30px;
            max-width: 600px;
            margin: 0 auto;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.4);
            border: 1px solid rgba(255, 255, 255, 0.08);
            position: relative;
        }
        
        .download-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 4px;
            background: linear-gradient(90deg, #ff4757, #ff6b81);
        }
        
        .download-icon {
            font-size: 36px;
            color: #ff6b81;
            margin-bottom: 15px;
        }
        
        .download-card h3 {
            color: #ffffff;
            margin-bottom: 12px;
            font-size: 22px;
        }
        
        .download-card p {
            color: #b0b0b0;
            margin-bottom: 25px;
            font-size: 15px;
            max-width: 450px;
            margin-left: auto;
            margin-right: auto;
        }
        
        .download-button {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            gap: 8px;
            background: linear-gradient(135deg, #ff4757 0%, #ff6b81 100%);
            color: white;
            padding: 14px 35px;
            font-size: 16px;
            font-weight: 600;
            text-decoration: none;
            border-radius: 40px;
            transition: all 0.3s;
            box-shadow: 0 6px 20px rgba(255, 71, 87, 0.4);
            margin: 10px;
        }
        
        .download-button:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 25px rgba(255, 71, 87, 0.5);
        }
        
        .download-info {
            margin-top: 25px;
            color: #888888;
            font-size: 13px;
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 15px;
        }
        
        .info-item {
            display: flex;
            align-items: center;
            gap: 6px;
        }
        
        /* 功能展示样式 */
        .features {
            padding: 60px 0;
            background: rgba(15, 15, 25, 0.4);
        }
        
        .feature-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            margin-top: 30px;
        }
        
        .feature-card {
            background: rgba(30, 30, 46, 0.6);
            border-radius: 10px;
            padding: 25px 20px;
            transition: all 0.3s;
            border: 1px solid rgba(255, 255, 255, 0.05);
            text-align: center;
        }
        
        .feature-card:hover {
            transform: translateY(-8px);
            background: rgba(35, 35, 55, 0.8);
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.3);
        }
        
        .feature-icon {
            font-size: 32px;
            color: #ff6b81;
            margin-bottom: 15px;
            height: 32px;
            display: flex;
            align-items: center;
            justify-content: center;
        }
        
        .feature-card h3 {
            font-size: 18px;
            margin-bottom: 12px;
            color: #ffffff;
        }
        
        .feature-card p {
            color: #b0b0b0;
            font-size: 14px;
        }
        
        /* 页脚样式 */
        footer {
            background: rgba(10, 10, 20, 0.95);
            padding: 40px 0 25px;
            border-top: 1px solid rgba(255, 255, 255, 0.05);
        }
        
        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 30px;
            margin-bottom: 30px;
        }
        
        .footer-section h3 {
            font-size: 16px;
            margin-bottom: 15px;
            color: #ff6b81;
        }
        
        .footer-section p, .footer-section a {
            color: #888888;
            text-decoration: none;
            margin-bottom: 8px;
            display: block;
            font-size: 13px;
            transition: color 0.3s;
        }
        
        .footer-section a:hover {
            color: #ff6b81;
        }
        
        .social-links {
            display: flex;
            gap: 12px;
            margin-top: 15px;
        }
        
        .social-links a {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 35px;
            height: 35px;
            background: rgba(255, 255, 255, 0.05);
            border-radius: 50%;
            transition: all 0.3s;
        }
        
        .social-links a:hover {
            background: rgba(255, 107, 129, 0.2);
            transform: translateY(-2px);
        }
        
        .copyright {
            padding-top: 25px;
            border-top: 1px solid rgba(255, 255, 255, 0.05);
            color: #666666;
            font-size: 12px;
            text-align: center;
        }
        
        /* 响应式设计 */
        @media (max-width: 768px) {
            .header-content {
                flex-direction: column;
                gap: 12px;
            }
            
            nav ul {
                gap: 12px;
            }
            
            .hero h2 {
                font-size: 28px;
            }
            
            .section-title {
                font-size: 22px;
            }
            
            .download-card {
                padding: 30px 20px;
            }
            
            .feature-grid {
                grid-template-columns: 1fr;
            }
            
            .footer-content {
                grid-template-columns: 1fr;
                gap: 25px;
            }
        }
        
        @media (max-width: 480px) {
            .hero h2 {
                font-size: 24px;
            }
            
            .download-button {
                padding: 12px 25px;
                font-size: 14px;
            }
            
            .download-info {
                flex-direction: column;
                gap: 8px;
            }
        }
    </style>
</head>
<body>
    <!-- 头部 -->
    <header>
        <div class="container">
            <div class="header-content">
                <div class="logo">
                    <div class="logo-icon">♛</div>
                    <h1>「Made in heaven」——神秘人千叶</h1>
                </div>
                <nav>
                    <ul>
                        <li><a href="#features" class="active">功能特性</a></li>
                        <li><a href="#download">下载</a></li>
                        <li><a href="#about">关于</a></li>
                    </ul>
                </nav>
            </div>
        </div>
    </header>

    <!-- 英雄区域 -->
    <section class="hero">
        <div class="container">
            <div class="hero-content">
                <div class="tagline">第五人格辅助工具</div>
                <h2>体验不一样的庄园游戏</h2>
                <p>一个由AI集体智慧缝缝补补而成的实验性项目，仅供学习交流</p>
                
                <div class="warning">
                    <h3><span class="warning-icon">⚠️</span> 重要提醒</h3>
                    <p>本项目源码是到处扒拉开源代码，让多个AI一块儿瞎改，缝缝补补攒出来的代码，纯属学习交流用途。倒卖本辅助死全家。</p>
                </div>
            </div>
        </div>
    </section>

    <!-- 下载区域 -->
    <section id="download" class="download-section">
        <div class="container">
            <h2 class="section-title">获取工具</h2>
            <div class="download-card">
                <div class="download-icon">⬇️</div>
                <h3>下载千叶辅助工具</h3>
                <p>请确保您已阅读并理解免责声明后再下载使用，本工具仅供学习交流，请勿用于商业用途。</p>
                <a href="https://pan.baidu.com/s/1qianye_project_2025" class="download-button">
                    <span>⬇️</span>
                    下载工具 (百度网盘)
                </a>
                <div class="download-info">
                    <div class="info-item">
                        <span>版本: 2.5</span>
                    </div>
                    <div class="info-item">
                        <span>大小: 约3.2MB</span>
                    </div>
                    <div class="info-item">
                        <span>更新: 2025年3月</span>
                    </div>
                    <div class="info-item">
                        <span>支持: Android 8.0+</span>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- 功能展示 -->
    <section id="features" class="features">
        <div class="container">
            <h2 class="section-title">功能特性</h2>
            <div class="feature-grid">
                <div class="feature-card">
                    <div class="feature-icon">👥</div>
                    <h3>角色透视</h3>
                    <p>显示监管者和求生者的位置、距离和状态信息，支持四角边框和方框显示。</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">🧰</div>
                    <h3>道具识别</h3>
                    <p>自动识别地图中的密码机、椅子、板子、箱子等地形元素，并显示距离。</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">📏</div>
                    <h3>距离计算</h3>
                    <p>精确计算与各种游戏对象的距离，帮助您更好地判断局势。</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">👑</div>
                    <h3>红夫人镜像</h3>
                    <p>特殊支持红夫人镜像模式，可显示镜像中的求生者位置。</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">👻</div>
                    <h3>监管者预知</h3>
                    <p>提前显示监管者类型，帮助制定应对策略。</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">⚙️</div>
                    <h3>自定义界面</h3>
                    <p>可自定义显示内容，支持拖拽悬浮按钮，灵活调整界面布局。</p>
                </div>
            </div>
        </div>
    </section>

    <!-- 页脚 -->
    <footer id="about">
        <div class="container">
            <div class="footer-content">
                <div class="footer-section">
                    <h3>关于我们</h3>
                    <p>一群热爱技术的开发者，通过AI协作开发的实验性项目。</p>
                    <p>作者: 神秘人千叶</p>
                    <p>源码来源于开源社区，尊重开源精神</p>
                </div>
                <div class="footer-section">
                    <h3>重要提醒</h3>
                    <p>本工具仅供学习交流，请勿用于商业用途。</p>
                    <p>使用本工具可能违反游戏规则，请谨慎使用。</p>
                    <p>24小时后请自觉删除。</p>
                </div>
                <div class="footer-section">
                    <h3>联系我们</h3>
                    <p>QQ群: 123456789</p>
                    <p>Telegram: @qianye_project</p>
                    <p>邮箱: contact@qianye.project</p>
                    <div class="social-links">
                        <a href="#">QQ</a>
                        <a href="#">TG</a>
                        <a href="#">GH</a>
                    </div>
                </div>
            </div>
            <div class="copyright">
                <p>© 2025 千叶项目组. 本网站内容纯属娱乐，如有雷同，纯属巧合。</p>
                <p>感谢所有参与本项目的AI助手：ChatGPT、DeepSeek、Kimi、豆包、Qwen、Qoder</p>
            </div>
        </div>
    </footer>

    <script>
        // 简单的滚动效果
        document.querySelectorAll('nav a').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                e.preventDefault();
                const targetId = this.getAttribute('href');
                const targetElement = document.querySelector(targetId);
                
                window.scrollTo({
                    top: targetElement.offsetTop - 70,
                    behavior: 'smooth'
                });
            });
        });
        
        // 导航激活状态
        window.addEventListener('scroll', function() {
            const sections = document.querySelectorAll('section');
            const navLinks = document.querySelectorAll('nav a');
            
            let current = '';
            sections.forEach(section => {
                const sectionTop = section.offsetTop;
                const sectionHeight = section.clientHeight;
                if (pageYOffset >= sectionTop - 80) {
                    current = section.getAttribute('id');
                }
            });
            
            navLinks.forEach(link => {
                link.classList.remove('active');
                if (link.getAttribute('href') === '#' + current) {
                    link.classList.add('active');
                }
            });
        });
    </script>
</body>
</html>
