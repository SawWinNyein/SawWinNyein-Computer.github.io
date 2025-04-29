<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>index.html</title>

  <style>
    /* Myanmar Font */
@font-face {
    font-family: 'Myanmar3';
    src: url('https://cdn.jsdelivr.net/gh/LeonarAung/MyanmarFonts@master/fonts/Myanmar3/Myanmar3.ttf');
}

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Myanmar3', sans-serif;
}

body {
    background-color: #f5f5f5;
    color: #333;
    line-height: 1.6;
}

.container {
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 20px;
}

/* Navigation */
nav {
    background-color: #2c3e50;
    color: white;
    padding: 15px 0;
    position: fixed;
    width: 100%;
    top: 0;
    z-index: 1000;
    transition: all 0.3s ease;
}

nav.scrolled {
    padding: 10px 0;
    box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
}

.logo {
    display: flex;
    align-items: center;
    font-size: 1.5rem;
    font-weight: bold;
}

.logo i {
    margin-right: 10px;
    font-size: 1.8rem;
}

.nav-links {
    display: flex;
    list-style: none;
}

.nav-links li {
    margin-left: 30px;
}

.nav-links a {
    color: white;
    text-decoration: none;
    font-size: 1.1rem;
    transition: color 0.3s;
}

.nav-links a:hover {
    color: #3498db;
}

.menu-toggle {
    display: none;
    cursor: pointer;
}

/* Hero Section */
.hero {
    background: linear-gradient(rgba(0, 0, 0, 0.7), rgba(0, 0, 0, 0.7)), url('https://images.unsplash.com/photo-1550751827-4bd374c3f58b?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1470&q=80');
    background-size: cover;
    background-position: center;
    height: 100vh;
    display: flex;
    align-items: center;
    text-align: center;
    color: white;
    padding-top: 80px;
}

.hero h1 {
    font-size: 2.5rem;
    margin-bottom: 20px;
}

.hero p {
    font-size: 1.2rem;
    margin-bottom: 30px;
    max-width: 700px;
    margin-left: auto;
    margin-right: auto;
}

/* Courses Section */
.courses {
    padding: 80px 0;
    background-color: white;
}

.courses h2 {
    text-align: center;
    margin-bottom: 50px;
    font-size: 2rem;
    color: #2c3e50;
}

.course-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 30px;
}

.course-card {
    background-color: #f9f9f9;
    border-radius: 10px;
    padding: 30px;
    text-align: center;
    transition: transform 0.3s, box-shadow 0.3s;
}

.course-card:hover {
    transform: translateY(-10px);
    box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
}

.course-card i {
    font-size: 3rem;
    color: #3498db;
    margin-bottom: 20px;
}

.course-card h3 {
    margin-bottom: 15px;
    color: #2c3e50;
}

/* About Section */
.about {
    padding: 80px 0;
    background-color: #f5f5f5;
}

.about h2 {
    text-align: center;
    margin-bottom: 50px;
    font-size: 2rem;
    color: #2c3e50;
}

.about-content {
    display: flex;
    align-items: center;
    gap: 50px;
}

.about-text {
    flex: 1;
}

.about-text p {
    margin-bottom: 20px;
    font-size: 1.1rem;
    line-height: 1.8;
}

.about-image {
    flex: 1;
}

.about-image img {
    width: 100%;
    border-radius: 10px;
    box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
}

/* Contact Section */
.contact {
    padding: 80px 0;
    background-color: white;
}

.contact h2 {
    text-align: center;
    margin-bottom: 50px;
    font-size: 2rem;
    color: #2c3e50;
}

#contactForm {
    max-width: 600px;
    margin: 0 auto;
}

.form-group {
    margin-bottom: 20px;
}

.form-group label {
    display: block;
    margin-bottom: 5px;
    font-weight: bold;
}

.form-group input,
.form-group textarea {
    width: 100%;
    padding: 10px;
    border: 1px solid #ddd;
    border-radius: 5px;
    font-size: 1rem;
}

.form-group textarea {
    resize: vertical;
    min-height: 150px;
}

/* Buttons */
.btn {
    display: inline-block;
    background-color: #3498db;
    color: white;
    padding: 12px 30px;
    border: none;
    border-radius: 5px;
    font-size: 1rem;
    cursor: pointer;
    transition: background-color 0.3s;
}

.btn:hover {
    background-color: #2980b9;
}

.btn-outline {
    display: inline-block;
    background-color: transparent;
    color: #3498db;
    padding: 10px 25px;
    border: 2px solid #3498db;
    border-radius: 5px;
    font-size: 1rem;
    cursor: pointer;
    transition: all 0.3s;
    margin-top: 20px;
}

.btn-outline:hover {
    background-color: #3498db;
    color: white;
}

/* Footer */
footer {
    background-color: #2c3e50;
    color: white;
    padding: 50px 0 20px;
}

