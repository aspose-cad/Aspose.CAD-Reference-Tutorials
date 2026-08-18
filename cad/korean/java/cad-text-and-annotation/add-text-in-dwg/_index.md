---
date: 2026-02-28
description: Aspose.CAD for Java를 사용하여 DWG에서 PDF를 생성하고, DWG를 PDF로 저장하며, DWG 도면에 텍스트를
  추가하는 방법을 단계별 가이드로 배워보세요.
linktitle: Add Text in DWG
second_title: Aspose.CAD Java API
title: Aspose.CAD for Java를 사용하여 DWG에서 PDF를 생성하고 텍스트를 추가하기
url: /ko/java/cad-text-and-annotation/add-text-in-dwg/
weight: 10
---

 "**마지막 업데이트:** 2026-02-28". Keep bold.

"**Tested With:** Aspose.CAD for Java 24.12" -> "**테스트 환경:** Aspose.CAD for Java 24.12"

"**Author:** Aspose" -> "**작성자:** Aspose"

Then closing shortcodes.

Finally backtop button shortcode.

We must ensure no extra spaces or missing elements.

Let's craft final output.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DWG에서 PDF 생성 및 텍스트 추가 - Aspose.CAD for Java 사용

## 소개

DWG 파일에서 **PDF를 생성**하고 사용자 정의 텍스트를 삽입해야 한다면, 올바른 곳에 오셨습니다. 이 튜토리얼에서는 전체 과정을 단계별로 살펴봅니다—DWG 도면을 로드하고, 텍스트 주석을 추가한 뒤, 마지막으로 Aspose.CAD for Java를 사용해 결과를 PDF로 저장합니다. 끝까지 진행하면 **DWG를 PDF로 저장**하는 방법, 텍스트 높이 맞춤, 기본 주석 추가 등을 이해하게 됩니다.

## 빠른 답변
- **Java에서 DWG를 PDF로 변환할 수 있나요?** 예, Aspose.CAD for Java는 간단한 API를 제공합니다.  
- **프로덕션 사용에 라이선스가 필요합니까?** 상업용 라이선스가 필요하며, 무료 체험판을 사용할 수 있습니다.  
- **DWG에 텍스트를 추가하는 방법은?** `CadText` 객체를 사용하고 이를 모델 스페이스에 추가합니다.  
- **텍스트 높이를 설정할 수 있나요?** 물론입니다—`CadText` 인스턴스에서 `setTextHeight()`를 사용합니다.  
- **출력이 벡터 기반인가요?** 래스터화 옵션을 `UseObjectColor`로 설정하면 PDF가 고품질 벡터 데이터를 유지합니다.

## “DWG에서 PDF 생성”이란 무엇인가요?
DWG 도면에서 PDF를 생성한다는 것은 원본 CAD 형식을 널리 지원되는 읽기 전용 문서로 변환하면서 원래의 기하학을 보존하는 것을 의미합니다. 이 변환은 CAD 소프트웨어가 없는 이해관계자와 설계를 공유해야 할 때 필수적입니다.

## 왜 Aspose.CAD for Java를 사용해 DWG를 PDF로 변환해야 할까요?
Aspose.CAD는 외부 CAD 설치가 필요 없는 순수 Java 솔루션을 제공합니다. **DWG를 PDF로 변환**을 지원하고, 벡터 정확성을 유지하며, 변환 전에 텍스트, 치수 또는 사용자 정의 그래픽과 같은 주석을 프로그래밍 방식으로 추가할 수 있습니다.

## 사전 요구 사항

튜토리얼을 진행하기 전에 다음 요구 사항을 충족했는지 확인하세요:

- Aspose.CAD for Java 라이브러리: [Aspose.CAD for Java 페이지](https://releases.aspose.com/cad/java/)에서 라이브러리를 다운로드하고 설치합니다.
- Java Development Kit (JDK): 시스템에 최신 JDK가 설치되어 있는지 확인합니다.
- DWG 도면: 텍스트를 추가하려는 DWG 파일을 준비합니다.

## 네임스페이스 가져오기

Java 코드에서 Aspose.CAD에 필요한 네임스페이스를 가져옵니다:

```java
import com.aspose.cad.Image;


import com.aspose.cad.fileformats.cad.CadDrawTypeMode;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.CadText;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

이제 제공된 코드 스니펫을 여러 단계로 나누어 살펴보겠습니다:

## 단계 1: 문서 디렉터리 및 DWG 파일 경로 설정

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String dwgPathToFile = dataDir + "SimpleEntites.dwg";
```

## 단계 2: DWG 이미지 로드

```java
Image image = Image.load(dwgPathToFile);
```

## 단계 3: CadText 객체 생성 (DWG에 텍스트 추가)

```java
CadText cadText = new CadText();
cadText.setStyleType("Standard");
cadText.setDefaultValue("Some custom text");
cadText.setColorId(256);
cadText.setLayerName("0");
cadText.getFirstAlignment().setX(47.9);
cadText.getFirstAlignment().setY(5.56);
cadText.setTextHeight(0.8);          // set text height in DWG units
cadText.setScaleX(0);
```

## 단계 4: CadImage에 텍스트 추가 (주석 삽입)

```java
CadImage cadImage = ((CadImage)(image));
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(cadText);
```

## 단계 5: PDF 옵션 설정 (DWG에서 PDF 생성 준비)

```java
PdfOptions pdfOptions = new PdfOptions();
```

## 단계 6: CadRasterizationOptions 구성 (PDF 렌더링 제어)

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setDrawType(CadDrawTypeMode.UseObjectColor);
cadRasterizationOptions.setPageHeight(1600);
cadRasterizationOptions.setPageWidth(1600);
cadRasterizationOptions.setLayouts(new String[] {"Model"});
```

## 단계 7: 수정된 DWG를 PDF로 저장 (dwg to pdf java)

```java
image.save(dataDir + "SimpleEntites_generated.dwg.pdf", pdfOptions);
```

이 단계들을 따라 하면 **DWG에서 PDF를 생성**, 사용자 정의 텍스트 추가, 텍스트 높이 제어 등을 몇 줄의 Java 코드만으로 구현할 수 있습니다.

## 대규모 환경에서 Java로 DWG를 PDF로 변환하려면?
**DWG PDF** 파일을 일괄 변환해야 한다면, 위 코드를 폴더에 있는 DWG 도면을 순회하는 루프에 넣으세요. 메모리 사용량을 낮게 유지하려면 `pageHeight`/`pageWidth`를 필요할 때만 조정하고, 각 파일에 대해 동일한 `PdfOptions` 인스턴스를 재사용하면 성능이 향상됩니다.

## 일반적인 문제 및 팁

- **텍스트가 보이지 않나요?** X/Y 좌표가 도면 범위 내에 있는지, 레이어가 표시되는지 확인하세요.  
- **텍스트 높이가 잘못되었나요?** `setTextHeight()` 값을 조정하세요; 값은 도면의 단위 시스템을 기준으로 합니다.  
- **PDF가 래스터화된 것처럼 보이나요?** 벡터 정보를 유지하려면 `CadDrawTypeMode.UseObjectColor`가 설정되어 있는지 확인하세요.  
- **대용량 파일에서 성능이 떨어지나요?** `pageHeight`/`pageWidth`를 필요한 경우에만 늘리고, 큰 값은 메모리를 많이 차지한다는 점을 유념하세요.

## 자주 묻는 질문

**Q: Aspose.CAD가 모든 버전의 DWG 파일과 호환되나요?**  
A: Aspose.CAD는 다양한 버전의 DWG 파일을 지원하여 광범위한 CAD 소프트웨어와의 호환성을 보장합니다.

**Q: 추가된 텍스트의 글꼴과 서식을 사용자 정의할 수 있나요?**  
A: 예, Aspose.CAD를 사용하면 DWG 파일에 추가된 텍스트의 글꼴, 스타일 및 기타 서식 옵션을 자유롭게 설정할 수 있습니다.

**Q: Aspose.CAD for Java에 대한 무료 체험판이 있나요?**  
A: 예, [여기](https://releases.aspose.com/)에서 무료 체험판을 받아 기능을 살펴볼 수 있습니다.

**Q: Aspose.CAD for Java에 대한 자세한 문서는 어디서 찾을 수 있나요?**  
A: 자세한 정보와 예제는 [여기](https://reference.aspose.com/cad/java/)의 문서를 참고하세요.

**Q: Aspose.CAD 지원을 받거나 도움을 받을 수 있는 방법은?**  
A: [Aspose.CAD 포럼](https://forum.aspose.com/c/cad/19)에서 커뮤니티와 소통하며 지원을 받을 수 있습니다.

---

**마지막 업데이트:** 2026-02-28  
**테스트 환경:** Aspose.CAD for Java 24.12  
**작성자:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}