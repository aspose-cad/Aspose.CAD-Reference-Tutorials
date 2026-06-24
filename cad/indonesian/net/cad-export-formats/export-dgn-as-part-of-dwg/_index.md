---
date: 2026-03-21
description: Pelajari cara membuat PDF dari DWG dan mengekspor DGN sebagai bagian
  dari DWG menggunakan Aspose.CAD untuk .NET. Panduan ini juga menunjukkan cara mengonversi
  DWG ke PDF dan mengatur opsi PDF.
linktitle: Export DGN as Part of DWG
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Buat PDF dari DWG dan Ekspor DGN sebagai Bagian dari DWG – Aspose.CAD untuk
  .NET
url: /id/net/cad-export-formats/export-dgn-as-part-of-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Buat PDF dari DWG dan Ekspor DGN sebagai Bagian dari DWG – Aspose.CAD untuk .NET

## Pendahuluan

Jika Anda perlu **membuat PDF dari DWG** sambil juga menyematkan desain DGN sebagai bagian dari DWG, Aspose.CAD untuk .NET mempermudahnya. Dalam tutorial ini kami akan membahas seluruh alur kerja: memuat DWG, menemukan DGN underlay yang disematkan, mengonfigurasi opsi rasterisasi, dan akhirnya mengekspor hasilnya ke dokumen PDF. Baik Anda membangun alat konversi batch, mesin pelaporan, atau layanan integrasi CAD‑BIM, langkah‑langkah di bawah ini akan memberi Anda fondasi yang solid dan siap produksi.

## Jawaban Cepat
- **Perpustakaan apa yang menangani konversi DWG → PDF?** Aspose.CAD for .NET  
- **Apakah saya dapat mengekspor DGN underlay saat membuat PDF?** Ya – underlay dapat diakses melalui `CadDgnUnderlay`.  
- **Metode apa yang mengatur opsi PDF?** `PdfOptions` bersama dengan `CadRasterizationOptions`.  
- **Apakah saya memerlukan lisensi untuk penggunaan komersial?** Ya, lisensi Aspose.CAD yang valid diperlukan.  
- **Versi .NET yang didukung?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.

## Apa itu “membuat PDF dari DWG”?

Membuat PDF dari file DWG berarti merender gambar vektor menjadi dokumen PDF berbasis raster atau vektor. Proses ini berguna untuk berbagi gambar dengan pemangku kepentingan yang tidak memiliki perangkat lunak CAD, pengarsipan, atau pembuatan laporan yang dapat dicetak. Aspose.CAD menyederhanakan tugas ini dengan menangani parsing entitas DWG secara mendalam dan memberikan kontrol terperinci atas output melalui `PdfOptions`.

## Mengapa mengekspor DGN sebagai bagian dari DWG?

DGN underlay sering mewakili geometri referensi dari proyek MicroStation. Dengan mengekspor DGN bersama DWG Anda mempertahankan konteks desain asli, memastikan bahwa konsumen downstream melihat set gambar lengkap. Ini sangat berharga dalam proyek multidisiplin di mana file DWG dan DGN coexist.

## Prasyarat

