---
date: 2026-02-23
description: Pelajari cara memuat file DWG menggunakan Aspose.CAD DWG untuk Java dan
  mengekstrak flag underlay – panduan langkah demi langkah untuk pengembang.
linktitle: Accessing Underlay Flags of DWG
second_title: Aspose.CAD Java API
title: aspose cad dwg – Muat DWG & Akses Bendera Underlay (Java)
url: /id/java/cad-file-manipulation/accessing-underlay-flags-of-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Muat File DWG & Akses Bendera Underlay – Aspose.CAD untuk Java

Dalam alur kerja CAD modern, **with aspose cad dwg you can quickly load a DWG file** dan mengambil detail underlay yang sering tersembunyi dari penonton biasa. Apakah Anda sedang membangun penampil DWG Java, mengotomatisasi pipeline proses batch dwg, atau mengekstrak metadata untuk integrasi GIS, Aspose.CAD untuk Java memberi Anda cara bersih, berbasis kode untuk melakukannya. Dalam tutorial ini kami akan memandu langkah‑langkah tepat untuk **load a DWG file**, mengiterasi entitasnya, dan membaca bendera underlay yang sering diabaikan oleh banyak pengembang.

## Jawaban Cepat
- **Apa kelas utama untuk membuka DWG?** `com.aspose.cad.Image.load()` mengembalikan sebuah `CadImage`.
- **Objek mana yang menyimpan informasi underlay?** `CadUnderlay` (atau tipe turunan seperti `CadDgnUnderlay`).
- **Apakah saya memerlukan lisensi untuk pengembangan?** Versi percobaan gratis cukup untuk pengujian; lisensi komersial diperlukan untuk produksi.
- **Bisakah saya memproses banyak file DWG dalam loop?** Ya – cukup ulangi pola muat‑dan‑iterasi.
- **Apakah pendekatan ini kompatibel dengan Java 11+?** Tentu saja, Aspose.CAD mendukung Java 8 hingga rilis LTS terbaru.

## aspose cad dwg – Memuat File DWG (Java)

`Image.load()` membaca konten DWG biner dan membuat objek `CadImage` di memori. Dari sana Anda dapat menjelajahi layer, blok, dan entitas underlay tanpa harus menangani format file DWG sendiri.

## Mengapa mengekstrak bendera underlay dari DWG?

Bendera underlay memberi tahu Anda bagaimana referensi eksternal (seperti underlay DGN atau PDF) diposisikan, diskalakan, dan diputar di dalam gambar. Mengetahui nilai‑nilai ini memungkinkan Anda untuk:

- Membuat ulang tata letak visual yang tepat dalam **java dwg viewer** khusus.
- Mengonversi underlay menjadi entitas CAD native untuk penyuntingan lebih lanjut.
- Menghasilkan laporan yang mencakup metadata underlay untuk kepatuhan atau dokumentasi.
- **Batch process dwg** file dan menyimpan metadata underlay mereka dalam basis data untuk analisis selanjutnya.

