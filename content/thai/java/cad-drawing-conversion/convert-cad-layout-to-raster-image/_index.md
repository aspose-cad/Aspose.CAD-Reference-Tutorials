---
title: แปลงเค้าโครง CAD เป็นรูปแบบภาพแรสเตอร์โดยใช้ Aspose.CAD สำหรับ Java
linktitle: แปลงเค้าโครง CAD เป็นรูปแบบภาพแรสเตอร์
second_title: Aspose.CAD Java API
description: แปลงเค้าโครง CAD เป็นภาพแรสเตอร์ได้อย่างง่ายดายโดยใช้ Aspose.CAD สำหรับ Java การสร้างภาพข้อมูลคุณภาพสูงเพื่อการทำงานร่วมกันที่ดียิ่งขึ้น
type: docs
weight: 12
url: /th/java/cad-drawing-conversion/convert-cad-layout-to-raster-image/
---
## การแนะนำ

ในโลกแบบไดนามิกของการออกแบบโดยใช้คอมพิวเตอร์ช่วย (CAD) ความสามารถในการแปลงเค้าโครง CAD เป็นรูปแบบภาพแรสเตอร์ได้อย่างราบรื่นถือเป็นทักษะที่มีคุณค่า Aspose.CAD สำหรับ Java กลายเป็นโซลูชันที่มีประสิทธิภาพเพื่อให้บรรลุงานนี้ได้อย่างมีประสิทธิภาพ ในบทช่วยสอนนี้ เราจะแนะนำคุณตลอดขั้นตอนการแปลงเค้าโครง CAD เป็นรูปภาพแรสเตอร์ทีละขั้นตอน โดยใช้ Aspose.CAD สำหรับ Java

## ข้อกำหนดเบื้องต้น

ก่อนที่จะเข้าสู่บทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

1. สภาพแวดล้อมการพัฒนา Java: ตรวจสอบให้แน่ใจว่าคุณมีสภาพแวดล้อมการพัฒนา Java ที่ใช้งานได้ติดตั้งอยู่ในระบบของคุณ

2.  ไลบรารี Aspose.CAD: ดาวน์โหลดและติดตั้งไลบรารี Aspose.CAD คุณสามารถรับได้จาก[Aspose.CAD สำหรับเอกสาร Java](https://reference.aspose.com/cad/java/).

## นำเข้าเนมสเปซ

เริ่มต้นด้วยการนำเข้าเนมสเปซที่จำเป็นเพื่อใช้ฟังก์ชันการทำงานของ Aspose.CAD สำหรับ Java ในโค้ด Java ของคุณ ให้รวมเนมสเปซต่อไปนี้:

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

ตอนนี้ เราจะแจกแจงโค้ดตัวอย่างออกเป็นชุดขั้นตอนในการแปลงเค้าโครง CAD ให้เป็นภาพแรสเตอร์
## ขั้นตอนที่ 1: ตั้งค่าไดเรกทอรีทรัพยากร

```java
// เส้นทางไปยังไดเร็กทอรีทรัพยากร
String dataDir = "Your Document Directory" + "CADConversion/";
```

ตรวจสอบให้แน่ใจว่าได้แทนที่ "Your Document Directory" ด้วยเส้นทางไปยังไดเร็กทอรีเอกสารจริงของคุณ

## ขั้นตอนที่ 2: โหลดไฟล์ CAD

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

ระบุเส้นทางไปยังไฟล์ CAD ของคุณ และโหลดโดยใช้ Aspose.CAD

## ขั้นตอนที่ 3: กำหนดค่าตัวเลือกการแรสเตอร์

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1200);
rasterizationOptions.setPageHeight(1200);
rasterizationOptions.setLayouts(new String[] {"Model", "Layout1"});
```

 สร้างอินสแตนซ์ของ`CadRasterizationOptions` และกำหนดขนาดและเค้าโครงหน้า

## ขั้นตอนที่ 4: ตั้งค่าตัวเลือกรูปภาพ

```java
ImageOptionsBase options = new TiffOptions(TiffExpectedFormat.Default);
options.setVectorRasterizationOptions(rasterizationOptions);
```

 สร้างอินสแตนซ์ของ`ImageOptions` และเชื่อมโยงกับตัวเลือกการแรสเตอร์

## ขั้นตอนที่ 5: บันทึกรูปภาพผลลัพธ์

```java
image.save(dataDir + "conic_pyramid_layoutstorasterimage_out_.tiff", options);
```

บันทึกภาพแรสเตอร์สุดท้ายในรูปแบบและตำแหน่งที่ต้องการ

ทำซ้ำขั้นตอนเหล่านี้ โดยปรับพารามิเตอร์ตามความจำเป็น เพื่อปรับแต่งการแปลงตามความต้องการเฉพาะของคุณ

## บทสรุป

Aspose.CAD สำหรับ Java ปรับปรุงกระบวนการแปลงเค้าโครง CAD เป็นภาพแรสเตอร์ ให้ความยืดหยุ่นและความแม่นยำ การใช้เทคนิคนี้อย่างเชี่ยวชาญจะช่วยเพิ่มความเป็นไปได้ในการแสดงภาพข้อมูลและการทำงานร่วมกันในโครงการ CAD ได้อย่างมีประสิทธิภาพ

## คำถามที่พบบ่อย

### คำถามที่ 1: Aspose.CAD สามารถใช้งานร่วมกับไฟล์ CAD ในรูปแบบต่างๆ ได้หรือไม่

A1: ใช่ Aspose.CAD รองรับรูปแบบ CAD ที่หลากหลาย รวมถึง DWG, DXF และ DGN

### คำถามที่ 2: ฉันสามารถปรับแต่งความละเอียดของภาพแรสเตอร์เอาท์พุตได้หรือไม่

 A2: แน่นอน. ปรับ`setPageWidth` และ`setPageHeight` พารามิเตอร์ใน`CadRasterizationOptions` เพื่อความละเอียดที่ต้องการ

### คำถามที่ 3: ฉันจะแปลงเค้าโครง CAD หลาย ๆ แบบพร้อมกันได้อย่างไร

 A3: เพียงขยายอาร์เรย์ที่ส่งผ่านไป`setLayouts` พร้อมชื่อของเค้าโครงที่คุณต้องการแปลง

### คำถามที่ 4: มีรูปแบบเอาต์พุตอื่นนอกเหนือจาก TIFF หรือไม่

A4: ใช่ Aspose.CAD รองรับรูปแบบเอาต์พุตที่หลากหลาย เช่น PNG, JPG และ PDF

### คำถามที่ 5: ฉันจะขอความช่วยเหลือหรือแบ่งปันประสบการณ์ของฉันกับ Aspose.CAD ได้ที่ไหน

A5: เยี่ยมชม[ฟอรั่ม Aspose.CAD](https://forum.aspose.com/c/cad/19) เพื่อมีส่วนร่วมกับชุมชนและรับการสนับสนุน