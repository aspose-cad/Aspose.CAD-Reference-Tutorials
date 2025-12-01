---
date: 2025-12-01
description: เรียนรู้วิธีส่งออกไฟล์ DXF เป็นภาพโดยใช้ Aspose.CAD สำหรับ Java คู่มือขั้นตอนนี้จะแสดงวิธีแปลง
  DXF เป็นภาพและแปลง DWF เป็น JPEG.
language: th
linktitle: Export Specific DXF Layout to Image with Java
second_title: Aspose.CAD Java API
title: วิธีส่งออกเลเอาต์ DXF เป็นภาพด้วย Aspose.CAD ใน Java
url: /java/additional-features/export-specific-layout-to-image/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# วิธีการส่งออกเลเอาต์ DXF เป็นภาพด้วย Aspose.CAD ใน Java

## บทนำ

หากคุณต้องการ **how to export dxf** รูปภาพแบบแรสเตอร์จากไฟล์วาดในแอปพลิเคชัน Java, Aspose.CAD for Java ทำให้กระบวนการเป็นเรื่องง่าย ในบทแนะนำนี้คุณจะได้เห็นวิธี **convert dxf to image** อย่างชัดเจน (และแม้แต่ **convert dwf to jpeg**) โดยการเลือกเลเอาต์ (เลเยอร์) เฉพาะจากไฟล์ต้นฉบับ เราจะเดินผ่านทุกขั้นตอน ตั้งแต่การตั้งค่าโปรเจกต์จนถึงการบันทึกไฟล์ JPEG สุดท้าย เพื่อให้คุณสามารถนำโซลูชันนี้ไปใช้ในโค้ดของคุณได้อย่างมั่นใจ

## คำตอบด่วน
- **What library is required?** Aspose.CAD for Java (มีรุ่นทดลองฟรี).  
- **Which formats can be exported?** DXF, DWF, DWG → JPEG, PNG, BMP, TIFF, etc.  
- **Can I choose a single layout/layer?** Yes – use `CadRasterizationOptions.setLayers()` to specify the desired layers.  
- **Do I need a license for production?** A commercial license is required for non‑evaluation use.  
- **How long does the implementation take?** About 10‑15 minutes for a basic conversion.

## DXF Layout การส่งออกเป็นภาพคืออะไร?
การส่งออกเลเอาต์ DXF หมายถึงการแปลงภาพเวกเตอร์ (DXF/DWF) ให้เป็นรูปแบบบิตแมพเช่น JPEG การทำเช่นนี้เป็นประโยชน์เมื่อคุณต้องการฝังภาพวาดในหน้าเว็บ, สร้างรูปย่อ, หรือแชร์ให้ผู้ใช้ที่ไม่มีซอฟต์แวร์ CAD

## ทำไมต้องแปลง DXF เป็นภาพด้วย Aspose.CAD?
- **No external CAD software** – การแปลงทำงานทั้งหมดใน Java.  
- **Fine‑grained control** – คุณสามารถเลือกเลเยอร์เดี่ยว, ตั้งค่าขนาดหน้า, DPI, และสีพื้นหลังได้.  
- **Broad format support** – นอกจาก JPEG คุณสามารถส่งออกเป็น PNG, BMP, TIFF, และอื่น ๆ.  
- **High fidelity** – ไลบรารีรักษาน้ำหนักเส้น, สี, และฟอนต์ระหว่างการแรสเตอร์อย่างแม่นยำ.

