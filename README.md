......., [01.01.2026 17:38]
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>SAT with Edu Pro - Master Your SAT</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.6;
            color: #e0e0e0;
            background: #0a0a0a;
            overflow-x: hidden;
        }

        /* Animated Background with Glow */
        .animated-bg {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: -1;
            background: linear-gradient(135deg, #0a0a0a 0%, #1a1a2e 50%, #0a0a0a 100%);
        }

        .animated-bg::before {
            content: '';
            position: absolute;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle, rgba(102, 126, 234, 0.15) 1px, transparent 1px);
            background-size: 50px 50px;
            animation: moveBackground 20s linear infinite;
        }

        .animated-bg::after {
            content: '';
            position: absolute;
            top: 20%;
            left: 10%;
            width: 500px;
            height: 500px;
            background: radial-gradient(circle, rgba(102, 126, 234, 0.2) 0%, transparent 70%);
            border-radius: 50%;
            filter: blur(60px);
            animation: float 8s ease-in-out infinite;
        }

        @keyframes moveBackground {
            0% { transform: translate(0, 0); }
            100% { transform: translate(50px, 50px); }
        }

        @keyframes float {
            0%, 100% { transform: translate(0, 0); }
            50% { transform: translate(100px, 100px); }
        }

        /* Glow Effects */
        .glow {
            box-shadow: 0 0 20px rgba(102, 126, 234, 0.5),
                        0 0 40px rgba(102, 126, 234, 0.3),
                        0 0 60px rgba(102, 126, 234, 0.2);
        }

        .glow-text {
            text-shadow: 0 0 10px rgba(102, 126, 234, 0.8),
                         0 0 20px rgba(102, 126, 234, 0.6),
                         0 0 30px rgba(102, 126, 234, 0.4);
        }

        /* Navigation */
        nav {
            background: rgba(26, 26, 46, 0.95);
            backdrop-filter: blur(10px);
            padding: 1rem 2rem;
            box-shadow: 0 4px 30px rgba(102, 126, 234, 0.3);
            position: sticky;
            top: 0;
            z-index: 1000;
            border-bottom: 1px solid rgba(102, 126, 234, 0.3);
        }

        .nav-container {
            max-width: 1200px;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-size: 1.8rem;
            font-weight: bold;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            filter: drop-shadow(0 0 20px rgba(102, 126, 234, 0.6));
            animation: pulse 2s ease-in-out infinite;
        }

        @keyframes pulse {
            0%, 100% { filter: drop-shadow(0 0 20px rgba(102, 126, 234, 0.6)); }
            50% { filter: drop-shadow(0 0 30px rgba(102, 126, 234, 0.9)); }
        }

        .nav-links {
            display: flex;
            gap: 2rem;
            align-items: center;
        }

        .nav-links a {
            color: #e0e0e0;
            text-decoration: none;
            transition: all 0.3s;
            position: relative;
        }

        .nav-links a::after {
            content: '';

......., [01.01.2026 17:38]
position: absolute;
            bottom: -5px;
            left: 0;
            width: 0;
            height: 2px;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            box-shadow: 0 0 10px rgba(102, 126, 234, 0.8);
            transition: width 0.3s;
        }

        .nav-links a:hover::after {
            width: 100%;
        }

        .auth-btn {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 0.7rem 1.8rem;
            border-radius: 25px;
            font-weight: bold;
            border: none;
            cursor: pointer;
            transition: all 0.3s;
        }

        .auth-btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 8px 25px rgba(102, 126, 234, 0.6),
                        0 0 30px rgba(102, 126, 234, 0.4);
        }

        .user-menu {
            position: relative;
        }

        .user-badge {
            background: linear-gradient(135deg, #f093fb 0%, #f5576c 100%);
            color: white;
            padding: 0.7rem 1.8rem;
            border-radius: 25px;
            font-weight: bold;
            cursor: pointer;
            transition: all 0.3s;
            box-shadow: 0 4px 15px rgba(240, 147, 251, 0.4);
        }

        .user-badge:hover {
            transform: translateY(-2px);
            box-shadow: 0 8px 25px rgba(240, 147, 251, 0.6);
        }

        .dropdown {
            display: none;
            position: absolute;
            top: 120%;
            right: 0;
            background: rgba(26, 26, 46, 0.95);
            backdrop-filter: blur(10px);
            border-radius: 15px;
            padding: 1rem;
            min-width: 200px;
            box-shadow: 0 8px 32px rgba(0, 0, 0, 0.5);
            border: 1px solid rgba(102, 126, 234, 0.3);
        }

        .dropdown.active {
            display: block;
            animation: slideDown 0.3s ease-out;
        }

        @keyframes slideDown {
            from { opacity: 0; transform: translateY(-10px); }
            to { opacity: 1; transform: translateY(0); }
        }

        .dropdown-item {
            padding: 0.8rem;
            color: #e0e0e0;
            cursor: pointer;
            border-radius: 8px;
            transition: all 0.3s;
        }

        .dropdown-item:hover {
            background: rgba(102, 126, 234, 0.2);
            transform: translateX(5px);
        }

        /* Hero Section */
        .hero {
            background: linear-gradient(135deg, rgba(102, 126, 234, 0.1) 0%, rgba(118, 75, 162, 0.1) 100%);
            color: white;
            padding: 6rem 2rem;
            text-align: center;
            position: relative;
            overflow: hidden;
        }

        .hero::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle, rgba(102, 126, 234, 0.2) 0%, transparent 70%);
            animation: rotateBg 15s linear infinite;
        }

        @keyframes rotateBg {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }

        .hero h1 {
            font-size: 3.5rem;
            margin-bottom: 1rem;
            position: relative;
            z-index: 1;
            background: linear-gradient(135deg, #fff 0%, #667eea 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            animation: slideDown 1s ease-out;
            text-shadow: 0 0 40px rgba(102, 126, 234, 0.8);
        }

        .hero p {
            font-size: 1.4rem;
            margin-bottom: 2rem;
            position: relative;
            z-index: 1;
            animation: slideUp 1s ease-out;
        }

......., [01.01.2026 17:38]
.cta-button {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 1.2rem 3.5rem;
            border: none;
            border-radius: 30px;
            font-size: 1.2rem;
            font-weight: bold;
            cursor: pointer;
            transition: all 0.3s;
            position: relative;
            z-index: 1;
        }

        .cta-button:hover {
            transform: translateY(-3px) scale(1.05);
            box-shadow: 0 15px 40px rgba(102, 126, 234, 0.6),
                        0 0 50px rgba(102, 126, 234, 0.5);
        }

        /* Container */
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 4rem 2rem;
        }

        .section-title {
            font-size: 2.8rem;
            text-align: center;
            margin-bottom: 3rem;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            filter: drop-shadow(0 0 20px rgba(102, 126, 234, 0.5));
        }

        /* Cards */
        .grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
            gap: 2rem;
            margin-bottom: 4rem;
        }

        .card {
            background: rgba(26, 26, 46, 0.6);
            backdrop-filter: blur(10px);
            border-radius: 20px;
            padding: 2.5rem;
            box-shadow: 0 8px 32px rgba(0, 0, 0, 0.3);
            transition: all 0.4s;
            border: 1px solid rgba(102, 126, 234, 0.2);
            position: relative;
            overflow: hidden;
        }

        .card::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle, rgba(102, 126, 234, 0.1) 0%, transparent 70%);
            opacity: 0;
            transition: opacity 0.4s;
        }

        .card:hover::before {
            opacity: 1;
        }

        .card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 50px rgba(102, 126, 234, 0.4),
                        0 0 60px rgba(102, 126, 234, 0.2);
            border-color: rgba(102, 126, 234, 0.6);
        }

        .card h3 {
            color: #667eea;
            margin-bottom: 1rem;
            font-size: 1.6rem;
            position: relative;
            z-index: 1;
            text-shadow: 0 0 20px rgba(102, 126, 234, 0.5);
        }

        .card p {
            color: #b0b0b0;
            margin-bottom: 1.5rem;
            position: relative;
            z-index: 1;
        }

        .card-button {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 0.9rem 2rem;
            border: none;
            border-radius: 25px;
            cursor: pointer;
            font-weight: bold;
            width: 100%;
            transition: all 0.3s;
            position: relative;
            z-index: 1;
        }

        .card-button:hover {
            transform: scale(1.05);
            box-shadow: 0 8px 25px rgba(102, 126, 234, 0.5),
                        0 0 40px rgba(102, 126, 234, 0.3);
        }

        /* Modal */
        .modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.8);
            backdrop-filter: blur(10px);
            z-index: 2000;
            justify-content: center;
            align-items: center;
        }

        .modal.active {
            display: flex;
            animation: fadeIn 0.3s ease-out;
        }

        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }

