---
date: 2026-03-05
description: تعلم كيفية تصدير ملفات DWG إلى PDF، وتمكين الخطوط المخفية، وتحويل DWG
  إلى PDF باستخدام Aspose.CAD للـ Java في هذا الدليل خطوة بخطوة.
linktitle: Export DWG as PDF Using Java
second_title: Aspose.CAD Java API
title: تصدير DWG إلى PDF مع الخطوط المخفية – Aspose.CAD للـ Java
url: /ar/java/cad-text-and-formatting/support-hidden-lines-in-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تصدير DWG إلى PDF مع الخطوط المخفية – Aspose.CAD للـ Java

## المقدمة

في هذا الدرس ستتعلم كيفية **export dwg to pdf** مع الحفاظ على الخطوط المخفية باستخدام Aspose.CAD للـ Java. سواء كنت بحاجة إلى **convert DWG to PDF**، أو إنشاء دليل على نمط **dwg to pdf tutorial**، أو ببساطة **save DWG as PDF** مع دعم الخطوط المخفية، سنرشدك خلال كل خطوة. في النهاية، ستحصل على حل جاهز للاستخدام يمكنك إدراجه في أي مشروع Java.

## إجابات سريعة
- **ماذا يغطي هذا الدرس؟** تمكين عرض الخطوط المخفية أثناء تصدير DWG إلى PDF باستخدام Aspose.CAD للـ Java.  
- **ما العملية الأساسية التي يتم تنفيذها؟** `export dwg to pdf`.  
- **هل أحتاج إلى ترخيص؟** الإصدار التجريبي المجاني يكفي للاختبار؛ يلزم ترخيص تجاري للإنتاج.  
- **ما المتطلبات المسبقة؟** بيئة تطوير Java، مكتبة Aspose.CAD للـ Java، وملفات DWG.  
- **كم من الوقت تستغرق عملية التنفيذ؟** حوالي 10‑15 دقيقة لإعداد أساسي.

## ما هو “export dwg to pdf”؟
تحويل ملف DWG إلى PDF يحول الرسم الهندسي القائم على المتجهات إلى تنسيق مستند محمول مع الحفاظ على الطبقات وأنواع الخطوط وعرض الخطوط المخفية الاختياري. هذا يجعل من السهل مشاركة تصاميم CAD مع أصحاب المصلحة الذين قد لا يمتلكون برنامج CAD.

## كيفية تمكين الخطوط المخفية عند تصدير DWG إلى PDF
يتم التحكم في الخطوط المخفية عبر إعداد التخطيط في خيارات التحويل إلى نقطية. باختيار تخطيط **Model**، يخبر Aspose.CAD المُحَوِّل بمعاملة الحواف المخفية كغير مرئية، مما يمنحك تمثيلًا نظيفًا ثنائي الأبعاد لنموذج ثلاثي الأبعاد.

## لماذا تمكين الخطوط المخفية عند التصدير؟
توفر الخطوط المخفية تمثيلًا بصريًا أوضح للنماذج ثلاثية الأبعاد المعقدة على صفحة ثنائية الأبعاد، مع التأكد من إبراز الحواف المرئية فقط. هذا يحسن قابلية القراءة وغالبًا ما يكون مطلوبًا في وثائق الهندسة.

## المتطلبات المسبقة

