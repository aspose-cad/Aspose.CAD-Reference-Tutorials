---
title: รองรับปากกาในการส่งออก
linktitle: รองรับปากกาในการส่งออก
second_title: Aspose.CAD Java API
description: การปรับแต่งปากกาหลักในการส่งออก CAD ด้วย Aspose.CAD สำหรับ Java ปฏิบัติตามคำแนะนำทีละขั้นตอนของเราเพื่อการบูรณาการที่ราบรื่น
weight: 13
url: /th/java/advanced-cad-features/pen-support-in-export/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# รองรับปากกาในการส่งออก

## การแนะนำ

ในสภาพแวดล้อมของการแปลง CAD (Computer-Aided Design) ที่เปลี่ยนแปลงตลอดเวลา Aspose.CAD สำหรับ Java กลายเป็นเครื่องมืออันทรงพลัง โดยนำเสนอความสามารถที่ครอบคลุมในการจัดการไฟล์ CAD ในบรรดาคุณสมบัติที่หลากหลาย การรองรับการปรับแต่งปากการะหว่างการส่งออกมีความโดดเด่น ทำให้ผู้ใช้สามารถปรับแต่งรูปลักษณ์ของภาพที่ส่งออกได้ บทช่วยสอนนี้จะแนะนำคุณตลอดกระบวนการใช้ประโยชน์จากการรองรับปากกาในฟังก์ชันการส่งออก โดยเน้นที่การใช้งานจริงโดยใช้ Java

## ข้อกำหนดเบื้องต้น

ก่อนที่จะเจาะลึกบทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

- สภาพแวดล้อมการพัฒนา Java: ตรวจสอบให้แน่ใจว่าคุณได้ตั้งค่าสภาพแวดล้อมการพัฒนา Java ที่ใช้งานได้บนเครื่องของคุณ

-  ไลบรารี Aspose.CAD: ดาวน์โหลดและรวมไลบรารี Aspose.CAD เข้ากับโปรเจ็กต์ Java ของคุณ คุณสามารถค้นหาห้องสมุด[ที่นี่](https://releases.aspose.com/cad/java/).

ตอนนี้ มาดูบทช่วยสอนและสำรวจขั้นตอนต่างๆ เพื่อควบคุมการรองรับปากการะหว่างการส่งออก CAD กัน

## นำเข้าเนมสเปซ

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.PenOptions;
import com.aspose.cad.internal.imaging.LineCap;
```

## ขั้นตอนที่ 1: กำหนดไดเร็กทอรีเอกสารของคุณ

```java
String dataDir = "Your Document Directory" + "CADConversion/";
```

ตรวจสอบให้แน่ใจว่าได้แทนที่ "Your Document Directory" ด้วยเส้นทางจริงไปยังเอกสาร CAD ของคุณ

## ขั้นตอนที่ 2: โหลดไฟล์ CAD

```java
String srcFile = dataDir + "conic_pyramid.dxf";
CadImage cadImage = (CadImage) Image.load(srcFile);
```

ขั้นตอนนี้เกี่ยวข้องกับการโหลดไฟล์ CAD ในกรณีนี้คือ "conic_pyramid.dxf" โดยใช้ไลบรารี Aspose.CAD

## ขั้นตอนที่ 3: กำหนดค่าตัวเลือกการแรสเตอร์

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(cadImage.getWidth() * 100);
rasterizationOptions.setPageHeight(cadImage.getHeight() * 100);
```

ปรับความกว้างและความสูงของหน้าตามความต้องการเฉพาะของคุณ ค่าเหล่านี้จะกำหนดขนาดของรูปภาพที่ส่งออก

## ขั้นตอนที่ 4: ปรับแต่งตัวเลือกปากกา

```java
PenOptions penOts = new PenOptions();
penOts.setStartCap(LineCap.Flat);
penOts.setEndCap(LineCap.Flat);
```

ปรับแต่งส่วนเริ่มต้นและส่วนปลายของปากกาตามต้องการ การปรับแต่งนี้ใช้กับการส่งออกออบเจ็กต์ CadImage ไปเป็นรูปแบบรูปภาพต่างๆ

## ขั้นตอนที่ 5: กำหนดค่าตัวเลือกการส่งออก PDF

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

ระบุตัวเลือกการแรสเตอร์แบบเวกเตอร์ รวมถึงตัวเลือกการแรสเตอร์ที่กำหนดค่าไว้ก่อนหน้านี้

## ขั้นตอนที่ 6: บันทึก PDF ที่ส่งออก

```java
cadImage.save((dataDir + "9LHATT-A56_generated.pdf"), pdfOptions);
```

บันทึก PDF ที่ส่งออกด้วยชื่อไฟล์ที่ระบุ ("9LHATT-A56_generated.pdf" ในตัวอย่างนี้) และตัวเลือกที่กำหนดค่าไว้

## บทสรุป

โดยสรุป การควบคุมการรองรับปากการะหว่างการส่งออก CAD ด้วย Aspose.CAD สำหรับ Java ช่วยให้ผู้ใช้สามารถปรับแต่งรูปลักษณ์ของภาพที่ส่งออกได้ ด้วยการทำตามคำแนะนำทีละขั้นตอนนี้ คุณจะได้เรียนรู้วิธีบูรณาการการปรับแต่งปากกาเข้ากับขั้นตอนการแปลง CAD ของคุณได้อย่างราบรื่น

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถปรับแต่งตัวเลือกปากกาสำหรับรูปแบบอื่นที่ไม่ใช่ PDF ได้หรือไม่

A1: ใช่ การปรับแต่งปากกาที่แสดงในบทช่วยสอนนี้สามารถใช้ได้กับรูปแบบรูปภาพต่างๆ รวมถึง PDF, PNG, BMP, GIF, JPEG2000, JPEG, PSD, TIFF และ WMF

### คำถามที่ 2: ฉันจะจัดการกับตัวพิมพ์เริ่มต้นและตัวพิมพ์ใหญ่ที่แตกต่างกันสำหรับปากกาได้อย่างไร

 A2: ใช้`PenOptions` คลาสเพื่อกำหนดจุดเริ่มต้นและส่วนท้ายที่ต้องการ ซึ่งให้ความยืดหยุ่นในการกำหนดลักษณะที่ปรากฏของเส้น

### คำถามที่ 3: จะเกิดอะไรขึ้นหากฉันไม่ระบุตัวเลือกปากกา

A3: หากตัวเลือกปากกาไม่ได้ตั้งค่าไว้อย่างชัดเจน ระบบจะใช้ปากกาเริ่มต้น ซึ่งอาจแตกต่างกันในบริบทที่แตกต่างกัน

### คำถามที่ 4: มีข้อควรพิจารณาเฉพาะสำหรับตัวเลือกการแรสเตอร์หรือไม่

A4: ปรับความกว้างและความสูงของหน้าในตัวเลือกแรสเตอร์เพื่อควบคุมขนาดของภาพที่ส่งออก

### คำถามที่ 5: ฉันจะรับการสนับสนุนเพิ่มเติมหรือการสนทนาในชุมชนได้จากที่ไหน

 A5: สำรวจฟอรัมชุมชน Aspose.CAD ได้ที่[ที่นี่](https://forum.aspose.com/c/cad/19) สำหรับการสนับสนุนและการอภิปราย
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
