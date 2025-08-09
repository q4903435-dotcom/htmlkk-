<!DOCTYPE html>
<html lang="vi">
<head>
  <meta charset="UTF-8">
  <title>Menu Panel Lite - Bé iu</title>
  <style>
    body {
      font-family: 'Segoe UI', sans-serif;
      background-color: #f2f2f2;
      padding: 20px;
      color: #333;
    }

    .panel {
      background: white;
      max-width: 400px;
      margin: auto;
      padding: 20px;
      border-radius: 10px;
      box-shadow: 0 0 10px rgba(0,0,0,0.1);
    }

    h2 {
      text-align: center;
      margin-bottom: 20px;
      color: #0099cc;
    }

    .section {
      margin-bottom: 25px;
    }

    label {
      display: block;
      margin-top: 10px;
      font-weight: bold;
    }

    input[type=range] {
      width: 100%;
    }

    .checkbox-group label {
      font-weight: normal;
    }

    .checkbox-group input {
      margin-right: 8px;
    }

    .value {
      font-size: 14px;
      margin-left: 10px;
      color: #555;
    }

    button {
      margin-top: 20px;
      width: 100%;
      padding: 10px;
      border: none;
      background-color: #0099cc;
      color: white;
      font-size: 16px;
      border-radius: 5px;
      cursor: pointer;
    }

    button:hover {
      background-color: #0077aa;
    }
  </style>
</head>
<body>

  <div class="panel">
    <h2>🌟 Menu Panel Lite</h2>

    <div class="section">
      <label for="buff">🔧 Buff nhạy & độ mượt: <span id="buffValue">100</span></label>
      <input type="range" id="buff" min="1" max="200" value="100" oninput="updateValue('buff')">
    </div>

    <div class="section">
      <label>⚙️ Chức năng:</label>
      <div class="checkbox-group">
        <label><input type="checkbox" id="nhẹTâm"> Nhẹ tâm</label>
        <label><input type="checkbox" id="lockhead"> Lockhead</label>
        <label><input type="checkbox" id="dataFix"> Data fix rung</label>
        <label><input type="checkbox" id="fixLo"> Fix lố</label>
      </div>
    </div>

    <div class="section">
      <label for="config">🛠 Buff tối ưu: <span id="configValue">60</span></label>
      <input type="range" id="config" min="1" max="120" value="60" oninput="updateValue('config')">

      <label style="margin-top:10px;"><input type="checkbox" id="toiUuThietBi"> Tối ưu thiết bị</label>
    </div>

    <button onclick="submitPanel()">💾 Lưu cấu hình</button>
  </div>

  <script>
    function updateValue(id) {
      document.getElementById(id + "Value").innerText = document.getElementById(id).value;
    }

    function submitPanel() {
      const config = {
        buff: document.getElementById('buff').value,
        config: document.getElementById('config').value,
        chứcNăng: {
          nhẹTâm: document.getElementById('nhẹTâm').checked,
          lockhead: document.getElementById('lockhead').checked,
          dataFix: document.getElementById('dataFix').checked,
          fixLo: document.getElementById('fixLo').checked
        },
        tốiƯuThiếtBị: document.getElementById('toiUuThietBi').checked
      };
      console.log("Cấu hình đã lưu:", config);
      alert("✅ Cấu hình đã lưu thành công!");
    }
  </script>

</body>
</html>
