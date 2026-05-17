---
date: 2026-03-24
description: تعلم كيفية تحويل DGN إلى PNG وحفظ CAD كـ JPEG باستخدام Aspose.CAD لـ
  .NET – دليل سريع لتحويل CAD إلى صورة.
linktitle: Export DGN to Raster Image
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: كيفية تحويل DGN إلى PNG في Aspose.CAD لـ .NET
url: /ar/net/cad-export-formats/export-dgn-to-raster-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تحويل DGN إلى PNG في Aspose.CAD لـ .NET

في تطوير .NET الحديث، **convert dgn to png** هو طلب شائع عندما تحتاج إلى عرض رسومات CAD على الويب أو تضمينها في التقارير. تجعل Aspose.CAD لـ .NET هذه التحويلة بسيطة، حيث تسمح لك بتحويل ملف DGN إلى صورة نقطية عالية الجودة ببضع أسطر من الشيفرة فقط. في هذا الدليل سنستعرض العملية بالكامل، من إعداد المشروع إلى حفظ ملف PNG النهائي (أو JPEG).

## إجابات سريعة
- **هل يمكنني تحويل DGN إلى PNG باستخدام Aspose.CAD؟** نعم – فقط قم بتكوين خيارات التحويل واختر إخراج PNG أو JPEG.  
- **هل أحتاج إلى ترخيص للاستخدام في الإنتاج؟** يتطلب ترخيص Aspose.CAD صالح للنشر غير التجريبي.  
- **ما إصدارات .NET المدعومة؟** .NET Framework 4.6+، .NET Core 3.1+، .NET 5/6/7.  
- **ما صيغ الصور المتاحة؟** PNG، JPEG، BMP، GIF، TIFF، وأكثر.  
- **هل معالجة الاستثناءات ضرورية؟** بالتأكيد – غلف عملية التحويل داخل try/catch للتعامل مع مشاكل الوصول إلى الملفات.

## ما هو “convert dgn to png”؟
تحويل ملف DGN (MicroStation) إلى PNG يعني تحويل بيانات CAD المتجهة إلى صورة مبنية على البكسل. هذا مفيد لإنشاء معاينات، تضمين الرسومات في رسائل بريد HTML، أو إنشاء صور مصغرة لأنظمة إدارة المستندات.

## لماذا نستخدم Aspose.CAD لتحويل CAD إلى صورة؟
- **لا توجد تبعيات خارجية** – يعمل بالكامل في الكود المُدار.  
- **دقة عالية** – يحافظ على سماكات الخطوط، الطبقات، والألوان.  
- **إخراج مرن** – يمكن التبديل بين PNG، JPEG، BMP، إلخ، بتغيير خيار واحد.  
- **محسن للأداء** – عملية التحويل سريعة حتى للرسومات الكبيرة.

## المتطلبات المسبقة

قبل أن نبدأ، تأكد من أن لديك:

- **Aspose.CAD for .NET** مثبتًا في مشروعك. يمكنك تنزيله من [الموقع الإلكتروني](https://reference.aspose.com/cad/net/).  
- ملف DGN تجريبي (مثلاً `Nikon_D90_Camera.dgn`) موجود في دليل معروف.

## استيراد المساحات الاسمية

ابدأ بإضافة عبارات `using` المطلوبة حتى تتمكن من الوصول إلى فئات Aspose.CAD.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## الخطوة 1: تحميل ملف DGN

حمّل ملف DGN المصدر في كائن `CadImage`. هذا الكائن يمثل رسم CAD في الذاكرة وسيكون المصدر لعملية التحويل.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Your code for further processing goes here
}
```

## الخطوة 2: تعريف خيارات التحويل

قم بتكوين كيفية تحويل رسم CAD إلى صورة نقطية. يمكنك التحكم في حجم الصورة، المقياس، ولون الخلفية هنا.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 600;
rasterizationOptions.PageHeight = 300;
rasterizationOptions.NoScaling = true;
rasterizationOptions.AutomaticLayoutsScaling = false;
```

