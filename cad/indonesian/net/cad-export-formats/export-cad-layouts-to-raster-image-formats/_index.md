---
date: 2026-03-21
description: Pelajari cara mengonversi dxf ke png dan format raster lainnya menggunakan
  Aspose.CAD untuk .NET. Ikuti panduan langkah demi langkah kami untuk ekspor lapisan
  CAD yang mulus.
linktitle: Export CAD Layouts to Raster Image Formats
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Konversi DXF ke PNG dengan Aspose.CAD untuk .NET
url: /id/net/cad-export-formats/export-cad-layouts-to-raster-image-formats/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ekspor Tata Letak CAD ke Format Gambar Raster di Aspose.CAD untuk .NET

## Pendahuluan

Apakah Anda ingin dengan efisien **convert dxf to png** dan format gambar raster lainnya menggunakan Aspose.CAD untuk .NET? Panduan langkah‑demi‑langkah ini akan memandu Anda melalui prosesnya, menyediakan instruksi terperinci dan potongan kode untuk membuat tugas ini lancar. Baik Anda seorang pengembang berpengalaman maupun pendatang baru di Aspose.CAD, tutorial ini melayani semua tingkat keahlian.

### Jawaban Cepat
- **Perpustakaan apa yang menangani konversi?** Aspose.CAD for .NET  
- **Format utama yang didukung secara bawaan?** JPEG, PNG, BMP, dan TIFF raster images  
- **Bisakah saya mengekspor lapisan CAD tertentu?** Yes – use `CadRasterizationOptions.Layers` to target individual layers  
- **Apakah saya memerlukan lisensi untuk produksi?** A valid Aspose.CAD license is required for non‑trial use  
- **Versi .NET yang didukung?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7  

## Apa itu **convert dxf to png**?

Mengonversi file DXF (Drawing Exchange Format) ke PNG berarti merasterkan data CAD berbasis vektor menjadi gambar berbasis piksel. Ini berguna ketika Anda perlu menyematkan gambar CAD dalam halaman web, laporan, atau lingkungan apa pun yang hanya mendukung grafik raster.

## Mengapa mengekspor lapisan CAD secara terpisah?

Mengekspor lapisan CAD secara individual memberi Anda kontrol granular atas output visual, mengurangi ukuran file untuk setiap gambar, dan memungkinkan Anda menerapkan gaya atau pemrosesan lanjutan khusus lapisan. Ini sangat berguna untuk gambar teknik besar di mana hanya sebagian lapisan yang relevan bagi audiens tertentu.

## Prasyarat