- **Aspose.CAD untuk .NET** – unduh di [sini](https://releases.aspose.com/cad/net/).  
- **Lingkungan Pengembangan** – Visual Studio (versi terbaru apa pun) atau IDE .NET pilihan Anda.  
- **Pengetahuan dasar C#** – Anda harus nyaman dengan sintaks C# dan struktur proyek .NET.

## Impor Namespace

Tambahkan direktif `using` yang diperlukan di bagian atas file sumber C# Anda:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Panduan Langkah‑per‑Langkah

### Langkah 1: Tentukan Jalur File

Tentukan file DWG input dan nama PDF output.

```csharp
// Input and Output file paths
string fileName = "BlockRefDgn.dwg";
string outPath = fileName + ".pdf";
```

### Langkah 2: Buat Instance `PdfOptions` (atur opsi pdf)

`PdfOptions` memungkinkan Anda mengontrol cara PDF dihasilkan, seperti ukuran halaman, kompresi, dan metadata.

```csharp
// Create an instance of PdfOptions class for exporting DWG to PDF
PdfOptions exportOptions = new PdfOptions();
```

### Langkah 3: Muat File DWG

Muat DWG sebagai `CadImage` sehingga Anda dapat memeriksa entitasnya.

```csharp
// Load the existing DWG file as an image and convert it to CadImage type
using (CadImage cadImage = (CadImage)Image.Load(fileName))
```

### Langkah 4: Iterasi Melalui Entitas

Jelajahi setiap entitas dalam gambar untuk menemukan DGN underlay.

```csharp
// Iterate through each entity inside the DWG file
foreach (CadBaseEntity baseEntity in cadImage.Entities)
```

### Langkah 5: Periksa Tipe Entitas (cara mengekspor dgn)

Identifikasi apakah entitas saat ini adalah DGN underlay.

```csharp
// Check if the entity is an image definition
if (baseEntity.TypeName == CadEntityTypeName.DGNUNDERLAY)
```

### Langkah 6: Dapatkan Jalur Underlay

Ambil jalur referensi eksternal file DGN.

```csharp
// If it's an image definition, get the external reference to the object
CadDgnUnderlay dgnFile = (CadDgnUnderlay)baseEntity;
Console.WriteLine(dgnFile.UnderlayPath);
```

### Langkah 7: Tentukan Opsi Rasterisasi (konversi dwg ke pdf)

Konfigurasikan cara DWG dirasterisasi sebelum ditempatkan ke dalam PDF.

```csharp
// Define settings for CadRasterizationOptions object
exportOptions.VectorRasterizationOptions = new CadRasterizationOptions()
{
    PageWidth = 1600,
    PageHeight = 1600,
    Layouts = new string[] { "Model" },
    AutomaticLayoutsScaling = false,
    NoScaling = true,
    BackgroundColor = Color.Black,
    DrawType = CadDrawTypeMode.UseObjectColor
};
```

### Langkah 8: Ekspor DWG ke PDF

Akhirnya, simpan gambar yang dirender sebagai file PDF.

```csharp
// Export the DWG to PDF by calling Save method
cadImage.Save(outPath, exportOptions);
```

## Masalah Umum dan Solusinya

| Issue | Reason | Fix |
|-------|--------|-----|
| **`Image.Load` melempar “File not found”** | Jalur tidak tepat atau file tidak ada. | Gunakan jalur absolut atau pastikan DWG disalin ke folder output. |
| **Jalur underlay kosong** | DGN underlay tidak disematkan atau referensi rusak. | Verifikasi bahwa DWG memang berisi DGN underlay dan file DGN eksternal dapat diakses. |
| **Output PDF kosong** | Opsi rasterisasi diatur ke ukuran nol. | Sesuaikan `PageWidth`/`PageHeight` atau set `NoScaling = false`. |
| **Pengecualian lisensi** | Menjalankan tanpa lisensi Aspose.CAD yang valid. | Terapkan lisensi sebelum memuat gambar: `License lic = new License(); lic.SetLicense("Aspose.CAD.lic");` |

## Pertanyaan yang Sering Diajukan

### Q1: Apakah saya dapat menggunakan Aspose.CAD untuk .NET dalam proyek komersial saya?
A1: Ya, Anda dapat. Kunjungi [sini](https://purchase.aspose.com/buy) untuk menjelajahi opsi lisensi.

### Q2: Apakah ada batasan ukuran file DWG yang dapat saya proses?
A2: Aspose.CAD mendukung penanganan file DWG besar, namun batasan perangkat keras dapat berlaku.

### Q3: Apakah tersedia versi percobaan?
A3: Ya, Anda dapat memperoleh percobaan gratis [sini](https://releases.aspose.com/).

### Q4: Bagaimana saya dapat memperoleh lisensi sementara?
A4: Lisensi sementara dapat diperoleh [sini](https://purchase.aspose.com/temporary-license/).

### Q5: Di mana saya dapat mencari bantuan jika mengalami masalah?
A5: Anda dapat mengunjungi forum Aspose.CAD [sini](https://forum.aspose.com/c/cad/19) untuk dukungan.

**Q: Bagaimana cara mengatur metadata PDF tambahan (penulis, judul, dll.)?**  
A: Gunakan properti `exportOptions.Metadata` sebelum memanggil `Save`.

**Q: Dapatkah saya mengekspor beberapa layout ke halaman PDF terpisah?**  
A: Ya – atur `Layouts = new string[] { "Layout1", "Layout2" }` dalam `CadRasterizationOptions`.

**Q: Apakah Aspose.CAD mendukung konversi DWG ke format gambar lain?**  
A: Tentu saja. Anda dapat mengekspor ke PNG, JPEG, SVG, dan lainnya dengan menggunakan overload `Image.Save` yang sesuai.

**Terakhir Diperbarui:** 2026-03-21  
**Diuji Dengan:** Aspose.CAD 24.11 untuk .NET  
**Penulis:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}