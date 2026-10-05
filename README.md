# MY-PORTOFOLIO-

Website portofolio pribadi Erizq Affanditya Nursin, mahasiswa Sistem Informasi Universitas Hasanuddin. Situs ini statis (HTML, CSS, JavaScript murni) tanpa framework dan tanpa proses build.

## Fitur

- Navigasi satu halaman dengan section Home, About, Skills, Projects, Education, Gallery, Certificates, dan Contact
- Mode terang dan gelap, pilihan tema disimpan di browser
- Hero interaktif dengan lanyard (kartu gantung berfoto)
- Daftar proyek dengan filter kategori dan jendela detail (modal)
- Galeri gambar tangan dan foto
- Tombol unduh CV dan tombol kembali ke atas
- Tampilan responsif untuk laptop dan HP

## Struktur Folder

```
.
├── index.html
├── css/
│   ├── style.css          # gaya utama
│   └── galeri.css         # gaya section galeri
├── js/
│   ├── lanyard.js         # animasi lanyard di hero
│   ├── script.js          # tema, navigasi, data proyek, modal
│   └── galeri.js          # data dan perilaku galeri
└── assets/
    ├── CV_Erizq_Affanditya_Nursin.pdf
    └── images/
        ├── profile.jpg, profile-cutout.webp
        ├── bg-skills.jpg, bg-education.jpg
        ├── marketplace.jpg, umkm-anging-mammiri.jpg, pameran-dapur-daeng-aso.jpg
        ├── placeholder-database.svg, placeholder-network.svg
        └── galeri/        # me-1..6.jpg dan draw-1..6.jpg
```

> **Penting:** `index.html` memanggil file memakai path relatif (`css/style.css`, `js/script.js`, `assets/images/...`). Struktur folder di atas harus dipertahankan. Jika file diletakkan rata di satu folder, CSS, JS, dan gambar tidak akan termuat.

## Menjalankan di Komputer

1. Ekstrak ZIP.
2. Buka `index.html` dengan browser (klik dua kali).

Opsional, untuk server lokal:

```bash
# di dalam folder proyek
python -m http.server 8000
# buka http://localhost:8000
```

## Deploy ke GitHub Pages

1. Buat repository baru di GitHub.
2. Unggah **isi** folder proyek (`index.html`, `css/`, `js/`, `assets/`), bukan folder pembungkusnya. Gunakan **Add file → Upload files**, lalu **seret folder-folder langsung** ke halaman agar struktur ikut terunggah. `index.html` harus berada di root repository.
3. Jangan sertakan `.DS_Store` dan `__MACOSX`.
4. Buka **Settings → Pages**. Pada **Source**, pilih **Deploy from a branch**, branch `main`, folder `/ (root)`, lalu **Save**.
5. Tunggu 1–2 menit. Situs tersedia di:
   `https://<username>.github.io/<nama-repository>/`

### Membuka di HP

Buka link GitHub Pages di atas lewat browser HP. Jika tampilan belum berubah setelah pembaruan, lakukan refresh paksa atau buka lewat tab incognito untuk menghindari cache.

### Jika CSS/JS tidak termuat

- Pastikan folder `css/`, `js/`, dan `assets/` ada di repository dan tidak diratakan.
- Pastikan huruf besar-kecil nama file sama persis. GitHub Pages membedakannya (`style.css` tidak sama dengan `Style.css`).
- Periksa tab **Network** di DevTools untuk melihat file mana yang menghasilkan 404.

## Cara Mengubah Konten

| Yang ingin diubah | Lokasi |
|---|---|
| Teks, section, link sosial media, sertifikat | `index.html` |
| Daftar proyek (nama, kategori, gambar, link) | array proyek di bagian atas `js/script.js` |
| Foto dan keterangan galeri | `js/galeri.js` dan folder `assets/images/galeri/` |
| Warna, font, tata letak | `css/style.css` dan `css/galeri.css` |
| CV | ganti `assets/CV_Erizq_Affanditya_Nursin.pdf` (pertahankan nama file, atau ubah link di `index.html`) |

### Yang masih perlu dilengkapi

- Link sertifikat di section Certificates masih berisi placeholder (`[Certificate URL]`, `[Link if available]`) di `index.html`.
- Gambar proyek Student Management Database dan Computer Network Simulation masih memakai placeholder SVG.
- Form kontak baru melakukan validasi dan menyimpan pesan di localStorage browser, jadi pesan belum terkirim ke email. Untuk mengirimkannya, sambungkan layanan seperti Formspree atau EmailJS di `js/script.js` (komentar `CONNECT BACKEND HERE`).

## Teknologi

- HTML5, CSS3, JavaScript (vanilla)
- Google Fonts: Inter, Sora, Playfair Display, Pinyon Script, Bodoni Moda (butuh koneksi internet)

## Kontak

Erizq Affanditya Nursin, Sistem Informasi, Universitas Hasanuddin.
Detail kontak dan sosial media ada di section Contact pada situs.
