---
date: 2026-05-04
description: เรียนรู้วิธีแปลงไฟล์ CAD PDF โดยการส่งออก DGN เป็น AutoCAD PDF ด้วย Aspose.CAD
  for Java คู่มือขั้นตอนโดยละเอียดพร้อมขนาด PDF ที่ปรับแต่งได้และตัวเลือกต่าง ๆ
keywords:
- convert cad pdf
- how to export dgn
- customize pdf size
- aspose cad download
- set pdf options
linktitle: การส่งออก DGN ในรูปแบบ AutoCAD ไปเป็น PDF
second_title: Aspose.CAD Java API
title: แปลง CAD PDF – การส่งออก DGN ไปยัง AutoCAD PDF อย่างง่ายดายด้วย Aspose.CAD
  สำหรับ Java
url: /th/java/dgn-export-options/exporting-dgn-to-pdf/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# แปลง CAD PDF: การส่งออก DGN ไปเป็น PDF ของ AutoCAD อย่างง่ายดายด้วย Aspose.CAD สำหรับ Java

## บทนำ

หากคุณต้องการ **convert CAD PDF** ไฟล์โดยตรงจากแหล่ง DGN คุณมาถูกที่แล้ว ในบทเรียนนี้เราจะพาคุณผ่านการใช้ Aspose.CAD for Java เพื่อส่งออกไฟล์ DGN ไปเป็น PDF ที่เข้ากันได้กับ AutoCAD คุณจะได้เห็นวิธีตั้งค่าขนาดหน้าที่กำหนดเอง เลือกเลย์เอาต์เฉพาะ และปรับแต่งผลลัพธ์ PDF อย่างละเอียด — ทั้งหมดนี้ด้วยโค้ดที่ชัดเจนเป็นขั้นตอนที่คุณสามารถนำไปใช้ในโปรเจกต์ของคุณได้ทันที

## คำตอบสั้น
- **What does “convert CAD PDF” mean?** หมายถึงการแปลงไฟล์แหล่ง CAD (เช่น DGN) ให้เป็น PDF ที่คงรักษาข้อมูลเวกเตอร์และความแม่นยำของเลย์เอาต์ไว้  
- **Which library handles the conversion?** Aspose.CAD for Java ให้การทดลองใช้ที่เชื่อถือได้และไม่มีค่าไลเซนส์สำหรับงานนี้  
- **Do I need a license for development?** การทดลองใช้ฟรีเพียงพอสำหรับการทดสอบ; จำเป็นต้องมีไลเซนส์เชิงพาณิชย์สำหรับการใช้งานในสภาพแวดล้อมจริง  
- **Can I customize the PDF size?** ได้ – `CadRasterizationOptions` ช่วยให้คุณตั้งค่าความกว้าง ความสูง และการสเกลของหน้า  
- **How many lines of code are required?** น้อยกว่า 20 บรรทัดของโค้ด Java เพื่อโหลด ตั้งค่า และบันทึก PDF  

## “convert CAD PDF” คืออะไร
การ **convert CAD PDF** หมายถึงการนำภาพวาด CAD ดั้งเดิม (เช่น DGN) มาสร้างเป็น PDF ที่คงรักษากราฟิกเวกเตอร์, ชั้น, และข้อมูลเลย์เอ์เดิมไว้ PDF ที่ได้สามารถดูได้บนอุปกรณ์ใดก็ได้โดยไม่ต้องใช้ซอฟต์แวร์ CAD ทำให้เหมาะสำหรับการแชร์, พิมพ์, หรือเก็บรักษา  

## ทำไมต้องใช้ Aspose.CAD for Java เพื่อแปลง CAD PDF?
- **Full format support** – รองรับ DGN, DWG, DXF และอื่น ๆ อีกมากมาย  
- **No external dependencies** – Java แท้ ไม่ต้องใช้ DLL ภายนอก  
- **Fine‑grained control** – คุณสามารถเลือกเลย์เอาต์ที่จะส่งออก ตั้งค่าขนาดหน้ากำหนดเอง และควบคุมคุณภาพการเรสเตอร์ไลซ์  
- **Scalable for batch jobs** – โหลดและบันทึกหลายสิบไฟล์ในลูปโดยมีภาระงานน้อย  

