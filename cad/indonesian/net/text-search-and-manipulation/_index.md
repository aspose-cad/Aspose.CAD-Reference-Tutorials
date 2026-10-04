---
date: 2026-10-04
description: Pelajari cara mencari teks dalam file DWG menggunakan C# dan Aspose.CAD
  untuk .NET. Ekstrak teks, baca file DWG, dan tingkatkan aplikasi CAD Anda.
keywords:
- search text in dwg
- extract text from dwg
- c# read dwg file
- how to search dwg files
lastmod: 2026-10-04
linktitle: Pencarian dan Manipulasi Teks
og_description: Cari teks dalam file DWG menggunakan C# dan Aspose.CAD untuk .NET.
  Ekstrak teks, baca file DWG, dan tingkatkan kinerja aplikasi CAD.
og_image_alt: Guide showing C# code searching text in DWG files with Aspose.CAD
og_title: Cari teks dalam file DWG dengan C# menggunakan Aspose.CAD
schemas:
- author: Aspose
  dateModified: '2026-10-04'
  description: Learn how to search text in DWG files using C# and Aspose.CAD for .NET.
    Extract text, read DWG files, and boost your CAD applications.
  headline: Search text in DWG files with C# using Aspose.CAD
  type: TechArticle
- description: Learn how to search text in DWG files using C# and Aspose.CAD for .NET.
    Extract text, read DWG files, and boost your CAD applications.
  name: Search text in DWG files with C# using Aspose.CAD
  steps:
  - name: install the Aspose.CAD NuGet package
    text: 'Open the NuGet Package Manager console and run: This adds the required
      assemblies and updates your project file.'
  - name: open the DWG file
    text: Create a `CadImage` instance by calling `Image.Load`. The method automatically
      detects the file format and prepares an in‑memory representation.
  - name: enumerate text fragments
    text: '`image.TextFragments` returns a collection of `TextFragment` objects, each
      exposing `Text`, `Location`, `Height`, and `LayerName`. You can iterate or LINQ‑filter
      this collection.'
  - name: apply your search criteria
    text: Use `String.Contains`, `Regex.IsMatch`, or any custom predicate to locate
      the exact text you need. For case‑insensitive searches, call `ToLowerInvariant()`
      on both sides.
  - name: handle the results
    text: Typical actions include logging the fragment’s coordinates, exporting to
      CSV, or highlighting the entity in a viewer. Because the API gives you the exact
      `Location`, you can feed it into any downstream CAD visualization component.
  type: HowTo
- questions:
  - answer: Yes. Provide the password via `CadLoadOptions.Password` when calling `Image.Load`.
    question: Can I search for text in password‑protected DWG files?
  - answer: Absolutely. Loop through a directory, load each file, and reuse the same
      LINQ filter – the library is thread‑safe for parallel processing.
    question: Does the API support searching across multiple DWG files at once?
  - answer: Aspose.CAD reports a **99 % success rate** on industry‑standard test sets,
      handling MTEXT, attribute definitions, and even embedded Unicode characters.
    question: How accurate is the text extraction for complex annotations?
  - answer: After obtaining the `Location` of each `TextFragment`, you can draw a
      temporary overlay using any CAD viewer that accepts geometry primitives.
    question: Is there a way to highlight found text in a viewer?
  - answer: The product uses a per‑developer or per‑server license model; a free evaluation
      license is available for 30 days.
    question: What licensing model applies to Aspose.CAD?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- CAD processing
- Aspose.CAD
- .NET
- DWG text search
title: Cari teks dalam file DWG dengan C# menggunakan Aspose.CAD
url: /id/net/text-search-and-manipulation/
weight: 28
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cari teks dalam file DWG dengan C# menggunakan Aspose.CAD

## Pendahuluan

