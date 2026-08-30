---
date: 2026-06-24
description: Pelajari cara membuat pdf dari dxf dan mengekspor dxf ke pdf menggunakan
  Aspose.CAD untuk Java, mengatur ukuran halaman pdf, dan menghasilkan pdf dari cad
  dengan kontrol yang tepat.
keywords:
- create pdf from dxf
- export dxf to pdf
- set pdf page size
- convert dwg to pdf
- export cad drawing pdf
linktitle: Ekspor Layout DXF Spesifik ke PDF dengan Java
schemas:
- author: Aspose
  dateModified: '2026-06-24'
  description: Learn how to create pdf from dxf and export dxf to pdf using Aspose.CAD
    for Java, set pdf page size, and generate pdf from cad with precise control.
  headline: Create pdf from dxf Layout to PDF with Aspose.CAD for Java
  type: TechArticle
- description: Learn how to create pdf from dxf and export dxf to pdf using Aspose.CAD
    for Java, set pdf page size, and generate pdf from cad with precise control.
  name: Create pdf from dxf Layout to PDF with Aspose.CAD for Java
  steps:
  - name: Set the Resource Directory
    text: Define the folder that contains your DXF files. Replace the placeholder
      with the actual path on your machine. > **Pro tip:** Use `System.getProperty("user.dir")`
      to build a relative path that works across environments.
  - name: Load the DXF File
    text: Load the source DXF using `Image.load()`. `Image.load()` reads a CAD file
      and returns an `Image` object representing its contents. The `Image.load()`
      method parses the DXF structure and creates an in‑memory representation that
      can be rasterized or saved directly.
  - name: Configure Rasterization Options (Set PDF Page Width in Java)
    text: Here we create `CadRasterizationOptions` and define the output page size.
      `CadRasterizationOptions` specifies how CAD data is rasterized, including page
      size, DPI, and layout selection. `CadRasterizationOptions` controls how the
      CAD data is rendered—page size, DPI, background color, and which layout
  - name: Create PDF Options (Java Convert CAD PDF)
    text: Link the rasterization settings to a `PdfOptions` instance. `PdfOptions`
      tells Aspose.CAD to generate a PDF file using the provided rasterization settings.
      `PdfOptions` is the container that tells the library to produce a PDF file,
      applying the rasterization settings defined earlier.
  - name: Export DXF to PDF (Create PDF from DXF)
    text: Finally, save the image as a PDF. `Image.save()` writes the rendered content
      to a file in the format specified by the options. The `save` call writes the
      rendered content to disk using the PDF options, producing a vector‑preserving
      PDF. After execution, you’ll find `conic_pyramid_layout_out_.pdf` in
  type: HowTo
