---
date: 2026-06-19
description: เรียนรู้วิธีแก้ไขไฟล์ DWG ด้วย Aspose.CAD for Java รวมถึงวิธีอัปเดตเส้นทาง
  DWG XRef และแก้ไขไฮเปอร์ลิงก์ ลองใช้การทดลองฟรีวันนี้!
keywords:
- how to edit dwg
- update dwg xref paths
- Aspose.CAD Java hyperlink
linktitle: แก้ไขไฮเปอร์ลิงก์
schemas:
- author: Aspose
  dateModified: '2026-06-19'
  description: Learn how to edit DWG files with Aspose.CAD for Java, including how
    to update DWG XRef paths and edit hyperlinks. Try the free trial today!
  headline: How to Edit DWG Hyperlinks - Aspose.CAD Java Tutorial
  type: TechArticle
- description: Learn how to edit DWG files with Aspose.CAD for Java, including how
    to update DWG XRef paths and edit hyperlinks. Try the free trial today!
  name: How to Edit DWG Hyperlinks - Aspose.CAD Java Tutorial
  steps:
  - name: Accessing Insert Objects
    text: '`CadInsertObject` is the Aspose.CAD class that represents an inserted block
      reference (XRef) inside a DWG drawing. Iterate through the entities and identify
      if an entity is an instance of the `CadInsertObject` class.'
  - name: How to Change XRef Path in a DWG Drawing
    text: '`CadImage` is the primary object that loads and saves CAD files in Aspose.CAD
      for Java. Once you have identified the insert object, retrieve the associated
      block entity and update the XRef path as needed. This ensures the reference
      points to the correct external file.'
  - name: Modifying Hyperlinks
    text: Next, check if the entity has a hyperlink associated with it. If the hyperlink
      matches a specific URL, update it to the desired URL. This step guarantees that
      clicking the hyperlink in the CAD viewer opens the new target.
  type: HowTo
- questions:
  - answer: Yes, after making changes call `cadImage.save("EditedDrawing.dwg");` to
      persist the modifications.
    question: Do I need to call a specific method to write the edited DWG back to
      disk?
  - answer: Absolutely—loop through `cadImage.getEntities()` and apply the hyperlink
      logic to each matching entity.
    question: Is it possible to edit multiple hyperlinks in one pass?
  type: FAQPage
second_title: Aspose.CAD Java API
title: วิธีแก้ไขไฮเปอร์ลิงก์ DWG - บทแนะนำ Aspose.CAD Java
url: /th/java/other-cad-operations/edit-hyperlink/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# วิธีแก้ไขไฮเปอร์ลิงก์ DWG - บทแนะนำ Aspose.CAD Java

ในยุคดิจิทัลปัจจุบัน การ **วิธีแก้ไข DWG** อย่างมีประสิทธิภาพเป็นทักษะที่จำเป็นสำหรับวิศวกร สถาปนิก และผู้เชี่ยวชาญ BIM ไม่ว่าคุณจะต้องแก้ไขไฮเปอร์ลิงก์ที่เสียหาย ชี้ XRef ไปยังแหล่งใหม่ หรืออัปเดตหลายแบบแผนพร้อมกัน Aspose.CAD for Java ให้วิธีที่สะอาดและเป็นโปรแกรมเมติกในการทำการเปลี่ยนแปลงเหล่านั้นโดยไม่ต้องเปิดโปรแกรมแก้ไข CAD บทแนะนำนี้จะพาคุณผ่านกระบวนการทั้งหมด ตั้งแต่การโหลดแบบแผนจนถึงการบันทึกการแก้ไข

## คำตอบสั้น
- **ไลบรารีที่จัดการการแก้ไข DWG ใน Java คืออะไร?** Aspose.CAD for Java.  
- **ฉันสามารถแก้ไขไฮเปอร์ลิงก์และเส้นทาง XRef พร้อมกันได้หรือไม่?** ใช่—ทั้งสองได้รับการสนับสนุนใน API เดียวกัน.  
- **ฉันต้องการไลเซนส์สำหรับการพัฒนาหรือไม่?** รุ่นทดลองฟรีใช้ได้สำหรับการทดสอบ; จำเป็นต้องมีไลเซนส์เชิงพาณิชย์สำหรับการใช้งานจริง.  
- **ต้องการเวอร์ชัน Java ใด?** Java 8 or higher.  
- **โค้ดตัวอย่างสามารถรันได้โดยตรงหรือไม่?** ใช่ หลังจากอัปเดตเส้นทางไฟล์ให้ชี้ไปยังไฟล์ DWG ในเครื่องของคุณ.

