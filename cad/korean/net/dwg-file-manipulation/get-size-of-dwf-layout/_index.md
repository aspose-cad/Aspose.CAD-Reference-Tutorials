---
title: C#에서 DWG 파일 작업 - DWF 레이아웃 크기 가져오기
linktitle: C#에서 DWG 파일 작업 - DWF 레이아웃 크기 가져오기
second_title: Aspose.CAD .NET - CAD 및 BIM 파일 형식
description: DWG 파일 처리에 있어 .NET용 Aspose.CAD의 강력한 기능을 살펴보세요. C#을 사용하여 DWF 레이아웃 크기를 쉽게 추출하는 방법을 알아보세요.
weight: 10
url: /ko/net/dwg-file-manipulation/get-size-of-dwf-layout/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# C#에서 DWG 파일 작업 - DWF 레이아웃 크기 가져오기

## 소개

CAD(Computer-Aided Design) 및 .NET 개발 영역에서 Aspose.CAD는 DWG 파일을 처리하는 강력한 도구입니다. 이 튜토리얼에서는 C#에서 DWG 파일을 사용하여 작업하고 DWF 레이아웃의 크기를 추출하는 과정을 안내합니다. 코드를 살펴보기 전에 이 여정을 시작하기 위한 모든 설정이 완료되었는지 확인하겠습니다.

## 전제 조건

이 튜토리얼을 원활하게 따르려면 다음 전제 조건이 갖추어져 있는지 확인하십시오.

-  .NET용 Aspose.CAD: .NET용 Aspose.CAD가 설치되어 있는지 확인하세요. 다음에서 다운로드할 수 있습니다.[.NET용 Aspose.CAD 다운로드 페이지](https://releases.aspose.com/cad/net/).

이제 필요한 도구가 준비되었으므로 코딩 영역으로 뛰어들어 보겠습니다.

## 네임스페이스 가져오기

코드 작업을 시작하기 전에 필수 네임스페이스를 가져오겠습니다.

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Dwf;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
```

이러한 네임스페이스는 C# 애플리케이션에서 Aspose.CAD를 사용하여 CAD 파일을 처리하기 위한 필수 클래스와 메서드를 제공합니다.

## 1단계: 환경 설정

프로젝트에 적합한 환경이 설정되었는지 확인하는 것부터 시작하세요. C# 프로젝트에서 Aspose.CAD 라이브러리를 참조하세요.

## 2단계: 파일 경로 정의

DWG 파일의 경로와 생성된 JPG 파일의 출력 디렉터리를 정의합니다.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "blocks_and_tables.dwf";
```

## 3단계: DWF 이미지 로드

Aspose.CAD를 사용하여 DWF 이미지를 로드합니다.

```csharp
using (DwfImage image = (DwfImage)Aspose.CAD.Image.Load(sourceFilePath))
{
    // 추가 단계에 대한 코드는 여기에 표시됩니다.
}
```

## 4단계: 페이지 반복

DWF 이미지의 페이지를 반복합니다.

```csharp
foreach (var page in image.Pages)
{
    // 추가 단계에 대한 코드는 여기에 표시됩니다.
}
```

## 5단계: 레이아웃 정보 가져오기

각 페이지에서 레이아웃 정보를 가져옵니다.

```csharp
var layout = page.Name;
System.Console.WriteLine("Layout= " + layout);
```

## 6단계: JPG 옵션 설정

레이아웃을 JPG 파일로 저장하기 위한 옵션을 설정합니다.

```csharp
using (FileStream fs = new FileStream(MyDir + "layout_" + layout + ".jpg", FileMode.Create))
{
    JpegOptions jpegOptions = new JpegOptions();
    CadRasterizationOptions options = new CadRasterizationOptions();
    options.Layouts = new string[] { layout };
    // 추가 단계에 대한 코드는 여기에 표시됩니다.
}
```

## 7단계: 페이지 크기 결정

DWF 레이아웃의 크기를 결정합니다.

```csharp
double sizeExtX = page.MaxPoint.X - page.MinPoint.X;
double sizeExtY = page.MaxPoint.Y - page.MinPoint.Y;
// 추가 단계에 대한 코드는 여기에 표시됩니다.
```

## 8단계: 페이지 크기 설정

단위 유형에 따라 페이지 크기를 설정합니다.

```csharp
if (page.UnitType == UnitType.Inch)
{
    options.PageHeight = CommonHelper.INtoPixels(sizeExtY, CommonHelper.DPI);
    options.PageWidth = CommonHelper.INtoPixels(sizeExtX, CommonHelper.DPI);
}
else if (page.UnitType == UnitType.Millimeter)
{
    options.PageHeight = CommonHelper.MMtoPixels(sizeExtY, CommonHelper.DPI);
    options.PageWidth = CommonHelper.MMtoPixels(sizeExtX, CommonHelper.DPI);
}
else
{
    options.PageHeight = (float)sizeExtY;
    options.PageWidth = (float)sizeExtX;
}
```

## 9단계: JPG 파일 저장

지정된 옵션을 사용하여 JPG 파일을 저장합니다.

```csharp
jpegOptions.VectorRasterizationOptions = options;
image.Save(fs, jpegOptions);
}
```

이제 C#에서 Aspose.CAD를 사용하여 DWG 파일에서 DWF 레이아웃 크기를 성공적으로 추출했습니다. Aspose.CAD가 .NET 개발을 위해 제공하는 더 많은 특징과 기능을 자유롭게 탐색해 보세요.

## 결론

이 튜토리얼에서는 Aspose.CAD를 사용하여 C#에서 DWG 파일로 작업하는 과정을 살펴보았습니다. 이러한 단계를 수행하면 DWF 레이아웃의 크기를 얻을 수 있을 뿐만 아니라 .NET 프로젝트의 다양한 CAD 관련 작업에 Aspose.CAD의 기능을 활용할 수도 있습니다.

## FAQ

### Q1: Aspose.CAD는 최신 DWG 파일 형식과 호환됩니까?

 A1: Aspose.CAD는 최신 버전을 포함하여 다양한 DWG 파일 형식을 지원합니다. 다음을 참조하세요.[선적 서류 비치](https://reference.aspose.com/cad/net/) 구체적인 호환성 세부정보를 확인하세요.

### Q2: Aspose.CAD를 상업용 프로젝트와 개인 프로젝트 모두에 사용할 수 있나요?

 A2: 예, Aspose.CAD는 상업용 및 개인용 모두에 유연한 라이센스 옵션을 제공합니다. 방문하다[구매 페이지](https://purchase.aspose.com/buy) 상세 사항은.

### Q3: Aspose.CAD의 임시 라이선스는 어떻게 얻을 수 있나요?

 A3: 다음에서 임시 라이센스를 받을 수 있습니다.[여기](https://purchase.aspose.com/temporary-license/) 평가 목적으로.

### Q4: Aspose.CAD에 대한 지원은 어디서 찾을 수 있나요?

답변 4: 질문이나 도움이 필요하면 다음을 방문하세요.[Aspose.CAD 포럼](https://forum.aspose.com/c/cad/19).

### Q5: Aspose.CAD에 대한 무료 평가판이 있습니까?

 A5: 예, Aspose.CAD 무료 평가판에 액세스할 수 있습니다.[여기](https://releases.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
