---
title: Merender Dokumen DWG di C# - Panduan Aspose.CAD
linktitle: Merender Dokumen DWG di C#
second_title: Aspose.CAD .NET - Format File CAD dan BIM
description: Pelajari cara merender dokumen DWG di C# menggunakan Aspose.CAD. Panduan langkah demi langkah ini mencakup impor, konfigurasi, dan penyimpanan dengan contoh kode.
weight: 17
url: /id/net/image-manipulation-and-rendering/rendering-dwg-documents/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Merender Dokumen DWG di C# - Panduan Aspose.CAD

## Perkenalan

Selamat datang di panduan komprehensif tentang merender dokumen DWG di C# menggunakan Aspose.CAD. Baik Anda seorang pengembang berpengalaman atau baru memulai dengan .NET, tutorial ini akan memandu Anda melalui proses memanfaatkan Aspose.CAD untuk merender file DWG secara efisien. Aspose.CAD adalah API canggih yang menyediakan fungsionalitas tangguh untuk bekerja dengan format file CAD, menjadikannya pilihan tepat bagi pengembang yang menangani file DWG.

## Prasyarat

Sebelum masuk ke tutorial, pastikan Anda memiliki prasyarat berikut:

- Pengetahuan dasar bahasa pemrograman C#.
- Visual Studio diinstal pada mesin Anda.
-  Pustaka Aspose.CAD terintegrasi ke dalam proyek Anda. Anda dapat mengunduhnya dari[Di Sini](https://releases.aspose.com/cad/net/).
- Contoh file DWG, seperti "Bottom_plate.dwg," untuk mengikuti contohnya.

## Impor Namespace

Untuk memulai, pastikan untuk mengimpor namespace yang diperlukan di awal kode C# Anda:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
using Aspose.CAD.FileFormats.Cad.CadTables;
using Aspose.CAD.FileFormats.Cad;
```

Sekarang, mari kita bagi contoh yang diberikan menjadi beberapa langkah:

## Langkah 1: Muat File DWG

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Bottom_plate.dwg";
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Kode Anda untuk memuat file DWG ada di sini.
}
```

## Langkah 2: Konfigurasikan Opsi Rasterisasi

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.Layouts = new string[] { "Model" };
rasterizationOptions.NoScaling = true;
//Konfigurasi rasterisasi tambahan dapat ditambahkan di sini.
```

## Langkah 3: Tentukan Wilayah yang Akan Digambar

```csharp
Point topLeft = new Point(6156, 7053);
double width = 3108;
double height = 2489;
```

## Langkah 4: Buat Area Pandang Baru

```csharp
CadVportTableObject newView = new CadVportTableObject();
newView.Name.Value = "*Active";
newView.CenterPoint.X = topLeft.X + width / 2f;
newView.CenterPoint.Y = topLeft.Y - height / 2f;
newView.ViewHeight.Value = height;
newView.ViewAspectRatio.Value = width / height;
```

## Langkah 5: Ganti Area Pandang Aktif

```csharp
for (int i = 0; i < cadImage.ViewPorts.Count; i++)
{
    CadVportTableObject currentView = (CadVportTableObject)(cadImage.ViewPorts[i]);
    if ((currentView.Name.Value == null && cadImage.ViewPorts.Count == 1) ||
    string.Equals(currentView.Name.Value.ToLowerInvariant(), "*active"))
    {
        cadImage.ViewPorts[i] = newView;
        break;
    }
}
```

## Langkah 6: Konfigurasikan Opsi PDF

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Langkah 7: Simpan DWG yang Dirender sebagai PDF

```csharp
cadImage.Save(MyDir, pdfOptions);
```

## Kesimpulan

Selamat! Anda telah berhasil merender dokumen DWG ke PDF menggunakan Aspose.CAD di C#. Jangan ragu untuk menjelajahi lebih banyak fitur dan menyesuaikan kode berdasarkan kebutuhan spesifik Anda.

## FAQ

### Q1: Bisakah saya menggunakan Aspose.CAD dengan format file CAD lainnya?

A1: Ya, Aspose.CAD mendukung berbagai format CAD, termasuk DWG, DXF, DWF, dan banyak lagi.

### Q2: Apakah Aspose.CAD kompatibel dengan .NET Core?

A2: Ya, Aspose.CAD kompatibel dengan .NET Framework dan .NET Core.

### Q3: Bagaimana cara menangani tata letak yang berbeda dalam file DWG?

 A3: Anda dapat menentukan tata letak yang diinginkan di`Layouts` milik`CadRasterizationOptions`.

### Q4: Apakah ada pertimbangan lisensi untuk menggunakan Aspose.CAD?

 A4: Untuk detail lisensi, kunjungi[Di Sini](https://purchase.aspose.com/buy).

### Q5: Di mana saya bisa mendapatkan dukungan tambahan?

A5: Kunjungi[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19) untuk dukungan dan diskusi komunitas.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
