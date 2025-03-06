---
title: Bekerja dengan File DWG di C# - Dapatkan Ukuran Tata Letak DWF
linktitle: Bekerja dengan File DWG di C# - Dapatkan Ukuran Tata Letak DWF
second_title: Aspose.CAD .NET - Format File CAD dan BIM
description: Jelajahi kekuatan Aspose.CAD untuk .NET dalam menangani file DWG. Pelajari cara mengekstrak ukuran tata letak DWF dengan mudah menggunakan C#.
weight: 10
url: /id/net/dwg-file-manipulation/get-size-of-dwf-layout/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Bekerja dengan File DWG di C# - Dapatkan Ukuran Tata Letak DWF

## Perkenalan

Di bidang desain berbantuan komputer (CAD) dan pengembangan .NET, Aspose.CAD berdiri sebagai alat yang ampuh untuk menangani file DWG. Tutorial ini akan memandu Anda melalui proses bekerja dengan file DWG di C# dan mengekstrak ukuran tata letak DWF. Sebelum kita mendalami kodenya, pastikan Anda sudah menyiapkan segalanya untuk memulai perjalanan ini.

## Prasyarat

Untuk mengikuti tutorial ini dengan lancar, pastikan Anda memiliki prasyarat berikut:

-  Aspose.CAD untuk .NET: Pastikan Anda telah menginstal Aspose.CAD untuk .NET. Anda dapat mengunduhnya dari[Halaman unduhan Aspose.CAD untuk .NET](https://releases.aspose.com/cad/net/).

Sekarang setelah Anda memiliki alat yang diperlukan, mari terjun ke arena coding.

## Impor Namespace

Sebelum kita mulai bekerja dengan kode, mari impor namespace yang diperlukan:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Dwf;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
```

Namespace ini akan menyediakan kelas dan metode penting untuk menangani file CAD dengan Aspose.CAD di aplikasi C# Anda.

## Langkah 1: Siapkan Lingkungan Anda

Mulailah dengan memastikan Anda telah menyiapkan lingkungan yang benar untuk proyek Anda. Referensikan perpustakaan Aspose.CAD di proyek C# Anda.

## Langkah 2: Tentukan Jalur File

Tentukan jalur untuk file DWG Anda dan direktori keluaran untuk file JPG yang dihasilkan:

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "blocks_and_tables.dwf";
```

## Langkah 3: Muat Gambar DWF

Muat gambar DWF menggunakan Aspose.CAD:

```csharp
using (DwfImage image = (DwfImage)Aspose.CAD.Image.Load(sourceFilePath))
{
    // Kode untuk langkah lebih lanjut akan ada di sini
}
```

## Langkah 4: Ulangi Melalui Halaman

Iterasi melalui halaman-halaman gambar DWF:

```csharp
foreach (var page in image.Pages)
{
    // Kode untuk langkah lebih lanjut akan ada di sini
}
```

## Langkah 5: Dapatkan Informasi Tata Letak

Dapatkan informasi tata letak dari setiap halaman:

```csharp
var layout = page.Name;
System.Console.WriteLine("Layout= " + layout);
```

## Langkah 6: Siapkan Opsi JPG

Siapkan opsi untuk menyimpan tata letak sebagai file JPG:

```csharp
using (FileStream fs = new FileStream(MyDir + "layout_" + layout + ".jpg", FileMode.Create))
{
    JpegOptions jpegOptions = new JpegOptions();
    CadRasterizationOptions options = new CadRasterizationOptions();
    options.Layouts = new string[] { layout };
    // Kode untuk langkah lebih lanjut akan ada di sini
}
```

## Langkah 7: Tentukan Ukuran Halaman

Tentukan ukuran tata letak DWF:

```csharp
double sizeExtX = page.MaxPoint.X - page.MinPoint.X;
double sizeExtY = page.MaxPoint.Y - page.MinPoint.Y;
// Kode untuk langkah lebih lanjut akan ada di sini
```

## Langkah 8: Siapkan Dimensi Halaman

Siapkan dimensi halaman berdasarkan jenis unit:

```csharp
if (page.UnitType == UnitType.Inch)
{
    options.PageHeight = CommonHelper.INtoPixels(sizeExtY, CommonHelper.DPI);
    options.PageWidth = CommonHelper.INtoPixels(sizeExtX, CommonHelper.DPI);
}
else if (page.UnitType == UnitType.Millimeter)
{
    options.PageHeight = CommonHelper.MMtoPixels(sizeExtY, CommonHelper.DPI);
    options.PageWidth = CommonHelper.MMtoPixels(sizeExtX, CommonHelper.DPI);
}
else
{
    options.PageHeight = (float)sizeExtY;
    options.PageWidth = (float)sizeExtX;
}
```

## Langkah 9: Simpan File JPG

Simpan file JPG dengan opsi yang ditentukan:

```csharp
jpegOptions.VectorRasterizationOptions = options;
image.Save(fs, jpegOptions);
}
```

Sekarang Anda telah berhasil mengekstrak ukuran layout DWF dari file DWG menggunakan Aspose.CAD di C#. Jangan ragu untuk menjelajahi lebih banyak fitur dan fungsi yang ditawarkan Aspose.CAD untuk pengembangan .NET.

## Kesimpulan

Dalam tutorial ini, kita telah mempelajari proses bekerja dengan file DWG di C# menggunakan Aspose.CAD. Dengan mengikuti langkah-langkah ini, Anda tidak hanya bisa mendapatkan ukuran tata letak DWF tetapi juga memanfaatkan kemampuan Aspose.CAD untuk berbagai tugas terkait CAD di proyek .NET Anda.

## FAQ

### Q1: Apakah Aspose.CAD kompatibel dengan format file DWG terbaru?

 A1: Aspose.CAD mendukung berbagai format file DWG, termasuk versi terbaru. Mengacu kepada[dokumentasi](https://reference.aspose.com/cad/net/) untuk detail kompatibilitas spesifik.

### Q2: Bisakah saya menggunakan Aspose.CAD untuk proyek komersial dan pribadi?

 A2: Ya, Aspose.CAD menawarkan opsi lisensi yang fleksibel untuk penggunaan komersial dan pribadi. Mengunjungi[halaman pembelian](https://purchase.aspose.com/buy) untuk lebih jelasnya.

### Q3: Bagaimana cara mendapatkan lisensi sementara untuk Aspose.CAD?

 A3: Anda bisa mendapatkan lisensi sementara dari[Di Sini](https://purchase.aspose.com/temporary-license/) untuk tujuan evaluasi.

### Q4: Di mana saya dapat menemukan dukungan untuk Aspose.CAD?

A4: Untuk pertanyaan atau bantuan apa pun, kunjungi[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19).

### Q5: Apakah ada uji coba gratis yang tersedia untuk Aspose.CAD?

 A5: Ya, Anda dapat mengakses Aspose.CAD versi uji coba gratis[Di Sini](https://releases.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
