<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ket hop Javascript voi CSS</title>
    <style>
        body {
            font-family: Arial, sans-serif;
        }
        button {
            margin: 3px;
            padding: 5px 10px;
            border: 1px solid #333;
            cursor: pointer;
        }
        select {
            margin: 5px;
            padding: 5px;
        }
        #NoiDung {
            width: 100%;
            height: 50px;
            border: 2px solid black;
            margin-top: 20px;
            padding: 10px;
            font-size: 20px;
        }
      
        #title {
            font-size: 24px;
            color: black;
            font-weight: bold;
        }
    </style>
</head>
<body>
<p>JAVASCRIPT và CSS</p>
    <button onclick="changeColor('blue')">Xanh</button>
    <button onclick="changeColor('red')">Đỏ</button>
    <button onclick="changeColor('yellow')">Vàng</button>
    <button onclick="changeColor('')">Không màu</button>
<br>
    <select id="fontSize">
        <option value="20px">20px</option>
        <option value="30px">30px</option>
        <option value="40px">40px</option>
    </select>
    <button onclick="changeFontSize()">Đặt cỡ chữ</button>
<br>
    <select id="heightSize">
        <option value="100px">100px</option>
        <option value="150px">150px</option>
        <option value="200px">200px</option>
    </select>
    <button onclick="changeHeight()">Đặt chiều cao</button>
    <button onclick="increaseHeight()">Tăng chiều cao</button>
<br>
    <button onclick="applyTitleCSS()">Nạp css tiêu đề</button><br>
    <button onclick="applyContentCSS()">Nạp css nội dung</button>

    <div id="NoiDung">#Nội Dung: Xin chào các bạn!</div>

    <script>
        function changeColor(color) {
            document.getElementById('NoiDung').style.backgroundColor = color;
        }

        function changeFontSize() {
            let size = document.getElementById('fontSize').value;
            document.getElementById('NoiDung').style.fontSize = size;
        }

        function changeHeight() {
            let height = document.getElementById('heightSize').value;
            document.getElementById('NoiDung').style.height = height;
        }

        function increaseHeight() {
            let currentHeight = document.getElementById('NoiDung').style.height;
            let newHeight = parseInt(currentHeight) + 50 + "px";
            document.getElementById('NoiDung').style.height = newHeight;
        }

   
        function applyTitleCSS() {
            document.getElementById('NoiDung').style.fontSize = "16px";
        }

      
        function applyContentCSS() {
            document.getElementById('NoiDung').style.fontSize = "30px";
        }
    </script>

</body>
</html>
