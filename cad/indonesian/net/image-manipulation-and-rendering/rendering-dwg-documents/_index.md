---
date: 2026-08-23
description: Pelajari cara membuat viewport DWG C# menggunakan Aspose.CAD. Panduan
  ini mencakup loading file DWG, mengonfigurasi rasterization, defining viewport,
  dan saving hasil sebagai PDF.
keywords:
- create viewport dwg c#
- render dwg c#
- aspose.cad .net
lastmod: 2026-08-23
linktitle: Merender Dokumen DWG dalam C#
og_description: Pelajari cara membuat viewport DWG C# menggunakan Aspose.CAD di .NET.
  Panduan langkah‑demi‑langkah ini menunjukkan loading, rasterizing, defining viewports,
  dan saving ke PDF.
og_image_alt: Guide showing how to create viewport dwg c# with Aspose.CAD in .NET
og_title: Cara membuat viewport DWG C# dengan Aspose.CAD untuk .NET
schemas:
- author: Aspose
  dateModified: '2026-08-23'
  description: Learn how to create viewport dwg c# using Aspose.CAD. This guide covers
    loading a DWG file, configuring rasterization, defining a viewport, and saving
    the result as PDF.
  headline: How to create viewport dwg c# with Aspose.CAD for .NET
  type: TechArticle
- questions:
  - answer: Load the DWG file with `CadImage.Load`.
    question: What is the first step?
  - answer: '`Viewport` inside `CadRasterizationOptions`.'
    question: Which class defines the view area?
  - answer: Yes, using `PdfOptions` after rasterization.
    question: Can I output to PDF?
  - answer: A commercial license is required; a free trial works for evaluation.
    question: Do I need a license for production?
  - answer: Absolutely – Aspose.CAD works with .NET Framework, .NET Core, and .NET 5/6.
    question: Is .NET Core supported?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- create viewport dwg c#
- Aspose.CAD
- C# CAD rendering
- DWG to PDF
- CAD viewports
title: Cara membuat viewport DWG C# dengan Aspose.CAD untuk .NET
url: /id/net/image-manipulation-and-rendering/rendering-dwg-documents/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Merender dokumen DWG di C# – tutorial membuat viewport dwg c#

## Pendahuluan

Dalam tutorial komprehensif ini Anda akan belajar cara **create viewport dwg c#** dengan Aspose.CAD dan merender file DWG ke PDF. Baik Anda perlu mengekstrak layout tertentu, menghasilkan lembar yang dapat dicetak, atau menyematkan tampilan CAD dalam laporan, mengontrol viewport memberi Anda kontrol rendering yang tepat. Aspose.CAD mendukung **20+ CAD formats** dan dapat memproses file dengan ribuan entitas tanpa memuat seluruh dokumen ke memori, menjadikannya ideal untuk aplikasi .NET berkinerja tinggi.

## Jawaban Cepat

- **Apa langkah pertama?** Muat file DWG dengan `CadImage.Load`.
- **Kelas mana yang mendefinisikan area tampilan?** `Viewport` di dalam `CadRasterizationOptions`.
- **Apakah saya dapat output ke PDF?** Ya, menggunakan `PdfOptions` setelah rasterisasi.
- **Apakah saya memerlukan lisensi untuk produksi?** Lisensi komersial diperlukan; percobaan gratis dapat digunakan untuk evaluasi.
- **Apakah .NET Core didukung?** Tentu – Aspose.CAD bekerja dengan .NET Framework, .NET Core, dan .NET 5/6.

## Prasyarat

Sebelum menyelam ke kode, pastikan Anda memiliki:

- Pengetahuan dasar tentang pemrograman C#.
- Visual Studio (edisi terbaru apa pun) terpasang.
- Pustaka Aspose.CAD ditambahkan ke proyek Anda. Anda dapat mengunduhnya dari [Aspose.CAD download page](https://releases.aspose.com/cad/net/).
- File DWG contoh seperti **Bottom_plate.dwg** untuk diikuti.

## Impor namespace

Tambahkan direktif `using` yang diperlukan di bagian atas file C# Anda agar kompiler dapat menemukan tipe Aspose.CAD.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
using Aspose.CAD.FileFormats.Cad.CadTables;
using Aspose.CAD.FileFormats.Cad;
```

Setelah lingkungan siap, mari kita jalani implementasinya langkah demi langkah.

## Cara membuat viewport dwg c#?

Untuk membuat viewport khusus, pertama muat file DWG ke dalam objek `CadImage`, kemudian konfigurasikan `CadRasterizationOptions` dengan layout dan skala yang diinginkan. Tentukan wilayah yang ingin ditampilkan, buat instance `CadVportTableObject` dengan pusat, tinggi, dan rasio aspek yang dihitung, ganti viewport aktif, atur opsi PDF apa pun, dan akhirnya simpan hasilnya.

## Langkah 1: muat file dwg

`CadImage.Load` memuat file DWG ke dalam objek `CadImage`, yang mewakili gambar CAD dalam memori.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Bottom_plate.dwg";
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Your code for loading the DWG file goes here.
}
```

## Langkah 2: konfigurasikan opsi rasterisasi

`CadRasterizationOptions` menentukan bagaimana gambar CAD dirasterisasi, termasuk pemilihan layout, skala, dan ukuran output.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.Layouts = new string[] { "Model" };
rasterizationOptions.NoScaling = true;
// Additional rasterization configurations can be added here.
```

## Langkah 3: definisikan wilayah untuk digambar

`Point` mendefinisikan koordinat X dan Y dari sudut kiri‑atas wilayah yang akan dirender.

```csharp
Point topLeft = new Point(6156, 7053);
double width = 3108;
double height = 2489;
```

## Langkah 4: buat viewport baru

`CadVportTableObject` mewakili objek viewport yang mengontrol area tampilan dan rasio aspek dari gambar yang dirender.

```csharp
CadVportTableObject newView = new CadVportTableObject();
newView.Name.Value = "*Active";
newView.CenterPoint.X = topLeft.X + width / 2f;
newView.CenterPoint.Y = topLeft.Y - height / 2f;
newView.ViewHeight.Value = height;
newView.ViewAspectRatio.Value = width / height;
```

## Langkah 5: ganti viewport aktif

Loop ini menggantikan viewport aktif dengan yang baru dibuat untuk menerapkan pengaturan tampilan khusus.

```csharp
for (int i = 0; i < cadImage.ViewPorts.Count; i++)
{
    CadVportTableObject currentView = (CadVportTableObject)(cadImage.ViewPorts[i]);
    if ((currentView.Name.Value == null && cadImage.ViewPorts.Count == 1) ||
    string.Equals(currentView.Name.Value.ToLowerInvariant(), "*active"))
    {
        cadImage.ViewPorts[i] = newView;
        break;
    }
}
```

## Langkah 6: konfigurasikan opsi PDF

`PdfOptions` mengonfigurasi parameter output PDF seperti kompresi dan metadata.

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Langkah 7: simpan dwg yang dirender sebagai PDF

`image.Save` menulis gambar yang dirender ke file menggunakan opsi format yang ditentukan.

```csharp
cadImage.Save(MyDir, pdfOptions);
```

## Mengapa menggunakan viewport khusus saat merender DWG?

Viewport khusus memungkinkan Anda mengisolasi layout atau wilayah tertentu, mengurangi ukuran file dan meningkatkan kecepatan rendering. Aspose.CAD dapat merender DWG 300‑halaman dalam waktu kurang dari 2 detik ketika viewport terfokus digunakan, dibandingkan dengan rendering seluruh gambar yang mungkin memakan beberapa detik lebih lama.

## Masalah umum dan solusi

- **Blank output** – Pastikan koordinat viewport berada dalam batas gambar; gunakan `CadImage.Size` untuk memverifikasi batas.
- **Missing layers** – Atur `CadRasterizationOptions.Layouts` ke nama layout yang tepat; jika tidak, layout default mungkin kosong.
- **Performance slowdown** – Nonaktifkan anti‑aliasing di `CadRasterizationOptions` jika Anda hanya memerlukan pratinjau cepat.

## Pertanyaan yang sering diajukan

### Q1: Bisakah saya menggunakan Aspose.CAD dengan format file CAD lainnya?

A1: Ya, Aspose.CAD mendukung berbagai format, termasuk DWG, DXF, DWF, dan lebih dari 20 tipe CAD tambahan.

### Q2: Apakah Aspose.CAD kompatibel dengan .NET Core?

A2: Ya, Aspose.CAD bekerja dengan .NET Framework, .NET Core, dan rilis .NET terbaru.

### Q3: Bagaimana saya dapat menangani layout yang berbeda dalam file DWG?

A3: Tentukan layout yang diinginkan menggunakan properti `Layouts` dari `CadRasterizationOptions` sebelum merender.

### Q4: Apakah ada pertimbangan lisensi untuk menggunakan Aspose.CAD?

A4: Untuk detail lisensi, kunjungi [Aspose.CAD licensing page](https://purchase.aspose.com/buy).

### Q5: Di mana saya dapat menemukan dukungan tambahan?

A5: Kunjungi [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) untuk bantuan komunitas dan diskusi.

### Q6: Bisakah saya merender langsung ke PNG alih-alih PDF?

A6: Ya, ubah `PdfOptions` menjadi `PngOptions` dan panggil `image.Save("output.png", pngOptions)`.

### Q7: Bagaimana cara menyematkan gambar yang dirender ke dalam aplikasi Windows Forms?

A7: Muat gambar yang disimpan ke dalam kontrol `PictureBox` menggunakan `Image.FromFile("output.png")`.

## Kesimpulan

Anda sekarang tahu cara **create viewport dwg c#** dan merender file DWG ke PDF (atau format raster lainnya) menggunakan Aspose.CAD. Dengan menguasai manipulasi viewport Anda memperoleh kontrol detail atas output visual, yang penting untuk menghasilkan gambar teknik yang akurat, laporan, atau thumbnail. Jelajahi pengaturan rasterisasi tambahan, bereksperimen dengan format output yang berbeda, dan integrasikan kode ke dalam layanan .NET yang lebih besar atau utilitas desktop.

---

**Terakhir Diperbarui:** 2026-08-23  
**Diuji dengan:** Aspose.CAD 24.11 for .NET  
**Penulis:** Aspose

## Tutorial Terkait

- [Cara Mengatur Viewport saat Mengonversi DWG ke PDF dengan Koordinat di C# - Tutorial Aspose.CAD](/cad/net/conversion-and-export/converting-dwg-to-pdf-with-coordinates/)
- [Pelajari Cara Mengatur Opsi Rasterisasi CAD – Ekspor Layout Khusus ke PDF dengan Aspose.CAD](/cad/net/advanced-export-techniques/exporting-specific-layouts-to-pdf/)
- [Cara mengonversi DWG ke PDF dan Gambar Raster menggunakan Aspose.CAD untuk .NET](/cad/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}