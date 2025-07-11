<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>DIGITAL EBOOK</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        /* Reset & Base Styles */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', system-ui, -apple-system, sans-serif;
        }
        
        body {
            /* Background Gradient Elegant */
            background: linear-gradient(135deg, #f5f7fa 0%, #e4e8f0 100%);
            color: #333;
            line-height: 1.6;
            overflow-x: hidden;
            min-height: 100vh;
            position: relative;
        }
        
        /* Efek geometri modern di background */
        body::before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 60vh;
            background: linear-gradient(45deg, rgba(0, 113, 227, 0.03) 0%, rgba(0, 161, 230, 0.05) 100%);
            clip-path: polygon(0 0, 100% 0, 100% 85%, 0% 100%);
            z-index: -1;
        }
        
        .container {
            max-width: 600px;
            margin: 0 auto;
            padding: 20px;
            width: 100%;
        }
        
        /* Header Styles */
   .profile {
       text-align: center;
       margin: 0 auto 30px;
       max-width: 90%;
       display: flex;
       flex-direction: column;
       align-items: center;
   }
   
   .profile-img {
       width: 120px;
       height: 120px;
       border-radius: 50%;
       object-fit: cover;
       border: 4px solid #fff;
       box-shadow: 0 4px 20px rgba(0, 0, 0, 0.12);
       margin-bottom: 20px;
   }
   
   .profile h1 {
       font-size: 24px;
       font-weight: 700;
       margin-bottom: 10px;
       color: #222;
   }
   
   .profile p {
       color: #666;
       font-size: 16px;
       max-width: 100%;
       margin: 0 auto;
       line-height: 1.5;
       padding: 0 15px;
   }
        
        /* Links Styles */
        .links {
            display: flex;
            flex-direction: column;
            gap: 15px;
            margin-bottom: 30px;
        }
        
        .link-item {
            background-color: rgba(255, 255, 255, 0.9);
            backdrop-filter: blur(5px);
            -webkit-backdrop-filter: blur(5px);
            border-radius: 12px;
            padding: 15px 20px;
            display: flex;
            align-items: center;
            text-decoration: none;
            color: #333;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.08);
            transition: all 0.3s ease;
            border: 1px solid rgba(255, 255, 255, 0.3);
            position: relative;
            overflow: hidden;
        }
        
        .link-item::before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            width: 3px;
            height: 100%;
            background: linear-gradient(to bottom, #0071e3, #00a1e6);
            transition: width 0.3s ease;
        }
        
        .link-item:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 25px rgba(0, 113, 227, 0.15);
        }
        
        .link-item:hover::before {
            width: 5px;
        }
        
        .link-icon {
            width: 40px;
            height: 40px;
            background: linear-gradient(135deg, rgba(0, 113, 227, 0.1) 0%, rgba(0, 161, 230, 0.1) 100%);
            border-radius: 10px;
            display: flex;
            align-items: center;
            justify-content: center;
            margin-right: 15px;
            flex-shrink: 0;
            color: #0071e3;
            font-size: 18px;
            transition: all 0.3s ease;
        }
        
        .link-item:hover .link-icon {
            background: linear-gradient(135deg, rgba(0, 113, 227, 0.2) 0%, rgba(0, 161, 230, 0.2) 100%);
            transform: scale(1.05);
        }
        
        .link-text {
            flex-grow: 1;
        }
        
        .link-text h3 {
            font-size: 16px;
            font-weight: 600;
            margin-bottom: 3px;
        }
        
        .link-text p {
            font-size: 13px;
            color: #888;
        }
        
        /* Promo Banner */
        .promo-banner {
            background: linear-gradient(135deg, #0071e3 0%, #00a1e6 100%);
            color: white;
            padding: 15px;
            border-radius: 12px;
            margin-bottom: 20px;
            text-align: center;
            font-weight: 600;
            box-shadow: 0 4px 15px rgba(0, 113, 227, 0.25);
            position: relative;
            overflow: hidden;
        }
        
        .promo-banner::after {
            content: "";
            position: absolute;
            top: -50%;
            right: -50%;
            width: 100%;
            height: 200%;
            background: radial-gradient(circle, rgba(255,255,255,0.15) 0%, rgba(255,255,255,0) 70%);
            transform: rotate(30deg);
        }
        
        /* Social Links */
        .social-links {
            display: flex;
            justify-content: center;
            gap: 15px;
            margin-top: 30px;
        }
        
        .social-link {
            width: 45px;
            height: 45px;
            border-radius: 50%;
            background-color: rgba(255, 255, 255, 0.9);
            backdrop-filter: blur(5px);
            -webkit-backdrop-filter: blur(5px);
            display: flex;
            align-items: center;
            justify-content: center;
            color: #555;
            font-size: 20px;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.08);
            transition: all 0.3s ease;
            border: 1px solid rgba(255, 255, 255, 0.3);
        }
        
        .social-link:hover {
            transform: translateY(-3px) scale(1.1);
            box-shadow: 0 6px 15px rgba(0, 0, 0, 0.12);
            color: #0071e3;
        }
        
        .footer {
            text-align: center;
            margin-top: 30px;
            color: #999;
            font-size: 13px;
            opacity: 0.8;
        }
        
        /* Animasi subtle untuk kesan premium */
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(10px); }
            to { opacity: 1; transform: translateY(0); }
        }
        
        .container {
            animation: fadeIn 0.6s ease-out;
        }
        
        /* Responsive Adjustments */
        @media (max-width: 480px) {
            .container {
                padding: 15px;
            }
            
            .profile-img {
                width: 100px;
                height: 100px;
            }
            
            .profile h1 {
                font-size: 22px;
            }
            
            .profile p {
                font-size: 15px;
                max-width: 90%;
            }
            
            .link-item {
                padding: 12px 15px;
            }
            
            .link-icon {
                width: 36px;
                height: 36px;
                font-size: 16px;
                margin-right: 12px;
            }
            
            body::before {
                height: 50vh;
                clip-path: polygon(0 0, 100% 0, 100% 90%, 0% 100%);
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- Profile Section -->
        <div class="profile">
            <img src="profil.png" alt="Profile" class="profile-img">
            <h1>DigitalEbook</h1>
            <p>silahkan lihat-lihat produk yang sangat bagus dan bisa untuk di jual kembali langsung cek sekarang dan segera dapatkan E-book gratis download sekarang!</p>
        </div>
        
        <!-- Promo Banner -->
        <div class="promo-banner">
            🚀 Gratis Ongkir + Cashback 10% hingga 31 Desember 2023!
        </div>
        
        <!-- Links Section -->
        <div class="links">
            <a href="https://wa.me/6282225921652" class="link-item" target="_blank">
                <div class="link-icon">
                    <i class="fab fa-whatsapp"></i>
                </div>
                <div class="link-text">
                    <h3>Order via WhatsApp</h3>
                    <p>Respon cepat 24 jam, klik untuk chat langsung</p>
                </div>
            </a>
            
            <a href="https://lynk.id/geminicuyyy" class="link-item" target="_blank">
                <div class="link-icon">
                    <i class="fas fa-store"></i>
                </div>
                <div class="link-text">
                    <h3>Lynk.id</h3>
                    <p>cek sekarang produk yang anda butuhkan disini</p>
                </div>
            </a>
            
            <a href="https://drive.google.com/file/d/1Yjsi20reI_Ypr6BBaVsLLAcnaaPaJ_kR/view?usp=drivesdk" class="link-item" target="_blank">
                <div class="link-icon">
                    <i class="fas fa-shopping-bag"></i>
                </div>
                <div class="link-text">
                    <h3>download ebook gratis</h3>
                    <p>E-book 99 Langkah suksek berbisnis E-commerce</p>
                </div>
            </a>
        </div>
        

        
        <!-- Footer -->
        <div class="footer">
            © 2023 DIGITAL E-BOOK. All rights reserved.
        </div>
    </div>
    
    <script>
        // Efek hover yang lebih smooth
        document.querySelectorAll('.link-item').forEach(link => {
            link.addEventListener('mouseenter', function() {
                this.style.transform = 'translateY(-5px)';
            });
            
            link.addEventListener('mouseleave', function() {
                this.style.transform = 'translateY(0)';
            });
        });
        
        // Animasi saat halaman dimuat
        document.addEventListener('DOMContentLoaded', () => {
            const links = document.querySelectorAll('.link-item');
            links.forEach((link, index) => {
                link.style.animationDelay = `${index * 0.1}s`;
            });
        });
    </script>
</body>
</html>
