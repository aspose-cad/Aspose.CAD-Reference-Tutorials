---
date: 2026-03-29
description: 이 단계별 가이드에서 Aspose.CAD for .NET을 사용하여 CAD에서 PDF를 만들고, 캔버스 크기를 설정하며, CAD를
  PDF 또는 TIFF로 내보내는 방법을 배웁니다.
linktitle: Setting Canvas Size and Mode
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: 'CAD에서 PDF 만들기: Aspose.CAD for .NET에서 캔버스 크기 및 모드 설정'
url: /ko/net/cad-features-and-support/setting-canvas-size-and-mode/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD for .NET에서 캔버스 크기 및 모드 설정

## 소개

**CAD 파일에서 PDF 생성**을 하면서 출력 차원을 제어하고 싶으신가요? 이 튜토리얼에서는 캔버스 크기와 모드를 설정하고, CAD 파일을 로드한 뒤 Aspose.CAD for .NET을 사용해 PDF 또는 TIFF로 내보내는 과정을 단계별로 안내합니다. **DXF를 PDF로 변환**하거나 고해상도 도면을 생성하거나 단순히 래스터화 영역을 조정하고자 할 때, 아래 단계가 실무에 바로 적용 가능한 솔루션을 제공합니다.

## 빠른 답변
- **“CAD에서 PDF 생성”이란 무엇인가요?** CAD 도면(e.g., DXF, DWG)을 벡터와 래스터 세부 정보를 보존한 PDF 문서로 변환하는 것입니다.  
- **출력 크기를 제어하는 옵션은?** `CadRasterizationOptions.PageWidth`와 `PageHeight`(캔버스 크기).  
- **TIFF로도 내보낼 수 있나요?** 예 – 동일한 래스터화 설정을 사용해 `TiffOptions`를 지정하면 됩니다.  
- **프로덕션에 라이선스가 필요합니까?** 상업용 라이선스가 필요합니다; 무료 체험판을 이용할 수 있습니다.  
- **지원되는 .NET 버전은?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.

## “CAD에서 PDF 생성”이란?
CAD에서 PDF를 생성한다는 것은 CAD 도면을 페이지 기반 형식(PDF)으로 렌더링하여 CAD 소프트웨어 없이도 보기, 인쇄, 공유할 수 있게 하는 것을 의미합니다. Aspose.CAD가 무거운 작업을 처리해 주며, 캔버스 크기, 스케일링, 출력 형식을 정의할 수 있습니다.

## CAD에서 PDF를 만들 때 캔버스 크기를 설정해야 하는 이유
캔버스 크기를 설정하면 최종 PDF 또는 TIFF의 해상도와 차원을 정확히 제어할 수 있습니다. 특히 다음과 같은 경우에 유용합니다.
- 특정 용지 크기로 인쇄할 도면을 준비할 때.  
- 웹 미리보기를 위한 썸네일 또는 고해상도 이미지를 생성할 때.  
- 여러 문서에 걸쳐 일관된 레이아웃을 유지하고자 할 때.

## 사전 준비

