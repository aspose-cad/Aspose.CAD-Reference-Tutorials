---
date: 2026-04-03
description: Pelajari cara merender file CAD dan mengonversi DWG ke PNG menggunakan
  Aspose.CAD untuk .NET. Panduan langkah demi langkah untuk menyimpan CAD sebagai
  gambar.
keywords:
- how to render cad
- convert dwg to png
- export cad to png
- save cad as image
- load dwg in .net
linktitle: Rendering Warna dalam File CAD
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Cara Merender File CAD dengan Warna – Panduan Aspose.CAD
url: /id/net/conversion-and-export/rendering-colors-in-cad-files/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cara Merender File CAD dengan Warna – Panduan Aspose.CAD

## Pendahuluan

Apakah Anda berjuang dengan **cara merender CAD** file dengan warna-warna cerah menggunakan .NET? Dalam panduan komprehensif langkah‑demi‑langkah ini kami akan menunjukkan secara tepat cara merender warna dalam file CAD, mengonversi DWG ke PNG, dan menyimpan gambar CAD Anda sebagai gambar berkualitas tinggi dengan perpustakaan Aspose.CAD.

## Jawaban Cepat
- **Perpustakaan apa yang terbaik untuk merender warna CAD?** Aspose.CAD untuk .NET  
- **Bisakah saya mengonversi DWG ke PNG dalam satu langkah?** Ya – rasterkan DWG dan simpan sebagai PNG.  
- **Apakah saya memerlukan lisensi untuk penggunaan produksi?** Lisensi sementara berfungsi untuk pengujian; lisensi penuh diperlukan untuk produksi.  
- **Versi .NET mana yang didukung?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.  
- **Apakah prosesnya cukup cepat untuk konversi batch?** Rendering dilakukan di memori dan cocok untuk operasi massal.

## Apa itu Merender Warna dalam File CAD?
Merender warna berarti mengambil informasi vektor yang disimpan dalam gambar CAD (DWG, DXF, dll.) dan merasterkannya menjadi gambar bitmap sambil mempertahankan warna objek asli. Ini penting ketika Anda perlu berbagi visual CAD dengan pemangku kepentingan yang tidak memiliki perangkat lunak CAD.

## Mengapa Menggunakan Aspose.CAD untuk Mengonversi DWG ke PNG?
- **Tidak ada ketergantungan eksternal** – berfungsi sepenuhnya offline.  
- **Fidelity penuh** – warna objek, ketebalan garis, dan lapisan dipertahankan.  
- **API sederhana** – kode satu baris untuk memuat, mengonfigurasi, dan menyimpan.  
- **Lintas‑platform** – berfungsi di runtime .NET Windows, Linux, dan macOS.

## Prasyarat

