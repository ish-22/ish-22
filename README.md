<!DOCTYPE html>
<html lang="en" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ishan Chinthaka - Portfolio</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        primary: '#1F2937',
                        accent: '#10B981',
                    }
                }
            },
            darkMode: 'class',
        }
    </script>
    <style>
        /* Parallax effect */
        .parallax {
            background-attachment: fixed;
            background-position: center;
            background-repeat: no-repeat;
            background-size: cover;
        }
        /* Skill bar animation */
        @keyframes fill {
            from { width: 0; }
            to { width: var(--progress); }
        }
        .skill-bar {
            animation: fill 2s ease-in-out forwards;
        }
    </style>
</head>
<body class="bg-gray-100 dark:bg-gray-900 text-gray-900 dark:text-gray-100 font-sans transition-colors duration-300">
    <!-- Navbar -->
    <nav class="fixed top-0 left-0 w-full bg-white dark:bg-gray-800 shadow-lg z-50">
        <div class="container mx-auto px-4 py-3 flex justify-between items-center">
            <a href="#" class="text-2xl font-bold text-primary dark:text-accent">Ishan Chinthaka</a>
            <ul class="flex space-x-6">
                <li><a href="#home" class="hover:text-accent">Home</a></li>
                <li><a href="#about" class="hover:text-accent">About</a></li>
                <li><a href="#skills" class="hover:text-accent">Skills</a></li>
                <li><a href="#projects" class="hover:text-accent">Projects</a></li>
                <li><a href="#contact" class="hover:text-accent">Contact</a></li>
            </ul>
            <button id="darkModeToggle" class="ml-4 p-2 rounded-full bg-gray-200 dark:bg-gray-700">
                <span class="sr-only">Toggle Dark Mode</span>
                🌙
            </button>
        </div>
    </nav>

    <!-- Hero Section with Parallax -->
    <section id="home" class="h-screen flex items-center justify-center parallax" style="background-image: url('https://source.unsplash.com/random/1920x1080/?tech');">
        <div class="text-center bg-black bg-opacity-50 p-10 rounded-lg">
            <h1 class="text-5xl font-bold mb-4">Web Developer & Aspiring Software Engineer</h1>
            <p class="text-xl mb-6">Passionate about building scalable systems with modern tech.</p>
            <a href="#contact" class="bg-accent text-white px-6 py-3 rounded-full hover:bg-green-600">Get in Touch</a>
        </div>
    </section>

    <!-- About Section -->
    <section id="about" class="py-20 container mx-auto px-4">
        <h2 class="text-4xl font-bold mb-8 text-center">About Me</h2>
        <div class="flex flex-col md:flex-row items-center">
            <img src="https://via.placeholder.com/300" alt="Ishan Chinthaka" class="w-64 h-64 rounded-full mb-6 md:mb-0 md:mr-10 object-cover">
            <div>
                <p class="mb-4">I am a highly focused, motivated, and analytical individual with a strong passion for challenges and problem-solving. I thrive in dynamic environments and am always eager to explore new growth opportunities.</p>
                <p class="mb-4">Currently pursuing BSc (Hons) in Software Engineering at Cardiff Metropolitan University (via ICBT Campus, Sri Lanka).</p>
                <p>Date of Birth: 22nd August 2002 | Gender: Male | Marital Status: Single</p>
            </div>
        </div>
    </section>

    <!-- Skills Section with Animated Bars -->
    <section id="skills" class="py-20 bg-gray-200 dark:bg-gray-800">
        <div class="container mx-auto px-4">
            <h2 class="text-4xl font-bold mb-8 text-center">Skills</h2>
            <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
                <!-- Example Skill -->
                <div>
                    <p class="font-semibold mb-1">JavaScript</p>
                    <div class="bg-gray-300 dark:bg-gray-600 h-4 rounded-full">
                        <div class="bg-accent h-4 rounded-full skill-bar" style="--progress: 90%;"></div>
                    </div>
                </div>
                <!-- Add more skills similarly -->
                <div>
                    <p class="font-semibold mb-1">Java</p>
                    <div class="bg-gray-300 dark:bg-gray-600 h-4 rounded-full">
                        <div class="bg-accent h-4 rounded-full skill-bar" style="--progress: 85%;"></div>
                    </div>
                </div>
                <!-- Repeat for other skills like Python, PHP, etc. -->
            </div>
        </div>
    </section>

    <!-- Projects Section with Cards -->
    <section id="projects" class="py-20 container mx-auto px-4">
        <h2 class="text-4xl font-bold mb-8 text-center">Projects</h2>
        <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
            <!-- Project Card -->
            <div class="bg-white dark:bg-gray-800 rounded-lg shadow-lg overflow-hidden transform hover:scale-105 transition-transform duration-300">
                <img src="https://via.placeholder.com/400x200" alt="Country Cafe" class="w-full h-48 object-cover">
                <div class="p-4">
                    <h3 class="text-2xl font-bold mb-2">Country Cafe Website</h3>
                    <p class="mb-4">Built with HTML, CSS, JS, MySQL, PHP. Features online ordering and reservations.</p>
                    <a href="#" class="text-accent hover:underline">View Project</a>
                </div>
            </div>
            <!-- Add more project cards -->
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="py-20 bg-gray-200 dark:bg-gray-800">
        <div class="container mx-auto px-4">
            <h2 class="text-4xl font-bold mb-8 text-center">Contact Me</h2>
            <form class="max-w-lg mx-auto" id="contactForm">
                <input type="text" placeholder="Name" class="w-full mb-4 p-3 rounded-lg border dark:border-gray-600" required>
                <input type="email" placeholder="Email" class="w-full mb-4 p-3 rounded-lg border dark:border-gray-600" required>
                <textarea placeholder="Message" class="w-full mb-4 p-3 rounded-lg border dark:border-gray-600" rows="5" required></textarea>
                <button type="submit" class="bg-accent text-white px-6 py-3 rounded-full w-full hover:bg-green-600">Send Message</button>
            </form>
        </div>
    </section>

    <!-- Footer -->
    <footer class="py-4 text-center bg-white dark:bg-gray-800">
        <p>&copy; 2025 Ishan Chinthaka. All rights reserved.</p>
    </footer>

    <script>
        // Dark Mode Toggle
        const toggle = document.getElementById('darkModeToggle');
        toggle.addEventListener('click', () => {
            document.documentElement.classList.toggle('dark');
            toggle.textContent = document.documentElement.classList.contains('dark') ? '☀️' : '🌙';
        });

        // Form Validation
        const form = document.getElementById('contactForm');
        form.addEventListener('submit', (e) => {
            e.preventDefault();
            if (form.checkValidity()) {
                alert('Message sent successfully!');
                form.reset();
            } else {
                alert('Please fill out all fields correctly.');
            }
        });
    </script>
</body>
</html>
