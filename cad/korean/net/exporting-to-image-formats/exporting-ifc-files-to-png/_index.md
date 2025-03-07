---
title: IFC 파일을 PNG로 내보내기 - Aspose.CAD Tutorial
linktitle: IFC 파일을 PNG로 내보내기
second_title: Aspose.CAD .NET - CAD 및 BIM 파일 형식
description: IFC에서 PNG로의 원활한 변환을 위한 강력한 솔루션인 .NET용 Aspose.CAD를 살펴보세요. 효율적인 CAD 파일 처리를 위해 지금 다운로드하세요.
weight: 10
url: /ko/net/exporting-to-image-formats/exporting-ifc-files-to-png/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# IFC 파일을 PNG로 내보내기 - Aspose.CAD Tutorial

## 소개

CAD(컴퓨터 지원 설계)의 역동적인 세계에서는 효율적인 파일 변환이 매우 중요합니다. .NET용 Aspose.CAD는 IFC(Industry Foundation Classes) 파일을 PNG 형식으로 내보내기 위한 원활한 기능을 제공하는 강력한 도구로 등장합니다. 이 단계별 튜토리얼은 Aspose.CAD를 원활하게 사용하는 과정을 안내합니다.

## 전제 조건

튜토리얼을 시작하기 전에 다음 전제 조건이 충족되었는지 확인하세요.

### 1. Aspose.CAD 설치

 .NET용 Aspose.CAD가 설치되어 있는지 확인하세요. 릴리스 페이지에서 다운로드할 수 있습니다.[여기](https://releases.aspose.com/cad/net/).

### 2. 문서 디렉토리

 문서에 대해 지정된 디렉터리를 만듭니다. 제공된 예에서 변수는`MyDir` 문서 디렉토리를 나타냅니다.

## 네임스페이스 가져오기

이제 필수 구성 요소가 설정되었으므로 Aspose.CAD 기능을 사용하기 위해 .NET 애플리케이션에 필요한 네임스페이스를 가져와 보겠습니다.

```csharp
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using Aspose.CAD.FileFormats.Ifc;
```

## 1단계: IFC 파일 로드

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "example.ifc";
using (IfcImage cadImage = (IfcImage)Image.Load(sourceFilePath))
{
```

 이 단계에서는 Aspose.CAD를 초기화합니다.`IfcImage` 개체를 선택하고 IFC 파일을 해당 개체에 로드합니다.

## 2단계: 래스터화 옵션 설정

```csharp
    CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
   
    rasterizationOptions.PageWidth = 100;
    rasterizationOptions.PageHeight = 100;
```

PNG 출력의 페이지 너비와 높이를 구성하는 래스터화 옵션을 정의합니다.

## 3단계: PNG 옵션 설정

```csharp
    PngOptions pngOptions = new PngOptions();
    pngOptions.VectorRasterizationOptions = rasterizationOptions;
```

PNG 옵션을 생성하고 이전에 정의한 래스터화 옵션을 연결합니다.

## 4단계: 출력 경로 지정

```csharp
    // 출력 경로도 설정
    string outPath = sourceFilePath + ".png";
    cadImage.Save(outPath, pngOptions);
}
```

PNG 파일의 출력 경로를 정의하고 이름이 ".png" 확장자를 가진 소스 파일과 동일한지 확인합니다. 마지막으로 변환된 이미지를 저장합니다.

## 결론

이러한 간단한 단계를 통해 Aspose.CAD for .NET을 사용하여 IFC 파일을 PNG로 성공적으로 내보냈습니다. 이 다목적 도구는 CAD 변환 프로세스를 단순화하여 개발자와 엔지니어가 액세스할 수 있도록 해줍니다.

## FAQ

### Q1: macOS 또는 Linux에서 .NET용 Aspose.CAD를 사용할 수 있습니까?

A1: 아니요, Aspose.CAD for .NET은 Windows 환경을 위해 특별히 설계되었습니다.

### Q2: 테스트 목적으로 임시 라이센스를 사용할 수 있습니까?

 A2: 예, 다음에서 임시 라이센스를 얻을 수 있습니다.[여기](https://purchase.aspose.com/temporary-license/) 평가를 위해.

### Q3: Aspose.CAD에 대한 지원은 어떻게 받을 수 있나요?

 A3: 다음을 방문하세요.[Aspose.CAD 포럼](https://forum.aspose.com/c/cad/19) 커뮤니티 지원 및 토론을 위해.

### Q4: 포괄적인 문서는 어디에서 찾을 수 있습니까?

 A4: 다음을 참조하세요.[Aspose.CAD 문서](https://reference.aspose.com/cad/net/) 자세한 정보와 예시를 확인하세요.

### Q5: 설치 중에 문제가 발생하면 어떻게 됩니까?

 A5: 문서를 확인하거나 관련 도움을 요청하세요.[Aspose.CAD 포럼](https://forum.aspose.com/c/cad/19).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
