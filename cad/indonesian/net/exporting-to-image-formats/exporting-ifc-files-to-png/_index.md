---
title: Mengekspor File IFC ke PNG - Tutorial Aspose.CAD
linktitle: Mengekspor File IFC ke PNG
second_title: Aspose.CAD .NET - Format File CAD dan BIM
description: Jelajahi Aspose.CAD untuk .NET, solusi tangguh untuk konversi IFC ke PNG yang lancar. Unduh sekarang untuk pemrosesan file CAD yang efisien.
type: docs
weight: 10
url: /id/net/exporting-to-image-formats/exporting-ifc-files-to-png/
---
## Perkenalan

Dalam dunia desain berbantuan komputer (CAD) yang dinamis, konversi file yang efisien sangatlah penting. Aspose.CAD untuk .NET muncul sebagai alat yang ampuh, menawarkan kemampuan tanpa batas untuk mengekspor file IFC (Industry Foundation Classes) ke format PNG. Tutorial langkah demi langkah ini akan memandu Anda melalui prosesnya, memastikan pengalaman yang lancar dengan Aspose.CAD.

## Prasyarat

Sebelum masuk ke tutorial, pastikan Anda memiliki prasyarat berikut:

### 1. Instalasi Aspose.CAD

 Pastikan Anda telah menginstal Aspose.CAD untuk .NET. Anda dapat mengunduhnya dari halaman rilis[Di Sini](https://releases.aspose.com/cad/net/).

### 2. Direktori Dokumen

 Buat direktori khusus untuk dokumen Anda. Dalam contoh yang diberikan, variabel`MyDir` mewakili direktori dokumen.

## Impor Namespace

Sekarang setelah Anda menyiapkan prasyaratnya, mari impor namespace yang diperlukan dalam aplikasi .NET Anda untuk menggunakan fungsionalitas Aspose.CAD.

```csharp
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using Aspose.CAD.FileFormats.Ifc;
```

## Langkah 1: Muat File IFC

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "example.ifc";
using (IfcImage cadImage = (IfcImage)Image.Load(sourceFilePath))
{
```

 Pada langkah ini, kami menginisialisasi Aspose.CAD`IfcImage` objek dan memuat file IFC ke dalamnya.

## Langkah 2: Tetapkan Opsi Rasterisasi

```csharp
    CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
   
    rasterizationOptions.PageWidth = 100;
    rasterizationOptions.PageHeight = 100;
```

Tentukan opsi rasterisasi untuk mengonfigurasi lebar dan tinggi halaman untuk keluaran PNG.

## Langkah 3: Tetapkan Opsi PNG

```csharp
    PngOptions pngOptions = new PngOptions();
    pngOptions.VectorRasterizationOptions = rasterizationOptions;
```

Buat opsi PNG dan kaitkan opsi rasterisasi yang telah ditentukan sebelumnya.

## Langkah 4: Tentukan Jalur Keluaran

```csharp
    // Tetapkan jalur keluaran juga
    string outPath = sourceFilePath + ".png";
    cadImage.Save(outPath, pngOptions);
}
```

Tentukan jalur keluaran untuk file PNG, pastikan nama file tersebut sama dengan file sumber dengan ekstensi ".png". Terakhir, simpan gambar yang dikonversi.

## Kesimpulan

Dengan langkah mudah ini, Anda telah berhasil mengekspor file IFC ke PNG menggunakan Aspose.CAD untuk .NET. Alat serbaguna ini menyederhanakan proses konversi CAD, sehingga dapat diakses oleh pengembang dan insinyur.

## FAQ

### Q1: Bisakah saya menggunakan Aspose.CAD untuk .NET di macOS atau Linux?

A1: Tidak, Aspose.CAD untuk .NET dirancang khusus untuk lingkungan Windows.

### Q2: Apakah lisensi sementara tersedia untuk tujuan pengujian?

 A2: Ya, Anda bisa mendapatkan lisensi sementara dari[Di Sini](https://purchase.aspose.com/temporary-license/) untuk evaluasi.

### Q3: Bagaimana saya bisa mendapatkan dukungan untuk Aspose.CAD?

 A3: Kunjungi[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19) untuk dukungan dan diskusi komunitas.

### Q4: Di mana saya dapat menemukan dokumentasi lengkap?

 A4: Lihat[Dokumentasi Aspose.CAD](https://reference.aspose.com/cad/net/) untuk informasi rinci dan contoh.

### Q5: Bagaimana jika saya mengalami masalah saat instalasi?

 A5: Periksa dokumentasi atau minta bantuan di[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19).