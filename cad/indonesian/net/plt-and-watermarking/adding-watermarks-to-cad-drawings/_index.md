---
date: 2026-09-29
description: Pelajari cara menambahkan watermark Aspose CAD ke gambar Anda menggunakan
  Aspose.CAD for .NET. Ikuti panduan langkah demi langkah ini untuk mempersonalisasi
  dan melindungi file CAD Anda.
keywords:
- aspose cad watermark
- convert dwg to pdf
- generate pdf with watermark
- how to watermark cad
- add watermark to dwg
lastmod: 2026-09-29
linktitle: Menambahkan Watermark ke Gambar CAD
og_description: Pelajari cara menambahkan watermark Aspose CAD ke gambar Anda menggunakan
  Aspose.CAD for .NET. Panduan langkah demi langkah ini mencakup prasyarat, memuat
  file, menerapkan watermark MTEXT atau teks, dan mengekspor ke PDF.
og_image_alt: Screenshot of Aspose.CAD watermarking tutorial for .NET
og_title: Tambahkan watermark Aspose CAD ke gambar Anda – panduan .NET cepat
schemas:
- author: Aspose
  dateModified: '2026-09-29'
  description: Learn how to add an Aspose CAD watermark to your drawings using Aspose.CAD
    for .NET. Follow this step‑by‑step guide to personalize and protect your CAD files.
  headline: How to add an Aspose CAD watermark to drawings
  type: TechArticle
- questions:
  - answer: Yes, you can set text, font family, size, color, rotation angle, and opacity
      directly on the MTEXT or Text entity.
    question: Can I customize the appearance of the watermark?
  - answer: Aspose.CAD supports more than 30 input and output formats, including DWG,
      DXF, DWF, DGN, and IFC.
    question: Is Aspose.CAD compatible with different CAD file formats?
  - answer: Absolutely. Call the watermark‑adding method multiple times with different
      positions or content.
    question: Can I add multiple watermarks to a single CAD drawing?
  - answer: Yes, you can explore Aspose.CAD's features with a free trial. Download
      **Aspose.CAD** [here](https://releases.aspose.com/).
    question: Does Aspose.CAD offer a free trial?
  - answer: For any queries or assistance, visit the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19).
    question: Where can I find support for Aspose.CAD?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- aspose cad
- cad watermark
- .net drawing
- dwg to pdf
- cad automation
title: Cara menambahkan watermark Aspose CAD ke gambar
url: /id/net/plt-and-watermarking/adding-watermarks-to-cad-drawings/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cara menambahkan watermark Aspose CAD ke gambar

## Pendahuluan

Menambahkan **aspose cad watermark** memungkinkan Anda melindungi hak kekayaan intelektual dan memberi merek pada setiap gambar yang Anda bagikan. Dengan Aspose.CAD untuk .NET Anda dapat menyisipkan watermark langsung ke dalam format DWG, DXF, atau format CAD lain yang didukung tanpa memerlukan perangkat lunak desain asli. Dalam tutorial ini Anda akan melihat mengapa watermark penting, format apa saja yang didukung, dan cara menerapkannya langkah demi langkah.

## Jawaban Cepat
- **Library apa yang saya butuhkan?** Aspose.CAD for .NET (download from the official site).  
- **Jenis file apa yang dapat saya beri watermark?** Over 30 CAD/BIM formats, including DWG, DXF, DWF, and DGN.  
- **Bisakah saya mengekspor hasilnya sebagai PDF?** Yes – the same API lets you save the watermarked drawing to PDF in one line.  
- **Apakah saya memerlukan lisensi untuk pengembangan?** A free trial works for testing; a commercial license is required for production.  
- **Apakah kode kompatibel dengan .NET 6?** Absolutely – Aspose.CAD supports .NET Framework 4.5+, .NET Core 3.1+, .NET 5+, and .NET 6+.

## Apa itu watermark Aspose CAD?
Sebuah **Aspose CAD watermark** adalah entitas teks atau MTEXT yang disisipkan Aspose.CAD ke dalam ruang model gambar CAD, ditampilkan sebagai lapisan semi‑transparan yang menyertai file. Ini melindungi gambar sambil tetap dapat diedit di penampil CAD standar.

## Mengapa menggunakan Aspose.CAD untuk watermark?
Aspose.CAD dapat memproses **30+** format CAD dan BIM serta menangani file dengan **hingga 1.000 halaman** tanpa memuat seluruh dokumen ke dalam memori. Kemampuan terukur ini berarti Anda dapat memproses secara batch arsip rekayasa besar secara efisien, mengurangi penggunaan memori server hingga **70 %** dibandingkan dengan pemuatan file per file secara naïf.

## Prasyarat

Sebelum Anda memulai, pastikan Anda memiliki:

- Aspose.CAD for .NET terinstal – Anda dapat mengunduh **Aspose.CAD for .NET** [di sini](https://releases.aspose.com/cad/net/).
- Folder yang berisi gambar CAD yang ingin Anda beri watermark.
- Lisensi Aspose yang valid (opsional untuk percobaan).

Sekarang, mari kita jalani proses penambahan watermark.

## Bagaimana cara menambahkan watermark ke gambar CAD?

Anda cukup memuat file CAD, membuat entitas watermark (MTEXT atau Text), menambahkannya ke ruang model, lalu menyimpan gambar dalam format yang diinginkan seperti PDF. Pendekatan ini bekerja untuk semua format CAD yang didukung dan dapat diprogram untuk pemrosesan batch.

## Impor namespace

`using Aspose.CAD;`  
`using Aspose.CAD.ImageOptions;`  
`using Aspose.CAD.FileFormats.Cad;`  

## Langkah 1: Memuat gambar CAD

Kelas `CadImage` mewakili gambar CAD yang dimuat ke dalam memori dan memberikan akses ke entitas‑entitasnya.  
```markdown
```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```
```

## Langkah 2: Menambahkan watermark sebagai MTEXT

`CadMText` adalah entitas yang menyimpan teks multi‑baris dengan pemformatan, cocok untuk pesan watermark.  
```markdown
```csharp
// The path to the documents directory.
string MyDir = "Your Document Directory";
using (CadImage cadImage = (CadImage)Image.Load(MyDir + "Drawing11.dwg")) {
```
```

## Langkah 3: Atau menambahkan watermark sebagai teks biasa

`CadText` mewakili entitas teks satu‑baris yang dapat ditempatkan di ruang model gambar.  
```markdown
```csharp
// Add new MTEXT
CadMText watermark = new CadMText();
watermark.Text = "Watermark message";
watermark.InitialTextHeight = 40;
watermark.InsertionPoint = new Cad3DPoint(300, 40);
watermark.LayerName = "0";
cadImage.BlockEntities["*Model_Space"].AddEntity(watermark);
```
```

## Langkah 4: Mengekspor ke PDF

`CadRasterizationOptions` menentukan cara rasterisasi gambar CAD, sementara `PdfOptions` menentukan pengaturan output PDF.  
```markdown
```csharp
// Alternatively, add a simpler entity like Text
CadText text = new CadText();
text.DefaultValue = "Watermark text";
text.TextHeight = 40;
text.FirstAlignment = new Cad3DPoint(300, 40);
text.LayerName = "0";
cadImage.BlockEntities["*Model_Space"].AddEntity(text);
```
```

Ulangi langkah‑langkah ini untuk setiap gambar dalam koleksi Anda, dan Anda akan menghasilkan file CAD ber‑watermark profesional yang siap didistribusikan.

## Masalah umum dan solusi

- **Watermark tidak terlihat setelah diekspor** – Pastikan properti `Opacity` dari entitas MTEXT atau Text diatur antara 0.3 dan 0.7; nilai di luar rentang ini dapat menghasilkan tampilan sepenuhnya tidak tembus atau tidak terlihat.  
- **File besar menyebabkan lonjakan memori** – Gunakan `Image.Load` dengan parameter `LoadOptions` untuk mengaktifkan streaming, yang menjaga penggunaan memori tetap rendah.  
- **Rendering font tidak tepat** – Instal font TrueType yang sama di server seperti yang digunakan saat gambar dibuat, atau sematkan font fallback melalui `MText.Font`.

## Pertanyaan yang sering diajukan

**Q: Bisakah saya menyesuaikan tampilan watermark?**  
A: Ya, Anda dapat mengatur teks, keluarga font, ukuran, warna, sudut rotasi, dan opacity langsung pada entitas MTEXT atau Text.

**Q: Apakah Aspose.CAD kompatibel dengan berbagai format file CAD?**  
A: Aspose.CAD mendukung lebih dari 30 format input dan output, termasuk DWG, DXF, DWF, DGN, dan IFC.

**Q: Bisakah saya menambahkan beberapa watermark ke satu gambar CAD?**  
A: Tentu saja. Panggil metode penambahan watermark beberapa kali dengan posisi atau konten yang berbeda.

**Q: Apakah Aspose.CAD menawarkan percobaan gratis?**  
A: Ya, Anda dapat menjelajahi fitur Aspose.CAD dengan percobaan gratis. Unduh **Aspose.CAD** [di sini](https://releases.aspose.com/).

**Q: Di mana saya dapat menemukan dukungan untuk Aspose.CAD?**  
A: Untuk pertanyaan atau bantuan, kunjungi [forum Aspose.CAD](https://forum.aspose.com/c/cad/19).

---

**Terakhir Diperbarui:** 2026-09-29  
**Diuji Dengan:** Aspose.CAD 24.11 for .NET  
**Penulis:** Aspose  








```csharp
// Export the CAD drawing with watermark to PDF
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
rasterizationOptions.Layouts = new[] { "Model" };
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
cadImage.Save(MyDir + "AddWatermark_out.pdf", pdfOptions);
```

## Tutorial Terkait

- [Konversi DWG ke PDF dan Tambahkan Teks dalam C# – Tutorial Aspose.CAD](/cad/net/dwg-file-manipulation/adding-text-to-dwg/)
- [Cara Mengonversi dan Mengekspor Gambar CAD ke PDF dengan Aspose.CAD untuk .NET – Tutorial](/cad/net/advanced-export-techniques/exporting-cad-drawings-to-pdf/)
- [Cara Mengonversi DWG ke PDF dengan Dukungan Mesh Menggunakan Aspose.CAD untuk .NET](/cad/net/cad-features-and-support/mesh-support/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}