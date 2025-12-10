---
date: 2025-12-10
description: Pelajari cara membuat PDF dari CAD menggunakan Aspose.CAD untuk Java
  dengan Auto Layout Scaling. Panduan langkah demi langkah ini menunjukkan cara mengekspor
  CAD ke PDF secara efisien dan dapat diandalkan.
linktitle: Setting Auto Layout Scaling
second_title: Aspose.CAD Java API
title: Buat PDF dari CAD – Skala Tata Letak Otomatis dengan Aspose.CAD Java
url: /id/java/advanced-cad-features/setting-auto-layout-scaling/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Buat PDF dari CAD – Auto Layout Scaling dengan Aspose.CAD Java

## Pendahuluan

Jika Anda perlu **membuat PDF dari CAD** dengan cepat dan dengan skala yang sempurna, Aspose.CAD untuk Java siap membantu. Auto Layout Scaling secara otomatis menyesuaikan dimensi tata letak sehingga PDF yang dihasilkan terlihat persis seperti yang diharapkan, terlepas dari ukuran halaman CAD asli. Dalam tutorial ini kami akan membahas proses lengkap—dari memuat file DXF hingga mengekspor PDF—sementara menyoroti kemampuan **export CAD to PDF** dari perpustakaan.

## Jawaban Cepat
- **Apa yang dilakukan Auto Layout Scaling?** Itu secara otomatis mengubah ukuran tata letak CAD agar sesuai dengan dimensi halaman target saat rasterisasi.
- **Format apa yang dapat saya konversi?** Semua format yang didukung oleh Aspose.CAD (misalnya, DXF, DWG, DWF) dapat dikonversi ke PDF.
- **Apakah saya memerlukan lisensi untuk produksi?** Ya, lisensi komersial diperlukan untuk penggunaan non‑evaluasi.
- **Berapa lama proses konversi?** Biasanya kurang dari satu detik untuk file standar pada perangkat keras modern.
- **Bisakah saya mengubah ukuran halaman?** Ya, Anda dapat mengatur dimensi halaman khusus melalui `CadRasterizationOptions`.

## Apa itu “membuat PDF dari CAD”?
Membuat PDF dari CAD berarti mengambil gambar teknik berbasis vektor (DXF, DWG, dll.) dan merasternya menjadi dokumen PDF. PDF tersebut mempertahankan kesetiaan visual gambar asli sekaligus dapat dilihat secara luas di platform apa pun.

## Mengapa menggunakan Auto Layout Scaling?
- **Output konsisten:** Menjamin semua tata letak mengisi halaman PDF tanpa perhitungan ukuran manual.
- **Menghemat waktu:** Menghilangkan kebutuhan untuk menyesuaikan faktor skala secara manual untuk setiap gambar.
- **Kualitas tinggi:** Mempertahankan ketebalan garis dan akurasi geometri selama konversi.

## Prasyarat

