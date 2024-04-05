---
title: ส่งออก DWG เป็น PDF หรือ Raster โดยใช้ Aspose.CAD สำหรับ Java
linktitle: ส่งออก DWG เป็น PDF หรือ Raster
second_title: Aspose.CAD Java API
description: สำรวจกระบวนการส่งออกไฟล์ DWG เป็น PDF หรือรูปภาพแรสเตอร์ใน Java ได้อย่างราบรื่นโดยใช้ Aspose.CAD คำแนะนำทีละขั้นตอนนี้รับประกันความแม่นยำและประสิทธิภาพ
type: docs
weight: 13
url: /th/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/
---
## การแนะนำ

ในโลกแบบไดนามิกของการออกแบบโดยใช้คอมพิวเตอร์ช่วย (CAD) การจัดการภาพวาดอย่างมีประสิทธิภาพถือเป็นสิ่งสำคัญ Aspose.CAD สำหรับ Java มอบโซลูชันอันทรงพลังสำหรับการส่งออกไฟล์ DWG เป็น PDF หรือรูปภาพแรสเตอร์ บทช่วยสอนนี้จะแนะนำคุณตลอดกระบวนการ เพื่อให้มั่นใจว่าคุณจะสามารถใช้ประโยชน์จาก Aspose.CAD สำหรับ Java ได้เต็มศักยภาพ

## ข้อกำหนดเบื้องต้น

ก่อนที่จะเข้าสู่บทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีสิ่งต่อไปนี้:

- ความเข้าใจพื้นฐานเกี่ยวกับการเขียนโปรแกรม Java
-  ติดตั้ง Aspose.CAD สำหรับไลบรารี Java แล้ว ถ้าไม่เช่นนั้นให้ดาวน์โหลด[ที่นี่](https://releases.aspose.com/cad/java/).
- ไฟล์ DWG เพื่อการทดสอบ คุณสามารถใช้ไฟล์ "Bottom_plate.dwg" ที่ให้มาได้

## นำเข้าเนมสเปซ

ในโปรเจ็กต์ Java ของคุณ ให้นำเข้าเนมสเปซที่จำเป็นเพื่อเริ่มต้นกระบวนการ:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.UnitType;
```

## ขั้นตอนที่ 1: โหลดไฟล์ DWG

 เริ่มต้นด้วยการโหลดไฟล์ DWG ของคุณโดยใช้ Aspose.CAD`Image` ระดับ:

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String srcFile = dataDir + "Bottom_plate.dwg";
Image objImage = Image.load(srcFile);
```

## ขั้นตอนที่ 2: กำหนดประเภทหน่วย

ถัดไป ตรวจสอบประเภทหน่วยของไฟล์ DWG ที่โหลด:

```java
Boolean currentUnitIsMetric = IsMetric(objImage.getUnitType());
int currentUnitCoefficient = objImage.getUnitType();
```

## ขั้นตอนที่ 3: ตั้งค่าตัวเลือกการแรสเตอร์

ขึ้นอยู่กับประเภทของหน่วย ให้กำหนดค่าตัวเลือกการแรสเตอร์:

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();

if (currentUnitIsMetric) {
    // หน่วยเมตริก
    double metersCoeff = 1 / 1000.0;
    double scaleFactor = metersCoeff / currentUnitCoefficient;
    rasterizationOptions.setPageWidth((float)(210 * scaleFactor));
    rasterizationOptions.setPageHeight((float)(297 * scaleFactor));
    rasterizationOptions.setUnitType(UnitType.Millimeter);
} else {
    // หน่วยจักรวรรดิ
    rasterizationOptions.setPageWidth((float)(8.27f / currentUnitCoefficient));
    rasterizationOptions.setPageHeight((float)(11.69f / currentUnitCoefficient));
    rasterizationOptions.setUnitType(UnitType.Inch);
}
```

## ขั้นตอนที่ 4: กำหนดค่าตัวเลือก PDF

ตั้งค่าตัวเลือกการส่งออก PDF:

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(new CadRasterizationOptions());
```

## ขั้นตอนที่ 5: บันทึกเป็น PDF

สุดท้าย ให้บันทึกไฟล์ DWG เป็น PDF:

```java
objImage.save(dataDir + "Saved.pdf", pdfOptions);
```

และคุณก็ได้แล้ว! คุณได้ส่งออกไฟล์ DWG เป็น PDF โดยใช้ Aspose.CAD สำหรับ Java สำเร็จแล้ว

## บทสรุป

บทช่วยสอนนี้ให้คำแนะนำทีละขั้นตอนเกี่ยวกับการใช้ประโยชน์จาก Aspose.CAD สำหรับ Java เพื่อส่งออกไฟล์ DWG เป็น PDF หรือรูปภาพแรสเตอร์ ไลบรารีนี้ทำให้กระบวนการง่ายขึ้น ช่วยให้คุณสามารถจัดการแบบร่าง CAD ในแอปพลิเคชัน Java ของคุณได้อย่างมีประสิทธิภาพ

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถใช้ Aspose.CAD สำหรับ Java กับเฟรมเวิร์ก Java อื่นได้หรือไม่

ตอบ 1: ใช่ Aspose.CAD สำหรับ Java ทำงานร่วมกับเฟรมเวิร์ก Java ยอดนิยมได้อย่างราบรื่น

### คำถามที่ 2: Aspose.CAD สำหรับ Java มีใบอนุญาตชั่วคราวหรือไม่

 A2: ได้ คุณสามารถขอรับใบอนุญาตชั่วคราวได้[ที่นี่](https://purchase.aspose.com/temporary-license/).

### คำถามที่ 3: ฉันจะรับการสนับสนุนสำหรับ Aspose.CAD สำหรับ Java ได้ที่ไหน

 A3: เยี่ยมชม[ฟอรั่ม Aspose.CAD](https://forum.aspose.com/c/cad/19) เพื่อขอความช่วยเหลือจากชุมชน

### คำถามที่ 4: ฉันจะซื้อใบอนุญาตสำหรับ Aspose.CAD สำหรับ Java ได้อย่างไร

 A4: คุณสามารถซื้อใบอนุญาตได้[ที่นี่](https://purchase.aspose.com/buy).

### คำถามที่ 5: Aspose.CAD สำหรับ Java รองรับหน่วยใดบ้าง

A5: Aspose.CAD สำหรับ Java รองรับทั้งหน่วยเมตริกและหน่วยอิมพีเรียล