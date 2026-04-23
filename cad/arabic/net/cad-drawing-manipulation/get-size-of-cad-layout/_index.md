---
date: 2026-03-21
description: تعلم كيفية الحصول على حجم تخطيط CAD في .NET باستخدام Aspose.CAD. اتبع
  دليلنا خطوة بخطوة للتعامل الفعال مع ملفات CAD.
linktitle: Get Size of CAD Layout
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: الحصول على حجم تخطيط CAD في Aspose.CAD لـ .NET
url: /ar/net/cad-drawing-manipulation/get-size-of-cad-layout/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# الحصول على حجم تخطيط CAD في Aspose.CAD لـ .NET

## المقدمة

في هذا الدرس الشامل ستكتشف **كيفية الحصول على حجم تخطيط CAD** باستخدام مكتبة Aspose.CAD لـ .NET. سواءً كنت تبني عارض CAD، أو تولد صورًا مصغرة، أو تحتاج إلى أبعاد تخطيط دقيقة للمعالجة اللاحقة، فإن معرفة الحجم الدقيق لكل تخطيط أمر أساسي. سنستعرض سير العمل بالكامل—من تحميل الرسم إلى استخراج أبعاد التخطيط وحفظها كصور إذا رغبت—حتى تتمكن من دمج هذه القدرة في تطبيقاتك بثقة.

## إجابات سريعة
- **ماذا يعني “الحصول على حجم تخطيط CAD”؟** يعني استخراج العرض والارتفاع (بوحدات الرسم) لكل تخطيط غير فارغ في ملف CAD.  
- **أي مكتبة تدعم ذلك؟** Aspose.CAD لـ .NET توفر واجهة برمجة تطبيقات بسيطة للوصول إلى معلومات التخطيط.  
- **هل أحتاج إلى ترخيص؟** النسخة التجريبية المجانية تكفي للتقييم؛ يلزم ترخيص تجاري للاستخدام في الإنتاج.  
- **الصيغ المدعومة؟** DWG، DXF والعديد من صيغ CAD/BIM الأخرى مدعومة بالكامل.  
- **الوقت التقريبي للتنفيذ؟** حوالي 10‑15 دقيقة لإنشاء روتين أساسي لاسترجاع الحجم.

## ما هو “الحصول على حجم تخطيط CAD”؟
يعني الحصول على حجم تخطيط CAD استخراج الامتدادات الهندسية لكل تخطيط (مساحة الورق) معرف في رسم CAD. تُعبّر هذه الامتدادات بوحدات الرسم الأصلية (عادةً ملليمترات أو بوصات) وتكون مفيدة لمهام مثل التحجيم، الطباعة، أو إنشاء صور معاينة.

## لماذا نسترجع حجم تخطيط CAD باستخدام Aspose.CAD؟
- **لا حاجة لبرنامج CAD** – يعمل بالكامل على الخادم.  
- **متعدد المنصات** – يعمل مع .NET Framework، .NET Core، و .NET 5/6+.  
- **قياسات دقيقة** – يُعيد الامتدادات الفعلية المخزنة في الملف، متجنبًا التحليل اليدوي.  
- **تكامل سهل** – استدعاءات API بسيطة تتناسب طبيعيًا مع مشاريع C# الحالية.

## المتطلبات المسبقة

قبل الغوص في الكود، تأكد من وجود ما يلي:

- تم تثبيت Aspose.CAD لـ .NET. يمكنك تنزيله من [صفحة تحميل Aspose.CAD لـ .NET](https://releases.aspose.com/cad/net/).
- ملف أو أكثر من ملفات CAD (DWG، DXF، إلخ) ترغب في تحليلها. يستخدم هذا الدليل ملفات `conic_pyramid.dxf` و `Bottom_plate.dwg` كأمثلة.

## استيراد مساحات الأسماء

في مشروع .NET الخاص بك، ابدأ باستيراد مساحات الأسماء المطلوبة:

```csharp
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadConsts;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.FileFormats.Cad.CadTables;
using Aspose.CAD.ImageOptions;
```

## الخطوة 1: إعداد دليل المستندات

حدد المجلد الذي يحتوي على ملفات CAD الخاصة بك. استبدل العنصر النائب بالمسار الفعلي على جهازك.

```csharp
string MyDir = "Your Document Directory";
```

## الخطوة 2: تحديد مسارات ملفات CAD

أنشئ مصفوفة تشير إلى كل ملف CAD تريد معالجته.

```csharp
string[] sourceFilePaths = new[]
{
    MyDir + "conic_pyramid.dxf",
    MyDir + "Bottom_plate.dwg"
};
```

## الخطوة 3: التكرار عبر ملفات CAD

حمّل كل ملف، اكتشف صيغته، واستعد لاستخراج معلومات التخطيط.

```csharp
foreach (var sourceFilePath in sourceFilePaths)
{
    string extension = Path.GetExtension(sourceFilePath);
    using (CadImage cadImage = (CadImage)Aspose.CAD.Image.Load(sourceFilePath))
    {
        // ... (continue to the next step)
    }
}
```

## الخطوة 4: الحصول على التخطيطات غير الفارغة

نحتاج إلى طريقة مساعدة تُعيد فقط التخطيطات التي تحتوي فعليًا على كيانات رسم. تُهمل التخطيطات الفارغة لأنها لا تملك حجمًا لتقارير عنه.

```csharp
private static List<string> GetNotEmptyLayouts(Image cadImage, string extension)
{
    // ... (continue to the next step)
}
```

## الخطوة 5: الحصول على التخطيطات لملفات DWG

تخزن ملفات DWG معلومات التخطيط في جدول `HeaderVariables`. الطريقة التالية تستخرج أسماء جميع التخطيطات غير الفارغة لرسم DWG.

```csharp
private static List<string> GetNotEmptyLayoutsForDwg(CadImage cadImage)
{
    // ... (continue to the next step)
}
```

## الخطوة 6: الحصول على التخطيطات لملفات DXF

تستخدم ملفات DXF بنية مختلفة. تقوم هذه الطريقة بتحليل مجموعة `Tables` للعثور على تخطيطات مساحة الورق التي تحتوي على كيانات.

```csharp
private static List<string> GetNotEmptyLayoutsForDxf(CadImage cadImage)
{
    // ... (continue to the next step)
}
```

## الخطوة 7: استرجاع حجم التخطيط وحفظه كصورة

أخيرًا، قم بالتكرار عبر كل تخطيط مكتشف، اقرأ امتداده، واختياريًا قم بتصوير التخطيط إلى ملف صورة للتحقق البصري.

```csharp
foreach (string layout in layouts)
{
    // ... (continue to the next step)
}
```

## المشكلات الشائعة والنصائح

- **أسماء التخطيطات مفقودة:** تأكد من أن ملف CAD يحتوي فعليًا على تخطيطات مساحة الورق؛ بعض الملفات تحتوي فقط على مساحة النموذج.  
- **الوحدات غير صحيحة:** يُعاد الحجم بوحدات الرسم الأصلية. حوّله إلى ملليمترات أو بوصات إذا لزم الأمر.  
- **الأداء:** تحميل ملفات DWG/DXF الكبيرة قد يستهلك الكثير من الذاكرة؛ فكر في معالجة الملفات بشكل غير متزامن أو على دفعات.

## الأسئلة المتكررة

**س: هل Aspose.CAD متوافق مع جميع صيغ ملفات CAD؟**  
ج: نعم، يدعم Aspose.CAD مجموعة واسعة من الصيغ، بما في ذلك DWG، DXF، DGN، والعديد من صيغ ملفات BIM.

**س: هل يمكنني تخصيص خيارات حفظ الصورة؟**  
ج: بالتأكيد! يمكنك تعديل `CadRasterizationOptions` (الصيغة، الدقة، لون الخلفية، إلخ) لتلبية احتياجاتك الخاصة.

**س: أين يمكنني العثور على وثائق إضافية؟**  
ج: راجع [وثائق Aspose.CAD](https://reference.aspose.com/cad/net/) للحصول على مراجع API مفصلة ومزيد من الأمثلة.

**س: هل هناك نسخة تجريبية مجانية متاحة؟**  
ج: نعم، يمكنك استكشاف Aspose.CAD عبر [نسخة تجريبية مجانية](https://releases.aspose.com/).

**س: كيف يمكنني الحصول على الدعم الفني؟**  
ج: للحصول على الدعم الفني، زر [منتدى Aspose.CAD](https://forum.aspose.com/c/cad/19).

---

**آخر تحديث:** 2026-03-21  
**تم الاختبار مع:** Aspose.CAD 24.11 لـ .NET  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}