---
date: 2026-02-17
description: Java CAD 라이브러리 Aspose.CAD for Java가 DWG를 PDF 또는 래스터 이미지로 빠르고 정확하게 내보내는
  방법을 배워보세요.
linktitle: Export DWG to PDF or Raster
second_title: Aspose.CAD Java API
title: Java CAD 라이브러리 Aspose.CAD for Java를 사용하여 DWG를 PDF 또는 래스터로 내보내기
url: /ko/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# java cad library Aspose.CAD for Java를 사용하여 DWG를 PDF 또는 래스터로 내보내기

## 소개

컴퓨터 지원 설계(CAD)의 역동적인 세계에서 도면을 효율적으로 처리하는 것이 중요합니다. **java cad library** **Aspose.CAD for Java**를 사용하면 **export dwg to pdf** — 또는 래스터 이미지 — 를 몇 줄의 코드만으로 수행할 수 있습니다. 이 튜토리얼은 DWG 파일을 로드하고 고품질 PDF를 생성하는 전체 과정을 단계별로 안내하며, 왜 Aspose.CAD Java가 CAD 변환 작업에 가장 적합한 라이브러리인지 강조합니다.

## 빠른 답변
- **이 튜토리얼은 무엇을 다루나요?** Aspose.CAD for Java를 사용하여 DWG 파일을 PDF 또는 래스터 이미지로 내보내기.  
- **라이선스가 필요합니까?** 평가용으로 무료 임시 라이선스를 제공하며, 프로덕션에서는 정식 라이선스가 필요합니다.  
- **지원되는 Java 버전은?** 최신 Aspose.CAD Java API는 Java 8 이상 런타임에서 작동합니다.  
- **DWG를 다른 이미지 형식으로 변환할 수 있나요?** 예 — 동일한 래스터화 옵션을 사용하면 PNG, JPEG, BMP 등으로 출력할 수 있습니다.  
- **변환 시간은 얼마나 걸리나요?** 일반 도면은 보통 1초 미만이며, 큰 파일은 몇 초가 걸릴 수 있습니다.

## DWG 변환에 java cad library가 최고의 선택인 이유는?
- **Pure Java 구현** – 네이티브 DLL이나 외부 도구가 필요 없습니다.  
- **정확한 단위 처리** – 미터법과 영국식 단위가 자동으로 감지됩니다.  
- **고품질 래스터 출력** – 세밀하게 조정된 DPI와 페이지 크기 제어.  
- **전체 PDF 지원** – 추가 종속성 없이 벡터를 보존하는 PDF 생성.  
- **유연한 라이선스** – 테스트용 **temporary license aspose**로 시작하고, 실제 운영 시 업그레이드합니다.

## “export dwg to pdf”란 무엇인가요?
DWG를 PDF로 내보낸다는 것은 기본 AutoCAD 도면을 휴대 가능하고 장치에 독립적인 PDF 문서로 변환하는 것을 의미합니다. 생성된 PDF는 벡터 데이터, 레이어 및 스케일을 보존하므로 공유, 인쇄 또는 보관에 이상적입니다.

## 이 변환에 Aspose.CAD Java를 사용하는 이유는?
**java cad library**가 단위 변환부터 래스터화까지 모든 작업을 내부적으로 처리하기 때문에, 타사 도구의 복잡성을 피하고 플랫폼 간 일관된 결과를 얻을 수 있습니다.

## 전제 조건

코드에 들어가기 전에 다음이 준비되어 있는지 확인하십시오:

