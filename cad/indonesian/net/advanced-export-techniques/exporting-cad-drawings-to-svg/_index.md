---
date: 2026-03-07
description: Pelajari cara mengekspor CAD ke SVG menggunakan Aspose.CAD untuk .NET,
  menyesuaikan warna SVG, dan mengonversi DWG ke SVG secara efisien.
linktitle: Exporting CAD Drawings to SVG Format
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Ekspor CAD ke SVG – Mengekspor Gambar CAD ke Format SVG - Panduan Aspose.CAD
url: /id/net/advanced-export-techniques/exporting-cad-drawings-to-svg/
weight: 15
---

 etc.

Also keep markdown tables with pipes.

Let's craft final answer.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ekspor CAD ke SVG – Mengekspor Gambar CAD ke Format SVG

## Pendahuluan

Mengekspor gambar CAD ke SVG adalah kebutuhan umum ketika Anda memerlukan grafik yang tidak bergantung pada resolusi untuk halaman web, laporan, atau visualisasi interaktif. Pada tutorial ini Anda akan belajar **cara mengekspor CAD ke SVG** dengan Aspose.CAD untuk .NET, menjelajahi opsi untuk **menyesuaikan warna SVG**, dan melihat bagaimana **mengonversi DWG ke SVG** (atau DXF ke SVG) hanya dengan beberapa baris kode. Langkah‑nya cepat, API‑nya intuitif, dan file SVG yang dihasilkan dapat diskalakan dengan sempurna di perangkat apa pun.

## Jawaban Cepat
- **Perpustakaan apa yang menangani konversi?** Aspose.CAD for .NET.  
- **Bisakah saya mengubah mode warna?** Ya – gunakan `SvgColorMode` untuk mengatur grayscale, hitam‑putih, atau warna penuh.  
- **Format CAD apa yang didukung?** DWG, DXF, dan banyak lainnya (lihat dokumentasi Aspose.CAD).  
- **Apakah saya memerlukan lisensi untuk pengembangan?** Lisensi sementara tersedia untuk pengujian.  
- **Berapa lama proses konversi?** Biasanya kurang dari satu detik untuk gambar standar.

## Apa itu “ekspor CAD ke SVG”?
Mengekspor CAD ke SVG berarti mengambil file CAD asli (seperti DWG atau DXF) dan merendernya ke dalam format Scalable Vector Graphics. SVG berbasis XML, ringan, dan dapat ditata dengan CSS—menjadikannya ideal untuk aplikasi web dan seluler modern.

## Mengapa menggunakan Aspose.CAD untuk mengekspor CAD ke SVG?
- **Tidak ada ketergantungan eksternal** – API .NET murni, tidak memerlukan instalasi AutoCAD.  
- **Kontrol detail** – Anda dapat **menyesuaikan warna SVG**, memutuskan apakah teks disimpan sebagai bentuk, dan memilih opsi rasterisasi.  
- **Dukungan format luas** – kode yang sama bekerja untuk **mengonversi DWG ke SVG**, **mengonversi DXF ke SVG**, dan format lain, menyederhanakan basis kode Anda.  
- **Kinerja tinggi** – dioptimalkan untuk kecepatan dan penggunaan memori rendah, cocok untuk pemrosesan batch.

## Prasyarat

Sebelum memulai, pastikan Anda memiliki:

