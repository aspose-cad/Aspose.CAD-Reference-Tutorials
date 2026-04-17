---
date: 2026-03-19
description: Pelajari cara mengubah ukuran gambar CAD di .NET dengan Aspose.CAD, termasuk
  cara mengubah skala unit gambar CAD dan menyesuaikan ukuran tata letak. Ikuti panduan
  langkah demi langkah kami.
linktitle: Adjusting CAD Drawing Size
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Cara Mengubah Ukuran Gambar CAD dengan Aspose.CAD untuk .NET
url: /id/net/cad-drawing-manipulation/adjust-cad-drawing-size/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cara Mengubah Ukuran Gambar CAD dengan Aspose.CAD untuk .NET

## Pendahuluan

Jika Anda perlu **how to resize CAD** file langsung dari aplikasi .NET Anda, Anda berada di tempat yang tepat. Dalam tutorial ini kami akan menunjukkan cara mengubah pengaturan unit CAD, menskalakan dimensi gambar CAD, dan menyesuaikan ukuran CAD secara programatis menggunakan Aspose.CAD untuk .NET. Pada akhir panduan Anda akan memiliki solusi yang solid dan siap produksi untuk mengubah ukuran format CAD apa pun yang didukung.

## Jawaban Cepat
- **Library apa yang diperlukan?** Aspose.CAD for .NET  
- **Apakah saya dapat mengubah tipe unit?** Ya – set `UnitType` di `CadRasterizationOptions`  
- **Apakah lisensi diperlukan untuk produksi?** Lisensi Aspose.CAD yang valid diperlukan untuk penggunaan non‑trial  
- **Format gambar apa yang diekspor contoh?** BMP (tetapi format raster yang didukung apa pun dapat digunakan)  
- **Berapa banyak baris kode?** Kurang dari 30 baris untuk operasi resize lengkap  

## Apa itu “how to resize CAD” dalam praktik?
Mengubah ukuran gambar CAD berarti mengonversi data vektor menjadi gambar raster pada skala atau unit tertentu (mis., sentimeter, inci). Ini berguna ketika Anda perlu menyisipkan gambar dalam laporan, menghasilkan thumbnail, atau mengintegrasikan visual CAD ke dalam halaman web.

## Mengapa menyesuaikan ukuran CAD dengan Aspose.CAD?
- **Tidak ada perangkat lunak CAD eksternal** – semuanya berjalan di dalam kode .NET Anda.  
- **Kontrol halus** atas unit, tata letak, dan opsi rasterisasi.  
- **Dukungan lintas format** – kode yang sama bekerja untuk DWG, DXF, DWF, dan lainnya.  

## Prasyarat

Sebelum kita mulai, pastikan Anda memiliki:

- Aspose.CAD for .NET Library: Unduh dan instal perpustakaan dari [halaman unduhan Aspose.CAD untuk .NET](https://releases.aspose.com/cad/net/).  
- Sample CAD Drawing: Sebuah file seperti `sample.dwg` ditempatkan di direktori dokumen proyek Anda.  

## Impor Namespace

Pertama, impor namespace yang memberi Anda akses ke kelas Aspose.CAD.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Langkah 1: Muat Gambar CAD

Muat file sumber ke dalam objek `Image`. Objek ini mewakili gambar CAD dalam memori dan akan menjadi dasar untuk semua operasi selanjutnya.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "sample.dwg";

// Load a CAD drawing in an instance of Image
using (var image = Aspose.CAD.Image.Load(sourceFilePath))
{
    // Your code here...
}
```

## Langkah 2: Buat BmpOptions (atau format raster lainnya)

`BmpOptions` memberi tahu Aspose.CAD cara merender data vektor saat Anda menyimpannya sebagai bitmap. Anda dapat menggantinya dengan `PngOptions`, `JpegOptions`, dll., tergantung pada format target Anda.

```csharp
Aspose.CAD.ImageOptions.BmpOptions bmpOptions = new Aspose.CAD.ImageOptions.BmpOptions();
```

## Langkah 3: Atur CadRasterizationOptions

`CadRasterizationOptions` menyimpan pengaturan inti untuk skala, konversi unit, dan pemilihan tata letak. Menautkannya ke properti `VectorRasterizationOptions` dari `BmpOptions` memastikan rasterizer menggunakan pengaturan khusus Anda.

```csharp
Aspose.CAD.ImageOptions.CadRasterizationOptions cadRasterizationOptions = new Aspose.CAD.ImageOptions.CadRasterizationOptions();
bmpOptions.VectorRasterizationOptions = cadRasterizationOptions;
```

## Langkah 4: Atur UnitType (ubah unit CAD)

Di sini kami mengubah unit CAD dari default menjadi sentimeter. Inilah tempat kata kunci **change cad unit** berada, dan secara langsung memengaruhi ukuran gambar akhir.

```csharp
cadRasterizationOptions.UnitType = Aspose.CAD.ImageOptions.UnitType.Centimeter;
```

## Langkah 5: Pilih Layout (atur layout CAD)

Jika gambar Anda berisi beberapa layout (mis., Model, Sheet1), tentukan mana yang ingin Anda rasterisasi. Memilih layout yang tepat sangat penting ketika Anda **set cad layouts** untuk output yang diubah ukurannya.

```csharp
cadRasterizationOptions.Layouts = new string[] { "Model" };
```

## Langkah 6: Ekspor ke BMP (ubah ukuran gambar CAD)

Akhirnya, simpan gambar yang telah dirasterisasi. File output mencerminkan ukuran, unit, dan layout baru yang Anda konfigurasikan—secara efektif menyelesaikan operasi **resize CAD drawing**.

```csharp
string outPath = sourceFilePath + ".bmp";
image.Save(outPath, bmpOptions);
```

Anda sekarang memiliki file BMP yang mewakili gambar CAD yang diubah ukurannya, siap untuk diproses lebih lanjut atau ditampilkan.

## Masalah Umum dan Solusinya

| Masalah | Mengapa Terjadi | Solusi |
|-------|----------------|-----|
| Output buram | DPI (dots per inch) default rendah | Set `cadRasterizationOptions.Resolution = 300;` sebelum menyimpan |
| Layout yang salah muncul | Typo pada nama layout | Verifikasi nama layout yang tepat menggunakan penampil CAD atau koleksi `Layouts` |
| Konversi unit terlihat tidak tepat | Mencampur unit metrik dan imperial | Pastikan `UnitType` sesuai dengan sistem pengukuran yang diinginkan |

## FAQs

### Q1: Apakah Aspose.CAD untuk .NET kompatibel dengan semua format CAD?

A1: Aspose.CAD untuk .NET mendukung berbagai format CAD, termasuk DWG, DXF, DWF, dan lainnya. Periksa [dokumentasi](https://reference.aspose.com/cad/net/) untuk daftar lengkap.

### Q2: Bisakah saya mengubah ukuran beberapa layout secara bersamaan?

A2: Ya, Anda dapat mengubah ukuran beberapa layout dengan menyesuaikan array `Layouts` dalam `CadRasterizationOptions`.

### Q3: Di mana saya dapat mendapatkan dukungan untuk Aspose.CAD untuk .NET?

A3: Kunjungi [forum Aspose.CAD](https://forum.aspose.com/c/cad/19) untuk dukungan komunitas dan bantuan.

### Q4: Apakah tersedia trial gratis?

A4: Ya, Anda dapat mencoba [trial gratis](https://releases.aspose.com/) untuk mengevaluasi fitur Aspose.CAD untuk .NET.

### Q5: Bagaimana saya dapat memperoleh lisensi sementara untuk Aspose.CAD untuk .NET?

A5: Dapatkan lisensi sementara untuk tujuan pengujian [di sini](https://purchase.aspose.com/temporary-license/).

## Pertanyaan yang Sering Diajukan

**Q: Bagaimana cara menskalakan gambar CAD tanpa mengubah tipe unit?**  
A: Sesuaikan properti `Zoom` dari `CadRasterizationOptions` (mis., `cadRasterizationOptions.Zoom = 2.0;`) untuk menggandakan ukuran sambil mempertahankan unit asli.

**Q: Bisakah saya mengekspor ke format selain BMP?**  
A: Tentu saja. Ganti `BmpOptions` dengan `PngOptions`, `JpegOptions`, atau kelas format raster lain yang didukung.

**Q: Apakah memungkinkan memproses batch folder gambar?**  
A: Ya. Loop melalui file dalam direktori, terapkan logika rasterisasi yang sama, dan simpan setiap output dengan nama unik.

---

**Terakhir Diperbarui:** 2026-03-19  
**Diuji Dengan:** Aspose.CAD for .NET 24.11 (latest at time of writing)  
**Penulis:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}