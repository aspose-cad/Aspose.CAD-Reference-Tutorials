---
date: 2026-07-04
description: Aspose.CAD for .NET를 사용하여 3D CAD 이미지에서 PDF 페이지 크기를 설정하고 PDF를 내보내는 방법을
  배웁니다 – DWG를 PDF로 변환하고 CAD를 PDF로 저장하는 단계별 가이드.
keywords:
- set pdf page size
- export pdf from cad
- convert dwg to pdf
- save cad as pdf
- cad to pdf tutorial
linktitle: 3D 이미지를 PDF로 내보내기
schemas:
- author: Aspose
  dateModified: '2026-07-04'
  description: Learn how to set PDF page size and export PDF from 3D CAD images using
    Aspose.CAD for .NET – a step‑by‑step guide to convert DWG to PDF and save CAD
    as PDF.
  headline: Set PDF page size – Export 3D Images to PDF with Aspose.CAD
  type: TechArticle
- description: Learn how to set PDF page size and export PDF from 3D CAD images using
    Aspose.CAD for .NET – a step‑by‑step guide to convert DWG to PDF and save CAD
    as PDF.
  name: Set PDF page size – Export 3D Images to PDF with Aspose.CAD
  steps:
  - name: Load the CAD Image
    text: '`Image` class represents a CAD drawing loaded into memory, ready for rasterization.'
  - name: Configure Rasterization Options (Save CAD as PDF)
    text: '`RasterizationOptions` class defines how the CAD data is rasterized, including
      page size, DPI, and whether 3‑D entities are rendered.'
  - name: Set PDF Options (Create PDF from CAD)
    text: '`PdfOptions` class holds the output format settings and links the rasterization
      options to PDF generation.'
  - name: Save as PDF (Generate PDF from 3D Model)
    text: '`Save` method on the `Image` object writes the rasterized content to the
      specified PDF file, producing a ready‑to‑share document.'
  type: HowTo
