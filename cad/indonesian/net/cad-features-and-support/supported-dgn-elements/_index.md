---
date: 2026-03-29
description: Pelajari cara mengonversi DGN ke PNG menggunakan Aspose.CAD untuk .NET.
  Panduan ini juga mencakup dukungan format file CAD dan seluruh set elemen DGN yang
  didukung.
linktitle: Supported DGN Elements
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Konversi DGN ke PNG dengan Aspose.CAD untuk .NET
url: /id/net/cad-features-and-support/supported-dgn-elements/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Mengonversi DGN ke PNG dengan Aspose.CAD untuk .NET

## Pendahuluan

Apakah Anda seorang pengembang .NET yang ingin **mengonversi DGN ke PNG** dengan mudah? Aspose.CAD untuk .NET menyediakan solusi kuat untuk menangani file DGN secara efisien. Dalam tutorial ini, kami akan membahas elemen DGN yang didukung, membimbing Anda melalui proses bekerja dengan Aspose.CAD untuk .NET sambil menunjukkan secara tepat cara mengekspor elemen tersebut ke gambar PNG.

## Jawaban Cepat
- **Apa yang dilakukan Aspose.CAD?** Ia membaca, memodifikasi, dan mengonversi file CAD/BIM (termasuk DGN) ke format raster seperti PNG.  
- **Apakah saya dapat mengonversi elemen DGN 2D dan 3D?** Ya – baik entitas 2‑D maupun 3‑D didukung.  
- **Versi .NET mana yang diperlukan?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **Apakah saya memerlukan lisensi untuk pengujian?** Versi percobaan gratis tersedia; lisensi diperlukan untuk produksi.  
- **Di mana saya dapat memperoleh perpustakaan?** Unduh dari situs resmi Aspose (tautan di bawah).

## Apa itu “mengonversi DGN ke PNG”?
Mengonversi DGN ke PNG berarti merender gambar DGN berbasis vektor (2‑D atau 3‑D) menjadi format gambar raster (PNG). Ini berguna ketika Anda perlu menampilkan gambar CAD di web, menyematkannya dalam laporan, atau menghasilkan thumbnail tanpa memerlukan penampil CAD.

## Mengapa menggunakan Aspose.CAD untuk .NET untuk dukungan format file CAD?
- **Dukungan penuh format file CAD** – DGN, DWG, DXF, DWF, dan lainnya.  
- **Tanpa ketergantungan eksternal** – perpustakaan .NET murni, tanpa instalasi CAD native.  
- **Rendering fidelity tinggi** – mempertahankan ketebalan garis, warna, dan geometri 3‑D.  
- **Pemrosesan batch** – dengan mudah mengulang banyak file dalam aplikasi sisi server.

## Prasyarat

Sebelum kita mulai, pastikan Anda memiliki hal berikut:

- Pengetahuan dasar tentang pemrograman .NET.  
- Visual Studio terpasang di mesin Anda.  
- Perpustakaan Aspose.CAD untuk .NET, yang dapat Anda unduh [di sini](https://releases.aspose.com/cad/net/).

## Impor Namespace

Untuk memulai proyek Anda, impor namespace yang diperlukan ke dalam aplikasi .NET Anda. Langkah ini memastikan Anda memiliki akses ke fungsionalitas yang disediakan oleh Aspose.CAD untuk .NET.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Dgn;
using Aspose.CAD.FileFormats.Dgn.DgnElements;
```

## Cara Mengonversi DGN ke PNG

Berikut adalah panduan langkah demi langkah yang memandu Anda memuat file DGN, mengiterasi elemennya, menangani entitas 2‑D dan 3‑D, dan akhirnya mengekspor hasilnya ke gambar raster PNG.

### Langkah 1: Muat File DGN

Mulailah dengan memuat file DGN yang ada sebagai `DgnImage` dalam aplikasi .NET Anda.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (DgnImage dgnImage = (DgnImage)Image.Load(sourceFilePath))
{
    // Your code here
}
```

### Langkah 2: Iterasi Elemen DGN

Iterasi elemen DGN menggunakan loop `foreach`. Aspose.CAD untuk .NET menyediakan berbagai jenis elemen DGN yang dapat Anda gunakan.

```csharp
foreach (DgnDrawingElementBase element in dgnImage.Elements)
{
    // Your code here
}
```

### Langkah 3: Tangani Entitas 2‑D yang Sebelumnya Didukung

Entitas ini kini juga didukung untuk rendering 3‑D. Pernyataan switch memungkinkan Anda mengarahkan logika berdasarkan tipe elemen.

```csharp
switch (element.Metadata.Type)
{
    case DgnElementType.Line:
    case DgnElementType.Ellipse:
    case DgnElementType.Curve:
    // Additional cases
        {
            // Your code here
            break;
        }
}
```

### Langkah 4: Tangani Entitas 3‑D yang Didukung

Aspose.CAD menambahkan dukungan penuh untuk beberapa elemen DGN 3‑D. Perluas switch untuk memprosesnya sesuai kebutuhan.

```csharp
switch (element.Metadata.Type)
{
    case DgnElementType.SolidHeader3D:
    case DgnElementType.Cone:
    case DgnElementType.CellHeader:
        {
            // Your code here
            break;
        }
}
```

### Langkah 5: Ekspor dan Simpan sebagai PNG

Setelah manipulasi yang diperlukan, ekspor gambar DGN ke gambar raster PNG dan simpan ke direktori yang ditentukan.

```csharp
Console.WriteLine("\nThe DGN file exported successfully to raster image.\nFile saved at " + MyDir);
```

> **Tips pro:** Gunakan `Image.Save` dengan `new PngOptions()` untuk mengontrol resolusi, warna latar belakang, dan pengaturan khusus PNG lainnya.

## Ikhtisar Dukungan Format File CAD

Aspose.CAD untuk .NET tidak terbatas pada DGN. Ia juga mendukung DWG, DXF, DWF, dan banyak format CAD lainnya, memberikan Anda satu API untuk menangani spektrum luas gambar teknik. Ini menjadikannya ideal untuk proyek yang memerlukan **dukungan format file CAD** di berbagai standar.

## Masalah Umum & Solusi

| Masalah | Alasan | Solusi |
|-------|--------|-----|
| **Gambar muncul kosong** | Diekspor dengan DPI nol | Tentukan `ResolutionX` dan `ResolutionY` dalam `PngOptions`. |
| **Geometri 3‑D hilang** | Tipe elemen tidak ditangani dalam switch | Tambahkan kasus `DgnElementType` yang hilang dan render sesuai. |
| **Kehabisan memori pada file besar** | Memuat seluruh file sekaligus | Proses elemen dalam batch atau gunakan streaming bila memungkinkan. |

## Pertanyaan yang Sering Diajukan

### Q1: Di mana saya dapat menemukan dokumentasi untuk Aspose.CAD untuk .NET?
A1: Anda dapat menemukan dokumentasi [di sini](https://reference.aspose.com/cad/net/).

### Q2: Bagaimana cara mengunduh Aspose.CAD untuk .NET?
A2: Anda dapat mengunduh perpustakaan [di sini](https://releases.aspose.com/cad/net/).

### Q3: Apakah tersedia percobaan gratis untuk Aspose.CAD untuk .NET?
A3: Ya, Anda dapat mengakses percobaan gratis [di sini](https://releases.aspose.com/).

### Q4: Di mana saya dapat memperoleh lisensi sementara untuk Aspose.CAD untuk .NET?
A4: Lisensi sementara tersedia [di sini](https://purchase.aspose.com/temporary-license/).

### Q5: Butuh bantuan atau memiliki pertanyaan?
A5: Kunjungi forum komunitas Aspose.CAD untuk .NET [support forum](https://forum.aspose.com/c/cad/19).

---

**Terakhir Diperbarui:** 2026-03-29  
**Diuji Dengan:** Aspose.CAD untuk .NET 24.11  
**Penulis:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}