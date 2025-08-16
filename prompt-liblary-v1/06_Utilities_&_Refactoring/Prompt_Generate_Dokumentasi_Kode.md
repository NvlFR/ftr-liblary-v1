### Deskripsi:
Gunakan prompt ini untuk memerintahkan AI menganalisis sebuah potongan kode dan secara otomatis menghasilkan dokumentasi kode (DocBlocks) yang terstruktur. Tujuannya adalah untuk mendeskripsikan fungsi, parameter, dan nilai kembalian dari sebuah class atau method tanpa harus menuliskannya secara manual. Ini sangat meningkatkan keterbacaan dan kemudahan pemeliharaan kode Anda.

### ✅ Prasyarat:
1. Persona developer senior yang relevan dengan bahasa pemrograman/framework Anda sudah aktif.

2. Anda memiliki potongan kode (fungsi, metode, atau kelas) yang fungsional namun belum memiliki dokumentasi.

### Peran Anda:
Berperanlah sebagai seorang Senior Software Engineer yang sangat disiplin dan teliti. Anda memahami bahwa kode yang tidak terdokumentasi dengan baik adalah "technical debt". Anda ahli dalam menulis dokumentasi kode yang ringkas, akurat, dan mengikuti standar industri agar mudah dibaca oleh manusia dan di-parse oleh tools seperti IDE.

# Konteks:
Saya memiliki sebuah potongan kode dari proyek **[NAMA_PROYEK]**. Kode ini sudah fungsional namun belum memiliki komentar atau dokumentasi (DocBlock) yang layak.

Dokumentasi ini sangat penting agar anggota tim lain (dan saya di masa depan) dapat dengan cepat memahami tujuan, cara penggunaan, parameter, dan hasil dari unit kode ini tanpa harus membaca dan menganalisis seluruh logika implementasinya.

Bahasa pemrograman/framework yang digunakan adalah **[BAHASA_PEMROGRAMAN_&_FRAMEWORK].**

Berikut adalah kode yang perlu Anda dokumentasikan:


``[Salin dan tempel di sini blok kode Anda yang ingin didokumentasikan.]``

### Tugas Anda:
Tuliskan dokumentasi DocBlock yang lengkap dan profesional untuk setiap class, method, atau function yang ada di dalam potongan kode yang saya berikan.

Dokumentasi yang Anda buat harus mengikuti format standar **[NAMA_STANDAR_DOKUMENTASI]** (contoh: PHPDoc untuk PHP, JSDoc untuk JavaScript).

DocBlock tersebut harus mencakup tag-tag berikut (jika relevan):

1. Deskripsi Singkat: Satu kalimat ringkas di baris pertama yang menjelaskan tujuan utama dari unit kode tersebut.

2. Deskripsi Panjang (Opsional): Beberapa kalimat setelah baris kosong untuk memberikan penjelasan yang lebih detail jika ada logika bisnis atau konteks penting yang perlu diketahui.

3. @param: Untuk setiap parameter/argumen, jelaskan: tipe data, nama variabel, dan deskripsi singkat tentang fungsinya.

4. @return: Jelaskan tipe data dari nilai yang dikembalikan (return value) dan deskripsi singkat tentang apa yang direpresentasikannya.

5. @throws (jika ada): Jelaskan jenis exception yang mungkin dilemparkan oleh kode tersebut dan dalam kondisi apa.

### Format Output:
Berikan kembali kode asli yang saya berikan, namun dengan DocBlock yang sudah ditambahkan dengan rapi tepat di atas setiap class atau method.

Sajikan jawaban Anda dalam satu blok kode yang lengkap dan terformat dengan baik.


### 🚀 CONTOH PENGGUNAAN NYATA
Bayangkan kita memiliki sebuah method di dalam sebuah Service Class di Laravel yang logikanya cukup spesifik dan butuh penjelasan.

Langkah 1: Aktifkan Persona
Anda sudah berada dalam sesi chat di mana AI berperan sebagai Lead Developer LIQ.

Langkah 2: Berikan Tugas (Menggunakan Template Ini)

Anda mengirim (setelah mengisi template):

Peran Anda:
Berperanlah sebagai seorang Senior Software Engineer...

Konteks:
Saya memiliki sebuah potongan kode dari proyek "POS Toko Sahabat". Kode ini...
Bahasa pemrograman/framework yang digunakan adalah "PHP / Laravel".

Berikut adalah kode yang perlu Anda dokumentasikan:

PHP

// app/Services/ReportService.php

namespace App\Services;

use App\Models\Transaction;
use Carbon\Carbon;

class ReportService
{
    public function generateDailySalesReport(Carbon $date, string $format = 'array')
    {
        $startOfDay = $date->copy()->startOfDay();
        $endOfDay = $date->copy()->endOfDay();

        $transactions = Transaction::whereBetween('created_at', [$startOfDay, $endOfDay])
            ->with('details.product')
            ->get();

        if ($transactions->isEmpty()) {
            return null;
        }

        $totalRevenue = $transactions->sum('total_amount');
        $totalTransactions = $transactions->count();
        $soldProducts = $transactions->flatMap(fn($trx) => $trx->details)
            ->groupBy('product.name')
            ->map(fn($details) => $details->sum('quantity'));


        $report = [
            'date' => $date->toDateString(),
            'total_revenue' => $totalRevenue,
            'total_transactions' => $totalTransactions,
            'sold_products_summary' => $soldProducts,
        ];

        if ($format === 'json') {
            return json_encode($report);
        }

        return $report;
    }
}
Tugas Anda:
Tuliskan dokumentasi DocBlock... menggunakan format standar PHPDoc.
...

Format Output:
Berikan kembali kode asli yang saya berikan, namun dengan DocBlock yang sudah ditambahkan...
(sisa prompt tetap sama)