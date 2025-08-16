### Deskripsi:
Gunakan prompt ini untuk memerintahkan AI membuat Database Seeder di Laravel. Seeder berfungsi untuk mengisi tabel database dengan data palsu (dummy) secara terprogram. Prompt ini akan memandu AI untuk menggunakan best practice dengan membuat Model Factory terlebih dahulu, yang kemudian dipanggil oleh Seeder. Ini sangat penting untuk development dan testing.

---
### ✅ Prasyarat:
1. Persona Persona_Lead_Developer_LIQ.md sudah aktif.

2. File Migration dan Model Eloquent untuk tabel yang akan diisi sudah ada (atau setidaknya sudah terdefinisi).

---

# Konteks:
Kita perlu mengisi database proyek **[NAMA_PROYEK]** dengan data dummy agar bisa melakukan pengembangan dan pengujian dengan data yang realistis.

Kita akan membuat seeder untuk Model **[NAMA_MODEL]** yang terhubung dengan tabel **[NAMA_TABEL]**.

### Tugas Anda:
Berperan sebagai seorang Lead Developer LIQ yang ahli dalam database seeding dan Model Factories di Laravel.

##### Tugas Anda adalah menulis kode PHP yang lengkap untuk dua file utama (Factory dan Seeder) untuk mengisi data dummy:

1. Buat sebuah Model Factory:
    - Buat sebuah model factory yang terasosiasi dengan model [NAMA_MODEL].

    - Di dalam metode definition(), gunakan library Faker bawaan Laravel untuk menghasilkan data yang terlihat nyata untuk setiap atribut/kolom yang bisa diisi (fillable).

    - Berikut adalah panduan untuk menghasilkan data di setiap kolom:
    ```
    [
    - nama_kolom_1: Gunakan Faker untuk [jenis_data_faker] (contoh: fake()->name(), fake()->company(), fake()->unique()->safeEmail())
    - nama_kolom_2: Gunakan Faker untuk [jenis_data_faker] (contoh: fake()->address(), fake()->randomNumber(2), fake()->randomFloat(2, 10000, 50000))
    - foreign_key_id: Ambil ID secara acak dari tabel relasi. (contoh:          User::inRandomOrder()->first()->id)
    ]
    ```

2. Buat sebuah Database Seeder:

    - Buat sebuah database seeder class dengan nama **[NAMA_SEEDER_CLASS]** (contoh: ProductSeeder).

    - Di dalam metode run(), panggil factory yang baru saja kita definisikan untuk membuat **[JUMLAH_DATA]** record data baru di database.

    - Terakhir, berikan instruksi untuk memanggil seeder class ini dari file database/seeders/DatabaseSeeder.php

### Catatan
Berikan kode PHP yang lengkap untuk setiap bagian secara terpisah dan berurutan:

- Kode untuk file Factory (misal: database/factories/ProductFactory.php).

- Kode untuk file Seeder Class (misal: database/seeders/ProductSeeder.php).

- Baris kode yang perlu ditambahkan ke dalam metode run() di database/seeders/DatabaseSeeder.php.

Sajikan semuanya dalam blok kode PHP yang rapi dengan nama file sebagai judulnya.


### 🚀 CONTOH PENGGUNAAN NYATA
Melanjutkan proyek "POS Toko Sahabat", kita akan membuat data dummy untuk produk-produk di toko kelontong.

Langkah 1: Aktifkan Persona

Anda mengirim:
(Isi dari Persona_Lead_Developer_LIQ.md)

AI merespons:
"Saya siap berperan sebagai Lead Developer LIQ. Silakan berikan tugasnya."

Langkah 2: Berikan Tugas (Menggunakan Template Ini)

Anda mengirim (setelah mengisi template):

Konteks:
Kita perlu mengisi database proyek "POS Toko Sahabat" dengan data dummy agar kita bisa melakukan pengembangan dan pengujian frontend tanpa database yang kosong.

Kita akan membuat seeder untuk Model Product yang berkorespondensi dengan tabel products.

Tugas Anda:
Berperan sebagai seorang Lead Developer LIQ yang ahli dalam database seeding dan Model Factories di Laravel.

... (bagian tugas lainnya tetap sama) ...

1. Buat sebuah Model Factory:

...

Berikut adalah panduan untuk menghasilkan data di setiap kolom:

[
- name: Gunakan nama produk toko kelontong yang umum di Indonesia (contoh: "Indomie Goreng Special", "Teh Botol Sosro Kotak", "Silverqueen 65g"). Jika sulit, gunakan fake()->words(3, true).
- sku: Gunakan fake()->unique()->ean8() untuk menghasilkan kode bar yang unik.
- price: Gunakan fake()->numberBetween(2500, 75000). Bulatkan ke ratusan terdekat.
- stock: Gunakan fake()->numberBetween(10, 200).
]
2. Buat sebuah Database Seeder:

Nama class Seeder: ProductSeeder

Gunakan factory untuk membuat 150 record produk.

...

Format Output:
Berikan kode PHP yang lengkap untuk setiap bagian secara terpisah...
(sisa prompt tetap sama)