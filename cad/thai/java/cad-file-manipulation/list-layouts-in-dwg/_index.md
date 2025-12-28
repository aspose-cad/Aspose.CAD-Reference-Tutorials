---
date: 2025-12-28
description: เรียนรู้วิธีอ่านไฟล์ DWG ด้วย Aspose.CAD สำหรับ Java และแสดงรายการเลย์เอาต์ในไฟล์
  DWG อย่างง่ายดาย ผสานรวมฟังก์ชัน CAD ที่ทรงพลังเข้าสู่แอปพลิเคชัน Java ของคุณ
linktitle: List Layouts in DWG
second_title: Aspose.CAD Java API
title: วิธีอ่าน DWG และแสดงรายการ Layout ใน DWG ด้วย Aspose.CAD สำหรับ Java
url: /th/java/cad-file-manipulation/list-layouts-in-dwg/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# วิธีอ่านไฟล์ DWG และแสดงรายการ Layouts ใน DWG ด้วย Aspose.CAD for Java

## บทนำ

หากคุณต้องการ **อ่าน DWG ** อย่างโปรแกรมและดึงข้อมูลเช่นชื่อ layout, Aspose.CAD for Java ทำให้เรื่องนี้ง่ายดาย ในบทเรียนขั้นตอน‑โดย‑ขั้นตอนนี้เราจะแสดงให้คุณ **วิธีอ่าน DWG** และแสดงรายการ layout ทั้งหมดที่อยู่ในไฟล์ DWG (หรือ DXF) เมื่อจบคู่มือคุณจะสามารถเพิ่มความสามารถนี้ในแอปพลิเคชัน Java ใด ๆ ที่ทำงานกับข้อมูล CAD ได้

## คำตอบสั้น
- **ต้องใช้ไลบรารีอะไร?** Aspose.CAD for Java
- **สามารถอ่านไฟล์ DWG บนระบบปฏิบัติการใดก็ได้หรือไม่?** ได้ – Java เป็นแบบข้ามแพลตฟอร์ม
- **ต้องมีลิขสิทธิ์เพื่อรันตัวอย่างหรือไม่?** ทดลองฟรีใช้สำหรับการประเมิน; ต้องมีลิขสิทธิ์สำหรับการใช้งานจริง
- **รองรับรูปแบบ CAD ใดบ้าง?** DWG, DXF, DWF และอื่น ๆ
- **โค้ดเข้ากันได้กับ Java 8+ หรือไม่?** แน่นอน

## “วิธีอ่าน dwg” ใน Java คืออะไร?

การอ่านไฟล์ DWG หมายถึงการโหลดข้อมูล CAD แบบไบนารีเข้าสู่โมเดลวัตถุที่คุณสามารถสอบถามได้ Aspose.CAD แยกโครงสร้าง DWG ที่ซับซ้อนออกเป็นคลาส .NET/Java ที่เรียบง่าย ทำให้คุณโฟกัสที่ข้อมูลที่ต้องการ – ในกรณีนี้คือชื่อ layout

## ทำไมต้องแสดงรายการ layouts ในไฟล์ DWG?

DWG สามารถมีหลาย layout (paper space, model space, sheet ที่กำหนดเอง) การรู้ชื่อ layout ช่วยให้คุณ:
- สร้างรายงานตาม layout
- ส่งออก layout เฉพาะเป็นภาพหรือ PDF
- ทำการประมวลผลชุดของ drawing อัตโนมัติ

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะลงลึกในโค้ด, ตรวจสอบว่าคุณมีสิ่งต่อไปนี้:

