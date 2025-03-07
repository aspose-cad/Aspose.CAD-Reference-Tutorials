---
title: Ekspor Gambar AutoCAD ke PDF - Aspose.CAD untuk Tutorial Java
linktitle: Ekspor Gambar AutoCAD ke PDF
second_title: Aspose.CAD Java API
description: Ekspor gambar AutoCAD ke PDF dengan mudah menggunakan Aspose.CAD untuk Java. Ikuti panduan langkah demi langkah kami untuk integrasi yang lancar.
weight: 10
url: /id/java/cad-export-options/export-autocad-images-to-pdf/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ekspor Gambar AutoCAD ke PDF - Aspose.CAD untuk Tutorial Java

## Perkenalan

Apakah Anda ingin mengonversi gambar AutoCAD ke PDF dengan lancar menggunakan Java? Tidak perlu mencari lagi! Dalam tutorial ini, kami akan memandu Anda melalui proses menggunakan Aspose.CAD untuk Java, perpustakaan canggih yang menyederhanakan tugas-tugas kompleks. Pada akhirnya, Anda akan memahami cara mengekspor gambar 3D ke PDF dengan mudah.

## Prasyarat

Sebelum masuk ke tutorial, pastikan Anda memiliki prasyarat berikut:

- Lingkungan Pengembangan Java: Pastikan Anda telah menyiapkan lingkungan pengembangan Java di sistem Anda.
-  Aspose.CAD untuk Perpustakaan Java: Unduh dan instal perpustakaan Aspose.CAD untuk Java dari[tautan unduhan](https://releases.aspose.com/cad/java/).
- Direktori Dokumen: Buat direktori untuk menyimpan file CAD Anda agar mudah diakses.

## Impor Namespace

Di proyek Java Anda, impor namespace yang diperlukan untuk memanfaatkan fungsionalitas Aspose.CAD untuk Java:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
//impor com.aspose.cad.imageoptions.TypeOfEntities;
```

Sekarang, mari kita pecahkan kode contoh menjadi beberapa langkah:

## Langkah 1: Tetapkan Jalur Direktori Sumber Daya

```java
String dataDir = "Your Document Directory" + "ExportingCAD/";
```

 Pastikan Anda menggantinya`"Your Document Directory"` dengan jalur ke direktori dokumen Anda.

## Langkah 2: Muat Gambar CAD

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image cadImage = Image.load(srcFile);
```

 Mengganti`"conic_pyramid.dxf"` dengan nama file AutoCAD Anda.

## Langkah 3: Tetapkan Opsi Rasterisasi

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(500);
rasterizationOptions.setPageHeight(500);
// rasterizationOptions.setTypeOfEntities(TypeOfEntities.Entities3D);

rasterizationOptions.setLayouts(new String[] {"Model"});
```

Sesuaikan pengaturan lebar, tinggi, dan tata letak berdasarkan preferensi Anda.

## Langkah 4: Konfigurasikan Opsi PDF

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

Siapkan opsi PDF, termasuk pengaturan rasterisasi vektor.

## Langkah 5: Simpan PDF

```java
cadImage.save(dataDir + "Export3DImagestoPDF_out_.pdf", pdfOptions);
```

Tentukan direktori keluaran dan nama file untuk PDF yang dihasilkan.

## Kesimpulan

Selamat! Anda telah berhasil mempelajari cara mengekspor gambar AutoCAD ke PDF menggunakan Aspose.CAD untuk Java. Panduan ramah pengguna ini menyederhanakan proses yang rumit, sehingga dapat diakses oleh pengembang dari semua tingkat keahlian.

## FAQ

### Q1: Dapatkah saya menggunakan Aspose.CAD untuk Java dengan format file CAD lainnya?

A1: Ya, Aspose.CAD mendukung berbagai format CAD, memberikan fleksibilitas dalam proyek Anda.

### Q2: Bagaimana cara mendapatkan lisensi sementara untuk Aspose.CAD untuk Java?

 A2: Kunjungi[Di Sini](https://purchase.aspose.com/temporary-license/) untuk mendapatkan izin sementara untuk evaluasi.

### Q3: Apakah ada opsi tata letak untuk rasterisasi?

A3: Ya, Anda dapat menyesuaikan tata letak sesuai kebutuhan Anda, sehingga meningkatkan proses rendering.

### Q4: Bisakah saya menyesuaikan ukuran file PDF keluaran?

A4: Tentu saja! Sesuaikan parameter lebar dan tinggi halaman dalam opsi rasterisasi.

### Q5: Di mana saya dapat mencari bantuan atau mendiskusikan masalah terkait Aspose.CAD untuk Java?

 A5: Pergilah ke[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19) untuk dukungan dan diskusi khusus.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
