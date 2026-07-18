---
date: 2026-07-18
description: Aspose.CAD for .NET를 사용하여 CAD를 PNG로 내보내는 방법. IFC 파일을 고품질 PNG 이미지로 빠르고
  안정적으로 변환합니다.
keywords:
- how to export cad to png
- Aspose.CAD IFC conversion
- CAD to PNG .NET
lastmod: 2026-07-18
linktitle: IFC 파일을 PNG로 내보내기
og_description: Aspose.CAD for .NET를 사용하여 CAD를 PNG로 내보내는 방법. 코드 없이 설정하는 단계별 IFC 파일을
  PNG 이미지로 변환하는 방법을 배웁니다.
og_image_alt: Guide showing IFC to PNG conversion with Aspose.CAD for .NET
og_title: CAD를 PNG로 내보내는 방법 – Aspose.CAD .NET 가이드
schemas:
- author: Aspose
  dateModified: '2026-07-18'
  description: How to export CAD to PNG using Aspose.CAD for .NET. Convert IFC files
    to high‑quality PNG images quickly and reliably.
  headline: How to Export CAD to PNG – Exporting IFC Files with Aspose.CAD
  type: TechArticle
- questions:
  - answer: No, Aspose.CAD for .NET is specifically designed for Windows environments.
    question: Can I use Aspose.CAD for .NET on macOS or Linux?
  - answer: Yes, you can obtain a temporary license from [here](https://purchase.aspose.com/temporary-license/)
      for evaluation.
    question: Is a temporary license available for testing purposes?
  - answer: Visit the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) for community
      support and discussions.
    question: How can I get support for Aspose.CAD?
  - answer: Refer to the [Aspose.CAD documentation](https://reference.aspose.com/cad/net/)
      for detailed information and examples.
    question: Where can I find comprehensive documentation?
  - answer: Check the documentation or seek assistance on the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19).
    question: What if I encounter issues during installation?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- export cad
- Aspose.CAD
- IFC to PNG
- .NET image conversion
title: CAD를 PNG로 내보내는 방법 – Aspose.CAD를 사용한 IFC 파일 내보내기
url: /ko/net/exporting-to-image-formats/exporting-ifc-files-to-png/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# CAD를 PNG로 내보내는 방법 – Aspose.CAD로 IFC 파일 내보내기

## 소개

**how to export cad to png**가 필요하다면, Aspose.CAD for .NET은 IFC(Industry Foundation Classes) 모델을 선명한 PNG 래스터 이미지로 변환하는 신뢰할 수 있는 코드 없는 방법을 제공합니다. 이 튜토리얼에서는 라이브러리 설치부터 최종 PNG 저장까지 전체 워크플로를 단계별로 안내하므로, 어떤 .NET 애플리케이션에도 자신 있게 변환을 통합할 수 있습니다.

## 빠른 답변
- **변환을 처리하는 라이브러리는 무엇입니까?** Aspose.CAD for .NET.
- **지원되는 소스 형식?** IFC (Industry Foundation Classes) files.
- **대상 이미지 형식?** PNG, 크기와 해상도를 완전히 제어할 수 있습니다.
- **최소 .NET 버전?** .NET Framework 4.5+ 또는 .NET Core 3.1+.
- **라이선스 요구 사항?** 프로덕션 사용을 위한 유효한 Aspose.CAD 라이선스.

## “how to export cad to png”란 무엇입니까?

이 용어는 IFC와 같은 CAD 기반 파일 형식을 Portable Network Graphics(PNG) 래스터 이미지로 변환하는 과정을 의미합니다. 이 변환을 통해 CAD 시각 자료를 웹 페이지, 문서 또는 보고서에 쉽게 조회, 공유 및 삽입할 수 있으며, 가볍고 널리 지원되는 형식으로 시각적 정확성을 유지하면서 특수 CAD 뷰어가 필요하지 않습니다.

## 이 변환에 Aspose.CAD를 사용하는 이유는?

Aspose.CAD는 **50+ CAD 및 BIM 형식**을 지원하며 전체 파일을 메모리에 로드하지 않고도 수백 페이지에 달하는 IFC 모델을 처리할 수 있습니다. 표준 서버 하드웨어에서 빠르고 메모리 효율적인 변환을 제공하며, 레이어, 선 두께 및 색상 매핑을 자동으로 처리하고 출력 품질 및 크기에 대한 광범위한 구성 옵션을 제공합니다.

## 전제 조건

