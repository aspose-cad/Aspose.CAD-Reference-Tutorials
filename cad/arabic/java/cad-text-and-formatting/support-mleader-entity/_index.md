---
date: 2026-05-20
description: تعلم كيفية دعم كيان MLeader في ملفات DWG باستخدام Aspose.CAD for Java
  – دليل خطوة بخطوة، مقتطفات كود، وأفضل الممارسات.
keywords:
- support mleader entity java
- Aspose.CAD DWG
- Java CAD manipulation
linktitle: دعم كيان MLeader لتنسيق DWG باستخدام Java
schemas:
- author: Aspose
  dateModified: '2026-05-20'
  description: Learn how to support mleader entity java in DWG files with Aspose.CAD
    for Java – step‑by‑step guide, code snippets, and best practices.
  headline: Support MLeader Entity Java – Working with DWG Format using Aspose.CAD
  type: TechArticle
- questions:
  - answer: Yes, Aspose.CAD supports over 50 CAD formats, including DXF, DGN, and
      SVG, enabling cross‑format workflows.
    question: Can I use Aspose.CAD for Java with other CAD formats?
  - answer: Refer to the [documentation](https://reference.aspose.com/cad/java/) for
      comprehensive API references and code samples.
    question: Where can I find detailed documentation for Aspose.CAD for Java?
  - answer: Yes, explore the functionalities firsthand with the [free trial](https://releases.aspose.com/).
    question: Is there a free trial available?
  - answer: Obtain a temporary license through [this link](https://purchase.aspose.com/temporary-license/).
    question: How can I obtain a temporary license for testing?
  - answer: Visit the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) to connect
      with the community and get help.
    question: Where can I seek community support and assistance?
  type: FAQPage
second_title: Aspose.CAD Java API
title: دعم كيان MLeader في Java – العمل مع تنسيق DWG باستخدام Aspose.CAD
url: /ar/java/cad-text-and-formatting/support-mleader-entity/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# دعم كيان MLeader في Java – العمل مع تنسيق DWG باستخدام Aspose.CAD

## مقدمة

في هذا الدرس ستتعلم كيفية **support mleader entity java** عند العمل مع ملفات DWG. Aspose.CAD for Java هي مكتبة يمكنها قراءة وتحرير وكتابة أكثر من **50 CAD formats**، مما يجعلها خيارًا موثوقًا لمعالجة CAD على مستوى المؤسسات. سنستعرض كل خطوة، من تحميل ملف DWG إلى التحقق من كل سمة من سمات MLeader، حتى تتمكن من دمج دعم MLeader الكامل في تطبيقات Java الخاصة بك.

## إجابات سريعة
- **ما يعني “support mleader entity java”؟** هذا يعني تمكين كود Java الخاص بك من قراءة وتعديل وكتابة كائنات MLeader داخل ملفات DWG باستخدام Aspose.CAD.  
- **ما المكتبة التي تتعامل مع كيانات DWG MLeader؟** Aspose.CAD for Java provides a complete API for DWG MLeader manipulation.  
- **هل أحتاج إلى ترخيص للإنتاج؟** نعم – يلزم الحصول على ترخيص تجاري للاستخدام في الإنتاج؛ يتوفر نسخة تجريبية مجانية للتقييم.  
- **هل يمكنني معالجة ملفات DWG الكبيرة؟** Aspose.CAD يمكنه التعامل مع ملفات DWG ذات مئات الصفحات دون تحميل المستند بالكامل في الذاكرة.  
- **ما نسخة Java المطلوبة؟** Java 8 أو أعلى مدعومة.

## ما هو support mleader entity java؟
*Support mleader entity java* تشير إلى قدرة تطبيق Java على قراءة وتحرير وكتابة كائنات **MLeader** (متعدد القادة) داخل رسومات DWG باستخدام Aspose.CAD API. هذا يتيح تحكمًا دقيقًا في خطوط القائد، نص التعليق، والمرجعيات المرتبطة بالكتل.

## لماذا تستخدم Aspose.CAD for Java؟
Aspose.CAD يدعم **50+ input and output formats** (بما في ذلك DWG وDXF وDGN وSVG) ويعالج الملفات حتى **2 GB** دون الحاجة إلى تثبيت AutoCAD الأصلي. نموذج البث الفعال في الذاكرة يقلل من استهلاك المعالج بنسبة تصل إلى **30 %** مقارنة بالعديد من المنافسين، مما يجعله مثاليًا لأتمتة CAD على الخادم.

## المتطلبات المسبقة

قبل أن نبدأ، تأكد من أن لديك:

1. **بيئة تطوير Java** – JDK 8 أو أحدث، مع IDE المفضلة لديك (IntelliJ، Eclipse، إلخ).  
2. **مكتبة Aspose.CAD** – قم بتنزيل وتثبيت مكتبة Aspose.CAD للـ Java من [download link](https://releases.aspose.com/cad/java/).

## استيراد المساحات الاسمية

مساحة الأسماء `com.aspose.cad` تحتوي على جميع الفئات التي ستحتاجها. أضف الاستيرادات التالية في أعلى ملف مصدر Java الخاص بك:

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.CadMLeader;
import com.aspose.cad.fileformats.cad.cadobjects.CadMLeaderContextData;
import com.aspose.cad.fileformats.cad.cadobjects.CadMLeaderLine;
import com.aspose.cad.fileformats.cad.cadobjects.CadMLeaderNode;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;

```

الآن دعنا نستعرض خطوات التنفيذ.

## كيفية تحميل ملف DWG والوصول إلى CadImage؟

قم بتحميل ملف DWG بسطر واحد من الشيفرة واحصل على كائن `CadImage` الذي يمثل الرسم بالكامل في الذاكرة. هذا الكائن يمنحك الوصول إلى جميع الكيانات، بما في ذلك MLeaders، دون الحاجة إلى خطوة تحليل منفصلة.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String file = dataDir + "Multileaders.dwg";
Image image = Image.load(file);
CadImage cadImage = (CadImage) image;
```

## كيفية التحقق من كيانات MLeader؟

`MLeader` يمثل كائن تعليقات متعددة القادة في رسم DWG.  
بعد تحميل الصورة، قم بالتكرار عبر مجموعة الكيانات في `CadImage` وفلترة الكائنات من النوع `MLeader`. يمكن بعد ذلك فحص كل مثال من `MLeader` للسمات المطلوبة مثل النمط، خطوط القائد، ونص التعليق.

```java
Assert.areNotEqual(cadImage.getEntities().length, 0);
CadMLeader cadMLeader = (CadMLeader) cadImage.getEntities()[2];
```

## كيفية التحقق من نمط MLeader والسمات؟

فئة `MLeaderStyle` تعرف الخصائص البصرية مثل حجم رأس السهم، نوع الخط، ونمط النص. من خلال استرجاع كائن النمط من كل `MLeader`، يمكنك التأكد من أنه يتطابق مع معايير التصميم الخاصة بك.

```java
Assert.areEqual(cadMLeader.getStyleDescription(), "Standard");
Assert.areEqual(cadMLeader.getLeaderStyleId(), "12E");
Assert.areEqual(cadMLeader.getArrowHeadId1(), "639");
Assert.areEqual(cadMLeader.getLeaderLineTypeID(), "14");
```

## كيفية الوصول إلى بيانات سياق MLeader؟

`getContextData()` تُرجع كائن بيانات السياق الذي يحتوي على الهندسة ومعلومات التثبيت لـ MLeader.  
بيانات سياق MLeader تشمل هندسة خط القائد، نقاط التثبيت، والمرجع الكتلي الذي يشير إليه القائد. استخدم طريقة `getContextData()` على كائن `MLeader` لاسترجاع هذه المعلومات لمزيد من المعالجة.

```java
CadMLeaderContextData context = cadMLeader.getContextData();
```

## كيفية التحقق من سمات السياق؟

تحقق من كل سمة سياق (مثل `AttachmentPoint`، `LeaderLineLength`) مقابل النطاقات المتوقعة. هذا يضمن أن التعليق سيظهر بشكل صحيح في عارضات CAD اللاحقة.

```java
Assert.areEqual(context.getArrowHeadSize(), 30.0, 0.1);
Assert.areEqual(context.getBasePoint().getX(), 481, 1);
Assert.areEqual(context.getContentScale(), 1.0, 0.01);
Assert.areEqual(context.getDefaultText().getValue(), "This is multileader with huge text\\P{\\H1.5x;6666666666666666666666666666\\P}bbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbb");
Assert.areEqual(context.hasMText(), true);
```

## كيفية الوصول إلى عقدة MLeader وخط القائد؟

`MLeaderNode` تمثل نقطة بدء خط القائد. من خلال الوصول إلى إحداثيات العقدة، يمكنك تعديل اتجاه القائد أو إعادة وضع التعليق حسب الحاجة.

```java
CadMLeaderNode mleaderNode = context.getLeaderNode();
Assert.areEqual(mleaderNode.getLastLeaderLinePoint().getX(), 473, 1);

CadMLeaderLine leaderLine = mleaderNode.getLeaderLine();
Assert.areEqual(leaderLine.getBreakEndPoint().toString(), null);
Assert.areEqual(Integer.toString(leaderLine.getBreakPointIndex().getValue()), Integer.toString(0));
Assert.areEqual(leaderLine.getBreakStartPoint().toString(), null);
Assert.areEqual(Integer.toString(leaderLine.getLeaderLineIndex().getValue()), Integer.toString(0));
Assert.areEqual(Integer.toString(leaderLine.getLeaderPoints().size()), Integer.toString(4));
```

## كيفية التحقق من سمات MLeader الإضافية؟

`getCustomData()` يوفر مجموعة من حقول البيانات المخصصة المرفقة بـ MLeader.  
بخلاف الهندسة الأساسية، قد تحتوي MLeaders على بيانات مخصصة مثل الارتفاع، الدوران، أو الحقول المعرفة من قبل المستخدم. تحقق من هذه السمات باستخدام مجموعة `getCustomData()` للحفاظ على سلامة البيانات.

```java
Assert.areEqual(Integer.toString(mleaderNode.getBranchIndex()), Integer.toString(0));
Assert.areEqual(mleaderNode.getDogLegLength(), 8.0, 0.1);
Assert.areEqual(context.hasMText(), true);
```

## كيفية التحقق من سمات النص؟

نص التعليق المرفق بـ MLeader مخزن في كائن `TextStyle`. تحقق من الخصائص مثل اسم الخط، الارتفاع، واللون لضمان التناسق عبر الرسم.

```java
Assert.areEqual(context.getTextAttachmentType().getValue(), (short) 1);
Assert.areEqual(context.getTextBackgroundColor().getValue(), 18);
Assert.areEqual(context.getTextHeight(), 20.0, 0.1);
Assert.areEqual(context.getTextStyleID().getValue(), "11");
Assert.areEqual(context.getTextRotation().getValue(), 0.0, 0.01);
```

## كيفية التعامل مع سمات MLeader الإضافية؟

`getExtendedData()` تُرجع حقول البيانات الموسعة لـ MLeader، مثل نوع خط القائد ومقياس التعليق.  
بعض ملفات DWG تشمل خصائص MLeader موسعة مثل `LeaderLineType` أو `AnnotationScale`. استخدم طريقة `getExtendedData()` لقراءة هذه القيم وتعديلها إذا لزم الأمر.

```java
Assert.areEqual(cadMLeader.getArrowHeadId1(), "639");
Assert.areEqual(cadMLeader.getLeaderType(), 1);
Assert.areEqual(cadMLeader.getBlockContentColor(), 0);
Assert.areEqual(cadMLeader.getLeaderLineColor(), 0);
Assert.areEqual(cadMLeader.getTextHeight(), 1.0, 0.01);
```

## المشكلات الشائعة والحلول

| المشكلة | السبب | الحل |
|-------|-------|----------|
| **NullPointerException عند الوصول إلى MLeader** | الرسم لا يحتوي على أي كائنات MLeader. | تحقق من `image.getEntities().size()` قبل التكرار، واحمِ نفسك من المجموعات الفارغة. |
| **تنسيق النص غير صحيح** | تم استخدام `TextStyle` الافتراضي بدلاً من النمط المقصود. | قم بتعيين `TextStyle` صراحةً على كل `MLeader` بعد تحميل الصورة. |
| **تباطؤ الأداء على ملفات DWG الكبيرة** | تحميل الملف بالكامل في الذاكرة. | استخدم `CadImage.load(InputStream, LoadOptions)` مع `LoadOptions.setMemorySavingMode(true)`. |

## الأسئلة المتكررة

**س: هل يمكنني استخدام Aspose.CAD for Java مع تنسيقات CAD أخرى؟**  
ج: نعم، Aspose.CAD يدعم أكثر من 50 تنسيق CAD، بما في ذلك DXF وDGN وSVG، مما يتيح تدفقات عمل عبر تنسيقات متعددة.

**س: أين يمكنني العثور على وثائق مفصلة لـ Aspose.CAD for Java؟**  
ج: راجع [documentation](https://reference.aspose.com/cad/java/) للحصول على مراجع API شاملة وعينات من الشيفرة.

**س: هل تتوفر نسخة تجريبية مجانية؟**  
ج: نعم، استكشف الوظائف مباشرةً عبر [free trial](https://releases.aspose.com/).

**س: كيف يمكنني الحصول على ترخيص مؤقت للاختبار؟**  
ج: احصل على ترخيص مؤقت عبر [this link](https://purchase.aspose.com/temporary-license/).

**س: أين يمكنني طلب الدعم والمساعدة من المجتمع؟**  
ج: زر [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) للتواصل مع المجتمع والحصول على المساعدة.

---

**آخر تحديث:** 2026-05-20  
**تم الاختبار مع:** Aspose.CAD for Java 24.9 (latest at time of writing)  
**المؤلف:** Aspose  

{{< blocks/products/products-backtop-button >}}

## دروس ذات صلة

- [إنشاء PDF من DWG وإضافة نص باستخدام Aspose.CAD for Java](/cad/java/cad-text-and-annotation/add-text-in-dwg/)
- [قراءة DWG بـ Java – البحث عن نص في DWG باستخدام Aspose.CAD for Java](/cad/java/cad-text-and-formatting/search-text-in-dwg/)
- [إضافة خصائص مخصصة لملفات DWG باستخدام Aspose.CAD for Java](/cad/java/additional-features/add-custom-properties/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}