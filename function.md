# 🎥 Redirect ke YouTube dengan Tekan Tombol

Skrip sederhana yang akan mengarahkan pengguna ke video YouTube jika mereka menekan tombol terus-menerus selama beberapa detik.

## 🚀 Fitur
- ⏳ Mengarahkan ke video setelah tombol ditekan selama 3 detik
- 🖥️ Mudah digunakan di halaman web
- 🎯 Dapat disesuaikan dengan URL video YouTube pilihan Anda

## 📦 Cara Menggunakan

1. Tambahkan skrip ini ke dalam proyek HTML atau JavaScript Anda:
   ```javascript
   let isHolding = false;
   let holdTimeout;

   // Ganti dengan URL video YouTube yang diinginkan
   const youtubeURL = "https://www.youtube.com/watch?v=VIDEO_ID";

   document.addEventListener("keydown", (event) => {
       if (!isHolding) {
           isHolding = true;
           holdTimeout = setTimeout(() => {
               window.location.href = youtubeURL;
           }, 3000); // Tekan terus selama 3 detik
       }
   });

   document.addEventListener("keyup", () => {
       isHolding = false;
       clearTimeout(holdTimeout);
   });
   ```

2. Ubah `VIDEO_ID` dengan ID video YouTube yang ingin dituju.

3. Masukkan skrip ini ke dalam proyek web Anda.

## 🛠 Teknologi yang Digunakan
- JavaScript murni (tanpa library tambahan)
- Browser modern

## 📄 Lisensi
Proyek ini dilisensikan di bawah [MIT License](https://opensource.org/licenses/MIT).

## 🌟 Kontribusi
Jika Anda ingin meningkatkan skrip ini, silakan buat pull request atau ajukan issue!

---

💡 **Jangan lupa untuk memberikan bintang ⭐ pada repositori ini jika menurut Anda bermanfaat!**

