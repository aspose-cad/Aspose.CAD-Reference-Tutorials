---
title: Menyesuaikan Ukuran Gambar CAD Menggunakan Tipe Unit dengan Aspose.CAD untuk Java
linktitle: Menyesuaikan Ukuran Gambar CAD Menggunakan Tipe Unit
second_title: Aspose.CAD Java API
description: Jelajahi kekuatan Aspose.CAD untuk Java dalam menyesuaikan ukuran gambar CAD dengan mudah. Ikuti panduan langkah demi langkah kami untuk presisi dan kemampuan beradaptasi.
weight: 14
url: /id/java/cad-file-manipulation/adjusting-cad-drawing-size-using-unit-type/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Menyesuaikan Ukuran Gambar CAD Menggunakan Tipe Unit dengan Aspose.CAD untuk Java

## Perkenalan

Dalam bidang Computer-Aided Design (CAD) yang terus berkembang, presisi dan kemampuan beradaptasi adalah hal yang terpenting. Salah satu persyaratan umum adalah menyesuaikan ukuran gambar CAD berdasarkan jenis unit tertentu. Aspose.CAD untuk Java muncul sebagai sekutu yang kuat, memberikan kemampuan tanpa batas untuk memanipulasi file CAD secara terprogram.

## Prasyarat

Sebelum masuk ke tutorial, pastikan Anda memiliki prasyarat berikut:

- Lingkungan Pengembangan Java: Pastikan Anda memiliki lingkungan pengembangan Java yang berfungsi pada mesin Anda.

-  Aspose.CAD untuk Perpustakaan Java: Unduh dan integrasikan perpustakaan Aspose.CAD ke dalam proyek Java Anda. Anda dapat memperoleh perpustakaan[Di Sini](https://releases.aspose.com/cad/java/).

## Impor Namespace

Dalam kode Java Anda, sertakan namespace yang diperlukan untuk mengakses fungsionalitas Aspose.CAD. Tambahkan impor berikut:

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

Sekarang, mari kita uraikan proses penyesuaian ukuran gambar CAD menggunakan tipe unit menjadi langkah-langkah yang dapat dikelola:

## Langkah 1: Tentukan Direktori Data

```java
String dataDir = "Your Document Directory" + "CADConversion/";
```

Tetapkan jalur untuk direktori tempat file CAD Anda berada.

## Langkah 2: Muat Gambar CAD

```java
String sourceFilePath = dataDir + "sample.dwg";
Image image = Image.load(sourceFilePath);
```

 Muat gambar CAD menggunakan Aspose.CAD`Image` kelas.

## Langkah 3: Buat Opsi BMP

```java
BmpOptions bmpOptions = new BmpOptions();
```

 Buat instance`BmpOptions` kelas untuk mengekspor tata letak CAD ke format BMP.

## Langkah 4: Konfigurasikan Opsi Rasterisasi

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
bmpOptions.setVectorRasterizationOptions(cadRasterizationOptions);
```

 Buat sebuah contoh dari`CadRasterizationOptions` dan mengasosiasikannya dengan`BmpOptions` untuk rasterisasi vektor.

## Langkah 5: Tetapkan Jenis Unit

```java
cadRasterizationOptions.setUnitType(UnitType.Centimeter);
```

Tentukan jenis unit yang diinginkan untuk gambar CAD. Dalam contoh ini, kami telah menetapkannya ke Centimeter.

## Langkah 6: Atur Tata Letak

```java
cadRasterizationOptions.setLayouts(new String[] { "Model" });
```

Tentukan tata letak yang akan dipertimbangkan selama ekspor. Dalam hal ini, kami telah memilih tata letak "Model".

## Langkah 7: Ekspor ke BMP

```java
String outPath = sourceFilePath + ".bmp";
image.save(outPath, bmpOptions);
```

Terakhir, simpan gambar CAD yang dimodifikasi dalam format BMP.

## Kesimpulan

Dengan Aspose.CAD untuk Java, menyesuaikan ukuran gambar CAD menjadi mudah. Tutorial ini telah memandu Anda melalui proses tersebut, menekankan pentingnya setiap langkah dalam mencapai hasil yang tepat.

## FAQ

### Q1: Bisakah saya menggunakan Aspose.CAD untuk Java dengan bahasa pemrograman lain?

A1: Aspose.CAD terutama mendukung Java, tetapi ada versi yang tersedia untuk bahasa lain seperti .NET.

### Q2: Apakah ada opsi lisensi untuk Aspose.CAD?

 A2: Ya, Anda dapat menjelajahi opsi lisensi dan membeli Aspose.CAD[Di Sini](https://purchase.aspose.com/buy).

### Q3: Apakah ada uji coba gratis yang tersedia untuk Aspose.CAD?

 A3: Tentu saja, Anda dapat mengakses uji coba gratis[Di Sini](https://releases.aspose.com/).

### Q4: Bagaimana saya bisa mendapatkan dukungan untuk Aspose.CAD untuk Java?

 A4: Kunjungi forum Aspose.CAD[Di Sini](https://forum.aspose.com/c/cad/19) untuk dukungan komprehensif.

### Q5: Bisakah saya mendapatkan lisensi sementara untuk Aspose.CAD?

 A5: Ya, Anda bisa mendapatkan lisensi sementara[Di Sini](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