1. **Aspose.CAD للـ Java** – قم بتحميل المكتبة من الموقع الرسمي [هنا](https://releases.aspose.com/cad/java/).  
2. **ملفات DWG** – احفظ رسومات DWG المصدرية في دليل معروف.  
3. **بيئة تطوير Java** – JDK 8+ وIDE المفضل لديك (Eclipse، IntelliJ، إلخ).  

الآن بعد أن تم إعدادك، دعنا نغوص في الشيفرة.

## استيراد المساحات الاسمية

ابدأ باستيراد الفئات اللازمة حتى تتمكن من العمل مع صور CAD وخيارات PDF.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import java.util.Arrays;
import java.util.List;
```

## الخطوة 1: إعداد مشروعك

أنشئ مشروع Java وأضف ملف JAR الخاص بـ Aspose.CAD إلى مسار البناء. ثم عرّف الدليل الذي يحتوي على ملفات DWG الخاصة بك.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

> **نصيحة احترافية:** استخدم مسارًا مطلقًا أو قم بتكوين مسار نسبي بناءً على مجلد موارد مشروعك.

## الخطوة 2: تحميل ملف DWG

حمّل ملف DWG المصدر إلى كائن `CadImage` حتى تتمكن من معالجته.

```java
String sourceFilePath = dataDir + "Bottom_plate.dwg";
String outPath = dataDir + "Bottom_plate.pdf";
CadImage cadImage = (CadImage)Image.load(sourceFilePath);
```

## الخطوة 3: تكوين خيارات التحويل إلى نقطية

اختر الطبقات التي تريد تضمينها واضبط حجم الصفحة ليتطابق مع الرسم الأصلي. هنا نتمكن من تمكين عرض الخطوط المخفية عبر تحديد التخطيط.

```java
List<String> list = Arrays.asList("Print","L1_RegMark","L2_RegMark");
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageHeight(cadImage.getHeight());
rasterizationOptions.setPageWidth(cadImage.getWidth()) ;
rasterizationOptions.setLayers(list);
```

## الخطوة 4: تعيين خيارات PDF

أخبر Aspose.CAD بتحويل البيانات المتجهة إلى PDF، باستخدام تخطيط “Model” لإبقاء الخطوط المخفية مخفية.

```java
PdfOptions pdfOptions = new PdfOptions();
rasterizationOptions.setLayouts(new String[] { "Model" });
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## الخطوة 5: حفظ النتيجة

أخيرًا، صدّر DWG كملف PDF. سيتم احترام الخطوط المخفية وفقًا للتخطيط الذي حددته.

```java
cadImage.save(outPath, pdfOptions);
System.out.println("\nThe DWG file exported successfully to PDF.\nFile saved at " + dataDir);
```

> **مشكلة شائعة:** نسيان تعيين التخطيط إلى `"Model"` سيؤدي إلى ظهور جميع الخطوط (بما فيها المخفية) صلبة في ملف PDF.

## المشكلات الشائعة والحلول

| المشكلة | سبب حدوثها | كيفية الإصلاح |
|-------|------------|----------------|
| PDF يظهر جميع الخطوط صلبة | لم يتم تعيين التخطيط إلى **Model** | تأكد من استدعاء `rasterizationOptions.setLayouts(new String[] { "Model" });` قبل الحفظ. |
| الطبقات مفقودة في الناتج | أسماء الطبقات غير صحيحة | تحقق من أسماء الطبقات في ملف DWG وتطابقها تمامًا في `list`. |
| خطأ نفاد الذاكرة في الملفات الكبيرة | حجم التحويل إلى نقطية كبير | قلل أبعاد الصفحة أو عالج الرسم على دفعات إذا أمكن. |

## الأسئلة المتكررة

### س1: هل يمكنني استخدام Aspose.CAD للـ Java مع صيغ ملفات CAD أخرى؟
نعم، يدعم Aspose.CAD صيغ CAD متعددة مثل DWG وDXF وDWF وغيرها.

### س2: هل يتوفر إصدار تجريبي مجاني لـ Aspose.CAD للـ Java؟
نعم، يمكنك العثور على الإصدار التجريبي المجاني [هنا](https://releases.aspose.com/).

### س3: كيف يمكنني الحصول على الدعم لـ Aspose.CAD للـ Java؟
قم بزيارة منتدى Aspose.CAD [هنا](https://forum.aspose.com/c/cad/19) للحصول على دعم المجتمع.

### س4: أين يمكنني العثور على الوثائق التفصيلية لـ Aspose.CAD للـ Java؟
راجع الوثائق [هنا](https://reference.aspose.com/cad/java/).

### س5: هل يمكنني شراء ترخيص مؤقت لـ Aspose.CAD للـ Java؟
نعم، يمكنك الحصول على ترخيص مؤقت [هنا](https://purchase.aspose.com/temporary-license/).

### س6: هل يعمل هذا الأسلوب أيضًا على تحويل DWG إلى PDF في بيئة خادم بدون واجهة رسومية؟
بالطبع. بما أن الشيفرة تستخدم فقط API الخاص بـ Aspose.CAD، فهي تعمل دون أي تبعيات واجهة مستخدم، مما يجعلها مثالية لأتمتة الخادم.

## الخلاصة

الآن لديك طريقة كاملة وجاهزة للإنتاج **export dwg to pdf** مع دعم الخطوط المخفية باستخدام Aspose.CAD للـ Java. يمكن دمج هذا النهج في أدوات المعالجة الدفعية، خدمات الويب، أو التطبيقات المكتبية لأتمتة تحويل CAD إلى PDF.

---

**آخر تحديث:** 2026-03-05  
**تم الاختبار مع:** Aspose.CAD للـ Java 24.12  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}