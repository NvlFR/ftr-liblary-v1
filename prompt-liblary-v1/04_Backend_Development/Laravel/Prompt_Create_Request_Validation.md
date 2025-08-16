### Deskripsi:
Gunakan prompt ini untuk memerintahkan AI membuat sebuah Form Request Class di Laravel. Best practice di Laravel adalah memisahkan logika validasi dari controller. Kelas ini akan secara otomatis memvalidasi data HTTP yang masuk sebelum logika di dalam controller Anda dieksekusi. Ini membuat kode Anda lebih bersih, lebih aman, dan lebih mudah dibaca.

### ✅ Prasyarat:
1. Persona Persona_Lead_Developer_LIQ.md sudah aktif.

2. Anda sudah tahu field apa saja dari sebuah form yang perlu divalidasi (biasanya saat membuat atau memperbarui data).

# Konteks:
Kita akan membuat sebuah Form Request Class di proyek **[NAMA_PROYEK]**.

Tujuan utama kelas ini adalah untuk menampung semua logika otorisasi (siapa yang boleh melakukan request ini) dan validasi (aturan untuk data yang masuk) untuk resource **[NAMA_RESOURCE]**. Ini akan digunakan di dalam metode Controller untuk menjaga kode tetap rapi (clean code).

### Tugas Anda:
Berperan sebagai seorang Lead Developer LIQ yang sangat mengutamakan keamanan dan kualitas kode melalui validasi yang ketat.

Tugas Anda adalah menulis kode PHP yang lengkap untuk sebuah Form Request Class dengan nama **[NAMA_FORM_REQUEST_CLASS]**.

Kelas tersebut harus memiliki konfigurasi sebagai berikut:
1. Metode authorize():

    - Tentukan logika otorisasi untuk request ini. Apakah semua pengguna yang sudah login boleh melakukan aksi ini, atau ada logika yang lebih spesifik (misalnya, hanya pengguna dengan peran 'admin')?
``[Tuliskan logika otorisasi di sini. Contoh: "Return true;", atau "Return auth()->user()->hasRole('admin');"]``

2. Metode rules():

    - Definisikan aturan-aturan validasi untuk setiap field yang diterima dari form. Gunakan format array dan sintaks validasi standar Laravel.
```
[
'field_1' => 'aturan_1|aturan_2|... (contoh: required|string|max:255)',
'field_2' => 'aturan_1|... (contoh: required|numeric|min:0)',
'field_3' => 'aturan_1|... (contoh: nullable|image|max:2048)',
'email'   => 'required|email|unique:users,email,[ID_YANG_DIKECUALIKAN_SAAT_UPDATE]'
]
```

### Catatan 
Berikan kode PHP yang lengkap untuk file Form Request tersebut.

Pastikan untuk menyertakan namespace, use statements, class yang mengekstensi FormRequest, serta metode authorize() dan rules() yang sudah terisi dengan benar.

Sajikan jawaban Anda dalam satu blok kode PHP yang rapi, siap untuk disimpan ke dalam file app/Http/Requests/[NAMA_FORM_REQUEST_CLASS].php.


### 🚀 CONTOH PENGGUNAAN NYATA
Melanjutkan proyek "POS Toko Sahabat". Kita akan membuat request validation yang akan digunakan oleh metode store() di ProductController yang sudah kita rancang sebelumnya.

Langkah 1: Aktifkan Persona
Anda sudah berada dalam sesi chat di mana AI berperan sebagai Lead Developer LIQ.

Langkah 2: Berikan Tugas (Menggunakan Template Ini)

Anda mengirim (setelah mengisi template):

Konteks:
Kita akan membuat sebuah Form Request Class di proyek "POS Toko Sahabat".

Kelas ini akan digunakan untuk memvalidasi data yang masuk saat membuat resource "Produk Baru".

Tugas Anda:
Berperan sebagai seorang Lead Developer LIQ...

Tugas Anda adalah menulis kode PHP yang lengkap untuk sebuah Form Request Class dengan nama StoreProductRequest.

Kelas tersebut harus memiliki konfigurasi sebagai berikut:

1. Metode authorize():

Return true; // Untuk saat ini, asumsikan semua pengguna yang terotentikasi bisa membuat produk.
2. Metode rules():

[
'name'  => 'required|string|max:255',
'sku'   => 'required|string|max:50|unique:products,sku',
'price' => 'required|numeric|min:0',
'stock' => 'required|integer|min:0'
]
Format Output:
Berikan kode PHP yang lengkap untuk file Form Request tersebut... siap untuk disimpan ke dalam file app/Http/Requests/StoreProductRequest.php.
(sisa prompt tetap sama)