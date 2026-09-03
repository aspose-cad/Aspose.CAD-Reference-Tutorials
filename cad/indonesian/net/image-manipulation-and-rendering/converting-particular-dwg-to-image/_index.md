---
date: 2026-08-12
description: Ekstrak teks dari DWG dan konversi DWG tertentu menjadi gambar dalam
  C# menggunakan Aspose.CAD untuk .NET. Pelajari langkah demi langkah dengan contoh
  kode.
keywords:
- extract text from dwg
- convert specific dwg to image
- Aspose.CAD .NET
lastmod: 2026-08-12
linktitle: Mengonversi DWG Tertentu menjadi Gambar dalam C#
og_description: Ekstrak teks dari DWG dan konversi DWG tertentu menjadi gambar dalam
  C# dengan Aspose.CAD. Ikuti panduan singkat ini untuk implementasi cepat.
og_image_alt: Guide showing DWG to image conversion and text extraction using Aspose.CAD
  in C#
og_title: Ekstrak teks dari DWG dan konversi DWG tertentu menjadi gambar dalam C#
schemas:
- author: Aspose
  dateModified: '2026-08-12'
  description: Extract text from DWG and convert specific DWG to image in C# using
    Aspose.CAD for .NET. Learn step‑by‑step with code snippets.
  headline: Extract text from DWG and convert specific DWG to image in C#
  type: TechArticle
