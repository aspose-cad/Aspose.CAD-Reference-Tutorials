---
date: 2025-12-28
description: Pelajari cara memuat file DWG dalam proyek Java dan mengatur nama font
  utama menggunakan Aspose.CAD untuk Java. Panduan langkah demi langkah untuk visual
  CAD yang sempurna.
linktitle: Substitute Font in DWG
second_title: Aspose.CAD Java API
title: Cara memuat file DWG di Java dan mengganti font dengan Aspose.CAD
url: /id/java/cad-text-and-annotation/substitute-font-in-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cara memuat file DWG Java dan mengganti font dengan Aspose.CAD

## Pendahuluan

Jika Anda perlu **memuat file DWG Java** dalam aplikasi dan memberikan gambar Anda tampilan yang halus, mengganti font adalah solusi cepat. Dengan Aspose.CAD untuk Java Anda dapat mengganti gaya teks default dengan font apa pun yang terpasang di sistem, memastikan setiap anotasi muncul persis seperti yang Anda harapkan. Dalam tutorial ini kami akan membahas seluruh proses—dari memuat file DWG di Java hingga menggunakan metode `setPrimaryFontName` untuk mengubah font.

## Jawaban Cepat
- **Perpustakaan apa yang saya butuhkan?** Aspose.CAD for Java.
- **Apakah saya dapat memuat file DWG di Java?** Ya, cukup panggil `Image.load()` pada path DWG.
- **Metode mana yang mengubah font?** `setPrimaryFontName`.
- **Apakah saya memerlukan lisensi untuk produksi?** Ya, lisensi komersial diperlukan.
- **Apakah pemrosesan batch memungkinkan?** Tentu – lakukan loop melalui banyak file dengan kode yang sama.

## Apa itu “load dwg file java”?

Memuat file DWG dalam lingkungan Java berarti membaca data CAD biner ke dalam objek `Image` yang dapat dimanipulasi oleh Aspose.CAD. Setelah file dimuat, Anda memiliki akses programatik penuh ke lapisan, gaya, dan entitas teks.

## Mengapa mengganti font dalam file DWG?

- **Konsistensi:** Menjamin semua kolaborator melihat jenis huruf yang sama, terlepas dari pengaturan font lokal mereka.  
- **Keterbacaan:** Beberapa font CAD default sulit dibaca di layar; mengganti ke font bersih seperti Arial meningkatkan kejelasan.  
- **Branding:** Menyesuaikan gambar teknis dengan panduan gaya perusahaan.

## Prasyarat

- **Java Development Kit (JDK)** – versi terbaru apa pun (disarankan 8+).  
- **Aspose.CAD untuk Java** – unduh dari [website](https://releases.aspose.com/cad/java/).  
- **File DWG contoh** – gambar yang ingin Anda modifikasi (Anda dapat menggunakan file DWG atau DXF apa pun untuk pengujian).

## Impor Namespace

Dalam proyek Java Anda, impor kelas yang diperlukan untuk bekerja dengan Aspose.CAD. Impor ini memberi Anda akses ke pemuatan gambar, objek khusus CAD, dan manipulasi gaya.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadtables.CadStyleTableObject;
```

## Panduan langkah‑demi‑langkah untuk mengganti font

### Langkah 1: Muat file DWG Anda (load dwg file java)

Pertama, arahkan API ke lokasi file DWG (atau DXF) Anda dan muat ke dalam objek `CadImage`.

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";

String srcFile = dataDir + "conic_pyramid.dxf";
CadImage cadImage = (CadImage) Image.load(srcFile);
```

> **Pro tip:** Jika Anda bekerja langsung dengan file DWG, ganti ekstensi `.dxf` dengan `.dwg` pada variabel `srcFile`.

### Langkah 2: Iterasi tabel gaya dan atur nama font utama

Setiap gambar CAD berisi koleksi objek gaya. Lakukan loop melalui mereka dan gunakan metode `setPrimaryFontName` (panggilan API yang **mengatur nama font utama**) untuk mengganti font.

```java
for(Object style : cadImage.getStyles())
{
    // Set the font name
    ((com.aspose.cad.fileformats.cad.cadtables.CadStyleTableObject)style).setPrimaryFontName("Arial");
}
```

Anda dapat mengubah `"Arial"` ke font apa pun yang terpasang di mesin yang menjalankan kode.

### Langkah 3: Simpan gambar yang telah dimodifikasi

Setelah memperbarui font, tulis perubahan kembali ke file DWG baru (atau timpa file asli).

```java
cadImage.save(dataDir + "output.dwg", new DwgOptions());
```

File yang disimpan kini menggunakan font yang Anda tentukan, dan setiap anotasi teks akan ditampilkan dengan jenis huruf tersebut.

## Masalah Umum dan Solusinya

| Masalah | Solusi |
|-------|----------|
| **Font tidak diterapkan** | Pastikan font terpasang di OS host dan ejaannya cocok persis. |
| **`Image.load` melempar pengecualian** | Pastikan path file benar dan file tersebut merupakan format DWG/DXF yang didukung. |
| **Penurunan kinerja pada file besar** | Proses file dalam thread terpisah atau batch untuk menghindari pemblokiran UI. |

## Pertanyaan yang Sering Diajukan

**Q: Apakah metode `setPrimaryFontName` memengaruhi hanya entitas teks?**  
A: Metode ini memperbarui font utama untuk tabel gaya, yang pada gilirannya memengaruhi semua objek teks yang merujuk pada gaya tersebut.

**Q: Bisakah saya menggunakan font khusus yang tidak terpasang di sistem?**  
A: Aspose.CAD bergantung pada registri font sistem operasi. Untuk menggunakan font khusus, instal font tersebut di mesin yang menjalankan kode.

**Q: Apakah memungkinkan mengubah font hanya untuk satu lapisan saja?**  
A: Ya, Anda dapat menyaring gaya berdasarkan nama lapisan sebelum memanggil `setPrimaryFontName`.

**Q: Versi Aspose.CAD apa yang diperlukan untuk file DWG 2022?**  
A: Rilis terbaru (per 2025) sepenuhnya mendukung DWG 2022. Selalu periksa catatan rilis untuk dukungan format tertentu.

**Q: Bagaimana cara menangani lisensi di lingkungan pengembangan?**  
A: Gunakan lisensi evaluasi sementara untuk pengujian. Untuk produksi, sematkan file lisensi yang Anda beli menggunakan `License.setLicense("Aspose.Total.Java.lic");`.

**Terakhir Diperbarui:** 2025-12-28  
**Diuji Dengan:** Aspose.CAD untuk Java 24.11  
**Penulis:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}