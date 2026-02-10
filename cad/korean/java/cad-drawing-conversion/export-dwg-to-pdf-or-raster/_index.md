---
date: 2025-12-18
description: Aspose.CAD를 사용하여 Java에서 DWG를 PDF 또는 래스터 이미지로 내보내는 방법을 살펴보세요. 이 단계별 가이드는
  DWG 파일의 정밀도, 효율성 및 손쉬운 변환을 보장합니다.
linktitle: Export DWG to PDF or Raster
second_title: Aspose.CAD Java API
title: Aspose.CAD for Java를 사용하여 DWG를 PDF 또는 래스터로 내보내기
url: /ko/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD for Java를 사용한 DWG를 PDF 또는 래스터로 내보내기

## 소개

컴퓨터 지원 설계(CAD)의 역동적인 세계에서 도면을 효율적으로 다루는 것은 매우 중요합니다. **Aspose.CAD for Java**를 사용하면 **export dwg to pdf** — 또는 래스터 이미지 — 를 몇 줄의 코드만으로 수행할 수 있습니다. 이 튜토리얼에서는 DWG 파일을 로드하고 고품질 PDF를 생성하는 전체 과정을 단계별로 안내하며, CAD 변환 작업에 Aspose.CAD Java가 왜 최고의 라이브러리인지 강조합니다.

## 빠른 답변
- **이 튜토리얼에서는 무엇을 다루나요?** Aspose.CAD for Java를 사용한 DWG 파일을 PDF 또는 래스터 이미지로 내보내는 방법.  
- **라이선스가 필요합니까?** 평가용으로 무료 임시 라이선스를 제공하며, 프로덕션에서는 정식 라이선스가 필요합니다.  
- **지원되는 Java 버전은?** 최신 Aspose.CAD Java API는 Java 8+ 런타임에서 모두 작동합니다.  
- **DWG를 다른 이미지 형식으로 변환할 수 있나요?** 예 – 동일한 래스터화 옵션을 사용해 PNG, JPEG, BMP 등으로 출력할 수 있습니다.  
- **변환에 걸리는 시간은?** 일반적인 도면은 1초 미만, 큰 파일은 몇 초 정도 소요됩니다.

## “export dwg to pdf”란 무엇인가요?
DWG를 PDF로 내보낸다는 것은 기본 AutoCAD 도면을 휴대 가능하고 장치에 독립적인 PDF 문서로 변환하는 것을 의미합니다. 결과 PDF는 벡터 데이터, 레이어 및 스케일을 보존하므로 공유, 인쇄 또는 보관에 이상적입니다.

## 이 변환에 Aspose.CAD Java를 사용하는 이유는?
- **외부 종속성 없음** – 순수 Java이며 네이티브 DLL이 필요 없습니다.  
- **정확한 단위 처리** – 미터법 또는 임페리얼 단위를 자동으로 인식합니다.  
- **고품질 래스터 출력** – DPI 및 페이지 크기 제어가 세밀하게 조정됩니다.  
- **전체 PDF 지원** – 추가 라이브러리 없이 벡터를 보존하는 PDF 생성이 가능합니다.

## 전제 조건

코드 작성을 시작하기 전에 다음을 준비하세요:

- Java 프로그래밍에 대한 기본 지식.  
- Aspose.CAD for Java 라이브러리가 설치되어 있어야 합니다. 아직 다운로드하지 않으셨다면 **[여기](https://releases.aspose.com/cad/java/)**에서 받으세요.  
- 테스트용 DWG 파일 – 이 가이드에서는 샘플 **Bottom_plate.dwg**를 사용합니다.

## 네임스페이스 가져오기

Java 프로젝트에서 변환을 시작하기 위해 필요한 클래스를 가져옵니다:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.UnitType;
```

## 단계별 가이드

### Step 1: Load the DWG File

먼저 `Image` 클래스를 사용해 DWG 도면을 로드합니다. 이렇게 하면 Aspose.CAD가 작업할 수 있는 메모리 내 표현이 생성됩니다.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String srcFile = dataDir + "Bottom_plate.dwg";
Image objImage = Image.load(srcFile);
```

### Step 2: Determine Unit Type

도면이 미터법인지 임페리얼인지 파악하는 것이 올바른 스케일링에 필수적입니다. 헬퍼 메서드 `IsMetric`(구현은 생략) 은 boolean 플래그를 반환합니다.

```java
Boolean currentUnitIsMetric = IsMetric(objImage.getUnitType());
int currentUnitCoefficient = objImage.getUnitType();
```

### Step 3: Set Rasterization Options

단위 시스템에 따라 페이지 크기, 스케일 및 목표 단위 유형을 설정합니다. 이러한 옵션은 DWG가 PDF에 포함되기 전에 래스터화되는 방식을 결정합니다.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();

if (currentUnitIsMetric) {
    // Metric units
    double metersCoeff = 1 / 1000.0;
    double scaleFactor = metersCoeff / currentUnitCoefficient;
    rasterizationOptions.setPageWidth((float)(210 * scaleFactor));
    rasterizationOptions.setPageHeight((float)(297 * scaleFactor));
    rasterizationOptions.setUnitType(UnitType.Millimeter);
} else {
    // Imperial units
    rasterizationOptions.setPageWidth((float)(8.27f / currentUnitCoefficient));
    rasterizationOptions.setPageHeight((float)(11.69f / currentUnitCoefficient));
    rasterizationOptions.setUnitType(UnitType.Inch);
}
```

### Step 4: Configure PDF Options

`PdfOptions` 인스턴스를 생성하고 래스터화 설정을 연결합니다. 이를 통해 Aspose.CAD가 최종 PDF에 래스터화된 콘텐츠를 삽입하는 방법을 지정합니다.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(new CadRasterizationOptions());
```

### Step 5: Save as PDF

마지막으로 도면을 PDF 파일로 내보냅니다. `save` 메서드는 출력 경로와 구성된 `PdfOptions` 를 인수로 받습니다.

```java
objImage.save(dataDir + "Saved.pdf", pdfOptions);
```

코드 실행이 완료되면 `DWGDrawings` 폴더에 **Saved.pdf** 가 생성되어 배포 또는 보관에 바로 사용할 수 있습니다.

## 일반적인 문제 및 팁

- **페이지 크기 오류** – 단위 변환 로직을 다시 확인하세요; 계수가 맞지 않으면 페이지가 과도하게 커질 수 있습니다.  
- **글꼴 또는 라인웨이트 누락** – 변환 전에 DWG가 외부 리소스를 참조하고 있는지 확인하세요.  
- **대형 도면의 성능** – 높은 품질이 필요할 때만 `CadRasterizationOptions` 의 `DPI` 값을 높이고, 처리 속도를 위해서는 낮은 DPI 를 사용하세요.

## 자주 묻는 질문

**Q: Aspose.CAD for Java를 다른 Java 프레임워크와 함께 사용할 수 있나요?**  
A: 예, Aspose.CAD for Java는 Spring, Jakarta EE, Android 등 인기 있는 Java 프레임워크와 원활하게 통합됩니다.

**Q: Aspose.CAD for Java용 임시 라이선스를 받을 수 있나요?**  
A: 예, 임시 라이선스는 **[여기](https://purchase.aspose.com/temporary-license/)**에서 얻을 수 있습니다.

**Q: Aspose.CAD for Java에 대한 지원은 어디서 받을 수 있나요?**  
A: 커뮤니티와 Aspose 엔지니어의 도움을 받으려면 **[Aspose.CAD 포럼](https://forum.aspose.com/c/cad/19)**을 방문하세요.

**Q: Aspose.CAD for Java 라이선스는 어떻게 구매하나요?**  
A: 라이선스는 **[여기](https://purchase.aspose.com/buy)**에서 구매할 수 있습니다.

**Q: Aspose.CAD for Java가 지원하는 단위는 무엇인가요?**  
A: Aspose.CAD for Java는 미터법과 임페리얼 단위를 모두 지원하며, 도면의 단위 시스템을 자동으로 감지합니다.

**Q: 동일한 API로 DWG를 다른 이미지 형식(PNG, JPEG 등)으로 변환할 수 있나요?**  
A: 물론입니다. `PdfOptions` 대신 해당 래스터 이미지 옵션(예: `PngOptions`)을 사용하고 동일한 `CadRasterizationOptions` 를 재사용하면 됩니다.

## 결론

이 튜토리얼에서는 Aspose.CAD for Java를 사용해 **export dwg to pdf** 및 래스터 이미지를 만드는 방법을 보여주었습니다. 단계별 가이드를 따라 하면 PDF 문서가 필요하거나 웹에 표시할 래스터 이미지가 필요한 경우에도 신뢰할 수 있는 CAD 변환 기능을 Java 애플리케이션에 손쉽게 통합할 수 있습니다.

---

**마지막 업데이트:** 2025-12-18  
**테스트 환경:** Aspose.CAD for Java 24.10  
**작성자:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}