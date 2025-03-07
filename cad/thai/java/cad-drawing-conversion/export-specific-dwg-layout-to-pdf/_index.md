---
title: ส่งออกเค้าโครง DWG เฉพาะเป็น PDF โดยใช้ Aspose.CAD สำหรับ Java
linktitle: ส่งออกเค้าโครง DWG เฉพาะเป็น PDF
second_title: Aspose.CAD Java API
description: สำรวจคำแนะนำทีละขั้นตอนเพื่อส่งออกเค้าโครง DWG เฉพาะเป็น PDF โดยใช้ Aspose.CAD สำหรับ Java เพิ่มประสิทธิภาพเวิร์กโฟลว์ CAD ของคุณได้อย่างง่ายดาย
weight: 14
url: /th/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# ส่งออกเค้าโครง DWG เฉพาะเป็น PDF โดยใช้ Aspose.CAD สำหรับ Java

## การแนะนำ

ในโลกแบบไดนามิกของการออกแบบโดยใช้คอมพิวเตอร์ช่วย (CAD) Aspose.CAD สำหรับ Java กลายเป็นเครื่องมืออันทรงพลังสำหรับจัดการและแปลงภาพวาด DWG ในบทช่วยสอนนี้ เราจะสำรวจสถานการณ์เฉพาะ: การส่งออกเค้าโครง DWG ที่กำหนดเป็นไฟล์ PDF กระบวนการนี้รับประกันความแม่นยำและความยืดหยุ่นในโครงการ CAD ของคุณ

## ข้อกำหนดเบื้องต้น

ก่อนที่จะเจาะลึกบทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

- สภาพแวดล้อมการพัฒนา Java: ตรวจสอบให้แน่ใจว่าคุณมีสภาพแวดล้อมการพัฒนา Java ที่ใช้งานได้บนระบบของคุณ
-  ไลบรารี Aspose.CAD: ดาวน์โหลดและตั้งค่าไลบรารี Aspose.CAD สำหรับ Java คุณสามารถค้นหาห้องสมุด[ที่นี่](https://releases.aspose.com/cad/java/).
- - ไฟล์ DWG: เตรียมไฟล์ DWG ให้พร้อมสำหรับการส่งออก คุณสามารถใช้ไฟล์ตัวอย่าง "visualization_-_conference_room.dwg" สำหรับบทช่วยสอนนี้

## นำเข้าเนมสเปซ

## ขั้นตอนที่ 1: ตั้งค่าสภาพแวดล้อมของโครงการ

เริ่มต้นด้วยการสร้างโปรเจ็กต์ Java และตรวจสอบให้แน่ใจว่าไลบรารี Aspose.CAD ได้รับการผสานรวมอย่างถูกต้อง คุณสามารถดาวน์โหลดได้[ที่นี่](https://releases.aspose.com/cad/java/).

## ขั้นตอนที่ 2: นำเข้าแพ็คเกจที่จำเป็น

ในคลาส Java ของคุณ ให้นำเข้าแพ็คเกจ Aspose.CAD ที่จำเป็นเพื่อใช้ฟังก์ชันต่างๆ ได้อย่างราบรื่น

```java

import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## ขั้นตอนที่ 3: โหลดไฟล์ DWG

ระบุเส้นทางของไฟล์ DWG ของคุณและโหลดลงในออบเจ็กต์รูปภาพ Aspose.CAD

```java
String srcFile = dataDir + "visualization_-_conference_room.dwg";
Image image = Image.load(srcFile);
```

## ขั้นตอนที่ 4: กำหนดค่าตัวเลือกการแรสเตอร์

 สร้างอินสแตนซ์ของ`CadRasterizationOptions` และปรับแต่งคุณสมบัติตามความต้องการของคุณ

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
// ระบุชื่อเค้าโครงที่ต้องการ
rasterizationOptions.setLayouts(new String[] {"Layout1"});
```

## ขั้นตอนที่ 5: ตั้งค่าตัวเลือกการส่งออก PDF

 สร้างก`PdfOptions` ตัวอย่างและตั้งค่า`VectorRasterizationOptions` คุณสมบัติที่กำหนดไว้ก่อนหน้านี้`CadRasterizationOptions`.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## ขั้นตอนที่ 6: ส่งออก DWG เป็น PDF

บันทึกภาพที่แก้ไขเป็นไฟล์ PDF เสร็จสิ้นกระบวนการแปลง

```java
image.save(dataDir + "ExportSpecificLayoutToPDF_out_.pdf", pdfOptions);
```

## บทสรุป

การเรียนรู้ศิลปะในการส่งออกเค้าโครง DWG เฉพาะเป็น PDF โดยใช้ Aspose.CAD สำหรับ Java สามารถปรับปรุงเวิร์กโฟลว์ CAD ของคุณได้อย่างมาก ด้วยขั้นตอนที่ให้มา คุณสามารถรวมฟังก์ชันการทำงานนี้เข้ากับโปรเจ็กต์ของคุณได้อย่างราบรื่น มั่นใจในความแม่นยำและประสิทธิภาพ

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถใช้ Aspose.CAD สำหรับ Java กับไลบรารี CAD ที่ใช้ Java อื่นๆ ได้หรือไม่

Aspose.CAD สำหรับ Java เป็นไลบรารีแบบสแตนด์อโลน แต่สามารถรวมเข้ากับไลบรารีที่ใช้ Java อื่นๆ ได้เพื่อเพิ่มฟังก์ชันการทำงาน

### คำถามที่ 2: มีตัวเลือกสิทธิ์การใช้งานสำหรับ Aspose.CAD หรือไม่

 ใช่ คุณสามารถสำรวจตัวเลือกสิทธิ์การใช้งานและรายละเอียดการซื้อได้[ที่นี่](https://purchase.aspose.com/buy).

### คำถามที่ 3: ฉันจะขอรับใบอนุญาตชั่วคราวสำหรับ Aspose.CAD ได้อย่างไร

 เยี่ยม[ลิงค์นี้](https://purchase.aspose.com/temporary-license/) เพื่อรับใบอนุญาตชั่วคราวสำหรับ Aspose.CAD

### คำถามที่ 4: ฉันจะรับการสนับสนุนสำหรับ Aspose.CAD ได้ที่ไหน

 หากมีข้อสงสัยหรือความช่วยเหลือ โปรดไปที่[ฟอรั่ม Aspose.CAD](https://forum.aspose.com/c/cad/19).

### คำถามที่ 5: Aspose.CAD มีรุ่นทดลองใช้ฟรีหรือไม่

 ใช่ คุณสามารถเข้าถึงการทดลองใช้ฟรีได้[ที่นี่](https://releases.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
