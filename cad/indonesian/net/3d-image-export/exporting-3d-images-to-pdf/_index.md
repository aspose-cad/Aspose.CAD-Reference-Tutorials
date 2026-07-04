---
date: 2026-07-04
description: Pelajari cara mengatur ukuran halaman PDF dan mengekspor PDF dari gambar
  CAD 3D menggunakan Aspose.CAD untuk .NET – panduan langkah demi langkah untuk mengonversi
  DWG ke PDF dan menyimpan CAD sebagai PDF.
keywords:
- set pdf page size
- export pdf from cad
- convert dwg to pdf
- save cad as pdf
- cad to pdf tutorial
linktitle: Mengekspor Gambar 3D ke PDF
schemas:
- author: Aspose
  dateModified: '2026-07-04'
  description: Learn how to set PDF page size and export PDF from 3D CAD images using
    Aspose.CAD for .NET – a step‑by‑step guide to convert DWG to PDF and save CAD
    as PDF.
  headline: Set PDF page size – Export 3D Images to PDF with Aspose.CAD
  type: TechArticle
- description: Learn how to set PDF page size and export PDF from 3D CAD images using
    Aspose.CAD for .NET – a step‑by‑step guide to convert DWG to PDF and save CAD
    as PDF.
  name: Set PDF page size – Export 3D Images to PDF with Aspose.CAD
  steps:
  - name: Load the CAD Image
    text: '`Image` class represents a CAD drawing loaded into memory, ready for rasterization.'
  - name: Configure Rasterization Options (Save CAD as PDF)
    text: '`RasterizationOptions` class defines how the CAD data is rasterized, including
      page size, DPI, and whether 3‑D entities are rendered.'
  - name: Set PDF Options (Create PDF from CAD)
    text: '`PdfOptions` class holds the output format settings and links the rasterization
      options to PDF generation.'
  - name: Save as PDF (Generate PDF from 3D Model)
    text: '`Save` method on the `Image` object writes the rasterized content to the
      specified PDF file, producing a ready‑to‑share document.'
  type: HowTo
