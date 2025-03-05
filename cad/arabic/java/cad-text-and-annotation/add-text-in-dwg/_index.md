---
title: إضافة نص في DWG باستخدام Aspose.CAD لـ Java
linktitle: إضافة نص في DWG
second_title: Aspose.CAD جافا API
description: قم بتحسين رسومات DWG الخاصة بك بسهولة باستخدام Aspose.CAD لـ Java. أضف نصًا بسلاسة باستخدام دليلنا المفصّل خطوة بخطوة.
type: docs
weight: 10
url: /ar/java/cad-text-and-annotation/add-text-in-dwg/
---
## مقدمة

في عالم التصميم بمساعدة الكمبيوتر (CAD)، يبرز Aspose.CAD for Java كأداة قوية لمعالجة وتحويل رسومات DWG. إحدى ميزاته المفيدة هي القدرة على إضافة نص إلى ملفات DWG بسلاسة. في هذا البرنامج التعليمي، سنرشدك خلال عملية إضافة نص إلى رسومات DWG باستخدام Aspose.CAD لـ Java.

## المتطلبات الأساسية

قبل الغوص في البرنامج التعليمي، تأكد من توفر المتطلبات الأساسية التالية:

-  Aspose.CAD لمكتبة Java: قم بتنزيل المكتبة وتثبيتها من ملف[Aspose.CAD لصفحة جافا](https://releases.aspose.com/cad/java/).

- Java Development Kit (JDK): تأكد من تثبيت أحدث إصدار من JDK على نظامك.

- رسم DWG: قم بإعداد ملف رسم DWG حيث تريد إضافة نص.

## استيراد مساحات الأسماء

في كود Java الخاص بك، قم باستيراد مساحات الأسماء الضرورية لـ Aspose.CAD:

```java
import com.aspose.cad.Image;


import com.aspose.cad.fileformats.cad.CadDrawTypeMode;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.CadText;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

الآن، دعونا نقسم مقتطف الشفرة المقدم إلى خطوات متعددة:

## الخطوة 1: إعداد دليل المستندات ومسار ملف DWG

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String dwgPathToFile = dataDir + "SimpleEntites.dwg";
```

## الخطوة 2: تحميل صورة DWG

```java
Image image = Image.load(dwgPathToFile);
```

## الخطوة 3: إنشاء كائن CadText

```java
CadText cadText = new CadText();
cadText.setStyleType("Standard");
cadText.setDefaultValue("Some custom text");
cadText.setColorId(256);
cadText.setLayerName("0");
cadText.getFirstAlignment().setX(47.9);
cadText.getFirstAlignment().setY(5.56);
cadText.setTextHeight(0.8);
cadText.setScaleX(0);
```

## الخطوة 4: إضافة نص إلى CadImage

```java
CadImage cadImage = ((CadImage)(image));
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(cadText);
```

## الخطوة 5: إعداد خيارات PDF

```java
PdfOptions pdfOptions = new PdfOptions();
```

## الخطوة 6: تكوين CadRasterizationOptions

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setDrawType(CadDrawTypeMode.UseObjectColor);
cadRasterizationOptions.setPageHeight(1600);
cadRasterizationOptions.setPageWidth(1600);
cadRasterizationOptions.setLayouts(new String[] {"Model"});
```

## الخطوة 7: احفظ ملف DWG المعدل بصيغة PDF

```java
image.save(dataDir + "SimpleEntites_generated.dwg.pdf", pdfOptions);
```

باتباع هذه الخطوات، ستتمكن من إضافة نص بسلاسة إلى رسومات DWG الخاصة بك باستخدام Aspose.CAD لـ Java.

## خاتمة

يعمل Aspose.CAD for Java على تمكين المطورين من تحسين رسومات DWG وتعديلها برمجيًا. قدم هذا البرنامج التعليمي دليلاً واضحًا خطوة بخطوة لإضافة نص إلى ملفات DWG الخاصة بك، مع عرض بساطة Aspose.CAD وقوته.

## الأسئلة الشائعة

### س 1: هل Aspose.CAD متوافق مع كافة إصدارات ملفات DWG؟

ج1: يدعم Aspose.CAD إصدارات مختلفة من ملفات DWG، مما يضمن التوافق مع مجموعة واسعة من برامج CAD.

### س2: هل يمكنني تخصيص الخط وتنسيق النص المضاف؟

ج2: نعم، يمكنك تخصيص الخط والنمط وخيارات التنسيق الأخرى للنص المضاف إلى ملفات DWG باستخدام Aspose.CAD.

### س3: هل تتوفر نسخة تجريبية مجانية من Aspose.CAD لـ Java؟

 ج3: نعم، يمكنك استكشاف ميزات Aspose.CAD من خلال الحصول على نسخة تجريبية مجانية منه[هنا](https://releases.aspose.com/).

### س4: أين يمكنني العثور على الوثائق التفصيلية الخاصة بـ Aspose.CAD لـ Java؟

 ج4: راجع الوثائق[هنا](https://reference.aspose.com/cad/java/) للحصول على معلومات وأمثلة متعمقة.

### س5: كيف يمكنني الحصول على الدعم أو طلب المساعدة فيما يتعلق بـ Aspose.CAD؟

ج5: قم بزيارة[منتدى Aspose.CAD](https://forum.aspose.com/c/cad/19) للحصول على المساعدة والتواصل مع المجتمع.