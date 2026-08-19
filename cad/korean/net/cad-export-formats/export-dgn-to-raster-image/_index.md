---
date: 2026-03-24
description: Aspose.CAD for .NET를 사용하여 dgn을 png로 변환하고 CAD를 jpeg로 저장하는 방법을 배우세요 – CAD를
  이미지로 변환하는 빠른 가이드.
linktitle: Export DGN to Raster Image
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Aspose.CAD for .NET에서 DGN을 PNG로 변환하는 방법
url: /ko/net/cad-export-formats/export-dgn-to-raster-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD for .NET에서 DGN을 PNG로 변환하기

현대 .NET 개발에서 **convert dgn to png**는 웹에 CAD 도면을 표시하거나 보고서에 삽입해야 할 때 흔히 요구되는 작업입니다. Aspose.CAD for .NET은 몇 줄의 코드만으로 DGN 파일을 고품질 래스터 이미지로 손쉽게 변환할 수 있도록 해줍니다. 이 가이드에서는 프로젝트 설정부터 최종 PNG(또는 JPEG) 파일 저장까지 전체 과정을 단계별로 안내합니다.

## Quick Answers
- **Aspose.CAD로 DGN을 PNG로 변환할 수 있나요?** 예 – 래스터화 옵션을 설정하고 PNG 또는 JPEG 출력을 선택하면 됩니다.  
- **프로덕션 사용에 라이선스가 필요합니까?** 비시험 배포에는 유효한 Aspose.CAD 라이선스가 필요합니다.  
- **지원되는 .NET 버전은 무엇인가요?** .NET Framework 4.6 이상, .NET Core 3.1 이상, .NET 5/6/7.  
- **사용 가능한 이미지 형식은 무엇인가요?** PNG, JPEG, BMP, GIF, TIFF 등.  
- **예외 처리가 필요합니까?** 물론입니다 – 파일 접근 문제를 처리하기 위해 변환 코드를 try/catch로 감싸세요.

## “convert dgn to png”란?
DGN(MicroStation) 파일을 PNG로 변환한다는 것은 벡터 CAD 데이터를 픽셀 기반 이미지로 래스터화하는 것을 의미합니다. 이는 미리보기 생성, HTML 이메일에 도면 삽입, 문서 관리 시스템용 썸네일 제작 등에 유용합니다.

## 왜 Aspose.CAD를 CAD → 이미지 변환에 사용하나요?
- **외부 종속성 없음** – 순수 관리 코드만으로 동작합니다.  
- **고충실도** – 선 굵기, 레이어, 색상을 정확히 보존합니다.  
- **유연한 출력** – PNG, JPEG, BMP 등 하나의 옵션만 바꾸면 다양한 포맷으로 저장할 수 있습니다.  
- **성능 최적화** – 대형 도면도 빠르게 래스터화됩니다.

## Prerequisites

시작하기 전에 다음이 준비되어 있는지 확인하세요:

- **Aspose.CAD for .NET**이 프로젝트에 설치되어 있어야 합니다. [웹사이트](https://reference.aspose.com/cad/net/)에서 다운로드할 수 있습니다.  
- 알려진 디렉터리에 샘플 DGN 파일(예: `Nikon_D90_Camera.dgn`)이 있어야 합니다.

## Import Namespaces

필요한 `using` 문을 추가하여 Aspose.CAD 클래스를 사용할 수 있게 합니다.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Step 1: Load the DGN File

소스 DGN을 `CadImage` 객체에 로드합니다. 이 객체는 메모리 상의 CAD 도면을 나타내며 래스터화의 원본이 됩니다.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Your code for further processing goes here
}
```

## Step 2: Define Rasterization Options

CAD 도면을 어떻게 래스터화할지 설정합니다. 여기서 이미지 크기, 스케일링, 배경 색 등을 제어할 수 있습니다.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 600;
rasterizationOptions.PageHeight = 300;
rasterizationOptions.NoScaling = true;
rasterizationOptions.AutomaticLayoutsScaling = false;
```

## Step 3: Choose the Output Format (PNG or JPEG)

튜토리얼은 PNG에 초점을 맞추지만 **save cad as jpeg**도 가능합니다. 적절한 이미지 옵션 객체를 생성하고 래스터화 설정을 연결합니다.

```csharp
ImageOptionsBase options = new JpegOptions();   // Change to PngOptions() for PNG output
options.VectorRasterizationOptions = rasterizationOptions;
```

> **Pro tip:** PNG 파일을 생성하려면 `new JpegOptions()`를 `new PngOptions()`로 교체하세요.

## Step 4: Save the Raster Image

마지막으로 `CadImage` 인스턴스의 `Save` 메서드를 호출하고 원하는 파일 이름과 앞서 구성한 옵션 객체를 전달합니다.

```csharp
cadImage.Save(MyDir + "ExportDGNToRasterImage_out.jpg", options);
```

`PngOptions`로 전환하면 파일이 `ExportDGNToRasterImage_out.png`로 저장됩니다.

## Common Issues and Solutions

| Issue | Cause | Fix |
|-------|-------|-----|
| **Blank output image** | `NoScaling` 설정이 잘못되었거나 레이아웃이 선택되지 않음 | `AutomaticLayoutsScaling = true`로 설정하거나 원하는 레이아웃을 지정하세요. |
| **Out‑of‑memory for large files** | 스트리밍 없이 큰 DGN을 로드 | `Image.Load(sourceFilePath, new LoadOptions { LoadOnDemand = true })`를 사용하세요. |
| **Unsupported DGN version** | 오래된 MicroStation 버전 | 레거시 포맷을 지원하는 최신 Aspose.CAD 버전을 사용하세요. |

## Frequently Asked Questions

**Q: DGN 파일을 JPEG 외의 포맷으로도 내보낼 수 있나요?**  
A: 예, Aspose.CAD for .NET은 PNG, BMP, GIF, TIFF 등 다양한 포맷을 지원합니다 – 옵션 클래스(`new PngOptions()` 등)만 교체하면 됩니다.

**Q: 변환 중 예외는 어떻게 처리해야 하나요?**  
A: 변환 코드를 `try/catch` 블록으로 감싸고 `Aspose.CAD.CadException`을 로깅하여 상세 오류 정보를 확인하세요.

**Q: Aspose.CAD for .NET의 체험판 버전이 있나요?**  
A: 예, 무료 체험판을 이용해 제품을 살펴볼 수 있습니다. 자세한 내용은 [여기](https://releases.aspose.com/)에서 확인하세요.

**Q: Aspose.CAD for .NET 관련 지원이나 토론을 어디서 할 수 있나요?**  
A: 커뮤니티 지원 및 토론은 [Aspose.CAD 포럼](https://forum.aspose.com/c/cad/19)에서 진행됩니다.

**Q: Aspose.CAD for .NET 임시 라이선스를 어떻게 얻나요?**  
A: 개발 필요에 맞는 임시 라이선스는 [이 링크](https://purchase.aspose.com/temporary-license/)에서 발급받을 수 있습니다.

## Conclusion

이제 Aspose.CAD for .NET을 사용해 **convert dgn to png**(또는 JPEG) 방법을 익혔습니다. 래스터화 옵션을 조정하고 이미지 옵션 클래스를 교체하면 프로젝트 요구에 맞는 출력을 손쉽게 만들 수 있습니다. 다양한 페이지 크기, DPI 설정, 파일 포맷을 실험해 보면서 최적의 래스터 이미지를 얻어 보세요.

---

**Last Updated:** 2026-03-24  
**Tested With:** Aspose.CAD 24.11 for .NET  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}