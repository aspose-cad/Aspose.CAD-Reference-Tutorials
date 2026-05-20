---
date: 2026-05-20
description: Pelajari cara mengonversi DWG ke PDF sambil menimpa deteksi otomatis
  halaman kode menggunakan Aspose.CAD for Java. Termasuk langkah-langkah export dwg
  to pdf, tips encoding, dan troubleshooting.
keywords:
- convert dwg pdf
- export dwg to pdf
- Aspose.CAD Java
linktitle: Menimpa Deteksi Otomatis Halaman Kode pada File DWG
schemas:
- author: Aspose
  dateModified: '2026-05-20'
  description: Learn how to convert DWG to PDF while overriding automatic code page
    detection using Aspose.CAD for Java. Includes export dwg to pdf steps, encoding
    tips, and troubleshooting.
  headline: Convert DWG to PDF – Override Code Page Detection in Java
  type: TechArticle
- description: Learn how to convert DWG to PDF while overriding automatic code page
    detection using Aspose.CAD for Java. Includes export dwg to pdf steps, encoding
    tips, and troubleshooting.
  name: Convert DWG to PDF – Override Code Page Detection in Java
  steps:
  - name: Set Up the Java Project
    text: Create a Maven or Gradle project and add the Aspose.CAD JAR to the classpath.
      This ensures the IDE can resolve the imported classes and that the runtime can
      locate the library.
  - name: Load the DWG File with a Specified Code Page
    text: Tell Aspose.CAD which encoding to use and whether to attempt recovery of
      malformed CIF/MIF data.
  - name: Export the CAD Image to PDF
    text: With the correct code page applied, you can safely export the drawing. The
      `PdfOptions` object lets you fine‑tune the PDF output (compression, rasterization,
      etc.).
  - name: Verify Success
    text: A simple console message confirms that the process completed without exceptions.
      You can repeat these steps for multiple DWG files, adjusting the source path
      and output name as needed.
  type: HowTo
- questions:
  - answer: It forces Aspose.CAD to use a specific character encoding instead of guessing.
    question: What does “override code page” mean?
  - answer: Yes – after setting the correct code page, you can save the CAD image
      as PDF.
    question: Can I export DWG directly to PDF?
  - answer: '`CodePages.Japanese` and `MifCodePages.Japanese` are the right choices.'
    question: Which encoding works for Japanese text?
  - answer: A commercial license is required; a temporary license is available for
      testing.
    question: Do I need a license for production use?
  - answer: Any recent version that supports `LoadOptions` and `PdfOptions`.
    question: What version of Aspose.CAD is needed?
  type: FAQPage
second_title: Aspose.CAD Java API
title: Konversi DWG ke PDF – Menimpa Deteksi Halaman Kode di Java
url: /id/java/dwg-file-operations/override-code-page-detection/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Konversi DWG ke PDF – Menimpa Deteksi Halaman Kode di Java

Dalam tutorial komprehensif ini Anda akan belajar **cara mengonversi DWG ke PDF** sambil menimpa deteksi otomatis halaman kode yang dapat merusak teks. Aspose.CAD untuk Java memberi Anda kontrol tepat atas pengkodean karakter, memungkinkan pemulihan data CIF/MIF yang rusak dan menghasilkan output PDF yang dapat diandalkan. Baik Anda membangun konverter batch maupun menambahkan pemrosesan CAD ke layanan Java yang lebih besar, langkah‑langkah di bawah ini akan memandu Anda melalui seluruh alur kerja—dari penyiapan proyek hingga verifikasi.

## Jawaban Cepat
- **Apa arti “menimpa halaman kode”?** Itu memaksa Aspose.CAD menggunakan pengkodean karakter tertentu alih‑alih menebak.
- **Apakah saya dapat mengekspor DWG langsung ke PDF?** Ya – setelah mengatur halaman kode yang tepat, Anda dapat menyimpan gambar CAD sebagai PDF.
- **Pengkodean apa yang cocok untuk teks Jepang?** `CodePages.Japanese` dan `MifCodePages.Japanese` adalah pilihan yang tepat.
- **Apakah saya memerlukan lisensi untuk penggunaan produksi?** Lisensi komersial diperlukan; lisensi sementara tersedia untuk pengujian.
- **Versi Aspose.CAD apa yang dibutuhkan?** Versi terbaru apa pun yang mendukung `LoadOptions` dan `PdfOptions`.

## Apa itu “ekspor CAD ke PDF”?
Mengekspor CAD ke PDF mengubah gambar DWG berbasis vektor menjadi dokumen PDF dengan tata letak tetap yang dapat dilihat secara universal. Konversi ini mempertahankan semua entitas geometris, garis, lapisan, dan teks yang disematkan, sambil meratakan gambar ke dalam format yang mudah dibagikan, dicetak, diarsipkan, atau disematkan dalam aplikasi lain tanpa memerlukan perangkat lunak CAD.

## Mengapa menimpa deteksi otomatis halaman kode?
Menentukan halaman kode secara manual menjamin bahwa byte teks diinterpretasikan dengan benar, menghilangkan karakter kacau yang sering muncul ketika deteksi otomatis Aspose.CAD menebak pengkodean warisan yang salah. Ini penting untuk skrip non‑Latin seperti Jepang, Cyrillic, atau Arab, dan memastikan PDF yang diekspor cocok dengan desain asli.

