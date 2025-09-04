<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>AI CV Creator - Build Your Professional CV</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary: #4a6cf7;
            --primary-dark: #3a5cd8;
            --secondary: #6c757d;
            --dark: #1d2636;
            --light: #f8f9fa;
            --success: #28a745;
            --danger: #dc3545;
            --warning: #ffc107;
            --info: #17a2b8;
            --light-bg: #f5f8ff;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background-color: var(--light-bg);
            color: #333;
            line-height: 1.6;
        }
        
        .container {
            width: 100%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 15px;
        }
        
        /* Header Styles */
        header {
            background: linear-gradient(135deg, var(--primary), var(--primary-dark));
            color: white;
            padding: 1rem 0;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
            position: sticky;
            top: 0;
            z-index: 100;
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
        
        .logo i {
            font-size: 2rem;
        }
        
        .logo h1 {
            font-size: 1.8rem;
            font-weight: 700;
        }
        
        nav ul {
            display: flex;
            list-style: none;
            gap: 20px;
        }
        
        nav a {
            color: white;
            text-decoration: none;
            font-weight: 500;
            transition: all 0.3s ease;
            padding: 5px 10px;
            border-radius: 4px;
        }
        
        nav a:hover, nav a.active {
            background: rgba(255, 255, 255, 0.1);
        }
        
        /* Hero Section */
        .hero {
            text-align: center;
            padding: 4rem 1rem;
            background: white;
            border-radius: 0 0 10px 10px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.05);
            margin-bottom: 2rem;
            background: linear-gradient(rgba(255,255,255,0.9), rgba(255,255,255,0.9)), url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" width="100" height="100" viewBox="0 0 100 100"><rect width="100" height="100" fill="%23f5f8ff"/><path d="M0 0L100 100" stroke="%234a6cf7" stroke-width="1"/><path d="M100 0L0 100" stroke="%234a6cf7" stroke-width="1"/></svg>');
            background-size: cover;
        }
        
        .hero h2 {
            font-size: 2.5rem;
            margin-bottom: 1rem;
            color: var(--dark);
        }
        
        .hero p {
            font-size: 1.2rem;
            color: var(--secondary);
            max-width: 800px;
            margin: 0 auto 2rem;
        }
        
        .btn {
            display: inline-block;
            padding: 12px 24px;
            background: var(--primary);
            color: white;
            border: none;
            border-radius: 5px;
            font-size: 1rem;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
            text-decoration: none;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
        }
        
        .btn:hover {
            background: var(--primary-dark);
            transform: translateY(-2px);
            box-shadow: 0 6px 8px rgba(0, 0, 0, 0.15);
        }
        
        .btn-secondary {
            background: var(--secondary);
        }
        
        .btn-secondary:hover {
            background: #5a6268;
        }
        
        .btn-success {
            background: var(--success);
        }
        
        .btn-success:hover {
            background: #218838;
        }
        
        /* Main Content */
        .main-content {
            display: flex;
            gap: 2rem;
            margin-bottom: 3rem;
        }
        
        /* Form Styles */
        .cv-form {
            flex: 1;
            background: white;
            padding: 2rem;
            border-radius: 10px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.05);
        }
        
        .form-section {
            margin-bottom: 2rem;
            padding-bottom: 1.5rem;
            border-bottom: 1px solid #eee;
        }
        
        .form-section h3 {
            color: var(--primary);
            padding-bottom: 0.5rem;
            margin-bottom: 1.5rem;
            border-bottom: 2px solid var(--primary);
            display: inline-block;
        }
        
        .form-group {
            margin-bottom: 1.2rem;
        }
        
        .form-group label {
            display: block;
            margin-bottom: 0.5rem;
            font-weight: 500;
            color: var(--dark);
        }
        
        .form-control {
            width: 100%;
            padding: 12px 15px;
            border: 1px solid #ddd;
            border-radius: 5px;
            font-size: 1rem;
            transition: all 0.3s ease;
        }
        
        .form-control:focus {
            border-color: var(--primary);
            outline: none;
            box-shadow: 0 0 0 3px rgba(74, 108, 247, 0.2);
        }
        
        textarea.form-control {
            min-height: 100px;
            resize: vertical;
        }
        
        /* Preview Styles */
        .cv-preview {
            flex: 1;
            background: white;
            padding: 2rem;
            border-radius: 10px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.05);
            position: sticky;
            top: 100px;
            max-height: calc(100vh - 120px);
            overflow-y: auto;
        }
        
        .preview-header {
            text-align: center;
            margin-bottom: 2rem;
            padding-bottom: 1.5rem;
            border-bottom: 2px solid #eee;
        }
        
        .preview-header h2 {
            font-size: 2rem;
            color: var(--dark);
            margin-bottom: 0.5rem;
        }
        
        .preview-header p {
            color: var(--secondary);
            font-size: 1.1rem;
        }
        
        .preview-section {
            margin-bottom: 1.5rem;
        }
        
        .preview-section h3 {
            color: var(--primary);
            border-bottom: 1px solid #eee;
            padding-bottom: 0.5rem;
            margin-bottom: 1rem;
        }
        
        .experience-item, .education-item {
            margin-bottom: 1.2rem;
        }
        
        .experience-item h4, .education-item h4 {
            color: var(--dark);
        }
        
        .date {
            color: var(--secondary);
            font-style: italic;
            margin-bottom: 0.5rem;
        }
        
        .skills-list {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
        }
        
        .skill-tag {
            background: #e9f0ff;
            color: var(--primary);
            padding: 5px 12px;
            border-radius: 20px;
            font-size: 0.9rem;
        }
        
        /* Features Section */
        .features {
            padding: 4rem 0;
            background: white;
            border-radius: 10px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.05);
            margin-bottom: 2rem;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 3rem;
        }
        
        .section-title h2 {
            font-size: 2.2rem;
            color: var(--dark);
            margin-bottom: 1rem;
        }
        
        .section-title p {
            color: var(--secondary);
            max-width: 700px;
            margin: 0 auto;
        }
        
        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }
        
        .feature-card {
            background: var(--light);
            padding: 2rem;
            border-radius: 10px;
            text-align: center;
            transition: all 0.3s ease;
        }
        
        .feature-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
        }
        
        .feature-icon {
            font-size: 2.5rem;
            color: var(--primary);
            margin-bottom: 1rem;
        }
        
        .feature-card h3 {
            margin-bottom: 1rem;
            color: var(--dark);
        }
        
        /* Footer */
        footer {
            background: var(--dark);
            color: white;
            padding: 3rem 0 1rem;
        }
        
        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            margin-bottom: 2rem;
        }
        
        .footer-column h3 {
            font-size: 1.2rem;
            margin-bottom: 1.5rem;
            position: relative;
            padding-bottom: 0.5rem;
        }
        
        .footer-column h3::after {
            content: '';
            position: absolute;
            left: 0;
            bottom: 0;
            width: 40px;
            height: 2px;
            background: var(--primary);
        }
        
        .footer-column p {
            margin-bottom: 1rem;
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
            transition: all 0.3s ease;
        }
        
        .footer-links a:hover {
            color: var(--primary);
            padding-left: 5px;
        }
        
        .social-links {
            display: flex;
            gap: 1rem;
            margin-top: 1rem;
        }
        
        .social-links a {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            width: 40px;
            height: 40px;
            background: rgba(255, 255, 255, 0.1);
            color: white;
            border-radius: 50%;
            transition: all 0.3s ease;
        }
        
        .social-links a:hover {
            background: var(--primary);
            transform: translateY(-3px);
        }
        
        .copyright {
            text-align: center;
            padding-top: 2rem;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        /* Responsive Design */
        @media (max-width: 992px) {
            .main-content {
                flex-direction: column;
            }
            
            .cv-preview {
                position: static;
                max-height: none;
            }
            
            .hero h2 {
                font-size: 2rem;
            }
            
            .hero p {
                font-size: 1rem;
            }
        }
        
        @media (max-width: 768px) {
            .header-content {
                flex-direction: column;
                text-align: center;
                gap: 1rem;
            }
            
            nav ul {
                justify-content: center;
                flex-wrap: wrap;
            }
            
            .logo {
                justify-content: center;
            }
            
            .hero {
                padding: 2rem 1rem;
            }
            
            .hero h2 {
                font-size: 1.8rem;
            }
            
            .section-title h2 {
                font-size: 1.8rem;
            }
        }
    </style>
</head>
<body>
    <!-- Header Section -->
    <header>
        <div class="container">
            <div class="header-content">
                <div class="logo">
                    <i class="fas fa-robot"></i>
                    <h1>AI CV Creator</h1>
                </div>
                <nav>
                    <ul>
                        <li><a href="#" class="active">Home</a></li>
                        <li><a href="#">Templates</a></li>
                        <li><a href="#">Examples</a></li>
                        <li><a href="#">Pricing</a></li>
                        <li><a href="#">Contact</a></li>
                    </ul>
                </nav>
            </div>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero">
        <div class="container">
            <h2>Create a Professional CV for AI Tools & Technologies</h2>
            <p>Stand out in the AI industry with a tailored CV that highlights your machine learning, deep learning, and AI tool expertise. Built by Amir for AI professionals.</p>
            <a href="#" class="btn">Get Started For Free</a>
        </div>
    </section>

    <!-- Main Content -->
    <div class="container">
        <div class="main-content">
            <!-- CV Form -->
            <div class="cv-form">
                <div class="form-section">
                    <h3>Personal Information</h3>
                    <div class="form-group">
                        <label for="fullName">Full Name</label>
                        <input type="text" id="fullName" class="form-control" placeholder="e.g. Jane Smith">
                    </div>
                    <div class="form-group">
                        <label for="jobTitle">Job Title</label>
                        <input type="text" id="jobTitle" class="form-control" placeholder="e.g. AI Engineer">
                    </div>
                    <div class="form-group">
                        <label for="email">Email</label>
                        <input type="email" id="email" class="form-control" placeholder="e.g. jane@example.com">
                    </div>
                    <div class="form-group">
                        <label for="phone">Phone</label>
                        <input type="tel" id="phone" class="form-control" placeholder="e.g. (555) 123-4567">
                    </div>
                    <div class="form-group">
                        <label for="location">Location</label>
                        <input type="text" id="location" class="form-control" placeholder="e.g. San Francisco, CA">
                    </div>
                    <div class="form-group">
                        <label for="summary">Professional Summary</label>
                        <textarea id="summary" class="form-control" placeholder="Brief overview of your skills and experience"></textarea>
                    </div>
                </div>

                <div class="form-section">
                    <h3>AI Skills & Technologies</h3>
                    <div class="form-group">
                        <label for="aiSkills">List your AI skills (comma separated)</label>
                        <textarea id="aiSkills" class="form-control" placeholder="e.g. TensorFlow, PyTorch, NLP, Computer Vision"></textarea>
                    </div>
                    <div class="form-group">
                        <label for="programming">Programming Languages</label>
                        <input type="text" id="programming" class="form-control" placeholder="e.g. Python, R, Java, C++">
                    </div>
                    <div class="form-group">
                        <label for="tools">AI Tools & Frameworks</label>
                        <input type="text" id="tools" class="form-control" placeholder="e.g. Keras, Scikit-learn, OpenAI GPT, Hugging Face">
                    </div>
                </div>

                <div class="form-section">
                    <h3>Work Experience</h3>
                    <div class="form-group">
                        <label for="jobTitle">Job Title</label>
                        <input type="text" class="form-control" placeholder="e.g. Machine Learning Engineer">
                    </div>
                    <div class="form-group">
                        <label for="company">Company</label>
                        <input type="text" class="form-control" placeholder="e.g. TechAI Solutions">
                    </div>
                    <div class="form-group">
                        <label for="dateRange">Date Range</label>
                        <input type="text" class="form-control" placeholder="e.g. Jan 2020 - Present">
                    </div>
                    <div class="form-group">
                        <label for="jobDescription">Description</label>
                        <textarea class="form-control" placeholder="Describe your responsibilities and achievements"></textarea>
                    </div>
                    <button class="btn btn-secondary">Add Another Position</button>
                </div>

                <div class="form-section">
                    <h3>Education</h3>
                    <div class="form-group">
                        <label for="degree">Degree</label>
                        <input type="text" class="form-control" placeholder="e.g. M.S. in Artificial Intelligence">
                    </div>
                    <div class="form-group">
                        <label for="school">School</label>
                        <input type="text" class="form-control" placeholder="e.g. Stanford University">
                    </div>
                    <div class="form-group">
                        <label for="gradYear">Graduation Year</label>
                        <input type="text" class="form-control" placeholder="e.g. 2019">
                    </div>
                </div>

                <div class="form-section">
                    <h3>AI Projects</h3>
                    <div class="form-group">
                        <label for="projectName">Project Name</label>
                        <input type="text" class="form-control" placeholder="e.g. Sentiment Analysis Tool">
                    </div>
                    <div class="form-group">
                        <label for="projectDesc">Description</label>
                        <textarea class="form-control" placeholder="Describe the project and technologies used"></textarea>
                    </div>
                    <button class="btn btn-secondary">Add Another Project</button>
                </div>

                <button class="btn btn-success" style="width: 100%;">Generate CV</button>
            </div>

            <!-- CV Preview -->
            <div class="cv-preview">
                <div class="preview-header">
                    <h2 id="previewName">Jane Smith</h2>
                    <p id="previewTitle">AI Engineer</p>
                    <p id="previewContact">jane@example.com • (555) 123-4567 • San Francisco, CA</p>
                </div>

                <div class="preview-section">
                    <h3>Professional Summary</h3>
                    <p id="previewSummary">Experienced AI engineer with 5+ years specializing in machine learning and deep learning applications. Skilled in developing AI solutions for various industries including healthcare, finance, and e-commerce.</p>
                </div>

                <div class="preview-section">
                    <h3>AI Skills & Technologies</h3>
                    <div class="skills-list">
                        <span class="skill-tag">TensorFlow</span>
                        <span class="skill-tag">PyTorch</span>
                        <span class="skill-tag">Python</span>
                        <span class="skill-tag">NLP</span>
                        <span class="skill-tag">Computer Vision</span>
                        <span class="skill-tag">OpenAI GPT</span>
                        <span class="skill-tag">Hugging Face</span>
                        <span class="skill-tag">Keras</span>
                        <span class="skill-tag">Scikit-learn</span>
                    </div>
                </div>

                <div class="preview-section">
                    <h3>Work Experience</h3>
                    <div class="experience-item">
                        <h4>Senior AI Engineer</h4>
                        <p class="date">TechAI Solutions • Jan 2020 - Present</p>
                        <p>Led development of machine learning models for predictive analytics, resulting in a 25% improvement in forecasting accuracy. Managed a team of 5 data scientists.</p>
                    </div>
                    <div class="experience-item">
                        <h4>Machine Learning Specialist</h4>
                        <p class="date">DataWorks Inc. • Jun 2017 - Dec 2019</p>
                        <p>Developed and deployed NLP models for sentiment analysis and text classification. Implemented deep learning solutions for image recognition tasks.</p>
                    </div>
                </div>

                <div class="preview-section">
                    <h3>Education</h3>
                    <div class="education-item">
                        <h4>M.S. in Artificial Intelligence</h4>
                        <p class="date">Stanford University • 2019</p>
                    </div>
                    <div class="education-item">
                        <h4>B.S. in Computer Science</h4>
                        <p class="date">UC Berkeley • 2015</p>
                    </div>
                </div>

                <div class="preview-section">
                    <h3>AI Projects</h3>
                    <div class="experience-item">
                        <h4>Sentiment Analysis Tool</h4>
                        <p>Developed a transformer-based model for analyzing customer feedback sentiment with 95% accuracy. Deployed as a microservice using Docker and Kubernetes.</p>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <!-- Features Section -->
    <section class="features">
        <div class="container">
            <div class="section-title">
                <h2>Why Choose AI CV Creator</h2>
                <p>Built by Amir specifically for AI professionals, our CV creator offers unique features to help you stand out in the competitive AI job market.</p>
            </div>
            
            <div class="features-grid">
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-brain"></i>
                    </div>
                    <h3>AI-Optimized Templates</h3>
                    <p>Templates designed specifically for AI roles, highlighting the skills and experience that recruiters look for.</p>
                </div>
                
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-bolt"></i>
                    </div>
                    <h3>Quick & Easy</h3>
                    <p>Create a professional CV in minutes with our intuitive drag-and-drop interface and pre-written examples.</p>
                </div>
                
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-download"></i>
                    </div>
                    <h3>Multiple Export Formats</h3>
                    <p>Download your CV as PDF, Word, or HTML. Perfect for online applications and professional profiles.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-column">
                    <h3>AI CV Creator</h3>
                    <p>Create professional CVs tailored for AI professionals. Stand out with a CV that highlights your unique skills in artificial intelligence.</p>
                    <div class="social-links">
                        <a href="#"><i class="fab fa-twitter"></i></a>
                        <a href="#"><i class="fab fa-linkedin"></i></a>
                        <a href="#"><i class="fab fa-github"></i></a>
                        <a href="#"><i class="fab fa-facebook"></i></a>
                    </div>
                </div>
                
                <div class="footer-column">
                    <h3>Quick Links</h3>
                    <ul class="footer-links">
                        <li><a href="#">Home</a></li>
                        <li><a href="#">Templates</a></li>
                        <li><a href="#">Examples</a></li>
                        <li><a href="#">Pricing</a></li>
                        <li><a href="#">Contact</a></li>
                    </ul>
                </div>
                
                <div class="footer-column">
                    <h3>Resources</h3>
                    <ul class="footer-links">
                        <li><a href="#">CV Writing Tips</a></li>
                        <li><a href="#">AI Industry Insights</a></li>
                        <li><a href="#">Job Search Strategies</a></li>
                        <li><a href="#">Interview Preparation</a></li>
                    </ul>
                </div>
                
                <div class="footer-column">
                    <h3>Contact Us</h3>
                    <p><i class="fas fa-envelope"></i> info@aicvcreator.com</p>
                    <p><i class="fas fa-phone"></i> +1 (555) 123-4567</p>
                    <p><i class="fas fa-map-marker-alt"></i> San Francisco, CA</p>
                </div>
            </div>
            
            <div class="copyright">
                <p>&copy; 2023 AI CV Creator. Built by Amir. All rights reserved.</p>
            </div>
        </div>
    </footer>

    <script>
        // Simple JavaScript to update the preview as user types
        document.getElementById('fullName').addEventListener('input', function(e) {
            document.getElementById('previewName').textContent = e.target.value || 'Jane Smith';
        });

        document.getElementById('jobTitle').addEventListener('input', function(e) {
            document.getElementById('previewTitle').textContent = e.target.value || 'AI Engineer';
        });

        document.getElementById('email').addEventListener('input', function(e) {
            updateContactInfo();
        });

        document.getElementById('phone').addEventListener('input', function(e) {
            updateContactInfo();
        });

        document.getElementById('location').addEventListener('input', function(e) {
            updateContactInfo();
        });

        document.getElementById('summary').addEventListener('input', function(e) {
            document.getElementById('previewSummary').textContent = e.target.value || 'Experienced AI engineer with 5+ years specializing in machine learning and deep learning applications. Skilled in developing AI solutions for various industries including healthcare, finance, and e-commerce.';
        });

        function updateContactInfo() {
            const email = document.getElementById('email').value || 'jane@example.com';
            const phone = document.getElementById('phone').value || '(555) 123-4567';
            const location = document.getElementById('location').value || 'San Francisco, CA';
            
            document.getElementById('previewContact').textContent = `${email} • ${phone} • ${location}`;
        }

        // You would add more JavaScript to handle all form fields and update the preview accordingly
        // This is a simplified version for demonstration purposes
    </script>
</body>
</html>
