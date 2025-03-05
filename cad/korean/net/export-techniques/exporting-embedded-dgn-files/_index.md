---
title: 내장된 DGN 파일 내보내기 - Aspose.CAD 튜토리얼
linktitle: 포함된 DGN 파일 내보내기
second_title: Aspose.CAD .NET - CAD 및 BIM 파일 형식
description: .NET용 Aspose.CAD의 강력한 기능을 살펴보세요. 이 단계별 튜토리얼을 통해 포함된 DGN 파일을 PDF로 쉽게 내보내는 방법을 알아보세요.
type: docs
weight: 14
url: /ko/net/export-techniques/exporting-embedded-dgn-files/
---
## 소개

역동적인 소프트웨어 개발 세계에서 .NET용 Aspose.CAD는 CAD(Computer-Aided Design) 파일을 처리하기 위한 강력한 도구로 돋보입니다. 이 튜토리얼은 .NET용 Aspose.CAD를 사용하여 내장된 DGN 파일을 내보내는 과정을 안내합니다. 숙련된 개발자이든 호기심이 많은 초보자이든 이 단계별 가이드는 Aspose.CAD의 기능을 효과적으로 활용하는 데 도움이 될 것입니다.

## 전제 조건

튜토리얼을 시작하기 전에 다음 전제 조건이 충족되었는지 확인하세요.

1.  .NET용 Aspose.CAD: 다음에서 라이브러리를 다운로드하고 설치하세요.[.NET용 Aspose.CAD](https://releases.aspose.com/cad/net/).

2. 개발 환경: Visual Studio 또는 기타 선호하는 IDE를 사용하여 .NET 개발 환경을 설정합니다.

3. 샘플 DXF 파일: 이 튜토리얼에서는 "conic_pyramid.dxf" 파일을 사용합니다. 지정된 문서 디렉토리에서 사용할 수 있는지 확인하십시오.

## 네임스페이스 가져오기

C# 코드에서 필요한 네임스페이스를 가져와야 합니다.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
```

## 1단계: DXF 파일 로드

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    //추가 단계를 위한 코드가 여기에 표시됩니다.
}
```

## 2단계: 래스터화 옵션 설정

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.Layouts = new[] { "Model" };
```

## 3단계: PDF 옵션 설정

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## 4단계: PDF로 저장

```csharp
cadImage.Save(MyDir + "conic_pyramid.pdf", pdfOptions);
```

## 5단계: 성공 메시지 표시

```csharp
Console.WriteLine("\nThe DXF drawing exported successfully to PDF.\nFile saved at " + MyDir);
```

## 결론

축하해요! .NET용 Aspose.CAD를 사용하여 포함된 DGN 파일을 PDF로 성공적으로 내보냈습니다. 이 튜토리얼에서는 필수 단계를 다루며 Aspose.CAD가 제공하는 고급 기능을 탐색할 수 있는 기초를 제공합니다.

## FAQ

### Q1: Aspose.CAD for .NET을 다른 프로그래밍 언어와 함께 사용할 수 있습니까?

A1: Aspose.CAD는 주로 .NET을 지원하지만 Aspose는 Java 및 Python을 포함한 다양한 언어에 대한 라이브러리를 제공합니다.

### Q2: Aspose.CAD for .NET에 대한 무료 평가판이 있습니까?

 A2: 예, 다음에서 무료 평가판을 받을 수 있습니다.[여기](https://releases.aspose.com/).

### Q3: Aspose.CAD for .NET에 대한 포괄적인 문서는 어디에서 찾을 수 있습니까?

 A3: 설명서를 참조하세요[여기](https://reference.aspose.com/cad/net/).

### Q4: Aspose.CAD for .NET에 대한 임시 라이선스는 어떻게 얻나요?

 A4: 임시 라이센스 취득[여기](https://purchase.aspose.com/temporary-license/).

### Q5: 도움이 필요하거나 커뮤니티에 참여하고 싶으십니까?

A5: 다음을 방문하세요.[Aspose.CAD 포럼](https://forum.aspose.com/c/cad/19) 지원과 토론을 위해.