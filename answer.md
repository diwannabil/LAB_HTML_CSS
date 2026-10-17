# Jawaban Praktikum: Diwan Nabil Mubarok (10224013)

## Bagian 1: Pemanasan
1.  Selector = nav a.active:hover
    Deklarasi (Declaration) = color: red;
    Property = color
    Value = red
    Pseudo-class = :hover
    tambahan, nav dan a adalah tag/element selector, sedangkan .active adalah class selector
2.  Block = <p>, <li>, <h2>
    Inline = <span>, <a>, <strong>
3.  A dan B karena <p>A</p> dan <p>B</p>berada di dalam <div class="box">
4.  merah karena selector #title memiliki specificity (tingkat kekhususan) tertinggi dibandingkan dua selector lainnya
5.  Tag <p> ditutup sebelum tag <strong>, padahal <strong> dibuka di dalam <p>. Tag harus ditutup dengan urutan terbalik dari pembukaannya.
harusnya <p>Hello <strong>world</strong></p>

## Bagian 3: Prediksi Selector Golf
P1.a = Hijau, b = Oranye, c = Biru prediksi tersebut di ambil berdasarkan aturan kecocokan selector dan specificity. 
P2. 1. #tech p: 1 ID + 1 elemen.
    2. .club p: 1 class + 1 elemen.
    3. main section p: 3 elemen.
    4. p: 1 elemen.
Setelah diuji (hasil sebenarnya):
Weekly hack nights. = hijau
Bring your own laptop. = oranye
© 2026 Student Affairs = biru
## Bagian 4: Box model
Q1 (content-box):
Diketahui:
width: 300px
padding: 16px di setiap sisi
border: 1px di setiap sisi
margin: 24px di setiap sisi
Dengan box-sizing: content-box, properti width hanya menghitung lebar content. Padding dan border ditambahkan di luar content.
Perhitungan lebar kartu dari tepi border ke tepi border:
300px + 16px + 16px + 1px + 1px = 334px
Jadi, lebar kartu yang terlihat adalah 334px.
Margin tidak dihitung sebagai bagian dari lebar kartu. Jika termasuk margin kiri dan kanan, total ruang horizontal adalah 334px + 24px + 24px = 382px.

Q2 (border-box):
Jika ditambahkan box-sizing: border-box, nilai width: 300px sudah mencakup content, padding, dan border.
Jadi, lebar kartu dari tepi border ke tepi border menjadi 300px. Area content mengecil agar padding dan border tetap termasuk dalam lebar tersebut. Margin tetap berada di luar kartu.

Pengecekan DevTools:
Content: 724 × 31.188 px
Padding: 0 px
Border: 0 px
Margin: kiri dan kanan 19.920 px, atas dan bawah 0 px

## Bagian 5: Tabel debug
## Bagian 5 — Debugging

| No. | Bug yang ditemukan | Perbaikan | Cara menemukannya |
|---:|---|---|---|
| 1 | Properti CSS `colour` salah | Diubah menjadi `color` | Membaca kode dan memeriksa CSS di DevTools |
| 2 | Kurang titik koma setelah `background: #dbe7f3` | Ditambahkan `;` | Membaca kode dan memeriksa Styles di DevTools |
| 3 | Selector `.Card` tidak cocok dengan class `card` | Diubah menjadi `.card` | Membandingkan selector CSS dengan class HTML |
| 4 | Nilai `font-size: 18 px` tidak valid | Diubah menjadi `18px` | DevTools menampilkan deklarasi CSS yang tidak valid |
| 5 | Nilai `text-align: centre` tidak valid | Diubah menjadi `center` | Membaca kode dan memeriksa Styles di DevTools |
| 6 | Tag `<h1>` ditutup dengan `</h2>` | Diubah menjadi `</h1>` | Validator HTML |
| 7 | Atribut `href` pada link About tidak memiliki tanda kutip penutup | Diubah menjadi `href="about.html"` | Validator HTML dan membaca kode |
| 8 | Selector `#news-list` tidak cocok dengan ID `newsList` | Selector diubah menjadi `#newsList` | Membandingkan selector CSS dengan ID HTML |
| 9 | Gambar tidak memiliki atribut `alt` | Ditambahkan `alt="Campus news banner"` | Validator HTML dan pemeriksaan aksesibilitas |

