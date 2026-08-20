---
date: 2026-04-03
description: Pelajari cara mengatur viewport dan mengonversi DWG ke PDF dalam C# menggunakan
  Aspose.CAD. Tutorial dwg ke pdf ini menunjukkan ekspor yang tepat dengan koordinat.
keywords:
- how to set viewport
- dwg to pdf tutorial
- convert dwg to pdf c#
linktitle: Mengonversi DWG ke PDF dengan Koordinat di C#
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Cara Mengatur Viewport saat Mengonversi DWG ke PDF dengan Koordinat di C# -
  Tutorial Aspose.CAD
url: /id/net/conversion-and-export/converting-dwg-to-pdf-with-coordinates/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Mengonversi DWG ke PDF dengan Koordinat di C# - Tutorial Aspose.CAD

## Pendahuluan

Selamat datang di tutorial komprehensif ini tentang **cara mengatur viewport** saat mengonversi file DWG ke PDF dengan koordinat yang ditentukan menggunakan Aspose.CAD untuk .NET. Dengan mengendalikan viewport, Anda mendapatkan PDF pixel‑perfect yang tepat sesuai area yang Anda butuhkan—sempurna untuk gambar konstruksi, pratinjau denah lantai, atau alur kerja BIM apa pun.

## Jawaban Cepat
- **Apa arti “set viewport”?** Itu mendefinisikan wilayah yang terlihat dan skala gambar CAD selama rasterisasi.  
- **Perpustakaan mana yang menangani konversi?** Aspose.CAD untuk .NET.  
- **Apakah saya memerlukan lisensi?** Versi percobaan gratis dapat digunakan untuk evaluasi; lisensi komersial diperlukan untuk produksi.  
- **Platform yang didukung?** Windows, Linux, dan macOS dengan .NET 5/6/7 atau .NET Framework 4.6+.  
- **Waktu implementasi tipikal?** Sekitar 10‑15 menit untuk konversi dasar.

## Prasyarat

Sebelum kita mulai, pastikan Anda memiliki prasyarat berikut:

- **Aspose.CAD Library** – Unduh dan instal pustaka Aspose.CAD untuk .NET. Anda dapat menemukan pustaka tersebut [di sini](https://releases.aspose.com/cad/net/).
- **Lingkungan Pengembangan** – Visual Studio, Rider, atau IDE apa pun yang mendukung pengembangan .NET.
- **File DWG** – Siapkan file DWG yang siap untuk dikonversi. Anda dapat menggunakan file contoh yang disediakan atau file DWG khusus Anda.

## Cara Mengatur Viewport untuk Ekspor PDF yang Presisi

Mengatur viewport adalah langkah inti yang memungkinkan Anda menentukan area tepat dari gambar yang ingin dirender. Pada kode di bawah ini kami membuat `CadVportTableObject` baru, menempatkannya dengan koordinat kiri‑atas, dan menghitung lebar, tinggi, serta rasio aspek. Ini adalah implementasi **cara mengatur viewport** yang menggerakkan seluruh proses konversi.

## Impor Namespace

Di proyek C# Anda, impor namespace yang diperlukan:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadParameters;
using Aspose.CAD.FileFormats.Cad.CadTables;
using Aspose.CAD.ImageOptions;
```

Mari kita uraikan kode menjadi panduan langkah‑demi‑langkah untuk pemahaman yang lebih baik:

## Langkah 1: Tentukan Direktori Dokumen

```csharp
string MyDir = "Your Document Directory";
```

## Langkah 2: Atur Jalur File DWG Sumber

```csharp
string sourceFilePath = MyDir + "visualization_-_conference_room.dwg";
```

## Langkah 3: Muat File DWG dan Konfigurasikan Opsi Rasterisasi

```csharp
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
    rasterizationOptions.Layouts = new string[] { "Model" };
    rasterizationOptions.NoScaling = true;
```

## Langkah 4: Tentukan Koordinat dan Viewport  

Di sini kami sebenarnya **mengatur viewport** (cara mengatur viewport) dengan menentukan sudut kiri‑atas, lebar, dan tinggi area yang ingin Anda ekspor.

```csharp
    Point topLeft = new Point(500, 1000);
    double width = 3108;
    double height = 2489;

    CadVportTableObject newView = new CadVportTableObject();
    newView.Name = new CadStringParameter();
    newView.Name.Init("*Active");
    newView.CenterPoint.X = topLeft.X + width / 2f;
    newView.CenterPoint.Y = topLeft.Y - height / 2f;
    newView.ViewHeight.Value = height;
    newView.ViewAspectRatio.Value = width / height;
```

## Langkah 5: Terapkan Pengaturan Viewport

```csharp
    for (int i = 0; i < cadImage.ViewPorts.Count; i++)
    {
        CadVportTableObject currentView = (CadVportTableObject)(cadImage.ViewPorts[i]);
        if (cadImage.ViewPorts.Count == 1 || string.Equals(currentView.Name.Value.ToLowerInvariant(), "*active"))
        {
            cadImage.ViewPorts[i] = newView;
            break;
        }
    }
```

## Langkah 6: Konfigurasikan Opsi PDF dan Ekspor  

Sekarang kami menggabungkan semuanya dan **mengonversi DWG ke PDF** menggunakan opsi rasterisasi yang baru saja kami siapkan.

```csharp
    Aspose.CAD.ImageOptions.PdfOptions pdfOptions = new Aspose.CAD.ImageOptions.PdfOptions();
    pdfOptions.VectorRasterizationOptions = rasterizationOptions;

    MyDir = MyDir + "ConvertDWGToPDFBySupplyingCoordinates_out.pdf";
    cadImage.Save(MyDir, pdfOptions);
}
```

## Langkah 7: Tampilkan Pesan Sukses

```csharp
Console.WriteLine("\nThe DWG file exported successfully to PDF.\nFile saved at " + MyDir);
```

## Kasus Penggunaan Umum

- **Dokumentasi konstruksi** – Hasilkan PDF yang dapat dicetak dari bagian denah lantai tertentu.  
- **Koordinasi BIM** – Ekspor hanya area yang diminati untuk deteksi benturan.  
- **Presentasi klien** – Sediakan PDF bersih dari ruangan atau elevasi yang dipilih tanpa menampilkan seluruh gambar.

## Kesimpulan

Selamat! Anda telah berhasil **mengonversi DWG ke PDF** dengan koordinat yang tepat dan mempelajari **cara mengatur viewport** menggunakan Aspose.CAD untuk .NET. **Tutorial dwg ke pdf** ini menunjukkan cara **membuat pdf dari dwg** dan **mengekspor dwg sebagai pdf c#** sambil mempertahankan kontrol penuh atas area output.

## FAQ

### Q1: Bisakah saya menggunakan Aspose.CAD dengan format file CAD lainnya?

A1: Ya, Aspose.CAD mendukung berbagai format CAD, termasuk DWG, DXF, DWF, dan lainnya.

### Q2: Bagaimana saya dapat menangani kesalahan selama proses konversi?

A2: Terapkan mekanisme penanganan kesalahan menggunakan blok try‑catch untuk menangkap dan mengelola pengecualian.

### Q3: Apakah Aspose.CAD cocok untuk lingkungan Windows dan Linux?

A3: Ya, Aspose.CAD kompatibel dengan platform Windows dan Linux.

### Q4: Bisakah saya menyesuaikan output PDF lebih lanjut?

A4: Tentu! Jelajahi berbagai opsi yang disediakan oleh Aspose.CAD untuk menyesuaikan output PDF sesuai kebutuhan spesifik Anda.

### Q5: Di mana saya dapat menemukan dukungan tambahan atau diskusi komunitas?

A5: Kunjungi [Aspose.CAD Forum](https://forum.aspose.com/c/cad/19) untuk dukungan komunitas dan diskusi.

## Pertanyaan Umum Tambahan

**Q: Apakah pendekatan ini bekerja dengan file DWG besar (ratusan MB)?**  
A: Ya. Rasterisasi dilakukan halaman‑per‑halaman, dan Anda dapat menyesuaikan `rasterizationOptions` (misalnya, `Resolution`) untuk menyeimbangkan kualitas dan penggunaan memori.

**Q: Bisakah saya mengekspor beberapa viewport ke halaman PDF terpisah?**  
A: Anda dapat melakukan loop melalui `cadImage.ViewPorts`, mengatur masing‑masing sebagai aktif, dan memanggil `Save` untuk setiap halaman, kemudian menggabungkan PDF menggunakan Aspose.PDF.

**Q: Apakah memungkinkan menambahkan watermark ke PDF yang dihasilkan?**  
A: Setelah menyimpan PDF, Anda dapat membukanya kembali dengan Aspose.PDF dan menerapkan watermark teks atau gambar sebelum menyajikannya kepada pengguna.

**Terakhir Diperbarui:** 2026-04-03  
**Diuji Dengan:** Aspose.CAD 24.11 untuk .NET  
**Penulis:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}