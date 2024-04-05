---
title: Ekspor DGN ke PDF di Aspose.CAD untuk .NET
linktitle: Ekspor DGN ke PDF
second_title: Aspose.CAD .NET - Format File CAD dan BIM
description: Pelajari cara mengekspor file DGN ke PDF dengan mudah menggunakan Aspose.CAD untuk .NET. Panduan langkah demi langkah untuk manipulasi file CAD yang lancar.
type: docs
weight: 12
url: /id/net/cad-export-formats/export-dgn-to-pdf/
---
## Perkenalan

Dalam dunia pengembangan .NET, Aspose.CAD adalah perpustakaan canggih yang memfasilitasi manipulasi dan konversi file CAD. Salah satu tugas umum yang sering dihadapi pengembang adalah mengekspor file DGN ke format PDF. Dalam tutorial ini, kita akan menjalani proses langkah demi langkah, menggunakan Aspose.CAD untuk .NET.

## Prasyarat

Sebelum masuk ke tutorial, pastikan Anda memiliki hal berikut:

- Pengetahuan tentang C# dan kerangka .NET.
-  Aspose.CAD untuk perpustakaan .NET diinstal. Anda dapat mengunduhnya[Di Sini](https://releases.aspose.com/cad/net/).
- Contoh file DGN, misalnya, "Nikon_D90_Camera.dgn" untuk tutorial ini.

## Impor Namespace

Dalam proyek C# Anda, mulailah dengan mengimpor namespace yang diperlukan:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Langkah 1: Muat File DGN

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (DgnImage cadImage = (DgnImage)Image.Load(sourceFilePath))
{
    // Kode Anda di sini...
}
```

## Langkah 2: Konfigurasikan Opsi Rasterisasi

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 600;
rasterizationOptions.PageHeight = 300;
rasterizationOptions.NoScaling = true;
rasterizationOptions.AutomaticLayoutsScaling = false;
```

## Langkah 3: Buat Opsi PDF

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Langkah 4: Simpan sebagai PDF

```csharp
cadImage.Save(MyDir + "ExportDGNToPdf_out.pdf", pdfOptions);
```

## Kesimpulan

Selamat! Anda telah berhasil mengekspor file DGN ke PDF menggunakan Aspose.CAD untuk .NET. Tutorial ini mencakup langkah-langkah penting, mulai dari memuat file DGN hingga mengonfigurasi opsi rasterisasi dan menyimpan hasilnya sebagai PDF.

## FAQ

### Q1: Bisakah saya menggunakan Aspose.CAD untuk .NET tanpa sepengetahuan CAD sebelumnya?

A1: Tentu saja! Aspose.CAD menyederhanakan tugas CAD yang kompleks, sehingga dapat diakses oleh pengembang dengan beragam latar belakang.

### Q2: Di mana saya dapat menemukan lebih banyak contoh dan dokumentasi untuk Aspose.CAD?

 A2: Jelajahi[dokumentasi](https://reference.aspose.com/cad/net/) untuk panduan dan contoh yang komprehensif.

### Q3: Apakah ada uji coba gratis yang tersedia untuk Aspose.CAD?

A3: Ya, Anda bisa mendapatkan uji coba gratis[Di Sini](https://releases.aspose.com/).

### Q4: Bagaimana saya bisa mendapatkan lisensi sementara untuk Aspose.CAD?

 A4: Dapatkan lisensi sementara[Di Sini](https://purchase.aspose.com/temporary-license/).

### Q5: Butuh bantuan atau punya pertanyaan?

A5: Kunjungi[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19) untuk dukungan masyarakat.