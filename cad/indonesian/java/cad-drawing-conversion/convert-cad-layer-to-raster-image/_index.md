---
title: Konversi Lapisan CAD ke Format Gambar Raster Menggunakan Aspose.CAD untuk Java
linktitle: Konversi Lapisan CAD ke Format Gambar Raster
second_title: Aspose.CAD Java API
description: Pelajari cara mengonversi lapisan CAD menjadi gambar raster dengan mudah menggunakan Aspose.CAD untuk Java. Ikuti panduan langkah demi langkah kami untuk visualisasi dokumen yang lancar.
weight: 11
url: /id/java/cad-drawing-conversion/convert-cad-layer-to-raster-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Konversi Lapisan CAD ke Format Gambar Raster Menggunakan Aspose.CAD untuk Java

## Perkenalan

Dalam bidang Computer-Aided Design (CAD), kemampuan untuk mengkonversi lapisan CAD ke format gambar raster dengan lancar merupakan aspek penting dalam manipulasi dan visualisasi dokumen. Aspose.CAD untuk Java muncul sebagai alat yang ampuh, menawarkan segudang fungsi untuk menyederhanakan proses konversi ini. Panduan langkah demi langkah ini akan memandu Anda melalui prosesnya, memastikan bahwa Anda memanfaatkan potensi penuh Aspose.CAD untuk Java.

## Prasyarat

Sebelum masuk ke tutorial, pastikan Anda memiliki prasyarat berikut:

- Lingkungan Pengembangan Java: Pastikan Anda telah menyiapkan lingkungan pengembangan Java di mesin Anda.

-  Perpustakaan Aspose.CAD: Unduh dan instal perpustakaan Aspose.CAD untuk Java dari[tautan unduhan](https://releases.aspose.com/cad/java/).

## Impor Namespace

Pada langkah ini, kami akan mengimpor namespace yang diperlukan untuk memulai proses.

### Impor Kelas Aspose.CAD

Dalam kode Java Anda, sertakan kelas Aspose.CAD menggunakan pernyataan import berikut:

```java
import com.aspose.cad.Image;


import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
import java.util.ArrayList;
import java.util.Arrays;
import java.util.List;
```

## Konversi Lapisan CAD ke Format Gambar Raster

Sekarang, mari kita bagi tutorial menjadi beberapa langkah untuk memastikan proses konversi yang lancar.

### Langkah 1: Siapkan File CAD

Mulailah dengan menentukan path ke file CAD Anda dan memuatnya ke dalam instance kelas Image.

```java
// Jalur ke direktori sumber daya.
String dataDir = "Your Document Directory" + "CADConversion/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

### Langkah 2: Konfigurasikan Opsi Rasterisasi

Buat instance CadRasterizationOptions untuk menentukan pengaturan rasterisasi.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(500);
rasterizationOptions.setPageHeight(500);
```

### Langkah 3: Tentukan Lapisan CAD

Tambahkan lapisan CAD yang diinginkan ke opsi rasterisasi.

```java
List<String> stringList = new ArrayList<>(Arrays.asList("0"));
rasterizationOptions.setLayers(stringList);
```

### Langkah 4: Atur Opsi JPEG

Buat instance JpegOptions (atau ImageOptions apa pun untuk format raster) dan tautkan ke CadRasterizationOptions.

```java
JpegOptions options = new JpegOptions();
options.setVectorRasterizationOptions(rasterizationOptions);
```

### Langkah 5: Ekspor ke JPEG

Terakhir, ekspor setiap layer ke format JPEG.

```java
image.save(dataDir + "CADLayersToRasterImageFormats_out_.jpg", options);
```

Ulangi langkah-langkah ini untuk lapisan tambahan atau sesuaikan pengaturan sesuai kebutuhan Anda.

## Kesimpulan

Dengan mengikuti panduan komprehensif ini, Anda telah berhasil memanfaatkan kemampuan Aspose.CAD untuk Java untuk mengonversi lapisan CAD ke format gambar raster. Alat ini memberdayakan Anda untuk meningkatkan visualisasi dan manipulasi dokumen dengan mudah.

## FAQ

### Q1: Bisakah saya menggunakan Aspose.CAD untuk Java dengan bahasa pemrograman lain?

A1: Aspose.CAD terutama mendukung Java, tetapi ada versi yang tersedia untuk bahasa lain seperti .NET.

### Q2: Di mana saya bisa mendapatkan dukungan atau bantuan tambahan?

 A2: Untuk pertanyaan atau bantuan apa pun, kunjungi[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19).

### Q3: Apakah tersedia uji coba gratis?

 A3: Ya, Anda dapat menjelajahi Aspose.CAD dengan mendapatkan uji coba gratis dari[Di Sini](https://releases.aspose.com/).

### Q4: Bagaimana cara mendapatkan lisensi sementara untuk Aspose.CAD?

 A4: Dapatkan lisensi sementara dari[Link ini](https://purchase.aspose.com/temporary-license/).

### Q5: Apakah ada persyaratan sistem khusus untuk Aspose.CAD untuk Java?

A5: Pastikan Anda memiliki lingkungan pengembangan Java yang kompatibel; lihat dokumentasi untuk persyaratan rinci.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
