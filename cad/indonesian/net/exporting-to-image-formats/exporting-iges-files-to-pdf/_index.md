---
title: Mengekspor File IGES ke PDF - Panduan Aspose.CAD
linktitle: Mengekspor File IGES ke PDF
second_title: Aspose.CAD .NET - Format File CAD dan BIM
description: Pelajari cara mengekspor file IGES ke PDF dengan mudah menggunakan Aspose.CAD untuk .NET. Ikuti panduan langkah demi langkah kami untuk manipulasi file CAD yang tepat.
weight: 11
url: /id/net/exporting-to-image-formats/exporting-iges-files-to-pdf/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Mengekspor File IGES ke PDF - Panduan Aspose.CAD

## Perkenalan

Dalam dunia desain berbantuan komputer (CAD) yang dinamis, kebutuhan untuk mengonversi file IGES ke format PDF adalah kebutuhan umum. Aspose.CAD untuk .NET memberikan solusi ampuh untuk tugas ini, menawarkan fleksibilitas dan presisi dalam menangani file CAD. Dalam tutorial ini, kami akan memandu Anda melalui proses mengekspor file IGES ke PDF menggunakan Aspose.CAD untuk .NET. Ayo selami!

## Prasyarat

Sebelum kita mulai, pastikan Anda memiliki prasyarat berikut:

1.  Aspose.CAD untuk Perpustakaan .NET: Pastikan Anda memiliki perpustakaan Aspose.CAD untuk .NET yang terintegrasi ke dalam proyek Anda. Anda dapat mengunduhnya dari[Di Sini](https://releases.aspose.com/cad/net/).

2. Lingkungan Pengembangan: Siapkan lingkungan pengembangan .NET, seperti Visual Studio, dengan konfigurasi yang diperlukan.

Sekarang setelah Anda mengurutkan prasyaratnya, mari beralih ke mengimpor namespace yang diperlukan.

## Impor Namespace

Dalam kode Anda, sertakan namespace berikut:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadConsts;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using static Aspose.CAD.Examples.CSharp.DWG_Drawings.SupportMLeaderEntityForDWGFormat;
using Aspose.CAD.ImageOptions;
```

Namespace ini menyediakan kelas penting untuk bekerja dengan gambar CAD dan opsi rasterisasi.

## Langkah 1: Siapkan Proyek Anda

Sebelum mendalami kodenya, buat proyek baru atau buka proyek yang sudah ada di lingkungan pengembangan .NET pilihan Anda.

## Langkah 2: Tambahkan Referensi Aspose.CAD

Referensikan perpustakaan Aspose.CAD di proyek Anda. Anda dapat melakukan ini dengan menambahkan file DLL Aspose.CAD yang diunduh.

## Langkah 3: Inisialisasi Jalur

Tetapkan jalur ke direktori dokumen Anda tempat file IGES berada:

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "figa2.igs";
```

## Langkah 4: Muat Gambar CAD

 Gunakan Aspose.CAD`Image.Load` metode untuk memuat file IGES:

```csharp
using (Image cadImage = Image.Load(sourceFilePath))
{
    // Kode Anda ada di sini
}
```

## Langkah 5: Konfigurasikan Opsi Rasterisasi

Tentukan opsi rasterisasi untuk menyesuaikan keluaran PDF:

```csharp
CadRasterizationOptions options = new CadRasterizationOptions
{
    PageHeight = 1000,
    PageWidth = 1000,
};

PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = options;
```

## Langkah 6: Simpan sebagai PDF

Simpan gambar CAD sebagai file PDF dengan opsi yang ditentukan:

```csharp
cadImage.Save(MyDir + "figa2.pdf", pdfOptions);
```

Dengan enam langkah mudah ini, Anda telah berhasil mengekspor file IGES ke PDF menggunakan Aspose.CAD untuk .NET.

## Kesimpulan

Dalam tutorial ini, kami telah menjelajahi cara mulus untuk mengonversi file IGES ke PDF menggunakan Aspose.CAD untuk .NET. Panduan langkah demi langkah memastikan proses yang lancar dan efisien, memberdayakan Anda untuk menangani file CAD dengan presisi.


## FAQ

### Q1: Dapatkah saya menggunakan Aspose.CAD untuk .NET dalam aplikasi web?

A1: Ya, Aspose.CAD untuk .NET cocok untuk aplikasi desktop dan web, memberikan solusi serbaguna untuk manipulasi file CAD.

### Q2: Di mana saya dapat menemukan dokumentasi tambahan untuk Aspose.CAD?

 A2: Jelajahi dokumentasi yang komprehensif[Di Sini](https://reference.aspose.com/cad/net/) untuk wawasan mendetail tentang Aspose.CAD untuk .NET.

### Q3: Apakah tersedia uji coba gratis?

 A3: Ya, Anda dapat mengakses uji coba gratis[Di Sini](https://releases.aspose.com/) untuk merasakan kemampuan Aspose.CAD untuk .NET.

### Q4: Bagaimana cara mendapatkan lisensi sementara?

 A4: Untuk lisensi sementara, kunjungi[Link ini](https://purchase.aspose.com/temporary-license/) untuk mendapatkan informasi perizinan yang diperlukan.

### Q5: Butuh bantuan atau punya pertanyaan?

A5: Bergabunglah dengan komunitas Aspose.CAD di[forum dukungan](https://forum.aspose.com/c/cad/19) untuk bantuan dan diskusi segera.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
