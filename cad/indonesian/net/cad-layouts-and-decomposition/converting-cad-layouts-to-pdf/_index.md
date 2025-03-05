---
title: Mengonversi Tata Letak CAD ke PDF - Tutorial Aspose.CAD
linktitle: Mengonversi Tata Letak CAD ke PDF
second_title: Aspose.CAD .NET - Format File CAD dan BIM
description: Konversikan tata letak CAD ke PDF dengan mudah menggunakan Aspose.CAD untuk .NET. Ikuti panduan langkah demi langkah kami untuk integrasi yang lancar.
type: docs
weight: 10
url: /id/net/cad-layouts-and-decomposition/converting-cad-layouts-to-pdf/
---
## Perkenalan

Apakah Anda ingin mengonversi tata letak CAD ke PDF dengan lancar? Aspose.CAD untuk .NET memberikan solusi tangguh untuk membuat proses ini efisien dan mudah. Dalam tutorial ini, kami akan memandu Anda melalui langkah-langkah menggunakan Aspose.CAD, API canggih yang memberdayakan pengembang untuk bekerja dengan file CAD dengan mudah.

## Prasyarat

Sebelum masuk ke tutorial, pastikan Anda memiliki prasyarat berikut:

-  Aspose.CAD untuk .NET: Unduh dan instal perpustakaan. Kamu bisa menemukannya[Di Sini](https://releases.aspose.com/cad/net/).

- Lingkungan .NET: Pastikan Anda memiliki lingkungan pengembangan .NET yang berfungsi.

- Contoh File CAD: Siapkan contoh file CAD untuk dikonversi. Untuk tutorial ini, kita akan menggunakan "conic_pyramid.dxf."

## Impor Namespace

Mulailah dengan mengimpor namespace yang diperlukan ke proyek .NET Anda. Langkah ini memastikan bahwa Anda memiliki akses ke fungsionalitas Aspose.CAD.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
using Aspose.CAD.FileFormats.Cad;
```

## Langkah 1: Siapkan Proyek Anda

Mulailah dengan menyiapkan proyek .NET Anda. Buat proyek baru atau buka proyek yang sudah ada di mana Anda ingin menerapkan konversi CAD ke PDF.

## Langkah 2: Tentukan Jalur File CAD Sumber

Tentukan jalur ke file CAD Anda. Dalam contoh kita, file sumbernya adalah "conic_pyramid.dxf."

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";
```

## Langkah 3: Muat File CAD

Buat instance kelas CadImage dan muat file CAD ke dalam aplikasi.

```csharp
using (Aspose.CAD.Image cadImage = (Aspose.CAD.Image)Image.Load(sourceFilePath))
```

## Langkah 4: Konfigurasikan Opsi Rasterisasi

Konfigurasikan opsi rasterisasi untuk menyesuaikan keluaran PDF. Tetapkan dimensi halaman, penskalaan tata letak, dan parameter relevan lainnya.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
// Opsi konfigurasi lainnya...
```

## Langkah 5: Atur Tata Letak

Tentukan tata letak yang ingin Anda sertakan dalam PDF. Dalam contoh ini, kami menggunakan tata letak "Model".

```csharp
rasterizationOptions.Layouts = new string[] { "Model" };
```

## Langkah 6: Tentukan Opsi PDF

Buat instance kelas PdfOptions dan kaitkan dengan opsi rasterisasi.

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Langkah 7: Atur Opsi Grafik

Konfigurasikan opsi grafik untuk PDF, termasuk mode penghalusan, rendering teks, dan interpolasi.

```csharp
rasterizationOptions.GraphicsOptions.SmoothingMode = SmoothingMode.HighQuality;
rasterizationOptions.GraphicsOptions.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
rasterizationOptions.GraphicsOptions.InterpolationMode = InterpolationMode.HighQualityBicubic;
```

## Langkah 8: Simpan ke PDF

Tentukan jalur keluaran untuk file PDF dan simpan tata letak CAD sebagai PDF.

```csharp
MyDir = MyDir + "CADLayoutsToPDF_out.pdf";
cadImage.Save(MyDir, pdfOptions);
```

## Kesimpulan

Selamat! Anda telah berhasil mengonversi tata letak CAD ke PDF menggunakan Aspose.CAD untuk .NET. Tutorial ini memberikan panduan komprehensif bagi pengembang yang ingin menyederhanakan proses ini dalam aplikasi mereka.

## FAQ

### Q1: Dapatkah saya mengonversi beberapa tata letak CAD sekaligus?

 A1: Ya, Anda dapat menentukan beberapa tata letak di`Layouts` array untuk memasukkannya ke dalam PDF.

### Q2: Apakah ada batasan pada format file CAD yang didukung?

A2: Aspose.CAD untuk .NET mendukung berbagai format CAD, termasuk DWG dan DXF.

### Q3: Bagaimana cara menyesuaikan tampilan keluaran PDF?

A3: Gunakan opsi rasterisasi dan grafik yang disediakan untuk menyesuaikan keluaran PDF sesuai preferensi Anda.

### Q4: Apakah ada versi uji coba yang tersedia untuk Aspose.CAD untuk .NET?

 A4: Ya, Anda dapat menjelajahi fitur-fiturnya dengan[versi percobaan gratis](https://releases.aspose.com/).

### Q5: Di mana saya dapat mencari dukungan atau mengajukan pertanyaan?

A5: Kunjungi[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19) untuk bantuan dan diskusi.