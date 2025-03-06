---
title: .NET용 Aspose.CAD에서 지원되는 DGN 요소
linktitle: 지원되는 DGN 요소
second_title: Aspose.CAD .NET - CAD 및 BIM 파일 형식
description: DGN 파일 처리를 위한 .NET용 Aspose.CAD의 강력한 기능을 살펴보세요. 2D 및 3D 요소를 원활하게 사용하려면 단계별 가이드를 따르세요.
weight: 18
url: /ko/net/cad-features-and-support/supported-dgn-elements/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# .NET용 Aspose.CAD에서 지원되는 DGN 요소

## 소개

DGN 파일을 원활하게 사용하고 싶은 .NET 개발자이신가요? .NET용 Aspose.CAD는 DGN 파일을 효율적으로 처리할 수 있는 강력한 솔루션을 제공합니다. 이 튜토리얼에서는 지원되는 DGN 요소를 자세히 살펴보고 .NET용 Aspose.CAD로 작업하는 과정을 안내합니다.

## 전제 조건

시작하기 전에 다음 사항이 있는지 확인하세요.

- .NET 프로그래밍에 대한 기본 지식.
- 컴퓨터에 Visual Studio가 설치되어 있습니다.
-  다운로드할 수 있는 .NET 라이브러리용 Aspose.CAD[여기](https://releases.aspose.com/cad/net/).

## 네임스페이스 가져오기

프로젝트를 시작하려면 필요한 네임스페이스를 .NET 애플리케이션으로 가져옵니다. 이 단계에서는 Aspose.CAD for .NET에서 제공하는 기능에 액세스할 수 있는지 확인합니다.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Dgn;
using Aspose.CAD.FileFormats.Dgn.DgnElements;
```

## 1단계: DGN 파일 로드

.NET 애플리케이션에서 기존 DGN 파일을 CadImage로 로드하는 것부터 시작하세요.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (DgnImage dgnImage = (DgnImage)Image.Load(sourceFilePath))
{
    // 여기에 귀하의 코드가 있습니다
}
```

## 2단계: DGN 요소 반복

foreach 루프를 사용하여 DGN 요소를 반복합니다. .NET용 Aspose.CAD는 작업할 수 있는 다양한 DGN 요소 유형을 제공합니다.

```csharp
foreach (DgnDrawingElementBase element in dgnImage.Elements)
{
    // 여기에 귀하의 코드가 있습니다
}
```

## 3단계: 이전에 지원된 엔터티 처리

이전에 지원되었던 2D 엔터티를 이제 3D에서도 지원됩니다.

```csharp
switch (element.Metadata.Type)
{
    case DgnElementType.Line:
    case DgnElementType.Ellipse:
    case DgnElementType.Curve:
    // 추가 사례
        {
            // 여기에 귀하의 코드가 있습니다
            break;
        }
}
```

## 4단계: 지원되는 3D 엔터티 처리

.NET용 Aspose.CAD에서 제공하는 지원되는 3D 엔터티를 처리합니다.

```csharp
switch (element.Metadata.Type)
{
    case DgnElementType.SolidHeader3D:
    case DgnElementType.Cone:
    case DgnElementType.CellHeader:
        {
            // 여기에 귀하의 코드가 있습니다
            break;
        }
}
```

## 5단계: 내보내기 및 저장

마지막으로 수정된 DGN 파일을 래스터 이미지로 내보내고 지정된 디렉토리에 저장합니다.

```csharp
Console.WriteLine("\nThe DGN file exported successfully to raster image.\nFile saved at " + MyDir);
```

## 결론

이 튜토리얼에서는 DGN 파일을 처리하고 조작하는 데 있어 .NET용 Aspose.CAD의 기능을 살펴보았습니다. 단계별 가이드를 따르면 지원되는 DGN 요소가 2D인지 3D 요소인지에 관계없이 효율적으로 작업할 수 있습니다. .NET용 Aspose.CAD를 사용하면 DGN 파일 처리를 .NET 응용 프로그램에 원활하게 통합할 수 있습니다.

## FAQ

### Q1: .NET용 Aspose.CAD 설명서는 어디서 찾을 수 있나요?

 A1: 문서를 찾을 수 있습니다.[여기](https://reference.aspose.com/cad/net/).

### Q2: .NET용 Aspose.CAD를 어떻게 다운로드하나요?

 A2: 라이브러리를 다운로드할 수 있습니다.[여기](https://releases.aspose.com/cad/net/).

### Q3: Aspose.CAD for .NET에 대한 무료 평가판이 있습니까?

 A3: 예, 무료 평가판에 액세스할 수 있습니다.[여기](https://releases.aspose.com/).

### Q4: Aspose.CAD for .NET의 임시 라이선스는 어디서 구할 수 있나요?

 A4: 임시 라이센스를 사용할 수 있습니다.[여기](https://purchase.aspose.com/temporary-license/).

### Q5: 도움이 필요하거나 질문이 있나요?

 A5: .NET용 Aspose.CAD 커뮤니티를 방문하세요.[지원 포럼](https://forum.aspose.com/c/cad/19).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
