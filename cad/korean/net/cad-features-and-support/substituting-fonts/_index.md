---
date: 2026-03-29
description: Aspose.CAD for .NET에서 글꼴을 빠르게 교체하는 방법을 배워보세요. 이 단계별 가이드는 기본 글꼴 이름을 설정하고
  CAD 도면을 효율적으로 맞춤화하는 방법을 보여줍니다.
linktitle: Substituting Fonts
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Aspose.CAD for .NET에서 글꼴 교체 방법
url: /ko/net/cad-features-and-support/substituting-fonts/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD for .NET에서 글꼴 교체하는 방법

## 소개

.NET을 사용한 CAD 개발 분야에서 **글꼴 교체 방법**을 배우는 것은 도면의 시각적 품질을 크게 향상시킬 수 있는 중요한 기술입니다. Aspose.CAD for .NET은 어떤 스타일이든 **기본 글꼴 이름**을 설정할 수 있는 간단한 API를 제공하여 전역 또는 선택적인 글꼴 교체를 손쉽게 할 수 있습니다. 이 튜토리얼에서는 도면을 로드하는 단계부터 전역 또는 특정 스타일 이름별로 글꼴을 교체하는 전체 과정을 안내합니다.

## 빠른 답변
- **CAD 조작을 위한 주요 클래스는 무엇인가요?** `Aspose.CAD.Image` (또는 파생 클래스 `CadImage`).
- **글꼴을 변경하는 속성은 무엇인가요?** `CadStyleTableObject`의 `PrimaryFontName`.
- **모든 스타일의 글꼴을 한 번에 교체할 수 있나요?** 예, `cadImage.Styles`를 반복하면서 해당 속성을 설정하면 됩니다.
- **프로덕션에 라이선스가 필요합니까?** 비체험용으로는 유효한 Aspose.CAD 라이선스가 필요합니다.
- **지원되는 .NET 버전은?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.

## CAD에서 글꼴 대체란 무엇인가요?

글꼴 대체는 CAD 도면에서 사용된 원래 서체를 대상 시스템에 존재하는 다른 서체로 교체하는 것을 의미합니다. 이는 원본 글꼴이 없을 때, 일관된 기업 스타일이 필요할 때, 혹은 제한된 글꼴만 지원하는 장치에서 인쇄하기 위해 도면을 준비할 때 특히 유용합니다.

## Aspose.CAD로 글꼴을 교체하는 이유

- **외부 종속성 없음** – 라이브러리가 내부적으로 글꼴 매핑을 처리합니다.
- **다양한 포맷 지원** – DXF, DWG, DGN 등.
- **프로그래밍 제어** – 배치 변환이나 CI 파이프라인을 위한 자동화가 가능합니다.
- **도면 기하학 보존** – 텍스트의 시각적 표현만 변경됩니다.

## 전제 조건

- .NET 프로그래밍에 대한 기본 지식.
- Aspose.CAD for .NET이 설치되어 있어야 합니다. 아직 설치하지 않았다면 [여기](https://releases.aspose.com/cad/net/)에서 다운로드하세요.
- 실험용 CAD 도면 파일(DXF, DWG 등).

## 네임스페이스 가져오기

시작하기 전에, .NET 애플리케이션에서 Aspose.CAD 기능에 접근하기 위해 필요한 네임스페이스를 가져오세요.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad.CadTables;
```

## 단계 1: CAD 도면 로드

`CadImage` 인스턴스로 CAD 도면을 로드하는 것으로 시작합니다. 문서 디렉터리의 올바른 경로를 제공했는지 확인하세요.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

using (CadImage cadImage = (CadImage)Aspose.CAD.Image.Load(sourceFilePath))
{
    // Your code for further actions goes here
}
```

## 단계 2: 스타일 반복

다음으로, `foreach` 루프를 사용하여 CAD 도면의 스타일을 반복합니다. 이를 통해 개별 글꼴 스타일에 접근하고 조작할 수 있습니다.

```csharp
foreach (CadStyleTableObject style in cadImage.Styles)
{
    // Your code for style manipulation goes here
}
```

## 글꼴 대체를 위한 기본 글꼴 이름 설정 방법

각 `CadStyleTableObject`의 `PrimaryFontName` 속성은 도면이 렌더링될 때 사용되는 글꼴을 제어합니다. 이 속성을 설정하면 원본 글꼴을 효과적으로 교체하게 됩니다.

### 단계 3: 전역적으로 글꼴 교체

**전체** 스타일의 글꼴을 교체하려면, 각 스타일의 `PrimaryFontName` 속성을 원하는 글꼴 이름(예: `"Arial"`)으로 설정합니다.

```csharp
foreach (CadStyleTableObject style in cadImage.Styles)
{
    style.PrimaryFontName = "Arial";
}
```

### 단계 4: 스타일 이름별 글꼴 교체

특정 스타일(예: `"Roman"`이라는 스타일)의 글꼴만 교체하려면, 루프 내부에 조건 검사를 추가합니다.

```csharp
foreach (CadStyleTableObject style in cadImage.Styles)
{
    if (style.StyleName == "Roman")
    {
        style.PrimaryFontName = "Arial";
    }
}
```

## 일반적인 문제 및 해결 방법

| 문제 | 원인 | 해결 방법 |
|-------|-------|-----|
| 코드를 실행한 후 글꼴이 변경되지 않음 | 도면이 캐시되었거나 읽기 전용 모드로 열림 | `cadImage.Save(...)`와 같이 수정 후 이미지를 저장하거나 파일을 다시 로드하여 확인하세요. |
| 원하는 글꼴이 시스템에 없음 | 코드를 실행하는 머신에 글꼴이 설치되지 않음 | 필요한 TrueType/OpenType 글꼴을 설치하거나 애플리케이션 리소스에 포함하세요. |
| 텍스트가 깨져 보임 | 인코딩이 올바르지 않거나 Unicode 지원이 부족함 | 필요한 문자 집합을 지원하는 글꼴(예: Arial Unicode MS)을 사용하세요. |

## 자주 묻는 질문

**Q: Aspose.CAD for .NET에서 글꼴 변경을 되돌릴 수 있나요?**  
A: 예, 원본 CAD 도면을 다시 로드하거나 수정하기 전에 백업 복사본을 유지하면 되돌릴 수 있습니다.

**Q: 수정할 수 있는 다른 글꼴 속성이 있나요?**  
A: 물론입니다. `PrimaryFontName` 외에도 `SecondaryFontName`, `FontFamily` 및 기타 스타일 관련 속성을 사용하여 고급 맞춤 설정이 가능합니다.

**Q: Aspose.CAD가 다양한 CAD 포맷과 호환되나요?**  
A: 예, Aspose.CAD는 DXF, DWG, DGN, DWF 등 다양한 포맷을 지원하여 프로젝트 전반에 걸친 유연성을 제공합니다.

**Q: 배치 처리에서 글꼴 대체를 자동화할 수 있나요?**  
A: 물론입니다. 로드 및 대체 로직을 CAD 파일이 들어 있는 폴더를 반복하는 루프에 감싸거나 CI/CD 파이프라인에 통합하면 됩니다.

**Q: Aspose.CAD for .NET에 대한 추가 지원은 어디서 찾을 수 있나요?**  
A: 추가 지원 및 커뮤니티 토론을 위해 [Aspose.CAD 포럼](https://forum.aspose.com/c/cad/19)을 방문하세요.

---

**마지막 업데이트:** 2026-03-29  
**테스트 환경:** Aspose.CAD for .NET (latest release)  
**작성자:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}