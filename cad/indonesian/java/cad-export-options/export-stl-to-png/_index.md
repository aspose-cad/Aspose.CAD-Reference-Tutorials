---
title: Ekspor STL ke PNG dengan Aspose.CAD untuk Java
linktitle: Ekspor STL ke PNG
second_title: Aspose.CAD Java API
description: Jelajahi proses mulus mengekspor file STL ke PNG di Java dengan Aspose.CAD. Sederhanakan alur kerja Anda dan tingkatkan proyek Java Anda dengan mudah.
type: docs
weight: 20
url: /id/java/cad-export-options/export-stl-to-png/
---
## Perkenalan

Apakah Anda ingin mengekspor file STL ke PNG menggunakan Java? Aspose.CAD untuk Java adalah solusi yang Anda butuhkan! Dalam tutorial ini, kami akan memandu Anda melalui proses langkah demi langkah. Sebagai penulis SEO yang mahir, saya akan memastikan kontennya tidak hanya informatif tetapi juga dioptimalkan untuk mesin pencari.

## Prasyarat

Sebelum masuk ke tutorial, pastikan Anda memiliki prasyarat berikut:

- Java Development Kit (JDK) diinstal pada mesin Anda.
-  Aspose.CAD untuk perpustakaan Java diunduh. Kamu bisa mendapatkannya[Di Sini](https://releases.aspose.com/cad/java/).
-  Lisensi yang sah atau lisensi sementara dari[Di Sini](https://purchase.aspose.com/temporary-license/).

## Impor Namespace

Di proyek Java Anda, impor namespace yang diperlukan:

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

Sekarang, mari kita bagi contoh ini menjadi beberapa langkah.

## Langkah 1: Siapkan Proyek Anda

Buat proyek Java baru dan tambahkan pustaka Aspose.CAD untuk Java ke dependensi proyek Anda.

## Langkah 2: Tentukan File STL Anda

Tentukan jalur ke file STL Anda. Misalnya:

```java
String dataDir = "Your Document Directory" + "ExportingSTL/";
String fileName = dataDir + "example.stl";
```

## Langkah 3: Muat File STL

 Muat file STL menggunakan`Image.load` metode:

```java
CadImage cadImage = (CadImage)Image.load(fileName);
```

## Langkah 4: Konfigurasikan Opsi Rasterisasi

Siapkan opsi rasterisasi untuk vektorisasi:

```java
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
```

## Langkah 5: Konfigurasikan Opsi PNG

Tentukan opsi untuk ekspor PNG:

```java
PngOptions pngOptions = new PngOptions();
// Batalkan komentar pada baris di bawah ini jika Anda ingin mengatur opsi rasterisasi vektor
// pngOptions.setVectorRasterizationOptions(vectorOptions);
```

## Langkah 6: Simpan sebagai PNG

Simpan gambar CAD sebagai file PNG:

```java
String outPath = dataDir + "galeon.stl.png";
cadImage.save(outPath, pngOptions);
```

Selamat! Anda telah berhasil mengekspor file STL ke PNG menggunakan Aspose.CAD untuk Java.

## Kesimpulan

Dalam tutorial ini, kita mempelajari cara memanfaatkan Aspose.CAD untuk Java untuk mengekspor file STL ke PNG dengan mudah. Pustaka yang kuat ini menyederhanakan tugas-tugas kompleks, menjadikannya aset berharga untuk proyek Java Anda.

## FAQ

### Q1: Apakah Aspose.CAD untuk Java kompatibel dengan semua versi file STL?

A1: Aspose.CAD untuk Java mendukung berbagai versi file STL, memastikan kompatibilitas dengan sebagian besar format umum.

### Q2: Dapatkah saya menggunakan Aspose.CAD untuk Java dalam proyek komersial?

 A2: Ya, Anda bisa. Cukup dapatkan lisensi yang valid dari[Di Sini](https://purchase.aspose.com/buy).

### Q3: Apakah saya memerlukan lisensi sementara untuk uji coba gratis?

 A3: Tidak, lisensi sementara tidak diperlukan untuk uji coba gratis. Anda dapat langsung memulai dengan versi uji coba[Di Sini](https://releases.aspose.com/).

### Q4: Di mana saya dapat menemukan dukungan tambahan atau mengajukan pertanyaan?

 A4: Kunjungi forum Aspose.CAD[Di Sini](https://forum.aspose.com/c/cad/19) untuk dukungan atau pertanyaan apa pun.

### Q5: Apakah tersedia dokumentasi lengkap?

 A5: Ya, dokumentasinya dapat ditemukan[Di Sini](https://reference.aspose.com/cad/java/).