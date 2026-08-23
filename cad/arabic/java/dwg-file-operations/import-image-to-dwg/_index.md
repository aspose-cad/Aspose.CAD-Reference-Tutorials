---
date: 2026-05-20
description: تعلم كيفية إضافة صورة إلى ملفات DWG باستخدام Aspose.CAD للـ Java وأيضًا
  تحويل DWG إلى PDF. اتبع دليلنا خطوة بخطوة للتطوير الفعال.
keywords:
- add image to dwg
- convert dwg to pdf
- import image into dwg
- embed raster image dwg
- dwg file operations
linktitle: استيراد صورة إلى ملف DWG باستخدام Java
schemas:
- author: Aspose
  dateModified: '2026-05-20'
  description: Learn how to add image to DWG files using Aspose.CAD for Java and also
    convert DWG to PDF. Follow our step-by-step guide for efficient development.
  headline: Add Image to DWG Files Effortlessly Using Aspose.CAD Java
  type: TechArticle
- description: Learn how to add image to DWG files using Aspose.CAD for Java and also
    convert DWG to PDF. Follow our step-by-step guide for efficient development.
  name: Add Image to DWG Files Effortlessly Using Aspose.CAD Java
  steps:
  - name: Load the DWG File
    text: First, point to the folder that contains your DWG drawing and load it with
      `Image.load`.
  - name: Define the Raster Image Definition
    text: The `CadRasterImageDef` class defines the external raster image resource
      to be embedded in the drawing.
  - name: Set Insertion Point and Scaling Vectors
    text: The insertion point determines where the lower‑left corner of the image
      will appear. The **U** and **V** vectors control horizontal and vertical scaling.
  - name: Create the CadRasterImage Object
    text: The `CadRasterImage` entity represents a raster picture placed in the DWG
      model space.
  - name: Add the Image to Model Space
    text: Insert the raster image into the `*Model_Space` block, then update the drawing’s
      object collection so the definition is saved.
  - name: Configure PDF Export Options (Optional)
    text: '`PdfOptions` specifies settings for saving a CAD drawing as a PDF file.
      `CadRasterizationOptions` defines how the CAD content is rasterized during PDF
      conversion.'
  - name: Save the Resulting PDF
    text: 'Finally, export the modified drawing as a PDF file. The same `image` instance
      is used, so the PDF reflects the newly added raster image. By following these
      steps, you can **add image to dwg** files quickly and also **save dwg as pdf**
      when needed, covering the most common **dwg file operations** in '
  type: HowTo
