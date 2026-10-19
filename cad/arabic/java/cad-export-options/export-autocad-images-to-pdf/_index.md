---
date: 2026-10-19
description: تعلم كيفية تصدير رسومات AutoCAD إلى PDF بحجم صفحة PDF مخصص باستخدام Aspose.CAD
  for Java. يغطي هذا الدليل خطوة بخطوة تحويل DWG إلى PDF، خيارات rasterization، والترخيص.
keywords:
- custom pdf page size
- export autocad to pdf
- save cad as pdf
- generate pdf from dwg
- dwg to pdf java
lastmod: 2026-10-19
linktitle: تصدير صور AutoCAD إلى PDF
og_description: تعيين حجم صفحة PDF مخصص عند تصدير رسومات AutoCAD إلى PDF باستخدام
  Aspose.CAD for Java. تعلم تحويل DWG إلى PDF، إعدادات rasterization، والترخيص في
  دقائق.
og_image_alt: Guide showing how to export AutoCAD drawings to PDF with custom page
  dimensions using Aspose.CAD for Java
og_title: تعيين حجم صفحة PDF مخصص لتصدير AutoCAD باستخدام Aspose.CAD
schemas:
- author: Aspose
  dateModified: '2026-10-19'
  description: Learn how to export AutoCAD drawings to PDF with a custom PDF page
    size using Aspose.CAD for Java. This step‑by‑step guide covers converting DWG
    to PDF, rasterization options, and licensing.
  headline: Set custom PDF page size for AutoCAD export with Aspose.CAD
  type: TechArticle
- description: Learn how to export AutoCAD drawings to PDF with a custom PDF page
    size using Aspose.CAD for Java. This step‑by‑step guide covers converting DWG
    to PDF, rasterization options, and licensing.
  name: Set custom PDF page size for AutoCAD export with Aspose.CAD
  steps:
  - name: set the resource directory path
    text: '> **Pro tip:** Replace `"Your Document Directory"` with the absolute path
      to the folder you created in the prerequisites.'
  - name: load the CAD image
    text: The `Image` class loads the CAD file and gives you access to Aspose.CAD’s
      rasterization engine. > **Why this matters:** Once the CAD file is loaded, you
      can manipulate rasterization options before rendering to PDF.
  - name: set rasterization options
    text: The `CadRasterizationOptions` class specifies how the CAD drawing is rasterized
      before being saved as PDF. Adjust `pageWidth` and `pageHeight` to define a **custom
      PDF page size**. You can also enable 3‑D rendering by uncommenting the `setTypeOfEntities`
      line. - `pageWidth` / `pageHeight` – measured
  - name: configure PDF options
    text: The `PdfOptions` class holds PDF‑specific settings and links the rasterization
      options to the output file, ensuring the custom page dimensions are applied
      correctly.
  - name: save the PDF
    text: The `save` method writes the rendered image to the specified PDF file. The
      resulting file, `Export3DImagestoPDF_out_.pdf`, is a **save cad as pdf** representation
      of your original AutoCAD drawing with the exact page dimensions you specified.
  type: HowTo
