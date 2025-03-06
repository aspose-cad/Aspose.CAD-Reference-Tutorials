---
title: Ekspor ke BMP dengan Aspose.CAD untuk Java
linktitle: Ekspor ke BMP
second_title: Aspose.CAD Java API
description: Jelajahi konversi CAD ke BMP yang lancar dengan Aspose.CAD untuk Java. Ikuti panduan langkah demi langkah kami untuk ekspor yang efisien dan tepat.
weight: 12
url: /id/java/cad-export-options/export-to-bmp/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ekspor ke BMP dengan Aspose.CAD untuk Java

## Perkenalan

Dalam lanskap desain digital yang terus berkembang, kemampuan mengekspor file Computer-Aided Design (CAD) ke berbagai format dengan lancar sangatlah penting. Aspose.CAD untuk Java menonjol sebagai solusi ampuh, menyediakan alat yang dibutuhkan pengembang untuk mengekspor file CAD ke format BMP secara efisien. Tutorial ini akan memandu Anda melalui proses langkah demi langkah, memastikan ekspor lancar dan sukses setiap saat.

## Prasyarat

Sebelum masuk ke tutorial, pastikan Anda memiliki prasyarat berikut:

- Aspose.CAD untuk Perpustakaan Java: Unduh dan instal perpustakaan Aspose.CAD untuk Java dari[Di Sini](https://releases.aspose.com/cad/java/).

- Lingkungan Pengembangan Java: Pastikan Anda telah menyiapkan lingkungan pengembangan Java di sistem Anda.

- Pengetahuan Dasar Java: Biasakan diri Anda dengan konsep dasar pemrograman Java.

## Impor Namespace

Di proyek Java Anda, impor namespace yang diperlukan untuk mengakses fungsionalitas Aspose.CAD:

```java
import com.aspose.cad.Image;
import com.aspose.cad.InterpolationMode;
import com.aspose.cad.SmoothingMode;
import com.aspose.cad.TextRenderingHint;

import com.aspose.cad.imageoptions.BmpOptions;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
//impor com.aspose.cad.imageoptions.TypeOfEntities;
```

## Langkah 1: Tetapkan Jalur Direktori Sumber Daya

Mulailah dengan menentukan jalur ke direktori sumber daya tempat file CAD berada.

```java
String dataDir = "Your Document Directory" + "ExportingCAD/";
```

## Langkah 2: Muat File CAD

 Muat file CAD ke Aspose.CAD`Image` obyek.

```java
String fileName = (dataDir + "site.dwf");
Image image = Image.load(fileName);
```

## Langkah 3: Konfigurasikan Opsi Ekspor BMP

Membuat dan mengonfigurasi opsi ekspor BMP, termasuk pengaturan rasterisasi.

```java
BmpOptions bmpOptions = new BmpOptions();
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
bmpOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## Langkah 4: Tetapkan Parameter Rasterisasi

Tentukan parameter seperti tinggi halaman, lebar halaman, dan tata letak untuk rasterisasi.

```java
rasterizationOptions.setPageHeight(500);
rasterizationOptions.setPageWidth(500);
rasterizationOptions.setLayouts(new String[] { "Model" });
```

## Langkah 5: Ekspor ke BMP

Tentukan jalur keluaran dan simpan file BMP.

```java
String outPath = dataDir + "site.bmp";
image.save(outPath, bmpOptions);
```

Ulangi langkah-langkah ini untuk setiap file CAD yang ingin Anda ekspor ke BMP menggunakan Aspose.CAD untuk Java.

## Kesimpulan

Mengekspor file CAD ke format BMP menjadi mudah dengan Aspose.CAD untuk Java. Dengan mengikuti panduan langkah demi langkah ini, Anda dapat dengan mudah mengintegrasikan fungsi ini ke dalam aplikasi Java Anda, memastikan konversi yang efisien dan tepat.

## FAQ

### Q1: Apakah Aspose.CAD untuk Java cocok untuk pemrosesan batch?

A1: Tentu saja! Aspose.CAD untuk Java mendukung pemrosesan batch, memungkinkan Anda menangani beberapa file CAD secara bersamaan secara efisien.

### Q2: Dapatkah saya menyesuaikan opsi rasterisasi untuk tata letak yang berbeda?

A2: Ya, Anda dapat menyesuaikan opsi rasterisasi seperti dimensi halaman dan tata letak sesuai dengan kebutuhan spesifik Anda.

### Q3: Di mana saya dapat menemukan dukungan tambahan untuk Aspose.CAD untuk Java?

 A3: Kunjungi[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19) untuk dukungan dan diskusi komunitas.

### Q4: Apakah tersedia uji coba gratis?

 A4: Ya, Anda dapat menjelajahi uji coba gratis Aspose.CAD untuk Java[Di Sini](https://releases.aspose.com/).

### Q5: Bagaimana cara mendapatkan lisensi sementara?

 A5: Dapatkan lisensi sementara untuk Aspose.CAD untuk Java[Di Sini](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
