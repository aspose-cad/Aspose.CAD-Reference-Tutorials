---
date: 2026-10-04
description: تعلم كيفية البحث عن النص في ملفات DWG باستخدام C# و Aspose.CAD لـ .NET.
  استخراج النص، قراءة ملفات DWG، وتعزيز تطبيقات CAD الخاصة بك.
keywords:
- search text in dwg
- extract text from dwg
- c# read dwg file
- how to search dwg files
lastmod: 2026-10-04
linktitle: بحث النص ومعالجته
og_description: البحث عن النص في ملفات DWG باستخدام C# و Aspose.CAD لـ .NET. استخراج
  النص، قراءة ملفات DWG، وتحسين أداء تطبيقات CAD.
og_image_alt: Guide showing C# code searching text in DWG files with Aspose.CAD
og_title: البحث عن النص في ملفات DWG باستخدام C# و Aspose.CAD
schemas:
- author: Aspose
  dateModified: '2026-10-04'
  description: Learn how to search text in DWG files using C# and Aspose.CAD for .NET.
    Extract text, read DWG files, and boost your CAD applications.
  headline: Search text in DWG files with C# using Aspose.CAD
  type: TechArticle
- description: Learn how to search text in DWG files using C# and Aspose.CAD for .NET.
    Extract text, read DWG files, and boost your CAD applications.
  name: Search text in DWG files with C# using Aspose.CAD
  steps:
  - name: install the Aspose.CAD NuGet package
    text: 'Open the NuGet Package Manager console and run: This adds the required
      assemblies and updates your project file.'
  - name: open the DWG file
    text: Create a `CadImage` instance by calling `Image.Load`. The method automatically
      detects the file format and prepares an in‑memory representation.
  - name: enumerate text fragments
    text: '`image.TextFragments` returns a collection of `TextFragment` objects, each
      exposing `Text`, `Location`, `Height`, and `LayerName`. You can iterate or LINQ‑filter
      this collection.'
  - name: apply your search criteria
    text: Use `String.Contains`, `Regex.IsMatch`, or any custom predicate to locate
      the exact text you need. For case‑insensitive searches, call `ToLowerInvariant()`
      on both sides.
  - name: handle the results
    text: Typical actions include logging the fragment’s coordinates, exporting to
      CSV, or highlighting the entity in a viewer. Because the API gives you the exact
      `Location`, you can feed it into any downstream CAD visualization component.
  type: HowTo
- questions:
  - answer: Yes. Provide the password via `CadLoadOptions.Password` when calling `Image.Load`.
    question: Can I search for text in password‑protected DWG files?
  - answer: Absolutely. Loop through a directory, load each file, and reuse the same
      LINQ filter – the library is thread‑safe for parallel processing.
    question: Does the API support searching across multiple DWG files at once?
  - answer: Aspose.CAD reports a **99 % success rate** on industry‑standard test sets,
      handling MTEXT, attribute definitions, and even embedded Unicode characters.
    question: How accurate is the text extraction for complex annotations?
  - answer: After obtaining the `Location` of each `TextFragment`, you can draw a
      temporary overlay using any CAD viewer that accepts geometry primitives.
    question: Is there a way to highlight found text in a viewer?
  - answer: The product uses a per‑developer or per‑server license model; a free evaluation
      license is available for 30 days.
    question: What licensing model applies to Aspose.CAD?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- CAD processing
- Aspose.CAD
- .NET
- DWG text search
title: البحث عن النص في ملفات DWG باستخدام C# و Aspose.CAD
url: /ar/net/text-search-and-manipulation/
weight: 28
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# البحث عن النص في ملفات DWG باستخدام C# و Aspose.CAD

## مقدمة

في هذا البرنامج التعليمي ستتعلم كيفية **search text in DWG** ملفات باستخدام C# عن طريق استخدام مكتبة Aspose.CAD القوية لـ .NET. سواء كنت بحاجة إلى تحديد التعليقات التوضيحية، استخراج قيم السمات، أو بناء فهرس قابل للبحث، فإن الخطوات أدناه ستوجهك عبر حل موثوق وعالي الأداء يعمل على كل من .NET Framework و .NET Core.

