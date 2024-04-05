---
title: C#을 사용하여 DWG 파일의 레이어 처리 - Aspose.CAD Tutorial
linktitle: C#을 사용하여 DWG 파일의 레이어 처리
second_title: Aspose.CAD .NET - CAD 및 BIM 파일 형식
description: .NET용 Aspose.CAD와 C#을 사용하여 DWG 파일의 레이어를 처리하는 방법을 알아보세요. 효율적인 CAD 파일 조작을 위한 단계별 가이드입니다.
type: docs
weight: 11
url: /ko/net/dwg-file-manipulation/support-of-layers/
---
## 소개

.NET용 Aspose.CAD와 C#을 사용하여 DWG 파일의 레이어를 처리하는 방법에 대한 심층 튜토리얼에 오신 것을 환영합니다. Aspose.CAD는 개발자가 CAD 파일 형식을 원활하게 사용할 수 있게 해주는 강력한 라이브러리입니다. 이 튜토리얼에서는 DWG 파일의 레이어를 처리하는 과정을 단계별로 안내합니다.

## 전제 조건

튜토리얼을 시작하기 전에 다음 전제 조건이 충족되었는지 확인하세요.

- C# 프로그래밍 언어에 대한 기본 지식.
- 컴퓨터에 Visual Studio가 설치되어 있습니다.
-  .NET 라이브러리용 Aspose.CAD는 다음에서 다운로드할 수 있습니다.[Aspose.CAD 웹사이트](https://releases.aspose.com/cad/net/).

## 네임스페이스 가져오기

시작하려면 필요한 네임스페이스를 C# 프로젝트로 가져옵니다. 이러한 네임스페이스는 CAD 파일 작업에 필요한 기능을 제공합니다.

```csharp
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
```

## 1단계: DWG 파일 로드

Aspose.CAD 라이브러리를 사용하여 DWG 파일을 C# 애플리케이션에 로드하는 것부터 시작하세요.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "for_layers_test.dwf";

using (Aspose.CAD.Image image = Aspose.CAD.Image.Load(sourceFilePath))
{
    // 후속 단계에 대한 코드가 여기에 표시됩니다.
}
```

## 2단계: 래스터화 옵션 구성

 인스턴스 만들기`CadRasterizationOptions` DWG 파일을 래스터화하는 방법을 정의하기 위해 해당 속성을 설정합니다.

```csharp
Aspose.CAD.ImageOptions.CadRasterizationOptions rasterizationOptions = new Aspose.CAD.ImageOptions.CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
```

## 3단계: 레이어 지정

래스터화 옵션에 원하는 레이어를 추가합니다. 이 예에서는 "LayerA"를 추가했습니다.

```csharp
rasterizationOptions.Layers = new string[] { "LayerA" };
```

## 4단계: 이미지 내보내기 옵션 구성

 필요한 이미지 내보내기 옵션을 만듭니다. 여기에서 우리는`JpegOptions` JPEG로 내보내기 위한 것입니다.

```csharp
JpegOptions jpegOptions = new JpegOptions();
jpegOptions.VectorRasterizationOptions = rasterizationOptions;
```

## 5단계: 내보낸 이미지 저장

출력 경로를 지정하고 래스터화된 DWG 파일을 JPEG로 저장합니다.

```csharp
MyDir = MyDir + "for_layers_test.jpg";
image.Save(MyDir, jpegOptions);
```

이제 .NET용 Aspose.CAD와 함께 C#을 사용하여 DWG 파일의 레이어를 성공적으로 처리했습니다.

## 결론

이 튜토리얼에서는 C#과 Aspose.CAD 라이브러리를 사용하여 DWG 파일의 레이어를 처리하는 과정을 살펴보았습니다. 다음 단계를 수행하면 .NET 응용 프로그램에서 CAD 파일을 효율적으로 사용할 수 있습니다.

## FAQ

### Q1: 여러 레이어를 동시에 처리할 수 있나요?

 A1: 네, 가능합니다. 간단히 레이어 이름을`rasterizationOptions.Layers` 정렬.

### Q2: Aspose.CAD 평가판을 사용할 수 있나요?

 A2: 예, 다음 사이트에서 무료 평가판을 받을 수 있습니다.[여기](https://releases.aspose.com/).

### Q3: 문서는 어디서 찾을 수 있나요?

 A3: 문서를 사용할 수 있습니다.[여기](https://reference.aspose.com/cad/net/).

### Q4: Aspose.CAD에 대한 지원은 어떻게 받나요?

 답변 4: 다음에서 지원을 요청할 수 있습니다.[Aspose.CAD 포럼](https://forum.aspose.com/c/cad/19).

### Q5: Aspose.CAD의 라이선스 옵션은 무엇입니까?

 A5: 라이선스 옵션과 구매 세부정보를 살펴볼 수 있습니다.[여기](https://purchase.aspose.com/buy).