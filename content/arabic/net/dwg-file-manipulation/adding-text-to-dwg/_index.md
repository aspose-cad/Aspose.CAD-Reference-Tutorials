---
title: إضافة نص إلى ملفات DWG في C# - البرنامج التعليمي Aspose.CAD
linktitle: إضافة نص إلى ملفات DWG في C#
second_title: Aspose.CAD .NET - تنسيق ملف CAD وBIM
description: تعرف على كيفية إضافة نص إلى ملفات DWG باستخدام C# وAspose.CAD. اتبع هذا البرنامج التعليمي خطوة بخطوة لتحقيق التكامل السلس. استكشف وثائق Aspose.CAD للحصول على إرشادات شاملة.
type: docs
weight: 14
url: /ar/net/dwg-file-manipulation/adding-text-to-dwg/
---
## مقدمة

في المجال الديناميكي للتصميم بمساعدة الكمبيوتر (CAD) وتطوير .NET، يبرز Aspose.CAD كأداة قوية لمعالجة ملفات DWG. تعد إضافة نص إلى ملفات DWG متطلبًا شائعًا، وفي هذا البرنامج التعليمي، سنستكشف كيفية تحقيق ذلك باستخدام C# وAspose.CAD.

## المتطلبات الأساسية

قبل الغوص في البرنامج التعليمي، تأكد من أن لديك ما يلي:

-  مكتبة Aspose.CAD: قم بتنزيل وتثبيت مكتبة Aspose.CAD من ملف[رابط التحميل](https://releases.aspose.com/cad/net/).

-  دليل المستندات: قم بإعداد دليل لمستنداتك، ولاحظ مساره كـ`MyDir`.

الآن، دعونا نقسم العملية إلى خطوات يمكن التحكم فيها.

## استيراد مساحات الأسماء

في كود C# الخاص بك، قم بتضمين مساحات الأسماء الضرورية للوصول إلى وظائف Aspose.CAD.

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

 قم بتحميل ملف DWG إلى ملف`Image` الكائن باستخدام مكتبة Aspose.CAD.

```csharp
string dwgPathToFile = MyDir + "SimpleEntites.dwg";
using (Image image = Image.Load(dwgPathToFile))
{
    // الكود الخاص بك للخطوات اللاحقة موجود هنا
}
```

## الخطوة 2: إنشاء كائن CadText

 إنشاء مثيل أ`CadText` كائن لتمثيل النص الذي تريد إضافته إلى ملف DWG.

```csharp
CadText cadText = new CadText();
cadText.StyleType = "Standard";
cadText.DefaultValue = "Some custom text";
cadText.ColorId = 256;
cadText.LayerName = "0";
cadText.FirstAlignment.X = 47.90;
cadText.FirstAlignment.Y = 5.56;
cadText.TextHeight = 0.8;
cadText.ScaleX = 0.0;
```

## الخطوة 3: إضافة نص إلى DWG

 أضف ما تم إنشاؤه`CadText` كائن إلى ملف DWG باستخدام Aspose.CAD.

```csharp
CadImage cadImage = (CadImage)image;
cadImage.BlockEntities["*Model_Space"].AddEntity(cadText);
```

## الخطوة 4: تكوين خيارات PDF

قم بتكوين خيارات PDF لحفظ ملف DWG المعدل كملف PDF.

```csharp
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.VectorRasterizationOptions = cadRasterizationOptions;
cadRasterizationOptions.DrawType = CadDrawTypeMode.UseObjectColor;
cadRasterizationOptions.PageHeight = 1600;
cadRasterizationOptions.PageWidth = 1600;
cadRasterizationOptions.Layouts = new string[] { "Model" };
```

## الخطوة 5: احفظ بصيغة PDF

احفظ ملف DWG المعدل كملف PDF مع النص المضاف.

```csharp
image.Save(MyDir + "SimpleEntites_generated.pdf", pdfOptions);
```

لقد نجحت الآن في إضافة نص إلى ملف DWG باستخدام C# وAspose.CAD. لا تتردد في استكشاف المزيد من الميزات والوظائف في Aspose.CAD لتلبية احتياجات معالجة CAD الخاصة بك.

## خاتمة

في هذا البرنامج التعليمي، قمنا بتغطية الخطوات الأساسية لإضافة نص إلى ملفات DWG باستخدام C# وAspose.CAD. يفتح هذا المزيج القوي إمكانيات إنشاء مستندات CAD ديناميكية ومخصصة.

## الأسئلة الشائعة

### س 1: هل Aspose.CAD متوافق مع كافة إصدارات ملفات DWG؟

ج1: يدعم Aspose.CAD نطاقًا واسعًا من إصدارات ملفات DWG، مما يضمن التوافق مع برامج CAD المتنوعة.

### س2: هل يمكنني إضافة كيانات نصية متعددة إلى ملف DWG واحد باستخدام Aspose.CAD؟

ج2: نعم، يمكنك إضافة كيانات نصية متعددة إلى ملف DWG عن طريق تكرار العملية الموضحة في البرنامج التعليمي.

### س3: كيف يمكنني تغيير خط النص ونمطه في Aspose.CAD؟

 A3: لتعديل خط النص ونمطه، اضبط خصائص الملف`CadText` الكائن قبل إضافته إلى ملف DWG.

### س 4: هل هناك أي اعتبارات ترخيص لاستخدام Aspose.CAD في مشروع تجاري؟

 ج4: نعم، تأكد من الامتثال لشروط ترخيص Aspose.CAD. تشير إلى[شراء Aspose.CAD](https://purchase.aspose.com/buy) للتفاصيل.

### س5: أين يمكنني طلب المساعدة أو مناقشة الاستعلامات المتعلقة بـ Aspose.CAD؟

 ج5: قم بزيارة[منتدى Aspose.CAD](https://forum.aspose.com/c/cad/19)للتواصل مع المجتمع والحصول على الدعم.