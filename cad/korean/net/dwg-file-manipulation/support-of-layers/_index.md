---
date: 2026-04-09
description: C#와 Aspose.CAD for .NET을 사용하여 DWG 레이어를 내보내고, DWG 이미지를 변환하며, DWG JPEG를
  저장하는 방법을 배웁니다. 효율적인 CAD 파일 조작을 위한 단계별 가이드.
keywords:
- export dwg layers
- convert dwg image
- dwg layer visibility
- save dwg jpeg
linktitle: C#를 사용한 DWG 파일 레이어 처리
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: C#를 사용하여 DWG 레이어 내보내기 – Aspose.CAD 튜토리얼
url: /ko/net/dwg-file-manipulation/support-of-layers/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# C#를 사용한 DWG 레이어 내보내기 – Aspose.CAD 튜토리얼

## 소개

이 포괄적인 가이드에서는 C#와 Aspose.CAD 라이브러리를 사용하여 **DWG 레이어를 내보내는 방법**을 배웁니다. **DWG 이미지** 형식을 **변환**하거나 **DWG 레이어 가시성**을 제어하거나 단순히 **DWG JPEG** 파일을 **저장**해야 할 경우, 아래 단계가 효율적으로 수행하는 방법을 정확히 보여줍니다. 튜토리얼이 끝날 때쯤에는 특정 레이어를 분리하고 고품질 JPEG로 렌더링하는 실행 가능한 코드 스니펫을 얻게 됩니다.

## 빠른 답변

- **“export dwg layers”가 무엇을 의미하나요?** 이는 DWG 파일의 선택된 레이어를 JPEG 또는 PNG와 같은 이미지 형식으로 래스터화하는 것을 의미합니다.  
- **이 작업에 가장 적합한 라이브러리는 무엇인가요?** Aspose.CAD for .NET은 AutoCAD 없이도 완전한 기능을 제공합니다.  
- **여러 레이어를 한 번에 내보낼 수 있나요?** 예 – 레이어 이름 배열을 래스터화 옵션에 전달하면 됩니다.  
- **프로덕션 사용에 라이선스가 필요합니까?** 상업용 라이선스가 필요하며, 평가용 무료 체험판을 사용할 수 있습니다.  
- **지원되는 출력 형식은 무엇인가요?** JPEG, PNG, BMP, TIFF 및 ImageOptions 클래스를 통한 여러 다른 형식이 지원됩니다.  

## export dwg layers란 무엇인가요?

DWG 레이어를 내보낸다는 것은 DWG 도면 내의 하나 이상의 레이어에 속하는 벡터 데이터를 가져와 비트맵 이미지로 래스터화하는 것을 의미합니다. 전체 CAD 파일을 공개하지 않고 도면의 특정 부분만을 공유하고 싶을 때 유용합니다.

## DWG 레이어 가시성을 제어하는 이유는 무엇인가요?

레이어 가시성을 제어하면 다음을 할 수 있습니다:
- 프레젠테이션이나 문서화를 위한 깔끔한 시각 자산을 생성합니다.
- 필요한 기하학만 내보내어 파일 크기를 줄입니다.
- 기밀 레이어를 숨겨서 독점 설계 세부 정보를 보호합니다.

## 전제 조건

