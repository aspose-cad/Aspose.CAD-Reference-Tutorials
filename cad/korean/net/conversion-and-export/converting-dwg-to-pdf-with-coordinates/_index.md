---
date: 2026-04-03
description: Aspose.CAD를 사용하여 C#에서 뷰포트를 설정하고 DWG를 PDF로 변환하는 방법을 배워보세요. 이 DWG to PDF
  튜토리얼은 좌표와 함께 정확한 내보내기를 보여줍니다.
keywords:
- how to set viewport
- dwg to pdf tutorial
- convert dwg to pdf c#
linktitle: C#에서 좌표와 함께 DWG를 PDF로 변환하기
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: C#에서 좌표와 함께 DWG를 PDF로 변환할 때 뷰포트 설정 방법 - Aspose.CAD 튜토리얼
url: /ko/net/conversion-and-export/converting-dwg-to-pdf-with-coordinates/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# C#에서 좌표와 함께 DWG를 PDF로 변환하기 - Aspose.CAD 튜토리얼

## 소개

Aspose.CAD for .NET을 사용하여 지정된 좌표로 DWG 파일을 PDF로 변환하면서 **뷰포트 설정 방법**에 대한 포괄적인 튜토리얼에 오신 것을 환영합니다. 뷰포트를 제어하면 필요한 영역과 정확히 일치하는 픽셀 완벽 PDF를 얻을 수 있어 건축 도면, 평면도 미리보기 또는 모든 BIM 워크플로에 이상적입니다.

## 빠른 답변
- **“set viewport”가 무엇을 의미하나요?** CAD 도면을 래스터화하는 동안 보이는 영역과 스케일을 정의합니다.  
- **어떤 라이브러리가 변환을 처리하나요?** Aspose.CAD for .NET.  
- **라이선스가 필요합니까?** 평가용으로는 무료 체험판을 사용할 수 있지만, 실제 운영을 위해서는 상용 라이선스가 필요합니다.  
- **지원되는 플랫폼은?** .NET 5/6/7 또는 .NET Framework 4.6+와 함께 Windows, Linux, macOS.  
- **일반적인 구현 시간은?** 기본 변환의 경우 약 10‑15분 정도 소요됩니다.

## 사전 요구 사항

시작하기 전에 다음 사전 요구 사항을 확인하십시오:

- **Aspose.CAD 라이브러리** – .NET용 Aspose.CAD 라이브러리를 다운로드하고 설치합니다. 라이브러리는 [here](https://releases.aspose.com/cad/net/)에서 찾을 수 있습니다.
- **개발 환경** – Visual Studio, Rider 또는 .NET 개발을 지원하는 모든 IDE.
- **DWG 파일** – 변환할 DWG 파일을 준비합니다. 제공된 예제 파일이나 사용자 정의 DWG 파일을 사용할 수 있습니다.

## 정확한 PDF 내보내기를 위한 뷰포트 설정 방법

뷰포트를 설정하는 것은 렌더링하려는 도면의 정확한 영역을 정의할 수 있게 하는 핵심 단계입니다. 아래 코드에서는 새로운 `CadVportTableObject`를 생성하고, 좌상단 좌표로 위치를 지정한 뒤, 너비, 높이 및 종횡비를 계산합니다. 이것이 **뷰포트 설정 방법** 구현이며, 변환의 나머지 부분을 주도합니다.

## 네임스페이스 가져오기

C# 프로젝트에서 필요한 네임스페이스를 가져옵니다:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadParameters;
using Aspose.CAD.FileFormats.Cad.CadTables;
using Aspose.CAD.ImageOptions;
```

코드를 단계별 가이드로 나누어 더 잘 이해할 수 있도록 하겠습니다:

## 단계 1: 문서 디렉터리 정의

```csharp
string MyDir = "Your Document Directory";
```

## 단계 2: 원본 DWG 파일 경로 설정

```csharp
string sourceFilePath = MyDir + "visualization_-_conference_room.dwg";
```

## 단계 3: DWG 파일 로드 및 래스터화 옵션 구성

```csharp
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
    rasterizationOptions.Layouts = new string[] { "Model" };
    rasterizationOptions.NoScaling = true;
```

## 단계 4: 좌표 및 뷰포트 정의

여기서는 실제로 **뷰포트를 설정** (뷰포트 설정 방법)하여 내보내려는 영역의 좌상단 모서리, 너비 및 높이를 지정합니다.

```csharp
    Point topLeft = new Point(500, 1000);
    double width = 3108;
    double height = 2489;

    CadVportTableObject newView = new CadVportTableObject();
    newView.Name = new CadStringParameter();
    newView.Name.Init("*Active");
    newView.CenterPoint.X = topLeft.X + width / 2f;
    newView.CenterPoint.Y = topLeft.Y - height / 2f;
    newView.ViewHeight.Value = height;
    newView.ViewAspectRatio.Value = width / height;
```

## 단계 5: 뷰포트 설정 적용

```csharp
    for (int i = 0; i < cadImage.ViewPorts.Count; i++)
    {
        CadVportTableObject currentView = (CadVportTableObject)(cadImage.ViewPorts[i]);
        if (cadImage.ViewPorts.Count == 1 || string.Equals(currentView.Name.Value.ToLowerInvariant(), "*active"))
        {
            cadImage.ViewPorts[i] = newView;
            break;
        }
    }
```

## 단계 6: PDF 옵션 구성 및 내보내기

이제 모든 것을 연결하고 방금 준비한 래스터화 옵션을 사용하여 **DWG를 PDF로 변환**합니다.

```csharp
    Aspose.CAD.ImageOptions.PdfOptions pdfOptions = new Aspose.CAD.ImageOptions.PdfOptions();
    pdfOptions.VectorRasterizationOptions = rasterizationOptions;

    MyDir = MyDir + "ConvertDWGToPDFBySupplyingCoordinates_out.pdf";
    cadImage.Save(MyDir, pdfOptions);
}
```

## 단계 7: 성공 메시지 표시

```csharp
Console.WriteLine("\nThe DWG file exported successfully to PDF.\nFile saved at " + MyDir);
```

## 일반적인 사용 사례

- **건설 문서화** – 특정 평면도 구역의 인쇄 가능한 PDF를 생성합니다.  
- **BIM 협업** – 충돌 감지를 위해 관심 영역만 내보냅니다.  
- **클라이언트 프레젠테이션** – 전체 도면을 노출하지 않고 선택된 방이나 입면의 깔끔한 PDF를 제공합니다.

## 결론

축하합니다! 정확한 좌표로 **DWG를 PDF로 변환**하고 Aspose.CAD for .NET을 사용하여 **뷰포트 설정 방법**을 배웠습니다. 이 **dwg to pdf tutorial**은 **dwg에서 pdf 생성** 및 **dwg를 pdf c#으로 내보내기**를 보여주며 출력 영역을 완전히 제어할 수 있습니다.

## FAQ

### Q1: Aspose.CAD를 다른 CAD 파일 형식과 함께 사용할 수 있나요?

A1: 네, Aspose.CAD는 DWG, DXF, DWF 등 다양한 CAD 형식을 지원합니다.

### Q2: 변환 과정에서 오류를 어떻게 처리할 수 있나요?

A2: 예외를 포착하고 관리하기 위해 try‑catch 블록을 사용하여 오류 처리 메커니즘을 구현합니다.

### Q3: Aspose.CAD가 Windows와 Linux 환경 모두에 적합한가요?

A3: 네, Aspose.CAD는 Windows와 Linux 플랫폼 모두와 호환됩니다.

### Q4: PDF 출력물을 추가로 맞춤 설정할 수 있나요?

A4: 물론입니다! Aspose.CAD가 제공하는 다양한 옵션을 살펴보면 PDF 출력을 특정 요구 사항에 맞게 조정할 수 있습니다.

### Q5: 추가 지원이나 커뮤니티 토론을 어디서 찾을 수 있나요?

A5: 커뮤니티 지원 및 토론을 위해 [Aspose.CAD Forum](https://forum.aspose.com/c/cad/19)을 방문하십시오.

## 추가 자주 묻는 질문

**Q: 이 방법이 대용량 DWG 파일(수백 MB)에도 작동하나요?**  
A: 네. 래스터화는 페이지별로 수행되며, `rasterizationOptions`(예: `Resolution`)를 조정하여 품질과 메모리 사용량의 균형을 맞출 수 있습니다.

**Q: 여러 뷰포트를 별도의 PDF 페이지로 내보낼 수 있나요?**  
A: `cadImage.ViewPorts`를 반복하면서 각각을 활성화하고 각 페이지에 대해 `Save`를 호출한 다음, Aspose.PDF를 사용해 PDF를 병합할 수 있습니다.

**Q: 생성된 PDF에 워터마크를 추가할 수 있나요?**  
A: PDF를 저장한 후 Aspose.PDF로 다시 열어 텍스트 또는 이미지 워터마크를 적용한 뒤 사용자에게 제공할 수 있습니다.

---

**Last Updated:** 2026-04-03  
**Tested With:** Aspose.CAD 24.11 for .NET  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}