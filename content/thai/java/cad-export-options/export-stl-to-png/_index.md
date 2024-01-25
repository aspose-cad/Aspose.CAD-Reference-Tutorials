---
title: ส่งออก STL เป็น PNG ด้วย Aspose.CAD สำหรับ Java
linktitle: ส่งออก STL เป็น PNG
second_title: Aspose.CAD Java API
description: สำรวจกระบวนการส่งออกไฟล์ STL ไปยัง PNG ใน Java ได้อย่างราบรื่นด้วย Aspose.CAD ลดความซับซ้อนของเวิร์กโฟลว์และปรับปรุงโปรเจ็กต์ Java ของคุณได้อย่างง่ายดาย
type: docs
weight: 20
url: /th/java/cad-export-options/export-stl-to-png/
---
## การแนะนำ

คุณต้องการส่งออกไฟล์ STL ไปยัง PNG โดยใช้ Java หรือไม่? Aspose.CAD สำหรับ Java คือโซลูชันที่คุณต้องการ! ในบทช่วยสอนนี้ เราจะแนะนำคุณตลอดกระบวนการทีละขั้นตอน ในฐานะนักเขียน SEO ที่เชี่ยวชาญ ฉันจะตรวจสอบให้แน่ใจว่าเนื้อหาไม่เพียงแต่ให้ข้อมูลเท่านั้น แต่ยังปรับให้เหมาะสมสำหรับเครื่องมือค้นหาด้วย

## ข้อกำหนดเบื้องต้น

ก่อนที่จะเข้าสู่บทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

- ติดตั้ง Java Development Kit (JDK) บนเครื่องของคุณแล้ว
-  ดาวน์โหลด Aspose.CAD สำหรับไลบรารี Java แล้ว คุณสามารถรับมันได้[ที่นี่](https://releases.aspose.com/cad/java/).
-  ใบอนุญาตที่ถูกต้องหรือใบอนุญาตชั่วคราวจาก[ที่นี่](https://purchase.aspose.com/temporary-license/).

## นำเข้าเนมสเปซ

ในโปรเจ็กต์ Java ของคุณ ให้นำเข้าเนมสเปซที่จำเป็น:

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

ตอนนี้ เรามาแบ่งตัวอย่างออกเป็นหลายขั้นตอนกัน

## ขั้นตอนที่ 1: ตั้งค่าโครงการของคุณ

สร้างโปรเจ็กต์ Java ใหม่และเพิ่มไลบรารี Aspose.CAD สำหรับ Java ไปยังการขึ้นต่อกันของโปรเจ็กต์ของคุณ

## ขั้นตอนที่ 2: ระบุไฟล์ STL ของคุณ

กำหนดเส้นทางไปยังไฟล์ STL ของคุณ ตัวอย่างเช่น:

```java
String dataDir = "Your Document Directory" + "ExportingSTL/";
String fileName = dataDir + "example.stl";
```

## ขั้นตอนที่ 3: โหลดไฟล์ STL

 โหลดไฟล์ STL โดยใช้นามสกุล`Image.load` วิธี:

```java
CadImage cadImage = (CadImage)Image.load(fileName);
```

## ขั้นตอนที่ 4: กำหนดค่าตัวเลือกการแรสเตอร์

ตั้งค่าตัวเลือกแรสเตอร์สำหรับการทำเวกเตอร์:

```java
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
```

## ขั้นตอนที่ 5: กำหนดค่าตัวเลือก PNG

ระบุตัวเลือกสำหรับการส่งออก PNG:

```java
PngOptions pngOptions = new PngOptions();
// ยกเลิกการใส่เครื่องหมายบรรทัดด้านล่างหากคุณต้องการตั้งค่าตัวเลือกการแรสเตอร์แบบเวกเตอร์
// pngOptions.setVectorRasterizationOptions(เวกเตอร์ตัวเลือก);
```

## ขั้นตอนที่ 6: บันทึกเป็น PNG

บันทึกภาพ CAD เป็นไฟล์ PNG:

```java
String outPath = dataDir + "galeon.stl.png";
cadImage.save(outPath, pngOptions);
```

ยินดีด้วย! คุณได้ส่งออกไฟล์ STL ไปยัง PNG โดยใช้ Aspose.CAD สำหรับ Java สำเร็จแล้ว

## บทสรุป

ในบทช่วยสอนนี้ เราได้สำรวจวิธีใช้ประโยชน์จาก Aspose.CAD สำหรับ Java เพื่อส่งออกไฟล์ STL เป็น PNG ได้อย่างง่ายดาย ไลบรารีอันทรงพลังนี้ทำให้งานที่ซับซ้อนง่ายขึ้น ทำให้เป็นทรัพย์สินที่มีค่าสำหรับโปรเจ็กต์ Java ของคุณ

## คำถามที่พบบ่อย

### คำถามที่ 1: Aspose.CAD สำหรับ Java เข้ากันได้กับไฟล์ STL ทุกเวอร์ชันหรือไม่

A1: Aspose.CAD สำหรับ Java รองรับไฟล์ STL เวอร์ชันต่างๆ เพื่อให้มั่นใจว่าสามารถเข้ากันได้กับรูปแบบทั่วไปส่วนใหญ่

### คำถามที่ 2: ฉันสามารถใช้ Aspose.CAD สำหรับ Java ในโครงการเชิงพาณิชย์ได้หรือไม่

 A2: ใช่คุณทำได้ เพียงได้รับใบอนุญาตที่ถูกต้องจาก[ที่นี่](https://purchase.aspose.com/buy).

### คำถามที่ 3: ฉันจำเป็นต้องมีใบอนุญาตชั่วคราวสำหรับการทดลองใช้ฟรีหรือไม่

 A3: ไม่ ไม่จำเป็นต้องมีใบอนุญาตชั่วคราวสำหรับการทดลองใช้ฟรี คุณสามารถเริ่มต้นใช้งานได้ทันทีด้วยเวอร์ชันทดลอง[ที่นี่](https://releases.aspose.com/).

### คำถามที่ 4: ฉันจะรับการสนับสนุนเพิ่มเติมหรือถามคำถามได้ที่ไหน

 A4: เยี่ยมชมฟอรั่ม Aspose.CAD[ที่นี่](https://forum.aspose.com/c/cad/19) สำหรับการสนับสนุนหรือข้อสงสัยใด ๆ

### คำถามที่ 5: มีเอกสารประกอบที่ครอบคลุมหรือไม่?

 A5: ใช่ สามารถดูเอกสารประกอบได้[ที่นี่](https://reference.aspose.com/cad/java/).