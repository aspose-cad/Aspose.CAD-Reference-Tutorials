---
date: 2026-03-21
description: تعلم كيفية إنشاء PDF من CAD، وتحويل DXF إلى PDF، وتعيين حجم الصفحة في
  CAD باستخدام Aspose.CAD لـ .NET مع تمكين التتبع. اتبع دليلنا خطوة بخطوة للحصول على
  تحكم كامل.
linktitle: Enable Tracking for CAD Rendering
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: إنشاء ملف PDF من CAD مع التتبع باستخدام Aspose.CAD لـ .NET
url: /ar/net/cad-drawing-manipulation/enable-tracking-for-cad-rendering/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# إنشاء PDF من CAD مع التتبع باستخدام Aspose.CAD لـ .NET

## المقدمة

في تطبيقات .NET الحديثة، **إنشاء PDF من CAD** هو مطلب شائع — سواء كنت بحاجة إلى مشاركة التصاميم مع أصحاب المصلحة غير التقنيين أو أرشفة الرسومات بصيغة محمولة. تجعل Aspose.CAD لـ .NET هذا التحويل بسيطًا بينما تقدم أيضًا ميزة **التتبع** التي تتيح لك مراقبة تقدم التصيير وجمع معلومات تشخيصية. في هذا الدليل سنستعرض العملية بالكامل: تحميل ملف DXF، ضبط حجم الصفحة، تحويله إلى PDF، وتمكين التتبع للحصول على رؤية كاملة لسلسلة التصيير.

## إجابات سريعة
- **هل يمكنني تحويل DXF إلى PDF باستخدام Aspose.CAD؟** نعم، المكتبة تدعم تحويل DXF إلى PDF مباشرةً.  
- **كيف يمكنني ضبط حجم الصفحة CAD أثناء التحويل؟** استخدم `CadRasterizationOptions.PageWidth` و `PageHeight`.  
- **هل التتبع إلزامي؟** لا، لكنه يوفر تشخيصات قيمة للرسومات الكبيرة أو المعقدة.  
- **ما إصدارات .NET المدعومة؟** .NET Framework 4.5+، .NET Core 3.1+، .NET 5/6+.  
- **هل أحتاج إلى ترخيص للإنتاج؟** يتطلب ترخيص تجاري؛ يتوفر نسخة تجريبية مجانية.

## ما هو “إنشاء PDF من CAD”؟
إنشاء PDF من CAD يعني تصيير رسم CAD (مثل DXF أو DWG) إلى مستند PDF رستر أو فيكتور. هذه العملية تحافظ على الدقة البصرية مع توفير صيغة يمكن فتحها على أي جهاز تقريبًا دون الحاجة إلى برنامج CAD متخصص.

## لماذا تمكين التتبع لتصوير CAD؟
يوفر التتبع نظرة فورية على محرك التصيير — مفيد للتصحيح، تحسين الأداء، والتدقيق. عندما تمكّن التتبع، تقوم Aspose.CAD بتسجيل كل خطوة من خطوات التصيير، مما يساعدك على تحديد نقاط الاختناق أو الأخطاء في المشاريع الكبيرة.

## المتطلبات المسبقة