## إجابات سريعة
- **ما المكتبة التي تتعامل مع بحث نص DWG؟** Aspose.CAD for .NET.
- **هل يمكنني استخراج النص من DWG؟** نعم – تُعيد API سلاسل نصية عادية لأي كيان تم العثور عليه.
- **ما إصدارات .NET المدعومة؟** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.
- **هل أحتاج إلى ترخيص للتطوير؟** ترخيص مؤقت مجاني يعمل للتقييم؛ الترخيص الكامل مطلوب للإنتاج.
- **هل العملية فعّالة من حيث الذاكرة؟** نعم، Aspose.CAD يعالج الملفات بطريقة تدفقية، مما يسمح بالتعامل مع DWG مئات الصفحات دون تحميل الملف بالكامل في الذاكرة.

## ما هو البحث عن النص في DWG؟

CadImage هو كائن Aspose.CAD الذي يمثل رسم CAD محملاً، ويكشف عن كياناته مثل قطع النص.  
TextFragment يمثل قطعة فردية من النص المستخرج، بما في ذلك محتواها وموقعها الهندسي.

تشير العبارة *search text in DWG* إلى تحديد بيانات السلسلة برمجياً—مثل أسماء الطبقات، قيم السمات، أو نص التعليقات التوضيحية—داخل ملف رسم DWG. Aspose.CAD يتيح هذه القدرة عبر كائن `CadImage` ومجموعة `TextFragment`، مما يسمح للمطورين باسترجاع النص ومعالجته بكفاءة.

## لماذا نستخدم Aspose.CAD للبحث عن نص DWG؟

Aspose.CAD يدعم **30+ تنسيقات CAD و BIM** (بما في ذلك DWG، DXF، DGN، DWF) ويمكنه معالجة ملفات تصل إلى **500 MB** دون تحميل كامل في الذاكرة. المكتبة تضمن **99 % دقة استخراج النص** على الرسومات المعقدة، وهو تحسين مُقاس مقارنة بالعديد من المحللات المفتوحة المصدر التي غالباً ما تفوت MTEXT المدمج أو سمات الكتل.

## كيفية البحث عن النص في ملفات DWG باستخدام C#؟

Image.Load هي طريقة ثابتة تقرأ ملف CAD وتعيد كائن CadImage.

قم بتحميل DWG باستخدام `Image.Load`، استرجع مجموعة `TextFragments`، وصّفها باستخدام LINQ بناءً على مصطلح البحث الخاص بك. هذا النمط المختصر يعمل بزمن خطي نسبة إلى عدد الكيانات النصية، لا يتطلب مكتبات إضافية، ويعمل بشكل ثابت عبر بيئات .NET Framework و .NET Core.

### الخطوة 1: تثبيت حزمة Aspose.CAD NuGet
افتح وحدة تحكم مدير الحزم NuGet وشغّل:

```
Install-Package Aspose.CAD
```

### الخطوة 2: فتح ملف DWG
أنشئ كائن `CadImage` عن طريق استدعاء `Image.Load`. الطريقة تكتشف تنسيق الملف تلقائياً وتُعد تمثيلاً في الذاكرة.

### الخطوة 3: تعداد قطع النص
`image.TextFragments` تُعيد مجموعة من كائنات `TextFragment`، كل منها يُظهر `Text`، `Location`، `Height`، و `LayerName`. يمكنك التكرار أو تصفية هذه المجموعة باستخدام LINQ.

### الخطوة 4: تطبيق معايير البحث الخاصة بك
استخدم `String.Contains`، `Regex.IsMatch`، أو أي شرط مخصص لتحديد النص الدقيق الذي تحتاجه. للبحث غير حساس لحالة الأحرف، استدعِ `ToLowerInvariant()` على الجانبين.