### 1. Aspose.CAD 설치
Ensure that you have Aspose.CAD for .NET installed. You can download it from the release page [here](https://releases.aspose.com/cad/net/).

### 2. 문서 디렉터리
Create a designated directory for your documents. In the provided example, the variable `MyDir` represents the document directory.

## 네임스페이스 가져오기
Now that the prerequisites are ready, import the namespaces required to work with Aspose.CAD in your .NET project.

```csharp
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using Aspose.CAD.FileFormats.Ifc;
```

## CAD를 PNG로 내보내는 방법은?

`IfcImage`는 PNG와 같은 래스터 형식으로 래스터화할 수 있는 IFC CAD 이미지를 나타냅니다. `new IfcImage("source.ifc")`로 IFC 파일을 로드하고, `RasterizationOptions`를 통해 래스터화 옵션을 구성한 뒤, `PngOptions`로 PNG 전용 설정을 지정하고, 마지막으로 `Save(outputPath, pngOptions)`를 호출합니다. 이 엔드‑투‑엔드 흐름은 몇 줄의 코드만으로 CAD 모델을 고해상도 PNG로 변환하며, 레이어, 색상 및 선 두께를 자동으로 처리합니다.

## 단계 1: IFC 파일 로드
The `IfcImage` class loads an IFC model and prepares it for rasterization.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "example.ifc";
using (IfcImage cadImage = (IfcImage)Image.Load(sourceFilePath))
{
```

이 단계에서는 Aspose.CAD `IfcImage` 객체를 초기화하고 IFC 파일을 로드합니다.

## 단계 2: 래스터화 옵션 설정
The `RasterizationOptions` class defines how vector data is converted into raster images, including page width, height, and background color.

```csharp
    CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
   
    rasterizationOptions.PageWidth = 100;
    rasterizationOptions.PageHeight = 100;
```

PNG 출력용 페이지 너비와 높이를 구성하기 위해 래스터화 옵션을 정의합니다.

## 단계 3: PNG 옵션 설정
The `PngOptions` class holds settings specific to PNG output, such as compression level and colour depth.

```csharp
    PngOptions pngOptions = new PngOptions();
    pngOptions.VectorRasterizationOptions = rasterizationOptions;
```

PNG 옵션을 생성하고 앞서 정의한 래스터화 옵션과 연결합니다.

## 단계 4: 출력 경로 지정
The output path determines where the generated PNG file will be saved.

```csharp
    // Set output path as well
    string outPath = sourceFilePath + ".png";
    cadImage.Save(outPath, pngOptions);
}
```

PNG 파일의 출력 경로를 정의하고, 소스 파일과 동일한 이름에 ".png" 확장자를 갖도록 합니다. 마지막으로 변환된 이미지를 저장합니다.

## 일반적인 문제 및 해결책
- **Missing fonts or line styles:** 소스 IFC가 모든 필요한 리소스를 참조하는지 확인하십시오; Aspose.CAD는 가능한 경우 누락된 자산을 삽입합니다.
- **Large files cause memory spikes:** 메모리 사용량을 제한하려면 `RasterizationOptions`의 `MemoryLimit` 속성을 사용하십시오.
- **Incorrect colours:** 소스 IFC 색상 정의가 IFC 스키마를 준수하는지 확인하십시오; Aspose.CAD는 표준 색상 매핑을 따릅니다.

## 자주 묻는 질문

**Q: Aspose.CAD for .NET를 macOS 또는 Linux에서 사용할 수 있나요?**  
A: 아니요, Aspose.CAD for .NET은 Windows 환경 전용으로 설계되었습니다.

**Q: 테스트용 임시 라이선스를 사용할 수 있나요?**  
A: 예, 평가를 위해 [here](https://purchase.aspose.com/temporary-license/)에서 임시 라이선스를 얻을 수 있습니다.

**Q: Aspose.CAD 지원을 어떻게 받을 수 있나요?**  
A: 커뮤니티 지원 및 토론을 위해 [Aspose.CAD forum](https://forum.aspose.com/c/cad/19)을 방문하십시오.

**Q: 포괄적인 문서는 어디에서 찾을 수 있나요?**  
A: 자세한 정보와 예제는 [Aspose.CAD documentation](https://reference.aspose.com/cad/net/)을 참조하십시오.

**Q: 설치 중 문제가 발생하면 어떻게 해야 하나요?**  
A: 문서를 확인하거나 [Aspose.CAD forum](https://forum.aspose.com/c/cad/19)에서 도움을 요청하십시오.

---

**Last Updated:** 2026-07-18  
**Tested With:** Aspose.CAD 24.11 for .NET  
**Author:** Aspose

## 관련 튜토리얼

- [Aspose.CAD for .NET에서 CAD 도면을 래스터 이미지로 변환](/cad/net/cad-drawing-manipulation/convert-cad-drawing-to-raster-image/)
- [Aspose.CAD for .NET으로 STL을 PNG로 쉽게 변환](/cad/net/stl-file-export/exporting-stl-files-to-png/)
- [Aspose.CAD for .NET에서 CAD 레이아웃을 래스터 이미지 형식으로 내보내기](/cad/net/cad-export-formats/export-cad-layouts-to-raster-image-formats/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}