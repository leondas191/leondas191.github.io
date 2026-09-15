
<html lang="bn">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>আমার আন্ডা | খাঁটি ও তাজা ডিম</title>
    <style>
        /* বেসিক স্টাইল ও রিসেট */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        body {
            color: #333;
            line-height: 1.6;
            background-color: #fdfcf9;
        }

        :root {
            --primary-color: #ffc107; /* ডিমের কুসুমের রঙ */
            --dark-color: #222431;
            --light-bg: #f8f9fa;
        }

        /* হেডার ও মেনুবার */
        header {
            background-color: #fff;
            box-shadow: 0 2px 10px rgba(0,0,0,0.05);
            position: sticky;
            top: 0;
            z-index: 100;
        }

        .nav-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            max-width: 1200px;
            margin: 0 auto;
            padding: 15px 20px;
        }

        .logo {
            font-size: 26px;
            font-weight: 800;
            color: var(--dark-color);
            text-decoration: none;
        }

        .logo span {
            color: var(--primary-color);
        }

        .nav-links {
            list-style: none;
            display: flex;
        }

        .nav-links li {
            margin-left: 20px;
        }

        .nav-links a {
            text-decoration: none;
            color: var(--dark-color);
            font-weight: 600;
            transition: color 0.3s;
        }

        .nav-links a:hover {
            color: var(--primary-color);
        }

        /* হিরো ব্যানার সেকশন (১ম ছবি এখানে ব্যাকগ্রাউন্ড হিসেবে থাকবে) */
        .hero {
            background: linear-gradient(rgba(0,0,0,0.55), rgba(0,0,0,0.55)), url('pic1.jpg') no-repeat center center/cover;
            height: 65vh;
            display: flex;
            justify-content: center;
            align-items: center;
            text-align: center;
            color: #fff;
            padding: 20px;
        }

        .hero-content h1 {
            font-size: 45px;
            margin-bottom: 15px;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.6);
        }

        .hero-content p {
            font-size: 18px;
            margin-bottom: 25px;
        }

        .btn {
            display: inline-block;
            background-color: var(--primary-color);
            color: var(--dark-color);
            padding: 12px 30px;
            text-decoration: none;
            font-weight: bold;
            border-radius: 25px;
            transition: all 0.3s;
        }

        .btn:hover {
            transform: scale(1.05);
            background-color: #e0a800;
            box-shadow: 0 5px 15px rgba(255,193,7,0.3);
        }

        /* সেকশন হেডিং স্টাইল */
        .section-title {
            text-align: center;
            margin: 60px 0 30px 0;
            font-size: 32px;
            color: var(--dark-color);
        }

        .section-title::after {
            content: '';
            display: block;
            width: 50px;
            height: 4px;
            background-color: var(--primary-color);
            margin: 10px auto 0 auto;
            border-radius: 2px;
        }

        /* কোম্পানির সিইও ও পরিচিতি সেকশন */
        .ceo-section {
            max-width: 1000px;
            margin: 0 auto 50px auto;
            padding: 30px 20px;
            background: #fff;
            border-radius: 15px;
            box-shadow: 0 5px 20px rgba(0,0,0,0.05);
            display: flex;
            align-items: center;
            gap: 40px;
        }

        .ceo-info {
            flex: 1;
        }

        .ceo-badge {
            background-color: #ffeaa7;
            color: #d63031;
            padding: 5px 15px;
            border-radius: 15px;
            font-size: 14px;
            font-weight: bold;
            display: inline-block;
            margin-bottom: 10px;
        }

        .ceo-name {
            font-size: 26px;
            font-weight: 700;
            color: var(--dark-color);
            margin-bottom: 10px;
        }

        /* আমাদের খামার ও গ্যালারি সেকশন (বাকি ২টি ছবি এখানে) */
        .gallery-section {
            max-width: 1200px;
            margin: 0 auto 50px auto;
            padding: 0 20px;
        }

        .gallery-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(450px, 1fr));
            gap: 25px;
        }

        .gallery-item {
            background: #fff;
            border-radius: 12px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0,0,0,0.06);
        }

        .gallery-item img {
            width: 100%;
            height: 400px;
            object-fit: cover;
            display: block;
        }

        .gallery-desc {
            padding: 15px;
            text-align: center;
            font-weight: 600;
            color: var(--dark-color);
            background-color: #fff;
        }

        /* কাস্টমার রিভিউ ও মূল্যতালিকা সেকশন */
        .business-info-section {
            background-color: var(--light-bg);
            padding: 60px 20px;
        }

        .info-container {
            max-width: 1200px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 40px;
        }

        .price-box, .review-box {
            background: #fff;
            padding: 30px;
            border-radius: 12px;
            box-shadow: 0 4px 10px rgba(0,0,0,0.03);
        }

        .price-item {
            display: flex;
            justify-content: space-between;
            padding: 12px 0;
            border-bottom: 1px dashed #ddd;
            font-size: 18px;
        }

        .price-item:last-child {
            border-bottom: none;
        }

        .price-tag {
            color: #e67e22;
            font-weight: bold;
        }

        /* কাস্টমার রিভিউ স্টাইল */
        .customer-card {
            border-left: 4px solid var(--primary-color);
            padding-left: 15px;
            margin-top: 20px;
        }

        .customer-name {
            font-weight: bold;
            font-size: 18px;
            color: var(--dark-color);
            margin-top: 10px;
        }

        .customer-tag {
            font-size: 13px;
            color: #27ae60;
            font-weight: 600;
        }

        /* যোগাযোগ সেকশন */
        .contact-section {
            max-width: 600px;
            margin: 60px auto;
            padding: 0 20px;
            text-align: center;
        }

        .contact-form {
            display: flex;
            flex-direction: column;
            gap: 15px;
            margin-top: 20px;
        }

        .contact-form input, .contact-form textarea {
            padding: 15px;
            border: 1px solid #ccc;
            border-radius: 5px;
            width: 100%;
            font-size: 16px;
        }

        /* ফুটার */
        footer {
            background-color: var(--dark-color);
            color: #fff;
            text-align: center;
            padding: 20px;
            margin-top: 60px;
        }

        /* মোবাইল রেসপনসিভ */
        @media (max-width: 768px) {
            .nav-container {
                flex-direction: column;
            }
            .nav-links {
                margin-top: 15px;
            }
            .hero-content h1 {
                font-size: 32px;
            }
            .ceo-section, .info-container {
                flex-direction: column;
                grid-template-columns: 1fr;
            }
            .gallery-grid {
                grid-template-columns: 1fr;
            }
            .gallery-item img {
                height: 300px;
            }
        }
    </style>
