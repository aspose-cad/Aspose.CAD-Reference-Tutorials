---
title: Konversikan Gambar CAD ke Gambar Raster di Aspose.CAD untuk .NET
linktitle: Ubah Gambar CAD menjadi Gambar Raster
second_title: Aspose.CAD .NET - Format File CAD dan BIM
description: Jelajahi proses mulus dalam mengonversi gambar CAD menjadi gambar raster di .NET dengan Aspose.CAD. Buka alur kerja yang efisien dan tingkatkan proyek CAD Anda dengan mudah.
type: docs
weight: 11
url: /id/net/cad-drawing-manipulation/convert-cad-drawing-to-raster-image/
---
## Perkenalan

Dalam lanskap desain berbantuan komputer (CAD) yang terus berkembang, kebutuhan untuk mengonversi gambar CAD menjadi gambar raster dengan lancar adalah hal yang terpenting. Panduan langkah demi langkah ini mengeksplorasi cara mencapai hal ini menggunakan pustaka Aspose.CAD untuk .NET yang canggih. Aspose.CAD menyederhanakan proses, memberikan pengembang seperangkat alat yang kuat untuk meningkatkan alur kerja terkait CAD mereka.

## Prasyarat

Sebelum masuk ke tutorial, pastikan Anda memiliki prasyarat berikut:

1.  Aspose.CAD untuk .NET Library: Unduh dan instal perpustakaan Aspose.CAD dari[Unduh Halaman](https://releases.aspose.com/cad/net/).

2. Lingkungan Pengembangan: Siapkan lingkungan pengembangan yang berfungsi dengan IDE yang kompatibel untuk pengembangan .NET.

## Impor Namespace

Dalam proyek .NET Anda, impor namespace yang diperlukan untuk mengakses fungsionalitas Aspose.CAD. Tambahkan yang berikut ini di awal file kode Anda:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Langkah 1: Tentukan Jalur File

```csharp
// Jalur ke direktori dokumen.
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";
```

Pastikan untuk mengganti "Direktori Dokumen Anda" dengan jalur sebenarnya ke file CAD Anda.

## Langkah 2: Muat Gambar CAD

```csharp
using (Aspose.CAD.Image image = Aspose.CAD.Image.Load(sourceFilePath))
{
```

Langkah ini menginisialisasi objek gambar Aspose.CAD dan memuat gambar CAD dari jalur file yang ditentukan.

## Langkah 3: Konfigurasikan Opsi Rasterisasi

```csharp
// Buat sebuah instance dari CadRasterizationOptions
Aspose.CAD.ImageOptions.CadRasterizationOptions rasterizationOptions = new Aspose.CAD.ImageOptions.CadRasterizationOptions();
// Atur lebar & tinggi halaman
rasterizationOptions.PageWidth = 1200;
rasterizationOptions.PageHeight = 1200;
```

Di sini, kami menyiapkan opsi rasterisasi, menentukan lebar dan tinggi halaman keluaran.

## Langkah 4: Buat pngOptions untuk gambar yang dihasilkan

```csharp
// Buat sebuah instance dari PNGOptions untuk gambar yang dihasilkan
ImageOptionsBase options = new Aspose.CAD.ImageOptions.PngOptions();
// Tetapkan opsi rasterisasi
options.VectorRasterizationOptions = rasterizationOptions;
```

Langkah ini melibatkan konfigurasi opsi untuk gambar yang dihasilkan, menentukan opsi rasterisasi yang telah ditentukan sebelumnya.

## Langkah 5: Simpan Gambar yang Dihasilkan

```csharp
MyDir = MyDir + "conic_pyramid_raster_image_out.png";
// Simpan gambar yang dihasilkan
image.Save(MyDir, options);
```

Simpan gambar raster yang dikonversi ke jalur file keluaran yang ditentukan.

## Langkah 6: Tampilkan Pesan Sukses

```csharp
// ExEnd:KonversiDrawingToRasterImage
Console.WriteLine("\nCAD drawing converted successfully to raster image format.\nFile saved at " + MyDir);
```

Tampilkan pesan sukses yang menunjukkan selesainya proses konversi.

## Kesimpulan

Dalam tutorial ini, kita menjelajahi proses langkah demi langkah mengonversi gambar CAD menjadi gambar raster menggunakan pustaka Aspose.CAD untuk .NET. Dengan fitur canggih dan kemudahan integrasi, Aspose.CAD memberdayakan pengembang untuk menyederhanakan alur kerja CAD mereka dengan mudah.

## FAQ

### Q1: Apakah Aspose.CAD kompatibel dengan semua format file CAD?

A1: Aspose.CAD mendukung berbagai format file CAD, termasuk DWG, DXF, DGN, dan banyak lagi. Mengacu kepada[dokumentasi](https://reference.aspose.com/cad/net/) untuk daftar lengkap.

### Q2: Dapatkah saya menyesuaikan opsi rasterisasi untuk proyek yang berbeda?

A2: Ya, Aspose.CAD memungkinkan penyesuaian ekstensif pada opsi rasterisasi, memungkinkan pengembang menyesuaikan keluaran berdasarkan kebutuhan proyek.

### Q3: Apakah ada uji coba gratis yang tersedia untuk Aspose.CAD?

 A3: Ya, Anda dapat menjelajahi fitur Aspose.CAD dengan uji coba gratis. Mengunjungi[Di Sini](https://releases.aspose.com/) untuk memulai.

### Q4: Bagaimana saya bisa mendapatkan dukungan untuk Aspose.CAD?

 A4: Untuk bantuan atau pertanyaan apa pun, kunjungi Aspose.CAD[forum dukungan](https://forum.aspose.com/c/cad/19).

### Q5: Apakah lisensi sementara tersedia untuk Aspose.CAD?
 
 A5: Ya, pengembang dapat memperoleh lisensi sementara untuk Aspose.CAD dari[Link ini](https://purchase.aspose.com/temporary-license/).