---
title: Mengekspor DWF ke PDF - Panduan Aspose.CAD
linktitle: Mengekspor DWF ke PDF
second_title: Aspose.CAD .NET - Format File CAD dan BIM
description: Jelajahi panduan yang lancar tentang mengekspor DWF ke PDF menggunakan Aspose.CAD untuk .NET. Tingkatkan kemampuan penanganan file CAD Anda dengan mudah.
type: docs
weight: 10
url: /id/net/file-format-conversion/exporting-dwf-to-pdf/
---
## Perkenalan

Dalam dunia pengembangan .NET, Aspose.CAD menonjol sebagai perpustakaan yang kuat untuk menangani file Computer-Aided Design (CAD). Dalam tutorial ini, kita akan fokus pada tugas tertentu: mengekspor file DWF (Design Web Format) ke PDF menggunakan Aspose.CAD untuk .NET. Baik Anda seorang pengembang berpengalaman atau baru memulai, ikuti terus untuk mengintegrasikan fungsi ini ke dalam aplikasi Anda dengan lancar.

## Prasyarat

Sebelum masuk ke tutorial, pastikan Anda memiliki prasyarat berikut:

-  Aspose.CAD untuk .NET: Pastikan Anda telah menginstal Aspose.CAD untuk .NET. Anda dapat mengunduhnya dari[Di Sini](https://releases.aspose.com/cad/net/).

- Lingkungan Pengembangan: Siapkan lingkungan pengembangan .NET yang berfungsi, termasuk Visual Studio atau IDE pilihan lainnya.

## Impor Namespace

Mulailah dengan mengimpor namespace yang diperlukan ke dalam proyek Anda. Langkah ini penting untuk mengakses fungsionalitas yang disediakan oleh Aspose.CAD.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
```

## Langkah 1: Muat File DWF

Mulailah dengan memuat file DWF yang ingin Anda ekspor ke PDF. Sesuaikan jalur file.

```csharp
string MyDir = "Your Document Directory";
string fileName = MyDir + "18-12-11 9644 - site.dwf";

using (Image image = Image.Load(fileName))
{
    // Kode Anda di sini...
}
```

## Langkah 2: Konfigurasikan Opsi Rasterisasi

Atur opsi rasterisasi untuk DWF untuk memastikan keluaran yang diinginkan. Dalam contoh ini, kita menentukan tinggi dan lebar halaman.

```csharp
CadRasterizationOptions dwfRasterizationOptions = new CadRasterizationOptions();
dwfRasterizationOptions.PageHeight = 500;
dwfRasterizationOptions.PageWidth = 500;
```

## Langkah 3: Tentukan Opsi PDF

Buat opsi PDF dan kaitkan dengan opsi rasterisasi yang dikonfigurasi sebelumnya.

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = dwfRasterizationOptions;
```

## Langkah 4: Ekspor ke PDF

Jalankan proses ekspor, tentukan jalur keluaran untuk file PDF yang dihasilkan.

```csharp
string outPath = MyDir + "18-12-11 9644 - site.pdf";
image.Save(outPath, pdfOptions);
```

## Langkah 5: Verifikasi Ekspor

Pastikan ekspor gambar 3D ke PDF berhasil. Tampilkan pesan konfirmasi dengan jalur file yang disimpan.

```csharp
Console.WriteLine("\n3D images exported successfully to PDF.\nFile saved at " + MyDir);
```

Sekarang Anda telah berhasil mengimplementasikan fungsionalitas ekspor DWF ke PDF di aplikasi .NET Anda menggunakan Aspose.CAD.

## Kesimpulan

Dalam tutorial ini, kita menjelajahi proses mengekspor file DWF ke PDF menggunakan Aspose.CAD untuk .NET. Dengan mengikuti langkah-langkah ini, Anda dapat dengan mudah mengintegrasikan fungsi ini ke dalam proyek Anda, sehingga meningkatkan kemampuan penanganan file CAD Anda.

## FAQ

### Q1: Dapatkah saya menggunakan Aspose.CAD untuk .NET dengan format file CAD lainnya?

A1: Ya, Aspose.CAD mendukung berbagai format file CAD, termasuk DWG, DXF, DWF, dan banyak lagi. Periksa dokumentasi untuk daftar lengkap.

### Q2: Di mana saya dapat menemukan dukungan tambahan untuk Aspose.CAD?

 A2: Untuk dukungan tambahan, kunjungi[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19) tempat Anda dapat bertanya dan berinteraksi dengan komunitas.

### Q3: Apakah ada uji coba gratis yang tersedia untuk Aspose.CAD?

 A3: Ya, Anda dapat menjelajahi Aspose.CAD versi uji coba gratis dari[Di Sini](https://releases.aspose.com/).

### Q4: Bagaimana cara mendapatkan lisensi sementara untuk Aspose.CAD?

 A4: Anda bisa mendapatkan lisensi sementara dari[Link ini](https://purchase.aspose.com/temporary-license/).

### Q5: Di mana saya dapat membeli versi lengkap Aspose.CAD untuk .NET?

 A5: Anda dapat membeli versi lengkap Aspose.CAD untuk .NET dari[Di Sini](https://purchase.aspose.com/buy).