---
date: 2025-12-28
description: เรียนรู้วิธีปรับแต่งแบบอักษรในภาพวาด DWG ด้วย Aspose.CAD สำหรับ Java
  คู่มือขั้นตอนต่อขั้นตอนในการเพิ่มข้อความ แทนที่แบบอักษร และทำให้คำอธิบาย CAD สมบูรณ์แบบ
linktitle: CAD Text and Annotation
second_title: Aspose.CAD Java API
title: วิธีปรับแต่งฟอนต์ในข้อความและคำอธิบาย CAD
url: /th/java/cad-text-and-annotation/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# วิธีปรับแต่งแบบอักษรในข้อความ CAD และคำอธิบาย

## Introduction 

หากคุณกำลังมองหา **วิธีปรับแต่งแบบอักษร** ในไฟล์ DWG ของคุณ คุณมาถูกที่แล้ว ในบทแนะนำนี้เราจะพาคุณผ่านการเพิ่มข้อความ, การแทนที่แบบอักษร, และการปรับสไตล์ของแบบอักษรโดยใช้ Aspose.CAD for Java ไม่ว่าคุณจะกำลังทำให้แผนภาพดูดีขึ้น, เตรียมเอกสารก่อสร้าง, หรือเพียงต้องการ **คำอธิบายข้อความ dwg** ที่ชัดเจนขึ้น ขั้นตอนเหล่านี้จะช่วยให้คุณได้ผลลัพธ์ระดับมืออาชีพอย่างรวดเร็วและเชื่อถือได้

## Quick Answers
- **วัตถุประสงค์หลักของการปรับแต่งแบบอักษรใน DWG คืออะไร?** เพื่อปรับปรุงความอ่านง่ายและให้สอดคล้องกับแบรนด์หรือมาตรฐานของโครงการ  
- **ไลบรารีที่จัดการการเปลี่ยนแปลงคืออะไร?** Aspose.CAD for Java.  
- **ฉันต้องการไลเซนส์หรือไม่?** การทดลองใช้ฟรีเพียงพอสำหรับการประเมิน; จำเป็นต้องมีไลเซนส์เชิงพาณิชย์สำหรับการใช้งานจริง  
- **ฉันสามารถประมวลผลไฟล์ DWG ขนาดใหญ่ได้หรือไม่?** ได้ – API สตรีมข้อมูลอย่างมีประสิทธิภาพ เหมาะกับภาพวาดขนาดใหญ่  
- **ต้องการซอฟต์แวร์เพิ่มเติมหรือไม่?** เพียงแค่ Java runtime (JDK 8 หรือใหม่กว่า) และ Aspose.CAD JAR  

## What is “how to customize fonts” in CAD?
การปรับแต่งแบบอักษรหมายถึงการแทนที่สไตล์ข้อความเริ่มต้นในไฟล์ DWG ด้วยแบบอักษรที่คุณเลือก, ปรับขนาด, น้ำหนัก, หรือใช้สไตล์ต่าง ๆ กับเลเยอร์หรือวัตถุเฉพาะ. สิ่งนี้ทำให้ภาพวาดแสดงผลตามที่คุณต้องการในทุกโปรแกรมดู

## Why use Aspose.CAD for Java to customize fonts?
- **การควบคุมเต็มรูปแบบ** ของวัตถุข้อความโดยไม่ต้องเปิดภาพวาดในโปรแกรมแก้ไขแบบ GUI  
- **การประมวลผลเป็นชุด** – จัดการหลายสิบไฟล์ในสคริปต์เดียว  
- **ข้ามแพลตฟอร์ม** – ทำงานบน Windows, Linux, และ macOS  
- **ไม่มีการพึ่งพาภายนอก** – API จัดการการแยกวิเคราะห์ DWG ภายใน  

## Prerequisites
- Java Development Kit 8 หรือใหม่กว่า ติดตั้งแล้ว  
- เพิ่ม Aspose.CAD for Java JAR ไปยัง classpath ของโปรเจคของคุณ  
- ไฟล์ DWG ที่คุณต้องการแก้ไข  

## How to Add Text in DWG
Adding new textual information is a common need when you want to label parts, add notes, or create **dwg text annotation**. Follow these steps:

1. **โหลดไฟล์ DWG** ด้วย `CadImage`.  
2. **สร้างเอนทิตี `CadText`** ด้วยสตริงที่ต้องการ, ตำแหน่ง, และแบบอักษร  
3. **เพิ่มเอนทิตี** ไปยังคอลเลกชันของเอนทิตีในภาพวาด  
4. **บันทึก** ไฟล์ที่แก้ไขแล้ว  

*หมายเหตุ: โค้ดสแนปเปตจริงไม่ได้มีการเปลี่ยนแปลงจากบทแนะนำต้นฉบับและรวมอยู่ในบทแนะนำย่อยที่เชื่อมโยง*  

## How to Replace Font in DWG
Replacing an existing font throughout a drawing helps maintain consistency, especially when the original font isn’t available on the target system.

