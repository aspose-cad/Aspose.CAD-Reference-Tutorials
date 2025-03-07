---
title: Dukungan 3D untuk DGN V7 di Aspose.CAD untuk .NET
linktitle: Dukungan 3D untuk DGN V7
second_title: Aspose.CAD .NET - Format File CAD dan BIM
description: Buka kekuatan dukungan 3D untuk DGN V7 di Aspose.CAD untuk .NET. Ikuti tutorial langkah demi langkah kami.
weight: 20
url: /id/net/cad-features-and-support/support-of-3d-for-dgn-v7/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Dukungan 3D untuk DGN V7 di Aspose.CAD untuk .NET

## Perkenalan

Selamat datang di tutorial komprehensif kami tentang memanfaatkan dukungan 3D untuk DGN V7 di Aspose.CAD untuk .NET! Aspose.CAD adalah perpustakaan canggih yang memungkinkan pengembang bekerja secara lancar dengan file CAD di aplikasi .NET mereka. Dalam tutorial ini, kita akan mengeksplorasi langkah-langkah untuk memanfaatkan dukungan 3D untuk DGN V7, memberi Anda pengetahuan untuk menyempurnakan proyek terkait CAD Anda.

## Prasyarat

Sebelum masuk ke tutorial, pastikan Anda memiliki prasyarat berikut:

-  Aspose.CAD untuk .NET: Pastikan Anda telah menginstal Aspose.CAD untuk .NET. Jika tidak, Anda dapat mengunduhnya dari[Di Sini](https://releases.aspose.com/cad/net/).

- Lingkungan Pengembangan: Siapkan lingkungan pengembangan yang sesuai, seperti Visual Studio, untuk pengembangan aplikasi .NET.

- Contoh File DGN: Siapkan contoh file DGN untuk pengujian. Anda dapat menggunakan file contoh yang disediakan "Nikon_D90_Camera.dgn."

Sekarang, mari masuk ke langkah-langkah untuk mencapai dukungan 3D untuk DGN V7 menggunakan Aspose.CAD untuk .NET!

## Impor Namespace

Di aplikasi .NET Anda, mulailah dengan mengimpor namespace yang diperlukan:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Dgn;
using Aspose.CAD.ImageOptions;
```

## Langkah 1: Siapkan Direktori Dokumen Anda

 Pastikan Anda telah menyiapkan direktori dokumen di proyek Anda. Mengganti`"Your Document Directory"` dengan jalur sebenarnya ke direktori dokumen Anda.

```csharp
string MyDir = "Your Document Directory";
```

## Langkah 2: Muat File DGN

Muat file DGN yang ada sebagai CadImage menggunakan kode berikut:

```csharp
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";
string outFile = MyDir + "Nikon_D90_Camera.dgn";

using (DgnImage dgnImage = (DgnImage)Image.Load(sourceFilePath))
{
    // Kode Anda untuk diproses lebih lanjut ada di sini
}
```

## Langkah 3: Konfigurasikan Opsi Ekspor PDF

Siapkan opsi untuk mengekspor ke PDF, tentukan opsi rasterisasi vektor seperti dimensi halaman, penskalaan tata letak otomatis, warna latar belakang, dan tata letak yang akan diekspor.

```csharp
var options = new PdfOptions
{
    VectorRasterizationOptions = new CadRasterizationOptions
    {
        PageWidth = 1500,
        PageHeight = 1500,
        AutomaticLayoutsScaling = true,
        BackgroundColor = Color.Black,
        Layouts = new string[] { "1", "2", "3", "9" } // Hanya ekspor tampilan tertentu
    }
};
```

## Langkah 4: Simpan Gambar Raster

Simpan file DGN sebagai gambar raster dengan opsi yang dikonfigurasi.

```csharp
dgnImage.Save(outFile, options);
```

## Kesimpulan

Selamat! Anda telah berhasil menggunakan Aspose.CAD untuk .NET untuk mengekspor file DGN dengan dukungan 3D ke gambar raster. Tutorial ini telah membekali Anda dengan langkah-langkah penting untuk mengintegrasikan fungsi ini ke dalam proyek CAD Anda.

## FAQ

### Q1: Dapatkah saya menggunakan Aspose.CAD untuk .NET dengan format file CAD lainnya?

A1: Ya, Aspose.CAD mendukung berbagai format file CAD, termasuk DWG dan DXF.

### Q2: Bagaimana cara menangani pengecualian saat bekerja dengan Aspose.CAD?

A2: Bungkus kode Anda dalam blok coba-tangkap, seperti yang ditunjukkan dalam contoh yang diberikan, untuk menangani pengecualian dengan baik.

### Q3: Apakah Aspose.CAD cocok untuk proyek komersial?

 A3: Tentu saja! Anda dapat membeli Aspose.CAD untuk .NET[Di Sini](https://purchase.aspose.com/buy).

### Q4: Bisakah saya mencoba Aspose.CAD untuk .NET sebelum membeli?

A4: Tentu saja! Jelajahi uji coba gratis[Di Sini](https://releases.aspose.com/).

### Q5: Di mana saya dapat menemukan dukungan komunitas untuk Aspose.CAD untuk .NET?

 A5: Kunjungi forum komunitas[Di Sini](https://forum.aspose.com/c/cad/19).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
