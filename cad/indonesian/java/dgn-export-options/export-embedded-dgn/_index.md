---
date: 2026-06-14
description: Pelajari cara mengekspor CAD ke PDF dan mengonversi DGN ke PDF menggunakan
  Aspose.CAD untuk Java. Panduan langkah demi langkah untuk pengembang Java.
keywords:
- export cad to pdf
- convert dwg to pdf
- convert dgn to pdf
- java convert cad pdf
- batch convert dgn pdf
linktitle: Ekspor DGN Tertanam
schemas:
- author: Aspose
  dateModified: '2026-06-14'
  description: Learn how to export CAD to PDF and convert DGN to PDF using Aspose.CAD
    for Java. Step‑by‑step guide for Java developers.
  headline: Export CAD to PDF – Export Embedded DGN with Aspose.CAD for Java
  type: TechArticle
- description: Learn how to export CAD to PDF and convert DGN to PDF using Aspose.CAD
    for Java. Step‑by‑step guide for Java developers.
  name: Export CAD to PDF – Export Embedded DGN with Aspose.CAD for Java
  steps:
  - name: Set Up Input and Output Paths
    text: Define the directory that contains your source file and specify the DWG
      that holds the embedded DGN.
  - name: Load DWG File
    text: '`Image` loads the DWG and automatically detects any embedded DGN data,
      exposing it for further processing.'
  - name: Configure Rasterization Options
    text: Select which layout(s) you want to include in the PDF. In this example we
      export only the **Model** layout, which is the most common view for engineering
      drawings.
  - name: Configure PDF Options
    text: Attach the rasterization settings to the PDF export options so that the
      final document respects the chosen layout and DPI.
  - name: Save PDF File
    text: Finally, write the PDF to disk using the configured options. The `save`
      method writes the configured image to the target file format on disk.
  type: HowTo
