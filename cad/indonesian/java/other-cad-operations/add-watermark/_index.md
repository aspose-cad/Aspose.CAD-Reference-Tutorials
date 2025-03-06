---
title: Tambahkan Tanda Air ke Gambar CAD - Aspose.CAD untuk Tutorial Java
linktitle: Tambahkan Tanda Air
second_title: Aspose.CAD Java API
description: Sempurnakan gambar CAD Anda dengan tanda air yang dipersonalisasi menggunakan Aspose.CAD untuk Java. Ikuti panduan langkah demi langkah kami untuk integrasi yang lancar.
weight: 12
url: /id/java/other-cad-operations/add-watermark/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Tambahkan Tanda Air ke Gambar CAD - Aspose.CAD untuk Tutorial Java

## Perkenalan

Selamat datang di panduan komprehensif tentang menambahkan tanda air ke gambar CAD menggunakan Aspose.CAD untuk Java. Dalam tutorial ini, Anda akan mempelajari cara mengintegrasikan tanda air secara efisien, menyempurnakan dokumen CAD Anda dengan pesan atau pencitraan merek yang dipersonalisasi. Aspose.CAD untuk Java menyediakan serangkaian fitur canggih, membuat proses penambahan tanda air menjadi mudah.

## Prasyarat

Sebelum kita mendalami tutorialnya, pastikan Anda memiliki prasyarat berikut:

-  Aspose.CAD untuk Java: Pastikan Anda telah menginstal perpustakaan Aspose.CAD di lingkungan Java Anda. Anda dapat mengunduhnya[Di Sini](https://releases.aspose.com/cad/java/).
- Java Development Kit (JDK): Pastikan Anda menginstal JDK versi terbaru di sistem Anda.

## Paket Impor

Di proyek Java Anda, impor paket Aspose.CAD yang diperlukan untuk memulai:

```java
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.Cad3DPoint;
import com.aspose.cad.fileformats.cad.cadobjects.CadMText;
import com.aspose.cad.fileformats.cad.cadobjects.CadText;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Langkah 1: Tambahkan MTEXT Baru

```java
//tambahkan MTEXT baru
CadMText watermark = new CadMText();
watermark.setText("Watermark message");
watermark.setInitialTextHeight(40);
watermark.setInsertionPoint(new Cad3DPoint(300, 40));
watermark.setLayerName("0");
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(watermark);
```

## Langkah 2: Tambahkan Entitas Sederhana seperti Teks

Anda juga dapat menambahkan entitas yang lebih jelas seperti teks:

```java
// atau tambahkan entitas yang lebih sederhana seperti Teks
CadText text = new CadText();
text.setDefaultValue("Watermark text");
text.setTextHeight(40);
text.setFirstAlignment(new Cad3DPoint(300, 40));
text.setLayerName("0") ;
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(text);
```

## Langkah 3: Ekspor ke PDF

Ekspor gambar CAD dengan tanda air tambahan ke file PDF:

```java
// ekspor ke pdf
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
rasterizationOptions.setLayouts(new String[]{"Model"});
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
cadImage.save(dataDir + "AddWatermark_out.pdf", pdfOptions);

```

## Kesimpulan

Selamat! Anda telah berhasil menambahkan tanda air ke gambar CAD Anda menggunakan Aspose.CAD untuk Java. Proses sederhana namun kuat ini memungkinkan Anda mempersonalisasi desain atau melindunginya dengan branding.

## FAQ

### Q1: Apakah Aspose.CAD kompatibel dengan semua format file CAD?

A1: Aspose.CAD mendukung berbagai format CAD, termasuk DWG, DXF, DWT, dan DWF.

### Q2: Dapatkah saya menyesuaikan tampilan teks tanda air?

A2: Ya, Anda memiliki kendali penuh atas tampilan tanda air, termasuk ukuran teks, warna, dan posisi.

### Q3: Apakah ada versi uji coba yang tersedia untuk Aspose.CAD untuk Java?

 A3: Ya, Anda dapat mendownload versi trial[Di Sini](https://releases.aspose.com/).

### Q4: Bagaimana saya bisa mendapatkan dukungan untuk Aspose.CAD?

 A4: Kunjungi[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19) untuk dukungan masyarakat.

### Q5: Di mana saya dapat menemukan dokumentasi lengkap Aspose.CAD untuk Java?

 A5: Lihat[dokumentasi](https://reference.aspose.com/cad/java/) untuk informasi rinci.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
