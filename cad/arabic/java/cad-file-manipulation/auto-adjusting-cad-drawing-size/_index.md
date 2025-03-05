---
title: الضبط التلقائي لحجم رسم CAD باستخدام Aspose.CAD لـ Java
linktitle: الضبط التلقائي لحجم رسم CAD
second_title: Aspose.CAD جافا API
description: استكشف العملية السلسة للضبط التلقائي لأحجام رسم CAD في Java باستخدام Aspose.CAD. اتبع دليلنا خطوة بخطوة لمعالجة ملفات CAD بكفاءة.
type: docs
weight: 13
url: /ar/java/cad-file-manipulation/auto-adjusting-cad-drawing-size/
---
## مقدمة

في عالم CAD (التصميم بمساعدة الكمبيوتر)، يعد ضبط أحجام الرسم مطلبًا شائعًا، ومع Aspose.CAD لـ Java، تصبح عملية سلسة. توفر هذه المكتبة القوية أدوات شاملة للتعامل مع ملفات CAD في تطبيقات Java. في هذا البرنامج التعليمي، سوف نستكشف عملية الضبط التلقائي لأحجام رسم CAD خطوة بخطوة باستخدام Aspose.CAD.

## المتطلبات الأساسية

قبل الغوص في البرنامج التعليمي، تأكد من توفر المتطلبات الأساسية التالية:

1.  بيئة تطوير Java: تأكد من تثبيت Java على جهازك. يمكنك تنزيله[هنا](https://www.java.com/en/download/).

2.  مكتبة Aspose.CAD: قم بتنزيل وتثبيت مكتبة Aspose.CAD لـ Java من[هنا](https://releases.aspose.com/cad/java/).

3. نموذج ملف CAD: احصل على نموذج ملف CAD (على سبيل المثال، Sample.dwg) متاحًا في دليل المستندات لديك.

## استيراد مساحات الأسماء

في تطبيق Java الخاص بك، قم بتضمين مساحات الأسماء اللازمة للاستفادة من وظيفة Aspose.CAD. هنا مثال:

```java

import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

الآن، دعونا نقسم عملية الضبط التلقائي لأحجام رسم CAD إلى خطوات يمكن التحكم فيها.

## الخطوة 1: قم بتحميل رسم CAD

```java
String dataDir = "Your Document Directory" + "CADConversion/";
String sourceFilePath = dataDir + "sample.dwg";
Image objImage = Image.load(sourceFilePath);
```

تتضمن هذه الخطوة تحميل رسم CAD من مسار الملف المحدد.

## الخطوة 2: إنشاء BmpOptions

```java
BmpOptions bmpOptions = new BmpOptions();
```

 إنشاء مثيل`BmpOptions` فئة، والتي سيتم استخدامها لتعيين خيارات مختلفة لتنسيق BMP.

## الخطوة 3: إنشاء CadRasterizationOptions

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
bmpOptions.setVectorRasterizationOptions(cadRasterizationOptions);
```

 إنشاء مثيل ل`CadRasterizationOptions` لتخصيص إعدادات التنقيط لملف CAD.

## الخطوة 4: تعيين خاصية التخطيطات

```java
cadRasterizationOptions.setLayouts(new String[]{"Model"});
```

حدد التخطيطات التي تريد تضمينها في الإخراج. في هذه الحالة، نستخدم تخطيط "النموذج".

## الخطوة 5: التصدير إلى تنسيق BMP

```java
String outPath = sourceFilePath + ".bmp";
objImage.save(outPath, bmpOptions);
```

وأخيرًا، احفظ رسم CAD المعدل بتنسيق BMP في مسار الإخراج المحدد.

كرر هذه الخطوات في تطبيق Java الخاص بك، وستنجح في ضبط حجم رسم CAD تلقائيًا باستخدام Aspose.CAD لـ Java.

## خاتمة

في هذا البرنامج التعليمي، تناولنا عملية الضبط التلقائي لأحجام رسم CAD باستخدام Aspose.CAD لـ Java. تعمل هذه المكتبة على تبسيط معالجة ملفات CAD، مما يوفر حلاً قويًا للمطورين.

## الأسئلة الشائعة

### س 1: هل Aspose.CAD متوافق مع تنسيقات ملفات CAD المختلفة؟

ج1: نعم، يدعم Aspose.CAD تنسيقات CAD المتنوعة، بما في ذلك DWG وDXF وDGN والمزيد.

### س2: هل يمكنني استخدام Aspose.CAD للمشاريع التجارية؟

 ج2: بالتأكيد! يزور[هنا](https://purchase.aspose.com/buy) لاستكشاف خيارات الترخيص.

### س3: كيف يمكنني الحصول على تراخيص مؤقتة لأغراض الاختبار؟

 ج3: الحصول على ترخيص مؤقت[هنا](https://purchase.aspose.com/temporary-license/) للاختبار والتقييم.

### س4: أين يمكنني العثور على الدعم لـ Aspose.CAD؟

 ج4: انضم إلى مجتمع Aspose.CAD[المنتدى](https://forum.aspose.com/c/cad/19) للمساعدة والمناقشات.

### س5: هل هناك نسخة تجريبية مجانية متاحة لـ Aspose.CAD لـ Java؟

 ج5: نعم، يمكنك الوصول إلى النسخة التجريبية المجانية[هنا](https://releases.aspose.com/) لاستكشاف إمكانيات المكتبة.