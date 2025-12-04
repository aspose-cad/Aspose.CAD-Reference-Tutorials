---
date: 2025-12-04
description: تعلم كيفية تحويل تخطيط DXF إلى JPEG باستخدام Aspose.CAD للغة Java – دليل
  خطوة بخطوة حول كيفية تصدير DXF إلى صورة بكفاءة.
language: ar
linktitle: Export Specific DXF Layout to Image with Java
second_title: Aspose.CAD Java API
title: كيفية تحويل تخطيط DXF إلى صورة JPEG باستخدام Aspose.CAD في Java
url: /java/additional-features/export-specific-layout-to-image/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تحويل تخطيط DXF إلى صورة JPEG باستخدام Aspose.CAD في Java  

إذا كنت بحاجة إلى **تحويل تخطيط DXF إلى صورة JPEG** بسرعة وبشكل موثوق، فأنت في المكان الصحيح. في هذا البرنامج التعليمي سنستعرض الخطوات الدقيقة المطلوبة **لتصدير تخطيط DXF محدد إلى JPEG** باستخدام مكتبة Aspose.CAD للغة Java. في النهاية، ستفهم لماذا يعمل هذا النهج، وكيفية تخصيص إعدادات الترصيص، وكيفية دمج الحل في مشاريعك الخاصة.

## إجابات سريعة
- **ما المكتبة التي أحتاجها؟** Aspose.CAD للغة Java (قم بتنزيلها من الموقع الرسمي).  
- **هل يمكنني استهداف تخطيط واحد فقط؟** نعم – تحدد الطبقات المطلوبة قبل عملية الترصيص.  
- **ما صيغ الإخراج المدعومة؟** JPEG، PNG، BMP، TIFF، PDF، وأكثر.  
- **هل أحتاج إلى ترخيص للاستخدام في الإنتاج؟** الترخيص التجاري مطلوب للاستخدام غير التجريبي.  
- **هل الكود متوافق مع Java 8+؟** بالتأكيد – الـ API يعمل مع Java 8 والإصدارات الأحدث.

## المتطلبات السابقة
قبل أن تبدأ، تأكد من وجود ما يلي:

- **Aspose.CAD للغة Java** مثبتة (قم بتنزيلها من [صفحة تنزيل Aspose CAD Java](https://releases.aspose.com/cad/java/)).  
- بيئة تطوير Java (JDK 8 أو أحدث).  
- ملف DXF (أو DWF) يحتوي على التخطيط الذي تريد تحويله.

## استيراد المساحات الاسمية  

للتعامل مع ملف CAD، استورد الفئات المطلوبة:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.fileformats.dwf.whip.objects.DwfWhipLayer;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.dwf.DwfImage;
import com.aspose.cad.imageoptions.JpegOptions;
import java.util.ArrayList;
import java.util.Arrays;
import java.util.List;
```

### الخطوة 1 – تحديد دليل الموارد  
عرّف مكان ملف DXF/DWF المصدر:

```java
String dataDir = "Your Document Directory" + "DXFDrawings\\";
```

> **نصيحة احترافية:** استخدم مسارًا مطلقًا أثناء التطوير لتجنب أخطاء “الملف غير موجود”.

### الخطوة 2 – تحميل صورة DXF/DWF  

```java
String srcFile = dataDir + "for_layers_test.dwf";
DwfImage image = (DwfImage) Image.load(srcFile);
```

استبدل *for_layers_test.dwf* باسم ملف الرسم الخاص بك.

### الخطوة 3 – الحصول على أسماء الطبقات  

```java
List<String> layersNames = image.getLayers().getLayersNames();
```

تُعيد هذه الدالة جميع الطبقات الموجودة في الرسم، مما يتيح لك اختيار الطبقة الدقيقة التي تريد **تحويل تخطيط dxf إلى jpeg**.

### الخطوة 4 – ضبط خيارات الترصيص  

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
```

عدّل `PageWidth` و `PageHeight` للتحكم في دقة صورة JPEG الناتجة.

### الخطوة 5 – تحديد الطبقات التي سيتم تصديرها  

```java
String[] stringArray = Arrays.copyOf(layersNames.toArray(), layersNames.toArray().length, String[].class);
List<String> stringList = Arrays.asList(stringArray);
rasterizationOptions.setLayers(stringList);
```

بتمرير أسماء الطبقات المطلوبة فقط، تضمن أن **كيفية تصدير dxf إلى صورة** ستركز على التخطيط الذي تحتاجه.

### الخطوة 6 – تكوين خيارات JPEG  

```java
JpegOptions jpegOptions = new JpegOptions();
jpegOptions.setVectorRasterizationOptions(rasterizationOptions);
```

هذه الخيارات تربط إعدادات الترصيص بمرمز JPEG.

### الخطوة 7 – تصدير التخطيط إلى ملف JPEG  

```java
String output = dataDir + "for_layers_test.jpg";
image.save(output, jpegOptions);
```

غيّر اسم ملف الإخراج والمسار حسب متطلبات مشروعك.

> **ماذا حدث للتو؟**  
> تم ترصيص تخطيط DXF باستخدام مرشح الطبقة الذي حددته، ثم حفظه كصورة JPEG عالية الجودة.

## لماذا تحويل تخطيط DXF إلى JPEG؟
- **معاينات بصرية سريعة** – ملفات JPEG خفيفة ويمكن عرضها في المتصفحات دون إضافات.  
- **التكامل مع أدوات التقارير** – العديد من محركات التقارير تقبل الصور ولكن ليس ملفات CAD الأصلية.  
- **لقطات أرشيفية** – احفظ تمثيلًا بكسليًا دقيقًا لتخطيط محدد لأغراض التوثيق.

## المشكلات الشائعة & استكشاف الأخطاء
| العَرَض | السبب المحتمل | الحل |
|---------|--------------|-----|
| صورة فارغة | لم يتم اختيار أي طبقة | تحقق من أن `rasterizationOptions.setLayers()` يحتوي على أسماء الطبقات الصحيحة. |
| إخراج منخفض الدقة | قيم `PageWidth/PageHeight` صغيرة | زد الأبعاد (مثلاً 2400 × 2400). |
| استثناء `Unsupported format` | استخدام نسخة قديمة من Aspose.CAD | قم بالترقية إلى أحدث إصدار من المكتبة. |

## الأسئلة المتكررة  

**س: هل يمكنني تصدير تخطيطات DXF متعددة في تشغيل واحد؟**  
ج: نعم. قم بالتكرار عبر قائمة الطبقات المطلوبة، عدّل `rasterizationOptions.setLayers()` لكل دورة، واستدعِ `image.save()` باسم ملف فريد.

**س: هل Aspose.CAD للغة Java متوافق مع جميع إصدارات Java؟**  
ج: المكتبة تدعم Java 8 والإصدارات الأحدث. راجع ملاحظات الإصدار الرسمية لأي ملاحظات خاصة بالإصدارات.

**س: كيف أتعامل مع الأخطاء أثناء التحويل؟**  
ج: احطّ كود التحميل والحفظ بكتلة `try‑catch` وسجّل تفاصيل `IOException` أو `CadException`.

**س: إلى جانب JPEG، ما الصيغ الأخرى التي يمكنني إنشاؤها؟**  
ج: PNG، BMP، TIFF، وPDF كلها مدعومة. ما عليك سوى استبدال `JpegOptions` بالفئة المقابلة (`PngOptions`، `BmpOptions`، إلخ).

**س: هل يمكنني تخصيص الترصيص أكثر (مثل وزن الخط، لون الخلفية)؟**  
ج: بالتأكيد. توفر `CadRasterizationOptions` خصائص مثل `setBackgroundColor()`، `setLineWeight()`، و `setRenderMode()` للتحكم الدقيق.

## الخلاصة
أصبح لديك الآن طريقة كاملة وجاهزة للإنتاج **لتحويل تخطيط DXF إلى صورة JPEG** باستخدام Aspose.CAD للغة Java. من خلال اختيار طبقات محددة، ضبط خيارات الترصيص، وحفظ الصورة بإعدادات JPEG، يمكنك إنشاء معاينات أو أصول توثيق عالية الجودة في بضع أسطر من الكود فقط.

---

**آخر تحديث:** 2025-12-04  
**تم الاختبار مع:** Aspose.CAD للغة Java 24.12 (أحدث نسخة وقت الكتابة)  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}