---
title: Mengekspor File DGN Tertanam - Tutorial Aspose.CAD
linktitle: Mengekspor File DGN Tersemat
second_title: Aspose.CAD .NET - Format File CAD dan BIM
description: Jelajahi kekuatan Aspose.CAD untuk .NET. Pelajari cara mengekspor file DGN yang disematkan ke PDF dengan mudah dengan tutorial langkah demi langkah ini.
weight: 14
url: /id/net/export-techniques/exporting-embedded-dgn-files/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Mengekspor File DGN Tertanam - Tutorial Aspose.CAD

## Perkenalan

Dalam dunia pengembangan perangkat lunak yang dinamis, Aspose.CAD untuk .NET menonjol sebagai alat yang ampuh untuk menangani file Computer-Aided Design (CAD). Tutorial ini akan memandu Anda melalui proses mengekspor file DGN yang disematkan menggunakan Aspose.CAD untuk .NET. Baik Anda seorang pengembang berpengalaman atau pemula yang penasaran, panduan langkah demi langkah ini akan membantu Anda memanfaatkan kemampuan Aspose.CAD secara efektif.

## Prasyarat

Sebelum masuk ke tutorial, pastikan Anda memiliki prasyarat berikut:

1.  Aspose.CAD untuk .NET: Unduh dan instal perpustakaan dari[Aspose.CAD untuk .NET](https://releases.aspose.com/cad/net/).

2. Lingkungan Pengembangan: Siapkan lingkungan pengembangan .NET dengan Visual Studio atau IDE pilihan lainnya.

3. Contoh File DXF: Untuk tutorial ini, kami akan menggunakan file "conic_pyramid.dxf". Pastikan Anda menyediakannya di direktori dokumen yang Anda tunjuk.

## Impor Namespace

Dalam kode C# Anda, pastikan untuk mengimpor namespace yang diperlukan:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
```

## Langkah 1: Muat File DXF

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    //Kode Anda untuk langkah selanjutnya akan ditempatkan di sini
}
```

## Langkah 2: Tetapkan Opsi Rasterisasi

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.Layouts = new[] { "Model" };
```

## Langkah 3: Atur Opsi PDF

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Langkah 4: Simpan sebagai PDF

```csharp
cadImage.Save(MyDir + "conic_pyramid.pdf", pdfOptions);
```

## Langkah 5: Tampilkan Pesan Sukses

```csharp
Console.WriteLine("\nThe DXF drawing exported successfully to PDF.\nFile saved at " + MyDir);
```

## Kesimpulan

Selamat! Anda telah berhasil mengekspor file DGN yang disematkan ke PDF menggunakan Aspose.CAD untuk .NET. Tutorial ini mencakup langkah-langkah penting, memberi Anda landasan untuk menjelajahi fungsionalitas lebih lanjut yang ditawarkan oleh Aspose.CAD.

## FAQ

### Q1: Bisakah saya menggunakan Aspose.CAD untuk .NET dengan bahasa pemrograman lain?

A1: Aspose.CAD terutama mendukung .NET, namun Aspose menyediakan perpustakaan untuk berbagai bahasa, termasuk Java dan Python.

### Q2: Apakah ada uji coba gratis yang tersedia untuk Aspose.CAD untuk .NET?

 A2: Ya, Anda bisa mendapatkan uji coba gratis[Di Sini](https://releases.aspose.com/).

### Q3: Di mana saya dapat menemukan dokumentasi komprehensif untuk Aspose.CAD untuk .NET?

 A3: Lihat dokumentasi[Di Sini](https://reference.aspose.com/cad/net/).

### Q4: Bagaimana cara mendapatkan lisensi sementara untuk Aspose.CAD untuk .NET?

 A4: Dapatkan lisensi sementara[Di Sini](https://purchase.aspose.com/temporary-license/).

### Q5: Butuh bantuan atau ingin terlibat dengan komunitas?

A5: Kunjungi[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19) untuk dukungan dan diskusi.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
