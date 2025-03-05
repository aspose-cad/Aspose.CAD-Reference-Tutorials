---
title: Ekspor DWG ke PDF atau Raster Menggunakan Aspose.CAD untuk Java
linktitle: Ekspor DWG ke PDF atau Raster
second_title: Aspose.CAD Java API
description: Jelajahi proses mulus mengekspor file DWG ke PDF atau gambar raster di Java menggunakan Aspose.CAD. Panduan langkah demi langkah ini memastikan presisi dan efisiensi.
type: docs
weight: 13
url: /id/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/
---
## Perkenalan

Dalam dunia desain berbantuan komputer (CAD) yang dinamis, penanganan gambar yang efisien sangatlah penting. Aspose.CAD untuk Java memberikan solusi ampuh untuk mengekspor file DWG ke PDF atau gambar raster. Tutorial ini akan memandu Anda melalui proses tersebut, memastikan Anda memanfaatkan potensi penuh Aspose.CAD untuk Java.

## Prasyarat

Sebelum masuk ke tutorial, pastikan Anda memiliki hal berikut:

- Pemahaman dasar pemrograman Java.
-  Aspose.CAD untuk perpustakaan Java diinstal. Jika tidak, unduh[Di Sini](https://releases.aspose.com/cad/java/).
- File DWG untuk tujuan pengujian. Anda dapat menggunakan file "Bottom_plate.dwg" yang disediakan.

## Impor Namespace

Di proyek Java Anda, impor namespace yang diperlukan untuk memulai proses:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.UnitType;
```

## Langkah 1: Muat File DWG

 Mulailah dengan memuat file DWG Anda menggunakan Aspose.CAD`Image` kelas:

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String srcFile = dataDir + "Bottom_plate.dwg";
Image objImage = Image.load(srcFile);
```

## Langkah 2: Tentukan Jenis Unit

Selanjutnya, periksa jenis unit file DWG yang dimuat:

```java
Boolean currentUnitIsMetric = IsMetric(objImage.getUnitType());
int currentUnitCoefficient = objImage.getUnitType();
```

## Langkah 3: Tetapkan Opsi Rasterisasi

Berdasarkan jenis unit, konfigurasikan opsi rasterisasi:

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();

if (currentUnitIsMetric) {
    // Satuan metrik
    double metersCoeff = 1 / 1000.0;
    double scaleFactor = metersCoeff / currentUnitCoefficient;
    rasterizationOptions.setPageWidth((float)(210 * scaleFactor));
    rasterizationOptions.setPageHeight((float)(297 * scaleFactor));
    rasterizationOptions.setUnitType(UnitType.Millimeter);
} else {
    // Unit kekaisaran
    rasterizationOptions.setPageWidth((float)(8.27f / currentUnitCoefficient));
    rasterizationOptions.setPageHeight((float)(11.69f / currentUnitCoefficient));
    rasterizationOptions.setUnitType(UnitType.Inch);
}
```

## Langkah 4: Konfigurasikan Opsi PDF

Siapkan opsi ekspor PDF:

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(new CadRasterizationOptions());
```

## Langkah 5: Simpan sebagai PDF

Terakhir, simpan file DWG sebagai PDF:

```java
objImage.save(dataDir + "Saved.pdf", pdfOptions);
```

Dan itu dia! Anda telah berhasil mengekspor file DWG ke PDF menggunakan Aspose.CAD untuk Java.

## Kesimpulan

Tutorial ini memberikan panduan langkah demi langkah dalam memanfaatkan Aspose.CAD untuk Java untuk mengekspor file DWG ke PDF atau gambar raster. Pustaka ini menyederhanakan prosesnya, memungkinkan Anda menangani gambar CAD secara efisien di aplikasi Java Anda.

## FAQ

### Q1: Dapatkah saya menggunakan Aspose.CAD untuk Java dengan kerangka kerja Java lainnya?

A1: Ya, Aspose.CAD untuk Java terintegrasi secara mulus dengan kerangka kerja Java yang populer.

### Q2: Apakah lisensi sementara tersedia untuk Aspose.CAD untuk Java?

 A2: Ya, Anda bisa mendapatkan lisensi sementara[Di Sini](https://purchase.aspose.com/temporary-license/).

### Q3: Di mana saya dapat menemukan dukungan untuk Aspose.CAD untuk Java?

 A3: Kunjungi[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19) untuk bantuan dari masyarakat.

### Q4: Bagaimana cara membeli lisensi Aspose.CAD untuk Java?

 A4: Anda dapat membeli lisensi[Di Sini](https://purchase.aspose.com/buy).

### Q5: Unit apa yang didukung Aspose.CAD untuk Java?

A5: Aspose.CAD untuk Java mendukung satuan metrik dan imperial.