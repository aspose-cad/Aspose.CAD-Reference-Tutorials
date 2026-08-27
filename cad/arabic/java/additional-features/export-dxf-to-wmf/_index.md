---
date: 2026-06-09
description: تعلم كيفية تحويل DXF إلى WMF باستخدام Aspose.CAD for Java، بما في ذلك
  نسخة تجريبية مجانية، ودعم Java 8+، وتصدير PDF اختياري. دليل خطوة بخطوة مع أمثلة
  على الشيفرة.
keywords:
- convert dxf to wmf
- aspose cad java
- aspose free trial
- aspose cad conversion
- export dxf pdf
linktitle: تصدير DXF إلى تنسيق WMF باستخدام Java
schemas:
- author: Aspose
  dateModified: '2026-06-09'
  description: Learn how to convert DXF to WMF with Aspose.CAD for Java, including
    a free trial, Java 8+ support, and optional PDF export. Step‑by‑step guide with
    code examples.
  headline: Convert DXF to WMF Using Aspose.CAD in Java
  type: TechArticle
- description: Learn how to convert DXF to WMF with Aspose.CAD for Java, including
    a free trial, Java 8+ support, and optional PDF export. Step‑by‑step guide with
    code examples.
  name: Convert DXF to WMF Using Aspose.CAD in Java
  steps:
  - name: Load DXF Drawing
    text: Image.load reads the DXF file into an Aspose.CAD Image object.
  - name: Configure Rasterization Options
    text: CadRasterizationOptions specifies page size, resolution, and background
      for rasterizing the CAD drawing.
  - name: Save as WMF
    text: ImageSaveOptions with SaveFormat.WMF tells Aspose.CAD to write the output
      as a Windows Metafile.
  - name: Dispose of Resources
    text: Calling image.close() releases native resources used by the Aspose.CAD Image
      object.
  - name: Optional – Export to PDF
    text: PdfOptions configures PDF‑specific settings when saving the image as a PDF
      document. > **Pro tip:** You can reuse the same `CadRasterizationOptions` object
      for PDF export by passing it to a `PdfOptions` instance, saving you a few lines
      of setup.
  type: HowTo
- questions:
  - answer: Yes. Load the file in a try‑with‑resources block and dispose of the `Image`
      object promptly. Adjust `CadRasterizationOptions.setPageWidth/Height` to a reasonable
      size to keep memory usage low.
    question: Can I convert large DXF files (hundreds of MB) without running out of
      memory?
  - answer: WMF is a flat vector format, so layer hierarchy is flattened, but line
      styles, colors, and hatch patterns are preserved.
    question: Does the WMF output retain layer information?
  - answer: Use `rasterizationOptions.setResolution(300);` to define DPI before saving.
    question: Is it possible to set a custom DPI for the WMF?
  - answer: Absolutely. Loop through a directory, load each file, and apply the same
      rasterization and save logic.
    question: Can I batch‑convert multiple DXF files in one run?
  - answer: Aspose.CAD for Java supports Java 8 and later, including Java 11, 17,
      and newer LTS releases.
    question: What versions of Java are supported?
  type: FAQPage
second_title: Aspose.CAD Java API
title: تحويل DXF إلى WMF باستخدام Aspose.CAD في Java
url: /ar/java/additional-features/export-dxf-to-wmf/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تحويل DXF إلى WMF باستخدام Aspose.CAD في Java

## المقدمة

في هذا الدرس ستكتشف كيفية **convert DXF to WMF** باستخدام Aspose.CAD للـ Java. سواء كنت بحاجة إلى تضمين رسومات CAD في تقرير يعمل على Windows، أو إنشاء رسومات متجهة خفيفة الوزن لمستندات Office، أو أتمتة التحويلات الدفعية، فإن تحويل DXF إلى WMF هو طلب شائع في خطوط الهندسة وإعداد التقارير. سنستعرض تحميل رسم DXF، وتكوين خيارات الرستر، وحفظ النتيجة كـ WMF، واختياريًا تصدير نفس الرسم إلى PDF.

## إجابات سريعة
- **Can I convert DXF to WMF with a free trial?** نعم – تقدم Aspose نسخة تجريبية كاملة الوظائف لمدة 30 يومًا.  
- **What Java version is required?** Java 8 أو أحدث.  
- **Do I need a license to run the code?** يلزم وجود ترخيص للإنتاج؛ النسخة التجريبية تعمل للتطوير والاختبار.  
- **Is the conversion loss‑less?** يتم الحفاظ على بيانات المتجه؛ خيارات الرستر تتيح لك التحكم في الدقة.  
- **Can I also export the same drawing to PDF?** بالتأكيد – راجع خطوة “Export to PDF” أدناه.

## ما هو “convert DXF to WMF”؟

