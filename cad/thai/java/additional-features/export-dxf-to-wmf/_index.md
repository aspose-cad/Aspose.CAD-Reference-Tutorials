---
title: ส่งออก DXF เป็นรูปแบบ WMF โดยใช้ Aspose.CAD ใน Java
linktitle: ส่งออก DXF เป็นรูปแบบ WMF โดยใช้ Java
second_title: Aspose.CAD Java API
description: ปลดล็อกพลังของ Aspose.CAD สำหรับ Java เรียนรู้วิธีส่งออกภาพวาด DXF เป็นรูปแบบ WMF ได้อย่างง่ายดายด้วยบทช่วยสอนโดยละเอียดของเรา ดาวน์โหลดไลบรารี ทำตามคำแนะนำทีละขั้นตอนของเรา และยกระดับการจัดการไฟล์ CAD ของคุณ
weight: 14
url: /th/java/additional-features/export-dxf-to-wmf/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# ส่งออก DXF เป็นรูปแบบ WMF โดยใช้ Aspose.CAD ใน Java

## การแนะนำ

ยินดีต้อนรับสู่คำแนะนำทีละขั้นตอนเกี่ยวกับการใช้ Aspose.CAD สำหรับ Java เพื่อส่งออกภาพวาด DXF เป็นรูปแบบ WMF Aspose.CAD เป็นไลบรารี Java ที่ทรงพลังซึ่งมีความสามารถมากมายสำหรับการทำงานกับไฟล์ CAD ในบทช่วยสอนนี้ เราจะแนะนำคุณตลอดขั้นตอนการแปลงไฟล์ DXF เป็นรูปแบบ WMF โดยใช้ Aspose.CAD

## ข้อกำหนดเบื้องต้น

ก่อนที่คุณจะเริ่มต้น ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

-  Aspose.CAD สำหรับ Java: ตรวจสอบให้แน่ใจว่าคุณมีไลบรารี Aspose.CAD ที่รวมอยู่ในโปรเจ็กต์ Java ของคุณ คุณสามารถดาวน์โหลดได้[ที่นี่](https://releases.aspose.com/cad/java/).

- ไดเร็กทอรีเอกสาร: ตั้งค่าไดเร็กทอรีเอกสารที่เก็บภาพวาด DXF ของคุณ

## นำเข้าเนมสเปซ

ในโปรเจ็กต์ Java ของคุณ ให้นำเข้าเนมสเปซที่จำเป็นเพื่อเข้าถึงฟังก์ชันการทำงานที่ Aspose.CAD มอบให้:

```java
import com.aspose.cad.Color;
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.ifc.IfcImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.WmfOptions;
```

## ขั้นตอนที่ 1: โหลดการวาด DXF

โหลดภาพวาด DXF ที่คุณต้องการส่งออกเป็นรูปแบบ WMF ตรวจสอบให้แน่ใจว่าระบุเส้นทางไปยังไฟล์ DXF อย่างถูกต้อง

```java
// เส้นทางไปยังไดเร็กทอรีทรัพยากร
String dataDir = "Your Document Directory" + "DXFDrawings/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

## ขั้นตอนที่ 2: กำหนดค่าตัวเลือกการแรสเตอร์

กำหนดค่าตัวเลือกการแรสเตอร์เพื่อกำหนดความกว้างและความสูงของหน้าเอาต์พุต ในตัวอย่างนี้ เราตั้งค่าความกว้างและความสูงของหน้าเป็น 100 หน่วย

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(100);
rasterizationOptions.setPageHeight(100);
WmfOptions wmfOptions = new WmfOptions();
```

## ขั้นตอนที่ 3: บันทึกเป็น WMF

บันทึกภาพวาด DXF ที่โหลดเป็นรูปแบบ WMF โดยใช้ตัวเลือกที่กำหนดค่าไว้

```java
cadImage.save(dataDir+" example.ifc.wmf", wmfOptions);
```

## ขั้นตอนที่ 4: กำจัดทรัพยากร

กำจัดทรัพยากรเพื่อเพิ่มหน่วยความจำและรับรองการจัดการทรัพยากรที่มีประสิทธิภาพ

```java
finally
{
  cadImage.dispose();
}
```

## ขั้นตอนที่ 5: ส่งออกเป็น PDF

หรือส่งออกภาพวาด DXF เป็นรูปแบบ PDF โดยใช้ Aspose.CAD

```java
image.save(dataDir + "conic_pyramid_out_.pdf"); 
```

ยินดีด้วย! คุณได้ส่งออกภาพวาด DXF เป็นรูปแบบ WMF โดยใช้ Aspose.CAD สำหรับ Java เรียบร้อยแล้ว

## บทสรุป

ในบทช่วยสอนนี้ เราได้สำรวจกระบวนการใช้ Aspose.CAD สำหรับ Java เพื่อส่งออกภาพวาด DXF เป็นรูปแบบ WMF ด้วยคุณสมบัติที่ครอบคลุมและใช้งานง่าย Aspose.CAD มอบโซลูชันที่เชื่อถือได้สำหรับการทำงานกับไฟล์ CAD ในโปรเจ็กต์ Java

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันจะหาเอกสาร Aspose.CAD ได้ที่ไหน

 A1: คุณสามารถเข้าถึงเอกสารประกอบได้[ที่นี่](https://reference.aspose.com/cad/java/).

### คำถามที่ 2: ฉันจะดาวน์โหลด Aspose.CAD สำหรับ Java ได้อย่างไร

 A2: ดาวน์โหลดไลบรารี[ที่นี่](https://releases.aspose.com/cad/java/).

### คำถามที่ 3: มีการทดลองใช้ฟรีหรือไม่?

A3: ใช่ คุณสามารถทดลองใช้ฟรีได้[ที่นี่](https://releases.aspose.com/).

### คำถามที่ 4: ต้องการตัวเลือกสิทธิ์การใช้งานชั่วคราวหรือไม่

 A4: สำรวจใบอนุญาตชั่วคราว[ที่นี่](https://purchase.aspose.com/temporary-license/).

### คำถามที่ 5: ฉันจะรับการสนับสนุนได้ที่ไหน?

 A5: เยี่ยมชมฟอรั่มสนับสนุน Aspose.CAD[ที่นี่](https://forum.aspose.com/c/cad/19).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