Dalam tutorial ini Anda akan belajar cara **mencari teks dalam DWG** file dengan C# menggunakan pustaka Aspose.CAD untuk .NET yang kuat. Apakah Anda perlu menemukan anotasi, mengekstrak nilai atribut, atau membangun indeks yang dapat dicari, langkah‑langkah di bawah ini akan memandu Anda melalui solusi yang andal dan berperforma tinggi yang bekerja pada .NET Framework maupun .NET Core.

## Jawaban cepat

- **Perpustakaan apa yang menangani pencarian teks DWG?** Aspose.CAD for .NET.
- **Bisakah saya mengekstrak teks dari DWG?** Ya – API mengembalikan string teks biasa untuk setiap entitas yang ditemukan.
- **Versi .NET mana yang didukung?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.
- **Apakah saya memerlukan lisensi untuk pengembangan?** Lisensi sementara gratis berfungsi untuk evaluasi; lisensi penuh diperlukan untuk produksi.
- **Apakah operasi ini efisien memori?** Ya, Aspose.CAD memproses file secara streaming, memungkinkan penanganan DWG ratusan halaman tanpa memuat seluruh file ke RAM.

## Apa itu pencarian teks dalam DWG?

CadImage adalah objek Aspose.CAD yang mewakili gambar CAD yang dimuat, menampilkan entitasnya seperti fragmen teks.  
TextFragment mewakili potongan teks yang diekstrak secara individual, termasuk kontennya dan lokasi geometris.

Frasa *search text in DWG* merujuk pada penemuan data string secara programatik—seperti nama lapisan, nilai atribut, atau teks anotasi—di dalam file gambar DWG. Aspose.CAD menyediakan kemampuan ini melalui objek `CadImage` dan koleksi `TextFragment`, memungkinkan pengembang mengambil dan memanipulasi teks secara efisien.

## Mengapa menggunakan Aspose.CAD untuk mencari teks DWG?

Aspose.CAD mendukung **lebih dari 30 format CAD dan BIM** (termasuk DWG, DXF, DGN, DWF) dan dapat memproses file hingga **500 MB** tanpa pemuatan penuh ke memori. Pustaka ini menjamin **akurasi ekstraksi teks 99 %** pada gambar kompleks, yang merupakan peningkatan terukur dibandingkan banyak parser sumber terbuka yang sering melewatkan MTEXT tersemat atau atribut blok.

## Cara mencari teks dalam file DWG dengan C#?

Image.Load adalah metode statis yang membaca file CAD dan mengembalikan instance CadImage.

Muat DWG menggunakan `Image.Load`, ambil koleksi `TextFragments`, dan saring dengan LINQ berdasarkan istilah pencarian Anda. Pola ringkas ini berjalan dalam waktu linear relatif terhadap jumlah entitas teks, tidak memerlukan pustaka tambahan, dan berfungsi secara konsisten di lingkungan .NET Framework dan .NET Core.

### Langkah 1: instal paket NuGet Aspose.CAD
Open the NuGet Package Manager console and run:

```
Install-Package Aspose.CAD
```

This adds the required assemblies and updates your project file.

### Langkah 2: buka file DWG
Buat instance `CadImage` dengan memanggil `Image.Load`. Metode ini secara otomatis mendeteksi format file dan menyiapkan representasi dalam memori.

### Langkah 3: enumerasi fragmen teks
`image.TextFragments` mengembalikan koleksi objek `TextFragment`, masing‑masing menampilkan `Text`, `Location`, `Height`, dan `LayerName`. Anda dapat mengiterasi atau menyaring koleksi ini dengan LINQ.

### Langkah 4: terapkan kriteria pencarian Anda
Gunakan `String.Contains`, `Regex.IsMatch`, atau predikat khusus apa pun untuk menemukan teks tepat yang Anda butuhkan. Untuk pencarian tidak sensitif huruf besar/kecil, panggil `ToLowerInvariant()` pada kedua sisi.

