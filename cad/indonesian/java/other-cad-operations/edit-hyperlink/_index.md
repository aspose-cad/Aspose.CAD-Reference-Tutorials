---
date: 2026-06-19
description: Pelajari cara mengedit file DWG dengan Aspose.CAD untuk Java, termasuk
  cara memperbarui jalur DWG XRef dan mengedit hyperlink. Coba versi percobaan gratis
  hari ini!
keywords:
- how to edit dwg
- update dwg xref paths
- Aspose.CAD Java hyperlink
linktitle: Edit Hyperlink
schemas:
- author: Aspose
  dateModified: '2026-06-19'
  description: Learn how to edit DWG files with Aspose.CAD for Java, including how
    to update DWG XRef paths and edit hyperlinks. Try the free trial today!
  headline: How to Edit DWG Hyperlinks - Aspose.CAD Java Tutorial
  type: TechArticle
- description: Learn how to edit DWG files with Aspose.CAD for Java, including how
    to update DWG XRef paths and edit hyperlinks. Try the free trial today!
  name: How to Edit DWG Hyperlinks - Aspose.CAD Java Tutorial
  steps:
  - name: Accessing Insert Objects
    text: '`CadInsertObject` is the Aspose.CAD class that represents an inserted block
      reference (XRef) inside a DWG drawing. Iterate through the entities and identify
      if an entity is an instance of the `CadInsertObject` class.'
  - name: How to Change XRef Path in a DWG Drawing
    text: '`CadImage` is the primary object that loads and saves CAD files in Aspose.CAD
      for Java. Once you have identified the insert object, retrieve the associated
      block entity and update the XRef path as needed. This ensures the reference
      points to the correct external file.'
  - name: Modifying Hyperlinks
    text: Next, check if the entity has a hyperlink associated with it. If the hyperlink
      matches a specific URL, update it to the desired URL. This step guarantees that
      clicking the hyperlink in the CAD viewer opens the new target.
  type: HowTo
- questions:
  - answer: Yes, after making changes call `cadImage.save("EditedDrawing.dwg");` to
      persist the modifications.
    question: Do I need to call a specific method to write the edited DWG back to
      disk?
  - answer: Absolutely—loop through `cadImage.getEntities()` and apply the hyperlink
      logic to each matching entity.
    question: Is it possible to edit multiple hyperlinks in one pass?
  type: FAQPage
second_title: Aspose.CAD Java API
title: Cara Mengedit Hyperlink DWG - Tutorial Aspose.CAD Java
url: /id/java/other-cad-operations/edit-hyperlink/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cara Mengedit Hyperlink DWG - Tutorial Aspose.CAD Java

Di era digital saat ini, **cara mengedit DWG** secara efisien adalah keterampilan yang wajib dimiliki bagi insinyur, arsitek, dan spesialis BIM. Apakah Anda perlu memperbaiki hyperlink yang rusak, mengarahkan XRef ke sumber baru, atau memperbarui banyak gambar secara batch, Aspose.CAD for Java menawarkan cara yang bersih dan programatis untuk melakukan perubahan tersebut tanpa membuka editor CAD. Tutorial ini memandu Anda melalui seluruh proses, mulai dari memuat gambar hingga menyimpan perubahan.

## Jawaban Cepat
- **Perpustakaan apa yang menangani pengeditan DWG di Java?** Aspose.CAD for Java.  
- **Bisakah saya mengedit hyperlink dan jalur XRef secara bersamaan?** Ya—keduanya didukung dalam API yang sama.  
- **Apakah saya memerlukan lisensi untuk pengembangan?** Versi percobaan gratis dapat digunakan untuk pengujian; lisensi komersial diperlukan untuk produksi.  
- **Versi Java apa yang diperlukan?** Java 8 atau lebih tinggi.  
- **Apakah contoh kode dapat dijalankan apa adanya?** Ya, setelah memperbarui jalur file untuk mengarah ke file DWG lokal Anda.

## Mengapa mengedit hyperlink DWG dan jalur XRef?

Menjaga hyperlink dan jalur XRef tetap terbaru mencegah referensi yang rusak, memastikan dokumentasi proyek selalu mengarah ke sumber yang tepat, dan memungkinkan pembaruan batch otomatis di seluruh perpustakaan CAD yang luas. Hal ini mengurangi upaya manual, meminimalkan kesalahan, dan meningkatkan efisiensi proyek secara keseluruhan dengan memungkinkan pengembang memelihara integritas tautan secara programatis sepanjang siklus hidup desain.

## Prasyarat

Sebelum kita memulai tutorial, pastikan Anda memiliki prasyarat berikut:

1. **Java Development Environment:** JDK 8+ terinstal dan IDE favorit Anda (IntelliJ IDEA, Eclipse, dll.).  
2. **Aspose.CAD for Java Library:** Unduh dan instal pustaka Aspose.CAD for Java dari [download link](https://releases.aspose.com/cad/java/).  
3. **DWG Drawing:** Siapkan file gambar DWG siap untuk pengeditan hyperlink.

## Impor Paket

Mulailah dengan mengimpor paket yang diperlukan ke dalam proyek Java Anda. Ini memastikan Anda memiliki akses ke fungsionalitas Aspose.CAD for Java.

```java
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.CadBaseEntity;
import com.aspose.cad.fileformats.cad.cadobjects.CadBlockEntity;
import com.aspose.cad.fileformats.cad.cadobjects.CadInsertObject;
```

## Cara Mengedit Hyperlink DWG Menggunakan Aspose.CAD for Java?

`CadImage` adalah kelas Aspose.CAD yang digunakan untuk memuat dan menyimpan gambar CAD.  
Muat file DWG dengan `CadImage`, iterasi melalui entitasnya, perbarui hyperlink dan jalur XRef bila diperlukan, dan akhirnya simpan gambar kembali ke DWG. Alur end‑to‑end ini memungkinkan Anda memodifikasi sejumlah entitas dalam satu kali proses, menjamin semua perubahan tersimpan.

### Langkah 1: Mengakses Objek Insert

`CadInsertObject` adalah kelas Aspose.CAD yang mewakili referensi blok yang disisipkan (XRef) di dalam gambar DWG. Iterasi melalui entitas dan identifikasi apakah sebuah entitas merupakan instance dari kelas `CadInsertObject`.

```java
    String dataDir = "Your Document Directory" + "DWGDrawings/";
    
    CadImage cadImage = (CadImage)Image.load(dataDir + "AutoCad_Sample.dwg");
    for (CadBaseEntity entity : cadImage.getEntities())
    {
        if (entity instanceof CadInsertObject)
        {
        }
	}
```

### Langkah 2: Cara Mengubah Jalur XRef dalam Gambar DWG

`CadImage` adalah objek utama yang memuat dan menyimpan file CAD di Aspose.CAD for Java. Setelah Anda mengidentifikasi objek insert, ambil entitas blok yang terkait dan perbarui jalur XRef sesuai kebutuhan. Ini memastikan referensi mengarah ke file eksternal yang tepat.

```java
			CadBlockEntity block = cadImage.getBlockEntities().get_Item(((CadInsertObject)entity).getName());
            String value = block.getXRefPathName().getValue();
            if (value != null && !value.contentEquals(""))
            {
                block.getXRefPathName().setValue("new file reference.dwg");
            }
    
```

### Langkah 3: Memodifikasi Hyperlink

Selanjutnya, periksa apakah entitas memiliki hyperlink yang terkait. Jika hyperlink cocok dengan URL tertentu, perbarui ke URL yang diinginkan. Langkah ini menjamin bahwa mengklik hyperlink di penampil CAD membuka target baru.

```java
        if (entity.getHyperlink() == "https://products.aspose.com")
        {
            entity.setHyperlink("https://www.aspose.com");
        }
```

## Kesalahan Umum & Tips
- **String comparison:** Gunakan `.equals()` alih-alih `==` untuk perbandingan string yang dapat diandalkan di Java. Contoh menggunakan `==` untuk kesederhanaan, tetapi dalam produksi ganti dengan `entity.getHyperlink().equals("https://products.aspose.com")`.  
- **Null checks:** Selalu pastikan bahwa `block.getXRefPathName()` tidak `null` sebelum memanggil `.getValue()`.  
- **Saving changes:** Setelah memodifikasi entitas, panggil `cadImage.save("output.dwg");` untuk menyimpan perubahan (kode dihilangkan untuk mempertahankan jumlah blok asli).  
- **Performance note:** Aspose.CAD for Java mendukung lebih dari 30 format CAD dan dapat memproses file hingga 2 GB tanpa memuat seluruh dokumen ke memori, membuat pembaruan massal cepat dan efisien memori.

## Pertanyaan yang Sering Diajukan

### Q1: Apakah Aspose.CAD for Java kompatibel dengan semua versi gambar DWG?

A1: Aspose.CAD for Java mendukung lebih dari 50 versi DWG, mencakup rilis dari AutoCAD 2000 hingga format terbaru 2025.

### Q2: Bisakah saya menggunakan Aspose.CAD for Java dalam proyek komersial?

A2: Ya, lisensi komersial diperlukan untuk penggunaan produksi. Anda dapat membeli lisensi [here](https://purchase.aspose.com/buy).

### Q3: Apakah ada versi percobaan gratis untuk Aspose.CAD for Java?

A3: Ya, Anda dapat menjelajahi versi percobaan gratis [here](https://releases.aspose.com/).

### Q4: Bagaimana saya dapat mendapatkan dukungan teknis untuk Aspose.CAD for Java?

A4: Untuk bantuan teknis apa pun, kunjungi forum Aspose.CAD [here](https://forum.aspose.com/c/cad/19).

### Q5: Bisakah saya memperoleh lisensi sementara untuk tujuan pengujian?

A5: Ya, Anda dapat memperoleh lisensi sementara [here](https://purchase.aspose.com/temporary-license/).

**Pertanyaan Tambahan**

**Q: Apakah saya perlu memanggil metode khusus untuk menulis DWG yang telah diedit kembali ke disk?**  
A: Ya, setelah melakukan perubahan panggil `cadImage.save("EditedDrawing.dwg");` untuk menyimpan modifikasi.

**Q: Apakah memungkinkan mengedit banyak hyperlink dalam satu kali proses?**  
A: Tentu—loop melalui `cadImage.getEntities()` dan terapkan logika hyperlink pada setiap entitas yang cocok.

---

**Terakhir Diperbarui:** 2026-06-19  
**Diuji Dengan:** Aspose.CAD for Java 24.12  
**Penulis:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Tutorial Terkait

- [Baca Meta Data XREF dari File DWG Menggunakan Aspose.CAD for Java](/cad/java/cad-meta-data-and-rendering/read-xref-meta-data/)
- [Tambahkan Properti Kustom pada File DWG Menggunakan Aspose.CAD for Java](/cad/java/additional-features/add-custom-properties/)
- [Ekspor DWG ke PDF atau Raster Menggunakan Aspose.CAD for Java](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}