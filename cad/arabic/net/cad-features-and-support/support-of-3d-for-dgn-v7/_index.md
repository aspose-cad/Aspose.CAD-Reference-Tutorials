---
date: 2026-03-29
description: تعلم كيفية تكوين خيارات تحويل CAD إلى نقطية وتصدير ملفات DGN إلى PDF
  مع دعم ثلاثي الأبعاد باستخدام Aspose.CAD لـ .NET.
linktitle: Support of 3D for DGN V7
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: تكوين خيارات تحويل CAD إلى نقطية لإصدار DGN V7 ثلاثي الأبعاد
url: /ar/net/cad-features-and-support/support-of-3d-for-dgn-v7/
weight: 20
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تكوين خيارات تمثيل CAD النقطية لملف DGN V7 ثلاثي الأبعاد

## مقدمة

في هذا الدرس الشامل ستتعلم **كيفية تكوين خيارات تمثيل CAD النقطية** لتصدير ملف DGN V7 ثلاثي الأبعاد إلى PDF باستخدام Aspose.CAD لـ .NET. سواءً كنت تبني عارض CAD، أو أداة تقارير، أو خط أنابيب تحويل آلي، فإن إتقان هذه الإعدادات يمنحك تحكمًا دقيقًا في حجم الصفحة، وتكبير التخطيط، وألوان الخلفية، والعروض المحددة التي تريد تصييرها. دعنا نتبع العملية خطوة بخطوة.

## إجابات سريعة
- **ماذا يعني “configure CAD rasterization options”?**  
  إنه يشير إلى ضبط الخصائص مثل أبعاد الصفحة، والتكبير، ولون الخلفية، واختيار التخطيط قبل تحويل ملف CAD إلى تنسيق نقطي (مثل PDF).
- **كيف يتم تصدير DGN إلى PDF مع دعم ثلاثي الأبعاد؟**  
  حمّل ملف DGN باستخدام `DgnImage`، عرّف `PdfOptions` + `CadRasterizationOptions`، ثم استدعِ `Save`.
- **هل أحتاج إلى ترخيص للاستخدام في الإنتاج؟**  
  نعم – يلزم ترخيص تجاري للنشر؛ يتوفر إصدار تجريبي مجاني.
- **ما إصدارات .NET المدعومة؟**  
  .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.
- **هل يمكنني اختيار عروض محددة للتصدير؟**  
  بالطبع – اضبط مصفوفة `Layouts` في خيارات التمثيل النقطي.

## ما هو “configure CAD rasterization options”؟

يعني تكوين خيارات تمثيل CAD النقطية تخصيص طريقة تمثيل رسمة CAD (تحويلها من متجه إلى صورة نقطية أو PDF). من خلال ضبط هذه الإعدادات تتحكم في المخرجات البصرية، والأداء، وحجم الملف للوثيقة الناتجة.

## لماذا تستخدم Aspose.CAD لتصدير DGN V7 ثلاثي الأبعاد؟

- **تكامل كامل مع .NET** – لا حاجة إلى COM أو DLLs أصلية.  
- **يدعم الهندسة ثلاثية الأبعاد** – يحتفظ بمعلومات العمق عند التمثيل إلى PDF.  
- **تحكم دقيق** – اختر التخطيطات الدقيقة، والتكبير، وألوان الخلفية.  
- **متعدد المنصات** – يعمل على Windows وLinux وmacOS مع .NET Core.

## المتطلبات المسبقة

قبل أن تبدأ، تأكد من أن لديك:

