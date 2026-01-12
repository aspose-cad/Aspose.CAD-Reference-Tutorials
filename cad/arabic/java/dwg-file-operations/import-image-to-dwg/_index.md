---
date: 2026-01-12
description: تعلم كيفية إضافة صورة إلى ملفات DWG باستخدام Aspose.CAD للغة Java وأيضًا
  تحويل DWG إلى PDF. اتبع دليلنا خطوة بخطوة لتطوير فعال.
linktitle: Import Image to DWG File Using Java
second_title: Aspose.CAD Java API
title: إضافة صورة إلى ملفات DWG بسهولة باستخدام Aspose.CAD Java
url: /ar/java/dwg-file-operations/import-image-to-dwg/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# إضافة صورة إلى ملفات DWG بسهولة باستخدام Aspose.CAD Java

في تطبيقات Java الحديثة، **إضافة صورة إلى DWG** ملفات هي متطلب شائع—سواء كنت تبني عارض CAD، أو تقوم بأتمتة تحديثات الرسومات، أو توليد وثائق. توفر Aspose.CAD for Java طريقة مباشرة وعالية الأداء لتضمين الصور النقطية مباشرة في رسومات DWG دون الحاجة إلى محرك CAD كامل. في هذا الدرس سنرشدك خلال العملية بالكامل، من تحميل ملف DWG إلى تصدير النتيجة كملف PDF.

## إجابات سريعة
- **ما المكتبة التي أحتاجها؟** Aspose.CAD for Java  
- **هل يمكنني أيضًا التصدير إلى PDF؟** نعم – استخدم `PdfOptions` مع `CadRasterizationOptions`  
- **هل أحتاج إلى ترخيص للتطوير؟** نسخة تجريبية مجانية تكفي للاختبار؛ يلزم ترخيص تجاري للإنتاج  
- **ما نسخة Java المدعومة؟** Java 8 وما فوق  
- **كم من الوقت تستغرق العملية؟** حوالي 10‑15 دقيقة لاستيراد صورة أساسي

## ما هو “إضافة صورة إلى dwg”؟
إضافة صورة إلى ملف DWG تعني إدراج صورة نقطية (PNG، JPEG، إلخ) ككائن `CadRasterImage` داخل مساحة النموذج (model space) للرسم. تصبح الصورة جزءًا من شجرة كائنات CAD ويمكن وضعها، وتكبيرها/تصغيرها، واقتصاصها مثل أي كائن CAD آخر.

## لماذا تستخدم Aspose.CAD for Java لإضافة صورة إلى dwg؟
- **لا يلزم وجود برنامج CAD** – تقوم الـ API بمعالجة تحليل DWG داخليًا.  
- **تحكم دقيق** في نقطة الإدراج، متجهات التكبير/التصغير، والاقتصاص.  
- **تحويل PDF مدمج** بحيث يمكنك إنشاء PDF قابل للطباعة في نفس سير العمل.  
- **متعدد المنصات** – يعمل على Windows وLinux وmacOS.

## المتطلبات المسبقة
- Aspose.CAD for Java: تأكد من تثبيت مكتبة Aspose.CAD. يمكنك تنزيلها [هنا](https://releases.aspose.com/cad/java/).  
- بيئة تطوير Java: JDK 8+ مع IDE المفضلة لديك (IntelliJ، Eclipse، VS Code، إلخ).

## Import Packages
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
أولاً، حدد المجلد الذي يحتوي على رسم DWG الخاص بك وقم بتحميله باستخدام `Image.load`.
```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String srcFile = dataDir + "Drawing11.dwg";
Image image = Image.load(srcFile);
```

### الخطوة 2: تعريف تعريف الصورة النقطية
أنشئ كائن `CadRasterImageDef` يشير إلى ملف PNG الخارجي الذي تريد تضمينه. يأخذ المُنشئ اسم ملف الصورة وأبعادها بالبكسل.
```java
CadRasterImageDef cadRasterImageDef = new CadRasterImageDef("road-sign-custom.png", 640, 562);
cadRasterImageDef.setObjectHandle("A3B4");
```

### الخطوة 3: تعيين نقطة الإدراج ومتجهات التكبير/التصغير
تحدد نقطة الإدراج مكان ظهور الزاوية السفلية اليسرى للصورة. متجهات **U** و **V** تتحكم في التكبير الأفقي والرأسي.
```java
Cad3DPoint insertionPoint = new Cad3DPoint(26.77, 22.35);
Cad3DPoint uVector = new Cad3DPoint(0.0061565450840500831, 0);
Cad3DPoint vVector = new Cad3DPoint(0, 0.0061565450840500822);
```

### الخطوة 4: إنشاء كائن CadRasterImage
اجمع التعريف، نقطة الإدراج، والمتجهات في كائن `CadRasterImage`. يمكنك أيضًا تعيين حدود الاقتصاص إذا كنت تريد إظهار جزء فقط من الصورة.
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
إذا كنت تحتاج أيضًا إلى نسخة PDF من الرسم، قم بتكوين `PdfOptions` مع `CadRasterizationOptions`. تُظهر هذه الخطوة كيفية **تحويل dwg إلى pdf** في نفس العملية.
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

باتباع هذه الخطوات، يمكنك **إضافة صورة إلى dwg** بسرعة وأيضًا **حفظ dwg كملف pdf** إذا لزم الأمر.

## المشكلات الشائعة والحلول
- **الصورة لا تظهر** – تحقق من أن مسار ملف الصورة (`road-sign-custom.png`) صحيح وأن أبعاد الصورة تتطابق مع القيم الممررة إلى `CadRasterImageDef`.  
- **التكبير غير صحيح** – اضبط متجهات U و V؛ فهي تمثل وحدات الرسم لكل بكسل.  
- **PDF يظهر فارغًا** – تأكد من أن `CadRasterizationOptions.setDrawType` مضبوط على `UseObjectColor` أو وضع مناسب آخر.

## الأسئلة المتكررة

**س: هل Aspose.CAD for Java متوافق مع جميع بيئات تطوير Java؟**  
ج: نعم، Aspose.CAD for Java متوافق مع معظم بيئات تطوير Java.

**س: هل يمكنني استخدام Aspose.CAD for Java للمشاريع التجارية؟**  
ج: نعم، يمكنك استخدام Aspose.CAD for Java للمشاريع التجارية. زر [هنا](https://purchase.aspose.com/buy) للحصول على تفاصيل الترخيص.

**س: هل هناك نسخة تجريبية مجانية متاحة لـ Aspose.CAD for Java؟**  
ج: نعم، يمكنك الوصول إلى النسخة التجريبية المجانية [هنا](https://releases.aspose.com/).

**س: كيف يمكنني الحصول على دعم لـ Aspose.CAD for Java؟**  
ج: يمكنك طلب الدعم في [منتدى Aspose.CAD](https://forum.aspose.com/c/cad/19).

**س: هل يمكنني الحصول على ترخيص مؤقت لـ Aspose.CAD for Java؟**  
ج: نعم، يمكنك الحصول على ترخيص مؤقت [هنا](https://purchase.aspose.com/temporary-license/).

---

**آخر تحديث:** 2026-01-12  
**تم الاختبار مع:** Aspose.CAD for Java 24.11  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}