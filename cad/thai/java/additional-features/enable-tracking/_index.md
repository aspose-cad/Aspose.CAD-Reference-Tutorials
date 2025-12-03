---
date: 2025-12-03
description: เรียนรู้วิธีตั้งขนาดหน้ากระดาษ PDF ขณะแปลง DWG เป็น PDF และเปิดใช้งานการติดตามในไฟล์
  DWG ด้วย Aspose.CAD สำหรับ Java – คู่มือครบถ้วนในการส่งออกไฟล์ PDF ของการวาด CAD
  อย่างแม่นยำ.
language: th
linktitle: Set PDF Page Size and Enable Tracking in DWG Files Using Java
second_title: Aspose.CAD Java API
title: ตั้งค่าขนาดหน้ากระดาษ PDF และเปิดใช้งานการติดตามในไฟล์ DWG ด้วย Aspose.CAD
  ใน Java
url: /java/additional-features/enable-tracking/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# กำหนดขนาดหน้า PDF และเปิดการติดตามในไฟล์ DWG ด้วย Aspose.CAD ใน Java

## บทนำ

หากคุณต้อง **กำหนดขนาดหน้า PDF** เมื่อ *แปลง DWG เป็น PDF* และต้องการติดตามปัญหาการเรนเดอร์ใด ๆ Aspose.CAD สำหรับ Java จะมอบวิธีการที่สะอาดและเป็นโปรแกรมเมติกให้ทำได้ทั้งสองอย่าง ในบทแนะนำนี้เราจะพาคุณผ่านขั้นตอนที่แม่นยำเพื่อกำหนดมิติของหน้า, เปิดการติดตาม, และส่งออกไฟล์ CAD เป็น PDF — ทั้งหมดจาก Java เมื่อจบคุณจะเข้าใจว่าทำไมการกำหนดขนาดหน้าที่ถูกต้องจึงสำคัญสำหรับการวาด CAD และวิธีจับข้อมูลการติดตามอย่างละเอียดระหว่างกระบวนการส่งออก

## คำตอบอย่างรวดเร็ว
- **What does “set PDF page size” affect?** มันกำหนดความกว้างและความสูงของแคนวาส PDF ที่สร้างขึ้น เพื่อให้การวาดของคุณพอดีอย่างสมบูรณ์  
- **Do I need a license to use this feature?** เวอร์ชันทดลองใช้ได้สำหรับการทดสอบ; ต้องมีลิขสิทธิ์เชิงพาณิชย์สำหรับการใช้งานจริง  
- **Which Aspose.CAD version is required?** เวอร์ชันล่าสุดใด ๆ ที่รองรับ `CadRasterizationOptions`  
- **Can I use this with other CAD formats?** ตัวอย่างแสดง DWG/DXF แต่แนวทางเดียวกันทำงานกับรูปแบบที่รองรับส่วนใหญ่  
- **How long does the conversion take?** ปกติใช้เวลาน้อยกว่าวินาทีสำหรับไฟล์ขนาดปานกลาง; ไฟล์ที่ใหญ่กว่าอาจใช้เวลานานขึ้น  

## “set PDF page size” คืออะไรในบริบทของการส่งออก CAD?
การกำหนดขนาดหน้า PDF บอกให้ตัวเรนเดอร์ทราบขนาดที่แน่นอน (เป็นพิกเซลหรือจุด) ของแคนวาสผลลัพธ์ ซึ่งสำคัญอย่างยิ่งสำหรับการวาดเชิงเทคนิคที่ต้องรักษาอัตราส่วนและการจัดวาง หากไม่มีการกำหนดขนาดหน้าอย่างชัดเจน PDF อาจใช้ขนาดเริ่มต้นที่ทำให้การวาดถูกตัดหรือบิดเบี้ยว

## ทำไมต้องกำหนดขนาดหน้า PDF เมื่อส่งออกการวาด CAD?
- **Preserve scale** – วิศวกรต้องการการพิมพ์ที่เป็นสเกลจริง  
- **Fit to paper** – เลือก A4, Letter หรือขนาดกำหนดเองที่ตรงกับสเปคของโครงการ  
- **Improve readability** – หน้าใหญ่ช่วยให้เห็นรายละเอียดเล็ก ๆ โดยไม่ต้องซูม  
- **Consistent output** – ระบบอัตโนมัติจะสร้าง PDF ที่มีขนาดเดียวกันทุกครั้งที่รัน  

## วิธีกำหนดขนาดหน้า PDF เมื่อแปลง DWG เป็น PDF?
ต่อไปเราจะกำหนด `CadRasterizationOptions` ด้วยค่าความกว้างและความสูงที่กำหนดเองก่อนทำการส่งออก ขั้นตอนนี้ตรงกับคีย์เวิร์ดหลัก **set PDF page size**  

## ข้อกำหนดเบื้องต้น

