---
description: Pelajari cara mengonversi DWG ke PNG dan mengekstrak objek OLE dari file
  DWG menggunakan Aspose.CAD untuk .NET – panduan singkat yang berfokus pada kode.
linktitle: Exporting OLE Objects from DWG Files
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Konversi DWG ke PNG & Ekspor Objek OLE - Tutorial Aspose.CAD
url: /id/net/advanced-export-techniques/exporting-ole-objects-from-dwg/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Mengekspor OLE Objects dari File DWG - Tutorial Aspose.CAD

## Introduction

Jika Anda perlu **mengonversi DWG ke PNG** sambil mengekstrak OLE objects yang tertanam, Anda berada di tempat yang tepat. Aspose.CAD untuk .NET membuat proses dua langkah ini menjadi sederhana, memungkinkan Anda mengotomatisasi ekstraksi dan rasterisasi hanya dengan beberapa baris C#. Dalam beberapa menit ke depan kami akan membahas seluruh alur kerja, mulai dari menyiapkan lingkungan hingga menyimpan setiap DWG sebagai PNG yang berisi data OLE yang telah diekstrak.

## Quick Answers
- **What does this tutorial cover?** Converting DWG to PNG and extracting OLE objects using Aspose.CAD for .NET.  
- **Do I need a license?** A free trial works for development; a commercial license is required for production.  
- **Which .NET versions are supported?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **Can I process multiple DWG files at once?** Yes – the sample loops through an array of file names.  
- **Where can I find more examples?** Check the official Aspose.CAD documentation and forum links below.

## What is **convert DWG to PNG**?
Mengonversi DWG (gambar AutoCAD) ke gambar PNG meraster data vektor, sehingga mudah dilihat atau disematkan dalam halaman web, laporan, atau aplikasi lain yang tidak secara native mendukung DWG. Ketika OLE objects hadir, mereka dapat diekstrak dan disimpan sebagai aset terpisah selama proses konversi.

## Why extract OLE objects from CAD files?
Banyak gambar DWG menyematkan spreadsheet, diagram, atau dokumen Office lain sebagai OLE objects. Mengekstraknya memungkinkan Anda menggunakan kembali data asli, mengotomatisasi pelaporan, atau memigrasikan konten ke format yang lebih baru tanpa kehilangan informasi yang tertanam.

## Prerequisites

- Aspose.CAD for .NET Library: Pastikan Anda telah menginstal library tersebut. Anda dapat mengunduhnya dari [Aspose.CAD for .NET download page](https://releases.aspose.com/cad/net/).
- Document Directory: Siapkan direktori tempat file DWG Anda disimpan. Ganti `"Your Document Directory"` dalam cuplikan kode yang disediakan dengan jalur yang sebenarnya.

## Import Namespaces

Di proyek .NET Anda, impor namespace yang diperlukan:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## Step‑by‑Step Guide

### Step 1: Set the Document Directory

```csharp
string MyDir = "Your Document Directory";
```

Ganti `"Your Document Directory"` dengan jalur tempat file DWG Anda berada.

### Step 2: List the DWG files you want to process

```csharp
string[] files = new string[] { "D ZD junior D10m H2m.dwg", "ZD - Senior D6m H2m45.dwg" };
```

### Step 3: Configure export options for PNG conversion

```csharp
PngOptions pngOptions = new PngOptions { };
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
pngOptions.VectorRasterizationOptions = rasterizationOptions;
rasterizationOptions.Layouts = new string[] { "Layout1" };
```

Anda dapat menyesuaikan `CadRasterizationOptions` (misalnya, `PageWidth`, `PageHeight`, `BackgroundColor`) agar sesuai dengan resolusi output yang diinginkan.

### Step 4: Iterate through each DWG and perform the conversion

```csharp
foreach (string file in files)
{
    using (CadImage cadImage = (CadImage)Image.Load(MyDir + file))
    {
        cadImage.Save(MyDir + file + "_out.png", pngOptions);
    }
}
```

Selama loop ini library secara otomatis **mengekstrak OLE objects** yang tertanam di setiap gambar dan menyertakannya dalam PNG yang dihasilkan. Jika Anda memerlukan aliran OLE mentah, Anda dapat mengakses koleksi `cadImage.OleObjects` – cara yang berguna untuk **how to extract ole** data secara programatik.

## Common Issues & Troubleshooting

- **Missing layout name** – Pastikan layout yang Anda tentukan (`"Layout1"` dalam contoh) ada di DWG sumber; jika tidak, rasterizer akan kembali ke model space default.
- **Large files cause memory pressure** – Proses file satu per satu (seperti yang ditunjukkan) dan segera dispose objek `CadImage` dengan `using`.
- **Unexpected colors** – Atur `rasterizationOptions.BackgroundColor` agar cocok dengan latar belakang gambar jika transparansi diperlukan.

## Frequently Asked Questions

### Q1: Is Aspose.CAD for .NET suitable for both junior and senior CAD files?
A1: Yes, Aspose.CAD for .NET is versatile and can handle a wide range of CAD files, including both junior and senior variants.

### Q2: Can I customize export options for different layouts?
A2: Absolutely! As shown in the tutorial, you can tailor export options, including layouts, to suit your specific needs.

### Q3: Where can I find detailed documentation for Aspose.CAD for .NET?
A3: Explore the [Aspose.CAD for .NET documentation](https://reference.aspose.com/cad/net/) for in‑depth information and examples.

### Q4: Is there a free trial available?
A4: Yes, you can experience the capabilities of Aspose.CAD for .NET with a free trial. Visit [this link](https://releases.aspose.com/) to get started.

### Q5: How can I get support or connect with the community?
A5: For support and community engagement, visit the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19).

### Q6: How do I **extract OLE from CAD** files without converting to PNG?
A6: Use the `CadImage.OleObjects` collection after loading the DWG; you can iterate through each `OleObject` and save its raw data to a file.

## Conclusion

Anda kini telah melihat cara **mengonversi DWG ke PNG** sambil secara mulus **mengekstrak OLE objects** menggunakan Aspose.CAD untuk .NET. Pendekatan ini menghemat waktu, menghilangkan langkah copy‑paste manual, dan terintegrasi dengan baik ke dalam pipeline otomatis. Jangan ragu untuk bereksperimen dengan format raster lain (JPEG, BMP) atau menjelajahi rangkaian fitur manipulasi CAD yang kaya yang ditawarkan Aspose.

---

**Last Updated:** 2026-03-13  
**Tested With:** Aspose.CAD 24.11 for .NET  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}