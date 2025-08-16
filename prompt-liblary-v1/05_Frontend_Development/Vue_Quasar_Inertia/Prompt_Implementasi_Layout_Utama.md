### Deskripsi:

Gunakan prompt ini untuk memerintahkan AI membuat sebuah Komponen Layout Utama (Persistent Layout). Di dalam aplikasi Inertia, layout adalah komponen Vue yang membungkus komponen halaman Anda. Tujuannya adalah untuk memiliki elemen UI yang konsisten (seperti navigasi dan header) di semua halaman tanpa perlu me-render ulang pada setiap navigasi, sehingga menciptakan pengalaman pengguna layaknya Single-Page Application (SPA) sejati.

### ✅ Prasyarat:

1. Persona Persona_Lead_Developer_LIQ.md sudah aktif.

2. Anda sudah memiliki gambaran umum tentang halaman-halaman utama apa saja yang akan ada di aplikasi Anda untuk dibuatkan menu navigasinya.

# Konteks:

Kita akan membuat komponen Layout Utama untuk proyek **[NAMA_PROYEK]**. Ini akan menjadi "kerangka" atau "cangkang" persisten untuk semua halaman Inertia kita.

Layout ini akan berisi elemen-elemen yang konsisten di seluruh aplikasi, seperti header dan sidebar navigasi. Kita akan memanfaatkan sepenuhnya sistem layout yang kuat dari Quasar Framework (QLayout, QHeader, QDrawer) dan sistem navigasi dari Inertia.js `(<Link>)`.

### Tugas Anda:

Berperan sebagai seorang Lead Developer LIQ yang ahli dalam membuat layout yang responsif dan fungsional.

Tugas Anda adalah menulis kode yang lengkap untuk sebuah Layout Component dengan nama file **[NAMA_FILE_VUE]**.

Layout tersebut harus memiliki struktur dan fungsionalitas sebagai berikut:

1. Bagian Script `(<script setup>)`:

   - Impor ref dari vue untuk mengontrol state drawer (sidebar). Buat sebuah ref bernama leftDrawerOpen dan sebuah fungsi untuk men-toggle-nya.

   - Impor komponen <Link> dari @inertiajs/vue3.

   - Buat sebuah const array bernama menuLinks yang berisi objek-objek untuk setiap item menu navigasi. Setiap objek harus memiliki properti: label (String), icon (String, nama ikon dari Quasar Material Icons), dan route (String, nama route dari Laravel).

   `[Daftar menu navigasi dengan format: { label: 'Nama Menu', icon: 'nama_icon', route: 'nama.route.laravel' }]`

2. Bagian Template `(<template>)`:

   - Gunakan komponen `<QLayout view="lHh Lpr lFf">` sebagai komponen akar.

   - Buat sebuah `<QHeader elevated>` dengan `<QToolbar>` di dalamnya.

     - Di dalam Toolbar, sertakan sebuah `<QBtn>` yang akan memanggil fungsi toggle untuk leftDrawerOpen.

     - Tambahkan sebuah `<QToolbarTitle>` yang berisi judul aplikasi: **[JUDUL_APLIKASI]**.

   - Buat sebuah `<QDrawer v-model="leftDrawerOpen" show-if-above bordered>` untuk sidebar navigasi.

   - Di dalam drawer, buat sebuah `<QList>`.

   - Gunakan v-for untuk melakukan iterasi pada array menuLinks.

   - Untuk setiap item, render komponen `<Link :href="route(link.route)">`.

   - Di dalam komponen `<Link>`, tempatkan sebuah `<QItem clickable v-ripple>` yang memiliki prop :active. Logika untuk :active adalah route().current(link.route).

   - Di dalam `<QItem>`, gunakan `<QItemSection avatar>` untuk ikon `(<QIcon :name="link.icon" />)` dan `<QItemSection>` untuk label `(<QItemLabel>{{ link.label }}</QItemLabel>)`.

   - Di dalam komponen `<QPageContainer>`, tempatkan tag `<slot />.` Ini adalah bagian paling penting, karena di sinilah Inertia akan merender komponen halaman spesifik Anda (misalnya: Products/Index.vue).

### Catatan

Berikan kode yang lengkap untuk Single File Component (.vue), termasuk `<script setup>` dan `<template>`.
Sajikan jawaban Anda dalam satu blok kode Vue yang rapi dan terformat dengan baik, siap untuk disimpan ke dalam file resources/js/Layouts/**[NAMA_FILE_VUE]**.

### 🚀 CONTOH PENGGUNAAN NYATA

Melanjutkan proyek "POS Toko Sahabat".

Langkah 1: Aktifkan Persona
Anda sudah berada dalam sesi chat di mana AI berperan sebagai Lead Developer LIQ.

Langkah 2: Berikan Tugas (Menggunakan Template Ini)

Anda mengirim (setelah mengisi template):

Konteks:
Kita akan membuat komponen Layout Utama untuk proyek "POS Toko Sahabat". Ini akan menjadi "kerangka" atau "cangkang" persisten untuk semua halaman Inertia kita.
...

Tugas Anda:
Berperan sebagai seorang Lead Developer LIQ...
Tugas Anda adalah menulis kode yang lengkap untuk sebuah Layout Component dengan nama file MainLayout.vue.

Layout tersebut harus memiliki struktur dan fungsionalitas sebagai berikut:

1. Bagian Script `(<script setup>)`:

...

Buat sebuah const array bernama menuLinks dengan isi sebagai berikut:

[
{ label: 'Dashboard', icon: 'dashboard', route: 'dashboard' },
{ label: 'Kasir', icon: 'point_of_sale', route: 'cashier.index' },
{ label: 'Produk', icon: 'inventory_2', route: 'products.index' },
{ label: 'Transaksi', icon: 'receipt_long', route: 'transactions.index' },
{ label: 'Supplier', icon: 'local_shipping', route: 'suppliers.index' }
] 2. Bagian Template `(<template>)`:

Gunakan <QLayout>...

Buat <QHeader> dengan <QToolbarTitle> berisi "POS Toko Sahabat".

... (sisa instruksi template tetap sama)

Format Output:
... siap untuk disimpan ke dalam file resources/js/Layouts/MainLayout.vue.
(sisa prompt tetap sama)