- **Aspose.CAD for Java Library** – ดาวน์โหลด JAR ล่าสุดจาก [เว็บไซต์](https://releases.aspose.com/cad/java/)
- **สภาพแวดล้อมการพัฒนา Java** – JDK 8 หรือสูงกว่า, พร้อม IDE หรือเครื่องมือสร้างที่คุณเลือก

## นำเข้า Namespaces

ในไฟล์ซอร์ส Java ของคุณ, นำเข้าคลาส Aspose.CAD ที่จำเป็น:

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.CadLayoutDictionary;
import com.aspose.cad.fileformats.cad.cadobjects.CadLayout;
```

## ขั้นตอนที่ 1: ตั้งค่า Document Directory ของคุณ

```java
String dataDir = "Your Document Directory" + "CADConversion/";
```

แทนที่ **“Your Document Directory”** ด้วยพาธเต็มที่เก็บไฟล์ CAD ของคุณ

## ขั้นตอนที่ 2: โหลดไฟล์ DWG

```java
String sourceFilePath = dataDir + "conic_pyramid.dxf";
Image image = Image.load(sourceFilePath);
CadImage cadImage = (CadImage)image;
```

เมธอด `Image.load` จะตรวจจับรูปแบบไฟล์โดยอัตโนมัติ, ดังนั้นคุณสามารถใช้โค้ดเดียวกันสำหรับไฟล์ **DWG** และ **DXF** ได้

## ขั้นตอนที่ 3: ดึง Layouts และพิมพ์ชื่อ

```java
CadLayoutDictionary layouts = cadImage.getLayouts();
for (CadLayout layout : layouts.getValues())
{
    System.out.println("Layout " + layout.getLayoutName());
}
```

ลูปจะวนผ่านอ็อบเจ็กต์ layout ทุกตัวและพิมพ์ชื่อของมันไปที่คอนโซล – วิธีง่าย ๆ เพื่อยืนยันว่าคุณได้ **อ่าน DWG** และดึงข้อมูล layout สำเร็จแล้ว

## ข้อผิดพลาดทั่วไป & เคล็ดลับ

- **พาธไฟล์ไม่ถูกต้อง** – ตรวจสอบให้แน่ใจว่า `dataDir` ลงท้ายด้วยตัวคั่น (`/` หรือ `\\`) ที่เหมาะกับ OS ของคุณ
- **เวอร์ชัน DWG ที่ไม่รองรับ** – ใช้เวอร์ชัน Aspose.CAD ล่าสุด; เวอร์ชัน DWG เก่าอาจต้องแปลงก่อน
- **การใช้หน่วยความจำ** – Drawing ขนาดใหญ่ใช้หน่วยความจำมาก. ปล่อยอ็อบเจ็กต์ `CadImage` เมื่อเสร็จ: `cadImage.dispose();`

## สรุป

ขอแสดงความยินดี! ตอนนี้คุณรู้ **วิธีอ่าน DWG** และแสดงรายการ layout ของมันด้วย Aspose.CAD for Java เทคนิคนี้เป็นพื้นฐานสำหรับการทำอัตโนมัติ CAD ขั้นสูง เช่น การส่งออก layout เฉพาะเป็นภาพหรือ PDF สำหรับการสำรวจเพิ่มเติม, ดูที่ [เอกสารอย่างเป็นทางการ](https://reference.aspose.com/cad/java/)

## คำถามที่พบบ่อย

### Q1: สามารถใช้ Aspose.CAD for Java กับรูปแบบไฟล์ CAD อื่นได้หรือไม่?

A1: ได้, Aspose.CAD รองรับรูปแบบ CAD ต่าง ๆ รวมถึง DWG, DXF, DWF และอื่น ๆ

### Q2: มีรุ่นทดลองฟรีสำหรับ Aspose.CAD for Java หรือไม่?

A2: มี, คุณสามารถรับรุ่นทดลองได้จาก [ที่นี่](https://releases.aspose.com/)

### Q3: จะหาชุมชนสนับสนุนสำหรับ Aspose.CAD for Java ได้จากที่ไหน?

A3: เยี่ยมชม [ฟอรั่ม Aspose.CAD](https://forum.aspose.com/c/cad/19) เพื่อรับการสนับสนุนจากชุมชน

### Q4: จะซื้อไลเซนส์สำหรับ Aspose.CAD for Java อย่างไร?

A4: คุณสามารถซื้อไลเซนส์ได้จาก [หน้าซื้อสินค้า](https://purchase.aspose.com/buy)

### Q5: สามารถใช้ไลเซนส์ชั่วคราวสำหรับการทดสอบได้หรือไม่?

A5: ได้, คุณสามารถรับไลเซนส์ชั่วคราวได้จาก [ที่นี่](https://purchase.aspose.com/temporary-license/)

**คำถามเพิ่มเติม**

**Q: วิธีนี้ทำงานกับการอ่านไฟล์ DWG บน Linux ได้หรือไม่?**  
A: แน่นอน. เนื่องจากโซลูชันเป็น Java แท้ ๆ จึงทำงานบน OS ใดก็ได้ที่มี JDK ที่เข้ากันได้

**Q: สามารถอ่านไฟล์ DWG โดยไม่โหลด drawing ทั้งหมดเข้าสู่หน่วยความจำได้หรือไม่?**  
A: Aspose.CAD โหลด drawing ทั้งหมดเข้าสู่หน่วยความจำ; สำหรับไฟล์ขนาดใหญ่มากอาจพิจารณาแยกประมวลผลเป็นเธรดหลาย ๆ ตัวหรือใช้ API สตรีมมิ่งหากมีในรุ่นต่อไป

**Q: มีวิธีกรอง layout ตามชื่อหรือไม่?**  
A: มี – หลังจากดึง `CadLayoutDictionary` คุณสามารถตรวจสอบ `layout.getLayoutName().equalsIgnoreCase("MyLayout")` ก่อนทำการประมวลผล

---

**อัปเดตล่าสุด:** 2025-12-28  
**ทดสอบกับ:** Aspose.CAD for Java 24.11  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}