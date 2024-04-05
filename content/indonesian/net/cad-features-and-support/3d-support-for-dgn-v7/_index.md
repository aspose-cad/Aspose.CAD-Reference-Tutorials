---
title: Dukungan 3D untuk DGN V7 di Aspose.CAD untuk .NET
linktitle: Dukungan 3D untuk DGN V7
second_title: Aspose.CAD .NET - Format File CAD dan BIM
description: Jelajahi kekuatan dukungan 3D untuk file DGN V7 di Aspose.CAD untuk .NET. Ikuti panduan langkah demi langkah kami untuk mengintegrasikan dan memanipulasi file CAD dengan mudah.
type: docs
weight: 10
url: /id/net/cad-features-and-support/3d-support-for-dgn-v7/
---
## Perkenalan

Dalam dunia pengembangan perangkat lunak yang dinamis, memiliki kemampuan untuk mengintegrasikan dan memanipulasi data 3D dengan lancar sangatlah penting. Aspose.CAD untuk .NET memberdayakan pengembang dengan seperangkat alat canggih untuk menangani file CAD secara efisien. Dalam tutorial ini, kita akan mempelajari seluk-beluk mengaktifkan dukungan 3D untuk file DGN V7 menggunakan Aspose.CAD untuk .NET.

## Prasyarat

Sebelum memulai perjalanan ini, pastikan Anda memiliki prasyarat berikut:

-  Aspose.CAD untuk .NET: Pastikan Anda telah menginstal perpustakaan. Anda dapat mengunduhnya dari[Halaman unduhan Aspose.CAD untuk .NET](https://releases.aspose.com/cad/net/).

- File DGN yang Valid: Siapkan file DGN valid yang ingin Anda proses menggunakan cuplikan kode yang disediakan. Anda dapat menggunakan milik Anda sendiri atau mengunduhnya untuk tujuan pengujian.

- Lingkungan Pengembangan .NET: Siapkan lingkungan pengembangan .NET untuk mengeksekusi kode yang disediakan. Jika Anda tidak memilikinya, Anda dapat mengikuti petunjuk instalasi di[Dokumentasi .NET](https://docs.microsoft.com/en-us/dotnet/core/install/).

## Impor Namespace

Untuk memulai, impor namespace yang diperlukan dalam proyek .NET Anda:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

Sekarang, mari kita uraikan cuplikan kode yang disediakan menjadi panduan langkah demi langkah.

## Langkah 1: Siapkan Lingkungan

Tentukan direktori dokumen Anda dan jalur ke file DGN:

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";
```

## Langkah 2: Muat File DGN

 Muat file DGN sebagai a`DgnImage` menggunakan Aspose.CAD`Image.Load` metode:

```csharp
using (DgnImage dgnImage = (DgnImage)Image.Load(sourceFilePath))
{
    // Cuplikan kode berlanjut...
}
```

## Langkah 3: Konfigurasikan Opsi Ekspor

Siapkan opsi ekspor, tentukan pengaturan rasterisasi vektor:

```csharp
var options = new PdfOptions
{
    VectorRasterizationOptions = new CadRasterizationOptions
    {
        PageWidth = 1500,
        PageHeight = 1500,
        CenterDrawing = true,
        AutomaticLayoutsScaling = true,
        BackgroundColor = Color.Black,
        Layouts = new string[] { "1", "2", "3", "9" } // Ekspor tampilan tertentu
    }
};
```

## Langkah 4: Simpan Hasilnya

 Memanfaatkan`Save` metode untuk mengekspor file DGN ke gambar raster:

```csharp
string outFile = "Your Output Directory"; // Tentukan direktori keluaran
dgnImage.Save(outFile, options);
```

## Kesimpulan

Selamat! Anda telah berhasil mengeluarkan dukungan 3D untuk file DGN V7 menggunakan Aspose.CAD untuk .NET. Tutorial ini memberikan peta jalan yang jelas, memandu Anda melalui setiap langkah untuk memastikan implementasi yang lancar.

## FAQ

### Q1: Dapatkah saya memproses beberapa file DGN secara bersamaan menggunakan pendekatan ini?

A1: Ya, Anda dapat memodifikasi kode untuk menangani banyak file dalam satu lingkaran atau sebagai bagian dari sistem pemrosesan batch.

### Q2: Format ekspor apa lagi yang didukung oleh Aspose.CAD untuk .NET?

 A2: Aspose.CAD untuk .NET mendukung berbagai format ekspor, termasuk PDF, PNG, JPG, dan banyak lagi. Mengacu kepada[dokumentasi](https://reference.aspose.com/cad/net/) untuk detailnya.

### Q3: Apakah Aspose.CAD untuk .NET kompatibel dengan versi .NET Core terbaru?

A3: Ya, Aspose.CAD untuk .NET dirancang agar kompatibel dengan versi .NET Core terbaru. Pastikan Anda menginstal versi yang sesuai di lingkungan Anda.

### Q4: Dapatkah saya menyesuaikan pengaturan ekspor lebih lanjut untuk kebutuhan spesifik saya?

 A4: Tentu saja! Kode yang diberikan menawarkan titik awal. Anda dapat menjelajahi opsi dan konfigurasi tambahan di[Dokumentasi Aspose.CAD](https://reference.aspose.com/cad/net/).

### Q5: Di mana saya dapat mencari bantuan atau berbagi pengalaman saya dengan Aspose.CAD untuk .NET?

A5: Bergabunglah dengan komunitas Aspose.CAD di[forum](https://forum.aspose.com/c/cad/19) untuk berinteraksi dengan pengembang lain dan mencari bantuan.