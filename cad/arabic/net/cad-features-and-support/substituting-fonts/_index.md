---
date: 2026-03-29
description: تعلم كيفية استبدال الخطوط في Aspose.CAD لـ .NET بسرعة. يوضح لك هذا الدليل
  خطوة بخطوة كيفية تعيين اسم الخط الأساسي وتخصيص رسومات CAD بفعالية.
linktitle: Substituting Fonts
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: كيفية استبدال الخطوط في Aspose.CAD لـ .NET
url: /ar/net/cad-features-and-support/substituting-fonts/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية استبدال الخطوط في Aspose.CAD لـ .NET

## المقدمة

في عالم تطوير CAD باستخدام .NET، يعتبر تعلم **كيفية استبدال الخطوط** مهارة حاسمة يمكنها تحسين جودة الرسومات بشكل كبير. تقدم Aspose.CAD لـ .NET واجهة برمجة تطبيقات بسيطة تتيح لك **تعيين اسم الخط الأساسي** لأي نمط، مما يجعل استبدال الخطوط عالميًا أو انتقائيًا أمرًا سهلًا. في هذا البرنامج التعليمي سنستعرض العملية بالكامل—من تحميل الرسم إلى استبدال الخطوط إما عالميًا أو حسب اسم النمط المحدد.

## إجابات سريعة
- **ما هي الفئة الرئيسية لمعالجة CAD؟** `Aspose.CAD.Image` (or its derived `CadImage`).
- **أي خاصية تغير الخط؟** `PrimaryFontName` on `CadStyleTableObject`.
- **هل يمكنني استبدال الخطوط لجميع الأنماط مرة واحدة؟** نعم، iterate through `cadImage.Styles` and set the property.
- **هل أحتاج إلى ترخيص للإنتاج؟** يتطلب ترخيص Aspose.CAD صالح للاستخدام غير التجريبي.
- **الإصدارات المدعومة من .NET؟** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.

## ما هو استبدال الخطوط في CAD؟
يعني استبدال الخطوط استبدال الخط الأصلي المستخدم في رسم CAD بخط آخر متوفر على النظام الهدف. يكون هذا مفيدًا بشكل خاص عندما يكون الخط الأصلي مفقودًا، أو عندما تحتاج إلى نمط مؤسسي موحد، أو عند إعداد الرسومات للطباعة على أجهزة تدعم مجموعة محدودة من الخطوط.

## لماذا استبدال الخطوط باستخدام Aspose.CAD؟
- **لا توجد تبعيات خارجية** – المكتبة تتعامل مع تعيين الخطوط داخليًا.
- **تعمل مع صيغ متعددة** – DXF, DWG, DGN, وغيرها.
- **تحكم برمجي** – أتمتة العملية للتحويلات الدفعية أو خطوط أنابيب CI.
- **يحافظ على هندسة الرسم** – فقط تمثيل النص البصري يتغير.

## المتطلبات المسبقة

