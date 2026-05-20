---
date: 2026-05-20
description: เรียนรู้วิธีเพิ่มรูปภาพลงในไฟล์ DWG ด้วย Aspose.CAD for Java และแปลง
  DWG เป็น PDF อีกด้วย. ปฏิบัติตามคู่มือขั้นตอนอย่างละเอียดของเราเพื่อการพัฒนาที่มีประสิทธิภาพ.
keywords:
- add image to dwg
- convert dwg to pdf
- import image into dwg
- embed raster image dwg
- dwg file operations
linktitle: นำเข้ารูปภาพไปยังไฟล์ DWG ด้วย Java
schemas:
- author: Aspose
  dateModified: '2026-05-20'
  description: Learn how to add image to DWG files using Aspose.CAD for Java and also
    convert DWG to PDF. Follow our step-by-step guide for efficient development.
  headline: Add Image to DWG Files Effortlessly Using Aspose.CAD Java
  type: TechArticle
- description: Learn how to add image to DWG files using Aspose.CAD for Java and also
    convert DWG to PDF. Follow our step-by-step guide for efficient development.
  name: Add Image to DWG Files Effortlessly Using Aspose.CAD Java
  steps:
  - name: Load the DWG File
    text: First, point to the folder that contains your DWG drawing and load it with
      `Image.load`.
  - name: Define the Raster Image Definition
    text: The `CadRasterImageDef` class defines the external raster image resource
      to be embedded in the drawing.
  - name: Set Insertion Point and Scaling Vectors
    text: The insertion point determines where the lower‑left corner of the image
      will appear. The **U** and **V** vectors control horizontal and vertical scaling.
  - name: Create the CadRasterImage Object
    text: The `CadRasterImage` entity represents a raster picture placed in the DWG
      model space.
  - name: Add the Image to Model Space
    text: Insert the raster image into the `*Model_Space` block, then update the drawing’s
      object collection so the definition is saved.
  - name: Configure PDF Export Options (Optional)
    text: '`PdfOptions` specifies settings for saving a CAD drawing as a PDF file.
      `CadRasterizationOptions` defines how the CAD content is rasterized during PDF
      conversion.'
  - name: Save the Resulting PDF
    text: 'Finally, export the modified drawing as a PDF file. The same `image` instance
      is used, so the PDF reflects the newly added raster image. By following these
      steps, you can **add image to dwg** files quickly and also **save dwg as pdf**
      when needed, covering the most common **dwg file operations** in '
  type: HowTo