- **Aspose.CAD لـ .NET** – قم بتنزيله من [هنا](https://releases.aspose.com/cad/net/).  
- **بيئة التطوير** – Visual Studio (أي نسخة حديثة) مع دعم .NET.  
- **ملف CAD تجريبي** – ملف DXF مثل `conic_pyramid.dxf` الذي ستقوم بتحويله وتتبع عملية التحويل.

## استيراد مساحات الأسماء

في مشروع .NET الخاص بك، استورد مساحات الأسماء المطلوبة:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using System.IO;
```

## دليل خطوة بخطوة

### الخطوة 1: تعيين دليل المستند (ضبط حجم الصفحة CAD)

استبدل **Your Document Directory** بالمسار المطلق حيث يقع ملف DXF الخاص بك. هذا هو المكان الذي يمكنك أيضًا تعديل أبعاد الصفحة من خلال خيارات الرستر لاحقًا.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";
```

### الخطوة 2: تحميل ملف CAD

طريقة `Image.Load` تقرأ رسم CAD إلى كائن `Aspose.CAD.Image`، مما يجهزه للتصيير.

```csharp
using (Image image = Image.Load(sourceFilePath))
{
    // Further steps will be implemented here
}
```

### الخطوة 3: إنشاء خيارات PDF (التحضير لتحويل dxf إلى pdf)

يتيح لك `MemoryStream` الاحتفاظ بـ PDF المُولد في الذاكرة، بينما يحمل `PdfOptions` جميع إعدادات PDF الخاصة.

```csharp
MemoryStream stream = new MemoryStream();
PdfOptions pdfOptions = new PdfOptions();
```

### الخطوة 4: تكوين خيارات الرستر (ضبط حجم الصفحة CAD)

هنا تقوم بتحديد حجم الصفحة الناتج (`PageWidth` و `PageHeight`). اضبط هذه القيم لتتناسب مع أبعاد PDF المطلوبة — هذا هو جوهر مطلب **ضبط حجم الصفحة CAD**.

```csharp
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.VectorRasterizationOptions = cadRasterizationOptions;
cadRasterizationOptions.PageWidth = 800;
cadRasterizationOptions.PageHeight = 600;
```

### الخطوة 5: حفظ الصورة المرسومة (إكمال سير عمل إنشاء pdf من cad)

استدعاء `Save` يكتب المحتوى المصور إلى تدفق الذاكرة باستخدام خيارات PDF التي قمت بتكوينها. في هذه المرحلة ستحصل على تمثيل PDF للملف CAD الأصلي، وسيتم التقاط معلومات التتبع تلقائيًا بواسطة المكتبة.

```csharp
image.Save(stream, pdfOptions);
```

## المشكلات الشائعة والحلول

| المشكلة | سبب حدوثه | الحل |
|-------|----------------|-----|
| **Blank PDF output** | Rasterization options not linked to `PdfOptions` | Ensure `pdfOptions.VectorRasterizationOptions = cadRasterizationOptions;` is set. |
| **Incorrect page size** | `PageWidth`/`PageHeight` left at defaults | Explicitly set both properties before saving. |
| **Performance slowdown on large DXF** | Tracking logs can be verbose | Disable or limit tracking in production by adjusting `Aspose.CAD.Logging` settings. |

## الأسئلة المتكررة

**س: هل Aspose.CAD لـ .NET مناسب لكل من التصوير الثنائي الأبعاد والثلاثي الأبعاد؟**  
ج: نعم، Aspose.CAD لـ .NET يدعم كل من التصوير الثنائي والثلاثي الأبعاد، ويوفر حلاً شاملاً لمختلف احتياجات التصميم.

**س: هل يمكنني استخدام Aspose.CAD لـ .NET مع أطر .NET أخرى؟**  
ج: بالتأكيد! يتكامل Aspose.CAD لـ .NET بسلاسة مع أطر .NET المتنوعة، مما يضمن المرونة والتوافق.

**س: هل تتوفر نسخة تجريبية مجانية لـ Aspose.CAD لـ .NET؟**  
ج: نعم، يمكنك استكشاف ميزات Aspose.CAD لـ .NET من خلال نسخة تجريبية مجانية متاحة [هنا](https://releases.aspose.com/).

**س: كيف يمكنني الحصول على دعم لـ Aspose.CAD لـ .NET؟**  
ج: لأي مساعدة أو استفسارات، زر [منتدى Aspose.CAD](https://forum.aspose.com/c/cad/19) للتواصل مع المجتمع والدعم.

**س: ما هي فوائد تمكين التتبع في تصوير CAD؟**  
ج: تمكين التتبع يعزز إمكانية التتبع والتحكم أثناء عملية التصيير، مما يضمن سير عمل أكثر شفافية وكفاءة.

## الخاتمة

لقد تعلمت الآن كيفية **إنشاء PDF من CAD**، **تحويل DXF إلى PDF**، و**ضبط حجم الصفحة CAD** مع الاستفادة من قدرات التتبع في Aspose.CAD. يمنحك هذا سير العمل المتكامل تحكمًا كاملاً في جودة التصيير، أبعاد الإخراج، ورؤية تشخيصية — مثالي لتطبيقات الهندسة على مستوى المؤسسات.

---

**آخر تحديث:** 2026-03-21  
**تم الاختبار مع:** Aspose.CAD لـ .NET 24.11  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}