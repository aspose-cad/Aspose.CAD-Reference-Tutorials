---
date: 2026-01-07
description: Pelajari cara mengekspor CAD ke PDF dan mengonversi DGN ke PDF menggunakan
  Aspose.CAD untuk Java. Panduan langkah demi langkah untuk pengembang Java.
linktitle: Export Embedded DGN
second_title: Aspose.CAD Java API
title: Ekspor CAD ke PDF – Ekspor DGN Tertanam dengan Aspose.CAD untuk Java
url: /id/java/dgn-export-options/export-embedded-dgn/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ekspor CAD ke PDF – Ekspor DGN Tersemat dengan Aspose.CAD untuk Java

## Pendahuluan

Dalam tutorial ini Anda akan menemukan **cara mengekspor CAD ke PDF** dengan mengonversi file DGN tersemat menjadi dokumen PDF berkualitas tinggi menggunakan Aspose.CAD untuk Java. Aspose.CAD adalah pustaka yang kuat yang memberi pengembang Java kontrol penuh atas manipulasi file CAD, baik Anda perlu **mengonversi DGN ke PDF**, **mengonversi DWG ke PDF**, atau sekadar merender gambar CAD ke format lain. Ikuti panduan langkah demi langkah di bawah ini, dan Anda akan dapat mengintegrasikan kemampuan ini ke dalam aplikasi Anda dalam hitungan menit.

## Jawaban Cepat
- **Apa arti “ekspor CAD ke PDF”?** Itu mengonversi gambar CAD (DWG, DGN, dll.) menjadi file PDF sambil mempertahankan kualitas vektor.  
- **Pustaka apa yang digunakan?** Aspose.CAD untuk Java.  
- **Apakah saya memerlukan lisensi?** Lisensi diperlukan untuk produksi; versi percobaan gratis tersedia.  
- **Apa saja prasyarat utama?** Lingkungan pengembangan Java dan JAR Aspose.CAD untuk Java.  
- **Bisakah saya menyesuaikan output?** Ya – Anda dapat memilih layout, mengatur opsi rasterisasi, dan mengontrol pengaturan PDF.

## Apa itu “ekspor CAD ke PDF”?
Mengekspor CAD ke PDF berarti mengambil file CAD asli (seperti DWG atau DGN) dan menghasilkan dokumen PDF yang secara akurat merepresentasikan geometri aslinya. PDF dapat dilihat di platform mana pun tanpa memerlukan perangkat lunak CAD, menjadikannya ideal untuk berbagi, mencetak, atau mengarsipkan.

## Mengapa menggunakan Aspose.CAD untuk Java untuk mengonversi DGN ke PDF?
- **Tanpa ketergantungan eksternal** – bekerja murni di Java.  
- **Mempertahankan data vektor** – PDF tetap tajam pada semua tingkat zoom.  
- **Kontrol detail** – pilih layout tertentu, atur DPI rasterisasi, dan sematkan font.  
- **Siap untuk perusahaan** – mendukung file besar, pemrosesan batch, dan opsi lisensi.

## Prasyarat

Sebelum kita mulai, pastikan Anda memiliki hal‑hal berikut:

- **Lingkungan Pengembangan Java** – JDK 8 atau lebih tinggi terpasang dan terkonfigurasi.  
- **Aspose.CAD untuk Java** – unduh JAR terbaru dari [sini](https://releases.aspose.com/cad/java/).  

## Impor Paket

Untuk memulai, Anda perlu mengimpor kelas‑kelas yang diperlukan dalam proyek Java Anda. Tambahkan pernyataan impor berikut ke file sumber Anda:

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Cara mengekspor DGN ke PDF menggunakan Aspose.CAD untuk Java?

Berikut adalah panduan berurutan yang jelas yang menunjukkan cara mengonversi file DGN tersemat (disimpan di dalam DWG) menjadi PDF.

### Langkah 1: Atur Jalur Input dan Output

Tentukan direktori yang berisi file sumber Anda dan sebutkan DWG yang menyimpan DGN tersemat.

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "BlockRefDgn.dwg";
```

### Langkah 2: Muat File DWG

Muat file DWG ke dalam objek `Image`. Aspose.CAD secara otomatis mendeteksi data DGN tersemat.

```java
Image objImage = Image.load(fileName);
```

### Langkah 3: Konfigurasikan Opsi Rasterisasi

Pilih layout mana yang ingin Anda sertakan dalam PDF. Pada contoh ini kami mengekspor hanya layout **Model**.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setLayouts(new String[] {"Model"});
```

### Langkah 4: Konfigurasikan Opsi PDF

Lampirkan pengaturan rasterisasi ke opsi ekspor PDF.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### Langkah 5: Simpan File PDF

Akhirnya, tulis PDF ke disk menggunakan opsi yang telah dikonfigurasi.

```java
objImage.save(dataDir + "BlockRefDgn.pdf", pdfOptions);
```

## Mengonversi DWG ke PDF – tip tambahan

Jika file sumber Anda adalah DWG biasa (tanpa DGN tersemat), Anda dapat menggunakan kembali kode yang sama – cukup ubah `fileName` untuk menunjuk ke DWG yang ingin Anda konversi. Opsi rasterisasi dan PDF tetap sama, memberikan alur kerja **mengonversi DWG ke PDF** yang konsisten.

## Masalah Umum dan Solusinya

| Masalah | Penyebab | Solusi |
|-------|--------|----------|
| **PDF kosong** | Nama layout tidak cocok | Pastikan nama layout yang diberikan ke `setLayouts` persis sama dengan layout di file sumber (case‑sensitive). |
| **Pengecualian lisensi** | Menggunakan versi percobaan tanpa lisensi | Terapkan lisensi Aspose.CAD yang valid sebelum memuat gambar (`License license = new License(); license.setLicense("Aspose.CAD.lic");`). |
| **File tidak ditemukan** | Jalur `dataDir` salah | Gunakan jalur absolut atau pastikan jalur relatif benar relatif terhadap direktori kerja proyek. |
| **Grafik beresolusi rendah** | DPI rasterisasi default rendah | Atur `rasterizationOptions.setPageWidth/Height` atau `setResolution` untuk meningkatkan DPI. |

## Pertanyaan yang Sering Diajukan

**T: Bisakah saya menggunakan Aspose.CAD untuk Java dalam proyek komersial?**  
J: Ya, Aspose.CAD untuk Java adalah pustaka komersial. Anda dapat memperoleh lisensi dari [sini](https://purchase.aspose.com/buy).

**T: Apakah tersedia versi percobaan gratis?**  
J: Ya, Anda dapat mengakses versi percobaan gratis Aspose.CAD untuk Java [sini](https://releases.aspose.com/).

**T: Bagaimana cara mendapatkan dukungan untuk Aspose.CAD untuk Java?**  
J: Anda dapat mencari dukungan di komunitas Aspose.CAD pada [forum](https://forum.aspose.com/c/cad/19).

**T: Bagaimana jika saya membutuhkan lisensi sementara?**  
J: Anda dapat memperoleh lisensi sementara [sini](https://purchase.aspose.com/temporary-license/).

**T: Di mana saya dapat menemukan dokumentasinya?**  
J: Dokumentasi tersedia [sini](https://reference.aspose.com/cad/java/).

## Kesimpulan

Anda kini telah mempelajari cara **mengekspor CAD ke PDF**, khususnya cara **mengonversi DGN ke PDF** dan bahkan **mengonversi DWG ke PDF** menggunakan Aspose.CAD untuk Java. Dengan mengikuti langkah‑langkah di atas, Anda dapat mengintegrasikan konversi CAD‑ke‑PDF yang mulus ke dalam solusi berbasis Java apa pun, menyediakan PDF berkualitas tinggi kepada pengguna tanpa memerlukan perangkat lunak CAD tambahan.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Terakhir Diperbarui:** 2026-01-07  
**Diuji Dengan:** Aspose.CAD untuk Java 24.12  
**Penulis:** Aspose