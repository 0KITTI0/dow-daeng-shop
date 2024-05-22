<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>DOW DAENG SHOP</title>
    <link rel="stylesheet" href="CSS/body.css">
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
            <li><a href="#contact">ติดต่อ</a></li>
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
                    <button>กดเพื่อดูรายระเอียดการบิการ</button>
                </div>
                <div class="item">
                    <img src="https://media.tenor.com/HO1YAH0_iMcAAAAi/roblox-logo.gif" alt="ROBLOX">
                    <h3>ROBLOX</h3>
                    <p>บริการซื้อขาย ID/Item เกม Roblox</p>
                    <p>ราคาเริ่มต้น 10บาท</p>
                    <button>กดเพื่อดูรายระเอียดการบิการ</button>
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

