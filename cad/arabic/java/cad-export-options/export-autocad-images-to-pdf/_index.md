---
date: 2026-10-19
description: تعلم كيفية تحويل DWG إلى PDF في Java باستخدام Aspose.CAD. يوضح لك هذا
  الدليل خطوة بخطوة كيفية تصدير AutoCAD PDF، حفظ CAD كـ PDF، وتطبيق الترخيص.
keywords:
- dwg to pdf java
- export autocad pdf
- java pdf export library
- aspose cad license
- save cad pdf
- customize pdf page size
lastmod: 2026-10-19
linktitle: تصدير صور AutoCAD إلى PDF
og_description: تعلم كيفية تحويل DWG إلى PDF في Java باستخدام Aspose.CAD. يرافقك هذا
  الدليل في عملية تصدير AutoCAD PDF، حفظ CAD كـ PDF، وإدارة الترخيص.
og_image_alt: 'Tutorial: convert DWG to PDF in Java with Aspose.CAD'
og_title: تحويل DWG إلى PDF في Java باستخدام Aspose.CAD
schemas:
- author: Aspose
  dateModified: '2026-10-19'
  description: Learn how to convert DWG to PDF in Java with Aspose.CAD. This step‑by‑step
    guide shows you how to export AutoCAD PDF, save CAD as PDF, and apply a license.
  headline: Convert DWG to PDF in Java using Aspose.CAD
  type: TechArticle
- description: Learn how to convert DWG to PDF in Java with Aspose.CAD. This step‑by‑step
    guide shows you how to export AutoCAD PDF, save CAD as PDF, and apply a license.
  name: Convert DWG to PDF in Java using Aspose.CAD
  steps:
  - name: set the resource directory path
    text: Replace `"Your Document Directory"` with the absolute path to the folder
      you created in the prerequisites. > **Pro tip:** Use `Paths.get(...).toAbsolutePath()`
      to avoid path‑related errors on different operating systems.
  - name: load the CAD image
    text: Loading the CAD file into an `Image` object gives you full access to Aspose.CAD’s
      rasterization engine. The `Image` class loads the DWG file and prepares it for
      conversion. > **Why this matters:** Once the drawing is in memory, you can query
      its layouts, layers, and metadata before rasterizing.
  - name: set rasterization options
    text: Adjust `pageWidth` and `pageHeight` to **customize PDF page size**. Enabling
      `setTypeOfEntities(TypeOfEntities.Entities3D)` allows full 3‑D rendering when
      needed. The `RasterizationOptions` object controls DPI, page dimensions, and
      entity types for the output. - `pageWidth` / `pageHeight` are measur
  - name: configure PDF options
    text: Tie the rasterization settings to the PDF output, ensuring the vector data
      is correctly transformed. The `PdfOptions` class links the rasterization configuration
      with the final PDF file.
  - name: save the PDF
    text: The resulting file, `Export3DImagestoPDF_out_.pdf`, is a **save cad as pdf**
      representation of your original AutoCAD drawing. The `save` method writes the
      rasterized image to a PDF file on disk.
  type: HowTo
- questions:
  - answer: Yes – the library supports DWG, DXF, DWF, DGN, and over 30 additional
      formats, giving you flexibility across projects.
    question: Can I use Aspose.CAD for Java with other CAD file formats?
  - answer: Visit the [temporary license page](https://purchase.aspose.com/temporary-license/)
      to request a time‑limited license for evaluation.
    question: How do I obtain a temporary license for Aspose.CAD for Java?
  - answer: Absolutely. Use `setLayouts("Model")`, `setLayouts("Layout1")`, etc.,
      to choose which view is rendered into the PDF.
    question: Are there layout options for rasterization?
  - answer: Yes – modify `pageWidth` and `pageHeight` in the rasterization options
      to match any required page dimensions.
    question: Can I change the size of the output PDF file?
  - answer: The dedicated community is available at the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19)
      where you can ask questions and share solutions.
    question: Where can I get help if I run into problems?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- dwg to pdf
- aspose.cad
- java cad conversion
- export autocad pdf
title: تحويل DWG إلى PDF في Java باستخدام Aspose.CAD
url: /ar/java/cad-export-options/export-autocad-images-to-pdf/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تصدير AutoCAD PDF – تصدير صور AutoCAD إلى PDF باستخدام Aspose.CAD للـ Java

## مقدمة

إذا كنت بحاجة إلى **تحويل DWG إلى PDF في Java**، فأنت في المكان الصحيح. يوضح هذا الدرس كيفية تصدير صور AutoCAD إلى PDF باستخدام Aspose.CAD للـ Java، مكتبة Java صافية تتعامل مع صيغ DWG وDXF وDWF والعديد من صيغ CAD الأخرى دون تبعيات أصلية. في النهاية ستتمكن من **حفظ CAD كملف PDF**، تعديل خيارات الرستر مثل حجم الصفحة، وتطبيق **ترخيص Aspose CAD** بشكل صحيح للاستخدام الإنتاجي.

