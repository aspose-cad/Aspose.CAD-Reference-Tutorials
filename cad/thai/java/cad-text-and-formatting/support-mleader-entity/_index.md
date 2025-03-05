---
title: รองรับเอนทิตี MLeader สำหรับรูปแบบ DWG ด้วย Aspose.CAD สำหรับ Java
linktitle: รองรับเอนทิตี MLeader สำหรับรูปแบบ DWG ด้วย Java
second_title: Aspose.CAD Java API
description: ปลดล็อกพลังของ Aspose.CAD สำหรับ Java ด้วยบทช่วยสอนทีละขั้นตอนของเราเกี่ยวกับการสนับสนุนเอนทิตี MLeader ในรูปแบบ DWG
type: docs
weight: 12
url: /th/java/cad-text-and-formatting/support-mleader-entity/
---
## การแนะนำ

ในขอบเขตของการออกแบบโดยใช้คอมพิวเตอร์ช่วย (CAD) ด้วย Java การทำความเข้าใจและการใช้งานการสนับสนุนสำหรับเอนทิตี MLeader ในรูปแบบ DWG ถือเป็นทักษะที่มีคุณค่า Aspose.CAD สำหรับ Java มอบโซลูชันที่มีประสิทธิภาพสำหรับงานดังกล่าว โดยมีชุดเครื่องมือและฟังก์ชันการทำงานอันทรงพลัง บทช่วยสอนนี้จะแนะนำคุณตลอดกระบวนการรองรับเอนทิตี MLeader ภายในไฟล์ DWG โดยใช้ Java กับ Aspose.CAD

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเจาะลึกบทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

1. สภาพแวดล้อมการพัฒนา Java: ตรวจสอบให้แน่ใจว่าคุณได้ตั้งค่าสภาพแวดล้อมการพัฒนา Java ไว้ในระบบของคุณ

