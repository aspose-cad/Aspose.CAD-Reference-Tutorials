---
title: Aspose.CAD for Java를 사용하여 CAD 레이아웃을 PDF로 내보내기
linktitle: CAD 레이아웃을 PDF로 내보내기
second_title: Aspose.CAD 자바 API
description: CAD 레이아웃을 PDF로 쉽게 내보내려면 Java용 Aspose.CAD를 탐색하세요. 효율적이고 안정적이며 개발자 친화적입니다.
weight: 11
url: /ko/java/cad-export-options/export-cad-layouts-to-pdf/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD for Java를 사용하여 CAD 레이아웃을 PDF로 내보내기

## 소개

끊임없이 진화하는 CAD(컴퓨터 지원 설계) 분야에서 Java용 Aspose.CAD는 CAD 파일을 조작하고 변환하는 강력한 도구로 돋보입니다. 이 튜토리얼에서는 Aspose.CAD for Java를 사용하여 CAD 레이아웃을 PDF로 내보내는 과정을 안내합니다. 숙련된 개발자이거나 CAD 세계에 뛰어든 이 단계별 가이드는 이 다용도 Java 라이브러리의 잠재력을 최대한 활용하는 데 도움이 될 것입니다.

## 전제 조건

튜토리얼을 시작하기 전에 다음 전제 조건이 충족되었는지 확인하세요.

-  Aspose.CAD for Java: 라이브러리가 설치되어 있는지 확인하세요. Aspose 웹사이트에서 다운로드할 수 있습니다.[여기](https://releases.aspose.com/cad/java/).

- Java 개발 환경: 컴퓨터에 Java 개발 환경이 설정되어 있는지 확인하십시오.

이제 모든 설정이 완료되었으므로 튜토리얼을 시작하겠습니다.

## 네임스페이스 가져오기

Java 코드에서 필요한 네임스페이스를 가져오는 것부터 시작하세요. 이러한 가져오기는 Java용 Aspose.CAD 작업에 필요한 클래스 및 메서드에 대한 액세스를 제공합니다.

```java
import com.aspose.cad.Image;
import com.aspose.cad.InterpolationMode;
import com.aspose.cad.SmoothingMode;
import com.aspose.cad.TextRenderingHint;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
//import com.aspose.cad.imageoptions.TypeOfEntities;
```

## 1단계: CAD 파일 로드

 다음을 사용하여 CAD 파일을 Java 애플리케이션에 로드하는 것으로 시작하십시오.`Image.load` 방법. 바꾸다`"conic_pyramid.dxf"` CAD 파일의 경로와 함께.

```java
String dataDir = "Your Document Directory" + "ExportingCAD/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image cadImage = Image.load(srcFile);
```

## 2단계: 래스터화 옵션 설정

 인스턴스 만들기`CadRasterizationOptions` CAD 엔터티를 래스터화하는 방법을 정의합니다. 요구 사항에 따라 페이지 너비, 페이지 높이, 레이아웃 크기 조정과 같은 매개변수를 조정합니다.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
rasterizationOptions.setAutomaticLayoutsScaling(true);
rasterizationOptions.setNoScaling(false);
rasterizationOptions.setContentAsBitmap(true);
rasterizationOptions.setLayouts(new String[]{"Model"});
```

## 3단계: PDF 옵션 설정

 인스턴스 만들기`PdfOptions` 래스터화 옵션과 연결합니다. 또한 스무딩 모드, 텍스트 렌더링 힌트, 보간 모드 등 PDF 내보내기에 대한 그래픽 옵션을 설정합니다.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
rasterizationOptions.getGraphicsOptions().setSmoothingMode(SmoothingMode.HighQuality);
rasterizationOptions.getGraphicsOptions().setTextRenderingHint(TextRenderingHint.AntiAliasGridFit);
rasterizationOptions.getGraphicsOptions().setInterpolationMode(InterpolationMode.HighQualityBicubic);
```

## 4단계: PDF로 내보내기

 마지막으로 다음을 사용하여 CAD 레이아웃을 PDF 파일로 내보냅니다.`save` 의 방법`cadImage` 물체.

```java
cadImage.save(dataDir + "CADLayoutsToPDF_out_.pdf", pdfOptions);
```

축하해요! Aspose.CAD for Java를 사용하여 CAD 레이아웃을 PDF로 성공적으로 내보냈습니다. CAD 파일 조작 경험을 향상시키기 위해 Aspose.CAD가 제공하는 추가 기능을 자유롭게 탐색하십시오.

## 결론

이 튜토리얼에서는 Aspose.CAD for Java를 사용하여 CAD 레이아웃을 PDF로 내보내는 과정을 살펴보았습니다. 강력한 기능과 사용하기 쉬운 API를 갖춘 Aspose.CAD는 개발자가 Java 애플리케이션에서 CAD 파일을 효율적으로 작업할 수 있도록 지원합니다.

## FAQ

### Q1: Aspose.CAD for Java를 다른 CAD 파일 형식과 함께 사용할 수 있습니까?

 A1: 예, Aspose.CAD는 DWG, DXF, DWF 등을 포함한 다양한 CAD 형식을 지원합니다. 문서를 확인하세요[여기](https://reference.aspose.com/cad/java/) 전체 목록을 보려면.

### Q2: Aspose.CAD for Java에 대한 무료 평가판이 있습니까?

 A2: 예, 무료 평가판을 통해 Aspose.CAD의 기능을 탐색할 수 있습니다.[여기](https://releases.aspose.com/).

### Q3: Java용 Aspose.CAD에 대한 지원을 어떻게 받을 수 있나요?

 A3: Aspose.CAD 포럼을 방문하세요.[여기](https://forum.aspose.com/c/cad/19) 지역 사회 지원을 위해. 프리미엄 지원을 받으려면 라이선스 구매를 고려하세요.[여기](https://purchase.aspose.com/buy).

### Q4: 자동 레이아웃 크기 조정과 수동 레이아웃 크기 조정의 차이점은 무엇입니까?

A4: 자동 레이아웃 크기 조정은 지정된 페이지 크기를 기준으로 레이아웃 크기를 조정하는 반면, 수동 크기 조정을 사용하면 사용자 정의 크기 조정 값을 설정할 수 있습니다.

### Q5: 내보낸 PDF 파일의 모양을 사용자 정의할 수 있습니까?

A5: 예, 코드의 그래픽 옵션을 사용자 정의하여 내보낸 PDF의 품질과 모양을 제어할 수 있습니다.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
