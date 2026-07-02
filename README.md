# SILLAGE — Maison de Parfum

Landing page e-commerce untuk brand parfum fiktif **SILLAGE**. Proyek ini awalnya berupa satu file HTML tunggal, kemudian dipisah menjadi struktur HTML / CSS / JavaScript standar agar lebih mudah dibaca, dikelola, dan dikembangkan.

## 📁 Struktur File

```
.
├── index.html   # Struktur & konten halaman
├── style.css    # Seluruh styling (tema, layout, animasi, responsif)
├── script.js    # Logika interaktif (produk, keranjang, checkout, dll)
└── README.md    # Dokumen ini
```

## ✨ Fitur

- **Hero section** dengan animasi asap (particle system via `<canvas>`)
- **Katalog produk** dengan pencarian, filter kategori (chip), dan filter harga
- **Kartu produk** dengan ilustrasi botol parfum berbasis SVG dinamis
- **Keranjang belanja** (cart drawer): tambah, ubah jumlah, hapus item
- **Checkout** lengkap dengan validasi form dan ringkasan pesanan (subtotal, pajak, ongkir)
- **Metode pembayaran** (kartu kredit / lainnya) dengan format otomatis nomor kartu & tanggal kedaluwarsa
- **Modal sukses** setelah order berhasil dibuat
- **Scroll reveal** animasi saat elemen masuk viewport (`IntersectionObserver`)
- **Navbar responsif** dengan hamburger menu untuk mobile
- **Google Analytics (dummy)** — event tracking untuk `add_to_cart`, `begin_checkout`, `purchase`, `product_view`, `search`, dll (menggunakan Measurement ID placeholder `G-XXXXXXXXXX`, belum tersambung ke akun GA sungguhan)

## 🛠️ Teknologi

- **HTML5** — markup semantik
- **CSS3** — custom properties (variabel warna/tema), flexbox, animasi, `backdrop-filter`
- **Vanilla JavaScript** — tanpa framework/library eksternal, murni DOM API
- **Google Fonts** — `Cormorant Garamond` (judul, serif) & `DM Sans` (body, sans-serif)

## 🎨 Tema Warna

| Variabel | Kode Warna | Kegunaan |
|---|---|---|
| `--obsidian` | `#0D0D0D` | Latar utama |
| `--champagne` | `#E8D5B0` | Aksen utama, judul |
| `--rose` | `#C9917A` | Aksen sekunder, hover |
| `--ivory` | `#F5F0E8` | Teks utama |
| `--sage` | `#7A8C7E` | Aksen tersier |
| `--card-bg` | `#141414` | Latar kartu/komponen |

Semua variabel didefinisikan di `:root` pada `style.css` sehingga tema bisa diubah cukup dari satu tempat.

## 🚀 Cara Menjalankan

Karena `index.html` memuat `style.css` dan `script.js` secara eksternal, buka melalui server lokal (bukan langsung double-click file) agar tidak terkendala kebijakan CORS/file:// pada beberapa browser:

```bash
# Dengan Python
python3 -m http.server 8000

# lalu buka di browser:
http://localhost:8000
```

Atau gunakan ekstensi **Live Server** di VS Code.

## 📝 Catatan

- Data produk (`products`) saat ini berupa array statis di dalam `script.js` — belum terhubung ke backend/database.
- Proses checkout dan pembayaran bersifat **simulasi**; tidak ada transaksi nyata yang diproses.
- Tracking Google Analytics menggunakan ID placeholder dan hanya untuk ilustrasi struktur event, belum aktif mengirim data ke akun GA manapun.

## 📄 Lisensi

Proyek demo untuk keperluan pembelajaran/portofolio.
