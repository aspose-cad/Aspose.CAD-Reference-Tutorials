---
date: 2026-01-10
description: เรียนรู้วิธีสร้างไฟล์ JPEG จากไฟล์ DGN ด้วย Aspose.CAD for Java บทเรียนแบบขั้นตอนนี้จะแสดงให้คุณเห็นวิธีแปลง
  DGN เป็น JPEG อย่างมีประสิทธิภาพ
linktitle: Exporting DGN in AutoCAD Format to Raster Image Format
second_title: Aspose.CAD Java API
title: วิธีสร้าง JPEG จาก DGN ด้วย Aspose.CAD สำหรับ Java
url: /th/java/dgn-export-options/exporting-dgn-to-raster-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# สร้าง JPEG จาก DGN ด้วย Aspose.CAD สำหรับ Java

## Introduction

ในคู่มือฉบับครอบคลุมนี้ คุณจะ **สร้าง JPEG จาก DGN** ด้วยเพียงไม่กี่บรรทัดของโค้ด Java ไม่ว่าคุณจะกำลังสร้างเครื่องมือแปลงแบบแบตช์หรือจำเป็นต้องแสดงภาพวาด CAD เป็นภาพที่เป็นมิตรต่อเว็บ การแปลง DGN เป็น JPEG เป็นความต้องการทั่วไปสำหรับหลายกระบวนการวิศวกรรมและการออกแบบ เราจะเดินผ่านทุกขั้นตอน—from ตั้งค่าไลบรารี Aspose.CAD ไปจนถึงการบันทึกภาพเรสเตอร์สุดท้าย—เพื่อให้คุณสามารถรวมโซลูชันนี้เข้ากับแอปพลิเคชันของคุณได้ทันที

## Quick Answers
- **What library is needed?** Aspose.CAD for Java  
- **Can I convert other CAD formats to JPEG?** ใช่, Aspose.CAD รองรับหลายรูปแบบ (ดูคีย์เวิร์ดรอง *convert cad to jpeg*)  
- **Do I need a license for production?** จำเป็นต้องมีใบอนุญาตเชิงพาณิชย์สำหรับการใช้งานที่ไม่ใช่แบบทดลอง  
- **What Java version is supported?** Java 8 หรือใหม่กว่า  
- **How long does a typical conversion take?** ปกติใช้เวลาน้อยกว่าวินาทีสำหรับภาพวาดขนาดมาตรฐาน  

## What is “create JPEG from DGN”?
การสร้าง JPEG จากไฟล์ DGN หมายถึงการเรสเตอร์ไอภาพวาด DGN ที่เป็นเวกเตอร์ให้เป็นภาพแบบพิกเซล (JPEG) กระบวนการนี้รักษาความแม่นยำของภาพในขณะที่สร้างไฟล์ที่มีขนาดเบา สามารถแสดงในเบราว์เซอร์, อีเมล หรือรายงานโดยไม่ต้องใช้ซอฟต์แวร์ CAD

## Why convert DGN to JPEG?
- **Easy sharing:** JPEG สามารถดูได้บนอุปกรณ์ใดก็ได้  
- **Performance:** ภาพเรสเตอร์โหลดเร็วกว่าไฟล์ CAD เวกเตอร์ในหน้าเว็บ  
- **Compatibility:** เครื่องมือหลายตัว (เช่น เครื่องมือสร้างรายงาน) รองรับเฉพาะรูปแบบเรสเตอร์  

## Prerequisites

ก่อนเริ่ม, ตรวจสอบว่าคุณมีสิ่งต่อไปนี้:

1. **Aspose.CAD Library** – ดาวน์โหลดจากเว็บไซต์อย่างเป็นทางการ **[here](https://releases.aspose.com/cad/java/)**  
2. **Java Development Kit (JDK)** – ติดตั้ง Java 8 หรือใหม่กว่าในเครื่องของคุณ  
3. **IDE** – IDE ที่รองรับ Java ใดก็ได้ เช่น IntelliJ IDEA หรือ Eclipse  

## Import Packages

เพิ่มการนำเข้า (import) ที่จำเป็นลงในคลาส Java ของคุณ:

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
```

## Step‑by‑Step Guide

### Step 1: Load the DGN File

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
DgnImage dgnImage = (DgnImage) Image.load(dataDir + "Nikon_D90_Camera.dgn");
```

*Explanation:* เมธอด `Image.load` จะอ่านไฟล์ DGN ต้นฉบับและคืนค่าเป็นอ็อบเจ็กต์ `DgnImage` ที่เราจะใช้ในการเรสเตอร์ต่อไป

### Step 2: Create a JpegOptions Object

```java
ImageOptionsBase options = new JpegOptions();
```

*Explanation:* `JpegOptions` บอกให้ Aspose.CAD รู้ว่ารูปแบบผลลัพธ์ควรเป็น JPEG และยังให้เราตั้งค่าการเรสเตอร์ได้อีกด้วย

### Step 3: Configure Rasterization Settings

```java
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(600);
vectorOptions.setPageHeight(400);
vectorOptions.setNoScaling(true);
vectorOptions.setAutomaticLayoutsScaling(false);
options.setVectorRasterizationOptions(vectorOptions);
```

*Explanation:* ตัวเลือกเหล่านี้กำหนดขนาดของภาพที่ได้และควบคุมพฤติกรรมการสเกล ปรับ `PageWidth` และ `PageHeight` ให้ตรงกับความละเอียดเป้าหมายของคุณ

### Step 4: Save the Converted Image

```java
OutputStream outStream = new FileOutputStream(dataDir + "ExportDGNToRasterImage_Out.jpg");
dgnImage.save(outStream, options);
```

*Explanation:* เมธอด `save` จะเขียน JPEG ที่เรสเตอร์แล้วลงในสตรีมเอาต์พุตที่ระบุ หลังจากขั้นตอนนี้คุณจะได้ไฟล์ JPEG พร้อมใช้งาน

> **Pro tip:** ห่อโค้ดการแปลงไว้ในบล็อก `try‑with‑resources` เพื่อให้สตรีมปิดโดยอัตโนมัติ

## Common Use Cases

- **Generating thumbnails** สำหรับตัวเรียกดูไฟล์ CAD  
- **Embedding drawings** ลงในรายงาน PDF หรือหน้า HTML  
- **Automated batch processing** ของคลังออกแบบ  

## Troubleshooting & Common Pitfalls

| Issue | Cause | Fix |
|-------|-------|-----|
| Blank or white output image | ตัวเลือกการเรสเตอร์ไม่ถูกต้อง (เช่น `NoScaling` ตั้งเป็น true พร้อมขนาดหน้าไม่ตรง) | ปรับ `PageWidth`/`PageHeight` หรือตั้ง `NoScaling` เป็น false |
| Out‑of‑memory error for large DGN files | โหลดไฟล์ขนาดใหญ่มากโดยไม่มีการสตรีม | เพิ่มขนาด heap ของ JVM (`-Xmx`) หรือประมวลผลไฟล์เป็นส่วนย่อย |
| JPEG quality not sufficient | คุณภาพ JPEG เริ่มต้นต่ำ | ใช้ `((JpegOptions)options).setQuality(100);` ก่อนบันทึก |

## Frequently Asked Questions

### Q1: Can I use Aspose.CAD for Java with other CAD file formats?

A1: ใช่, Aspose.CAD รองรับรูปแบบหลากหลาย ทำให้คุณสามารถ **convert CAD to JPEG** และส่งออกเป็นรูปแบบเรสเตอร์หรือเวกเตอร์อื่น ๆ ได้

### Q2: Is there a free trial available for Aspose.CAD for Java?

A2: มี, คุณสามารถเข้าถึงการทดลองใช้ฟรี **[here](https://releases.aspose.com/)**

### Q3: Where can I find documentation for Aspose.CAD for Java?

A3: ดูเอกสาร **[here](https://reference.aspose.com/cad/java/)**

### Q4: How can I get support for Aspose.CAD for Java?

A4: เยี่ยมชมฟอรัมสนับสนุน **[here](https://forum.aspose.com/c/cad/19)**

### Q5: Where can I purchase a license for Aspose.CAD for Java?

A5: คุณสามารถซื้อใบอนุญาต **[here](https://purchase.aspose.com/buy)**

## Conclusion

คุณได้เรียนรู้วิธี **สร้าง JPEG จาก DGN** ด้วย Aspose.CAD for Java แล้ว ด้วยการทำตามขั้นตอนข้างต้น คุณสามารถรวมการแปลง DGN‑to‑JPEG เข้าไปในแอปพลิเคชัน Java ใดก็ได้ ไม่ว่าจะเป็นเครื่องมือเดสก์ท็อป, บริการเว็บ หรือพายป์ไลน์อัตโนมัติ

---

**Last Updated:** 2026-01-10  
**Tested With:** Aspose.CAD for Java 24.11 (latest at time of writing)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}