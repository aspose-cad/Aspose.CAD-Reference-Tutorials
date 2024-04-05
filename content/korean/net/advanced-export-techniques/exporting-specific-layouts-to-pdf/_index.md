---
title: 특정 레이아웃을 PDF로 내보내기 - Aspose.CAD 가이드
linktitle: 특정 레이아웃을 PDF로 내보내기
second_title: Aspose.CAD .NET - CAD 및 BIM 파일 형식
description: .NET용 Aspose.CAD를 사용하여 특정 레이아웃을 PDF로 내보내는 방법을 알아보세요. 원활한 통합을 위한 단계별 가이드입니다.
type: docs
weight: 13
url: /ko/net/advanced-export-techniques/exporting-specific-layouts-to-pdf/
---
## 소개

.NET용 Aspose.CAD를 사용하여 특정 레이아웃을 PDF로 내보내는 방법에 대한 단계별 가이드에 오신 것을 환영합니다. Aspose.CAD는 개발자가 CAD 파일 형식을 원활하게 사용할 수 있게 해주는 강력한 라이브러리입니다. 이 튜토리얼에서는 .NET 환경에서 Aspose.CAD를 사용하여 DWG 파일의 특정 레이아웃을 PDF로 내보내는 데 중점을 둘 것입니다.

## 전제 조건

튜토리얼을 시작하기 전에 다음 전제 조건이 충족되었는지 확인하세요.

-  .NET 라이브러리용 Aspose.CAD: Aspose.CAD 라이브러리가 설치되어 있는지 확인하세요. 당신은 그것을 다운로드 할 수 있습니다[여기](https://releases.aspose.com/cad/net/).

- 개발 환경: Visual Studio와 같은 .NET 개발 환경을 설정합니다.

## 네임스페이스 가져오기

.NET 프로젝트에서 Aspose.CAD에 필요한 네임스페이스를 가져옵니다.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## 1단계: DWG 파일 로드

```csharp
// 문서 디렉터리의 경로입니다.
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "visualization_-_conference_room.dwg";

using (Image image = Image.Load(sourceFilePath))
{
    // 추가 단계에 대한 코드는 여기에 있습니다.
}
```

## 2단계: CadRasterizationOptions 설정

```csharp
// CadRasterizationOptions 인스턴스를 생성하고 다양한 속성을 설정합니다.
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
```

## 3단계: 레이아웃 이름 지정

```csharp
// 원하는 레이아웃 이름을 지정하세요.
rasterizationOptions.Layouts = new string[] { "Layout1" };
```

## 4단계: PdfOptions 생성

```csharp
// PdfOptions 인스턴스 만들기
PdfOptions pdfOptions = new PdfOptions();
// VectorRasterizationOptions 속성 설정
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## 5단계: PDF로 내보내기

```csharp
MyDir = MyDir + "ExportSpecificLayoutToPDF_out.pdf";
// DWG를 PDF로 내보내기
image.Save(MyDir, pdfOptions);
```

## 6단계: 성공 메시지 표시

```csharp
// 성공 메시지 표시
Console.WriteLine("\nThe DWG file with a specific layout exported successfully to PDF.\nFile saved at " + MyDir);
```

## 결론

축하해요! .NET용 Aspose.CAD를 사용하여 특정 레이아웃을 PDF로 내보내는 방법을 성공적으로 배웠습니다. 이 가이드에서는 이 기능을 프로젝트에 쉽게 통합할 수 있도록 자세한 연습을 제공합니다.

## FAQ

### Q1: 여러 레이아웃을 동시에 내보낼 수 있나요?

 A1: 예, 간단히 수정하면 됩니다.`Layouts` 원하는 모든 레이아웃의 이름을 포함하려면 3단계의 배열을 사용하세요.

### Q2: Aspose.CAD는 다른 CAD 파일 형식과 호환됩니까?

A2: 예, Aspose.CAD는 DWG, DXF, DWF 등을 포함한 다양한 CAD 형식을 지원합니다.

### Q3: PDF 출력 설정을 어떻게 조정할 수 있습니까?

 A3: 다음의 속성을 살펴보세요.`CadRasterizationOptions` 사용자 정의 옵션은 2단계에서 확인하세요.

### Q4: 추가 Aspose.CAD 문서는 어디서 찾을 수 있나요?

 A4: 다음을 방문하세요.[선적 서류 비치](https://reference.aspose.com/cad/net/) 자세한 정보를 확인하세요.

### Q5: 무료 평가판이 제공됩니까?

 A5: 예, 무료 평가판에 액세스할 수 있습니다.[여기](https://releases.aspose.com/).