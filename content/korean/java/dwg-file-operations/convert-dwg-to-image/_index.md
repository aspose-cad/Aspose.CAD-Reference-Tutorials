---
title: Java를 사용하여 특정 DWG를 이미지로 변환
linktitle: Java를 사용하여 특정 DWG를 이미지로 변환
second_title: Aspose.CAD 자바 API
description: Java용 Aspose.CAD를 사용하여 DWG를 이미지로 원활하게 변환하는 방법을 살펴보세요. 효율적인 파일 형식 변환을 위한 단계별 가이드를 따르세요.
type: docs
weight: 14
url: /ko/java/dwg-file-operations/convert-dwg-to-image/
---
## 소개

끊임없이 진화하는 디지털 디자인 환경에서 DWG 도면을 이미지로 변환해야 하는 필요성은 일반적인 요구 사항입니다. Aspose.CAD for Java는 이 작업을 원활하게 수행할 수 있는 강력한 도구로 등장합니다. 이 튜토리얼에서는 Aspose.CAD for Java를 사용하여 특정 DWG 파일을 이미지로 변환하는 과정을 안내합니다.

## 전제 조건

튜토리얼을 시작하기 전에 다음 전제조건이 충족되었는지 확인하십시오.
1.  JDK(Java Development Kit): Java용 Aspose.CAD를 사용하려면 시스템에 호환 가능한 JDK가 설치되어 있어야 합니다. 최신 JDK는 다음에서 다운로드할 수 있습니다.[오라클의 웹사이트](https://www.oracle.com/java/technologies/javase-downloads.html).
2.  Java 라이브러리용 Aspose.CAD: 다음에서 Java 라이브러리용 Aspose.CAD를 다운로드하고 설치합니다.[Aspose.CAD 다운로드 페이지](https://releases.aspose.com/cad/java/).
3. IDE(통합 개발 환경): IntelliJ IDEA 또는 Eclipse 등 Java 개발에 선호하는 IDE를 선택하세요.

## 패키지 가져오기

Java 프로젝트에서 원활한 통합을 위해 필요한 Aspose.CAD 패키지를 가져옵니다. 코드에 다음을 포함합니다.

```java
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadconsts.CadEntityTypeName;
import com.aspose.cad.fileformats.cad.cadobjects.CadBaseEntity;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import java.util.ArrayList;
import java.util.Collection;
import java.util.Iterator;
import java.util.List;
import java.util.ListIterator;
```

## 1단계: 프로젝트 설정

Java 프로젝트가 필요한 Aspose.CAD 라이브러리로 설정되어 있고 JDK가 IDE에 올바르게 구성되어 있는지 확인하세요.

## 2단계: DWG 파일 경로 지정

변환하려는 DWG 파일의 경로를 정의합니다. 업데이트`dataDir` 그리고`sourceFilePath` 그에 따라 변수.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String sourceFilePath = dataDir + "visualization_-_conference_room.dwg";
```

## 3단계: 텍스트 엔터티 필터링

DWG 엔터티를 반복하고 Aspose.CAD 라이브러리를 사용하여 텍스트 엔터티를 필터링합니다.

```java
CadImage cadImage = (CadImage) (Image.load(sourceFilePath));
CadBaseEntity[] entities = cadImage.getEntities();
List<CadBaseEntity> filteredEntities = new ArrayList<>();
for (CadBaseEntity baseEntity : entities) {
    if ((baseEntity.getTypeName() == CadEntityTypeName.TEXT)) {
        filteredEntities.add(baseEntity);
    }
}
CadBaseEntity[] arr = new CadBaseEntity[filteredEntities.size()];
cadImage.setEntities(filteredEntities.toArray(arr));
```

## 4단계: 래스터화 옵션 설정

 인스턴스 만들기`CadRasterizationOptions` PDF 변환을 위한 속성을 구성합니다.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
rasterizationOptions.setAutomaticLayoutsScaling(true);
```

## 5단계: PDF로 내보내기

 만들기`PdfOptions` 예를 들어 벡터 래스터화 옵션을 설정하고 변환된 PDF 파일을 저장합니다.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
String outFile = dataDir + "result_out_generated.pdf";
cadImage.save(outFile, pdfOptions);
```

축하해요! Aspose.CAD for Java를 사용하여 특정 DWG 파일을 이미지로 성공적으로 변환했습니다.

## 결론

Java용 Aspose.CAD는 DWG에서 이미지로의 변환 프로세스를 단순화하여 설계 작업 흐름에 유연성과 효율성을 제공합니다. 이 도구를 프로젝트에 통합하여 생산성을 높이고 파일 형식 변환을 간소화하세요.

## FAQ

### Q1: Aspose.CAD는 모든 버전의 DWG 파일과 호환됩니까?

A1: Aspose.CAD는 광범위한 DWG 버전을 지원하여 다양한 파일 형식과의 호환성을 보장합니다.

### Q2: 출력 이미지의 해상도를 맞춤 설정할 수 있나요?

A2: 예, 튜토리얼에서는 페이지 너비와 높이를 설정하여 해상도를 제어하는 방법을 보여줍니다.

### Q3: Aspose.CAD는 일괄 변환에 적합합니까?

A3: 물론이죠. Aspose.CAD에서는 일괄 처리가 가능하므로 여러 DWG 파일을 동시에 변환할 수 있습니다.

### Q4: 추가 지원이나 커뮤니티 토론은 어디서 찾을 수 있나요?

 A4: 다음을 방문하세요.[Aspose.CAD 포럼](https://forum.aspose.com/c/cad/19) 지원과 토론을 위해.

### Q5: 구매하기 전에 Aspose.CAD를 사용해 볼 수 있나요?

 A5: 예. 다음에서 제공되는 무료 평가판을 통해 도구를 살펴보세요.[이 링크](https://releases.aspose.com/).