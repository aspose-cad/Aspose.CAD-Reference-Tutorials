---
date: 2026-05-25
description: Pelajari cara mengatur Metered Licensing di Aspose.CAD untuk Java guna
  mengoptimalkan pemrosesan CAD, mengurangi biaya, dan melacak penggunaan secara efisien.
keywords:
- how to set metered
- Aspose.CAD licensing
- Java metered licensing
linktitle: Cara Mengatur Metered Licensing di Aspose.CAD
schemas:
- author: Aspose
  dateModified: '2026-05-25'
  description: Learn how to set metered licensing in Aspose.CAD for Java to optimize
    CAD processing, reduce costs, and track usage efficiently.
  headline: How to Set Metered Licensing in Aspose.CAD
  type: TechArticle
- questions:
  - answer: A usage‑based model that tracks API calls and charges per consumption
      unit.
    question: What is metered licensing?
  - answer: Two keys – a public and a private key – generated from your Aspose account.
    question: How many keys are required?
  - answer: Yes, call `License.getConsumptionQuantity()` before and after processing.
    question: Can I check usage programmatically?
  - answer: A free trial license can be obtained from the Aspose website.
    question: Is a trial available?
  - answer: Java 8 through 17 are fully supported.
    question: Which Java version is supported?
  type: FAQPage
second_title: Aspose.CAD Java API
title: Cara Mengatur Metered Licensing di Aspose.CAD
url: /id/java/licensing-and-configuration/metered-licensing-in-aspose-cad/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Lisensi Metered di Aspose.CAD

## Pendahuluan

Buka potensi penuh Aspose.CAD untuk Java dengan lisensi **cara mengatur metered**! Panduan langkah demi langkah ini membawa Anda melalui setiap tahap—dari menginstal prasyarat, mengimpor paket yang tepat, hingga mengukur konsumsi sebelum dan sesudah pemrosesan. Pada akhir Anda akan tahu persis **cara mengatur metered** kunci, membaca metrik penggunaan, dan menjaga alur kerja CAD Anda tetap hemat biaya.

## Jawaban Cepat
- **Apa itu lisensi metered?** Model berbasis penggunaan yang melacak panggilan API dan mengenakan biaya per unit konsumsi.  
- **Berapa banyak kunci yang diperlukan?** Dua kunci – kunci publik dan kunci pribadi – yang dihasilkan dari akun Aspose Anda.  
- **Bisakah saya memeriksa penggunaan secara programatis?** Ya, panggil `License.getConsumptionQuantity()` sebelum dan sesudah pemrosesan.  
- **Apakah tersedia versi percobaan?** Lisensi percobaan gratis dapat diperoleh dari situs web Aspose.  
- **Versi Java mana yang didukung?** Java 8 sampai 17 didukung sepenuhnya.

## Apa itu lisensi metered di Aspose.CAD?
Lisensi metered adalah model bayar‑sesuai‑pakai Aspose.CAD yang mencatat setiap panggilan API sebagai unit konsumsi. Ini memungkinkan Anda memantau penggunaan secara tepat, menghindari over‑provisioning, dan hanya membayar apa yang benar‑benar Anda konsumsi.

## Mengapa menggunakan lisensi metered untuk pemrosesan CAD?
Aspose.CAD mendukung **lebih dari 50** format input dan output—termasuk DWG, DXF, DGN, dan SVG—dan dapat memproses file hingga **2 GB** tanpa memuat seluruh dokumen ke memori. Efisiensi ini menghasilkan biaya server yang lebih rendah, terutama saat menangani batch gambar yang besar.

## Prasyarat

Sebelum menyelami dunia lisensi metered dengan Aspose.CAD, pastikan Anda memiliki hal‑hal berikut:

### Instalasi Java Development Kit (JDK)