- questions:
  - answer: Yes, Aspose.CAD for Java works with any IDE that supports JDK 8+, including
      IntelliJ IDEA, Eclipse, and VS Code.
    question: Is Aspose.CAD for Java compatible with all Java development environments?
  - answer: Yes, you can use Aspose.CAD for Java for commercial projects. Visit **[here](https://purchase.aspose.com/buy)**
      for licensing details.
    question: Can I use Aspose.CAD for Java for commercial projects?
  - answer: Yes, you can access the free trial **[here](https://releases.aspose.com/)**.
    question: Is there a free trial available for Aspose.CAD for Java?
  - answer: You can seek support on the **[Aspose.CAD forum](https://forum.aspose.com/c/cad/19)**.
    question: How can I get support for Aspose.CAD for Java?
  - answer: Yes, you can get a temporary license **[here](https://purchase.aspose.com/temporary-license/)**.
    question: Can I obtain a temporary license for Aspose.CAD for Java?
  type: FAQPage
second_title: Aspose.CAD Java API
title: إضافة صورة إلى ملفات DWG بسهولة باستخدام Aspose.CAD Java
url: /ar/java/dwg-file-operations/import-image-to-dwg/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# إضافة صورة إلى ملفات DWG بسهولة باستخدام Aspose.CAD Java

في تطبيقات Java الحديثة، **إضافة صورة إلى DWG** ملفات هي متطلب شائع — سواء كنت تبني عارض CAD، أو تقوم بأتمتة تحديثات الرسومات، أو توليد الوثائق. توفر Aspose.CAD for Java طريقة مباشرة وعالية الأداء لدمج الصور النقطية مباشرةً في رسومات DWG دون الحاجة إلى محرك CAD كامل. في هذا البرنامج التعليمي سنرشدك خلال العملية بالكامل، من تحميل ملف DWG إلى تصدير النتيجة كملف PDF، وسنغطي أيضًا كيفية **استيراد صورة إلى dwg** و **تحويل dwg إلى pdf** في سير عمل واحد.

## إجابات سريعة
- **ما المكتبة التي أحتاجها؟** Aspose.CAD for Java  
- **هل يمكنني أيضًا التصدير إلى PDF؟** نعم – استخدم `PdfOptions` مع `CadRasterizationOptions`  
- **هل أحتاج إلى ترخيص للتطوير؟** نسخة تجريبية مجانية تعمل للاختبار؛ يلزم ترخيص تجاري للإنتاج  
- **ما نسخة Java المدعومة؟** Java 8 وما فوق  
- **كم يستغرق التنفيذ؟** حوالي 10‑15 دقيقة لاستيراد صورة أساسي  

## ما هو “إضافة صورة إلى dwg”؟
إضافة صورة إلى ملف DWG تعني دمج صورة نقطية (PNG، JPEG، إلخ) ككيان **CadRasterImage** داخل مساحة نموذج الرسم، حيث يمكن وضعها، وتكبيرها/تصغيرها، وربما قصها مثل أي كائن CAD آخر. يتم تخزينها في جدول كائنات الرسم وتُعرض بواسطة عارضات CAD القياسية.

## لماذا تستخدم Aspose.CAD for Java لإضافة صورة إلى dwg؟
يمكنك دمج الرسومات النقطية في ملفات DWG دون تثبيت أي برنامج CAD من طرف ثالث، وتوفر API تحكمًا دقيقًا على نقطة الإدراج، ومتجهات التكبير/التصغير، وحدود القص. تعالج Aspose.CAD ملفات تصل إلى 2 GB، وتدعم **أكثر من 50 صيغة إدخال وإخراج**، وتعمل على Windows وLinux وmacOS، مما يتيح لك دمج معالجة CAD في أي خلفية مبنية على Java.

## المتطلبات المسبقة
- **Aspose.CAD for Java** – قم بتنزيل أحدث JAR من الموقع الرسمي **[هنا](https://releases.aspose.com/cad/java/)**.  
- **Java Development Kit** – JDK 8 أو أحدث، مع بيئة التطوير المفضلة لديك (IntelliJ IDEA، Eclipse، VS Code، إلخ).  
- ترخيص **Aspose.CAD** صالح للاستخدام في الإنتاج (النسخة التجريبية تعمل للتجربة).  

## استيراد الحزم
تستورد التعليمات التالية الفئات الأساسية من Aspose.CAD المستخدمة في معالجة الصور وتحويل PDF.

```java
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.cad.CadDrawTypeMode;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.*;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## دليل خطوة بخطوة

### الخطوة 1: تحميل ملف DWG
أولاً، حدد المجلد الذي يحتوي على رسم DWG الخاص بك وحمّله باستخدام `Image.load`.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String srcFile = dataDir + "Drawing11.dwg";
Image image = Image.load(srcFile);
```

### الخطوة 2: تعريف تعريف الصورة النقطية
تحدد فئة `CadRasterImageDef` المورد الخارجي للصورة النقطية الذي سيتم دمجه في الرسم.

```java
CadRasterImageDef cadRasterImageDef = new CadRasterImageDef("road-sign-custom.png", 640, 562);
cadRasterImageDef.setObjectHandle("A3B4");
```

### الخطوة 3: تعيين نقطة الإدراج ومتجهات التكبير
تحدد نقطة الإدراج مكان ظهور الزاوية السفلية اليسرى للصورة. تتحكم المتجهات **U** و **V** في التكبير الأفقي والعمودي.

```java
Cad3DPoint insertionPoint = new Cad3DPoint(26.77, 22.35);
Cad3DPoint uVector = new Cad3DPoint(0.0061565450840500831, 0);
Cad3DPoint vVector = new Cad3DPoint(0, 0.0061565450840500822);
```

### الخطوة 4: إنشاء كائن CadRasterImage
يمثل الكيان `CadRasterImage` صورة نقطية موضوعة في مساحة نموذج DWG.

```java
CadRasterImage cadRasterImage = new CadRasterImage(cadRasterImageDef, insertionPoint, uVector, vVector);
cadRasterImage.setImageDefReference("A3B4");
cadRasterImage.setDisplayFlags((short)7);
cadRasterImage.setClippingState((short)0);
cadRasterImage.getClipBoundaryVertexList().add(new Cad2DPoint(-0.5, 0.5));
cadRasterImage.getClipBoundaryVertexList().add(new Cad2DPoint(639.5, 561.5));
```

### الخطوة 5: إضافة الصورة إلى مساحة النموذج
أدرج الصورة النقطية في كتلة `*Model_Space`، ثم حدّث مجموعة كائنات الرسم بحيث يتم حفظ التعريف.

```java
CadImage cadImage = ((CadImage)(image));
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(cadRasterImage);
CadBaseObject[] objs = cadImage.getObjects();
CadBaseObject[] arr = new CadBaseObject[objs.length + 1];
int ind = 0;
for (CadBaseObject obj : objs)
{
    arr[ind] = obj;
    ind++;
}
arr[ind] = cadRasterImageDef;
cadImage.setObjects(arr);
```

### الخطوة 6: تكوين خيارات تصدير PDF (اختياري)
`PdfOptions` يحدد الإعدادات لحفظ رسم CAD كملف PDF. `CadRasterizationOptions` يحدد كيفية تحويل محتوى CAD إلى صورة نقطية أثناء تحويل PDF.

```java
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setDrawType(CadDrawTypeMode.UseObjectColor);
cadRasterizationOptions.setPageHeight(1600);
cadRasterizationOptions.setPageWidth(1600);
cadRasterizationOptions.setLayouts(new String[] {"Model"});
```

### الخطوة 7: حفظ ملف PDF الناتج
أخيرًا، صدّر الرسم المعدل كملف PDF. يتم استخدام نفس كائن `image`، لذا يعكس PDF الصورة النقطية المضافة حديثًا.

```java
image.save((srcFile + "_generated.pdf"), pdfOptions);
```

باتباع هذه الخطوات، يمكنك **إضافة صورة إلى dwg** بسرعة وأيضًا **حفظ dwg كـ pdf** عند الحاجة، مما يغطي أكثر عمليات **ملفات dwg** شيوعًا في روتين واحد ومختصر.

## المشكلات الشائعة والحلول
- **الصورة لا تظهر** – تحقق من أن مسار ملف الصورة (`road-sign-custom.png`) صحيح وأن أبعاد الصورة تطابق القيم الممررة إلى `CadRasterImageDef`.  
- **التكبير غير صحيح** – اضبط المتجهات U و V؛ فهي تمثل وحدات الرسم لكل بكسل.  
- **PDF يظهر فارغًا** – تأكد من أن `CadRasterizationOptions.setDrawType` مضبوط على `UseObjectColor` أو وضع مناسب آخر.  

## الأسئلة المتكررة

**س: هل Aspose.CAD for Java متوافق مع جميع بيئات تطوير Java؟**  
ج: نعم، يعمل Aspose.CAD for Java مع أي بيئة تطوير تدعم JDK 8+، بما في ذلك IntelliJ IDEA وEclipse وVS Code.

**س: هل يمكنني استخدام Aspose.CAD for Java للمشاريع التجارية؟**  
ج: نعم، يمكنك استخدام Aspose.CAD for Java للمشاريع التجارية. زر **[هنا](https://purchase.aspose.com/buy)** للحصول على تفاصيل الترخيص.

**س: هل هناك نسخة تجريبية مجانية متاحة لـ Aspose.CAD for Java؟**  
ج: نعم، يمكنك الوصول إلى النسخة التجريبية **[هنا](https://releases.aspose.com/)**.

**س: كيف يمكنني الحصول على الدعم لـ Aspose.CAD for Java؟**  
ج: يمكنك طلب الدعم على **[منتدى Aspose.CAD](https://forum.aspose.com/c/cad/19)**.

**س: هل يمكنني الحصول على ترخيص مؤقت لـ Aspose.CAD for Java؟**  
ج: نعم، يمكنك الحصول على ترخيص مؤقت **[هنا](https://purchase.aspose.com/temporary-license/)**.

**آخر تحديث:** 2026-05-20  
**تم الاختبار باستخدام:** Aspose.CAD for Java 24.11  
**المؤلف:** Aspose  

{{< blocks/products/products-backtop-button >}}

## دروس ذات صلة

- [تصدير DWG إلى PDF أو صورة نقطية باستخدام Aspose.CAD for Java](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)
- [إضافة خصائص مخصصة لملفات DWG باستخدام Aspose.CAD for Java](/cad/java/additional-features/add-custom-properties/)
- [حفظ CAD كـ PNG – تحويل رسم CAD إلى صيغة صورة نقطية باستخدام Aspose.CAD for Java](/cad/java/cad-drawing-conversion/convert-cad-drawing-to-raster-image/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}