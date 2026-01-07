---
date: 2026-01-07
description: Pelajari cara mengekspor CAD ke SVG dengan Aspose.CAD untuk Java. Panduan
  langkah demi langkah ini menunjukkan cara mengonversi DWG ke SVG, mengatur mode
  warna SVG, dan mengintegrasikan perpustakaan ke dalam proyek Java Anda.
linktitle: Export to SVG
second_title: Aspose.CAD Java API
title: Ekspor CAD ke SVG Menggunakan Aspose.CAD untuk Java
url: /id/java/cad-to-pdf-and-svg-export-options/export-to-svg/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ekspor CAD ke SVG Menggunakan Aspose.CAD untuk Java

## Pendahuluan

Selamat datang di dunia Aspose.CAD untuk Java, sebuah perpustakaan kuat yang memungkinkan pengembang memanipulasi gambar CAD dengan mudah. Baik Anda pengembang berpengalaman maupun pemula di bidang CAD, panduan komprehensif ini akan membawa Anda melalui **ekspor CAD ke SVG** langkah demi langkah, menunjukkan cara mengonversi DWG ke SVG, mengatur mode warna SVG, dan mengintegrasikan API ke dalam proyek Java Anda.

## Jawaban Cepat
- **Apa arti “ekspor CAD ke SVG”?** Itu mengonversi gambar CAD (misalnya DWG) menjadi file Scalable Vector Graphics yang dapat ditampilkan di peramban.  
- **Perpustakaan mana yang menangani konversi?** Aspose.CAD untuk Java menyediakan API sederhana untuk tugas ini.  
- **Apakah saya memerlukan lisensi untuk pengembangan?** Versi percobaan gratis cukup untuk pengujian; lisensi komersial diperlukan untuk produksi.  
- **Bisakah saya mengontrol output warna SVG?** Ya, Anda dapat mengatur mode warna SVG (misalnya grayscale).  
- **Apakah ada perangkat lunak tambahan yang diperlukan?** Hanya runtime Java dan file JAR Aspose.CAD.

## Prasyarat

Sebelum memulai tutorial, pastikan Anda memiliki prasyarat berikut:

- Lingkungan Pengembangan Java: Pastikan Java telah terpasang di sistem Anda.  
- Perpustakaan Aspose.CAD: Unduh dan instal Aspose.CAD untuk Java dari [tautan unduhan](https://releases.aspose.com/cad/java/).  
- Direktori Dokumen: Buat direktori untuk gambar CAD Anda, dan catat jalurnya.

## Impor Namespace

Pada langkah ini, kita akan mengimpor namespace yang diperlukan untuk memulai perjalanan Aspose.CAD Anda. Ikuti langkah-langkah berikut:

### Langkah 1: Buka Proyek Java Anda
Buka proyek Java Anda di IDE pilihan.

### Langkah 2: Tambahkan Perpustakaan Aspose.CAD
Tambahkan perpustakaan Aspose.CAD ke proyek Anda. Anda dapat melakukannya dengan menyertakan file JAR dalam dependensi proyek.

### Langkah 3: Impor Namespace
Di kelas Java Anda, impor namespace yang diperlukan:

```java
import com.aspose.cad.Image;
import com.aspose.cad.imageoptions.SvgOptions;
import com.aspose.cad.imageoptions.SvgColorMode;
```

## Ekspor CAD ke SVG

Setelah semua persiapan selesai, mari kita selami proses **ekspor CAD ke SVG** langkah demi langkah menggunakan Aspose.CAD untuk Java.

### Langkah 1: Tentukan Direktori Sumber Daya
Definisikan jalur ke direktori sumber daya Anda, tempat gambar CAD berada:

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

### Langkah 2: Muat Gambar CAD
Muat gambar CAD menggunakan perpustakaan Aspose.CAD:

```java
Image image = Image.load(dataDir + "meshes.dwg");
```

### Langkah 3: Konfigurasikan Opsi Ekspor SVG
Konfigurasikan opsi ekspor SVG untuk menyesuaikan output. Di sini kita **mengatur mode warna SVG** ke grayscale dan memberi tahu exporter untuk mengonversi teks menjadi bentuk:

```java
SvgOptions options = new SvgOptions();
options.setColorType(SvgColorMode.Grayscale);
options.setTextAsShapes(true);
```

### Langkah 4: Simpan sebagai SVG
Simpan gambar CAD sebagai file SVG:

```java
image.save(dataDir + "meshes.svg");
```

> **Tips pro:** Jika Anda perlu **mengonversi DWG ke SVG** sambil mempertahankan warna, ubah `SvgColorMode.Grayscale` menjadi `SvgColorMode.FullColor`.

Selamat! Anda telah berhasil mengekspor gambar CAD ke SVG menggunakan Aspose.CAD untuk Java.

## Mengapa Menggunakan Aspose.CAD untuk Ekspor CAD ke SVG?
- **Fidelity tinggi:** Data vektor dipertahankan, memastikan SVG terlihat persis seperti gambar CAD asli.  
- **Tanpa ketergantungan eksternal:** Konversi berjalan sepenuhnya di dalam Java, menghilangkan kebutuhan alat tambahan.  
- **Output dapat disesuaikan:** Opsi seperti `setColorType` memungkinkan Anda mengontrol apakah SVG berwarna abu-abu atau berwarna penuh.

## Masalah Umum dan Solusinya
- **File tidak ditemukan:** Pastikan `dataDir` mengarah ke folder yang benar dan nama file DWG cocok.  
- **Output SVG kosong:** Pastikan Anda telah mengatur `options.setTextAsShapes(true)` jika gambar berisi teks yang harus muncul sebagai bentuk.  
- **Format CAD tidak didukung:** Aspose.CAD mendukung DWG, DXF, DWF, dan beberapa format lainnya; periksa dokumentasi untuk daftar lengkapnya.

## Kesimpulan

Dalam tutorial ini, kami menjelajahi proses mulus memanfaatkan Aspose.CAD untuk Java guna **mengekspor CAD ke SVG**. Dengan API yang intuitif dan fitur yang kuat, Aspose.CAD menyederhanakan tugas kompleks, memberikan pengembang alat serbaguna untuk manipulasi CAD.

## FAQ

### Q1: Bisakah saya menggunakan Aspose.CAD untuk Java dengan format CAD lain?

A1: Ya, Aspose.CAD mendukung berbagai format CAD, termasuk DWG, DXF, DWF, dan lainnya.

### Q2: Apakah Aspose.CAD cocok untuk pemula maupun pengembang berpengalaman?

A2: Tentu! Aspose.CAD menawarkan API yang ramah pengguna, sehingga mudah diakses pemula, sekaligus menyediakan fitur lanjutan untuk pengembang berpengalaman.

### Q3: Di mana saya dapat menemukan dukungan tambahan atau diskusi komunitas?

A3: Kunjungi [Forum Aspose.CAD](https://forum.aspose.com/c/cad/19) untuk dukungan dan diskusi.

### Q4: Apakah ada versi percobaan gratis?

A4: Ya, Anda dapat menjelajahi Aspose.CAD dengan [percobaan gratis](https://releases.aspose.com/).

### Q5: Bagaimana cara membeli lisensi untuk Aspose.CAD untuk Java?

A5: Anda dapat membeli lisensi melalui [halaman pembelian](https://purchase.aspose.com/buy).

## Pertanyaan yang Sering Diajukan

**T: Bisakah saya mengonversi file DXF ke SVG menggunakan kode yang sama?**  
J: Ya, cukup ganti nama file dengan file DXF; API menangani kedua format tersebut.

**T: Bagaimana cara mengubah output menjadi SVG berwarna penuh?**  
J: Atur `options.setColorType(SvgColorMode.FullColor);` sebelum menyimpan.

**T: Apakah memungkinkan menyematkan font dalam SVG yang dihasilkan?**  
J: Aspose.CAD saat ini mengonversi teks menjadi bentuk; penyematan font tidak diperlukan.

**T: Apakah perpustakaan ini bekerja di Linux dan macOS?**  
J: Perpustakaan Java bersifat platform‑independen dan berjalan di mana saja JVM yang kompatibel tersedia.

**T: Versi Aspose.CAD apa yang digunakan dalam tutorial ini?**  
J: Contoh ini diuji dengan Aspose.CAD untuk Java 24.10.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Terakhir Diperbarui:** 2026-01-07  
**Diuji Dengan:** Aspose.CAD untuk Java 24.10  
**Penulis:** Aspose  

---