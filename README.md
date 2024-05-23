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
