---
title: Mengonversi DWG Tertentu ke Gambar di C# - Panduan Aspose.CAD
linktitle: Mengonversi DWG Tertentu ke Gambar di C#
second_title: Aspose.CAD .NET - Format File CAD dan BIM
description: Jelajahi Aspose.CAD untuk .NET. Konversi DWG ke gambar dalam C# dengan mudah. Panduan komprehensif dengan contoh kode.
type: docs
weight: 15
url: /id/net/image-manipulation-and-rendering/converting-particular-dwg-to-image/
---
## Perkenalan

Dalam dunia pengembangan perangkat lunak yang dinamis, penanganan file CAD yang efisien sangatlah penting. Aspose.CAD untuk .NET muncul sebagai solusi ampuh, memberikan pengembang seperangkat alat canggih untuk memanipulasi dan mengonversi file CAD dengan lancar. Dalam tutorial ini, kita akan mendalami proses mengonversi file DWG tertentu menjadi gambar menggunakan C#.

## Prasyarat

Sebelum kita memulai perjalanan coding ini, pastikan Anda memiliki prasyarat berikut:

- Visual Studio: Lingkungan pengembangan untuk menulis dan mengeksekusi kode C#.
-  Aspose.CAD untuk .NET: Pastikan Anda telah menginstal perpustakaan. Anda dapat menemukan tautan unduhan[Di Sini](https://releases.aspose.com/cad/net/).
- File DWG: Siapkan file DWG untuk dikonversi. Anda dapat menggunakan file contoh "visualization_-_conference_room.dwg" untuk panduan ini.

## Impor Namespace

Dalam kode C# Anda, pastikan untuk mengimpor namespace yang diperlukan untuk bekerja dengan Aspose.CAD:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadConsts;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## Langkah 1: Muat File DWG

Mulailah dengan memuat file DWG ke dalam kerangka Aspose.CAD:

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "visualization_-_conference_room.dwg";
var cadImage = (CadImage)Aspose.CAD.Image.Load(sourceFilePath);
```

## Langkah 2: Filter Entitas

Selanjutnya, filter entitas dalam file DWG. Dalam contoh ini, kami akan fokus pada mengekstraksi entitas teks:

```csharp
CadBaseEntity[] entities = cadImage.Entities;
List<CadBaseEntity> filteredEntities = new List<CadBaseEntity>();

foreach (CadBaseEntity baseEntity in entities)
{
    // Seleksi atau penyaringan entitas
    if (baseEntity.TypeName == CadEntityTypeName.TEXT)
    {
        filteredEntities.Add(baseEntity);
    }
}

cadImage.Entities = filteredEntities.ToArray();
```

## Langkah 3: Tetapkan Opsi Rasterisasi

 Buat sebuah contoh dari`CadRasterizationOptions` dan tentukan propertinya untuk konversi gambar:

```csharp
Aspose.CAD.ImageOptions.CadRasterizationOptions rasterizationOptions =
    new Aspose.CAD.ImageOptions.CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
rasterizationOptions.AutomaticLayoutsScaling = true;
```

## Langkah 4: Atur Opsi PDF

 Buat sebuah contoh dari`PdfOptions` dan tetapkan opsi rasterisasi:

```csharp
Aspose.CAD.ImageOptions.PdfOptions pdfOptions = new Aspose.CAD.ImageOptions.PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Langkah 5: Simpan sebagai PDF

Terakhir, simpan gambar yang dikonversi sebagai file PDF:

```csharp
string outFile = MyDir + "result_out_generated.pdf";
cadImage.Save(outFile, pdfOptions);
```

## Kesimpulan

Selamat! Anda telah berhasil mengonversi file DWG tertentu menjadi gambar menggunakan Aspose.CAD untuk .NET. Tutorial ini memberikan gambaran sekilas tentang kemampuan perpustakaan yang hebat, memberdayakan pengembang untuk bekerja secara efisien dengan file CAD dalam aplikasi mereka.

## FAQ

### Q1: Apakah Aspose.CAD kompatibel dengan semua versi file DWG?

A1: Aspose.CAD mendukung berbagai versi file DWG, memastikan kompatibilitas di berbagai perangkat lunak CAD.

### Q2: Dapatkah saya menyesuaikan opsi rasterisasi untuk keluaran yang berbeda?

A2: Tentu saja! Aspose.CAD memberikan fleksibilitas dalam menyesuaikan opsi rasterisasi untuk memenuhi kebutuhan spesifik Anda untuk format output yang berbeda.

### Q3: Di mana saya dapat menemukan contoh dan dokumentasi tambahan?

 A3: Jelajahi secara komprehensif[Dokumentasi Aspose.CAD](https://reference.aspose.com/cad/net/) untuk lebih banyak contoh dan panduan mendalam.

### Q4: Apakah ada uji coba gratis yang tersedia untuk Aspose.CAD?

 A4: Ya, Anda dapat mengakses uji coba gratis[Di Sini](https://releases.aspose.com/) untuk merasakan potensi penuh Aspose.CAD.

### Q5: Bagaimana saya bisa mendapatkan dukungan atau terhubung dengan komunitas untuk mendapatkan bantuan?

A5: Kunjungi[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19) untuk dukungan, diskusi, dan kolaborasi dengan komunitas.