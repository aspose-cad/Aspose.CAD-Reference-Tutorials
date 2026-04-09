---
date: 2026-04-09
description: تعلم كيفية تحويل DWG إلى صورة وكيفية قراءة علامات التحتية باستخدام Aspose.CAD
  لـ .NET في هذا الدليل خطوة بخطوة.
keywords:
- convert dwg to image
- how to read underlay
- Aspose.CAD DWG underlay flags
linktitle: استكشاف أعلام التحتية لملفات DWG
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: تحويل DWG إلى صورة – استكشاف علامات التراكب لملفات DWG - دليل Aspose.CAD
url: /ar/net/dwg-file-manipulation/exploring-underlay-flags-of-dwg/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# استكشاف أعلام التراكب للملفات DWG - دليل Aspose.CAD

## مقدمة

إذا كنت تغوص في عالم ملفات CAD المعقد، وبشكل خاص ملفات DWG، وتريد **تحويل DWG إلى صورة** مع اكتشاف **كيفية قراءة أعلام التراكب**، فأنت في المكان الصحيح. يشرح هذا الدليل كل خطوة باستخدام مكتبة Aspose.CAD for .NET القوية، حتى تتمكن من استخراج معلومات التراكب وعرض الرسم كصورة بثقة.

## إجابات سريعة
- **ماذا يعني “convert DWG to image”؟**  
  يعني ذلك عرض رسم DWG بصيغة نقطية (PNG، JPEG، إلخ) باستخدام Aspose.CAD.
- **ما الطريقة التي تكشف عن أعلام التراكب؟**  
  الوصول إلى خاصية `Flags` لكائن `CadUnderlay` بعد تحميل ملف DWG.
- **هل أحتاج إلى ترخيص لـ Aspose.CAD؟**  
  يتوفر ترخيص مؤقت للتقييم؛ ويتطلب الترخيص الكامل للإنتاج.
- **ما إصدارات .NET المدعومة؟**  
  .NET Framework 4.6+، .NET Core 3.1+، .NET 5/6 وما بعده.
- **هل يمكنني استخراج هندسة التراكب؟**  
  نعم – مسار التراكب، نقطة الإدراج، المقياس، الدوران، وحالات الأعلام كلها قابلة للوصول.

## ما هو “convert DWG to image” ولماذا يهم؟

تحويل ملف DWG إلى صورة يتيح لك عرض رسومات CAD في المتصفحات، تضمينها في التقارير، أو مشاركتها مع أصحاب المصلحة الذين لا يمتلكون عارض CAD. أثناء العرض، غالبًا ما تحتاج إلى فحص كائنات **التراكب** (مثل مراجع DGN) لضمان ظهورها بشكل صحيح. فهم أعلام التراكب يساعدك على حل مشكلات القص، العرض بالأحادية اللون، ومشكلات الرؤية قبل إنشاء الصورة النهائية.

## المتطلبات المسبقة