......., [01.01.2026 17:38]
.modal-content {
            background: rgba(26, 26, 46, 0.95);
            backdrop-filter: blur(20px);
            padding: 3rem;
            border-radius: 25px;
            width: 90%;
            max-width: 450px;
            position: relative;
            border: 1px solid rgba(102, 126, 234, 0.3);
            box-shadow: 0 20px 60px rgba(0, 0, 0, 0.7),
                        0 0 100px rgba(102, 126, 234, 0.3);
            animation: slideUp 0.4s ease-out;
        }

        .close-btn {
            position: absolute;
            top: 1rem;
            right: 1.5rem;
            font-size: 2rem;
            cursor: pointer;
            color: #999;
            transition: all 0.3s;
        }

        .close-btn:hover {
            color: #667eea;
            transform: rotate(90deg);
            text-shadow: 0 0 20px rgba(102, 126, 234, 0.8);
        }

        .modal-content h2 {
            color: #667eea;
            margin-bottom: 2rem;
            text-align: center;
            font-size: 2rem;
            text-shadow: 0 0 20px rgba(102, 126, 234, 0.6);
        }

        .form-group {
            margin-bottom: 1.5rem;
        }

        .form-group label {
            display: block;
            margin-bottom: 0.5rem;
            color: #e0e0e0;
            font-weight: bold;
        }

        .form-group input {
            width: 100%;
            padding: 1rem;
            border: 2px solid rgba(102, 126, 234, 0.3);
            border-radius: 10px;
            font-size: 1rem;
            background: rgba(40, 40, 60, 0.6);
            color: #e0e0e0;
            transition: all 0.3s;
        }

        .form-group input:focus {
            outline: none;
            border-color: #667eea;
            box-shadow: 0 0 20px rgba(102, 126, 234, 0.4),
                        inset 0 0 10px rgba(102, 126, 234, 0.1);
        }

        .submit-btn {
            width: 100%;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 1.2rem;
            border: none;
            border-radius: 25px;
            font-size: 1.1rem;
            font-weight: bold;
            cursor: pointer;
            margin-top: 1rem;
            transition: all 0.3s;
        }

        .submit-btn:hover {
            transform: scale(1.05);
            box-shadow: 0 8px 30px rgba(102, 126, 234, 0.5),
                        0 0 50px rgba(102, 126, 234, 0.4);
        }

        .toggle-link {
            color: #667eea;
            cursor: pointer;
            text-decoration: underline;
            transition: all 0.3s;
        }

        .toggle-link:hover {
            text-shadow: 0 0 10px rgba(102, 126, 234, 0.8);
        }

        /* Page Management */
        .page {
            display: none;
        }

        .page.active {
            display: block;
            animation: fadeIn 0.5s ease-out;
        }

        /* Footer */
        footer {
            background: rgba(26, 26, 46, 0.95);
            color: #e0e0e0;
            padding: 3rem 2rem;
            text-align: center;
            border-top: 1px solid rgba(102, 126, 234, 0.3);
            margin-top: 4rem;
        }

        .footer-links a {
            color: #667eea;
            margin: 0 1rem;
            text-decoration: none;
            transition: all 0.3s;
        }

        .footer-links a:hover {
            text-shadow: 0 0 15px rgba(102, 126, 234, 0.8);
        }

        /* Vocabulary Section */
        .vocab-card {
            background: rgba(26, 26, 46, 0.8);
            border-radius: 15px;
            padding: 2rem;
            border: 1px solid rgba(102, 126, 234, 0.3);
            transition: all 0.3s;
        }

        .vocab-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 30px rgba(102, 126, 234, 0.3),
                        0 0 50px rgba(102, 126, 234, 0.2);
            border-color: rgba(102, 126, 234, 0.6);
        }

