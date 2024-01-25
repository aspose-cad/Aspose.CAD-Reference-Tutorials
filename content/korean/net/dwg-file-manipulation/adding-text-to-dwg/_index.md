---
title: C#에서 DWG 파일에 텍스트 추가 - Aspose.CAD Tutorial
linktitle: C#에서 DWG 파일에 텍스트 추가
second_title: Aspose.CAD .NET - CAD 및 BIM 파일 형식
description: C# 및 Aspose.CAD를 사용하여 DWG 파일에 텍스트를 추가하는 방법을 알아보세요. 원활한 통합을 위해 이 단계별 튜토리얼을 따르세요. 포괄적인 지침을 보려면 Aspose.CAD 문서를 살펴보세요.
type: docs
weight: 14
url: /ko/net/dwg-file-manipulation/adding-text-to-dwg/
---
## 소개

CAD(컴퓨터 지원 설계) 및 .NET 개발의 동적 영역에서 Aspose.CAD는 DWG 파일을 조작하기 위한 강력한 도구로 돋보입니다. DWG 파일에 텍스트를 추가하는 것은 일반적인 요구 사항이며, 이 튜토리얼에서는 C# 및 Aspose.CAD를 사용하여 이를 달성하는 방법을 살펴보겠습니다.

## 전제 조건

튜토리얼을 시작하기 전에 다음 사항이 준비되어 있는지 확인하세요.

-  Aspose.CAD 라이브러리: Aspose.CAD 라이브러리를 다운로드하여 설치합니다.[다운로드 링크](https://releases.aspose.com/cad/net/).

-  문서 디렉터리: 문서 디렉터리를 설정하고 해당 경로를 다음과 같이 기록해 둡니다.`MyDir`.

이제 프로세스를 관리 가능한 단계로 나누어 보겠습니다.

## 네임스페이스 가져오기

C# 코드에 Aspose.CAD 기능에 액세스하는 데 필요한 네임스페이스를 포함합니다.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.FileFormats.Cad.CadConsts;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadObjects.AttEntities;
using Aspose.CAD.ImageOptions;
```

## 1단계: DWG 파일 로드

 DWG 파일을`Image` Aspose.CAD 라이브러리를 사용하는 객체입니다.

```csharp
string dwgPathToFile = MyDir + "SimpleEntites.dwg";
using (Image image = Image.Load(dwgPathToFile))
{
    // 후속 단계에 대한 코드가 여기에 표시됩니다.
}
```

## 2단계: CadText 객체 생성

 인스턴스화`CadText` DWG 파일에 추가할 텍스트를 나타내는 객체입니다.

```csharp
CadText cadText = new CadText();
cadText.StyleType = "Standard";
cadText.DefaultValue = "Some custom text";
cadText.ColorId = 256;
cadText.LayerName = "0";
cadText.FirstAlignment.X = 47.90;
cadText.FirstAlignment.Y = 5.56;
cadText.TextHeight = 0.8;
cadText.ScaleX = 0.0;
```

## 3단계: DWG에 텍스트 추가

 생성된 것을 추가하세요.`CadText` Aspose.CAD를 사용하여 DWG 파일에 객체를 추가합니다.

```csharp
CadImage cadImage = (CadImage)image;
cadImage.BlockEntities["*Model_Space"].AddEntity(cadText);
```

## 4단계: PDF 옵션 구성

수정된 DWG 파일을 PDF로 저장하기 위한 PDF 옵션을 구성합니다.

```csharp
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.VectorRasterizationOptions = cadRasterizationOptions;
cadRasterizationOptions.DrawType = CadDrawTypeMode.UseObjectColor;
cadRasterizationOptions.PageHeight = 1600;
cadRasterizationOptions.PageWidth = 1600;
cadRasterizationOptions.Layouts = new string[] { "Model" };
```

## 5단계: PDF로 저장

수정된 DWG 파일을 텍스트가 추가된 PDF로 저장합니다.

```csharp
image.Save(MyDir + "SimpleEntites_generated.pdf", pdfOptions);
```

이제 C# 및 Aspose.CAD를 사용하여 DWG 파일에 텍스트를 성공적으로 추가했습니다. CAD 조작 요구 사항에 맞게 Aspose.CAD의 더 많은 특징과 기능을 자유롭게 탐색해 보세요.

## 결론

이 튜토리얼에서는 C# 및 Aspose.CAD를 사용하여 DWG 파일에 텍스트를 추가하는 필수 단계를 다루었습니다. 이 강력한 조합은 동적이며 사용자 정의된 CAD 문서 생성 가능성을 열어줍니다.

## FAQ

### Q1: Aspose.CAD는 모든 버전의 DWG 파일과 호환됩니까?

A1: Aspose.CAD는 광범위한 DWG 파일 버전을 지원하여 다양한 CAD 소프트웨어와의 호환성을 보장합니다.

### Q2: Aspose.CAD를 사용하여 단일 DWG 파일에 여러 텍스트 엔터티를 추가할 수 있습니까?

A2: 예, 튜토리얼에 설명된 프로세스를 반복하여 DWG 파일에 여러 텍스트 엔터티를 추가할 수 있습니다.

### Q3: Aspose.CAD에서 텍스트 글꼴과 스타일을 어떻게 변경할 수 있나요?

 A3: 텍스트 글꼴과 스타일을 수정하려면`CadText` 객체를 DWG 파일에 추가하기 전에

### Q4: Aspose.CAD를 상업용 프로젝트에 사용할 때 라이센스 고려 사항이 있습니까?

 A4: 예, Aspose.CAD 라이선스 조건을 준수하는지 확인하세요. 인용하다[Aspose.CAD 구매](https://purchase.aspose.com/buy) 자세한 내용은.

### Q5: Aspose.CAD 관련 문의는 어디서 도움을 받거나 논의할 수 있나요?

A5: 다음을 방문하세요.[Aspose.CAD 포럼](https://forum.aspose.com/c/cad/19)커뮤니티와 연결하고 지원을 받으세요.