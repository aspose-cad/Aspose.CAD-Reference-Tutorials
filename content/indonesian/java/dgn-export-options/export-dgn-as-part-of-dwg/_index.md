---
title: Ekspor DGN ke DWG dengan Aspose.CAD untuk Java
linktitle: Ekspor DGN sebagai Bagian dari DWG
second_title: Aspose.CAD Java API
description: Jelajahi cara mengekspor DGN sebagai bagian dari DWG menggunakan Aspose.CAD untuk Java. Ikuti panduan langkah demi langkah kami untuk manipulasi file CAD yang efisien.
type: docs
weight: 10
url: /id/java/dgn-export-options/export-dgn-as-part-of-dwg/
---
## Perkenalan

Dalam tutorial ini, kita akan mempelajari cara menggunakan Aspose.CAD untuk Java untuk mengekspor file DGN (MicroStation Design) sebagai bagian dari file DWG (AutoCAD Drawing). Aspose.CAD adalah perpustakaan canggih yang menyediakan fungsionalitas komprehensif untuk bekerja dengan format file CAD. Panduan langkah demi langkah ini akan membantu Anda memahami proses mengekspor DGN sebagai bagian dari DWG menggunakan Java.

## Prasyarat

Sebelum kita mendalami tutorialnya, pastikan Anda memiliki prasyarat berikut:
1. Perpustakaan Aspose.CAD: Unduh dan instal perpustakaan Aspose.CAD untuk Java. Anda dapat menemukan perpustakaan[Di Sini](https://releases.aspose.com/cad/java/).
2. Java Development Kit (JDK): Pastikan Anda telah menginstal Java di sistem Anda.
3. Lingkungan Pengembangan Terintegrasi (IDE): Pilih IDE Java seperti Eclipse atau IntelliJ untuk pengalaman pengembangan yang lebih lancar.

## Paket Impor

Di proyek Java Anda, impor paket Aspose.CAD yang diperlukan untuk mengaktifkan manipulasi file CAD. Berikut ini contohnya:

```java
import com.aspose.cad;
import com.aspose.cad.imageoptions;
import com.aspose.cad.fileformats.cad.cadconsts;
import com.aspose.cad.fileformats.cad;
import com.aspose.cad.fileformats.cad.cadobjects;
```

## Langkah 1: Tetapkan Jalur File

 Tentukan jalur file input dan output untuk file DWG. Perbarui`dataDir`, `fileName` , Dan`outPath` variabel yang sesuai.

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "BlockRefDgn.dwg";
String outPath = dataDir + "BlockRefDgn.dwg.pdf";
```

## Langkah 2: Buat Instance PdfOptions

 Buat sebuah instance dari`PdfOptions` kelas, saat kami mengekspor file DWG ke format PDF.

```java
PdfOptions exportOptions = new PdfOptions();
```

## Langkah 3: Muat File DWG

 Muat file DWG yang ada sebagai gambar dan konversikan menjadi`CadImage` jenis.

```java
CadImage cadImage = (CadImage) Image.load(fileName);
```

## Langkah 4: Iterasi Melalui Entitas

Telusuri setiap entitas di dalam file DWG dan periksa apakah itu definisi gambar. Jika ya, ambil referensi eksternal ke objek tersebut.

```java
for (CadBaseEntity baseEntity : cadImage.getEntities()) {
    if (baseEntity.getTypeName() == CadEntityTypeName.DGNUNDERLAY) {
        CadDgnUnderlay dgnFile = (CadDgnUnderlay)baseEntity;
        System.out.println(dgnFile.getUnderlayPath());
    }
}
```

## Langkah 5: Tentukan Opsi Rasterisasi

 Tentukan pengaturan untuk`CadRasterizationOptions`objek, termasuk lebar halaman, tinggi, tata letak, dan warna latar belakang.

```java
CadRasterizationOptions vectorRasterizationOptions = new CadRasterizationOptions();
vectorRasterizationOptions.setPageWidth(1600);
vectorRasterizationOptions.setPageHeight(1600);
vectorRasterizationOptions.setLayouts(new String[] { "Model" });
vectorRasterizationOptions.setAutomaticLayoutsScaling(false);
vectorRasterizationOptions.setNoScaling(true);
vectorRasterizationOptions.setBackgroundColor(Color.getBlack());
vectorRasterizationOptions.setDrawType(CadDrawTypeMode.UseObjectColor);
```

## Langkah 6: Tetapkan Opsi Rasterisasi Vektor

Atur opsi rasterisasi vektor untuk ekspor.

```java
exportOptions.setVectorRasterizationOptions(vectorRasterizationOptions);
```

## Langkah 7: Ekspor DWG ke PDF

 Terakhir, ekspor DWG ke PDF dengan memanggil`save` metode.

```java
cadImage.save(outPath, exportOptions);
```

## Kesimpulan

Selamat! Anda telah berhasil mempelajari cara mengekspor file DGN sebagai bagian dari file DWG menggunakan Aspose.CAD untuk Java. Pustaka canggih ini menyediakan kemampuan ekstensif untuk bekerja dengan file CAD, menjadikan tugas manipulasi file CAD Anda efisien dan mudah.

## FAQ

### Q1: Di mana saya dapat menemukan dokumentasi Aspose.CAD untuk Java?

 A1: Dokumentasi dapat ditemukan[Di Sini](https://reference.aspose.com/cad/java/).

### Q2: Bagaimana cara mengunduh perpustakaan Aspose.CAD untuk Java?

 A2: Anda dapat mengunduh perpustakaan dari[Link ini](https://releases.aspose.com/cad/java/).

### Q3: Apakah tersedia uji coba gratis untuk Aspose.CAD untuk Java?

 A3: Ya, Anda dapat menemukan uji coba gratis[Di Sini](https://releases.aspose.com/).

### Q4: Di mana saya bisa mendapatkan lisensi sementara Aspose.CAD untuk Java?

 A4: Dapatkan lisensi sementara[Di Sini](https://purchase.aspose.com/temporary-license/).

### Q5: Butuh bantuan atau punya pertanyaan?

 A5: Kunjungi forum dukungan komunitas Aspose.CAD[Di Sini](https://forum.aspose.com/c/cad/19).