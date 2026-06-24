---
date: 2026-02-28
description: เรียนรู้วิธีสร้าง PDF จาก DWG, บันทึก DWG เป็น PDF, และเพิ่มข้อความลงในแบบร่าง
  DWG ด้วย Aspose.CAD สำหรับ Java—คู่มือขั้นตอนโดยละเอียด.
linktitle: Add Text in DWG
second_title: Aspose.CAD Java API
title: สร้าง PDF จาก DWG และเพิ่มข้อความโดยใช้ Aspose.CAD สำหรับ Java
url: /th/java/cad-text-and-annotation/add-text-in-dwg/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# สร้าง PDF จาก DWG และเพิ่มข้อความด้วย Aspose.CAD for Java

## บทนำ

หากคุณต้อง **สร้าง PDF จาก DWG** พร้อมกับแทรกข้อความที่กำหนดเอง คุณมาถูกที่แล้ว ในบทแนะนำนี้เราจะเดินผ่านกระบวนการทั้งหมด—การโหลดไฟล์ DWG, การเพิ่มคำอธิบายข้อความ, และสุดท้ายการบันทึกผลลัพธ์เป็น PDF ด้วย Aspose.CAD for Java เมื่อเสร็จสิ้นคุณจะเข้าใจวิธี **บันทึก DWG เป็น PDF**, ปรับความสูงของข้อความ, และแม้กระทั่งเพิ่มคำอธิบายพื้นฐาน

## คำตอบอย่างรวดเร็ว
- **ฉันสามารถแปลง DWG เป็น PDF ใน Java ได้หรือไม่?** ได้, Aspose.CAD for Java มี API ที่ใช้งานง่าย  
- **ต้องใช้ไลเซนส์สำหรับการใช้งานในผลิตภัณฑ์จริงหรือไม่?** จำเป็นต้องมีไลเซนส์เชิงพาณิชย์; มีรุ่นทดลองฟรีให้ใช้  
- **วิธีใดที่ใช้เพิ่มข้อความลงใน DWG?** ใช้วัตถุ `CadText` แล้วเพิ่มลงใน model space  
- **ฉันสามารถตั้งค่าความสูงของข้อความได้หรือไม่?** แน่นอน—ใช้ `setTextHeight()` กับอินสแตนซ์ `CadText`  
- **ผลลัพธ์เป็นแบบเวกเตอร์หรือไม่?** เมื่อกำหนดตัวเลือกการเรสเตอร์ไลซ์เป็น `UseObjectColor` PDF จะคงข้อมูลเวกเตอร์คุณภาพสูงไว้

## “สร้าง PDF จาก DWG” คืออะไร?
การสร้าง PDF จากไฟล์ DWG หมายถึงการแปลงรูปแบบ CAD ดั้งเดิมให้เป็นเอกสารที่อ่านได้อย่างกว้างขวางและเป็นแบบอ่าน‑อย่างเดียว โดยยังคงรักษาเรขาคณิตเดิมไว้ การแปลงนี้สำคัญเมื่อคุณต้องการแชร์แบบออกแบบกับผู้มีส่วนได้ส่วนเสียที่ไม่มีซอฟต์แวร์ CAD

## ทำไมต้องใช้ Aspose.CAD for Java เพื่อแปลง DWG เป็น PDF?
Aspose.CAD ให้โซลูชันแบบ pure‑Java ที่ไม่ต้องติดตั้ง CAD ภายนอก รองรับ **convert DWG to PDF**, รักษาความแม่นยำของเวกเตอร์, และให้คุณเพิ่มคำอธิบายเช่นข้อความ, มิติ, หรือกราฟิกที่กำหนดเองก่อนการแปลงได้โดยอัตโนมัติ

## ข้อกำหนดเบื้องต้น

ก่อนเริ่มทำตามบทแนะนำนี้ ให้ตรวจสอบว่าคุณมีสิ่งต่อไปนี้พร้อมใช้งานแล้ว:

- ไลบรารี Aspose.CAD for Java: ดาวน์โหลดและติดตั้งจากหน้า [Aspose.CAD for Java page](https://releases.aspose.com/cad/java/)  
- Java Development Kit (JDK): ตรวจสอบว่ามี JDK เวอร์ชันล่าสุดติดตั้งอยู่ในระบบของคุณ  
- ไฟล์ DWG: เตรียมไฟล์ DWG ที่ต้องการเพิ่มข้อความลงไป

## นำเข้า Namespaces

ในโค้ด Java ของคุณ ให้นำเข้า namespaces ที่จำเป็นสำหรับ Aspose.CAD:

```java
import com.aspose.cad.Image;


import com.aspose.cad.fileformats.cad.CadDrawTypeMode;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.CadText;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

ต่อไปเราจะวิเคราะห์ส่วนของโค้ดที่ให้ไว้เป็นหลายขั้นตอน:

## ขั้นตอนที่ 1: ตั้งค่าไดเรกทอรีเอกสารและเส้นทางไฟล์ DWG

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String dwgPathToFile = dataDir + "SimpleEntites.dwg";
```

## ขั้นตอนที่ 2: โหลดภาพ DWG

```java
Image image = Image.load(dwgPathToFile);
```

## ขั้นตอนที่ 3: สร้างวัตถุ CadText (เพิ่มข้อความลงใน DWG)

```java
CadText cadText = new CadText();
cadText.setStyleType("Standard");
cadText.setDefaultValue("Some custom text");
cadText.setColorId(256);
cadText.setLayerName("0");
cadText.getFirstAlignment().setX(47.9);
cadText.getFirstAlignment().setY(5.56);
cadText.setTextHeight(0.8);          // set text height in DWG units
cadText.setScaleX(0);
```

## ขั้นตอนที่ 4: เพิ่มข้อความลงใน CadImage (แทรกคำอธิบาย)

```java
CadImage cadImage = ((CadImage)(image));
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(cadText);
```

## ขั้นตอนที่ 5: ตั้งค่า PDF Options (เตรียมสร้าง PDF จาก DWG)

```java
PdfOptions pdfOptions = new PdfOptions();
```

## ขั้นตอนที่ 6: กำหนดค่า CadRasterizationOptions (ควบคุมการเรนเดอร์ PDF)

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setDrawType(CadDrawTypeMode.UseObjectColor);
cadRasterizationOptions.setPageHeight(1600);
cadRasterizationOptions.setPageWidth(1600);
cadRasterizationOptions.setLayouts(new String[] {"Model"});
```

## ขั้นตอนที่ 7: บันทึก DWG ที่แก้ไขเป็น PDF (dwg to pdf java)

```java
image.save(dataDir + "SimpleEntites_generated.dwg.pdf", pdfOptions);
```

โดยทำตามขั้นตอนเหล่านี้ คุณจะสามารถ **สร้าง PDF จาก DWG**, เพิ่มข้อความที่กำหนดเอง, และควบคุมความสูงของข้อความ—ทั้งหมดด้วยเพียงไม่กี่บรรทัดของโค้ด Java

## วิธีแปลง DWG เป็น PDF ใน Java อย่างเป็นชุด?
หากต้อง **แปลง DWG PDF** เป็นชุด ให้ใส่โค้ดข้างต้นไว้ในลูปที่วนผ่านโฟลเดอร์ของไฟล์ DWG ปรับ `pageHeight`/`pageWidth` เฉพาะเมื่อจำเป็นเพื่อรักษาการใช้หน่วยความจำให้ต่ำ, และใช้อินสแตนซ์ `PdfOptions` เดียวกันสำหรับแต่ละไฟล์เพื่อเพิ่มประสิทธิภาพ

## ปัญหาที่พบบ่อยและเคล็ดลับ

- **ข้อความไม่ปรากฏ?** ตรวจสอบว่า พิกัด X/Y อยู่ในขอบเขตของแบบและเลเยอร์มองเห็นได้  
- **ความสูงของข้อความไม่ถูกต้อง?** ปรับ `setTextHeight()`; ค่าจะอยู่ในระบบหน่วยของแบบ  
- **PDF ดูเหมือนถูกเรสเตอร์ไลซ์?** ตรวจสอบให้ `CadDrawTypeMode.UseObjectColor` ถูกตั้งค่าเพื่อคงข้อมูลเวกเตอร์ไว้  
- **ประสิทธิภาพเมื่อไฟล์ใหญ่?** เพิ่ม `pageHeight`/`pageWidth` เฉพาะเมื่อจำเป็น; ค่าที่ใหญ่กว่าจะใช้หน่วยความจำมากขึ้น

## คำถามที่พบบ่อย

**Q: Aspose.CAD รองรับไฟล์ DWG ทุกเวอร์ชันหรือไม่?**  
A: Aspose.CAD รองรับหลายเวอร์ชันของไฟล์ DWG, ทำให้เข้ากันได้กับซอฟต์แวร์ CAD หลากหลายประเภท  

**Q: ฉันสามารถปรับแต่งฟอนต์และรูปแบบของข้อความที่เพิ่มได้หรือไม่?**  
A: ได้, คุณสามารถปรับแต่งฟอนต์, สไตล์, และตัวเลือกการจัดรูปแบบอื่น ๆ สำหรับข้อความที่เพิ่มลงในไฟล์ DWG ด้วย Aspose.CAD  

**Q: มีรุ่นทดลองฟรีสำหรับ Aspose.CAD for Java หรือไม่?**  
A: มี, คุณสามารถสำรวจคุณสมบัติของ Aspose.CAD ได้โดยรับรุ่นทดลองฟรีจาก [here](https://releases.aspose.com/)  

**Q: จะหาเอกสารรายละเอียดของ Aspose.CAD for Java ได้จากที่ไหน?**  
A: ดูเอกสารได้ที่ [here](https://reference.aspose.com/cad/java/) เพื่อข้อมูลเชิงลึกและตัวอย่างเพิ่มเติม  

**Q: จะขอรับการสนับสนุนหรือขอความช่วยเหลือเกี่ยวกับ Aspose.CAD ได้อย่างไร?**  
A: เยี่ยมชม [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) เพื่อรับความช่วยเหลือและเชื่อมต่อกับชุมชน

---

**อัปเดตล่าสุด:** 2026-02-28  
**ทดสอบด้วย:** Aspose.CAD for Java 24.12  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}