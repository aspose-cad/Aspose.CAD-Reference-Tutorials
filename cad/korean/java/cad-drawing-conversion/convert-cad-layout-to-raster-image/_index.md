---
date: 2026-10-04
description: Aspose.CAD for Java를 사용하여 DWG를 PNG로 빠르게 변환하고 CAD를 PNG 또는 기타 래스터 형식으로
  내보내는 방법을 배웁니다. 고품질 결과를 신속하게 얻으세요.
keywords:
- convert dwg to png
- dwg to raster image
- convert cad to pdf
- export cad as png
- convert dwg to jpeg
lastmod: 2026-10-04
linktitle: CAD 레이아웃을 래스터 이미지 형식으로 변환
og_description: Aspose.CAD for Java를 사용하여 DWG를 PNG로 빠르게 변환합니다. CAD를 PNG, JPEG, TIFF
  등으로 내보내는 단계별 방법을 배워보세요.
og_image_alt: 'Developer guide: Convert DWG to PNG and other raster formats using
  Aspose.CAD for Java'
og_title: Aspose.CAD for Java를 사용하여 DWG를 PNG 및 기타 래스터 형식으로 변환
schemas:
- author: Aspose
  dateModified: '2026-10-04'
  description: Learn how to quickly convert dwg to png and export cad as png or other
    raster formats using Aspose.CAD for Java. Get high‑quality results fast.
  headline: Convert DWG to PNG and other raster formats using Aspose.CAD for Java
  type: TechArticle
- description: Learn how to quickly convert dwg to png and export cad as png or other
    raster formats using Aspose.CAD for Java. Get high‑quality results fast.
  name: Convert DWG to PNG and other raster formats using Aspose.CAD for Java
  steps:
  - name: set up the resource directory
    text: Replace `"Your Document Directory"` with the absolute path where your CAD
      files reside. This directory will be used for both input and output files.
  - name: load the CAD file
    text: '`Image.load` parses the source file and creates an in‑memory representation
      that you can rasterize. You can load any supported format (DWG, DXF, DGN, etc.)
      – this is the **how to convert cad** part.'
  - name: configure rasterization options
    text: '`CadRasterizationOptions` defines how the vector data is turned into pixels.
      `setPageWidth` and `setPageHeight` control output resolution (larger values
      = higher DPI). `setLayouts` lets you **convert CAD to raster** for specific
      layouts; omit it to rasterize the whole drawing.'
  - name: set image options
    text: '`TiffOptions` (or `PngOptions` for PNG) tells Aspose which raster format
      to generate and lets you fine‑tune compression, color depth, and other format‑specific
      settings. Choose the options class that matches your desired output.'
  - name: save the resultant image
    text: Call `save` on the `Image` instance, passing the output file name and the
      options object. Change the file extension to `.png` (and use `PngOptions`) to
      **save CAD as PNG**. The same pattern works for JPEG, BMP, or PDF. > **Common
      pitfall:** Forgetting to match the file extension with the options cla
  type: HowTo
- questions:
  - answer: Yes, it supports over 30 CAD and raster formats, including DWG, DXF, DGN,
      and SVG.
    question: Is Aspose.CAD compatible with different CAD file formats?
  - answer: Absolutely. Adjust `setPageWidth`, `setPageHeight`, or `setResolution`
      in `CadRasterizationOptions` to achieve the desired DPI.
    question: Can I customize the resolution of the output raster image?
  - answer: Provide an array with all layout names to `setLayouts`, e.g., `new String[]{"Model","Layout1","Layout2"}`.
    question: How can I convert multiple CAD layouts in a single run?
  - answer: Yes—PNG, JPEG, BMP, PDF, and more are available via their respective `*Options`
      classes.
    question: Are there output formats besides TIFF supported?
  - answer: Visit the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) for community
      support and official assistance.
    question: Where can I get help or share my experience with Aspose.CAD?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- convert dwg
- Aspose.CAD
- Java raster conversion
- CAD image processing
title: Aspose.CAD for Java를 사용하여 DWG를 PNG 및 기타 래스터 형식으로 변환
url: /ko/java/cad-drawing-conversion/convert-cad-layout-to-raster-image/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD for Java를 사용하여 DWG를 PNG 및 기타 래스터 형식으로 변환

## 소개

`Aspose.CAD for Java`은 PNG, JPEG, TIFF와 같은 래스터 이미지로 CAD 파일을 프로그래밍 방식으로 변환할 수 있게 해주는 라이브러리입니다. DWG를 PNG(또는 다른 래스터 이미지 형식)로 변환하는 것은 CAD 뷰어가 없는 팀원과 도면을 공유하거나, 문서에 디자인을 삽입하거나, 웹 갤러리를 위한 썸네일을 생성해야 할 때 흔히 요구됩니다. 이 가이드에서는 전체 도면 파일이든 특정 레이아웃이든 빠르고 안정적으로 dwg를 png로 변환하는 방법을 배웁니다. 웹 미리보기, 보고 도구 또는 모바일 앱을 위해 **convert CAD to raster**가 필요할 수도 있습니다.

