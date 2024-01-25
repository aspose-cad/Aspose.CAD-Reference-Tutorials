---
title: ส่งออก IFC เป็น PNG ด้วย Aspose.CAD สำหรับ Java
linktitle: ส่งออก IFC เป็น PNG
second_title: Aspose.CAD Java API
description: แปลง IFC เป็น PNG ได้อย่างง่ายดายด้วย Aspose.CAD สำหรับ Java ปฏิบัติตามบทช่วยสอนทีละขั้นตอนของเรา
type: docs
weight: 18
url: /th/java/cad-export-options/export-ifc-to-png/
---
## การแนะนำ

ยินดีต้อนรับสู่บทช่วยสอนทีละขั้นตอนเกี่ยวกับการส่งออก IFC (Industry Foundation Classes) ไปยัง PNG โดยใช้ Aspose.CAD สำหรับ Java Aspose.CAD เป็นไลบรารี Java ที่ทรงพลังซึ่งมีความสามารถมากมายสำหรับการทำงานกับไฟล์ CAD รวมถึงรูปแบบ IFC ในบทช่วยสอนนี้ เราจะแนะนำคุณตลอดกระบวนการแปลงไฟล์ IFC เป็นรูปภาพ PNG พร้อมคำอธิบายโดยละเอียดในแต่ละขั้นตอน

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเริ่มต้น ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

-  ไลบรารี Aspose.CAD: ดาวน์โหลดและติดตั้งไลบรารี Aspose.CAD สำหรับ Java จาก[ลิ้งค์ดาวน์โหลด](https://releases.aspose.com/cad/java/).

- ไดเร็กทอรีเอกสาร: เตรียมไดเร็กทอรีบนระบบของคุณซึ่งมีไฟล์ IFC ของคุณอยู่

## นำเข้าเนมสเปซ

ในโปรเจ็กต์ Java ของคุณ ให้นำเข้าเนมสเปซที่จำเป็นดังที่แสดงด้านล่าง:

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.ifc.IfcImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

## ขั้นตอนที่ 1: โหลดไฟล์ IFC

```java
String dataDir = "Your Document Directory" + "ExportingIFC/";
String fileName = dataDir + "example.ifc";
IfcImage cadImage = (IfcImage)Image.load(fileName);
```

ขั้นตอนนี้เกี่ยวข้องกับการโหลดไฟล์ IFC โดยใช้ Aspose.CAD

## ขั้นตอนที่ 2: ตั้งค่าตัวเลือกเวกเตอร์

```java
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
```

กำหนดค่าตัวเลือกเวกเตอร์สำหรับการแรสเตอร์ โดยระบุความกว้างและความสูงของหน้า

## ขั้นตอนที่ 3: ตั้งค่าตัวเลือก PNG

```java
PngOptions pngOptions = new PngOptions();
pngOptions.setVectorRasterizationOptions(vectorOptions);
```

ตั้งค่าตัวเลือก PNG รวมถึงตัวเลือกการแรสเตอร์แบบเวกเตอร์

## ขั้นตอนที่ 4: บันทึกเป็น PNG

```java
String outPath = dataDir + "example.png";
cadImage.save(outPath, pngOptions);
```

บันทึกภาพที่ประมวลผลในรูปแบบ PNG

## บทสรุป

ยินดีด้วย! คุณได้แปลงไฟล์ IFC เป็น PNG โดยใช้ Aspose.CAD สำหรับ Java สำเร็จแล้ว บทช่วยสอนนี้ให้คำแนะนำที่ครอบคลุม เพื่อให้มั่นใจว่าคุณสามารถรวมฟังก์ชันการทำงานนี้เข้ากับโปรเจ็กต์ของคุณได้อย่างราบรื่น

## คำถามที่พบบ่อย

### คำถามที่ 1: Aspose.CAD เข้ากันได้กับไฟล์ IFC ทุกเวอร์ชันหรือไม่

 A1: Aspose.CAD รองรับไฟล์ IFC เวอร์ชันต่างๆ อ้างถึง[เอกสารประกอบ](https://reference.aspose.com/cad/java/) สำหรับรายละเอียดความเข้ากันได้

### คำถามที่ 2: ฉันสามารถปรับแต่งตัวเลือกการแรสเตอร์เพิ่มเติมได้หรือไม่

 A2: แน่นอน! สำรวจ[เอกสารประกอบ](https://reference.aspose.com/cad/java/) สำหรับตัวเลือกการปรับแต่งขั้นสูง

### คำถามที่ 3: มีเวอร์ชันทดลองใช้งานหรือไม่

A3: ได้ คุณสามารถเข้าถึงเวอร์ชันทดลองใช้ฟรีได้[ที่นี่](https://releases.aspose.com/).

### คำถามที่ 4: ฉันจะรับสิทธิ์การใช้งานชั่วคราวสำหรับ Aspose.CAD ได้อย่างไร

 A4: รับใบอนุญาตชั่วคราวจาก[ลิงค์นี้](https://purchase.aspose.com/temporary-license/).

### คำถามที่ 5: ฉันจะขอความช่วยเหลือหรือหารือเกี่ยวกับปัญหาได้ที่ไหน

A5: เยี่ยมชม[ฟอรั่ม Aspose.CAD](https://forum.aspose.com/c/cad/19) เพื่อสนับสนุนชุมชน
