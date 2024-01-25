---
title: Java용 Aspose.CAD를 사용하여 DWG를 규정 준수 PDF로 변환
linktitle: DWG에서 규정 준수 PDF로
second_title: Aspose.CAD 자바 API
description: Java용 Aspose.CAD를 사용하여 DWG 도면을 PDF/A1a 및 PDF/A1b 호환 파일로 쉽게 변환합니다. 정확하고 쉽게 작업 흐름을 간소화하세요.
type: docs
weight: 11
url: /ko/java/cad-to-pdf-and-svg-export-options/dwg-to-compliance-pdf/
---
## 소개

끊임없이 진화하는 디지털 설계 세계에서 DWG 도면을 규정 준수 PDF 형식으로 변환해야 하는 필요성은 원활한 협업과 표준화된 문서화에 매우 중요합니다. Aspose.CAD for Java는 이 프로세스에서 효율성과 정확성을 제공하는 강력한 도구로 등장합니다. 이 튜토리얼에서는 Java용 Aspose.CAD를 활용하여 DWG 파일을 호환 PDF로 쉽게 변환하고 PDF/A1a 및 PDF/A1b 표준을 준수하는 방법을 살펴보겠습니다.

## 전제 조건

튜토리얼을 시작하기 전에 다음 전제 조건이 충족되었는지 확인하세요.

- Java 개발 환경: 시스템에 작동 중인 Java 개발 환경이 설정되어 있는지 확인하십시오.
-  Aspose.CAD 라이브러리: 다음에서 Java용 Aspose.CAD 라이브러리를 다운로드하고 설치합니다.[다운로드 링크](https://releases.aspose.com/cad/java/).
- 문서 디렉토리: DWG 도면을 저장할 디렉토리를 만듭니다.

## 네임스페이스 가져오기

Java 프로젝트에서 Aspose.CAD의 기능에 액세스하는 데 필요한 네임스페이스를 가져옵니다. Java 파일 시작 부분에 다음 줄을 추가합니다.

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfCompliance;
import com.aspose.cad.imageoptions.PdfDocumentOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## 1단계: 리소스 디렉터리 설정

DWG 도면이 저장되는 리소스 디렉토리의 경로를 정의합니다.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

## 2단계: DWG 파일 로드

Aspose.CAD 라이브러리를 사용하여 DWG 파일을 로드합니다.

```java
String srcFile = dataDir + "Bottom_plate.dwg";
Image objImage = Image.load(srcFile);
```

## 3단계: PDF 옵션 만들기

PdfOptions 인스턴스를 만들고 벡터 래스터화 옵션을 설정합니다.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(new CadRasterizationOptions());
```

## 4단계: 핵심 PDF 옵션 설정

규정 준수 표준(PDF/A1a 또는 PDF/A1b)을 지정하여 핵심 PDF 옵션을 설정합니다.

```java
pdfOptions.setCorePdfOptions(new PdfDocumentOptions());
pdfOptions.getCorePdfOptions().setCompliance(PdfCompliance.PdfA1a);
```

## 5단계: 규정 준수 A1a로 PDF 저장

A1a를 준수하여 PDF 파일을 저장하십시오.

```java
objImage.save(dataDir + "Saved1.pdf", pdfOptions);
```

## 6단계: 규정 준수를 A1b로 변경

규격을 PDF/A1b로 변경하고 PDF를 저장합니다.

```java
pdfOptions.getCorePdfOptions().setCompliance(PdfCompliance.PdfA1b);
objImage.save(dataDir + "Saved.pdf", pdfOptions);
```

변환하려는 각 DWG 파일에 대해 이 단계를 반복합니다.

## 결론

결론적으로, Aspose.CAD for Java는 DWG 파일을 규정 준수 PDF로 변환하기 위한 강력한 솔루션을 제공합니다. 이 단계별 가이드를 따르면 변환 프로세스를 간소화하고 문서가 업계 표준을 준수하는지 확인할 수 있습니다.

## FAQ

### Q1: Aspose.CAD는 모든 버전의 DWG 파일과 호환됩니까?

 A1: Aspose.CAD는 최신 버전을 포함하여 다양한 버전의 DWG 파일을 지원합니다. 다음을 참조하세요.[선적 서류 비치](https://reference.aspose.com/cad/java/) 자세한 호환성 정보를 확인하세요.

### Q2: Aspose.CAD를 사용하여 PDF 출력 설정을 사용자 정의할 수 있습니까?

A2: 물론이죠! Aspose.CAD는 사용자 정의를 위한 다양한 옵션을 제공하므로 PDF 출력을 특정 요구 사항에 맞게 조정할 수 있습니다.

### Q3: Aspose.CAD에 임시 라이선스를 사용할 수 있나요?

 A3: 예, 테스트 목적으로 임시 라이센스를 얻을 수 있습니다.[이 링크](https://purchase.aspose.com/temporary-license/).

### Q4: Aspose.CAD에 대한 지원을 구하거나 커뮤니티와 상호 작용할 수 있는 곳은 어디입니까?

 A4: 다음을 방문하세요.[Aspose.CAD 포럼](https://forum.aspose.com/c/cad/19) 커뮤니티 지원 및 토론을 위해.

### Q5: 구매하기 전에 Aspose.CAD를 무료로 사용해 볼 수 있나요?

 A5: 물론이죠! 다음에서 무료 평가판을 다운로드하세요.[여기](https://releases.aspose.com/) 결정을 내리기 전에 기능을 탐색합니다.