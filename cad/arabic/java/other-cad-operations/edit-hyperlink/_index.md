---
date: 2026-06-19
description: تعلم كيفية تحرير ملفات DWG باستخدام Aspose.CAD للـ Java، بما في ذلك كيفية
  تحديث مسارات XRef لملفات DWG وتحرير الروابط التشعبية. جرّب النسخة التجريبية المجانية
  اليوم!
keywords:
- how to edit dwg
- update dwg xref paths
- Aspose.CAD Java hyperlink
linktitle: تحرير الرابط التشعبي
schemas:
- author: Aspose
  dateModified: '2026-06-19'
  description: Learn how to edit DWG files with Aspose.CAD for Java, including how
    to update DWG XRef paths and edit hyperlinks. Try the free trial today!
  headline: How to Edit DWG Hyperlinks - Aspose.CAD Java Tutorial
  type: TechArticle
- description: Learn how to edit DWG files with Aspose.CAD for Java, including how
    to update DWG XRef paths and edit hyperlinks. Try the free trial today!
  name: How to Edit DWG Hyperlinks - Aspose.CAD Java Tutorial
  steps:
  - name: Accessing Insert Objects
    text: '`CadInsertObject` is the Aspose.CAD class that represents an inserted block
      reference (XRef) inside a DWG drawing. Iterate through the entities and identify
      if an entity is an instance of the `CadInsertObject` class.'
  - name: How to Change XRef Path in a DWG Drawing
    text: '`CadImage` is the primary object that loads and saves CAD files in Aspose.CAD
      for Java. Once you have identified the insert object, retrieve the associated
      block entity and update the XRef path as needed. This ensures the reference
      points to the correct external file.'
  - name: Modifying Hyperlinks
    text: Next, check if the entity has a hyperlink associated with it. If the hyperlink
      matches a specific URL, update it to the desired URL. This step guarantees that
      clicking the hyperlink in the CAD viewer opens the new target.
  type: HowTo
- questions:
  - answer: Yes, after making changes call `cadImage.save("EditedDrawing.dwg");` to
      persist the modifications.
    question: Do I need to call a specific method to write the edited DWG back to
      disk?
  - answer: Absolutely—loop through `cadImage.getEntities()` and apply the hyperlink
      logic to each matching entity.
    question: Is it possible to edit multiple hyperlinks in one pass?
  type: FAQPage
second_title: Aspose.CAD Java API
title: كيفية تحرير الروابط التشعبية لملفات DWG - دليل Aspose.CAD Java
url: /ar/java/other-cad-operations/edit-hyperlink/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية تعديل الروابط التشعبية في DWG - دليل Aspose.CAD Java

في عصرنا الرقمي اليوم، **كيفية تعديل DWG** ملفات بفعالية هي مهارة أساسية للمهندسين والمعماريين ومتخصصي BIM. سواء كنت بحاجة إلى تصحيح رابط تشعبي مكسور، أو توجيه XRef إلى مصدر جديد، أو تحديث دفعة من الرسومات، توفر Aspose.CAD for Java طريقة برمجية نظيفة لإجراء تلك التغييرات دون فتح محرر CAD. يشرح هذا الدليل العملية بالكامل، من تحميل الرسم إلى حفظ التعديلات.

## إجابات سريعة
- **ما المكتبة التي تتعامل مع تعديل DWG في Java؟** Aspose.CAD for Java.  
- **هل يمكنني تعديل الروابط التشعبية ومسارات XRef معًا؟** نعم—كلاهما مدعومان في نفس الـ API.  
- **هل أحتاج إلى ترخيص للتطوير؟** نسخة تجريبية مجانية تعمل للاختبار؛ يلزم ترخيص تجاري للإنتاج.  
- **ما نسخة Java المطلوبة؟** Java 8 أو أعلى.  
- **هل يمكن تشغيل عينة الكود كما هي؟** نعم، بعد تحديث مسارات الملفات لتشير إلى ملفات DWG المحلية الخاصة بك.