## 빠른 답변
- **DWG를 PNG로 처리하는 라이브러리는?** Aspose.CAD for Java은 변환 엔진을 제공합니다.  
- **어떤 래스터 형식으로 내보낼 수 있나요?** PNG, JPEG, TIFF, PDF, BMP 및 30가지 이상의 추가 형식.  
- **테스트에 라이선스가 필요합니까?** 개발에는 무료 체험판을 사용할 수 있으며, 프로덕션에는 상용 라이선스가 필요합니다.  
- **특정 레이아웃을 선택할 수 있나요?** 예 – `setLayouts`를 사용하여 “Model”, “Layout1” 등을 지정합니다.  
- **고해상도 출력이 가능한가요?** 물론입니다 – `setPageWidth`와 `setPageHeight`(또는 `setResolution`)를 조정하여 DPI를 제어합니다.

## “convert dwg to png”란 무엇인가요?

Convert dwg to png는 DWG 벡터 도면을 표준 이미지 뷰어에서 표시할 수 있는 픽셀 기반 PNG 이미지로 변환하는 것을 의미합니다. 이 과정은 벡터 엔티티를 래스터화하여 선 두께, 색상 및 레이어를 보존하면서 고정 해상도 비트맵으로 변환합니다. 결과물은 PDF, Word 문서 또는 벡터 지원이 제한된 웹 페이지에 삽입하기에 이상적입니다.

## CAD를 PNG(또는 기타 래스터 형식)로 내보내는 이유

CAD를 PNG로 내보내면 모든 주요 플랫폼에서 보편적인 호환성, 빠른 로딩 및 손쉬운 삽입이 가능합니다. 무거운 DWG 파일을 여는 것에 비해 래스터 이미지는 즉시 로드되며, PNG의 무손실 압축은 시각적 충실도를 보장합니다. 해상도, 배경 색상 및 레이아웃을 제어함으로써 파일이 데스크톱, 모바일 장치 또는 브라우저에서 보이든 모든 이해관계자가 동일한 모습을 보게 됩니다.

## 일반적인 사용 사례

| 시나리오 | 래스터 출력이 도움이 되는 이유 |
|----------|------------------------|
| **프로젝트 문서화** | PDF 또는 Word 문서에 PNG를 삽입하면 검토자에게 CAD 소프트웨어가 필요하지 않습니다. |
| **웹 포털** | DWG 파일에서 생성된 썸네일은 즉시 로드되어 사용자 경험을 향상시킵니다. |
| **모바일 앱** | CAD 뷰어가 없는 장치에서도 래스터 이미지가 올바르게 표시됩니다. |
| **자동 보고** | 여러 레이아웃을 PNG/JPEG로 일괄 변환하여 차트나 대시보드에 포함합니다. |

## 사전 요구 사항

시작하기 전에 다음을 확인하세요:

1. **Java 개발 환경** – JDK 8 이상이 설치되고 구성되어 있어야 합니다.  
2. **Aspose.CAD for Java** – 최신 JAR를 [Aspose.CAD for Java documentation](https://reference.aspose.com/cad/java/)에서 다운로드하십시오.  

## 네임스페이스 가져오기

`com.aspose.cad.Image`는 메모리 내에서 모든 CAD 파일을 나타내는 핵심 클래스입니다. `com.aspose.cad.imageoptions.*`는 각 래스터 형식에 대한 옵션 객체를 제공합니다. 도면을 로드하고, 래스터화를 구성하고, 출력을 저장하는 데 필요한 클래스를 가져오세요.

> **팁:** **CAD를 PNG로 내보내**려는 경우 TIFF 대신 `TiffOptions`를 `PngOptions`( `com.aspose.cad.imageoptions.PngOptions`에 있음)로 교체하세요.

## 단계별 가이드

### 단계 1: 리소스 디렉터리 설정

`"Your Document Directory"`를 CAD 파일이 위치한 절대 경로로 교체하세요. 이 디렉터리는 입력 및 출력 파일 모두에 사용됩니다.

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

### 단계 2: CAD 파일 로드

`Image.load`는 소스 파일을 파싱하여 래스터화할 수 있는 메모리 내 표현을 생성합니다. 지원되는 모든 형식(DWG, DXF, DGN 등)을 로드할 수 있으며, 이는 **how to convert cad** 부분입니다.

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";
```

### 단계 3: 래스터화 옵션 구성

`CadRasterizationOptions`는 벡터 데이터를 픽셀로 변환하는 방식을 정의합니다. `setPageWidth`와 `setPageHeight`는 출력 해상도를 제어합니다(값이 클수록 DPI가 높아짐). `setLayouts`를 사용하면 특정 레이아웃에 대해 **convert CAD to raster**할 수 있으며, 생략하면 전체 도면을 래스터화합니다.

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

### 단계 4: 이미지 옵션 설정

`TiffOptions`(PNG의 경우 `PngOptions`)는 Aspose에 생성할 래스터 형식을 알려주며 압축, 색 깊이 및 기타 형식별 설정을 세밀하게 조정할 수 있게 합니다. 원하는 출력에 맞는 옵션 클래스를 선택하세요.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1200);
rasterizationOptions.setPageHeight(1200);
rasterizationOptions.setLayouts(new String[] {"Model", "Layout1"});
```

### 단계 5: 결과 이미지 저장

`Image` 인스턴스에서 `save`를 호출하고 출력 파일 이름과 옵션 객체를 전달합니다. 파일 확장자를 `.png`로 변경하고(`PngOptions` 사용) **CAD를 PNG로 저장**합니다. 동일한 패턴이 JPEG, BMP 또는 PDF에도 적용됩니다.

```java
ImageOptionsBase options = new TiffOptions(TiffExpectedFormat.Default);
options.setVectorRasterizationOptions(rasterizationOptions);
```

> **일반적인 실수:** 파일 확장자와 옵션 클래스를 일치시키지 않으면 `UnsupportedFormatException`이 발생합니다. 항상 두 요소를 일치시켜 주세요.

## 일반적인 문제 및 해결책

| 문제 | 해결책 |
|-------|----------|
| **빈 출력 이미지** | `setLayouts`의 레이아웃 이름이 소스 CAD 파일의 이름과 정확히 일치하는지 확인하세요. |
| **저해상도 PNG** | `setPageWidth`/`setPageHeight`를 늘리거나 래스터화 옵션에서 `setResolution`을 설정하세요. |
| **지원되지 않는 DWG 버전** | 최신 Aspose.CAD 버전을 사용하고 있는지 확인하세요; 이전 릴리스는 최신 DWG를 지원하지 않을 수 있습니다. |
| **대용량 파일에서 메모리 오류** | 페이지를 하나씩 처리하거나 JVM 힙(`-Xmx2g`)을 늘리세요. |

## 자주 묻는 질문

**Q: Aspose.CAD가 다양한 CAD 파일 형식과 호환되나요?**  
A: 예, DWG, DXF, DGN, SVG 등을 포함해 30가지 이상의 CAD 및 래스터 형식을 지원합니다.

**Q: 출력 래스터 이미지의 해상도를 맞춤 설정할 수 있나요?**  
A: 물론입니다. 원하는 DPI를 얻기 위해 `CadRasterizationOptions`에서 `setPageWidth`, `setPageHeight` 또는 `setResolution`을 조정하세요.

**Q: 한 번에 여러 CAD 레이아웃을 변환하려면 어떻게 해야 하나요?**  
A: `setLayouts`에 모든 레이아웃 이름을 배열로 제공하세요. 예: `new String[]{"Model","Layout1","Layout2"}`.

**Q: TIFF 외에 지원되는 출력 형식이 있나요?**  
A: 예—각각의 `*Options` 클래스를 통해 PNG, JPEG, BMP, PDF 등 더 많은 형식을 사용할 수 있습니다.

**Q: Aspose.CAD에 대한 도움을 받거나 경험을 공유하려면 어디로 가면 되나요?**  
A: 커뮤니티 지원 및 공식 지원을 위해 [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) 를 방문하세요.

## 결론

이 단계들을 따르면 **DWG를 PNG로 변환**, **CAD를 PNG로 내보내**, **CAD를 JPEG로 저장**하거나 필요한 다른 모든 래스터 형식을 생성할 수 있습니다. Aspose.CAD for Java는 복잡한 작업을 처리해 주므로 고품질 이미지를 애플리케이션, 문서 또는 웹 포털에 통합하는 데 집중할 수 있습니다. 30가지 이상의 형식을 지원하고 전체 파일을 메모리에 로드하지 않고도 수백 페이지 도면을 렌더링할 수 있는 능력은 엔터프라이즈급 CAD 래스터화에 강력한 선택이 됩니다.

---

**마지막 업데이트:** 2026-10-04  
**테스트 환경:** Aspose.CAD for Java 24.12  
**작성자:** Aspose  







```java
image.save(dataDir + "conic_pyramid_layoutstorasterimage_out_.tiff", options);
```

```bash
java -jar aspose-cad.jar -i input.dwg -o output.png -w 1200 -h 1200
```

## 관련 튜토리얼

- [Java CAD 라이브러리 Aspose.CAD for Java를 사용하여 DWG를 PDF 또는 래스터로 빠르게 내보내기](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)
- [Aspose.CAD for Java로 DWG를 BMP로 변환](/cad/java/cad-export-options/export-to-bmp/)
- [Aspose.CAD for Java를 사용하여 특정 레이아웃으로 DWG를 PDF로 내보내기](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}