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

## Introduction

ในบทเรียนนี้คุณจะได้เรียนรู้วิธี **ส่งออก DWG เป็น PDF** พร้อมคงเส้นที่ซ่อนอยู่โดยใช้ Aspose.CAD สำหรับ Java ไม่ว่าคุณจะต้องการ **แปลง DWG เป็น PDF**, สร้างคู่มือสไตล์ **dwg to pdf tutorial**, หรือเพียงแค่ **บันทึก DWG เป็น PDF** พร้อมการสนับสนุนเส้นที่ซ่อนอยู่ เราจะพาคุณผ่านทุกขั้นตอนจนจบ เมื่อเสร็จแล้วคุณจะมีโซลูชันพร้อมใช้งานที่สามารถใส่ลงในโปรเจกต์ Java ใดก็ได้

## Quick Answers
- **What does this tutorial cover?** การเปิดใช้งานการเรนเดอร์เส้นที่ซ่อนอยู่ขณะส่งออก DWG เป็น PDF ด้วย Aspose.CAD สำหรับ Java.  
- **Which primary operation is performed?** `export dwg as pdf`.  
- **Do I need a license?** ทดลองใช้ฟรีได้สำหรับการทดสอบ; ต้องมีลิขสิทธิ์เชิงพาณิชย์สำหรับการใช้งานจริง.  
- **What are the prerequisites?** สภาพแวดล้อมการพัฒนา Java, ไลบรารี Aspose.CAD สำหรับ Java, และไฟล์ DWG.  
- **How long does implementation take?** ประมาณ 10‑15 นาทีสำหรับการตั้งค่าเบื้องต้น.

## What is “export dwg as pdf”?
การส่งออกไฟล์ DWG ไปเป็น PDF จะทำการแปลงภาพวาด CAD ที่เป็นเวกเตอร์ให้เป็นรูปแบบเอกสารพกพา (PDF) พร้อมคงเลเยอร์, ประเภทเส้น, และการเรนเดอร์เส้นที่ซ่อนอยู่ (ถ้ามี) ทำให้สามารถแชร์การออกแบบ CAD ให้กับผู้มีส่วนได้ส่วนเสียที่อาจไม่มีซอฟต์แวร์ CAD ได้อย่างง่ายดาย

## Why enable hidden lines when exporting?
เส้นที่ซ่อนอยู่ช่วยให้การแสดงผลโมเดล 3 มิติที่ซับซ้อนบนหน้า 2 มิติชัดเจนยิ่งขึ้น โดยเน้นเฉพาะขอบที่มองเห็นได้เท่านั้น ซึ่งทำให้เอกสารอ่านง่ายขึ้นและมักเป็นข้อกำหนดสำหรับเอกสารวิศวกรรม

## Prerequisites