시작하기 전에 다음이 준비되어 있는지 확인하십시오:
- C# 프로그래밍 언어에 대한 기본 지식.
- 머신에 Visual Studio가 설치되어 있음.
- Aspose.CAD for .NET 라이브러리, [Aspose.CAD 웹사이트](https://releases.aspose.com/cad/net/)에서 다운로드할 수 있습니다.

## 네임스페이스 가져오기

시작하려면 래스터화 및 이미지 내보내기 기능에 접근할 수 있는 네임스페이스를 가져오세요.

```csharp
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
```

## 1단계: DWG 파일 로드

소스 DWG(또는 DWF) 파일을 `Image` 객체에 로드합니다. 이 객체는 메모리 내에서 전체 도면을 나타냅니다.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "for_layers_test.dwf";

using (Aspose.CAD.Image image = Aspose.CAD.Image.Load(sourceFilePath))
{
    // Your code for subsequent steps goes here
}
```

*왜 중요한가:* 파일을 한 번 로드하면 동일한 `image` 인스턴스를 여러 레이어별 내보내기에 재사용할 수 있어 성능이 향상됩니다.

## 2단계: 래스터화 옵션 구성

`CadRasterizationOptions` 인스턴스를 생성하여 Aspose.CAD에 도면을 어떻게 렌더링할지 지정합니다. 여기서는 내보낸 JPEG가 선명하도록 높은 해상도(1600 × 1600)를 설정합니다.

```csharp
Aspose.CAD.ImageOptions.CadRasterizationOptions rasterizationOptions = new Aspose.CAD.ImageOptions.CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
```

필요에 따라 배경 색상, 선 두께 스케일링 또는 안티앨리어싱 설정을 조정할 수도 있습니다.

## 3단계: 레이어 지정 (DWG 레이어 가시성)

**export dwg layers**를 위해 원하는 레이어를 추가합니다. 이 예제에서는 “LayerA”만 내보냅니다. 여러 레이어를 내보내려면 배열에 나열하기만 하면 됩니다.

```csharp
rasterizationOptions.Layers = new string[] { "LayerA" };
```

*팁:* 도면에 표시된 정확한 레이어 이름을 사용하세요; 레이어 이름은 대소문자를 구분합니다.

## 4단계: 이미지 내보내기 옵션 구성

생성하려는 이미지 형식을 선택합니다. JPEG는 품질과 파일 크기의 균형이 좋기 때문에 웹 미리보기를 위한 **save dwg jpeg** 파일에 이상적이므로 `JpegOptions`를 사용합니다.

```csharp
JpegOptions jpegOptions = new JpegOptions();
jpegOptions.VectorRasterizationOptions = rasterizationOptions;
```

**convert dwg image**를 PNG 또는 TIFF로 변환해야 하면 `JpegOptions`를 해당 옵션 클래스로 교체하십시오.

## 5단계: 내보낸 이미지 저장

출력 파일 경로를 정의하고 `Save`를 호출합니다. 래스터화 엔진은 제공한 레이어 목록을 존중하므로 최종 JPEG에 “LayerA”만 표시됩니다.

```csharp
MyDir = MyDir + "for_layers_test.jpg";
image.Save(MyDir, jpegOptions);
```

이 라인이 실행된 후에는 문서 디렉터리에서 `for_layers_test.jpg`를 찾을 수 있으며, 선택된 레이어만 포함됩니다.

## 일반적인 문제 및 해결책

| 문제 | 해결책 |
|-------|------------|
| **레이어 이름을 찾을 수 없음** | 원본 DWG에서 레이어의 정확한 철자와 대소문자를 확인하십시오. CAD 뷰어를 사용하여 레이어 이름을 나열하세요. |
| **빈 출력 이미지** | 래스터화 옵션에 투명하지 않은 배경이 설정되어 있는지, 선택한 레이어에 실제로 기하학이 포함되어 있는지 확인하십시오. |
| **저해상도 출력** | `PageWidth`와 `PageHeight`를 늘리거나 `CadRasterizationOptions`에서 `Resolution`을 설정하십시오. |
| **지원되지 않는 DWG 버전** | 최신 Aspose.CAD 버전으로 업데이트하십시오; 최신 AutoCAD 릴리스를 지원합니다. |

## 자주 묻는 질문

### Q1: 동시에 여러 레이어를 처리할 수 있나요?
예, 가능합니다. 레이어 이름을 `rasterizationOptions.Layers` 배열에 추가하기만 하면 됩니다.

### Q2: Aspose.CAD 체험판을 사용할 수 있나요?
예, [here](https://releases.aspose.com/)에서 무료 체험판을 받을 수 있습니다.

### Q3: 문서는 어디에서 찾을 수 있나요?
문서는 [here](https://reference.aspose.com/cad/net/)에서 확인할 수 있습니다.

### Q4: Aspose.CAD 지원은 어떻게 받을 수 있나요?
[Aspose.CAD 포럼](https://forum.aspose.com/c/cad/19)에서 지원을 받을 수 있습니다.

### Q5: Aspose.CAD 라이선스 옵션은 무엇인가요?
[here](https://purchase.aspose.com/buy)에서 라이선스 옵션 및 구매 세부 정보를 확인할 수 있습니다.

**추가 Q&A**

**Q: 도면을 JPEG 대신 PNG로 내보낼 수 있나요?**  
A: 물론 가능합니다. `JpegOptions`를 `PngOptions`로 교체하고 파일 확장자를 적절히 조정하십시오.

**Q: 라이브러리가 선 스타일과 색상을 보존하나요?**  
A: 예. 모든 벡터 속성이 래스터화 과정에서 충실히 렌더링됩니다.

---

**마지막 업데이트:** 2026-04-09  
**테스트 환경:** Aspose.CAD for .NET (latest release)  
**작성자:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}