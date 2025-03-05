---
title: Java용 Aspose.CAD를 사용하여 손쉽게 DGN을 AutoCAD PDF로 내보내기
linktitle: AutoCAD 형식의 DGN을 PDF로 내보내기
second_title: Aspose.CAD 자바 API
description: Java용 Aspose.CAD를 사용하여 DGN 파일을 PDF의 AutoCAD 형식으로 내보내는 방법에 대한 단계별 가이드를 살펴보세요. Java 애플리케이션의 CAD 처리 기능을 손쉽게 향상시키십시오.
type: docs
weight: 12
url: /ko/java/dgn-export-options/exporting-dgn-to-pdf/
---
## 소개

Java용 Aspose.CAD를 사용하여 AutoCAD 형식의 DGN 파일을 PDF로 내보내는 방법에 대한 포괄적인 튜토리얼에 오신 것을 환영합니다. CAD 파일을 처리하기 위해 Java 애플리케이션의 기능을 향상시키려는 경우 Aspose.CAD가 탁월한 선택입니다. 이 튜토리얼에서는 DGN 파일을 내보내는 과정을 단계별로 안내합니다.


## 전제 조건
튜토리얼을 시작하기 전에 다음 전제 조건이 충족되었는지 확인하세요.
-  Aspose.CAD 라이브러리: Java용 Aspose.CAD 라이브러리가 설치되어 있는지 확인하세요. 당신은 그것을 다운로드 할 수 있습니다[여기](https://releases.aspose.com/cad/java/).
- 문서 디렉터리: 입력 및 출력 파일이 저장될 문서 디렉터리를 설정합니다.

## 패키지 가져오기

Java 프로젝트에서 Aspose.CAD 기능에 액세스하는 데 필요한 패키지를 가져옵니다.

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

이제 예제 코드를 여러 단계로 나누어 보겠습니다.

## 1단계: 파일 경로 정의

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "Nikon_D90_Camera.dgn";
String outFile  = dataDir + "Nikon_D90_Camera.pdf";
```

"Your Document Directory"를 파일이 있는 실제 경로로 바꾸십시오.

## 2단계: DGN 이미지 로드

```java
DgnImage objImage = (DgnImage) Image.load(fileName);
```

Aspose.CAD를 사용하여 DGN 파일을 로드합니다.

## 3단계: PDF 내보내기 옵션 설정

```java
PdfOptions options = new PdfOptions();
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
vectorOptions.setAutomaticLayoutsScaling(true);
vectorOptions.setLayouts(new String[] { "1", "2", "3", "9" }); // 특정 보기 내보내기
options.setVectorRasterizationOptions(vectorOptions);
```

페이지 크기 및 레이아웃 기본 설정을 포함한 PDF 내보내기 옵션을 정의합니다.

## 4단계: PDF 파일 저장

```java
objImage.save(outFile, options);
```

내보낸 PDF 파일을 저장합니다.

변환하려는 추가 DGN 파일에 대해 이 단계를 반복합니다. 축하해요! Java용 Aspose.CAD를 사용하여 DGN 파일을 PDF의 AutoCAD 형식으로 성공적으로 내보냈습니다.

## 결론

이 튜토리얼에서는 Java용 Aspose.CAD를 활용하여 애플리케이션의 CAD 파일 처리 기능을 향상시키는 방법을 살펴보았습니다. 따라하기 쉬운 단계와 코드 예제를 통해 이제 DGN 파일을 PDF의 AutoCAD 형식으로 원활하게 내보낼 수 있습니다.

## FAQ

### Q1: Aspose.CAD는 모든 CAD 파일 형식과 호환됩니까?

A1: 예, Aspose.CAD는 광범위한 CAD 형식을 지원하므로 다양한 파일 형식을 처리하는 데 있어 다양성을 보장합니다.

### Q2: PDF 내보내기 설정을 사용자 정의할 수 있습니까?

A2: 물론이죠. 튜토리얼에 표시된 대로 요구 사항에 맞게 페이지 크기 및 레이아웃과 같은 옵션을 조정할 수 있습니다.

### Q3: 추가 지원이나 도움은 어디서 찾을 수 있나요?

 A3: 다음을 방문하세요.[Aspose.CAD 포럼](https://forum.aspose.com/c/cad/19) 커뮤니티 지원 및 토론을 위해.

### Q4: 무료 평가판이 제공됩니까?

 A4: 예, 무료 평가판에 액세스할 수 있습니다.[여기](https://releases.aspose.com/).

### Q5: 임시 라이센스는 어떻게 얻을 수 있나요?

 A5: 임시 라이센스 받기[여기](https://purchase.aspose.com/temporary-license/).