---
date: 2026-08-12
description: Aspose.CAD for .NET를 사용하여 DWG에서 텍스트를 추출하고 특정 DWG를 C#에서 이미지로 변환합니다. 단계별
  코드 스니펫을 통해 학습하세요.
keywords:
- extract text from dwg
- convert specific dwg to image
- Aspose.CAD .NET
lastmod: 2026-08-12
linktitle: 특정 DWG를 C#에서 이미지로 변환
og_description: Aspose.CAD를 사용하여 DWG에서 텍스트를 추출하고 특정 DWG를 C#에서 이미지로 변환합니다. 빠른 구현을 위한
  간결한 가이드를 따라보세요.
og_image_alt: Guide showing DWG to image conversion and text extraction using Aspose.CAD
  in C#
og_title: DWG에서 텍스트를 추출하고 특정 DWG를 C#에서 이미지로 변환
schemas:
- author: Aspose
  dateModified: '2026-08-12'
  description: Extract text from DWG and convert specific DWG to image in C# using
    Aspose.CAD for .NET. Learn step‑by‑step with code snippets.
  headline: Extract text from DWG and convert specific DWG to image in C#
  type: TechArticle
- questions:
  - answer: Aspose.CAD supports DWG releases from AutoCAD 2000 up to the latest 2024
      version, covering over 90 % of files created in the field.
    question: Is Aspose.CAD compatible with all versions of DWG files?
  - answer: Yes – you can change resolution, image format, anti‑aliasing, and background
      color to suit PNG, JPEG, or PDF targets.
    question: Can I customize the rasterization options for different outputs?
  - answer: Explore the comprehensive [Aspose.CAD documentation](https://reference.aspose.com/cad/net/)
      for more code samples and API details.
    question: Where can I find additional examples and documentation?
  - answer: Absolutely – you can download a trial version on the **[Aspose trial download
      page](https://releases.aspose.com/)** and evaluate all features without restrictions
      for 30 days.
    question: Is there a free trial available for Aspose.CAD?
  - answer: Join the active [Aspose.CAD forum](https://forum.aspose.com/c/cad/19)
      where developers share solutions and the Aspose team answers questions.
    question: How can I get support or connect with the community?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- extract text from dwg
- Aspose.CAD
- C# CAD processing
title: DWG에서 텍스트를 추출하고 특정 DWG를 C#에서 이미지로 변환
url: /ko/net/image-manipulation-and-rendering/converting-particular-dwg-to-image/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# C#에서 특정 DWG를 이미지로 변환하기 - Aspose.CAD 가이드

## 소개

현대 엔지니어링 애플리케이션에서는 보고서 작성이나 시각화를 위해 **DWG에서 텍스트 추출** 및 **특정 DWG를 이미지로 변환** 형식이 자주 필요합니다. Aspose.CAD for .NET은 외부 CAD 소프트웨어 없이도 두 작업을 모두 처리할 수 있는 완전한 기능을 갖춘 API를 제공합니다. 이 튜토리얼에서는 DWG를 로드하고, 텍스트 엔터티를 필터링하며, 도면을 래스터화하고, 최종적으로 결과를 PDF 이미지로 저장하는 방법을 깔끔한 C# 코드로 배웁니다.

## 빠른 답변
- **첫 번째 단계는 무엇인가요?** `new CadImage("file.dwg")` 로 DWG 파일을 로드합니다.  
- **텍스트를 필터링하는 클래스는 무엇인가요?** `CadEntityFilter` 를 사용하여 `Text` 엔터티를 선택합니다.  
- **이미지 크기를 어떻게 정의하나요?** `CadRasterizationOptions` 에서 `Width`와 `Height`를 설정합니다.  
- **사용되는 출력 형식은 무엇인가요?** 예제는 PDF로 저장하며, PDF에 래스터 이미지가 포함됩니다.  
- **프로덕션에 라이선스가 필요합니까?** 예 – 상용 Aspose.CAD 라이선스를 사용하면 평가 제한이 해제됩니다.

## DWG에서 텍스트를 추출하는 방법

DWG를 로드하고, 텍스트 엔터티만 선택하는 필터를 적용한 다음 각 엔터티의 `TextString` 속성을 읽습니다. 이 방법은 도면에 존재하는 모든 주석, 레이블 또는 치수 텍스트를 반환하므로 검색, 인덱싱 또는 보고에 재사용할 수 있습니다.

## 특정 DWG를 이미지로 변환하는 이유

DWG를 래스터 이미지로 변환하면 네이티브 CAD 형식을 렌더링할 수 없는 문서, 웹 페이지 또는 모바일 앱에 도면을 삽입할 수 있습니다. Aspose.CAD는 **50개 이상의 CAD 형식**을 처리하며, 200 MB 미만의 메모리로 수백 페이지에 달하는 도면을 래스터화할 수 있어 고처리량 서버 시나리오에 적합합니다.

## 사전 요구 사항

- C# 프로젝트를 컴파일하고 실행하기 위한 Visual Studio(최근 버전 중 하나).  
- Aspose.CAD for .NET – 라이브러리가 설치되어 있는지 확인하십시오. 다운로드 링크는 **[Aspose.CAD for .NET 다운로드 페이지](https://releases.aspose.com/cad/net/)** 에서 찾을 수 있습니다.  
- 작업하려는 DWG 파일; 코드 스니펫에서는 샘플 파일 *visualization_-_conference_room.dwg* 를 사용합니다.

## 네임스페이스 가져오기

다음 네임스페이스를 통해 핵심 CAD 클래스, 래스터화 옵션 및 PDF 출력 도우미에 접근할 수 있습니다:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadConsts;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## 단계 1: dwg 파일 로드

`CadImage` 인스턴스를 생성하면서 DWG 파일 경로를 전달합니다. `CadImage` 객체는 메모리 내에 전체 도면을 나타내며 레이어, 엔터티 및 메타데이터에 접근할 수 있게 합니다.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "visualization_-_conference_room.dwg";
var cadImage = (CadImage)Aspose.CAD.Image.Load(sourceFilePath);
```

## 단계 2: 엔터티 필터링

`CadEntityFilter`를 사용하면 필요한 엔터티만 선택할 수 있습니다. 이 가이드에서는 **텍스트** 객체만 유지하고, 라인, 원 및 최종 이미지에 포함하고 싶지 않은 기타 기하학을 제외하도록 구성합니다.

```csharp
CadBaseEntity[] entities = cadImage.Entities;
List<CadBaseEntity> filteredEntities = new List<CadBaseEntity>();

foreach (CadBaseEntity baseEntity in entities)
{
    // Selection or filtration of entities
    if (baseEntity.TypeName == CadEntityTypeName.TEXT)
    {
        filteredEntities.Add(baseEntity);
    }
}

cadImage.Entities = filteredEntities.ToArray();
```

## 단계 3: 래스터화 옵션 설정

`CadRasterizationOptions`는 도면을 비트맵으로 변환하는 방식을 제어합니다. 출력 크기, 배경 색상 및 해상도(DPI)를 정의할 수 있습니다. 다음 정의 앵커가 클래스를 소개합니다:

`CadRasterizationOptions` 클래스는 CAD 도면을 래스터 형식으로 변환하기 위한 이미지 차원, 해상도 및 렌더링 설정을 지정합니다.  

PDF 내보내기에 옵션을 전달하기 전에 원하는 너비, 높이 및 배경 색상을 설정합니다.

```csharp
Aspose.CAD.ImageOptions.CadRasterizationOptions rasterizationOptions =
    new Aspose.CAD.ImageOptions.CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
rasterizationOptions.AutomaticLayoutsScaling = true;
```

## 단계 4: PDF 옵션 설정

`PdfOptions`는 압축과 같은 PDF 전용 기능과 래스터화 설정을 함께 묶습니다. 이 클래스에 대한 정의 앵커가 먼저 나타납니다:

`PdfOptions`는 PDF 문서 내에서 CAD 데이터가 렌더링되는 방식을 결정하는 래스터화 옵션을 포함한 PDF 생성 매개변수를 캡슐화합니다.  

이전에 만든 `CadRasterizationOptions` 인스턴스를 `VectorRasterizationOptions` 속성에 할당합니다.

```csharp
Aspose.CAD.ImageOptions.PdfOptions pdfOptions = new Aspose.CAD.ImageOptions.PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## 단계 5: PDF로 저장

마지막으로 `CadImage` 객체의 `Save` 메서드를 호출하고 대상 파일 이름과 구성된 `PdfOptions`를 전달합니다. PDF에는 필터링된 도면의 고품질 이미지가 포함됩니다.

```csharp
string outFile = MyDir + "result_out_generated.pdf";
cadImage.Save(outFile, pdfOptions);
```

## 일반적인 문제 및 해결 방법

- **필터링 후 텍스트가 누락됨** – DWG에 실제로 `Text` 엔터티가 포함되어 있는지 확인하십시오; 일부 도면은 주석을 `MText`로 저장합니다. 필요에 따라 필터에 `MText`를 포함하도록 조정하십시오.  
- **출력 이미지가 비어 있음** – 래스터화 DPI가 충분히 높은지(300 DPI가 안전한 기본값) 확인하고, PDF를 볼 때 배경 색상이 투명으로 설정되지 않았는지 확인하십시오.  
- **대용량 파일에서 메모리 부족 오류** – 스트리밍을 가능하게 하는 `LoadOptions` 오버로드를 사용하면 파일 전체를 한 번에 메모리로 로드하는 것을 방지할 수 있습니다.

## 자주 묻는 질문

**Q: Aspose.CAD가 모든 버전의 DWG 파일과 호환됩니까?**  
A: Aspose.CAD는 AutoCAD 2000부터 최신 2024 버전까지의 DWG 릴리스를 지원하며, 현장에서 생성된 파일의 90 % 이상을 커버합니다.

**Q: 다양한 출력에 대해 래스터화 옵션을 맞춤 설정할 수 있나요?**  
A: 예 – 해상도, 이미지 형식, 안티앨리어싱 및 배경 색상을 PNG, JPEG 또는 PDF 대상에 맞게 변경할 수 있습니다.

**Q: 추가 예제와 문서는 어디에서 찾을 수 있나요?**  
A: 더 많은 코드 샘플과 API 세부 정보를 보려면 포괄적인 [Aspose.CAD 문서](https://reference.aspose.com/cad/net/)를 살펴보세요.

**Q: Aspose.CAD의 무료 체험판이 있나요?**  
A: 물론입니다 – **[Aspose 체험판 다운로드 페이지](https://releases.aspose.com/)** 에서 체험판을 다운로드하여 30일 동안 제한 없이 모든 기능을 평가할 수 있습니다.

**Q: 지원을 받거나 커뮤니티와 연결하려면 어떻게 해야 하나요?**  
A: 개발자들이 솔루션을 공유하고 Aspose 팀이 질문에 답변하는 활발한 [Aspose.CAD 포럼](https://forum.aspose.com/c/cad/19) 에 참여하세요.

---

**마지막 업데이트:** 2026-08-12  
**테스트 환경:** Aspose.CAD 24.11 for .NET  
**작성자:** Aspose

## 관련 튜토리얼

- [C#를 사용한 DWG 파일 텍스트 검색 - Aspose.CAD 튜토리얼](/cad/net/text-search-and-manipulation/searching-text-in-dwg-files/)
- [.NET용 Aspose.CAD에서 CAD 도면을 래스터 이미지로 변환](/cad/net/cad-drawing-manipulation/convert-cad-drawing-to-raster-image/)
- [C#에서 DWG 문서 렌더링 - Aspose.CAD 가이드](/cad/net/image-manipulation-and-rendering/rendering-dwg-documents/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< blocks/products/products-backtop-button >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}