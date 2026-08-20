---
date: 2026-04-09
description: Pelajari cara memuat file DWFX dengan C# dan mengonversi CAD ke PDF menggunakan
  Aspose.CAD untuk .NET. Panduan langkah demi langkah untuk integrasi yang mulus.
keywords:
- load dwfx file c#
- c# convert cad to pdf
- aspose.cad dwfx
linktitle: Membuka dan Mengakses File DWFX di C#
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Cara Memuat File DWFX di C# dengan Panduan Aspose.CAD
url: /id/net/dwg-file-manipulation/opening-and-accessing-dwfx-files/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cara Memuat File DWFX di C# dengan Panduan Aspose.CAD

## Pendahuluan

Jika Anda perlu **load DWFX file C#** dan mengubahnya menjadi PDF, Anda berada di tempat yang tepat. Dalam tutorial ini kami akan menjelaskan langkah‑langkah tepat untuk membuka gambar DWFX dengan Aspose.CAD untuk .NET, mengonfigurasi rasterisasi, dan akhirnya **c# convert CAD to PDF**. Baik Anda membuat utilitas desktop maupun layanan web, pendekatannya tetap sama dan bekerja dengan versi .NET apa pun yang didukung oleh Aspose.CAD.

## Jawaban Cepat
- **What library do I need?** Aspose.CAD for .NET  
- **Can I convert DWFX to PDF?** Yes – just configure `CadRasterizationOptions` and use `PdfOptions`.  
- **Which .NET versions are supported?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **Do I need a license for testing?** A free trial works for development; a permanent license is required for production.  
- **How long does the code take to run?** Loading and converting a typical DWFX file finishes in under a second on a modern CPU.

## Apa itu File DWFX?

DWFX (Design Web Format XPS) adalah representasi berbasis XML dari gambar CAD yang dapat dirender di peramban dan penampil lainnya. Karena menyimpan data vektor, format ini ideal untuk konversi PDF berkualitas tinggi tanpa kehilangan detail.

## Mengapa Menggunakan Aspose.CAD untuk Memuat File DWFX di C#?

* **Full format support** – Aspose.CAD memahami DWFX bersama puluhan format CAD lainnya.  
* **No external dependencies** – Pure .NET, no need for AutoCAD or other native components.  
* **Easy raster‑to‑vector conversion** – Switch between raster images and vector PDFs with a few lines of code.  

## Prasyarat

Sebelum kita masuk ke kode, pastikan Anda memiliki:

1. **Aspose.CAD for .NET** terpasang. Anda dapat mengunduhnya [here](https://releases.aspose.com/cad/net/).  
2. Sebuah folder yang berisi file DWFX yang ingin Anda proses. Catat jalur lengkap untuk lokasi sumber dan output.

## Cara Memuat File DWFX di C#

Berikut adalah panduan langkah‑demi‑langkah. Setiap langkah disertai penjelasan singkat, diikuti oleh blok kode tepat yang perlu Anda salin.

### Impor Namespace

```csharp
using Aspose.CAD.ImageOptions;
using System;
```

Namespace ini memberi Anda akses ke kelas `Image` untuk memuat file CAD serta opsi yang diperlukan untuk rasterisasi dan output PDF.

### Langkah 1: Siapkan Direktori Sumber dan Output

```csharp
string SourceDir = "Your Document Directory";
string OutputDir = "Your Document Directory";
```

Ganti `"Your Document Directory"` dengan jalur tempat file DWFX Anda berada dan tempat Anda ingin menyimpan PDF.

### Langkah 2: Muat File DWFX

```csharp
using (Image cadDrawing = Image.Load(SourceDir + "Tyrannosaurus.dwfx"))
```

`Image.Load` membaca file DWFX ke dalam objek `Image` yang dapat diproses oleh Aspose.CAD. Ubah `"Tyrannosaurus.dwfx"` menjadi nama gambar Anda sendiri.

### Langkah 3: Konfigurasikan Opsi Rasterisasi

```csharp
var rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = cadDrawing.Size.Width;
rasterizationOptions.PageHeight = cadDrawing.Size.Height;
```

Opsi rasterisasi memberi tahu Aspose.CAD seberapa besar halaman yang dihasilkan. Menggunakan dimensi gambar asli mempertahankan skala yang tepat.

### Langkah 4: Simpan sebagai PDF (c# convert CAD to PDF)

```csharp
PdfOptions CADf = new PdfOptions();
CADf.VectorRasterizationOptions = rasterizationOptions;
cadDrawing.Save(OutputDir + "OpenDwfxFile_out.pdf", CADf);
```

Di sini kami **c# convert CAD to PDF** dengan melampirkan pengaturan rasterisasi ke objek `PdfOptions` dan memanggil `Save`. File output akan ditempatkan di folder yang Anda tentukan.

### Langkah 5: Tampilkan Pesan Sukses

```csharp
Console.WriteLine("OpenDwfxFile executed successfully");
```

Pesan konsol sederhana memberi tahu Anda bahwa konversi selesai tanpa error.

## Masalah Umum & Tips

* **File not found** – Periksa kembali jalur `SourceDir` dan pastikan nama file cocok persis, termasuk huruf besar/kecil.  
* **Blank PDF** – Pastikan file DWFX memang berisi data vektor; beberapa alat ekspor menghasilkan gambar kosong.  
* **Performance** – Untuk gambar yang sangat besar, pertimbangkan mengurangi `PageWidth`/`PageHeight` atau menetapkan `Resolution` yang lebih rendah pada `CadRasterizationOptions`.

## Pertanyaan yang Sering Diajukan

### Q1: Apakah Aspose.CAD untuk .NET kompatibel dengan semua file DWFX?

A1: Aspose.CAD untuk .NET mendukung berbagai format CAD, termasuk DWFX. Namun, disarankan memeriksa dokumentasi untuk detail kompatibilitas spesifik.

### Q2: Di mana saya dapat menemukan dokumentasi untuk Aspose.CAD untuk .NET?

A2: Dokumentasi tersedia [here](https://reference.aspose.com/cad/net/).

### Q3: Bisakah saya mencoba Aspose.CAD untuk .NET sebelum membeli?

A3: Ya, Anda dapat mengunduh versi percobaan gratis [here](https://releases.aspose.com/).

### Q4: Bagaimana cara mendapatkan lisensi sementara untuk Aspose.CAD untuk .NET?

A4: Lisensi sementara dapat diperoleh [here](https://purchase.aspose.com/temporary-license/).

### Q5: Butuh dukungan atau memiliki pertanyaan lain?

A5: Kunjungi [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) untuk bantuan.

### Q6: Bisakah saya memproses batch beberapa file DWFX?

A6: Tentu saja. Bungkus logika pemuatan dan penyimpanan di dalam loop `foreach` yang mengiterasi file‑file dalam sebuah direktori.

### Q7: Apakah konversi mempertahankan lapisan dan warna?

A7: Informasi vektor seperti lapisan dan warna dipertahankan dalam PDF ketika DWFX sumber berisi data tersebut.

---

**Terakhir Diperbarui:** 2026-04-09  
**Diuji Dengan:** Aspose.CAD for .NET 24.11  
**Penulis:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}