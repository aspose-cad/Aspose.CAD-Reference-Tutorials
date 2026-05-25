---
date: 2026-05-25
description: เรียนรู้วิธีตั้งค่าใบอนุญาตแบบมิเตอร์ใน Aspose.CAD สำหรับ Java เพื่อเพิ่มประสิทธิภาพการประมวลผล
  CAD ลดค่าใช้จ่าย และติดตามการใช้งานอย่างมีประสิทธิภาพ
keywords:
- how to set metered
- Aspose.CAD licensing
- Java metered licensing
linktitle: วิธีตั้งค่าใบอนุญาตแบบมิเตอร์ใน Aspose.CAD
schemas:
- author: Aspose
  dateModified: '2026-05-25'
  description: Learn how to set metered licensing in Aspose.CAD for Java to optimize
    CAD processing, reduce costs, and track usage efficiently.
  headline: How to Set Metered Licensing in Aspose.CAD
  type: TechArticle
- questions:
  - answer: A usage‑based model that tracks API calls and charges per consumption
      unit.
    question: What is metered licensing?
  - answer: Two keys – a public and a private key – generated from your Aspose account.
    question: How many keys are required?
  - answer: Yes, call `License.getConsumptionQuantity()` before and after processing.
    question: Can I check usage programmatically?
  - answer: A free trial license can be obtained from the Aspose website.
    question: Is a trial available?
  - answer: Java 8 through 17 are fully supported.
    question: Which Java version is supported?
  type: FAQPage
second_title: Aspose.CAD Java API
title: วิธีตั้งค่าใบอนุญาตแบบมิเตอร์ใน Aspose.CAD
url: /th/java/licensing-and-configuration/metered-licensing-in-aspose-cad/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# การให้สิทธิ์แบบมิเตอร์ใน Aspose.CAD

## บทนำ

ปลดล็อกศักยภาพเต็มของ Aspose.CAD สำหรับ Java ด้วย **วิธีตั้งค่ามิเตอร์**! คู่มือขั้นตอนนี้จะพาคุณผ่านทุกขั้นตอน — ตั้งแต่การติดตั้งข้อกำหนดเบื้องต้น การนำเข้าแพ็กเกจที่ถูกต้อง ไปจนถึงการวัดการใช้ก่อนและหลังการประมวลผล เมื่อเสร็จสิ้นคุณจะทราบอย่างแม่นยำ **วิธีตั้งค่ามิเตอร์** คีย์, อ่านเมตริกการใช้, และทำให้กระบวนการทำงาน CAD ของคุณคุ้มค่าตามต้นทุน.

## คำตอบด่วน
- **อะไรคือการให้สิทธิ์แบบมิเตอร์?** โมเดลการให้สิทธิ์แบบใช้ตามการใช้งานที่ติดตามการเรียก API และเรียกเก็บตามหน่วยการใช้.  
- **ต้องใช้กุญแจกี่ใบ?** กุญแจสองใบ — กุญแจสาธารณะและกุญแจส่วนตัว — สร้างจากบัญชี Aspose ของคุณ.  
- **ฉันสามารถตรวจสอบการใช้โปรแกรมได้หรือไม่?** ใช่, เรียก `License.getConsumptionQuantity()` ก่อนและหลังการประมวลผล.  
- **มีรุ่นทดลองหรือไม่?** สามารถรับใบอนุญาตทดลองฟรีจากเว็บไซต์ Aspose.  
- **รองรับเวอร์ชัน Java ใด?** Java 8 ถึง 17 ได้รับการสนับสนุนเต็มรูปแบบ.

## การให้สิทธิ์แบบมิเตอร์ใน Aspose.CAD คืออะไร?
การให้สิทธิ์แบบมิเตอร์คือโมเดลจ่ายตามการใช้ของ Aspose.CAD ที่บันทึกการเรียกแต่ละ API เป็นหน่วยการใช้ ช่วยให้คุณตรวจสอบการใช้ที่แม่นยำ, ป้องกันการจัดสรรเกินความจำเป็น, และจ่ายเฉพาะสิ่งที่คุณใช้จริงเท่านั้น.

