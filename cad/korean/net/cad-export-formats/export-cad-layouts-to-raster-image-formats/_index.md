---
title: .NET용 Aspose.CAD에서 CAD 레이아웃을 래스터 이미지 형식으로 내보내기
linktitle: CAD 레이아웃을 래스터 이미지 형식으로 내보내기
second_title: Aspose.CAD .NET - CAD 및 BIM 파일 형식
description: .NET용 Aspose.CAD를 사용하여 CAD 레이아웃을 래스터 이미지로 내보내는 방법을 알아보세요. 원활한 변환을 위해 단계별 가이드를 따르세요.
type: docs
weight: 10
url: /ko/net/cad-export-formats/export-cad-layouts-to-raster-image-formats/
---
## 소개

Aspose.CAD for .NET을 사용하여 CAD 레이아웃을 래스터 이미지 형식으로 효율적으로 변환하고 싶으십니까? 이 단계별 가이드는 작업을 원활하게 수행할 수 있도록 자세한 지침과 코드 조각을 제공하여 프로세스를 안내합니다. 숙련된 개발자이든 Aspose.CAD를 처음 접하는 사람이든 이 튜토리얼은 모든 수준의 전문 지식을 충족시킵니다.

## 전제 조건

튜토리얼을 시작하기 전에 다음 사항을 확인하세요.

- .NET 라이브러리용 Aspose.CAD: Aspose.CAD 라이브러리가 설치되어 있는지 확인하세요. 그렇지 않은 경우 다음에서 다운로드할 수 있습니다.[Aspose.CAD 웹사이트](https://releases.aspose.com/cad/net/).

- CAD 도면 파일: 래스터 이미지 형식으로 변환할 CAD 도면 파일(예: conic_pyramid.dxf)을 준비합니다.

## 네임스페이스 가져오기

.NET 프로젝트에서 Aspose.CAD 기능을 활용하는 데 필요한 네임스페이스를 가져옵니다. 코드 시작 부분에 다음 네임스페이스를 포함합니다.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## 1단계: CAD 도면 로드

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

// Image 인스턴스에 CAD 도면 로드
using (var image = Image.Load(sourceFilePath))
{
    // CAD 도면을 로드하기 위한 코드는 여기에 있습니다.
}
```

## 2단계: CadRasterizationOptions 생성

```csharp
// CadRasterizationOptions 인스턴스 생성
var rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 500;
rasterizationOptions.PageHeight = 500;
```

## 3단계: 레이어 지정

```csharp
// CadRasterizationOptions의 레이어 목록에 레이어 이름을 추가합니다.
rasterizationOptions.Layers = new string[] { "LayerA" };
```

## 4단계: JpegOptions 생성

```csharp
// JpegOptions(또는 래스터 형식의 경우 ImageOptions) 인스턴스를 생성합니다.
var options = new JpegOptions();
options.VectorRasterizationOptions = rasterizationOptions;
```

## 5단계: JPEG 형식으로 내보내기

```csharp
// 각 레이어를 Jpeg 형식으로 내보내기
MyDir = MyDir + "CADLayersToRasterImageFormats_out.jpg";
image.Save(MyDir, options);
```

## 추가 단계: 모든 레이어 변환

모든 레이어를 변환하려면 다음 방법을 사용하십시오.

```csharp
ConvertAllLayersToRasterImageFormats();
```

이 방법은 CAD 도면의 모든 레이어를 반복하여 각 레이어를 별도의 Jpeg 파일로 내보냅니다.

## 결론

축하해요! Aspose.CAD for .NET을 사용하여 CAD 레이아웃을 래스터 이미지 형식으로 내보내는 방법을 성공적으로 배웠습니다. 이 튜토리얼은 CAD 변환을 위한 효율적이고 안정적인 솔루션을 찾는 개발자에게 포괄적인 가이드를 제공합니다.

## FAQ

### Q1: 내보낼 때 다른 이미지 형식을 사용할 수 있나요?

 A1: 네, 가능합니다. 간단하게 교체하세요`JpegOptions` 다음과 같은 원하는 형식의 옵션을 사용하여`PngOptions` 또는`BmpOptions`.

### Q2: 평가판을 사용할 수 있나요?

 A2: 예, 평가판을 다운로드하여 Aspose.CAD의 기능을 탐색할 수 있습니다.[여기](https://releases.aspose.com/).

### Q3: Aspose.CAD에 대한 지원은 어떻게 받을 수 있나요?

 A3: Aspose.CAD를 방문하세요.[법정](https://forum.aspose.com/c/cad/19) 커뮤니티 지원을 원하거나 전용 지원을 위한 라이선스 구매를 고려해보세요.

### Q4: 임시 라이센스를 사용할 수 있습니까?

 A4: 예, 임시 라이센스를 얻을 수 있습니다.[여기](https://purchase.aspose.com/temporary-license/).

### Q5: 문서는 어디서 찾을 수 있나요?

 A5: 자세한 문서를 참조하세요.[여기](https://reference.aspose.com/cad/net/).