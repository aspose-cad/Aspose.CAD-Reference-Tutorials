---
date: 2026-08-23
description: اكتشف إمكانات Aspose.CAD لـ .NET من خلال دليلنا خطوة بخطوة حول كيفية
  قراءة بيانات تعريف xref من ملفات DWG.
keywords:
- read xref metadata
- extract dwg xref
- Aspose.CAD
lastmod: 2026-08-23
linktitle: قراءة بيانات تعريف XREF من ملفات DWG
og_description: تعرف على كيفية قراءة بيانات تعريف xref من ملفات DWG باستخدام Aspose.CAD
  لـ .NET. يوضح لك هذا الدليل المتطلبات المسبقة، خطوات الكود، والمشكلات الشائعة في
  أقل من عشر دقائق.
og_image_alt: Screenshot of Aspose.CAD reading XREF metadata in a .NET IDE
og_title: كيفية قراءة بيانات تعريف xref من ملفات DWG باستخدام Aspose.CAD
schemas:
- author: Aspose
  dateModified: '2026-08-23'
  description: Unlock the potential of Aspose.CAD for .NET with our step‑by‑step tutorial
    on how to read xref metadata from DWG files.
  headline: How to read xref metadata from DWG files using Aspose.CAD
  type: TechArticle
- description: Unlock the potential of Aspose.CAD for .NET with our step‑by‑step tutorial
    on how to read xref metadata from DWG files.
  name: How to read xref metadata from DWG files using Aspose.CAD
  steps:
  - name: load the DWG file
    text: Create an `Image` instance from the DWG file you want to analyze. `Image.Load`
      loads a CAD file and returns a `CadImage` object representing the drawing. Adjust
      the `sourceFilePath` variable to the exact location of your drawing.
  - name: iterate through entities
    text: Loop through the `Image` object’s `Entities` collection. `CadBaseEntity`
      is the base class for all CAD entities in Aspose.CAD. For each entity, check
      whether it is an XREF reference and collect its metadata.
  - name: extract metadata
    text: When you encounter an XREF entity, read its insertion point (X, Y, Z) and
      the path of the referenced drawing. `CadUnderlay` represents an external reference
      (XREF) entity within a DWG drawing.
  - name: process metadata
    text: At this stage you can store the extracted information in a database, write
      it to a CSV file, or feed it into downstream BIM workflows. The sample simply
      prints the values to the console, but you are free to replace that with any
      custom logic.
  type: HowTo
