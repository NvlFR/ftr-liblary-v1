### Deskripsi:
Gunakan prompt ini untuk memerintahkan AI membuat sebuah Komponen Vue yang Dapat Digunakan Ulang (Reusable Component). Komponen ini akan berupa sebuah dialog (pop-up) yang berisi form untuk membuat (Create) dan memperbarui (Update) data. Komponen ini akan menggunakan QDialog dan QForm dari Quasar, serta composable useForm dari Inertia.js untuk manajemen state dan validasi.

### ✅ Prasyarat:
1. Persona Persona_Lead_Developer_LIQ.md sudah aktif.

2. Anda sudah tahu field-field apa saja yang dibutuhkan oleh form untuk sebuah resource.

3. Anda sudah memiliki backend (Controller & Route) untuk aksi store dan update.

# Konteks:
Kita akan membuat Komponen Vue yang Dapat Digunakan Ulang (Reusable Component) untuk proyek **[NAMA_PROYEK]**.

Komponen ini akan menjadi sebuah Dialog Form yang menggunakan Quasar QDialog dan QForm. Tujuannya adalah agar kita bisa menggunakan form yang sama untuk aksi 'Tambah Data Baru' dan 'Edit Data', yang biasanya dipicu dari halaman indeks.

Komponen ini harus mandiri dan mengelola state-nya sendiri (termasuk data input dan pesan error) menggunakan composable useForm dari Inertia.js.

### Tugas Anda:
Berperan sebagai seorang Lead Developer LIQ yang ahli dalam component-based design dan manajemen state form dengan Inertia di Vue 3.

Tugas Anda adalah menulis kode yang lengkap untuk sebuah Reusable Form Dialog Component dengan nama file **[NAMA_FILE_VUE]**.

Komponen tersebut harus memiliki fungsionalitas sebagai berikut:

1. Props:

    - Gunakan defineModel``<boolean>()`` (atau prop modelValue dan emit('update:modelValue')) agar visibilitas dialog bisa dikontrol dari komponen induk menggunakan v-model.

    - Buat sebuah prop bernama **[NAMA_PROP_MODEL]** (contoh: product, supplier). Tipe datanya adalah Object dan bersifat opsional (default null). Prop ini akan diisi dengan data resource saat kita ingin mengedit.

2. Bagian Script ``(<script setup>)``:

    - Impor useForm dari @inertiajs/vue3 dan impor watch, computed dari vue.

    - Inisialisasi form state menggunakan const form = useForm({...}). Definisikan semua field yang ada di dalam form dengan nilai awalnya string kosong ('') atau null.

    - Buat sebuah computed property bernama isEditMode yang akan bernilai true jika prop **[NAMA_PROP_MODEL]** tidak null.

    - Gunakan watch untuk "mengamati" perubahan pada prop [NAMA_PROP_MODEL]. Jika prop ini berubah (diisi data untuk diedit), segera perbarui nilai-nilai di dalam form Inertia (form.name = props.[NAMA_PROP_MODEL].name, dst.). Jika prop menjadi null, reset form (form.reset()).

    - Buat sebuah fungsi submit() yang cerdas:

        - Jika isEditMode bernilai true, jalankan form.put(route('**[ROUTE_NAME_UPDATE]**', props.**[NAMA_PROP_MODEL]**.id), { onSuccess: () => ... }).

        - Jika isEditMode bernilai false, jalankan form.post(route('**[ROUTE_NAME_STORE]**'), { onSuccess: () => ... }).

        - Pada onSuccess, panggil fungsi untuk menutup dialog.

3. Bagian Template ``(<template>)``:

    - Gunakan komponen ``<QDialog>`` yang v-model-nya terikat pada prop yang Anda definisikan.

    - Di dalam dialog, gunakan struktur ``<QCard>, <QCardSection>, dan <QForm @submit.prevent="submit">.``

    - Buat judul card yang dinamis menggunakan computed property, contoh: ``{{ isEditMode ? 'Edit Data' : 'Tambah Data Baru' }}.``

    - Buat input untuk setiap field form menggunakan komponen Quasar yang sesuai ``(misal: <QInput>, <QSelect>)``.

        - Bind v-model dari setiap input ke state form Inertia (contoh: v-model="form.name").

        - Tampilkan pesan error validasi dari Inertia dengan prop :error-message="form.errors.name" dan :error="form.errors.name ? true : false".

    - Di dalam ``<QCardActions>``, buat tombol "Simpan" ``(<QBtn type="submit">)`` yang memiliki state loading (:loading="form.processing") dan tombol "Batal" ``(<QBtn>)`` untuk menutup dialog.

### Catatan
Berikan kode yang lengkap untuk Single File Component (.vue). Sajikan dalam satu blok kode Vue yang rapi, siap untuk disimpan ke dalam file resources/js/Components/[NAMA_FILE_VUE].

### 🚀 CONTOH PENGGUNAAN NYATA
Melanjutkan fitur Produk untuk proyek "POS Toko Sahabat".

 Langkah 1: Pastikan Persona Aktif
Anda sudah berada dalam sesi chat di mana AI berperan sebagai Lead Developer LIQ.

Langkah 2: Berikan Tugas (Menggunakan Template Ini)

Anda mengirim (setelah mengisi template):

Konteks:
Kita akan membuat Komponen Vue yang Dapat Digunakan Ulang untuk proyek "POS Toko Sahabat". Komponen ini akan berupa sebuah Dialog Form untuk menambah dan mengedit data Produk.

Tugas Anda:
...
Tugas Anda adalah menulis kode yang lengkap untuk sebuah Reusable Form Dialog Component dengan nama file ProductFormDialog.vue.

Komponen tersebut harus memiliki fungsionalitas berikut:

1. Props:

Gunakan defineModel``<boolean>() ``untuk v-model.

Buat prop bernama product (Object, default null).

2. Bagian Script ``(<script setup>)``:

Inisialisasi useForm dengan field: name, sku, price, dan stock.

Gunakan watch pada prop product untuk mengisi atau me-reset form.

Fungsi submit() harus melakukan POST ke route 'products.store' saat mode create, dan PUT ke route 'products.update' saat mode edit.

Saat onSuccess, tutup dialog.

3. Bagian Template ``(<template>)``:

Gunakan ``<QDialog>...``

Buat judul dinamis: ``{{ isEditMode ? 'Edit Produk' : 'Tambah Produk Baru' }}.``

Buat ``<QInput> ``untuk name, sku, price (type number), dan stock (type number). Tampilkan error validasi untuk masing-masing.

...

Format Output:
...siap untuk disimpan ke dalam file resources/js/Components/ProductFormDialog.vue.
(sisa prompt tetap sama)