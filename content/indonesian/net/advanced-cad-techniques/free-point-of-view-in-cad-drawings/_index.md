---
title: Sudut Pandang Gratis dalam Gambar CAD - Panduan Aspose.CAD
linktitle: Sudut Pandang Gratis dalam Gambar CAD
second_title: Aspose.CAD .NET - Format File CAD dan BIM
description: Jelajahi kebebasan visualisasi CAD dengan Aspose.CAD untuk .NET. Ikuti panduan langkah demi langkah kami untuk mendapatkan sudut pandang unik.
type: docs
weight: 11
url: /id/net/advanced-cad-techniques/free-point-of-view-in-cad-drawings/
---
Dalam bidang Computer-Aided Design (CAD), mendapatkan sudut pandang bebas dalam gambar adalah aspek penting dalam memvisualisasikan dan menyajikan desain yang rumit. Aspose.CAD untuk .NET memberikan solusi tangguh untuk mencapai kebebasan ini, memungkinkan pengguna memanipulasi dan mengoptimalkan gambar CAD dengan mudah. Dalam panduan langkah demi langkah ini, kita akan menjelajahi proses mendapatkan sudut pandang bebas dalam gambar CAD menggunakan Aspose.CAD untuk .NET.

## Prasyarat

Sebelum masuk ke tutorial, pastikan Anda memiliki prasyarat berikut:

1. Instalasi Aspose.CAD
 Pastikan Anda telah menginstal Aspose.CAD untuk .NET di lingkungan pengembangan Anda. Jika belum, Anda dapat mendownloadnya dari[Situs web Aspose.CAD](https://releases.aspose.com/cad/net/).

2. File Gambar CAD
Siapkan file gambar CAD yang ingin Anda manipulasi. Untuk panduan ini, kami akan menggunakan contoh file bernama "conic_pyramid.dxf."

3. Pengembangan lingkungan
Siapkan lingkungan pengembangan .NET yang berfungsi dengan Visual Studio atau IDE pilihan apa pun.

## Impor Namespace

Dalam proyek .NET Anda, impor namespace yang diperlukan untuk fungsionalitas Aspose.CAD. Tambahkan cuplikan kode berikut ke bagian atas file Anda:

```csharp
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
```


## Langkah 1: Tentukan Direktori Dokumen

```csharp
// Jalur ke direktori dokumen.
string MyDir = "Your Document Directory";
```

Pastikan untuk mengganti "Direktori Dokumen Anda" dengan jalur sebenarnya ke direktori dokumen Anda.

## Langkah 2: Tentukan File Sumber

```csharp
string sourceFilePath = MyDir + "conic_pyramid.dxf";
```

Berikan jalur ke file gambar CAD Anda.

## Langkah 3: Tetapkan Jalur Keluaran

```csharp
var outPath = Path.Combine(MyDir, "FreePointOfView_out.jpg");
```

Tentukan jalur di mana gambar CAD yang dimanipulasi akan disimpan.

## Langkah 4: Muat Gambar CAD

```csharp
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
```

Muat gambar CAD menggunakan Aspose.CAD.

## Langkah 5: Konfigurasikan Opsi JPEG

```csharp
JpegOptions options = new JpegOptions
{
    VectorRasterizationOptions = new CadRasterizationOptions
    {
        PageWidth = 1500, PageHeight = 1500
    }
};
```

Konfigurasikan opsi untuk mengekspor gambar CAD ke format JPEG.

## Langkah 6: Atur Sudut Rotasi

```csharp
float xAngle = 10; //Sudut rotasi sepanjang sumbu X
float yAngle = 30; //Sudut rotasi sepanjang sumbu Y
float zAngle = 40; //Sudut rotasi sepanjang sumbu Z
((CadRasterizationOptions)(options.VectorRasterizationOptions)).ObserverPoint = new ObserverPoint(xAngle, yAngle, zAngle);
```

Tentukan sudut rotasi sepanjang sumbu X, Y, dan Z untuk mencapai sudut pandang yang diinginkan.

## Langkah 7: Simpan Gambar CAD yang Dimanipulasi

```csharp
cadImage.Save(outPath, options);
}
```

Simpan gambar CAD yang dimanipulasi ke jalur keluaran yang ditentukan.

## Langkah 8: Tampilkan Pesan Sukses

```csharp
Console.WriteLine("\n3D images exported successfully to JPEG.\nFile saved at " + outPath);
```

Beri tahu pengguna tentang keberhasilan ekspor gambar 3D.

## Kesimpulan

Dalam tutorial ini, kita telah menjelajahi proses mendapatkan sudut pandang bebas dalam gambar CAD menggunakan Aspose.CAD untuk .NET. Dengan mengikuti petunjuk langkah demi langkah ini, Anda dapat meningkatkan kemampuan visualisasi CAD dan menyajikan desain Anda dengan perspektif baru.


## FAQ

### Q1: Dapatkah saya menggunakan Aspose.CAD untuk .NET dengan format file CAD lainnya?

A1: Ya, Aspose.CAD untuk .NET mendukung berbagai format file CAD, termasuk DWG dan DXF.

### Q2: Apakah ada versi uji coba Aspose.CAD yang tersedia?

 A2: Ya, Anda dapat mengunduh versi uji coba gratis dari[Di Sini](https://releases.aspose.com/).

### Q3: Bagaimana cara mendapatkan lisensi sementara untuk Aspose.CAD?

 A3: Anda dapat memperoleh lisensi sementara dari[Di Sini](https://purchase.aspose.com/temporary-license/).

### Q4: Di mana saya dapat menemukan dukungan tambahan untuk Aspose.CAD?

 A4: Kunjungi[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19) untuk dukungan dan diskusi komunitas.

### Q5: Dapatkah saya menyesuaikan opsi ekspor untuk format gambar yang berbeda?

A5: Tentu saja! Aspose.CAD menyediakan berbagai opsi penyesuaian, memungkinkan Anda menyesuaikan proses ekspor dengan kebutuhan spesifik Anda.