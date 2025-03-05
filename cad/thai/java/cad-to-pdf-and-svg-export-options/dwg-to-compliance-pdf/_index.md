---
title: DWG สู่การปฏิบัติตาม PDF โดยใช้ Aspose.CAD สำหรับ Java
linktitle: DWG สู่การปฏิบัติตามข้อกำหนด PDF
second_title: Aspose.CAD Java API
description: แปลงภาพวาด DWG เป็นไฟล์ที่รองรับ PDF/A1a และ PDF/A1b ได้อย่างง่ายดายโดยใช้ Aspose.CAD สำหรับ Java ปรับปรุงขั้นตอนการทำงานของคุณอย่างแม่นยำและง่ายดาย
type: docs
weight: 11
url: /th/java/cad-to-pdf-and-svg-export-options/dwg-to-compliance-pdf/
---
## การแนะนำ

ในโลกของการออกแบบดิจิทัลที่มีการพัฒนาอยู่ตลอดเวลา ความจำเป็นในการแปลงภาพวาด DWG เป็นรูปแบบ PDF ที่สอดคล้องถือเป็นสิ่งสำคัญสำหรับการทำงานร่วมกันที่ราบรื่นและเอกสารที่เป็นมาตรฐาน Aspose.CAD สำหรับ Java กลายเป็นเครื่องมืออันทรงพลังที่ให้ประสิทธิภาพและความแม่นยำในกระบวนการนี้ ในบทช่วยสอนนี้ เราจะสำรวจวิธีใช้ Aspose.CAD สำหรับ Java เพื่อแปลงไฟล์ DWG เป็น PDF ที่เป็นไปตามข้อกำหนดได้อย่างง่ายดาย เพื่อให้มั่นใจว่าเป็นไปตามมาตรฐาน PDF/A1a และ PDF/A1b

## ข้อกำหนดเบื้องต้น

ก่อนที่จะเข้าสู่บทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

- สภาพแวดล้อมการพัฒนา Java: ตรวจสอบให้แน่ใจว่าคุณได้ตั้งค่าสภาพแวดล้อมการพัฒนา Java ที่ใช้งานได้บนระบบของคุณ
-  ไลบรารี Aspose.CAD: ดาวน์โหลดและติดตั้งไลบรารี Aspose.CAD สำหรับ Java จาก[ลิ้งค์ดาวน์โหลด](https://releases.aspose.com/cad/java/).
- ไดเร็กทอรีเอกสาร: สร้างไดเร็กทอรีเพื่อจัดเก็บภาพวาด DWG ของคุณ

## นำเข้าเนมสเปซ

ในโปรเจ็กต์ Java ของคุณ ให้นำเข้าเนมสเปซที่จำเป็นเพื่อเข้าถึงฟังก์ชันการทำงานของ Aspose.CAD เพิ่มบรรทัดต่อไปนี้ที่จุดเริ่มต้นของไฟล์ Java ของคุณ:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfCompliance;
import com.aspose.cad.imageoptions.PdfDocumentOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## ขั้นตอนที่ 1: ตั้งค่าไดเรกทอรีทรัพยากร

กำหนดเส้นทางไปยังไดเรกทอรีทรัพยากรของคุณซึ่งจัดเก็บภาพวาด DWG

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

## ขั้นตอนที่ 2: โหลดไฟล์ DWG

โหลดไฟล์ DWG โดยใช้ไลบรารี Aspose.CAD

```java
String srcFile = dataDir + "Bottom_plate.dwg";
Image objImage = Image.load(srcFile);
```

## ขั้นตอนที่ 3: สร้างตัวเลือก PDF

สร้างอินสแตนซ์ของ PdfOptions และตั้งค่าตัวเลือกการแรสเตอร์เวกเตอร์

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(new CadRasterizationOptions());
```

## ขั้นตอนที่ 4: ตั้งค่าตัวเลือก Core PDF

ตั้งค่าตัวเลือก PDF หลัก โดยระบุมาตรฐานการปฏิบัติตามข้อกำหนด (PDF/A1a หรือ PDF/A1b)

```java
pdfOptions.setCorePdfOptions(new PdfDocumentOptions());
pdfOptions.getCorePdfOptions().setCompliance(PdfCompliance.PdfA1a);
```

## ขั้นตอนที่ 5: บันทึก PDF ด้วยการปฏิบัติตาม A1a

บันทึกไฟล์ PDF ตามมาตรฐาน A1a

```java
objImage.save(dataDir + "Saved1.pdf", pdfOptions);
```

## ขั้นตอนที่ 6: เปลี่ยนการปฏิบัติตามข้อกำหนดเป็น A1b

เปลี่ยนการปฏิบัติตามข้อกำหนดเป็น PDF/A1b และบันทึก PDF

```java
pdfOptions.getCorePdfOptions().setCompliance(PdfCompliance.PdfA1b);
objImage.save(dataDir + "Saved.pdf", pdfOptions);
```

ทำซ้ำขั้นตอนเหล่านี้กับไฟล์ DWG แต่ละไฟล์ที่คุณต้องการแปลง

## บทสรุป

โดยสรุป Aspose.CAD สำหรับ Java มอบโซลูชันที่มีประสิทธิภาพสำหรับการแปลงไฟล์ DWG เป็น PDF ตามมาตรฐาน ด้วยการทำตามคำแนะนำทีละขั้นตอนนี้ คุณสามารถปรับปรุงกระบวนการแปลงและรับรองว่าเอกสารของคุณเป็นไปตามมาตรฐานอุตสาหกรรม

## คำถามที่พบบ่อย

### คำถามที่ 1: Aspose.CAD เข้ากันได้กับไฟล์ DWG ทุกเวอร์ชันหรือไม่

 A1: Aspose.CAD รองรับไฟล์ DWG หลากหลายเวอร์ชัน รวมถึงเวอร์ชันล่าสุดด้วย อ้างถึง[เอกสารประกอบ](https://reference.aspose.com/cad/java/) สำหรับข้อมูลความเข้ากันได้โดยละเอียด

### คำถามที่ 2: ฉันสามารถปรับแต่งการตั้งค่าเอาต์พุต PDF โดยใช้ Aspose.CAD ได้หรือไม่

A2: แน่นอน! Aspose.CAD มีตัวเลือกมากมายสำหรับการปรับแต่ง ซึ่งช่วยให้คุณปรับแต่งเอาต์พุต PDF ตามความต้องการเฉพาะของคุณได้

### คำถามที่ 3: Aspose.CAD มีใบอนุญาตชั่วคราวหรือไม่

 A3: ได้ คุณสามารถขอรับใบอนุญาตชั่วคราวสำหรับการทดสอบได้จาก[ลิงค์นี้](https://purchase.aspose.com/temporary-license/).

### คำถามที่ 4: ฉันจะขอรับการสนับสนุนหรือโต้ตอบกับชุมชนสำหรับ Aspose.CAD ได้ที่ไหน

 A4: เยี่ยมชม[ฟอรั่ม Aspose.CAD](https://forum.aspose.com/c/cad/19) สำหรับการสนับสนุนและการอภิปรายของชุมชน

### คำถามที่ 5: ฉันสามารถทดลองใช้ Aspose.CAD ฟรีก่อนตัดสินใจซื้อได้หรือไม่

 A5: แน่นอน! ดาวน์โหลดเวอร์ชันทดลองใช้ฟรีได้ที่[ที่นี่](https://releases.aspose.com/) เพื่อสำรวจความสามารถก่อนตัดสินใจ