1. **Aspose.CAD for Java Library** – unduh versi terbaru dari [halaman unduhan](https://releases.aspose.com/cad/java/).  
2. **Direktori Sumber Daya** – buat folder di mesin Anda untuk menyimpan file CAD; ganti `"Your Document Directory"` dalam kode dengan jalur tersebut.  
3. **File CAD Contoh** – untuk panduan ini kami akan menggunakan `conic_pyramid.dxf`, yang termasuk dalam set data contoh Aspose.

## Impor Namespace

Pertama, impor kelas yang diperlukan. Ini memberi kami akses ke pemuatan gambar, rasterisasi, dan fitur ekspor PDF.

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Langkah 1: Muat File CAD

Memuat file sumber adalah langkah pertama dalam **cara mengekspor CAD** ke dokumen PDF.

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

## Langkah 2: Buat Opsi Rasterisasi

Tentukan dimensi halaman target. Anda juga dapat menggunakan blok ini untuk **mengatur ukuran halaman CAD** secara manual jika menginginkan tata letak khusus.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
```

## Langkah 3: Atur Auto Layout Scaling

Aktifkan fitur skala otomatis. Ini adalah inti dari **cara mengatur skala** untuk konversi CAD‑ke‑PDF.

```java
rasterizationOptions.setAutomaticLayoutsScaling(true);
```

## Langkah 4: Buat Opsi PDF

Hubungkan pengaturan rasterisasi ke opsi ekspor PDF.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## Langkah 5: Ekspor ke PDF

Akhirnya, simpan gambar yang dirender sebagai file PDF. Langkah ini menyelesaikan alur kerja **konversi DXF ke PDF**.

```java
image.save(dataDir + "result_out_.pdf", pdfOptions);
```

Ulangi langkah-langkah di atas untuk file CAD tambahan yang perlu Anda proses.

## Masalah Umum & Pemecahan Masalah

| Gejala | Penyebab Kemungkinan | Solusi |
|---------|----------------------|--------|
| PDF kosong | Opsi rasterisasi tidak diatur atau jalur file salah | Verifikasi jalur `srcFile` dan pastikan `setPageWidth/Height` tidak nol |
| Skala terdistorsi | `setAutomaticLayoutsScaling` dibiarkan `false` | Aktifkan skala otomatis atau hitung faktor skala secara manual |
| Lapisan hilang | DXF sumber berisi entitas yang tidak didukung | Periksa catatan rilis Aspose.CAD untuk tipe entitas yang didukung |

## FAQ

### Q1: Apakah Aspose.CAD untuk Java kompatibel dengan semua format file CAD?
A1: Aspose.CAD untuk Java mendukung berbagai format CAD, termasuk DWG, DXF, dan DWF.

### Q2: Bisakah saya menyesuaikan opsi skala lebih lanjut?
A2: Ya, kelas `CadRasterizationOptions` menyediakan berbagai properti untuk penyesuaian skala dan pengaturan lainnya secara detail.

### Q3: Di mana saya dapat menemukan dokumentasi tambahan untuk Aspose.CAD untuk Java?
A3: Lihat [dokumentasi](https://reference.aspose.com/cad/java/) untuk informasi mendalam dan contoh.

### Q4: Apakah tersedia percobaan gratis untuk Aspose.CAD untuk Java?
A4: Ya, Anda dapat mencoba [percobaan gratis](https://releases.aspose.com/) untuk merasakan kemampuan Aspose.CAD untuk Java.

### Q5: Bagaimana saya dapat mencari bantuan atau berdiskusi tentang Aspose.CAD untuk Java?
A5: Kunjungi [forum Aspose.CAD](https://forum.aspose.com/c/cad/19) untuk terhubung dengan komunitas dan mencari dukungan.

**Pertanyaan Umum Tambahan**

**Q: Bagaimana cara mengonversi file DWG ke PDF alih-alih DXF?**  
A: Kode yang sama berfungsi; cukup ubah ekstensi file di `srcFile` menjadi `.dwg`.

**Q: Bisakah saya mengatur DPI khusus untuk PDF beresolusi tinggi?**  
A: Ya, gunakan `rasterizationOptions.setResolution(300);` (atau DPI apa pun yang Anda butuhkan).

**Q: Apakah memungkinkan untuk menyematkan font dalam PDF yang dihasilkan?**  
A: Aspose.CAD meraster gambar, sehingga font dirender sebagai vektor; tidak diperlukan penyematan font terpisah.

## Kesimpulan

Dengan mengikuti panduan ini, Anda kini tahu cara **membuat PDF dari CAD** menggunakan Aspose.CAD untuk Java dengan Auto Layout Scaling. Proses ini menyederhanakan alur kerja **export CAD to PDF**, memastikan skala yang konsisten, dan menghemat waktu pengembangan yang berharga. Jangan ragu untuk bereksperimen dengan berbagai ukuran halaman, resolusi, dan format CAD untuk memenuhi kebutuhan proyek Anda.

---

**Terakhir Diperbarui:** 2025-12-10  
**Diuji Dengan:** Aspose.CAD for Java 24.12 (terbaru)  
**Penulis:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}