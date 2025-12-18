---
date: 2025-12-18
description: Aspose.CAD for Java를 사용하여 DWG를 PNG 및 기타 래스터 이미지 형식으로 변환하는 방법을 배워보세요.
  고품질 결과로 CAD를 PNG로 내보냅니다.
linktitle: Convert CAD Layout to Raster Image Format
second_title: Aspose.CAD Java API
title: Aspose.CAD for Java를 사용하여 DWG를 PNG 및 기타 래스터 형식으로 변환
url: /ko/java/cad-drawing-conversion/convert-cad-layout-to-raster-image/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DWG를 PNG 및 기타 래스터 형식으로 변환하기 - Aspose.CAD for Java 사용

## 소개

DWG를 PNG(또는 기타 래스터 이미지 형식)로 변환하는 것은 CAD 뷰어가 없는 팀원과 CAD 도면을 공유하거나, 문서에 디자인을 삽입하거나, 웹 갤러리를 위한 썸네일을 생성해야 할 때 흔히 요구되는 작업입니다. Aspose.CAD for Java는 전체 도면 파일이든 특정 레이아웃이든 관계없이 이 변환을 간단하게 수행할 수 있게 해줍니다. 이 튜토리얼에서는 **CAD 레이아웃을 래스터 이미지로 변환**하는 정확한 단계를 살펴보며, 동일한 방법으로 PNG, JPEG, TIFF, PDF 출력도 만들 수 있습니다.

## 빠른 답변
- **DWG를 PNG로 변환하는 라이브러리는?** Aspose.CAD for Java  
- **어떤 형식으로 내보낼 수 있나요?** PNG, JPEG, TIFF, PDF, BMP 등  
- **테스트에 라이선스가 필요합니까?** 개발에는 무료 체험판으로 충분하며, 프로덕션에서는 라이선스가 필요합니다  
- **특정 레이아웃을 선택할 수 있나요?** 예, `setLayouts`를 사용하여 “Model”, “Layout1” 등을 지정합니다  
- **고해상도 출력이 가능한가요?** 물론입니다—`setPageWidth`와 `setPageHeight`를 조정하여 DPI를 제어합니다  

## “convert dwg to png”란 무엇인가요?

“convert dwg to png”라는 표현은 벡터 기반 DWG 파일(많은 CAD 애플리케이션의 기본 형식)을 픽셀 기반 PNG 이미지로 래스터화하는 과정을 의미합니다. 래스터 이미지는 웹 표시, 이메일 공유 및 비‑CAD 소프트웨어와의 통합에 이상적입니다.

## CAD를 PNG(또는 기타 래스터 형식)으로 내보내는 이유는?
- **범용 호환성:** PNG와 JPEG는 사실상 모든 이미지 뷰어와 브라우저에서 지원됩니다.  
- **빠른 로딩:** 무거운 DWG 파일을 여는 것보다 래스터 이미지가 즉시 로드됩니다.  
- **간편 삽입:** 추가 플러그인 없이 PNG를 Word, PowerPoint, HTML 등에 직접 삽입할 수 있습니다.  
- **일관된 외관:** 해상도, 배경, 레이아웃을 제어하여 모든 이해관계자가 동일한 시각을 보게 합니다.

## 사전 요구 사항

