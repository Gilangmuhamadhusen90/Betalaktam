<html lang="id">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0"
  <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@500;700&family=Poppins:wght@400;600&display=swap" rel="stylesheet">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: 'Poppins', sans-serif;
      background: linear-gradient(to right, #0f2027, #203a43, #2c5364);
      color: white;
      overflow-x: hidden;
    }

    header {
      text-align: center;
      padding: 60px 20px 30px;
      background: rgba(255,255,255,0.05);
      box-shadow: 0 4px 20px rgba(0,0,0,0.3);
    }

    header h1 {
      font-family: 'Playfair Display', serif;
      font-size: 2.8em;
      color: #f4c430;
      text-shadow: 0 0 10px #f4c430;
    }

    header p {
      font-size: 1.2em;
      margin-top: 10px;
      color: #f5f5f5;
    }

    section {
      max-width: 1100px;
      margin: 60px auto;
      padding: 20px;
    }

    .produk {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 30px;
    }

    .card {
      background: rgba(255,255,255,0.1);
      border-radius: 20px;
      overflow: hidden;
      text-align: center;
      padding-bottom: 20px;
      transition: transform 0.3s, box-shadow 0.3s;
    }

    .card:hover {
      transform: translateY(-8px);
      box-shadow: 0 10px 30px rgba(255,255,255,0.2);
    }

    .card img {
      width: 100%;
      height: 200px;
      object-fit: cover;
      border-bottom: 2px solid #f4c430;
    }

    .card h3 {
      margin-top: 15px;
      color: #f4c430;
      font-family: 'Playfair Display', serif;
    }

    .card p {
      margin: 10px 20px;
      font-size: 0.95em;
      color: #f0f0f0;
    }

    footer {
      text-align: center;
      background: rgba(0,0,0,0.5);
      padding: 40px 20px;
      margin-top: 40px;
      border-top: 1px solid #f4c430;
    }

    .like-btn {
      background: #f4c430;
      border: none;
      color: #000;
      font-weight: bold;
      padding: 10px 20px;
      border-radius: 25px;
      cursor: pointer;
      transition: background 0.3s;
    }

    .like-btn:hover {
      background: #ffdf70;
    }

    .comments {
      margin-top: 20px;
    }

    textarea {
      width: 80%;
      max-width: 400px;
      height: 80px;
      border-radius: 10px;
      padding: 10px;
      border: none;
      outline: none;
      resize: none;
      font-family: 'Poppins', sans-serif;
    }

    button.comment-btn {
      margin-top: 10px;
      padding: 8px 16px;
      border: none;
      border-radius: 8px;
      background: #f4c430;
      cursor: pointer;
      font-weight: bold;
    }

    .comment-list {
      margin-top: 15px;
      text-align: left;
      max-width: 500px;
      margin-left: auto;
      margin-right: auto;
    }

    .comment-item {
      background: rgba(255,255,255,0.1);
      border-radius: 8px;
      padding: 8px 12px;
      margin-bottom: 8px;
    }
  </style>
</head>
<body>
  <audio autoplay loop>
    <source src="dreams.mp3" type="audio/mpeg">
  </audio>

  <header>
    <h1>Betalaktam Penisilin</h1>
    <p>PT Meprofarm Pharmaceutical Industries</p>
  </header>

  <section>
    <div class="produk">
      <div class="card">
        <img src="Amoxicillin.png" alt="Amoxicillin">
        <h3>Amoxicillin</h3>
        <p>Antibiotik spektrum luas yang efektif melawan berbagai infeksi bakteri. Digunakan untuk infeksi saluran pernapasan, telinga, dan kulit.</p>
      </div>

      <div class="card">
        <img src="Ancla.png" alt="Ancla">
        <h3>Ancla</h3>
        <p>Produk turunan penisilin dengan efektivitas tinggi terhadap bakteri gram positif dan negatif. Diformulasikan untuk efektivitas optimal.</p>
      </div>

      <div class="card">
        <img src="Clamixin.png" alt="Clamixin">
        <h3>Clamixin</h3>
        <p>Antibiotik kombinasi yang bekerja menghentikan pertumbuhan bakteri penyebab infeksi pada sistem pernapasan dan pencernaan.</p>
      </div>

      <div class="card">
        <img src="Co-Amoxiclav.png" alt="Co-Amoxiclav">
        <h3>Co-Amoxiclav</h3>
        <p>Kombinasi Amoxicillin dan Clavulanic Acid yang meningkatkan efektivitas terhadap bakteri yang resisten terhadap antibiotik biasa.</p>
      </div>
    </div>
  </section>

  <footer>
    <div>
      <button class="like-btn" onclick="likeWebsite()"> Like (<span id='likeCount'>0</span>)</button>
    </div>

    <div class="comments">
      <h3>Komentar</h3>
      <textarea id="commentInput" placeholder="Tulis komentar Anda..."></textarea><br>
      <button class="comment-btn" onclick="addComment()">Kirim</button>
      <div class="comment-list" id="commentList"></div>
    </div>

    <p style="margin-top:30px; font-size:0.9em; color:#ccc;">© 2025 Gilang Muhamad Husen. All Rights Reserved.</p>
  </footer>

  <script>
    let likes = 0;
    function likeWebsite() {
      likes++;
      document.getElementById("likeCount").innerText = likes;
    }

    function addComment() {
      const input = document.getElementById('commentInput');
      const list = document.getElementById('commentList');
      if (input.value.trim() !== "") {
        const item = document.createElement('div');
        item.className = 'comment-item';
        item.innerText = input.value;
        list.prepend(item);
        input.value = "";
      }
    }
  </script>
</body>
</html>

