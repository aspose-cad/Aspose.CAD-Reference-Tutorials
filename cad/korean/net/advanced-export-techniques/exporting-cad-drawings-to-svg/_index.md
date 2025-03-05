---
title: CAD 도면을 SVG 형식으로 내보내기 - Aspose.CAD 가이드
linktitle: CAD 도면을 SVG 형식으로 내보내기
second_title: Aspose.CAD .NET - CAD 및 BIM 파일 형식
description: .NET용 Aspose.CAD를 사용하여 CAD 도면을 SVG로 내보내는 원활한 프로세스를 살펴보세요. 유연성과 사용자 정의를 통해 CAD 개발을 강화하세요.
type: docs
weight: 15
url: /ko/net/advanced-export-techniques/exporting-cad-drawings-to-svg/
---
## 소개

역동적인 CAD(컴퓨터 지원 설계) 세계에서 도면을 다양한 형식으로 내보내는 능력은 중요한 기술입니다. SVG(Scalable Vector Graphics)는 확장성과 다양성으로 인해 인기를 얻은 형식 중 하나입니다. 이 튜토리얼에서는 강력한 .NET용 Aspose.CAD 라이브러리를 사용하여 CAD 도면을 SVG로 내보내는 방법을 살펴보겠습니다.

## 전제 조건

튜토리얼을 시작하기 전에 다음 전제 조건이 충족되었는지 확인하세요.

-  .NET 라이브러리용 Aspose.CAD: .NET 라이브러리용 Aspose.CAD를 다운로드하고 설치합니다. 도서관을 찾으실 수 있습니다[여기](https://releases.aspose.com/cad/net/).

- 개발 환경: Visual Studio 또는 기타 .NET 개발 도구를 사용하여 적합한 개발 환경을 설정합니다.

## 네임스페이스 가져오기

시작하려면 필요한 네임스페이스를 프로젝트로 가져옵니다.

```csharp
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## 1단계: 문서 디렉터리 설정

```csharp
// 문서 디렉터리의 경로입니다.
string MyDir = "Your Document Directory";
```

## 2단계: CAD 도면 로드

```csharp
using (Image image = Image.Load(MyDir + "sample.dwg"))
{
```

## 3단계: SVG 내보내기 옵션 구성

```csharp
    var options = new SvgOptions();
    options.ColorType = SvgColorMode.Grayscale;
    options.TextAsShapes = true;
```

## 4단계: SVG 파일 저장

```csharp
    image.Save(MyDir + "sample.svg", options);
}
```

이러한 간단한 단계를 따르면 Aspose.CAD for .NET을 사용하여 CAD 도면을 SVG로 원활하게 내보낼 수 있습니다. 라이브러리는 유연성과 사용자 정의 옵션을 제공하므로 요구 사항에 따라 출력을 조정할 수 있습니다.

## 결론

결론적으로 Aspose.CAD for .NET은 CAD 도면을 SVG로 내보내는 과정을 단순화합니다. 직관적인 API와 강력한 기능을 통해 CAD 응용 프로그램을 사용하는 개발자에게 유용한 도구입니다.

## FAQ

### Q1: Aspose.CAD는 모든 CAD 형식과 호환됩니까?

A1: Aspose.CAD는 DWG 및 DXF를 포함한 다양한 CAD 형식을 지원하여 광범위한 호환성을 보장합니다.

### Q2: SVG로 내보낼 때 색상 모드를 사용자 정의할 수 있습니까?

A2: 예, Aspose.CAD를 사용하면 색상 모드를 선택하여 출력에 유연성을 제공할 수 있습니다.

### Q3: 테스트 목적으로 임시 라이센스를 사용할 수 있습니까?

 A3: 예, 임시 라이센스를 얻을 수 있습니다.[여기](https://purchase.aspose.com/temporary-license/) 평가를 위해.

### Q4: Aspose.CAD에 대한 자세한 문서는 어디서 찾을 수 있나요?

 A4: 문서를 사용할 수 있습니다.[여기](https://reference.aspose.com/cad/net/).

### Q5: Aspose.CAD와 관련된 지원을 받거나 질문을 하려면 어떻게 해야 합니까?

 A5: 커뮤니티 포럼을 방문하세요.[여기](https://forum.aspose.com/c/cad/19) 지원과 토론을 위해.