---
date: 2025-11-29
description: تعلم كيفية تحويل DXF إلى WMF باستخدام Aspose.CAD للغة Java، تحميل رسم
  DXF، واستخدام تصدير Aspose إلى PDF كخيار. دليل خطوة بخطوة مع أمثلة على الشيفرة.
language: ar
linktitle: Export DXF to WMF Format Using Java
second_title: Aspose.CAD Java API
title: تحويل DXF إلى WMF باستخدام Aspose.CAD في Java
url: /java/additional-features/export-dxf-to-wmf/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تحويل DXF إلى WMF باستخدام Aspose.CAD في Java

## المقدمة

في هذا الدرس ستكتشف كيفية **تحويل DXF إلى WMF** باستخدام Aspose.CAD للـ Java. سواءً كنت بحاجة إلى تضمين رسومات CAD في تقرير يعمل على Windows أو ترغب فقط في الحصول على تنسيق متجه خفيف الوزن، فإن تحويل DXF إلى WMF هو طلب شائع. سنستعرض تحميل رسم DXF، تكوين خيارات الرستر، حفظ النتيجة كملف WMF، وحتى استخدام تصدير Aspose إلى PDF كخطوة اختيارية.

## إجابات سريعة
- **هل يمكنني تحويل DXF إلى WMF باستخدام نسخة تجريبية مجانية؟** نعم – تقدم Aspose نسخة تجريبية كاملة الوظائف لمدة 30 يومًا.  
- **ما إصدار Java المطلوب؟** Java 8 أو أحدث.  
- **هل أحتاج إلى ترخيص لتشغيل الكود؟** الترخيص مطلوب للإنتاج؛ النسخة التجريبية تعمل للتطوير والاختبار.  
- **هل التحويل بدون فقدان للجودة؟** يتم الحفاظ على البيانات المتجهة؛ خيارات الرستر تتيح لك التحكم في الدقة.  
- **هل يمكنني أيضًا تصدير نفس الرسم إلى PDF؟** بالتأكيد – راجع خطوة “التصدير إلى PDF” أدناه.

## ما هو “تحويل DXF إلى WMF”؟

تحويل DXF إلى WMF يعني أخذ ملف Drawing Exchange Format (DXF) — وهو تنسيق CAD شائع الاستخدام — وتحويله إلى Windows Metafile (WMF). WMF هو تنسيق صورة متجهة يندمج بسلاسة مع Microsoft Office، وتطبيقات Windows، والعديد من أدوات إعداد التقارير.

## لماذا نستخدم Aspose.CAD للـ Java؟

- **بدون تبعيات خارجية** – جافا صافية، لا ملفات DLL أصلية.  
- **دقة عالية** – يحافظ على الطبقات، الألوان، وأنماط الخطوط.  
- **رستر مدمج** – ضبط حجم الصفحة، الدقة، والخلفية بدقة.  
- **حل شامل** – نفس الـ API يدعم أيضًا التصدير إلى PDF، PNG، SVG، وأكثر.

## المتطلبات المسبقة

قبل أن تبدأ، تأكد من وجود ما يلي:

