---
date: 2026-02-28
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

หากคุณกำลังมองหาวิธีที่เชื่อถือได้ **วิธีอ่าน dwg** ไฟล์โดยโปรแกรม, Aspose.CAD for Java ให้ API ที่สะอาดและข้ามแพลตฟอร์มซึ่งช่วยให้คุณโหลดภาพวาดและดึงข้อมูลที่ต้องการออกมา—เช่นชื่อของทุก layout ภายในไฟล์ ในบทแนะนำแบบขั้นตอนนี้เราจะแสดง **วิธีอ่าน DWG** และแสดงรายการ layout ทั้งหมดที่อยู่ในไฟล์ DWG (หรือ DXF) เพื่อให้คุณสามารถนำความสามารถนี้ไปใช้ในแอปพลิเคชัน Java ใด ๆ ที่ทำงานกับข้อมูล CAD

## คำตอบอย่างรวดเร็ว
- **ต้องใช้ไลบรารีอะไร?** Aspose.CAD for Java.  
- **สามารถอ่านไฟล์ DWG บนระบบปฏิบัติการใดก็ได้หรือไม่?** ได้ – Java ข้ามแพลตฟอร์ม, ดังนั้นคุณสามารถ **อ่าน dwg บน linux** ได้ง่ายเท่ากับบน Windows.  
- **ต้องมีลิขสิทธิ์เพื่อรันตัวอย่างหรือไม่?** ทดลองใช้ฟรีสำหรับการประเมิน; จำเป็นต้องมีลิขสิทธิ์สำหรับการใช้งานจริง.  
- **รองรับรูปแบบ CAD ใดบ้าง?** DWG, DXF, DWF, และอื่น ๆ.  
- **โค้ดนี้เข้ากันได้กับ Java 8+ หรือไม่?** แน่นอน.

## “how to read dwg” ใน Java คืออะไร?

การอ่านไฟล์ DWG หมายถึงการโหลดข้อมูล CAD แบบไบนารีเข้าสู่โมเดลอ็อบเจกต์ที่คุณสามารถสอบถามได้ Aspose.CAD แยกโครงสร้าง DWG ที่ซับซ้อนออกเป็นคลาส Java ที่ง่ายต่อการใช้งาน, ทำให้คุณมุ่งเน้นที่ข้อมูลที่ต้องการ – ในกรณีนี้คือชื่อ layout.

## ทำไมต้องแสดงรายการ layouts ในไฟล์ DWG?

DWG สามารถมีหลาย layout (paper space, model space, แผ่นกำหนดเอง) การรู้ชื่อ layout ช่วยให้คุณ:

- สร้างรายงานตาม layout.  
- ส่งออก layout เฉพาะเป็นภาพหรือ PDF.  
- ทำการประมวลผลชุดของภาพวาดโดยอัตโนมัติ.  

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะลงลึกในโค้ด, ตรวจสอบว่าคุณมีสิ่งต่อไปนี้:

- **Aspose.CAD for Java Library** – ดาวน์โหลด JAR ล่าสุดจาก [website](https://releases.aspose.com/cad/java/).  
- **สภาพแวดล้อมการพัฒนา Java** – JDK 8 หรือสูงกว่า, และ IDE หรือเครื่องมือสร้างที่คุณเลือก.

## นำเข้า Namespaces

ในไฟล์ซอร์ส Java ของคุณ, นำเข้าคลาส Aspose.CAD ที่จำเป็น:

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.CadLayoutDictionary;
import com.aspose.cad.fileformats.cad.cadobjects.CadLayout;
```

## ขั้นตอนที่ 1: ตั้งค่าไดเรกทอรีเอกสารของคุณ

```java
String dataDir = "Your Document Directory" + "CADConversion/";
```

แทนที่ **“Your Document Directory”** ด้วยเส้นทางเต็มที่ที่ไฟล์ CAD ของคุณอยู่ บน Linux คุณอาจใช้เส้นทางเช่น `/home/user/cad/`.

## ขั้นตอนที่ 2: โหลดไฟล์ DWG

```java
String sourceFilePath = dataDir + "conic_pyramid.dxf";
Image image = Image.load(sourceFilePath);
CadImage cadImage = (CadImage)image;
```

เมธอด `Image.load` จะตรวจจับรูปแบบไฟล์โดยอัตโนมัติ, ดังนั้นโค้ดเดียวกันทำงานได้ทั้งไฟล์ **DWG** และ **DXF**.

## ขั้นตอนที่ 3: รับ Layouts และพิมพ์ชื่อ

```java
CadLayoutDictionary layouts = cadImage.getLayouts();
for (CadLayout layout : layouts.getValues())
{
    System.out.println("Layout " + layout.getLayoutName());
}
```

ลูปนี้จะวนผ่านอ็อบเจกต์ layout ทุกตัวและพิมพ์ชื่อของมันไปยังคอนโซล – วิธีง่าย ๆ เพื่อยืนยันว่าคุณได้ **อ่าน DWG** และดึงข้อมูล layout สำเร็จ.

## วิธีแปลง DWG เป็น PDF บน Linux

หากคุณต้องการแปลง layout เฉพาะเป็น PDF, Aspose.CAD สามารถเรนเดอร์ layout เป็นภาพและจากนั้นคุณสามารถใช้ Aspose.PDF (หรือไลบรารี PDF ใด ๆ) เพื่อฝังภาพนั้นลงในเอกสาร PDF โค้ดการแปลงจะเหมือนกันบน Linux เนื่องจาก API เป็น Java แท้ ๆ.

## ข้อผิดพลาดทั่วไป & เคล็ดลับ

- **เส้นทางไฟล์ไม่ถูกต้อง** – ตรวจสอบให้แน่ใจว่า `dataDir` ลงท้ายด้วยตัวคั่น (`/` หรือ `\\`) ที่เหมาะสมกับ OS ของคุณ.  
- **เวอร์ชัน DWG ที่ไม่รองรับ** – ตรวจสอบว่าคุณใช้ Aspose.CAD เวอร์ชันล่าสุด; เวอร์ชัน DWG เก่าอาจต้องแปลงก่อน.  
- **การใช้หน่วยความจำ** – ภาพวาดขนาดใหญ่สามารถใช้หน่วยความจำมาก. ปล่อยอ็อบเจกต์ `CadImage` เมื่อเสร็จ: `cadImage.dispose();`.  
- **รันบนเซิร์ฟเวอร์แบบ headless** – ไม่ต้องใช้คอมโพเนนต์ UI, ดังนั้นโค้ดทำงานบนเซิร์ฟเวอร์ Linux ที่ไม่มีสภาพแวดล้อมกราฟิกได้.

## สรุป

ขอแสดงความยินดี! ตอนนี้คุณรู้ **วิธีอ่าน dwg** และแสดงรายการ layout ของมันด้วย Aspose.CAD for Java เทคนิคนี้เป็นพื้นฐานสำหรับการทำอัตโนมัติ CAD ขั้นสูงต่อไป, เช่นการส่งออก layout เฉพาะเป็นภาพ, PDF, หรือแม้กระทั่งการแปลง DWG เป็น PDF บน Linux. สำหรับการสำรวจเพิ่มเติม, ดูที่ [documentation](https://reference.aspose.com/cad/java/) อย่างเป็นทางการ.

## คำถามที่พบบ่อย

**Q1: สามารถใช้ Aspose.CAD for Java กับรูปแบบไฟล์ CAD อื่นได้หรือไม่?**  
A1: ได้, Aspose.CAD รองรับรูปแบบ CAD ต่าง ๆ รวมถึง DWG, DXF, DWF, และอื่น ๆ.

**Q2: มีรุ่นทดลองฟรีสำหรับ Aspose.CAD for Java หรือไม่?**  
A2: มี, คุณสามารถรับรุ่นทดลองได้จาก [here](https://releases.aspose.com/).

**Q3: จะหาการสนับสนุนจากชุมชนสำหรับ Aspose.CAD for Java ได้ที่ไหน?**  
A3: เยี่ยมชม [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) เพื่อรับการสนับสนุนจากชุมชน.

**Q4: วิธีการซื้อไลเซนส์สำหรับ Aspose.CAD for Java คืออะไร?**  
A4: คุณสามารถซื้อไลเซนส์ได้จาก [purchase page](https://purchase.aspose.com/buy).

**Q5: สามารถใช้ไลเซนส์ชั่วคราวสำหรับการทดสอบได้หรือไม่?**  
A5: ได้, คุณสามารถรับไลเซนส์ชั่วคราวได้จาก [here](https://purchase.aspose.com/temporary-license/).

**คำถามเพิ่มเติม**

**Q: วิธีนี้ทำงานได้กับการอ่านไฟล์ DWG บน Linux หรือไม่?**  
A: แน่นอน. เนื่องจากโซลูชันเป็น Java แท้ ๆ, จึงทำงานบน OS ใดก็ได้ที่มี JDK ที่เข้ากันได้.

**Q: สามารถอ่านไฟล์ DWG โดยไม่โหลดภาพวาดทั้งหมดเข้าสู่หน่วยความจำได้หรือไม่?**  
A: Aspose.CAD โหลดภาพวาดเข้าสู่หน่วยความจำ; สำหรับไฟล์ขนาดใหญ่มากอาจพิจารณาประมวลผลในเธรดแยกหรือใช้ API สตรีมมิ่งหากมีในรุ่นต่อไป.

**Q: มีวิธีกรอง layout ตามชื่อหรือไม่?**  
A: มี – หลังจากดึง `CadLayoutDictionary` มา, คุณสามารถตรวจสอบ `layout.getLayoutName().equalsIgnoreCase("MyLayout")` ก่อนทำการประมวลผล.

---

**อัปเดตล่าสุด:** 2026-02-28  
**ทดสอบด้วย:** Aspose.CAD for Java 24.11  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}