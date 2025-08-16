### Deskripsi:
Gunakan prompt ini untuk memerintahkan AI menulis Unit Test atau Feature Test menggunakan Pest PHP Framework. Tujuannya adalah untuk membuat serangkaian tes otomatis yang memverifikasi bahwa sebuah potongan kode (misalnya, sebuah metode di controller atau logika di model) berfungsi sesuai harapan dalam berbagai skenario. Menulis tes adalah praktik fundamental untuk membangun aplikasi yang andal dan mudah dirawat.

### ✅ Prasyarat:
1. Persona Persona_Lead_Developer_LIQ.md (atau persona developer senior lainnya) sudah aktif.

2, Anda memiliki potongan kode (sebuah "unit") yang jelas untuk diuji.

3. Idealnya, Model Factory untuk membuat data dummy sudah ada (hasil dari Prompt_Generate_Seeder_Data_Dummy.md), karena ini akan sangat mempermudah penulisan tes.

### Peran Anda:
Berperanlah sebagai seorang Senior Software Engineer dengan spesialisasi dalam Quality Assurance (QA) dan pengembangan berbasis tes (Test-Driven Development). Anda sangat mahir menulis unit test dan feature test yang bersih, ekspresif, dan andal menggunakan Pest PHP di dalam ekosistem Laravel. Anda berpikir dalam skenario, mencakup "happy path" (kasus sukses) dan "sad path" (kasus kegagalan).

# Konteks:
Saya ingin Anda menulis test suite (serangkaian tes) untuk sebuah fungsionalitas di proyek **[NAMA_PROYEK]**.

Fokus pengujian adalah pada **[DESKRIPSI_SINGKAT_FUNGSI_YANG_DIUJI]** **(contoh: "metode store di ProductController" atau "sebuah accessor di Model User").**

Tujuan kita adalah untuk memverifikasi bahwa fungsionalitas ini bekerja sesuai harapan dalam berbagai kondisi dan untuk mencegah regresi (kerusakan pada fitur yang sudah ada) di masa depan.

Berikut adalah kode yang akan kita uji:

``[Salin dan tempel di sini blok kode yang relevan, misalnya satu metode controller atau model.]``

### Tugas Anda:
Tuliskan sebuah file test yang lengkap menggunakan sintaks Pest PHP.

File test tersebut harus mencakup beberapa skenario pengujian (test cases) yang relevan untuk memastikan cakupan yang baik. Pikirkan tentang semua kemungkinan input dan output.

Berikut adalah skenario utama yang perlu Anda cakup dalam tes Anda:
```
[
- Skenario 1 (Happy Path): Deskripsikan apa yang seharusnya terjadi saat semuanya berjalan lancar. (Contoh: "Harus berhasil menyimpan data baru ke database saat input valid dan pengguna terotentikasi.")
- Skenario 2 (Sad Path / Validation): Deskripsikan apa yang seharusnya terjadi saat ada input yang tidak valid. (Contoh: "Harus gagal dan mengembalikan error validasi jika field yang wajib diisi dikosongkan.")
- Skenario 3 (Sad Path / Authorization): Deskripsikan apa yang terjadi jika pengguna tidak memiliki izin. (Contoh: "Harus mengembalikan status 403 (Forbidden) jika pengguna dengan peran 'guest' mencoba mengaksesnya.")
- Skenario 4 (Edge Case - Opsional): Deskripsikan skenario unik atau kasus batas. (Contoh: "Harus bisa menangani input dengan nilai 0 atau string kosong dengan benar.")
]
```

### Struktur Test (Penting):
Untuk setiap test case (it(...) atau test(...)), gunakan struktur komentar // Arrange, // Act, // Assert untuk kejelasan:

// Arrange: Siapkan semua kondisi awal, seperti membuat pengguna palsu (User::factory()->create()) dan data yang akan dikirim.

// Act: Lakukan aksi utama yang sedang diuji, seperti melakukan request ke endpoint ($this->actingAs($user)->post(...)).

// Assert: Gunakan berbagai ekspektasi Pest (expect(...)) atau assertion bawaan Laravel untuk memverifikasi hasilnya (contoh: assertDatabaseHas(...), assertRedirect(), assertSessionHasErrors(...)).

### Format Output:
Berikan kode PHP yang lengkap untuk file test Pest.

Pastikan untuk menyertakan use statements yang diperlukan di bagian atas (untuk Model, Controller, dll).

Gunakan trait RefreshDatabase untuk memastikan database bersih untuk setiap tes.

Sajikan jawaban Anda dalam satu blok kode PHP yang rapi, siap untuk disimpan ke dalam file di direktori tests/Feature/ atau tests/Unit/.


### 🚀 CONTOH PENGGUNAAN NYATA
Kita akan menulis tes untuk metode store() di ProductController yang telah kita buat untuk proyek "POS Toko Sahabat".

Langkah 1: Aktifkan Persona
Anda sudah berada dalam sesi chat di mana AI berperan sebagai Lead Developer LIQ / QA.

Langkah 2: Berikan Tugas (Menggunakan Template Ini)

Anda mengirim (setelah mengisi template):

Peran Anda:
Berperanlah sebagai seorang Senior Software Engineer dengan spesialisasi dalam Testing (QA)...

Konteks:
Saya ingin Anda menulis test suite untuk sebuah fungsionalitas di proyek "POS Toko Sahabat".
Fokus pengujian adalah pada "metode store di ProductController untuk membuat produk baru".
...
Berikut adalah kode yang akan kita uji:

PHP

// app/Http/Controllers/ProductController.php
public function store(StoreProductRequest $request)
{
    Product::create($request->validated());

    return to_route('products.index')->with('message', 'Produk berhasil ditambahkan.');
}
Tugas Anda:
Tuliskan sebuah file test menggunakan sintaks Pest PHP.
...
Berikut adalah skenario utama yang perlu Anda cakup dalam tes Anda:

[
- Skenario 1 (Happy Path): "Tes bahwa pengguna yang sudah login dapat membuat produk baru dengan data yang valid, datanya tersimpan di database, dan diarahkan kembali ke halaman index."
- Skenario 2 (Validation Path): "Tes bahwa request akan gagal dengan validation error jika 'name' atau 'price' tidak diisi."
- Skenario 3 (Authorization Path): "Tes bahwa pengguna yang belum login (guest) tidak bisa membuat produk dan akan diarahkan ke halaman login."
]
...

Format Output:
...siap untuk disimpan ke dalam file di direktori tests/Feature/ProductManagementTest.php.
(sisa prompt tetap sama)