## ทำไมต้องใช้การให้สิทธิ์แบบมิเตอร์สำหรับการประมวลผล CAD?
Aspose.CAD รองรับรูปแบบการนำเข้าและส่งออก **กว่า 50** รูปแบบ — รวมถึง DWG, DXF, DGN, และ SVG — และสามารถประมวลผลไฟล์ขนาดสูงสุด **2 GB** โดยไม่ต้องโหลดเอกสารทั้งหมดเข้าสู่หน่วยความจำ ประสิทธิภาพนี้ทำให้ค่าใช้จ่ายเซิร์ฟเวอร์ลดลง, โดยเฉพาะเมื่อจัดการชุดภาพวาดขนาดใหญ่.

## ข้อกำหนดเบื้องต้น

ก่อนจะดำดิ่งสู่การให้สิทธิ์แบบมิเตอร์กับ Aspose.CAD, โปรดตรวจสอบว่าคุณมีสิ่งต่อไปนี้พร้อมแล้ว:

### การติดตั้ง Java Development Kit (JDK)

ตรวจสอบว่าคุณได้ติดตั้ง Java Development Kit เวอร์ชันล่าสุดบนระบบของคุณแล้ว คุณสามารถดาวน์โหลดได้จาก [here](https://www.oracle.com/java/technologies/javase-downloads.html).

### ไลบรารี Aspose.CAD สำหรับ Java

ตรวจสอบให้แน่ใจว่าได้ดาวน์โหลดและตั้งค่าไลบรารี Aspose.CAD สำหรับ Java คุณสามารถค้นหาไลบรารีได้จาก [here](https://releases.aspose.com/cad/java/). คุณยังสามารถเรียกดูการปล่อย Aspose อื่น ๆ ได้จาก [here](https://releases.aspose.com/).

## วิธีตั้งค่าการให้สิทธิ์แบบมิเตอร์ใน Aspose.CAD สำหรับ Java?

โหลดกุญแจสาธารณะและส่วนตัวของคุณ, เรียก `License.setMeteredKey(publicKey, privateKey)`, แล้วไลบรารีจะเปลี่ยนเป็นโหมดมิเตอร์ทันที การเรียกครั้งเดียวนี้เปิดการติดตามการใช้สำหรับทุกการดำเนินการ API ถัดไป, ทำให้คุณสามารถสอบถามการใช้ก่อนและหลังขั้นตอนการประมวลผลใด ๆ ได้.

## นำเข้าแพ็กเกจ

เพื่อใช้ไลบรารี, ให้นำเข้าแพ็กเกจหลักของมัน:

`import com.aspose.cad.*;` นำคลาส Aspose.CAD เข้าสู่โปรเจกต์ของคุณ.

```java
import com.aspose.cad;
```

## ขั้นตอนที่ 1: ตั้งค่ากุญแจมิเตอร์

`setMeteredKey` ลงทะเบียนกุญแจสาธารณะและส่วนตัวของคุณกับไลบรารี Aspose.CAD.

ขั้นแรก, ตั้งค่ากุญแจมิเตอร์โดยใช้เมธอด `setMeteredKey`. แทนที่ `<valid public key>` และ `<valid private key>` ด้วยกุญแจสาธารณะและส่วนตัวที่แท้จริงของคุณ.

```java
Metered.setMeteredKey("<valid public key>", "<valid private key>");
```

## ขั้นตอนที่ 2: รับค่าปริมาณการใช้ก่อนการประมวลผล

`getConsumptionQuantity` คืนค่าจำนวนหน่วยการใช้ที่บันทึกจนถึงขณะนี้.

ดึงค่าปริมาณการใช้ก่อนเข้าถึง API ของ Aspose.CAD เพื่อให้ได้ความเข้าใจเบื้องต้น.

```java
BigDecimal quantityOld = Metered.getConsumptionQuantity();
System.out.println("Consumption quantity before processing: " + quantityOld);
```

## ขั้นตอนที่ 3: การประมวลผล

ดำเนินการประมวลผล CAD ที่คุณต้องการโดยใช้ฟังก์ชันของ Aspose.CAD. ยกเลิกคอมเมนต์โค้ดสแนปที่เกี่ยวข้องกับงานของคุณ, เช่นการโหลดภาพ CAD.

```java
// Example:
// com.aspose.cad.fileformats.cad.CadImage image =
// (com.aspose.cad.fileformats.cad.CadImage)com.aspose.cad.Image.load("BlockRefDgn.dwg");
```

## ขั้นตอนที่ 4: รับค่าปริมาณการใช้หลังการประมวลผล

หลังการประมวลผล, ให้รับค่าปริมาณการใช้อีกครั้งเพื่อประเมินผลกระทบ.

```java
BigDecimal quantity = Metered.getConsumptionQuantity();
System.out.println("Consumption quantity after processing: " + quantity);
```

ทำซ้ำขั้นตอนเหล่านี้สำหรับการประมวลผลหรือภารกิจเพิ่มเติมตามต้องการ.

## ปัญหาทั่วไปและวิธีแก้

- **Invalid key error:** ตรวจสอบอีกครั้งว่ากุญแจทั้งสองคัดลอกตรงตามที่แสดงในบัญชี Aspose ของคุณ; ช่องว่างเพิ่มเติมทำให้การตรวจสอบล้มเหลว.  
- **Zero consumption reported:** ตรวจสอบว่าคุณเรียก `License.getConsumptionQuantity()` *หลัง* การใช้ API ครั้งแรก; การเรียกครั้งแรกจะเริ่มต้นตัวนับ.  
- **Performance slowdown on large files:** ใช้ `CadImage.load(..., LoadOptions)` พร้อม `LoadOptions.setLoadMode(LoadMode.Stream)` เพื่อหลีกเลี่ยงการโหลดไฟล์เต็มเข้าสู่หน่วยความจำ.

## คำถามที่พบบ่อย

**Q1: ฉันสามารถใช้การให้สิทธิ์แบบมิเตอร์เพื่อการประเมินได้หรือไม่?**  
A1: ใช่, คุณสามารถรับใบอนุญาตทดลองฟรีได้จาก [here](https://releases.aspose.com/).

**Q2: ฉันจะหาเอกสารรายละเอียดสำหรับ Aspose.CAD สำหรับ Java ได้ที่ไหน?**  
A2: ดูเอกสารที่ [here](https://reference.aspose.com/cad/java/).

**Q3: ฉันจะซื้อใบอนุญาตสำหรับ Aspose.CAD สำหรับ Java อย่างไร?**  
A3: ไปที่หน้าซื้อ [here](https://purchase.aspose.com/buy).

**Q4: มีตัวเลือกใบอนุญาตชั่วคราวหรือไม่?**  
A5: ใช่, คุณสามารถสำรวจใบอนุญาตชั่วคราวได้ที่ [here](https://purchase.aspose.com/temporary-license/).

**Q5: ต้องการการสนับสนุนจากชุมชนหรือมีคำถามเฉพาะ?**  
A5: ไปที่ฟอรั่ม Aspose.CAD [here](https://forum.aspose.com/c/cad/19).

**Q6: การให้สิทธิ์แบบมิเตอร์ทำงานกับการปรับใช้บนคลาวด์หรือไม่?**  
A6: แน่นอน. การเรียก `setMeteredKey` เดียวกันทำงานใน Docker, Kubernetes หรือสภาพแวดล้อมแบบ serverless.

**Q7: ฉันสามารถรีเซ็ตตัวนับการใช้ได้หรือไม่?**  
A7: ตัวนับจะรีเซ็ตอัตโนมัติเมื่อเริ่มต้นรอบบิลใหม่; คุณไม่สามารถรีเซ็ตด้วยตนเองได้.

## สรุป

ขอแสดงความยินดี! คุณได้เชี่ยวชาญการให้สิทธิ์ **วิธีตั้งค่ามิเตอร์** กับ Aspose.CAD สำหรับ Java อย่างสำเร็จ ด้วยการทำตามคู่มือนี้, คุณได้ตั้งค่าและรวมการให้สิทธิ์แบบมิเตอร์เข้ากับโปรเจกต์ Java ของคุณอย่างราบรื่น, ทำให้การใช้ความสามารถของ Aspose.CAD มีประสิทธิภาพและค่าใช้จ่ายโปร่งใส.

---

**อัปเดตล่าสุด:** 2026-05-25  
**ทดสอบด้วย:** Aspose.CAD for Java 24.10  
**ผู้เขียน:** Aspose  

{{< blocks/products/products-backtop-button >}}

## บทแนะนำที่เกี่ยวข้อง

- [แปลง CAD เป็น PDF ด้วย Aspose.CAD สำหรับ Java – คู่มือเต็ม](/cad/java/)
- [สร้าง PDF จาก CAD – ส่งออก DXF เป็น PDF ด้วย Aspose.CAD สำหรับ Java](/cad/java/additional-features/export-dxf-to-pdf/)
- [ตั้งขนาด Canvas – ฟีเจอร์ CAD ขั้นสูงด้วย Aspose.CAD สำหรับ Java](/cad/java/advanced-cad-features/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}