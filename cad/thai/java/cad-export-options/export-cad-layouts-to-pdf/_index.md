---
date: 2025-12-21
description: เรียนรู้วิธีการส่งออกเค้าโครง CAD เป็น PDF ด้วย Aspose.CAD for Java –
  วิธีที่รวดเร็วและเชื่อถือได้ในการสร้าง PDF จากไฟล์ CAD.
linktitle: Export CAD Layouts to PDF
second_title: Aspose.CAD Java API
title: วิธีส่งออกเลเอาต์ CAD เป็น PDF ด้วย Aspose.CAD สำหรับ Java
url: /th/java/cad-export-options/export-cad-layouts-to-pdf/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# วิธีการส่งออกเลย์เอาต์ CAD เป็น PDF ด้วย Aspose.CAD สำหรับ Java

## บทนำ

ในบทแนะนำนี้ เราจะแสดงให้คุณเห็น **วิธีการส่งออก CAD** เลย์เอาต์เป็น PDF ด้วย Aspose.CAD สำหรับ Java ไม่ว่าคุณจะทำงานกับ DWG, DXF หรือรูปแบบ CAD อื่น ๆ คู่มือนี้จะพาคุณผ่านขั้นตอนแบบโปรแกรมที่สะอาดและเชื่อถือได้เพื่อสร้าง PDF จากไฟล์ CAD อย่างรวดเร็ว

## คำตอบอย่างรวดเร็ว
- **ห้องสมุดทำอะไร?** มันแปลงภาพวาด CAD (DWG, DXF, DWF ฯลฯ) เป็น PDF, รูปภาพเรสเตอร์, และรูปแบบอื่น ๆ.  
- **ใช้ภาษาอะไร?** Java – โค้ดทำงานบนแพลตฟอร์มที่เข้ากันได้กับ JVM ใด ๆ  
- **ต้องการไลเซนส์หรือไม่?** มีการทดลองใช้ฟรี; จำเป็นต้องมีไลเซนส์เชิงพาณิชย์สำหรับการใช้งานจริง.  
- **ฉันสามารถแปลง DWG เป็น PDF ใน Java ได้หรือไม่?** ได้ – API เดียวกันสนับสนุนการแปลง **dwg to pdf java**.  
- **ขั้นตอนหลักคืออะไร?** โหลดไฟล์ CAD, ตั้งค่าตัวเลือกการเรสเตอร์ไลซ์, กำหนดค่าตัวเลือก PDF, และบันทึกผลลัพธ์.

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะดำเนินการสู่บทแนะนำ โปรดตรวจสอบว่าคุณมีข้อกำหนดต่อไปนี้พร้อมใช้งานแล้ว:

- Aspose.CAD for Java: ตรวจสอบว่าคุณได้ติดตั้งไลบรารีแล้ว คุณสามารถดาวน์โหลดได้จากเว็บไซต์ Aspose [ที่นี่](https://releases.aspose.com/cad/java/).
- สภาพแวดล้อมการพัฒนา Java: ตรวจสอบว่าคุณได้ตั้งค่าสภาพแวดล้อมการพัฒนา Java บนเครื่องของคุณแล้ว.

ตอนนี้คุณได้ตั้งค่าทุกอย่างเรียบร้อยแล้ว มาเริ่มต้นบทแนะนำกันเถอะ

## “วิธีการส่งออก CAD” คืออะไร?

การส่งออก CAD หมายถึงการแปลงข้อมูลการวาด CAD ดั้งเดิม (เช่น DWG, DXF หรือ DWF) ให้เป็นรูปแบบที่อ่านได้ทั่วไปมากขึ้นเช่น PDF กระบวนการนี้สำคัญสำหรับการแชร์การออกแบบกับผู้มีส่วนได้ส่วนเสียที่อาจไม่มีซอฟต์แวร์ CAD ติดตั้งอยู่

## ทำไมต้องใช้ Aspose.CAD สำหรับ Java เพื่อส่งออก CAD เป็น PDF?

- **ความแม่นยำสูง** – กราฟิกเวกเตอร์จะถูกเก็บรักษาไว้ และตัวเลือกการเรสเตอร์ไลซ์ช่วยให้คุณปรับคุณภาพได้ละเอียด.  
- **ไม่มีการพึ่งพาภายนอก** – เป็น Java แท้ ๆ ไม่ต้องใช้ DLL หรือคอมโพเนนต์ COM.  
- **รองรับหลายรูปแบบ** – คุณยังสามารถ **generate pdf from cad** ไฟล์ที่สร้างจาก DWG, DWF หรือรูปแบบอื่น ๆ.  
- **ขยายได้สำหรับงานแบบแบตช์** – เหมาะสำหรับการทำงานอัตโนมัติบนเซิร์ฟเวอร์, CI pipelines, หรือยูทิลิตี้บนเดสก์ท็อป.

## นำเข้า Namespaces

ในโค้ด Java ของคุณ ให้เริ่มต้นด้วยการนำเข้า Namespaces ที่จำเป็น การนำเข้าต่าง ๆ นี้จะให้คุณเข้าถึงคลาสและเมธอดที่ต้องใช้สำหรับทำงานกับ Aspose.CAD สำหรับ Java

```java
import com.aspose.cad.Image;
import com.aspose.cad.InterpolationMode;
import com.aspose.cad.SmoothingMode;
import com.aspose.cad.TextRenderingHint;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
//import com.aspose.cad.imageoptions.TypeOfEntities;
```

## ขั้นตอนที่ 1: โหลดไฟล์ CAD

เริ่มต้นด้วยการโหลดไฟล์ CAD เข้าไปในแอปพลิเคชัน Java ของคุณโดยใช้เมธอด `Image.load` แทนที่ `"conic_pyramid.dxf"` ด้วยพาธของไฟล์ CAD ของคุณ

```java
String dataDir = "Your Document Directory" + "ExportingCAD/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image cadImage = Image.load(srcFile);
```

## ขั้นตอนที่ 2: ตั้งค่าตัวเลือกการเรสเตอร์ไลซ์

สร้างอินสแตนซ์ของ `CadRasterizationOptions` เพื่อกำหนดว่าควรเรสเตอร์ไลซ์เอนทิตี้ของ CAD อย่างไร ปรับพารามิเตอร์เช่น ความกว้างของหน้า, ความสูงของหน้า, และสเกลเลย์เอาต์ตามความต้องการของคุณ

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
rasterizationOptions.setAutomaticLayoutsScaling(true);
rasterizationOptions.setNoScaling(false);
rasterizationOptions.setContentAsBitmap(true);
rasterizationOptions.setLayouts(new String[]{"Model"});
```

## ขั้นตอนที่ 3: ตั้งค่าตัวเลือก PDF

สร้างอินสแตนซ์ของ `PdfOptions` และเชื่อมโยงกับตัวเลือกการเรสเตอร์ไลซ์ นอกจากนี้ยังตั้งค่าตัวเลือกกราฟิกสำหรับการส่งออก PDF เช่น โหมดการทำให้เรียบ, คำแนะนำการเรนเดอร์ข้อความ, และโหมดการแทรกสอด

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
rasterizationOptions.getGraphicsOptions().setSmoothingMode(SmoothingMode.HighQuality);
rasterizationOptions.getGraphicsOptions().setTextRenderingHint(TextRenderingHint.AntiAliasGridFit);
rasterizationOptions.getGraphicsOptions().setInterpolationMode(InterpolationMode.HighQualityBicubic);
```

## ขั้นตอนที่ 4: ส่งออกเป็น PDF

สุดท้าย ให้ส่งออกเลย์เอาต์ CAD เป็นไฟล์ PDF โดยใช้เมธอด `save` ของอ็อบเจ็กต์ `cadImage`

```java
cadImage.save(dataDir + "CADLayoutsToPDF_out_.pdf", pdfOptions);
```

## ปัญหาและวิธีแก้ไขทั่วไป

| ปัญหา | สาเหตุ | วิธีแก้ |
|-------|--------|-----|
| **ผลลัพธ์ PDF ว่าง** | ตัวเลือกการเรสเตอร์ไลซ์ตั้งค่าไม่ถูกต้อง (เช่น ชื่อเลย์เอาต์ไม่ตรงกัน) | ตรวจสอบว่า `rasterizationOptions.setLayouts()` ตรงกับชื่อเลย์เอาต์ในไฟล์ CAD ของคุณ. |
| **ภาพความละเอียดต่ำ** | `PageWidth`/`PageHeight` เล็กเกินไป | เพิ่มขนาดหน้าหรือกำหนด DPI สูงขึ้นโดยใช้ `rasterizationOptions.setResolution()`. |
| **เวอร์ชัน CAD ไม่รองรับ** | เวอร์ชัน DWG/DXF เก่าอาจต้องการเวอร์ชัน Aspose.CAD ที่ใหม่กว่า | ดาวน์โหลดเวอร์ชันไลบรารีล่าสุดจากเว็บไซต์ Aspose. |

## คำถามที่พบบ่อย

### Q1: ฉันสามารถใช้ Aspose.CAD สำหรับ Java กับรูปแบบไฟล์ CAD อื่น ๆ ได้หรือไม่?

A1: ใช่, Aspose.CAD รองรับรูปแบบ CAD ต่าง ๆ รวมถึง DWG, DXF, DWF, และอื่น ๆ ตรวจสอบเอกสาร [ที่นี่](https://reference.aspose.com/cad/java/) เพื่อดูรายการเต็ม

### Q2: มีการทดลองใช้ฟรีสำหรับ Aspose.CAD สำหรับ Java หรือไม่?

A2: ใช่, คุณสามารถสำรวจคุณสมบัติของ Aspose.CAD ด้วยการทดลองใช้ฟรี [ที่นี่](https://releases.aspose.com/)

### Q3: ฉันจะรับการสนับสนุนสำหรับ Aspose.CAD สำหรับ Java ได้อย่างไร?

A3: เยี่ยมชมฟอรั่ม Aspose.CAD [ที่นี่](https://forum.aspose.com/c/cad/19) เพื่อรับการสนับสนุนจากชุมชน สำหรับการสนับสนุนระดับพรีเมี่ยม พิจารณาซื้อไลเซนส์ [ที่นี่](https://purchase.aspose.com/buy)

### Q4: ความแตกต่างระหว่างการสเกลเลย์เอาต์อัตโนมัติและแบบแมนนวลคืออะไร?

A4: การสเกลเลย์เอาต์อัตโนมัติจะปรับขนาดเลย์เอาต์ตามมิติหน้าที่ระบุไว้ ส่วนการสเกลแบบแมนนวลให้คุณตั้งค่าค่าการสเกลที่กำหนดเองได้

### Q5: ฉันสามารถปรับแต่งลักษณะของไฟล์ PDF ที่ส่งออกได้หรือไม่?

A5: ใช่, คุณสามารถปรับแต่งตัวเลือกกราฟิกในโค้ดเพื่อควบคุมคุณภาพและลักษณะของ PDF ที่ส่งออก

### Q6: Aspose.CAD รองรับการแปลง **dwg to pdf java** โดยตรงหรือไม่?

A6: แน่นอน. ตัวเลือกการเรสเตอร์ไลซ์และ PDF เดียวกันทำงานกับไฟล์ DWG ทำให้การแปลง **dwg to pdf java** ราบรื่น

### Q7: มีวิธีการ **generate pdf from cad** โดยไม่ต้องเรสเตอร์ไลซ์เป็นบิตแมพหรือไม่?

A7: โดยการตั้งค่า `rasterizationOptions.setContentAsBitmap(false)` คุณสามารถเก็บข้อมูลเวกเตอร์ไว้เมื่อเป็นไปได้ ทำให้ได้ PDF ที่เป็นเวกเตอร์แท้จริง

**อัปเดตล่าสุด:** 2025-12-21  
**ทดสอบด้วย:** Aspose.CAD for Java 24.10  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}