## إجابات سريعة
- **هل يمكنني تحويل DWG إلى PDF باستخدام Java؟** نعم – Aspose.CAD للـ Java يدعم بشكل أصلي DWG وDXF والعديد من صيغ CAD الأخرى.  
- **هل أحتاج إلى ترخيص؟** ترخيص **Aspose CAD** الدائم يزيل جميع قيود التقييم؛ ترخيص مؤقت متاح للاختبار.  
- **ما إصدارات Java المدعومة؟** Java 8 وما فوق مدعومة بالكامل.  
- **هل يمكنني التحكم في أبعاد صفحة PDF؟** بالتأكيد – قم بتعيين `pageWidth` و `pageHeight` في خيارات الرستر.  
- **هل يمكن تنفيذ التصيير ثلاثي الأبعاد؟** نعم – فعّل `TypeOfEntities.Entities3D` لترصيص الكيانات ثلاثية الأبعاد.

## ما هو تصدير AutoCAD إلى PDF؟
تصدير AutoCAD PDF هو عملية تحويل رسومات CAD المتجهة إلى مستند PDF محمول. يحافظ على الطبقات، وزن الخطوط، الألوان، وبشكل اختياري الهندسة ثلاثية الأبعاد، مما يسهل مشاركة التصاميم مع العملاء أو أرشفتها دون الحاجة إلى برنامج CAD.

## لماذا تحويل DWG إلى PDF باستخدام Aspose.CAD للـ Java؟
يدعم Aspose.CAD **أكثر من 50 صيغة إدخال وإخراج**، يعالج رسومات مئات الصفحات دون تحميل الملف بالكامل في الذاكرة، ويعمل على أي منصة تدعم Java 8+. تمنحك المكتبة تحكمًا كاملاً في DPI، حجم الصفحة، وتخطيطها، بحيث يمكنك **تخصيص حجم صفحة PDF** ليتطابق مع مواصفات المشروع الدقيقة، كل ذلك دون الحاجة لتثبيت ملفات DLL أصلية.

## المتطلبات المسبقة

