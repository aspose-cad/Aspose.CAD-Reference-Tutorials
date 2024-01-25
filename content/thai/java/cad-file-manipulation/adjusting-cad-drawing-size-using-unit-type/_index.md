---
title: การปรับขนาดการเขียนแบบ CAD โดยใช้ประเภทหน่วยด้วย Aspose.CAD สำหรับ Java
linktitle: การปรับขนาดการเขียนแบบ CAD โดยใช้ประเภทยูนิต
second_title: Aspose.CAD Java API
description: สำรวจพลังของ Aspose.CAD สำหรับ Java ในการปรับขนาดการวาด CAD ได้อย่างง่ายดาย ปฏิบัติตามคำแนะนำทีละขั้นตอนของเราเพื่อความแม่นยำและความสามารถในการปรับเปลี่ยน
type: docs
weight: 14
url: /th/java/cad-file-manipulation/adjusting-cad-drawing-size-using-unit-type/
---
## การแนะนำ

ในขอบเขตที่เปลี่ยนแปลงตลอดเวลาของการออกแบบโดยใช้คอมพิวเตอร์ช่วย (CAD) ความแม่นยำและความสามารถในการปรับตัวเป็นสิ่งสำคัญยิ่ง ข้อกำหนดทั่วไปประการหนึ่งคือการปรับขนาดของแบบร่าง CAD ตามประเภทหน่วยเฉพาะ Aspose.CAD สำหรับ Java กลายเป็นพันธมิตรที่ทรงพลัง โดยมอบความสามารถที่ราบรื่นในการจัดการไฟล์ CAD โดยทางโปรแกรม

## ข้อกำหนดเบื้องต้น

ก่อนที่จะเข้าสู่บทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

- สภาพแวดล้อมการพัฒนา Java: ตรวจสอบให้แน่ใจว่าคุณได้ตั้งค่าสภาพแวดล้อมการพัฒนา Java ที่ใช้งานได้บนเครื่องของคุณ

-  Aspose.CAD สำหรับไลบรารี Java: ดาวน์โหลดและรวมไลบรารี Aspose.CAD เข้ากับโปรเจ็กต์ Java ของคุณ คุณสามารถขอรับห้องสมุดได้[ที่นี่](https://releases.aspose.com/cad/java/).

## นำเข้าเนมสเปซ

ในโค้ด Java ของคุณ ให้รวมเนมสเปซที่จำเป็นเพื่อเข้าถึงฟังก์ชันการทำงานของ Aspose.CAD เพิ่มการนำเข้าต่อไปนี้:

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

ตอนนี้ เรามาแจกแจงขั้นตอนการปรับขนาดการเขียนแบบ CAD โดยใช้ประเภทหน่วยเป็นขั้นตอนที่สามารถจัดการได้:

## ขั้นตอนที่ 1: กำหนดไดเร็กทอรีข้อมูล

```java
String dataDir = "Your Document Directory" + "CADConversion/";
```

กำหนดเส้นทางสำหรับไดเร็กทอรีที่มีไฟล์ CAD ของคุณ

## ขั้นตอนที่ 2: โหลด CAD Drawing

```java
String sourceFilePath = dataDir + "sample.dwg";
Image image = Image.load(sourceFilePath);
```

 โหลดแบบร่าง CAD โดยใช้ Aspose.CAD's`Image` ระดับ.

## ขั้นตอนที่ 3: สร้างตัวเลือก BMP

```java
BmpOptions bmpOptions = new BmpOptions();
```

 ยกตัวอย่าง`BmpOptions` คลาสสำหรับส่งออกเค้าโครง CAD เป็นรูปแบบ BMP

## ขั้นตอนที่ 4: กำหนดค่าตัวเลือกการแรสเตอร์

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
bmpOptions.setVectorRasterizationOptions(cadRasterizationOptions);
```

 สร้างอินสแตนซ์ของ`CadRasterizationOptions` และเชื่อมโยงมันเข้ากับ`BmpOptions` สำหรับการแรสเตอร์เวกเตอร์

## ขั้นตอนที่ 5: ตั้งค่าประเภทยูนิต

```java
cadRasterizationOptions.setUnitType(UnitType.Centimeter);
```

ระบุประเภทหน่วยที่ต้องการสำหรับการเขียนแบบ CAD ในตัวอย่างนี้ เราได้ตั้งค่าเป็นเซนติเมตร

## ขั้นตอนที่ 6: ตั้งค่าเค้าโครง

```java
cadRasterizationOptions.setLayouts(new String[] { "Model" });
```

กำหนดเค้าโครงที่จะพิจารณาระหว่างการส่งออก ในกรณีนี้ เราได้เลือกเค้าโครง "แบบจำลอง"

## ขั้นตอนที่ 7: ส่งออกเป็น BMP

```java
String outPath = sourceFilePath + ".bmp";
image.save(outPath, bmpOptions);
```

สุดท้าย ให้บันทึกแบบร่าง CAD ที่แก้ไขแล้วในรูปแบบ BMP

## บทสรุป

ด้วย Aspose.CAD สำหรับ Java การปรับขนาดการวาด CAD กลายเป็นเรื่องง่าย บทช่วยสอนนี้ได้อธิบายคุณตลอดกระบวนการ โดยเน้นความสำคัญของแต่ละขั้นตอนในการบรรลุผลลัพธ์ที่แม่นยำ

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถใช้ Aspose.CAD สำหรับ Java กับภาษาการเขียนโปรแกรมอื่นได้หรือไม่

คำตอบ 1: Aspose.CAD รองรับ Java เป็นหลัก แต่มีเวอร์ชันสำหรับภาษาอื่น เช่น .NET

### คำถามที่ 2: มีตัวเลือกสิทธิ์การใช้งานสำหรับ Aspose.CAD หรือไม่

 ตอบ 2: ได้ คุณสามารถสำรวจตัวเลือกสิทธิ์การใช้งานและซื้อ Aspose.CAD ได้[ที่นี่](https://purchase.aspose.com/buy).

### คำถามที่ 3: Aspose.CAD มีรุ่นทดลองใช้ฟรีหรือไม่

 A3: แน่นอน คุณสามารถทดลองใช้ฟรีได้[ที่นี่](https://releases.aspose.com/).

### คำถามที่ 4: ฉันจะรับการสนับสนุนสำหรับ Aspose.CAD สำหรับ Java ได้อย่างไร

 A4: เยี่ยมชมฟอรั่ม Aspose.CAD[ที่นี่](https://forum.aspose.com/c/cad/19) เพื่อการสนับสนุนอย่างครอบคลุม

### คำถามที่ 5: ฉันสามารถขอรับใบอนุญาตชั่วคราวสำหรับ Aspose.CAD ได้หรือไม่

 A5: ได้ คุณสามารถขอรับใบอนุญาตชั่วคราวได้[ที่นี่](https://purchase.aspose.com/temporary-license/).