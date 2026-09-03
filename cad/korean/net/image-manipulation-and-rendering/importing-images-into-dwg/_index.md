---
date: 2026-08-17
description: .NET용 C#와 Aspose.CAD를 사용하여 dwg 파일에 이미지를 추가하는 방법을 배웁니다. 이 가이드는 이미지 가져오기,
  삽입 위치 설정 및 PDF로 내보내는 과정을 단계별로 안내합니다.
keywords:
- add image to dwg
- convert dwg to pdf
- set insertion point dwg
- embed png in dwg
- save dwg as pdf
lastmod: 2026-08-17
linktitle: C#를 사용한 DWG 파일에 이미지 가져오기
og_description: C#를 사용하여 dwg 파일에 이미지를 추가하는 방법을 배웁니다. 이 튜토리얼은 이미지 가져오기, 삽입 위치 설정 및
  Aspose.CAD를 이용한 dwg를 pdf로 변환하는 내용을 다룹니다.
og_image_alt: Guide showing C# code to embed an image into a DWG file using Aspose.CAD
og_title: C#와 Aspose.CAD를 사용하여 dwg 파일에 이미지를 추가하는 방법
schemas:
- author: Aspose
  dateModified: '2026-08-17'
  description: Learn how to add image to dwg files using C# and Aspose.CAD for .NET.
    This guide walks you through importing images, setting insertion points, and exporting
    to PDF.
  headline: How to add image to dwg files with C# using Aspose.CAD
  type: TechArticle
- description: Learn how to add image to dwg files using C# and Aspose.CAD for .NET.
    This guide walks you through importing images, setting insertion points, and exporting
    to PDF.
  name: How to add image to dwg files with C# using Aspose.CAD
  steps:
  - name: set up your document directory
    text: Prepare the folder that contains the source DWG and the image you want to
      embed.
  - name: load the dwg file
    text: The `CadImage` class represents a DWG drawing and provides access to its
      entities, layers, and metadata.
  - name: define the image properties
    text: Create an `Image` object that points to the raster file (e.g., PNG) and
      specify its format.
  - name: set insertion point dwg and vectors
    text: Specify where the image should appear inside the drawing and how it should
      be scaled. The insertion point is defined by a 2‑D coordinate, while the vectors
      control width and height.
  - name: create and configure the raster image
    text: Instantiate a `RasterImage` object, assign the image data, and set any additional
      rendering options.
  - name: add image to dwg file
    text: Insert the configured raster image into the DWG’s entities collection so
      it becomes part of the drawing.
  - name: save as pdf (export dwg to pdf)
    text: After embedding the image you can **convert dwg to pdf** or **save dwg as
      pdf** with a single call. This is useful for sharing the drawing with stakeholders
      who don’t have CAD software.
  type: HowTo
