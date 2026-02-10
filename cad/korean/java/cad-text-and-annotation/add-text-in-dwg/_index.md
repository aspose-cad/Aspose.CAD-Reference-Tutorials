---
date: 2025-12-28
description: Aspose.CAD for Java를 사용하여 DWG에서 PDF를 생성하고, DWG를 PDF로 저장하며, DWG 도면에 텍스트를
  추가하는 방법을 단계별 가이드로 배워보세요.
linktitle: Add Text in DWG
second_title: Aspose.CAD Java API
title: Aspose.CAD for Java를 사용하여 DWG에서 PDF를 만들고 텍스트를 추가하기
url: /ko/java/cad-text-and-annotation/add-text-in-dwg/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DWG에서 PDF 생성 및 Aspose.CAD for Java를 사용한 텍스트 추가

## 소개

**DWG** 파일에서 **PDF를 생성**하면서 사용자 정의 텍스트를 삽입해야 한다면, 이곳이 바로 정답입니다. 이 튜토리얼에서는 DWG 도면을 로드하고, 텍스트 주석을 추가한 뒤, 최종적으로 Aspose.CAD for Java를 사용해 PDF로 저장하는 전체 과정을 단계별로 안내합니다. 튜토리얼을 마치면 **DWG를 PDF로 저장**하는 방법, 텍스트 높이를 커스터마이징하는 방법, 기본 주석을 추가하는 방법을 이해하게 됩니다.

## 빠른 답변
- **Java에서 DWG를 PDF로 변환할 수 있나요?** 예, Aspose.CAD for Java는 간단한 API를 제공합니다.  
- **프로덕션 사용에 라이선스가 필요합니까?** 상업용 라이선스가 필요합니다; 무료 체험판을 이용할 수 있습니다.  
- **DWG에 텍스트를 추가하는 메서드는?** `CadText` 객체를 사용하고 이를 모델 스페이스에 추가합니다.  
- **텍스트 높이를 설정할 수 있나요?** 물론입니다—`CadText` 인스턴스의 `setTextHeight()` 메서드를 사용합니다.  
- **출력은 벡터 기반인가요?** 래스터화 옵션을 `UseObjectColor` 로 설정하면 PDF가 고품질 벡터 데이터를 유지합니다.

## 사전 준비

튜토리얼을 진행하기 전에 다음 항목들을 준비하세요:

- Aspose.CAD for Java 라이브러리: [Aspose.CAD for Java 페이지](https://releases.aspose.com/cad/java/)에서 라이브러리를 다운로드하고 설치합니다.  
- Java Development Kit (JDK): 최신 JDK가 시스템에 설치되어 있는지 확인합니다.  
- DWG 도면: 텍스트를 추가하고자 하는 DWG 파일을 준비합니다.

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

이 단계들을 따라 하면 **DWG에서 PDF를 생성**하고, 사용자 정의 텍스트를 추가하며, 텍스트 높이를 제어할 수 있습니다—모두 몇 줄의 Java 코드만으로 가능합니다.

## DWG에 텍스트를 추가하고 PDF로 변환하는 이유

DWG 파일에 직접 텍스트를 추가하면 다음과 같은 장점이 있습니다:

- **디자인에 메모나 부품 번호** 등을 표시할 수 있습니다.  
- **인쇄 가능한 문서**를 만들 수 있으며, PDF는 읽기 전용이면서 널리 지원되는 포맷입니다.  
- **대량 CAD 라이브러리의 배치 처리**를 자동화하여 수동 편집 없이 작업을 수행할 수 있습니다.

## 일반적인 문제 및 팁

- **텍스트가 보이지 않나요?** X/Y 좌표가 도면 범위 내에 있는지, 레이어가 표시 상태인지 확인하세요.  
- **텍스트 높이가 잘못되었나요?** `setTextHeight()` 값을 조정하세요; 단위는 도면의 단위 시스템을 따릅니다.  
- **PDF가 래스터화된 것처럼 보이나요?** `CadDrawTypeMode.UseObjectColor` 를 설정해 벡터 정보를 유지하도록 합니다.  
- **대용량 파일에서 성능이 떨어지나요?** `pageHeight`/`pageWidth` 값을 필요에 따라만 늘리세요; 값이 클수록 메모리 사용량이 증가합니다.

## 자주 묻는 질문

**Q: Aspose.CAD가 모든 버전의 DWG 파일과 호환되나요?**  
A: Aspose.CAD는 다양한 DWG 버전을 지원하므로 폭넓은 CAD 소프트웨어와 호환됩니다.

**Q: 추가된 텍스트의 글꼴과 서식을 커스터마이즈할 수 있나요?**  
A: 예, Aspose.CAD를 사용하면 DWG 파일에 추가되는 텍스트의 글꼴, 스타일 및 기타 서식 옵션을 자유롭게 조정할 수 있습니다.

**Q: Aspose.CAD for Java의 무료 체험판을 이용할 수 있나요?**  
A: 예, [여기](https://releases.aspose.com/)에서 무료 체험판을 받아 기능을 확인할 수 있습니다.

**Q: Aspose.CAD for Java에 대한 자세한 문서는 어디서 찾을 수 있나요?**  
A: 자세한 정보와 예제는 [여기](https://reference.aspose.com/cad/java/)의 문서를 참고하세요.

**Q: Aspose.CAD 지원이나 도움을 받을 수 있는 방법은?**  
A: [Aspose.CAD 포럼](https://forum.aspose.com/c/cad/19)에서 커뮤니티와 소통하며 지원을 받을 수 있습니다.

---

**마지막 업데이트:** 2025-12-28  
**테스트 환경:** Aspose.CAD for Java 24.12  
**작성자:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}