---
date: 2026-03-26
description: Pelajari cara membuat PDF dari CAD dan mengonversi DXF ke PDF menggunakan
  Aspose.CAD untuk .NET. Sesuaikan opsi pena untuk visual yang menakjubkan dalam PDF,
  PNG, BMP, dan lainnya.
linktitle: Pen Support in Export
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Buat PDF dari CAD dengan Opsi Pena Kustom – Aspose.CAD untuk .NET
url: /id/net/cad-features-and-support/pen-support-in-export/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Tingkatkan Ekspor CAD dengan Opsi Pena Kustom di Aspose.CAD untuk .NET

## Pendahuluan

Jika Anda perlu **membuat PDF dari CAD** dengan cepat dan kontrol visual penuh, Aspose.CAD untuk .NET memberikan hal itu. Dengan memanfaatkan fitur dukungan pena perpustakaan, Anda dapat menentukan cap awal dan akhir, sambungan garis, serta atribut gambar lainnya, menghasilkan PDF yang terlihat persis seperti yang Anda inginkan. Tutorial ini memandu Anda melalui seluruh proses—dari memuat file DXF hingga mengekspor PDF yang selesai—serta menunjukkan bagaimana pengaturan yang sama dapat digunakan kembali saat Anda **mengekspor CAD ke PNG** atau **merasterisasi data gambar CAD** untuk format lain.

## Jawaban Cepat
- **Apa arti “membuat PDF dari CAD”?** Itu mengonversi gambar CAD berbasis vektor (misalnya DXF) menjadi dokumen PDF sambil mempertahankan geometri dan gaya.  
- **Format apa yang mendukung opsi pena?** PDF, PNG, BMP, GIF, JPEG2000, JPEG, PSD, TIFF, dan WMF.  
- **Apakah saya memerlukan lisensi untuk pengembangan?** Versi percobaan gratis cukup untuk pengujian; lisensi komersial diperlukan untuk produksi.  
- **Bisakah saya mengubah cap garis untuk format lain?** Ya—opsi pena berlaku untuk target rasterisasi apa pun yang didukung Aspose.CAD.  
- **Versi .NET apa yang didukung?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.

## Apa itu dukungan pena dalam ekspor CAD?

Dukungan pena memungkinkan Anda menyesuaikan cara garis digambar ketika gambar CAD dirasterisasi atau vektor‑rasterisasi. Anda dapat mengatur properti seperti `StartCap`, `EndCap`, `LineJoin`, dan `DashStyle`. Pengaturan ini memengaruhi tampilan akhir gambar atau PDF yang diekspor, memberi Anda kontrol halus atas kualitas visual.

## Mengapa menggunakan opsi pena kustom saat **membuat PDF dari CAD**?

- **Branding konsisten** – cocokkan gaya garis perusahaan di semua dokumen.  
- **Keterbacaan yang lebih baik** – cap dan sambungan yang lebih tebal membuat gambar teknik lebih jelas di layar dan cetakan.  
- **Fleksibilitas lintas‑format** – konfigurasi pena yang sama bekerja untuk PNG, BMP, dan format raster lainnya, menghemat waktu Anda.

## Prasyarat

