---
date: 2026-03-07
description: Pelajari cara mengganti font dalam file DWG menggunakan Aspose.CAD untuk
  Java. Panduan langkah demi langkah ini menunjukkan **cara mengganti font** dari
  gaya tertentu dengan presisi.
linktitle: Substitute Font of a Particular Style in DWG
second_title: Aspose.CAD Java API
title: Cara Mengganti Font pada Gaya Tertentu di DWG Menggunakan Aspose.CAD untuk
  Java
url: /id/java/cad-text-and-annotation/substitute-font-of-particular-style-in-dwg/
weight: 12
---

: keep **text**.

Also keep code placeholders unchanged.

Now produce final answer.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cara Mengganti Font pada Gaya Tertentu di DWG Menggunakan Aspose.CAD untuk Java

## Pendahuluan

Di dunia CAD (Computer‑Aided Design), presisi dan detail sangat penting, dan **mengetahui cara mengganti font** dalam sebuah gambar dapat menghemat Anda berjam‑jam kerja ulang. Aspose.CAD untuk Java memberikan pengembang cara yang bersih dan terprogram untuk memodifikasi file DWG, termasuk kemampuan mengubah font dari gaya teks tertentu. Pada tutorial ini kami akan memandu Anda langkah demi langkah untuk mengganti font pada gaya tertentu dalam file DWG, menjelaskan mengapa Anda mungkin ingin melakukannya, dan menunjukkan cara memverifikasi hasilnya.

## Jawaban Cepat
- **Apa arti “replace font” dalam DWG?** Mengubah properti font utama yang terkait dengan definisi gaya teks.  
- **Perpustakaan mana yang menangani ini?** Aspose.CAD untuk Java.  
- **Apakah saya memerlukan lisensi?** Versi percobaan gratis cukup untuk pengujian; lisensi komersial diperlukan untuk produksi.  
- **Bisakah saya mengubah beberapa gaya sekaligus?** Ya – iterasi melalui koleksi gaya dan atur masing‑masing font.  
- **Apakah kode kompatibel dengan Java 8+?** Tentu saja, API menargetkan Java 8 dan yang lebih baru.

## Apa itu Penggantian Font dalam DWG?
Penggantian font berarti memperbarui properti *font utama* dari sebuah gaya teks (juga disebut “style” dalam terminologi DWG). Ketika sebuah gambar merujuk gaya tersebut, setiap potongan teks secara otomatis mengadopsi font baru, memastikan tampilan yang konsisten di seluruh file.

## Mengapa Memodifikasi Gaya Teks DWG?
- **Mempertahankan konsistensi merek:** Gunakan font perusahaan di semua gambar.  
- **Memperbaiki font yang hilang:** Ganti font yang tidak tersedia dengan yang terpasang pada sistem target.  
- **Mempersiapkan untuk pencetakan/plotting:** Beberapa plotter memerlukan font khusus untuk output yang akurat.  

## Prasyarat

Sebelum Anda memulai tutorial ini, pastikan Anda telah menyiapkan hal‑hal berikut:

1. **Aspose.CAD untuk Java Library:** Unduh dan instal perpustakaan Aspose.CAD. Anda dapat menemukan perpustakaan dan dokumentasinya [di sini](https://releases.aspose.com/cad/java/).

2. **Java Development Kit (JDK):** Pastikan Java terpasang di mesin Anda.

Sekarang setelah Anda memiliki alat yang diperlukan, mari lanjut ke bagian berikutnya.

## Impor Namespace (diperlukan untuk memodifikasi gaya teks DWG)

Di Java, mengimpor namespace yang tepat sangat penting untuk memanfaatkan pustaka eksternal. Dalam kasus ini, pastikan Anda mengimpor namespace Aspose.CAD yang diperlukan. Berikut cara melakukannya:

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
```

Sekarang, mari uraikan contoh kode menjadi beberapa langkah.

## Langkah 1: Atur Direktori Sumber Daya

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";
```

Ganti `"Your Document Directory"` dengan path ke direktori dokumen Anda yang sebenarnya.

## Langkah 2: Muat Gambar CAD

```java
String srcFile = dataDir + "conic_pyramid.dxf";

// Load a CAD drawing in an instance of CadImage
CadImage cadImage = (CadImage)Image.load(srcFile);
```

Pastikan untuk mengganti `"conic_pyramid.dxf"` dengan nama sebenarnya dari gambar CAD Anda.

## Langkah 3: Tentukan Font untuk Gaya (ubah font gaya DWG)

```java
// Specify the font for one particular style
((CadStyleTableObject)cadImage.getStyles().get_Item(0)).setPrimaryFontName("Arial");
```

Sesuaikan nama font ("Arial" dalam contoh ini) sesuai kebutuhan Anda. Baris ini **menetapkan font utama gaya DWG**, secara efektif menggantikan font lama.

## Masalah Umum dan Solusinya

| Masalah | Penyebab | Solusi |
|-------|-------|----------|
| Font tidak berubah setelah disimpan | Gambar tidak disimpan setelah dimodifikasi | Panggil `cadImage.save(outputPath);` setelah mengatur font. |
| Nama font tidak dikenali | Font tidak terpasang pada sistem tempat kode dijalankan | Instal font tersebut atau gunakan nama font generik (mis., "Tahoma"). |
| `ClassCastException` | Tipe objek salah dari `get_Item` | Pastikan indeks mengarah ke `CadStyleTableObject`. |

## FAQ

### Q1: Apakah saya dapat mengganti beberapa font dalam satu file DWG?

A1: Ya, Anda dapat iterasi melalui gaya yang berbeda dan mengatur font utama untuk setiap gaya secara individual.

### Q2: Apakah ada batasan pada nama font yang dapat saya gunakan?

A2: Tidak, Anda dapat menggunakan nama font apa pun yang valid dan tersedia di sistem Anda.

### Q3: Apakah saya dapat membatalkan penggantian font?

A3: Aspose.CAD memberikan fleksibilitas; Anda dapat mengembalikan perubahan atau menyimpan versi berbeda dari file DWG Anda.

### Q4: Apakah tutorial ini berlaku untuk format CAD lain?

A4: Meskipun contoh berfokus pada DWG, prinsip serupa dapat diterapkan pada format CAD lain yang didukung.

### Q5: Bagaimana saya dapat mendapatkan dukungan untuk Aspose.CAD untuk Java?

A5: Kunjungi [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) untuk dukungan komunitas dan diskusi.

## Pertanyaan Umum Tambahan

**Q: Bagaimana cara menyimpan gambar yang dimodifikasi?**  
A: Setelah mengatur font baru, panggil `cadImage.save(dataDir + "output.dwg");` untuk menulis perubahan ke file baru.

**Q: Apakah saya dapat mengganti font hanya pada objek anotasi?**  
A: Ya, filter koleksi gaya untuk gaya yang terkait anotasi sebelum menerapkan `setPrimaryFontName`.

**Q: Apakah memungkinkan untuk meninjau perubahan font tanpa menyimpan?**  
A: Anda dapat merender gambar ke bitmap menggunakan `cadImage.save(outputStream, new ImageOptions());` untuk meninjau di memori.

**Q: Apakah Aspose.CAD mendukung font TrueType dan OpenType?**  
A: Baik TrueType (.ttf) maupun OpenType (.otf) didukung sepenuhnya selama font tersebut terpasang pada OS host.

## Pertanyaan yang Sering Diajukan

**Q: Versi Aspose.CAD apa yang diperlukan untuk kode ini?**  
A: API yang digunakan dalam tutorial ini tersedia di Aspose.CAD untuk Java 24.11 dan yang lebih baru.

**Q: Apakah saya dapat menjalankan kode ini di server Linux?**  
A: Ya, selama font yang diperlukan terpasang di server dan Java 8+ tersedia.

**Q: Bagaimana cara menampilkan semua gaya teks yang tersedia sebelum mengubah font?**  
A: Iterasi melalui `cadImage.getStyles()` dan cetak nama serta font utama masing‑masing gaya.

**Q: Apakah ada cara untuk memproses banyak file DWG secara batch?**  
A: Bungkus logika dalam loop yang memuat tiap file, memperbarui gaya yang diinginkan, dan menyimpan output.

**Q: Apakah mengubah font utama memengaruhi dimensi atau spasi?**  
A: Metri font dapat berbeda, sehingga Anda mungkin perlu menyesuaikan tinggi teks atau posisi setelah perubahan.

## Kesimpulan

Aspose.CAD untuk Java membuka kemungkinan kuat untuk manipulasi CAD, dan **cara mengganti font** hanyalah salah satu dari banyak kemampuan yang dimilikinya. Bereksperimenlah dengan gaya yang berbeda, gunakan kata kunci sekunder seperti *modify DWG text style* atau *set primary font dwg* untuk menyempurnakan gambar Anda, dan integrasikan kode ke dalam pipeline otomasi yang lebih besar untuk pemrosesan batch.

---

**Last Updated:** 2026-03-07  
**Tested With:** Aspose.CAD for Java 24.11  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}