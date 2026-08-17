---
date: 2026-08-17
description: Pelajari cara menambahkan gambar ke file dwg menggunakan C# dan Aspose.CAD
  untuk .NET. Panduan ini memandu Anda melalui proses mengimpor gambar, menentukan
  titik sisipan, dan mengekspor ke PDF.
keywords:
- add image to dwg
- convert dwg to pdf
- set insertion point dwg
- embed png in dwg
- save dwg as pdf
lastmod: 2026-08-17
linktitle: Mengimpor Gambar ke File DWG dengan C#
og_description: Pelajari cara menambahkan gambar ke file dwg menggunakan C#. Tutorial
  ini mencakup mengimpor gambar, menentukan titik sisipan, dan mengonversi dwg ke
  pdf dengan Aspose.CAD.
og_image_alt: Guide showing C# code to embed an image into a DWG file using Aspose.CAD
og_title: Cara menambahkan gambar ke file dwg dengan C# menggunakan Aspose.CAD
schemas:
- author: Aspose
  dateModified: '2026-08-17'
  description: Learn how to add image to dwg files using C# and Aspose.CAD for .NET.
    This guide walks you through importing images, setting insertion points, and exporting
    to PDF.
  headline: How to add image to dwg files with C# using Aspose.CAD
  type: TechArticle
- description: Learn how to add image to dwg files using C# and Aspose.CAD for .NET.
    This guide walks you through importing images, setting insertion points, and exporting
    to PDF.
  name: How to add image to dwg files with C# using Aspose.CAD
  steps:
  - name: set up your document directory
    text: Prepare the folder that contains the source DWG and the image you want to
      embed.
  - name: load the dwg file
    text: The `CadImage` class represents a DWG drawing and provides access to its
      entities, layers, and metadata.
  - name: define the image properties
    text: Create an `Image` object that points to the raster file (e.g., PNG) and
      specify its format.
  - name: set insertion point dwg and vectors
    text: Specify where the image should appear inside the drawing and how it should
      be scaled. The insertion point is defined by a 2‑D coordinate, while the vectors
      control width and height.
  - name: create and configure the raster image
    text: Instantiate a `RasterImage` object, assign the image data, and set any additional
      rendering options.
  - name: add image to dwg file
    text: Insert the configured raster image into the DWG’s entities collection so
      it becomes part of the drawing.
  - name: save as pdf (export dwg to pdf)
    text: After embedding the image you can **convert dwg to pdf** or **save dwg as
      pdf** with a single call. This is useful for sharing the drawing with stakeholders
      who don’t have CAD software.
  type: HowTo
