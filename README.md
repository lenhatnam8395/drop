<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CYBERTRON GEAR - Đồ Chơi Công Nghệ Tương Lai</title>
    <link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@400;600;800;900&family=Rajdhani:wght@500;600;700&display=swap" rel="stylesheet">
    
    <style>
        /* ==================== CẤU HÌNH BIẾN MÀU SẮC ==================== */
        :root {
            --bg-cyber: #06060a;
            --bg-card: #0f111a;
            --matrix-blue: #00f0ff;
            --bumblebee-yellow: #ffb700;
            --text-main: #e2e8f0;
            --text-gray: #718096;
            --font-tech: 'Orbitron', sans-serif;
            --font-body: 'Rajdhani', sans-serif;
        }

        /* RESET LỚP NỀN */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            scroll-behavior: smooth;
        }

        body {
            background-color: var(--bg-cyber);
            color: var(--text-main);
            font-family: var(--font-body);
            font-size: 18px;
            overflow-x: hidden;
            background-image: 
                linear-gradient(rgba(0, 240, 255, 0.03) 1px, transparent 1px),
                linear-gradient(90deg, rgba(0, 240, 255, 0.03) 1px, transparent 1px);
            background-size: 30px 30px;
        }

        /* ==================== THANH ĐIỀU HƯỚNG (HEADER) ==================== */
        header {
            width: 100%;
            padding: 15px 5%;
            background: rgba(6, 6, 10, 0.85);
            backdrop-filter: blur(10px);
            border-bottom: 2px solid rgba(0, 240, 255, 0.2);
            position: fixed;
            top: 0;
            z-index: 1000;
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
        }

        .logo {
            font-family: var(--font-tech);
            font-weight: 900;
            font-size: 1.5rem;
            color: var(--text-main);
            text-transform: uppercase;
            letter-spacing: 1px;
            display: flex;
            align-items: center;
            gap: 8px;
        }

        .logo span {
            color: var(--matrix-blue);
            text-shadow: 0 0 10px var(--matrix-blue);
        }

        nav {
            display: flex;
            gap: 20px;
            flex-wrap: wrap;
        }

        nav a {
            font-family: var(--font-tech);
            color: var(--text-main);
            text-decoration: none;
            font-size: 0.85rem;
            letter-spacing: 1px;
            transition: 0.3s;
            text-transform: uppercase;
            white-space: nowrap;
        }

        nav a:hover, nav a.active {
            color: var(--matrix-blue);
            text-shadow: 0 0 8px var(--matrix-blue);
        }

        /* ==================== PHẦN BANNER CHÍNH (HERO SECTION) ==================== */
        .hero {
            height: 100vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            padding: 0 20px;
            position: relative;
            margin-top: 60px;
        }

        .hero::before {
            content: '';
            position: absolute;
            top: 0; left: 0; width: 100%; height: 100%;
            background: linear-gradient(rgba(0,240,255,0) 95%, rgba(0,240,255,0.15) 98%, rgba(0,240,255,0) 100%);
            background-size: 100% 400%;
            animation: scanline 6s linear infinite;
            pointer-events: none;
        }

        @keyframes scanline {
            0% { background-position: 0% 0%; }
            100% { background-position: 0% 100%; }
        }

        .hero h1 {
            font-family: var(--font-tech);
            font-size: 3.2rem;
            font-weight: 900;
            text-transform: uppercase;
            letter-spacing: 3px;
            line-height: 1.2;
            margin-bottom: 20px;
            color: #ffffff;
            max-width: 100%;
        }

        .hero h1 span {
            color: transparent;
            -webkit-text-stroke: 1px var(--matrix-blue);
            filter: drop-shadow(0 0 10px rgba(0,240,255,0.6));
        }

        .hero p {
            font-size: 1.2rem;
            color: var(--text-gray);
            max-width: 600px;
            margin-bottom: 40px;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .btn-cyber {
            font-family: var(--font-tech);
            padding: 12px 30px;
            font-size: 0.95rem;
            font-weight: bold;
            color: #000000;
            background: var(--matrix-blue);
            border: none;
            cursor: pointer;
            text-transform: uppercase;
            letter-spacing: 1px;
            position: relative;
            clip-path: polygon(15px 0%, 100% 0%, 100% calc(100% - 15px), calc(100% - 15px) 100%, 0% 100%, 0% 15px);
            transition: 0.3s;
            box-shadow: 0 0 20px rgba(0, 240, 255, 0.4);
            max-width: 100%;
            white-space: normal;
        }

        .btn-cyber:hover {
            background: var(--bumblebee-yellow);
            box-shadow: 0 0 25px var(--bumblebee-yellow);
            transform: scale(1.05);
        }

        /* ==================== DANH MỤC SẢN PHẨM ==================== */
        .products-section {
            padding: 100px 5%;
            background: #090b11;
        }

        .section-title {
            font-family: var(--font-tech);
            text-align: center;
            font-size: 2.2rem;
            text-transform: uppercase;
            margin-bottom: 60px;
            letter-spacing: 2px;
            position: relative;
        }

        .section-title::after {
            content: '';
            display: block;
            width: 80px;
            height: 3px;
            background: var(--matrix-blue);
            margin: 15px auto 0;
            box-shadow: 0 0 10px var(--matrix-blue);
        }

        .grid-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
            gap: 30px;
            max-width: 1200px;
            margin: 0 auto;
        }

        .product-card {
            background: var(--bg-card);
            border: 1px solid rgba(0, 240, 255, 0.15);
            border-radius: 4px;
            padding: 20px;
            position: relative;
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            transition: all 0.4s ease;
            clip-path: polygon(0 0, calc(100% - 20px) 0, 100% 20px, 100% 100%, 20px 100%, 0 calc(100% - 20px));
        }

        .product-card:hover {
            border-color: var(--matrix-blue);
            box-shadow: 0 0 20px rgba(0, 240, 255, 0.25);
            transform: translateY(-5px);
        }

        .tech-badge {
            position: absolute;
            top: 15px;
            left: 15px;
            background: rgba(255, 183, 0, 0.15);
            border: 1px solid var(--bumblebee-yellow);
            color: var(--bumblebee-yellow);
            padding: 4px 8px;
            font-size: 0.7rem;
            font-family: var(--font-tech);
            text-transform: uppercase;
            letter-spacing: 1px;
            z-index: 2;
        }

        .product-img {
            width: 100%;
            height: 200px;
            object-fit: cover;
            background: #161925;
            border: 1px solid rgba(255,255,255,0.05);
            margin-bottom: 20px;
        }

        .product-title {
            font-family: var(--font-tech);
            font-size: 1.1rem;
            text-transform: uppercase;
            margin-bottom: 10px;
            color: #ffffff;
        }

        .product-desc {
            color: var(--text-gray);
            font-size: 0.95rem;
            line-height: 1.4;
            margin-bottom: 20px;
            flex-grow: 1;
        }

        .price-box {
            display: flex;
            justify-content: space-between;
            align-items: center;
            border-top: 1px dashed rgba(255,255,255,0.1);
            padding-top: 15px;
            flex-wrap: wrap;
            gap: 10px;
        }

        .price {
            font-family: var(--font-tech);
            font-size: 1.3rem;
            color: var(--matrix-blue);
            font-weight: bold;
        }

        .btn-buy {
            font-family: var(--font-tech);
            background: transparent;
            border: 1px solid var(--matrix-blue);
            color: var(--matrix-blue);
            padding: 8px 15px;
            font-size: 0.8rem;
            font-weight: bold;
            cursor: pointer;
            text-transform: uppercase;
            transition: 0.3s;
            clip-path: polygon(8px 0%, 100% 0%, 100% calc(100% - 8px), calc(100% - 8px) 100%, 0% 100%, 0% 8px);
        }

        .btn-buy:hover {
            background: rgba(0, 240, 255, 0.1);
            box-shadow: 0 0 12px var(--matrix-blue);
        }

        /* ==================== FOOTER ==================== */
        .footer-section {
            padding: 40px 5%;
            border-top: 2px solid rgba(0, 240, 255, 0.2);
            text-align: center;
            background: var(--bg-cyber);
            font-family: var(--font-tech);
            font-size: 0.85rem;
            color: var(--text-gray);
        }

        /* ==================== MODAL POPUP ==================== */
        .modal {
            display: none;
            position: fixed;
            top: 0; left: 0; width: 100%; height: 100%;
            background: rgba(0, 0, 0, 0.85);
            z-index: 2000;
            justify-content: center;
            align-items: center;
            backdrop-filter: blur(5px);
            padding: 15px;
        }

        .modal-content {
            background: var(--bg-card);
            border: 2px solid var(--matrix-blue);
            box-shadow: 0 0 30px var(--matrix-blue);
            padding: 30px 20px;
            max-width: 450px;
            width: 100%;
            text-align: center;
            position: relative;
            clip-path: polygon(20px 0%, 100% 0%, 100% calc(100% - 20px), calc(100% - 20px) 100%, 0% 100%, 0% 20px);
        }

        .modal-content h3 {
            font-family: var(--font-tech);
            color: #ffffff;
            margin-bottom: 15px;
            font-size: 1.2rem;
            text-transform: uppercase;
        }

        .modal-content p {
            margin-bottom: 25px;
            color: var(--text-gray);
            font-size: 0.95rem;
        }

        .btn-close {
            position: absolute;
            top: 10px; right: 15px;
            background: transparent; border: none;
            color: var(--text-gray); font-size: 1.5rem; cursor: pointer;
        }
        .btn-close:hover { color: var(--matrix-blue); }

        /* ==================== RESPONSIVE ==================== */
        @media (max-width: 900px) {
            header { flex-direction: column; padding: 15px 0; gap: 15px; }
            nav { justify-content: center; width: 100%; }
            .hero h1 { font-size: 2.5rem; }
        }

        @media (max-width: 600px) {
            nav { display: none; }
            .hero h1 { font-size: 2rem; }
            .hero p { font-size: 1rem; }
            .section-title { font-size: 1.8rem; }
            .product-card { padding: 15px; }
            .price { font-size: 1.2rem; }
            .modal-content { padding: 25px 15px; }
        }
    </style>
