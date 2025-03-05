---
title: .NET용 Aspose.CAD에서 캔버스 크기 및 모드 설정
linktitle: 캔버스 크기 및 모드 설정
second_title: Aspose.CAD .NET - CAD 및 BIM 파일 형식
description: .NET용 Aspose.CAD에서 캔버스 크기 및 모드 설정에 대한 단계별 가이드를 살펴보세요. 이 포괄적인 튜토리얼을 사용하여 쉽게 CAD 렌더링을 최적화하십시오.
type: docs
weight: 16
url: /ko/net/cad-features-and-support/setting-canvas-size-and-mode/
---
## 소개

.NET용 Aspose.CAD의 잠재력을 최대한 활용하고 CAD 렌더링 경험을 혁신할 준비가 되셨습니까? 이 단계별 튜토리얼에서는 강력한 Aspose.CAD 라이브러리를 사용하여 캔버스 크기와 모드를 설정하는 복잡한 과정을 살펴보겠습니다. 숙련된 개발자이든 이제 막 시작하는 개발자이든 이 가이드는 Aspose.CAD의 기능을 효과적으로 활용할 수 있도록 프로세스를 안내합니다.

## 전제 조건

튜토리얼을 시작하기 전에 다음 전제 조건이 충족되었는지 확인하세요.

-  Aspose.CAD 라이브러리: Aspose.CAD 라이브러리를 다운로드하여 설치합니다.[Aspose.CAD 웹사이트](https://releases.aspose.com/cad/net/).

- 개발 환경: 컴퓨터에 .NET 개발 환경이 설정되어 있는지 확인하세요.

-  샘플 CAD 파일: 이 튜토리얼에서는 샘플 DXF 파일을 사용합니다. 다음에서 하나를 찾을 수 있습니다.[Aspose.CAD 문서](https://reference.aspose.com/cad/net/).

## 네임스페이스 가져오기

시작하려면 .NET 애플리케이션 시작 부분에서 필요한 네임스페이스를 가져옵니다.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## 1단계: CAD 파일 로드

다음 코드를 사용하여 CAD 파일을 로드하는 것으로 시작합니다.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

using (Image image = Image.Load(sourceFilePath))
{
    //추가 단계를 위한 코드가 여기에 표시됩니다.
}
```

## 2단계: CadRasterizationOptions 생성

 인스턴스 만들기`CadRasterizationOptions` 속성을 설정합니다.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
rasterizationOptions.AutomaticLayoutsScaling = true;
rasterizationOptions.NoScaling = false;
```

## 3단계: PdfOptions 생성

 인스턴스 만들기`PdfOptions` 그리고 그것을 설정`VectorRasterizationOptions` 재산:

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## 4단계: PDF로 내보내기

구성된 옵션을 사용하여 CAD 파일을 PDF로 내보냅니다.

```csharp
image.Save(MyDir + "result_out.pdf", pdfOptions);
```

## 5단계: TiffOptions 생성

 인스턴스 만들기`TiffOptions` 그리고 그것을 설정`VectorRasterizationOptions` 재산:

```csharp
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.VectorRasterizationOptions = rasterizationOptions;
```

## 6단계: TIFF로 내보내기

구성된 옵션을 사용하여 CAD 파일을 TIFF로 내보냅니다.

```csharp
image.Save(MyDir + "result_out.tiff", tiffOptions);
```

## 결론

축하해요! .NET용 Aspose.CAD에서 캔버스 크기와 모드를 성공적으로 설정했습니다. 이 강력한 기능은 CAD 렌더링의 가능성을 열어줍니다. 다양한 옵션을 실험하고 .NET 애플리케이션에서 Aspose.CAD의 모든 잠재력을 발견하십시오.

## FAQ

### Q1: Aspose.CAD를 다른 .NET 라이브러리와 함께 사용할 수 있습니까?

A1: 예, Aspose.CAD는 다른 .NET 라이브러리와 원활하게 통합되어 CAD 조작을 위한 향상된 기능을 제공합니다.

### Q2: Aspose.CAD에 대한 무료 평가판을 사용할 수 있습니까?

 A2: 예, 무료 평가판을 통해 Aspose.CAD의 기능을 탐색할 수 있습니다. 방문하다[여기](https://releases.aspose.com/) 시작하려면.

### Q3: Aspose.CAD에 대한 지원은 어떻게 받을 수 있나요?

 A3: 지원 및 토론을 원하시면 다음을 방문하세요.[Aspose.CAD 포럼](https://forum.aspose.com/c/cad/19).

### Q4: Aspose.CAD에 대한 종합 문서는 어디서 찾을 수 있나요?

 A4: 다음을 참조하세요.[Aspose.CAD 문서](https://reference.aspose.com/cad/net/) 자세한 정보와 예시를 확인하세요.

### Q5: .NET용 Aspose.CAD를 어떻게 구매하나요?

 A5: Aspose.CAD를 구매하려면[구매 페이지](https://purchase.aspose.com/buy).