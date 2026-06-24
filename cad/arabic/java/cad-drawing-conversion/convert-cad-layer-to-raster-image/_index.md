---
date: 2026-04-13
description: تعلم كيفية تحويل طبقة CAD إلى صورة نقطية باستخدام Aspose.CAD للـ Java.
  يوضح هذا الدليل خطوة بخطوة التحويل على مستوى الطبقة إلى صور نقطية.
keywords:
- java rasterize cad layer
- Aspose CAD Java
- convert CAD layer to raster
linktitle: تحويل طبقة CAD إلى تنسيق صورة نقطية
second_title: Aspose.CAD Java API
title: جافا تحويل طبقة CAD إلى رستر – دليل Aspose CAD
url: /ar/java/cad-drawing-conversion/convert-cad-layer-to-raster-image/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# دليل Aspose CAD Java: تحويل طبقة CAD إلى تنسيق صورة نقطية

## المقدمة

إذا كنت بحاجة إلى **java rasterize cad layer** للملفات لتسهيل المشاركة أو الطباعة أو معالجة الصور اللاحقة، فأنت في المكان الصحيح. في هذا الدرس سنستعرض كيف يتيح لك Aspose.CAD for Java اختيار طبقات فردية من رسم CAD وتصديرها كصور نقطية عالية الجودة مثل JPEG أو PNG أو BMP. في النهاية ستفهم لماذا تعتبر الرسترزة الانتقائية مهمة، وكيفية تكوين خيارات الرسترزة، وكيفية حفظ النتيجة ببضع أسطر من الشيفرة فقط.

## إجابات سريعة

- **What does this tutorial cover?** تحويل طبقات CAD المحددة إلى صور نقطية باستخدام Aspose.CAD for Java.  
- **Which formats are supported?** أي تنسيق نقطي يدعمه Aspose (JPEG، PNG، BMP، إلخ).  
- **Do I need a license?** النسخة التجريبية المجانية تعمل للتطوير؛ يلزم وجود ترخيص للإنتاج.  
- **What are the prerequisites?** بيئة تطوير Java ومكتبة Aspose.CAD Java.  
- **How long does implementation take?** تقريبًا 10–15 دقيقة للتحويل الأساسي.

## ما هو “java rasterize cad layer”؟

تعني عملية رسترزة طبقة CAD تحويل بيانات المتجهات لتلك الطبقة المحددة إلى صورة مبنية على البكسل. تحافظ هذه العملية على المظهر البصري للطبقة مع جعلها متوافقة مع أي نظام يمكنه عرض تنسيقات الصور القياسية.

## لماذا تستخدم هذا النهج؟

- **Selective Export** – يتم تصيير الطبقات التي تحتاجها فقط، مما يقلل من حجم الملف ووقت المعالجة.  
- **Format Flexibility** – استبدل `JpegOptions` بـ `PngOptions` أو `BmpOptions`، دون تغيير المنطق الأساسي.  
- **High‑Quality Rendering** – يحافظ Aspose.CAD على أوزان الخطوط والألوان والنصوص تمامًا كما في ملف CAD الأصلي.

## المتطلبات المسبقة

قبل الغوص في الشيفرة، تأكد من توفر ما يلي:

- **Java Development Environment** – JDK 8 أو أعلى مثبت ومُكوَّن.  
- **Aspose.CAD Library** – قم بتنزيل وتثبيت مكتبة Aspose.CAD للـ Java من [رابط التحميل](https://releases.aspose.com/cad/java/).

## استيراد الحزم

في هذه الخطوة، سنستورد الفئات اللازمة لبدء العمل مع ملفات CAD.

### استيراد فئات Aspose.CAD

في ملف مصدر Java الخاص بك، أدرج الاستيرادات المطلوبة من Aspose.CAD:

```java
import com.aspose.cad.Image;


import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
import java.util.ArrayList;
import java.util.Arrays;
import java.util.List;
```

## تحويل طبقة CAD إلى تنسيق صورة نقطية

فيما يلي العملية الكاملة خطوة بخطوة. يتم شرح كل خطوة بلغة بسيطة قبل كتلة الشيفرة، حتى تعرف بالضبط ما يحدث.

### الخطوة 1: إعداد ملف CAD

أولًا، حدد موقع ملف CAD الخاص بك وحمّله في كائن `Image`.

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

### الخطوة 2: تكوين خيارات الرسترزة

أنشئ مثيلًا من `CadRasterizationOptions` لتحديد حجم وجودة صورة الإخراج.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(500);
rasterizationOptions.setPageHeight(500);
```

### الخطوة 3: تحديد طبقات CAD

أضف أسماء الطبقات التي تريد رسترزتها. في هذا المثال، نقوم بتصدير الطبقة الافتراضية `"0"`.

```java
List<String> stringList = new ArrayList<>(Arrays.asList("0"));
rasterizationOptions.setLayers(stringList);
```

### الخطوة 4: إعداد خيارات JPEG

أنشئ كائن `JpegOptions` (أو أي خيارات صورة نقطية أخرى) واربطه بإعدادات الرسترزة.

```java
JpegOptions options = new JpegOptions();
options.setVectorRasterizationOptions(rasterizationOptions);
```

### الخطوة 5: تصدير إلى JPEG

أخيرًا، احفظ الطبقة المرسومة كملف JPEG.

```java
image.save(dataDir + "CADLayersToRasterImageFormats_out_.jpg", options);
```

كرر الخطوات السابقة للطبقات الإضافية أو عدّل معلمات الرسترزة (الدقة، لون الخلفية، إلخ) لتلبية متطلباتك الخاصة.

## المشكلات الشائعة واستكشاف الأخطاء

| العَرَض | السبب المحتمل | الحل |
|---------|--------------|-----|
| صورة فارغة | لم يتم تحديد طبقات أو اسم الطبقة غير صحيح | تحقق من وجود أسماء الطبقات في ملف CAD؛ استخدم `image.getLayers()` لعرضها. |
| دقة منخفضة | DPI الافتراضي منخفض | اضبط `rasterizationOptions.setResolution(300);` (أو أعلى) قبل الحفظ. |
| تنسيق CAD غير مدعوم | استخدام نسخة قديمة من Aspose.CAD | قم بتحديث إلى أحدث إصدار من Aspose.CAD for Java. |

## الأسئلة المتكررة

**س: هل يمكنني استخدام Aspose.CAD for Java مع لغات برمجة أخرى؟**  
ج: Aspose.CAD يدعم Java في المقام الأول، لكن هناك إصدارات للـ .NET و C++ ولغات أخرى متاحة.

**س: أين يمكنني العثور على دعم أو مساعدة إضافية؟**  
ج: لأي استفسارات أو مساعدة، زر [منتدى Aspose.CAD](https://forum.aspose.com/c/cad/19).

**س: هل هناك نسخة تجريبية مجانية متاحة؟**  
ج: نعم، يمكنك استكشاف Aspose.CAD بالحصول على نسخة تجريبية مجانية من [هنا](https://releases.aspose.com/).

**س: كيف يمكنني الحصول على ترخيص مؤقت لـ Aspose.CAD؟**  
ج: احصل على ترخيص مؤقت من [هذا الرابط](https://purchase.aspose.com/temporary-license/).

**س: هل هناك متطلبات نظام محددة لـ Aspose.CAD for Java؟**  
ج: تأكد من أن لديك بيئة تطوير Java متوافقة؛ راجع الوثائق للحصول على المتطلبات التفصيلية.

---

**آخر تحديث:** 2026-04-13  
**تم الاختبار مع:** Aspose.CAD for Java 24.12 (latest at time of writing)  
**المؤلف:** Aspose

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}