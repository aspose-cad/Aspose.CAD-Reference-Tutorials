---
date: 2026-02-15
description: Pelajari cara mengatur ukuran halaman kustom dan membuat PDF dari CAD
  menggunakan Aspose.CAD untuk Java. Panduan langkah demi langkah ini mencakup mengekspor
  CAD ke PDF dengan Auto Layout Scaling.
linktitle: Setting Auto Layout Scaling
second_title: Aspose.CAD Java API
title: Atur Ukuran Halaman Kustom – PDF dari CAD dengan Skala Tata Letak Otomatis
url: /id/java/advanced-cad-features/setting-auto-layout-scaling/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Atur Ukuran Halaman Kustom – Buat PDF dari CAD dengan Skala Tata Letak Otomatis

## Pendahuluan

Jika Anda perlu **atur ukuran halaman kustom** saat Anda **membuat PDF dari CAD** file dengan cepat dan skala yang sempurna, Aspose.CAD for Java siap membantu Anda. Auto Layout Scaling secara otomatis menyesuaikan dimensi tata letak sehingga PDF yang dihasilkan terlihat persis seperti yang diharapkan, terlepas dari ukuran halaman CAD asli. Dalam tutorial ini kami akan membahas proses lengkap—dari memuat file DXF hingga mengekspor PDF—sementara menyoroti kemampuan **export CAD to PDF** perpustakaan dan menunjukkan bagaimana Anda juga dapat **convert DWG to PDF** atau **increase PDF resolution** bila diperlukan.

## Jawaban Cepat
- **Apa yang dilakukan Auto Layout Scaling?** Ia secara otomatis mengubah ukuran tata letak CAD agar sesuai dengan dimensi halaman target saat rasterisasi.
- **Format apa yang dapat saya konversi?** Setiap format yang didukung oleh Aspose.CAD (misalnya, DXF, DWG, DWF) dapat dikonversi ke PDF.
- **Apakah saya memerlukan lisensi untuk produksi?** Ya, lisensi komersial diperlukan untuk penggunaan non‑evaluasi.
- **Berapa lama proses konversi berlangsung?** Biasanya kurang dari satu detik untuk file standar pada perangkat keras modern.
- **Apakah saya dapat mengubah ukuran halaman?** Ya, Anda dapat mengatur dimensi halaman kustom melalui `CadRasterizationOptions`.

## Apa itu “create PDF from CAD”?

Membuat PDF dari CAD berarti mengambil gambar teknik berbasis vektor (DXF, DWG, dll.) dan merasternya menjadi dokumen PDF. PDF tersebut mempertahankan kesetiaan visual gambar asli sekaligus dapat dilihat secara luas di platform apa pun.

## Mengapa menggunakan Auto Layout Scaling?

- **Output konsisten:** Menjamin semua tata letak mengisi halaman PDF tanpa perhitungan ukuran manual.
- **Menghemat waktu:** Menghilangkan kebutuhan untuk menyesuaikan faktor skala secara manual untuk setiap gambar.
- **Kualitas tinggi:** Mempertahankan ketebalan garis dan akurasi geometri selama konversi.
- **Fleksibilitas:** Berfungsi untuk **convert dxf to pdf**, **convert dwg to pdf**, dan bahkan ketika Anda perlu **increase PDF resolution** untuk file siap cetak.

## Prasyarat

