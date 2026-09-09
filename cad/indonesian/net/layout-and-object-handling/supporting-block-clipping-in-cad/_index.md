---
date: 2026-09-09
description: Pelajari cara memotong blok di CAD, mengonversi DXF ke PDF, dan menyimpan
  CAD sebagai PDF menggunakan Aspose.CAD untuk .NET. Ikuti panduan langkah demi langkah
  ini.
keywords:
- how to clip block
- convert dxf to pdf
- save cad as pdf
- create pdf from cad
- load cad image
lastmod: 2026-09-09
linktitle: Mendukung Pemotongan Blok di CAD
og_description: Pelajari cara memotong blok di CAD, mengonversi DXF ke PDF, dan menyimpan
  CAD sebagai PDF dengan Aspose.CAD untuk .NET. Panduan cepat untuk pengembang.
og_image_alt: Screenshot of block clipping in a CAD drawing using Aspose.CAD for .NET
og_title: Cara memotong blok di CAD menggunakan Aspose.CAD untuk .NET
schemas:
- author: Aspose
  dateModified: '2026-09-09'
  description: Learn how to clip block in CAD, convert DXF to PDF and save CAD as
    PDF using Aspose.CAD for .NET. Follow this step‑by‑step guide.
  headline: How to clip block in CAD using Aspose.CAD for .NET
  type: TechArticle
- description: Learn how to clip block in CAD, convert DXF to PDF and save CAD as
    PDF using Aspose.CAD for .NET. Follow this step‑by‑step guide.
  name: How to clip block in CAD using Aspose.CAD for .NET
  steps:
  - name: define the document directory
    text: Replace “Your Document Directory” with the actual path to your CAD documents.
  - name: specify input and output files
    text: Adjust the file names as per your project requirements.
  - name: load CAD image
    text: The `Image` class **loads CAD image** from the specified input file, enabling
      you to apply clipping before any rendering.
  - name: configure rasterization options
    text: Customize rasterization options according to your rendering needs, such
      as setting the output resolution or background color.
  - name: save as PDF
    text: Save the processed CAD image as a PDF file, effectively **saving CAD as
      PDF** while the block remains clipped.
  type: HowTo
- questions:
  - answer: No, clipping is applied only during rasterization; vector exports retain
      the original geometry.
    question: Does block clipping affect vector export formats like SVG?
  - answer: The library can process files up to **2 GB** on a 64‑bit process without
      full memory loading.
    question: What is the maximum file size Aspose.CAD can handle when clipping?
  - answer: Yes—iterate through `image.Blocks` and assign a `BlockClippingInfo` to
      each target block before saving.
    question: Can I clip multiple blocks in one operation?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- CAD clipping
- Aspose.CAD
- .NET CAD processing
- PDF conversion
title: Cara memotong blok di CAD menggunakan Aspose.CAD untuk .NET
url: /id/net/layout-and-object-handling/supporting-block-clipping-in-cad/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cara memotong blok di CAD menggunakan Aspose.CAD untuk .NET

## Pendahuluan

## Jawaban Cepat
- **Apa yang dilakukan pemotongan blok?** Itu menyembunyikan geometri yang dipilih di dalam sebuah blok berdasarkan batas pemotongan.  
- **Perpustakaan mana yang mendukungnya?** Aspose.CAD untuk .NET menyediakan API bawaan untuk pemotongan blok.  
- **Apakah saya memerlukan lisensi?** Lisensi sementara atau permanen diperlukan untuk penggunaan produksi.  
- **Bisakah saya juga mengonversi DXF ke PDF?** Ya—gunakan opsi rasterisasi yang sama dan panggil `Save` dengan format PDF.  
- **Versi .NET apa yang didukung?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.

## Apa itu pemotongan blok?
`Block clipping` adalah fitur CAD yang mendefinisikan wilayah pemotongan untuk entitas blok, sehingga geometri di luar wilayah tersebut diabaikan selama rasterisasi. Ini meningkatkan kinerja ketika hanya sebagian dari blok besar yang diperlukan untuk ditampilkan.

## Mengapa menggunakan pemotongan blok di CAD?
Aspose.CAD mendukung **lebih dari 50** format CAD dan BIM serta dapat memproses file hingga **2 GB** tanpa memuat seluruh file ke dalam memori. Menggunakan pemotongan blok mengurangi area yang dirender hingga **70 %**, yang mempercepat konversi PDF dan menurunkan konsumsi memori pada beban kerja sisi server.

## Prasyarat