- Perpustakaan Aspose.CAD: Unduh dan instal perpustakaan Aspose.CAD dari [sini](https://releases.aspose.com/cad/net/).  
- Lingkungan Pengembangan: Pastikan Anda memiliki lingkungan pengembangan .NET yang sudah disiapkan.  
- File CAD: Siapkan file CAD contoh untuk pengujian. Anda dapat menggunakan “test1.dwg” untuk tutorial ini.

## Impor Namespace

Dalam proyek .NET Anda, impor namespace yang diperlukan untuk mengakses fungsionalitas Aspose.CAD. Tambahkan baris berikut di awal kode Anda:

```csharp
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
```

## Langkah 1: Siapkan Proyek Anda

Buat proyek .NET baru dan atur direktori yang diperlukan. Pastikan perpustakaan Aspose.CAD direferensikan dalam proyek Anda.

## Langkah 2: Tentukan Jalur File

Tentukan jalur untuk file CAD masukan Anda dan file PNG keluaran. Perbarui baris berikut dalam kode Anda:

```csharp
string MyDir = "Your Document Directory";
string inputFile = MyDir + "test1.dwg";
string outputFile = MyDir + "test1.png";
```

## Langkah 3: Muat File CAD

Gunakan kode berikut untuk membuka dan memuat file CAD:

```csharp
using (FileStream fs = new FileStream(inputFile, FileMode.Open))
{
    using (FileStream output = new FileStream(outputFile, FileMode.Create))
    {
        Image document = Image.Load(fs);
```

## Langkah 4: Konfigurasikan Opsi Rasterisasi

Konfigurasikan opsi rasterisasi untuk menyesuaikan proses rendering. Perbarui baris berikut:

```csharp
PngOptions saveOptions = new PngOptions();

CadRasterizationOptions options = new CadRasterizationOptions();
options.NoScaling = false;
options.PageHeight = document.Height * 10;
options.PageWidth = document.Width * 10;
options.DrawType = Aspose.CAD.FileFormats.Cad.CadDrawTypeMode.UseObjectColor;
saveOptions.VectorRasterizationOptions = options;
```

## Langkah 5: Simpan Gambar yang Dirender

Simpan gambar yang dirender menggunakan opsi yang ditentukan:

```csharp
document.Save(output, saveOptions);
```

## Mengapa Ini Penting

Menyimpan CAD sebagai gambar (PNG, JPEG, dll.) adalah kebutuhan umum ketika Anda perlu menyisipkan gambar dalam laporan, halaman web, atau lampiran email. Dengan menguasai **cara merender CAD**, Anda menghilangkan kebutuhan akan penampil pihak ketiga dan memastikan output visual yang konsisten di semua platform.

## Masalah Umum dan Solusinya

| Masalah | Penyebab | Solusi |
|-------|-------|----------|
| Gambar kosong keluar | `NoScaling` diatur ke `true` dengan dimensi nol | Pastikan `PageHeight` dan `PageWidth` dihitung dari gambar yang dimuat (seperti yang ditunjukkan). |
| Warna muncul salah | `DrawType` salah | Gunakan `CadDrawTypeMode.UseObjectColor` untuk mempertahankan warna objek asli. |
| File tidak ditemukan | Jalur `MyDir` tidak tepat | Verifikasi jalur direktori berakhir dengan slash atau gunakan `Path.Combine`. |
| Kehabisan memori pada file besar | Rendering pada DPI sangat tinggi | Kurangi faktor skala (mis., `*5` alih-alih `*10`). |

## Kesimpulan

Selamat! Anda telah berhasil mempelajari **cara merender CAD** file, mengonversi DWG ke PNG, dan **menyimpan CAD sebagai gambar** menggunakan Aspose.CAD untuk .NET. Pengetahuan ini memungkinkan Anda mengintegrasikan rendering CAD langsung ke dalam aplikasi Anda, mengotomatiskan pembuatan laporan, pratinjau web, dan lainnya.

## FAQ

### Q1: Bisakah saya menggunakan Aspose.CAD secara gratis?

A1: Aspose.CAD menawarkan versi percobaan gratis yang tersedia [di sini](https://releases.aspose.com/). Anda dapat menjelajahi fiturnya sebelum melakukan pembelian.

### Q2: Di mana saya dapat menemukan dokumentasi terperinci untuk Aspose.CAD?

A2: Referensi dokumentasi [di sini](https://reference.aspose.com/cad/net/) untuk informasi mendalam tentang fungsionalitas Aspose.CAD.

### Q3: Bagaimana cara mendapatkan lisensi sementara untuk Aspose.CAD?

A3: Dapatkan lisensi sementara [di sini](https://purchase.aspose.com/temporary-license/) untuk keperluan pengujian.

### Q4: Butuh bantuan atau memiliki pertanyaan?

A4: Kunjungi komunitas Aspose.CAD [forum](https://forum.aspose.com/c/cad/19) untuk dukungan dan diskusi.

### Q5: Di mana saya dapat membeli perpustakaan Aspose.CAD?

A5: Beli Aspose.CAD [di sini](https://purchase.aspose.com/buy) untuk membuka potensi penuhnya.

## Pertanyaan Umum Tambahan

**Q: Bagaimana saya dapat **mengonversi DWG ke PNG** tanpa kehilangan ketebalan garis?**  
A: Pertahankan skala default `PageHeight` dan `PageWidth` (mis., kalikan dengan 10) dan atur `options.DrawType` ke `UseObjectColor`. Ini mempertahankan ketebalan garis dan warna.

**Q: Apakah memungkinkan untuk **mengekspor CAD ke PNG** dalam layanan latar belakang?**  
A: Ya. API Aspose.CAD aman untuk thread pada operasi hanya-baca, sehingga Anda dapat memuat dan merasterkan file di dalam pekerja latar belakang.

**Q: Bisakah saya **memuat DWG di .NET** dari array byte alih-alih file?**  
A: Tentu saja. Gunakan `Image.Load(byteArray)` alih-alih `FileStream` dan ikuti langkah rasterisasi yang sama.

**Q: Format apa yang harus saya pilih untuk kualitas terbaik saat **menyimpan CAD sebagai gambar**?**  
A: PNG menyediakan kompresi lossless dan mempertahankan fidelitas warna, menjadikannya ideal untuk gambar teknik.

**Q: Apakah Aspose.CAD mendukung format raster lain seperti JPEG atau BMP?**  
A: Ya – cukup ganti `PngOptions` dengan `JpegOptions` atau `BmpOptions` dan sesuaikan pengaturan khusus format apa pun.

---

**Last Updated:** 2026-04-03  
**Tested With:** Aspose.CAD 24.11 for .NET  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}