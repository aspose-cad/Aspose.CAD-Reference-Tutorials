---
title: Mengatur Latar Belakang dan Warna Gambar di Aspose.CAD untuk .NET
linktitle: Mengatur Latar Belakang dan Warna Gambar
second_title: Aspose.CAD .NET - Format File CAD dan BIM
description: Kuasai Aspose.CAD untuk .NET. Atur latar belakang dan warna gambar dengan mudah. Ikuti panduan langkah demi langkah kami.
weight: 15
url: /id/net/cad-features-and-support/setting-background-and-drawing-colors/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Mengatur Latar Belakang dan Warna Gambar di Aspose.CAD untuk .NET

## Perkenalan

Dalam dunia pengembangan .NET yang dinamis, Aspose.CAD muncul sebagai alat yang ampuh untuk menangani file Computer-Aided Design (CAD). Jika Anda ingin meningkatkan keterampilan Anda dalam memanipulasi gambar CAD, tutorial ini adalah pintu gerbang Anda. Kami akan mempelajari seluk-beluk pengaturan latar belakang dan warna gambar menggunakan Aspose.CAD untuk .NET, memberi Anda panduan langkah demi langkah yang memastikan kejelasan dan efektivitas.

## Prasyarat

Sebelum kita memulai perjalanan ini, pastikan Anda memiliki prasyarat berikut:

- Pemahaman dasar tentang pengembangan .NET.
-  Pemasangan Aspose.CAD untuk .NET. Jika Anda belum melakukannya, Anda dapat mengunduhnya[Di Sini](https://releases.aspose.com/cad/net/).
- Contoh file CAD untuk eksperimen. Anda dapat menemukannya di direktori dokumen Anda.

## Impor Namespace

Di proyek .NET Anda, mulailah dengan mengimpor namespace yang diperlukan:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Langkah 1: Muat File CAD

Mulailah dengan memuat file CAD yang ingin Anda kerjakan menggunakan cuplikan kode berikut:

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

using (Image image = Image.Load(sourceFilePath))
{
    // Kode Anda untuk diproses lebih lanjut ada di sini
}
```

## Langkah 2: Konfigurasikan Opsi Rasterisasi

 Buat sebuah contoh dari`CadRasterizationOptions` dan atur propertinya untuk latar belakang dan pengaturan warna gambar:

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
rasterizationOptions.BackgroundColor = Color.Beige;
rasterizationOptions.DrawType = CadDrawTypeMode.UseDrawColor;
rasterizationOptions.DrawColor = Color.Blue;
```

## Langkah 3: Ekspor ke PDF

 Buat sebuah contoh dari`PdfOptions` dan atur`VectorRasterizationOptions` Properti:

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;

// Ekspor CAD ke PDF
image.Save(MyDir + "result_out.pdf", pdfOptions);
```

## Langkah 4: Ekspor ke TIFF

 Buat sebuah contoh dari`TiffOptions` dan atur`VectorRasterizationOptions` Properti:

```csharp
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.VectorRasterizationOptions = rasterizationOptions;

// Ekspor CAD ke TIFF
image.Save(MyDir + "result_out.tiff", tiffOptions);
```

## Kesimpulan

Selamat! Anda telah berhasil mempelajari cara mengatur warna latar belakang dan gambar di Aspose.CAD untuk .NET. Tutorial ini membekali Anda dengan keterampilan untuk memanipulasi file CAD dengan mudah.

## FAQ

### Q1: Bisakah saya menggunakan Aspose.CAD untuk .NET dengan semua jenis file CAD?

A1: Ya, Aspose.CAD mendukung berbagai format CAD, termasuk DWG, DXF, dan DGN.

### Q2: Apakah uji coba gratis tersedia untuk Aspose.CAD untuk .NET?

 A2: Ya, Anda dapat menjelajahi uji coba gratis[Di Sini](https://releases.aspose.com/).

### Q3: Di mana saya dapat menemukan dokumentasi terperinci untuk Aspose.CAD untuk .NET?

 A3: Lihat dokumentasi[Di Sini](https://reference.aspose.com/cad/net/).

### Q4: Bagaimana saya bisa mendapatkan lisensi sementara untuk Aspose.CAD?

 A4: Lisensi sementara dapat diperoleh[Di Sini](https://purchase.aspose.com/temporary-license/).

### Q5: Butuh bantuan atau ingin terhubung dengan komunitas?

 A5: Kunjungi forum dukungan[Di Sini](https://forum.aspose.com/c/cad/19).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