</head>
<body>

    <header>
        <div class="logo">CYBERTRON <span>GEAR</span></div>
        <nav>
            <a href="#home" class="active">Hệ Thống</a>
            <a href="#products">Kho Vũ Khí</a>
            <a href="https://zalo.me/0383748395" target="_blank">Kết Nối</a>
        </nav>
    </header>

    <section class="hero" id="home">
        <h1>NÂNG CẤP CHIẾN GIÁP <span>CÔNG NGHỆ</span></h1>
        <p>Kho đồ chơi tối tân tối ưu hóa không gian làm việc và khoang lái của bạn</p>
        <button class="btn-cyber" onclick="scrollToProducts()">Kích Hoạt Ngay</button>
    </section>

    <section class="products-section" id="products">
        <h2 class="section-title">THIẾT BỊ HIỆN DIỆN</h2>
        
        <div class="grid-container">
            <div class="product-card">
                <span class="tech-badge">Năng Lượng 100%</span>
                <img src="https://images.unsplash.com/photo-1555538995-73ee16a133f1?auto=format&fit=crop&w=400&q=80" alt="Đèn LED Trụ" class="product-img">
                <div>
                    <h3 class="product-title">Đèn Tháp LED RGB MATRIX</h3>
                    <p class="product-desc">Cảm biến sóng âm theo nhịp nhạc siêu nhạy. Kiến tạo không gian Cyberpunk cốt lõi cho góc máy.</p>
                </div>
                <div class="price-box">
                    <span class="price">350.000đ</span>
                    <button class="btn-buy" onclick="triggerOrder('Đèn Tháp LED RGB MATRIX')">Nạp Gear</button>
                </div>
            </div>

            <div class="product-card">
                <span class="tech-badge">Best Seller</span>
                <img src="https://images.unsplash.com/photo-1508962914676-134849a727f0?auto=format&fit=crop&w=400&q=80" alt="Đồng hồ Nixie" class="product-img">
                <div>
                    <h3 class="product-title">Đồng Hồ LED Bán Dẫn</h3>
                    <p class="product-desc">Mô phỏng hệ thống ống đèn phát quang cơ khí cổ điển. Linh hồn của một dân chơi công nghệ thứ thiệt.</p>
                </div>
                <div class="price-box">
                    <span class="price">1.250.000đ</span>
                    <button class="btn-buy" onclick="triggerOrder('Đồng Hồ LED Bán Dẫn')">Nạp Gear</button>
                </div>
            </div>

            <div class="product-card">
                <span class="tech-badge">Limited Edition</span>
                <img src="https://images.unsplash.com/photo-1617814076367-b759c7d7e738?auto=format&fit=crop&w=400&q=80" alt="Nước hoa phi thuyền" class="product-img">
                <div>
                    <h3 class="product-title">Phi Thuyền Khuếch Tán</h3>
                    <p class="product-desc">Nước hoa cao cấp đặt taplo xe hơi. Cánh quạt tua-bin tự quay bằng động cơ năng lượng mặt trời.</p>
                </div>
                <div class="price-box">
                    <span class="price">290.000đ</span>
                    <button class="btn-buy" onclick="triggerOrder('Phi Thuyền Khuếch Tán')">Nạp Gear</button>
                </div>
            </div>

            <div class="product-card">
                <span class="tech-badge">Tương Thích Cao</span>
                <img src="https://images.unsplash.com/photo-1563720223185-11003d516935?auto=format&fit=crop&w=400&q=80" alt="Sạc không dây Magsafe" class="product-img">
                <div>
                    <h3 class="product-title">Kẹp Sạc MagSafe Sò Lạnh</h3>
                    <p class="product-desc">Tích hợp tản nhiệt sò lạnh làm mát máy siêu tốc, tích hợp đèn LED báo trạng thái sạc cho khoang lái.</p>
                </div>
                <div class="price-box">
                    <span class="price">490.000đ</span>
                    <button class="btn-buy" onclick="triggerOrder('Kẹp Sạc MagSafe Sò Lạnh')">Nạp Gear</button>
                </div>
            </div>
        </div>
    </section>

    <footer class="footer-section" id="contact">
        <p>© 2026 CYBERTRON GEAR CORE SYSTEM. ALL RIGHTS RESERVED.</p>
        <p style="font-size: 0.75rem; color:#4a5568; margin-top: 10px;">Hệ thống phân phối Dropshipping đồ chơi công nghệ tối tân.</p>
    </footer>

    <div class="modal" id="orderModal">
        <div class="modal-content">
            <button class="btn-close" onclick="closeModal()">✕</button>
            <h3 id="modalProductTitle">THIẾT BỊ ĐÃ KHỞI ĐỘNG</h3>
            <p>Hệ thống đang điều hướng bạn đến kênh hỗ trợ Zalo cá nhân để xử lý đóng gói và bàn giao COD bảo mật.</p>
            <a href="#" id="zaloLink" target="_blank">
                <button class="btn-cyber">Kết Nối Tổng Kho</button>
            </a>
        </div>
    </div>

    <script>
        function scrollToProducts() {
            document.getElementById('products').scrollIntoView();
        }

        function triggerOrder(productName) {
            document.getElementById('modalProductTitle').innerText = "KÍCH HOẠT: " + productName;
            
            /* SỬA ĐỔI 2: Đưa số điện thoại Zalo của bạn vào sự kiện click để nhảy trực tiếp khi bấm nút trong Modal */
            document.getElementById('zaloLink').href = "https://zalo.me/0383748395"; 
            
            document.getElementById('orderModal').style.display = 'flex';
        }

        function closeModal() {
            document.getElementById('orderModal').style.display = 'none';
        }

        window.onclick = function(event) {
            let modal = document.getElementById('orderModal');
            if (event.target == modal) {
                modal.style.display = "none";
            }
        }
    </script>
</body>
</html>
