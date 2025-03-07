---
title: 캔버스 크기 및 모드 설정
linktitle: 캔버스 크기 및 모드 설정
second_title: Aspose.CAD 자바 API
description: 캔버스 크기 및 모드 설정에 대한 단계별 가이드를 통해 Java용 Aspose.CAD의 강력한 기능을 살펴보세요. CAD 파일을 PDF 및 TIFF 형식으로 쉽게 변환하세요.
weight: 16
url: /ko/java/advanced-cad-features/set-canvas-size-and-mode/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 캔버스 크기 및 모드 설정

## 소개

CAD 변환 프로세스를 향상시키기 위해 Java용 Aspose.CAD의 기능을 활용하고 싶으십니까? 이 포괄적인 가이드는 Aspose.CAD for Java를 사용하여 캔버스 크기와 모드를 설정하는 단계를 안내합니다. 숙련된 개발자이든 이제 막 시작하는 개발자이든 이 튜토리얼은 필요한 통찰력을 제공할 것입니다.

## 전제 조건

튜토리얼을 시작하기 전에 다음 전제 조건이 충족되었는지 확인하세요.

-  Java용 Aspose.CAD: Java 환경에 Aspose.CAD 라이브러리가 설치되어 있는지 확인하십시오. 당신은 그것을 다운로드 할 수 있습니다[여기](https://releases.aspose.com/cad/java/).

- 문서 디렉터리: CAD 파일을 저장할 문서 디렉터리를 설정합니다. 이 디렉터리는 자습서 단계에서 참조됩니다.

이제 단계별 가이드를 시작해 보겠습니다.

## 네임스페이스 가져오기

이 단계에서는 Aspose.CAD 프로젝트를 시작하는 데 필요한 네임스페이스를 가져옵니다.
```java
import java.awt.Image;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

## 1단계: Aspose.CAD 클래스 가져오기

```java
// 리소스 디렉터리의 경로입니다.
String dataDir = "Your Document Directory" + "CADConversion/";

String srcFile = dataDir + "conic_pyramid.dxf";
com.aspose.cad.Image objImage = com.aspose.cad.Image.load(srcFile);
```

 이 스니펫에서는 리소스 디렉터리 경로를 설정하고 Aspose.CAD를 사용하여 DXF 파일을 로드합니다.`Image` 수업.

## 2단계: CadRasterizationOptions 속성 설정

```java
// CadRasterizationOptions 인스턴스를 생성하고 다양한 속성을 설정합니다.
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);

rasterizationOptions.setAutomaticLayoutsScaling(true);
rasterizationOptions.setNoScaling(true);
```

 여기서는 인스턴스를 생성합니다.`CadRasterizationOptions` 페이지 너비, 페이지 높이, 크기 조정 옵션과 같은 속성을 구성합니다.

## 3단계: PdfOptions 생성 및 VectorRasterizationOptions 설정

```java
// PdfOptions 인스턴스 만들기
PdfOptions pdfOptions = new PdfOptions();

// VectorRasterizationOptions 속성 설정
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

 이제 우리는`PdfOptions` 인스턴스를 설정하고`VectorRasterizationOptions` 속성을 이전에 구성한`CadRasterizationOptions`.

## 4단계: PDF로 내보내기

```java
// CAD를 PDF로 내보내기
objImage.save(dataDir + "result_out_.pdf", pdfOptions);
```

마지막으로 지정된 옵션을 사용하여 CAD 이미지를 PDF 파일로 저장합니다.

## 5단계: TiffOptions 생성 및 VectorRasterizationOptions 설정

```java
// TiffOptions 인스턴스 생성
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);

// VectorRasterizationOptions 속성 설정
tiffOptions.setVectorRasterizationOptions(rasterizationOptions);
```

이 단계에서는`TiffOptions` 인스턴스를 구성하고`VectorRasterizationOptions` 재산.

## 6단계: TIFF로 내보내기

```java
// CAD를 TIFF로 내보내기
objImage.save(dataDir + "result_out_.tiff", tiffOptions);
```

마지막으로 지정된 옵션을 사용하여 CAD 이미지를 TIFF 파일에 저장합니다.

## 결론

 축하해요! Aspose.CAD for Java를 사용하여 캔버스 크기와 모드를 성공적으로 설정했습니다. 이 튜토리얼은 CAD 변환 프로젝트를 위한 견고한 기반을 제공합니다. 더 많은 기능과 가능성을 살펴보세요.[Aspose.CAD 문서](https://reference.aspose.com/cad/java/).

## FAQ

### Q1: 다른 Java 프레임워크와 함께 Java용 Aspose.CAD를 사용할 수 있습니까?

A1: 예, Aspose.CAD는 다양한 Java 프레임워크와 원활하게 통합되도록 설계되었습니다.

### Q2: Aspose.CAD에 임시 라이선스를 사용할 수 있나요?

 A2: 예, 임시 라이센스를 얻을 수 있습니다.[여기](https://purchase.aspose.com/temporary-license/).

### Q3: Aspose.CAD에 대한 커뮤니티 지원은 어디서 받을 수 있나요?

 A3: 다음을 방문하세요.[Aspose.CAD 포럼](https://forum.aspose.com/c/cad/19) 커뮤니티 지원 및 토론을 위해.

### Q4: Aspose.CAD를 무료로 사용해 볼 수 있나요?

 A4: 물론이죠! 무료 평가판 받기[여기](https://releases.aspose.com/).

### Q5: Java용 Aspose.CAD를 어떻게 구매하나요?

 A5: 제품 구매[여기](https://purchase.aspose.com/buy).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
