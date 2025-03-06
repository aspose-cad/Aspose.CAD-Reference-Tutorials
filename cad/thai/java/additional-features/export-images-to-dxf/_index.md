---
title: ส่งออกรูปภาพเป็นรูปแบบ DXF โดยใช้ Aspose.CAD สำหรับ Java
linktitle: ส่งออกรูปภาพเป็นรูปแบบ DXF โดยใช้ Java
second_title: Aspose.CAD Java API
description: สำรวจกระบวนการส่งออกรูปภาพเป็นรูปแบบ DXF ได้อย่างราบรื่นโดยใช้ Aspose.CAD สำหรับ Java คำแนะนำทีละขั้นตอน คำถามที่พบบ่อย และอื่นๆ อีกมากมาย
weight: 15
url: /th/java/additional-features/export-images-to-dxf/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# ส่งออกรูปภาพเป็นรูปแบบ DXF โดยใช้ Aspose.CAD สำหรับ Java

## การแนะนำ

ยินดีต้อนรับสู่บทช่วยสอนที่ครอบคลุมเกี่ยวกับการส่งออกรูปภาพเป็นรูปแบบ DXF โดยใช้ Aspose.CAD สำหรับ Java Aspose.CAD เป็นไลบรารี Java อันทรงพลังที่ช่วยให้นักพัฒนาสามารถทำงานกับภาพวาด CAD โดยทางโปรแกรม ในบทช่วยสอนนี้ เราจะแนะนำคุณตลอดขั้นตอนการส่งออกรูปภาพเป็นรูปแบบ DXF โดยสาธิตขั้นตอนและเทคนิคต่างๆ เพื่อให้งานนี้สำเร็จ

## ข้อกำหนดเบื้องต้น

ก่อนที่คุณจะเริ่มต้น ตรวจสอบให้แน่ใจว่าคุณมีสิ่งต่อไปนี้:

- ความเข้าใจพื้นฐานเกี่ยวกับการเขียนโปรแกรม Java
-  ติดตั้ง Aspose.CAD สำหรับไลบรารี Java แล้ว คุณสามารถดาวน์โหลดได้[ที่นี่](https://releases.aspose.com/cad/java/).
- ใบอนุญาตที่ถูกต้องหรือใบอนุญาตชั่วคราวสำหรับ Aspose.CAD รับมัน[ที่นี่](https://purchase.aspose.com/temporary-license/).
- ภาพตัวอย่างบางส่วนในรูปแบบ DXF สำหรับการทดสอบ

## นำเข้าเนมสเปซ

ในโปรเจ็กต์ Java ของคุณ ให้นำเข้าเนมสเปซที่จำเป็นสำหรับ Aspose.CAD:

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadconsts.CadEntityTypeName;
import com.aspose.cad.fileformats.cad.cadobjects.CadBaseEntity;
import com.aspose.cad.fileformats.cad.cadobjects.CadText;
import com.aspose.cad.fileformats.cad.cadtables.CadStyleTableObject;
import java.io.File;
import static java.lang.System.in;
```

## ขั้นตอนที่ 1: ตั้งค่าแบบอักษรใหม่ต่อเอกสาร

```java
// เส้นทางไปยังไดเร็กทอรีทรัพยากร
String dataDir = "Your Document Directory" + "DXFDrawings/";

File[] files = new File(dataDir).listFiles();
for (File file : files) {
    String extension = GetFileExtension(file);
    if (extension.equals(".dxf")) {
        CadImage cadImage = (CadImage)Image.load(file.getName());
        for (Object style : cadImage.getStyles()) {
            ((CadStyleTableObject)style).setPrimaryFontName("Broadway");
        }
        cadImage.save(file.getName() + "_font.dxf");
    }
}
```

## ขั้นตอนที่ 2: ซ่อนเส้น "ตรง" ทั้งหมด

```java
CadImage cadImageEntity = (CadImage)Image.load(file.getName());
for (CadBaseEntity entity : cadImageEntity.getEntities()) {
    if (entity.getTypeName() == CadEntityTypeName.LINE) {
        entity.setVisible((short)0);
    }
}
cadImageEntity.save(file.getName() + "_lines.dxf");
```

## ขั้นตอนที่ 3: การจัดการกับข้อความ

```java
CadImage cadImageText = (CadImage)Image.load(file.getName());
for (CadBaseEntity entity : cadImageText.getEntities()) {
    if (entity.getTypeName() == CadEntityTypeName.TEXT) {
        ((CadText)entity).setDefaultValue("New text here!!! :)");
        break;
    }
}
cadImageText.save(file.getName() + "_text.dxf");
```

ทำซ้ำขั้นตอนเหล่านี้สำหรับไฟล์ DXF แต่ละไฟล์ในไดเรกทอรีของคุณ

## บทสรุป

ยินดีด้วย! คุณได้เรียนรู้วิธีส่งออกรูปภาพเป็นรูปแบบ DXF โดยใช้ Aspose.CAD สำหรับ Java เรียบร้อยแล้ว บทช่วยสอนนี้ครอบคลุมขั้นตอนที่สำคัญ รวมถึงการตั้งค่าแบบอักษร การซ่อนบรรทัด และการจัดการข้อความภายในรูปภาพ CAD

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถใช้ Aspose.CAD สำหรับ Java โดยไม่มีใบอนุญาตได้หรือไม่

 A1: คุณสามารถใช้กับใบอนุญาตชั่วคราวที่มีอยู่ได้[ที่นี่](https://purchase.aspose.com/temporary-license/).

### คำถามที่ 2: ฉันจะหาเอกสารประกอบ Aspose.CAD ได้ที่ไหน

 A2: มีเอกสารประกอบให้[ที่นี่](https://reference.aspose.com/cad/java/).

### คำถามที่ 3: ฉันจะรับการสนับสนุนสำหรับ Aspose.CAD ได้อย่างไร

 A3: เยี่ยมชมฟอรั่มการสนับสนุน[ที่นี่](https://forum.aspose.com/c/cad/19).

### คำถามที่ 4: ฉันจะดาวน์โหลด Aspose.CAD สำหรับ Java ได้ที่ไหน

 A4: ดาวน์โหลดห้องสมุด[ที่นี่](https://releases.aspose.com/cad/java/).

### คำถามที่ 5: มีการทดลองใช้ฟรีหรือไม่?

 A5: ใช่ คุณสามารถทดลองใช้ฟรีได้[ที่นี่](https://releases.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
