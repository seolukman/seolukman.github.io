<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Lukman Mansuri - Digital Marketing Specialist</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            background: #000;
            color: #fff;
            font-family: 'Arial', sans-serif;
            overflow-x: hidden;
        }

        /* Background */
        .background {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: -1;
        }

        .bg-gradient {
            position: absolute;
            inset: 0;
            background: linear-gradient(135deg, rgba(147, 51, 234, 0.1) 0%, rgba(0, 0, 0, 1) 50%, rgba(59, 130, 246, 0.1) 100%);
        }

        .mouse-follower {
            position: absolute;
            width: 400px;
            height: 400px;
            background: radial-gradient(circle, rgba(147, 51, 234, 0.1) 0%, rgba(236, 72, 153, 0.05) 50%, transparent 70%);
            border-radius: 50%;
            filter: blur(40px);
            pointer-events: none;
            transition: all 0.3s ease;
        }

        .floating-particle {
            position: absolute;
            border-radius: 50%;
            filter: blur(20px);
            animation: float 6s ease-in-out infinite;
        }

        .particle-1 {
            top: 25%;
            left: 25%;
            width: 200px;
            height: 200px;
            background: radial-gradient(circle, rgba(59, 130, 246, 0.1) 0%, transparent 70%);
            animation-delay: 0s;
        }

        .particle-2 {
            bottom: 25%;
            right: 25%;
            width: 300px;
            height: 300px;
            background: radial-gradient(circle, rgba(34, 197, 94, 0.1) 0%, transparent 70%);
            animation-delay: 3s;
        }

        @keyframes float {
            0%, 100% { transform: translateY(0px) scale(1); }
            50% { transform: translateY(-20px) scale(1.1); }
        }

        /* Container */
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* Hero Section */
        .hero {
            min-height: 100vh;
            display: flex;
            align-items: center;
            position: relative;
            z-index: 1;
        }

        .hero-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 80px;
            align-items: center;
        }

        .hero-left {
            animation: slideInLeft 1s ease-out;
        }

        .badge {
            display: inline-flex;
            align-items: center;
            gap: 8px;
            padding: 12px 20px;
            background: rgba(147, 51, 234, 0.2);
            border: 1px solid rgba(147, 51, 234, 0.3);
            border-radius: 50px;
            margin-bottom: 30px;
            font-size: 14px;
            color: #c084fc;
        }

        .sparkle {
            animation: sparkle 2s ease-in-out infinite;
        }

        @keyframes sparkle {
            0%, 100% { transform: scale(1) rotate(0deg); }
            50% { transform: scale(1.2) rotate(180deg); }
        }

        .hero-title {
            font-size: 5rem;
            font-weight: 900;
            line-height: 0.9;
            margin-bottom: 30px;
        }

        .name-first {
            background: linear-gradient(135deg, #fff 0%, #c084fc 50%, #f472b6 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .name-last {
            background: linear-gradient(135deg, #a855f7 0%, #ec4899 50%, #f97316 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            animation: gradientShift 3s ease-in-out infinite;
        }

        @keyframes gradientShift {
            0%, 100% { filter: hue-rotate(0deg); }
            50% { filter: hue-rotate(30deg); }
        }

        .hero-description {
            font-size: 1.25rem;
            line-height: 1.6;
            color: #d1d5db;
            margin-bottom: 30px;
            max-width: 500px;
        }

        .hero-info {
            display: flex;
            gap: 30px;
            margin-bottom: 40px;
            font-size: 14px;
            color: #9ca3af;
        }

        .info-item {
            display: flex;
            align-items: center;
            gap: 8px;
        }

        .hero-buttons {
            display: flex;
            gap: 20px;
            flex-wrap: wrap;
        }

        .btn-primary, .btn-secondary {
            padding: 16px 32px;
            border-radius: 50px;
            font-weight: 600;
            font-size: 16px;
            cursor: pointer;
            transition: all 0.3s ease;
            display: flex;
            align-items: center;
            gap: 8px;
            border: none;
        }

        .btn-primary {
            background: linear-gradient(135deg, #8b5cf6 0%, #ec4899 100%);
            color: white;
            position: relative;
            overflow: hidden;
        }

        .btn-primary:hover {
            transform: scale(1.05);
            box-shadow: 0 20px 40px rgba(139, 92, 246, 0.3);
        }

        .btn-primary:hover .arrow {
            transform: translateX(4px);
        }

        .btn-secondary {
            background: transparent;
            color: white;
            border: 2px solid #6b7280;
        }

        .btn-secondary:hover {
            border-color: #8b5cf6;
            background: rgba(139, 92, 246, 0.1);
        }

        /* Avatar */
        .hero-right {
            display: flex;
            justify-content: center;
            animation: slideInRight 1s ease-out;
        }

        .avatar-container {
            position: relative;
            width: 350px;
            height: 350px;
        }

        .rotating-ring {
            position: absolute;
            border-radius: 50%;
            border: 2px solid;
        }

        .ring-1 {
            inset: 0;
            border-color: rgba(147, 51, 234, 0.3);
            animation: rotate 20s linear infinite;
        }

        .ring-2 {
            inset: 20px;
            border-color: rgba(236, 72, 153, 0.3);
            animation: rotateReverse 15s linear infinite;
        }

        .ring-3 {
            inset: 40px;
            border-color: rgba(59, 130, 246, 0.3);
            animation: rotate 25s linear infinite;
        }

        .avatar {
            position: absolute;
            inset: 60px;
            background: linear-gradient(135deg, #8b5cf6 0%, #ec4899 50%, #f97316 100%);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            box-shadow: 0 20px 60px rgba(139, 92, 246, 0.4);
        }

        .avatar-icon {
            font-size: 80px;
            opacity: 0.8;
        }

        .floating-icon {
            position: absolute;
            width: 50px;
            height: 50px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 24px;
        }

        .icon-1 {
            top: -10px;
            right: -10px;
            background: linear-gradient(135deg, #8b5cf6 0%, #ec4899 100%);
            animation: bounce 2s ease-in-out infinite;
        }

        .icon-2 {
            bottom: -10px;
            left: -10px;
            background: linear-gradient(135deg, #3b82f6 0%, #06b6d4 100%);
            animation: pulse 2s ease-in-out infinite;
        }

        .icon-3 {
            top: 50%;
            left: -30px;
            background: linear-gradient(135deg, #10b981 0%, #34d399 100%);
            animation: ping 2s ease-in-out infinite;
        }

        @keyframes rotate {
            from { transform: rotate(0deg); }
            to { transform: rotate(360deg); }
        }

        @keyframes rotateReverse {
            from { transform: rotate(360deg); }
            to { transform: rotate(0deg); }
        }

        @keyframes bounce {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-10px); }
        }

        @keyframes pulse {
            0%, 100% { transform: scale(1); }
            50% { transform: scale(1.1); }
        }

        @keyframes ping {
            0%, 100% { transform: scale(1); opacity: 1; }
            50% { transform: scale(1.2); opacity: 0.8; }
        }

        /* Sections */
        section {
            padding: 120px 0;
            position: relative;
            z-index: 1;
        }

        .section-header {
            text-align: center;
            margin-bottom: 80px;
        }

        .section-title {
            font-size: 4rem;
            font-weight: 900;
            margin-bottom: 20px;
        }

        .section-subtitle {
            font-size: 1.25rem;
            color: #9ca3af;
            max-width: 600px;
            margin: 0 auto;
            line-height: 1.6;
        }

        /* Skills Section */
        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 30px;
        }

        .skill-card {
            background: rgba(17, 24, 39, 0.5);
            border: 1px solid rgba(75, 85, 99, 0.3);
            border-radius: 20px;
            padding: 40px;
            transition: all 0.3s ease;
            opacity: 1;
            transform: translateY(0);
        }

        .skill-card:hover {
            transform: translateY(-10px) scale(1.02);
            border-color: rgba(139, 92, 246, 0.5);
            box-shadow: 0 20px 40px rgba(139, 92, 246, 0.1);
        }

        .skill-icon {
            width: 60px;
            height: 60px;
            border-radius: 15px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 28px;
            margin-bottom: 25px;
            transition: transform 0.3s ease;
        }

        .skill-card:hover .skill-icon {
            transform: scale(1.1);
        }

        .skill-card h3 {
            font-size: 1.5rem;
            font-weight: 700;
            margin-bottom: 20px;
            transition: color 0.3s ease;
        }

        .skill-card:hover h3 {
            color: #c084fc;
        }

        .skill-progress {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 10px;
            font-size: 14px;
        }

        .skill-label {
            color: #9ca3af;
        }

        .skill-percentage {
            color: #c084fc;
            font-weight: 600;
        }

        .progress-bar {
            width: 100%;
            height: 8px;
            background: rgba(75, 85, 99, 0.5);
            border-radius: 4px;
            overflow: hidden;
        }

        .progress-fill {
            height: 100%;
            border-radius: 4px;
            transition: width 1s ease-out;
        }

        /* Timeline */
        .timeline {
            position: relative;
            max-width: 1000px;
            margin: 0 auto;
        }

        .timeline-line {
            position: absolute;
            left: 50%;
            transform: translateX(-50%);
            width: 4px;
            height: 100%;
            background: linear-gradient(to bottom, #8b5cf6 0%, #ec4899 50%, #f97316 100%);
            border-radius: 2px;
        }

        .timeline-item {
            position: relative;
            margin-bottom: 80px;
            opacity: 1;
            transform: translateX(0);
        }

        .timeline-item.left {
            transform: translateX(0);
        }

        .timeline-content {
            background: rgba(17, 24, 39, 0.8);
            border: 1px solid rgba(75, 85, 99, 0.3);
            border-radius: 20px;
            padding: 40px;
            width: 45%;
            transition: all 0.3s ease;
        }

        .timeline-item.right .timeline-content {
            margin-left: 55%;
        }

        .timeline-item.left .timeline-content {
            margin-right: 55%;
        }

        .timeline-content:hover {
            border-color: rgba(139, 92, 246, 0.5);
            transform: scale(1.02);
        }

        .timeline-dot {
            position: absolute;
            left: 50%;
            top: 50%;
            transform: translate(-50%, -50%);
            width: 20px;
            height: 20px;
            background: linear-gradient(135deg, #f97316 0%, #dc2626 100%);
            border-radius: 50%;
            border: 4px solid #000;
        }

        .timeline-dot.current {
            background: linear-gradient(135deg, #8b5cf6 0%, #ec4899 100%);
        }

        .current-badge {
            display: inline-flex;
            align-items: center;
            gap: 8px;
            padding: 8px 16px;
            background: rgba(34, 197, 94, 0.2);
            color: #4ade80;
            border-radius: 20px;
            font-size: 12px;
            margin-bottom: 15px;
        }

        .pulse-dot {
            width: 8px;
            height: 8px;
            background: #4ade80;
            border-radius: 50%;
            animation: pulse 2s ease-in-out infinite;
        }

        .timeline-content h3 {
            font-size: 1.5rem;
            font-weight: 700;
            margin-bottom: 10px;
        }

        .company {
            color: #c084fc;
            font-weight: 600;
            margin-bottom: 8px;
        }

        .duration {
            color: #9ca3af;
            font-size: 14px;
            margin-bottom: 15px;
        }

        .description {
            color: #d1d5db;
            line-height: 1.6;
        }

        /* Education Grid */
        .education-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 30px;
        }

        .education-card {
            background: rgba(17, 24, 39, 0.5);
            border: 1px solid rgba(75, 85, 99, 0.3);
            border-radius: 20px;
            padding: 40px;
            text-align: center;
            transition: all 0.3s ease;
            opacity: 1;
            transform: translateY(0);
        }

        .education-card:hover {
            transform: translateY(-10px) scale(1.02);
            border-color: rgba(139, 92, 246, 0.5);
        }

        .education-icon {
            width: 80px;
            height: 80px;
            border-radius: 20px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 40px;
            margin: 0 auto 25px;
            transition: transform 0.3s ease;
        }

        .education-card:hover .education-icon {
            transform: scale(1.1);
        }

        .education-card h3 {
            font-size: 1.25rem;
            font-weight: 700;
            margin-bottom: 15px;
        }

        .qualification {
            color: #9ca3af;
            margin-bottom: 10px;
        }

        .year {
            color: #6b7280;
            font-size: 14px;
            margin-bottom: 20px;
        }

        .result {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding-top: 20px;
            border-top: 1px solid rgba(75, 85, 99, 0.3);
        }

        .percentage {
            font-weight: 700;
            font-size: 1.1rem;
        }

        /* Contact Grid */
        .contact-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            margin-bottom: 60px;
        }

        .contact-card {
            background: rgba(17, 24, 39, 0.5);
            border: 1px solid rgba(75, 85, 99, 0.3);
            border-radius: 20px;
            padding: 40px;
            text-align: center;
            transition: all 0.3s ease;
            opacity: 1;
            transform: translateY(0);
        }

        .contact-card:hover {
            transform: translateY(-10px) scale(1.02);
            border-color: rgba(139, 92, 246, 0.5);
        }

        .contact-icon {
            width: 80px;
            height: 80px;
            border-radius: 20px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 40px;
            margin: 0 auto 25px;
            transition: transform 0.3s ease;
        }

        .contact-card:hover .contact-icon {
            transform: scale(1.1);
        }

        .contact-card h3 {
            font-size: 1.25rem;
            font-weight: 700;
            margin-bottom: 15px;
        }

        .contact-card p {
            color: #9ca3af;
            transition: color 0.3s ease;
        }

        .contact-card:hover p {
            color: #c084fc;
        }

        /* Declaration */
        .declaration {
            text-align: center;
            background: linear-gradient(135deg, rgba(147, 51, 234, 0.1) 0%, rgba(236, 72, 153, 0.1) 100%);
            border: 1px solid rgba(147, 51, 234, 0.3);
            border-radius: 20px;
            padding: 40px;
        }

        .declaration-text {
            color: #d1d5db;
            margin-bottom: 20px;
            font-size: 1.1rem;
            line-height: 1.6;
        }

        .thank-you {
            font-size: 1.5rem;
            font-weight: 700;
            background: linear-gradient(135deg, #c084fc 0%, #ec4899 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        /* Gradient Classes */
        .purple-gradient { background: linear-gradient(135deg, #8b5cf6 0%, #ec4899 100%); }
        .blue-gradient { background: linear-gradient(135deg, #3b82f6 0%, #06b6d4 100%); }
        .green-gradient { background: linear-gradient(135deg, #10b981 0%, #34d399 100%); }
        .orange-gradient { background: linear-gradient(135deg, #f97316 0%, #dc2626 100%); }
        .yellow-gradient { background: linear-gradient(135deg, #eab308 0%, #f97316 100%); }
        .indigo-gradient { background: linear-gradient(135deg, #6366f1 0%, #8b5cf6 100%); }

        .purple-text { color: #c084fc; }
        .blue-text { 
            background: linear-gradient(135deg, #60a5fa 0%, #34d399 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }
        .green-text { 
            background: linear-gradient(135deg, #4ade80 0%, #34d399 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }
        .orange-text { 
            background: linear-gradient(135deg, #fb923c 0%, #dc2626 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        /* Animations */
        @keyframes slideInLeft {
            from {
                opacity: 0;
                transform: translateX(-50px);
            }
            to {
                opacity: 1;
                transform: translateX(0);
            }
        }

        @keyframes slideInRight {
            from {
                opacity: 0;
                transform: translateX(50px);
            }
            to {
                opacity: 1;
                transform: translateX(0);
            }
        }

        /* Scrollbar */
        ::-webkit-scrollbar {
            width: 8px;
        }

        ::-webkit-scrollbar-track {
            background: #111;
        }

        ::-webkit-scrollbar-thumb {
            background: linear-gradient(to bottom, #8b5cf6, #ec4899);
            border-radius: 4px;
        }

        ::-webkit-scrollbar-thumb:hover {
            background: linear-gradient(to bottom, #7c3aed, #db2777);
        }

        ::selection {
            background: rgba(139, 92, 246, 0.3);
            color: white;
        }

        /* Responsive */
        @media (max-width: 768px) {
            .hero-content {
                grid-template-columns: 1fr;
                gap: 40px;
                text-align: center;
            }
            
            .hero-title {
                font-size: 3rem;
            }
            
            .section-title {
                font-size: 2.5rem;
            }
            
            .timeline-content {
                width: 90%;
                margin: 0 5% !important;
            }
            
            .timeline-line {
                left: 20px;
            }
            
            .timeline-dot {
                left: 20px;
            }
            
            .avatar-container {
                width: 250px;
                height: 250px;
            }
            
            .avatar-icon {
                font-size: 60px;
            }
        }
    </style>
</head>
<body>
    <!-- Animated Background -->
    <div class="background">
        <div class="bg-gradient"></div>
        <div class="mouse-follower" id="mouseFollower"></div>
        <div class="floating-particle particle-1"></div>
        <div class="floating-particle particle-2"></div>
    </div>

    <!-- Hero Section -->
    <section class="hero">
        <div class="container">
            <div class="hero-content">
                <div class="hero-left">
                    <div class="badge">
                        <span class="sparkle">✨</span>
                        <span>Digital Marketing Specialist</span>
                    </div>
                    
                    <h1 class="hero-title">
                        <span class="name-first">LUKMAN</span>
                        <br>
                        <span class="name-last">MANSURI</span>
                    </h1>
                    
                    <p class="hero-description">
                        Transforming digital landscapes through strategic SEO, compelling content, and data-driven marketing solutions that drive real results.
                    </p>
                    
                    <div class="hero-info">
                        <div class="info-item">
                            <span class="icon">📍</span>
                            <span>Vadodara, Gujarat</span>
                        </div>
                        <div class="info-item">
                            <span class="icon">📅</span>
                            <span>Born Dec 17, 1998</span>
                        </div>
                        <div class="info-item">
                            <span class="icon">🌐</span>
                            <span>Gujarati, Hindi, English</span>
                        </div>
                    </div>
                    
                    <div class="hero-buttons">
                        <button class="btn-primary">
                            <span>Explore My Work</span>
                            <span class="arrow">→</span>
                        </button>
                        <button class="btn-secondary">
                            <span class="icon">🔗</span>
                            <span>Download CV</span>
                        </button>
                    </div>
                </div>
                
                <div class="hero-right">
                    <div class="avatar-container">
                        <div class="rotating-ring ring-1"></div>
                        <div class="rotating-ring ring-2"></div>
                        <div class="rotating-ring ring-3"></div>
                        
                        <div class="avatar">
                            <div class="avatar-icon">👤</div>
                        </div>
                        
                        <div class="floating-icon icon-1">🎯</div>
                        <div class="floating-icon icon-2">⚡</div>
                        <div class="floating-icon icon-3">✨</div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Skills Section -->
    <section class="skills" id="skills">
        <div class="container">
            <div class="section-header">
                <h2 class="section-title">EXPERTISE</h2>
                <p class="section-subtitle">
                    Mastering the art of digital transformation through cutting-edge strategies and innovative solutions
                </p>
            </div>
            
            <div class="skills-grid">
                <div class="skill-card" data-skill="95">
                    <div class="skill-icon purple-gradient">🎯</div>
                    <h3>SEO Optimization</h3>
                    <div class="skill-progress">
                        <span class="skill-label">Proficiency</span>
                        <span class="skill-percentage">95%</span>
                    </div>
                    <div class="progress-bar">
                        <div class="progress-fill purple-gradient" style="width: 95%"></div>
                    </div>
                </div>
                
                <div class="skill-card" data-skill="88">
                    <div class="skill-icon blue-gradient">💻</div>
                    <h3>Content Strategy</h3>
                    <div class="skill-progress">
                        <span class="skill-label">Proficiency</span>
                        <span class="skill-percentage">88%</span>
                    </div>
                    <div class="progress-bar">
                        <div class="progress-fill blue-gradient" style="width: 88%"></div>
                    </div>
                </div>
                
                <div class="skill-card" data-skill="82">
                    <div class="skill-icon green-gradient">📢</div>
                    <h3>Google Ads</h3>
                    <div class="skill-progress">
                        <span class="skill-label">Proficiency</span>
                        <span class="skill-percentage">82%</span>
                    </div>
                    <div class="progress-bar">
                        <div class="progress-fill green-gradient" style="width: 82%"></div>
                    </div>
                </div>
                
                <div class="skill-card" data-skill="90">
                    <div class="skill-icon orange-gradient">📱</div>
                    <h3>Social Media</h3>
                    <div class="skill-progress">
                        <span class="skill-label">Proficiency</span>
                        <span class="skill-percentage">90%</span>
                    </div>
                    <div class="progress-bar">
                        <div class="progress-fill orange-gradient" style="width: 90%"></div>
                    </div>
                </div>
                
                <div class="skill-card" data-skill="93">
                    <div class="skill-icon yellow-gradient">🏢</div>
                    <h3>Google My Business</h3>
                    <div class="skill-progress">
                        <span class="skill-label">Proficiency</span>
                        <span class="skill-percentage">93%</span>
                    </div>
                    <div class="progress-bar">
                        <div class="progress-fill yellow-gradient" style="width: 93%"></div>
                    </div>
                </div>
                
                <div class="skill-card" data-skill="75">
                    <div class="skill-icon indigo-gradient">🌐</div>
                    <h3>Web Development</h3>
                    <div class="skill-progress">
                        <span class="skill-label">Proficiency</span>
                        <span class="skill-percentage">75%</span>
                    </div>
                    <div class="progress-bar">
                        <div class="progress-fill indigo-gradient" style="width: 75%"></div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Experience Section -->
    <section class="experience" id="experience">
        <div class="container">
            <div class="section-header">
                <h2 class="section-title blue-text">JOURNEY</h2>
            </div>
            
            <div class="timeline">
                <div class="timeline-line"></div>
                
                <div class="timeline-item right">
                    <div class="timeline-content">
                        <div class="current-badge">
                            <div class="pulse-dot"></div>
                            Current Position
                        </div>
                        <h3>SEO Strategist</h3>
                        <p class="company">Techovarya</p>
                        <p class="duration">April 2024 - Present</p>
                        <p class="description">
                            Developing and implementing comprehensive SEO strategies to improve organic search rankings and drive targeted traffic.
                        </p>
                    </div>
                    <div class="timeline-dot current"></div>
                </div>
                
                <div class="timeline-item left">
                    <div class="timeline-content">
                        <h3>SEO Strategist</h3>
                        <p class="company">TechMero</p>
                        <p class="duration">December 2023 - March 2024 · 4 mos</p>
                        <p class="description">
                            Created and executed SEO strategies to improve search rankings and organic traffic for clients across various industries.
                        </p>
                    </div>
                    <div class="timeline-dot"></div>
                </div>
                
                <div class="timeline-item right">
                    <div class="timeline-content">
                        <h3>SEO Executive</h3>
                        <p class="company">Smartscripts Private Limited</p>
                        <p class="duration">April 2023 - October 2023 · 7 mos</p>
                        <p class="description">
                            Managed on-page and off-page SEO activities including keyword research, content optimization, and link building.
                        </p>
                    </div>
                    <div class="timeline-dot"></div>
                </div>
                
                <div class="timeline-item left">
                    <div class="timeline-content">
                        <h3>Digital Marketing Intern</h3>
                        <p class="company">Stimulus Co</p>
                        <p class="duration">September 2022 - March 2023 · 7 mos</p>
                        <p class="description">
                            Gained hands-on experience in SEO, content writing, and digital marketing strategies under professional guidance.
                        </p>
                    </div>
                    <div class="timeline-dot"></div>
                </div>
                
                <div class="timeline-item right">
                    <div class="timeline-content">
                        <h3>Lead Coordinator</h3>
                        <p class="company">Sanfinity Creative Solution</p>
                        <p class="duration">July 2021 - October 2021</p>
                        <p class="description">
                            Orchestrated lead generation initiatives and coordinated multi-channel marketing campaigns, contributing to significant client acquisition growth.
                        </p>
                    </div>
                    <div class="timeline-dot"></div>
                </div>
            </div>
        </div>
    </section>

    <!-- Education Section -->
    <section class="education" id="education">
        <div class="container">
            <div class="section-header">
                <h2 class="section-title green-text">EDUCATION</h2>
            </div>
            
            <div class="education-grid">
                <div class="education-card">
                    <div class="education-icon purple-gradient">🎓</div>
                    <h3>Ebrahim Bawany ITI</h3>
                    <p class="qualification">Digital Marketing</p>
                    <p class="year">February 2022</p>
                    <div class="result">
                        <span>Result:</span>
                        <span class="percentage purple-text">66.14%</span>
                    </div>
                </div>
                
                <div class="education-card">
                    <div class="education-icon blue-gradient">🎓</div>
                    <h3>Narayan Public School</h3>
                    <p class="qualification">Higher Secondary Certificate (HSC)</p>
                    <p class="year">July 2014 - May 2016</p>
                    <div class="result">
                        <span>Result:</span>
                        <span class="percentage blue-text">42.22%</span>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section class="contact" id="contact">
        <div class="container">
            <div class="section-header">
                <h2 class="section-title orange-text">CONNECT</h2>
                <p class="section-subtitle">
                    Ready to transform your digital presence? Let's create something extraordinary together.
                </p>
            </div>
            
            <div class="contact-grid">
                <div class="contact-card">
                    <div class="contact-icon purple-gradient">📞</div>
                    <h3>Phone</h3>
                    <p>+91 9033588841</p>
                </div>
                
                <div class="contact-card">
                    <div class="contact-icon blue-gradient">✉️</div>
                    <h3>Email</h3>
                    <p>lukmandevelopers@gmail.com</p>
                </div>
                
                <div class="contact-card">
                    <div class="contact-icon green-gradient">📍</div>
                    <h3>Location</h3>
                    <p>Mandvi Ladwada, Vadodara-390017</p>
                </div>
            </div>
            
            <div class="declaration">
                <p class="declaration-text">
                    I hereby declare that all the information provided above is true to the best of my knowledge.
                </p>
                <p class="thank-you">
                    Thank you for exploring my journey.
                </p>
            </div>
        </div>
    </section>

    <script>
    // Mouse follower effect
    document.addEventListener('mousemove', (e) => {
        const mouseFollower = document.getElementById('mouseFollower');
        if (mouseFollower) {
            mouseFollower.style.left = (e.clientX - 200) + 'px';
            mouseFollower.style.top = (e.clientY - 200) + 'px';
        }
    });

    // Make all elements visible immediately
    document.addEventListener('DOMContentLoaded', () => {
        // Show all elements immediately
        const animatableElements = document.querySelectorAll('.skill-card, .timeline-item, .education-card, .contact-card');
        animatableElements.forEach(el => {
            el.style.opacity = '1';
            el.style.transform = 'translateY(0)';
            
            // Special handling for skill progress bars
            if (el.classList.contains('skill-card')) {
                const progressFill = el.querySelector('.progress-fill');
                const skillPercentage = el.getAttribute('data-skill');
                if (progressFill && skillPercentage) {
                    progressFill.style.width = skillPercentage + '%';
                }
            }
        });

        // Add staggered animation delays (for visual appeal)
        document.querySelectorAll('.skill-card').forEach((card, index) => {
            card.style.transitionDelay = `${index * 100}ms`;
        });
        
        document.querySelectorAll('.education-card').forEach((card, index) => {
            card.style.transitionDelay = `${index * 150}ms`;
        });
        
        document.querySelectorAll('.contact-card').forEach((card, index) => {
            card.style.transitionDelay = `${index * 100}ms`;
        });
        
        document.querySelectorAll('.timeline-item').forEach((item, index) => {
            item.style.transitionDelay = `${index * 200}ms`;
        });

        // Smooth scrolling for anchor links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({
                        behavior: 'smooth',
                        block: 'start'
                    });
                }
            });
        });

        // Button hover effects
        document.querySelectorAll('.btn-primary, .btn-secondary').forEach(button => {
            button.addEventListener('mouseenter', function() {
                this.style.transform = 'scale(1.05)';
            });
            
            button.addEventListener('mouseleave', function() {
                this.style.transform = 'scale(1)';
            });
        });

        // Parallax effect for floating particles
        window.addEventListener('scroll', () => {
            const scrolled = window.pageYOffset;
            const particles = document.querySelectorAll('.floating-particle');
            
            particles.forEach((particle, index) => {
                const speed = 0.5 + (index * 0.2);
                particle.style.transform = `translateY(${scrolled * speed}px)`;
            });
        });

        // Fade-in page load animation
        document.body.style.opacity = '0';
        document.body.style.transition = 'opacity 0.5s ease';
        
        setTimeout(() => {
            document.body.style.opacity = '1';
        }, 100);
    });
</script>

</body>
</html>
