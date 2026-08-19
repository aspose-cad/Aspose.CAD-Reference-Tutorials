---
date: 2026-03-24
description: Aspose.CAD for .NET를 사용해 DGN V7의 3D 지원을 포함한 DGN을 PDF(및 PNG)로 변환하는 방법을
  단계별로 배워보세요.
linktitle: 3D Support for DGN V7
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Aspose.CAD for .NET을 사용하여 DGN을 PDF(3D 지원)로 변환
url: /ko/net/cad-features-and-support/3d-support-for-dgn-v7/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD for .NET를 사용한 DGN을 PDF(3D 지원)로 변환

## 소개

현대 CAD 워크플로에서 **DGN을 PDF로 변환**하고 3‑D 기하학을 빠르게 유지하는 것은 필수적입니다. 문서를 생성하거나, 비‑CAD 이해관계자와 설계를 공유하거나, 프로젝트를 보관할 때 Aspose.CAD for .NET은 DGN V7 파일을 고품질 PDF(및 PNG) 출력으로 변환하는 신뢰할 수 있는 방법을 제공합니다. 이 튜토리얼에서는 3D 지원을 활성화하고 DGN 파일에서 PDF를 생성하는 정확한 단계를 단계별로 안내합니다.

## 빠른 답변
- **이 튜토리얼이 다루는 내용은?** Aspose.CAD for .NET을 사용하여 3D 지원을 활성화하고 DGN V7을 PDF로 변환하는 방법.  
- **주요 출력 형식은?** PDF(선택적으로 PNG 내보내기 가능).  
- **라이선스가 필요한가요?** 무료 체험판으로 테스트할 수 있으며, 실제 운영 환경에서는 상용 라이선스가 필요합니다.  
- **지원되는 .NET 버전은?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **구현 소요 시간은?** 기본 변환의 경우 약 10‑15분 정도 소요됩니다.

## “convert DGN to PDF”란 무엇인가요?

DGN을 PDF로 변환한다는 것은 MicroStation DGN 파일에 저장된 벡터 데이터를 특수 CAD 소프트웨어 없이도 모든 장치에서 볼 수 있는 휴대용 문서 형식으로 렌더링하는 것을 의미합니다. Aspose.CAD의 3‑D 래스터화 엔진을 사용하면 변환 시 레이아웃, 색상 및 깊이 정보를 보존하여 정확한 시각적 표현을 제공합니다.

## 왜 Aspose.CAD를 사용해야 할까요?

- **Full 3‑D rasterization** – 깊이와 레이아웃 정보를 유지합니다.  
- **No external dependencies** – 순수 .NET 라이브러리이며 MicroStation이 필요 없습니다.  
- **Multiple output formats** – PDF, PNG, JPEG, TIFF 등 다양한 형식을 지원합니다(보조 키워드 *convert dgn to png*도 기본 제공).  
- **Cross‑platform** – Windows, Linux, macOS에서 모두 동작합니다.

## 사전 요구 사항

시작하기 전에 다음을 준비하세요:

- Aspose.CAD for .NET이 설치되어 있어야 합니다. [Aspose.CAD for .NET 다운로드 페이지](https://releases.aspose.com/cad/net/)에서 다운로드할 수 있습니다.  
- 처리하려는 유효한 DGN V7 파일.  
- .NET 개발 환경(Visual Studio, VS Code 또는 CLI). 설치 방법은 [.NET 문서](https://docs.microsoft.com/en-us/dotnet/core/install/)에 나와 있습니다.

## 네임스페이스 가져오기

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

이 네임스페이스들을 통해 핵심 Aspose.CAD 클래스와 표준 .NET 유틸리티에 접근할 수 있습니다.

## 단계 1: 환경 설정

소스 DGN 파일이 위치한 경로와 출력 PDF를 저장할 경로를 정의합니다.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";
```

> **Pro tip:** 플랫폼에 독립적인 경로 구성을 위해 `Path.Combine`을 사용하세요.

## 단계 2: DGN 파일 로드

`Image.Load`를 사용해 파일을 로드하고 `DgnImage` 인스턴스를 생성합니다. 이 단계에서 CAD 데이터를 래스터화할 준비를 합니다.

```csharp
using (DgnImage dgnImage = (DgnImage)Image.Load(sourceFilePath))
{
    // Code snippet continues...
}
```

## 단계 3: 내보내기 옵션 구성

`PdfOptions`와 `CadRasterizationOptions`를 설정합니다. 여기서 페이지 크기, 배경 및 내보낼 레이아웃(뷰)을 제어합니다.

```csharp
var options = new PdfOptions
{
    VectorRasterizationOptions = new CadRasterizationOptions
    {
        PageWidth = 1500,
        PageHeight = 1500,
        CenterDrawing = true,
        AutomaticLayoutsScaling = true,
        BackgroundColor = Color.Black,
        Layouts = new string[] { "1", "2", "3", "9" } // Export specific views
    }
};
```

PNG로 변환하려면 **convert DGN to PNG**가 필요할 경우 `PdfOptions`를 `PngOptions`로 교체하고 동일한 래스터화 설정을 유지하면 됩니다.

## 단계 4: 결과 저장

마지막으로 렌더링된 출력을 원하는 위치에 기록합니다.

```csharp
string outFile = "Your Output Directory"; // Specify the output directory
dgnImage.Save(outFile, options);
```

실행 후 원본 3‑D DGN 도면을 충실히 재현한 PDF 파일(옵션을 변경한 경우 PNG 파일)을 찾을 수 있습니다.

## 일반적인 문제 및 팁

- **Missing layouts:** `Layouts`에 지정한 레이아웃 이름이 DGN 파일에 존재하는지 확인하세요. 일치하지 않으면 무시됩니다.  
- **Large files:** 메모리 사용량이 급증하는 것을 방지하려면 `PageWidth`/`PageHeight` 값을 점진적으로 늘리세요.  
- **Color accuracy:** 배경이 어둡게 보이면 `BackgroundColor`가 원하는 값(예: `Color.White`)으로 설정되어 있는지 확인하세요.

## 결론

이제 Aspose.CAD for .NET을 사용해 전체 3‑D 지원을 갖춘 **DGN을 PDF로 변환**하는 방법을 마스터했습니다. 이 워크플로는 자동화 파이프라인, 데스크톱 유틸리티 또는 웹 서비스에 통합되어 모든 사용자에게 CAD 시각화를 제공할 수 있습니다.

## FAQ

### Q1: 이 방법으로 여러 DGN 파일을 동시에 처리할 수 있나요?

A1: 네, 코드를 수정하여 루프 안에서 여러 파일을 처리하거나 배치 처리 시스템의 일부로 사용할 수 있습니다.

### Q2: Aspose.CAD for .NET이 지원하는 다른 내보내기 형식은 무엇인가요?

A2: Aspose.CAD for .NET은 PDF, PNG, JPG 등 다양한 형식을 지원합니다. 자세한 내용은 [문서](https://reference.aspose.com/cad/net/)를 참고하세요.

### Q3: Aspose.CAD for .NET은 최신 .NET Core 버전과 호환되나요?

A3: 네, 최신 .NET Core 버전과 호환되도록 설계되었습니다. 환경에 맞는 적절한 버전을 설치하세요.

### Q4: 내 특정 요구 사항에 맞게 내보내기 설정을 더 세부적으로 조정할 수 있나요?

A4: 물론입니다! 제공된 코드는 시작점에 불과합니다. 추가 옵션 및 구성은 [Aspose.CAD 문서](https://reference.aspose.com/cad/net/)에서 확인할 수 있습니다.

### Q5: Aspose.CAD for .NET에 대한 도움을 받거나 경험을 공유하려면 어디에 가면 되나요?

A5: 다른 개발자와 소통하고 지원을 받으려면 [포럼](https://forum.aspose.com/c/cad/19)에 참여하세요.

---

**Last Updated:** 2026-03-24  
**Tested With:** Aspose.CAD 24.11 for .NET  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}