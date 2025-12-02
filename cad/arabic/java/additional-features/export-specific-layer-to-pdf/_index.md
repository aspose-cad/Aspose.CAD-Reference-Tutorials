---
date: 2025-11-30
description: تعرّف على كيفية إنشاء ملف PDF من ملفات DXF وتصدير طبقة محددة باستخدام
  Aspose.CAD للغة Java. يوضح لك هذا الدليل خطوة بخطوة كيفية تحويل DXF إلى PDF بسرعة
  وبشكل موثوق.
language: ar
linktitle: Export Specific Layer of DXF Drawing to PDF with Java
second_title: Aspose.CAD Java API
title: 'إنشاء PDF من DXF: تصدير الطبقة باستخدام Aspose.CAD للغة Java'
url: /java/additional-features/export-specific-layer-to-pdf/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# إنشاء PDF من DXF: تصدير الطبقة باستخدام Aspose.CAD للـ Java

## المقدمة

إذا كنت بحاجة إلى **إنشاء PDF من رسومات DXF** مع الاحتفاظ فقط بالطبقات التي تهمك، فإن Aspose.CAD للـ Java يجعل العملية سهلة. في هذا الدرس سنستعرض سيناريو واقعي: تصدير طبقة واحدة من ملف DXF إلى مستند PDF. ستتعرف على لماذا يعتبر هذا الأسلوب مفيدًا لإنشاء رسومات خفيفة الوزن، مشاركة تفاصيل التصميم مع مستخدمين غير متخصصين في CAD، أو بناء خطوط أنابيب تقارير مؤتمتة.

## إجابات سريعة
- **ما الذي يغطيه هذا الدرس؟** تصدير طبقة محددة من DXF إلى PDF باستخدام Aspose.CAD للـ Java.  
- **الفائدة الأساسية؟** تحتفظ فقط بالهندسة المطلوبة، مما يقلل حجم الملف والازدحام البصري.  
- **المتطلبات المسبقة؟** Java SDK، مكتبة Aspose.CAD للـ Java، وملف DXF للعمل معه.  
- **كم من الوقت تستغرق العملية؟** تقريبًا 10‑15 دقيقة لإعداد أساسي.  
- **هل يمكن تصدير طبقات متعددة؟** نعم – فقط عدّل قائمة الطبقات (انظر الخطوة 3).

## ما هو “إنشاء PDF من DXF”؟
تحويل ملف DXF (Drawing Exchange Format) إلى مستند PDF هو طلب شائع عندما يجب مشاركة بيانات CAD مع أصحاب المصلحة الذين لا يمتلكون برنامج CAD. يحافظ تنسيق PDF على الدقة البصرية مع إمكانية العرض على جميع الأنظمة.

## لماذا نستخدم Aspose.CAD للـ Java لتحويل DXF إلى PDF؟
- **بدون تبعيات خارجية** – جافا صافية، لا ملفات DLL أصلية.  
- **تحكم دقيق في الطبقات** – اختر بالضبط الطبقات التي تريد ظهورها في الناتج.  
- **تصيير عالي الجودة** – DPI قابل للتكوين، حجم الصفحة، وخيارات العرض.  
- **متعدد المنصات** – يعمل على Windows، Linux، و macOS.

## المتطلبات المسبقة

