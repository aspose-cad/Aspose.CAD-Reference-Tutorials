---
date: 2026-05-20
description: Pelajari cara menambahkan gambar ke file DWG menggunakan Aspose.CAD untuk
  Java serta mengonversi DWG ke PDF. Ikuti panduan langkah demi langkah kami untuk
  pengembangan yang efisien.
keywords:
- add image to dwg
- convert dwg to pdf
- import image into dwg
- embed raster image dwg
- dwg file operations
linktitle: Impor Gambar ke File DWG Menggunakan Java
schemas:
- author: Aspose
  dateModified: '2026-05-20'
  description: Learn how to add image to DWG files using Aspose.CAD for Java and also
    convert DWG to PDF. Follow our step-by-step guide for efficient development.
  headline: Add Image to DWG Files Effortlessly Using Aspose.CAD Java
  type: TechArticle
- description: Learn how to add image to DWG files using Aspose.CAD for Java and also
    convert DWG to PDF. Follow our step-by-step guide for efficient development.
  name: Add Image to DWG Files Effortlessly Using Aspose.CAD Java
  steps:
  - name: Load the DWG File
    text: First, point to the folder that contains your DWG drawing and load it with
      `Image.load`.
  - name: Define the Raster Image Definition
    text: The `CadRasterImageDef` class defines the external raster image resource
      to be embedded in the drawing.
  - name: Set Insertion Point and Scaling Vectors
    text: The insertion point determines where the lower‑left corner of the image
      will appear. The **U** and **V** vectors control horizontal and vertical scaling.
  - name: Create the CadRasterImage Object
    text: The `CadRasterImage` entity represents a raster picture placed in the DWG
      model space.
  - name: Add the Image to Model Space
    text: Insert the raster image into the `*Model_Space` block, then update the drawing’s
      object collection so the definition is saved.
  - name: Configure PDF Export Options (Optional)
    text: '`PdfOptions` specifies settings for saving a CAD drawing as a PDF file.
      `CadRasterizationOptions` defines how the CAD content is rasterized during PDF
      conversion.'
  - name: Save the Resulting PDF
    text: 'Finally, export the modified drawing as a PDF file. The same `image` instance
      is used, so the PDF reflects the newly added raster image. By following these
      steps, you can **add image to dwg** files quickly and also **save dwg as pdf**
      when needed, covering the most common **dwg file operations** in '
  type: HowTo
