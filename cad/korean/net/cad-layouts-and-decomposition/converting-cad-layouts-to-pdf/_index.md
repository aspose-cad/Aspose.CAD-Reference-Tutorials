---
title: CAD 레이아웃을 PDF로 변환 - Aspose.CAD 튜토리얼
linktitle: CAD 레이아웃을 PDF로 변환
second_title: Aspose.CAD .NET - CAD 및 BIM 파일 형식
description: Aspose.CAD for .NET을 사용하여 CAD 레이아웃을 PDF로 손쉽게 변환하세요. 원활한 통합을 위한 단계별 가이드를 따르세요.
weight: 10
url: /ko/net/cad-layouts-and-decomposition/converting-cad-layouts-to-pdf/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# CAD 레이아웃을 PDF로 변환 - Aspose.CAD 튜토리얼

## 소개

CAD 레이아웃을 PDF로 원활하게 변환하고 싶으십니까? .NET용 Aspose.CAD는 이 프로세스를 효율적이고 간단하게 만드는 강력한 솔루션을 제공합니다. 이 튜토리얼에서는 개발자가 CAD 파일을 쉽게 작업할 수 있도록 지원하는 강력한 API인 Aspose.CAD를 사용하는 단계를 안내합니다.

## 전제 조건

튜토리얼을 시작하기 전에 다음 전제조건이 충족되었는지 확인하십시오.

-  .NET용 Aspose.CAD: 라이브러리를 다운로드하고 설치합니다. 당신은 그것을 찾을 수 있습니다[여기](https://releases.aspose.com/cad/net/).

- .NET 환경: 작동하는 .NET 개발 환경이 있는지 확인하세요.

- 샘플 CAD 파일: 변환할 샘플 CAD 파일을 준비합니다. 이 튜토리얼에서는 "conic_pyramid.dxf"를 사용합니다.

## 네임스페이스 가져오기

필요한 네임스페이스를 .NET 프로젝트로 가져오는 것부터 시작하세요. 이 단계에서는 Aspose.CAD 기능에 액세스할 수 있는지 확인합니다.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
using Aspose.CAD.FileFormats.Cad;
```

## 1단계: 프로젝트 설정

.NET 프로젝트를 설정하여 시작하세요. 새 프로젝트를 생성하거나 CAD에서 PDF로의 변환을 구현하려는 기존 프로젝트를 엽니다.

## 2단계: 소스 CAD 파일 경로 정의

CAD 파일의 경로를 지정합니다. 이 예에서 소스 파일은 "conic_pyramid.dxf"입니다.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";
```

## 3단계: CAD 파일 로드

CadImage 클래스의 인스턴스를 만들고 CAD 파일을 응용 프로그램에 로드합니다.

```csharp
using (Aspose.CAD.Image cadImage = (Aspose.CAD.Image)Image.Load(sourceFilePath))
```

## 4단계: 래스터화 옵션 구성

PDF 출력을 사용자 정의하려면 래스터화 옵션을 구성하십시오. 페이지 크기, 레이아웃 크기 조정 및 기타 관련 매개변수를 설정합니다.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
// 기타 구성 옵션...
```

## 5단계: 레이아웃 설정

PDF에 포함할 레이아웃을 지정합니다. 이 예에서는 "모델" 레이아웃을 사용합니다.

```csharp
rasterizationOptions.Layouts = new string[] { "Model" };
```

## 6단계: PDF 옵션 정의

PdfOptions 클래스의 인스턴스를 만들고 이를 래스터화 옵션과 연결합니다.

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## 7단계: 그래픽 옵션 설정

다듬기 모드, 텍스트 렌더링 및 보간을 포함하여 PDF에 대한 그래픽 옵션을 구성합니다.

```csharp
rasterizationOptions.GraphicsOptions.SmoothingMode = SmoothingMode.HighQuality;
rasterizationOptions.GraphicsOptions.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
rasterizationOptions.GraphicsOptions.InterpolationMode = InterpolationMode.HighQualityBicubic;
```

## 8단계: PDF로 저장

PDF 파일의 출력 경로를 지정하고 CAD 레이아웃을 PDF로 저장합니다.

```csharp
MyDir = MyDir + "CADLayoutsToPDF_out.pdf";
cadImage.Save(MyDir, pdfOptions);
```

## 결론

축하해요! Aspose.CAD for .NET을 사용하여 CAD 레이아웃을 PDF로 성공적으로 변환했습니다. 이 튜토리얼은 애플리케이션에서 이 프로세스를 간소화하려는 개발자를 위한 포괄적인 가이드를 제공합니다.

## FAQ

### Q1: 여러 CAD 레이아웃을 한 번에 변환할 수 있습니까?

 A1: 예, 여러 레이아웃을 지정할 수 있습니다.`Layouts` PDF에 포함시키려면 배열을 선택하세요.

### Q2: 지원되는 CAD 파일 형식에 제한이 있습니까?

A2: Aspose.CAD for .NET은 DWG 및 DXF를 포함한 다양한 CAD 형식을 지원합니다.

### Q3: PDF 출력의 모양을 어떻게 사용자 정의할 수 있습니까?

A3: 제공된 래스터화 및 그래픽 옵션을 사용하여 PDF 출력을 원하는 대로 조정하세요.

### Q4: Aspose.CAD for .NET에 사용할 수 있는 평가판이 있습니까?

 A4: 예, 다음을 통해 기능을 탐색할 수 있습니다.[무료 평가판](https://releases.aspose.com/).

### Q5: 어디서 지원을 받거나 질문을 할 수 있나요?

A5: 다음을 방문하세요.[Aspose.CAD 포럼](https://forum.aspose.com/c/cad/19) 도움과 토론을 위해.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
