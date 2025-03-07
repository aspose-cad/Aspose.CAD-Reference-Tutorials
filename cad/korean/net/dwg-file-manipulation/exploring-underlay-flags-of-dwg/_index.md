---
title: DWG 파일의 언더레이 플래그 탐색 - Aspose.CAD Tutorial
linktitle: DWG 파일의 언더레이 플래그 탐색
second_title: Aspose.CAD .NET - CAD 및 BIM 파일 형식
description: DWG 파일 언더레이 플래그를 탐색하면서 .NET용 Aspose.CAD의 강력한 기능을 활용해 보세요. 단계별 가이드를 따르세요.
weight: 13
url: /ko/net/dwg-file-manipulation/exploring-underlay-flags-of-dwg/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DWG 파일의 언더레이 플래그 탐색 - Aspose.CAD Tutorial

## 소개

CAD 파일, 특히 DWG 파일의 복잡한 세계를 탐구하고 언더레이 플래그의 신비를 풀고 싶다면 바로 이곳에 오셨습니다. 이 튜토리얼은 강력한 .NET용 Aspose.CAD 라이브러리를 사용하여 DWG 파일의 언더레이 플래그를 탐색하는 과정을 안내합니다.

## 전제 조건

튜토리얼을 시작하기 전에 다음 사항이 있는지 확인하세요.

- C# 및 .NET 프로그래밍에 대한 기본적인 이해.
-  .NET 라이브러리용 Aspose.CAD가 설치되었습니다. 그렇지 않은 경우 다운로드할 수 있습니다.[여기](https://releases.aspose.com/cad/net/).
- 테스트용 DWG 파일입니다. 튜토리얼에서 제공되는 샘플 파일 "BlockRefDgn.dwg"를 사용할 수 있습니다.

## 네임스페이스 가져오기

시작하려면 필요한 네임스페이스를 가져와야 합니다. 다음은 도움이 되는 내용입니다.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;

```

## 1단계: DWG 파일 로드 및 CadImage로 변환

기존 DWG 파일을 로드하고 이를 CadImage로 변환하여 시작합니다.

```csharp
string fileName = MyDir + "BlockRefDgn.dwg";

// DWG 파일을 로드하고 CadImage로 변환
using (CadImage image = (CadImage)Image.Load(fileName))
{
    // 후속 단계에 대한 코드가 여기에 표시됩니다.
}
```

## 2단계: 엔터티 반복

다음으로 DWG 파일 내의 각 도면요소를 반복합니다.

```csharp
foreach (CadBaseEntity entity in image.Entities)
{
    // 후속 단계에 대한 코드가 여기에 표시됩니다.
}
```

## 3단계: CadDgnUnderlay 유형 확인

엔터티가 CadDgnUnderlay 유형인지 확인합니다.

```csharp
if (entity is CadDgnUnderlay)
{
    // 후속 단계에 대한 코드가 여기에 표시됩니다.
}
```

## 4단계: 언더레이 플래그에 액세스

다양한 언더레이 플래그에 액세스하고 관련 정보를 추출합니다.

```csharp
CadUnderlay underlay = entity as CadUnderlay;

Console.WriteLine(underlay.UnderlayPath);
Console.WriteLine(underlay.UnderlayName);
Console.WriteLine(underlay.InsertionPoint.X);
Console.WriteLine(underlay.InsertionPoint.Y);
Console.WriteLine(underlay.RotationAngle);
Console.WriteLine(underlay.ScaleX);
Console.WriteLine(underlay.ScaleY);
Console.WriteLine(underlay.ScaleZ);
Console.WriteLine((underlay.Flags & UnderlayFlags.UnderlayIsOn) == UnderlayFlags.UnderlayIsOn);
Console.WriteLine((underlay.Flags & UnderlayFlags.ClippingIsOn) == UnderlayFlags.ClippingIsOn);
Console.WriteLine((underlay.Flags & UnderlayFlags.Monochrome) != UnderlayFlags.Monochrome);
```

## 결론

축하해요! .NET용 Aspose.CAD를 사용하여 DWG 파일의 언더레이 플래그를 성공적으로 탐색했습니다. 이 튜토리얼에서는 엔터티를 탐색하고 언더레이에 대한 중요한 정보를 추출하는 데 필요한 지식을 제공합니다.

## FAQ

### Q1: Aspose.CAD for .NET을 다른 CAD 파일 형식과 함께 사용할 수 있습니까?

A1: Aspose.CAD는 DWG, DXF, DGN 등을 포함한 다양한 CAD 형식을 지원합니다. 전체 목록은 설명서를 확인하세요.

### Q2: Aspose.CAD for .NET에 임시 라이선스를 사용할 수 있나요?

 A2: 예, 임시 라이센스를 얻을 수 있습니다.[여기](https://purchase.aspose.com/temporary-license/).

### Q3: .NET용 Aspose.CAD에 대한 지원은 어디서 찾을 수 있습니까?

 A3: 지원 포럼을 방문하세요.[여기](https://forum.aspose.com/c/cad/19) 도움을 위해.

### Q4: .NET용 Aspose.CAD를 어떻게 구매하나요?

A4: 도서관 구입[여기](https://purchase.aspose.com/buy).

### Q5: 무료 평가판이 제공됩니까?

 A5: 예, 무료 평가판에 액세스할 수 있습니다.[여기](https://releases.aspose.com/).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
