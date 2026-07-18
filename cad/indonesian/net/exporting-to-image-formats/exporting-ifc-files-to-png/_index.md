---
date: 2026-07-18
description: Cara mengekspor CAD ke PNG menggunakan Aspose.CAD untuk .NET. Mengonversi
  file IFC menjadi gambar PNG berkualitas tinggi dengan cepat dan dapat diandalkan.
keywords:
- how to export cad to png
- Aspose.CAD IFC conversion
- CAD to PNG .NET
lastmod: 2026-07-18
linktitle: Mengekspor File IFC ke PNG
og_description: Cara mengekspor CAD ke PNG menggunakan Aspose.CAD untuk .NET. Pelajari
  konversi file IFC ke gambar PNG langkah demi langkah dengan pengaturan tanpa kode.
og_image_alt: Guide showing IFC to PNG conversion with Aspose.CAD for .NET
og_title: Cara Mengekspor CAD ke PNG – Panduan Aspose.CAD .NET
schemas:
- author: Aspose
  dateModified: '2026-07-18'
  description: How to export CAD to PNG using Aspose.CAD for .NET. Convert IFC files
    to high‑quality PNG images quickly and reliably.
  headline: How to Export CAD to PNG – Exporting IFC Files with Aspose.CAD
  type: TechArticle
- questions:
  - answer: No, Aspose.CAD for .NET is specifically designed for Windows environments.
    question: Can I use Aspose.CAD for .NET on macOS or Linux?
  - answer: Yes, you can obtain a temporary license from [here](https://purchase.aspose.com/temporary-license/)
      for evaluation.
    question: Is a temporary license available for testing purposes?
  - answer: Visit the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) for community
      support and discussions.
    question: How can I get support for Aspose.CAD?
  - answer: Refer to the [Aspose.CAD documentation](https://reference.aspose.com/cad/net/)
      for detailed information and examples.
    question: Where can I find comprehensive documentation?
  - answer: Check the documentation or seek assistance on the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19).
    question: What if I encounter issues during installation?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- export cad
- Aspose.CAD
- IFC to PNG
- .NET image conversion
title: Cara Mengekspor CAD ke PNG – Mengekspor File IFC dengan Aspose.CAD
url: /id/net/exporting-to-image-formats/exporting-ifc-files-to-png/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cara Mengekspor CAD ke PNG – Mengekspor File IFC dengan Aspose.CAD

## Pendahuluan

Jika Anda perlu **how to export cad to png**, Aspose.CAD untuk .NET menawarkan cara yang andal dan tanpa kode untuk mengubah model IFC (Industry Foundation Classes) menjadi gambar raster PNG yang tajam. Dalam tutorial ini kami akan membahas seluruh alur kerja—dari menginstal pustaka hingga menyimpan PNG akhir—sehingga Anda dapat mengintegrasikan konversi ini ke dalam aplikasi .NET apa pun dengan percaya diri.

## Jawaban Cepat
- **Library apa yang menangani konversi?** Aspose.CAD for .NET.
- **Format sumber yang didukung?** File IFC (Industry Foundation Classes).
- **Format gambar target?** PNG, dengan kontrol penuh atas ukuran dan resolusi.
- **Versi .NET minimum?** .NET Framework 4.5+ atau .NET Core 3.1+.
- **Persyaratan lisensi?** Lisensi Aspose.CAD yang valid untuk penggunaan produksi.

## Apa itu “how to export cad to png”?

Frasa ini merujuk pada proses mengonversi format file berbasis CAD, seperti IFC, menjadi gambar Portable Network Graphics (PNG) raster. Konversi ini memungkinkan tampilan, berbagi, dan penyematan visual CAD dengan mudah di halaman web, dokumentasi, atau laporan, menyediakan format ringan yang didukung secara luas dan mempertahankan fidelitas visual tanpa memerlukan penampil CAD khusus.

## Mengapa menggunakan Aspose.CAD untuk konversi ini?

Aspose.CAD mendukung **lebih dari 50 format CAD dan BIM** serta dapat memproses model IFC berukuran ratusan halaman tanpa memuat seluruh file ke dalam memori. Ia memberikan konversi yang cepat dan efisien memori pada perangkat keras server standar, secara otomatis menangani lapisan, ketebalan garis, dan pemetaan warna sambil menawarkan opsi konfigurasi yang luas untuk kualitas dan ukuran output.

## Prasyarat

