---
date: 2026-02-17
description: เรียนรู้วิธีแปลง DWG เป็น PNG และส่งออก CAD เป็น PNG หรือรูปแบบเรสเตอร์อื่น
  ๆ ด้วย Aspose.CAD for Java รับผลลัพธ์คุณภาพสูงอย่างรวดเร็ว.
linktitle: Convert CAD Layout to Raster Image Format
second_title: Aspose.CAD Java API
title: แปลง DWG เป็น PNG และรูปแบบเรสเตอร์อื่น ๆ ด้วย Aspose.CAD สำหรับ Java
url: /th/java/cad-drawing-conversion/convert-cad-layout-to-raster-image/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# แปลง DWG เป็น PNG และรูปแบบ Raster อื่น ๆ ด้วย Aspose.CAD for Java

## บทนำ

การแปลง DWG เป็น PNG (หรือรูปแบบภาพ raster อื่น) เป็นความต้องการทั่วไปเมื่อคุณต้องการแชร์แบบ CAD ให้กับทีมที่ไม่มีโปรแกรมดู CAD ฝังการออกแบบในเอกสาร หรือสร้างภาพย่อสำหรับแกลเลอรีเว็บ **ในคู่มือนี้คุณจะได้เรียนรู้วิธีแปลง dwg เป็น png อย่างรวดเร็วและเชื่อถือได้** ไม่ว่าคุณจะทำงานกับไฟล์แบบเต็มหรือเพียงเลย์เอาต์เฉพาะ คุณอาจต้อง **แปลง CAD เป็น raster** สำหรับการแสดงตัวอย่างบนเว็บ เครื่องมือรายงาน หรือแอปมือถือ Aspose.CAD for Java ทำให้การแปลงนี้ง่ายดายและให้คุณควบคุมความละเอียด เลือกเลย์เอาต์ และรูปแบบผลลัพธ์ได้เต็มที่

## คำตอบสั้น
- **ไลบรารีที่จัดการ DWG เป็น PNG คืออะไร?** Aspose.CAD for Java  
- **สามารถส่งออกรูปแบบใดได้บ้าง?** PNG, JPEG, TIFF, PDF, BMP และอื่น ๆ  
- **ต้องใช้ไลเซนส์สำหรับการทดสอบหรือไม่?** ทดลองใช้ฟรีได้สำหรับการพัฒนา; ต้องมีไลเซนส์สำหรับการใช้งานจริง  
- **สามารถเลือกเลย์เอาต์เฉพาะได้หรือไม่?** ได้, ใช้ `setLayouts` เพื่อระบุ “Model”, “Layout1” เป็นต้น  
- **สามารถสร้างผลลัพธ์ความละเอียดสูงได้หรือไม่?** แน่นอน—ปรับ `setPageWidth` และ `setPageHeight` เพื่อควบคุม DPI  

## “convert dwg to png” คืออะไร?

วลี “convert dwg to png” หมายถึงกระบวนการนำไฟล์ DWG ที่เป็นเวกเตอร์ (รูปแบบดั้งเดิมของหลายแอปพลิเคชัน CAD) มาทำ rasterization ให้เป็นภาพ PNG ที่เป็นพิกเซล ภาพ raster เหมาะสำหรับการแสดงบนเว็บ การแชร์อีเมล และการรวมเข้ากับซอฟต์แวร์ที่ไม่ใช่ CAD

## ทำไมต้องส่งออก CAD เป็น PNG (หรือ raster format อื่น)?

- **ความเข้ากันได้ทั่วโลก:** PNG และ JPEG รองรับโดยโปรแกรมดูภาพและเบราว์เซอร์เกือบทุกตัว  
- **โหลดเร็ว:** ภาพ raster โหลดทันทีเมื่อเทียบกับการเปิดไฟล์ DWG ขนาดใหญ่  
- **ฝังง่าย:** แทรก PNG ลงใน Word, PowerPoint หรือ HTML ได้โดยไม่ต้องใช้ปลั๊กอินเพิ่มเติม  
- **รูปลักษณ์สม่ำเสมอ:** คุณควบคุมความละเอียด พื้นหลัง และเลย์เอาต์ ทำให้ทุกคนเห็นภาพเดียวกัน  

## กรณีการใช้งานทั่วไป

| สถานการณ์ | ทำไมผลลัพธ์ raster จึงช่วยได้ |
|----------|------------------------|
| **เอกสารโครงการ** | การฝัง PNG ใน PDF หรือ Word ทำให้ผู้ตรวจสอบไม่ต้องมีซอฟต์แวร์ CAD |
| **พอร์ทัลเว็บ** | ภาพย่อที่สร้างจากไฟล์ DWG โหลดทันทีและปรับปรุงประสบการณ์ผู้ใช้ |
| **แอปมือถือ** | ภาพ raster แสดงผลได้อย่างถูกต้องบนอุปกรณ์ที่ไม่มีโปรแกรมดู CAD |
| **การรายงานอัตโนมัติ** | แปลงหลายเลย์เอาต์เป็น PNG/JPEG พร้อมกันเพื่อใส่ในแผนภูมิหรือแดชบอร์ด |

## ข้อกำหนดเบื้องต้น

ก่อนเริ่มทำตามขั้นตอนต่อไปนี้ให้ตรวจสอบว่าคุณมี:

