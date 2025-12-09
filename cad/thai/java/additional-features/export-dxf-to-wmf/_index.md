---
date: 2025-11-29
description: เรียนรู้วิธีแปลง DXF เป็น WMF ด้วย Aspose.CAD สำหรับ Java, โหลดภาพวาด
  DXF, และหากต้องการใช้การส่งออกของ Aspose เป็น PDF. คู่มือแบบขั้นตอนพร้อมตัวอย่างโค้ด.
linktitle: Export DXF to WMF Format Using Java
second_title: Aspose.CAD Java API
title: แปลง DXF เป็น WMF ด้วย Aspose.CAD ใน Java
url: /th/java/additional-features/export-dxf-to-wmf/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# แปลง DXF เป็น WMF ด้วย Aspose.CAD ใน Java

## บทนำ

ในบทแนะนำนี้คุณจะได้เรียนรู้วิธี **แปลง DXF เป็น WMF** ด้วย Aspose.CAD สำหรับ Java ไม่ว่าคุณจะต้องการฝังภาพวาด CAD ลงในรายงานบน Windows หรือเพียงต้องการรูปแบบเวกเตอร์ที่มีขนาดเบา การแปลง DXF เป็น WMF เป็นความต้องการที่พบบ่อย เราจะเดินผ่านขั้นตอนการโหลดไฟล์ DXF การกำหนดค่าตัวเลือกการเรสเตอร์ไลซ์ การบันทึกผลลัพธ์เป็น WMF และแม้กระทั่งการใช้ Aspose ส่งออกเป็น PDF เป็นขั้นตอนเสริม

## คำตอบสั้น
- **ฉันสามารถแปลง DXF เป็น WMF ด้วยการทดลองใช้งานฟรีได้หรือไม่?** ได้ – Aspose มีรุ่นทดลองเต็มฟังก์ชัน 30 วัน  
- **ต้องใช้ Java เวอร์ชันใด?** Java 8 หรือใหม่กว่า  
- **ต้องมีใบอนุญาตเพื่อรันโค้ดหรือไม่?** จำเป็นต้องมีใบอนุญาตสำหรับการใช้งานในผลิตภัณฑ์; รุ่นทดลองใช้ได้สำหรับการพัฒนาและทดสอบ  
- **การแปลงนี้ไม่มีการสูญเสียข้อมูลหรือไม่?** ข้อมูลเวกเตอร์จะถูกเก็บรักษา; ตัวเลือกการเรสเตอร์ไลซ์ช่วยให้คุณควบคุมความละเอียดได้  
- **ฉันสามารถส่งออกภาพวาดเดียวกันเป็น PDF ได้หรือไม่?** แน่นอน – ดูขั้นตอน “ส่งออกเป็น PDF” ด้านล่าง

## “แปลง DXF เป็น WMF” คืออะไร?

การแปลง DXF เป็น WMF หมายถึงการนำไฟล์ Drawing Exchange Format (DXF) – ฟอร์แมต CAD ที่ใช้กันอย่างกว้างขวาง – มาแปลงเป็น Windows Metafile (WMF) WMF เป็นฟอร์แมตภาพเวกเตอร์ที่ทำงานร่วมกับ Microsoft Office, แอปพลิเคชัน Windows และเครื่องมือรายงานหลายประเภทได้อย่างราบรื่น

## ทำไมต้องใช้ Aspose.CAD สำหรับ Java?

- **ไม่มีการพึ่งพาไลบรารีภายนอก** – Java แท้, ไม่ต้องใช้ DLL เนทีฟ  
- **ความแม่นยำสูง** – รักษาชั้น, สี, และสไตล์เส้น  
- **มีการเรสเตอร์ไลซ์ในตัว** – ปรับขนาดหน้า, ความละเอียด, และพื้นหลังได้ละเอียด  
- **โซลูชันครบวงจร** – API เดียวกันยังสนับสนุนการส่งออกเป็น PDF, PNG, SVG, และอื่น ๆ

