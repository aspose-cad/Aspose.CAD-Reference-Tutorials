---
title: Tingkatkan Ekspor CAD dengan Opsi Pena Kustom di Aspose.CAD untuk .NET
linktitle: Dukungan Pena dalam Ekspor
second_title: Aspose.CAD .NET - Format File CAD dan BIM
description: Pelajari cara meningkatkan ekspor gambar CAD Anda menggunakan Aspose.CAD untuk .NET. Sesuaikan opsi pena untuk visual menakjubkan dalam PDF, PNG, BMP, dan lainnya.
type: docs
weight: 12
url: /id/net/cad-features-and-support/pen-support-in-export/
---
## Perkenalan

Aspose.CAD untuk .NET menyediakan seperangkat alat canggih untuk bekerja dengan file Computer-Aided Design (CAD), memungkinkan pengembang memanipulasi dan mengekspor gambar CAD dengan lancar. Salah satu fitur penting adalah dukungan pena selama ekspor, memungkinkan pengguna untuk menyesuaikan pengaturan batas awal dan akhir pena saat mengekspor gambar CAD ke berbagai format seperti PDF, PNG, BMP, GIF, JPEG2000, JPEG, PSD, TIFF, dan WMF.

Dalam tutorial ini, kita akan mempelajari secara spesifik dukungan pena dalam ekspor menggunakan Aspose.CAD untuk .NET. Kami akan menguraikan setiap langkah, memberikan penjelasan dan contoh yang jelas untuk memandu Anda melalui proses tersebut.

## Prasyarat

Sebelum kita mendalami tutorialnya, pastikan Anda memiliki prasyarat berikut:

- Aspose.CAD untuk .NET diinstal di lingkungan pengembangan Anda. Anda dapat mengunduhnya dari[halaman rilis](https://releases.aspose.com/cad/net/).

- Pemahaman dasar tentang format file CAD, khususnya DXF (Drawing Exchange Format).

- Pengetahuan tentang bahasa pemrograman C#.

## Impor Namespace

Untuk memulai, pastikan Anda mengimpor namespace yang diperlukan dalam proyek C# Anda:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Drawing;
using System.Drawing.Drawing2D;
```

## Langkah 1: Siapkan Direktori Dokumen Anda

Tentukan direktori tempat dokumen CAD Anda berada:

```csharp
string MyDir = "Your Document Directory";
```

## Langkah 2: Muat Gambar CAD

Muat gambar CAD menggunakan Aspose.CAD:

```csharp
string sourceFilePath = MyDir + "conic_pyramid.dxf";
CadImage cadImage = (CadImage)Image.Load(sourceFilePath);
```

## Langkah 3: Konfigurasikan Opsi Rasterisasi

Buat opsi rasterisasi dan PDF untuk menyesuaikan proses ekspor:

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
PdfOptions pdfOptions = new PdfOptions();
```

## Langkah 4: Sesuaikan Opsi Pena

Mengatur opsi tutup awal dan akhir untuk pena:

```csharp
rasterizationOptions.PenOptions = new PenOptions
{
   StartCap = LineCap.Flat,
   EndCap = LineCap.Flat
};
```

## Langkah 5: Terapkan Opsi Rasterisasi Vektor

Terapkan opsi rasterisasi ke opsi PDF:

```csharp
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Langkah 6: Simpan PDF yang Diekspor

Simpan gambar CAD dengan opsi pena khusus sebagai file PDF:

```csharp
cadImage.Save(MyDir + "9LHATT-A56_generated.pdf", pdfOptions);
```

## Kesimpulan

Dalam tutorial ini, kita telah menjelajahi dukungan pena dalam fitur ekspor Aspose.CAD untuk .NET. Dengan mengikuti panduan langkah demi langkah, Anda dapat dengan mudah menyesuaikan pengaturan batas awal dan akhir untuk pena, sehingga meningkatkan fleksibilitas ekspor gambar CAD Anda.

Jangan ragu untuk bereksperimen dengan opsi pena yang berbeda untuk mendapatkan efek visual yang diinginkan pada gambar yang Anda ekspor.

## FAQ

### Q1: Bisakah saya menggunakan opsi pena ini untuk format gambar lain selain PDF?

A1: Ya, opsi pena dapat diterapkan ke berbagai format gambar seperti PNG, BMP, GIF, JPEG, dan lainnya.

### Q2: Di mana saya dapat menemukan dokumentasi tambahan untuk Aspose.CAD untuk .NET?

 A2: Lihat[dokumentasi](https://reference.aspose.com/cad/net/) untuk informasi lengkap dan contoh.

### Q3: Apakah ada uji coba gratis yang tersedia untuk Aspose.CAD untuk .NET?

 A3: Ya, Anda dapat mengakses uji coba gratis[Di Sini](https://releases.aspose.com/).

### Q4: Bagaimana saya bisa mendapatkan lisensi sementara untuk Aspose.CAD untuk .NET?

 A4: Kunjungi[halaman lisensi sementara](https://purchase.aspose.com/temporary-license/) untuk opsi lisensi sementara.

### Q5: Di mana saya dapat mencari dukungan komunitas untuk Aspose.CAD untuk .NET?

 A5: Terlibat dengan komunitas di[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19).