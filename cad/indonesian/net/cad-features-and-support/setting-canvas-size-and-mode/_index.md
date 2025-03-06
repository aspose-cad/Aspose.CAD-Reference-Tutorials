---
title: Mengatur Ukuran dan Mode Kanvas di Aspose.CAD untuk .NET
linktitle: Mengatur Ukuran dan Mode Kanvas
second_title: Aspose.CAD .NET - Format File CAD dan BIM
description: Jelajahi panduan langkah demi langkah tentang pengaturan ukuran dan mode kanvas di Aspose.CAD untuk .NET. Optimalkan rendering CAD Anda dengan mudah menggunakan tutorial komprehensif ini.
weight: 16
url: /id/net/cad-features-and-support/setting-canvas-size-and-mode/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Mengatur Ukuran dan Mode Kanvas di Aspose.CAD untuk .NET

## Perkenalan

Apakah Anda siap untuk membuka potensi penuh Aspose.CAD untuk .NET dan merevolusi pengalaman rendering CAD Anda? Dalam tutorial langkah demi langkah ini, kita akan mempelajari seluk-beluk pengaturan ukuran dan mode kanvas menggunakan pustaka Aspose.CAD yang canggih. Baik Anda seorang pengembang berpengalaman atau baru memulai, panduan ini akan memandu Anda melalui prosesnya, memastikan Anda memanfaatkan kemampuan Aspose.CAD secara efektif.

## Prasyarat

Sebelum kita mendalami tutorialnya, pastikan Anda memiliki prasyarat berikut:

-  Perpustakaan Aspose.CAD: Unduh dan instal perpustakaan Aspose.CAD dari[Situs web Aspose.CAD](https://releases.aspose.com/cad/net/).

- Lingkungan Pengembangan: Pastikan Anda telah menyiapkan lingkungan pengembangan .NET di mesin Anda.

-  Contoh File CAD: Untuk tutorial ini, kami akan menggunakan contoh file DXF. Anda dapat menemukannya di[Dokumentasi Aspose.CAD](https://reference.aspose.com/cad/net/).

## Impor Namespace

Untuk memulai, impor namespace yang diperlukan di awal aplikasi .NET Anda:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Langkah 1: Muat File CAD

Mulailah dengan memuat file CAD menggunakan kode berikut:

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

using (Image image = Image.Load(sourceFilePath))
{
    //Kode Anda untuk langkah selanjutnya akan ditempatkan di sini
}
```

## Langkah 2: Buat Opsi CadRasterization

 Buat sebuah contoh dari`CadRasterizationOptions` dan atur propertinya:

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
rasterizationOptions.AutomaticLayoutsScaling = true;
rasterizationOptions.NoScaling = false;
```

## Langkah 3: Buat Opsi Pdf

 Buat sebuah contoh dari`PdfOptions` dan atur`VectorRasterizationOptions` Properti:

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Langkah 4: Ekspor ke PDF

Ekspor file CAD ke PDF menggunakan opsi yang dikonfigurasi:

```csharp
image.Save(MyDir + "result_out.pdf", pdfOptions);
```

## Langkah 5: Buat TiffOptions

 Buat sebuah contoh dari`TiffOptions` dan atur`VectorRasterizationOptions` Properti:

```csharp
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Langkah 6: Ekspor ke TIFF

Ekspor file CAD ke TIFF menggunakan opsi yang dikonfigurasi:

```csharp
image.Save(MyDir + "result_out.tiff", tiffOptions);
```

## Kesimpulan

Selamat! Anda telah berhasil mengatur ukuran dan mode kanvas di Aspose.CAD untuk .NET. Fitur canggih ini membuka banyak kemungkinan untuk rendering CAD. Bereksperimenlah dengan berbagai opsi dan temukan potensi penuh Aspose.CAD dalam aplikasi .NET Anda.

## FAQ

### Q1: Bisakah saya menggunakan Aspose.CAD dengan perpustakaan .NET lainnya?

A1: Ya, Aspose.CAD terintegrasi secara mulus dengan perpustakaan .NET lainnya, memberikan peningkatan kemampuan untuk manipulasi CAD.

### Q2: Apakah uji coba gratis tersedia untuk Aspose.CAD?

 A2: Ya, Anda dapat menjelajahi fitur Aspose.CAD dengan uji coba gratis. Mengunjungi[Di Sini](https://releases.aspose.com/) untuk memulai.

### Q3: Bagaimana saya bisa mendapatkan dukungan untuk Aspose.CAD?

 A3: Untuk dukungan dan diskusi, kunjungi[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19).

### Q4: Di mana saya dapat menemukan dokumentasi komprehensif untuk Aspose.CAD?

 A4: Lihat[Dokumentasi Aspose.CAD](https://reference.aspose.com/cad/net/) untuk informasi rinci dan contoh.

### Q5: Bagaimana cara membeli Aspose.CAD untuk .NET?

 A5: Untuk membeli Aspose.CAD, kunjungi[halaman pembelian](https://purchase.aspose.com/buy).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
