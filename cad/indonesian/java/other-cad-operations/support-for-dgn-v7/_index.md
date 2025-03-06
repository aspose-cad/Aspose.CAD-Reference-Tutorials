---
title: Panduan Konversi DGN ke PDF - Aspose.CAD untuk Java
linktitle: Dukungan untuk DGN V7
second_title: Aspose.CAD Java API
description: Konversi file DGN ke PDF dengan mudah menggunakan Aspose.CAD untuk Java. Ikuti panduan langkah demi langkah kami untuk integrasi yang lancar dan alur kerja yang efisien.
weight: 11
url: /id/java/other-cad-operations/support-for-dgn-v7/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Panduan Konversi DGN ke PDF - Aspose.CAD untuk Java

## Perkenalan

Dalam dunia CAD (Computer-Aided Design) yang dinamis, konversi file DGN (Desain) yang efisien ke PDF (Portable Document Format) merupakan persyaratan penting. Aspose.CAD untuk Java muncul sebagai solusi canggih, menawarkan integrasi tanpa batas dan kemampuan yang tangguh. Panduan langkah demi langkah ini bertujuan memandu Anda melalui proses mengekspor file DGN ke PDF menggunakan Aspose.CAD untuk Java, memastikan alur kerja yang lancar dan efisien.

## Prasyarat

Sebelum masuk ke tutorial, pastikan Anda memiliki prasyarat berikut:
-  Aspose.CAD untuk Java Library: Unduh dan instal perpustakaan dari[Halaman Unduh Aspose.CAD untuk Java](https://releases.aspose.com/cad/java/).
- Lingkungan Pengembangan Java: Pastikan Anda telah menyiapkan lingkungan pengembangan Java di mesin Anda.

## Paket Impor

Mulailah dengan mengimpor paket yang diperlukan ke proyek Java Anda:

## Langkah 1: Impor Paket yang Diperlukan

Di proyek Java Anda, impor paket yang diperlukan untuk Aspose.CAD untuk Java.
```java
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.cad.CadRasterizationOptions;
import com.aspose.cad.fileformats.cad.cadobjects.DgnImage;
import com.aspose.cad.imageoptions.PdfOptions;
import java.awt.Color;
```

## Langkah 2: Tetapkan Jalur File

Tentukan jalur untuk file DGN masukan Anda dan file PDF keluaran.

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "Nikon_D90_Camera.dgn";
String outFile  = dataDir + "Nikon_D90_Camera.pdf";
```

## Langkah 3: Muat Gambar DGN

Muat gambar DGN menggunakan perpustakaan Aspose.CAD.

```java
DgnImage objImage = (DgnImage)Image.load(fileName);
```

## Langkah 4: Konfigurasikan Opsi Ekspor PDF

Siapkan opsi untuk mengekspor ke PDF, termasuk dimensi halaman, penskalaan tata letak otomatis, warna latar belakang, dan tata letak spesifik yang akan diekspor.

```java
PdfOptions options = new PdfOptions();
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
vectorOptions.setAutomaticLayoutsScaling(true);
vectorOptions.setBackgroundColor(Color.getBlack());
vectorOptions.setLayouts(new String[] { "1", "2", "3", "9" }); //hanya mengekspor 4 (1,2,3 dan 9) tampilan
options.setVectorRasterizationOptions(vectorOptions);
```

## Langkah 5: Simpan File PDF

Simpan gambar DGN sebagai file PDF dengan opsi yang ditentukan.

```java
objImage.save(outFile, options);
```

Ulangi langkah-langkah ini untuk file DGN yang berbeda, sesuaikan jalur dan opsi file sesuai kebutuhan.

## Kesimpulan

Dengan Aspose.CAD untuk Java, mengonversi file DGN ke PDF menjadi proses yang mudah. Panduan ini membekali Anda dengan pengetahuan untuk mengintegrasikan perpustakaan ke dalam proyek Java Anda dengan lancar, memfasilitasi konversi file CAD yang efisien.

## FAQ

### Q1: Dapatkah saya menggunakan Aspose.CAD untuk Java dengan format file CAD lainnya?

A1: Ya, Aspose.CAD mendukung berbagai format CAD, menyediakan fungsionalitas serbaguna selain konversi DGN ke PDF.

### Q2: Apakah lisensi sementara tersedia untuk Aspose.CAD untuk Java?

 A2: Ya, Anda bisa mendapatkan lisensi sementara[Di Sini](https://purchase.aspose.com/temporary-license/) untuk tujuan pengujian.

### Q3: Bagaimana cara mencari dukungan atau mengajukan pertanyaan tentang Aspose.CAD untuk Java?

 A3: Kunjungi[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19)untuk berhubungan dengan masyarakat dan mencari bantuan.

### Q4: Tata letak apa yang dapat saya ekspor saat mengonversi DGN ke PDF?

 A4: Anda dapat menentukan tata letak yang akan diekspor dengan menyesuaikan`setLayouts` array dalam kode.

### Q5: Di mana saya dapat menemukan dokumentasi komprehensif untuk Aspose.CAD untuk Java?

 A5: Lihat[Aspose.CAD untuk dokumentasi Java](https://reference.aspose.com/cad/java/) untuk informasi rinci.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
