---
title: أصبح التحويل من STL إلى PNG أمرًا سهلاً باستخدام Aspose.CAD لـ .NET
linktitle: تصدير ملفات STL إلى PNG
second_title: Aspose.CAD .NET - تنسيق ملف CAD وBIM
description: قم بتحويل ملفات STL إلى PNG بسهولة باستخدام Aspose.CAD لـ .NET. اتبع دليلنا خطوة بخطوة للتكامل السلس. التحميل الان!
type: docs
weight: 10
url: /ar/net/stl-file-export/exporting-stl-files-to-png/
---
## مقدمة
في عالم التصميم بمساعدة الكمبيوتر (CAD) الديناميكي، يعد التحويل الفعال للملفات أمرًا بالغ الأهمية. Aspose.CAD for .NET عبارة عن مجموعة أدوات قوية تعمل على تبسيط عملية تصدير ملفات STL إلى PNG، مما يوفر للمطورين المرونة والوظائف التي يحتاجون إليها. سيرشدك هذا البرنامج التعليمي خلال العملية خطوة بخطوة، مما يضمن الانتقال السلس من STL إلى PNG باستخدام Aspose.CAD.
## المتطلبات الأساسية
قبل أن نتعمق في البرنامج التعليمي، تأكد من أن لديك ما يلي:
1.  Aspose.CAD لـ .NET: قم بتنزيل وتثبيت مكتبة Aspose.CAD. يمكن ان تجدها[هنا](https://releases.aspose.com/cad/net/).
2. بيئة التطوير: قم بإعداد بيئة تطوير .NET المفضلة لديك.
3. ملف STL: احصل على ملف STL جاهز للتحويل. في هذا البرنامج التعليمي، سوف نستخدم ملف مثال يسمى "galeon.stl."
## استيراد مساحات الأسماء
لبدء العملية، قم باستيراد مساحات الأسماء الضرورية في تطبيق .NET الخاص بك. وهذا يضمن أن لديك إمكانية الوصول إلى الفئات والأساليب المطلوبة لتحويل STL إلى PNG.
```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```
## الخطوة 1: تحديد الدليل ومسار الملف المصدر
```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "galeon.stl";
```
تأكد من استبدال "دليل المستندات الخاص بك" بمسار الدليل الفعلي حيث يوجد ملف STL الخاص بك.
## الخطوة 2: قم بتحميل صورة CAD
```csharp
using (var cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // سيتم تنفيذ المزيد من الخطوات ضمن هذه الكتلة
}
```
تقوم هذه الخطوة بتحميل ملف STL كصورة CAD، مما يسمح لك بمعالجته وتصديره.
## الخطوة 3: تعيين خيارات التنقيط
```csharp
var rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 100;
rasterizationOptions.PageHeight = 100;
```
اضبط عرض الصفحة وارتفاعها وفقًا لتفضيلاتك ومتطلباتك. تحدد هذه الإعدادات أبعاد PNG المصدرة.
## الخطوة 4: تكوين خيارات PNG
```csharp
PngOptions pngOptions = new PngOptions();
pngOptions.VectorRasterizationOptions = rasterizationOptions;
```
قم بإنشاء خيارات PNG، مع دمج إعدادات التنقيط المحددة في الخطوة السابقة.
## الخطوة 5: احفظ ملف PNG
```csharp
string outPath = sourceFilePath + ".png";
cadImage.Save(outPath, pngOptions);
```
حدد مسار الإخراج لملف PNG واحفظ صورة CAD بتنسيق PNG باستخدام الخيارات المتوفرة.
كرر هذه الخطوات حسب الحاجة لحالة الاستخدام المحددة الخاصة بك، وستنجح في تصدير ملفات STL إلى PNG باستخدام Aspose.CAD لـ .NET.
## خاتمة
يعمل Aspose.CAD for .NET على تبسيط المهمة المعقدة المتمثلة في تحويل ملفات STL إلى PNG، مما يوفر للمطورين مجموعة أدوات موثوقة. باتباع هذا الدليل التفصيلي، يمكنك دمج هذه الوظيفة بسلاسة في تطبيقاتك.
## الأسئلة الشائعة
### س: هل يمكنني تخصيص أبعاد PNG المصدرة؟
 قطعاً! في الخطوة 3، قم بضبط`PageWidth` و`PageHeight` القيم لتلبية متطلباتك المحددة.
### س: هل الترخيص المؤقت متاح لأغراض الاختبار؟
 نعم يمكنك الحصول على ترخيص مؤقت[هنا](https://purchase.aspose.com/temporary-license/) للاختبار والتقييم.
### س: أين يمكنني العثور على دعم إضافي أو مناقشات مجتمعية؟
 قم بزيارة[منتدى Aspose.CAD](https://forum.aspose.com/c/cad/19) للحصول على الدعم والمناقشات التعاونية.
### س: هل هناك تنسيقات ملفات أخرى مدعومة للتحويل؟
 نعم، يدعم Aspose.CAD تنسيقات CAD المختلفة بخلاف STL. الرجوع إلى[توثيق](https://reference.aspose.com/cad/net/) للحصول على قائمة شاملة.
### س: هل يمكنني معالجة ملفات STL متعددة دفعة واحدة؟
بالتأكيد! قم بتنفيذ حلقة بناءً على الخطوات المقدمة لمعالجة ملفات STL المتعددة دفعة واحدة.