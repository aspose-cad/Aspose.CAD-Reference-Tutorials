---
date: 2026-03-02
description: Pelajari cara membuat satu PDF dengan tata letak berbeda menggunakan
  Aspise.CAD untuk .NET – mengonversi CAD ke PDF, mengekspor DWG ke PDF, dan menyimpan
  CAD sebagai PDF secara efisien.
linktitle: Creating Single PDF with Different Layouts
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Cara membuat PDF tunggal dengan Tata Letak Berbeda - Panduan Aspose.CAD
url: /id/net/advanced-cad-techniques/creating-single-pdf-with-different-layouts/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cara membuat PDF tunggal dengan Tata Letak Berbeda - Panduan Aspose.CAD

## Pendahuluan

Jika Anda perlu **membuat file pdf tunggal** yang berisi beberapa tata letak CAD, Anda berada di tempat yang tepat. Pada tutorial ini kami akan memandu langkah demi langkah yang diperlukan untuk mengonversi gambar CAD menjadi satu dokumen PDF, menangani banyak tata letak di sepanjang proses. Anda akan melihat bagaimana Aspose.CAD untuk .NET memudahkan **konversi CAD ke PDF**, **ekspor DWG ke PDF**, dan **menyimpan CAD sebagai PDF** hanya dengan beberapa baris kode C#.

## Jawaban Cepat
- **Apa yang dibahas dalam tutorial ini?** Membuat satu PDF yang mencakup beberapa tata letak CAD.  
- **Perpustakaan apa yang digunakan?** Aspose.CAD untuk .NET.  
- **Apakah saya memerlukan lisensi?** Versi percobaan gratis cukup untuk evaluasi; lisensi diperlukan untuk produksi.  
- **Format CAD yang didukung?** DWG, DXF, DGN, dan banyak lainnya.  
- **Waktu implementasi tipikal?** Sekitar 10‑15 menit untuk konversi dasar.

## Apa itu “create single pdf” dalam konteks CAD?

Membuat PDF tunggal berarti mengambil satu file sumber CAD yang mungkin berisi beberapa definisi tata letak (paper spaces) dan menggabungkan setiap tata letak menjadi halaman terpisah dalam satu dokumen PDF. Ini sangat berguna untuk rencana arsitektur, skema teknik, atau skenario apa pun di mana klien mengharapkan paket PDF yang terintegrasi.

## Mengapa menggunakan Aspose.CAD untuk tugas ini?

- **Tanpa ketergantungan eksternal** – murni .NET, tidak memerlukan instalasi AutoCAD.  
- **Kontrol penuh atas rasterisasi** – Anda dapat mengatur ukuran halaman, DPI, dan dimensi tata letak khusus.  
- **Rendering dengan fidelitas tinggi** – data vektor dipertahankan bila memungkinkan, memastikan output yang tajam.  
- **Siap untuk batch** – kode yang sama dapat ditempatkan dalam loop untuk memproses banyak gambar secara otomatis.

## Prasyarat