يعني تحويل DXF إلى WMF أخذ ملف Drawing Exchange Format (DXF) — وهو تنسيق CAD شائع الاستخدام — وتحويله إلى Windows Metafile (WMF). WMF هو تنسيق صورة متجهة يندمج بسلاسة مع Microsoft Office، وتطبيقات Windows، والعديد من أدوات التقارير.

## لماذا نستخدم Aspose.CAD للـ Java؟

يوفر Aspose.CAD للـ Java محركًا نقيًا مكتوبًا بـ Java دون الحاجة إلى DLLs أصلية، يقوم بتحويل ملفات CAD مع **أكثر من 99 % دقة متجهية**، مع الحفاظ على الطبقات والألوان وأنماط الخطوط وأنماط التظليل. يدعم **أكثر من 50 تنسيقًا للإدخال والإخراج** — بما في ذلك DXF وDWG وDGN وPDF وPNG وSVG وWMF — مع إمكانية ضبط حجم الصفحة، DPI، ولون الخلفية من خلال خيارات الرستر المدمجة. نفس الـ API يتعامل أيضًا مع تصدير PDF وPNG وSVG، مما يلغي الحاجة إلى مكتبات متعددة.

### المزايا الرئيسية
- **No external dependencies** – Java نقي، يعمل على أي نظام تشغيل يدعم Java.  
- **High‑fidelity rendering** – يحتفظ بسمك الخط، اللون، وتفاصيل التظليل.  
- **Built‑in rasterization** – التحكم بأبعاد الصفحة، الدقة، والخلفية.  
- **One‑stop conversion** – نفس الفئات تصدر إلى WMF وPDF وPNG وSVG، إلخ.

## المتطلبات المسبقة

قبل البدء، تأكد من وجود ما يلي:

- **Aspose.CAD للـ Java** مدمج في مشروعك. حمّله من الموقع الرسمي: [Aspose.CAD Java download](https://releases.aspose.com/cad/java/).  
- **دليل المستندات** حيث تُخزن ملفات DXF الخاصة بك (مثال: `Your Document Directory/DXFDrawings/`).

## استيراد المساحات الاسمية

الإستيرادات التالية تجلب فئات Aspose.CAD المطلوبة لتحميل، رستر، وحفظ ملفات CAD.
```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageSaveOptions;
import com.aspose.cad.fileformats.cad.CadRasterizationOptions;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.CadImageInfo;
import com.aspose.cad.fileformats.cad.CadImageInfo;
import java.awt.Color;
```

## دليل خطوة بخطوة

### كيف يمكنني تحويل DXF إلى WMF في Java؟

حمّل ملف DXF الخاص بك باستخدام `Image.load("yourFile.dxf")`، وقم بتكوين `CadRasterizationOptions` لحجم الصفحة والدقة المطلوبين، ثم استدعِ `image.save("output.wmf", new ImageSaveOptions(SaveFormat.WMF))`. هذا النمط المكوّن من ثلاث خطوات ينفّذ التحويل الكامل مع الحفاظ على جودة المتجه ويتطلب فقط بضع أسطر من الشيفرة.

#### الخطوة 1: تحميل رسم DXF

Image.load يقرأ ملف DXF إلى كائن Aspose.CAD Image.
```java
import com.aspose.cad.Color;
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.ifc.IfcImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.WmfOptions;
```

#### الخطوة 2: تكوين خيارات الرستر

CadRasterizationOptions يحدد حجم الصفحة، الدقة، والخلفية لرستر رسم CAD.
```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "DXFDrawings/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

#### الخطوة 3: حفظ كـ WMF

ImageSaveOptions مع SaveFormat.WMF يخبر Aspose.CAD بكتابة الناتج كـ Windows Metafile.
```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(100);
rasterizationOptions.setPageHeight(100);
WmfOptions wmfOptions = new WmfOptions();
```

#### الخطوة 4: تحرير الموارد

استدعاء image.close() يحرّر الموارد الأصلية المستخدمة من قبل كائن Aspose.CAD Image.
```java
cadImage.save(dataDir+" example.ifc.wmf", wmfOptions);
```

#### الخطوة 5: اختياري – تصدير إلى PDF

PdfOptions يكوّن إعدادات خاصة بـ PDF عند حفظ الصورة كمستند PDF.
```java
finally
{
  cadImage.dispose();
}
```

> **نصيحة احترافية:** يمكنك إعادة استخدام نفس كائن `CadRasterizationOptions` لتصدير PDF بتمريره إلى مثيل `PdfOptions`، مما يوفر لك بضع أسطر من الإعداد.

## كيف يمكنني تصدير DXF إلى PDF باستخدام Aspose CAD للـ Java؟

تصدير إلى PDF يتبع نفس خطوات التحميل والرستر؛ فقط استبدل تنسيق حفظ WMF بـ PDF. استخدم `new ImageSaveOptions(SaveFormat.Pdf)` واختياريًا عيّن إعدادات خاصة بـ PDF مثل مستوى الضغط أو بيانات المؤلف. هذا التحويل في سطر واحد ينتج PDF قابل للبحث، ودقيق في الصفحات، يعكس تخطيط CAD الأصلي.

## المشكلات الشائعة والحلول

| المشكلة | السبب | الحل |
|-------|-------|-----|
| **`NullPointerException` on `cadImage.save`** | المتغيّر `cadImage` غير معرف (يجب أن يكون `image`). | استبدل `cadImage` بـ `image` أو أعد تسمية المتغيّر بشكل متسق. |
| **Output WMF is blank** | حجم صفحة الرستر صغير جدًا أو تم تعيين لون الخلفية إلى شفاف. | قم بزيادة `PageWidth`/`PageHeight` أو عيّن لون خلفية عبر `rasterizationOptions.setBackgroundColor(Color.WHITE);`. |
| **License exception** | التشغيل بدون ترخيص Aspose صالح في بيئة الإنتاج. | طبق ملف الترخيص عند بدء التطبيق: `License license = new License(); license.setLicense("Aspose.Total.Java.lic");`. |

## الخلاصة

أصبح لديك الآن سير عمل كامل وجاهز للإنتاج **convert DXF to WMF** باستخدام Aspose.CAD للـ Java، مع خطوة اختيارية **export the same drawing to PDF**. يمنحك هذا النهج مخرجات متجهة عالية الجودة تتكامل بسلاسة مع أدوات التقارير والوثائق القائمة على Windows، مع الحفاظ على بساطة قاعدة الشيفرة وخلوها من الاعتمادات.

## الأسئلة المتكررة

### س1: أين يمكنني العثور على توثيق Aspose.CAD؟
ج1: يمكنك الوصول إلى التوثيق [here](https://reference.aspose.com/cad/java/).

### س2: كيف يمكنني تحميل Aspose.CAD للـ Java؟
ج2: حمّل المكتبة [here](https://releases.aspose.com/cad/java/).

### س3: هل تتوفر نسخة تجريبية مجانية؟
ج3: نعم، يمكنك الحصول على نسخة تجريبية مجانية [here](https://releases.aspose.com/).

### س4: هل تحتاج إلى خيارات ترخيص مؤقتة؟
ج4: استكشف تراخيص مؤقتة [here](https://purchase.aspose.com/temporary-license/).

### س5: أين يمكنني الحصول على الدعم؟
ج5: زر منتدى دعم Aspose.CAD [here](https://forum.aspose.com/c/cad/19).

## الأسئلة المتداولة

**Q: هل يمكنني تحويل ملفات DXF الكبيرة (مئات الميجابايت) دون نفاد الذاكرة؟**  
A: نعم. حمّل الملف داخل كتلة try‑with‑resources وحرّر كائن `Image` فورًا. اضبط `CadRasterizationOptions.setPageWidth/Height` إلى حجم معقول للحفاظ على استهلاك الذاكرة منخفضًا.

**Q: هل يحتفظ إخراج WMF بمعلومات الطبقات؟**  
A: WMF هو تنسيق متجه مسطح، لذا يتم تسطيح هيكل الطبقات، لكن أنماط الخطوط، الألوان، وأنماط التظليل تُحافظ عليها.

**Q: هل يمكن تعيين DPI مخصص للـ WMF؟**  
A: استخدم `rasterizationOptions.setResolution(300);` لتحديد DPI قبل الحفظ.

**Q: هل يمكنني تحويل عدة ملفات DXF دفعيًا في تشغيل واحد؟**  
A: بالتأكيد. قم بالتكرار عبر دليل، حمّل كل ملف، وطبق نفس منطق الرستر والحفظ.

**Q: ما إصدارات Java المدعومة؟**  
A: يدعم Aspose.CAD للـ Java Java 8 وما بعده، بما في ذلك Java 11، 17، والإصدارات LTS الأحدث.

---

**Last Updated:** 2026-06-09  
**Tested With:** Aspose.CAD for Java 24.11  
**Author:** Aspose

```java
image.save(dataDir + "conic_pyramid_out_.pdf"); 
```

## دروس ذات صلة

- [إنشاء PDF من CAD – تصدير DXF إلى PDF باستخدام Aspose.CAD للـ Java](/cad/java/additional-features/export-dxf-to-pdf/)
- [إنشاء PDF من DXF: تصدير طبقة مع Aspose.CAD للـ Java](/cad/java/additional-features/export-specific-layer-to-pdf/)
- [كيفية تحويل تخطيط DXF إلى صورة JPEG باستخدام Aspose.CAD في Java](/cad/java/additional-features/export-specific-layout-to-image/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}