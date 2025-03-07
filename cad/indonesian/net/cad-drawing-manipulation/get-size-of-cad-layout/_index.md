---
title: Dapatkan Ukuran Tata Letak CAD di Aspose.CAD untuk .NET
linktitle: Dapatkan Ukuran Tata Letak CAD
second_title: Aspose.CAD .NET - Format File CAD dan BIM
description: Pelajari cara mengambil ukuran tata letak CAD di .NET menggunakan Aspose.CAD. Ikuti panduan langkah demi langkah kami untuk manipulasi file CAD yang efisien.
weight: 14
url: /id/net/cad-drawing-manipulation/get-size-of-cad-layout/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Dapatkan Ukuran Tata Letak CAD di Aspose.CAD untuk .NET

## Perkenalan

Selamat datang di panduan komprehensif tentang cara mendapatkan ukuran tata letak CAD menggunakan Aspose.CAD untuk .NET. Aspose.CAD adalah perpustakaan canggih yang memungkinkan pengembang bekerja dengan file CAD dengan lancar. Dalam tutorial ini, kami akan memandu Anda melalui proses mengambil ukuran tata letak CAD menggunakan contoh praktis dan petunjuk langkah demi langkah.

## Prasyarat

Sebelum kita mendalami tutorialnya, pastikan Anda memiliki prasyarat berikut:

-  Aspose.CAD untuk .NET: Pastikan Anda telah menginstal perpustakaan Aspose.CAD. Anda dapat mengunduhnya dari[Halaman unduhan Aspose.CAD untuk .NET](https://releases.aspose.com/cad/net/).

- File Dokumen: Siapkan file CAD yang ingin Anda kerjakan. Tutorial ini menggunakan "conic_pyramid.dxf" dan "Bottom_plate.dwg" sebagai contoh.

Sekarang, mari kita mulai!

## Impor Namespace

Di proyek .NET Anda, mulailah dengan mengimpor namespace yang diperlukan:

```csharp
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadConsts;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.FileFormats.Cad.CadTables;
using Aspose.CAD.ImageOptions;
```

## Langkah 1: Siapkan Direktori Dokumen

 Tetapkan jalur ke direktori dokumen Anda. Mengganti`"Your Document Directory"` dengan jalur sebenarnya.

```csharp
string MyDir = "Your Document Directory";
```

## Langkah 2: Tentukan Jalur File CAD

Tentukan serangkaian jalur file CAD yang ingin Anda analisis. Dalam contoh ini, kami menggunakan "conic_pyramid.dxf" dan "Bottom_plate.dwg."

```csharp
string[] sourceFilePaths = new[]
{
    MyDir + "conic_pyramid.dxf",
    MyDir + "Bottom_plate.dwg"
};
```

## Langkah 3: Iterasi Melalui File CAD

Ulangi setiap file CAD dan ambil informasi tata letak.

```csharp
foreach (var sourceFilePath in sourceFilePaths)
{
    string extension = Path.GetExtension(sourceFilePath);
    using (CadImage cadImage = (CadImage)Aspose.CAD.Image.Load(sourceFilePath))
    {
        // ... (lanjutkan ke langkah berikutnya)
    }
}
```

## Langkah 4: Dapatkan Tata Letak Tidak Kosong

Tentukan metode pembantu untuk mendapatkan tata letak yang tidak kosong berdasarkan jenis file CAD.

```csharp
private static List<string> GetNotEmptyLayouts(Image cadImage, string extension)
{
    // ... (lanjutkan ke langkah berikutnya)
}
```

## Langkah 5: Dapatkan Tata Letak untuk File DWG

Menerapkan logika untuk mengambil tata letak yang tidak kosong untuk file DWG.

```csharp
private static List<string> GetNotEmptyLayoutsForDwg(CadImage cadImage)
{
    // ... (lanjutkan ke langkah berikutnya)
}
```

## Langkah 6: Dapatkan Tata Letak untuk File DXF

Menerapkan logika untuk mengambil tata letak yang tidak kosong untuk file DXF.

```csharp
private static List<string> GetNotEmptyLayoutsForDxf(CadImage cadImage)
{
    // ... (lanjutkan ke langkah berikutnya)
}
```

## Langkah 7: Ambil Ukuran Tata Letak dan Simpan sebagai Gambar

Selesaikan proses mendapatkan ukuran tata letak dan menyimpannya sebagai gambar.

```csharp
foreach (string layout in layouts)
{
    // ... (lanjutkan ke langkah berikutnya)
}
```

## Kesimpulan

Selamat! Anda telah berhasil mempelajari cara mendapatkan ukuran tata letak CAD menggunakan Aspose.CAD untuk .NET. Tutorial ini mencakup langkah-langkah penting, mulai dari menyiapkan proyek Anda hingga mengambil informasi tata letak dan menyimpannya sebagai gambar. Sekarang Anda dapat menggabungkan pengetahuan ini ke dalam aplikasi .NET Anda untuk manipulasi file CAD yang efisien.

## FAQ

### Q1: Apakah Aspose.CAD kompatibel dengan semua format file CAD?

A1: Ya, Aspose.CAD mendukung berbagai format file CAD, termasuk DWG dan DXF.

### Q2: Dapatkah saya menyesuaikan opsi penyimpanan gambar?

A2: Tentu saja! Anda dapat menyesuaikan pilihan gambar, seperti format dan resolusi, untuk memenuhi kebutuhan spesifik Anda.

### Q3: Di mana saya dapat menemukan dokumentasi tambahan?

 A3: Lihat[Dokumentasi Aspose.CAD](https://reference.aspose.com/cad/net/) untuk informasi rinci dan contoh.

### Q4: Apakah tersedia uji coba gratis?

 A4: Ya, Anda dapat menjelajahi Aspose.CAD dengan a[uji coba gratis](https://releases.aspose.com/).

### Q5; Bagaimana saya bisa mendapatkan dukungan teknis?

 A5: Untuk dukungan teknis, kunjungi[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
