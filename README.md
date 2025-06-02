<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
</head>
<body>

  <h1>💻 Materi Dasar Pemrograman dengan JavaScript</h1>

  <h2>1. Apa itu JavaScript?</h2>
  <p><strong>JavaScript</strong> adalah bahasa pemrograman yang digunakan untuk menambahkan interaktivitas pada halaman web.</p>
  <p>✅ Digunakan untuk:</p>
  <ul>
    <li>Menangani event (klik, hover, input)</li>
    <li>Memanipulasi elemen HTML dan CSS</li>
    <li>Mengambil data dari server (AJAX/Fetch)</li>
    <li>Membuat aplikasi web modern</li>
  </ul>

  <h2>2. Cara Menyisipkan JavaScript</h2>
  <pre><code>&lt;!-- Inline --&gt;
&lt;button onclick="alert('Halo!')"&gt;Klik Saya&lt;/button&gt;

&lt;!-- Internal --&gt;
&lt;script&gt;
  alert("Halo dari script internal!");
&lt;/script&gt;

&lt;!-- External --&gt;
&lt;script src="script.js"&gt;&lt;/script&gt;
</code></pre>

  <h2>3. Variabel dan Tipe Data</h2>
  <pre><code>let nama = "Ari";      // bisa diubah
const umur = 21;       // tidak bisa diubah
var kota = "Lampung";  // versi lama, hindari</code></pre>
  <p><strong>Tipe data umum:</strong></p>
  <ul>
    <li>String: "Halo"</li>
    <li>Number: 10, 3.14</li>
    <li>Boolean: true, false</li>
    <li>Array: ["apel", "jeruk"]</li>
    <li>Object: { nama: "Ari", umur: 21 }</li>
  </ul>

  <h2>4. Operator Dasar</h2>
  <table>
    <tr><th>Jenis</th><th>Contoh</th></tr>
    <tr><td>Aritmatika</td><td>+, -, *, /, %</td></tr>
    <tr><td>Perbandingan</td><td>==, ===, !=, &gt;, &lt;</td></tr>
    <tr><td>Logika</td><td>&amp;&amp;, ||, !</td></tr>
  </table>

  <h2>5. Struktur Kontrol</h2>
  <h3>If-Else</h3>
  <pre><code>let umur = 20;
if (umur &gt;= 18) {
  console.log("Dewasa");
} else {
  console.log("Belum dewasa");
}</code></pre>

  <h3>Switch</h3>
  <pre><code>let hari = "Senin";
switch(hari) {
  case "Senin":
    console.log("Hari kerja");
    break;
  case "Minggu":
    console.log("Hari libur");
    break;
}</code></pre>

  <h3>Looping</h3>
  <pre><code>for(let i = 1; i &lt;= 5; i++) {
  console.log("Perulangan ke-" + i);
}

let i = 0;
while(i &lt; 3) {
  console.log(i);
  i++;
}</code></pre>

  <h2>6. Fungsi (Function)</h2>
  <pre><code>function sapa(nama) {
  return "Halo, " + nama + "!";
}

console.log(sapa("Ari"));</code></pre>

  <h2>7. Manipulasi DOM</h2>
  <pre><code>&lt;p id="teks"&gt;Halo Dunia&lt;/p&gt;
&lt;button onclick="ubahTeks()"&gt;Ubah&lt;/button&gt;

&lt;script&gt;
  function ubahTeks() {
    document.getElementById("teks").innerHTML = "Teks telah diubah!";
  }
&lt;/script&gt;
</code></pre>

  <h2>8. Event Handling</h2>
  <pre><code>&lt;button onclick="salam()"&gt;Klik aku!&lt;/button&gt;

&lt;script&gt;
  function salam() {
    alert("Halo dunia!");
  }
&lt;/script&gt;
</code></pre>

  <h2>9. Array dan Object</h2>
  <pre><code>let buah = ["apel", "mangga", "jeruk"];
console.log(buah[1]); // mangga

let orang = {
  nama: "Ari",
  umur: 21
};
console.log(orang.nama); // Ari
</code></pre>

  <h2>10. Bonus: Interaktif Form</h2>
  <pre><code>&lt;input type="text" id="nama" placeholder="Masukkan nama" /&gt;
&lt;button onclick="tampilkanNama()"&gt;Tampilkan&lt;/button&gt;
&lt;p id="hasil"&gt;&lt;/p&gt;

&lt;script&gt;
  function tampilkanNama() {
    let nama = document.getElementById("nama").value;
    document.getElementById("hasil").innerText = "Halo, " + nama;
  }
&lt;/script&gt;
</code></pre>

  <h2>✅ Tips Belajar JavaScript</h2>
  <ul>
    <li>Gunakan browser console (tekan <code>F12</code> → tab Console)</li>
    <li>Latihan di situs seperti:
      <ul>
        <li><a href="https://jsfiddle.net" target="_blank">JSFiddle</a></li>
        <li><a href="https://codepen.io" target="_blank">CodePen</a></li>
        <li><a href="https://replit.com" target="_blank">Replit</a></li>
      </ul>
    </li>
    <li>Setelah menguasai dasar, lanjut ke DOM, Fetch API, dan Framework (React, Vue, dsb)</li>
  </ul>

  <h2>📦 Contoh Project Sederhana: Kalkulator Tambah</h2>

  <h3>index.html</h3>
  <pre><code>&lt;!DOCTYPE html&gt;
&lt;html lang="id"&gt;
&lt;head&gt;
  &lt;meta charset="UTF-8"&gt;
  &lt;title&gt;Kalkulator Tambah&lt;/title&gt;
&lt;/head&gt;
&lt;body&gt;
  &lt;h1&gt;Kalkulator Tambah&lt;/h1&gt;
  &lt;input type="number" id="angka1" placeholder="Angka pertama" /&gt;
  &lt;input type="number" id="angka2" placeholder="Angka kedua" /&gt;
  &lt;button onclick="jumlahkan()"&gt;Jumlahkan&lt;/button&gt;
  &lt;p&gt;Hasil: &lt;span id="hasil"&gt;&lt;/span&gt;&lt;/p&gt;

  &lt;script src="script.js"&gt;&lt;/script&gt;
&lt;/body&gt;
&lt;/html&gt;
</code></pre>

  <h3>script.js</h3>
  <pre><code>function jumlahkan() {
  let a = parseFloat(document.getElementById("angka1").value);
  let b = parseFloat(document.getElementById("angka2").value);
  let hasil = a + b;
  document.getElementById("hasil").innerText = hasil;
}</code></pre>

</body>
</html>
