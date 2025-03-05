---
title: Dukungan untuk DGN V7 di Aspose.CAD untuk .NET
linktitle: Dukungan untuk DGN V7
second_title: Aspose.CAD .NET - Format File CAD dan BIM
description: Jelajahi Aspose.CAD untuk dukungan .NET yang lancar untuk DGN V7. Konversikan file DGN menjadi gambar raster dengan mudah dengan panduan langkah demi langkah.
type: docs
weight: 19
url: /id/net/cad-features-and-support/support-for-dgn-v7/
---
## Perkenalan

Dalam bidang pengembangan .NET, Aspose.CAD menonjol sebagai perpustakaan yang kuat untuk menangani file Computer-Aided Design (CAD). Tutorial ini mempelajari fitur spesifik Aspose.CAD untuk .NET—dukungan untuk file DGN V7. DGN, kependekan dari Design, adalah format file yang banyak digunakan dalam domain CAD. Aspose.CAD menyederhanakan proses bekerja dengan file DGN V7, menawarkan pengalaman yang mulus kepada pengembang.

## Prasyarat

Sebelum kita mendalami penerapannya, pastikan Anda memiliki prasyarat berikut:

-  Aspose.CAD untuk .NET: Pastikan Anda telah menginstal perpustakaan Aspose.CAD. Anda dapat mengunduhnya dari[situs web](https://releases.aspose.com/cad/net/).

- Lingkungan Pengembangan: Siapkan lingkungan pengembangan .NET yang berfungsi, termasuk Visual Studio atau IDE pilihan lainnya.

Sekarang setelah prasyaratnya diurutkan, mari kita jelajahi cara memanfaatkan dukungan untuk DGN V7 di Aspose.CAD untuk .NET.

## Impor Namespace

Mulailah dengan mengimpor namespace yang diperlukan untuk mengakses fungsionalitas Aspose.CAD:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Langkah 1: Muat File DGN

 Mulailah dengan memuat file DGN yang ada sebagai a`CadImage` Mengganti`"Your Document Directory"` Dan`"Nikon_D90_Camera.dgn"` dengan jalur direktori dan nama file yang sesuai.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Kode untuk langkah selanjutnya ada di sini...
}
```

## Langkah 2: Konfigurasikan Opsi Rasterisasi

 Membuat`CadRasterizationOptions` objek untuk mendefinisikan dan mengatur berbagai properti yang terkait dengan rasterisasi.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions
{
    PageWidth = 600,
    PageHeight = 300,
    NoScaling = true,
    AutomaticLayoutsScaling = false
};
```

## Langkah 3: Tetapkan Opsi Rasterisasi Vektor

 Membuat`JpegOptions` objek karena kami bermaksud untuk mengkonversi file DGN ke JPEG. Tetapkan yang dibuat sebelumnya`CadRasterizationOptions` keberatan dengan hal itu.

```csharp
ImageOptionsBase options = new JpegOptions
{
    VectorRasterizationOptions = rasterizationOptions
};
```

## Langkah 4: Simpan Gambar Rasterisasi

 Hubungi`Save` metode`CadImage` objek kelas untuk mengekspor file DGN ke gambar raster, dalam hal ini JPEG.

```csharp
cadImage.Save(MyDir + "ExportDGNToRasterImage_out.jpeg", options);
```

Setelah langkah-langkah ini selesai, file DGN berhasil diekspor ke gambar raster.

## Kesimpulan

Dalam tutorial ini, kami menjelajahi dukungan lancar untuk DGN V7 di Aspose.CAD untuk .NET. Dengan mengikuti panduan langkah demi langkah, pengembang dapat dengan mudah mengonversi file DGN menjadi gambar raster, memperluas kemampuan aplikasi .NET mereka.

## FAQ

### Q1: Apakah Aspose.CAD kompatibel dengan spesifikasi DGN V7 terbaru?

A1: Ya, Aspose.CAD dirancang untuk menangani file DGN V7 dengan lancar, memastikan kompatibilitas dengan spesifikasi terbaru.

### Q2: Dapatkah saya menyesuaikan opsi rasterisasi untuk konversi file DGN?

 A2: Tentu saja. Tutorial ini menunjukkan cara membuat dan mengkonfigurasi`CadRasterizationOptions` untuk menyesuaikan proses konversi.

### Q3: Apakah ada format output lain yang didukung selain JPEG?

A3: Ya, Aspose.CAD mendukung berbagai format keluaran. Anda dapat menjelajahi dokumentasi untuk daftar lengkap.

### Q4: Bagaimana saya bisa mendapatkan dukungan untuk pertanyaan terkait Aspose.CAD?

 A4: Kunjungi[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19) untuk dukungan dan diskusi komunitas.

### Q5: Apakah ada uji coba gratis yang tersedia untuk Aspose.CAD untuk .NET?

 A5: Ya, Anda dapat mengakses uji coba gratis[Di Sini](https://releases.aspose.com/).