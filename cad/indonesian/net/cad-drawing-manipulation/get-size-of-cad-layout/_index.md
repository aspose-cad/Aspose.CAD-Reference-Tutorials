---
date: 2026-03-21
description: Pelajari cara mendapatkan ukuran tata letak CAD di .NET menggunakan Aspose.CAD.
  Ikuti panduan langkah demi langkah kami untuk manipulasi file CAD yang efisien.
linktitle: Get Size of CAD Layout
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Dapatkan Ukuran Tata Letak CAD di Aspose.CAD untuk .NET
url: /id/net/cad-drawing-manipulation/get-size-of-cad-layout/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Mendapatkan Ukuran Layout CAD di Aspose.CAD untuk .NET

## Pendahuluan

Dalam tutorial komprehensif ini Anda akan menemukan **cara mendapatkan ukuran layout CAD** menggunakan pustaka Aspose.CAD untuk .NET. Baik Anda sedang membangun penampil CAD, menghasilkan thumbnail, atau memerlukan dimensi layout yang tepat untuk pemrosesan lanjutan, mengetahui ukuran pasti setiap layout sangat penting. Kami akan membimbing Anda melalui seluruh alur kerja—dari memuat gambar hingga mengekstrak dimensi layout dan secara opsional menyimpannya sebagai gambar—sehingga Anda dapat mengintegrasikan kemampuan ini ke dalam aplikasi Anda dengan percaya diri.

## Jawaban Cepat
- **Apa arti “mendapatkan ukuran layout CAD”?** Itu berarti mengambil lebar dan tinggi (dalam satuan gambar) dari setiap layout yang tidak kosong dalam file CAD.  
- **Pustaka mana yang mendukung ini?** Aspose.CAD untuk .NET menyediakan API sederhana untuk mengakses informasi layout.  
- **Apakah saya memerlukan lisensi?** Versi percobaan gratis dapat digunakan untuk evaluasi; lisensi komersial diperlukan untuk penggunaan produksi.  
- **Format yang didukung?** DWG, DXF, dan banyak format CAD/BIM lainnya didukung sepenuhnya.  
- **Waktu implementasi tipikal?** Sekitar 10‑15 menit untuk rutinitas pengambilan ukuran dasar.

## Apa itu “mendapatkan ukuran layout CAD”?
Mendapatkan ukuran layout CAD berarti mengekstrak ekstensi geometris dari setiap layout (paper space) yang didefinisikan dalam sebuah gambar CAD. Ekstensi ini dinyatakan dalam satuan asli gambar (biasanya milimeter atau inci) dan berguna untuk tugas seperti penskalaan, pencetakan, atau pembuatan gambar pratinjau.

## Mengapa mengambil ukuran layout CAD dengan Aspose.CAD?
- **Tidak memerlukan perangkat lunak CAD** – Berjalan sepenuhnya di sisi server.  
- **Lintas‑platform** – Berfungsi dengan .NET Framework, .NET Core, dan .NET 5/6+.  
- **Pengukuran akurat** – Mengembalikan ekstensi tepat sebagaimana disimpan dalam file, menghindari parsing manual.  
- **Integrasi mudah** – Panggilan API sederhana cocok secara alami dengan proyek C# yang ada.

## Prasyarat

Sebelum kita masuk ke kode, pastikan Anda memiliki hal‑hal berikut:

- Aspose.CAD untuk .NET terpasang. Anda dapat mengunduhnya dari [halaman unduhan Aspose.CAD untuk .NET](https://releases.aspose.com/cad/net/).
- Satu atau lebih file CAD (DWG, DXF, dll.) yang ingin Anda analisis. Panduan ini menggunakan `conic_pyramid.dxf` dan `Bottom_plate.dwg` sebagai contoh file.

## Mengimpor Namespace

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

## Langkah 1: Menyiapkan Direktori Dokumen

Tentukan folder yang berisi file CAD Anda. Ganti placeholder dengan jalur sebenarnya di mesin Anda.

```csharp
string MyDir = "Your Document Directory";
```

## Langkah 2: Menentukan Jalur File CAD

Buat array yang menunjuk ke setiap file CAD yang ingin diproses.

```csharp
string[] sourceFilePaths = new[]
{
    MyDir + "conic_pyramid.dxf",
    MyDir + "Bottom_plate.dwg"
};
```

## Langkah 3: Mengiterasi File CAD

Muat setiap file, deteksi formatnya, dan siapkan untuk mengekstrak informasi layout.

```csharp
foreach (var sourceFilePath in sourceFilePaths)
{
    string extension = Path.GetExtension(sourceFilePath);
    using (CadImage cadImage = (CadImage)Aspose.CAD.Image.Load(sourceFilePath))
    {
        // ... (continue to the next step)
    }
}
```

## Langkah 4: Mendapatkan Layout yang Tidak Kosong

Kita memerlukan metode bantu yang mengembalikan hanya layout yang benar‑benar berisi entitas gambar. Layout kosong diabaikan karena tidak memiliki ukuran untuk dilaporkan.

```csharp
private static List<string> GetNotEmptyLayouts(Image cadImage, string extension)
{
    // ... (continue to the next step)
}
```

## Langkah 5: Mendapatkan Layout untuk File DWG

File DWG menyimpan informasi layout di tabel `HeaderVariables`. Metode berikut mengekstrak nama semua layout yang tidak kosong untuk gambar DWG.

```csharp
private static List<string> GetNotEmptyLayoutsForDwg(CadImage cadImage)
{
    // ... (continue to the next step)
}
```

## Langkah 6: Mendapatkan Layout untuk File DXF

File DXF menggunakan struktur yang berbeda. Metode ini mem-parsing koleksi `Tables` untuk menemukan layout paper space yang berisi entitas.

```csharp
private static List<string> GetNotEmptyLayoutsForDxf(CadImage cadImage)
{
    // ... (continue to the next step)
}
```

## Langkah 7: Mengambil Ukuran Layout dan Menyimpan sebagai Gambar

Akhirnya, lakukan perulangan pada setiap layout yang ditemukan, baca ekstensi‑nya, dan secara opsional render layout ke file gambar untuk verifikasi visual.

```csharp
foreach (string layout in layouts)
{
    // ... (continue to the next step)
}
```

## Masalah Umum & Tips

- **Nama layout tidak ditemukan:** Pastikan file CAD memang berisi layout paper space; beberapa file hanya memiliki model space.  
- **Satuan tidak tepat:** Ukuran dikembalikan dalam satuan asli gambar. Konversikan ke milimeter atau inci bila diperlukan.  
- **Kinerja:** Memuat file DWG/DXF yang sangat besar dapat memakan memori secara intensif; pertimbangkan memproses file secara asynchronous atau dalam batch.

## Pertanyaan yang Sering Diajukan

**T: Apakah Aspose.CAD kompatibel dengan semua format file CAD?**  
J: Ya, Aspose.CAD mendukung beragam format, termasuk DWG, DXF, DGN, dan banyak tipe file BIM.

**T: Bisakah saya menyesuaikan opsi penyimpanan gambar?**  
J: Tentu! Anda dapat mengatur `CadRasterizationOptions` (format, resolusi, warna latar belakang, dll.) sesuai kebutuhan spesifik Anda.

**T: Di mana saya dapat menemukan dokumentasi tambahan?**  
J: Lihat [dokumentasi Aspose.CAD](https://reference.aspose.com/cad/net/) untuk referensi API terperinci dan contoh lainnya.

**T: Apakah ada versi percobaan gratis?**  
J: Ya, Anda dapat menjelajahi Aspose.CAD dengan [versi percobaan gratis](https://releases.aspose.com/).

**T: Bagaimana cara mendapatkan dukungan teknis?**  
J: Untuk dukungan teknis, kunjungi [forum Aspose.CAD](https://forum.aspose.com/c/cad/19).

---

**Terakhir Diperbarui:** 2026-03-21  
**Diuji Dengan:** Aspose.CAD 24.11 untuk .NET  
**Penulis:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}