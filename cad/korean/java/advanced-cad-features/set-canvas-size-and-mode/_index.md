---
date: 2026-08-29
description: Aspose.CAD for Java를 사용하여 pdf 페이지 크기를 설정하고 CAD를 PDF로 변환하는 방법을 배우세요. automatic
  layout scaling 및 TIFF export를 지원합니다.
keywords:
- set pdf page size
- convert cad to pdf
- canvas size java
- high resolution tiff
- change pdf dimensions
lastmod: 2026-08-29
linktitle: pdf 페이지 크기 설정 – cad를 pdf로 변환
og_description: Aspose.CAD를 사용하여 Java에서 CAD 도면을 PDF로 변환하면서 pdf 페이지 크기를 설정하는 방법을 배우세요.
  이 가이드는 canvas dimensions, automatic layout scaling, 그리고 high‑resolution TIFF 내보내기를
  다룹니다.
og_image_alt: Tutorial showing how to set pdf page size and convert CAD to PDF in
  Java
og_title: pdf 페이지 크기 설정 – Aspose와 Java를 사용해 CAD를 PDF로 변환
schemas:
- author: Aspose
  dateModified: '2026-08-29'
  description: Learn how to set pdf page size and convert CAD to PDF using Aspose.CAD
    for Java, with automatic layout scaling and TIFF export.
  headline: Set pdf page size – convert cad to pdf (Java)
  type: TechArticle
- questions:
  - answer: No. Canvas size controls page dimensions; vector data remains resolution‑independent,
      ensuring crisp rendering at any zoom level.
    question: does the canvas size affect vector quality in the PDF?
  - answer: Yes. Adjust `rasterizationOptions.setResolution(dpiValue)` before creating
      `TiffOptions`.
    question: can I set a different DPI for the TIFF output?
  - answer: Use Aspose.PDF to load the generated PDF and call `pdf.getPages().setPageSize(PageSize.A4)`
      or a custom size.
    question: how can I change PDF dimensions for an existing PDF without re‑rendering
      the CAD?
  - answer: Keep `setAutomaticLayoutsScaling(true)` and avoid `setNoScaling(true)`;
      this retains layer visibility and layout fidelity.
    question: what is the best way to convert dxf to pdf while preserving layers?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- set pdf page size
- convert cad
- Aspose.CAD
- Java
- high resolution tiff
title: pdf 페이지 크기 설정 – cad를 pdf로 변환 (Java)
url: /ko/java/advanced-cad-features/set-canvas-size-and-mode/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# pdf 페이지 크기 설정 – CAD를 PDF로 변환 (Java)

## 소개

CAD 도면을 PDF로 변환하면서 **pdf 페이지 크기 설정**이 필요하다면, 올바른 곳에 오셨습니다. 이 튜토리얼에서는 Aspose.CAD for Java를 사용하여 정확한 캔버스 크기를 정의하고, 자동 레이아웃 스케일링을 활성화한 다음 결과를 PDF와 TIFF 모두로 내보내는 방법을 보여드립니다. 인쇄용 엔지니어링 도면을 준비하든 웹 갤러리를 위한 썸네일을 생성하든, 페이지 크기와 출력 해상도를 제어하는 ​​것은 필수적입니다.

## 빠른 답변
- **“convert CAD to PDF”가 의미하는 바는?** CAD 도면(예: DXF, DWG)을 모든 플랫폼에서 볼 수 있는 PDF 문서로 변환하는 것입니다.  
- **TIFF로도 내보낼 수 있나요?** 예—`TiffOptions`를 사용하여 고해상도 래스터 이미지를 생성합니다.  
- **Java에서 캔버스 크기를 제어하는 옵션은?** `CadRasterizationOptions.setPageWidth/Height`.  
- **자동 레이아웃 스케일링이란?** 캔버스 크기가 변경될 때 원래 레이아웃 비율을 유지하는 플래그(`setAutomaticLayoutsScaling(true)`).  
- **Aspose.CAD에 라이선스가 필요합니까?** 프로덕션 사용을 위해 임시 또는 영구 라이선스가 필요합니다.

## Java에서 CAD를 PDF로 변환할 때 pdf 페이지 크기 설정 방법

CAD 파일을 로드하고, 원하는 너비와 높이로 `CadRasterizationOptions`를 구성한 다음 자동 레이아웃 스케일링을 활성화하고 결과를 PDF로 저장합니다. 이 두 단계 접근 방식은 벡터 품질을 손상시키지 않으면서 출력 페이지의 정확한 치수를 제어할 수 있게 해줍니다.

## CAD를 PDF로 변환한다는 것은 무엇인가요?