- فهم أساسي للبرمجة بلغة C# و .NET.  
- مكتبة **Aspose.CAD for .NET** مثبتة. إذا لم تكن لديك بعد، قم بتنزيلها **[here](https://releases.aspose.com/cad/net/)**.  
- ملف DWG للاختبار – يتم استخدام ملف العينة **“BlockRefDgn.dwg”** طوال هذا الدليل.

## استيراد مساحات الأسماء

لبدء العمل، استورد مساحات الأسماء الضرورية:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## الخطوة 1: تحميل ملف DWG وتحويله إلى `CadImage`

أولاً، حمّل ملف DWG وحوله إلى كائن `CadImage`. هذا الكائن يمنحك الوصول إلى جميع كيانات الرسم، بما في ذلك التراكبات.

```csharp
string fileName = MyDir + "BlockRefDgn.dwg";

// Load DWG file and convert to CadImage
using (CadImage image = (CadImage)Image.Load(fileName))
{
    // Your code for subsequent steps will go here
}
```

## الخطوة 2: التكرار عبر الكيانات

بعد ذلك، قم بالتكرار عبر كل كيان في الرسم. هنا ستحدد مواقع كائنات التراكب.

```csharp
foreach (CadBaseEntity entity in image.Entities)
{
    // Your code for subsequent steps will go here
}
```

## الخطوة 3: التحقق من نوع `CadDgnUnderlay`

حدد كيانات التراكب عن طريق فحص نوعها في وقت التشغيل. تمثل فئة `CadDgnUnderlay` التراكبات DGN المدمجة في ملف DWG.

```csharp
if (entity is CadDgnUnderlay)
{
    // Your code for subsequent steps will go here
}
```

## الخطوة 4: الوصول إلى أعلام التراكب

بمجرد حصولك على كائن `CadDgnUnderlay`، قم بتحويله إلى `CadUnderlay` لقراءة خصائصه وحالات الأعلام. تخبرك الأعلام ما إذا كان التراكب مرئيًا، مقصوصًا، أو معروضًا بالأحادية اللون.

```csharp
CadUnderlay underlay = entity as CadUnderlay;

Console.WriteLine(underlay.UnderlayPath);
Console.WriteLine(underlay.UnderlayName);
Console.WriteLine(underlay.InsertionPoint.X);
Console.WriteLine(underlay.InsertionPoint.Y);
Console.WriteLine(underlay.RotationAngle);
Console.WriteLine(underlay.ScaleX);
Console.WriteLine(underlay.ScaleY);
Console.WriteLine(underlay.ScaleZ);
Console.WriteLine((underlay.Flags & UnderlayFlags.UnderlayIsOn) == UnderlayFlags.UnderlayIsOn);
Console.WriteLine((underlay.Flags & UnderlayFlags.ClippingIsOn) == UnderlayFlags.ClippingIsOn);
Console.WriteLine((underlay.Flags & UnderlayFlags.Monochrome) != UnderlayFlags.Monochrome);
```

### ما الذي يخبرك به الناتج

- **UnderlayPath / UnderlayName** – مكان وجود ملف DGN الخارجي.  
- **InsertionPoint (X, Y)** – الإحداثيات التي يُوضع فيها التراكب في مساحة DWG.  
- **RotationAngle** – زاوية الدوران المطبقة على التراكب.  
- **ScaleX / ScaleY / ScaleZ** – عوامل التحجيم لكل محور.  
- **Flags** – قيم منطقية تشير إلى الرؤية (`UnderlayIsOn`)، القص (`ClippingIsOn`)، والعرض بالأحادية اللون (`Monochrome`).

## المشكلات الشائعة والحلول

| Issue | Reason | Fix |
|-------|--------|-----|
| No output for flag checks | Underlay flags are defaulted to 0 when the underlay is turned off. | Ensure the DWG actually contains an active underlay or toggle visibility in the source CAD file. |
| `Invalid cast` exception | The entity is not a `CadDgnUnderlay`. | Verify the `if (entity is CadDgnUnderlay)` guard before casting. |
| Image rendering fails after flag extraction | Underlay may be clipped or turned off, leading to a blank area. | Adjust the flags (`UnderlayIsOn = true`, `ClippingIsOn = false`) before rendering the final image. |

## الأسئلة المتكررة

### س1: هل يمكنني استخدام Aspose.CAD for .NET مع صيغ ملفات CAD أخرى؟

A1: Aspose.CAD supports various CAD formats, including DWG, DXF, DGN, and more. Check the documentation for the full list.

### س2: هل يتوفر ترخيص مؤقت لـ Aspose.CAD for .NET؟

A2: Yes, you can obtain a temporary license **[here](https://purchase.aspose.com/temporary-license/)**.

### س3: أين يمكنني العثور على الدعم لـ Aspose.CAD for .NET؟

A3: Visit the support forum **[here](https://forum.aspose.com/c/cad/19)** for assistance.

### س4: كيف أشتري Aspose.CAD for .NET؟

A4: Purchase the library **[here](https://purchase.aspose.com/buy)**.

### س5: هل يتوفر نسخة تجريبية مجانية؟

A5: Yes, you can access the free trial **[here](https://releases.aspose.com/)**.

## الخلاصة

تهانينا! لقد تعلمت بنجاح **كيفية تحويل DWG إلى صورة** مع إتقان **كيفية قراءة أعلام التراكب** باستخدام Aspose.CAD for .NET. مع هذه المعرفة يمكنك:

- عرض رسومات DWG كصور نقطية للويب أو تقارير.  
- فحص وتعديل خصائص التراكب لضمان العرض الصحيح.  
- تصحيح مشكلات الرؤية، القص، والعرض بالأحادية اللون قبل إنشاء الصورة النهائية.

لا تتردد في استكشاف ميزات Aspose.CAD الأخرى مثل إدارة الطبقات، استخراج النص، والتحويل الجماعي لتوسيع سير عمل أتمتة CAD الخاص بك.

---

**آخر تحديث:** 2026-04-09  
**تم الاختبار مع:** Aspose.CAD for .NET 24.11  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}