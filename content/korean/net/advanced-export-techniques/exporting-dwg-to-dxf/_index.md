---
title: C#에서 DWG를 DXF 형식으로 내보내기 - Aspose.CAD Tutorial
linktitle: C#에서 DWG를 DXF 형식으로 내보내기
second_title: Aspose.CAD .NET - CAD 및 BIM 파일 형식
description: Aspose.CAD를 사용하여 C#에서 CAD 파일 조작을 잠금 해제합니다. DWG를 DXF로 쉽게 내보내는 방법을 알아보세요. 원활한 통합을 위한 단계별 가이드를 따르세요.
type: docs
weight: 10
url: /ko/net/advanced-export-techniques/exporting-dwg-to-dxf/
---
## 소개

CAD 파일 조작을 위한 강력한 솔루션을 찾고 있는 .NET 개발자라면 Aspose.CAD가 가장 적합한 도구입니다. 이 단계별 튜토리얼에서는 Aspose.CAD와 함께 C#을 사용하여 DWG 파일을 DXF 형식으로 내보내는 과정을 안내합니다.

## 전제 조건

튜토리얼을 시작하기 전에 다음 전제 조건이 충족되었는지 확인하세요.

1.  Aspose.CAD 라이브러리: Aspose.CAD 라이브러리를 다운로드하여 설치하세요.[이 링크](https://releases.aspose.com/cad/net/).

2. 개발 환경: Visual Studio와 같은 C# 개발 환경을 설정합니다.

3. 샘플 DWG 파일: 내보낼 샘플 DWG 파일을 준비합니다. 이 튜토리얼에서는 "Your Document Directory" 디렉터리에 있는 "Line.dwg"라는 파일을 사용합니다.

## 네임스페이스 가져오기

C# 프로젝트에서 Aspose.CAD 작업에 필요한 네임스페이스를 포함합니다.

```csharp
using Aspose.CAD.FileFormats.Cad;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## 1단계: DWG 파일 로드

C# 애플리케이션에 DWG 파일을 로드하는 것부터 시작합니다. 이를 달성하기 위한 코드 조각은 다음과 같습니다.

```csharp
string MyDir = "Your Document Directory";
string inputFile = MyDir + "Line.dwg";
using (var cadImage = (CadImage)Image.Load(inputFile))
{
    //추가 단계를 위한 코드가 여기에 표시됩니다.
}
```

## 2단계: DXF로 저장

DWG 파일이 로드되면 다음 단계는 DXF 파일로 저장하는 것입니다. 이전 using 블록 내에 다음 코드를 추가합니다.

```csharp
string outFile = MyDir + "Line_19.2.dxf";
cadImage.Save(outFile);
```

## 결론

축하해요! C#에서 Aspose.CAD를 사용하여 DWG 파일을 DXF 형식으로 내보냈습니다. 이 간단하면서도 강력한 프로세스는 응용 프로그램에서 CAD 파일을 조작할 수 있는 가능성의 세계를 열어줍니다.

## FAQ

### Q1: Aspose.CAD는 최신 CAD 파일 형식과 호환됩니까?

A1: 예, Aspose.CAD는 최신 CAD 파일 형식과의 호환성을 보장하기 위해 정기적으로 업데이트됩니다.

### Q2: 상업용 프로젝트에 Aspose.CAD를 사용할 수 있나요?

 A2: 물론이죠! Aspose.CAD에는 개인용 및 상업용 라이센스 옵션이 함께 제공됩니다. 방문하다[이 링크](https://purchase.aspose.com/buy) 자세한 내용은.

### Q3: 무료 평가판이 제공됩니까?

 A3: 예, 무료 평가판을 통해 Aspose.CAD를 탐색할 수 있습니다. 방문하다[이 링크](https://releases.aspose.com/) 시작하려면.

### Q4: Aspose.CAD에 대한 자세한 문서는 어디서 찾을 수 있나요?

 A4: 다음 문서를 참조하세요.[이 링크](https://reference.aspose.com/cad/net/) 종합적인 안내를 위해.

### Q5: 도움이 필요하거나 구체적인 질문이 있습니까?

 A5: Aspose.CAD 커뮤니티 포럼을 방문하세요.[여기](https://forum.aspose.com/c/cad/19)전문가 지원 및 지역 사회 지원을 위해.