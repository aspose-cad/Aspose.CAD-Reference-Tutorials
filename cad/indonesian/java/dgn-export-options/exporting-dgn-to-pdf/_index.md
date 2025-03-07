---
title: Ekspor DGN ke AutoCAD PDF yang mudah dengan Aspose.CAD untuk Java
linktitle: Mengekspor DGN dalam Format AutoCAD ke PDF
second_title: Aspose.CAD Java API
description: Jelajahi panduan langkah demi langkah tentang mengekspor file DGN ke format AutoCAD dalam PDF menggunakan Aspose.CAD untuk Java. Tingkatkan kemampuan penanganan CAD aplikasi Java Anda dengan mudah.
weight: 12
url: /id/java/dgn-export-options/exporting-dgn-to-pdf/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ekspor DGN ke AutoCAD PDF yang mudah dengan Aspose.CAD untuk Java

## Perkenalan

Selamat datang di tutorial komprehensif tentang penggunaan Aspose.CAD untuk Java untuk mengekspor file DGN dalam format AutoCAD ke PDF. Jika Anda ingin meningkatkan kemampuan aplikasi Java Anda dalam menangani file CAD, Aspose.CAD adalah pilihan yang sangat baik. Dalam tutorial ini, kami akan memandu Anda melalui proses mengekspor file DGN langkah demi langkah.


## Prasyarat
Sebelum kita masuk ke tutorialnya, pastikan Anda memiliki prasyarat berikut:
-  Perpustakaan Aspose.CAD: Pastikan Anda telah menginstal perpustakaan Aspose.CAD untuk Java. Anda dapat mengunduhnya[Di Sini](https://releases.aspose.com/cad/java/).
- Direktori Dokumen: Siapkan direktori dokumen tempat file input dan output Anda akan disimpan.

## Paket Impor

Di proyek Java Anda, impor paket yang diperlukan untuk mengakses fungsionalitas Aspose.CAD:

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

Sekarang, mari kita pecahkan kode contoh menjadi beberapa langkah:

## Langkah 1: Tentukan Jalur File

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "Nikon_D90_Camera.dgn";
String outFile  = dataDir + "Nikon_D90_Camera.pdf";
```

Pastikan untuk mengganti "Direktori Dokumen Anda" dengan jalur sebenarnya tempat file Anda berada.

## Langkah 2: Muat Gambar DGN

```java
DgnImage objImage = (DgnImage) Image.load(fileName);
```

Muat file DGN menggunakan Aspose.CAD.

## Langkah 3: Tetapkan Opsi Ekspor PDF

```java
PdfOptions options = new PdfOptions();
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
vectorOptions.setAutomaticLayoutsScaling(true);
vectorOptions.setLayouts(new String[] { "1", "2", "3", "9" }); // Ekspor tampilan tertentu
options.setVectorRasterizationOptions(vectorOptions);
```

Tentukan opsi ekspor PDF, termasuk dimensi halaman dan preferensi tata letak.

## Langkah 4: Simpan File PDF

```java
objImage.save(outFile, options);
```

Simpan file PDF yang diekspor.

Ulangi langkah-langkah ini untuk file DGN tambahan apa pun yang ingin Anda konversi. Selamat! Anda telah berhasil mengekspor file DGN ke format AutoCAD dalam PDF menggunakan Aspose.CAD untuk Java.

## Kesimpulan

Dalam tutorial ini, kita mempelajari cara memanfaatkan Aspose.CAD untuk Java untuk meningkatkan kemampuan penanganan file CAD aplikasi Anda. Dengan langkah-langkah dan contoh kode yang mudah diikuti, kini Anda dapat mengekspor file DGN ke format AutoCAD dalam PDF dengan lancar.

## FAQ

### Q1: Apakah Aspose.CAD kompatibel dengan semua format file CAD?

A1: Ya, Aspose.CAD mendukung berbagai format CAD, memastikan keserbagunaan dalam menangani berbagai jenis file.

### Q2: Dapatkah saya menyesuaikan pengaturan ekspor PDF?

A2: Tentu saja. Seperti yang ditunjukkan dalam tutorial, Anda dapat menyesuaikan opsi seperti dimensi halaman dan tata letak agar sesuai dengan kebutuhan Anda.

### Q3: Di mana saya bisa mendapatkan dukungan atau bantuan tambahan?

 A3: Kunjungi[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19) untuk dukungan dan diskusi komunitas.

### Q4: Apakah tersedia uji coba gratis?

 A4: Ya, Anda dapat mengakses uji coba gratis[Di Sini](https://releases.aspose.com/).

### Q5: Bagaimana cara mendapatkan lisensi sementara?

 A5: Dapatkan lisensi sementara[Di Sini](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
