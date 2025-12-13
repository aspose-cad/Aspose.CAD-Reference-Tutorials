---
date: 2025-12-13
description: تعلم كيفية حفظ ملفات CAD كـ JPEG في Java باستخدام Aspose.CAD، وإضافة
  طبقات متعددة، وضبط أبعاد CAD لتحويل الصورة بدقة.
linktitle: Support of Layers in CAD
second_title: Aspose.CAD Java API
title: حفظ CAD كـ JPEG مع دعم الطبقات في Java
url: /ar/java/advanced-cad-features/support-of-layers-in-cad/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# حفظ CAD كـ JPEG مع دعم الطبقات في Java

## Introduction

في هذا الدرس ستكتشف كيفية **حفظ CAD كـ JPEG** مع الاستفادة الكاملة من دعم الطبقات في Aspose.CAD for Java. تسمح لك الطبقات بعزل أجزاء محددة من الرسم، مما يجعل من السهل تصدير ما تحتاجه فقط. سنستعرض كل خطوة، من إعداد البيئة إلى تصدير JPEG يتضمن فقط الطبقات التي تختارها.

## Quick Answers
- **ماذا يعني “حفظ CAD كـ JPEG”؟** يحول رسم CAD إلى صورة JPEG نقطية.
- **هل يمكنني تضمين طبقات مختارة فقط؟** نعم – استخدم طريقة `setLayers` لتحديد الطبقات التي تريد عرضها.
- **كيف يمكنني تغيير حجم الصورة؟** عدل `setPageWidth` و `setPageHeight` في `CadRasterizationOptions`.
- **هل هذا حل مخصص لـ Java فقط؟** المثال يستخدم Aspose.CAD for Java، لكن المفاهيم نفسها تنطبق على لغات أخرى.
- **هل أحتاج إلى ترخيص؟** النسخة التجريبية المجانية تعمل للاختبار؛ يلزم ترخيص تجاري للإنتاج.

## Prerequisites

قبل البدء، تأكد من توفر ما يلي:

1. **مكتبة Aspose.CAD for Java** – قم بتنزيلها من الـ[موقع](https://releases.aspose.com/cad/java/). اتبع دليل التثبيت لإضافة ملفات JAR إلى مسار الفئة (classpath) في مشروعك.  
2. **بيئة تطوير Java** – JDK حديث (الإصدار 8 أو أحدث) مثبت على جهازك.

الآن بعد أن تم إعداد كل شيء، دعنا نستكشف الكود اللازم **لحفظ CAD كـ JPEG** مع عرض الطبقات المختارة.

## Import Namespaces

ابدأ باستيراد الفئات المطلوبة من Aspose.CAD وأدوات Java القياسية:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
import java.util.ArrayList;
import java.util.Arrays;
import java.util.List;
```

## Step‑by‑Step Guide

### Step 1: Set Up File Paths

حدد موقع ملف DWF المصدر ومكان كتابة ملف JPEG الناتج.

```java
String dataDir = "Your Document Directory" + "DWFDrawings/";
String srcFile = dataDir + "for_layers_test.dwf";
String outFile = dataDir + "for_layers_test.jpg";
```

### Step 2: Load the DWF Image

استخدم طريقة `Image.load` من Aspose.CAD لقراءة رسم CAD.

```java
Image image = Image.load(srcFile);
```

### Step 3: Configure Rasterization Options (Adjust CAD Dimensions)

أنشئ كائن `CadRasterizationOptions` وحدد حجم الإخراج المطلوب. تغيير هذه القيم يتيح لك **ضبط أبعاد CAD** للصورة النهائية.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
```

### Step 4: Specify Layers (Add Multiple Layers)

إذا كنت تريد عرض أكثر من طبقة، ببساطة أضف أسمائها إلى القائمة. هنا نبدأ بطبقة واحدة تسمى “LayerA”.

```java
List<String> stringList = new ArrayList<>(Arrays.asList("LayerA"));
rasterizationOptions.setLayers(stringList);
```

*نصيحة احترافية:* لإ **إضافة طبقات متعددة**، وسّع استدعاء `Arrays.asList`، مثال: `Arrays.asList("LayerA", "LayerB", "LayerC")`.

### Step 5: Configure JPEG Options (Java Convert CAD Image)

اربط إعدادات التحويل إلى تنسيق JPEG.

```java
JpegOptions jpegOptions = new JpegOptions();
jpegOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### Step 6: Export to JPG (Save CAD as JPEG)

أخيرًا، اكتب الصورة إلى القرص. هذه الخطوة **تحفظ رسم CAD كملف JPEG** يحتوي فقط على الطبقات المختارة.

```java
image.save(outFile, jpegOptions);
```

باتباع هذه الخطوات، تكون قد نجحت في **حفظ CAD كـ JPEG** مع التحكم في الطبقات الظاهرة وتخصيص أبعاد الصورة.

## Common Issues and Solutions

| المشكلة | الحل |
|-------|----------|
| **الطبقات لا تظهر** | تأكد من أن أسماء الطبقات مطابقة تمامًا لما هو مخزن في ملف DWF (حساسة لحالة الأحرف). |
| **الصورة الناتجة فارغة** | تأكد من أن `setPageWidth` و `setPageHeight` كافيان لتغطية أبعاد الرسم. |
| **استثناء الترخيص** | استخدم ترخيص تجريبي للاختبار؛ احصل على ترخيص كامل لبيئات الإنتاج. |

## Frequently Asked Questions

**س: هل يمكنني إضافة طبقات متعددة إلى خيارات التحويل؟**  
ج: بالتأكيد. قم بتمديد `stringList` بأسماء طبقات إضافية، مثال: `Arrays.asList("LayerA", "LayerB")`.

**س: هل Aspose.CAD متوافق مع صيغ CAD أخرى؟**  
ج: نعم، يدعم DWG، DXF، DWF، والعديد من الصيغ الأخرى.

**س: كيف يمكنني تغيير أبعاد الصورة الناتجة؟**  
ج: عدل `setPageWidth` و `setPageHeight` في كائن `CadRasterizationOptions`.

**س: أين يمكنني شراء ترخيص لـ Aspose.CAD؟**  
ج: يمكنك استكشاف خيارات الترخيص [هنا](https://purchase.aspose.com/buy).

**س: أين يمكنني الحصول على دعم المجتمع؟**  
ج: انضم إلى مجتمع Aspose.CAD على الـ[منتدى](https://forum.aspose.com/c/cad/19) للحصول على المساعدة والنقاشات.

---

**آخر تحديث:** 2025-12-13  
**تم الاختبار باستخدام:** Aspose.CAD for Java 24.11  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}