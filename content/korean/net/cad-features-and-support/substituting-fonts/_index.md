---
title: .NET용 Aspose.CAD에서 글꼴 대체
linktitle: 글꼴 대체
second_title: Aspose.CAD .NET - CAD 및 BIM 파일 형식
description: Aspose.CAD에서 .NET용 글꼴을 손쉽게 대체하는 방법을 알아보세요. CAD 도면에서 효율적인 글꼴 사용자 정의를 위한 단계별 가이드를 따르십시오.
type: docs
weight: 17
url: /ko/net/cad-features-and-support/substituting-fonts/
---
## 소개

.NET을 사용한 CAD 개발 영역에서 글꼴을 조작하는 능력은 중요한 기술입니다. .NET용 Aspose.CAD는 이러한 목적을 위한 강력한 도구 세트를 제공하여 개발자가 CAD 도면 내에서 글꼴을 원활하게 대체할 수 있도록 합니다. 이 튜토리얼에서는 프로세스를 단계별로 살펴보고 글꼴 대체를 효율적으로 수행하는 방법을 보여줍니다.

## 전제 조건

튜토리얼을 시작하기 전에 다음 사항을 확인하세요.

- .NET 프로그래밍에 대한 기본 지식.
-  .NET용 Aspose.CAD가 설치되었습니다. 그렇지 않은 경우 다운로드할 수 있습니다.[여기](https://releases.aspose.com/cad/net/).
- 실습을 위한 CAD 도면 파일입니다.

## 네임스페이스 가져오기

시작하기 전에 .NET 애플리케이션에서 Aspose.CAD 기능에 액세스하는 데 필요한 네임스페이스를 가져옵니다.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad.CadTables;
```

## 1단계: CAD 도면 로드

 CAD 도면을 인스턴스로 로드하여 시작합니다.`CadImage`. 문서 디렉터리에 올바른 경로를 제공했는지 확인하세요.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

using (CadImage cadImage = (CadImage)Aspose.CAD.Image.Load(sourceFilePath))
{
    //추가 작업을 위한 코드는 여기에 있습니다.
}
```

## 2단계: 스타일 반복

 다음으로, 다음을 사용하여 CAD 도면의 스타일을 반복합니다.`foreach` 고리. 이를 통해 개별 글꼴 스타일에 액세스하고 조작할 수 있습니다.

```csharp
foreach (CadStyleTableObject style in cadImage.Styles)
{
    // 스타일 조작을 위한 코드는 여기에 있습니다.
}
```

## 3단계: 전역적으로 글꼴 대체

 모든 스타일을 전체적으로 글꼴로 대체하려면`PrimaryFontName` 각 스타일의 속성을 원하는 글꼴 이름(예: "Arial")으로 설정합니다.

```csharp
foreach (CadStyleTableObject style in cadImage.Styles)
{
    style.PrimaryFontName = "Arial";
}
```

## 4단계: 스타일 이름으로 글꼴 대체

특정 스타일을 글꼴로 대체하려면 루프 내에서 스타일 이름을 확인하면 됩니다.

```csharp
foreach (CadStyleTableObject style in cadImage.Styles)
{
    if (style.StyleName == "Roman")
    {
        style.PrimaryFontName = "Arial";
    }
}
```

## 결론

축하해요! .NET용 Aspose.CAD에서 글꼴을 대체하는 방법을 성공적으로 배웠습니다. 이 기술은 원하는 대로 CAD 도면의 모양을 사용자 정의하는 데 유용합니다.

## FAQ

### Q1: Aspose.CAD for .NET에서 글꼴 변경 사항을 되돌릴 수 있나요?

A1: 예, 원본 CAD 도면을 다시 로드하거나 백업을 유지하여 글꼴 변경 사항을 되돌릴 수 있습니다.

### Q2: 수정할 수 있는 다른 글꼴 속성이 있습니까?

A2: 물론이죠. 게다가`PrimaryFontName`, Aspose.CAD for .NET은 고급 사용자 정의를 위해 다양한 글꼴 관련 속성에 대한 액세스를 제공합니다.

### Q3: Aspose.CAD는 다른 CAD 형식과 호환됩니까?

A3: 예, Aspose.CAD는 광범위한 CAD 형식을 지원하여 개발 프로젝트의 유연성을 보장합니다.

### Q4: 일괄 처리에서 글꼴 대체를 자동화할 수 있습니까?

A4: 물론 일괄 처리를 구현하여 여러 CAD 도면에서 글꼴 대체를 자동화할 수 있습니다.

### Q5: .NET용 Aspose.CAD에 대한 추가 지원은 어디서 찾을 수 있나요?

 A5: 추가 지원 및 커뮤니티 토론을 보려면 다음을 방문하세요.[Aspose.CAD 포럼](https://forum.aspose.com/c/cad/19).

