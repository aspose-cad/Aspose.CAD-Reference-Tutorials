---
date: 2026-02-20
description: Aspose.CAD for Java를 사용하여 DWG를 BMP로 변환하고 CAD를 BMP로 효율적으로 내보내는 방법을 배워보세요.
  정확한 변환을 위한 단계별 가이드를 따라가세요.
linktitle: Export to BMP
second_title: Aspose.CAD Java API
title: Aspose.CAD for Java를 사용하여 DWG를 BMP로 변환
url: /ko/java/cad-export-options/export-to-bmp/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD for Java를 사용하여 DWG를 BMP로 변환

## 소개

현대 엔지니어링 워크플로우에서는 **convert DWG to BMP**를 빠르고 안정적으로 수행하는 것이 썸네일, 문서 작성 또는 CAD 시각화를 웹 애플리케이션에 통합하는 데 필수적입니다. Aspose.CAD for Java는 래스터화 설정을 완벽히 제어하면서 **export CAD to BMP**를 할 수 있는 간단한 API를 제공합니다. 이 튜토리얼에서는 환경 설정부터 최종 BMP 이미지 저장까지 전체 과정을 단계별로 안내하여, Java 프로젝트에 자신 있게 이 기능을 추가할 수 있도록 도와드립니다.

## 빠른 답변
- **어떤 라이브러리가 필요합니까?** Aspose.CAD for Java (free trial available).  
- **변환을 지원하는 파일 형식은 무엇입니까?** DWG, DWF, DXF, 및 기타 많은 CAD 형식을 BMP로 변환할 수 있습니다.  
- **개발에 라이선스가 필요합니까?** 테스트용 임시 또는 평가 라이선스로 충분하며, 프로덕션에서는 정식 라이선스가 필요합니다.  
- **변환에 걸리는 시간은 얼마나 됩니까?** 최신 하드웨어에서 일반적인 크기의 도면은 1초 미만에 처리됩니다.  
- **여러 파일을 배치 처리할 수 있습니까?** 예—각 파일에 대해 변환 코드를 반복 실행하면 됩니다.

## DWG를 BMP로 변환한다는 것은 무엇인가요?

DWG를 BMP로 변환한다는 것은 벡터 기반 CAD 도면을 래스터 비트맵 이미지로 바꾸는 것을 의미합니다. 이는 브라우저에서 표시하거나 문서에 삽입하거나, CAD 파일을 지원하지 않는 이미지 편집 도구에서 처리해야 할 때 유용합니다.

## 왜 Aspose.CAD를 사용해 CAD를 BMP로 내보내나요?
- **외부 종속성 없음** – pure Java, no native DLLs.  
- **고품질** – preserves line weights, colors, and layers.  
- **맞춤형 래스터화** – control page size, resolution, and rendering quality.  
- **배치 준비** – easy to integrate into automated pipelines.

## 전제 조건

튜토리얼을 진행하기 전에 다음 사항을 준비하십시오:

