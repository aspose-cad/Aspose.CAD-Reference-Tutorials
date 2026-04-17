---
date: 2026-03-05
description: เรียนรู้วิธีการส่งออกไฟล์ DWG เป็น PDF, เปิดใช้งานเส้นที่ซ่อนอยู่, และแปลง
  DWG เป็น PDF ด้วย Aspose.CAD สำหรับ Java ในบทแนะนำแบบทีละขั้นตอนนี้
linktitle: Export DWG as PDF Using Java
second_title: Aspose.CAD Java API
title: ส่งออก DWG เป็น PDF พร้อมเส้นที่ซ่อน – Aspose.CAD สำหรับ Java
url: /th/java/cad-text-and-formatting/support-hidden-lines-in-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# ส่งออก DWG เป็น PDF พร้อมเส้นที่ซ่อน – Aspose.CAD for Java

## บทนำ

ในบทแนะนำนี้คุณจะได้เรียนรู้วิธี **export dwg to pdf** พร้อมคงเส้นที่ซ่อนโดยใช้ Aspose.CAD for Java ไม่ว่าคุณจะต้องการ **convert DWG to PDF**, สร้างคู่มือสไตล์ **dwg to pdf tutorial**, หรือเพียงแค่ **save DWG as PDF** พร้อมการสนับสนุนเส้นที่ซ่อน เราจะพาคุณผ่านทุกขั้นตอนจนเสร็จสิ้น เมื่อเสร็จคุณจะมีโซลูชันพร้อมใช้งานที่สามารถนำไปใส่ในโปรเจกต์ Java ใดก็ได้.

## คำตอบอย่างรวดเร็ว
- **What does this tutorial cover?** การเปิดใช้งานการเรนเดอร์เส้นที่ซ่อนขณะส่งออก DWG เป็น PDF ด้วย Aspose.CAD for Java.  
- **Which primary operation is performed?** `export dwg to pdf`.  
- **Do I need a license?** การทดลองใช้ฟรีสามารถใช้ทดสอบได้; ต้องมีใบอนุญาตเชิงพาณิชย์สำหรับการใช้งานจริง.  
- **What are the prerequisites?** สภาพแวดล้อมการพัฒนา Java, ไลบรารี Aspose.CAD for Java, และไฟล์ DWG.  
- **How long does implementation take?** ประมาณ 10‑15 นาทีสำหรับการตั้งค่าเบื้องต้น.

## อะไรคือ “export dwg to pdf”?

การส่งออกไฟล์ DWG เป็น PDF จะเปลี่ยนแปลงภาพวาด CAD ที่เป็นเวกเตอร์ให้เป็นรูปแบบเอกสารพกพาในขณะที่คงชั้น, ประเภทเส้น, และการเรนเดอร์เส้นที่ซ่อนแบบเลือกได้ ทำให้การแชร์การออกแบบ CAD กับผู้มีส่วนได้ส่วนเสียที่อาจไม่มีซอฟต์แวร์ CAD เป็นเรื่องง่าย.

## วิธีเปิดใช้งานเส้นที่ซ่อนเมื่อส่งออก DWG เป็น PDF

เส้นที่ซ่อนจะถูกควบคุมผ่านการตั้งค่า layout ในตัวเลือกการเรสเตอร์ไลซ์ โดยการเลือก layout **Model** Aspose.CAD จะบอกตัวเรนเดอร์ให้ถือขอบที่ซ่อนเป็นไม่มองเห็น ทำให้คุณได้ภาพ 2‑D ที่สะอาดของโมเดล 3‑D.

## ทำไมต้องเปิดใช้งานเส้นที่ซ่อนเมื่อส่งออก?

เส้นที่ซ่อนช่วยให้การแสดงภาพโมเดล 3‑D ที่ซับซ้อนบนหน้า 2‑D ชัดเจนขึ้น โดยทำให้ขอบที่มองเห็นเท่านั้นที่ถูกเน้น ซึ่งช่วยเพิ่มความอ่านง่ายและมักจำเป็นสำหรับเอกสารวิศวกรรม.

## ข้อกำหนดเบื้องต้น

