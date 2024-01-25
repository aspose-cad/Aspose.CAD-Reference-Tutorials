---
title: Mengekspor Objek OLE dari File DWG - Tutorial Aspose.CAD
linktitle: Mengekspor Objek OLE dari File DWG
second_title: Aspose.CAD .NET - Format File CAD dan BIM
description: Jelajahi panduan langkah demi langkah tentang mengekspor objek OLE dari file DWG menggunakan Aspose.CAD untuk .NET. Tingkatkan keterampilan manipulasi file CAD Anda dengan mudah.
type: docs
weight: 12
url: /id/net/advanced-export-techniques/exporting-ole-objects-from-dwg/
---
## Perkenalan

Apakah Anda ingin mengekstrak objek OLE dari file DWG dengan mudah? Aspose.CAD untuk .NET hadir untuk menyederhanakan proses untuk Anda. Dalam tutorial ini, kami akan memandu Anda mengekspor objek OLE langkah demi langkah, memastikan Anda memanfaatkan perpustakaan .NET yang kuat ini. 

## Prasyarat

Sebelum kita mendalami tutorialnya, pastikan Anda memiliki prasyarat berikut:

-  Aspose.CAD untuk .NET Library: Pastikan Anda telah menginstal perpustakaan. Anda dapat mengunduhnya dari[Halaman unduhan Aspose.CAD untuk .NET](https://releases.aspose.com/cad/net/).

-  Direktori Dokumen: Siapkan direktori tempat file DWG Anda disimpan. Mengganti`"Your Document Directory"` dalam cuplikan kode yang disediakan dengan jalur sebenarnya.

## Impor Namespace

Dalam proyek .NET Anda, Anda harus mengimpor namespace yang diperlukan untuk memanfaatkan fungsionalitas Aspose.CAD. Gunakan cuplikan kode berikut:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## Langkah 1: Atur Direktori Dokumen

```csharp
string MyDir = "Your Document Directory";
```

 Mengganti`"Your Document Directory"` dengan jalur tempat file DWG Anda berada.

## Langkah 2: Tentukan File DWG

```csharp
string[] files = new string[] { "D ZD junior D10m H2m.dwg", "ZD - Senior D6m H2m45.dwg" };
```

Buat daftar file DWG yang ingin Anda proses dalam array.

## Langkah 3: Konfigurasikan Opsi Ekspor

```csharp
PngOptions pngOptions = new PngOptions { };
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
pngOptions.VectorRasterizationOptions = rasterizationOptions;
rasterizationOptions.Layouts = new string[] { "Layout1" };
```

Sesuaikan opsi ekspor berdasarkan kebutuhan Anda. Dalam contoh ini, kami mengonfigurasi ekspor PNG dengan tata letak tertentu.

## Langkah 4: Ulangi File dan Ekspor

```csharp
foreach (string file in files)
{
    using (CadImage cadImage = (CadImage)Image.Load(MyDir + file))
    {
        cadImage.Save(MyDir + file + "_out.png", pngOptions);
    }
}
```

Ulangi file DWG yang ditentukan, muat masing-masing file, dan simpan file PNG yang diekspor dengan opsi yang ditentukan.

## Kesimpulan

Selamat! Anda telah berhasil mengekspor objek OLE dari file DWG menggunakan Aspose.CAD untuk .NET. Pustaka yang kuat ini menyederhanakan tugas-tugas kompleks, memberikan efisiensi dan fleksibilitas dalam manipulasi file CAD.

## FAQ

### Q1: Apakah Aspose.CAD untuk .NET cocok untuk file CAD junior dan senior?

A1: Ya, Aspose.CAD untuk .NET serbaguna dan dapat menangani berbagai macam file CAD, termasuk varian junior dan senior.

### Q2: Dapatkah saya menyesuaikan opsi ekspor untuk tata letak yang berbeda?

A2: Tentu saja! Seperti yang ditunjukkan dalam tutorial, Anda dapat menyesuaikan opsi ekspor, termasuk tata letak, untuk memenuhi kebutuhan spesifik Anda.

### Q3: Di mana saya dapat menemukan dokumentasi terperinci untuk Aspose.CAD untuk .NET?

 A3: Jelajahi[Aspose.CAD untuk dokumentasi .NET](https://reference.aspose.com/cad/net/) untuk informasi mendalam dan contoh.

### Q4: Apakah tersedia uji coba gratis?

 A4: Ya, Anda dapat merasakan kemampuan Aspose.CAD untuk .NET dengan uji coba gratis. Mengunjungi[Link ini](https://releases.aspose.com/) untuk memulai.

### Q5: Bagaimana saya bisa mendapatkan dukungan atau terhubung dengan komunitas?

 A5: Untuk dukungan dan keterlibatan komunitas, kunjungi[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19).