Pastikan Anda memiliki versi terbaru Java Development Kit terpasang di sistem Anda. Anda dapat mengunduhnya dari [sini](https://www.oracle.com/java/technologies/javase-downloads.html).

### Perpustakaan Aspose.CAD untuk Java

Pastikan untuk mengunduh dan menyiapkan perpustakaan Aspose.CAD untuk Java. Anda dapat menemukan perpustakaan tersebut [di sini](https://releases.aspose.com/cad/java/). Anda juga dapat menelusuri rilis Aspose lainnya [di sini](https://releases.aspose.com/).

## Cara mengatur lisensi metered di Aspose.CAD untuk Java?

Muat kunci publik dan pribadi Anda, panggil `License.setMeteredKey(publicKey, privateKey)`, dan perpustakaan langsung beralih ke mode metered. Panggilan tunggal ini mengaktifkan pelacakan penggunaan untuk setiap operasi API berikutnya, memungkinkan Anda menanyakan konsumsi sebelum dan sesudah langkah pemrosesan apa pun.

## Impor Paket

Untuk menggunakan perpustakaan, impor paket intinya:

`import com.aspose.cad.*;` membawa kelas Aspose.CAD ke dalam proyek Anda.

```java
import com.aspose.cad;
```

## Langkah 1: Atur Kunci Metered

`setMeteredKey` mendaftarkan kunci publik dan pribadi Anda ke perpustakaan Aspose.CAD.

Pertama, atur kunci metered menggunakan metode `setMeteredKey`. Ganti `<valid public key>` dan `<valid private key>` dengan kunci publik dan pribadi Anda yang sebenarnya.

```java
Metered.setMeteredKey("<valid public key>", "<valid private key>");
```

## Langkah 2: Dapatkan Kuantitas Konsumsi Sebelum Pemrosesan

`getConsumptionQuantity` mengembalikan total jumlah unit konsumsi yang tercatat sejauh ini.

Ambil nilai kuantitas yang dikonsumsi sebelum mengakses API Aspose.CAD untuk mendapatkan pemahaman awal.

```java
BigDecimal quantityOld = Metered.getConsumptionQuantity();
System.out.println("Consumption quantity before processing: " + quantityOld);
```

## Langkah 3: Pemrosesan

Lakukan pemrosesan CAD yang Anda inginkan menggunakan fungsionalitas Aspose.CAD. Hapus komentar pada potongan kode yang terkait dengan tugas spesifik Anda, seperti memuat gambar CAD.

```java
// Example:
// com.aspose.cad.fileformats.cad.CadImage image =
// (com.aspose.cad.fileformats.cad.CadImage)com.aspose.cad.Image.load("BlockRefDgn.dwg");
```

## Langkah 4: Dapatkan Kuantitas Konsumsi Setelah Pemrosesan

Setelah pemrosesan, dapatkan kembali nilai kuantitas yang dikonsumsi untuk menilai dampaknya.

```java
BigDecimal quantity = Metered.getConsumptionQuantity();
System.out.println("Consumption quantity after processing: " + quantity);
```

Ulangi langkah‑langkah ini untuk pemrosesan atau tugas tambahan sesuai kebutuhan.

## Masalah Umum dan Solusinya

- **Kesalahan kunci tidak valid:** Periksa kembali bahwa kedua kunci disalin persis seperti yang ditampilkan di akun Aspose Anda; spasi tambahan menyebabkan kegagalan otentikasi.  
- **Laporan konsumsi nol:** Pastikan Anda memanggil `License.getConsumptionQuantity()` *setelah* penggunaan API pertama; panggilan pertama menginisialisasi penghitung.  
- **Penurunan kinerja pada file besar:** Gunakan `CadImage.load(..., LoadOptions)` dengan `LoadOptions.setLoadMode(LoadMode.Stream)` untuk menghindari memuat seluruh file ke memori.

## Pertanyaan yang Sering Diajukan

**Q1: Bisakah saya menggunakan lisensi metered untuk tujuan evaluasi?**  
A1: Ya, Anda dapat memperoleh lisensi percobaan gratis [di sini](https://releases.aspose.com/).

**Q2: Di mana saya dapat menemukan dokumentasi detail untuk Aspose.CAD untuk Java?**  
A2: Lihat dokumentasi [di sini](https://reference.aspose.com/cad/java/).

**Q3: Bagaimana cara membeli lisensi untuk Aspose.CAD untuk Java?**  
A3: Kunjungi halaman pembelian [di sini](https://purchase.aspose.com/buy).

**Q4: Apakah ada opsi lisensi sementara yang tersedia?**  
A5: Ya, Anda dapat menjelajahi lisensi sementara [di sini](https://purchase.aspose.com/temporary-license/).

**Q5: Membutuhkan dukungan komunitas atau memiliki pertanyaan khusus?**  
A5: Kunjungi forum Aspose.CAD [di sini](https://forum.aspose.com/c/cad/19).

**Q6: Apakah lisensi metered bekerja dengan penyebaran cloud?**  
A6: Tentu saja. Panggilan `setMeteredKey` yang sama berfungsi di Docker, Kubernetes, atau lingkungan serverless.

**Q7: Bisakah saya mereset penghitung konsumsi?**  
A7: Penghitung secara otomatis direset pada awal setiap periode penagihan baru; Anda tidak dapat meresetnya secara manual.

## Kesimpulan

Selamat! Anda telah berhasil menguasai **cara mengatur metered** lisensi dengan Aspose.CAD untuk Java. Dengan mengikuti panduan ini, Anda telah menyiapkan dan mengintegrasikan lisensi metered secara mulus ke dalam proyek Java Anda, memastikan penggunaan kemampuan Aspose.CAD yang efisien sambil menjaga biaya tetap transparan.

---

**Terakhir Diperbarui:** 2026-05-25  
**Diuji Dengan:** Aspose.CAD untuk Java 24.10  
**Penulis:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Tutorial Terkait

- [Konversi CAD ke PDF dengan Aspose.CAD untuk Java – Tutorial Lengkap](/cad/java/)
- [Buat PDF dari CAD – Ekspor DXF ke PDF dengan Aspose.CAD untuk Java](/cad/java/additional-features/export-dxf-to-pdf/)
- [Atur Ukuran Kanvas – Fitur CAD Lanjutan dengan Aspose.CAD untuk Java](/cad/java/advanced-cad-features/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}