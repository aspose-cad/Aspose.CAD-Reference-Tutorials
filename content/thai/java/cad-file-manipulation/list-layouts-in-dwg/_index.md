---
title: แสดงรายการเค้าโครงใน DWG โดยใช้ Aspose.CAD สำหรับ Java
linktitle: แสดงรายการเค้าโครงใน DWG
second_title: Aspose.CAD Java API
description: สำรวจ Aspose.CAD สำหรับ Java และแสดงรายการเค้าโครงในไฟล์ DWG ได้อย่างง่ายดาย รวมฟังก์ชัน CAD อันทรงพลังเข้ากับแอปพลิเคชัน Java ของคุณ
type: docs
weight: 12
url: /th/java/cad-file-manipulation/list-layouts-in-dwg/
---
## การแนะนำ

ยินดีต้อนรับสู่คำแนะนำทีละขั้นตอนเกี่ยวกับการใช้ Aspose.CAD สำหรับ Java เพื่อแสดงรายการเค้าโครงในไฟล์ DWG Aspose.CAD เป็นไลบรารีอันทรงพลังที่ช่วยให้นักพัฒนาสามารถทำงานกับไฟล์ CAD โดยทางโปรแกรม ในบทช่วยสอนนี้ เราจะเน้นไปที่งานเฉพาะ: การแสดงเค้าโครงในไฟล์ DWG เมื่อสิ้นสุดคู่มือนี้ คุณจะสามารถรวมฟังก์ชันการทำงานนี้เข้ากับแอปพลิเคชัน Java ของคุณได้อย่างราบรื่น

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเจาะลึกบทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

-  Aspose.CAD สำหรับไลบรารี Java: ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้งไลบรารี Aspose.CAD สำหรับ Java แล้ว คุณสามารถดาวน์โหลดได้จาก[เว็บไซต์](https://releases.aspose.com/cad/java/).

- สภาพแวดล้อมการพัฒนา Java: ตั้งค่าสภาพแวดล้อมการพัฒนา Java บนเครื่องของคุณ

## นำเข้าเนมสเปซ

ในแอปพลิเคชัน Java ของคุณ คุณต้องนำเข้าเนมสเปซที่จำเป็นเพื่อใช้ Aspose.CAD เพิ่มบรรทัดต่อไปนี้ที่จุดเริ่มต้นของไฟล์ Java ของคุณ:

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.CadLayoutDictionary;
import com.aspose.cad.fileformats.cad.cadobjects.CadLayout;
```

## ขั้นตอนที่ 1: ตั้งค่าไดเร็กทอรีเอกสารของคุณ

```java
String dataDir = "Your Document Directory" + "CADConversion/";
```

ตรวจสอบให้แน่ใจว่าได้แทนที่ "Your Document Directory" ด้วยเส้นทางไปยังไดเร็กทอรีที่เก็บไฟล์ CAD ของคุณ

## ขั้นตอนที่ 2: โหลดไฟล์ DWG

```java
String sourceFilePath = dataDir + "conic_pyramid.dxf";
Image image = Image.load(sourceFilePath);
CadImage cadImage = (CadImage)image;
```

โหลดไฟล์ DWG โดยใช้เส้นทางไฟล์ที่ระบุ

## ขั้นตอนที่ 3: รับเลย์เอาต์และชื่อการพิมพ์

```java
CadLayoutDictionary layouts = cadImage.getLayouts();
for (CadLayout layout : layouts.getValues())
{
    System.out.println("Layout " + layout.getLayoutName());
}
```

ดึงเค้าโครงจากไฟล์ DWG และพิมพ์ชื่อไปยังคอนโซล

## บทสรุป

 ยินดีด้วย! คุณได้แสดงรายการเค้าโครงในไฟล์ DWG โดยใช้ Aspose.CAD สำหรับ Java เรียบร้อยแล้ว บทช่วยสอนนี้ครอบคลุมขั้นตอนสำคัญ ตั้งแต่การตั้งค่าสภาพแวดล้อมไปจนถึงการพิมพ์ชื่อโครงร่าง รู้สึกอิสระที่จะสำรวจคุณสมบัติเพิ่มเติมของ Aspose.CAD สำหรับ Java ใน[เอกสารประกอบ](https://reference.aspose.com/cad/java/).

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถใช้ Aspose.CAD สำหรับ Java กับไฟล์ CAD รูปแบบอื่นได้หรือไม่

A1: ใช่ Aspose.CAD รองรับรูปแบบ CAD หลากหลาย รวมถึง DWG, DXF, DWF และอื่นๆ

### คำถามที่ 2: Aspose.CAD สำหรับ Java มีรุ่นทดลองใช้ฟรีหรือไม่

 A2: ได้ คุณสามารถขอรับรุ่นทดลองใช้ฟรีได้จาก[ที่นี่](https://releases.aspose.com/).

### คำถามที่ 3: ฉันจะรับการสนับสนุนชุมชนสำหรับ Aspose.CAD สำหรับ Java ได้ที่ไหน

 A3: เยี่ยมชม[ฟอรั่ม Aspose.CAD](https://forum.aspose.com/c/cad/19) เพื่อสนับสนุนชุมชน

### คำถามที่ 4: ฉันจะซื้อใบอนุญาตสำหรับ Aspose.CAD สำหรับ Java ได้อย่างไร

 A4: คุณสามารถซื้อใบอนุญาตได้จาก[หน้าซื้อ](https://purchase.aspose.com/buy).

### คำถามที่ 5: ฉันสามารถใช้ใบอนุญาตชั่วคราวเพื่อการทดสอบได้หรือไม่

 A5: ได้ คุณสามารถขอรับใบอนุญาตชั่วคราวได้[ที่นี่](https://purchase.aspose.com/temporary-license/).