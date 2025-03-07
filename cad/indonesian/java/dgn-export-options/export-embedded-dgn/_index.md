---
title: Ekspor DGN Tersemat ke PDF dengan Aspose.CAD untuk Java
linktitle: Ekspor Tertanam DGN
second_title: Aspose.CAD Java API
description: Jelajahi panduan langkah demi langkah tentang mengekspor file DGN yang disematkan ke PDF menggunakan Aspose.CAD untuk Java. Sempurnakan aplikasi Java Anda dengan manipulasi file CAD yang lancar.
weight: 11
url: /id/java/dgn-export-options/export-embedded-dgn/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ekspor DGN Tersemat ke PDF dengan Aspose.CAD untuk Java

## Perkenalan

Selamat datang di tutorial komprehensif tentang mengekspor file DGN yang disematkan menggunakan Aspose.CAD untuk Java. Aspose.CAD adalah perpustakaan canggih yang memungkinkan pengembang Java bekerja dengan file CAD dengan lancar. Dalam tutorial ini, kami akan memandu Anda melalui proses mengekspor file DGN yang disematkan ke PDF menggunakan petunjuk langkah demi langkah. Baik Anda seorang pengembang berpengalaman atau baru memulai, tutorial ini akan membantu Anda memanfaatkan kemampuan Aspose.CAD untuk menyempurnakan aplikasi Java Anda.

## Prasyarat

Sebelum kita masuk ke tutorialnya, pastikan Anda memiliki prasyarat berikut:
- Lingkungan Pengembangan Java: Pastikan Anda telah menyiapkan lingkungan pengembangan Java di mesin Anda.
-  Aspose.CAD untuk Java: Unduh dan instal Aspose.CAD untuk perpustakaan Java dari[Di Sini](https://releases.aspose.com/cad/java/).

## Paket Impor

Untuk memulai, Anda perlu mengimpor paket yang diperlukan ke proyek Java Anda. Tambahkan pernyataan import berikut ke kode Anda:

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

Sekarang, mari kita pecahkan kode contoh menjadi beberapa langkah:

## Langkah 1: Atur Jalur Input dan Output

Tentukan jalur direktori tempat dokumen Anda berada dan tentukan nama file DWG masukan.

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "BlockRefDgn.dwg";
```

## Langkah 2: Muat File DWG

 Muat file DWG ke dalam file`Image` objek menggunakan Aspose.CAD.

```java
Image objImage = Image.load(fileName);
```

## Langkah 3: Konfigurasikan Opsi Rasterisasi

Konfigurasikan opsi rasterisasi, seperti tata letak untuk disertakan dalam ekspor.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setLayouts(new String[] {"Model"});
```

## Langkah 4: Konfigurasikan Opsi PDF

Siapkan opsi PDF, termasuk opsi rasterisasi vektor.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## Langkah 5: Simpan File PDF

Simpan file PDF dengan opsi yang dikonfigurasi.
```java
objImage.save(dataDir + "BlockRefDgn.pdf", pdfOptions);
```

## Kesimpulan

Selamat! Anda telah berhasil mengekspor file DGN yang disematkan ke PDF menggunakan Aspose.CAD untuk Java. Tutorial ini membahas langkah-langkah penting untuk mengintegrasikan Aspose.CAD ke dalam aplikasi Java Anda untuk manipulasi file CAD yang efisien.

## FAQ

### Q1: Dapatkah saya menggunakan Aspose.CAD untuk Java dalam proyek komersial?

 A1: Ya, Aspose.CAD untuk Java adalah perpustakaan komersial. Anda dapat memperoleh lisensi dari[Di Sini](https://purchase.aspose.com/buy).

### Q2: Apakah tersedia uji coba gratis?

 A2:Ya, Anda dapat mengakses uji coba gratis Aspose.CAD untuk Java[Di Sini](https://releases.aspose.com/).

### Q3: Bagaimana saya bisa mendapatkan dukungan untuk Aspose.CAD untuk Java?

A3: Anda dapat mencari dukungan dari komunitas Aspose.CAD di[forum](https://forum.aspose.com/c/cad/19).

### Q4: Bagaimana jika saya memerlukan lisensi sementara?

 A4: Anda bisa mendapatkan lisensi sementara[Di Sini](https://purchase.aspose.com/temporary-license/).

### Q5: Di mana saya dapat menemukan dokumentasinya?

 A5: Dokumentasi tersedia[Di Sini](https://reference.aspose.com/cad/java/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
