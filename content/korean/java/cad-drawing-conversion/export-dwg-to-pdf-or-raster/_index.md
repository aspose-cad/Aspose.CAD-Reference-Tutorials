---
title: Java용 Aspose.CAD를 사용하여 DWG를 PDF 또는 래스터로 내보내기
linktitle: DWG를 PDF 또는 래스터로 내보내기
second_title: Aspose.CAD 자바 API
description: Aspose.CAD를 사용하여 DWG 파일을 PDF 또는 Java의 래스터 이미지로 내보내는 원활한 프로세스를 살펴보세요. 이 단계별 가이드는 정확성과 효율성을 보장합니다.
type: docs
weight: 13
url: /ko/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/
---
## 소개

CAD(컴퓨터 지원 설계)의 역동적인 세계에서는 도면을 효율적으로 처리하는 것이 중요합니다. Aspose.CAD for Java는 DWG 파일을 PDF 또는 래스터 이미지로 내보내기 위한 강력한 솔루션을 제공합니다. 이 튜토리얼은 프로세스를 안내하여 Java용 Aspose.CAD의 잠재력을 최대한 활용하도록 보장합니다.

## 전제 조건

튜토리얼을 시작하기 전에 다음 사항을 확인하세요.

- Java 프로그래밍에 대한 기본 이해.
-  Java 라이브러리용 Aspose.CAD가 설치되었습니다. 그렇지 않은 경우 다운로드하십시오.[여기](https://releases.aspose.com/cad/java/).
- 테스트용 DWG 파일입니다. 제공된 "Bottom_plate.dwg" 파일을 사용할 수 있습니다.

## 네임스페이스 가져오기

Java 프로젝트에서 프로세스를 시작하는 데 필요한 네임스페이스를 가져옵니다.

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.UnitType;
```

## 1단계: DWG 파일 로드

 Aspose.CAD를 사용하여 DWG 파일을 로드하는 것부터 시작하세요.`Image` 수업:

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String srcFile = dataDir + "Bottom_plate.dwg";
Image objImage = Image.load(srcFile);
```

## 2단계: 단위 유형 결정

다음으로 로드된 DWG 파일의 단위 유형을 확인합니다.

```java
Boolean currentUnitIsMetric = IsMetric(objImage.getUnitType());
int currentUnitCoefficient = objImage.getUnitType();
```

## 3단계: 래스터화 옵션 설정

단위 유형에 따라 래스터화 옵션을 구성합니다.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();

if (currentUnitIsMetric) {
    // 미터법 단위
    double metersCoeff = 1 / 1000.0;
    double scaleFactor = metersCoeff / currentUnitCoefficient;
    rasterizationOptions.setPageWidth((float)(210 * scaleFactor));
    rasterizationOptions.setPageHeight((float)(297 * scaleFactor));
    rasterizationOptions.setUnitType(UnitType.Millimeter);
} else {
    // 제국 단위
    rasterizationOptions.setPageWidth((float)(8.27f / currentUnitCoefficient));
    rasterizationOptions.setPageHeight((float)(11.69f / currentUnitCoefficient));
    rasterizationOptions.setUnitType(UnitType.Inch);
}
```

## 4단계: PDF 옵션 구성

PDF 내보내기 옵션 설정:

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(new CadRasterizationOptions());
```

## 5단계: PDF로 저장

마지막으로 DWG 파일을 PDF로 저장합니다.

```java
objImage.save(dataDir + "Saved.pdf", pdfOptions);
```

그리고 거기에 있습니다! Java용 Aspose.CAD를 사용하여 DWG 파일을 PDF로 성공적으로 내보냈습니다.

## 결론

이 튜토리얼에서는 Java용 Aspose.CAD를 활용하여 DWG 파일을 PDF 또는 래스터 이미지로 내보내는 방법에 대한 단계별 가이드를 제공했습니다. 이 라이브러리는 프로세스를 단순화하여 Java 애플리케이션에서 CAD 도면을 효율적으로 처리할 수 있도록 해줍니다.

## FAQ

### Q1: 다른 Java 프레임워크와 함께 Java용 Aspose.CAD를 사용할 수 있습니까?

A1: 예, Aspose.CAD for Java는 널리 사용되는 Java 프레임워크와 완벽하게 통합됩니다.

### Q2: Aspose.CAD for Java에 임시 라이선스를 사용할 수 있나요?

 A2: 예, 임시 라이센스를 얻을 수 있습니다.[여기](https://purchase.aspose.com/temporary-license/).

### Q3: Java용 Aspose.CAD에 대한 지원은 어디서 찾을 수 있나요?

 A3: 다음을 방문하세요.[Aspose.CAD 포럼](https://forum.aspose.com/c/cad/19) 지역 사회의 도움을 요청합니다.

### Q4: Aspose.CAD for Java 라이선스는 어떻게 구매할 수 있나요?

 A4: 라이센스를 구매할 수 있습니다.[여기](https://purchase.aspose.com/buy).

### Q5: Aspose.CAD for Java는 어떤 단위를 지원합니까?

A5: Java용 Aspose.CAD는 미터법과 영국식 단위를 모두 지원합니다.