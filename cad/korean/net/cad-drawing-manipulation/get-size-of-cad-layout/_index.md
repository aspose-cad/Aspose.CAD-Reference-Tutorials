---
title: .NET용 Aspose.CAD에서 CAD 레이아웃 크기 가져오기
linktitle: CAD 레이아웃 크기 가져오기
second_title: Aspose.CAD .NET - CAD 및 BIM 파일 형식
description: Aspose.CAD를 사용하여 .NET에서 CAD 레이아웃 크기를 검색하는 방법을 알아보세요. 효율적인 CAD 파일 조작을 위한 단계별 가이드를 따르십시오.
weight: 14
url: /ko/net/cad-drawing-manipulation/get-size-of-cad-layout/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# .NET용 Aspose.CAD에서 CAD 레이아웃 크기 가져오기

## 소개

.NET용 Aspose.CAD를 사용하여 CAD 레이아웃의 크기를 얻는 방법에 대한 포괄적인 가이드에 오신 것을 환영합니다. Aspose.CAD는 개발자가 CAD 파일을 원활하게 사용할 수 있게 해주는 강력한 라이브러리입니다. 이 튜토리얼에서는 실제 예제와 단계별 지침을 사용하여 CAD 레이아웃의 크기를 검색하는 과정을 안내합니다.

## 전제 조건

튜토리얼을 시작하기 전에 다음 전제 조건이 충족되었는지 확인하세요.

-  .NET용 Aspose.CAD: Aspose.CAD 라이브러리가 설치되어 있는지 확인하세요. 다음에서 다운로드할 수 있습니다.[.NET용 Aspose.CAD 다운로드 페이지](https://releases.aspose.com/cad/net/).

- 문서 파일: 작업하려는 CAD 파일을 준비합니다. 이 튜토리얼에서는 "conic_pyramid.dxf" 및 "Bottom_plate.dwg"를 예로 사용합니다.

이제 시작해보자!

## 네임스페이스 가져오기

.NET 프로젝트에서 필요한 네임스페이스를 가져오는 것부터 시작하세요.

```csharp
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadConsts;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.FileFormats.Cad.CadTables;
using Aspose.CAD.ImageOptions;
```

## 1단계: 문서 디렉터리 설정

 문서 디렉터리의 경로를 설정합니다. 바꾸다`"Your Document Directory"` 실제 경로와 함께.

```csharp
string MyDir = "Your Document Directory";
```

## 2단계: CAD 파일 경로 지정

분석하려는 CAD 파일 경로 배열을 정의합니다. 이 예에서는 "conic_pyramid.dxf"와 "Bottom_plate.dwg"를 사용합니다.

```csharp
string[] sourceFilePaths = new[]
{
    MyDir + "conic_pyramid.dxf",
    MyDir + "Bottom_plate.dwg"
};
```

## 3단계: CAD 파일 반복

각 CAD 파일을 반복하고 레이아웃 정보를 검색합니다.

```csharp
foreach (var sourceFilePath in sourceFilePaths)
{
    string extension = Path.GetExtension(sourceFilePath);
    using (CadImage cadImage = (CadImage)Aspose.CAD.Image.Load(sourceFilePath))
    {
        // ...(다음 단계로 계속)
    }
}
```

## 4단계: 비어 있지 않은 레이아웃 가져오기

CAD 파일 형식을 기반으로 비어 있지 않은 레이아웃을 가져오는 도우미 메서드를 정의합니다.

```csharp
private static List<string> GetNotEmptyLayouts(Image cadImage, string extension)
{
    // ...(다음 단계로 계속)
}
```

## 5단계: DWG 파일의 레이아웃 가져오기

DWG 파일에 대해 비어 있지 않은 레이아웃을 검색하는 논리를 구현합니다.

```csharp
private static List<string> GetNotEmptyLayoutsForDwg(CadImage cadImage)
{
    // ...(다음 단계로 계속)
}
```

## 6단계: DXF 파일의 레이아웃 가져오기

DXF 파일에 대해 비어 있지 않은 레이아웃을 검색하는 논리를 구현합니다.

```csharp
private static List<string> GetNotEmptyLayoutsForDxf(CadImage cadImage)
{
    // ...(다음 단계로 계속)
}
```

## 7단계: 레이아웃 크기 검색 및 이미지로 저장

레이아웃 크기를 가져와 이미지로 저장하는 과정을 완료합니다.

```csharp
foreach (string layout in layouts)
{
    // ...(다음 단계로 계속)
}
```

## 결론

축하해요! .NET용 Aspose.CAD를 사용하여 CAD 레이아웃의 크기를 얻는 방법을 성공적으로 배웠습니다. 이 튜토리얼에서는 프로젝트 설정부터 레이아웃 정보 검색 및 이미지로 저장까지 필수 단계를 다루었습니다. 이제 효율적인 CAD 파일 조작을 위해 이 지식을 .NET 애플리케이션에 통합할 수 있습니다.

## FAQ

### Q1: Aspose.CAD는 모든 CAD 파일 형식과 호환됩니까?

A1: 예, Aspose.CAD는 DWG 및 DXF를 포함한 다양한 CAD 파일 형식을 지원합니다.

### Q2: 이미지 저장 옵션을 사용자 정의할 수 있나요?

A2: 물론이죠! 특정 요구 사항에 맞게 형식, 해상도 등의 이미지 옵션을 조정할 수 있습니다.

### Q3: 추가 문서는 어디서 찾을 수 있나요?

 A3: 다음을 참조하세요.[Aspose.CAD 문서](https://reference.aspose.com/cad/net/) 자세한 정보와 예시를 확인하세요.

### Q4: 무료 평가판이 제공됩니까?

 A4: 예, Aspose.CAD를 탐색할 수 있습니다.[무료 시험판](https://releases.aspose.com/).

### Q5; 기술지원은 어떻게 받을 수 있나요?

 A5: 기술 지원을 받으려면[Aspose.CAD 포럼](https://forum.aspose.com/c/cad/19).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
