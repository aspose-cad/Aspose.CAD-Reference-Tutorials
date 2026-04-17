---
date: 2026-03-19
description: Pelajari cara mengonversi CAD ke PNG di .NET menggunakan Aspose.CAD,
  menyimpan CAD sebagai PNG secara efisien, dan menyederhanakan alur kerja gambar
  raster Anda.
linktitle: Convert CAD Drawing to Raster Image
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Konversi CAD ke PNG di Aspose.CAD untuk .NET
url: /id/net/cad-drawing-manipulation/convert-cad-drawing-to-raster-image/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Mengonversi CAD ke PNG di Aspose.CAD untuk .NET

## Pendahuluan

Dalam aplikasi modern yang berfokus pada CAD, **mengonversi CAD ke PNG** adalah kebutuhan umum—baik Anda perlu menghasilkan thumbnail, menyematkan gambar dalam halaman web, atau mengarsipkan desain sebagai gambar raster. Tutorial ini memandu Anda melalui proses lengkap mengonversi gambar CAD (DXF, DWG, dll.) ke file PNG berkualitas tinggi menggunakan pustaka Aspose.CAD untuk .NET. Pada akhir tutorial, Anda akan dapat **menyimpan CAD sebagai PNG** dengan kontrol penuh atas pengaturan rasterisasi, menjadikan alur kerja Anda lebih cepat dan lebih dapat diandalkan.

## Jawaban Cepat
- **Perpustakaan apa yang terbaik untuk konversi CAD‑to‑PNG?** Aspose.CAD untuk .NET.  
- **Format file apa yang dapat diekspor ke PNG?** DWG, DXF, DGN, dan format CAD lain yang didukung.  
- **Apakah saya memerlukan lisensi untuk penggunaan produksi?** Ya, lisensi komersial diperlukan; tersedia versi percobaan gratis.  
- **Bisakah saya menyesuaikan ukuran dan kualitas gambar?** Tentu—opsi rasterisasi memungkinkan Anda mengatur lebar halaman, tinggi, warna latar belakang, dan lainnya.  
- **Apakah kode kompatibel dengan .NET Core / .NET 6?** Ya, API yang sama berfungsi di .NET Framework, .NET Core, dan .NET 5/6.

## Apa itu “convert CAD to PNG”?
Mengonversi CAD ke PNG berarti merasterkan gambar CAD berbasis vektor menjadi format gambar berbasis piksel (PNG). Proses ini mempertahankan fidelitas visual sambil membuat file mudah ditampilkan di peramban, aplikasi seluler, atau lingkungan apa pun yang tidak mendukung format CAD secara native.

## Mengapa menggunakan Aspose.CAD untuk mengonversi CAD ke PNG?
- **Tanpa ketergantungan eksternal** – murni .NET, tidak memerlukan mesin CAD native.  
- **Dukungan format lengkap** – menangani DWG, DXF, DGN, dan lainnya.  
- **Kontrol rasterisasi yang detail** – ukuran halaman, resolusi, latar belakang, ketebalan garis, dll.  
- **Kinerja tinggi** – dioptimalkan untuk pemrosesan batch sisi server.

## Prasyarat

Sebelum memulai, pastikan Anda memiliki:

