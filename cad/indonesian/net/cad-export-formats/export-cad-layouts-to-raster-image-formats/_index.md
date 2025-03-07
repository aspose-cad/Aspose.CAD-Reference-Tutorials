---
title: Ekspor Tata Letak CAD ke Format Gambar Raster di Aspose.CAD untuk .NET
linktitle: Ekspor Tata Letak CAD ke Format Gambar Raster
second_title: Aspose.CAD .NET - Format File CAD dan BIM
description: Pelajari cara mengekspor tata letak CAD ke gambar raster menggunakan Aspose.CAD untuk .NET. Ikuti panduan langkah demi langkah kami untuk konversi yang lancar.
weight: 10
url: /id/net/cad-export-formats/export-cad-layouts-to-raster-image-formats/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ekspor Tata Letak CAD ke Format Gambar Raster di Aspose.CAD untuk .NET

## Perkenalan

Apakah Anda ingin mengonversi tata letak CAD ke format gambar raster secara efisien menggunakan Aspose.CAD untuk .NET? Panduan langkah demi langkah ini akan memandu Anda melalui prosesnya, memberikan petunjuk mendetail dan cuplikan kode untuk membuat tugas menjadi lancar. Baik Anda seorang pengembang berpengalaman atau pendatang baru di Aspose.CAD, tutorial ini melayani semua tingkat keahlian.

## Prasyarat

Sebelum masuk ke tutorial, pastikan Anda memiliki hal berikut:

- Aspose.CAD untuk Perpustakaan .NET: Pastikan Anda telah menginstal perpustakaan Aspose.CAD. Jika belum, Anda dapat mendownloadnya dari[Situs web Aspose.CAD](https://releases.aspose.com/cad/net/).

- File Gambar CAD: Siapkan file gambar CAD (misalnya conic_pyramid.dxf) yang ingin Anda konversi ke format gambar raster.

## Impor Namespace

Dalam proyek .NET Anda, impor namespace yang diperlukan untuk memanfaatkan fungsionalitas Aspose.CAD. Sertakan namespace berikut di awal kode Anda:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Langkah 1: Muat Gambar CAD

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

// Muat gambar CAD dalam contoh Gambar
using (var image = Image.Load(sourceFilePath))
{
    // Kode Anda untuk memuat gambar CAD ada di sini
}
```

## Langkah 2: Buat Opsi CadRasterization

```csharp
// Buat sebuah instance dari CadRasterizationOptions
var rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 500;
rasterizationOptions.PageHeight = 500;
```

## Langkah 3: Tentukan Lapisan

```csharp
// Tambahkan nama lapisan ke daftar lapisan CadRasterizationOptions
rasterizationOptions.Layers = new string[] { "LayerA" };
```

## Langkah 4: Buat JpegOptions

```csharp
// Buat instance JpegOptions (atau ImageOptions apa pun untuk format raster)
var options = new JpegOptions();
options.VectorRasterizationOptions = rasterizationOptions;
```

## Langkah 5: Ekspor ke Format Jpeg

```csharp
// Ekspor setiap lapisan ke format JPEG
MyDir = MyDir + "CADLayersToRasterImageFormats_out.jpg";
image.Save(MyDir, options);
```

## Langkah Tambahan: Konversi Semua Lapisan

Jika Anda ingin mengonversi semua lapisan, gunakan metode berikut:

```csharp
ConvertAllLayersToRasterImageFormats();
```

Metode ini mengulangi semua lapisan dalam gambar CAD, mengekspor setiap lapisan ke file Jpeg terpisah.

## Kesimpulan

Selamat! Anda telah berhasil mempelajari cara mengekspor tata letak CAD ke format gambar raster menggunakan Aspose.CAD untuk .NET. Tutorial ini memberikan panduan komprehensif bagi pengembang yang mencari solusi efisien dan andal untuk konversi CAD.

## FAQ

### Q1: Bisakah saya menggunakan format gambar lain untuk mengekspor?

 A1: Ya, Anda bisa. Ganti saja`JpegOptions` dengan pilihan format yang diinginkan, seperti`PngOptions` atau`BmpOptions`.

### Q2: Apakah ada versi uji coba yang tersedia?

 A2: Ya, Anda dapat menjelajahi fungsionalitas Aspose.CAD dengan mengunduh versi uji coba[Di Sini](https://releases.aspose.com/).

### Q3: Bagaimana saya bisa mendapatkan dukungan untuk Aspose.CAD?

 A3: Kunjungi Aspose.CAD[forum](https://forum.aspose.com/c/cad/19) untuk dukungan komunitas atau pertimbangkan untuk membeli lisensi untuk dukungan khusus.

### Q4: Apakah lisensi sementara tersedia?

 A4: Ya, Anda bisa mendapatkan lisensi sementara[Di Sini](https://purchase.aspose.com/temporary-license/).

### Q5: Di mana saya dapat menemukan dokumentasinya?

 A5: Lihat dokumentasi rinci[Di Sini](https://reference.aspose.com/cad/net/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
