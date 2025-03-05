---
title: العمل مع ملفات DWG في C# - احصل على حجم تخطيط DWF
linktitle: العمل مع ملفات DWG في C# - احصل على حجم تخطيط DWF
second_title: Aspose.CAD .NET - تنسيق ملف CAD وBIM
description: اكتشف قوة Aspose.CAD لـ .NET في التعامل مع ملفات DWG. تعلم كيفية استخراج أحجام تخطيطات DWF بسهولة باستخدام لغة C#.
type: docs
weight: 10
url: /ar/net/dwg-file-manipulation/get-size-of-dwf-layout/
---
## مقدمة

في مجال التصميم بمساعدة الكمبيوتر (CAD) وتطوير .NET، يمثل Aspose.CAD أداة قوية للتعامل مع ملفات DWG. سيرشدك هذا البرنامج التعليمي خلال عملية العمل مع ملفات DWG في لغة C# واستخراج حجم تخطيط DWF. قبل أن نتعمق في التعليمات البرمجية، دعونا نتأكد من إعداد كل شيء للبدء في هذه الرحلة.

## المتطلبات الأساسية

لمتابعة هذا البرنامج التعليمي بسلاسة، تأكد من توفر المتطلبات الأساسية التالية:

-  Aspose.CAD for .NET: تأكد من تثبيت Aspose.CAD for .NET. يمكنك تنزيله من[صفحة تنزيل Aspose.CAD لـ .NET](https://releases.aspose.com/cad/net/).

الآن بعد أن حصلت على الأدوات اللازمة، دعنا ننتقل إلى مجال البرمجة.

## استيراد مساحات الأسماء

قبل أن نبدأ العمل مع الكود، فلنستورد مساحات الأسماء المطلوبة:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Dwf;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
```

ستوفر مساحات الأسماء هذه الفئات والأساليب الأساسية للتعامل مع ملفات CAD باستخدام Aspose.CAD في تطبيق C# الخاص بك.

## الخطوة 1: إعداد بيئتك

ابدأ بالتأكد من أن لديك البيئة المناسبة التي تم إعدادها لمشروعك. قم بالرجوع إلى مكتبة Aspose.CAD في مشروع C# الخاص بك.

## الخطوة 2: تحديد مسارات الملفات

حدد المسارات لملف DWG الخاص بك ودليل الإخراج لملفات JPG التي تم إنشاؤها:

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "blocks_and_tables.dwf";
```

## الخطوة 3: قم بتحميل صورة DWF

قم بتحميل صورة DWF باستخدام Aspose.CAD:

```csharp
using (DwfImage image = (DwfImage)Aspose.CAD.Image.Load(sourceFilePath))
{
    // رمز لمزيد من الخطوات سوف تذهب هنا
}
```

## الخطوة 4: التكرار عبر الصفحات

قم بالتكرار عبر صفحات صورة DWF:

```csharp
foreach (var page in image.Pages)
{
    // رمز لمزيد من الخطوات سوف تذهب هنا
}
```

## الخطوة 5: الحصول على معلومات التخطيط

احصل على معلومات التخطيط من كل صفحة:

```csharp
var layout = page.Name;
System.Console.WriteLine("Layout= " + layout);
```

## الخطوة 6: إعداد خيارات JPG

قم بإعداد الخيارات لحفظ التخطيط كملف JPG:

```csharp
using (FileStream fs = new FileStream(MyDir + "layout_" + layout + ".jpg", FileMode.Create))
{
    JpegOptions jpegOptions = new JpegOptions();
    CadRasterizationOptions options = new CadRasterizationOptions();
    options.Layouts = new string[] { layout };
    // رمز لمزيد من الخطوات سوف تذهب هنا
}
```

## الخطوة 7: تحديد حجم الصفحة

تحديد حجم تخطيط DWF:

```csharp
double sizeExtX = page.MaxPoint.X - page.MinPoint.X;
double sizeExtY = page.MaxPoint.Y - page.MinPoint.Y;
// رمز لمزيد من الخطوات سوف تذهب هنا
```

## الخطوة 8: إعداد أبعاد الصفحة

قم بإعداد أبعاد الصفحة بناءً على نوع الوحدة:

```csharp
if (page.UnitType == UnitType.Inch)
{
    options.PageHeight = CommonHelper.INtoPixels(sizeExtY, CommonHelper.DPI);
    options.PageWidth = CommonHelper.INtoPixels(sizeExtX, CommonHelper.DPI);
}
else if (page.UnitType == UnitType.Millimeter)
{
    options.PageHeight = CommonHelper.MMtoPixels(sizeExtY, CommonHelper.DPI);
    options.PageWidth = CommonHelper.MMtoPixels(sizeExtX, CommonHelper.DPI);
}
else
{
    options.PageHeight = (float)sizeExtY;
    options.PageWidth = (float)sizeExtX;
}
```

## الخطوة 9: احفظ ملف JPG

احفظ ملف JPG بالخيارات المحددة:

```csharp
jpegOptions.VectorRasterizationOptions = options;
image.Save(fs, jpegOptions);
}
```

لقد نجحت الآن في استخراج حجم تخطيط DWF من ملف DWG باستخدام Aspose.CAD في C#. لا تتردد في استكشاف المزيد من الميزات والوظائف التي يقدمها Aspose.CAD لتطوير .NET.

## خاتمة

في هذا البرنامج التعليمي، تناولنا عملية العمل مع ملفات DWG في لغة C# باستخدام Aspose.CAD. باتباع هذه الخطوات، لا يمكنك الحصول على حجم تخطيط DWF فحسب، بل يمكنك أيضًا الاستفادة من إمكانات Aspose.CAD لمختلف المهام المتعلقة بـ CAD في مشاريع .NET الخاصة بك.

## الأسئلة الشائعة

### س1: هل يتوافق Aspose.CAD مع أحدث تنسيقات ملفات DWG؟

 A1: يدعم Aspose.CAD تنسيقات ملفات DWG المتنوعة، بما في ذلك أحدث الإصدارات. الرجوع إلى[توثيق](https://reference.aspose.com/cad/net/) للحصول على تفاصيل التوافق المحددة.

### س2: هل يمكنني استخدام Aspose.CAD لكل من المشاريع التجارية والشخصية؟

 ج2: نعم، يقدم Aspose.CAD خيارات ترخيص مرنة للاستخدام التجاري والشخصي. قم بزيارة[صفحة الشراء](https://purchase.aspose.com/buy) لمزيد من التفاصيل.

### س3: كيف يمكنني الحصول على ترخيص مؤقت لـ Aspose.CAD؟

 ج3: يمكنك الحصول على ترخيص مؤقت من[هنا](https://purchase.aspose.com/temporary-license/) لأغراض التقييم.

### س4: أين يمكنني العثور على الدعم لـ Aspose.CAD؟

ج4: لأية استفسارات أو مساعدة، قم بزيارة[منتدى Aspose.CAD](https://forum.aspose.com/c/cad/19).

### س5: هل هناك نسخة تجريبية مجانية متاحة لـ Aspose.CAD؟

 ج5: نعم، يمكنك الوصول إلى نسخة تجريبية مجانية من Aspose.CAD[هنا](https://releases.aspose.com/).