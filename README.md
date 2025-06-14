<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>DASEN - Layanan Multi Usaha Desa</title>
  <style>
    body { font-family: Arial, sans-serif; background: #f9f9f9; margin: 0; padding: 0; }
    header { background: #0a6cff; color: white; padding: 20px; text-align: center; }
    header img.logo { max-height: 50px; display: block; margin: 0 auto 10px; }
    nav { background: #e0e0e0; display: flex; flex-wrap: nowrap; overflow-x: auto; padding: 10px; white-space: nowrap; }
    nav button { background: #fff; border: 1px solid #ccc; border-radius: 5px; padding: 8px 12px; margin-right: 8px; cursor: pointer; font-size: 14px; }
    nav button.active { background: #0a6cff; color: white; border-color: #0a6cff; }
    section { padding: 15px; margin: 10px; background: white; border-radius: 10px; box-shadow: 0 2px 8px rgba(0,0,0,0.1); display: none; }
    section.active { display: block; }
    h2 { color: #0a6cff; font-size: 18px; }
    .paket, .testimonial { margin-bottom: 10px; font-size: 14px; }
    .formulir label { display: block; margin-top: 10px; font-size: 14px; }
    .formulir input, .formulir select { width: 100%; padding: 8px; margin-top: 5px; border-radius: 5px; border: 1px solid #ccc; font-size: 14px; }
    .wa-button { display: inline-block; background: #25D366; color: white; padding: 10px; text-align: center; width: 100%; text-decoration: none; border-radius: 5px; margin-top: 20px; font-weight: bold; border: none; cursor: pointer; font-size: 16px; }
    .galeri img { width: 100%; border-radius: 8px; margin-bottom: 10px; }
    .testimonial { padding: 10px; border-left: 4px solid #0a6cff; background: #f1f7ff; border-radius: 5px; font-size: 14px; }
    footer { text-align: center; font-size: 12px; color: #666; padding: 20px 10px; }
    ul.coverage { margin: 10px 0 20px; padding-left: 20px; font-size: 14px; }
  </style>
</head>
<body>
  <header>
    <img src="gg.jpg" alt="Logo Dasen" class="logo">
    <h1 style="font-size: 20px;">DASEN - Layanan Multi Usaha Desa</h1>
    <p style="font-size: 14px;">Internet | Konter | CCTV | Air Masak | Makeup</p>
  </header>

  <nav>
    <button onclick="tampilkan('internet', event)" class="active">Internet</button>
    <button onclick="tampilkan('konter', event)">Konter</button>
    <button onclick="tampilkan('cctv', event)">CCTV</button>
    <button onclick="tampilkan('air', event)">Air</button>
    <button onclick="tampilkan('makeup', event)">Makeup</button>
    <button onclick="tampilkan('kontak', event)">Kontak</button>
  </nav>

  <section id="internet" class="active">
    <h2>Paket Internet</h2>
    <div class="paket">🔹 10 Mbps – Rp 100.000/bln</div>
    <div class="paket">🔹 20 Mbps – Rp 150.000/bln</div>
    <div class="paket">🔹 30 Mbps – Rp 200.000/bln</div>

    <h2>Wilayah Jangkauan</h2>
    <ul class="coverage">
      <li>Desa A</li>
      <li>Desa B</li>
      <li>Dusun C</li>
      <li>Dusun D</li>
    </ul>

    <h2>Formulir Pendaftaran</h2>
    <form class="formulir" onsubmit="return handleForm(this)">
      <label for="nama">Nama:</label>
      <input type="text" id="nama" required>

      <label for="alamat">Alamat:</label>
      <input type="text" id="alamat" required>

      <label for="lokasi">Lokasi (Desa/Dusun):</label>
      <input type="text" id="lokasi" required>

      <label for="wa">Nomor WhatsApp:</label>
      <input type="text" id="wa" required>

      <label for="paket">Paket yang Dipilih:</label>
      <select id="paket" required>
        <option value="10 Mbps">10 Mbps – Rp 100.000</option>
        <option value="20 Mbps">20 Mbps – Rp 150.000</option>
        <option value="30 Mbps">30 Mbps – Rp 200.000</option>
      </select>

      <button type="submit" class="wa-button">Kirim via WhatsApp</button>
    </form>

    <h2>Galeri Internet</h2>
    <div class="galeri">
      <img src="https://via.placeholder.com/800x400?text=Foto+Pemasangan" alt="">
      <img src="https://via.placeholder.com/800x400?text=Teknisi" alt="">
    </div>

    <h2>Testimoni Pelanggan</h2>
    <div class="testimonial">"Internet stabil dan cepat!" – Ibu Sari</div>
  </section>

  <section id="konter">
    <h2>Konter Pulsa & Aksesoris</h2>
    <p>Kami menyediakan layanan isi ulang pulsa all operator, paket data internet, dan menjual berbagai aksesoris HP seperti charger, headset, casing, kartu perdana, dan lainnya. Cocok untuk kebutuhan komunikasi dan gaya Anda.</p>
    <p>Kami juga melayani transaksi keuangan digital seperti:</p>
    <ul>
      <li>Tarik tunai e-wallet (Dana, OVO, GoPay)</li>
      <li>Top up saldo & game</li>
      <li>Pembayaran token listrik, PDAM, BPJS, dan lainnya</li>
    </ul>
    <div class="galeri">
      <img src="https://via.placeholder.com/800x400?text=Etalase+Aksesoris" alt="">
      <img src="https://via.placeholder.com/800x400?text=Display+HP" alt="">
    </div>
  </section>

  <section id="cctv">
    <h2>Pasang & Servis CCTV</h2>
    <p>Layanan pemasangan, servis, dan pemantauan CCTV rumah dan kantor.</p>
    <div class="galeri">
      <img src="https://via.placeholder.com/800x400?text=Instalasi+CCTV" alt="">
      <img src="https://via.placeholder.com/800x400?text=Teknisi+CCTV+di+Lapangan" alt="">
      <img src="https://via.placeholder.com/800x400?text=Monitor+Pemantauan" alt="">
    </div>
  </section>

  <section id="air">
    <h2>Isi Ulang Air Masak</h2>
    <p>Layanan isi ulang air masak higienis dan bersih untuk warga sekitar.</p>
    <div class="galeri">
      <img src="https://via.placeholder.com/800x400?text=Depot+Air" alt="">
    </div>
  </section>

  <section id="makeup">
    <h2>Jasa Makeup (Rias)</h2>
    <p>Makeup untuk acara pernikahan, wisuda, dan lain-lain oleh perias profesional.</p>
    <div class="galeri">
      <img src="https://via.placeholder.com/800x400?text=Makeup+Client" alt="">
    </div>
  </section>

  <section id="kontak">
    <h2>Kontak & Bantuan</h2>
    <p>Alamat Usaha: Desa Air Satan</p>
    <p>Telepon: <a href="https://wa.me/6281272197728">0812-7219-7728</a></p>
  </section>

  <footer>
    &copy; 2025 DASEN Multi Usaha Desa
  </footer>

  <script>
    function handleForm(form) {
      const nama = document.getElementById('nama').value;
      const alamat = document.getElementById('alamat').value;
      const lokasi = document.getElementById('lokasi').value;
      const wa = document.getElementById('wa').value;
      const paket = document.getElementById('paket').value;
      const message = `Halo, saya ingin daftar internet:\nNama: ${nama}\nAlamat: ${alamat}\nLokasi: ${lokasi}\nNo. WA: ${wa}\nPaket: ${paket}`;
      const waLink = `https://wa.me/6281272197728?text=${encodeURIComponent(message)}`;
      window.open(waLink, '_blank');
      return false;
    }

    function tampilkan(id, event) {
      document.querySelectorAll('section').forEach(s => s.classList.remove('active'));
      document.getElementById(id).classList.add('active');
      document.querySelectorAll('nav button').forEach(b => b.classList.remove('active'));
      if (event && event.target) {
        event.target.classList.add('active');
      }
    }
  </script>
</body>
</html>
