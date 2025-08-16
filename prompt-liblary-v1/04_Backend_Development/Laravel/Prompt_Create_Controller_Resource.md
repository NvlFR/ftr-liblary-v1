### Deskripsi:
Gunakan prompt ini untuk memerintahkan AI membuat sebuah Resource Controller di Laravel. Controller ini akan berisi kerangka (skeleton) dari 7 metode standar yang diperlukan untuk operasi CRUD. Prompt ini secara khusus disesuaikan untuk aplikasi LIQ, di mana Controller akan merender halaman Vue menggunakan Inertia::render() dan menangani aksi form dengan RedirectResponse.

### ✅ Prasyarat:
- Persona Persona_Lead_Developer_LIQ.md sudah aktif.

- Model Eloquent untuk resource yang akan dikelola sudah dibuat (hasil dari Prompt_Create_Model_Eloquent.md).

# Konteks:
Kita akan membuat Controller untuk proyek **[NAMA_PROYEK]**.

Controller ini akan berfungsi sebagai pusat logika untuk menangani semua permintaan HTTP yang berkaitan dengan resource **[NAMA_RESOURCE]**. Controller ini akan dibangun untuk aplikasi Inertia.js, artinya view akan di-render menggunakan Inertia::render() dan aksi CUD (Create, Update, Delete) akan diakhiri dengan sebuah redirect.

### Tugas Anda:
Berperan sebagai seorang Lead Developer LIQ yang sangat memahami arsitektur MVC dan routing di Laravel.

Tugas Anda adalah menulis kode PHP yang lengkap untuk sebuah Resource Controller dengan nama Class **[NAMA_CONTROLLER_CLASS]** yang akan mengelola Model **[NAMA_MODEL]**.

Controller tersebut harus memiliki 7 metode standar resource (index, create, store, show, edit, update, destroy).

##### Mohon implementasikan logika dasar atau placeholder di dalam setiap metode sebagai berikut:

- index(): Ambil semua data dari Model **[NAMA_MODEL]** (gunakan paginasi sederhana, misal 10 per halaman) dan kirimkan ke halaman Inertia **[NAMA_FOLDER_VIEW]**/Index.vue.

- create(): Tampilkan halaman Inertia **[NAMA_FOLDER_VIEW]**/Create.vue yang berisi form untuk menambah data baru.

- store(): Gunakan type-hint **[NAMA_FORM_REQUEST_CLASS]** pada parameter $request untuk validasi. Buat record baru di database menggunakan **[NAMA_MODEL]**::create($request->validated()). Terakhir, kembalikan sebuah redirect ke halaman index dengan pesan sukses (->with('message', '...')).

- show(): Gunakan route model binding **([NAMA_MODEL] $[NAMA_MODEL_VARIABLE])**. Tampilkan halaman Inertia **[NAMA_FOLDER_VIEW]**/Show.vue dengan data 

    **$[NAMA_MODEL_VARIABLE]**.



- edit(): Gunakan route model binding **([NAMA_MODEL] $[NAMA_MODEL_VARIABLE])**. Tampilkan halaman Inertia 
    
    **[NAMA_FOLDER_VIEW]**/Edit.vue dengan data
 **$[NAMA_MODEL_VARIABLE]** untuk form edit.

- update(): Gunakan type-hint **[NAMA_FORM_REQUEST_CLASS]** pada parameter $request dan route model binding 

    **[NAMA_MODEL]**
    **$[NAMA_MODEL_VARIABLE]**. 

    Perbarui record $product->update($request->validated()). Terakhir, kembalikan sebuah redirect ke halaman index dengan pesan sukses.



- destroy(): Gunakan route model binding **([NAMA_MODEL] $[NAMA_MODEL_VARIABLE])**. Hapus record tersebut. Terakhir, kembalikan sebuah redirect ke halaman index dengan pesan sukses.

### Catatan 
Berikan kode PHP yang lengkap untuk file Controller.

Pastikan untuk menyertakan namespace, use statements yang relevan (untuk Request, Inertia, Model, dll.), class, dan kerangka lengkap dari 7 metode yang telah diisi sesuai instruksi.

Sajikan jawaban Anda dalam satu blok kode PHP yang rapi, siap untuk disimpan ke dalam file app/Http/Controllers/[NAMA_CONTROLLER_CLASS].php


### 🚀 CONTOH PENGGUNAAN NYATA
Melanjutkan proyek "POS Toko Sahabat", kita akan membuat Controller untuk mengelola Produk.

Langkah 1: Aktifkan Persona
Anda sudah berada dalam sesi chat di mana AI berperan sebagai Lead Developer LIQ.

Langkah 2: Berikan Tugas (Menggunakan Template Ini)

Anda mengirim (setelah mengisi template):

Konteks:
Kita akan membuat Controller untuk proyek "POS Toko Sahabat". Controller ini akan berfungsi sebagai pusat logika untuk menangani semua permintaan HTTP yang berkaitan dengan resource "Produk". Controller ini akan dibangun untuk aplikasi Inertia.js...

Tugas Anda:
Berperan sebagai seorang Lead Developer LIQ...

Tugas Anda adalah menulis kode PHP yang lengkap untuk sebuah Resource Controller dengan nama Class ProductController yang akan mengelola Model Product.

Controller tersebut harus memiliki 7 metode standar...
(Instruksi detail untuk 7 metode diisi dengan placeholder yang sudah diganti):

index(): ...kirimkan ke halaman Inertia Products/Index.vue.

create(): ...tampilkan halaman Inertia Products/Create.vue.

store(): Gunakan StoreProductRequest, buat record Product, redirect ke halaman index.

show(): Gunakan Product $product, tampilkan Products/Show.vue dengan data $product.

edit(): Gunakan Product $product, tampilkan Products/Edit.vue dengan data $product.

update(): Gunakan UpdateProductRequest dan Product $product, perbarui record $product, redirect ke index.

destroy(): Gunakan Product $product, hapus record $product, redirect ke index.

Format Output:
Berikan kode PHP yang lengkap untuk file Controller... siap untuk disimpan ke dalam file app/Http/Controllers/ProductController.php.
(sisa prompt tetap sama)
