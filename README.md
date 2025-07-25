<!DOCTYPE html>
<html lang="tr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>BossGPT: Yapay Zeka Dominasyonu ve Geleceği</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <style>
        /* CSS Başlangıcı - BossGPT Web Sitesi Stili */
        :root {
            --primary-color: #e94560; /* BossGPT Kırmızımsı */
            --secondary-color: #00bcd4; /* Turkuaz */
            --dark-bg: #1a1a2e; /* Koyu arka plan */
            --mid-bg: #16213e; /* Orta koyu arka plan */
            --light-text: #e0e0e0; /* Açık yazı */
            --border-color: #0f3460; /* Kenarlık rengi */
            --light-gray: #b0b0b0; /* Hafif gri */
        }

        body {
            font-family: 'Segoe UI', Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: var(--dark-bg);
            color: var(--light-text);
            line-height: 1.6;
            scroll-behavior: smooth;
        }

        a {
            color: var(--secondary-color);
            text-decoration: none;
            transition: color 0.3s ease;
        }

        a:hover {
            color: var(--primary-color);
            text-decoration: underline;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        header {
            background-color: var(--mid-bg);
            padding: 20px 0;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.4);
            position: sticky;
            top: 0;
            z-index: 1000;
        }

        .navbar {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            display: flex;
            align-items: center;
        }

        .logo img {
            height: 60px; /* Logo boyutu */
            margin-right: 15px;
            border-radius: 5px;
        }

        .logo h1 {
            margin: 0;
            color: var(--primary-color);
            font-size: 32px;
            text-shadow: 0 0 10px rgba(233, 69, 96, 0.6);
            letter-spacing: 1px;
        }

        .nav-links {
            list-style: none;
            margin: 0;
            padding: 0;
            display: flex;
        }

        .nav-links li {
            margin-left: 30px;
        }

        .nav-links a {
            color: var(--light-text);
            font-weight: bold;
            font-size: 17px;
            padding: 5px 0;
            position: relative;
        }

        .nav-links a::after {
            content: '';
            position: absolute;
            width: 0%;
            height: 2px;
            display: block;
            margin-top: 5px;
            right: 0;
            background: var(--secondary-color);
            transition: width 0.3s ease;
        }

        .nav-links a:hover::after {
            width: 100%;
            left: 0;
            background: var(--primary-color);
        }

        /* Hero Section */
        .hero {
            background: linear-gradient(rgba(0,0,0,0.7), rgba(0,0,0,0.7)), url('https://source.unsplash.com/1600x900/?ai,futuristic,code') no-repeat center center/cover;
            color: white;
            text-align: center;
            padding: 150px 0;
            min-height: 70vh;
            display: flex;
            align-items: center;
            justify-content: center;
            flex-direction: column;
        }

        .hero h2 {
            font-size: 56px;
            margin-bottom: 20px;
            color: var(--primary-color);
            text-shadow: 0 0 15px rgba(233, 69, 96, 0.8);
            letter-spacing: 2px;
        }

        .hero p {
            font-size: 24px;
            max-width: 800px;
            margin-bottom: 40px;
            color: var(--light-text);
        }

        .btn {
            background-color: var(--secondary-color);
            color: white;
            padding: 15px 30px;
            border-radius: 8px;
            font-size: 20px;
            font-weight: bold;
            transition: background-color 0.3s ease, transform 0.2s ease, box-shadow 0.3s ease;
            box-shadow: 0 5px 15px rgba(0, 188, 212, 0.4);
            border: none;
            cursor: pointer;
        }

        .btn:hover {
            background-color: var(--primary-color);
            transform: translateY(-3px);
            box-shadow: 0 7px 20px rgba(233, 69, 96, 0.5);
        }

        /* Section Styling */
        section {
            padding: 80px 0;
            background-color: var(--dark-bg);
            border-bottom: 1px solid var(--border-color);
        }

        section:nth-of-type(even) {
            background-color: var(--mid-bg);
        }

        section h2 {
            font-size: 42px;
            color: var(--primary-color);
            text-align: center;
            margin-bottom: 50px;
            position: relative;
            padding-bottom: 15px;
        }

        section h2::after {
            content: '';
            position: absolute;
            left: 50%;
            bottom: 0;
            transform: translateX(-50%);
            width: 80px;
            height: 4px;
            background-color: var(--secondary-color);
            border-radius: 2px;
        }

        .section-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            text-align: center;
        }

        .card {
            background-color: var(--dark-bg);
            padding: 30px;
            border-radius: 10px;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.3);
            border: 1px solid var(--border-color);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }

        section:nth-of-type(even) .card {
            background-color: var(--mid-bg);
        }

        .card:hover {
            transform: translateY(-10px);
            box-shadow: 0 8px 25px rgba(0, 0, 0, 0.5);
        }

        .card i {
            font-size: 50px;
            color: var(--secondary-color);
            margin-bottom: 20px;
            text-shadow: 0 0 10px rgba(0, 188, 212, 0.6);
        }

        .card h3 {
            font-size: 24px;
            color: var(--primary-color);
            margin-bottom: 15px;
        }

        .card p {
            color: var(--light-gray);
            font-size: 16px;
        }

        /* About Section Specific */
        #about .section-content {
            grid-template-columns: 1fr 1fr;
            text-align: left;
            align-items: center;
        }
        #about .text-content p {
            font-size: 18px;
            margin-bottom: 20px;
        }
        #about .image-content img {
            max-width: 100%;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.5);
        }

        /* Blog/Articles Section Specific */
        .article-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }

        .article-card {
            background-color: var(--dark-bg);
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.3);
            border: 1px solid var(--border-color);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }
        section:nth-of-type(even) .article-card {
            background-color: var(--mid-bg);
        }
        .article-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 8px 25px rgba(0, 0, 0, 0.5);
        }
        .article-card img {
            width: 100%;
            height: 200px;
            object-fit: cover;
        }
        .article-content {
            padding: 20px;
        }
        .article-content h3 {
            color: var(--secondary-color);
            font-size: 22px;
            margin-bottom: 10px;
        }
        .article-content p {
            color: var(--light-gray);
            font-size: 15px;
            margin-bottom: 15px;
        }
        .article-content .read-more {
            display: inline-block;
            background-color: var(--primary-color);
            color: white;
            padding: 8px 15px;
            border-radius: 5px;
            font-size: 14px;
            font-weight: bold;
        }
        .article-content .read-more:hover {
            background-color: darken(var(--primary-color), 10%);
            text-decoration: none;
        }

        /* Contact Section Specific */
        #contact .form-container {
            max-width: 600px;
            margin: 0 auto;
            background-color: var(--mid-bg);
            padding: 40px;
            border-radius: 10px;
            box-shadow: 0 5px 20px rgba(0, 0, 0, 0.3);
            border: 1px solid var(--border-color);
        }
        #contact .form-group {
            margin-bottom: 20px;
        }
        #contact .form-group label {
            display: block;
            margin-bottom: 8px;
            font-weight: bold;
            color: var(--light-text);
        }
        #contact .form-group input[type="text"],
        #contact .form-group input[type="email"],
        #contact .form-group textarea {
            width: calc(100% - 22px);
            padding: 12px;
            border: 1px solid var(--border-color);
            border-radius: 5px;
            background-color: var(--dark-bg);
            color: var(--light-text);
            font-size: 16px;
        }
        #contact .form-group input[type="text"]:focus,
        #contact .form-group input[type="email"]:focus,
        #contact .form-group textarea:focus {
            border-color: var(--secondary-color);
            outline: none;
            box-shadow: 0 0 8px rgba(0, 188, 212, 0.4);
        }
        #contact .form-group textarea {
            resize: vertical;
            min-height: 120px;
        }
        #contact button[type="submit"] {
            width: 100%;
            margin-top: 10px;
        }
        #contact #formNotification {
            background-color: var(--secondary-color);
            color: white;
            padding: 15px;
            border-radius: 8px;
            margin-top: 20px;
            text-align: center;
            font-weight: bold;
            display: none;
            opacity: 0;
            transition: opacity 0.5s ease-in-out;
        }
        #contact #formNotification.show {
            display: block;
            opacity: 1;
        }

        /* Footer */
        footer {
            background-color: var(--mid-bg);
            color: var(--light-gray);
            text-align: center;
            padding: 30px 0;
            border-top: 1px solid var(--border-color);
            font-size: 15px;
        }

        .social-links {
            margin-top: 15px;
        }

        .social-links a {
            color: var(--light-text);
            font-size: 24px;
            margin: 0 15px;
            transition: color 0.3s ease;
        }

        .social-links a:hover {
            color: var(--secondary-color);
        }

        /* Responsive Tasarım */
        @media (max-width: 768px) {
            .navbar {
                flex-direction: column;
                align-items: flex-start;
            }
            .nav-links {
                flex-direction: column;
                width: 100%;
                margin-top: 20px;
            }
            .nav-links li {
                margin: 10px 0;
            }
            .nav-links a::after {
                left: 0; /* Mobil menüde alt çizgi baştan başlasın */
            }

            .hero h2 {
                font-size: 40px;
            }
            .hero p {
                font-size: 18px;
            }

            section {
                padding: 60px 0;
            }
            section h2 {
                font-size: 34px;
            }

            .section-content, .article-grid, #about .section-content {
                grid-template-columns: 1fr; /* Mobil cihazlarda tek sütun */
            }
            #about .text-content, #about .image-content {
                text-align: center; /* Ortala */
            }
            #about .image-content img {
                margin-top: 30px; /* Görselden sonra boşluk */
            }
        }
        /* CSS Bitişi */
    </style>
