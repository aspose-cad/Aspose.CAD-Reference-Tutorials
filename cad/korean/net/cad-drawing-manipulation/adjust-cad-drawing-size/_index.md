---
date: 2026-03-19
description: .NET에서 Aspose.CAD를 사용해 CAD 도면 크기를 조정하는 방법을 배우고, CAD 도면 단위를 스케일링하고 레이아웃
  크기를 조정하는 방법을 포함합니다. 단계별 가이드를 따라보세요.
linktitle: Adjusting CAD Drawing Size
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Aspose.CAD for .NET를 사용하여 CAD 도면 크기 조정하는 방법
url: /ko/net/cad-drawing-manipulation/adjust-cad-drawing-size/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD for .NET을 사용한 CAD 도면 크기 조정 방법

## Introduction

.NET 애플리케이션에서 직접 **how to resize CAD** 파일을 조정해야 한다면, 올바른 곳에 오셨습니다. 이 튜토리얼에서는 Aspose.CAD for .NET을 사용하여 CAD 단위 설정을 변경하고, CAD 도면 크기를 스케일링하며, 프로그램matically CAD 크기를 조정하는 방법을 보여드립니다. 가이드가 끝날 때쯤이면 지원되는 모든 CAD 형식에 대해 크기 조정을 수행할 수 있는 견고하고 프로덕션 준비된 솔루션을 갖추게 됩니다.

## Quick Answers
- **필요한 라이브러리는?** Aspose.CAD for .NET  
- **단위 유형을 변경할 수 있나요?** 예 – `CadRasterizationOptions`의 `UnitType` 설정  
- **프로덕션에 라이선스가 필요합니까?** 비체험용으로는 유효한 Aspose.CAD 라이선스가 필요합니다  
- **예제에서 내보내는 이미지 형식은?** BMP (하지만 지원되는 모든 래스터 형식 사용 가능)  
- **코드 라인은 몇 줄인가요?** 전체 크기 조정 작업에 30줄 미만  

## What is “how to resize CAD” in practice?

CAD 도면의 크기 조정은 벡터 데이터를 특정 스케일 또는 단위(예: 센티미터, 인치)로 래스터 이미지로 변환하는 것을 의미합니다. 이는 보고서에 도면을 삽입하거나 썸네일을 생성하거나 CAD 시각화를 웹 페이지에 통합해야 할 때 유용합니다.

## Why adjust CAD size with Aspose.CAD?
- **외부 CAD 소프트웨어가 필요 없음** – 모든 작업이 .NET 코드 내부에서 실행됩니다.  
- **세밀한 제어** 단위, 레이아웃 및 래스터화 옵션에 대한.  
- **크로스 포맷 지원** – 동일한 코드가 DWG, DXF, DWF 등에서 작동합니다.  

## Prerequisites

시작하기 전에 다음을 준비하세요:

- Aspose.CAD for .NET 라이브러리: [Aspose.CAD for .NET 다운로드 페이지](https://releases.aspose.com/cad/net/)에서 라이브러리를 다운로드하고 설치합니다.  
- 샘플 CAD 도면: `sample.dwg`와 같은 파일을 프로젝트의 document 디렉터리에 배치합니다.  

## Import Namespaces

먼저, Aspose.CAD 클래스에 접근할 수 있도록 네임스페이스를 가져옵니다.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Step 1: Load the CAD Drawing

`Image` 객체에 소스 파일을 로드합니다. 이 객체는 메모리 내에서 CAD 도면을 나타내며 이후 모든 작업의 기반이 됩니다.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "sample.dwg";

// Load a CAD drawing in an instance of Image
using (var image = Aspose.CAD.Image.Load(sourceFilePath))
{
    // Your code here...
}
```

## Step 2: Create BmpOptions (or any other raster format)

`BmpOptions`는 벡터 데이터를 비트맵으로 저장할 때 Aspose.CAD가 어떻게 렌더링할지 지정합니다. 대상 형식에 따라 `PngOptions`, `JpegOptions` 등으로 교체할 수 있습니다.

```csharp
Aspose.CAD.ImageOptions.BmpOptions bmpOptions = new Aspose.CAD.ImageOptions.BmpOptions();
```

## Step 3: Set CadRasterizationOptions

`CadRasterizationOptions`는 스케일링, 단위 변환 및 레이아웃 선택을 위한 핵심 설정을 포함합니다. 이를 `BmpOptions`의 `VectorRasterizationOptions` 속성과 연결하면 래스터라이저가 사용자 지정 설정을 사용합니다.

```csharp
Aspose.CAD.ImageOptions.CadRasterizationOptions cadRasterizationOptions = new Aspose.CAD.ImageOptions.CadRasterizationOptions();
bmpOptions.VectorRasterizationOptions = cadRasterizationOptions;
```

## Step 4: Set UnitType (change CAD unit)

여기서는 CAD 단위를 기본값에서 센티미터로 변경합니다. 이 부분이 **change cad unit** 키워드가 위치하는 곳이며 최종 이미지 크기에 직접 영향을 줍니다.

```csharp
cadRasterizationOptions.UnitType = Aspose.CAD.ImageOptions.UnitType.Centimeter;
```

## Step 5: Choose Layouts (set CAD layouts)

도면에 여러 레이아웃(예: Model, Sheet1)이 포함되어 있다면, 래스터화할 레이아웃을 지정합니다. 크기 조정된 출력에 대해 **set cad layouts**를 할 때 올바른 레이아웃을 선택하는 것이 중요합니다.

```csharp
cadRasterizationOptions.Layouts = new string[] { "Model" };
```

## Step 6: Export to BMP (resize CAD drawing)

마지막으로 래스터화된 이미지를 저장합니다. 출력 파일은 구성한 새로운 크기, 단위 및 레이아웃을 반영하며, **resize CAD drawing** 작업을 효과적으로 완료합니다.

```csharp
string outPath = sourceFilePath + ".bmp";
image.Save(outPath, bmpOptions);
```

이제 크기가 조정된 CAD 도면을 나타내는 BMP 파일이 생성되었으며, 추가 처리나 표시를 위해 사용할 수 있습니다.

## Common Issues and Solutions

| 문제 | 발생 원인 | 해결 방법 |
|------|----------|----------|
| 출력이 흐림 | 기본 DPI(인치당 점) 낮음 | 저장하기 전에 `cadRasterizationOptions.Resolution = 300;` 설정 |
| 잘못된 레이아웃 표시 | 레이아웃 이름 오타 | CAD 뷰어나 `Layouts` 컬렉션을 사용해 정확한 레이아웃 이름을 확인 |
| 단위 변환이 부정확함 | 미터법과 영국식 단위 혼용 | `UnitType`이 원하는 측정 시스템과 일치하는지 확인 |

## FAQs

### Q1: Aspose.CAD for .NET은 모든 CAD 형식과 호환됩니까?

Aspose.CAD for .NET은 DWG, DXF, DWF 등 다양한 CAD 형식을 지원합니다. 전체 목록은 [문서](https://reference.aspose.com/cad/net/)를 확인하세요.

### Q2: 여러 레이아웃을 동시에 크기 조정할 수 있나요?

예, `CadRasterizationOptions`의 `Layouts` 배열을 조정하여 여러 레이아웃을 동시에 크기 조정할 수 있습니다.

### Q3: Aspose.CAD for .NET에 대한 지원은 어디서 받을 수 있나요?

커뮤니티 지원 및 도움을 받으려면 [Aspose.CAD 포럼](https://forum.aspose.com/c/cad/19)을 방문하세요.

### Q4: 무료 체험판이 있나요?

예, Aspose.CAD for .NET의 기능을 평가하려면 [무료 체험판](https://releases.aspose.com/)을 이용해볼 수 있습니다.

### Q5: Aspose.CAD for .NET의 임시 라이선스를 어떻게 얻을 수 있나요?

테스트용 임시 라이선스는 [여기](https://purchase.aspose.com/temporary-license/)에서 얻을 수 있습니다.

## Frequently Asked Questions

**Q: 단위 유형을 변경하지 않고 CAD 도면을 어떻게 스케일링하나요?**  
A: `CadRasterizationOptions`의 `Zoom` 속성을 조정합니다(예: `cadRasterizationOptions.Zoom = 2.0;`). 이렇게 하면 원래 단위를 유지하면서 크기를 두 배로 늘릴 수 있습니다.

**Q: BMP 외의 형식으로 내보낼 수 있나요?**  
A: 물론 가능합니다. `BmpOptions`를 `PngOptions`, `JpegOptions` 또는 다른 지원되는 래스터 형식 클래스로 교체하면 됩니다.

**Q: 도면 폴더를 일괄 처리할 수 있나요?**  
A: 예. 디렉터리의 파일들을 순회하면서 동일한 래스터화 로직을 적용하고, 각 출력 파일을 고유한 이름으로 저장하면 됩니다.

---

**마지막 업데이트:** 2026-03-19  
**테스트 환경:** Aspose.CAD for .NET 24.11 (latest at time of writing)  
**작성자:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}