---
date: 2026-05-04
description: تعلم كيفية تحويل DXF إلى DWG وتعيين الخط الأساسي في Java باستخدام Aspose.CAD.
  دليل خطوة بخطوة للحصول على رسومات CAD مثالية.
keywords:
- convert dxf to dwg
- set primary font
- change dwg text style
- how to substitute font
- aspose cad licensing
linktitle: استبدال الخط في DWG
second_title: Aspose.CAD Java API
title: تحويل dxf إلى dwg وتغيير الخط في DWG باستخدام Aspose.CAD Java
url: /ar/java/cad-text-and-annotation/substitute-font-in-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية تحميل ملف DWG في Java واستبدال الخط باستخدام Aspose.CAD

## مقدمة

إذا كنت بحاجة إلى **convert dxf to dwg** في تطبيقات Java ومنح رسوماتك مظهرًا مصقولًا، فإن استبدال الخط يُعد حلاً سريعًا. باستخدام Aspose.CAD for Java يمكنك استبدال نمط النص الافتراضي بأي خط مثبت على النظام، مما يضمن ظهور كل تعليق بالضبط كما تتوقع. في هذا البرنامج التعليمي سنستعرض العملية بالكامل — من تحميل ملف DWG في Java إلى استخدام طريقة `setPrimaryFontName` لتغيير الخط.

## إجابات سريعة
- **ما المكتبة التي أحتاجها؟** Aspose.CAD for Java.  
- **هل يمكنني تحميل ملف DWG في Java؟** نعم، ما عليك سوى استدعاء `Image.load()` على مسار DWG.  
- **أي طريقة تغير الخط؟** `setPrimaryFontName`.  
- **هل أحتاج إلى ترخيص للإنتاج؟** نعم، يلزم الحصول على ترخيص تجاري.  
- **هل المعالجة الدفعية ممكنة؟** بالتأكيد – قم بتكرار عدة ملفات باستخدام نفس الشيفرة.

## ما هو **convert dxf to dwg**؟

تشير عبارة “convert dxf to dwg” إلى تحويل ملف DXF (Drawing Exchange Format) إلى تنسيق DWG الأصلي المستخدم في العديد من تطبيقات CAD. يتيح التحويل لك أخذ رسم DXF المدعوم على نطاق واسع، وإدخاله في سير عمل DWG، ثم تطبيق تنسيقات متقدمة — مثل استبدال الخط — باستخدام Aspose.CAD.

## لماذا استبدال الخطوط في ملف DWG؟

- **الاتساق:** يضمن أن جميع المتعاونين يرون نفس الخط، بغض النظر عن إعدادات الخط المحلية لديهم.  
- **قابلية القراءة:** بعض خطوط CAD الافتراضية يصعب قراءتها على الشاشات؛ استبدالها بخط نظيف مثل Arial يحسن الوضوح.  
- **العلامة التجارية:** يطابق الرسومات التقنية مع دليل الأنماط المؤسسية.

## حالات الاستخدام الشائعة

| السيناريو | لماذا يهم |
|----------|-----------|
| **تحويل دفعي للرسومات DXF القديمة** | يمكنك تحويلها إلى DWG وتطبيق خط الشركة في خطوة واحدة. |
| **تحضير الرسومات لعروض العملاء** | الخطوط المتسقة والقابلة للقراءة تجعل المستندات تبدو احترافية. |
| **خطوط أنابيب CAD المؤتمتة** | إدراج استبدال الخط يلغي خطوات المعالجة اللاحقة اليدوية. |

## المتطلبات المسبقة

