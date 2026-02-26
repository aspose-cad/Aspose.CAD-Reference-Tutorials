---
date: 2026-01-12
description: Pelajari cara menambahkan gambar ke file DWG menggunakan Aspose.CAD untuk
  Java dan juga mengonversi DWG ke PDF. Ikuti panduan langkah demi langkah kami untuk
  pengembangan yang efisien.
linktitle: Import Image to DWG File Using Java
second_title: Aspose.CAD Java API
title: Tambahkan Gambar ke File DWG dengan Mudah Menggunakan Aspose.CAD Java
url: /id/java/dwg-file-operations/import-image-to-dwg/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Menambahkan Gambar ke File DWG dengan Mudah Menggunakan Aspose.CAD Java

Dalam aplikasi Java modern, **menambahkan gambar ke file DWG** adalah kebutuhan umum—baik Anda sedang membangun penampil CAD, mengotomatisasi pembaruan gambar, atau menghasilkan dokumentasi. Aspose.CAD untuk Java memberikan cara yang sederhana dan berperforma tinggi untuk menyisipkan gambar raster langsung ke dalam gambar DWG tanpa memerlukan mesin CAD lengkap. Pada tutorial ini kami akan memandu Anda melalui seluruh proses, mulai dari memuat DWG hingga mengekspor hasilnya sebagai PDF.

## Jawaban Cepat
- **Perpustakaan apa yang saya perlukan?** Aspose.CAD untuk Java  
- **Apakah saya juga dapat mengekspor ke PDF?** Ya – gunakan `PdfOptions` dengan `CadRasterizationOptions`  
- **Apakah saya memerlukan lisensi untuk pengembangan?** Versi percobaan gratis dapat digunakan untuk pengujian; lisensi komersial diperlukan untuk produksi  
- **Versi Java mana yang didukung?** Java 8 ke atas  
- **Berapa lama implementasinya?** Sekitar 10‑15 menit untuk impor gambar dasar

## Apa itu “menambahkan gambar ke dwg”?
Menambahkan gambar ke file DWG berarti menyisipkan gambar raster (PNG, JPEG, dll.) sebagai objek `CadRasterImage` di dalam ruang model gambar. Gambar tersebut menjadi bagian dari pohon entitas CAD dan dapat diposisikan, diskalakan, serta dipotong seperti objek CAD lainnya.

## Mengapa menggunakan Aspose.CAD untuk Java untuk menambahkan gambar ke dwg?
- **Tidak memerlukan perangkat lunak CAD** – API menangani parsing DWG secara internal.  
- **Kontrol detail** atas titik sisipan, vektor skala, dan pemotongan.  
- **Konversi PDF bawaan** sehingga Anda dapat menghasilkan PDF yang dapat dicetak dalam alur kerja yang sama.  
- **Lintas platform** – berfungsi di Windows, Linux, dan macOS.