- Aspose.CAD for Java 라이브러리: Aspose.CAD for Java 라이브러리를 [here](https://releases.aspose.com/cad/java/)에서 다운로드하고 설치하십시오.
- Java 개발 환경: 시스템에 Java 개발 환경이 설정되어 있는지 확인하십시오.
- 기본 Java 지식: 기본 Java 프로그래밍 개념에 익숙해지십시오.

## 네임스페이스 가져오기

Java 프로젝트에서 Aspose.CAD 기능에 접근하기 위해 필요한 네임스페이스를 가져옵니다:

```java
import com.aspose.cad.Image;
import com.aspose.cad.InterpolationMode;
import com.aspose.cad.SmoothingMode;
import com.aspose.cad.TextRenderingHint;

import com.aspose.cad.imageoptions.BmpOptions;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
//import com.aspose.cad.imageoptions.TypeOfEntities;
```

## Aspose.CAD for Java를 사용하여 DWG를 BMP로 변환하는 방법

아래는 원본 워크플로우를 그대로 따르면서 추가적인 컨텍스트와 모범 사례 팁을 제공하는 단계별 가이드입니다.

### 단계 1: 리소스 디렉터리 경로 설정

CAD 파일이 위치한 리소스 디렉터리 경로를 정의합니다.

```java
String dataDir = "Your Document Directory" + "ExportingCAD/";
```

> **Pro tip:** `System.getProperty("user.dir")`를 사용하여 환경에 관계없이 작동하는 절대 경로를 구축하십시오.

### 단계 2: CAD 파일 로드

CAD 파일을 Aspose.CAD `Image` 객체에 로드합니다.

```java
String fileName = (dataDir + "site.dwf");
Image image = Image.load(fileName);
```

> **Why this matters:** 파일을 한 번만 로드하면 필요에 따라 여러 내보내기 형식에 대해 `Image` 인스턴스를 재사용할 수 있습니다.

### 단계 3: BMP 내보내기 옵션 구성

BMP 내보내기 옵션을 생성하고 래스터화 설정을 구성합니다.

```java
BmpOptions bmpOptions = new BmpOptions();
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
bmpOptions.setVectorRasterizationOptions(rasterizationOptions);
```

> **Tip:** `bmpOptions.setBitsPerPixel(24);`를 설정하여 색 깊이를 제어할 수 있습니다.

### 단계 4: 래스터화 매개변수 설정

페이지 높이, 페이지 너비 및 레이아웃과 같은 매개변수를 정의합니다.

```java
rasterizationOptions.setPageHeight(500);
rasterizationOptions.setPageWidth(500);
rasterizationOptions.setLayouts(new String[] { "Model" });
```

> **Common pitfall:** 레이아웃을 지정하지 않으면 다중 레이아웃 도면에서 빈 이미지가 생성될 수 있습니다.

### 단계 5: BMP로 내보내기

출력 경로를 지정하고 BMP 파일을 저장합니다.

```java
String outPath = dataDir + "site.bmp";
image.save(outPath, bmpOptions);
```

> **Result:** `site.bmp` 파일이 `ExportingCAD` 폴더에 생성되어 보고서, 웹 페이지 또는 추가 이미지 처리에 바로 사용할 수 있습니다.

Aspose.CAD for Java를 사용하여 BMP로 내보내고자 하는 각 CAD 파일에 대해 위 단계를 반복하십시오.

## 일반적인 문제 및 해결책

| 문제 | 원인 | 해결책 |
|-------|-------|----------|
| 빈 BMP 출력 | 잘못된 레이아웃 이름 또는 레이아웃 누락 | 레이아웃 이름이 원본 CAD 파일과 일치하는지 확인하십시오(예: `"Model"`). |
| 저해상도 이미지 | 기본 래스터화 DPI가 낮음 | `rasterizationOptions.setResolution(300);`을 설정하여 고품질로 만드세요. |
| 대용량 파일에서 OutOfMemoryError 발생 | 힙 공간 부족 | JVM 힙을 늘리세요(`-Xmx2g`) 또는 파일을 작은 배치로 처리하십시오. |

## 결론

Aspose.CAD for Java를 사용하면 CAD 파일을 BMP 형식으로 내보내는 작업이 매우 간단해집니다. 이 단계별 가이드를 따르면 **convert DWG to BMP** 기능을 Java 애플리케이션에 원활히 통합할 수 있어, 어떤 엔지니어링 워크플로우에서도 효율적이고 정확한 변환을 보장합니다.

## FAQ

### Q1: Aspose.CAD for Java는 배치 처리에 적합합니까?

A1: 물론입니다! Aspose.CAD for Java는 배치 처리를 지원하므로 여러 CAD 파일을 동시에 효율적으로 처리할 수 있습니다.

### Q2: 서로 다른 레이아웃에 대해 래스터화 옵션을 맞춤 설정할 수 있습니까?

A2: 예, 페이지 크기와 레이아웃 등 래스터화 옵션을 필요에 따라 자유롭게 조정할 수 있습니다.

### Q3: Aspose.CAD for Java에 대한 추가 지원은 어디에서 찾을 수 있습니까?

A3: 커뮤니티 지원 및 토론을 위해 [Aspose.CAD 포럼](https://forum.aspose.com/c/cad/19)을 방문하십시오.

### Q4: 무료 체험판을 이용할 수 있습니까?

A4: 예, Aspose.CAD for Java의 무료 체험판을 [here](https://releases.aspose.com/)에서 확인할 수 있습니다.

### Q5: 임시 라이선스를 어떻게 얻을 수 있습니까?

A5: Aspose.CAD for Java의 임시 라이선스는 [here](https://purchase.aspose.com/temporary-license/)에서 얻을 수 있습니다.

## 자주 묻는 질문

**Q:** 동일한 코드로 다른 CAD 형식(예: DXF)을 BMP로 변환할 수 있습니까?  
**A:** 예. `fileName`의 확장자를 변경하면 Aspose.CAD가 자동으로 변환을 처리합니다.

**Q:** BMP에 투명 배경을 설정할 수 있습니까?  
**A:** BMP는 투명도를 기본적으로 지원하지 않으므로 알파 채널이 필요하면 PNG로 내보내는 것을 고려하십시오.

**Q:** 생성된 BMP를 PDF 보고서에 삽입하려면 어떻게 해야 합니까?  
**A:** 표준 이미지 라이브러리(예: iText)를 사용해 BMP를 로드하고 이미지 객체로 PDF에 추가하면 됩니다.

**Q:** 라이브러리가 고해상도 인쇄를 지원합니까?  
**A:** 예. `rasterizationOptions.setResolution()`을 600 DPI 이상으로 설정하면 인쇄 품질 출력이 가능합니다.

**Q:** 상업적 사용을 위한 라이선스 옵션은 무엇입니까?  
**A:** Aspose는 영구 라이선스, 구독 라이선스, 임시 라이선스를 제공하며, 맞춤 견적은 영업팀에 문의하십시오.

---

**Last Updated:** 2026-02-20  
**Tested With:** Aspose.CAD for Java 24.11 (latest at time of writing)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}