---
date: 2026-03-29
description: Aspose.CAD for .NET을 사용하여 DGN을 PNG로 변환하는 방법을 배웁니다. 이 가이드는 CAD 파일 형식 지원
  및 지원되는 DGN 요소 전체에 대해서도 다룹니다.
linktitle: Supported DGN Elements
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: .NET용 Aspose.CAD로 DGN을 PNG로 변환
url: /ko/net/cad-features-and-support/supported-dgn-elements/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD for .NET을 사용한 DGN을 PNG로 변환

## 소개

원활하게 **DGN을 PNG로 변환**하려는 .NET 개발자이신가요? Aspose.CAD for .NET은 DGN 파일을 효율적으로 처리할 수 있는 강력한 솔루션을 제공합니다. 이 튜토리얼에서는 지원되는 DGN 요소들을 자세히 살펴보고, Aspose.CAD for .NET을 사용하여 해당 요소들을 PNG 이미지로 내보내는 방법을 단계별로 안내합니다.

## 빠른 답변
- **Aspose.CAD는 무엇을 하나요?** CAD/BIM 파일(DGN 포함)을 읽고, 수정하며, PNG와 같은 래스터 형식으로 변환합니다.  
- **2D 및 3D DGN 요소를 변환할 수 있나요?** 예, 2‑D와 3‑D 엔터티 모두 지원됩니다.  
- **필요한 .NET 버전은?** .NET Framework 4.5 이상, .NET Core 3.1 이상, .NET 5/6 이상.  
- **테스트에 라이선스가 필요합니까?** 무료 체험판을 사용할 수 있으며, 실제 운영에는 라이선스가 필요합니다.  
- **라이브러리는 어디서 구할 수 있나요?** 공식 Aspose 사이트에서 다운로드하세요 (아래 링크).

## “convert DGN to PNG”란?
DGN을 PNG로 변환한다는 것은 벡터 기반 DGN 도면(2‑D 또는 3‑D)을 래스터 이미지 형식(PNG)으로 렌더링하는 것을 의미합니다. 이는 웹에서 CAD 도면을 표시하거나, 보고서에 삽입하거나, CAD 뷰어 없이 썸네일을 생성해야 할 때 유용합니다.

## CAD 파일 형식 지원을 위해 Aspose.CAD for .NET을 사용하는 이유
- **전체 CAD 파일 형식 지원** – DGN, DWG, DXF, DWF 등.  
- **외부 종속성 없음** – 순수 .NET 라이브러리이며, 별도의 CAD 설치가 필요하지 않습니다.  
- **고품질 렌더링** – 선 두께, 색상 및 3‑D 기하학을 그대로 유지합니다.  
- **배치 처리** – 서버 측 애플리케이션에서 다수의 파일을 쉽게 반복 처리할 수 있습니다.

## 전제 조건

시작하기 전에 다음이 필요합니다:

- .NET 프로그래밍에 대한 기본 지식.  
- 컴퓨터에 Visual Studio가 설치되어 있어야 합니다.  
- Aspose.CAD for .NET 라이브러리([here](https://releases.aspose.com/cad/net/)에서 다운로드).

## 네임스페이스 가져오기

프로젝트를 시작하려면 .NET 애플리케이션에 필요한 네임스페이스를 가져오세요. 이렇게 하면 Aspose.CAD for .NET이 제공하는 기능을 사용할 수 있습니다.

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

## DGN을 PNG로 변환하는 방법

아래 단계별 가이드를 따라 DGN 파일을 로드하고, 요소를 순회하며, 2‑D 및 3‑D 엔터티를 처리한 뒤, 최종적으로 PNG 래스터 이미지로 내보내는 과정을 진행합니다.

### 단계 1: DGN 파일 로드

기존 DGN 파일을 .NET 애플리케이션에서 `DgnImage` 객체로 로드합니다.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (DgnImage dgnImage = (DgnImage)Image.Load(sourceFilePath))
{
    // Your code here
}
```

### 단계 2: DGN 요소 반복

`foreach` 루프를 사용해 DGN 요소들을 순회합니다. Aspose.CAD for .NET은 다양한 DGN 요소 유형을 제공합니다.

```csharp
foreach (DgnDrawingElementBase element in dgnImage.Elements)
{
    // Your code here
}
```

### 단계 3: 이전에 지원되던 2‑D 엔터티 처리

이러한 엔터티는 이제 3‑D 렌더링도 지원합니다. `switch` 문을 사용해 요소 유형에 따라 로직을 분기합니다.

```csharp
switch (element.Metadata.Type)
{
    case DgnElementType.Line:
    case DgnElementType.Ellipse:
    case DgnElementType.Curve:
    // Additional cases
        {
            // Your code here
            break;
        }
}
```

### 단계 4: 지원되는 3‑D 엔터티 처리

Aspose.CAD는 여러 3‑D DGN 요소에 대한 전체 지원을 추가했습니다. 필요에 따라 `switch`에 해당 처리를 확장하세요.

```csharp
switch (element.Metadata.Type)
{
    case DgnElementType.SolidHeader3D:
    case DgnElementType.Cone:
    case DgnElementType.CellHeader:
        {
            // Your code here
            break;
        }
}
```

### 단계 5: PNG로 내보내기 및 저장

필요한 조작을 마친 후, DGN 도면을 PNG 래스터 이미지로 내보내고 지정된 디렉터리에 저장합니다.

```csharp
Console.WriteLine("\nThe DGN file exported successfully to raster image.\nFile saved at " + MyDir);
```

> **Pro tip:** `Image.Save`와 `new PngOptions()`를 사용해 해상도, 배경색 및 기타 PNG 전용 설정을 제어할 수 있습니다.

## CAD 파일 형식 지원 개요

Aspose.CAD for .NET은 DGN에 국한되지 않고 DWG, DXF, DWF 등 다양한 CAD 형식을 지원합니다. 이를 통해 하나의 API로 광범위한 엔지니어링 도면을 처리할 수 있어, 여러 표준을 지원해야 하는 프로젝트에 이상적입니다.

## 일반적인 문제 및 해결책

| 문제 | 원인 | 해결책 |
|-------|--------|-----|
| **이미지가 비어 있음** | DPI가 0으로 내보냄 | `PngOptions`에 `ResolutionX`와 `ResolutionY`를 지정하세요. |
| **3‑D 기하학 누락** | 스위치에서 요소 유형이 처리되지 않음 | 누락된 `DgnElementType` 케이스를 추가하고 적절히 렌더링하세요. |
| **대용량 파일에서 메모리 부족** | 파일을 한 번에 전체 로드 | 요소를 배치로 처리하거나 가능한 경우 스트리밍을 사용하세요. |

## 자주 묻는 질문

### Q1: Aspose.CAD for .NET 문서는 어디서 찾을 수 있나요?
A1: 문서는 [here](https://reference.aspose.com/cad/net/)에서 확인할 수 있습니다.

### Q2: Aspose.CAD for .NET을 어떻게 다운로드하나요?
A2: 라이브러리는 [here](https://releases.aspose.com/cad/net/)에서 다운로드할 수 있습니다.

### Q3: Aspose.CAD for .NET의 무료 체험판이 있나요?
A3: 예, 무료 체험판은 [here](https://releases.aspose.com/)에서 이용할 수 있습니다.

### Q4: Aspose.CAD for .NET 임시 라이선스는 어디서 받을 수 있나요?
A4: 임시 라이선스는 [here](https://purchase.aspose.com/temporary-license/)에서 제공됩니다.

### Q5: 도움이나 질문이 있나요?
A5: Aspose.CAD for .NET 커뮤니티 [support forum](https://forum.aspose.com/c/cad/19)를 방문하세요.

---

**마지막 업데이트:** 2026-03-29  
**테스트 환경:** Aspose.CAD for .NET 24.11  
**작성자:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}