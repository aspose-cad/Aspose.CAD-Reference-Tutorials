---
date: 2026-04-09
description: 이 단계별 가이드에서 Aspose.CAD for .NET을 사용하여 DWG를 이미지로 변환하고 언더레이 플래그를 읽는 방법을
  배워보세요.
keywords:
- convert dwg to image
- how to read underlay
- Aspose.CAD DWG underlay flags
linktitle: DWG 파일의 언더레이 플래그 탐색
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: DWG를 이미지로 변환 – DWG 파일의 언더레이 플래그 탐색 - Aspose.CAD 튜토리얼
url: /ko/net/dwg-file-manipulation/exploring-underlay-flags-of-dwg/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DWG 파일의 언더레이 플래그 탐색 - Aspose.CAD 튜토리얼

## 소개

CAD 파일, 특히 DWG 파일의 복잡한 세계를 탐구하고 있으며 **DWG를 이미지로 변환**하고 **언더레이 플래그를 읽는 방법**을 찾고 있다면, 올바른 곳에 오셨습니다. 이 튜토리얼은 강력한 Aspose.CAD for .NET 라이브러리를 사용하여 모든 단계를 안내하므로 언더레이 정보를 추출하고 자신 있게 이미지를 렌더링할 수 있습니다.

## 빠른 답변
- **“DWG를 이미지로 변환”이 무엇을 의미합니까?**  
  이는 Aspose.CAD를 사용하여 DWG 도면을 래스터 형식(PNG, JPEG 등)으로 렌더링하는 것을 의미합니다.
- **어떤 메서드가 언더레이 플래그를 표시합니까?**  
  `DWG`를 로드한 후 `CadUnderlay` 객체의 `Flags` 속성에 접근합니다.
- **Aspose.CAD에 라이선스가 필요합니까?**  
  평가용 임시 라이선스를 사용할 수 있으며, 프로덕션에서는 정식 라이선스가 필요합니다.
- **지원되는 .NET 버전은 무엇입니까?**  
  .NET Framework 4.6+, .NET Core 3.1+, .NET 5/6 및 이후 버전.
- **언더레이 기하학을 추출할 수 있습니까?**  
  예 – 언더레이 경로, 삽입점, 스케일, 회전 및 플래그 상태 모두에 접근할 수 있습니다.

## “DWG를 이미지로 변환”이란 무엇이며 왜 중요한가요?

DWG 파일을 이미지로 변환하면 CAD 도면을 브라우저에 표시하거나 보고서에 삽입하거나 CAD 뷰어가 없는 이해관계자와 공유할 수 있습니다. 렌더링 중에는 **언더레이** 객체(예: DGN 참조)를 검사하여 올바르게 표시되는지 확인해야 할 때가 많습니다. 언더레이 플래그를 이해하면 최종 이미지를 생성하기 전에 클리핑, 단색 렌더링 및 가시성 문제를 해결하는 데 도움이 됩니다.

## 전제 조건

