---
date: 2025-12-19
description: تعلم كيفية تصدير ملفات PDF من AutoCAD باستخدام Aspose.CAD للغة Java.
  يوضح لك هذا الدليل خطوة بخطوة كيفية تحويل DWG إلى PDF، وحفظ CAD كملف PDF، والتعامل
  مع الترخيص.
linktitle: Export AutoCAD Images to PDF
second_title: Aspose.CAD Java API
title: تصدير PDF من AutoCAD - تصدير صور AutoCAD إلى PDF باستخدام Aspose.CAD لجافا
  (دليل تعليمي)
url: /ar/java/cad-export-options/export-autocad-images-to-pdf/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تصدير AutoCAD PDF - تصدير صور AutoCAD إلى PDF باستخدام Aspose.CAD للـ Java

## المقدمة

هل تبحث عن طريقة لتصدير **AutoCAD PDF** بسلاسة باستخدام Java؟ لا تبحث أكثر! في هذا الدرس سنرشدك خطوة بخطوة إلى تحويل صور AutoCAD إلى PDF باستخدام Aspose.CAD للـ Java، مكتبة قوية تجعل عملية **تحويل DWG إلى PDF** سهلة. في النهاية ستفهم كيفية **حفظ CAD كـ PDF**، وتطبيق إعدادات رستر مخصصة، والعمل مع ترخيص Aspose.CAD للاستخدام الإنتاجي.

## إجابات سريعة
- **هل يمكنني تحويل DWG إلى PDF باستخدام Java؟** نعم، Aspose.CAD للـ Java يدعم DWG وDXF والعديد من الصيغ الأخرى.  
- **هل أحتاج إلى ترخيص؟** يتطلب **ترخيص Aspose CAD** لاستخدام غير محدود؛ ترخيص مؤقت متاح للتقييم.  
- **ما نسخة Java المدعومة؟** Java 8+ (المكتبة متوافقة مع جميع إصدارات JDK الحديثة).  
- **هل يمكنني تخصيص حجم صفحة PDF؟** بالتأكيد – عدل `pageWidth` و `pageHeight` في خيارات الرستر.  
- **هل يمكن إجراء رستر ثلاثي الأبعاد؟** نعم، فعّل `TypeOfEntities.Entities3D` للحصول على رندرة ثلاثية الأبعاد كاملة.

## ما هو **تصدير AutoCAD PDF**؟
يعني تصدير AutoCAD PDF تحويل رسومات CAD القائمة على المتجهات (DWG، DXF، DWF، إلخ) إلى مستند PDF محمول مع الحفاظ على الطبقات، وزن الخطوط، وإمكانية تضمين الهندسة ثلاثية الأبعاد. هذا مفيد لمشاركة التصاميم مع العملاء، الأرشفة، أو الطباعة دون الحاجة إلى برنامج CAD.

## لماذا تستخدم Aspose.CAD للـ Java لت **تصدير AutoCAD PDF**؟
- **دعم كامل للملفات** – يعمل مع DWG وDXF وDWF والعديد غيرها.  
- **بدون تبعيات خارجية** – مكتبة Java صافية، لا تحتاج إلى DLLs أصلية.  
- **رستر عالي الجودة** – تحكم في DPI، حجم الصفحة، والتخطيط.  
- **مرونة الترخيص** – ابدأ بتجربة مجانية، ثم ارتقِ إلى **ترخيص Aspose CAD** دائم.  

## المتطلبات المسبقة

