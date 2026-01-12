---
date: 2026-01-12
description: เรียนรู้วิธีเพิ่มรูปภาพลงในไฟล์ DWG ด้วย Aspose.CAD สำหรับ Java และแปลง
  DWG เป็น PDF ตามขั้นตอนของเราเพื่อการพัฒนาที่มีประสิทธิภาพ
linktitle: Import Image to DWG File Using Java
second_title: Aspose.CAD Java API
title: เพิ่มรูปภาพลงในไฟล์ DWG อย่างง่ายดายด้วย Aspose.CAD Java
url: /th/java/dwg-file-operations/import-image-to-dwg/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# เพิ่มรูปภาพลงในไฟล์ DWG อย่างง่ายดายด้วย Aspose.CAD Java

ในแอปพลิเคชัน Java สมัยใหม่ **การเพิ่มรูปภาพลงใน DWG** เป็นความต้องการที่พบบ่อย—ไม่ว่าจะเป็นการสร้างตัวดู CAD, การทำงานอัตโนมัติในการอัปเดตแบบร่าง, หรือการสร้างเอกสารประกอบ Aspose.CAD for Java ให้วิธีที่ตรงไปตรงมาและมีประสิทธิภาพสูงในการฝังรูปภาพ raster ลงในภาพวาด DWG โดยไม่ต้องใช้เครื่องมือ CAD เต็มรูปแบบ ในบทแนะนำนี้เราจะพาคุณผ่านกระบวนการทั้งหมด ตั้งแต่การโหลด DWG จนถึงการส่งออกผลลัพธ์เป็น PDF

## คำตอบสั้น ๆ
- **ต้องใช้ไลบรารีอะไร?** Aspose.CAD for Java  
- **สามารถส่งออกเป็น PDF ได้หรือไม่?** ได้ – ใช้ `PdfOptions` ร่วมกับ `CadRasterizationOptions`  
- **ต้องมีไลเซนส์สำหรับการพัฒนาหรือไม่?** ทดลองใช้ฟรีได้สำหรับการทดสอบ; ต้องมีไลเซนส์เชิงพาณิชย์สำหรับการใช้งานจริง  
- **รองรับเวอร์ชัน Java ไหน?** Java 8 ขึ้นไป  
- **ใช้เวลานำไปใช้งานเท่าไหร่?** ประมาณ 10‑15 นาทีสำหรับการนำเข้ารูปภาพพื้นฐาน

## “add image to dwg” คืออะไร?
การเพิ่มรูปภาพลงในไฟล์ DWG หมายถึงการแทรกรูปภาพ raster (PNG, JPEG ฯลฯ) เป็นอ็อบเจ็กต์ `CadRasterImage` ภายใน model space ของแบบร่าง รูปภาพจะกลายเป็นส่วนหนึ่งของโครงสร้าง CAD และสามารถกำหนดตำแหน่ง, ปรับขนาด, และคลิปได้เช่นเดียวกับอ็อบเจ็กต์ CAD อื่น ๆ

## ทำไมต้องใช้ Aspose.CAD for Java เพื่อเพิ่มรูปภาพลงใน dwg?
- **ไม่ต้องใช้ซอฟต์แวร์ CAD** – API จัดการการพาร์ส DWG ภายในเอง  
- **ควบคุมได้ละเอียด** เกี่ยวกับจุดแทรก, เวกเตอร์สเกล, และการคลิป  
- **มีฟังก์ชันแปลงเป็น PDF** ในตัว ทำให้สามารถสร้าง PDF ที่พิมพ์ได้ในขั้นตอนเดียวกัน  
- **ข้ามแพลตฟอร์ม** – ทำงานบน Windows, Linux, และ macOS

