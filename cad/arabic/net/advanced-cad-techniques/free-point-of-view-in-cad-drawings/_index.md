---
date: 2026-03-05
description: تعلم كيفية تحويل DXF إلى JPEG، وإنشاء صورة CAD ثلاثية الأبعاد، وتغيير
  زاوية عرض CAD باستخدام Aspose.CAD لـ .NET. اتبع دليلنا خطوة بخطوة.
linktitle: Free Point of View in CAD Drawings
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: تحويل DXF إلى JPEG – منظور مجاني في رسومات CAD | دليل Aspose.CAD
url: /ar/net/advanced-cad-techniques/free-point-of-view-in-cad-drawings/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تحويل DXF إلى JPEG – منظور حر في رسومات CAD

في هذا الدرس ستكتشف كيفية **تحويل DXF إلى JPEG** مع الحصول على منظور حر في رسم CAD الخاص بك. عن طريق تدوير نقطة المراقب يمكنك **إنشاء صورة CAD ثلاثية الأبعاد**، **تغيير زاوية عرض CAD**، وأخيرًا **تصدير CAD إلى JPEG** باستخدام Aspose.CAD لـ .NET. دعنا نتبع العملية بالكامل، بدءًا من إعداد البيئة حتى حفظ الصورة النهائية.

## الإجابات السريعة
- **ما معنى “convert DXF to JPEG”?** يحول ملف DXF القائم على المتجهات إلى صورة JPEG نقطية.  
- **ما المكتبة التي تتعامل مع التحويل؟** توفر Aspose.CAD لـ .NET واجهة برمجة تطبيقات بسيطة لهذه المهمة.  
- **هل أحتاج إلى ترخيص؟** النسخة التجريبية المجانية تعمل للتطوير؛ يلزم ترخيص تجاري للإنتاج.  
- **هل يمكنني تعديل زاوية العرض؟** نعم – تقوم بتعيين `ObserverPoint` لتدوير النموذج على محاور X و Y و Z.  
- **ما حجم الإخراج الذي يمكنني اختياره؟** تسمح لك خصائص `PageWidth` و `PageHeight` بتحديد أي دقة تحتاجها.

## ما هو “convert DXF إلى JPEG”؟
تحويل ملف DXF (Drawing Exchange Format) إلى JPEG يُنشئ لقطة bitmap للتصميم، مما يجعل من السهل مشاركتها، أو تضمينها في المستندات، أو عرضها على الويب دون الحاجة إلى برنامج CAD.

## لماذا تستخدم Aspose.CAD لتصدير CAD إلى JPEG؟
- **لا حاجة لتثبيت CAD** – تعمل المكتبة في أي بيئة .NET.  
- **تحكم كامل في التصيير** – يمكنك ضبط خيارات التحويل إلى نقطية، DPI، لون الخلفية، ونقطة المراقب.  
- **يدعم العديد من صيغ CAD** – DWG، DXF، DWF، وأكثر، بحيث يمكن لنفس الكود **حفظ CAD كـ JPG** لمصادر مختلفة.  
- **إخراج عالي الجودة** – تحويل المتجه إلى نقطية يحافظ على حدة الخطوط والتفاصيل.

## المتطلبات المسبقة

قبل البدء، تأكد من أن لديك ما يلي:

1. **تثبيت Aspose.CAD** – قم بتحميل وإضافة أحدث Aspose.CAD لـ .NET من [موقع Aspose.CAD](https://releases.aspose.com/cad/net/).  
2. **ملف رسم CAD** – ملف DXF ترغب في تحويله، مثال: `conic_pyramid.dxf`.  
3. **بيئة التطوير** – Visual Studio، VS Code، أو أي بيئة تطوير متوافقة مع .NET.

## استيراد المساحات الاسمية

أضف عبارات `using` المطلوبة في أعلى ملف C# الخاص بك:

```csharp
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
```

## دليل خطوة بخطوة

### الخطوة 1: تعريف دليل المستند
```csharp
// The path to the documents directory.
string MyDir = "Your Document Directory";
```
استبدل `"Your Document Directory"` بالمجلد الفعلي الذي يحتوي على ملف DXF الخاص بك.

### الخطوة 2: تحديد ملف المصدر
```csharp
string sourceFilePath = MyDir + "conic_pyramid.dxf";
```
هذا هو المسار إلى ملف DXF الذي ستقوم **بتحويله إلى JPEG**.

### الخطوة 3: تعيين مسار الإخراج
```csharp
var outPath = Path.Combine(MyDir, "FreePointOfView_out.jpg");
```
هنا تحدد أين سيتم كتابة **ملف JPEG المحفوظ**.

### الخطوة 4: تحميل صورة CAD
```csharp
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
```
كائن `CadImage` يمنحك الوصول إلى خيارات التحويل إلى نقطية.

### الخطوة 5: تكوين خيارات JPEG
```csharp
JpegOptions options = new JpegOptions
{
    VectorRasterizationOptions = new CadRasterizationOptions
    {
        PageWidth = 1500, PageHeight = 1500
    }
};
```
هذه الإعدادات تتحكم في دقة **JPEG** الناتج.

### الخطوة 6: تعيين زوايا الدوران (تغيير زاوية عرض CAD)
```csharp
float xAngle = 10; //Angle of rotation along the X axis
float yAngle = 30; //Angle of rotation along the Y axis
float zAngle = 40; //Angle of rotation along the Z axis
((CadRasterizationOptions)(options.VectorRasterizationOptions)).ObserverPoint = new ObserverPoint(xAngle, yAngle, zAngle);
```
قم بضبط الزوايا للحصول على **منظور حر** المطلوب وفعليًا **إنشاء صورة CAD ثلاثية الأبعاد**.

### الخطوة 7: حفظ رسم CAD المُعالج
```csharp
cadImage.Save(outPath, options);
}
```
هذه العملية **تُصدر CAD إلى JPEG** باستخدام زاوية العرض المُكوَّنة.

### الخطوة 8: عرض رسالة النجاح
```csharp
Console.WriteLine("\n3D images exported successfully to JPEG.\nFile saved at " + outPath);
```
إخراج سطر الأوامر الودي يؤكد أن التحويل نجح.

## المشكلات الشائعة والحلول
- **الصورة تظهر فارغة** – تأكد من أن نقطة المراقب ضمن نطاق معقول؛ الزوايا المتطرفة قد تقص النموذج.  
- **ملف الإخراج كبير جدًا** – قلل من `PageWidth`/`PageHeight` أو زد ضغط JPEG عبر `options.Quality`.  
- **كيانات DXF غير مدعومة** – تدعم Aspose.CAD معظم الكيانات القياسية؛ تحقق من ملاحظات إصدار المكتبة لأي قيود.

## الأسئلة المتكررة

**س: هل يمكنني استخدام Aspose.CAD لـ .NET مع صيغ ملفات CAD أخرى؟**  
ج: نعم، يدعم Aspose.CAD صيغ DWG، DWF، DGN، والعديد غيرها بالإضافة إلى DXF.

**س: هل تتوفر نسخة تجريبية من Aspose.CAD؟**  
ج: نعم، يمكنك تنزيل نسخة تجريبية مجانية من [هنا](https://releases.aspose.com/).

**س: كيف يمكنني الحصول على ترخيص مؤقت لـ Aspose.CAD؟**  
ج: يمكنك الحصول على ترخيص مؤقت من [هنا](https://purchase.aspose.com/temporary-license/).

**س: أين يمكنني العثور على دعم إضافي لـ Aspose.CAD؟**  
ج: زر [منتدى Aspose.CAD](https://forum.aspose.com/c/cad/19) للحصول على دعم المجتمع والنقاشات.

**س: هل يمكنني تخصيص خيارات التصدير لصيغ صور مختلفة؟**  
ج: بالتأكيد! توفر Aspose.CAD مجموعة من الخيارات للتخصيص، مما يتيح لك تعديل عملية التصدير وفقًا لمتطلباتك الخاصة.

---

**آخر تحديث:** 2026-03-05  
**تم الاختبار مع:** Aspose.CAD 24.12 لـ .NET  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}