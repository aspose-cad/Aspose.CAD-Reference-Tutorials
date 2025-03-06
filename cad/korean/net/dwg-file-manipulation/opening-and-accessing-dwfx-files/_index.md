---
title: C#에서 DWFX 파일 열기 및 액세스 - Aspose.CAD 가이드
linktitle: C#에서 DWFX 파일 열기 및 액세스
second_title: Aspose.CAD .NET - CAD 및 BIM 파일 형식
description: .NET용 Aspose.CAD를 사용하여 C#에서 DWFX 파일을 열고 액세스하는 방법을 알아보세요. 애플리케이션에 원활하게 통합하기 위한 단계별 가이드입니다.
weight: 12
url: /ko/net/dwg-file-manipulation/opening-and-accessing-dwfx-files/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# C#에서 DWFX 파일 열기 및 액세스 - Aspose.CAD 가이드

## 소개

강력한 .NET용 Aspose.CAD 라이브러리를 사용하여 C#에서 DWFX 파일을 열고 액세스하는 방법에 대한 단계별 가이드에 오신 것을 환영합니다. CAD 기능을 C# 애플리케이션에 통합하려는 개발자라면 잘 찾아오셨습니다. 이 튜토리얼에서는 모든 기술 수준의 개발자가 액세스할 수 있도록 프로세스를 간단한 단계로 나누어 단계별로 안내합니다.

## 전제 조건

튜토리얼을 시작하기 전에 다음 전제 조건이 충족되었는지 확인하세요.

1.  .NET 라이브러리용 Aspose.CAD: .NET용 Aspose.CAD 라이브러리가 설치되어 있는지 확인하세요. 당신은 그것을 다운로드 할 수 있습니다[여기](https://releases.aspose.com/cad/net/).

2. 문서 디렉토리: DWFX 파일을 저장할 디렉토리를 설정합니다. C# 코드의 소스 및 출력 디렉터리를 기록해 둡니다.

## 네임스페이스 가져오기

C# 프로젝트에서 필요한 네임스페이스를 가져오는 것부터 시작합니다.

```csharp
using Aspose.CAD.ImageOptions;
using System;
```

이러한 네임스페이스는 응용 프로그램에서 CAD 파일 작업을 위한 필수 클래스와 기능을 제공합니다.

## 1단계: 소스 및 출력 디렉터리 설정

```csharp
string SourceDir = "Your Document Directory";
string OutputDir = "Your Document Directory";
```

"Your Document Directory"를 소스 및 출력 디렉터리의 실제 경로로 바꾸십시오.

## 2단계: DWFX 파일 로드

```csharp
using (Image cadDrawing = Image.Load(SourceDir + "Tyrannosaurus.dwfx"))
```

 다음을 사용하여 DWFX 파일을 로드합니다.`Image.Load` 방법. "Tyrannosaurus.dwfx"를 DWFX 파일의 실제 이름으로 바꾸십시오.

## 3단계: 래스터화 옵션 구성

```csharp
var rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = cadDrawing.Size.Width;
rasterizationOptions.PageHeight = cadDrawing.Size.Height;
```

로드된 CAD 도면의 크기에 따라 래스터화 옵션을 구성합니다.

## 4단계: PDF로 저장

```csharp
PdfOptions CADf = new PdfOptions();
CADf.VectorRasterizationOptions = rasterizationOptions;
cadDrawing.Save(OutputDir + "OpenDwfxFile_out.pdf", CADf);
```

구성된 래스터화 옵션을 적용하여 로드된 DWFX 파일을 PDF로 저장합니다.

## 5단계: 성공 메시지 표시

```csharp
Console.WriteLine("OpenDwfxFile executed successfully");
```

코드가 성공적으로 실행되었음을 확인하기 위해 성공 메시지를 콘솔에 인쇄합니다.

## 결론

축하해요! .NET용 Aspose.CAD를 사용하여 C#에서 DWFX 파일을 열고 액세스하는 방법을 성공적으로 배웠습니다. 이 가이드에서는 디렉터리 설정부터 CAD 파일 로드, 구성 및 저장까지 필수 단계를 다루었습니다.

## FAQ

### Q1: Aspose.CAD for .NET은 모든 DWFX 파일과 호환됩니까?

A1: .NET용 Aspose.CAD는 DWFX를 포함한 광범위한 CAD 형식을 지원합니다. 그러나 특정 호환성 세부 정보는 설명서를 확인하는 것이 좋습니다.

### Q2: Aspose.CAD for .NET 문서는 어디서 찾을 수 있나요?

 A2: 문서를 사용할 수 있습니다.[여기](https://reference.aspose.com/cad/net/).

### Q3: 구매하기 전에 Aspose.CAD for .NET을 사용해 볼 수 있나요?

 A3: 예, 무료 평가판을 다운로드할 수 있습니다.[여기](https://releases.aspose.com/).

### Q4: Aspose.CAD for .NET에 대한 임시 라이선스는 어떻게 얻나요?

 A4: 임시 라이센스를 얻을 수 있습니다[여기](https://purchase.aspose.com/temporary-license/).

### Q5: 지원이 필요하거나 더 많은 질문이 있습니까?

A5: 다음을 방문하세요.[Aspose.CAD 포럼](https://forum.aspose.com/c/cad/19) 도움을 위해.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
