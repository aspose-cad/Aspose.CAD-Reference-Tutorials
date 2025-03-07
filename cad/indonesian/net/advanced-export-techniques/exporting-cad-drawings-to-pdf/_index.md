---
title: Mengekspor Gambar CAD ke PDF - Tutorial Aspose.CAD
linktitle: Mengekspor Gambar CAD ke PDF
second_title: Aspose.CAD .NET - Format File CAD dan BIM
description: Ekspor gambar CAD ke PDF secara lancar dengan Aspose.CAD untuk .NET. Ikuti panduan langkah demi langkah kami untuk konversi yang efisien.
weight: 14
url: /id/net/advanced-export-techniques/exporting-cad-drawings-to-pdf/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Mengekspor Gambar CAD ke PDF - Tutorial Aspose.CAD

## Perkenalan

Dalam dunia desain berbantuan komputer (CAD) yang terus berkembang, kebutuhan untuk mengekspor gambar rumit ke berbagai format adalah hal yang sangat penting. Aspose.CAD untuk .NET hadir untuk menyelamatkan, menyediakan seperangkat alat canggih untuk mengonversi gambar CAD ke PDF dengan lancar. Dalam tutorial ini, kita akan mempelajari proses mengekspor gambar CAD ke PDF menggunakan Aspose.CAD untuk .NET, menguraikan setiap langkah untuk memastikan pengalaman belajar yang lancar dan komprehensif.

## Prasyarat

Sebelum kita mendalami tutorialnya, pastikan Anda memiliki prasyarat berikut:

-  Aspose.CAD untuk Perpustakaan .NET: Pastikan Anda telah menginstal perpustakaan Aspose.CAD untuk .NET. Anda dapat mengunduhnya dari[situs web](https://releases.aspose.com/cad/net/).

- File Gambar CAD: Siapkan file gambar CAD untuk dikonversi. Dalam contoh ini, kita akan menggunakan "Bottom_plate.dwg."

- Lingkungan Pengembangan: Siapkan lingkungan pengembangan .NET, seperti Visual Studio, untuk mengeksekusi kode yang disediakan.

## Impor Namespace

Mulailah dengan mengimpor namespace yang diperlukan untuk memanfaatkan fungsionalitas Aspose.CAD untuk .NET. Tambahkan baris kode berikut ke awal proyek Anda:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Langkah 1: Muat Gambar CAD

Mulailah dengan memuat gambar CAD menggunakan perpustakaan Aspose.CAD. Gunakan cuplikan kode berikut:

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Bottom_plate.dwg";

using (Image image = Image.Load(sourceFilePath))
{
    // Kode untuk langkah selanjutnya akan dimasukkan di sini.
}
```

## Langkah 2: Tetapkan Opsi Rasterisasi

 Buat sebuah contoh dari`CadRasterizationOptions` dan atur propertinya untuk menyesuaikan proses rasterisasi. Ini menentukan tampilan file PDF yang diekspor.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.BackgroundColor = Color.White;
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
```

## Langkah 3: Atur Opsi PDF

 Buat sebuah contoh dari`PdfOptions` dan mengaitkan yang telah ditentukan sebelumnya`CadRasterizationOptions` dengan itu.

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Langkah 4: Ekspor ke PDF

Tentukan jalur keluaran untuk file PDF dan jalankan proses ekspor.

```csharp
MyDir = MyDir + "Bottom_plate_out.pdf";
image.Save(MyDir, pdfOptions);
```

## Langkah 5: Pesan Penyelesaian

Tampilkan pesan yang menunjukkan keberhasilan ekspor file DWG ke PDF.

```csharp
Console.WriteLine("\nThe DWG file exported successfully to PDF.\nFile saved at " + MyDir);
```

## Kesimpulan

Selamat! Anda telah berhasil mempelajari cara mengekspor gambar CAD ke PDF menggunakan Aspose.CAD untuk .NET. Proses efisien ini memastikan bahwa desain rumit Anda mudah dibagikan dan diakses dalam format PDF yang diterima secara universal.

## FAQ

### Q1: Bisakah saya menggunakan Aspose.CAD untuk .NET di lingkungan Windows dan Linux?

A1: Ya, Aspose.CAD untuk .NET kompatibel dengan platform Windows dan Linux.

### Q2: Apakah ada batasan ukuran atau kompleksitas gambar CAD untuk konversi ini?

A2: Aspose.CAD untuk .NET dirancang untuk menangani gambar dengan berbagai ukuran dan kompleksitas secara efisien.

### Q3: Dapatkah saya menyesuaikan tampilan PDF yang diekspor?

 A3: Tentu saja! Itu`CadRasterizationOptions` memungkinkan Anda menyesuaikan aspek visual dari keluaran PDF.

### Q4: Apakah ada versi uji coba yang tersedia untuk Aspose.CAD untuk .NET?

 A4: Ya, Anda dapat menjelajahi fitur-fiturnya dengan[versi percobaan gratis](https://releases.aspose.com/).

### Q5: Di mana saya bisa mencari bantuan jika saya menemui masalah selama proses tersebut?

A5: Kunjungi[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19) untuk dukungan khusus dan kolaborasi komunitas.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
