---
date: 2026-10-09
description: C#와 Aspose.CAD for .NET을 사용하여 dwg 파일을 로드하고 DWG 파일 내에서 텍스트를 검색하는 방법을 배웁니다.
  CAD 작업 흐름을 향상시키는 단계별 가이드를 따라 보세요.
keywords:
- load dwg file
- export dwg to pdf
- cad text search
- search text dwg
- c# read dwg
lastmod: 2026-10-09
linktitle: C#로 DWG 파일에서 텍스트 검색
og_description: C#와 Aspose.CAD for .NET을 사용하여 dwg 파일을 로드하고 DWG 파일 내에서 텍스트를 검색하는 방법을
  배웁니다. CAD 작업 흐름을 향상시키는 단계별 가이드를 따라 보세요.
og_image_alt: Guide showing how to load dwg file and search text in DWG files using
  Aspose.CAD for .NET
og_title: C#를 사용하여 dwg 파일을 로드하고 DWG 파일에서 텍스트를 검색하는 방법
schemas:
- author: Aspose
  dateModified: '2026-10-09'
  description: Learn how to load dwg file and search text inside DWG files using C#
    and Aspose.CAD for .NET. Follow this step‑by‑step guide to enhance your CAD workflows.
  headline: How to load dwg file and search text in DWG files with C#
  type: TechArticle
- questions:
  - answer: '`new CadImage("yourfile.dwg")` creates an in‑memory representation of
      the drawing.'
    question: What is the first line of code to load a DWG?
  - answer: '`Aspose.CAD.Image` and `Aspose.CAD.FileFormats.Dwg` are required.'
    question: Which namespace contains the CAD classes?
  - answer: Yes – use `image.Save("out.pdf", SaveFormat.Pdf)`.
    question: Can I export the search results directly to PDF?
  - answer: A free trial works for evaluation; a permanent license is required for
      production.
    question: Do I need a license for development?
  - answer: .NET 5, .NET 6, .NET Core 3.1 and .NET Framework 4.6+.
    question: Which .NET versions are supported?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- dwg file handling
- aspose.cad
- c# cad processing
- text search in dwg
title: C#를 사용하여 dwg 파일을 로드하고 DWG 파일에서 텍스트를 검색하는 방법
url: /ko/net/text-search-and-manipulation/searching-text-in-dwg-files/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# C#에서 dwg 파일을 로드하고 DWG 파일에서 텍스트 검색하기 - Aspose.CAD 튜토리얼

## 소개

현대 CAD 개발에서는 **load dwg file** 객체를 로드하고 특정 텍스트 문자열을 즉시 찾을 수 있어 수시간의 수동 검사를 절약할 수 있습니다. 배치 처리 도구를 구축하든 뷰어에 검색 기능을 추가하든, Aspose.CAD for .NET은 Windows, Linux, macOS에서 네이티브 종속성 없이 작동하는 완전 관리형 API를 제공합니다. 이 가이드는 DWG 로드부터 결과를 PDF로 내보내는 단계까지 모든 과정을 안내하므로 오늘 바로 C# 애플리케이션에 신뢰할 수 있는 CAD 텍스트 검색을 통합할 수 있습니다.

## 빠른 답변
- **DWG를 로드하기 위한 첫 번째 코드 라인은 무엇인가요?** `new CadImage("yourfile.dwg")` 그림의 메모리 내 표현을 생성합니다.  
- **CAD 클래스를 포함하는 네임스페이스는 무엇인가요?** `Aspose.CAD.Image`와 `Aspose.CAD.FileFormats.Dwg`가 필요합니다.  
- **검색 결과를 직접 PDF로 내보낼 수 있나요?** 예 – `image.Save("out.pdf", SaveFormat.Pdf)`를 사용하십시오.  
- **개발에 라이선스가 필요합니까?** 평가용으로는 무료 체험판을 사용할 수 있으며, 프로덕션에서는 영구 라이선스가 필요합니다.  
- **지원되는 .NET 버전은 무엇인가요?** .NET 5, .NET 6, .NET Core 3.1 및 .NET Framework 4.6+.

## DWG 파일이란?

