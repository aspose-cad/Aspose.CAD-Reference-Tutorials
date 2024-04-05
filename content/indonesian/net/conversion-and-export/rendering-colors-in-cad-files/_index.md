---
title: Merender Warna dalam File CAD - Panduan Aspose.CAD
linktitle: Merender Warna dalam File CAD
second_title: Aspose.CAD .NET - Format File CAD dan BIM
description: Render file master CAD dalam .NET dengan Aspose.CAD. Ikuti panduan langkah demi langkah kami untuk mendapatkan warna yang cerah.
type: docs
weight: 10
url: /id/net/conversion-and-export/rendering-colors-in-cad-files/
---
## Perkenalan

Apakah Anda menghadapi tantangan dalam merender warna dalam file CAD menggunakan .NET? Tidak perlu mencari lagi! Dalam panduan komprehensif ini, kami akan memandu Anda melalui proses langkah demi langkah menggunakan perpustakaan Aspose.CAD yang kuat. Di akhir tutorial ini, Anda akan dibekali dengan pengetahuan untuk merender warna dengan mudah di file CAD Anda.

## Prasyarat

Sebelum kita mendalami tutorialnya, pastikan Anda memiliki prasyarat berikut:

-  Perpustakaan Aspose.CAD: Unduh dan instal perpustakaan Aspose.CAD dari[Di Sini](https://releases.aspose.com/cad/net/).

- Lingkungan Pengembangan: Pastikan Anda telah menyiapkan lingkungan pengembangan .NET.

- File CAD: Siapkan contoh file CAD untuk pengujian. Anda dapat menggunakan "test1.dwg" untuk tutorial ini.

## Impor Namespace

Dalam proyek .NET Anda, impor namespace yang diperlukan untuk mengakses fungsionalitas Aspose.CAD. Tambahkan baris berikut di awal kode Anda:

```csharp
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
```

## Langkah 1: Siapkan Proyek Anda

Buat proyek .NET baru dan siapkan direktori yang diperlukan. Pastikan perpustakaan Aspose.CAD direferensikan dalam proyek Anda.

## Langkah 2: Tentukan Jalur File

Tentukan jalur untuk file CAD masukan Anda dan file PNG keluaran. Perbarui baris berikut dalam kode Anda:

```csharp
string MyDir = "Your Document Directory";
string inputFile = MyDir + "test1.dwg";
string outputFile = MyDir + "test1.png";
```

## Langkah 3: Muat File CAD

Gunakan kode berikut untuk membuka dan memuat file CAD:

```csharp
using (FileStream fs = new FileStream(inputFile, FileMode.Open))
{
    using (FileStream output = new FileStream(outputFile, FileMode.Create))
    {
        Image document = Image.Load(fs);
```

## Langkah 4: Konfigurasikan Opsi Rasterisasi

Konfigurasikan opsi rasterisasi untuk menyesuaikan proses rendering. Perbarui baris berikut:

```csharp
PngOptions saveOptions = new PngOptions();

CadRasterizationOptions options = new CadRasterizationOptions();
options.NoScaling = false;
options.PageHeight = document.Height * 10;
options.PageWidth = document.Width * 10;
options.DrawType = Aspose.CAD.FileFormats.Cad.CadDrawTypeMode.UseObjectColor;
saveOptions.VectorRasterizationOptions = options;
```

## Langkah 5: Simpan Gambar yang Dirender

Simpan gambar yang dirender menggunakan opsi yang ditentukan:

```csharp
document.Save(output, saveOptions);
```

## Kesimpulan

Selamat! Anda telah berhasil merender warna dalam file CAD menggunakan Aspose.CAD untuk .NET. Panduan langkah demi langkah ini telah membekali Anda dengan keterampilan untuk meningkatkan kemampuan rendering CAD Anda.

## FAQ

### Q1: Bisakah saya menggunakan Aspose.CAD secara gratis?

 A1: Aspose.CAD menawarkan versi uji coba gratis yang tersedia[Di Sini](https://releases.aspose.com/)Anda dapat menjelajahi fitur-fiturnya sebelum melakukan pembelian.

### Q2: Di mana saya dapat menemukan dokumentasi terperinci untuk Aspose.CAD?

 A2: Lihat dokumentasi[Di Sini](https://reference.aspose.com/cad/net/) untuk informasi mendalam tentang fungsi Aspose.CAD.

### Q3: Bagaimana cara mendapatkan lisensi sementara untuk Aspose.CAD?

 A3: Dapatkan lisensi sementara[Di Sini](https://purchase.aspose.com/temporary-license/) untuk tujuan pengujian.

### Q4: Butuh bantuan atau punya pertanyaan?

 A4: Kunjungi komunitas Aspose.CAD[forum](https://forum.aspose.com/c/cad/19) untuk dukungan dan diskusi.

### Q5: Di mana saya bisa membeli perpustakaan Aspose.CAD?

 A5: Beli Aspose.CAD[Di Sini](https://purchase.aspose.com/buy) untuk membuka potensi penuhnya.