---
date: 2026-01-02
description: เรียนรู้วิธีการเปลี่ยนแบบอักษรในไฟล์ DWG ด้วย Aspose.CAD สำหรับ Java
  คู่มือขั้นตอนต่อขั้นตอนสำหรับการปรับแต่งสไตล์อย่างแม่นยำ.
linktitle: Substitute Font of a Particular Style in DWG
second_title: Aspose.CAD Java API
title: วิธีเปลี่ยนฟอนต์ของสไตล์เฉพาะใน DWG ด้วย Aspose.CAD สำหรับ Java
url: /th/java/cad-text-and-annotation/substitute-font-of-particular-style-in-dwg/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# วิธีการแทนที่ฟอนต์ของสไตล์เฉพาะใน DWG ด้วย Aspose.CAD for Java

## บทนำ

ในโลกของ CAD (Computer-Aided Design) ความแม่นยำและรายละเอียดเป็นสิ่งสำคัญ, และ **การรู้วิธีแทนที่ฟอนต์** ในภาพวาดสามารถช่วยคุณประหยัดเวลานับไม่ถ้วนจากการทำงานซ้ำ. Aspose.CAD for Java มอบวิธีที่สะอาดและโปรแกรมเมติกให้กับนักพัฒนาในการแก้ไขไฟล์ DWG, รวมถึงความสามารถในการเปลี่ยนฟอนต์ของสไตล์ข้อความเฉพาะ. ในบทแนะนำนี้เราจะพาคุณผ่านขั้นตอนที่แม่นยำเพื่อแทนที่ฟอนต์ของสไตล์เฉพาะในไฟล์ DWG, อธิบายเหตุผลที่คุณอาจต้องทำเช่นนั้น, และแสดงวิธีตรวจสอบผลลัพธ์.

## คำตอบสั้น

- **“replace font” หมายถึงอะไรใน DWG?** การเปลี่ยนฟอนต์หลักที่เชื่อมโยงกับการกำหนดสไตล์ข้อความ.  
- **ไลบรารีที่จัดการเรื่องนี้คืออะไร?** Aspose.CAD for Java.  
- **ฉันต้องการไลเซนส์หรือไม่?** ทดลองฟรีใช้ได้สำหรับการทดสอบ; ต้องมีไลเซนส์เชิงพาณิชย์สำหรับการใช้งานจริง.  
- **ฉันสามารถเปลี่ยนหลายสไตล์พร้อมกันได้หรือไม่?** ได้ – ทำการวนลูปผ่านคอลเลกชันสไตล์และตั้งค่าฟอนต์แต่ละอัน.  
- **โค้ดนี้เข้ากันได้กับ Java 8+ หรือไม่?** แน่นอน, API รองรับ Java 8 และรุ่นใหม่กว่า.

## ฟอนต์รีเพลสเมนท์ใน DWG คืออะไร?

ฟอนต์รีเพลสเมนท์หมายถึงการอัปเดตคุณสมบัติ *primary font* ของสไตล์ข้อความ (ซึ่งบางครั้งเรียกว่า “style” ในศัพท์ของ DWG). เมื่อภาพวาดอ้างอิงสไตล์นั้น, ข้อความทุกชิ้นจะอัตโนมัติใช้ฟอนต์ใหม่, ทำให้ลักษณะการแสดงผลสอดคล้องกันทั่วทั้งไฟล์.

## ทำไมต้องแก้ไขสไตล์ข้อความ DWG?

- **รักษาความสอดคล้องของแบรนด์:** ใช้ฟอนต์ขององค์กรในทุกภาพวาด.  
- **แก้ไขฟอนต์ที่หายไป:** แทนที่ฟอนต์ที่ไม่มีอยู่ด้วยฟอนต์ที่ติดตั้งบนระบบเป้าหมาย.  
- **เตรียมสำหรับการพิมพ์/พล็อต:** เครื่องพล็อตบางรุ่นต้องการฟอนต์เฉพาะสำหรับผลลัพธ์ที่แม่นยำ.  

## ข้อกำหนดเบื้องต้น

ก่อนที่คุณจะเริ่มทำตามบทแนะนำนี้, โปรดตรวจสอบว่าคุณได้ตั้งค่าดังต่อไปนี้แล้ว:

1. **Aspose.CAD for Java Library:** ดาวน์โหลดและติดตั้งไลบรารี Aspose.CAD. คุณสามารถค้นหาไลบรารีและเอกสารได้ [ที่นี่](https://releases.aspose.com/cad/java/).

2. **Java Development Kit (JDK):** ตรวจสอบว่าคุณได้ติดตั้ง Java บนเครื่องของคุณแล้ว.

เมื่อคุณมีเครื่องมือที่จำเป็นแล้ว, ไปยังส่วนต่อไป.

## นำเข้า Namespaces (จำเป็นสำหรับการแก้ไขสไตล์ข้อความ DWG)

ใน Java การนำเข้า Namespaces ที่ถูกต้องเป็นสิ่งสำคัญสำหรับการใช้ไลบรารีภายนอก. ในกรณีนี้, ให้แน่ใจว่าคุณได้นำเข้า Namespaces ของ Aspose.CAD ที่จำเป็น. ตัวอย่างการทำเช่นนี้มีดังนี้:

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
```

ตอนนี้เราจะทำการแยกโค้ดตัวอย่างออกเป็นหลายขั้นตอน.

## ขั้นตอนที่ 1: ตั้งค่าไดเรกทอรีทรัพยากร

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";
```

แทนที่ `"Your Document Directory"` ด้วยพาธไปยังไดเรกทอรีเอกสารจริงของคุณ.

## ขั้นตอนที่ 2: โหลดภาพวาด CAD

```java
String srcFile = dataDir + "conic_pyramid.dxf";

// Load a CAD drawing in an instance of CadImage
CadImage cadImage = (CadImage)Image.load(srcFile);
```

ตรวจสอบให้แน่ใจว่าได้แทนที่ `"conic_pyramid.dxf"` ด้วยชื่อไฟล์ CAD ของคุณจริง.

## ขั้นตอนที่ 3: ระบุฟอนต์สำหรับสไตล์ (เปลี่ยนฟอนต์สไตล์ DWG)

```java
// Specify the font for one particular style
((CadStyleTableObject)cadImage.getStyles().get_Item(0)).setPrimaryFontName("Arial");
```

ปรับชื่อฟอนต์ ("Arial" ในตัวอย่างนี้) ตามความต้องการของคุณ. บรรทัดนี้ **sets the primary font DWG** style, effectively replacing the old font.

## ปัญหาทั่วไปและวิธีแก้

| Issue | Cause | Solution |
|-------|-------|----------|
| ฟอนต์ไม่เปลี่ยนหลังจากบันทึก | ภาพวาดไม่ได้รับการบันทึกหลังจากแก้ไข | เรียก `cadImage.save(outputPath);` หลังจากตั้งค่าฟอนต์. |
| ไม่รู้จักชื่อฟอนต์ | ฟอนต์ไม่ได้ติดตั้งบนระบบที่รันโค้ด | ติดตั้งฟอนต์หรือใช้ชื่อฟอนต์ทั่วไป (เช่น "Tahoma"). |
| `ClassCastException` | ประเภทอ็อบเจกต์จาก `get_Item` ไม่ถูกต้อง | ตรวจสอบให้ดัชนีชี้ไปที่ `CadStyleTableObject`. |

## คำถามที่พบบ่อย

### Q1: Can I substitute multiple fonts in one DWG file?

A1: Yes, you can iterate through different styles and set the primary font for each style individually.

### Q2: Is there a limit to the font names I can use?

A2: No, you can use any valid font name available on your system.

### Q3: Can I undo font substitutions?

A3: Aspose.CAD provides flexibility; you can revert changes or save different versions of your DWG file.

### Q4: Does this tutorial apply to other CAD formats?

A4: While the example focuses on DWG, similar principles can be applied to other supported CAD formats.

### Q5: How can I get support for Aspose.CAD for Java?

A5: Visit the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) for community support and discussions.

## คำถามที่พบบ่อยเพิ่มเติม

**Q: How do I save the modified drawing?**  
A: After setting the new font, call `cadImage.save(dataDir + "output.dwg");` to write the changes to a new file.

**Q: Can I replace the font of annotation objects only?**  
A: Yes, filter the style collection for annotation‑related styles before applying `setPrimaryFontName`.

**Q: Is it possible to preview the font change without saving?**  
A: You can render the image to a bitmap using `cadImage.save(outputStream, new ImageOptions());` to preview in memory.

**Q: Does Aspose.CAD support TrueType and OpenType fonts?**  
A: Both TrueType (.ttf) and OpenType (.otf) fonts are fully supported as long as they are installed on the host OS.

## สรุป

Aspose.CAD for Java เปิดโอกาสอันทรงพลังสำหรับการจัดการ CAD, และ **how to replace font** เป็นเพียงหนึ่งในความสามารถหลายอย่างของมัน. ทดลองกับสไตล์ต่าง ๆ, ใช้คีย์เวิร์ดรองเช่น *modify DWG text style* หรือ *set primary font dwg* เพื่อปรับแต่งภาพวาดของคุณให้ละเอียดขึ้น, และผสานโค้ดเข้ากับกระบวนการอัตโนมัติขนาดใหญ่สำหรับการประมวลผลเป็นชุด.

---

**อัปเดตล่าสุด:** 2026-01-02  
**ทดสอบด้วย:** Aspose.CAD for Java 24.11  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}