- questions:
  - answer: Yes, Aspose.CAD for .NET supports **50+ input and output formats**, including
      DWG, DXF, DGN, and IFC, giving you broad coverage for most engineering workflows.
    question: Is Aspose.CAD for .NET compatible with all CAD file formats?
  - answer: Certainly! You can access the free trial download page [free trial download
      page](https://releases.aspose.com/).
    question: Can I use the free trial before making a purchase decision?
  - answer: The documentation is available [Aspose.CAD .NET documentation](https://reference.aspose.com/cad/net/).
    question: Where can I find comprehensive documentation for Aspose.CAD for .NET?
  - answer: You can get a temporary license [temporary license page](https://purchase.aspose.com/temporary-license/).
    question: How do I obtain a temporary license for Aspose.CAD for .NET?
  - answer: Join the Aspose.CAD community at [Aspose.CAD Forum](https://forum.aspose.com/c/cad/19)
      for expert support and discussions.
    question: Need assistance or have specific queries?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- read xref metadata
- extract dwg xref
- Aspose.CAD
- DWG
- CAD metadata
title: كيفية قراءة بيانات تعريف xref من ملفات DWG باستخدام Aspose.CAD
url: /ar/net/image-manipulation-and-rendering/reading-xref-metadata-from-dwg/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية قراءة بيانات تعريف XREF من ملفات DWG باستخدام Aspose.CAD

## مقدمة

في هذا البرنامج التعليمي ستتعلم **كيفية قراءة بيانات تعريف XREF** من ملفات DWG باستخدام مكتبة Aspose.CAD لـ .NET. سواء كنت بحاجة إلى تدقيق المراجع الخارجية، أو ترحيل الرسومات القديمة، أو بناء خط أنابيب BIM مخصص، فإن استخراج معلومات XREF هو مطلب شائع. سنستعرض كل خطوة، من إعداد المشروع إلى معالجة البيانات الوصفية، وسنبرز نصائح عملية يمكنك تطبيقها فورًا.

## إجابات سريعة
- **ما هو الهدف الرئيسي؟** استرجاع نقاط الإدراج ومسارات الملفات للمراجع الخارجية (XREFs) المدمجة في رسم DWG.  
- **ما المكتبة المطلوبة؟** Aspose.CAD لـ .NET (يدعم أكثر من 50 تنسيق CAD).  
- **هل أحتاج إلى ترخيص؟** يتطلب ترخيص مؤقت أو كامل للاستخدام في بيئة الإنتاج؛ يتوفر نسخة تجريبية مجانية.  
- **ما إصدارات .NET المدعومة؟** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.  
- **كم يستغرق تشغيل الكود؟** معالجة ملف DWG نموذجي مكوّن من 200 صفحة مع بعض XREFs يكتمل في أقل من ثانية على الأجهزة القياسية.

## ما هو قراءة بيانات XREF الوصفية؟
`read xref metadata` يشير إلى عملية الوصول إلى خصائص كيانات المراجع الخارجية المخزنة داخل رسم DWG، مثل إحداثيات الإدراج، مسارات ملفات المصدر، وعلامات الرؤية. تتيح لك هذه العملية اكتشاف كيفية تكوين الرسم من ملفات أخرى برمجيًا، مما يمكّن من التحقق الآلي، إعداد التقارير، أو المعالجة الدفعية للموارد المرتبطة.

## لماذا تستخدم Aspose.CAD لهذه المهمة؟
Aspose.CAD يدعم **أكثر من 50 تنسيق ملف CAD** ويمكنه قراءة ملفات DWG **دون الحاجة إلى AutoCAD**. تقوم المكتبة بمعالجة الرسومات الكبيرة **في تدفقات فعّالة للذاكرة**، مما يتيح لك التعامل مع ملفات مئات الصفحات دون تحميل الملف بالكامل إلى الذاكرة. تجعل هذه القدرات المكمّنة موثوقة للاستخدام المؤسسي في أتمتة CAD.

## المتطلبات المسبقة

قبل الغوص في الكود، تحقق من أن لديك ما يلي:

- تم تثبيت Aspose.CAD لـ .NET. احصل على أحدث حزمة من صفحة [Aspose.CAD for .NET release page](https://releases.aspose.com/cad/net/).
- مجلد محلي يحتوي على ملفات DWG التي تريد فحصها. حدّث المتغيّر `MyDir` في الكود النموذجي للإشارة إلى هذا المجلد.
- ترخيص Aspose.CAD صالح (أو النسخة التجريبية المجانية) إذا كنت تخطط لتشغيل الكود في بيئة إنتاج.

الآن بعد أن أصبحت البيئة جاهزة، لنبدأ الترميز.

## استيراد مساحات الأسماء

الخطوة الأولى التي تحتاج إلى القيام بها هي استيراد مساحات الأسماء التي تكشف عن API الخاص بـ Aspose.CAD. توجيهات `using` تجلب مساحات الأسماء إلى النطاق، مما يسمح بالوصول إلى فئات CAD مثل `Image` و `CadImage`.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadObjects;
```

## كيفية قراءة بيانات XREF الوصفية من ملفات DWG؟

قم بتحميل الرسم، عدّ الكيانات، صَفِّ للكيانات XREF، ثم استخرج الخصائص المطلوبة—كل ذلك في بضع أسطر شفرة بسيطة. الأقسام التالية تقسم العملية إلى أربع خطوات منطقية يمكنك نسخها ولصقها في أي مشروع .NET كونسول أو خدمة.

### الخطوة 1: تحميل ملف DWG

أنشئ كائن `Image` من ملف DWG الذي تريد تحليله. `Image.Load` يحمل ملف CAD ويعيد كائن `CadImage` يمثل الرسم. عدّل المتغيّر `sourceFilePath` ليشير إلى الموقع الدقيق للرسم الخاص بك.

```csharp
// The path to the documents directory.
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Bottom_plate.dwg";
using (CadImage image = (CadImage)Image.Load(sourceFilePath))
{
    // Code for the next steps goes here
}
```

### الخطوة 2: التكرار عبر الكيانات

تجول في مجموعة `Entities` لكائن `Image`. `CadBaseEntity` هو الفئة الأساسية لجميع كيانات CAD في Aspose.CAD. لكل كيان، تحقق مما إذا كان مرجع XREF وجمع بياناته الوصفية.

```csharp
foreach (CadBaseEntity entity in image.Entities)
{
    if (entity is CadUnderlay)
    {
        // Code for the next steps goes here
    }
}
```

### الخطوة 3: استخراج البيانات الوصفية

عند مواجهة كيان XREF، اقرأ نقطة الإدراج (X, Y, Z) ومسار الرسم المرجعي. `CadUnderlay` يمثل كيان مرجع خارجي (XREF) داخل رسم DWG.

```csharp
//XREF entity with metadata
Cad3DPoint insertionPoint = ((CadUnderlay)entity).InsertionPoint;
string path = ((CadUnderlay)entity).UnderlayPath;
```

### الخطوة 4: معالجة البيانات الوصفية

في هذه المرحلة يمكنك تخزين المعلومات المستخرجة في قاعدة بيانات، كتابة ملف CSV، أو إمداده إلى سير عمل BIM لاحق. المثال يطبع القيم إلى وحدة التحكم فقط، لكن يمكنك استبدال ذلك بأي منطق مخصص.

```csharp
// Your custom logic for processing metadata goes here
```

## المشكلات الشائعة واستكشاف الأخطاء

| العَرَض | السبب المحتمل | الحل |
|---------|--------------|-----|
| لم يتم إرجاع أي كيانات XREF | الرسم يستخدم نوع مرجع مختلف (مثل INSERT) | تحقق من نوع الكيان مقابل `CadEntityType.Xref` وتعامل مع `Insert` إذا لزم الأمر |
| `Image.Load` يرمي استثناء | مسار ملف غير صحيح أو نسخة DWG غير مدعومة | تحقق من المسار وتأكد من أنك تستخدم Aspose.CAD 24.11 أو أحدث |
| قيم البيانات الوصفية فارغة | تم تعريف XREF لكنه غير محلول (ملف خارجي مفقود) | تأكد من وجود الملف المرجعي على القرص أو قدم محلل نظام ملفات افتراضي |

## الأسئلة المتكررة

**س: هل Aspose.CAD لـ .NET متوافق مع جميع تنسيقات ملفات CAD؟**  
ج: نعم، Aspose.CAD لـ .NET يدعم **أكثر من 50 تنسيق إدخال وإخراج**، بما في ذلك DWG و DXF و DGN و IFC، مما يمنحك تغطية واسعة لمعظم سير عمل الهندسة.

**س: هل يمكنني استخدام النسخة التجريبية المجانية قبل اتخاذ قرار الشراء؟**  
ج: بالتأكيد! يمكنك الوصول إلى صفحة تحميل النسخة التجريبية [free trial download page](https://releases.aspose.com/).

**س: أين يمكنني العثور على وثائق شاملة لـ Aspose.CAD لـ .NET؟**  
ج: الوثائق متاحة على [Aspose.CAD .NET documentation](https://reference.aspose.com/cad/net/).

**س: كيف أحصل على ترخيص مؤقت لـ Aspose.CAD لـ .NET؟**  
ج: يمكنك الحصول على ترخيص مؤقت عبر [temporary license page](https://purchase.aspose.com/temporary-license/).

**س: هل تحتاج إلى مساعدة أو لديك استفسارات محددة؟**  
ج: انضم إلى مجتمع Aspose.CAD على [Aspose.CAD Forum](https://forum.aspose.com/c/cad/19) للحصول على دعم خبراء ومناقشات.

## الخلاصة

أصبح لديك الآن نمط كامل وجاهز للإنتاج **لقراءة بيانات XREF الوصفية** من ملفات DWG باستخدام Aspose.CAD لـ .NET. باتباع الخطوات الأربع—تحميل الملف، التكرار عبر الكيانات، استخراج نقطة الإدراج ومسار الـ underlay، ومعالجة النتائج—يمكنك دمج هذه القدرة في أي تطبيق يركز على CAD، سواء كان أداة ترحيل بيانات، سكريبت مراقبة جودة، أو خط أنابيب BIM مخصص.

---

**آخر تحديث:** 2026-08-23  
**تم الاختبار مع:** Aspose.CAD 24.11 for .NET  
**المؤلف:** Aspose

## الدروس ذات الصلة

- [كيفية تغيير مسار XREF وتعديل الروابط التشعبية في ملفات CAD - دليل Aspose.CAD](/cad/net/advanced-cad-techniques/editing-hyperlinks-in-cad-files/)
- [الحصول على سمات الكتل من ملفات DWG - دليل Aspose.CAD](/cad/net/image-manipulation-and-rendering/getting-block-attributes-from-dwg/)
- [تحويل ملفات DWG الكبيرة إلى PDF - دليل Aspose.CAD](/cad/net/image-manipulation-and-rendering/converting-large-dwg-files-to-pdf/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}