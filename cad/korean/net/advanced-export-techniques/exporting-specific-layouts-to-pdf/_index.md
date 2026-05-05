---
date: 2026-03-13
description: Aspose.CAD for .NET를 사용하여 CAD 래스터화 옵션을 설정하고 특정 DWG 레이아웃을 PDF로 내보내는 방법을
  배우세요 – CAD 파일에서 PDF를 생성하기 위한 최종 가이드.
linktitle: Exporting Specific Layouts to PDF
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: CAD 래스터화 옵션 설정 – 특정 레이아웃을 PDF로 내보내기 - Aspose.CAD 가이드
url: /ko/net/advanced-export-techniques/exporting-specific-layouts-to-pdf/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 특정 레이아웃을 PDF로 내보내기 - Aspose.CAD 가이드

## 소개

이 튜토리얼에서는 **CAD 래스터화 옵션을 설정하는 방법**을 알아보고, DWG 파일의 단일 레이아웃 또는 여러 레이아웃을 직접 PDF로 내보낼 수 있습니다. Aspose.CAD for .NET은 *dwg to pdf conversion c#* 과정을 간단하게 만들어 주며, 페이지 크기, 해상도 및 레이아웃 선택에 대한 완전한 제어를 제공합니다. 가이드를 끝까지 따라 하면 **CAD 파일에서 PDF 만들기**를 몇 줄의 코드만으로 구현할 수 있습니다.

## 빠른 답변
- **“set cad rasterization options”는 무엇을 하나요?**  
  Aspose.CAD에 벡터 데이터(레이아웃, 레이어, 선 두께)를 래스터화된 PDF 페이지로 렌더링하도록 지시합니다.  
- **DWG 레이아웃을 PDF로 내보내는 메서드는?**  
  `CadRasterizationOptions`가 포함된 `PdfOptions`를 구성한 뒤 `Image.Save`를 사용합니다.  
- **한 번에 여러 레이아웃을 내보낼 수 있나요?**  
  예 – `Layouts` 속성에 레이아웃 이름 배열을 제공하면 됩니다.  
- **프로덕션 사용에 라이선스가 필요합니까?**  
  상업용 라이선스가 필요합니다; 평가용 무료 체험판을 이용할 수 있습니다.  
- **지원되는 .NET 버전은?**  
  .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6 이상.

## “set cad rasterization options”란?
`CadRasterizationOptions`는 CAD 엔터티를 PDF와 같은 래스터 기반 형식으로 변환할 때 래스터화 방식을 제어하는 클래스입니다. 페이지 크기, 레이아웃 선택, 배경 색상 등 속성을 설정함으로써 **export dwg layout to pdf** 작업의 시각적 결과를 지정합니다.

## CAD 래스터화 옵션을 설정해야 하는 이유
- **정밀도** – 원본 CAD 도면에 표시된 선 두께와 스케일을 정확히 유지합니다.  
- **성능** – 필요한 레이아웃만 렌더링해 파일 크기와 처리 시간을 줄입니다.  
- **유연성** – 페이지 너비/높이, DPI, 배경을 조정해 보고서 표준에 맞출 수 있습니다.  

## 사전 요구 사항

코드 작성을 시작하기 전에 다음을 준비하세요:

- **Aspose.CAD for .NET**이 설치되어 있어야 합니다. [여기](https://releases.aspose.com/cad/net/)에서 다운로드할 수 있습니다.  
- .NET 개발 환경(Visual Studio, VS Code 또는 선호하는 IDE).  
- 최소 하나의 레이아웃을 포함한 DWG 파일(예시 파일은 `visualization_-_conference_room.dwg`).

## 네임스페이스 가져오기

.NET 프로젝트에서 Aspose.CAD에 필요한 네임스페이스를 가져옵니다.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## 단계별 가이드

### 단계 1: DWG 파일 로드

먼저 변환하려는 DWG 파일의 경로를 Aspose.CAD에 지정합니다.

```csharp
// The path to the documents directory.
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "visualization_-_conference_room.dwg";

using (Image image = Image.Load(sourceFilePath))
{
    // Your code for further steps goes here.
}
```

### 단계 2: **CadRasterizationOptions** 설정

PDF 페이지 크기와 해상도를 결정하는 래스터화 설정을 구성합니다.

```csharp
// Create an instance of CadRasterizationOptions and set its various properties
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
```

> **프로 팁:** `PageWidth`와 `PageHeight`를 목표 PDF 레이아웃의 크기에 맞게 조정하세요. 값이 클수록 디테일이 증가하지만 파일 크기도 커집니다.

### 단계 3: 레이아웃 이름 지정

Aspose.CAD에 렌더링할 레이아웃을 알려줍니다. `"Layout1"`을 DWG 파일에 실제 존재하는 레이아웃 이름으로 바꾸세요.

```csharp
// Specify desired layout name
rasterizationOptions.Layouts = new string[] { "Layout1" };
```

> **왜 중요한가:** `Layouts` 배열을 제한하면 원하지 않는 시트를 내보내지 않게 되어 **dwg to pdf conversion c#** 작업이 더 빠르고 결과 PDF가 깔끔해집니다.

### 단계 4: `PdfOptions` 생성

래스터화 설정을 PDF 내보내기 옵션에 연결합니다.

```csharp
// Create an instance of PdfOptions
PdfOptions pdfOptions = new PdfOptions();
// Set the VectorRasterizationOptions property
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

### 단계 5: PDF로 내보내기

렌더링된 레이아웃을 PDF 파일로 저장합니다.

```csharp
MyDir = MyDir + "ExportSpecificLayoutToPDF_out.pdf";
// Export the DWG to PDF
image.Save(MyDir, pdfOptions);
```

### 단계 6: 성공 메시지 표시

콘솔에 간단한 출력으로 작업이 성공했음을 확인합니다.

```csharp
// Display success message
Console.WriteLine("\nThe DWG file with a specific layout exported successfully to PDF.\nFile saved at " + MyDir);
```

## 일반적인 문제 및 해결책

| 문제 | 원인 | 해결 방법 |
|------|------|-----------|
| **PDF가 생성되지 않음** | `Layouts` 배열이 DWG에 존재하지 않는 레이아웃 이름과 일치함 | CAD 뷰어로 레이아웃 이름을 확인하고 `Layouts` 속성을 업데이트 |
| **빈 페이지** | `PageWidth`/`PageHeight`가 0이거나 너무 작게 설정됨 | 현실적인 크기(예: 1600 × 1600) 사용하거나 해당 속성을 생략해 Aspose가 자동 계산하도록 함 |
| **스케일링 오류** | 고해상도 출력에 DPI가 설정되지 않음 | 내보내기 전에 `rasterizationOptions.Resolution = 300;` 등 원하는 DPI를 지정 |

## 자주 묻는 질문

**Q: 여러 레이아웃을 동시에 내보낼 수 있나요?**  
A: 예, 단계 3에서 `Layouts` 배열에 원하는 모든 레이아웃 이름을 포함하면 됩니다. 예: `new string[] { "Layout1", "Layout2" }`.

**Q: Aspose.CAD가 다른 CAD 파일 형식을 지원하나요?**  
A: 물론입니다. DWG, DXF, DWF, DGN 등 다양한 형식을 지원합니다.

**Q: 페이지 크기 외에 PDF 출력 설정을 조정하려면?**  
A: `CadRasterizationOptions`의 `Resolution`, `BackgroundColor`, `DrawType` 등 추가 속성을 활용해 결과를 미세 조정할 수 있습니다.

**Q: 추가 Aspose.CAD 문서는 어디서 찾을 수 있나요?**  
A: 자세한 API 레퍼런스와 예제는 [documentation](https://reference.aspose.com/cad/net/)을 참고하세요.

**Q: 무료 체험판을 이용할 수 있나요?**  
A: 예, 무료 체험판은 [여기](https://releases.aspose.com/)에서 받을 수 있습니다.

## 결론

이제 **CAD 래스터화 옵션을 설정**하고 이를 활용해 Aspose.CAD for .NET으로 **특정 DWG 레이아웃을 PDF로 내보내는** 방법을 익혔습니다. 이 접근 방식은 변환 과정을 정밀하게 제어할 수 있게 해 주며, C# 애플리케이션에 CAD‑to‑PDF 기능을 빠르고 안정적으로 통합할 수 있습니다.

---

**마지막 업데이트:** 2026-03-13  
**테스트 환경:** Aspose.CAD 24.11 for .NET  
**작성자:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}