## Prasyarat
- **Aspose.CAD Library** – unduh dari halaman [releases](https://releases.aspose.com/cad/java/).  
- **Java Development Kit** – JDK 8 atau lebih baru.  
- **Sebuah folder** yang berisi file DWG yang ingin Anda analisis. Ganti `"Your Document Directory"` dalam kode dengan path aktual Anda.

## Impor Namespace

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.CadBaseEntity;
import com.aspose.cad.fileformats.cad.cadobjects.CadDgnUnderlay;
import com.aspose.cad.fileformats.cad.cadobjects.CadUnderlay;
import com.aspose.cad.fileformats.cad.cadobjects.UnderlayFlags;
```

## Panduan Langkah‑demi‑Langkah

### Langkah 1: Atur Direktori Sumber Daya
```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "DWGDrawings/";
```
Tentukan lokasi file DWG Anda. Menggunakan folder khusus menjaga contoh tetap bersih dan dapat dipindahkan.

### Langkah 2: Muat File DWG
```java
// Input file name and path
String fileName = dataDir + "BlockRefDgn.dwg";

// Load an existing DWG file and convert it into CadImage 
CadImage image = (CadImage)Image.load(fileName);
```
Di sini kami **load dwg file** `BlockRefDgn.dwg` ke dalam instance `CadImage`, siap untuk inspeksi.

### Langkah 3: Iterasi Entitas DWG
```java
// Go through each entity inside the DWG file
for(CadBaseEntity entity : image.getEntities())
```
Loop ini melintasi setiap entitas—garis, lingkaran, blok, dan underlay—sehingga kami dapat memilih yang diperlukan.

### Langkah 4: Identifikasi Entitas CadDgnUnderlay
```java
// Check if entity is of CadDgnUnderlay type
if (entity instanceof CadDgnUnderlay)
```
Hanya objek `CadDgnUnderlay` yang berisi bendera underlay yang kami cari, jadi kami menyaringnya.

### Langkah 5: Akses Informasi Underlay
```java
// Access different underlay flags 
CadUnderlay underlay = (CadUnderlay) entity;
System.out.println(underlay.getUnderlayPath());
System.out.println(underlay.getUnderlayName());
// ... (Additional underlay properties)
break;
```
Setelah kami memiliki `CadUnderlay`, kami dapat membaca path, nama, titik sisipan, rotasi, faktor skala, dan enum `UnderlayFlags` yang menunjukkan visibilitas, pemotongan, dan opsi rendering lainnya.

## Cara memuat file dwg dalam proses batch

Jika Anda perlu **batch process dwg** file, bungkus langkah‑langkah di atas dalam loop `for` sederhana yang mengiterasi semua file di `dataDir`. Panggilan `Image.load()` yang sama bekerja untuk setiap file, dan Anda dapat menyimpan bendera yang diekstrak ke CSV atau basis data untuk pelaporan selanjutnya.

## Masalah Umum & Tips
- **Null underlay path** – Pastikan DWG benar‑benar merujuk ke file eksternal; jika tidak, path akan kosong.
- **Unsupported underlay type** – Aspose.CAD saat ini mendukung underlay DGN; underlay PDF belum tersedia melalui API.
- **License exceptions** – Menjalankan kode tanpa lisensi yang valid akan menambahkan watermark pada gambar yang diekspor.
- **Performance tip:** Gunakan kembali satu instance `Image` saat memproses banyak file dalam batch untuk mengurangi beban GC.

## Pertanyaan yang Sering Diajukan

**Q: Bisakah saya menggunakan Aspose.CAD untuk Java dengan format file CAD lain?**  
A: Aspose.CAD terutama berfokus pada format DWG, tetapi juga mendukung DXF, DWF, dan format CAD lainnya.

**Q: Apakah ada versi percobaan tersedia untuk Aspose.CAD untuk Java?**  
A: Ya, Anda dapat menjelajahi fitur dengan percobaan gratis dari [di sini](https://releases.aspose.com/).

**Q: Bagaimana saya dapat mendapatkan dukungan atau bantuan dengan Aspose.CAD untuk Java?**  
A: Kunjungi [forum Aspose.CAD](https://forum.aspose.com/c/cad/19) untuk dukungan komunitas dan diskusi.

**Q: Apakah lisensi sementara tersedia untuk Aspose.CAD untuk Java?**  
A: Ya, Anda dapat memperoleh lisensi sementara [di sini](https://purchase.aspose.com/temporary-license/).

**Q: Di mana saya dapat menemukan dokumentasi lengkap untuk Aspose.CAD untuk Java?**  
A: Lihat [dokumentasi](https://reference.aspose.com/cad/java/) untuk informasi detail.

---

**Terakhir Diperbarui:** 2026-02-23  
**Diuji Dengan:** Aspose.CAD 24.12 for Java  
**Penulis:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}