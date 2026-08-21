---
date: 2026-04-13
description: เรียนรู้วิธีการแปลงเลเยอร์ CAD เป็นภาพเรสเตอร์ด้วย Java โดยใช้ Aspose.CAD
  for Java คู่มือแบบทีละขั้นตอนนี้แสดงการแปลงระดับเลเยอร์เป็นภาพเรสเตอร์.
keywords:
- java rasterize cad layer
- Aspose CAD Java
- convert CAD layer to raster
linktitle: แปลงเลเยอร์ CAD เป็นรูปแบบภาพเรสเตอร์
second_title: Aspose.CAD Java API
title: Java แปลงชั้น CAD เป็นเรสเตอร์ – บทแนะนำ Aspose CAD
url: /th/java/cad-drawing-conversion/convert-cad-layer-to-raster-image/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# บทแนะนำ Aspose CAD Java: แปลงชั้น CAD เป็นรูปแบบภาพเรสเตอร์

## บทนำ

หากคุณต้องการ **java rasterize cad layer** ไฟล์เพื่อการแชร์ การพิมพ์ หรือการประมวลผลภาพต่อไปอย่างง่ายดาย คุณมาถูกที่แล้ว ในบทแนะนำนี้เราจะอธิบายว่า Aspose.CAD for Java จะช่วยให้คุณเลือกชั้นเฉพาะจากภาพวาด CAD และส่งออกเป็นภาพเรสเตอร์คุณภาพสูงเช่น JPEG, PNG หรือ BMP อย่างไร เมื่อเสร็จสิ้นคุณจะเข้าใจว่าการเรสเตอร์ไลซ์แบบเลือกชั้นมีความสำคัญอย่างไร วิธีการกำหนดค่าตัวเลือกการเรสเตอร์ไลซ์ และวิธีบันทึกผลลัพธ์ด้วยเพียงไม่กี่บรรทัดของโค้ด

## คำตอบอย่างรวดเร็ว
- **หัวข้อของบทแนะนำนี้คืออะไร?** การแปลงชั้น CAD ที่เลือกเป็นภาพเรสเตอร์โดยใช้ Aspose.CAD for Java.  
- **รูปแบบใดบ้างที่รองรับ?** รูปแบบเรสเตอร์ใด ๆ ที่ Aspose รองรับ (JPEG, PNG, BMP, ฯลฯ).  
- **ฉันต้องการไลเซนส์หรือไม่?** การทดลองใช้ฟรีทำงานสำหรับการพัฒนา; จำเป็นต้องมีไลเซนส์สำหรับการใช้งานจริง.  
- **ข้อกำหนดเบื้องต้นคืออะไร?** สภาพแวดล้อมการพัฒนา Java และไลบรารี Aspose.CAD Java.  
- **การดำเนินการใช้เวลานานเท่าไหร่?** ประมาณ 10–15 นาทีสำหรับการแปลงพื้นฐาน.

## อะไรคือ “java rasterize cad layer”?

การเรสเตอร์ไลซ์ชั้น CAD หมายถึงการแปลงข้อมูลเวกเตอร์ของชั้นนั้นเป็นภาพที่อิงพิกเซล กระบวนการนี้รักษาลักษณะการแสดงผลของชั้นไว้ในขณะที่ทำให้เข้ากันได้กับระบบใด ๆ ที่สามารถแสดงรูปแบบภาพมาตรฐานได้

## ทำไมต้องใช้วิธีนี้?

- **การส่งออกแบบเลือก** – เราเรนเดอร์เฉพาะชั้นที่ต้องการเท่านั้น ลดขนาดไฟล์และเวลาประมวลผล.  
- **ความยืดหยุ่นของรูปแบบ** – เปลี่ยน `JpegOptions` เป็น `PngOptions`, `BmpOptions` ฯลฯ ได้โดยไม่ต้องแก้ไขตรรกะหลัก.  
- **การเรนเดอร์คุณภาพสูง** – Aspose.CAD รักษาน้ำหนักเส้น, สี, และข้อความให้ตรงกับไฟล์ CAD ต้นฉบับ.

## ข้อกำหนดเบื้องต้น

ก่อนจะลงมือเขียนโค้ด โปรดตรวจสอบว่าคุณมีสิ่งต่อไปนี้:

- **สภาพแวดล้อมการพัฒนา Java** – ติดตั้งและกำหนดค่า JDK 8 หรือสูงกว่า.  
- **ไลบรารี Aspose.CAD** – ดาวน์โหลดและติดตั้งไลบรารี Aspose.CAD สำหรับ Java จาก [ลิงก์ดาวน์โหลด](https://releases.aspose.com/cad/java/).  

## นำเข้า Namespaces

ในขั้นตอนนี้ เราจะนำเข้าคลาสที่จำเป็นเพื่อเริ่มทำงานกับไฟล์ CAD

### นำเข้าคลาส Aspose.CAD

ในไฟล์ซอร์ส Java ของคุณ ให้เพิ่มการนำเข้า Aspose.CAD ที่ต้องการ:

```java
import com.aspose.cad.Image;


import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
import java.util.ArrayList;
import java.util.Arrays;
import java.util.List;
```

## แปลงชั้น CAD เป็นรูปแบบภาพเรสเตอร์

ต่อไปนี้เป็นกระบวนการแบบครบถ้วน ทีละขั้นตอน แต่ละขั้นจะอธิบายด้วยภาษาง่าย ๆ ก่อนโค้ดบล็อก เพื่อให้คุณเข้าใจสิ่งที่กำลังเกิดขึ้น

### ขั้นตอนที่ 1: ตั้งค่าไฟล์ CAD

แรกสุด ให้ระบุไฟล์ CAD ของคุณและโหลดเข้าอ็อบเจ็กต์ `Image`

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

### ขั้นตอนที่ 2: กำหนดค่าตัวเลือกการเรสเตอร์ไลซ์

สร้างอินสแตนซ์ `CadRasterizationOptions` เพื่อกำหนดขนาดและคุณภาพของภาพผลลัพธ์

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(500);
rasterizationOptions.setPageHeight(500);
```

### ขั้นตอนที่ 3: ระบุชั้น CAD

เพิ่มชื่อชั้นที่คุณต้องการเรสเตอร์ไลซ์ ในตัวอย่างนี้เราจะส่งออกชั้นเริ่มต้น `"0"`

```java
List<String> stringList = new ArrayList<>(Arrays.asList("0"));
rasterizationOptions.setLayers(stringList);
```

### ขั้นตอนที่ 4: ตั้งค่าตัวเลือก JPEG

สร้างอ็อบเจ็กต์ `JpegOptions` (หรือตัวเลือกภาพเรสเตอร์อื่น) และเชื่อมโยงกับการตั้งค่าการเรสเตอร์ไลซ์

```java
JpegOptions options = new JpegOptions();
options.setVectorRasterizationOptions(rasterizationOptions);
```

### ขั้นตอนที่ 5: ส่งออกเป็น JPEG

สุดท้าย บันทึกชั้นที่เรสเตอร์ไลซ์เป็นไฟล์ JPEG

```java
image.save(dataDir + "CADLayersToRasterImageFormats_out_.jpg", options);
```

ทำซ้ำขั้นตอนข้างต้นสำหรับชั้นเพิ่มเติมหรือปรับพารามิเตอร์การเรสเตอร์ไลซ์ (ความละเอียด, สีพื้นหลัง, ฯลฯ) ให้ตรงกับความต้องการของคุณ

## ปัญหาทั่วไปและการแก้ไขปัญหา

| อาการ | สาเหตุที่เป็นไปได้ | วิธีแก้ไข |
|---------|--------------|-----|
| ผลลัพธ์เป็นภาพสีขาว | ไม่ได้ระบุชั้นหรือระบุชื่อชั้นผิด | ตรวจสอบว่าชื่อชั้นมีอยู่ในไฟล์ CAD; ใช้ `image.getLayers()` เพื่อแสดงรายการชั้น. |
| ความละเอียดต่ำ | DPI เริ่มต้นต่ำ | ตั้งค่า `rasterizationOptions.setResolution(300);` (หรือสูงกว่า) ก่อนบันทึก. |
| ไม่รองรับรูปแบบ CAD | ใช้เวอร์ชัน Aspose.CAD เก่ากว่า | อัปเดตเป็นรุ่นล่าสุดของ Aspose.CAD for Java. |

## คำถามที่พบบ่อย

**ถาม: ฉันสามารถใช้ Aspose.CAD for Java กับภาษาโปรแกรมอื่นได้หรือไม่?**  
ตอบ: Aspose.CAD รองรับหลัก ๆ Java แต่ก็มีเวอร์ชันสำหรับ .NET, C++, และภาษาอื่น ๆ ให้เลือกใช้

**ถาม: ฉันจะหาแหล่งสนับสนุนหรือความช่วยเหลือเพิ่มเติมได้จากที่ไหน?**  
ตอบ: สำหรับคำถามหรือความช่วยเหลือใด ๆ เยี่ยมชม [ฟอรั่ม Aspose.CAD](https://forum.aspose.com/c/cad/19)

**ถาม: มีการทดลองใช้ฟรีหรือไม่?**  
ตอบ: มี, คุณสามารถสำรวจ Aspose.CAD โดยรับการทดลองใช้ฟรีจาก [ที่นี่](https://releases.aspose.com/)

**ถาม: ฉันจะขอรับไลเซนส์ชั่วคราวสำหรับ Aspose.CAD ได้อย่างไร?**  
ตอบ: รับไลเซนส์ชั่วคราวได้จาก [ลิงก์นี้](https://purchase.aspose.com/temporary-license/)

**ถาม: มีข้อกำหนดระบบเฉพาะสำหรับ Aspose.CAD for Java หรือไม่?**  
ตอบ: ตรวจสอบให้แน่ใจว่าคุณมีสภาพแวดล้อมการพัฒนา Java ที่เข้ากันได้; ดูเอกสารสำหรับรายละเอียดข้อกำหนด

---

**อัปเดตล่าสุด:** 2026-04-13  
**ทดสอบกับ:** Aspose.CAD for Java 24.12 (ล่าสุด ณ เวลาที่เขียน)  
**ผู้เขียน:** Aspose

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}