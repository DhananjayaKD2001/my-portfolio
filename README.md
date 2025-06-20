<!DOCTYPE html>
<html lang="en">

	
 
 
 
 
 
 <head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Kavindu Dhananjaya | ICT Portfolio</title>
    <style>
        /* ============================================
           BASIC RESET & GLOBAL STYLES
           ============================================ */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #0f2027 0%, #203a43 50%, #2c5364 100%); /* Professional dark gradient */
            color: white;
            min-height: 100vh;
            line-height: 1.6;
        }

        /* ============================================
           CONTAINER & LAYOUT
           ============================================ */
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }

        /* ============================================
           HEADER SECTION STYLES
           ============================================ */
        header {
            text-align: center;
            padding: 60px 0;
            background: rgba(255, 255, 255, 0.1); /* Semi-transparent white background */
            backdrop-filter: blur(15px); /* Glass effect */
            border-radius: 25px;
            margin-bottom: 40px;
            box-shadow: 0 15px 35px rgba(0, 0, 0, 0.2); /* Drop shadow */
            border: 1px solid rgba(255, 255, 255, 0.1); /* Subtle border */
        }

        /* Profile Image Circle */
        .profile-img {
            width: 200px;
            height: 200px;
            border-radius: 50%; /* Makes it circular */
            margin: 0 auto 25px;
            position: relative;
            overflow: hidden;
            border: 4px solid rgba(255, 255, 255, 0.3);
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
        }

        .profile-img img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            object-position: center;
            transition: transform 0.3s ease;
        }

        .profile-img:hover img {
            transform: scale(1.05);
        }

        /* Shine animation effect for profile image */
        .profile-img::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: linear-gradient(45deg, transparent, rgba(255,255,255,0.2), transparent);
            transform: rotate(45deg);
            animation: shine 4s infinite; /* Repeating shine effect */
        }

        /* Keyframe animation for shine effect */
        @keyframes shine {
            0% { transform: translateX(-100%) translateY(-100%) rotate(45deg); }
            50% { transform: translateX(100%) translateY(100%) rotate(45deg); }
            100% { transform: translateX(-100%) translateY(-100%) rotate(45deg); }
        }

        /* Main heading styles */
        h1 {
            font-size: 3.5em;
            margin-bottom: 10px;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3);
            background: linear-gradient(45deg, #fff, #f0f8ff); /* Gradient text */
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        /* Subtitle under name */
        .subtitle {
            font-size: 1.4em;
            opacity: 0.9;
            margin-bottom: 20px;
            color: #ffd700; /* Gold color */
        }

        /* University information */
        .university {
            font-size: 1.1em;
            opacity: 0.8;
            margin-bottom: 25px;
        }

        /* ============================================
           CONTACT INFORMATION SECTION
           ============================================ */
        .contact-info {
            display: flex;
            justify-content: center;
            gap: 30px;
            margin-top: 25px;
            flex-wrap: wrap; /* Wraps on smaller screens */
        }

        .contact-item {
            color: white;
            text-decoration: none;
            padding: 12px 24px;
            background: rgba(255, 255, 255, 0.15); /* Semi-transparent background */
            border-radius: 25px;
            transition: all 0.3s ease; /* Smooth hover transition */
            border: 1px solid rgba(255, 255, 255, 0.2);
        }

        /* Hover effects for contact items */
        .contact-item:hover {
            background: rgba(255, 255, 255, 0.25);
            transform: translateY(-3px); /* Lifts up on hover */
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
        }

        /* ============================================
           MAIN CONTENT SECTIONS
           ============================================ */
        .section {
            background: rgba(255, 255, 255, 0.1); /* Glass-morphism effect */
            backdrop-filter: blur(15px);
            border-radius: 25px;
            padding: 45px;
            margin-bottom: 35px;
            box-shadow: 0 15px 35px rgba(0, 0, 0, 0.2);
            border: 1px solid rgba(255, 255, 255, 0.1);
        }

        /* Section headings */
        .section h2 {
            font-size: 2.5em;
            margin-bottom: 25px;
            text-align: center;
            color: #ffd700; /* Gold color for headings */
            text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.3);
        }

        /* About section text */
        .about-text {
            font-size: 1.1em;
            text-align: center;
            max-width: 800px;
            margin: 0 auto;
            opacity: 0.95;
        }

        /* ============================================
           SKILLS SECTION
           ============================================ */
        .skills-container {
            display: grid;
            grid-template-columns: 1fr 1fr; /* Two equal columns */
            gap: 40px;
            margin-top: 30px;
        }

        .skills-category h3 {
            color: #ffd700;
            font-size: 1.5em;
            margin-bottom: 20px;
            text-align: center;
        }

        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr)); /* Responsive grid */
            gap: 20px;
        }

        /* Individual skill cards */
        .skill-card {
            background: rgba(255, 255, 255, 0.1);
            padding: 25px;
            border-radius: 15px;
            text-align: center;
            transition: all 0.3s ease;
            border: 1px solid rgba(255, 255, 255, 0.1);
        }

        /* Hover effects for skill cards */
        .skill-card:hover {
            transform: translateY(-5px); /* Lifts card on hover */
            background: rgba(255, 255, 255, 0.15);
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.2);
        }

        .skill-icon {
            font-size: 2.5em;
            margin-bottom: 15px;
        }

        /* ============================================
           PROJECTS SECTION
           ============================================ */
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr)); /* Responsive project cards */
            gap: 25px;
            margin-top: 30px;
        }

        /* Individual project cards */
        .project-card {
            background: rgba(255, 255, 255, 0.1);
            padding: 30px;
            border-radius: 20px;
            transition: all 0.3s ease;
            border: 1px solid rgba(255, 255, 255, 0.1);
        }

        /* Hover effects for project cards */
        .project-card:hover {
            transform: translateY(-8px);
            background: rgba(255, 255, 255, 0.15);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.2);
        }

        .project-card h3 {
            color: #ffd700;
            margin-bottom: 15px;
            font-size: 1.3em;
        }

        .project-card p {
            opacity: 0.9;
            line-height: 1.6;
        }

        /* Technology tags in projects */
        .tech-tags {
            margin-top: 15px;
            display: flex;
            flex-wrap: wrap;
            gap: 8px;
        }

       .tech-tag {
            background: rgba(255, 215, 0, 0.2); /* Gold background */
            color: #ffd700;
            padding: 5px 12px;
            border-radius: 15px;
            font-size: 0.9em;
            border: 1px solid rgba(255, 215, 0, 0.3);
        }

        /* ============================================
           EDUCATION SECTION
           ============================================ */
        .education-item {
            background: rgba(255, 255, 255, 0.1);
            padding: 25px;
            border-radius: 15px;
            margin-bottom: 20px;
            border-left: 4px solid #ffd700; /* Gold accent line */
        }

        .education-item h3 {
            color: #ffd700;
            margin-bottom: 10px;
        }

        .education-item .year {
            color: #4ecdc4;
            font-weight: bold;
            margin-bottom: 5px;
        }

        /* ============================================
           FOOTER SECTION
           ============================================ */
        footer {
            text-align: center;
            padding: 40px 0;
            margin-top: 50px;
            border-top: 1px solid rgba(255, 255, 255, 0.2);
            opacity: 0.8;
        }

        /* ============================================
           PROFESSIONAL ENHANCEMENTS
           ============================================ */
        
        /* Download CV Button */
        .download-cv {
            background: linear-gradient(45deg, #ff6b6b, #4ecdc4);
            color: white;
            padding: 15px 30px;
            border: none;
            border-radius: 25px;
            font-size: 1.1em;
            font-weight: bold;
            cursor: pointer;
            transition: all 0.3s ease;
            text-decoration: none;
            display: inline-block;
            margin-top: 20px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
        }

        .download-cv:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 25px rgba(0, 0, 0, 0.3);
        }

        /* Professional badges */
        .professional-badge {
            background: rgba(255, 215, 0, 0.1);
            border: 2px solid #ffd700;
            color: #ffd700;
            padding: 8px 16px;
            border-radius: 20px;
            font-size: 0.9em;
            margin: 5px;
            display: inline-block;
        }

        /* Status indicator */
        .status-indicator {
            display: inline-block;
            width: 12px;
            height: 12px;
            background: #4ecdc4;
            border-radius: 50%;
            margin-right: 8px;
            animation: pulse 2s infinite;
        }

        @keyframes pulse {
            0% { opacity: 1; }
            50% { opacity: 0.5; }
            100% { opacity: 1; }
        }
        @media (max-width: 768px) {
            /* Mobile adjustments */
            h1 {
                font-size: 2.5em;
            }
            
            .container {
                padding: 15px;
            }
            
            .section {
                padding: 25px;
            }

            /* Stack skills columns on mobile */
            .skills-container {
                grid-template-columns: 1fr;
                gap: 30px;
            }

            /* Adjust contact info for mobile */
            .contact-info {
                flex-direction: column;
                align-items: center;
                gap: 15px;
            }

            /* Smaller project cards on mobile */
            .projects-grid {
                grid-template-columns: 1fr;
            }
        }

        @media (max-width: 480px) {
            /* Extra small screens */
            .profile-img {
                width: 120px;
                height: 120px;
                font-size: 50px;
            }

            h1 {
                font-size: 2em;
            }

            .section h2 {
                font-size: 2em;
            }
        }
	/* ============================================
  	      IMAGE POPUP/MODAL STYLES
   	      ============================================ */
		.image-modal {
    		display: none;
    		position: fixed;
    		z-index: 9999;
    		left: 0;
    		top: 0;
    		width: 100%;
    		height: 100%;
    		background-color: rgba(0, 0, 0, 0.9);
    		backdrop-filter: blur(5px);
	}

	.modal-content {
    		position: relative;
    		margin: auto;
    		padding: 20px;
    		width: 90%;
    		height: 100%;
    		display: flex;
    		align-items: center;
    		justify-content: center;
	}

	.modal-image {
    		max-width: 90%;
   		max-height: 90%;
    		border-radius: 15px;
    		box-shadow: 0 20px 60px rgba(0, 0, 0, 0.5);
    		transition: transform 0.3s ease;
	}

	.close-modal {
    		position: absolute;
    		top: 30px;
    		right: 50px;
    		color: white;
    		font-size: 40px;
    		font-weight: bold;
    		cursor: pointer;
    		z-index: 10000;
    		background: rgba(0, 0, 0, 0.5);
    		width: 50px;
    		height: 50px;
    		border-radius: 50%;
    		display: flex;
    		align-items: center;
    		justify-content: center;
    		transition: all 0.3s ease;
	}

	.close-modal:hover {
    		background: rgba(255, 0, 0, 0.7);
    		transform: scale(1.1);
	}

	/* Zoom effect on modal image */
	.modal-image:hover {
    		transform: scale(1.02);
	}

	/* Animation for modal */
	.image-modal.show {
    		display: flex;
    		animation: fadeIn 0.3s ease;
	}

	@keyframes fadeIn {
    		from { opacity: 0; }
    		to { opacity: 1; }
	}

	/* Mobile responsive */
	@media (max-width: 768px) {
    		.close-modal {
        		top: 20px;
        		right: 20px;
        		font-size: 30px;
        		width: 40px;
        		height: 40px;
    		}
    
    		.modal-image {
       			max-width: 95%;
        		max-height: 80%;
    		}
	}
    </style>
