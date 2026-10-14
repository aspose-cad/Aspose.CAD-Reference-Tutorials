---
date: 2026-10-14
description: Java용 CAD 라이브러리 Aspose.CAD가 DWG를 PDF 또는 raster images로 빠르고 정확하게 내보내는
  방법을 알아보세요.
keywords:
- export dwg pdf
- high quality pdf
- dwg to pdf tutorial
- aspose cad java
- java cad library
lastmod: 2026-10-14
linktitle: DWG PDF 및 raster images 내보내기
og_description: Aspose.CAD for Java를 사용하여 DWG를 PDF로 빠르게 내보냅니다. 고품질 PDF 변환, raster
  options 및 라이선스에 대해 단계별 가이드를 확인하세요.
og_image_alt: Tutorial showing Java code to convert DWG drawings to PDF and raster
  formats with Aspose.CAD
og_title: Java CAD 라이브러리 Aspose.CAD를 사용하여 DWG를 PDF 및 raster images로 내보내기
schemas:
- author: Aspose
  dateModified: '2026-10-14'
  description: Learn how the Java CAD library Aspose.CAD for Java can export DWG to
    PDF or raster images quickly and accurately.
  headline: Export DWG PDF and raster images using Java CAD library Aspose.CAD
  type: TechArticle
- description: Learn how the Java CAD library Aspose.CAD for Java can export DWG to
    PDF or raster images quickly and accurately.
  name: Export DWG PDF and raster images using Java CAD library Aspose.CAD
  steps:
  - name: Load the DWG file
    text: First, load your DWG drawing using the `Image` class. This creates an in‑memory
      representation that Aspose.CAD can work with.
  - name: Determine unit type
    text: Understanding whether the drawing uses metric or imperial units is essential
      for correct scaling. The helper method `IsMetric` (implementation omitted for
      brevity) returns a boolean flag.
  - name: Set rasterization options
    text: The `CadRasterizationOptions` class defines rasterization parameters such
      as DPI, page size, and unit conversion. Based on the unit system, configure
      page size, scaling, and the target unit type. These options drive how the DWG
      is rasterized before being wrapped into a PDF.
  - name: Configure PDF options (pdf options cad)
    text: The `PdfOptions` class specifies PDF‑specific settings, including compression
      and metadata. Create a `PdfOptions` instance and attach the rasterization settings.
      This tells Aspose.CAD how to embed the rasterized content into the final PDF.
  - name: Save as PDF
    text: The `save` method writes the image to the given file path using the supplied
      options. Finally, export the drawing to a PDF file. The `save` method takes
      the output path and the configured `PdfOptions`. When the code finishes, you’ll
      find **Saved.pdf** in your `DWGDrawings` folder, ready for distribu
  type: HowTo
