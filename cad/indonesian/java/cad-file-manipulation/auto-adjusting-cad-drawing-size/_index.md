---
title: Menyesuaikan Ukuran Gambar CAD Secara Otomatis Menggunakan Aspose.CAD untuk Java
linktitle: Menyesuaikan Ukuran Gambar CAD Secara Otomatis
second_title: Aspose.CAD Java API
description: Jelajahi proses penyesuaian otomatis ukuran gambar CAD yang mulus di Java menggunakan Aspose.CAD. Ikuti panduan langkah demi langkah kami untuk manipulasi file CAD yang efisien.
weight: 13
url: /id/java/cad-file-manipulation/auto-adjusting-cad-drawing-size/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Menyesuaikan Ukuran Gambar CAD Secara Otomatis Menggunakan Aspose.CAD untuk Java

## Perkenalan

Dalam dunia CAD (Computer-Aided Design), menyesuaikan ukuran gambar adalah persyaratan umum, dan dengan Aspose.CAD untuk Java, prosesnya menjadi lancar. Pustaka canggih ini menyediakan alat komprehensif untuk menangani file CAD dalam aplikasi Java. Dalam tutorial ini, kita akan menjelajahi proses langkah demi langkah penyesuaian otomatis ukuran gambar CAD menggunakan Aspose.CAD.

## Prasyarat

Sebelum masuk ke tutorial, pastikan Anda memiliki prasyarat berikut:

1.  Lingkungan Pengembangan Java: Pastikan Anda telah menginstal Java di mesin Anda. Anda dapat mengunduhnya[Di Sini](https://www.java.com/en/download/).

2.  Perpustakaan Aspose.CAD: Unduh dan instal perpustakaan Aspose.CAD untuk Java dari[Di Sini](https://releases.aspose.com/cad/java/).

3. Contoh File CAD: Sediakan contoh file CAD (misalnya, sample.dwg) di direktori dokumen Anda.

## Impor Namespace

Dalam aplikasi Java Anda, sertakan namespace yang diperlukan untuk memanfaatkan fungsionalitas Aspose.CAD. Berikut ini contohnya:

```java

import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

Sekarang, mari kita uraikan proses penyesuaian otomatis ukuran gambar CAD menjadi langkah-langkah yang dapat dikelola.

## Langkah 1: Muat Gambar CAD

```java
String dataDir = "Your Document Directory" + "CADConversion/";
String sourceFilePath = dataDir + "sample.dwg";
Image objImage = Image.load(sourceFilePath);
```

Langkah ini melibatkan memuat gambar CAD dari jalur file yang ditentukan.

## Langkah 2: Buat BmpOptions

```java
BmpOptions bmpOptions = new BmpOptions();
```

 Buat instance`BmpOptions` kelas, yang akan digunakan untuk mengatur berbagai pilihan format BMP.

## Langkah 3: Buat Opsi CadRasterization

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
bmpOptions.setVectorRasterizationOptions(cadRasterizationOptions);
```

 Buat sebuah contoh dari`CadRasterizationOptions` untuk menyesuaikan pengaturan rasterisasi untuk file CAD.

## Langkah 4: Tetapkan Properti Tata Letak

```java
cadRasterizationOptions.setLayouts(new String[]{"Model"});
```

Tentukan tata letak yang ingin Anda sertakan dalam output. Dalam hal ini, kami menggunakan tata letak "Model".

## Langkah 5: Ekspor ke Format BMP

```java
String outPath = sourceFilePath + ".bmp";
objImage.save(outPath, bmpOptions);
```

Terakhir, simpan gambar CAD yang disesuaikan dalam format BMP ke jalur keluaran yang ditentukan.

Ulangi langkah-langkah ini di aplikasi Java Anda, dan Anda akan berhasil menyesuaikan ukuran gambar CAD secara otomatis menggunakan Aspose.CAD untuk Java.

## Kesimpulan

Dalam tutorial ini, kita telah mempelajari proses penyesuaian otomatis ukuran gambar CAD menggunakan Aspose.CAD untuk Java. Pustaka ini menyederhanakan manipulasi file CAD, memberikan solusi tangguh bagi pengembang.

## FAQ

### Q1: Apakah Aspose.CAD kompatibel dengan format file CAD yang berbeda?

A1: Ya, Aspose.CAD mendukung berbagai format CAD, termasuk DWG, DXF, DGN, dan banyak lagi.

### Q2: Dapatkah saya menggunakan Aspose.CAD untuk proyek komersial?

 A2: Tentu saja! Mengunjungi[Di Sini](https://purchase.aspose.com/buy) untuk mengeksplorasi opsi lisensi.

### Q3: Bagaimana saya bisa mendapatkan lisensi sementara untuk tujuan pengujian?

 A3: Dapatkan lisensi sementara[Di Sini](https://purchase.aspose.com/temporary-license/) untuk pengujian dan evaluasi.

### Q4: Di mana saya dapat menemukan dukungan untuk Aspose.CAD?

 A4: Bergabunglah dengan komunitas Aspose.CAD[forum](https://forum.aspose.com/c/cad/19) untuk bantuan dan diskusi.

### Q5: Apakah tersedia uji coba gratis untuk Aspose.CAD untuk Java?

 A5: Ya, Anda dapat mengakses uji coba gratis[Di Sini](https://releases.aspose.com/) untuk mengeksplorasi kemampuan perpustakaan.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
