---
title: C#에서 특정 DWG를 이미지로 변환 - Aspose.CAD 가이드
linktitle: C#에서 특정 DWG를 이미지로 변환
second_title: Aspose.CAD .NET - CAD 및 BIM 파일 형식
description: .NET용 Aspose.CAD를 살펴보세요. DWG를 C#의 이미지로 손쉽게 변환하세요. 코드 예제가 포함된 종합 가이드입니다.
type: docs
weight: 15
url: /ko/net/image-manipulation-and-rendering/converting-particular-dwg-to-image/
---
## 소개

역동적인 소프트웨어 개발 세계에서는 CAD 파일을 효율적으로 처리하는 것이 중요합니다. .NET용 Aspose.CAD는 개발자에게 CAD 파일을 원활하게 조작하고 변환할 수 있는 강력한 도구 세트를 제공하는 강력한 솔루션으로 등장합니다. 이 튜토리얼에서는 C#을 사용하여 특정 DWG 파일을 이미지로 변환하는 과정을 살펴보겠습니다.

## 전제 조건

이 코딩 여정을 시작하기 전에 다음 전제 조건이 충족되었는지 확인하세요.

- Visual Studio: C# 코드를 작성하고 실행하기 위한 개발 환경입니다.
-  .NET용 Aspose.CAD: 라이브러리가 설치되어 있는지 확인하세요. 다운로드 링크를 찾을 수 있습니다[여기](https://releases.aspose.com/cad/net/).
- DWG 파일: 변환할 DWG 파일을 준비합니다. 샘플 파일 "시각화"를 사용할 수 있습니다_-_conference_room.dwg"를 참조하세요.

## 네임스페이스 가져오기

C# 코드에서 Aspose.CAD 작업에 필요한 네임스페이스를 가져와야 합니다.

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadConsts;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## 1단계: DWG 파일 로드

DWG 파일을 Aspose.CAD 프레임워크에 로드하여 시작합니다.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "visualization_-_conference_room.dwg";
var cadImage = (CadImage)Aspose.CAD.Image.Load(sourceFilePath);
```

## 2단계: 엔터티 필터링

다음으로 DWG 파일의 요소를 필터링합니다. 이 예에서는 텍스트 엔터티 추출에 중점을 둡니다.

```csharp
CadBaseEntity[] entities = cadImage.Entities;
List<CadBaseEntity> filteredEntities = new List<CadBaseEntity>();

foreach (CadBaseEntity baseEntity in entities)
{
    // 엔터티 선택 또는 필터링
    if (baseEntity.TypeName == CadEntityTypeName.TEXT)
    {
        filteredEntities.Add(baseEntity);
    }
}

cadImage.Entities = filteredEntities.ToArray();
```

## 3단계: 래스터화 옵션 설정

 인스턴스 만들기`CadRasterizationOptions` 이미지 변환에 대한 속성을 정의합니다.

```csharp
Aspose.CAD.ImageOptions.CadRasterizationOptions rasterizationOptions =
    new Aspose.CAD.ImageOptions.CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
rasterizationOptions.AutomaticLayoutsScaling = true;
```

## 4단계: PDF 옵션 설정

 인스턴스 만들기`PdfOptions` 래스터화 옵션을 할당합니다.

```csharp
Aspose.CAD.ImageOptions.PdfOptions pdfOptions = new Aspose.CAD.ImageOptions.PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## 5단계: PDF로 저장

마지막으로 변환된 이미지를 PDF 파일로 저장합니다.

```csharp
string outFile = MyDir + "result_out_generated.pdf";
cadImage.Save(outFile, pdfOptions);
```

## 결론

축하해요! .NET용 Aspose.CAD를 사용하여 특정 DWG 파일을 이미지로 성공적으로 변환했습니다. 이 튜토리얼에서는 라이브러리의 강력한 기능을 간략히 살펴보고 개발자가 애플리케이션에서 CAD 파일을 효율적으로 사용할 수 있도록 지원합니다.

## FAQ

### Q1: Aspose.CAD는 모든 버전의 DWG 파일과 호환됩니까?

A1: Aspose.CAD는 다양한 버전의 DWG 파일을 지원하여 광범위한 CAD 소프트웨어 간의 호환성을 보장합니다.

### Q2: 다양한 출력에 대한 래스터화 옵션을 사용자 정의할 수 있습니까?

A2: 물론이죠! Aspose.CAD는 다양한 출력 형식에 대한 특정 요구 사항을 충족하기 위해 래스터화 옵션을 조정하는 유연성을 제공합니다.

### Q3: 추가 예제와 문서는 어디에서 찾을 수 있습니까?

 A3: 포괄적인 탐색[Aspose.CAD 문서](https://reference.aspose.com/cad/net/) 더 많은 예시와 심층적인 안내를 확인하세요.

### Q4: Aspose.CAD에 대한 무료 평가판이 있습니까?

 A4: 예, 무료 평가판에 액세스할 수 있습니다.[여기](https://releases.aspose.com/) Aspose.CAD의 잠재력을 최대한 경험해보세요.

### Q5: 어떻게 지원을 받거나 도움을 받기 위해 커뮤니티에 연결할 수 있나요?

A5: 다음을 방문하세요.[Aspose.CAD 포럼](https://forum.aspose.com/c/cad/19) 커뮤니티와의 지원, 토론 및 협력을 위해.