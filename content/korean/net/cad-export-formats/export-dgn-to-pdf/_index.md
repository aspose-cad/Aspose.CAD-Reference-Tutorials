---
title: .NET용 Aspose.CAD에서 DGN을 PDF로 내보내기
linktitle: DGN을 PDF로 내보내기
second_title: Aspose.CAD .NET - CAD 및 BIM 파일 형식
description: .NET용 Aspose.CAD를 사용하여 DGN 파일을 PDF로 쉽게 내보내는 방법을 알아보세요. 원활한 CAD 파일 조작을 위한 단계별 가이드입니다.
type: docs
weight: 12
url: /ko/net/cad-export-formats/export-dgn-to-pdf/
---
## 소개

.NET 개발 세계에서 Aspose.CAD는 CAD 파일의 조작 및 변환을 용이하게 하는 강력한 라이브러리입니다. 개발자가 자주 접하는 일반적인 작업 중 하나는 DGN 파일을 PDF 형식으로 내보내는 것입니다. 이 튜토리얼에서는 .NET용 Aspose.CAD를 사용하여 프로세스를 단계별로 안내합니다.

## 전제 조건

튜토리얼을 시작하기 전에 다음 사항이 준비되어 있는지 확인하세요.

- C# 및 .NET 프레임워크에 대한 실무 지식.
-  .NET 라이브러리용 Aspose.CAD가 설치되었습니다. 당신은 그것을 다운로드 할 수 있습니다[여기](https://releases.aspose.com/cad/net/).
- 이 튜토리얼의 샘플 DGN 파일(예: "Nikon_D90_Camera.dgn")입니다.

## 네임스페이스 가져오기

C# 프로젝트에서 필요한 네임스페이스를 가져오는 것부터 시작합니다.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## 1단계: DGN 파일 로드

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (DgnImage cadImage = (DgnImage)Image.Load(sourceFilePath))
{
    // 여기에 귀하의 코드가 있습니다 ...
}
```

## 2단계: 래스터화 옵션 구성

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 600;
rasterizationOptions.PageHeight = 300;
rasterizationOptions.NoScaling = true;
rasterizationOptions.AutomaticLayoutsScaling = false;
```

## 3단계: PDF 옵션 만들기

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## 4단계: PDF로 저장

```csharp
cadImage.Save(MyDir + "ExportDGNToPdf_out.pdf", pdfOptions);
```

## 결론

축하해요! .NET용 Aspose.CAD를 사용하여 DGN 파일을 PDF로 성공적으로 내보냈습니다. 이 튜토리얼에서는 DGN 파일 로드부터 래스터화 옵션 구성 및 출력을 PDF로 저장하는 것까지 필수 단계를 다루었습니다.

## FAQ

### Q1: 사전 CAD 지식 없이도 Aspose.CAD for .NET을 사용할 수 있나요?

A1: 물론이죠! Aspose.CAD는 복잡한 CAD 작업을 단순화하여 다양한 배경을 가진 개발자가 액세스할 수 있도록 해줍니다.

### Q2: Aspose.CAD에 대한 추가 예제와 문서는 어디서 찾을 수 있나요?

 A2: 탐색해 보세요.[선적 서류 비치](https://reference.aspose.com/cad/net/) 포괄적인 가이드와 예시를 보려면

### Q3: Aspose.CAD에 대한 무료 평가판이 있습니까?

A3: 예, 무료 평가판을 받을 수 있습니다.[여기](https://releases.aspose.com/).

### Q4: Aspose.CAD의 임시 라이선스는 어떻게 얻을 수 있나요?

 A4: 임시 라이센스 취득[여기](https://purchase.aspose.com/temporary-license/).

### Q5: 도움이 필요하거나 질문이 있나요?

A5: 다음을 방문하세요.[Aspose.CAD 포럼](https://forum.aspose.com/c/cad/19) 지역 사회 지원을 위해.