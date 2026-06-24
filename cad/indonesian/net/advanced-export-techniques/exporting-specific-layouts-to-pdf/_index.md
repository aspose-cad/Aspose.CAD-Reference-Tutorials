---
date: 2026-03-13
description: Pelajari cara mengatur opsi rasterisasi CAD dan mengekspor tata letak
  DWG tertentu ke PDF menggunakan Aspose.CAD untuk .NET – panduan definitif untuk
  membuat PDF dari file CAD.
linktitle: Exporting Specific Layouts to PDF
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Atur Opsi Rasterisasi CAD – Ekspor Tata Letak Tertentu ke PDF - Panduan Aspose.CAD
url: /id/net/advanced-export-techniques/exporting-specific-layouts-to-pdf/
weight: 13
---

 is.

Also markdown links: keep same.

Now produce final output.

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Mengekspor Tata Letak Spesifik ke PDF - Panduan Aspose.CAD

## Pendahuluan

Dalam tutorial ini Anda akan menemukan **cara mengatur opsi rasterisasi CAD** sehingga Anda dapat mengekspor satu tata letak—atau beberapa tata letak—dari file DWG langsung ke PDF. Aspose.CAD untuk .NET membuat proses *dwg to pdf conversion c#* menjadi sederhana, memberi Anda kontrol penuh atas ukuran halaman, resolusi, dan pemilihan tata letak. Pada akhir panduan Anda akan dapat **membuat PDF dari file CAD** dengan hanya beberapa baris kode.

## Jawaban Cepat
- **Apa yang dilakukan “set cad rasterization options”?**  
  Ini memberi tahu Aspose.CAD bagaimana merender data vektor (tata letak, lapisan, ketebalan garis) menjadi halaman PDF yang dirasterkan.  
- **Metode apa yang mengekspor tata letak DWG ke PDF?**  
  Gunakan `Image.Save` dengan `PdfOptions` yang telah dikonfigurasi yang berisi `CadRasterizationOptions` Anda.  
- **Apakah saya dapat mengekspor lebih dari satu tata letak sekaligus?**  
  Ya – berikan array nama tata letak pada properti `Layouts`.  
- **Apakah saya memerlukan lisensi untuk penggunaan produksi?**  
  Lisensi komersial diperlukan; versi percobaan gratis tersedia untuk evaluasi.  
- **Versi .NET apa yang didukung?**  
  .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6 dan yang lebih baru.

## Apa itu “set cad rasterization options”?
`CadRasterizationOptions` adalah kelas yang mengontrol bagaimana entitas CAD dirasterkan saat dikonversi ke format berbasis raster seperti PDF. Dengan mengonfigurasi propertinya—dimensi halaman, pemilihan tata letak, warna latar belakang, dll.—Anda menentukan hasil visual dari operasi **export dwg layout to pdf**.

## Mengapa mengatur opsi rasterisasi CAD?
- **Presisi** – Mempertahankan ketebalan garis dan skala persis seperti yang muncul dalam gambar CAD asli.  
- **Kinerja** – Merender hanya tata letak yang Anda butuhkan, mengurangi ukuran file dan waktu pemrosesan.  
- **Fleksibilitas** – Menyesuaikan lebar/tinggi halaman, DPI, dan latar belakang agar sesuai dengan standar pelaporan Anda.  

## Prasyarat

Sebelum kita masuk ke kode, pastikan Anda memiliki:

- **Aspose.CAD untuk .NET** terpasang. Anda dapat mengunduhnya [di sini](https://releases.aspose.com/cad/net/).  
- Lingkungan pengembangan .NET (Visual Studio, VS Code, atau IDE lain yang Anda sukai).  
- File DWG yang berisi setidaknya satu tata letak (file contoh yang digunakan di sini adalah `visualization_-_conference_room.dwg`).

## Impor Namespace

Di proyek .NET Anda, impor namespace yang diperlukan untuk Aspose.CAD:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Panduan Langkah‑per‑Langkah

### Langkah 1: Muat file DWG

Pertama, arahkan Aspose.CAD ke file DWG sumber yang ingin Anda konversi.

```csharp
// The path to the documents directory.
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "visualization_-_conference_room.dwg";

using (Image image = Image.Load(sourceFilePath))
{
    // Your code for further steps goes here.
}
```

### Langkah 2: Atur **CadRasterizationOptions**

Di sini kami mengonfigurasi pengaturan rasterisasi yang menentukan ukuran halaman PDF dan resolusinya.

```csharp
// Create an instance of CadRasterizationOptions and set its various properties
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
```

> **Tips pro:** Sesuaikan `PageWidth` dan `PageHeight` agar cocok dengan dimensi tata letak PDF target Anda. Nilai yang lebih besar meningkatkan detail tetapi juga ukuran file.

### Langkah 3: Tentukan nama tata letak

Beritahu Aspose.CAD tata letak mana yang akan dirender. Ganti `"Layout1"` dengan nama tepat tata letak di file DWG Anda.

```csharp
// Specify desired layout name
rasterizationOptions.Layouts = new string[] { "Layout1" };
```

> **Mengapa ini penting:** Dengan membatasi array `Layouts` Anda menghindari mengekspor lembar yang tidak diinginkan, sehingga operasi **dwg to pdf conversion c#** menjadi lebih cepat dan PDF yang dihasilkan lebih bersih.

### Langkah 4: Buat `PdfOptions`

Hubungkan pengaturan rasterisasi ke opsi ekspor PDF.

```csharp
// Create an instance of PdfOptions
PdfOptions pdfOptions = new PdfOptions();
// Set the VectorRasterizationOptions property
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

### Langkah 5: Ekspor ke PDF

Akhirnya, simpan tata letak yang telah dirender sebagai file PDF.

```csharp
MyDir = MyDir + "ExportSpecificLayoutToPDF_out.pdf";
// Export the DWG to PDF
image.Save(MyDir, pdfOptions);
```

### Langkah 6: Tampilkan pesan sukses

Output konsol singkat mengonfirmasi operasi berhasil.

```csharp
// Display success message
Console.WriteLine("\nThe DWG file with a specific layout exported successfully to PDF.\nFile saved at " + MyDir);
```

## Masalah Umum & Solusi

| Masalah | Penyebab | Solusi |
|-------|-------|-----|
| **Tidak ada PDF yang dihasilkan** | Array `Layouts` tidak cocok dengan nama tata letak apa pun di DWG. | Verifikasi nama tata letak menggunakan penampil CAD dan perbarui properti `Layouts`. |
| **Halaman kosong** | `PageWidth`/`PageHeight` diatur ke 0 atau nilai sangat kecil. | Gunakan dimensi realistis (misalnya, 1600 × 1600) atau biarkan Aspose menghitung otomatis dengan menghilangkan properti tersebut. |
| **Skala tidak tepat** | DPI tidak diatur ketika output beresolusi tinggi diperlukan. | Atur `rasterizationOptions.Resolution = 300;` (atau DPI yang diinginkan) sebelum mengekspor. |

## Pertanyaan yang Sering Diajukan

**T: Bisakah saya mengekspor beberapa tata letak sekaligus?**  
J: Ya, cukup ubah array `Layouts` pada Langkah 3 untuk menyertakan semua nama tata letak yang diinginkan, misalnya `new string[] { "Layout1", "Layout2" }`.

**T: Apakah Aspose.CAD kompatibel dengan format file CAD lain?**  
J: Tentu. Ia mendukung DWG, DXF, DWF, DGN, dan banyak format lainnya.

**T: Bagaimana saya dapat menyesuaikan pengaturan output PDF selain ukuran halaman?**  
J: Jelajahi properti tambahan `CadRasterizationOptions` seperti `Resolution`, `BackgroundColor`, dan `DrawType` untuk menyempurnakan hasil.

**T: Di mana saya dapat menemukan dokumentasi Aspose.CAD tambahan?**  
J: Kunjungi [dokumentasi](https://reference.aspose.com/cad/net/) untuk referensi API mendalam dan contoh.

**T: Apakah ada versi percobaan gratis?**  
J: Ya, Anda dapat mengakses versi percobaan gratis [di sini](https://releases.aspose.com/).

## Kesimpulan

Anda kini telah mempelajari cara **mengatur opsi rasterisasi CAD** dan menggunakannya untuk **mengekspor tata letak DWG tertentu ke PDF** dengan Aspose.CAD untuk .NET. Pendekatan ini memberi Anda kontrol presisi atas proses konversi, memungkinkan integrasi fungsi CAD‑ke‑PDF ke dalam aplikasi C# apa pun dengan cepat dan andal.

---

**Terakhir Diperbarui:** 2026-03-13  
**Diuji Dengan:** Aspose.CAD 24.11 untuk .NET  
**Penulis:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}