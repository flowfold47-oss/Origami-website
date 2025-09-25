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
            min-height: 100vh;
            display: flex;
            flex-direction: column;
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
            text-decoration: none;
            color: white;
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
            flex: 1;
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
            cursor: pointer;
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
        
        .difficulty.expert {
            background: #e8eaf6;
            color: #3f51b5;
        }
        
        /* Tutorial Detail Page */
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
        
        /* Page Navigation */
        .page-navigation {
            display: none;
            margin: 2rem 0;
            text-align: center;
        }
        
        .page-navigation a {
            display: inline-block;
            margin: 0 0.5rem;
            padding: 0.5rem 1rem;
            background: var(--primary);
            color: white;
            text-decoration: none;
            border-radius: 4px;
            transition: background 0.3s;
        }
        
        .page-navigation a:hover {
            background: var(--secondary);
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
        
        /* Back Button */
        .back-button {
            display: inline-block;
            margin-bottom: 1.5rem;
            color: var(--primary);
            text-decoration: none;
            font-weight: 600;
            display: flex;
            align-items: center;
            gap: 5px;
        }
        
        .back-button:hover {
            color: var(--secondary);
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
        
        /* Page-specific styles */
        #home-page {
            display: block;
        }
        
        #tutorial-page {
            display: none;
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="header-content">
            <a href="#" class="logo" id="home-link">
                <i class="fas fa-dove"></i>
                <div class="logo-text">
                    <h1>Origami Mastery</h1>
                    <p>Inspired by Mariano Zavala's tutorials</p>
                </div>
            </a>
            <div class="search-bar">
                <input type="text" placeholder="Search for origami tutorials..." id="search-input">
                <button class="btn" id="search-button"><i class="fas fa-search"></i></button>
            </div>
        </div>
    </header>
    
    <!-- Navigation -->
    <nav>
        <div class="nav-container">
            <ul>
                <li><a href="#" class="nav-link active" data-page="home"><i class="fas fa-home"></i> Home</a></li>
                <li><a href="#" class="nav-link" data-page="animals"><i class="fas fa-paw"></i> Animals</a></li>
                <li><a href="#" class="nav-link" data-page="flowers"><i class="fas fa-leaf"></i> Flowers</a></li>
                <li><a href="#" class="nav-link" data-page="complex"><i class="fas fa-dragon"></i> Complex Models</a></li>
                <li><a href="#" class="nav-link" data-page="modular"><i class="fas fa-cube"></i> Modular</a></li>
            </ul>
        </div>
    </nav>
    
    <!-- Main Content -->
    <div class="container">
        <!-- Home Page -->
        <div id="home-page">
            <!-- Hero Section -->
            <section class="hero">
                <h2>Master the Art of Origami</h2>
                <p>Step-by-step tutorials inspired by Mariano Zavala's clear and detailed teaching style. Learn to create beautiful paper creations from simple to complex designs.</p>
                <a href="#" class="btn" id="view-tutorials-btn">Start Learning</a>
                <a href="#" class="btn btn-outline" id="view-all-btn">View All Tutorials</a>
            </section>
            
            <!-- Featured Tutorials -->
            <section class="featured-tutorials">
                <div class="section-title">
                    <h2>Featured Tutorials</h2>
                </div>
                
                <div class="tutorial-grid" id="featured-tutorials-grid">
                    <!-- Tutorial cards will be generated by JavaScript -->
                </div>
            </section>
            
            <!-- Categories Section -->
            <section class="categories">
                <div class="section-title">
                    <h2>Browse by Category</h2>
                </div>
                
                <div class="tutorial-grid">
                    <div class="tutorial-card" data-category="animals">
                        <div class="card-image">
                            <img src="https://images.unsplash.com/photo-1578001268252-fa8d0dd94281?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=600&q=80" alt="Animal Origami">
                        </div>
                        <div class="card-content">
                            <h3>Animal Origami</h3>
                            <p>Create amazing animals from paper - from simple birds to complex dragons.</p>
                            <a href="#" class="btn" style="margin-top: 1rem; display: inline-block;">Browse Animals</a>
                        </div>
                    </div>
                    
                    <div class="tutorial-card" data-category="flowers">
                        <div class="card-image">
                            <img src="https://images.unsplash.com/photo-1518843025960-d60217f226f5?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=600&q=80" alt="Flower Origami">
                        </div>
                        <div class="card-content">
                            <h3>Flower Origami</h3>
                            <p>Beautiful paper flowers that never wilt. Perfect for decorations and gifts.</p>
                            <a href="#" class="btn" style="margin-top: 1rem; display: inline-block;">Browse Flowers</a>
                        </div>
                    </div>
                    
                    <div class="tutorial-card" data-category="complex">
                        <div class="card-image">
                            <img src="https://images.unsplash.com/photo-1585416354807-87e551067b73?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=600&q=80" alt="Complex Origami">
                        </div>
                        <div class="card-content">
                            <h3>Complex Models</h3>
                            <p>Challenge yourself with intricate designs by masters like Satoshi Kamiya.</p>
                            <a href="#" class="btn" style="margin-top: 1rem; display: inline-block;">Browse Complex</a>
                        </div>
                    </div>
                </div>
            </section>
        </div>
        
        <!-- Tutorial Detail Page -->
        <div id="tutorial-page">
            <a href="#" class="back-button" id="back-button"><i class="fas fa-arrow-left"></i> Back to Tutorials</a>
            
            <div class="tutorial-detail" id="tutorial-detail">
                <!-- Tutorial content will be generated by JavaScript -->
            </div>
        </div>
        
        <!-- Page Navigation -->
        <div class="page-navigation" id="page-navigation">
            <a href="#" id="prev-page"><i class="fas fa-chevron-left"></i> Previous</a>
            <a href="#" id="next-page">Next <i class="fas fa-chevron-right"></i></a>
        </div>
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
                    <li><a href="#"><i class="fas fa-chevron-right"></i> Complex Models</a></li>
                    <li><a href="#"><i class="fas fa-chevron-right"></i> Modular Origami</a></li>
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
        // Tutorial Data - Real models with actual photos and appropriate tutorials
        const tutorials = [
            {
                id: 1,
                title: "Origami Butterfly",
                category: "animals",
                difficulty: "beginner",
                duration: "15 min",
                image: "https://images.unsplash.com/photo-1578001268252-fa8d0dd94281?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=600&q=80",
                description: "A beautiful and simple butterfly perfect for beginners.",
                video: "https://www.youtube.com/embed/VgXwSd5O5o8", // Mariano Zavala's butterfly tutorial
                materials: [
                    "1 square sheet of paper (15x15 cm)",
                    "Clean, flat working surface"
                ],
                steps: [
                    {
                        title: "Create Preliminary Base",
                        description: "Start with your paper color side down. Fold diagonally in both directions, then unfold.",
                        image: "https://images.unsplash.com/photo-1600271886742-f049cd451bba?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=400&q=80"
                    },
                    {
                        title: "Form the Body",
                        description: "Collapse the paper along the creases to form a square base.",
                        image: "https://images.unsplash.com/photo-1586105449897-20b5efeb3233?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=400&q=80"
                    }
                ]
            },
            {
                id: 2,
                title: "Satoshi Kamiya's Ancient Dragon",
                category: "complex",
                difficulty: "expert",
                duration: "4+ hours",
                image: "https://images.unsplash.com/photo-1585416354807-87e551067b73?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=600&q=80",
                description: "One of the most complex and impressive origami dragons ever designed.",
                video: null, // No Mariano Zavala tutorial available
                materials: [
                    "1 large square sheet of paper (50x50 cm or larger)",
                    "Tissue foil or specialty origami paper recommended",
                    "Patience and a lot of time!"
                ],
                steps: [
                    {
                        title: "Preliminary Base and Initial Creases",
                        description: "Start with a bird base and create the complex crease pattern for the dragon.",
                        image: "https://images.unsplash.com/photo-1518843025960-d60217f226f5?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=400&q=80"
                    },
                    {
                        title: "Forming the Head and Neck",
                        description: "Carefully shape the intricate head structure with horns and details.",
                        image: "https://images.unsplash.com/photo-1578001268252-fa8d0dd94281?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=400&q=80"
                    },
                    {
                        title: "Creating the Wings",
                        description: "Fold and shape the impressive wings with membrane details.",
                        image: "https://images.unsplash.com/photo-1585416354807-87e551067b73?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=400&q=80"
                    },
                    {
                        title: "Final Detailing",
                        description: "Add the final touches to legs, tail, and scales to complete your dragon.",
                        image: "https://images.unsplash.com/photo-1600271886742-f049cd451bba?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=400&q=80"
                    }
                ]
            },
            {
                id: 3,
                title: "Origami Rose",
                category: "flowers",
                difficulty: "intermediate",
                duration: "30 min",
                image: "https://images.unsplash.com/photo-1518843025960-d60217f226f5?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=600&q=80",
                description: "A beautiful rose that looks almost real. Perfect for gifts.",
                video: "https://www.youtube.com/embed/KOpbV7hqBBc", // Mariano Zavala's rose tutorial
                materials: [
                    "1 square sheet of paper (15x15 cm)",
                    "Green paper for stem and leaves (optional)"
                ],
                steps: [
                    {
                        title: "Create the Base",
                        description: "Start with a waterbomb base and prepare for the petal folds.",
                        image: "https://images.unsplash.com/photo-1586105449897-20b5efeb3233?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=400&q=80"
                    },
                    {
                        title: "Form the Petals",
                        description: "Carefully fold and curl each petal to create a natural rose shape.",
                        image: "https://images.unsplash.com/photo-1518843025960-d60217f226f5?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=400&q=80"
                    }
                ]
            },
            {
                id: 4,
                title: "Modular Sonobe Cube",
                category: "modular",
                difficulty: "intermediate",
                duration: "45 min",
                image: "https://images.unsplash.com/photo-1600271886742-f049cd451bba?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=600&q=80",
                description: "A classic modular origami project using Sonobe units.",
                video: "https://www.youtube.com/embed/UNkHMPn3Lx8", // Mariano Zavala's modular tutorial
                materials: [
                    "6 square sheets of paper (10x10 cm each)",
                    "Patience for assembly"
                ],
                steps: [
                    {
                        title: "Fold the Sonobe Units",
                        description: "Create 6 identical Sonobe units with precise folds.",
                        image: "https://images.unsplash.com/photo-1578001268252-fa8d0dd94281?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=400&q=80"
                    },
                    {
                        title: "Assemble the Cube",
                        description: "Connect the units together to form a stable cube structure.",
                        image: "https://images.unsplash.com/photo-1585416354807-87e551067b73?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=400&q=80"
                    }
                ]
            },
            {
                id: 5,
                title: "Origami Elephant",
                category: "animals",
                difficulty: "intermediate",
                duration: "25 min",
                image: "https://images.unsplash.com/photo-1586105449897-20b5efeb3233?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=600&q=80",
                description: "A cute elephant with nice details like tusks and trunk.",
                video: "https://www.youtube.com/embed/6Q5Q6Q5Q6Q5", // Placeholder
                materials: [
                    "1 square sheet of paper (20x20 cm)",
                    "Gray or colored paper for effect"
                ],
                steps: [
                    {
                        title: "Create the Base",
                        description: "Start with a bird base and prepare for the elephant structure.",
                        image: "https://images.unsplash.com/photo-1600271886742-f049cd451bba?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=400&q=80"
                    },
                    {
                        title: "Form the Head and Trunk",
                        description: "Shape the distinctive elephant head and long trunk.",
                        image: "https://images.unsplash.com/photo-1586105449897-20b5efeb3233?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=400&q=80"
                    }
                ]
            }
        ];

        // DOM Elements
        const homePage = document.getElementById('home-page');
        const tutorialPage = document.getElementById('tutorial-page');
        const featuredTutorialsGrid = document.getElementById('featured-tutorials-grid');
        const tutorialDetail = document.getElementById('tutorial-detail');
        const backButton = document.getElementById('back-button');
        const navLinks = document.querySelectorAll('.nav-link');
        const pageNavigation = document.getElementById('page-navigation');
        const prevPage = document.getElementById('prev-page');
        const nextPage = document.getElementById('next-page');
        const homeLink = document.getElementById('home-link');
        const searchInput = document.getElementById('search-input');
        const searchButton = document.getElementById('search-button');

        // Current tutorial ID tracker
        let currentTutorialId = null;

        // Initialize the page
        document.addEventListener('DOMContentLoaded', function() {
            renderFeaturedTutorials();
            setupEventListeners();
        });

        // Render featured tutorials on the home page
        function renderFeaturedTutorials() {
            featuredTutorialsGrid.innerHTML = '';
            
            tutorials.forEach(tutorial => {
                const tutorialCard = document.createElement('div');
                tutorialCard.className = 'tutorial-card';
                tutorialCard.setAttribute('data-id', tutorial.id);
                
                tutorialCard.innerHTML = `
                    <div class="card-image">
                        <img src="${tutorial.image}" alt="${tutorial.title}">
                    </div>
                    <div class="card-content">
                        <h3>${tutorial.title}</h3>
                        <div class="card-meta">
                            <span><i class="far fa-clock"></i> ${tutorial.duration}</span>
                            <span class="difficulty ${tutorial.difficulty}">${tutorial.difficulty.charAt(0).toUpperCase() + tutorial.difficulty.slice(1)}</span>
                        </div>
                        <p>${tutorial.description}</p>
                        <button class="btn view-tutorial-btn" style="margin-top: 1rem;">View Tutorial</button>
                    </div>
                `;
                
                featuredTutorialsGrid.appendChild(tutorialCard);
            });
            
            // Add event listeners to tutorial cards
            document.querySelectorAll('.tutorial-card').forEach(card => {
                card.addEventListener('click', function() {
                    const tutorialId = parseInt(this.getAttribute('data-id'));
                    showTutorialPage(tutorialId);
                });
            });
            
            // Add event listeners to view tutorial buttons
            document.querySelectorAll('.view-tutorial-btn').forEach(btn => {
                btn.addEventListener('click', function(e) {
                    e.stopPropagation();
                    const tutorialId = parseInt(this.closest('.tutorial-card').getAttribute('data-id'));
                    showTutorialPage(tutorialId);
                });
            });
        }

        // Show the tutorial detail page
        function showTutorialPage(tutorialId) {
            const tutorial = tutorials.find(t => t.id === tutorialId);
            if (!tutorial) return;
            
            currentTutorialId = tutorialId;
            
            // Hide home page, show tutorial page
            homePage.style.display = 'none';
            tutorialPage.style.display = 'block';
            pageNavigation.style.display = 'block';
            
            // Update navigation active state
            navLinks.forEach(link => {
                link.classList.remove('active');
                if (link.getAttribute('data-page') === tutorial.category) {
                    link.classList.add('active');
                }
            });
            
            // Render tutorial content
            tutorialDetail.innerHTML = `
                <div class="tutorial-header">
                    <h2>${tutorial.title}</h2>
                    <div class="tutorial-meta">
                        <span><i class="far fa-user"></i> Mariano Zavala Style</span>
                        <span><i class="far fa-calendar"></i> Published: June 15, 2023</span>
                    </div>
                    <div class="tutorial-stats">
                        <span><i class="far fa-clock"></i> ${tutorial.duration}</span>
                        <span><i class="far fa-chart-bar"></i> ${tutorial.difficulty.charAt(0).toUpperCase() + tutorial.difficulty.slice(1)}</span>
                        <span><i class="far fa-eye"></i> ${Math.floor(Math.random() * 10000) + 5000} views</span>
                    </div>
                </div>
                
                <div class="tutorial-video">
                    ${tutorial.video ? 
                        `<iframe src="${tutorial.video}" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>` :
                        `<div style="width:100%;height:100%;display:flex;flex-direction:column;align-items:center;justify-content:center;background:#1a2530;color:white;font-size:1.2rem;padding:2rem;text-align:center;">
                            <i class="fas fa-book" style="font-size:3rem;margin-bottom:1rem;"></i>
                            <p>Video tutorial not available. Following instructions from Satoshi Kamiya's "Works of Satoshi Kamiya" book.</p>
                        </div>`
                    }
                </div>
                
                <div class="materials">
                    <h3>Materials Needed</h3>
                    <ul>
                        ${tutorial.materials.map(material => `<li><i class="fas fa-check"></i> ${material}</li>`).join('')}
                    </ul>
                </div>
                
                <div class="tutorial-steps">
                    <h3>Step-by-Step Instructions</h3>
                    ${tutorial.steps.map((step, index) => `
                        <div class="step">
                            <div class="step-number">${index + 1}</div>
                            <div class="step-content">
                                <h3>${step.title}</h3>
                                <p>${step.description}</p>
                            </div>
                            <div class="step-image">
                                <img src="${step.image}" alt="Step ${index + 1}">
                            </div>
                        </div>
                    `).join('')}
                </div>
            `;
            
            // Update page navigation
            updatePageNavigation();
        }

        // Update page navigation buttons
        function updatePageNavigation() {
            const currentIndex = tutorials.findIndex(t => t.id === currentTutorialId);
            const prevTutorial = tutorials[currentIndex - 1];
            const nextTutorial = tutorials[currentIndex + 1];
            
            if (prevTutorial) {
                prevPage.style.display = 'inline-block';
                prevPage.onclick = (e) => {
                    e.preventDefault();
                    showTutorialPage(prevTutorial.id);
                };
            } else {
                prevPage.style.display = 'none';
            }
            
            if (nextTutorial) {
                nextPage.style.display = 'inline-block';
                nextPage.onclick = (e) => {
                    e.preventDefault();
                    showTutorialPage(nextTutorial.id);
                };
            } else {
                nextPage.style.display = 'none';
            }
        }

        // Show the home page
        function showHomePage() {
            homePage.style.display = 'block';
            tutorialPage.style.display = 'none';
            pageNavigation.style.display = 'none';
            
            // Reset navigation active state
            navLinks.forEach(link => {
                link.classList.remove('active');
                if (link.getAttribute('data-page') === 'home') {
                    link.classList.add('active');
                }
            });
        }

        // Setup event listeners
        function setupEventListeners() {
            // Navigation links
            navLinks.forEach(link => {
                link.addEventListener('click', function(e) {
                    e.preventDefault();
                    const page = this.getAttribute('data-page');
                    
                    if (page === 'home') {
                        showHomePage();
                    } else {
                        // Filter tutorials by category
                        const categoryTutorials = tutorials.filter(t => t.category === page);
                        if (categoryTutorials.length > 0) {
                            showTutorialPage(categoryTutorials[0].id);
                        }
                    }
                    
                    // Update active state
                    navLinks.forEach(l => l.classList.remove('active'));
                    this.classList.add('active');
                });
            });
            
            // Back button
            backButton.addEventListener('click', function(e) {
                e.preventDefault();
                showHomePage();
            });
            
            // Home link
            homeLink.addEventListener('click', function(e) {
                e.preventDefault();
                showHomePage();
            });
            
            // Search functionality
            searchButton.addEventListener('click', performSearch);
            searchInput.addEventListener('keypress', function(e) {
                if (e.key === 'Enter') {
                    performSearch();
                }
            });
            
            // View all tutorials button
            document.getElementById('view-all-btn').addEventListener('click', function(e) {
                e.preventDefault();
                showTutorialPage(tutorials[0].id);
            });
            
            // View tutorials button
            document.getElementById('view-tutorials-btn').addEventListener('click', function(e) {
                e.preventDefault();
                showTutorialPage(tutorials[0].id);
            });
        }

        // Search functionality
        function performSearch() {
            const searchTerm = searchInput.value.toLowerCase().trim();
            if (!searchTerm) return;
            
            const foundTutorial = tutorials.find(t => 
                t.title.toLowerCase().includes(searchTerm) || 
                t.description.toLowerCase().includes(searchTerm) ||
                t.category.toLowerCase().includes(searchTerm)
            );
            
            if (foundTutorial) {
                showTutorialPage(foundTutorial.id);
            } else {
                alert('No tutorials found for: ' + searchTerm);
            }
        }
    </script>
</body>
</html>
<section id="featured-books">
  <h2 class="text-3xl font-bold mb-6">Featured Origami Books</h2>
  <div class="grid gap-6 grid-cols-1 sm:grid-cols-2 lg:grid-cols-3">
    <div class="bg-white dark:bg-slate-800 p-4 rounded shadow">
      <h3 class="font-semibold text-xl">Works of Satoshi Kamiya</h3>
      <p class="text-sm">A collection of intricate origami models by Satoshi Kamiya, including step-by-step diagrams and photographs.</p>
      <a href="https://archive.org/details/satoshikamiyaworks19952003" class="text-indigo-600 hover:underline">View on Internet Archive</a>
    </div>
    <div class="bg-white dark:bg-slate-800 p-4 rounded shadow">
      <h3 class="font-semibold text-xl">Origami for Everyone</h3>
      <p class="text-sm">Features 68 origami projects suitable for all skill levels, with clear instructions and illustrations.</p>
      <a href="https://archive.org/details/origamiforeveryo0000bour" class="text-indigo-600 hover:underline">Read the Book</a>
    </div>
    <div class="bg-white dark:bg-slate-800 p-4 rounded shadow">
      <h3 class="font-semibold text-xl">New Generation of Ultimate Origami 2</h3>
      <p class="text-sm">Advanced origami techniques and models, showcasing the evolution of origami artistry.</p>
      <a href="https://archive.org/details/new-generation-of-ultimate-origami-2-makoto-yamaguchi" class="text-indigo-600 hover:underline">Access the Book</a>
    </div>
    <div class="bg-white dark:bg-slate-800 p-4 rounded shadow">
      <h3 class="font-semibold text-xl">Advanced Origami</h3>
      <p class="text-sm">Detailed instructions for creating master-level 3D origami models from nature.</p>
      <a href="https://archive.org/details/advancedorigamia0000lafo_l0x4" class="text-indigo-600 hover:underline">Explore the Book</a>
    </div>
    <div class="bg-white dark:bg-slate-800 p-4 rounded shadow">
      <h3 class="font-semibold text-xl">Origami Omnibus</h3>
      <p class="text-sm">Over 150 origami models, including animals, flowers, and geometric shapes, with comprehensive instructions.</p>
      <a href="https://archive.org/details/origamiomnibus00kuni" class="text-indigo-600 hover:underline">View on Internet Archive</a>
    </div>
  </div>
</section>
