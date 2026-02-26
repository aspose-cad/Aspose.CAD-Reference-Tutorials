---
date: 2026-01-10
description: Aspose.CAD for Java를 사용하여 DGN을 DWG로 내보내고 MicroStation DGN을 AutoCAD DWG로
  변환하는 방법을 배웁니다. 단계별 가이드.
linktitle: Export DGN as Part of DWG
second_title: Aspose.CAD Java API
title: Aspose.CAD for Java를 사용하여 DGN을 DWG로 내보내기
url: /ko/java/dgn-export-options/export-dgn-as-part-of-dwg/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Export DGN to DWG with Aspose.CAD for Java

## Introduction

이 튜토리얼에서는 **export dgn to dwg** 방법과 Aspose.CAD for Java 라이브러리를 사용하여 MicroStation DGN 디자인을 AutoCAD DWG 파일에 삽입하는 방법을 배웁니다. 레거시 MicroStation 도면을 마이그레이션하거나 DGN 언더레이를 DWG 레이아웃과 결합해야 할 경우, 이 가이드는 환경 설정부터 최종 DWG의 PDF 미리보기를 생성하는 단계까지 모두 안내합니다.

## Quick Answers
- **“export dgn to dwg”는 무엇을 달성하나요?** DGN 언더레이를 DWG에 삽입하여 AutoCAD에서 원활하게 볼 수 있게 합니다.
- **빠른 미리보기를 위해 결과를 어떤 형식으로 내보낼 수 있나요?** `PdfOptions`를 사용하여 **CAD 파일을 PDF로 내보낼** 수 있습니다.
- **코드를 실행하려면 라이선스가 필요합니까?** 프로덕션 사용을 위해 임시 또는 유료 Aspose.CAD 라이선스가 필요합니다.
- **지원되는 Java 버전은 무엇인가요?** Java 8 이상이면 최신 Aspose.CAD for Java 릴리스와 호환됩니다.
- **무료 체험판이 있나요?** 네 – Aspose 웹사이트에서 체험판을 다운로드할 수 있습니다.

## What is “export dgn to dwg”?
Exporting DGN to DWG는 MicroStation DGN 디자인을 AutoCAD DWG 도면 내부의 언더레이로 변환하거나 삽입하는 것을 의미합니다. 이를 통해 CAD 전문가가 기존 DGN 자산을 처음부터 다시 만들지 않고도 활용할 수 있습니다.

## Why convert MicroStation DGN to AutoCAD DWG?
- **Collaboration:** AutoCAD를 사용하는 팀이 DGN 콘텐츠를 직접 보고 편집할 수 있습니다.
- **Standardization:** DWG는 PDF 생성, 3D 렌더링 등 많은 다운스트림 워크플로의 사실상 표준 형식입니다.
- **Preservation:** 원본 DGN 참조를 그대로 유지하여 데이터 손실을 최소화합니다.

## Prerequisites

튜토리얼을 시작하기 전에 다음 전제 조건을 준비하십시오:
1. **Aspose.CAD Library:** Aspose.CAD for Java 라이브러리를 다운로드하고 설치합니다. 라이브러리는 [here](https://releases.aspose.com/cad/java/)에서 찾을 수 있습니다.
2. **Java Development Kit (JDK):** 시스템에 Java가 설치되어 있는지 확인합니다.
3. **Integrated Development Environment (IDE):** Eclipse 또는 IntelliJ와 같은 Java IDE를 선택하면 개발이 더 원활합니다.

## Import Packages

Java 프로젝트에서 CAD 파일 조작을 위해 필요한 Aspose.CAD 패키지를 가져옵니다. 예시는 다음과 같습니다:

```java
import com.aspose.cad;
import com.aspose.cad.imageoptions;
import com.aspose.cad.fileformats.cad.cadconsts;
import com.aspose.cad.fileformats.cad;
import com.aspose.cad.fileformats.cad.cadobjects;
```

## Step 1: Set File Paths

DWG 파일의 입력 및 출력 경로를 정의합니다. `dataDir`, `fileName`, `outPath` 변수를 적절히 업데이트하십시오.

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "BlockRefDgn.dwg";
String outPath = dataDir + "BlockRefDgn.dwg.pdf";
```

## Step 2: Create PdfOptions Instance

`PdfOptions` 클래스의 인스턴스를 생성합니다. 여기서는 **CAD 파일을 PDF로 내보내** 빠르게 확인하기 위함입니다.

```java
PdfOptions exportOptions = new PdfOptions();
```

## Step 3: Load DWG File

기존 DWG 파일을 이미지로 로드하고 `CadImage` 타입으로 변환합니다.

```java
CadImage cadImage = (CadImage) Image.load(fileName);
```

## Step 4: Iterate Through Entities

DWG 파일 내부의 각 엔터티를 순회하면서 이미지 정의인지 확인합니다. 이미지 정의인 경우 외부 참조를 가져옵니다.

```java
for (CadBaseEntity baseEntity : cadImage.getEntities()) {
    if (baseEntity.getTypeName() == CadEntityTypeName.DGNUNDERLAY) {
        CadDgnUnderlay dgnFile = (CadDgnUnderlay)baseEntity;
        System.out.println(dgnFile.getUnderlayPath());
    }
}
```

## Step 5: Define Rasterization Options

`CadRasterizationOptions` 객체의 설정을 정의합니다. 여기에는 페이지 너비, 높이, 레이아웃 및 배경 색상이 포함됩니다.

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

## Step 6: Set Vector Rasterization Options

내보내기를 위한 벡터 래스터화 옵션을 설정합니다.

```java
exportOptions.setVectorRasterizationOptions(vectorRasterizationOptions);
```

## Step 7: Export DWG to PDF

마지막으로 `save` 메서드를 호출하여 DWG를 PDF로 내보냅니다.

```java
cadImage.save(outPath, exportOptions);
```

## Common Issues and Solutions

| Issue | Cause | Solution |
|-------|-------|----------|
| **No DGN underlay appears** | The DWG does not contain a `DGNUNDERLAY` entity. | Verify that the source DWG includes a DGN reference. |
| **PDF is blank** | Rasterization options set to zero size or wrong layout. | Ensure `setPageWidth`/`setPageHeight` are positive and `setLayouts` matches the DWG layout name. |
| **License exception** | Running without a valid Aspose.CAD license. | Apply a temporary or purchased license before calling any API methods. |

## Frequently Asked Questions

### Q1: Where can I find the documentation for Aspose.CAD for Java?

A1: The documentation can be found [here](https://reference.aspose.com/cad/java/).

### Q2: How can I download the Aspose.CAD library for Java?

A2: You can download the library from [this link](https://releases.aspose.com/cad/java/).

### Q3: Is there a free trial available for Aspose.CAD for Java?

A3: Yes, you can find the free trial [here](https://releases.aspose.com/).

### Q4: Where can I get a temporary license for Aspose.CAD for Java?

A4: Obtain a temporary license [here](https://purchase.aspose.com/temporary-license/).

### Q5: Need help or have questions?

A5: Visit the Aspose.CAD community support forum [here](https://forum.aspose.com/c/cad/19).

### Q6: Can I convert the resulting PDF back to DWG?

A6: The PDF is a raster preview; conversion back to DWG requires a separate reverse‑engineering tool.

### Q7: Does this approach work with other CAD formats like DWF or DXF?

A7: Yes, Aspose.CAD supports many formats; you only need to adjust the file extensions and rasterization settings accordingly.

---

**Last Updated:** 2026-01-10  
**Tested With:** Aspose.CAD for Java 24.11  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}