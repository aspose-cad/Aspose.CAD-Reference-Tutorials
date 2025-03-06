---
title: DWG를 PDF 또는 래스터 이미지로 내보내기 - Aspose.CAD 가이드
linktitle: DWG를 PDF 또는 래스터 이미지로 내보내기
second_title: Aspose.CAD .NET - CAD 및 BIM 파일 형식
description: .NET용 Aspose.CAD를 사용하여 DWG를 PDF 또는 래스터 이미지로 내보내는 방법에 대한 포괄적인 가이드를 살펴보세요. 이 강력한 라이브러리를 사용하여 단계와 전제 조건을 알아보고 실습해 보세요.
weight: 11
url: /ko/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DWG를 PDF 또는 래스터 이미지로 내보내기 - Aspose.CAD 가이드

## 소개

.NET 애플리케이션에서 DWG 파일을 PDF 또는 래스터 이미지로 원활하게 변환하고 싶으십니까? 더 이상 보지 마세요! 이 단계별 가이드는 강력한 .NET용 Aspose.CAD 라이브러리를 사용하는 프로세스를 안내합니다. 숙련된 개발자이든 이제 막 시작하는 개발자이든 이 튜토리얼은 모든 기술 수준을 충족합니다.

## 전제 조건

튜토리얼을 시작하기 전에 다음 사항이 준비되어 있는지 확인하세요.

- .NET 프로그래밍에 대한 기본적인 이해.
-  .NET 라이브러리용 Aspose.CAD가 설치되었습니다. 그렇지 않은 경우 다운로드하십시오.[여기](https://releases.aspose.com/cad/net/).
- .NET 개발을 위해 선호하는 IDE(통합 개발 환경)가 설정되었습니다.

## 네임스페이스 가져오기

.NET 프로젝트에 필요한 네임스페이스를 가져와서 시작해 보겠습니다. 이렇게 하면 코드에서 Aspose.CAD 기능에 액세스할 수 있습니다.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
```

## 1단계: DWG 파일 로드

변환하려는 DWG 파일을 로드하여 시작하십시오. "문서 디렉토리"를 DWG 파일 경로로 바꾸십시오.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Bottom_plate.dwg";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // DWG를 로드하기 위한 코드는 여기에 있습니다.
}
```

## 2단계: PDF 내보내기 설정

이제 PDF 내보내기 설정을 구성해 보겠습니다. 이 예에서는 레이아웃을 설정하고 단위 변환을 처리하는 방법을 보여줍니다.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.Layouts = new string[] { "Model" };

// 단위계 확인 및 정의
bool currentUnitIsMetric = false;
double currentUnitCoefficient = 1.0;
DefineUnitSystem(cadImage.UnitType, out currentUnitIsMetric, out currentUnitCoefficient);

// PDF 내보내기 설정을 위한 코드는 여기에 있습니다.
```

## 3단계: PDF로 내보내기

구성된 설정을 사용하여 PDF로 내보내기를 실행합니다.

```csharp
PdfOptions pdfOptions = new PdfOptions
{
    VectorRasterizationOptions = rasterizationOptions
};

cadImage.Save(outPath, pdfOptions);
```

## 4단계: 래스터 이미지로 내보내기

PNG와 같은 래스터 이미지로 내보내는 기능을 확장합니다.

```csharp
// 300DPI의 A4 크기 - 2480x3508
rasterizationOptions.PageHeight = 3508;
rasterizationOptions.PageWidth = 2480;

PngOptions pngOptions = new PngOptions
{
    VectorRasterizationOptions = rasterizationOptions
};

cadImage.Save(outPath.Replace("pdf", "png"), pngOptions);
```

## 결론

축하해요! .NET용 Aspose.CAD를 사용하여 DWG 파일을 PDF와 래스터 이미지로 내보내는 방법을 성공적으로 배웠습니다. 이 강력한 라이브러리는 프로세스를 간소화하여 효율적이고 개발자 친화적으로 만듭니다.

## FAQ

### Q1: 상업용 프로젝트에서 Aspose.CAD for .NET을 사용할 수 있나요?

 A1: 네, 가능합니다. 방문하다[buy.aspose.com/buy](https://purchase.aspose.com/buy) 라이선스 세부정보를 확인하세요.

### Q2: 무료 평가판을 이용할 수 있나요?

 A2: 물론이죠! 무료 평가판을 받아보세요[여기](https://releases.aspose.com/).

### Q3: .NET용 Aspose.CAD에 대한 지원을 어떻게 받을 수 있나요?

 A3: 다음으로 가세요.[Aspose.CAD 포럼](https://forum.aspose.com/c/cad/19) 지역 사회 지원을 위해.

### Q4: 테스트 목적으로 임시 라이선스를 얻을 수 있나요?

 A4: 네, 임시 면허를 취득할 수 있습니다.[여기](https://purchase.aspose.com/temporary-license/).

### Q5: 자세한 문서는 어디서 찾을 수 있나요?

 A5: 문서는 다음에서 확인할 수 있습니다.[Aspose.CAD](https://reference.aspose.com/cad/net/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
