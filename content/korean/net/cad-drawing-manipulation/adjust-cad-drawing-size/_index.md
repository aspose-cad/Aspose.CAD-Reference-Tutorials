---
title: .NET용 Aspose.CAD에서 CAD 도면 크기 조정
linktitle: CAD 도면 크기 조정
second_title: Aspose.CAD .NET - CAD 및 BIM 파일 형식
description: Aspose.CAD를 사용하여 .NET에서 CAD 도면 크기를 쉽게 조정하는 방법을 알아보세요. 원활한 크기 조정을 위해 단계별 가이드를 따르세요.
type: docs
weight: 10
url: /ko/net/cad-drawing-manipulation/adjust-cad-drawing-size/
---
## 소개

.NET 애플리케이션에서 CAD 도면의 크기를 원활하게 조정하고 싶으십니까? .NET용 Aspose.CAD는 CAD 도면 크기 조정을 쉽게 처리할 수 있는 강력한 솔루션을 제공합니다. 이 튜토리얼에서는 Aspose.CAD를 사용하여 CAD 도면 크기 조정의 복잡성을 이해할 수 있도록 각 단계를 세분화하여 프로세스를 안내합니다.

## 전제 조건

튜토리얼을 시작하기 전에 다음 전제 조건이 충족되었는지 확인하세요.

- .NET 라이브러리용 Aspose.CAD: 다음에서 라이브러리를 다운로드하고 설치합니다.[.NET용 Aspose.CAD 다운로드 페이지](https://releases.aspose.com/cad/net/).
- 샘플 CAD 도면: 문서 디렉토리에 샘플 CAD 도면 파일(예: "sample.dwg")이 있는지 확인하십시오.

## 네임스페이스 가져오기

필요한 네임스페이스를 .NET 애플리케이션으로 가져오는 것부터 시작하세요. 이 단계는 .NET용 Aspose.CAD가 제공하는 기능에 액세스하는 데 중요합니다.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## 1단계: CAD 도면 로드

Aspose.CAD.Image 클래스의 인스턴스에 CAD 도면을 로드하는 것부터 시작하세요. 샘플 도면의 파일 경로가 올바른지 확인하세요.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "sample.dwg";

// Image 인스턴스에 CAD 도면 로드
using (var image = Aspose.CAD.Image.Load(sourceFilePath))
{
    // 여기에 귀하의 코드가 있습니다 ...
}
```

## 2단계: BmpOptions 생성

CAD 도면을 BMP 파일로 저장할 때 옵션을 지정하는 BmpOptions 클래스의 인스턴스를 만듭니다.

```csharp
Aspose.CAD.ImageOptions.BmpOptions bmpOptions = new Aspose.CAD.ImageOptions.BmpOptions();
```

## 3단계: CadRasterizationOptions 설정

CadRasterizationOptions 클래스를 인스턴스화하고 벡터 래스터화에 대한 해당 속성을 구성합니다.

```csharp
Aspose.CAD.ImageOptions.CadRasterizationOptions cadRasterizationOptions = new Aspose.CAD.ImageOptions.CadRasterizationOptions();
bmpOptions.VectorRasterizationOptions = cadRasterizationOptions;
```

## 4단계: UnitType 속성 설정

CadRasterizationOptions의 UnitType 속성을 설정하여 크기 조정을 위한 단위 유형을 지정합니다. 이 예에서는 센티미터로 설정되어 있습니다.

```csharp
cadRasterizationOptions.UnitType = Aspose.CAD.ImageOptions.UnitType.Centimeter;
```

## 5단계: 레이아웃 속성 설정

Layouts 속성을 설정하여 크기가 조정된 도면에 포함할 레이아웃을 지정합니다.

```csharp
cadRasterizationOptions.Layouts = new string[] { "Model" };
```

## 6단계: BMP로 내보내기

마지막으로 Save 메서드를 사용하여 크기가 조정된 레이아웃을 BMP 파일로 저장합니다.

```csharp
string outPath = sourceFilePath + ".bmp";
image.Save(outPath, bmpOptions);
```

이제 .NET용 Aspose.CAD를 사용하여 CAD 도면의 크기를 성공적으로 조정했습니다!

## 결론

이 튜토리얼에서는 Aspose.CAD를 사용하여 .NET에서 CAD 도면의 크기를 조정하는 과정을 살펴보았습니다. 다음 단계를 따르면 이 기능을 애플리케이션에 원활하게 통합하여 원활한 사용자 경험을 제공할 수 있습니다.

## 자주 묻는 질문

### Q1: Aspose.CAD for .NET은 모든 CAD 형식과 호환됩니까?

 A1: .NET용 Aspose.CAD는 DWG, DXF, DWF 등을 포함한 광범위한 CAD 형식을 지원합니다. 을 체크 해봐[선적 서류 비치](https://reference.aspose.com/cad/net/) 전체 목록을 보려면.

### Q2: 여러 레이아웃의 크기를 동시에 조정할 수 있나요?

A2: 예, CadRasterizationOptions에서 레이아웃 배열을 조정하여 여러 레이아웃의 크기를 조정할 수 있습니다.

### Q3: .NET용 Aspose.CAD에 대한 지원은 어디서 받을 수 있나요?

 A3: 다음을 방문하세요.[Aspose.CAD 포럼](https://forum.aspose.com/c/cad/19) 지역 사회 지원 및 지원을 위해.

### Q4: 무료 평가판이 제공됩니까?

 A4: 예, 다음을 탐색할 수 있습니다.[무료 시험판](https://releases.aspose.com/) .NET용 Aspose.CAD의 기능을 평가합니다.

### Q5: Aspose.CAD for .NET의 임시 라이선스를 어떻게 얻을 수 있나요?

 A5: 테스트 목적으로 임시 라이선스를 얻습니다.[여기](https://purchase.aspose.com/temporary-license/).