- **Aspose.CAD للـ Java** مدمج في مشروعك. حمّله من الموقع الرسمي: [تحميل Aspose.CAD Java](https://releases.aspose.com/cad/java/).  
- **دليل المستندات** حيث تُخزن ملفات DXF (مثال: `Your Document Directory/DXFDrawings/`).  

## استيراد المساحات الاسمية

في ملف Java المصدر، استورد فئات Aspose.CAD التي ستحتاجها:

```java
import com.aspose.cad.Color;
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.ifc.IfcImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.WmfOptions;
```

## دليل خطوة بخطوة

### الخطوة 1: تحميل رسم DXF

أولاً، **حمّل رسم DXF** الذي تريد تحويله. طريقة `Image.load` تقرأ الملف إلى الذاكرة.

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "DXFDrawings/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

### الخطوة 2: تكوين خيارات الرستر

قم بإعداد معلمات الرستر التي تتحكم في حجم ملف WMF الناتج. في هذا المثال نستخدم صفحة بحجم 100 × 100 وحدة.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(100);
rasterizationOptions.setPageHeight(100);
WmfOptions wmfOptions = new WmfOptions();
```

### الخطوة 3: حفظ كملف WMF

الآن احفظ الرسم المحمّل كملف WMF باستخدام الخيارات المعرفة أعلاه.

```java
cadImage.save(dataDir+" example.ifc.wmf", wmfOptions);
```

### الخطوة 4: تحرير الموارد

تحرير الموارد بشكل صحيح يمنع تسرب الذاكرة، خاصةً عند معالجة رسومات متعددة.

```java
finally
{
  cadImage.dispose();
}
```

### الخطوة 5: اختياري – تصدير Aspose إلى PDF

إذا كنت تحتاج أيضًا إلى نسخة PDF من نفس الرسم، فإن Aspose.CAD يجعل ذلك سطرًا واحدًا.

```java
image.save(dataDir + "conic_pyramid_out_.pdf"); 
```

> **نصيحة احترافية:** يمكنك إعادة استخدام كائن `CadRasterizationOptions` نفسه لتصدير PDF بتمريره إلى كائن `PdfOptions`.

## المشكلات الشائعة والحلول

| المشكلة | السبب | الحل |
|-------|-------|-----|
| **`NullPointerException` عند `cadImage.save`** | المتغيّر `cadImage` غير معرف (يجب أن يكون `image`). | استبدل `cadImage` بـ `image` أو أعد تسمية المتغيّر بشكل متسق. |
| **ملف WMF الناتج فارغ** | حجم صفحة الرستر صغير جدًا أو لون الخلفية مضبوط على شفاف. | زد `PageWidth`/`PageHeight` أو عيّن لون خلفية عبر `rasterizationOptions.setBackgroundColor(Color.getWhite());`. |
| **استثناء الترخيص** | تشغيل بدون ترخيص Aspose صالح في بيئة الإنتاج. | طبّق ملف الترخيص عند بدء التطبيق: `License license = new License(); license.setLicense("Aspose.Total.Java.lic");`. |

## الخاتمة

الآن لديك سير عمل كامل وجاهز للإنتاج **لتحويل DXF إلى WMF** باستخدام Aspose.CAD للـ Java، مع خطوة اختيارية **لتصدير Aspose إلى PDF**. يمنحك هذا النهج مخرجات متجهة عالية الجودة تتكامل بسلاسة مع أدوات إعداد التقارير والوثائق القائمة على Windows.

## الأسئلة المتكررة

### س1: أين يمكنني العثور على وثائق Aspose.CAD؟

ج1: يمكنك الوصول إلى الوثائق [هنا](https://reference.aspose.com/cad/java/).

### س2: كيف أحمل Aspose.CAD للـ Java؟

ج2: حمّل المكتبة [هنا](https://releases.aspose.com/cad/java/).

### س3: هل هناك نسخة تجريبية مجانية؟

ج3: نعم، يمكنك الحصول على نسخة تجريبية مجانية [هنا](https://releases.aspose.com/).

### س4: هل توجد خيارات ترخيص مؤقت؟

ج4: استكشف تراخيص مؤقتة [هنا](https://purchase.aspose.com/temporary-license/).

### س5: أين يمكنني الحصول على الدعم؟

ج5: زر منتدى دعم Aspose.CAD [هنا](https://forum.aspose.com/c/cad/19).

## أسئلة شائعة

**س: هل يمكنني تحويل ملفات DXF الكبيرة (مئات الميجابايت) دون نفاد الذاكرة؟**  
ج: نعم. حمّل الملف داخل كتلة `try‑with‑resources` وتخلّص من كائن `Image` فور الانتهاء. اضبط `CadRasterizationOptions.setPageWidth/Height` إلى حجم معقول لتقليل استهلاك الذاكرة.

**س: هل يحتفظ إخراج WMF بمعلومات الطبقات؟**  
ج: WMF هو تنسيق متجه مسطح، لذا يتم تسطيح هيكل الطبقات، لكن أنماط الخطوط والألوان تُحافظ عليها.

**س: هل يمكن تعيين DPI مخصص للـ WMF؟**  
ج: استخدم `rasterizationOptions.setResolution(300);` لتحديد DPI قبل الحفظ.

**س: هل يمكنني تحويل عدة ملفات DXF دفعة واحدة في تشغيل واحد؟**  
ج: بالتأكيد. قم بالتكرار عبر دليل، حمّل كل ملف، وطبق نفس منطق الرستر والحفظ.

**س: ما إصدارات Java المدعومة؟**  
ج: يدعم Aspose.CAD للـ Java Java 8 وما بعده (بما في ذلك Java 11، 17، وإصدارات LTS الأحدث).

---

**آخر تحديث:** 2025-11-29  
**تم الاختبار مع:** Aspose.CAD للـ Java 24.11  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}