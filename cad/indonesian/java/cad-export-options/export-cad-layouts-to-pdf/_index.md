---
date: 2025-12-21
description: Pelajari cara mengekspor tata letak CAD ke PDF menggunakan Aspose.CAD
  untuk Java – cara cepat dan andal untuk menghasilkan PDF dari file CAD.
linktitle: Export CAD Layouts to PDF
second_title: Aspose.CAD Java API
title: Cara Mengekspor Layout CAD ke PDF dengan Aspose.CAD untuk Java
url: /id/java/cad-export-options/export-cad-layouts-to-pdf/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cara Mengekspor Tata Letak CAD ke PDF dengan Aspose.CAD untuk Java

## Pendahuluan

Dalam tutorial ini, kami akan menunjukkan **cara mengekspor CAD** tata letak ke PDF dengan Aspose.CAD untuk Java. Baik Anda bekerja dengan DWG, DXF, atau format CAD lainnya, panduan ini akan memandu Anda melalui pendekatan programatik yang bersih untuk menghasilkan PDF dari file CAD dengan cepat dan dapat diandalkan.

## Jawaban Cepat
- **Apa yang dilakukan perpustakaan ini?** It converts CAD drawings (DWG, DXF, DWF, etc.) into PDF, raster images, and other formats.  
- **Bahasa apa yang digunakan?** Java – the code runs on any JVM‑compatible platform.  
- **Apakah saya memerlukan lisensi?** Versi percobaan gratis tersedia; lisensi komersial diperlukan untuk produksi.  
- **Bisakah saya mengonversi DWG ke PDF di Java?** Ya – API yang sama mendukung **dwg to pdf java** conversions.  
- **Apa langkah utama?** Muat file CAD, atur opsi rasterisasi, konfigurasikan opsi PDF, dan simpan hasilnya.

## Prasyarat

Sebelum kita memulai tutorial, pastikan Anda memiliki prasyarat berikut:

- Aspose.CAD untuk Java: Pastikan Anda telah menginstal perpustakaan tersebut. Anda dapat mengunduhnya dari situs web Aspose [di sini](https://releases.aspose.com/cad/java/).
- Lingkungan Pengembangan Java: Pastikan Anda memiliki lingkungan pengembangan Java yang terpasang di mesin Anda.

Setelah semuanya siap, mari kita mulai tutorial.

## Apa itu “cara mengekspor cad”?

Mengekspor CAD berarti mengonversi data gambar CAD asli (seperti DWG, DXF, atau DWF) ke format yang lebih universal dapat dibaca seperti PDF. Proses ini penting untuk berbagi desain dengan pemangku kepentingan yang mungkin tidak memiliki perangkat lunak CAD terpasang.

## Mengapa Menggunakan Aspose.CAD untuk Java untuk Mengekspor CAD ke PDF?

- **High fidelity** – grafik vektor dipertahankan, dan opsi rasterisasi memungkinkan Anda menyesuaikan kualitas secara halus.  
- **No external dependencies** – Java murni, tanpa DLL native atau komponen COM.  
- **Supports multiple formats** – Anda juga dapat **generate pdf from cad** file yang dibuat dalam DWG, DWF, atau format lainnya.  
- **Scalable for batch jobs** – ideal untuk otomatisasi sisi server, pipeline CI, atau utilitas desktop.

## Impor Namespace

Dalam kode Java Anda, mulailah dengan mengimpor namespace yang diperlukan. Impor ini memberikan akses ke kelas dan metode yang dibutuhkan untuk bekerja dengan Aspose.CAD untuk Java.

```java
import com.aspose.cad.Image;
import com.aspose.cad.InterpolationMode;
import com.aspose.cad.SmoothingMode;
import com.aspose.cad.TextRenderingHint;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
//import com.aspose.cad.imageoptions.TypeOfEntities;
```

## Langkah 1: Muat File CAD

Mulailah dengan memuat file CAD ke dalam aplikasi Java Anda menggunakan metode `Image.load`. Ganti `"conic_pyramid.dxf"` dengan jalur ke file CAD Anda.

```java
String dataDir = "Your Document Directory" + "ExportingCAD/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image cadImage = Image.load(srcFile);
```

## Langkah 2: Atur Opsi Rasterisasi

Buat sebuah instance `CadRasterizationOptions` untuk menentukan bagaimana entitas CAD harus dirasterisasi. Sesuaikan parameter seperti lebar halaman, tinggi halaman, dan skala tata letak sesuai kebutuhan Anda.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
rasterizationOptions.setAutomaticLayoutsScaling(true);
rasterizationOptions.setNoScaling(false);
rasterizationOptions.setContentAsBitmap(true);
rasterizationOptions.setLayouts(new String[]{"Model"});
```

## Langkah 3: Atur Opsi PDF

Buat sebuah instance `PdfOptions` dan hubungkan dengan opsi rasterisasi. Selain itu, atur opsi grafis untuk ekspor PDF, seperti mode smoothing, petunjuk rendering teks, dan mode interpolasi.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
rasterizationOptions.getGraphicsOptions().setSmoothingMode(SmoothingMode.HighQuality);
rasterizationOptions.getGraphicsOptions().setTextRenderingHint(TextRenderingHint.AntiAliasGridFit);
rasterizationOptions.getGraphicsOptions().setInterpolationMode(InterpolationMode.HighQualityBicubic);
```

## Langkah 4: Ekspor ke PDF

Akhirnya, ekspor tata letak CAD ke file PDF menggunakan metode `save` dari objek `cadImage`.

```java
cadImage.save(dataDir + "CADLayoutsToPDF_out_.pdf", pdfOptions);
```

## Masalah Umum dan Solusinya

| Issue | Reason | Fix |
|-------|--------|-----|
| **Output PDF kosong** | Opsi rasterisasi tidak diatur dengan benar (misalnya, nama tata letak tidak cocok) | Verifikasi `rasterizationOptions.setLayouts()` sesuai dengan nama tata letak dalam file CAD Anda. |
| **Gambar beresolusi rendah** | `PageWidth`/`PageHeight` terlalu kecil | Tingkatkan dimensi halaman atau atur DPI yang lebih tinggi melalui `rasterizationOptions.setResolution()`. |
| **Versi CAD tidak didukung** | Versi DWG/DXF yang lebih lama mungkin memerlukan build Aspose.CAD yang lebih baru | Unduh versi perpustakaan terbaru dari situs Aspose. |

## Pertanyaan yang Sering Diajukan

### Q1: Bisakah saya menggunakan Aspose.CAD untuk Java dengan format file CAD lainnya?

A1: Ya, Aspose.CAD mendukung berbagai format CAD, termasuk DWG, DXF, DWF, dan lainnya. Periksa dokumentasi [di sini](https://reference.aspose.com/cad/java/) untuk daftar lengkap.

### Q2: Apakah ada versi percobaan gratis untuk Aspose.CAD untuk Java?

A2: Ya, Anda dapat menjelajahi fitur Aspose.CAD dengan versi percobaan gratis [di sini](https://releases.aspose.com/).

### Q3: Bagaimana cara mendapatkan dukungan untuk Aspose.CAD untuk Java?

A3: Kunjungi forum Aspose.CAD [di sini](https://forum.aspose.com/c/cad/19) untuk dukungan komunitas. Untuk dukungan premium, pertimbangkan membeli lisensi [di sini](https://purchase.aspose.com/buy).

### Q4: Apa perbedaan antara skala tata letak otomatis dan manual?

A4: Skala tata letak otomatis menyesuaikan ukuran tata letak berdasarkan dimensi halaman yang ditentukan, sementara skala manual memungkinkan Anda mengatur nilai skala khusus.

### Q5: Bisakah saya menyesuaikan tampilan file PDF yang diekspor?

A5: Ya, Anda dapat menyesuaikan opsi grafis dalam kode untuk mengontrol kualitas dan tampilan PDF yang diekspor.

### Q6: Apakah Aspose.CAD mendukung konversi **dwg to pdf java** secara langsung?

A6: Tentu saja. Opsi rasterisasi dan PDF yang sama bekerja untuk file DWG, memungkinkan konversi **dwg to pdf java** yang mulus.

### Q7: Apakah ada cara untuk **generate pdf from cad** tanpa meraster ke bitmap?

A7: Dengan mengatur `rasterizationOptions.setContentAsBitmap(false)`, Anda dapat mempertahankan data vektor bila memungkinkan, menghasilkan PDF berbasis vektor yang sesungguhnya.

**Terakhir Diperbarui:** 2025-12-21  
**Diuji Dengan:** Aspose.CAD for Java 24.10  
**Penulis:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}