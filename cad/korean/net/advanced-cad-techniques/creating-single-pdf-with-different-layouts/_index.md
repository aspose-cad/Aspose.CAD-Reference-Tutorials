---
title: 다양한 레이아웃으로 단일 PDF 만들기 - Aspose.CAD 가이드
linktitle: 다양한 레이아웃으로 단일 PDF 만들기
second_title: Aspose.CAD .NET - CAD 및 BIM 파일 형식
description: .NET용 Aspose.CAD를 사용하여 다양한 레이아웃으로 단일 PDF를 만듭니다. 원활한 통합과 효율적인 PDF 생성을 위한 단계별 가이드를 따르세요.
type: docs
weight: 13
url: /ko/net/advanced-cad-techniques/creating-single-pdf-with-different-layouts/
---
## 소개

Aspose.CAD for .NET을 사용하여 다양한 레이아웃의 CAD 도면에서 단일 PDF 문서를 생성하려고 하시나요? 이 단계별 가이드는 원활한 통합과 효율적인 PDF 생성을 달성하는 데 도움이 되는 프로세스를 안내합니다. .NET용 Aspose.CAD는 프로그래밍 방식으로 CAD 도면을 조작할 수 있는 강력한 기능을 제공하며, 이 튜토리얼에서는 다양한 레이아웃으로 단일 PDF를 만드는 데 중점을 둘 것입니다.

## 전제 조건

튜토리얼을 시작하기 전에 다음 전제조건이 충족되었는지 확인하십시오.

-  .NET용 Aspose.CAD: .NET용 Aspose.CAD가 설치되어 있는지 확인하세요. 다음에서 다운로드할 수 있습니다.[여기](https://releases.aspose.com/cad/net/).

- 개발 환경: .NET 개발 환경을 설정하고 C# 프로그래밍에 대한 기본 지식을 갖추고 있습니다.

## 네임스페이스 가져오기

C# 프로젝트에서 .NET용 Aspose.CAD의 기능을 활용하는 데 필요한 네임스페이스를 포함합니다.

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## 1단계: CAD 이미지 로드

```csharp
// 문서 디렉터리의 경로입니다.
string MyDir = "Your Document Directory";

using (CadImage cadImage = (CadImage)Image.Load(MyDir + "City skyway map.dwg"))
{
    // 1단계의 코드가 여기에 표시됩니다.
}
```

## 2단계: 래스터화 옵션 사용자 정의

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1000;
rasterizationOptions.PageHeight = 1000;

// 여러 레이아웃에 대한 사용자 정의 크기
rasterizationOptions.LayoutPageSizes.Add("ANSI C Plot", new SizeF(500, 1000));
rasterizationOptions.LayoutPageSizes.Add("8.5 x 11 Plot", new SizeF(1000, 100));
```

## 3단계: PDF 옵션 정의

```csharp
PdfOptions pdfOptions = new PdfOptions() { VectorRasterizationOptions = rasterizationOptions };
```

## 4단계: PDF로 저장

```csharp
cadImage.Save(MyDir + "singlePDF_out.pdf", pdfOptions);
```

이제 Aspose.CAD for .NET을 사용하여 다양한 레이아웃의 단일 PDF 문서를 성공적으로 만들었습니다. 자유롭게 더 많은 기능을 살펴보고 특정 요구 사항에 따라 코드를 맞춤설정해 보세요.

## 결론

이 튜토리얼에서는 Aspose.CAD for .NET을 사용하여 다양한 레이아웃의 CAD 도면에서 단일 PDF를 만드는 과정을 다루었습니다. 이 강력한 라이브러리는 CAD 조작 작업을 단순화하고 다양한 시나리오에 대한 유연성을 제공합니다.

## FAQ

### Q1: Aspose.CAD for .NET을 다른 CAD 형식과 함께 사용할 수 있습니까?

A1: 예, .NET용 Aspose.CAD는 DWG, DXF, DGN 등과 같은 다양한 CAD 형식을 지원합니다.

### Q2: 무료 평가판을 이용할 수 있나요?

 A2: 예, 무료 평가판을 사용해 볼 수 있습니다.[여기](https://releases.aspose.com/).

### Q3: .NET용 Aspose.CAD에 대한 지원을 어떻게 받을 수 있나요?

 A3: 다음을 방문하세요.[Aspose.CAD 포럼](https://forum.aspose.com/c/cad/19) 지역 사회 지원을 위해.

### Q4: 자세한 문서는 어디서 찾을 수 있나요?

 A4: 설명서를 참조하세요[여기](https://reference.aspose.com/cad/net/).

### Q5: .NET용 Aspose.CAD 라이선스를 구입할 수 있나요?

 A5: 예, 라이센스를 구입할 수 있습니다.[여기](https://purchase.aspose.com/buy).