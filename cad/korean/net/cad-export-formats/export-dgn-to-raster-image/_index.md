---
title: .NET용 Aspose.CAD에서 DGN을 래스터 이미지로 내보내기
linktitle: DGN을 래스터 이미지로 내보내기
second_title: Aspose.CAD .NET - CAD 및 BIM 파일 형식
description: .NET용 Aspose.CAD를 사용하여 DGN을 래스터 이미지로 손쉽게 변환하세요. 단계별 가이드를 살펴보고 CAD 파일 조작에서 .NET의 강력한 기능을 활용해 보세요.
weight: 13
url: /ko/net/cad-export-formats/export-dgn-to-raster-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# .NET용 Aspose.CAD에서 DGN을 래스터 이미지로 내보내기

## 소개

.NET 개발의 동적 영역에서 Aspose.CAD는 CAD(Computer-Aided Design) 파일을 처리하기 위한 강력한 도구로 등장합니다. 이 튜토리얼에서는 .NET용 Aspose.CAD를 사용하여 DGN 파일을 래스터 이미지로 내보내는 과정을 자세히 설명합니다. DGN 파일을 시각적으로 매력적인 래스터 이미지로 원활하게 변환하고 싶다면 잘 찾아오셨습니다.

## 전제 조건

이 여정을 시작하기 전에 다음과 같은 전제 조건이 갖추어져 있는지 확인하세요.

-  .NET용 Aspose.CAD: .NET 프로젝트에 Aspose.CAD 라이브러리가 설치되어 있는지 확인하세요. 라이브러리 및 관련 문서는 다음에서 찾을 수 있습니다.[웹사이트](https://reference.aspose.com/cad/net/).

- 샘플 DGN 파일: 변환할 DGN 파일을 준비합니다. 이 예에서는 "Nikon_D90_Camera.dgn"을 사용합니다.

이제 단계별 가이드를 살펴보겠습니다.

## 네임스페이스 가져오기

.NET 프로젝트에서 Aspose.CAD에 필요한 네임스페이스를 가져오는 것부터 시작하세요. 이 단계를 통해 DGN을 래스터 이미지로 변환하는 데 필요한 클래스와 메서드에 액세스할 수 있습니다.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## 1단계: DGN 파일 로드

 DGN 파일을`CadImage` 물체. 이는 후속 작업의 기반을 제공합니다.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // 추가 처리를 위한 코드는 여기에 있습니다.
}
```

## 2단계: 래스터화 옵션 정의

 만들기`CadRasterizationOptions` 개체를 만들고 다양한 속성을 설정하여 요구 사항에 따라 래스터화 프로세스를 사용자 정의합니다.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 600;
rasterizationOptions.PageHeight = 300;
rasterizationOptions.NoScaling = true;
rasterizationOptions.AutomaticLayoutsScaling = false;
```

## 3단계: JpegOptions 객체 생성

 우리는 DGN 파일을 JPEG로 변환하는 것을 목표로 하므로`JpegOptions` 객체를 지정하고 이전에 정의한 것을 할당합니다.`CadRasterizationOptions` 그것에.

```csharp
ImageOptionsBase options = new JpegOptions();
options.VectorRasterizationOptions = rasterizationOptions;
```

## 4단계: 래스터 이미지 저장

 활용`Save` 의 방법`CadImage` DGN 파일을 원하는 형식(이 경우 JPEG)의 래스터 이미지로 내보내는 클래스입니다.

```csharp
cadImage.Save(MyDir + "ExportDGNToRasterImage_out.jpg", options);
```

## 결론

축하해요! .NET용 Aspose.CAD를 사용하여 DGN 파일을 래스터 이미지로 내보내는 단계를 성공적으로 탐색했습니다. 이 튜토리얼에서는 이 기능을 .NET 프로젝트에 쉽게 통합하는 데 필요한 필수 지식을 제공합니다.

## FAQ

### Q1: DGN 파일을 JPEG 이외의 형식으로 내보낼 수 있습니까?

A1: 예, .NET용 Aspose.CAD는 다양한 출력 형식을 지원합니다. 3단계에서 이에 따라 옵션을 수정할 수 있습니다.

### Q2 변환 과정에서 발생하는 예외 처리는 어떻게 하나요?

A2: 잠재적인 문제를 해결하려면 제공된 코드에 설명된 대로 적절한 예외 처리가 있는지 확인하세요.

### Q3: Aspose.CAD for .NET에 사용할 수 있는 평가판이 있습니까?

 A3: 예, 무료 평가판을 통해 제품을 살펴볼 수 있습니다. 방문하다[여기](https://releases.aspose.com/) 자세한 내용은.

### Q4: Aspose.CAD for .NET과 관련된 문제에 대해 도움을 구하거나 논의할 수 있는 곳은 어디입니까?

 A4: 다음으로 가세요.[Aspose.CAD 포럼](https://forum.aspose.com/c/cad/19) 커뮤니티 지원 및 토론을 위해.

### Q5: .NET용 Aspose.CAD의 임시 라이선스를 어떻게 얻나요?

 A5: 방문[이 링크](https://purchase.aspose.com/temporary-license/)귀하의 개발 요구에 맞는 임시 라이센스를 취득하십시오.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
