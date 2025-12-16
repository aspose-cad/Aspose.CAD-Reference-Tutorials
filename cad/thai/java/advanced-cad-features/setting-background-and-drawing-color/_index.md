---
date: 2025-12-12
description: เรียนรู้วิธีตั้งค่าสีพื้นหลังใน Java ด้วย Aspose.CAD for Java ขณะแปลง
  CAD เป็น PDF และ TIFF ปรับแต่งสีการวาดเพื่อผลลัพธ์ระดับมืออาชีพ.
linktitle: Setting Background and Drawing Color
second_title: Aspose.CAD Java API
title: ตั้งค่าสีพื้นหลังใน Java ด้วย Aspose.CAD สำหรับ Java
url: /th/java/advanced-cad-features/setting-background-and-drawing-color/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# ตั้งค่าสีพื้นหลัง java ด้วย Aspose.CAD for Java

## Introduction

ในกระบวนการทำงาน CAD สมัยใหม่ การสามารถ **set background color java** ระหว่างการแปลงเป็นสิ่งสำคัญสำหรับการสร้างเอกสารที่ชัดเจนและพร้อมนำเสนอ Aspose.CAD for Java ทำให้การแปลงไฟล์ CAD เป็น PDF หรือ TIFF เป็นเรื่องง่าย พร้อมให้คุณควบคุมสีพื้นหลังและสีการวาดได้เต็มที่ ในบทแนะนำนี้เราจะเดินผ่านกระบวนการทั้งหมด—from การโหลดไฟล์ DXF ไปจนถึงการส่งออกไฟล์ PDF และ TIFF ด้วยสีที่คุณเลือก.

## Quick Answers
- **ไลบรารีใดที่จัดการการแปลง CAD ใน Java?** Aspose.CAD for Java.
- **ฉันสามารถเปลี่ยนสีพื้นหลังระหว่างการแปลงได้หรือไม่?** ใช่, โดยใช้ `CadRasterizationOptions.setBackgroundColor`.
- **รูปแบบผลลัพธ์ที่รองรับคืออะไร?** PDF และ TIFF (ทั้งสองเป็นแบบเรสเตอร์).
- **ต้องการไลเซนส์สำหรับการใช้งานในผลิตภัณฑ์หรือไม่?** จำเป็นต้องมีไลเซนส์เชิงพาณิชย์; มีการทดลองใช้ฟรี.
- **การแปลงแบบจำนวนมากได้รับการสนับสนุนหรือไม่?** แน่นอน—ประมวลผลหลายไฟล์ในลูปด้วยการตั้งค่าเดียวกัน.

## What is “set background color java” in the context of CAD conversion?

การตั้งค่าสีพื้นหลังใน Java หมายถึงการกำหนดค่าตัวเลือกการเรสเตอร์ไลซ์เพื่อให้ภาพที่เรนเดอร์ (PDF หรือ TIFF) ใช้สีที่คุณระบุแทนพื้นหลังสีขาวเริ่มต้น ซึ่งช่วยเพิ่มความคอนทราสต์โดยเฉพาะเมื่อภาพ CAD มีเส้นสีอ่อน.

## Why use Aspose.CAD for Java to convert CAD to PDF or TIFF?

- **ความแม่นยำสูง** – รักษาน้ำหนักเส้น, ชั้น, และสี.
- **ไม่มีการพึ่งพาภายนอก** – Java แท้, ไม่มีไลบรารีเนทีฟ.
- **การเรนเดอร์ที่ยืดหยุ่น** – ควบคุมขนาดหน้า, DPI, สีพื้นหลัง, และสีการวาด.
- **การประมวลผลเป็นชุด** – เหมาะสำหรับสายงานอัตโนมัติ.

## Prerequisites

