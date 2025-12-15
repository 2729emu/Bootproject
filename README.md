# Bootproject
Project
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Personal Profile - Eman Tofik</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background-color: #f5f7fa;
            color: #333;
            line-height: 1.6;
            padding: 20px;
            max-width: 1200px;
            margin: 0 auto;
        }
        
        header {
            text-align: center;
            padding: 30px 0;
            background: linear-gradient(135deg, #4b6cb7 0%, #182848 100%);
            color: white;
            border-radius: 10px;
            margin-bottom: 30px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }
        
        h1 {
            font-size: 2.8rem;
            margin-bottom: 10px;
            letter-spacing: 1px;
        }
        
        .subtitle {
            font-size: 1.2rem;
            opacity: 0.9;
            font-weight: 300;
        }
        
        .container {
            display: flex;
            flex-wrap: wrap;
            gap: 30px;
            margin-bottom: 30px;
        }
        
        .bio-section {
            flex: 1;
            min-width: 300px;
            background-color: white;
            padding: 25px;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
        }
        
        .image-section {
            flex: 1;
            min-width: 300px;
            display: flex;
            flex-direction: column;
            align-items: center;
            background-color: white;
            padding: 25px;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
        }
        
        h2 {
            color: #182848;
            margin-bottom: 20px;
            padding-bottom: 10px;
            border-bottom: 2px solid #4b6cb7;
        }
        
        .profile-img-container {
            position: relative;
            width: 280px;
            height: 280px;
            margin-bottom: 20px;
        }
        
        .profile-img {
            width: 100%;
            height: 100%;
            border-radius: 50%;
            object-fit: cover;
            border: 5px solid #4b6cb7;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }
        
        .profile-img-placeholder {
            width: 100%;
            height: 100%;
            border-radius: 50%;
            border: 5px solid #4b6cb7;
            background: linear-gradient(135deg, #e0e7ff 0%, #c7d2fe 100%);
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            color: #4b6cb7;
            font-weight: 600;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }
        
        .profile-img-placeholder i {
            font-size: 4rem;
            margin-bottom: 15px;
        }
        
        .interests {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            margin-top: 20px;
        }
        
        .interest-tag {
            background-color: #eef2ff;
            padding: 8px 15px;
            border-radius: 20px;
            font-size: 0.9rem;
            color: #4b6cb7;
        }
        
        .form-section {
            background-color: white;
            padding: 30px;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            margin-bottom: 30px;
        }
        
        .form-row {
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
            margin-bottom: 20px;
        }
        
        .form-group {
            flex: 1;
            min-width: 250px;
        }
        
        label {
            display: block;
            margin-bottom: 8px;
            font-weight: 600;
            color: #182848;
        }
        
        input, textarea {
            width: 100%;
            padding: 12px 15px;
            border: 1px solid #ddd;
            border-radius: 5px;
            font-size: 1rem;
            transition: border 0.3s;
        }
        
        input:focus, textarea:focus {
            outline: none;
            border-color: #4b6cb7;
            box-shadow: 0 0 0 2px rgba(75, 108, 183, 0.2);
        }
        
        textarea {
            min-height: 150px;
            resize: vertical;
        }
        
        .submit-btn {
            background: linear-gradient(135deg, #4b6cb7 0%, #182848 100%);
            color: white;
            border: none;
            padding: 14px 30px;
            font-size: 1.1rem;
            border-radius: 5px;
            cursor: pointer;
            transition: transform 0.3s, box-shadow 0.3s;
            font-weight: 600;
            letter-spacing: 1px;
        }
        
        .submit-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 7px 15px rgba(0, 0, 0, 0.1);
        }
        
        .submit-btn:active {
            transform: translateY(0);
        }
        
        footer {
            text-align: center;
            padding: 20px;
            color: #666;
            font-size: 0.9rem;
            border-top: 1px solid #eee;
            margin-top: 20px;
        }
        
        .social-links {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 20px;
        }
        
        .social-icon {
            color: #4b6cb7;
            font-size: 1.5rem;
            transition: transform 0.3s;
        }
        
        .social-icon:hover {
            transform: translateY(-5px);
        }
        
        .message-success {
            display: none;
            background-color: #d4edda;
            color: #155724;
            padding: 15px;
            border-radius: 5px;
            margin-top: 20px;
            border: 1px solid #c3e6cb;
        }
        
        .error {
            color: #dc3545;
            font-size: 0.9rem;
            margin-top: 5px;
            display: none;
        }
        
        .upload-btn {
            margin-top: 15px;
            padding: 10px 20px;
            background-color: #eef2ff;
            color: #4b6cb7;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            font-weight: 600;
            transition: background-color 0.3s;
        }
        
        .upload-btn:hover {
            background-color: #dbe4ff;
        }
        
        .highlight {
            color: #4b6cb7;
            font-weight: 600;
        }
        
        .made-in-canada {
            font-size: 0.8rem;
            color: #666;
            margin-top: 5px;
            font-style: italic;
        }
        
        @media (max-width: 768px) {
            .container {
                flex-direction: column;
            }
            
            h1 {
                font-size: 2.2rem;
            }
            
            .profile-img-container {
                width: 220px;
                height: 220px;
            }
        }
    </style>
</head>
<body>
    <header>
        <h1>Eman Tofik</h1>
        <p class="subtitle">Engineering Student & Future Leader</p>
    </header>
    
    <div class="container">
        <section class="bio-section">
            <h2>About Me</h2>
            <p>My name is <span class="highlight">Eman Tofik</span>. I am an <span class="highlight">18-year-old student</span> currently pursuing my education in engineering. I'm in my <span class="highlight">second year</span> at the School of Engineering, where I'm developing my technical skills and knowledge to prepare for a future in technology and innovation.</p>
            
            <p>My ultimate goal is to become a <span class="highlight">great leader</span> who can develop innovative solutions and make a positive impact in the world. I believe that with dedication, creativity, and the right technical skills, I can contribute to building technologies that solve real-world problems.</p>
            
            <p>As an engineering student, I'm passionate about learning how things work and finding ways to improve them. I'm particularly interested in how technology can be used to create positive change and help people in their daily lives.</p>
            
            <div class="interests">
                <div class="interest-tag">Engineering</div>
                <div class="interest-tag">Leadership</div>
                <div class="interest-tag">Technology</div>
                <div class="interest-tag">Innovation</div>
                <div class="interest-tag">Problem Solving</div>
                <div class="interest-tag">Development</div>
            </div>
        </section>
        
        <section class="image-section">
            <h2>Profile Photo</h2>
            <div class="profile-img-container">
                <!-- Your Profile Image -->
                <img src="data:image/jpeg;base64,/9j/4AAQSkZJRgABAQAAAQABAAD/2wBDAAYEBQYFBAYGBQYHBwYIChAKCgkJChQODwwQFxQYGBcUFhYaHSUfGhsjHBYWICwgIyYnKSopGR8tMC0oMCUoKSj/2wBDAQcHBwoIChMKChMoGhYaKCgoKCgoKCgoKCgoKCgoKCgoKCgoKCgoKCgoKCgoKCgoKCgoKCgoKCgoKCgoKCgoKCj/wAARCAHgAeADASIAAhEBAxEB/8QAFQABAQAAAAAAAAAAAAAAAAAAAAv/xAAUEAEAAAAAAAAAAAAAAAAAAAAA/8QAFQEBAQAAAAAAAAAAAAAAAAAAAAX/xAAUEQEAAAAAAAAAAAAAAAAAAAAA/9oADAMBAAIRAxEAPwCdAAUv/9k=" alt="Eman Tofik" class="profile-img" id="profileImage">
                <div class="made-in-canada">Made in Canada</div>
            </div>
            
            <button class="upload-btn" id="uploadBtn">
                <i class="fas fa-sync-alt"></i> Change Profile Picture
            </button>
            
            <p style="margin-top: 15px; text-align: center;">This is my profile picture. I'm an engineering student aspiring to become a great leader in technology development.</p>
        </section>
    </div>
    
    <section class="form-section">
        <h2>Get In Touch</h2>
        <p>I'm always interested in connecting with fellow students, mentors, and professionals in the engineering and technology fields. Whether you want to collaborate on projects, share knowledge, or discuss future opportunities, feel free to reach out!</p>
        
        <form id="contactForm">
            <div class="form-row">
                <div class="form-group">
                    <label for="name">Your Name *</label>
                    <input type="text" id="name" name="name" placeholder="Enter your name" required>
                    <div class="error" id="nameError">Please enter your name</div>
                </div>
                <div class="form-group">
                    <label for="email">Your Email *</label>
                    <input type="email" id="email" name="email" placeholder="Enter your email" required>
                    <div class="error" id="emailError">Please enter a valid email address</div>
                </div>
            </div>
            
            <div class="form-group">
                <label for="message">Your Message *</label>
                <textarea id="message" name="message" placeholder="What would you like to discuss?" required></textarea>
                <div class="error" id="messageError">Please enter your message</div>
            </div>
            
            <button type="submit" class="submit-btn">
                <i class="fas fa-paper-plane"></i> Send Message
            </button>
            
            <div class="message-success" id="successMessage">
                <i class="fas fa-check-circle"></i> Thank you for your message! I'll get back to you soon.
            </div>
        </form>
    </section>
    
    <footer>
        <p>© 2023 Eman Tofik. All rights reserved.</p>
        <p>This personal profile page was created as part of an HTML learning project.</p>
        
        <div class="social-links">
            <a href="#" class="social-icon"><i class="fab fa-github"></i></a>
            <a href="#" class="social-icon"><i class="fab fa-linkedin"></i></a>
            <a href="#" class="social-icon"><i class="fab fa-twitter"></i></a>
            <a href="#" class="social-icon"><i class="fas fa-graduation-cap"></i></a>
        </div>
    </footer>
    
    <script>
        // Contact Form Handling
        document.getElementById('contactForm').addEventListener('submit', function(event) {
            event.preventDefault();
            
            // Reset previous errors and success message
            document.getElementById('nameError').style.display = 'none';
            document.getElementById('emailError').style.display = 'none';
            document.getElementById('messageError').style.display = 'none';
            document.getElementById('successMessage').style.display = 'none';
            
            // Get form values
            const name = document.getElementById('name').value.trim();
            const email = document.getElementById('email').value.trim();
            const message = document.getElementById('message').value.trim();
            
            let isValid = true;
            
            // Validate name
            if (name === '') {
                document.getElementById('nameError').style.display = 'block';
                isValid = false;
            }
            
            // Validate email
            const emailPattern = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
            if (!emailPattern.test(email)) {
                document.getElementById('emailError').style.display = 'block';
                isValid = false;
            }
            
            // Validate message
            if (message === '') {
                document.getElementById('messageError').style.display = 'block';
                isValid = false;
            }
            
            // If form is valid, show success message and reset form
            if (isValid) {
                document.getElementById('successMessage').style.display = 'block';
                document.getElementById('contactForm').reset();
                
                // Scroll to success message
                document.getElementById('successMessage').scrollIntoView({ 
                    behavior: 'smooth',
                    block: 'center'
                });
                
                // In a real application, you would send the form data to a server here
                console.log('Form submitted with:', { name, email, message });
            }
        });
        
        // Add input event listeners to hide errors when user starts typing
        document.getElementById('name').addEventListener('input', function() {
            document.getElementById('nameError').style.display = 'none';
        });
        
        document.getElementById('email').addEventListener('input', function() {
            document.getElementById('emailError').style.display = 'none';
        });
        
        document.getElementById('message').addEventListener('input', function() {
            document.getElementById('messageError').style.display = 'none';
        });
        
        // Profile Picture Upload Functionality
        document.getElementById('uploadBtn').addEventListener('click', function() {
            // Create a file input element
            const fileInput = document.createElement('input');
            fileInput.type = 'file';
            fileInput.accept = 'image/*';
            
            // When a file is selected
            fileInput.addEventListener('change', function(event) {
                const file = event.target.files[0];
                if (file) {
                    // Check if it's an image file
                    if (!file.type.match('image.*')) {
                        alert('Please select an image file (JPEG, PNG, etc.)');
                        return;
                    }
                    
                    // Create a FileReader to read the image
                    const reader = new FileReader();
                    
                    reader.onload = function(e) {
                        // Display the uploaded image
                        const profileImage = document.getElementById('profileImage');
                        
                        profileImage.src = e.target.result;
                        
                        // Show success message
                        alert('Profile picture updated successfully!');
                    };
                    
                    reader.readAsDataURL(file);
                }
            });
            
            // Trigger the file input dialog
            fileInput.click();
        });
    </script>
</body>
</html>