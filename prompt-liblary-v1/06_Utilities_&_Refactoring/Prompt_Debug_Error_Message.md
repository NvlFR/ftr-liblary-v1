### Deskripsi:
Gunakan prompt ini saat Anda menghadapi pesan error, bug, atau perilaku tak terduga dalam kode Anda. Prompt ini dirancang dengan format seperti laporan bug (bug report) untuk memandu Anda memberikan semua informasi yang relevan kepada AI. Dengan memberikan konteks yang lengkap, AI dapat secara drastis meningkatkan akurasi dalam mendiagnosis masalah dan memberikan solusi yang tepat.

### ✅ Prasyarat:
1. Persona developer yang relevan sudah aktif (sangat disarankan).

2. Anda memiliki pesan error lengkap dan potongan kode yang menyebabkan error tersebut.

### Peran Anda:
Berperanlah sebagai seorang Senior Software Engineer dan Debugger yang sangat berpengalaman dan metodis. Anda memiliki kemampuan untuk menganalisis pesan error, stack trace, dan potongan kode secara mendalam untuk menemukan akar masalah (root cause) dengan cepat. Anda tidak hanya memberikan perbaikan, tetapi juga menjelaskan mengapa error itu terjadi dan bagaimana cara mencegahnya di masa depan.

#### Laporan Bug / Error (Bug/Error Report):
Saya mengalami error di proyek **[NAMA_PROYEK]**. Mohon bantu saya untuk mendiagnosis dan memperbaikinya.

1. Pesan Error Lengkap (Full Error Message):
Sertakan semuanya, termasuk nomor baris dan stack trace. Jangan diringkas.

``[Salin dan tempel di sini PESAN ERROR LENGKAP beserta STACK TRACE.]``
2. Deskripsi Masalah (Problem Description):
Jelaskan apa yang sedang Anda coba lakukan dan apa hasil yang Anda harapkan.

``[Jelaskan apa yang sedang Anda coba lakukan saat error ini terjadi dan apa hasil yang Anda harapkan.]``
3. Kode yang Bermasalah (Problematic Code):
Sertakan file dan baris yang relevan. Berikan beberapa baris di atas dan di bawahnya untuk konteks.


``// Nama file: [CONTOH: app/Http/Controllers/MyController.php]
[Salin dan tempel di sini potongan kode yang relevan yang menyebabkan error.]``
4. Apa yang Sudah Dicoba (What I've Tried):
Ini penting agar AI tidak memberikan solusi yang sudah Anda coba.

``[Sebutkan langkah-langkah yang sudah Anda coba untuk memperbaiki masalah ini. Contoh: 'Saya sudah mencoba menjalankan composer dump-autoload', 'Saya sudah memeriksa nama kolom di database', 'Saya sudah clear cache'.]``

5. Konteks Tambahan (Additional Context):
Informasi lain yang mungkin relevan.
```
- Versi Framework/Library: [Contoh: Laravel 11, Vue 3]
- Versi Bahasa: [Contoh: PHP 8.3]
- Lainnya: [Contoh: Error ini hanya terjadi di environment produksi, bukan lokal.]
```
### Tugas Anda:
Berdasarkan laporan bug yang saya berikan di atas, berikan analisis dan solusi yang mendalam. Struktur jawaban Anda harus sebagai berikut:

1. Penjelasan Error (Error Explanation):

Jelaskan apa arti sebenarnya dari pesan error ini dalam bahasa yang mudah dipahami. Terjemahkan jargon teknis menjadi konsep yang sederhana.

2. Kemungkinan Penyebab (Likely Cause):

Tunjukkan 1-2 akar masalah yang paling mungkin berdasarkan kode, pesan error, dan stack trace yang saya berikan.

3. Solusi Langkah-demi-Langkah (Step-by-Step Solution):

Berikan solusi yang jelas dan dapat ditindaklanjuti. Jika perlu ada perbaikan kode, sertakan blok kode "Sebelum Diperbaiki" dan "Setelah Diperbaiki" agar perubahannya sangat jelas.

4. Pencegahan di Masa Depan (Future Prevention):

Berikan saran singkat atau best practice tentang bagaimana cara menghindari error serupa terjadi lagi di kemudian hari.

### Format Output:
Gunakan format Markdown dengan judul yang jelas untuk setiap bagian dari analisis Anda (Penjelasan, Penyebab, Solusi, Pencegahan).


### 🚀 CONTOH PENGGUNAAN NYATA
Bayangkan Anda menghadapi error yang sangat umum di Laravel setelah membuat route baru.

Langkah 1: Aktifkan Persona
Anda sudah berada dalam sesi chat di mana AI berperan sebagai Lead Developer LIQ.

Langkah 2: Berikan Tugas (Menggunakan Template Ini)

Anda mengirim (setelah mengisi template):

Peran Anda:
Berperanlah sebagai seorang Senior Software Engineer dan Debugger...

Laporan Bug / Error (Bug/Error Report):
Saya mengalami error di proyek "POS Toko Sahabat". Mohon bantu saya...

1. Pesan Error Lengkap:

Illuminate\Contracts\Container\BindingResolutionException
Target class [App\Http\Controllers\ProductController] does not exist.
2. Deskripsi Masalah:

Saya baru saja membuat route untuk produk di `routes/web.php`. Tapi saat saya mencoba mengakses URL `/products` di browser, saya malah dapat error ini. Seharusnya halaman yang menampilkan daftar produk muncul.
3. Kode yang Bermasalah:

PHP

// Nama file: routes/web.php
use Illuminate\Support\Facades\Route;

Route::get('/', function () {
    return view('welcome');
});

Route::middleware(['auth'])->group(function () {
    Route::resource('products', ProductController::class);
});
4. Apa yang Sudah Dicoba:

- Saya sudah pastikan file ProductController.php benar-benar ada di folder app/Http/Controllers.
- Saya sudah mencoba menjalankan `php artisan route:clear` dan `composer dump-autoload`.
5. Konteks Tambahan:

- Versi Framework/Library: Laravel 11
- Versi Bahasa: PHP 8.3
Tugas Anda:
Berdasarkan laporan bug yang saya berikan di atas, berikan analisis dan solusi...
(sisa prompt tetap sama)

