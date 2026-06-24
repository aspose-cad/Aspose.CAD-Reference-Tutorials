---
date: 2026-02-20
description: تعلم كيفية تصدير PDF من AutoCAD باستخدام Aspose.CAD للـ Java. يوضح لك
  هذا الدليل خطوة بخطوة كيفية **تحويل DWG إلى PDF**، **حفظ CAD كملف PDF**، وكيفية
  التعامل مع الترخيص.
linktitle: Export AutoCAD Images to PDF
second_title: Aspose.CAD Java API
title: تحويل DWG إلى PDF - تصدير صور AutoCAD إلى PDF باستخدام Aspose.CAD للـ Java
url: /ar/java/cad-export-options/export-autocad-images-to-pdf/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تصدير AutoCAD PDF - تصدير صور AutoCAD إلى PDF باستخدام Aspose.CAD للغة Java

## مقدمة

هل تبحث عن **تحويل DWG إلى PDF** باستخدام Java؟ لا تبحث أكثر! في هذا الدرس سنرشدك إلى تحويل صور AutoCAD إلى PDF باستخدام Aspose.CAD للغة Java، مكتبة قوية تجعل عملية **تحويل DWG إلى PDF** سهلة. في النهاية ستفهم كيفية **حفظ CAD كـ PDF**، وتطبيق إعدادات الترصيص المخصصة، والعمل برخصة Aspose.CAD للاستخدام الإنتاجي.

## إجابات سريعة
- **هل يمكنني تحويل DWG إلى PDF باستخدام Java؟** نعم، Aspose.CAD للغة Java يدعم DWG وDXF والعديد من الصيغ الأخرى.  
- **هل أحتاج إلى رخصة؟** رخصة **Aspose CAD** مطلوبة للاستخدام غير المحدود؛ رخصة مؤقتة متاحة للتقييم.  
- **ما نسخة Java المدعومة؟** Java 8+ (المكتبة متوافقة مع جميع إصدارات JDK الحديثة).  
- **هل يمكنني تخصيص حجم صفحة PDF؟** بالتأكيد – عدل `pageWidth` و `pageHeight` في خيارات الترصيص.  
- **هل الترصيص ثلاثي الأبعاد ممكن؟** نعم، فعّل `TypeOfEntities.Entities3D` للحصول على عرض ثلاثي الأبعاد كامل.

## ما هو **export autocad pdf**؟
تصدير AutoCAD PDF يعني تحويل رسومات CAD القائمة على المتجهات (DWG، DXF، DWF، إلخ) إلى مستند PDF محمول مع الحفاظ على الطبقات، وزن الخطوط، وإمكانية تضمين الهندسة ثلاثية الأبعاد. هذا مفيد لمشاركة التصاميم مع العملاء، الأرشفة، أو الطباعة دون الحاجة إلى برنامج CAD.

## لماذا تحويل DWG إلى PDF باستخدام Aspose.CAD للغة Java؟
- **دعم كامل للملفات** – يعمل مع DWG، DXF، DWF، والعديد غيرها.  
- **بدون تبعيات خارجية** – مكتبة Java صافية، لا تحتاج إلى DLLs أصلية.  
- **ترصيص عالي الجودة** – تحكم في DPI، حجم الصفحة، والتخطيط، بحيث يمكنك **تخصيص حجم صفحة PDF** ليتناسب مع متطلبات مشروعك.  
- **مرونة الترخيص** – ابدأ بتجربة مجانية، ثم ارتقِ إلى رخصة **Aspose CAD** دائمة.  

## المتطلبات المسبقة

قبل البدء، تأكد من وجود التالي:

- **بيئة تطوير Java** – JDK 8 أو أحدث مثبتة.  
- **مكتبة Aspose.CAD للغة Java** – قم بتنزيلها من [رابط التحميل](https://releases.aspose.com/cad/java/).  
- **دليل المستندات** – مجلد على جهازك حيث ستوجد ملفات CAD المصدرية وملفات PDF المولدة.

## استيراد المساحات الاسمية

في مشروع Java الخاص بك، استورد الفئات اللازمة للعمل مع Aspose.CAD:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
//import com.aspose.cad.imageoptions.TypeOfEntities;
```

الآن دعنا نستعرض الشيفرة خطوة بخطوة.

## كيفية تحويل DWG إلى PDF باستخدام Aspose.CAD للغة Java

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

> **لماذا هذا مهم:** تحميل ملف CAD إلى كائن `Image` يمنحك وصولًا كاملًا إلى محرك الترصيص الخاص بـ Aspose.CAD.

### الخطوة 3: تعيين خيارات الترصيص

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(500);
rasterizationOptions.setPageHeight(500);
// rasterizationOptions.setTypeOfEntities(TypeOfEntities.Entities3D);

rasterizationOptions.setLayouts(new String[] {"Model"});
```

- عدل `pageWidth` و `pageHeight` لت **تخصيص حجم صفحة PDF**.  
- ألغِ التعليق عن سطر `setTypeOfEntities` إذا كنت بحاجة إلى **java convert cad pdf** للكيانات ثلاثية الأبعاد.  
- استدعاء `setLayouts` يحدد أي تخطيط (Model، Layout1، إلخ) سيتم عرضه.

### الخطوة 4: تكوين خيارات PDF

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

هذا يربط إعدادات الترصيص بمخرجات PDF، مما يضمن تحويل البيانات المتجهة بشكل صحيح.

### الخطوة 5: حفظ PDF

```java
cadImage.save(dataDir + "Export3DImagestoPDF_out_.pdf", pdfOptions);
```

الملف الناتج، `Export3DImagestoPDF_out_.pdf`، هو تمثيل **save cad as pdf** لرسم AutoCAD الأصلي الخاص بك.

## المشكلات الشائعة والحلول

| العَرَض | السبب المحتمل | الحل |
|---------|--------------|-----|
| ملف PDF فارغ | لم يتم تعيين خيارات الترصيص أو عدم تطابق التخطيط | تحقق من أن `setLayouts` يطابق اسم التخطيط في ملف CAD الخاص بك. |
| صورة منخفضة الدقة | `pageWidth`/`pageHeight` صغير جدًا | زيادة الأبعاد أو تعيين DPI أعلى عبر `rasterizationOptions.setResolution(...)`. |
| استثناء الترخيص | لم يتم تطبيق رخصة صالحة | طبق رخصة **Aspose CAD** أو استخدم رخصة مؤقتة للاختبار. |

## الأسئلة المتكررة

### س1: هل يمكنني استخدام Aspose.CAD للغة Java مع صيغ ملفات CAD أخرى؟
نعم، يدعم Aspose.CAD مجموعة واسعة من الصيغ بما في ذلك DWG، DWF، DGN، وغيرها، مما يمنحك مرونة في مشاريعك.

### س2: كيف يمكنني الحصول على رخصة مؤقتة لـ Aspose.CAD للغة Java؟
قم بزيارة [هنا](https://purchase.aspose.com/temporary-license/) للحصول على رخصة مؤقتة للتقييم.

### س3: هل هناك خيارات تخطيط للترصيص؟
نعم، يمكنك تخصيص التخطيطات (مثل `"Model"`، `"Layout1"`) عبر طريقة `setLayouts` للتحكم في أي عرض يتم عرضه.

### س4: هل يمكنني تخصيص حجم ملف PDF الناتج؟
بالطبع! عدل معلمات `pageWidth` و `pageHeight` في خيارات الترصيص لتتناسب مع الأبعاد المطلوبة.

### س5: أين يمكنني طلب المساعدة أو مناقشة المشكلات المتعلقة بـ Aspose.CAD للغة Java؟
توجه إلى [منتدى Aspose.CAD](https://forum.aspose.com/c/cad/19) للحصول على دعم مخصص ومناقشات المجتمع.

**آخر تحديث:** 2026-02-20  
**تم الاختبار مع:** Aspose.CAD للغة Java 24.10  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}