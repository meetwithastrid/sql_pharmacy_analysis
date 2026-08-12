# Analisis Inventory & Risiko Stok Pada Produk Farmasi

Project ini berisi analisis data inventory obat menggunakan SQL (SQLite) di Google Colab. Dataset berisi 2.000+ data obat dari apotek di Mesir, mencakup informasi kategori, harga, stok, dan tanggal kedaluwarsa.

# Tentang Dataset
Dataset publik dari Kaggle berisi 2.042 baris data obat dengan 14 kolom, 
mencakup nama obat, kandungan aktif, kategori terapi, bentuk sediaan, harga (EGP), stok, tanggal kedaluwarsa, produsen, serta status ketersediaan dan popularitas.

# Tools
- SQLite (via Python `sqlite3`)
- Google Colab
- Pandas (untuk pembersihan data & menampilkan hasil query)

# Isi Analisis
File: `farmasi_analysis.ipynb`

| No | Query | Fokus Analisis |
|----|-------|-----------------|
| 1 | WHERE + BETWEEN | Obat yang akan kedaluwarsa dalam periode tertentu |
| 2 | WHERE + CASE WHEN | Obat populer namun kehabisan stok |
| 3 | GROUP BY + MIN/MAX | Harga termurah & termahal per kategori obat |
| 4 | LIKE | Pencarian semua obat berbentuk tablet |

# Catatan
Sebelum dianalisis, kolom tanggal kedaluwarsa (`expiry_date`) dirapikan 
terlebih dahulu karena format aslinya tidak konsisten antar baris.
