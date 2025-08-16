### Deskripsi:
Gunakan prompt ini untuk memerintahkan AI membuat sebuah Model Eloquent di Laravel. Model ini berfungsi sebagai representasi objek dari sebuah tabel database, memungkinkan Anda untuk berinteraksi dengan data (query, insert, update, delete) secara elegan dan intuitif. Prompt ini akan memandu AI untuk mendefinisikan properti penting seperti $fillable dan metode relasi.

### ✅ Prasyarat:
1. Persona Persona_Lead_Developer_LIQ.md sudah aktif.

2. File Migration untuk tabel yang bersangkutan sudah dibuat atau setidaknya sudah dirancang, sehingga daftar kolom dan potensi relasinya sudah jelas. 

# Konteks:
Kita akan membuat Model Eloquent untuk proyek **[NAMA_PROYEK]**.

Model ini akan menjadi representasi dari tabel **[NAMA_TABEL]** di dalam aplikasi kita. Tugasnya adalah untuk menangani semua interaksi data dengan tabel tersebut, termasuk mendefinisikan atribut yang bisa diisi dan relasinya dengan model lain.

### Tugas Anda:
Berperan sebagai seorang Lead Developer LIQ yang sangat memahami best practice dalam penulisan Model Eloquent di Laravel.

Tugas Anda adalah menulis kode PHP yang lengkap untuk sebuah Model Eloquent dengan nama Class **[NAMA_MODEL]**.

##### Model tersebut harus memiliki konfigurasi sebagai berikut:

1. Atribut yang Bisa Diisi (Fillable Attributes):
    - Atur properti protected $fillable untuk mengizinkan mass assignment pada kolom-kolom berikut:
    ```   
    [
    'kolom_1',
    'kolom_2',
    'kolom_3',
    ...
    ] 
    ```

2. Relasi Eloquent (Eloquent Relationships):
    -  Definisikan metode-metode publik berikut untuk merepresentasikan relasi database. Gunakan nama metode yang sesuai dengan konvensi Laravel (nama relasi, camelCase).

    ```
    [
    - nama_relasi_1: jenis_relasi (misal: belongsTo), Model_Tujuan (misal: User::class), foreign_key (opsional, jika tidak sesuai konvensi), local_key (opsional)
    - nama_relasi_2: jenis_relasi (misal: hasMany), Model_Tujuan (misal: Post::class)
    - nama_relasi_3: jenis_relasi (misal: belongsToMany), Model_Tujuan (misal: Tag::class)
    ]
    ```

3. (Opsional) Properti Tambahan:

    - Jika diperlukan, tambahkan properti lain seperti:

        - $casts: Untuk melakukan casting tipe data atribut.

        - $hidden: Untuk menyembunyikan atribut dari representasi JSON/array.

        - $with: Untuk selalu melakukan eager load pada relasi tertentu.
        
        

     ``[Tuliskan properti tambahan jika ada. Contoh: "$casts = ['is_published' => 'boolean', 'price' => 'decimal:2']". Jika tidak ada, biarkan kosong.]``

### Catatan 
Berikan kode PHP yang lengkap untuk file Model tersebut.

Pastikan untuk menyertakan namespace, use statements yang relevan (terutama untuk model lain dalam relasi), class, dan semua properti serta metode relasi yang telah didefinisikan.

Sajikan jawaban Anda dalam satu blok kode PHP yang rapi, siap untuk disimpan ke dalam file app/Models/[NAMA_MODEL].php.



### 🚀 CONTOH PENGGUNAAN NYATA
Melanjutkan proyek "POS Toko Sahabat", kita akan membuat Model untuk Transaction. Model ini menarik karena memiliki relasi ke User dan TransactionDetail.

Langkah 1: Aktifkan Persona

Anda mengirim:
(Isi dari Persona_Lead_Developer_LIQ.md)

AI merespons:
"Saya siap berperan sebagai Lead Developer LIQ. Silakan berikan tugasnya."

Langkah 2: Berikan Tugas (Menggunakan Template Ini)

Anda mengirim (setelah mengisi template):

Konteks:
Kita akan membuat Model Eloquent untuk proyek "POS Toko Sahabat".

Model ini akan menjadi representasi dari tabel transactions di dalam aplikasi kita.

Tugas Anda:
Berperan sebagai seorang Lead Developer LIQ...

Tugas Anda adalah menulis kode PHP yang lengkap untuk sebuah Model Eloquent dengan nama Class Transaction.

Model tersebut harus memiliki konfigurasi sebagai berikut:

1. Atribut yang Bisa Diisi (Fillable Attributes):

[
'user_id',
'total_amount',
'payment_method'
]
2. Relasi Eloquent (Eloquent Relationships):

[
- user: belongsTo, User::class
- details: hasMany, TransactionDetail::class
]
3. (Opsional) Properti Tambahan:

$casts = [
    'total_amount' => 'decimal:2'
]
Format Output:
Berikan kode PHP yang lengkap untuk file Model tersebut...
(sisa prompt tetap sama)