......., [01.01.2026 17:38]
.vocab-word {
            font-size: 1.8rem;
            font-weight: bold;
            color: #667eea;
            margin-bottom: 0.5rem;
            text-shadow: 0 0 15px rgba(102, 126, 234, 0.5);
        }

        .vocab-type {
            color: #764ba2;
            font-style: italic;
            margin-bottom: 1rem;
        }

        /* Success Message */
        .success-message {
            background: rgba(76, 175, 80, 0.2);
            border: 2px solid #4CAF50;
            color: #4CAF50;
            padding: 1rem;
            border-radius: 10px;
            margin-bottom: 1rem;
            text-align: center;
            box-shadow: 0 0 20px rgba(76, 175, 80, 0.3);
            animation: slideDown 0.5s ease-out;
        }

        .error-message {
            background: rgba(244, 67, 54, 0.2);
            border: 2px solid #f44336;
            color: #f44336;
            padding: 1rem;
            border-radius: 10px;
            margin-bottom: 1rem;
            text-align: center;
            box-shadow: 0 0 20px rgba(244, 67, 54, 0.3);
            animation: shake 0.5s ease-out;
        }

        @keyframes shake {
            0%, 100% { transform: translateX(0); }
            25% { transform: translateX(-10px); }
            75% { transform: translateX(10px); }
        }

        @media (max-width: 768px) {
            .hero h1 { font-size: 2.2rem; }
            .nav-links { gap: 1rem; font-size: 0.9rem; }
            .grid { grid-template-columns: 1fr; }
        }
    </style>
