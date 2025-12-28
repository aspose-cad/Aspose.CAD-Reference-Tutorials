---
date: 2025-12-28
description: تعلم كيفية إنشاء ملف PDF من CAD عن طريق تحويل DWG إلى PDF باستخدام Aspose.CAD
  للغة Java. اتبع التعليمات خطوة بخطوة لتصدير تخطيط DWG إلى PDF وإنشاء الصور.
linktitle: Render DWG Document to Image with Java
second_title: Aspose.CAD Java API
title: 'إنشاء PDF من CAD: DWG إلى صورة باستخدام Aspose.CAD للـ Java'
url: /ar/java/cad-meta-data-and-rendering/render-dwg-to-image/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تحويل مستند DWG إلى صورة باستخدام Aspose.CAD للـ Java

## المقدمة

في عالم تطوير Java الديناميكي، تبرز Aspose.CAD كأداة قوية للتعامل مع ملفات التصميم بمساعدة الحاسوب (CAD). **يُظهر هذا الدرس كيفية إنشاء PDF من CAD** عن طريق تحويل مستند DWG إلى صورة ثم تصديره إلى PDF. سواء كنت مطورًا متمرسًا أو تبدأ رحلتك البرمجية، سيوجهك هذا الدليل خطوة بخطوة عبر العملية بوضوح وسهولة.

## إجابات سريعة
- **ما المكتبة التي أحتاجها؟** Aspose.CAD للـ Java.  
- **هل يمكنني تحويل DWG إلى PDF؟** نعم – يوضح المثال تحويل تخطيط DWG إلى PDF.  
- **هل أحتاج إلى ترخيص للإنتاج؟** يلزم وجود ترخيص Aspose.CAD صالح للاستخدام غير التجريبي.  
- **ما هي بيئات التطوير المتكاملة المدعومة؟** Eclipse، IntelliJ IDEA، NetBeans، وأي بيئة تدعم Java.  
- **ما هي صيغ الإخراج المتاحة؟** PDF، PNG، JPEG، BMP، وغيرها من صيغ الرسوم النقطية.  

## ما هو إنشاء PDF من CAD؟

إنشاء PDF من CAD يعني أخذ رسم قائم على المتجهات (مثل ملف DWG) وتحويله إلى مستند PDF إما عبر التحويل إلى نقطية أو الاحتفاظ بالمتجهات. يتيح ذلك مشاركة الرسومات التقنية بسهولة، وطباعة، وأرشفة دون الحاجة إلى تطبيق CAD الأصلي.

## لماذا نستخدم Aspose.CAD للـ Java؟

- **بدون تبعيات خارجية** – المكتبة تعمل مباشرةً.  
- **عرض عالي الدقة** – يحافظ على وزن الخطوط، الطبقات، والتخطيطات.  
- **معالجة دفعات** – يمكنك تحويل عدة رسومات في تشغيل واحد.  
- **متعدد المنصات** – يعمل على Windows، Linux، و macOS.  

## المتطلبات المسبقة

- **بيئة تطوير Java** – JDK 8 أو أعلى مثبت.  
- **مكتبة Aspose.CAD للـ Java** – تحميل من [رابط التحميل](https://releases.aspose.com/cad/java/).  
- **مستند DWG** – ملف DWG ترغب في تحويله (عينة أو ملفك الخاص).  

## استيراد المساحات الاسمية

في كود Java الخاص بك، استورد الفئات الضرورية للاستفادة من وظائف Aspose.CAD:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

الآن، لنقسم مثال الكود إلى خطوات متعددة لفهم شامل:

## الخطوة 1: تحديد دليل الموارد

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

استبدل `"Your Document Directory"` بالمسار الفعلي حيث يتم تخزين ملفات DWG.

## الخطوة 2: تحميل مستند DWG

```java
String srcFile = dataDir + "visualization_-_conference_room.dwg";
Image image = Image.load(srcFile);
```

يقوم هذا بتحميل ملف DWG إلى كائن `Image` يمكن لـ Aspose.CAD التعامل معه.

## الخطوة 3: تعيين خيارات التحويل إلى نقطية

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
rasterizationOptions.setLayouts(new String[] {"Layout1"});
```

هنا نحدد كيفية تحويل الرسم إلى نقطية: حجم الصفحة والتخطيط المحدد للعرض. هذه هي الخطوة الأساسية لـ **render dwg to image** و **export dwg layout pdf**.

## الخطوة 4: إنشاء خيارات PDF

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

`PdfOptions` يربط إعدادات التحويل إلى نقطية بصيغة الإخراج PDF.

## الخطوة 5: التصدير إلى PDF

```java
image.save(dataDir + "ExportSpecificLayoutToPDF_out_.pdf", pdfOptions);
```

طريقة `save` تكتب الصورة المُحوَّلة إلى ملف PDF، مما يؤدي فعليًا إلى **convert dwg to pdf**.

## المشكلات الشائعة والحلول

| المشكلة | الحل |
|-------|----------|
| **File not found** | Verify that `dataDir` points to the correct folder and that the DWG filename is correct. |
| **Blank PDF output** | Ensure the layout name (`"Layout1"`) exists in the DWG file; use `image.getAvailableLayouts()` to list them. |
| **Low image quality** | Increase `PageWidth` and `PageHeight` or set `rasterizationOptions.setResolution(300);`. |

## الأسئلة المتكررة

### س1: هل يمكنني عرض تخطيطات متعددة من ملف DWG واحد؟

ج1: نعم، يمكنك ذلك. فقط عدل أسماء التخطيطات في مصفوفة `setLayouts` وفقًا لذلك.

### س2: هل Aspose.CAD متوافق مع بيئات تطوير Java المختلفة؟

ج2: نعم، Aspose.CAD متوافق مع بيئات تطوير Java الشهيرة مثل Eclipse، IntelliJ IDEA، وغيرها.

### س3: أين يمكنني العثور على مساعدة ودعم إضافيين؟

ج3: زر [منتدى Aspose.CAD](https://forum.aspose.com/c/cad/19) للحصول على دعم المجتمع والنقاشات.

### س4: كيف يمكنني الحصول على ترخيص مؤقت لـ Aspose.CAD؟

ج4: يمكنك الحصول على ترخيص مؤقت من [هنا](https://purchase.aspose.com/temporary-license/).

### س5: هل هناك المزيد من خيارات العرض المتاحة في Aspose.CAD؟

ج5: بالتأكيد، استكشف الـ [وثائق](https://reference.aspose.com/cad/java/) الشاملة للحصول على معلومات مفصلة.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**آخر تحديث:** 2025-12-28  
**تم الاختبار باستخدام:** Aspose.CAD for Java 24.11  
**المؤلف:** Aspose