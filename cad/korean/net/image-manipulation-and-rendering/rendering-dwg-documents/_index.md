---
title: C#에서 DWG 문서 렌더링 - Aspose.CAD 가이드
linktitle: C#에서 DWG 문서 렌더링
second_title: Aspose.CAD .NET - CAD 및 BIM 파일 형식
description: Aspose.CAD를 사용하여 C#에서 DWG 문서를 렌더링하는 방법을 알아보세요. 이 단계별 가이드에서는 코드 예제를 사용하여 가져오기, 구성 및 저장을 다룹니다.
type: docs
weight: 17
url: /ko/net/image-manipulation-and-rendering/rendering-dwg-documents/
---
## 소개

Aspose.CAD를 사용하여 C#에서 DWG 문서를 렌더링하는 방법에 대한 종합 가이드에 오신 것을 환영합니다. 숙련된 개발자이거나 .NET을 처음 시작하는 개발자라면 이 튜토리얼에서는 Aspose.CAD를 활용하여 DWG 파일을 효율적으로 렌더링하는 과정을 안내합니다. Aspose.CAD는 CAD 파일 형식 작업을 위한 강력한 기능을 제공하는 강력한 API이므로 DWG 파일을 다루는 개발자가 선택할 수 있습니다.

## 전제 조건

튜토리얼을 시작하기 전에 다음 전제조건이 충족되었는지 확인하십시오.

- C# 프로그래밍 언어에 대한 기본 지식.
- 컴퓨터에 Visual Studio가 설치되어 있습니다.
-  Aspose.CAD 라이브러리가 프로젝트에 통합되었습니다. 다음에서 다운로드할 수 있습니다.[여기](https://releases.aspose.com/cad/net/).
- 예제와 함께 사용할 "Bottom_plate.dwg"와 같은 샘플 DWG 파일.

## 네임스페이스 가져오기

시작하려면 C# 코드 시작 부분에 필요한 네임스페이스를 가져와야 합니다.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
using Aspose.CAD.FileFormats.Cad.CadTables;
using Aspose.CAD.FileFormats.Cad;
```

이제 제공된 예제를 여러 단계로 나누어 보겠습니다.

## 1단계: DWG 파일 로드

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Bottom_plate.dwg";
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // DWG 파일을 로드하기 위한 코드가 여기에 있습니다.
}
```

## 2단계: 래스터화 옵션 구성

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.Layouts = new string[] { "Model" };
rasterizationOptions.NoScaling = true;
//여기에 추가 래스터화 구성을 추가할 수 있습니다.
```

## 3단계: 그릴 영역 정의

```csharp
Point topLeft = new Point(6156, 7053);
double width = 3108;
double height = 2489;
```

## 4단계: 새 뷰포트 만들기

```csharp
CadVportTableObject newView = new CadVportTableObject();
newView.Name.Value = "*Active";
newView.CenterPoint.X = topLeft.X + width / 2f;
newView.CenterPoint.Y = topLeft.Y - height / 2f;
newView.ViewHeight.Value = height;
newView.ViewAspectRatio.Value = width / height;
```

## 5단계: 활성 뷰포트 교체

```csharp
for (int i = 0; i < cadImage.ViewPorts.Count; i++)
{
    CadVportTableObject currentView = (CadVportTableObject)(cadImage.ViewPorts[i]);
    if ((currentView.Name.Value == null && cadImage.ViewPorts.Count == 1) ||
    string.Equals(currentView.Name.Value.ToLowerInvariant(), "*active"))
    {
        cadImage.ViewPorts[i] = newView;
        break;
    }
}
```

## 6단계: PDF 옵션 구성

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## 7단계: 렌더링된 DWG를 PDF로 저장

```csharp
cadImage.Save(MyDir, pdfOptions);
```

## 결론

축하해요! C#에서 Aspose.CAD를 사용하여 DWG 문서를 PDF로 성공적으로 렌더링했습니다. 자유롭게 더 많은 기능을 살펴보고 특정 요구 사항에 따라 코드를 맞춤설정해 보세요.

## FAQ

### Q1: Aspose.CAD를 다른 CAD 파일 형식과 함께 사용할 수 있습니까?

A1: 예, Aspose.CAD는 DWG, DXF, DWF 등을 포함한 다양한 CAD 형식을 지원합니다.

### Q2: Aspose.CAD는 .NET Core와 호환됩니까?

A2: 예, Aspose.CAD는 .NET Framework 및 .NET Core와 모두 호환됩니다.

### Q3: DWG 파일의 다양한 레이아웃을 어떻게 처리할 수 있습니까?

 A3: 원하는 레이아웃을 지정할 수 있습니다.`Layouts` 의 자산`CadRasterizationOptions`.

### Q4: Aspose.CAD 사용 시 라이선스 고려 사항이 있나요?

 A4: 라이선스에 대한 자세한 내용을 보려면 다음을 방문하세요.[여기](https://purchase.aspose.com/buy).

### Q5: 추가 지원은 어디서 찾을 수 있나요?

A5: 다음을 방문하세요.[Aspose.CAD 포럼](https://forum.aspose.com/c/cad/19) 커뮤니티 지원 및 토론을 위해.