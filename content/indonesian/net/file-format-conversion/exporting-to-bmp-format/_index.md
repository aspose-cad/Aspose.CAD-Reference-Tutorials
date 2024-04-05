---
title: Mengekspor ke Format BMP - Tutorial Aspose.CAD
linktitle: Mengekspor ke Format BMP
second_title: Aspose.CAD .NET - Format File CAD dan BIM
description: Jelajahi dunia ekspor gambar 3D yang mulus ke BMP menggunakan Aspose.CAD untuk .NET. Ikuti tutorial kami untuk pengalaman tanpa kerumitan.
type: docs
weight: 11
url: /id/net/file-format-conversion/exporting-to-bmp-format/
---
## Perkenalan

Dalam dunia pengembangan perangkat lunak yang dinamis, Aspose.CAD untuk .NET menonjol sebagai alat yang ampuh untuk menangani file Computer-Aided Design (CAD). Jika Anda ingin mengekspor gambar CAD ke format BMP yang banyak digunakan, tutorial ini adalah panduan Anda. Dalam panduan langkah demi langkah ini, kita akan menjelajahi proses mengekspor gambar 3D ke BMP menggunakan Aspose.CAD untuk .NET. Ayo selami!

## Prasyarat

Sebelum kita memulai tutorial ini, pastikan Anda memiliki prasyarat berikut:

-  Aspose.CAD untuk .NET: Unduh dan instal perpustakaan Aspose.CAD dari[Di Sini](https://releases.aspose.com/cad/net/).
- Lingkungan Pengembangan: Siapkan lingkungan pengembangan .NET.
- File CAD: Siapkan file CAD untuk diekspor. Untuk contoh ini, kita akan menggunakan "18-12-11 9644 - site.dwf."

## Impor Namespace

Di proyek .NET Anda, pastikan untuk mengimpor namespace yang diperlukan:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
```

## Langkah 1: Muat Gambar CAD

Mulailah dengan memuat gambar CAD ke dalam proyek Anda. Ganti "Direktori Dokumen Anda" dengan jalur direktori sebenarnya.

```csharp
string MyDir = "Your Document Directory";
string inputFile = MyDir + "18-12-11 9644 - site.dwf";

using (Image image = Image.Load(inputFile))
{
    // Kode Anda untuk memuat gambar ada di sini
}
```

## Langkah 2: Konfigurasikan Opsi Ekspor BMP

Siapkan opsi ekspor BMP, termasuk opsi rasterisasi vektor untuk file CAD.

```csharp
BmpOptions bmpOptions = new BmpOptions();
var dwfRasterizationOptions = new CadRasterizationOptions();
bmpOptions.VectorRasterizationOptions = dwfRasterizationOptions;

dwfRasterizationOptions.PageHeight = 500;
dwfRasterizationOptions.PageWidth = 500;
```

## Langkah 3: Ekspor ke BMP

Jalankan proses ekspor, tentukan jalur keluaran untuk file BMP.

```csharp
string outPath = MyDir + "18-12-11 9644 - site.bmp";
image.Save(outPath, bmpOptions);
```

## Kesimpulan

Selamat! Anda telah berhasil mengekspor gambar 3D ke BMP menggunakan Aspose.CAD untuk .NET. Tutorial ini memberikan gambaran sekilas tentang keserbagunaan Aspose.CAD, membuat tugas-tugas kompleks terasa mudah.

## FAQ

### Q1: Bisakah saya menggunakan Aspose.CAD untuk .NET dengan format file CAD apa pun?

A1: Ya, Aspose.CAD mendukung berbagai format file CAD, memberikan fleksibilitas dalam proyek Anda.

### Q2: Apakah lisensi sementara tersedia untuk tujuan pengujian?

 A2: Tentu saja! Anda bisa mendapatkan lisensi sementara[Di Sini](https://purchase.aspose.com/temporary-license/) untuk evaluasi.

### Q3: Di mana saya dapat menemukan dokumentasi komprehensif untuk Aspose.CAD?

 A3: Lihat dokumentasi[Di Sini](https://reference.aspose.com/cad/net/) untuk informasi rinci dan contoh.

### Q4: Bagaimana cara saya mencari dukungan atau terhubung dengan komunitas?

 A4: Kunjungi forum Aspose.CAD[Di Sini](https://forum.aspose.com/c/cad/19) untuk bertanya dan terlibat dengan komunitas.

### Q5: Bisakah saya membeli Aspose.CAD untuk .NET?

 A5: Ya, Anda dapat membeli Aspose.CAD[Di Sini](https://purchase.aspose.com/buy) untuk membuka potensi penuhnya untuk proyek Anda.
