---
title: CAD 도면에 워터마크 추가 - Java 튜토리얼용 Aspose.CAD
linktitle: 워터 마크를 추가
second_title: Aspose.CAD 자바 API
description: Aspose.CAD for Java를 사용하여 개인화된 워터마크로 CAD 도면을 향상하세요. 원활한 통합을 위한 단계별 가이드를 따르세요.
type: docs
weight: 12
url: /ko/java/other-cad-operations/add-watermark/
---
## 소개

Aspose.CAD for Java를 사용하여 CAD 도면에 워터마크를 추가하는 방법에 대한 포괄적인 가이드에 오신 것을 환영합니다. 이 튜토리얼에서는 워터마크를 효율적으로 통합하여 개인화된 메시지나 브랜딩으로 CAD 문서를 향상시키는 방법을 배우게 됩니다. Aspose.CAD for Java는 강력한 기능 세트를 제공하여 워터마크 추가 프로세스를 간단하게 만듭니다.

## 전제 조건

튜토리얼을 시작하기 전에 다음 전제 조건이 충족되었는지 확인하세요.

-  Java용 Aspose.CAD: Java 환경에 Aspose.CAD 라이브러리가 설치되어 있는지 확인하십시오. 당신은 그것을 다운로드 할 수 있습니다[여기](https://releases.aspose.com/cad/java/).
- JDK(Java Development Kit): 시스템에 최신 버전의 JDK가 설치되어 있는지 확인하십시오.

## 패키지 가져오기

Java 프로젝트에서 시작하려면 필요한 Aspose.CAD 패키지를 가져옵니다.

```java
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.Cad3DPoint;
import com.aspose.cad.fileformats.cad.cadobjects.CadMText;
import com.aspose.cad.fileformats.cad.cadobjects.CadText;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## 1단계: 새 MTEXT 추가

```java
//새 MTEXT 추가
CadMText watermark = new CadMText();
watermark.setText("Watermark message");
watermark.setInitialTextHeight(40);
watermark.setInsertionPoint(new Cad3DPoint(300, 40));
watermark.setLayerName("0");
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(watermark);
```

## 2단계: 텍스트와 같은 단순 엔터티 추가

텍스트와 같이 보다 간단한 엔터티를 추가할 수도 있습니다.

```java
// 또는 텍스트와 같은 더 간단한 엔터티를 추가하세요.
CadText text = new CadText();
text.setDefaultValue("Watermark text");
text.setTextHeight(40);
text.setFirstAlignment(new Cad3DPoint(300, 40));
text.setLayerName("0") ;
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(text);
```

## 3단계: PDF로 내보내기

워터마크가 추가된 CAD 도면을 PDF 파일로 내보냅니다.

```java
// PDF로 내보내기
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
rasterizationOptions.setLayouts(new String[]{"Model"});
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
cadImage.save(dataDir + "AddWatermark_out.pdf", pdfOptions);

```

## 결론

축하해요! Aspose.CAD for Java를 사용하여 CAD 도면에 워터마크를 성공적으로 추가했습니다. 이 간단하면서도 강력한 프로세스를 통해 디자인을 개인화하거나 브랜딩으로 보호할 수 있습니다.

## FAQ

### Q1: Aspose.CAD는 모든 CAD 파일 형식과 호환됩니까?

A1: Aspose.CAD는 DWG, DXF, DWT 및 DWF를 포함한 다양한 CAD 형식을 지원합니다.

### Q2: 워터마크 텍스트의 모양을 사용자 정의할 수 있습니까?

A2: 예, 텍스트 크기, 색상, 위치를 포함하여 워터마크의 모양을 완전히 제어할 수 있습니다.

### Q3: Aspose.CAD for Java에 사용할 수 있는 평가판이 있습니까?

 A3: 예, 평가판을 다운로드할 수 있습니다.[여기](https://releases.aspose.com/).

### Q4: Aspose.CAD에 대한 지원은 어떻게 받을 수 있나요?

 A4: 다음을 방문하세요.[Aspose.CAD 포럼](https://forum.aspose.com/c/cad/19) 지역 사회 지원을 위해.

### Q5: Aspose.CAD for Java에 대한 전체 문서는 어디에서 찾을 수 있나요?

 A5: 다음을 참조하세요.[선적 서류 비치](https://reference.aspose.com/cad/java/) 자세한 정보를 보려면.