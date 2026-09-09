---
date: 2026-09-09
description: Pelajari cara menggunakan Aspose CAD export untuk mengonversi tata letak
  DXF tertentu ke JPEG atau PNG di .NET. Ikuti petunjuk langkah demi langkah untuk
  hasil cepat.
keywords:
- aspose cad export
- how to export dxf
- convert dxf to jpeg
- batch export dxf
- convert dwf to jpeg
lastmod: 2026-09-09
linktitle: Mengekspor Tata Letak DXF Tertentu ke Gambar
og_description: Pelajari cara menggunakan Aspose CAD export untuk mengonversi tata
  letak DXF tertentu ke JPEG atau PNG di .NET. Ikuti petunjuk langkah demi langkah
  untuk hasil cepat.
og_image_alt: Tutorial showing Aspose CAD export of DXF layout to JPEG image in .NET
og_title: Aspose CAD export – mengekspor tata letak DXF tertentu ke gambar
schemas:
- author: Aspose
  dateModified: '2026-09-09'
  description: Learn how to use Aspose CAD export to convert a specific DXF layout
    to JPEG or PNG in .NET. Follow step‑by‑step instructions for fast results.
  headline: Aspose CAD export – exporting a specific DXF layout to an image
  type: TechArticle
- description: Learn how to use Aspose CAD export to convert a specific DXF layout
    to JPEG or PNG in .NET. Follow step‑by‑step instructions for fast results.
  name: Aspose CAD export – exporting a specific DXF layout to an image
  steps:
  - name: set up your project
    text: Create a new .NET project or open an existing one where you plan to implement
      the Aspose.CAD functionality.
  - name: load CAD image
    text: 'Use the following code to load a CAD image from your specified file path:'
  - name: configure rasterization options
    text: 'Set up the rasterization options, specifying the page width and height:'
  - name: iterate over layers
    text: 'Retrieve the layers from the CAD image and iterate through them:'
  - name: export layers to images
    text: For each layer, export it to a JPEG image using the configured options.
      The `JpegOptions` class defines JPEG‑specific settings such as quality and compression
      level. Repeat these steps for each layer in the CAD image.
  type: HowTo
- questions:
  - answer: Yes – you can script a folder scan and call the same export routine for
      each file; the library is optimized for high‑throughput scenarios.
    question: Does Aspose CAD export support batch processing of thousands of files?
  - answer: Absolutely – set the `JpegQuality` property in `RasterizationOptions`
      to a value between 0 and 100.
    question: Can I control the JPEG quality level?
  - answer: Yes – change the `Save` format to `SaveFormat.Png` and adjust any transparency
      settings as needed.
    question: Is it possible to export a layout as a PNG instead of JPEG?
  - answer: Aspose.CAD supports .NET Framework 4.5+, .NET Core 3.1+, .NET 5, .NET
      6 and later.
    question: What .NET versions are officially supported?
  - answer: The engine streams pages to disk and never loads the full document into
      memory, allowing processing of multi‑gigabyte files on modest hardware.
    question: How does Aspose CAD export handle very large drawings?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- aspose cad
- dxf export
- cad to image
- c# cad processing
- cad conversion
title: Aspose CAD export – mengekspor tata letak DXF tertentu ke gambar
url: /id/net/layout-and-object-handling/exporting-specific-dxf-layout-to-image/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ekspor Aspose CAD – mengekspor tata letak DXF tertentu ke gambar

## Pendahuluan

Ekspor Aspose CAD memungkinkan Anda mengonversi gambar CAD, termasuk tata letak DXF individual, langsung ke gambar raster seperti JPEG atau PNG tanpa memerlukan perangkat lunak CAD pihak ketiga. Dalam tutorial ini Anda akan belajar cara memuat file DXF, memilih tata letak yang Anda butuhkan, dan mengekspornya ke gambar menggunakan beberapa baris kode .NET.

## Jawaban Cepat
- **Library apa yang diperlukan?** Aspose.CAD for .NET (komponen ekspor Aspose CAD).  
- **Bisakah saya mengekspor hanya satu tata letak?** Ya – Anda dapat memilih tata letak tertentu sebelum rasterisasi.  
- **Format output yang didukung?** JPEG, PNG, BMP, TIFF, dan lainnya.  
- **Apakah lisensi diperlukan untuk produksi?** Lisensi Aspose.CAD yang valid diperlukan untuk penggunaan non‑trial.  
- **Apakah akan bekerja pada .NET 6+?** Tentu – perpustakaan menargetkan .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.

