---
title: Java용 Aspose.CAD를 사용하여 동적 PDF 작성
linktitle: 다양한 레이아웃이 포함된 단일 PDF
second_title: Aspose.CAD 자바 API
description: Aspose.CAD for Java를 사용하여 CAD 도면의 다양한 레이아웃으로 멋진 PDF를 생성하세요. Java 개발자를 위한 손쉬운 통합과 강력한 기능.
weight: 16
url: /ko/java/other-cad-operations/single-pdf-different-layouts/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java용 Aspose.CAD를 사용하여 동적 PDF 작성

## 소개

개발자가 CAD 도면을 쉽게 조작할 수 있도록 지원하는 강력한 라이브러리인 Aspose.CAD for Java의 세계에 오신 것을 환영합니다. 이 튜토리얼에서는 Aspose.CAD for Java를 사용하여 다양한 레이아웃으로 단일 PDF를 만드는 방법을 살펴보겠습니다. 숙련된 개발자이든 이제 막 시작하는 개발자이든 이 단계별 가이드가 프로세스를 안내해 드립니다.

## 전제 조건

이 여정을 시작하기 전에 다음과 같은 전제 조건이 갖추어져 있는지 확인하세요.
- Java 환경: 컴퓨터에 Java가 설치되어 있는지 확인하십시오.
-  Aspose.CAD 라이브러리: 다음에서 Java용 Aspose.CAD 라이브러리를 다운로드하고 설치합니다.[다운로드 링크](https://releases.aspose.com/cad/java/).
- 문서 디렉토리: DWG 도면용 디렉토리를 설정합니다.

## 패키지 가져오기

Java 프로젝트에서 필요한 패키지를 가져옵니다.

```java
import com.aspose.cad.Image;
import com.aspose.cad.SizeF;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.VectorRasterizationOptions;
```

## 1단계: CAD 도면 로드

 CAD 도면을`CadImage` 물체:

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
CadImage cadImage = (CadImage)Image.load(dataDir + "City skyway map.dwg");
```

## 2단계: 래스터화 옵션 구성

CAD 이미지에 대한 래스터화 옵션을 설정합니다.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1000);
rasterizationOptions.setPageHeight(1000);
```

## 3단계: 레이아웃 페이지 크기 사용자 정의

CAD 도면 내의 여러 레이아웃에 대한 사용자 정의 크기를 정의합니다.

```java
rasterizationOptions.getLayoutPageSizes().addItem("ANSI C Plot", new SizeF(500, 1000));
rasterizationOptions.getLayoutPageSizes().addItem("8.5 x 11 Plot", new SizeF(1000, 100));
```

## 4단계: PDF 옵션 설정

래스터화 설정을 통합하여 PDF 옵션을 구성합니다.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## 5단계: PDF로 저장

처리된 CAD 이미지를 PDF로 저장합니다.

```java
cadImage.save(dataDir + "singlePDF_out.pdf", pdfOptions);
```

축하해요! Aspose.CAD for Java를 사용하여 다양한 레이아웃의 단일 PDF를 성공적으로 만들었습니다.

## 결론

이 튜토리얼에서는 CAD 도면에서 다양한 레이아웃이 포함된 PDF를 생성하기 위해 Java용 Aspose.CAD의 원활한 통합을 살펴보았습니다. 라이브러리의 유연성과 강력한 기능으로 인해 CAD 조작 작업에 적합한 라이브러리입니다.

## FAQ

### Q1: Aspose.CAD for Java를 다른 Java 라이브러리와 함께 사용할 수 있나요?

A1: 예, Aspose.CAD for Java는 다른 Java 라이브러리와 완벽하게 통합되어 광범위한 기능을 제공하도록 설계되었습니다.

### Q2: 평가판을 사용할 수 있나요?

 A2: 물론이죠! 무료 평가판에 액세스할 수 있습니다[여기](https://releases.aspose.com/).

### Q3: 추가 지원은 어디서 찾을 수 있나요?

 A3: 다음을 방문하세요.[Aspose.CAD 포럼](https://forum.aspose.com/c/cad/19) 커뮤니티 지원 및 토론을 위해.

### Q4: 임시 라이센스는 어떻게 얻나요?

 A4: 임시 라이센스를 얻을 수 있습니다[여기](https://purchase.aspose.com/temporary-license/).

### Q5: 정식 버전은 어디서 구입할 수 있나요?

A5: Java용 Aspose.CAD 정식 버전을 구입하세요.[여기](https://purchase.aspose.com/buy).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
