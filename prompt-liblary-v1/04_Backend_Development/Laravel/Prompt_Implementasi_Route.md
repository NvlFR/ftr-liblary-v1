### Deskripsi:
Gunakan prompt ini untuk memerintahkan AI membuat kode registrasi rute (route) di Laravel. Secara spesifik, prompt ini difokuskan untuk mendaftarkan sebuah Resource Controller menggunakan metode Route::resource(), yang secara otomatis akan membuat semua rute yang diperlukan untuk aksi CRUD. Prompt ini juga menekankan pentingnya menerapkan middleware untuk melindungi rute.

### ✅ Prasyarat:
1. Persona Persona_Lead_Developer_LIQ.md sudah aktif.

2. Resource Controller untuk fitur yang bersangkutan sudah dibuat (hasil dari Prompt_Create_Controller_Resource.md).

# Konteks:
Kita perlu mendaftarkan route (rute) untuk resource **[NAMA_RESOURCE]** di proyek **[NAMA_PROYEK]**.

Rute ini akan menjadi titik masuk (entry point) dari browser dan akan memetakan berbagai URL dan metode HTTP (GET, POST, PUT, DELETE) ke metode-metode yang sesuai di dalam **[NAMA_CONTROLLER_CLASS]**.

Karena kita telah membuat Resource Controller yang mengikuti konvensi Laravel, kita akan menggunakan metode Route::resource() untuk mendaftarkan ketujuh rute standar sekaligus secara efisien.

## Tugas Anda:
Berperan sebagai seorang Lead Developer LIQ yang memahami bagaimana merancang rute yang bersih dan aman.

###### Tugas Anda adalah menulis baris kode PHP yang diperlukan untuk mendaftarkan resource route di dalam file routes/web.php.

Rute tersebut harus memiliki konfigurasi sebagai berikut:

1. URL Path: Gunakan path URL **[NAMA_PATH_URL]**. Sesuai konvensi, ini adalah bentuk jamak dan kebab-case (atau snake_case) dari nama resource.

2. Controller Class: Hubungkan path tersebut ke Class Controller **[NAMA_CONTROLLER_CLASS]**.

3. Middleware: Pastikan semua rute untuk resource ini dilindungi oleh middleware yang sesuai untuk keamanan.

``[Sebutkan middleware yang diperlukan. Contoh: "['auth', 'verified']" untuk memastikan hanya pengguna yang sudah login dan emailnya terverifikasi yang bisa mengakses.]``

# Catatan
Berikan hanya blok kode PHP yang berisi definisi rute tersebut.

Jika ada use statement yang diperlukan di bagian atas file (untuk mengimpor Class Controller), sertakan juga.

Kode harus siap untuk disalin dan ditempel di dalam file routes/web.php, idealnya di dalam grup middleware.



### 🚀 CONTOH PENGGUNAAN NYATA
Menyelesaikan implementasi backend untuk fitur Produk di proyek "POS Toko Sahabat".

Langkah 1: Aktifkan Persona
Anda sudah berada dalam sesi chat di mana AI berperan sebagai Lead Developer LIQ.

Langkah 2: Berikan Tugas (Menggunakan Template Ini)

Anda mengirim (setelah mengisi template):

Konteks:
Kita perlu mendaftarkan route (rute) untuk resource "Produk" di proyek "POS Toko Sahabat".

Rute ini akan menghubungkan URL yang diakses oleh pengguna ke metode-metode yang ada di dalam ProductController yang telah kita buat.

Karena kita mengikuti konvensi resource controller, kita harus menggunakan metode Route::resource() untuk efisiensi.

Tugas Anda:
Berperan sebagai seorang Lead Developer LIQ...

Tugas Anda adalah menulis baris kode PHP yang diperlukan untuk mendaftarkan resource route di dalam file routes/web.php.

Rute tersebut harus memiliki konfigurasi sebagai berikut:

URL Path: 'products'

Controller Class: ProductController::class

Middleware: ['auth'] (artinya, hanya pengguna yang sudah login yang bisa mengakses halaman produk).

Format Output:
Berikan hanya blok kode PHP yang berisi definisi rute tersebut...
(sisa prompt tetap sama)