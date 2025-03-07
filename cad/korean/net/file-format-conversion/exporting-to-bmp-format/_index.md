---
title: BMP 형식으로 내보내기 - Aspose.CAD 튜토리얼
linktitle: BMP 형식으로 내보내기
second_title: Aspose.CAD .NET - CAD 및 BIM 파일 형식
description: .NET용 Aspose.CAD를 사용하여 BMP로 3D 이미지를 원활하게 내보내는 세계를 탐험해보세요. 번거롭지 않은 경험을 위해 튜토리얼을 따르십시오.
weight: 11
url: /ko/net/file-format-conversion/exporting-to-bmp-format/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# BMP 형식으로 내보내기 - Aspose.CAD 튜토리얼

## 소개

역동적인 소프트웨어 개발 세계에서 .NET용 Aspose.CAD는 CAD(Computer-Aided Design) 파일을 처리하기 위한 강력한 도구로 돋보입니다. CAD 이미지를 널리 사용되는 BMP 형식으로 내보내려는 경우 이 튜토리얼이 가장 적합한 가이드입니다. 이 단계별 연습에서는 .NET용 Aspose.CAD를 사용하여 3D 이미지를 BMP로 내보내는 과정을 살펴보겠습니다. 뛰어들어보자!

## 전제 조건

이 튜토리얼을 시작하기 전에 다음 전제 조건이 충족되었는지 확인하세요.

-  .NET용 Aspose.CAD: 다음에서 Aspose.CAD 라이브러리를 다운로드하고 설치하세요.[여기](https://releases.aspose.com/cad/net/).
- 개발 환경: .NET 개발 환경을 설정합니다.
- CAD 파일: 내보낼 CAD 파일을 준비합니다. 이 예에서는 "18-12-11 9644 - site.dwf"를 사용합니다.

## 네임스페이스 가져오기

.NET 프로젝트에서 필요한 네임스페이스를 가져와야 합니다.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
```

## 1단계: CAD 이미지 로드

CAD 이미지를 프로젝트에 로드하는 것부터 시작하세요. "문서 디렉토리"를 실제 디렉토리 경로로 바꾸십시오.

```csharp
string MyDir = "Your Document Directory";
string inputFile = MyDir + "18-12-11 9644 - site.dwf";

using (Image image = Image.Load(inputFile))
{
    // 이미지를 로드하기 위한 코드는 여기에 있습니다.
}
```

## 2단계: BMP 내보내기 옵션 구성

CAD 파일의 벡터 래스터화 옵션을 포함하여 BMP 내보내기 옵션을 설정합니다.

```csharp
BmpOptions bmpOptions = new BmpOptions();
var dwfRasterizationOptions = new CadRasterizationOptions();
bmpOptions.VectorRasterizationOptions = dwfRasterizationOptions;

dwfRasterizationOptions.PageHeight = 500;
dwfRasterizationOptions.PageWidth = 500;
```

## 3단계: BMP로 내보내기

BMP 파일의 출력 경로를 지정하여 내보내기 프로세스를 실행합니다.

```csharp
string outPath = MyDir + "18-12-11 9644 - site.bmp";
image.Save(outPath, bmpOptions);
```

## 결론

축하해요! .NET용 Aspose.CAD를 사용하여 3D 이미지를 BMP로 성공적으로 내보냈습니다. 이 튜토리얼에서는 Aspose.CAD의 다양성을 엿볼 수 있어 복잡한 작업도 쉽게 할 수 있습니다.

## FAQ

### Q1: Aspose.CAD for .NET을 모든 CAD 파일 형식과 함께 사용할 수 있습니까?

A1: 예, Aspose.CAD는 다양한 CAD 파일 형식을 지원하여 프로젝트에 유연성을 제공합니다.

### Q2: 테스트 목적으로 임시 라이센스를 사용할 수 있습니까?

 A2: 물론이죠! 임시면허를 취득할 수 있습니다.[여기](https://purchase.aspose.com/temporary-license/) 평가를 위해.

### Q3: Aspose.CAD에 대한 포괄적인 문서는 어디서 찾을 수 있나요?

 A3: 설명서를 참조하세요[여기](https://reference.aspose.com/cad/net/) 자세한 정보와 예시를 확인하세요.

### 질문4: 어떻게 지원을 구하거나 커뮤니티와 연결됩니까?

 A4: Aspose.CAD 포럼을 방문하세요.[여기](https://forum.aspose.com/c/cad/19) 질문을 하고 커뮤니티에 참여합니다.

### Q5: .NET용 Aspose.CAD를 구입할 수 있나요?

 A5: 예, Aspose.CAD를 구입할 수 있습니다.[여기](https://purchase.aspose.com/buy) 귀하의 프로젝트에 대한 잠재력을 최대한 발휘할 수 있습니다.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
