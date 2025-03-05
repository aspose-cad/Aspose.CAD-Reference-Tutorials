---
title: Mengekspor DWG ke PDF atau Gambar Raster - Panduan Aspose.CAD
linktitle: Mengekspor DWG ke PDF atau Gambar Raster
second_title: Aspose.CAD .NET - Format File CAD dan BIM
description: Jelajahi panduan komprehensif tentang mengekspor DWG ke PDF atau gambar raster menggunakan Aspose.CAD untuk .NET. Pelajari langkah-langkahnya, prasyaratnya, dan pelajari langsung perpustakaan canggih ini.
type: docs
weight: 11
url: /id/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/
---
## Perkenalan

Apakah Anda ingin mengonversi file DWG ke PDF atau gambar raster dengan lancar di aplikasi .NET Anda? Tidak perlu mencari lagi! Panduan langkah demi langkah ini akan memandu Anda melalui proses menggunakan pustaka Aspose.CAD untuk .NET yang kuat. Baik Anda seorang pengembang berpengalaman atau baru memulai, tutorial ini melayani semua tingkat keahlian.

## Prasyarat

Sebelum kita masuk ke tutorialnya, pastikan Anda memiliki yang berikut ini:

- Pemahaman dasar tentang pemrograman .NET.
-  Aspose.CAD untuk perpustakaan .NET diinstal. Jika tidak, unduh[Di Sini](https://releases.aspose.com/cad/net/).
- Lingkungan pengembangan terintegrasi (IDE) favorit Anda disiapkan untuk pengembangan .NET.

## Impor Namespace

Mari kita mulai dengan mengimpor namespace yang diperlukan dalam proyek .NET Anda. Ini memastikan bahwa Anda memiliki akses ke fungsionalitas Aspose.CAD dalam kode Anda.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
```

## Langkah 1: Muat File DWG

Mulailah dengan memuat file DWG yang ingin Anda konversi. Ganti "Direktori Dokumen Anda" dengan jalur ke file DWG Anda.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Bottom_plate.dwg";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Kode Anda untuk memuat DWG ada di sini
}
```

## Langkah 2: Siapkan Ekspor PDF

Sekarang, mari konfigurasikan pengaturan ekspor PDF. Contoh ini menunjukkan cara mengatur tata letak dan menangani konversi unit.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.Layouts = new string[] { "Model" };

// Periksa dan tentukan sistem satuannya
bool currentUnitIsMetric = false;
double currentUnitCoefficient = 1.0;
DefineUnitSystem(cadImage.UnitType, out currentUnitIsMetric, out currentUnitCoefficient);

// Kode Anda untuk menyiapkan ekspor PDF ada di sini
```

## Langkah 3: Ekspor ke PDF

Jalankan ekspor ke PDF menggunakan pengaturan yang dikonfigurasi.

```csharp
PdfOptions pdfOptions = new PdfOptions
{
    VectorRasterizationOptions = rasterizationOptions
};

cadImage.Save(outPath, pdfOptions);
```

## Langkah 4: Ekspor ke Gambar Raster

Perluas fungsionalitas untuk mengekspor ke gambar raster, seperti PNG.

```csharp
// Ukuran A4 pada 300 DPI - 2480 x 3508
rasterizationOptions.PageHeight = 3508;
rasterizationOptions.PageWidth = 2480;

PngOptions pngOptions = new PngOptions
{
    VectorRasterizationOptions = rasterizationOptions
};

cadImage.Save(outPath.Replace("pdf", "png"), pngOptions);
```

## Kesimpulan

Selamat! Anda telah berhasil mempelajari cara menggunakan Aspose.CAD untuk .NET untuk mengekspor file DWG ke PDF dan gambar raster. Pustaka yang kuat ini menyederhanakan proses, menjadikannya efisien dan ramah pengembang.

## FAQ

### Q1: Dapatkah saya menggunakan Aspose.CAD untuk .NET dalam proyek komersial saya?

 A1: Ya, Anda bisa. Mengunjungi[pembelian.aspose.com/buy](https://purchase.aspose.com/buy) untuk rincian perizinan.

### Q2: Apakah tersedia uji coba gratis?

 A2: Tentu saja! Dapatkan uji coba gratis Anda[Di Sini](https://releases.aspose.com/).

### Q3: Bagaimana saya bisa mendapatkan dukungan untuk Aspose.CAD untuk .NET?

 A3: Pergilah ke[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19) untuk dukungan masyarakat.

### Q4: Bisakah saya mendapatkan lisensi sementara untuk tujuan pengujian?

 A4: Ya, Anda bisa mendapatkan lisensi sementara[Di Sini](https://purchase.aspose.com/temporary-license/).

### Q5: Di mana saya dapat menemukan dokumentasi detailnya?

 A5: Dokumentasi tersedia di[Asumsikan.CAD](https://reference.aspose.com/cad/net/).