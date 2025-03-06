---
title: Java용 Aspose.CAD를 사용하여 DGN을 DWG로 내보내기
linktitle: DGN을 DWG의 일부로 내보내기
second_title: Aspose.CAD 자바 API
description: Java용 Aspose.CAD를 사용하여 DGN을 DWG의 일부로 내보내는 방법을 살펴보세요. 효율적인 CAD 파일 조작을 위한 단계별 가이드를 따르십시오.
weight: 10
url: /ko/java/dgn-export-options/export-dgn-as-part-of-dwg/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java용 Aspose.CAD를 사용하여 DGN을 DWG로 내보내기

## 소개

이 튜토리얼에서는 Java용 Aspose.CAD를 사용하여 DGN(MicroStation Design) 파일을 DWG(AutoCAD Drawing) 파일의 일부로 내보내는 방법을 살펴보겠습니다. Aspose.CAD는 CAD 파일 형식으로 작업할 수 있는 포괄적인 기능을 제공하는 강력한 라이브러리입니다. 이 단계별 가이드는 Java를 사용하여 DWG의 일부로 DGN을 내보내는 프로세스를 이해하는 데 도움이 됩니다.

## 전제 조건

튜토리얼을 시작하기 전에 다음 전제 조건이 충족되었는지 확인하세요.
1. Aspose.CAD 라이브러리: Java용 Aspose.CAD 라이브러리를 다운로드하고 설치합니다. 도서관을 찾으실 수 있습니다[여기](https://releases.aspose.com/cad/java/).
2. JDK(Java Development Kit): 시스템에 Java가 설치되어 있는지 확인하십시오.
3. 통합 개발 환경(IDE): 보다 원활한 개발 환경을 위해 Eclipse 또는 IntelliJ와 같은 Java IDE를 선택하세요.

## 패키지 가져오기

Java 프로젝트에서 필요한 Aspose.CAD 패키지를 가져와 CAD 파일 조작을 활성화합니다. 예는 다음과 같습니다.

```java
import com.aspose.cad;
import com.aspose.cad.imageoptions;
import com.aspose.cad.fileformats.cad.cadconsts;
import com.aspose.cad.fileformats.cad;
import com.aspose.cad.fileformats.cad.cadobjects;
```

## 1단계: 파일 경로 설정

 DWG 파일의 입력 및 출력 파일 경로를 정의합니다. 업데이트`dataDir`, `fileName` , 그리고`outPath` 그에 따라 변수.

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "BlockRefDgn.dwg";
String outPath = dataDir + "BlockRefDgn.dwg.pdf";
```

## 2단계: PdfOptions 인스턴스 생성

 인스턴스를 생성합니다.`PdfOptions` DWG 파일을 PDF 형식으로 내보내는 중입니다.

```java
PdfOptions exportOptions = new PdfOptions();
```

## 3단계: DWG 파일 로드

 기존 DWG 파일을 이미지로 로드하고 이를`CadImage` 유형.

```java
CadImage cadImage = (CadImage) Image.load(fileName);
```

## 4단계: 엔터티 반복

DWG 파일 내의 각 엔터티를 살펴보고 이미지 정의인지 확인합니다. 그렇다면 객체에 대한 외부 참조를 검색하십시오.

```java
for (CadBaseEntity baseEntity : cadImage.getEntities()) {
    if (baseEntity.getTypeName() == CadEntityTypeName.DGNUNDERLAY) {
        CadDgnUnderlay dgnFile = (CadDgnUnderlay)baseEntity;
        System.out.println(dgnFile.getUnderlayPath());
    }
}
```

## 5단계: 래스터화 옵션 정의

 에 대한 설정을 정의합니다.`CadRasterizationOptions`페이지 너비, 높이, 레이아웃 및 배경색을 포함한 개체.

```java
CadRasterizationOptions vectorRasterizationOptions = new CadRasterizationOptions();
vectorRasterizationOptions.setPageWidth(1600);
vectorRasterizationOptions.setPageHeight(1600);
vectorRasterizationOptions.setLayouts(new String[] { "Model" });
vectorRasterizationOptions.setAutomaticLayoutsScaling(false);
vectorRasterizationOptions.setNoScaling(true);
vectorRasterizationOptions.setBackgroundColor(Color.getBlack());
vectorRasterizationOptions.setDrawType(CadDrawTypeMode.UseObjectColor);
```

## 6단계: 벡터 래스터화 옵션 설정

내보내기에 대한 벡터 래스터화 옵션을 설정합니다.

```java
exportOptions.setVectorRasterizationOptions(vectorRasterizationOptions);
```

## 7단계: DWG를 PDF로 내보내기

 마지막으로 다음을 호출하여 DWG를 PDF로 내보냅니다.`save` 방법.

```java
cadImage.save(outPath, exportOptions);
```

## 결론

축하해요! Aspose.CAD for Java를 사용하여 DGN 파일을 DWG 파일의 일부로 내보내는 방법을 성공적으로 배웠습니다. 이 강력한 라이브러리는 CAD 파일 작업을 위한 광범위한 기능을 제공하여 CAD 파일 조작 작업을 효율적이고 간단하게 만듭니다.

## FAQ

### Q1: Aspose.CAD for Java 설명서는 어디서 찾을 수 있나요?

 A1: 문서를 찾을 수 있습니다.[여기](https://reference.aspose.com/cad/java/).

### Q2: Java용 Aspose.CAD 라이브러리를 어떻게 다운로드할 수 있나요?

 A2: 다음에서 라이브러리를 다운로드할 수 있습니다.[이 링크](https://releases.aspose.com/cad/java/).

### Q3: Aspose.CAD for Java에 대한 무료 평가판이 있습니까?

 A3: 예, 무료 평가판을 찾을 수 있습니다.[여기](https://releases.aspose.com/).

### Q4: Aspose.CAD for Java의 임시 라이선스는 어디서 구할 수 있나요?

 A4: 임시 라이센스 취득[여기](https://purchase.aspose.com/temporary-license/).

### Q5: 도움이 필요하거나 질문이 있나요?

 A5: Aspose.CAD 커뮤니티 지원 포럼을 방문하세요.[여기](https://forum.aspose.com/c/cad/19).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
