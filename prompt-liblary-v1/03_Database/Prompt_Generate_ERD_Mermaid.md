# Konteks:
Kita akan merancang struktur dan relasi database untuk proyek **[NAMA_PROYEK]**.

Berdasarkan kebutuhan fungsional yang telah kita definisikan, sistem ini perlu menyimpan dan mengelola data untuk entitas-entitas berikut:

```[Tuliskan daftar entitas utama (yang akan menjadi tabel) dan deskripsi singkat data apa saja yang perlu disimpan untuk masing-masing. Gunakan bahasa sederhana.]

Contoh:
- Pengguna: Perlu menyimpan nama, email, password yang di-hash, dan peran (role).
- Produk: Perlu menyimpan nama produk, kode SKU, harga, dan jumlah stok.
- Transaksi: Perlu mencatat waktu transaksi, total pembayaran, dan siapa kasir yang melayani.
- Detail Transaksi: Ini adalah tabel perantara untuk mencatat produk apa saja dan berapa banyak yang dibeli dalam satu transaksi.
```

---
### Tugas Anda:
Berperanlah sebagai seorang Database **Administrator (DBA)** atau **Data Modeler** yang berpengalaman.

Tugas Anda adalah membuat sebuah Entity-Relationship Diagram **(ERD)** yang jelas dan akurat menggunakan **sintaks Mermaid JS**.

##### ERD yang Anda buat harus mencakup:

1. Semua Entitas sebagai Tabel: Pastikan semua entitas yang saya sebutkan di atas direpresentasikan sebagai tabel dalam diagram.

---
2. Atribut **(Kolom)** dan Tipe Data: Untuk setiap tabel, daftarkan atribut-atribut utamanya beserta tipe datanya. Tandai dengan jelas mana yang merupakan Primary Key (PK) dan mana yang Foreign Key **(FK)**.

---
3. Relasi dan Kardinalitas: Gambarkan hubungan antar tabel dengan menggunakan notasi kardinalitas Mermaid yang benar. Berikan label pada relasi untuk menjelaskan hubungannya.

    - Gunakan **||--o{ untuk relasi one-to-many**.

    - Gunakan **||--|| untuk relasi one-to-one**.

    - Gunakan }**o--o{ untuk relasi many-to-many (biasanya melalui tabel perantara)**.

---
Pastikan Anda mempertimbangkan relasi logis seperti:
``[Deskripsikan hubungan antar entitas Anda di sini. Contoh: "Satu Pengguna bisa memiliki BANYAK Transaksi. Satu Transaksi bisa terdiri dari BANYAK Produk (melalui tabel Detail Transaksi)."]``

---
### Catatan 
Berikan hanya blok kode Mermaid JS yang lengkap dan siap pakai, yang diawali dengan erDiagram. Jangan tambahkan penjelasan atau teks lain di luar blok kode, agar saya bisa langsung menyalin dan menempelkannya ke dalam renderer.


---
### Deskripsi:
Gunakan prompt ini untuk memerintahkan AI mengubah deskripsi kebutuhan data sebuah proyek menjadi Entity-Relationship Diagram (ERD) visual. Prompt ini secara spesifik meminta output dalam format kode Mermaid JS, sebuah sintaks berbasis teks yang dapat secara otomatis di-render menjadi diagram. Ini sangat berguna untuk dokumentasi teknis (SDD) dan untuk memvisualisasikan struktur database sebelum menulis satu baris pun kode migration.

---
### ✅ Prasyarat:
1. Persona Persona_System_Architect.md atau Persona_Lead_Developer_[STACK].md sudah aktif.

2. Anda sudah memiliki pemahaman tentang entitas-entitas utama dan data apa yang perlu disimpan, yang biasanya didapat dari dokumen "Kebutuhan Fungsional" (Modul 01).

---

### 🚀 CONTOH PENGGUNAAN NYATA
Menggunakan proyek "POS Toko Sahabat" sebagai contoh.

Langkah 1: Aktifkan Persona

Anda mengirim:
(Isi dari Persona_System_Architect.md)

AI merespons:
"Saya siap berperan sebagai System Architect senior. Silakan berikan konteks dan tugas spesifiknya."

Langkah 2: Berikan Tugas (Menggunakan Template Ini)

Anda mengirim (setelah mengisi template):

Konteks:
Kita akan merancang struktur dan relasi database untuk proyek "POS Toko Sahabat".

Berdasarkan kebutuhan fungsional yang telah kita definisikan, sistem ini perlu menyimpan dan mengelola data untuk entitas-entitas berikut:

- Users: Untuk menyimpan data kasir/admin. Perlu data nama, email, password, dan role (admin/kasir).
- Products: Untuk menyimpan data produk. Perlu data nama, SKU, harga jual, jumlah stok.
- Transactions: Untuk mencatat setiap penjualan. Perlu data waktu transaksi, total jumlah bayar, metode pembayaran, dan ID kasir yang melakukan transaksi.
- Transaction_Details: Tabel perantara untuk mencatat produk apa saja yang ada di dalam satu transaksi, termasuk kuantitas dan harga produk saat itu.
Tugas Anda:
Berperanlah sebagai seorang Database Administrator (DBA) atau Data Modeler yang berpengalaman.

Tugas Anda adalah membuat sebuah Entity-Relationship Diagram (ERD) yang jelas dan akurat menggunakan sintaks Mermaid JS.

... (bagian tugas lainnya tetap sama) ...

Pastikan Anda mempertimbangkan relasi logis seperti:
"Satu User (kasir) dapat melakukan BANYAK Transactions. Satu Transaction memiliki BANYAK Transaction_Details. Satu Product dapat muncul di BANYAK Transaction_Details."

Format Output:
Berikan hanya blok kode Mermaid JS yang lengkap dan siap pakai...
(sisa prompt tetap sama)