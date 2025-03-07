---
title: DXF 특정 레이아웃을 PDF로 내보내기 - Aspose.CAD 가이드
linktitle: DXF 특정 레이아웃을 PDF로 내보내기
second_title: Aspose.CAD .NET - CAD 및 BIM 파일 형식
description: .NET용 Aspose.CAD를 사용하여 DXF 특정 레이아웃을 PDF로 내보내는 방법을 알아보세요. 효율적이고 고품질의 변환을 위한 단계별 가이드를 따르세요.
weight: 11
url: /ko/net/export-techniques/exporting-dxf-specific-layout-to-pdf/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DXF 특정 레이아웃을 PDF로 내보내기 - Aspose.CAD 가이드

## 소개

.NET용 Aspose.CAD의 강력한 기능을 사용하여 DXF 특정 레이아웃을 PDF로 내보내는 방법에 대한 Aspose.CAD 튜토리얼에 오신 것을 환영합니다. 이 단계별 가이드는 "모델"이라는 특정 레이아웃에 초점을 맞춰 DXF 파일을 PDF로 변환하는 과정을 안내합니다. Aspose.CAD는 변환 프로세스를 간소화하는 효율적인 도구와 기능을 제공하여 CAD 도면의 고품질 출력을 보장합니다.

## 전제 조건

튜토리얼을 시작하기 전에 다음 전제 조건이 충족되었는지 확인하세요.

- .NET용 Aspose.CAD: .NET 프로젝트에 Aspose.CAD 라이브러리가 설치되어 있는지 확인하세요. 당신은 그것을 다운로드 할 수 있습니다[여기](https://releases.aspose.com/cad/net/) 설명서에 제공된 설치 지침을 따르세요.

- 개발 환경: Visual Studio 또는 기타 선호하는 IDE를 포함하여 작동하는 .NET 개발 환경을 설정합니다.

- DXF 파일: PDF로 변환하려는 DXF 파일을 준비합니다. 이 가이드에서는 "conic_pyramid.dxf"라는 예제 파일을 사용합니다.

## 네임스페이스 가져오기

.NET 프로젝트에 Aspose.CAD 기능을 활용하는 데 필요한 네임스페이스를 포함합니다. 코드 시작 부분에 다음 줄을 추가합니다.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
namespace Aspose.CAD.Examples.CSharp.DXF_Drawings

```

## 1단계: DXF 파일 로드

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

using (Image image = Image.Load(sourceFilePath))
{
    //추가 단계를 위한 코드가 여기에 표시됩니다.
}
```

## 2단계: 래스터화 옵션 설정

```csharp
// CadRasterizationOptions 인스턴스를 생성하고 다양한 속성을 설정합니다.
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
// 원하는 레이아웃 이름을 지정하세요.
rasterizationOptions.Layouts = new string[] { "Model" };
```

## 3단계: PDF 옵션 설정

```csharp
// PdfOptions 인스턴스 만들기
PdfOptions pdfOptions = new PdfOptions();
// VectorRasterizationOptions 속성 설정
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## 4단계: 출력 경로 정의

```csharp
MyDir = MyDir + "conic_pyramid_layout_out.pdf";
```

## 5단계: DXF를 PDF로 내보내기

```csharp
// DXF를 PDF로 내보내기
image.Save(MyDir, pdfOptions);
```

## 6단계: 성공 메시지 표시

```csharp
// 성공 메시지 표시
Console.WriteLine("\nThe DXF file with the specific layout exported successfully to PDF.\nFile saved at " + MyDir);
```

## 결론

축하해요! Aspose.CAD for .NET을 사용하여 특정 레이아웃이 포함된 DXF 파일을 PDF로 내보내는 방법을 성공적으로 배웠습니다. 이 가이드에서는 DXF 파일 로드부터 래스터화 옵션 설정 및 PDF로 내보내기까지 필수 단계를 다루었습니다.

## FAQ

### Q1: Aspose.CAD는 모든 버전의 DXF 파일과 호환됩니까?

 A1: Aspose.CAD는 다양한 버전의 DXF 파일을 지원합니다. 다음을 참조하세요.[선적 서류 비치](https://reference.aspose.com/cad/net/) 지원되는 버전 목록을 보려면

### Q2: PDF 출력 설정을 사용자 정의할 수 있습니까?

A2: 예, 속성을 조정하여 PDF 출력 설정을 사용자 정의할 수 있습니다.`CadRasterizationOptions` 그리고`PdfOptions` 귀하의 요구 사항에 따라.

### Q3: Aspose.CAD에 대한 무료 평가판이 있습니까?

 A3: 예, 다음 사이트를 방문하여 무료 평가판으로 Aspose.CAD를 탐색할 수 있습니다.[여기](https://releases.aspose.com/).

### Q4: Aspose.CAD에 대한 지원은 어떻게 받을 수 있나요?

 A4: 지원이나 문의 사항이 있는 경우 다음을 방문하세요.[Aspose.CAD 포럼](https://forum.aspose.com/c/cad/19).

### Q5: Aspose.CAD 라이선스는 어디서 구입할 수 있나요?

 A5: Aspose.CAD 라이선스를 구매할 수 있습니다.[여기](https://purchase.aspose.com/buy).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
