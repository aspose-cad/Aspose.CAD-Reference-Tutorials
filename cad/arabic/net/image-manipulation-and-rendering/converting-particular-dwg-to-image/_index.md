---
date: 2026-08-12
description: استخراج النص من ملفات DWG وتحويل DWG محدد إلى صورة باستخدام C# مع Aspose.CAD
  لـ .NET. تعلم خطوة بخطوة مع مقتطفات الشيفرة.
keywords:
- extract text from dwg
- convert specific dwg to image
- Aspose.CAD .NET
lastmod: 2026-08-12
linktitle: تحويل DWG معين إلى صورة باستخدام C#
og_description: استخراج النص من ملفات DWG وتحويل DWG محدد إلى صورة باستخدام C# مع
  Aspose.CAD. اتبع هذا الدليل المختصر للتنفيذ السريع.
og_image_alt: Guide showing DWG to image conversion and text extraction using Aspose.CAD
  in C#
og_title: استخراج النص من ملفات DWG وتحويل DWG محدد إلى صورة باستخدام C#
schemas:
- author: Aspose
  dateModified: '2026-08-12'
  description: Extract text from DWG and convert specific DWG to image in C# using
    Aspose.CAD for .NET. Learn step‑by‑step with code snippets.
  headline: Extract text from DWG and convert specific DWG to image in C#
  type: TechArticle
