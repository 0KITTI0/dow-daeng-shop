<!DOCTYPE html>
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
                    <p>บริการซื้อขาย ID เกมROV</p>
                    <p>ราคาเริ่มต้น 50บาท</p>
                    <button>กดเพื่อดูรายระเอียดการบิการ</button>
                </div>
                <div class="item">
                    <img src="https://media.tenor.com/HO1YAH0_iMcAAAAi/roblox-logo.gif" alt="ROBLOX">
                    <h3>ROBLOX</h3>
                    <p>รายละเอียดสินค้า 2</p>
                    <p>ราคา: $15</p>
                    <button>หยิบใส่ตะกร้า</button>
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
    </div>
</body>
</html>
