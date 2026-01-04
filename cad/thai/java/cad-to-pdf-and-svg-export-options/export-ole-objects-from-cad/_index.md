---
date: 2026-01-04
description: เรียนรู้วิธี **บันทึก CAD เป็น PNG** และส่งออกวัตถุ OLE จากไฟล์ CAD อย่างง่ายดายโดยใช้
  Aspose.CAD for Java การตั้งค่าที่รวดเร็ว ตัวอย่างโค้ดเต็ม และเคล็ดลับการปฏิบัติที่ดีที่สุด.
linktitle: Export OLE Objects from CAD
second_title: Aspose.CAD Java API
title: บันทึกไฟล์ CAD เป็น PNG และส่งออกวัตถุ OLE ด้วย Aspose.CAD สำหรับ Java
url: /th/java/cad-to-pdf-and-svg-export-options/export-ole-objects-from-cad/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# บันทึก CAD เป็น PNG และส่งออกวัตถุ OLE ด้วย Aspose.CAD สำหรับ Java

## บทนำ

ในโลกที่เปลี่ยนแปลงอย่างรวดเร็วของ Computer‑Aided Design (CAD) การ **บันทึก CAD เป็น PNG** พร้อมกับการดึงวัตถุ OLE (Object Linking and Embedding) ที่ฝังอยู่สามารถทำให้กระบวนการทำงานของคุณเป็นระเบียบมากขึ้น ไม่ว่าคุณจะสร้างเครื่องมือแปลงแบบเป็นชุด, สร้างภาพย่อสำหรับพอร์ทัลเว็บ, หรือเพียงต้องการเก็บบันทึกเนื้อหา OLE, Aspose.CAD สำหรับ Java ให้วิธีการที่สะอาดและเป็นโปรแกรมเมติกเพื่อทำสิ่งนั้นได้ ในบทแนะนำนี้เราจะเดินผ่านกระบวนการทั้งหมด ตั้งแต่การตั้งค่าโปรเจกต์จนถึงการส่งออกแต่ละวัตถุ OLE เป็นภาพ PNG

## คำตอบสั้น
- **ฉันสามารถส่งออกวัตถุ OLE โดยตรงเป็น PNG ได้หรือไม่?** ได้ – Aspose.CAD โหลดไฟล์ CAD แล้วให้คุณเรสเตอร์ไลซ์แต่ละเลเอาต์เป็น PNG  
- **ต้องใช้ Java เวอร์ชันใด?** Java 8 หรือใหม่กว่า  
- **ต้องมีลิขสิทธิ์สำหรับฟีเจอร์นี้หรือไม่?** เวอร์ชันทดลองฟรีใช้ได้สำหรับการประเมิน; ต้องมีลิขสิทธิ์สำหรับการใช้งานจริง  
- **ข้อมูลเวกเตอร์จะถูกเก็บไว้หรือไม่?** การเรสเตอร์ไลซ์ PNG รักษาความแม่นยำของภาพ, แต่ผลลัพธ์เป็นภาพราสเตอร์ ไม่ใช่เวกเตอร์  
- **รองรับการประมวลผลเป็นชุดหรือไม่?** แน่นอน – ทำการวนลูปไฟล์หลายไฟล์ตามตัวอย่างโค้ด

## ข้อกำหนดเบื้องต้น

ก่อนเริ่ม, ตรวจสอบว่าคุณมีสิ่งต่อไปนี้:

