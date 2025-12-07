---
date: 2025-12-07
description: เรียนรู้วิธีตั้งขนาดหน้ากระดาษ PDF ขณะแปลง CAD เป็น PDF ด้วย Aspose.CAD
  สำหรับ Java ทำตามคู่มือขั้นตอนต่อขั้นตอนนี้เพื่อเปิดใช้งานการติดตาม แปลง CAD เป็น
  PDF และบันทึก CAD เป็น PDF อย่างมีประสิทธิภาพ
language: th
linktitle: Set PDF Page Size – Enable Tracking for CAD Rendering
second_title: Aspose.CAD Java API
title: วิธีตั้งขนาดหน้ากระดาษ PDF และเปิดใช้งานการติดตามสำหรับกระบวนการเรนเดอร์ CAD
url: /java/advanced-cad-features/enable-tracking-for-cad-rendering-process/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# เปิดใช้งานการติดตามสำหรับกระบวนการเรนเดอร์ CAD

## บทนำ

ในบทเรียนนี้คุณจะได้เรียนรู้วิธี **ตั้งขนาดหน้ากระดาษ PDF** ขณะ **แปลง CAD เป็น PDF** ด้วย **Aspose.CAD for Java** การเปิดใช้งานการติดตามจะทำให้คุณมองเห็นภาพรวมของ pipeline การเรนเดอร์ได้อย่างเต็มที่ ทำให้การดีบักและปรับประสิทธิภาพการแปลงไฟล์ CAD (เช่น DXF) เป็น PDF ง่ายขึ้น ไม่ว่าคุณจะต้องการ **บันทึก CAD เป็น PDF** สร้าง PDF จาก DXF หรือเพียงแค่ควบคุมขนาดผลลัพธ์ ขั้นตอนต่อไปนี้จะพาคุณผ่านกระบวนการทั้งหมด

## คำตอบสั้น ๆ
- **“ตั้งขนาดหน้ากระดาษ PDF” ทำอะไร?** กำหนดความกว้างและความสูงของหน้ากระดาษ PDF ที่ได้จากการเรนเดอร์ CAD  
- **ทำไมต้องเปิดใช้งานการติดตาม?** การติดตามบันทึกแต่ละขั้นตอนของการแปลง ช่วยให้คุณพบคอขวดหรือข้อผิดพลาดได้ง่ายขึ้น  
- **ต้องมีลิขสิทธิ์หรือไม่?** สามารถใช้รุ่นทดลองฟรีสำหรับการประเมินได้; ต้องมีลิขสิทธิ์เชิงพาณิชย์สำหรับการใช้งานจริง  
- **รูปแบบ CAD ใดบ้างที่รองรับ?** DWG, DXF, DGN และอื่น ๆ อีกมาก – ดูเอกสาร Aspose.CAD สำหรับรายการเต็ม  
- **สามารถเปลี่ยนขนาดหน้าได้แบบไดนามิกหรือไม่?** ได้ – เพียงปรับค่า `PageWidth` และ `PageHeight` ใน `CadRasterizationOptions`

## “ตั้งขนาดหน้ากระดาษ PDF” ในการเรนเดอร์ CAD คืออะไร?

การตั้งขนาดหน้ากระดาษ PDF บอก rasterizer ว่าแคนวาสควรมีขนาดเท่าไหร่เมื่อข้อมูล CAD แบบเวกเตอร์ถูกแปลงเป็นหน้ากระดาษ PDF สิ่งนี้สำคัญเพื่อรักษาความคมชัดของภาพ โดยเฉพาะเมื่อทำงานกับแบบแปลนวิศวกรรมที่ละเอียด

## ทำไมต้องเปิดใช้งานการติดตามสำหรับการเรนเดอร์ CAD?

การเปิดใช้งานการติดตามให้บันทึกรายละเอียดของแต่ละขั้นตอน – ตั้งแต่การโหลดไฟล์ต้นฉบับจนถึงการเขียนไฟล์ PDFออกมา ช่วยให้คุณ:

- วินิจฉัยว่าทำไมแบบแปลนบางแบบอาจแสดงผลไม่ถูกต้อง  
- วัดเวลาในการทำงานของแต่ละขั้นตอน เพื่อปรับประสิทธิภาพ  
- ยืนยันว่าขนาดหน้ากระดาษที่คุณตั้งค่าได้ถูกนำไปใช้จริง

## ข้อกำหนดเบื้องต้น

ก่อนเริ่มตั้งค่าการติดตาม ให้ตรวจสอบว่าคุณมีสิ่งต่อไปนี้พร้อมใช้งาน:

1. **สภาพแวดล้อมการพัฒนา Java** – ติดตั้ง Java 8 หรือใหม่กว่าในเครื่องของคุณ  
2. **ไลบรารี Aspose.CAD** – ดาวน์โหลดและรวมไลบรารี Aspose.CAD เข้ากับโปรเจกต์ Java ของคุณ คุณสามารถหาลิงก์ดาวน์โหลดได้ [ที่นี่](https://releases.aspose.com/cad/java/)  
3. **โฟลเดอร์เอกสาร** – เตรียมโฟลเดอร์สำหรับเก็บไฟล์ CAD และ PDF ที่สร้างขึ้น

## นำเข้า Namespaces

ในโปรเจกต์ Java ของคุณ ให้นำเข้าชุด namespace ที่จำเป็นเพื่อใช้ฟังก์ชันของ Aspose.CAD เพิ่มบรรทัดต่อไปนี้ที่ส่วนต้นของโค้ด:

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;

import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## ตั้งค่าเส้นทางโฟลเดอร์ทรัพยากร

```java
String dataDir = "Your Document Directory" + "CADConversion/";
```

แทนที่ `"Your Document Directory"` ด้วยเส้นทางจริงของโฟลเดอร์เอกสารของคุณ

## โหลดไฟล์ CAD

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

ระบุเส้นทางไปยังไฟล์ CAD ของคุณ ให้แน่ใจว่าไฟล์อยู่ในโฟลเดอร์เอกสารที่กำหนดไว้

## ตั้งค่าตัวเลือกการส่งออก PDF

```java
OutputStream stream = new FileOutputStream(dataDir + "conic_pyramid.pdf");
PdfOptions pdfOptions = new PdfOptions();
```

สร้าง stream สำหรับการส่งออกและตั้งค่าตัวเลือก PDF สำหรับการแปลง

## กำหนดค่า CadRasterizationOptions (ตั้งขนาดหน้ากระดาษ PDF)

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setPageWidth(800);
cadRasterizationOptions.setPageHeight(600);
```

ที่นี่เราจะ **ตั้งขนาดหน้ากระดาษ PDF** โดยกำหนดค่า `PageWidth` และ `PageHeight` ปรับค่าตามขนาดที่ต้องการสำหรับแบบแปลนวิศวกรรมของคุณ ขั้นตอนนี้มีผลโดยตรงต่อการสเกลและการเรนเดอร์เนื้อหา CAD ใน PDF สุดท้าย

## บันทึกไฟล์ PDF

```java
image.save(stream, pdfOptions);
```

บันทึกไฟล์ PDF ที่เรนเดอร์แล้วพร้อมตัวเลือกที่กำหนดไว้

## ยืนยันการเปิดใช้งานการติดตาม

```java
System.out.println("Tracking enabled successfully for CAD rendering process.");
```

ตรวจสอบว่าการติดตามได้ถูกเปิดใช้งานสำเร็จสำหรับกระบวนการเรนเดอร์ CAD

## ปัญหาที่พบบ่อยและการแก้ไข

| อาการ | สาเหตุที่เป็นไปได้ | วิธีแก้ |
|---------|--------------|-----|
| หน้า PDF แสดงเป็นสีขาว | `PageWidth`/`PageHeight` ตั้งเป็น 0 | ตรวจสอบให้แน่ใจว่าได้กำหนดขนาดที่ไม่เป็นศูนย์ |
| ไฟล์ผลลัพธ์เสีย | ไม่ได้ปิด Output stream | เรียก `stream.close()` หลังจาก `image.save(...)` |
| ชั้นบางส่วนหายใน PDF | ไฟล์ CAD มี entities ที่ไม่รองรับ | ยืนยันว่าไฟล์รูปแบบนั้นได้รับการสนับสนุนเต็มที่โดย Aspose.CAD |

## คำถามที่พบบ่อย

### Q1: Aspose.CAD รองรับรูปแบบไฟล์ CAD ทุกประเภทหรือไม่?

A1: Aspose.CAD รองรับรูปแบบ CAD หลากหลายรวมถึง DWG, DXF, DGN และอื่น ๆ ดูรายละเอียดเพิ่มเติมใน [เอกสาร](https://reference.aspose.com/cad/java/)

### Q2: ฉันสามารถปรับขนาดผลลัพธ์ของไฟล์ PDF ได้หรือไม่?

A2: แน่นอน! ปรับพารามิเตอร์ `PageWidth` และ `PageHeight` ใน `CadRasterizationOptions` เพื่อกำหนดขนาดผลลัพธ์ตามต้องการ

### Q3: มีรุ่นทดลองฟรีสำหรับ Aspose.CAD for Java หรือไม่?

A3: มี คุณสามารถสำรวจความสามารถของ Aspose.CAD ได้โดยรับรุ่นทดลอง [ที่นี่](https://releases.aspose.com/)

### Q4: จะหาชุมชนสนับสนุนสำหรับคำถามเกี่ยวกับ Aspose.CAD ได้จากที่ไหน?

A4: เยี่ยมชม [ฟอรั่ม Aspose.CAD](https://forum.aspose.com/c/cad/19) เพื่อเข้าร่วมกับชุมชนและขอความช่วยเหลือ

### Q5: มีลิขสิทธิ์ชั่วคราวสำหรับ Aspose.CAD หรือไม่?

A5: มี หากคุณต้องการลิขสิทธิ์ชั่วคราว สามารถขอได้ [ที่นี่](https://purchase.aspose.com/temporary-license/)

## สรุป

ขอแสดงความยินดี! คุณได้เรียนรู้วิธี **ตั้งขนาดหน้ากระดาษ PDF** และเปิดใช้งานการติดตามสำหรับการเรนเดอร์ CAD ด้วย **Aspose.CAD for Java** คู่มือนี้ทำให้คุณสามารถ **แปลง CAD เป็น PDF**, **บันทึก CAD เป็น PDF**, และสร้าง PDF จาก DXF พร้อมควบคุมขนาดหน้าและบันทึกการทำงานอย่างละเอียด อย่าลังเลที่จะทดลองขนาดหน้าต่าง ๆ และสำรวจตัวเลือกการ rasterization เพิ่มเติมเพื่อให้เหมาะกับกระบวนการวิศวกรรมของคุณ

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**อัปเดตล่าสุด:** 2025-12-07  
**ทดสอบกับ:** Aspose.CAD for Java 24.12 (ล่าสุด ณ เวลาที่เขียน)  
**ผู้เขียน:** Aspose  

---