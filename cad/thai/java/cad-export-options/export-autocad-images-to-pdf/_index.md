---
title: ส่งออกรูปภาพ AutoCAD เป็น PDF - Aspose.CAD สำหรับการสอน Java
linktitle: ส่งออกรูปภาพ AutoCAD เป็น PDF
second_title: Aspose.CAD Java API
description: ส่งออกรูปภาพ AutoCAD เป็น PDF ได้อย่างง่ายดายโดยใช้ Aspose.CAD สำหรับ Java ปฏิบัติตามคำแนะนำทีละขั้นตอนของเราเพื่อการบูรณาการที่ราบรื่น
type: docs
weight: 10
url: /th/java/cad-export-options/export-autocad-images-to-pdf/
---
## การแนะนำ

คุณต้องการแปลงรูปภาพ AutoCAD เป็น PDF โดยใช้ Java ได้อย่างราบรื่นหรือไม่? ไม่ต้องมองอีกต่อไป! ในบทช่วยสอนนี้ เราจะแนะนำคุณตลอดกระบวนการโดยใช้ Aspose.CAD สำหรับ Java ซึ่งเป็นไลบรารีอันทรงพลังที่ทำให้งานที่ซับซ้อนง่ายขึ้น ในตอนท้าย คุณจะสามารถส่งออกภาพ 3 มิติเป็น PDF ได้อย่างง่ายดาย

## ข้อกำหนดเบื้องต้น

ก่อนที่จะเข้าสู่บทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

- สภาพแวดล้อมการพัฒนา Java: ตรวจสอบให้แน่ใจว่าคุณได้ตั้งค่าสภาพแวดล้อมการพัฒนา Java บนระบบของคุณ
-  Aspose.CAD สำหรับไลบรารี Java: ดาวน์โหลดและติดตั้ง Aspose.CAD สำหรับไลบรารี Java จาก[ลิ้งค์ดาวน์โหลด](https://releases.aspose.com/cad/java/).
- Document Directory: สร้างไดเร็กทอรีเพื่อจัดเก็บไฟล์ CAD ของคุณเพื่อให้เข้าถึงได้ง่าย

## นำเข้าเนมสเปซ

ในโปรเจ็กต์ Java ของคุณ ให้นำเข้าเนมสเปซที่จำเป็นเพื่อใช้ฟังก์ชันการทำงานของ Aspose.CAD สำหรับ Java:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
//นำเข้า com.aspose.cad.imageoptions.TypeOfEntities;
```

ตอนนี้ เรามาแบ่งโค้ดตัวอย่างออกเป็นหลายขั้นตอน:

## ขั้นตอนที่ 1: ตั้งค่าเส้นทางไดเรกทอรีทรัพยากร

```java
String dataDir = "Your Document Directory" + "ExportingCAD/";
```

 ให้แน่ใจว่าคุณเปลี่ยน`"Your Document Directory"` พร้อมเส้นทางไปยังไดเร็กทอรีเอกสารของคุณ

## ขั้นตอนที่ 2: โหลดอิมเมจ CAD

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image cadImage = Image.load(srcFile);
```

 แทนที่`"conic_pyramid.dxf"` ด้วยชื่อไฟล์ AutoCAD ของคุณ

## ขั้นตอนที่ 3: ตั้งค่าตัวเลือกการแรสเตอร์

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(500);
rasterizationOptions.setPageHeight(500);
// rasterizationOptions.setTypeOfEntities (TypeOfEntities.Entities3D);

rasterizationOptions.setLayouts(new String[] {"Model"});
```

ปรับการตั้งค่าความกว้าง ความสูง และเค้าโครงตามความต้องการของคุณ

## ขั้นตอนที่ 4: กำหนดค่าตัวเลือก PDF

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

ตั้งค่าตัวเลือก PDF รวมถึงการตั้งค่าการแรสเตอร์เวกเตอร์

## ขั้นตอนที่ 5: บันทึก PDF

```java
cadImage.save(dataDir + "Export3DImagestoPDF_out_.pdf", pdfOptions);
```

ระบุไดเร็กทอรีเอาต์พุตและชื่อไฟล์สำหรับ PDF ที่สร้างขึ้น

## บทสรุป

ยินดีด้วย! คุณได้เรียนรู้วิธีส่งออกรูปภาพ AutoCAD เป็น PDF โดยใช้ Aspose.CAD สำหรับ Java เรียบร้อยแล้ว คู่มือที่เป็นมิตรต่อผู้ใช้นี้ทำให้กระบวนการที่ซับซ้อนง่ายขึ้น ทำให้นักพัฒนาทุกระดับสามารถเข้าถึงได้

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถใช้ Aspose.CAD สำหรับ Java กับไฟล์ CAD รูปแบบอื่นได้หรือไม่

ตอบ 1: ใช่ Aspose.CAD รองรับรูปแบบ CAD ที่หลากหลาย ซึ่งให้ความยืดหยุ่นในโครงการของคุณ

### คำถามที่ 2: ฉันจะขอรับใบอนุญาตชั่วคราวสำหรับ Aspose.CAD สำหรับ Java ได้อย่างไร

 A2: เยี่ยมเลย[ที่นี่](https://purchase.aspose.com/temporary-license/) เพื่อขอรับใบอนุญาตชั่วคราวเพื่อการประเมิน

### คำถามที่ 3: มีตัวเลือกเค้าโครงสำหรับการแรสเตอร์หรือไม่

A3: ได้ คุณสามารถปรับแต่งเลย์เอาต์ได้ตามความต้องการของคุณ ซึ่งเป็นการเพิ่มประสิทธิภาพกระบวนการเรนเดอร์

### คำถามที่ 4: ฉันสามารถกำหนดขนาดของไฟล์ PDF เอาต์พุตได้หรือไม่

A4: แน่นอน! ปรับพารามิเตอร์ความกว้างและความสูงของหน้าในตัวเลือกการแรสเตอร์

### คำถามที่ 5: ฉันจะขอความช่วยเหลือหรือหารือเกี่ยวกับปัญหาที่เกี่ยวข้องกับ Aspose.CAD สำหรับ Java ได้ที่ไหน

 A5: ตรงไปที่[ฟอรั่ม Aspose.CAD](https://forum.aspose.com/c/cad/19) สำหรับการสนับสนุนและการอภิปรายโดยเฉพาะ