---
date: 2026-03-21
description: Aspose.CAD를 사용하여 .NET에서 CAD 레이아웃 크기를 가져오는 방법을 배우세요. 효율적인 CAD 파일 조작을 위한
  단계별 가이드를 따라보세요.
linktitle: Get Size of CAD Layout
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Aspose.CAD for .NET에서 CAD 레이아웃 크기 가져오기
url: /ko/net/cad-drawing-manipulation/get-size-of-cad-layout/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD for .NET에서 CAD 레이아웃 크기 가져오기

## 소개

이 포괄적인 튜토리얼에서는 Aspose.CAD 라이브러리를 사용하여 **CAD 레이아웃 크기를 가져오는 방법**을 알아봅니다. CAD 뷰어를 구축하거나 썸네일을 생성하거나, 다운스트림 처리에 필요한 정확한 레이아웃 치수가 필요할 때, 각 레이아웃의 정확한 크기를 아는 것이 필수적입니다. 도면을 로드하고 레이아웃 치수를 추출한 다음 필요에 따라 이미지를 저장하는 전체 워크플로우를 단계별로 안내하므로, 자신만의 애플리케이션에 이 기능을 자신 있게 통합할 수 있습니다.

## 빠른 답변
- **‘CAD 레이아웃 크기 가져오기’는 무엇을 의미합니까?** CAD 파일에서 비어 있지 않은 각 레이아웃의 너비와 높이(도면 단위)를 가져오는 것을 의미합니다.  
- **어떤 라이브러리가 이를 지원합니까?** Aspose.CAD for .NET은 레이아웃 정보를 액세스할 수 있는 간단한 API를 제공합니다.  
- **라이선스가 필요합니까?** 평가용 무료 체험판을 사용할 수 있으며, 프로덕션 사용 시 상용 라이선스가 필요합니다.  
- **지원되는 형식은?** DWG, DXF 및 기타 많은 CAD/BIM 형식을 완벽히 지원합니다.  
- **구현 소요 시간은?** 기본 크기 조회 루틴을 만드는 데 약 10‑15분 정도 소요됩니다.

## ‘CAD 레이아웃 크기 가져오기’란 무엇인가요?
CAD 레이아웃 크기를 가져온다는 것은 CAD 도면에 정의된 각 레이아웃(종이 공간)의 기하학적 범위를 추출하는 것을 의미합니다. 이 범위는 도면의 기본 단위(보통 밀리미터 또는 인치)로 표현되며, 스케일링, 인쇄 또는 미리보기 이미지 생성과 같은 작업에 유용합니다.

## 왜 Aspose.CAD로 CAD 레이아웃 크기를 가져와야 할까요?
- **CAD 소프트웨어가 필요 없음** – 서버 측에서 완전히 동작합니다.  
- **크로스‑플랫폼** – .NET Framework, .NET Core, .NET 5/6+에서 모두 작동합니다.  
- **정확한 측정** – 파일에 저장된 정확한 범위를 반환하므로 수동 파싱을 피할 수 있습니다.  
- **쉬운 통합** – 간단한 API 호출로 기존 C# 프로젝트에 자연스럽게 녹아듭니다.

## 전제 조건

코드를 진행하기 전에 다음이 설치되어 있는지 확인하세요:

- Aspose.CAD for .NET이 설치되어 있어야 합니다. [Aspose.CAD for .NET 다운로드 페이지](https://releases.aspose.com/cad/net/)에서 다운로드할 수 있습니다.  
- 분석하려는 하나 이상의 CAD 파일(DWG, DXF 등). 이 가이드에서는 `conic_pyramid.dxf`와 `Bottom_plate.dwg` 샘플 파일을 사용합니다.

## 네임스페이스 가져오기

프로젝트에서 필요한 네임스페이스를 가져옵니다:

```csharp
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadConsts;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.FileFormats.Cad.CadTables;
using Aspose.CAD.ImageOptions;
```

## 1단계: 문서 디렉터리 설정

CAD 파일이 들어 있는 폴더를 정의합니다. 자리표시자를 실제 경로로 교체하세요.

```csharp
string MyDir = "Your Document Directory";
```

## 2단계: CAD 파일 경로 지정

처리하려는 각 CAD 파일을 가리키는 배열을 만듭니다.

```csharp
string[] sourceFilePaths = new[]
{
    MyDir + "conic_pyramid.dxf",
    MyDir + "Bottom_plate.dwg"
};
```

## 3단계: CAD 파일 순회

각 파일을 로드하고 형식을 감지한 뒤 레이아웃 정보를 추출할 준비를 합니다.

```csharp
foreach (var sourceFilePath in sourceFilePaths)
{
    string extension = Path.GetExtension(sourceFilePath);
    using (CadImage cadImage = (CadImage)Aspose.CAD.Image.Load(sourceFilePath))
    {
        // ... (continue to the next step)
    }
}
```

## 4단계: 비어 있지 않은 레이아웃 가져오기

실제로 도면 엔티티를 포함하고 있는 레이아웃만 반환하는 도우미 메서드가 필요합니다. 비어 있는 레이아웃은 크기를 보고할 것이 없으므로 무시합니다.

```csharp
private static List<string> GetNotEmptyLayouts(Image cadImage, string extension)
{
    // ... (continue to the next step)
}
```

## 5단계: DWG 파일용 레이아웃 가져오기

DWG 파일은 `HeaderVariables` 테이블에 레이아웃 정보를 저장합니다. 다음 메서드는 DWG 도면에서 비어 있지 않은 모든 레이아웃 이름을 추출합니다.

```csharp
private static List<string> GetNotEmptyLayoutsForDwg(CadImage cadImage)
{
    // ... (continue to the next step)
}
```

## 6단계: DXF 파일용 레이아웃 가져오기

DXF 파일은 구조가 다릅니다. 이 메서드는 `Tables` 컬렉션을 파싱하여 엔티티를 포함하는 종이 공간 레이아웃을 찾습니다.

```csharp
private static List<string> GetNotEmptyLayoutsForDxf(CadImage cadImage)
{
    // ... (continue to the next step)
}
```

## 7단계: 레이아웃 크기 가져오기 및 이미지로 저장

마지막으로 발견된 각 레이아웃을 순회하면서 범위를 읽고, 필요에 따라 레이아웃을 이미지 파일로 렌더링하여 시각적으로 확인할 수 있습니다.

```csharp
foreach (string layout in layouts)
{
    // ... (continue to the next step)
}
```

## 일반적인 문제 및 팁

- **레이아웃 이름 누락:** CAD 파일에 실제로 종이 공간 레이아웃이 포함되어 있는지 확인하세요. 일부 파일은 모델 공간만 가지고 있습니다.  
- **단위 오류:** 크기는 도면의 기본 단위로 반환됩니다. 필요에 따라 밀리미터 또는 인치로 변환하세요.  
- **성능:** 매우 큰 DWG/DXF 파일을 로드하면 메모리를 많이 사용할 수 있으므로 비동기 처리나 배치 처리를 고려하세요.

## 자주 묻는 질문

**Q: Aspose.CAD가 모든 CAD 파일 형식을 지원하나요?**  
A: 네, Aspose.CAD는 DWG, DXF, DGN을 포함한 다양한 형식과 많은 BIM 파일 유형을 지원합니다.

**Q: 이미지 저장 옵션을 커스터마이즈할 수 있나요?**  
A: 물론입니다! `CadRasterizationOptions`(포맷, 해상도, 배경색 등)를 조정하여 필요에 맞게 설정할 수 있습니다.

**Q: 추가 문서는 어디에서 찾을 수 있나요?**  
A: 자세한 API 레퍼런스와 더 많은 예제는 [Aspose.CAD 문서](https://reference.aspose.com/cad/net/)를 참고하세요.

**Q: 무료 체험판을 이용할 수 있나요?**  
A: 네, [무료 체험판](https://releases.aspose.com/)으로 Aspose.CAD를 살펴볼 수 있습니다.

**Q: 기술 지원은 어떻게 받나요?**  
A: 기술 지원이 필요하면 [Aspose.CAD 포럼](https://forum.aspose.com/c/cad/19)을 방문하세요.

---

**마지막 업데이트:** 2026-03-21  
**테스트 환경:** Aspose.CAD 24.11 for .NET  
**작성자:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}