- **مجموعة تطوير Java** – JDK 8 أو أحدث مثبت على جهازك.  
- **Aspose.CAD للـ Java** – قم بتحميل أحدث JAR من [رابط التحميل](https://releases.aspose.com/cad/java/).  
- **دليل العمل** – مجلد حيث سيتم تخزين ملفات DWG المصدرية وملفات PDF المولدة.

## استيراد مساحات الأسماء

تمثل فئة `Image` أي رسم CAD يمكن رسترته، بينما تسمح `RasterizationOptions` و `PdfOptions` بضبط التحويل بدقة.

فئة `Image` هي الكائن الأعلى مستوى في Aspose.CAD الذي يحتفظ برسم CAD في الذاكرة.  
فئة `RasterizationOptions` تحدد كيفية رستر البيانات المتجهة قبل كتابتها إلى PDF.  
فئة `PdfOptions` تجمع إعدادات الرستر مع معلمات الإخراج الخاصة بـ PDF.

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
//import com.aspose.cad.imageoptions.TypeOfEntities;
```

الآن دعنا نستعرض الكود خطوة بخطوة.

## كيفية تحويل DWG إلى PDF باستخدام Aspose.CAD للـ Java؟

لتحويل ملف DWG إلى PDF باستخدام Aspose.CAD للـ Java، قم بتحميل الرسم باستخدام فئة Image، اضبط CadRasterizationOptions (مثل DPI، حجم الصفحة، وأنواع الكيانات)، احزم هذه الخيارات في PdfOptions، ثم استدعِ طريقة الحفظ مع تحديد اسم ملف .pdf. يضمن هذا التسلسل رستر البيانات المتجهة بشكل صحيح وتطابق PDF الناتج مع متطلبات التخطيط الخاصة بك.

### الخطوة 1: تعيين مسار دليل الموارد

استبدل `"Your Document Directory"` بالمسار المطلق للمجلد الذي أنشأته في المتطلبات المسبقة.

```java
String dataDir = "Your Document Directory" + "ExportingCAD/";
```

> **نصيحة احترافية:** استخدم `Paths.get(...).toAbsolutePath()` لتجنب الأخطاء المتعلقة بالمسارات على أنظمة تشغيل مختلفة.

### الخطوة 2: تحميل صورة CAD

تحميل ملف CAD إلى كائن `Image` يمنحك وصولًا كاملًا إلى محرك رستر Aspose.CAD.

فئة `Image` تقوم بتحميل ملف DWG وتجهزه للتحويل.

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image cadImage = Image.load(srcFile);
```

> **لماذا هذا مهم:** بمجرد تحميل الرسم في الذاكرة، يمكنك استعلام عن تخطيطاتها، طبقاتها، والبيانات الوصفية قبل الرستر.

### الخطوة 3: تعيين خيارات الرستر

قم بتعديل `pageWidth` و `pageHeight` لت **تخصيص حجم صفحة PDF**. تمكين `setTypeOfEntities(TypeOfEntities.Entities3D)` يسمح بالرستر الكامل ثلاثي الأبعاد عند الحاجة.

كائن `RasterizationOptions` يتحكم في DPI، أبعاد الصفحة، وأنواع الكيانات للإخراج.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(500);
rasterizationOptions.setPageHeight(500);
// rasterizationOptions.setTypeOfEntities(TypeOfEntities.Entities3D);

rasterizationOptions.setLayouts(new String[] {"Model"});
```

- `pageWidth` / `pageHeight` تُقاس بالنقاط (1 pt = 1/72 in).  
- ألغِ التعليق عن سطر `setTypeOfEntities` لتصوير ثلاثي الأبعاد.  
- `setLayouts` يحدد أي تخطيط (Model، Layout1، إلخ) سيتم تصييره.

### الخطوة 4: تكوين خيارات PDF

ربط إعدادات الرستر بإخراج PDF، لضمان تحويل البيانات المتجهة بشكل صحيح.

فئة `PdfOptions` تربط تكوين الرستر بملف PDF النهائي.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### الخطوة 5: حفظ PDF

الملف الناتج، `Export3DImagestoPDF_out_.pdf`، هو تمثيل **حفظ CAD كملف PDF** للرسم الأصلي في AutoCAD.

طريقة `save` تكتب الصورة المرسرة إلى ملف PDF على القرص.

```java
cadImage.save(dataDir + "Export3DImagestoPDF_out_.pdf", pdfOptions);
```

## المشكلات الشائعة والحلول

| العَرَض | السبب المحتمل | الحل |
|---------|--------------|-----|
| مخرجات PDF فارغة | خيارات الرستر غير مضبوطة أو عدم تطابق التخطيط | تحقق من أن `setLayouts` يطابق اسم التخطيط في ملف CAD الخاص بك. |
| صورة منخفضة الدقة | `pageWidth`/`pageHeight` صغيرة جدًا | زد الأبعاد أو اضبط DPI أعلى عبر `rasterizationOptions.setResolution(...)`. |
| استثناء الترخيص | لم يتم تطبيق ترخيص صالح | قم بتطبيق **ترخيص Aspose CAD** أو استخدم ترخيصًا مؤقتًا للاختبار. |

## الأسئلة المتكررة

**س: هل يمكنني استخدام Aspose.CAD للـ Java مع صيغ CAD أخرى؟**  
ج: نعم – المكتبة تدعم DWG، DXF، DWF، DGN، وأكثر من 30 صيغة إضافية، مما يمنحك مرونة عبر المشاريع.

**س: كيف أحصل على ترخيص مؤقت لـ Aspose.CAD للـ Java؟**  
ج: زر [صفحة الترخيص المؤقت](https://purchase.aspose.com/temporary-license/) لطلب ترخيص محدود الوقت للتقييم.

**س: هل هناك خيارات تخطيط للرستر؟**  
ج: بالتأكيد. استخدم `setLayouts("Model")`، `setLayouts("Layout1")`، إلخ، لاختيار العرض الذي سيُصَدر إلى PDF.

**س: هل يمكنني تغيير حجم ملف PDF الناتج؟**  
ج: نعم – عدّل `pageWidth` و `pageHeight` في خيارات الرستر لتتناسب مع أي أبعاد صفحة مطلوبة.

**س: أين يمكنني الحصول على مساعدة إذا واجهت مشاكل؟**  
ج: المجتمع المخصص متاح في [منتدى Aspose.CAD](https://forum.aspose.com/c/cad/19) حيث يمكنك طرح الأسئلة ومشاركة الحلول.

**آخر تحديث:** 2026-10-19  
**تم الاختبار مع:** Aspose.CAD للـ Java 24.10  
**المؤلف:** Aspose

## دروس ذات صلة

- [تصدير DWG إلى PDF في Java – ضبط حجم صفحة PDF باستخدام Aspose.CAD](/cad/java/cad-export-options/export-to-pdf/)
- [تصدير DWG إلى PDF: تخطيط محدد باستخدام Aspose.CAD للـ Java](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)
- [تصدير DWG إلى PDF وتمكين التتبع باستخدام Aspose.CAD Java](/cad/java/additional-features/enable-tracking/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}