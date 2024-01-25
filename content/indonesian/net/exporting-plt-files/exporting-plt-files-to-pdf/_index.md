---
title: Mengekspor File PLT ke PDF - Panduan Aspose.CAD
linktitle: Mengekspor File PLT ke PDF
second_title: Aspose.CAD .NET - Format File CAD dan BIM
description: Konversi file PLT ke PDF dengan mudah menggunakan Aspose.CAD untuk .NET. Ikuti panduan langkah demi langkah kami untuk integrasi yang lancar dan hasil yang andal.
type: docs
weight: 11
url: /id/net/exporting-plt-files/exporting-plt-files-to-pdf/
---
Dalam dunia desain berbantuan komputer (CAD) yang dinamis, kemampuan untuk mengonversi file PLT ke format PDF dengan lancar adalah keterampilan yang berharga. Aspose.CAD untuk .NET memberdayakan pengembang untuk mencapai tugas ini dengan mudah. Dalam tutorial ini, kita akan menjalani proses langkah demi langkah, memastikan kejelasan dan pemahaman di setiap kesempatan.

## Prasyarat

Sebelum kita mendalami tutorialnya, pastikan Anda memiliki prasyarat berikut:

1.  Aspose.CAD untuk Perpustakaan .NET: Pastikan Anda telah menginstal perpustakaan Aspose.CAD. Anda dapat mengunduhnya[Di Sini](https://releases.aspose.com/cad/net/).

2. Lingkungan Pengembangan: Siapkan lingkungan pengembangan .NET yang berfungsi.

## Impor Namespace

Di proyek .NET Anda, mulailah dengan mengimpor namespace yang diperlukan:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadConsts;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using static Aspose.CAD.Examples.CSharp.DWG_Drawings.SupportMLeaderEntityForDWGFormat;
using Aspose.CAD.ImageOptions;
```

Namespace ini akan menyediakan kelas dan fungsi penting untuk menangani operasi CAD.

## Langkah 1: Siapkan Direktori Dokumen

Mulailah dengan menentukan jalur ke direktori dokumen Anda dalam kode Anda:

```csharp
string MyDir = "Your Document Directory";
```

Ganti "Direktori Dokumen Anda" dengan jalur sebenarnya ke dokumen Anda.

## Langkah 2: Muat File PLT

Muat file PLT ke dalam gambar CAD menggunakan cuplikan kode berikut:

```csharp
string sourceFilePath = MyDir + "50states.plt";

using (Image cadImage = Image.Load(sourceFilePath))
{
    // Kode Anda ada di sini
}
```

## Langkah 3: Konfigurasikan Opsi Rasterisasi

Konfigurasikan opsi rasterisasi untuk mengekspor ke PDF. Tetapkan dimensi halaman, jenis gambar, dan warna latar belakang:

```csharp
CadRasterizationOptions options = new CadRasterizationOptions
{
    PageHeight = 1600,
    PageWidth = 1600,
    DrawType = CadDrawTypeMode.UseObjectColor,
    BackgroundColor = Color.White
};
```

## Langkah 4: Atur Opsi PDF

Tentukan opsi PDF dan tautkan ke opsi rasterisasi yang telah ditetapkan sebelumnya:

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = options;
```

## Langkah 5: Simpan sebagai PDF

Simpan gambar CAD sebagai file PDF:

```csharp
cadImage.Save(MyDir + "50states.pdf", pdfOptions);
```

## Kesimpulan

Dalam tutorial ini, kita telah mempelajari proses mengekspor file PLT ke PDF menggunakan Aspose.CAD untuk .NET. Pustaka serbaguna ini menyederhanakan pengoperasian CAD, menjadikannya alat yang sangat berharga bagi pengembang yang membutuhkan konversi file yang efisien dan andal.

## FAQ

### Q1: Bisakah saya menggunakan Aspose.CAD untuk .NET di aplikasi web saya?

A1: Ya, Aspose.CAD untuk .NET kompatibel dengan aplikasi desktop dan web.

### Q2: Apakah ada uji coba gratis yang tersedia untuk Aspose.CAD untuk .NET?

 A2: Tentu saja, Anda dapat mencoba uji coba gratis[Di Sini](https://releases.aspose.com/).

### Q3: Bagaimana saya bisa mendapatkan dukungan untuk Aspose.CAD untuk .NET?

 A3: Kunjungi[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19) untuk dukungan dan bimbingan masyarakat.

### Q4: Format file apa yang didukung Aspose.CAD?

A4: Aspose.CAD mendukung berbagai format CAD, termasuk DWG, DXF, dan PLT.

### Q5: Di mana saya dapat menemukan dokumentasi terperinci untuk Aspose.CAD untuk .NET?

 A5: Lihat[Dokumentasi Aspose.CAD](https://reference.aspose.com/cad/net/) untuk informasi mendalam.