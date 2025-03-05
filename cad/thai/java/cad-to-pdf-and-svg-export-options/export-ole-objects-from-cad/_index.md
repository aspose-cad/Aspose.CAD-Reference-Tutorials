---
title: ส่งออกวัตถุ OLE จาก CAD โดยใช้ Aspose.CAD สำหรับ Java
linktitle: ส่งออกวัตถุ OLE จาก CAD
second_title: Aspose.CAD Java API
description: ปลดล็อกศักยภาพของ Aspose.CAD สำหรับ Java ส่งออกวัตถุ OLE จากไฟล์ CAD ได้อย่างง่ายดาย ดาวน์โหลดทันทีเพื่อการจัดการข้อมูล CAD ที่ราบรื่น
type: docs
weight: 10
url: /th/java/cad-to-pdf-and-svg-export-options/export-ole-objects-from-cad/
---
## การแนะนำ

ในโลกแบบไดนามิกของการออกแบบโดยใช้คอมพิวเตอร์ช่วย (CAD) การจัดการและการแยกวัตถุ OLE (การเชื่อมโยงและการฝังวัตถุ) อย่างมีประสิทธิภาพเป็นสิ่งสำคัญ Aspose.CAD สำหรับ Java มอบโซลูชันอันทรงพลังสำหรับการส่งออกอ็อบเจ็กต์ OLE จากไฟล์ CAD คำแนะนำทีละขั้นตอนนี้จะแนะนำคุณตลอดกระบวนการ เพื่อให้มั่นใจว่าคุณจะได้ใช้ประโยชน์จากศักยภาพสูงสุดของเครื่องมือนี้

## ข้อกำหนดเบื้องต้น

ก่อนที่จะเข้าสู่บทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

- สภาพแวดล้อม Java: ตรวจสอบให้แน่ใจว่าคุณได้ตั้งค่าสภาพแวดล้อมการพัฒนา Java บนเครื่องของคุณ
-  Aspose.CAD สำหรับ Java: ดาวน์โหลดและติดตั้งไลบรารี Aspose.CAD สำหรับ Java พบกับห้องสมุดได้ที่[ลิ้งค์ดาวน์โหลด](https://releases.aspose.com/cad/java/).
- ไฟล์ CAD: เตรียมไฟล์ CAD ที่มีวัตถุ OLE ที่คุณต้องการส่งออก

## นำเข้าเนมสเปซ

ในการเริ่มต้น ให้นำเข้าเนมสเปซที่จำเป็นลงในโปรเจ็กต์ Java ของคุณ เนมสเปซเหล่านี้มีคลาสและฟังก์ชันที่จำเป็นสำหรับการทำงานกับไฟล์ CAD โดยใช้ Aspose.CAD

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

ตอนนี้ เรามาแบ่งกระบวนการส่งออกวัตถุ OLE จาก CAD ออกเป็นหลายขั้นตอน:

## ขั้นตอนที่ 1: ตั้งค่าไดเร็กทอรีเอกสารของคุณ

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

ตรวจสอบให้แน่ใจว่าได้แทนที่ "Your Document Directory" ด้วยเส้นทางไปยังไดเร็กทอรีที่มีไฟล์ CAD ของคุณ

## ขั้นตอนที่ 2: กำหนดชื่อไฟล์ CAD

```java
String[] files = new String[] { "D ZD junior D10m H2m.dwg", "ZD - Senior D6m H2m45.dwg" };
```

 ระบุชื่อของไฟล์ CAD ที่คุณต้องการประมวลผลในรูปแบบ`files` อาร์เรย์

## ขั้นตอนที่ 3: ตั้งค่าตัวเลือกการส่งออก PNG

```java
PngOptions pngOptions = new PngOptions();
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
pngOptions.setVectorRasterizationOptions(rasterizationOptions);
rasterizationOptions.setLayouts(new String[] { "Layout1" });
```

กำหนดค่าตัวเลือกการส่งออก PNG รวมถึงการตั้งค่าแรสเตอร์เวกเตอร์และเค้าโครง

## ขั้นตอนที่ 4: วนซ้ำผ่านไฟล์ CAD

```java
for(String file : files)
{
    CadImage cadImage = (CadImage)Image.load(dataDir + file);
    cadImage.save(dataDir + file + "_out.png", pngOptions);
}
```

วนซ้ำไฟล์ CAD แต่ละไฟล์ที่ระบุ โหลดโดยใช้ Aspose.CAD และบันทึกวัตถุ OLE เป็นรูปภาพ PNG

## บทสรุป

ด้วยขั้นตอนที่เรียบง่ายแต่ทรงพลังเหล่านี้ คุณสามารถส่งออกออบเจ็กต์ OLE จากไฟล์ CAD ได้อย่างราบรื่นโดยใช้ Aspose.CAD สำหรับ Java เครื่องมืออเนกประสงค์นี้ช่วยให้นักพัฒนาสามารถจัดการข้อมูล CAD ได้อย่างมีประสิทธิภาพ โดยเปิดโอกาสใหม่ๆ ในการพัฒนาแอปพลิเคชัน CAD

## คำถามที่พบบ่อย

### คำถามที่ 1: Aspose.CAD เข้ากันได้กับไฟล์ CAD ทุกรูปแบบหรือไม่

 A1: Aspose.CAD รองรับรูปแบบ CAD หลากหลาย รวมถึง DWG, DXF และ DGN อ้างถึง[เอกสารประกอบ](https://reference.aspose.com/cad/java/) สำหรับรายการทั้งหมด

### คำถามที่ 2: ฉันสามารถกำหนดการตั้งค่าการส่งออกสำหรับวัตถุ OLE เองได้หรือไม่

ตอบ 2: ใช่ Aspose.CAD มีตัวเลือกมากมายสำหรับการปรับแต่งการตั้งค่าการส่งออก ซึ่งช่วยให้คุณปรับแต่งผลลัพธ์ตามความต้องการเฉพาะของคุณได้

### คำถามที่ 3: Aspose.CAD มีรุ่นทดลองใช้ฟรีหรือไม่

 A3: ได้ คุณสามารถสำรวจความสามารถของ Aspose.CAD ได้โดยการทดลองใช้ฟรีจาก[ที่นี่](https://releases.aspose.com/).

### คำถามที่ 4: ฉันจะรับการสนับสนุนจากชุมชนสำหรับ Aspose.CAD ได้ที่ไหน

 A4: เข้าร่วมชุมชน Aspose.CAD ที่[ฟอรั่ม](https://forum.aspose.com/c/cad/19) เพื่อขอความช่วยเหลือและแบ่งปันประสบการณ์ของคุณ

### คำถามที่ 5: ฉันจะซื้อใบอนุญาตสำหรับ Aspose.CAD ได้อย่างไร

A5: เยี่ยมชม[หน้าซื้อ](https://purchase.aspose.com/buy) เพื่อรับใบอนุญาตที่เหมาะสมกับความต้องการในการพัฒนาของคุณ