- questions:
  - answer: Yes, Aspose.CAD supports more than 50 input and output formats, including
      DWG, DXF, DGN, STL, and IFC, ensuring flexibility for any project.
    question: Is Aspose.CAD compatible with all CAD file formats?
  - answer: Absolutely. Set `PageWidth` and `PageHeight` in `RasterizationOptions`
      to any size in points, inches, or millimetres before calling `Save`.
    question: Can I customize the page dimensions when exporting to PDF?
  - answer: Yes, you can obtain temporary licenses for Aspose.CAD by visiting [Temporary
      License](https://purchase.aspose.com/temporary-license/).
    question: Are temporary licenses available for Aspose.CAD?
  - answer: Head to the [Aspose.CAD Forum](https://forum.aspose.com/c/cad/19) for
      expert help and peer‑to‑peer advice.
    question: Where can I find additional support or community discussions?
  - answer: Yes, you can explore the features of Aspose.CAD by accessing the [free
      trial](https://releases.aspose.com/).
    question: Is there a free trial version of Aspose.CAD?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Atur ukuran halaman PDF – Ekspor Gambar 3D ke PDF dengan Aspose.CAD
url: /id/net/3d-image-export/exporting-3d-images-to-pdf/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Mengekspor Gambar 3D ke PDF - Tutorial Aspose.CAD

## Pendahuluan

Jika Anda perlu **mengatur ukuran halaman PDF** saat mengonversi gambar CAD 3‑D ke PDF, Anda berada di tempat yang tepat. Tutorial ini menunjukkan, langkah demi langkah, cara memuat file CAD, mengonfigurasi opsi rasterisasi—termasuk dimensi halaman khusus—dan menghasilkan PDF berkualitas tinggi menggunakan Aspose.CAD untuk .NET. Pada akhir tutorial Anda akan dapat **mengekspor PDF dari CAD**, **menyimpan CAD sebagai PDF**, dan mengontrol setiap detail tata letak tanpa menginstal AutoCAD.

## Jawaban Cepat
- **Apa arti “mengekspor PDF dari CAD”?** Ini mengonversi gambar CAD (DWG, DXF, DGN, dll.) menjadi PDF yang dapat dibuka di perangkat apa pun.  
- **Perpustakaan mana yang melakukan konversi?** Aspose.CAD untuk .NET menyediakan rasterisasi dan ekspor PDF tanpa ketergantungan eksternal.  
- **Apakah saya memerlukan lisensi?** Lisensi sementara atau penuh diperlukan untuk produksi; versi percobaan gratis tersedia.  
- **Bisakah saya mengatur dimensi halaman khusus?** Ya—gunakan `PageWidth` dan `PageHeight` dalam `RasterizationOptions`.  
- **Apakah geometri 3‑D akan dipertahankan?** Entitas 3‑D dirasterisasi; aktifkan `TypeOfEntities.Entities3D` untuk dukungan 3‑D penuh.

## Apa itu “ekspor PDF” dalam konteks CAD?

Mengekspor PDF dari CAD berarti mengambil gambar CAD (DWG, DXF, DGN, dll.) dan mengonversinya menjadi file PDF yang dapat berisi grafik vektor, tampilan 3‑D yang dirasterisasi, dan informasi tata letak halaman yang tepat, memudahkan berbagi dengan siapa saja yang tidak memiliki perangkat lunak CAD.

## Mengapa menggunakan Aspose.CAD untuk mengekspor PDF?

Aspose.CAD memungkinkan Anda **mengatur ukuran halaman PDF** dan mengekspor PDF sepenuhnya dalam kode .NET yang dikelola. Ia mendukung lebih dari 50 format CAD, memproses file hingga 2 GB tanpa memuat seluruh dokumen ke memori, dan mempertahankan ketebalan garis, warna, serta rendering entitas 3‑D opsional dengan DPI rasterisasi hingga 1200. Perpustakaan ini berjalan di Windows, Linux, dan macOS, sehingga PDF yang dihasilkan dapat digunakan di platform apa pun.

## Prasyarat

- **Aspose.CAD untuk .NET** terinstal. Unduh dari [Aspose.CAD for .NET download page](https://releases.aspose.com/cad/net/).  
- Folder yang berisi file CAD yang ingin Anda konversi (misalnya, `C:\CAD\`).  
- .NET 6.0 atau lebih baru (atau .NET Framework 4.7.2).  

## Impor Namespace

Pernyataan `using` mengimpor namespace Aspose.CAD yang diperlukan untuk bekerja dengan opsi rasterisasi dan PDF.  

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
```

## Panduan Langkah‑per‑Langkah

### Cara mengatur ukuran halaman PDF saat mengekspor CAD ke PDF?

Muat file CAD Anda, konfigurasikan dimensi halaman dalam `RasterizationOptions`, lampirkan opsi tersebut ke instance `PdfOptions`, dan panggil `Save`. Alur empat langkah ini memberi Anda kontrol penuh atas ukuran output dan kualitas sambil menjaga kode tetap ringkas.

### Langkah 1: Muat Gambar CAD

Kelas `Image` mewakili gambar CAD yang dimuat ke memori, siap untuk rasterisasi.  

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";
using (Image cadImage = Image.Load(sourceFilePath))
{
    // Your code for loading the CAD image goes here
}
```

### Langkah 2: Konfigurasikan Opsi Rasterisasi (Simpan CAD sebagai PDF)

Kelas `RasterizationOptions` menentukan bagaimana data CAD dirasterisasi, termasuk ukuran halaman, DPI, dan apakah entitas 3‑D dirender.  

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 500;
rasterizationOptions.PageHeight = 500;
// rasterizationOptions.TypeOfEntities = TypeOfEntities.Entities3D;

rasterizationOptions.Layouts = new string[] { "Model" };
```

### Langkah 3: Atur Opsi PDF (Buat PDF dari CAD)

Kelas `PdfOptions` menyimpan pengaturan format output dan menghubungkan opsi rasterisasi ke pembuatan PDF.  

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

### Langkah 4: Simpan sebagai PDF (Hasilkan PDF dari Model 3D)

Metode `Save` pada objek `Image` menulis konten yang dirasterisasi ke file PDF yang ditentukan, menghasilkan dokumen siap‑dibagikan.  

```csharp
MyDir = MyDir + "Export3DImagestoPDF_out.pdf";
cadImage.Save(MyDir, pdfOptions);
```

## Masalah Umum dan Solusinya

| Masalah | Alasan | Solusi |
|-------|--------|-----|
| **PDF keluaran kosong** | Nama layout salah atau layout `Model` tidak ada. | Verifikasi `rasterizationOptions.Layouts` cocok dengan layout yang ada dalam file CAD. |
| **Resolusi rendah** | DPI rasterisasi default rendah. | Atur `rasterizationOptions.Resolution = 300;` sebelum menyimpan. |
| **Entitas 3‑D tidak ditampilkan** | `TypeOfEntities` dikomentari. | Hapus komentar pada `rasterizationOptions.TypeOfEntities = TypeOfEntities.Entities3D;`. |
| **Pengecualian lisensi** | Menggunakan percobaan tanpa lisensi. | Terapkan lisensi sementara atau permanen via `License license = new License(); license.SetLicense("Aspose.CAD.lic");`. |

## Pertanyaan yang Sering Diajukan

**Q: Apakah Aspose.CAD kompatibel dengan semua format file CAD?**  
A: Ya, Aspose.CAD mendukung lebih dari 50 format input dan output, termasuk DWG, DXF, DGN, STL, dan IFC, memastikan fleksibilitas untuk proyek apa pun.

**Q: Apakah saya dapat menyesuaikan dimensi halaman saat mengekspor ke PDF?**  
A: Tentu saja. Atur `PageWidth` dan `PageHeight` dalam `RasterizationOptions` ke ukuran apa pun dalam poin, inci, atau milimeter sebelum memanggil `Save`.

**Q: Apakah lisensi sementara tersedia untuk Aspose.CAD?**  
A: Ya, Anda dapat memperoleh lisensi sementara untuk Aspose.CAD dengan mengunjungi [Temporary License](https://purchase.aspose.com/temporary-license/).

**Q: Di mana saya dapat menemukan dukungan tambahan atau diskusi komunitas?**  
A: Kunjungi [Aspose.CAD Forum](https://forum.aspose.com/c/cad/19) untuk bantuan ahli dan saran sesama pengguna.

**Q: Apakah ada versi percobaan gratis Aspose.CAD?**  
A: Ya, Anda dapat menjelajahi fitur Aspose.CAD dengan mengakses [free trial](https://releases.aspose.com/).

## Kesimpulan

Anda kini memiliki metode lengkap yang siap produksi untuk **mengatur ukuran halaman PDF** dan **mengekspor PDF dari gambar CAD 3D** menggunakan Aspose.CAD untuk .NET. Dengan menyesuaikan opsi rasterisasi, Anda dapat menyetel resolusi, tata letak halaman, dan rendering entitas 3‑D untuk memenuhi setiap kebutuhan dokumentasi. Bereksperimenlah dengan pengaturan DPI dan dimensi halaman yang berbeda untuk mencapai keseimbangan sempurna antara ukuran file dan fidelitas visual.

{{< blocks/products/products-backtop-button >}}

## Tutorial Terkait

- [Mengekspor Tata Letak Spesifik ke PDF - Panduan Aspose.CAD](/cad/net/advanced-export-techniques/exporting-specific-layouts-to-pdf/)
- [Mengekspor DWG ke PDF atau Gambar Raster - Panduan Aspose.CAD](/cad/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/)
- [Ekspor DGN ke PDF dalam Aspose.CAD untuk .NET](/cad/net/cad-export-formats/export-dgn-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

--- 

**Last Updated:** 2026-07-04  
**Tested With:** Aspose.CAD 24.11 for .NET  
**Author:** Aspose