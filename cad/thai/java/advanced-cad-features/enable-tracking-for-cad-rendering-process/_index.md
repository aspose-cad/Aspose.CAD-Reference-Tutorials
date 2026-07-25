---
date: 2026-02-12
description: เรียนรู้วิธีตั้งขนาดหน้ากระดาษ PDF ขณะแปลง CAD เป็น PDF ด้วย Aspose.CAD
  for Java ทำตามคู่มือขั้นตอนต่อขั้นตอนนี้เพื่อเปิดใช้งานการติดตาม, แปลง CAD เป็น
  PDF, และบันทึก CAD เป็น PDF อย่างมีประสิทธิภาพ
linktitle: Set PDF Page Size – Enable Tracking for CAD Rendering
second_title: Aspose.CAD Java API
title: วิธีกำหนดขนาดหน้ากระดาษ PDF และเปิดใช้งานการติดตามสำหรับกระบวนการเรนเดอร์ CAD
url: /th/java/advanced-cad-features/enable-tracking-for-cad-rendering-process/
weight: 10
---

Make sure to keep code block placeholders unchanged.

Now produce final content.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# เปิดใช้งานการติดตามสำหรับกระบวนการเรนเดอร์ CAD

## บทนำ

ในบทเรียนนี้คุณจะได้เรียนรู้วิธี **ตั้งขนาดหน้ากระดาษ PDF** ขณะ **แปลง CAD เป็น PDF** ด้วยการใช้ **Aspose.CAD for Java** การเปิดใช้งานการติดตามจะทำให้คุณมองเห็นภาพรวมของขั้นตอนการเรนเดอร์อย่างเต็มที่ ทำให้การดีบักและปรับประสิทธิภาพการแปลงไฟล์ CAD (เช่น DXF) เป็น PDF ง่ายขึ้น ไม่ว่าคุณจะต้องการ **บันทึก CAD เป็น PDF**, สร้าง PDF จาก DXF, หรือเพียงแค่ควบคุมขนาดผลลัพธ์ ขั้นตอนต่อไปนี้จะพาคุณผ่านกระบวนการทั้งหมด

## คำตอบอย่างรวดเร็ว
- **ตั้งขนาดหน้ากระดาษ PDF ทำอะไร?** มันกำหนดความกว้างและความสูงของหน้ากระดาษ PDF ที่ได้จากการเรนเดอร์ CAD.  
- **ทำไมต้องเปิดใช้งานการติดตาม?** การติดตามบันทึกแต่ละขั้นตอนของการแปลง ช่วยให้คุณพบคอขวดด้านประสิทธิภาพหรือข้อผิดพลาด.  
- **ฉันต้องการไลเซนส์หรือไม่?** การทดลองใช้ฟรีเพียงพอสำหรับการประเมิน; จำเป็นต้องมีไลเซนส์เชิงพาณิชย์สำหรับการใช้งานจริง.  
- **รูปแบบ CAD ใดบ้างที่รองรับ?** DWG, DXF, DGN และอื่น ๆ อีกมาก – ดูเอกสาร Aspose.CAD สำหรับรายการเต็ม.  
- **ฉันสามารถเปลี่ยนขนาดหน้ากระดาษได้แบบเรียลไทม์หรือไม่?** ได้ – เพียงปรับค่า `PageWidth` และ `PageHeight` ใน `CadRasterizationOptions`.

## การตั้งขนาดหน้ากระดาษ PDF ในการเรนเดอร์ CAD คืออะไร?

การตั้งขนาดหน้ากระดาษ PDF จะบอกให้ตัวแรสเตอร์ไลเซอร์ทราบว่าพื้นผิวควรมีขนาดเท่าใดเมื่อข้อมูล CAD แบบเวกเตอร์ถูกแปลงเป็นหน้ากระดาษ PDF สิ่งนี้สำคัญต่อการรักษาความคมชัดของภาพ โดยเฉพาะเมื่อทำงานกับแบบแปลนวิศวกรรมที่ละเอียด

