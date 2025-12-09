---
date: 2025-11-30
description: تعلم كيفية إضافة خصائص مخصصة لملفات DWG في جافا باستخدام Aspose.CAD.
  عزّز تنظيم واسترجاع المعلومات في رسومات CAD بسهولة.
linktitle: Add Custom Properties to DWG Files Using Java
second_title: Aspose.CAD Java API
title: إضافة خصائص مخصصة لملفات DWG باستخدام Aspose.CAD للـ Java
url: /ar/java/additional-features/add-custom-properties/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# إضافة خصائص مخصصة لملفات DWG باستخدام Aspose.CAD للـ Java

التعامل مع رسومات CAD برمجياً هو حاجة يومية للعديد من مطوري Java. في هذا الدرس ستكتشف **كيفية إضافة خصائص مخصصة لملفات dwg** باستخدام مكتبة Aspose.CAD للـ Java القوية. في نهاية الدليل ستحصل على مقتطف كود قابل لإعادة الاستخدام يضيف البيانات الوصفية مباشرةً إلى رأس ملف DWG، مما يجعل رسوماتك أسهل في الفهرسة والبحث والصيانة.

## المقدمة

Aspose.CAD للـ Java هي مكتبة مُدارة بالكامل ولا تعتمد على .NET تتيح لك قراءة وتعديل وكتابة مجموعة واسعة من صيغ CAD دون الحاجة إلى AutoCAD. إضافة خصائص مخصصة إلى ملف DWG يمنحك طريقة خفيفة لتخزين معلومات إضافية — مثل رموز المشروع، ملاحظات المراجعة، أو تفاصيل المالك — داخل ملف الرسم نفسه.

## إجابات سريعة

- **ماذا يعني “add custom properties dwg”؟** يعني إدراج أزواج اسم/قيمة معرفة من قبل المستخدم في بيانات رأس ملف DWG.  
- **أي مكتبة تتعامل مع هذا؟** Aspose.CAD للـ Java توفر API بسيطة لقراءة وكتابة تلك الخصائص.  
- **كم من الوقت تستغرق عملية التنفيذ؟** عادةً 5‑10 دقائق لمثال أساسي.  
- **هل أحتاج إلى ترخيص؟** الإصدار التجريبي المجاني يكفي للتطوير؛ يتطلب الترخيص التجاري للإنتاج.  
- **هل هو متوافق مع صيغ CAD أخرى؟** نعم—DXF، DWF، وأكثر مدعومة.

## ما هو إضافة خصائص مخصصة إلى ملفات DWG؟

الخصائص المخصصة هي أزواج مفتاح‑قيمة مخزنة في رأس ملف DWG. لا يتم عرضها في هندسة الرسم ولكن يمكن لأي تطبيق يدعم CAD الوصول إليها، مما يتيح إدارة بيانات أفضل، تقارير آلية، وتكامل مع أنظمة PLM.

## لماذا نستخدم Aspose.CAD لهذه المهمة؟

- **No AutoCAD dependency** – يعمل على أي نظام تشغيل أو خط أنابيب CI.  
- **Full‑featured API** – قراءة، تعديل، وحفظ دون فقدان الدقة.  
- **High performance** – يعالج الرسومات الكبيرة في ثوانٍ.  
- **Cross‑format support** – يعمل نفس الكود مع DXF، DWF، وغيرها.

## المتطلبات المسبقة

قبل أن تبدأ، تأكد من أن لديك:

- **Java Development Kit (JDK) 8+** مثبت ومُكوَّن في بيئة التطوير IDE الخاصة بك.  
- **Aspose.CAD للـ Java** المكتبة – قم بتحميل أحدث ملف JAR من [صفحة تحميل Aspose.CAD](https://releases.aspose.com/cad/java/).  
- ملف **DWG/DXF تجريبي** للتجربة (يستخدم الدرس `conic_pyramid.dxf`).

## استيراد المساحات الاسمية

أضف الاستيرادات المطلوبة إلى فئة Java الخاصة بك لتتمكن من العمل مع كائنات Aspose.CAD.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;

import java.util.Map;
```

## دليل خطوة بخطوة

### الخطوة 1: إعداد مشروعك

أنشئ مشروع Maven/Gradle جديد (أو مشروع IDE بسيط) وضع ملف JAR الخاص بـ Aspose.CAD في مسار الفئة (classpath). يضمن ذلك توفر حزم `com.aspose.cad.*` أثناء وقت التجميع.

### الخطوة 2: تعريف مسارات الملفات

حدد موقع الرسم المصدر ومكان كتابة الملف المعدل.

```java
String dataDir = "Your Document Directory" + "DXFDrawings/";
String srcFile = dataDir + "conic_pyramid.dxf";
String outFile = dataDir + "AddCustomProperties_out.dxf";
```

### الخطوة 3: تحميل ملف DWG

استخدم الطريقة الساكنة `Image.load` لقراءة الرسم إلى كائن `CadImage`.

```java
CadImage cadImage = (CadImage)Image.load(srcFile);
```

### الخطوة 4: إضافة خصائص مخصصة

أدخل البيانات الوصفية الخاصة بك مباشرةً في رأس الرسم. كل استدعاء يضيف زوج اسم/قيمة جديد.

```java
cadImage.getHeader().getCustomProperties().put("CUSTOM_PROPERTY_1", "Custom property test 1");
cadImage.getHeader().getCustomProperties().put("CUSTOM_PROPERTY_2", "Custom property test 2");
cadImage.getHeader().getCustomProperties().put("CUSTOM_PROPERTY_3", "Custom property test 3");
```

> **نصيحة:** حافظ على أسماء الخصائص مختصرة (حد أقصى 31 حرفًا) وتجنب المسافات للحفاظ على التوافق مع عارضات CAD القديمة.

### الخطوة 5: حفظ ملف DWG المعدل

احفظ التغييرات عن طريق استدعاء `save`. الآن يحتوي ملف الإخراج على الخصائص المخصصة التي أضفتها.

```java
cadImage.save(outFile);
```

### الخطوة 6: تنفيذ الكود

شغّل البرنامج من IDE أو سطر الأوامر. إذا تم الإعداد بشكل صحيح، سترى رسالة تأكيد.

```java
System.out.println("\nAddCustomProperties executed successfully.");
```

## المشكلات الشائعة والحلول

| المشكلة | السبب المحتمل | الحل |
|---------|--------------|-----|
| **`java.lang.NoClassDefFoundError: com/aspose/cad/Image`** | ملف JAR الخاص بـ Aspose.CAD غير موجود في مسار الفئة | أضف ملف JAR إلى مجلد `libs` في مشروعك أو أعلن عنه في Maven/Gradle. |
| **Properties not appearing in the saved file** | استخدام نسخة DWG لا تدعم الخصائص المخصصة | تأكد من أنك تعمل مع إصدارات DWG/DXF 2000 أو أحدث؛ قد تتجاهل الصيغ القديمة رؤوس مخصصة. |
| **`OutOfMemoryError` on large files** | تحميل رسم كبير جدًا دون استخدام التدفق | استخدم `Image.load` مع كائن `LoadOptions` الذي يتيح تحميلًا فعالًا للذاكرة. |

## الأسئلة المتكررة

**س: هل يمكنني إضافة خصائص مخصصة إلى صيغ CAD أخرى؟**  
ج: نعم. Aspose.CAD للـ Java يدعم DXF، DWF، DGN، وأكثر، وتعمل نفس واجهة `getHeader().getCustomProperties()` عبر هذه الصيغ.

**س: هل Aspose.CAD للـ Java متوافق مع جميع بيئات التطوير المتكاملة الرئيسية؟**  
ج: بالطبع. يعمل مع Eclipse، IntelliJ IDEA، NetBeans، وحتى عمليات بناء سطر الأوامر البسيطة.

**س: أين يمكنني العثور على مزيد من الأمثلة والوثائق التفصيلية؟**  
ج: قم بزيارة [مرجع Aspose.CAD Java API الرسمي](https://reference.aspose.com/cad/java/) للحصول على قائمة كاملة بالفئات، الطرق، ومشاريع العينة.

**س: هل يمكنني تجربة Aspose.CAD للـ Java قبل الشراء؟**  
ج: نعم — قم بتحميل نسخة تجريبية مجانية لمدة 30 يومًا من [صفحة تحميل Aspose.CAD](https://releases.aspose.com/).

**س: كيف أحصل على الدعم إذا واجهت صعوبات؟**  
ج: منتدى مجتمع Aspose وبوابة الدعم المخصصة لـ [Aspose.CAD](https://forum.aspose.com/c/cad/19) هي أماكن ممتازة لطرح الأسئلة ومشاركة الحلول.

---

**آخر تحديث:** 2025-11-30  
**تم الاختبار مع:** Aspose.CAD للـ Java 24.11  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}