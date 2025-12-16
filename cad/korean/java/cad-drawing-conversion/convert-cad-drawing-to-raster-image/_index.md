---
date: 2025-12-16
description: Aspose.CAD for Java를 사용하여 CAD를 PNG로 변환하는 방법을 배우세요. DWG를 이미지로 내보내기, CAD를
  PNG로 저장하기, CAD를 래스터 이미지로 변환 옵션 등을 포함합니다.
linktitle: Convert CAD Drawing to Raster Image Format
second_title: Aspose.CAD Java API
title: Aspose.CAD for Java를 사용하여 CAD를 PNG로 변환하는 방법
url: /ko/java/cad-drawing-conversion/convert-cad-drawing-to-raster-image/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD for Java를 사용하여 CAD를 PNG로 변환하는 방법

현대 엔지니어링 워크플로우에서는 도면을 브라우저에 표시하거나 문서에 삽입하거나 CAD 소프트웨어가 없는 이해관계자와 공유하기 위해 **CAD를 PNG로 변환**해야 할 경우가 많습니다. 이 튜토리얼에서는 CAD 파일을 로드하고 고품질 PNG 래스터 이미지로 내보내는 전체 과정을 강력한 Aspose.CAD 라이브러리 for Java를 사용하여 단계별로 안내합니다.

## 빠른 답변
- **주된 목적은 무엇인가요?** CAD 도면을 PNG 래스터 이미지로 변환합니다.  
- **사용되는 라이브러리는?** Aspose.CAD for Java.  
- **라이선스가 필요합니까?** 무료 체험판을 사용할 수 있으며, 실제 운영에서는 라이선스가 필요합니다.  
- **이미지 크기를 맞춤 설정할 수 있나요?** 예, `CadRasterizationOptions`를 사용하여 너비와 높이를 설정합니다.  
- **지원되는 CAD 포맷은?** DWG, DXF, DWF 등 다수.

## “CAD를 PNG로 변환”이란?
CAD를 PNG로 변환한다는 것은 벡터 기반 CAD 콘텐츠(DWG, DXF 등)를 픽셀 기반 이미지 포맷으로 래스터화하는 것을 의미합니다. PNG는 투명성을 유지하고 무손실 품질을 제공하므로 웹 미리보기, 문서화 및 보고에 이상적입니다.

## 왜 CAD를 PNG로 변환해야 할까요 (CAD를 래스터 이미지로 변환)?
- **범용 보기:** PNG는 특수 CAD 뷰어 없이 모든 장치에서 작동합니다.  
- **빠른 로딩:** 래스터 이미지는 웹 페이지에서 즉시 로드됩니다.  
- **간편 삽입:** PNG를 PDF, Word 문서 또는 슬라이드에 삽입할 수 있습니다.  
- **일관된 외관:** 설계된 대로 선 굵기, 색상 및 레이어를 정확히 유지합니다.

## 사전 요구 사항
시작하기 전에 다음이 준비되어 있는지 확인하세요:

1. **Java 개발 환경** – JDK 8 이상이 설치되고 구성되어 있어야 합니다.  
2. **Aspose.CAD 라이브러리** – 라이브러리를 다운로드하여 프로젝트에 추가합니다. 라이브러리는 **[here](https://releases.aspose.com/cad/java/)**에서 찾을 수 있습니다.

## 네임스페이스 가져오기
Aspose.CAD 객체를 사용하기 위해 Java 클래스에 필요한 import 문을 추가합니다.

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

## CAD를 PNG로 변환하는 단계별 가이드

### 단계 1: CAD 도면 로드
먼저 `Image.load()`를 사용하여 원본 CAD 파일(DXF, DWG 등)을 로드합니다.

```java
String dataDir = "Your Document Directory" + "CADConversion/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

> **팁:** 경로 문제를 방지하려면 CAD 파일을 전용 폴더(예: `CADConversion`)에 보관하세요.

### 단계 2: 래스터화 옵션 설정 (DWG를 이미지로 내보내기)
출력 이미지 크기와 기타 래스터 설정을 정의합니다.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1200);
rasterizationOptions.setPageHeight(1200);
```

필요에 따라 여기서 배경 색상, 선 렌더링 모드 및 DPI도 제어할 수 있습니다.

### 단계 3: 이미지 옵션 생성 (CAD를 PNG로 저장)
`PngOptions` 인스턴스를 생성하고 래스터화 설정을 연결합니다.

```java
ImageOptionsBase options = new PngOptions();
options.setVectorRasterizationOptions(rasterizationOptions);
```

### 단계 4: 래스터 이미지 저장 (CAD 파일을 PNG로)
마지막으로 PNG 파일을 디스크에 기록합니다.

```java
image.save(dataDir + "conic_pyramid_raster_image_out.png", options);
```

생성된 파일 `conic_pyramid_raster_image_out.png`는 원본 CAD 도면의 고해상도 PNG 표현입니다.

### 다른 파일에 대해 반복
`srcFile`을 다른 CAD 파일을 가리키도록 변경하고 동일한 단계를 실행하면 됩니다. 동일한 코드는 DWG, DWF 및 기타 지원 포맷에서도 작동합니다.

## 일반적인 문제 및 해결책

| 문제 | 해결책 |
|-------|----------|
| **빈 PNG 출력** | 원본 CAD 파일이 올바르게 로드되는지 확인하세요(`Image.load()`가 예외를 발생시키지 않아야 합니다). |
| **잘못된 차원** | `PageWidth` / `PageHeight`를 조정하거나 `rasterizationOptions.setResolution(...)`으로 DPI를 설정하세요. |
| **레이어 누락** | CAD 파일의 레이어가 숨겨져 있지 않은지 확인하고 `CadRasterizationOptions.setDrawType(CadDrawTypeMode.Vector);`를 사용하세요. |
| **라이선스 오류** | 유효한 Aspose.CAD 라이선스 파일을 사용하세요(`License license = new License(); license.setLicense("Aspose.CAD.lic");`). |

## 자주 묻는 질문

**Q1: Aspose.CAD가 모든 CAD 포맷과 호환되나요?**  
A1: Aspose.CAD는 DWG, DXF, DWF 등 다양한 CAD 포맷을 지원합니다. 전체 목록은 **[documentation](https://reference.aspose.com/cad/java/)**를 참고하세요.

**Q2: 특정 요구에 맞게 래스터화 옵션을 맞춤 설정할 수 있나요?**  
A2: 예, Aspose.CAD는 래스터화 옵션 설정에 유연성을 제공하여 요구 사항(크기, DPI, 배경 색상 등)에 맞게 출력을 조정할 수 있습니다.

**Q3: Aspose.CAD 관련 문의에 대한 지원은 어디서 받을 수 있나요?**  
A3: **[Aspose.CAD 포럼](https://forum.aspose.com/c/cad/19)**을 방문하여 도움을 받고 커뮤니티와 소통하세요.

**Q4: Aspose.CAD for Java의 무료 체험판이 있나요?**  
A4: 예, **[here](https://releases.aspose.com/)**에서 무료 체험판을 받아 Aspose.CAD 기능을 살펴볼 수 있습니다.

**Q5: Aspose.CAD for Java를 구매하려면 어떻게 해야 하나요?**  
A5: Aspose.CAD for Java를 구매하려면 **[purchase page](https://purchase.aspose.com/buy)**를 방문하세요.

---

**마지막 업데이트:** 2025-12-16  
**테스트 환경:** Aspose.CAD for Java 24.11 (작성 시 최신 버전)  
**작성자:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}