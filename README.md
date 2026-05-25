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
            --header-height: 110px; 
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

        /* KHUNG CHUẨN CĂN GIỮA TOÀN BỘ WEBSITE */
        .container {
            width: 95%; /* Chiếm 95% màn hình để luôn có khoảng không 2 bên */
            max-width: 1400px; /* Mở rộng tối đa lên 1400px */
            margin: 0 auto; /* Tự động căn giữa */
        }

        /* ==================== HEADER ==================== */
        header {
            width: 100%;
            min-height: var(--header-height);
            background: var(--white);
            box-shadow: 0 2px 10px rgba(0,0,0,0.05);
            position: fixed;
            top: 0;
            z-index: 1000;
            display: flex;
            justify-content: center; /* Đảm bảo nội dung bên trong được căn giữa theo container */
        }

        .header-container {
            display: flex;
            justify-content: space-between; /* Đẩy logo sang trái, menu sang phải */
            align-items: center;
            width: 95%;
            max-width: 1400px;
            padding: 10px 0;
            flex-wrap: wrap; /* Cho phép xuống dòng nếu màn hình thu nhỏ, chống mất chữ */
        }

        /* CỤM LOGO VÀ TÊN CÔNG TY */
        .logo-link {
            display: flex;
            align-items: center;
            gap: 15px; 
            text-decoration: none;
        }

        .logo-img {
            max-height: 80px; /* Chỉnh lại tỷ lệ chuẩn để không làm méo khung header */
            width: auto;
            display: block;
        }

        .logo-text {
            font-weight: 800;
            font-size: 1.7rem;
            color: var(--primary-green);
            white-space: nowrap;
            letter-spacing: 0.5px;
        }

        .logo-text span {
            color: var(--primary-blue);
        }

        nav {
            display: flex;
            gap: 25px;
            align-items: center;
        }

        nav a {
            color: var(--text-dark);
            text-decoration: none;
            font-size: 1.05rem;
            font-weight: 700;
            transition: 0.3s;
            text-transform: uppercase;
            white-space: nowrap; /* Đảm bảo từng nút menu không bị gãy ngang */
        }

        nav a:hover, nav a.active {
            color: var(--primary-blue);
        }

        /* ==================== HERO BANNER ==================== */
        .hero {
            background: linear-gradient(135deg, #e8f0fe 0%, #e6f4ea 100%);
            padding-top: calc(var(--header-height) + 50px); 
            padding-bottom: 70px;
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

        /* CHIA 2 CỘT RỘNG */
        .grid-container {
            display: grid;
            grid-template-columns: 1fr 1fr; /* Chia 2 ô đều nhau */
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
            height: 420px; /* Tăng chiều cao để cân đối với khung rộng */
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

        /* ĐÃ SỬA: Hiển thị đầy đủ tên sản phẩm, cho phép rớt dòng tự nhiên */
        .product-title {
            font-size: 1.4rem;
            font-weight: 700;
            color: var(--primary-blue);
            margin-bottom: 15px;
            line-height: 1.4;
            white-space: normal; /* Chống bị cắt ngang chữ */
        }

        .product-specs {
            list-style: none;
            margin-bottom: 25px;
