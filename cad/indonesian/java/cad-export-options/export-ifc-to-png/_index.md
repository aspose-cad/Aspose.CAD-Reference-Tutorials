---
date: 2025-12-21
description: Ubah IFC menjadi PNG dengan mudah menggunakan Aspose.CAD untuk Java.
  Ikuti tutorial langkah demi langkah kami.
linktitle: Export IFC to PNG
second_title: Aspose.CAD Java API
title: Konversi IFC ke PNG dengan Aspose.CAD untuk Java
url: /id/java/cad-export-options/export-ifc-to-png/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Mengonversi IFC ke PNG dengan Aspose.CAD untuk Java

## Pendahuluan

Dalam tutorial ini Anda akan belajar **cara mengonversi IFC ke PNG** menggunakan pustaka Aspose.CAD yang kuat untuk Java. Baik Anda sedang membangun penampil BIM, menghasilkan thumbnail untuk portal konstruksi, atau mengotomatisasi alur kerja dokumentasi, mengonversi file IFC (Industry Foundation Classes) ke gambar raster adalah kebutuhan umum. Kami akan membimbing Anda melalui setiap langkah, menjelaskan alasan di balik pengaturan, dan memberi tips untuk mendapatkan hasil visual terbaik.

## Jawaban Cepat
- **Perpustakaan apa yang dibutuhkan?** Aspose.CAD untuk Java (tersedia versi percobaan gratis).  
- **Versi IFC yang didukung?** Sebagian besar file IFC 2x3 dan IFC4 dapat diproses.  
- **Waktu konversi tipikal?** Beberapa detik untuk model standar; tergantung pada ukuran file.  
- **Apakah saya memerlukan lisensi?** Lisensi sementara diperlukan untuk penggunaan produksi.  
- **Bisakah saya menyesuaikan ukuran gambar?** Ya – gunakan `CadRasterizationOptions` untuk mengatur lebar dan tinggi.

## Apa itu “convert IFC to PNG”?
Mengonversi IFC ke PNG berarti merasterisasi model bangunan 3‑D (IFC) menjadi gambar bitmap 2‑D (PNG). Proses ini meratakan geometri, menerapkan gaya visual default, dan menghasilkan gambar portabel yang dapat ditampilkan di peramban, laporan, atau aplikasi seluler tanpa memerlukan penampil CAD.

## Mengapa menggunakan Aspose.CAD untuk Java?
- **Tidak memerlukan perangkat lunak CAD eksternal** – API Java murni, bekerja di semua platform.  
- **Rendering berkualitas tinggi** – mempertahankan ketebalan garis, warna, dan lapisan.  
- **Kontrol penuh** – opsi rasterisasi memungkinkan Anda menentukan resolusi, latar belakang, dan lainnya.  
- **Lisensi mudah** – lisensi percobaan dan sementara mempermudah evaluasi.

## Prasyarat

Sebelum memulai, pastikan Anda memiliki:

- **Aspose.CAD Library** – unduh dan instal dari [download link](https://releases.aspose.com/cad/java/).  
- **Java Development Kit (JDK)** – versi 8 atau lebih baru.  
- **Folder** yang berisi file IFC yang ingin Anda konversi.

## Impor Namespace

Di proyek Java Anda, impor kelas yang diperlukan:

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.ifc.IfcImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

## Panduan Langkah‑per‑Langkah

### Langkah 1: Muat File IFC

```java
String dataDir = "Your Document Directory" + "ExportingIFC/";
String fileName = dataDir + "example.ifc";
IfcImage cadImage = (IfcImage)Image.load(fileName);
```

Di sini kami memuat file IFC sumber ke dalam objek `IfcImage`. Aspose.CAD secara otomatis mengurai struktur IFC dan menyiapkannya untuk rasterisasi.

### Langkah 2: Atur Opsi Vektor (Rasterisasi)

```java
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
```

`CadRasterizationOptions` mengontrol bagaimana geometri 3‑D diratakan. Sesuaikan `PageWidth` dan `PageHeight` agar sesuai dengan resolusi PNG yang diinginkan. Nilai yang lebih besar menghasilkan gambar dengan detail lebih tinggi tetapi meningkatkan penggunaan memori.

### Langkah 3: Konfigurasikan Pengaturan Ekspor PNG

```java
PngOptions pngOptions = new PngOptions();
pngOptions.setVectorRasterizationOptions(vectorOptions);
```

`PngOptions` memberi tahu Aspose.CAD untuk menghasilkan file PNG dan menghubungkan pengaturan rasterisasi yang telah didefinisikan pada langkah sebelumnya.

### Langkah 4: Simpan Gambar sebagai PNG

```java
String outPath = dataDir + "example.png";
cadImage.save(outPath, pngOptions);
```

Metode `save` menulis gambar yang telah dirasterisasi ke disk. Setelah baris ini dijalankan, Anda akan menemukan `example.png` di direktori yang sama dengan file IFC sumber Anda.

## Masalah Umum dan Solusinya

| Masalah | Mengapa Terjadi | Solusi |
|-------|----------------|-----|
| **Blank PNG output** | Opsi rasterisasi lebar/tinggi diatur ke 0 atau sangat kecil. | Pastikan `PageWidth` dan `PageHeight` adalah bilangan bulat positif (misalnya, 1500). |
| **Missing layers or colors** | Tampilan default mungkin menyembunyikan beberapa lapisan. | Gunakan `vectorOptions.setRenderMode(CadRenderMode.Wireframe)` atau sesuaikan visibilitas lapisan melalui API (jika diperlukan). |
| **Out‑of‑memory errors** for huge IFC files | Resolusi sangat tinggi mengonsumsi banyak RAM. | Turunkan resolusi atau proses model dalam bagian‑bagian. |

## FAQ

### Q1: Apakah Aspose.CAD kompatibel dengan semua versi file IFC?

A1: Aspose.CAD mendukung berbagai versi file IFC. Lihat [dokumentasi](https://reference.aspose.com/cad/java/) untuk detail kompatibilitas.

### Q2: Bisakah saya menyesuaikan opsi rasterisasi lebih lanjut?

A2: Tentu saja! Jelajahi [dokumentasi](https://reference.aspose.com/cad/java/) untuk opsi kustomisasi lanjutan.

### Q3: Apakah ada versi percobaan yang tersedia?

A3: Ya, Anda dapat mengakses versi percobaan gratis [di sini](https://releases.aspose.com/).

### Q4: Bagaimana cara mendapatkan lisensi sementara untuk Aspose.CAD?

A4: Dapatkan lisensi sementara dari [tautan ini](https://purchase.aspose.com/temporary-license/).

### Q5: Di mana saya dapat mencari bantuan atau mendiskusikan masalah?

A5: Kunjungi [forum Aspose.CAD](https://forum.aspose.com/c/cad/19) untuk dukungan komunitas.

## Pertanyaan yang Sering Diajukan (Tambahan)

**Q:** Bisakah saya mengonversi beberapa file IFC sekaligus?  
**A:** Ya. Bungkus logika pemuatan dan penyimpanan di dalam loop yang mengiterasi daftar jalur file.

**Q:** Bagaimana cara mengubah warna latar belakang PNG?  
**A:** Setel `vectorOptions.setBackgroundColor(Color.getWhite())` (atau `java.awt.Color` lainnya) sebelum membuat `PngOptions`.

**Q:** Apakah memungkinkan mengekspor ke format raster lain seperti JPEG atau BMP?  
**A:** Tentu. Ganti `PngOptions` dengan `JpegOptions` atau `BmpOptions` dan sesuaikan pengaturan khusus format bila diperlukan.

**Q:** Apakah saya perlu melepaskan sumber daya setelah konversi?  
**A:** Panggil `cadImage.dispose()` setelah selesai untuk membebaskan memori native.

---

**Last Updated:** 2025-12-21  
**Tested With:** Aspose.CAD for Java 24.12 (latest at time of writing)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}