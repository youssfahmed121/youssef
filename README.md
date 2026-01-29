<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ElegantWed - أفخم تجهيزات الأعراس</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        :root {
            --primary: #e63946;
            --secondary: #1d3557;
            --accent: #f1faee;
            --light: #a8dadc;
            --dark: #457b9d;
            --gold: #d4af37;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.6;
            color: #333;
            background-color: #f8f9fa;
        }

        /* Header Styles */
        header {
            background: linear-gradient(135deg, var(--secondary) 0%, var(--dark) 100%);
            color: white;
            padding: 1rem 0;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            box-shadow: 0 2px 10px rgba(0,0,0,0.2);
        }

        .navbar {
            max-width: 1400px;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 0 2rem;
        }

        .logo {
            font-size: 2rem;
            font-weight: bold;
            color: var(--gold);
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .logo i {
            color: var(--gold);
        }

        .nav-links {
            display: flex;
            gap: 2rem;
            list-style: none;
        }

        .nav-links a {
            color: white;
            text-decoration: none;
            font-weight: 500;
            font-size: 1.1rem;
            padding: 8px 12px;
            border-radius: 5px;
            transition: all 0.3s ease;
        }

        .nav-links a:hover, .nav-links a.active {
            background: var(--gold);
            color: var(--secondary);
        }

        .nav-buttons {
            display: flex;
            gap: 1rem;
        }

        .btn {
            padding: 10px 25px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            font-weight: 600;
            transition: all 0.3s ease;
            text-decoration: none;
            display: inline-block;
        }

        .btn-primary {
            background: var(--gold);
            color: var(--secondary);
        }

        .btn-primary:hover {
            background: #c5a42a;
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(0,0,0,0.2);
        }

        .btn-outline {
            background: transparent;
            border: 2px solid var(--gold);
            color: var(--gold);
        }

        .btn-outline:hover {
            background: var(--gold);
            color: var(--secondary);
        }

        .hamburger {
            display: none;
            background: none;
            border: none;
            color: white;
            font-size: 1.5rem;
            cursor: pointer;
        }

        /* Hero Section */
        .hero {
            background: linear-gradient(rgba(0,0,0,0.6), rgba(0,0,0,0.6)), url('https://images.unsplash.com/photo-1519741497674-611481863552?w=1600') center/cover no-repeat;
            height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            color: white;
            margin-top: 70px;
        }

        .hero-content {
            max-width: 800px;
            padding: 2rem;
        }

        .hero h1 {
            font-size: 4rem;
            margin-bottom: 1rem;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.5);
            background: linear-gradient(to right, var(--gold), #fff);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .hero p {
            font-size: 1.5rem;
            margin-bottom: 2rem;
            text-shadow: 1px 1px 3px rgba(0,0,0,0.5);
        }

        /* Features Section */
        .features {
            padding: 5rem 2rem;
            background: white;
        }

        .container {
            max-width: 1400px;
            margin: 0 auto;
        }

        .section-title {
            text-align: center;
            margin-bottom: 3rem;
        }

        .section-title h2 {
            font-size: 2.5rem;
            color: var(--secondary);
            margin-bottom: 1rem;
            position: relative;
            display: inline-block;
        }

        .section-title h2::after {
            content: '';
            position: absolute;
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
            width: 80px;
            height: 4px;
            background: var(--gold);
            border-radius: 2px;
        }

        .section-title p {
            color: #666;
            margin-top: 1rem;
        }

        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            margin-top: 2rem;
        }

        .feature-card {
            background: white;
            padding: 2rem;
            border-radius: 10px;
            text-align: center;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            transition: all 0.3s ease;
            border: 2px solid transparent;
        }

        .feature-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 10px 25px rgba(0,0,0,0.15);
            border-color: var(--gold);
        }

        .feature-icon {
            font-size: 3rem;
            color: var(--gold);
            margin-bottom: 1rem;
        }

        .feature-card h3 {
            font-size: 1.5rem;
            color: var(--secondary);
            margin-bottom: 1rem;
        }

        .feature-card p {
            color: #666;
            line-height: 1.8;
        }

        /* Products Section */
        .products {
            padding: 5rem 2rem;
            background: #f8f9fa;
        }

        .products-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            margin-top: 2rem;
        }

        .product-card {
            background: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            transition: all 0.3s ease;
        }

        .product-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0,0,0,0.2);
        }

        .product-img {
            height: 250px;
            width: 100%;
            object-fit: cover;
        }

        .product-info {
            padding: 1.5rem;
        }

        .product-info h3 {
            font-size: 1.3rem;
            color: var(--secondary);
            margin-bottom: 0.5rem;
        }

        .product-info p {
            color: #666;
            margin-bottom: 1rem;
            font-size: 0.95rem;
        }

        .product-price {
            font-size: 1.5rem;
            font-weight: bold;
            color: var(--primary);
            margin-bottom: 1rem;
        }

        /* Testimonials Section */
        .testimonials {
            padding: 5rem 2rem;
            background: linear-gradient(135deg, var(--secondary) 0%, var(--dark) 100%);
            color: white;
        }

        .testimonials .section-title h2 {
            color: white;
        }

        .testimonials .section-title h2::after {
            background: var(--gold);
        }

        .testimonials-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            margin-top: 2rem;
        }

        .testimonial-card {
            background: rgba(255,255,255,0.1);
            padding: 2rem;
            border-radius: 10px;
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255,255,255,0.2);
        }

        .testimonial-header {
            display: flex;
            align-items: center;
            gap: 1rem;
            margin-bottom: 1rem;
        }

        .testimonial-img {
            width: 60px;
            height: 60px;
            border-radius: 50%;
            object-fit: cover;
            border: 3px solid var(--gold);
        }

        .testimonial-info h4 {
            font-size: 1.2rem;
            color: var(--gold);
        }

        .testimonial-info p {
            font-size: 0.9rem;
            color: rgba(255,255,255,0.7);
        }

        .testimonial-text {
            font-style: italic;
            line-height: 1.8;
            margin-bottom: 1rem;
            position: relative;
            padding-right: 20px;
        }

        .testimonial-text::before {
            content: '"';
            font-size: 3rem;
            color: var(--gold);
            opacity: 0.3;
            position: absolute;
            top: -20px;
            right: 0;
        }

        .rating {
            color: var(--gold);
            font-size: 1.2rem;
        }

        /* Contact Section */
        .contact {
            padding: 5rem 2rem;
            background: white;
        }

        .contact-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 3rem;
            margin-top: 2rem;
        }

        .contact-info {
            display: flex;
            flex-direction: column;
            gap: 1.5rem;
        }

        .contact-item {
            display: flex;
            align-items: flex-start;
            gap: 1rem;
        }

        .contact-icon {
            width: 50px;
            height: 50px;
            background: var(--gold);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--secondary);
            font-size: 1.2rem;
            flex-shrink: 0;
        }

        .contact-text h3 {
            color: var(--secondary);
            margin-bottom: 0.5rem;
        }

        .contact-form .form-group {
            margin-bottom: 1.5rem;
        }

        .contact-form input,
        .contact-form textarea {
            width: 100%;
            padding: 12px 15px;
            border: 2px solid #ddd;
            border-radius: 5px;
            font-size: 1rem;
            transition: border-color 0.3s ease;
        }

        .contact-form input:focus,
        .contact-form textarea:focus {
            outline: none;
            border-color: var(--gold);
        }

        .contact-form textarea {
            min-height: 150px;
            resize: vertical;
        }

        /* Footer */
        footer {
            background: var(--secondary);
            color: white;
            padding: 3rem 2rem 1rem;
        }

        .footer-container {
            max-width: 1400px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
        }

        .footer-col h3 {
            font-size: 1.3rem;
            margin-bottom: 1.5rem;
            position: relative;
            padding-bottom: 10px;
        }

        .footer-col h3::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 50px;
            height: 3px;
            background: var(--gold);
        }

        .footer-links {
            list-style: none;
            display: flex;
            flex-direction: column;
            gap: 10px;
        }

        .footer-links a {
            color: #ccc;
            text-decoration: none;
            transition: color 0.3s ease;
        }

        .footer-links a:hover {
            color: var(--gold);
        }

        .footer-about p {
            color: #ccc;
            line-height: 1.8;
            margin-bottom: 1rem;
        }

        .social-links {
            display: flex;
            gap: 15px;
            margin-top: 1rem;
        }

        .social-links a {
            width: 40px;
            height: 40px;
            background: rgba(255,255,255,0.1);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            transition: all 0.3s ease;
            text-decoration: none;
        }

        .social-links a:hover {
            background: var(--gold);
            transform: translateY(-3px);
        }

        .copyright {
            text-align: center;
            padding-top: 2rem;
            margin-top: 2rem;
            border-top: 1px solid rgba(255,255,255,0.1);
            color: #ccc;
            font-size: 0.9rem;
        }

        /* Animations */
        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .animate {
            animation: fadeInUp 0.8s ease forwards;
        }

        .animate-delay-1 { animation-delay: 0.2s; }
        .animate-delay-2 { animation-delay: 0.4s; }
        .animate-delay-3 { animation-delay: 0.6s; }

        /* Responsive Design */
        @media (max-width: 768px) {
            .hamburger {
                display: block;
            }

            .nav-links {
                position: fixed;
                top: 70px;
                right: -100%;
                flex-direction: column;
                background: var(--secondary);
                width: 250px;
                height: calc(100vh - 70px);
                padding: 2rem;
                transition: right 0.3s ease;
                box-shadow: -5px 0 15px rgba(0,0,0,0.1);
            }

            .nav-links.active {
                right: 0;
            }

            .hero h1 {
                font-size: 2.5rem;
            }

            .hero p {
                font-size: 1.2rem;
            }

            .section-title h2 {
                font-size: 2rem;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <nav class="navbar">
            <div class="logo">
                <i class="fas fa-ring"></i>
                <span>ElegantWed</span>
            </div>
            <ul class="nav-links">
                <li><a href="#home" class="active">الرئيسية</a></li>
                <li><a href="#features">المميزات</a></li>
                <li><a href="#products">المنتجات</a></li>
                <li><a href="#testimonials">آراء العملاء</a></li>
                <li><a href="#contact">اتصل بنا</a></li>
            </ul>
            <div class="nav-buttons">
                <button class="btn btn-outline"><i class="fas fa-user"></i> تسجيل الدخول</button>
                <button class="btn btn-primary"><i class="fas fa-shopping-cart"></i> سلة التسوق</button>
            </div>
            <button class="hamburger" id="hamburger">
                <i class="fas fa-bars"></i>
            </button>
        </nav>
    </header>

    <!-- Hero Section -->
    <section class="hero" id="home">
        <div class="hero-content animate">
            <h1>أعراس أحلامك تبدأ هنا</h1>
            <p>نقدم لك أفخم تجهيزات حفلات الزفاف بجودة عالية وأسعار تنافسية</p>
            <a href="#products" class="btn btn-primary">تصفح منتجاتنا</a>
        </div>
    </section>

    <!-- Features Section -->
    <section class="features" id="features">
        <div class="container">
            <div class="section-title animate">
                <h2>لماذا تختارنا</h2>
                <p>نقدم أفضل الخدمات لضمان حفل زفاف لا يُنسى</p>
            </div>
            <div class="features-grid">
                <div class="feature-card animate animate-delay-1">
                    <div class="feature-icon">
                        <i class="fas fa-crown"></i>
                    </div>
                    <h3>جودة عالية</h3>
                    <p>نستخدم أفضل المواد والخامات لضمان جودة تدوم طويلاً</p>
                </div>
                <div class="feature-card animate animate-delay-2">
                    <div class="feature-icon">
                        <i class="fas fa-truck"></i>
                    </div>
                    <h3>توصيل مجاني</h3>
                    <p>خدمة توصيل مجانية لجميع أنحاء المملكة</p>
                </div>
                <div class="feature-card animate animate-delay-3">
                    <div class="feature-icon">
                        <i class="fas fa-headset"></i>
                    </div>
                    <h3>دعم فني</h3>
                    <p>فريق دعم متاح 24/7 للرد على جميع استفساراتك</p>
                </div>
                <div class="feature-card animate">
                    <div class="feature-icon">
                        <i class="fas fa-gift"></i>
                    </div>
                    <h3>عروض خاصة</h3>
                    <p>خصومات حصرية وعروض مميزة على جميع المنتجات</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Products Section -->
    <section class="products" id="products">
        <div class="container">
            <div class="section-title animate">
                <h2>منتجاتنا المميزة</h2>
                <p>تصفح أحدث منتجاتنا لتجهيز حفل زفافك</p>
            </div>
            <div class="products-grid">
                <div class="product-card animate animate-delay-1">
                    <img src="https://images.unsplash.com/photo-1560448204-8cf87f3c39c2?w=600" alt="فستان زفاف" class="product-img">
                    <div class="product-info">
                        <h3>فستان زفاف كريستال</h3>
                        <p>فستان زفاف فاخر مزين بالكريستال والأحجار الكريمة</p>
                        <div class="product-price">2,499 ر.س</div>
                        <button class="btn btn-primary">أضف للسلة</button>
                    </div>
                </div>
                <div class="product-card animate animate-delay-2">
                    <img src="https://images.unsplash.com/photo-1527529482837-4698179dc6ce?w=600" alt="ديكور قاعة" class="product-img">
                    <div class="product-info">
                        <h3>ديكور قاعة فاخر</h3>
                        <p>ديكور كامل للقاعة بألوان ذهبية ووردية</p>
                        <div class="product-price">3,999 ر.س</div>
                        <button class="btn btn-primary">أضف للسلة</button>
                    </div>
                </div>
                <div class="product-card animate animate-delay-3">
                    <img src="https://images.unsplash.com/photo-1519741497674-611481863552?w=600" alt="طقم مجوهرات" class="product-img">
                    <div class="product-info">
                        <h3>طقم مجوهرات</h3>
                        <p>طقم مجوهرات ذهبي مكون من عقد وأقراط وسوار</p>
                        <div class="product-price">1,899 ر.س</div>
                        <button class="btn btn-primary">أضف للسلة</button>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Testimonials Section -->
    <section class="testimonials" id="testimonials">
        <div class="container">
            <div class="section-title animate">
                <h2>آراء عملائنا</h2>
                <p>اقرأ تجارب عملائنا الذين وثقوا بنا</p>
            </div>
            <div class="testimonials-grid">
                <div class="testimonial-card animate animate-delay-1">
                    <div class="testimonial-header">
                        <img src="https://randomuser.me/api/portraits/women/44.jpg" alt="سارة أحمد" class="testimonial-img">
                        <div class="testimonial-info">
                            <h4>سارة أحمد</h4>
                            <p>زفاف 2024</p>
                        </div>
                    </div>
                    <p class="testimonial-text">خدمة ممتازة وجودة رائعة! كل شيء كان مثالياً في حفل زفافي بفضل فريق ElegantWed.</p>
                    <div class="rating">
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                    </div>
                </div>
                <div class="testimonial-card animate animate-delay-2">
                    <div class="testimonial-header">
                        <img src="https://randomuser.me/api/portraits/women/68.jpg" alt="نورا محمد" class="testimonial-img">
                        <div class="testimonial-info">
                            <h4>نورا محمد</h4>
                            <p>زفاف 2023</p>
                        </div>
                    </div>
                    <p class="testimonial-text">تعاملت معهم وكانت التجربة رائعة من البداية للنهاية. الأسعار معقولة والجودة ممتازة.</p>
                    <div class="rating">
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star-half-alt"></i>
                    </div>
                </div>
                <div class="testimonial-card animate animate-delay-3">
                    <div class="testimonial-header">
                        <img src="https://randomuser.me/api/portraits/women/32.jpg" alt="ليان خالد" class="testimonial-img">
                        <div class="testimonial-info">
                            <h4>ليان خالد</h4>
                            <p>زفاف 2024</p>
                        </div>
                    </div>
                    <p class="testimonial-text">أشكر الفريق على الاهتمام بالتفاصيل والسرعة في التوصيل. أنصح الجميع بالتعامل معهم!</p>
                    <div class="rating">
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section class="contact" id="contact">
        <div class="container">
            <div class="section-title animate">
                <h2>اتصل بنا</h2>
                <p>نحن هنا للرد على جميع استفساراتك</p>
            </div>
            <div class="contact-container">
                <div class="contact-info animate animate-delay-1">
                    <div class="contact-item">
                        <div class="contact-icon">
                            <i class="fas fa-map-marker-alt"></i>
                        </div>
                        <div class="contact-text">
                            <h3>العنوان</h3>
                            <p>الرياض، المملكة العربية السعودية</p>
                        </div>
                    </div>
                    <div class="contact-item">
                        <div class="contact-icon">
                            <i class="fas fa-phone"></i>
                        </div>
                        <div class="contact-text">
                            <h3>الهاتف</h3>
                            <p>+966 11 123 4567</p>
                        </div>
                    </div>
                    <div class="contact-item">
                        <div class="contact-icon">
                            <i class="fas fa-envelope"></i>
                        </div>
                        <div class="contact-text">
                            <h3>البريد الإلكتروني</h3>
                            <p>info@elegantwed.com</p>
                        </div>
                    </div>
                    <div class="contact-item">
                        <div class="contact-icon">
                            <i class="fas fa-clock"></i>
                        </div>
                        <div class="contact-text">
                            <h3>ساعات العمل</h3>
                            <p>الأحد - الخميس: 9 صباحاً - 10 مساءً<br>الجمعة - السبت: 4 مساءً - 12 صباحاً</p>
                        </div>
                    </div>
                </div>
                <div class="contact-form animate animate-delay-2">
                    <form>
                        <div class="form-group">
                            <input type="text" placeholder="اسمك الكامل" required>
                        </div>
                        <div class="form-group">
                            <input type="email" placeholder="بريدك الإلكتروني" required>
                        </div>
                        <div class="form-group">
                            <input type="tel" placeholder="رقم الهاتف">
                        </div>
                        <div class="form-group">
                            <textarea placeholder="رسالتك" required></textarea>
                        </div>
                        <button type="submit" class="btn btn-primary">إرسال الرسالة</button>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-container">
                <div class="footer-col footer-about">
                    <h3>ElegantWed</h3>
                    <p>نحن متخصصون في توفير أفخم تجهيزات حفلات الزفاف بجودة عالية وأسعار تنافسية لنجعل يومك الخاص لا يُنسى.</p>
                    <div class="social-links">
                        <a href="#"><i class="fab fa-instagram"></i></a>
                        <a href="#"><i class="fab fa-twitter"></i></a>
                        <a href="#"><i class="fab fa-facebook-f"></i></a>
                        <a href="#"><i class="fab fa-whatsapp"></i></a>
                    </div>
                </div>
                <div class="footer-col">
                    <h3>روابط سريعة</h3>
                    <ul class="footer-links">
                        <li><a href="#home">الرئيسية</a></li>
                        <li><a href="#features">المميزات</a></li>
                        <li><a href="#products">المنتجات</a></li>
                        <li><a href="#testimonials">آراء العملاء</a></li>
                        <li><a href="#contact">اتصل بنا</a></li>
                    </ul>
                </div>
                <div class="footer-col">
                    <h3>المنتجات</h3>
                    <ul class="footer-links">
                        <li><a href="#">فساتين زفاف</a></li>
                        <li><a href="#">مجوهرات</a></li>
                        <li><a href="#">ديكور القاعات</a></li>
                        <li><a href="#">إكسسوارات</a></li>
                        <li><a href="#">هدايا الزفاف</a></li>
                    </ul>
                </div>
                <div class="footer-col">
                    <h3>النشرة البريدية</h3>
                    <p>اشترك في نشرتنا البريدية لتلقي أحدث العروض والأخبار</p>
                    <form class="newsletter-form" style="margin-top: 15px;">
                        <input type="email" placeholder="بريدك الإلكتروني" style="width: 100%; padding: 10px; margin-top: 10px; border-radius: 5px; border: none;">
                        <button type="submit" class="btn btn-primary" style="width: 100%; margin-top: 10px; padding: 10px;">اشترك الآن</button>
                    </form>
                </div>
            </div>
            <div class="copyright">
                <p>&copy; 2026 ElegantWed. جميع الحقوق محفوظة.</p>
            </div>
        </div>
    </footer>

    <script>
        // Mobile Menu Toggle
        const hamburger = document.getElementById('hamburger');
        const navLinks = document.querySelector('.nav-links');

        hamburger.addEventListener('click', () => {
            navLinks.classList.toggle('active');
            hamburger.innerHTML = navLinks.classList.contains('active') 
                ? '<i class="fas fa-times"></i>' 
                : '<i class="fas fa-bars"></i>';
        });

        // Close mobile menu when clicking a link
        document.querySelectorAll('.nav-links a').forEach(link => {
            link.addEventListener('click', () => {
                navLinks.classList.remove('active');
                hamburger.innerHTML = '<i class="fas fa-bars"></i>';
            });
        });

        // Smooth scrolling for anchor links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    window.scrollTo({
                        top: target.offsetTop - 70,
                        behavior: 'smooth'
                    });
                }
            });
        });

        // Add scroll animation
        const animateElements = document.querySelectorAll('.animate');
        
        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.style.opacity = 1;
                    entry.target.style.transform = 'translateY(0)';
                }
            });
        }, { threshold: 0.1 });

        animateElements.forEach(element => {
            element.style.opacity = 0;
            element.style.transform = 'translateY(30px)';
            element.style.transition = 'opacity 0.6s ease, transform 0.6s ease';
            observer.observe(element);
        });

        // Form submission
        const forms = document.querySelectorAll('form');
        forms.forEach(form => {
            form.addEventListener('submit', (e) => {
                e.preventDefault();
                alert('تم إرسال رسالتك بنجاح! سنرد عليك قريباً.');
                form.reset();
            });
        });

        // Product card hover effect enhancement
        const productCards = document.querySelectorAll('.product-card');
        productCards.forEach(card => {
            const button = card.querySelector('button');
            button.addEventListener('click', () => {
                button.innerHTML = '<i class="fas fa-check"></i> تمت الإضافة';
                button.style.background = '#28a745';
                
                setTimeout(() => {
                    button.innerHTML = '<i class="fas fa-shopping-cart"></i> أضف للسلة';
                    button.style.background = '';
                }, 2000);
            });
        });
    </script>
</body>
</html>
