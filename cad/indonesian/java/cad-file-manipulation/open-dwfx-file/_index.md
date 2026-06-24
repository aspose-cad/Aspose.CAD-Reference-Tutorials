---
date: 2026-02-23
description: Pelajari cara mengonversi DWFX ke PDF dan menyimpan CAD sebagai PDF menggunakan
  Aspose.CAD untuk Java. Panduan singkat untuk membuka file DWFX dan menghasilkan
  PDF.
linktitle: Open DWFX File
second_title: Aspose.CAD Java API
title: Konversi DWFX ke PDF dengan Aspose.CAD untuk Java
url: /id/java/cad-file-manipulation/open-dwfx-file/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Convert DWFX to PDF dengan Aspose.CAD untuk Java

## Pendahuluan

Dalam dunia desain yang bergerak cepat saat ini, pengembang sering perlu **convert DWFX to PDF** sehingga gambar CAD dapat dibagikan kepada pemangku kepentingan non‑teknis. Aspose.CAD for Java membuat tugas ini sederhana, memungkinkan Anda membuka file DWFX, merasternya, dan **save CAD as PDF** dengan hanya beberapa baris kode. Dalam tutorial ini kami akan membahas seluruh proses—dari menyiapkan lingkungan Anda hingga memverifikasi PDF akhir—sehingga Anda dapat menangani file DWFX dengan percaya diri dalam aplikasi Java Anda.

## Jawaban Cepat
- **Apa tujuan utama panduan ini?** Untuk menunjukkan cara mengonversi DWFX ke PDF menggunakan Aspose.CAD for Java.  
- **Perpustakaan mana yang diperlukan?** Aspose.CAD for Java (unduh dari situs resmi Aspose).  
- **Apakah saya memerlukan lisensi?** Versi percobaan gratis dapat digunakan untuk pengembangan; lisensi komersial diperlukan untuk produksi.  
- **Bisakah saya membuka file DWFX secara langsung?** Ya, gunakan `Image.load` untuk membuka file DWFX.  
- **Format output apa yang dihasilkan contoh ini?** File PDF yang disimpan ke direktori output yang ditentukan.

## Apa itu “convert DWFX to PDF”?

Mengonversi DWFX ke PDF berarti mengambil gambar DWFX berbasis vektor—yang umum digunakan dalam produk Autodesk—dan merendernya menjadi dokumen PDF yang portabel dan didukung secara luas. Hal ini memungkinkan tampilan, pencetakan, dan berbagi yang mudah tanpa memerlukan perangkat lunak CAD di sisi penerima.

## Mengapa menggunakan Aspose.CAD for Java untuk **save CAD as PDF**?

- **Tidak ada dependensi eksternal:** API Java murni, tidak memerlukan mesin CAD native.  
- **Rendering dengan fidelitas tinggi:** Mempertahankan ketebalan garis, warna, dan lapisan.  
- **Ramahan pemrosesan batch:** Ideal untuk otomatisasi sisi server atau layanan cloud.  
- **Cross‑platform:** Berfungsi di Windows, Linux, dan macOS.

## Prasyarat

Sebelum kami menyelam ke dalam kode, pastikan Anda memiliki hal‑hal berikut:

- **Aspose.CAD for Java Library** – Unduh dari [halaman unduhan Aspose.CAD for Java](https://releases.aspose.com/cad/java/).  
- **Java Development Environment** – JDK 8 atau lebih baru, dengan IDE atau alat build pilihan Anda.  
- **DWFX File** – File DWFX contoh (misalnya `Tyrannosaurus.dwfx`) untuk menguji konversi.

## Impor Namespace

Pertama, impor kelas‑kelas yang akan kami gunakan:

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Cara Mengonversi DWFX ke PDF menggunakan Aspose.CAD for Java

Berikut adalah penjelasan langkah demi langkah. Setiap langkah mencakup penjelasan singkat diikuti oleh kode tepat yang akan Anda jalankan.

### Langkah 1: Muat File DWFX  

```java
String SourceDir = Utils.getDataDir_DWFXDrawings();
String OutputDir = Utils.getDataDir_Output();
String filePath = SourceDir + "Tyrannosaurus.dwfx";

Image cadImageDwf = Image.load(filePath);
```

Metode `Image.load` membaca file DWFX ke dalam memori, memberikan kita objek `CadImage` yang siap untuk rasterisasi.

### Langkah 2: Atur Opsi Rasterisasi  

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(cadImageDwf.getSize().getWidth());
rasterizationOptions.setPageHeight(cadImageDwf.getSize().getHeight());
```

Opsi-opsi ini menentukan ukuran halaman output, memastikan PDF sesuai dengan dimensi gambar asli.

### Langkah 3: Konfigurasikan Opsi PDF  

```java
PdfOptions CADf = new PdfOptions();
CADf.setVectorRasterizationOptions(rasterizationOptions);
```

Di sini kami mengikat pengaturan rasterisasi ke konfigurasi ekspor PDF.

### Langkah 4: Simpan sebagai PDF  

```java
cadImageDwf.save(OutputDir + "OpenDwfxFile_out.pdf", CADf);
```

Memanggil `save` menulis gambar yang diraster ke file PDF di folder output.

### Langkah 5: Verifikasi Keberhasilan  

```java
System.out.println("OpenDwfxFile executed successfully");
```

Pesan konsol sederhana mengonfirmasi bahwa konversi selesai tanpa error.

## Masalah Umum dan Solusinya

| Masalah | Penyebab Kemungkinan | Solusi |
|-------|--------------|----------|
| **Output PDF kosong** | Lebar/tinggi rasterisasi diatur ke 0 | Pastikan `cadImageDwf.getSize()` mengembalikan dimensi yang valid sebelum mengatur opsi. |
| **Error out‑of‑memory** | File DWFX sangat besar | Tingkatkan ukuran heap JVM (`-Xmx2g`) atau proses file dalam bagian yang lebih kecil. |
| **Font hilang** | Font tidak tertanam dalam DWFX sumber | Instal font yang diperlukan di server atau gunakan `CadRasterizationOptions.setFontName` untuk menentukan fallback. |

## Pertanyaan yang Sering Diajukan

### Q1: Bisakah saya menggunakan Aspose.CAD for Java dengan format file CAD lainnya?  
A1: Ya, Aspose.CAD for Java mendukung berbagai format CAD, menyediakan solusi serbaguna bagi pengembang.

### Q2: Apakah tersedia percobaan gratis untuk Aspose.CAD for Java?  
A2: Ya, Anda dapat menjelajahi kemampuan Aspose.CAD for Java dengan percobaan gratis. Kunjungi [tautan ini](https://releases.aspose.com/) untuk memulai.

### Q3: Bagaimana saya dapat mendapatkan dukungan untuk Aspose.CAD for Java?  
A3: Bergabunglah dengan komunitas Aspose.CAD di [forum dukungan](https://forum.aspose.com/c/cad/19) untuk bantuan dan kolaborasi.

### Q4: Apakah lisensi sementara tersedia untuk Aspose.CAD for Java?  
A4: Ya, Anda dapat memperoleh lisensi sementara untuk Aspose.CAD for Java. Kunjungi [tautan ini](https://purchase.aspose.com/temporary-license/) untuk detail lebih lanjut.

### Q5: Di mana saya dapat menemukan dokumentasi untuk Aspose.CAD for Java?  
A5: Dokumentasi lengkap tersedia [di sini](https://reference.aspose.com/cad/java/).

---

**Terakhir Diperbarui:** 2026-02-23  
**Diuji Dengan:** Aspose.CAD for Java 24.11  
**Penulis:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}