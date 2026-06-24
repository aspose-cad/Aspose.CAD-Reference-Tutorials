---
date: 2026-05-04
description: Pelajari cara mengonversi file CAD PDF dengan mengekspor DGN ke PDF AutoCAD
  menggunakan Aspose.CAD untuk Java. Panduan langkah demi langkah dengan ukuran PDF
  yang dapat disesuaikan dan opsi-opsi.
keywords:
- convert cad pdf
- how to export dgn
- customize pdf size
- aspose cad download
- set pdf options
linktitle: Mengekspor DGN dalam Format AutoCAD ke PDF
second_title: Aspose.CAD Java API
title: Konversi CAD PDF – Ekspor DGN ke PDF AutoCAD dengan Mudah menggunakan Aspose.CAD
  untuk Java
url: /id/java/dgn-export-options/exporting-dgn-to-pdf/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Konversi CAD PDF: Ekspor DGN ke PDF AutoCAD dengan Mudah menggunakan Aspose.CAD untuk Java

## Pendahuluan

Jika Anda perlu **mengonversi CAD PDF** secara langsung dari sumber DGN, Anda berada di tempat yang tepat. Dalam tutorial ini kami akan memandu Anda menggunakan Aspose.CAD untuk Java untuk mengekspor file DGN ke PDF yang kompatibel dengan AutoCAD. Anda akan melihat cara mengatur dimensi halaman khusus, memilih tata letak tertentu, dan menyempurnakan output PDF—semua dengan kode langkah‑demi‑langkah yang jelas dan dapat langsung Anda gunakan dalam proyek Anda.

## Jawaban Cepat
- **Apa arti “convert CAD PDF”?** Ini merujuk pada transformasi file sumber CAD (seperti DGN) menjadi PDF yang mempertahankan data vektor dan kesetiaan tata letak.  
- **Perpustakaan mana yang menangani konversi?** Aspose.CAD untuk Java menyediakan percobaan bebas lisensi yang andal untuk tugas ini.  
- **Apakah saya memerlukan lisensi untuk pengembangan?** Percobaan gratis dapat digunakan untuk pengujian; lisensi komersial diperlukan untuk penggunaan produksi.  
- **Bisakah saya menyesuaikan ukuran PDF?** Ya – `CadRasterizationOptions` memungkinkan Anda mengatur lebar, tinggi, dan skala halaman.  
- **Berapa banyak baris kode yang diperlukan?** Kurang dari 20 baris kode Java untuk memuat, mengonfigurasi, dan menyimpan PDF.

## Apa itu “convert CAD PDF”?
Mengonversi CAD PDF berarti mengambil gambar CAD asli (misalnya DGN) dan menghasilkan PDF yang mempertahankan grafik vektor, lapisan, dan informasi tata letak asli. PDF yang dihasilkan dapat dilihat di perangkat apa pun tanpa memerlukan perangkat lunak CAD, menjadikannya ideal untuk berbagi, mencetak, atau mengarsipkan.

## Mengapa menggunakan Aspose.CAD untuk Java untuk mengonversi CAD PDF?
- **Dukungan format lengkap** – DGN, DWG, DXF, dan banyak lagi.  
- **Tanpa ketergantungan eksternal** – Java murni, tanpa DLL native.  
- **Kontrol detail** – Anda dapat memilih tata letak yang akan diekspor, mengatur ukuran halaman khusus, dan mengendalikan kualitas rasterisasi.  
- **Skalabel untuk pekerjaan batch** – memuat dan menyimpan puluhan file dalam loop dengan overhead minimal.

## Prasyarat
Sebelum kita mulai, pastikan Anda memiliki hal‑hal berikut:

- **Perpustakaan Aspose.CAD** – unduh [di sini](https://releases.aspose.com/cad/java/).  
- **Direktori Dokumen** – folder di mesin Anda tempat file DGN masuk dan PDF keluar akan disimpan.

## Impor Paket

Di proyek Java Anda, impor paket yang diperlukan untuk mengakses fungsionalitas Aspose.CAD:

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

Sekarang, mari kita uraikan contoh kode menjadi beberapa langkah:

## Langkah 1: Tentukan Jalur File (cara mengekspor dgn)

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "Nikon_D90_Camera.dgn";
String outFile  = dataDir + "Nikon_D90_Camera.pdf";
```

Pastikan untuk mengganti `"Your Document Directory"` dengan jalur sebenarnya tempat file Anda berada.

## Langkah 2: Muat Gambar DGN

```java
DgnImage objImage = (DgnImage) Image.load(fileName);
```

Muat file DGN menggunakan Aspose.CAD.

## Langkah 3: Atur Opsi Ekspor PDF (sesuaikan ukuran pdf, atur opsi pdf)

```java
PdfOptions options = new PdfOptions();
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
vectorOptions.setAutomaticLayoutsScaling(true);
vectorOptions.setLayouts(new String[] { "1", "2", "3", "9" }); // Export specific views
options.setVectorRasterizationOptions(vectorOptions);
```

Di sini kami mendefinisikan opsi ekspor PDF, termasuk dimensi halaman, skala otomatis, dan tata letak DGN (view) spesifik yang ingin Anda sertakan dalam PDF akhir.

## Langkah 4: Simpan File PDF

```java
objImage.save(outFile, options);
```

Simpan file PDF yang telah diekspor. Metode `save` menerapkan semua opsi yang Anda konfigurasikan pada langkah sebelumnya.

Ulangi langkah‑langkah ini untuk setiap file DGN tambahan yang ingin Anda konversi. Selamat! Anda telah berhasil **mengonversi CAD PDF** dengan mengekspor file DGN ke format AutoCAD dalam PDF menggunakan Aspose.CAD untuk Java.

## Masalah Umum dan Solusinya
| Masalah | Mengapa Terjadi | Solusi |
|-------|----------------|-----|
| **File tidak ditemukan** | Jalur `dataDir` salah | Periksa kembali jalur folder dan pastikan file DGN ada. |
| **Halaman kosong di PDF** | `AutomaticLayoutsScaling` disetel ke `false` atau ID tata letak hilang | Pertahankan `setAutomaticLayoutsScaling(true)` dan verifikasi nama tata letak (`"1","2",…`). |
| **Output beresolusi rendah** | DPI rasterisasi default rendah | Gunakan `vectorOptions.setResolution(300);` untuk meningkatkan kualitas (tambahkan sebelum `setVectorRasterizationOptions`). |
| **Pengecualian lisensi** | Menjalankan tanpa lisensi yang valid di produksi | Terapkan lisensi sementara atau berbayar seperti yang dijelaskan dalam dokumentasi Aspose. |

## Pertanyaan yang Sering Diajukan (Tambahan)

**T: Bisakah saya mengekspor hanya satu tata letak dari file DGN multi‑tata letak?**  
J: Ya – tentukan ID tata letak yang diinginkan dalam `vectorOptions.setLayouts(new String[] { "2" });`.

**T: Apakah memungkinkan menyematkan font dalam PDF yang dihasilkan?**  
J: Aspose.CAD secara otomatis menyematkan font yang diperlukan saat data vektor dirasterisasi; Anda juga dapat mengontrol penyematan font melalui `PdfOptions` bila diperlukan.

**T: Bagaimana cara memproses banyak file DGN secara batch?**  
J: Bungkus langkah‑langkah tersebut dalam loop `for` yang iterasi atas daftar nama file, menggunakan instance `PdfOptions` yang sama untuk setiap iterasi.

**T: Apakah perpustakaan mendukung PDF yang dilindungi kata sandi?**  
J: Ya – Anda dapat menetapkan kata sandi pada objek `PdfOptions` melalui `options.setPassword("yourPassword");`.

**T: Di mana saya dapat menemukan contoh lain?**  
J: Dokumentasi resmi Aspose.CAD dan repositori contoh berisi banyak skenario tambahan.

## FAQ's (Asli)

### Q1: Apakah Aspose.CAD kompatibel dengan semua format file CAD?

A1: Ya, Aspose.CAD mendukung beragam format CAD, memastikan fleksibilitas dalam menangani berbagai tipe file.

### Q2: Bisakah saya menyesuaikan pengaturan ekspor PDF?

A2: Tentu. Seperti yang ditunjukkan dalam tutorial, Anda dapat menyesuaikan opsi seperti dimensi halaman dan tata letak sesuai kebutuhan.

### Q3: Di mana saya dapat menemukan dukungan atau bantuan tambahan?

A3: Kunjungi [forum Aspose.CAD](https://forum.aspose.com/c/cad/19) untuk dukungan komunitas dan diskusi.

### Q4: Apakah ada percobaan gratis yang tersedia?

A4: Ya, Anda dapat mengakses percobaan gratis [di sini](https://releases.aspose.com/).

### Q5: Bagaimana cara mendapatkan lisensi sementara?

A5: Dapatkan lisensi sementara [di sini](https://purchase.aspose.com/temporary-license/).

## Kesimpulan

Dalam tutorial ini kami menjelaskan cara **mengonversi CAD PDF** dengan memanfaatkan Aspose.CAD untuk Java. Dengan hanya beberapa baris kode Anda dapat memuat gambar DGN, menyempurnakan opsi ekspor PDF, dan menghasilkan PDF berkualitas tinggi siap untuk dibagikan atau diarsipkan. Jangan ragu untuk bereksperimen dengan ukuran halaman, tata letak, atau pemrosesan batch yang berbeda agar sesuai dengan kebutuhan proyek Anda.

---

**Terakhir Diperbarui:** 2026-05-04  
**Diuji Dengan:** Aspose.CAD untuk Java 24.12  
**Penulis:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}