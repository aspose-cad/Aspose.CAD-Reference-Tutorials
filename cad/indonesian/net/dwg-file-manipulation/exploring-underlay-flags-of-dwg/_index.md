---
date: 2026-04-09
description: Pelajari cara mengonversi DWG ke gambar dan cara membaca flag underlay
  menggunakan Aspose.CAD untuk .NET dalam panduan langkah demi langkah ini.
keywords:
- convert dwg to image
- how to read underlay
- Aspose.CAD DWG underlay flags
linktitle: Menjelajahi Bendera Underlay pada File DWG
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Mengonversi DWG ke Gambar – Menjelajahi Flag Underlay pada File DWG - Tutorial
  Aspose.CAD
url: /id/net/dwg-file-manipulation/exploring-underlay-flags-of-dwg/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Menjelajahi Bendera Underlay pada File DWG - Tutorial Aspose.CAD

## Pendahuluan

Jika Anda menyelami dunia kompleks file CAD, khususnya file DWG, dan ingin **mengonversi DWG ke gambar** sekaligus menemukan **cara membaca bendera underlay**, Anda berada di tempat yang tepat. Tutorial ini memandu Anda melalui setiap langkah menggunakan pustaka Aspose.CAD untuk .NET yang kuat, sehingga Anda dapat mengekstrak informasi underlay dan merender gambar dengan percaya diri.

## Jawaban Cepat
- **Apa arti “convert DWG to image”?**  
  Artinya merender gambar DWG ke format raster (PNG, JPEG, dll.) menggunakan Aspose.CAD.
- **Metode apa yang mengungkapkan bendera underlay?**  
  Akses properti `Flags` pada objek `CadUnderlay` setelah memuat DWG.
- **Apakah saya memerlukan lisensi untuk Aspose.CAD?**  
  Lisensi sementara tersedia untuk evaluasi; lisensi penuh diperlukan untuk produksi.
- **Versi .NET apa yang didukung?**  
  .NET Framework 4.6+, .NET Core 3.1+, .NET 5/6 dan yang lebih baru.
- **Bisakah saya mengekstrak geometri underlay?**  
  Ya – jalur underlay, titik sisipan, skala, rotasi, dan status bendera semuanya dapat diakses.

## Apa itu “convert DWG to image” dan mengapa penting?

Mengonversi file DWG menjadi gambar memungkinkan Anda menampilkan gambar CAD di peramban, menyematkannya dalam laporan, atau membagikannya kepada pemangku kepentingan yang tidak memiliki penampil CAD. Saat merender, Anda sering perlu memeriksa objek **underlay** (mis., referensi DGN) untuk memastikan mereka tampil dengan benar. Memahami bendera underlay membantu Anda memecahkan masalah pemotongan, rendering monokrom, dan masalah visibilitas sebelum menghasilkan gambar akhir.

## Prasyarat