- questions:
  - answer: Yes, Aspose.CAD for Java works with any IDE that supports JDK 8+, including
      IntelliJ IDEA, Eclipse, and VS Code.
    question: Is Aspose.CAD for Java compatible with all Java development environments?
  - answer: Yes, you can use Aspose.CAD for Java for commercial projects. Visit **[here](https://purchase.aspose.com/buy)**
      for licensing details.
    question: Can I use Aspose.CAD for Java for commercial projects?
  - answer: Yes, you can access the free trial **[here](https://releases.aspose.com/)**.
    question: Is there a free trial available for Aspose.CAD for Java?
  - answer: You can seek support on the **[Aspose.CAD forum](https://forum.aspose.com/c/cad/19)**.
    question: How can I get support for Aspose.CAD for Java?
  - answer: Yes, you can get a temporary license **[here](https://purchase.aspose.com/temporary-license/)**.
    question: Can I obtain a temporary license for Aspose.CAD for Java?
  type: FAQPage
second_title: Aspose.CAD Java API
title: เพิ่มรูปภาพลงในไฟล์ DWG อย่างง่ายดายด้วย Aspose.CAD Java
url: /th/java/dwg-file-operations/import-image-to-dwg/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# เพิ่มรูปภาพลงในไฟล์ DWG อย่างง่ายดายด้วย Aspose.CAD Java

ในแอปพลิเคชัน Java สมัยใหม่, **adding an image to DWG** เป็นความต้องการทั่วไป—ไม่ว่าคุณจะกำลังสร้าง CAD viewer, ทำการอัปเดตแบบอัตโนมัติ, หรือสร้างเอกสาร. Aspose.CAD for Java ให้วิธีที่ตรงไปตรงมาและมีประสิทธิภาพสูงในการฝังรูปภาพ raster ลงในภาพวาด DWG โดยไม่ต้องใช้เครื่องมือ CAD เต็มรูปแบบ. ในบทแนะนำนี้เราจะพาคุณผ่านกระบวนการทั้งหมด, ตั้งแต่การโหลด DWG ไปจนถึงการส่งออกผลลัพธ์เป็น PDF, และเราจะอธิบายวิธี **import image into dwg** และ **convert dwg to pdf** ในขั้นตอนเดียว.

## คำตอบอย่างรวดเร็ว
- **ต้องใช้ไลบรารีอะไร?** Aspose.CAD for Java  
- **ฉันสามารถส่งออกเป็น PDF ได้ไหม?** Yes – use `PdfOptions` with `CadRasterizationOptions`  
- **ฉันต้องการไลเซนส์สำหรับการพัฒนาหรือไม่?** A free trial works for testing; a commercial license is required for production  
- **เวอร์ชัน Java ที่รองรับคืออะไร?** Java 8 and higher  
- **การดำเนินการใช้เวลานานเท่าไหร่?** About 10‑15 minutes for a basic image import  

## “add image to dwg” คืออะไร?
การเพิ่มรูปภาพลงในไฟล์ DWG หมายถึงการฝังภาพ raster (PNG, JPEG ฯลฯ) เป็นเอนทิตี้ **CadRasterImage** ภายใน model space ของภาพวาด, ซึ่งสามารถกำหนดตำแหน่ง, ปรับขนาด, และตัดคลิปได้เช่นเดียวกับวัตถุ CAD อื่น ๆ. มันจะถูกเก็บในตารางอ็อบเจ็กต์ของภาพวาดและแสดงผลโดยโปรแกรมดู CAD มาตรฐาน.

## ทำไมต้องใช้ Aspose.CAD for Java เพื่อเพิ่มรูปภาพลงใน dwg?
คุณสามารถฝังกราฟิก raster ลงในไฟล์ DWG ได้โดยไม่ต้องติดตั้งซอฟต์แวร์ CAD ของบุคคลที่สาม, และ API ให้การควบคุมระดับพิกเซลที่แม่นยำสำหรับจุดแทรก, เวกเตอร์สเกล, และขอบเขตการคลิป. Aspose.CAD รองรับไฟล์ขนาดถึง 2 GB, มี **50+ input and output formats**, และทำงานบน Windows, Linux, และ macOS, ทำให้คุณสามารถรวมการจัดการ CAD เข้าใน backend ที่ใช้ Java ได้ทุกประเภท.

## ข้อกำหนดเบื้องต้น
- **Aspose.CAD for Java** – ดาวน์โหลด JAR ล่าสุดจากเว็บไซต์อย่างเป็นทางการ **[here](https://releases.aspose.com/cad/java/)**.  
- **Java Development Kit** – JDK 8 หรือใหม่กว่า พร้อม IDE ที่คุณชื่นชอบ (IntelliJ IDEA, Eclipse, VS Code ฯลฯ).  
- ใบอนุญาต **Aspose.CAD** ที่ถูกต้องสำหรับการใช้งานในผลิตภัณฑ์ (รุ่นทดลองใช้ได้สำหรับการทดลอง).  

## นำเข้าแพ็กเกจ
การนำเข้าต่อไปนี้จะนำคลาส Aspose.CAD ที่จำเป็นสำหรับการจัดการรูปภาพและการแปลงเป็น PDF มาใช้.  
```java
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.cad.CadDrawTypeMode;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.*;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## คู่มือขั้นตอนต่อขั้นตอน

### ขั้นตอนที่ 1: โหลดไฟล์ DWG
ก่อนอื่น, ระบุตำแหน่งโฟลเดอร์ที่มีภาพวาด DWG ของคุณและโหลดด้วย `Image.load`.  
```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String srcFile = dataDir + "Drawing11.dwg";
Image image = Image.load(srcFile);
```

### ขั้นตอนที่ 2: กำหนด Raster Image Definition
คลาส `CadRasterImageDef` กำหนดทรัพยากรภาพ raster ภายนอกที่จะฝังในภาพวาด.  
```java
CadRasterImageDef cadRasterImageDef = new CadRasterImageDef("road-sign-custom.png", 640, 562);
cadRasterImageDef.setObjectHandle("A3B4");
```

### ขั้นตอนที่ 3: ตั้งค่าจุดแทรกและเวกเตอร์สเกล
จุดแทรกกำหนดตำแหน่งมุมล่างซ้ายของภาพที่จะปรากฏ. เวกเตอร์ **U** และ **V** ควบคุมการสเกลในแนวนอนและแนวตั้ง.  
```java
Cad3DPoint insertionPoint = new Cad3DPoint(26.77, 22.35);
Cad3DPoint uVector = new Cad3DPoint(0.0061565450840500831, 0);
Cad3DPoint vVector = new Cad3DPoint(0, 0.0061565450840500822);
```

### ขั้นตอนที่ 4: สร้างอ็อบเจ็กต์ CadRasterImage
เอนทิตี้ `CadRasterImage` แสดงภาพ raster ที่วางใน model space ของ DWG.  
```java
CadRasterImage cadRasterImage = new CadRasterImage(cadRasterImageDef, insertionPoint, uVector, vVector);
cadRasterImage.setImageDefReference("A3B4");
cadRasterImage.setDisplayFlags((short)7);
cadRasterImage.setClippingState((short)0);
cadRasterImage.getClipBoundaryVertexList().add(new Cad2DPoint(-0.5, 0.5));
cadRasterImage.getClipBoundaryVertexList().add(new Cad2DPoint(639.5, 561.5));
```

### ขั้นตอนที่ 5: เพิ่มรูปภาพลงใน Model Space
แทรกรูป raster ลงในบล็อก `*Model_Space`, จากนั้นอัปเดตคอลเลกชันอ็อบเจ็กต์ของภาพวาดเพื่อให้การกำหนดค่าถูกบันทึก.  
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

### ขั้นตอนที่ 6: กำหนดค่าตัวเลือกการส่งออก PDF (ไม่บังคับ)
`PdfOptions` ระบุการตั้งค่าสำหรับการบันทึกภาพวาด CAD เป็นไฟล์ PDF. `CadRasterizationOptions` กำหนดวิธีการ rasterize เนื้อหา CAD ระหว่างการแปลงเป็น PDF.  
```java
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setDrawType(CadDrawTypeMode.UseObjectColor);
cadRasterizationOptions.setPageHeight(1600);
cadRasterizationOptions.setPageWidth(1600);
cadRasterizationOptions.setLayouts(new String[] {"Model"});
```

### ขั้นตอนที่ 7: บันทึกไฟล์ PDF ที่ได้
สุดท้าย, ส่งออกภาพวาดที่แก้ไขเป็นไฟล์ PDF. อินสแตนซ์ `image` เดียวกันถูกใช้, ดังนั้น PDF จะสะท้อนภาพ raster ที่เพิ่งเพิ่มใหม่.  
```java
image.save((srcFile + "_generated.pdf"), pdfOptions);
```

โดยทำตามขั้นตอนเหล่านี้, คุณสามารถ **add image to dwg** ไฟล์ได้อย่างรวดเร็วและยัง **save dwg as pdf** เมื่อจำเป็น, ครอบคลุมการดำเนินการ **dwg file operations** ที่พบบ่อยที่สุดในรูทีนเดียวที่กระชับ.

## ปัญหาทั่วไปและวิธีแก้
- **Image not appearing** – ตรวจสอบให้แน่ใจว่าเส้นทางไฟล์รูปภาพ (`road-sign-custom.png`) ถูกต้องและขนาดภาพตรงกับค่าที่ส่งไปยัง `CadRasterImageDef`.  
- **Incorrect scaling** – ปรับเวกเตอร์ U และ V; พวกมันแสดงหน่วยภาพวาดต่อพิกเซล.  
- **PDF looks blank** – ตรวจสอบให้ `CadRasterizationOptions.setDrawType` ตั้งค่าเป็น `UseObjectColor` หรือโหมดที่เหมาะสมอื่น ๆ.  

## คำถามที่พบบ่อย

**Q: Aspose.CAD for Java รองรับสภาพแวดล้อมการพัฒนา Java ทั้งหมดหรือไม่?**  
A: ใช่, Aspose.CAD for Java ทำงานกับ IDE ใดก็ได้ที่รองรับ JDK 8+, รวมถึง IntelliJ IDEA, Eclipse, และ VS Code.

**Q: ฉันสามารถใช้ Aspose.CAD for Java ในโครงการเชิงพาณิชย์ได้หรือไม่?**  
A: ใช่, คุณสามารถใช้ Aspose.CAD for Java ในโครงการเชิงพาณิชย์. เยี่ยมชม **[here](https://purchase.aspose.com/buy)** สำหรับรายละเอียดการให้ลิขสิทธิ์.

**Q: มีรุ่นทดลองฟรีสำหรับ Aspose.CAD for Java หรือไม่?**  
A: มี, คุณสามารถเข้าถึงรุ่นทดลองฟรี **[here](https://releases.aspose.com/)**.

**Q: ฉันจะขอรับการสนับสนุนสำหรับ Aspose.CAD for Java ได้อย่างไร?**  
A: คุณสามารถขอรับการสนับสนุนได้ที่ **[Aspose.CAD forum](https://forum.aspose.com/c/cad/19)**.

**Q: ฉันสามารถขอรับลิขสิทธิ์ชั่วคราวสำหรับ Aspose.CAD for Java ได้หรือไม่?**  
A: ได้, คุณสามารถรับลิขสิทธิ์ชั่วคราว **[here](https://purchase.aspose.com/temporary-license/)**.

---

**อัปเดตล่าสุด:** 2026-05-20  
**ทดสอบด้วย:** Aspose.CAD for Java 24.11  
**ผู้เขียน:** Aspose  

{{< blocks/products/products-backtop-button >}}

## บทแนะนำที่เกี่ยวข้อง

- [Export DWG to PDF or Raster Using Aspose.CAD for Java](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)
- [Add Custom Properties DWG Files Using Aspose.CAD for Java](/cad/java/additional-features/add-custom-properties/)
- [Save CAD as PNG – Convert CAD Drawing to Raster Image Format Using Aspose.CAD for Java](/cad/java/cad-drawing-conversion/convert-cad-drawing-to-raster-image/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}