### الخطوة 5: معالجة النتائج
تشمل الإجراءات النموذجية تسجيل إحداثيات القطعة، تصدير إلى CSV، أو تمييز الكيان في عارض. لأن الـ API يزودك بـ `Location` الدقيق، يمكنك تمريره إلى أي مكوّن تصور CAD لاحق.

## كيفية استخراج النص من DWG؟

TextFragment هو الكائن الذي يحمل النص المستخرج والبيانات الوصفية المرتبطة به مثل الموقع والطبقة.

استخراج النص مماثل للبحث؛ ببساطة عد مجموعة `TextFragment` واقرأ خاصية `TextFragment.Text` لكل عنصر. يمكنك دمج السلاسل في مستند واحد، كتابتها إلى ملف CSV، أو تمريرها إلى فهرس بحث لاسترجاع سريع عبر رسومات متعددة.

## المشكلات الشائعة واستكشاف الأخطاء

- **Missing MTEXT:** بعض إصدارات DWG القديمة تخزن النص متعدد الأسطر في سمات الكتل. تأكد من فحص `image.Blocks` للعثور على كائنات `Attribute`.
- **Encoding issues:** قد تستخدم ملفات DWG صفحات ترميز غير Unicode. اضبط `image.LoadOptions.Encoding` إلى `System.Text.Encoding` المناسب قبل التحميل.
- **Large files:** للملفات الأكبر من 200 MB، فعّل `image.LoadOptions.Streaming = true` للحفاظ على استهلاك الذاكرة تحت 100 MB.

## الأسئلة المتكررة

**س: هل يمكنني البحث عن نص في ملفات DWG محمية بكلمة مرور؟**  
ج: نعم. قدّم كلمة المرور عبر `CadLoadOptions.Password` عند استدعاء `Image.Load`.

**س: هل تدعم الـ API البحث عبر عدة ملفات DWG في آن واحد؟**  
ج: بالتأكيد. قم بالتكرار عبر دليل، حمّل كل ملف، وأعد استخدام نفس مرشح LINQ – المكتبة آمنة للخطوط المتعددة للمعالجة المتوازية.

**س: ما مدى دقة استخراج النص للتعليقات التوضيحية المعقدة؟**  
ج: Aspose.CAD يعلن عن **99 % معدل نجاح** على مجموعات اختبار معيارية صناعية، مع معالجة MTEXT، تعريفات السمات، وحتى الأحرف Unicode المدمجة.

**س: هل هناك طريقة لتمييز النص المكتشف في عارض؟**  
ج: بعد الحصول على `Location` لكل `TextFragment`، يمكنك رسم طبقة مؤقتة باستخدام أي عارض CAD يقبل الأشكال الهندسية.

**س: ما نموذج الترخيص المطبق على Aspose.CAD؟**  
ج: المنتج يستخدم نموذج ترخيص لكل مطور أو لكل خادم؛ ترخيص تقييم مجاني متاح لمدة 30 يوماً.

---

**آخر تحديث:** 2026-10-04  
**تم الاختبار مع:** Aspose.CAD 24.11 for .NET  
**المؤلف:** Aspose  

## دروس البحث عن النص ومعالجته

### [البحث عن النص في ملفات DWG باستخدام C# - دليل Aspose.CAD](./searching-text-in-dwg-files/)

```csharp
using Aspose.CAD;
using Aspose.CAD.ImageOptions;

// Load the DWG file
using var image = (CadImage)Image.Load("sample.dwg");

// Retrieve all text fragments
var fragments = image.TextFragments;

// Filter fragments that contain the target string
var matches = fragments.Where(t => t.Text.Contains("TargetString"));
```

## دروس ذات صلة

- [تحويل DWG إلى PDF وإضافة نص في C# – دليل Aspose.CAD](/cad/net/dwg-file-manipulation/adding-text-to-dwg/)
- [كيفية تحويل DWG إلى PDF وصور نقطية باستخدام Aspose.CAD لـ .NET](/cad/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/)
- [كيفية عرض CAD وتحويل DWG – Aspose.CAD .NET](/cad/net/conversion-and-export/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}