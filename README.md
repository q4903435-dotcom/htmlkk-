<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <title>REGEDIT MENU - ĐĂNG NHẬP</title>
    <style>
        body {
            background-color: #111;
            color: white;
            font-family: 'Segoe UI', sans-serif;
            padding: 20px;
        }
        .container {
            max-width: 600px;
            margin: auto;
            background: #1f1f1f;
            padding: 25px;
            border-radius: 12px;
            box-shadow: 0 0 10px #00ffc8;
        }
        h1 {
            text-align: center;
            color: #00ffc8;
        }
        label {
            margin-top: 10px;
            display: block;
        }
        input[type="text"], input[type="file"], input[type="range"] {
            width: 100%;
            padding: 8px;
            margin: 8px 0 15px;
            border-radius: 5px;
            border: none;
        }
        button {
            width: 100%;
            padding: 12px;
            background-color: #00ffc8;
            color: black;
            font-weight: bold;
            font-size: 16px;
            border: none;
            border-radius: 6px;
            cursor: pointer;
        }
        button:hover {
            background-color: #00d9a0;
        }
        .checkbox-group {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
        }
        .checkbox-group label {
            flex: 1 1 45%;
            background: #2c2c2c;
            padding: 8px;
            border-radius: 6px;
        }
        #output {
            margin-top: 20px;
            background: #000;
            padding: 10px;
            border-radius: 6px;
            white-space: pre-wrap;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>ĐĂNG NHẬP MENU REGEDIT</h1>
        <label for="key">🔑 Nhập KEY:</label>
        <input type="text" id="key" placeholder="Nhập KEY tại đây..." />
        <button onclick="verifyKey()">XÁC NHẬN KEY</button>

        <div id="menu" style="display:none; margin-top: 25px;">
            <label>🎮 Chức năng hỗ trợ:</label>
            <div class="checkbox-group">
                <label><input type="checkbox"> Nhẹ tâm</label>
                <label><input type="checkbox"> Bám đầu</label>
                <label><input type="checkbox"> Fix rung</label>
                <label><input type="checkbox"> Fix lố</label>
                <label><input type="checkbox"> Fix nặng tâm</label>
                <label><input type="checkbox"> AIMLOCK</label>
                <label><input type="checkbox"> Đạn thẳng</label>
            </div>

            <label for="dpi">📏 Chỉnh DPI: <output id="dpiValue">500</output></label>
            <input type="range" id="dpi" min="1" max="1000" value="500" oninput="dpiValue.value = dpi.value">

            <label for="file">📁 Chọn file REGEDIT:</label>
            <input type="file" id="file" accept=".cpp,.txt" />

            <button onclick="loadRegedit()">KÍCH HOẠT REGEDIT</button>

            <div id="output"></div>
        </div>
    </div>

    <script>
        const correctKey = "123456";

        function verifyKey() {
            const keyInput = document.getElementById("key").value.trim();
            const menuDiv = document.getElementById("menu");
            const output = document.getElementById("output");

            if (keyInput === correctKey) {
                menuDiv.style.display = "block";
                output.innerText = "✅ KEY hợp lệ. Đã mở khóa chức năng!";
            } else {
                menuDiv.style.display = "none";
                output.innerText = "❌ KEY sai. Vui lòng thử lại.";
            }
        }

        function loadRegedit() {
            const fileInput = document.getElementById("file");
            const output = document.getElementById("output");

            if (!fileInput.files.length) {
                output.innerText = "⚠️ Vui lòng chọn file REGEDIT.";
                return;
            }

            const reader = new FileReader();
            reader.onload = function(e) {
                output.innerText = "📄 REGEDIT:\n\n" + e.target.result;
            };
            reader.readAsText(fileInput.files[0]);
        }
    </script>
</body>
</html>
