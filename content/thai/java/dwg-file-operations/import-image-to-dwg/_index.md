---
title: นำเข้ารูปภาพไปยังไฟล์ DWG ได้อย่างง่ายดายโดยใช้ Aspose.CAD Java
linktitle: นำเข้ารูปภาพไปยังไฟล์ DWG โดยใช้ Java
second_title: Aspose.CAD Java API
description: สำรวจการรวมรูปภาพเข้ากับไฟล์ DWG ได้อย่างราบรื่นโดยใช้ Aspose.CAD สำหรับ Java ปฏิบัติตามคำแนะนำทีละขั้นตอนของเราเพื่อการพัฒนาที่มีประสิทธิภาพ
type: docs
weight: 10
url: /th/java/dwg-file-operations/import-image-to-dwg/
---
## การแนะนำ

ในโลกแบบไดนามิกของการพัฒนา Java การรวมรูปภาพเข้ากับไฟล์ DWG ได้กลายเป็นส่วนสำคัญของแอปพลิเคชันจำนวนมาก Aspose.CAD สำหรับ Java มอบโซลูชันที่มีประสิทธิภาพสำหรับนักพัฒนาที่กำลังมองหาวิธีการนำเข้ารูปภาพไปยังไฟล์ DWG ที่มีประสิทธิภาพ ในบทช่วยสอนนี้ เราจะแนะนำคุณตลอดกระบวนการทีละขั้นตอน เพื่อให้แน่ใจว่าจะรวมรูปภาพได้อย่างราบรื่นโดยใช้ Aspose.CAD สำหรับ Java

## ข้อกำหนดเบื้องต้น

ก่อนที่จะเข้าสู่บทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:
- Aspose.CAD สำหรับ Java: ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้งไลบรารี Aspose.CAD แล้ว คุณสามารถดาวน์โหลดได้[ที่นี่](https://releases.aspose.com/cad/java/).
- สภาพแวดล้อมการพัฒนา Java: ตั้งค่าสภาพแวดล้อมการพัฒนา Java ของคุณด้วยการกำหนดค่าที่จำเป็นทั้งหมด

## แพ็คเกจนำเข้า

ในการเริ่มต้น ให้นำเข้าแพ็คเกจ Aspose.CAD ที่จำเป็นลงในโปรเจ็กต์ Java ของคุณ:

```java
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.cad.CadDrawTypeMode;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.*;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## ขั้นตอนที่ 1: โหลดไฟล์ DWG และรูปภาพ

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String srcFile = dataDir + "Drawing11.dwg";
Image image = Image.load(srcFile);
```

## ขั้นตอนที่ 2: กำหนด CadRasterImage

```java
CadRasterImageDef cadRasterImageDef = new CadRasterImageDef("road-sign-custom.png", 640, 562);
cadRasterImageDef.setObjectHandle("A3B4");
```

## ขั้นตอนที่ 3: ตั้งค่าจุดแทรกและเวกเตอร์

```java
Cad3DPoint insertionPoint = new Cad3DPoint(26.77, 22.35);
Cad3DPoint uVector = new Cad3DPoint(0.0061565450840500831, 0);
Cad3DPoint vVector = new Cad3DPoint(0, 0.0061565450840500822);
```

## ขั้นตอนที่ 4: สร้างวัตถุ CadRasterImage

```java
CadRasterImage cadRasterImage = new CadRasterImage(cadRasterImageDef, insertionPoint, uVector, vVector);
cadRasterImage.setImageDefReference("A3B4");
cadRasterImage.setDisplayFlags((short)7);
cadRasterImage.setClippingState((short)0);
cadRasterImage.getClipBoundaryVertexList().add(new Cad2DPoint(-0.5, 0.5));
cadRasterImage.getClipBoundaryVertexList().add(new Cad2DPoint(639.5, 561.5));
```

## ขั้นตอนที่ 5: เพิ่มรูปภาพลงใน DWG

```java
CadImage cadImage = ((CadImage)(image));
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(cadRasterImage);
CadBaseObject[] objs = cadImage.getObjects();
CadBaseObject[] arr = new CadBaseObject[objs.length + 1];
int ind = 0;
for (CadBaseObject obj : objs)
{
    arr[ind] = obj;
    ind++;
}
arr[ind] = cadRasterImageDef;
cadImage.setObjects(arr);
```

## ขั้นตอนที่ 6: ตั้งค่าตัวเลือก PDF

```java
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setDrawType(CadDrawTypeMode.UseObjectColor);
cadRasterizationOptions.setPageHeight(1600);
cadRasterizationOptions.setPageWidth(1600);
cadRasterizationOptions.setLayouts(new String[] {"Model"});
```

## ขั้นตอนที่ 7: บันทึก PDF

```java
image.save((srcFile + "_generated.pdf"), pdfOptions);
```

เมื่อทำตามขั้นตอนเหล่านี้ คุณจะสามารถนำเข้ารูปภาพไปยังไฟล์ DWG ได้อย่างง่ายดายโดยใช้ Aspose.CAD สำหรับ Java

## บทสรุป

โดยสรุป Aspose.CAD สำหรับ Java ช่วยให้นักพัฒนา Java สามารถปรับปรุงแอปพลิเคชันของตนได้โดยการผสานรวมรูปภาพลงในไฟล์ DWG ได้อย่างราบรื่น คำแนะนำทีละขั้นตอนช่วยให้มั่นใจได้ถึงการใช้งานฟีเจอร์นี้อย่างราบรื่นและมีประสิทธิภาพ

## คำถามที่พบบ่อย

### คำถามที่ 1: Aspose.CAD สำหรับ Java เข้ากันได้กับสภาพแวดล้อมการพัฒนา Java ทั้งหมดหรือไม่

ตอบ 1: ใช่ Aspose.CAD สำหรับ Java เข้ากันได้กับสภาพแวดล้อมการพัฒนา Java ส่วนใหญ่

### คำถามที่ 2: ฉันสามารถใช้ Aspose.CAD สำหรับ Java สำหรับโครงการเชิงพาณิชย์ได้หรือไม่

 A2: ได้ คุณสามารถใช้ Aspose.CAD สำหรับ Java สำหรับโครงการเชิงพาณิชย์ได้ เยี่ยม[ที่นี่](https://purchase.aspose.com/buy) สำหรับรายละเอียดใบอนุญาต

### คำถามที่ 3: Aspose.CAD สำหรับ Java มีรุ่นทดลองใช้ฟรีหรือไม่

 A3: ได้ คุณสามารถเข้าถึงรุ่นทดลองใช้ฟรีได้[ที่นี่](https://releases.aspose.com/).

### คำถามที่ 4: ฉันจะรับการสนับสนุนสำหรับ Aspose.CAD สำหรับ Java ได้อย่างไร

 A4: คุณสามารถขอรับการสนับสนุนได้ที่[ฟอรั่ม Aspose.CAD](https://forum.aspose.com/c/cad/19).

### คำถามที่ 5: ฉันสามารถขอรับใบอนุญาตชั่วคราวสำหรับ Aspose.CAD สำหรับ Java ได้หรือไม่

 A5: ได้ คุณสามารถขอรับใบอนุญาตชั่วคราวได้[ที่นี่](https://purchase.aspose.com/temporary-license/).