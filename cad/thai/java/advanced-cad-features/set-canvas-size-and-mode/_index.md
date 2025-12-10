---
date: 2025-12-10
description: เรียนรู้วิธีแปลง CAD เป็น PDF ด้วย Aspose.CAD สำหรับ Java พร้อมตั้งค่าขนาดแคนวาส
  การปรับสเกลเลย์เอาต์อัตโนมัติ และการส่งออกเป็น TIFF.
linktitle: Convert CAD to PDF – Set Canvas Size & Mode
second_title: Aspose.CAD Java API
title: แปลง CAD เป็น PDF – ตั้งขนาดแคนวาสและโหมด (Java)
url: /th/java/advanced-cad-features/set-canvas-size-and-mode/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# ตั้งขนาดแคนวาสและโหมด

## คำนำ

คุณกำลังมองหา **การแปลง CAD เป็น PDF** พร้อมการควบคุมขนาดแคนวาสและโหมดการเรนเดอร์อย่างเต็มที่หรือไม่? คู่มือฉบับสมบูรณ์นี้จะพาคุณผ่านขั้นตอนที่จำเป็นเพื่อกำหนดขนาดแคนวาสใน Java, เปิดใช้งานการปรับสเกลเลย์เอาต์อัตโนมัติ, แล้วส่งออกผลลัพธ์เป็นไฟล์ PDF และ TIFF ด้วย Aspose.CAD ไม่ว่าคุณจะกำลังปรับแต่งไลน์พายป์ไลน์การผลิตหรือทดลองต้นแบบ คุณจะพบคำแนะนำที่ชัดเจนและทำได้จริงที่นี่

## คำตอบสั้น
- **“การแปลง CAD เป็น PDF” หมายถึงอะไร?** การแปลงภาพวาด CAD (เช่น DXF, DWG) ให้เป็นเอกสาร PDF ที่สามารถดูได้บนทุกแพลตฟอร์ม  
- **ฉันสามารถส่งออกเป็น TIFF ได้หรือไม่?** ได้ — ใช้ `TiffOptions` เพื่อสร้างภาพเรสเตอร์ความละเอียดสูง  
- **ตัวเลือกใดที่ควบคุมขนาดแคนวาสใน Java?** `CadRasterizationOptions.setPageWidth/Height`  
- **การปรับสเกลเลย์เอาต์อัตโนมัติคืออะไร?** ธง (`setAutomaticLayoutsScaling(true)`) ที่รักษาสัดส่วนเลย์เอาต์เดิมเมื่อขนาดแคนวาสเปลี่ยนแปลง  
- **ต้องใช้ลิขสิทธิ์สำหรับ Aspose.CAD หรือไม่?** จำเป็นต้องมีลิขสิทธิ์ชั่วคราวหรือถาวรสำหรับการใช้งานในผลิตภัณฑ์

## **การแปลง CAD เป็น PDF** คืออะไร?

การแปลง CAD เป็น PDF หมายถึงการนำภาพวาดวิศวกรรมแบบเวกเตอร์มารันเดอร์เป็นหน้ากระดาษ PDF โดยคงรักษาเส้น, ชั้น, และเรขาคณิตไว้ พร้อมทำให้ไฟล์สามารถเข้าถึงได้ทั่วโลก

## ทำไมต้องตั้งขนาดแคนวาส **java**?

การตั้งขนาดแคนวาสใน Java ช่วยให้คุณกำหนดความละเอียดและขนาดหน้ากระดาษของผลลัพธ์ได้ ทำให้ไฟล์ PDF หรือ TIFF ที่ได้ตรงกับความต้องการด้านการพิมพ์หรือการแสดงผลของคุณ อีกทั้งยังให้คุณควบคุมพฤติกรรมการสเกล ซึ่งสำคัญสำหรับภาพวาดขนาดใหญ่

## ข้อกำหนดเบื้องต้น

ก่อนจะเริ่มทำตามบทแนะนำ โปรดตรวจสอบว่าคุณมีสิ่งต่อไปนี้พร้อมใช้งานแล้ว:

- Aspose.CAD for Java: ตรวจสอบว่าคุณได้ติดตั้งไลบรารี Aspose.CAD ในสภาพแวดล้อม Java ของคุณแล้ว คุณสามารถดาวน์โหลดได้ [ที่นี่](https://releases.aspose.com/cad/java/)  
- โฟลเดอร์เอกสาร: ตั้งค่าโฟลเดอร์เพื่อเก็บไฟล์ CAD ของคุณ โฟลเดอร์นี้จะถูกอ้างอิงในขั้นตอนของบทแนะนำ

ตอนนี้เรามาเริ่มต้นตามขั้นตอนแบบทีละขั้นตอนกันเลย

## นำเข้า Namespaces

ในขั้นตอนนี้ เราจะนำเข้า namespace ที่จำเป็นเพื่อเริ่มต้นโปรเจกต์ Aspose.CAD ของคุณ

```java
import java.awt.Image;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

## ขั้นตอนที่ 1: นำเข้าคลาส Aspose.CAD

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";

String srcFile = dataDir + "conic_pyramid.dxf";
com.aspose.cad.Image objImage = com.aspose.cad.Image.load(srcFile);
```

ในโค้ดส่วนนี้ เราตั้งค่าพาธไปยังไดเรกทอรีทรัพยากรและโหลดไฟล์ DXF ด้วยคลาส `Image` ของ Aspose.CAD

## ขั้นตอนที่ 2: ตั้งค่าคุณสมบัติ **CadRasterizationOptions** (ตั้งขนาดแคนวาส java)

```java
// Create an instance of CadRasterizationOptions and set its various properties
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);

rasterizationOptions.setAutomaticLayoutsScaling(true);
rasterizationOptions.setNoScaling(true);
```

ที่นี่ เราสร้างอินสแตนซ์ของ `CadRasterizationOptions` และกำหนดคุณสมบัติต่าง ๆ เช่น ความกว้างหน้า, ความสูงหน้า, และ **การปรับสเกลเลย์เอาต์อัตโนมัติ** นี่คือหัวใจของ **การกำหนดโหมดแคนวาส** สำหรับการแปลงของคุณ

## ขั้นตอนที่ 3: สร้าง PdfOptions และตั้งค่า VectorRasterizationOptions

```java
// Create an instance of PdfOptions
PdfOptions pdfOptions = new PdfOptions();

// Set the VectorRasterizationOptions property
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

ต่อมา เราสร้างอินสแตนซ์ของ `PdfOptions` และตั้งค่าคุณสมบัติ `VectorRasterizationOptions` ให้เป็น `CadRasterizationOptions` ที่กำหนดไว้ก่อนหน้า

## ขั้นตอนที่ 4: ส่งออกเป็น PDF (แปลง cad เป็น pdf)

```java
// Export CAD to PDF
objImage.save(dataDir + "result_out_.pdf", pdfOptions);
```

สุดท้าย เราบันทึกภาพ CAD เป็นไฟล์ PDF ด้วยตัวเลือกที่ระบุไว้ ทำให้กระบวนการ **แปลง CAD เป็น PDF** เสร็จสมบูรณ์

## ขั้นตอนที่ 5: สร้าง TiffOptions และตั้งค่า VectorRasterizationOptions (ส่งออก cad เป็น tiff)

```java
// Create an instance of TiffOptions
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);