- **Aspose.CAD for Java Library** – ดาวน์โหลดได้จาก [here](https://releases.aspose.com/cad/java/).
- **โฟลเดอร์สำหรับไฟล์ CAD ของคุณ** – แทนที่ `"Your Document Directory" + "CADConversion/"` ด้วยเส้นทางจริงบนเครื่องของคุณ.

## Import Namespaces

First, import the classes you’ll need. These imports give you access to color handling, rasterization options, and the output formats.

```java
import java.awt.Color;
import java.awt.Image;

import com.aspose.cad.fileformats.cad.CadDrawTypeMode;
import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

## Step‑by‑Step Guide

### Step 1: Load the CAD file

We load the source DXF (or any supported CAD format) into an `Image` object.

```java
String dataDir = "Your Document Directory" + "CADConversion/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image objImage = Image.load(srcFile);
```

### Step 2: Configure background and drawing color

Here we set the page dimensions, choose a background color, and tell the renderer to use a specific drawing color instead of the original CAD colors.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
rasterizationOptions.setBackgroundColor(com.aspose.cad.Color.getBeige());   // example background
rasterizationOptions.setDrawType(CadDrawTypeMode.UseDrawColor);
rasterizationOptions.setBackgroundColor(com.aspose.cad.Color.getBlue());   // overwrite with blue if needed
```

> **เคล็ดลับ:** ทดลองใช้ `CadDrawTypeMode.UseOriginalColors` หากคุณต้องการรักษาสีดั้งเดิมของ CAD ไว้ขณะยังคงใช้พื้นหลังที่กำหนดเอง.

### Step 3: Create PDF and save

We bind the rasterization options to `PdfOptions` and save the result as a PDF file.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
objImage.save(dataDir + "result_out_.pdf", pdfOptions);
```

### Step 4: Create TIFF and save

The same rasterization settings can be reused for TIFF output.

```java
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.setVectorRasterizationOptions(rasterizationOptions);
objImage.save(dataDir + "result_out_.tiff", tiffOptions);
```

## Common Issues & Solutions

| ปัญหา | วิธีแก้ |
|-------|----------|
| **สีพื้นหลังไม่เปลี่ยน** | ตรวจสอบให้แน่ใจว่าคุณเรียก `setBackgroundColor` *หลังจาก* ตั้งค่า draw type. การเรียกครั้งที่สองจะเขียนทับการเรียกครั้งแรก, ดังนั้นให้ตั้งค่าสีที่ต้องการเป็นการเรียกสุด. |
| **ผลลัพธ์เบลอ** | เพิ่ม `PageWidth`/`PageHeight` หรือกำหนด DPI ที่สูงขึ้นผ่าน `rasterizationOptions.setResolution(...)`. |
| **ข้อยกเว้นไฟล์ไม่พบ** | ตรวจสอบว่าเส้นทาง `dataDir` ลงท้ายด้วยตัวคั่น (`/` หรือ `\\`) และไฟล์นั้นมีอยู่จริง. |

## Frequently Asked Questions

**ถาม: Aspose.CAD for Java เหมาะสำหรับการแปลงเป็นจำนวนมากหรือไม่?**  
ตอบ: แน่นอน คุณสามารถใส่โค้ดในลูปและประมวลผลหลายสิบไฟล์ด้วยการตั้งค่าเรสเตอร์ไลซ์เดียวกัน.

**ถาม: ฉันสามารถปรับแต่งสีพื้นหลังในไฟล์ที่สร้างขึ้นได้หรือไม่?**  
ตอบ: ได้ บทแนะนำนี้แสดงวิธีตั้งค่า `com.aspose.cad.Color` ใดก็ได้ที่คุณต้องการสำหรับทั้ง PDF และ TIFF.

**ถาม: ฉันจะหาเอกสารอธิบายอย่างละเอียดสำหรับ Aspose.CAD for Java ได้จากที่ไหน?**  
ตอบ: ดูที่ [documentation](https://reference.aspose.com/cad/java/) เพื่อรายละเอียดเชิงลึกและตัวอย่างเพิ่มเติม.

**ถาม: มีการทดลองใช้ฟรีหรือไม่?**  
ตอบ: มี, ทดลองใช้คุณสมบัติต่าง ๆ ด้วย [free trial](https://releases.aspose.com/).

**ถาม: ฉันจะขอรับการสนับสนุนสำหรับ Aspose.CAD for Java ได้อย่างไร?**  
ตอบ: เยี่ยมชม [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) เพื่อถามคำถามและแบ่งปันประสบการณ์กับชุมชน.

---

**อัปเดตล่าสุด:** 2025-12-12  
**ทดสอบด้วย:** Aspose.CAD for Java 24.11  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}