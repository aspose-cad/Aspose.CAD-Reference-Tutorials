---
date: 2025-12-25
description: เรียนรู้วิธีส่งออกไฟล์ DWG เป็น BMP ด้วย Aspose.CAD สำหรับ Java คู่มือขั้นตอนต่อขั้นตอนนี้แสดงการปรับขนาดภาพวาด
  CAD และการแปลง CAD เป็น BMP อย่างมีประสิทธิภาพ
linktitle: Adjusting CAD Drawing Size Using Unit Type
second_title: Aspose.CAD Java API
title: ส่งออก DWG เป็น BMP – ปรับขนาด CAD ด้วยประเภทหน่วย (Java)
url: /th/java/cad-file-manipulation/adjusting-cad-drawing-size-using-unit-type/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# ส่งออก DWG เป็น BMP – ปรับขนาดการวาด CAD ด้วย Unit Type ด้วย Aspose.CAD for Java

## คำนำ

เมื่อคุณต้องการ **ส่งออก DWG เป็น BMP** การควบคุมขนาดผลลัพธ์และหน่วยวัดเป็นสิ่งสำคัญสำหรับการประมวลผลต่อหรือการพิมพ์ ในบทแนะนำนี้คุณจะได้เรียนรู้วิธีปรับขนาดการวาด CAD และแปลง CAD เป็น BMP ด้วย Aspose.CAD for Java โดยใช้คุณสมบัติ `UnitType` เพื่อกำหนดหน่วยวัด ขั้นตอนต่าง ๆ จะอธิบายด้วยภาษาง่าย ๆ เพื่อให้คุณทำตามได้แม้จะเป็นมือใหม่กับไลบรารีนี้ก็ตาม

## คำตอบสั้น ๆ
- **“ส่งออก DWG เป็น BMP” หมายถึงอะไร?** การแปลงไฟล์ DWG ให้เป็นภาพราสเตอร์ BMP  
- **คุณสมบัติใดที่ควบคุมขนาดผลลัพธ์?** `CadRasterizationOptions.setUnitType()` กำหนดหน่วย (เช่น เซนติเมตร)  
- **ต้องมีลิขสิทธิ์เพื่อรันโค้ดหรือไม่?** สามารถใช้รุ่นทดลองฟรีสำหรับการประเมินผล; ต้องมีลิขสิทธิ์สำหรับการใช้งานจริง  
- **สามารถเลือกเลย์เอาต์อื่นได้หรือไม่?** ใช่, ใช้ `setLayouts()` เพื่อระบุเลย์เอาต์โมเดลหรือพีเปอร์สเปซ  
- **รูปแบบผลลัพธ์ที่รองรับมีอะไรบ้าง?** นอกจาก BMP แล้ว ยังสามารถส่งออกเป็น PNG, JPEG, TIFF ฯลฯ โดยเปลี่ยนคลาสตัวเลือก

## **ส่งออก DWG เป็น BMP** คืออะไร?

การส่งออก DWG เป็น BMP หมายถึงการเรสเตอร์ไลซ์ไฟล์ DWG ที่เป็นเวกเตอร์ให้เป็นภาพบิตแมพ (BMP) ซึ่งมีประโยชน์เมื่อคุณต้องการภาพที่แม่นยำระดับพิกเซลสำหรับระบบเก่า, กระบวนการประมวลผลภาพ, หรือการแสดงผลแบบง่าย ๆ

## ทำไมต้องปรับขนาดการวาด CAD ด้วย **Unit Type**?

การตั้งค่า Unit Type ช่วยให้คุณควบคุมมิติจริงของภาพที่ส่งออกได้โดยไม่ต้องคำนวณสเกลด้วยตนเอง สิ่งนี้ทำให้บิตแมพตรงกับการวัดในโลกจริง (เช่น เซนติเมตร) ซึ่งสำคัญสำหรับแบบแผนวิศวกรรมและเอกสารที่ต้องพิมพ์

## ข้อกำหนดเบื้องต้น

ก่อนจะเริ่มทำตามบทแนะนำนี้ โปรดตรวจสอบว่าคุณมีสิ่งต่อไปนี้พร้อมใช้งานแล้ว:

- **สภาพแวดล้อมการพัฒนา Java** – JDK ที่ทำงานได้ (เวอร์ชัน 8 ขึ้นไป) และ IDE หรือเครื่องมือสร้าง (Maven/Gradle)  
- **Aspose.CAD for Java Library** – ดาวน์โหลดและรวมไลบรารี Aspose.CAD เข้ากับโปรเจกต์ Java ของคุณ คุณสามารถรับไลบรารีได้จาก [ที่นี่](https://releases.aspose.com/cad/java/)

## นำเข้า Namespaces

ในโค้ด Java ของคุณ ให้เพิ่มการนำเข้าที่จำเป็นเพื่อใช้ฟังก์ชันของ Aspose.CAD เพิ่มบรรทัด import ดังต่อไปนี้:

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

ต่อไปเราจะอธิบายขั้นตอนการปรับขนาดการวาด CAD ด้วย Unit Type อย่างเป็นระบบ:

## ขั้นตอนที่ 1: กำหนด Data Directory

```java
String dataDir = "Your Document Directory" + "CADConversion/";
```

กำหนดพาธของโฟลเดอร์ที่เก็บไฟล์ CAD ของคุณ

## ขั้นตอนที่ 2: โหลด CAD Drawing

```java
String sourceFilePath = dataDir + "sample.dwg";
Image image = Image.load(sourceFilePath);
```

โหลดไฟล์ CAD ด้วยคลาส `Image` ของ Aspose.CAD

## ขั้นตอนที่ 3: สร้าง BMP Options

```java
BmpOptions bmpOptions = new BmpOptions();
```

สร้างอ็อบเจกต์ `BmpOptions` เพื่อส่งออกเลย์เอาต์ CAD เป็นรูปแบบ BMP

## ขั้นตอนที่ 4: ตั้งค่า Rasterization Options

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
bmpOptions.setVectorRasterizationOptions(cadRasterizationOptions);
```

สร้างอินสแตนซ์ของ `CadRasterizationOptions` และเชื่อมโยงกับ `BmpOptions` เพื่อทำการเรสเตอร์ไลซ์เวกเตอร์

## ขั้นตอนที่ 5: ตั้งค่า Unit Type

```java
cadRasterizationOptions.setUnitType(UnitType.Centimeter);
```

ระบุ Unit Type ที่ต้องการสำหรับการวาด CAD ในตัวอย่างนี้ เราได้ตั้งค่าเป็น **Centimeter** ซึ่งจะมีผลโดยตรงต่อขนาดภาพที่ส่งออกเมื่อคุณ **ปรับขนาดการวาด CAD**

## ขั้นตอนที่ 6: ตั้งค่า Layouts

```java
cadRasterizationOptions.setLayouts(new String[] { "Model" });
```

กำหนดเลย์เอาต์ที่ต้องการพิจารณาในระหว่างการส่งออก ในกรณีนี้เราเลือกเลย์เอาต์ **"Model"** แต่คุณสามารถสลับไปใช้พีเปอร์สเปซได้หากต้องการ

## ขั้นตอนที่ 7: ส่งออกเป็น BMP

```java
String outPath = sourceFilePath + ".bmp";
image.save(outPath, bmpOptions);
```

สุดท้ายให้บันทึกไฟล์ CAD ที่ปรับแก้แล้วเป็นรูปแบบ BMP ขั้นตอนนี้จะสรุปกระบวนการ **ส่งออก DWG เป็น BMP** พร้อมคงการปรับขนาดที่คุณตั้งค่าไว้

## ปัญหาที่พบบ่อยและวิธีแก้

| ปัญหา | สาเหตุ | วิธีแก้ |
|-------|--------|-----|
| **ภาพผลลัพธ์เล็กเกินไป** | ไม่ได้ตั้งค่า Unit Type หรือใช้ค่าเริ่มต้น (pixel) | เรียก `setUnitType()` พร้อมหน่วยที่ต้องการ (เช่น `UnitType.Centimeter`) |
| **ส่งออกเลย์เอาต์ผิด** | ชื่อเลย์เอาต์พิมพ์ผิด | ตรวจสอบชื่อเลย์เอาต์ด้วยโปรแกรมดู CAD; ใช้สตริงที่ตรงกันใน `setLayouts()` |
| **ข้อยกเว้นลิขสิทธิ์** | รันโดยไม่มีลิขสิทธิ์ที่ถูกต้องในสภาพการผลิต | ใส่ลิขสิทธิ์ชั่วคราวหรือถาวรตามที่อธิบายใน FAQ |

## คำถามที่พบบ่อย (ขยาย)

**ถาม: ฉันสามารถใช้ Aspose.CAD for Java กับภาษาโปรแกรมอื่นได้หรือไม่?**  
ตอบ: Aspose.CAD รองรับหลัก ๆ สำหรับ Java แต่ก็มีเวอร์ชันสำหรับภาษาอื่นเช่น .NET

**ถาม: มีตัวเลือกลิขสิทธิ์สำหรับ Aspose.CAD หรือไม่?**  
ตอบ: มี, คุณสามารถสำรวจตัวเลือกและซื้อ Aspose.CAD ได้จาก [ที่นี่](https://purchase.aspose.com/buy)

**ถาม: มีรุ่นทดลองฟรีสำหรับ Aspose.CAD หรือไม่?**  
ตอบ: แน่นอน, คุณสามารถเข้าถึงรุ่นทดลองฟรีได้จาก [ที่นี่](https://releases.aspose.com/)

**ถาม: จะขอรับการสนับสนุนสำหรับ Aspose.CAD for Java อย่างไร?**  
ตอบ: เยี่ยมชมฟอรั่ม Aspose.CAD [ที่นี่](https://forum.aspose.com/c/cad/19) เพื่อรับการสนับสนุนอย่างครบวงจร

**ถาม: สามารถขอรับลิขสิทธิ์ชั่วคราวสำหรับ Aspose.CAD ได้หรือไม่?**  
ตอบ: ได้, คุณสามารถขอรับลิขสิทธิ์ชั่วคราวได้จาก [ที่นี่](https://purchase.aspose.com/temporary-license/)

---

**อัปเดตล่าสุด:** 2025-12-25  
**ทดสอบกับ:** Aspose.CAD for Java 24.10  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}