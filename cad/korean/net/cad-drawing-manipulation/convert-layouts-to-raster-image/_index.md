---
title: .NET용 Aspose.CAD에서 레이아웃을 래스터 이미지로 변환
linktitle: 레이아웃을 래스터 이미지로 변환
second_title: Aspose.CAD .NET - CAD 및 BIM 파일 형식
description: Aspose.CAD for .NET을 사용하여 CAD 레이아웃을 래스터 이미지로 쉽게 변환하세요. 강력한 CAD 조작 기능으로 개발을 강화하세요.
weight: 12
url: /ko/net/cad-drawing-manipulation/convert-layouts-to-raster-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# .NET용 Aspose.CAD에서 레이아웃을 래스터 이미지로 변환

## 소개

.NET 애플리케이션에서 레이아웃을 래스터 이미지로 쉽게 변환하고 싶으십니까? 더 이상 보지 마세요! 이 단계별 가이드는 CAD(Computer-Aided Design) 작업을 단순화하는 강력한 라이브러리인 Aspose.CAD for .NET을 사용하는 프로세스를 안내합니다.

## 전제 조건

튜토리얼을 시작하기 전에 다음 전제 조건이 충족되었는지 확인하세요.

- .NET 라이브러리용 Aspose.CAD: 다음에서 라이브러리를 다운로드하고 설치합니다.[.NET용 Aspose.CAD 다운로드 페이지](https://releases.aspose.com/cad/net/).

- 개발 환경: 컴퓨터에 작동하는 .NET 개발 환경이 설정되어 있는지 확인하세요.

- 변환할 문서: 래스터 이미지로 변환할 레이아웃이 포함된 CAD 문서를 준비합니다.

- 문서 디렉터리: 코드의 자리 표시자 "문서 디렉터리"를 문서 디렉터리 경로로 바꿉니다.

## 네임스페이스 가져오기

먼저, 코드에서 Aspose.CAD 기능에 액세스할 수 있도록 필요한 네임스페이스를 가져와 보겠습니다.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## 1단계: CAD 문서 로드

Aspose.CAD 라이브러리를 사용하여 CAD 문서를 로드하는 것부터 시작하세요.

```csharp
string sourceFilePath = MyDir + "conic_pyramid.dxf";
using (Image image = Image.Load(sourceFilePath))
{
    //추가 단계를 위한 코드가 여기에 표시됩니다.
}
```

## 2단계: 래스터화 옵션 구성

 인스턴스 만들기`CadRasterizationOptions` 페이지 너비, 높이를 설정하고 변환하려는 레이아웃을 지정합니다.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1200;
rasterizationOptions.PageHeight = 1200;
rasterizationOptions.Layouts = new string[] { "Model", "Layout1" };
```

## 3단계: 결과 이미지에 대한 TiffOptions 설정

 인스턴스 만들기`TiffOptions`결과 이미지의 형식을 정의합니다.

```csharp
ImageOptionsBase options = new TiffOptions(TiffExpectedFormat.Default);
options.VectorRasterizationOptions = rasterizationOptions;
```

## 4단계: 결과 이미지 저장

출력 경로를 지정하고 변환된 이미지를 저장합니다.

```csharp
string outputFilePath = MyDir + "conic_pyramid_layoutstorasterimage_out.tiff";
image.Save(outputFilePath, options);
```

## 결론

축하해요! Aspose.CAD for .NET을 사용하여 CAD 레이아웃을 래스터 이미지 형식으로 성공적으로 변환했습니다. 가능성은 무궁무진하며 이 가이드는 CAD 관련 작업의 출발점이 됩니다.

## FAQ

### Q1: Aspose.CAD는 모든 CAD 형식과 호환됩니까?

 A1: Aspose.CAD는 DWG, DXF, DWF, STL 등을 포함한 광범위한 CAD 형식을 지원합니다. 을 체크 해봐[선적 서류 비치](https://reference.aspose.com/cad/net/) 포괄적인 목록을 보려면

### Q2: Aspose.CAD의 임시 라이선스는 어떻게 얻을 수 있나요?

 A2: 다음을 방문하세요.[임시 라이센스 페이지](https://purchase.aspose.com/temporary-license/) 테스트 및 평가 목적으로 임시 라이센스를 취득합니다.

### Q3: Aspose.CAD에 대한 지원은 어디서 찾을 수 있나요?

 답변 3: 포럼은 도움을 구할 수 있는 좋은 장소입니다. 방문하다[Aspose.CAD 포럼](https://forum.aspose.com/c/cad/19) 커뮤니티에 연결하고 도움을 받으려면

### Q4: Aspose.CAD를 무료로 사용해 볼 수 있나요?

 A4: 물론이죠! 당신의[무료 시험판](https://releases.aspose.com/) Aspose.CAD의 기능과 기능을 탐색합니다.

### Q5: Aspose.CAD 라이선스는 어디서 구입할 수 있나요?

 A5: 다음으로 이동하세요.[구매 페이지](https://purchase.aspose.com/buy) 라이센스를 구매하고 Aspose.CAD의 잠재력을 최대한 활용하세요.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