- questions:
  - answer: Aspose.CAD supports DWG releases from AutoCAD 2000 up to the latest 2024
      version, covering over 90 % of files created in the field.
    question: Is Aspose.CAD compatible with all versions of DWG files?
  - answer: Yes – you can change resolution, image format, anti‑aliasing, and background
      color to suit PNG, JPEG, or PDF targets.
    question: Can I customize the rasterization options for different outputs?
  - answer: Explore the comprehensive [Aspose.CAD documentation](https://reference.aspose.com/cad/net/)
      for more code samples and API details.
    question: Where can I find additional examples and documentation?
  - answer: Absolutely – you can download a trial version on the **[Aspose trial download
      page](https://releases.aspose.com/)** and evaluate all features without restrictions
      for 30 days.
    question: Is there a free trial available for Aspose.CAD?
  - answer: Join the active [Aspose.CAD forum](https://forum.aspose.com/c/cad/19)
      where developers share solutions and the Aspose team answers questions.
    question: How can I get support or connect with the community?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- extract text from dwg
- Aspose.CAD
- C# CAD processing
title: Ekstrak teks dari DWG dan konversi DWG tertentu menjadi gambar dalam C#
url: /id/net/image-manipulation-and-rendering/converting-particular-dwg-to-image/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Mengonversi DWG tertentu menjadi gambar di C# - Panduan Aspose.CAD

## Pendahuluan

Dalam aplikasi rekayasa modern, Anda sering perlu **mengekstrak teks dari file DWG** dan **mengonversi DWG tertentu menjadi format gambar** untuk pelaporan atau visualisasi. Aspose.CAD untuk .NET memberikan API lengkap yang menangani kedua tugas tersebut tanpa memerlukan perangkat lunak CAD eksternal. Pada tutorial ini Anda akan belajar cara memuat DWG, menyaring entitas teks, meraster gambar, dan akhirnya menyimpan hasilnya sebagai gambar PDF—semua dengan kode C# yang bersih.

## Jawaban cepat
- **Apa langkah pertama?** Muat file DWG dengan `new CadImage("file.dwg")`.  
- **Kelas mana yang menyaring teks?** Gunakan `CadEntityFilter` untuk memilih entitas `Text`.  
- **Bagaimana cara menentukan ukuran gambar?** Atur `Width` dan `Height` pada `CadRasterizationOptions`.  
- **Format output apa yang digunakan?** Contoh menyimpan ke PDF, yang menyisipkan gambar raster.  
- **Apakah saya memerlukan lisensi untuk produksi?** Ya – lisensi komersial Aspose.CAD menghapus batas evaluasi.

## Cara mengekstrak teks dari dwg?

Muat DWG, terapkan filter yang hanya memilih entitas teks, lalu baca properti `TextString` dari setiap entitas. Pendekatan ini mengembalikan semua anotasi, label, atau teks dimensi yang ada dalam gambar, memungkinkan Anda menggunakannya kembali untuk pencarian, pengindeksan, atau pelaporan.

## Mengapa mengonversi dwg tertentu menjadi gambar?

Mengonversi DWG menjadi gambar raster memungkinkan Anda menyisipkan gambar dalam dokumen, halaman web, atau aplikasi seluler yang tidak dapat merender format CAD asli. Aspose.CAD memproses **lebih dari 50+ format CAD** dan dapat meraster gambar dengan ratusan halaman sambil menggunakan kurang dari 200 MB memori, sehingga cocok untuk skenario server dengan throughput tinggi.

## Prasyarat

- Visual Studio (edisi terbaru apa pun) untuk mengompilasi dan menjalankan proyek C#.  
- Aspose.CAD untuk .NET – pastikan perpustakaan telah terpasang. Anda dapat menemukan tautan unduhan di **[halaman unduhan Aspose.CAD untuk .NET](https://releases.aspose.com/cad/net/)**.  
- File DWG yang ingin Anda kerjakan; file contoh *visualization_-_conference_room.dwg* digunakan dalam potongan kode.

## Impor namespace

Namespace berikut memberi Anda akses ke kelas CAD inti, opsi rasterisasi, dan pembantu output PDF:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadConsts;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## Langkah 1: memuat file dwg

Buat instance `CadImage` dengan memberikan jalur file DWG Anda. Objek `CadImage` mewakili seluruh gambar dalam memori dan menyediakan akses ke lapisan, entitas, serta metadata-nya.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "visualization_-_conference_room.dwg";
var cadImage = (CadImage)Aspose.CAD.Image.Load(sourceFilePath);
```

## Langkah 2: menyaring entitas

`CadEntityFilter` memungkinkan Anda memilih hanya entitas yang diperlukan. Pada panduan ini kami mengonfigurasinya untuk mempertahankan objek **teks**, mengabaikan garis, lingkaran, dan geometri lain yang tidak Anda inginkan dalam gambar akhir.

```csharp
CadBaseEntity[] entities = cadImage.Entities;
List<CadBaseEntity> filteredEntities = new List<CadBaseEntity>();

foreach (CadBaseEntity baseEntity in entities)
{
    // Selection or filtration of entities
    if (baseEntity.TypeName == CadEntityTypeName.TEXT)
    {
        filteredEntities.Add(baseEntity);
    }
}

cadImage.Entities = filteredEntities.ToArray();
```

## Langkah 3: mengatur opsi rasterisasi

`CadRasterizationOptions` mengontrol cara gambar diubah menjadi bitmap. Anda dapat menentukan ukuran output, warna latar belakang, dan resolusi (DPI). Definisi berikut memperkenalkan kelas tersebut:

Kelas `CadRasterizationOptions` menentukan dimensi gambar, resolusi, dan pengaturan rendering untuk mengonversi gambar CAD ke format raster.  

Atur lebar, tinggi, dan warna latar belakang yang diinginkan sebelum meneruskan opsi ke pengekspor PDF.

```csharp
Aspose.CAD.ImageOptions.CadRasterizationOptions rasterizationOptions =
    new Aspose.CAD.ImageOptions.CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
rasterizationOptions.AutomaticLayoutsScaling = true;
```

## Langkah 4: mengatur opsi PDF

`PdfOptions` menggabungkan pengaturan rasterisasi dengan fitur khusus PDF seperti kompresi. Definisi kelas ini muncul pertama kali:

`PdfOptions` mengenkapsulasi parameter pembuatan PDF, termasuk opsi rasterisasi yang menentukan bagaimana data CAD dirender di dalam dokumen PDF.  

Tetapkan instance `CadRasterizationOptions` yang telah dibuat sebelumnya ke properti `VectorRasterizationOptions`.

```csharp
Aspose.CAD.ImageOptions.PdfOptions pdfOptions = new Aspose.CAD.ImageOptions.PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Langkah 5: menyimpan sebagai PDF

Akhirnya, panggil metode `Save` pada objek `CadImage`, berikan nama file target dan `PdfOptions` yang telah dikonfigurasi. PDF akan berisi gambar berkualitas tinggi dari gambar yang telah disaring.

```csharp
string outFile = MyDir + "result_out_generated.pdf";
cadImage.Save(outFile, pdfOptions);
```

## Masalah umum dan pemecahan masalah

- **Teks tidak muncul setelah penyaringan** – Pastikan DWG memang berisi entitas `Text`; beberapa gambar menyimpan anotasi sebagai `MText`. Sesuaikan filter untuk menyertakan `MText` bila diperlukan.  
- **Gambar output kosong** – Verifikasi bahwa DPI rasterisasi cukup tinggi (300 DPI adalah nilai aman) dan bahwa warna latar belakang tidak diatur menjadi transparan saat melihat PDF.  
- **Kesalahan out‑of‑memory pada file besar** – Gunakan overload `LoadOptions` yang memungkinkan streaming, sehingga seluruh file tidak dimuat ke memori sekaligus.

## Pertanyaan yang sering diajukan

**T: Apakah Aspose.CAD kompatibel dengan semua versi file DWG?**  
J: Aspose.CAD mendukung rilis DWG dari AutoCAD 2000 hingga versi terbaru 2024, mencakup lebih dari 90 % file yang dibuat di lapangan.

**T: Bisakah saya menyesuaikan opsi rasterisasi untuk output yang berbeda?**  
J: Ya – Anda dapat mengubah resolusi, format gambar, anti‑aliasing, dan warna latar belakang untuk memenuhi kebutuhan PNG, JPEG, atau target PDF.

**T: Di mana saya dapat menemukan contoh tambahan dan dokumentasi?**  
J: Jelajahi dokumentasi lengkap [Aspose.CAD](https://reference.aspose.com/cad/net/) untuk lebih banyak contoh kode dan detail API.

**T: Apakah ada versi percobaan gratis untuk Aspose.CAD?**  
J: Tentu – Anda dapat mengunduh versi percobaan di **[halaman unduhan percobaan Aspose](https://releases.aspose.com/)** dan mengevaluasi semua fitur tanpa batasan selama 30 hari.

**T: Bagaimana cara mendapatkan dukungan atau terhubung dengan komunitas?**  
J: Bergabunglah dengan forum aktif [Aspose.CAD](https://forum.aspose.com/c/cad/19) di mana para pengembang berbagi solusi dan tim Aspose menjawab pertanyaan.

---

**Terakhir diperbarui:** 2026-08-12  
**Diuji dengan:** Aspose.CAD 24.11 untuk .NET  
**Penulis:** Aspose

## Tutorial Terkait

- [Mencari Teks dalam File DWG dengan C# - Tutorial Aspose.CAD](/cad/net/text-search-and-manipulation/searching-text-in-dwg-files/)
- [Mengonversi Gambar CAD ke Gambar Raster di Aspose.CAD untuk .NET](/cad/net/cad-drawing-manipulation/convert-cad-drawing-to-raster-image/)
- [Merender Dokumen DWG di C# - Panduan Aspose.CAD](/cad/net/image-manipulation-and-rendering/rendering-dwg-documents/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< blocks/products/products-backtop-button >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}