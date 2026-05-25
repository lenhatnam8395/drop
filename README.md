<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>DOBACO LOGISTICS - Tổng Kho Phân Phối Máy Sưởi DB HOME Hải Phòng</title>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&display=swap" rel="stylesheet">
    
    <style>
        /* ==================== CẤU HÌNH BIẾN MÀU SẮC DOBACO ==================== */
        :root {
            --primary-blue: #1a73e8; 
            --primary-green: #34a853; 
            --bg-light: #f8f9fa;
            --text-dark: #202124;
            --text-gray: #5f6368;
            --white: #ffffff;
            --border-color: #e8eaed;
            --font-main: 'Inter', sans-serif;
            --header-height: 120px; 
        }

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
            overflow-x: hidden; 
        }

        /* KHUNG CHỨA SẢN PHẨM Ở GIỮA ĐÃ ĐƯỢC NỚI RỘNG THÊM */
        .container {
            width: 100%;
            max-width: 1350px; /* Đã tăng từ 1200px lên 1350px để khung thẻ to hơn */
            margin: 0 auto; 
            padding: 0 20px; 
        }

        /* ==================== HEADER TRÀN VIỀN ==================== */
        header {
            width: 100%;
            min-height: var(--header-height);
            background: var(--white);
            box-shadow: 0 2px 10px rgba(0,0,0,0.05);
            position: fixed;
            top: 0;
            z-index: 1000;
        }

        /* Khung riêng cho Header để tràn ra sát viền màn hình */
        .header-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            width: 100%;
            height: 100%;
            padding: 10px 4%; /* Khoảng cách sát mép trái phải màn hình */
            min-height: var(--header-height);
        }

        /* CỤM Logo VÀ TÊN CÔNG TY CĂN TRÁI */
        .Logo-link {
            display: flex;
            align-items: center;
            gap: 15px; 
            text-decoration: none;
        }

        .Logo-img {
            max-height: 100px; 
            width: auto;
            display: block;
        }

        .Logo-text {
            font-weight: 800;
            font-size: 1.8rem;
            color: var(--primary-green);
            white-space: nowrap;
            letter-spacing: 0.5px;
        }

        .Logo-text span {
            color: var(--primary-blue);
        }

        nav {
            display: flex;
            gap: 25px;
        }

        nav a {
            color: var(--text-dark);
            text-decoration: none;
            font-size: 1.05rem;
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
            padding-top: calc(var(--header-height) + 60px); 
            padding-bottom: 80px;
            text-align: center;
        }

        .hero h1 {
            font-size: 2.8rem;
            font-weight: 800;
            color: var(--primary-blue);
            margin-bottom: 20px;
            line-height: 1.2;
        }

        .hero p {
            font-size: 1.2rem;
            color: var(--text-gray);
            max-width: 800px;
            margin: 0 auto 30px;
        }

        .btn-main {
            display: inline-block;
            padding: 15px 35px;
            font-size: 1rem;
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
            transform: translateY(-2px);
        }

        /* ==================== SẢN PHẨM ==================== */
        .products-section {
            padding: 80px 0;
        }

        .section-title {
            text-align: center;
            font-size: 2.2rem;
            font-weight: 800;
            color: var(--text-dark);
            margin-bottom: 50px;
            text-transform: uppercase;
        }

        .section-title span {
            color: var(--primary-green);
        }

        /* ÉP CHUẨN 2 CỘT RỘNG TRÊN MÀN HÌNH MÁY TÍNH */
        .grid-container {
            display: grid;
            grid-template-columns: 1fr 1fr; /* Chia đúng 2 ô bằng nhau, full chiều rộng container */
            gap: 40px;
        }

        .product-card {
            background: var(--white);
            border: 1px solid var(--border-color);
            border-radius: 12px;
            overflow: hidden;
            transition: 0.3s;
            display: flex;
            flex-direction: column;
            height: 100%;
        }

        .product-card:hover {
            box-shadow: 0 10px 30px rgba(0,0,0,0.08);
            border-color: var(--primary-blue);
            transform: translateY(-5px);
        }

        .product-img {
            width: 100%;
            height: 400px; /* Ảnh to hơn để cân xứng với card rộng */
            object-fit: contain;
            background: #fff;
            border-bottom: 1px solid var(--border-color);
            padding: 15px;
        }

        .product-content {
            padding: 30px;
            display: flex;
            flex-direction: column;
            flex-grow: 1;
        }

        .badge {
            display: inline-block;
            background: #ffebee;
            color: #d32f2f;
            padding: 5px 12px;
            border-radius: 4px;
            font-size: 0.85rem;
            font-weight: 700;
            margin-bottom: 15px;
            align-self: flex-start;
        }

        .badge-green {
            background: #e6f4ea;
            color: var(--primary-green);
        }

        /* TÊN SẢN PHẨM ĐẢM BẢO NẰM TRÊN 1 DÒNG */
        .product-title {
            font-size: 1.3rem;
            font-weight: 700;
            color: var(--primary-blue);
            margin-bottom: 15px;
            white-space: nowrap; /* Ép không rớt dòng */
            overflow: hidden; 
            text-overflow: ellipsis; /* Hiện dấu ... nếu màn hình quá bé */
        }

        .product-specs {
            list-style: none;
            margin-bottom: 25px;
            flex-grow: 1;
        }

        .product-specs li {
            position: relative;
            padding-left: 22px;
            margin-bottom: 10px;
            font-size: 1rem;
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
            font-size: 1.15rem;
            font-weight: 700;
            color: #d32f2f;
            text-align: center;
            margin-top: auto;
            margin-bottom: 15px;
            padding: 12px;
            background: #f8f9fa;
            border-radius: 6px;
        }

        /* ==================== FOOTER ==================== */
        footer {
            background: var(--text-dark);
            color: var(--white);
            padding: 40px 0;
            text-align: center;
        }

        footer p {
            color: #9aa0a6;
            font-size: 0.95rem;
            margin-bottom: 5px;
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
            border-radius: 12px;
            padding: 30px;
            max-width: 450px;
            width: 100%;
            text-align: center;
            position: relative;
        }

        .modal-content h3 {
            color: var(--primary-blue);
            margin-bottom: 15px;
        }

        .modal-content p {
            color: var(--text-gray);
            margin-bottom: 25px;
            font-size: 1rem;
        }

        .btn-close {
            position: absolute;
            top: 15px; right: 15px;
            background: transparent; border: none;
            color: var(--text-gray); font-size: 1.5rem; cursor: pointer;
        }

        /* ==================== RESPONSIVE CHO ĐIỆN THOẠI/TABLET ==================== */
        @media (max-width: 1024px) {
            .product-title {
                font-size: 1.1rem; /* Giảm nhẹ font chữ tên SP trên màn nhỏ để vẫn giữ 1 dòng */
            }
        }

        @media (max-width: 900px) {
            .header-container { flex-direction: column; justify-content: center; gap: 15px; padding: 15px; }
            .hero { padding-top: 220px; } 
            .hero h1 { font-size: 2.2rem; }
            
            /* Dưới 900px thì chuyển thành 1 cột xếp chồng lên nhau */
            .grid-container { grid-template-columns: 1fr; }
            .product-title { white-space: normal; } /* Bỏ ép 1 dòng trên điện thoại */
        }

        @media (max-width: 600px) {
            .Logo-img { max-height: 80px; } 
            .Logo-text { font-size: 1.4rem; }
            nav { gap: 10px; flex-wrap: wrap; justify-content: center;}
            nav a { font-size: 0.85rem; }
            
            .hero { padding-top: 240px; }
            .hero h1 { font-size: 1.8rem; }
            .product-img { height: 280px; }
        }
    </style>
</head>
<body>

    <header>
        <div class="header-container">
            <a href="#" class="Logo-link">
                <img src="Logo.png" alt="Dobaco Logistics Logo" class="Logo-img">
                <span class="Logo-text">DOBACO <span>LOGISTICS</span></span>
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
                        <h3 class="product-title" title="Máy Sưởi Gốm Treo Tường / Để Bàn K23-J">Máy Sưởi Gốm Treo Tường / Để Bàn K23-J</h3>
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
                        <span class="badge badge-green">NHẬP KHẨU - SẴN KHO</span>
                        <h3 class="product-title" title="Quạt Sưởi Gốm Dáng Đứng DB HOME K11-D">Quạt Sưởi Gốm Dáng Đứng DB HOME K11-D</h3>
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
