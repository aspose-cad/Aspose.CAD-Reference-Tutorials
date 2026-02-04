---
date: 2026-02-04
description: เรียนรู้วิธีสร้าง PDF จาก DXF และส่งออก DXF เป็น PDF ด้วย Aspose.CAD
  สำหรับ Java ตั้งค่าความกว้างของหน้ากระดาษ PDF และสร้าง PDF จาก CAD ด้วยการควบคุมที่แม่นยำ
linktitle: Export Specific DXF Layout to PDF with Java
second_title: Aspose.CAD Java API
title: สร้าง PDF จาก Layout DXF เป็น PDF ด้วย Aspose.CAD สำหรับ Java
url: /th/java/additional-features/export-specific-layout-to-pdf/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# สร้าง PDF จาก Layout DXF เป็น PDF ด้วย Aspose.CAD สำหรับ Java

## บทนำ

หากคุณเป็นนักพัฒนา Java ที่ทำงานกับภาพวาด CAD คุณคงรู้ว่า **how to export dxf** อย่างแม่นยำสามารถทำให้โครงการประสบความสำเร็จหรือไม่สำเร็จได้ ไม่ว่าคุณจะสร้างรายงานวิศวกรรม แบ่งปันแบบออกแบบกับลูกค้า หรือทำการแปลงเป็นชุดอัตโนมัติ ไลบรารีการแปลง PDF สำหรับ Java ที่เชื่อถือได้เป็นสิ่งจำเป็น ในบทแนะนำนี้เราจะพาคุณผ่านขั้นตอน **creating pdf from dxf** layout files, การควบคุมขนาดหน้า, และการรักษาคุณภาพเวกเตอร์ให้คงเดิมด้วย **Aspose.CAD for Java**.

## คำตอบสั้น

- **What is the primary library?** Aspose.CAD for Java, ไลบรารีการแปลง PDF สำหรับ Java ที่ออกแบบมาสำหรับ CAD.  
- **Can I choose a specific layout?** ได้ – ใช้ `CadRasterizationOptions.setLayouts()` เพื่อระบุชื่อ layout  
- **How do I set page size?** ปรับ `setPageWidth()` และ `setPageHeight()` ใน rasterization options (เช่น 1600 × 1600).  
- **Do I need a license for production?** จำเป็นต้องมีใบอนุญาตเชิงพาณิชย์สำหรับการใช้งานในสภาพการผลิต; มีรุ่นทดลองฟรีให้ใช้.  
- **What Java version is supported?** Java 8 ขึ้นไป (JDK 1.8+).

## วิธีสร้าง PDF จาก Layout DXF

การส่งออกไฟล์ DXF หมายถึงการแปลงข้อมูลเวกเตอร์ของมันเป็นรูปแบบอื่น—โดยส่วนใหญ่คือ PDF—พร้อมคงรักษาชั้น, ความหนาของเส้น, และข้อมูล layout ไว้ Aspose.CAD จัดการงานที่ซับซ้อนให้คุณ ทำให้คุณสามารถมุ่งเน้นที่ตรรกะของธุรกิจแทนการวิเคราะห์ไฟล์ระดับต่ำ.

## ทำไมต้องใช้ Aspose.CAD สำหรับ Java?

- **Full‑featured CAD support** – รองรับ DWG, DXF, DWF และอื่น ๆ  
- **No external dependencies** – Java แท้, ไม่มี DLL เนทีฟ  
- **Precise rasterization** – เลือกผลลัพธ์เป็นเวกเตอร์หรือแรสเตอร์, ตั้งค่า DPI, ขนาดหน้า, และ layout  
- **High performance** – ปรับให้เหมาะกับการประมวลผลเป็นชุดและสถานการณ์ฝั่งเซิร์ฟเวอร์  
- **Export dxf to pdf** ด้วยบรรทัดโค้ดเดียว, ทำให้เหมาะสำหรับกระบวนการทำงาน **java convert cad pdf**

## ข้อกำหนดเบื้องต้น

ก่อนเริ่ม, โปรดตรวจสอบว่าคุณมี:

1. **Java Development Kit (JDK)** – Java 8 หรือใหม่กว่า ดาวน์โหลดได้จาก [Oracle](https://www.oracle.com/java/technologies/javase-downloads.html).  
2. **Aspose.CAD for Java** – ดาวน์โหลด JAR ล่าสุดจาก [Aspose.CAD download page](https://releases.aspose.com/cad/java/).  
3. IDE หรือเครื่องมือสร้าง (Maven/Gradle) เพื่อเพิ่ม Aspose.CAD JAR ไปยัง classpath ของโปรเจคของคุณ.

## นำเข้า Namespaces

ขั้นแรก, นำเข้าคลาสที่คุณต้องการ การนำเข้าตัวนี้จะให้คุณเข้าถึงการโหลดภาพ, ตัวเลือกการแรสเตอร์, และการตั้งค่าเอาต์พุต PDF.

```java
import com.aspose.cad.Image;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## คู่มือขั้นตอนต่อขั้นตอน

### ขั้นตอนที่ 1: ตั้งค่าไดเรกทอรีทรัพยากร

กำหนดโฟลเดอร์ที่บรรจุไฟล์ DXF ของคุณ แทนที่ตัวแปรตำแหน่งที่เก็บด้วยเส้นทางจริงบนเครื่องของคุณ.

```java
String dataDir = "Your Document Directory" + "DXFDrawings/";
```

> **Pro tip:** ใช้ `System.getProperty("user.dir")` เพื่อสร้างเส้นทางสัมพันธ์ที่ทำงานได้ในทุกสภาพแวดล้อม.

### ขั้นตอนที่ 2: โหลดไฟล์ DXF

โหลด DXF ต้นฉบับโดยใช้ `Image.load()` วิธีนี้จะอ่านไฟล์ CAD เข้าไปในอ็อบเจ็กต์ `Image` ของ Aspose.CAD.

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile); 
```

### ขั้นตอนที่ 3: ตั้งค่าตัวเลือกการแรสเตอร์ (กำหนดความกว้างหน้ากระดาษ PDF ใน Java)

ที่นี่เราจะสร้าง `CadRasterizationOptions` และกำหนดขนาดหน้าผลลัพธ์ ปรับความกว้าง/ความสูงให้ตรงกับมิติ PDF ที่ต้องการ.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);   
rasterizationOptions.setLayouts(new String[] {"Model"});
```

- `setPageWidth` / `setPageHeight` – ควบคุม **set pdf page width** (และความสูง) สำหรับ PDF.  
- `setLayouts` – ระบุ layout ที่จะเรนเดอร์; `"Model"` เป็น model space เริ่มต้นในหลายไฟล์ DXF.

### ขั้นตอนที่ 4: สร้าง PDF Options (Java Convert CAD PDF)

เชื่อมการตั้งค่าการแรสเตอร์กับอินสแตนซ์ `PdfOptions` นี้บอก Aspose.CAD ให้ส่งออกเป็น PDF แทนภาพแรสเตอร์.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### ขั้นตอนที่ 5: ส่งออก DXF เป็น PDF (สร้าง PDF จาก DXF)

สุดท้าย, บันทึกภาพเป็น PDF ชื่อไฟล์ผลลัพธ์จะลงท้ายด้วย `_layout_out_.pdf` เพื่อบ่งบอกว่าการแปลงเฉพาะ layout.

```java
image.save(dataDir + "conic_pyramid_layout_out_.pdf", pdfOptions);
```

หลังจากรัน, คุณจะพบไฟล์ `conic_pyramid_layout_out_.pdf` ในไดเรกทอรีเดียวกัน, มีเฉพาะ layout **Model** ที่เรนเดอร์ตามขนาดที่คุณตั้งค่า.

## กรณีการใช้งานทั่วไป

| สถานการณ์ | เหตุผลที่วิธีนี้ช่วยได้ |
|----------|-----------------------|
| **Automated report generation** | รับประกันว่าทุกรูปภาพจะถูกส่งออกด้วยขนาดหน้าที่เดียวกัน ทำให้ PDF ชุดเป็นแบบเดียวกัน. |
| **Client‑facing design previews** | การส่งออก layout เดียว (เช่น “Model” หรือ “Sheet1”) ลดขนาดไฟล์ในขณะที่คงความแม่นยำของเวกเตอร์. |
| **Legacy DWG to PDF migration** | แม้ว่าตัวอย่างนี้จะใช้ DXF, API เดียวกันทำงานสำหรับ **convert dwg to pdf** ด้วยการเปลี่ยนแปลงโค้ดเพียงเล็กน้อย. |
| **Embedding CAD drawings in web portals** | PDF ที่สร้างขึ้นสามารถสตรีมโดยตรงไปยังเบราว์เซอร์โดยไม่ต้องใช้เครื่องมือแปลงเพิ่มเติม. |

## ปัญหาทั่วไปและวิธีแก้

| ปัญหา | สาเหตุ | วิธีแก้ |
|-------|--------|-----|
| **Blank PDF** | ชื่อ layout ไม่ตรงกัน | ตรวจสอบชื่อ layout ที่แน่นอนในไฟล์ DXF (ใช้ CAD viewer). |
| **Incorrect page size** | `setPageWidth/Height` ไม่ได้ถูกนำไปใช้ | ตรวจสอบว่าคุณตั้งค่าตัวเลือกการแรสเตอร์ **ก่อน** สร้าง `PdfOptions`. |
| **Out‑of‑memory for large files** | โหลด DXF ขนาดใหญ่เข้าสู่หน่วยความจำ | ใช้การสตรีมหรือเพิ่ม heap ของ JVM (`-Xmx2g`). |
| **Missing fonts** | องค์ประกอบข้อความใช้ฟอนต์ที่ไม่มีในระบบ | ติดตั้งฟอนต์ที่จำเป็นบนเซิร์ฟเวอร์หรือฝังฟอนต์ผ่าน `CadRasterizationOptions`. |
| **Need to export multiple layouts** | เรียกใช้ layout เดียวเท่านั้น | เรียก `setLayouts` พร้อมอาร์เรย์ของชื่อ layout และทำซ้ำขั้นตอน `save` สำหรับแต่ละ layout. |

## คำถามที่พบบ่อย

**Q: Is Aspose.CAD for Java suitable for both beginners and experienced developers?**  
A: แน่นอน. API นี้ใช้งานง่ายสำหรับผู้เริ่มต้นในขณะเดียวกันก็ให้การปรับแต่งเชิงลึกสำหรับผู้ใช้ระดับสูง.

**Q: Can I customize the rasterization options for different layouts?**  
A: ใช่. ปรับ `CadRasterizationOptions` (ขนาดหน้า, DPI, สีพื้นหลัง) ตาม layout ที่ต้องการ.

**Q: Where can I find comprehensive documentation for Aspose.CAD for Java?**  
A: เอกสารโดยละเอียดสามารถดูได้ [ที่นี่](https://reference.aspose.com/cad/java/).

**Q: Is there a free trial available for Aspose.CAD for Java?**  
A: มี, คุณสามารถดาวน์โหลดรุ่นทดลองได้ [ที่นี่](https://releases.aspose.com/).

**Q: How can I get support for Aspose.CAD for Java?**  
A: เยี่ยมชมฟอรั่มสนับสนุน [ที่นี่](https://forum.aspose.com/c/cad/19) เพื่อรับความช่วยเหลือจากชุมชนและทีมงาน.

## สรุป

ในคู่มือนี้เราได้สาธิต **how to create pdf from dxf** layout ไปเป็น PDF ด้วย Aspose.CAD สำหรับ Java, ครอบคลุมตั้งแต่การตั้งค่าสภาพแวดล้อมจนถึงการปรับขนาดหน้าที่ละเอียด ด้วยการใช้ **java pdf conversion library** นี้, คุณสามารถทำงานอัตโนมัติของกระบวนการ CAD‑to‑PDF, รักษาความแม่นยำของเวกเตอร์, และรวมการสร้าง PDF อย่างราบรื่นเข้าสู่แอปพลิเคชัน Java ของคุณ ไม่ว่าคุณต้องการ **export dxf to pdf**, **convert dwg to pdf**, หรือ **generate pdf from cad** สำหรับการประมวลผลต่อไป, ขั้นตอนข้างต้นจะให้พื้นฐานที่มั่นคง.

---

**อัปเดตล่าสุด:** 2026-02-04  
**ทดสอบด้วย:** Aspose.CAD for Java 24.12 (ล่าสุด ณ เวลาที่เขียน)  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}