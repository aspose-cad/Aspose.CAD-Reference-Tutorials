---
title: DWG를 규정 준수 PDF로 변환 - Aspose.CAD 튜토리얼
linktitle: DWG를 규정 준수 PDF로 변환
second_title: Aspose.CAD .NET - CAD 및 BIM 파일 형식
description: .NET용 Aspose.CAD를 사용하여 DWG를 규정 준수 PDF로 변환합니다. 단계별 안내를 보려면 튜토리얼을 따르세요.
weight: 13
url: /ko/net/conversion-and-export/converting-dwg-to-compliance-pdf/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DWG를 규정 준수 PDF로 변환 - Aspose.CAD 튜토리얼

## 소개

.NET용 Aspose.CAD를 사용하여 DWG 파일을 규정 준수 PDF로 변환하는 방법에 대한 단계별 튜토리얼에 오신 것을 환영합니다. Aspose.CAD는 개발자가 CAD 파일 형식으로 쉽게 작업할 수 있게 해주는 강력한 .NET API입니다. 이 튜토리얼에서는 자세한 예와 설명을 통해 DWG 파일을 규정 준수 PDF로 변환하는 과정을 안내합니다.

## 전제 조건

시작하기 전에 다음 전제 조건이 충족되었는지 확인하세요.

-  .NET용 Aspose.CAD: Aspose.CAD 라이브러리가 .NET 프로젝트에 통합되어 있는지 확인하세요. 당신은 그것을 다운로드 할 수 있습니다[여기](https://releases.aspose.com/cad/net/).

- 개발 환경: 작동하는 .NET 개발 환경을 설치하고 올바르게 구성되었는지 확인합니다.

- 샘플 DWG 파일: 규정 준수 PDF로 변환하려는 샘플 DWG 파일을 다운로드합니다.

## 네임스페이스 가져오기

.NET 프로젝트에서 Aspose.CAD 기능을 활용하는 데 필요한 네임스페이스를 가져옵니다.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
```

이제 DWG 파일을 규정 준수 PDF로 변환하는 과정을 여러 단계로 나누어 보겠습니다.

## 1단계: DWG 파일 로드

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Bottom_plate.dwg";

Aspose.CAD.Image cadImage = Aspose.CAD.Image.Load(sourceFilePath);
```

## 2단계: 래스터화 옵션 설정

 인스턴스 만들기`CadRasterizationOptions` 배경색, 페이지 너비, 페이지 높이 등의 속성을 구성합니다.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions
{
    BackgroundColor = Aspose.CAD.Color.White,
    PageWidth = 1600,
    PageHeight = 1600
};
```

## 3단계: PDF 옵션 만들기

 인스턴스 만들기`PdfOptions` 벡터 래스터화 옵션을 설정합니다.

```csharp
PdfOptions pdfOptions = new PdfOptions
{
    VectorRasterizationOptions = rasterizationOptions,
    CorePdfOptions = new PdfDocumentOptions { Compliance = PdfCompliance.PdfA1a }
};
```

## 4단계: PDF로 저장(A1a 규정 준수)

CAD 이미지를 A1a 규격 준수 PDF로 저장합니다.

```csharp
cadImage.Save(MyDir + "PDFA1_A.pdf", pdfOptions);
```

## 5단계: PDF로 저장(A1b 규정 준수)

규정 준수 유형을 A1b로 변경하고 CAD 이미지를 규정 준수 PDF로 저장합니다.

```csharp
pdfOptions.CorePdfOptions.Compliance = PdfCompliance.PdfA1b;
cadImage.Save(MyDir + "PDFA1_B.pdf", pdfOptions);
```

## 결론

축하해요! .NET용 Aspose.CAD를 사용하여 DWG 파일을 규정 준수 PDF로 성공적으로 변환했습니다. 이 튜토리얼은 CAD 변환 기능을 애플리케이션에 통합하려는 개발자를 위한 포괄적인 가이드를 제공합니다.

## FAQ

### Q1: Aspose.CAD를 사용하여 다른 CAD 형식을 규정 준수 PDF로 변환할 수 있습니까?

A1: 예, Aspose.CAD는 다양한 CAD 형식을 지원하므로 규정 준수 PDF로 변환할 수 있습니다.

### Q2: Aspose.CAD는 .NET Core와 호환됩니까?

A2: 예, Aspose.CAD는 .NET Framework 및 .NET Core와 모두 호환됩니다.

### Q3: Aspose.CAD에 대한 라이센스 옵션이 있습니까?

 A3: 예, 라이선스 옵션을 탐색할 수 있습니다.[여기](https://purchase.aspose.com/buy).

### Q4: 무료 평가판이 제공됩니까?

 A4: 예, 무료 평가판을 받을 수 있습니다.[여기](https://releases.aspose.com/).

### Q5: Aspose.CAD에 대한 지원은 어디서 받을 수 있나요?

A5: 다음을 방문하세요.[Aspose.CAD 포럼](https://forum.aspose.com/c/cad/19) 지원 관련 문의사항이 있는 경우
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