- **مكتبة Aspose.CAD للـ Java** – حمّلها من [توثيق Aspose.CAD Java](https://reference.aspose.com/cad/java/).  
- **بيئة تطوير جافا** – JDK 8 أو أعلى، وIDE أو أداة بناء من اختيارك.

## استيراد المساحات الاسمية

أولاً، استورد الفئات التي ستحتاجها. إبقاء الاستيرادات معًا يساعد على قراءة الكود ويسهل التحديثات المستقبلية.

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import java.util.ArrayList;
import java.util.Arrays;
import java.util.List;
```

## الخطوة 1: إعداد دليل الموارد

عرّف المجلد الذي يحتوي على ملفات DXF المصدرية. استبدل العنصر النائب بالمسار الفعلي على جهازك.

```java
String dataDir = "Your Document Directory" + "DXFDrawings/";
```

## الخطوة 2: تحميل رسم DXF

حمّل ملف DXF إلى كائن `Image`. يقوم Aspose.CAD تلقائيًا باكتشاف تنسيق الملف.

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

## الخطوة 3: تكوين خيارات التصيير (اختيار الطبقة)

هنا نخبر Aspose.CAD أي الطبقات يجب تصييرها. المثال يحتفظ فقط بالطبقة الافتراضية `"0"`. لتصدير طبقة مختلفة، استبدل `"0"` باسم الطبقة الدقيق في رسمك.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);

List<String> stringList = new ArrayList<>(Arrays.asList("0"));
rasterizationOptions.setLayers(stringList);
```

**نصيحة احترافية:** يمكنك إضافة أسماء طبقات متعددة إلى `stringList` (مثلًا `Arrays.asList("Layer1", "Layer2")`) لتصدير عدة طبقات مرة واحدة.

## الخطوة 4: إنشاء خيارات PDF

اربط إعدادات التصيير بإعدادات إخراج PDF.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## الخطوة 5: التصدير إلى PDF (إنشاء PDF من DXF)

أخيرًا، احفظ الطبقة المحددة كملف PDF. سيحتوي ملف PDF الناتج فقط على الهندسة من الطبقات التي حددتها.

```java
image.save(dataDir + "conic_pyramid_layer_out_.pdf", pdfOptions);
```

## المشكلات الشائعة والحلول

| المشكلة | السبب | الحل |
|-------|--------|-----|
| **لا يوجد إخراج أو PDF فارغ** | عدم تطابق اسم الطبقة أو حساسية الأحرف | تحقق من أسماء الطبقات الدقيقة في ملف DXF (استخدم عارض CAD) وتأكد من مطابقتها في `setLayers`. |
| **تحجيم غير صحيح** | عرض/ارتفاع الصفحة لا يتطابق مع وحدات الرسم | عدّل `setPageWidth` / `setPageHeight` أو اضبط `setResolution` في `CadRasterizationOptions`. |
| **استثناء الترخيص** | استخدام النسخة التجريبية دون تطبيق ترخيص | حمّل ملف الترخيص باستخدام `License license = new License(); license.setLicense("Aspose.CAD.Java.lic");`. |

## الأسئلة المتكررة

**س: هل يمكنني تصدير طبقات متعددة في آن واحد؟**  
ج: نعم. عدّل `stringList` في الخطوة 3 لتضم جميع أسماء الطبقات المطلوبة، مثل `Arrays.asList("LayerA", "LayerB")`.

**س: هل Aspose.CAD متوافق مع جميع إصدارات DXF؟**  
ج: يدعم Aspose.CAD مجموعة واسعة من إصدارات DXF، من R12 القديمة حتى أحدث الإصدارات، مما يضمن توافقًا واسعًا.

**س: كيف أتعامل مع الأخطاء أثناء عملية التصدير؟**  
ج: ضع كود التحميل والحفظ داخل كتلة `try‑catch` وسجّل تفاصيل `Exception`. سيمكنك ذلك من معالجة الملفات التالفة أو مشاكل الأذونات بشكل سلس.

**س: هل أحتاج إلى ترخيص تجاري للاستخدام في الإنتاج؟**  
ج: نعم. الترخيص المؤقت يكفي للتقييم، لكن الترخيص المدفوع يزيل العلامات المائية للتقييم ويفتح جميع الوظائف.

**س: أين يمكنني الحصول على مساعدة إضافية أو أمثلة؟**  
ج: زر [منتدى Aspose.CAD](https://forum.aspose.com/c/cad/19) للدعم المجتمعي، أو راجع توثيق API الرسمي لمزيد من عينات الكود.

## الخاتمة

لقد تعلمت الآن **كيفية إنشاء PDF من DXF** عن طريق تصدير طبقة محددة باستخدام Aspose.CAD للـ Java. يمنحك هذا الأسلوب تحكمًا كاملاً في المحتوى البصري للملف PDF الناتج، مما يجعله مثاليًا للمشاركة الخفيفة، التقارير المؤتمتة، أو دمج بيانات CAD في تطبيقات Java أكبر. لا تتردد في تجربة إعدادات تصيير مختلفة، اختيار طبقات متعددة، وتعديل خيارات PDF لتتناسب مع احتياجات مشروعك.

---

**آخر تحديث:** 2025-11-30  
**تم الاختبار مع:** Aspose.CAD للـ Java 24.11  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}