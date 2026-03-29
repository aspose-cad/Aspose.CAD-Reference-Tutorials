---
date: 2026-03-29
description: Aspose.CAD for .NET를 사용하여 CAD 래스터화 옵션을 구성하고 3D 지원이 포함된 DGN을 PDF로 내보내는
  방법을 배우세요.
linktitle: Support of 3D for DGN V7
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: DGN V7 3D용 CAD 래스터화 옵션 구성
url: /ko/net/cad-features-and-support/support-of-3d-for-dgn-v7/
weight: 20
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DGN V7 3D용 CAD 래스터화 옵션 구성

## 소개

이 포괄적인 튜토리얼에서는 Aspose.CAD for .NET을 사용하여 3‑D DGN V7 파일을 PDF로 내보내기 위해 **CAD 래스터화 옵션을 구성하는 방법**을 배웁니다. CAD 뷰어, 보고서 도구, 자동 변환 파이프라인을 구축하든, 이러한 설정을 마스터하면 페이지 크기, 레이아웃 스케일링, 배경 색상 및 렌더링하려는 특정 뷰에 대한 정확한 제어가 가능합니다. 단계별로 과정을 살펴보겠습니다.

## 빠른 답변
- **“CAD 래스터화 옵션을 구성한다”는 의미는 무엇인가요?**  
  CAD 파일을 래스터 형식(예: PDF)으로 변환하기 전에 페이지 치수, 스케일링, 배경 색상 및 레이아웃 선택과 같은 속성을 설정하는 것을 의미합니다.
- **3‑D 지원으로 DGN을 PDF로 내보내는 방법?**  
  `DgnImage`로 DGN을 로드하고 `PdfOptions`와 `CadRasterizationOptions`를 정의한 뒤 `Save`를 호출합니다.
- **프로덕션 사용을 위해 라이선스가 필요합니까?**  
  예 – 배포를 위해서는 상용 라이선스가 필요합니다; 무료 체험판을 사용할 수 있습니다.
- **지원되는 .NET 버전은 무엇인가요?**  
  .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.
- **특정 뷰를 선택하여 내보낼 수 있나요?**  
  물론입니다 – 래스터화 옵션의 `Layouts` 배열을 설정하면 됩니다.

## “CAD 래스터화 옵션을 구성한다”는 무엇인가요?

CAD 래스터화 옵션을 구성한다는 것은 CAD 도면이 래스터화(벡터에서 비트맵 또는 PDF로 변환)되는 방식을 사용자 정의하는 것을 의미합니다. 이러한 설정을 조정하면 시각적 출력, 성능 및 최종 문서의 파일 크기를 제어할 수 있습니다.

## 3‑D DGN V7 내보내기에 Aspose.CAD를 사용하는 이유

- **Full .NET integration** – COM이나 네이티브 DLL이 필요 없습니다.  
- **Supports 3‑D geometry** – PDF로 렌더링할 때 깊이 정보를 유지합니다.  
- **Fine‑grained control** – 정확한 레이아웃, 스케일링 및 배경 색상을 선택할 수 있습니다.  
- **Cross‑platform** – .NET Core와 함께 Windows, Linux, macOS에서 작동합니다.

## 전제 조건

시작하기 전에 다음이 준비되어 있는지 확인하세요:

- **Aspose.CAD for .NET** – [here](https://releases.aspose.com/cad/net/)에서 다운로드합니다.  
- **Visual Studio** 또는 호환 가능한 .NET IDE.  
- **샘플 DGN 파일** – 이 가이드에서는 `Nikon_D90_Camera.dgn`(Aspose 샘플 팩에 포함)을 사용합니다.  

이제 모든 준비가 끝났으니, 코드로 들어가 보겠습니다.

## 네임스페이스 가져오기

.NET 프로젝트에서 필요한 네임스페이스를 가져옵니다:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Dgn;
using Aspose.CAD.ImageOptions;
```

## 단계 1: 문서 디렉터리 설정

소스 DGN과 출력 파일이 위치할 폴더를 가리키는 변수를 생성합니다.

```csharp
string MyDir = "Your Document Directory";
```

## 단계 2: DGN 파일 로드

`DgnImage`로 DGN 파일을 로드합니다. 이 객체를 통해 CAD 데이터와 래스터화 파이프라인에 접근할 수 있습니다.

```csharp
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";
string outFile = MyDir + "Nikon_D90_Camera.dgn";

using (DgnImage dgnImage = (DgnImage)Image.Load(sourceFilePath))
{
    // Your code for further processing goes here
}
```

## 단계 3: PDF 내보내기 옵션 구성 (CAD 래스터화 옵션 구성)

여기서 **CAD 래스터화 옵션**을 구성하여 3‑D 모델이 PDF에 어떻게 렌더링될지 지정합니다. 페이지 크기, 자동 레이아웃 스케일링, 배경 색상 및 내보낼 정확한 레이아웃(뷰)을 조정할 수 있습니다.

```csharp
var options = new PdfOptions
{
    VectorRasterizationOptions = new CadRasterizationOptions
    {
        PageWidth = 1500,
        PageHeight = 1500,
        AutomaticLayoutsScaling = true,
        BackgroundColor = Color.Black,
        Layouts = new string[] { "1", "2", "3", "9" } // Only export specified views
    }
};
```

## 단계 4: 래스터 이미지 저장

구성한 옵션을 사용하여 DGN을 PDF 파일로 내보냅니다.

```csharp
dgnImage.Save(outFile, options);
```

## 일반적인 문제 및 해결책

| 문제 | 해결책 |
|-------|----------|
| **빈 PDF 출력** | `Layouts` 배열에 DGN 파일에 존재하는 올바른 뷰 식별자가 포함되어 있는지 확인합니다. |
| **잘못된 색상** | `BackgroundColor`가 원하는 값으로 설정되어 있는지 확인합니다; 밝은 배경은 `Color.White`를 사용하세요. |
| **대용량 파일에서 성능 병목 현상** | `AutomaticLayoutsScaling`을 활성화하고, 더 작은 래스터 해상도를 위해 `PageWidth/PageHeight`를 줄이는 것을 고려하세요. |
| **라이선스 예외** | 이미지 로드 전에 유효한 Aspose.CAD 라이선스를 설치하여 체험판 워터마크를 방지합니다. |

## 자주 묻는 질문

**Q: Aspose.CAD for .NET를 다른 CAD 파일 형식과 함께 사용할 수 있나요?**  
A: 예, Aspose.CAD는 DWG, DXF, DWF, DGN 등 다양한 형식을 지원합니다.

**Q: Aspose.CAD를 사용할 때 예외를 어떻게 처리할 수 있나요?**  
A: 코드를 `try‑catch` 블록으로 감싸고 `Aspose.CAD.CADException`을 확인하여 자세한 오류 정보를 얻으세요.

**Q: Aspose.CAD는 상업 프로젝트에 적합한가요?**  
A: 물론입니다. 라이선스는 [here](https://purchase.aspose.com/buy)에서 구매할 수 있습니다.

**Q: 구매 전에 Aspose.CAD for .NET를 체험해볼 수 있나요?**  
A: 예, 무료 체험판은 [here](https://releases.aspose.com/)에서 제공됩니다.

**Q: Aspose.CAD에 대한 커뮤니티 지원을 어디서 찾을 수 있나요?**  
A: 토론 포럼은 [here](https://forum.aspose.com/c/cad/19)에서 확인하세요.

---

**Last Updated:** 2026-03-29  
**Tested With:** Aspose.CAD 24.11 for .NET  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}