## Apa itu Ekspor Aspose CAD?

Ekspor Aspose CAD adalah bagian dari perpustakaan Aspose.CAD yang mengonversi file CAD dan BIM menjadi gambar raster atau vektor. Ia menyediakan API satu‑panggilan untuk merender tata letak, halaman, atau lapisan apa pun tanpa menginstal AutoCAD. Komponen ini juga mendukung pemrosesan batch, output resolusi tinggi, dan opsi rendering lanjutan seperti anti‑aliasing dan kontrol warna latar belakang.

## Mengapa menggunakan Ekspor Aspose CAD untuk konversi DXF?

Ekspor Aspose CAD mendukung **lebih dari 30 format CAD/BIM** dan dapat merender file dengan hingga **10 000 halaman** sambil menjaga penggunaan memori di bawah **50 MB** dengan streaming data. Mesin ini mempertahankan ketebalan garis, warna, dan pola hatch, menghasilkan output JPEG yang pixel‑perfect yang cocok dengan gambar asli. Ia juga menghilangkan kebutuhan akan instalasi CAD desktop yang mahal, menjadikan pipeline konversi otomatis sederhana dan hemat biaya.

## Prasyarat

- Aspose.CAD Library: Unduh dan instal perpustakaan Aspose.CAD dari [halaman rilis](https://releases.aspose.com/cad/net/).  
- Lingkungan Pengembangan: Pastikan Anda memiliki lingkungan pengembangan .NET yang terpasang di mesin Anda.

## Impor namespace

Dalam proyek .NET Anda, mulailah dengan mengimpor namespace yang diperlukan untuk mengakses fungsionalitas yang disediakan oleh Aspose.CAD:

```csharp
using System;
```

## Cara mengekspor tata letak DXF tertentu ke gambar?

Muat file DXF, pilih tata letak yang diinginkan, konfigurasikan opsi rasterisasi, lalu simpan hasilnya sebagai gambar. Seluruh proses hanya memerlukan beberapa pemanggilan metode dan berjalan dalam waktu kurang dari satu detik untuk gambar tipikal. Kelas `CadImage` mewakili gambar CAD yang dimuat ke memori, memberikan akses ke lapisan, tata letak, dan opsi renderingnya.

### Langkah 1: siapkan proyek Anda
Buat proyek .NET baru atau buka proyek yang sudah ada di mana Anda berencana mengimplementasikan fungsionalitas Aspose.CAD.

### Langkah 2: muat gambar CAD
Gunakan kode berikut untuk memuat gambar CAD dari jalur file yang Anda tentukan:

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "for_layers_test.dwf";

using (var image = (Aspose.CAD.FileFormats.Cad.CadImage)Aspose.CAD.Image.Load(sourceFilePath))
{
    // Your code for further steps will go here.
}
```

### Langkah 3: konfigurasikan opsi rasterisasi
Atur opsi rasterisasi, menentukan lebar dan tinggi halaman:

```csharp
var rasterizationOptions = new Aspose.CAD.ImageOptions.CadRasterizationOptions();
rasterizationOptions.PageWidth = 500;
rasterizationOptions.PageHeight = 500;
```

### Langkah 4: iterasi lapisan
Ambil lapisan dari gambar CAD dan iterasi melalui mereka:

```csharp
var layersList = image.Layers;
foreach (var layerName in layersList.GetLayersNames())
{
    // Your code for further steps will go here.
}
```

### Langkah 5: ekspor lapisan ke gambar
Untuk setiap lapisan, ekspor ke gambar JPEG menggunakan opsi yang telah dikonfigurasikan. Kelas `JpegOptions` mendefinisikan pengaturan khusus JPEG seperti kualitas dan tingkat kompresi.

```csharp
rasterizationOptions.Layers = new string[] { layerName };
var options = new Aspose.CAD.ImageOptions.JpegOptions();
options.VectorRasterizationOptions = rasterizationOptions;
image.Save(layerName + "_out.jpg", options);
```

Ulangi langkah-langkah ini untuk setiap lapisan dalam gambar CAD.

## Cara mengekspor batch tata letak DXF ke gambar?

Anda dapat menempatkan semua file DXF dalam satu folder, mengulangi setiap file, memilih tata letak yang diinginkan, dan memanggil logika ekspor yang sama. Pendekatan ini memungkinkan Anda mengonversi puluhan gambar dalam satu kali jalan, ideal untuk pipeline otomatis. Dengan menggunakan kembali pengaturan rasterisasi dan penyimpanan yang sama, Anda memastikan kualitas output yang konsisten di seluruh batch.

## Cara mengonversi dwf ke jpeg dengan Aspose CAD?

Ekspor Aspose CAD juga menangani file DWF. Muat DWF menggunakan `CadImage.Load`, atur opsi rasterisasi yang sama, dan panggil `Save` dengan format JPEG. API-nya identik dengan alur kerja DXF, sehingga Anda dapat menggunakan kembali basis kode yang sama. Antarmuka seragam ini menyederhanakan konversi koleksi file CAD campuran tanpa cabang kode tambahan.

## Masalah umum dan solusi
- **Nama tata letak hilang:** Verifikasi bahwa pengidentifikasi tata letak cocok dengan nama yang ditampilkan di manajer lapisan file CAD.  
- **Lonjakan memori pada file besar:** Gunakan `CadImage.Load` dengan `LoadOptions` yang mengaktifkan streaming untuk menjaga memori tetap rendah.  
- **Warna tidak tepat:** Pastikan properti `BackgroundColor` dalam `RasterizationOptions` diatur ke `Color.White` jika Anda memerlukan kanvas putih.

## FAQ

### Q1: Bisakah saya menggunakan Aspose.CAD dengan kerangka .NET lainnya?
A1: Ya, Aspose.CAD kompatibel dengan berbagai kerangka .NET, memberikan fleksibilitas untuk kebutuhan pengembangan Anda.

### Q2: Apakah lisensi sementara tersedia untuk Aspose.CAD?
A2: Ya, Anda dapat memperoleh lisensi sementara untuk Aspose.CAD dari [halaman lisensi sementara](https://purchase.aspose.com/temporary-license/).

### Q3: Bagaimana saya dapat mendapatkan dukungan untuk Aspose.CAD?
A3: Kunjungi [forum Aspose.CAD](https://forum.aspose.com/c/cad/19) untuk mendapatkan dukungan komunitas dan bantuan.

### Q4: Apakah ada percobaan gratis untuk Aspose.CAD?
A4: Ya, Anda dapat menjelajahi percobaan gratis Aspose.CAD di [halaman percobaan gratis Aspose.CAD](https://releases.aspose.com/).

### Q5: Di mana saya dapat menemukan dokumentasi terperinci untuk Aspose.CAD?
A5: Referensikan dokumentasi lengkap [Aspose.CAD documentation](https://reference.aspose.com/cad/net/) untuk informasi mendalam.

## Pertanyaan yang Sering Diajukan

**Q: Apakah ekspor Aspose CAD mendukung pemrosesan batch ribuan file?**  
A: Ya – Anda dapat menulis skrip pemindaian folder dan memanggil rutin ekspor yang sama untuk setiap file; perpustakaan dioptimalkan untuk skenario throughput tinggi.

**Q: Bisakah saya mengontrol tingkat kualitas JPEG?**  
A: Tentu – atur properti `JpegQuality` dalam `RasterizationOptions` ke nilai antara 0 dan 100.

**Q: Apakah memungkinkan mengekspor tata letak sebagai PNG alih-alih JPEG?**  
A: Ya – ubah format `Save` menjadi `SaveFormat.Png` dan sesuaikan pengaturan transparansi sesuai kebutuhan.

**Q: Versi .NET apa yang secara resmi didukung?**  
A: Aspose.CAD mendukung .NET Framework 4.5+, .NET Core 3.1+, .NET 5, .NET 6, dan selanjutnya.

**Q: Bagaimana ekspor Aspose CAD menangani gambar yang sangat besar?**  
A: Mesin melakukan streaming halaman ke disk dan tidak pernah memuat seluruh dokumen ke memori, memungkinkan pemrosesan file multi‑gigabyte pada perangkat keras yang sederhana.

**Last Updated:** 2026-09-09  
**Tested With:** Aspose.CAD 24.12 for .NET  
**Author:** Aspose

## Tutorial Terkait

- [Convert DXF to PNG with Aspose.CAD for .NET](/cad/net/cad-export-formats/export-cad-layouts-to-raster-image-formats/)
- [Aspose CAD Example: Convert Layouts to Raster Image in .NET](/cad/net/cad-drawing-manipulation/convert-layouts-to-raster-image/)
- [Learn to Set CAD Rasterization Options – Export Specific Layouts to PDF with Aspose.CAD](/cad/net/advanced-export-techniques/exporting-specific-layouts-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}