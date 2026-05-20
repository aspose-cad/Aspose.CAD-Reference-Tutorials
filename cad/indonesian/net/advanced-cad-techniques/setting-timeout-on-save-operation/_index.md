---
date: 2026-03-05
description: Pelajari cara mengatur batas waktu pada operasi penyimpanan saat mengonversi
  DWG ke PDF dengan Aspose.CAD untuk .NET. Tingkatkan efisiensi dan kontrol dalam
  aplikasi .NET Anda.
linktitle: Setting Timeout on Save Operation
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Cara Mengatur Timeout pada Operasi Penyimpanan - Tutorial Aspose.CAD
url: /id/net/advanced-cad-techniques/setting-timeout-on-save-operation/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cara Mengatur Timeout pada Operasi Simpan - Tutorial Aspose.CAD

## Pendahuluan

Dalam panduan ini, Anda akan mempelajari **cara mengatur timeout** pada operasi penyimpanan CAD, sebuah teknik yang membantu Anda menjaga konversi yang berjalan lama tidak menjadi proses yang tidak responsif. Mengelola timeout sangat berguna ketika Anda **mengonversi DWG ke PDF** atau **mengekspor CAD PDF** dalam pekerjaan batch atau layanan web. Aspose.CAD untuk .NET menyediakan API yang bersih yang memungkinkan Anda mengontrol operasi penyimpanan sambil tetap memanfaatkan mesin rasterisasi yang kuat.

## Jawaban Cepat
- **Apa yang dikontrol oleh timeout?** Ia menghentikan operasi simpan/ekspor jika berjalan lebih lama dari periode yang ditentukan.  
- **Format mana yang paling diuntungkan?** Mengonversi file DWG besar ke PDF atau gambar raster di mana waktu pemrosesan dapat bervariasi.  
- **Apakah saya memerlukan lisensi?** Lisensi Aspose.CAD yang valid diperlukan untuk penggunaan produksi; percobaan gratis dapat digunakan untuk evaluasi.  
- **Bisakah saya menyesuaikan durasinya?** Ya—cukup ubah nilai `Thread.Sleep` (dalam milidetik) sesuai skenario Anda.  
- **Apakah pendekatan ini ramah async?** Contoh ini menggunakan `Task.Factory.StartNew`, sehingga mudah diintegrasikan ke alur kerja async.

## Apa itu “cara mengatur timeout” dalam konteks penyimpanan CAD?

Mengatur timeout berarti melampirkan `InterruptionToken` ke opsi penyimpanan dan memicu interupsi setelah interval yang telah ditentukan. Ini mencegah operasi menggantung tanpa batas, memberikan kinerja yang dapat diprediksi dan manajemen sumber daya yang lebih baik.

## Mengapa menggunakan Aspose.CAD untuk mengonversi DWG ke PDF dengan timeout?

- **Keandalan:** Menjamin bahwa konversi yang tidak terkendali tidak akan memblokir layanan Anda.  
- **Skalabilitas:** Memungkinkan Anda memproses banyak file secara paralel tanpa khawatir satu file menghambat alur kerja.  
- **Kualitas:** Mempertahankan rasterisasi berkualitas tinggi Aspose.CAD sambil menambahkan kontrol keamanan.

## Prasyarat

Sebelum kita mulai, pastikan Anda memiliki hal‑hal berikut:

- **Aspose.CAD for .NET** – terintegrasi ke dalam proyek Anda. Anda dapat mengunduhnya [di sini](https://releases.aspose.com/cad/net/).
- **Direktori Dokumen** – folder tempat file DWG sumber dan PDF output Anda akan berada.

## Impor Namespace

Pertama, impor namespace yang menyediakan kelas‑kelas yang kita perlukan untuk rasterisasi, opsi PDF, dan mekanisme interupsi.

```csharp
using Aspose.CAD.ImageOptions;
using System;
using System.Threading;
using System.Threading.Tasks;
```

## Cara Mengatur Timeout pada Operasi Simpan

Berikut adalah langkah‑demi‑langkah. Setiap langkah mencakup penjelasan singkat diikuti oleh blok kode asli (tidak diubah).

### Langkah 1: Muat Gambar CAD

Kami memuat file DWG sumber dari direktori yang ditentukan. Metode `Image.Load` mengembalikan objek `Image` yang mewakili gambar CAD.

```csharp
// Example: Loading CAD Drawing
string SourceDir = "Your Document Directory";
string OutputDir = "Your Document Directory";

using (Image cadDrawing = Image.Load(SourceDir + "Drawing11.dwg"))
{
    // Code for subsequent steps will be placed here
}
```

### Langkah 2: Konfigurasi Opsi Rasterisasi

Atur opsi rasterisasi sehingga PDF yang diekspor cocok dengan dimensi gambar asli. Di sini Anda mengontrol lebar halaman, tinggi, dan pengaturan rendering lainnya.

```csharp
// Example: Configuring Rasterization Options
var rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = cadDrawing.Size.Width;
rasterizationOptions.PageHeight = cadDrawing.Size.Height;
```

### Langkah 3: Buat Opsi PDF (Ekspor CAD PDF)

Buat instance `PdfOptions` dan lampirkan pengaturan rasterisasi. Objek ini akan diteruskan ke metode `Save` untuk menghasilkan versi PDF dari file DWG.

```csharp
// Example: Creating PDF Options
PdfOptions CADf = new PdfOptions();
CADf.VectorRasterizationOptions = rasterizationOptions;
```

### Langkah 4: Implementasikan Mekanisme Timeout

Kami menggunakan `InterruptionTokenSource` untuk memperoleh token yang dapat menginterupsi operasi penyimpanan. Tugas latar belakang melakukan ekspor, sementara thread utama tidur selama durasi timeout yang diinginkan (misalnya, 10 detik). Setelah tidur, kami memanggil `Interrupt()` untuk membatalkan operasi jika masih berjalan.

```csharp
// Example: Implementing Timeout Mechanism
using (var its = new InterruptionTokenSource())
{
    CADf.InterruptionToken = its.Token;

    var exportTask = Task.Factory.StartNew(() =>
    {
        cadDrawing.Save(OutputDir + "PutTimeoutOnSave_out.pdf", CADf);
    });

    Thread.Sleep(10000); // Set your desired timeout duration in milliseconds
    its.Interrupt();

    exportTask.Wait();
}
```

### Langkah 5: Finalisasi dan Konfirmasi

Setelah ekspor (atau interupsi), tulis pesan konfirmasi ke konsol. Dalam aplikasi nyata Anda mungkin mencatat hasil atau memicu sebuah event.

```csharp
// Example: Finalizing and Confirming
Console.WriteLine("PutTimeoutOnSave executed successfully");
```

## Masalah Umum dan Solusinya

| Masalah | Penyebab | Solusi |
|-------|-------|--------|
| Ekspor menggantung tanpa batas | Token interupsi tidak terpasang | Pastikan `CADf.InterruptionToken = its.Token;` diatur sebelum memulai tugas. |
| PDF kosong atau rusak | Path direktori output tidak benar | Verifikasi `OutputDir` diakhiri dengan pemisah path dan nama file valid. |
| Timeout terlalu singkat, menyebabkan abort prematur | Nilai `Thread.Sleep` terlalu rendah untuk file besar | Tingkatkan durasi sleep atau hitung timeout adaptif berdasarkan ukuran file. |

## Pertanyaan yang Sering Diajukan

**Q1: Bisakah saya menyesuaikan durasi timeout?**  
A: Tentu saja. Ubah nilai yang diberikan ke `Thread.Sleep` (dalam milidetik) agar sesuai dengan harapan kinerja Anda.

**Q2: Apakah ada opsi lain untuk rasterisasi?**  
A: Ya. `CadRasterizationOptions` menawarkan properti seperti `Resolution`, `BackgroundColor`, dan `DrawType` untuk menyetel output PDF secara detail.

**Q3: Bagaimana cara menangani interupsi dalam aplikasi saya?**  
A: Gunakan kelas `InterruptionToken` dan `InterruptionTokenSource` seperti yang ditunjukkan. Mereka menyediakan cara yang thread‑safe untuk menghentikan operasi yang berjalan lama.

**Q4: Apakah Aspose.CAD cocok untuk file CAD 2D dan 3D?**  
A: Ia mendukung beragam format 2D dan 3D, termasuk DWG, DXF, DGN, dan lainnya.

**Q5: Di mana saya dapat menemukan bantuan lebih lanjut atau dukungan komunitas?**  
A: Kunjungi [forum Aspose.CAD](https://forum.aspose.com/c/cad/19) untuk diskusi komunitas, contoh kode, dan tips pemecahan masalah.

## Kesimpulan

Dengan mengikuti langkah‑langkah di atas, Anda kini mengetahui **cara mengatur timeout** pada operasi penyimpanan CAD, memungkinkan Anda dengan andal **mengonversi DWG ke PDF** atau **mengekspor CAD PDF** tanpa risiko proses yang tidak responsif. Terapkan pola ini ke konverter batch, layanan web, atau pipeline otomatis apa pun di mana prediktabilitas sangat penting.

---

**Terakhir Diperbarui:** 2026-03-05  
**Diuji Dengan:** Aspose.CAD 24.12 for .NET  
**Penulis:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}