- معرفة أساسية ببرمجة .NET.
- تم تثبيت Aspose.CAD لـ .NET. إذا لم تقم بتثبيته بعد، قم بتحميله [هنا](https://releases.aspose.com/cad/net/).
- ملف رسم CAD (DXF, DWG, إلخ) للتجربة.

## استيراد مساحات الأسماء

قبل البدء، استورد مساحات الأسماء الضرورية للوصول إلى وظائف Aspose.CAD في تطبيق .NET الخاص بك.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad.CadTables;
```

## الخطوة 1: تحميل رسم CAD

ابدأ بتحميل رسم CAD إلى كائن من نوع `CadImage`. تأكد من توفير المسار الصحيح إلى دليل المستندات الخاص بك.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

using (CadImage cadImage = (CadImage)Aspose.CAD.Image.Load(sourceFilePath))
{
    // Your code for further actions goes here
}
```

## الخطوة 2: التكرار عبر الأنماط

بعد ذلك، قم بالتكرار عبر الأنماط في رسم CAD باستخدام حلقة `foreach`. يتيح لك ذلك الوصول إلى أنماط الخط الفردية وتعديلها.

```csharp
foreach (CadStyleTableObject style in cadImage.Styles)
{
    // Your code for style manipulation goes here
}
```

## كيفية تعيين اسم الخط الأساسي لاستبدال الخطوط

خاصية `PrimaryFontName` على كل `CadStyleTableObject` تتحكم في الخط المستخدم عند عرض الرسم. من خلال تعيين هذه الخاصية، تقوم فعليًا باستبدال الخط الأصلي.

### الخطوة 3: استبدال الخطوط عالميًا

لإستبدال الخطوط لجميع الأنماط **جميع**، قم بتعيين خاصية `PrimaryFontName` لكل نمط إلى اسم الخط المطلوب، على سبيل المثال، `"Arial"`.

```csharp
foreach (CadStyleTableObject style in cadImage.Styles)
{
    style.PrimaryFontName = "Arial";
}
```

### الخطوة 4: استبدال الخط حسب اسم النمط

إذا كنت بحاجة فقط إلى استبدال الخط لنمط محدد (مثلاً، النمط المسمى `"Roman"`)، أضف شرطًا شرطيًا داخل الحلقة.

```csharp
foreach (CadStyleTableObject style in cadImage.Styles)
{
    if (style.StyleName == "Roman")
    {
        style.PrimaryFontName = "Arial";
    }
}
```

## المشكلات الشائعة & استكشاف الأخطاء

| المشكلة | السبب | الحل |
|-------|-------|-----|
| الخط لا يتغير بعد تشغيل الكود | الرسم مخزن مؤقتًا أو مفتوح في وضع القراءة فقط | تأكد من حفظ الصورة بعد التعديل (`cadImage.Save(...)`) أو أعد تحميل الملف للتحقق. |
| الخط المطلوب غير موجود على النظام | الخط غير مثبت على الجهاز الذي يشغل الكود | قم بتثبيت الخط TrueType/OpenType المطلوب أو دمجه في موارد التطبيق. |
| النص يظهر مشوهًا | ترميز غير صحيح أو عدم وجود دعم Unicode | استخدم خطًا يدعم مجموعة الأحرف المطلوبة (مثلاً، Arial Unicode MS). |

## الأسئلة المتكررة

**س: هل يمكنني استرجاع تغييرات الخط في Aspose.CAD لـ .NET؟**  
ج: نعم، يمكنك الاسترجاع عن طريق إعادة تحميل رسم CAD الأصلي أو عن طريق الاحتفاظ بنسخة احتياطية قبل إجراء التعديلات.

**س: هل هناك خصائص خطوط أخرى يمكنني تعديلها؟**  
ج: بالطبع. بجانب `PrimaryFontName`، يمكنك العمل مع `SecondaryFontName`، `FontFamily`، وغيرها من السمات المتعلقة بالأنماط للتخصيص المتقدم.

**س: هل Aspose.CAD متوافق مع صيغ CAD المختلفة؟**  
ج: نعم، يدعم Aspose.CAD مجموعة واسعة من الصيغ مثل DXF، DWG، DGN، DWF، وغيرها، مما يمنحك مرونة عبر المشاريع.

**س: هل يمكنني أتمتة استبدال الخطوط في المعالجة الدفعية؟**  
ج: بالتأكيد. ضع منطق التحميل والاستبدال داخل حلقة تتكرر على مجلد من ملفات CAD، أو دمجه في خط أنابيب CI/CD.

**س: أين يمكنني العثور على دعم إضافي لـ Aspose.CAD لـ .NET؟**  
ج: للحصول على دعم إضافي ومناقشات المجتمع، زر [منتدى Aspose.CAD](https://forum.aspose.com/c/cad/19).

---

**آخر تحديث:** 2026-03-29  
**تم الاختبار مع:** Aspose.CAD لـ .NET (أحدث إصدار)  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}