### 1. Instalasi Aspose.CAD
Pastikan Anda telah menginstal Aspose.CAD untuk .NET. Anda dapat mengunduhnya dari halaman rilis [di sini](https://releases.aspose.com/cad/net/).

### 2. Direktori Dokumen
Buat direktori khusus untuk dokumen Anda. Dalam contoh yang diberikan, variabel `MyDir` mewakili direktori dokumen.

## Impor Namespace
Sekarang prasyarat sudah siap, impor namespace yang diperlukan untuk bekerja dengan Aspose.CAD dalam proyek .NET Anda.

```csharp
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using Aspose.CAD.FileFormats.Ifc;
```

## Cara Mengekspor CAD ke PNG?

`IfcImage` mewakili gambar CAD IFC yang dapat dirasterkan ke format raster seperti PNG. Muat file IFC Anda dengan `new IfcImage("source.ifc")`, konfigurasikan rasterisasi melalui `RasterizationOptions`, atur pengaturan khusus PNG dengan `PngOptions`, dan akhirnya panggil `Save(outputPath, pngOptions)`. Alur end‑to‑end ini mengonversi model CAD menjadi PNG resolusi tinggi dalam beberapa baris kode, menangani lapisan, warna, dan ketebalan garis secara otomatis.

## Langkah 1: Muat File IFC
Kelas `IfcImage` memuat model IFC dan menyiapkannya untuk rasterisasi.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "example.ifc";
using (IfcImage cadImage = (IfcImage)Image.Load(sourceFilePath))
{
```

Pada langkah ini kami menginisialisasi objek Aspose.CAD `IfcImage` dan memuat file IFC ke dalamnya.

## Langkah 2: Atur Opsi Rasterisasi
Kelas `RasterizationOptions` mendefinisikan bagaimana data vektor diubah menjadi gambar raster, termasuk lebar halaman, tinggi, dan warna latar belakang.

```csharp
    CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
   
    rasterizationOptions.PageWidth = 100;
    rasterizationOptions.PageHeight = 100;
```

Tentukan opsi rasterisasi untuk mengonfigurasi lebar dan tinggi halaman output PNG.

## Langkah 3: Atur Opsi PNG
Kelas `PngOptions` menyimpan pengaturan khusus untuk output PNG, seperti tingkat kompresi dan kedalaman warna.

```csharp
    PngOptions pngOptions = new PngOptions();
    pngOptions.VectorRasterizationOptions = rasterizationOptions;
```

Buat opsi PNG dan kaitkan dengan opsi rasterisasi yang telah didefinisikan sebelumnya.

## Langkah 4: Tentukan Jalur Output
Jalur output menentukan di mana file PNG yang dihasilkan akan disimpan.

```csharp
    // Set output path as well
    string outPath = sourceFilePath + ".png";
    cadImage.Save(outPath, pngOptions);
}
```

Tentukan jalur output untuk file PNG, pastikan memiliki nama yang sama dengan file sumber dengan ekstensi ".png". Akhirnya, simpan gambar yang telah dikonversi.

## Masalah Umum dan Solusinya
- **Font atau gaya garis yang hilang:** Pastikan IFC sumber merujuk semua sumber daya yang diperlukan; Aspose.CAD menyematkan aset yang hilang bila memungkinkan.
- **File besar menyebabkan lonjakan memori:** Gunakan properti `MemoryLimit` pada `RasterizationOptions` untuk membatasi penggunaan memori.
- **Warna tidak tepat:** Verifikasi bahwa definisi warna IFC sumber mematuhi skema IFC; Aspose.CAD menghormati pemetaan warna standar.

## Pertanyaan yang Sering Diajukan

**Q: Dapatkah saya menggunakan Aspose.CAD untuk .NET di macOS atau Linux?**  
A: Tidak, Aspose.CAD untuk .NET dirancang khusus untuk lingkungan Windows.

**Q: Apakah ada lisensi sementara yang tersedia untuk tujuan pengujian?**  
A: Ya, Anda dapat memperoleh lisensi sementara dari [di sini](https://purchase.aspose.com/temporary-license/) untuk evaluasi.

**Q: Bagaimana cara mendapatkan dukungan untuk Aspose.CAD?**  
A: Kunjungi [forum Aspose.CAD](https://forum.aspose.com/c/cad/19) untuk dukungan komunitas dan diskusi.

**Q: Di mana saya dapat menemukan dokumentasi lengkap?**  
A: Lihat [dokumentasi Aspose.CAD](https://reference.aspose.com/cad/net/) untuk informasi detail dan contoh.

**Q: Bagaimana jika saya mengalami masalah selama instalasi?**  
A: Periksa dokumentasi atau minta bantuan di [forum Aspose.CAD](https://forum.aspose.com/c/cad/19).

---

**Terakhir Diperbarui:** 2026-07-18  
**Diuji Dengan:** Aspose.CAD 24.11 untuk .NET  
**Penulis:** Aspose

## Tutorial Terkait

- [Konversi Gambar CAD ke Gambar Raster di Aspose.CAD untuk .NET](/cad/net/cad-drawing-manipulation/convert-cad-drawing-to-raster-image/)
- [Konversi STL ke PNG dengan Mudah menggunakan Aspose.CAD untuk .NET](/cad/net/stl-file-export/exporting-stl-files-to-png/)
- [Ekspor Layout CAD ke Format Gambar Raster di Aspose.CAD untuk .NET](/cad/net/cad-export-formats/export-cad-layouts-to-raster-image-formats/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}