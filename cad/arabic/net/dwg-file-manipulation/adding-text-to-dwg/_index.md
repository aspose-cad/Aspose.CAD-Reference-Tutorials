---
date: 2026-04-06
description: تعلم كيفية تحويل ملفات DWG إلى PDF وإضافة نص مخصص باستخدام C# و Aspose.CAD.
  يغطي هذا الدليل خطوة بخطوة إنشاء PDF من DWG، وإدراج كيان نصي، وتغيير خط النص في
  DWG.
keywords:
- convert dwg to pdf
- generate pdf from dwg
- insert text entity
- change dwg text font
- aspose cad dwg pdf
linktitle: إضافة نص إلى ملفات DWG باستخدام C#
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: تحويل DWG إلى PDF وإضافة نص في C# – دليل Aspose.CAD
url: /ar/net/dwg-file-manipulation/adding-text-to-dwg/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تحويل DWG إلى PDF وإضافة نص في C# – دليل Aspose.CAD

## مقدمة

في عالم CAD وتطوير .NET المتسارع، **تحويل DWG إلى PDF** مع إدراج تعليقات مخصصة هو طلب شائع. سواء كنت بحاجة إلى إنشاء رسومات قابلة للطباعة للعملاء أو تضمين ملاحظات ديناميكية مباشرةً في DWG، تجعل Aspose.CAD المهمة سهلة. في هذا الدليل ستتعلم كيفية **تحويل DWG إلى PDF**، **إضافة كيان نصي**، وحتى **تغيير خط نص DWG** باستخدام C#.

## إجابات سريعة
- **ما هي المكتبة الأفضل لتحويل DWG‑to‑PDF؟** Aspose.CAD for .NET  
- **هل يمكنني إضافة نص مخصص أثناء التحويل؟** نعم – أنشئ كيان `CadText` وأضفه قبل الحفظ.  
- **هل أحتاج إلى ترخيص للاستخدام الإنتاجي؟** يلزم الحصول على ترخيص تجاري؛ يتوفر إصدار تجريبي مجاني.  
- **ما إصدارات .NET المدعومة؟** .NET Framework 4.5+، .NET Core 3.1+، .NET 5/6+.  
- **هل يمكن تغيير خط النص؟** نعم، عدّل خصائص `CadText` مثل `StyleType` و `TextHeight`.

## ما هو “convert dwg to pdf”؟

تحويل ملف DWG إلى PDF يحول رسم CAD قائم على المتجهات إلى مستند قابل للمشاركة على نطاق واسع ومستقل عن الجهاز. يحتفظ PDF بالهندسة الأصلية والطبقات، مع السماح لك بإدراج التعليقات التوضيحية أو النص أو بيانات تعريفية أخرى. تتولى Aspose.CAD عملية التحويل إلى نقطية والرسم المتجه تلقائيًا، لذا لا تحتاج إلى أي برنامج CAD من طرف ثالث على الخادم.

## لماذا نضيف نصًا إلى DWG قبل التحويل؟

إدراج النص مباشرةً في DWG يمنحك تحكمًا كاملًا في الموضع والتنسيق وتعيين الطبقة. عندما يتم تحويل الملف لاحقًا إلى PDF، يظهر النص بالضبط في الموضع الذي وضعته فيه، مما يحافظ على نية التصميم ويقضي على الحاجة إلى المعالجة اللاحقة في محرر PDF.

## المتطلبات المسبقة

