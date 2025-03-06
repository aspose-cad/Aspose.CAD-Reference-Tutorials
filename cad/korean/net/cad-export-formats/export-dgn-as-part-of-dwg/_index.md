---
title: .NET용 Aspose.CAD에서 DWG의 일부로 DGN 내보내기
linktitle: DGN을 DWG의 일부로 내보내기
second_title: Aspose.CAD .NET - CAD 및 BIM 파일 형식
description: .NET용 Aspose.CAD에서 DWG의 일부로 DGN을 내보내는 방법을 알아보세요. 원활한 통합을 위한 단계별 가이드를 따르세요.
weight: 11
url: /ko/net/cad-export-formats/export-dgn-as-part-of-dwg/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# .NET용 Aspose.CAD에서 DWG의 일부로 DGN 내보내기

## 소개

.NET 개발 세계에서 Aspose.CAD는 CAD(Computer-Aided Design) 파일 작업을 위한 강력한 라이브러리로 돋보입니다. 이 튜토리얼은 .NET용 Aspose.CAD를 사용하여 DGN(디자인) 파일을 DWG(도면) 파일의 일부로 내보내는 과정을 안내합니다. 숙련된 개발자이든 이제 막 시작하는 개발자이든 이 단계별 가이드는 Aspose.CAD의 기능을 활용하여 특정 작업을 효율적으로 수행하는 데 도움이 될 것입니다.

## 전제 조건

튜토리얼을 시작하기 전에 다음 전제 조건이 충족되었는지 확인하세요.

-  .NET용 Aspose.CAD: .NET용 Aspose.CAD 라이브러리가 설치되어 있는지 확인하세요. 당신은 그것을 다운로드 할 수 있습니다[여기](https://releases.aspose.com/cad/net/).

- 개발 환경: Visual Studio와 같은 선호하는 .NET 개발 환경을 설정합니다.

- C# 기본 지식: C# 프로그래밍 언어에 익숙해집니다.

## 네임스페이스 가져오기

C# 프로젝트에서 Aspose.CAD 기능에 액세스하는 데 필요한 네임스페이스를 포함합니다. 코드 파일 시작 부분에 다음 using 지시문을 추가합니다.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

이제 제공된 코드를 여러 단계로 나누어 보겠습니다.

## 1단계: 파일 경로 정의

```csharp
//입력 및 출력 파일 경로
string fileName = "BlockRefDgn.dwg";
string outPath = fileName + ".pdf";
```

## 2단계: PdfOptions 인스턴스 생성

```csharp
// DWG를 PDF로 내보내기 위한 PdfOptions 클래스의 인스턴스 생성
PdfOptions exportOptions = new PdfOptions();
```

## 3단계: DWG 파일 로드

```csharp
// 기존 DWG 파일을 이미지로 로드하고 CadImage 유형으로 변환합니다.
using (CadImage cadImage = (CadImage)Image.Load(fileName))
```

## 4단계: 엔터티 반복

```csharp
// DWG 파일 내의 각 엔터티를 반복합니다.
foreach (CadBaseEntity baseEntity in cadImage.Entities)
```

## 5단계: 엔터티 유형 확인

```csharp
// 엔터티가 이미지 정의인지 확인하세요.
if (baseEntity.TypeName == CadEntityTypeName.DGNUNDERLAY)
```

## 6단계: 언더레이 경로 가져오기

```csharp
// 이미지 정의인 경우 객체에 대한 외부 참조를 가져옵니다.
CadDgnUnderlay dgnFile = (CadDgnUnderlay)baseEntity;
Console.WriteLine(dgnFile.UnderlayPath);
```

## 7단계: 래스터화 옵션 정의

```csharp
// CadRasterizationOptions 개체에 대한 설정 정의
exportOptions.VectorRasterizationOptions = new CadRasterizationOptions()
{
    PageWidth = 1600,
    PageHeight = 1600,
    Layouts = new string[] { "Model" },
    AutomaticLayoutsScaling = false,
    NoScaling = true,
    BackgroundColor = Color.Black,
    DrawType = CadDrawTypeMode.UseObjectColor
};
```

## 8단계: DWG를 PDF로 내보내기

```csharp
// Save 메서드를 호출하여 DWG를 PDF로 내보냅니다.
cadImage.Save(outPath, exportOptions);
```

## 결론

축하해요! Aspose.CAD for .NET을 사용하여 DGN 파일을 DWG 파일의 일부로 내보내는 과정을 성공적으로 진행했습니다. 이 튜토리얼에서는 이 특정 작업을 원활하게 수행하기 위한 기본 단계와 코드 조각을 제공했습니다.

## FAQ

### Q1: 상업용 프로젝트에서 Aspose.CAD for .NET을 사용할 수 있나요?
 A1: 네, 가능합니다. 방문하다[여기](https://purchase.aspose.com/buy) 라이선스 옵션을 살펴보세요.

### Q2: 처리할 수 있는 DWG 파일 크기에 제한이 있습니까?
A2: Aspose.CAD는 대용량 DWG 파일 처리를 지원하지만 하드웨어 제한이 적용될 수 있습니다.

### Q3: 평가판을 사용할 수 있나요?
A3: 예, 무료 평가판을 받을 수 있습니다.[여기](https://releases.aspose.com/).

### Q4: 임시 라이센스는 어떻게 얻을 수 있나요?
 A4: 임시 라이센스를 얻을 수 있습니다[여기](https://purchase.aspose.com/temporary-license/).

### Q5: 문제가 발생하면 어디서 도움을 받을 수 있나요?
 A5: Aspose.CAD 포럼을 방문할 수 있습니다.[여기](https://forum.aspose.com/c/cad/19) 지원을 위해.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
