---
date: 2026-03-29
description: Pelajari cara mengonversi DGN ke JPEG dengan Aspose.CAD untuk .NET, yang
  menyediakan dukungan penuh untuk DGN V7 dan memungkinkan Anda mengonversi CAD ke
  gambar raster dengan mudah.
linktitle: Support for DGN V7
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Konversi DGN ke JPEG dengan Aspose.CAD untuk .NET – Dukungan V7
url: /id/net/cad-features-and-support/support-for-dgn-v7/
weight: 19
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Mengonversi DGN ke JPEG dengan Aspose.CAD untuk .NET – Dukungan V7

## Pendahuluan

Dalam tutorial ini Anda akan belajar cara **mengonversi DGN ke JPEG** dengan Aspose.CAD untuk .NET, memanfaatkan dukungan penuh DGN V7 pada perpustakaan. Mengonversi file DGN ke gambar raster seperti JPEG adalah kebutuhan umum ketika Anda perlu menyematkan gambar CAD ke halaman web, aplikasi seluler, atau alat pelaporan. Aspose.CAD juga memungkinkan Anda **mengonversi CAD ke raster** secara efisien, memberi fleksibilitas dalam cara Anda menyajikan data desain.

## Jawaban Cepat
- **Apa yang dibahas dalam tutorial ini?** Mengonversi file DGN V7 ke gambar raster JPEG menggunakan Aspose.CAD untuk .NET.  
- **Versi perpustakaan apa yang diperlukan?** Versi terbaru Aspose.CAD untuk .NET yang mencakup dukungan DGN V7.  
- **Apakah saya memerlukan lisensi?** Versi percobaan gratis dapat digunakan untuk pengembangan; lisensi komersial diperlukan untuk produksi.  
- **Bisakah saya mengubah ukuran output?** Ya – opsi rasterisasi memungkinkan Anda mengatur lebar halaman, tinggi, dan skala.  
- **Apakah JPEG satu‑satunya format output?** Tidak – Aspose.CAD mendukung banyak format raster (PNG, BMP, TIFF, dll.).

## Apa itu DGN V7?
DGN (Design) adalah format file yang awalnya dibuat oleh Bentley Systems untuk MicroStation. Versi 7 menambahkan geometri dan metadata yang lebih kaya, menjadikannya pilihan populer untuk proyek teknik sipil dan infrastruktur. Aspose.CAD untuk .NET dapat membaca file DGN V7 secara langsung, mengekspose kontennya sebagai objek `CadImage` yang dapat Anda rasterisasi atau konversi ke format lain.

## Mengapa mengonversi DGN ke JPEG?
- **Siap untuk web:** Gambar JPEG ringan dan langsung ditampilkan di peramban tanpa memerlukan plugin khusus.  
- **Lintas platform:** JPEG dapat dilihat di perangkat apa pun, menjadikannya ideal untuk berbagi gambar CAD dengan pemangku kepentingan non‑teknis.  
- **Alur kerja yang disederhanakan:** Mengonversi ke format raster menghilangkan kebutuhan akan penampil CAD khusus dalam proses hilir.

## Prasyarat

Sebelum kita masuk ke implementasi, pastikan Anda memiliki hal‑hal berikut:

- **Aspose.CAD untuk .NET** – unduh dari [situs web](https://releases.aspose.com/cad/net/).  
- **Lingkungan pengembangan** – Visual Studio (atau IDE apa pun yang mendukung .NET).  

Menyiapkan hal‑hal ini akan memungkinkan Anda mengikuti langkah‑langkah tanpa gangguan.

## Mengimpor Namespace

Mulailah dengan mengimpor namespace yang diperlukan untuk penanganan CadImage dan rasterisasi.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Langkah 1: Memuat File DGN

Muat file DGN sumber ke dalam objek `CadImage`. Ganti jalur placeholder dengan folder yang berisi file DGN Anda.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Subsequent steps will be placed here.
}
```

## Langkah 2: Mengonfigurasi Opsi Rasterisasi

Tentukan bagaimana gambar DGN harus dirasterisasi. Anda dapat mengontrol dimensi output dan perilaku skala.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions
{
    PageWidth = 600,
    PageHeight = 300,
    NoScaling = true,
    AutomaticLayoutsScaling = false
};
```

## Langkah 3: Menetapkan Opsi Rasterisasi Vektor

Buat objek `JpegOptions` (atau opsi format raster lainnya) dan lampirkan pengaturan rasterisasi.

```csharp
ImageOptionsBase options = new JpegOptions
{
    VectorRasterizationOptions = rasterizationOptions
};
```

## Langkah 4: Menyimpan Gambar yang Dirasterisasi

Akhirnya, ekspor gambar DGN ke file JPEG menggunakan metode `Save`.

```csharp
cadImage.Save(MyDir + "ExportDGNToRasterImage_out.jpeg", options);
```

Ketika kode berhasil dijalankan, Anda akan menemukan representasi JPEG dari gambar DGN V7 asli di folder yang ditentukan.

## Masalah Umum dan Solusinya

| Masalah | Solusi |
|-------|----------|
| **File tidak ditemukan** | Verifikasi bahwa `MyDir` diakhiri dengan pemisah jalur (`\\` atau `/`) dan nama file sudah benar. |
| **Gambar output kosong** | Pastikan `NoScaling` diatur dengan tepat; setel ke `false` jika Anda ingin gambar mengisi halaman. |
| **Entitas tidak didukung** | Aspose.CAD mendukung sebagian besar entitas DGN, namun objek yang sangat lama atau khusus mungkin diabaikan. Periksa log konversi untuk peringatan. |

## Pertanyaan yang Sering Diajukan

### Q1: Apakah Aspose.CAD kompatibel dengan spesifikasi DGN V7 terbaru?
**A:** Ya, Aspose.CAD sepenuhnya mendukung DGN V7, menangani baik geometri maupun metadata sesuai standar terbaru.

### Q2: Bisakah saya menyesuaikan opsi rasterisasi untuk konversi file DGN?
**A:** Tentu saja. Kelas `CadRasterizationOptions` memungkinkan Anda menyesuaikan ukuran halaman, skala, ketebalan garis, warna latar belakang, dan lainnya.

### Q3: Apakah ada format output lain selain JPEG yang didukung?
**A:** Ya, Aspose.CAD dapat mengekspor ke PNG, BMP, TIFF, dan beberapa format raster lainnya. Cukup gunakan kelas `*Options` yang sesuai (misalnya, `PngOptions`).

### Q4: Bagaimana cara mendapatkan bantuan terkait pertanyaan Aspose.CAD?
**A:** Kunjungi [forum Aspose.CAD](https://forum.aspose.com/c/cad/19) untuk dukungan komunitas dan respons resmi.

### Q5: Apakah tersedia versi percobaan gratis untuk Aspose.CAD untuk .NET?
**A:** Ya, Anda dapat mengunduh versi percobaan dari [di sini](https://releases.aspose.com/).

---

**Terakhir Diperbarui:** 2026-03-29  
**Diuji Dengan:** Aspose.CAD 24.12 untuk .NET  
**Penulis:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}