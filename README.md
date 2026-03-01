<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Khám Phá Phong Nha - Kẻ Bàng</title>
    <style>
        * { margin: 0; padding: 0; box-sizing: border-box; }
        body { font-family: 'Segoe UI', Arial, sans-serif; line-height: 1.6; background: #f9f9f9; }
        
        .container { max-width: 1100px; margin: auto; padding: 50px 20px; }
        .section-title { text-align: center; margin-bottom: 40px; color: #1a472a; }

        /* Grid hiển thị các địa điểm */
        .grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 20px; }
        
        .card { 
            background: white; 
            padding: 20px; 
            border-radius: 12px; 
            box-shadow: 0 4px 6px rgba(0,0,0,0.1); 
            cursor: pointer; 
            transition: all 0.3s ease;
            text-align: center;
            border: 2px solid transparent;
        }
        .card:hover { 
            transform: translateY(-10px); 
            border-color: #1a472a;
            box-shadow: 0 10px 20px rgba(0,0,0,0.15);
        }
        .card h3 { color: #1a472a; margin-bottom: 10px; }
        .card p { color: #666; font-size: 0.9rem; }
        .click-hint { margin-top: 15px; display: inline-block; color: #2ecc71; font-weight: bold; font-size: 0.8rem; }

        /* Cấu trúc Modal (Cửa sổ hiện ảnh) */
        .modal {
            display: none; /* Ẩn mặc định */
            position: fixed;
            z-index: 2000;
            left: 0; top: 0;
            width: 100%; height: 100%;
            background-color: rgba(0,0,0,0.9);
            justify-content: center;
            align-items: center;
            flex-direction: column;
        }
        .modal-content {
            max-width: 80%;
            max-height: 70%;
            border-radius: 8px;
            box-shadow: 0 0 20px rgba(255,255,255,0.2);
        }
        #caption {
            color: white;
            margin-top: 20px;
            font-size: 1.5rem;
            font-weight: bold;
        }
        .close-btn {
            position: absolute;
            top: 20px; right: 35px;
            color: #f1f1f1;
            font-size: 40px;
            font-weight: bold;
            cursor: pointer;
        }
    </style>
    <style>
        /* CSS Reset & Cơ bản */
        * { margin: 0; padding: 0; box-sizing: border-box; }
        body { font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif; line-height: 1.6; color: #333; }
        
        /* Navigation */
        nav { background: #1a472a; color: white; padding: 1rem; position: fixed; width: 100%; top: 0; z-index: 1000; display: flex; justify-content: space-between; align-items: center; }
        nav h1 { font-size: 1.2rem; text-transform: uppercase; letter-spacing: 2px; }
        nav ul { display: flex; list-style: none; }
        nav ul li { margin-left: 20px; }
        nav ul li a { color: white; text-decoration: none; font-weight: bold; }

        /* Hero Section */
        .hero { 
            height: 80vh; 
            background: linear-gradient(rgba(0,0,0,0.5), rgba(0,0,0,0.5)), 
                        url('https://s3-ap-southeast-1.amazonaws.com/cntatr-assets-ap-southeast-1-250226768838-55a62c9399d4d8a6/2024/07/danh-lam-thang-canh-viet-nam-3.jpg?tr=q-70,c-at_max,w-1000,h-600') no-repeat center center/cover;
            display: flex; flex-direction: column; justify-content: center; align-items: center; 
            color: white; text-align: center; padding: 0 20px;
        }
        .hero h2 { font-size: 3.5rem; margin-bottom: 10px; }
        .hero p { font-size: 1.2rem; max-width: 800px; }

        /* Section chung */
        .container { max-width: 1100px; margin: auto; overflow: hidden; padding: 4rem 2rem; }
        .section-title { text-align: center; margin-bottom: 3rem; position: relative; }
        .section-title::after { content: ''; background: #1a472a; height: 3px; width: 50px; position: absolute; bottom: -10px; left: 50%; transform: translateX(-50%); }

        /* Giới thiệu Grid */
        .grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 2rem; }
        .card { background: #f4f4f4; padding: 1.5rem; border-radius: 8px; transition: 0.3s; }
        .card:hover { transform: translateY(-5px); box-shadow: 0 5px 15px rgba(0,0,0,0.1); }
        .card h3 { color: #1a472a; margin-bottom: 10px; }

        /* Footer */
        footer { background: #333; color: white; text-align: center; padding: 2rem; margin-top: 2rem; }
    </style>
</head>
<body>

    <nav>
        <h1>Phong Nha - Kẻ Bàng</h1>
        <ul>
            <li><a href="#intro">Giới thiệu</a></li>
            <li><a href="#destinations">Điểm đến</a></li>
        </ul>
    </nav>

    <header class="hero">
        <h2>Khám Phá Kỳ Quan Thiên Nhiên</h2>
        <p>Vườn quốc gia Phong Nha - Kẻ Bàng, di sản thiên nhiên thế giới được UNESCO công nhận, nơi ẩn chứa những bí mật triệu năm của tạo hóa.</p>
    </header>

    <section id="intro" class="container">
        <h2 class="section-title">Tổng quan Di sản</h2>
        <p style="text-align: center;">Tọa lạc tại tỉnh Quảng Bình, Việt Nam, đây là vùng đá vôi cổ nhất châu Á với hệ thống hơn 300 hang động lớn nhỏ cùng hệ sinh thái động thực vật vô cùng phong phú.</p>
        <p>Phong Nha-Kẻ Bàng nổi tiếng không chỉ nhờ vào phong cảnh hùng vĩ và giá trị khoa học độc đáo, vùng đất này còn lưu giữ những chứng tích lịch sử quý giá. Nơi đây là minh chứng của một thời kỳ đấu tranh máu lửa của dân tộc Việt Nam nói chung và nhân dân Phong Nha nói riêng.</section></p>
    </section>
    <section id="history" class="container">
        <h2 class="section-title">Lịch sử</h2>
        <p style="text-align: center;">Tồn tại hàng nghìn năm từ năm 192 - 1832, Chăm Pa được xem là một trong những quốc gia tồn tại lâu đời ở Đông Nam Á. Trong thời kỳ huy hoàng, vương quốc Chăm Pa nằm trải dài trên khắp miền Trung và đã để lại vô số công trình kiến trúc độc đáo.

Theo lịch sử Phong Nha thời tiền sử, nơi đây thuộc một phần lãnh thổ của Chăm Pa và là khu vực giao thương chiến lược với các nước trong khu vực. Nhờ nằm gần các tuyến đường thuỷ quan trọng và tiếp giáp biển Đông, nơi đây đã trở thành trung tâm giao lưu thương mại và văn hoá quan trọng. Các nước như Trung Hoa, Đại Việt, Khơ Me,... khi đến Chăm Pa đều đi qua khu vực này.

Qua hàng trăm năm, mảnh đất này đã chứng kiến những sự kiện ngoại giao và chiến tranh giữa các nước, đặc biệt là giữa Chăm Pa và Đại Việt. Với địa thế núi rừng hiểm trở ở phía tây và giáp biển ở phía đông, Phong Nha còn là cửa ngõ quân sự, nơi diễn ra nhiều trận chiến ác liệt cả trên bộ và trên biển. Đến năm 1832, Chăm Pa chính thức bị đánh bại và trở thành một phần lãnh thổ của Việt Nam.</p>
    </section>
<div class="container">
        <h2 class="section-title">Bấm vào địa điểm để xem hình ảnh</h2>
        
        <div class="grid">
            <div class="card" onclick="openModal('https://phongnhaviet.com/uploads/service/phong_nha/dong-phong-nha-ke-bang-dep-den-choang-ngop.jpg', 'Động Phong Nha - Kỳ quan đệ nhất động')">
                <h3>Động Phong Nha</h3>
                <p>Khám phá hệ thống sông ngầm và thạch nhũ huyền ảo bằng thuyền.</p>
                <span class="click-hint">Xem hình ảnh →</span>
            </div>

            <div class="card" onclick="openModal('https://webdulichmientrung.com/wp-content/uploads/2020/02/thienduong.jpg', 'Động Thiên Đường - Hoàng cung trong lòng đất')">
                <h3>Động Thiên Đường</h3>
                <p>Hang động khô dài nhất châu Á với vẻ đẹp kỳ vĩ của tạo hóa.</p>
                <span class="click-hint">Xem hình ảnh →</span>
            </div>

            <div class="card" onclick="openModal('https://images2.thanhnien.vn/528068263637045248/2023/5/5/son-doong-16832729533231329428982.jpg', 'Hang Sơn Đoòng - Hang động lớn nhất thế giới')">
                <h3>Hang Sơn Đoòng</h3>
                <p>Tuyệt tác thiên nhiên với hệ sinh thái riêng biệt bên trong lòng đất.</p>
                <span class="click-hint">Xem hình ảnh →</span>
            </div>
        </div>
    </div>

    <div id="myModal" class="modal">
        <span class="close-btn" onclick="closeModal()">&times;</span>
        <img class="modal-content" id="img01">
        <div id="caption"></div>
    </div>

    <script>
        function openModal(imgSrc, title) {
            document.getElementById("myModal").style.display = "flex";
            document.getElementById("img01").src = imgSrc;
            document.getElementById("caption").innerHTML = title;
        }

        function closeModal() {
            document.getElementById("myModal").style.display = "none";
        }

        // Đóng modal khi bấm ra ngoài vùng ảnh
        window.onclick = function(event) {
            var modal = document.getElementById("myModal");
            if (event.target == modal) {
                modal.style.display = "none";
            }
        }
    </script>
     <footer>
        <p>&copy; 2024 Du lịch Quảng Bình - Vẻ đẹp bất tận</p>
    </footer>
    <footer>
        <p>&copy; nhóm 7 lớp 12a1 </p>
    </footer>
</body>
</html>
