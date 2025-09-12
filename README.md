# thuyettrinhtoan
thuyet trinh toan
<!DOCTYPE html>
<html lang="vi">
<head>
  <meta charset="UTF-8" />
  <title>Thuyết Trình Toán 10 - Định Lý Sin</title>
  <style>
    /* ... (giữ nguyên phần CSS như của bạn) ... */
    * { box-sizing: border-box; }
    body { margin: 0; font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif; color: #fff; background: linear-gradient(135deg, #0f2027, #203a43, #2c5364); overflow-x: hidden; animation: bgFlow 20s infinite alternate; position: relative; }
    @keyframes bgFlow { 0% { background-position: left top; } 100% { background-position: right bottom; } }
    .slide { max-width: 900px; margin: 80px auto; background: rgba(255, 255, 255, 0.07); border-radius: 15px; padding: 40px; box-shadow: 0 0 30px rgba(255, 255, 255, 0.2); backdrop-filter: blur(8px); animation: fadeIn 1.5s ease-in-out; transition: opacity 0.5s ease, filter 0.5s ease; position: relative; z-index: 10; }
    .slide.dimmed { opacity: 0.4; filter: brightness(0.7); }
    @keyframes fadeIn { 0% { opacity: 0; transform: translateY(30px); } 100% { opacity: 1; transform: translateY(0); } }
    h1, h2 { text-align: center; color: #ffda79; }
    .team, .contact { text-align: center; font-style: italic; margin-bottom: 20px; color: #cceaff; z-index: 10; position: relative; }
    .section { margin-top: 30px; animation: fadeIn 2s; }
    .box { background-color: rgba(255, 255, 255, 0.1); padding: 20px; border-left: 5px solid #ffda79; border-radius: 10px; margin: 15px 0; color: #e0f7ff; }
    .mini-game { background-color: rgba(255, 255, 153, 0.2); border-left: 5px solid #ffcc00; }
    .exercise { background-color: rgba(173, 216, 230, 0.2); border-left: 5px solid #33d9b2; }
    button { background-color: #ffb142; color: black; border: none; padding: 10px 20px; border-radius: 8px; cursor: pointer; font-weight: bold; margin-top: 10px; transition: 0.3s; }
    button:hover { background-color: #ff793f; transform: scale(1.05); }
    input[type='text'] { padding: 8px; border-radius: 5px; border: none; margin-right: 10px; width: 120px; }
    table { width: 100%; border-collapse: collapse; background-color: rgba(255, 255, 255, 0.08); margin-top: 20px; }
    th, td { padding: 10px; border: 1px solid #ffffff33; text-align: center; color: #fff; }
    th { background-color: #ffda79; color: #000; }
    .snowflake { position: fixed; top: -10px; background: white; border-radius: 50%; opacity: 0.8; pointer-events: none; animation-name: fall; animation-timing-function: linear; animation-iteration-count: infinite; z-index: 5; }
    @keyframes fall { to { transform: translateY(100vh); } }
    @media screen and (max-width: 600px) { .slide { padding: 20px; margin: 30px 10px; } }
  </style>
</head>
<body>
  <div class="slide">
    <h1>Thuyết Trình Toán 10</h1>
    <h2>Định Lý Sin</h2>

    <div class="team">
      Thành viên: Nguyễn Lâm, Phạm Cao Phong, Tuấn, Tuấn Khang , Quang Hải <br />
      Lớp: 10XH2
    </div>

    <div class="section">
      <h2>1. Định Lý Sin</h2>
      <div class="box">
        Trong tam giác ABC bất kỳ:
        <pre>a / sin A = b / sin B = c / sin C</pre>
        ➤ Dùng để tính cạnh hoặc góc khi biết 2 góc và 1 cạnh, hoặc 2 cạnh và 1 góc đối diện.
      </div>
      <div class="box" style="background-color: rgba(255, 230, 230, 0.12); border-left: 5px solid #fd79a8; margin-top: 10px;">
        <strong>Mẹo nhớ “Thần chú Sin”:</strong> <br>
        <em>
          <b>“Sin đối – Cạnh chia Sin Góc!”</b><br>
          <span style="color:#ffd700">
            → Muốn biết cạnh thì lấy cạnh chia cho Sin góc đối diện!<br>
            Muốn biết góc thì lấy cạnh chia Sin, tra ngược lại!
          </span>
        </em><br>
        <strong>Ví dụ vui:</strong> <br>
        Hãy nhớ câu: <b>“Áp lực cuộc đời cũng giống như Sin: cứ đối diện mà chia sẻ!”</b>
      </div>
    </div>

    <div class="section">
      <h2>2. Ví Dụ Minh Họa</h2>
      <div class="box">
        Cho tam giác ABC, a = 7cm, A = 30°, b = 9cm, B = 45°. Tính góc C.<br><br>
        <strong>Lời giải:</strong><br>
        Áp dụng định lý Sin:<br>
        <pre>a/sinA = b/sinB ⇒ 7/sin(30°) = 9/sin(45°)</pre>
        Giải ra ta được:<br>
        sin(30°) = 0.5, sin(45°) ≈ 0.707<br>
        7 / 0.5 = 9 / 0.707<br>
        14 = 12.73 (gần đúng)<br>
        (Sử dụng tính chất tổng các góc tam giác = 180° để tìm góc C)
      </div>
    </div>

    <div class="section">
      <h2>3. Mini Game</h2>
      <div class="box mini-game">
        <strong>Câu hỏi 1:</strong><br />
        Trong tam giác ABC, a = 8, A = 30°, b = 10, B = 45°. Góc C gần đúng bằng bao nhiêu?<br />
        <input type="text" id="answer1" placeholder="Nhập đáp án (độ)" />
        <button onclick="checkAnswer1()">Kiểm tra</button>
        <p id="result1"></p>
      </div>

      <div class="box mini-game" style="margin-top: 20px;">
        <strong>Câu hỏi 2:</strong><br />
        Cho tam giác ABC có a = 5, b = 7, c = 8. Tính góc C (độ).<br />
        <input type="text" id="answer2" placeholder="Nhập đáp án (độ)" />
        <button onclick="checkAnswer2()">Kiểm tra</button>
        <p id="result2"></p>
      </div>
    </div>

    <div class="section">
      <h2>4. Bài Tập Cơ Bản</h2>
      <div class="box exercise">
        <ul>
          <li>1. Cho tam giác có a = 6cm, b = 8cm, góc C = 90°. Tính cạnh c.</li>
          <li>2. Cho tam giác có A = 60°, B = 45°, a = 5cm. Tính cạnh b.</li>
          <li>3. Tìm góc C trong tam giác có a = 7, b = 10, c = 12.</li>
        </ul>
      </div>
    </div>

    <div class="section">
      <h2>5. Bảng Những Điều Cần Nhớ</h2>
      <div class="box">
        <table>
          <thead>
            <tr>
              <th>Định Lý</th>
              <th>Công Thức</th>
              <th>Ứng Dụng</th>
            </tr>
          </thead>
          <tbody>
            <tr>
              <td>Định Lý Sin</td>
              <td>a / sin A = b / sin B = c / sin C</td>
              <td>Tính cạnh hoặc góc trong tam giác bất kỳ</td>
            </tr>
          </tbody>
        </table>
      </div>
    </div>

    <div class="contact">
      Liên hệ nhóm qua Zalo:
      <a href="https://zalo.me/0359710381" target="_blank" style="color:#ffda79; text-decoration: underline;">
        0359710381
      </a>
    </div>
  </div>

  <script>
    function checkAnswer1() {
      const answer = document.getElementById('answer1').value.trim();
      const result = document.getElementById('result1');
      if (answer === '') {
        result.textContent = 'Vui lòng nhập đáp án.';
        result.style.color = 'yellow';
        return;
      }
      const ansNum = Number(answer);
      if (ansNum >= 100 && ansNum <= 110) {
        result.textContent = 'Chính xác! Góc C ≈ 105°.';
        result.style.color = '#00ff00';
      } else {
        result.textContent = 'Sai rồi! Đáp án đúng là khoảng 105°. Hãy thử lại hoặc xem đáp án.';
        result.style.color = 'red';
      }
    }

    function checkAnswer2() {
      const answer = document.getElementById('answer2').value.trim();
      const result = document.getElementById('result2');
      if (answer === '') {
        result.textContent = 'Vui lòng nhập đáp án.';
        result.style.color = 'yellow';
        return;
      }
      const ansNum = Number(answer);
      if (ansNum >= 60 && ansNum <= 65) {
        result.textContent = 'Chính xác! Góc C ≈ 63°.';
        result.style.color = '#00ff00';
      } else {
        result.textContent = 'Sai rồi! Đáp án đúng khoảng 63°. Hãy thử lại hoặc xem đáp án.';
        result.style.color = 'red';
      }
    }

    // Hiệu ứng mờ đậm slide khi chuột di chuyển ra ngoài 2 bên
    document.body.addEventListener('mousemove', e => {
      const slide = document.querySelector('.slide');
      const width = window.innerWidth;
      const mouseX = e.clientX;

      // Nếu chuột nằm trong 30% giữa màn hình thì sáng, ngoài ra mờ đi
      if (mouseX > width * 0.35 && mouseX < width * 0.65) {
        slide.classList.remove('dimmed');
      } else {
        slide.classList.add('dimmed');
      }
    });

    // Khi chuột rời khỏi body thì cũng mờ slide
    document.body.addEventListener('mouseleave', () => {
      const slide = document.querySelector('.slide');
      slide.classList.add('dimmed');
    });

    // Khi chuột vào body thì sáng slide
    document.body.addEventListener('mouseenter', () => {
      const slide = document.querySelector('.slide');
      slide.classList.remove('dimmed');
    });

    // Tạo hiệu ứng tuyết rơi
    const numSnowflakes = 30;

    function createSnowflake() {
      const snowflake = document.createElement('div');
      snowflake.classList.add('snowflake');

      // Kích thước ngẫu nhiên
      const size = Math.random() * 7 + 3 + 'px';
      snowflake.style.width = size;
      snowflake.style.height = size;

      // Vị trí ngang ban đầu
      snowflake.style.left = Math.random() * window.innerWidth + 'px';

      // Thời gian rơi ngẫu nhiên từ 7 đến 15 giây
      const duration = Math.random() * 8 + 7;
      snowflake.style.animationDuration = duration + 's';

      // Độ mờ ngẫu nhiên
      snowflake.style.opacity = Math.random() * 0.5 + 0.3;

      document.body.appendChild(snowflake);

      // Khi kết thúc animation, snowflake sẽ được reset để rơi lại
      snowflake.addEventListener('animationiteration', () => {
        snowflake.style.left = Math.random() * window.innerWidth + 'px';
      });

      return snowflake;
    }

    for (let i = 0; i < numSnowflakes; i++) {
      createSnowflake();
    }
  </script>
</body>
</html>
