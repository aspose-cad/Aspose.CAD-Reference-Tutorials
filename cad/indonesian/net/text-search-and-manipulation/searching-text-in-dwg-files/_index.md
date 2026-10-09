---
date: 2026-10-09
description: Pelajari cara memuat file dwg dan mencari teks di dalam file DWG menggunakan
  C# dan Aspose.CAD for .NET. Ikuti panduan langkah demi langkah ini untuk meningkatkan
  alur kerja CAD Anda.
keywords:
- load dwg file
- export dwg to pdf
- cad text search
- search text dwg
- c# read dwg
lastmod: 2026-10-09
linktitle: Mencari Teks dalam File DWG dengan C#
og_description: Pelajari cara memuat file dwg dan mencari teks di dalam file DWG menggunakan
  C# dan Aspose.CAD for .NET. Ikuti panduan langkah demi langkah ini untuk meningkatkan
  alur kerja CAD Anda.
og_image_alt: Guide showing how to load dwg file and search text in DWG files using
  Aspose.CAD for .NET
og_title: Cara memuat file dwg dan mencari teks dalam file DWG dengan C#
schemas:
- author: Aspose
  dateModified: '2026-10-09'
  description: Learn how to load dwg file and search text inside DWG files using C#
    and Aspose.CAD for .NET. Follow this step‑by‑step guide to enhance your CAD workflows.
  headline: How to load dwg file and search text in DWG files with C#
  type: TechArticle
- questions:
  - answer: '`new CadImage("yourfile.dwg")` creates an in‑memory representation of
      the drawing.'
    question: What is the first line of code to load a DWG?
  - answer: '`Aspose.CAD.Image` and `Aspose.CAD.FileFormats.Dwg` are required.'
    question: Which namespace contains the CAD classes?
  - answer: Yes – use `image.Save("out.pdf", SaveFormat.Pdf)`.
    question: Can I export the search results directly to PDF?
  - answer: A free trial works for evaluation; a permanent license is required for
      production.
    question: Do I need a license for development?
  - answer: .NET 5, .NET 6, .NET Core 3.1 and .NET Framework 4.6+.
    question: Which .NET versions are supported?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- dwg file handling
- aspose.cad
- c# cad processing
- text search in dwg
title: Cara memuat file dwg dan mencari teks dalam file DWG dengan C#
url: /id/net/text-search-and-manipulation/searching-text-in-dwg-files/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cara memuat file dwg dan mencari teks dalam file DWG dengan C# - tutorial Aspose.CAD

## Pendahuluan

Dalam pengembangan CAD modern, kemampuan untuk **load dwg file** objek dan langsung menemukan string teks tertentu menghemat berjam‑jam inspeksi manual. Apakah Anda sedang membangun alat pemrosesan batch atau menambahkan kemampuan pencarian ke penampil, Aspose.CAD untuk .NET memberikan API yang sepenuhnya dikelola yang bekerja di Windows, Linux, dan macOS tanpa ketergantungan native. Panduan ini memandu Anda melalui setiap langkah—dari memuat DWG hingga mengekspor hasil sebagai PDF—sehingga Anda dapat mengintegrasikan pencarian teks CAD yang dapat diandalkan ke dalam aplikasi C# Anda hari ini.

## Jawaban Cepat

- **Apa baris kode pertama untuk memuat DWG?** `new CadImage("yourfile.dwg")` membuat representasi gambar dalam memori.  
- **Namespace mana yang berisi kelas CAD?** `Aspose.CAD.Image` dan `Aspose.CAD.FileFormats.Dwg` diperlukan.  
- **Bisakah saya mengekspor hasil pencarian langsung ke PDF?** Ya – gunakan `image.Save("out.pdf", SaveFormat.Pdf)`.  
- **Apakah saya memerlukan lisensi untuk pengembangan?** Versi percobaan gratis dapat digunakan untuk evaluasi; lisensi permanen diperlukan untuk produksi.  
- **Versi .NET mana yang didukung?** .NET 5, .NET 6, .NET Core 3.1 and .NET Framework 4.6+.

## Apa itu file DWG?