</head>
<body>

    <header>
        <div class="nav-container">
            <a href="#" class="logo">🥚 আমার<span>আন্ডা</span></a>
            <ul class="nav-links">
                <li><a href="#home">হোম</a></li>
                <li><a href="#ceo">পরিচিতি</a></li>
                <li><a href="#gallery">আমাদের খামার</a></li>
                <li><a href="#info">মূল্য ও রিভিউ</a></li>
                <li><a href="#contact">যোগাযোগ</a></li>
            </ul>
        </div>
    </header>

    <section id="home" class="hero">
        <div class="hero-content">
            <h1>খামার থেকে সরাসরি তাজা ডিম আপনার টেবিলে</h1>
            <p>"আমার আন্ডা" - শতভাগ খাঁটি, পুষ্টিকর এবং স্বাস্থ্যকর ডিমের সুপরিচিত প্রতিষ্ঠান।</p>
            <a href="#info" class="btn">আজকের রেট দেখুন</a>
        </div>
    </section>

    <section id="ceo" style="padding: 10px 0;">
        <h2 class="section-title">নেতৃত্বে আমাদের টিম</h2>
        <div class="ceo-section">
            <div class="ceo-info">
                <span class="ceo-badge">কোম্পানি সিইও (CEO)</span>
                <h3 class="ceo-name">তন্ময় ব্যাপারী (Tonmoy Bepary)</h3>
                <p style="color: #555; font-size: 16px;">
                    "আমাদের লক্ষ্য প্রতিটি পরিবারে সাশ্রয়ী মূল্যে সম্পূর্ণ অর্গানিক এবং পুষ্টিকর ডিম পৌঁছে দেওয়া। 'আমার আন্ডা' কোনো কৃত্রিম উপায়ে নয়, বরং সম্পূর্ণ প্রাকৃতিক ও স্বাস্থ্যকর উপায়ে ডিম উৎপাদন নিশ্চিত করে।"
                </p>
            </div>
        </div>
    </section>

    <section id="gallery" class="gallery-section">
        <h2 class="section-title">আমাদের খামার গ্যালারি</h2>
        <div class="gallery-grid">
            
            <div class="gallery-item">
                <img src=".pic1.jpg" alt="তাজা ডিম সংগ্রহ">
                <div class="gallery-desc">খামার থেকে প্রতিদিনের তাজা ডিম সংগ্রহ</div>
            </div>

            <div class="gallery-item">
                <img src=".pic2.jpg" alt="ডিমের গুণগত মান যাচাই">
                <div class="gallery-desc">প্রতিটি আন্ডার শতভাগ পুষ্টিগুণ নিশ্চিতকরণ</div>
            </div>

        </div>
    </section>

    <section id="info" class="business-info-section">
        <div class="info-container">
            
            <div class="price-box">
                <h3 style="margin-bottom: 20px; color: var(--dark-color);">আজকের বাজার দর</h3>
                <div class="price-item">
                    <span>১ হালি (খুচরা)</span>
                    <span class="price-tag">৳ ৫০</span>
                </div>
                <div class="price-item">
                    <span>১ ডজন (ফ্যামিলি প্যাক)</span>
                    <span class="price-tag">৳ ১৫০</span>
                </div>
                <div class="price-item">
                    <span>১০০ টি (পাইকারি দর)</span>
                    <span class="price-tag">৳ ১,১৮০</span>
                </div>
                <p style="font-size: 12px; color: #888; margin-top: 15px;">*বাজারের পরিস্থিতি অনুযায়ী দাম সামান্য পরিবর্তিত হতে পারে।</p>
            </div>

            <div class="review-box">
                <h3 style="color: var(--dark-color);">আমাদের সম্মানিত গ্রাহক</h3>
                <div class="customer-card">
                    <p style="font-style: italic; color: #555;">
                        "আমি 'আমার আন্ডা' থেকে নিয়মিত ডিম নিচ্ছি। এদের ডিমের সাইজ যেমন বড়, কুসুমের রঙও একদম খাঁটি দেশি ডিমের মতো গাঢ় হলুদ। বাচ্চাদের প্রতিদিন নির্দ্বিধায় খাওয়াচ্ছি।"
                    </p>
                    <div class="customer-name">শাফিউর রহমান (Shafiur Rahman)</div>
                    <div class="customer-tag">🏆 প্রথম গ্রাহক (First Customer)</div>
                </div>
            </div>

        </div>
    </section>

    <section id="contact" class="contact-section">
        <h2 class="section-title">অর্ডার করতে আজই যোগাযোগ করুন</h2>
        <p>আপনার নাম ও মোবাইল নম্বর লিখে নিচে মেসেজ সাবমিট করুন।</p>
        <form class="contact-form" action="#" method="POST">
            <input type="text" placeholder="আপনার নাম" required>
            <input type="email" placeholder="আপনার ইমেইল বা মোবাইল নম্বর" required>
            <textarea rows="4" placeholder="আপনার প্রয়োজনীয় ডিমের পরিমাণ বা বার্তা লিখুন..." required></textarea>
            <button type="submit" class="btn" style="border:none; cursor:pointer; width: 100%;">অর্ডার কনফার্ম করুন</button>
        </form>
    </section>

    <footer>
        <p>&copy; 2026 আমার আন্ডা। সর্বস্বত্ব সংরক্ষিত।</p>
    </footer>

</body>
</html>