- Java 프로그래밍에 대한 기본 지식.  
- Aspose.CAD for Java 라이브러리가 설치되어 있어야 합니다. 아직 다운로드하지 않으셨다면 **[here](https://releases.aspose.com/cad/java/)**에서 받으세요.  
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

### Step 1: DWG 파일 로드

먼저 `Image` 클래스를 사용하여 DWG 도면을 로드합니다. 이렇게 하면 Aspose.CAD가 사용할 수 있는 메모리 내 표현이 생성됩니다.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String srcFile = dataDir + "Bottom_plate.dwg";
Image objImage = Image.load(srcFile);
```

### Step 2: 단위 유형 결정

도면이 미터법인지 영국식 단위인지 파악하는 것은 올바른 스케일링에 필수적입니다. 헬퍼 메서드 `IsMetric`(구현은 간략히 생략)은 부울 값을 반환합니다.

```java
Boolean currentUnitIsMetric = IsMetric(objImage.getUnitType());
int currentUnitCoefficient = objImage.getUnitType();
```

### Step 3: 래스터화 옵션 설정

단위 시스템에 따라 페이지 크기, 스케일 및 대상 단위 유형을 구성합니다. 이러한 옵션은 DWG가 PDF로 래핑되기 전에 어떻게 래스터화될지를 결정합니다.

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

### Step 4: PDF 옵션 구성 (pdf options cad)

`PdfOptions` 인스턴스를 생성하고 래스터화 설정을 연결합니다. 이를 통해 Aspose.CAD가 최종 PDF에 래스터화된 콘텐츠를 어떻게 삽입할지 지정합니다.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(new CadRasterizationOptions());
```

### Step 5: PDF로 저장

마지막으로 도면을 PDF 파일로 내보냅니다. `save` 메서드는 출력 경로와 구성된 `PdfOptions`를 인수로 받습니다.

```java
objImage.save(dataDir + "Saved.pdf", pdfOptions);
```

코드 실행이 끝나면 `DWGDrawings` 폴더에 **Saved.pdf**가 생성되어 배포하거나 보관할 수 있습니다.

## java cad library를 사용하여 dwg 래스터 이미지 변환 방법

PDF 대신 래스터 이미지가 필요하면 `PdfOptions`를 적절한 래스터 이미지 옵션(예: `PngOptions`, `JpegOptions`)으로 교체하면 됩니다. 동일한 `CadRasterizationOptions` 인스턴스를 재사용할 수 있어 최소한의 코드 변경으로 **convert dwg raster** 파일을 변환할 수 있습니다.

## pdf options cad를 사용하여 pdf dwg 생성 방법

위 예제는 이미 **generates pdf dwg** 출력을 보여줍니다. `pdfOptions`를 조정하면—예를 들어 `pdfOptions.setCompress(true)`를 설정하면—PDF 크기와 품질을 제어할 수 있습니다. 이는 **pdf options cad** API의 유연성을 보여줍니다.

## 일반적인 문제 및 팁

- **페이지 크기 오류** – 단위 변환 로직을 다시 확인하십시오; 계수가 맞지 않으면 페이지가 과도하게 커질 수 있습니다.  
- **글꼴 또는 라인웨이트 누락** – 변환 전에 DWG가 외부 리소스를 참조하고 있는지 확인하십시오.  
- **대형 도면의 성능** – 높은 품질이 필요할 때만 `CadRasterizationOptions`의 `DPI` 설정을 높이고, 낮은 DPI로 처리 속도를 높이세요.  
- **라이선스 문제** – 평가용으로 **temporary license aspose**를 사용할 수 있으며, 프로덕션 배포에는 정식 라이선스가 필요합니다.

## 자주 묻는 질문

**Q: Aspose.CAD for Java를 다른 Java 프레임워크와 함께 사용할 수 있나요?**  
A: 예, Aspose.CAD for Java는 Spring, Jakarta EE, Android와 같은 인기 있는 Java 프레임워크와 원활하게 통합됩니다.

**Q: Aspose.CAD for Java용 임시 라이선스를 제공하나요?**  
A: 예, 임시 라이선스는 **[here](https://purchase.aspose.com/temporary-license/)**에서 받을 수 있습니다.

**Q: Aspose.CAD for Java에 대한 지원은 어디서 받을 수 있나요?**  
A: 커뮤니티와 Aspose 엔지니어의 도움을 받으려면 **[Aspose.CAD forum](https://forum.aspose.com/c/cad/19)**를 방문하십시오.

**Q: Aspose.CAD for Java 라이선스는 어떻게 구매하나요?**  
A: 라이선스는 **[here](https://purchase.aspose.com/buy)**에서 구매할 수 있습니다.

**Q: Aspose.CAD for Java가 지원하는 단위는 무엇인가요?**  
A: Aspose.CAD for Java는 미터법과 영국식 단위를 모두 지원하며, 도면의 단위 시스템을 자동으로 감지합니다.

**Q: 동일한 API를 사용해 DWG를 다른 이미지 형식(PNG, JPEG 등)으로 변환할 수 있나요?**  
A: 물론입니다. `PdfOptions`를 적절한 래스터 이미지 옵션(예: `PngOptions`)으로 교체하고 동일한 `CadRasterizationOptions`를 재사용하면 됩니다.

## 결론

이 튜토리얼에서는 **java cad library** Aspose.CAD for Java를 사용하여 **export dwg to pdf** 및 래스터 이미지를 만드는 방법을 보여주었습니다. 단계별 가이드를 따라 하면 문서용 PDF든 웹 표시용 래스터 이미지든 신뢰할 수 있는 CAD 변환을 모든 Java 애플리케이션에 통합할 수 있습니다.

---

**마지막 업데이트:** 2026-02-17  
**테스트 환경:** Aspose.CAD for Java 24.10  
**작성자:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}