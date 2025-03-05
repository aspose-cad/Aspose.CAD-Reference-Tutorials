---
title: Menambahkan Teks ke File DWG di C# - Tutorial Aspose.CAD
linktitle: Menambahkan Teks ke File DWG di C#
second_title: Aspose.CAD .NET - Format File CAD dan BIM
description: Pelajari cara menambahkan teks ke file DWG menggunakan C# dan Aspose.CAD. Ikuti tutorial langkah demi langkah ini untuk integrasi yang lancar. Jelajahi dokumentasi Aspose.CAD untuk panduan komprehensif.
type: docs
weight: 14
url: /id/net/dwg-file-manipulation/adding-text-to-dwg/
---
## Perkenalan

Dalam bidang dinamis desain berbantuan komputer (CAD) dan pengembangan .NET, Aspose.CAD menonjol sebagai alat yang ampuh untuk memanipulasi file DWG. Menambahkan teks ke file DWG adalah persyaratan umum, dan dalam tutorial ini, kita akan mempelajari cara mencapainya menggunakan C# dan Aspose.CAD.

## Prasyarat

Sebelum masuk ke tutorial, pastikan Anda memiliki hal berikut:

-  Perpustakaan Aspose.CAD: Unduh dan instal perpustakaan Aspose.CAD dari[tautan unduhan](https://releases.aspose.com/cad/net/).

-  Direktori Dokumen: Siapkan direktori untuk dokumen Anda, dan catat jalurnya sebagai`MyDir`.

Sekarang, mari kita bagi prosesnya menjadi langkah-langkah yang dapat dikelola.

## Impor Namespace

Dalam kode C# Anda, sertakan namespace yang diperlukan untuk mengakses fungsionalitas Aspose.CAD.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.FileFormats.Cad.CadConsts;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadObjects.AttEntities;
using Aspose.CAD.ImageOptions;
```

## Langkah 1: Muat File DWG

 Muat file DWG ke dalam file`Image` objek menggunakan perpustakaan Aspose.CAD.

```csharp
string dwgPathToFile = MyDir + "SimpleEntites.dwg";
using (Image image = Image.Load(dwgPathToFile))
{
    // Kode Anda untuk langkah selanjutnya ada di sini
}
```

## Langkah 2: Buat Objek CadText

 Buat contoh a`CadText` objek untuk mewakili teks yang ingin Anda tambahkan ke file DWG.

```csharp
CadText cadText = new CadText();
cadText.StyleType = "Standard";
cadText.DefaultValue = "Some custom text";
cadText.ColorId = 256;
cadText.LayerName = "0";
cadText.FirstAlignment.X = 47.90;
cadText.FirstAlignment.Y = 5.56;
cadText.TextHeight = 0.8;
cadText.ScaleX = 0.0;
```

## Langkah 3: Tambahkan Teks ke DWG

 Tambahkan yang dibuat`CadText` keberatan dengan file DWG menggunakan Aspose.CAD.

```csharp
CadImage cadImage = (CadImage)image;
cadImage.BlockEntities["*Model_Space"].AddEntity(cadText);
```

## Langkah 4: Konfigurasikan Opsi PDF

Konfigurasikan opsi PDF untuk menyimpan file DWG yang dimodifikasi sebagai PDF.

```csharp
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.VectorRasterizationOptions = cadRasterizationOptions;
cadRasterizationOptions.DrawType = CadDrawTypeMode.UseObjectColor;
cadRasterizationOptions.PageHeight = 1600;
cadRasterizationOptions.PageWidth = 1600;
cadRasterizationOptions.Layouts = new string[] { "Model" };
```

## Langkah 5: Simpan sebagai PDF

Simpan file DWG yang dimodifikasi sebagai PDF dengan teks tambahan.

```csharp
image.Save(MyDir + "SimpleEntites_generated.pdf", pdfOptions);
```

Sekarang, Anda telah berhasil menambahkan teks ke file DWG menggunakan C# dan Aspose.CAD. Jangan ragu untuk menjelajahi lebih banyak fitur dan fungsi Aspose.CAD untuk kebutuhan manipulasi CAD Anda.

## Kesimpulan

Dalam tutorial ini, kami telah membahas langkah-langkah penting untuk menambahkan teks ke file DWG menggunakan C# dan Aspose.CAD. Kombinasi kuat ini membuka kemungkinan pembuatan dokumen CAD yang dinamis dan disesuaikan.

## FAQ

### Q1: Apakah Aspose.CAD kompatibel dengan semua versi file DWG?

A1: Aspose.CAD mendukung berbagai versi file DWG, memastikan kompatibilitas dengan berbagai perangkat lunak CAD.

### Q2: Bisakah saya menambahkan beberapa entitas teks ke satu file DWG menggunakan Aspose.CAD?

A2: Ya, Anda dapat menambahkan beberapa entitas teks ke file DWG dengan mengulangi proses yang dijelaskan dalam tutorial.

### Q3: Bagaimana cara mengubah font dan gaya teks di Aspose.CAD?

 A3: Untuk mengubah font dan gaya teks, sesuaikan properti`CadText` objek sebelum menambahkannya ke file DWG.

### Q4: Apakah ada pertimbangan lisensi untuk menggunakan Aspose.CAD dalam proyek komersial?

 A4: Ya, pastikan kepatuhan terhadap ketentuan lisensi Aspose.CAD. Mengacu pada[Pembelian Aspose.CAD](https://purchase.aspose.com/buy) untuk detailnya.

### Q5: Di mana saya dapat mencari bantuan atau mendiskusikan pertanyaan terkait Aspose.CAD?

A5: Kunjungi[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19)untuk terhubung dengan komunitas dan mendapatkan dukungan.