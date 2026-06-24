---
date: 2026-03-29
description: Aspose.CAD for .NET를 사용하여 DGN을 JPEG로 변환하는 방법을 배우고, DGN V7을 완벽히 지원하며 CAD를
  래스터 이미지로 쉽게 변환할 수 있습니다.
linktitle: Support for DGN V7
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Aspose.CAD for .NET – V7 지원으로 DGN을 JPEG로 변환
url: /ko/net/cad-features-and-support/support-for-dgn-v7/
weight: 19
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DGN을 JPEG로 변환하기 – Aspose.CAD for .NET – V7 지원

## 소개

이 튜토리얼에서는 Aspose.CAD for .NET을 사용하여 **DGN을 JPEG로 변환**하는 방법을 배우게 됩니다. 이 라이브러리는 전체 DGN V7 지원을 제공하므로 이를 활용할 수 있습니다. DGN 파일을 JPEG와 같은 래스터 이미지로 변환하는 것은 CAD 도면을 웹 페이지, 모바일 앱 또는 보고서 도구에 삽입해야 할 때 흔히 요구되는 작업입니다. Aspose.CAD는 또한 **CAD를 래스터** 형식으로 효율적으로 변환할 수 있어 설계 데이터를 표시하는 방식에 유연성을 제공합니다.

## 빠른 답변
- **이 튜토리얼은 무엇을 다루나요?** Aspose.CAD for .NET을 사용하여 DGN V7 파일을 JPEG 래스터 이미지로 변환합니다.  
- **필요한 라이브러리 버전은?** DGN V7 지원이 포함된 최신 Aspose.CAD for .NET 릴리스라면 모두 사용 가능합니다.  
- **라이선스가 필요합니까?** 개발에는 무료 체험판을 사용할 수 있으며, 운영 환경에서는 상용 라이선스가 필요합니다.  
- **출력 크기를 변경할 수 있나요?** 예 – 래스터화 옵션을 통해 페이지 너비, 높이 및 스케일을 설정할 수 있습니다.  
- **JPEG만 출력 형식인가요?** 아니요 – Aspose.CAD는 PNG, BMP, TIFF 등 다양한 래스터 형식을 지원합니다.

## DGN V7이란?
DGN(Design)은 Bentley Systems에서 MicroStation용으로 처음 만든 파일 형식입니다. 버전 7은 더 풍부한 기하학 및 메타데이터를 제공하여 토목·인프라 프로젝트에서 많이 사용됩니다. Aspose.CAD for .NET은 DGN V7 파일을 직접 읽을 수 있으며, 해당 내용을 `CadImage` 객체로 노출하여 래스터화하거나 다른 형식으로 변환할 수 있습니다.

## 왜 DGN을 JPEG로 변환하나요?
- **웹 친화적:** JPEG 이미지는 가볍고 브라우저에서 별도의 플러그인 없이 즉시 표시됩니다.  
- **크로스 플랫폼:** JPEG는 모든 기기에서 볼 수 있어 비전문가와 CAD 도면을 공유하기에 이상적입니다.  
- **간소화된 워크플로:** 래스터 형식으로 변환하면 후속 프로세스에서 CAD 전용 뷰어가 필요 없게 됩니다.

## 사전 요구 사항

구현에 들어가기 전에 다음 항목을 준비하십시오:

- **Aspose.CAD for .NET** – [website](https://releases.aspose.com/cad/net/)에서 다운로드하십시오.  
- **개발 환경** – Visual Studio(또는 .NET을 지원하는 IDE).

이 항목들을 준비하면 중단 없이 단계별로 진행할 수 있습니다.

## 네임스페이스 가져오기

먼저 CadImage 처리와 래스터화를 위해 필요한 네임스페이스를 가져옵니다.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## 1단계: DGN 파일 로드

`CadImage` 객체에 원본 DGN 파일을 로드합니다. 자리표시자 경로를 DGN 파일이 있는 폴더 경로로 교체하십시오.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Subsequent steps will be placed here.
}
```

## 2단계: 래스터화 옵션 구성

DGN 도면을 어떻게 래스터화할지 정의합니다. 출력 크기와 스케일 동작을 제어할 수 있습니다.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions
{
    PageWidth = 600,
    PageHeight = 300,
    NoScaling = true,
    AutomaticLayoutsScaling = false
};
```

## 3단계: 벡터 래스터화 옵션 설정

`JpegOptions` 객체(또는 다른 래스터 형식 옵션)를 생성하고 래스터화 설정을 연결합니다.

```csharp
ImageOptionsBase options = new JpegOptions
{
    VectorRasterizationOptions = rasterizationOptions
};
```

## 4단계: 래스터화된 이미지 저장

마지막으로 `Save` 메서드를 사용하여 DGN 도면을 JPEG 파일로 내보냅니다.

```csharp
cadImage.Save(MyDir + "ExportDGNToRasterImage_out.jpeg", options);
```

코드가 성공적으로 실행되면 지정한 폴더에 원본 DGN V7 도면의 JPEG 표현이 저장됩니다.

## 일반적인 문제 및 해결책

| 문제 | 해결책 |
|-------|----------|
| **파일을 찾을 수 없음** | `MyDir`이 경로 구분자(`\\` 또는 `/`)로 끝나는지, 파일 이름이 올바른지 확인하십시오. |
| **빈 출력 이미지** | `NoScaling`이 적절히 설정되었는지 확인하십시오; 페이지를 전체 채우려면 `false`로 설정하십시오. |
| **지원되지 않는 엔터티** | Aspose.CAD는 대부분의 DGN 엔터티를 지원하지만, 매우 오래되었거나 사용자 정의 객체는 무시될 수 있습니다. 경고는 변환 로그를 확인하십시오. |

## 자주 묻는 질문

### Q1: Aspose.CAD가 최신 DGN V7 사양과 호환되나요?
**A:** 예, Aspose.CAD는 DGN V7을 완벽히 지원하며 최신 표준에 따라 기하학 및 메타데이터를 처리합니다.

### Q2: DGN 파일 변환을 위한 래스터화 옵션을 맞춤 설정할 수 있나요?
**A:** 물론입니다. `CadRasterizationOptions` 클래스를 사용하면 페이지 크기, 스케일링, 선 두께, 배경 색상 등을 조정할 수 있습니다.

### Q3: JPEG 외에 지원되는 다른 출력 형식이 있나요?
**A:** 예, Aspose.CAD는 PNG, BMP, TIFF 등 여러 래스터 형식으로 내보낼 수 있습니다. 해당 `*Options` 클래스(e.g., `PngOptions`)를 사용하면 됩니다.

### Q4: Aspose.CAD 관련 질문에 대한 도움을 어떻게 받을 수 있나요?
**A:** 커뮤니티 지원 및 공식 답변을 위해 [Aspose.CAD forum](https://forum.aspose.com/c/cad/19)을 방문하십시오.

### Q5: Aspose.CAD for .NET의 무료 체험판이 있나요?
**A:** 예, [here](https://releases.aspose.com/)에서 체험판을 다운로드할 수 있습니다.

---

**마지막 업데이트:** 2026-03-29  
**테스트 환경:** Aspose.CAD 24.12 for .NET  
**작성자:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}