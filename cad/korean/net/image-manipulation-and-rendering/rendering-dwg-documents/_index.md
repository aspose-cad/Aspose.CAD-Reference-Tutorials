---
date: 2026-08-23
description: Aspose.CAD를 사용하여 C#에서 viewport DWG를 만드는 방법을 배웁니다. 이 가이드는 DWG 파일 로드, rasterization
  구성, viewport 정의 및 결과를 PDF로 저장하는 과정을 다룹니다.
keywords:
- create viewport dwg c#
- render dwg c#
- aspose.cad .net
lastmod: 2026-08-23
linktitle: C#에서 DWG 문서 렌더링
og_description: Aspose.CAD를 사용하여 .NET에서 C#로 viewport DWG를 만드는 방법을 배웁니다. 이 단계별 가이드는
  loading, rasterizing, defining viewports 및 saving to PDF 과정을 보여줍니다.
og_image_alt: Guide showing how to create viewport dwg c# with Aspose.CAD in .NET
og_title: Aspose.CAD for .NET를 사용하여 C#에서 viewport DWG를 만드는 방법
schemas:
- author: Aspose
  dateModified: '2026-08-23'
  description: Learn how to create viewport dwg c# using Aspose.CAD. This guide covers
    loading a DWG file, configuring rasterization, defining a viewport, and saving
    the result as PDF.
  headline: How to create viewport dwg c# with Aspose.CAD for .NET
  type: TechArticle
- questions:
  - answer: Load the DWG file with `CadImage.Load`.
    question: What is the first step?
  - answer: '`Viewport` inside `CadRasterizationOptions`.'
    question: Which class defines the view area?
  - answer: Yes, using `PdfOptions` after rasterization.
    question: Can I output to PDF?
  - answer: A commercial license is required; a free trial works for evaluation.
    question: Do I need a license for production?
  - answer: Absolutely – Aspose.CAD works with .NET Framework, .NET Core, and .NET 5/6.
    question: Is .NET Core supported?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- create viewport dwg c#
- Aspose.CAD
- C# CAD rendering
- DWG to PDF
- CAD viewports
title: Aspose.CAD for .NET를 사용하여 C#에서 viewport DWG를 만드는 방법
url: /ko/net/image-manipulation-and-rendering/rendering-dwg-documents/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# C#에서 DWG 문서 렌더링 – 뷰포트 DWG C# 튜토리얼 만들기

## 소개

이 포괄적인 튜토리얼에서는 Aspose.CAD를 사용하여 **create viewport dwg c#**를 만들고 DWG 파일을 PDF로 렌더링하는 방법을 배웁니다. 특정 레이아웃을 추출하거나 인쇄 가능한 시트를 생성하거나 보고서에 CAD 뷰를 삽입해야 할 경우, 뷰포트를 제어하면 정확한 렌더링 제어가 가능합니다. Aspose.CAD는 **20+ CAD formats**를 지원하며 전체 문서를 메모리에 로드하지 않고도 수천 개의 엔터티가 포함된 파일을 처리할 수 있어 고성능 .NET 애플리케이션에 이상적입니다.

## 빠른 답변

- **첫 번째 단계는 무엇인가요?** `CadImage.Load`를 사용하여 DWG 파일을 로드합니다.
- **뷰 영역을 정의하는 클래스는 무엇인가요?** `CadRasterizationOptions` 안의 `Viewport`.
- **PDF로 출력할 수 있나요?** 래스터화 후 `PdfOptions`를 사용합니다.
- **프로덕션에 라이선스가 필요합니까?** 상용 라이선스가 필요하며, 평가용으로는 무료 체험판을 사용할 수 있습니다.
- **.NET Core가 지원되나요?** 물론입니다 – Aspose.CAD는 .NET Framework, .NET Core 및 .NET 5/6과 함께 작동합니다.

## 전제 조건

Before diving into the code, make sure you have:

- C# 프로그래밍에 대한 기본 지식.
- Visual Studio(최근 버전) 설치.
- 프로젝트에 Aspose.CAD 라이브러리를 추가했습니다. [Aspose.CAD download page](https://releases.aspose.com/cad/net/)에서 다운로드할 수 있습니다.
- 예제로 사용할 **Bottom_plate.dwg**와 같은 샘플 DWG 파일.

## 네임스페이스 가져오기

C# 파일 상단에 필요한 `using` 지시문을 추가하여 컴파일러가 Aspose.CAD 타입을 찾을 수 있도록 합니다.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
using Aspose.CAD.FileFormats.Cad.CadTables;
using Aspose.CAD.FileFormats.Cad;
```

환경이 준비되었으니, 구현 과정을 단계별로 살펴보겠습니다.

## 뷰포트 DWG C#를 만드는 방법?

맞춤 뷰포트를 만들려면 먼저 DWG 파일을 `CadImage` 객체에 로드한 다음, 원하는 레이아웃과 스케일링을 사용하여 `CadRasterizationOptions`를 구성합니다. 표시하려는 영역을 정의하고, 계산된 중심, 높이 및 종횡비를 사용하여 `CadVportTableObject`를 인스턴스화합니다. 활성 뷰포트를 교체하고 PDF 옵션을 설정한 뒤 최종적으로 결과를 저장합니다.

## 1단계: dwg 파일 로드

`CadImage.Load`는 DWG 파일을 `CadImage` 객체에 로드하며, 이는 메모리 내에서 CAD 도면을 나타냅니다.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Bottom_plate.dwg";
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Your code for loading the DWG file goes here.
}
```

## 2단계: 래스터화 옵션 구성

`CadRasterizationOptions`는 레이아웃 선택, 스케일링 및 출력 크기를 포함하여 CAD 도면이 어떻게 래스터화되는지를 지정합니다.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.Layouts = new string[] { "Model" };
rasterizationOptions.NoScaling = true;
// Additional rasterization configurations can be added here.
```

## 3단계: 그릴 영역 정의

`Point`는 렌더링할 영역의 좌상단 모서리 X 및 Y 좌표를 정의합니다.

```csharp
Point topLeft = new Point(6156, 7053);
double width = 3108;
double height = 2489;
```

## 4단계: 새 뷰포트 생성

`CadVportTableObject`는 렌더링된 도면의 표시 영역과 종횡비를 제어하는 뷰포트 객체를 나타냅니다.

```csharp
CadVportTableObject newView = new CadVportTableObject();
newView.Name.Value = "*Active";
newView.CenterPoint.X = topLeft.X + width / 2f;
newView.CenterPoint.Y = topLeft.Y - height / 2f;
newView.ViewHeight.Value = height;
newView.ViewAspectRatio.Value = width / height;
```

## 5단계: 활성 뷰포트 교체

루프는 새로 만든 뷰포트로 활성 뷰포트를 교체하여 맞춤 뷰 설정을 적용합니다.

```csharp
for (int i = 0; i < cadImage.ViewPorts.Count; i++)
{
    CadVportTableObject currentView = (CadVportTableObject)(cadImage.ViewPorts[i]);
    if ((currentView.Name.Value == null && cadImage.ViewPorts.Count == 1) ||
    string.Equals(currentView.Name.Value.ToLowerInvariant(), "*active"))
    {
        cadImage.ViewPorts[i] = newView;
        break;
    }
}
```

## 6단계: PDF 옵션 구성

`PdfOptions`는 압축 및 메타데이터와 같은 PDF 출력 매개변수를 구성합니다.

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## 7단계: 렌더링된 dwg를 PDF로 저장

`image.Save`는 지정된 형식 옵션을 사용하여 렌더링된 이미지를 파일에 기록합니다.

```csharp
cadImage.Save(MyDir, pdfOptions);
```

## DWG 렌더링 시 맞춤 뷰포트를 사용하는 이유

맞춤 뷰포트를 사용하면 특정 레이아웃이나 영역을 분리하여 파일 크기를 줄이고 렌더링 속도를 향상시킬 수 있습니다. 집중된 뷰포트를 사용할 경우 Aspose.CAD는 300페이지 DWG를 2초 미만에 렌더링할 수 있으며, 전체 도면을 렌더링할 때보다 몇 초 정도 더 빠릅니다.

## 일반적인 문제 및 해결책

- **Blank output** – 뷰포트 좌표가 도면 범위 내에 있는지 확인하고, `CadImage.Size`를 사용하여 경계를 검증하십시오.
- **Missing layers** – `CadRasterizationOptions.Layouts`를 올바른 레이아웃 이름으로 설정하십시오; 그렇지 않으면 기본 레이아웃이 비어 있을 수 있습니다.
- **Performance slowdown** – 빠른 미리보기가 필요할 경우 `CadRasterizationOptions`에서 안티앨리어싱을 비활성화하십시오.

## 자주 묻는 질문

### Q1: Aspose.CAD를 다른 CAD 파일 형식과 함께 사용할 수 있나요?

A1: 예, Aspose.CAD는 DWG, DXF, DWF를 포함한 다양한 형식을 지원하며 20가지 이상의 추가 CAD 유형을 지원합니다.

### Q2: Aspose.CAD가 .NET Core와 호환되나요?

A2: 예, Aspose.CAD는 .NET Framework, .NET Core 및 최신 .NET 릴리스와 함께 작동합니다.

### Q3: DWG 파일에서 서로 다른 레이아웃을 어떻게 처리할 수 있나요?

A3: 렌더링 전에 `CadRasterizationOptions`의 `Layouts` 속성을 사용하여 원하는 레이아웃을 지정합니다.

### Q4: Aspose.CAD 사용 시 라이선스 고려 사항이 있나요?

A4: 라이선스 상세 정보는 [Aspose.CAD licensing page](https://purchase.aspose.com/buy)에서 확인하십시오.

### Q5: 추가 지원을 어디서 찾을 수 있나요?

A5: 커뮤니티 도움 및 토론을 위해 [Aspose.CAD forum](https://forum.aspose.com/c/cad/19)을 방문하십시오.

### Q6: PDF 대신 PNG로 직접 렌더링할 수 있나요?

A6: 예, `PdfOptions`를 `PngOptions`로 변경하고 `image.Save("output.png", pngOptions)`를 호출합니다.

### Q7: 렌더링된 이미지를 Windows Forms 애플리케이션에 어떻게 삽입하나요?

A7: `Image.FromFile("output.png")`를 사용하여 저장된 이미지를 `PictureBox` 컨트롤에 로드합니다.

## 결론

이제 **create viewport dwg c#**를 수행하고 Aspose.CAD를 사용하여 DWG 파일을 PDF(또는 기타 래스터 형식)로 렌더링하는 방법을 알게 되었습니다. 뷰포트 조작을 마스터하면 시각적 출력에 대한 세밀한 제어를 얻을 수 있으며, 이는 정확한 엔지니어링 도면, 보고서 또는 썸네일을 생성하는 데 필수적입니다. 추가 래스터화 설정을 탐색하고 다양한 출력 형식을 실험하며 코드를 더 큰 .NET 서비스나 데스크톱 유틸리티에 통합해 보세요.

---

**마지막 업데이트:** 2026-08-23  
**테스트 환경:** Aspose.CAD 24.11 for .NET  
**작성자:** Aspose

## 관련 튜토리얼

- [C#에서 좌표와 함께 DWG를 PDF로 변환하면서 뷰포트를 설정하는 방법 - Aspose.CAD 튜토리얼](/cad/net/conversion-and-export/converting-dwg-to-pdf-with-coordinates/)
- [CAD 래스터화 옵션 설정 방법 – Aspose.CAD를 사용하여 특정 레이아웃을 PDF로 내보내기](/cad/net/advanced-export-techniques/exporting-specific-layouts-to-pdf/)
- [Aspose.CAD for .NET을 사용하여 DWG를 PDF 및 래스터 이미지로 변환하는 방법](/cad/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}