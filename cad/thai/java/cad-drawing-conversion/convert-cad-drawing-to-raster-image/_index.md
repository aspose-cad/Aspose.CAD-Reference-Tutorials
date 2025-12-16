---
date: 2025-12-16
description: เรียนรู้วิธีแปลง CAD เป็น PNG ด้วย Aspose.CAD สำหรับ Java รวมถึงการส่งออก
  DWG เป็นภาพ การบันทึก CAD เป็น PNG และตัวเลือกการแปลง CAD เป็นภาพเรสเตอร์
linktitle: Convert CAD Drawing to Raster Image Format
second_title: Aspose.CAD Java API
title: วิธีแปลง CAD เป็น PNG ด้วย Aspose.CAD สำหรับ Java
url: /th/java/cad-drawing-conversion/convert-cad-drawing-to-raster-image/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# วิธีแปลง CAD เป็น PNG ด้วย Aspose.CAD สำหรับ Java

ในกระบวนการทำงานด้านวิศวกรรมสมัยใหม่ คุณมักต้องการ **แปลง CAD เป็น PNG** เพื่อให้ภาพวาดสามารถแสดงในเบราว์เซอร์ ฝังในเอกสาร หรือแชร์กับผู้มีส่วนได้ส่วนเสียที่ไม่มีซอฟต์แวร์ CAD คู่มือฉบับนี้จะพาคุณผ่านกระบวนการทั้งหมด—ตั้งแต่การโหลดไฟล์ CAD ไปจนถึงการส่งออกภาพ raster PNG คุณภาพสูง—โดยใช้ไลบรารี Aspose.CAD ที่ทรงพลังสำหรับ Java

## คำตอบอย่างรวดเร็ว
- **วัตถุประสงค์หลักคืออะไร?** แปลงภาพวาด CAD เป็นภาพ raster PNG.  
- **ใช้ไลบรารีใด?** Aspose.CAD for Java.  
- **ต้องการไลเซนส์หรือไม่?** มีการทดลองใช้ฟรี; จำเป็นต้องมีไลเซนส์สำหรับการใช้งานในผลิตภัณฑ์.  
- **สามารถปรับขนาดภาพได้หรือไม่?** ได้, ใช้ `CadRasterizationOptions` เพื่อกำหนดความกว้างและความสูง.  
- **รูปแบบ CAD ที่รองรับ?** DWG, DXF, DWF, และอื่น ๆ อีกมาก.

## “แปลง CAD เป็น PNG” คืออะไร?
การแปลง CAD เป็น PNG หมายถึงการทำ raster ให้กับเนื้อหา CAD ที่เป็นเวกเตอร์ (DWG, DXF ฯลฯ) เป็นรูปแบบภาพแบบพิกเซล PNG รักษาความโปร่งใสและคุณภาพ lossless ทำให้เหมาะสำหรับการแสดงตัวอย่างบนเว็บ, เอกสาร, และการรายงาน

## ทำไมต้องแปลง CAD เป็น PNG (CAD เป็นภาพ raster)?
- **การดูที่เป็นสากล:** PNG ทำงานบนอุปกรณ์ใดก็ได้โดยไม่ต้องใช้โปรแกรมดู CAD พิเศษ.  
- **การโหลดที่เร็ว:** ภาพ raster โหลดได้ทันทีในหน้าเว็บ.  
- **การฝังที่ง่าย:** แทรก PNG ลงใน PDF, เอกสาร Word, หรือสไลด์.  
- **ลักษณะที่สม่ำเสมอ:** รักษาน้ำหนักเส้น, สี, และเลเยอร์ให้เหมือนเดิมตามการออกแบบ.

## ข้อกำหนดเบื้องต้น
ก่อนเริ่ม, ตรวจสอบว่าคุณมี:

1. **สภาพแวดล้อมการพัฒนา Java** – JDK 8 หรือใหม่กว่า ติดตั้งและกำหนดค่าแล้ว.  
2. **ไลบรารี Aspose.CAD** – ดาวน์โหลดและเพิ่มไลบรารีลงในโปรเจคของคุณ คุณสามารถหาไลบรารีได้ **[ที่นี่](https://releases.aspose.com/cad/java/)**.

## นำเข้า Namespaces
เพิ่ม import ที่จำเป็นในคลาส Java ของคุณเพื่อให้สามารถทำงานกับวัตถุ Aspose.CAD ได้.

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

## คู่มือขั้นตอนการแปลง CAD เป็น PNG

### ขั้นตอนที่ 1: โหลดภาพวาด CAD
แรกเริ่ม, โหลดไฟล์ CAD ต้นฉบับ (DXF, DWG ฯลฯ) ด้วย `Image.load()`.

```java
String dataDir = "Your Document Directory" + "CADConversion/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

> **เคล็ดลับ:** เก็บไฟล์ CAD ของคุณในโฟลเดอร์เฉพาะ (เช่น `CADConversion`) เพื่อหลีกเลี่ยงปัญหาเส้นทาง.

### ขั้นตอนที่ 2: ตั้งค่า Rasterization Options (ส่งออก dwg เป็นภาพ)
กำหนดขนาดภาพเอาต์พุตและการตั้งค่า raster อื่น ๆ.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1200);
rasterizationOptions.setPageHeight(1200);
```

คุณยังสามารถควบคุมสีพื้นหลัง, โหมดการเรนเดอร์เส้น, และ DPI ที่นี่หากต้องการ.

### ขั้นตอนที่ 3: สร้าง Image Options (บันทึก cad เป็น png)
สร้างอินสแตนซ์ `PngOptions` และแนบการตั้งค่า rasterization.

```java
ImageOptionsBase options = new PngOptions();
options.setVectorRasterizationOptions(rasterizationOptions);
```

### ขั้นตอนที่ 4: บันทึก Raster Image (ไฟล์ cad เป็น png)
สุดท้าย, เขียนไฟล์ PNG ลงดิสก์.

```java
image.save(dataDir + "conic_pyramid_raster_image_out.png", options);
```

ไฟล์ที่ได้ `conic_pyramid_raster_image_out.png` เป็นภาพ PNG ความละเอียดสูงที่แสดงภาพวาด CAD ดั้งเดิมของคุณ.

### ทำซ้ำสำหรับไฟล์อื่น ๆ
เพียงเปลี่ยนค่า `srcFile` ให้ชี้ไปยังไฟล์ CAD อื่นและรันขั้นตอนเดียวกัน โค้ดเดียวกันทำงานได้กับ DWG, DWF, และรูปแบบที่รองรับอื่น ๆ.

## ปัญหาที่พบบ่อยและวิธีแก้

| ปัญหา | วิธีแก้ |
|-------|----------|
| **ผลลัพธ์ PNG ว่าง** | ตรวจสอบว่าไฟล์ CAD ต้นฉบับโหลดอย่างถูกต้อง (`Image.load()` ไม่ควรเกิดข้อยกเว้น). |
| **ขนาดไม่ถูกต้อง** | ปรับ `PageWidth` / `PageHeight` หรือกำหนด DPI ผ่าน `rasterizationOptions.setResolution(...)`. |
| **เลเยอร์หาย** | ตรวจสอบว่าเลเยอร์ของไฟล์ CAD ไม่ได้ถูกซ่อน; ใช้ `CadRasterizationOptions.setDrawType(CadDrawTypeMode.Vector);`. |
| **ข้อผิดพลาดไลเซนส์** | ใช้ไฟล์ไลเซนส์ Aspose.CAD ที่ถูกต้อง (`License license = new License(); license.setLicense("Aspose.CAD.lic");`). |

## คำถามที่พบบ่อย

**Q1: Aspose.CAD รองรับรูปแบบ CAD ทั้งหมดหรือไม่?**  
A1: Aspose.CAD รองรับรูปแบบ CAD มากมาย รวมถึง DWG, DXF, DWF, และอื่น ๆ ดู **[เอกสาร](https://reference.aspose.com/cad/java/)** สำหรับรายการเต็ม.

**Q2: ฉันสามารถปรับแต่ง rasterization options ให้ตรงกับความต้องการของฉันได้หรือไม่?**  
A2: ได้, Aspose.CAD ให้ความยืดหยุ่นในการตั้งค่า rasterization options เพื่อให้คุณสามารถปรับผลลัพธ์ตามความต้องการ (ขนาด, DPI, สีพื้นหลัง, ฯลฯ).

**Q3: ฉันจะหาแหล่งสนับสนุนสำหรับคำถามเกี่ยวกับ Aspose.CAD ได้จากที่ไหน?**  
A3: เยี่ยมชม **[ฟอรั่ม Aspose.CAD](https://forum.aspose.com/c/cad/19)** เพื่อรับความช่วยเหลือและร่วมสนทนากับชุมชน.

**Q4: มีการทดลองใช้ฟรีสำหรับ Aspose.CAD for Java หรือไม่?**  
A4: มี, คุณสามารถสำรวจคุณสมบัติของ Aspose.CAD โดยรับการทดลองใช้ฟรี **[ที่นี่](https://releases.aspose.com/)**.

**Q5: ฉันจะซื้อ Aspose.CAD for Java ได้อย่างไร?**  
A5: เพื่อซื้อ Aspose.CAD for Java, เยี่ยมชม **[หน้าการซื้อ](https://purchase.aspose.com/buy)**.

---

**อัปเดตล่าสุด:** 2025-12-16  
**ทดสอบด้วย:** Aspose.CAD for Java 24.11 (ล่าสุด ณ เวลาที่เขียน)  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}