## ทำไมต้องเปิดใช้งานการติดตามสำหรับการเรนเดอร์ CAD?

การเปิดใช้งานการติดตามจะให้บันทึกรายละเอียดของแต่ละขั้นตอน — ตั้งแต่การโหลดไฟล์ต้นฉบับจนถึงการเขียนผลลัพธ์เป็น PDF มันช่วยให้คุณ:
- วินิจฉัยว่าทำไมแบบแปลนบางแบบอาจเรนเดอร์ไม่ถูกต้อง  
- วัดเวลาที่ใช้ในแต่ละขั้นตอน ซึ่งเป็นประโยชน์สำหรับการปรับจูนประสิทธิภาพ  
- ตรวจสอบว่าขนาดหน้ากระดาษที่คุณกำหนดได้ถูกนำไปใช้จริงหรือไม่  

## ข้อกำหนดเบื้องต้น

ก่อนจะเริ่มตั้งค่าการติดตาม โปรดตรวจสอบว่าคุณมีข้อกำหนดต่อไปนี้ครบแล้ว:
1. **สภาพแวดล้อมการพัฒนา Java** – ต้องติดตั้ง Java 8 หรือรุ่นที่ใหม่กว่าในเครื่องของคุณ.  
2. **ไลบรารี Aspose.CAD** – ดาวน์โหลดและรวมไลบรารี Aspose.CAD เข้ากับโปรเจกต์ Java ของคุณ คุณสามารถค้นหาลิงก์ดาวน์โหลดได้ [ที่นี่](https://releases.aspose.com/cad/java/).  
3. **ไดเรกทอรีเอกสาร** – เตรียมไดเรกทอรีเพื่อเก็บไฟล์ CAD ของคุณและ PDF ที่สร้างขึ้น.  

## นำเข้า Namespaces

ในโปรเจกต์ Java ของคุณ ให้นำเข้า namespaces ที่จำเป็นเพื่อใช้ฟังก์ชันของ Aspose.CAD เพิ่มบรรทัดต่อไปนี้ที่ส่วนต้นของโค้ดของคุณ:

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;

import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## ตั้งค่าเส้นทางไดเรกทอรีทรัพยากร

```java
String dataDir = "Your Document Directory" + "CADConversion/";
```

แทนที่ `"Your Document Directory"` ด้วยเส้นทางจริงของไดเรกทอรีเอกสารของคุณ.

## โหลดไฟล์ CAD

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

ระบุเส้นทางไปยังไฟล์ CAD ของคุณ ให้แน่ใจว่าไฟล์อยู่ในไดเรกทอรีเอกสารที่กำหนด

## ตั้งค่าตัวเลือกการส่งออก PDF

```java
OutputStream stream = new FileOutputStream(dataDir + "conic_pyramid.pdf");
PdfOptions pdfOptions = new PdfOptions();
```

สร้างสตรีมเอาต์พุตและตั้งค่าตัวเลือก PDF สำหรับการแปลง

## กำหนดค่า CadRasterizationOptions (ตั้งขนาดหน้ากระดาษ PDF)

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setPageWidth(800);
cadRasterizationOptions.setPageHeight(600);
```

ที่นี่เราจะ **ตั้งขนาดหน้ากระดาษ PDF** โดยกำหนดค่า `PageWidth` และ `PageHeight` ปรับค่าต่าง ๆ ให้ตรงกับขนาดที่ต้องการสำหรับแบบแปลนวิศวกรรมของคุณ นี่คือขั้นตอนหลักที่ตอบ **วิธีตั้งขนาด PDF** เมื่อคุณ **java cad to pdf**.

## บันทึกไฟล์ PDF

```java
image.save(stream, pdfOptions);
```

บันทึกไฟล์ PDF ที่เรนเดอร์ด้วยตัวเลือกที่กำหนด

## ตรวจสอบการเปิดใช้งานการติดตาม

```java
System.out.println("Tracking enabled successfully for CAD rendering process.");
```

ยืนยันว่าการติดตามได้ถูกเปิดใช้งานอย่างสำเร็จสำหรับกระบวนการเรนเดอร์ CAD

## ปัญหาทั่วไปและการแก้ไขปัญหา

| อาการ | สาเหตุที่เป็นไปได้ | วิธีแก้ |
|---------|--------------|-----|
| หน้า PDF ปรากฏเป็นสีขาว | `PageWidth`/`PageHeight` ตั้งค่าเป็น 0 | ตรวจสอบให้แน่ใจว่ากำหนดมิติที่ไม่เป็นศูนย์ |
| ไฟล์ผลลัพธ์เสียหาย | สตรีมเอาต์พุตไม่ได้ปิด | เรียก `stream.close()` หลังจาก `image.save(...)`. |
| ชั้นบางส่วนหายใน PDF | ไฟล์ CAD ใช้เอนทิตีที่ไม่รองรับ | ตรวจสอบว่าไฟล์ฟอร์แมตได้รับการสนับสนุนเต็มที่โดย Aspose.CAD. |

## คำถามที่พบบ่อย

### Q1: Aspose.CAD รองรับรูปแบบไฟล์ CAD ทั้งหมดหรือไม่?

A1: Aspose.CAD รองรับรูปแบบ CAD หลากหลายรวมถึง DWG, DXF, DGN และอื่น ๆ ดูที่ [เอกสาร](https://reference.aspose.com/cad/java/) สำหรับรายการครบถ้วน

### Q2: ฉันสามารถปรับขนาดผลลัพธ์ของไฟล์ PDF ได้หรือไม่?

A2: แน่นอน! ปรับพารามิเตอร์ `PageWidth` และ `PageHeight` ใน `CadRasterizationOptions` เพื่อกำหนดขนาดผลลัพธ์ตามต้องการ

### Q3: มีการทดลองใช้ฟรีสำหรับ Aspose.CAD for Java หรือไม่?

A3: มี, คุณสามารถสำรวจความสามารถของ Aspose.CAD โดยรับการทดลองใช้ฟรีได้ [ที่นี่](https://releases.aspose.com/).

### Q4: ฉันจะขอรับการสนับสนุนจากชุมชนสำหรับคำถามที่เกี่ยวกับ Aspose.CAD ได้อย่างไร?

A4: เยี่ยมชม [ฟอรั่ม Aspose.CAD](https://forum.aspose.com/c/cad/19) เพื่อเข้าร่วมกับชุมชนและขอความช่วยเหลือ

### Q5: มีไลเซนส์ชั่วคราวสำหรับ Aspose.CAD หรือไม่?

A5: มี, หากคุณต้องการไลเซนส์ชั่วคราว คุณสามารถขอได้ [ที่นี่](https://purchase.aspose.com/temporary-license/).

## สรุป

ยินดีด้วย! ตอนนี้คุณได้เรียนรู้วิธี **ตั้งขนาดหน้ากระดาษ PDF** และเปิดใช้งานการติดตามสำหรับการเรนเดอร์ CAD ด้วย **Aspose.CAD for Java** คู่มือนี้ทำให้คุณสามารถ **แปลง CAD เป็น PDF**, **บันทึก CAD เป็น PDF**, และสร้าง PDF จาก DXF พร้อมการควบคุมขนาดหน้ากระดาษอย่างเต็มที่และบันทึกการทำงานอย่างละเอียด อย่าลังเลที่จะทดลองขนาดหน้ากระดาษต่าง ๆ และสำรวจตัวเลือกการแรสเตอร์ไลเซอร์เพิ่มเติมเพื่อให้เหมาะกับกระบวนการวิศวกรรมของคุณ

---

**อัปเดตล่าสุด:** 2026-02-12  
**ทดสอบกับ:** Aspose.CAD for Java 24.12 (ล่าสุด ณ เวลาที่เขียน)  
**ผู้เขียน:** Aspose  

---

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}