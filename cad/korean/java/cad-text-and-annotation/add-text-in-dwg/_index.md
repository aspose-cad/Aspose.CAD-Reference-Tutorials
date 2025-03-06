---
title: Java용 Aspose.CAD를 사용하여 DWG에 텍스트 추가
linktitle: DWG에 텍스트 추가
second_title: Aspose.CAD 자바 API
description: Java용 Aspose.CAD를 사용하여 DWG 도면을 손쉽게 향상하세요. 단계별 가이드를 통해 원활하게 텍스트를 추가하세요.
weight: 10
url: /ko/java/cad-text-and-annotation/add-text-in-dwg/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java용 Aspose.CAD를 사용하여 DWG에 텍스트 추가

## 소개

컴퓨터 지원 설계(CAD) 영역에서 Java용 Aspose.CAD는 DWG 도면을 조작하고 변환하는 강력한 도구로 돋보입니다. 편리한 기능 중 하나는 DWG 파일에 텍스트를 원활하게 추가하는 기능입니다. 이 튜토리얼에서는 Aspose.CAD for Java를 사용하여 DWG 도면에 텍스트를 추가하는 과정을 안내합니다.

## 전제 조건

튜토리얼을 시작하기 전에 다음 전제 조건이 충족되었는지 확인하세요.

-  Java 라이브러리용 Aspose.CAD: 다음에서 라이브러리를 다운로드하고 설치합니다.[Aspose.CAD for Java 페이지](https://releases.aspose.com/cad/java/).

- JDK(Java Development Kit): 시스템에 최신 JDK가 설치되어 있는지 확인하십시오.

- DWG 도면: 텍스트를 추가할 DWG 도면 파일을 준비합니다.

## 네임스페이스 가져오기

Java 코드에서 Aspose.CAD에 필요한 네임스페이스를 가져옵니다.

```java
import com.aspose.cad.Image;


import com.aspose.cad.fileformats.cad.CadDrawTypeMode;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.CadText;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

이제 제공된 코드 조각을 여러 단계로 나누어 보겠습니다.

## 1단계: 문서 디렉터리 및 DWG 파일 경로 설정

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String dwgPathToFile = dataDir + "SimpleEntites.dwg";
```

## 2단계: DWG 이미지 로드

```java
Image image = Image.load(dwgPathToFile);
```

## 3단계: CadText 객체 생성

```java
CadText cadText = new CadText();
cadText.setStyleType("Standard");
cadText.setDefaultValue("Some custom text");
cadText.setColorId(256);
cadText.setLayerName("0");
cadText.getFirstAlignment().setX(47.9);
cadText.getFirstAlignment().setY(5.56);
cadText.setTextHeight(0.8);
cadText.setScaleX(0);
```

## 4단계: CadImage에 텍스트 추가

```java
CadImage cadImage = ((CadImage)(image));
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(cadText);
```

## 5단계: PDF 옵션 설정

```java
PdfOptions pdfOptions = new PdfOptions();
```

## 6단계: CadRasterizationOptions 구성

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setDrawType(CadDrawTypeMode.UseObjectColor);
cadRasterizationOptions.setPageHeight(1600);
cadRasterizationOptions.setPageWidth(1600);
cadRasterizationOptions.setLayouts(new String[] {"Model"});
```

## 7단계: 수정된 DWG를 PDF로 저장

```java
image.save(dataDir + "SimpleEntites_generated.dwg.pdf", pdfOptions);
```

다음 단계를 수행하면 Aspose.CAD for Java를 사용하여 DWG 도면에 텍스트를 원활하게 추가할 수 있습니다.

## 결론

Java용 Aspose.CAD는 개발자가 DWG 도면을 프로그래밍 방식으로 향상하고 수정할 수 있도록 지원합니다. 이 튜토리얼에서는 DWG 파일에 텍스트를 추가하는 방법에 대한 명확한 단계별 가이드를 제공하여 Aspose.CAD의 단순성과 강력함을 보여주었습니다.

## FAQ

### Q1: Aspose.CAD는 모든 버전의 DWG 파일과 호환됩니까?

A1: Aspose.CAD는 다양한 버전의 DWG 파일을 지원하여 광범위한 CAD 소프트웨어와의 호환성을 보장합니다.

### Q2: 추가된 텍스트의 글꼴과 서식을 사용자 정의할 수 있나요?

A2: 예, Aspose.CAD를 사용하여 DWG 파일에 추가된 텍스트의 글꼴, 스타일 및 기타 서식 옵션을 사용자 정의할 수 있습니다.

### Q3: Aspose.CAD for Java에 대한 무료 평가판이 있습니까?

 A3: 예, 다음에서 무료 평가판을 받아 Aspose.CAD의 기능을 탐색할 수 있습니다.[여기](https://releases.aspose.com/).

### Q4: Aspose.CAD for Java에 대한 자세한 문서는 어디서 찾을 수 있나요?

 A4: 설명서를 참조하세요[여기](https://reference.aspose.com/cad/java/) 자세한 정보와 예시를 확인하세요.

### Q5: Aspose.CAD에 대한 지원을 받거나 도움을 받으려면 어떻게 해야 합니까?

A5: 다음을 방문하세요.[Aspose.CAD 포럼](https://forum.aspose.com/c/cad/19) 도움을 받고 지역 사회와 연결됩니다.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