- **Java Development Kit (JDK)** – Java 8 หรือใหม่กว่า ติดตั้งบนเครื่องของคุณ  
- **Aspose.CAD for Java** – ดาวน์โหลดจากหน้า [Aspose CAD download page](https://releases.aspose.com/cad/java/)  
- **Document Directory** – โฟลเดอร์ที่บรรจุไฟล์ DWG/DXF ที่คุณต้องการประมวลผล  

## นำเข้า Namespaces

ก่อนอื่นให้ import คลาสที่จำเป็น โค้ดบล็อกจะคงไว้เหมือนต้นฉบับ

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.CadRenderResult;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.RenderResult;
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
```

## ขั้นตอนที่ 1: โหลดไฟล์ DWG/DXF

โหลดไฟล์การวาดต้นฉบับ ปรับเส้นทางให้ชี้ไปยังไฟล์ของคุณ

```java
String dataDir = "Your Document Directory" + "DXFDrawings/";
Image image = Image.load(dataDir + "conic_pyramid.dxf");
```

## ขั้นตอนที่ 2: กำหนดค่าตัวเลือกการส่งออก PDF (รวมถึงขนาดหน้า)

ที่นี่เราตั้งค่าความกว้างและความสูงของหน้า – นี่คือจุดที่เราจะ **กำหนดขนาดหน้า PDF** ค่าต่าง ๆ อยู่ในหน่วยพิกเซล; คุณสามารถแปลงจากนิ้วหรือมิลลิเมตรตามต้องการ

```java
OutputStream stream = new FileOutputStream(dataDir + "output_conic_pyramid.pdf");
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setPageWidth(800);   // <-- custom width
cadRasterizationOptions.setPageHeight(600);  // <-- custom height
```

> **Tip:** หากคุณต้องการใช้ขนาดกระดาษมาตรฐาน ให้ใช้การแปลง `1 inch = 72 points` สำหรับหน้า A4 (8.27 × 11.69 in) ให้ตั้งค่า `pageWidth = 595` และ `pageHeight = 842`

## ขั้นตอนที่ 3: ใช้การติดตาม

การติดตามจะจับปัญหาการเรนเดอร์ใด ๆ เราแนบตัวจัดการแบบกำหนดเองที่จะถูกเรียกหลังจากการส่งออก

```java
cadRasterizationOptions.RenderResult = new ErrorHandler();
```

## ขั้นตอนที่ 4: ส่งออกเป็น PDF

ทำการแปลง ตอนนี้ PDF จะถูกสร้างด้วยขนาดที่คุณกำหนดและข้อมูลการติดตามจะถูกพิมพ์ลงคอนโซล

```java
System.out.println("Exporting to pdf format");
image.save(stream, pdfOptions);
```

## ขั้นตอนที่ 5: คลาส CadRenderHandler

ตัวจัดการนี้พิมพ์ข้อผิดพลาดใด ๆ ที่เกิดขึ้นระหว่างการเรนเดอร์ ช่วยให้คุณดีบักเมื่อ **ส่งออก CAD drawing PDF**

```java
public static class ErrorHandler extends CadRasterizationOptions.CadRenderHandler {
    @Override
    public void invoke(CadRenderResult result) {
        System.out.println("Tracking results of exporting");

        if (result.isRenderComplete())
            return;

        System.out.println("Have some problems:");

        int idxError = 1;
        for (RenderResult rr : result.getFailures()) {
            System.out.printf("{0}. {1}, {2}", idxError, rr.getRenderCode(), rr.getMessage());
            idxError++;
        }
    }
}
```

## ปัญหาที่พบบ่อยและวิธีแก้

| Issue | Cause | Fix |
|-------|-------|-----|
| **Blank PDF** | Page size set to 0 or too small | Verify `setPageWidth` and `setPageHeight` are positive values. |
| **Missing geometry** | Rendering errors captured by the handler | Review the console output from `ErrorHandler` and address the specific `RenderCode`. |
| **File not found** | Incorrect `dataDir` path | Use an absolute path or ensure the directory exists. |
| **License exception** | Using the trial without a valid license for large files | Apply your Aspose.CAD license before loading the image. |

## คำถามที่พบบ่อย

**Q: Can I enable tracking for other CAD file formats using Aspose.CAD for Java?**  
A: Aspose.CAD primarily supports DWG/DXF for tracking. For other formats, consult the official documentation.

**Q: How can I handle additional export options in Aspose.CAD for Java?**  
A: The library offers many options such as DPI, background color, and vector rasterization. See the [Aspose.CAD Java Documentation](https://reference.aspose.com/cad/java/) for details.

**Q: Is there a trial version available for Aspose.CAD for Java?**  
A: Yes, you can download a free trial from the [Aspose.CAD Free Trial](https://releases.aspose.com/).

**Q: Where can I seek assistance or discuss issues related to Aspose.CAD for Java?**  
A: Visit the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) for community support and official answers.

**Q: How do I obtain a temporary license for Aspose.CAD for Java?**  
A: Follow the steps outlined on the [Temporary License](https://purchase.aspose.com/temporary-license/) page.

**Last Updated:** 2025-12-03  
**Tested With:** Aspose.CAD for Java 24.11 (latest at time of writing)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}