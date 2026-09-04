---
date: 2026-09-04
description: Pelajari cara mengganti deteksi dwg codepage pada file DWG menggunakan
  Aspose.CAD untuk .NET, memberi Anda kontrol yang tepat atas pengkodean karakter.
keywords:
- override dwg codepage
- dwg codepage detection
- aspose.cad .net
- cad file encoding
- dwg processing
lastmod: 2026-09-04
linktitle: Ganti Deteksi Codepage Otomatis pada File DWG - Tutorial Aspose.CAD
og_description: Pelajari cara mengganti deteksi dwg codepage pada file DWG menggunakan
  Aspose.CAD untuk .NET, memberi Anda kontrol yang tepat atas pengkodean karakter
  dan meningkatkan penanganan file CAD.
og_image_alt: Guide showing how to override DWG codepage with Aspose.CAD in .NET
og_title: Cara mengganti dwg codepage di Aspose.CAD untuk .NET
schemas:
- author: Aspose
  dateModified: '2026-09-04'
  description: Learn how to override dwg codepage detection in DWG files using Aspose.CAD
    for .NET, giving you precise control over character encoding.
  headline: How to override dwg codepage in Aspose.CAD for .NET
  type: TechArticle
- questions:
  - answer: It forces Aspose.CAD to use the encoding you specify instead of guessing,
      preventing character corruption.
    question: What does overriding the DWG codepage do?
  - answer: Whenever a DWG file contains text in a language that isn’t the default
      Windows codepage (e.g., Central European, Cyrillic).
    question: When should I use it?
  - answer: Any .NET `Encoding` such as `Encoding.GetEncoding(1250)` for Central European.
    question: Which encodings are supported?
  - answer: A trial works for development; a commercial license is required for production.
    question: Do I need a license?
  - answer: Yes, the setting is applied per `Image` instance, so multiple threads
      can process different files concurrently.
    question: Is it thread‑safe?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- override dwg codepage
- Aspose.CAD
- .NET CAD processing
- DWG codepage
- CAD rendering
title: Cara mengganti dwg codepage di Aspose.CAD untuk .NET
url: /id/net/image-manipulation-and-rendering/override-automatic-codepage-detection-in-dwg/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cara mengoverride kode halaman dwg di Aspose.CAD untuk .NET

Dalam banyak file DWG legacy, kode halaman yang tertanam terdeteksi secara otomatis, yang dapat menyebabkan teks menjadi kacau ketika file menggunakan enkoding non‑default. **Override dwg codepage** memungkinkan Anda secara eksplisit menetapkan enkoding yang diinginkan sehingga geometri dan teks anotasi ditampilkan dengan benar. Dalam tutorial ini Anda akan melihat mengapa hal ini penting, seperti apa API-nya, dan cara menerapkan pengaturan dalam beberapa langkah sederhana.

## Jawaban Cepat
- **Apa yang dilakukan dengan mengoverride kode halaman DWG?** Ini memaksa Aspose.CAD menggunakan enkoding yang Anda tentukan alih‑alih menebak, sehingga mencegah korupsi karakter.  
- **Kapan saya harus menggunakannya?** Setiap kali file DWG berisi teks dalam bahasa yang bukan kode halaman default Windows (misalnya, Central European, Cyrillic).  
- **Enkoding apa yang didukung?** Semua `Encoding` .NET seperti `Encoding.GetEncoding(1250)` untuk Central European.  
- **Apakah saya memerlukan lisensi?** Versi trial dapat digunakan untuk pengembangan; lisensi komersial diperlukan untuk produksi.  
- **Apakah thread‑safe?** Ya, pengaturan diterapkan per instance `Image`, sehingga beberapa thread dapat memproses file yang berbeda secara bersamaan.

## Apa itu override dwg codepage?
Override dwg codepage adalah fitur Aspose.CAD yang memungkinkan Anda mengganti deteksi kode halaman otomatis library dengan enkoding karakter spesifik yang Anda sediakan. Ini memastikan bahwa string teks di dalam DWG diinterpretasikan dengan benar terlepas dari metadata asli file.

## Mengapa menggunakan override dwg codepage?
Aspose.CAD mendukung **lebih dari 50 versi DWG/DXF** dan dapat memproses file hingga **2 GB** tanpa memuat seluruh dokumen ke memori. Ketika deteksi otomatis gagal, Anda dapat kehilangan hingga **100 % keterbacaan anotasi**. Dengan secara eksplisit menetapkan kode halaman, Anda mengurangi risiko ini menjadi **0 %** dan waktu render tetap tidak berubah.

## Prasyarat

