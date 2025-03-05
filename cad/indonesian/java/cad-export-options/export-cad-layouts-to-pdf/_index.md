---
title: Ekspor Tata Letak CAD ke PDF dengan Aspose.CAD untuk Java
linktitle: Ekspor Tata Letak CAD ke PDF
second_title: Aspose.CAD Java API
description: Jelajahi Aspose.CAD untuk Java untuk mengekspor tata letak CAD ke PDF dengan mudah. Efisien, andal, dan ramah pengembang.
type: docs
weight: 11
url: /id/java/cad-export-options/export-cad-layouts-to-pdf/
---
## Perkenalan

Dalam bidang desain berbantuan komputer (CAD) yang terus berkembang, Aspose.CAD untuk Java menonjol sebagai alat yang ampuh untuk memanipulasi dan mengonversi file CAD. Dalam tutorial ini, kami akan memandu Anda melalui proses mengekspor tata letak CAD ke PDF menggunakan Aspose.CAD untuk Java. Baik Anda seorang pengembang berpengalaman atau baru saja terjun ke dunia CAD, panduan langkah demi langkah ini akan membantu Anda memanfaatkan potensi penuh dari perpustakaan Java serbaguna ini.

## Prasyarat

Sebelum kita mendalami tutorialnya, pastikan Anda memiliki prasyarat berikut:

-  Aspose.CAD untuk Java: Pastikan Anda telah menginstal perpustakaan. Anda dapat mengunduhnya dari situs web Aspose[Di Sini](https://releases.aspose.com/cad/java/).

- Lingkungan Pengembangan Java: Pastikan Anda telah menyiapkan lingkungan pengembangan Java di mesin Anda.

Sekarang semuanya sudah siap, mari kita mulai tutorialnya.

## Impor Namespace

Dalam kode Java Anda, mulailah dengan mengimpor namespace yang diperlukan. Impor ini menyediakan akses ke kelas dan metode yang diperlukan untuk bekerja dengan Aspose.CAD untuk Java.

```java
import com.aspose.cad.Image;
import com.aspose.cad.InterpolationMode;
import com.aspose.cad.SmoothingMode;
import com.aspose.cad.TextRenderingHint;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
//impor com.aspose.cad.imageoptions.TypeOfEntities;
```

## Langkah 1: Muat File CAD

 Mulailah dengan memuat file CAD ke aplikasi Java Anda menggunakan`Image.load` metode. Mengganti`"conic_pyramid.dxf"` dengan jalur ke file CAD Anda.

```java
String dataDir = "Your Document Directory" + "ExportingCAD/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image cadImage = Image.load(srcFile);
```

## Langkah 2: Tetapkan Opsi Rasterisasi

 Buat sebuah contoh dari`CadRasterizationOptions` untuk menentukan bagaimana entitas CAD harus dirasterisasi. Sesuaikan parameter seperti lebar halaman, tinggi halaman, dan skala tata letak sesuai dengan kebutuhan Anda.

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

 Buat sebuah contoh dari`PdfOptions` dan mengaitkannya dengan opsi rasterisasi. Selain itu, atur opsi grafik untuk ekspor PDF, seperti mode penghalusan, petunjuk rendering teks, dan mode interpolasi.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
rasterizationOptions.getGraphicsOptions().setSmoothingMode(SmoothingMode.HighQuality);
rasterizationOptions.getGraphicsOptions().setTextRenderingHint(TextRenderingHint.AntiAliasGridFit);
rasterizationOptions.getGraphicsOptions().setInterpolationMode(InterpolationMode.HighQualityBicubic);
```

## Langkah 4: Ekspor ke PDF

 Terakhir, ekspor tata letak CAD ke file PDF menggunakan`save` metode`cadImage` obyek.

```java
cadImage.save(dataDir + "CADLayoutsToPDF_out_.pdf", pdfOptions);
```

Selamat! Anda telah berhasil mengekspor tata letak CAD ke PDF menggunakan Aspose.CAD untuk Java. Jangan ragu untuk menjelajahi fitur dan fungsi tambahan yang ditawarkan oleh Aspose.CAD untuk meningkatkan pengalaman manipulasi file CAD Anda.

## Kesimpulan

Dalam tutorial ini, kita mempelajari proses mengekspor tata letak CAD ke PDF menggunakan Aspose.CAD untuk Java. Dengan fitur-fitur canggih dan API yang mudah digunakan, Aspose.CAD memberdayakan pengembang untuk bekerja secara efisien dengan file CAD dalam aplikasi Java mereka.

## FAQ

### Q1: Dapatkah saya menggunakan Aspose.CAD untuk Java dengan format file CAD lainnya?

 A1: Ya, Aspose.CAD mendukung berbagai format CAD, termasuk DWG, DXF, DWF, dan banyak lagi. Periksa dokumentasinya[Di Sini](https://reference.aspose.com/cad/java/) untuk daftar lengkap.

### Q2: Apakah tersedia uji coba gratis untuk Aspose.CAD untuk Java?

 A2: Ya, Anda dapat menjelajahi fitur Aspose.CAD dengan uji coba gratis[Di Sini](https://releases.aspose.com/).

### Q3: Bagaimana saya bisa mendapatkan dukungan untuk Aspose.CAD untuk Java?

 A3: Kunjungi forum Aspose.CAD[Di Sini](https://forum.aspose.com/c/cad/19) untuk dukungan masyarakat. Untuk dukungan premium, pertimbangkan untuk membeli lisensi[Di Sini](https://purchase.aspose.com/buy).

### Q4: Apa perbedaan antara penskalaan tata letak otomatis dan manual?

A4: Penskalaan tata letak otomatis menyesuaikan ukuran tata letak berdasarkan dimensi halaman yang ditentukan, sedangkan penskalaan manual memungkinkan Anda menyetel nilai penskalaan khusus.

### Q5: Dapatkah saya menyesuaikan tampilan file PDF yang diekspor?

A5: Ya, Anda dapat menyesuaikan opsi grafik dalam kode untuk mengontrol kualitas dan tampilan PDF yang diekspor.