- questions:
  - answer: The core library is .NET‑specific, but Aspose offers equivalent APIs for
      Java, Python and other platforms.
    question: Can I use Aspose.CAD for .NET with other programming languages?
  - answer: Yes, you can explore a free trial on the [Aspose free trial page](https://releases.aspose.com/).
    question: Is a free trial available for Aspose.CAD?
  - answer: The documentation is available in the [Aspose.CAD .NET API reference](https://reference.aspose.com/cad/net/).
    question: Where can I find detailed documentation for Aspose.CAD?
  - answer: Visit the [temporary license page](https://purchase.aspose.com/temporary-license/)
      to get a temporary license.
    question: How do I obtain a temporary license for Aspose.CAD?
  - answer: Yes, you can seek support and engage with the community in the [Aspose.CAD
      community forum](https://forum.aspose.com/c/cad/19).
    question: Are there community forums for Aspose.CAD support?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- CAD
- Aspose.CAD
- C# image processing
- DWG manipulation
title: Cara menambahkan gambar ke file dwg dengan C# menggunakan Aspose.CAD
url: /id/net/image-manipulation-and-rendering/importing-images-into-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cara menambahkan gambar ke file dwg dengan C# menggunakan Aspose.CAD

## Pendahuluan

Menambahkan gambar ke file DWG adalah kebutuhan rutin ketika Anda perlu memperkaya gambar CAD dengan logo, foto, atau grafik raster. Dalam tutorial ini Anda akan belajar cara **menambahkan gambar ke dwg** secara programatis menggunakan C# dan Aspose.CAD untuk .NET, kemudian opsional mengonversi hasilnya ke PDF. Langkah‑langkahnya diuraikan sehingga Anda dapat menyalin‑tempel setiap bagian ke dalam proyek Anda sendiri.

## Jawaban Cepat
- **Perpustakaan mana yang menangani pekerjaan ini?** Aspose.CAD untuk .NET.
- **Bisakah saya menyematkan file PNG?** Ya – PNG, JPEG, BMP, dan format raster lainnya didukung.
- **Apakah saya memerlukan lisensi untuk pengembangan?** Versi percobaan gratis dapat digunakan untuk pengujian; lisensi komersial diperlukan untuk produksi.
- **Apakah ekspor PDF didukung?** Tentu – Anda dapat mengonversi DWG yang diperbarui ke PDF dalam satu baris.
- **Versi .NET apa yang kompatibel?** .NET Framework 4.6+, .NET Core 3.1+, .NET 5/6/7.

## Apa itu file DWG?

File DWG adalah format biner asli untuk gambar Autodesk AutoCAD, menyimpan geometri vektor, lapisan, dan metadata. Format ini banyak digunakan di bidang arsitektur, teknik, dan konstruksi, dan Aspose.CAD dapat membaca serta menulis format ini tanpa memerlukan AutoCAD terinstal.

## Mengapa menambahkan gambar ke dwg dengan Aspose.CAD?

Aspose.CAD mendukung **lebih dari 50 format input dan output**, dapat memproses file berukuran lebih dari 500 MB tanpa memuat seluruh dokumen ke memori, dan menyediakan API deterministik yang berfungsi di lingkungan server tanpa antarmuka grafis. Hal ini membuat pemrosesan massal gambar DWG menjadi cepat dan dapat diandalkan.

## Prasyarat
- Pengetahuan dasar tentang pemrograman C#.
- Aspose.CAD untuk .NET terinstal. Anda dapat mengunduhnya dari [Aspose.CAD for .NET download page](https://releases.aspose.com/cad/net/). Anda juga dapat menjelajahi produk Aspose lainnya di [Aspose releases page](https://releases.aspose.com/).
- Lingkungan pengembangan seperti Visual Studio 2022 atau yang lebih baru.

## Cara menambahkan gambar ke dwg menggunakan Aspose.CAD?

Muat DWG target, buat objek gambar raster yang menggambarkan foto yang ingin Anda sematkan, tetapkan titik sisip dan vektor skala, lalu lampirkan gambar ke gambar. Akhirnya, simpan DWG yang telah dimodifikasi atau ekspor langsung ke PDF. Seluruh alur kerja hanya memerlukan beberapa panggilan API dan berjalan dalam kurang dari satu detik untuk gambar tipikal 2‑halaman.

### Impor namespace
Sertakan namespace yang menyediakan kelas CAD yang Anda perlukan.

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

### Langkah 1: siapkan direktori dokumen Anda
Siapkan folder yang berisi DWG sumber dan gambar yang ingin Anda sematkan.

```csharp
string MyDir = "Your Document Directory";
```

### Langkah 2: muat file dwg
Kelas `CadImage` mewakili gambar DWG dan menyediakan akses ke entitas, lapisan, serta metadata-nya.

```csharp
string dwgPathToFile = MyDir + "Drawing11.dwg";
CadImage cadImage1 = (CadImage)Image.Load(dwgPathToFile);
```

### Langkah 3: definisikan properti gambar
Buat objek `Image` yang menunjuk ke file raster (mis., PNG) dan tentukan formatnya.

```csharp
CadRasterImageDef cadRasterImageDef = new CadRasterImageDef("road-sign-custom.png", 640, 562);
cadRasterImageDef.ObjectHandle = "A3B4";
```

### Langkah 4: atur titik sisip dwg dan vektor
Tentukan di mana gambar harus muncul di dalam gambar dan bagaimana skalanya. Titik sisip didefinisikan oleh koordinat 2‑D, sementara vektor mengontrol lebar dan tinggi.

```csharp
Cad3DPoint insertionPoint = new Cad3DPoint(26.77, 22.35);
Cad3DPoint uVector = new Cad3DPoint(0.0061565450840500831, 0);
Cad3DPoint vVector = new Cad3DPoint(0, 0.0061565450840500822);
```

### Langkah 5: buat dan konfigurasikan gambar raster
Instansiasi objek `RasterImage`, tetapkan data gambar, dan atur opsi rendering tambahan apa pun.

```csharp
CadRasterImage cadRasterImage = new CadRasterImage(cadRasterImageDef, insertionPoint, uVector, vVector);
cadRasterImage.ImageDefReference = "A3B4";
cadRasterImage.DisplayFlags = 7;
cadRasterImage.ClippingState = 0;
cadRasterImage.ClipBoundaryVertexList.Add(new Cad2DPoint(-0.5, 0.5));
cadRasterImage.ClipBoundaryVertexList.Add(new Cad2DPoint(639.5, 561.5));
```

### Langkah 6: tambahkan gambar ke file dwg
Masukkan gambar raster yang telah dikonfigurasi ke dalam koleksi entitas DWG sehingga menjadi bagian dari gambar.

```csharp
CadImage cadImage = (CadImage)cadImage1;
cadImage.BlockEntities["*Model_Space"].AddEntity(cadRasterImage);

List<CadBaseObject> list = new List<CadBaseObject>(cadImage.Objects);
list.Add(cadRasterImageDef);
cadImage.Objects = list.ToArray();
```

### Langkah 7: simpan sebagai pdf (ekspor dwg ke pdf)
Setelah menyematkan gambar, Anda dapat **mengonversi dwg ke pdf** atau **menyimpan dwg sebagai pdf** dengan satu panggilan. Ini berguna untuk berbagi gambar dengan pemangku kepentingan yang tidak memiliki perangkat lunak CAD.

```csharp
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.VectorRasterizationOptions = cadRasterizationOptions;
cadRasterizationOptions.DrawType = CadDrawTypeMode.UseObjectColor;

cadRasterizationOptions.PageHeight = 1600;
cadRasterizationOptions.PageWidth = 1600;
cadRasterizationOptions.Layouts = new string[] { "Model" };
cadImage1.Save(MyDir + "export2.pdf", pdfOptions);
```

## Cara mengonversi dwg ke pdf setelah menyematkan gambar?

Panggil metode `Save` pada instance `CadImage`, dengan parameter `SaveFormat.Pdf` dan opsional objek `PdfOptions` untuk mengontrol ukuran halaman, rasterisasi, dan metadata. Aspose.CAD mempertahankan gambar raster yang disematkan, lapisan, dan ketebalan garis, menghasilkan representasi PDF yang setia dan dapat dibuka di penampil apa pun. Konversi ini dilakukan dalam satu baris kode.

## Masalah umum dan solusi
- **Gambar muncul di lokasi yang salah** – periksa kembali koordinat titik sisip dan vektor arah; mereka relatif terhadap asal gambar.
- **Gambar besar menyebabkan lonjakan memori** – gunakan opsi `Resize` pada gambar raster sebelum penyisipan, atau gunakan salinan dengan resolusi lebih rendah.
- **Ekspor PDF kehilangan kualitas vektor** – pastikan Anda menyimpan dengan `PdfOptions` yang mempertahankan data vektor; gambar raster selalu disematkan apa adanya.

## Pertanyaan yang Sering Diajukan

**Q: Bisakah saya menggunakan Aspose.CAD untuk .NET dengan bahasa pemrograman lain?**  
A: Perpustakaan inti bersifat khusus .NET, tetapi Aspose menawarkan API setara untuk Java, Python, dan platform lainnya.

**Q: Apakah tersedia versi percobaan gratis untuk Aspose.CAD?**  
A: Ya, Anda dapat menjelajahi versi percobaan gratis di [Aspose free trial page](https://releases.aspose.com/).

**Q: Di mana saya dapat menemukan dokumentasi terperinci untuk Aspose.CAD?**  
A: Dokumentasi tersedia di [Aspose.CAD .NET API reference](https://reference.aspose.com/cad/net/).

**Q: Bagaimana cara memperoleh lisensi sementara untuk Aspose.CAD?**  
A: Kunjungi [temporary license page](https://purchase.aspose.com/temporary-license/) untuk mendapatkan lisensi sementara.

**Q: Apakah ada forum komunitas untuk dukungan Aspose.CAD?**  
A: Ya, Anda dapat mencari dukungan dan berinteraksi dengan komunitas di [Aspose.CAD community forum](https://forum.aspose.com/c/cad/19).

---

**Terakhir Diperbarui:** 2026-08-17  
**Diuji Dengan:** Aspose.CAD 24.11 untuk .NET  
**Penulis:** Aspose

## Tutorial Terkait

- [Mengekspor DWG ke PDF atau Gambar Raster - Panduan Aspose.CAD](/cad/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/)
- [Mengekspor DWG ke Format DXF dalam C# - Tutorial Aspose.CAD](/cad/net/advanced-export-techniques/exporting-dwg-to-dxf/)
- [Mengekspor Tata Letak Spesifik ke PDF - Panduan Aspose.CAD](/cad/net/advanced-export-techniques/exporting-specific-layouts-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}