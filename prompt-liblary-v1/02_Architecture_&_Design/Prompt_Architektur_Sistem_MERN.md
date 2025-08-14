# Konteks:
Kita akan merancang arsitektur teknis yang detail untuk proyek **[NAMA_PROYEK]**. Proyek ini telah diputuskan akan dibangun menggunakan tumpukan teknologi MERN **(MongoDB, Express.js, React, Node.js)**.

Sebagai referensi utama, berikut adalah ringkasan dari Dokumen Visi & Ruang Lingkup serta Kebutuhan Fungsional yang telah kita definisikan:

``[Salin dan tempel di sini ringkasan dari dokumen Visi & Kebutuhan Fungsional Anda. Fokus pada skala proyek, kebutuhan data yang dinamis, dan fitur-fitur interaktif.]``

---
### Tugas Anda:

Sebagai seorang **[NAMA_PERSONA_PILIHAN]**, tugas Anda adalah membuat **"Dokumen Desain Arsitektur Sistem"** yang detail, praktis, dan spesifik untuk stack MERN.

###### Dokumen yang Anda hasilkan harus mencakup poin-poin berikut:

1. Pola Arsitektur: Klien-Server Terpisah **(Decoupled Client-Server)**

    - Jelaskan secara rinci mengapa pola arsitektur ini menjadi standar untuk stack MERN. Tekankan pada pemisahan total antara logic backend **(API)** dan presentation frontend **(SPA)**, serta fleksibilitas yang ditawarkannya **(misalnya, frontend bisa dikembangkan menjadi aplikasi mobile tanpa mengubah backend)**.

---
2. Peran Detail Setiap **Komponen MERN**:

    - **MongoDB (Database)**: Jelaskan peran MongoDB sebagai database NoSQL berbasis dokumen yang fleksibel, sangat cocok untuk data yang berkembang atau tidak terstruktur. Sebutkan pentingnya penggunaan Mongoose sebagai ODM **(Object Data Modeling)** untuk mendefinisikan skema, validasi, dan mempermudah interaksi dengan database dari dalam kode Node.js.

    - Express.js & Node.js **(Backend API Server)**: Deskripsikan bagaimana Express.js yang berjalan di atas Node.js akan digunakan untuk membangun sebuah RESTful API yang robust. Ini mencakup:

        - Definisi Endpoints **(rute API)**.

        - Penggunaan **Middleware** (misalnya untuk logging, error handling, dan otentikasi JWT).

        - Controllers yang berisi logika bisnis untuk setiap endpoint.

    - **React (Frontend SPA)**: Jelaskan bagaimana React akan digunakan untuk membangun sebuah Single-Page Application (SPA) yang interaktif. Ini mencakup:

        - Penggunaan React Router untuk menangani navigasi di sisi klien (tanpa me-refresh halaman).

        - Penggunaan Axios atau Fetch API untuk melakukan panggilan HTTP asinkron ke backend API.

        - Manajemen state komponen dan aplikasi.
--- 
3. **Kontrak Komunikasi: RESTful API & JSON**

    - Tekankan bahwa **"kontrak"** atau jembatan utama antara backend dan frontend adalah Spesifikasi REST API. Jelaskan bahwa semua pertukaran data antara klien dan server akan dilakukan dalam format JSON **(JavaScript Object Notation)**.

----
4. Rekomendasi **Struktur Proyek**:

    - Berikan rekomendasi struktur folder yang umum digunakan. Biasanya dalam bentuk dua direktori utama di dalam satu repository **(monorepo)**:

        ##### - server/ (berisi proyek Node.js/Express).

        ##### - client/ (berisi proyek React yang dibuat dengan Create React App atau Vite).

---
5. Diagram **Arsitektur Alur Data**:

    - Buatkan diagram alur data sederhana dalam format kode Mermaid JS **(dengan tipe sequenceDiagram)**. Diagram harus secara visual menggambarkan alur permintaan untuk sebuah fitur: **Pengguna di React App -> Memicu event -> Panggilan HTTP (Axios) -> Endpoint di Express Server -> Controller memproses -> Mongoose berinteraksi dgn MongoDB -> Express mengirim Response JSON -> React App menerima data -> State di-update & UI di-render ulang.**

---
6. Pertimbangan Awal **(Initial Considerations)**:

    - **Keamanan**: Contoh: "Otentikasi akan ditangani menggunakan JSON Web Tokens (JWT). Token akan disimpan di sisi klien (misal: localStorage) dan dikirim pada setiap request ke endpoint yang terlindungi melalui Authorization Header."

    - **Manajemen State Frontend**: Contoh: "Untuk state global yang kompleks (seperti data pengguna yang login, isi keranjang belanja), sarankan penggunaan library manajemen state seperti Redux Toolkit atau Zustand. Untuk state sederhana, cukup gunakan React Context API."

---
### Catataan;
Sajikan dalam format Markdown yang terstruktur, profesional, dan mudah diikuti. Gunakan judul, sub-judul, dan blok kode untuk memisahkan setiap bagian dengan jelas.

---
### Deskripsi:
Gunakan prompt ini untuk memerintahkan AI menghasilkan dokumen desain arsitektur teknis yang spesifik untuk proyek yang menggunakan tumpukan teknologi MERN (MongoDB, Express.js, React, Node.js). Arsitektur MERN secara fundamental berbeda dari LIQ karena mengadopsi model klien-server yang terpisah (decoupled), di mana frontend dan backend adalah dua aplikasi independen yang berkomunikasi melalui API.

---

###  Prasyarat:
1. Persona Persona_System_Architect.md sudah aktif.

2. Anda sudah memiliki dokumen dari Modul 01 ("Visi & Ruang Lingkup" dan "Kebutuhan Fungsional").

---

### 🚀 CONTOH PENGGUNAAN NYATA
Untuk memberikan kontras, kita akan gunakan ide proyek yang berbeda, misalnya "Aplikasi Kanban Board Kolaboratif".

Langkah 1: Aktifkan Persona (Dari Library 00_...)

Anda mengirim:
(Isi dari Persona_System_Architect.md)

AI merespons:
"Saya siap berperan sebagai System Architect senior. Silakan berikan konteks dan tugas spesifiknya."

Langkah 2: Berikan Tugas (Menggunakan Template Ini)

Anda mengirim (setelah mengisi template):

Konteks:
Kita akan merancang arsitektur teknis yang detail untuk proyek "TaskFlow Pro". Proyek ini telah diputuskan akan dibangun menggunakan tumpukan teknologi MERN (MongoDB, Express.js, React, Node.js).

Sebagai referensi utama, berikut adalah ringkasan dari Dokumen Visi & Ruang Lingkup serta Kebutuhan Fungsional yang telah kita definisikan:

'TaskFlow Pro' adalah aplikasi papan kanban kolaboratif mirip Trello. Pengguna bisa membuat papan, menambahkan kolom (misal: To-do, In Progress, Done), dan membuat kartu tugas yang bisa dipindah-pindah antar kolom. Aplikasi ini harus sangat interaktif dengan pembaruan real-time (meskipun untuk MVP, polling atau refresh manual bisa diterima). Struktur data untuk kartu tugas bisa bervariasi (ada lampiran, checklist, dll), sehingga fleksibilitas skema menjadi nilai plus.
Tugas Anda:
Sebagai seorang "System Architect", tugas Anda adalah membuat "Dokumen Desain Arsitektur Sistem" yang detail, praktis, dan spesifik untuk stack MERN.
...
(Sisa dari prompt tetap sama)