- questions:
  - answer: Yes, Aspose.CAD for Java seamlessly integrates with popular Java frameworks
      such as Spring, Jakarta EE, and Android.
    question: Can I use Aspose.CAD for Java with other Java frameworks?
  - answer: Yes, you can obtain a temporary license **[obtain a temporary license](https://purchase.aspose.com/temporary-license/)**.
    question: Is a temporary license available for Aspose.CAD for Java?
  - answer: Visit the **[Aspose.CAD forum](https://forum.aspose.com/c/cad/19)** for
      assistance from the community and Aspose engineers.
    question: Where can I find support for Aspose.CAD for Java?
  - answer: You can purchase a license **[purchase a license](https://purchase.aspose.com/buy)**.
    question: How can I purchase a license for Aspose.CAD for Java?
  - answer: Aspose.CAD for Java supports both metric and imperial units, automatically
      detecting the drawing’s unit system.
    question: What units does Aspose.CAD for Java support?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- export dwg
- aspose.cad
- java cad conversion
title: Java CAD 라이브러리 Aspose.CAD를 사용하여 DWG를 PDF 및 raster images로 내보내기
url: /ko/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java CAD 라이브러리 Aspose.CAD를 사용하여 DWG PDF 및 래스터 이미지 내보내기

## 소개

DWG를 PDF로 내보내는 것은 엔지니어, 건축가 및 네이티브 파일 형식을 노출하지 않고 CAD 도면을 공유해야 하는 모든 사람에게 자주 요구되는 작업입니다. **Aspose.CAD for Java**를 사용하면 **export dwg pdf** — 또는 래스터 이미지 — 를 Java 코드 몇 줄만으로 수행할 수 있으며, 벡터 정확도와 레이아웃 정밀도를 유지합니다. 이 튜토리얼에서는 DWG 파일을 로드하고, 래스터화 설정을 구성한 다음, 결과를 고품질 PDF 또는 이미지로 저장하는 과정을 단계별로 안내합니다. 또한 Aspose.CAD가 신뢰할 수 있는 크로스‑플랫폼 변환을 위해 선호되는 Java CAD 라이브러리인 이유도 확인할 수 있습니다.

PDF 변환에만 집중된 가이드를 보려면 [Export DWG to PDF tutorial](/java/cad-drawing-conversion/export-dwg-to-pdf/)를 참조하세요.

## 빠른 답변
- **이 튜토리얼은 무엇을 다루나요?** Aspose.CAD for Java를 사용하여 DWG 파일을 PDF 또는 래스터 이미지로 내보내기.  
- **라이선스가 필요합니까?** 평가용으로 무료 임시 라이선스를 사용할 수 있으며, 프로덕션에서는 정식 라이선스가 필요합니다.  
- **지원되는 Java 버전은?** 최신 Aspose.CAD Java API는 Java 8 이상 런타임에서 작동합니다.  
- **DWG를 다른 이미지 형식으로 변환할 수 있나요?** 예 – 동일한 래스터화 옵션을 사용하면 PNG, JPEG, BMP 등으로 출력할 수 있습니다.  
- **변환 시간은 얼마나 걸리나요?** 일반 도면은 보통 1초 미만이며, 큰 파일은 몇 초가 걸릴 수 있습니다.

## Java CAD 라이브러리가 DWG 변환에 최적의 선택인 이유

Aspose.CAD for Java가 최적의 선택인 이유는 네이티브 DLL이 필요 없는 순수 Java 구현을 제공하고, 미터법 또는 임페리얼 단위를 자동으로 감지하며, 최대 1200 DPI의 래스터 출력을 제공하고, 외부 종속성 없이 벡터를 보존하는 PDF를 생성하기 때문입니다. 또한 이 라이브러리는 임시 라이선스로 시작하여 엔터프라이즈 규모로 확장할 수 있는 유연한 라이선스 모델을 제공합니다.

## “export dwg to pdf”란 무엇인가요?

`Export dwg pdf`는 네이티브 DWG 도면 파일을 벡터 데이터, 레이어 및 스케일을 유지하면서 PDF 문서로 변환하는 과정입니다. 이 변환은 장치에 독립적인 파일을 생성하여 AutoCAD 없이도 모든 플랫폼에서 볼 수 있습니다. PDF가 벡터 정보를 유지하기 때문에 텍스트는 검색 가능하고 그래픽은 어떤 확대 수준에서도 선명하게 유지되어 문서화, 클라이언트 검토 및 보관에 이상적입니다.

## 이 변환에 Aspose.CAD Java를 사용해야 하는 이유

Aspose.CAD Java를 사용해야 하는 이유는 라이브러리가 단위 변환, 래스터화 및 PDF 삽입을 내부적으로 처리하여 서드파티 도구나 복잡한 명령줄 파이프라인이 필요 없기 때문입니다. API는 개발자를 위해 설계되었으며, 단일 `Image` 객체가 도면을 나타내고 몇 개의 구성 객체를 통해 DPI, 페이지 크기 및 압축을 세밀하게 조정할 수 있습니다. 결과적으로 Windows, Linux, macOS 환경 전반에 걸쳐 일관되고 재현 가능한 출력이 제공됩니다.

## 사전 요구 사항

- Java 프로그래밍에 대한 기본 지식.  
- Aspose.CAD for Java 라이브러리가 설치되어 있어야 합니다. 아직 다운로드하지 않았다면 **[download Aspose.CAD for Java](https://releases.aspose.com/cad/java/)**를 받으세요.  
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

### 단계 1: DWG 파일 로드

먼저 `Image` 클래스를 사용하여 DWG 도면을 로드합니다. 이렇게 하면 Aspose.CAD가 작업할 수 있는 메모리 내 표현이 생성됩니다.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String srcFile = dataDir + "Bottom_plate.dwg";
Image objImage = Image.load(srcFile);
```

### 단계 2: 단위 유형 결정

도면이 미터법인지 임페리얼 단위인지를 파악하는 것은 올바른 스케일링을 위해 필수적입니다. 헬퍼 메서드 `IsMetric`(구현은 간략히 생략)은 부울 값을 반환합니다.

```java
Boolean currentUnitIsMetric = IsMetric(objImage.getUnitType());
int currentUnitCoefficient = objImage.getUnitType();
```

### 단계 3: 래스터화 옵션 설정

`CadRasterizationOptions` 클래스는 DPI, 페이지 크기 및 단위 변환과 같은 래스터화 매개변수를 정의합니다. 단위 시스템에 따라 페이지 크기, 스케일링 및 대상 단위 유형을 구성합니다. 이러한 옵션은 DWG가 PDF로 래핑되기 전에 어떻게 래스터화되는지를 결정합니다.

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

### 단계 4: PDF 옵션 구성 (pdf options cad)

`PdfOptions` 클래스는 압축 및 메타데이터를 포함한 PDF 전용 설정을 지정합니다. `PdfOptions` 인스턴스를 생성하고 래스터화 설정을 연결합니다. 이를 통해 Aspose.CAD에 래스터화된 콘텐츠를 최종 PDF에 어떻게 삽입할지 알려줍니다.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(new CadRasterizationOptions());
```

### 단계 5: PDF로 저장

`save` 메서드는 제공된 옵션을 사용하여 이미지를 지정된 파일 경로에 기록합니다. 마지막으로 도면을 PDF 파일로 내보냅니다. `save` 메서드는 출력 경로와 구성된 `PdfOptions`를 인수로 받습니다.

```java
objImage.save(dataDir + "Saved.pdf", pdfOptions);
```

코드 실행이 완료되면 `DWGDrawings` 폴더에 **Saved.pdf**가 생성되어 배포 또는 보관에 사용할 수 있습니다.

## Java CAD 라이브러리를 사용하여 DWG 래스터 이미지를 변환하는 방법

`PdfOptions`를 `PngOptions` 또는 `JpegOptions`와 같은 래스터 전용 옵션 클래스로 교체하면 DWG를 래스터 형식으로 변환할 수 있습니다. 동일한 `CadRasterizationOptions` 인스턴스를 재사용하고 출력 형식을 조정한 뒤, 새로운 옵션 객체와 함께 `save` 메서드를 호출합니다. 이 방법을 사용하면 한 줄만 바꾸어 PNG, JPEG, BMP 또는 TIFF 파일을 생성할 수 있어 워크플로우가 일관됩니다.

## PDF 옵션 CAD를 사용하여 PDF DWG를 생성하는 방법

위 예제는 이미 **pdf dwg** 출력을 **생성**합니다. PDF 크기를 미세 조정하려면 `pdfOptions.setCompress(true)`를 호출하여 압축을 활성화하세요. 또한 추가 `PdfOptions` 속성을 통해 사용자 정의 메타데이터를 삽입하거나 PDF 버전을 설정하고, 비밀번호 보호를 추가할 수 있습니다. 이러한 조정으로 Java 코드베이스를 떠나지 않고 최종 PDF를 완전히 제어할 수 있습니다.

## 일반적인 문제 및 팁

- **페이지 크기 오류** – 단위 변환 로직을 다시 확인하세요; 계수가 일치하지 않으면 페이지가 과도하게 커질 수 있습니다.  
- **폰트 또는 라인웨이트 누락** – 변환 전에 DWG가 외부 리소스를 참조하고 있는지 확인하세요.  
- **대형 도면 성능** – 높은 품질이 필요할 때만 `CadRasterizationOptions`의 `DPI` 설정을 높이고, 낮은 DPI로 처리 속도를 높이세요.  
- **라이선스 문제** – 평가용으로 **temporary license Aspose**를 사용할 수 있으며, 프로덕션 배포에는 정식 라이선스가 필요합니다.

## 자주 묻는 질문

**Q: Aspose.CAD for Java를 다른 Java 프레임워크와 함께 사용할 수 있나요?**  
A: 예, Aspose.CAD for Java는 Spring, Jakarta EE, Android와 같은 인기 있는 Java 프레임워크와 원활하게 통합됩니다.

**Q: Aspose.CAD for Java에 임시 라이선스가 제공되나요?**  
A: 예, 임시 라이선스는 **[obtain a temporary license](https://purchase.aspose.com/temporary-license/)**에서 얻을 수 있습니다.

**Q: Aspose.CAD for Java 지원을 어디서 찾을 수 있나요?**  
A: 커뮤니티와 Aspose 엔지니어의 도움을 받으려면 **[Aspose.CAD forum](https://forum.aspose.com/c/cad/19)**를 방문하세요.

**Q: Aspose.CAD for Java 라이선스는 어떻게 구매하나요?**  
A: 라이선스는 **[purchase a license](https://purchase.aspose.com/buy)**에서 구매할 수 있습니다.

**Q: Aspose.CAD for Java가 지원하는 단위는 무엇인가요?**  
A: Aspose.CAD for Java는 미터법과 임페리얼 단위를 모두 지원하며, 도면의 단위 시스템을 자동으로 감지합니다.

**Q: 동일한 API를 사용하여 DWG를 다른 이미지 형식(PNG, JPEG 등)으로 변환할 수 있나요?**  
A: 물론입니다. `PdfOptions`를 적절한 래스터 이미지 옵션(예: `PngOptions`)으로 교체하고 동일한 `CadRasterizationOptions`를 재사용하면 됩니다.

## 결론

이 튜토리얼에서는 **java cad library** Aspose.CAD for Java를 사용하여 **export dwg pdf** 및 래스터 이미지를 내보내는 방법을 보여주었습니다. 단계별 가이드를 따라 하면 문서용 PDF든 웹 표시용 래스터 이미지든 신뢰할 수 있는 CAD 변환을 모든 Java 애플리케이션에 통합할 수 있습니다. 라이브러리의 순수 Java 특성, 고품질 출력 및 유연한 라이선스 모델은 소규모 유틸리티와 대규모 엔터프라이즈 파이프라인 모두에 적합한 선택입니다.

---

**Last Updated:** 2026-10-14  
**Tested With:** Aspose.CAD for Java 24.10  
**Author:** Aspose

## 관련 튜토리얼

- [Aspose.CAD for Java를 사용한 특정 레이아웃으로 DWG를 PDF로 내보내기](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)
- [Java에서 DWG를 PDF로 내보내기 – Aspose.CAD로 PDF 페이지 크기 설정](/cad/java/cad-export-options/export-to-pdf/)
- [숨은 선을 포함한 DWG를 PDF로 내보내기 – Aspose.CAD for Java](/cad/java/cad-text-and-formatting/support-hidden-lines-in-dwg/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}