---
date: 2026-01-02
description: เรียนรู้วิธีส่งออก DWG เป็น PDF, เปิดใช้งานเส้นที่ซ่อนอยู่, และแปลง DWG
  เป็น PDF ด้วย Aspose.CAD สำหรับ Java ในบทแนะนำแบบขั้นตอนต่อขั้นตอนนี้.
linktitle: Export DWG as PDF with Hidden Lines Using Java
second_title: Aspose.CAD Java API
title: ส่งออก DWG เป็น PDF พร้อมเส้นที่ซ่อน – Aspose.CAD สำหรับ Java
url: /th/java/cad-text-and-formatting/support-hidden-lines-in-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# ส่งออก DWG เป็น PDF พร้อมเส้นที่ซ่อนอยู่ – Aspose.CAD สำหรับ Java

## การแนะนำ

ในบทเรียนนี้คุณจะได้ฟัง ** ส่งออก DWG เป็น PDF** พร้อมคงเส้นประธานของตัวเครื่อง Aspose.CAD สำหรับ Java ความต้องการ ** DWG เป็น PDF**, สร้างคู่มือสไตล์ **dwg to pdf บทช่วยสอน**, หรือเพียงแค่ ** DWG เป็น PDF** พร้อมด้วยบันทึกเส้นตรงของไดรฟ์ข้อมูลคุณผ่านทุกขั้นตอนอีกครั้งที่คุณจะได้ไม่ต้องแปลงและไม่ต้องใส่โปรเจกต์ Java เลย

## คำตอบด่วน
- **บทช่วยสอนนี้ครอบคลุมอะไรบ้าง?** การเปิดใช้งานการเรนเดอร์เส้นตรงในขณะที่ส่งออก DWG เป็น PDF ด้วย Aspose.CAD สำหรับ Java
- **ดำเนินการหลักใด** `ส่งออก dwg เป็น pdf`
- **Do I need a License?** เอกสารฟรีได้สำหรับการทดสอบ; ต้องมีลิขสิทธิ์เรื่องนี้เป็นหลัก.
- **ข้อกำหนดเบื้องต้นมีอะไรบ้าง** คุณสมบัติของนักพัฒนา Java, ไลบรารี Aspose.CAD สำหรับ Java, และไฟล์ DWG.
- **การดำเนินการใช้เวลานานเท่าใด** ส่วนวันที่ 10-15 สำหรับการอธิบายเบื้องต้น

## “ส่งออก dwg เป็น pdf” คืออะไร?
ไฟล์ไฟล์ DWG ไปเป็น PDF จะทำในแกนหลักของ CAD ที่เป็นส่วนประกอบของเอกสารพกพา (PDF) พร้อมด้วยองค์ประกอบคงที่, ประเภทเส้น, ส่วนเรนเดอร์เส้นตรง (โดยทั่วไป) ส่วนท้องถิ่นสามารถแชร์การออกแบบ CAD ให้กับผู้มีส่วนได้ส่วนเสียในส่วนที่ไม่มีคุณสมบัติ CAD หลักการ

## เหตุใดจึงเปิดใช้งานบรรทัดที่ซ่อนอยู่เมื่อส่งออก
ผู้บริหารจะช่วยให้โมเดล 3 ส่วนนี้เป็นส่วนหนึ่งบนหน้า 2 ส่วนที่ชัดเจนยิ่งขึ้นโดยเน้นเฉพาะขอบที่ระบบควบคุมได้เท่านั้น เอกสารที่อ่านได้และมักจะเป็นข้อกำหนดสำหรับเอกสารวิศวกรรม

## ข้อกำหนดเบื้องต้น