.footer-content {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 30px;
    margin-bottom: 30px;
}

.footer-section h3 {
    margin-bottom: 20px;
    font-size: 1.3rem;
}

.footer-section ul {
    list-style: none;
}

.footer-section ul li {
    margin-bottom: 10px;
}

.footer-section ul li a {
    color: #ddd;
    text-decoration: none;
    transition: color 0.3s;
}

.footer-section ul li a:hover {
    color: #3498db;
}

.footer-section p {
    margin-bottom: 10px;
    display: flex;
    align-items: center;
}

.footer-section p i {
    margin-right: 10px;
    width: 20px;
    text-align: center;
}

.copyright {
    text-align: center;
    padding-top: 20px;
    border-top: 1px solid rgba(255, 255, 255, 0.1);
}

/* Responsive Design */
@media (max-width: 768px) {
    .menu-toggle {
        display: block;
        font-size: 1.5rem;
    }

    .nav-links {
        position: fixed;
        top: 70px;
        left: -100%;
        width: 100%;
        height: calc(100vh - 70px);
        background-color: #2c3e50;
        flex-direction: column;
        align-items: center;
        padding: 20px 0;
        transition: left 0.3s ease;
    }

    .nav-links.active {
        left: 0;
    }

    .nav-links li {
        margin: 15px 0;
    }

    .hero h1 {
        font-size: 2rem;
    }

    .about-content {
        flex-direction: column;
    }

    .about-image {
        margin-top: 30px;
    }
}
  </style>

  
</head>
<body>
  <!DOCTYPE html>
<html lang="my">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>အခြေခံကွန်ပျူတာသင်တန်း</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <!-- Navigation Bar -->
    <nav id="navbar">
        <div class="container">
            <div class="logo">
                <i class="fas fa-laptop-code"></i>
                <span>ကွန်ပျူတာအခြေခံ</span>
            </div>
            <ul class="nav-links">
                <li><a href="#home">ပင်မစာမျက်နှာ</a></li>
                <li><a href="#courses">သင်တန်းများ</a></li>
                <li><a href="#about">ကျွန်ုပ်တို့အကြောင်း</a></li>
                <li><a href="#contact">ဆက်သွယ်ရန်</a></li>
            </ul>
            <div class="menu-toggle">
                <i class="fas fa-bars"></i>
            </div>
        </div>
    </nav>

    <!-- Hero Section -->
    <section id="home" class="hero">
        <div class="container">
            <h1>ကွန်ပျူတာအခြေခံများကို လွယ်ကူစွာလေ့လာပါ</h1>
            <p>အွန်လိုင်းမှတစ်ဆင့် အခမဲ့သင်ခန်းစာများဖြင့် လေ့လာနိုင်ပါပြီ</p>
            <button id="startLearningBtn" class="btn">ယခုစတင်လေ့လာမည်</button>
        </div>
    </section>

    <!-- Courses Section -->
    <section id="courses" class="courses">
        <div class="container">
            <h2>သင်တန်းများ</h2>
            <div class="course-grid">
                <div class="course-card">
                    <i class="fas fa-file-word"></i>
                    <h3>Microsoft Word</h3>
                    <p>စာစီစာရိုက်နည်းများနှင့် စာရွက်စာတမ်းများပြုလုပ်နည်း</p>
                    <button class="btn-outline">သင်ခန်းစာများကြည့်ရန်</button>
                </div>
                <div class="course-card">
                    <i class="fas fa-file-excel"></i>
                    <h3>Microsoft Excel</h3>
                    <p>ဇယားများပြုလုပ်ခြင်းနှင့် အချက်အလက်များစီမံခန့်ခွဲနည်း</p>
                    <button class="btn-outline">သင်ခန်းစာများကြည့်ရန်</button>
                </div>
                <div class="course-card">
                    <i class="fas fa-file-powerpoint"></i>
                    <h3>Microsoft PowerPoint</h3>
                    <p>ဆွဲဆောင်မှုရှိသော မိတ်ဆက်ပွဲစာရွက်များပြုလုပ်နည်း</p>
                    <button class="btn-outline">သင်ခန်းစာများကြည့်ရန်</button>
                </div>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section id="about" class="about">
        <div class="container">
            <h2>ကျွန်ုပ်တို့အကြောင်း</h2>
            <div class="about-content">
                <div class="about-text">
                    <p>ကျွန်ုပ်တို့၏ ရည်ရွယ်ချက်မှာ မြန်မာနိုင်ငံရှိ လူတိုင်းကွန်ပျူတာအခြေခံများကို အလွယ်တကူနားလည်စွာ လေ့လာနိုင်စေရန်ဖြစ်ပါသည်။</p>
                    <p>အွန်လိုင်းမှတစ်ဆင့် အခမဲ့သင်ကြားပေးခြင်း၊ လက်တွေ့အသုံးချနိုင်သော သင်ခန်းစာများဖြင့် သင်ကြားပေးလျက်ရှိပါသည်။</p>
                </div>
                <div class="about-image">
                    <img src="https://imgur.com/VO6OFC1.jpg" alt="ကွန်ပျူတာသင်တန်း">
                   
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="contact">
        <div class="container">
            <h2>ဆက်သွယ်ရန်</h2>
            <form id="contactForm">
                <div class="form-group">
                    <label for="name">အမည်</label>
                    <input type="text" id="name" required>
                </div>
                <div class="form-group">
                    <label for="email">အီးမေးလ်</label>
                    <input type="email" id="email" required>
                </div>
                <div class="form-group">
                    <label for="message">မက်ဆေ့ချ်</label>
                    <textarea id="message" rows="5" required></textarea>
                </div>
                <button type="submit" class="btn">ပေးပို့မည်</button>
            </form>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-section">
                    <h3>လင့်ခ်များ</h3>
                    <ul>
                        <li><a href="#home">ပင်မစာမျက်နှာ</a></li>
                        <li><a href="#courses">သင်တန်းများ</a></li>
                        <li><a href="#about">ကျွန်ုပ်တို့အကြောင်း</a></li>
                        <li><a href="#contact">ဆက်သွယ်ရန်</a></li>
                    </ul>
                </div>
                <div class="footer-section">
                    <h3>ဆက်သွယ်ရန်</h3>
                    <p><i class="fas fa-phone"></i> ၀၉ ၄၄၉ ၀၃၆ ၃၂၉</p>
                    <p><i class="fas fa-envelope"></i>sawwinnyein2002@gmail.com</p>
                    <p><i class="fas fa-map-marker-alt"></i>ကော့သလော်ဘုန်းတော်ကြီးကျောင်း၊ ဘားအံမြို့</p>
                </div>
            </div>
            <div class="copyright">
                <p>&copy; 2023 အခြေခံကွန်ပျူတာသင်တန်း. All rights reserved.</p>
            </div>
        </div>
    </footer>

    <script src="script.js"></script>
