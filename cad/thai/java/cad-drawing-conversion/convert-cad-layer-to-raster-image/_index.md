---
date: 2025-12-18
description: เรียนรู้วิธีทำบทเรียน Aspose CAD Java ที่แปลงชั้น CAD เป็นภาพราสเตอร์ได้อย่างง่ายดาย
  ปฏิบัติตามคู่มือขั้นตอนต่อขั้นตอนของเราเพื่อการแสดงผลเอกสารที่ราบรื่น
linktitle: Convert CAD Layer to Raster Image Format
second_title: Aspose.CAD Java API
title: บทแนะนำ Aspose CAD Java – แปลงเลเยอร์ CAD เป็นรูปแบบภาพแรสเตอร์
url: /th/java/cad-drawing-conversion/convert-cad-layer-to-raster-image/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose CAD Java Tutorial: แปลงชั้น CAD เป็นรูปแบบภาพเรสเตอร์

## บทนำ

ในโลกของ Computer‑Aided Design (CAD) การแปลงชั้น CAD แต่ละชั้นเป็นรูปแบบภาพเรสเตอร์เป็นสิ่งสำคัญสำหรับการแชร์ พิมพ์ หรือการประมวลผลภาพต่อไป **aspose cad java tutorial** นี้จะแสดงวิธีใช้ **Aspose.CAD for Java** เพื่อดึงชั้นเฉพาะและบันทึกเป็น JPEG (หรือรูปแบบเรสเตอร์อื่นใด) เมื่ออ่านคู่มือนี้จนจบ คุณจะเข้าใจว่าการแปลงระดับชั้นมีความสำคัญอย่างไร วิธีตั้งค่าตัวเลือกการเรสเตอร์ไลซ์ และวิธีส่งออกผลลัพธ์ด้วยเพียงไม่กี่บรรทัดของโค้ด

## คำตอบอย่างรวดเร็ว
- **บทเรียนนี้ครอบคลุมอะไร?** การแปลงชั้น CAD ที่เลือกเป็นภาพเรสเตอร์โดยใช้ Aspose.CAD for Java.  
- **รูปแบบที่รองรับคืออะไร?** รูปแบบเรสเตอร์ใดๆ ที่ Aspose รองรับ (JPEG, PNG, BMP, ฯลฯ).  
- **ต้องการใบอนุญาตหรือไม่?** รุ่นทดลองฟรีสามารถใช้ได้สำหรับการพัฒนา; จำเป็นต้องมีใบอนุญาตสำหรับการใช้งานจริง.  
- **ข้อกำหนดเบื้องต้นคืออะไร?** สภาพแวดล้อมการพัฒนา Java และไลบรารี Aspose.CAD สำหรับ Java.  
- **ใช้เวลานานเท่าไหร่ในการดำเนินการ?** ประมาณ 10–15 นาทีสำหรับการแปลงพื้นฐาน.

## ข้อกำหนดเบื้องต้น

ก่อนเริ่มเขียนโค้ด โปรดตรวจสอบว่าคุณมีสิ่งต่อไปนี้:

- **Java Development Environment** – ติดตั้งและกำหนดค่า JDK 8 หรือสูงกว่า.  
- **Aspose.CAD Library** – ดาวน์โหลดและติดตั้งไลบรารี Aspose.CAD สำหรับ Java จาก [download link](https://releases.aspose.com/cad/java/).

## นำเข้า Namespaces

ในขั้นตอนนี้ เราจะนำเข้าคลาสที่จำเป็นเพื่อเริ่มทำงานกับไฟล์ CAD.

### นำเข้าคลาส Aspose.CAD

ในไฟล์ซอร์ส Java ของคุณ ให้รวมการนำเข้า Aspose.CAD ที่จำเป็น:

```java
import com.aspose.cad.Image;


import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
import java.util.ArrayList;
import java.util.Arrays;
import java.util.List;
```

## แปลงชั้น CAD เป็นรูปแบบภาพเรสเตอร์

ด้านล่างเป็นกระบวนการแบบเต็มขั้นตอน แต่ละขั้นจะอธิบายด้วยภาษาง่ายก่อนบล็อกโค้ด เพื่อให้คุณเข้าใจว่ากำลังเกิดอะไรขึ้น

### ขั้นตอนที่ 1: ตั้งค่าไฟล์ CAD

แรกสุด ให้ระบุตำแหน่งไฟล์ CAD ของคุณและโหลดเข้าสู่วัตถุ `Image`.

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

### ขั้นตอนที่ 2: กำหนดค่าตัวเลือกการเรสเตอร์ไลซ์

สร้างอินสแตนซ์ `CadRasterizationOptions` เพื่อกำหนดขนาดและคุณภาพของภาพผลลัพธ์.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(500);
rasterizationOptions.setPageHeight(500);
```

### ขั้นตอนที่ 3: ระบุชั้น CAD

เพิ่มชื่อชั้นที่คุณต้องการเรสเตอร์ไลซ์ ในตัวอย่างนี้เราจะส่งออกชั้นเริ่มต้น `"0"`.

```java
List<String> stringList = new ArrayList<>(Arrays.asList("0"));
rasterizationOptions.setLayers(stringList);
```

### ขั้นตอนที่ 4: ตั้งค่า JPEG Options

สร้างอ็อบเจ็กต์ `JpegOptions` (หรืออ็อบเจ็กต์ตัวเลือกภาพเรสเตอร์อื่น) แล้วเชื่อมโยงกับการตั้งค่าการเรสเตอร์ไลซ์.

```java
JpegOptions options = new JpegOptions();
options.setVectorRasterizationOptions(rasterizationOptions);
```

### ขั้นตอนที่ 5: ส่งออกเป็น JPEG

สุดท้าย ให้บันทึกชั้นที่เรสเตอร์ไลซ์เป็นไฟล์ JPEG.

```java
image.save(dataDir + "CADLayersToRasterImageFormats_out_.jpg", options);
```

ทำซ้ำขั้นตอนข้างต้นสำหรับชั้นเพิ่มเติมหรือปรับพารามิเตอร์การเรสเตอร์ไลซ์ (ความละเอียด, สีพื้นหลัง ฯลฯ) เพื่อให้ตรงกับความต้องการของคุณ.

## ทำไมต้องใช้วิธีนี้?

- **Selective Export** – เฉพาะชั้นที่คุณต้องการเท่านั้นที่ถูกเรนเดอร์ ลดขนาดไฟล์และเวลาในการประมวลผล.  
- **Format Flexibility** – เปลี่ยน `JpegOptions` เป็น `PngOptions`, `BmpOptions`, ฯลฯ โดยไม่ต้องแก้ไขตรรกะหลัก.  
- **High‑Quality Rendering** – Aspose.CAD รักษาความหนาของเส้น สี และข้อความให้เหมือนกับไฟล์ CAD ดั้งเดิม.

## ปัญหาที่พบบ่อยและการแก้ไข

| อาการ | สาเหตุที่เป็นไปได้ | วิธีแก้ |
|---------|--------------|-----|
| ผลลัพธ์เป็นภาพสีขาว | ไม่ได้ระบุชั้นหรือระบุชื่อชั้นผิด | ตรวจสอบว่าชื่อชั้นมีอยู่ในไฟล์ CAD; ใช้ `image.getLayers()` เพื่อแสดงรายการ. |
| ความละเอียดต่ำ | DPI เริ่มต้นต่ำ | ตั้งค่า `rasterizationOptions.setResolution(300);` (หรือสูงกว่า) ก่อนบันทึก. |
| ไม่รองรับรูปแบบ CAD | ใช้เวอร์ชัน Aspose.CAD เก่า | อัปเดตเป็นเวอร์ชันล่าสุดของ Aspose.CAD for Java. |

## คำถามที่พบบ่อย

**Q: ฉันสามารถใช้ Aspose.CAD for Java กับภาษาโปรแกรมอื่นได้หรือไม่?**  
**A:** Aspose.CAD รองรับ Java เป็นหลัก แต่มีเวอร์ชันสำหรับ .NET, C++, และภาษาอื่นๆ ให้เลือกใช้.

**Q: ฉันสามารถหาแหล่งสนับสนุนหรือความช่วยเหลือเพิ่มเติมได้จากที่ไหน?**  
**A:** สำหรับคำถามหรือความช่วยเหลือใดๆ ให้เยี่ยมชม [Aspose.CAD forum](https://forum.aspose.com/c/cad/19).

**Q: มีรุ่นทดลองฟรีหรือไม่?**  
**A:** มี คุณสามารถสำรวจ Aspose.CAD ได้โดยรับรุ่นทดลองฟรีจาก [here](https://releases.aspose.com/).

**Q: ฉันจะขอรับใบอนุญาตชั่วคราวสำหรับ Aspose.CAD ได้อย่างไร?**  
**A:** รับใบอนุญาตชั่วคราวได้จาก [this link](https://purchase.aspose.com/temporary-license/).

**Q: มีข้อกำหนดระบบเฉพาะสำหรับ Aspose.CAD for Java หรือไม่?**  
**A:** ตรวจสอบว่าคุณมีสภาพแวดล้อมการพัฒนา Java ที่เข้ากันได้; ดูเอกสารสำหรับรายละเอียดข้อกำหนด.

---

**อัปเดตล่าสุด:** 2025-12-18  
**ทดสอบกับ:** Aspose.CAD for Java 24.12 (latest at time of writing)  
**ผู้เขียน:** Aspose

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