- **بيئة تطوير Java** – JDK 8 أو أحدث مثبت.  
- **مكتبة Aspose.CAD للـ Java** – حمّلها من [رابط التحميل](https://releases.aspose.com/cad/java/).  
- **دليل المستندات** – مجلد على جهازك حيث توجد ملفات CAD المصدر والملفات PDF المولدة.

## استيراد الحزم

في مشروع Java الخاص بك، استورد الفئات اللازمة للعمل مع Aspose.CAD:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
//import com.aspose.cad.imageoptions.TypeOfEntities;
```

الآن دعنا نستعرض الكود خطوة بخطوة.

## دليل خطوة بخطوة

### الخطوة 1: تعيين مسار دليل الموارد

```java
String dataDir = "Your Document Directory" + "ExportingCAD/";
```

> **نصيحة احترافية:** استبدل `"Your Document Directory"` بالمسار المطلق للمجلد الذي أنشأته في المتطلبات المسبقة.

### الخطوة 2: تحميل صورة CAD

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image cadImage = Image.load(srcFile);
```

> **لماذا هذا مهم:** تحميل ملف CAD إلى كائن `Image` يمنحك وصولًا كاملًا إلى محرك الرستر الخاص بـ Aspose.CAD.

### الخطوة 3: تعيين خيارات الرستر

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(500);
rasterizationOptions.setPageHeight(500);
// rasterizationOptions.setTypeOfEntities(TypeOfEntities.Entities3D);

rasterizationOptions.setLayouts(new String[] {"Model"});
```

- عدّل `pageWidth` و `pageHeight` لتغيير حجم ملف PDF الناتج.  
- ألغِ التعليق عن سطر `setTypeOfEntities` إذا كنت تحتاج إلى **java convert cad pdf** للكيانات ثلاثية الأبعاد.  
- استدعاء `setLayouts` يحدد أي تخطيط (Model، Layout1، إلخ) سيتم رندره.

### الخطوة 4: تكوين خيارات PDF

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

هذا يربط إعدادات الرستر بمخرجات PDF، مما يضمن تحويل البيانات المتجهة بشكل صحيح.

### الخطوة 5: حفظ ملف PDF

```java
cadImage.save(dataDir + "Export3DImagestoPDF_out_.pdf", pdfOptions);
```

الملف الناتج، `Export3DImagestoPDF_out_.pdf`، هو تمثيل **حفظ CAD كـ PDF** لرسمك الأصلي في AutoCAD.

## المشكلات الشائعة والحلول

| العَرَض | السبب المحتمل | الحل |
|---------|--------------|-----|
| ملف PDF فارغ | لم يتم ضبط خيارات الرستر أو عدم تطابق التخطيط | تحقق من أن `setLayouts` يطابق اسم التخطيط في ملف CAD الخاص بك. |
| صورة منخفضة الدقة | `pageWidth`/`pageHeight` صغير جدًا | زيادة الأبعاد أو ضبط DPI أعلى عبر `rasterizationOptions.setResolution(...)`. |
| استثناء الترخيص | لم يتم تطبيق ترخيص صالح | طبق **ترخيص Aspose CAD** أو استخدم ترخيصًا مؤقتًا للاختبار. |

## الأسئلة المتكررة

### Q1: هل يمكنني استخدام Aspose.CAD للـ Java مع صيغ ملفات CAD أخرى؟
نعم، Aspose.CAD يدعم مجموعة واسعة من الصيغ بما فيها DWG وDWF وDGN وغيرها، مما يمنحك مرونة في مشاريعك.

### Q2: كيف يمكنني الحصول على ترخيص مؤقت لـ Aspose.CAD للـ Java؟
زر [هنا](https://purchase.aspose.com/temporary-license/) للحصول على ترخيص مؤقت للتقييم.

### Q3: هل هناك خيارات تخطيط للرستر؟
نعم، يمكنك تخصيص التخطيطات (مثل `"Model"`، `"Layout1"`) عبر طريقة `setLayouts` للتحكم في العرض الذي يتم رندره.

### Q4: هل يمكنني تخصيص حجم ملف PDF الناتج؟
بالطبع! عدّل معلمات `pageWidth` و `pageHeight` في خيارات الرستر لتناسب الأبعاد المطلوبة.

### Q5: أين يمكنني طلب المساعدة أو مناقشة المشكلات المتعلقة بـ Aspose.CAD للـ Java؟
توجه إلى [منتدى Aspose.CAD](https://forum.aspose.com/c/cad/19) للحصول على دعم مخصص ومناقشات المجتمع.

---

**آخر تحديث:** 2025-12-19  
**تم الاختبار مع:** Aspose.CAD for Java 24.10  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}