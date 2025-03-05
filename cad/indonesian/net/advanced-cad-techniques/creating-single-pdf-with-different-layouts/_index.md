---
title: Membuat PDF Tunggal dengan Tata Letak Berbeda - Panduan Aspose.CAD
linktitle: Membuat PDF Tunggal dengan Tata Letak Berbeda
second_title: Aspose.CAD .NET - Format File CAD dan BIM
description: Buat satu PDF dengan tata letak berbeda menggunakan Aspose.CAD untuk .NET. Ikuti panduan langkah demi langkah kami untuk integrasi yang lancar dan pembuatan PDF yang efisien.
type: docs
weight: 13
url: /id/net/advanced-cad-techniques/creating-single-pdf-with-different-layouts/
---
## Perkenalan

Apakah Anda ingin membuat satu dokumen PDF dari gambar CAD dengan tata letak berbeda menggunakan Aspose.CAD untuk .NET? Panduan langkah demi langkah ini akan memandu Anda melalui prosesnya, membantu Anda mencapai integrasi yang lancar dan pembuatan PDF yang efisien. Aspose.CAD untuk .NET menyediakan fitur canggih untuk memanipulasi gambar CAD secara terprogram, dan dalam tutorial ini, kita akan fokus pada pembuatan satu PDF dengan tata letak berbeda.

## Prasyarat

Sebelum masuk ke tutorial, pastikan Anda memiliki prasyarat berikut:

-  Aspose.CAD untuk .NET: Pastikan Anda telah menginstal Aspose.CAD untuk .NET. Anda dapat mengunduhnya dari[Di Sini](https://releases.aspose.com/cad/net/).

- Lingkungan Pengembangan: Siapkan lingkungan pengembangan .NET, dan miliki pemahaman dasar tentang pemrograman C#.

## Impor Namespace

Dalam proyek C# Anda, sertakan namespace yang diperlukan untuk memanfaatkan fungsionalitas Aspose.CAD untuk .NET:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## Langkah 1: Muat Gambar CAD

```csharp
// Jalur ke direktori dokumen.
string MyDir = "Your Document Directory";

using (CadImage cadImage = (CadImage)Image.Load(MyDir + "City skyway map.dwg"))
{
    // Kode Anda untuk Langkah 1 ada di sini
}
```

## Langkah 2: Sesuaikan Opsi Rasterisasi

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1000;
rasterizationOptions.PageHeight = 1000;

// Ukuran khusus untuk beberapa tata letak
rasterizationOptions.LayoutPageSizes.Add("ANSI C Plot", new SizeF(500, 1000));
rasterizationOptions.LayoutPageSizes.Add("8.5 x 11 Plot", new SizeF(1000, 100));
```

## Langkah 3: Tentukan Opsi PDF

```csharp
PdfOptions pdfOptions = new PdfOptions() { VectorRasterizationOptions = rasterizationOptions };
```

## Langkah 4: Simpan sebagai PDF

```csharp
cadImage.Save(MyDir + "singlePDF_out.pdf", pdfOptions);
```

Sekarang Anda telah berhasil membuat satu dokumen PDF dengan tata letak berbeda menggunakan Aspose.CAD untuk .NET. Jangan ragu untuk menjelajahi lebih banyak fitur dan menyesuaikan kode sesuai dengan kebutuhan spesifik Anda.

## Kesimpulan

Dalam tutorial ini, kami membahas proses pembuatan satu PDF dari gambar CAD dengan tata letak berbeda menggunakan Aspose.CAD untuk .NET. Pustaka canggih ini menyederhanakan tugas manipulasi CAD dan menawarkan fleksibilitas untuk berbagai skenario.

## FAQ

### Q1: Dapatkah saya menggunakan Aspose.CAD untuk .NET dengan format CAD lainnya?

A1: Ya, Aspose.CAD untuk .NET mendukung berbagai format CAD seperti DWG, DXF, DGN, dan banyak lagi.

### Q2: Apakah tersedia uji coba gratis?

 A2: Ya, Anda dapat menjelajahi uji coba gratis[Di Sini](https://releases.aspose.com/).

### Q3: Bagaimana saya bisa mendapatkan dukungan untuk Aspose.CAD untuk .NET?

 A3: Kunjungi[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19) untuk dukungan masyarakat.

### Q4: Di mana saya dapat menemukan dokumentasi terperinci?

 A4: Lihat dokumentasi[Di Sini](https://reference.aspose.com/cad/net/).

### Q5: Dapatkah saya membeli lisensi Aspose.CAD untuk .NET?

 A5: Ya, Anda bisa membeli lisensinya[Di Sini](https://purchase.aspose.com/buy).