---
date: 2026-04-03
description: تعلم كيفية تعيين نافذة العرض وتحويل ملفات DWG إلى PDF باستخدام C# و Aspose.CAD.
  يوضح هذا الدرس حول تحويل DWG إلى PDF تصديرًا دقيقًا مع الإحداثيات.
keywords:
- how to set viewport
- dwg to pdf tutorial
- convert dwg to pdf c#
linktitle: تحويل DWG إلى PDF مع الإحداثيات في C#
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: كيفية تعيين نافذة العرض أثناء تحويل DWG إلى PDF مع الإحداثيات في C# - دليل
  Aspose.CAD
url: /ar/net/conversion-and-export/converting-dwg-to-pdf-with-coordinates/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تحويل DWG إلى PDF مع الإحداثيات في C# - دليل Aspose.CAD

## مقدمة

مرحبًا بكم في هذا الدرس الشامل حول **كيفية تعيين منطقة العرض** أثناء تحويل ملفات DWG إلى PDF مع إحداثيات محددة باستخدام Aspose.CAD لـ .NET. من خلال التحكم في منطقة العرض ستحصل على ملفات PDF بدقة بكسل مطابقة تمامًا للمنطقة التي تحتاجها — مثالية لرسومات الإنشاء، ومعاينات مخططات الطوابق، أو أي سير عمل BIM.

## إجابات سريعة
- **ماذا يعني “set viewport”?** يحدد المنطقة المرئية وتكبير/تصغير رسم CAD أثناء التحويل النقطي.  
- **أي مكتبة تتعامل مع التحويل؟** Aspose.CAD لـ .NET.  
- **هل أحتاج إلى رخصة؟** النسخة التجريبية المجانية تكفي للتقييم؛ تحتاج إلى رخصة تجارية للإنتاج.  
- **المنصات المدعومة؟** Windows و Linux و macOS مع .NET 5/6/7 أو .NET Framework 4.6+.  
- **الوقت النموذجي للتنفيذ؟** حوالي 10‑15 دقيقة للتحويل الأساسي.

## المتطلبات المسبقة

قبل أن نبدأ، تأكد من توفر المتطلبات التالية:

- **مكتبة Aspose.CAD** – قم بتنزيل وتثبيت مكتبة Aspose.CAD لـ .NET. يمكنك العثور على المكتبة [هنا](https://releases.aspose.com/cad/net/).
- **بيئة التطوير** – Visual Studio أو Rider أو أي بيئة تطوير تدعم .NET.
- **ملف DWG** – احرص على وجود ملف DWG جاهز للتحويل. يمكنك استخدام ملف المثال المرفق أو ملف DWG الخاص بك.

## كيفية تعيين منطقة العرض لتصدير PDF دقيق

تعيين منطقة العرض هو الخطوة الأساسية التي تسمح لك بتحديد المنطقة الدقيقة من الرسم التي تريد تصييرها. في الشيفرة أدناه نقوم بإنشاء كائن `CadVportTableObject` جديد، ونضعه باستخدام إحداثيات الزاوية العلوية اليسرى، ونحسب العرض والارتفاع ونسبة الأبعاد. هذا هو تنفيذ **كيفية تعيين منطقة العرض** الذي يدفع بقية عملية التحويل.

## استيراد مساحات الأسماء

في مشروع C# الخاص بك، استورد مساحات الأسماء اللازمة:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadParameters;
using Aspose.CAD.FileFormats.Cad.CadTables;
using Aspose.CAD.ImageOptions;
```

دعنا نقسم الشيفرة إلى دليل خطوة بخطوة لفهم أفضل:

## الخطوة 1: تعريف دليل المستند

```csharp
string MyDir = "Your Document Directory";
```

## الخطوة 2: تحديد مسار ملف DWG المصدر

```csharp
string sourceFilePath = MyDir + "visualization_-_conference_room.dwg";
```

## الخطوة 3: تحميل ملف DWG وتكوين خيارات التحويل النقطي

```csharp
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
    rasterizationOptions.Layouts = new string[] { "Model" };
    rasterizationOptions.NoScaling = true;
```

## الخطوة 4: تعريف الإحداثيات ومنطقة العرض  

هنا نقوم فعليًا **بتعيين منطقة العرض** (كيفية تعيين منطقة العرض) عن طريق تحديد الزاوية العلوية اليسرى، العرض، والارتفاع للمنطقة التي تريد تصديرها.

```csharp
    Point topLeft = new Point(500, 1000);
    double width = 3108;
    double height = 2489;

    CadVportTableObject newView = new CadVportTableObject();
    newView.Name = new CadStringParameter();
    newView.Name.Init("*Active");
    newView.CenterPoint.X = topLeft.X + width / 2f;
    newView.CenterPoint.Y = topLeft.Y - height / 2f;
    newView.ViewHeight.Value = height;
    newView.ViewAspectRatio.Value = width / height;
```

## الخطوة 5: تطبيق إعدادات منطقة العرض

```csharp
    for (int i = 0; i < cadImage.ViewPorts.Count; i++)
    {
        CadVportTableObject currentView = (CadVportTableObject)(cadImage.ViewPorts[i]);
        if (cadImage.ViewPorts.Count == 1 || string.Equals(currentView.Name.Value.ToLowerInvariant(), "*active"))
        {
            cadImage.ViewPorts[i] = newView;
            break;
        }
    }
```

## الخطوة 6: تكوين خيارات PDF وتصدير  

الآن نجمع كل شيء معًا و**نحول DWG إلى PDF** باستخدام خيارات التحويل النقطي التي أعددناها للتو.

```csharp
    Aspose.CAD.ImageOptions.PdfOptions pdfOptions = new Aspose.CAD.ImageOptions.PdfOptions();
    pdfOptions.VectorRasterizationOptions = rasterizationOptions;

    MyDir = MyDir + "ConvertDWGToPDFBySupplyingCoordinates_out.pdf";
    cadImage.Save(MyDir, pdfOptions);
}
```

## الخطوة 7: عرض رسالة النجاح

```csharp
Console.WriteLine("\nThe DWG file exported successfully to PDF.\nFile saved at " + MyDir);
```

## حالات الاستخدام الشائعة

- **توثيق الإنشاء** – إنشاء ملفات PDF قابلة للطباعة لأقسام مخططات الطوابق المحددة.  
- **تنسيق BIM** – تصدير المنطقة المطلوبة فقط للكشف عن التعارضات.  
- **عروض العملاء** – تقديم ملف PDF نظيف لغرفة أو ارتفاع مختار دون الكشف عن كامل الرسم.

## الخاتمة

تهانينا! لقد نجحت في **تحويل DWG إلى PDF** باستخدام إحداثيات دقيقة وتعلمت **كيفية تعيين منطقة العرض** باستخدام Aspose.CAD لـ .NET. يوضح هذا **دليل تحويل dwg إلى pdf** كيفية **إنشاء pdf من dwg** و**تصدير dwg كـ pdf c#** مع الحفاظ على التحكم الكامل في منطقة الإخراج.

## الأسئلة الشائعة

### س1: هل يمكنني استخدام Aspose.CAD مع صيغ ملفات CAD أخرى؟

ج1: نعم، يدعم Aspose.CAD صيغ CAD متعددة، بما في ذلك DWG و DXF و DWF وغير ذلك.

### س2: كيف يمكنني التعامل مع الأخطاء أثناء عملية التحويل؟

ج2: نفّذ آليات معالجة الأخطاء باستخدام كتل try‑catch لالتقاط وإدارة الاستثناءات.

### س3: هل Aspose.CAD مناسب لكل من بيئات Windows و Linux؟

ج3: نعم، Aspose.CAD متوافق مع كل من منصات Windows و Linux.

### س4: هل يمكنني تخصيص مخرجات PDF أكثر؟

ج4: بالتأكيد! استكشف الخيارات الواسعة التي يوفرها Aspose.CAD لتخصيص مخرجات PDF وفقًا لمتطلباتك الخاصة.

### س5: أين يمكنني العثور على دعم إضافي أو مناقشات المجتمع؟

ج5: زر [منتدى Aspose.CAD](https://forum.aspose.com/c/cad/19) للحصول على دعم المجتمع والمناقشات.

## أسئلة شائعة إضافية

**س: هل يعمل هذا الأسلوب مع ملفات DWG الكبيرة (مئات الميجابايت)؟**  
ج: نعم. يتم تنفيذ التحويل النقطي صفحة بصفحة، ويمكنك تعديل `rasterizationOptions` (مثل `Resolution`) لتحقيق التوازن بين الجودة واستخدام الذاكرة.

**س: هل يمكنني تصدير عدة مناطق عرض إلى صفحات PDF منفصلة؟**  
ج: يمكنك التكرار عبر `cadImage.ViewPorts`، تعيين كل واحدة كفعّالة، واستدعاء `Save` لكل صفحة، ثم دمج ملفات PDF باستخدام Aspose.PDF.

**س: هل يمكن إضافة علامة مائية إلى ملف PDF المُولد؟**  
ج: بعد حفظ PDF، يمكنك إعادة فتحه باستخدام Aspose.PDF وتطبيق علامة مائية نصية أو صورة قبل تسليمها للمستخدم.

---

**آخر تحديث:** 2026-04-03  
**تم الاختبار مع:** Aspose.CAD 24.11 لـ .NET  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}