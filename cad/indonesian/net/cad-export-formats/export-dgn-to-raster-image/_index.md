---
date: 2026-03-24
description: Pelajari cara mengonversi DGN ke PNG dan menyimpan CAD sebagai JPEG menggunakan
  Aspose.CAD untuk .NET – panduan cepat untuk konversi CAD ke gambar.
linktitle: Export DGN to Raster Image
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Cara Mengonversi DGN ke PNG di Aspose.CAD untuk .NET
url: /id/net/cad-export-formats/export-dgn-to-raster-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Mengonversi DGN ke PNG di Aspose.CAD untuk .NET

Dalam pengembangan .NET modern, **convert dgn to png** adalah kebutuhan umum ketika Anda perlu menampilkan gambar CAD di web atau menyematkannya dalam laporan. Aspose.CAD untuk .NET membuat konversi ini sederhana, memungkinkan Anda mengubah file DGN menjadi gambar raster berkualitas tinggi dengan hanya beberapa baris kode. Dalam panduan ini kami akan membahas seluruh proses, mulai dari menyiapkan proyek hingga menyimpan file PNG (atau JPEG) akhir.

## Jawaban Cepat
- **Bisakah saya mengonversi DGN ke PNG dengan Aspose.CAD?** Ya – cukup konfigurasikan opsi rasterisasi dan pilih output PNG atau JPEG.  
- **Apakah saya memerlukan lisensi untuk penggunaan produksi?** Lisensi Aspose.CAD yang valid diperlukan untuk penyebaran non‑trial.  
- **Versi .NET mana yang didukung?** .NET Framework 4.6+, .NET Core 3.1+, .NET 5/6/7.  
- **Format gambar apa yang tersedia?** PNG, JPEG, BMP, GIF, TIFF, dan lainnya.  
- **Apakah penanganan pengecualian diperlukan?** Tentu – bungkus konversi dalam try/catch untuk menangani masalah akses file.

## Apa itu “convert dgn to png”?
Mengonversi file DGN (MicroStation) ke PNG berarti merasterkan data CAD vektor menjadi gambar berbasis piksel. Ini berguna untuk pembuatan pratinjau, menyematkan gambar dalam email HTML, atau membuat thumbnail untuk sistem manajemen dokumen.

## Mengapa menggunakan Aspose.CAD untuk konversi CAD ke gambar?
- **Tanpa ketergantungan eksternal** – berfungsi sepenuhnya dalam kode yang dikelola.  
- **Fidelity tinggi** – mempertahankan ketebalan garis, lapisan, dan warna.  
- **Output fleksibel** – beralih antara PNG, JPEG, BMP, dll., dengan mengubah satu opsi.  
- **Dioptimalkan untuk kinerja** – rasterisasi cepat bahkan untuk gambar besar.

## Prasyarat

Sebelum memulai, pastikan Anda memiliki:

- **Aspose.CAD untuk .NET** terpasang di proyek Anda. Anda dapat mengunduhnya dari [website](https://reference.aspose.com/cad/net/).  
- File DGN contoh (misalnya `Nikon_D90_Camera.dgn`) yang ditempatkan di direktori yang diketahui.

## Impor Namespace

Mulailah dengan menambahkan pernyataan `using` yang diperlukan sehingga Anda dapat mengakses kelas Aspose.CAD.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Langkah 1: Muat File DGN

Muat DGN sumber ke dalam objek `CadImage`. Objek ini mewakili gambar CAD dalam memori dan akan menjadi sumber untuk rasterisasi.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Your code for further processing goes here
}
```

## Langkah 2: Tentukan Opsi Rasterisasi

Konfigurasikan cara gambar CAD harus dirasterisasi. Anda dapat mengontrol ukuran gambar, skala, dan warna latar belakang di sini.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 600;
rasterizationOptions.PageHeight = 300;
rasterizationOptions.NoScaling = true;
rasterizationOptions.AutomaticLayoutsScaling = false;
```

## Langkah 3: Pilih Format Output (PNG atau JPEG)

Meskipun tutorial ini berfokus pada PNG, Anda mungkin juga ingin **save cad as jpeg**. Buat objek opsi gambar yang sesuai dan lampirkan pengaturan rasterisasi.

```csharp
ImageOptionsBase options = new JpegOptions();   // Change to PngOptions() for PNG output
options.VectorRasterizationOptions = rasterizationOptions;
```

> **Pro tip:** Untuk menghasilkan file PNG, ganti `new JpegOptions()` dengan `new PngOptions()`.

## Langkah 4: Simpan Gambar Raster

Akhirnya, panggil `Save` pada instance `CadImage`, memberikan nama file yang diinginkan dan objek opsi yang telah Anda konfigurasikan.

```csharp
cadImage.Save(MyDir + "ExportDGNToRasterImage_out.jpg", options);
```

Jika Anda beralih ke `PngOptions`, file akan disimpan sebagai `ExportDGNToRasterImage_out.png`.

## Masalah Umum dan Solusinya

| Masalah | Penyebab | Solusi |
|-------|-------|-----|
| **Gambar output kosong** | `NoScaling` diatur tidak benar atau layout tidak dipilih | Setel `AutomaticLayoutsScaling = true` atau tentukan layout yang diinginkan. |
| **Kekurangan memori untuk file besar** | Memuat DGN besar tanpa streaming | Gunakan `Image.Load(sourceFilePath, new LoadOptions { LoadOnDemand = true })`. |
| **Versi DGN tidak didukung** | Versi MicroStation yang lebih lama | Pastikan Anda memiliki versi Aspose.CAD terbaru yang mendukung format lama. |

## Pertanyaan yang Sering Diajukan

**Q: Bisakah saya mengekspor file DGN ke format selain JPEG?**  
A: Ya, Aspose.CAD untuk .NET mendukung PNG, BMP, GIF, TIFF, dan lainnya – cukup ganti kelas opsi (mis., `new PngOptions()`).

**Q: Bagaimana cara menangani pengecualian selama konversi?**  
A: Bungkus kode konversi dalam blok `try/catch` dan log `Aspose.CAD.CadException` untuk informasi kesalahan yang detail.

**Q: Apakah ada versi percobaan yang tersedia untuk Aspose.CAD untuk .NET?**  
A: Ya, Anda dapat menjelajahi produk dengan percobaan gratis. Kunjungi [di sini](https://releases.aspose.com/) untuk informasi lebih lanjut.

**Q: Di mana saya dapat mencari bantuan atau mendiskusikan masalah terkait Aspose.CAD untuk .NET?**  
A: Kunjungi [forum Aspose.CAD](https://forum.aspose.com/c/cad/19) untuk dukungan komunitas dan diskusi.

**Q: Bagaimana cara mendapatkan lisensi sementara untuk Aspose.CAD untuk .NET?**  
A: Kunjungi [tautan ini](https://purchase.aspose.com/temporary-license/) untuk memperoleh lisensi sementara bagi kebutuhan pengembangan Anda.

## Kesimpulan

Anda kini telah mempelajari cara **convert dgn to png** (atau JPEG) menggunakan Aspose.CAD untuk .NET. Dengan menyesuaikan opsi rasterisasi dan menukar kelas opsi gambar, Anda dapat menyesuaikan output agar sesuai dengan kebutuhan proyek apa pun. Jangan ragu untuk bereksperimen dengan ukuran halaman berbeda, pengaturan DPI, dan format file untuk mendapatkan gambar raster yang sempurna bagi aplikasi Anda.

---

**Terakhir Diperbarui:** 2026-03-24  
**Diuji Dengan:** Aspose.CAD 24.11 untuk .NET  
**Penulis:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}