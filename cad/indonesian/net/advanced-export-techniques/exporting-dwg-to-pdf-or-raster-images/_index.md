---
date: 2026-03-16
description: Pelajari cara mengonversi DWG ke PDF atau gambar raster dengan Aspose.CAD
  untuk .NET. Tutorial cad ke pdf langkah demi langkah ini mencakup mengekspor DWG
  ke format gambar seperti PNG dan menunjukkan cara mengekspor DWG ke file gambar
  secara efisien.
linktitle: Exporting DWG to PDF or Raster Images
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Cara mengonversi DWG ke PDF dan Gambar Raster menggunakan Aspose.CAD untuk
  .NET
url: /id/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Mengekspor DWG ke PDF atau Gambar Raster - Panduan Aspose.CAD

## Pendahuluan

Jika Anda perlu **mengonversi DWG ke PDF** (atau ke format raster seperti PNG) langsung dari aplikasi .NET, Anda berada di tempat yang tepat. Dalam tutorial ini kami akan menjelaskan langkah‑langkah tepat yang diperlukan untuk menggunakan Aspose.CAD untuk .NET melakukan konversi, menjelaskan mengapa perpustakaan ini merupakan pilihan yang solid, dan menunjukkan cara menangani output PDF dan gambar dengan hanya beberapa baris kode.

## Jawaban Cepat
- **Perpustakaan apa yang menangani konversi DWG?** Aspose.CAD untuk .NET  
- **Bisakah saya mengekspor DWG ke PNG serta PDF?** Ya – opsi rasterisasi yang sama bekerja untuk kedua format.  
- **Apakah saya memerlukan lisensi untuk pengembangan?** Versi percobaan gratis dapat digunakan untuk pengujian; lisensi komersial diperlukan untuk produksi.  
- **Versi .NET apa yang didukung?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **Apakah konversi satuan ditangani secara otomatis?** Anda dapat mendefinisikan sistem satuan secara manual (metrik atau imperial) seperti yang ditunjukkan dalam kode.

## Apa itu “mengonversi DWG ke PDF”?

Mengonversi DWG ke PDF berarti mengambil gambar CAD (DWG) dan merendernya menjadi dokumen portabel yang hanya dapat dilihat (PDF). Ini berguna untuk berbagi desain dengan pemangku kepentingan yang tidak memiliki perangkat lunak CAD, membuat dokumentasi yang dapat dicetak, atau mengarsipkan gambar dalam format yang dapat dibaca secara universal.

## Mengapa menggunakan Aspose.CAD untuk konversi ini?
- **Tidak ada ketergantungan eksternal** – perpustakaan ini bekerja sepenuhnya dalam kode terkelola.  
- **Fidelity tinggi** – mempertahankan lapisan, ketebalan garis, dan informasi tata letak.  
- **Opsi raster bawaan** – memungkinkan Anda mengekspor ke PNG, JPEG, BMP, dll., dengan satu objek konfigurasi.  
- **Lintas platform** – bekerja di Windows, Linux, dan macOS dengan .NET Core.

## Prasyarat

Sebelum kita memulai tutorial, pastikan Anda memiliki hal‑hal berikut:

- Pemahaman dasar tentang pemrograman .NET.  
- Perpustakaan Aspose.CAD untuk .NET terpasang. Jika belum, unduh di [sini](https://releases.aspose.com/cad/net/).  
- IDE (Integrated Development Environment) favorit Anda sudah disiapkan untuk pengembangan .NET.

## Impor Namespace

Mari kita mulai dengan mengimpor namespace yang diperlukan dalam proyek .NET Anda. Ini memastikan Anda memiliki akses ke fungsi Aspose.CAD dalam kode Anda.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
```

## Langkah 1: Muat File DWG

Mulailah dengan memuat file DWG yang ingin Anda konversi. Ganti `"Your Document Directory"` dengan jalur ke file DWG Anda.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Bottom_plate.dwg";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Your code for loading DWG goes here
}
```

## Langkah 2: Siapkan Ekspor PDF (Cara mengekspor DWG ke PDF)

Sekarang, mari konfigurasikan pengaturan ekspor PDF. Contoh ini menunjukkan cara mengatur tata letak dan menangani konversi satuan.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.Layouts = new string[] { "Model" };

// Check and define the unit system
bool currentUnitIsMetric = false;
double currentUnitCoefficient = 1.0;
DefineUnitSystem(cadImage.UnitType, out currentUnitIsMetric, out currentUnitCoefficient);

// Your code for setting up PDF export goes here
```

## Langkah 3: Ekspor ke PDF

Jalankan ekspor ke PDF menggunakan pengaturan yang telah dikonfigurasi.

```csharp
PdfOptions pdfOptions = new PdfOptions
{
    VectorRasterizationOptions = rasterizationOptions
};

cadImage.Save(outPath, pdfOptions);
```

## Langkah 4: Ekspor ke Gambar Raster (ekspor dwg ke gambar)

Perluas fungsionalitas untuk mengekspor ke gambar raster, seperti PNG.

```csharp
// A4 size at 300 DPI - 2480 x 3508
rasterizationOptions.PageHeight = 3508;
rasterizationOptions.PageWidth = 2480;

PngOptions pngOptions = new PngOptions
{
    VectorRasterizationOptions = rasterizationOptions
};

cadImage.Save(outPath.Replace("pdf", "png"), pngOptions);
```

## Masalah Umum dan Solusinya

| Masalah | Mengapa Terjadi | Cara Memperbaiki |
|-------|----------------|------------|
| **Halaman kosong dalam PDF** | Tata letak tidak ditentukan dengan benar | Pastikan `rasterizationOptions.Layouts` mencakup nama tata letak yang tepat (mis., `"Model"`). |
| **Dimensi tidak tepat** | DPI atau ukuran halaman tidak cocok | Sesuaikan nilai `PageHeight`, `PageWidth`, dan DPI dalam `CadRasterizationOptions`. |
| **Satuan muncul salah** | Konversi satuan tidak didefinisikan | Gunakan `DefineUnitSystem` untuk mengatur `currentUnitIsMetric` dan `currentUnitCoefficient` berdasarkan `cadImage.UnitType`. |
| **Pengecualian lisensi** | Batasan versi percobaan | Terapkan lisensi sementara atau permanen sebelum memanggil `Image.Load`. |

## Pertanyaan yang Sering Diajukan

### Q1: Bisakah saya menggunakan Aspose.CAD untuk .NET dalam proyek komersial saya?
A1: Ya, Anda dapat. Kunjungi [purchase.aspose.com/buy](https://purchase.aspose.com/buy) untuk detail lisensi.

### Q2: Apakah tersedia versi percobaan gratis?
A2: Tentu! Dapatkan versi percobaan gratis Anda [di sini](https://releases.aspose.com/).

### Q3: Bagaimana saya dapat mendapatkan dukungan untuk Aspose.CAD untuk .NET?
A3: Kunjungi [forum Aspose.CAD](https://forum.aspose.com/c/cad/19) untuk dukungan komunitas.

### Q4: Bisakah saya mendapatkan lisensi sementara untuk tujuan pengujian?
A4: Ya, Anda dapat memperoleh lisensi sementara [di sini](https://purchase.aspose.com/temporary-license/).

### Q5: Di mana saya dapat menemukan dokumentasi terperinci?
A5: Dokumentasi tersedia di [Aspose.CAD](https://reference.aspose.com/cad/net/).

### Q6: Bagaimana cara **menyimpan CAD sebagai PNG** dengan kualitas tinggi?
A6: Atur `PageHeight` dan `PageWidth` ke dimensi piksel yang diinginkan dan pilih DPI 300 atau lebih tinggi dalam `CadRasterizationOptions`.

### Q7: Apa cara terbaik untuk **mengonversi dwg** ketika file sumber berisi banyak tata letak?
A7: Isi `rasterizationOptions.Layouts` dengan semua nama tata letak yang ingin Anda ekspor, kemudian lakukan loop melalui setiap tata letak dan panggil `Save` untuk setiap format output.

---

**Terakhir Diperbarui:** 2026-03-16  
**Diuji Dengan:** Aspose.CAD 24.11 untuk .NET  
**Penulis:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}