1. **สภาพแวดล้อมการพัฒนา Java** – ติดตั้ง JDK 8 หรือใหม่กว่าและตั้งค่าเรียบร้อย  
2. **Aspose.CAD for Java** – ดาวน์โหลด JAR เวอร์ชันล่าสุดจาก [เอกสาร Aspose.CAD for Java](https://reference.aspose.com/cad/java/)  

## นำเข้า Namespace

แรกเริ่มให้ import คลาสที่จำเป็น การ import นี้ทำให้คุณเข้าถึงการโหลดภาพ ตัวเลือก rasterization และการตั้งค่าออก TIFF/PNG

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

> **เคล็ดลับ:** หากต้องการ **ส่งออก CAD เป็น PNG** แทน TIFF ให้เปลี่ยน `TiffOptions` เป็น `PngOptions` (อยู่ใน `com.aspose.cad.imageoptions.PngOptions`)

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

คุณสามารถโหลดไฟล์รูปแบบที่รองรับใดก็ได้ (DWG, DXF, DGN ฯลฯ) นี่คือส่วน **วิธีแปลง cad** เพียงชี้ไปที่ไฟล์และให้ Aspose จัดการการพาร์ส

### ขั้นตอนที่ 3: ตั้งค่าตัวเลือก Rasterization

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1200);
rasterizationOptions.setPageHeight(1200);
rasterizationOptions.setLayouts(new String[] {"Model", "Layout1"});
```

- `setPageWidth` / `setPageHeight` ควบคุมความละเอียดผลลัพธ์ (ค่ามาก = DPI สูง)  
- `setLayouts` ให้คุณ **แปลง CAD เป็น raster** สำหรับเลย์เอาต์เฉพาะ; ไม่กำหนดจะ rasterize ทั้งหมด

### ขั้นตอนที่ 4: ตั้งค่า Image Options

```java
ImageOptionsBase options = new TiffOptions(TiffExpectedFormat.Default);
options.setVectorRasterizationOptions(rasterizationOptions);
```

หากต้องการ PNG ให้สร้าง `PngOptions` แทน `TiffOptions` นี่คือจุดที่คุณ **ส่งออก CAD เป็น PNG**

### ขั้นตอนที่ 5: บันทึกภาพผลลัพธ์

```java
image.save(dataDir + "conic_pyramid_layoutstorasterimage_out_.tiff", options);
```

เปลี่ยนนามสกุลไฟล์เป็น `.png` (และอ็อบเจ็กต์ options เป็น `PngOptions`) เพื่อ **บันทึก CAD เป็น JPEG/PNG**

> **ข้อผิดพลาดทั่วไป:** ลืมให้สอดคล้องระหว่างนามสกุลไฟล์กับคลาส options จะทำให้เกิด `UnsupportedFormatException` ควรตรวจสอบให้ตรงกันเสมอ

## ปัญหาที่พบบ่อยและวิธีแก้

| ปัญหา | วิธีแก้ |
|-------|----------|
| **ภาพผลลัพธ์เป็นสีขาว** | ตรวจสอบว่าชื่อเลย์เอาต์ใน `setLayouts` ตรงกับชื่อในไฟล์ CAD ต้นฉบับ |
| **PNG ความละเอียดต่ำ** | เพิ่มค่า `setPageWidth` / `setPageHeight` หรือกำหนด `setResolution` ใน rasterization options |
| **ไม่รองรับเวอร์ชัน DWG** | ใช้ Aspose.CAD เวอร์ชันล่าสุด; เวอร์ชันเก่าอาจไม่รองรับ DWG ใหม่ |
| **ข้อผิดพลาดหน่วยความจำกับไฟล์ขนาดใหญ่** | ประมวลผลหน้าแต่ละหน้าแยกกันหรือเพิ่ม heap ของ JVM (`-Xmx2g`) |

## คำถามที่พบบ่อย

**ถาม: Aspose.CAD รองรับรูปแบบไฟล์ CAD ต่าง ๆ หรือไม่?**  
ตอบ: รองรับ DWG, DXF, DGN และอื่น ๆ มากมาย

**ถาม: สามารถปรับความละเอียดของภาพ raster ที่ออกได้หรือไม่?**  
ตอบ: แน่นอน ปรับ `setPageWidth`, `setPageHeight` หรือ `setResolution` ใน `CadRasterizationOptions`

**ถาม: จะทำอย่างไรให้แปลงหลายเลย์เอาต์ของ CAD ในการรันเดียว?**  
ตอบ: ส่งอาเรย์ชื่อเลย์เอาต์ทั้งหมดให้กับ `setLayouts` เช่น `new String[]{"Model","Layout1","Layout2"}`

**ถาม: มีรูปแบบผลลัพธ์อื่นนอกจาก TIFF หรือไม่?**  
ตอบ: มี—PNG, JPEG, BMP, PDF และอื่น ๆ ผ่านคลาส `*Options` ที่เกี่ยวข้อง

**ถาม: จะหาความช่วยเหลือหรือแชร์ประสบการณ์กับ Aspose.CAD ได้ที่ไหน?**  
ตอบ: เยี่ยมชม [ฟอรั่ม Aspose.CAD](https://forum.aspose.com/c/cad/19) เพื่อรับการสนับสนุนจากชุมชนและทีมงานอย่างเป็นทางการ

## สรุป

โดยทำตามขั้นตอนเหล่านี้คุณสามารถ **แปลง DWG เป็น PNG**, **ส่งออก CAD เป็น PNG**, **บันทึก CAD เป็น JPEG** หรือสร้าง raster format ใด ๆ ที่ต้องการ Aspose.CAD for Java จะจัดการส่วนที่ยุ่งยากให้คุณ ทำให้คุณมุ่งเน้นที่การนำภาพคุณภาพสูงไปใช้ในแอปพลิเคชัน เอกสาร หรือพอร์ทัลเว็บของคุณได้อย่างเต็มที่

---

**อัปเดตล่าสุด:** 2026-02-17  
**ทดสอบกับ:** Aspose.CAD for Java 24.12  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}