- **مكتبة Aspose.CAD** – قم بتنزيلها من [download link](https://releases.aspose.com/cad/net/).  
- **بيئة .NET تعمل** (Visual Studio 2022، .NET 6، أو أي نسخة متوافقة).  
- **مجلد لملفات الاختبار** – سنشير إليه باسم `MyDir` طوال الدليل.

الآن، دعنا نتبع العملية خطوة بخطوة.

## استيراد مساحات الأسماء

أضف عبارات `using` المطلوبة حتى تتمكن من الوصول إلى فئات Aspose.CAD.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.FileFormats.Cad.CadConsts;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadObjects.AttEntities;
using Aspose.CAD.ImageOptions;
```

## الخطوة 1: تحميل ملف DWG

حمّل ملف DWG المصدر في كائن `Image`. يتيح لك هذا الكائن الوصول إلى الكيانات الأساسية في CAD.

```csharp
string dwgPathToFile = MyDir + "SimpleEntites.dwg";
using (Image image = Image.Load(dwgPathToFile))
{
    // Subsequent steps will be performed inside this block
}
```

## الخطوة 2: إنشاء كائن CadText (إدراج كيان نصي)

تمثل فئة `CadText` سطرًا واحدًا من النص في DWG. هنا نقوم بتعيين نمطه وقيمته ولونه وطبقةه وموقعه. عدّل `StyleType` أو `TextHeight` لت **تغيير خط نص DWG**.

```csharp
CadText cadText = new CadText();
cadText.StyleType = "Standard";          // Font/style – change to alter DWG text font
cadText.DefaultValue = "Some custom text";
cadText.ColorId = 256;                    // 256 = ByLayer (you can use a specific ACI color)
cadText.LayerName = "0";
cadText.FirstAlignment.X = 47.90;
cadText.FirstAlignment.Y = 5.56;
cadText.TextHeight = 0.8;                 // Height influences visual size
cadText.ScaleX = 0.0;
```

## الخطوة 3: إضافة كيان النص إلى مساحة النموذج

تحتوي مساحة نموذج DWG على معظم كائنات الرسم. بإضافة `CadText` إلى كتلة `*Model_Space`، يصبح النص جزءًا من الرسم.

```csharp
CadImage cadImage = (CadImage)image;
cadImage.BlockEntities["*Model_Space"].AddEntity(cadText);
```

## الخطوة 4: تكوين خيارات PDF (إنشاء PDF من DWG)

قم بإعداد خيارات التحويل إلى نقطية التي تتحكم في كيفية تحويل DWG إلى PDF. يمكنك تعديل حجم الصفحة، نوع الرسم، وتخطيط الصفحة.

```csharp
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.VectorRasterizationOptions = cadRasterizationOptions;
cadRasterizationOptions.DrawType = CadDrawTypeMode.UseObjectColor;
cadRasterizationOptions.PageHeight = 1600;
cadRasterizationOptions.PageWidth = 1600;
cadRasterizationOptions.Layouts = new string[] { "Model" };
```

## الخطوة 5: حفظ DWG المعدل كملف PDF

أخيرًا، صدّر الرسم المعدل. يتضمن ملف PDF الناتج النص المضاف حديثًا.

```csharp
image.Save(MyDir + "SimpleEntites_generated.pdf", pdfOptions);
```

> **نصيحة احترافية:** إذا كنت بحاجة إلى PDF بدقة أعلى، قم بزيادة `PageHeight` و `PageWidth` بصورة متناسبة.

## المشكلات الشائعة والحلول

| المشكلة | السبب | الحل |
|-------|--------|-----|
| النص لا يظهر في PDF | طبقة أو معرف لون خاطئ | تأكد من وجود `LayerName` وأن `ColorId` مضبوط على لون مرئي (مثلاً 7 للأبيض). |
| النص في غير موضعه | إحداثيات محاذاة غير صحيحة | تحقق من قيم `FirstAlignment.X/Y` بالنسبة لوحدات الرسم. |
| PDF فارغ | لم يتم ضبط خيارات التحويل إلى نقطية | اضبط `DrawType` إلى `UseObjectColor` أو `UseObjectLineWeight`. |

## الأسئلة المتكررة (الموجودة)

### س1: هل Aspose.CAD متوافق مع جميع إصدارات ملفات DWG؟

A1: يدعم Aspose.CAD مجموعة واسعة من إصدارات ملفات DWG، مما يضمن التوافق مع مختلف برامج CAD.

### س2: هل يمكنني إضافة عدة كيانات نصية إلى ملف DWG واحد باستخدام Aspose.CAD؟

A2: نعم، يمكنك إضافة عدة كيانات نصية إلى ملف DWG عن طريق تكرار العملية الموضحة في الدليل.

### س3: كيف يمكنني تغيير خط النص والنمط في Aspose.CAD؟

A3: لتعديل خط النص والنمط، عدّل خصائص كائن `CadText` قبل إضافته إلى ملف DWG.

### س4: هل هناك أي اعتبارات ترخيص لاستخدام Aspose.CAD في مشروع تجاري؟

A5: نعم، تأكد من الالتزام بشروط ترخيص Aspose.CAD. راجع [Aspose.CAD Purchase](https://purchase.aspose.com/buy) للتفاصيل.

### س5: أين يمكنني طلب المساعدة أو مناقشة الاستفسارات المتعلقة بـ Aspose.CAD؟

A5: زر [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) للتواصل مع المجتمع والحصول على الدعم.

## أسئلة إضافية

**س: كيف يمكنني إنشاء PDF من DWG دون إضافة نص؟**  
A: تخطى خطوة إنشاء `CadText` وقم مباشرةً بتكوين `PdfOptions` قبل استدعاء `image.Save(...)`.

**س: هل يمكنني تغيير لون النص برمجيًا؟**  
A: نعم، اضبط `cadText.ColorId` على رقم لون ACI محدد (مثلاً 1 للأحمر).

**س: هل يمكن إدراج نص متعدد الأسطر؟**  
A: استخدم `CadMText` لكتل النص المتعدد الأسطر؛ النهج مشابه لـ `CadText`.

**س: هل يدعم Aspose.CAD التحويل الجماعي لعدة ملفات DWG؟**  
A: بالتأكيد – قم بالتكرار عبر مجلد يحتوي على ملفات DWG، نفّذ نفس الخطوات، واحفظ كل ملف كـ PDF.

## الخلاصة

أصبح لديك الآن سير عمل كامل وجاهز للإنتاج **لتحويل DWG إلى PDF**، **إضافة نص مخصص**، و**تخصيص مظهر النص** باستخدام C# و Aspose.CAD. هذه التقنية مثالية لتوليد الرسومات تلقائيًا، خطوط تقارير، أو أي سيناريو يتطلب إغناء ملفات CAD في الوقت الفعلي.

---

**آخر تحديث:** 2026-04-06  
**تم الاختبار مع:** Aspose.CAD 24.11 for .NET  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}