- **Java Development Kit (JDK)** – أي نسخة حديثة (يوصى بالإصدار 8 أو أعلى).  
- **Aspose.CAD for Java** – حمّل من [الموقع](https://releases.aspose.com/cad/java/).  
- **Sample DWG/DXF file** – رسم تريد تعديله (يمكنك استخدام أي ملف DWG أو DXF للاختبار).

## استيراد مساحات الأسماء

في مشروع Java الخاص بك، استورد الفئات الضرورية للعمل مع Aspose.CAD. تتيح لك هذه الاستيرادات الوصول إلى تحميل الصور، والكائنات الخاصة بـ CAD، وتعديل الأنماط.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadtables.CadStyleTableObject;
```

## دليل خطوة بخطوة لاستبدال الخط

### الخطوة 1: تحميل ملف DWG الخاص بك (load dwg file java)

أولاً، وجه الـ API إلى موقع ملف DWG (أو DXF) الخاص بك وقم بتحميله إلى كائن `CadImage`.

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";

String srcFile = dataDir + "conic_pyramid.dxf";
CadImage cadImage = (CadImage) Image.load(srcFile);
```

> **نصيحة احترافية:** إذا كنت تعمل مع ملفات DWG مباشرةً، استبدل امتداد `.dxf` بـ `.dwg` في المتغير `srcFile`.

### الخطوة 2: التكرار عبر جدول الأنماط وتعيين اسم الخط الأساسي

كل رسم CAD يحتوي على مجموعة من كائنات النمط. قم بالتكرار عبرها واستخدم طريقة `setPrimaryFontName` (نداء الـ API الذي **يحدد اسم الخط الأساسي**) لاستبدال الخط.

```java
for(Object style : cadImage.getStyles())
{
    // Set the font name
    ((com.aspose.cad.fileformats.cad.cadtables.CadStyleTableObject)style).setPrimaryFontName("Arial");
}
```

يمكنك تغيير `"Arial"` إلى أي خط مثبت على الجهاز الذي يشغل الشيفرة.

### الخطوة 3: حفظ الرسم المعدل

بعد تحديث الخط، اكتب التغييرات إلى ملف DWG جديد (أو استبدل الأصلي).

```java
cadImage.save(dataDir + "output.dwg", new DwgOptions());
```

الملف المحفوظ الآن يستخدم الخط الذي حددته، وأي تعليق نصي سيظهر بهذا الخط.

## المشكلات الشائعة والحلول

| المشكلة | الحل |
|---------|------|
| **الخط غير مطبق** | تحقق من أن الخط مثبت على نظام التشغيل المضيف وأن التهجئة مطابقة تمامًا. |
| **`Image.load` يرمي استثناء** | تأكد من صحة مسار الملف وأنه بصيغة DWG/DXF مدعومة. |
| **تباطؤ الأداء على الملفات الكبيرة** | عالج الملفات في خيط منفصل أو قم بتجميعها لتجنب حجب واجهة المستخدم. |

## الأسئلة المتكررة

**س: هل تؤثر طريقة `setPrimaryFontName` فقط على كائنات النص؟**  
ج: تقوم بتحديث الخط الأساسي لجدول الأنماط، مما يؤثر بدوره على جميع كائنات النص التي تشير إلى ذلك النمط.

**س: هل يمكنني استخدام خط مخصص غير مثبت على النظام؟**  
ج: يعتمد Aspose.CAD على سجل خطوط نظام التشغيل. لاستخدام خط مخصص، قم بتثبيته على الجهاز الذي يشغل الشيفرة.

**س: هل من الممكن تغيير الخط لطبقة واحدة فقط؟**  
ج: نعم، يمكنك تصفية الأنماط حسب اسم الطبقة قبل استدعاء `setPrimaryFontName`.

**س: ما هو إصدار Aspose.CAD المطلوب لملفات DWG 2022؟**  
ج: الإصدار الأخير (حتى عام 2025) يدعم بالكامل DWG 2022. تحقق دائمًا من ملاحظات الإصدار لدعم الصيغ المحددة.

**س: كيف أتعامل مع الترخيص في بيئة التطوير؟**  
ج: استخدم ترخيص تقييم مؤقت للاختبار. للإنتاج، قم بدمج ملف الترخيص المشتراة باستخدام `License.setLicense("Aspose.Total.Java.lic");`.

---

**آخر تحديث:** 2026-05-04  
**تم الاختبار باستخدام:** Aspose.CAD for Java 24.11  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}