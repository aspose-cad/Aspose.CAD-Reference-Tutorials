---
date: 2026-01-10
description: تعلم كيفية تصدير DGN إلى DWG وتحويل ملفات MicroStation DGN إلى AutoCAD
  DWG باستخدام Aspose.CAD للغة Java. دليل خطوة بخطوة.
linktitle: Export DGN as Part of DWG
second_title: Aspose.CAD Java API
title: تصدير DGN إلى DWG باستخدام Aspose.CAD للـ Java
url: /ar/java/dgn-export-options/export-dgn-as-part-of-dwg/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تصدير DGN إلى DWG باستخدام Aspose.CAD للـ Java

## مقدمة

في هذا الدرس، ستتعلم كيفية **export dgn to dwg** ودمج تصميم MicroStation DGN داخل ملف AutoCAD DWG باستخدام مكتبة Aspose.CAD للـ Java. سواءً كنت تقوم بترحيل رسومات MicroStation القديمة أو تحتاج إلى دمج طبقات DGN تحتية مع تخطيطات DWG، يوجهك هذا الدليل خلال كل خطوة — من إعداد البيئة إلى إنشاء معاينة PDF للملف DWG النهائي.

## الإجابات السريعة
- **ما الذي يحققه “export dgn to dwg”?** يقوم بدمج DGN تحتية داخل DWG، مما يتيح عرضًا سلسًا في AutoCAD.
- **ما الصيغة التي يمكنني تصدير النتيجة إليها للمعاينة السريعة؟** يمكنك **export cad file to pdf** باستخدام `PdfOptions`.
- **هل أحتاج إلى ترخيص لتشغيل الكود؟** يلزم وجود ترخيص مؤقت أو مدفوع لـ Aspose.CAD للاستخدام في الإنتاج.
- **ما نسخة Java المدعومة؟** Java 8 أو أحدث تعمل مع أحدث إصدار من Aspose.CAD للـ Java.
- **هل تتوفر نسخة تجريبية مجانية؟** نعم – قم بتحميل نسخة تجريبية من موقع Aspose.

## ما هو “export dgn to dwg”؟
يعني تصدير DGN إلى DWG تحويل أو دمج تصميم MicroStation DGN كطبقة تحتية داخل رسم AutoCAD DWG. يتيح ذلك لمهندسي CAD الاستفادة من الأصول الموجودة بصيغة DGN دون الحاجة إلى إعادة إنشاء الهندسة من الصفر.

## لماذا تحويل MicroStation DGN إلى AutoCAD DWG؟
- **التعاون:** يمكن للفرق التي تستخدم AutoCAD عرض محتوى DGN وتحريره مباشرة.
- **التوحيد:** DWG هو الصيغة الفعلية للعديد من سير العمل اللاحقة (مثل إنشاء PDF، التصيير ثلاثي الأبعاد).
- **الحفظ:** يحافظ على مراجع DGN الأصلية دون تعديل، مما يقلل فقدان البيانات.

## المتطلبات المسبقة

