---
title: .NET용 Aspose.CAD에서 배경 및 그리기 색상 설정
linktitle: 배경 및 그리기 색상 설정
second_title: Aspose.CAD .NET - CAD 및 BIM 파일 형식
description: .NET용 마스터 Aspose.CAD. 배경과 그림 색상을 손쉽게 설정하세요. 단계별 가이드를 따르세요.
weight: 15
url: /ko/net/cad-features-and-support/setting-background-and-drawing-colors/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# .NET용 Aspose.CAD에서 배경 및 그리기 색상 설정

## 소개

.NET 개발의 역동적인 세계에서 Aspose.CAD는 CAD(Computer-Aided Design) 파일을 처리하기 위한 강력한 도구로 등장합니다. CAD 도면 조작 기술을 향상시키고 싶다면 이 튜토리얼이 바로 여러분의 관문입니다. .NET용 Aspose.CAD를 사용하여 배경 설정 및 색상 그리기의 복잡성을 자세히 알아보고 명확성과 효율성을 보장하는 단계별 가이드를 제공합니다.

## 전제 조건

이 여정을 시작하기 전에 다음과 같은 전제 조건이 갖추어져 있는지 확인하세요.

- .NET 개발에 대한 기본 이해.
-  .NET용 Aspose.CAD 설치. 아직 안 하신 분들은 다운로드 하시면 됩니다[여기](https://releases.aspose.com/cad/net/).
- 실험용 샘플 CAD 파일입니다. 문서 디렉토리에서 찾을 수 있습니다.

## 네임스페이스 가져오기

.NET 프로젝트에서 필요한 네임스페이스를 가져오는 것부터 시작하세요.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## 1단계: CAD 파일 로드

다음 코드 조각을 사용하여 작업하려는 CAD 파일을 로드하는 것부터 시작하세요.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

using (Image image = Image.Load(sourceFilePath))
{
    // 추가 처리를 위한 코드는 여기에 있습니다.
}
```

## 2단계: 래스터화 옵션 구성

 인스턴스 만들기`CadRasterizationOptions` 배경 및 도면 색상 설정에 대한 속성을 설정합니다.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
rasterizationOptions.BackgroundColor = Color.Beige;
rasterizationOptions.DrawType = CadDrawTypeMode.UseDrawColor;
rasterizationOptions.DrawColor = Color.Blue;
```

## 3단계: PDF로 내보내기

 인스턴스 만들기`PdfOptions` 그리고 설정`VectorRasterizationOptions` 재산:

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;

// CAD를 PDF로 내보내기
image.Save(MyDir + "result_out.pdf", pdfOptions);
```

## 4단계: TIFF로 내보내기

 인스턴스 만들기`TiffOptions` 그리고 설정`VectorRasterizationOptions` 재산:

```csharp
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.VectorRasterizationOptions = rasterizationOptions;

// CAD를 TIFF로 내보내기
image.Save(MyDir + "result_out.tiff", tiffOptions);
```

## 결론

축하해요! .NET용 Aspose.CAD에서 배경 및 도면 색상을 설정하는 방법을 성공적으로 배웠습니다. 이 튜토리얼은 CAD 파일을 손쉽게 조작하는 기술을 제공합니다.

## FAQ

### Q1: 모든 유형의 CAD 파일에 Aspose.CAD for .NET을 사용할 수 있습니까?

A1: 예, Aspose.CAD는 DWG, DXF 및 DGN을 포함한 다양한 CAD 형식을 지원합니다.

### Q2: Aspose.CAD for .NET에 대한 무료 평가판을 사용할 수 있습니까?

 A2: 예, 무료 평가판을 사용해 볼 수 있습니다.[여기](https://releases.aspose.com/).

### Q3: Aspose.CAD for .NET에 대한 자세한 문서는 어디서 찾을 수 있나요?

 A3: 설명서를 참조하세요[여기](https://reference.aspose.com/cad/net/).

### Q4: Aspose.CAD에 대한 임시 라이선스를 어떻게 얻을 수 있나요?

 A4: 임시 라이센스를 얻을 수 있습니다[여기](https://purchase.aspose.com/temporary-license/).

### Q5: 도움이 필요하거나 커뮤니티와 연결하고 싶으십니까?

 A5: 지원 포럼을 방문하세요.[여기](https://forum.aspose.com/c/cad/19).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