- **Aspose.CAD for .NET** terinstal. Anda dapat mengunduh perpustakaan [di sini](https://releases.aspose.com/cad/net/).  
- Lingkungan pengembangan .NET (Visual Studio, Rider, atau .NET CLI).  
- File CAD (DWG atau DXF) yang ingin Anda konversi.

## Impor Namespace

Pertama, bawa namespace yang diperlukan ke dalam proyek Anda agar kelas‑kelas tersedia.

```csharp
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## Panduan Langkah‑per‑Langkah

### Langkah 1: Atur Direktori Dokumen  
Tentukan folder tempat file CAD sumber Anda berada dan tempat output SVG akan disimpan.

```csharp
// The path to the documents directory.
string MyDir = "Your Document Directory";
```

### Langkah 2: Muat Gambar CAD  
Gunakan `Image.Load` untuk membaca file DWG (atau DXF). Ini bekerja untuk skenario **load DWG .NET**.

```csharp
using (Image image = Image.Load(MyDir + "sample.dwg"))
{
```

### Langkah 3: Konfigurasikan Opsi Ekspor SVG  
Sesuaikan pengaturan ekspor agar sesuai dengan kebutuhan Anda. Di sini kami mengatur mode warna ke grayscale dan memaksa semua teks dirender sebagai bentuk vektor.

```csharp
    var options = new SvgOptions();
    options.ColorType = SvgColorMode.Grayscale;   // customize SVG color mode
    options.TextAsShapes = true;                  // ensures text appears as shapes
```

### Langkah 4: Simpan File SVG  
Akhirnya, tulis file SVG ke disk. Langkah ini **menyimpan CAD sebagai SVG** dan menyelesaikan konversi.

```csharp
    image.Save(MyDir + "sample.svg", options);
}
```

Dengan mengikuti empat langkah singkat ini, Anda dapat **mengonversi DWG ke SVG** (atau **mengonversi DXF ke SVG**) dengan kontrol penuh atas tampilan output.

## Masalah Umum dan Solusinya

| Masalah | Penyebab | Solusi |
|-------|-------|-----|
| **Output SVG kosong** | Jalur file sumber tidak benar atau file rusak. | Verifikasi `MyDir` dan pastikan file CAD terbuka tanpa error. |
| **Warna terlihat salah** | `SvgColorMode` secara tidak sengaja diatur ke Grayscale. | Ubah `options.ColorType` menjadi `SvgColorMode.FullColor` untuk mempertahankan warna asli. |
| **Teks hilang** | `TextAsShapes` diatur ke `false` dan penampil tidak mendukung font tersemat. | Pertahankan `TextAsShapes = true` atau sematkan font yang diperlukan dalam SVG. |

## FAQ

### Q1: Apakah Aspose.CAD kompatibel dengan semua format CAD?

A1: Aspose.CAD mendukung berbagai format CAD, termasuk DWG dan DXF, memastikan kompatibilitas yang luas.

### Q2: Bisakah saya menyesuaikan mode warna saat mengekspor ke SVG?

A2: Ya, Aspose.CAD memungkinkan Anda memilih mode warna, memberikan fleksibilitas pada output.

### Q3: Apakah lisensi sementara tersedia untuk tujuan pengujian?

A3: Ya, Anda dapat memperoleh lisensi sementara [di sini](https://purchase.aspose.com/temporary-license/) untuk evaluasi.

### Q4: Di mana saya dapat menemukan dokumentasi detail untuk Aspose.CAD?

A4: Dokumentasi tersedia [di sini](https://reference.aspose.com/cad/net/).

### Q5: Bagaimana cara mendapatkan dukungan atau mengajukan pertanyaan terkait Aspose.CAD?

A5: Kunjungi forum komunitas [di sini](https://forum.aspose.com/c/cad/19) untuk dukungan dan diskusi.

## Pertanyaan yang Sering Diajukan

**Q: Bisakah saya menggunakan kode ini dengan .NET Core atau .NET 6?**  
A: Tentu saja. Aspose.CAD for .NET kompatibel dengan .NET Framework, .NET Core, dan .NET 5/6+.

**Q: Apakah memungkinkan mengekspor hanya layout atau layer tertentu?**  
A: Ya. Gunakan `SvgOptions` untuk mengatur `PageIndex` atau menyaring layer sebelum menyimpan.

**Q: Bagaimana cara menyematkan gaya CSS khusus ke dalam SVG yang dihasilkan?**  
A: Setelah menyimpan, Anda dapat memproses XML SVG untuk menyisipkan elemen `<style>`, atau gunakan `options.CustomCss` jika tersedia pada versi terbaru.

**Q: Apa batas ukuran untuk file CAD sumber?**  
A: Perpustakaan dapat menangani file besar, namun konsumsi memori meningkat seiring kompleksitas. Untuk gambar sangat besar, pertimbangkan memproses halaman secara terpisah.

**Q: Apakah konversi mempertahankan ketebalan garis dan tipe garis?**  
A: Secara default, ketebalan garis dipertahankan. Anda dapat menyesuaikan opsi rendering di `SvgOptions` untuk kontrol yang lebih halus.

---

**Terakhir Diperbarui:** 2026-03-07  
**Diuji Dengan:** Aspose.CAD for .NET 24.12  
**Penulis:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}