- **Java Development Kit (JDK)** – ติดตั้งและกำหนดค่า Java 8+  
- **Aspose.CAD for Java** – ดาวน์โหลดไลบรารีล่าสุดจาก [ลิงก์ดาวน์โหลด](https://releases.aspose.com/cad/java/)  
- **ไฟล์แหล่งที่มาของ CAD** – ไฟล์ DWG/DXF/DGN ใด ๆ ที่มีวัตถุ OLE ที่คุณต้องการส่งออก

## นำเข้า Namespaces

เพื่อทำงานกับไฟล์ CAD คุณต้องนำเข้าคลาสหลักของ Aspose.CAD เก็บบล็อกการนำเข้าไว้ตามที่แสดง – มันให้คลาสที่ใช้ต่อในบทแนะนำ

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

## วิธีบันทึก CAD เป็น PNG

ด้านล่างเป็นคำแนะนำสั้น ๆ ทีละขั้นตอนที่แสดง **วิธีส่งออกวัตถุ OLE และบันทึก CAD เป็น PNG** แต่ละขั้นตอนมีคำอธิบายสั้น ๆ ตามด้วยโค้ดที่ต้องคัดลอกไปยังโปรเจกต์ของคุณ

### ขั้นตอนที่ 1: ตั้งค่าไดเรกทอรีเอกสารของคุณ

กำหนดโฟลเดอร์ที่เก็บแบบร่าง CAD ของคุณ แทนที่ตัวแปรตำแหน่งที่เก็บด้วยพาธจริงบนเครื่องของคุณ

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

### ขั้นตอนที่ 2: กำหนดชื่อไฟล์ CAD

ระบุชื่อไฟล์ CAD ทุกไฟล์ที่ต้องการประมวลผล คุณสามารถเพิ่มรายการได้ตามต้องการ

```java
String[] files = new String[] { "D ZD junior D10m H2m.dwg", "ZD - Senior D6m H2m45.dwg" };
```

### ขั้นตอนที่ 3: ตั้งค่าตัวเลือกการส่งออก PNG

กำหนดค่าการเรสเตอร์ไลซ์ ที่นี่เราตั้งค่าให้ใช้เลเอาต์เฉพาะ (`Layout1`) และใช้ตัวเลือก PNG เริ่มต้น

```java
PngOptions pngOptions = new PngOptions();
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
pngOptions.setVectorRasterizationOptions(rasterizationOptions);
rasterizationOptions.setLayouts(new String[] { "Layout1" });
```

### ขั้นตอนที่ 4: วนลูปไฟล์ CAD และบันทึกเป็น PNG

โหลดไฟล์ CAD แต่ละไฟล์, เรสเตอร์ไลซ์วัตถุ OLE, แล้วเขียนไฟล์ PNG ผลลัพธ์ ส่วนต่อท้าย `_out.png` ช่วยให้คุณแยกแยะภาพที่สร้างขึ้นได้ง่าย

```java
for(String file : files)
{
    CadImage cadImage = (CadImage)Image.load(dataDir + file);
    cadImage.save(dataDir + file + "_out.png", pngOptions);
}
```

## ปัญหาที่พบบ่อยและวิธีแก้

| ปัญหา | สาเหตุ | วิธีแก้ |
|---------|----------------|-----|
| **`Image.load` ขว้าง `FileNotFoundException`** | พาธ `dataDir` ไม่ถูกต้องหรือชื่อไฟล์พิมพ์ผิด | ตรวจสอบสตริงของไดเรกทอรีและให้แน่ใจว่าชื่อไฟล์ตรงกันอย่างแม่นยำ รวมถึงช่องว่าง |
| **PNG ที่ส่งออกเป็นภาพสีขาว** | ชื่อเลเอาต์ไม่มีในไฟล์ CAD ต้นฉบับ | ใช้ `cadImage.getLayouts()` เพื่อแสดงเลเอาต์ที่มีอยู่, แล้วอัปเดต `rasterizationOptions.setLayouts(...)` |
| **ไฟล์ CAD ขนาดใหญ่ทำให้เกิด OutOfMemoryError** | การเรสเตอร์ไลซ์ภาพความละเอียดสูงใช้หน่วยความจำมาก | เพิ่มขนาด heap ของ JVM (`-Xmx2g`) หรือ ลดความละเอียดการเรสเตอร์ไลซ์ด้วย `rasterizationOptions.setResolution(...)` |

## คำถามที่พบบ่อย

### Q1: Aspose.CAD รองรับรูปแบบไฟล์ CAD ทุกประเภทหรือไม่?

A1: Aspose.CAD รองรับรูปแบบ CAD ต่าง ๆ รวมถึง DWG, DXF, และ DGN. ดูรายละเอียดเพิ่มเติมใน [เอกสารอ้างอิง](https://reference.aspose.com/cad/java/)

### Q2: สามารถปรับแต่งการตั้งค่าการส่งออกสำหรับวัตถุ OLE ได้หรือไม่?

A2: ได้, Aspose.CAD มีตัวเลือกมากมายสำหรับการปรับแต่งการส่งออก, ช่วยให้คุณกำหนดผลลัพธ์ให้ตรงตามความต้องการของคุณ

### Q3: มีรุ่นทดลองฟรีสำหรับ Aspose.CAD หรือไม่?

A3: มี, คุณสามารถสำรวจความสามารถของ Aspose.CAD ได้โดยรับรุ่นทดลองฟรีจาก [ที่นี่](https://releases.aspose.com/)

### Q4: จะหาชุมชนสนับสนุนสำหรับ Aspose.CAD ได้จากที่ไหน?

A4: เข้าร่วมชุมชน Aspose.CAD ที่ [ฟอรั่ม](https://forum.aspose.com/c/cad/19) เพื่อขอความช่วยเหลือและแบ่งปันประสบการณ์

### Q5: จะซื้อไลเซนส์สำหรับ Aspose.CAD อย่างไร?

A5: เยี่ยมชม [หน้าการซื้อ](https://purchase.aspose.com/buy) เพื่อเลือกไลเซนส์ที่เหมาะกับความต้องการการพัฒนาของคุณ

## สรุป

โดยทำตามขั้นตอนง่าย ๆ ทั้งห้าขั้นตอนนี้ คุณสามารถ **บันทึก CAD เป็น PNG** และดึงวัตถุ OLE ที่ฝังอยู่ทั้งหมดด้วยเพียงไม่กี่บรรทัดของโค้ด Java วิธีนี้เหมาะสำหรับการแปลงเป็นชุด, รายงานอัตโนมัติ, หรือสถานการณ์ใด ๆ ที่ต้องการภาพราสเตอร์ของเนื้อหา CAD โดยไม่ต้องส่งออกด้วยมือ ลองปรับตัวเลือกการเรสเตอร์ไลซ์ต่าง ๆ เพื่อให้ตรงกับความต้องการด้านคุณภาพและประสิทธิภาพของคุณ

---

**อัปเดตล่าสุด:** 2026-01-04  
**ทดสอบกับ:** Aspose.CAD for Java 24.12 (ล่าสุด ณ เวลาที่เขียน)  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}