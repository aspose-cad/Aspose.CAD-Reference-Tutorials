---
date: 2026-04-06
description: تعلم كيفية تحويل DWF إلى JPG في C# باستخدام Aspose.CAD واكتشف كيفية استخراج
  حجم تخطيط DWF من ملفات DWG.
keywords:
- convert dwf to jpg
- how to extract dwf
- convert dwg to jpg
linktitle: العمل مع ملفات DWG في C# - الحصول على حجم تخطيط DWF
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: تحويل DWF إلى JPG في C# – الحصول على حجم تخطيط DWF من DWG
url: /ar/net/dwg-file-manipulation/get-size-of-dwf-layout/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تحويل DWF إلى JPG في C# – الحصول على حجم تخطيط DWF من DWG

## مقدمة

إذا كنت بحاجة إلى **تحويل DWF إلى JPG** مع معرفة أبعاد التخطيط الدقيقة، فأنت في المكان الصحيح. في هذا البرنامج التعليمي سنستعرض مثالًا كاملاً من البداية إلى النهاية يستخدم Aspose.CAD for .NET لفتح ملف DWF مشتق من DWG، قراءة حجم كل تخطيط، وحفظ التخطيط كصورة JPG عالية الجودة. في النهاية لن تعرف فقط كيفية استخراج معلومات تخطيط DWF بل ستحصل أيضًا على مقطع شفرة قابل لإعادة الاستخدام يمكنك إدراجه في أي مشروع C#.

## إجابات سريعة
- **ماذا يعني “تحويل DWF إلى JPG”؟** يعني تحويل تخطيط DWF المتجه إلى صورة bitmap بصيغة JPEG.  
- **لماذا قراءة حجم التخطيط أولاً؟** معرفة الأبعاد الدقيقة تتيح لك ضبط أبعاد الصفحة بشكل صحيح، مما يجنب التشويه أو القطع في الناتج.  
- **أي مكتبة تتعامل مع ذلك؟** Aspose.CAD for .NET توفر دعمًا كاملاً لـ DWG و DWF وتحويل الصور النقطية.  
- **هل أحتاج إلى ترخيص؟** الترخيص المؤقت يكفي للتقييم؛ الترخيص الكامل مطلوب للإنتاج.  
- **ما إصدارات .NET المدعومة؟** .NET Framework 4.5+، .NET Core 3.1+، .NET 5/6/7.

## ما هو “تحويل DWF إلى JPG” ولماذا هو مهم؟

تحويل ملف DWF (Design Web Format) إلى JPG يخلق صورة محمولة يمكن عرضها في المتصفحات، تضمينها في التقارير، أو مشاركتها مع أصحاب المصلحة الذين لا يمتلكون برنامج CAD. يمنحك التحويل أيضًا المرونة لمعالجة الصورة (تغيير الحجم، الضغط، إضافة علامة مائية) باستخدام أدوات معالجة الصور القياسية.

## لماذا استخراج حجم تخطيط DWF؟

يمكن أن يحتوي ملف DWF على تخطيطات متعددة، كل منها بنظام إحداثيات ووحدات خاصة (بوصة، ملليمتر، إلخ). استخراج حجم التخطيط يتيح لك:

1. الحفاظ على نسبة العرض إلى الارتفاع الأصلية عند التحويل إلى نقطية.  
2. اختيار DPI المناسب لإخراج عالي الدقة.  
3. أتمتة معالجة دفعات متعددة من التخطيطات دون تعديل يدوي.

## المتطلبات المسبقة

للمتابعة بسلاسة، تأكد من توفر المتطلبات التالية:

- Aspose.CAD for .NET: تأكد من تثبيت Aspose.CAD for .NET. يمكنك تنزيله من [صفحة تنزيل Aspose.CAD for .NET](https://releases.aspose.com/cad/net/).

وجود المكتبة جاهزة يعني أنك تستطيع التركيز على الشفرة بدلاً من البحث عن التبعيات.

## استيراد مساحات الأسماء

قبل بدء الترميز، استورد مساحات الأسماء المطلوبة. هذه توفر الفئات التي سنحتاجها للعمل مع ملفات CAD، خيارات التحويل النقطي، وإدخال/إخراج الملفات.

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

## الخطوة 1: إعداد بيئتك

أنشئ مشروع C# جديد من نوع console أو class‑library، أضف مرجعًا إلى **Aspose.CAD.dll**، وتأكد من أن المشروع يستهدف نسخة .NET متوافقة.

## الخطوة 2: تعريف مسارات الملفات (كيفية استخراج DWF)

حدد مكان وجود ملف DWF المصدر ومكان كتابة ملفات JPG الناتجة.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "blocks_and_tables.dwf";
```

> **نصيحة احترافية:** استخدم `Path.Combine(MyDir, "blocks_and_tables.dwf")` لمعالجة المسارات بأمان على أنظمة تشغيل مختلفة.

## الخطوة 3: تحميل صورة DWF

حمّل ملف DWF في كائن `Aspose.CAD.Image`. نقوم بتحويله إلى `DwfImage` لأننا نحتاج إلى الوصول إلى خصائص الصفحة المحددة.

```csharp
using (DwfImage image = (DwfImage)Aspose.CAD.Image.Load(sourceFilePath))
{
    // Code for further steps will go here
}
```

## الخطوة 4: التكرار عبر الصفحات

يمكن أن يحتوي DWF على عدة صفحات (تخطيطات). قم بالتكرار عبر كل واحدة لمعالجتها بشكل فردي.

```csharp
foreach (var page in image.Pages)
{
    // Code for further steps will go here
}
```

## الخطوة 5: الحصول على معلومات التخطيط

داخل الحلقة، استخرج اسم التخطيط. سيُستخدم هذا الاسم لكل من التسجيل وتسمية ملف JPG الناتج.

```csharp
var layout = page.Name;
System.Console.WriteLine("Layout= " + layout);
```

## الخطوة 6: إعداد خيارات JPG

أنشئ مثيلًا من `JpegOptions` وقم بتكوين خيارات التحويل النقطي. الخاصية `Layouts` تخبر Aspose.CAD أي تخطيط يجب عرضه.

```csharp
using (FileStream fs = new FileStream(MyDir + "layout_" + layout + ".jpg", FileMode.Create))
{
    JpegOptions jpegOptions = new JpegOptions();
    CadRasterizationOptions options = new CadRasterizationOptions();
    options.Layouts = new string[] { layout };
    // Code for further steps will go here
}
```

## الخطوة 7: تحديد حجم الصفحة (تحويل dwg إلى jpg)

احسب عرض وارتفاع التخطيط بوحداته الأصلية. هذه المعلومات أساسية لضبط حجم الصفحة النقطية بشكل صحيح.

```csharp
double sizeExtX = page.MaxPoint.X - page.MinPoint.X;
double sizeExtY = page.MaxPoint.Y - page.MinPoint.Y;
// Code for further steps will go here
```

## الخطوة 8: إعداد أبعاد الصفحة

حوّل الوحدات الأصلية (بوصة أو ملليمتر) إلى بكسل باستخدام الطرق المساعدة التي توفرها Aspose.CAD. إذا لم يكن نوع الوحدة أحدهما، نعود إلى القيم الخام.

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

## الخطوة 9: حفظ ملف JPG

أخيرًا، اربط خيارات التحويل النقطي بخيارات JPEG واحفظ الصورة على القرص.

```csharp
jpegOptions.VectorRasterizationOptions = options;
image.Save(fs, jpegOptions);
}
```

عند انتهاء الحلقة، ستحصل على ملف JPG لكل تخطيط، كلٌ بحجم يطابق تمامًا أبعاد DWF الأصلية.

## المشكلات الشائعة والحلول

| العَرَض | السبب المحتمل | الحل |
|---------|--------------|-----|
| إخراج JPG فارغ | `options.Layouts` غير مُضبط بشكل صحيح | تحقق من أن اسم التخطيط يطابق `page.Name`. |
| صورة مشوهة | تحويل DPI غير صحيح | استخدم `CommonHelper.DPI = 300` (أو DPI المستهدف) قبل التحويل. |
| الملف غير موجود | مسار `MyDir` غير صحيح | استخدم مسارات مطلقة أو `Path.Combine`. |
| استثناء الترخيص | لم يتم تطبيق ترخيص | حمّل ترخيصًا مؤقتًا أو دائمًا قبل استدعاء `Image.Load`. |

## الأسئلة المتكررة

### س1: هل Aspose.CAD متوافق مع أحدث صيغ ملفات DWG؟

ج1: Aspose.CAD يدعم صيغ DWG المتعددة، بما في ذلك أحدث الإصدارات. راجع [الوثائق](https://reference.aspose.com/cad/net/) للحصول على تفاصيل التوافق المحددة.

### س2: هل يمكنني استخدام Aspose.CAD للمشاريع التجارية والشخصية؟

ج2: نعم، Aspose.CAD يقدم خيارات ترخيص مرنة للاستخدام التجاري والشخصي. زر [صفحة الشراء](https://purchase.aspose.com/buy) للمزيد من التفاصيل.

### س3: كيف يمكنني الحصول على ترخيص مؤقت لـ Aspose.CAD؟

ج3: يمكنك الحصول على ترخيص مؤقت من [هنا](https://purchase.aspose.com/temporary-license/) لأغراض التقييم.

### س4: أين يمكنني العثور على الدعم لـ Aspose.CAD؟

ج4: لأي استفسارات أو مساعدة، زر [منتدى Aspose.CAD](https://forum.aspose.com/c/cad/19).

### س5: هل هناك نسخة تجريبية مجانية لـ Aspose.CAD؟

ج5: نعم، يمكنك الوصول إلى نسخة تجريبية مجانية من Aspose.CAD [هنا](https://releases.aspose.com/).

### س6: كيف يمكنني تحويل ملف DWG مباشرة إلى JPG دون استخراج DWF أولاً؟

ج6: يمكنك تحميل ملف DWG باستخدام `Aspose.CAD.Image.Load` واستخدام نفس سير عمل التحويل النقطي؛ فقط اضبط `options.Layouts` إلى اسم(أسماء) التخطيط المطلوبة من DWG.

### س7: هل يحافظ التحويل على جودة المتجه؟

ج7: بمجرد تحويله إلى JPG، تصبح الصورة قائمة على البتات، لذا تُفقد قابلية التكبير المتجهية. للحصول على تكبير بدون فقدان الجودة، فكر في التصدير إلى PNG أو SVG بدلاً من ذلك.

---

**آخر تحديث:** 2026-04-06  
**تم الاختبار مع:** Aspose.CAD 24.11 for .NET  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}