قبل أن نغوص في الدرس، تأكد من توفر المتطلبات التالية:
1. **Aspose.CAD Library:** قم بتنزيل وتثبيت مكتبة Aspose.CAD للـ Java. يمكنك العثور على المكتبة [هنا](https://releases.aspose.com/cad/java/).
2. **Java Development Kit (JDK):** تأكد من تثبيت Java على نظامك.
3. **Integrated Development Environment (IDE):** اختر بيئة تطوير Java مثل Eclipse أو IntelliJ لتجربة تطوير أكثر سلاسة.

## استيراد الحزم

في مشروع Java الخاص بك، استورد الحزم الضرورية من Aspose.CAD لتمكين معالجة ملفات CAD. إليك مثالاً:

```java
import com.aspose.cad;
import com.aspose.cad.imageoptions;
import com.aspose.cad.fileformats.cad.cadconsts;
import com.aspose.cad.fileformats.cad;
import com.aspose.cad.fileformats.cad.cadobjects;
```

## الخطوة 1: تعيين مسارات الملفات

حدد مسارات الملفات الإدخال والإخراج لملف DWG. قم بتحديث المتغيرات `dataDir` و `fileName` و `outPath` وفقًا لذلك.

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "BlockRefDgn.dwg";
String outPath = dataDir + "BlockRefDgn.dwg.pdf";
```

## الخطوة 2: إنشاء كائن PdfOptions

أنشئ مثيلًا من الفئة `PdfOptions`، حيث أننا **exporting the CAD file to PDF** للتحقق السريع.

```java
PdfOptions exportOptions = new PdfOptions();
```

## الخطوة 3: تحميل ملف DWG

حمّل ملف DWG الموجود كصورة وحوله إلى النوع `CadImage`.

```java
CadImage cadImage = (CadImage) Image.load(fileName);
```

## الخطوة 4: التجول عبر الكيانات

انتقل عبر كل كيان داخل ملف DWG وتحقق مما إذا كان تعريف صورة. إذا كان كذلك، استرجع المرجع الخارجي للعنصر.

```java
for (CadBaseEntity baseEntity : cadImage.getEntities()) {
    if (baseEntity.getTypeName() == CadEntityTypeName.DGNUNDERLAY) {
        CadDgnUnderlay dgnFile = (CadDgnUnderlay)baseEntity;
        System.out.println(dgnFile.getUnderlayPath());
    }
}
```

## الخطوة 5: تعريف خيارات الترصيص

عرّف الإعدادات لكائن `CadRasterizationOptions`، بما في ذلك عرض الصفحة، الارتفاع، التخطيطات، ولون الخلفية.

```java
CadRasterizationOptions vectorRasterizationOptions = new CadRasterizationOptions();
vectorRasterizationOptions.setPageWidth(1600);
vectorRasterizationOptions.setPageHeight(1600);
vectorRasterizationOptions.setLayouts(new String[] { "Model" });
vectorRasterizationOptions.setAutomaticLayoutsScaling(false);
vectorRasterizationOptions.setNoScaling(true);
vectorRasterizationOptions.setBackgroundColor(Color.getBlack());
vectorRasterizationOptions.setDrawType(CadDrawTypeMode.UseObjectColor);
```

## الخطوة 6: تعيين خيارات الترصيص المتجه

حدد خيارات الترصيص المتجه للتصدير.

```java
exportOptions.setVectorRasterizationOptions(vectorRasterizationOptions);
```

## الخطوة 7: تصدير DWG إلى PDF

أخيرًا، صدّر DWG إلى PDF عن طريق استدعاء طريقة `save`.

```java
cadImage.save(outPath, exportOptions);
```

## المشكلات الشائعة والحلول

| المشكلة | السبب | الحل |
|-------|-------|----------|
| **عدم ظهور DGN تحتية** | ملف DWG لا يحتوي على كيان `DGNUNDERLAY`. | تحقق من أن ملف DWG المصدر يتضمن مرجع DGN. |
| **PDF فارغ** | تم ضبط خيارات الترصيص على حجم صفر أو تخطيط غير صحيح. | تأكد من أن `setPageWidth`/`setPageHeight` قيمهما موجبة وأن `setLayouts` يطابق اسم تخطيط DWG. |
| **استثناء الترخيص** | تشغيل بدون ترخيص Aspose.CAD صالح. | قم بتطبيق ترخيص مؤقت أو مدفوع قبل استدعاء أي من طرق API. |

## الأسئلة المتكررة

### س1: أين يمكنني العثور على وثائق Aspose.CAD للـ Java؟

ج1: يمكن العثور على الوثائق [هنا](https://reference.aspose.com/cad/java/).

### س2: كيف يمكنني تحميل مكتبة Aspose.CAD للـ Java؟

ج2: يمكنك تحميل المكتبة من [هذا الرابط](https://releases.aspose.com/cad/java/).

### س3: هل تتوفر نسخة تجريبية مجانية لـ Aspose.CAD للـ Java؟

ج3: نعم، يمكنك العثور على النسخة التجريبية [هنا](https://releases.aspose.com/).

### س4: أين يمكنني الحصول على ترخيص مؤقت لـ Aspose.CAD للـ Java؟

ج4: احصل على ترخيص مؤقت [هنا](https://purchase.aspose.com/temporary-license/).

### س5: هل تحتاج إلى مساعدة أو لديك أسئلة؟

ج5: زر منتدى دعم مجتمع Aspose.CAD [هنا](https://forum.aspose.com/c/cad/19).

### س6: هل يمكنني تحويل PDF الناتج مرة أخرى إلى DWG؟

ج6: الـ PDF هو معاينة نقطية؛ تحويله مرة أخرى إلى DWG يتطلب أداة هندسة عكسية منفصلة.

### س7: هل يعمل هذا النهج مع صيغ CAD أخرى مثل DWF أو DXF؟

ج7: نعم، يدعم Aspose.CAD العديد من الصيغ؛ كل ما عليك هو تعديل امتدادات الملفات وإعدادات الترصيص وفقًا لذلك.

---

**آخر تحديث:** 2026-01-10  
**تم الاختبار مع:** Aspose.CAD للـ Java 24.11  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}