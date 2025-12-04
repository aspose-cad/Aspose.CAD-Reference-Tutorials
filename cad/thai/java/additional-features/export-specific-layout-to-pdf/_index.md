---
date: 2025-12-04
description: เรียนรู้วิธีส่งออกไฟล์ DXF เป็น PDF ด้วย Aspose.CAD สำหรับ Java, สร้าง
  PDF จาก DXF, และตั้งค่าขนาดหน้าใน Java เพื่อการแปลง CAD ที่แม่นยำ.
language: th
linktitle: Export Specific DXF Layout to PDF with Java
second_title: Aspose.CAD Java API
title: วิธีส่งออกเลเอาต์ DXF เป็น PDF ด้วย Aspose.CAD สำหรับ Java
url: /java/additional-features/export-specific-layout-to-pdf/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# วิธีการส่งออกเลเอาต์ DXF เป็น PDF ด้วย Aspose.CAD สำหรับ Java

## บทนำ

หากคุณเป็นนักพัฒนา Java ที่ทำงานกับภาพวาด CAD คุณคงทราบว่า **วิธีการส่งออก dxf** อย่างแม่นยำสามารถทำให้โครงการประสบความสำเร็จหรือไม่สำเร็จได้ ไม่ว่าจะเป็นการสร้างรายงานวิศวกรรม การแชร์แบบออกแบบกับลูกค้า หรือการทำการแปลงเป็นชุดอัตโนมัติ การมีไลบรารีแปลง PDF สำหรับ Java ที่เชื่อถือได้จึงเป็นสิ่งจำเป็น ในบทแนะนำนี้เราจะพาคุณผ่านขั้นตอนการส่งออกเลเอาต์ DXF เฉพาะเป็น PDF ด้วย **Aspose.CAD for Java** โดยจะแสดงวิธี **สร้าง pdf จาก dxf** การควบคุมขนาดหน้า และการรักษาคุณภาพเวกเตอร์ให้คงที่

## คำตอบสั้น
- **ไลบรารีหลักคืออะไร?** Aspose.CAD for Java, ไลบรารีแปลง PDF สำหรับ CAD ที่ออกแบบมาสำหรับ Java
- **สามารถเลือกเลเอาต์เฉพาะได้หรือไม่?** ได้ – ใช้ `CadRasterizationOptions.setLayouts()` เพื่อระบุชื่อเลเอาต์
- **ตั้งค่าขนาดหน้าอย่างไร?** ปรับ `setPageWidth()` และ `setPageHeight()` ใน rasterization options (เช่น 1600 × 1600)
- **ต้องมีลิขสิทธิ์สำหรับการใช้งานในผลิตภัณฑ์หรือไม่?** จำเป็นต้องมีลิขสิทธิ์เชิงพาณิชย์สำหรับการใช้งานในผลิตภัณฑ์; มีรุ่นทดลองฟรีให้ใช้
- **รองรับเวอร์ชัน Java ใด?** Java 8 ขึ้นไป (JDK 1.8+)

## “วิธีการส่งออก dxf” ใน Java คืออะไร?

การส่งออกไฟล์ DXF หมายถึงการแปลงข้อมูลเวกเตอร์ของไฟล์เป็นรูปแบบอื่น—โดยส่วนใหญ่คือ PDF—พร้อมคงรักษาชั้น, ความหนาของเส้น, และข้อมูลเลเอาต์ไว้ Aspose.CAD จะจัดการส่วนที่ซับซ้อนให้คุณ ทำให้คุณสามารถมุ่งเน้นที่ตรรกะธุรกิจแทนการพาร์สไฟล์ระดับล่าง

## ทำไมต้องใช้ Aspose.CAD for Java?

- **รองรับ CAD อย่างครบวงจร** – รองรับ DWG, DXF, DWF และอื่น ๆ
- **ไม่มีการพึ่งพาไลบรารีภายนอก** – Pure Java, ไม่ต้องใช้ DLL แบบเนทีฟ
- **การเรสเตอร์ไลซ์ที่แม่นยำ** – เลือกเอาต์พุตเป็นเวกเตอร์หรือแรสเตอร์ ตั้งค่า DPI, ขนาดหน้า, และเลเอาต์
- **ประสิทธิภาพสูง** – ปรับให้เหมาะกับการประมวลผลเป็นชุดและสถานการณ์ฝั่งเซิร์ฟเวอร์

