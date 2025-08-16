### Deskripsi:
Gunakan prompt ini untuk memerintahkan AI membuat sebuah halaman Inertia.js yang lengkap menggunakan Vue 3 Composition API 
**``(<script setup>)``.**
Halaman ini secara spesifik bertujuan untuk menampilkan sekumpulan data (koleksi) yang diterima dari controller Laravel di dalam sebuah komponen tabel yang canggih dari Quasar Framework, yaitu QTable.

### ✅ Prasyarat:
1. Persona Persona_Lead_Developer_LIQ.md sudah aktif.

2. Endpoint backend (Controller dan Route) untuk metode index sudah selesai dibuat dan siap mengirimkan data (biasanya dengan paginasi) melalui Inertia::render().

# Konteks:
Kita akan membuat halaman frontend untuk proyek **[NAMA_PROYEK]** menggunakan Vue 3, Quasar, dan Inertia.js.

Halaman ini akan berfungsi sebagai halaman utama (indeks) untuk menampilkan daftar data **[NAMA_RESOURCE_JAMAK]** yang dikirim dari controller **[NAMA_CONTROLLER_CLASS]**@index.

Data tersebut akan kita tampilkan dalam sebuah tabel yang interaktif dan responsif menggunakan komponen QTable dari Quasar.

### Tugas Anda:
Berperan sebagai seorang Lead Developer LIQ yang sangat ahli dalam membangun antarmuka dengan Vue 3 Composition API **``(<script setup>)``** dan Quasar Framework.

Tugas Anda adalah menulis kode yang lengkap untuk sebuah Inertia Page Component dengan nama file [NAMA_FILE_VUE].

Komponen tersebut harus memiliki konfigurasi sebagai berikut:

1. Bagian Script **``(<script setup>)``**:

    - Gunakan defineProps untuk mendefinisikan prop yang diterima dari controller Laravel. Prop utama harus bernama **[NAMA_PROP_DATA]**. Asumsikan prop ini adalah objek yang dikirim oleh paginasi standar Laravel (memiliki properti .data yang berisi array item).

    - Buat sebuah computed property atau konstanta const columns yang berisi array konfigurasi kolom untuk QTable. Kolom ini harus sesuai dengan data yang ingin ditampilkan.

    ``[Sebutkan kolom-kolom yang ingin ditampilkan, nama field datanya, dan labelnya. Contoh: "Kolom 'Nama Produk' (mengambil dari field 'name'), 'Harga' (field 'price'), 'Stok' (field 'stock')".]``
   - Pastikan Anda menambahkan satu kolom di akhir dengan name: 'actions' dan label: 'Aksi' untuk menampung tombol-tombol interaksi.

2. Bagian Template **``(<template>)``**:

    - Gunakan komponen Quasar <QPage> sebagai pembungkus utama halaman.

    - Tambahkan judul halaman yang jelas **``(misalnya: <h1>Daftar [NAMA_RESOURCE_JAMAK]</h1>)``** dan sebuah tombol ``<QBtn>`` dengan icon add untuk mengarahkan ke halaman create (gunakan komponen ``<Link>`` dari Inertia untuk ini).

    - Implementasikan komponen ``<QTable>``. Konfigurasikan props utamanya:

        - :rows di-binding ke data array dari prop (contoh: **[NAMA_PROP_DATA]**.data).

        - :columns di-binding ke konstanta columns yang Anda buat di script.

        - row-key="id" **(asumsikan setiap data memiliki ID unik)**.

    - Gunakan slot #body-cell-actions di dalam ``<QTable>`` untuk mendefinisikan tampilan kolom 'Aksi'. Di dalam slot ini, render beberapa ``<QBtn>`` (misalnya, untuk Edit dan Hapus) yang juga dibungkus dengan komponen ``<Link>`` dari Inertia untuk mengarahkan ke route yang sesuai (misalnya, products.edit atau products.destroy).


### Catatan
Berikan kode yang lengkap untuk Single File Component (.vue), termasuk bagian ``<script setup>`` dan ``<template>``.
Sajikan jawaban Anda dalam satu blok kode Vue yang rapi dan terformat dengan baik, siap untuk disimpan ke dalam file resources/js/Pages/**[NAMA_FILE_VUE]**.


### 🚀 CONTOH PENGGUNAAN NYATA
Melanjutkan implementasi fitur Produk untuk proyek "POS Toko Sahabat".

Langkah 1: Aktifkan Persona
Anda sudah berada dalam sesi chat di mana AI berperan sebagai Lead Developer LIQ.

Langkah 2: Berikan Tugas (Menggunakan Template Ini)

Anda mengirim (setelah mengisi template):

Konteks:
Kita akan membuat halaman frontend untuk proyek "POS Toko Sahabat"...
Halaman ini akan berfungsi untuk menampilkan daftar data "Produk" yang dikirim dari controller ProductController@index.
Data akan ditampilkan dalam sebuah tabel menggunakan komponen QTable dari Quasar.

Tugas Anda:
Berperan sebagai seorang Lead Developer LIQ...
Tugas Anda adalah menulis kode yang lengkap untuk sebuah Inertia Page Component dengan nama file Products/Index.vue.

Komponen tersebut harus memiliki konfigurasi sebagai berikut:

1. Bagian Script (<script setup>):

Gunakan defineProps untuk prop bernama products.

Buat konstanta columns dengan spesifikasi:

[
- Kolom dengan label 'Nama Produk', mengambil dari field 'name'.
- Kolom dengan label 'SKU', mengambil dari field 'sku'.
- Kolom dengan label 'Harga', mengambil dari field 'price', dan format tampilannya sebagai mata uang Rupiah.
- Kolom dengan label 'Stok', mengambil dari field 'stock'.
]
Tambahkan kolom 'Aksi' di akhir.

2. Bagian Template (<template>):

Gunakan <QPage>...

Tambahkan judul "Manajemen Produk" dan tombol <QBtn> "Tambah Produk" yang mengarah ke route products.create.

Implementasikan <QTable>...

Di dalam slot aksi, buat <QBtn> "Edit" yang mengarah ke route products.edit dan <QBtn> "Hapus" yang mengarah ke route products.destroy dengan metode DELETE.

Format Output:
Berikan kode yang lengkap... siap untuk disimpan ke dalam file resources/js/Pages/Products/Index.vue.
(sisa prompt tetap sama)
