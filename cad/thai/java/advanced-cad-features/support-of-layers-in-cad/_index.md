---
date: 2025-12-13
description: เรียนรู้วิธีบันทึกไฟล์ CAD เป็น JPEG ใน Java ด้วย Aspose.CAD, เพิ่มหลายเลเยอร์,
  และปรับขนาด CAD เพื่อการแปลงภาพที่แม่นยำ.
linktitle: Support of Layers in CAD
second_title: Aspose.CAD Java API
title: บันทึก CAD เป็น JPEG พร้อมการสนับสนุนเลเยอร์ใน Java
url: /th/java/advanced-cad-features/support-of-layers-in-cad/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# บันทึก CAD เป็น JPEG พร้อมการสนับสนุนเลเยอร์ใน Java

## Introduction

ในบทแนะนำนี้คุณจะได้ค้นพบวิธี **บันทึก CAD เป็น JPEG** พร้อมใช้ประโยชน์จากการสนับสนุนเลเยอร์ใน Aspose.CAD for Java. เลเยอร์ช่วยให้คุณแยกส่วนเฉพาะของภาพวาด ทำให้การส่งออกเฉพาะสิ่งที่ต้องการเป็นเรื่องง่าย เราจะเดินผ่านแต่ละขั้นตอน ตั้งแต่การตั้งค่าสภาพแวดล้อมจนถึงการส่งออก JPEG ที่รวมเฉพาะเลเยอร์ที่คุณเลือก.

## Quick Answers
- **การบันทึก CAD เป็น JPEG หมายถึงอะไร?** มันแปลงภาพวาด CAD เป็นภาพ JPEG แบบแรสเตอร์.  
- **ฉันสามารถรวมเฉพาะเลเยอร์ที่เลือกได้หรือไม่?** ได้ – ใช้เมธอด `setLayers` เพื่อระบุว่าเลเยอร์ใดจะเรนเดอร์.  
- **ฉันจะเปลี่ยนขนาดภาพได้อย่างไร?** ปรับ `setPageWidth` และ `setPageHeight` ใน `CadRasterizationOptions`.  
- **นี่เป็นโซลูชันเฉพาะ Java หรือไม่?** ตัวอย่างใช้ Aspose.CAD for Java แต่แนวคิดเดียวกันสามารถใช้กับภาษาอื่นได้.  
- **ฉันต้องการไลเซนส์หรือไม่?** การทดลองใช้ฟรีทำงานสำหรับการทดสอบ; จำเป็นต้องมีไลเซนส์เชิงพาณิชย์สำหรับการใช้งานจริง.

## Prerequisites

ก่อนเริ่มทำงาน โปรดตรวจสอบว่าคุณมีสิ่งต่อไปนี้:

1. **Aspose.CAD for Java Library** – ดาวน์โหลดจาก [website](https://releases.aspose.com/cad/java/). ทำตามคู่มือการติดตั้งเพื่อเพิ่มไฟล์ JAR ไปยัง classpath ของโปรเจกต์ของคุณ.  
2. **Java Development Environment** – JDK รุ่นล่าสุด (8 หรือใหม่กว่า) ที่ติดตั้งบนเครื่องของคุณ.

เมื่อเราตั้งค่าเรียบร้อยแล้ว มาดูโค้ดที่จำเป็นสำหรับ **บันทึก CAD เป็น JPEG** พร้อมการเรนเดอร์เลเยอร์แบบเลือก.

## Import Namespaces

นำเข้าชื่อเนมสเปซที่จำเป็น:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
import java.util.ArrayList;
import java.util.Arrays;
import java.util.List;
```

## Step‑by‑Step Guide

### Step 1: Set Up File Paths

กำหนดตำแหน่งไฟล์ต้นทาง DWF และตำแหน่งไฟล์ JPEG ที่จะเขียนออก:

```java
String dataDir = "Your Document Directory" + "DWFDrawings/";
String srcFile = dataDir + "for_layers_test.dwf";
String outFile = dataDir + "for_layers_test.jpg";
```

### Step 2: Load the DWF Image

โหลดภาพ DWF:

```java
Image image = Image.load(srcFile);
```

### Step 3: Configure Rasterization Options (Adjust CAD Dimensions)

กำหนดค่าตัวเลือกการเรซอร์ไรซ์ (ปรับขนาด CAD):

สร้างอินสแตนซ์ `CadRasterizationOptions` และตั้งค่าขนาดเอาต์พุตที่ต้องการ การเปลี่ยนค่าเหล่านี้ทำให้คุณ **ปรับขนาด CAD** สำหรับ JPEG สุดท้าย.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
```

### Step 4: Specify Layers (Add Multiple Layers)

ระบุเลเยอร์ (เพิ่มหลายเลเยอร์):

หากต้องการเรนเดอร์มากกว่าหนึ่งเลเยอร์ เพียงเพิ่มชื่อของพวกมันลงในรายการ ที่นี่เราจะเริ่มด้วยเลเยอร์เดียวชื่อ “LayerA”.

```java
List<String> stringList = new ArrayList<>(Arrays.asList("LayerA"));
rasterizationOptions.setLayers(stringList);
```

*เคล็ดลับ:* เพื่อ **เพิ่มหลายเลเยอร์**, ขยายการเรียก `Arrays.asList` เช่น `Arrays.asList("LayerA", "LayerB", "LayerC")`.

### Step 5: Configure JPEG Options (Java Convert CAD Image)

กำหนดค่าตัวเลือก JPEG (Java แปลงภาพ CAD):

เชื่อมการตั้งค่าเรซอร์ไรซ์กับรูปแบบเอาต์พุต JPEG.

```java
JpegOptions jpegOptions = new JpegOptions();
jpegOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### Step 6: Export to JPG (Save CAD as JPEG)

ส่งออกเป็น JPG (บันทึก CAD เป็น JPEG):

สุดท้าย เขียนภาพลงดิสก์ ขั้นตอนนี้ **บันทึกภาพวาด CAD เป็นไฟล์ JPEG** ที่มีเฉพาะเลเยอร์ที่เลือก.

```java
image.save(outFile, jpegOptions);
```

โดยทำตามขั้นตอนเหล่านี้ คุณได้ **บันทึก CAD เป็น JPEG** อย่างสำเร็จ พร้อมการควบคุมว่าเลเยอร์ใดปรากฏและการปรับขนาดภาพตามต้องการ.

## Common Issues and Solutions

| ปัญหา | วิธีแก้ |
|-------|----------|
| **เลเยอร์ไม่ปรากฏ** | ตรวจสอบว่าชื่อเลเยอร์ตรงกับที่เก็บในไฟล์ DWF อย่างแม่นยำ (แยกแยะตัวพิมพ์ใหญ่‑เล็ก). |
| **ภาพเอาต์พุตเป็นสีขาว** | ตรวจสอบให้แน่ใจว่า `setPageWidth` และ `setPageHeight` มีขนาดเพียงพอสำหรับขอบเขตของภาพวาด. |
| **ข้อยกเว้นไลเซนส์** | ใช้ไลเซนส์ทดลองสำหรับการทดสอบ; รับไลเซนส์เต็มสำหรับสภาพแวดล้อมการผลิต. |

## Frequently Asked Questions

**ถาม: ฉันสามารถเพิ่มหลายเลเยอร์ไปยังตัวเลือกการเรซอร์ไรซ์ได้หรือไม่?**  
ตอบ: แน่นอน. ขยาย `stringList` ด้วยชื่อเลเยอร์เพิ่มเติม เช่น `Arrays.asList("LayerA", "LayerB")`.

**ถาม: Aspose.CAD รองรับรูปแบบ CAD อื่น ๆ หรือไม่?**  
ตอบ: ใช่, รองรับ DWG, DXF, DWF และรูปแบบอื่น ๆ อีกมากมาย.

**ถาม: ฉันจะเปลี่ยนขนาดภาพเอาต์พุตได้อย่างไร?**  
ตอบ: ปรับ `setPageWidth` และ `setPageHeight` ในอินสแตนซ์ `CadRasterizationOptions`.

**ถาม: ฉันสามารถซื้อไลเซนส์สำหรับ Aspose.CAD ได้จากที่ไหน?**  
ตอบ: คุณสามารถสำรวจตัวเลือกการไลเซนส์ได้ [ที่นี่](https://purchase.aspose.com/buy).

**ถาม: ฉันจะรับการสนับสนุนจากชุมชนได้จากที่ไหน?**  
ตอบ: เข้าร่วมชุมชน Aspose.CAD ใน [ฟอรั่ม](https://forum.aspose.com/c/cad/19) เพื่อขอความช่วยเหลือและสนทนา.

**Last Updated:** 2025-12-13  
**Tested With:** Aspose.CAD for Java 24.11  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}