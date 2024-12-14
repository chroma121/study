<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Study Mastery Course</title>
    <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&family=Playfair+Display:wght@400;700&display=swap" rel="stylesheet">
    <style>
        body {
            margin: 0;
            font-family: 'Roboto', sans-serif;
            color: #333;
            overflow-x: hidden;
        }
        header {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            background: rgba(255, 255, 255, 0.8);
            backdrop-filter: blur(10px);
            padding: 1rem 2rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
            z-index: 1000;
        }
        header a {
            text-decoration: none;
            color: #333;
            font-weight: bold;
            margin-left: 1rem;
        }
        section {
            min-height: 100vh;
            padding: 5rem 2rem;
            text-align: center;
        }
        #home {
            background: linear-gradient(to bottom, #e3f2fd, #90caf9);
            display: flex;
            align-items: center;
            justify-content: center;
            position: relative;
        }
        #home h1 {
            font-family: 'Playfair Display', serif;
            font-size: 3rem;
            color: #0d47a1;
        }
        .animated-image {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%) scale(1);
            transition: transform 0.5s ease;
        }
        #home:hover .animated-image {
            transform: translate(-50%, -50%) scale(1.1);
        }
        #about, #services, #introduction {
            background: #f5f5f5;
        }
        .btn {
            padding: 1rem 2rem;
            background: #0d47a1;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            font-size: 1rem;
            transition: background 0.3s ease;
        }
        .btn:hover {
            background: #1565c0;
        }
        footer {
            padding: 1rem;
            text-align: center;
            background: #333;
            color: white;
        }
        .scrolling-effect {
            animation: scrollEffect 6s infinite alternate;
        }
        @keyframes scrollEffect {
            0% { transform: translateY(0); }
            100% { transform: translateY(-20px); }
        }
    </style>
</head>
<body>
    <header>
        <div>Study Mastery</div>
        <nav>
            <a href="#home">Home</a>
            <a href="#about">About</a>
            <a href="#services">Services</a>
            <a href="#introduction">Introduction</a>
        </nav>
    </header>

    <section id="home">
        <h1>Master the Art of Studying</h1>
        <img src="study-image.jpg" alt="Studying" class="animated-image scrolling-effect" width="300">
    </section>

    <section id="about">
        <h2>About Us</h2>
        <p>We provide proven methods to enhance your study techniques and achieve academic success.</p>
    </section>

    <section id="services">
        <h2>Our Services</h2>
        <p>Learn through expertly crafted online courses, personalized coaching, and interactive resources.</p>
        <button class="btn">Explore Courses</button>
    </section>

    <section id="introduction">
        <h2>Course Introduction</h2>
        <p>Get a sneak peek into the course content and see how it can transform your learning experience.</p>
        <button class="btn">Start Now</button>
    </section>

    <footer>
        &copy; 2024 Study Mastery | All Rights Reserved
    </footer>

    <script>
        // Smooth scrolling for navigation links
        document.querySelectorAll('header a').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                e.preventDefault();
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });

        // Parallax effect for the animated image on scroll
        window.addEventListener('scroll', () => {
            const animatedImage = document.querySelector('.animated-image');
            const scrollY = window.scrollY;
            animatedImage.style.transform = `translate(-50%, calc(-50% + ${scrollY * 0.3}px)) scale(1.1)`;
        });

        // Button interactivity
        document.querySelectorAll('.btn').forEach(button => {
            button.addEventListener('click', () => {
                alert('This feature is coming soon!');
            });
        });
    </script>
</body>
</html>
