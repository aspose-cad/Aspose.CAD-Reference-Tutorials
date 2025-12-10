---
date: 2025-12-10
description: Aspose.CAD for Java와 Auto Layout Scaling을 사용하여 CAD에서 PDF를 만드는 방법을 배워보세요.
  이 단계별 가이드는 CAD를 PDF로 효율적이고 신뢰성 있게 내보내는 방법을 보여줍니다.
linktitle: Setting Auto Layout Scaling
second_title: Aspose.CAD Java API
title: CAD에서 PDF 만들기 – Aspose.CAD Java를 사용한 자동 레이아웃 스케일링
url: /ko/java/advanced-cad-features/setting-auto-layout-scaling/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# CAD에서 PDF 만들기 – Aspose.CAD Java를 사용한 자동 레이아웃 스케일링

## Introduction

CAD 파일에서 **PDF 만들기**를 빠르고 완벽한 스케일링으로 해야 한다면, Aspose.CAD for Java가 해결해 줍니다. Auto Layout Scaling은 레이아웃 차원을 자동으로 조정하여 원본 CAD 페이지 크기에 관계없이 결과 PDF가 정확히 의도한 대로 보이게 합니다. 이 튜토리얼에서는 DXF 파일을 로드하는 것부터 PDF로 내보내는 전체 과정을 단계별로 살펴보면서 라이브러리의 **export CAD to PDF** 기능을 강조합니다.

## Quick Answers
- **Auto Layout Scaling이 무엇을 하나요?** 래스터화할 때 CAD 레이아웃을 자동으로 크기 조정하여 대상 페이지 차원에 맞춥니다.
- **어떤 형식을 변환할 수 있나요?** Aspose.CAD에서 지원하는 모든 형식(예: DXF, DWG, DWF)은 PDF로 변환할 수 있습니다.
- **프로덕션에 라이선스가 필요합니까?** 예, 평가용이 아닌 사용에는 상업용 라이선스가 필요합니다.
- **변환 시간은 얼마나 걸리나요?** 일반 파일은 최신 하드웨어에서 보통 1초 미만입니다.
- **페이지 크기를 변경할 수 있나요?** 예, `CadRasterizationOptions`를 통해 사용자 정의 페이지 차원을 설정할 수 있습니다.

## What is “CAD에서 PDF 만들기”?
CAD에서 PDF를 만든다는 것은 벡터 기반 엔지니어링 도면(DXF, DWG 등)을 PDF 문서로 래스터화하는 것을 의미합니다. PDF는 원본 도면의 시각적 정확성을 유지하면서 모든 플랫폼에서 널리 볼 수 있습니다.

## Why use Auto Layout Scaling?
- **일관된 출력:** 모든 레이아웃이 PDF 페이지를 채우도록 보장하며 수동 크기 계산이 필요 없습니다.
- **시간 절약:** 각 도면마다 스케일링 팩터를 수동으로 조정할 필요가 없습니다.
- **고품질:** 변환 중에 선 두께와 기하학적 정확성을 유지합니다.

## Prerequisites