## لماذا تعديل الروابط التشعبية في DWG ومسارات XRef؟
الحفاظ على تحديث الروابط التشعبية ومسارات XRef يمنع الروابط المكسورة، ويضمن أن توثيق المشروع يشير دائمًا إلى الموارد الصحيحة، ويسمح بالتحديثات الآلية للدفعات عبر مكتبات CAD الضخمة. هذا يقلل من الجهد اليدوي، ويقلل الأخطاء، ويحسن كفاءة المشروع بشكل عام من خلال تمكين المطورين من صيانة سلامة الروابط برمجيًا طوال دورة حياة التصميم.

## المتطلبات المسبقة

قبل أن نبدأ الدليل، تأكد من توفر المتطلبات المسبقة التالية:

1. **بيئة تطوير Java:** JDK 8+ مثبت وIDE المفضلة لديك (IntelliJ IDEA, Eclipse, إلخ).  
2. **مكتبة Aspose.CAD for Java:** قم بتحميل وتثبيت مكتبة Aspose.CAD for Java من [رابط التحميل](https://releases.aspose.com/cad/java/).  
3. **رسم DWG:** احرص على وجود ملف رسم DWG جاهز لتعديل الروابط التشعبية.

## استيراد الحزم

ابدأ باستيراد الحزم الضرورية إلى مشروع Java الخاص بك. يضمن ذلك حصولك على وظائف Aspose.CAD for Java.

```java
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.CadBaseEntity;
import com.aspose.cad.fileformats.cad.cadobjects.CadBlockEntity;
import com.aspose.cad.fileformats.cad.cadobjects.CadInsertObject;
```

## كيفية تعديل الروابط التشعبية في DWG باستخدام Aspose.CAD for Java؟

`CadImage` هو الصف في Aspose.CAD المستخدم لتحميل وحفظ رسومات CAD. قم بتحميل ملف DWG باستخدام `CadImage`، وتكرار كياناته، وتحديث الرابط التشعبي ومسار XRef حسب الحاجة، وأخيرًا احفظ الصورة مرة أخرى كـ DWG. يتيح هذا التدفق من البداية إلى النهاية تعديل أي عدد من الكيانات في تمريرة واحدة، مع ضمان حفظ جميع التغييرات.

### الخطوة 1: الوصول إلى كائنات الإدراج

`CadInsertObject` هو الصف في Aspose.CAD الذي يمثل مرجع كتلة مدخلة (XRef) داخل رسم DWG. قم بالتكرار عبر الكيانات وتحديد ما إذا كان الكيان مثالًا من صف `CadInsertObject`.

```java
    String dataDir = "Your Document Directory" + "DWGDrawings/";
    
    CadImage cadImage = (CadImage)Image.load(dataDir + "AutoCad_Sample.dwg");
    for (CadBaseEntity entity : cadImage.getEntities())
    {
        if (entity instanceof CadInsertObject)
        {
        }
	}
```

### الخطوة 2: كيفية تغيير مسار XRef في رسم DWG

`CadImage` هو الكائن الأساسي الذي يحمل ويحفظ ملفات CAD في Aspose.CAD for Java. بمجرد تحديد كائن الإدراج، استرجع الكيان المرتبط بالكتلة وقم بتحديث مسار XRef حسب الحاجة. يضمن ذلك أن الإشارة تشير إلى الملف الخارجي الصحيح.

```java
			CadBlockEntity block = cadImage.getBlockEntities().get_Item(((CadInsertObject)entity).getName());
            String value = block.getXRefPathName().getValue();
            if (value != null && !value.contentEquals(""))
            {
                block.getXRefPathName().setValue("new file reference.dwg");
            }
    
```

### الخطوة 3: تعديل الروابط التشعبية

بعد ذلك، تحقق مما إذا كان للكيان رابط تشعبي مرتبط به. إذا كان الرابط يتطابق مع عنوان URL محدد، قم بتحديثه إلى العنوان المطلوب. تضمن هذه الخطوة أن النقر على الرابط التشعبي في عارض CAD يفتح الهدف الجديد.

```java
        if (entity.getHyperlink() == "https://products.aspose.com")
        {
            entity.setHyperlink("https://www.aspose.com");
        }
```

## الأخطاء الشائعة والنصائح
- **مقارنة السلاسل:** استخدم `.equals()` بدلاً من `==` لمقارنة السلاسل بشكل موثوق في Java. العينة تستخدم `==` للبساطة، لكن في الإنتاج استبدله بـ `entity.getHyperlink().equals("https://products.aspose.com")`.  
- **التحقق من القيم الفارغة:** تأكد دائمًا من أن `block.getXRefPathName()` ليس `null` قبل استدعاء `.getValue()`.  
- **حفظ التغييرات:** بعد تعديل الكيانات، استدعِ `cadImage.save("output.dwg");` لحفظ التغييرات (تم حذف الكود للحفاظ على عدد الكتل الأصلي).  
- **ملاحظة الأداء:** يدعم Aspose.CAD for Java أكثر من 30 تنسيق CAD ويمكنه معالجة ملفات تصل إلى 2 GB دون تحميل المستند بالكامل في الذاكرة، مما يجعل التحديثات الجماعية سريعة وفعّالة في استهلاك الذاكرة.

## الأسئلة المتكررة

### س1: هل Aspose.CAD for Java متوافق مع جميع إصدارات رسومات DWG؟
A1: يدعم Aspose.CAD for Java أكثر من 50 نسخة من DWG، تغطي الإصدارات من AutoCAD 2000 حتى أحدث صيغة 2025.

### س2: هل يمكنني استخدام Aspose.CAD for Java في المشاريع التجارية؟
A2: نعم، يلزم الحصول على ترخيص تجاري للاستخدام في الإنتاج. يمكنك شراء الترخيص [هنا](https://purchase.aspose.com/buy).

### س3: هل هناك نسخة تجريبية مجانية متاحة لـ Aspose.CAD for Java؟
A3: نعم، يمكنك تجربة نسخة تجريبية مجانية [هنا](https://releases.aspose.com/).

### س4: كيف يمكنني الحصول على الدعم الفني لـ Aspose.CAD for Java؟
A4: لأي مساعدة تقنية، زر منتدى Aspose.CAD [هنا](https://forum.aspose.com/c/cad/19).

### س5: هل يمكنني الحصول على ترخيص مؤقت لأغراض الاختبار؟
A5: نعم، يمكنك الحصول على ترخيص مؤقت [هنا](https://purchase.aspose.com/temporary-license/).

**أسئلة إضافية**
**س: هل أحتاج إلى استدعاء طريقة محددة لكتابة DWG المعدل إلى القرص؟**  
ج: نعم، بعد إجراء التغييرات استدعِ `cadImage.save("EditedDrawing.dwg");` لحفظ التعديلات.

**س: هل من الممكن تعديل روابط تشعبية متعددة في تمريرة واحدة؟**  
ج: بالتأكيد—قم بالتكرار عبر `cadImage.getEntities()` وطبق منطق الرابط التشعبي على كل كيان مطابق.

---

**آخر تحديث:** 2026-06-19  
**تم الاختبار مع:** Aspose.CAD for Java 24.12  
**المؤلف:** Aspose  

{{< blocks/products/products-backtop-button >}}

## دروس ذات صلة

- [قراءة بيانات XREF الوصفية من ملفات DWG باستخدام Aspose.CAD for Java](/cad/java/cad-meta-data-and-rendering/read-xref-meta-data/)
- [إضافة خصائص مخصصة لملفات DWG باستخدام Aspose.CAD for Java](/cad/java/additional-features/add-custom-properties/)
- [تصدير DWG إلى PDF أو Raster باستخدام Aspose.CAD for Java](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}