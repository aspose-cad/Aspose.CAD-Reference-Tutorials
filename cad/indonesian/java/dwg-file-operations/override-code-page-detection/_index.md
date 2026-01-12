---
date: 2026-01-12
description: Pelajari cara mengekspor CAD ke PDF sambil mengesampingkan deteksi halaman
  kode otomatis pada file DWG menggunakan Aspose.CAD untuk Java. Menangani pengkodean
  dan CIF/MIF yang rusak.
linktitle: Override Automatic Code Page Detection in DWG Files
second_title: Aspose.CAD Java API
title: Ekspor CAD ke PDF – Mengabaikan Deteksi Halaman Kode Otomatis pada File DWG
  dengan Java
url: /id/java/dwg-file-operations/override-code-page-detection/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ekspor CAD ke PDF – Menimpa Deteksi Halaman Kode Otomatis pada File DWG dengan Java

## Introduction

Dalam panduan komprehensif ini Anda akan menemukan **cara mengekspor CAD ke PDF** sambil menimpa deteksi halaman kode otomatis yang dapat merusak teks pada file DWG. Aspose.CAD untuk Java memberi Anda kontrol detail atas pengkodean, memungkinkan Anda memulihkan data CIF/MIF yang rusak dan menghasilkan output PDF yang dapat diandalkan. Baik Anda membangun konverter batch atau mengintegrasikan pemrosesan CAD ke dalam aplikasi Java yang lebih besar, langkah‑langkah di bawah ini akan memandu Anda melalui seluruh alur kerja.

## Quick Answers
- **Apa arti “override code page”?** Itu memaksa Aspose.CAD menggunakan pengkodean karakter tertentu alih‑alih menebak.
- **Bisakah saya mengekspor DWG langsung ke PDF?** Ya – setelah mengatur halaman kode yang tepat, Anda dapat menyimpan gambar CAD sebagai PDF.
- **Pengkodean mana yang bekerja untuk teks Jepang?** `CodePages.Japanese` dan `MifCodePages.Japanese` adalah pilihan yang tepat.
- **Apakah saya memerlukan lisensi untuk penggunaan produksi?** Lisensi komersial diperlukan; lisensi sementara tersedia untuk pengujian.
- **Versi Aspose.CAD mana yang dibutuhkan?** Versi terbaru apa pun yang mendukung `LoadOptions` dan `PdfOptions`.

## What is “export CAD to PDF”?
Mengekspor CAD ke PDF mengubah gambar CAD berbasis vektor menjadi format dokumen berlayout tetap yang didukung secara luas. PDF yang dihasilkan mempertahankan garis, lapisan, dan teks sambil memudahkan berbagi, mencetak, atau menyematkan gambar dalam aplikasi lain.

## Why override the automatic code page detection?
File DWG sering menyimpan teks menggunakan halaman kode warisan. Deteksi otomatis Aspose.CAD dapat salah menafsirkan byte‑byte ini, menghasilkan karakter yang kacau. Dengan secara manual menentukan halaman kode, Anda memastikan teks muncul persis seperti yang dimaksud dalam PDF yang diekspor, terutama untuk skrip non‑Latin seperti Jepang, Cyrillic, atau Arab.

## Prerequisites
- **Lingkungan Pengembangan Java** – JDK 8+ dan IDE pilihan Anda.
- **Aspose.CAD untuk Java** – Unduh pustaka dari situs resmi [di sini](https://releases.aspose.com/cad/java/).
- **File Contoh DWG** – Gunakan `SimpleEntities.dwg` yang disediakan atau DWG apa pun yang ingin Anda konversi.

## Import Packages
In your Java project, import the necessary Aspose.CAD classes:

```java
import com.aspose.cad.CodePages;
import com.aspose.cad.Image;
import com.aspose.cad.LoadOptions;
import com.aspose.cad.MifCodePages;
import com.aspose.cad.fileformats.cad.CadImage;
```

## Step‑by‑Step Guide

### Step 1: Set Up the Java Project
Buat proyek Maven atau Gradle baru dan tambahkan JAR Aspose.CAD ke classpath. Langkah ini memastikan IDE dapat menemukan kelas‑kelas yang diimpor.

### Step 2: Load the DWG File with a Specified Code Page
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

### Step 3: Export the CAD Image to PDF
Dengan halaman kode yang tepat diterapkan, Anda dapat mengekspor gambar dengan aman. Objek `PdfOptions` memungkinkan Anda menyesuaikan output PDF secara detail (kompresi, rasterisasi, dll.).

```java
// Perform export or other operations with cadImage
// For example, exporting to PDF
PdfOptions pdfOptions = new PdfOptions();
cadImage.save("output.pdf", pdfOptions);
```

### Step 4: Verify Success
Pesan konsol sederhana mengonfirmasi bahwa proses selesai tanpa pengecualian.

```java
System.out.println("OverrideAutomaticCodePageDetectionDwg executed successfully");
```

Anda dapat mengulangi langkah‑langkah ini untuk beberapa file DWG, menyesuaikan jalur sumber dan nama output sesuai kebutuhan.

## Common Issues & Solutions
- **Karakter sampah masih muncul:** Periksa kembali bahwa `specifiedEncoding` cocok dengan halaman kode DWG asli. Gunakan enum `CodePages` yang berbeda jika diperlukan.
- **`NullPointerException` pada `cadImage.save`:** Pastikan file DWG dimuat dengan benar; periksa jalur dan izin file.
- **Ukuran PDF terlalu besar:** Aktifkan kompresi di `PdfOptions` (misalnya, `pdfOptions.setCompress(true)`).

## Frequently Asked Questions

**T1: Apakah Aspose.CAD kompatibel dengan semua versi file DWG?**  
J1: Aspose.CAD mendukung berbagai versi DWG, termasuk AutoCAD 2018 dan rilis sebelumnya.

**T2: Bisakah saya menggunakan Aspose.CAD untuk proyek komersial?**  
J2: Ya, lisensi komersial diperlukan untuk penggunaan produksi. Anda dapat memperoleh lisensi [di sini](https://purchase.aspose.com/buy).

**T3: Apakah ada batasan pada versi percobaan gratis?**  
J3: Versi percobaan memberlakukan batasan ukuran dan fitur; lihat dokumentasi resmi untuk detailnya.

**T4: Bagaimana cara mendapatkan dukungan untuk Aspose.CAD?**  
J4: Kunjungi komunitas [forum Aspose.CAD](https://forum.aspose.com/c/cad/19) untuk bantuan dan diskusi.

**T5: Apakah ada lisensi sementara yang tersedia untuk tujuan pengujian?**  
J5: Ya, lisensi sementara dapat diminta [di sini](https://purchase.aspose.com/temporary-license/).

---

**Terakhir Diperbarui:** 2026-01-12  
**Diuji Dengan:** Aspose.CAD for Java 24.11 (latest at time of writing)  
**Penulis:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}