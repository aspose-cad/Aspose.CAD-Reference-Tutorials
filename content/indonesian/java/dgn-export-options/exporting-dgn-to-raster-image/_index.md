---
title: Konversi Java DGN ke JPEG dengan Tutorial Aspose.CAD
linktitle: Mengekspor DGN dalam Format AutoCAD ke Format Gambar Raster
second_title: Aspose.CAD Java API
description: Pelajari cara mengekspor file DGN ke gambar JPEG di Java menggunakan Aspose.CAD. Tutorial langkah demi langkah ini memandu Anda melalui proses dengan mudah.
type: docs
weight: 13
url: /id/java/dgn-export-options/exporting-dgn-to-raster-image/
---
## Perkenalan

Selamat datang di tutorial komprehensif tentang mengekspor file DGN (Desain) ke Format Gambar Raster menggunakan Aspose.CAD untuk Java. Aspose.CAD adalah perpustakaan canggih yang memungkinkan pengembang Java bekerja dengan file CAD dengan lancar. Dalam tutorial ini, kami akan memandu Anda melalui proses mengonversi file DGN ke gambar JPEG, memberi Anda petunjuk langkah demi langkah dan contoh kode.

## Prasyarat

Sebelum masuk ke tutorial, pastikan Anda memiliki prasyarat berikut:
1.  Perpustakaan Aspose.CAD: Pastikan Anda telah menginstal perpustakaan Aspose.CAD untuk Java. Anda dapat mengunduhnya[Di Sini](https://releases.aspose.com/cad/java/).
2. Java Development Kit (JDK): Pastikan Anda telah menginstal Java di mesin Anda.
3. Lingkungan Pengembangan Terintegrasi (IDE): Gunakan IDE yang kompatibel dengan Java seperti IntelliJ atau Eclipse.

## Paket Impor

Di proyek Java Anda, impor paket yang diperlukan untuk Aspose.CAD. Tambahkan baris berikut ke kode Anda:

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
```

## Langkah 1: Muat File DGN

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
DgnImage dgnImage = (DgnImage) Image.load(dataDir + "Nikon_D90_Camera.dgn");
```

## Langkah 2: Buat Objek JpegOptions

```java
ImageOptionsBase options = new JpegOptions();
```

## Langkah 3: Tetapkan Opsi Rasterisasi

```java
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(600);
vectorOptions.setPageHeight(400);
vectorOptions.setNoScaling(true);
vectorOptions.setAutomaticLayoutsScaling(false);
options.setVectorRasterizationOptions(vectorOptions);
```

## Langkah 4: Simpan Gambar yang Dikonversi

```java
OutputStream outStream = new FileOutputStream(dataDir + "ExportDGNToRasterImage_Out.jpg");
dgnImage.save(outStream, options);
```

Ulangi langkah-langkah ini untuk file DGN spesifik Anda, sesuaikan jalur file.

## Kesimpulan

Selamat! Anda telah berhasil mempelajari cara mengekspor file DGN ke Format Gambar Raster menggunakan Aspose.CAD untuk Java. Tutorial ini telah membekali Anda dengan pengetahuan untuk memasukkan fungsi ini ke dalam aplikasi Java Anda.

## FAQ

### Q1: Dapatkah saya menggunakan Aspose.CAD untuk Java dengan format file CAD lainnya?

A1: Ya, Aspose.CAD mendukung berbagai format CAD, memberikan solusi serbaguna untuk pengembang Java.

### Q2: Apakah tersedia uji coba gratis untuk Aspose.CAD untuk Java?

 A2: Ya, Anda dapat mengakses uji coba gratis[Di Sini](https://releases.aspose.com/).

### Q3: Di mana saya dapat menemukan dokumentasi Aspose.CAD untuk Java?

 A3: Lihat dokumentasi[Di Sini](https://reference.aspose.com/cad/java/).

### Q4: Bagaimana saya bisa mendapatkan dukungan untuk Aspose.CAD untuk Java?

 A4: Kunjungi forum dukungan[Di Sini](https://forum.aspose.com/c/cad/19).

### Q5: Di mana saya dapat membeli lisensi Aspose.CAD untuk Java?

 A5: Anda dapat membeli lisensi[Di Sini](https://purchase.aspose.com/buy).