---
date: 2026-02-28
description: تعلم كيفية إنشاء PDF من DWG، حفظ DWG كملف PDF، وإضافة نص إلى رسومات DWG
  باستخدام Aspose.CAD for Java—دليل خطوة بخطوة.
linktitle: Add Text in DWG
second_title: Aspose.CAD Java API
title: إنشاء PDF من DWG وإضافة نص باستخدام Aspose.CAD لجافا
url: /ar/java/cad-text-and-annotation/add-text-in-dwg/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# إنشاء PDF من DWG وإضافة نص باستخدام Aspose.CAD للغة Java

## المقدمة

إذا كنت بحاجة إلى **إنشاء PDF من DWG** مع إدراج نص مخصص، فأنت في المكان الصحيح. في هذا البرنامج التعليمي سنستعرض العملية بالكامل — تحميل رسم DWG، إضافة توضيح نصي، وأخيرًا حفظ النتيجة كملف PDF باستخدام Aspose.CAD للغة Java. في النهاية ستفهم كيفية **حفظ DWG كـ PDF**، تخصيص ارتفاع النص، وحتى إضافة توضيحات أساسية.

## إجابات سريعة
- **هل يمكنني تحويل DWG إلى PDF في Java؟** نعم، Aspose.CAD للغة Java يوفر واجهة برمجة تطبيقات بسيطة.  
- **هل أحتاج إلى ترخيص للاستخدام الإنتاجي؟** يلزم ترخيص تجاري؛ يتوفر نسخة تجريبية مجانية.  
- **ما الطريقة التي تضيف نصًا إلى DWG؟** استخدم كائن `CadText` وأضفه إلى مساحة النموذج.  
- **هل يمكنني تعيين ارتفاع النص؟** بالتأكيد — استخدم `setTextHeight()` على مثيل `CadText`.  
- **هل الناتج قائم على المتجهات؟** عندما تُضبط خيارات التحويل إلى نقطية على `UseObjectColor`، يحتفظ PDF ببيانات المتجهات عالية الجودة.

## ما هو “إنشاء PDF من DWG”؟
إنشاء PDF من رسم DWG يعني تحويل تنسيق CAD الأصلي إلى مستند مقروء‑فقط مدعوم على نطاق واسع مع الحفاظ على الهندسة الأصلية. هذه العملية ضرورية عندما تحتاج إلى مشاركة التصاميم مع أصحاب المصلحة الذين لا يمتلكون برنامج CAD.

## لماذا تستخدم Aspose.CAD للغة Java لتحويل DWG إلى PDF؟
توفر Aspose.CAD حلاً بحتًا للغة Java لا يتطلب تثبيت CAD خارجي. تدعم **تحويل DWG إلى PDF**، وتحافظ على دقة المتجهات، وتتيح لك إضافة توضيحات برمجية مثل النصوص، الأبعاد، أو الرسومات المخصصة قبل التحويل.

## المتطلبات المسبقة

قبل الغوص في البرنامج التعليمي، تأكد من توفر المتطلبات المسبقة التالية:

- مكتبة Aspose.CAD للغة Java: قم بتنزيل وتثبيت المكتبة من صفحة [Aspose.CAD للغة Java](https://releases.aspose.com/cad/java/).
- مجموعة تطوير جافا (JDK): تأكد من تثبيت أحدث نسخة من JDK على نظامك.
- رسم DWG: حضّر ملف رسم DWG الذي تريد إضافة النص إليه.

## استيراد مساحات الأسماء

في شفرة Java الخاصة بك، استورد مساحات الأسماء الضرورية لـ Aspose.CAD:

```java
import com.aspose.cad.Image;


import com.aspose.cad.fileformats.cad.CadDrawTypeMode;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.CadText;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

الآن، دعنا نقسم مقتطف الشفرة المقدم إلى خطوات متعددة:

## Step 1: إعداد دليل المستند ومسار ملف DWG

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String dwgPathToFile = dataDir + "SimpleEntites.dwg";
```

## Step 2: تحميل صورة DWG

```java
Image image = Image.load(dwgPathToFile);
```

## Step 3: إنشاء كائن CadText (إضافة نص إلى DWG)

```java
CadText cadText = new CadText();
cadText.setStyleType("Standard");
cadText.setDefaultValue("Some custom text");
cadText.setColorId(256);
cadText.setLayerName("0");
cadText.getFirstAlignment().setX(47.9);
cadText.getFirstAlignment().setY(5.56);
cadText.setTextHeight(0.8);          // set text height in DWG units
cadText.setScaleX(0);
```

## Step 4: إضافة نص إلى CadImage (إدراج توضيح)

```java
CadImage cadImage = ((CadImage)(image));
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(cadText);
```

## Step 5: إعداد خيارات PDF (التحضير لإنشاء PDF من DWG)

```java
PdfOptions pdfOptions = new PdfOptions();
```

## Step 6: تكوين CadRasterizationOptions (التحكم في عرض PDF)

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setDrawType(CadDrawTypeMode.UseObjectColor);
cadRasterizationOptions.setPageHeight(1600);
cadRasterizationOptions.setPageWidth(1600);
cadRasterizationOptions.setLayouts(new String[] {"Model"});
```

## Step 7: حفظ DWG المعدل كملف PDF (dwg إلى pdf java)

```java
image.save(dataDir + "SimpleEntites_generated.dwg.pdf", pdfOptions);
```

باتباع هذه الخطوات، ستتمكن من **إنشاء PDF من DWG**، إضافة نص مخصص، والتحكم في ارتفاع النص — كل ذلك ببضع أسطر فقط من شفرة Java.

## كيف يمكن تحويل DWG إلى PDF في Java على نطاق واسع؟
إذا كنت بحاجة إلى **تحويل دفعة من ملفات DWG إلى PDF**، ضع الشفرة أعلاه داخل حلقة تتنقل عبر مجلد يحتوي على رسومات DWG. قم بضبط `pageHeight`/`pageWidth` فقط عند الضرورة للحفاظ على استهلاك الذاكرة منخفضًا، وأعد استخدام نفس مثيل `PdfOptions` لكل ملف لتحسين الأداء.

## مشكلات شائعة ونصائح

- **النص لا يظهر؟** تحقق من أن إحداثيات X/Y ضمن حدود الرسم وأن الطبقة مرئية.
- **ارتفاع النص غير صحيح؟** اضبط `setTextHeight()`؛ القيمة بوحدة نظام الرسم.
- **الـ PDF يبدو مُرصًّا؟** تأكد من ضبط `CadDrawTypeMode.UseObjectColor` للحفاظ على معلومات المتجهات.
- **الأداء مع الملفات الكبيرة؟** زد `pageHeight`/`pageWidth` فقط حسب الحاجة؛ القيم الأكبر تستهلك المزيد من الذاكرة.

## الأسئلة المتكررة

**س: هل Aspose.CAD متوافق مع جميع إصدارات ملفات DWG؟**  
ج: يدعم Aspose.CAD إصدارات متعددة من ملفات DWG، مما يضمن التوافق مع مجموعة واسعة من برامج CAD.

**س: هل يمكنني تخصيص الخط وتنسيق النص المضاف؟**  
ج: نعم، يمكنك تخصيص الخط، النمط، وغيرها من خيارات التنسيق للنص المضاف إلى ملفات DWG باستخدام Aspose.CAD.

**س: هل هناك نسخة تجريبية مجانية متاحة لـ Aspose.CAD للغة Java؟**  
ج: نعم، يمكنك استكشاف ميزات Aspose.CAD بالحصول على نسخة تجريبية مجانية من [هنا](https://releases.aspose.com/).

**س: أين يمكنني العثور على وثائق مفصلة لـ Aspose.CAD للغة Java؟**  
ج: راجع الوثائق [هنا](https://reference.aspose.com/cad/java/) للحصول على معلومات وأمثلة متعمقة.

**س: كيف يمكنني الحصول على الدعم أو طلب المساعدة بخصوص Aspose.CAD؟**  
ج: زر منتدى [Aspose.CAD](https://forum.aspose.com/c/cad/19) للحصول على المساعدة والتواصل مع المجتمع.

---

**آخر تحديث:** 2026-02-28  
**تم الاختبار مع:** Aspose.CAD للغة Java 24.12  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}