- Pemahaman dasar tentang pemrograman C# dan .NET.  
- Perpustakaan **Aspose.CAD for .NET** terpasang. Jika belum memilikinya, unduh **[here](https://releases.aspose.com/cad/net/)**.  
- File DWG untuk pengujian – file contoh **“BlockRefDgn.dwg”** digunakan sepanjang panduan ini.

## Impor Namespace

Untuk memulai, impor namespace yang diperlukan:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Langkah 1: Muat File DWG dan Konversi ke `CadImage`

Pertama, muat file DWG dan cast ke `CadImage`. Objek ini memberi Anda akses ke semua entitas gambar, termasuk underlay.

```csharp
string fileName = MyDir + "BlockRefDgn.dwg";

// Load DWG file and convert to CadImage
using (CadImage image = (CadImage)Image.Load(fileName))
{
    // Your code for subsequent steps will go here
}
```

## Langkah 2: Iterasi Melalui Entitas

Selanjutnya, loop melalui setiap entitas dalam gambar. Di sinilah Anda akan menemukan objek underlay.

```csharp
foreach (CadBaseEntity entity in image.Entities)
{
    // Your code for subsequent steps will go here
}
```

## Langkah 3: Periksa Tipe `CadDgnUnderlay`

Identifikasi entitas underlay dengan memeriksa tipe runtime mereka. Kelas `CadDgnUnderlay` mewakili underlay DGN yang disematkan dalam DWG.

```csharp
if (entity is CadDgnUnderlay)
{
    // Your code for subsequent steps will go here
}
```

## Langkah 4: Akses Bendera Underlay

Setelah Anda memiliki `CadDgnUnderlay`, cast ke `CadUnderlay` untuk membaca properti dan status benderanya. Bendera memberi tahu apakah underlay terlihat, dipotong, atau dirender dalam monokrom.

```csharp
CadUnderlay underlay = entity as CadUnderlay;

Console.WriteLine(underlay.UnderlayPath);
Console.WriteLine(underlay.UnderlayName);
Console.WriteLine(underlay.InsertionPoint.X);
Console.WriteLine(underlay.InsertionPoint.Y);
Console.WriteLine(underlay.RotationAngle);
Console.WriteLine(underlay.ScaleX);
Console.WriteLine(underlay.ScaleY);
Console.WriteLine(underlay.ScaleZ);
Console.WriteLine((underlay.Flags & UnderlayFlags.UnderlayIsOn) == UnderlayFlags.UnderlayIsOn);
Console.WriteLine((underlay.Flags & UnderlayFlags.ClippingIsOn) == UnderlayFlags.ClippingIsOn);
Console.WriteLine((underlay.Flags & UnderlayFlags.Monochrome) != UnderlayFlags.Monochrome);
```

### Apa yang ditunjukkan output

- **UnderlayPath / UnderlayName** – lokasi file DGN eksternal.  
- **InsertionPoint (X, Y)** – koordinat tempat underlay ditempatkan dalam ruang DWG.  
- **RotationAngle** – rotasi yang diterapkan pada underlay.  
- **ScaleX / ScaleY / ScaleZ** – faktor skala untuk masing-masing sumbu.  
- **Flags** – nilai boolean yang menunjukkan visibilitas (`UnderlayIsOn`), pemotongan (`ClippingIsOn`), dan rendering monokrom (`Monochrome`).

## Masalah Umum & Solusi

| Masalah | Alasan | Solusi |
|---------|--------|--------|
| Tidak ada output untuk pemeriksaan bendera | Bendera underlay default ke 0 ketika underlay dimatikan. | Pastikan DWG benar‑benar berisi underlay yang aktif atau ubah visibilitas di file CAD sumber. |
| `Invalid cast` exception | Entitas bukan `CadDgnUnderlay`. | Verifikasi guard `if (entity is CadDgnUnderlay)` sebelum melakukan casting. |
| Rendering gambar gagal setelah ekstraksi bendera | Underlay mungkin terpotong atau dimatikan, menghasilkan area kosong. | Sesuaikan bendera (`UnderlayIsOn = true`, `ClippingIsOn = false`) sebelum merender gambar akhir. |

## Pertanyaan yang Sering Diajukan

### Q1: Bisakah saya menggunakan Aspose.CAD untuk .NET dengan format file CAD lain?

A1: Aspose.CAD mendukung berbagai format CAD, termasuk DWG, DXF, DGN, dan lainnya. Periksa dokumentasi untuk daftar lengkap.

### Q2: Apakah lisensi sementara tersedia untuk Aspose.CAD untuk .NET?

A2: Ya, Anda dapat memperoleh lisensi sementara **[here](https://purchase.aspose.com/temporary-license/)**.

### Q3: Di mana saya dapat menemukan dukungan untuk Aspose.CAD untuk .NET?

A3: Kunjungi forum dukungan **[here](https://forum.aspose.com/c/cad/19)** untuk bantuan.

### Q4: Bagaimana cara membeli Aspose.CAD untuk .NET?

A4: Beli perpustakaan **[here](https://purchase.aspose.com/buy)**.

### Q5: Apakah tersedia percobaan gratis?

A5: Ya, Anda dapat mengakses percobaan gratis **[here](https://releases.aspose.com/)**.

## Kesimpulan

Selamat! Anda telah berhasil mempelajari **cara mengonversi DWG ke gambar** sekaligus menguasai **cara membaca bendera underlay** menggunakan Aspose.CAD untuk .NET. Dengan pengetahuan ini Anda dapat:

- Merender gambar DWG sebagai gambar raster untuk skenario web atau pelaporan.  
- Memeriksa dan memanipulasi properti underlay untuk memastikan tampilan yang tepat.  
- Men-debug masalah visibilitas, pemotongan, dan monokrom sebelum menghasilkan gambar akhir.

Jelajahi fitur Aspose.CAD lainnya seperti manajemen layer, ekstraksi teks, dan konversi batch untuk memperluas alur kerja otomatisasi CAD Anda.

---

**Last Updated:** 2026-04-09  
**Tested With:** Aspose.CAD for .NET 24.11  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}