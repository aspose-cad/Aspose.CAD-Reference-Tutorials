---
title: Mengimpor Gambar ke File DWG dengan C# - Panduan Aspose.CAD
linktitle: Mengimpor Gambar ke File DWG dengan C#
second_title: Aspose.CAD .NET - Format File CAD dan BIM
description: Pelajari cara mengimpor gambar ke file DWG menggunakan C# dengan Aspose.CAD untuk .NET. Ikuti panduan langkah demi langkah kami untuk integrasi yang lancar.
weight: 11
url: /id/net/image-manipulation-and-rendering/importing-images-into-dwg/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Mengimpor Gambar ke File DWG dengan C# - Panduan Aspose.CAD

## Perkenalan

Dalam bidang desain berbantuan komputer (CAD), memasukkan gambar ke dalam file DWG adalah tugas yang umum dan penting. Aspose.CAD untuk .NET menyediakan seperangkat alat canggih untuk menyederhanakan proses ini, sehingga dapat diakses oleh pengembang C#. Dalam tutorial ini, kita akan mempelajari cara mengimpor gambar ke file DWG langkah demi langkah.

## Prasyarat

Sebelum mendalami panduan ini, pastikan Anda memiliki hal berikut:

- Pengetahuan dasar tentang pemrograman C#.
-  Aspose.CAD untuk .NET diinstal. Anda dapat mengunduhnya[Di Sini](https://releases.aspose.com/cad/net/).
- Lingkungan pengembangan telah disiapkan.

## Impor Namespace

Pastikan untuk menyertakan namespace yang diperlukan dalam proyek C# Anda:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## Langkah 1: Siapkan Direktori Dokumen Anda

```csharp
string MyDir = "Your Document Directory";
```

## Langkah 2: Muat File DWG

```csharp
string dwgPathToFile = MyDir + "Drawing11.dwg";
CadImage cadImage1 = (CadImage)Image.Load(dwgPathToFile);
```

## Langkah 3: Tentukan Properti Gambar

```csharp
CadRasterImageDef cadRasterImageDef = new CadRasterImageDef("road-sign-custom.png", 640, 562);
cadRasterImageDef.ObjectHandle = "A3B4";
```

## Langkah 4: Tetapkan Titik Penyisipan dan Vektor

```csharp
Cad3DPoint insertionPoint = new Cad3DPoint(26.77, 22.35);
Cad3DPoint uVector = new Cad3DPoint(0.0061565450840500831, 0);
Cad3DPoint vVector = new Cad3DPoint(0, 0.0061565450840500822);
```

## Langkah 5: Buat dan Konfigurasikan Gambar Raster

```csharp
CadRasterImage cadRasterImage = new CadRasterImage(cadRasterImageDef, insertionPoint, uVector, vVector);
cadRasterImage.ImageDefReference = "A3B4";
cadRasterImage.DisplayFlags = 7;
cadRasterImage.ClippingState = 0;
cadRasterImage.ClipBoundaryVertexList.Add(new Cad2DPoint(-0.5, 0.5));
cadRasterImage.ClipBoundaryVertexList.Add(new Cad2DPoint(639.5, 561.5));
```

## Langkah 6: Tambahkan Gambar ke File DWG

```csharp
CadImage cadImage = (CadImage)cadImage1;
cadImage.BlockEntities["*Model_Space"].AddEntity(cadRasterImage);

List<CadBaseObject> list = new List<CadBaseObject>(cadImage.Objects);
list.Add(cadRasterImageDef);
cadImage.Objects = list.ToArray();
```

## Langkah 7: Simpan sebagai PDF

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

## Kesimpulan

Mengintegrasikan gambar ke dalam file DWG menggunakan C# dan Aspose.CAD untuk .NET adalah proses yang mulus, memberdayakan pengembang untuk menyempurnakan proyek CAD mereka dengan elemen visual dengan mudah.

## FAQ

### Q1: Bisakah saya menggunakan Aspose.CAD untuk .NET dengan bahasa pemrograman lain?

A1: Aspose.CAD terutama dirancang untuk .NET, tetapi Aspose menyediakan perpustakaan untuk berbagai bahasa pemrograman.

### Q2: Apakah uji coba gratis tersedia untuk Aspose.CAD untuk .NET?

 A2: Ya, Anda dapat menjelajahi uji coba gratis[Di Sini](https://releases.aspose.com/).

### Q3: Di mana saya dapat menemukan dokumentasi terperinci untuk Aspose.CAD?

 A3: Dokumentasi tersedia[Di Sini](https://reference.aspose.com/cad/net/).

### Q4: Bagaimana cara mendapatkan lisensi sementara Aspose.CAD untuk .NET?

 A4: Kunjungi[Link ini](https://purchase.aspose.com/temporary-license/) untuk mendapatkan izin sementara.

### Q5: Apakah ada forum komunitas untuk dukungan Aspose.CAD?

 A5: Ya, Anda dapat mencari dukungan dan terlibat dengan komunitas[Di Sini](https://forum.aspose.com/c/cad/19).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
