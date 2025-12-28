---
date: 2025-12-28
description: เรียนรู้วิธีสร้าง PDF จาก DWG, บันทึก DWG เป็น PDF, และเพิ่มข้อความลงในแบบร่าง
  DWG ด้วย Aspose.CAD สำหรับ Java—คู่มือแบบทีละขั้นตอน.
linktitle: Add Text in DWG
second_title: Aspose.CAD Java API
title: สร้าง PDF จาก DWG และเพิ่มข้อความโดยใช้ Aspose.CAD สำหรับ Java
url: /th/java/cad-text-and-annotation/add-text-in-dwg/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# สร้าง PDF จาก DWG และเพิ่มข้อความโดยใช้ Aspose.CAD สำหรับ Java

## บทนำ

หากคุณต้องการ **สร้าง PDF จาก DWG** พร้อมกับแทรกข้อความที่กำหนดเอง คุณมาถูกที่แล้ว ในบทเรียนนี้เราจะอธิบายขั้นตอนทั้งหมด—การโหลดภาพวาด DWG, การเพิ่มคำอธิบายข้อความ, และสุดท้ายการบันทึกผลลัพธ์เป็น PDF โดยใช้ Aspose.CAD สำหรับ Java เมื่อเสร็จคุณจะเข้าใจวิธี **บันทึก DWG เป็น PDF**, ปรับความสูงของข้อความ, และแม้กระทั่งเพิ่มคำอธิบายพื้นฐาน

## คำตอบอย่างรวดเร็ว
- **Can I convert DWG to PDF in Java?** ใช่, Aspose.CAD สำหรับ Java มี API ที่ใช้งานง่าย.  
- **Do I need a license for production use?** จำเป็นต้องมีใบอนุญาตเชิงพาณิชย์; มีการทดลองใช้ฟรี.  
- **Which method adds text to a DWG?** ใช้วัตถุ `CadText` แล้วเพิ่มลงใน model space.  
- **Can I set the text height?** แน่นอน—ใช้ `setTextHeight()` กับอินสแตนซ์ `CadText`.  
- **Is the output vector‑based?** เมื่อกำหนดตัวเลือก rasterization เป็น `UseObjectColor` PDF จะคงข้อมูลเวกเตอร์คุณภาพสูง.

## ข้อกำหนดเบื้องต้น

ก่อนเริ่มบทเรียน โปรดตรวจสอบว่าคุณมีข้อกำหนดต่อไปนี้พร้อมใช้งาน:

- Aspose.CAD for Java Library: ดาวน์โหลดและติดตั้งไลบรารีจาก [Aspose.CAD for Java page](https://releases.aspose.com/cad/java/).

- Java Development Kit (JDK): ตรวจสอบว่าคุณได้ติดตั้ง JDK เวอร์ชันล่าสุดบนระบบของคุณ.

- DWG Drawing: เตรียมไฟล์ภาพวาด DWG ที่คุณต้องการเพิ่มข้อความ.

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

ต่อไปนี้เราจะอธิบายส่วนของโค้ดที่ให้ไว้เป็นหลายขั้นตอน:

## Step 1: Set up Document Directory and DWG File Path

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String dwgPathToFile = dataDir + "SimpleEntites.dwg";
```

## Step 2: Load DWG Image

```java
Image image = Image.load(dwgPathToFile);
```

## Step 3: Create CadText Object (Add Text to DWG)

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

## Step 4: Add Text to CadImage (Insert Annotation)

```java
CadImage cadImage = ((CadImage)(image));
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(cadText);
```

## Step 5: Set Up PDF Options (Prepare to create PDF from DWG)

```java
PdfOptions pdfOptions = new PdfOptions();
```

## Step 6: Configure CadRasterizationOptions (Control PDF rendering)

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setDrawType(CadDrawTypeMode.UseObjectColor);
cadRasterizationOptions.setPageHeight(1600);
cadRasterizationOptions.setPageWidth(1600);
cadRasterizationOptions.setLayouts(new String[] {"Model"});
```

## Step 7: Save the Modified DWG as PDF (dwg to pdf java)

```java
image.save(dataDir + "SimpleEntites_generated.dwg.pdf", pdfOptions);
```

โดยทำตามขั้นตอนเหล่านี้ คุณจะสามารถ **สร้าง PDF จาก DWG**, เพิ่มข้อความที่กำหนดเอง, และควบคุมความสูงของข้อความ—ทั้งหมดด้วยเพียงไม่กี่บรรทัดของโค้ด Java.

## ทำไมต้องเพิ่มข้อความใน DWG แล้วแปลงเป็น PDF?

การเพิ่มข้อความโดยตรงในไฟล์ DWG มีประโยชน์สำหรับ:

- **Marking up designs** ด้วยโน้ตหรือหมายเลขชิ้นส่วน.
- **Creating printable documentation** ที่ PDF ทำหน้าที่เป็นรูปแบบอ่าน‑อย่างเดียวที่ได้รับการสนับสนุนอย่างกว้างขวาง.
- **Automating batch processing** ของไลบรารี CAD ขนาดใหญ่โดยไม่ต้องแก้ไขด้วยมือ.

## ปัญหาที่พบบ่อยและเคล็ดลับ

- **Text not appearing?** ตรวจสอบว่า พิกัด X/Y อยู่ภายในขอบเขตของภาพวาดและเลเยอร์มองเห็นได้.
- **Incorrect text height?** ปรับ `setTextHeight()`; ค่าจะอยู่ในระบบหน่วยของภาพวาด.
- **PDF looks rasterized?** ตรวจสอบว่าได้ตั้งค่า `CadDrawTypeMode.UseObjectColor` เพื่อรักษาข้อมูลเวกเตอร์.
- **Performance on large files?** เพิ่ม `pageHeight`/`pageWidth` เฉพาะเมื่อจำเป็น; ค่าที่ใหญ่ขึ้นจะใช้หน่วยความจำมากขึ้น.

## คำถามที่พบบ่อย

**Q: Is Aspose.CAD compatible with all versions of DWG files?**  
A: Aspose.CAD รองรับหลายเวอร์ชันของไฟล์ DWG, ทำให้เข้ากันได้กับซอฟต์แวร์ CAD หลากหลายประเภท.

**Q: Can I customize the font and formatting of the added text?**  
A: ใช่, คุณสามารถปรับแต่งฟอนต์, สไตล์, และตัวเลือกการจัดรูปแบบอื่น ๆ ของข้อความที่เพิ่มในไฟล์ DWG ด้วย Aspose.CAD.

**Q: Is there a free trial available for Aspose.CAD for Java?**  
A: ใช่, คุณสามารถสำรวจคุณสมบัติของ Aspose.CAD โดยรับการทดลองใช้ฟรีจาก [here](https://releases.aspose.com/).

**Q: Where can I find detailed documentation for Aspose.CAD for Java?**  
A: ดูเอกสาร [here](https://reference.aspose.com/cad/java/) เพื่อรับข้อมูลเชิงลึกและตัวอย่าง.

**Q: How can I get support or seek help with Aspose.CAD?**  
A: เยี่ยมชม [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) เพื่อรับความช่วยเหลือและเชื่อมต่อกับชุมชน.

---

**อัปเดตล่าสุด:** 2025-12-28  
**ทดสอบกับ:** Aspose.CAD for Java 24.12  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}