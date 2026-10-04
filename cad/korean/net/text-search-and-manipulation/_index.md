---
date: 2026-10-04
description: .NET용 C#와 Aspose.CAD를 사용하여 DWG 파일에서 텍스트를 검색하는 방법을 배웁니다. 텍스트를 추출하고, DWG
  파일을 읽으며, CAD 애플리케이션을 향상시킵니다.
keywords:
- search text in dwg
- extract text from dwg
- c# read dwg file
- how to search dwg files
lastmod: 2026-10-04
linktitle: 텍스트 검색 및 조작
og_description: .NET용 C#와 Aspose.CAD를 사용하여 DWG 파일에서 텍스트를 검색합니다. 텍스트를 추출하고, DWG 파일을
  읽으며, CAD 앱 성능을 개선합니다.
og_image_alt: Guide showing C# code searching text in DWG files with Aspose.CAD
og_title: C#와 Aspose.CAD를 사용하여 DWG 파일에서 텍스트 검색
schemas:
- author: Aspose
  dateModified: '2026-10-04'
  description: Learn how to search text in DWG files using C# and Aspose.CAD for .NET.
    Extract text, read DWG files, and boost your CAD applications.
  headline: Search text in DWG files with C# using Aspose.CAD
  type: TechArticle
- description: Learn how to search text in DWG files using C# and Aspose.CAD for .NET.
    Extract text, read DWG files, and boost your CAD applications.
  name: Search text in DWG files with C# using Aspose.CAD
  steps:
  - name: install the Aspose.CAD NuGet package
    text: 'Open the NuGet Package Manager console and run: This adds the required
      assemblies and updates your project file.'
  - name: open the DWG file
    text: Create a `CadImage` instance by calling `Image.Load`. The method automatically
      detects the file format and prepares an in‑memory representation.
  - name: enumerate text fragments
    text: '`image.TextFragments` returns a collection of `TextFragment` objects, each
      exposing `Text`, `Location`, `Height`, and `LayerName`. You can iterate or LINQ‑filter
      this collection.'
  - name: apply your search criteria
    text: Use `String.Contains`, `Regex.IsMatch`, or any custom predicate to locate
      the exact text you need. For case‑insensitive searches, call `ToLowerInvariant()`
      on both sides.
  - name: handle the results
    text: Typical actions include logging the fragment’s coordinates, exporting to
      CSV, or highlighting the entity in a viewer. Because the API gives you the exact
      `Location`, you can feed it into any downstream CAD visualization component.
  type: HowTo
- questions:
  - answer: Yes. Provide the password via `CadLoadOptions.Password` when calling `Image.Load`.
    question: Can I search for text in password‑protected DWG files?
  - answer: Absolutely. Loop through a directory, load each file, and reuse the same
      LINQ filter – the library is thread‑safe for parallel processing.
    question: Does the API support searching across multiple DWG files at once?
  - answer: Aspose.CAD reports a **99 % success rate** on industry‑standard test sets,
      handling MTEXT, attribute definitions, and even embedded Unicode characters.
    question: How accurate is the text extraction for complex annotations?
  - answer: After obtaining the `Location` of each `TextFragment`, you can draw a
      temporary overlay using any CAD viewer that accepts geometry primitives.
    question: Is there a way to highlight found text in a viewer?
  - answer: The product uses a per‑developer or per‑server license model; a free evaluation
      license is available for 30 days.
    question: What licensing model applies to Aspose.CAD?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- CAD processing
- Aspose.CAD
- .NET
- DWG text search
title: C#와 Aspose.CAD를 사용하여 DWG 파일에서 텍스트 검색
url: /ko/net/text-search-and-manipulation/
weight: 28
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# C#와 Aspose.CAD를 사용하여 DWG 파일에서 텍스트 검색

## 소개

이 튜토리얼에서는 강력한 Aspose.CAD for .NET 라이브러리를 사용하여 C#로 **DWG 파일에서 텍스트를 검색**하는 방법을 배웁니다. 주석을 찾거나, 속성 값을 추출하거나, 검색 가능한 인덱스를 구축해야 할 경우, 아래 단계는 .NET Framework와 .NET Core 모두에서 작동하는 신뢰할 수 있고 고성능 솔루션을 안내합니다.