- questions:
  - answer: Aspose.CAD supports DWG releases from AutoCAD 2000 up to the latest 2024
      version, covering over 90 % of files created in the field.
    question: Is Aspose.CAD compatible with all versions of DWG files?
  - answer: Yes – you can change resolution, image format, anti‑aliasing, and background
      color to suit PNG, JPEG, or PDF targets.
    question: Can I customize the rasterization options for different outputs?
  - answer: Explore the comprehensive [Aspose.CAD documentation](https://reference.aspose.com/cad/net/)
      for more code samples and API details.
    question: Where can I find additional examples and documentation?
  - answer: Absolutely – you can download a trial version on the **[Aspose trial download
      page](https://releases.aspose.com/)** and evaluate all features without restrictions
      for 30 days.
    question: Is there a free trial available for Aspose.CAD?
  - answer: Join the active [Aspose.CAD forum](https://forum.aspose.com/c/cad/19)
      where developers share solutions and the Aspose team answers questions.
    question: How can I get support or connect with the community?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- extract text from dwg
- Aspose.CAD
- C# CAD processing
title: استخراج النص من ملفات DWG وتحويل DWG محدد إلى صورة باستخدام C#
url: /ar/net/image-manipulation-and-rendering/converting-particular-dwg-to-image/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تحويل ملف DWG معين إلى صورة في C# - دليل Aspose.CAD

## المقدمة

في تطبيقات الهندسة الحديثة، غالبًا ما تحتاج إلى **استخراج النص من ملفات DWG** و**تحويل DWG محدد إلى صيغ صورة** للتقارير أو التصور. توفر Aspose.CAD لـ .NET واجهة برمجة تطبيقات كاملة المميزات تتعامل مع كلا المهمتين دون الحاجة إلى أي برنامج CAD خارجي. في هذا الدرس ستتعلم كيفية تحميل ملف DWG، تصفية الكيانات النصية، تحويل الرسم إلى نقطية، وأخيرًا حفظ النتيجة كصورة PDF — كل ذلك بكود C# نظيف.

## إجابات سريعة
- **ما هي الخطوة الأولى؟** تحميل ملف DWG باستخدام `new CadImage("file.dwg")`.  
- **أي فئة تقوم بتصفية النص؟** استخدم `CadEntityFilter` لاختيار الكيانات `Text`.  
- **كيف تحدد حجم الصورة؟** اضبط `Width` و `Height` في `CadRasterizationOptions`.  
- **ما هو تنسيق الإخراج المستخدم؟** المثال يحفظ إلى PDF، الذي يضم الصورة النقطية.  
- **هل أحتاج إلى ترخيص للإنتاج؟** نعم – ترخيص Aspose.CAD التجاري يزيل حدود التقييم.

## كيفية استخراج النص من DWG؟

قم بتحميل ملف DWG، ثم طبّق مرشحًا يختار فقط الكيانات النصية، وبعد ذلك اقرأ خاصية `TextString` لكل كيان. تُعيد هذه الطريقة كل قطعة من التعليقات التوضيحية أو العلامات أو نص الأبعاد الموجودة في الرسم، مما يتيح لك إعادة استخدامها للبحث أو الفهرسة أو التقارير.

## لماذا تحويل DWG محدد إلى صورة؟

تحويل DWG إلى صورة نقطية يتيح لك تضمين الرسم في مستندات أو صفحات ويب أو تطبيقات هاتفية لا يمكنها عرض صيغ CAD الأصلية. تعالج Aspose.CAD **أكثر من 50+ صيغة CAD** ويمكنها تحويل رسومات متعددة الصفحات إلى نقطية باستخدام أقل من 200 ميغابايت من الذاكرة، مما يجعلها مناسبة لسيناريوهات الخوادم عالية الإنتاجية.

## المتطلبات المسبقة

- Visual Studio (أي إصدار حديث) لتجميع وتشغيل مشاريع C#.  
- Aspose.CAD لـ .NET – تأكد من تثبيت المكتبة. يمكنك العثور على رابط التحميل في **[صفحة تحميل Aspose.CAD لـ .NET](https://releases.aspose.com/cad/net/)**.  
- ملف DWG تريد العمل معه؛ يتم استخدام ملف العينة *visualization_-_conference_room.dwg* في مقتطفات الشيفرة.

## استيراد مساحات الأسماء

تُتيح لك مساحات الأسماء التالية الوصول إلى الفئات الأساسية في CAD، خيارات التحويل إلى نقطية، ومساعدي إخراج PDF:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadConsts;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## الخطوة 1: تحميل ملف DWG

أنشئ كائن `CadImage` بتمرير مسار ملف DWG الخاص بك. يمثل كائن `CadImage` الرسم بالكامل في الذاكرة ويوفر الوصول إلى طبقاته، كياناته، وبياناته الوصفية.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "visualization_-_conference_room.dwg";
var cadImage = (CadImage)Aspose.CAD.Image.Load(sourceFilePath);
```

## الخطوة 2: تصفية الكيانات

يتيح لك `CadEntityFilter` اختيار الكيانات التي تحتاجها فقط. في هذا الدليل نقوم بتكوينه للاحتفاظ بالكائنات **النصية**، متجاهلين الخطوط والدوائر وغيرها من الهندسة التي لا تريدها في الصورة النهائية.

```csharp
CadBaseEntity[] entities = cadImage.Entities;
List<CadBaseEntity> filteredEntities = new List<CadBaseEntity>();

foreach (CadBaseEntity baseEntity in entities)
{
    // Selection or filtration of entities
    if (baseEntity.TypeName == CadEntityTypeName.TEXT)
    {
        filteredEntities.Add(baseEntity);
    }
}

cadImage.Entities = filteredEntities.ToArray();
```

## الخطوة 3: تعيين خيارات التحويل إلى نقطية

`CadRasterizationOptions` يتحكم في كيفية تحويل الرسم إلى صورة نقطية. يمكنك تحديد حجم الإخراج، لون الخلفية، والدقة (DPI). المُعرّف التالي يقدّم الفئة:

الفئة `CadRasterizationOptions` تحدد أبعاد الصورة، الدقة، وإعدادات العرض لتحويل رسومات CAD إلى صيغ نقطية.  

حدد العرض والارتفاع المطلوبين ولون الخلفية قبل تمرير الخيارات إلى مُصدّر PDF.

```csharp
Aspose.CAD.ImageOptions.CadRasterizationOptions rasterizationOptions =
    new Aspose.CAD.ImageOptions.CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
rasterizationOptions.AutomaticLayoutsScaling = true;
```

## الخطوة 4: تعيين خيارات PDF

`PdfOptions` يجمع بين إعدادات التحويل إلى نقطية وميزات PDF الخاصة مثل الضغط. المُعرّف لهذه الفئة يظهر أولاً:

`PdfOptions` يضم معلمات إنشاء PDF، بما في ذلك خيارات التحويل إلى نقطية التي تحدد كيفية عرض بيانات CAD داخل مستند PDF.  

عيّن كائن `CadRasterizationOptions` الذي أنشأته مسبقًا إلى الخاصية `VectorRasterizationOptions`.

```csharp
Aspose.CAD.ImageOptions.PdfOptions pdfOptions = new Aspose.CAD.ImageOptions.PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## الخطوة 5: حفظ كملف PDF

أخيرًا، استدعِ طريقة `Save` على كائن `CadImage`، مع تمرير اسم الملف الهدف وخيارات `PdfOptions` المكوّنة. سيحتوي ملف PDF على صورة عالية الجودة للرسم المصفّى.

```csharp
string outFile = MyDir + "result_out_generated.pdf";
cadImage.Save(outFile, pdfOptions);
```

## المشكلات الشائعة واستكشاف الأخطاء

- **نص مفقود بعد التصفية** – تأكد من أن ملف DWG يحتوي فعليًا على كيانات `Text`؛ بعض الرسومات تخزن التعليقات التوضيحية كـ `MText`. عدّل الفلتر ليشمل `MText` إذا لزم الأمر.  
- **صورة ناتجة فارغة** – تحقق من أن DPI للتحويل إلى نقطية عالي بما فيه الكفاية (300 DPI هو الافتراضي الآمن) وأن لون الخلفية ليس شفافًا عند عرض PDF.  
- **أخطاء نفاد الذاكرة في الملفات الكبيرة** – استخدم نسخة `LoadOptions` التي تتيح البث، مما يمنع تحميل الملف بالكامل إلى الذاكرة مرة واحدة.

## الأسئلة المتكررة

**س: هل Aspose.CAD متوافق مع جميع إصدارات ملفات DWG؟**  
ج: يدعم Aspose.CAD إصدارات DWG من AutoCAD 2000 حتى أحدث إصدار 2024، ويغطي أكثر من 90 % من الملفات التي تم إنشاؤها في المجال.

**س: هل يمكنني تخصيص خيارات التحويل إلى نقطية لمخرجات مختلفة؟**  
ج: نعم – يمكنك تغيير الدقة، صيغة الصورة، مضاد التعرج، ولون الخلفية لتناسب أهداف PNG أو JPEG أو PDF.

**س: أين يمكنني العثور على أمثلة إضافية ووثائق؟**  
ج: استكشف الوثائق الشاملة لـ [Aspose.CAD documentation](https://reference.aspose.com/cad/net/) للحصول على مزيد من عينات الشيفرة وتفاصيل API.

**س: هل هناك نسخة تجريبية مجانية متاحة لـ Aspose.CAD؟**  
ج: بالتأكيد – يمكنك تنزيل نسخة تجريبية من **[صفحة تحميل التجربة الخاصة بـ Aspose](https://releases.aspose.com/)** وتقييم جميع الميزات دون قيود لمدة 30 يومًا.

**س: كيف يمكنني الحصول على الدعم أو التواصل مع المجتمع؟**  
ج: انضم إلى منتدى [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) النشط حيث يشارك المطورون حلولًا ويجيب فريق Aspose على الأسئلة.

---

**آخر تحديث:** 2026-08-12  
**تم الاختبار مع:** Aspose.CAD 24.11 لـ .NET  
**المؤلف:** Aspose

## دروس ذات صلة

- [البحث عن النص في ملفات DWG باستخدام C# - دليل Aspose.CAD](/cad/net/text-search-and-manipulation/searching-text-in-dwg-files/)
- [تحويل رسم CAD إلى صورة نقطية في Aspose.CAD لـ .NET](/cad/net/cad-drawing-manipulation/convert-cad-drawing-to-raster-image/)
- [عرض مستندات DWG في C# - دليل Aspose.CAD](/cad/net/image-manipulation-and-rendering/rendering-dwg-documents/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< blocks/products/products-backtop-button >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}