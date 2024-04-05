---
title: PLT 파일을 이미지로 내보내기 - Aspose.CAD Tutorial
linktitle: PLT 파일을 이미지로 내보내기
second_title: Aspose.CAD .NET - CAD 및 BIM 파일 형식
description: Aspose.CAD for .NET을 사용하여 PLT 파일을 이미지로 손쉽게 변환하세요. CAD 파일 조작 요구 사항에 맞는 유연한 옵션과 원활한 통합을 살펴보세요.
type: docs
weight: 10
url: /ko/net/exporting-plt-files/exporting-plt-files-to-image/
---
## 소개

.NET용 Aspose.CAD를 사용하여 PLT 파일을 이미지로 내보내는 방법에 대한 포괄적인 튜토리얼에 오신 것을 환영합니다! PLT 파일을 다양한 이미지 형식으로 원활하게 변환하려는 경우 올바른 위치에 오셨습니다. Aspose.CAD for .NET은 효율적인 CAD 파일 조작을 위한 강력한 기능과 유연성을 제공하며, 이 튜토리얼에서는 프로세스를 단계별로 안내합니다.

## 전제 조건

튜토리얼을 시작하기 전에 다음 전제 조건이 충족되었는지 확인하세요.

-  .NET용 Aspose.CAD: Aspose.CAD 라이브러리가 설치되어 있는지 확인하세요. 다음에서 다운로드할 수 있습니다.[여기](https://releases.aspose.com/cad/net/).

-  문서 디렉터리: 문서 디렉터리를 설정하고 해당 경로를 기록해 둡니다. 이것을 다음과 같이 지칭할 것이다.`MyDir`코드 예제에서.

이제 튜토리얼을 시작해 보겠습니다.

## 네임스페이스 가져오기

Aspose.CAD 기능에 액세스하려면 .NET 프로젝트에서 필요한 네임스페이스를 가져오는 것부터 시작하세요. 코드 시작 부분에 다음 줄을 추가합니다.

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadConsts;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using static Aspose.CAD.Examples.CSharp.DWG_Drawings.SupportMLeaderEntityForDWGFormat;
using Aspose.CAD.ImageOptions;
```

## 1단계: PLT 파일 로드

```csharp
string sourceFilePath = MyDir + "50states.plt";

using (Image cadImage = Image.Load(sourceFilePath))
{
    // 후속 단계에 대한 코드가 여기에 표시됩니다.
}
```

 이 단계에서는 다음을 사용하여 PLT 파일을 로드합니다.`Image.Load` Aspose.CAD에서 제공하는 메소드입니다.

## 2단계: 이미지 내보내기 옵션 구성

```csharp
ImageOptionsBase imageOptions = new JpegOptions();
CadRasterizationOptions options = new CadRasterizationOptions
{
    PageHeight = 500,
    PageWidth = 1000,
    // 필요에 따라 추가 옵션을 추가합니다.
};
imageOptions.VectorRasterizationOptions = options;
```

 여기서는 이미지 내보내기 옵션을 설정합니다. 이 예에서는 JpegOptions를 사용하지만 요구 사항에 따라 다른 형식을 선택할 수도 있습니다. 조정하다`PageHeight` 그리고`PageWidth` 출력 이미지에 필요한 대로.

## 3단계: 이미지 저장

```csharp
cadImage.Save(MyDir + "50states.jpg", imageOptions);
```

 마지막으로 변환된 이미지를 다음을 사용하여 저장합니다.`Save` 방법, 출력 경로와 이전에 구성된 이미지 옵션을 지정합니다.

다른 PLT 파일에 대해 이 단계를 반복하거나 특정 요구 사항에 따라 옵션을 사용자 정의합니다.

## 결론

축하해요! .NET용 Aspose.CAD를 사용하여 PLT 파일을 이미지로 내보내는 방법을 성공적으로 배웠습니다. 이 강력한 라이브러리는 CAD 파일 조작을 위한 유연성과 효율성을 제공하므로 프로젝트에 유용한 도구가 됩니다.

## FAQ

### Q1: PLT 파일을 JPEG 이외의 형식으로 내보낼 수 있습니까?

A1: 물론이죠! PNG, GIF, BMP 등과 같이 Aspose.CAD에서 지원하는 다양한 이미지 형식 중에서 선택할 수 있습니다.

### Q2: 더 많은 제어를 위해 래스터화 옵션을 사용자 정의하려면 어떻게 해야 합니까?

 A2: 간단히 속성을 조정하면 됩니다.`CadRasterizationOptions` 특정 요구 사항에 맞게 출력을 조정하려면 2단계의 클래스를 선택하세요.

### Q3: 평가판을 사용할 수 있나요?

 A3: 예, 무료 평가판을 통해 Aspose.CAD의 기능을 탐색할 수 있습니다.[여기](https://releases.aspose.com/).

### Q4: 자세한 문서는 어디서 찾을 수 있나요?

 A4: 포괄적인 문서를 사용할 수 있습니다.[여기](https://reference.aspose.com/cad/net/).

### Q5: 도움이 필요하거나 질문이 있나요?

 A5: 커뮤니티를 방문하세요[법정](https://forum.aspose.com/c/cad/19) 지원과 토론을 위해.