1. **Aspose.CAD for Java 라이브러리** – 최신 버전을 [download page](https://releases.aspose.com/cad/java/)에서 다운로드하십시오.  
2. **리소스 디렉터리 – CAD 파일을 저장할 폴더를 만든 후, 코드에서 `"Your Document Directory"`를 해당 경로로 교체하십시오.  
3. **샘플 CAD 파일** – 이 가이드에서는 Aspose 샘플 데이터 세트에 포함된 `conic_pyramid.dxf`를 사용합니다.

## Import Namespaces

먼저, 필요한 클래스를 가져옵니다. 이를 통해 이미지 로드, 래스터화 및 PDF 내보내기 기능에 접근할 수 있습니다.

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Step 1: Load the CAD File

소스 파일을 로드하는 것은 PDF 문서로 **how to export CAD** 하는 첫 번째 단계입니다.

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

## Step 2: Create Rasterization Options

대상 페이지 차원을 정의합니다. 사용자 정의 레이아웃을 원한다면 이 블록을 사용해 **set CAD page size**를 수동으로 설정할 수도 있습니다.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
```

## Step 3: Set Auto Layout Scaling

자동 스케일링 기능을 활성화합니다. 이는 CAD‑to‑PDF 변환을 위한 **how to set scaling**의 핵심입니다.

```java
rasterizationOptions.setAutomaticLayoutsScaling(true);
```

## Step 4: Create PDF Options

래스터화 설정을 PDF 내보내기 옵션에 연결합니다.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## Step 5: Export to PDF

마지막으로, 렌더링된 이미지를 PDF 파일로 저장합니다. 이 단계가 **convert DXF to PDF** 워크플로를 완료합니다.

```java
image.save(dataDir + "result_out_.pdf", pdfOptions);
```

추가로 처리해야 할 CAD 파일이 있으면 위 단계를 반복하십시오.

## Common Issues & Troubleshooting

| 증상 | 가능한 원인 | 해결 방법 |
|---------||-----|
| 빈 PDF 출력 | 래스터화 옵션이 설정되지 않았거나 파일 경로가 올바르지 않음 | `srcFile` 경로를 확인하고 `setPageWidth/Height`가 0이 아닌지 확인하십시오 |
| 왜곡된 스케일링 | `setAutomaticLayoutsScaling`이 `false`로 남아 있음 | 자동 스케일링을 활성화하거나 스케일링 팩터를 수동으로 계산하십시오 |
| 누락된 레이어 | 소스 DXF에 지원되지 않는 엔터티가 포함됨 | 지원되는 엔터티 유형에 대한 Aspose.CAD 릴리스 노트를 확인하십시오 |

## FAQ's

### Q1: Aspose.CAD for Java가 모든 CAD 파일 형식과 호환됩니까?
A1: Aspose.CAD for Java는 DWG, DXF, DWF 등을 포함한 다양한 CAD 형식을 지원합니다.

### Q2: 스케일링 옵션을 더 세부적으로 맞춤 설정할 수 있나요?
A2: 예, `CadRasterizationOptions` 클래스는 스케일링 및 기타 설정을 미세 조정할 수 있는 다양한 속성을 제공합니다.

### Q3: Aspose.CAD for Java에 대한 추가 문서는 어디에서 찾을 수 있나요?
A3: 자세한 정보와 예제는 [documentation](https://reference.aspose.com/cad/java/)을 참고하십시오.

### Q4: Aspose.CAD for Java의 무료 체험판이 있나요?
A4: 예, [free trial](https://releases.aspose.com/)을 통해 Aspose.CAD for Java의 기능을 체험할 수 있습니다.

### Q5: Aspose.CAD for Java에 대한 지원을 받거나 토론에 참여하려면 어떻게 해야 하나요?
A5: 커뮤니티와 연결하고 지원을 받으려면 [Aspose.CAD forum](https://forum.aspose.com/c/cad/19)을 방문하십시오.

**Additional Common Questions**

**Q: DWG 파일을 PDF로 변환하려면 어떻게 해야 하나요? (DXF 대신)**
A: 동일한 코드가 작동합니다; `srcFile`의 파일 확장자를 `.dwg`로 바꾸면 됩니다.

**Q: 고해상도 PDF를 위해 사용자 정의 DPI를 설정할 수 있나요?**
A: 예, `rasterizationOptions.setResolution(300);`와 같이 원하는 DPI를 설정하십시오.

**Q: 생성된 PDF에 폰트를 포함시킬 수 있나요?**
A: Aspose.CAD는 도면을 래스터화하므로 폰트가 벡터로 렌더링됩니다; 별도의 폰트 포함은 필요하지 않습니다.

## Conclusion

이 가이드를 따라 하면 Aspose.CAD for Java와 Auto Scaling을 사용하여 CAD 파일에서 **PDF 만들기** 하는 방법을 알게 됩니다. 이 과정은 **export CAD to PDF** 워크플로를 간소화하고 일관된 스케일링을 보장하며 개발 시간을 절약합니다. 프로젝트 요구에 맞게 다양한 페이지 크기, 해상도 및 CAD 형식을 자유롭게 실험해 보세요.

---

**Last Updated:** 2025-12-10  
**Tested With:** Aspose.CAD for Java 24.12 (latest)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}