1. **Aspose.CAD for Java** – ดาวน์โหลดไลบรารีจากเว็บไซต์อย่างเป็นทางการ [here](https://releases.aspose.com/cad/java/).  
2. **DWG files** – มีไฟล์ DWG ต้นฉบับจัดเก็บในโฟลเดอร์ที่ทราบตำแหน่ง.  
3. **Java development environment** – JDK 8+ และ IDE ที่คุณชอบ (Eclipse, IntelliJ ฯลฯ).  

เมื่อเตรียมพร้อมแล้ว ไปที่ขั้นตอนโค้ดกันต่อ

## Import Namespaces

เริ่มต้นด้วยการนำเข้าคลาสที่จำเป็นเพื่อทำงานกับภาพ CAD และตัวเลือก PDF

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import java.util.Arrays;
import java.util.List;
```

## Step 1: Set Up Your Project

สร้างโปรเจกต์ Java แล้วเพิ่มไฟล์ JAR ของ Aspose.CAD ไปยัง build path จากนั้นกำหนดไดเรกทอรีที่เก็บไฟล์ DWG ของคุณ

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

> **Pro tip:** ใช้เส้นทางแบบ absolute หรือกำหนดเส้นทางแบบ relative ตามโฟลเดอร์ resources ของโปรเจกต์

## Step 2: Load DWG File

โหลดไฟล์ DWG ต้นฉบับเข้าไปในอ็อบเจกต์ `CadImage` เพื่อให้สามารถจัดการได้

```java
String sourceFilePath = dataDir + "Bottom_plate.dwg";
String outPath = dataDir + "Bottom_plate.pdf";
CadImage cadImage = (CadImage)Image.load(sourceFilePath);
```

## Step 3: Configure Rasterization Options

เลือกเลเยอร์ที่ต้องการรวมและตั้งค่าขนาดหน้าให้ตรงกับภาพวาดต้นฉบับ ที่นี่เราจะเปิดใช้งานการเรนเดอร์เส้นที่ซ่อนอยู่โดยระบุ layout

```java
List<String> list = Arrays.asList("Print","L1_RegMark","L2_RegMark");
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageHeight(cadImage.getHeight());
rasterizationOptions.setPageWidth(cadImage.getWidth()) ;
rasterizationOptions.setLayers(list);
```

## Step 4: Set PDF Options

บอก Aspose.CAD ให้แปลงข้อมูลเวกเตอร์เป็น PDF โดยใช้ layout “Model” เพื่อให้เส้นที่ซ่อนอยู่ถูกซ่อนไว้

```java
PdfOptions pdfOptions = new PdfOptions();
rasterizationOptions.setLayouts(new String[] { "Model" });
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## Step 5: Save the Result

สุดท้าย ส่งออก DWG เป็นไฟล์ PDF เส้นที่ซ่อนอยู่จะได้รับการเคารพตาม layout ที่ตั้งค่าไว้

```java
cadImage.save(outPath, pdfOptions);
System.out.println("\nThe DWG file exported successfully to PDF.\nFile saved at " + dataDir);
```

> **Common Pitfall:** หากลืมตั้งค่า layout เป็น `"Model"` จะทำให้เส้นทั้งหมด (รวมถึงเส้นที่ซ่อนอยู่) ปรากฏเป็นเส้นทึบใน PDF

## Conclusion

คุณมีวิธีการที่สมบูรณ์และพร้อมใช้งานในระดับผลิตเพื่อ **ส่งออก DWG เป็น PDF** พร้อมการสนับสนุนเส้นที่ซ่อนอยู่โดยใช้ Aspose.CAD สำหรับ Java วิธีนี้สามารถนำไปผสานกับเครื่องมือประมวลผลแบบแบตช์, เว็บเซอร์วิส, หรือแอปพลิเคชันเดสก์ท็อปเพื่อทำการแปลง CAD‑to‑PDF อัตโนมัติได้

## Frequently Asked Questions

### Q1: Can I use Aspose.CAD for Java with other CAD file formats?
A1: Yes, Aspose.CAD supports various CAD formats such as DWG, DXF, DWF, and more.

### Q2: Is there a free trial available for Aspose.CAD for Java?
A2: Yes, you can find the free trial [here](https://releases.aspose.com/).

### Q3: How do I get support for Aspose.CAD for Java?
A3: Visit the Aspose.CAD forum [here](https://forum.aspose.com/c/cad/19) for community support.

### Q4: Where can I find detailed documentation for Aspose.CAD for Java?
A4: Refer to the documentation [here](https://reference.aspose.com/cad/java/).

### Q5: Can I purchase a temporary license for Aspose.CAD for Java?
A5: Yes, you can obtain a temporary license [here](https://purchase.aspose.com/temporary-license/).

### Q6: Does this method also work for converting DWG to PDF in a headless server environment?
A6: Absolutely. Since the code uses only the Aspose.CAD API, it runs without any UI dependencies, making it ideal for server‑side automation.

---

**Last Updated:** 2026-01-02  
**Tested With:** Aspose.CAD for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}