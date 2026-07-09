---
date: 2026-07-09
description: Aspose.CAD for .NET를 사용하여 IGES를 PDF로 변환하는 방법을 배웁니다. 단계별 가이드를 따라 IGES
  파일을 빠르고 정확하게 PDF로 내보내세요.
keywords:
- convert iges to pdf
- export iges as pdf
- create pdf from iges
- convert cad file to pdf
- generate pdf from cad
lastmod: 2026-07-09
linktitle: IGES 파일을 PDF로 내보내기
og_description: Aspose.CAD for .NET를 사용하여 IGES를 PDF로 변환합니다. 이 튜토리얼은 코드 없이 단계별로 IGES
  파일을 효율적으로 PDF로 내보내는 방법을 보여줍니다.
og_image_alt: Guide showing conversion of IGES files to PDF with Aspose.CAD in .NET
og_title: IGES를 PDF로 변환 – Aspose.CAD 빠른 가이드
schemas:
- author: Aspose
  dateModified: '2026-07-09'
  description: Learn how to convert IGES to PDF using Aspose.CAD for .NET. Follow
    this step‑by‑step guide to export IGES files as PDF quickly and accurately.
  headline: Convert IGES to PDF with Aspose.CAD – Quick Guide
  type: TechArticle
- description: Learn how to convert IGES to PDF using Aspose.CAD for .NET. Follow
    this step‑by‑step guide to export IGES files as PDF quickly and accurately.
  name: Convert IGES to PDF with Aspose.CAD – Quick Guide
  steps:
  - name: Set up Your Project
    text: Create a new .NET console or class‑library project, or open an existing
      one where you want to add the conversion feature.
  - name: Add Aspose.CAD Reference
    text: Add the downloaded Aspose.CAD DLL to your project references. In Visual
      Studio, right‑click **References → Add Reference → Browse** and select the DLL.
  - name: Initialize the Path
    text: Define the folder that contains your IGES file and the output location.
  - name: Load the CAD Image
    text: '`Image.Load` reads the IGES file and creates an in‑memory representation.
      The `Image` class is Aspose.CAD''s primary entry point for any CAD format.'
  - name: Configure Rasterization Options
    text: '`PdfOptions` (derived from `CadRasterizationOptions`) lets you set page
      size, resolution, and vector‑preserving flags. The `PdfOptions` class defines
      how the CAD drawing is rasterized and saved as PDF.'
  - name: Save as PDF
    text: Finally, write the PDF file to disk. With these six straightforward steps,
      you have successfully **convert iges to pdf** using Aspose.CAD for .NET.
  type: HowTo