- questions:
  - answer: The core library is .NET‑specific, but Aspose offers equivalent APIs for
      Java, Python and other platforms.
    question: Can I use Aspose.CAD for .NET with other programming languages?
  - answer: Yes, you can explore a free trial on the [Aspose free trial page](https://releases.aspose.com/).
    question: Is a free trial available for Aspose.CAD?
  - answer: The documentation is available in the [Aspose.CAD .NET API reference](https://reference.aspose.com/cad/net/).
    question: Where can I find detailed documentation for Aspose.CAD?
  - answer: Visit the [temporary license page](https://purchase.aspose.com/temporary-license/)
      to get a temporary license.
    question: How do I obtain a temporary license for Aspose.CAD?
  - answer: Yes, you can seek support and engage with the community in the [Aspose.CAD
      community forum](https://forum.aspose.com/c/cad/19).
    question: Are there community forums for Aspose.CAD support?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- CAD
- Aspose.CAD
- C# image processing
- DWG manipulation
title: C#와 Aspose.CAD를 사용하여 dwg 파일에 이미지를 추가하는 방법
url: /ko/net/image-manipulation-and-rendering/importing-images-into-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# C#와 Aspose.CAD를 사용하여 dwg 파일에 이미지를 추가하는 방법

## 소개

DWG 파일에 이미지를 추가하는 것은 로고, 사진 또는 래스터 그래픽으로 CAD 도면을 풍부하게 만들고자 할 때 흔히 필요한 작업입니다. 이 튜토리얼에서는 C#와 Aspose.CAD for .NET을 사용하여 **dwg에 이미지를 추가**하는 방법을 단계별로 배우고, 필요에 따라 결과를 PDF로 변환하는 방법도 살펴봅니다. 각 섹션을 복사‑붙여넣기만 하면 자신의 프로젝트에 바로 적용할 수 있습니다.

## 빠른 답변
- **어떤 라이브러리가 작업을 처리합니까?** Aspose.CAD for .NET.
- **PNG 파일을 삽입할 수 있나요?** 예 – PNG, JPEG, BMP 및 기타 래스터 형식을 지원합니다.
- **개발에 라이선스가 필요합니까?** 무료 체험판으로 테스트가 가능하며, 상용 라이선스는 프로덕션에 필요합니다.
- **PDF 내보내기가 지원됩니까?** 물론입니다 – 업데이트된 DWG를 한 줄로 PDF로 변환할 수 있습니다.
- **어떤 .NET 버전과 호환됩니까?** .NET Framework 4.6+, .NET Core 3.1+, .NET 5/6/7.

## DWG 파일이란?

DWG 파일은 Autodesk AutoCAD 도면의 고유 이진 형식으로, 벡터 기하, 레이어 및 메타데이터를 저장합니다. 건축, 엔지니어링, 건설 분야에서 널리 사용되며, Aspose.CAD는 AutoCAD가 설치되지 않아도 이 형식을 읽고 쓸 수 있습니다.

## Aspose.CAD로 dwg에 이미지를 추가하는 이유

Aspose.CAD는 **50개 이상의 입력 및 출력 형식**을 지원하고, 전체 문서를 메모리에 로드하지 않아도 500 MB 이상의 파일을 처리할 수 있으며, 헤드리스 서버 환경에서도 동작하는 결정적인 API를 제공합니다. 이를 통해 DWG 도면을 대량으로 빠르고 안정적으로 처리할 수 있습니다.

## 사전 요구 사항
- C# 프로그래밍에 대한 기본 지식.
- Aspose.CAD for .NET이 설치되어 있어야 합니다. [Aspose.CAD for .NET 다운로드 페이지](https://releases.aspose.com/cad/net/)에서 다운로드할 수 있습니다. 또한 다른 Aspose 제품은 [Aspose 릴리스 페이지](https://releases.aspose.com/)에서 확인할 수 있습니다.
- Visual Studio 2022 이상과 같은 개발 환경.

## Aspose.CAD를 사용하여 dwg에 이미지를 추가하는 방법?

대상 DWG를 로드하고, 삽입하려는 사진을 설명하는 래스터 이미지 객체를 만든 뒤, 삽입 지점과 스케일 벡터를 설정하고 이미지를 도면에 첨부합니다. 마지막으로 수정된 DWG를 저장하거나 바로 PDF로 내보낼 수 있습니다. 전체 워크플로는 몇 번의 API 호출만으로 완료되며 일반적인 2페이지 도면은 1초 미만에 처리됩니다.

### 네임스페이스 가져오기
필요한 CAD 클래스를 노출하는 네임스페이스를 포함합니다.

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

### 단계 1: 문서 디렉터리 설정
소스 DWG와 삽입하려는 이미지가 들어 있는 폴더를 준비합니다.

```csharp
string MyDir = "Your Document Directory";
```

### 단계 2: dwg 파일 로드
`CadImage` 클래스는 DWG 도면을 나타내며 엔터티, 레이어 및 메타데이터에 접근할 수 있게 해줍니다.

```csharp
string dwgPathToFile = MyDir + "Drawing11.dwg";
CadImage cadImage1 = (CadImage)Image.Load(dwgPathToFile);
```

### 단계 3: 이미지 속성 정의
래스터 파일(예: PNG)을 가리키는 `Image` 객체를 생성하고 형식을 지정합니다.

```csharp
CadRasterImageDef cadRasterImageDef = new CadRasterImageDef("road-sign-custom.png", 640, 562);
cadRasterImageDef.ObjectHandle = "A3B4";
```

### 단계 4: 삽입 지점 및 벡터 설정
이미지가 도면 내 어디에 표시될지와 크기 조정 방법을 지정합니다. 삽입 지점은 2‑D 좌표로 정의되고, 벡터는 너비와 높이를 제어합니다.

```csharp
Cad3DPoint insertionPoint = new Cad3DPoint(26.77, 22.35);
Cad3DPoint uVector = new Cad3DPoint(0.0061565450840500831, 0);
Cad3DPoint vVector = new Cad3DPoint(0, 0.0061565450840500822);
```

### 단계 5: 래스터 이미지 생성 및 구성
`RasterImage` 객체를 인스턴스화하고 이미지 데이터를 할당한 뒤 추가 렌더링 옵션을 설정합니다.

```csharp
CadRasterImage cadRasterImage = new CadRasterImage(cadRasterImageDef, insertionPoint, uVector, vVector);
cadRasterImage.ImageDefReference = "A3B4";
cadRasterImage.DisplayFlags = 7;
cadRasterImage.ClippingState = 0;
cadRasterImage.ClipBoundaryVertexList.Add(new Cad2DPoint(-0.5, 0.5));
cadRasterImage.ClipBoundaryVertexList.Add(new Cad2DPoint(639.5, 561.5));
```

### 단계 6: dwg 파일에 이미지 추가
구성된 래스터 이미지를 DWG의 엔터티 컬렉션에 삽입하여 도면의 일부가 되게 합니다.

```csharp
CadImage cadImage = (CadImage)cadImage1;
cadImage.BlockEntities["*Model_Space"].AddEntity(cadRasterImage);

List<CadBaseObject> list = new List<CadBaseObject>(cadImage.Objects);
list.Add(cadRasterImageDef);
cadImage.Objects = list.ToArray();
```

### 단계 7: pdf로 저장 (dwg를 pdf로 내보내기)
이미지를 삽입한 후 **dwg를 pdf로 변환**하거나 **dwg를 pdf로 저장**하는 호출을 한 번만 하면 됩니다. 이는 CAD 소프트웨어가 없는 이해관계자와 도면을 공유할 때 유용합니다.

```csharp
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.VectorRasterizationOptions = cadRasterizationOptions;
cadRasterizationOptions.DrawType = CadDrawTypeMode.UseObjectColor;

cadRasterizationOptions.PageHeight = 1600;
cadRasterizationOptions.PageWidth = 1600;
cadRasterizationOptions.Layouts = new string[] { "Model" };
cadImage1.Save(MyDir + "export2.pdf", pdfOptions);
```

## 이미지를 삽입한 후 dwg를 pdf로 변환하는 방법?

`CadImage` 인스턴스의 `Save` 메서드를 호출하고 `SaveFormat.Pdf`와 선택적으로 `PdfOptions` 객체를 전달하여 페이지 크기, 래스터화 및 메타데이터를 제어합니다. Aspose.CAD는 삽입된 래스터 이미지, 레이어 및 선 굵기를 그대로 유지하면서 모든 뷰어에서 열 수 있는 정확한 PDF를 생성합니다. 이 변환은 한 줄의 코드로 수행됩니다.

## 일반적인 문제 및 해결책
- **이미지가 잘못된 위치에 표시됩니다** – 삽입 지점 좌표와 방향 벡터를 다시 확인하십시오; 이는 도면의 원점에 상대적입니다.
- **큰 이미지가 메모리 급증을 일으킵니다** – 삽입 전에 래스터 이미지에 `Resize` 옵션을 사용하거나 낮은 해상도 복사본을 사용하십시오.
- **PDF 내보내기 시 벡터 품질이 손실됩니다** – 벡터 데이터를 유지하는 `PdfOptions`로 저장하고 있는지 확인하십시오; 래스터 이미지는 그대로 삽입됩니다.

## 자주 묻는 질문

**Q: Aspose.CAD for .NET를 다른 프로그래밍 언어와 함께 사용할 수 있나요?**  
A: 핵심 라이브러리는 .NET 전용이지만, Aspose는 Java, Python 및 기타 플랫폼용 동등한 API를 제공합니다.

**Q: Aspose.CAD에 대한 무료 체험판이 제공되나요?**  
A: 예, [Aspose 무료 체험 페이지](https://releases.aspose.com/)에서 무료 체험판을 확인할 수 있습니다.

**Q: Aspose.CAD에 대한 자세한 문서는 어디에서 찾을 수 있나요?**  
A: 문서는 [Aspose.CAD .NET API reference](https://reference.aspose.com/cad/net/)에서 확인할 수 있습니다.

**Q: Aspose.CAD 임시 라이선스는 어떻게 얻나요?**  
A: [임시 라이선스 페이지](https://purchase.aspose.com/temporary-license/)에서 임시 라이선스를 받을 수 있습니다.

**Q: Aspose.CAD 지원을 위한 커뮤니티 포럼이 있나요?**  
A: 예, [Aspose.CAD 커뮤니티 포럼](https://forum.aspose.com/c/cad/19)에서 지원을 요청하고 커뮤니티와 소통할 수 있습니다.

---

**마지막 업데이트:** 2026-08-17  
**테스트 환경:** Aspose.CAD 24.11 for .NET  
**작성자:** Aspose

## 관련 튜토리얼

- [DWG를 PDF 또는 래스터 이미지로 내보내기 - Aspose.CAD 가이드](/cad/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/)
- [C#에서 DWG를 DXF 형식으로 내보내기 - Aspose.CAD 튜토리얼](/cad/net/advanced-export-techniques/exporting-dwg-to-dxf/)
- [특정 레이아웃을 PDF로 내보내기 - Aspose.CAD 가이드](/cad/net/advanced-export-techniques/exporting-specific-layouts-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}