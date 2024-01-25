---
title: Mengonversi DWG ke PDF Kepatuhan - Tutorial Aspose.CAD
linktitle: Mengonversi DWG ke PDF Kepatuhan
second_title: Aspose.CAD .NET - Format File CAD dan BIM
description: Konversikan DWG ke PDF Kepatuhan dengan Aspose.CAD untuk .NET. Ikuti tutorial kami untuk panduan langkah demi langkah.
type: docs
weight: 13
url: /id/net/conversion-and-export/converting-dwg-to-compliance-pdf/
---
## Perkenalan

Selamat datang di tutorial langkah demi langkah kami tentang mengonversi file DWG ke PDF Kepatuhan menggunakan Aspose.CAD untuk .NET. Aspose.CAD adalah .NET API yang kuat yang memungkinkan pengembang bekerja dengan format file CAD dengan mudah. Dalam tutorial ini, kami akan memandu Anda melalui proses mengonversi file DWG ke PDF Kepatuhan dengan contoh dan penjelasan mendetail.

## Prasyarat

Sebelum kita mulai, pastikan Anda memiliki prasyarat berikut:

-  Aspose.CAD untuk .NET: Pastikan Anda memiliki perpustakaan Aspose.CAD yang terintegrasi ke dalam proyek .NET Anda. Anda dapat mengunduhnya[Di Sini](https://releases.aspose.com/cad/net/).

- Lingkungan Pengembangan: Pasang lingkungan pengembangan .NET yang berfungsi, dan pastikan lingkungan tersebut dikonfigurasi dengan benar.

- Contoh File DWG: Unduh contoh file DWG yang ingin Anda konversi ke PDF Kepatuhan.

## Impor Namespace

Dalam proyek .NET Anda, impor namespace yang diperlukan untuk memanfaatkan fungsionalitas Aspose.CAD.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
```

Sekarang, mari kita uraikan proses konversi file DWG ke PDF Kepatuhan menjadi beberapa langkah.

## Langkah 1: Muat File DWG

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Bottom_plate.dwg";

Aspose.CAD.Image cadImage = Aspose.CAD.Image.Load(sourceFilePath);
```

## Langkah 2: Tetapkan Opsi Rasterisasi

 Buat sebuah contoh dari`CadRasterizationOptions` dan konfigurasikan propertinya, seperti warna latar belakang, lebar halaman, dan tinggi halaman.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions
{
    BackgroundColor = Aspose.CAD.Color.White,
    PageWidth = 1600,
    PageHeight = 1600
};
```

## Langkah 3: Buat Opsi PDF

 Buat sebuah contoh dari`PdfOptions` dan atur opsi rasterisasi vektor.

```csharp
PdfOptions pdfOptions = new PdfOptions
{
    VectorRasterizationOptions = rasterizationOptions,
    CorePdfOptions = new PdfDocumentOptions { Compliance = PdfCompliance.PdfA1a }
};
```

## Langkah 4: Simpan sebagai PDF (Kepatuhan A1a)

Simpan gambar CAD sebagai PDF Kepatuhan dengan kepatuhan A1a.

```csharp
cadImage.Save(MyDir + "PDFA1_A.pdf", pdfOptions);
```

## Langkah 5: Simpan sebagai PDF (Kepatuhan A1b)

Ubah jenis kepatuhan menjadi A1b dan simpan gambar CAD sebagai PDF Kepatuhan.

```csharp
pdfOptions.CorePdfOptions.Compliance = PdfCompliance.PdfA1b;
cadImage.Save(MyDir + "PDFA1_B.pdf", pdfOptions);
```

## Kesimpulan

Selamat! Anda telah berhasil mengonversi file DWG ke PDF Kepatuhan menggunakan Aspose.CAD untuk .NET. Tutorial ini memberikan panduan komprehensif bagi pengembang yang ingin mengintegrasikan kemampuan konversi CAD ke dalam aplikasi mereka.

## FAQ

### Q1: Bisakah saya mengonversi format CAD lain ke PDF Kepatuhan menggunakan Aspose.CAD?

A1: Ya, Aspose.CAD mendukung berbagai format CAD, memungkinkan konversi ke PDF Kepatuhan.

### Q2: Apakah Aspose.CAD kompatibel dengan .NET Core?

A2: Ya, Aspose.CAD kompatibel dengan .NET Framework dan .NET Core.

### Q3: Apakah ada opsi lisensi untuk Aspose.CAD?

 A3: Ya, Anda dapat menjelajahi opsi lisensi[Di Sini](https://purchase.aspose.com/buy).

### Q4: Apakah tersedia uji coba gratis?

 A4: Ya, Anda bisa mendapatkan uji coba gratis[Di Sini](https://releases.aspose.com/).

### Q5: Di mana saya bisa mendapatkan dukungan untuk Aspose.CAD?

A5: Kunjungi[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19) untuk pertanyaan terkait dukungan apa pun.