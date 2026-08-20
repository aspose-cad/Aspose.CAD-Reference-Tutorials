---
date: 2026-03-29
description: Pelajari cara membuat PDF dari CAD, mengatur ukuran kanvas, dan mengekspor
  CAD ke PDF atau TIFF menggunakan Aspose.CAD untuk .NET dalam panduan langkah demi
  langkah ini.
linktitle: Setting Canvas Size and Mode
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: 'Cara Membuat PDF dari CAD: Mengatur Ukuran Kanvas dan Mode di Aspose.CAD untuk
  .NET'
url: /id/net/cad-features-and-support/setting-canvas-size-and-mode/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Mengatur Ukuran Kanvas dan Mode di Aspose.CAD untuk .NET

## Pendahuluan

Siap untuk **create PDF from CAD** file sambil mengontrol dimensi output? Dalam tutorial ini kami akan menjelaskan cara mengatur ukuran kanvas dan mode, memuat file CAD, serta mengekspornya ke PDF atau TIFF dengan Aspose.CAD untuk .NET. Baik Anda perlu **convert DXF to PDF**, menghasilkan gambar beresolusi tinggi, atau sekadar menyesuaikan area rasterisasi, langkah-langkah di bawah ini akan memberikan solusi yang solid dan siap produksi.

## Jawaban Cepat
- **Apa arti “create PDF from CAD”?** Mengonversi gambar CAD (mis., DXF, DWG) menjadi dokumen PDF yang mempertahankan detail vektor dan raster.  
- **Opsi mana yang mengontrol ukuran output?** `CadRasterizationOptions.PageWidth` dan `PageHeight` (ukuran kanvas).  
- **Bisakah saya mengekspor ke TIFF juga?** Ya – gunakan `TiffOptions` dengan pengaturan rasterisasi yang sama.  
- **Apakah saya memerlukan lisensi untuk produksi?** Lisensi komersial diperlukan; versi percobaan gratis tersedia.  
- **Versi .NET yang didukung?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.

## Apa itu “create PDF from CAD”?
Membuat PDF dari CAD berarti merender gambar CAD ke dalam format berorientasi halaman (PDF) yang dapat dilihat, dicetak, atau dibagikan tanpa memerlukan perangkat lunak CAD. Aspose.CAD menangani proses berat, memungkinkan Anda menentukan ukuran kanvas, skala, dan format output.

## Mengapa mengatur ukuran kanvas saat membuat PDF dari CAD?
Mengatur ukuran kanvas memberi Anda kontrol yang tepat atas resolusi dan dimensi PDF atau TIFF yang dihasilkan. Ini sangat berguna ketika:
- Menyiapkan gambar untuk pencetakan pada ukuran kertas tertentu.  
- Membuat thumbnail atau gambar beresolusi tinggi untuk pratinjau web.  
- Menjamin tata letak yang konsisten di seluruh dokumen.

## Prasyarat

