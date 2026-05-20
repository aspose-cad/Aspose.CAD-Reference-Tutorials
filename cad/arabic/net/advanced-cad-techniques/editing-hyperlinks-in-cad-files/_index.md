---
date: 2026-03-05
description: تعلم كيفية تغيير مسار الإشارة الخارجية (xref)، وتحديث مرجع الكتلة، وإدارة
  الروابط التشعبية في CAD باستخدام Aspose.CAD لـ .NET في بضع خطوات سهلة.
linktitle: Editing Hyperlinks in CAD Files
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: كيفية تغيير مسار الـxref وتعديل الروابط التشعبية في ملفات CAD - دليل Aspose.CAD
url: /ar/net/advanced-cad-techniques/editing-hyperlinks-in-cad-files/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تحرير الروابط التشعبية في ملفات CAD - دليل Aspose.CAD

## المقدمة

مرحبًا بكم في دليلنا خطوة بخطوة حول كيفية **change xref path** وتحرير الروابط التشعبية في ملفات CAD باستخدام Aspose.CAD لـ .NET. سواء كنت بحاجة إلى **update block reference** أو ببساطة **manage CAD hyperlinks**، فإن هذا البرنامج التعليمي يوجهك عبر العملية الكاملة، من تحميل ملف DWG إلى حفظ التغييرات. في النهاية، ستحصل على نمط واضح وقابل لإعادة الاستخدام للحفاظ على ربط مستندات CAD الخاصة بك بشكل صحيح.

## إجابات سريعة
- **What does “change xref path” mean?** إنه يقوم بتحديث مسار ملف المرجع الخارجي (XRef) المخزن في كتلة CAD.  
- **Which library handles this?** Aspose.CAD لـ .NET يوفر واجهة برمجة تطبيقات بسيطة لتحرير مسارات XRef والروابط التشعبية.  
- **Do I need a license?** نسخة التجربة المجانية تكفي للتطوير؛ يلزم الحصول على ترخيص تجاري للإنتاج.  
- **Can I use this with .NET Core?** نعم، المكتبة تدعم .NET Framework و .NET Core/.NET 5+.  
- **How long does the implementation take?** عادةً أقل من 10 دقائق لملف أساسي.

## ما هو تغيير مسار XRef؟

في مصطلحات CAD، الـ **XRef** (المرجع الخارجي) يشير إلى ملف رسم آخر يتم إدراجه ككتلة. تغيير مسار XRef يعني توجيه الكتلة إلى موقع ملف جديد، وهو أمر أساسي عند إعادة تنظيم مجلدات المشروع أو تحديث الموارد المرتبطة.

## لماذا تحديث مرجع الكتلة وإدارة الروابط التشعبية في CAD؟

- **Maintain consistency** عندما يتم نقل الملفات عبر بيئات مختلفة.  
- **Avoid broken links** التي قد تتسبب في أخطاء أثناء العرض أو المعالجة اللاحقة.  
- **Streamline BIM workflows** عبر ضمان تحديث جميع المراجع برمجيًا.

## المتطلبات المسبقة

