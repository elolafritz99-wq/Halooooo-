<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Open it 🧸</title>
  <link href="https://fonts.googleapis.com/css2?family=Baloo+2:wght@400;600&display=swap" rel="stylesheet">
  <style>
    body {
      margin: 0;
      height: 100vh;
      background: linear-gradient(135deg, #ffe0c3, #ffd6e7);
      display: flex;
      justify-content: center;
      align-items: center;
      font-family: 'Baloo 2', cursive;
    }

    .card {
      background: #fff;
      padding: 40px;
      border-radius: 35px;
      text-align: center;
      width: 330px;
      box-shadow: 0 15px 30px rgba(0,0,0,0.15);
    }

    .bear {
      font-size: 70px;
      animation: bounce 1.5s infinite;
    }

    h1 {
      color: #ff5c8a;
      font-size: 22px;
      margin: 20px 0;
    }

    button {
      margin-top: 15px;
      padding: 12px 30px;
      border: none;
      border-radius: 30px;
      background: #ff9fbd;
      color: white;
      font-size: 15px;
      cursor: pointer;
      transition: 0.3s;
    }

    button:hover {
      background: #ff6fa5;
      transform: scale(1.08);
    }

    .page {
      display: none;
    }

    .page.active {
      display: block;
    }

    @keyframes bounce {
      0%, 100% { transform: translateY(0); }
      50% { transform: translateY(-10px); }
    }
  </style>
</head>
<body>

  <div class="card">
    <div class="bear">🧸</div>

    <!-- Intro -->
    <div class="page active">
      <h1>Open it 💕</h1>
      <button onclick="nextPage()">Open 🧸</button>
    </div>

    <!-- Page 1 -->
    <div class="page">
      <h1>naa koy e sultii</h1>
      <button onclick="nextPage()">Next page ➡️</button>
    </div>

    <!-- Page 2 -->
    <div class="page">
      <h1>halaaaa halaaaa sure jud ka?</h1>
      <button onclick="nextPage()">Next page ➡️</button>
    </div>

    <!-- Page 3 -->
    <div class="page">
      <h1>secret para bibo 😍😍😍</h1>
      <button onclick="restart()">Replay 🔁</button>
    </div>

  </div>

  <script>
    let currentPage = 0;
    const pages = document.querySelectorAll(".page");

    function nextPage() {
      pages[currentPage].classList.remove("active");
      currentPage++;
      pages[currentPage].classList.add("active");
    }

    function restart() {
      pages[currentPage].classList.remove("active");
      currentPage = 0;
      pages[currentPage].classList.add("active");
    }
  </script>

</body>
</html>
