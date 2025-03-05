---
title: Mengganti Font di Aspose.CAD untuk .NET
linktitle: Mengganti Font
second_title: Aspose.CAD .NET - Format File CAD dan BIM
description: Pelajari cara mengganti font di Aspose.CAD dengan .NET dengan mudah. Ikuti panduan langkah demi langkah kami untuk penyesuaian font yang efisien dalam gambar CAD Anda.
type: docs
weight: 17
url: /id/net/cad-features-and-support/substituting-fonts/
---
## Perkenalan

Dalam bidang pengembangan CAD menggunakan .NET, kemampuan memanipulasi font adalah keterampilan yang sangat penting. Aspose.CAD untuk .NET menyediakan seperangkat alat yang kuat untuk tujuan ini, memungkinkan pengembang mengganti font dengan mulus dalam gambar CAD mereka. Dalam tutorial ini, kita akan menjelajahi proses langkah demi langkah, menunjukkan cara mencapai substitusi font secara efisien.

## Prasyarat

Sebelum mendalami tutorial, pastikan Anda memiliki hal berikut:

- Pengetahuan dasar tentang pemrograman .NET.
-  Aspose.CAD untuk .NET diinstal. Jika belum, Anda dapat mendownloadnya[Di Sini](https://releases.aspose.com/cad/net/).
- File gambar CAD untuk latihan langsung.

## Impor Namespace

Sebelum memulai, impor namespace yang diperlukan untuk mengakses fungsionalitas Aspose.CAD di aplikasi .NET Anda.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad.CadTables;
```

## Langkah 1: Muat Gambar CAD

 Mulailah dengan memuat gambar CAD ke dalam contoh`CadImage`. Pastikan Anda memberikan jalur yang benar ke direktori dokumen Anda.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

using (CadImage cadImage = (CadImage)Aspose.CAD.Image.Load(sourceFilePath))
{
    //Kode Anda untuk tindakan selanjutnya ada di sini
}
```

## Langkah 2: Ulangi Gaya

 Selanjutnya, ulangi gaya pada gambar CAD menggunakan a`foreach` lingkaran. Ini memungkinkan Anda mengakses dan memanipulasi gaya font individual.

```csharp
foreach (CadStyleTableObject style in cadImage.Styles)
{
    // Kode Anda untuk manipulasi gaya ada di sini
}
```

## Langkah 3: Gantikan Font Secara Global

 Untuk mengganti font secara global untuk semua gaya, atur`PrimaryFontName` properti untuk setiap gaya dengan nama font yang diinginkan, misalnya "Arial".

```csharp
foreach (CadStyleTableObject style in cadImage.Styles)
{
    style.PrimaryFontName = "Arial";
}
```

## Langkah 4: Gantikan Font dengan Nama Gaya

Jika Anda ingin mengganti font dengan gaya tertentu, Anda dapat melakukannya dengan mencentang nama gaya di dalam loop.

```csharp
foreach (CadStyleTableObject style in cadImage.Styles)
{
    if (style.StyleName == "Roman")
    {
        style.PrimaryFontName = "Arial";
    }
}
```

## Kesimpulan

Selamat! Anda telah berhasil mempelajari cara mengganti font di Aspose.CAD dengan .NET. Keterampilan ini berharga untuk menyesuaikan tampilan gambar CAD sesuai preferensi Anda.

## FAQ

### Q1: Dapatkah saya mengembalikan perubahan font di Aspose.CAD untuk .NET?

A1: Ya, Anda dapat mengembalikan perubahan font dengan memuat ulang gambar CAD asli atau dengan menyimpan cadangan.

### Q2: Apakah ada properti font lain yang dapat saya modifikasi?

A2: Tentu saja, selain itu`PrimaryFontName`, Aspose.CAD untuk .NET menyediakan akses ke berbagai properti terkait font untuk penyesuaian tingkat lanjut.

### Q3: Apakah Aspose.CAD kompatibel dengan format CAD yang berbeda?

A3: Ya, Aspose.CAD mendukung berbagai format CAD, memastikan fleksibilitas dalam proyek pengembangan Anda.

### Q4: Dapatkah saya mengotomatiskan substitusi font dalam pemrosesan batch?

A4: Tentu saja, Anda dapat menerapkan pemrosesan batch untuk mengotomatiskan substitusi font di beberapa gambar CAD.

### Q5: Di mana saya dapat menemukan dukungan tambahan untuk Aspose.CAD untuk .NET?

 A5: Untuk dukungan tambahan dan diskusi komunitas, kunjungi[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19).

