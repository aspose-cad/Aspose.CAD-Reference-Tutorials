---
date: 2025-12-18
description: เรียนรู้วิธีแปลง DWG เป็น PNG และรูปแบบภาพเรสเตอร์อื่น ๆ ด้วย Aspose.CAD
  สำหรับ Java ส่งออก CAD เป็น PNG ด้วยผลลัพธ์คุณภาพสูง
linktitle: Convert CAD Layout to Raster Image Format
second_title: Aspose.CAD Java API
title: แปลงไฟล์ DWG เป็น PNG และรูปแบบเรสเตอร์อื่น ๆ ด้วย Aspose.CAD สำหรับ Java
url: /th/java/cad-drawing-conversion/convert-cad-layout-to-raster-image/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# แปลง DWG เป็น PNG และรูปแบบเรสเตอร์อื่น ๆ ด้วย Aspose.CAD สำหรับ Java

## บทนำ

การแปลง DWG เป็น PNG (หรือรูปแบบภาพเรสเตอร์อื่น ๆ) เป็นความต้องการทั่วไปเมื่อคุณต้องการแชร์แบบ CAD ให้กับทีมที่ไม่มีโปรแกรมดู CAD ฝังการออกแบบในเอกสาร หรือสร้างภาพย่อสำหรับแกลเลอรีบนเว็บ Aspose.CAD สำหรับ Java ทำให้การแปลงนี้ง่ายดาย ไม่ว่าคุณจะทำงานกับไฟล์แบบเต็มหรือเพียงเลย์เอาต์เฉพาะ ในบทแนะนำนี้เราจะเดินผ่านขั้นตอนที่แน่นอนเพื่อ **แปลงเลย์เอาต์ CAD เป็นภาพเรสเตอร์**—เทคนิคเดียวกันที่คุณสามารถใช้ผลิต PNG, JPEG, TIFF หรือ PDF ได้

## คำตอบสั้น ๆ
- **ไลบรารีที่จัดการการแปลง DWG เป็น PNG คืออะไร?** Aspose.CAD สำหรับ Java  
- **สามารถส่งออกเป็นฟอร์แมตอะไรได้บ้าง?** PNG, JPEG, TIFF, PDF, BMP และอื่น ๆ  
- **ต้องใช้ไลเซนส์สำหรับการทดสอบหรือไม่?** เวอร์ชันทดลองฟรีใช้ได้สำหรับการพัฒนา; ต้องมีไลเซนส์สำหรับการใช้งานจริง  
- **สามารถเลือกเลย์เอาต์เฉพาะได้หรือไม่?** ใช่, ใช้ `setLayouts` เพื่อระบุ “Model”, “Layout1” เป็นต้น  
- **สามารถสร้างผลลัพธ์ความละเอียดสูงได้หรือไม่?** แน่นอน—ปรับ `setPageWidth` และ `setPageHeight` เพื่อควบคุม DPI  

## “convert dwg to png” คืออะไร?

วลี “convert dwg to png” หมายถึงกระบวนการนำไฟล์ DWG ที่เป็นเวกเตอร์ (ฟอร์แมตดั้งเดิมของหลายแอปพลิเคชัน CAD) มาทำให้เป็นภาพ PNG ที่เป็นพิกเซล รูปภาพเรสเตอร์เหมาะสำหรับการแสดงบนเว็บ, การแชร์อีเมล, และการรวมเข้ากับซอฟต์แวร์ที่ไม่ใช่ CAD

## ทำไมต้องส่งออก CAD เป็น PNG (หรือรูปแบบเรสเตอร์อื่น ๆ)?

- **ความเข้ากันได้ทั่วโลก:** PNG และ JPEG รองรับโดยโปรแกรมดูภาพและเบราว์เซอร์เกือบทุกตัว  
- **การโหลดที่รวดเร็ว:** ภาพเรสเตอร์โหลดทันทีเมื่อเทียบกับการเปิดไฟล์ DWG ขนาดใหญ่  
- **การฝังที่ง่าย:** แทรก PNG ลงใน Word, PowerPoint หรือ HTML ได้โดยไม่ต้องใช้ปลั๊กอินเพิ่มเติม  
- **ลักษณะที่สม่ำเสมอ:** คุณควบคุมความละเอียด, พื้นหลัง, และเลย์เอาต์ ทำให้ทุกผู้มีส่วนได้ส่วนเสียเห็นภาพเดียวกัน  

## ข้อกำหนดเบื้องต้น

ก่อนเริ่มทำตามขั้นตอนต่อไปนี้ให้แน่ใจว่าคุณมี:

1. **สภาพแวดล้อมการพัฒนา Java** – JDK 8 หรือใหม่กว่า ติดตั้งและกำหนดค่าเรียบร้อยแล้ว  
2. **Aspose.CAD สำหรับ Java** – ดาวน์โหลด JAR ล่าสุดจาก [เอกสาร Aspose.CAD สำหรับ Java](https://reference.aspose.com/cad/java/)  

## นำเข้า Namespaces

ก่อนอื่นให้นำเข้าคลาสที่จำเป็น การนำเข้านี้ทำให้คุณเข้าถึงการโหลดภาพ, ตัวเลือกการเรสเตอร์ไลซ์, และการตั้งค่าเอาต์พุต TIFF/PNG

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

> **เคล็ดลับ:** หากต้องการส่งออกเป็น PNG แทน TIFF ให้เปลี่ยน `TiffOptions` เป็น `PngOptions` (อยู่ใน `com.aspose.cad.imageoptions.PngOptions`)

## คู่มือแบบขั้นตอน

### ขั้นตอนที่ 1: ตั้งค่าโฟลเดอร์ทรัพยากร

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";
```

เปลี่ยน `"Your Document Directory"` ให้เป็นพาธเต็มที่เก็บไฟล์ CAD ของคุณ

### ขั้นตอนที่ 2: โหลดไฟล์ CAD

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

คุณสามารถโหลดฟอร์แมตที่รองรับได้ทุกประเภท (DWG, DXF, DGN ฯลฯ) ส่วนนี้คือ **วิธีแปลง cad** เพียงระบุไฟล์และให้ Aspose จัดการการพาร์ส

### ขั้นตอนที่ 3: ตั้งค่าตัวเลือกการเรสเตอร์ไลซ์

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1200);
rasterizationOptions.setPageHeight(1200);
rasterizationOptions.setLayouts(new String[] {"Model", "Layout1"});
```

- `setPageWidth` / `setPageHeight` ควบคุมความละเอียดของผลลัพธ์ (ค่ามาก = DPI สูง)  
- `setLayouts` ให้คุณ **แปลง cad เป็นเรสเตอร์** สำหรับเลย์เอาต์เฉพาะ; ไม่กำหนดจะทำการเรสเตอร์ไลซ์ทั้งภาพวาด

### ขั้นตอนที่ 4: ตั้งค่าตัวเลือกภาพ

```java
ImageOptionsBase options = new TiffOptions(TiffExpectedFormat.Default);
options.setVectorRasterizationOptions(rasterizationOptions);
```

หากต้องการ PNG ให้สร้างอินสแตนซ์ `PngOptions` แทน `TiffOptions` นี่คือจุดที่คุณ **ส่งออก cad เป็น png**

### ขั้นตอนที่ 5: บันทึกภาพผลลัพธ์

```java
image.save(dataDir + "conic_pyramid_layoutstorasterimage_out_.tiff", options);
```

เปลี่ยนนามสกุลไฟล์เป็น `.png` (และอ็อบเจกต์ options เป็น `PngOptions`) เพื่อ **บันทึก CAD เป็น JPEG/PNG**

> **ข้อผิดพลาดทั่วไป:** ลืมให้ส่วนขยายไฟล์ตรงกับคลาส options จะทำให้เกิด `UnsupportedFormatException` ควรตรวจสอบให้ตรงกันเสมอ

## ปัญหาที่พบบ่อยและวิธีแก้

| ปัญหา | วิธีแก้ |
|-------|----------|
| **ภาพผลลัพธ์เป็นสีขาว** | ตรวจสอบว่าชื่อเลย์เอาต์ใน `setLayouts` ตรงกับชื่อในไฟล์ CAD ต้นฉบับ |
| **PNG ความละเอียดต่ำ** | เพิ่มค่า `setPageWidth` / `setPageHeight` หรือกำหนด `setResolution` ในตัวเลือกการเรสเตอร์ไลซ์ |
| **เวอร์ชัน DWG ไม่รองรับ** | ใช้เวอร์ชันล่าสุดของ Aspose.CAD; เวอร์ชันเก่าอาจไม่รองรับ DWG รุ่นใหม่ |
| **ข้อผิดพลาดหน่วยความจำกับไฟล์ขนาดใหญ่** | ประมวลผลหน้าแต่ละหน้าแยกกันหรือเพิ่ม heap ของ JVM (`-Xmx2g`) |

## คำถามที่พบบ่อย

**ถาม: Aspose.CAD รองรับฟอร์แมตไฟล์ CAD ต่าง ๆ หรือไม่?**  
ตอบ: รองรับ DWG, DXF, DGN และอื่น ๆ อีกหลายประเภท

**ถาม: สามารถปรับความละเอียดของภาพเรสเตอร์ที่ส่งออกได้หรือไม่?**  
ตอบ: แน่นอน ปรับ `setPageWidth`, `setPageHeight` หรือ `setResolution` ใน `CadRasterizationOptions`

**ถาม: จะทำอย่างไรให้แปลงหลายเลย์เอาต์ CAD ในการรันเดียว?**  
ตอบ: ส่งอาร์เรย์ชื่อเลย์เอาต์ทั้งหมดให้กับ `setLayouts` เช่น `new String[]{"Model","Layout1","Layout2"}`

**ถาม: มีฟอร์แมตเอาต์พุตอื่นนอกจาก TIFF หรือไม่?**  
ตอบ: มี—PNG, JPEG, BMP, PDF และอื่น ๆ ผ่านคลาส `*Options` ที่เกี่ยวข้อง

**ถาม: จะหาความช่วยเหลือหรือแชร์ประสบการณ์กับ Aspose.CAD ได้ที่ไหน?**  
ตอบ: เยี่ยมชม [ฟอรั่ม Aspose.CAD](https://forum.aspose.com/c/cad/19) เพื่อรับการสนับสนุนจากชุมชนและทีมงานอย่างเป็นทางการ

## สรุป

โดยทำตามขั้นตอนเหล่านี้คุณสามารถ **แปลง DWG เป็น PNG**, **ส่งออก CAD เป็น PNG**, **บันทึก CAD เป็น JPEG** หรือสร้างรูปแบบเรสเตอร์อื่น ๆ ที่ต้องการ Aspose.CAD สำหรับ Java จะทำงานหนักให้คุณ คุณจึงมุ่งเน้นที่การนำภาพคุณภาพสูงไปใช้ในแอปพลิเคชัน, เอกสาร หรือพอร์ทัลเว็บของคุณได้เลย

---

**อัปเดตล่าสุด:** 2025-12-18  
**ทดสอบกับ:** Aspose.CAD สำหรับ Java 24.12  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}