- questions:
  - answer: Yes, Aspose.CAD works in ASP.NET, ASP.NET Core, and other web frameworks,
      providing server‑side conversion without UI dependencies.
    question: Can I use Aspose.CAD for .NET in a web application?
  - answer: Explore the comprehensive documentation [here](https://reference.aspose.com/cad/net/)
      for detailed insights into all supported features.
    question: Where can I find additional documentation for Aspose.CAD?
  - answer: Yes, you can access a free trial [here](https://releases.aspose.com/)
      to evaluate the library before purchasing.
    question: Is there a free trial available?
  - answer: For temporary licenses, visit [this link](https://purchase.aspose.com/temporary-license/)
      to get the required licensing information.
    question: How can I obtain a temporary license?
  - answer: Join the Aspose.CAD community on the [support forum](https://forum.aspose.com/c/cad/19)
      for prompt help and discussions.
    question: Need assistance or have questions?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- convert iges to pdf
- Aspose.CAD
- .NET CAD conversion
title: Aspose.CAD를 사용하여 IGES를 PDF로 변환 – 빠른 가이드
url: /ko/net/exporting-to-image-formats/exporting-iges-files-to-pdf/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD를 사용하여 IGES를 PDF로 변환

## 소개

컴퓨터 지원 설계(CAD)의 빠르게 변화하는 세계에서 **convert IGES to PDF**는 엔지니어와 건축가가 매일 수행하는 일상적인 작업입니다. 클라이언트 검토를 위한 인쇄 가능한 문서가 필요하든 버전 관리를 위한 가벼운 아카이브가 필요하든, IGES 파일을 PDF로 내보내면 원본 기하학을 보존하면서 파일을 모든 장치에서 접근 가능하게 만들 수 있습니다. 이 튜토리얼에서는 Aspose.CAD for .NET을 사용하여 IGES를 PDF로 변환하는 정확한 단계를 안내하므로 .NET 애플리케이션 어디에서든 프로세스를 자동화할 수 있습니다.

## 빠른 답변
- **어떤 라이브러리가 변환을 처리합니까?** Aspose.CAD for .NET.  
- **필요한 코드 라인은 몇 줄입니까?** 일반적으로 두 줄: IGES 파일을 로드하고 `Save`를 호출합니다.  
- **페이지 크기와 품질을 제어할 수 있나요?** 예, `CadRasterizationOptions`를 통해 가능합니다.  
- **프로덕션에 라이선스가 필요합니까?** 상업용 라이선스가 필요합니다; 무료 체험판을 사용할 수 있습니다. 임시 라이선스는 [이 링크](https://purchase.aspose.com/temporary-license/)에서 얻을 수 있습니다.  
- **지원되는 .NET 버전은 무엇입니까?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.

## “convert IGES to PDF”란 무엇인가요?
*Converting IGES to PDF*는 중립적인 CAD 교환 파일(IGES)을 모든 장치에서 CAD 소프트웨어 없이 열 수 있는 포터블 문서 형식(PDF)으로 렌더링하는 것을 의미합니다. 변환은 벡터 기하학, 레이어 및 주석을 보존하면서 고정 레이아웃 문서로 평면화합니다.

## 이 변환에 Aspose.CAD를 사용하는 이유는?
Aspose.CAD는 **30개 이상의 CAD 및 BIM 포맷**을 지원하며 전체 문서를 메모리에 로드하지 않고 **2 GB**까지 처리할 수 있어 빠른 서버‑사이드 변환을 제공하고 타사 종속성이 없습니다. 이러한 성능은 배치 처리 파이프라인 및 클라우드 기반 서비스에 최적입니다.

## 사전 요구 사항

시작하기 전에 다음을 준비하십시오:

1. **Aspose.CAD for .NET Library** – [여기](https://releases.aspose.com/cad/net/)에서 다운로드하십시오. API 참조는 [여기](https://reference.aspose.com/cad/net/)에서 확인할 수 있습니다.  
2. **.NET 개발 환경** – Visual Studio, Rider 또는 .NET 5+를 지원하는 모든 IDE.

이제 사전 요구 사항이 충족되었으니 변환에 필요한 네임스페이스를 가져오겠습니다.

## 네임스페이스 가져오기

`Image` 클래스는 메모리 내에서 CAD 도면을 나타내는 기본 클래스입니다. `CadRasterizationOptions`는 벡터 출력용 CAD 도면의 래스터화 방식을 정의합니다. `PdfOptions` 클래스는 PDF 파일에 대한 출력 설정을 지정합니다.

``` 
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
```

이 네임스페이스들은 CAD 도면을 로드, 래스터화 및 저장하는 핵심 기능을 제공합니다.

## Aspose.CAD를 사용하여 IGES를 PDF로 변환하는 방법은?

`Image.Load`로 IGES 파일을 로드하고 즉시 PDF 래스터화 옵션과 함께 `Save`를 호출하면 두 문장만으로 전체 변환이 완료됩니다. 라이브러리는 벡터 렌더링, 글꼴 포함 및 페이지 스케일링을 자동으로 처리하므로 원본 IGES 모델의 정확한 PDF 복제본을 얻을 수 있습니다.

### 단계 1: 프로젝트 설정

새 .NET 콘솔 또는 클래스‑라이브러리 프로젝트를 만들거나 변환 기능을 추가하려는 기존 프로젝트를 엽니다.

### 단계 2: Aspose.CAD 참조 추가

다운로드한 Aspose.CAD DLL을 프로젝트 참조에 추가합니다. Visual Studio에서 **References → Add Reference → Browse**를 마우스 오른쪽 버튼으로 클릭하고 DLL을 선택합니다.

### 단계 3: 경로 초기화

IGES 파일이 들어 있는 폴더와 출력 위치를 정의합니다.

``` 
string sourceDir = @"C:\CAD\Source";
string outputDir = @"C:\CAD\Output";
string igesFile = Path.Combine(sourceDir, "sample.iges");
string pdfFile = Path.Combine(outputDir, "sample.pdf");
```

### 단계 4: CAD 이미지 로드

`Image.Load`가 IGES 파일을 읽고 메모리 내 표현을 생성합니다.

``` 
Image cadImage = Image.Load(igesFile);
```

`Image` 클래스는 Aspose.CAD가 모든 CAD 포맷을 처리하는 주요 진입점입니다.

### 단계 5: 래스터화 옵션 구성

`PdfOptions`(`CadRasterizationOptions`에서 파생) 를 사용하면 페이지 크기, 해상도 및 벡터 보존 플래그를 설정할 수 있습니다.

``` 
PdfOptions pdfOptions = new PdfOptions
{
    VectorRasterizationOptions = new CadRasterizationOptions
    {
        PageWidth = 842,      // A4 width in points
        PageHeight = 595,     // A4 height in points
        Resolution = 300      // 300 DPI for high‑quality output
    }
};
```

`PdfOptions` 클래스는 CAD 도면이 어떻게 래스터화되고 PDF로 저장되는지를 정의합니다.

### 단계 6: PDF로 저장

마지막으로 PDF 파일을 디스크에 기록합니다.

``` 
cadImage.Save(pdfFile, pdfOptions);
```

이 여섯 단계만으로 Aspose.CAD for .NET을 사용하여 **convert iges to pdf**를 성공적으로 수행했습니다.

## 일반적인 함정 및 팁

- **대용량 파일:** 더 세밀한 디테일이 필요할 때만 `Resolution`을 높이세요; 높은 DPI는 메모리 사용량을 증가시킵니다.  
- **글꼴 누락:** IGES 파일에 사용된 사용자 정의 글꼴이 서버에 설치되어 있는지 확인하십시오. 그렇지 않으면 대체 글꼴이 적용됩니다.  
- **배치 변환:** `foreach` 루프에 로드‑저장 로직을 감싸서 여러 IGES 파일을 자동으로 처리하도록 하세요.

## 자주 묻는 질문

**Q: Aspose.CAD for .NET을 웹 애플리케이션에서 사용할 수 있나요?**  
A: 예, Aspose.CAD는 ASP.NET, ASP.NET Core 및 기타 웹 프레임워크에서 작동하며 UI 종속성 없이 서버‑사이드 변환을 제공합니다.

**Q: Aspose.CAD에 대한 추가 문서는 어디에서 찾을 수 있나요?**  
A: 자세한 기능 정보를 보려면 포괄적인 문서 [여기](https://reference.aspose.com/cad/net/)를 탐색하십시오.

**Q: 무료 체험판을 이용할 수 있나요?**  
A: 예, 라이브러리를 구매 전에 평가할 수 있도록 무료 체험판을 [여기](https://releases.aspose.com/)에서 이용할 수 있습니다.

**Q: 임시 라이선스는 어떻게 얻나요?**  
A: 임시 라이선스는 [이 링크](https://purchase.aspose.com/temporary-license/)에서 필요한 라이선스 정보를 확인하여 받을 수 있습니다.

**Q: 도움이 필요하거나 질문이 있나요?**  
A: 신속한 지원과 토론을 위해 Aspose.CAD 커뮤니티 [지원 포럼](https://forum.aspose.com/c/cad/19)에 참여하십시오.

---

**마지막 업데이트:** 2026-07-09  
**테스트 환경:** Aspose.CAD 24.11 for .NET  
**작성자:** Aspose

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadConsts;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using static Aspose.CAD.Examples.CSharp.DWG_Drawings.SupportMLeaderEntityForDWGFormat;
using Aspose.CAD.ImageOptions;
```

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "figa2.igs";
```

```csharp
using (Image cadImage = Image.Load(sourceFilePath))
{
    // Your code goes here
}
```

```csharp
CadRasterizationOptions options = new CadRasterizationOptions
{
    PageHeight = 1000,
    PageWidth = 1000,
};

PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = options;
```

```csharp
cadImage.Save(MyDir + "figa2.pdf", pdfOptions);
```

추가 리소스는 메인 릴리스 페이지 [여기](https://releases.aspose.com/)를 참조하십시오. 도움이 필요하면 [지원 포럼](https://forum.aspose.com/c/cad/19)을 방문하십시오.

## 관련 튜토리얼

- [DWG를 PDF 또는 래스터 이미지로 내보내기 - Aspose.CAD 가이드](/cad/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/)
- [DXF를 PDF 형식으로 내보내기 - Aspose.CAD 튜토리얼](/cad/net/export-techniques/exporting-dxf-to-pdf-format/)
- [Aspose.CAD for .NET에서 DGN을 PDF로 내보내기](/cad/net/cad-export-formats/export-dgn-to-pdf/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}