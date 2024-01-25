---
title: CAD 도면에 워터마크 추가 - Aspose.CAD 가이드
linktitle: CAD 도면에 워터마크 추가
second_title: Aspose.CAD .NET - CAD 및 BIM 파일 형식
description: .NET용 Aspose.CAD를 사용하여 전문적인 워터마크로 CAD 도면을 향상하세요. 개인화되고 매력적인 디자인을 위한 단계별 가이드를 따르십시오.
type: docs
weight: 11
url: /ko/net/plt-and-watermarking/adding-watermarks-to-cad-drawings/
---
## 소개

전문적인 워터마크를 추가하여 CAD 도면을 향상시키고 싶으십니까? .NET용 Aspose.CAD는 워터마크를 CAD 파일에 원활하게 통합할 수 있는 강력한 솔루션을 제공합니다. 이 단계별 가이드에서는 Aspose.CAD를 사용하여 워터마크를 추가하는 과정을 안내하여 도면에 중요한 정보를 전달할 뿐만 아니라 고유한 마크도 포함되도록 합니다.

## 전제 조건

튜토리얼을 시작하기 전에 다음 사항을 확인하세요.
-  .NET용 Aspose.CAD: Aspose.CAD 라이브러리가 설치되어 있는지 확인하세요. 당신은 그것을 다운로드 할 수 있습니다[여기](https://releases.aspose.com/cad/net/).
- 문서 디렉토리: CAD 도면을 저장할 디렉토리를 설정합니다.
이제 CAD 도면에 워터마크를 추가해 보겠습니다!

## 네임스페이스 가져오기

필요한 네임스페이스를 .NET 프로젝트로 가져오는 것부터 시작하세요.

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## 1단계: CAD 도면 로드

```csharp
// 문서 디렉터리의 경로입니다.
string MyDir = "Your Document Directory";
using (CadImage cadImage = (CadImage)Image.Load(MyDir + "Drawing11.dwg")) {
```

## 2단계: MTEXT로 워터마크 추가

```csharp
// 새 MTEXT 추가
CadMText watermark = new CadMText();
watermark.Text = "Watermark message";
watermark.InitialTextHeight = 40;
watermark.InsertionPoint = new Cad3DPoint(300, 40);
watermark.LayerName = "0";
cadImage.BlockEntities["*Model_Space"].AddEntity(watermark);
```

## 3단계: 또는 워터마크를 텍스트로 추가

```csharp
// 또는 텍스트와 같은 더 간단한 엔터티를 추가하세요.
CadText text = new CadText();
text.DefaultValue = "Watermark text";
text.TextHeight = 40;
text.FirstAlignment = new Cad3DPoint(300, 40);
text.LayerName = "0";
cadImage.BlockEntities["*Model_Space"].AddEntity(text);
```

## 4단계: PDF로 내보내기

```csharp
// 워터마크가 포함된 CAD 도면을 PDF로 내보내기
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
rasterizationOptions.Layouts = new[] { "Model" };
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
cadImage.Save(MyDir + "AddWatermark_out.pdf", pdfOptions);
```

다양한 도면에 대해 이 단계를 반복하면 전문가 수준의 워터마크가 있는 CAD 파일을 즉시 얻을 수 있습니다!

## 결론

축하해요! Aspose.CAD for .NET을 사용하여 CAD 도면에 워터마크를 추가하는 방법을 성공적으로 배웠습니다. 이 간단하면서도 강력한 프로세스를 통해 기술 도면의 무결성을 유지하면서 설계를 개인화할 수 있습니다.

## FAQ

### Q1: 워터마크의 모양을 사용자 정의할 수 있나요?

A1: 예, 원하는 대로 워터마크의 텍스트, 글꼴, 크기 및 위치를 사용자 정의할 수 있습니다.

### Q2: Aspose.CAD는 다른 CAD 파일 형식과 호환됩니까?

A2: Aspose.CAD는 DWG 및 DXF를 포함한 다양한 CAD 파일 형식을 지원하여 광범위한 호환성을 보장합니다.

### Q3: 단일 CAD 도면에 여러 워터마크를 추가할 수 있습니까?

A3: 물론이죠! 필요에 따라 워터마크를 추가할 수 있어 다양한 사용 사례에 유연성을 제공할 수 있습니다.

### Q4: Aspose.CAD는 무료 평가판을 제공합니까?

A4: 예, 무료 평가판을 통해 Aspose.CAD의 기능을 탐색할 수 있습니다. 그것을 얻으십시오[여기](https://releases.aspose.com/).

### Q5: Aspose.CAD에 대한 지원은 어디서 찾을 수 있나요?

 A5: 질문이나 도움이 필요하면 다음을 방문하세요.[Aspose.CAD 포럼](https://forum.aspose.com/c/cad/19).