- questions:
  - answer: Yes, Aspose.CAD for Java is a commercial library. You can obtain a license
      from [here](https://purchase.aspose.com/buy).
    question: Can I use Aspose.CAD for Java in a commercial project?
  - answer: Yes, you can access a free trial of Aspose.CAD for Java [here](https://releases.aspose.com/).
    question: Is there a free trial available?
  - answer: You can seek support from the Aspose.CAD community on the [forum](https://forum.aspose.com/c/cad/19).
    question: How can I get support for Aspose.CAD for Java?
  - answer: You can obtain a temporary license [here](https://purchase.aspose.com/temporary-license/).
    question: What if I need a temporary license?
  - answer: The documentation is available [here](https://reference.aspose.com/cad/java/).
    question: Where can I find the official documentation?
  type: FAQPage
second_title: Aspose.CAD Java API
title: Ekspor CAD ke PDF – Ekspor DGN Tertanam dengan Aspose.CAD untuk Java
url: /id/java/dgn-export-options/export-embedded-dgn/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Export CAD ke PDF – Ekspor DGN Tersemat dengan Aspose.CAD untuk Java

## Pendahuluan

Dalam tutorial ini Anda akan menemukan **cara mengekspor CAD ke PDF** dengan mengonversi file DGN tersemat menjadi dokumen PDF berkualitas tinggi menggunakan Aspose.CAD untuk Java. Aspose.CAD adalah pustaka yang kuat yang memberi pengembang Java kontrol penuh atas manipulasi file CAD, baik Anda perlu **mengonversi DGN ke PDF**, **mengonversi DWG ke PDF**, atau sekadar merender gambar CAD dalam format lain. Ikuti panduan langkah‑demi‑langkah di bawah ini, dan Anda akan dapat mengintegrasikan kemampuan ini ke dalam aplikasi Anda dalam hitungan menit.

## Jawaban Cepat

- **Apa arti “export CAD to PDF”?** Itu mengonversi gambar CAD (DWG, DGN, dll.) menjadi file PDF sambil mempertahankan kualitas vektor.  
- **Pustaka apa yang digunakan?** Aspose.CAD untuk Java.  
- **Apakah saya memerlukan lisensi?** Lisensi diperlukan untuk produksi; versi percobaan gratis tersedia.  
- **Apa prasyarat utama?** Lingkungan pengembangan Java dan JAR Aspose.CAD untuk Java.  
- **Bisakah saya menyesuaikan output?** Ya – Anda dapat memilih tata letak, mengatur opsi rasterisasi, dan mengontrol pengaturan PDF.

## Apa itu “export CAD ke PDF”?

Export CAD ke PDF mengonversi gambar CAD asli (DWG, DGN, dll.) menjadi file PDF yang mempertahankan geometri vektor, lapisan, dan tata letak asli, memungkinkan siapa pun untuk melihat, mencetak, atau membagikan desain tanpa perangkat lunak CAD. Transformasi ini menghasilkan dokumen yang independen platform dan tampak identik pada tingkat zoom apa pun, menjadikannya ideal untuk kolaborasi dan arsip.

## Mengapa menggunakan Aspose.CAD untuk Java untuk mengonversi DGN ke PDF?

Aspose.CAD untuk Java menyediakan solusi murni Java yang menghilangkan kebutuhan akan alat CAD eksternal, memastikan kesetiaan vektor yang tepat dalam PDF yang dihasilkan, dan menawarkan opsi konfigurasi yang luas seperti pemilihan tata letak, kontrol DPI, dan penyematan font, menjadikannya ideal untuk tugas konversi sederhana maupun skala perusahaan.

- **Tidak ada ketergantungan eksternal** – berfungsi murni di Java pada sistem operasi apa pun.  
- **Mempertahankan data vektor** – PDF tetap tajam pada tingkat zoom apa pun.  
- **Kontrol detail** – pilih tata letak tertentu, atur DPI rasterisasi, dan sematkan font.  
- **Siap untuk perusahaan** – mendukung file hingga **2 GB**, pemrosesan batch ribuan gambar, dan lisensi yang fleksibel.  

## Prasyarat

Sebelum kita mulai, pastikan Anda memiliki hal berikut:

- **Lingkungan Pengembangan Java** – JDK 8 atau lebih tinggi terpasang dan dikonfigurasi.  
- **Aspose.CAD untuk Java** – unduh JAR terbaru dari [di sini](https://releases.aspose.com/cad/java/).  

## Impor Paket

Pernyataan `import` membawa kelas Aspose.CAD yang diperlukan ke dalam ruang lingkup. `Image` adalah kelas inti yang mewakili setiap file CAD yang dapat dirasterkan, sementara `PdfOptions` dan `RasterizationOptions` memungkinkan Anda menyesuaikan output PDF secara detail. `CadRasterizationOptions` menentukan parameter rasterisasi seperti DPI, ukuran halaman, dan tata letak untuk rendering CAD.

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

## Cara mengekspor CAD ke PDF menggunakan Aspose.CAD untuk Java?

Proses dimulai dengan memuat file DWG yang berisi DGN tersemat, kemudian mengatur parameter rasterisasi untuk menentukan resolusi dan tata letak output, melampirkan parameter tersebut ke objek PdfOptions, dan akhirnya memanggil metode `save` untuk menghasilkan PDF. Pendekatan ini memastikan hasil berkualitas tinggi, mempertahankan vektor dengan kode minimal.

Berikut adalah panduan berurutan yang jelas yang menunjukkan secara tepat cara mengonversi file DGN tersemat (disimpan di dalam DWG) menjadi PDF.

### Langkah 1: Siapkan Jalur Input dan Output

Tentukan direktori yang berisi file sumber Anda dan sebutkan DWG yang menyimpan DGN tersemat.

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "BlockRefDgn.dwg";
```

### Langkah 2: Muat File DWG

`Image` memuat DWG dan secara otomatis mendeteksi data DGN tersemat, memperlihatkannya untuk pemrosesan lebih lanjut.

```java
Image objImage = Image.load(fileName);
```

### Langkah 3: Konfigurasikan Opsi Rasterisasi

Pilih tata letak yang ingin Anda sertakan dalam PDF. Pada contoh ini kami mengekspor hanya tata letak **Model**, yang merupakan tampilan paling umum untuk gambar teknik.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setLayouts(new String[] {"Model"});
```

### Langkah 4: Konfigurasikan Opsi PDF

Lampirkan pengaturan rasterisasi ke opsi ekspor PDF sehingga dokumen akhir menghormati tata letak dan DPI yang dipilih.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### Langkah 5: Simpan File PDF

Terakhir, tulis PDF ke disk menggunakan opsi yang telah dikonfigurasi. Metode `save` menulis gambar yang telah dikonfigurasi ke format file target di disk.

```java
objImage.save(dataDir + "BlockRefDgn.pdf", pdfOptions);
```

## Konversi DWG ke PDF – tip tambahan

Jika file sumber Anda adalah DWG biasa (tanpa DGN tersemat), Anda dapat menggunakan kembali kode yang sama – cukup ubah `fileName` untuk menunjuk ke DWG yang ingin Anda konversi. Opsi rasterisasi dan PDF tetap sama, memberikan alur kerja **konversi DWG ke PDF** yang konsisten.

## Masalah Umum dan Solusinya

| Masalah | Penyebab | Solusi |
|-------|--------|----------|
| **Output PDF kosong** | Nama tata letak tidak cocok | Pastikan nama tata letak yang diberikan ke `setLayouts` persis cocok dengan tata letak di file sumber (case‑sensitive). |
| **Pengecualian lisensi** | Menggunakan versi percobaan tanpa lisensi | Terapkan lisensi Aspose.CAD yang valid sebelum memuat gambar (`License license = new License(); license.setLicense("Aspose.CAD.lic");`). |
| **File tidak ditemukan** | Path `dataDir` tidak benar | Gunakan path absolut atau pastikan path relatif benar relatif terhadap direktori kerja proyek. |
| **Grafik beresolusi rendah** | DPI rasterisasi default terlalu rendah | Setel `rasterizationOptions.setResolution(300)` atau sesuaikan `setPageWidth/Height` untuk meningkatkan DPI. |

## Pertanyaan yang Sering Diajukan

**Q: Bisakah saya menggunakan Aspose.CAD untuk Java dalam proyek komersial?**  
A: Ya, Aspose.CAD untuk Java adalah pustaka komersial. Anda dapat memperoleh lisensi dari [di sini](https://purchase.aspose.com/buy).

**Q: Apakah tersedia versi percobaan gratis?**  
A: Ya, Anda dapat mengakses versi percobaan gratis Aspose.CAD untuk Java [di sini](https://releases.aspose.com/).

**Q: Bagaimana saya dapat mendapatkan dukungan untuk Aspose.CAD untuk Java?**  
A: Anda dapat mencari dukungan dari komunitas Aspose.CAD di [forum](https://forum.aspose.com/c/cad/19).

**Q: Bagaimana jika saya membutuhkan lisensi sementara?**  
A: Anda dapat memperoleh lisensi sementara [di sini](https://purchase.aspose.com/temporary-license/).

**Q: Di mana saya dapat menemukan dokumentasi resmi?**  
A: Dokumentasi tersedia [di sini](https://reference.aspose.com/cad/java/).

## Kesimpulan

Anda kini telah mempelajari cara **mengekspor CAD ke PDF**, khususnya cara **mengonversi DGN ke PDF** dan bahkan **mengonversi DWG ke PDF** menggunakan Aspose.CAD untuk Java. Dengan mengikuti langkah‑langkah di atas, Anda dapat mengintegrasikan konversi CAD‑ke‑PDF yang mulus ke dalam solusi berbasis Java apa pun, menyajikan PDF berkualitas tinggi kepada pengguna Anda tanpa memerlukan perangkat lunak CAD tambahan.

---

**Terakhir Diperbarui:** 2026-06-14  
**Diuji Dengan:** Aspose.CAD for Java 24.12  
**Penulis:** Aspose

{{< blocks/products/products-backtop-button >}}

## Tutorial Terkait

- [Ekspor DGN ke DWG dengan Aspose.CAD untuk Java – Tutorial](/cad/java/dgn-export-options/)
- [Ekspor DGN ke PDF AutoCAD Tanpa Kesulitan dengan Aspose.CAD untuk Java](/cad/java/dgn-export-options/exporting-dgn-to-pdf/)
- [dwg ke pdf java – Ekspor CAD ke PDF dengan Aspose.CAD](/cad/java/cad-export-options/export-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}