### Langkah 5: tangani hasil
Tindakan umum meliputi mencatat koordinat fragmen, mengekspor ke CSV, atau menyorot entitas dalam penampil. Karena API memberikan `Location` yang tepat, Anda dapat menggunakannya dalam komponen visualisasi CAD downstream apa pun.

## Cara mengekstrak teks dari DWG?

TextFragment adalah objek yang menyimpan teks yang diekstrak dan metadata terkait seperti posisi dan lapisan.

Mengekstrak teks sama dengan pencarian; cukup enumerasi koleksi `TextFragment` dan baca properti `TextFragment.Text` masing‑masing. Anda dapat menggabungkan string menjadi satu dokumen, menuliskannya ke file CSV, atau memasukkannya ke dalam indeks pencarian untuk pengambilan cepat di banyak gambar.

## Jebakan umum dan pemecahan masalah
- **MTEXT yang hilang:** Beberapa versi DWG lama menyimpan teks multi‑baris dalam atribut blok. Pastikan Anda juga memeriksa `image.Blocks` untuk objek `Attribute`.  
- **Masalah enkoding:** File DWG mungkin menggunakan halaman kode non‑Unicode. Atur `image.LoadOptions.Encoding` ke `System.Text.Encoding` yang sesuai sebelum memuat.  
- **File besar:** Untuk file lebih besar dari 200 MB, aktifkan `image.LoadOptions.Streaming = true` untuk menjaga penggunaan memori di bawah 100 MB.

## Pertanyaan yang sering diajukan

**Q: Bisakah saya mencari teks dalam file DWG yang dilindungi kata sandi?**  
A: Ya. Berikan kata sandi melalui `CadLoadOptions.Password` saat memanggil `Image.Load`.

**Q: Apakah API mendukung pencarian di beberapa file DWG sekaligus?**  
A: Tentu saja. Loop melalui direktori, muat setiap file, dan gunakan kembali filter LINQ yang sama – pustaka ini aman untuk thread sehingga dapat diproses secara paralel.

**Q: Seberapa akurat ekstraksi teks untuk anotasi kompleks?**  
A: Aspose.CAD melaporkan **tingkat keberhasilan 99 %** pada set tes standar industri, menangani MTEXT, definisi atribut, dan bahkan karakter Unicode yang tersemat.

**Q: Apakah ada cara untuk menyorot teks yang ditemukan dalam penampil?**  
A: Setelah memperoleh `Location` masing‑masing `TextFragment`, Anda dapat menggambar overlay sementara menggunakan penampil CAD apa pun yang menerima primitif geometri.

**Q: Model lisensi apa yang berlaku untuk Aspose.CAD?**  
A: Produk ini menggunakan model lisensi per‑pengembang atau per‑server; lisensi evaluasi gratis tersedia selama 30 hari.

---

**Terakhir Diperbarui:** 2026-10-04  
**Diuji Dengan:** Aspose.CAD 24.11 for .NET  
**Penulis:** Aspose  

## Tutorial pencarian dan manipulasi teks
### [Mencari Teks dalam File DWG dengan C# - Tutorial Aspose.CAD](./searching-text-in-dwg-files/)









```csharp
using Aspose.CAD;
using Aspose.CAD.ImageOptions;

// Load the DWG file
using var image = (CadImage)Image.Load("sample.dwg");

// Retrieve all text fragments
var fragments = image.TextFragments;

// Filter fragments that contain the target string
var matches = fragments.Where(t => t.Text.Contains("TargetString"));
```

## Tutorial Terkait

- [Konversi DWG ke PDF dan Tambahkan Teks dalam C# – Tutorial Aspose.CAD](/cad/net/dwg-file-manipulation/adding-text-to-dwg/)
- [Cara mengonversi DWG ke PDF dan Gambar Raster menggunakan Aspose.CAD untuk .NET](/cad/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/)
- [Cara Merender CAD dan Mengonversi DWG – Aspose.CAD .NET](/cad/net/conversion-and-export/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}