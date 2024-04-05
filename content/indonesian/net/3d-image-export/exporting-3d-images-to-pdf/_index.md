---
title: Mengekspor Gambar 3D ke PDF - Tutorial Aspose.CAD
linktitle: Mengekspor Gambar 3D ke PDF
second_title: Aspose.CAD .NET - Format File CAD dan BIM
description: Konversi gambar CAD 3D ke PDF dengan mudah menggunakan Aspose.CAD untuk .NET. Ikuti tutorial langkah demi langkah kami untuk ekspor PDF yang lancar.
type: docs
weight: 10
url: /id/net/3d-image-export/exporting-3d-images-to-pdf/
---
## Perkenalan

Apakah Anda ingin mengekspor gambar 3D ke PDF dengan lancar menggunakan Aspose.CAD untuk .NET? Tutorial langkah demi langkah ini akan memandu Anda melalui proses tersebut, memastikan bahwa Anda memanfaatkan kekuatan Aspose.CAD untuk dengan mudah mengonversi gambar 3D Anda ke format PDF.

## Prasyarat

Sebelum masuk ke tutorial, pastikan Anda memiliki prasyarat berikut:

-  Aspose.CAD untuk .NET: Pastikan Anda telah menginstal perpustakaan Aspose.CAD untuk .NET. Jika belum, Anda dapat mendownloadnya dari[Halaman unduhan Aspose.CAD untuk .NET](https://releases.aspose.com/cad/net/).

- Direktori Dokumen: Siapkan direktori tempat file CAD Anda disimpan, dan catat jalurnya.

## Impor Namespace

Di proyek .NET Anda, impor namespace yang diperlukan untuk bekerja dengan Aspose.CAD. Tambahkan baris berikut ke bagian atas file kode Anda:

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

 Mulailah dengan memuat gambar CAD yang ingin Anda ekspor ke PDF. Menggunakan`Load` metode dari perpustakaan Aspose.CAD. Mengganti`"conic_pyramid.dxf"` dengan jalur ke file CAD Anda.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";
using (Image cadImage = Image.Load(sourceFilePath))
{
    // Kode Anda untuk memuat gambar CAD ada di sini
}
```

## Langkah 2: Konfigurasikan Opsi Rasterisasi

 Konfigurasikan opsi rasterisasi untuk gambar CAD. Tetapkan parameter seperti lebar halaman, tinggi halaman, dan tata letak. Batalkan komentar pada baris yang terkait dengan`TypeOfEntities` jika entitas Anda 3D.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 500;
rasterizationOptions.PageHeight = 500;
// rasterizationOptions.TypeOfEntities = TypeOfEntities.Entities3D;

rasterizationOptions.Layouts = new string[] { "Model" };
```

## Langkah 3: Atur Opsi PDF

Buat opsi PDF dan kaitkan dengan opsi rasterisasi.

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Langkah 4: Simpan sebagai PDF

Simpan gambar CAD sebagai file PDF menggunakan opsi yang dikonfigurasi. Tentukan jalur keluaran untuk file PDF.

```csharp
MyDir = MyDir + "Export3DImagestoPDF_out.pdf";
cadImage.Save(MyDir, pdfOptions);
```

## Kesimpulan

Selamat! Anda telah berhasil mengekspor gambar 3D ke PDF menggunakan Aspose.CAD untuk .NET. Tutorial sederhana ini memastikan Anda dengan mudah mengonversi file CAD Anda ke format yang lebih mudah diakses.

## FAQ

### Q1: Apakah Aspose.CAD kompatibel dengan semua format file CAD?

A1: Ya, Aspose.CAD mendukung berbagai format CAD, memastikan fleksibilitas dalam menangani berbagai jenis file.

### Q2: Dapatkah saya menyesuaikan dimensi halaman saat mengekspor ke PDF?

A2: Tentu saja. Tutorial ini menunjukkan cara mengonfigurasi lebar dan tinggi halaman sesuai dengan kebutuhan Anda.

### Q3: Apakah lisensi sementara tersedia untuk Aspose.CAD?

 A3: Ya, Anda bisa mendapatkan lisensi sementara untuk Aspose.CAD dengan mengunjungi[Lisensi Sementara](https://purchase.aspose.com/temporary-license/).

### Q4: Di mana saya bisa mendapatkan dukungan tambahan atau diskusi komunitas?

 A4: Pergilah ke[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19) untuk dukungan dan keterlibatan dengan komunitas.

### Q5: Apakah Aspose.CAD versi uji coba gratis tersedia?

 A5: Ya, Anda dapat menjelajahi fitur Aspose.CAD dengan mengakses[uji coba gratis](https://releases.aspose.com/).