- questions:
  - answer: Yes, Aspose.CAD supports more than 50 input and output formats, including
      DWG, DXF, DGN, STL, and IFC, ensuring flexibility for any project.
    question: Is Aspose.CAD compatible with all CAD file formats?
  - answer: Absolutely. Set `PageWidth` and `PageHeight` in `RasterizationOptions`
      to any size in points, inches, or millimetres before calling `Save`.
    question: Can I customize the page dimensions when exporting to PDF?
  - answer: Yes, you can obtain temporary licenses for Aspose.CAD by visiting [Temporary
      License](https://purchase.aspose.com/temporary-license/).
    question: Are temporary licenses available for Aspose.CAD?
  - answer: Head to the [Aspose.CAD Forum](https://forum.aspose.com/c/cad/19) for
      expert help and peer‑to‑peer advice.
    question: Where can I find additional support or community discussions?
  - answer: Yes, you can explore the features of Aspose.CAD by accessing the [free
      trial](https://releases.aspose.com/).
    question: Is there a free trial version of Aspose.CAD?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: PDF 페이지 크기 설정 – Aspose.CAD로 3D 이미지 PDF 내보내기
url: /ko/net/3d-image-export/exporting-3d-images-to-pdf/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 3D 이미지 PDF로 내보내기 - Aspose.CAD 튜토리얼

## 소개

3‑D CAD 도면을 PDF로 변환하면서 **PDF 페이지 크기 설정**이 필요하다면, 바로 여기가 정답입니다. 이 튜토리얼에서는 CAD 파일을 로드하고, 사용자 정의 페이지 크기를 포함한 래스터화 옵션을 구성한 다음, Aspose.CAD for .NET을 사용해 고품질 PDF를 생성하는 방법을 단계별로 보여줍니다. 끝까지 따라오면 **export PDF from CAD**, **save CAD as PDF**를 수행하고 AutoCAD를 설치하지 않아도 모든 레이아웃 세부 사항을 제어할 수 있게 됩니다.

## 빠른 답변
- **What does “export PDF from CAD” mean?** CAD 도면(DWG, DXF, DGN 등)을 PDF로 변환하여 모든 장치에서 열 수 있게 합니다.  
- **Which library performs the conversion?** Aspose.CAD for .NET은 외부 종속성 없이 래스터화 및 PDF 내보내기를 제공합니다.  
- **Do I need a license?** 프로덕션 환경에서는 임시 또는 정식 라이선스가 필요하며, 무료 체험판을 사용할 수 있습니다.  
- **Can I set custom page dimensions?** 예 — `RasterizationOptions`에서 `PageWidth`와 `PageHeight`를 사용합니다.  
- **Will 3‑D geometry be retained?** 3‑D 엔터티는 래스터화되며, 전체 3‑D 지원을 위해 `TypeOfEntities.Entities3D`를 활성화합니다.

## CAD 컨텍스트에서 “export PDF”란 무엇인가요?

CAD에서 PDF를 내보낸다는 것은 CAD 도면(DWG, DXF, DGN 등)을 PDF 파일로 변환하는 것으로, 벡터 그래픽, 래스터화된 3‑D 뷰 및 정확한 페이지 레이아웃 정보를 포함할 수 있어 CAD 소프트웨어가 없는 사람과도 쉽게 공유할 수 있습니다.

## PDF 내보내기에 Aspose.CAD를 사용하는 이유

Aspose.CAD를 사용하면 **set PDF page size**를 지정하고 완전 관리형 .NET 코드만으로 PDF를 내보낼 수 있습니다. 50개 이상의 CAD 형식을 지원하고, 전체 문서를 메모리에 로드하지 않고도 2 GB까지 파일을 처리하며, 선 굵기, 색상 및 선택적 3‑D 엔터티 렌더링을 최대 1200 DPI의 래스터화 해상도로 보존합니다. 이 라이브러리는 Windows, Linux, macOS에서 실행되므로 생성된 PDF는 모든 플랫폼에서 작동합니다.

## 사전 요구 사항

- **Aspose.CAD for .NET**가 설치되어 있어야 합니다. [Aspose.CAD for .NET download page](https://releases.aspose.com/cad/net/)에서 다운로드하십시오.  
- 변환하려는 CAD 파일이 들어 있는 폴더(예: `C:\CAD\`).  
- .NET 6.0 이상(또는 .NET Framework 4.7.2).

## 네임스페이스 가져오기

`using` 문은 래스터화 및 PDF 옵션 작업에 필요한 Aspose.CAD 네임스페이스를 가져옵니다.  

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
```

## 단계별 가이드

### CAD를 PDF로 내보낼 때 PDF 페이지 크기를 설정하는 방법?

CAD 파일을 로드하고 `RasterizationOptions`에서 페이지 크기를 구성한 다음, 해당 옵션을 `PdfOptions` 인스턴스에 연결하고 `Save`를 호출합니다. 이 네 단계 흐름을 통해 출력 크기와 품질을 완벽히 제어하면서 코드도 간결하게 유지할 수 있습니다.

### 단계 1: CAD 이미지 로드

`Image` 클래스는 메모리에 로드된 CAD 도면을 나타내며, 래스터화를 위해 준비됩니다.  

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";
using (Image cadImage = Image.Load(sourceFilePath))
{
    // Your code for loading the CAD image goes here
}
```

### 단계 2: 래스터화 옵션 구성 (CAD를 PDF로 저장)

`RasterizationOptions` 클래스는 페이지 크기, DPI 및 3‑D 엔터티 렌더링 여부 등 CAD 데이터를 래스터화하는 방식을 정의합니다.  

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 500;
rasterizationOptions.PageHeight = 500;
// rasterizationOptions.TypeOfEntities = TypeOfEntities.Entities3D;

rasterizationOptions.Layouts = new string[] { "Model" };
```

### 단계 3: PDF 옵션 설정 (CAD에서 PDF 생성)

`PdfOptions` 클래스는 출력 형식 설정을 보관하고 래스터화 옵션을 PDF 생성에 연결합니다.  

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

### 단계 4: PDF로 저장 (3D 모델에서 PDF 생성)

`Image` 객체의 `Save` 메서드는 래스터화된 내용을 지정된 PDF 파일에 기록하여 바로 공유할 수 있는 문서를 생성합니다.  

```csharp
MyDir = MyDir + "Export3DImagestoPDF_out.pdf";
cadImage.Save(MyDir, pdfOptions);
```

## 일반적인 문제 및 해결책

| 문제 | 원인 | 해결책 |
|-------|--------|-----|
| **출력 PDF가 비어 있음** | 레이아웃 이름이 잘못되었거나 `Model` 레이아웃이 없습니다. | `rasterizationOptions.Layouts`가 CAD 파일에 존재하는 레이아웃과 일치하는지 확인하십시오. |
| **해상도 낮음** | 기본 래스터화 DPI가 낮습니다. | 저장하기 전에 `rasterizationOptions.Resolution = 300;`을 설정하십시오. |
| **3‑D 엔터티가 표시되지 않음** | `TypeOfEntities`가 주석 처리되어 있습니다. | `rasterizationOptions.TypeOfEntities = TypeOfEntities.Entities3D;`의 주석을 해제하십시오. |
| **라이선스 예외** | 라이선스 없이 체험판을 사용하고 있습니다. | `License license = new License(); license.SetLicense("Aspose.CAD.lic");`를 사용하여 임시 또는 영구 라이선스를 적용하십시오. |

## 자주 묻는 질문

**Q: Aspose.CAD가 모든 CAD 파일 형식과 호환됩니까?**  
**A:** 예, Aspose.CAD는 DWG, DXF, DGN, STL, IFC 등을 포함한 50개 이상의 입력 및 출력 형식을 지원하므로 모든 프로젝트에 유연성을 제공합니다.

**Q: PDF로 내보낼 때 페이지 크기를 사용자 정의할 수 있나요?**  
**A:** 물론입니다. `Save`를 호출하기 전에 `RasterizationOptions`에서 `PageWidth`와 `PageHeight`를 포인트, 인치 또는 밀리미터 단위의 원하는 크기로 설정하십시오.

**Q: Aspose.CAD에 대한 임시 라이선스를 제공하나요?**  
**A:** 예, [Temporary License](https://purchase.aspose.com/temporary-license/) 페이지에서 Aspose.CAD의 임시 라이선스를 받을 수 있습니다.

**Q: 추가 지원이나 커뮤니티 토론을 어디서 찾을 수 있나요?**  
**A:** 전문가 도움과 동료 간 조언을 위해 [Aspose.CAD Forum](https://forum.aspose.com/c/cad/19)으로 이동하십시오.

**Q: Aspose.CAD의 무료 체험 버전이 있나요?**  
**A:** 예, [free trial](https://releases.aspose.com/)에 접속하여 Aspose.CAD의 기능을 살펴볼 수 있습니다.

## 결론

이제 Aspose.CAD for .NET을 사용하여 **set PDF page size**와 **export PDF from 3D CAD images**를 수행하는 완전한 프로덕션 준비 방법을 갖추었습니다. 래스터화 옵션을 조정하면 해상도, 페이지 레이아웃 및 3‑D 엔터티 렌더링을 세밀하게 조정하여 모든 문서 요구 사항을 충족할 수 있습니다. 다양한 DPI 설정과 페이지 크기를 실험하여 파일 크기와 시각적 품질 사이의 최적 균형을 찾아보세요.

{{< blocks/products/products-backtop-button >}}

## 관련 튜토리얼

- [특정 레이아웃을 PDF로 내보내기 - Aspose.CAD 가이드](/cad/net/advanced-export-techniques/exporting-specific-layouts-to-pdf/)
- [DWG를 PDF 또는 래스터 이미지로 내보내기 - Aspose.CAD 가이드](/cad/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/)
- [Aspose.CAD for .NET에서 DGN을 PDF로 내보내기](/cad/net/cad-export-formats/export-dgn-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

--- 

**마지막 업데이트:** 2026-07-04  
**테스트 환경:** Aspose.CAD 24.11 for .NET  
**작성자:** Aspose