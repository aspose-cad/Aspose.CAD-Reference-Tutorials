---
date: 2025-12-21
description: เรียนรู้วิธีแปลง DWG เป็น BMP และส่งออก CAD เป็น BMP ด้วย Aspose.CAD
  for Java ผ่านคู่มือขั้นตอนโดยละเอียดนี้.
linktitle: Export to BMP
second_title: Aspose.CAD Java API
title: วิธีแปลง DWG เป็น BMP ด้วย Aspose.CAD สำหรับ Java
url: /th/java/cad-export-options/export-to-bmp/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# แปลง DWG เป็น BMP ด้วย Aspose.CAD for Java

## บทนำ

ในกระบวนการทำงานออกแบบดิจิทัลสมัยใหม่ การสามารถ **แปลง DWG เป็น BMP** ได้อย่างรวดเร็วและเชื่อถือได้เป็นสิ่งสำคัญ ไม่ว่าคุณจะสร้างบริการประมวลผลแบบชุดหรือเพียงต้องการแปลงไฟล์เดี่ยว Aspose.CAD for Java ให้ API ที่แข็งแกร่งสำหรับ **ส่งออก CAD เป็น BMP** พร้อมการควบคุมการตั้งค่าการเรสเตอร์ไลซ์อย่างเต็มที่ ในบทแนะนำนี้คุณจะได้ทำตามขั้นตอนทั้งหมด—from การโหลดไฟล์ DWG ไปจนถึงการบันทึกภาพ BMP สุดท้าย—เพื่อให้คุณสามารถรวมการแปลงนี้เข้าไปในแอปพลิเคชัน Java ของคุณได้อย่างมั่นใจ

## คำตอบสั้น
- **ต้องใช้ไลบรารีอะไร?** Aspose.CAD for Java
- **สามารถแปลง DWG เป็น BMP ด้วยบรรทัดเดียวได้หรือไม่?** ไม่ได้ ต้องโหลดไฟล์ ตั้งค่าการเรสเตอร์ไลซ์ แล้วจึงบันทึก
- **ต้องใช้ลิขสิทธิ์สำหรับการผลิตหรือไม่?** ใช่ ต้องมีลิขสิทธิ์เชิงพาณิชย์; มีเวอร์ชันทดลองฟรี
- **API รองรับการแปลงแบบชุดหรือไม่?** แน่นอน—สามารถวนลูปไฟล์และใช้ตัวเลือกเดียวกันซ้ำได้
- **รองรับเวอร์ชัน Java ใด?** Java 8 ขึ้นไป

## “แปลง DWG เป็น BMP” คืออะไร?

การแปลงไฟล์ DWG (AutoCAD drawing) เป็น BMP (bitmap) จะทำการเรสเตอร์ไลซ์ข้อมูลเวกเตอร์เป็นรูปแบบพิกเซล ซึ่งมีประโยชน์เมื่อคุณต้องการภาพที่สามารถดูได้ทั่วทุกแพลตฟอร์มสำหรับรายงาน รูปย่อ หรือการแสดงตัวอย่างบนเว็บโดยไม่ต้องใช้ซอฟต์แวร์ CAD

## ทำไมต้องใช้ Aspose.CAD for Java เพื่อส่งออก CAD เป็น BMP?

- **ไม่มีการพึ่งพาภายนอก** – Java แท้ ๆ ไม่ต้องใช้ DLL เนทีฟ
- **การเรสเตอร์ไลซ์ละเอียด** – ควบคุมขนาดหน้า การจัดวาง การทำแอนตี้อัลลิอาซิง
- **ความแม่นยำสูง** – รักษาน้ำหนักเส้น สี และเลเยอร์
- **ขยายได้** – ทำงานกับไฟล์เดี่ยวหรืองานชุดขนาดใหญ่

## ข้อกำหนดเบื้องต้น

ก่อนจะลงมือเขียนโค้ด ตรวจสอบว่าคุณมี:

- **Aspose.CAD for Java Library** – ดาวน์โหลดจาก [ที่นี่](https://releases.aspose.com/cad/java/)
- **สภาพแวดล้อมการพัฒนา Java** – JDK 8+ และ IDE ที่คุณชอบ
- **ความรู้พื้นฐาน Java** – ความคุ้นเคยกับคลาส เมธอด และการทำ I/O ของไฟล์

## นำเข้า Namespaces

ในโปรเจกต์ Java ของคุณ ให้นำเข้าชื่อเนมสเปซที่จำเป็นเพื่อเข้าถึงฟังก์ชันของ Aspose.CAD:

```java
import com.aspose.cad.Image;
import com.aspose.cad.InterpolationMode;
import com.aspose.cad.SmoothingMode;
import com.aspose.cad.TextRenderingHint;

import com.aspose.cad.imageoptions.BmpOptions;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
//import com.aspose.cad.imageoptions.TypeOfEntities;
```

## ขั้นตอนที่ 1: ตั้งค่าเส้นทางโฟลเดอร์ทรัพยากร

กำหนดโฟลเดอร์ที่บรรจุไฟล์ DWG (หรือ CAD อื่น) ที่คุณต้องการแปลง

```java
String dataDir = "Your Document Directory" + "ExportingCAD/";
```

## ขั้นตอนที่ 2: โหลดไฟล์ CAD

สร้างอ็อบเจ็กต์ `Image` โดยโหลดไฟล์ DWG ต้นฉบับ

```java
String fileName = (dataDir + "site.dwf");
Image image = Image.load(fileName);
```

## ขั้นตอนที่ 3: กำหนดตัวเลือกการส่งออก BMP

สร้างอินสแตนซ์ `BmpOptions` และแนบอ็อบเจ็กต์ `CadRasterizationOptions` ที่ควบคุมการเรสเตอร์ไลซ์เวกเตอร์

```java
BmpOptions bmpOptions = new BmpOptions();
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
bmpOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## ขั้นตอนที่ 4: ตั้งค่าพารามิเตอร์การเรสเตอร์ไลซ์

ปรับขนาดหน้ากระดาษและระบุเลเอาต์ที่ต้องการเรนเดอร์ การตั้งค่าเหล่านี้ส่งผลโดยตรงต่อคุณภาพและขนาดของ BMP ที่ได้

```java
rasterizationOptions.setPageHeight(500);
rasterizationOptions.setPageWidth(500);
rasterizationOptions.setLayouts(new String[] { "Model" });
```

## ขั้นตอนที่ 5: ส่งออกเป็น BMP

ระบุเส้นทางไฟล์ผลลัพธ์และเรียกเมธอด `save` เพื่อบันทึกไฟล์ BMP

```java
String outPath = dataDir + "site.bmp";
image.save(outPath, bmpOptions);
```

ทำซ้ำขั้นตอนข้างต้นสำหรับแต่ละไฟล์ CAD ที่คุณต้องการ **แปลง DWG เป็น BMP** ด้วย Aspose.CAD for Java

## ปัญหาทั่วไป & เคล็ดลับ

- **ชื่อเลเอาต์ไม่ถูกต้อง** – ตรวจสอบให้แน่ใจว่าชื่อเลเอาต์ตรงกับที่กำหนดในไฟล์ DWG (เช่น `"Model"` หรือ `"Layout1"`)
- **ผลลัพธ์ความละเอียดต่ำ** – เพิ่มค่า `PageWidth` และ `PageHeight` เพื่อให้ได้ DPI สูงขึ้น
- **การใช้หน่วยความจำมาก** – สำหรับภาพวาดขนาดใหญ่มาก ควรประมวลผลไฟล์ทีละไฟล์และทำลายอ็อบเจ็กต์ `Image` หลังการบันทึกแต่ละครั้ง

## คำถามที่พบบ่อย

### Q1: Aspose.CAD for Java เหมาะกับการประมวลผลแบบชุดหรือไม่?

A1: แน่นอน! Aspose.CAD for Java รองรับการประมวลผลแบบชุด ช่วยให้คุณจัดการไฟล์ CAD หลายไฟล์ได้อย่างมีประสิทธิภาพ

### Q2: สามารถปรับแต่งตัวเลือกการเรสเตอร์ไลซ์สำหรับเลเอาต์ต่าง ๆ ได้หรือไม่?

A2: ได้ คุณสามารถปรับแต่งตัวเลือกเช่นขนาดหน้าและเลเอาต์ตามความต้องการของแต่ละกรณี

### Q3: จะหาแหล่งสนับสนุนเพิ่มเติมสำหรับ Aspose.CAD for Java ได้จากที่ไหน?

A3: เยี่ยมชม [ฟอรั่ม Aspose.CAD](https://forum.aspose.com/c/cad/19) เพื่อรับการสนับสนุนจากชุมชนและการสนทนาต่าง ๆ

### Q4: มีเวอร์ชันทดลองฟรีหรือไม่?

A4: มี คุณสามารถทดลองใช้ Aspose.CAD for Java ได้ฟรีที่ [นี่](https://releases.aspose.com/)

### Q5: จะขอรับลิขสิทธิ์ชั่วคราวได้อย่างไร?

A5: ขอรับลิขสิทธิ์ชั่วคราวสำหรับ Aspose.CAD for Java ได้ที่ [นี่](https://purchase.aspose.com/temporary-license/)

## คำถามที่พบบ่อยเพิ่มเติม

**Q: สามารถแปลงรูปแบบ CAD อื่น (เช่น DXF, DGN) เป็น BMP ได้หรือไม่?**  
A: ได้ API เดียวกันทำงานกับ DXF, DGN, DWF และรูปแบบที่รองรับอื่น ๆ

**Q: การแปลงนี้รักษาการมองเห็นของเลเยอร์หรือไม่?**  
A: โดยค่าเริ่มต้นเลเยอร์ที่มองเห็นทั้งหมดจะถูกเรสเตอร์ไลซ์; คุณสามารถซ่อนเลเยอร์ผ่าน `CadRasterizationOptions` หากต้องการ

**Q: สามารถตั้งค่าสีพื้นหลังสำหรับ BMP ได้หรือไม่?**  
A: ได้ ใช้ `rasterizationOptions.setBackgroundColor(Color.getWhite());` ก่อนบันทึก

**Q: จะจัดการไฟล์ CAD ที่มีการป้องกันด้วยรหัสผ่านอย่างไร?**  
A: โหลดไฟล์ด้วย `Image.load(fileName, loadOptions)` โดย `loadOptions` มีการระบุรหัสผ่าน

**Q: วิธีที่ดีที่สุดในการเพิ่มประสิทธิภาพสำหรับชุดงานขนาดใหญ่คืออะไร?**  
A: ใช้อินสแตนซ์ `BmpOptions` เดียวและเปลี่ยนเฉพาะเส้นทางไฟล์อินพุตสำหรับแต่ละรอบ

## สรุป

ด้วยการทำตามคู่มือนี้ คุณจะมีพื้นฐานที่มั่นคงสำหรับ **การแปลง DWG เป็น BMP** และ **การส่งออก CAD เป็น BMP** ด้วย Aspose.CAD for Java นำขั้นตอนเหล่านี้ไปผสานในแอปพลิเคชันของคุณเพื่ออัตโนมัติการสร้างภาพ, สร้างรูปย่อ, หรือเตรียมทรัพยากรสำหรับกระบวนการต่อไป

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**อัปเดตล่าสุด:** 2025-12-21  
**ทดสอบกับ:** Aspose.CAD for Java 24.11  
**ผู้เขียน:** Aspose  

---