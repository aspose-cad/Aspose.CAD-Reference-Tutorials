---
title: Menangani Lapisan dalam File DWG dengan C# - Tutorial Aspose.CAD
linktitle: Menangani Lapisan dalam File DWG dengan C#
second_title: Aspose.CAD .NET - Format File CAD dan BIM
description: Pelajari cara menangani lapisan dalam file DWG menggunakan C# dengan Aspose.CAD untuk .NET. Panduan langkah demi langkah untuk manipulasi file CAD yang efisien.
type: docs
weight: 11
url: /id/net/dwg-file-manipulation/support-of-layers/
---
## Perkenalan

Selamat datang di tutorial mendalam kami tentang menangani lapisan dalam file DWG menggunakan C# dengan Aspose.CAD untuk .NET. Aspose.CAD adalah perpustakaan canggih yang memungkinkan pengembang bekerja dengan format file CAD dengan lancar. Dalam tutorial ini, kami akan memandu Anda melalui proses penanganan lapisan dalam file DWG langkah demi langkah.

## Prasyarat

Sebelum kita mendalami tutorialnya, pastikan Anda memiliki prasyarat berikut:

- Pengetahuan dasar bahasa pemrograman C#.
- Visual Studio diinstal pada mesin Anda.
-  Aspose.CAD untuk perpustakaan .NET, yang dapat Anda unduh dari[Situs web Aspose.CAD](https://releases.aspose.com/cad/net/).

## Impor Namespace

Untuk memulai, impor namespace yang diperlukan ke proyek C# Anda. Namespace ini menyediakan fungsionalitas yang diperlukan untuk bekerja dengan file CAD.

```csharp
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
```

## Langkah 1: Muat File DWG

Mulailah dengan memuat file DWG ke aplikasi C# Anda menggunakan perpustakaan Aspose.CAD.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "for_layers_test.dwf";

using (Aspose.CAD.Image image = Aspose.CAD.Image.Load(sourceFilePath))
{
    // Kode Anda untuk langkah selanjutnya ada di sini
}
```

## Langkah 2: Konfigurasikan Opsi Rasterisasi

 Buat sebuah contoh dari`CadRasterizationOptions` dan atur propertinya untuk menentukan bagaimana file DWG harus dirasterisasi.

```csharp
Aspose.CAD.ImageOptions.CadRasterizationOptions rasterizationOptions = new Aspose.CAD.ImageOptions.CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
```

## Langkah 3: Tentukan Lapisan

Tambahkan lapisan yang diinginkan ke opsi rasterisasi. Dalam contoh ini, kami telah menambahkan "LayerA."

```csharp
rasterizationOptions.Layers = new string[] { "LayerA" };
```

## Langkah 4: Konfigurasikan Opsi Ekspor Gambar

 Buat opsi ekspor gambar yang diperlukan. Di sini, kami menggunakan`JpegOptions` untuk mengekspor ke JPEG.

```csharp
JpegOptions jpegOptions = new JpegOptions();
jpegOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Langkah 5: Simpan Gambar yang Diekspor

Tentukan jalur keluaran dan simpan file DWG raster sebagai JPEG.

```csharp
MyDir = MyDir + "for_layers_test.jpg";
image.Save(MyDir, jpegOptions);
```

Sekarang Anda telah berhasil menangani lapisan dalam file DWG menggunakan C# dengan Aspose.CAD untuk .NET.

## Kesimpulan

Dalam tutorial ini, kita mempelajari proses penanganan lapisan dalam file DWG menggunakan C# dan perpustakaan Aspose.CAD. Dengan mengikuti langkah-langkah ini, Anda dapat bekerja secara efisien dengan file CAD di aplikasi .NET Anda.

## FAQ

### Q1: Dapatkah saya menangani beberapa lapisan secara bersamaan?

 A1: Ya, Anda bisa. Cukup tambahkan nama layer ke`rasterizationOptions.Layers` Himpunan.

### Q2: Apakah versi uji coba Aspose.CAD tersedia?

 A2: Ya, Anda bisa mendapatkan versi uji coba gratis dari[Di Sini](https://releases.aspose.com/).

### Q3: Di mana saya dapat menemukan dokumentasinya?

 A3: Dokumentasi tersedia[Di Sini](https://reference.aspose.com/cad/net/).

### Q4: Bagaimana cara mendapatkan dukungan untuk Aspose.CAD?

 A4: Anda dapat mencari dukungan di[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19).

### Q5: Apa saja pilihan lisensi untuk Aspose.CAD?

 A5: Anda dapat menjelajahi opsi lisensi dan detail pembelian[Di Sini](https://purchase.aspose.com/buy).