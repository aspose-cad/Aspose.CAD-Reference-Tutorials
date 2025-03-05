---
title: Mengekspor Gambar CAD ke Format SVG - Panduan Aspose.CAD
linktitle: Mengekspor Gambar CAD ke Format SVG
second_title: Aspose.CAD .NET - Format File CAD dan BIM
description: Jelajahi proses mulus dalam mengekspor gambar CAD ke SVG menggunakan Aspose.CAD untuk .NET. Tingkatkan pengembangan CAD Anda dengan fleksibilitas dan penyesuaian.
type: docs
weight: 15
url: /id/net/advanced-export-techniques/exporting-cad-drawings-to-svg/
---
## Perkenalan

Dalam dunia CAD (Computer-Aided Design) yang dinamis, kemampuan mengekspor gambar ke berbagai format adalah keterampilan yang sangat penting. SVG (Scalable Vector Graphics) adalah salah satu format yang mendapatkan popularitas karena skalabilitas dan fleksibilitasnya. Dalam tutorial ini, kita akan menjelajahi cara mengekspor gambar CAD ke SVG menggunakan pustaka Aspose.CAD untuk .NET yang canggih.

## Prasyarat

Sebelum masuk ke tutorial, pastikan Anda memiliki prasyarat berikut:

-  Aspose.CAD untuk Perpustakaan .NET: Unduh dan instal perpustakaan Aspose.CAD untuk .NET. Anda dapat menemukan perpustakaan[Di Sini](https://releases.aspose.com/cad/net/).

- Lingkungan Pengembangan: Siapkan lingkungan pengembangan yang sesuai dengan Visual Studio atau alat pengembangan .NET lainnya.

## Impor Namespace

Untuk memulai, impor namespace yang diperlukan ke dalam proyek Anda:

```csharp
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## Langkah 1: Atur Direktori Dokumen

```csharp
// Jalur ke direktori dokumen.
string MyDir = "Your Document Directory";
```

## Langkah 2: Muat Gambar CAD

```csharp
using (Image image = Image.Load(MyDir + "sample.dwg"))
{
```

## Langkah 3: Konfigurasikan Opsi Ekspor SVG

```csharp
    var options = new SvgOptions();
    options.ColorType = SvgColorMode.Grayscale;
    options.TextAsShapes = true;
```

## Langkah 4: Simpan File SVG

```csharp
    image.Save(MyDir + "sample.svg", options);
}
```

Dengan mengikuti langkah-langkah sederhana ini, Anda dapat mengekspor gambar CAD ke SVG dengan lancar menggunakan Aspose.CAD untuk .NET. Perpustakaan memberikan opsi fleksibilitas dan penyesuaian, memungkinkan Anda menyesuaikan keluaran sesuai dengan kebutuhan Anda.

## Kesimpulan

Kesimpulannya, Aspose.CAD untuk .NET menyederhanakan proses mengekspor gambar CAD ke SVG. API intuitif dan fitur-fiturnya yang tangguh menjadikannya alat yang berharga bagi pengembang yang bekerja dengan aplikasi CAD.

## FAQ

### Q1: Apakah Aspose.CAD kompatibel dengan semua format CAD?

A1: Aspose.CAD mendukung berbagai format CAD, termasuk DWG dan DXF, memastikan kompatibilitas luas.

### Q2: Dapatkah saya menyesuaikan mode warna saat mengekspor ke SVG?

A2: Ya, Aspose.CAD memungkinkan Anda memilih mode warna, memberikan fleksibilitas dalam output.

### Q3: Apakah lisensi sementara tersedia untuk tujuan pengujian?

 A3: Ya, Anda bisa mendapatkan lisensi sementara[Di Sini](https://purchase.aspose.com/temporary-license/) untuk evaluasi.

### Q4: Di mana saya dapat menemukan dokumentasi terperinci untuk Aspose.CAD?

 A4: Dokumentasi tersedia[Di Sini](https://reference.aspose.com/cad/net/).

### Q5: Bagaimana saya bisa mendapatkan dukungan atau mengajukan pertanyaan terkait Aspose.CAD?

 A5: Kunjungi forum komunitas[Di Sini](https://forum.aspose.com/c/cad/19) untuk dukungan dan diskusi.