## ข้อกำหนดเบื้องต้น
ก่อนเริ่ม, ตรวจสอบว่าคุณมี:
- **Aspose.CAD for Java** – ดาวน์โหลด JAR เวอร์ชันล่าสุดจาก [Aspose.CAD download page](https://releases.aspose.com/cad/java/).  
- สภาพแวดล้อมการพัฒนา Java (**Java development environment**) (JDK 8 หรือสูงกว่า).  
- ไฟล์ **DXF/DWF** ที่คุณต้องการแปลง (ตัวอย่างใช้ `for_layers_test.dwf`).

## นำเข้า Namespaces
ก่อนอื่น, นำเข้าคลาสที่คุณต้องการใช้.  
```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.fileformats.dwf.whip.objects.DwfWhipLayer;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.dwf.DwfImage;
import com.aspose.cad.imageoptions.JpegOptions;
import java.util.ArrayList;
import java.util.Arrays;
import java.util.List;
```

ตอนนี้เราจะอธิบายกระบวนการแปลงแบบทีละขั้นตอน.

## ขั้นตอนที่ 1: ตั้งค่าโฟลเดอร์ทรัพยากร
กำหนดโฟลเดอร์ที่บรรจุไฟล์ DXF/DWF ต้นฉบับของคุณ.  
```java
String dataDir = "Your Document Directory" + "DXFDrawings\\";
```

> **Pro tip:** ใช้เส้นทางแบบ absolute หรือเส้นทางที่สัมพันธ์กับโฟลเดอร์รากของโปรเจกต์เพื่อหลีกเลี่ยง `FileNotFoundException`.

## ขั้นตอนที่ 2: โหลดภาพ DXF/DWF
โหลดภาพวาดด้วย Aspose.CAD ตัวอย่างใช้ไฟล์ DWF แต่โค้ดเดียวกันทำงานได้กับ DXF.  
```java
String srcFile = dataDir + "for_layers_test.dwf";
DwfImage image = (DwfImage) Image.load(srcFile);
```

> **Why DWF?** ไลบรารีจัดการ DWF คล้ายกับ DXF ดังนั้นตัวเลือกการแรสเตอร์จะเหมือนกัน ทำให้คุณสามารถ **convert dwf to jpeg** ได้อย่างง่ายดาย.

## ขั้นตอนที่ 3: ดึงชื่อเลเยอร์
ดึงชื่อเลเยอร์ทั้งหมดเพื่อให้คุณเลือกเลเยอร์ที่ต้องการส่งออก.  
```java
List<String> layersNames = image.getLayers().getLayersNames();
```

ตอนนี้คุณมี `List<String>` ที่บรรจุชื่อของแต่ละเลเอาต์.

## ขั้นตอนที่ 4: ตั้งค่าตัวเลือกการแรสเตอร์
กำหนดขนาดภาพเอาต์พุต, ความละเอียด, และการตั้งค่าแรสเตอร์อื่น ๆ.  
```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
```

ปรับ `PageWidth` และ `PageHeight` ให้ตรงกับขนาดภาพที่ต้องการ คุณยังสามารถตั้งค่า DPI ผ่าน `setResolution` ได้.

## ขั้นตอนที่ 5: ระบุเลเยอร์ (เลือกเลเอาต์)
แปลงรายการเลเยอร์ให้เป็นรูปแบบที่ `setLayers()` ต้องการและเลือกเลเยอร์ที่ต้องการเรนเดอร์.  
```java
String[] stringArray = Arrays.copyOf(layersNames.toArray(), layersNames.toArray().length, String[].class);
List<String> stringList = Arrays.asList(stringArray);
rasterizationOptions.setLayers(stringList);
```

หากคุณต้องการเพียงเลเอาต์เดียว, ให้แทนที่ `stringList` ด้วยรายการที่มีชื่อเลเยอร์นั้นเท่านั้น.

## ขั้นตอนที่ 6: ตั้งค่า JPEG Options
ห่อหุ้มการตั้งค่าแรสเตอร์ภายในอ็อบเจ็กต์ `JpegOptions`.  
```java
JpegOptions jpegOptions = new JpegOptions();
jpegOptions.setVectorRasterizationOptions(rasterizationOptions);
```

คุณยังสามารถตั้งค่าคุณภาพ JPEG (`jpegOptions.setQuality(90)`) หากต้องการ.

## ขั้นตอนที่ 7: ส่งออก DXF/DWF เป็นภาพ
สุดท้าย, บันทึกภาพที่แรสเตอร์ลงดิสก์.  
```java
String output = dataDir + "for_layers_test.jpg";
image.save(output, jpegOptions);
```

ไฟล์ `for_layers_test.jpg` ตอนนี้มีเลเอาต์ที่เลือกแสดงเป็น JPEG คุณภาพสูง.

## ปัญหาที่พบบ่อยและวิธีแก้
| ปัญหา | สาเหตุ | วิธีแก้ |
|-------|--------|----------|
| **ภาพผลลัพธ์เป็นสีขาว** | ชื่อเลเยอร์ไม่ถูกต้องหรือรายการเลเยอร์ว่างเปล่า | ตรวจสอบว่า `layersNames` มีชื่อที่คาดหวังและส่งรายการที่ถูกต้องไปยัง `setLayers()`. |
| **ข้อผิดพลาดหน่วยความจำไม่พอ** | ขนาดหน้าที่ใหญ่เกินไป | ลด `PageWidth/PageHeight` หรือเพิ่มขนาด heap ของ JVM (`-Xmx`). |
| **รูปแบบไฟล์ที่ไม่รองรับ** | ใช้เวอร์ชันเก่าของ Aspose.CAD | อัปเดตเป็น JAR เวอร์ชันล่าสุดจาก Aspose. |
| **คุณภาพภาพต่ำ** | คุณภาพ JPEG เริ่มต้นต่ำ | เรียก `jpegOptions.setQuality(95)` ก่อนบันทึก. |

## คำถามที่พบบ่อย
**Q: ฉันสามารถส่งออกหลายเลเอาต์ DXF ในการทำงานเดียวได้หรือไม่?**  
A: ได้. วนลูปผ่านชื่อเลเยอร์ที่ต้องการ, อัปเดต `rasterizationOptions.setLayers()` ในแต่ละรอบ, และเรียก `image.save()` พร้อมชื่อไฟล์ผลลัพธ์ที่ไม่ซ้ำกัน.

**Q: Aspose.CAD for Java รองรับกับเวอร์ชัน Java ทั้งหมดหรือไม่?**  
A: ไลบรารีรองรับ Java 8 ขึ้นไป ตรวจสอบบันทึกการปล่อยเวอร์ชันสำหรับหมายเหตุเฉพาะเวอร์ชัน.

**Q: ฉันจะจัดการข้อผิดพลาดระหว่างการแปลงอย่างไร?**  
A: ห่อโค้ดการแปลงในบล็อก `try‑catch` และจับ `Exception` หรือข้อยกเว้นเฉพาะของ Aspose เพื่อบันทึกหรือแสดงข้อความที่มีความหมาย.

**Q: นอกจาก JPEG แล้ว มีรูปแบบภาพอื่นใดบ้างที่พร้อมใช้งาน?**  
A: คุณสามารถใช้ `PngOptions`, `BmpOptions`, `TiffOptions` เป็นต้น โดยเปลี่ยน `JpegOptions` เป็นคลาสที่เหมาะสม.

**Q: ฉันสามารถปรับสีพื้นหลังหรือความหนาของเส้นได้หรือไม่?**  
A: ได้. `CadRasterizationOptions` มีคุณสมบัติเช่น `setBackgroundColor()` และ `setLineWeight()` สำหรับการปรับแต่งละเอียด.

---

**อัปเดตล่าสุด:** 2025-12-01  
**ทดสอบด้วย:** Aspose.CAD for Java 24.11 (latest at time of writing)  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}