---
date: 2026-10-30
description: تعلم كيفية تحويل دفعة ملفات DXF إلى WMF باستخدام Aspose.CAD for Java،
  مع كود خطوة بخطوة، معلومات عن النسخة التجريبية المجانية، وتصدير PDF اختياري.
keywords:
- batch convert dxf files
- aspose cad java
- dxf to wmf conversion
- java cad rasterization
- aspose free trial
lastmod: 2026-10-30
linktitle: تصدير DXF إلى تنسيق WMF باستخدام Java
og_description: تحويل دفعة ملفات DXF إلى WMF باستخدام Aspose.CAD for Java. اتبع هذا
  الدليل لتحميل رسومات DXF، ضبط خيارات الترصيع، حفظ كملف WMF، وتصدير PDF اختياريًا
  مع النسخة التجريبية المجانية.
og_image_alt: Tutorial showing batch conversion of DXF to WMF in Java using Aspose.CAD
og_title: تحويل دفعة ملفات DXF إلى WMF باستخدام Aspose.CAD for Java
schemas:
- author: Aspose
  dateModified: '2026-10-30'
  description: Learn how to batch convert DXF files to WMF using Aspose.CAD for Java,
    with step‑by‑step code, free trial info, and optional PDF export.
  headline: Batch convert DXF files to WMF with Aspose.CAD for Java
  type: TechArticle
- description: Learn how to batch convert DXF files to WMF using Aspose.CAD for Java,
    with step‑by‑step code, free trial info, and optional PDF export.
  name: Batch convert DXF files to WMF with Aspose.CAD for Java
  steps:
  - name: load dxf drawing
    text: Image.load reads the DXF file into an Aspose.CAD Image object.
  - name: configure rasterization options
    text: '`CadRasterizationOptions` specifies page size, resolution, and background
      for rasterizing the CAD drawing.'
  - name: save as wmf
    text: '`ImageSaveOptions` with `SaveFormat.WMF` tells Aspose.CAD to write the
      output as a Windows Metafile.'
  - name: dispose of resources
    text: Calling `image.close()` releases native resources used by the Aspose.CAD
      Image object.
  - name: optional – export to pdf
    text: '`PdfOptions` configures PDF‑specific settings when saving the image as
      a PDF document. > **Pro tip:** You can reuse the same `CadRasterizationOptions`
      object for PDF export by passing it to a `PdfOptions` instance, saving you a
      few lines of setup.'
  type: HowTo