1. **Aspose.CAD untuk .NET** – unduh dari [halaman unduhan](https://releases.aspose.com/cad/net/).  
2. IDE yang kompatibel dengan .NET (Visual Studio, Rider, atau VS Code) dengan proyek yang menargetkan .NET Framework 4.6+ atau .NET Core 3.1+.  

## Mengimpor Namespace

Di proyek .NET Anda, impor namespace yang diperlukan untuk mengakses fungsionalitas Aspose.CAD. Tambahkan berikut ini di awal file kode Anda:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Panduan Langkah‑demi‑Langkah

### Langkah 1: Tentukan Jalur File
Tetapkan file CAD sumber dan jalur PNG tujuan. Ganti placeholder dengan direktori aktual di mesin Anda.

```csharp
// The path to the documents directory.
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";
```

### Langkah 2: Muat Gambar CAD
Buka file CAD menggunakan `Aspose.CAD.Image.Load`. Ini membuat representasi dalam memori dari gambar yang dapat Anda rasterkan.

```csharp
using (Aspose.CAD.Image image = Aspose.CAD.Image.Load(sourceFilePath))
{
```

### Langkah 3: Konfigurasikan Opsi Rasterisasi  
Tentukan bagaimana data vektor harus diubah menjadi piksel. Di sini kami mengatur kanvas 1200 × 1200 piksel, tetapi Anda dapat menyesuaikan `PageWidth` dan `PageHeight` sesuai kebutuhan (misalnya, untuk **convert dwg to png** pada DPI tertentu).

```csharp
// Create an instance of CadRasterizationOptions
Aspose.CAD.ImageOptions.CadRasterizationOptions rasterizationOptions = new Aspose.CAD.ImageOptions.CadRasterizationOptions();
// Set page width & height
rasterizationOptions.PageWidth = 1200;
rasterizationOptions.PageHeight = 1200;
```

> **Pro tip:** Untuk meningkatkan kecepatan render pada gambar besar, Anda juga dapat mengatur `rasterizationOptions.BackgroundColor` ke warna solid atau mengaktifkan `rasterizationOptions.DrawType` untuk konversi vektor yang lebih cepat.

### Langkah 4: Buat Opsi PNG untuk Gambar Hasil  
Bungkus pengaturan rasterisasi di dalam objek `PngOptions`, yang memberi tahu Aspose.CAD untuk menghasilkan file PNG.

```csharp
// Create an instance of PngOptions for the resultant image
ImageOptionsBase options = new Aspose.CAD.ImageOptions.PngOptions();
// Set rasterization options
options.VectorRasterizationOptions = rasterizationOptions;
```

### Langkah 5: Simpan PNG Hasil  
Gabungkan jalur direktori dengan nama file yang diinginkan dan tulis gambar yang telah dirasterkan ke disk. Langkah ini **menyimpan CAD sebagai PNG**.

```csharp
MyDir = MyDir + "conic_pyramid_raster_image_out.png";
// Save resultant image
image.Save(MyDir, options);
```

### Langkah 6: Tampilkan Pesan Sukses  
Konfirmasi bahwa konversi berhasil dan tunjukkan lokasi file yang disimpan.

```csharp
//ExEnd:ConvertDrawingToRasterImage            
Console.WriteLine("\nCAD drawing converted successfully to raster image format.\nFile saved at " + MyDir);
```

> **Catatan:** Blok `using` dari Langkah 2 secara otomatis membuang objek `Image`, memastikan semua sumber daya dilepaskan.

## Masalah Umum dan Solusinya

| Masalah | Penyebab | Solusi |
|-------|-------|-----|
| **Output PNG kosong** | Opsi rasterisasi tidak diatur (misalnya, `PageWidth`/`PageHeight` tidak ada). | Pastikan `CadRasterizationOptions` mendefinisikan ukuran kanvas yang tidak nol. |
| **Warna tidak tepat** | Warna latar belakang default putih; gambar sumber menggunakan lapisan transparan. | Setel `rasterizationOptions.BackgroundColor = Color.Transparent;` |
| **Keterlambatan kinerja pada file DWG besar** | Resolusi tinggi tanpa pembagian ubin. | Gunakan `rasterizationOptions.LayoutOptions` untuk membatasi area render atau turunkan DPI. |
| **Pengecualian lisensi** | Menjalankan tanpa lisensi yang valid di produksi. | Terapkan lisensi melalui `License license = new License(); license.SetLicense("Aspose.CAD.lic");` sebelum memuat gambar. |

## Pertanyaan yang Sering Diajukan

### Q1: Apakah Aspose.CAD kompatibel dengan semua format file CAD?
A1: Aspose.CAD mendukung berbagai format file CAD, termasuk DWG, DXF, DGN, dan lainnya. Lihat [dokumentasi](https://reference.aspose.com/cad/net/) untuk daftar lengkap.

### Q2: Bisakah saya menyesuaikan opsi rasterisasi untuk proyek yang berbeda?
A2: Ya, Aspose.CAD memungkinkan kustomisasi luas opsi rasterisasi, memungkinkan pengembang menyesuaikan output berdasarkan kebutuhan proyek.

### Q3: Apakah tersedia percobaan gratis untuk Aspose.CAD?
A3: Ya, Anda dapat menjelajahi fitur Aspose.CAD dengan percobaan gratis. Kunjungi [di sini](https://releases.aspose.com/) untuk memulai.

### Q4: Bagaimana cara mendapatkan dukungan untuk Aspose.CAD?
A4: Untuk bantuan atau pertanyaan, kunjungi [forum dukungan](https://forum.aspose.com/c/cad/19) Aspose.CAD.

### Q5: Apakah lisensi sementara tersedia untuk Aspose.CAD?
A5: Ya, pengembang dapat memperoleh lisensi sementara untuk Aspose.CAD dari [tautan ini](https://purchase.aspose.com/temporary-license/).

### Q6: Bisakah saya menggunakan metode ini untuk **convert DWG to PNG** juga?
A6: Tentu saja. Kode yang sama bekerja untuk file DWG; cukup ubah ekstensi file sumber menjadi `.dwg`.

### Q7: Bagaimana cara **export DXF to image** dengan latar belakang transparan?
A7: Setel `rasterizationOptions.BackgroundColor = Color.Transparent;` sebelum menyimpan PNG.

**Terakhir Diperbarui:** 2026-03-19  
**Diuji Dengan:** Aspose.CAD 24.11 untuk .NET (rilis terbaru)  
**Penulis:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}