</head>
<body>
    <div class="animated-bg"></div>

    <!-- Navigation -->
    <nav>
        <div class="nav-container">
            <div class="logo glow-text">SAT with Edu Pro</div>
            <div class="nav-links">
                <a href="#" onclick="showPage('home')">Home</a>
                <a href="#" onclick="showPage('materials')">Materials</a>
                <a href="#" onclick="showPage('vocabulary')">Vocabulary</a>
                <a href="#" onclick="showPage('courses')">Courses</a>
                <a href="#" onclick="showPage('pricing')">Pricing</a>
                <div id="authSection">
                    <button class="auth-btn glow" onclick="openAuthModal('login')" id="loginBtn">Log In</button>
                </div>
            </div>
        </div>
    </nav>

    <!-- Home Page -->
    <div id="home" class="page active">
        <section class="hero">
            <h1 class="glow-text">Master Your SAT with Confidence</h1>
            <p>Access real practice tests, track progress, and achieve your dream score</p>
            <button class="cta-button glow" onclick="openAuthModal('signup')">Get Started Free</button>
        </section>

        <div class="container">
            <h2 class="section-title">Why Choose SAT with Edu Pro?</h2>
            <div class="grid">
                <div class="card">
                    <h3>📚 Free SAT Materials</h3>
                    <p>Access comprehensive study guides, practice tests, and resources.</p>
                    <button class="card-button" onclick="showPage('materials')">Browse Materials</button>
                </div>
                <div class="card">
                    <h3>📖 Vocabulary Builder</h3>
                    <p>Master 1000+ essential SAT vocabulary words with examples.</p>
                    <button class="card-button" onclick="showPage('vocabulary')">Learn Words</button>
                </div>
                <div class="card">
                    <h3>🎓 Expert Courses</h3>
                    <p>Structured courses designed to boost your score significantly.</p>
                    <button class="card-button" onclick="showPage('courses')">View Courses</button>
                </div>
                <div class="card">
                    <h3>⭐ Premium Plans</h3>
                    <p>Unlock advanced features and personalized learning paths.</p>
                    <button class="card-button" onclick="showPage('pricing')">View Plans</button>
                </div>
            </div>
        </div>
    </div>

