---
title: Membuat PDF Dinamis dengan Aspose.CAD untuk Java
linktitle: PDF Tunggal dengan Tata Letak Berbeda
second_title: Aspose.CAD Java API
description: Buat PDF menakjubkan dengan beragam tata letak dari gambar CAD menggunakan Aspose.CAD untuk Java. Integrasi yang mudah dan fitur canggih untuk pengembang Java.
weight: 16
url: /id/java/other-cad-operations/single-pdf-different-layouts/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Membuat PDF Dinamis dengan Aspose.CAD untuk Java

## Perkenalan

Selamat datang di dunia Aspose.CAD untuk Java, perpustakaan canggih yang memberdayakan pengembang untuk memanipulasi gambar CAD dengan mudah. Dalam tutorial ini, kita akan mendalami cara membuat satu PDF dengan tata letak berbeda menggunakan Aspose.CAD untuk Java. Baik Anda seorang pengembang berpengalaman atau baru memulai, panduan langkah demi langkah ini akan memandu Anda melalui prosesnya.

## Prasyarat

Sebelum kita memulai perjalanan ini, pastikan Anda memiliki prasyarat berikut:
- Lingkungan Java: Pastikan Anda telah menginstal Java di mesin Anda.
-  Perpustakaan Aspose.CAD: Unduh dan instal perpustakaan Aspose.CAD untuk Java dari[tautan unduhan](https://releases.aspose.com/cad/java/).
- Direktori Dokumen: Siapkan direktori untuk gambar DWG Anda.

## Paket Impor

Di proyek Java Anda, impor paket yang diperlukan:

```java
import com.aspose.cad.Image;
import com.aspose.cad.SizeF;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.VectorRasterizationOptions;
```

## Langkah 1: Muat Gambar CAD

 Mulailah dengan memuat gambar CAD Anda ke a`CadImage` obyek:

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
CadImage cadImage = (CadImage)Image.load(dataDir + "City skyway map.dwg");
```

## Langkah 2: Konfigurasikan Opsi Rasterisasi

Siapkan opsi rasterisasi untuk gambar CAD:

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1000);
rasterizationOptions.setPageHeight(1000);
```

## Langkah 3: Sesuaikan Ukuran Halaman Tata Letak

Tentukan ukuran khusus untuk beberapa tata letak dalam gambar CAD:

```java
rasterizationOptions.getLayoutPageSizes().addItem("ANSI C Plot", new SizeF(500, 1000));
rasterizationOptions.getLayoutPageSizes().addItem("8.5 x 11 Plot", new SizeF(1000, 100));
```

## Langkah 4: Atur Opsi PDF

Konfigurasikan opsi PDF, dengan menggabungkan pengaturan rasterisasi:

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## Langkah 5: Simpan sebagai PDF

Simpan gambar CAD yang diproses sebagai PDF:

```java
cadImage.save(dataDir + "singlePDF_out.pdf", pdfOptions);
```

Selamat! Anda telah berhasil membuat satu PDF dengan tata letak berbeda menggunakan Aspose.CAD untuk Java.

## Kesimpulan

Dalam tutorial ini, kami menjelajahi integrasi Aspose.CAD untuk Java untuk menghasilkan PDF dengan beragam tata letak dari gambar CAD. Fleksibilitas perpustakaan dan fitur-fitur canggih menjadikannya pilihan tepat untuk tugas manipulasi CAD.

## FAQ

### Q1: Bisakah saya menggunakan Aspose.CAD untuk Java dengan perpustakaan Java lainnya?

A1: Ya, Aspose.CAD untuk Java dirancang untuk berintegrasi secara mulus dengan pustaka Java lainnya, menyediakan fungsionalitas yang luas.

### Q2: Apakah ada versi uji coba yang tersedia?

 A2: Tentu saja! Anda dapat mengakses versi uji coba gratis[Di Sini](https://releases.aspose.com/).

### Q3: Di mana saya bisa mendapatkan dukungan tambahan?

 A3: Kunjungi[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19) untuk dukungan dan diskusi komunitas.

### Q4: Bagaimana cara mendapatkan lisensi sementara?

 A4: Anda bisa mendapatkan lisensi sementara[Di Sini](https://purchase.aspose.com/temporary-license/).

### Q5: Dimana saya bisa membeli versi lengkapnya?

A5: Beli versi lengkap Aspose.CAD untuk Java[Di Sini](https://purchase.aspose.com/buy).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
