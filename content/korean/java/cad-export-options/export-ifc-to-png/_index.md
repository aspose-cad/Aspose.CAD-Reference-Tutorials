---
title: Java용 Aspose.CAD를 사용하여 IFC를 PNG로 내보내기
linktitle: IFC를 PNG로 내보내기
second_title: Aspose.CAD 자바 API
description: Java용 Aspose.CAD를 사용하여 IFC를 PNG로 손쉽게 변환하세요. 단계별 튜토리얼을 따라해보세요.
type: docs
weight: 18
url: /ko/java/cad-export-options/export-ifc-to-png/
---
## 소개

Java용 Aspose.CAD를 사용하여 IFC(Industry Foundation Classes)를 PNG로 내보내는 방법에 대한 단계별 튜토리얼에 오신 것을 환영합니다. Aspose.CAD는 IFC 형식을 포함하여 CAD 파일 작업을 위한 광범위한 기능을 제공하는 강력한 Java 라이브러리입니다. 이 튜토리얼에서는 각 단계에 대한 자세한 설명과 함께 IFC 파일을 PNG 이미지로 변환하는 과정을 안내합니다.

## 전제 조건

시작하기 전에 다음 전제 조건이 충족되었는지 확인하세요.

-  Aspose.CAD 라이브러리: 다음에서 Java용 Aspose.CAD 라이브러리를 다운로드하고 설치합니다.[다운로드 링크](https://releases.aspose.com/cad/java/).

- 문서 디렉터리: 시스템에서 IFC 파일이 있는 디렉터리를 준비합니다.

## 네임스페이스 가져오기

Java 프로젝트에서 아래와 같이 필요한 네임스페이스를 가져옵니다.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.ifc.IfcImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

## 1단계: IFC 파일 로드

```java
String dataDir = "Your Document Directory" + "ExportingIFC/";
String fileName = dataDir + "example.ifc";
IfcImage cadImage = (IfcImage)Image.load(fileName);
```

이 단계에는 Aspose.CAD를 사용하여 IFC 파일을 로드하는 작업이 포함됩니다.

## 2단계: 벡터 옵션 설정

```java
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
```

페이지 너비와 높이를 지정하여 래스터화를 위한 벡터 옵션을 구성합니다.

## 3단계: PNG 옵션 설정

```java
PngOptions pngOptions = new PngOptions();
pngOptions.setVectorRasterizationOptions(vectorOptions);
```

벡터 래스터화 옵션을 포함한 PNG 옵션을 설정합니다.

## 4단계: PNG로 저장

```java
String outPath = dataDir + "example.png";
cadImage.save(outPath, pngOptions);
```

처리된 이미지를 PNG 형식으로 저장합니다.

## 결론

축하해요! Java용 Aspose.CAD를 사용하여 IFC 파일을 PNG로 성공적으로 변환했습니다. 이 튜토리얼에서는 이 기능을 프로젝트에 원활하게 통합할 수 있도록 포괄적인 가이드를 제공했습니다.

## FAQ

### Q1: Aspose.CAD는 모든 버전의 IFC 파일과 호환됩니까?

 A1: Aspose.CAD는 다양한 버전의 IFC 파일을 지원합니다. 다음을 참조하세요.[선적 서류 비치](https://reference.aspose.com/cad/java/) 호환성 세부정보를 확인하세요.

### Q2: 래스터화 옵션을 추가로 사용자 정의할 수 있나요?

 A2: 물론이죠! 탐색[선적 서류 비치](https://reference.aspose.com/cad/java/) 고급 사용자 정의 옵션.

### Q3: 평가판을 사용할 수 있나요?

A3: 예, 무료 평가판에 액세스할 수 있습니다.[여기](https://releases.aspose.com/).

### Q4: Aspose.CAD에 대한 임시 라이선스를 어떻게 얻을 수 있나요?

 A4: 임시 라이센스를 받으십시오.[이 링크](https://purchase.aspose.com/temporary-license/).

### Q5: 어디에서 도움을 구하거나 문제를 논의할 수 있나요?

A5: 다음을 방문하세요.[Aspose.CAD 포럼](https://forum.aspose.com/c/cad/19) 지역 사회 지원을 위해.
