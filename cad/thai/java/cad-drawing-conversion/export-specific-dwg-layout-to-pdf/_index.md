---
date: 2025-12-21
description: เรียนรู้วิธีแปลง DWG เป็น PDF โดยการส่งออกเลย์เอาต์ DWG เฉพาะเป็น PDF
  ด้วย Aspose.CAD สำหรับ Java ทำตามบทเรียนขั้นตอนต่อขั้นตอนการแปลง DWG เป็น PDF นี้เพื่อทำให้กระบวนการทำงาน
  CAD ของคุณเป็นระเบียบและรวดเร็วขึ้น
linktitle: Export Specific DWG Layout to PDF
second_title: Aspose.CAD Java API
title: แปลง DWG เป็น PDF – ส่งออกเลย์เอาต์ด้วย Aspose.CAD สำหรับ Java
url: /th/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# แปลง DWG เป็น PDF – ส่งออก Layout เฉพาะด้วย Aspose.CAD for Java

## บทนำ

ในโลกที่เปลี่ยนแปลงอย่างรวดเร็วของการออกแบบด้วยคอมพิวเตอร์ (Computer‑Aided Design หรือ CAD) การ **convert DWG to PDF** เป็นความต้องการที่พบบ่อยเมื่อแชร์แบบกับลูกค้า ผู้รับเหมา หรือผู้มีส่วนได้ส่วนเสียที่ไม่ใช่เทคนิค Aspose.CAD for Java ทำให้การแปลงนี้ง่ายดาย และยังให้คุณเลือก layout เดียวจากไฟล์ DWG ที่มีหลาย layout ได้อีกด้วย ในบทเรียนนี้เราจะอธิบาย **วิธีส่งออก layout เฉพาะของ DWG** ไปเป็น PDF เพื่อให้คุณส่งมอบสิ่งที่โครงการของคุณต้องการโดยไม่มีหน้าที่เกินหรือการตัดภาพด้วยมือ

## คำตอบสั้น

- **“convert DWG to PDF” หมายถึงอะไร?** มันแปลงภาพวาด DWG ให้เป็นเอกสาร PDF โดยคงข้อมูลเวกเตอร์และความแม่นยำของ layout ไว้  
- **ไลบรารีใดที่ทำการแปลง?** Aspose.CAD for Java มี API ที่พร้อมใช้งาน  
- **ฉันต้องมีลิขสิทธิ์สำหรับการใช้งานจริงหรือไม่?** ใช่ จำเป็นต้องมีลิขสิทธิ์เชิงพาณิชย์; สามารถใช้รุ่นทดลองฟรีเพื่อประเมินผล  
- **ฉันสามารถเลือก layout เดียวได้หรือไม่?** ได้แน่นอน – ตั้งค่า property `Layouts` ให้เป็นชื่อ layout ที่ต้องการ  
- **เวอร์ชัน Java ที่รองรับคืออะไร?** Java 8 และรุ่นต่อมาทั้งหมดรองรับเต็มที่  

## ข้อกำหนดเบื้องต้น

ก่อนเริ่มทำงาน โปรดตรวจสอบว่าคุณมี:

- **สภาพแวดล้อมการพัฒนา Java** – JDK 8+ และ IDE ที่คุณชื่นชอบ  
- **ไลบรารี Aspose.CAD** – ดาวน์โหลด JAR ล่าสุดจากเว็บไซต์อย่างเป็นทางการ **[here](https://releases.aspose.com/cad/java/)**  
- **ไฟล์ DWG** – แบบที่มีอย่างน้อยหนึ่ง layout (เช่น *visualization_-_conference_room.dwg*)  

## ทำไมต้องส่งออก Layout เฉพาะของ DWG ไปเป็น PDF?

ไฟล์ DWG จำนวนมากมีหลาย paper space (layout) การส่งออกไฟล์ทั้งหมดอาจทำให้ได้ PDF ขนาดใหญ่พร้อมหน้าที่ไม่ต้องการ การเลือก layout เดียว:

- ลดขนาดไฟล์  
- ทำให้ผู้ดูมุ่งเน้นไปที่แผ่นแบบที่เกี่ยวข้อง  
- สอดคล้องกับมาตรฐานเอกสารของโครงการ  

## คู่มือขั้นตอน

### ขั้นตอนที่ 1: ตั้งค่าสภาพแวดล้อมโครงการ

สร้างโปรเจกต์ Java ใหม่ (Maven, Gradle หรือ IDE ธรรมดา) แล้วเพิ่ม JAR ของ Aspose.CAD ไปยัง classpath ของคุณ คุณสามารถดาวน์โหลดได้ **[here](https://releases.aspose.com/cad/java/)**  

### ขั้นตอนที่ 2: นำเข้าแพ็กเกจที่จำเป็น

เพิ่ม namespace ของ Aspose.CAD ที่จำเป็นลงในคลาส Java ของคุณ  

```java
import com.aspose.cad.Image;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

### ขั้นตอนที่ 3: โหลดไฟล์ DWG

ระบุตำแหน่งไฟล์ DWG ที่ต้องการแปลงและโหลดเข้าเป็นอ็อบเจ็กต์ `Image`  

```java
String srcFile = dataDir + "visualization_-_conference_room.dwg";
Image image = Image.load(srcFile);
```

### ขั้นตอนที่ 4: กำหนดค่าตัวเลือกการเรสเตอร์ไลเซชัน

กำหนดขนาดหน้าและที่สำคัญคือ layout ที่ต้องการส่งออก  

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
// Specify desired layout name
rasterizationOptions.setLayouts(new String[] {"Layout1"});
```

### ขั้นตอนที่ 5: ตั้งค่าตัวเลือกการส่งออก PDF

เชื่อมการตั้งค่าการเรสเตอร์ไลเซชันกับตัวส่งออก PDF  

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### ขั้นตอนที่ 6: ส่งออก DWG เป็น PDF

บันทึกผลลัพธ์เป็นไฟล์ PDF ผลลัพธ์จะมีเฉพาะ **Layout1** เท่านั้น ทำให้การ **convert DWG to PDF** สะอาดและตรงตามที่ต้องการ  

```java
image.save(dataDir + "ExportSpecificLayoutToPDF_out_.pdf", pdfOptions);
```

## ปัญหาที่พบบ่อยและวิธีแก้

| ปัญหา | สาเหตุ | วิธีแก้ |
|-------|--------|----------|
| **Layout not found** | ชื่อ layout พิมพ์ผิดหรือไม่มีในไฟล์ DWG. | ใช้ `image.getLayoutNames()` เพื่อแสดงรายชื่อ layout ที่มี แล้วเลือกชื่อที่ถูกต้อง. |
| **Low resolution PDF** | `PageWidth`/`PageHeight` มีค่าต่ำเกินไป. | เพิ่มขนาด (เช่น 2000 × 2000) หรือกำหนด `rasterizationOptions.setResolution(300);`. |
| **License exception** | รันโดยไม่มีลิขสิทธิ์ที่ถูกต้องในสภาพแวดล้อมที่ไม่ใช่รุ่นทดลอง. | ใส่ลิขสิทธิ์ Aspose.CAD ก่อนโหลดภาพ: `License license = new License(); license.setLicense("Aspose.CAD.lic");`. |

## คำถามที่พบบ่อย

**Q1: ฉันสามารถใช้ Aspose.CAD for Java ร่วมกับไลบรารี CAD ที่พัฒนาด้วย Java อื่นได้หรือไม่?**  
A: Aspose.CAD for Java เป็นไลบรารีแบบสแตนด์อโลน แต่สามารถผสานกับไลบรารี Java‑based อื่นเพื่อเพิ่มฟังก์ชันการทำงานได้  

**Q2: มีตัวเลือกลิขสิทธิ์สำหรับ Aspose.CAD หรือไม่?**  
A: มี คุณสามารถสำรวจตัวเลือกลิขสิทธิ์และรายละเอียดการซื้อ **[here](https://purchase.aspose.com/buy)**  

**Q3: ฉันจะขอรับลิขสิทธิ์ชั่วคราวสำหรับ Aspose.CAD ได้อย่างไร?**  
A: เยี่ยมชม **[this link](https://purchase.aspose.com/temporary-license/)** เพื่อขอรับลิขสิทธิ์ชั่วคราว  

**Q4: ฉันจะหาแหล่งสนับสนุนสำหรับ Aspose.CAD ได้จากที่ไหน?**  
A: สำหรับคำถามหรือความช่วยเหลือใด ๆ ให้ไปที่ **[Aspose.CAD forum](https://forum.aspose.com/c/cad/19)**  

**Q5: มีรุ่นทดลองฟรีสำหรับ Aspose.CAD หรือไม่?**  
A: มี คุณสามารถเข้าถึงรุ่นทดลองฟรี **[here](https://releases.aspose.com/)**  

## สรุป

โดยทำตาม **dwg to pdf tutorial** นี้ คุณจะมีวิธีที่เชื่อถือได้ในการ **convert DWG to PDF** โดยมุ่งเป้าไปที่ layout เดียว วิธีนี้ช่วยประหยัดพื้นที่จัดเก็บ เร่งการแชร์เอกสาร และทำให้กระบวนการทำงาน CAD ของคุณเป็นระเบียบ คุณสามารถทดลองตั้งค่าการเรสเตอร์ไลเซชันต่าง ๆ หรือรวมหลาย layout เป็น PDF ไฟล์เดียวตามที่โครงการของคุณพัฒนา  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2025-12-21  
**Tested With:** Aspose.CAD for Java 24.12  
**Author:** Aspose