- questions:
  - answer: Absolutely. The API is straightforward for newcomers while offering deep
      customization for power users.
    question: Is Aspose.CAD for Java suitable for both beginners and experienced developers?
  - answer: Yes. Adjust `CadRasterizationOptions` (page size, DPI, background color)
      per layout as needed.
    question: Can I customize the rasterization options for different layouts?
  - answer: Detailed docs are available [here](https://reference.aspose.com/cad/java/).
    question: Where can I find comprehensive documentation for Aspose.CAD for Java?
  - answer: Yes, you can download a trial version [here](https://releases.aspose.com/).
    question: Is there a free trial available for Aspose.CAD for Java?
  - answer: Visit the support forum [here](https://forum.aspose.com/c/cad/19) for
      community and staff assistance.
    question: How can I get support for Aspose.CAD for Java?
  type: FAQPage
second_title: Aspose.CAD Java API
title: Buat pdf dari Layout dxf ke PDF dengan Aspose.CAD untuk Java
url: /id/java/additional-features/export-specific-layout-to-pdf/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Buat pdf dari Layout dxf ke PDF dengan Aspose.CAD untuk Java

## Pendahuluan

Jika Anda seorang pengembang Java yang bekerja dengan gambar CAD, Anda tahu bahwa **cara mengekspor dxf** secara akurat dapat menentukan keberhasilan atau kegagalan sebuah proyek. Apakah Anda membuat laporan teknik, berbagi desain dengan klien, atau mengotomatisasi konversi batch, pustaka konversi PDF Java yang handal sangat penting. Dalam tutorial ini kami akan memandu Anda melalui **pembuatan pdf dari dxf** file tata letak, mengontrol dimensi halaman, dan menjaga kualitas vektor tetap utuh dengan **Aspose.CAD untuk Java**.

## Jawaban Cepat
- **Apa pustaka utama?** Aspose.CAD for Java, a dedicated Java PDF conversion library for CAD.
- **Apakah saya dapat memilih tata letak tertentu?** Yes – use `CadRasterizationOptions.setLayouts()` to target a layout name.
- **Bagaimana cara mengatur ukuran halaman?** Adjust `setPageWidth()` and `setPageHeight()` in rasterization options (e.g., 1600 × 1600).
- **Apakah saya memerlukan lisensi untuk produksi?** A commercial license is required for production use; a free trial is available.
- **Versi Java apa yang didukung?** Java 8 and higher (JDK 1.8+).

## Apa itu membuat pdf dari dxf?
Membuat PDF dari DXF berarti mengonversi gambar CAD yang disimpan dalam format DXF menjadi dokumen PDF sambil mempertahankan data vektor, lapisan, dan informasi tata letak. **Aspose.CAD untuk Java** melakukan konversi ini dalam satu panggilan, menghilangkan kebutuhan akan langkah raster menengah.

## Mengapa menggunakan Aspose.CAD untuk Java?
Aspose.CAD untuk Java menyediakan dukungan CAD yang komprehensif, menangani lebih dari 30 format tanpa ketergantungan eksternal, dan menawarkan rasterisasi yang tepat dengan DPI yang dapat disesuaikan, ukuran halaman, dan pilihan tata letak. Mesin berperforma tinggi-nya memungkinkan konversi batch cepat sambil mempertahankan kesetiaan vektor, menjadikannya ideal untuk penyebaran di sisi server dan cloud.

- **Dukungan CAD lengkap** – Menangani **lebih dari 30** format CAD, termasuk DWG, DXF, DWF, DGN, dan DWT.  
- **Tanpa ketergantungan eksternal** – Murni Java, tidak memerlukan DLL native, yang menyederhanakan penyebaran di Linux, Windows, atau lingkungan kontainer.  
- **Rasterisasi tepat** – Pilih output vektor atau raster, atur DPI, ukuran halaman, dan tata letak. Misalnya, pustaka dapat merender DXF 500‑halaman dalam kurang dari 5 detik pada server standar 2‑core.  
- **Kinerja tinggi** – Dioptimalkan untuk pemrosesan batch; dapat mengonversi 1.000 file dalam satu thread dengan penggunaan heap kurang dari 200 MB.  
- **Ekspor dxf ke pdf** dengan satu baris kode, menjadikannya ideal untuk **java convert cad pdf** workflows.

## Prasyarat

Sebelum Anda memulai, pastikan Anda memiliki:

1. **Java Development Kit (JDK)** – Java 8 atau lebih baru. Download it from [Oracle](https://www.oracle.com/java/technologies/javase-downloads.html).  
2. **Aspose.CAD for Java** – Grab the latest JAR from the [Aspose.CAD download page](https://releases.aspose.com/cad/java/).  
3. IDE atau alat build (Maven/Gradle) untuk menambahkan JAR Aspose.CAD ke classpath proyek Anda.

## Impor Namespace

Pertama, impor kelas yang Anda perlukan. Impor ini memberi Anda akses ke pemuatan gambar, opsi rasterisasi, dan pengaturan output PDF.

Kelas `Image` adalah objek inti Aspose.CAD yang **mewakili file CAD yang dimuat dalam memori**. Ia menyediakan metode untuk merender dan menyimpan konten dalam berbagai format.

```java
import com.aspose.cad.Image;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Panduan Langkah‑per‑Langkah

### Langkah 1: Atur Direktori Sumber Daya

Tentukan folder yang berisi file DXF Anda. Ganti placeholder dengan jalur sebenarnya di mesin Anda.

```java
String dataDir = "Your Document Directory" + "DXFDrawings/";
```

> **Tip Pro:** Gunakan `System.getProperty("user.dir")` untuk membangun jalur relatif yang berfungsi di berbagai lingkungan.

### Langkah 2: Muat File DXF

Muat DXF sumber menggunakan `Image.load()`.  
`Image.load()` membaca file CAD dan mengembalikan objek `Image` yang mewakili isinya.

Metode `Image.load()` mem-parsing struktur DXF dan membuat representasi dalam memori yang dapat dirasterisasi atau disimpan langsung.

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile); 
```

### Langkah 3: Konfigurasikan Opsi Rasterisasi (Atur Lebar Halaman PDF di Java)

Di sini kami membuat `CadRasterizationOptions` dan menentukan ukuran halaman output.  
`CadRasterizationOptions` menentukan cara data CAD dirasterisasi, termasuk ukuran halaman, DPI, dan pilihan tata letak.

`CadRasterizationOptions` mengontrol **bagaimana data CAD dirender—ukuran halaman, DPI, warna latar belakang, dan tata letak mana yang akan dirasterisasi**.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);   
rasterizationOptions.setLayouts(new String[] {"Model"});
```

- `setPageWidth` / `setPageHeight` – mengontrol **lebar halaman pdf** (dan tinggi) untuk PDF.  
- `setLayouts` – menentukan tata letak mana yang akan dirender; `"Model"` adalah ruang model default di banyak file DXF.

### Langkah 4: Buat Opsi PDF (Java Convert CAD PDF)

Hubungkan pengaturan rasterisasi ke instance `PdfOptions`.  
`PdfOptions` memberi tahu Aspose.CAD untuk menghasilkan file PDF menggunakan pengaturan rasterisasi yang diberikan.

`PdfOptions` adalah wadah yang memberi tahu pustaka untuk menghasilkan file PDF, menerapkan pengaturan rasterisasi yang didefinisikan sebelumnya.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### Langkah 5: Ekspor DXF ke PDF (Buat PDF dari DXF)

Akhirnya, simpan gambar sebagai PDF.  
`Image.save()` menulis konten yang dirender ke file dalam format yang ditentukan oleh opsi.

Pemanggilan `save` menulis konten yang dirender ke disk menggunakan opsi PDF, menghasilkan PDF yang mempertahankan vektor.

```java
image.save(dataDir + "conic_pyramid_layout_out_.pdf", pdfOptions);
```

Setelah eksekusi, Anda akan menemukan `conic_pyramid_layout_out_.pdf` di direktori yang sama, berisi **hanya tata letak Model** yang dirender pada dimensi yang Anda atur.

## Kasus Penggunaan Umum

| Skenario | Mengapa metode ini membantu |
|----------|-----------------------------|
| **Pembuatan laporan otomatis** | Menjamin setiap gambar diekspor dengan ukuran halaman yang sama, membuat PDF batch seragam. |
| **Pratinjau desain untuk klien** | Mengekspor satu tata letak (mis., “Model” atau “Sheet1”) mengurangi ukuran file sambil mempertahankan kesetiaan vektor. |
| **Migrasi DWG lama ke PDF** | Meskipun contoh ini menggunakan DXF, API yang sama bekerja untuk **convert dwg to pdf** dengan perubahan kode minimal. |
| **Menyematkan gambar CAD di portal web** | PDF yang dihasilkan dapat langsung di-stream ke browser tanpa alat konversi tambahan. |

## Masalah Umum dan Solusinya

| Masalah | Alasan | Solusi |
|---------|--------|--------|
| **PDF kosong** | Nama tata letak tidak cocok | Verifikasi nama tata letak yang tepat di DXF (gunakan penampil CAD). |
| **Ukuran halaman tidak tepat** | `setPageWidth/Height` tidak diterapkan | Pastikan Anda mengatur opsi rasterisasi **sebelum** membuat `PdfOptions`. |
| **Kehabisan memori untuk file besar** | Memuat DXF besar ke memori | Gunakan streaming atau tingkatkan heap JVM (`-Xmx2g`). |
| **Font hilang** | Elemen teks menggunakan font yang tidak tersedia | Instal font yang diperlukan di server atau sematkan melalui `CadRasterizationOptions`. |
| **Perlu mengekspor beberapa tata letak** | Hanya satu panggilan tata letak | Panggil `setLayouts` dengan array nama tata letak dan ulangi langkah `save` untuk masing‑masing. |

## Pertanyaan yang Sering Diajukan

**T: Apakah Aspose.CAD untuk Java cocok untuk pemula maupun pengembang berpengalaman?**  
**J: Tentu saja. API ini mudah dipahami bagi pemula sekaligus menawarkan kustomisasi mendalam bagi pengguna berpengalaman.**

**T: Bisakah saya menyesuaikan opsi rasterisasi untuk tata letak yang berbeda?**  
**J: Ya. Sesuaikan `CadRasterizationOptions` (ukuran halaman, DPI, warna latar belakang) per tata letak sesuai kebutuhan.**

**T: Di mana saya dapat menemukan dokumentasi lengkap untuk Aspose.CAD untuk Java?**  
**J: Dokumentasi detail tersedia [di sini](https://reference.aspose.com/cad/java/).**

**T: Apakah ada versi percobaan gratis untuk Aspose.CAD untuk Java?**  
**J: Ya, Anda dapat mengunduh versi percobaan [di sini](https://releases.aspose.com/).**

**T: Bagaimana saya dapat mendapatkan dukungan untuk Aspose.CAD untuk Java?**  
**J: Kunjungi forum dukungan [di sini](https://forum.aspose.com/c/cad/19) untuk bantuan komunitas dan staf.**

## Kesimpulan

Dalam panduan ini kami menunjukkan **cara membuat pdf dari dxf** tata letak ke PDF menggunakan Aspose.CAD untuk Java, mencakup semua hal mulai dari penyiapan lingkungan hingga penyetelan ukuran halaman secara detail. Dengan memanfaatkan **pustaka konversi pdf java** ini, Anda dapat mengotomatisasi alur kerja CAD‑ke‑PDF, mempertahankan kesetiaan vektor, dan mengintegrasikan pembuatan PDF yang mulus ke dalam aplikasi Java Anda. Apakah Anda perlu **mengekspor dxf ke pdf**, **mengonversi dwg ke pdf**, atau **menghasilkan pdf dari cad** untuk pemrosesan lanjutan, langkah‑langkah di atas memberi Anda dasar yang kuat.

---

**Last Updated:** 2026-06-24  
**Tested With:** Aspose.CAD for Java 24.12 (latest at time of writing)  
**Author:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Tutorial Terkait

- [Buat PDF dari CAD – Ekspor DXF ke PDF dengan Aspose.CAD untuk Java](/cad/java/additional-features/export-dxf-to-pdf/)
- [Buat PDF dari DXF: Ekspor Lapisan dengan Aspose.CAD untuk Java](/cad/java/additional-features/export-specific-layer-to-pdf/)
- [Konversi CAD ke PDF – Atur Ukuran Kanvas & Mode (Java)](/cad/java/advanced-cad-features/set-canvas-size-and-mode/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}