- معرفة أساسية بـ C# وتطوير .NET.  
- تثبيت Aspose.CAD لـ .NET – قم بتنزيله [here](https://releases.aspose.com/cad/net/).  
- ملف CAD تجريبي (مثال: *AutoCad_Sample.dwg*) للتجربة.

## استيراد المساحات الاسمية

في مشروع C# الخاص بك، أضف المساحات الاسمية المطلوبة:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

الآن دعنا نتبع تنفيذ العملية خطوة بخطوة.

## الخطوة 1: تحميل ملف CAD

```csharp
// The path to the documents directory.
string MyDir = "Your Document Directory";
string dwgPathToFile = MyDir + "AutoCad_Sample.dwg";

using (CadImage cadImage = (CadImage)Image.Load(dwgPathToFile))
{
    // Your code for editing hyperlinks will go here.
}
```

## الخطوة 2: التكرار عبر الكيانات

```csharp
foreach (CadBaseEntity entity in cadImage.Entities)
{
    // Your code for handling each entity will go here.
}
```

## الخطوة 3: تحرير كائنات الإدراج – تغيير مسار XRef

```csharp
if (entity is CadInsertObject)
{
    CadBlockEntity block = cadImage.BlockEntities[((CadInsertObject)entity).Name];
    if (!string.IsNullOrEmpty(block.XRefPathName.Value))
    {
        // **Primary keyword usage:** change xref path
        block.XRefPathName.Value = "new file reference.dwg";
    }
}
```

*هنا نقوم **update block reference** عن طريق تعيين اسم ملف XRef جديد. هذا هو جوهر تغيير مسار XRef.*

## الخطوة 4: تعديل الروابط التشعبية – إدارة روابط CAD

```csharp
if (entity.Hyperlink == "https://products.aspose.com")
{
    // **Secondary keyword usage:** manage cad hyperlinks
    entity.Hyperlink = "https://www.aspose.com";
}
```

*هذا المقتطف يوضح كيفية **update CAD links** (الروابط التشعبية) لتوجيهها إلى العنوان الويب الصحيح.*

## المشكلات الشائعة والحلول

| المشكلة | السبب | الحل |
|-------|-------|-----|
| XRef path not updating | Block is not an `CadInsertObject` | Verify entity type before casting. |
| Hyperlink unchanged | Hyperlink property is null or different case | Use `StringComparison.OrdinalIgnoreCase` when comparing. |
| File fails to load | Missing Aspose.CAD license in production | Apply a valid license before loading the image. |

## الخاتمة

لقد تعلمت الآن كيفية **change xref path**، **update block reference**، وإدارة الروابط التشعبية في CAD باستخدام Aspose.CAD لـ .NET. تتيح لك هذه القدرات الحفاظ على تنظيم المشاريع الكبيرة من CAD وخلوها من الروابط المكسورة، مما يعزز الاعتمادية في خطوط الأنابيب الآلية.

## الأسئلة المتكررة

### س1: هل Aspose.CAD متوافق مع صيغ ملفات CAD الأخرى؟

A1: نعم، Aspose.CAD يدعم صيغ CAD متعددة، بما في ذلك DWG، DXF، DGN، وغيرها.

### س2: هل يمكنني تجربة Aspose.CAD قبل الشراء؟

A2: بالتأكيد! يمكنك الحصول على نسخة تجريبية مجانية [here](https://releases.aspose.com/).

### س3: أين يمكنني العثور على الوثائق التفصيلية لـ Aspose.CAD؟

A3: راجع الوثائق [here](https://reference.aspose.com/cad/net/).

### س4: كيف أحصل على ترخيص مؤقت لـ Aspose.CAD؟

A4: احصل على ترخيص مؤقت [here](https://purchase.aspose.com/temporary-license/).

### س5: هل تحتاج إلى مساعدة أو لديك أسئلة؟

A5: زر منتدى الدعم الخاص بنا [here](https://forum.aspose.com/c/cad/19).

## أسئلة متكررة إضافية

**س: هل يمكنني تغيير مسارات XRef متعددة برمجيًا في تمريرة واحدة؟**  
ج: نعم، قم بالتكرار عبر جميع كائنات `CadInsertObject` واضبط `XRefPathName.Value` حسب الحاجة.

**س: هل يؤثر تغيير مسار XRef على المظهر البصري للرسم؟**  
ج: يتم تحديث المرجع، لكن الرسم سيعرض الملف الخارجي الجديد عند فتحه في عارض CAD.

**س: هل هناك طريقة لسرد جميع الروابط التشعبية الحالية في ملف CAD؟**  
ج: قم بالتكرار عبر `cadImage.Entities` وجمع قيم `entity.Hyperlink` التي لا تكون فارغة أو null.

**س: هل سيعمل هذا النهج مع ملفات DWG الكبيرة (مئات الميغابايت)؟**  
ج: Aspose.CAD مُحسّن للأداء، لكن تأكد من توفر ذاكرة كافية وفكر في المعالجة على دفعات إذا لزم الأمر.

---

**آخر تحديث:** 2026-03-05  
**تم الاختبار مع:** Aspose.CAD 24.12 لـ .NET  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}