- C# 및 .NET 프로그래밍에 대한 기본적인 이해.  
- **Aspose.CAD for .NET** 라이브러리가 설치되어 있습니다. 아직 없으시면 **[here](https://releases.aspose.com/cad/net/)**에서 다운로드하십시오.  
- 테스트용 DWG 파일 – 샘플 파일 **“BlockRefDgn.dwg”**가 이 가이드 전반에 걸쳐 사용됩니다.

## 네임스페이스 가져오기

시작하려면 필요한 네임스페이스를 가져오세요:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## 1단계: DWG 파일을 로드하고 `CadImage`로 변환

먼저 DWG 파일을 로드하고 `CadImage`로 캐스팅합니다. 이 객체를 통해 언더레이를 포함한 모든 도면 엔터티에 접근할 수 있습니다.

```csharp
string fileName = MyDir + "BlockRefDgn.dwg";

// Load DWG file and convert to CadImage
using (CadImage image = (CadImage)Image.Load(fileName))
{
    // Your code for subsequent steps will go here
}
```

## 2단계: 엔터티 순회

다음으로 도면의 모든 엔터티를 반복합니다. 여기서 언더레이 객체를 찾게 됩니다.

```csharp
foreach (CadBaseEntity entity in image.Entities)
{
    // Your code for subsequent steps will go here
}
```

## 3단계: `CadDgnUnderlay` 유형 확인

런타임 유형을 확인하여 언더레이 엔터티를 식별합니다. `CadDgnUnderlay` 클래스는 DWG에 포함된 DGN 언더레이를 나타냅니다.

```csharp
if (entity is CadDgnUnderlay)
{
    // Your code for subsequent steps will go here
}
```

## 4단계: 언더레이 플래그 접근

`CadDgnUnderlay`를 확보하면 이를 `CadUnderlay`로 캐스팅하여 속성과 플래그 상태를 읽습니다. 플래그는 언더레이가 보이는지, 클리핑 되었는지, 단색으로 렌더링되는지를 알려줍니다.

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

### 출력 내용

- **UnderlayPath / UnderlayName** – 외부 DGN 파일이 위치한 경로.  
- **InsertionPoint (X, Y)** – 언더레이가 DWG 공간에 배치되는 좌표.  
- **RotationAngle** – 언더레이에 적용된 회전.  
- **ScaleX / ScaleY / ScaleZ** – 각 축에 대한 스케일링 계수.  
- **Flags** – 가시성(`UnderlayIsOn`), 클리핑(`ClippingIsOn`), 단색 렌더링(`Monochrome`)을 나타내는 불리언 값.

## 일반적인 문제 및 해결책

| 문제 | 원인 | 해결책 |
|-------|--------|-----|
| 플래그 확인에 대한 출력 없음 | 언더레이가 꺼져 있을 때 언더레이 플래그가 0으로 기본 설정됩니다. | DWG에 실제 활성 언더레이가 포함되어 있는지 확인하거나 원본 CAD 파일에서 가시성을 전환하십시오. |
| `Invalid cast` 예외 | 엔터티가 `CadDgnUnderlay`가 아닙니다. | 캐스팅하기 전에 `if (entity is CadDgnUnderlay)` 조건을 확인하십시오. |
| 플래그 추출 후 이미지 렌더링 실패 | 언더레이가 클리핑되었거나 꺼져 있어 빈 영역이 발생할 수 있습니다. | 최종 이미지를 렌더링하기 전에 플래그(`UnderlayIsOn = true`, `ClippingIsOn = false`)를 조정하십시오. |

## 자주 묻는 질문

### Q1: Aspose.CAD for .NET를 다른 CAD 파일 형식과 함께 사용할 수 있나요?

A1: Aspose.CAD는 DWG, DXF, DGN 등을 포함한 다양한 CAD 형식을 지원합니다. 전체 목록은 문서를 확인하십시오.

### Q2: Aspose.CAD for .NET에 임시 라이선스가 제공됩니까?

A2: 예, 임시 라이선스를 **[here](https://purchase.aspose.com/temporary-license/)**에서 얻을 수 있습니다.

### Q3: Aspose.CAD for .NET에 대한 지원을 어디서 찾을 수 있나요?

A3: 지원 포럼 **[here](https://forum.aspose.com/c/cad/19)**을 방문하여 도움을 받으세요.

### Q4: Aspose.CAD for .NET를 어떻게 구매합니까?

A4: 라이브러리를 **[here](https://purchase.aspose.com/buy)**에서 구매하십시오.

### Q5: 무료 체험판이 제공됩니까?

A5: 예, 무료 체험판을 **[here](https://releases.aspose.com/)**에서 이용할 수 있습니다.

## 결론

축하합니다! Aspose.CAD for .NET를 사용하여 **DWG를 이미지로 변환**하는 방법과 **언더레이 플래그를 읽는** 방법을 성공적으로 습득했습니다. 이 지식을 통해 다음을 수행할 수 있습니다:

- 웹 또는 보고서 시나리오를 위해 DWG 도면을 래스터 이미지로 렌더링합니다.  
- 언더레이 속성을 검사하고 조작하여 올바른 표시를 보장합니다.  
- 최종 이미지 생성 전에 가시성, 클리핑 및 단색 문제를 디버깅합니다.

레이어 관리, 텍스트 추출, 배치 변환 등 다른 Aspose.CAD 기능을 자유롭게 탐색하여 CAD 자동화 워크플로를 더욱 확장하십시오.

---

**마지막 업데이트:** 2026-04-09  
**테스트 환경:** Aspose.CAD for .NET 24.11  
**작성자:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}