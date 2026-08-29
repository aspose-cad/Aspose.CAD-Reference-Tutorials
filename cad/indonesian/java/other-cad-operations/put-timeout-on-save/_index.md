---
date: 2026-06-19
description: Pelajari cara mengatur timeout saat menyimpan gambar CAD dengan Aspose.CAD
  untuk Java. Tingkatkan kinerja, hindari kegagalan, dan ekspor CAD ke PDF secara
  efisien.
keywords:
- how to set timeout
- convert dwg to pdf
- export cad to pdf
linktitle: Atur Timeout pada Penyimpanan
schemas:
- author: Aspose
  dateModified: '2026-06-19'
  description: Learn how to set timeout on saving CAD drawings with Aspose.CAD for
    Java. Boost performance, avoid hangs, and export CAD to PDF efficiently.
  headline: How to Set Timeout on Save for CAD with Aspose.CAD
  type: TechArticle
- description: Learn how to set timeout on saving CAD drawings with Aspose.CAD for
    Java. Boost performance, avoid hangs, and export CAD to PDF efficiently.
  name: How to Set Timeout on Save for CAD with Aspose.CAD
  steps:
  - name: Set Source and Output Directories
    text: Ensure you have the correct source and output directories for your CAD drawings.
  - name: Create Interruption Token Source
    text: Initialize an interruption token source to manage interruptions during the
      save operation.
  - name: Load CAD Drawing
    text: The `CadImage` class is Aspose.CAD's core object that represents a CAD drawing
      in memory, offering methods for rendering and conversion.
  - name: Configure Rasterization Options
    text: '`CadRasterizationOptions` specifies how the CAD drawing is rasterized into
      an image. Configure rasterization options for the CAD drawing.'
  - name: Configure PDF Options
    text: '`PdfOptions` defines settings for saving a CAD drawing as a PDF document.
      Set up PDF options with vector rasterization options and the interruption token.'
  - name: Save Drawing with Timeout
    text: Save the CAD drawing to a PDF file with the specified timeout.
  - name: Handle Interruption
    text: '`OperationCanceledException` is thrown when a save operation exceeds the
      specified timeout. Create a thread to handle the save operation and interrupt
      it after a specified timeout.'
  type: HowTo
- questions:
  - answer: Yes, wrap each conversion in its own thread with a separate interruption
      token to enforce per‑file time limits.
    question: Can I use this feature to convert DWG to PDF in a batch job?
  - answer: The timeout mechanism is tied to the `InterruptionTokenSource` and works
      with any format that respects the token, including PDF, PNG, and SVG.
    question: Does the timeout work on all output formats?
  - answer: Aspose.CAD automatically discards incomplete output, so you won’t end
      up with corrupted PDFs.
    question: What happens to partially written files after a timeout?
  - answer: Yes, a valid Aspose.CAD license is required for commercial deployments;
      a free trial is available for evaluation.
    question: Is a license required for production use?
  - answer: The official Aspose.CAD documentation provides additional code snippets
      and best‑practice guidelines.
    question: Where can I find more examples of using interruption tokens?
  type: FAQPage
second_title: Aspose.CAD Java API
title: Cara Mengatur Timeout pada Penyimpanan CAD dengan Aspose.CAD
url: /id/java/other-cad-operations/put-timeout-on-save/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cara Mengatur Timeout pada Penyimpanan CAD dengan Aspose.CAD

## Pendahuluan

Dalam panduan komprehensif ini Anda akan mempelajari **cara mengatur timeout** saat menyimpan gambar CAD menggunakan Aspose.CAD untuk Java. Menerapkan timeout mencegah operasi penyimpanan yang berjalan lama menggantungkan aplikasi Anda, yang terutama penting ketika Anda perlu **mengekspor CAD ke PDF** atau **mengonversi DWG ke PDF** dalam skenario pemrosesan batch. Aspose.CAD untuk Java mendukung lebih dari 50 format CAD dan dapat menangani file dengan ratusan halaman tanpa memuat seluruh dokumen ke memori, memberikan kinerja dan penggunaan sumber daya yang dapat diprediksi.

