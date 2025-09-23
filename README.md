<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Origami Mastery | Mariano Zavala Style Tutorials</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        :root {
            --primary: #2c3e50;
            --secondary: #e74c3c;
            --accent: #3498db;
            --light: #f9f9f9;
            --dark: #2c3e50;
            --text: #333;
            --text-light: #777;
        }
        
        body {
            background-color: var(--light);
            color: var(--text);
            line-height: 1.6;
        }
        
        /* Header Styles */
        header {
            background: linear-gradient(135deg, var(--primary), #1a2530);
            color: white;
            padding: 1.5rem 0;
            box-shadow: 0 2px 15px rgba(0,0,0,0.1);
        }
        
        .header-content {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 1.5rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
        }
        
        .logo {
            display: flex;
            align-items: center;
            gap: 15px;
        }
        
        .logo i {
            font-size: 2.5rem;
            color: var(--secondary);
        }
        
        .logo-text h1 {
            font-size: 2.2rem;
            font-weight: 700;
            letter-spacing: 1px;
        }
        
        .logo-text p {
            font-size: 0.9rem;
            opacity: 0.8;
            margin-top: 5px;
        }
        
        /* Navigation */
        nav {
            background: white;
            padding: 1rem 0;
            position: sticky;
            top: 0;
            z-index: 100;
            box-shadow: 0 2px 10px rgba(0,0,0,0.05);
        }
        
        .nav-container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 1.5rem;
        }
        
        nav ul {
            list-style: none;
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 10px;
        }
        
        nav a {
            color: var(--dark);
            text-decoration: none;
            padding: 0.7rem 1.5rem;
            border-radius: 30px;
            font-weight: 600;
            transition: all 0.3s ease;
            display: flex;
            align-items: center;
            gap: 8px;
        }
        
        nav a:hover, nav a.active {
            background: var(--secondary);
            color: white;
        }
        
        /* Main Content */
        .container {
            max-width: 1200px;
            margin: 2rem auto;
            padding: 0 1.5rem;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 2.5rem;
            position: relative;
        }
        
        .section-title h2 {
            font-size: 2.2rem;
            color: var(--primary);
            display: inline-block;
            padding-bottom: 10px;
        }
        
        .section-title h2:after {
            content: '';
            position: absolute;
            width: 70px;
            height: 4px;
            background: var(--secondary);
            bottom: 0;
            left: 50%;
            transform: translateX(-50%);
        }
        
        /* Hero Section */
        .hero {
            background: linear-gradient(rgba(0,0,0,0.7), rgba(0,0,0,0.7)), url('https://images.unsplash.com/photo-1518843025960-d60217f226f5?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1200&q=80');
            background-size: cover;
            background-position: center;
            color: white;
            text-align: center;
            padding: 5rem 2rem;
            border-radius: 10px;
            margin-bottom: 3rem;
        }
        
        .hero h2 {
            font-size: 3rem;
            margin-bottom: 1rem;
            text-shadow: 2px 2px 5px rgba(0,0,0,0.5);
        }
        
        .hero p {
            font-size: 1.2rem;
            max-width: 700px;
            margin: 0 auto 2rem;
            opacity: 0.9;
        }
        
        .btn {
            display: inline-block;
            background: var(--secondary);
            color: white;
            padding: 0.8rem 2rem;
            border-radius: 30px;
            text-decoration: none;
            font-weight: 600;
            transition: all 0.3s ease;
            border: none;
            cursor: pointer;
            font-size: 1rem;
        }
        
        .btn:hover {
            background: #c0392b;
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }
        
        .btn-outline {
            background: transparent;
            border: 2px solid white;
            margin-left: 10px;
        }
        
        .btn-outline:hover {
            background: white;
            color: var(--secondary);
        }
        
        /* Tutorial Grid */
        .tutorial-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 2rem;
            margin-top: 2rem;
        }
        
        .tutorial-card {
            background: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }
        
        .tutorial-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0,0,0,0.1);
        }
        
        .card-image {
            height: 200px;
            overflow: hidden;
        }
        
        .card-image img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s ease;
        }
        
        .tutorial-card:hover .card-image img {
            transform: scale(1.1);
        }
        
        .card-content {
            padding: 1.5rem;
        }
        
        .card-content h3 {
            font-size: 1.3rem;
            margin-bottom: 0.5rem;
            color: var(--primary);
        }
        
        .card-meta {
            display: flex;
            justify-content: space-between;
            font-size: 0.9rem;
            color: var(--text-light);
            margin-bottom: 1rem;
        }
        
        .difficulty {
            display: inline-block;
            padding: 0.2rem 0.7rem;
            border-radius: 20px;
            font-size: 0.8rem;
            font-weight: 600;
        }
        
        .difficulty.beginner {
            background: #e8f6f3;
            color: #1abc9c;
        }
        
        .difficulty.intermediate {
            background: #fef9e7;
            color: #f39c12;
        }
        
        .difficulty.advanced {
            background: #fdedec;
            color: #e74c3c;
        }
        
        /* Tutorial Detail */
        .tutorial-detail {
            background: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
            margin-bottom: 3rem;
        }
        
        .tutorial-header {
            padding: 2rem;
            border-bottom: 1px solid #eee;
        }
        
        .tutorial-header h2 {
            font-size: 2rem;
            color: var(--primary);
            margin-bottom: 0.5rem;
        }
        
        .tutorial-meta {
            display: flex;
            gap: 1.5rem;
            margin-bottom: 1rem;
            flex-wrap: wrap;
        }
        
        .tutorial-stats {
            display: flex;
            gap: 1.5rem;
            color: var(--text-light);
        }
        
        .tutorial-video {
            width: 100%;
            height: 500px;
            background: #000;
        }
        
        .tutorial-video iframe {
            width: 100%;
            height: 100%;
            border: none;
        }
        
        .tutorial-steps {
            padding: 2rem;
        }
        
        .step {
            margin-bottom: 2rem;
            display: flex;
            gap: 1.5rem;
        }
        
        .step-number {
            background: var(--primary);
            color: white;
            width: 40px;
            height: 40px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: bold;
            flex-shrink: 0;
        }
        
        .step-content {
            flex: 1;
        }
        
        .step-content h3 {
            margin-bottom: 0.5rem;
            color: var(--primary);
        }
        
        .step-image {
            width: 200px;
            height: 150px;
            border-radius: 5px;
            overflow: hidden;
            flex-shrink: 0;
        }
        
        .step-image img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
        
        /* Materials Section */
        .materials {
            background: #f8f9fa;
            padding: 2rem;
            border-radius: 10px;
            margin-bottom: 2rem;
        }
        
        .materials h3 {
            margin-bottom: 1rem;
            color: var(--primary);
        }
        
        .materials ul {
            list-style: none;
        }
        
        .materials li {
            padding: 0.5rem 0;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .materials li i {
            color: var(--secondary);
        }
        
        /* Footer */
        footer {
            background: var(--dark);
            color: white;
            padding: 3rem 0 1.5rem;
            margin-top: 4rem;
        }
        
        .footer-content {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 1.5rem;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
        }
        
        .footer-section h3 {
            font-size: 1.3rem;
            margin-bottom: 1.5rem;
            position: relative;
            padding-bottom: 10px;
        }
        
        .footer-section h3:after {
            content: '';
            position: absolute;
            width: 50px;
            height: 3px;
            background: var(--secondary);
            bottom: 0;
            left: 0;
        }
        
        .footer-links {
            list-style: none;
        }
        
        .footer-links li {
            margin-bottom: 0.8rem;
        }
        
        .footer-links a {
            color: #ddd;
            text-decoration: none;
            transition: color 0.3s ease;
            display: flex;
            align-items: center;
            gap: 8px;
        }
        
        .footer-links a:hover {
            color: var(--secondary);
            padding-left: 5px;
        }
        
        .social-links {
            display: flex;
            gap: 15px;
            margin-top: 1.5rem;
        }
        
        .social-links a {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 40px;
            height: 40px;
            background: rgba(255,255,255,0.1);
            border-radius: 50%;
            color: white;
            transition: all 0.3s ease;
        }
        
        .social-links a:hover {
            background: var(--secondary);
            transform: translateY(-3px);
        }
        
        .copyright {
            text-align: center;
            padding-top: 2rem;
            margin-top: 2rem;
            border-top: 1px solid rgba(255,255,255,0.1);
            font-size: 0.9rem;
            color: #aaa;
        }
        
        /* Responsive Design */
        @media (max-width: 768px) {
            .header-content {
                flex-direction: column;
                text-align: center;
                gap: 1rem;
            }
            
            .hero h2 {
                font-size: 2.2rem;
            }
            
            .tutorial-grid {
                grid-template-columns: 1fr;
            }
            
            .step {
                flex-direction: column;
            }
            
            .step-image {
                width: 100%;
                height: 200px;
            }
            
            .tutorial-video {
                height: 300px;
            }
            
            nav ul {
                flex-direction: column;
                align-items: center;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="header-content">
            <div class="logo">
                <i class="fas fa-dove"></i>
                <div class="logo-text">
                    <h1>Origami Mastery</h1>
                    <p>Inspired by Mariano Zavala's tutorials</p>
                </div>
            </div>
            <div class="search-bar">
                <input type="text" placeholder="Search for origami tutorials...">
                <button class="btn"><i class="fas fa-search"></i></button>
            </div>
        </div>
    </header>
    
    <!-- Navigation -->
    <nav>
        <div class="nav-container">
            <ul>
                <li><a href="#" class="active"><i class="fas fa-home"></i> Home</a></li>
                <li><a href="#"><i class="fas fa-star"></i> Featured</a></li>
                <li><a href="#"><i class="fas fa-paw"></i> Animals</a></li>
                <li><a href="#"><i class="fas fa-leaf"></i> Flowers</a></li>
                <li><a href="#"><i class="fas fa-cube"></i> Modular</a></li>
                <li><a href="#"><i class="fas fa-gift"></i> Holiday</a></li>
                <li><a href="#"><i class="fas fa-user"></i> About</a></li>
            </ul>
        </div>
    </nav>
    
    <!-- Main Content -->
    <div class="container">
        <!-- Hero Section -->
        <section class="hero">
            <h2>Master the Art of Origami</h2>
            <p>Step-by-step tutorials inspired by Mariano Zavala's clear and detailed teaching style. Learn to create beautiful paper creations from simple to complex designs.</p>
            <a href="#" class="btn">Start Learning</a>
            <a href="#" class="btn btn-outline">View All Tutorials</a>
        </section>
        
        <!-- Featured Tutorials -->
        <section class="featured-tutorials">
            <div class="section-title">
                <h2>Featured Tutorials</h2>
            </div>
            
            <div class="tutorial-grid">
                <!-- Tutorial Card 1 -->
                <div class="tutorial-card">
                    <div class="card-image">
                        <img src="https://images.unsplash.com/photo-1585416354807-87e551067b73?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=600&q=80" alt="Origami Crane">
                    </div>
                    <div class="card-content">
                        <h3>Elegant Origami Crane</h3>
                        <div class="card-meta">
                            <span><i class="far fa-clock"></i> 25 min</span>
                            <span class="difficulty intermediate">Intermediate</span>
                        </div>
                        <p>Learn to fold the classic Japanese crane, a symbol of peace and longevity.</p>
                        <a href="#" class="btn" style="margin-top: 1rem; display: inline-block;">View Tutorial</a>
                    </div>
                </div>
                
                <!-- Tutorial Card 2 -->
                <div class="tutorial-card">
                    <div class="card-image">
                        <img src="https://images.unsplash.com/photo-1518843025960-d60217f226f5?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=600&q=80" alt="Origami Rose">
                    </div>
                    <div class="card-content">
                        <h3>Beautiful Origami Rose</h3>
                        <div class="card-meta">
                            <span><i class="far fa-clock"></i> 35 min</span>
                            <span class="difficulty advanced">Advanced</span>
                        </div>
                        <p>Create a stunning paper rose that looks almost real. Perfect for gifts.</p>
                        <a href="#" class="btn" style="margin-top: 1rem; display: inline-block;">View Tutorial</a>
                    </div>
                </div>
                
                <!-- Tutorial Card 3 -->
                <div class="tutorial-card">
                    <div class="card-image">
                        <img src="https://images.unsplash.com/photo-1578001268252-fa8d0dd94281?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=600&q=80" alt="Origami Dragon">
                    </div>
                    <div class="card-content">
                        <h3>Mythical Origami Dragon</h3>
                        <div class="card-meta">
                            <span><i class="far fa-clock"></i> 45 min</span>
                            <span class="difficulty advanced">Advanced</span>
                        </div>
                        <p>Challenge yourself with this intricate dragon design. Impressive results!</p>
                        <a href="#" class="btn" style="margin-top: 1rem; display: inline-block;">View Tutorial</a>
                    </div>
                </div>
            </div>
        </section>
        
        <!-- Tutorial Detail Section -->
        <section class="tutorial-detail-section">
            <div class="section-title">
                <h2>Tutorial of the Week</h2>
            </div>
            
            <div class="tutorial-detail">
                <div class="tutorial-header">
                    <h2>Origami Butterfly - Detailed Tutorial</h2>
                    <div class="tutorial-meta">
                        <span><i class="far fa-user"></i> Mariano Zavala Style</span>
                        <span><i class="far fa-calendar"></i> Published: June 15, 2023</span>
                    </div>
                    <div class="tutorial-stats">
                        <span><i class="far fa-clock"></i> 20 minutes</span>
                        <span><i class="far fa-chart-bar"></i> Intermediate</span>
                        <span><i class="far fa-eye"></i> 12,543 views</span>
                    </div>
                </div>
                
                <div class="tutorial-video">
                    <!-- Placeholder for video -->
                    <div style="width:100%;height:100%;display:flex;align-items:center;justify-content:center;background:#1a2530;color:white;font-size:1.2rem;">
                        <i class="fas fa-play-circle" style="font-size:3rem;margin-right:1rem;"></i>
                        Tutorial Video Player
                    </div>
                </div>
                
                <div class="materials">
                    <h3>Materials Needed</h3>
                    <ul>
                        <li><i class="fas fa-check"></i> 1 square sheet of paper (15x15 cm)</li>
                        <li><i class="fas fa-check"></i> Clean, flat working surface</li>
                        <li><i class="fas fa-check"></i> Optional: Bone folder for crisp folds</li>
                    </ul>
                </div>
                
                <div class="tutorial-steps">
                    <h3>Step-by-Step Instructions</h3>
                    
                    <div class="step">
                        <div class="step-number">1</div>
                        <div class="step-content">
                            <h3>Create Preliminary Base</h3>
                            <p>Start with your paper color side down. Fold diagonally in both directions, then unfold. Flip the paper over and fold in half horizontally and vertically, then unfold. You should have a grid of creases.</p>
                        </div>
                        <div class="step-image">
                            <img src="https://images.unsplash.com/photo-1600271886742-f049cd451bba?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=400&q=80" alt="Step 1">
                        </div>
                    </div>
                    
                    <div class="step">
                        <div class="step-number">2</div>
                        <div class="step-content">
                            <h3>Form the Body</h3>
                            <p>Collapse the paper along the creases to form a square base. This is the foundation for many origami models. Make sure all folds are precise for best results.</p>
                        </div>
                        <div class="step-image">
                            <img src="https://images.unsplash.com/photo-1586105449897-20b5efeb3233?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=400&q=80" alt="Step 2">
                        </div>
                    </div>
                    
                    <div class="step">
                        <div class="step-number">3</div>
                        <div class="step-content">
                            <h3>Shape the Wings</h3>
                            <p>Carefully fold the top layers down to create the butterfly's wings. Pay attention to symmetry as this will determine how balanced your final model looks.</p>
                        </div>
                        <div class="step-image">
                            <img src="https://images.unsplash.com/photo-1518843025960-d60217f226f5?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=400&q=80" alt="Step 3">
                        </div>
                    </div>
                    
                    <div class="step">
                        <div class="step-number">4</div>
                        <div class="step-content">
                            <h3>Final Adjustments</h3>
                            <p>Gently curve the wings to give your butterfly a more natural appearance. Make small adjustments until you're happy with the shape. Your origami butterfly is complete!</p>
                        </div>
                        <div class="step-image">
                            <img src="https://images.unsplash.com/photo-1578001268252-fa8d0dd94281?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=400&q=80" alt="Step 4">
                        </div>
                    </div>
                </div>
            </div>
        </section>
    </div>
    
    <!-- Footer -->
    <footer>
        <div class="footer-content">
            <div class="footer-section">
                <h3>Origami Mastery</h3>
                <p>Learn the beautiful art of paper folding with our detailed tutorials inspired by Mariano Zavala's teaching style.</p>
                <div class="social-links">
                    <a href="#"><i class="fab fa-youtube"></i></a>
                    <a href="#"><i class="fab fa-instagram"></i></a>
                    <a href="#"><i class="fab fa-pinterest"></i></a>
                    <a href="#"><i class="fab fa-facebook"></i></a>
                </div>
            </div>
            
            <div class="footer-section">
                <h3>Quick Links</h3>
                <ul class="footer-links">
                    <li><a href="#"><i class="fas fa-chevron-right"></i> Home</a></li>
                    <li><a href="#"><i class="fas fa-chevron-right"></i> Tutorials</a></li>
                    <li><a href="#"><i class="fas fa-chevron-right"></i> Beginner Guides</a></li>
                    <li><a href="#"><i class="fas fa-chevron-right"></i> Paper Recommendations</a></li>
                    <li><a href="#"><i class="fas fa-chevron-right"></i> About Us</a></li>
                </ul>
            </div>
            
            <div class="footer-section">
                <h3>Categories</h3>
                <ul class="footer-links">
                    <li><a href="#"><i class="fas fa-chevron-right"></i> Animals</a></li>
                    <li><a href="#"><i class="fas fa-chevron-right"></i> Flowers</a></li>
                    <li><a href="#"><i class="fas fa-chevron-right"></i> Modular Origami</a></li>
                    <li><a href="#"><i class="fas fa-chevron-right"></i> Holiday Themes</a></li>
                    <li><a href="#"><i class="fas fa-chevron-right"></i> Geometric Shapes</a></li>
                </ul>
            </div>
            
            <div class="footer-section">
                <h3>Newsletter</h3>
                <p>Subscribe to get notified about new tutorials and origami tips.</p>
                <form>
                    <input type="email" placeholder="Your email address" style="width:100%;padding:0.8rem;margin:1rem 0;border-radius:4px;border:none;">
                    <button type="submit" class="btn" style="width:100%;">Subscribe</button>
                </form>
            </div>
        </div>
        
        <div class="copyright">
            <p>&copy; 2023 Origami Mastery. Inspired by Mariano Zavala's tutorial style. All rights reserved.</p>
        </div>
    </footer>

    <script>
        // Simple JavaScript for interactive elements
        document.addEventListener('DOMContentLoaded', function() {
            // Add active class to navigation links on click
            const navLinks = document.querySelectorAll('nav a');
            navLinks.forEach(link => {
                link.addEventListener('click', function() {
                    navLinks.forEach(l => l.classList.remove('active'));
                    this.classList.add('active');
                });
            });
            
            // Tutorial card hover effect enhancement
            const tutorialCards = document.querySelectorAll('.tutorial-card');
            tutorialCards.forEach(card => {
                card.addEventListener('mouseenter', function() {
                    this.style.transform = 'translateY(-10px)';
                });
                
                card.addEventListener('mouseleave', function() {
                    this.style.transform = 'translateY(0)';
                });
            });
            
            // Simple search functionality
            const searchInput = document.querySelector('.search-bar input');
            const searchButton = document.querySelector('.search-bar button');
            
            searchButton.addEventListener('click', function() {
                const searchTerm = searchInput.value.toLowerCase();
                if (searchTerm) {
                    alert('Searching for: ' + searchTerm);
                    // In a real implementation, this would filter the tutorials
                }
            });
            
            searchInput.addEventListener('keypress', function(e) {
                if (e.key === 'Enter') {
                    searchButton.click();
                }
            });
        });
    </script>
</body>
</html>
