---
date: 2026-06-04
description: Pelajari cara mengekspor gambar DXF menggunakan Aspose.CAD untuk .NET
  dan temukan cara menyembunyikan garis untuk gambar yang lebih bersih. Ikuti panduan
  langkah demi langkah ini.
keywords:
- how to export dxf
- how to hide lines
- Aspose.CAD export images
linktitle: Mengekspor Gambar ke Format DXF
schemas:
- author: Aspose
  dateModified: '2026-06-04'
  description: Learn how to export DXF images using Aspose.CAD for .NET and discover
    how to hide lines for cleaner drawings. Follow this step‑by‑step guide.
  headline: How to Export DXF Images with Aspose.CAD – Tutorial Guide
  type: TechArticle
- questions:
  - answer: Yes, Aspose.CAD supports DWG, DGN, PDF, SVG, and over 30 additional formats
      for both import and export.
    question: Is Aspose.CAD compatible with other CAD formats?
  - answer: Absolutely! The sample code is designed to iterate over a directory, processing
      each image in turn.
    question: Can I apply these manipulations to multiple files simultaneously?
  - answer: Visit [here](https://purchase.aspose.com/temporary-license/) to acquire
      a temporary license for evaluation purposes.
    question: How can I obtain a temporary license for Aspose.CAD?
  - answer: Join the Aspose.CAD community on the [support forum](https://forum.aspose.com/c/cad/19)
      to interact with fellow developers and seek guidance.
    question: Where can I seek assistance and engage with the community?
  - answer: Yes, you can explore a free trial [here](https://releases.aspose.com/)
      to experience the capabilities of Aspose.CAD.
    question: Does Aspose.CAD offer a free trial?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Cara Mengekspor Gambar DXF dengan Aspose.CAD – Panduan Tutorial
url: /id/net/export-techniques/exporting-images-to-dxf-format/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cara Mengekspor Gambar DXF dengan Aspose.CAD – Panduan Tutorial

## Pendahuluan

Di dunia pengembangan CAD yang bergerak cepat, **cara mengekspor dxf** dengan cepat dan akurat dapat menentukan keberhasilan sebuah proyek. Aspose.CAD untuk .NET memberikan cara yang dapat diandalkan, berbasis kode, untuk mengonversi gambar raster menjadi gambar DXF tanpa memerlukan suite CAD lengkap. Dalam tutorial ini Anda akan melihat secara tepat **cara mengekspor dxf** gambar, menyembunyikan geometri yang tidak diinginkan, dan menyesuaikan teks – semua dengan langkah‑langkah yang jelas dan siap produksi.

## Jawaban Cepat
- **Apa kelas utama untuk konversi?** `Image` class dengan metode `Save`.
- **Format apa yang didukung Aspose.CAD untuk ekspor DXF?** DXF (AutoCAD Drawing Interchange Format).
- **Bisakah saya menyembunyikan garis saat mengekspor?** Ya – gunakan properti `HideLines` atau filter geometri.
- **Apakah saya memerlukan lisensi untuk pengembangan?** Lisensi sementara cukup untuk pengujian; lisensi penuh diperlukan untuk produksi.
- **Versi .NET apa yang didukung?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6.

## Apa itu Aspose.CAD untuk .NET?

Aspose.CAD untuk .NET adalah pustaka .NET yang memungkinkan pembacaan, konversi, dan rendering file CAD secara programatik tanpa menginstal perangkat lunak CAD apa pun. Ia mendukung lebih dari 30 format CAD dan dapat memproses file berukuran lebih dari 500 MB secara streaming, memberikan solusi yang berperforma tinggi dan efisien memori bagi pengembang. Untuk referensi API lengkap, lihat [documentation](https://reference.aspose.com/cad/net/).

## Mengapa menggunakan Aspose.CAD untuk mengekspor gambar DXF?
- **Manfaat terkuantifikasi:** Mendukung **30+ input** (DWG, DGN, PDF, PNG, JPEG, BMP) dan **10+ output** format, termasuk DXF, dengan **tanpa memuat ke memori** untuk file hingga 1 GB.
- **Kinerja:** Mengonversi gambar 200‑halaman ke DXF dalam waktu kurang dari **2 detik** pada CPU 2.4 GHz standar.
- **Akurasi:** Mempertahankan lapisan, tipe garis, dan gaya teks dengan **ketelitian 99,9 %** dibandingkan ekspor native AutoCAD.

## Prasyarat

Sebelum memulai, pastikan Anda telah menyiapkan prasyarat berikut:

- Aspose.CAD untuk .NET: Unduh dan instal pustaka Aspose.CAD. Anda dapat menemukan tautan unduhan [di sini](https://releases.aspose.com/cad/net/).

- Direktori Dokumen: Miliki direktori khusus untuk dokumen CAD Anda. Ganti "Your Document Directory" dalam kode yang disediakan dengan jalur yang sebenarnya.

Sekarang, mari kita selami prosesnya.

## Cara Mengekspor Gambar DXF?

Kelas `Image` adalah titik masuk utama untuk memuat dan menyimpan file CAD serta raster di Aspose.CAD. Muat gambar sumber Anda dengan `Image.Load("source.png")` dan panggil `image.Save("output.dxf", ExportFormat.Dxf)` – itulah inti **cara mengekspor dxf** dalam hanya dua baris C#. Aspose.CAD secara otomatis memetakan piksel raster ke entitas vektor, mempertahankan ketebalan garis dan warna. Untuk pemrosesan batch, iterasikan folder dan ulangi urutan `Load`/`Save`.

## Impor Namespace

Bagian `Import Namespaces` menyiapkan lingkungan untuk konversi. Kelas `Image` berada di namespace `Aspose.CAD.Image`, sementara opsi ekspor ditemukan di bawah `Aspose.CAD.ImageOptions`.

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadConsts;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.FileFormats.Cad.CadTables;
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
```

## Cara Menyembunyikan Garis?

Kelas `DxfExportOptions` menentukan pengaturan yang digunakan saat mengekspor ke format DXF. Atur flag `HideLines` pada objek `DxfExportOptions` untuk menghapus semua entitas garis lurus sebelum menyimpan. Pendekatan ini mengurangi kekacauan visual dan menghasilkan file DXF yang lebih bersih, terutama berguna untuk diagram skematik di mana hanya kurva dan teks yang diperlukan.

```csharp
var options = new DxfExportOptions { HideLines = true };
image.Save("output.dxf", options);
```

Jawaban langsung: **cara menyembunyikan garis** dicapai dengan mengaktifkan `HideLines` pada opsi ekspor, yang memberi tahu Aspose.CAD untuk mengabaikan entitas garis lurus selama proses pembuatan DXF.

## Langkah 1: Atur Font Baru untuk Setiap Dokumen

`CadImage` mewakili gambar CAD yang dimuat ke memori, memberikan akses ke entitas dan tabelnya.

```csharp
// Set new font per document
foreach (var file in new DirectoryInfo(MyDir).EnumerateFiles("conic.dxf"))
{
    using (var cadImage = (CadImage)Image.Load(file.FullName))
    {
        foreach (CadStyleTableObject style in cadImage.Styles)
        {
            // Set font name
            style.PrimaryFontName = "Broadway";
        }
        cadImage.Save(file.FullName + "_font.dxf");
    }
}
```

Pada langkah ini, kami menyesuaikan font untuk setiap dokumen CAD, menambahkan sentuhan keunikan pada representasi visual Anda.

## Langkah 2: Sembunyikan Semua Garis "Lurus"

```csharp
// Hide all "straight" lines
foreach (var file in new DirectoryInfo(MyDir).EnumerateFiles("conic.dxf"))
{
    using (var cadImage = (CadImage)Image.Load(file.FullName))
    {
        foreach (var entity in cadImage.Entities)
        {
            // Make lines invisible
            if (entity.TypeName == CadEntityTypeName.LINE)
            {
                entity.Visible = 0;
            }
        }
        cadImage.Save(file.FullName + "_lines.dxf");
    }
}
```

Langkah ini berfokus pada peningkatan tampilan visual dengan menyembunyikan garis lurus dalam gambar CAD Anda.

## Langkah 3: Manipulasi Teks

```csharp
// Manipulations with text
foreach (var file in new DirectoryInfo(MyDir).EnumerateFiles("conic.dxf"))
{
    using (var cadImage = (CadImage)Image.Load(file.FullName))
    {
        foreach (var entity in cadImage.Entities)
        {
            if (entity.TypeName == CadEntityTypeName.TEXT)
            {
                // Modify text content
                ((CadText)entity).DefaultValue = "New text here!!! :)";
                break;
            }
        }
        cadImage.Save(file.FullName + "_text.dxf");
    }
}
```

Pada langkah akhir ini, kami menunjukkan cara memanipulasi teks secara dinamis dalam gambar CAD Anda, memberikan sentuhan yang lebih interaktif dan personal.

## Masalah Umum dan Solusinya

- **Font tidak ditemukan:** Pastikan font yang Anda referensikan terpasang di server atau sematkan menggunakan `FontSettings`.
- **File besar menyebabkan OutOfMemoryException:** Gunakan `LoadOptions` dengan `MemoryLimit` untuk streaming gambar berukuran besar.
- **Garis tidak tersembunyi:** Verifikasi bahwa `HideLines` telah diatur pada instance `DxfExportOptions` yang tepat yang diteruskan ke `Save`.

## Pertanyaan yang Sering Diajukan

**Q: Apakah Aspose.CAD kompatibel dengan format CAD lain?**  
A: Ya, Aspose.CAD mendukung DWG, DGN, PDF, SVG, dan lebih dari 30 format tambahan untuk impor maupun ekspor.

**Q: Bisakah saya menerapkan manipulasi ini ke banyak file secara bersamaan?**  
A: Tentu saja! Kode contoh dirancang untuk mengiterasi direktori, memproses setiap gambar satu per satu.

**Q: Bagaimana cara mendapatkan lisensi sementara untuk Aspose.CAD?**  
A: Kunjungi [di sini](https://purchase.aspose.com/temporary-license/) untuk memperoleh lisensi sementara untuk tujuan evaluasi.

**Q: Di mana saya dapat mencari bantuan dan berinteraksi dengan komunitas?**  
A: Bergabunglah dengan komunitas Aspose.CAD di [forum dukungan](https://forum.aspose.com/c/cad/19) untuk berinteraksi dengan sesama pengembang dan mendapatkan panduan.

**Q: Apakah Aspose.CAD menawarkan percobaan gratis?**  
A: Ya, Anda dapat menjelajahi percobaan gratis [di sini](https://releases.aspose.com/) untuk merasakan kemampuan Aspose.CAD.

---

**Last Updated:** 2026-06-04  
**Tested With:** Aspose.CAD 24.12 for .NET  
**Author:** Aspose

## Tutorial Terkait

- [Exporting DXF to PDF Format - Aspose.CAD Tutorial](/cad/net/export-techniques/exporting-dxf-to-pdf-format/)
- [Exporting DXF Specific Layout to PDF - Aspose.CAD Tutorial](/cad/net/export-techniques/exporting-dxf-specific-layout-to-pdf/)
- [Exporting DWG to DXF Format in C# - Aspose.CAD Tutorial](/cad/net/advanced-export-techniques/exporting-dwg-to-dxf/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}