// Set the VectorRasterizationOptions property
tiffOptions.setVectorRasterizationOptions(rasterizationOptions);
```

ในขั้นตอนนี้ เราตั้งค่าอินสแตนซ์ของ `TiffOptions` และกำหนดคุณสมบัติ `VectorRasterizationOptions` ของมัน

## ขั้นตอนที่ 6: ส่งออกเป็น TIFF

```java
// Export CAD to TIFF
objImage.save(dataDir + "result_out_.tiff", tiffOptions);
```

สุดท้าย เราบันทึกภาพ CAD เป็นไฟล์ TIFF ด้วยตัวเลือกที่ระบุไว้ แสดงวิธี **ส่งออก CAD เป็น TIFF** หลังจากตั้งค่าขนาดแคนวาสแล้ว

## ปัญหาทั่วไปและวิธีแก้

| ปัญหา | สาเหตุ | วิธีแก้ |
|-------|-------|-----|
| PDF ที่ได้เป็นหน้าว่าง | `setNoScaling(true)` ปิดการเรนเดอร์สำหรับบางภาพวาด | ลบ `setNoScaling(true)` หรือกำหนดเป็น `false` |
| ความละเอียด TIFF ดูต่ำ | ความกว้าง/สูงของหน้าเล็กเกินไป | เพิ่มค่าของ `setPageWidth` / `setPageHeight` |
| เลย์เอาต์บิดเบี้ยว | ปิดการปรับสเกลเลย์เอาต์อัตโนมัติ | ตรวจสอบให้แน่ใจว่า `setAutomaticLayoutsScaling(true)` ถูกเปิดใช้งาน |

## สรุป

ขอแสดงความยินดี! คุณได้ทำ **การแปลง CAD เป็น PDF** และ **การส่งออก CAD เป็น TIFF** พร้อม **ตั้งขนาดแคนวาส java**, เปิด **การปรับสเกลเลย์เอาต์อัตโนมัติ**, และเรียนรู้วิธี **กำหนดโหมดแคนวาส** เพื่อให้ได้ผลลัพธ์คุณภาพสูง บทแนะนำนี้เป็นพื้นฐานที่มั่นคงสำหรับโครงการแปลง CAD ของคุณ สำรวจคุณลักษณะและความเป็นไปได้เพิ่มเติมได้ใน [เอกสาร Aspose.CAD](https://reference.aspose.com/cad/java/)

## คำถามที่พบบ่อย

### Q1: ฉันสามารถใช้ Aspose.CAD for Java ร่วมกับเฟรมเวิร์ก Java อื่นได้หรือไม่?

A1: ได้, Aspose.CAD ถูกออกแบบให้ทำงานร่วมกับเฟรมเวิร์ก Java ต่าง ๆ อย่างราบรื่น

### Q2: มีลิขสิทธิ์ชั่วคราวสำหรับ Aspose.CAD หรือไม่?

A2: มี, คุณสามารถรับลิขสิทธิ์ชั่วคราวได้ [ที่นี่](https://purchase.aspose.com/temporary-license/)

### Q3: จะหาชุมชนสนับสนุนสำหรับ Aspose.CAD ได้จากที่ไหน?

A3: เยี่ยมชม [ฟอรั่ม Aspose.CAD](https://forum.aspose.com/c/cad/19) เพื่อรับการสนับสนุนและการสนทนาจากชุมชน

### Q4: ฉันสามารถทดลองใช้ Aspose.CAD ได้ฟรีหรือไม่?

A4: แน่นอน! รับการทดลองใช้ฟรีได้ [ที่นี่](https://releases.aspose.com/)

### Q5: จะซื้อ Aspose.CAD for Java ได้จากที่ไหน?

A5: ซื้อผลิตภัณฑ์ได้ [ที่นี่](https://purchase.aspose.com/buy)

**คำถามและคำตอบเพิ่มเติม**

**ถาม: ขนาดแคนวาสมีผลต่อคุณภาพเวกเตอร์ใน PDF หรือไม่?**  
ตอบ: ไม่. ขนาดแคนวาสกำหนดขนาดหน้ากระดาษ; ข้อมูลเวกเตอร์ยังคงเป็นอิสระจากความละเอียด ทำให้การเรนเดอร์คมชัดที่ระดับการซูมใด ๆ

**ถาม: ฉันสามารถตั้ง DPI ที่แตกต่างสำหรับการส่งออก TIFF ได้หรือไม่?**  
ตอบ: ได้. ปรับ `rasterizationOptions.setResolution(dpiValue)` ก่อนสร้าง `TiffOptions`

---

**อัปเดตล่าสุด:** 2025-12-10  
**ทดสอบกับ:** Aspose.CAD for Java 24.12  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}