- Aspose.CAD untuk .NET terpasang (unduh dari [halaman rilis](https://releases.aspose.com/cad/net/)).  
- Pengetahuan dasar tentang DXF (Drawing Exchange Format).  
- Familiaritas dengan pemrograman C#.

## Impor Namespace

Untuk memulai, pastikan Anda mengimpor namespace yang diperlukan dalam proyek C# Anda:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Drawing;
using System.Drawing.Drawing2D;
```

## Langkah 1: Siapkan Direktori Dokumen Anda

Tentukan folder yang berisi file CAD sumber:

```csharp
string MyDir = "Your Document Directory";
```

## Langkah 2: Muat Gambar CAD

Muat gambar CAD (misalnya file DXF) ke dalam objek `Aspose.CAD.Image`:

```csharp
string sourceFilePath = MyDir + "conic_pyramid.dxf";
CadImage cadImage = (CadImage)Image.Load(sourceFilePath);
```

## Langkah 3: Konfigurasikan Opsi Rasterisasi

Buat objek opsi rasterisasi dan PDF. Objek-objek ini memungkinkan Anda mengontrol bagaimana data CAD diubah menjadi gambar raster atau halaman PDF:

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
PdfOptions pdfOptions = new PdfOptions();
```

## Langkah 4: Kustomisasi Opsi Pena

Di sinilah Anda **menyesuaikan pena** yang menggambar garis. Anda dapat mengatur cap awal dan akhir menjadi `Flat`, `Round`, `Square`, dll. Ini adalah inti dari “cara mengekspor CAD” dengan gaya visual yang Anda butuhkan:

```csharp
rasterizationOptions.PenOptions = new PenOptions
{
   StartCap = LineCap.Flat,
   EndCap = LineCap.Flat
};
```

*Tip profesional:* Bereksperimenlah dengan `LineCap.Round` untuk ujung garis yang lebih halus saat Anda **mengekspor CAD ke PNG**.

## Langkah 5: Terapkan Opsi Rasterisasi Vektor

Lampirkan pengaturan rasterisasi ke opsi PDF sehingga proses ekspor mengetahui konfigurasi pena mana yang akan digunakan:

```csharp
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Langkah 6: Simpan PDF yang Diekspor

Akhirnya, hasilkan file PDF. Langkah ini **membuat PDF dari CAD** dengan opsi pena kustom yang diterapkan:

```csharp
cadImage.Save(MyDir + "9LHATT-A56_generated.pdf", pdfOptions);
```

Anda dapat mengganti `PdfOptions` dengan `PngOptions`, `BmpOptions`, dll., untuk **mengekspor CAD ke PNG** atau format raster lainnya sambil mempertahankan konfigurasi pena yang sama.

## Kasus Penggunaan Umum

- **Dokumentasi teknis** – sematkan gaya garis yang tepat dalam PDF teknik.  
- **Pembuatan laporan otomatis** – proses batch banyak file DXF menjadi PDF dengan satu profil pena.  
- **Layanan web** – sediakan API yang mengonversi file DXF yang diunggah menjadi PDF secara langsung, memastikan gaya yang konsisten.

## Pemecahan Masalah & Jebakan Umum

| Masalah | Penyebab | Solusi |
|-------|--------|----------|
| Garis yang diekspor tampak lebih tebal dari yang diharapkan | DPI lebih tinggi dari yang dimaksud | Atur `rasterizationOptions.PageWidth` / `PageHeight` atau sesuaikan `Resolution`. |
| Opsi pena diabaikan untuk output PNG | Menggunakan `ImageOptions` alih‑alih `VectorRasterizationOptions` | Pastikan Anda menetapkan `rasterizationOptions.PenOptions` sebelum menyimpan. |
| File PDF kosong | Jalur DXF sumber salah atau file rusak | Verifikasi `sourceFilePath` dan pastikan DXF dimuat tanpa pengecualian. |

## FAQ

### Q1: Bisakah saya menggunakan opsi pena ini untuk format gambar lain selain PDF?

A1: Ya, opsi pena dapat diterapkan ke berbagai format gambar seperti PNG, BMP, GIF, JPEG, dan lainnya.

### Q2: Di mana saya dapat menemukan dokumentasi tambahan untuk Aspose.CAD untuk .NET?

A2: Lihat [dokumentasi](https://reference.aspose.com/cad/net/) untuk informasi lengkap dan contoh.

### Q3: Apakah ada versi percobaan gratis untuk Aspose.CAD untuk .NET?

A3: Ya, Anda dapat mengakses percobaan gratis [di sini](https://releases.aspose.com/).

### Q4: Bagaimana cara mendapatkan lisensi sementara untuk Aspose.CAD untuk .NET?

A4: Kunjungi [halaman lisensi sementara](https://purchase.aspose.com/temporary-license/) untuk opsi lisensi sementara.

### Q5: Di mana saya dapat mencari dukungan komunitas untuk Aspose.CAD untuk .NET?

A5: Bergabunglah dengan komunitas di [forum Aspose.CAD](https://forum.aspose.com/c/cad/19).

## Pertanyaan Umum Tambahan

**T: Bagaimana cara **mengonversi DXF ke PDF** secara programatis?**  
J: Muat DXF dengan `Image.Load`, konfigurasikan `CadRasterizationOptions` dan `PdfOptions`, lalu panggil `Save` seperti pada langkah‑langkah di atas.

**T: Bisakah saya merasterisasi gambar CAD tanpa membuat PDF?**  
J: Ya—gunakan `PngOptions`, `BmpOptions`, atau kelas format raster lainnya dan tetapkan `rasterizationOptions` yang sama untuk rasterisasi berkualitas tinggi.

**T: Apakah memungkinkan mengubah lebar garis saat membuat PDF dari CAD?**  
J: Sesuaikan `rasterizationOptions.CustomLineWidth` atau ubah properti `PenOptions.Width` sebelum menyimpan.

**T: Apakah perpustakaan ini mendukung file DXF 3D?**  
J: Aspose.CAD berfokus pada data vektor 2D; entitas 3D diabaikan selama rasterisasi.

**T: Versi Aspose.CAD berapa yang diperlukan untuk fitur ini?**  
J: Dukungan pena tersedia sejak versi 20.9; versi yang lebih baru akan berfungsi.

---

**Terakhir Diperbarui:** 2026-03-26  
**Diuji Dengan:** Aspose.CAD untuk .NET 24.12  
**Penulis:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}