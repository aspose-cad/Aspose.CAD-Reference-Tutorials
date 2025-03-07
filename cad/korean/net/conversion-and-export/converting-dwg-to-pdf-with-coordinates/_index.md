---
title: C#에서 좌표를 사용하여 DWG를 PDF로 변환 - Aspose.CAD Tutorial
linktitle: C#에서 좌표를 사용하여 DWG를 PDF로 변환
second_title: Aspose.CAD .NET - CAD 및 BIM 파일 형식
description: Aspose.CAD를 사용하여 C#에서 특정 좌표를 사용하여 DWG를 PDF로 변환하는 방법을 알아보세요. 정확하고 효율적인 CAD 파일 변환을 위한 단계별 가이드를 따르십시오.
weight: 11
url: /ko/net/conversion-and-export/converting-dwg-to-pdf-with-coordinates/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# C#에서 좌표를 사용하여 DWG를 PDF로 변환 - Aspose.CAD Tutorial

## 소개

.NET용 Aspose.CAD를 사용하여 지정된 좌표를 사용하여 DWG 파일을 PDF로 변환하는 방법에 대한 포괄적인 튜토리얼에 오신 것을 환영합니다. Aspose.CAD는 개발자가 .NET 애플리케이션에서 CAD 파일 형식을 원활하게 사용할 수 있게 해주는 강력한 라이브러리입니다. 이 튜토리얼에서는 정밀도를 높이기 위해 특정 좌표를 제공하면서 DWG 파일을 PDF로 변환하는 과정을 안내합니다.

## 전제 조건

시작하기 전에 다음 필수 구성 요소가 있는지 확인하세요.

- Aspose.CAD 라이브러리: .NET용 Aspose.CAD 라이브러리를 다운로드하고 설치합니다. 도서관을 찾으실 수 있습니다[여기](https://releases.aspose.com/cad/net/).

- 개발 환경: Visual Studio 또는 기타 선호하는 IDE를 포함하여 호환 가능한 개발 환경이 설정되어 있는지 확인하세요.

- DWG 파일: 변환할 DWG 파일을 준비합니다. 제공된 예제 파일이나 사용자 정의 DWG 파일을 사용할 수 있습니다.

## 네임스페이스 가져오기

C# 프로젝트에서 필요한 네임스페이스를 가져옵니다.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadParameters;
using Aspose.CAD.FileFormats.Cad.CadTables;
using Aspose.CAD.ImageOptions;
```

더 나은 이해를 위해 코드를 단계별 가이드로 나누어 보겠습니다.

## 1단계: 문서 디렉터리 정의

```csharp
string MyDir = "Your Document Directory";
```

## 2단계: 원본 DWG 파일 경로 설정

```csharp
string sourceFilePath = MyDir + "visualization_-_conference_room.dwg";
```

## 3단계: DWG 파일 로드 및 래스터화 옵션 구성

```csharp
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
    rasterizationOptions.Layouts = new string[] { "Model" };
    rasterizationOptions.NoScaling = true;
```

## 4단계: 좌표 및 뷰포트 정의

```csharp
    Point topLeft = new Point(500, 1000);
    double width = 3108;
    double height = 2489;

    CadVportTableObject newView = new CadVportTableObject();
    newView.Name = new CadStringParameter();
    newView.Name.Init("*Active");
    newView.CenterPoint.X = topLeft.X + width / 2f;
    newView.CenterPoint.Y = topLeft.Y - height / 2f;
    newView.ViewHeight.Value = height;
    newView.ViewAspectRatio.Value = width / height;
```

## 5단계: 뷰포트 설정 적용

```csharp
    for (int i = 0; i < cadImage.ViewPorts.Count; i++)
    {
        CadVportTableObject currentView = (CadVportTableObject)(cadImage.ViewPorts[i]);
        if (cadImage.ViewPorts.Count == 1 || string.Equals(currentView.Name.Value.ToLowerInvariant(), "*active"))
        {
            cadImage.ViewPorts[i] = newView;
            break;
        }
    }
```

## 6단계: PDF 옵션 구성 및 내보내기

```csharp
    Aspose.CAD.ImageOptions.PdfOptions pdfOptions = new Aspose.CAD.ImageOptions.PdfOptions();
    pdfOptions.VectorRasterizationOptions = rasterizationOptions;

    MyDir = MyDir + "ConvertDWGToPDFBySupplyingCoordinates_out.pdf";
    cadImage.Save(MyDir, pdfOptions);
}
```

## 7단계: 성공 메시지 표시

```csharp
Console.WriteLine("\nThe DWG file exported successfully to PDF.\nFile saved at " + MyDir);
```

## 결론

축하해요! .NET용 Aspose.CAD를 사용하여 지정된 좌표를 사용하여 DWG 파일을 PDF로 성공적으로 변환했습니다. 이 튜토리얼에서는 필수 단계를 다루고 개발자를 위한 명확한 가이드를 제공했습니다.

## FAQ

### Q1: Aspose.CAD를 다른 CAD 파일 형식과 함께 사용할 수 있습니까?

A1: 예, Aspose.CAD는 DWG, DXF, DWF 등을 포함한 다양한 CAD 형식을 지원합니다.

### Q2: 변환 과정에서 발생하는 오류는 어떻게 처리하나요?

A2: try-catch 블록을 사용하여 오류 처리 메커니즘을 구현하여 예외를 캡처하고 관리합니다.

### Q3: Aspose.CAD는 Windows와 Linux 환경 모두에 적합합니까?

A3: 예, Aspose.CAD는 Windows 및 Linux 플랫폼과 모두 호환됩니다.

### Q4: PDF 출력을 추가로 사용자 정의할 수 있습니까?

A4: 물론이죠! Aspose.CAD에서 제공하는 광범위한 옵션을 탐색하여 PDF 출력을 특정 요구 사항에 맞게 조정하십시오.

### Q5: 추가 지원이나 커뮤니티 토론은 어디서 찾을 수 있나요?

A5: 다음을 방문하세요.[Aspose.CAD 포럼](https://forum.aspose.com/c/cad/19) 커뮤니티 지원 및 토론을 위해.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