CAD를 PDF로 변환한다는 것은 벡터 기반 엔지니어링 도면을 PDF 페이지로 렌더링하여 선 작업, 레이어 및 기하학을 보존하면서 파일을 보편적으로 접근 가능하게 만드는 것을 의미합니다. 이 과정은 지정된 옵션에 따라 도면을 래스터화하여 CAD 소프트웨어 없이도 모든 장치에서 열 수 있는 PDF를 생성하고, 원본 디자인의 시각적 충실도를 유지합니다.

## Java에서 캔버스 크기를 설정하는 이유

Java에서 캔버스 크기를 설정하면 출력 해상도와 페이지 치수를 정의할 수 있어 생성된 PDF 또는 TIFF가 인쇄 또는 디스플레이 요구 사항에 맞도록 보장합니다. 또한 스케일링 동작을 제어할 수 있어 대형 도면에 필수적입니다.

## 전제 조건

튜토리얼을 시작하기 전에 다음 전제 조건이 준비되어 있는지 확인하십시오:

- Aspose.CAD for Java: Aspose.CAD 라이브러리가 Java 환경에 설치되어 있는지 확인하십시오. Aspose.CAD for Java 라이브러리는 [here](https://releases.aspose.com/cad/java/)에서 다운로드할 수 있습니다.
- Document directory: CAD 파일을 저장할 문서 디렉터리를 설정하십시오. 이 디렉터리는 튜토리얼 단계에서 참조됩니다.

이제 단계별 가이드를 시작해 보겠습니다.

## 네임스페이스 가져오기

이 단계에서는 Aspose.CAD 프로젝트를 시작하기 위해 필요한 네임스페이스를 가져옵니다.

`Image`는 CAD 파일을 로드하는 데 사용되는 주요 클래스입니다.

```java
import java.awt.Image;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

## 단계 1: Aspose.CAD 클래스 가져오기

`Image` 클래스는 CAD 도면을 로드하고 저장하는 메서드를 제공합니다.

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";

String srcFile = dataDir + "conic_pyramid.dxf";
com.aspose.cad.Image objImage = com.aspose.cad.Image.load(srcFile);
```

이 스니펫에서는 리소스 디렉터리 경로를 설정하고 Aspose.CAD의 `Image` 클래스를 사용하여 DXF 파일을 로드합니다.

## 단계 2: CadRasterizationOptions 속성 설정 (set canvas size java)

`CadRasterizationOptions`는 CAD‑to‑raster 변환을 위한 페이지 크기 및 스케일링과 같은 래스터화 설정을 지정합니다.

```java
// Create an instance of CadRasterizationOptions and set its various properties
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);

rasterizationOptions.setAutomaticLayoutsScaling(true);
rasterizationOptions.setNoScaling(true);
```

여기서는 `CadRasterizationOptions` 인스턴스를 생성하고 페이지 너비, 페이지 높이 및 **automatic layout scaling**과 같은 속성을 구성합니다. 이는 변환을 위한 **configure canvas mode**의 핵심입니다.

## 단계 3: PdfOptions 생성 및 vectorRasterizationOptions 설정

`PdfOptions`는 변환을 위한 PDF 출력 설정을 정의합니다.

```java
// Create an instance of PdfOptions
PdfOptions pdfOptions = new PdfOptions();

// Set the VectorRasterizationOptions property
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

이제 `PdfOptions` 인스턴스를 생성하고 `VectorRasterizationOptions` 속성을 이전에 구성한 `CadRasterizationOptions`로 설정합니다.

## 단계 4: PDF로 내보내기 (convert CAD to PDF)

```java
// Export CAD to PDF
objImage.save(dataDir + "result_out_.pdf", pdfOptions);
```

마지막으로 지정된 옵션을 사용하여 CAD 이미지를 PDF 파일로 저장하고 **convert CAD to PDF** 프로세스를 완료합니다.

## 단계 5: TiffOptions 생성 및 vectorRasterizationOptions 설정 (export CAD to TIFF)

`TiffOptions`는 압축 및 해상도와 같은 TIFF 출력 매개변수를 구성합니다.

```java
// Create an instance of TiffOptions
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);

// Set the VectorRasterizationOptions property
tiffOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## 단계 6: TIFF로 내보내기

```java
// Export CAD to TIFF
objImage.save(dataDir + "result_out_.tiff", tiffOptions);
```

마지막으로 지정된 옵션을 사용하여 CAD 이미지를 TIFF 파일로 저장하고 캔버스 크기를 구성한 후 **export CAD to TIFF** 방법을 보여줍니다.

## 일반적인 문제 및 해결책

