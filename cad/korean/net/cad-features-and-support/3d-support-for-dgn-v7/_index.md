---
title: .NET용 Aspose.CAD에서 DGN V7에 대한 3D 지원
linktitle: DGN V7에 대한 3D 지원
second_title: Aspose.CAD .NET - CAD 및 BIM 파일 형식
description: .NET용 Aspose.CAD에서 DGN V7 파일에 대한 3D 지원 기능을 살펴보세요. CAD 파일을 손쉽게 통합하고 조작하려면 단계별 가이드를 따르십시오.
weight: 10
url: /ko/net/cad-features-and-support/3d-support-for-dgn-v7/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# .NET용 Aspose.CAD에서 DGN V7에 대한 3D 지원

## 소개

소프트웨어 개발의 역동적인 세계에서는 3D 데이터를 원활하게 통합하고 조작하는 능력을 갖는 것이 중요합니다. .NET용 Aspose.CAD는 개발자에게 CAD 파일을 효율적으로 처리할 수 있는 강력한 도구 세트를 제공합니다. 이 튜토리얼에서는 .NET용 Aspose.CAD를 사용하여 DGN V7 파일에 대한 3D 지원을 활성화하는 복잡한 과정을 살펴보겠습니다.

## 전제 조건

이 여정을 시작하기 전에 다음과 같은 전제 조건이 갖추어져 있는지 확인하세요.

-  .NET용 Aspose.CAD: 라이브러리가 설치되어 있는지 확인하세요. 다음에서 다운로드할 수 있습니다.[.NET용 Aspose.CAD 다운로드 페이지](https://releases.aspose.com/cad/net/).

- 유효한 DGN 파일: 제공된 코드 조각을 사용하여 처리할 유효한 DGN 파일을 준비합니다. 직접 사용하거나 테스트 목적으로 다운로드할 수 있습니다.

- .NET 개발 환경: 제공된 코드를 실행하기 위해 .NET 개발 환경을 설정합니다. 없는 경우 다음의 설치 지침을 따를 수 있습니다.[.NET 문서](https://docs.microsoft.com/en-us/dotnet/core/install/).

## 네임스페이스 가져오기

시작하려면 .NET 프로젝트에서 필요한 네임스페이스를 가져옵니다.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

이제 제공된 코드 조각을 단계별 가이드로 분석해 보겠습니다.

## 1단계: 환경 설정

문서 디렉터리와 DGN 파일 경로를 정의합니다.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";
```

## 2단계: DGN 파일 로드

 DGN 파일을 다음과 같이 로드합니다.`DgnImage` Aspose.CAD를 사용하여`Image.Load` 방법:

```csharp
using (DgnImage dgnImage = (DgnImage)Image.Load(sourceFilePath))
{
    // 코드 조각이 계속됩니다...
}
```

## 3단계: 내보내기 옵션 구성

벡터 래스터화 설정을 지정하여 내보내기 옵션을 설정합니다.

```csharp
var options = new PdfOptions
{
    VectorRasterizationOptions = new CadRasterizationOptions
    {
        PageWidth = 1500,
        PageHeight = 1500,
        CenterDrawing = true,
        AutomaticLayoutsScaling = true,
        BackgroundColor = Color.Black,
        Layouts = new string[] { "1", "2", "3", "9" } // 특정 보기 내보내기
    }
};
```

## 4단계: 결과 저장

 활용`Save` DGN 파일을 래스터 이미지로 내보내는 방법:

```csharp
string outFile = "Your Output Directory"; // 출력 디렉터리 지정
dgnImage.Save(outFile, options);
```

## 결론

축하해요! .NET용 Aspose.CAD를 사용하여 DGN V7 파일에 대한 3D 지원을 성공적으로 해제했습니다. 이 튜토리얼에서는 원활한 구현을 보장하기 위해 각 단계를 안내하는 명확한 로드맵을 제공했습니다.

## FAQ

### Q1: 이 접근 방식을 사용하여 여러 DGN 파일을 동시에 처리할 수 있습니까?

A1: 예, 루프 내에서 또는 일괄 처리 시스템의 일부로 여러 파일을 처리하도록 코드를 수정할 수 있습니다.

### Q2: Aspose.CAD for .NET은 어떤 다른 내보내기 형식을 지원합니까?

 A2: .NET용 Aspose.CAD는 PDF, PNG, JPG 등을 포함한 다양한 내보내기 형식을 지원합니다. 다음을 참조하세요.[선적 서류 비치](https://reference.aspose.com/cad/net/) 자세한 내용은.

### Q3: Aspose.CAD for .NET은 최신 .NET Core 버전과 호환됩니까?

A3: 예, .NET용 Aspose.CAD는 최신 .NET Core 버전과 호환되도록 설계되었습니다. 사용자 환경에 적절한 버전이 설치되어 있는지 확인하십시오.

### Q4: 특정 요구 사항에 맞게 내보내기 설정을 추가로 사용자 정의할 수 있습니까?

 A4: 물론이죠! 제공된 코드는 시작점을 제공합니다. 다음에서 추가 옵션과 구성을 탐색할 수 있습니다.[Aspose.CAD 문서](https://reference.aspose.com/cad/net/).

### Q5: Aspose.CAD for .NET에 대한 도움을 구하거나 경험을 공유할 수 있는 곳은 어디입니까?

A5: Aspose.CAD 커뮤니티에 가입하세요.[법정](https://forum.aspose.com/c/cad/19) 다른 개발자와 상호 작용하고 도움을 구합니다.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