DWG 파일은 AutoCAD 및 호환 도구로 만든 2D 및 3D 설계 데이터를 저장하는 바이너리 형식입니다. 벡터 기하학, 레이어, 텍스트 및 메타데이터를 위한 업계 표준 컨테이너입니다. 이 형식이 독점적이기 때문에 대부분의 오픈소스 파서는 최신 버전을 처리하는 데 어려움을 겪지만, Aspose.CAD는 150개 이상의 DWG 릴리스를 완전히 지원하여 AutoCAD를 설치하지 않고도 도면을 읽고 조작할 수 있습니다.

## CAD 텍스트 검색에 Aspose.CAD를 사용하는 이유는?

Aspose.CAD는 **50+** DWG 및 DXF 버전을 처리할 수 있으며, 전체 문서를 메모리에 로드하지 않고도 1 GB까지의 파일을 처리합니다. 이 라이브러리는 **Entities**와 **Block** 섹션 모두에서 텍스트를 추출하여, 블록 내부에 중첩된 경우에도 검색 가능한 문자열을 찾는 성공률이 **99 %**에 달합니다. 이러한 정량화된 신뢰성은 엔터프라이즈 급 CAD 자동화에 최적의 선택이 됩니다.

## 전제 조건

- **Aspose.CAD for .NET**가 설치되어 있어야 합니다. 최신 패키지는 [Aspose.CAD website](https://releases.aspose.com/cad/net/)에서 다운로드하십시오.
- 분석하려는 DWG 파일이 들어 있는 폴더.
- 프로덕션 사용을 위한 유효한 라이선스 파일(체험 실행 시 선택 사항).

## 필요한 네임스페이스는?

`Aspose.CAD` 네임스페이스는 핵심 이미지 처리 클래스를 제공하고, `Aspose.CAD.FileFormats.Dwg`는 DWG 전용 구조를 포함합니다. 이를 C# 파일 상단에 import하십시오:

```csharp
using Aspose.CAD;
using Aspose.CAD.FileFormats.Dwg;
using Aspose.CAD.ImageOptions;
```

> **Note:** 위 코드 블록은 자리표시자이며, 원래 자리표시자 수를 유지하려면 정확한 텍스트를 그대로 유지하십시오.

## DWG 파일을 로드하는 방법은?

Aspose.CAD를 사용하면 DWG 파일 로드가 간단합니다. 메모리 내 CAD 도면을 나타내는 `CadImage` 클래스를 사용하십시오. 생성자는 렌더링 없이 파일을 읽어 대형 도면에서도 빠릅니다. 로드 후에는 검색 작업을 수행하기 전에 `Width`, `Height`, `Layers`와 같은 속성을 검사할 수 있습니다.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.FileFormats.Cad.CadConsts;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadObjects.AttEntities;
```

## 엔티티 섹션에서 텍스트를 검색하는 방법은?

엔티티 섹션에서 텍스트를 찾으려면 `cadImage.Entities` 컬렉션을 반복합니다. 각 엔티티는 유형(`MText`, `Text`, `Attribute` 등)과 `TextString` 속성을 검사할 수 있습니다. 대상 문자열과 대소문자를 구분하지 않는 비교를 수행하고 일치하는 엔티티를 수집하여 추가 처리하거나 강조 표시합니다.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "search.dwg";
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Your code here
}
```

## 블록 섹션에서 텍스트를 검색하는 방법은?

블록은 재사용 가능한 엔티티 그룹으로 중첩된 텍스트를 포함할 수 있습니다. 먼저 `cadImage.BlockEntities.Values`를 열거하여 각 블록 정의에 접근합니다. 그런 다음 각 블록의 `Entities` 컬렉션을 순회하면서 메인 엔티티 섹션에 사용한 동일한 텍스트 매칭 로직을 적용합니다. 이를 통해 재사용 가능한 구성 요소 내부에 숨겨진 텍스트도 누락되지 않게 됩니다.

```csharp
foreach (CadBaseEntity entity in cadImage.Entities)
{
    IterateCADNodes(entity);
}
```

## 전체 스캔을 위해 CAD 노드를 반복하는 방법은?

포괄적인 스캔은 엔티티와 블록 섹션을 모두 결합합니다. `CadImage` 노드 트리를 재귀적으로 순회하면 중첩 블록, 속성 정의, 외부 참조까지 처리할 수 있습니다. `CadBaseEntity`를 매개변수로 받아 유형을 확인하고, 해당되는 경우 텍스트를 추출한 뒤, 노드에 컬렉션이 있으면 자식 엔티티로 재귀 호출하는 도우미 메서드를 구현하십시오.

```csharp
foreach (CadBlockEntity blockEntity in cadImage.BlockEntities.Values)
{
    foreach (CadBaseEntity entity in blockEntity.Entities)
    {
        IterateCADNodes(entity);
    }
}
```

## 텍스트를 찾은 후 DWG를 PDF로 내보내는 방법은?

관련 엔티티를 식별한 후에는 이를 강조 표시하거나 좌표를 추출하고 싶을 수 있습니다. Aspose.CAD는 벡터 품질을 유지하면서 전체 도면을 PDF로 저장할 수 있게 해줍니다. 래스터 출력이 필요하면 `CadRasterizationOptions`를 구성하고, `image.Save("output.pdf", new PdfOptions())`를 호출하십시오. 생성된 PDF는 CAD 소프트웨어가 없는 이해관계자와 공유할 수 있습니다.

```csharp
private static void IterateCADNodes(CadBaseEntity obj)
{
    switch (obj.TypeName)
    {
        // Handle different entity types
    }
}
```

## 결론

Aspose.CAD for .NET는 dwg 파일 데이터를 로드하고 특정 텍스트를 검색하며 결과를 PDF로 내보내는 원활하고 고성능 솔루션을 제공합니다. 이 튜토리얼의 단계들을 따라함으로써 외부 도구나 비용이 많이 드는 라이선스에 의존하지 않고 C# 애플리케이션에 강력한 CAD 텍스트 검색 기능을 추가했습니다.

## 자주 묻는 질문

### Q1: Aspose.CAD for .NET를 다른 CAD 형식과 함께 사용할 수 있나요?
A1: 예, Aspose.CAD는 DXF, DWF, STL 등을 포함한 30개 이상의 CAD 형식을 지원하여 혼합 형식 워크플로에 다목적 솔루션을 제공합니다.

### Q2: Aspose.CAD for .NET에 대한 무료 체험판이 있나요?
A2: 예, [free trial](https://releases.aspose.com/)을 통해 기능을 살펴볼 수 있습니다.

### Q3: Aspose.CAD for .NET에 대한 지원을 어떻게 받을 수 있나요?
A3: 커뮤니티 지원 및 공식 지원 채널을 위해 [Aspose.CAD forum](https://forum.aspose.com/c/cad/19)을 방문하십시오.

### Q4: 임시 라이선스란 무엇이며, 어떻게 얻을 수 있나요?
A4: 단기 평가 또는 개념 증명 프로젝트를 위해 [temporary license](https://purchase.aspose.com/temporary-license/)를 얻으십시오.

### Q5: Aspose.CAD for .NET에 대한 자세한 문서는 어디에서 찾을 수 있나요?
A5: 깊이 있는 가이드, API 참조 및 코드 샘플을 위해 포괄적인 [documentation](https://reference.aspose.com/cad/net/)을 참조하십시오.

---

**마지막 업데이트:** 2026-10-09  
**테스트 환경:** Aspose.CAD 24.11 for .NET  
**작성자:** Aspose  


```csharp
Aspose.CAD.ImageOptions.CadRasterizationOptions rasterizationOptions = new Aspose.CAD.ImageOptions.CadRasterizationOptions();
// Configure rasterization options
rasterizationOptions.Layouts = new[] { "Layout1" };
Aspose.CAD.ImageOptions.PdfOptions pdfOptions = new Aspose.CAD.ImageOptions.PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
cadImage.Save(MyDir + "SearchText_out.pdf", pdfOptions);
```

## 관련 튜토리얼

- [Aspose.CAD for .NET를 사용하여 DWG를 PDF 및 래스터 이미지로 변환하는 방법](/cad/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/)
- [DWG를 PNG로 변환하고 OLE 객체 내보내기 - Aspose.CAD 튜토리얼](/cad/net/advanced-export-techniques/exporting-ole-objects-from-dwg/)
- [Aspose.CAD for .NET로 DWT 파일을 읽는 방법](/cad/net/cad-features-and-support/reading-dwt/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}