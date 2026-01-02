---
date: 2026-01-02
description: تعلم كيفية تصدير DWG كملف PDF، وتمكين الخطوط المخفية، وتحويل DWG إلى
  PDF باستخدام Aspose.CAD للغة Java في هذا الدرس خطوة بخطوة.
linktitle: Export DWG as PDF with Hidden Lines Using Java
second_title: Aspose.CAD Java API
title: تصدير DWG كملف PDF مع الخطوط المخفية – Aspose.CAD للـ Java
url: /ar/java/cad-text-and-formatting/support-hidden-lines-in-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تصدير DWG كملف PDF مع الخطوط المخفية – Aspose.CAD for Java

## مقدمة

في هذا البرنامج التعليمي ستتعلم كيفية **تصدير DWG كملف PDF** مع الحفاظ على الخطوط المخفية باستخدام Aspose.CAD for Java. سواء كنت تحتاج إلى **تحويل DWG إلى PDF**، أو إنشاء دليل على نمط **dwg to pdf tutorial**، أو ببساطة **حفظ DWG كملف PDF** مع دعم الخطوط المخفية، سنرشدك خلال كل خطوة. في النهاية، ستحصل على حل جاهز للاستخدام يمكنك إدراجه في أي مشروع Java.

## إجابات سريعة
- **ماذا يغطي هذا البرنامج التعليمي؟** تمكين عرض الخطوط المخفية أثناء تصدير DWG إلى PDF باستخدام Aspose.CAD for Java.  
- **ما العملية الأساسية التي يتم تنفيذها؟** `export dwg as pdf`.  
- **هل أحتاج إلى ترخيص؟** النسخة التجريبية المجانية تكفي للاختبار؛ يلزم الحصول على ترخيص تجاري للإنتاج.  
- **ما المتطلبات المسبقة؟** بيئة تطوير Java، مكتبة Aspose.CAD for Java، وملفات DWG.  
- **كم يستغرق التنفيذ؟** حوالي 10‑15 دقيقة لإعداد أساسي.

## ما هو “export dwg as pdf”؟
تصدير ملف DWG إلى PDF يحول الرسم الهندسي القائم على المتجهات إلى تنسيق مستند محمول مع الحفاظ على الطبقات وأنواع الخطوط وعرض الخطوط المخفية الاختياري. هذا يجعل من السهل مشاركة تصاميم CAD مع أصحاب المصلحة الذين قد لا يمتلكون برنامج CAD.

## لماذا تمكين الخطوط المخفية عند التصدير؟
توفر الخطوط المخفية تمثيلاً بصريًا أوضح للنماذج ثلاثية الأبعاد المعقدة على صفحة ثنائية الأبعاد، مع التأكيد على الحواف الظاهرة فقط. هذا يحسن قابلية القراءة وغالبًا ما يكون مطلوبًا في وثائق الهندسة.

## المتطلبات المسبقة

1. **Aspose.CAD for Java** – قم بتحميل المكتبة من الموقع الرسمي [هنا](https://releases.aspose.com/cad/java/).  
2. **ملفات DWG** – احفظ رسومات DWG المصدرية في دليل معروف.  
3. **بيئة تطوير Java** – JDK 8+ وIDE المفضل لديك (Eclipse، IntelliJ، إلخ).  

الآن بعد أن تم إعداد كل شيء، دعنا ننتقل إلى الكود.

## استيراد المساحات الاسمية

ابدأ باستيراد الفئات الضرورية حتى تتمكن من التعامل مع صور CAD وخيارات PDF.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import java.util.Arrays;
import java.util.List;
```

## الخطوة 1: إعداد المشروع

أنشئ مشروع Java وأضف ملف JAR الخاص بـ Aspose.CAD إلى مسار البناء. ثم عرّف الدليل الذي يحتوي على ملفات DWG الخاصة بك.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

> **نصيحة احترافية:** استخدم مسارًا مطلقًا أو قم بتكوين مسار نسبي بناءً على مجلد موارد المشروع.

## الخطوة 2: تحميل ملف DWG

حمّل ملف DWG المصدر إلى كائن `CadImage` حتى تتمكن من معالجته.

```java
String sourceFilePath = dataDir + "Bottom_plate.dwg";
String outPath = dataDir + "Bottom_plate.pdf";
CadImage cadImage = (CadImage)Image.load(sourceFilePath);
```

## الخطوة 3: تكوين خيارات التحويل إلى نقطية

اختر الطبقات التي تريد تضمينها وحدد حجم الصفحة ليتطابق مع الرسم الأصلي. هنا نقوم بتمكين عرض الخطوط المخفية عن طريق تحديد التخطيط.

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

> **مشكلة شائعة:** نسيان تعيين التخطيط إلى `"Model"` سيتسبب في ظهور جميع الخطوط (بما فيها المخفية) كخطوط صلبة في ملف PDF.

## الخاتمة

الآن لديك طريقة كاملة وجاهزة للإنتاج **لتصدير DWG كملف PDF** مع دعم الخطوط المخفية باستخدام Aspose.CAD for Java. يمكن دمج هذا النهج في أدوات المعالجة الدفعية، خدمات الويب، أو تطبيقات سطح المكتب لأتمتة تحويل CAD إلى PDF.

## الأسئلة المتكررة

### س1: هل يمكنني استخدام Aspose.CAD for Java مع صيغ CAD أخرى؟
ج1: نعم، يدعم Aspose.CAD صيغ CAD متعددة مثل DWG، DXF، DWF، وأكثر.

### س2: هل هناك نسخة تجريبية مجانية متاحة لـ Aspose.CAD for Java؟
ج2: نعم، يمكنك العثور على النسخة التجريبية [هنا](https://releases.aspose.com/).

### س3: كيف أحصل على الدعم لـ Aspose.CAD for Java؟
ج3: زر منتدى Aspose.CAD [هنا](https://forum.aspose.com/c/cad/19) للحصول على دعم المجتمع.

### س4: أين يمكنني العثور على الوثائق التفصيلية لـ Aspose.CAD for Java؟
ج4: راجع الوثائق [هنا](https://reference.aspose.com/cad/java/).

### س5: هل يمكنني شراء ترخيص مؤقت لـ Aspose.CAD for Java؟
ج5: نعم، يمكنك الحصول على ترخيص مؤقت [هنا](https://purchase.aspose.com/temporary-license/).

### س6: هل تعمل هذه الطريقة أيضًا على تحويل DWG إلى PDF في بيئة خادم بدون واجهة رسومية؟
ج6: بالتأكيد. بما أن الكود يستخدم فقط واجهة Aspose.CAD API، فإنه يعمل دون أي تبعيات واجهة مستخدم، مما يجعله مثاليًا لأتمتة الخادم.

---

**آخر تحديث:** 2026-01-02  
**تم الاختبار مع:** Aspose.CAD for Java 24.12  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}