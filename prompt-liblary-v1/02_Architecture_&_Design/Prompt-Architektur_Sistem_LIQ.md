# Konteks:
Kita akan merancang arsitektur teknis yang detail untuk proyek **[NAMA_PROYEK]**. Proyek ini telah diputuskan akan dibangun menggunakan tumpukan teknologi **LIQ (Laravel, Inertia.js, Quasar)**.

Sebagai referensi utama, berikut adalah ringkasan dari Dokumen Visi & Ruang Lingkup serta Kebutuhan Fungsional yang telah kita definisikan:

``[Salin dan tempel di sini ringkasan dari dokumen Visi & Kebutuhan Fungsional Anda. Fokus pada skala proyek, pengguna, dan fitur-fitur utama yang paling kompleks.]``


### Tugas Anda:
Sebagai seorang **[NAMA_PERSONA_PILIHAN]**, tugas Anda adalah membuat "Dokumen Desain Arsitektur Sistem" yang detail, praktis, dan spesifik untuk stack LIQ.

---
###### Dokumen yang Anda hasilkan harus mencakup poin-poin berikut:

1. Pola Arsitektur: **Modular Monolith**

    - Jelaskan secara singkat mengapa pola **Monolithic** **(atau lebih spesifik, Modular Monolithic)** sangat cocok untuk aplikasi berbasis Laravel dan Inertia. Tekankan pada kemudahan pengembangan, deployment yang simpel, dan bagaimana Laravel secara alami mendukung pendekatan ini.

---
2. Peran Detail Setiap **Komponen LIQ**:

    - Laravel **(Backend Core)**: Deskripsikan secara rinci bagaimana Laravel akan digunakan untuk:

        - **Routing**: Penggunaan routes/web.php untuk menangani semua permintaan halaman.

        - **Controllers**: Sebagai orkestrator yang berisi logika bisnis, memvalidasi input (menggunakan Form Request Validation), dan menyiapkan data untuk frontend.

        - **Models (Eloquent)**: Sebagai lapisan abstraksi untuk berinteraksi dengan database, lengkap dengan relasi antar model.

        - **Database Migrations**: Untuk manajemen skema database yang terversi.

    - **Inertia.js (The Glue)**: Jelaskan peran krusial Inertia:

        - Bagaimana fungsi **Inertia::render()** di dalam Controller akan menjadi jembatan utama, mengirimkan data **(props)** dari backend ke komponen halaman Vue tanpa perlu membangun API terpisah.

        - Bagaimana form **helper** dari Inertia akan menyederhanakan proses pengiriman form dari frontend.

    - Quasar **(Frontend UI Framework)**: Jelaskan bagaimana Quasar akan diintegrasikan sebagai plugin Vue untuk:

        - Menyediakan UI Components siap pakai **(sebutkan contoh relevan seperti QLayout, QDrawer, QTable, QForm, QInput, QBtn)**.

        - Mengatur layouting utama aplikasi **(misalnya, layout dengan sidebar dan header).**

---
3. Rekomendasi **Struktur Folder Frontend**:

    - Berikan rekomendasi struktur folder yang baik di dalam direktori resources/js/ untuk mengorganisir kode frontend. Contoh:

        ##### - .../js/Pages/ (Untuk komponen halaman Inertia, misal: Products/Index.vue)

        ##### - .../js/Components/ (Untuk komponen Vue/Quasar yang bisa dipakai ulang, misal: DeleteConfirmDialog.vue)

        ##### - .../js/Layouts/ (Untuk komponen layout utama, misal: MainLayout.vue)

        ##### - .../js/Composables/ (Untuk logika reaktif yang bisa dipakai ulang dengan Vue 3 Composition API).

---

4. Diagram **Arsitektur Alur Data**:

    - Buatkan diagram alur data sederhana dalam format kode Mermaid JS **``(dengan tipe graph LR; atau sequenceDiagram).``** Diagram harus secara visual menggambarkan bagaimana sebuah permintaan dari pengguna di-handle, contohnya untuk menampilkan halaman daftar produk: **``Pengguna -> Klik Link -> Browser (GET Request) -> Laravel Route -> ProductController@index -> Query DB via Eloquent -> Inertia::render('Products/Index', data) -> Browser merender komponen Vue Page dengan Quasar Components.``**

    ---

5. Pertimbangan Awal **(Initial Considerations)**:

    - Berikan 1-2 poin singkat dan praktis mengenai:

        - **Keamanan**: Contoh: "Semua rute yang memerlukan login akan dilindungi oleh middleware auth bawaan Laravel."

        - **Performa**: Contoh: "Gunakan eager loading (metode with()) di Eloquent untuk menghindari masalah N+1 query saat mengambil data relasional."

---
### Catatan
Sajikan dalam format Markdown yang terstruktur, profesional, dan mudah diikuti. Gunakan judul, sub-judul, dan blok kode untuk memisahkan setiap bagian dengan jelas.

### Deskripsi:
Gunakan prompt ini untuk memerintahkan AI menghasilkan dokumen desain arsitektur teknis yang spesifik untuk proyek yang menggunakan tumpukan teknologi LIQ (Laravel, Inertia.js, Quasar). Prompt ini akan memandu AI untuk menjelaskan bagaimana setiap komponen teknologi akan bekerja sama, bagaimana struktur proyek akan diatur, dan bagaimana alur data akan berjalan.

---
### ✅ Prasyarat:
Persona Persona_System_Architect.md atau (lebih direkomendasikan) Persona_Lead_Developer_LIQ.md sudah aktif. Persona LIQ lebih disarankan karena memiliki pemahaman yang lebih spesifik.

Anda sudah memiliki dokumen dari Modul 01 ("Visi & Ruang Lingkup" dan "Kebutuhan Fungsional").

---

### 🚀 CONTOH PENGGUNAAN NYATA
Melanjutkan proyek "POS Toko Sahabat".

Langkah 1: Aktifkan Persona (Dari Library 00_...)

Anda mengirim:
(Isi dari Persona_Lead_Developer_LIQ.md)

AI merespons:
"Saya siap berperan sebagai Lead Developer LIQ. Silakan berikan tugasnya."

Langkah 2: Berikan Tugas (Menggunakan Template Ini)

Anda mengirim (setelah mengisi template):

Konteks:
Kita akan merancang arsitektur teknis yang detail untuk proyek "POS Toko Sahabat". Proyek ini telah diputuskan akan dibangun menggunakan tumpukan teknologi LIQ (Laravel, Inertia.js, Quasar).

Sebagai referensi utama, berikut adalah ringkasan dari Dokumen Visi & Ruang Lingkup serta Kebutuhan Fungsional yang telah kita definisikan:

'POS Toko Sahabat' adalah aplikasi kasir untuk toko kelontong. Skala proyek ini untuk satu toko, dengan kemungkinan ekspansi di masa depan. Pengguna adalah kasir dan pemilik toko. Fitur utama meliputi: Manajemen Produk (CRUD, stok, SKU), Halaman Kasir dengan pencarian produk cepat dan dukungan barcode, Proses Transaksi Tunai, dan Laporan Penjualan Harian.
Tugas Anda:
Sebagai seorang "Lead Developer LIQ", tugas Anda adalah membuat "Dokumen Desain Arsitektur Sistem" yang detail, praktis, dan spesifik untuk stack LIQ.
...
(Sisa dari prompt tetap sama)

---