- questions:
  - answer: Yes, Aspose.CAD for Java works with any IDE that supports JDK 8+, including
      IntelliJ IDEA, Eclipse, and VS Code.
    question: Is Aspose.CAD for Java compatible with all Java development environments?
  - answer: Yes, you can use Aspose.CAD for Java for commercial projects. Visit **[here](https://purchase.aspose.com/buy)**
      for licensing details.
    question: Can I use Aspose.CAD for Java for commercial projects?
  - answer: Yes, you can access the free trial **[here](https://releases.aspose.com/)**.
    question: Is there a free trial available for Aspose.CAD for Java?
  - answer: You can seek support on the **[Aspose.CAD forum](https://forum.aspose.com/c/cad/19)**.
    question: How can I get support for Aspose.CAD for Java?
  - answer: Yes, you can get a temporary license **[here](https://purchase.aspose.com/temporary-license/)**.
    question: Can I obtain a temporary license for Aspose.CAD for Java?
  type: FAQPage
second_title: Aspose.CAD Java API
title: Tambahkan Gambar ke File DWG dengan Mudah Menggunakan Aspose.CAD Java
url: /id/java/dwg-file-operations/import-image-to-dwg/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Tambahkan Gambar ke File DWG dengan Mudah Menggunakan Aspose.CAD Java

Dalam aplikasi Java modern, **menambahkan gambar ke DWG** merupakan kebutuhan umum—baik Anda sedang membangun penampil CAD, mengotomatisasi pembaruan gambar, atau menghasilkan dokumentasi. Aspose.CAD untuk Java memberikan cara yang sederhana dan berperforma tinggi untuk menyematkan gambar raster langsung ke dalam gambar DWG tanpa memerlukan mesin CAD lengkap. Dalam tutorial ini kami akan memandu Anda melalui seluruh proses, mulai dari memuat DWG hingga mengekspor hasilnya sebagai PDF, dan kami juga akan membahas cara **mengimpor gambar ke dwg** dan **mengonversi dwg ke pdf** dalam satu alur kerja.

## Jawaban Cepat
- **Library apa yang saya butuhkan?** Aspose.CAD for Java  
- **Apakah saya juga dapat mengekspor ke PDF?** Yes – use `PdfOptions` with `CadRasterizationOptions`  
- **Apakah saya memerlukan lisensi untuk pengembangan?** A free trial works for testing; a commercial license is required for production  
- **Versi Java mana yang didukung?** Java 8 and higher  
- **Berapa lama implementasinya?** About 10‑15 minutes for a basic image import  

## Apa itu “menambahkan gambar ke dwg”?

Menambahkan gambar ke file DWG berarti menyematkan gambar raster (PNG, JPEG, dll.) sebagai entitas **CadRasterImage** di dalam ruang model gambar, dimana gambar tersebut dapat diposisikan, diskalakan, dan opsional dipotong seperti objek CAD lainnya. Gambar tersebut disimpan dalam tabel objek gambar dan ditampilkan oleh penampil CAD standar.

## Mengapa menggunakan Aspose.CAD untuk Java untuk menambahkan gambar ke dwg?

Anda dapat menyematkan grafik raster ke dalam file DWG tanpa menginstal perangkat lunak CAD pihak ketiga, dan API memberikan kontrol pixel‑perfect atas titik penyisipan, vektor skala, dan batas pemotongan. Aspose.CAD memproses file hingga ukuran 2 GB, mendukung **lebih dari 50 format input dan output**, serta berjalan di Windows, Linux, dan macOS, memungkinkan Anda mengintegrasikan manipulasi CAD ke dalam backend berbasis Java apa pun.

## Prasyarat
- **Aspose.CAD for Java** – unduh JAR terbaru dari situs resmi **[here](https://releases.aspose.com/cad/java/)**.  
- **Java Development Kit** – JDK 8 atau lebih baru, dengan IDE pilihan Anda (IntelliJ IDEA, Eclipse, VS Code, dll.).  
- Lisensi **Aspose.CAD** yang valid untuk penggunaan produksi (versi trial dapat digunakan untuk percobaan).  

## Impor Paket

Impor berikut membawa kelas Aspose.CAD penting yang digunakan untuk manipulasi gambar dan konversi PDF.  
```java
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.cad.CadDrawTypeMode;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.*;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Panduan Langkah‑per‑Langkah

### Langkah 1: Muat File DWG

Pertama, arahkan ke folder yang berisi gambar DWG Anda dan muat dengan `Image.load`.  
```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String srcFile = dataDir + "Drawing11.dwg";
Image image = Image.load(srcFile);
```

### Langkah 2: Definisikan Definisi Gambar Raster

Kelas `CadRasterImageDef` mendefinisikan sumber gambar raster eksternal yang akan disematkan dalam gambar.  
```java
CadRasterImageDef cadRasterImageDef = new CadRasterImageDef("road-sign-custom.png", 640, 562);
cadRasterImageDef.setObjectHandle("A3B4");
```

### Langkah 3: Atur Titik Penyisipan dan Vektor Skala

Titik penyisipan menentukan dimana sudut kiri‑bawah gambar akan muncul. Vektor **U** dan **V** mengontrol skala horizontal dan vertikal.  
```java
Cad3DPoint insertionPoint = new Cad3DPoint(26.77, 22.35);
Cad3DPoint uVector = new Cad3DPoint(0.0061565450840500831, 0);
Cad3DPoint vVector = new Cad3DPoint(0, 0.0061565450840500822);
```

### Langkah 4: Buat Objek CadRasterImage

Entitas `CadRasterImage` mewakili gambar raster yang ditempatkan di ruang model DWG.  
```java
CadRasterImage cadRasterImage = new CadRasterImage(cadRasterImageDef, insertionPoint, uVector, vVector);
cadRasterImage.setImageDefReference("A3B4");
cadRasterImage.setDisplayFlags((short)7);
cadRasterImage.setClippingState((short)0);
cadRasterImage.getClipBoundaryVertexList().add(new Cad2DPoint(-0.5, 0.5));
cadRasterImage.getClipBoundaryVertexList().add(new Cad2DPoint(639.5, 561.5));
```

### Langkah 5: Tambahkan Gambar ke Ruang Model

Sisipkan gambar raster ke dalam blok `*Model_Space`, kemudian perbarui koleksi objek gambar sehingga definisinya disimpan.  
```java
CadImage cadImage = ((CadImage)(image));
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(cadRasterImage);
CadBaseObject[] objs = cadImage.getObjects();
CadBaseObject[] arr = new CadBaseObject[objs.length + 1];
int ind = 0;
for (CadBaseObject obj : objs)
{
    arr[ind] = obj;
    ind++;
}
arr[ind] = cadRasterImageDef;
cadImage.setObjects(arr);
```

### Langkah 6: Konfigurasikan Opsi Ekspor PDF (Opsional)

`PdfOptions` menentukan pengaturan untuk menyimpan gambar CAD sebagai file PDF. `CadRasterizationOptions` mendefinisikan bagaimana konten CAD dirasterisasi selama konversi PDF.  
```java
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setDrawType(CadDrawTypeMode.UseObjectColor);
cadRasterizationOptions.setPageHeight(1600);
cadRasterizationOptions.setPageWidth(1600);
cadRasterizationOptions.setLayouts(new String[] {"Model"});
```

### Langkah 7: Simpan PDF Hasil

Akhirnya, ekspor gambar yang dimodifikasi sebagai file PDF. Instansi `image` yang sama digunakan, sehingga PDF mencerminkan gambar raster yang baru ditambahkan.  
```java
image.save((srcFile + "_generated.pdf"), pdfOptions);
```

Dengan mengikuti langkah‑langkah ini, Anda dapat **menambahkan gambar ke dwg** dengan cepat dan juga **menyimpan dwg sebagai pdf** bila diperlukan, mencakup operasi **file dwg** yang paling umum dalam satu rutinitas yang ringkas.

## Masalah Umum dan Solusinya
- **Image not appearing** – Verifikasi bahwa jalur file gambar (`road-sign-custom.png`) sudah benar dan bahwa dimensi gambar cocok dengan nilai yang diberikan ke `CadRasterImageDef`.  
- **Incorrect scaling** – Sesuaikan vektor U dan V; mereka mewakili satuan gambar per piksel.  
- **PDF looks blank** – Pastikan `CadRasterizationOptions.setDrawType` diatur ke `UseObjectColor` atau mode lain yang sesuai.  

## Pertanyaan yang Sering Diajukan

**Q: Apakah Aspose.CAD untuk Java kompatibel dengan semua lingkungan pengembangan Java?**  
A: Ya, Aspose.CAD untuk Java bekerja dengan IDE apa pun yang mendukung JDK 8+, termasuk IntelliJ IDEA, Eclipse, dan VS Code.

**Q: Bisakah saya menggunakan Aspose.CAD untuk Java untuk proyek komersial?**  
A: Ya, Anda dapat menggunakan Aspose.CAD untuk Java untuk proyek komersial. Kunjungi **[here](https://purchase.aspose.com/buy)** untuk detail lisensi.

**Q: Apakah ada trial gratis yang tersedia untuk Aspose.CAD untuk Java?**  
A: Ya, Anda dapat mengakses trial gratis **[here](https://releases.aspose.com/)**.

**Q: Bagaimana cara mendapatkan dukungan untuk Aspose.CAD untuk Java?**  
A: Anda dapat mencari dukungan di **[Aspose.CAD forum](https://forum.aspose.com/c/cad/19)**.

**Q: Bisakah saya memperoleh lisensi sementara untuk Aspose.CAD untuk Java?**  
A: Ya, Anda dapat memperoleh lisensi sementara **[here](https://purchase.aspose.com/temporary-license/)**.

---

**Terakhir Diperbarui:** 2026-05-20  
**Diuji Dengan:** Aspose.CAD for Java 24.11  
**Penulis:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Tutorial Terkait

- [Ekspor DWG ke PDF atau Raster Menggunakan Aspose.CAD untuk Java](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)
- [Tambahkan Properti Kustom pada File DWG Menggunakan Aspose.CAD untuk Java](/cad/java/additional-features/add-custom-properties/)
- [Simpan CAD sebagai PNG – Konversi Gambar CAD ke Format Gambar Raster Menggunakan Aspose.CAD untuk Java](/cad/java/cad-drawing-conversion/convert-cad-drawing-to-raster-image/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}