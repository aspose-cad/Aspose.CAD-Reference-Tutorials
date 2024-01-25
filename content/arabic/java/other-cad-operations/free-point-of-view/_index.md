---
title: عرض وجهة نظر مجاني باستخدام Aspose.CAD لـ Java
linktitle: وجهة نظر مجانية
second_title: Aspose.CAD جافا API
description: اكتشف قوة Aspose.CAD لـ Java في هذا البرنامج التعليمي حول تحقيق عرض وجهة نظر مجاني لرسومات CAD. أطلق العنان لإمكانيات Aspose.CAD.
type: docs
weight: 14
url: /ar/java/other-cad-operations/free-point-of-view/
---
## مقدمة

مرحبًا بك في "وجهة النظر المجانية - البرنامج التعليمي Aspose.CAD لـ Java." في هذا الدليل الشامل، سنرشدك خلال عملية الاستفادة من Aspose.CAD لـ Java لتحقيق عرض وجهة نظر مجاني لرسومات CAD. Aspose.CAD هي مكتبة Java قوية توفر مجموعة واسعة من الميزات للعمل مع ملفات التصميم بمساعدة الكمبيوتر (CAD). سيغطي البرنامج التعليمي المتطلبات الأساسية الضرورية، واستيراد الحزم الأساسية، وتقسيم كل مثال إلى أدلة خطوة بخطوة.

## المتطلبات الأساسية

قبل الغوص في البرنامج التعليمي، تأكد من توفر المتطلبات الأساسية التالية:
-  Aspose.CAD لمكتبة Java: قم بتنزيل وتثبيت مكتبة Aspose.CAD لـ Java من[رابط التحميل](https://releases.aspose.com/cad/java/).
- Java Development Kit (JDK): تأكد من تثبيت Java على جهازك.

## حزم الاستيراد

للبدء، قم باستيراد الحزم المطلوبة إلى مشروع Java الخاص بك. أضف أسطر التعليمات البرمجية التالية في بداية ملف Java الخاص بك:
```java
import com.aspose.cad.fileformats.ObserverPoint;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.Image;
import com.aspose.cad.imageoptions.JpegOptions;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.ObserverPoint;
```

تعتبر هذه الحزم ضرورية للعمل مع ملفات CAD وتخصيص خيارات العرض.

الآن، دعونا نقسم المثال المقدم إلى خطوات متعددة:

## الخطوة 1: قم بإعداد دليل المستندات الخاص بك

```java
String dataDir = "Your Document Directory" + "CADConversion/";
```

استبدل "دليل المستندات الخاص بك" بالمسار إلى دليل المستندات الفعلي.

## الخطوة 2: قم بتحميل رسم CAD

```java
String sourceFilePath = dataDir + "conic_pyramid.dxf";
Image objImage = Image.load(sourceFilePath);
```

حدد المسار إلى رسم CAD الخاص بك، وقم بتحميله باستخدام الملف`Image` فصل.

## الخطوة 3: تكوين خيارات تنقيط CAD

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
cadRasterizationOptions.setPageHeight(1500);
cadRasterizationOptions.setPageWidth(1500);
```

قم بتخصيص خيارات تنقيط CAD وفقًا لمتطلباتك، مثل ارتفاع الصفحة وعرضها.

## الخطوة 4: إعداد خيارات Jpeg

```java
JpegOptions options = new JpegOptions();
options.setVectorRasterizationOptions(cadRasterizationOptions);
```

 إنشاء مثيل ل`JpegOptions` وربطها بخيارات التنقيط التي تم تكوينها مسبقًا.

## الخطوة 5: تحديد زوايا الدوران

```java
float xAngle = 10;
float yAngle = 30;
float zAngle = 40;
ObserverPoint obvPoint = new ObserverPoint(xAngle, yAngle, zAngle);
cadRasterizationOptions.setObserverPoint(obvPoint);
```

حدد زوايا الدوران على طول المحاور X وY وZ لعرض نقطة الرؤية الحرة.

## الخطوة 6: احفظ الصورة المقدمة

```java
objImage.save(dataDir + "FreePointOfView_out.jpeg", options);
```

احفظ الصورة المقدمة بالخيارات المحددة في الموقع المطلوب.

كرر هذه الخطوات لحالة الاستخدام المحددة الخاصة بك، مما يضمن عرض وجهة نظر مجانية لرسومات CAD الخاصة بك.

## خاتمة

تهانينا! لقد تعلمت بنجاح كيفية تنفيذ عرض وجهة نظر مجانية باستخدام Aspose.CAD لـ Java. غطى هذا البرنامج التعليمي الخطوات الأساسية، بدءًا من إعداد المتطلبات الأساسية وحتى تخصيص خيارات العرض وحفظ الصورة الناتجة.

## الأسئلة الشائعة

### س1: هل يمكنني استخدام Aspose.CAD لـ Java على أنظمة أساسية متعددة؟

A1: نعم، Aspose.CAD for Java مستقل عن النظام الأساسي ويمكن استخدامه على أنظمة تشغيل مختلفة.

### س2: هل توجد أي خيارات ترخيص لـ Aspose.CAD لـ Java؟

 ج٢: نعم، يمكنك استكشاف خيارات الترخيص وإجراء عملية شراء[هنا](https://purchase.aspose.com/buy).

### س3: هل هناك نسخة تجريبية مجانية متاحة؟

 ج3: نعم، يمكنك الوصول إلى نسخة تجريبية مجانية[هنا](https://releases.aspose.com/).

### س 4: أين يمكنني العثور على دعم لـ Aspose.CAD لـ Java؟

 ج4: قم بزيارة[منتدى Aspose.CAD](https://forum.aspose.com/c/cad/19) لدعم المجتمع والمناقشات.

### س5: كيف يمكنني الحصول على ترخيص مؤقت؟

 ج5: الحصول على ترخيص مؤقت[هنا](https://purchase.aspose.com/temporary-license/).