---
title: 내보내기 시 펜 지원
linktitle: 내보내기 시 펜 지원
second_title: Aspose.CAD 자바 API
description: Java용 Aspose.CAD를 사용하여 CAD 내보내기의 마스터 펜 사용자 정의. 원활한 통합을 위한 단계별 가이드를 따르세요.
weight: 13
url: /ko/java/advanced-cad-features/pen-support-in-export/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 내보내기 시 펜 지원

## 소개

끊임없이 진화하는 CAD(Computer-Aided Design) 변환 환경에서 Java용 Aspose.CAD는 CAD 파일을 조작하기 위한 광범위한 기능을 제공하는 강력한 도구로 등장합니다. 다양한 기능 중에서 내보내기 중 펜 사용자 정의 지원이 눈에 띕니다. 이를 통해 사용자는 내보낸 이미지의 모양을 맞춤화할 수 있습니다. 이 튜토리얼에서는 Java를 사용한 실제 구현에 중점을 두고 내보내기 기능에서 펜 지원을 활용하는 프로세스를 안내합니다.

## 전제 조건

튜토리얼을 자세히 살펴보기 전에 다음 전제 조건이 충족되었는지 확인하세요.

- Java 개발 환경: 귀하의 컴퓨터에 기능적인 Java 개발 환경이 설정되어 있는지 확인하십시오.

-  Aspose.CAD 라이브러리: Aspose.CAD 라이브러리를 다운로드하여 Java 프로젝트에 통합하세요. 도서관을 찾으실 수 있습니다[여기](https://releases.aspose.com/cad/java/).

이제 튜토리얼로 이동하여 CAD 내보내기 중 펜 지원을 활용하는 단계를 살펴보겠습니다.

## 네임스페이스 가져오기

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.PenOptions;
import com.aspose.cad.internal.imaging.LineCap;
```

## 1단계: 문서 디렉터리 정의

```java
String dataDir = "Your Document Directory" + "CADConversion/";
```

"문서 디렉토리"를 CAD 문서의 실제 경로로 바꾸십시오.

## 2단계: CAD 파일 로드

```java
String srcFile = dataDir + "conic_pyramid.dxf";
CadImage cadImage = (CadImage) Image.load(srcFile);
```

이 단계에는 Aspose.CAD 라이브러리를 사용하여 CAD 파일(이 경우 "conic_pyramid.dxf")을 로드하는 작업이 포함됩니다.

## 3단계: 래스터화 옵션 구성

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(cadImage.getWidth() * 100);
rasterizationOptions.setPageHeight(cadImage.getHeight() * 100);
```

특정 요구 사항에 따라 페이지 너비와 높이를 조정합니다. 이러한 값은 내보낸 이미지의 크기를 결정합니다.

## 4단계: 펜 옵션 사용자 정의

```java
PenOptions penOts = new PenOptions();
penOts.setStartCap(LineCap.Flat);
penOts.setEndCap(LineCap.Flat);
```

필요에 따라 펜의 시작 및 끝 캡을 사용자 정의합니다. 이 사용자 정의는 CadImage 개체를 다양한 이미지 형식으로 내보낼 때 적용됩니다.

## 5단계: PDF 내보내기 옵션 구성

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

이전에 구성한 래스터화 옵션을 포함하여 벡터 래스터화 옵션을 지정합니다.

## 6단계: 내보낸 PDF 저장

```java
cadImage.save((dataDir + "9LHATT-A56_generated.pdf"), pdfOptions);
```

내보낸 PDF를 지정된 파일 이름(이 예에서는 "9LHATT-A56_generated.pdf")과 구성된 옵션으로 저장합니다.

## 결론

결론적으로, Aspose.CAD for Java를 사용하여 CAD를 내보내는 동안 펜 지원을 활용하면 사용자가 내보낸 이미지의 모양을 사용자 정의할 수 있습니다. 이 단계별 가이드를 따라 펜 사용자 정의를 CAD 변환 워크플로에 원활하게 통합하는 방법을 배웠습니다.

## FAQ

### Q1: PDF 이외의 형식에 대한 펜 옵션을 사용자 정의할 수 있습니까?

A1: 예, 이 튜토리얼에서 설명하는 펜 사용자 정의는 PDF, PNG, BMP, GIF, JPEG2000, JPEG, PSD, TIFF 및 WMF를 포함한 다양한 이미지 형식에 적용 가능합니다.

### 질문 2: 펜의 시작 대문자와 끝 대문자가 다른 경우 어떻게 처리할 수 있나요?

 A2: 활용`PenOptions` 원하는 시작 및 끝 대문자를 설정하는 클래스를 사용하여 선의 모양을 정의하는 데 유연성을 제공합니다.

### Q3: 펜 옵션을 지정하지 않으면 어떻게 되나요?

대답 3: 펜 옵션이 명시적으로 설정되지 않은 경우 시스템은 상황에 따라 달라질 수 있는 기본 펜을 사용합니다.

### Q4: 래스터화 옵션에 대해 특별히 고려해야 할 사항이 있습니까?

A4: 래스터화 옵션에서 페이지 너비와 높이를 조정하여 내보낸 이미지의 크기를 제어합니다.

### Q5: 추가 지원이나 커뮤니티 토론은 어디서 찾을 수 있나요?

 A5: Aspose.CAD 커뮤니티 포럼을 살펴보세요.[여기](https://forum.aspose.com/c/cad/19) 지원과 토론을 위해.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
