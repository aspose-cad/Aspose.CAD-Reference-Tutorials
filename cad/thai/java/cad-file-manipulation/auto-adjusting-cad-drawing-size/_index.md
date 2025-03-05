---
title: การปรับขนาดการวาด CAD อัตโนมัติโดยใช้ Aspose.CAD สำหรับ Java
linktitle: การปรับขนาดการวาด CAD อัตโนมัติ
second_title: Aspose.CAD Java API
description: สำรวจกระบวนการที่ไร้รอยต่อของการปรับขนาดการวาด CAD อัตโนมัติใน Java โดยใช้ Aspose.CAD ปฏิบัติตามคำแนะนำทีละขั้นตอนของเราเพื่อการจัดการไฟล์ CAD ที่มีประสิทธิภาพ
type: docs
weight: 13
url: /th/java/cad-file-manipulation/auto-adjusting-cad-drawing-size/
---
## การแนะนำ

ในโลกของ CAD (Computer-Aided Design) การปรับขนาดภาพวาดเป็นข้อกำหนดทั่วไป และด้วย Aspose.CAD สำหรับ Java มันจะกลายเป็นกระบวนการที่ราบรื่น ไลบรารีอันทรงพลังนี้มีเครื่องมือที่ครอบคลุมสำหรับการจัดการไฟล์ CAD ในแอปพลิเคชัน Java ในบทช่วยสอนนี้ เราจะสำรวจกระบวนการปรับขนาดการวาด CAD อัตโนมัติแบบทีละขั้นตอนโดยใช้ Aspose.CAD

## ข้อกำหนดเบื้องต้น

ก่อนที่จะเข้าสู่บทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

1.  สภาพแวดล้อมการพัฒนา Java: ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้ง Java บนเครื่องของคุณ คุณสามารถดาวน์โหลดได้[ที่นี่](https://www.java.com/en/download/).

2.  ไลบรารี Aspose.CAD: ดาวน์โหลดและติดตั้งไลบรารี Aspose.CAD สำหรับ Java จาก[ที่นี่](https://releases.aspose.com/cad/java/).

3. ไฟล์ CAD ตัวอย่าง: มีไฟล์ CAD ตัวอย่าง (เช่น example.dwg) อยู่ในไดเร็กทอรีเอกสารของคุณ

## นำเข้าเนมสเปซ

ในแอปพลิเคชัน Java ของคุณ ให้รวมเนมสเปซที่จำเป็นเพื่อใช้ฟังก์ชันการทำงานของ Aspose.CAD นี่คือตัวอย่าง:

```java

import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

ตอนนี้ เรามาแจกแจงขั้นตอนการปรับขนาดการวาด CAD อัตโนมัติเป็นขั้นตอนที่สามารถจัดการได้

## ขั้นตอนที่ 1: โหลดแบบร่าง CAD

```java
String dataDir = "Your Document Directory" + "CADConversion/";
String sourceFilePath = dataDir + "sample.dwg";
Image objImage = Image.load(sourceFilePath);
```

ขั้นตอนนี้เกี่ยวข้องกับการโหลดแบบร่าง CAD จากเส้นทางไฟล์ที่ระบุ

## ขั้นตอนที่ 2: สร้าง BmpOptions

```java
BmpOptions bmpOptions = new BmpOptions();
```

 ยกตัวอย่าง`BmpOptions` ซึ่งจะใช้ตั้งค่าตัวเลือกต่างๆ สำหรับรูปแบบ BMP

## ขั้นตอนที่ 3: สร้าง CadRasterizationOptions

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
bmpOptions.setVectorRasterizationOptions(cadRasterizationOptions);
```

 สร้างอินสแตนซ์ของ`CadRasterizationOptions` เพื่อปรับแต่งการตั้งค่าแรสเตอร์สำหรับไฟล์ CAD

## ขั้นตอนที่ 4: ตั้งค่าคุณสมบัติเลย์เอาต์

```java
cadRasterizationOptions.setLayouts(new String[]{"Model"});
```

ระบุเค้าโครงที่คุณต้องการรวมไว้ในเอาต์พุต ในกรณีนี้ เราใช้เค้าโครง "โมเดล"

## ขั้นตอนที่ 5: ส่งออกเป็นรูปแบบ BMP

```java
String outPath = sourceFilePath + ".bmp";
objImage.save(outPath, bmpOptions);
```

สุดท้าย ให้บันทึกแบบร่าง CAD ที่ปรับแล้วในรูปแบบ BMP ไปยังเส้นทางเอาต์พุตที่ระบุ

ทำซ้ำขั้นตอนเหล่านี้ในแอปพลิเคชัน Java ของคุณ และคุณจะปรับขนาดการวาด CAD อัตโนมัติได้สำเร็จโดยใช้ Aspose.CAD สำหรับ Java

## บทสรุป

ในบทช่วยสอนนี้ เราได้อธิบายขั้นตอนการปรับขนาดการวาด CAD อัตโนมัติโดยใช้ Aspose.CAD สำหรับ Java ไลบรารีนี้ทำให้การจัดการไฟล์ CAD ง่ายขึ้น ซึ่งเป็นโซลูชันที่มีประสิทธิภาพสำหรับนักพัฒนา

## คำถามที่พบบ่อย

### คำถามที่ 1: Aspose.CAD สามารถใช้งานร่วมกับไฟล์ CAD ในรูปแบบต่างๆ ได้หรือไม่

A1: ใช่ Aspose.CAD รองรับรูปแบบ CAD หลากหลาย รวมถึง DWG, DXF, DGN และอื่นๆ

### คำถามที่ 2: ฉันสามารถใช้ Aspose.CAD สำหรับโครงการเชิงพาณิชย์ได้หรือไม่

 A2: แน่นอน! เยี่ยม[ที่นี่](https://purchase.aspose.com/buy) เพื่อสำรวจตัวเลือกการออกใบอนุญาต

### คำถามที่ 3: ฉันจะรับใบอนุญาตชั่วคราวเพื่อการทดสอบได้อย่างไร

 A3: รับใบอนุญาตชั่วคราว[ที่นี่](https://purchase.aspose.com/temporary-license/) เพื่อการทดสอบและประเมินผล

### คำถามที่ 4: ฉันจะรับการสนับสนุนสำหรับ Aspose.CAD ได้ที่ไหน

 A4: เข้าร่วมชุมชน Aspose.CAD[ฟอรั่ม](https://forum.aspose.com/c/cad/19) เพื่อขอความช่วยเหลือและหารือ

### คำถามที่ 5: Aspose.CAD สำหรับ Java มีรุ่นทดลองใช้ฟรีหรือไม่

 A5: ได้ คุณสามารถเข้าถึงรุ่นทดลองใช้ฟรีได้[ที่นี่](https://releases.aspose.com/) เพื่อสำรวจความสามารถของห้องสมุด