- Aspose.CAD Library: Unduh dan instal pustaka Aspose.CAD dari [situs Aspose.CAD](https://releases.aspose.com/cad/net/).
- Development Environment: Pastikan Anda memiliki lingkungan pengembangan .NET yang terpasang di mesin Anda.
- Sample CAD File: Untuk tutorial ini, kami akan menggunakan file DXF contoh. Anda dapat menemukan satu di [dokumentasi Aspose.CAD](https://reference.aspose.com/cad/net/).

## Impor Namespace

Pertama, impor namespace yang diperlukan untuk pemrosesan CAD:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Cara Membuat PDF dari CAD dengan Ukuran Kanvas Kustom

### Langkah 1: Muat File CAD

Kita mulai dengan **memuat file CAD** (mis., DXF) ke dalam objek `Image`. Ini adalah titik di mana Anda **memuat file CAD** ke memori.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

using (Image image = Image.Load(sourceFilePath))
{
    // Your code for further steps will go here
}
```

### Langkah 2: Buat CadRasterizationOptions

Buat instance `CadRasterizationOptions` dan tentukan ukuran kanvas. Properti `PageWidth` dan `PageHeight` memungkinkan Anda **mengatur ukuran kanvas** ke dimensi tepat yang Anda butuhkan.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
rasterizationOptions.AutomaticLayoutsScaling = true;
rasterizationOptions.NoScaling = false;
```

### Langkah 3: Buat PdfOptions (Ekspor CAD ke PDF)

Hubungkan pengaturan rasterisasi ke objek `PdfOptions`. Konfigurasi ini memungkinkan Anda **mengekspor CAD ke PDF** dengan kanvas kustom yang telah Anda tentukan.

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

### Langkah 4: Ekspor ke PDF (Konversi DXF ke PDF)

Sekarang simpan gambar sebagai PDF. Langkah ini **membuat PDF dari CAD** menggunakan opsi yang telah kami atur.

```csharp
image.Save(MyDir + "result_out.pdf", pdfOptions);
```

### Langkah 5: Buat TiffOptions (Ekspor CAD ke TIFF)

Jika Anda juga memerlukan gambar raster, konfigurasikan `TiffOptions`. Opsi rasterisasi yang sama digunakan kembali, sehingga **ekspor CAD ke TIFF** menghormati ukuran kanvas.

```csharp
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.VectorRasterizationOptions = rasterizationOptions;
```

### Langkah 6: Ekspor ke TIFF

Terakhir, simpan gambar sebagai file TIFF.

```csharp
image.Save(MyDir + "result_out.tiff", tiffOptions);
```

## Masalah Umum dan Solusinya

- **Canvas appears cropped** – Verifikasi bahwa `AutomaticLayoutsScaling` diatur ke `true` dan `NoScaling` ke `false` sehingga gambar berskala menyesuaikan kanvas.  
- **Low‑resolution PDF** – Tingkatkan `PageWidth`/`PageHeight` atau atur `Resolution` pada `CadRasterizationOptions`.  
- **File not found error** – Pastikan `MyDir` mengarah ke direktori yang valid dan nama file DXF cocok persis.

## Pertanyaan yang Sering Diajukan

### Q1: Bisakah saya menggunakan Aspose.CAD dengan perpustakaan .NET lainnya?
A1: Ya, Aspose.CAD terintegrasi secara mulus dengan perpustakaan .NET lainnya, memberikan kemampuan yang ditingkatkan untuk manipulasi CAD.

### Q2: Apakah tersedia percobaan gratis untuk Aspose.CAD?
A2: Ya, Anda dapat menjelajahi fitur Aspose.CAD dengan percobaan gratis. Kunjungi [di sini](https://releases.aspose.com/) untuk memulai.

### Q3: Bagaimana saya dapat mendapatkan dukungan untuk Aspose.CAD?
A3: Untuk dukungan dan diskusi, kunjungi [forum Aspose.CAD](https://forum.aspose.com/c/cad/19).

### Q4: Di mana saya dapat menemukan dokumentasi lengkap untuk Aspose.CAD?
A4: Lihat [dokumentasi Aspose.CAD](https://reference.aspose.com/cad/net/) untuk informasi detail dan contoh.

### Q5: Bagaimana cara membeli Aspose.CAD untuk .NET?
A5: Untuk membeli Aspose.CAD, kunjungi [halaman pembelian](https://purchase.aspose.com/buy).

**Q: Bisakah saya mengekspor gambar CAD multi‑halaman ke satu PDF?**  
A: Ya. Atur `PageCount` dalam `CadRasterizationOptions` dan pustaka akan menggabungkan halaman menjadi satu PDF.

**Q: Apakah ukuran kanvas memengaruhi kualitas data vektor?**  
A: Data vektor tetap independen dari resolusi; ukuran kanvas hanya memengaruhi elemen rasterisasi dan resolusi gambar.

**Last Updated:** 2026-03-29  
**Tested With:** Aspose.CAD 24.11 for .NET  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}