1. **เปิดไฟล์ DWG** ด้วย `CadImage`.  
2. **วนลูป** ผ่านวัตถุ `CadText` ทั้งหมด.  
3. **ตั้งค่าคุณสมบัติ `FontName`** ให้เป็นแบบอักษรที่คุณต้องการ (เช่น “Arial”)  
4. **บันทึก** ภาพวาดที่อัปเดตแล้ว  

วิธีนี้อธิบายอย่างละเอียดในบทแนะนำย่อย “Substitute Font in DWG”

## How to Change DWG Font Style for a Particular Style
Sometimes only a specific text style (e.g., “Title”) needs a new font while others stay unchanged.

1. **ระบุชื่อสไตล์** ที่คุณต้องการแก้ไข.  
2. **ค้นหาอ็อบเจ็กต์ `CadTextStyle` ที่สอดคล้อง**.  
3. **อัปเดต `FontName`** ของมันและคุณลักษณะสไตล์เพิ่มเติมใด ๆ  
4. **บันทึกการเปลี่ยนแปลง** โดยการบันทึกไฟล์  

คู่มือขั้นตอนโดยละเอียดมีในบทแนะนำย่อย “Substitute Font of a Particular Style in DWG”

## Common Use Cases
- **ภาพวาดก่อสร้าง** ที่ต้องใช้แบบอักษรมาตรฐานของบริษัท  
- **แผนผังสถาปัตยกรรม** ที่ต้องการคำอธิบายที่อ่านง่ายสำหรับลูกค้า  
- **การแปลงเป็นชุด** ของไฟล์ DWG เก่าเป็นชุดแบบอักษรใหม่ขององค์กร  

## CAD Text and Annotation Tutorials
### [Add Text in DWG Using Aspose.CAD for Java](./add-text-in-dwg/)
เพิ่มประสิทธิภาพให้กับภาพวาด DWG ของคุณอย่างง่ายดายด้วย Aspose.CAD for Java. เพิ่มข้อความอย่างราบรื่นด้วยคู่มือขั้นตอนของเรา

### [Substitute Font in DWG with Aspose.CAD for Java](./substitute-font-in-dwg/)
เพิ่มประสิทธิภาพการออกแบบ CAD ของคุณอย่างง่ายดาย. เรียนรู้การแทนที่แบบอักษรในไฟล์ DWG ด้วย Aspose.CAD for Java. คู่มือขั้นตอนเพื่อความสมบูรณ์แบบของภาพ

### [Substitute Font of a Particular Style in DWG Using Aspose.CAD for Java](./substitute-font-of-particular-style-in-dwg/)
เรียนรู้วิธีการแทนที่แบบอักษรในไฟล์ DWG ด้วย Aspose.CAD for Java. คู่มือขั้นตอนสำหรับการปรับแต่งสไตล์อย่างแม่นยำ

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

## Frequently Asked Questions

**Q: ฉันสามารถใช้วิธีเหล่านี้กับไฟล์ DWG ที่สร้างในเวอร์ชัน AutoCAD เก่าได้หรือไม่?**  
A: ได้. Aspose.CAD รองรับเวอร์ชัน DWG ตั้งแต่ R12 จนถึงรุ่นล่าสุด

**Q: จะเกิดอะไรขึ้นหากแบบอักษรเป้าหมายไม่ได้ติดตั้งบนเครื่องของผู้ดู?**  
A: ภาพวาดจะกลับไปใช้แบบอักษรเริ่มต้น ซึ่งอาจส่งผลต่อการจัดวาง. การฝังแบบอักษรหรือการตรวจสอบให้แน่ใจว่าติดตั้งบนทุกเครื่องเป็นสิ่งที่แนะนำ

**Q: สามารถแทนที่แบบอักษรได้เฉพาะบนเลเยอร์ที่กำหนดหรือไม่?**  
A: แน่นอน. กรองวัตถุ `CadText` ตาม `LayerName` ก่อนเปลี่ยน `FontName`

**Q: ฉันต้องสร้างภาพวาดใหม่หลังจากเปลี่ยนแบบอักษรหรือไม่?**  
A: ไม่จำเป็นต้องสร้างใหม่ด้วยตนเอง; การบันทึก `CadImage` จะเขียนการอัปเดตทั้งหมดลงในไฟล์

**Q: ฉันจะตรวจสอบได้อย่างไรว่าแบบอักษรถูกเปลี่ยนอย่างถูกต้อง?**  
A: เปิด DWG ด้วยโปรแกรมดูใด ๆ ที่รองรับแบบอักษรที่เลือก, หรือโดยโปรแกรมนับจำนวนวัตถุ `CadText` เพื่ออ่านค่า `FontName` กลับมา

**อัปเดตล่าสุด:** 2025-12-28  
**ทดสอบด้วย:** Aspose.CAD for Java 24.12  
**ผู้เขียน:** Aspose