......., [01.01.2026 17:38]
<!-- Materials Page -->
    <div id="materials" class="page">
        <div class="container">
            <h2 class="section-title">Free SAT Materials</h2>
            <div class="grid">
                <div class="card">
                    <h3>📝 Practice Tests</h3>
                    <p>Full-length SAT practice tests with answer explanations.</p>
                    <button class="card-button">Download PDF</button>
                </div>
                <div class="card">
                    <h3>📖 Study Guides</h3>
                    <p>Comprehensive guides covering all SAT sections.</p>
                    <button class="card-button">Access Guides</button>
                </div>
                <div class="card">
                    <h3>🧮 Math Formulas</h3>
                    <p>Essential formulas and concepts for SAT Math.</p>
                    <button class="card-button">Download Sheet</button>
                </div>
            </div>
        </div>
    </div>

    <!-- Vocabulary Page -->
    <div id="vocabulary" class="page">
        <div class="container">
            <h2 class="section-title">SAT Vocabulary Builder</h2>
            <div class="grid" id="vocabGrid">
                <!-- Vocabulary cards will be generated -->
            </div>
        </div>
    </div>

    <!-- Courses Page -->
    <div id="courses" class="page">
        <div class="container">
            <h2 class="section-title">Free SAT Courses</h2>
            <div class="grid">
                <div class="card">
                    <h3>🎯 SAT Fundamentals</h3>
                    <p>Master the basics - perfect for beginners.</p>
                    <p><strong>Duration:</strong> 4 weeks | <strong>Level:</strong> Beginner</p>
                    <button class="card-button">Enroll Now</button>
                </div>
                <div class="card">
                    <h3>🚀 Advanced Strategies</h3>
                    <p>Learn techniques to maximize your score.</p>
                    <p><strong>Duration:</strong> 6 weeks | <strong>Level:</strong> Advanced</p>
                    <button class="card-button">Enroll Now</button>
                </div>
                <div class="card">
                    <h3>📐 Math Mastery</h3>
                    <p>Complete coverage of all SAT math concepts.</p>
                    <p><strong>Duration:</strong> 5 weeks | <strong>Level:</strong> All Levels</p>
                    <button class="card-button">Enroll Now</button>
                </div>
            </div>
        </div>
    </div>

    <!-- Pricing Page -->
    <div id="pricing" class="page">
        <div class="container">
            <h2 class="section-title">Choose Your Plan</h2>
            <div class="grid">
                <div class="card">
                    <h3>Free Plan</h3>
                    <p style="font-size: 2.5rem; font-weight: bold; color: #667eea; margin: 1rem 0;">$0<span style="font-size: 1rem;">/month</span></p>
                    <p>✅ Basic materials</p>
                    <p>✅ 3 practice tests</p>
                    <p>✅ 500 vocabulary words</p>
                    <button class="card-button" onclick="alert('You\'re on the Free plan!')">Current Plan</button>
                </div>
                <div class="card glow">
                    <h3>Pro Plan</h3>
                    <p style="font-size: 2.5rem; font-weight: bold; color: #667eea; margin: 1rem 0;">$15<span style="font-size: 1rem;">/month</span></p>
                    <p>✅ Everything in Free</p>
                    <p>✅ Unlimited practice tests</p>
                    <p>✅ 5,000+ vocabulary words</p>
                    <p>✅ Advanced analytics</p>
                    <button class="card-button">Upgrade to Pro</button>
                </div>
                <div class="card">

......., [01.01.2026 17:38]
<h3>Expert Plan</h3>
                    <p style="font-size: 2.5rem; font-weight: bold; color: #667eea; margin: 1rem 0;">$30<span style="font-size: 1rem;">/month</span></p>
                    <p>✅ Everything in Pro</p>
                    <p>✅ AI-powered tutor</p>
                    <p>✅ 1-on-1 consultations</p>
                    <p>✅ Essay feedback</p>
                    <button class="card-button">Upgrade to Expert</button>
                </div>
            </div>
        </div>
    </div>

    <!-- Auth Modal -->
    <div id="authModal" class="modal">
        <div class="modal-content">
            <span class="close-btn" onclick="closeAuthModal()">&times;</span>
            <h2 id="authTitle">Welcome Back!</h2>
            <div id="messageContainer"></div>
            <form onsubmit="handleAuth(event)" id="authForm">
                <div class="form-group" id="nameGroup" style="display: none;">
                    <label for="authName">Full Name</label>
                    <input type="text" id="authName" placeholder="Enter your full name">
                </div>
                <div class="form-group">
                    <label for="authEmail">Email</label>
                    <input type="email" id="authEmail" required placeholder="Enter your email">
                </div>
                <div class="form-group">
                    <label for="authPassword">Password</label>
                    <input type="password" id="authPassword" required placeholder="Enter your password" minlength="6">
                </div>
                <button type="submit" class="submit-btn glow" id="submitBtn">Log In</button>
                <p style="text-align: center; margin-top: 1rem; color: #b0b0b0;">
                    <span id="toggleText">Don't have an account?</span>
                    <span class="toggle-link" onclick="toggleAuthMode()">Sign up</span>
                </p>
            </form>
        </div>
    </div>

    <!-- Footer -->
    <footer>
        <div>
            <h3 class="glow-text">SAT with Edu Pro</h3>
            <div class="footer-links" style="margin: 1.5rem 0;">
                <a href="#privacy">Privacy</a>
                <a href="#terms">Terms</a>
                <a href="mailto:blackpro2552@gmail.com">Contact
