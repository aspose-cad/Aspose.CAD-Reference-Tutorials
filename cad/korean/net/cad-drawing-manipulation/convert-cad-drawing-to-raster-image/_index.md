---
title: .NET용 Aspose.CAD에서 CAD 도면을 래스터 이미지로 변환
linktitle: CAD 도면을 래스터 이미지로 변환
second_title: Aspose.CAD .NET - CAD 및 BIM 파일 형식
description: Aspose.CAD를 사용하여 .NET에서 CAD 도면을 래스터 이미지로 변환하는 원활한 프로세스를 살펴보세요. 효율적인 워크플로우를 활용하고 CAD 프로젝트를 손쉽게 향상하세요.
type: docs
weight: 11
url: /ko/net/cad-drawing-manipulation/convert-cad-drawing-to-raster-image/
---
## 소개

끊임없이 진화하는 CAD(컴퓨터 지원 설계) 환경에서는 CAD 도면을 래스터 이미지로 원활하게 변환하는 것이 무엇보다 중요합니다. 이 단계별 가이드에서는 강력한 .NET용 Aspose.CAD 라이브러리를 사용하여 이를 달성하는 방법을 살펴봅니다. Aspose.CAD는 프로세스를 단순화하여 개발자에게 CAD 관련 워크플로우를 향상시킬 수 있는 강력한 도구 세트를 제공합니다.

## 전제 조건

튜토리얼을 시작하기 전에 다음 전제 조건이 충족되었는지 확인하세요.

1.  .NET 라이브러리용 Aspose.CAD: 다음에서 Aspose.CAD 라이브러리를 다운로드하고 설치하세요.[다운로드 페이지](https://releases.aspose.com/cad/net/).

2. 개발 환경: .NET 개발용 호환 IDE를 사용하여 작업 개발 환경을 설정합니다.

## 네임스페이스 가져오기

.NET 프로젝트에서 Aspose.CAD 기능에 액세스하는 데 필요한 네임스페이스를 가져옵니다. 코드 파일 시작 부분에 다음을 추가합니다.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## 1단계: 파일 경로 정의

```csharp
// 문서 디렉터리의 경로입니다.
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";
```

"문서 디렉토리"를 CAD 파일의 실제 경로로 바꾸십시오.

## 2단계: CAD 도면 로드

```csharp
using (Aspose.CAD.Image image = Aspose.CAD.Image.Load(sourceFilePath))
{
```

이 단계에서는 Aspose.CAD 이미지 개체를 초기화하고 지정된 파일 경로에서 CAD 도면을 로드합니다.

## 3단계: 래스터화 옵션 구성

```csharp
// CadRasterizationOptions 인스턴스 생성
Aspose.CAD.ImageOptions.CadRasterizationOptions rasterizationOptions = new Aspose.CAD.ImageOptions.CadRasterizationOptions();
// 페이지 너비 및 높이 설정
rasterizationOptions.PageWidth = 1200;
rasterizationOptions.PageHeight = 1200;
```

여기서는 출력 페이지의 너비와 높이를 정의하는 래스터화 옵션을 설정합니다.

## 4단계: 결과 이미지에 대한 PngOptions 만들기

```csharp
// 결과 이미지에 대한 PngOptions 인스턴스를 만듭니다.
ImageOptionsBase options = new Aspose.CAD.ImageOptions.PngOptions();
// 래스터화 옵션 설정
options.VectorRasterizationOptions = rasterizationOptions;
```

이 단계에는 이전에 정의한 래스터화 옵션을 지정하고 결과 이미지에 대한 옵션을 구성하는 작업이 포함됩니다.

## 5단계: 결과 이미지 저장

```csharp
MyDir = MyDir + "conic_pyramid_raster_image_out.png";
// 결과 이미지 저장
image.Save(MyDir, options);
```

변환된 래스터 이미지를 지정된 출력 파일 경로에 저장합니다.

## 6단계: 성공 메시지 표시

```csharp
// ExEnd:Convert DrawingToRasterImage
Console.WriteLine("\nCAD drawing converted successfully to raster image format.\nFile saved at " + MyDir);
```

변환 프로세스가 완료되었음을 나타내는 성공 메시지를 표시합니다.

## 결론

이 튜토리얼에서는 .NET용 Aspose.CAD 라이브러리를 사용하여 CAD 도면을 래스터 이미지로 변환하는 단계별 프로세스를 살펴보았습니다. 강력한 기능과 통합 용이성을 갖춘 Aspose.CAD는 개발자가 CAD 작업 흐름을 쉽게 간소화할 수 있도록 지원합니다.

## FAQ

### Q1: Aspose.CAD는 모든 CAD 파일 형식과 호환됩니까?

A1: Aspose.CAD는 DWG, DXF, DGN 등을 포함한 광범위한 CAD 파일 형식을 지원합니다. 다음을 참조하세요.[선적 서류 비치](https://reference.aspose.com/cad/net/) 포괄적인 목록을 보려면

### Q2: 다양한 프로젝트에 대한 래스터화 옵션을 사용자 정의할 수 있습니까?

A2: 예, Aspose.CAD는 래스터화 옵션의 광범위한 사용자 정의를 허용하므로 개발자는 프로젝트 요구 사항에 따라 출력을 맞춤화할 수 있습니다.

### Q3: Aspose.CAD에 대한 무료 평가판이 있습니까?

 A3: 예, 무료 평가판을 통해 Aspose.CAD의 기능을 탐색할 수 있습니다. 방문하다[여기](https://releases.aspose.com/) 시작하려면.

### Q4: Aspose.CAD에 대한 지원은 어떻게 받을 수 있나요?

 A4: 도움이나 문의사항이 있으면 Aspose.CAD를 방문하세요.[지원 포럼](https://forum.aspose.com/c/cad/19).

### Q5: Aspose.CAD에 임시 라이선스를 사용할 수 있나요?
 
 A5: 예, 개발자는 Aspose.CAD에 대한 임시 라이선스를 다음에서 얻을 수 있습니다.[이 링크](https://purchase.aspose.com/temporary-license/).