2.  ไลบรารี Aspose.CAD: ดาวน์โหลดและติดตั้งไลบรารี Aspose.CAD สำหรับ Java จาก[ลิ้งค์ดาวน์โหลด](https://releases.aspose.com/cad/java/).

## นำเข้าเนมสเปซ

ในโปรเจ็กต์ Java ของคุณ ให้นำเข้าเนมสเปซที่จำเป็นเพื่อใช้ประโยชน์จากความสามารถของ Aspose.CAD อย่างมีประสิทธิภาพ รวมบรรทัดต่อไปนี้ในรหัสของคุณ:

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.CadMLeader;
import com.aspose.cad.fileformats.cad.cadobjects.CadMLeaderContextData;
import com.aspose.cad.fileformats.cad.cadobjects.CadMLeaderLine;
import com.aspose.cad.fileformats.cad.cadobjects.CadMLeaderNode;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;

```

ตอนนี้ เราจะแจกแจงโค้ดออกเป็นคำแนะนำทีละขั้นตอนเพื่อรองรับเอนทิตี MLeader สำหรับรูปแบบ DWG โดยใช้ Java กับ Aspose.CAD

## 1. โหลดไฟล์ DWG และเข้าถึง CadImage

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String file = dataDir + "Multileaders.dwg";
Image image = Image.load(file);
CadImage cadImage = (CadImage) image;
```

## 2. ตรวจสอบเอนทิตี MLeader

```java
Assert.areNotEqual(cadImage.getEntities().length, 0);
CadMLeader cadMLeader = (CadMLeader) cadImage.getEntities()[2];
```

### 3. ตรวจสอบสไตล์และคุณสมบัติของ MLeader

```java
Assert.areEqual(cadMLeader.getStyleDescription(), "Standard");
Assert.areEqual(cadMLeader.getLeaderStyleId(), "12E");
Assert.areEqual(cadMLeader.getArrowHeadId1(), "639");
Assert.areEqual(cadMLeader.getLeaderLineTypeID(), "14");
```

## 4. เข้าถึงข้อมูลบริบทของ MLeader

```java
CadMLeaderContextData context = cadMLeader.getContextData();
```

## 5. ตรวจสอบแอตทริบิวต์บริบท

```java
Assert.areEqual(context.getArrowHeadSize(), 30.0, 0.1);
Assert.areEqual(context.getBasePoint().getX(), 481, 1);
Assert.areEqual(context.getContentScale(), 1.0, 0.01);
Assert.areEqual(context.getDefaultText().getValue(), "This is multileader with huge text\\P{\\H1.5x;6666666666666666666666666666\\P}bbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbb");
Assert.areEqual(context.hasMText(), true);
```

## 6. เข้าถึง MLeader Node และ Leader Line

```java
CadMLeaderNode mleaderNode = context.getLeaderNode();
Assert.areEqual(mleaderNode.getLastLeaderLinePoint().getX(), 473, 1);

CadMLeaderLine leaderLine = mleaderNode.getLeaderLine();
Assert.areEqual(leaderLine.getBreakEndPoint().toString(), null);
Assert.areEqual(Integer.toString(leaderLine.getBreakPointIndex().getValue()), Integer.toString(0));
Assert.areEqual(leaderLine.getBreakStartPoint().toString(), null);
Assert.areEqual(Integer.toString(leaderLine.getLeaderLineIndex().getValue()), Integer.toString(0));
Assert.areEqual(Integer.toString(leaderLine.getLeaderPoints().size()), Integer.toString(4));
```

## 7. ตรวจสอบคุณสมบัติ MLeader เพิ่มเติม

```java
Assert.areEqual(Integer.toString(mleaderNode.getBranchIndex()), Integer.toString(0));
Assert.areEqual(mleaderNode.getDogLegLength(), 8.0, 0.1);
Assert.areEqual(context.hasMText(), true);
```

## 8. ตรวจสอบคุณสมบัติข้อความ

```java
Assert.areEqual(context.getTextAttachmentType().getValue(), (short) 1);
Assert.areEqual(context.getTextBackgroundColor().getValue(), 18);
Assert.areEqual(context.getTextHeight(), 20.0, 0.1);
Assert.areEqual(context.getTextStyleID().getValue(), "11");
Assert.areEqual(context.getTextRotation().getValue(), 0.0, 0.01);
```

## 9. คุณสมบัติ MLeader เพิ่มเติม

```java
Assert.areEqual(cadMLeader.getArrowHeadId1(), "639");
Assert.areEqual(cadMLeader.getLeaderType(), 1);
Assert.areEqual(cadMLeader.getBlockContentColor(), 0);
Assert.areEqual(cadMLeader.getLeaderLineColor(), 0);
Assert.areEqual(cadMLeader.getTextHeight(), 1.0, 0.01);
```

## บทสรุป

ยินดีด้วย! คุณได้อ่านคำแนะนำที่ครอบคลุมเกี่ยวกับการสนับสนุนเอนทิตี MLeader สำหรับรูปแบบ DWG โดยใช้ Java และ Aspose.CAD เรียบร้อยแล้ว ความสามารถนี้เปิดประตูสู่การปรับแต่ง CAD ขั้นสูงและปรับปรุงชุดเครื่องมือการพัฒนา Java ของคุณ

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถใช้ Aspose.CAD สำหรับ Java กับรูปแบบ CAD อื่นๆ ได้หรือไม่

ตอบ 1: ใช่ Aspose.CAD รองรับรูปแบบ CAD ที่หลากหลายนอกเหนือจาก DWG ซึ่งให้ความคล่องตัวในโครงการของคุณ

### คำถามที่ 2: ฉันจะหาเอกสารโดยละเอียดสำหรับ Aspose.CAD สำหรับ Java ได้ที่ไหน

 A2: โปรดดูที่[เอกสารประกอบ](https://reference.aspose.com/cad/java/) สำหรับข้อมูลเชิงลึกเกี่ยวกับความสามารถของ Aspose.CAD

### คำถามที่ 3: มีการทดลองใช้ฟรีหรือไม่?

 A3: ใช่ สำรวจฟังก์ชันการทำงานโดยตรงด้วย[ทดลองฟรี](https://releases.aspose.com/).

### คำถามที่ 4: ฉันจะรับสิทธิ์การใช้งานชั่วคราวสำหรับ Aspose.CAD ได้อย่างไร

A4: รับใบอนุญาตชั่วคราวผ่าน[ลิงค์นี้](https://purchase.aspose.com/temporary-license/).

### คำถามที่ 5: ฉันสามารถขอรับการสนับสนุนและความช่วยเหลือจากชุมชนได้ที่ไหน?

A5: เยี่ยมชม[ฟอรั่ม Aspose.CAD](https://forum.aspose.com/c/cad/19) เพื่อเชื่อมต่อกับชุมชนและรับความช่วยเหลือ