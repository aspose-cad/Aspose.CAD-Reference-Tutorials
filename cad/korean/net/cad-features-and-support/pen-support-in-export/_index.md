---
title: .NET용 Aspose.CAD의 사용자 정의 펜 옵션을 사용하여 CAD 내보내기 향상
linktitle: 내보내기 시 펜 지원
second_title: Aspose.CAD .NET - CAD 및 BIM 파일 형식
description: .NET용 Aspose.CAD를 사용하여 CAD 이미지 내보내기를 향상시키는 방법을 알아보세요. PDF, PNG, BMP 등의 멋진 시각적 개체를 위해 펜 옵션을 사용자 정의하세요.
weight: 12
url: /ko/net/cad-features-and-support/pen-support-in-export/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# .NET용 Aspose.CAD의 사용자 정의 펜 옵션을 사용하여 CAD 내보내기 향상

## 소개

.NET용 Aspose.CAD는 CAD(Computer-Aided Design) 파일 작업을 위한 강력한 도구 세트를 제공하여 개발자가 CAD 이미지를 원활하게 조작하고 내보낼 수 있도록 합니다. 주목할만한 기능 중 하나는 내보내기 중 펜 지원으로, 사용자는 CAD 이미지를 PDF, PNG, BMP, GIF, JPEG2000, JPEG, PSD, TIFF 및 WMF와 같은 다양한 형식으로 내보낼 때 펜의 시작 및 끝 캡 설정을 사용자 정의할 수 있습니다.

이 튜토리얼에서는 Aspose.CAD for .NET을 사용하여 내보내기 시 펜 지원의 세부 사항을 살펴보겠습니다. 우리는 각 단계를 세분화하여 프로세스를 안내하는 명확한 설명과 예를 제공할 것입니다.

## 전제 조건

튜토리얼을 시작하기 전에 다음 전제 조건이 충족되었는지 확인하세요.

- 개발 환경에 설치된 .NET용 Aspose.CAD. 다음에서 다운로드할 수 있습니다.[릴리스 페이지](https://releases.aspose.com/cad/net/).

- CAD 파일 형식, 특히 DXF(도면 교환 형식)에 대한 기본 이해.

- C# 프로그래밍 언어에 대한 실무 지식.

## 네임스페이스 가져오기

시작하려면 C# 프로젝트에서 필요한 네임스페이스를 가져와야 합니다.

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Drawing;
using System.Drawing.Drawing2D;
```

## 1단계: 문서 디렉토리 설정

CAD 문서가 있는 디렉토리를 정의합니다.

```csharp
string MyDir = "Your Document Directory";
```

## 2단계: CAD 이미지 로드

Aspose.CAD를 사용하여 CAD 이미지를 로드합니다.

```csharp
string sourceFilePath = MyDir + "conic_pyramid.dxf";
CadImage cadImage = (CadImage)Image.Load(sourceFilePath);
```

## 3단계: 래스터화 옵션 구성

래스터화 및 PDF 옵션을 만들어 내보내기 프로세스를 사용자 정의합니다.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
PdfOptions pdfOptions = new PdfOptions();
```

## 4단계: 펜 옵션 사용자 정의

펜의 시작 및 끝 캡 옵션을 설정합니다.

```csharp
rasterizationOptions.PenOptions = new PenOptions
{
   StartCap = LineCap.Flat,
   EndCap = LineCap.Flat
};
```

## 5단계: 벡터 래스터화 옵션 적용

PDF 옵션에 래스터화 옵션을 적용합니다.

```csharp
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## 6단계: 내보낸 PDF 저장

사용자 정의된 펜 옵션을 사용하여 CAD 이미지를 PDF 파일로 저장합니다.

```csharp
cadImage.Save(MyDir + "9LHATT-A56_generated.pdf", pdfOptions);
```

## 결론

이 튜토리얼에서는 .NET용 Aspose.CAD의 내보내기 기능에서 펜 지원을 살펴보았습니다. 단계별 가이드를 따르면 펜의 시작 및 끝 캡 설정을 쉽게 사용자 정의하여 CAD 이미지 내보내기의 유연성을 높일 수 있습니다.

내보낸 이미지에서 원하는 시각적 효과를 얻으려면 다양한 펜 옵션을 자유롭게 실험해 보세요.

## FAQ

### Q1: PDF 이외의 다른 이미지 형식에 이러한 펜 옵션을 사용할 수 있습니까?

A1: 예, 펜 옵션은 PNG, BMP, GIF, JPEG 등과 같은 다양한 이미지 형식에 적용될 수 있습니다.

### Q2: Aspose.CAD for .NET에 대한 추가 문서는 어디서 찾을 수 있나요?

 A2: 다음을 참조하세요.[선적 서류 비치](https://reference.aspose.com/cad/net/) 포괄적인 정보와 예시를 보려면

### Q3: Aspose.CAD for .NET에 대한 무료 평가판이 있습니까?

 A3: 예, 무료 평가판에 액세스할 수 있습니다.[여기](https://releases.aspose.com/).

### Q4: Aspose.CAD for .NET의 임시 라이선스를 어떻게 얻을 수 있나요?

 A4: 다음을 방문하세요.[임시 라이센스 페이지](https://purchase.aspose.com/temporary-license/) 임시 라이센스 옵션의 경우.

### Q5: Aspose.CAD for .NET에 대한 커뮤니티 지원은 어디서 찾을 수 있나요?

 A5: 커뮤니티에 참여하세요.[Aspose.CAD 포럼](https://forum.aspose.com/c/cad/19).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