</body>
</html>

  <script>
    // Mobile Menu Toggle
const menuToggle = document.querySelector('.menu-toggle');
const navLinks = document.querySelector('.nav-links');

menuToggle.addEventListener('click', () => {
    navLinks.classList.toggle('active');
});

// Close mobile menu when clicking on a link
document.querySelectorAll('.nav-links a').forEach(link => {
    link.addEventListener('click', () => {
        navLinks.classList.remove('active');
    });
});

// Sticky Navigation on Scroll
window.addEventListener('scroll', () => {
    const nav = document.querySelector('nav');
    nav.classList.toggle('scrolled', window.scrollY > 0);
});

// Smooth Scrolling for Anchor Links
document.querySelectorAll('a[href^="#"]').forEach(anchor => {
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

// Contact Form Submission
const contactForm = document.getElementById('contactForm');

contactForm.addEventListener('submit', function(e) {
    e.preventDefault();
    
    const name = document.getElementById('name').value;
    const email = document.getElementById('email').value;
    const message = document.getElementById('message').value;
    
    // Here you would typically send the data to a server
    // For this example, we'll just show an alert
    alert(`ကျေးဇူးတင်ပါသည် ${name}!\nသင့်မက်ဆေ့ချ်ကိုလက်ခံရရှိပါပြီ။ မကြာမီပြန်လည်ဆက်သွယ်ပေးပါမည်။`);
    
    // Reset the form
    contactForm.reset();
});

// Start Learning Button Animation
const startLearningBtn = document.getElementById('startLearningBtn');

startLearningBtn.addEventListener('mouseover', () => {
    startLearningBtn.style.transform = 'scale(1.05)';
});

startLearningBtn.addEventListener('mouseout', () => {
    startLearningBtn.style.transform = 'scale(1)';
});

startLearningBtn.addEventListener('click', () => {
    window.scrollTo({
        top: document.getElementById('courses').offsetTop - 70,
        behavior: 'smooth'
    });
});

// Course Card Animation
const courseCards = document.querySelectorAll('.course-card');

courseCards.forEach(card => {
    card.addEventListener('mouseover', () => {
        const icon = card.querySelector('i');
        icon.style.transform = 'rotate(15deg)';
        icon.style.color = '#e74c3c';
    });
    
    card.addEventListener('mouseout', () => {
        const icon = card.querySelector('i');
        icon.style.transform = 'rotate(0)';
        icon.style.color = '#3498db';
    });
});

// Current Year for Footer
document.querySelector('.copyright p').innerHTML = `&copy; ${new Date().getFullYear()} အခြေခံကွန်ပျူတာသင်တန်း. All rights reserved.`;
  </script>
</body>
</html>
