---
date: 2026-09-09
description: Aspose CAD export를 사용하여 .NET에서 특정 DXF 레이아웃을 JPEG 또는 PNG로 변환하는 방법을 배웁니다.
  빠른 결과를 위한 단계별 지침을 따라 보세요.
keywords:
- aspose cad export
- how to export dxf
- convert dxf to jpeg
- batch export dxf
- convert dwf to jpeg
lastmod: 2026-09-09
linktitle: 특정 DXF 레이아웃을 이미지로 내보내기
og_description: Aspose CAD export를 사용하여 .NET에서 특정 DXF 레이아웃을 JPEG 또는 PNG로 변환하는 방법을
  배웁니다. 빠른 결과를 위한 단계별 지침을 따라 보세요.
og_image_alt: Tutorial showing Aspose CAD export of DXF layout to JPEG image in .NET
og_title: Aspose CAD export – 특정 DXF 레이아웃을 이미지로 내보내기
schemas:
- author: Aspose
  dateModified: '2026-09-09'
  description: Learn how to use Aspose CAD export to convert a specific DXF layout
    to JPEG or PNG in .NET. Follow step‑by‑step instructions for fast results.
  headline: Aspose CAD export – exporting a specific DXF layout to an image
  type: TechArticle
- description: Learn how to use Aspose CAD export to convert a specific DXF layout
    to JPEG or PNG in .NET. Follow step‑by‑step instructions for fast results.
  name: Aspose CAD export – exporting a specific DXF layout to an image
  steps:
  - name: set up your project
    text: Create a new .NET project or open an existing one where you plan to implement
      the Aspose.CAD functionality.
  - name: load CAD image
    text: 'Use the following code to load a CAD image from your specified file path:'
  - name: configure rasterization options
    text: 'Set up the rasterization options, specifying the page width and height:'
  - name: iterate over layers
    text: 'Retrieve the layers from the CAD image and iterate through them:'
  - name: export layers to images
    text: For each layer, export it to a JPEG image using the configured options.
      The `JpegOptions` class defines JPEG‑specific settings such as quality and compression
      level. Repeat these steps for each layer in the CAD image.
  type: HowTo
- questions:
  - answer: Yes – you can script a folder scan and call the same export routine for
      each file; the library is optimized for high‑throughput scenarios.
    question: Does Aspose CAD export support batch processing of thousands of files?
  - answer: Absolutely – set the `JpegQuality` property in `RasterizationOptions`
      to a value between 0 and 100.
    question: Can I control the JPEG quality level?
  - answer: Yes – change the `Save` format to `SaveFormat.Png` and adjust any transparency
      settings as needed.
    question: Is it possible to export a layout as a PNG instead of JPEG?
  - answer: Aspose.CAD supports .NET Framework 4.5+, .NET Core 3.1+, .NET 5, .NET
      6 and later.
    question: What .NET versions are officially supported?
  - answer: The engine streams pages to disk and never loads the full document into
      memory, allowing processing of multi‑gigabyte files on modest hardware.
    question: How does Aspose CAD export handle very large drawings?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- aspose cad
- dxf export
- cad to image
- c# cad processing
- cad conversion
title: Aspose CAD export – 특정 DXF 레이아웃을 이미지로 내보내기
url: /ko/net/layout-and-object-handling/exporting-specific-dxf-layout-to-image/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose CAD export – 특정 DXF 레이아웃을 이미지로 내보내기

## 소개

Aspose CAD export를 사용하면 개별 DXF 레이아웃을 포함한 CAD 도면을 JPEG 또는 PNG와 같은 래스터 이미지로 직접 변환할 수 있으며, 서드파티 CAD 소프트웨어가 필요하지 않습니다. 이 튜토리얼에서는 DXF 파일을 로드하고, 필요한 레이아웃을 선택한 뒤, 몇 줄의 .NET 코드로 이미지를 내보내는 방법을 배웁니다.

## 빠른 답변
- **필요한 라이브러리는?** Aspose.CAD for .NET (Aspose CAD export 구성 요소).  
- **한 레이아웃만 내보낼 수 있나요?** 예 – 래스터화하기 전에 특정 레이아웃을 선택할 수 있습니다.  
- **지원되는 출력 형식?** JPEG, PNG, BMP, TIFF 등.  
- **프로덕션에 라이선스가 필요합니까?** 비체험 사용을 위해 유효한 Aspose.CAD 라이선스가 필요합니다.  
- **.NET 6+에서 작동합니까?** 물론입니다 – 라이브러리는 .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7을 대상으로 합니다.