1. **Aspose.CAD for Java** – ดาวน์โหลดไลบรารีจากเว็บไซต์อย่างเป็นทางการ [ที่นี่](https://releases.aspose.com/cad/java/).  
2. **DWG files** – มีไฟล์ DWG ต้นฉบับที่จัดเก็บในไดเรกทอรีที่รู้จัก.  
3. **Java development environment** – JDK 8+ และ IDE ที่คุณชื่นชอบ (Eclipse, IntelliJ ฯลฯ).  

เมื่อคุณตั้งค่าเรียบร้อยแล้ว ให้เราลงลึกไปที่โค้ด.

## นำเข้าชื่อเนมสเปซ

เริ่มต้นโดยการนำเข้าคลาสที่จำเป็นเพื่อให้คุณสามารถทำงานกับภาพ CAD และตัวเลือก PDF.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import java.util.Arrays;
import java.util.List;
```

## ขั้นตอนที่ 1: ตั้งค่าโปรเจกต์ของคุณ

สร้างโปรเจกต์ Java และเพิ่มไฟล์ JAR ของ Aspose.CAD ไปยังเส้นทางการสร้างของคุณ จากนั้นกำหนดไดเรกทอรีที่เก็บไฟล์ DWG ของคุณ.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

> **เคล็ดลับ:** ใช้เส้นทางแบบเต็มหรือกำหนดเส้นทางแบบสัมพันธ์ตามโฟลเดอร์ resources ของโปรเจกต์ของคุณ.

## ขั้นตอนที่ 2: โหลดไฟล์ DWG

โหลดไฟล์ DWG ต้นฉบับเข้าสู่วัตถุ `CadImage` เพื่อให้คุณสามารถจัดการได้.

```java
String sourceFilePath = dataDir + "Bottom_plate.dwg";
String outPath = dataDir + "Bottom_plate.pdf";
CadImage cadImage = (CadImage)Image.load(sourceFilePath);
```

## ขั้นตอนที่ 3: กำหนดค่าตัวเลือกการเรสเตอร์ไลซ์

เลือกชั้นที่คุณต้องการรวมและตั้งค่าขนาดหน้าให้ตรงกับภาพวาดต้นฉบับ นี่คือจุดที่เราจะเปิดใช้งานการเรนเดอร์เส้นที่ซ่อนโดยระบุ layout.

```java
List<String> list = Arrays.asList("Print","L1_RegMark","L2_RegMark");
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageHeight(cadImage.getHeight());
rasterizationOptions.setPageWidth(cadImage.getWidth()) ;
rasterizationOptions.setLayers(list);
```

## ขั้นตอนที่ 4: ตั้งค่าตัวเลือก PDF

บอก Aspose.CAD ให้เรสเตอร์ไลซ์ข้อมูลเวกเตอร์เป็น PDF โดยใช้ layout “Model” เพื่อให้เส้นที่ซ่อนคงอยู่ในสภาพซ่อน.

```java
PdfOptions pdfOptions = new PdfOptions();
rasterizationOptions.setLayouts(new String[] { "Model" });
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## ขั้นตอนที่ 5: บันทึกผลลัพธ์

สุดท้าย ส่งออก DWG เป็นไฟล์ PDF เส้นที่ซ่อนจะถูกเคารพตาม layout ที่คุณตั้งค่า.

```java
cadImage.save(outPath, pdfOptions);
System.out.println("\nThe DWG file exported successfully to PDF.\nFile saved at " + dataDir);
```

> **ข้อผิดพลาดทั่วไป:** การลืมตั้งค่า layout เป็น `"Model"` จะทำให้ทุกเส้น (รวมถึงเส้นที่ซ่อน) ปรากฏเป็นเส้นทึบใน PDF.

## ปัญหาทั่วไปและวิธีแก้

| ปัญหา | สาเหตุ | วิธีแก้ |
|-------|--------|----------|
| PDF แสดงเส้นทั้งหมดเป็นเส้นทึบ | ไม่ได้ตั้งค่า layout เป็น **Model** | ตรวจสอบให้แน่ใจว่าได้เรียก `rasterizationOptions.setLayouts(new String[] { "Model" });` ก่อนบันทึก. |
| ไม่มีชั้นในผลลัพธ์ | ชื่อชั้นไม่ถูกต้อง | ตรวจสอบชื่อชั้นในไฟล์ DWG และให้ตรงกับใน `list` อย่างแม่นยำ. |
| ข้อผิดพลาด out‑of‑memory กับไฟล์ขนาดใหญ่ | ขนาดการเรสเตอร์ไลซ์ใหญ่เกินไป | ลดขนาดหน้าหรือประมวลผลภาพวาดเป็นส่วนย่อยหากเป็นไปได้. |

## คำถามที่พบบ่อย

### Q1: ฉันสามารถใช้ Aspose.CAD for Java กับรูปแบบไฟล์ CAD อื่นได้หรือไม่?
A1: ใช่, Aspose.CAD รองรับรูปแบบ CAD ต่าง ๆ เช่น DWG, DXF, DWF, และอื่น ๆ

### Q2: มีการทดลองใช้ฟรีสำหรับ Aspose.CAD for Java หรือไม่?
A2: ใช่, คุณสามารถหาการทดลองใช้ฟรีได้ [ที่นี่](https://releases.aspose.com/).

### Q3: ฉันจะรับการสนับสนุนสำหรับ Aspose.CAD for Java ได้อย่างไร?
A3: เยี่ยมชมฟอรั่ม Aspose.CAD [ที่นี่](https://forum.aspose.com/c/cad/19) เพื่อรับการสนับสนุนจากชุมชน.

### Q4: ฉันจะหาเอกสารรายละเอียดสำหรับ Aspose.CAD for Java ได้จากที่ไหน?
A4: ดูเอกสารรายละเอียดได้ [ที่นี่](https://reference.aspose.com/cad/java/).

### Q5: ฉันสามารถซื้อใบอนุญาตชั่วคราวสำหรับ Aspose.CAD for Java ได้หรือไม่?
A5: ใช่, คุณสามารถรับใบอนุญาตชั่วคราวได้ [ที่นี่](https://purchase.aspose.com/temporary-license/).

### Q6: วิธีนี้ทำงานได้กับการแปลง DWG เป็น PDF ในสภาพแวดล้อมเซิร์ฟเวอร์แบบไม่มี UI (headless) หรือไม่?
A6: แน่นอน. เนื่องจากโค้ดใช้เฉพาะ Aspose.CAD API จึงทำงานโดยไม่มีการพึ่งพา UI ใด ๆ ทำให้เหมาะสำหรับการทำงานอัตโนมัติบนเซิร์ฟเวอร์.

## สรุป

ตอนนี้คุณมีวิธีที่ครบถ้วนและพร้อมใช้งานในระดับการผลิตเพื่อ **export dwg to pdf** พร้อมการสนับสนุนเส้นที่ซ่อนโดยใช้ Aspose.CAD for Java วิธีนี้สามารถผสานรวมกับเครื่องมือประมวลผลแบบแบช, เว็บเซอร์วิส, หรือแอปพลิเคชันเดสก์ท็อปเพื่อทำการแปลง CAD‑to‑PDF อัตโนมัติได้.

---

**อัปเดตล่าสุด:** 2026-03-05  
**ทดสอบกับ:** Aspose.CAD for Java 24.12  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}