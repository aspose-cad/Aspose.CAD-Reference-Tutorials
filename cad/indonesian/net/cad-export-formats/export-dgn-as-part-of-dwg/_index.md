---
title: Ekspor DGN sebagai Bagian dari DWG di Aspose.CAD untuk .NET
linktitle: Ekspor DGN sebagai Bagian dari DWG
second_title: Aspose.CAD .NET - Format File CAD dan BIM
description: Pelajari cara mengekspor DGN sebagai bagian dari DWG di Aspose.CAD untuk .NET. Ikuti panduan langkah demi langkah kami untuk integrasi yang lancar.
type: docs
weight: 11
url: /id/net/cad-export-formats/export-dgn-as-part-of-dwg/
---
## Perkenalan

Dalam dunia pengembangan .NET, Aspose.CAD menonjol sebagai perpustakaan yang kuat untuk bekerja dengan file Computer-Aided Design (CAD). Tutorial ini akan memandu Anda melalui proses mengekspor file DGN (Desain) sebagai bagian dari file DWG (Gambar) menggunakan Aspose.CAD untuk .NET. Baik Anda seorang pengembang berpengalaman atau baru memulai, panduan langkah demi langkah ini akan membantu Anda memanfaatkan kemampuan Aspose.CAD untuk mencapai tugas khusus ini secara efisien.

## Prasyarat

Sebelum masuk ke tutorial, pastikan Anda memiliki prasyarat berikut:

-  Aspose.CAD untuk .NET: Pastikan Anda telah menginstal perpustakaan Aspose.CAD untuk .NET. Anda dapat mengunduhnya[Di Sini](https://releases.aspose.com/cad/net/).

- Lingkungan Pengembangan: Siapkan lingkungan pengembangan .NET pilihan Anda, seperti Visual Studio.

- Pengetahuan Dasar C#: Biasakan diri Anda dengan bahasa pemrograman C#.

## Impor Namespace

Dalam proyek C# Anda, sertakan namespace yang diperlukan untuk mengakses fungsionalitas Aspose.CAD. Tambahkan arahan penggunaan berikut di awal file kode Anda:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

Sekarang, mari kita bagi kode yang diberikan menjadi beberapa langkah:

## Langkah 1: Tentukan Jalur File

```csharp
//Jalur file masukan dan keluaran
string fileName = "BlockRefDgn.dwg";
string outPath = fileName + ".pdf";
```

## Langkah 2: Buat Instance PdfOptions

```csharp
// Buat instance kelas PdfOptions untuk mengekspor DWG ke PDF
PdfOptions exportOptions = new PdfOptions();
```

## Langkah 3: Muat File DWG

```csharp
// Muat file DWG yang ada sebagai gambar dan konversikan ke tipe CadImage
using (CadImage cadImage = (CadImage)Image.Load(fileName))
```

## Langkah 4: Iterasi Melalui Entitas

```csharp
// Ulangi setiap entitas di dalam file DWG
foreach (CadBaseEntity baseEntity in cadImage.Entities)
```

## Langkah 5: Periksa Jenis Entitas

```csharp
// Periksa apakah entitas tersebut merupakan definisi gambar
if (baseEntity.TypeName == CadEntityTypeName.DGNUNDERLAY)
```

## Langkah 6: Dapatkan Jalur Underlay

```csharp
// Jika itu adalah definisi gambar, dapatkan referensi eksternal ke objek tersebut
CadDgnUnderlay dgnFile = (CadDgnUnderlay)baseEntity;
Console.WriteLine(dgnFile.UnderlayPath);
```

## Langkah 7: Tentukan Opsi Rasterisasi

```csharp
// Tentukan pengaturan untuk objek CadRasterizationOptions
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

## Langkah 8: Ekspor DWG ke PDF

```csharp
// Ekspor DWG ke PDF dengan memanggil metode Simpan
cadImage.Save(outPath, exportOptions);
```

## Kesimpulan

Selamat! Anda telah berhasil menjalani proses mengekspor file DGN sebagai bagian dari file DWG menggunakan Aspose.CAD untuk .NET. Tutorial ini telah memberi Anda langkah-langkah dasar dan cuplikan kode untuk mencapai tugas khusus ini dengan lancar.

## FAQ

### Q1: Dapatkah saya menggunakan Aspose.CAD untuk .NET dalam proyek komersial saya?
 A1: Ya, Anda bisa. Mengunjungi[Di Sini](https://purchase.aspose.com/buy) untuk mengeksplorasi opsi lisensi.

### Q2: Apakah ada batasan ukuran file DWG yang dapat saya proses?
A2: Aspose.CAD mendukung penanganan file DWG berukuran besar, namun batasan perangkat keras mungkin berlaku.

### Q3: Apakah ada versi uji coba yang tersedia?
A3: Ya, Anda bisa mendapatkan uji coba gratis[Di Sini](https://releases.aspose.com/).

### Q4: Bagaimana cara mendapatkan lisensi sementara?
 A4: Lisensi sementara dapat diperoleh[Di Sini](https://purchase.aspose.com/temporary-license/).

### Q5: Dimana saya bisa mencari bantuan jika saya menemui masalah?
 A5: Anda dapat mengunjungi forum Aspose.CAD[Di Sini](https://forum.aspose.com/c/cad/19) untuk dukungan.