</head>
<body>
    <!-- ============================================
         MAIN CONTAINER
         ============================================ -->
    <div class="container">
        
        <!-- ============================================
             HEADER SECTION - Name, Title, Contact
             ============================================ -->
        <header>
            <!-- Profile Image with popup functionality -->
		<div class="profile-img">
    			<img src="images/profile.jpeg" 
         		alt="Kavindu Dhananjaya Profile Photo" 
         		id="profilePhoto"
         		onclick="openImageModal(this)"
         		style="cursor: pointer;"
         		title="Click to view full image">
		</div>
	    <!-- Image Modal/Popup -->
		<div id="imageModal" class="image-modal" onclick="closeImageModal()">
    			<div class="modal-content">
        		<span class="close-modal" onclick="closeImageModal()">&times;</span>
        		<img id="modalImage" class="modal-image" src="" alt="Profile Photo">
    			</div>
		</div>
            
            <!-- Main heading with name -->
            <h1>Kavindu Dhananjaya</h1>
            
            <!-- Job title/specialization with status -->
            <p class="subtitle">
                <span class="status-indicator"></span>
                ICT Undergraduate | Network Technology Specialist
            </p>
            
            <!-- University information -->
            <p class="university">University of Sri Jayewardenepura</p>
            
            <!-- Professional badges -->
            <div style="margin: 20px 0;">
                <span class="professional-badge">Available for Internships</span>
                <span class="professional-badge">Network Specialist</span>
                <span class="professional-badge">IoT Developer</span>
            </div>
            
            <!-- Download CV button -->
            <a href="C:\Users\Kavindu Bosa\Desktop\Portfolio\CV/Kavindu Dhananjaya.pdf" class="download-cv" download="Kavindu Dhananjaya.pdf" target="_blank">
                📄 Download CV
            </a>
            
            <!-- Contact information buttons -->
            <div class="contact-info">
                <a href="tel:+94728250339" class="contact-item">📞 +94 72 825 0339</a>
                <a href="mailto:dhananjayakd1@gmail.com" class="contact-item">📧 Email Me</a>
                <a href="https://linkedin.com/in/kavindu-dhananjaya" class="contact-item" target="_blank">💼 LinkedIn</a>
                <a href="https://github.com/kavindudhananjaya" class="contact-item" target="_blank">💻 GitHub</a>
            </div>
        </header>

        <!-- ============================================
             ABOUT/PROFILE SECTION
             ============================================ -->
        <section class="section">
            <h2>Profile</h2>
            <p class="about-text">
                Dedicated ICT undergraduate specializing in networking, with a strong foundation in network protocols, 
                security, and system administration. Passionate about creating innovative solutions that bridge the gap 
                between technology and real-world applications. Seeking opportunities to apply and expand my networking 
                expertise in a professional environment while contributing to cutting-edge projects.
            </p>
        </section>

        <!-- ============================================
             SKILLS SECTION - Hard & Soft Skills
             ============================================ -->
        <section class="section">
            <h2>Skills & Expertise</h2>
            <div class="skills-container">
                
                <!-- Technical/Hard Skills Column -->
                <div class="skills-category">
                    <h3>Technical Skills</h3>
                    <div class="skills-grid">
                        <div class="skill-card">
                            <div class="skill-icon">🌐</div>
                            <h4>Network Configuration</h4>
                            <p>Router & Switch Setup</p>
                        </div>
                        <div class="skill-card">
                            <div class="skill-icon">🔧</div>
                            <h4>Network Design</h4>
                            <p>Planning & Implementation</p>
                        </div>
                        <div class="skill-card">
                            <div class="skill-icon">💻</div>
                            <h4>Object Oriented Programming</h4>
                            <p>Software Development</p>
                        </div>
                        <div class="skill-card">
                            <div class="skill-icon">🏠</div>
                            <h4>IoT & Smart Systems</h4>
                            <p>Home Automation</p>
                        </div>
                    </div>
                </div>

                <!-- Soft Skills Column -->
                <div class="skills-category">
                    <h3>Professional Skills</h3>
                    <div class="skills-grid">
                        <div class="skill-card">
                            <div class="skill-icon">⏰</div>
                            <h4>Time Management</h4>
                            <p>Efficient Task Planning</p>
                        </div>
                        <div class="skill-card">
                            <div class="skill-icon">👥</div>
                            <h4>Leadership</h4>
                            <p>Team Coordination</p>
                        </div>
                        <div class="skill-card">
                            <div class="skill-icon">🧩</div>
                            <h4>Problem Solving</h4>
                            <p>Analytical Thinking</p>
                        </div>
                        <div class="skill-card">
                            <div class="skill-icon">🎯</div>
                            <h4>Critical Thinking</h4>
                            <p>Strategic Analysis</p>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- ============================================
             PROJECTS SECTION
             ============================================ -->
        <section class="section">
            <h2>Featured Projects</h2>
            <div class="projects-grid">
                
                <!-- Project 1: Traffic Sign Recognition -->
                <div class="project-card">
                    <h3>🚦 Traffic Sign Recognition System</h3>
                    <p>
                        Developed an Arduino-based Traffic Sign Recognition System with advanced computer vision capabilities. 
                        The system uses machine learning to recognize traffic signs, adjust vehicle speed automatically, 
                        and provide voice instructions to drivers for enhanced road safety.
                    </p>
                    <div class="tech-tags">
                        <span class="tech-tag">Arduino</span>
                        <span class="tech-tag">OpenCV</span>
                        <span class="tech-tag">TensorFlow</span>
                        <span class="tech-tag">CNN</span>
                        <span class="tech-tag">Google Speech API</span>
                    </div>
                </div>

                <!-- Project 2: Reservation System -->
                <div class="project-card">
                    <h3>📅 Lecture Halls & Labs Reservation System</h3>
                    <p>
                        Created an automated reservation platform that streamlines facility booking for educational institutions. 
                        Lecturers can reserve facilities while students can view availability in real-time. Features include 
                        conflict detection, automated notifications, and comprehensive reporting.
                    </p>
                    <div class="tech-tags">
                        <span class="tech-tag">React</span>
                        <span class="tech-tag">MongoDB</span>
                        <span class="tech-tag">Express.js</span>
                        <span class="tech-tag">Node.js</span>
                    </div>
                </div>

                <!-- Project 3: Smart Home Automation -->
                <div class="project-card">
                    <h3>🏠 Smart Home Automation System</h3>
                    <p>
                        Designed and implemented a comprehensive smart home automation system using Cisco Packet Tracer. 
                        The project demonstrates practical networking and IoT integration skills with secure automation, 
                        real-time monitoring, and automated response systems for modern smart homes.
                    </p>
                    <div class="tech-tags">
                        <span class="tech-tag">Cisco Packet Tracer</span>
                        <span class="tech-tag">IoT</span>
                        <span class="tech-tag">Network Security</span>
                        <span class="tech-tag">Automation</span>
                    </div>
                </div>
            </div>
        </section>

        <!-- ============================================
             EDUCATION SECTION
             ============================================ -->
        <section class="section">
            <h2>Education</h2>
            
            <!-- Current University Education -->
            <div class="education-item">
                <div class="year">2022 - Present</div>
                <h3>Bachelor of Information and Communication Technology (Hons)</h3>
                <p><strong>University of Sri Jayewardenepura</strong></p>
                <p>Specialized in Network Technology</p>
                <p>Focus areas: Network protocols, security, system administration, and IoT integration</p>
            </div>

            <!-- Previous School Education -->
            <div class="education-item">
                <div class="year">2017 - 2020</div>
                <h3>Advanced Level Education</h3>
                <p><strong>Bandaranayake College, Gampaha</strong></p>
                <p>Passed with B3 grades in ICT, Engineering Technology, and Science for Technology</p>
            </div>
        </section>

        <!-- ============================================
             FOOTER SECTION
             ============================================ -->
        <footer>
            <p>&copy; 2024 Kavindu Dhananjaya. Built with passion for technology and innovation </p>
            <p>Specialized in Network Technology | University of Sri Jayewardenepura</p>
            <p>Version: 2.0.0 | Last Updated: June 2024</p>
        </footer>
    </div>

    <!-- ============================================
         JAVASCRIPT - Interactive Features
         ============================================ -->
    <script>
        // Wait for the page to fully load before running scripts
        document.addEventListener('DOMContentLoaded', function() {
            
            // ============================================
            // SMOOTH SCROLLING FOR INTERNAL LINKS
            // ============================================
            const links = document.querySelectorAll('a[href^="#"]');
            links.forEach(link => {
                link.addEventListener('click', function(e) {
                    e.preventDefault(); // Prevent default jump behavior
                    const target = document.querySelector(this.getAttribute('href'));
                    if (target) {
                        // Smooth scroll to target element
                        target.scrollIntoView({ behavior: 'smooth' });
                    }
                });
            });

            // ============================================
            // TYPING ANIMATION FOR MAIN TITLE
            // ============================================
            const title = document.querySelector('h1');
            const originalText = title.textContent;
            title.textContent = ''; // Clear the text initially
            
            let i = 0;
            const typeWriter = () => {
                if (i < originalText.length) {
                    title.textContent += originalText.charAt(i); // Add one character
                    i++;
                    setTimeout(typeWriter, 100); // Delay between characters
                }
            };
            
            // Start typing animation after 500ms delay
            setTimeout(typeWriter, 500);

            // ============================================
            // STAGGERED ANIMATION FOR SKILL CARDS
            // ============================================
            const skillCards = document.querySelectorAll('.skill-card');
            skillCards.forEach((card, index) => {
                // Delay each card's animation based on its position
                card.style.animationDelay = `${index * 0.2}s`;
                
                // Add a subtle entrance animation
                card.style.opacity = '0';
                card.style.transform = 'translateY(20px)';
                
                setTimeout(() => {
                    card.style.transition = 'all 0.6s ease';
                    card.style.opacity = '1';
                    card.style.transform = 'translateY(0)';
                }, index * 200);
            });

            // ============================================
            // PROFILE IMAGE UPLOAD FUNCTIONALITY
            // ============================================
            
            // Function to handle profile image upload
            function handleImageUpload() {
                const input = document.createElement('input');
                input.type = 'file';
                input.accept = 'image/*';
                
                input.onchange = function(event) {
                    const file = event.target.files[0];
                    if (file) {
                        const reader = new FileReader();
                        reader.onload = function(e) {
                            const profileImg = document.getElementById('profilePhoto');
                            profileImg.src = e.target.result;
                        };
                        reader.readAsDataURL(file);
                    }
                };
                
                input.click();
            }

            // Add click listener to profile image for upload functionality
            const profileImg = document.getElementById('profilePhoto');
            if (profileImg) {
                //profileImg.addEventListener('click', handleImageUpload);
                profileImg.style.cursor = 'pointer';
                profileImg.title = 'Click to change profile photo';
            }

            // ============================================
            // ENHANCED PROFESSIONAL INTERACTIONS
            // ============================================
            const projectCards = document.querySelectorAll('.project-card');
            projectCards.forEach(card => {
                // Add click interaction with visual feedback
                card.addEventListener('click', function() {
                    // Temporary color change on click
                    this.style.background = 'rgba(255, 255, 255, 0.2)';
                    this.style.transform = 'scale(0.98)'; // Slight shrink effect
                    
                    // Reset after short delay
                    setTimeout(() => {
                        this.style.background = 'rgba(255, 255, 255, 0.1)';
                        this.style.transform = 'translateY(-8px)'; // Return to hover state
                    }, 150);
                });

                // Add mouse enter/leave effects for better interactivity
                card.addEventListener('mouseenter', function() {
                    this.style.cursor = 'pointer';
                });
            });

            // ============================================
            // CONTACT ITEM CLICK HANDLERS
            // ============================================
            const contactItems = document.querySelectorAll('.contact-item');
            contactItems.forEach(item => {
                item.addEventListener('click', function(e) {
                    // Add a subtle click animation
                    this.style.transform = 'translateY(-3px) scale(0.95)';
                    setTimeout(() => {
                        this.style.transform = 'translateY(-3px) scale(1)';
                    }, 100);
                });
            });

            // ============================================
            // SCROLL-BASED ANIMATIONS (Optional Enhancement)
            // ============================================
            const sections = document.querySelectorAll('.section');
            
            const observerOptions = {
                threshold: 0.1, // Trigger when 10% of element is visible
                rootMargin: '0px 0px -50px 0px'
            };

            // Observer to add animations when sections come into view
            const sectionObserver = new IntersectionObserver(function(entries) {
                entries.forEach(entry => {
                    if (entry.isIntersecting) {
                        entry.target.style.opacity = '1';
                        entry.target.style.transform = 'translateY(0)';
                    }
                });
            }, observerOptions);

            // Initially hide sections for scroll animation
            sections.forEach(section => {
                section.style.opacity = '0';
                section.style.transform = 'translateY(30px)';
                section.style.transition = 'all 0.6s ease';
                sectionObserver.observe(section); // Start observing each section
            });

            // ============================================
            // CONSOLE LOG FOR DEVELOPERS
            // ============================================
            console.log('🌐 Kavindu Dhananjaya Portfolio Loaded Successfully!');
            console.log('📧 Contact: dhananjayakd1@gmail.com');
            console.log('🎓 University of Sri Jayewardenepura - ICT');
        });

        // ============================================
        // UTILITY FUNCTIONS
        // ============================================
        
        // ============================================
        // PROFESSIONAL FUNCTIONS
        // ============================================
        
        // Function to download CV (you can link to actual CV file)
        function downloadCV() {
            // For now, this will show an alert. Replace with actual CV download link
            alert('CV download will be available soon! \nContact: dhananjayakd1@gmail.com');
            
            // Uncomment below line when you have actual CV file
            // window.open('path/to/your/cv.pdf', '_blank');
        }

        // Function to copy email to clipboard (can be used with email button)
        function copyEmail() {
            const email = 'dhananjayakd1@gmail.com';
            navigator.clipboard.writeText(email).then(function() {
                alert('Email copied to clipboard: ' + email);
            }).catch(function(err) {
                console.error('Could not copy email: ', err);
            });
        }

        // Function to show a welcome message (can be called on page load)
        function showWelcome() {
            setTimeout(() => {
                console.log('Welcome to Kavindu Dhananjaya\'s Portfolio! 🚀');
            }, 2000);
        }

        // Call welcome function
        showWelcome();

	// ============================================
	// IMAGE POPUP/MODAL FUNCTIONALITY
	// ============================================

	// Function to open image in modal
		function openImageModal(imageElement) {
    		const modal = document.getElementById('imageModal');
    		const modalImage = document.getElementById('modalImage');
    
    	// Set the modal image source to clicked image
    		modalImage.src = imageElement.src;
    		modalImage.alt = imageElement.alt;
    
    	// Show the modal
   		modal.classList.add('show');
    		modal.style.display = 'flex';
    
    	// Prevent body scrolling when modal is open
    		document.body.style.overflow = 'hidden';
	}

	// Function to close image modal
		function closeImageModal() {
    		const modal = document.getElementById('imageModal');
    
    	// Hide the modal
    		modal.classList.remove('show');
    		modal.style.display = 'none';
    
    	// Restore body scrolling
    		document.body.style.overflow = 'auto';
	}

	// Close modal when pressing Escape key
		document.addEventListener('keydown', function(event) {
    		if (event.key === 'Escape') {
        	closeImageModal();
    	}
	});

	// Prevent modal from closing when clicking on the image itself
		document.getElementById('modalImage').addEventListener('click', function(event) {
    		event.stopPropagation();
		});
    </script>
</body>
</html>