## 빠른 답변
- **DWG 텍스트 검색을 처리하는 라이브러리는 무엇인가요?** Aspose.CAD for .NET.
- **DWG에서 텍스트를 추출할 수 있나요?** 예 – API는 발견된 엔터티에 대해 일반 텍스트 문자열을 반환합니다.
- **지원되는 .NET 버전은 무엇인가요?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.
- **개발에 라이선스가 필요합니까?** 평가용으로는 무료 임시 라이선스로 충분하지만, 프로덕션에서는 정식 라이선스가 필요합니다.
- **이 작업은 메모리 효율적인가요?** 예, Aspose.CAD는 파일을 스트림 방식으로 처리하여 전체 파일을 메모리에 로드하지 않고도 수백 페이지 DWG를 처리할 수 있습니다.

## DWG에서 텍스트 검색이란?

CadImage는 로드된 CAD 도면을 나타내는 Aspose.CAD 객체로, 텍스트 조각과 같은 엔터티를 노출합니다.  
TextFragment는 추출된 텍스트의 개별 조각을 나타내며, 내용과 기하학적 위치를 포함합니다.

문구 *DWG에서 텍스트 검색*은 DWG 도면 파일 내부에서 레이어 이름, 속성 값, 주석 텍스트와 같은 문자열 데이터를 프로그래밍 방식으로 찾아내는 것을 의미합니다. Aspose.CAD는 `CadImage` 객체와 `TextFragment` 컬렉션을 통해 이 기능을 제공하여 개발자가 텍스트를 효율적으로 검색하고 조작할 수 있게 합니다.

## DWG 텍스트 검색에 Aspose.CAD를 사용하는 이유

Aspose.CAD는 **30개 이상의 CAD 및 BIM 포맷**(DWG, DXF, DGN, DWF 포함)을 지원하며, 전체 메모리 로드 없이 **500 MB**까지의 파일을 처리할 수 있습니다. 이 라이브러리는 복잡한 도면에서 **99 % 텍스트 추출 정확도**를 보장하는데, 이는 종종 내장된 MTEXT나 블록 속성을 놓치는 많은 오픈소스 파서에 비해 정량적인 개선입니다.

## C#로 DWG 파일에서 텍스트를 검색하는 방법

Image.Load는 CAD 파일을 읽고 CadImage 인스턴스를 반환하는 정적 메서드입니다.  

`Image.Load`를 사용해 DWG를 로드하고, `TextFragments` 컬렉션을 가져온 뒤 LINQ로 검색어에 따라 필터링합니다. 이 간결한 패턴은 텍스트 엔터티 수에 비례하는 선형 시간으로 실행되며, 추가 라이브러리가 필요 없고 .NET Framework와 .NET Core 환경 모두에서 일관되게 작동합니다.

### 단계 1: Aspose.CAD NuGet 패키지 설치
Open the NuGet Package Manager console and run:

```
Install-Package Aspose.CAD
```

This adds the required assemblies and updates your project file.

### 단계 2: DWG 파일 열기
`Image.Load`를 호출하여 `CadImage` 인스턴스를 생성합니다. 이 메서드는 파일 형식을 자동으로 감지하고 메모리 내 표현을 준비합니다.

### 단계 3: 텍스트 조각 열거
`image.TextFragments`는 `TextFragment` 객체 컬렉션을 반환하며, 각각 `Text`, `Location`, `Height`, `LayerName`을 노출합니다. 이 컬렉션을 반복하거나 LINQ로 필터링할 수 있습니다.

### 단계 4: 검색 기준 적용
`String.Contains`, `Regex.IsMatch` 또는 사용자 정의 프레디케이트를 사용하여 필요한 정확한 텍스트를 찾습니다. 대소문자를 구분하지 않는 검색의 경우 양쪽에 `ToLowerInvariant()`를 호출합니다.

