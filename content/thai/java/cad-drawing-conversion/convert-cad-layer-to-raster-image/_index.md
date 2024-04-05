---
title: แปลงเลเยอร์ CAD เป็นรูปแบบภาพแรสเตอร์โดยใช้ Aspose.CAD สำหรับ Java
linktitle: แปลงเลเยอร์ CAD เป็นรูปแบบภาพแรสเตอร์
second_title: Aspose.CAD Java API
description: เรียนรู้วิธีแปลงเลเยอร์ CAD เป็นภาพแรสเตอร์ได้อย่างง่ายดายด้วย Aspose.CAD สำหรับ Java ปฏิบัติตามคำแนะนำทีละขั้นตอนของเราเพื่อการแสดงภาพเอกสารที่ราบรื่น
type: docs
weight: 11
url: /th/java/cad-drawing-conversion/convert-cad-layer-to-raster-image/
---
## การแนะนำ

ในขอบเขตของการออกแบบโดยใช้คอมพิวเตอร์ช่วย (CAD) ความสามารถในการแปลงเลเยอร์ CAD เป็นรูปแบบภาพแรสเตอร์ได้อย่างราบรื่นถือเป็นส่วนสำคัญของการจัดการเอกสารและการแสดงภาพ Aspose.CAD สำหรับ Java กลายเป็นเครื่องมือที่ทรงพลัง โดยมีฟังก์ชันการทำงานมากมายเพื่อปรับปรุงกระบวนการแปลงนี้ คำแนะนำทีละขั้นตอนนี้จะแนะนำคุณตลอดกระบวนการ เพื่อให้มั่นใจว่าคุณได้ใช้ประโยชน์จาก Aspose.CAD สำหรับ Java อย่างเต็มศักยภาพ

## ข้อกำหนดเบื้องต้น

ก่อนที่จะเข้าสู่บทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

- สภาพแวดล้อมการพัฒนา Java: ตรวจสอบให้แน่ใจว่าคุณได้ตั้งค่าสภาพแวดล้อมการพัฒนา Java บนเครื่องของคุณ

-  ไลบรารี Aspose.CAD: ดาวน์โหลดและติดตั้งไลบรารี Aspose.CAD สำหรับ Java จาก[ลิ้งค์ดาวน์โหลด](https://releases.aspose.com/cad/java/).

## นำเข้าเนมสเปซ

ในขั้นตอนนี้ เราจะนำเข้าเนมสเปซที่จำเป็นเพื่อเริ่มต้นกระบวนการ

### นำเข้าคลาส Aspose.CAD

ในโค้ด Java ของคุณ ให้รวมคลาส Aspose.CAD โดยใช้คำสั่งนำเข้าต่อไปนี้:

```java
import com.aspose.cad.Image;


import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
import java.util.ArrayList;
import java.util.Arrays;
import java.util.List;
```

## แปลงเลเยอร์ CAD เป็นรูปแบบภาพแรสเตอร์

ตอนนี้ เราจะแบ่งบทแนะนำออกเป็นหลายขั้นตอนเพื่อให้แน่ใจว่ากระบวนการแปลงจะราบรื่น

### ขั้นตอนที่ 1: ตั้งค่าไฟล์ CAD

เริ่มต้นด้วยการระบุเส้นทางไปยังไฟล์ CAD ของคุณและโหลดลงในอินสแตนซ์ของคลาส Image

```java
// เส้นทางไปยังไดเร็กทอรีทรัพยากร
String dataDir = "Your Document Directory" + "CADConversion/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

### ขั้นตอนที่ 2: กำหนดค่าตัวเลือกการแรสเตอร์

สร้างอินสแตนซ์ของ CadRasterizationOptions เพื่อกำหนดการตั้งค่าสำหรับการแรสเตอร์

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(500);
rasterizationOptions.setPageHeight(500);
```

### ขั้นตอนที่ 3: ระบุเลเยอร์ CAD

เพิ่มเลเยอร์ CAD ที่ต้องการลงในตัวเลือกการแรสเตอร์

```java
List<String> stringList = new ArrayList<>(Arrays.asList("0"));
rasterizationOptions.setLayers(stringList);
```

### ขั้นตอนที่ 4: ตั้งค่าตัวเลือก JPEG

สร้างอินสแตนซ์ของ JpegOptions (หรือ ImageOptions ใดๆ สำหรับรูปแบบแรสเตอร์) และลิงก์ไปยัง CadRasterizationOptions

```java
JpegOptions options = new JpegOptions();
options.setVectorRasterizationOptions(rasterizationOptions);
```

### ขั้นตอนที่ 5: ส่งออกเป็น JPEG

สุดท้าย ส่งออกแต่ละเลเยอร์เป็นรูปแบบ JPEG

```java
image.save(dataDir + "CADLayersToRasterImageFormats_out_.jpg", options);
```

ทำซ้ำขั้นตอนเหล่านี้สำหรับเลเยอร์เพิ่มเติมหรือปรับแต่งการตั้งค่าตามความต้องการของคุณ

## บทสรุป

ด้วยการทำตามคำแนะนำที่ครอบคลุมนี้ คุณได้ประสบความสำเร็จในการควบคุมความสามารถของ Aspose.CAD สำหรับ Java ในการแปลงเลเยอร์ CAD เป็นรูปแบบภาพแรสเตอร์ เครื่องมือนี้ช่วยให้คุณปรับปรุงการแสดงภาพและการจัดการเอกสารได้อย่างง่ายดาย

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถใช้ Aspose.CAD สำหรับ Java กับภาษาการเขียนโปรแกรมอื่นได้หรือไม่

คำตอบ 1: Aspose.CAD รองรับ Java เป็นหลัก แต่มีเวอร์ชันสำหรับภาษาอื่น เช่น .NET

### คำถามที่ 2: ฉันจะรับการสนับสนุนหรือความช่วยเหลือเพิ่มเติมได้จากที่ไหน

 A2: หากมีข้อสงสัยหรือความช่วยเหลือ โปรดไปที่[ฟอรั่ม Aspose.CAD](https://forum.aspose.com/c/cad/19).

### คำถามที่ 3: มีการทดลองใช้ฟรีหรือไม่?

 A3: ได้ คุณสามารถสำรวจ Aspose.CAD ได้โดยขอรับรุ่นทดลองใช้ฟรีจาก[ที่นี่](https://releases.aspose.com/).

### คำถามที่ 4: ฉันจะขอรับใบอนุญาตชั่วคราวสำหรับ Aspose.CAD ได้อย่างไร

 A4: รับใบอนุญาตชั่วคราวจาก[ลิงค์นี้](https://purchase.aspose.com/temporary-license/).

### คำถามที่ 5: มีข้อกำหนดระบบเฉพาะสำหรับ Aspose.CAD สำหรับ Java หรือไม่

A5: ตรวจสอบให้แน่ใจว่าคุณมีสภาพแวดล้อมการพัฒนา Java ที่เข้ากันได้ โปรดดูเอกสารประกอบสำหรับข้อกำหนดโดยละเอียด