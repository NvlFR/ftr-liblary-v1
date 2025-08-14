# Konteks:
Kita akan melanjutkan ke tahap perencanaan detail untuk proyek **[NAMA_PROYEK]**. Sekarang kita perlu memecah setiap fitur yang telah kita sepakati dalam dokumen Visi & Ruang Lingkup menjadi kebutuhan-kebutuhan yang lebih spesifik dan dapat diukur.

Berikut adalah daftar fitur 'In-Scope' yang telah kita definisikan untuk versi pertama **(MVP)**:

``[Salin dan tempel di sini daftar fitur 'In-Scope' dari dokumen Visi & Ruang Lingkup Anda. Gunakan format daftar poin.]
``

---
### Tugas Anda:
Sebagai seorang System Analyst, tugas Anda adalah mengubah daftar fitur di atas menjadi sebuah "Dokumen Spesifikasi Kebutuhan Fungsional (Functional Requirements Specification)" yang detail dan terstruktur.

---
##### Ikuti aturan pemformatan berikut dengan ketat:

1. Gunakan ID Unik: Setiap kebutuhan fungsional utama harus memiliki ID unik dengan format F-XXX (contoh: F-001, F-002) untuk kemudahan pelacakan (traceability).

2. Berikan Deskripsi: Untuk setiap ID, berikan deskripsi singkat (1-2 kalimat) yang menjelaskan tujuan dari fungsionalitas tersebut.

3. Detailkan Sub-Kebutuhan/Kriteria: Di bawah setiap deskripsi, buat daftar poin (sub-requirements atau kriteria) yang merinci aksi, aturan, atau kondisi spesifik yang harus dipenuhi oleh sistem. Gunakan ID turunan jika perlu (contoh: F-001.1, F-001.2).

---
### Contoh Format yang Diharapkan:
```
**[F-001] Judul Kebutuhan Fungsional**
**Deskripsi:** Penjelasan singkat tentang tujuan utama dari fitur ini.
**Kriteria/Sub-Kebutuhan:**
- F-001.1: Sistem harus memungkinkan pengguna [Peran Pengguna] untuk membuat data baru.
- F-001.2: Form untuk membuat data baru harus berisi field A (wajib), B (opsional), dan C (pilihan dari daftar).
- F-001.3: Setelah data berhasil disimpan, sistem harus menampilkan notifikasi sukses dan mengarahkan pengguna kembali ke halaman daftar.
```

---
## Catatan:
##### Untuk Penulis Yang Harus diperhatikan ketika memakai Liblary ini
Sajikan seluruh dokumen dalam format Markdown yang terstruktur dan rapi sesuai contoh di atas. Mulai dari F-001 untuk fitur pertama dalam daftar, dan lanjutkan secara berurutan.

---
### Deskripsi
Gunakan prompt ini untuk mengubah daftar fitur tingkat tinggi (yang ada di dokumen Visi & Ruang Lingkup) menjadi sebuah Spesifikasi Kebutuhan Fungsional yang formal dan terstruktur. Dokumen ini akan menjadi checklist utama selama proses pengembangan untuk memastikan semua fungsi yang diharapkan telah dibuat.

---
### ✅ Prasyarat:
1. Persona Persona_Business_Analyst.md (atau peran System Analyst) sudah aktif.

2. Anda sudah memiliki dokumen "Visi & Ruang Lingkup" dan daftar fitur 'In-Scope' yang jelas sebagai hasil dari prompt sebelumnya.

---

#### 🚀 CONTOH PENGGUNAAN NYATA
Melanjutkan contoh proyek "KlinikPintar Vet System". Misalkan, hasil dari prompt sebelumnya memberikan daftar fitur In-Scope sebagai berikut:

Manajemen Data Pasien (Hewan) & Pemilik

Pencatatan Rekam Medis

Manajemen Jadwal Janji Temu (Appointment)

Autentikasi Pengguna (Dokter, Staf Administrasi)

Fitur Pencarian Data Pasien

Langkah 1: Pastikan Persona Aktif
Anda sudah berada dalam sesi chat di mana AI berperan sebagai Business/System Analyst.

Langkah 2: Berikan Tugas (Menggunakan Template Ini)

Anda mengirim (setelah mengisi template):

Konteks:
Kita akan melanjutkan ke tahap perencanaan detail untuk proyek "KlinikPintar Vet System". Kita sekarang perlu merinci fitur-fitur yang telah kita sepakati dalam dokumen Visi & Ruang Lingkup.

```
Berikut adalah daftar fitur 'In-Scope' yang telah kita definisikan untuk versi pertama (MVP):

- Manajemen Data Pasien (Hewan) & Pemilik
- Pencatatan Rekam Medis
- Manajemen Jadwal Janji Temu (Appointment)
- Autentikasi Pengguna (Dokter, Staf Administrasi)
- Fitur Pencarian Data Pasien
```
Tugas Anda:
Sebagai seorang System Analyst, tugas Anda adalah mengubah daftar fitur di atas menjadi sebuah "Dokumen Spesifikasi Kebutuhan Fungsional (Functional Requirements Specification)" yang detail.
...
(Sisa dari prompt tetap sama, termasuk bagian 'Contoh Format yang Diharapkan')

---