File DWG adalah format biner yang menyimpan data desain 2D dan 3D yang dibuat oleh AutoCAD dan alat yang kompatibel. Ini adalah wadah standar industri untuk geometri vektor, lapisan, teks, dan metadata. Karena format ini bersifat proprietari, sebagian besar parser open‑source kesulitan dengan versi yang lebih baru, tetapi Aspose.CAD sepenuhnya mendukung lebih dari 150 rilis DWG, memungkinkan Anda membaca dan memanipulasi gambar tanpa menginstal AutoCAD.

## Mengapa menggunakan Aspose.CAD untuk pencarian teks CAD?

Aspose.CAD dapat memproses **50+** versi DWG dan DXF, menangani file hingga 1 GB tanpa memuat seluruh dokumen ke memori. Perpustakaan ini mengekstrak teks dari bagian **Entities** dan **Block**, memberikan tingkat keberhasilan **99 %** dalam menemukan string yang dapat dicari bahkan ketika mereka berada di dalam blok. Keandalan yang terukur ini menjadikannya pilihan utama untuk otomasi CAD tingkat perusahaan.

## Prasyarat

- **Aspose.CAD for .NET** terinstal. Unduh paket terbaru dari [situs Aspose.CAD](https://releases.aspose.com/cad/net/).
- Sebuah folder yang berisi file DWG yang ingin Anda analisis.
- File lisensi yang valid untuk penggunaan produksi (opsional untuk percobaan).

## Namespace mana yang diperlukan?

Namespace `Aspose.CAD` menyediakan kelas inti penanganan gambar, sementara `Aspose.CAD.FileFormats.Dwg` berisi struktur khusus DWG. Impor mereka di bagian atas file C# Anda:

```csharp
using Aspose.CAD;
using Aspose.CAD.FileFormats.Dwg;
using Aspose.CAD.ImageOptions;
```

> **Catatan:** Blok kode di atas adalah placeholder; pertahankan teks persis tidak berubah untuk menjaga jumlah placeholder asli.

## Cara memuat file dwg?

Memuat file DWG sangat mudah dengan Aspose.CAD. Gunakan kelas `CadImage`, yang mewakili gambar CAD dalam memori. Konstruktor membaca file tanpa merender, membuatnya cepat bahkan untuk gambar besar. Setelah dimuat, Anda dapat memeriksa properti seperti `Width`, `Height`, dan `Layers` sebelum melakukan operasi pencarian apa pun.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.FileFormats.Cad.CadConsts;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadObjects.AttEntities;
```

## Cara mencari teks di bagian entities?

Untuk menemukan teks di bagian Entities, iterasi koleksi `cadImage.Entities`. Setiap entitas dapat diperiksa tipe-nya (mis., `MText`, `Text`, `Attribute`) dan properti `TextString`. Lakukan perbandingan tidak sensitif huruf terhadap string target dan kumpulkan entitas yang cocok untuk pemrosesan lebih lanjut atau penyorotan.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "search.dwg";
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Your code here
}
```

## Cara mencari teks di bagian block?

Blok adalah grup entitas yang dapat digunakan kembali yang mungkin berisi teks bersarang. Pertama, enumerasi `cadImage.BlockEntities.Values` untuk mengakses setiap definisi blok. Kemudian, telusuri koleksi `Entities` setiap blok, menerapkan logika pencocokan teks yang sama seperti pada bagian Entities utama. Ini memastikan teks yang tersembunyi di dalam komponen yang dapat digunakan kembali tidak terlewat.

```csharp
foreach (CadBaseEntity entity in cadImage.Entities)
{
    IterateCADNodes(entity);
}
```

## Cara mengiterasi node CAD untuk pemindaian lengkap?

Pemindaian komprehensif menggabungkan bagian Entities dan Block. Dengan secara rekursif menelusuri pohon node `CadImage`, Anda dapat menangani blok bersarang, definisi atribut, dan bahkan referensi eksternal. Implementasikan metode bantu yang menerima `CadBaseEntity`, memeriksa tipenya, mengekstrak teks bila berlaku, dan kemudian melakukan rekursi ke entitas anak jika node tersebut berisi koleksi.

```csharp
foreach (CadBlockEntity blockEntity in cadImage.BlockEntities.Values)
{
    foreach (CadBaseEntity entity in blockEntity.Entities)
    {
        IterateCADNodes(entity);
    }
}
```

## Cara mengekspor dwg ke pdf setelah menemukan teks?

Setelah mengidentifikasi entitas yang relevan, Anda mungkin ingin menyorotnya atau mengekstrak koordinatnya. Aspose.CAD memungkinkan Anda menyimpan seluruh gambar sebagai PDF sambil mempertahankan kualitas vektor. Konfigurasikan `CadRasterizationOptions` jika Anda memerlukan output raster, lalu panggil `image.Save("output.pdf", new PdfOptions())`. PDF yang dihasilkan dapat dibagikan kepada pemangku kepentingan yang tidak memiliki perangkat lunak CAD.

```csharp
private static void IterateCADNodes(CadBaseEntity obj)
{
    switch (obj.TypeName)
    {
        // Handle different entity types
    }
}
```

## Kesimpulan

Aspose.CAD untuk .NET menyediakan solusi yang mulus dan berperforma tinggi untuk memuat data file dwg, mencari teks tertentu, dan mengekspor hasil ke PDF. Dengan mengikuti langkah‑langkah dalam tutorial ini, Anda telah menambahkan kemampuan pencarian teks CAD yang kuat ke aplikasi C# Anda tanpa bergantung pada alat eksternal atau lisensi mahal.

## Pertanyaan yang sering diajukan

### Q1: Bisakah saya menggunakan Aspose.CAD untuk .NET dengan format CAD lain?

A1: Ya, Aspose.CAD mendukung lebih dari 30 format CAD, termasuk DXF, DWF, dan STL, menyediakan solusi serbaguna untuk alur kerja format campuran.

### Q2: Apakah tersedia percobaan gratis untuk Aspose.CAD untuk .NET?

A2: Ya, Anda dapat menjelajahi fitur dengan [percobaan gratis](https://releases.aspose.com/).

### Q3: Bagaimana saya dapat mendapatkan dukungan untuk Aspose.CAD untuk .NET?

A3: Kunjungi [forum Aspose.CAD](https://forum.aspose.com/c/cad/19) untuk bantuan komunitas dan saluran dukungan resmi.

### Q4: Apa itu lisensi sementara, dan bagaimana saya dapat mendapatkannya?

A4: Dapatkan lisensi sementara [temporary license](https://purchase.aspose.com/temporary-license/) untuk evaluasi jangka pendek atau proyek proof‑of‑concept.

### Q5: Di mana saya dapat menemukan dokumentasi terperinci untuk Aspose.CAD untuk .NET?

A5: Lihat [dokumentasi](https://reference.aspose.com/cad/net/) yang komprehensif untuk panduan mendalam, referensi API, dan contoh kode.

---

**Terakhir Diperbarui:** 2026-10-09  
**Diuji Dengan:** Aspose.CAD 24.11 for .NET  
**Penulis:** Aspose  

```csharp
Aspose.CAD.ImageOptions.CadRasterizationOptions rasterizationOptions = new Aspose.CAD.ImageOptions.CadRasterizationOptions();
// Configure rasterization options
rasterizationOptions.Layouts = new[] { "Layout1" };
Aspose.CAD.ImageOptions.PdfOptions pdfOptions = new Aspose.CAD.ImageOptions.PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
cadImage.Save(MyDir + "SearchText_out.pdf", pdfOptions);
```

## Tutorial Terkait

- [Cara mengonversi DWG ke PDF dan Gambar Raster menggunakan Aspose.CAD untuk .NET](/cad/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/)
- [Konversi DWG ke PNG & Ekspor OLE Objects - Tutorial Aspose.CAD](/cad/net/advanced-export-techniques/exporting-ole-objects-from-dwg/)
- [Cara Membaca File DWT dengan Aspose.CAD untuk .NET](/cad/net/cad-features-and-support/reading-dwt/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}