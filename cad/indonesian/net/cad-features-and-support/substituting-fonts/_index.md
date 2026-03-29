---
date: 2026-03-29
description: Pelajari cara mengganti font di Aspose.CAD untuk .NET dengan cepat. Panduan
  langkah demi langkah ini menunjukkan cara mengatur nama font utama dan menyesuaikan
  gambar CAD secara efisien.
linktitle: Substituting Fonts
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Cara Mengganti Font di Aspose.CAD untuk .NET
url: /id/net/cad-features-and-support/substituting-fonts/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cara Mengganti Font di Aspose.CAD untuk .NET

## Pendahuluan

Dalam dunia pengembangan CAD menggunakan .NET, mempelajari **cara mengganti font** merupakan keterampilan penting yang dapat secara dramatis meningkatkan kualitas visual gambar Anda. Aspose.CAD untuk .NET menawarkan API yang sederhana yang memungkinkan Anda **mengatur nama font utama** untuk setiap gaya, menjadikan substitusi font secara global atau selektif sangat mudah. Dalam tutorial ini kami akan membahas seluruh proses—dari memuat gambar hingga menukar font secara global atau berdasarkan nama gaya tertentu.

## Jawaban Cepat
- **Apa kelas utama untuk manipulasi CAD?** `Aspose.CAD.Image` (atau yang diturunkan `CadImage`).
- **Properti mana yang mengubah font?** `PrimaryFontName` pada `CadStyleTableObject`.
- **Apakah saya dapat mengganti font untuk semua gaya sekaligus?** Ya, iterasi melalui `cadImage.Styles` dan atur properti tersebut.
- **Apakah saya membutuhkan lisensi untuk produksi?** Lisensi Aspose.CAD yang valid diperlukan untuk penggunaan non‑trial.
- **Versi .NET yang didukung?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.

## Apa itu Substitusi Font dalam CAD?
Substitusi font berarti mengganti jenis huruf asli yang digunakan dalam gambar CAD dengan yang lain yang tersedia di sistem target. Ini sangat berguna ketika font asli tidak ada, ketika Anda membutuhkan gaya korporat yang konsisten, atau saat menyiapkan gambar untuk pencetakan pada perangkat yang hanya mendukung sejumlah font terbatas.

## Mengapa Mengganti Font dengan Aspose.CAD?
- **Tidak ada ketergantungan eksternal** – perpustakaan menangani pemetaan font secara internal.
- **Berfungsi dengan banyak format** – DXF, DWG, DGN, dan lainnya.
- **Kontrol programatik** – mengotomatiskan proses untuk konversi batch atau pipeline CI.
- **Mempertahankan geometri gambar** – hanya representasi visual teks yang berubah.

## Prasyarat

- Pengetahuan dasar tentang pemrograman .NET.
- Aspose.CAD untuk .NET terpasang. Jika Anda belum menginstalnya, unduh [di sini](https://releases.aspose.com/cad/net/).
- File gambar CAD (DXF, DWG, dll.) untuk percobaan.

## Impor Namespace

Sebelum memulai, impor namespace yang diperlukan untuk mengakses fungsionalitas Aspose.CAD dalam aplikasi .NET Anda.

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

Mulailah dengan memuat gambar CAD ke dalam sebuah instance `CadImage`. Pastikan Anda memberikan jalur yang benar ke direktori dokumen Anda.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

using (CadImage cadImage = (CadImage)Aspose.CAD.Image.Load(sourceFilePath))
{
    // Your code for further actions goes here
}
```

## Langkah 2: Iterasi Gaya

Selanjutnya, iterasi gaya dalam gambar CAD menggunakan loop `foreach`. Ini memungkinkan Anda mengakses dan memanipulasi gaya font individu.

```csharp
foreach (CadStyleTableObject style in cadImage.Styles)
{
    // Your code for style manipulation goes here
}
```

## Cara Mengatur Nama Font Utama untuk Substitusi Font

Properti `PrimaryFontName` pada setiap `CadStyleTableObject` mengontrol font mana yang digunakan saat gambar dirender. Dengan mengatur properti ini Anda secara efektif mengganti font asli.

### Langkah 3: Substitusi Font Secara Global

Untuk mengganti font untuk **semua** gaya, atur properti `PrimaryFontName` untuk setiap gaya ke nama font yang diinginkan, misalnya, `"Arial"`.

```csharp
foreach (CadStyleTableObject style in cadImage.Styles)
{
    style.PrimaryFontName = "Arial";
}
```

### Langkah 4: Substitusi Font Berdasarkan Nama Gaya

Jika Anda hanya perlu mengganti font untuk gaya tertentu (misalnya, gaya bernama `"Roman"`), tambahkan pemeriksaan kondisi di dalam loop.

```csharp
foreach (CadStyleTableObject style in cadImage.Styles)
{
    if (style.StyleName == "Roman")
    {
        style.PrimaryFontName = "Arial";
    }
}
```

## Masalah Umum & Pemecahan Masalah

| Masalah | Penyebab | Solusi |
|-------|-------|-----|
| Font tidak berubah setelah menjalankan kode | Gambar di-cache atau dibuka dalam mode baca‑saja | Pastikan Anda menyimpan gambar setelah modifikasi (`cadImage.Save(...)`) atau memuat ulang file untuk memverifikasi. |
| Font yang diinginkan tidak ditemukan di sistem | Font tidak terinstal pada mesin yang menjalankan kode | Instal font TrueType/OpenType yang diperlukan atau sematkan dalam sumber daya aplikasi. |
| Teks muncul berantakan | Enkoding tidak tepat atau dukungan Unicode tidak ada | Gunakan font yang mendukung set karakter yang diperlukan (mis., Arial Unicode MS). |

## Pertanyaan yang Sering Diajukan

**Q: Apakah saya dapat mengembalikan perubahan font di Aspose.CAD untuk .NET?**  
A: Ya, Anda dapat mengembalikan dengan memuat ulang gambar CAD asli atau dengan menyimpan salinan cadangan sebelum melakukan modifikasi.

**Q: Apakah ada properti font lain yang dapat saya modifikasi?**  
A: Tentu saja. Selain `PrimaryFontName`, Anda dapat bekerja dengan `SecondaryFontName`, `FontFamily`, dan atribut terkait gaya lainnya untuk penyesuaian lanjutan.

**Q: Apakah Aspose.CAD kompatibel dengan berbagai format CAD?**  
A: Ya, Aspose.CAD mendukung berbagai format seperti DXF, DWG, DGN, DWF, dan lainnya, memberi Anda fleksibilitas di seluruh proyek.

**Q: Apakah saya dapat mengotomatisasi substitusi font dalam pemrosesan batch?**  
A: Tentu. Bungkus logika pemuatan dan substitusi dalam loop yang mengiterasi folder berisi file CAD, atau integrasikan ke dalam pipeline CI/CD.

**Q: Di mana saya dapat menemukan dukungan tambahan untuk Aspose.CAD untuk .NET?**  
A: Untuk dukungan tambahan dan diskusi komunitas, kunjungi [forum Aspose.CAD](https://forum.aspose.com/c/cad/19).

---

**Terakhir Diperbarui:** 2026-03-29  
**Diuji Dengan:** Aspose.CAD for .NET (latest release)  
**Penulis:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}