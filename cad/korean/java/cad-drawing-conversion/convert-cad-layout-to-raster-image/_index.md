---
title: Aspose.CAD for Java를 사용하여 CAD 레이아웃을 래스터 이미지 형식으로 변환
linktitle: CAD 레이아웃을 래스터 이미지 형식으로 변환
second_title: Aspose.CAD 자바 API
description: Aspose.CAD for Java를 사용하여 CAD 레이아웃을 래스터 이미지로 쉽게 변환하세요. 향상된 협업을 위한 고품질 시각화.
weight: 12
url: /ko/java/cad-drawing-conversion/convert-cad-layout-to-raster-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD for Java를 사용하여 CAD 레이아웃을 래스터 이미지 형식으로 변환

## 소개

CAD(컴퓨터 지원 설계)의 역동적인 세계에서 CAD 레이아웃을 래스터 이미지 형식으로 원활하게 변환하는 능력은 귀중한 기술입니다. Aspose.CAD for Java는 이 작업을 효율적으로 수행하기 위한 강력한 솔루션으로 등장합니다. 이 튜토리얼에서는 Aspose.CAD for Java를 사용하여 CAD 레이아웃을 래스터 이미지로 변환하는 과정을 단계별로 안내합니다.

## 전제 조건

튜토리얼을 시작하기 전에 다음 전제 조건이 충족되었는지 확인하세요.

1. Java 개발 환경: 시스템에 Java 개발 환경이 설치되어 있는지 확인하십시오.

2.  Aspose.CAD 라이브러리: Aspose.CAD 라이브러리를 다운로드하여 설치합니다. 에서 얻으실 수 있습니다.[Java 문서용 Aspose.CAD](https://reference.aspose.com/cad/java/).

## 네임스페이스 가져오기

Java용 Aspose.CAD의 기능을 활용하는 데 필요한 네임스페이스를 가져오는 것부터 시작하세요. Java 코드에 다음 네임스페이스를 포함합니다.

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

이제 예제 코드를 CAD 레이아웃을 래스터 이미지로 변환하는 일련의 단계로 나누어 보겠습니다.
## 1단계: 리소스 디렉터리 설정

```java
// 리소스 디렉터리의 경로입니다.
String dataDir = "Your Document Directory" + "CADConversion/";
```

"Your Document Directory"를 실제 문서 디렉터리 경로로 바꾸십시오.

## 2단계: CAD 파일 로드

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

CAD 파일의 경로를 지정하고 Aspose.CAD를 사용하여 로드합니다.

## 3단계: 래스터화 옵션 구성

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1200);
rasterizationOptions.setPageHeight(1200);
rasterizationOptions.setLayouts(new String[] {"Model", "Layout1"});
```

 인스턴스 만들기`CadRasterizationOptions` 페이지 크기와 레이아웃을 설정합니다.

## 4단계: 이미지 옵션 설정

```java
ImageOptionsBase options = new TiffOptions(TiffExpectedFormat.Default);
options.setVectorRasterizationOptions(rasterizationOptions);
```

 인스턴스 만들기`ImageOptions` 래스터화 옵션과 연결합니다.

## 5단계: 결과 이미지 저장

```java
image.save(dataDir + "conic_pyramid_layoutstorasterimage_out_.tiff", options);
```

최종 래스터 이미지를 원하는 형식과 위치에 저장합니다.

필요에 따라 매개변수를 조정하면서 이러한 단계를 반복하여 특정 요구 사항에 따라 변환을 사용자 정의합니다.

## 결론

Aspose.CAD for Java는 CAD 레이아웃을 래스터 이미지로 변환하는 프로세스를 간소화하여 유연성과 정확성을 제공합니다. 이 기술을 익히면 CAD 프로젝트에서 효율적인 시각화 및 협업 가능성이 열립니다.

## FAQ

### Q1: Aspose.CAD는 다른 CAD 파일 형식과 호환됩니까?

A1: 예, Aspose.CAD는 DWG, DXF 및 DGN을 포함한 다양한 CAD 형식을 지원합니다.

### Q2: 출력 래스터 이미지의 해상도를 사용자 정의할 수 있습니까?

 A2: 물론이죠. 조정하다`setPageWidth` 그리고`setPageHeight` 매개변수`CadRasterizationOptions` 원하는 해상도를 위해

### Q3: 여러 CAD 레이아웃을 동시에 변환하려면 어떻게 해야 합니까?

 A3: 전달된 배열을 확장하기만 하면 됩니다.`setLayouts` 변환하려는 레이아웃의 이름을 사용하세요.

### Q4: TIFF 외에 다른 출력 형식이 지원됩니까?

A4: 예, Aspose.CAD는 PNG, JPG 및 PDF와 같은 다양한 출력 형식을 지원합니다.

### Q5: Aspose.CAD에 대한 도움을 구하거나 경험을 공유할 수 있는 곳은 어디입니까?

A5: 다음을 방문하세요.[Aspose.CAD 포럼](https://forum.aspose.com/c/cad/19) 지역 사회에 참여하고 지원을 받으십시오.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
