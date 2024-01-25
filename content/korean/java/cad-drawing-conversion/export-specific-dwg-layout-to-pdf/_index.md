---
title: Java용 Aspose.CAD를 사용하여 특정 DWG 레이아웃을 PDF로 내보내기
linktitle: 특정 DWG 레이아웃을 PDF로 내보내기
second_title: Aspose.CAD 자바 API
description: Java용 Aspose.CAD를 사용하여 특정 DWG 레이아웃을 PDF로 내보내는 단계별 가이드를 살펴보세요. CAD 워크플로를 손쉽게 최적화하세요.
type: docs
weight: 14
url: /ko/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/
---
## 소개

CAD(Computer-Aided Design)의 역동적인 세계에서 Java용 Aspose.CAD는 DWG 도면을 조작하고 변환하는 강력한 도구로 등장합니다. 이 튜토리얼에서는 지정된 DWG 레이아웃을 PDF 파일로 내보내는 특정 시나리오를 살펴보겠습니다. 이 프로세스는 CAD 프로젝트의 정확성과 유연성을 보장합니다.

## 전제 조건

튜토리얼을 자세히 살펴보기 전에 다음 전제 조건이 충족되었는지 확인하세요.

- Java 개발 환경: 시스템에 기능적인 Java 개발 환경이 있는지 확인하십시오.
-  Aspose.CAD 라이브러리: Java용 Aspose.CAD 라이브러리를 다운로드하고 설정합니다. 도서관을 찾으실 수 있습니다[여기](https://releases.aspose.com/cad/java/).
- DWG 파일: 내보낼 DWG 파일을 준비합니다. 샘플 파일 "시각화"를 사용할 수 있습니다_-_이 튜토리얼에서는 conference_room.dwg'를 참조하세요.

## 네임스페이스 가져오기

## 1단계: 프로젝트 환경 설정

먼저 Java 프로젝트를 생성하고 Aspose.CAD 라이브러리가 올바르게 통합되었는지 확인하세요. 당신은 그것을 다운로드 할 수 있습니다[여기](https://releases.aspose.com/cad/java/).

## 2단계: 필요한 패키지 가져오기

Java 클래스에서 필수 Aspose.CAD 패키지를 가져와서 기능을 원활하게 활용하세요.

```java

import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## 3단계: DWG 파일 로드

DWG 파일의 경로를 지정하고 Aspose.CAD 이미지 개체에 로드합니다.

```java
String srcFile = dataDir + "visualization_-_conference_room.dwg";
Image image = Image.load(srcFile);
```

## 4단계: 래스터화 옵션 구성

 인스턴스 만들기`CadRasterizationOptions` 요구 사항에 따라 속성을 사용자 정의합니다.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
// 원하는 레이아웃 이름을 지정하세요.
rasterizationOptions.setLayouts(new String[] {"Layout1"});
```

## 5단계: PDF 내보내기 옵션 설정

 만들기`PdfOptions` 인스턴스를 설정하고`VectorRasterizationOptions` 속성을 이전에 구성한`CadRasterizationOptions`.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## 6단계: DWG를 PDF로 내보내기

수정된 이미지를 PDF 파일로 저장하면 변환 과정이 완료됩니다.

```java
image.save(dataDir + "ExportSpecificLayoutToPDF_out_.pdf", pdfOptions);
```

## 결론

Aspose.CAD for Java를 사용하여 특정 DWG 레이아웃을 PDF로 내보내는 기술을 익히면 CAD 작업 흐름을 크게 향상시킬 수 있습니다. 제공된 단계를 통해 이 기능을 프로젝트에 원활하게 통합하여 정확성과 효율성을 보장할 수 있습니다.

## FAQ

### Q1: Aspose.CAD for Java를 다른 Java 기반 CAD 라이브러리와 함께 사용할 수 있습니까?

Aspose.CAD for Java는 독립형 라이브러리이지만 확장된 기능을 위해 다른 Java 기반 라이브러리와 통합될 수 있습니다.

### Q2: Aspose.CAD에 대한 라이센스 옵션이 있습니까?

 예, 라이선스 옵션과 구매 세부정보를 살펴볼 수 있습니다.[여기](https://purchase.aspose.com/buy).

### Q3: Aspose.CAD의 임시 라이선스는 어떻게 얻을 수 있나요?

 방문하다[이 링크](https://purchase.aspose.com/temporary-license/) Aspose.CAD에 대한 임시 라이센스를 얻으려면.

### Q4: Aspose.CAD에 대한 지원은 어디서 찾을 수 있나요?

 질문이나 도움이 필요하면 다음을 방문하세요.[Aspose.CAD 포럼](https://forum.aspose.com/c/cad/19).

### Q5: Aspose.CAD에 대한 무료 평가판이 있습니까?

 예, 무료 평가판에 액세스할 수 있습니다[여기](https://releases.aspose.com/).