1. **Aspose.CAD for Java Library** – unduh versi terbaru dari [download page](https://releases.aspose.com/cad/java/).  
2. **Resource Directory** – buat folder di mesin Anda untuk menyimpan file CAD; ganti `"Your Document Directory"` dalam kode dengan jalur tersebut.  
3. **Sample CAD File** – untuk panduan ini kami akan menggunakan `conic_pyramid.dxf`, yang termasuk dalam set data contoh Aspose.

## Impor Namespace

Pertama, impor kelas yang diperlukan. Ini memberi kami akses ke fitur pemuatan gambar, rasterisasi, dan ekspor PDF.

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Cara Mengatur Ukuran Halaman Kustom untuk PDF dari CAD

Sebelum kita masuk ke kode langkah demi langkah, mari pahami mengapa **atur ukuran halaman kustom** penting. Saat Anda **atur ukuran halaman kustom**, Anda mengontrol dimensi fisik PDF yang dihasilkan (misalnya, A4, Letter, atau ukuran khusus). Ini penting untuk alur kerja teknik di mana gambar harus sesuai dengan standar lembar atau ketika Anda perlu menyematkan PDF ke dalam dokumen yang lebih besar.

### Langkah 1: Muat File CAD

Memuat file sumber adalah langkah pertama dalam **how to export CAD** ke dokumen PDF.

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

### Langkah 2: Buat Opsi Rasterisasi

Tentukan dimensi halaman target. Anda juga dapat menggunakan blok ini untuk **set CAD page size** secara manual jika Anda menginginkan tata letak kustom.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
```

### Langkah 3: Atur Auto Layout Scaling

Aktifkan fitur skala otomatis. Ini adalah inti dari **how to set scaling** untuk konversi CAD‑to‑PDF.

```java
rasterizationOptions.setAutomaticLayoutsScaling(true);
```

### Langkah 4: Buat Opsi PDF

Hubungkan pengaturan rasterisasi ke opsi ekspor PDF.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### Langkah 5: Ekspor ke PDF

Akhirnya, simpan gambar yang dirender sebagai file PDF. Langkah ini menyelesaikan alur kerja **convert dxf to pdf**.

```java
image.save(dataDir + "result_out_.pdf", pdfOptions);
```

Ulangi langkah-langkah di atas untuk file CAD tambahan yang perlu Anda proses, baik itu **DWG**, **DWF**, atau format lain yang didukung.

## Kasus Penggunaan Umum

| Skenario | Mengapa mengatur ukuran halaman kustom? |
|----------|----------------------------------------|
| **Pengajuan gambar konstruksi** | Menyelaraskan PDF dengan ukuran lembar standar A1/A2 yang diperlukan oleh badan regulasi. |
| **Penyematan dalam manual teknis** | Menjamin gambar sesuai dengan tata letak manual yang telah ditentukan tanpa skala tambahan. |
| **Pencetakan resolusi tinggi** | Memungkinkan Anda meningkatkan DPI (misalnya, `rasterizationOptions.setResolution(300)`) sambil menjaga konsistensi dimensi halaman. |

## Masalah Umum & Pemecahan Masalah

| Gejala | Penyebab Kemungkinan | Perbaikan |
|--------|----------------------|-----------|
| Output PDF kosong | Opsi rasterisasi tidak diatur atau jalur file tidak benar | Verifikasi jalur `srcFile` dan pastikan `setPageWidth/Height` tidak nol |
| Skala terdistorsi | `setAutomaticLayoutsScaling` dibiarkan `false` | Aktifkan skala otomatis atau hitung faktor skala secara manual |
| Lapisan hilang | DXF sumber berisi entitas yang tidak didukung | Periksa catatan rilis Aspose.CAD untuk tipe entitas yang didukung |

## Pertanyaan yang Sering Diajukan

**Q: Apakah Aspose.CAD for Java kompatibel dengan semua format file CAD?**  
A: Aspose.CAD for Java mendukung berbagai format CAD, termasuk DWG, DXF, dan DWF.

**Q: Dapatkah saya menyesuaikan opsi skala lebih lanjut?**  
A: Ya, kelas `CadRasterizationOptions` menyediakan properti untuk penyetelan halus skala, DPI, dan pengaturan rasterisasi lainnya.

**Q: Di mana saya dapat menemukan dokumentasi tambahan untuk Aspose.CAD for Java?**  
A: Lihat [documentation](https://reference.aspose.com/cad/java/) untuk informasi mendalam dan contoh.

**Q: Apakah ada percobaan gratis yang tersedia untuk Aspose.CAD for Java?**  
A: Ya, Anda dapat menjelajahi [free trial](https://releases.aspose.com/) untuk merasakan kemampuan Aspose.CAD for Java.

**Q: Bagaimana saya dapat mencari bantuan atau berpartisipasi dalam diskusi tentang Aspose.CAD for Java?**  
A: Kunjungi [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) untuk terhubung dengan komunitas dan mencari dukungan.

**Pertanyaan Umum Tambahan**

**Q: Bagaimana cara mengonversi file DWG ke PDF alih-alih DXF?**  
A: Kode yang sama berfungsi; cukup ubah ekstensi file di `srcFile` menjadi `.dwg`.

**Q: Dapatkah saya mengatur DPI kustom untuk PDF resolusi lebih tinggi?**  
A: Ya, gunakan `rasterizationOptions.setResolution(300);` (atau DPI apa pun yang Anda butuhkan).

**Q: Apakah memungkinkan untuk menyematkan font dalam PDF yang dihasilkan?**  
A: Aspose.CAD meraster gambar, sehingga font dirender sebagai vektor; tidak diperlukan penyematan font terpisah.

## Kesimpulan

Dengan mengikuti panduan ini Anda kini tahu cara **set custom page size** dan **create PDF from CAD** file menggunakan Aspose.CAD for Java dengan Auto Layout Scaling. Proses ini menyederhanakan alur kerja **export CAD to PDF**, memastikan skala yang konsisten, dan menghemat waktu pengembangan Anda. Silakan bereksperimen dengan ukuran halaman, resolusi, dan format CAD yang berbeda untuk memenuhi kebutuhan proyek Anda, apakah Anda **converting DWG to PDF**, **increasing PDF resolution**, atau membangun pemroses batch **java CAD to PDF**.

---

**Terakhir Diperbarui:** 2026-02-15  
**Diuji Dengan:** Aspose.CAD for Java 24.12 (latest)  
**Penulis:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}