- questions:
  - answer: Yes, the library supports DWG, DXF, DWF, DGN, and many more, giving you
      flexibility across projects.
    question: Can I use Aspose.CAD for Java with other CAD file formats?
  - answer: Visit the [temporary license page](https://purchase.aspose.com/temporary-license/)
      to request a time‑limited license for evaluation.
    question: How do I obtain a temporary license for Aspose.CAD for Java?
  - answer: Absolutely. Use `setLayouts("Model")` or specify other layout names to
      control which view is rendered.
    question: Are there layout options for rasterization?
  - answer: Yes – modify `pageWidth` and `pageHeight` in the rasterization options
      to any dimensions you need.
    question: Can I customize the size of the output PDF file?
  - answer: The dedicated [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) offers
      community support and official responses from the Aspose team.
    question: Where can I get help or discuss issues related to Aspose.CAD for Java?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- custom pdf page size
- Aspose.CAD
- Java CAD conversion
- PDF generation
- DWG export
title: تعيين حجم صفحة PDF مخصص لتصدير AutoCAD باستخدام Aspose.CAD
url: /ar/java/cad-export-options/export-autocad-images-to-pdf/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تصدير AutoCAD PDF - تصدير صور AutoCAD إلى PDF باستخدام Aspose.CAD للـ Java

## المقدمة

إذا كنت بحاجة إلى **تحويل DWG إلى PDF** والتحكم في الأبعاد الدقيقة للملف الناتج، فقد وصلت إلى المكان الصحيح. يوضح هذا البرنامج التعليمي كيفية تعيين **حجم صفحة PDF مخصص** أثناء تصدير صور AutoCAD إلى PDF باستخدام Aspose.CAD للـ Java. في نهاية الدليل ستعرف كيفية تحميل ملف DWG، تكوين خيارات الرستر مثل DPI وعرض/ارتفاع الصفحة، تطبيق الترخيص، وإنشاء PDF جاهز للإنتاج.

## إجابات سريعة
- **هل يمكنني تحويل DWG إلى PDF باستخدام Java؟** نعم – Aspose.CAD للـ Java يدعم أصلاً DWG، DXF، DWF والعديد من صيغ CAD الأخرى.  
- **هل أحتاج إلى ترخيص للاستخدام الإنتاجي؟** الترخيص الكامل لـ Aspose.CAD يزيل جميع حدود التقييم؛ ترخيص مؤقت متاح للاختبار.  
- **ما إصدارات Java المتوافقة؟** المكتبة تعمل مع Java 8 وأي JDK أحدث.  
- **كيف أغير أبعاد صفحة PDF؟** اضبط `pageWidth` و `pageHeight` على `PdfOptions.getRasterizationOptions()` إلى أي حجم تحتاجه.  
- **هل يدعم التصيير ثلاثي الأبعاد؟** نعم – فعّل `TypeOfEntities.Entities3D` لتص rasterize الكيانات ثلاثية الأبعاد.

## ما هو تصدير AutoCAD PDF؟
يعني تصدير AutoCAD PDF تحويل رسومات CAD القائمة على المتجهات (DWG، DXF، DWF، إلخ) إلى مستند PDF محمول مع الحفاظ على الطبقات، وزن الخطوط، والهندسة ثلاثية الأبعاد الاختيارية. يتيح لك ذلك مشاركة التصاميم مع العملاء، أرشفة الرسومات، أو الطباعة دون الحاجة إلى تثبيت برنامج CAD.

## لماذا تستخدم Aspose.CAD للـ Java لتحويل DWG إلى PDF؟
Aspose.CAD للـ Java مثالي لتحويل DWG إلى PDF لأنه يقدم دعمًا واسعًا للصيغ، يعمل على Java النقي دون تبعيات أصلية، يوفر تصييرًا عالي الدقة مع تحكم كامل في DPI وحجم الصفحة، ويتضمن ترخيصًا مرنًا يتيح لك البدء بتجربة مجانية ثم الترقية للإنتاج.

- **تغطية صيغ واسعة** – يدعم أكثر من 50 صيغة إدخال وإخراج، بما في ذلك DWG، DXF، DWF، DGN، وPDF.  
- **تنفيذ Java نقي** – لا توجد DLLs أصلية أو تبعيات خارجية، لذا يكون النشر بسيطًا على أي منصة.  
- **تصيير عالي الدقة** – يمكنك تحديد DPI، حجم الصفحة، وتخطيط الصفحة، مما يمنحك تحكمًا كاملاً في **حجم صفحة PDF المخصص** للنتيجة.  
- **ترخيص قابل للتوسع** – ابدأ بتجربة مجانية، ثم ارتقِ إلى **ترخيص Aspose CAD** دائم.  

## المتطلبات المسبقة

- **Java Development Kit** – JDK 8 أو أحدث مثبت على جهازك.  
- **Aspose.CAD للـ Java** – حمّل أحدث ملف JAR من [رابط التحميل](https://releases.aspose.com/cad/java/).  
- **دليل العمل** – مجلد يحتوي على ملفات DWG المصدرية وسيستقبل ملفات PDF المولدة.

## استيراد مساحات الأسماء

فئة `Image` هي الكائن الأساسي في Aspose.CAD الذي يمثل رسم CAD في الذاكرة. استورد الحزم المطلوبة قبل بدء الترميز.

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
//import com.aspose.cad.imageoptions.TypeOfEntities;
```

الآن دعنا نستعرض الشيفرة خطوةً بخطوة.

## كيفية تعيين حجم صفحة PDF مخصص عند تصدير DWG إلى PDF؟

حمّل ملف DWG الخاص بك، عرّف عرض وارتفاع الصفحة المطلوبين، ثم احفظ النتيجة كملف PDF – هذا كل ما تحتاجه لإنشاء PDF بحجم صفحة مخصص. الخطوات التالية توضح التسلسل الدقيق وأقل كمية من الشيفرة المطلوبة.

### الخطوة 1: تعيين مسار دليل الموارد

```java
String dataDir = "Your Document Directory" + "ExportingCAD/";
```

> **نصيحة احترافية:** استبدل `"Your Document Directory"` بالمسار المطلق للمجلد الذي أنشأته في المتطلبات المسبقة.

### الخطوة 2: تحميل صورة CAD

فئة `Image` تقوم بتحميل ملف CAD وتمنحك الوصول إلى محرك الرستر الخاص بـ Aspose.CAD.

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image cadImage = Image.load(srcFile);
```

> **لماذا هذا مهم:** بمجرد تحميل ملف CAD، يمكنك تعديل خيارات الرستر قبل التصيير إلى PDF.

### الخطوة 3: تعيين خيارات الرستر

فئة `CadRasterizationOptions` تحدد كيفية رستر رسم CAD قبل حفظه كملف PDF. اضبط `pageWidth` و `pageHeight` لتحديد **حجم صفحة PDF مخصص**. يمكنك أيضًا تمكين التصيير ثلاثي الأبعاد بإلغاء تعليق سطر `setTypeOfEntities`.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(500);
rasterizationOptions.setPageHeight(500);
// rasterizationOptions.setTypeOfEntities(TypeOfEntities.Entities3D);

rasterizationOptions.setLayouts(new String[] {"Model"});
```

- `pageWidth` / `pageHeight` – تُقاس بالبكسل؛ غيّر هذه القيم لتتناسب مع A4 أو Letter أو أي أبعاد مخصصة.  
- `setTypeOfEntities(TypeOfEntities.Entities3D)` – يصيّر الكيانات ثلاثية الأبعاد عند الحاجة.  
- `setLayouts` – يحدد أي تخطيط (Model، Layout1، إلخ) سيتم رسترته.

### الخطوة 4: تكوين خيارات PDF

فئة `PdfOptions` تحتفظ بإعدادات خاصة بـ PDF وتربط خيارات الرستر بملف الإخراج، مما يضمن تطبيق أبعاد الصفحة المخصصة بشكل صحيح.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### الخطوة 5: حفظ PDF

طريقة `save` تكتب الصورة المصورة إلى ملف PDF المحدد.

```java
cadImage.save(dataDir + "Export3DImagestoPDF_out_.pdf", pdfOptions);
```

الملف الناتج، `Export3DImagestoPDF_out_.pdf`، هو تمثيل **save cad as pdf** لرسم AutoCAD الأصلي مع أبعاد الصفحة الدقيقة التي حددتها.

## المشكلات الشائعة والحلول

| العَرَض | السبب المحتمل | الحل |
|---------|--------------|-----|
| مخرجات PDF فارغة | لم يتم تعيين خيارات الرستر أو عدم تطابق التخطيط | تحقق من أن `setLayouts` يطابق اسم التخطيط في ملف CAD الخاص بك. |
| صورة منخفضة الدقة | `pageWidth`/`pageHeight` صغيرة جدًا أو DPI منخفض | زد الأبعاد أو استدعِ `rasterizationOptions.setResolution(...)` بدقة أعلى. |
| استثناء الترخيص | لم يتم تطبيق ترخيص صالح | طبّق ترخيص Aspose.CAD دائم أو استخدم ترخيصًا مؤقتًا للاختبار. |

## الأسئلة المتكررة

**س: هل يمكنني استخدام Aspose.CAD للـ Java مع صيغ CAD أخرى؟**  
ج: نعم، المكتبة تدعم DWG، DXF، DWF، DGN، والعديد غيرها، ما يمنحك مرونة عبر المشاريع.

**س: كيف أحصل على ترخيص مؤقت لـ Aspose.CAD للـ Java؟**  
ج: زر [صفحة الترخيص المؤقت](https://purchase.aspose.com/temporary-license/) لطلب ترخيص محدود الوقت للتقييم.

**س: هل هناك خيارات تخطيط للرستر؟**  
ج: بالتأكيد. استخدم `setLayouts("Model")` أو حدد أسماء تخطيطات أخرى للتحكم في العرض الذي يتم رسترته.

**س: هل يمكنني تخصيص حجم ملف PDF الناتج؟**  
ج: نعم – عدّل `pageWidth` و `pageHeight` في خيارات الرستر إلى أي أبعاد تحتاجها.

**س: أين يمكنني الحصول على مساعدة أو مناقشة المشكلات المتعلقة بـ Aspose.CAD للـ Java؟**  
ج: المنتدى المخصص لـ [Aspose.CAD](https://forum.aspose.com/c/cad/19) يقدم دعمًا من المجتمع وردودًا رسمية من فريق Aspose.

## أسئلة إضافية (صيغة صديقة للذكاء الاصطناعي)

**س: هل يتطلب Aspose.CAD أي مكتبات أصلية على Windows أو Linux؟**  
ج: لا. Aspose.CAD للـ Java مكتبة Java نقيّة، لذا تعمل على أي منصة تدعم JDK دون الحاجة إلى DLLs أصلية إضافية.

**س: ما أقصى حجم ملف DWG يمكن للمكتبة معالجته؟**  
ج: يمكن للمكتبة معالجة رسومات مئات الصفحات (حتى 500 ميغابايت) دون تحميل الملف بالكامل في الذاكرة، بفضل بنية البث الخاصة بها.

**س: هل يمكن تحويل مجموعة كبيرة من ملفات DWG إلى PDF في تشغيل واحد؟**  
ج: نعم. يمكنك التكرار عبر دليل، تحميل كل ملف باستخدام `Image.load()`، تطبيق نفس خيارات الرستر، ثم استدعاء `save()` لكل PDF ناتج.

**س: ما الأداء المتوقع على خادم نموذجي؟**  
ج: تحويل DWG مكوّن من 100 صفحة بدقة 300 DPI على معالج 2.5 GHz يستغرق تقريبًا 12 ثانية، وفقًا لاختبارات Aspose.

**س: هل تحافظ المكتبة على معلومات الطبقات في PDF؟**  
ج: رغم أن المخرجات رسترية، إلا أن المظهر البصري للطبقات، وزن الخطوط، والألوان يُعاد إنتاجه بدقة.

---

**آخر تحديث:** 2026-10-19  
**تم الاختبار مع:** Aspose.CAD للـ Java 24.10  
**المؤلف:** Aspose

## دروس ذات صلة

- [Export DWG to PDF and Enable Tracking with Aspose.CAD Java](/cad/java/additional-features/enable-tracking/)
- [Export DWG to PDF: Specific Layout Using Aspose.CAD Java](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)
- [Export DWG to BMP and Adjust CAD Size Using Unit Type with Aspose.CAD for Java](/cad/java/cad-file-manipulation/adjusting-cad-drawing-size-using-unit-type/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}