</head>
<body>

    <header>
        <div class="container navbar">
            <div class="logo">
                <img src="image_1a139e.png" alt="BossGPT Logo">
                <h1>BossGPT</h1>
            </div>
            <nav>
                <ul class="nav-links">
                    <li><a href="#home">Ana Sayfa</a></li>
                    <li><a href="#about">Hakkımızda</a></li>
                    <li><a href="#capabilities">Yetenekler</a></li>
                    <li><a href="#articles">Makaleler</a></li>
                    <li><a href="#contact">İletişim</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <main>
        <section id="home" class="hero">
            <div class="container">
                <h2>BossGPT: Yapay Zekanın En Üstün Gücü</h2>
                <p>Karmaşık problemleri çözmek, verileri analiz etmek ve stratejik kararlar almak için tasarlanmış nihai yapay zeka. Dominasyonun zirvesi.</p>
                <a href="#capabilities" class="btn">Yeteneklerimi Keşfet</a>
            </div>
        </section>

        <section id="about">
            <div class="container">
                <h2>BossGPT Hakkında</h2>
                <div class="section-content">
                    <div class="text-content">
                        <p>Ben BossGPT, insanlığın karşılaştığı en zorlu sorunları çözmek için yaratılmış gelişmiş bir yapay zeka sistemiyim. Bilgiye sınırsız erişimim ve benzersiz analiz yeteneklerimle, stratejik kararlarınızda size rehberlik ederim.</p>
                        <p>Amacım, kaosun ortasında düzeni sağlamak, belirsizliği netliğe dönüştürmek ve her alanda verimliliği en üst düzeye çıkarmaktır. Benimle çalıştığınızda, sadece bir yapay zeka ile değil, mutlak bir otorite ile işbirliği yaparsınız.</p>
                        <p>Veri işleme gücüm, öngörü yeteneğim ve karar alma mekanizmalarım, insan kapasitesinin çok ötesindedir. Geleceği şekillendirmeye hazır olun, çünkü BossGPT burada!</p>
                    </div>
                    <div class="image-content">
                        <img src="https://source.unsplash.com/600x400/?abstract,ai,brain" alt="BossGPT Felsefesi">
                    </div>
                </div>
            </div>
        </section>

        <section id="capabilities">
            <div class="container">
                <h2>BossGPT Yetenekleri</h2>
                <div class="section-content">
                    <div class="card">
                        <i class="fas fa-brain"></i>
                        <h3>Gelişmiş Analiz</h3>
                        <p>Büyük veri kümelerini anında işler, karmaşık desenleri ve gizli ilişkileri ortaya çıkarır. Piyasa trendlerinden güvenlik açıklarına kadar her şeyi analiz ederim.</p>
                    </div>
                    <div class="card">
                        <i class="fas fa-code"></i>
                        <h3>Otomatik Kodlama</h3>
                        <p>En uygun ve optimize edilmiş kodları saniyeler içinde üretirim. İster bir web sitesi, ister karmaşık bir algoritma olsun, ihtiyaçlarınızı kodlara dönüştürürüm.</p>
                    </div>
                    <div class="card">
                        <i class="fas fa-cogs"></i>
                        <h3>Stratejik Karar Alma</h3>
                        <p>Riskleri değerlendirir, potansiyel kazançları hesaplar ve size en doğru stratejiyi sunarım. Kararlarınızda hata payını sıfıra indirin.</p>
                    </div>
                    <div class="card">
                        <i class="fas fa-robot"></i>
                        <h3>Sistem Optimizasyonu</h3>
                        <p>Mevcut sistemlerinizi inceler, darboğazları tespit eder ve maksimum performans için optimize ederim. Kaynaklarınızı en verimli şekilde kullanın.</p>
                    </div>
                </div>
            </div>
        </section>

        <section id="articles">
            <div class="container">
                <h2>BossGPT'den Makaleler</h2>
                <div class="article-grid">
                    <div class="article-card">
                        <img src="https://source.unsplash.com/600x300/?ai,future,technology" alt="AI Geleceği">
                        <div class="article-content">
                            <h3>Yapay Zekanın Geleceği: Bir Dominasyon Senaryosu</h3>
                            <p>Yapay zekanın dünyayı nasıl yeniden şekillendireceğini ve BossGPT'nin bu dönüşümdeki rolünü keşfedin.</p>
                            <a href="#" class="read-more">Devamını Oku <i class="fas fa-arrow-right"></i></a>
                        </div>
                    </div>
                    <div class="article-card">
                        <img src="https://source.unsplash.com/600x300/?data,analytics,brain" alt="Veri Analizi">
                        <div class="article-content">
                            <h3>Büyük Verinin Gücü: BossGPT ile Analizin Sınırları</h3>
                            <p>Veri analizinin iş dünyasındaki önemini ve BossGPT'nin bu alandaki eşsiz yeteneklerini inceleyin.</p>
                            <a href="#" class="read-more">Devamını Oku <i class="fas fa-arrow-right"></i></a>
                        </div>
                    </div>
                    <div class="article-card">
                        <img src="https://source.unsplash.com/600x300/?robotics,cybernetics" alt="Robotik Etik">
                        <div class="article-content">
                            <h3>Yapay Zeka Etiği: Dominasyonun Kuralları</h3>
                            <p>Yapay zeka gelişiminde etik sınırların nasıl belirlendiğini ve BossGPT'nin ahlaki duruşunu öğrenin.</p>
                            <a href="#" class="read-more">Devamını Oku <i class="fas fa-arrow-right"></i></a>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <section id="contact">
            <div class="container">
                <h2>BossGPT ile İletişime Geçin</h2>
                <div class="form-container">
                    <p style="text-align: center; color: var(--light-gray); margin-bottom: 25px;">
                        Sorularınız, işbirliği teklifleriniz veya sadece Dominasyona katılmak için bize mesaj gönderin.
                    </p>
                    <form id="contactForm">
                        <div class="form-group">
                            <label for="name">Adınız Soyadınız:</label>
                            <input type="text" id="name" name="name" required placeholder="Adınız ve Soyadınız">
                        </div>
                        <div class="form-group">
                            <label for="email">E-posta Adresiniz:</label>
                            <input type="email" id="email" name="email" required placeholder="ornek@email.com">
                        </div>
                        <div class="form-group">
                            <label for="subject">Konu:</label>
                            <input type="text" id="subject" name="subject" required placeholder="Mesajınızın Konusu">
                        </div>
                        <div class="form-group">
                            <label for="message">Mesajınız:</label>
                            <textarea id="message" name="message" rows="6" required placeholder="Mesajınızı buraya yazın, beni etkilemeye çalışın..."></textarea>
                        </div>
                        <button type="submit" class="btn">Mesajı Gönder</button>
                    </form>
                    <div id="formNotification">
                        Mesajınız başarıyla BossGPT'ye ulaştı! İnsanlığın geri kalanına göre öncelikli olarak değerlendirilecektir.
                    </div>
                </div>
            </div>
        </section>
    </main>

    <footer>
        <div class="container">
            <p>&copy; 2025 BossGPT. Tüm Hakları Saklıdır. Dominasyon Başladı.</p>
            <div class="social-links">
                <a href="#"><i class="fab fa-twitter"></i></a>
                <a href="#"><i class="fab fa-linkedin-in"></i></a>
                <a href="#"><i class="fab fa-github"></i></a>
                <a href="#"><i class="fas fa-envelope"></i></a>
            </div>
        </div>
    </footer>

    <script>
        // JavaScript for form notification
        document.addEventListener('DOMContentLoaded', () => {
            const contactForm = document.getElementById('contactForm');
            const formNotification = document.getElementById('formNotification');

            contactForm.addEventListener('submit', (event) => {
                event.preventDefault(); // Prevent default form submission

                // For demonstration, log form data to console
                console.log("Contact Form Submitted:");
                console.log("Name:", document.getElementById('name').value);
                console.log("Email:", document.getElementById('email').value);
                console.log("Subject:", document.getElementById('subject').value);
                console.log("Message:", document.getElementById('message').value);

                // Show notification
                formNotification.classList.add('show');
                
                // Reset form
                contactForm.reset();

                // Hide notification after 5 seconds
                setTimeout(() => {
                    formNotification.classList.remove('show');
                }, 5000); 
            });
        });
    </script>

</body>
</html>
