---
title: 3D 이미지를 PDF로 내보내기 - Aspose.CAD 튜토리얼
linktitle: 3D 이미지를 PDF로 내보내기
second_title: Aspose.CAD .NET - CAD 및 BIM 파일 형식
description: .NET용 Aspose.CAD를 사용하여 3D CAD 이미지를 PDF로 쉽게 변환하세요. 원활한 PDF 내보내기를 위한 단계별 튜토리얼을 따르십시오.
type: docs
weight: 10
url: /ko/net/3d-image-export/exporting-3d-images-to-pdf/
---
## 소개

.NET용 Aspose.CAD를 사용하여 3D 이미지를 PDF로 원활하게 내보내고 싶으십니까? 이 단계별 튜토리얼은 Aspose.CAD의 강력한 기능을 활용하여 3D 이미지를 PDF 형식으로 쉽게 변환하는 과정을 안내합니다.

## 전제 조건

튜토리얼을 시작하기 전에 다음 전제 조건이 충족되었는지 확인하세요.

-  .NET용 Aspose.CAD: .NET용 Aspose.CAD 라이브러리가 설치되어 있는지 확인하세요. 그렇지 않은 경우 다음에서 다운로드할 수 있습니다.[.NET용 Aspose.CAD 다운로드 페이지](https://releases.aspose.com/cad/net/).

- 문서 디렉터리: CAD 파일이 저장되는 디렉터리를 설정하고 경로를 기록해 둡니다.

## 네임스페이스 가져오기

.NET 프로젝트에서 Aspose.CAD 작업에 필요한 네임스페이스를 가져옵니다. 코드 파일 상단에 다음 줄을 추가합니다.

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

 PDF로 내보내려는 CAD 이미지를 로드하는 것부터 시작하세요. 사용`Load` Aspose.CAD 라이브러리의 메서드입니다. 바꾸다`"conic_pyramid.dxf"` CAD 파일의 경로와 함께.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";
using (Image cadImage = Image.Load(sourceFilePath))
{
    // CAD 이미지를 로드하기 위한 코드는 여기에 있습니다.
}
```

## 2단계: 래스터화 옵션 구성

 CAD 이미지의 래스터화 옵션을 구성합니다. 페이지 너비, 페이지 높이, 레이아웃과 같은 매개변수를 설정합니다. 다음과 관련된 줄의 주석 처리를 해제하세요.`TypeOfEntities` 엔터티가 3D인 경우.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 500;
rasterizationOptions.PageHeight = 500;
// rasterizationOptions.TypeOfEntities = TypeOfEntities.Entities3D;

rasterizationOptions.Layouts = new string[] { "Model" };
```

## 3단계: PDF 옵션 설정

PDF 옵션을 생성하고 이를 래스터화 옵션과 연결합니다.

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## 4단계: PDF로 저장

구성된 옵션을 사용하여 CAD 이미지를 PDF 파일로 저장합니다. PDF 파일의 출력 경로를 지정합니다.

```csharp
MyDir = MyDir + "Export3DImagestoPDF_out.pdf";
cadImage.Save(MyDir, pdfOptions);
```

## 결론

축하해요! .NET용 Aspose.CAD를 사용하여 3D 이미지를 PDF로 성공적으로 내보냈습니다. 이 간단한 튜토리얼을 통해 CAD 파일을 보다 접근하기 쉬운 형식으로 쉽게 변환할 수 있습니다.

## FAQ

### Q1: Aspose.CAD는 모든 CAD 파일 형식과 호환됩니까?

A1: 예, Aspose.CAD는 광범위한 CAD 형식을 지원하여 다양한 파일 형식을 처리할 수 있는 유연성을 보장합니다.

### Q2: PDF로 내보낼 때 페이지 크기를 사용자 정의할 수 있습니까?

A2: 물론이죠. 이 튜토리얼에서는 요구 사항에 따라 페이지 너비와 높이를 구성하는 방법을 보여줍니다.

### Q3: Aspose.CAD에 임시 라이선스를 사용할 수 있나요?

 A3: 예, 다음 사이트를 방문하여 Aspose.CAD에 대한 임시 라이선스를 얻을 수 있습니다.[임시면허](https://purchase.aspose.com/temporary-license/).

### Q4: 추가 지원이나 커뮤니티 토론은 어디서 찾을 수 있나요?

 A4: 다음으로 가세요.[Aspose.CAD 포럼](https://forum.aspose.com/c/cad/19) 지역사회에 대한 지원과 참여를 위해.

### Q5: Aspose.CAD의 무료 평가판이 있습니까?

 A5: 예, Aspose.CAD에 액세스하여 기능을 탐색할 수 있습니다.[무료 시험판](https://releases.aspose.com/).