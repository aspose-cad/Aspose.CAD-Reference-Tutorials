---
title: Mengonversi DWG ke PDF dengan Koordinat di C# - Tutorial Aspose.CAD
linktitle: Mengonversi DWG ke PDF dengan Koordinat di C#
second_title: Aspose.CAD .NET - Format File CAD dan BIM
description: Pelajari cara mengonversi DWG ke PDF dengan koordinat tertentu di C# menggunakan Aspose.CAD. Ikuti panduan langkah demi langkah kami untuk konversi file CAD yang tepat dan efisien.
type: docs
weight: 11
url: /id/net/conversion-and-export/converting-dwg-to-pdf-with-coordinates/
---
## Perkenalan

Selamat datang di tutorial komprehensif tentang mengonversi file DWG ke PDF dengan koordinat tertentu menggunakan Aspose.CAD untuk .NET. Aspose.CAD adalah perpustakaan canggih yang memungkinkan pengembang bekerja dengan format file CAD dalam aplikasi .NET mereka dengan lancar. Dalam tutorial ini, kami akan memandu Anda melalui proses mengonversi file DWG ke PDF sambil memberikan koordinat tertentu untuk meningkatkan presisi.

## Prasyarat

Sebelum kita mulai, pastikan Anda memiliki prasyarat berikut:

- Perpustakaan Aspose.CAD: Unduh dan instal perpustakaan Aspose.CAD untuk .NET. Anda dapat menemukan perpustakaan[Di Sini](https://releases.aspose.com/cad/net/).

- Lingkungan Pengembangan: Pastikan Anda telah menyiapkan lingkungan pengembangan yang kompatibel, termasuk Visual Studio atau IDE pilihan lainnya.

- File DWG: Siapkan file DWG untuk dikonversi. Anda dapat menggunakan file contoh yang disediakan atau file DWG khusus Anda.

## Impor Namespace

Dalam proyek C# Anda, impor namespace yang diperlukan:

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

Mari kita pecahkan kodenya menjadi panduan langkah demi langkah untuk pemahaman yang lebih baik:

## Langkah 1: Tentukan Direktori Dokumen

```csharp
string MyDir = "Your Document Directory";
```

## Langkah 2: Atur Jalur File Sumber DWG

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

## Langkah 4: Tentukan Koordinat dan Area Pandang

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

## Langkah 5: Terapkan Pengaturan Area Pandang

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

## Kesimpulan

Selamat! Anda telah berhasil mengonversi file DWG ke PDF dengan koordinat yang ditentukan menggunakan Aspose.CAD untuk .NET. Tutorial ini mencakup langkah-langkah penting dan memberikan panduan yang jelas bagi pengembang.

## FAQ

### Q1: Bisakah saya menggunakan Aspose.CAD dengan format file CAD lainnya?

A1: Ya, Aspose.CAD mendukung berbagai format CAD, termasuk DWG, DXF, DWF, dan banyak lagi.

### Q2: Bagaimana cara menangani kesalahan selama proses konversi?

A2: Menerapkan mekanisme penanganan kesalahan menggunakan blok coba-tangkap untuk menangkap dan mengelola pengecualian.

### Q3: Apakah Aspose.CAD cocok untuk lingkungan Windows dan Linux?

A3: Ya, Aspose.CAD kompatibel dengan platform Windows dan Linux.

### Q4: Dapatkah saya menyesuaikan keluaran PDF lebih lanjut?

A4: Tentu saja! Jelajahi opsi ekstensif yang disediakan oleh Aspose.CAD untuk menyesuaikan keluaran PDF dengan kebutuhan spesifik Anda.

### Q5: Di mana saya bisa mendapatkan dukungan tambahan atau diskusi komunitas?

A5: Kunjungi[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19) untuk dukungan dan diskusi komunitas.