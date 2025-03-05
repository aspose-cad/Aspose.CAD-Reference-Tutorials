---
title: DWG 파일에서 OLE 객체 내보내기 - Aspose.CAD Tutorial
linktitle: DWG 파일에서 OLE 객체 내보내기
second_title: Aspose.CAD .NET - CAD 및 BIM 파일 형식
description: .NET용 Aspose.CAD를 사용하여 DWG 파일에서 OLE 개체를 내보내는 방법에 대한 단계별 가이드를 살펴보세요. CAD 파일 조작 기술을 쉽게 향상시키십시오.
type: docs
weight: 12
url: /ko/net/advanced-export-techniques/exporting-ole-objects-from-dwg/
---
## 소개

DWG 파일에서 OLE 객체를 쉽게 추출하고 싶으십니까? .NET용 Aspose.CAD는 프로세스를 간소화하기 위해 여기에 있습니다. 이 자습서에서는 OLE 개체를 내보내는 과정을 단계별로 안내하여 이 강력한 .NET 라이브러리를 최대한 활용할 수 있도록 합니다. 

## 전제 조건

튜토리얼을 시작하기 전에 다음 전제 조건이 충족되었는지 확인하세요.

-  .NET 라이브러리용 Aspose.CAD: 라이브러리가 설치되어 있는지 확인하세요. 다음에서 다운로드할 수 있습니다.[.NET용 Aspose.CAD 다운로드 페이지](https://releases.aspose.com/cad/net/).

-  문서 디렉토리: DWG 파일이 저장되는 디렉토리를 설정합니다. 바꾸다`"Your Document Directory"` 제공된 코드 조각에서 실제 경로를 사용하세요.

## 네임스페이스 가져오기

.NET 프로젝트에서 Aspose.CAD 기능을 활용하려면 필요한 네임스페이스를 가져와야 합니다. 다음 코드 조각을 사용하세요.

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## 1단계: 문서 디렉터리 설정

```csharp
string MyDir = "Your Document Directory";
```

 바꾸다`"Your Document Directory"` DWG 파일이 있는 경로를 사용합니다.

## 2단계: DWG 파일 지정

```csharp
string[] files = new string[] { "D ZD junior D10m H2m.dwg", "ZD - Senior D6m H2m45.dwg" };
```

배열 내에서 처리할 DWG 파일을 나열합니다.

## 3단계: 내보내기 옵션 구성

```csharp
PngOptions pngOptions = new PngOptions { };
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
pngOptions.VectorRasterizationOptions = rasterizationOptions;
rasterizationOptions.Layouts = new string[] { "Layout1" };
```

요구 사항에 따라 내보내기 옵션을 사용자 정의하세요. 이 예에서는 지정된 레이아웃으로 PNG 내보내기를 구성합니다.

## 4단계: 파일 반복 및 내보내기

```csharp
foreach (string file in files)
{
    using (CadImage cadImage = (CadImage)Image.Load(MyDir + file))
    {
        cadImage.Save(MyDir + file + "_out.png", pngOptions);
    }
}
```

지정된 DWG 파일을 반복하고 각 파일을 로드한 다음 정의된 옵션을 사용하여 내보낸 PNG 파일을 저장합니다.

## 결론

축하해요! .NET용 Aspose.CAD를 사용하여 DWG 파일에서 OLE 개체를 성공적으로 내보냈습니다. 이 강력한 라이브러리는 복잡한 작업을 단순화하여 CAD 파일 조작에 효율성과 유연성을 제공합니다.

## FAQ

### Q1: Aspose.CAD for .NET은 주니어 및 시니어 CAD 파일 모두에 적합합니까?

A1: 예, .NET용 Aspose.CAD는 다목적이며 주니어 및 시니어 변형을 모두 포함하여 광범위한 CAD 파일을 처리할 수 있습니다.

### Q2: 다양한 레이아웃에 대한 내보내기 옵션을 사용자 정의할 수 있습니까?

A2: 물론이죠! 튜토리얼에 표시된 대로 특정 요구 사항에 맞게 레이아웃을 포함한 내보내기 옵션을 맞춤화할 수 있습니다.

### Q3: Aspose.CAD for .NET에 대한 자세한 문서는 어디서 찾을 수 있나요?

 A3: 탐색해 보세요.[.NET 문서용 Aspose.CAD](https://reference.aspose.com/cad/net/) 자세한 정보와 예시를 확인하세요.

### Q4: 무료 평가판이 제공됩니까?

 A4: 예, 무료 평가판을 통해 Aspose.CAD for .NET의 기능을 경험할 수 있습니다. 방문하다[이 링크](https://releases.aspose.com/) 시작하려면.

### Q5: 어떻게 지원을 받거나 커뮤니티에 연결할 수 있나요?

 A5: 지원 및 커뮤니티 참여를 원하시면 다음을 방문하세요.[Aspose.CAD 포럼](https://forum.aspose.com/c/cad/19).