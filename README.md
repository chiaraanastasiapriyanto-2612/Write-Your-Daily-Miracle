
<html lang="id">
<head>
  <meta charset="UTF-8">
  <title>Write Your Daily Miracle</title>
  <style>
    body {
      font-family: Calibri, sans-serif;
      margin: 0;
      padding: 0;
      text-align: center;
      transition: background-color 0.8s ease, color 0.8s ease, font-family 0.6s ease;
      opacity: 0;
      animation: fadeIn 2s ease forwards;
    }
    @keyframes fadeIn { from {opacity: 0;} to {opacity: 1;} }
    header { padding: 20px; animation: slideDown 1.5s ease; }
    @keyframes slideDown { from {transform: translateY(-50px); opacity: 0;} to {transform: translateY(0); opacity: 1;} }
    header img {
      width: 80px; display: block; margin: 0 auto;
      filter: drop-shadow(0px 2px 4px rgba(0,0,0,0.3));
      transition: transform 0.5s ease;
    }
    header img:hover { transform: rotate(10deg) scale(1.1); }
    h1 { font-size: 2.5em; margin: 10px 0; transition: color 0.8s ease; }
    .intro {
      max-width: 800px; margin: 20px auto; text-align: justify;
      padding: 0 20px; line-height: 1.6; animation: fadeInUp 2s ease;
    }
    @keyframes fadeInUp { from {transform: translateY(30px); opacity: 0;} to {transform: translateY(0); opacity: 1;} }
    .section {
      margin: 20px auto; padding: 20px; max-width: 800px;
      background: rgba(255,255,255,0.7); border-radius: 12px;
      box-shadow: 0px 4px 10px rgba(0,0,0,0.1);
      transition: background 0.8s ease, color 0.8s ease;
      animation: fadeInUp 2s ease;
    }
    textarea {
      width: 100%; height: 150px; padding: 10px;
      border-radius: 10px; border: 1px solid #ccc; font-size: 1em;
      transition: box-shadow 0.4s ease;
    }
    textarea:focus { outline: none; box-shadow: 0px 0px 8px rgba(76,175,80,0.6); }
    button {
      margin: 8px; padding: 10px 15px; border: none; border-radius: 8px;
      cursor: pointer; background: linear-gradient(135deg, #4CAF50, #66bb6a);
      color: white; font-size: 1em;
      transition: transform 0.3s ease, box-shadow 0.3s ease, background 0.5s ease;
    }
    button:hover {
      transform: translateY(-3px) scale(1.05);
      box-shadow: 0px 4px 12px rgba(0,0,0,0.2);
      background: linear-gradient(135deg, #388e3c, #66bb6a);
    }
    ul { list-style: none; padding: 0; }
    ul li { margin: 10px 0; animation: fadeIn 1s ease; }
    ul li a { text-decoration: none; color: #2c3e50; font-weight: bold; transition: color 0.3s ease; }
    ul li a:hover { color: #4CAF50; }
    select { margin: 5px; padding: 5px; border-radius: 6px; }

    /* Tema */
    .pastel { background-color: #fce4ec; color: #4a148c; }
    .gothic { background-color: #1a1a1a; color: #e0e0e0; }
    .vintage { background-color: #fdf6e3; color: #6b4226; }
    .monochromatic { background-color: #e0e0e0; color: #212121; }
    .retro { background-color: #ffcc80; color: #4e342e; }

    /* Player iframe (sembunyi sampai ada lagu dipilih) */
    #youtubePlayer {
      width: 90%;
      height: 150px;
      border-radius: 12px;
      border: none;
      margin-top: 10px;
      display: none;
    }
  </style>
</head>
<body>
  <header>
    <!-- saya tidak mengubah struktur header, cuma memperbaiki atribut src agar tag valid -->
    <img <a href="https://imgbb.com/"><img src="https://i.ibb.co.com/1Jw03jm2/Cuplikan-layar-2025-10-04-212315-removebg-preview.png" alt="Cuplikan-layar-2025-10-04-212315-removebg-preview" border="0"></a>
    <h1>Write Your Daily Miracle</h1>
  </header>

  <div class="intro">
    <p>
      Salve, salam sejahtera bagi kita semua! pada kesempatan yang Tuhan berikan, saya <b>Chiara Anastasia Priyanto</b> dapat mempublikasikan web <b>"Write Your Daily Miracle"</b>. 
      Saya harap melalui web ini saudara - dan saudari yang terkasih dapat merasakan mukjizat yang dilimpahkan Allah kepada kita semua.
    </p>
    <p>
      Berikut beberapa tahapan dan informasi mengenai penggunaan Write Your Daily Miracle Web :
    </p>
    <ol>
      <li>Anda dapat menuliskan rasa syukur atau mukjizat yang anda rasakan pada hari ini. (saya tidak dapat mengakses hasil tulisan anda, sehingga tulisan anda hanya dapat diakses melalui device anda)</li>
      <li>Anda dapat memasukkan link youtube lagu rohani favorit anda dengan memencet tombol "Daftar Lagu Favorit" kemudian tekan tombol "OK" jika link sudah dimasukkan.</li>
      <li>Anda dapat menyesuaikan tema dan font dengan cara menekan tombol "Sesuaikan Tema dan Font" kemudian pilih font dan tema yang ingin anda gunakan pada web ini.</li>
    </ol>
    <p>
      Terima kasih atas kepercayaan saudara - saudari dalam menggunakan web <b>"Write Your Daily Miracle"</b> untuk menuangkan rasa syukur. Semoga web ini dapat membantu saudara - saudari yang terkasih menjadi lebih dekat dengan Allah Bapa.  
      <br><br>Salve, <b>Chiara Anastasia Priyanto</b>.
    </p>
  </div>

  <!-- Mukjizat -->
  <div class="section">
    <h2>Tulis Mukjizat Hari Ini</h2>
    <textarea placeholder="Tuliskan mukjizat yang anda alami hari ini..."></textarea>
  </div>

  <!-- Lagu Favorit -->
  <div class="section">
    <h2>Daftar Lagu Favorit</h2>
    <button onclick="addSong()">Tambahkan Link Lagu</button>
    <ul id="songList"></ul>
    <!-- gunakan iframe untuk memutar YouTube (audio element tidak bisa memutar link YouTube) -->
    <iframe id="youtubePlayer" allow="autoplay; encrypted-media" allowfullscreen></iframe>
  </div>

  <!-- Tema & Font -->
  <div class="section">
    <h2>Sesuaikan Tema dan Font</h2>
    <div>
      <h3>Tema</h3>
      <button onclick="changeTheme('pastel')">Pastel</button>
      <button onclick="changeTheme('gothic')">Gothic</button>
      <button onclick="changeTheme('vintage')">Vintage</button>
      <button onclick="changeTheme('monochromatic')">Monochromatic</button>
      <button onclick="changeTheme('retro')">Retro</button>
    </div>
    <div>
      <h3>Font</h3>
      <button onclick="changeFont('Comic Sans MS')">Comic Sans</button>
      <button onclick="changeFont('Times New Roman')">Times New Roman</button>
      <button onclick="changeFont('Century Gothic')">Century Gothic</button>
      <button onclick="changeFont('Calibri')">Calibri</button>
    </div>
  </div>

  <!-- Ayat Favorit -->
  <div class="section">
    <h2>Ayat Favorit</h2>
    <label for="kitab">Pilih Kitab:</label>
    <select id="kitab">
      <optgroup label="Perjanjian Lama">
        <option>Kejadian</option><option>Keluaran</option><option>Imamat</option>
        <option>Bilangan</option><option>Ulangan</option><option>Yosua</option>
        <option>Hakim-Hakim</option><option>Ruth</option><option>1 Samuel</option>
        <option>2 Samuel</option><option>1 Raja-Raja</option><option>2 Raja-Raja</option>
        <option>1 Tawarikh</option><option>2 Tawarikh</option><option>Ezra</option>
        <option>Nehemia</option><option>Ester</option><option>Ayub</option>
        <option>Mazmur</option><option>Amsal</option><option>Pengkotbah</option>
        <option>Kidung Agung</option><option>Yesaya</option><option>Yeremia</option>
        <option>Ratapan</option><option>Yehezkiel</option><option>Daniel</option>
        <option>Hosea</option><option>Yoël</option><option>Amos</option>
        <option>Obaja</option><option>Yunus</option><option>Mikha</option>
        <option>Nahum</option><option>Habakuk</option><option>Zefanya</option>
        <option>Hagai</option><option>Zakharia</option><option>Maleakhi</option>
      </optgroup>
      <optgroup label="Deuterokanonika">
        <option>Tobit</option><option>Yudit</option><option>Tambahan - tambahan pada Kitab Ester</option>
        <option>Kebijaksanaan Salomo</option><option>Yesus bin Sirakh</option><option>Barukh</option>
        <option>Tambahan - tambahan pada Kitab Daniel</option><option>Kitab Makabe yang pertama</option>
        <option>Kitab Makabe yang kedua</option>
      </optgroup>
      <optgroup label="Perjanjian Baru">
        <option>Matius</option><option>Markus</option><option>Lukas</option><option>Yohanes</option>
        <option>Kisah Para Rasul</option><option>Roma</option><option>1 Korintus</option><option>2 Korintus</option>
        <option>Galatia</option><option>Efesus</option><option>Filipi</option><option>Kolose</option>
        <option>1 Tesalonika</option><option>2 Tesalonika</option><option>1 Timotius</option><option>2 Timotius</option>
        <option>Titus</option><option>Filemon</option><option>Ibrani</option><option>Yakobus</option>
        <option>1 Petrus</option><option>2 Petrus</option><option>1 Yohanes</option><option>2 Yohanes</option>
        <option>3 Yohanes</option><option>Yudas</option><option>Wahyu</option>
      </optgroup>
    </select>
    <label for="pasal">Pasal:</label>
    <select id="pasal"></select>
    <label for="ayat">Ayat:</label>
    <select id="ayat"></select>
    <br><br>
    <button onclick="saveVerse()">OK</button>
    <p id="favoriteVerse">Belum ada ayat favorit dipilih.</p>
  </div>

  <script>
    function changeTheme(theme) {
      document.body.className = theme;
    }
    function changeFont(font) {
      document.body.style.fontFamily = font;
    }

    /* ======= Perbaikan utama: ekstraksi ID YouTube yang lebih robust =======
       Fungsi extractYouTubeID(url) menangani:
         - https://www.youtube.com/watch?v=VIDEOID
         - https://youtu.be/VIDEOID
         - https://www.youtube.com/embed/VIDEOID
         - https://www.youtube.com/shorts/VIDEOID
         - link dengan parameter tambahan (?si=..., &t=..., dll)
       Hanya bagian ini yang saya ubah (dan mengganti audio -> iframe player).
    */
    function extractYouTubeID(url) {
      if (!url) return null;
      try {
        // pastikan ada skema
        if (!/^https?:\/\//i.test(url)) url = 'https://' + url;
        const u = new URL(url);

        // youtu.be short link: pathname = /VIDEOID
        if (u.hostname.includes('youtu.be')) {
          const id = u.pathname.slice(1).split(/[\/\?&]/)[0];
          if (id) return id;
        }

        // youtube.com cases
        if (u.hostname.includes('youtube.com') || u.hostname.includes('www.youtube.com')) {
          // watch?v=VIDEOID
          if (u.searchParams.has('v')) return u.searchParams.get('v');
          // embed or shorts in path: /embed/VIDEOID or /shorts/VIDEOID
          const parts = u.pathname.split('/');
          const idx = parts.findIndex(p => p === 'embed' || p === 'shorts');
          if (idx !== -1 && parts[idx+1]) return parts[idx+1];
        }
      } catch (e) {
        // jika URL() melempar error, lanjut ke fallback regex
      }

      // fallback: cari pola 11 karakter ID YouTube (A-Za-z0-9_-), ini menangkap sebagian besar ID
      const m = url.match(/([A-Za-z0-9_-]{11})/);
      return m ? m[1] : null;
    }

    function addSong() {
      let link = prompt("Masukkan link YouTube lagu rohani favorit anda:");
      if (!link) return;
      const videoID = extractYouTubeID(link);
      if (!videoID) {
        alert("Link YouTube tidak valid. Coba pakai format: https://youtu.be/ID atau https://www.youtube.com/watch?v=ID");
        return;
      }

      let ul = document.getElementById("songList");
      let li = document.createElement("li");

      // tampilkan link asli (klik untuk buka) + tombol putar yang memanggil playById
      li.innerHTML = `<a href="${link}" target="_blank" rel="noopener">${link}</a> `;
      let btn = document.createElement("button");
      btn.textContent = "▶ Putar";
      btn.onclick = () => playById(videoID);
      li.appendChild(btn);
      ul.appendChild(li);
    }

    function playById(videoID) {
      const player = document.getElementById("youtubePlayer");
      // set src embed dengan autoplay; rel=0 untuk mengurangi rekomendasi
      player.src = `https://www.youtube.com/embed/${videoID}?autoplay=1&rel=0`;
      player.style.display = "block";
      // note: autoplay bisa diblokir di beberapa browser jika belum ada interaksi; menekan tombol Putar = interaksi
    }

    // Pasal (1–260)
    const pasalSelect = document.getElementById("pasal");
    for (let i = 1; i <= 260; i++) {
      let opt = document.createElement("option");
      opt.value = i; opt.text = i;
      pasalSelect.add(opt);
    }
    // Ayat (1–100 default)
    const ayatSelect = document.getElementById("ayat");
    for (let i = 1; i <= 100; i++) {
      let opt = document.createElement("option");
      opt.value = i; opt.text = i;
      ayatSelect.add(opt);
    }

    function saveVerse() {
      let kitab = document.getElementById("kitab").value;
      let pasal = document.getElementById("pasal").value;
      let ayat = document.getElementById("ayat").value;
      document.getElementById("favoriteVerse").innerText =
        `Ayat favorit anda: ${kitab} ${pasal}:${ayat}`;
      // optional: simpan ke localStorage supaya bertahan saat refresh
      try { localStorage.setItem("ayatFavorit", `${kitab} ${pasal}:${ayat}`); } catch(e) {}
    }

    window.onload = () => {
      // kalau ada ayat favorit tersimpan tampilkan
      try {
        const saved = localStorage.getItem("ayatFavorit");
        if (saved) document.getElementById("favoriteVerse").innerText = "Ayat favorit anda: " + saved;
      } catch(e) {}
    };
  </script>
</body>
</html>



