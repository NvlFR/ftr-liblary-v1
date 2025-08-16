# Konteks:
Kita akan membuat file migration untuk mendefinisikan skema tabel secara konkret di dalam proyek Laravel [NAMA_PROYEK].

Sebagai acuan, kita akan menggunakan desain dari ERD yang telah dibuat atau berdasarkan spesifikasi detail di bawah ini.

**Opsional: Tempel kode ERD Mermaid di sini untuk memberikan konteks visual kepada AI.**
``[Salin dan tempel di sini kode Mermaid JS ERD Anda]``

---
### Tugas Anda:
Berperan sebagai seorang Lead Developer LIQ yang sangat ahli dengan Laravel Schema Builder.

Tugas Anda adalah menulis kode PHP yang lengkap untuk sebuah file migration Laravel yang akan membuat tabel bernama **[NAMA_TABEL]**.

##### Berikut adalah spesifikasi detail untuk kolom-kolom dan relasi tabel tersebut. Mohon ikuti dengan sangat teliti:

```[
- id: (Primary Key, bigIncrements)
- nama_kolom_1: tipe_data (misal: string, 255), constraint (misal: nullable(), unique(), default('nilai'))
- nama_kolom_2: tipe_data (misal: decimal, 8, 2), constraint (misal: unsigned())
- foreign_key_id: tipe_data (misal: foreignId), constraint (misal: constrained('nama_tabel_referensi')->onDelete('cascade'))
- timestamps: (Gunakan ->timestamps() untuk created_at dan updated_at)
]
```

---

### Catatan
Berikan kode PHP yang lengkap dan siap pakai untuk sebuah file migration.


- Pastikan untuk menyertakan namespace, use Schema, class, serta metode up() dan down() yang sudah terisi dengan benar.

-  Metode down() harus berisi Schema::dropIfExists**('[NAMA_TABEL]')**;.

- Sajikan jawaban Anda dalam satu blok kode PHP yang rapi, seolah-olah saya bisa langsung menyalin dan menyimpannya ke dalam file database/migrations/YYYY_MM_DD_HHMMSS_create_[nama_tabel]_table.php.


---
### Deskripsi:
Gunakan prompt ini untuk mengonversi desain tabel dari ERD atau deskripsi tekstual menjadi sebuah file migration Laravel yang fungsional. Prompt ini akan memandu AI untuk menulis kode PHP menggunakan Schema Builder Laravel, lengkap dengan tipe data, constraints (aturan), dan definisi foreign key.

---

### ✅ Prasyarat:
1. Persona Persona_Lead_Developer_LIQ.md sudah aktif, karena ini membutuhkan pengetahuan spesifik tentang Laravel.

2. Anda sudah memiliki desain ERD atau spesifikasi kolom yang jelas untuk tabel yang akan dibuat (hasil dari Prompt_Generate_ERD_Mermaid.md).

---


###  CONTOH PENGGUNAAN NYATA
Melanjutkan proyek "POS Toko Sahabat". Kita akan membuat tabel perantara transaction_details. Tabel ini menarik karena memiliki dua foreign key.

Langkah 1: Aktifkan Persona

Anda mengirim:
(Isi dari Persona_Lead_Developer_LIQ.md)

AI merespons:
"Saya siap berperan sebagai Lead Developer LIQ. Silakan berikan tugasnya."

Langkah 2: Berikan Tugas (Menggunakan Template Ini)

Anda mengirim (setelah mengisi template):

Konteks:
Kita akan membuat file migration untuk mendefinisikan skema tabel di dalam proyek Laravel "POS Toko Sahabat".
(Anda bisa menempelkan ERD dari prompt sebelumnya di sini jika mau)

Tugas Anda:
Berperan sebagai seorang Lead Developer LIQ yang sangat ahli dengan Laravel Schema Builder.

Tugas Anda adalah menulis kode PHP yang lengkap untuk sebuah file migration Laravel yang akan membuat tabel bernama transaction_details.

Berikut adalah spesifikasi detail untuk kolom-kolom dan relasi tabel tersebut. Mohon ikuti dengan sangat teliti:

[
- id: (Primary Key)
- transaction_id: foreignId, constrained ke tabel 'transactions', onDelete('cascade') -> jika transaksi dihapus, detailnya juga ikut terhapus.
- product_id: foreignId, constrained ke tabel 'products', onDelete('set null') -> jika produk dihapus, riwayat penjualan tetap ada, hanya produknya menjadi null.
- quantity: integer, unsigned.
- price: decimal, 10, 2 -> Harga produk PADA SAAT transaksi terjadi, bukan harga saat ini.
]
(Catatan: kita sengaja tidak menggunakan timestamps() di sini)

Format Output:
Berikan kode PHP yang lengkap untuk file migration...
(sisa prompt tetap sama)

---