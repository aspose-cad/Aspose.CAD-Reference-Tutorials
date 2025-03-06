---
title: .NET용 Aspose.CAD에서 DGN V7 지원
linktitle: DGN V7 지원
second_title: Aspose.CAD .NET - CAD 및 BIM 파일 형식
description: DGN V7에 대한 .NET의 원활한 지원을 위한 Aspose.CAD를 살펴보세요. 단계별 안내에 따라 DGN 파일을 래스터 이미지로 손쉽게 변환하세요.
weight: 19
url: /ko/net/cad-features-and-support/support-for-dgn-v7/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# .NET용 Aspose.CAD에서 DGN V7 지원

## 소개

.NET 개발 영역에서 Aspose.CAD는 CAD(Computer-Aided Design) 파일을 처리하기 위한 강력한 라이브러리로 돋보입니다. 이 튜토리얼에서는 .NET용 Aspose.CAD의 특정 기능인 DGN V7 파일 지원에 대해 자세히 설명합니다. Design의 약자인 DGN은 CAD 분야에서 널리 사용되는 파일 형식입니다. Aspose.CAD는 DGN V7 파일 작업 프로세스를 단순화하여 개발자에게 원활한 경험을 제공합니다.

## 전제 조건

구현을 시작하기 전에 다음 전제 조건이 충족되었는지 확인하세요.

-  .NET용 Aspose.CAD: Aspose.CAD 라이브러리가 설치되어 있는지 확인하세요. 다음에서 다운로드할 수 있습니다.[웹사이트](https://releases.aspose.com/cad/net/).

- 개발 환경: Visual Studio 또는 기타 선호하는 IDE를 포함하여 작동하는 .NET 개발 환경을 설정합니다.

이제 전제 조건이 정렬되었으므로 .NET용 Aspose.CAD에서 DGN V7 지원을 활용하는 방법을 살펴보겠습니다.

## 네임스페이스 가져오기

Aspose.CAD의 기능에 액세스하려면 필요한 네임스페이스를 가져오는 것부터 시작하세요.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## 1단계: DGN 파일 로드

 기존 DGN 파일을`CadImage` 바꾸다`"Your Document Directory"` 그리고`"Nikon_D90_Camera.dgn"` 적절한 디렉토리 경로와 파일 이름을 사용하십시오.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // 추가 단계에 대한 코드는 여기에 있습니다...
}
```

## 2단계: 래스터화 옵션 구성

 만들기`CadRasterizationOptions` 래스터화와 관련된 다양한 속성을 정의하고 설정하는 객체입니다.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions
{
    PageWidth = 600,
    PageHeight = 300,
    NoScaling = true,
    AutomaticLayoutsScaling = false
};
```

## 3단계: 벡터 래스터화 옵션 설정

 만들기`JpegOptions` DGN 파일을 JPEG로 변환하려고 합니다. 이전에 만든 할당`CadRasterizationOptions` 그것에 반대합니다.

```csharp
ImageOptionsBase options = new JpegOptions
{
    VectorRasterizationOptions = rasterizationOptions
};
```

## 4단계: 래스터화된 이미지 저장

 를 불러`Save` 의 방법`CadImage` DGN 파일을 래스터 이미지(이 경우 JPEG)로 내보내는 클래스 객체입니다.

```csharp
cadImage.Save(MyDir + "ExportDGNToRasterImage_out.jpeg", options);
```

이러한 단계가 완료되면 DGN 파일이 래스터 이미지로 성공적으로 내보내집니다.

## 결론

이 튜토리얼에서는 .NET용 Aspose.CAD에서 DGN V7에 대한 원활한 지원을 살펴보았습니다. 단계별 가이드를 따르면 개발자는 DGN 파일을 래스터 이미지로 쉽게 변환하여 .NET 응용 프로그램의 기능을 확장할 수 있습니다.

## FAQ

### Q1: Aspose.CAD는 최신 DGN V7 사양과 호환됩니까?

A1: 예, Aspose.CAD는 DGN V7 파일을 원활하게 처리하도록 설계되어 최신 사양과의 호환성을 보장합니다.

### Q2: DGN 파일 변환을 위한 래스터화 옵션을 사용자 정의할 수 있습니까?

 A2: 물론이죠. 튜토리얼에서는 생성 및 구성 방법을 보여줍니다.`CadRasterizationOptions` 변환 프로세스를 맞춤화합니다.

### Q3: JPEG 외에 지원되는 다른 출력 형식이 있습니까?

A3: 예, Aspose.CAD는 다양한 출력 형식을 지원합니다. 포괄적인 목록에 대한 설명서를 탐색할 수 있습니다.

### Q4: Aspose.CAD 관련 쿼리에 대한 지원은 어떻게 받을 수 있나요?

 A4: 다음을 방문하세요.[Aspose.CAD 포럼](https://forum.aspose.com/c/cad/19) 커뮤니티 지원 및 토론을 위해.

### Q5: Aspose.CAD for .NET에 대한 무료 평가판이 있습니까?

 A5: 예, 무료 평가판에 액세스할 수 있습니다.[여기](https://releases.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