## สิ่งที่ต้องเตรียม

ก่อนเริ่มทำงานให้ตรวจสอบว่าคุณมี:

- **Aspose.CAD สำหรับ Java** ที่รวมไว้ในโปรเจกต์ของคุณ ดาวน์โหลดได้จากเว็บไซต์อย่างเป็นทางการ: [Aspose.CAD Java download](https://releases.aspose.com/cad/java/)  
- **โฟลเดอร์เอกสาร** ที่เก็บไฟล์ DXF ของคุณ (เช่น `Your Document Directory/DXFDrawings/`)

## นำเข้า Namespaces

ในไฟล์ซอร์ส Java ของคุณ ให้นำเข้าคลาส Aspose.CAD ที่จำเป็น:

```java
import com.aspose.cad.Color;
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.ifc.IfcImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.WmfOptions;
```

## คู่มือแบบขั้นตอน

### ขั้นตอนที่ 1: โหลดภาพวาด DXF

แรกสุด **โหลดภาพวาด DXF** ที่ต้องการแปลง วิธี `Image.load` จะอ่านไฟล์เข้าสู่หน่วยความจำ

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "DXFDrawings/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

### ขั้นตอนที่ 2: กำหนดค่าตัวเลือกการเรสเตอร์ไลซ์

ตั้งค่าพารามิเตอร์การเรสเตอร์ไลซ์ที่ควบคุมขนาดของ WMF ที่จะได้ ในตัวอย่างนี้เราจะใช้หน้า 100 × 100 หน่วย

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(100);
rasterizationOptions.setPageHeight(100);
WmfOptions wmfOptions = new WmfOptions();
```

### ขั้นตอนที่ 3: บันทึกเป็น WMF

ต่อไปบันทึกภาพวาดที่โหลดไว้เป็นไฟล์ WMF โดยใช้ตัวเลือกที่กำหนดไว้ข้างต้น

```java
cadImage.save(dataDir+" example.ifc.wmf", wmfOptions);
```

### ขั้นตอนที่ 4: ปล่อยทรัพยากร

การปล่อยทรัพยากรอย่างถูกต้องช่วยป้องกันการรั่วของหน่วยความจำ โดยเฉพาะเมื่อประมวลผลหลายภาพวาด

```java
finally
{
  cadImage.dispose();
}
```

### ขั้นตอนที่ 5: ตัวเลือกเสริม – ส่งออก Aspose เป็น PDF

หากคุณต้องการเวอร์ชัน PDF ของภาพวาดเดียวกัน Aspose.CAD ทำให้เป็นบรรทัดเดียวได้เลย

```java
image.save(dataDir + "conic_pyramid_out_.pdf"); 
```

> **เคล็ดลับมืออาชีพ:** คุณสามารถใช้วัตถุ `CadRasterizationOptions` เดียวกันสำหรับการส่งออกเป็น PDF โดยส่งต่อให้กับอินสแตนซ์ `PdfOptions`

## ปัญหาและวิธีแก้ทั่วไป

| ปัญหา | สาเหตุ | วิธีแก้ |
|-------|-------|-----|
| **`NullPointerException` บน `cadImage.save`** | ตัวแปร `cadImage` ไม่ได้กำหนดค่า (ควรเป็น `image`) | แทนที่ `cadImage` ด้วย `image` หรือเปลี่ยนชื่อตัวแปรให้สอดคล้องกัน |
| **ผลลัพธ์ WMF เป็นสีขาวเปล่า** | ขนาดหน้าการเรสเตอร์ไลซ์เล็กเกินไปหรือสีพื้นหลังตั้งเป็นโปร่งใส | เพิ่มค่า `PageWidth`/`PageHeight` หรือกำหนดสีพื้นหลังโดยใช้ `rasterizationOptions.setBackgroundColor(Color.getWhite());` |
| **ข้อยกเว้นใบอนุญาต** | รันโดยไม่มีใบอนุญาต Aspose ที่ถูกต้องในสภาพการผลิต | ใช้ไฟล์ใบอนุญาตที่เริ่มแอปพลิเคชัน: `License license = new License(); license.setLicense("Aspose.Total.Java.lic");` |

## สรุป

คุณมีเวิร์กโฟลว์ครบถ้วนพร้อมใช้งานในระดับผลิตภัณฑ์เพื่อ **แปลง DXF เป็น WMF** ด้วย Aspose.CAD สำหรับ Java พร้อมขั้นตอนเสริม **ส่งออก Aspose เป็น PDF** วิธีนี้ให้ผลลัพธ์เวกเตอร์คุณภาพสูงที่ผสานรวมกับเครื่องมือรายงานและเอกสารบน Windows ได้อย่างไร้รอยต่อ

## คำถามที่พบบ่อย

### Q1: จะหาเอกสาร Aspose.CAD ได้จากที่ไหน?

A1: คุณสามารถเข้าถึงเอกสารได้ [ที่นี่](https://reference.aspose.com/cad/java/)

### Q2: จะดาวน์โหลด Aspose.CAD สำหรับ Java ได้อย่างไร?

A2: ดาวน์โหลดไลบรารีได้ [ที่นี่](https://releases.aspose.com/cad/java/)

### Q3: มีรุ่นทดลองฟรีหรือไม่?

A3: มี, คุณสามารถรับรุ่นทดลองได้ [ที่นี่](https://releases.aspose.com/)

### Q4: ต้องการตัวเลือกใบอนุญาตชั่วคราว?

A4: สำรวจใบอนุญาตชั่วคราวได้ [ที่นี่](https://purchase.aspose.com/temporary-license/)

### Q5: จะหาการสนับสนุนได้จากที่ไหน?

A5: เยี่ยมชมฟอรั่มสนับสนุน Aspose.CAD [ที่นี่](https://forum.aspose.com/c/cad/19)

## คำถามที่พบบ่อยเพิ่มเติม

**ถาม: สามารถแปลงไฟล์ DXF ขนาดใหญ่ (หลายร้อย MB) โดยไม่ทำให้หน่วยความจำหมดได้หรือไม่?**  
ตอบ: ได้. โหลดไฟล์ในบล็อก `try‑with‑resources` และปล่อยอ็อบเจ็กต์ `Image` ทันที ปรับ `CadRasterizationOptions.setPageWidth/Height` ให้เหมาะสมเพื่อควบคุมการใช้หน่วยความจำ

**ถาม: ผลลัพธ์ WMF จะรักษาข้อมูลชั้น (layer) ไว้หรือไม่?**  
ตอบ: WMF เป็นฟอร์แมตเวกเตอร์แบบแบน จึงไม่มีโครงสร้างชั้น แต่สไตล์เส้นและสีจะถูกเก็บรักษา

**ถาม: สามารถกำหนด DPI ที่กำหนดเองสำหรับ WMF ได้หรือไม่?**  
ตอบ: ใช้ `rasterizationOptions.setResolution(300);` เพื่อกำหนด DPI ก่อนบันทึก

**ถาม: สามารถแปลงหลายไฟล์ DXF เป็นชุดเดียวกันได้หรือไม่?**  
ตอบ: แน่นอน. วนลูปผ่านโฟลเดอร์ โหลดแต่ละไฟล์ แล้วใช้ตรรกะการเรสเตอร์ไลซ์และบันทึกเดียวกัน

**ถาม: รองรับเวอร์ชัน Java ใดบ้าง?**  
ตอบ: Aspose.CAD สำหรับ Java รองรับ Java 8 ขึ้นไป (รวมถึง Java 11, 17 และรุ่น LTS ใหม่ ๆ)

---

**อัปเดตล่าสุด:** 2025-11-29  
**ทดสอบด้วย:** Aspose.CAD for Java 24.11  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}