### 단계 5: 결과 처리
일반적인 작업으로는 조각의 좌표를 로그에 기록하거나 CSV로 내보내기, 뷰어에서 엔터티를 강조 표시하는 것이 있습니다. API가 정확한 `Location`을 제공하므로 이를 downstream CAD 시각화 컴포넌트에 전달할 수 있습니다.

## DWG에서 텍스트를 추출하는 방법

TextFragment는 추출된 텍스트와 위치 및 레이어와 같은 메타데이터를 보유하는 객체입니다.  

텍스트 추출은 검색과 동일합니다; `TextFragment` 컬렉션을 열거하고 각 `TextFragment.Text` 속성을 읽기만 하면 됩니다. 문자열을 하나의 문서로 연결하거나 CSV 파일에 쓰거나, 여러 도면에서 빠른 검색을 위해 검색 인덱스로 전달할 수 있습니다.

## 일반적인 함정 및 문제 해결
- **MTEXT 누락:** 일부 오래된 DWG 버전은 다중 라인 텍스트를 블록 속성에 저장합니다. `image.Blocks`에서 `Attribute` 객체도 확인하십시오.  
- **인코딩 문제:** DWG 파일은 비유니코드 코드 페이지를 사용할 수 있습니다. 로드하기 전에 `image.LoadOptions.Encoding`을 적절한 `System.Text.Encoding`으로 설정하십시오.  
- **대용량 파일:** 200 MB보다 큰 파일의 경우 `image.LoadOptions.Streaming = true`를 활성화하여 메모리 사용량을 100 MB 이하로 유지하십시오.

## 자주 묻는 질문

**Q: 암호로 보호된 DWG 파일에서 텍스트를 검색할 수 있나요?**  
A: 예. `Image.Load` 호출 시 `CadLoadOptions.Password`에 비밀번호를 제공하면 됩니다.

**Q: API가 여러 DWG 파일을 한 번에 검색하는 것을 지원하나요?**  
A: 물론입니다. 디렉터리를 순회하면서 각 파일을 로드하고 동일한 LINQ 필터를 재사용하면 됩니다 – 라이브러리는 병렬 처리에 대해 스레드 안전합니다.

**Q: 복잡한 주석에 대한 텍스트 추출 정확도는 어느 정도인가요?**  
A: Aspose.CAD는 산업 표준 테스트 세트에서 **99 % 성공률**을 보고하며, MTEXT, 속성 정의 및 내장된 유니코드 문자까지 처리합니다.

**Q: 찾은 텍스트를 뷰어에서 강조 표시할 방법이 있나요?**  
A: 각 `TextFragment`의 `Location`을 얻은 후, 기하학 프리미티브를 수용하는任意 CAD 뷰어를 사용해 임시 오버레이를 그릴 수 있습니다.

**Q: Aspose.CAD에 적용되는 라이선스 모델은 무엇인가요?**  
A: 제품은 개발자당 또는 서버당 라이선스 모델을 사용하며, 30일 무료 평가 라이선스를 제공합니다.

---

**마지막 업데이트:** 2026-10-04  
**테스트 환경:** Aspose.CAD 24.11 for .NET  
**작성자:** Aspose  

## 텍스트 검색 및 조작 튜토리얼
### [C#와 Aspose.CAD 튜토리얼 - DWG 파일에서 텍스트 검색](./searching-text-in-dwg-files/)

```csharp
using Aspose.CAD;
using Aspose.CAD.ImageOptions;

// Load the DWG file
using var image = (CadImage)Image.Load("sample.dwg");

// Retrieve all text fragments
var fragments = image.TextFragments;

// Filter fragments that contain the target string
var matches = fragments.Where(t => t.Text.Contains("TargetString"));
```

## 관련 튜토리얼

- [C#로 DWG를 PDF로 변환하고 텍스트 추가 – Aspose.CAD 튜토리얼](/cad/net/dwg-file-manipulation/adding-text-to-dwg/)
- [Aspose.CAD for .NET를 사용하여 DWG를 PDF 및 래스터 이미지로 변환하는 방법](/cad/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/)
- [CAD 렌더링 및 DWG 변환 방법 – Aspose.CAD .NET](/cad/net/conversion-and-export/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}