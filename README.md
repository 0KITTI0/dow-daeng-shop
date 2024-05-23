
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>DOW DAENG SHOP</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #7c7c7c; /* เปลี่ยนสีพื้นหลังของ body เป็นสีเทาอ่อน */
        }
        header {
            background-color: #c40202;
            color: #fff;
            padding: 10px 0;
            text-align: center;
        }
        nav {
            background-color: #1d0d0d;
            color: #fff;
            text-align: center;
            padding: 10px 0;
        }
        nav ul {
            list-style-type: none;
            margin: 0;
            padding: 0;
        }
        nav ul li {
            display: inline;
            margin-right: 20px;
        }
        nav ul li a {
            color: #fff;
            text-decoration: none;
        }
        .container {
            width: 80%;
            margin: auto;
            overflow: hidden;
        }
        .main-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            grid-gap: 20px;
        }
        .item {
            border: 1px solid #ccc;
            padding: 20px;
            text-align: center;
        }
        .item img {
            max-width: 100%;
            height: auto;
        }
        .hidden {
            display: none;
        }
        .main-content {
            display: flex;
            flex-wrap: wrap;
        }
        .item {
            flex: 1 1 calc(33.33% - 20px); /* ความกว้างของแต่ละไอเท็ม */
            margin-bottom: 20px;
        }
        @media screen and (max-width: 768px) {
            .item {
                flex: 1 1 calc(50% - 20px); /* ให้แสดงเป็น 2 แถวเมื่อหน้าจอเล็กกว่า 768px */
            }
        }
        @media screen and (max-width: 480px) {
            .item {
                flex: 1 1 100%; /* ให้แสดงเป็น 1 แถวเมื่อหน้าจอเล็กกว่า 480px */
            }
        }
        .item img {
            max-width: 325px; /* ปรับขนาดรูปให้มีความกว้างไม่เกิน 100px */
            height: auto; /* จัดให้สูงของรูปปรับตามอัตราส่วน */
        }
    </style>
    <script>
        function showPage(pageId) {
            var pages = document.querySelectorAll('.page');
            pages.forEach(function(page) {
                page.classList.add('hidden');
            });
            document.getElementById(pageId).classList.remove('hidden');
        }

        function loadPage() {
            const hash = window.location.hash.substring(1);
            if (hash) {
                showPage(hash);
            } else {
                showPage('home');
            }
        }

        window.addEventListener('hashchange', loadPage);
        window.addEventListener('load', loadPage);

        function showROVPage() {
            window.location.href = "#rov";
        }
        function showROBLOXPage() {
            window.location.href = "#roblox";
        }
        function showBRAWHALLAPage() {
            window.location.href = "#BRAWHALLA";
        }
    </script>
</head>
<body>
    <header>
        <h1>DOW DAENG SHOP</h1>
    </header>
    <nav>
        <ul>
            <li><a href="#home">หน้าแรก</a></li>
            <li><a href="#products">สินค้า</a></li>
            <li><a href="#about">เกี่ยวกับเรา</a></li>
            <li><a href="#contact">ติดต่อเรา</a></li>
        </ul>
    </nav>
    <div class="container">
        <div id="home" class="page">
            <h2>ยินดีต้อนรับสู่ DOW DAENG SHOP</h2>
            <p>เลือกเมนูด้านบนเพื่อดูข้อมูลเพิ่มเติม</p>
        </div>
        <div id="products" class="page hidden">
            <h2>สินค้า</h2>
            <div class="main-content">
                <div class="item">
                    <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT2uIx-58vV_cKQL3BAyioi2-2DD7PNZn6isw&usqp=CAU" alt="ROV">
                    <h3>ROV</h3>
                    <p>บริการซื้อขาย ID/ขึ้นแรงค์ เกมROV</p>
                    <p>ราคาเริ่มต้น 50บาท</p>
                    <button onclick="showROVPage()">กดเพื่อดูรายระเอียดการบิการ</button>
                </div>
                <div class="item">
                    <img src="https://media.tenor.com/HO1YAH0_iMcAAAAi/roblox-logo.gif" alt="ROBLOX">
                    <h3>ROBLOX</h3>
                    <p>บริการซื้อขาย ID/Item เกม Roblox</p>
                    <p>ราคาเริ่มต้น 50บาท</p>
                    <button onclick="showROBLOXPage()">กดเพื่อดูรายระเอียดการบิการ</button>
                </div>
                <div class="item">
                    <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/4/43/PUBG_Mobile_simple_logo_black.png/1200px-PUBG_Mobile_simple_logo_black.png" alt="PUBG">
                    <h3>PUBG</h3>
                    <p>บริการซื้อขาย ID/ขึ้นแรงค์ เกมPUBG</p>
                    <p>ราคาเริ่มต้น 50บาท</p>
                    <button onclick="showPUBGage()">กดเพื่อดูรายระเอียดการบิการ</button>
                </div>
                <div class="item">
                    <img src="https://play-lh.googleusercontent.com/pGTbyodNnwtdEOVVXgMiyZ0FQwY1AVvcm7h_FNZc5eLUggAeQ-GR4JN811nQdN4LnQ=w240-h480-rw" alt="FREE FIRE">
                    <h3>ROV</h3>
                    <p>บริการซื้อขาย ID/ขึ้นแรงค์ เกมFREE FIRE</p>
                    <p>ราคาเริ่มต้น 50บาท</p>
                    <button onclick="showFFPage()">กดเพื่อดูรายระเอียดการบิการ</button>
                </div>
                <div class="item">
                    <img src="https://static.wikia.nocookie.net/brawlhalla_gamepedia/images/1/12/Brawlhalla_Logo_2017.png/revision/latest?cb=20220101211109" alt="BRAWHALLA">
                    <h3>BRAWHALLA</h3>
                    <p>บริการซื้อขาย ID/ขึ้นแรงค์ เกมBRAWHALLA</p>
                    <p>ราคาเริ่มต้น 50บาท</p>
                    <button onclick="showBRAWHALLAPage()">กดเพื่อดูรายระเอียดการบิการ</button>
                </div>
                <div class="item">
                    <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT2uIx-58vV_cKQL3BAyioi2-2DD7PNZn6isw&usqp=CAU" alt="ROV">
                    <h3>ROV</h3>
                    <p>บริการซื้อขาย ID/ขึ้นแรงค์ เกมROV</p>
                    <p>ราคาเริ่มต้น 50บาท</p>
                    <button onclick="showROVPage()">กดเพื่อดูรายระเอียดการบิการ</button>
                </div>
                <!-- เพิ่มไอเท็มเพิ่มเติมตามต้องการ -->
            </div>
        </div>
        <div id="about" class="page hidden">
            <h2>เกี่ยวกับเรา</h2>
            <p>ข้อมูลเกี่ยวกับธุรกิจของเรา</p>
        </div>
        <div id="contact" class="page hidden">
            <h2>ติดต่อเรา</h2>
            <p>ข้อมูลการติดต่อ</p>
        </div>
        <div id="rov" class="page hidden">
            <h2>ROV</h2>
            <p>รายละเอียดเกี่ยวกับ ROV จะปรากฏที่นี่...</p>
        </div>
        <div id="roblox" class="page hidden">
            <h2>ROBLOX</h2>
            <p>รายละเอียดเกี่ยวกับ ROBLOX จะปรากฏที่นี่...</p>
        </div>
        <div id="BRAWHALLA" class="page hidden">
            <h2>BRAWHALLA</h2>
            <p>รายละเอียดเกี่ยวกับ BRAWHALLA จะปรากฏที่
นี่...</p>
        </div>
    </div>
</body>
</html>

}