1. **Aspose.CAD สำหรับ Java** – ดาวน์โหลดไลบรารีจากเว็บไซต์อย่างเป็นทางการ [ที่นี่](https://releases.aspose.com/cad/java/)
2. **ไฟล์ DWG** – มีไฟล์ DWG เอกสารต้นฉบับที่ทราบตำแหน่ง
3. **สภาพแวดล้อมการพัฒนา Java** – JDK 8+ และ IDE ที่คุณชอบ (Eclipse, IntelliJ และอื่นๆ)

จะต้องปฏิบัติตามขั้นตอนโค้ดกันต่อ

## นำเข้าเนมสเปซ

เริ่มต้นด้วยการนำเข้าคลาสที่จำเป็นเพื่อทำงานกับภาพ CAD และตัวเลือก PDF

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import java.util.Arrays;
import java.util.List;
```

## ขั้นตอนที่ 1: ตั้งค่าโครงการของคุณ

สร้างโปรเจกต์ Java แล้วเพิ่มไฟล์ JAR ของ Aspose.CAD ไปยัง build path จากนั้นกำหนดไดเรกทอรีที่เก็บไฟล์ DWG ของคุณ

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

> **เคล็ดลับสำหรับมือโปร:** ใช้เส้นทางแบบสัมบูรณ์หรือเส้นทางแบบสัมพันธ์ตามทรัพยากรของโปรเจกต์

## ขั้นตอนที่ 2: โหลดไฟล์ DWG

โหลดไฟล์ DWG ต้นฉบับเข้าไปในอ็อบเจกต์ `CadImage` เพื่อให้สามารถจัดการได้

```java
String sourceFilePath = dataDir + "Bottom_plate.dwg";
String outPath = dataDir + "Bottom_plate.pdf";
CadImage cadImage = (CadImage)Image.load(sourceFilePath);
```

## ขั้นตอนที่ 3: กำหนดค่าตัวเลือกการแรสเตอร์

เลือกเลเยอร์ที่ต้องการรวมและตั้งค่าขนาดหน้าให้ตรงกับภาพวาดต้นฉบับ ที่นี่เราจะเปิดใช้งานการเรนเดอร์เส้นที่ซ่อนอยู่โดยระบุ layout

```java
List<String> list = Arrays.asList("Print","L1_RegMark","L2_RegMark");
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageHeight(cadImage.getHeight());
rasterizationOptions.setPageWidth(cadImage.getWidth()) ;
rasterizationOptions.setLayers(list);
```

## ขั้นตอนที่ 4: ตั้งค่าตัวเลือก PDF

บอก Aspose.CAD ให้แปลงข้อมูลเวกเตอร์เป็น PDF โดยใช้ layout “Model” เพื่อให้เส้นที่ซ่อนอยู่ถูกซ่อนไว้

```java
PdfOptions pdfOptions = new PdfOptions();
rasterizationOptions.setLayouts(new String[] { "Model" });
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## ขั้นตอนที่ 5: บันทึกผลลัพธ์

สุดท้าย ส่งออก DWG เป็นไฟล์ PDF เส้นที่ซ่อนอยู่จะได้รับการเคารพตาม layout ที่ตั้งค่าไว้

```java
cadImage.save(outPath, pdfOptions);
System.out.println("\nThe DWG file exported successfully to PDF.\nFile saved at " + dataDir);
```

> **ข้อผิดพลาดทั่วไป:** หากลืมการตั้งค่าเค้าโครงเป็น `"Model"` คุณจะมีเส้นทั้งหมด (รวมถึงเส้นระบบควบคุม) ปรากฏขึ้นเป็นเส้นทึบใน PDF

## บทสรุป

คุณสามารถใช้วิธีการตรวจสอบและเตรียมความพร้อมในระดับการผลิตเพื่อ ** ส่งออก DWG เป็น PDF** พร้อมด้วยหลักสูตรต่างๆ ของโครงสร้าง Aspose.CAD สำหรับ Java วิธีการดำเนินการกับเครื่องมือต่างๆ กับแบบแบตช์, เว็บเซอร์วิส, หรือแอปพลิเคชันสำหรับระบบควบคุม CAD‑to‑PDF อัตโนมัติได้

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถใช้ Aspose.CAD สำหรับ Java กับไฟล์ CAD รูปแบบอื่นได้หรือไม่
A1: ใช่ Aspose.CAD รองรับรูปแบบ CAD หลากหลาย เช่น DWG, DXF, DWF และอื่นๆ

### คำถามที่ 2: Aspose.CAD สำหรับ Java มีรุ่นทดลองใช้ฟรีหรือไม่
ตอบ 2: ได้ คุณสามารถดูรุ่นทดลองใช้ฟรีได้[ที่นี่](https://releases.aspose.com/)

### Q3: ฉันจะรับการสนับสนุน Aspose.CAD สำหรับ Java ได้อย่างไร A3: เยี่ยมชมฟอรัม Aspose.CAD [ที่นี่](https://forum.aspose.com/c/cad/19) เพื่อขอรับการสนับสนุนจากชุมชน

### Q4: ฉันจะหาเอกสารประกอบการใช้งาน Aspose.CAD สำหรับ Java ได้ที่ไหน?
A4: โปรดดูเอกสารประกอบการใช้งาน [ที่นี่](https://reference.aspose.com/cad/java/)

### Q5: ฉันสามารถซื้อใบอนุญาตชั่วคราวสำหรับ Aspose.CAD สำหรับ Java ได้หรือไม่?
A5: ได้ คุณสามารถขอรับใบอนุญาตชั่วคราวได้ [ที่นี่](https://purchase.aspose.com/temporary-license/)

### Q6: วิธีนี้ใช้ได้กับการแปลง DWG เป็น PDF ในสภาพแวดล้อมเซิร์ฟเวอร์แบบไม่มี UI หรือไม่?

A6: ได้อย่างแน่นอน เนื่องจากโค้ดใช้เฉพาะ API ของ Aspose.CAD เท่านั้น จึงทำงานได้โดยไม่ต้องพึ่งพา UI ใดๆ ทำให้เหมาะสำหรับการทำงานอัตโนมัติฝั่งเซิร์ฟเวอร์

---

**อัปเดตล่าสุด:** 2 มกราคม 2026
**ทดสอบกับ:** Aspose.CAD for Java 24.12
**ผู้เขียน:** Aspose 

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}