## Prasyarat
- Aspose.CAD untuk Java: Pastikan Anda telah menginstal pustaka Aspose.CAD. Anda dapat mengunduhnya [di sini](https://releases.aspose.com/cad/java/).  
- Lingkungan Pengembangan Java: JDK 8+ dengan IDE pilihan Anda (IntelliJ, Eclipse, VS Code, dll.).

## Mengimpor Paket
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
Buat `CadRasterImageDef` yang merujuk ke file PNG eksternal yang ingin Anda sematkan. Konstruktor menerima nama file gambar dan dimensi pixel‑nya.
```java
CadRasterImageDef cadRasterImageDef = new CadRasterImageDef("road-sign-custom.png", 640, 562);
cadRasterImageDef.setObjectHandle("A3B4");
```

### Langkah 3: Atur Titik Sisipan dan Vektor Skala
Titik sisipan menentukan di mana sudut kiri‑bawah gambar akan muncul. Vektor **U** dan **V** mengontrol skala horizontal dan vertikal.
```java
Cad3DPoint insertionPoint = new Cad3DPoint(26.77, 22.35);
Cad3DPoint uVector = new Cad3DPoint(0.0061565450840500831, 0);
Cad3DPoint vVector = new Cad3DPoint(0, 0.0061565450840500822);
```

### Langkah 4: Buat Objek CadRasterImage
Gabungkan definisi, titik sisipan, dan vektor ke dalam `CadRasterImage`. Anda juga dapat mengatur batas pemotongan jika hanya ingin bagian tertentu gambar yang terlihat.
```java
CadRasterImage cadRasterImage = new CadRasterImage(cadRasterImageDef, insertionPoint, uVector, vVector);
cadRasterImage.setImageDefReference("A3B4");
cadRasterImage.setDisplayFlags((short)7);
cadRasterImage.setClippingState((short)0);
cadRasterImage.getClipBoundaryVertexList().add(new Cad2DPoint(-0.5, 0.5));
cadRasterImage.getClipBoundaryVertexList().add(new Cad2DPoint(639.5, 561.5));
```

### Langkah 5: Tambahkan Gambar ke Ruang Model
Sisipkan gambar raster ke dalam blok `*Model_Space`, lalu perbarui koleksi objek gambar sehingga definisinya disimpan.
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
Jika Anda juga memerlukan versi PDF dari gambar, konfigurasikan `PdfOptions` bersama dengan `CadRasterizationOptions`. Langkah ini menunjukkan cara **mengonversi dwg ke pdf** dalam alur kerja yang sama.
```java
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setDrawType(CadDrawTypeMode.UseObjectColor);
cadRasterizationOptions.setPageHeight(1600);
cadRasterizationOptions.setPageWidth(1600);
cadRasterizationOptions.setLayouts(new String[] {"Model"});
```

### Langkah 7: Simpan PDF yang Dihasilkan
Akhirnya, ekspor gambar yang telah dimodifikasi sebagai file PDF. Instansi `image` yang sama digunakan, sehingga PDF mencerminkan gambar raster yang baru ditambahkan.
```java
image.save((srcFile + "_generated.pdf"), pdfOptions);
```

Dengan mengikuti langkah‑langkah ini, Anda dapat **menambahkan gambar ke dwg** dengan cepat dan juga **menyimpan dwg sebagai pdf** bila diperlukan.

## Masalah Umum dan Solusinya
- **Gambar tidak muncul** – Pastikan jalur file gambar (`road-sign-custom.png`) benar dan dimensi gambar cocok dengan nilai yang diberikan ke `CadRasterImageDef`.  
- **Skala tidak tepat** – Sesuaikan vektor U dan V; mereka mewakili satuan gambar per pixel.  
- **PDF terlihat kosong** – Pastikan `CadRasterizationOptions.setDrawType` diatur ke `UseObjectColor` atau mode yang sesuai lainnya.

## Pertanyaan yang Sering Diajukan

**T: Apakah Aspose.CAD untuk Java kompatibel dengan semua lingkungan pengembangan Java?**  
J: Ya, Aspose.CAD untuk Java kompatibel dengan sebagian besar lingkungan pengembangan Java.

**T: Bisakah saya menggunakan Aspose.CAD untuk Java untuk proyek komersial?**  
J: Ya, Anda dapat menggunakan Aspose.CAD untuk Java untuk proyek komersial. Kunjungi [di sini](https://purchase.aspose.com/buy) untuk detail lisensi.

**T: Apakah tersedia versi percobaan gratis untuk Aspose.CAD untuk Java?**  
J: Ya, Anda dapat mengakses versi percobaan gratis [di sini](https://releases.aspose.com/).

**T: Bagaimana cara mendapatkan dukungan untuk Aspose.CAD untuk Java?**  
J: Anda dapat mencari dukungan di [forum Aspose.CAD](https://forum.aspose.com/c/cad/19).

**T: Bisakah saya memperoleh lisensi sementara untuk Aspose.CAD untuk Java?**  
J: Ya, Anda dapat memperoleh lisensi sementara [di sini](https://purchase.aspose.com/temporary-license/).

---

**Terakhir Diperbarui:** 2026-01-12  
**Diuji Dengan:** Aspose.CAD untuk Java 24.11  
**Penulis:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}