1. **Java 개발 환경** – JDK 8 이상이 설치되고 구성되어 있어야 합니다.  
2. **Aspose.CAD for Java** – 최신 JAR를 [Aspose.CAD for Java documentation](https://reference.aspose.com/cad/java/)에서 다운로드합니다.  

## 네임스페이스 가져오기

먼저 필요한 클래스를 가져옵니다. 이러한 import 구문을 통해 이미지 로드, 래스터화 옵션 및 TIFF/PNG 출력 설정에 접근할 수 있습니다.

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

> **Pro tip:** PNG 대신 TIFF를 내보내려면 `TiffOptions`를 `com.aspose.cad.imageoptions.PngOptions`에 있는 `PngOptions`로 교체하십시오.

## 단계별 가이드

### 단계 1: 리소스 디렉터리 설정

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";
```

`"Your Document Directory"`를 CAD 파일이 위치한 절대 경로로 교체하십시오.

### 단계 2: CAD 파일 로드

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

지원되는 모든 형식(DWG, DXF, DGN 등)을 로드할 수 있습니다. 이것이 **how to convert cad** 부분이며, 파일을 지정하고 Aspose가 파싱하도록 하면 됩니다.

### 단계 3: 래스터화 옵션 구성

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1200);
rasterizationOptions.setPageHeight(1200);
rasterizationOptions.setLayouts(new String[] {"Model", "Layout1"});
```

- `setPageWidth` / `setPageHeight`는 출력 해상도를 제어합니다(값이 클수록 DPI가 높아짐).  
- `setLayouts`를 사용하면 특정 레이아웃에 대해 **convert cad to raster**를 수행할 수 있습니다; 전체 도면을 래스터화하려면 생략합니다.

### 단계 4: 이미지 옵션 설정

```java
ImageOptionsBase options = new TiffOptions(TiffExpectedFormat.Default);
options.setVectorRasterizationOptions(rasterizationOptions);
```

PNG를 원한다면 `TiffOptions` 대신 `PngOptions`를 인스턴스화하십시오. 여기서 **export cad as png**를 수행합니다.

### 단계 5: 결과 이미지 저장

```java
image.save(dataDir + "conic_pyramid_layoutstorasterimage_out_.tiff", options);
```

파일 확장자를 `.png`(옵션 객체도 `PngOptions`로)로 변경하면 **save CAD as JPEG/PNG**이 가능합니다.

> **Common Pitfall:** 파일 확장자와 옵션 클래스가 일치하지 않으면 `UnsupportedFormatException`이 발생합니다. 항상 두 요소를 동일하게 유지하십시오.

## 일반적인 문제 및 해결책

| Issue | Solution |
|-------|----------|
| **빈 출력 이미지** | `setLayouts`에 지정한 레이아웃 이름이 원본 CAD 파일의 레이아웃과 정확히 일치하는지 확인하십시오. |
| **저해상도 PNG** | `setPageWidth` / `setPageHeight` 값을 늘리거나 래스터화 옵션에서 `setResolution`을 설정하십시오. |
| **지원되지 않는 DWG 버전** | 최신 Aspose.CAD 버전을 사용하십시오; 오래된 버전은 최신 DWG 릴리스를 지원하지 않을 수 있습니다. |
| **대용량 파일에서 메모리 오류** | 페이지를 하나씩 처리하거나 JVM 힙(`-Xmx2g`)을 늘리십시오. |

## 자주 묻는 질문

**Q: Aspose.CAD가 다양한 CAD 파일 형식을 지원하나요?**  
A: 예, DWG, DXF, DGN 등 많은 형식을 지원합니다.

**Q: 출력 래스터 이미지의 해상도를 사용자 정의할 수 있나요?**  
A: 물론입니다. `CadRasterizationOptions`에서 `setPageWidth`, `setPageHeight` 또는 `setResolution`을 조정하십시오.

**Q: 한 번에 여러 CAD 레이아웃을 변환하려면 어떻게 해야 하나요?**  
A: `setLayouts`에 모든 레이아웃 이름을 배열로 제공하면 됩니다. 예: `new String[]{"Model","Layout1","Layout2"}`.

**Q: TIFF 외에 지원되는 출력 형식이 있나요?**  
A: 예—PNG, JPEG, BMP, PDF 등 각 `*Options` 클래스를 통해 사용할 수 있습니다.

**Q: Aspose.CAD에 대한 도움을 받거나 경험을 공유하려면 어디로 가면 되나요?**  
A: 커뮤니티 지원 및 공식 지원을 위해 [Aspose.CAD forum](https://forum.aspose.com/c/cad/19)을 방문하십시오.

## 결론

이 단계들을 따르면 **DWG를 PNG로 변환**, **CAD를 PNG로 내보내기**, **CAD를 JPEG로 저장** 또는 필요한 다른 래스터 형식을 생성할 수 있습니다. Aspose.CAD for Java가 복잡한 작업을 처리해 주므로 고품질 이미지를 애플리케이션, 문서 또는 웹 포털에 쉽게 통합할 수 있습니다.

---

**마지막 업데이트:** 2025-12-18  
**테스트 환경:** Aspose.CAD for Java 24.12  
**작성자:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}