## ข้อกำหนดเบื้องต้น
- Aspose.CAD for Java: ตรวจสอบว่าคุณได้ติดตั้งไลบรารี Aspose.CAD แล้ว คุณสามารถดาวน์โหลดได้จาก [ที่นี่](https://releases.aspose.com/cad/java/)  
- สภาพแวดล้อมการพัฒนา Java: JDK 8+ พร้อม IDE ที่คุณชื่นชอบ (IntelliJ, Eclipse, VS Code ฯลฯ)

## นำเข้าแพ็คเกจ
```java
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.cad.CadDrawTypeMode;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.*;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## คู่มือขั้นตอนโดยละเอียด

### ขั้นตอนที่ 1: โหลดไฟล์ DWG
แรกสุด ให้ระบุตำแหน่งโฟลเดอร์ที่มีไฟล์ DWG ของคุณและโหลดด้วย `Image.load`
```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String srcFile = dataDir + "Drawing11.dwg";
Image image = Image.load(srcFile);
```

### ขั้นตอนที่ 2: กำหนด Raster Image Definition
สร้าง `CadRasterImageDef` ที่อ้างอิงไฟล์ PNG ภายนอกที่คุณต้องการฝัง ตัวสร้างรับชื่อไฟล์ภาพและขนาดพิกเซลของมัน
```java
CadRasterImageDef cadRasterImageDef = new CadRasterImageDef("road-sign-custom.png", 640, 562);
cadRasterImageDef.setObjectHandle("A3B4");
```

### ขั้นตอนที่ 3: ตั้งค่าจุดแทรกและเวกเตอร์สเกล
จุดแทรกกำหนดตำแหน่งมุมล่างซ้ายของรูปภาพ **U** และ **V** เวกเตอร์ควบคุมการสเกลแนวนอนและแนวตั้ง
```java
Cad3DPoint insertionPoint = new Cad3DPoint(26.77, 22.35);
Cad3DPoint uVector = new Cad3DPoint(0.0061565450840500831, 0);
Cad3DPoint vVector = new Cad3DPoint(0, 0.0061565450840500822);
```

### ขั้นตอนที่ 4: สร้างอ็อบเจ็กต์ CadRasterImage
รวม definition, จุดแทรก, และเวกเตอร์เข้าด้วยกันเป็น `CadRasterImage` คุณยังสามารถกำหนดขอบเขตการคลิปได้หากต้องการให้เห็นเฉพาะส่วนของรูปภาพ
```java
CadRasterImage cadRasterImage = new CadRasterImage(cadRasterImageDef, insertionPoint, uVector, vVector);
cadRasterImage.setImageDefReference("A3B4");
cadRasterImage.setDisplayFlags((short)7);
cadRasterImage.setClippingState((short)0);
cadRasterImage.getClipBoundaryVertexList().add(new Cad2DPoint(-0.5, 0.5));
cadRasterImage.getClipBoundaryVertexList().add(new Cad2DPoint(639.5, 561.5));
```

### ขั้นตอนที่ 5: เพิ่มรูปภาพลงใน Model Space
แทรกรูป raster ลงในบล็อก `*Model_Space` แล้วอัปเดตคอลเลกชันอ็อบเจ็กต์ของแบบร่างเพื่อให้ definition ถูกบันทึก
```java
CadImage cadImage = ((CadImage)(image));
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(cadRasterImage);
CadBaseObject[] objs = cadImage.getObjects();
CadBaseObject[] arr = new CadBaseObject[objs.length + 1];
int ind = 0;
for (CadBaseObject obj : objs)
{
    arr[ind] = obj;
    ind++;
}
arr[ind] = cadRasterImageDef;
cadImage.setObjects(arr);
```

### ขั้นตอนที่ 6: ตั้งค่าตัวเลือกการส่งออก PDF (ไม่บังคับ)
หากต้องการไฟล์ PDF ของแบบร่างด้วย ให้กำหนด `PdfOptions` ร่วมกับ `CadRasterizationOptions` ขั้นตอนนี้แสดงวิธี **convert dwg to pdf** ในกระบวนการเดียวกัน
```java
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setDrawType(CadDrawTypeMode.UseObjectColor);
cadRasterizationOptions.setPageHeight(1600);
cadRasterizationOptions.setPageWidth(1600);
cadRasterizationOptions.setLayouts(new String[] {"Model"});
```

### ขั้นตอนที่ 7: บันทึก PDF ที่ได้
สุดท้าย ส่งออกแบบร่างที่แก้ไขเป็นไฟล์ PDF โดยใช้อินสแตนซ์ `image` เดียวกัน ดังนั้น PDF จะสะท้อนรูป raster ที่เพิ่มใหม่
```java
image.save((srcFile + "_generated.pdf"), pdfOptions);
```

โดยทำตามขั้นตอนเหล่านี้ คุณสามารถ **add image to dwg** ได้อย่างรวดเร็วและยัง **save dwg as pdf** หากต้องการ

## ปัญหาที่พบบ่อยและวิธีแก้
- **รูปภาพไม่แสดง** – ตรวจสอบว่าเส้นทางไฟล์รูป (`road-sign-custom.png`) ถูกต้องและขนาดภาพตรงกับค่าที่ส่งให้ `CadRasterImageDef`  
- **สเกลไม่ถูกต้อง** – ปรับค่า U และ V เวกเตอร์; ค่าดังกล่าวแสดงหน่วย drawing ต่อพิกเซล  
- **PDF แสดงเป็นสีขาว** – ตรวจสอบให้ `CadRasterizationOptions.setDrawType` ตั้งเป็น `UseObjectColor` หรือโหมดที่เหมาะสมอื่น ๆ

## คำถามที่พบบ่อย

**Q: Aspose.CAD for Java รองรับสภาพแวดล้อมการพัฒนา Java ทุกประเภทหรือไม่?**  
A: ใช่, Aspose.CAD for Java รองรับสภาพแวดล้อมการพัฒนา Java ส่วนใหญ่

**Q: สามารถใช้ Aspose.CAD for Java ในโครงการเชิงพาณิชย์ได้หรือไม่?**  
A: ใช่, คุณสามารถใช้ Aspose.CAD for Java ในโครงการเชิงพาณิชย์ได้ ดูรายละเอียดไลเซนส์ได้ที่ [ที่นี่](https://purchase.aspose.com/buy)

**Q: มีรุ่นทดลองฟรีสำหรับ Aspose.CAD for Java หรือไม่?**  
A: มี, คุณสามารถเข้าถึงรุ่นทดลองได้ [ที่นี่](https://releases.aspose.com/)

**Q: จะขอรับการสนับสนุนสำหรับ Aspose.CAD for Java ได้อย่างไร?**  
A: คุณสามารถขอรับการสนับสนุนได้จาก [ฟอรั่ม Aspose.CAD](https://forum.aspose.com/c/cad/19)

**Q: สามารถขอรับไลเซนส์ชั่วคราวสำหรับ Aspose.CAD for Java ได้หรือไม่?**  
A: ได้, คุณสามารถรับไลเซนส์ชั่วคราวได้ [ที่นี่](https://purchase.aspose.com/temporary-license/)

---

**อัปเดตล่าสุด:** 2026-01-12  
**ทดสอบกับ:** Aspose.CAD for Java 24.11  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}