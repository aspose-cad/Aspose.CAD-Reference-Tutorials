---
date: 2025-11-30
description: Pelajari cara menambahkan properti khusus pada file DWG di Java menggunakan
  Aspose.CAD. Tingkatkan organisasi dan pengambilan informasi dalam gambar CAD dengan
  mudah.
language: id
linktitle: Add Custom Properties to DWG Files Using Java
second_title: Aspose.CAD Java API
title: Tambahkan Properti Kustom pada File DWG Menggunakan Aspose.CAD untuk Java
url: /java/additional-features/add-custom-properties/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Tambahkan Properti Kustom pada File DWG Menggunakan Aspose.CAD untuk Java

Manipulasi gambar CAD secara programatik adalah kebutuhan harian bagi banyak pengembang Java. Dalam tutorial ini Anda akan menemukan **cara menambahkan properti kustom pada file dwg** menggunakan pustaka Aspose.CAD untuk Java yang kuat. Pada akhir panduan, Anda akan memiliki potongan kode yang dapat digunakan kembali yang menyisipkan metadata langsung ke header file DWG, membuat gambar Anda lebih mudah dikatalogkan, dicari, dan dipelihara.

## Pendahuluan

Aspose.CAD untuk Java adalah pustaka yang sepenuhnya dikelola tanpa .NET yang memungkinkan Anda membaca, mengedit, dan menulis berbagai format CAD tanpa memerlukan AutoCAD. Menambahkan properti kustom ke file DWG memberi Anda cara ringan untuk menyimpan informasi tambahan—seperti kode proyek, catatan revisi, atau detail pemilik—langsung di dalam file gambar itu sendiri.

## Jawaban Cepat
- **Apa arti “add custom properties dwg”?** Artinya memasukkan pasangan nama/nilai yang ditentukan pengguna ke dalam metadata header file DWG.  
- **Library mana yang menangani ini?** Aspose.CAD untuk Java menyediakan API sederhana untuk membaca dan menulis properti tersebut.  
- **Berapa lama implementasinya?** Biasanya 5‑10 menit untuk contoh dasar.  
- **Apakah saya memerlukan lisensi?** Versi percobaan gratis dapat digunakan untuk pengembangan; lisensi komersial diperlukan untuk produksi.  
- **Apakah kompatibel dengan format CAD lain?** Ya—DXF, DWF, dan lainnya didukung.

## Apa Itu Menambahkan Properti Kustom ke File DWG?

Properti kustom adalah pasangan kunci‑nilai yang disimpan di header DWG. Mereka tidak ditampilkan dalam geometri gambar tetapi dapat diakses oleh aplikasi yang mendukung CAD, memungkinkan manajemen data yang lebih baik, pelaporan otomatis, dan integrasi dengan sistem PLM.

## Mengapa Menggunakan Aspose.CAD untuk Tugas Ini?

- **Tanpa ketergantungan AutoCAD** – berfungsi di semua OS atau pipeline CI.  
- **API lengkap** – membaca, memodifikasi, dan menyimpan tanpa kehilangan kualitas.  
- **Kinerja tinggi** – memproses gambar besar dalam hitungan detik.  
- **Dukungan lintas format** – kode yang sama berfungsi untuk DXF, DWF, dan lainnya.

## Prasyarat

Sebelum memulai, pastikan Anda memiliki:

