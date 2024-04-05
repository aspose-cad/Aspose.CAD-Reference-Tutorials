---
title: Mengekspor Tata Letak Tertentu ke PDF - Panduan Aspose.CAD
linktitle: Mengekspor Tata Letak Tertentu ke PDF
second_title: Aspose.CAD .NET - Format File CAD dan BIM
description: Pelajari cara mengekspor tata letak tertentu ke PDF menggunakan Aspose.CAD untuk .NET. Panduan langkah demi langkah untuk integrasi yang lancar.
type: docs
weight: 13
url: /id/net/advanced-export-techniques/exporting-specific-layouts-to-pdf/
---
## Perkenalan

Selamat datang di panduan langkah demi langkah kami tentang mengekspor tata letak tertentu ke PDF menggunakan Aspose.CAD untuk .NET. Aspose.CAD adalah perpustakaan canggih yang memungkinkan pengembang bekerja dengan format file CAD dengan lancar. Dalam tutorial ini, kami akan fokus mengekspor tata letak tertentu dari file DWG ke PDF menggunakan Aspose.CAD di lingkungan .NET.

## Prasyarat

Sebelum kita mendalami tutorialnya, pastikan Anda memiliki prasyarat berikut:

-  Aspose.CAD untuk Perpustakaan .NET: Pastikan Anda telah menginstal perpustakaan Aspose.CAD. Anda dapat mengunduhnya[Di Sini](https://releases.aspose.com/cad/net/).

- Lingkungan Pengembangan: Siapkan lingkungan pengembangan .NET, seperti Visual Studio.

## Impor Namespace

Di proyek .NET Anda, impor namespace yang diperlukan untuk Aspose.CAD:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Langkah 1: Muat File DWG

```csharp
// Jalur ke direktori dokumen.
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "visualization_-_conference_room.dwg";

using (Image image = Image.Load(sourceFilePath))
{
    // Kode Anda untuk langkah selanjutnya ada di sini.
}
```

## Langkah 2: Tetapkan Opsi CadRasterization

```csharp
// Buat instance CadRasterizationOptions dan atur berbagai propertinya
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
```

## Langkah 3: Tentukan Nama Tata Letak

```csharp
// Tentukan nama tata letak yang diinginkan
rasterizationOptions.Layouts = new string[] { "Layout1" };
```

## Langkah 4: Buat Opsi Pdf

```csharp
// Buat sebuah instance dari PdfOptions
PdfOptions pdfOptions = new PdfOptions();
// Setel properti VectorRasterizationOptions
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Langkah 5: Ekspor ke PDF

```csharp
MyDir = MyDir + "ExportSpecificLayoutToPDF_out.pdf";
// Ekspor DWG ke PDF
image.Save(MyDir, pdfOptions);
```

## Langkah 6: Tampilkan Pesan Sukses

```csharp
// Tampilkan pesan sukses
Console.WriteLine("\nThe DWG file with a specific layout exported successfully to PDF.\nFile saved at " + MyDir);
```

## Kesimpulan

Selamat! Anda telah berhasil mempelajari cara mengekspor tata letak tertentu ke PDF menggunakan Aspose.CAD untuk .NET. Panduan ini memberikan panduan mendetail, memastikan Anda dapat mengintegrasikan fungsi ini ke dalam proyek Anda dengan mudah.

## FAQ

### Q1: Dapatkah saya mengekspor beberapa tata letak secara bersamaan?

 A1: Ya, cukup modifikasi`Layouts` array di Langkah 3 untuk memasukkan nama semua tata letak yang diinginkan.

### Q2: Apakah Aspose.CAD kompatibel dengan format file CAD lainnya?

A2: Ya, Aspose.CAD mendukung berbagai format CAD, termasuk DWG, DXF, DWF, dan banyak lagi.

### Q3: Bagaimana cara menyesuaikan pengaturan keluaran PDF?

 A3: Jelajahi properti`CadRasterizationOptions` di Langkah 2 untuk opsi penyesuaian.

### Q4: Di mana saya dapat menemukan dokumentasi Aspose.CAD tambahan?

 A4: Kunjungi[dokumentasi](https://reference.aspose.com/cad/net/) untuk informasi mendalam.

### Q5: Apakah tersedia uji coba gratis?

 A5: Ya, Anda dapat mengakses uji coba gratis[Di Sini](https://releases.aspose.com/).