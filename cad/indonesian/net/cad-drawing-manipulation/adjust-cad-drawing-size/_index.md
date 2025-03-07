---
title: Menyesuaikan Ukuran Gambar CAD di Aspose.CAD untuk .NET
linktitle: Menyesuaikan Ukuran Gambar CAD
second_title: Aspose.CAD .NET - Format File CAD dan BIM
description: Pelajari cara menyesuaikan ukuran gambar CAD dengan mudah di .NET menggunakan Aspose.CAD. Ikuti panduan langkah demi langkah kami untuk mengubah ukuran dengan lancar.
weight: 10
url: /id/net/cad-drawing-manipulation/adjust-cad-drawing-size/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Menyesuaikan Ukuran Gambar CAD di Aspose.CAD untuk .NET

## Perkenalan

Apakah Anda ingin menyesuaikan ukuran gambar CAD di aplikasi .NET Anda dengan lancar? Aspose.CAD untuk .NET memberikan solusi tangguh, memungkinkan Anda menangani pengubahan ukuran gambar CAD dengan mudah. Dalam tutorial ini, kami akan memandu Anda melalui prosesnya, menguraikan setiap langkah untuk memastikan Anda memahami seluk-beluk mengubah ukuran gambar CAD menggunakan Aspose.CAD.

## Prasyarat

Sebelum kita mendalami tutorialnya, pastikan Anda memiliki prasyarat berikut:

- Aspose.CAD untuk .NET Library: Unduh dan instal perpustakaan dari[Halaman unduhan Aspose.CAD untuk .NET](https://releases.aspose.com/cad/net/).
- Contoh Gambar CAD: Pastikan Anda memiliki contoh file gambar CAD (misalnya, "sample.dwg") di direktori dokumen Anda.

## Impor Namespace

Mulailah dengan mengimpor namespace yang diperlukan ke dalam aplikasi .NET Anda. Langkah ini penting untuk mengakses fungsionalitas yang disediakan oleh Aspose.CAD untuk .NET.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Langkah 1: Muat Gambar CAD

Mulailah dengan memuat gambar CAD ke dalam instance kelas Aspose.CAD.Image. Pastikan Anda memiliki jalur file yang benar untuk gambar sampel Anda.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "sample.dwg";

// Muat gambar CAD dalam contoh Gambar
using (var image = Aspose.CAD.Image.Load(sourceFilePath))
{
    // Kode Anda di sini...
}
```

## Langkah 2: Buat BmpOptions

Buat instance kelas BmpOptions, yang bertanggung jawab untuk menentukan opsi saat menyimpan gambar CAD sebagai file BMP.

```csharp
Aspose.CAD.ImageOptions.BmpOptions bmpOptions = new Aspose.CAD.ImageOptions.BmpOptions();
```

## Langkah 3: Tetapkan Opsi CadRasterization

Buat instance kelas CadRasterizationOptions dan konfigurasikan propertinya untuk rasterisasi vektor.

```csharp
Aspose.CAD.ImageOptions.CadRasterizationOptions cadRasterizationOptions = new Aspose.CAD.ImageOptions.CadRasterizationOptions();
bmpOptions.VectorRasterizationOptions = cadRasterizationOptions;
```

## Langkah 4: Tetapkan Properti UnitType

Atur properti UnitType dari CadRasterizationOptions untuk menentukan jenis unit yang akan diubah ukurannya. Dalam contoh ini, diatur ke Centimeter.

```csharp
cadRasterizationOptions.UnitType = Aspose.CAD.ImageOptions.UnitType.Centimeter;
```

## Langkah 5: Tetapkan Properti Tata Letak

Tentukan tata letak yang ingin Anda sertakan dalam gambar yang diubah ukurannya dengan mengatur properti Tata Letak.

```csharp
cadRasterizationOptions.Layouts = new string[] { "Model" };
```

## Langkah 6: Ekspor ke BMP

Terakhir, simpan tata letak yang diubah ukurannya sebagai file BMP menggunakan metode Simpan.

```csharp
string outPath = sourceFilePath + ".bmp";
image.Save(outPath, bmpOptions);
```

Sekarang Anda telah berhasil menyesuaikan ukuran gambar CAD Anda menggunakan Aspose.CAD untuk .NET!

## Kesimpulan

Dalam tutorial ini, kita mempelajari proses mengubah ukuran gambar CAD di .NET menggunakan Aspose.CAD. Dengan mengikuti langkah-langkah ini, Anda dapat dengan mudah mengintegrasikan fungsi ini ke dalam aplikasi Anda, sehingga memberikan pengalaman pengguna yang lancar.

## FAQ

### Q1: Apakah Aspose.CAD untuk .NET kompatibel dengan semua format CAD?

 A1: Aspose.CAD untuk .NET mendukung berbagai format CAD, termasuk DWG, DXF, DWF, dan banyak lagi. Periksalah[dokumentasi](https://reference.aspose.com/cad/net/) untuk daftar lengkapnya.

### Q2: Dapatkah saya mengubah ukuran beberapa tata letak secara bersamaan?

A2: Ya, Anda dapat mengubah ukuran beberapa tata letak dengan menyesuaikan larik tata letak di CadRasterizationOptions.

### Q3: Di mana saya bisa mendapatkan dukungan untuk Aspose.CAD untuk .NET?

 A3: Kunjungi[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19) untuk dukungan dan bantuan masyarakat.

### Q4: Apakah tersedia uji coba gratis?

 A4: Ya, Anda dapat menjelajahi a[uji coba gratis](https://releases.aspose.com/) untuk mengevaluasi fitur Aspose.CAD untuk .NET.

### Q5: Bagaimana cara mendapatkan lisensi sementara Aspose.CAD untuk .NET?

 A5: Dapatkan lisensi sementara untuk tujuan pengujian[Di Sini](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