- **Aspose.CAD لـ .NET** – قم بتنزيله من [here](https://releases.aspose.com/cad/net/).  
- **Visual Studio** أو أي بيئة تطوير .NET متوافقة.  
- **ملف DGN تجريبي** – سنستخدم في هذا الدليل `Nikon_D90_Camera.dgn` (موجود في حزمة عينات Aspose).  

الآن بعد أن كل شيء جاهز، دعنا نغوص في الشيفرة.

## استيراد مساحات الأسماء

في مشروع .NET الخاص بك، استورد مساحات الأسماء المطلوبة:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Dgn;
using Aspose.CAD.ImageOptions;
```

## الخطوة 1: إعداد دليل المستند الخاص بك

أنشئ متغيرًا يشير إلى المجلد الذي سيحتوي على ملف DGN المصدر وملفات الإخراج.

```csharp
string MyDir = "Your Document Directory";
```

## الخطوة 2: تحميل ملف DGN

حمّل ملف DGN كـ `DgnImage`. هذا الكائن يتيح لك الوصول إلى بيانات CAD وسلسلة تمثيل النقطية.

```csharp
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";
string outFile = MyDir + "Nikon_D90_Camera.dgn";

using (DgnImage dgnImage = (DgnImage)Image.Load(sourceFilePath))
{
    // Your code for further processing goes here
}
```

## الخطوة 3: تكوين خيارات تصدير PDF (Configure CAD Rasterization Options)

هنا نقوم **بتكوين خيارات تمثيل CAD النقطية** التي تحدد كيفية تمثيل النموذج ثلاثي الأبعاد إلى PDF. يمكنك تعديل حجم الصفحة، وتمكين تكبير التخطيط التلقائي، وتعيين لون الخلفية، واختيار التخطيطات (العروض) الدقيقة التي تريد تصديرها.

```csharp
var options = new PdfOptions
{
    VectorRasterizationOptions = new CadRasterizationOptions
    {
        PageWidth = 1500,
        PageHeight = 1500,
        AutomaticLayoutsScaling = true,
        BackgroundColor = Color.Black,
        Layouts = new string[] { "1", "2", "3", "9" } // Only export specified views
    }
};
```

## الخطوة 4: حفظ الصورة النقطية

أخيرًا، صدّر ملف DGN إلى ملف PDF باستخدام الخيارات التي قمت بتكوينها للتو.

```csharp
dgnImage.Save(outFile, options);
```

## المشكلات الشائعة والحلول

| المشكلة | الحل |
|-------|----------|
| **إخراج PDF فارغ** | تحقق من أن مصفوفة `Layouts` تحتوي على معرفات العروض الصحيحة الموجودة في ملف DGN. |
| **ألوان غير صحيحة** | تأكد من ضبط `BackgroundColor` على القيمة المطلوبة؛ استخدم `Color.White` لخلفية فاتحة. |
| **عنق زجاجة في الأداء على الملفات الكبيرة** | فعّل `AutomaticLayoutsScaling` وفكّر في تقليل `PageWidth/PageHeight` للحصول على دقة نقطية أصغر. |
| **استثناء الترخيص** | قم بتثبيت ترخيص Aspose.CAD صالح قبل تحميل الصورة لتجنب علامات مائية تجريبية. |

## الأسئلة المتكررة

**س: هل يمكنني استخدام Aspose.CAD لـ .NET مع صيغ ملفات CAD أخرى؟**  
ج: نعم، يدعم Aspose.CAD صيغ DWG, DXF, DWF, DGN، والعديد من الصيغ الأخرى.

**س: كيف يمكنني معالجة الاستثناءات عند العمل مع Aspose.CAD؟**  
ج: ضع الشيفرة داخل كتلة `try‑catch` وتفحص `Aspose.CAD.CADException` للحصول على معلومات تفصيلية عن الخطأ.

**س: هل Aspose.CAD مناسب للمشاريع التجارية؟**  
ج: بالتأكيد. يمكنك شراء ترخيص من [here](https://purchase.aspose.com/buy).

**س: هل يمكنني تجربة Aspose.CAD لـ .NET قبل الشراء؟**  
ج: نعم، يتوفر إصدار تجريبي مجاني [here](https://releases.aspose.com/).

**س: أين يمكنني العثور على دعم المجتمع لـ Aspose.CAD؟**  
ج: انضم إلى منتدى المناقشة [here](https://forum.aspose.com/c/cad/19).

---

**آخر تحديث:** 2026-03-29  
**تم الاختبار مع:** Aspose.CAD 24.11 لـ .NET  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}