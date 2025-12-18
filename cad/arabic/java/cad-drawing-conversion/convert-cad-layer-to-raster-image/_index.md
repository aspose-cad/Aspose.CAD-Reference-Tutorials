---
date: 2025-12-18
description: تعلم كيفية تنفيذ برنامج تعليمي لـ Aspose CAD بلغة Java يحول طبقات CAD
  إلى صور نقطية بسهولة. اتبع دليلنا خطوة بخطوة لتصور المستند بسلاسة.
linktitle: Convert CAD Layer to Raster Image Format
second_title: Aspose.CAD Java API
title: دليل Aspose CAD Java – تحويل طبقة CAD إلى تنسيق صورة نقطية
url: /ar/java/cad-drawing-conversion/convert-cad-layer-to-raster-image/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# دليل Aspose CAD Java: تحويل طبقة CAD إلى تنسيق صورة نقطية

## المقدمة

في عالم التصميم بمساعدة الحاسوب (CAD)، يُعد تحويل طبقات CAD الفردية إلى صيغ صور نقطية أمرًا أساسيًا لتسهيل المشاركة والطباعة أو المعالجة اللاحقة للصور. يُظهر لك هذا **aspose cad java tutorial** كيفية الاستفادة من **Aspose.CAD for Java** لاستخراج طبقات محددة وحفظها كملف JPEG (أو أي صيغة نقطية أخرى). في نهاية هذا الدليل ستفهم لماذا يُهم التحويل على مستوى الطبقة، وكيفية تكوين خيارات التحويل إلى صورة نقطية، وكيفية تصدير النتيجة ببضع أسطر من الشيفرة فقط.

## إجابات سريعة
- **ما الذي يغطيه هذا الدليل؟** تحويل طبقات CAD المحددة إلى صور نقطية باستخدام Aspose.CAD for Java.  
- **ما الصيغ المدعومة؟** أي صيغة نقطية يدعمها Aspose (JPEG، PNG، BMP، إلخ).  
- **هل أحتاج إلى ترخيص؟** النسخة التجريبية المجانية تكفي للتطوير؛ الترخيص مطلوب للإنتاج.  
- **ما المتطلبات المسبقة؟** بيئة تطوير Java ومكتبة Aspose.CAD للـ Java.  
- **كم من الوقت تستغرق عملية التنفيذ؟** تقريبًا 10–15 دقيقة للتحويل الأساسي.

## المتطلبات المسبقة

قبل الغوص في الشيفرة، تأكد من توفر ما يلي:

- **بيئة تطوير Java** – JDK 8 أو أعلى مثبتة ومُكوَّنة.  
- **مكتبة Aspose.CAD** – قم بتنزيل وتثبيت مكتبة Aspose.CAD للـ Java من [رابط التحميل](https://releases.aspose.com/cad/java/).  

## استيراد الحزم

في هذه الخطوة، سنستورد الفئات الضرورية للبدء في العمل مع ملفات CAD.

### استيراد فئات Aspose.CAD

في ملف Java الخاص بك، أدرج الاستيرادات المطلوبة من Aspose.CAD:

```java
import com.aspose.cad.Image;


import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
import java.util.ArrayList;
import java.util.Arrays;
import java.util.List;
```

## تحويل طبقة CAD إلى تنسيق صورة نقطية

فيما يلي العملية الكاملة خطوة بخطوة. يتم شرح كل خطوة بلغة بسيطة قبل كتلة الشيفرة، لتعرف بالضبط ما يحدث.

### الخطوة 1: إعداد ملف CAD

أولاً، حدد موقع ملف CAD الخاص بك وحمّله في كائن `Image`.

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

### الخطوة 2: تكوين خيارات التحويل إلى صورة نقطية

أنشئ كائن `CadRasterizationOptions` لتحديد حجم الصورة الناتجة وجودتها.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(500);
rasterizationOptions.setPageHeight(500);
```

### الخطوة 3: تحديد طبقات CAD

أضف أسماء الطبقات التي تريد تحويلها إلى صورة نقطية. في هذا المثال، نقوم بتصدير الطبقة الافتراضية `"0"`.

```java
List<String> stringList = new ArrayList<>(Arrays.asList("0"));
rasterizationOptions.setLayers(stringList);
```

### الخطوة 4: إعداد خيارات JPEG

أنشئ كائن `JpegOptions` (أو أي خيارات صورة نقطية أخرى) واربطه بإعدادات التحويل إلى صورة نقطية.

```java
JpegOptions options = new JpegOptions();
options.setVectorRasterizationOptions(rasterizationOptions);
```

### الخطوة 5: التصدير إلى JPEG

أخيرًا، احفظ الطبقة المحوّلة كملف JPEG.

```java
image.save(dataDir + "CADLayersToRasterImageFormats_out_.jpg", options);
```

كرر الخطوات السابقة للطبقات الإضافية أو عدّل معلمات التحويل إلى صورة نقطية (الدقة، لون الخلفية، إلخ) لتلبية متطلباتك الخاصة.

## لماذا نستخدم هذا النهج؟

- **التصدير الانتقائي** – يتم عرض الطبقات التي تحتاجها فقط، مما يقلل حجم الملف ووقت المعالجة.  
- **مرونة الصيغ** – يمكن استبدال `JpegOptions` بـ `PngOptions` أو `BmpOptions` وغيرها دون تعديل المنطق الأساسي.  
- **عرض عالي الجودة** – يحافظ Aspose.CAD على سماكة الخطوط والألوان والنصوص كما هي في ملف CAD الأصلي.

## المشكلات الشائعة & استكشاف الأخطاء وإصلاحها

| العَرَض | السبب المحتمل | الحل |
|---------|--------------|-----|
| صورة فارغة | لم يتم تحديد طبقات أو تم كتابة اسم طبقة غير صحيح | تحقق من وجود أسماء الطبقات في ملف CAD؛ استخدم `image.getLayers()` لعرضها. |
| دقة منخفضة | DPI الافتراضي منخفض | عيّن `rasterizationOptions.setResolution(300);` (أو أعلى) قبل الحفظ. |
| صيغة CAD غير مدعومة | استخدام نسخة قديمة من Aspose.CAD | حدّث إلى أحدث إصدار من Aspose.CAD for Java. |

## الأسئلة المتكررة

**س: هل يمكنني استخدام Aspose.CAD for Java مع لغات برمجة أخرى؟**  
ج: يدعم Aspose.CAD أساسًا Java، لكن هناك إصدارات لـ .NET، C++، ولغات أخرى متاحة.

**س: أين يمكنني العثور على دعم إضافي أو مساعدة؟**  
ج: لأي استفسارات أو مساعدة، تفضل بزيارة [منتدى Aspose.CAD](https://forum.aspose.com/c/cad/19).

**س: هل تتوفر نسخة تجريبية مجانية؟**  
ج: نعم، يمكنك استكشاف Aspose.CAD بالحصول على نسخة تجريبية مجانية من [هنا](https://releases.aspose.com/).

**س: كيف يمكنني الحصول على ترخيص مؤقت لـ Aspose.CAD؟**  
ج: احصل على ترخيص مؤقت من [هذا الرابط](https://purchase.aspose.com/temporary-license/).

**س: هل هناك متطلبات نظام محددة لـ Aspose.CAD for Java؟**  
ج: تأكد من أن لديك بيئة تطوير Java متوافقة؛ راجع الوثائق للحصول على المتطلبات التفصيلية.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**آخر تحديث:** 2025-12-18  
**تم الاختبار مع:** Aspose.CAD for Java 24.12 (latest at time of writing)  
**المؤلف:** Aspose