## Jawaban Cepat
- **Apa yang dilakukan timeout?** Ini menghentikan operasi penyimpanan setelah periode yang ditentukan, membebaskan thread dan mencegah kebocoran sumber daya.  
- **Kelas mana yang mengontrol timeout?** `InterruptionTokenSource` menyediakan token pembatalan yang digunakan oleh rutin penyimpanan.  
- **Apakah saya masih dapat mengekspor CAD ke PDF setelah timeout?** Ya – Anda dapat menangkap pengecualian interupsi dan mencoba lagi atau mencatat kegagalan.  
- **Apakah saya memerlukan lisensi khusus?** Lisensi Aspose.CAD reguler sudah cukup; fitur timeout sudah terintegrasi.  
- **Apakah pendekatan ini aman untuk thread?** Ya, ketika setiap penyimpanan dijalankan di thread masing‑masing dengan tokennya sendiri.

## Apa itu timeout dalam operasi penyimpanan CAD?
Timeout adalah batas waktu yang dapat dikonfigurasi yang, ketika terlampaui, memaksa proses penyimpanan berhenti dan mengeluarkan pengecualian interupsi. Ini melindungi aplikasi Java Anda dari kegagalan yang tak terbatas yang disebabkan oleh gambar yang kompleks atau kemacetan I/O.

## Mengapa mengatur timeout saat menyimpan file CAD?
Aspose.CAD dapat **mengonversi DWG ke PDF** dan **mengekspor CAD ke PDF** dalam waktu kurang dari satu detik untuk gambar tipikal, tetapi file yang sangat besar atau rusak dapat memakan menit. Dengan mendefinisikan timeout Anda menjamin bahwa setiap penyimpanan tunggal tidak akan melebihi, misalnya, 30 detik, menjaga throughput batch secara keseluruhan tetap stabil dan mencegah kelaparan thread.

## Prasyarat

