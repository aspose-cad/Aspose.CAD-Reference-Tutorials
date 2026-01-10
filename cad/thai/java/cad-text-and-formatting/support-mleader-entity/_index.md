---
date: 2026-01-10
description: เรียนรู้วิธีอ่านไฟล์ DWG และสร้างเอนทิตี multileader DWG ด้วย Aspose.CAD
  for Java ในบทแนะนำแบบขั้นตอนนี้
linktitle: Support MLeader Entity for DWG Format with Java
second_title: Aspose.CAD Java API
title: วิธีอ่าน DWG และสนับสนุน MLeader ด้วย Aspose.CAD สำหรับ Java
url: /th/java/cad-text-and-formatting/support-mleader-entity/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# วิธีอ่านไฟล์ DWG และสนับสนุน MLeader ด้วย Aspose.CAD สำหรับ Java

## คำนำ

หากคุณต้องการ **อ่านไฟล์ DWG ** และทำงานกับ **เอนทิตี้ DWG แบบ multileader** ในแอปพลิเคชัน Java คุณมาถูกที่แล้ว Aspose.CAD สำหรับ Java ให้วิธีการที่สะอาดและเป็นโปรแกรมเมติกในการเปิดไฟล์ DWG ตรวจสอบอ็อบเจ็กต์ MLeader และตรวจสอบคุณสมบัติต่าง ๆ — ทั้งหมดนี้โดยไม่ต้องใช้เครื่อง CAD เต็มรูปแบบ ในบทแนะนำนี้เราจะเดินผ่านทุกขั้นตอน ตั้งแต่การโหลดไฟล์ DWG ไปจนถึงการยืนยันว่าข้อมูล multileader ตรงกับสไตล์ที่คาดหวัง

## คำตอบสั้น
- **“วิธีอ่าน dwg” มีขั้นตอนอะไรบ้าง?** โหลด DWG ด้วย `Image.load()` แล้วแคสต์เป็น `CadImage`
- **ฉันสามารถสร้างเอนทิตี้ dwg แบบ multileader ได้หรือไม่?** ได้ — คุณสามารถเพิ่ม แก้ไข และตรวจสอบอ็อบเจ็กต์ MLeader ได้โดยใช้ API CadMLeader
- **ต้องใช้เวอร์ชันไลบรารีใด?** เวอร์ชัน Aspose.CAD สำหรับ Java ใดก็ได้ที่อัปเดต (API ที่แสดงทำงานกับบิลด์ 2024+)
- **ต้องมีลิขสิทธิ์สำหรับการพัฒนาหรือไม่?** ลิขสิทธิ์ชั่วคราวใช้สำหรับการทดสอบ; ต้องมีลิขสิทธิ์เต็มสำหรับการใช้งานจริง
- **โค้ดนี้เป็นข้ามแพลตฟอร์มหรือไม่?** แน่นอน — Java ทำงานบน Windows, Linux และ macOS

## “วิธีอ่าน dwg” กับ Aspose.CAD คืออะไร?

การอ่านไฟล์ DWG หมายถึงการแปลงภาพวาดไบนารีเป็นอ็อบเจ็กต์ `CadImage` ที่อยู่ในหน่วยความจำ เมื่อคุณมีอ็อบเจ็กต์นี้แล้ว คุณสามารถวนลูปตรวจสอบเอนทิตี้ต่าง ๆ (เส้น, วงกลม, ข้อความ, **MLeader** ฯลฯ) และตรวจสอบคุณสมบัติของมันได้

## ทำไมต้องสนับสนุนเอนทิตี้ MLeader?

อ็อบเจ็กต์ MLeader (multileader) รวมเส้นนำกับข้อความหรือบล็อกที่แนบไว้ ทำให้เป็นส่วนสำคัญสำหรับคำอธิบายในภาพวาดวิศวกรรม การสนับสนุนพวกมันทำให้คุณสามารถ:

- ตรวจสอบว่าคำอธิบายสอดคล้องกับมาตรฐานของบริษัท
- ดึงข้อความเพื่อประมวลผลต่อ (เช่น การสร้าง BOM)
- แก้ไขสไตล์ของ leader หรือเปลี่ยนเนื้อหาบล็อกโดยอัตโนมัติ

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะลงลึก โปรดตรวจสอบว่าคุณมี:

1. **สภาพแวดล้อมการพัฒนา Java** — JDK 11+ และ IDE ที่คุณชอบ (IntelliJ, Eclipse, VS Code)  
2. **Aspose.CAD สำหรับ Java** — ดาวน์โหลด JAR ล่าสุดจาก [download link](https://releases.aspose.com/cad/java/)  

## นำเข้า Namespaces

เพิ่มการนำเข้าต่อไปนี้ในคลาส Java ของคุณเพื่อให้ทำงานกับเอนทิตี้ DWG และตัวเลือกการเรสเตอร์ไลซ์ได้:

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

## วิธีอ่านไฟล์ DWG ด้วย Aspose.CAD สำหรับ Java

### ขั้นตอนที่ 1: โหลดไฟล์ DWG และรับ `CadImage`

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String file = dataDir + "Multileaders.dwg";
Image image = Image.load(file);
CadImage cadImage = (CadImage) image;
```

### ขั้นตอนที่ 2: ตรวจสอบว่าภาพวาดมีเอนทิตี้ MLeader หรือไม่

```java
Assert.areNotEqual(cadImage.getEntities().length, 0);
CadMLeader cadMLeader = (CadMLeader) cadImage.getEntities()[2];
```

### ขั้นตอนที่ 3: ตรวจสอบสไตล์ MLeader และแอตทริบิวต์พื้นฐาน

```java
Assert.areEqual(cadMLeader.getStyleDescription(), "Standard");
Assert.areEqual(cadMLeader.getLeaderStyleId(), "12E");
Assert.areEqual(cadMLeader.getArrowHeadId1(), "639");
Assert.areEqual(cadMLeader.getLeaderLineTypeID(), "14");
```

### ขั้นตอนที่ 4: เข้าถึงข้อมูลบริบทของ MLeader (หัวใจของ multileader)

```java
CadMLeaderContextData context = cadMLeader.getContextData();
```

### ขั้นตอนที่ 5: ตรวจสอบแอตทริบิวต์ระดับบริบท

```java
Assert.areEqual(context.getArrowHeadSize(), 30.0, 0.1);
Assert.areEqual(context.getBasePoint().getX(), 481, 1);
Assert.areEqual(context.getContentScale(), 1.0, 0.01);
Assert.areEqual(context.getDefaultText().getValue(),
    "This is multileader with huge text\\P{\\H1.5x;6666666666666666666666666666\\P}bbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbb");
Assert.areEqual(context.hasMText(), true);
```

### ขั้นตอนที่ 6: ทำงานกับโหนด MLeader และเส้นนำของมัน

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

### ขั้นตอนที่ 7: ตรวจสอบแอตทริบิวต์เพิ่มเติมของโหนด MLeader

```java
Assert.areEqual(Integer.toString(mleaderNode.getBranchIndex()), Integer.toString(0));
Assert.areEqual(mleaderNode.getDogLegLength(), 8.0, 0.1);
Assert.areEqual(context.hasMText(), true);
```

### ขั้นตอนที่ 8: ตรวจสอบคุณสมบัติเกี่ยวกับข้อความ

```java
Assert.areEqual(context.getTextAttachmentType().getValue(), (short) 1);
Assert.areEqual(context.getTextBackgroundColor().getValue(), 18);
Assert.areEqual(context.getTextHeight(), 20.0, 0.1);
Assert.areEqual(context.getTextStyleID().getValue(), "11");
Assert.areEqual(context.getTextRotation().getValue(), 0.0, 0.01);
```

### ขั้นตอนที่ 9: ตรวจสอบแอตทริบิวต์อื่น ๆ ของ MLeader เพื่อความสมบูรณ์

```java
Assert.areEqual(cadMLeader.getArrowHeadId1(), "639");
Assert.areEqual(cadMLeader.getLeaderType(), 1);
Assert.areEqual(cadMLeader.getBlockContentColor(), 0);
Assert.areEqual(cadMLeader.getLeaderLineColor(), 0);
Assert.areEqual(cadMLeader.getTextHeight(), 1.0, 0.01);
```

## ปัญหาที่พบบ่อยและวิธีแก้

| ปัญหา | สาเหตุ | วิธีแก้ |
|-------|--------|---------|
| `ClassCastException` เมื่อทำการแคสต์เอนทิตี้ | ดัชนีที่เลือกไม่ได้เป็นอ็อบเจ็กต์ MLeader | ตรวจสอบ `cadImage.getEntities()[i] instanceof CadMLeader` ก่อนทำการแคสต์ |
| ค่า `null` สำหรับจุดของเส้นนำ | ภาพวาดใช้สไตล์ leader แบบกำหนดเองที่ยังไม่รองรับเต็มที่ | ใช้เวอร์ชัน Aspose.CAD ล่าสุดหรือกลับไปใช้สไตล์เริ่มต้นสำหรับการทดสอบ |
| การตรวจสอบค่าตัวเลขล้มเหลว | ความแตกต่างของการปัดเศษระหว่างเวอร์ชัน CAD | ปรับค่าความทนทานใน `Assert.areEqual(..., delta)` ตามตัวอย่าง |

## คำถามที่พบบ่อย

**ถาม: ฉันสามารถใช้ Aspose.CAD สำหรับ Java กับรูปแบบ CAD อื่นได้หรือไม่?**  
ตอบ: ได้, Aspose.CAD รองรับ DXF, DWF, DGN และหลายรูปแบบราสเตอร์อื่น ๆ นอกเหนือจาก DWG

**ถาม: ฉันจะหาเอกสารรายละเอียดของ Aspose.CAD สำหรับ Java ได้จากที่ไหน?**  
ตอบ: ดูที่ [documentation](https://reference.aspose.com/cad/java/) อย่างเป็นทางการสำหรับรายละเอียด API และตัวอย่างโค้ด

**ถาม: มีรุ่นทดลองฟรีหรือไม่?**  
ตอบ: มีแน่นอน — คุณสามารถดาวน์โหลดรุ่นทดลองจากหน้า [free trial](https://releases.aspose.com/)  

**ถาม: จะขอรับลิขสิทธิ์ชั่วคราวสำหรับการทดสอบได้อย่างไร?**  
ตอบ: รับลิขสิทธิ์ชั่วคราวผ่าน [temporary license link](https://purchase.aspose.com/temporary-license/)  

**ถาม: จะสอบถามชุมชนเพื่อขอความช่วยเหลือได้ที่ไหน?**  
ตอบ: ฟอรั่ม [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) เป็นที่ดีที่สุดสำหรับการแชร์คำถามและวิธีแก้

## สรุป

คุณได้เรียนรู้วิธีอ่านไฟล์ DWG และ **สร้างเอนทิตี้ multileader DWG** อย่างครบถ้วนด้วย Aspose.CAD สำหรับ Java แล้ว โดยทำตามขั้นตอนข้างต้น คุณสามารถตรวจสอบสไตล์ MLeader, ดึงข้อมูลคำอธิบาย, และผสานการประมวลผล DWG เข้ากับเวิร์กโฟลว์ที่ใช้ Java ใด ๆ ได้

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2026-01-10  
**Tested With:** Aspose.CAD 24.11 for Java  
**Author:** Aspose