## Prasyarat
- **Lingkungan Pengembangan Java** – JDK 8+ dan IDE pilihan Anda.  
- **Aspose.CAD untuk Java** – Unduh pustaka dari situs resmi [di sini](https://releases.aspose.com/cad/java/).  
- **File Contoh DWG** – Gunakan `SimpleEntities.dwg` yang disediakan atau DWG apa pun yang ingin Anda konversi.

## Impor Paket
Kelas `Document`, `LoadOptions`, dan `PdfOptions` adalah inti proses konversi.

Kelas `Document` mewakili gambar CAD dalam memori, menyediakan metode untuk memuat, memanipulasi, dan menyimpan file dalam berbagai format.  
Kelas `LoadOptions` memungkinkan Anda menentukan halaman kode dan opsi pemulihan saat memuat file DWG.  
Kelas `PdfOptions` mengontrol pengaturan khusus PDF seperti kompresi, rasterisasi, dan metadata.

Di proyek Java Anda, impor kelas Aspose.CAD yang diperlukan:

```java
import com.aspose.cad.CodePages;
import com.aspose.cad.Image;
import com.aspose.cad.LoadOptions;
import com.aspose.cad.MifCodePages;
import com.aspose.cad.fileformats.cad.CadImage;
```

## Cara mengonversi DWG ke PDF dengan menimpa halaman kode?
Muat file DWG menggunakan `LoadOptions` untuk menentukan halaman kode yang tepat, lalu panggil metode `save` pada `CadImage` yang dihasilkan dengan instance `PdfOptions` yang telah dikonfigurasi. Pendekatan dua langkah ini memastikan teks diinterpretasikan dengan benar dan PDF yang dihasilkan mempertahankan fidelitas gambar asli, lapisan, serta kualitas vektor.

### Langkah 1: Siapkan Proyek Java
Buat proyek Maven atau Gradle dan tambahkan JAR Aspose.CAD ke classpath. Ini memastikan IDE dapat menemukan kelas yang diimpor dan runtime dapat menemukan pustaka.

### Langkah 2: Muat File DWG dengan Halaman Kode yang Ditentukan
Beritahu Aspose.CAD pengkodean mana yang akan digunakan dan apakah akan mencoba memulihkan data CIF/MIF yang rusak.

```java
String SourceDir = "Your Document Directory";
String dwgPathToFile = SourceDir + "SimpleEntites.dwg";
LoadOptions opts = new LoadOptions();
opts.setSpecifiedEncoding(CodePages.Japanese);
opts.setSpecifiedMifEncoding(MifCodePages.Japanese);
opts.setRecoverMalformedCifMif(false);
CadImage cadImage = (CadImage) Image.load(dwgPathToFile, opts);
```

### Langkah 3: Ekspor Gambar CAD ke PDF
Dengan halaman kode yang tepat diterapkan, Anda dapat mengekspor gambar dengan aman. Objek `PdfOptions` memungkinkan Anda menyesuaikan output PDF (kompresi, rasterisasi, dll.).

```java
// Perform export or other operations with cadImage
// For example, exporting to PDF
PdfOptions pdfOptions = new PdfOptions();
cadImage.save("output.pdf", pdfOptions);
```

### Langkah 4: Verifikasi Keberhasilan
Pesan konsol sederhana mengonfirmasi bahwa proses selesai tanpa pengecualian.

```java
System.out.println("OverrideAutomaticCodePageDetectionDwg executed successfully");
```

Anda dapat mengulangi langkah‑langkah ini untuk banyak file DWG, menyesuaikan jalur sumber dan nama output sesuai kebutuhan.

## Masalah Umum & Solusi
- **Karakter sampah masih muncul:** Periksa kembali bahwa `specifiedEncoding` cocok dengan halaman kode DWG asli. Gunakan enum `CodePages` yang berbeda bila diperlukan.  
- **`NullPointerException` pada `cadImage.save`:** Pastikan file DWG berhasil dimuat; periksa jalur dan izin file.  
- **Ukuran PDF terlalu besar:** Aktifkan kompresi di `PdfOptions` (misalnya, `pdfOptions.setCompress(true)`) untuk mengurangi ukuran file tanpa mengorbankan kualitas.

## Pertanyaan yang Sering Diajukan

**T1: Apakah Aspose.CAD kompatibel dengan semua versi file DWG?**  
J1: Aspose.CAD mendukung lebih dari 30 versi DWG, termasuk AutoCAD 2018 dan rilis sebelumnya.

**T2: Bisakah saya menggunakan Aspose.CAD untuk proyek komersial?**  
J2: Ya, lisensi komersial diperlukan untuk penggunaan produksi. Anda dapat memperoleh lisensi [di sini](https://purchase.aspose.com/buy).

**T3: Apakah ada batasan pada versi percobaan gratis?**  
J3: Versi percobaan memberlakukan batasan ukuran dan fitur; lihat dokumentasi resmi untuk detailnya.

**T4: Bagaimana cara mendapatkan dukungan untuk Aspose.CAD?**  
J4: Kunjungi komunitas [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) untuk bantuan dan diskusi.

**T5: Apakah ada lisensi sementara tersedia untuk tujuan pengujian?**  
J5: Ya, lisensi sementara dapat diminta [di sini](https://purchase.aspose.com/temporary-license/).

---

**Terakhir Diperbarui:** 2026-05-20  
**Diuji Dengan:** Aspose.CAD untuk Java 24.11 (terbaru pada saat penulisan)  
**Penulis:** Aspose

## Tutorial Terkait

- [Ekspor DWG ke PDF dan Konversi Gambar CAD – Tutorial Aspose.CAD Java](/cad/java/cad-drawing-conversion/)
- [Ekspor Layout DWG Spesifik ke PDF Menggunakan Aspose.CAD untuk Java](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)
- [Ekspor DWG ke PDF atau Raster Menggunakan Aspose.CAD untuk Java](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< blocks/products/products-backtop-button >}}

{{< /blocks/products/pf/main-wrap-class >}}