| 문제 | 원인 | 해결 방법 |
|-------|-------|-----|
| 출력 PDF가 비어 있음 | `setNoScaling(true)`가 일부 도면의 렌더링을 비활성화함 | `setNoScaling(true)`를 제거하거나 `false`로 설정합니다. |
| TIFF 해상도가 낮게 보임 | 페이지 너비/높이가 너무 작음 | `setPageWidth` / `setPageHeight` 값을 늘립니다. |
| 레이아웃이 왜곡됨 | 자동 레이아웃 스케일링이 비활성화됨 | `setAutomaticLayoutsScaling(true)`가 활성화되어 있는지 확인합니다. |

## 캔버스 크기와 DPI를 조정하는 이유

캔버스 크기를 변경하면 출력의 래스터화 해상도에 직접적인 영향을 줍니다. **TIFF 해상도를 높여야** 하는 경우, `TiffOptions`를 만들기 전에 `setPageWidth` / `setPageHeight` 값을 올리거나 `rasterizationOptions.setResolution(300)`을 호출하면 됩니다. 이를 통해 인쇄 또는 상세 검토에 적합한 고품질 래스터 이미지를 얻을 수 있습니다.

## 자주 묻는 질문

**Q1: Aspose.CAD for Java를 다른 Java 프레임워크와 함께 사용할 수 있나요?**  
A: 예, Aspose.CAD는 다양한 Java 프레임워크와 원활하게 통합되도록 설계되었습니다.

**Q2: Aspose.CAD에 대한 임시 라이선스를 제공하나요?**  
A: 예, 임시 라이선스 페이지는 [here](https://purchase.aspose.com/temporary-license/)에서 얻을 수 있습니다.

**Q3: Aspose.CAD에 대한 커뮤니티 지원은 어디서 받을 수 있나요?**  
A: 커뮤니티 지원 및 토론은 Aspose.CAD 포럼 [Aspose.CAD forum](https://forum.aspose.com/c/cad/19)에서 확인하십시오.

**Q4: Aspose.CAD를 무료로 체험할 수 있나요?**  
A: 물론입니다! 무료 체험 다운로드 페이지는 [here](https://releases.aspose.com/)에서 확인하세요.

**Q5: Aspose.CAD for Java를 어떻게 구매하나요?**  
A: Aspose.CAD for Java 구매는 [here](https://purchase.aspose.com/buy)에서 가능합니다.

**추가 Q&A**

**Q: 캔버스 크기가 PDF의 벡터 품질에 영향을 미치나요?**  
A: 아니요. 캔버스 크기는 페이지 치수를 제어할 뿐이며, 벡터 데이터는 해상도에 독립적이어서 어떤 확대 수준에서도 선명하게 렌더링됩니다.

**Q: TIFF 출력에 다른 DPI를 설정할 수 있나요?**  
A: 예. `TiffOptions`를 만들기 전에 `rasterizationOptions.setResolution(dpiValue)`를 조정하면 됩니다.

**Q: CAD를 다시 렌더링하지 않고 기존 PDF의 페이지 크기를 변경하려면 어떻게 해야 하나요?**  
A: Aspose.PDF를 사용하여 생성된 PDF를 로드하고 `pdf.getPages().setPageSize(PageSize.A4)` 또는 사용자 정의 크기를 호출합니다.

**Q: 레이어를 보존하면서 DXF를 PDF로 변환하는 가장 좋은 방법은 무엇인가요?**  
A: `setAutomaticLayoutsScaling(true)`를 유지하고 `setNoScaling(true)`를 피하면 레이어 가시성과 레이아웃 충실도를 유지할 수 있습니다.

## 결론

축하합니다! **convert CAD to PDF**와 **export CAD to TIFF**를 성공적으로 수행했으며 **set canvas size java**를 적용하고 **automatic layout scaling**을 활성화했으며 고품질 출력을 위한 **configure canvas mode** 방법을 배웠습니다. 이 튜토리얼은 CAD 변환 프로젝트를 위한 탄탄한 기반을 제공합니다. 더 많은 기능과 가능성은 [Aspose.CAD documentation](https://reference.aspose.com/cad/java/)에서 확인하세요.

---

**마지막 업데이트:** 2026-08-29  
**테스트 환경:** Aspose.CAD for Java 24.12  
**작성자:** Aspose

## 관련 튜토리얼

- [캔버스 크기 설정 – Aspose.CAD for Java 고급 CAD 기능](/cad/java/advanced-cad-features/)
- [Java에서 DWG를 PDF로 내보내기 – Aspose.CAD로 PDF 페이지 크기 설정](/cad/java/cad-export-options/export-to-pdf/)
- [맞춤 페이지 크기 설정 – 자동 레이아웃 스케일링을 사용한 CAD에서 PDF](/cad/java/advanced-cad-features/setting-auto-layout-scaling/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}