Sebelum masuk ke tutorial, pastikan Anda memiliki prasyarat berikut:
- **Aspose.CAD for Java Library** – Pastikan Anda telah mengintegrasikan pustaka Aspose.CAD untuk Java ke dalam proyek Anda. Anda dapat mengunduh pustaka tersebut dari [website](https://releases.aspose.com/cad/java/).
- **Development Environment** – Siapkan lingkungan pengembangan Java Anda dengan semua alat dan dependensi yang diperlukan.

## Impor Paket

Untuk memulai, impor paket yang diperlukan ke dalam proyek Java Anda. Tambahkan baris berikut di awal file Java Anda:

```java
import com.aspose.cad.Image;
import com.aspose.cad.InterruptionTokenSource;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import java.util.concurrent.TimeUnit;
```

Sekarang, mari kita uraikan contoh kode menjadi instruksi langkah demi langkah:

## Cara mengatur timeout pada penyimpanan gambar CAD?

Muat file CAD Anda, buat `InterruptionTokenSource` dengan timeout yang diinginkan, dan berikan token tersebut ke opsi penyimpanan PDF. Jika operasi melebihi timeout, Aspose.CAD akan melempar `OperationCanceledException`, yang dapat Anda tangkap untuk menangani kegagalan secara elegan.

### Langkah 1: Atur Direktori Sumber dan Output

```java
final String SourceDir = Utils.getDataDir_DWGDrawings();
final String OutputDir = Utils.getDataDir_Output();
```

Pastikan Anda memiliki direktori sumber dan output yang benar untuk gambar CAD Anda.

### Langkah 2: Buat Interruption Token Source

```java
final InterruptionTokenSource source = new com.aspose.cad.InterruptionTokenSource();
```

Inisialisasi sumber token interupsi untuk mengelola interupsi selama operasi penyimpanan.

### Langkah 3: Muat Gambar CAD

Kelas `CadImage` adalah objek inti Aspose.CAD yang mewakili gambar CAD dalam memori, menyediakan metode untuk rendering dan konversi.

```java
final CadImage cadImageBig = (CadImage)Image.load(SourceDir + "Drawing11.dwg");
```

### Langkah 4: Konfigurasikan Opsi Rasterisasi

`CadRasterizationOptions` menentukan bagaimana gambar CAD di rasterisasi menjadi sebuah gambar.

```java
CadRasterizationOptions rasterizationOptionsBig = new CadRasterizationOptions();
rasterizationOptionsBig.setPageWidth(cadImageBig.getSize().getWidth() / 2);
rasterizationOptionsBig.setPageHeight(cadImageBig.getSize().getHeight() / 2);
```

Konfigurasikan opsi rasterisasi untuk gambar CAD.

### Langkah 5: Konfigurasikan Opsi PDF

`PdfOptions` mendefinisikan pengaturan untuk menyimpan gambar CAD sebagai dokumen PDF.

```java
final PdfOptions CADfBig = new PdfOptions();
CADfBig.setVectorRasterizationOptions(rasterizationOptionsBig);
CADfBig.setInterruptionToken(source.getToken());
```

Siapkan opsi PDF dengan opsi rasterisasi vektor dan token interupsi.

### Langkah 6: Simpan Gambar dengan Timeout

```java
cadImageBig.save(OutputDir + "PutTimeoutOnSave_out.pdf", CADfBig);
```

Simpan gambar CAD ke file PDF dengan timeout yang ditentukan.

### Langkah 7: Tangani Interupsi

`OperationCanceledException` dilempar ketika operasi penyimpanan melebihi timeout yang ditentukan.

```java
java.lang.Thread thread = new java.lang.Thread(new Runnable() {
    @Override
    public void run() {
        try {
            cadImageBig.save(OutputDir + "PutTimeoutOnSave_out.pdf", CADfBig);
        } catch (Throwable th) {
            System.out.println("interrupted !!!");
        }
    }
});
thread.start();
TimeUnit.SECONDS.sleep(3);
source.interrupt();
thread.join();
```

Buat thread untuk menangani operasi penyimpanan dan interupsi setelah timeout yang ditentukan.

## Masalah Umum dan Solusinya

- **Timeout Terlalu Pendek** – Jika Anda menerima interupsi yang sering, tingkatkan nilai timeout untuk mengakomodasi gambar yang lebih besar.  
- **InterruptedException Tidak Ditangkap** – Selalu bungkus pemanggilan penyimpanan dalam blok try‑catch untuk `OperationCanceledException` guna mencegah aplikasi crash.  
- **Konsumsi Memori** – Gunakan `PdfOptions.setVectorRasterizationOptions` untuk men-stream output daripada memuat seluruh file ke memori.

## Pertanyaan yang Sering Diajukan

**Q: Bisakah saya menggunakan fitur ini untuk mengonversi DWG ke PDF dalam pekerjaan batch?**  
A: Ya, bungkus setiap konversi dalam thread masing‑masing dengan token interupsi terpisah untuk menegakkan batas waktu per‑file.

**Q: Apakah timeout berfungsi pada semua format output?**  
A: Mekanisme timeout terikat pada `InterruptionTokenSource` dan berfungsi dengan format apa pun yang menghormati token, termasuk PDF, PNG, dan SVG.

**Q: Apa yang terjadi pada file yang ditulis sebagian setelah timeout?**  
A: Aspose.CAD secara otomatis membuang output yang tidak lengkap, sehingga Anda tidak akan mendapatkan PDF yang rusak.

**Q: Apakah lisensi diperlukan untuk penggunaan produksi?**  
A: Ya, lisensi Aspose.CAD yang valid diperlukan untuk penyebaran komersial; versi percobaan gratis tersedia untuk evaluasi.

**Q: Di mana saya dapat menemukan contoh lebih lanjut tentang penggunaan token interupsi?**  
A: Dokumentasi resmi Aspose.CAD menyediakan potongan kode tambahan dan panduan praktik terbaik.

## Sumber Daya Tambahan

- [releases page](https://releases.aspose.com/cad/java/) – Halaman unduhan langsung untuk rilis terbaru Aspose.CAD untuk Java.  
- [documentation](https://reference.aspose.com/cad/java/) – Referensi API lengkap dan panduan pengembang.  
- [this link](https://releases.aspose.com/) – Rilis produk Aspose secara umum.  
- [here](https://purchase.aspose.com/temporary-license/) – Dapatkan lisensi sementara untuk pengujian.  
- [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) – Dukungan komunitas dan diskusi.

## Kesimpulan

Anda kini telah menguasai **cara mengatur timeout** untuk menyimpan gambar CAD dengan Aspose.CAD untuk Java. Dengan mengintegrasikan `InterruptionTokenSource` ke dalam alur kerja Anda, Anda dapat dengan andal **mengekspor CAD ke PDF** atau **mengonversi DWG ke PDF** tanpa risiko hang yang lama, menjaga aplikasi Anda tetap responsif dan dapat diskalakan.

**Terakhir Diperbarui:** 2026-06-19  
**Diuji Dengan:** Aspose.CAD untuk Java 24.12  
**Penulis:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Tutorial Terkait

- [Ekspor DWG ke PDF atau Raster Menggunakan Aspose.CAD untuk Java](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)
- [Ekspor Layout DWG Spesifik ke PDF Menggunakan Aspose.CAD untuk Java](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)
- [Konversi DWG ke PNG dan Format Raster Lainnya Menggunakan Aspose.CAD untuk Java](/cad/java/cad-drawing-conversion/convert-cad-layout-to-raster-image/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}