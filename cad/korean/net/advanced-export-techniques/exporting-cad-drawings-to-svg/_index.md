---
date: 2026-03-07
description: Aspose.CAD for .NET를 사용하여 CAD를 SVG로 내보내는 방법, SVG 색상을 사용자 지정하는 방법, 그리고
  DWG를 효율적으로 SVG로 변환하는 방법을 배워보세요.
linktitle: Exporting CAD Drawings to SVG Format
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: CAD를 SVG로 내보내기 – CAD 도면을 SVG 형식으로 내보내기 - Aspose.CAD 가이드
url: /ko/net/advanced-export-techniques/exporting-cad-drawings-to-svg/
weight: 15
---

07  
**Tested With:** Aspose.CAD for .NET 24.12  
**Author:** Aspose  

Translate labels but keep dates.

"**마지막 업데이트:** 2026-03-07" etc.

Then closing shortcodes.

Make sure to keep all shortcodes exactly.

Now produce final content.

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# CAD를 SVG로 내보내기 – CAD 도면을 SVG 형식으로 내보내기

## 소개

CAD 도면을 SVG로 내보내는 것은 웹 페이지, 보고서 또는 인터랙티브 시각화에 해상도에 독립적인 그래픽이 필요할 때 흔히 요구되는 작업입니다. 이 튜토리얼에서는 Aspose.CAD for .NET을 사용해 **CAD를 SVG로 내보내는 방법**을 배우고, **SVG 색상 사용자 정의** 옵션을 탐색하며, 몇 줄의 코드만으로 **DWG를 SVG로 변환**(또는 DXF를 SVG로 변환)하는 방법을 확인합니다. 단계는 빠르고, API는 직관적이며, 생성된 SVG 파일은 모든 장치에서 완벽하게 스케일됩니다.

## 빠른 답변
- **변환을 담당하는 라이브러리는 무엇인가요?** Aspose.CAD for .NET.  
- **색상 모드를 변경할 수 있나요?** 예 – `SvgColorMode`를 사용해 그레이스케일, 흑백, 전체 색상 중 선택할 수 있습니다.  
- **지원되는 CAD 형식은 무엇인가요?** DWG, DXF 및 기타 다수 (Aspose.CAD 문서 참고).  
- **개발에 라이선스가 필요합니까?** 테스트용 임시 라이선스를 사용할 수 있습니다.  
- **변환에 얼마나 걸리나요?** 일반 도면은 보통 1초 이하입니다.

## “CAD를 SVG로 내보내기”란 무엇인가요?
CAD를 SVG로 내보낸다는 것은 DWG 또는 DXF와 같은 네이티브 CAD 파일을 Scalable Vector Graphics 형식으로 렌더링하는 것을 의미합니다. SVG는 XML 기반이며 가볍고 CSS로 스타일링할 수 있어 현대 웹 및 모바일 애플리케이션에 이상적입니다.

## 왜 Aspose.CAD를 사용해 CAD를 SVG로 내보내나요?
- **외부 종속성 없음** – 순수 .NET API이며 AutoCAD 설치가 필요 없습니다.  
- **세밀한 제어** – **SVG 색상을 사용자 정의**하고, 텍스트를 도형으로 유지할지 결정하고, 래스터화 옵션을 선택할 수 있습니다.  
- **광범위한 형식 지원** – 동일한 코드로 **DWG를 SVG로 변환**, **DXF를 SVG로 변환** 및 기타 형식을 처리할 수 있어 코드베이스가 단순해집니다.  
- **고성능** – 속도와 낮은 메모리 사용량에 최적화되어 배치 처리에 적합합니다.

## 사전 요구 사항

시작하기 전에 다음이 준비되어 있는지 확인하십시오:

