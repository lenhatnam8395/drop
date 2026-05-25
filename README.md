<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>DOBACO LOGISTICS - Tổng Kho Phân Phối Máy Sưởi DB HOME</title>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&display=swap" rel="stylesheet">
    
    <style>
        /* ==================== CẤU HÌNH BIẾN MÀU SẮC LẤY CẢM HỨNG TỪ LOGO DOBACO ==================== */
        :root {
            --primary-blue: #1a73e8; /* Xanh dương Dobaco */
            --primary-green: #34a853; /* Xanh lá Dobaco */
            --bg-light: #f8f9fa;
            --text-dark: #202124;
            --text-gray: #5f6368;
            --white: #ffffff;
            --border-color: #e8eaed;
            --font-main: 'Inter', sans-serif;
        }

        /* RESET */
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

        /* ==================== HEADER ==================== */
        header {
            width: 100%;
            padding: 15px 5%;
            background: var(--white);
            box-shadow: 0 2px 10px rgba(0,0,0,0.05);
            position: fixed;
            top: 0;
            z-index: 1000;
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
        }

        .logo {
            font-weight: 800;
            font-size: 1.5rem;
            color: var(--primary-green);
            text-transform: uppercase;
            letter-spacing: 0.5px;
            display: flex;
            align-items: center;
            gap: 10px;
            text-decoration: none;
        }

        .logo span {
            color: var(--primary-blue);
        }

        nav {
            display: flex;
            gap: 25px;
            flex-wrap: wrap;
        }

        nav a {
            color: var(--text-dark);
            text-decoration: none;
            font-size: 0.95rem;
            font-weight: 600;
            transition: 0.3s;
            text-transform: uppercase;
        }

        nav a:hover {
            color: var(--primary-blue);
        }

        /* ==================== HERO BANNER ==================== */
        .hero {
            background: linear-gradient(135deg, #e8f0fe 0%, #e6f4ea 100%);
            padding: 120px 20px 80px;
            text-align: center;
        }

        .hero h1 {
            font-size: 2.8rem;
            font-weight: 800;
            color: var(--primary-blue);
            margin-bottom: 20px;
            line-height: 1.3;
        }

        .hero p {
            font-size: 1.2rem;
            color: var(--text-gray);
            max-width: 700px;
            margin: 0 auto 30px;
        }

        .btn-main {
            display: inline-block;
            padding: 14px 35px;
            font-size: 1rem;
            font-weight: 700;
            color: var(--white);
            background: var(--primary-blue);
            border: none;
            border-radius: 8px;
            cursor: pointer;
            text-transform: uppercase;
            text-decoration: none;
            transition: all 0.3s ease;
            box-shadow: 0 4px 15px rgba(26, 115, 232, 0.3);
        }

        .btn-main:hover {
            background: var(--primary-green);
            box-shadow: 0 4px 15px rgba(52, 168, 83, 0.3);
            transform: translateY(-2px);
        }

        /* ==================== SẢN PHẨM ==================== */
        .products-section {
            padding: 80px 5%;
            max-width: 1200px;
            margin: 0 auto;
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

        .grid-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 40px;
        }

        .product-card {
            background: var(--white);
            border: 1px solid var(--border-color);
            border-radius: 12px;
            overflow: hidden;
            transition: all 0.3s ease;
            display: flex;
            flex-direction: column;
        }

        .product-card:hover {
            box-shadow: 0 10px 30px rgba(0,0,0,0.08);
            border-color: var(--primary-blue);
            transform: translateY(-5px);
        }

        .product-img {
            width: 100%;
            height: 350px;
            object-fit: contain;
            background: #fff;
            border-bottom: 1px solid var(--border-color);
            padding: 10px;
        }

        .product-content {
            padding: 25px;
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
            font-size: 0.8rem;
            font-weight: 700;
            margin-bottom: 15px;
            align-self: flex-start;
        }

        .badge-green {
            background: #e6f4ea;
            color: var(--primary-green);
        }

        .product-title {
            font-size: 1.3rem;
            font-weight: 700;
            color: var(--primary-blue);
            margin-bottom: 15px;
            line-height: 1.4;
        }

        .product-specs {
            list-style: none;
            margin-bottom: 25px;
            flex-grow: 1;
        }

        .product-specs li {
            position: relative;
            padding-left: 20px;
            margin-bottom: 8px;
            font-size: 0.95rem;
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
            font-size: 1.1rem;
            font-weight: 700;
            color: #d32f2f;
            text-align: center;
            margin-bottom: 15px;
            padding: 10px;
            background: #f8f9fa;
            border-radius: 6px;
        }

        /* ==================== FOOTER ==================== */
        footer {
            background: var(--text-dark);
            color: var(--white);
            padding: 40px 5%;
            text-align: center;
        }

        footer p {
            color: #9aa0a6;
            font-size: 0.9rem;
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
            backdrop-filter: blur(3px);
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
            box-shadow: 0 20px 40px rgba(0,0,0,0.2);
        }

        .modal-content h3 {
            color: var(--primary-blue);
            margin-bottom: 15px;
            font-size: 1.4rem;
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

        .btn-close:hover { color: #d32f2f; }

        /* RESPONSIVE */
        @media (max-width: 768px) {
            header { flex-direction: column; padding: 15px; gap: 15px; }
            nav { justify-content: center; width: 100%; }
            .hero h1 { font-size: 2rem; }
            .section-title { font-size: 1.8rem; }
        }
    </style>
</head>
<body>

    <header>
        <a href="#" class="logo">DOBACO <span>LOGISTICS</span></a>
        <nav>
            <a href="#home">Trang Chủ</a>
            <a href="#products">Sản Phẩm</a>
            <a href="https://zalo.me/0383748395" target="_blank">Nhận Báo Giá Sỉ</a>
        </nav>
    </header>

    <section class="hero" id="home">
        <h1>TỔNG KHO PHÂN PHỐI<br>MÁY SƯỞI DB HOME CHÍNH HÃNG</h1>
        <p>Giải pháp sưởi ấm hoàn hảo chuẩn Châu Âu. Nguồn hàng sẵn sàng tại tổng kho Hải Phòng, đáp ứng sỉ/lẻ số lượng lớn với mức chiết khấu tốt nhất thị trường.</p>
        <button class="btn-main" onclick="triggerOrder('Tư vấn Báo Giá Sỉ/Lẻ')">Liên Hệ Báo Giá Ngay</button>
    </section>

    <section class="products-section" id="products">
        <h2 class="section-title">Danh Mục <span>Sản Phẩm</span></h2>
        
        <div class="grid-container">
            <div class="product-card">
                <img src="k23.jpg" alt="Máy Sưởi Gốm K23-J" class="product-img" onerror="this.src='https://images.unsplash.com/photo-1634825964860-6fc58f278c2e?auto=format&fit=crop&w=600&q=80'">
                <div class="product-content">
                    <span class="badge">SỈ LẺ SỐ LƯỢNG CỰC LỚN</span>
                    <h3 class="product-title">Máy Sưởi Gốm Treo Tường / Để Bàn DB HOME K23-J</h3>
                    <ul class="product-specs">
                        <li><strong>Điện áp/Công suất:</strong> AC 220-240V | 1200W - 2000W</li>
                        <li><strong>Bảo hành:</strong> 12 tháng (Lỗi NSX)</li>
                        <li>Thiết kế nhỏ gọn, hiện đại, linh hoạt lắp đặt mọi không gian.</li>
                        <li>Công nghệ sưởi ấm êm ái, an toàn tuyệt đối.</li>
                        <li>Đạt chuẩn xuất khẩu Châu Âu (Chứng chỉ CE, ROHS, GS).</li>
                    </ul>
                    <div class="price-contact">Giá cực tốt cho Đại Lý / Khách Sỉ</div>
                    <button class="btn-main" style="width: 100%;" onclick="triggerOrder('Máy Sưởi Gốm DB HOME K23-J')">Nhận Báo Giá Qua Zalo</button>
                </div>
            </div>

            <div class="product-card">
                <img src="k11.jpg" alt="Quạt Sưởi Gốm K11-D" class="product-img" onerror="this.src='https://images.unsplash.com/photo-1581057421867-b586071fb8ea?auto=format&fit=crop&w=600&q=80'">
                <div class="product-content">
                    <span class="badge badge-green">SẴN KHO SỐ LƯỢNG LỚN</span>
                    <h3 class="product-title">Quạt Sưởi Gốm Dáng Đứng DB HOME K11-D</h3>
                    <ul class="product-specs">
                        <li><strong>Công suất:</strong> 1400W - 2000W</li>
                        <li><strong>Bảo hành:</strong> 12 tháng (Lỗi NSX)</li>
                        <li>Kiểu dáng tháp hiện đại, nhỏ gọn, tiện di chuyển mọi nơi.</li>
                        <li>Công nghệ sưởi gốm: Làm ấm nhanh, KHÔNG đốt oxy, KHÔNG khô da, KHÔNG phát sáng.</li>
                        <li>Đạt chuẩn Châu Âu CE/ROHS, an toàn cho trẻ nhỏ và người già.</li>
                    </ul>
                    <div class="price-contact">Chiết khấu cao cho đơn hàng lớn</div>
                    <button class="btn-main" style="width: 100%;" onclick="triggerOrder('Quạt Sưởi Gốm DB HOME K11-D')">Nhận Báo Giá Qua Zalo</button>
                </div>
            </div>
        </div>
    </section>

    <footer>
        <h3 style="margin-bottom: 10px; color: var(--primary-green);">DOBACO LOGISTICS</h3>
        <p>Hệ thống vận tải và phân phối hàng hóa chuyên nghiệp.</p>
        <p>© 2026 Bản quyền thuộc về Dobaco Logistics. All rights reserved.</p>
    </footer>

    <div class="modal" id="orderModal">
        <div class="modal-content">
            <button class="btn-close" onclick="closeModal()">✕</button>
            <h3 id="modalProductTitle">DOBACO LOGISTICS</h3>
            <p>Hệ thống đang chuyển hướng bạn đến Zalo cá nhân của bộ phận kinh doanh để nhận báo giá chiết khấu và quy trình giao nhận.</p>
            <a href="https://zalo.me/0383748395" target="_blank" style="text-decoration: none;">
                <button class="btn-main" style="width: 100%;">Mở Zalo Trực Tiếp</button>
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
