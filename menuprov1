<!DOCTYPE html>
<html lang="vi">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>H5GG Control Panel</title>
  <style>
    body {
      font-family: 'Segoe UI', sans-serif;
      background: #0e0e0e;
      color: #fff;
      padding: 20px;
    }

    .menu-box {
      max-width: 450px;
      margin: auto;
      background: #1a1a1a;
      border-radius: 12px;
      padding: 20px;
      box-shadow: 0 0 20px rgba(0, 255, 200, 0.15);
    }

    h2 {
      text-align: center;
      margin-bottom: 20px;
      color: #00ffc3;
    }

    .form-control {
      display: flex;
      align-items: center;
      justify-content: space-between;
      margin: 12px 0;
      padding: 10px 14px;
      background: #2a2a2a;
      border-radius: 8px;
    }

    label {
      font-size: 16px;
    }

    input[type="checkbox"] {
      transform: scale(1.3);
      cursor: pointer;
    }

    .run-btn {
      width: 100%;
      padding: 12px;
      margin-top: 20px;
      background: #00b894;
      color: white;
      border: none;
      border-radius: 10px;
      font-size: 16px;
      font-weight: bold;
      transition: background 0.3s ease;
    }

    .run-btn:hover {
      background: #00cec9;
      cursor: pointer;
    }

    .footer {
      text-align: center;
      margin-top: 20px;
      font-size: 14px;
      color: #888;
    }
  </style>
</head>
<body>

  <div class="menu-box">
    <h2>🛠️ H5GG MENU FORM</h2>

    <div class="form-control">
      <label>🌿 Nhẹ Tâm</label>
      <input type="checkbox" id="light_crosshair">
    </div>

    <div class="form-control">
      <label>🛠️ Fix Lố</label>
      <input type="checkbox" id="fix_lo">
    </div>

    <div class="form-control">
      <label>🔧 Fix Rung</label>
      <input type="checkbox" id="fix_rung">
    </div>

    <div class="form-control">
      <label>🔥 Fix Nặng Tâm</label>
      <input type="checkbox" id="heavy_crosshair">
    </div>

    <div class="form-control">
      <label>🎯 AimHead</label>
      <input type="checkbox" id="aim_head">
    </div>

    <div class="form-control">
      <label>🛡️ AntiBan</label>
      <input type="checkbox" id="anti_ban">
    </div>

    <div class="form-control">
      <label>🎯 AimLock</label>
      <input type="checkbox" id="aim_lock">
    </div>

    <div class="form-control">
      <label>🤖 Aimbot</label>
      <input type="checkbox" id="aim_bot">
    </div>

    <button class="run-btn" onclick="activateFeatures()">🚀 Kích Hoạt Tính Năng</button>

    <div class="footer">© 2025 H5GG UI by DevPro</div>
  </div>

  <script>
    function activateFeatures() {
      const features = {
        light_crosshair: document.getElementById('light_crosshair').checked,
        fix_lo: document.getElementById('fix_lo').checked,
        fix_rung: document.getElementById('fix_rung').checked,
        heavy_crosshair: document.getElementById('heavy_crosshair').checked,
        aim_head: document.getElementById('aim_head').checked,
        anti_ban: document.getElementById('anti_ban').checked,
        aim_lock: document.getElementById('aim_lock').checked,
        aim_bot: document.getElementById('aim_bot').checked
      };

      for (const [key, isEnabled] of Object.entries(features)) {
        if (isEnabled) {
          runH5GGScript(key);
        }
      }

      alert("✅ Đã kích hoạt các chức năng được chọn!");
    }

    function runH5GGScript(scriptName) {
      // Đây là nơi bạn gắn mã của từng script H5GG
      switch (scriptName) {
        case 'light_crosshair':
          h5gg.setValueAt(0x11111111, "float", 1.0);
          break;
        case 'fix_lo':
          h5gg.setValueAt(0x22222222, "float", 0.5);
          break;
        case 'fix_rung':
          h5gg.setValueAt(0x33333333, "float", 0.0);
          break;
        case 'heavy_crosshair':
          h5gg.setValueAt(0x44444444, "float", 3.0);
          break;
        case 'aim_head':
          h5gg.setValueAt(0x55555555, "float", 999.0);
          break;
        case 'anti_ban':
          h5gg.setValueAt(0x66666666, "byte", 0);
          break;
        case 'aim_lock':
          h5gg.setValueAt(0x77777777, "float", 1.0);
          break;
        case 'aim_bot':
          h5gg.setValueAt(0x88888888, "float", 5.0);
          break;
      }
    }
  </script>

</body>
</html>