## Bagian 6: Tabel Code Review
| # | Baris | Masalah | Mengapa penting | Perbaikan saya |
|---|-------|---------|-----------------|----------------|
| 1 | Awal dokumen | Tidak ada `<!DOCTYPE html>`. | Browser bisa menggunakan mode kompatibilitas yang tidak diharapkan. | Menambahkan `<!DOCTYPE html>`. |
| 2 | Awal dokumen | Tag `<html>` tidak memiliki atribut bahasa. | Teknologi bantu kesulitan menentukan bahasa utama halaman. | Menggunakan `<html lang="id">`. |
| 3 | Bagian `<head>` | Tidak ada meta charset dan viewport. | Encoding karakter dan tampilan pada perangkat seluler tidak dinyatakan secara eksplisit. | Menambahkan meta charset UTF-8 dan viewport. |
| 4 | Header | Menggunakan `<div>` sebagai header dan judul. | Struktur halaman kurang semantik dan judul tidak dikenali sebagai heading. | Menggunakan `<header>` dan `<h1>`. |
| 5 | Navigasi | Menggunakan `<div>` untuk navigasi. | Bagian navigasi tidak ditandai secara semantik. | Menggunakan `<nav>` dan daftar link. |
| 6 | CSS `.header` | Lebar tetap `1200px`. | Bisa menyebabkan halaman melebar melebihi layar kecil. | Menggunakan lebar responsif dan `max-width`. |
| 7 | CSS `.nav a` | Menggunakan `!important`. | Membuat aturan warna link lebih sulit diubah atau ditimpa. | Menghapus `!important`. |
| 8 | CSS `.sidebar` | Selector `.sidebar` tidak digunakan. | Kode CSS yang tidak terpakai membuat stylesheet kurang bersih. | Menghapus aturan yang tidak diperlukan. |
| 9 | Bagian About Us dan Contact Us | Judul dibuat dengan `<div>` dan inline CSS. | Struktur heading tidak jelas dan gaya sulit dipelihara. | Menggunakan `<h2>` dan aturan CSS terpisah. |
| 10 | Gambar | Elemen `<img>` tidak memiliki atribut `alt`. | Pengguna pembaca layar tidak mendapatkan deskripsi gambar. | Menambahkan atribut `alt` yang sesuai. |
| 11 | Formulir | Input tidak memiliki label dan input email memakai `type="text"`. | Formulir kurang aksesibel dan tidak memiliki validasi format email bawaan. | Menambahkan `<label>` dan menggunakan `type="email"`. |
| 12 | Bagian konten | Jarak diatur dengan `<br>` berulang dan tombol hanya menampilkan `alert()`. | Tata letak sulit dipelihara dan tombol tidak benar-benar mengirim data. | Mengatur jarak melalui CSS dan memakai formulir dengan backend jika pengiriman sungguhan diperlukan. |

Refleksi:
1. Masalah mana yang paling sulit disadari hanya dengan melihat halamannya di browser? Mengapa?
Menurut saya, masalah yang paling sulit disadari adalah tidak adanya label yang terhubung dengan input formulir dan penggunaan `!important` pada CSS. Halaman masih dapat terlihat normal, tetapi masalah tersebut memengaruhi aksesibilitas dan pemeliharaan kode.

2. Halaman aslinya berfungsi. Mengapa masalah-masalah ini tetap penting?
Halaman yang terlihat baik belum tentu memiliki struktur HTML yang benar, mudah diakses, dan responsif di berbagai perangkat. Kode yang baik memudahkan pengembangan selanjutnya dan mengurangi risiko masalah ketika halaman diperbarui.

3. Satu kebiasaan apa yang akan kamu lakukan untuk memeriksa HTML/CSS sebelum dikumpulkan?
Saya akan memeriksa HTML menggunakan W3C Validator dan menguji tampilan halaman dengan DevTools. Saya juga akan memeriksa heading, label formulir, atribut gambar, responsivitas, serta aturan CSS yang tidak valid atau tidak terpakai.

## Bagian 7: Exit ticket
1.Sebuah aturan CSS terdiri dari selector dan declaration block. Selector digunakan untuk memilih elemen HTML yang akan diberi gaya, sedangkan declaration block berisi satu atau lebih deklarasi. Setiap deklarasi terdiri dari property dan value, misalnya color: red;.

2.Saya masih perlu berlatih memahami specificity ketika beberapa selector CSS menargetkan elemen yang sama, terutama saat melibatkan ID, class, dan selector elemen.

3.Saya sekarang bisa membuat selector CSS sederhana, mengatur warna dan ukuran teks, serta menghubungkan file CSS eksternal ke HTML tanpa perlu mencari contoh terlebih dahulu.