## الخطوة 3: اختيار صيغة الإخراج (PNG أو JPEG)

على الرغم من أن الشرح يركز على PNG، قد ترغب أيضًا في **save cad as jpeg**. أنشئ كائن خيارات الصورة المناسب وأرفق إعدادات التحويل.

```csharp
ImageOptionsBase options = new JpegOptions();   // Change to PngOptions() for PNG output
options.VectorRasterizationOptions = rasterizationOptions;
```

> **نصيحة احترافية:** لإنشاء ملف PNG، استبدل `new JpegOptions()` بـ `new PngOptions()`.

## الخطوة 4: حفظ الصورة النقطية

أخيرًا، استدعِ `Save` على مثيل `CadImage`، مع توفير اسم الملف المطلوب وكائن الخيارات الذي قمت بتكوينه.

```csharp
cadImage.Save(MyDir + "ExportDGNToRasterImage_out.jpg", options);
```

إذا قمت بالتبديل إلى `PngOptions`، سيتم حفظ الملف باسم `ExportDGNToRasterImage_out.png`.

## المشكلات الشائعة والحلول

| المشكلة | السبب | الحل |
|-------|-------|-----|
| **Blank output image** | `NoScaling` تم تعيينه بشكل غير صحيح أو لم يتم اختيار التخطيط | قم بتعيين `AutomaticLayoutsScaling = true` أو حدد التخطيط المطلوب. |
| **Out‑of‑memory for large files** | تحميل ملف DGN كبير دون استخدام البث | استخدم `Image.Load(sourceFilePath, new LoadOptions { LoadOnDemand = true })`. |
| **Unsupported DGN version** | إصدارات MicroStation القديمة | تأكد من أنك تستخدم أحدث نسخة من Aspose.CAD التي تدعم الصيغ القديمة. |

## الأسئلة المتكررة

**س: هل يمكنني تصدير ملفات DGN إلى صيغ غير JPEG؟**  
**ج:** نعم، يدعم Aspose.CAD لـ .NET صيغ PNG، BMP، GIF، TIFF، وأكثر – فقط استبدل فئة الخيارات (مثلاً `new PngOptions()`).

**س: كيف يجب أن أتعامل مع الاستثناءات أثناء التحويل؟**  
**ج:** غلف كود التحويل داخل كتلة `try/catch` وسجّل `Aspose.CAD.CadException` للحصول على معلومات تفصيلية عن الخطأ.

**س: هل هناك نسخة تجريبية متاحة لـ Aspose.CAD لـ .NET؟**  
**ج:** نعم، يمكنك تجربة المنتج بنسخة تجريبية مجانية. زر [هنا](https://releases.aspose.com/) لمزيد من المعلومات.

**س: أين يمكنني طلب المساعدة أو مناقشة المشكلات المتعلقة بـ Aspose.CAD لـ .NET؟**  
**ج:** توجه إلى [منتدى Aspose.CAD](https://forum.aspose.com/c/cad/19) للحصول على دعم المجتمع والنقاشات.

**س: كيف أحصل على ترخيص مؤقت لـ Aspose.CAD لـ .NET؟**  
**ج:** زر [هذا الرابط](https://purchase.aspose.com/temporary-license/) للحصول على ترخيص مؤقت لاحتياجات التطوير الخاصة بك.

## الخلاصة

لقد تعلمت الآن كيفية **convert dgn to png** (أو JPEG) باستخدام Aspose.CAD لـ .NET. من خلال تعديل خيارات التحويل وتبديل فئة خيارات الصورة، يمكنك تخصيص الناتج ليتناسب مع أي متطلبات مشروع. لا تتردد في تجربة أحجام صفحات مختلفة، إعدادات DPI، وصيغ الملفات للحصول على الصورة النقطية المثالية لتطبيقك.

---

**آخر تحديث:** 2026-03-24  
**تم الاختبار مع:** Aspose.CAD 24.11 لـ .NET  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}