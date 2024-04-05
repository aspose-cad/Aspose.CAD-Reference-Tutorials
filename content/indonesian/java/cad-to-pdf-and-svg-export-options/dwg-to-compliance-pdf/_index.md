---
title: DWG untuk Kepatuhan PDF Menggunakan Aspose.CAD untuk Java
linktitle: DWG ke PDF Kepatuhan
second_title: Aspose.CAD Java API
description: Konversi gambar DWG dengan mudah ke file yang sesuai dengan PDF/A1a dan PDF/A1b menggunakan Aspose.CAD untuk Java. Sederhanakan alur kerja Anda dengan presisi dan mudah.
type: docs
weight: 11
url: /id/java/cad-to-pdf-and-svg-export-options/dwg-to-compliance-pdf/
---
## Perkenalan

Dalam dunia desain digital yang terus berkembang, kebutuhan untuk mengonversi gambar DWG ke format PDF yang sesuai sangat penting untuk kolaborasi yang lancar dan dokumentasi standar. Aspose.CAD untuk Java muncul sebagai alat yang ampuh, menawarkan efisiensi dan presisi dalam proses ini. Dalam tutorial ini, kita akan mempelajari cara memanfaatkan Aspose.CAD untuk Java untuk dengan mudah mengonversi file DWG ke PDF yang sesuai, memastikan kepatuhan terhadap standar PDF/A1a dan PDF/A1b.

## Prasyarat

Sebelum masuk ke tutorial, pastikan Anda memiliki prasyarat berikut:

- Lingkungan Pengembangan Java: Pastikan Anda memiliki lingkungan pengembangan Java yang berfungsi di sistem Anda.
-  Perpustakaan Aspose.CAD: Unduh dan instal perpustakaan Aspose.CAD untuk Java dari[tautan unduhan](https://releases.aspose.com/cad/java/).
- Direktori Dokumen: Buat direktori untuk menyimpan gambar DWG Anda.

## Impor Namespace

Di proyek Java Anda, impor namespace yang diperlukan untuk mengakses fungsionalitas Aspose.CAD. Tambahkan baris berikut di awal file Java Anda:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfCompliance;
import com.aspose.cad.imageoptions.PdfDocumentOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Langkah 1: Atur Direktori Sumber Daya

Tentukan jalur ke direktori sumber daya Anda tempat gambar DWG disimpan.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

## Langkah 2: Muat File DWG

Muat file DWG menggunakan perpustakaan Aspose.CAD.

```java
String srcFile = dataDir + "Bottom_plate.dwg";
Image objImage = Image.load(srcFile);
```

## Langkah 3: Buat Opsi PDF

Buat instance PdfOptions dan atur opsi rasterisasi vektor.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(new CadRasterizationOptions());
```

## Langkah 4: Tetapkan Opsi Inti PDF

Atur opsi inti PDF, tentukan standar kepatuhan (PDF/A1a atau PDF/A1b).

```java
pdfOptions.setCorePdfOptions(new PdfDocumentOptions());
pdfOptions.getCorePdfOptions().setCompliance(PdfCompliance.PdfA1a);
```

## Langkah 5: Simpan PDF dengan Kepatuhan A1a

Simpan file PDF dengan kepatuhan A1a.

```java
objImage.save(dataDir + "Saved1.pdf", pdfOptions);
```

## Langkah 6: Ubah Kepatuhan ke A1b

Ubah kepatuhan ke PDF/A1b dan simpan PDF.

```java
pdfOptions.getCorePdfOptions().setCompliance(PdfCompliance.PdfA1b);
objImage.save(dataDir + "Saved.pdf", pdfOptions);
```

Ulangi langkah-langkah ini untuk setiap file DWG yang ingin Anda konversi.

## Kesimpulan

Kesimpulannya, Aspose.CAD untuk Java memberikan solusi tangguh untuk mengonversi file DWG menjadi PDF yang sesuai. Dengan mengikuti panduan langkah demi langkah ini, Anda dapat menyederhanakan proses konversi dan memastikan bahwa dokumen Anda mematuhi standar industri.

## FAQ

### Q1: Apakah Aspose.CAD kompatibel dengan semua versi file DWG?

 A1: Aspose.CAD mendukung berbagai versi file DWG, termasuk yang terbaru. Mengacu kepada[dokumentasi](https://reference.aspose.com/cad/java/) untuk informasi kompatibilitas terperinci.

### Q2: Dapatkah saya menyesuaikan pengaturan keluaran PDF menggunakan Aspose.CAD?

A2: Tentu saja! Aspose.CAD menawarkan berbagai opsi penyesuaian, memungkinkan Anda menyesuaikan keluaran PDF dengan kebutuhan spesifik Anda.

### Q3: Apakah lisensi sementara tersedia untuk Aspose.CAD?

 A3: Ya, Anda bisa mendapatkan lisensi sementara untuk tujuan pengujian dari[Link ini](https://purchase.aspose.com/temporary-license/).

### Q4: Di mana saya dapat mencari dukungan atau berinteraksi dengan komunitas untuk Aspose.CAD?

 A4: Kunjungi[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19) untuk dukungan dan diskusi komunitas.

### Q5: Dapatkah saya mencoba Aspose.CAD secara gratis sebelum melakukan pembelian?

 A5: Tentu saja! Unduh versi uji coba gratis dari[Di Sini](https://releases.aspose.com/) untuk mengeksplorasi kemampuan sebelum mengambil keputusan.