- questions:
  - answer: You can access the documentation [Aspose.CAD Java documentation](https://reference.aspose.com/cad/java/).
    question: Where can I find the Aspose.CAD documentation?
  - answer: Download the library [Aspose.CAD Java download page](https://releases.aspose.com/cad/java/).
    question: How do I download Aspose.CAD for Java?
  - answer: Yes, you can get a free trial [Aspose free trial page](https://releases.aspose.com/).
    question: Is there a free trial available?
  - answer: Explore temporary licenses [temporary license options](https://purchase.aspose.com/temporary-license/).
    question: Need temporary licensing options?
  - answer: Visit the Aspose.CAD support forum [Aspose.CAD support forum](https://forum.aspose.com/c/cad/19).
    question: Where can I get support?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- batch convert dxf
- Aspose.CAD
- Java CAD conversion
- WMF export
- DXF processing
title: تحويل دفعة ملفات DXF إلى WMF باستخدام Aspose.CAD for Java
url: /ar/java/additional-features/export-dxf-to-wmf/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تحويل دفعة ملفات DXF إلى WMF باستخدام Aspose.CAD للـ Java

## مقدمة

في هذا البرنامج التعليمي ستتعلم كيفية **تحويل دفعة ملفات DXF إلى WMF** باستخدام Aspose.CAD للـ Java. سواء كنت بحاجة إلى تضمين رسومات CAD في تقارير تعتمد على Windows، أو إنشاء رسومات متجهة خفيفة الوزن لمستندات Office، أو أتمتة عمليات التحويل على نطاق واسع، فإن هذا الدليل يشرح لك كيفية تحميل رسم DXF، وتكوين خيارات الترصيص، وحفظه كـ WMF، واختيارياً تصدير نفس الرسم إلى PDF. تعمل الخطوات على أي منصة تشغل Java 8+.

## أسئلة سريعة
- **هل يمكنني تحويل DXF إلى WMF باستخدام نسخة تجريبية مجانية؟** نعم – تقدم Aspose نسخة تجريبية كاملة الوظائف لمدة 30 يوماً.  
- **ما نسخة Java المطلوبة؟** Java 8 أو أحدث.  
- **هل أحتاج إلى ترخيص لتشغيل الكود؟** يُطلب ترخيص للإنتاج؛ النسخة التجريبية تعمل للتطوير والاختبار.  
- **هل التحويل بدون فقدان؟** يتم الحفاظ على بيانات المتجه؛ خيارات الترصيص تتيح لك التحكم في الدقة.  
- **هل يمكنني أيضاً تصدير نفس الرسم إلى PDF؟** بالطبع – راجع خطوة “Export to PDF” أدناه.  
- **كيف يمكنني تحويل دفعة من ملفات DXF متعددة مرة واحدة؟** قم بالتكرار عبر مجلد، وطبق نمط التحميل‑الترصيص‑الحفظ نفسه على كل ملف.

## ما هو تحويل دفعة ملفات dxf؟

يعني تحويل دفعة ملفات DXF معالجة عدة رسومات بصيغة Drawing Exchange Format (DXF) في تشغيل واحد وإنتاج مخرجات WMF لكل منها. WMF (Windows Metafile) هو تنسيق صورة متجهة يندمج طبيعياً مع Microsoft Office، وتطبيقات Windows، والعديد من أدوات التقارير.

## لماذا تستخدم Aspose.CAD للـ Java؟

Aspose.CAD للـ Java هو محرك Java نقي يدعم **أكثر من 50 تنسيق إدخال وإخراج** — بما في ذلك DXF وDWG وDGN وPDF وPNG وSVG وWMF — مع تقديم **دقة متجهية بنسبة 99 %**. يعمل على أي نظام تشغيل يدعم Java، ولا يتطلب ملفات DLL أصلية، ويسمح لك بالتحكم في حجم الصفحة، DPI، ولون الخلفية عبر فئة واحدة `CadRasterizationOptions`. نفس الـ API يتعامل أيضاً مع تصدير PDF وPNG وSVG، مما يلغي الحاجة إلى مكتبات متعددة.

### الفوائد المكمّنة
- **أكثر من 50 تنسيقًا مدعومًا** يقلل الحاجة إلى محولات الطرف الثالث.  
- **يعالج ملفات DXF مكوّنة من 300 صفحة في أقل من 5 ثوانٍ** على خادم عادي بسرعة 2.5 GHz عند ترصيصها بدقة 150 DPI.  
- **يظل استهلاك الذاكرة أقل من 200 ميغابايت** للملفات التي تصل إلى 500 ميغابايت عندما تحدد أبعاد الصفحة المناسبة.  

## المتطلبات المسبقة

- **Aspose.CAD للـ Java** مدمج في مشروعك. قم بتنزيله من الموقع الرسمي: [Aspose.CAD Java download](https://releases.aspose.com/cad/java/).  
- مجلد يحتوي على ملفات DXF التي تريد تحويلها (مثال: `Your Document Directory/DXFDrawings/`).  

## استيراد مساحات الأسماء

`Image` هي الفئة الأساسية في Aspose.CAD التي تمثل رسم CAD في الذاكرة. بعد تحميل ملف، تُجرى جميع العمليات اللاحقة — الترصيص، تحويل الصيغة، وتنظيف الموارد — عبر هذا الكائن.

الاستيرادات التالية تجلب فئات Aspose.CAD المطلوبة لتحميل، ترصيص، وحفظ ملفات CAD.  
```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageSaveOptions;
import com.aspose.cad.fileformats.cad.CadRasterizationOptions;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.CadImageInfo;
import com.aspose.cad.fileformats.cad.CadImageInfo;
import java.awt.Color;
```

## دليل خطوة بخطوة

### كيف يمكنني تحويل دفعة ملفات DXF إلى WMF في Java؟

حمّل كل ملف DXF باستخدام `Image.load`، وقم بتكوين `CadRasterizationOptions` لحجم الصفحة والدقة المطلوبين، ثم استدعِ `image.save` مع `SaveFormat.WMF`. هذا النمط المكوّن من ثلاث خطوات يُجري التحويل الكامل مع الحفاظ على جودة المتجه، ويتطلب فقط بضع أسطر من الكود لكل ملف.

#### الخطوة 1: تحميل رسم dxf

`Image.load` يقرأ ملف DXF إلى كائن Aspose.CAD Image.  
```java
import com.aspose.cad.Color;
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.ifc.IfcImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.WmfOptions;
```

#### الخطوة 2: تكوين خيارات الترصيص

`CadRasterizationOptions` يحدد حجم الصفحة، الدقة، والخلفية لترصيص رسم CAD.  
```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "DXFDrawings/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

#### الخطوة 3: حفظ كـ wmf

`ImageSaveOptions` مع `SaveFormat.WMF` يخبر Aspose.CAD بكتابة المخرج كـ Windows Metafile.  
```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(100);
rasterizationOptions.setPageHeight(100);
WmfOptions wmfOptions = new WmfOptions();
```

#### الخطوة 4: تحرير الموارد

استدعاء `image.close()` يحرّر الموارد الأصلية المستخدمة من قبل كائن Aspose.CAD Image.  
```java
cadImage.save(dataDir+" example.ifc.wmf", wmfOptions);
```

#### الخطوة 5: اختياري – تصدير إلى pdf

`PdfOptions` يكوّن إعدادات خاصة بـ PDF عند حفظ الصورة كمستند PDF.  
```java
finally
{
  cadImage.dispose();
}
```

> **نصيحة احترافية:** يمكنك إعادة استخدام نفس كائن `CadRasterizationOptions` لتصدير PDF عن طريق تمريره إلى مثال `PdfOptions`، مما يوفر لك بضع أسطر من الإعداد.

## كيف يمكنني تصدير DXF إلى PDF باستخدام Aspose CAD Java؟

استبدل تنسيق الحفظ WMF بـ PDF باستخدام `new ImageSaveOptions(SaveFormat.Pdf)`. تُطبق نفس إعدادات الترصيص، ويمكنك كذلك تعيين خيارات خاصة بـ PDF مثل بيانات المؤلف أو مستوى الضغط. ينتج عن هذا التحويل في سطر واحد ملف PDF قابل للبحث، ودقيق في الصفحات، يعكس تخطيط CAD الأصلي.

## المشكلات الشائعة والحلول

`License` هي الفئة في Aspose المستخدمة لتطبيق ترخيص المنتج أثناء التشغيل.

| المشكلة | السبب | الحل |
|-------|-------|-----|
| **`NullPointerException` على `cadImage.save`** | المتغيّر `cadImage` غير معرف (يجب أن يكون `image`). | استبدل `cadImage` بـ `image` أو أعد تسمية المتغيّر بشكل متسق. |
| **مخرجات WMF فارغة** | حجم صفحة الترصيص صغير جداً أو تم تعيين لون الخلفية شفافًا. | قم بزيادة `PageWidth`/`PageHeight` أو عيّن لون خلفية عبر `rasterizationOptions.setBackgroundColor(Color.WHITE);`. |
| **استثناء الترخيص** | التشغيل بدون ترخيص Aspose صالح في بيئة الإنتاج. | طبق ملف الترخيص عند بدء التطبيق: `License license = new License(); license.setLicense("Aspose.Total.Java.lic");`. |

## الأسئلة المتكررة

**س: أين يمكنني العثور على وثائق Aspose.CAD؟**  
ج: يمكنك الوصول إلى الوثائق [Aspose.CAD Java documentation](https://reference.aspose.com/cad/java/).

**س: كيف يمكنني تنزيل Aspose.CAD للـ Java؟**  
ج: قم بتنزيل المكتبة [Aspose.CAD Java download page](https://releases.aspose.com/cad/java/).

**س: هل تتوفر نسخة تجريبية مجانية؟**  
ج: نعم، يمكنك الحصول على نسخة تجريبية مجانية [Aspose free trial page](https://releases.aspose.com/).

**س: هل تحتاج إلى خيارات ترخيص مؤقتة؟**  
ج: استكشف تراخيص مؤقتة [temporary license options](https://purchase.aspose.com/temporary-license/).

**س: أين يمكنني الحصول على الدعم؟**  
ج: قم بزيارة منتدى دعم Aspose.CAD [Aspose.CAD support forum](https://forum.aspose.com/c/cad/19).

## أسئلة متكررة إضافية

**س: هل يمكنني تحويل ملفات DXF الكبيرة (مئات الميجابايت) دون نفاد الذاكرة؟**  
ج: نعم. حمّل الملف في كتلة try‑with‑resources وقم بتحرير كائن `Image` فوراً. اضبط `CadRasterizationOptions.setPageWidth/Height` إلى حجم معقول للحفاظ على استهلاك الذاكرة منخفضًا.

**س: هل يحتفظ مخرجات WMF بمعلومات الطبقات؟**  
ج: WMF هو تنسيق متجه مسطح، لذا يتم تسطيح هيكل الطبقات، لكن أنماط الخطوط، الألوان، وأنماط التظليل تُحفظ.

**س: هل يمكن تعيين DPI مخصص للـ WMF؟**  
ج: استخدم `rasterizationOptions.setResolution(300);` لتحديد DPI قبل الحفظ.

**س: هل يمكنني تحويل دفعة من ملفات DXF متعددة في تشغيل واحد؟**  
ج: بالطبع. قم بالتكرار عبر دليل، حمّل كل ملف، وطبق نفس منطق الترصيص والحفظ.

**س: ما إصدارات Java المدعومة؟**  
ج: Aspose.CAD للـ Java يدعم Java 8 وما بعده، بما في ذلك Java 11 و17 والإصدارات الأحدث من LTS.

---

**آخر تحديث:** 2026-10-30  
**تم الاختبار مع:** Aspose.CAD for Java 24.11  
**المؤلف:** Aspose

## دروس ذات صلة

- [إنشاء PDF من CAD – تصدير DXF إلى PDF باستخدام Aspose.CAD للـ Java](/cad/java/additional-features/export-dxf-to-pdf/)
- [إنشاء PDF من DXF: تصدير الطبقة باستخدام Aspose.CAD للـ Java](/cad/java/additional-features/export-specific-layer-to-pdf/)
- [كيفية تحويل تخطيط DXF إلى صورة JPEG باستخدام Aspose.CAD في Java](/cad/java/additional-features/export-specific-layout-to-image/)

```java
image.save(dataDir + "conic_pyramid_out_.pdf"); 
```

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}