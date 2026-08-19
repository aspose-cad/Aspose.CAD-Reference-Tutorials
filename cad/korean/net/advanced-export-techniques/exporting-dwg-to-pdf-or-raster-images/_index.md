---
date: 2026-03-16
description: Aspose.CAD for .NET를 사용하여 DWG를 PDF 또는 래스터 이미지로 변환하는 방법을 배워보세요. 이 단계별
  CAD to PDF 튜토리얼에서는 DWG를 PNG와 같은 이미지 형식으로 내보내는 방법과 DWG를 이미지 파일로 효율적으로 내보내는 방법을 다룹니다.
linktitle: Exporting DWG to PDF or Raster Images
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Aspose.CAD for .NET를 사용하여 DWG를 PDF 및 래스터 이미지로 변환하는 방법
url: /ko/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DWG를 PDF 또는 래스터 이미지로 내보내기 - Aspose.CAD 가이드

## 소개

.NET 애플리케이션에서 직접 **DWG를 PDF**(또는 PNG와 같은 래스터 형식)로 변환해야 한다면, 여기가 바로 정답입니다. 이 튜토리얼에서는 Aspose.CAD for .NET을 사용하여 변환을 수행하는 데 필요한 정확한 단계들을 안내하고, 라이브러리가 왜 좋은 선택인지 설명하며, 몇 줄의 코드만으로 PDF와 이미지 출력 모두를 처리하는 방법을 보여드립니다.

## 빠른 답변
- **DWG 변환을 처리하는 라이브러리는?** Aspose.CAD for .NET  
- **DWG를 PDF뿐만 아니라 PNG로도 내보낼 수 있나요?** 예 – 동일한 래스터화 옵션이 두 형식 모두에 적용됩니다.  
- **개발에 라이선스가 필요합니까?** 테스트용으로는 무료 체험판을 사용할 수 있으며, 프로덕션에서는 상업용 라이선스가 필요합니다.  
- **지원되는 .NET 버전은?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **단위 변환이 자동으로 처리되나요?** 코드에 표시된 대로 단위 시스템을 수동으로 정의할 수 있습니다 (미터법 또는 영국식).

## DWG를 PDF로 변환한다는 것은 무엇인가요?

DWG를 PDF로 변환한다는 것은 CAD 도면(DWG)을 가져와서 휴대가 가능하고 보기 전용인 문서(PDF)로 렌더링하는 것을 의미합니다. 이는 CAD 소프트웨어가 없는 이해관계자와 설계를 공유하거나, 인쇄 가능한 문서를 만들거나, 보편적으로 읽을 수 있는 형식으로 도면을 보관하는 데 유용합니다.

## 왜 이 변환에 Aspose.CAD를 사용해야 할까요?

- **외부 종속성 없음** – 라이브러리가 완전히 관리되는 코드에서 동작합니다.  
- **고충실도** – 레이어, 선 굵기 및 레이아웃 정보를 유지합니다.  
- **내장 래스터 옵션** – 단일 구성 객체로 PNG, JPEG, BMP 등으로 내보낼 수 있습니다.  
- **크로스 플랫폼** – .NET Core와 함께 Windows, Linux, macOS에서 동작합니다.

## 전제 조건

튜토리얼을 시작하기 전에 다음 사항이 준비되어 있는지 확인하세요:

- .NET 프로그래밍에 대한 기본 이해.  
- Aspose.CAD for .NET 라이브러리가 설치되어 있어야 합니다. 아직 설치하지 않았다면 [여기](https://releases.aspose.com/cad/net/)에서 다운로드하세요.  
- .NET 개발을 위한 선호하는 통합 개발 환경(IDE)이 설정되어 있어야 합니다.

## 네임스페이스 가져오기

.NET 프로젝트에서 필요한 네임스페이스를 가져오면서 시작해 보겠습니다. 이렇게 하면 코드에서 Aspose.CAD 기능에 접근할 수 있습니다.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
```

## 단계 1: DWG 파일 로드

변환하려는 DWG 파일을 로드합니다. `"Your Document Directory"`를 DWG 파일이 위치한 경로로 교체하세요.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Bottom_plate.dwg";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Your code for loading DWG goes here
}
```

## 단계 2: PDF 내보내기 설정 (DWG를 PDF로 내보내는 방법)

이제 PDF 내보내기 설정을 구성합니다. 이 예제는 레이아웃을 지정하고 단위 변환을 처리하는 방법을 보여줍니다.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.Layouts = new string[] { "Model" };

// Check and define the unit system
bool currentUnitIsMetric = false;
double currentUnitCoefficient = 1.0;
DefineUnitSystem(cadImage.UnitType, out currentUnitIsMetric, out currentUnitCoefficient);

// Your code for setting up PDF export goes here
```

## 단계 3: PDF로 내보내기

구성된 설정을 사용하여 PDF로 내보냅니다.

```csharp
PdfOptions pdfOptions = new PdfOptions
{
    VectorRasterizationOptions = rasterizationOptions
};

cadImage.Save(outPath, pdfOptions);
```

## 단계 4: 래스터 이미지로 내보내기 (DWG를 이미지로 내보내기)

PNG와 같은 래스터 이미지로 내보내는 기능을 확장합니다.

```csharp
// A4 size at 300 DPI - 2480 x 3508
rasterizationOptions.PageHeight = 3508;
rasterizationOptions.PageWidth = 2480;

PngOptions pngOptions = new PngOptions
{
    VectorRasterizationOptions = rasterizationOptions
};

cadImage.Save(outPath.Replace("pdf", "png"), pngOptions);
```

## 일반적인 문제 및 해결책

| 문제 | 발생 원인 | 해결 방법 |
|------|----------|----------|
| **PDF에서 빈 페이지** | 레이아웃이 올바르게 지정되지 않음 | `rasterizationOptions.Layouts`에 올바른 레이아웃 이름(예: `"Model"`)이 포함되어 있는지 확인하세요. |
| **잘못된 차원** | DPI 또는 페이지 크기 불일치 | `CadRasterizationOptions`에서 `PageHeight`, `PageWidth`, DPI 값을 조정하세요. |
| **단위가 잘못 표시됨** | 단위 변환이 정의되지 않음 | `cadImage.UnitType`을 기반으로 `DefineUnitSystem`을 사용해 `currentUnitIsMetric` 및 `currentUnitCoefficient`를 설정하세요. |
| **라이선스 예외** | 체험판 제한 | `Image.Load`를 호출하기 전에 임시 또는 영구 라이선스를 적용하세요. |

## 자주 묻는 질문

### Q1: 상업 프로젝트에서 Aspose.CAD for .NET을 사용할 수 있나요?
A1: 예, 사용할 수 있습니다. 라이선스 상세 정보는 [purchase.aspose.com/buy](https://purchase.aspose.com/buy)에서 확인하세요.

### Q2: 무료 체험판을 이용할 수 있나요?
A2: 물론입니다! 무료 체험판은 [여기](https://releases.aspose.com/)에서 받으세요.

### Q3: Aspose.CAD for .NET에 대한 지원은 어떻게 받을 수 있나요?
A3: 커뮤니티 지원은 [Aspose.CAD 포럼](https://forum.aspose.com/c/cad/19)에서 확인하세요.

### Q4: 테스트 용도로 임시 라이선스를 받을 수 있나요?
A4: 예, 임시 라이선스는 [여기](https://purchase.aspose.com/temporary-license/)에서 받을 수 있습니다.

### Q5: 자세한 문서는 어디서 찾을 수 있나요?
A5: 문서는 [Aspose.CAD](https://reference.aspose.com/cad/net/)에서 확인할 수 있습니다.

### Q6: 고품질로 **CAD를 PNG로 저장**하려면 어떻게 해야 하나요?
A6: `CadRasterizationOptions`에서 원하는 픽셀 크기로 `PageHeight`와 `PageWidth`를 설정하고 DPI를 300 이상으로 선택하세요.

### Q7: 원본 파일에 여러 레이아웃이 포함된 경우 **DWG를 변환하는** 가장 좋은 방법은?
A7: 내보내려는 모든 레이아웃 이름을 `rasterizationOptions.Layouts`에 채운 뒤, 각 레이아웃을 순회하며 원하는 출력 형식마다 `Save`를 호출하세요.

---

**Last Updated:** 2026-03-16  
**Tested With:** Aspose.CAD 24.11 for .NET  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}