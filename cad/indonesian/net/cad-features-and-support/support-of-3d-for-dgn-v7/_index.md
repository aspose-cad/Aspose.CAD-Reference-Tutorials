---
date: 2026-03-29
description: Pelajari cara mengonfigurasi opsi rasterisasi CAD dan mengekspor DGN
  ke PDF dengan dukungan 3D menggunakan Aspose.CAD untuk .NET.
linktitle: Support of 3D for DGN V7
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Konfigurasikan Opsi Rasterisasi CAD untuk DGN V7 3D
url: /id/net/cad-features-and-support/support-of-3d-for-dgn-v7/
weight: 20
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Konfigurasikan Opsi Rasterisasi CAD untuk DGN V7 3D

## Pendahuluan

Dalam tutorial komprehensif ini Anda akan belajar **cara mengkonfigurasi opsi rasterisasi CAD** untuk mengekspor file DGN V7 3‑D ke PDF menggunakan Aspose.CAD untuk .NET. Baik Anda sedang membangun penampil CAD, alat pelaporan, atau pipeline konversi otomatis, menguasai pengaturan ini memberi Anda kontrol tepat atas ukuran halaman, skala tata letak, warna latar belakang, dan tampilan spesifik yang ingin Anda render. Mari kita jalani prosesnya langkah demi langkah.

## Jawaban Cepat
- **Apa arti “configure CAD rasterization options”?**  
  Ini merujuk pada pengaturan properti seperti dimensi halaman, skala, warna latar belakang, dan pemilihan tata letak sebelum mengonversi file CAD ke format raster (mis., PDF).
- **Bagaimana cara mengekspor DGN ke PDF dengan dukungan 3‑D?**  
  Muat DGN dengan `DgnImage`, definisikan `PdfOptions` + `CadRasterizationOptions`, lalu panggil `Save`.
- **Apakah saya memerlukan lisensi untuk penggunaan produksi?**  
  Ya – lisensi komersial diperlukan untuk penerapan; versi percobaan gratis tersedia.
- **Versi .NET mana yang didukung?**  
  .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.
- **Bisakah saya memilih tampilan tertentu untuk diekspor?**  
  Tentu – atur array `Layouts` dalam opsi rasterisasi.

## Apa itu “configure CAD rasterization options”?

Mengkonfigurasi opsi rasterisasi CAD berarti menyesuaikan cara gambar CAD diubah menjadi raster (dikonversi dari vektor ke bitmap atau PDF). Dengan menyesuaikan pengaturan ini Anda mengontrol output visual, kinerja, dan ukuran file dokumen yang dihasilkan.

## Mengapa menggunakan Aspose.CAD untuk ekspor DGN V7 3‑D?

- **Integrasi .NET penuh** – tidak memerlukan COM atau DLL native.  
- **Mendukung geometri 3‑D** – mempertahankan informasi kedalaman saat merender ke PDF.  
- **Kontrol detail** – pilih tata letak, skala, dan warna latar belakang yang tepat.  
- **Lintas platform** – berfungsi di Windows, Linux, dan macOS dengan .NET Core.

## Prasyarat

Sebelum memulai, pastikan Anda memiliki:

- **Aspose.CAD untuk .NET** – unduh dari [here](https://releases.aspose.com/cad/net/).  
- **Visual Studio** atau IDE .NET kompatibel lainnya.  
- **File DGN contoh** – untuk panduan ini kami akan menggunakan `Nikon_D90_Camera.dgn` (termasuk dalam paket contoh Aspose).  

Sekarang semua siap, mari kita selami kode.

## Impor Namespace

Dalam proyek .NET Anda, impor namespace yang diperlukan:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Dgn;
using Aspose.CAD.ImageOptions;
```

## Langkah 1: Siapkan Direktori Dokumen Anda

Buat variabel yang menunjuk ke folder tempat DGN sumber dan file output Anda berada.

```csharp
string MyDir = "Your Document Directory";
```

## Langkah 2: Muat File DGN

Muat file DGN sebagai `DgnImage`. Objek ini memberi Anda akses ke data CAD dan pipeline rasterisasi.

```csharp
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";
string outFile = MyDir + "Nikon_D90_Camera.dgn";

using (DgnImage dgnImage = (DgnImage)Image.Load(sourceFilePath))
{
    // Your code for further processing goes here
}
```

## Langkah 3: Konfigurasikan Opsi Ekspor PDF (Configure CAD Rasterization Options)

Di sini kami **mengkonfigurasi opsi rasterisasi CAD** yang menentukan bagaimana model 3‑D dirender ke PDF. Anda dapat menyesuaikan ukuran halaman, mengaktifkan skala tata letak otomatis, mengatur warna latar belakang, dan memilih tata letak (tampilan) tepat yang ingin diekspor.

```csharp
var options = new PdfOptions
{
    VectorRasterizationOptions = new CadRasterizationOptions
    {
        PageWidth = 1500,
        PageHeight = 1500,
        AutomaticLayoutsScaling = true,
        BackgroundColor = Color.Black,
        Layouts = new string[] { "1", "2", "3", "9" } // Only export specified views
    }
};
```

## Langkah 4: Simpan Gambar Raster

Akhirnya, ekspor DGN ke file PDF menggunakan opsi yang baru saja Anda konfigurasikan.

```csharp
dgnImage.Save(outFile, options);
```

## Masalah Umum dan Solusinya

| Masalah | Solusi |
|-------|----------|
| **Output PDF kosong** | Pastikan array `Layouts` berisi pengidentifikasi tampilan yang benar yang ada di file DGN. |
| **Warna tidak tepat** | Pastikan `BackgroundColor` diatur ke nilai yang diinginkan; gunakan `Color.White` untuk latar belakang terang. |
| **Bottleneck kinerja pada file besar** | Aktifkan `AutomaticLayoutsScaling` dan pertimbangkan mengurangi `PageWidth/PageHeight` untuk resolusi raster yang lebih kecil. |
| **Pengecualian lisensi** | Pasang lisensi Aspose.CAD yang valid sebelum memuat gambar untuk menghindari watermark percobaan. |

## Pertanyaan yang Sering Diajukan

**Q: Bisakah saya menggunakan Aspose.CAD untuk .NET dengan format file CAD lainnya?**  
A: Ya, Aspose.CAD mendukung DWG, DXF, DWF, DGN, dan banyak format lainnya.

**Q: Bagaimana saya dapat menangani pengecualian saat bekerja dengan Aspose.CAD?**  
A: Bungkus kode Anda dalam blok `try‑catch` dan periksa `Aspose.CAD.CADException` untuk informasi detail tentang kesalahan.

**Q: Apakah Aspose.CAD cocok untuk proyek komersial?**  
A: Tentu. Anda dapat membeli lisensi [here](https://purchase.aspose.com/buy).

**Q: Bisakah saya mencoba Aspose.CAD untuk .NET sebelum membeli?**  
A: Ya, versi percobaan gratis tersedia [here](https://releases.aspose.com/).

**Q: Di mana saya dapat menemukan dukungan komunitas untuk Aspose.CAD?**  
A: Bergabunglah dengan forum diskusi [here](https://forum.aspose.com/c/cad/19).

---

**Terakhir Diperbarui:** 2026-03-29  
**Diuji Dengan:** Aspose.CAD 24.11 for .NET  
**Penulis:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}