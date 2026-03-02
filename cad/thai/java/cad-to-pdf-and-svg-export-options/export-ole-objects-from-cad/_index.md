---
date: 2026-03-02
description: ปลดล็อกศักยภาพของ Aspose.CAD สำหรับ Java อย่างง่ายดาย ส่งออกวัตถุ OLE
  ได้โดยไม่มีความยุ่งยากและ **บันทึก CAD เป็น PNG** ดาวน์โหลดตอนนี้เพื่อการจัดการข้อมูล
  CAD ที่ราบรื่น
linktitle: Export OLE Objects from CAD
second_title: Aspose.CAD Java API
title: บันทึก CAD เป็น PNG – ส่งออกวัตถุ OLE ด้วย Aspose.CAD สำหรับ Java
url: /th/java/cad-to-pdf-and-svg-export-options/export-ole-objects-from-cad/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# บันทึก CAD เป็น PNG – ส่งออกวัตถุ OLE ด้วย Aspose.CAD สำหรับ Java

## บทนำ

ในโลกที่เปลี่ยนแปลงอย่างรวดเร็วของ Computer-Aided Design (CAD) การจัดการและสกัดวัตถุ OLE (Object Linking and Embedding) อย่างมีประสิทธิภาพ—พร้อมกับความสามารถในการ **บันทึก CAD เป็น PNG**—เป็นสิ่งสำคัญสำหรับกระบวนการทำงานต่อเนื่อง เช่น การรายงาน, การแสดงตัวอย่างบนเว็บ, หรือการเก็บถาวร Aspose.CAD สำหรับ Java มอบโซลูชันแบบ code‑first ที่ทรงพลังซึ่งช่วยให้คุณสามารถส่งออกวัตถุ OLE และแปลงภาพวาด CAD เป็นภาพ PNG คุณภาพสูงได้ด้วยไม่กี่บรรทัดของโค้ด

## คำตอบด่วน
- **Aspose.CAD ทำอะไร?** มันอ่าน, ปรับแต่ง, และแปลงไฟล์ CAD (DWG, DXF, DGN ฯลฯ) โดยไม่ต้องใช้ซอฟต์แวร์ CAD ดั้งเดิม  
- **ฉันสามารถบันทึก CAD เป็น PNG ได้หรือไม่?** ได้—ใช้ `PngOptions` ร่วมกับ `CadRasterizationOptions` เพื่อเรสเตอร์ไลซ์เลย์เอาต์ใดก็ได้  
- **วิธีส่งออกวัตถุ OLE?** โหลดไฟล์ CAD ด้วย `Image.load` แล้วบันทึกแต่ละเลย์เอาต์ที่มี OLE เป็น PNG  
- **ต้องการไลเซนส์หรือไม่?** มีรุ่นทดลองฟรี; ไลเซนส์เชิงพาณิชย์จะลบข้อจำกัดของรุ่นประเมินผล  
- **ต้องการ Java เวอร์ชันใด?** รองรับ Java 8 หรือสูงกว่าอย่างเต็มที่  

## **save CAD as PNG** คืออะไร?
การบันทึก CAD เป็น PNG หมายถึงการเรสเตอร์ไลซ์ภาพวาด CAD ที่เป็นเวกเตอร์ให้เป็นภาพ PNG ที่เป็นพิกเซล การแปลงนี้มีประโยชน์เมื่อคุณต้องการรูปแบบที่เบา, สามารถดูได้ทั่วโลกสำหรับหน้าเว็บ, แอปมือถือ, หรือเอกสาร

## ทำไมต้องใช้ Aspose.CAD สำหรับ Java เพื่อ **convert CAD to PNG**?
- **ไม่ต้องติดตั้ง CAD** – ไลบรารีทำงานทั้งหมดใน Java  
- **รักษาความแม่นยำของเลย์เอาต์** – สามารถเลือกเลย์เอาต์เฉพาะ, ควบคุม DPI, และรักษาคุณภาพเส้นได้  
- **ประมวลผลแบบแบตช์** – ทำซ้ำหลายไฟล์ด้วยลูปง่าย ๆ  
- **ส่งออกวัตถุ OLE** – เนื้อหา OLE ที่ฝังอยู่ในไฟล์ DWG/DXF จะถูกเรนเดอร์อัตโนมัติเป็นภาพ PNG  

## ข้อกำหนดเบื้องต้น

ก่อนเริ่มทำตามบทเรียนนี้ โปรดตรวจสอบว่าคุณมีข้อกำหนดต่อไปนี้พร้อมใช้งาน:

- **สภาพแวดล้อม Java** – ตรวจสอบว่าคุณมีสภาพแวดล้อมการพัฒนา Java ตั้งค่าไว้บนเครื่องของคุณแล้ว  
- **Aspose.CAD สำหรับ Java** – ดาวน์โหลดและติดตั้งไลบรารี Aspose.CAD สำหรับ Java คุณสามารถหาไลบรารีได้จาก [download link](https://releases.aspose.com/cad/java/)  
- **ไฟล์ CAD** – เตรียมไฟล์ CAD ที่มีวัตถุ OLE ที่คุณต้องการส่งออก  

## นำเข้า Namespaces

เพื่อเริ่มต้น ให้นำเข้า namespaces ที่จำเป็นเข้าสู่โครงการ Java ของคุณ Namespaces เหล่านี้ให้คลาสและฟังก์ชันที่จำเป็นสำหรับการทำงานกับไฟล์ CAD ด้วย Aspose.CAD

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

ตอนนี้เราจะอธิบายขั้นตอนการส่งออกวัตถุ OLE จาก CAD เป็นหลายขั้นตอน:

## วิธี **save CAD as PNG** และส่งออกวัตถุ OLE

### ขั้นตอนที่ 1: ตั้งค่าไดเรกทอรีเอกสารของคุณ

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

อย่าลืมแทนที่ `"Your Document Directory"` ด้วยพาธของไดเรกทอรีที่เก็บไฟล์ CAD ของคุณ

### ขั้นตอนที่ 2: กำหนดชื่อไฟล์ CAD

```java
String[] files = new String[] { "D ZD junior D10m H2m.dwg", "ZD - Senior D6m H2m45.dwg" };
```

ระบุชื่อไฟล์ CAD ที่คุณต้องการประมวลผลในอาเรย์ `files`

### ขั้นตอนที่ 3: ตั้งค่าตัวเลือกการส่งออก PNG

```java
PngOptions pngOptions = new PngOptions();
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
pngOptions.setVectorRasterizationOptions(rasterizationOptions);
rasterizationOptions.setLayouts(new String[] { "Layout1" });
```

กำหนดค่าตัวเลือกการส่งออก PNG รวมถึงการเรสเตอร์ไลซ์เวกเตอร์และการตั้งค่าเลย์เอาต์ ตัวเลือกเหล่านี้ทำให้คุณ **convert CAD to PNG** ด้วยคุณภาพที่ต้องการ

### ขั้นตอนที่ 4: วนลูปผ่านไฟล์ CAD

```java
for(String file : files)
{
    CadImage cadImage = (CadImage)Image.load(dataDir + file);
    cadImage.save(dataDir + file + "_out.png", pngOptions);
}
```

วนลูปผ่านแต่ละไฟล์ CAD ที่ระบุ, โหลดด้วย Aspose.CAD, และบันทึกวัตถุ OLE เป็นภาพ PNG ลูปนี้แสดงวิธีง่าย ๆ ในการ **convert DWG to PNG** แบบเป็นกลุ่ม

## ปัญหาและวิธีแก้ไขทั่วไป

| ปัญหา | สาเหตุ | วิธีแก้ |
|-------|-------|----------|
| **ผลลัพธ์ PNG ว่าง** | ชื่อเลย์เอาต์ไม่ตรงกัน | ตรวจสอบให้แน่ใจว่าชื่อเลย์เอาต์ (`"Layout1"`) มีอยู่ใน DWG ต้นฉบับ |
| **กราฟิก OLE หายไป** | วัตถุ OLE ถูกเก็บในเลย์เอาต์อื่น | รวมเลย์เอาต์ที่เกี่ยวข้องทั้งหมดใน `rasterizationOptions.setLayouts(...)` |
| **ข้อผิดพลาดหน่วยความจำไม่พอในไฟล์ขนาดใหญ่** | การตั้งค่า DPI สูง | ลด DPI ผ่าน `rasterizationOptions.setResolution(...)` หรือประมวลผลไฟล์ทีละไฟล์ |

## คำถามที่พบบ่อย

**Q: Aspose.CAD รองรับรูปแบบไฟล์ CAD ทุกประเภทหรือไม่?**  
A: Aspose.CAD รองรับรูปแบบ CAD หลากหลาย รวมถึง DWG, DXF, และ DGN. ดูรายละเอียดเพิ่มเติมใน [documentation](https://reference.aspose.com/cad/java/) สำหรับรายการเต็ม

**Q: ฉันสามารถปรับแต่งการตั้งค่าการส่งออกสำหรับวัตถุ OLE ได้หรือไม่?**  
A: ได้, Aspose.CAD มีตัวเลือกการปรับแต่งการส่งออกอย่างกว้างขวาง ช่วยให้คุณปรับผลลัพธ์ให้ตรงกับความต้องการของคุณ

**Q: มีรุ่นทดลองฟรีสำหรับ Aspose.CAD หรือไม่?**  
A: มี, คุณสามารถสำรวจความสามารถของ Aspose.CAD ได้โดยรับรุ่นทดลองฟรีจาก [here](https://releases.aspose.com/)

**Q: จะหาแหล่งสนับสนุนชุมชนสำหรับ Aspose.CAD ได้จากที่ไหน?**  
A: เข้าร่วมชุมชน Aspose.CAD ที่ [forum](https://forum.aspose.com/c/cad/19) เพื่อขอความช่วยเหลือและแบ่งปันประสบการณ์

**Q: จะซื้อไลเซนส์สำหรับ Aspose.CAD ได้อย่างไร?**  
A: เยี่ยมชม [purchase page](https://purchase.aspose.com/buy) เพื่อเลือกไลเซนส์ที่เหมาะกับความต้องการการพัฒนาของคุณ

## สรุป

ด้วยขั้นตอนง่าย ๆ แต่ทรงพลังเหล่านี้ คุณสามารถ **บันทึก CAD เป็น PNG** พร้อมกับส่งออกวัตถุ OLE จากไฟล์ CAD ได้อย่างราบรื่นโดยใช้ Aspose.CAD สำหรับ Java เครื่องมืออเนกประสงค์นี้ช่วยให้นักพัฒนาจัดการข้อมูล CAD ได้อย่างมีประสิทธิภาพ เปิดโอกาสใหม่ ๆ ในการพัฒนาแอปพลิเคชัน CAD และกระบวนการทำงานต่อเนื่องที่อิงภาพ

---

**Last Updated:** 2026-03-02  
**Tested With:** Aspose.CAD for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}