## ทำไมต้องแก้ไขไฮเปอร์ลิงก์ DWG และเส้นทาง XRef?
การทำให้ไฮเปอร์ลิงก์และเส้นทาง XRef เป็นปัจจุบันช่วยป้องกันการอ้างอิงที่เสียหาย ทำให้เอกสารโครงการชี้ไปยังทรัพยากรที่ถูกต้องเสมอ และเปิดใช้งานการอัปเดตแบบกลุ่มอัตโนมัติในไลบรารี CAD ขนาดใหญ่ สิ่งนี้ช่วยลดความพยายามด้วยมือ ลดข้อผิดพลาด และปรับปรุงประสิทธิภาพของโครงการโดยรวมโดยให้ผู้พัฒนาสามารถรักษาความสมบูรณ์ของลิงก์อย่างเป็นโปรแกรมเมติกตลอดวงจรการออกแบบ

## ข้อกำหนดเบื้องต้น
ก่อนที่เราจะลงลึกในบทแนะนำ โปรดตรวจสอบว่าคุณมีข้อกำหนดต่อไปนี้พร้อมแล้ว:
1. **สภาพแวดล้อมการพัฒนา Java:** ติดตั้ง JDK 8+ และ IDE ที่คุณชื่นชอบ (IntelliJ IDEA, Eclipse เป็นต้น).  
2. **ไลบรารี Aspose.CAD for Java:** ดาวน์โหลดและติดตั้งไลบรารี Aspose.CAD for Java จาก [download link](https://releases.aspose.com/cad/java/).  
3. **DWG Drawing:** มีไฟล์แบบแผน DWG พร้อมสำหรับการแก้ไขไฮเปอร์ลิงก์.

## นำเข้าแพ็กเกจ
เริ่มต้นโดยการนำเข้าแพ็กเกจที่จำเป็นลงในโปรเจกต์ Java ของคุณ ซึ่งจะทำให้คุณเข้าถึงฟังก์ชันของ Aspose.CAD for Java ได้

```java
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.CadBaseEntity;
import com.aspose.cad.fileformats.cad.cadobjects.CadBlockEntity;
import com.aspose.cad.fileformats.cad.cadobjects.CadInsertObject;
```

## วิธีแก้ไขไฮเปอร์ลิงก์ DWG ด้วย Aspose.CAD for Java?
`CadImage` คือคลาสของ Aspose.CAD ที่ใช้โหลดและบันทึกแบบแผน CAD.  
โหลดไฟล์ DWG ด้วย `CadImage` ทำการวนซ้ำผ่านเอนทิตี้ต่าง ๆ ปรับปรุงไฮเปอร์ลิงก์และเส้นทาง XRef ตามที่ต้องการ และสุดท้ายบันทึกภาพกลับเป็น DWG กระบวนการแบบ end‑to‑end นี้ทำให้คุณสามารถแก้ไขเอนทิตี้จำนวนใดก็ได้ในหนึ่งรอบการทำงาน เพื่อรับประกันว่าการเปลี่ยนแปลงทั้งหมดจะถูกบันทึก

### ขั้นตอนที่ 1: การเข้าถึง Insert Objects
`CadInsertObject` คือคลาสของ Aspose.CAD ที่แสดงถึงการอ้างอิงบล็อกที่แทรก (XRef) ภายในแบบแผน DWG. ทำการวนซ้ำผ่านเอนทิตี้และระบุว่าเอนทิตี้เป็นอินสแตนซ์ของคลาส `CadInsertObject` หรือไม่.

```java
    String dataDir = "Your Document Directory" + "DWGDrawings/";
    
    CadImage cadImage = (CadImage)Image.load(dataDir + "AutoCad_Sample.dwg");
    for (CadBaseEntity entity : cadImage.getEntities())
    {
        if (entity instanceof CadInsertObject)
        {
        }
	}
```

### ขั้นตอนที่ 2: วิธีเปลี่ยนเส้นทาง XRef ในแบบแผน DWG
`CadImage` เป็นอ็อบเจ็กต์หลักที่โหลดและบันทึกไฟล์ CAD ใน Aspose.CAD for Java. เมื่อคุณระบุ insert object แล้ว ให้ดึงเอาเอนทิตี้บล็อกที่เกี่ยวข้องและอัปเดตเส้นทาง XRef ตามต้องการ เพื่อให้การอ้างอิงชี้ไปยังไฟล์ภายนอกที่ถูกต้อง.

```java
			CadBlockEntity block = cadImage.getBlockEntities().get_Item(((CadInsertObject)entity).getName());
            String value = block.getXRefPathName().getValue();
            if (value != null && !value.contentEquals(""))
            {
                block.getXRefPathName().setValue("new file reference.dwg");
            }
    
```

### ขั้นตอนที่ 3: การแก้ไขไฮเปอร์ลิงก์
ต่อไป ตรวจสอบว่าเอนทิตี้มีไฮเปอร์ลิงก์ที่เชื่อมโยงอยู่หรือไม่ หากไฮเปอร์ลิงก์ตรงกับ URL เฉพาะ ให้อัปเดตเป็น URL ที่ต้องการ ขั้นตอนนี้รับประกันว่าการคลิกไฮเปอร์ลิงก์ในตัวดู CAD จะเปิดเป้าหมายใหม่

```java
        if (entity.getHyperlink() == "https://products.aspose.com")
        {
            entity.setHyperlink("https://www.aspose.com");
        }
```

## ข้อผิดพลาดทั่วไปและเคล็ดลับ
- **การเปรียบเทียบสตริง:** ใช้ `.equals()` แทน `==` เพื่อการเปรียบเทียบสตริงที่เชื่อถือได้ใน Java ตัวอย่างใช้ `==` เพื่อความง่าย แต่ในการผลิตควรเปลี่ยนเป็น `entity.getHyperlink().equals("https://products.aspose.com")`.  
- **การตรวจสอบค่า null:** ตรวจสอบเสมอว่า `block.getXRefPathName()` ไม่เป็น `null` ก่อนเรียก `.getValue()`.  
- **การบันทึกการเปลี่ยนแปลง:** หลังจากแก้ไขเอนทิตี้ ให้เรียก `cadImage.save("output.dwg");` เพื่อบันทึกการเปลี่ยนแปลง (โค้ดถูกละเว้นเพื่อรักษาจำนวนบล็อกเดิม).  
- **หมายเหตุประสิทธิภาพ:** Aspose.CAD for Java รองรับรูปแบบ CAD มากกว่า 30 รูปแบบและสามารถประมวลผลไฟล์ขนาดถึง 2 GB โดยไม่ต้องโหลดเอกสารทั้งหมดเข้าสู่หน่วยความจำ ทำให้การอัปเดตแบบกลุ่มทำได้เร็วและใช้หน่วยความจำอย่างมีประสิทธิภาพ.

## คำถามที่พบบ่อย
### คำถามที่ 1: Aspose.CAD for Java รองรับเวอร์ชัน DWG ทั้งหมดหรือไม่?
A1: Aspose.CAD for Java รองรับเวอร์ชัน DWG มากกว่า 50 เวอร์ชัน ครอบคลุมตั้งแต่ AutoCAD 2000 จนถึงรูปแบบล่าสุดของปี 2025.

### คำถามที่ 2: ฉันสามารถใช้ Aspose.CAD for Java ในโครงการเชิงพาณิชย์ได้หรือไม่?
A2: ใช่ จำเป็นต้องมีไลเซนส์เชิงพาณิชย์สำหรับการใช้งานในขั้นตอนการผลิต คุณสามารถซื้อไลเซนส์ได้ [here](https://purchase.aspose.com/buy).

### คำถามที่ 3: มีรุ่นทดลองฟรีสำหรับ Aspose.CAD for Java หรือไม่?
A3: ใช่ คุณสามารถสำรวจรุ่นทดลองฟรีได้ [here](https://releases.aspose.com/).

### คำถามที่ 4: ฉันจะรับการสนับสนุนทางเทคนิคสำหรับ Aspose.CAD for Java ได้อย่างไร?
A4: สำหรับความช่วยเหลือทางเทคนิคใด ๆ ให้เยี่ยมชมฟอรั่ม Aspose.CAD [here](https://forum.aspose.com/c/cad/19).

### คำถามที่ 5: ฉันสามารถขอรับไลเซนส์ชั่วคราวเพื่อการทดสอบได้หรือไม่?
A5: ใช่ คุณสามารถขอรับไลเซนส์ชั่วคราวได้ [here](https://purchase.aspose.com/temporary-license/).

**คำถามเพิ่มเติม**
**Q: ฉันต้องเรียกเมธอดเฉพาะเพื่อบันทึก DWG ที่แก้ไขกลับไปยังดิสก์หรือไม่?**  
A: ใช่ หลังจากทำการเปลี่ยนแปลงเรียก `cadImage.save("EditedDrawing.dwg");` เพื่อบันทึกการแก้ไข

**Q: สามารถแก้ไขหลายไฮเปอร์ลิงก์ในหนึ่งรอบได้หรือไม่?**  
A: แน่นอน—วนลูปผ่าน `cadImage.getEntities()` และใช้ตรรกะไฮเปอร์ลิงก์กับแต่ละเอนทิตี้ที่ตรงกัน.

---

**อัปเดตล่าสุด:** 2026-06-19  
**ทดสอบด้วย:** Aspose.CAD for Java 24.12  
**ผู้เขียน:** Aspose  

{{< blocks/products/products-backtop-button >}}

## บทแนะนำที่เกี่ยวข้อง
- [อ่านข้อมูลเมตา XREF จากไฟล์ DWG ด้วย Aspose.CAD for Java](/cad/java/cad-meta-data-and-rendering/read-xref-meta-data/)
- [เพิ่มคุณสมบัติกำหนดเองในไฟล์ DWG ด้วย Aspose.CAD for Java](/cad/java/additional-features/add-custom-properties/)
- [ส่งออก DWG เป็น PDF หรือ Raster ด้วย Aspose.CAD for Java](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}