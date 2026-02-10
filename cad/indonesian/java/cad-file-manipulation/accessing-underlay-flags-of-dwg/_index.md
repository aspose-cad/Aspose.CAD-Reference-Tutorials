---
date: 2025-12-22
description: Pelajari cara memuat file DWG dan mengekstrak informasi underlay dengan
  Aspose.CAD untuk Java – panduan langkah demi langkah yang mencakup flag underlay.
linktitle: Accessing Underlay Flags of DWG
second_title: Aspose.CAD Java API
title: Muat File DWG & Akses Bendera Underlay – Aspose.CAD untuk Java
url: /id/java/cad-file-manipulation/accessing-underlay-flags-of-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Muat File DWG & Akses Flag Underlay – Aspose.CAD untuk Java

Dalam alur kerja CAD modern, **memuat file DWG** dengan cepat dan mengambil detail underlay adalah kebutuhan umum. Baik Anda sedang membangun viewer, mengotomatisasi pemrosesan batch, atau mengekstrak metadata untuk integrasi GIS, Aspose.CAD untuk Java memberi Anda cara bersih berbasis kode untuk melakukannya. Dalam tutorial ini kami akan menjelaskan langkah‑langkah tepat untuk **memuat file DWG**, mengiterasi entitasnya, dan membaca flag underlay yang sering diabaikan oleh banyak pengembang.

## Jawaban Cepat
- **Apa kelas utama untuk membuka DWG?** `com.aspose.cad.Image.load()` returns a `CadImage`.
- **Objek mana yang menyimpan informasi underlay?** `CadUnderlay` (or its derived types like `CadDgnUnderlay`).
- **Apakah saya memerlukan lisensi untuk pengembangan?** A free trial works for testing; a commercial license is required for production.
- **Bisakah saya memproses beberapa file DWG dalam loop?** Yes – just repeat the load‑and‑iterate pattern.
- **Apakah pendekatan ini kompatibel dengan Java 11+?** Absolutely, Aspose.CAD supports Java 8 through the latest LTS releases.

## Apa itu “load dwg file” dalam Aspose.CAD?
`Image.load()` membaca konten biner DWG dan membuat objek `CadImage` di memori. Dari sana Anda dapat menjelajahi layer, block, dan entitas underlay tanpa harus menangani format file DWG secara langsung.

## Mengapa mengekstrak flag underlay dari DWG?
Flag underlay memberi tahu Anda bagaimana referensi eksternal (seperti underlay DGN atau PDF) diposisikan, diskalakan, dan diputar di dalam gambar. Mengetahui nilai-nilai ini memungkinkan Anda untuk:
- Membuat kembali tata letak visual yang tepat dalam viewer khusus.
- Mengonversi underlay menjadi entitas CAD native untuk penyuntingan lebih lanjut.
- Menghasilkan laporan yang mencakup metadata underlay untuk kepatuhan atau dokumentasi.

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

## Panduan Langkah‑per‑Langkah

### Langkah 1: Atur Direktori Sumber Daya
```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "DWGDrawings/";
```
Tentukan di mana file DWG Anda berada. Menggunakan folder khusus menjaga contoh tetap bersih dan dapat dipindahkan.

### Langkah 2: Muat File DWG
```java
// Input file name and path
String fileName = dataDir + "BlockRefDgn.dwg";

// Load an existing DWG file and convert it into CadImage 
CadImage image = (CadImage)Image.load(fileName);
```
Di sini kami **memuat file dwg** `BlockRefDgn.dwg` ke dalam instance `CadImage`, siap untuk inspeksi.

### Langkah 3: Iterasi Entitas DWG
```java
// Go through each entity inside the DWG file
for(CadBaseEntity entity : image.getEntities())
```
Loop ini melintasi setiap entitas—garis, lingkaran, block, dan underlay—sehingga kami dapat memilih yang kami butuhkan.

### Langkah 4: Identifikasi Entitas CadDgnUnderlay
```java
// Check if entity is of CadDgnUnderlay type
if (entity instanceof CadDgnUnderlay)
```
Hanya objek `CadDgnUnderlay` yang berisi flag underlay yang kami cari, jadi kami menyaringnya.

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

## Masalah Umum & Tips
- **Null underlay path** – Pastikan DWG benar‑benar merujuk ke file eksternal; jika tidak, path akan kosong.
- **Unsupported underlay type** – Aspose.CAD saat ini mendukung underlay DGN; underlay PDF belum tersedia melalui API.
- **License exceptions** – Menjalankan kode tanpa lisensi yang valid akan menambahkan watermark pada gambar yang diekspor.

## Pertanyaan yang Sering Diajukan

**Q: Bisakah saya menggunakan Aspose.CAD untuk Java dengan format file CAD lain?**  
A: Aspose.CAD terutama berfokus pada format DWG, tetapi juga mendukung DXF, DWF, dan format CAD lainnya.

**Q: Apakah tersedia versi percobaan untuk Aspose.CAD untuk Java?**  
A: Ya, Anda dapat menjelajahi fitur dengan percobaan gratis dari [sini](https://releases.aspose.com/).

**Q: Bagaimana saya dapat mendapatkan dukungan atau bantuan dengan Aspose.CAD untuk Java?**  
A: Kunjungi [forum Aspose.CAD](https://forum.aspose.com/c/cad/19) untuk dukungan komunitas dan diskusi.

**Q: Apakah lisensi sementara tersedia untuk Aspose.CAD untuk Java?**  
A: Ya, Anda dapat memperoleh lisensi sementara [di sini](https://purchase.aspose.com/temporary-license/).

**Q: Di mana saya dapat menemukan dokumentasi lengkap untuk Aspose.CAD untuk Java?**  
A: Lihat [dokumentasi](https://reference.aspose.com/cad/java/) untuk informasi detail.

---

**Terakhir Diperbarui:** 2025-12-22  
**Diuji Dengan:** Aspose.CAD 24.12 untuk Java  
**Penulis:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}