- Aspose.CAD untuk .NET: Pastikan Anda telah menginstal Aspose.CAD untuk .NET. Anda dapat mengunduhnya dari [here](https://releases.aspose.com/cad/net/).  
- Lingkungan Pengembangan: Siapkan lingkungan pengembangan .NET, dan miliki pemahaman dasar tentang pemrograman C#.

## Impor Namespace

Di proyek C# Anda, sertakan namespace yang diperlukan untuk memanfaatkan fungsionalitas Aspose.CAD untuk .NET:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## Panduan langkah demi langkah

### Langkah 1: Muat Gambar CAD

Pertama, muat file CAD sumber (misalnya, gambar DWG). Kelas `CadImage` memberi Anda akses ke semua tata letak di dalam file.

```csharp
// The path to the documents directory.
string MyDir = "Your Document Directory";

using (CadImage cadImage = (CadImage)Image.Load(MyDir + "City skyway map.dwg"))
{
    // Your code for Step 1 goes here
}
```

### Langkah 2: Sesuaikan Opsi Rasterisasi

Tentukan bagaimana setiap tata letak harus dirasterisasi. Anda dapat mengatur ukuran halaman default dan kemudian menimpanya untuk tata letak tertentu menggunakan `LayoutPageSizes`.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1000;
rasterizationOptions.PageHeight = 1000;

// Custom sizes for several layouts
rasterizationOptions.LayoutPageSizes.Add("ANSI C Plot", new SizeF(500, 1000));
rasterizationOptions.LayoutPageSizes.Add("8.5 x 11 Plot", new SizeF(1000, 100));
```

> **Tip pro:** Sesuaikan DPI (`rasterizationOptions.Resolution`) jika Anda memerlukan output beresolusi tinggi untuk gambar detail.

### Langkah 3: Definisikan Opsi PDF

Bungkus pengaturan rasterisasi dalam objek `PdfOptions`. Ini memberi tahu Aspose.CAD untuk merender data CAD langsung ke aliran PDF.

```csharp
PdfOptions pdfOptions = new PdfOptions() { VectorRasterizationOptions = rasterizationOptions };
```

### Langkah 4: Simpan sebagai PDF

Akhirnya, panggil `Save` pada instance `CadImage`, berikan nama file PDF target dan opsi yang telah disiapkan. Perpustakaan akan menghasilkan satu PDF yang berisi halaman untuk setiap tata letak yang Anda konfigurasikan.

```csharp
cadImage.Save(MyDir + "singlePDF_out.pdf", pdfOptions);
```

Setelah pemanggilan ini, Anda akan memiliki PDF yang menggabungkan tata letak “ANSI C Plot” dan “8.5 x 11 Plot” menjadi satu dokumen yang kohesif.

## Masalah umum & pemecahan masalah

| Masalah | Penyebab | Solusi |
|-------|--------|-----|
| Tata letak tidak muncul di PDF | `LayoutPageSizes` tidak didefinisikan untuk nama tata letak | Verifikasi nama tata letak yang tepat dalam file CAD (case‑sensitive). |
| Output ber kualitas rendah | DPI default adalah 96 | Atur `rasterizationOptions.Resolution = 300` (atau lebih tinggi) sebelum menyimpan. |
| File tidak ditemukan | Path `MyDir` salah | Gunakan `Path.Combine` untuk membangun path yang independen platform. |

## Pertanyaan yang Sering Diajukan

### Q1: Bisakah saya menggunakan Aspose.CAD untuk .NET dengan format CAD lain?

A1: Ya, Aspose.CAD untuk .NET mendukung berbagai format CAD seperti DWG, DXF, DGN, dan lainnya.

### Q2: Apakah tersedia versi percobaan gratis?

A2: Ya, Anda dapat menjelajahi versi percobaan gratis [here](https://releases.aspose.com/).

### Q3: Bagaimana cara mendapatkan dukungan untuk Aspose.CAD untuk .NET?

A3: Kunjungi [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) untuk dukungan komunitas.

### Q4: Di mana saya dapat menemukan dokumentasi detail?

A4: Lihat dokumentasi [here](https://reference.aspose.com/cad/net/).

### Q5: Bisakah saya membeli lisensi untuk Aspose.CAD untuk .NET?

A5: Ya, Anda dapat membeli lisensi [here](https://purchase.aspose.com/buy).

**Pertanyaan & Jawaban Tambahan**

**T:** Bagaimana cara **mengekspor DWG ke PDF** dengan ukuran halaman khusus?  
**J:** Gunakan `CadRasterizationOptions.LayoutPageSizes` untuk memetakan setiap tata letak DWG ke dimensi halaman PDF yang diinginkan, seperti yang ditunjukkan pada Langkah 2.

**T:** Apakah memungkinkan untuk **menyimpan CAD sebagai PDF** tanpa meraster data vektor?  
**J:** Aspose.CAD selalu meraster saat membuat PDF, tetapi Anda dapat meningkatkan DPI untuk mempertahankan fidelitas visual.

## Kesimpulan

Dalam panduan ini kami menunjukkan cara **membuat file pdf tunggal** dari gambar CAD yang berisi banyak tata letak, menggunakan Aspose.CAD untuk .NET. Sekarang Anda memiliki blok‑bangunan untuk **mengonversi CAD ke PDF**, **mengekspor DWG ke PDF**, dan **menyimpan CAD sebagai PDF** dalam alur kerja otomatis tunggal. Bereksperimenlah dengan berbagai pengaturan rasterisasi untuk menyesuaikan kebutuhan kualitas proyek Anda, dan integrasikan kode ini ke dalam pipeline pemrosesan batch yang lebih besar bila diperlukan.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2026-03-02  
**Tested With:** Aspose.CAD untuk .NET 24.11  
**Author:** Aspose  

---