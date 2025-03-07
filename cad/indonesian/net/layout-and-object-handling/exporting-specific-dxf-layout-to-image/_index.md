---
title: Mengekspor Tata Letak DXF Tertentu ke Gambar - Tutorial Aspose.CAD
linktitle: Mengekspor Tata Letak DXF Tertentu ke Gambar
second_title: Aspose.CAD .NET - Format File CAD dan BIM
description: Jelajahi panduan langkah demi langkah tentang penggunaan Aspose.CAD untuk .NET guna mengekspor tata letak DXF tertentu ke gambar. Maksimalkan efisiensi pengembangan .NET Anda dengan tutorial hebat ini.
weight: 10
url: /id/net/layout-and-object-handling/exporting-specific-dxf-layout-to-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Mengekspor Tata Letak DXF Tertentu ke Gambar - Tutorial Aspose.CAD

## Perkenalan

Dalam bidang pengembangan .NET, Aspose.CAD menonjol sebagai alat yang ampuh untuk menangani file Computer-Aided Design (CAD). Secara khusus, ini menyediakan fungsionalitas komprehensif untuk mengekspor tata letak DXF tertentu ke gambar. Tutorial ini akan memandu Anda melalui proses langkah demi langkah, memungkinkan Anda memanfaatkan kemampuan Aspose.CAD dengan mudah.

## Prasyarat

Sebelum masuk ke tutorial, pastikan Anda memiliki prasyarat berikut:

-  Perpustakaan Aspose.CAD: Unduh dan instal perpustakaan Aspose.CAD dari[halaman rilis](https://releases.aspose.com/cad/net/).

- Lingkungan Pengembangan: Pastikan Anda telah menyiapkan lingkungan pengembangan .NET di mesin Anda.

## Impor Namespace

Di proyek .NET Anda, mulailah dengan mengimpor namespace yang diperlukan untuk mengakses fungsionalitas yang disediakan oleh Aspose.CAD:

```csharp
using System;
```

## Langkah 1: Siapkan Proyek Anda

Buat proyek .NET baru atau buka proyek yang sudah ada di mana Anda berencana untuk mengimplementasikan fungsionalitas Aspose.CAD.

## Langkah 2: Muat Gambar CAD

Gunakan kode berikut untuk memuat gambar CAD dari jalur file yang Anda tentukan:

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "for_layers_test.dwf";

using (var image = (Aspose.CAD.FileFormats.Cad.CadImage)Aspose.CAD.Image.Load(sourceFilePath))
{
    // Kode Anda untuk langkah selanjutnya akan ditempatkan di sini.
}
```

## Langkah 3: Konfigurasikan Opsi Rasterisasi

Siapkan opsi rasterisasi, tentukan lebar dan tinggi halaman:

```csharp
var rasterizationOptions = new Aspose.CAD.ImageOptions.CadRasterizationOptions();
rasterizationOptions.PageWidth = 500;
rasterizationOptions.PageHeight = 500;
```

## Langkah 4: Ulangi Lapisan

Ambil lapisan dari gambar CAD dan ulangi lapisan tersebut:

```csharp
var layersList = image.Layers;
foreach (var layerName in layersList.GetLayersNames())
{
    // Kode Anda untuk langkah selanjutnya akan ditempatkan di sini.
}
```

## Langkah 5: Ekspor Lapisan ke Gambar

Untuk setiap lapisan, ekspor ke gambar JPEG menggunakan opsi yang dikonfigurasi:

```csharp
rasterizationOptions.Layers = new string[] { layerName };
var options = new Aspose.CAD.ImageOptions.JpegOptions();
options.VectorRasterizationOptions = rasterizationOptions;
image.Save(layerName + "_out.jpg", options);
```

Ulangi langkah ini untuk setiap lapisan pada gambar CAD.

## Kesimpulan

Selamat! Anda telah berhasil mempelajari cara mengekspor tata letak DXF tertentu ke gambar menggunakan Aspose.CAD di lingkungan .NET. Tutorial ini telah membekali Anda dengan langkah-langkah penting untuk memanfaatkan perpustakaan canggih ini secara maksimal.

## FAQ

### Q1: Dapatkah saya menggunakan Aspose.CAD dengan kerangka .NET lainnya?

A1: Ya, Aspose.CAD kompatibel dengan berbagai kerangka .NET, memberikan fleksibilitas untuk kebutuhan pengembangan Anda.

### Q2: Apakah lisensi sementara tersedia untuk Aspose.CAD?

 A2: Ya, Anda bisa mendapatkan lisensi sementara untuk Aspose.CAD dari[Di Sini](https://purchase.aspose.com/temporary-license/).

### Q3: Bagaimana saya bisa mendapatkan dukungan untuk Aspose.CAD?

 A3: Kunjungi[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19) untuk mendapatkan dukungan dan bantuan masyarakat.

### Q4: Apakah ada uji coba gratis yang tersedia untuk Aspose.CAD?

 A4: Ya, Anda dapat menjelajahi uji coba gratis Aspose.CAD[Di Sini](https://releases.aspose.com/).

### Q5: Di mana saya dapat menemukan dokumentasi terperinci untuk Aspose.CAD?

 A5: Lihat secara komprehensif[Dokumentasi Aspose.CAD](https://reference.aspose.com/cad/net/) untuk informasi mendalam.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
