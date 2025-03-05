---
title: Menambahkan Tanda Air ke Gambar CAD - Panduan Aspose.CAD
linktitle: Menambahkan Tanda Air ke Gambar CAD
second_title: Aspose.CAD .NET - Format File CAD dan BIM
description: Sempurnakan gambar CAD Anda dengan tanda air profesional menggunakan Aspose.CAD untuk .NET. Ikuti panduan langkah demi langkah kami untuk desain yang dipersonalisasi dan menarik.
type: docs
weight: 11
url: /id/net/plt-and-watermarking/adding-watermarks-to-cad-drawings/
---
## Perkenalan

Apakah Anda ingin menyempurnakan gambar CAD Anda dengan menambahkan tanda air profesional? Aspose.CAD untuk .NET memberikan solusi tangguh untuk mengintegrasikan tanda air ke dalam file CAD Anda dengan lancar. Dalam panduan langkah demi langkah ini, kami akan memandu Anda melalui proses penambahan tanda air menggunakan Aspose.CAD, memastikan gambar Anda tidak hanya menyampaikan informasi penting tetapi juga membawa tanda unik Anda.

## Prasyarat

Sebelum masuk ke tutorial, pastikan Anda memiliki hal berikut:
-  Aspose.CAD untuk .NET: Pastikan Anda telah menginstal perpustakaan Aspose.CAD. Anda dapat mengunduhnya[Di Sini](https://releases.aspose.com/cad/net/).
- Direktori Dokumen Anda: Siapkan direktori untuk menyimpan gambar CAD Anda.
Sekarang, mari mulai menambahkan tanda air ke gambar CAD Anda!

## Impor Namespace

Mulailah dengan mengimpor namespace yang diperlukan ke proyek .NET Anda:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadObjects;
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
using (CadImage cadImage = (CadImage)Image.Load(MyDir + "Drawing11.dwg")) {
```

## Langkah 2: Tambahkan Tanda Air sebagai MTEXT

```csharp
// Tambahkan MTEXT baru
CadMText watermark = new CadMText();
watermark.Text = "Watermark message";
watermark.InitialTextHeight = 40;
watermark.InsertionPoint = new Cad3DPoint(300, 40);
watermark.LayerName = "0";
cadImage.BlockEntities["*Model_Space"].AddEntity(watermark);
```

## Langkah 3: Atau Tambahkan Tanda Air sebagai Teks

```csharp
// Alternatifnya, tambahkan entitas yang lebih sederhana seperti Teks
CadText text = new CadText();
text.DefaultValue = "Watermark text";
text.TextHeight = 40;
text.FirstAlignment = new Cad3DPoint(300, 40);
text.LayerName = "0";
cadImage.BlockEntities["*Model_Space"].AddEntity(text);
```

## Langkah 4: Ekspor ke PDF

```csharp
// Ekspor gambar CAD dengan tanda air ke PDF
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
rasterizationOptions.Layouts = new[] { "Model" };
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
cadImage.Save(MyDir + "AddWatermark_out.pdf", pdfOptions);
```

Ulangi langkah-langkah ini untuk gambar yang berbeda, dan Anda akan memiliki file CAD yang diberi tanda air yang terlihat profesional dalam waktu singkat!

## Kesimpulan

Selamat! Anda telah berhasil mempelajari cara menambahkan tanda air ke gambar CAD Anda menggunakan Aspose.CAD untuk .NET. Proses sederhana namun kuat ini memungkinkan Anda mempersonalisasi desain Anda sambil menjaga integritas gambar teknis Anda.

## FAQ

### Q1: Dapatkah saya menyesuaikan tampilan tanda air?

A1: Ya, Anda dapat menyesuaikan teks, font, ukuran, dan posisi tanda air sesuai preferensi Anda.

### Q2: Apakah Aspose.CAD kompatibel dengan format file CAD yang berbeda?

A2: Aspose.CAD mendukung berbagai format file CAD, termasuk DWG dan DXF, memastikan kompatibilitas luas.

### Q3: Dapatkah saya menambahkan beberapa tanda air ke satu gambar CAD?

A3: Tentu saja! Anda dapat menambahkan tanda air sebanyak yang diperlukan, sehingga memberikan fleksibilitas untuk berbagai kasus penggunaan.

### Q4: Apakah Aspose.CAD menawarkan uji coba gratis?

A4: Ya, Anda dapat menjelajahi fitur Aspose.CAD dengan uji coba gratis. Mendapatkan[Di Sini](https://releases.aspose.com/).

### Q5: Di mana saya dapat menemukan dukungan untuk Aspose.CAD?

 A5: Untuk pertanyaan atau bantuan apa pun, kunjungi[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19).