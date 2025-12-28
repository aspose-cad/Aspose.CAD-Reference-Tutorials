---
date: 2025-12-28
description: تعلم كيفية إنشاء PDF من DWG، حفظ DWG كملف PDF، وإضافة نص إلى رسومات DWG
  باستخدام Aspose.CAD للغة Java—دليل خطوة بخطوة.
linktitle: Add Text in DWG
second_title: Aspose.CAD Java API
title: إنشاء PDF من DWG وإضافة نص باستخدام Aspose.CAD للـ Java
url: /ar/java/cad-text-and-annotation/add-text-in-dwg/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# إنشاء PDF من DWG وإضافة نص باستخدام Aspose.CAD للـ Java

## المقدمة

إذا كنت بحاجة إلى **إنشاء PDF من ملفات DWG** مع إدراج نص مخصص، فأنت في المكان الصحيح. في هذا الدرس سنستعرض العملية بالكامل—تحميل رسم DWG، إضافة توضيح نصي، وأخيرًا حفظ النتيجة كملف PDF باستخدام Aspose.CAD للـ Java. في النهاية ستفهم كيف **تحفظ DWG كـ PDF**، تخصيص ارتفاع النص، وحتى إضافة توضيحات أساسية.

## إجابات سريعة
- **هل يمكنني تحويل DWG إلى PDF في Java؟** نعم، Aspose.CAD للـ Java يوفر واجهة برمجة تطبيقات بسيطة.  
- **هل أحتاج إلى ترخيص للاستخدام الإنتاجي؟** يلزم الحصول على ترخيص تجاري؛ يتوفر نسخة تجريبية مجانية.  
- **ما الطريقة التي تضيف نصًا إلى DWG؟** استخدم كائن `CadText` وأضفه إلى مساحة النموذج.  
- **هل يمكنني ضبط ارتفاع النص؟** بالتأكيد—استخدم `setTextHeight()` على نسخة `CadText`.  
- **هل الإخراج قائم على المتجهات؟** عندما تُضبط خيارات الرستر إلى `UseObjectColor`، يحتفظ PDF ببيانات المتجهات عالية الجودة.

## المتطلبات المسبقة

قبل الغوص في الدرس، تأكد من توفر المتطلبات التالية:

- مكتبة Aspose.CAD للـ Java: قم بتحميل وتثبيت المكتبة من [صفحة Aspose.CAD للـ Java](https://releases.aspose.com/cad/java/).

- مجموعة تطوير جافا (JDK): تأكد من تثبيت أحدث نسخة من JDK على نظامك.

- رسم DWG: حضّر ملف رسم DWG ترغب في إضافة النص إليه.

## استيراد المساحات الاسمية

في كود Java الخاص بك، استورد المساحات الاسمية اللازمة لـ Aspose.CAD:

```java
import com.aspose.cad.Image;


import com.aspose.cad.fileformats.cad.CadDrawTypeMode;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.CadText;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

الآن، لنقسم المقتطف البرمجي المقدم إلى عدة خطوات:

## الخطوة 1: إعداد دليل المستند ومسار ملف DWG

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String dwgPathToFile = dataDir + "SimpleEntites.dwg";
```

## الخطوة 2: تحميل صورة DWG

```java
Image image = Image.load(dwgPathToFile);
```

## الخطوة 3: إنشاء كائن CadText (إضافة نص إلى DWG)

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

## الخطوة 4: إضافة نص إلى CadImage (إدراج توضيح)

```java
CadImage cadImage = ((CadImage)(image));
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(cadText);
```

## الخطوة 5: إعداد خيارات PDF (التحضير لإنشاء PDF من DWG)

```java
PdfOptions pdfOptions = new PdfOptions();
```

## الخطوة 6: تكوين CadRasterizationOptions (التحكم في عرض PDF)

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setDrawType(CadDrawTypeMode.UseObjectColor);
cadRasterizationOptions.setPageHeight(1600);
cadRasterizationOptions.setPageWidth(1600);
cadRasterizationOptions.setLayouts(new String[] {"Model"});
```

## الخطوة 7: حفظ DWG المعدل كـ PDF (dwg إلى pdf java)

```java
image.save(dataDir + "SimpleEntites_generated.dwg.pdf", pdfOptions);
```

باتباع هذه الخطوات، ستتمكن من **إنشاء PDF من DWG**، إضافة نص مخصص، والتحكم في ارتفاع النص—كل ذلك ببضع أسطر من كود Java.

## لماذا إضافة نص إلى DWG وتحويله إلى PDF؟

إضافة نص مباشرة إلى ملف DWG مفيدة لـ:

- **وضع علامات على التصاميم** مع ملاحظات أو أرقام أجزاء.  
- **إنشاء وثائق قابلة للطباعة** حيث يكون PDF صيغة للقراءة فقط ومدعومة على نطاق واسع.  
- **أتمتة المعالجة الدفعية** لمكتبات CAD الكبيرة دون تعديل يدوي.

## المشكلات الشائعة والنصائح

- **النص لا يظهر؟** تحقق من أن إحداثيات X/Y داخل حدود الرسم وأن الطبقة مرئية.  
- **ارتفاع النص غير صحيح؟** عدل `setTextHeight()`؛ القيمة بوحدة نظام الرسم.  
- **PDF يبدو مُرصًّا؟** تأكد من ضبط `CadDrawTypeMode.UseObjectColor` للحفاظ على المعلومات المتجهية.  
- **الأداء مع الملفات الكبيرة؟** زد `pageHeight`/`pageWidth` فقط حسب الحاجة؛ القيم الأكبر تستهلك المزيد من الذاكرة.

## الأسئلة المتكررة

**س: هل Aspose.CAD متوافق مع جميع إصدارات ملفات DWG؟**  
ج: يدعم Aspose.CAD إصدارات متعددة من ملفات DWG، مما يضمن التوافق مع مجموعة واسعة من برامج CAD.

**س: هل يمكنني تخصيص الخط وتنسيق النص المضاف؟**  
ج: نعم، يمكنك تخصيص الخط، النمط، وخيارات التنسيق الأخرى للنص المضاف إلى ملفات DWG باستخدام Aspose.CAD.

**س: هل تتوفر نسخة تجريبية مجانية لـ Aspose.CAD للـ Java؟**  
ج: نعم، يمكنك استكشاف ميزات Aspose.CAD بالحصول على نسخة تجريبية مجانية من [هنا](https://releases.aspose.com/).

**س: أين يمكنني العثور على وثائق مفصلة لـ Aspose.CAD للـ Java؟**  
ج: راجع الوثائق [هنا](https://reference.aspose.com/cad/java/) للحصول على معلومات متعمقة وأمثلة.

**س: كيف يمكنني الحصول على الدعم أو المساعدة بخصوص Aspose.CAD؟**  
ج: زر منتدى [Aspose.CAD](https://forum.aspose.com/c/cad/19) للحصول على المساعدة والتواصل مع المجتمع.

---

**آخر تحديث:** 2025-12-28  
**تم الاختبار مع:** Aspose.CAD للـ Java 24.12  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}