- **Aspose.CAD for .NET Library** – download it from the [Aspose.CAD website](https://releases.aspose.com/cad/net/).  
- **CAD Drawing File** – a DXF file (e.g., `conic_pyramid.dxf`) that you want to convert to raster formats.  

## Impor Namespace

Dalam proyek .NET Anda, impor namespace yang diperlukan untuk memanfaatkan fungsionalitas Aspose.CAD. Sertakan namespace berikut di awal kode Anda:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Cara **convert dxf to png** – Panduan Langkah‑demi‑Langkah

### Langkah 1: Muat Gambar CAD

Pertama, muat file DXF ke dalam objek `Image`. Objek ini mewakili seluruh gambar CAD dalam memori.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

// Load a CAD drawing in an instance of Image
using (var image = Image.Load(sourceFilePath))
{
    // Your code for loading the CAD drawing goes here
}
```

### Langkah 2: Buat `CadRasterizationOptions`

Konfigurasikan pengaturan rasterisasi seperti dimensi output dan resolusi. Opsi-opsi ini mengontrol bagaimana data vektor dirasterisasi.

```csharp
// Create an instance of CadRasterizationOptions
var rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 500;
rasterizationOptions.PageHeight = 500;
```

### Langkah 3: Tentukan Lapisan (Ekspor Lapisan CAD)

Jika Anda hanya membutuhkan lapisan tertentu, cantumkan namanya di sini. Ini menunjukkan **export cad layers** secara individual.

```csharp
// Add the layer name to the CadRasterizationOptions's layer list
rasterizationOptions.Layers = new string[] { "LayerA" };
```

### Langkah 4: Pilih Format Gambar – Simpan CAD sebagai PNG (atau JPEG)

Buat objek opsi khusus format gambar. Ganti `JpegOptions` dengan `PngOptions` ketika Anda ingin **save cad as png**.

```csharp
// Create an instance of JpegOptions (or any ImageOptions for raster formats)
var options = new JpegOptions();
options.VectorRasterizationOptions = rasterizationOptions;
```

> **Tip pro:** Untuk menghasilkan file PNG, cukup buat instance `new PngOptions()` alih-alih `JpegOptions`.

### Langkah 5: Ekspor ke Format JPEG (atau PNG)

Akhirnya, simpan gambar yang telah dirasterisasi ke disk. Ekstensi file menentukan format output.

```csharp
// Export each layer to Jpeg format
MyDir = MyDir + "CADLayersToRasterImageFormats_out.jpg";
image.Save(MyDir, options);
```

Ketika Anda mengganti `JpegOptions` dengan `PngOptions`, kode yang sama akan **convert dxf to png** dan menghasilkan file `.png`.

### Langkah Tambahan: Konversi Semua Lapisan

Jika Anda perlu **convert cad to raster** untuk setiap lapisan dalam gambar, panggil metode pembantu di bawah ini. Metode ini mengiterasi semua lapisan dan menyimpan masing‑masing sebagai gambar terpisah.

```csharp
ConvertAllLayersToRasterImageFormats();
```

> *Catatan:* Implementasi `ConvertAllLayersToRasterImageFormats` merupakan bagian dari suite contoh lengkap Aspose.CAD dan menunjukkan pemrosesan batch lapisan.

## Masalah Umum & Pemecahan Masalah

| Gejala | Penyebab Kemungkinan | Perbaikan |
|---------|--------------|-----|
| Gambar kosong atau putih | Opsi rasterisasi tidak diatur (mis., `PageWidth`/`PageHeight` = 0) | Pastikan `PageWidth` dan `PageHeight` memiliki nilai positif |
| Lapisan hilang | Nama lapisan tidak tepat dalam array `Layers` | Verifikasi nama lapisan yang tepat dalam file CAD (case‑sensitive) |
| PNG kualitas rendah | DPI default rendah | Setel `rasterizationOptions.Resolution = 300;` untuk kualitas lebih tinggi |

## Pertanyaan yang Sering Diajukan (Asli)

### Q1: Bisakah saya menggunakan format gambar lain untuk ekspor?
A1: Yes, you can. Simply replace `JpegOptions` with the desired format's options, such as `PngOptions` or `BmpOptions`.

### Q2: Apakah ada versi percobaan yang tersedia?
A2: Yes, you can explore the functionality of Aspose.CAD by downloading the trial version [here](https://releases.aspose.com/).

### Q3: Bagaimana saya dapat mendapatkan dukungan untuk Aspose.CAD?
A3: Visit the Aspose.CAD [forum](https://forum.aspose.com/c/cad/19) for community support or consider purchasing a license for dedicated support.

### Q4: Apakah lisensi sementara tersedia?
A4: Yes, you can obtain a temporary license [here](https://purchase.aspose.com/temporary-license/).

### Q5: Di mana saya dapat menemukan dokumentasi?
A5: Refer to the detailed documentation [here](https://reference.aspose.com/cad/net/).

## FAQ Tambahan

**Q: Bisakah saya mengekspor semua lapisan dalam satu perintah?**  
A: Ya, gunakan metode `ConvertAllLayersToRasterImageFormats` yang ditunjukkan di atas.

**Q: Apakah Aspose.CAD mendukung format vektor seperti SVG?**  
A: Ini terutama menargetkan format raster, tetapi Anda dapat mengekspor ke PDF yang mempertahankan data vektor.

**Q: Bagaimana saya mengontrol warna latar belakang PNG yang diekspor?**  
A: Setel `rasterizationOptions.BackgroundColor` ke `Color` yang diinginkan sebelum menyimpan.

**Q: Apakah memungkinkan mengekspor satu tata letak saja alih-alih seluruh gambar?**  
A: Ya, konfigurasikan `rasterizationOptions.Layouts` untuk menentukan nama tata letak yang ingin Anda rasterisasi.

## Kesimpulan

Anda kini telah mempelajari cara **convert dxf to png**, **export cad layers**, dan **save cad as png** atau JPEG menggunakan Aspose.CAD untuk .NET. Dengan menyesuaikan `CadRasterizationOptions` dan menukar opsi format gambar, Anda dapat menyesuaikan konversi untuk hampir semua output raster yang Anda perlukan. Jelajahi opsi format lain dalam API Aspose.CAD untuk memperluas alur kerja CAD‑to‑raster Anda.

---

**Terakhir Diperbarui:** 2026-03-21  
**Diuji Dengan:** Aspose.CAD for .NET 24.11 (latest at time of writing)  
**Penulis:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}