## ข้อกำหนดเบื้องต้น

ก่อนเริ่มทำตามขั้นตอนต่อไปนี้ให้ตรวจสอบว่าคุณมี:

1. **Java Development Kit (JDK)** – Java 8 หรือใหม่กว่า ดาวน์โหลดได้จาก [Oracle](https://www.oracle.com/java/technologies/javase-downloads.html)
2. **Aspose.CAD for Java** – ดาวน์โหลด JAR ล่าสุดจาก [หน้าดาวน์โหลด Aspose.CAD](https://releases.aspose.com/cad/java/)
3. IDE หรือเครื่องมือสร้าง (Maven/Gradle) เพื่อเพิ่ม JAR ของ Aspose.CAD เข้าไปใน classpath ของโครงการ

## นำเข้า Namespaces

ก่อนอื่นให้นำเข้าคลาสที่จำเป็น การนำเข้าตัวนี้จะทำให้คุณเข้าถึงการโหลดภาพ, ตัวเลือกการเรสเตอร์ไลซ์, และการตั้งค่าเอาต์พุต PDF ได้

```java
import com.aspose.cad.Image;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

### คู่มือแบบขั้นตอน

### ขั้นตอนที่ 1: ตั้งค่าโฟลเดอร์ทรัพยากร

กำหนดโฟลเดอร์ที่เก็บไฟล์ DXF ของคุณ แทนที่ตัวแปร placeholder ด้วยพาธที่แท้จริงบนเครื่องของคุณ

```java
String dataDir = "Your Document Directory" + "DXFDrawings/";
```

> **เคล็ดลับ:** ใช้ `System.getProperty("user.dir")` เพื่อสร้างพาธแบบ relative ที่ทำงานได้ในทุกสภาพแวดล้อม

### ขั้นตอนที่ 2: โหลดไฟล์ DXF

โหลดไฟล์ DXF ต้นฉบับด้วย `Image.load()` วิธีนี้จะอ่านไฟล์ CAD เข้าเป็นอ็อบเจ็กต์ `Image` ของ Aspose.CAD

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile); 
```

### ขั้นตอนที่ 3: ตั้งค่าตัวเลือกการเรสเตอร์ไลซ์ (ตั้งค่าขนาดหน้า Java)

ที่นี่เราจะสร้าง `CadRasterizationOptions` และกำหนดขนาดหน้าที่ต้องการออกเป็น PDF ปรับความกว้าง/สูงให้ตรงกับมิติที่ต้องการ

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);   
rasterizationOptions.setLayouts(new String[] {"Model"});
```

- `setPageWidth` / `setPageHeight` – ควบคุม **set page size java** สำหรับ PDF
- `setLayouts` – ระบุเลเอาต์ที่ต้องการเรนเดอร์; `"Model"` เป็นเลเอาต์โมเดลเริ่มต้นในไฟล์ DXF จำนวนมาก

### ขั้นตอนที่ 4: สร้าง PDF Options (Java Convert CAD PDF)

เชื่อมการตั้งค่าการเรสเตอร์ไลซ์กับอินสแตนซ์ `PdfOptions` ซึ่งบอก Aspose.CAD ให้ส่งออกเป็น PDF แทนภาพแรสเตอร์

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### ขั้นตอนที่ 5: ส่งออก DXF เป็น PDF (Create PDF from DXF)

สุดท้ายให้บันทึกภาพเป็น PDF ชื่อไฟล์ผลลัพธ์จะลงท้ายด้วย `_layout_out_.pdf` เพื่อบ่งบอกว่าการแปลงเป็นแบบเฉพาะเลเอาต์

```java
image.save(dataDir + "conic_pyramid_layout_out_.pdf", pdfOptions);
```

หลังจากรันเสร็จ คุณจะพบไฟล์ `conic_pyramid_layout_out_.pdf` ในโฟลเดอร์เดียวกัน ซึ่งมีเพียงเลเอาต์ **Model** ที่เรนเดอร์ตามขนาดที่คุณตั้งค่าไว้

## ปัญหาทั่วไปและวิธีแก้

| ปัญหา | สาเหตุ | วิธีแก้ |
|-------|--------|--------|
| **PDF ว่างเปล่า** | ชื่อเลเอาต์ไม่ตรง | ตรวจสอบชื่อเลเอาต์ที่แน่นอนในไฟล์ DXF (ใช้โปรแกรมดู CAD) |
| **ขนาดหน้าไม่ถูกต้อง** | `setPageWidth/Height` ไม่ถูกนำไปใช้ | ตรวจสอบว่าคุณตั้งค่าตัวเลือกการเรสเตอร์ไลซ์ **ก่อน** สร้าง `PdfOptions` |
| **หน่วยความจำไม่พอสำหรับไฟล์ขนาดใหญ่** | โหลด DXF ขนาดใหญ่มากในหน่วยความจำ | ใช้การสตรีมหรือเพิ่ม heap ของ JVM (`-Xmx2g`) |
| **ฟอนต์หาย** | องค์ประกอบข้อความใช้ฟอนต์ที่ไม่มีบนเซิร์ฟเวอร์ | ติดตั้งฟอนต์ที่จำเป็นบนเซิร์ฟเวอร์หรือฝังฟอนต์ผ่าน `CadRasterizationOptions` |

## คำถามที่พบบ่อย

**ถาม: Aspose.CAD for Java เหมาะกับทั้งผู้เริ่มต้นและนักพัฒนาที่มีประสบการณ์หรือไม่?**  
ตอบ: แน่นอน API ถูกออกแบบให้ใช้งานง่ายสำหรับผู้ใหม่ในขณะเดียวกันก็ให้ความยืดหยุ่นลึกซึ้งสำหรับผู้ใช้ระดับสูง

**ถาม: สามารถปรับตัวเลือกการเรสเตอร์ไลซ์สำหรับเลเอาต์ต่าง ๆ ได้หรือไม่?**  
ตอบ: ได้ คุณสามารถปรับ `CadRasterizationOptions` (ขนาดหน้า, DPI, สีพื้นหลัง) แยกตามเลเอาต์ตามต้องการ

**ถาม: จะหาเอกสารประกอบที่ครบถ้วนสำหรับ Aspose.CAD for Java ได้จากที่ไหน?**  
ตอบ: เอกสารโดยละเอียดมีให้ที่ [นี่](https://reference.aspose.com/cad/java/)

**ถาม: มีรุ่นทดลองฟรีสำหรับ Aspose.CAD for Java หรือไม่?**  
ตอบ: มี คุณสามารถดาวน์โหลดรุ่นทดลองได้จาก [ที่นี่](https://releases.aspose.com/)

**ถาม: จะขอรับการสนับสนุนสำหรับ Aspose.CAD for Java อย่างไร?**  
ตอบ: เยี่ยมชมฟอรั่มสนับสนุน [ที่นี่](https://forum.aspose.com/c/cad/19) เพื่อรับความช่วยเหลือจากชุมชนและทีมงาน

## สรุป

ในคู่มือนี้เราได้สาธิต **วิธีการส่งออก dxf** เลเอาต์เป็น PDF ด้วย Aspose.CAD for Java ตั้งแต่การเตรียมสภาพแวดล้อมจนถึงการปรับขนาดหน้าอย่างละเอียด ด้วยการใช้ **java pdf conversion library** นี้ คุณสามารถทำอัตโนมัติการแปลง CAD‑to‑PDF รักษาความคมชัดของเวกเตอร์ และรวมการสร้าง PDF อย่างราบรื่นเข้าไปในแอปพลิเคชัน Java ของคุณได้

---

**อัปเดตล่าสุด:** 2025-12-04  
**ทดสอบกับ:** Aspose.CAD for Java 24.12 (ล่าสุด ณ เวลาที่เขียน)  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}