- Aspose.CAD 라이브러리: [Aspose.CAD 웹사이트](https://releases.aspose.com/cad/net/)에서 Aspose.CAD 라이브러리를 다운로드하고 설치합니다.  
- 개발 환경: 머신에 .NET 개발 환경이 구성되어 있는지 확인합니다.  
- 샘플 CAD 파일: 이 튜토리얼에서는 샘플 DXF 파일을 사용합니다. 파일은 [Aspose.CAD 문서](https://reference.aspose.com/cad/net/)에서 찾을 수 있습니다.

## 네임스페이스 가져오기

CAD 처리를 위해 필요한 네임스페이스를 가져옵니다:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## 사용자 지정 캔버스 크기로 CAD에서 PDF 만들기

### 단계 1: CAD 파일 로드

먼저 **CAD 파일을 로드**합니다(e.g., DXF). 이 단계에서 CAD 파일을 메모리의 `Image` 객체로 불러옵니다.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

using (Image image = Image.Load(sourceFilePath))
{
    // Your code for further steps will go here
}
```

### 단계 2: CadRasterizationOptions 생성

`CadRasterizationOptions` 인스턴스를 만들고 캔버스 크기를 정의합니다. `PageWidth`와 `PageHeight` 속성을 사용해 **캔버스 크기**를 정확히 지정할 수 있습니다.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
rasterizationOptions.AutomaticLayoutsScaling = true;
rasterizationOptions.NoScaling = false;
```

### 단계 3: PdfOptions 생성 (CAD를 PDF로 내보내기)

래스터화 설정을 `PdfOptions` 객체에 연결합니다. 이 구성으로 **CAD를 PDF로 내보내기** 시 사용자 지정 캔버스를 적용할 수 있습니다.

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

### 단계 4: PDF로 내보내기 (DXF를 PDF로 변환)

이제 이미지를 PDF로 저장합니다. 이 단계는 설정한 옵션을 사용해 **CAD에서 PDF 생성**을 수행합니다.

```csharp
image.Save(MyDir + "result_out.pdf", pdfOptions);
```

### 단계 5: TiffOptions 생성 (CAD를 TIFF로 내보내기)

래스터 이미지가 필요하다면 `TiffOptions`를 구성합니다. 동일한 래스터화 옵션을 재사용하므로 **CAD를 TIFF로 내보내기** 시 캔버스 크기가 유지됩니다.

```csharp
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.VectorRasterizationOptions = rasterizationOptions;
```

### 단계 6: TIFF로 내보내기

마지막으로 도면을 TIFF 파일로 저장합니다.

```csharp
image.Save(MyDir + "result_out.tiff", tiffOptions);
```

## 일반적인 문제와 해결책

- **캔버스가 잘려 보임** – `AutomaticLayoutsScaling`이 `true`이고 `NoScaling`이 `false`인지 확인하여 도면이 캔버스에 맞게 스케일링되도록 합니다.  
- **저해상도 PDF** – `PageWidth`/`PageHeight`를 늘리거나 `CadRasterizationOptions`의 `Resolution`을 높입니다.  
- **파일을 찾을 수 없음 오류** – `MyDir`이 유효한 디렉터리를 가리키고 DXF 파일 이름이 정확히 일치하는지 확인합니다.

## 자주 묻는 질문

### Q1: Aspose.CAD를 다른 .NET 라이브러리와 함께 사용할 수 있나요?
A1: 예, Aspose.CAD는 다른 .NET 라이브러리와 원활히 통합되어 CAD 조작 기능을 확장합니다.

### Q2: Aspose.CAD의 무료 체험판이 있나요?
A2: 예, 무료 체험판으로 Aspose.CAD 기능을 체험할 수 있습니다. 시작하려면 [여기](https://releases.aspose.com/)를 방문하세요.

### Q3: Aspose.CAD 지원은 어떻게 받을 수 있나요?
A3: 지원 및 토론은 [Aspose.CAD 포럼](https://forum.aspose.com/c/cad/19)에서 확인하세요.

### Q4: Aspose.CAD에 대한 포괄적인 문서는 어디서 찾을 수 있나요?
A4: 자세한 정보와 예제는 [Aspose.CAD 문서](https://reference.aspose.com/cad/net/)를 참고하세요.

### Q5: Aspose.CAD for .NET을 구매하려면 어떻게 해야 하나요?
A5: 구매는 [구매 페이지](https://purchase.aspose.com/buy)에서 진행할 수 있습니다.

**추가 Q&A**

**Q: 다중 페이지 CAD 도면을 하나의 PDF로 내보낼 수 있나요?**  
A: 예. `CadRasterizationOptions`의 `PageCount`를 설정하면 라이브러리가 페이지들을 하나의 PDF로 결합합니다.

**Q: 캔버스 크기가 벡터 데이터 품질에 영향을 미치나요?**  
A: 벡터 데이터는 해상도에 독립적이며, 캔버스 크기는 래스터화된 요소와 이미지 해상도에만 영향을 줍니다.

---

**마지막 업데이트:** 2026-03-29  
**테스트 환경:** Aspose.CAD 24.11 for .NET  
**작성자:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}