- **Aspose.CAD for .NET**가 설치되어 있어야 합니다. 라이브러리는 [here](https://releases.aspose.com/cad/net/)에서 다운로드할 수 있습니다.  
- .NET 개발 환경 (Visual Studio, Rider, 또는 .NET CLI).  
- 변환하려는 CAD 파일 (DWG 또는 DXF).

## 네임스페이스 가져오기

먼저 프로젝트에 필요한 네임스페이스를 추가하여 클래스를 사용할 수 있도록 합니다.

```csharp
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## 단계별 가이드

### 단계 1: 문서 디렉터리 설정  
소스 CAD 파일이 위치한 폴더와 SVG 출력이 저장될 폴더를 정의합니다.

```csharp
// The path to the documents directory.
string MyDir = "Your Document Directory";
```

### 단계 2: CAD 도면 로드  
`Image.Load`를 사용해 DWG(또는 DXF) 파일을 읽습니다. 이는 **load DWG .NET** 시나리오에 적용됩니다.

```csharp
using (Image image = Image.Load(MyDir + "sample.dwg"))
{
```

### 단계 3: SVG 내보내기 옵션 구성  
출력 요구에 맞게 내보내기 설정을 조정합니다. 여기서는 색상 모드를 그레이스케일로 설정하고 모든 텍스트를 벡터 도형으로 강제 변환합니다.

```csharp
    var options = new SvgOptions();
    options.ColorType = SvgColorMode.Grayscale;   // customize SVG color mode
    options.TextAsShapes = true;                  // ensures text appears as shapes
```

### 단계 4: SVG 파일 저장  
마지막으로 SVG 파일을 디스크에 기록합니다. 이 단계는 **CAD를 SVG로 저장**하고 변환을 완료합니다.

```csharp
    image.Save(MyDir + "sample.svg", options);
}
```

이 네 단계만 따르면 **DWG를 SVG로 변환**(또는 **DXF를 SVG로 변환**)을 전체 출력 모양을 완벽히 제어하면서 수행할 수 있습니다.

## 일반적인 문제 및 해결책

| 문제 | 원인 | 해결 방법 |
|------|------|-----------|
| **빈 SVG 출력** | 소스 파일 경로가 잘못되었거나 파일이 손상되었습니다. | `MyDir`을 확인하고 CAD 파일이 오류 없이 열리는지 확인하십시오. |
| **색상이 잘못 표시됨** | `SvgColorMode`가 실수로 그레이스케일로 설정되었습니다. | `options.ColorType`을 `SvgColorMode.FullColor`로 변경하여 원래 색상을 유지하십시오. |
| **텍스트 누락** | `TextAsShapes`가 `false`로 설정되어 있고 뷰어가 내장 폰트를 지원하지 않습니다. | `TextAsShapes = true`로 유지하거나 SVG에 필요한 폰트를 포함하십시오. |

## FAQ

### Q1: Aspose.CAD가 모든 CAD 형식과 호환되나요?
A1: Aspose.CAD는 DWG와 DXF를 포함한 다양한 CAD 형식을 지원하여 폭넓은 호환성을 제공합니다.

### Q2: SVG로 내보낼 때 색상 모드를 사용자 정의할 수 있나요?
A2: 예, Aspose.CAD를 사용하면 색상 모드를 선택할 수 있어 출력에 유연성을 제공합니다.

### Q3: 테스트용 임시 라이선스를 받을 수 있나요?
A3: 예, 평가용 임시 라이선스를 [here](https://purchase.aspose.com/temporary-license/)에서 얻을 수 있습니다.

### Q4: Aspose.CAD에 대한 자세한 문서는 어디서 찾을 수 있나요?
A4: 문서는 [here](https://reference.aspose.com/cad/net/)에서 확인할 수 있습니다.

### Q5: Aspose.CAD와 관련된 지원이나 질문은 어디에 문의하나요?
A5: 지원 및 토론은 커뮤니티 포럼 [here](https://forum.aspose.com/c/cad/19)에서 확인하십시오.

## 자주 묻는 질문

**Q: 이 코드를 .NET Core 또는 .NET 6에서 사용할 수 있나요?**  
A: 물론입니다. Aspose.CAD for .NET은 .NET Framework, .NET Core 및 .NET 5/6+와 호환됩니다.

**Q: 특정 레이아웃이나 레이어만 내보낼 수 있나요?**  
A: 가능합니다. `SvgOptions`를 사용해 `PageIndex`를 설정하거나 저장 전에 레이어를 필터링하십시오.

**Q: 생성된 SVG에 사용자 정의 CSS 스타일을 삽입하려면 어떻게 해야 하나요?**  
A: 저장 후 SVG XML을 후처리하여 `<style>` 요소를 삽입하거나, 최신 버전에서 제공되는 경우 `options.CustomCss`를 사용할 수 있습니다.

**Q: 원본 CAD 파일의 크기 제한이 있나요?**  
A: 라이브러리는 큰 파일도 처리하지만 복잡도가 높을수록 메모리 사용량이 증가합니다. 매우 큰 도면의 경우 페이지별로 처리하는 것을 고려하십시오.

**Q: 변환 시 선 굵기와 선 종류가 유지되나요?**  
A: 기본적으로 선 굵기는 유지됩니다. 보다 세밀한 제어가 필요하면 `SvgOptions`의 렌더링 옵션을 조정하십시오.

---

**마지막 업데이트:** 2026-03-07  
**테스트 환경:** Aspose.CAD for .NET 24.12  
**작성자:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}