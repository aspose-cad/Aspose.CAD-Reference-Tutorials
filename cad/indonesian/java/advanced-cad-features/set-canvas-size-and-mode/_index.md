---
title: Atur Ukuran dan Mode Kanvas
linktitle: Atur Ukuran dan Mode Kanvas
second_title: Aspose.CAD Java API
description: Jelajahi kekuatan Aspose.CAD untuk Java dengan panduan langkah demi langkah kami dalam mengatur ukuran dan mode kanvas. Konversi file CAD ke format PDF dan TIFF dengan mudah.
weight: 16
url: /id/java/advanced-cad-features/set-canvas-size-and-mode/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Atur Ukuran dan Mode Kanvas

## Perkenalan

Apakah Anda ingin memanfaatkan kekuatan Aspose.CAD untuk Java untuk meningkatkan proses konversi CAD Anda? Panduan komprehensif ini akan memandu Anda melalui langkah-langkah mengatur ukuran dan mode kanvas menggunakan Aspose.CAD untuk Java. Baik Anda seorang pengembang berpengalaman atau baru memulai, tutorial ini akan memberi Anda wawasan yang Anda perlukan.

## Prasyarat

Sebelum masuk ke tutorial, pastikan Anda memiliki prasyarat berikut:

-  Aspose.CAD untuk Java: Pastikan Anda telah menginstal perpustakaan Aspose.CAD di lingkungan Java Anda. Anda dapat mengunduhnya[Di Sini](https://releases.aspose.com/cad/java/).

- Direktori Dokumen: Siapkan direktori dokumen untuk menyimpan file CAD Anda. Direktori ini akan direferensikan dalam langkah-langkah tutorial.

Sekarang, mari kita mulai dengan panduan langkah demi langkah.

## Impor Namespace

Pada langkah ini, kami akan mengimpor namespace yang diperlukan untuk memulai proyek Aspose.CAD Anda.
```java
import java.awt.Image;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

## Langkah 1: Impor Kelas Aspose.CAD

```java
// Jalur ke direktori sumber daya.
String dataDir = "Your Document Directory" + "CADConversion/";

String srcFile = dataDir + "conic_pyramid.dxf";
com.aspose.cad.Image objImage = com.aspose.cad.Image.load(srcFile);
```

 Dalam cuplikan ini, kami menyiapkan jalur ke direktori sumber daya dan memuat file DXF menggunakan Aspose.CAD's`Image` kelas.

## Langkah 2: Tetapkan Properti CadRasterizationOptions

```java
// Buat instance CadRasterizationOptions dan atur berbagai propertinya
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);

rasterizationOptions.setAutomaticLayoutsScaling(true);
rasterizationOptions.setNoScaling(true);
```

 Di sini, kita membuat sebuah instance dari`CadRasterizationOptions` dan mengonfigurasi properti seperti lebar halaman, tinggi halaman, dan opsi penskalaan.

## Langkah 3: Buat PdfOptions dan Setel VectorRasterizationOptions

```java
// Buat sebuah instance dari PdfOptions
PdfOptions pdfOptions = new PdfOptions();

// Setel properti VectorRasterizationOptions
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

 Sekarang, kita membuat a`PdfOptions` contoh dan mengaturnya`VectorRasterizationOptions` properti ke yang dikonfigurasi sebelumnya`CadRasterizationOptions`.

## Langkah 4: Ekspor ke PDF

```java
// Ekspor CAD ke PDF
objImage.save(dataDir + "result_out_.pdf", pdfOptions);
```

Terakhir, kami menyimpan gambar CAD ke file PDF menggunakan opsi yang ditentukan.

## Langkah 5: Buat TiffOptions dan Setel VectorRasterizationOptions

```java
// Buat sebuah instance dari TiffOptions
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);

// Setel properti VectorRasterizationOptions
tiffOptions.setVectorRasterizationOptions(rasterizationOptions);
```

Pada langkah ini, kami menyiapkan a`TiffOptions` contoh dan konfigurasikan`VectorRasterizationOptions` Properti.

## Langkah 6: Ekspor ke TIFF

```java
// Ekspor CAD ke TIFF
objImage.save(dataDir + "result_out_.tiff", tiffOptions);
```

Terakhir, kami menyimpan gambar CAD ke file TIFF menggunakan opsi yang ditentukan.

## Kesimpulan

 Selamat! Anda telah berhasil mengatur ukuran dan mode kanvas menggunakan Aspose.CAD untuk Java. Tutorial ini memberikan dasar yang kuat untuk proyek konversi CAD Anda. Jelajahi lebih banyak fitur dan kemungkinan di[Dokumentasi Aspose.CAD](https://reference.aspose.com/cad/java/).

## FAQ

### Q1: Dapatkah saya menggunakan Aspose.CAD untuk Java dengan kerangka kerja Java lainnya?

A1: Ya, Aspose.CAD dirancang untuk berintegrasi secara mulus dengan berbagai kerangka kerja Java.

### Q2: Apakah lisensi sementara tersedia untuk Aspose.CAD?

 A2: Ya, Anda bisa mendapatkan lisensi sementara[Di Sini](https://purchase.aspose.com/temporary-license/).

### Q3: Di mana saya bisa mendapatkan dukungan komunitas untuk Aspose.CAD?

 A3: Kunjungi[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19) untuk dukungan dan diskusi komunitas.

### Q4: Dapatkah saya mencoba Aspose.CAD secara gratis?

 A4: Tentu saja! Dapatkan uji coba gratis[Di Sini](https://releases.aspose.com/).

### Q5: Bagaimana cara membeli Aspose.CAD untuk Java?

 A5: Beli produknya[Di Sini](https://purchase.aspose.com/buy).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
