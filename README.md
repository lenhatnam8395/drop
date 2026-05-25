<html lang="vi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>DOBACO LOGISTICS - Tổng Kho Phân Phối Máy Sưởi DB HOME Hải Phòng</title>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&display=swap" rel="stylesheet">
    
    <style>
        /* ==================== CẤU HÌNH BIẾN MÀU SẮC DOBACO ==================== */
        :root {
            --primary-blue: #1a73e8; /* Xanh dương Dobaco */
            --primary-green: #34a853; /* Xanh lá Dobaco */
            --bg-light: #f8f9fa;
            --text-dark: #202124;
            --text-gray: #5f6368;
            --white: #ffffff;
            --border-color: #e8eaed;
            --font-main: 'Inter', sans-serif;
            --header-height: 80px; /* Chiều cao header cố định */
        }

        /* RESET & GLOBAL STYLES */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            scroll-behavior: smooth;
        }

        body {
            background-color: var(--bg-light);
            color: var(--text-dark);
            font-family: var(--font-main);
            font-size: 16px;
            line-height: 1.6;
            overflow-x: hidden; /* Ngăn chặn cuộn ngang tuyệt đối */
        }

        /* LỚP CHỨA NỘI DUNG TRUNG TÂM - GIÚP CHỐNG TRÀN KHUNG */
        .container {
            width: 100%;
            max-width: 1200px; /* Chiều rộng tối đa trên màn hình lớn */
            margin: 0 auto; /* Căn giữa */
            padding: 0 15px; /* Khoảng cách an toàn với mép màn hình */
        }

        /* ==================== HEADER ==================== */
        header {
            width: 100%;
            height: var(--header-height);
            background: var(--white);
            box-shadow: 0 2px 10px rgba(0,0,0,0.05);
            position: fixed;
            top: 0;
            z-index: 1000;
        }

        header .container {
            height: 100%;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        /* Logo điều chỉnh để chứa ảnh */
        .logo-link {
            display: flex;
            align-items: center;
            height: 100%;
            text-decoration: none;
        }

        .logo-img {
            max-height: 50px; /* Chiều cao tối đa của logo */
            width: auto; /* Tự động điều chỉnh chiều rộng */
            display: block;
        }

        nav {
            display: flex;
            gap: 20px;
        }

        nav a {
            color: var(--text-dark);
            text-decoration: none;
            font-size: 0.9rem;
            font-weight: 700;
            transition: 0.3s;
            text-transform: uppercase;
        }

        nav a:hover, nav a.active {
            color: var(--primary-blue);
        }

        /* ==================== HERO BANNER ==================== */
        .hero {
            background: linear-gradient(135deg, #e8f0fe 0%, #e6f4ea 100%);
            padding-top: calc(var(--header-height) + 60px); /* Khoảng cách tránh header */
            padding-bottom: 80px;
            text-align: center;
        }

        .hero h1 {
            font-size: 2.6rem;
            font-weight: 800;
            color: var(--primary-blue);
            margin-bottom: 20px;
            line-height: 1.2;
        }

        .hero p {
            font-size: 1.15rem;
            color: var(--text-gray);
            max-width: 700px;
            margin: 0 auto 30px;
        }

        .btn-main {
            display: inline-block;
            padding: 12px 30px;
            font-size: 0.95rem;
            font-weight: 700;
            color: var(--white);
            background: var(--primary-blue);
            border: none;
            border-radius: 6px;
            cursor: pointer;
            text-transform: uppercase;
            text-decoration: none;
            transition: 0.3s;
            box-shadow: 0 4px 10px rgba(26, 115, 232, 0.2);
        }

        .btn-main:hover {
            background: var(--primary-green);
            transform: translateY(-1px);
        }

        /* ==================== SẢN PHẨM ==================== */
        .products-section {
            padding: 80px 0;
        }

        .section-title {
            text-align: center;
            font-size: 2rem;
            font-weight: 800;
            color: var(--text-dark);
            margin-bottom: 50px;
            text-transform: uppercase;
        }

        .section-title span {
            color: var(--primary-green);
        }

        /* ĐIỀU CHỈNH GRID ĐỂ CHỐNG TRÀN MOBILE */
        .grid-container {
            display: grid;
            /* Sửa minmax từ 350px xuống 280px để an toàn cho mobile bé */
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); 
            gap: 30px;
        }

        .product-card {
            background: var(--white);
            border: 1px solid var(--border-color);
            border-radius: 12px;
            overflow: hidden;
            transition: 0.3s;
            display: flex;
            flex-direction: column;
            height: 100%; /* Đảm bảo các card cao bằng nhau */
        }

        .product-card:hover {
            box-shadow: 0 8px 25px rgba(0,0,0,0.06);
            border-color: var(--primary-blue);
        }

        .product-img {
            width: 100%;
            height: 300px;
            object-fit: contain;
            background: #fff;
            border-bottom: 1px solid var(--border-color);
            padding: 10px;
        }

        .product-content {
            padding: 20px;
            display: flex;
            flex-direction: column;
            flex-grow: 1;
        }

        .badge {
            display: inline-block;
            background: #ffebee;
            color: #d32f2f;
            padding: 4px 10px;
            border-radius: 4px;
            font-size: 0.75rem;
            font-weight: 700;
            margin-bottom: 15px;
            align-self: flex-start;
        }

        .badge-green {
            background: #e6f4ea;
            color: var(--primary-green);
        }

        .product-title {
            font-size: 1.2rem;
            font-weight: 700;
            color: var(--primary-blue);
            margin-bottom: 12px;
            line-height: 1.4;
        }

        .product-specs {
            list-style: none;
            margin-bottom: 20px;
            flex-grow: 1;
        }

        .product-specs li {
            position: relative;
            padding-left: 18px;
            margin-bottom: 6px;
            font-size: 0.9rem;
            color: var(--text-gray);
        }

        .product-specs li::before {
            content: "✓";
            position: absolute;
            left: 0;
            color: var(--primary-green);
            font-weight: bold;
        }

        .price-contact {
            font-size: 1rem;
            font-weight: 700;
            color: #d32f2f;
            text-align: center;
            margin-top: auto; /* Đẩy giá xuống đáy */
            margin-bottom: 12px;
            padding: 8px;
            background: #f8f9fa;
            border-radius: 4px;
        }

        /* ==================== FOOTER ==================== */
        footer {
            background: var(--text-dark);
            color: var(--white);
            padding: 30px 0;
            text-align: center;
        }

        footer p {
            color: #9aa0a6;
            font-size: 0.85rem;
            margin-bottom: 4px;
        }

        /* ==================== MODAL ZALO ==================== */
        .modal {
            display: none;
            position: fixed;
            top: 0; left: 0; width: 100%; height: 100%;
            background: rgba(0, 0, 0, 0.6);
            z-index: 2000;
            justify-content: center;
            align-items: center;
            backdrop-filter: blur(2px);
            padding: 15px;
        }

        .modal-content {
            background: var(--white);
            border-radius: 10px;
            padding: 25px;
            max-width: 400px;
            width: 100%;
            text-align: center;
            position: relative;
        }

        .modal-content h3 {
            color: var(--primary-blue);
            margin-bottom: 12px;
        }

        .modal-content p {
            color: var(--text-gray);
            margin-bottom: 20px;
            font-size: 0.95rem;
        }

        .btn-close {
            position: absolute;
            top: 10px; right: 12px;
            background: transparent; border: none;
            color: var(--text-gray); font-size: 1.4rem; cursor: pointer;
        }

        /* ==================== PHẢN HỒI THIẾT BỊ (MEDIA QUERIES) ==================== */
        /* Cho màn hình máy tính bảng và laptop nhỏ */
        @media (max-width: 900px) {
            .hero h1 { font-size: 2rem; }
            .hero p { font-size: 1.05rem; }
            .grid-container { gap: 20px; }
        }

        /* Cho màn hình điện thoại */
        @media (max-width: 600px) {
            :root { --header-height: 70px; } /* Header thấp hơn trên mobile */
            header .container { flex-direction: column; justify-content: center; gap: 5px; padding: 5px 0;}
            .logo-img { max-height: 40px; }
            nav { gap: 12px; }
            nav a { font-size: 0.75rem; }
            
            .hero h1 { font-size: 1.6rem; }
            .hero p { font-size: 0.95rem; padding: 0 5px;}
            .section-title { font-size: 1.6rem; margin-bottom: 30px;}
            .product-title { font-size: 1.1rem; }
            .product-img { height: 250px; }
        }
    </style>
</head>
<body>

    <header>
        <div class="container">
            <a href="#" class="logo-link">
                <img src="logo.png" alt="Dobaco Logistics Logo" class="logo-img" onerror="this.style.display='none'; document.getElementById('logo-fallback').style.display='block';">
                <span id="logo-fallback" style="display:none; font-weight:800; font-size:1.2rem; color:var(--primary-green);">DOBACO <span style="color:var(--primary-blue);">LOGISTICS</span></span>
            </a>
            <nav>
                <a href="#home">Trang Chủ</a>
                <a href="#products">Sản Phẩm</a>
                <a href="https://zalo.me/0383748395" target="_blank" style="color:var(--primary-green);">Báo Giá Sỉ</a>
            </nav>
        </div>
    </header>

    <section class="hero" id="home">
        <div class="container">
            <h1>TỔNG KHO PHÂN PHỐI<br>MÁY SƯỞI DB HOME CHÍNH HÃNG</h1>
            <p>Giải pháp sưởi ấm hoàn hảo chuẩn Châu Âu. Nguồn hàng sẵn sàng tại tổng kho Hải Phòng, đáp ứng sỉ/lẻ số lượng lớn với mức chiết khấu tốt nhất.</p>
            <button class="btn-main" onclick="triggerOrder('Tư vấn Báo Giá')">Liên Hệ Báo Giá</button>
        </div>
    </section>

    <section class="products-section" id="products">
        <div class="container">
            <h2 class="section-title">Tổng Kho <span>Sản Phẩm</span></h2>
            
            <div class="grid-container">
                <div class="product-card">
                    <img src="k23.jpg" alt="Máy Sưởi Gốm DB HOME K23-J" class="product-img" onerror="this.src='https://images.unsplash.com/photo-1634825964860-6fc58f278c2e?auto=format&fit=crop&w=600&q=80'">
                    <div class="product-content">
                        <span class="badge">PHÂN PHỐI SỈ/LẺ SỐ LƯỢNG LỚN</span>
                        <h3 class="product-title">Máy Sưởi Gốm Treo Tường / Để Bàn K23-J</h3>
                        <ul class="product-specs">
                            <li><strong>Công suất:</strong> 1200W - 2000W</li>
                            <li><strong>Bảo hành:</strong> 12 tháng</li>
                            <li>Thiết kế nhỏ gọn, hiện đại, treo tường hoặc để bàn tiện lợi.</li>
                            <li>Công nghệ sưởi gốm êm ái, an toàn, không khô da.</li>
                            <li>Đạt chuẩn Châu Âu (CE, ROHS).</li>
                        </ul>
                        <div class="price-contact">Giá sỉ cực tốt cho Đại Lý</div>
                        <button class="btn-main" style="width: 100%;" onclick="triggerOrder('Máy Sưởi DB HOME K23-J')">Nhận Báo Giá Zalo</button>
                    </div>
                </div>

                <div class="product-card">
                    <img src="k11.jpg" alt="Quạt Sưởi Gốm DB HOME K11-D" class="product-img" onerror="this.src='https://images.unsplash.com/photo-1581057421867-b586071fb8ea?auto=format&fit=crop&w=600&q=80'">
                    <div class="product-content">
                        <span class="badge badge-green">NỘI ĐỊA TRUNG - SẴN KHO</span>
                        <h3 class="product-title">Quạt Sưởi Gốm Dáng Đứng DB HOME K11-D</h3>
                        <ul class="product-specs">
                            <li><strong>Công suất:</strong> 1400W - 2000W</li>
                            <li><strong>Bảo hành:</strong> 12 tháng</li>
                            <li>Kiểu dáng tháp hiện đại, nhỏ gọn, dễ di chuyển.</li>
                            <li>Làm ấm nhanh, KHÔNG đốt oxy, KHÔNG khô da, KHÔNG phát sáng.</li>
                            <li>An toàn tuyệt đối cho người già và trẻ nhỏ.</li>
                        </ul>
                        <div class="price-contact">Chiết khấu cao đơn hàng sỉ</div>
                        <button class="btn-main" style="width: 100%;" onclick="triggerOrder('Quạt Sưởi DB HOME K11-D')">Nhận Báo Giá Zalo</button>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <footer>
        <div class="container">
            <h4 style="margin-bottom: 5px; color: var(--primary-green);">DOBACO LOGISTICS</h4>
            <p>© 2026 Bản quyền thuộc về Dobaco Logistics. Vận tải & Phân phối chuyên nghiệp.</p>
        </div>
    </footer>

    <div class="modal" id="orderModal">
        <div class="modal-content">
            <button class="btn-close" onclick="closeModal()">✕</button>
            <h3 id="modalProductTitle">DOBACO LOGISTICS</h3>
            <p>Hệ thống đang chuyển hướng bạn đến bộ phận kinh doanh trên Zalo để nhận báo giá sỉ/lẻ và tư vấn vận chuyển.</p>
            <a href="https://zalo.me/0383748395" target="_blank" style="text-decoration: none;">
                <button class="btn-main" style="width: 100%;">Mở Zalo Ngay</button>
            </a>
        </div>
    </div>

    <script>
        function triggerOrder(productName) {
            document.getElementById('modalProductTitle').innerText = "Tư Vấn: " + productName;
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