## ข้อกำหนดเบื้องต้น
ก่อนที่เราจะเริ่ม โปรดตรวจสอบว่าคุณมีสิ่งต่อไปนี้:
- **Aspose.CAD Library** – ดาวน์โหลดได้จาก [here](https://releases.aspose.com/cad/java/).  
- **Document Directory** – โฟลเดอร์บนเครื่องของคุณที่เก็บไฟล์ DGN เข้าและไฟล์ PDF ออก  

## นำเข้าแพ็กเกจ
In your Java project, import the necessary packages to access Aspose.CAD functionalities:

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

ตอนนี้ เราจะแบ่งโค้ดตัวอย่างออกเป็นหลายขั้นตอน:

## ขั้นตอนที่ 1: กำหนดเส้นทางไฟล์ (วิธีส่งออก dgn)

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "Nikon_D90_Camera.dgn";
String outFile  = dataDir + "Nikon_D90_Camera.pdf";
```

ตรวจสอบให้แน่ใจว่าได้แทนที่ `"Your Document Directory"` ด้วยเส้นทางจริงที่ไฟล์ของคุณอยู่

## ขั้นตอนที่ 2: โหลด DGN Image

```java
DgnImage objImage = (DgnImage) Image.load(fileName);
```

โหลดไฟล์ DGN ด้วย Aspose.CAD

## ขั้นตอนที่ 3: ตั้งค่า PDF Export Options (ปรับขนาด pdf, ตั้งค่าตัวเลือก pdf)

```java
PdfOptions options = new PdfOptions();
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
vectorOptions.setAutomaticLayoutsScaling(true);
vectorOptions.setLayouts(new String[] { "1", "2", "3", "9" }); // Export specific views
options.setVectorRasterizationOptions(vectorOptions);
```

ที่นี่เรากำหนดตัวเลือกการส่งออก PDF รวมถึงขนาดหน้า, การสเกลอัตโนมัติ, และเลย์เอาต์ DGN (view) ที่คุณต้องการรวมใน PDF สุดท้าย

## ขั้นตอนที่ 4: บันทึก PDF File

```java
objImage.save(outFile, options);
```

บันทึกไฟล์ PDF ที่ส่งออก เมธอด `save` จะใช้ตัวเลือกทั้งหมดที่คุณกำหนดในขั้นตอนก่อนหน้า

ทำซ้ำขั้นตอนเหล่านี้สำหรับไฟล์ DGN เพิ่มเติมที่คุณต้องการแปลง ขอแสดงความยินดี! คุณได้ทำการ **convert CAD PDF** สำเร็จโดยการส่งออกไฟล์ DGN ไปเป็นรูปแบบ AutoCAD ใน PDF ด้วย Aspose.CAD for Java

## ปัญหาทั่วไปและวิธีแก้
| Issue | Why it Happens | Fix |
|-------|----------------|-----|
| **File not found** | เส้นทาง `dataDir` ไม่ถูกต้อง | ตรวจสอบเส้นทางโฟลเดอร์อีกครั้งและให้แน่ใจว่าไฟล์ DGN มีอยู่ |
| **Blank pages in PDF** | `AutomaticLayoutsScaling` ถูกตั้งเป็น `false` หรือไม่มี ID ของเลย์เอาต์ | คงไว้ `setAutomaticLayoutsScaling(true)` และตรวจสอบชื่อเลย์เอาต์ (`"1","2",…`) |
| **Low‑resolution output** | ค่า DPI ของการเรสเตอร์ไลซ์เริ่มต้นต่ำ | ใช้ `vectorOptions.setResolution(300);` เพื่อเพิ่มคุณภาพ (เพิ่มก่อน `setVectorRasterizationOptions`) |
| **License exception** | ทำงานโดยไม่มีไลเซนส์ที่ถูกต้องในสภาพแวดล้อมการผลิต | ใช้ไลเซนส์ชั่วคราวหรือไลเซนส์ที่ซื้อแล้วตามที่อธิบายในเอกสาร Aspose |

## คำถามที่พบบ่อย (Additional)

**Q: Can I export only a single layout from a multi‑layout DGN file?**  
A: ใช่ – ระบุ ID ของเลย์เอาต์ที่ต้องการใน `vectorOptions.setLayouts(new String[] { "2" });`.

**Q: Is it possible to embed fonts in the resulting PDF?**  
A: Aspose.CAD จะฝังฟอนต์ที่จำเป็นโดยอัตโนมัติเมื่อข้อมูลเวกเตอร์ถูกเรสเตอร์ไลซ์; คุณยังสามารถควบคุมการฝังฟอนต์ผ่าน `PdfOptions` หากต้องการ

**Q: How do I process many DGN files in a batch?**  
A: ใส่ขั้นตอนเหล่านี้ไว้ในลูป `for` ที่วนผ่านรายการชื่อไฟล์ และใช้ `PdfOptions` ตัวเดียวกันสำหรับแต่ละการทำซ้ำ

**Q: Does the library support password‑protected PDFs?**  
A: ใช่ – คุณสามารถตั้งรหัสผ่านบนอ็อบเจกต์ `PdfOptions` ผ่าน `options.setPassword("yourPassword");`.

**Q: Where can I find more examples?**  
A: เอกสารอย่างเป็นทางการของ Aspose.CAD และคลังตัวอย่างมีสถานการณ์เพิ่มเติมหลายอย่าง

## FAQ's (Original)

### Q1: Aspose.CAD รองรับรูปแบบไฟล์ CAD ทั้งหมดหรือไม่?
A1: ใช่, Aspose.CAD รองรับรูปแบบไฟล์ CAD หลากหลาย ทำให้สามารถจัดการกับประเภทไฟล์ต่าง ๆ ได้อย่างหลากหลาย

### Q2: ฉันสามารถปรับแต่งการตั้งค่าการส่งออก PDF ได้หรือไม่?
A2: แน่นอน ตามที่แสดงในบทเรียน คุณสามารถปรับตัวเลือกต่าง ๆ เช่น ขนาดหน้าและเลย์เอาต์ให้ตรงกับความต้องการของคุณ

### Q3: ฉันสามารถหาแหล่งสนับสนุนหรือความช่วยเหลือเพิ่มเติมได้ที่ไหน?
A3: เยี่ยมชม [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) เพื่อรับการสนับสนุนจากชุมชนและการสนทนา

### Q4: มีการทดลองใช้ฟรีหรือไม่?
A4: ใช่, คุณสามารถเข้าถึงการทดลองใช้ฟรีได้จาก [here](https://releases.aspose.com/).

### Q5: ฉันจะขอรับไลเซนส์ชั่วคราวได้อย่างไร?
A5: รับไลเซนส์ชั่วคราวได้จาก [here](https://purchase.aspose.com/temporary-license/).

## สรุป

ในบทเรียนนี้เราได้สำรวจวิธี **convert CAD PDF** ด้วยการใช้ Aspose.CAD for Java ด้วยเพียงไม่กี่บรรทัดของโค้ด คุณสามารถโหลดภาพวาด DGN ปรับแต่งตัวเลือกการส่งออก PDF อย่างละเอียด และสร้าง PDF คุณภาพสูงพร้อมสำหรับการแชร์หรือเก็บรักษา อย่าลังเลที่จะทดลองกับขนาดหน้า, เลย์เอาต์ หรือการประมวลผลเป็นชุดเพื่อให้ตรงกับความต้องการของโครงการของคุณ

---

**อัปเดตล่าสุด:** 2026-05-04  
**ทดสอบด้วย:** Aspose.CAD for Java 24.12  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}