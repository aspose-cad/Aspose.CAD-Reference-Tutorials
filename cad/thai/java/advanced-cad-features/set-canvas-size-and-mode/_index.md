---
title: ตั้งค่าขนาดและโหมดแคนวาส
linktitle: ตั้งค่าขนาดและโหมดแคนวาส
second_title: Aspose.CAD Java API
description: สำรวจประสิทธิภาพของ Aspose.CAD สำหรับ Java ด้วยคำแนะนำทีละขั้นตอนเกี่ยวกับการตั้งค่าขนาดและโหมดแคนวาส แปลงไฟล์ CAD เป็นรูปแบบ PDF และ TIFF ได้อย่างง่ายดาย
type: docs
weight: 16
url: /th/java/advanced-cad-features/set-canvas-size-and-mode/
---
## การแนะนำ

คุณต้องการควบคุมพลังของ Aspose.CAD สำหรับ Java เพื่อปรับปรุงกระบวนการแปลง CAD ของคุณหรือไม่? คู่มือที่ครอบคลุมนี้จะแนะนำคุณตลอดขั้นตอนการตั้งค่าขนาดและโหมดแคนวาสโดยใช้ Aspose.CAD สำหรับ Java ไม่ว่าคุณจะเป็นนักพัฒนาที่มีประสบการณ์หรือเพิ่งเริ่มต้น บทช่วยสอนนี้จะให้ข้อมูลเชิงลึกที่คุณต้องการ

## ข้อกำหนดเบื้องต้น

ก่อนที่จะเข้าสู่บทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

-  Aspose.CAD สำหรับ Java: ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้งไลบรารี Aspose.CAD ในสภาพแวดล้อม Java ของคุณ คุณสามารถดาวน์โหลดได้[ที่นี่](https://releases.aspose.com/cad/java/).

- Document Directory: ตั้งค่าไดเร็กทอรีเอกสารเพื่อจัดเก็บไฟล์ CAD ของคุณ ไดเรกทอรีนี้จะถูกอ้างอิงในขั้นตอนการสอน

ตอนนี้ เรามาเริ่มด้วยคำแนะนำทีละขั้นตอนกันดีกว่า

## นำเข้าเนมสเปซ

ในขั้นตอนนี้ เราจะนำเข้าเนมสเปซที่จำเป็นเพื่อเริ่มต้นโครงการ Aspose.CAD ของคุณ
```java
import java.awt.Image;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

## ขั้นตอนที่ 1: นำเข้าคลาส Aspose.CAD

```java
// เส้นทางไปยังไดเร็กทอรีทรัพยากร
String dataDir = "Your Document Directory" + "CADConversion/";

String srcFile = dataDir + "conic_pyramid.dxf";
com.aspose.cad.Image objImage = com.aspose.cad.Image.load(srcFile);
```

 ในตัวอย่างนี้ เราตั้งค่าเส้นทางไปยังไดเร็กทอรีทรัพยากรและโหลดไฟล์ DXF โดยใช้ Aspose.CAD`Image` ระดับ.

## ขั้นตอนที่ 2: ตั้งค่าคุณสมบัติ CadRasterizationOptions

```java
// สร้างอินสแตนซ์ของ CadRasterizationOptions และตั้งค่าคุณสมบัติต่างๆ
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);

rasterizationOptions.setAutomaticLayoutsScaling(true);
rasterizationOptions.setNoScaling(true);
```

 ที่นี่เราสร้างอินสแตนซ์ของ`CadRasterizationOptions` และกำหนดค่าคุณสมบัติ เช่น ความกว้างของหน้า ความสูงของหน้า และตัวเลือกการปรับขนาด

## ขั้นตอนที่ 3: สร้าง PdfOptions และตั้งค่า VectorRasterizationOptions

```java
// สร้างอินสแตนซ์ของ PdfOptions
PdfOptions pdfOptions = new PdfOptions();

// ตั้งค่าคุณสมบัติ VectorRasterizationOptions
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

 ตอนนี้เราสร้าง`PdfOptions` ตัวอย่างและตั้งค่า`VectorRasterizationOptions` คุณสมบัติที่กำหนดไว้ก่อนหน้านี้`CadRasterizationOptions`.

## ขั้นตอนที่ 4: ส่งออกเป็น PDF

```java
// ส่งออก CAD เป็น PDF
objImage.save(dataDir + "result_out_.pdf", pdfOptions);
```

สุดท้ายนี้ เราจะบันทึกอิมเมจ CAD เป็นไฟล์ PDF โดยใช้ตัวเลือกที่ระบุ

## ขั้นตอนที่ 5: สร้าง TiffOptions และตั้งค่า VectorRasterizationOptions

```java
// สร้างอินสแตนซ์ของ TiffOptions
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);

// ตั้งค่าคุณสมบัติ VectorRasterizationOptions
tiffOptions.setVectorRasterizationOptions(rasterizationOptions);
```

ในขั้นตอนนี้ เราได้ตั้งค่า a`TiffOptions` อินสแตนซ์และกำหนดค่า`VectorRasterizationOptions` คุณสมบัติ.

## ขั้นตอนที่ 6: ส่งออกเป็น TIFF

```java
// ส่งออก CAD เป็น TIFF
objImage.save(dataDir + "result_out_.tiff", tiffOptions);
```

สุดท้ายนี้ เราจะบันทึกอิมเมจ CAD ลงในไฟล์ TIFF โดยใช้ตัวเลือกที่ระบุ

## บทสรุป

 ยินดีด้วย! คุณได้ตั้งค่าขนาดและโหมดแคนวาสโดยใช้ Aspose.CAD สำหรับ Java สำเร็จแล้ว บทช่วยสอนนี้เป็นรากฐานที่มั่นคงสำหรับโครงการแปลง CAD ของคุณ สำรวจคุณสมบัติและความเป็นไปได้เพิ่มเติมใน[เอกสาร Aspose.CAD](https://reference.aspose.com/cad/java/).

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถใช้ Aspose.CAD สำหรับ Java กับเฟรมเวิร์ก Java อื่นได้หรือไม่

ตอบ 1: ใช่ Aspose.CAD ได้รับการออกแบบมาเพื่อทำงานร่วมกับเฟรมเวิร์ก Java ต่างๆ ได้อย่างราบรื่น

### คำถามที่ 2: Aspose.CAD มีใบอนุญาตชั่วคราวหรือไม่

 A2: ได้ คุณสามารถขอรับใบอนุญาตชั่วคราวได้[ที่นี่](https://purchase.aspose.com/temporary-license/).

### คำถามที่ 3: ฉันจะรับการสนับสนุนจากชุมชนสำหรับ Aspose.CAD ได้ที่ไหน

 A3: เยี่ยมชม[ฟอรั่ม Aspose.CAD](https://forum.aspose.com/c/cad/19) สำหรับการสนับสนุนและการอภิปรายของชุมชน

### คำถามที่ 4: ฉันสามารถทดลองใช้ Aspose.CAD ได้ฟรีหรือไม่

 A4: แน่นอน! ทดลองใช้ฟรี[ที่นี่](https://releases.aspose.com/).

### คำถามที่ 5: ฉันจะซื้อ Aspose.CAD สำหรับ Java ได้อย่างไร

 A5: ซื้อสินค้า[ที่นี่](https://purchase.aspose.com/buy).