- **Java Development Kit (JDK) 8+** terpasang dan dikonfigurasi di IDE Anda.  
- Pustaka **Aspose.CAD untuk Java** – unduh JAR terbaru dari [halaman unduhan Aspose.CAD](https://releases.aspose.com/cad/java/).  
- **File DWG/DXF contoh** untuk percobaan (tutorial ini menggunakan `conic_pyramid.dxf`).

## Impor Namespace

Tambahkan impor yang diperlukan ke kelas Java Anda agar dapat bekerja dengan objek Aspose.CAD.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;

import java.util.Map;
```

## Panduan Langkah‑per‑Langkah

### Langkah 1: Siapkan Proyek Anda

Buat proyek Maven/Gradle baru (atau proyek IDE sederhana) dan letakkan JAR Aspose.CAD pada classpath. Ini memastikan paket `com.aspose.cad.*` tersedia saat kompilasi.

### Langkah 2: Tentukan Jalur File

Tentukan lokasi file gambar sumber dan tempat file yang telah dimodifikasi akan disimpan.

```java
String dataDir = "Your Document Directory" + "DXFDrawings/";
String srcFile = dataDir + "conic_pyramid.dxf";
String outFile = dataDir + "AddCustomProperties_out.dxf";
```

### Langkah 3: Muat File DWG

Gunakan metode statis `Image.load` untuk membaca gambar ke dalam objek `CadImage`.

```java
CadImage cadImage = (CadImage)Image.load(srcFile);
```

### Langkah 4: Tambahkan Properti Kustom

Sisipkan metadata Anda langsung ke header gambar. Setiap pemanggilan menambahkan pasangan nama/nilai baru.

```java
cadImage.getHeader().getCustomProperties().put("CUSTOM_PROPERTY_1", "Custom property test 1");
cadImage.getHeader().getCustomProperties().put("CUSTOM_PROPERTY_2", "Custom property test 2");
cadImage.getHeader().getCustomProperties().put("CUSTOM_PROPERTY_3", "Custom property test 3");
```

> **Tip:** Jaga nama properti tetap singkat (maks 31 karakter) dan hindari spasi untuk mempertahankan kompatibilitas dengan penampil CAD lama.

### Langkah 5: Simpan File DWG yang Dimodifikasi

Simpan perubahan dengan memanggil `save`. File output kini berisi properti kustom yang Anda tambahkan.

```java
cadImage.save(outFile);
```

### Langkah 6: Jalankan Kode

Jalankan program dari IDE atau baris perintah Anda. Jika semuanya telah disiapkan dengan benar, Anda akan melihat pesan konfirmasi.

```java
System.out.println("\nAddCustomProperties executed successfully.");
```

## Masalah Umum & Solusi

| Problem | Likely Cause | Fix |
|---------|--------------|-----|
| **`java.lang.NoClassDefFoundError: com/aspose/cad/Image`** | JAR Aspose.CAD tidak berada di classpath | Tambahkan JAR ke folder `libs` proyek Anda atau deklarasikan di Maven/Gradle. |
| **Properties not appearing in the saved file** | Menggunakan versi DWG yang tidak mendukung properti kustom | Pastikan Anda bekerja dengan versi DWG/DXF 2000 atau lebih baru; format lama mungkin mengabaikan header kustom. |
| **`OutOfMemoryError` on large files** | Muat gambar yang sangat besar tanpa streaming | Gunakan `Image.load` dengan objek `LoadOptions` yang mengaktifkan pemuatan efisien memori. |

## Pertanyaan yang Sering Diajukan

**Q: Bisakah saya menambahkan properti kustom ke format file CAD lain?**  
A: Ya. Aspose.CAD untuk Java mendukung DXF, DWF, DGN, dan lainnya, dan API `getHeader().getCustomProperties()` yang sama berfungsi di semua format tersebut.

**Q: Apakah Aspose.CAD untuk Java kompatibel dengan semua IDE utama?**  
A: Tentu saja. Ia bekerja dengan Eclipse, IntelliJ IDEA, NetBeans, dan bahkan build baris perintah sederhana.

**Q: Di mana saya dapat menemukan contoh lebih banyak dan dokumentasi detail?**  
A: Kunjungi [Referensi API Aspose.CAD Java resmi](https://reference.aspose.com/cad/java/) untuk daftar lengkap kelas, metode, dan proyek contoh.

**Q: Bisakah saya mencoba Aspose.CAD untuk Java sebelum membeli?**  
A: Ya—unduh percobaan gratis 30‑hari dari [halaman unduhan Aspose.CAD](https://releases.aspose.com/).

**Q: Bagaimana cara mendapatkan dukungan jika saya mengalami kesulitan?**  
A: Forum komunitas Aspose dan [portal dukungan Aspose.CAD](https://forum.aspose.com/c/cad/19) yang khusus adalah tempat yang bagus untuk mengajukan pertanyaan dan berbagi solusi.

---

**Terakhir Diperbarui:** 2025-11-30  
**Diuji Dengan:** Aspose.CAD for Java 24.11  
**Penulis:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}