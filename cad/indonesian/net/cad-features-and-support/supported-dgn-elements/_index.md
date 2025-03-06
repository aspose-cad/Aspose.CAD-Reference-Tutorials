---
title: Elemen DGN yang didukung di Aspose.CAD untuk .NET
linktitle: Elemen DGN yang Didukung
second_title: Aspose.CAD .NET - Format File CAD dan BIM
description: Jelajahi Aspose.CAD untuk fitur canggih .NET untuk menangani file DGN. Ikuti panduan langkah demi langkah kami untuk bekerja secara lancar dengan elemen 2D dan 3D.
weight: 18
url: /id/net/cad-features-and-support/supported-dgn-elements/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Elemen DGN yang didukung di Aspose.CAD untuk .NET

## Perkenalan

Apakah Anda seorang pengembang .NET yang ingin bekerja dengan file DGN dengan lancar? Aspose.CAD untuk .NET memberikan solusi tangguh untuk menangani file DGN secara efisien. Dalam tutorial ini, kami akan mempelajari elemen DGN yang didukung, memandu Anda melalui proses bekerja dengan Aspose.CAD untuk .NET.

## Prasyarat

Sebelum kita mulai, pastikan Anda memiliki hal berikut:

- Pengetahuan dasar tentang pemrograman .NET.
- Visual Studio diinstal pada mesin Anda.
-  Aspose.CAD untuk perpustakaan .NET, yang dapat Anda unduh[Di Sini](https://releases.aspose.com/cad/net/).

## Impor Namespace

Untuk memulai proyek Anda, impor namespace yang diperlukan ke aplikasi .NET Anda. Langkah ini memastikan bahwa Anda memiliki akses ke fungsionalitas yang disediakan oleh Aspose.CAD untuk .NET.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Dgn;
using Aspose.CAD.FileFormats.Dgn.DgnElements;
```

## Langkah 1: Muat File DGN

Mulailah dengan memuat file DGN yang ada sebagai CadImage di aplikasi .NET Anda.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (DgnImage dgnImage = (DgnImage)Image.Load(sourceFilePath))
{
    // Kode Anda di sini
}
```

## Langkah 2: Iterasi Melalui Elemen DGN

Iterasi elemen DGN menggunakan loop foreach. Aspose.CAD untuk .NET menyediakan berbagai tipe elemen DGN yang dapat Anda gunakan.

```csharp
foreach (DgnDrawingElementBase element in dgnImage.Elements)
{
    // Kode Anda di sini
}
```

## Langkah 3: Tangani Entitas yang Sebelumnya Didukung

Tangani entitas 2D yang sebelumnya didukung, yang kini juga didukung untuk 3D.

```csharp
switch (element.Metadata.Type)
{
    case DgnElementType.Line:
    case DgnElementType.Ellipse:
    case DgnElementType.Curve:
    // Kasus tambahan
        {
            // Kode Anda di sini
            break;
        }
}
```

## Langkah 4: Tangani Entitas 3D yang Didukung

Tangani entitas 3D yang didukung yang disediakan oleh Aspose.CAD untuk .NET.

```csharp
switch (element.Metadata.Type)
{
    case DgnElementType.SolidHeader3D:
    case DgnElementType.Cone:
    case DgnElementType.CellHeader:
        {
            // Kode Anda di sini
            break;
        }
}
```

## Langkah 5: Ekspor dan Simpan

Terakhir, ekspor file DGN yang dimodifikasi ke gambar raster dan simpan ke direktori yang ditentukan.

```csharp
Console.WriteLine("\nThe DGN file exported successfully to raster image.\nFile saved at " + MyDir);
```

## Kesimpulan

Dalam tutorial ini, kita mengeksplorasi kemampuan Aspose.CAD untuk .NET dalam menangani dan memanipulasi file DGN. Dengan mengikuti panduan langkah demi langkah, Anda dapat bekerja secara efisien dengan elemen DGN yang didukung, baik itu entitas 2D atau 3D. Aspose.CAD untuk .NET memberdayakan Anda untuk mengintegrasikan pemrosesan file DGN dengan lancar ke dalam aplikasi .NET Anda.

## FAQ

### Q1: Di mana saya dapat menemukan dokumentasi Aspose.CAD untuk .NET?

 A1: Anda dapat menemukan dokumentasinya[Di Sini](https://reference.aspose.com/cad/net/).

### Q2: Bagaimana cara mengunduh Aspose.CAD untuk .NET?

 A2: Anda dapat mengunduh perpustakaan[Di Sini](https://releases.aspose.com/cad/net/).

### Q3: Apakah ada uji coba gratis yang tersedia untuk Aspose.CAD untuk .NET?

 A3: Ya, Anda dapat mengakses uji coba gratis[Di Sini](https://releases.aspose.com/).

### Q4: Di mana saya bisa mendapatkan lisensi sementara Aspose.CAD untuk .NET?

 A4: Lisensi sementara tersedia[Di Sini](https://purchase.aspose.com/temporary-license/).

### Q5: Butuh bantuan atau punya pertanyaan?

 A5: Kunjungi komunitas Aspose.CAD untuk .NET[forum dukungan](https://forum.aspose.com/c/cad/19).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