## Aspose CAD export란?

Aspose CAD export는 Aspose.CAD 라이브러리의 일부로, CAD 및 BIM 파일을 래스터 또는 벡터 이미지로 변환합니다. AutoCAD를 설치하지 않고도 모든 레이아웃, 페이지 또는 레이어를 렌더링할 수 있는 단일 호출 API를 제공합니다. 이 구성 요소는 배치 처리, 고해상도 출력 및 안티앨리어싱, 배경색 제어와 같은 고급 렌더링 옵션도 지원합니다.

## DXF 변환에 Aspose CAD export를 사용하는 이유

Aspose CAD export는 **30개 이상의 CAD/BIM 형식**을 지원하며, **10 000 페이지**까지의 파일을 스트리밍으로 메모리 사용량을 **50 MB** 이하로 유지하면서 렌더링할 수 있습니다. 엔진은 선 굵기, 색상 및 해치 패턴을 보존하여 원본 도면과 일치하는 픽셀 완벽 JPEG 출력을 제공합니다. 또한 비용이 많이 드는 데스크톱 CAD 설치가 필요 없으므로 자동화된 변환 파이프라인을 간단하고 비용 효율적으로 만들 수 있습니다.

## 사전 요구 사항

- Aspose.CAD 라이브러리: [release page](https://releases.aspose.com/cad/net/)에서 Aspose.CAD 라이브러리를 다운로드하고 설치합니다.  
- 개발 환경: 머신에 .NET 개발 환경이 설정되어 있는지 확인합니다.

## 네임스페이스 가져오기

.NET 프로젝트에서 Aspose.CAD가 제공하는 기능에 접근하려면 필요한 네임스페이스를 가져와야 합니다:

```csharp
using System;
```

## 특정 DXF 레이아웃을 이미지로 내보내는 방법?

DXF 파일을 로드하고, 원하는 레이아웃을 선택한 뒤, 래스터화 옵션을 구성하고 결과 이미지를 저장합니다. 전체 과정은 몇 번의 메서드 호출만으로 완료되며 일반적인 도면은 1초 미만에 처리됩니다. `CadImage` 클래스는 메모리에 로드된 CAD 도면을 나타내며, 레이어, 레이아웃 및 렌더링 옵션에 접근할 수 있게 해줍니다.

### 단계 1: 프로젝트 설정
Aspose.CAD 기능을 구현할 새 .NET 프로젝트를 만들거나 기존 프로젝트를 엽니다.

### 단계 2: CAD 이미지 로드
지정한 파일 경로에서 CAD 이미지를 로드하는 코드는 다음과 같습니다:

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "for_layers_test.dwf";

using (var image = (Aspose.CAD.FileFormats.Cad.CadImage)Aspose.CAD.Image.Load(sourceFilePath))
{
    // Your code for further steps will go here.
}
```

### 단계 3: 래스터화 옵션 구성
페이지 너비와 높이를 지정하여 래스터화 옵션을 설정합니다:

```csharp
var rasterizationOptions = new Aspose.CAD.ImageOptions.CadRasterizationOptions();
rasterizationOptions.PageWidth = 500;
rasterizationOptions.PageHeight = 500;
```

### 단계 4: 레이어 반복
CAD 이미지에서 레이어를 가져와 반복합니다:

```csharp
var layersList = image.Layers;
foreach (var layerName in layersList.GetLayersNames())
{
    // Your code for further steps will go here.
}
```

### 단계 5: 레이어를 이미지로 내보내기
각 레이어를 구성된 옵션을 사용해 JPEG 이미지로 내보냅니다. `JpegOptions` 클래스는 품질 및 압축 수준과 같은 JPEG 전용 설정을 정의합니다.

```csharp
rasterizationOptions.Layers = new string[] { layerName };
var options = new Aspose.CAD.ImageOptions.JpegOptions();
options.VectorRasterizationOptions = rasterizationOptions;
image.Save(layerName + "_out.jpg", options);
```

CAD 이미지의 각 레이어에 대해 이 단계를 반복합니다.

## DXF 레이아웃을 이미지로 일괄 내보내는 방법

모든 DXF 파일을 폴더에 넣고 각 파일을 순회하면서 원하는 레이아웃을 선택하고 동일한 내보내기 로직을 호출하면 됩니다. 이 방법을 사용하면 한 번에 수십 개의 도면을 변환할 수 있어 자동화 파이프라인에 적합합니다. 동일한 래스터화 및 저장 설정을 재사용하면 배치 전체에 걸쳐 일관된 출력 품질을 보장합니다.

## Aspose CAD로 DWF를 JPEG로 변환하는 방법

Aspose CAD export는 DWF 파일도 처리합니다. `CadImage.Load`로 DWF를 로드하고 동일한 래스터화 옵션을 설정한 뒤 JPEG 형식으로 `Save`를 호출하면 됩니다. API는 DXF 작업 흐름과 동일하므로 동일한 코드 베이스를 재사용할 수 있습니다. 이 일관된 인터페이스는 추가 코드 분기 없이 혼합 CAD 파일 컬렉션을 변환하는 작업을 단순화합니다.

## 일반적인 문제 및 해결책
- **레이아웃 이름 누락:** CAD 파일의 레이어 관리자에 표시된 이름과 레이아웃 식별자가 일치하는지 확인합니다.  
- **대용량 파일 메모리 급증:** 메모리를 낮게 유지하려면 스트리밍을 활성화하는 `LoadOptions`와 함께 `CadImage.Load`를 사용합니다.  
- **색상 오류:** 흰색 캔버스가 필요하면 `RasterizationOptions`의 `BackgroundColor` 속성이 `Color.White`로 설정되어 있는지 확인합니다.

## FAQ

### Q1: Aspose.CAD를 다른 .NET 프레임워크와 함께 사용할 수 있나요?
A1: 예, Aspose.CAD는 다양한 .NET 프레임워크와 호환되며 개발 요구에 유연성을 제공합니다.

### Q2: Aspose.CAD용 임시 라이선스를 제공하나요?
A2: 예, [temporary license page](https://purchase.aspose.com/temporary-license/)에서 Aspose.CAD용 임시 라이선스를 얻을 수 있습니다.

### Q3: Aspose.CAD 지원을 어떻게 받을 수 있나요?
A3: [Aspose.CAD 포럼](https://forum.aspose.com/c/cad/19)을 방문하여 커뮤니티 지원 및 도움을 받으세요.

### Q4: Aspose.CAD의 무료 체험이 있나요?
A4: 예, [Aspose.CAD 무료 체험 페이지](https://releases.aspose.com/)에서 무료 체험을 확인할 수 있습니다.

### Q5: Aspose.CAD에 대한 자세한 문서는 어디서 찾을 수 있나요?
A5: 포괄적인 [Aspose.CAD 문서](https://reference.aspose.com/cad/net/)를 참고하세요.

## 자주 묻는 질문

**Q: Aspose CAD export가 수천 개 파일의 일괄 처리를 지원합니까?**  
A: 예 – 폴더 스캔 스크립트를 작성하고 각 파일에 대해 동일한 내보내기 루틴을 호출할 수 있으며, 라이브러리는 고처리량 시나리오에 최적화되어 있습니다.

**Q: JPEG 품질 수준을 제어할 수 있나요?**  
A: 물론입니다 – `RasterizationOptions`의 `JpegQuality` 속성을 0에서 100 사이의 값으로 설정합니다.

**Q: 레이아웃을 JPEG 대신 PNG로 내보낼 수 있나요?**  
A: 예 – `Save` 형식을 `SaveFormat.Png`로 변경하고 필요에 따라 투명도 설정을 조정합니다.

**Q: 공식적으로 지원되는 .NET 버전은 무엇인가요?**  
A: Aspose.CAD는 .NET Framework 4.5+, .NET Core 3.1+, .NET 5, .NET 6 이상을 지원합니다.

**Q: Aspose CAD export는 매우 큰 도면을 어떻게 처리하나요?**  
A: 엔진은 페이지를 디스크에 스트리밍하고 전체 문서를 메모리에 로드하지 않으므로, 보통 하드웨어에서도 다기가바이트 파일을 처리할 수 있습니다.

**마지막 업데이트:** 2026-09-09  
**테스트 환경:** Aspose.CAD 24.12 for .NET  
**작성자:** Aspose

## 관련 튜토리얼

- [DXF를 PNG로 변환 (Aspose.CAD for .NET)](/cad/net/cad-export-formats/export-cad-layouts-to-raster-image-formats/)
- [Aspose CAD 예제: .NET에서 레이아웃을 래스터 이미지로 변환](/cad/net/cad-drawing-manipulation/convert-layouts-to-raster-image/)
- [CAD 래스터화 옵션 설정 배우기 – Aspose.CAD로 특정 레이아웃을 PDF로 내보내기](/cad/net/advanced-export-techniques/exporting-specific-layouts-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}