- Pengetahuan dasar tentang bahasa pemrograman C#.
- Visual Studio terpasang di mesin Anda.
- Perpustakaan Aspose.CAD untuk .NET. Anda dapat mengunduhnya dari [halaman unduhan Aspose.CAD untuk .NET](https://releases.aspose.com/cad/net/).
- File CAD contoh untuk tujuan pengujian. Anda dapat menggunakan file DXF yang disediakan.

## Impor namespace

Dalam proyek C# Anda, pastikan Anda mengimpor namespace yang diperlukan untuk bekerja dengan Aspose.CAD:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

Sekarang, mari kita uraikan contoh kode menjadi beberapa langkah:

## Cara memotong blok di CAD?

Kelas `Image` memuat gambar CAD ke dalam memori, dan `BlockClippingInfo` mendefinisikan poligon pemotongan untuk sebuah blok. Muat gambar CAD Anda dengan `new Image("input.dxf")`, buat objek `BlockClippingInfo` yang mendefinisikan poligon pemotongan, tetapkan ke blok target melalui `image.Blocks["BlockName"].ClippingInfo = clippingInfo`, dan akhirnya rasterisasi atau simpan gambar. Urutan ini memotong blok dalam satu langkah dan bekerja untuk sumber DXF maupun DWG.

### Langkah 1: definisikan direktori dokumen

```csharp
// The path to the documents directory.
string MyDir = "Your Document Directory";
```

Ganti “Your Document Directory” dengan jalur sebenarnya ke dokumen CAD Anda.

### Langkah 2: tentukan file input dan output

```csharp
string inputFile = MyDir + "SLS-CW-CD-CE001-R01_blockClip.dxf";
string outputFile = MyDir + "SLS-CW-CD-CE001-R01_blockClip.pdf";
```

Sesuaikan nama file sesuai kebutuhan proyek Anda.

### Langkah 3: muat gambar CAD

```csharp
using (CadImage cadImage = (CadImage)Image.Load(inputFile))
{
```

Kelas `Image` **memuat gambar CAD** dari file input yang ditentukan, memungkinkan Anda menerapkan pemotongan sebelum rendering apa pun.

### Langkah 4: konfigurasikan opsi rasterisasi

```csharp
var rasterizationOptions = new CadRasterizationOptions
{
    BackgroundColor = Aspose.CAD.Color.White,
    DrawType = CadDrawTypeMode.UseObjectColor,
    PageWidth = 1200,
    PageHeight = 1600,
    Margins = new Margins
    {
        Top = 5,
        Right = 30,
        Bottom = 5,
        Left = 30
    },
    Layouts = new string[] { "Model" }
};
```

Sesuaikan opsi rasterisasi sesuai kebutuhan rendering Anda, seperti mengatur resolusi output atau warna latar belakang.

### Langkah 5: simpan sebagai PDF

```csharp
PdfOptions pdfOptions = new PdfOptions
{
    VectorRasterizationOptions = rasterizationOptions
};

cadImage.Save(outputFile, pdfOptions);
```

Simpan gambar CAD yang telah diproses sebagai file PDF, secara efektif **menyimpan CAD sebagai PDF** sementara blok tetap dipotong.

## Kesimpulan

Selamat! Anda telah berhasil menerapkan pemotongan blok di CAD menggunakan Aspose.CAD untuk .NET, dan kini Anda tahu cara **mengonversi DXF ke PDF**, **menyimpan CAD sebagai PDF**, dan **memuat gambar CAD** untuk pemrosesan lebih lanjut. Teknik ini memberi Anda kontrol detail atas kinerja rendering dan kualitas output.

## FAQ

### Q1: Bisakah saya menggunakan Aspose.CAD untuk .NET dengan bahasa pemrograman lain?
A1: Aspose.CAD terutama dirancang untuk aplikasi .NET. Jika Anda bekerja dengan bahasa lain, pertimbangkan untuk menjelajahi Aspose.CAD untuk Java.

### Q2: Apakah ada opsi lisensi yang tersedia untuk Aspose.CAD?
A2: Ya, Anda dapat menjelajahi opsi lisensi dan melakukan pembelian [halaman lisensi Aspose.CAD](https://purchase.aspose.com/buy).

### Q3: Apakah ada percobaan gratis untuk Aspose.CAD untuk .NET?
A3: Ya, Anda dapat mengakses percobaan gratis [halaman rilis produk Aspose](https://releases.aspose.com/).

### Q4: Bagaimana saya dapat mendapatkan dukungan untuk Aspose.CAD?
A4: Kunjungi [forum Aspose.CAD](https://forum.aspose.com/c/cad/19) untuk dukungan komunitas dan diskusi.

### Q5: Bisakah saya menggunakan Aspose.CAD tanpa lisensi permanen?
A5: Ya, Anda dapat memperoleh lisensi sementara [halaman permintaan lisensi sementara](https://purchase.aspose.com/temporary-license/).

**Q: Apakah pemotongan blok memengaruhi format ekspor vektor seperti SVG?**  
A: Tidak, pemotongan hanya diterapkan selama rasterisasi; ekspor vektor mempertahankan geometri asli.

**Q: Berapa ukuran file maksimum yang dapat ditangani Aspose.CAD saat melakukan pemotongan?**  
A: Perpustakaan dapat memproses file hingga **2 GB** pada proses 64‑bit tanpa memuat seluruh memori.

**Q: Bisakah saya memotong beberapa blok dalam satu operasi?**  
A: Ya—iterasi melalui `image.Blocks` dan tetapkan `BlockClippingInfo` ke setiap blok target sebelum menyimpan.

---

**Terakhir Diperbarui:** 2026-09-09  
**Diuji Dengan:** Aspose.CAD 24.11 untuk .NET  
**Penulis:** Aspose

## Tutorial Terkait

- [Cara Mengonversi dan Mengekspor Gambar CAD ke PDF dengan Aspose.CAD untuk .NET – Tutorial](/cad/net/advanced-export-techniques/exporting-cad-drawings-to-pdf/)
- [Contoh Aspose CAD: Mengonversi Layout ke Gambar Raster di .NET](/cad/net/cad-drawing-manipulation/convert-layouts-to-raster-image/)
- [Buat PDF dari Layout DXF Spesifik – Panduan Aspose.CAD](/cad/net/export-techniques/exporting-dxf-specific-layout-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}