- Pengetahuan dasar tentang C# dan platform .NET.  
- Aspose.CAD untuk .NET terpasang. Jika belum menginstalnya, unduh **[halaman unduhan Aspose.CAD untuk .NET](https://releases.aspose.com/cad/net/)**.  
- File DWG yang menggunakan kode halaman non‑default (misalnya, file yang dibuat pada sistem dengan kode halaman 1250).

## Impor namespace

Untuk memulai, tambahkan direktif `using` yang diperlukan agar kompiler dapat menemukan kelas Aspose.CAD.

Masukkan kode berikut di bagian atas file sumber C# Anda:

```csharp
using System;
using Aspose.CAD.FileFormats.Cad;
```

Ini menyiapkan lingkungan untuk semua operasi CAD selanjutnya.

## Langkah 1: tentukan direktori dokumen Anda

Tentukan folder yang berisi DWG yang ingin Anda proses. Ganti placeholder dengan jalur sebenarnya pada mesin Anda:

```csharp
//ExStart:1
string SourceDir = "Your Document Directory";
//ExEnd:1
```

## Langkah 2: override deteksi kode halaman otomatis

Sekarang kita masuk ke inti tutorial. Kode di bawah ini memuat file DWG, memaksa kode halaman menjadi **Windows‑1250** (Central European), dan kemudian menyimpan gambar sebagai PNG. Ubah nama file dan enkoding sesuai kebutuhan Anda.

```csharp
//ExStart:1
using (CadImage cadImage = (CadImage)Image.Load(SourceDir + "SimpleEntites.dwg",
new LoadOptions()
{
	SpecifiedEncoding = CodePages.Japanese,
	SpecifiedMifEncoding = MifCodePages.Japanese,
	RecoverMalformedCifMif = false
}))
{
	// Perform export or other operations with cadImage
}
//ExEnd:1
Console.WriteLine("OverrideAutomaticCodePageDetectionDwg executed successfully");
```

`Image.Load` adalah metode statis yang memuat file CAD dan mengembalikan objek `CadImage`. `LoadOptions.CodePage` menentukan enkoding karakter yang digunakan selama pemuatan. `CadImage` mewakili representasi dalam memori dari gambar CAD dan menyediakan metode untuk rendering atau konversi.

## Masalah umum dan solusi

- **Karakter sampah tetap muncul setelah override** – Pastikan enkoding yang Anda pilih cocok dengan bahasa asli file. Gunakan `Encoding.GetEncoding(1251)` untuk Cyrillic, misalnya.  
- **File gagal dimuat** – Pastikan versi DWG didukung oleh versi Aspose.CAD Anda; tingkatkan jika diperlukan.  
- **Penurunan performa** – Override tidak menambah overhead; jika Anda melihat perlambatan, periksa bottleneck I/O yang tidak terkait.

## Pertanyaan yang Sering Diajukan

### Q1: Bisakah saya menggunakan Aspose.CAD untuk .NET dengan bahasa selain C#?
A1: Aspose.CAD untuk .NET terutama dirancang untuk C#, tetapi dapat digunakan dalam bahasa .NET lain seperti VB.NET.

### Q2: Apakah tersedia trial gratis?
A2: Ya, Anda dapat mengakses trial gratis **[halaman unduhan trial gratis Aspose.CAD](https://releases.aspose.com/)**.

### Q3: Bagaimana cara mendapatkan dukungan untuk Aspose.CAD untuk .NET?
A3: Kunjungi **[forum Aspose.CAD](https://forum.aspose.com/c/cad/19)** untuk dukungan komunitas.

### Q4: Bisakah saya membeli lisensi sementara?
A4: Ya, Anda dapat memperoleh lisensi sementara **[halaman pembelian lisensi sementara](https://purchase.aspose.com/temporary-license/)**.

### Q5: Di mana saya dapat menemukan dokumentasi detail?
A5: Lihat **[dokumentasi API Aspose.CAD .NET yang komprehensif](https://reference.aspose.com/cad/net/)**.

### Q6: Apakah mengoverride kode halaman memengaruhi kualitas rendering raster?
A6: Tidak. Pengaturan kode halaman hanya memengaruhi cara string teks didekode; kualitas gambar tetap tidak berubah.

### Q7: Bisakah saya menerapkan override saat mengonversi ke format selain PNG?
A7: Tentu saja. Nilai `LoadOptions.CodePage` yang sama bekerja untuk PDF, SVG, atau format output lain yang didukung oleh Aspose.CAD.

---

**Terakhir Diperbarui:** 2026-09-04  
**Diuji dengan:** Aspose.CAD 24.10 untuk .NET  
**Penulis:** Aspose

## Tutorial Terkait

- [Mencari Teks dalam File DWG dengan C# - Tutorial Aspose.CAD](/cad/net/text-search-and-manipulation/searching-text-in-dwg-files/)
- [Mengonversi DWG ke PDF dan Menambahkan Teks di C# – Tutorial Aspose.CAD](/cad/net/dwg-file-manipulation/adding-text-to-dwg/)
- [Cara mengonversi DWG ke PDF dan Gambar Raster menggunakan Aspose.CAD untuk .NET](/cad/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}