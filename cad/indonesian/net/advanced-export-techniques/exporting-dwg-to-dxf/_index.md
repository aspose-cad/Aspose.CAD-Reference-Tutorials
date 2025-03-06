---
title: Mengekspor DWG ke Format DXF dalam C# - Tutorial Aspose.CAD
linktitle: Mengekspor DWG ke Format DXF di C#
second_title: Aspose.CAD .NET - Format File CAD dan BIM
description: Buka kunci manipulasi file CAD di C# dengan Aspose.CAD. Belajar mengekspor DWG ke DXF dengan mudah. Ikuti panduan langkah demi langkah kami untuk integrasi yang lancar.
weight: 10
url: /id/net/advanced-export-techniques/exporting-dwg-to-dxf/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Mengekspor DWG ke Format DXF dalam C# - Tutorial Aspose.CAD

## Perkenalan

Jika Anda seorang pengembang .NET yang mencari solusi ampuh untuk memanipulasi file CAD, Aspose.CAD adalah alat pilihan Anda. Dalam tutorial langkah demi langkah ini, kami akan memandu Anda melalui proses mengekspor file DWG ke format DXF menggunakan C# dengan Aspose.CAD.

## Prasyarat

Sebelum masuk ke tutorial, pastikan Anda memiliki prasyarat berikut:

1.  Perpustakaan Aspose.CAD: Unduh dan instal perpustakaan Aspose.CAD dari[Link ini](https://releases.aspose.com/cad/net/).

2. Lingkungan Pengembangan: Siapkan lingkungan pengembangan C#, seperti Visual Studio.

3. Contoh File DWG: Siapkan contoh file DWG yang ingin Anda ekspor. Untuk tutorial ini, kita akan menggunakan file bernama "Line.dwg" di direktori "Direktori Dokumen Anda".

## Impor Namespace

Dalam proyek C# Anda, sertakan namespace yang diperlukan untuk bekerja dengan Aspose.CAD:

```csharp
using Aspose.CAD.FileFormats.Cad;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## Langkah 1: Muat File DWG

Mulailah dengan memuat file DWG ke aplikasi C# Anda. Berikut cuplikan kode untuk mencapai hal ini:

```csharp
string MyDir = "Your Document Directory";
string inputFile = MyDir + "Line.dwg";
using (var cadImage = (CadImage)Image.Load(inputFile))
{
    //Kode Anda untuk langkah selanjutnya akan ditempatkan di sini
}
```

## Langkah 2: Simpan sebagai DXF

Setelah file DWG dimuat, langkah selanjutnya adalah menyimpannya sebagai file DXF. Tambahkan kode berikut dalam blok penggunaan sebelumnya:

```csharp
string outFile = MyDir + "Line_19.2.dxf";
cadImage.Save(outFile);
```

## Kesimpulan

Selamat! Anda telah berhasil mengekspor file DWG ke format DXF menggunakan Aspose.CAD di C#. Proses sederhana namun kuat ini membuka banyak kemungkinan manipulasi file CAD dalam aplikasi Anda.

## FAQ

### Q1: Apakah Aspose.CAD kompatibel dengan format file CAD terbaru?

A1: Ya, Aspose.CAD diperbarui secara berkala untuk memastikan kompatibilitas dengan format file CAD terbaru.

### Q2: Bisakah saya menggunakan Aspose.CAD dalam proyek komersial saya?

 A2: Tentu saja! Aspose.CAD hadir dengan opsi lisensi untuk penggunaan pribadi dan komersial. Mengunjungi[Link ini](https://purchase.aspose.com/buy) untuk detailnya.

### Q3: Apakah tersedia uji coba gratis?

 A3: Ya, Anda dapat menjelajahi Aspose.CAD dengan uji coba gratis. Mengunjungi[Link ini](https://releases.aspose.com/) untuk memulai.

### Q4: Di mana saya dapat menemukan dokumentasi terperinci untuk Aspose.CAD?

 A4: Lihat dokumentasi di[Link ini](https://reference.aspose.com/cad/net/) untuk panduan komprehensif.

### Q5: Butuh bantuan atau memiliki pertanyaan spesifik?

 A5: Kunjungi forum komunitas Aspose.CAD[Di Sini](https://forum.aspose.com/c/cad/19)untuk bantuan ahli dan dukungan masyarakat.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
