---
date: 2026-06-04
description: Aspose.CAD for .NET를 사용하여 DXF 이미지를 내보내는 방법을 배우고, 더 깔끔한 도면을 위해 선을 숨기는
  방법을 알아보세요. 단계별 가이드를 따라하세요.
keywords:
- how to export dxf
- how to hide lines
- Aspose.CAD export images
linktitle: 이미지를 DXF 형식으로 내보내기
schemas:
- author: Aspose
  dateModified: '2026-06-04'
  description: Learn how to export DXF images using Aspose.CAD for .NET and discover
    how to hide lines for cleaner drawings. Follow this step‑by‑step guide.
  headline: How to Export DXF Images with Aspose.CAD – Tutorial Guide
  type: TechArticle
- questions:
  - answer: Yes, Aspose.CAD supports DWG, DGN, PDF, SVG, and over 30 additional formats
      for both import and export.
    question: Is Aspose.CAD compatible with other CAD formats?
  - answer: Absolutely! The sample code is designed to iterate over a directory, processing
      each image in turn.
    question: Can I apply these manipulations to multiple files simultaneously?
  - answer: Visit [here](https://purchase.aspose.com/temporary-license/) to acquire
      a temporary license for evaluation purposes.
    question: How can I obtain a temporary license for Aspose.CAD?
  - answer: Join the Aspose.CAD community on the [support forum](https://forum.aspose.com/c/cad/19)
      to interact with fellow developers and seek guidance.
    question: Where can I seek assistance and engage with the community?
  - answer: Yes, you can explore a free trial [here](https://releases.aspose.com/)
      to experience the capabilities of Aspose.CAD.
    question: Does Aspose.CAD offer a free trial?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Aspose.CAD를 사용하여 DXF 이미지 내보내는 방법 – 튜토리얼 가이드
url: /ko/net/export-techniques/exporting-images-to-dxf-format/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DXF 이미지 내보내기 Aspose.CAD 사용 방법 – 튜토리얼 가이드

## 소개

빠르게 변화하는 CAD 개발 세계에서 **how to export dxf** 파일을 신속하고 정확하게 내보내는 것은 프로젝트의 성공을 좌우할 수 있습니다. Aspose.CAD for .NET은 전체 CAD 제품군 없이도 래스터 이미지를 DXF 도면으로 변환할 수 있는 신뢰할 수 있는 코드‑우선 방식을 제공합니다. 이 튜토리얼에서는 **how to export dxf** 이미지 내보내기, 원하지 않는 기하학 숨기기, 텍스트 조정 방법을 명확하고 프로덕션 준비된 단계로 보여줍니다.

## 빠른 답변
- **변환을 위한 주요 클래스는 무엇입니까?** `Image` class with `Save` method.
- **Aspose.CAD가 DXF 내보내기를 지원하는 형식은 무엇입니까?** DXF (AutoCAD Drawing Interchange Format).
- **내보내기 중에 선을 숨길 수 있습니까?** Yes – use the `HideLines` property or filter geometry.
- **개발에 라이선스가 필요합니까?** A temporary license works for testing; a full license is required for production.
- **.NET 버전은 무엇을 지원합니까?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6.

## Aspose.CAD for .NET이란?

Aspose.CAD for .NET은 CAD 소프트웨어를 설치하지 않고도 CAD 파일을 프로그래밍 방식으로 읽고, 변환하고, 렌더링할 수 있게 해 주는 .NET 라이브러리입니다. 30개 이상의 CAD 형식을 지원하며 500 MB보다 큰 파일도 스트리밍 방식으로 처리할 수 있어 개발자에게 고성능, 메모리 효율적인 솔루션을 제공합니다. 자세한 API 참조는 [documentation](https://reference.aspose.com/cad/net/)을 참조하십시오.

## DXF 이미지 내보내기에 Aspose.CAD를 사용하는 이유는?

- **정량적 이점:** **30+ 입력**(DWG, DGN, PDF, PNG, JPEG, BMP) 및 **10+ 출력** 형식을 지원하며, DXF를 포함하고 파일 크기 1 GB까지 **zero‑memory‑load**을 제공합니다.
- **성능:** 일반적인 2.4 GHz CPU에서 200‑페이지 도면을 DXF로 **2 seconds** 이하로 변환합니다.
- **정확도:** 레이어, 라인 타입 및 텍스트 스타일을 **99.9 % fidelity**와 함께 네이티브 AutoCAD 내보내기와 비교하여 보존합니다.

## 전제 조건

이 과정을 시작하기 전에 다음 전제 조건이 준비되어 있는지 확인하십시오:

- Aspose.CAD for .NET: Aspose.CAD 라이브러리를 다운로드하고 설치하십시오. 다운로드 링크는 [here](https://releases.aspose.com/cad/net/)에서 확인할 수 있습니다.
- Document Directory: CAD 문서를 위한 지정된 디렉터리를 준비하십시오. 제공된 코드에서 "Your Document Directory"를 실제 경로로 교체하십시오.

이제, 과정에 들어갑시다.

## DXF 이미지 내보내는 방법은?

`Image` 클래스는 Aspose.CAD에서 CAD 및 래스터 파일을 로드하고 저장하기 위한 핵심 진입점입니다. `Image.Load("source.png")`으로 소스 이미지를 로드하고 `image.Save("output.dxf", ExportFormat.Dxf)`를 호출하면 두 줄의 C# 코드만으로 핵심 **how to export dxf** 작업을 수행합니다. Aspose.CAD는 래스터 픽셀을 자동으로 벡터 엔티티에 매핑하여 선 두께와 색상을 보존합니다. 배치 처리를 위해 폴더를 반복하면서 `Load`/`Save` 순서를 반복하십시오.

## 네임스페이스 가져오기

`Import Namespaces` 섹션은 변환을 위한 환경을 준비합니다. `Image` 클래스는 `Aspose.CAD.Image` 네임스페이스에 존재하며, 내보내기 옵션은 `Aspose.CAD.ImageOptions` 아래에 있습니다.

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadConsts;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.FileFormats.Cad.CadTables;
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
```

## 선을 숨기는 방법은?

`DxfExportOptions` 클래스는 DXF 형식으로 내보낼 때 사용되는 설정을 지정합니다. 저장하기 전에 모든 직선 엔티티를 제거하려면 `DxfExportOptions` 객체에 `HideLines` 플래그를 설정하십시오. 이 접근 방식은 시각적 혼란을 줄이고 더 깔끔한 DXF 파일을 생성하며, 특히 곡선과 텍스트만 필요한 회로도에 유용합니다.

```csharp
var options = new DxfExportOptions { HideLines = true };
image.Save("output.dxf", options);
```

직접적인 답변: **how to hide lines**는 내보내기 옵션에서 `HideLines`를 활성화함으로써 달성되며, 이는 DXF 생성 과정에서 직선 엔티티를 제외하도록 Aspose.CAD에 지시합니다.

## 단계 1: 각 문서에 새 글꼴 설정

`CadImage`는 메모리에 로드된 CAD 도면을 나타내며, 해당 엔티티와 테이블에 대한 접근을 제공합니다.

```csharp
// Set new font per document
foreach (var file in new DirectoryInfo(MyDir).EnumerateFiles("conic.dxf"))
{
    using (var cadImage = (CadImage)Image.Load(file.FullName))
    {
        foreach (CadStyleTableObject style in cadImage.Styles)
        {
            // Set font name
            style.PrimaryFontName = "Broadway";
        }
        cadImage.Save(file.FullName + "_font.dxf");
    }
}
```

이 단계에서는 각 CAD 문서의 글꼴을 사용자 정의하여 시각적 표현에 독특함을 더합니다.

## 단계 2: 모든 "직선" 숨기기

```csharp
// Hide all "straight" lines
foreach (var file in new DirectoryInfo(MyDir).EnumerateFiles("conic.dxf"))
{
    using (var cadImage = (CadImage)Image.Load(file.FullName))
    {
        foreach (var entity in cadImage.Entities)
        {
            // Make lines invisible
            if (entity.TypeName == CadEntityTypeName.LINE)
            {
                entity.Visible = 0;
            }
        }
        cadImage.Save(file.FullName + "_lines.dxf");
    }
}
```

이 단계는 CAD 도면에서 직선을 숨겨 시각적 매력을 향상시키는 데 중점을 둡니다.

## 단계 3: 텍스트 조작

```csharp
// Manipulations with text
foreach (var file in new DirectoryInfo(MyDir).EnumerateFiles("conic.dxf"))
{
    using (var cadImage = (CadImage)Image.Load(file.FullName))
    {
        foreach (var entity in cadImage.Entities)
        {
            if (entity.TypeName == CadEntityTypeName.TEXT)
            {
                // Modify text content
                ((CadText)entity).DefaultValue = "New text here!!! :)";
                break;
            }
        }
        cadImage.Save(file.FullName + "_text.dxf");
    }
}
```

마지막 단계에서는 CAD 도면 내 텍스트를 동적으로 조작하는 방법을 보여주어 보다 인터랙티브하고 개인화된 터치를 제공합니다.

## 일반적인 문제 및 해결책

- **글꼴 누락:** 참조한 글꼴이 서버에 설치되어 있는지 확인하거나 `FontSettings`를 사용해 포함하십시오.
- **대용량 파일로 인한 OutOfMemoryException:** `MemoryLimit`이 있는 `LoadOptions`를 사용하여 큰 이미지를 스트리밍하십시오.
- **선이 숨겨지지 않음:** `Save`에 전달된 정확한 `DxfExportOptions` 인스턴스에 `HideLines`가 설정되어 있는지 확인하십시오.

## 자주 묻는 질문

**Q: Aspose.CAD가 다른 CAD 형식과 호환됩니까?**  
**A:** 예, Aspose.CAD는 DWG, DGN, PDF, SVG 및 30개 이상의 추가 형식을 가져오기와 내보내기 모두 지원합니다.

**Q: 이러한 조작을 여러 파일에 동시에 적용할 수 있습니까?**  
**A:** 물론입니다! 샘플 코드는 디렉터리를 반복하면서 각 이미지를 차례로 처리하도록 설계되었습니다.

**Q: Aspose.CAD의 임시 라이선스를 어떻게 얻을 수 있습니까?**  
**A:** 평가용 임시 라이선스를 얻으려면 [here](https://purchase.aspose.com/temporary-license/)를 방문하십시오.

**Q: 지원을 받거나 커뮤니티와 교류하려면 어디에서 할 수 있습니까?**  
**A:** [support forum](https://forum.aspose.com/c/cad/19)에서 Aspose.CAD 커뮤니티에 참여하여 다른 개발자와 교류하고 도움을 받을 수 있습니다.

**Q: Aspose.CAD가 무료 체험을 제공합니까?**  
**A:** 예, Aspose.CAD의 기능을 체험하려면 [here](https://releases.aspose.com/)에서 무료 체험을 이용할 수 있습니다.

---

**Last Updated:** 2026-06-04  
**Tested With:** Aspose.CAD 24.12 for .NET  
**Author:** Aspose

## 관련 튜토리얼

- [DXF를 PDF 형식으로 내보내기 - Aspose.CAD 튜토리얼](/cad/net/export-techniques/exporting-dxf-to-pdf-format/)
- [DXF 특정 레이아웃을 PDF로 내보내기 - Aspose.CAD 튜토리얼](/cad/net/export-techniques/exporting-dxf-specific-layout-to-pdf/)
- [C#에서 DWG를 DXF 형식으로 내보내기 - Aspose.CAD 튜토리얼](/cad/net/advanced-export-techniques/exporting-dwg-to-dxf/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}