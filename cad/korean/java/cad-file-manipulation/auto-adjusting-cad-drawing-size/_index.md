---
date: 2025-12-22
description: Aspose.CAD를 사용하여 Java에서 CAD 도면을 내보내고 DWG를 BMP로 변환하는 방법을 배워보세요. 효율적인 CAD
  파일 조작을 위한 단계별 가이드를 따라보세요.
linktitle: Auto Adjusting CAD Drawing Size
second_title: Aspose.CAD Java API
title: Aspose.CAD for Java를 사용하여 CAD 도면을 BMP로 내보내는 방법
url: /ko/java/cad-file-manipulation/auto-adjusting-cad-drawing-size/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspise.CAD for Java를 사용하여 CAD 도면을 BMP로 내보내는 방법

## Introduction

Java에서 **how to export cad** 파일을 명확하고 신뢰할 수 있게 내보내는 방법을 찾고 있다면, 여기가 바로 정답입니다. Aspose.CAD for Java를 사용하면 도면 크기를 자동으로 조정할 뿐만 아니라 몇 줄의 코드만으로 **DWG를 BMP로 변환**할 수 있습니다. 이 튜토리얼은 환경 설정부터 원본 CAD 레이아웃을 보존하는 BMP 이미지 생성까지 전체 과정을 단계별로 안내합니다.

## Quick Answers
- **“how to export cad”가 의미하는 것은 무엇인가요?** CAD 파일(DWG, DXF 등)을 BMP, PNG, PDF와 같은 다른 형식으로 변환하는 것을 의미합니다.  
- **어떤 라이브러리가 변환을 담당하나요?** Aspose.CAD for Java가 이 작업을 위한 간단한 API를 제공합니다.  
- **라이선스가 필요합니까?** 테스트용 임시 라이선스로 충분하지만, 실제 운영 환경에서는 정식 라이선스가 필요합니다.  
- **한 번에 여러 레이아웃을 내보낼 수 있나요?** 네 – `Layouts` 속성을 설정하면 렌더링할 레이아웃을 지정할 수 있습니다.  
- **BMP가 유일한 출력 형식인가요?** 아니요 – PNG, JPEG, TIFF 등 다른 형식으로도 내보낼 수 있습니다.

## What is “how to export cad” with Aspose.CAD?

CAD 내보내기는 DWG 파일과 같은 네이티브 CAD 도면을 래스터 이미지 또는 다른 벡터 형식으로 변환하는 작업을 의미합니다. Aspose.CAD는 CAD 구조 파싱, 벡터 엔티티 래스터화, 선택한 이미지 형식으로 결과를 쓰는 모든 복잡한 과정을 자동으로 처리합니다.

## Why use Aspose.CAD for Java to **convert DWG to BMP**?
- **외부 종속성 없음** – 순수 Java이며 네이티브 DLL이 필요하지 않습니다.  
- **DWG, DXF, DGN 등 다양한 형식에 대한 완전 지원**.  
- **세밀한 제어** – 레이아웃 선택, 스케일링, 배경색 등 래스터화 옵션을 자유롭게 설정할 수 있습니다.  
- **고성능** – 서버에서 배치 처리에 적합합니다.

## Prerequisites

시작하기 전에 다음 항목을 준비하십시오:

1. **Java Development Kit** – [여기](https://www.java.com/en/download/)에서 다운로드합니다.  
2. **Aspose.CAD for Java 라이브러리** – 최신 JAR 파일을 [여기](https://releases.aspose.com/cad/java/)에서 얻으세요.  
3. **샘플 CAD 파일** – 프로젝트의 `document` 디렉터리에 위치한 `sample.dwg`와 같은 DWG 파일.

## Import Namespaces

Java 애플리케이션에서 Aspose.CAD 기능을 사용하려면 필요한 네임스페이스를 포함해야 합니다. 예시는 다음과 같습니다:

```java

import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

이제 **how to export cad** 과정을 관리 가능한 단계로 나누어 보겠습니다.

## Step‑by‑Step Guide

### Step 1: Load the CAD Drawing

```java
String dataDir = "Your Document Directory" + "CADConversion/";
String sourceFilePath = dataDir + "sample.dwg";
Image objImage = Image.load(sourceFilePath);
```

소스 DWG 파일을 `Image` 객체에 로드합니다. 이 객체가 이후 모든 작업의 진입점이 됩니다.

### Step 2: Create `BmpOptions`

```java
BmpOptions bmpOptions = new BmpOptions();
```

`BmpOptions`는 BMP 출력에 특화된 래스터화 설정을 보관합니다.

### Step 3: Configure Rasterization Settings

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
bmpOptions.setVectorRasterizationOptions(cadRasterizationOptions);
```

여기서 래스터화 옵션을 BMP 옵션에 연결하여 CAD 엔티티가 어떻게 렌더링될지 제어합니다.

### Step 4: Set the Layout(s) to Export

```java
cadRasterizationOptions.setLayouts(new String[]{"Model"});
```

`Layouts` 속성을 사용해 Aspose.CAD가 포함할 도면 레이아웃을 지정합니다. 대부분의 경우 `"Model"`이 변환하려는 기본 레이아웃입니다.

### Step 5: Export to BMP Format

```java
String outPath = sourceFilePath + ".bmp";
objImage.save(outPath, bmpOptions);
```

구성된 `BmpOptions`와 함께 `save` 메서드를 호출하면 BMP 파일이 디스크에 저장됩니다. 이렇게 하면 **convert DWG to BMP** 작업이 완료됩니다.

## Common Issues and Solutions

| Issue | Reason | Fix |
|-------|--------|-----|
| 출력 이미지가 비어 있음 | 레이아웃 이름이 잘못되었거나 레이아웃이 누락됨 | CAD 파일과 레이아웃 이름이 일치하는지 확인하십시오(예: `"Model"`). |
| 해상도 낮음 | 기본 DPI가 낮음 | 저장하기 전에 `cadRasterizationOptions.setResolution(300);`을 설정하십시오. |
| 대용량 파일에서 메모리 부족 오류 | 큰면은 더 많은 힙이 필요합니다 | JVM 힙 크기를 (`-Xmx2g`) 늘리거나 페이지를 개별적으로 처리하십시오. |

## Frequently Asked Questions

**Q: Aspose.CAD가 다양한 CAD 파일 형식을 지원하나요?**  
A: 네, Aspose.CAD는 DWG, DXF, DGN 등 많은 형식을 지원합니다.

**Q: Aspose.CAD를 상업 프로젝트에 사용할 수 있나요?**  
A: 물론입니다. 생산 환경에서는 [여기](https://purchase.aspose.com/buy)에서 라이선스를 구매하십시오.

**Q: 테스트용 임시 라이선스는 어떻게 얻나요?**  
A: [여기](https://purchase.aspose.com/temporary-license/)에서 임시 라이선스를 받을 수 있습니다.

**Q: 커뮤니티 지원은 어디서 받을 수 있나요?**  
A: [forum](https://forum.aspose.com/c/cad/19)에서 Aspose.CAD 커뮤니티 포럼에 참여하세요.

**Q: Aspose.CAD for Java에 대한 무료 체험판이 있나요?**  
A: 네, [여기](https://releases.aspose.com/)에서 무료 체험판을 다운로드하십시오.

## Conclusion

이 가이드에서는 Java에서 **how to export cad** 파일을 처리하고 Aspose.CAD를 사용해 **DWG를 BMP로 변환**하는 전체 흐름을 보여주었습니다. 위의 다섯 단계를 따르면 데스크톱 도구, 웹 서비스 또는 배치 처리 파이프라인 등 어떤 Java 애플리케이션에도 CAD‑to‑이미지 변환 기능을 손쉽게 통합할 수 있습니다. 옵션 클래스를 교체하면 PNG, JPEG, PDF 등 다른 출력 형식도 손쉽게 사용할 수 있으니, Aspose.CAD의 풍부한 기능을 활용해 모든 CAD 조작 요구를 만족시키세요.

---

**마지막 업데이트:** 2025-12-22  
**테스트 환경:** Aspose.CAD for Java 24.12  
**작성자:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}