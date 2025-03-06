---
title: DGN에서 PDF로 변환 가이드 - Java용 Aspose.CAD
linktitle: DGN V7 지원
second_title: Aspose.CAD 자바 API
description: Java용 Aspose.CAD를 사용하여 DGN 파일을 PDF로 쉽게 변환하세요. 원활한 통합과 효율적인 작업 흐름을 위한 단계별 가이드를 따르세요.
weight: 11
url: /ko/java/other-cad-operations/support-for-dgn-v7/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DGN에서 PDF로 변환 가이드 - Java용 Aspose.CAD

## 소개

역동적인 CAD(Computer-Aided Design) 세계에서는 DGN(Design) 파일을 PDF(Portable Document Format)로 효율적으로 변환하는 것이 중요한 요구 사항입니다. Aspose.CAD for Java는 원활한 통합과 강력한 기능을 제공하는 강력한 솔루션으로 등장합니다. 이 단계별 가이드는 원활하고 효율적인 작업 흐름을 보장하기 위해 Java용 Aspose.CAD를 사용하여 DGN 파일을 PDF로 내보내는 과정을 안내하는 것을 목표로 합니다.

## 전제 조건

튜토리얼을 시작하기 전에 다음 전제 조건이 충족되었는지 확인하세요.
-  Java 라이브러리용 Aspose.CAD: 다음에서 라이브러리를 다운로드하고 설치합니다.[Java 다운로드 페이지용 Aspose.CAD](https://releases.aspose.com/cad/java/).
- Java 개발 환경: 컴퓨터에 Java 개발 환경이 설정되어 있는지 확인하십시오.

## 패키지 가져오기

필요한 패키지를 Java 프로젝트로 가져오는 것부터 시작하세요.

## 1단계: 필요한 패키지 가져오기

Java 프로젝트에서 Aspose.CAD for Java에 필요한 패키지를 가져옵니다.
```java
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.cad.CadRasterizationOptions;
import com.aspose.cad.fileformats.cad.cadobjects.DgnImage;
import com.aspose.cad.imageoptions.PdfOptions;
import java.awt.Color;
```

## 2단계: 파일 경로 설정

입력 DGN 파일과 출력 PDF 파일의 경로를 정의합니다.

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "Nikon_D90_Camera.dgn";
String outFile  = dataDir + "Nikon_D90_Camera.pdf";
```

## 3단계: DGN 이미지 로드

Aspose.CAD 라이브러리를 사용하여 DGN 이미지를 로드합니다.

```java
DgnImage objImage = (DgnImage)Image.load(fileName);
```

## 4단계: PDF 내보내기 옵션 구성

페이지 크기, 자동 레이아웃 크기 조정, 배경색 및 내보낼 특정 레이아웃을 포함하여 PDF로 내보내기 위한 옵션을 설정합니다.

```java
PdfOptions options = new PdfOptions();
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
vectorOptions.setAutomaticLayoutsScaling(true);
vectorOptions.setBackgroundColor(Color.getBlack());
vectorOptions.setLayouts(new String[] { "1", "2", "3", "9" }); //4개(1,2,3 및 9)개의 보기만 내보냅니다.
options.setVectorRasterizationOptions(vectorOptions);
```

## 5단계: PDF 파일 저장

지정된 옵션을 사용하여 DGN 이미지를 PDF 파일로 저장합니다.

```java
objImage.save(outFile, options);
```

필요에 따라 파일 경로와 옵션을 조정하여 다른 DGN 파일에 대해 이 단계를 반복합니다.

## 결론

Java용 Aspose.CAD를 사용하면 DGN 파일을 PDF로 변환하는 과정이 간단해집니다. 이 가이드는 라이브러리를 Java 프로젝트에 원활하게 통합하여 효율적인 CAD 파일 변환을 촉진하는 지식을 제공합니다.

## FAQ

### Q1: Aspose.CAD for Java를 다른 CAD 파일 형식과 함께 사용할 수 있습니까?

A1: 예, Aspose.CAD는 다양한 CAD 형식을 지원하여 DGN을 넘어 PDF로 변환하는 다양한 기능을 제공합니다.

### Q2: Aspose.CAD for Java에 임시 라이선스를 사용할 수 있나요?

 A2: 예, 임시 라이센스를 얻을 수 있습니다.[여기](https://purchase.aspose.com/temporary-license/) 테스트 목적으로.

### Q3: Aspose.CAD for Java에 대한 지원을 요청하거나 질문하려면 어떻게 해야 합니까?

 A3: 다음을 방문하세요.[Aspose.CAD 포럼](https://forum.aspose.com/c/cad/19)지역사회와 연결하고 도움을 구합니다.

### Q4: DGN을 PDF로 변환할 때 어떤 레이아웃을 내보낼 수 있습니까?

 A4: 사용자 정의하여 내보낼 레이아웃을 지정할 수 있습니다.`setLayouts` 코드에 배열을 추가합니다.

### Q5: Aspose.CAD for Java에 대한 포괄적인 문서는 어디서 찾을 수 있나요?

 A5: 다음을 참조하세요.[Java 문서용 Aspose.CAD](https://reference.aspose.com/cad/java/) 자세한 정보를 보려면.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
